---
title: Nasazení jednotek škálování hraniční sítě na vlastní hardware pomocí LBD
description: Toto téma vysvětluje, jak zřídit místní jednotky škálování hrany pomocí vlastního hardwaru a nasazení, které je založeno na místních obchodních datech (LBD).
author: cabeln
ms.date: 11/29/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 2407d4e3c6adaf5df2e8f5440ee8336f86012caf
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920666"
---
# <a name="deploy-edge-scale-units-on-custom-hardware-using-lbd"></a>Nasazení jednotek škálování hraniční sítě na vlastní hardware pomocí LBD

[!include [banner](../includes/banner.md)]

Jednotky škálování hrany hrají důležitou roli v distribuované hybridní topologii pro správu dodavatelského řetězce. V hybridní topologii můžete rozdělit pracovní zátěže mezi vaše cloudové centrum Supply Chain Management a další jednotky škálování v cloudu nebo na hraně.

Jednotky škálování hrany lze nasadit vytvořením [místního prostředí](../../fin-ops-core/dev-itpro/deployment/on-premises-deployment-landing-page.md) místních obchodních dat (LBD) a poté je nakonfigurovat tak, aby fungovaly jako jednotka škálování ve vaší distribuované hybridní topologii pro správu dodavatelského řetězce. Toho je dosaženo propojením místního prostředí LBD s prostředím Supply Chain Management v cloudu, které bylo nakonfigurováno tak, aby fungovalo jako centrum.  

Toto téma popisuje, jak nastavit místní prostředí LBD jako jednotku škálování hrany a pak ji přidružit k centru.

## <a name="deployment-overview"></a>Přehled nasazení

Zde je přehled kroků nasazení.

1. **Povolte slot LBD ve svém projektu LBD v Microsoft Dynamics Lifecycle Services (LCS).**

1. **Nastavte a nasaďte prostředí LBD s *prázdnou* databází.**

    Použijte LCS k nasazení prostředí LBD s nejnovější topologií a prázdnou databází. Pro více informací viz část [Nastavení a nasazení prostředí LBD s prázdnou databází](#set-up-deploy) dále v tomto tématu. Musíte používat Supply Chain Management verze 10.0.21 s nebo vyšší v prostředích center a jednotek škálování.

1. **Nahrajte cílové balíčky do prostředků projektu LBD v LCS.**

    Připravte si balíčky aplikací, platformy a přizpůsobení, které použijete v centru a jednotce škálování hran. Pro více informací viz část [Nahrání cílových balíčků do prostředků projektu LBD v LCS](#upload-packages) dále v tomto tématu.

1. **Obsluhujte prostředí LBD pomocí cílových balíčků.**

    Tento krok zajistí, že na centru i paprsku bude nasazeno stejné sestavení a přizpůsobení. Pro více informací viz část [Obsluha prostředí LBD pomocí cílových balíčků](#service-target-packages) dále v tomto tématu.

1. **Dokončete konfiguraci jednotky škálování a přiřazení pracovní zátěže.**

    Pro více informací viz část [Přiřazení jednotky škálování hrany LBD k centru](#assign-edge-to-hub) dále v tomto tématu.

Zbývající části tohoto tématu poskytují podrobnější informace o tom, jak provést tyto kroky.

## <a name="set-up-and-deploy-an-lbd-environment-with-an-empty-database"></a><a name="set-up-deploy"></a>Nastavte a nasaďte prostředí LBD s prázdnou databází

Tento krok vytvoří funkční prostředí LBD. Prostředí však nemusí mít nutně stejnou verzi aplikace a platformy jako prostředí centra. Kromě toho stále chybí přizpůsobení a ještě nebylo povoleno, aby fungovalo jako jednotka škálování.

1. Postupujte podle pokynů v části [Nastavení a nasazení místních prostředí (Platform Update 41 a novější)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md). Musíte používat Supply Chain Management verze 10.0.21 s nebo vyšší v prostředích center a jednotek škálování. Kromě toho musíte použít skripty infrastruktury verze 2.12.0 nebo novější. 

    > [!IMPORTANT]
    > Přečtěte si zbytek této části **před** provedením kroků v tomto tématu.

1. Než popíšete svou konfiguraci v souboru infrastructure\\ConfigTemplate.xml, spusťte následující skript:

    ```powershell
    .\Configure-ScriptsForEdgeScaleUnits.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > Tento skript odstraní veškerou konfiguraci, která není potřeba pro nasazení jednotek škálování hrany.

1. Nastavte databázi, která obsahuje prázdná data, jak je popsáno v části [Konfigurace databází](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb). Pro tento krok použijte prázdný soubor data.bak.
1. Poté, co dokončíte [Konfiguraci databází](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb), spusťte následující skript pro konfiguraci databáze Scale Unit Alm Orchestrator.

    > [!NOTE]
    > Nekonfigurujte databázi Financial Reporting během [Konfigurace databází](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb).

    ```powershell
    .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName EdgeScaleUnit
    ```

    Skript Initialize-Database.ps1 provádí následující akce:

    1. Vytvořte prázdnou databázi s názvem **ScaleUnitAlmDb**.
    2. Mapujte uživatele na databázové role na základě následující tabulky.

        | Uživatel            | Typ | Role databáze |
        |-----------------|------|---------------|
        | svc-LocalAgent$ | gMSA | db\_owner     |

1. Dále postupujte podle pokynů v části [Nastavení a nasazení místních prostředí (Platform Update 41 a novější)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md).
1. Poté, co dokončíte krok [Nakonfigurujte AD FS](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb), postupujte takto:

    1. Vytvořte novou aplikaci Active Directory Federation Services (AD FS), která umožní službě Alm Orchestration komunikovat s vaším aplikačním objektovým serverem (AOS).

        ```powershell
        # Host URL is your DNS record\host name for accessing the AOS
        .\Create-ADFSServerApplicationForEdgeScaleUnits.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -HostUrl 'https://ax.d365ffo.onprem.contoso.com'
        ```

    1. Vytvořte novou aplikaci Azure Active Directory (Azure AD), která umožní službě Alm Orchestration komunikovat se službou Scale Unit Management.

        ```powershell
        # Example .\Create-SumAADApplication.ps1 -ConfigurationFilePath ..\ConfigTemplate.xml -TenantId '6240a19e-86f1-41af-91ab-dbe29dbcfb95' -ApplicationDisplayName 'EdgeAgent-SUMCommunication-EN01'
        .\Create-SumAADApplication.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                       -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                       -ApplicationDisplayName '<Whichever name you want the Azure AD app to have>'
        ```

1. Dále postupujte podle pokynů v části [Nastavení a nasazení místních prostředí (Platform Update 41 a novější)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md). Když musíte zadat konfiguraci pro místního agenta, ujistěte se, že jste povolili funkce Edge Scale Unit a poskytli všechny požadované parametry.

    ![Povolení funkcí Edge Scale Unit.](media/EnableEdgeScaleUnitFeatures.png "Povolení funkcí Edge Scale Unit.")

1. Před nasazením prostředí z LCS nastavte skript před nasazením. Další informace viz [Předběžné nasazení místního agenta a skripty po nasazení](../../fin-ops-core/dev-itpro/lifecycle-services/pre-post-scripts.md).

    1. Zkopírujte skript Configure-CloudAndEdge.ps1 ze složky **Jednotka škálování** v **Skripty infrastruktury** do složky **Skripty** ve sdílené složce úložiště souborů agenta, která byla nastavena v prostředí. Typická cesta je \\\\lbdiscsi01\\agent\\Scripts.
    2. Vytvořte skript **PreDeployment.ps1**, který bude volat skripty pomocí požadovaných parametrů. Skript před nasazením musí být vložen do služky **Skripty** ve sdílené složce úložiště souborů agenta. Jinak nelze spustit. Typická cesta je \\\\lbdiscsi01\\agent\\Scripts\\PreDeployment.ps1.

        Obsah skriptu PreDeployment.ps1 bude připomínat následující příklad.

        ```powershell
        $agentShare = '\\lbdiscsi01\agent'
        
        Write-Output "AgentShare is set to $agentShare" 
        . $PSScriptRoot\Configure-CloudAndEdge.ps1 -AgentShare $agentShare -InstanceId '@A'
        ```

        > [!NOTE]
        > Parametr InstanceId smí obsahovat pouze dva znaky. První znak je @ a druhý může být jakékoli velké písmeno v anglické abecedě.
        >
        > - Platné hodnoty:
        >   - @D
        >   - @X
        > - Neplatné hodnoty:
        >   - @a
        >   - @4
        >   - @#

1. Nasaďte prostředí pomocí nejnovější základní topologie, která je k dispozici.
1. Po nasazení prostředí svého postupujte takto:

    1. Spusťte následující příkazy SQL ve vaší obchodní databázi (AXDB).

        ```sql
        ALTER TABLE dbo.NUMBERSEQUENCETABLE ENABLE CHANGE_TRACKING WITH (TRACK_COLUMNS_UPDATED = ON)
        delete from NumberSequenceTable
        delete from NumberSequenceReference
        delete from NumberSequenceScope
        delete from FeatureManagementMetadata
        delete from FeatureManagementState
        delete from SysFeatureStateV0
        ```

    1. Zvyšte souběžnou maximální dávkovou relaci na hodnotu vyšší než 4.

        ```sql
        Update batchserverconfig set maxbatchsessions = '<Replace with number of concurrent batch tasks you want>'
        ```

    1. Ověřte, že ve vaší obchodní databázi (AXDB) bylo povoleno sledování změn.

        1. Spusťte aplikaci SQL Server Management Studio (SSMS).
        1. Vyberte a podržte svoji obchodní databázi (AXDB) (nebo klikněte pravým tlačítkem) a vyberte možnost **Vlastnosti**.
        1. V okně, které se objeví, vyberte **Sledování změn** a pak nastavte následující hodnoty:

            - **Change Tracking:** *True*
            - **Retention Period:** *7*
            - **Retention Units:** *Days*
            - **Auto Cleanup:** *True*

    1. Přidejte ID aplikace AD FS, které jste vytvořili dříve (pomocí skriptu Create-ADFSServerApplicationForEdgeScaleUnits.ps1) do tabulky aplikací Azure AD ve vaší jednotce škálování. Tento krok můžete dokončit ručně prostřednictvím uživatelského rozhraní (UI). Případně jej můžete dokončit prostřednictvím databáze pomocí následujícího skriptu.

        ```sql
        DECLARE @ALMOrchestratorId NVARCHAR(76) = '<Replace with the ADFS Application ID created in a previous step>';

        IF NOT EXISTS (SELECT TOP 1 1 FROM SysAADClientTable WHERE AADClientId = @ALMOrchestratorId)
        BEGIN
            INSERT INTO SysAADClientTable (AADClientId, UserId, Name, ModifiedBy, CreatedBy)
            VALUES (@ALMOrchestratorId, 'ScaleUnitManagement', 'Scale Unit Management', 'Admin', 'Admin');
        END
        ```

## <a name="set-up-an-azure-key-vault-and-an-azure-ad-application-to-enable-communication-between-scale-units"></a><a name="set-up-keyvault"></a>Nastavte trezor klíčů Azure a aplikaci Azure AD pro umožnění komunikace mezi jednotkami škálování

1. Po nasazení prostředí vytvořte další aplikaci Azure AD umožňující důvěryhodnou komunikaci mezi vaším centrem a jednotkou škálování.

    ```powershell
    .\Create-SpokeToHubAADApplication.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                          -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                          -ApplicationDisplayName '<Whichever name you want the Azure AD app to have>'
    ```

1. Po vytvoření aplikace musíte vytvořit tajný kód klienta a uložit informace do trezoru klíčů Azure. Kromě toho musíte udělit přístup k aplikaci Azure AD, která byla vytvořena, aby mohla získat tajné kódy, které jsou uloženy v trezoru klíčů. Pro vaše pohodlí následující skript automaticky provede všechny požadované akce.

    ```powershell
    .\Create-SpokeToHubAADAppSecrets.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                         -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                         -SubscriptionName '<Any subscription within your tenant>' `
                                         -ResourceGroupName '<Any resource group within your subscription>' `
                                         -KeyVaultName '<Any key vault within your resource group>' `
                                         -Location '<Any Azure location where Azure Key Vault is available>' `
                                         -LCSEnvironmentId '<The LCS environment ID of your deployed scale unit>' `
    ```

    > [!NOTE]
    > Pokud žádný trezor klíčů nemá zadanou hodnotu **KeyVaultName**, skript ji automaticky vytvoří.

1. Přidejte ID aplikace Azure AD, kterou jste právě vytvořili (při použití skriptu Create-SpokeToHubAADApplication.ps1) do tabulky aplikací Azure AD ve vašem centru. Tento krok můžete dokončit ručně prostřednictvím uživatelského rozhraní.

## <a name="upload-target-packages-into-lbd-project-assets-in-lcs"></a><a name="upload-packages"></a>Nahrajte cílové balíčky do prostředků projektu LBD v LCS

Tento krok připraví verzi aplikace, verzi platformy a přizpůsobení, které budou převedeny do prostředí jednotky škálování LBD.

1. Nahrajte stejný kombinovaný balíček aplikace/platformy, který byl aplikován na prostředí centra, do knihovny aktiv místního projektu LCS.
1. Získejte kopii vlastního nasaditelného balíčku aplikace/platformy, který byl aplikován na prostředí centra, a nahrajte ji do knihovny aktiv místního projektu LCS.

## <a name="service-the-lbd-environment-with-target-packages"></a><a name="service-target-packages"></a>Obsluhujte prostředí LBD pomocí cílových balíčků

Tento krok uvede do souladu verzi aplikace, verzi platformy a přizpůsobení v prostředí jednotky škálování LBD s centrem.

1. Vybavte prostředí LBD pomocí kombinovaného balíčku aplikace/platformy, který jste nahráli v předchozím kroku.
1. Vybavte prostředí LBD pomocí vlastního nasaditelného balíčku, jste nahráli v předchozím kroku.

    ![Použití aktualizací v LCS.](media/cloud_edge-LBD-LCS-ServiceLBDEnv1.png "Použití aktualizací v LCS")

    ![Výběr balíčku přizpůsobení.](media/cloud_edge-LBD-LCS-ServiceLBDEnv2.png "Výběr balíčku přizpůsobení")

## <a name="assign-your-lbd-edge-scale-unit-to-a-hub"></a><a name="assign-edge-to-hub"></a>Přiřaďte jednotku škálování hrany LBD k centru

Konfiguraci a správu jednotky škálování hrany provádíte prostřednictvím portálu pro správu jednotek škálování. Další informace naleznete v [Správa cloudových jednotek škálování a úkolů pomocí portálu správce jednotky škálování](./cloud-edge-landing-page.md#scale-unit-manager-portal).

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
