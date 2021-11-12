---
title: Nasazení jednotek škálování hraniční sítě na vlastní hardware pomocí LBD (Preview)
description: Toto téma vysvětluje, jak zřídit místní jednotky škálování hrany pomocí vlastního hardwaru a nasazení, které je založeno na místních obchodních datech (LBD).
author: cabeln
ms.date: 04/22/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 0ebbdaab9d6f040497d3158db2712e102b6e9aa8
ms.sourcegitcommit: 1e5a46271bf7fae2f958d2b1b666a8d2583e04a8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/25/2021
ms.locfileid: "7678974"
---
# <a name="deploy-edge-scale-units-on-custom-hardware-using-lbd-preview"></a>Nasazení jednotek škálování hraniční sítě na vlastní hardware pomocí LBD (Preview)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)] <!--KFM: Until 11/1/2021 -->

Jednotky škálování hrany hrají důležitou roli v distribuované hybridní topologii pro správu dodavatelského řetězce. V hybridní topologii můžete rozdělit pracovní zátěže mezi vaše cloudové centrum Supply Chain Management a další jednotky škálování v cloudu nebo na hraně.

Jednotky škálování hrany lze nasadit vytvořením [místního prostředí](../../fin-ops-core/dev-itpro/deployment/on-premises-deployment-landing-page.md) místních obchodních dat (LBD) a poté je nakonfigurovat tak, aby fungovaly jako jednotka škálování ve vaší distribuované hybridní topologii pro správu dodavatelského řetězce. Toho je dosaženo propojením místního prostředí LBD s prostředím Supply Chain Management v cloudu, které bylo nakonfigurováno tak, aby fungovalo jako centrum.  

Jednotky škálování hrany jsou aktuálně ve verzi Preview. Prostředí tohoto typu tedy smíte používat pouze podle [podmínek Preview](https://aka.ms/scmcnepreviewterms).

Toto téma popisuje, jak nastavit místní prostředí LBD jako jednotku škálování hrany a pak ji přidružit k centru.

## <a name="deployment-overview"></a>Přehled nasazení

Zde je přehled kroků nasazení.

1. **Povolte slot LBD ve svém projektu LBD v Microsoft Dynamics Lifecycle Services (LCS).**

    Během verze Preview se jednotky škálování hrany LBD zaměřují na stávající zákazníky LBD. Další 60denní omezený slot LBD sandbox bude poskytován pouze ve specifických situacích zákazníků.

1. **Nastavte a nasaďte prostředí LBD s *prázdnou* databází.**

    Použijte LCS k nasazení prostředí LBD s nejnovější topologií a prázdnou databází. Pro více informací viz část [Nastavení a nasazení prostředí LBD s prázdnou databází](#set-up-deploy) dále v tomto tématu. Musíte používat Supply Chain Management verze 10.0.19 s aktualizací platformy 43 nebo vyšší v prostředích center a jednotek škálování.

1. **Nahrajte cílové balíčky do prostředků projektu LBD v LCS.**

    Připravte si balíčky aplikací, platformy a přizpůsobení, které použijete v centru a jednotce škálování hran. Pro více informací viz část [Nahrání cílových balíčků do prostředků projektu LBD v LCS](#upload-packages) dále v tomto tématu.

1. **Obsluhujte prostředí LBD pomocí cílových balíčků.**

    Tento krok zajistí, že na centru i paprsku bude nasazeno stejné sestavení a přizpůsobení. Pro více informací viz část [Obsluha prostředí LBD pomocí cílových balíčků](#service-target-packages) dále v tomto tématu.

1. **Dokončete konfiguraci jednotky škálování a přiřazení pracovní zátěže.**

    Pro více informací viz část [Přiřazení jednotky škálování hrany LBD k centru](#assign-edge-to-hub) dále v tomto tématu.

Zbývající části tohoto tématu poskytují podrobnější informace o tom, jak provést tyto kroky.

## <a name="set-up-and-deploy-an-lbd-environment-with-an-empty-database"></a><a name="set-up-deploy"></a>Nastavte a nasaďte prostředí LBD s prázdnou databází

Tento krok vytvoří funkční prostředí LBD. Prostředí však nemusí mít nutně stejnou verzi aplikace a platformy jako prostředí centra. Kromě toho stále chybí přizpůsobení a ještě nebylo povoleno, aby fungovalo jako jednotka škálování.

1. Postupujte podle pokynů v části [Nastavení a nasazení místních prostředí (Platform Update 41 a novější)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md). Musíte používat Supply Chain Management verze 10.0.19 s aktualizací platformy 43 nebo vyšší v prostředích center a jednotek škálování

    > [!IMPORTANT]
    > Přečtěte si zbytek této části **před** provedením kroků v tomto tématu.

1. Než popíšete svou konfiguraci v souboru infrastructure\\ConfigTemplate.xml, spusťte následující skript:

    ```powershell
    .\Configure-ScriptsForEdgeScaleUnits.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > Tento skript odstraní veškerou konfiguraci, která není potřeba pro nasazení jednotek škálování hrany.

1. Nastavte databázi, která obsahuje prázdná data, jak je popsáno v části [Konfigurace databází](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb). Pro tento krok použijte prázdný soubor data.bak.
1. Nastavte skript před nasazením. Další informace viz [Předběžné nasazení místního agenta a skripty po nasazení](../../fin-ops-core/dev-itpro/lifecycle-services/pre-post-scripts.md).

    1. Zkopírujte obsah ze složky **Jednotka škálování** v **Skripty infrastruktury** do složky **Skripty** ve sdílené složce úložiště souborů agenta, která byla nastavena v prostředí. Typická cesta je \\\\lbdiscsi01\\agent\\Scripts.
    2. Vytvořte skript **PreDeployment.ps1**, který bude volat skripty pomocí požadovaných parametrů. Skript před nasazením musí být vložen do služky **Skripty** ve sdílené složce úložiště souborů agenta. Jinak nelze spustit. Typická cesta je \\\\lbdiscsi01\\agent\\Scripts\\PreDeployment.ps1.

        Obsah skriptu PreDeployment.ps1 bude připomínat následující příklad.

        ```powershell
        $agentShare = '\\lbdiscsi01\agent'
        
        Write-Output "AgentShare is set to $agentShare" 
        & $agentShare\Scripts\Configure-CloudandEdge.ps1 -AgentShare $agentShare -InstanceId '@A' -DatabaseServer 'lbdsqla01.contoso.com' -DatabaseName 'AXDB'
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

## <a name="upload-target-packages-into-lbd-project-assets-in-lcs"></a><a name="upload-packages"></a>Nahrajte cílové balíčky do prostředků projektu LBD v LCS

Tento krok připraví verzi aplikace, verzi platformy a přizpůsobení, které budou převedeny do prostředí jednotky škálování LBD.

1. Nahrajte stejný kombinovaný balíček aplikace/platformy, který byl aplikován na prostředí centra, do knihovny aktiv místního projektu LCS.
1. Získejte kopii vlastního nasaditelného balíčku aplikace/platformy, který byl aplikován na prostředí centra, a nahrajte ji do knihovny aktiv místního projektu LCS.

## <a name="service-the-lbd-environment-with-target-packages"></a><a name="service-target-packages"></a>Obsluhujte prostředí LBD pomocí cílových balíčků

Tento krok uvede do souladu verzi aplikace, verzi platformy a přizpůsobení v prostředí jednotky škálování LBD s centrem.

1. Vybavte prostředí LBD pomocí kombinovaného balíčku aplikace/platformy, který jste nahráli v předchozím kroku.
1. Vybavte prostředí LBD pomocí vlastního nasaditelného balíčku, jste nahráli v předchozím kroku.

    ![Výběr možnosti Údržba > Použít aktualizace v LCS.](media/cloud_edge-LBD-LCS-ServiceLBDEnv1.png "Výběr možnosti Údržba > Použít aktualizace v LCS")

    ![Výběr balíčku přizpůsobení.](media/cloud_edge-LBD-LCS-ServiceLBDEnv2.png "Výběr balíčku přizpůsobení")

## <a name="assign-your-lbd-edge-scale-unit-to-a-hub"></a><a name="assign-edge-to-hub"></a>Přiřaďte jednotku škálování hrany LBD k centru

Zatímco jednotky škálování hrany jsou stále v Preview, musíte použít [nástroje pro nasazení a konfiguraci jednotek škálování](https://github.com/microsoft/SCMScaleUnitDevTools), které jsou dostupné na GitHubu, pro přiřazení jednotky škálování hrany LBD k centru. Proces umožňuje, aby konfigurace LBD fungovala jako jednotka škálování hrany a přidružila ji k centru. Proces je podobný konfiguraci samostatného vývojového prostředí.

1. Stáhněte si nejnovější verzi [SCMScaleUnitDevTools](https://github.com/microsoft/SCMScaleUnitDevTools/releases) a rozbalte obsah souboru.
1. Vytvořte kopii souboru `UserConfig.sample.xml` a pojmenujte ji `UserConfig.xml`.
1. Vytvořte aplikaci Microsoft Azure Active Directory (Azure AD) ve klientovi Azure AD, jak je uvedeno v části [Průvodce nasazením pro jednotku škálování a pracovní zátěže](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide#aad-application-registrations).
    1. Po vytvoření přejděte na formulář žádosti Azure AD (SysAADClientTable) v centru.
    1. Vytvořte nový záznam a nastavte **ID klienta** na ID aplikace, kterou jste vytvořili. Nastavte **Název** na *ScaleUnits* a **Uživatelské ID** na *Admin*.

1. Vytvořte aplikaci Active Directory Federation Service (AD FS), jak je uvedeno v části [Průvodce nasazením pro jednotku škálování a pracovní zátěže](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide#adfs-application-registrations).
    1. Po vytvoření přejděte na formulář žádosti Azure AD (SysAADClientTable) v jednotce škálování hrany.
    1. Vytvořte nový záznam a nastavte **ID klienta** na ID aplikace, kterou jste vytvořili. Nastavte **uživatelské ID** na *Admin*.

1. Upravte soubor `UserConfig.xml`.
    1. V části `InterAOSAADConfiguration` zadejte informace z aplikace Azure AD, kterou jste vytvořili dříve.
        - V prvku `AppId` zadejte ID aplikace Azure.
        - V prvku `AppSecret` zadejte ID tajný kód aplikace Azure.
        - Prvek `Authority` musí obsahovat adresu URL určující bezpečnostní oprávnění pro vašeho klienta.

        ```xml
        <InterAOSAADConfiguration>
            <AppId>8dab14f6-97b1-48e3-b51b-350b45f6ede5</AppId>
            <AppSecret>k6em-_7.lopty56TGUedDTVhtER-j_6anY1</AppSecret>
            <Authority>https://login.windows.net/contoso.onmicrosoft.com</Authority>
        </InterAOSAADConfiguration>
        ```

    1. V části `ScaleUnitConfiguration` u první `ScaleUnitInstance` upravte část `AuthConfiguration`.
        - V prvku `AppId` zadejte ID aplikace Azure.
        - V prvku `AppSecret` zadejte ID tajný kód aplikace Azure.
        - Prvek `Authority` musí obsahovat adresu URL určující bezpečnostní oprávnění pro vašeho klienta.

        ```xml
        <AuthConfiguration>
            <AppId>8dab14f6-97b1-48e3-b51b-350b45f6ede5</AppId>
            <AppSecret>k6em-_7.lopdz.6d3DTVOtf9Lo-j_6anY1</AppSecret>
            <Authority>https://login.windows.net/contoso.onmicrosoft.com</Authority>
        </AuthConfiguration>
        ```

    1. Pro stejnou `ScaleUnitInstance` navíc nastavte následující hodnoty:
        - V prvku `Domain` zadejte adresu URL centra. Například: `https://cloudhub.sandbox.operations.dynamics.com/`
        - V prvku `EnvironmentType` zkontrolujte, že je nastavena hodnota `LCSHosted`.

    1. V části `ScaleUnitConfiguration` u druhé `ScaleUnitInstance` upravte část `AuthConfiguration`.
        - V prvku `AppId` zadejte ID aplikace AD FS.
        - V prvku `AppSecret` zadejte ID tajný kód aplikace ADFS.
        - Prvek `Authority` musí obsahovat adresu URL vaší instance služby AD FS.

        ```xml
        <AuthConfiguration>
            <AppId>26b16f25-21d8-4d36-987b-62df292895aa</AppId>
            <AppSecret>iZFfObgI6lLtY9kEbBjEFV98NqI5_YZ0e5SBcWER</AppSecret>
            <Authority>https://adfs.contoso.com/adfs</Authority>
        </AuthConfiguration>
        ```

    1. Pro stejnou `ScaleUnitInstance` navíc nastavte následující hodnoty:
        - V prvku `Domain` zadejte adresu URL jednotky škálování hrany. Například: https://ax.contoso.com/
        - V prvku `EnvironmentType` zkontrolujte, že je nastavena hodnota LBD.
        - V prvku `ScaleUnitId` zadejte stejnou hodnotu, jakou jste zadali pro prvek `InstanceId` při konfiguraci skriptu před nasazením `Configure-CloudandEdge.ps1`.

        > [!NOTE]
        > Pokud nepoužíváte výchozí Id (@A), ujistěte se, že aktualizujete ScaleUnitId pro každý ConfiguredWorkload v části Workloads.

1. Otevřete PowerShell a přejděte do složky obsahující soubor `UserConfig.xml`.

1. Spusťte nástroj tímto příkazem.

    ```powershell
    .\CLI.exe
    ```

    > [!NOTE]
    > Po každé akci budete muset nástroj znovu spustit.

1. V nástroji vyberte **2. Připravit prostředí pro instalaci pracovní zátěže**. Poté spusťte následující kroky:
    1. Vyberte **1. Připravit centrum**.
    1. Vyberte **2. Připravit jednotku škálování**.

    > [!NOTE]
    > Pokud tento příkaz nespouštíte z čisté instalace a selže, proveďte následující akce:
    >
    > - Odstraňte všechny složky ze složky `aos-storage` (kromě `GACAssemblies`).
    > - Spusťte následující příkaz SQL ve vaší obchodní databázi (AXDB):
    >
    > ```sql 
    > delete from storagefoler
    > ```

1. Spusťte následující příkazy SQL ve vaší obchodní databázi (AXDB):

    ```sql
    delete from FEATUREMANAGEMENTMETADATA
    delete from FEATUREMANAGEMENTSTATE
    delete from NUMBERSEQUENCESCOPE
    ```

1. Ověřte, že ve vaší obchodní databázi (AXDB) bylo povoleno sledování změn
    1. Spusťte aplikaci SQL Server Management Studio (SSMS).
    1. Klikněte pravým tlačítkem na svou obchodní databázi (AXDB) a vyberte vlastnosti.
    1. V okně, které se otevře, vyberte **Sledování změn** a proveďte následující nastavení:

        - **Change Tracking:** *True*
        - **Retention Period:** *7*
        - **Retention Units:** *Days*
        - **Auto Cleanup:** *True*

1. V nástroji vyberte **3. Nainstalovat úlohy**. Poté spusťte následující kroky:
    1. Vyberte **1. Nainstalovat na centrum**.
    1. Vyberte **2. Nainstalovat na jednotku škálování**.

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
