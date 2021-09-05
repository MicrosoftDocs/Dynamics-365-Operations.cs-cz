---
title: Nastavení viditelnosti zásob
description: Toto téma popisuje, jak nainstalovat doplněk Viditelnost zásob pro Microsoft Dynamics 365 Supply Chain Management.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 8573fe01abb1c6092012baf85e8b7df40b74a31f
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/13/2021
ms.locfileid: "7343577"
---
# <a name="set-up-inventory-visibility"></a>Nastavení viditelnosti zásob

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

Toto téma popisuje, jak nainstalovat doplněk Viditelnost zásob pro Microsoft Dynamics 365 Supply Chain Management.

Musíte nainstalovat doplněk Viditelnost zásob pomocí Microsoft Dynamics Lifecycle Services (LCS). LCS je portál pro spolupráci, který poskytuje prostředí a sadu pravidelně aktualizovaných služeb, které vám pomohou spravovat životní cyklus aplikace vašich aplikací Finance and Operations.

Další informace naleznete v tématu [Zdroje Lifecycle Services](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

## <a name="inventory-visibility-prerequisites"></a>Předpoklady pro Viditelnost zásob

Před instalací doplňku Viditelnost zásob musíte provést následující úkoly:

- Získejte implementační projekt LCS s alespoň jedním nasazeným prostředím.
- Ujistěte se, že byly splněny předpoklady pro nastavení doplňků. Další informace o těchto prerekvizitách naleznete v tématu [Přehled doplňků](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Viditelnost zásob nevyžaduje propojení duálního zápisu.
- Kontaktujte produktový tým doplňku Viditelnost zásob na adrese [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) a vyžádejte si následující požadované soubory:

    - `InventoryServiceApplication.PackageDeployer.zip`
    - `Inventory Visibility Integration.zip` (pokud je spuštěná verze Supply Chain Management starší než verze 10.0.18)

> [!NOTE]
> Mezi země a regiony, které jsou v současné době podporovány, patří Kanada (CCA, ECA), Spojené státy (WUS, EUS), Evropská unie (NEU, WEU), Spojené království (SUK, WUK) a Austrálie (EAU, SEAU) .

Máte-li jakékoli dotazy týkající se těchto předpokladů, obraťte se prosím na produktový tým doplňku Viditelnost zásob.

## <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a>Nastavení Dataverse

Chcete-li nastavit Dataverse tak, aby jej bylo možné použít s Viditelností zásob, použijte nástroj package deployer k nasazení balíčku Viditelnost zásob. Následující pododdíly popisují, jak jednotlivé úkoly provést.

> [!NOTE]
> V současné době jsou podporována pouze prostředí Dataverse, která byla vytvořena pomocí LCS. Pokud vaše prostředí Dataverse bylo vytvořeno jiným způsobem (například pomocí centra pro správu Power Apps) a pokud je propojeno s vaším prostředím Supply Chain Management, musíte nejprve kontaktovat produktový tým Viditelnosti zásob a vyřešit problém s mapováním. Pak můžete instalovat doplněk Viditelnost zásob.

### <a name="migrate-from-an-old-version-of-the-dataverse-solution"></a>Migrace ze staré verze řešení Dataverse

Pokud jste nainstalovali starší verzi řešení Dataverse Viditelnost zásob, aktualizujte svou verzi podle těchto pokynů. K dispozici jsou dva případy:

- **Případ 1:** Pokud ručně nastavujete Dataverse importováním řešení `Inventory Visibility Dataverse Solution_1_0_0_2_managed.zip`, postupujte takto:

    1. Stáhněte následující tři soubory:

        - `Inventory Visibility Dataverse Solution_1_0_0_3_managed.zip`
        - `InventoryServiceBase_managed.cab`
        - `InventoryServiceApplication.PackageDeployer.zip`

    1. Ručně importujte `Inventory Visibility Dataverse Solution_1_0_0_3_managed.zip` a `InventoryServiceBase_managed.cab` do Dataverse podle těchto kroků:

        1. Otevřete adresu URL svého prostředí Dataverse.
        1. Otevřete stránku **Řešení**.
        1. Vyberte **Import**.

    1. Pomocí nástroje package deployer nasaďte balíček `InventoryServiceApplication.PackageDeployer.zip`. Pokyny viz sekce [K nasazení balíčku použijte nástroj package deployer](#deploy-package) dále v tomto tématu.

- **Případ 2:** Pokud nastavujete Dataverse pomocí nástroje package deployer před instalací staršího balíčku `.*PackageDeployer.zip`, stáhněte `InventoryServiceApplication.PackageDeployer.zip` a proveďte aktualizaci. Pokyny viz sekce [K nasazení balíčku použijte nástroj package deployer](#deploy-package).

### <a name="use-the-package-deployer-tool-to-deploy-the-package"></a><a name="deploy-package"></a>Pomocí nástroje package deployer nasaďte balíček

1. Nainstalujte vývojářské nástroje podle popisu v části [Stáhněte si nástroje z NuGet](/dynamics365/customerengagement/on-premises/developer/download-tools-nuget).
1. Odblokujte soubor `InventoryServiceApplication.PackageDeployer.zip`, který jste stáhli ze skupiny Teams, postupujte takto:

    1. Vyberte a podržte soubor (nebo klikněte pravým tlačítkem) a vyberte možnost **Vlastnosti**.
    1. V dialogovém okně **Vlastnosti** na kartě **Všeobecné** najděte sekci **Zabezpečení**, vyberte **Odblokovat** a použijte změnu. Pokud sekce **Zabezpečení** na kartě **Všeobecné** neexistuje, soubor není blokován. V takovém případě pokračujte dalším krokem.

    ![Odblokování staženého souboru](media/unblock-file.png "Odblokování staženého souboru")

1. Rozbalte `InventoryServiceApplication.PackageDeployer.zip`, chcete-li najít následující položky:

    - Složka `InventoryServiceApplication`
    - Soubor `[Content_Types].xml`
    - Soubor `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll`

1. Zkopírujte každou z těchto položek do adresáře `.\Tools\PackageDeployment`. (Tento adresář byl vytvořen při instalaci nástrojů pro vývojáře.)
1. Spusťte `.\Tools\PackageDeployment\PackageDeployer.exe` a podle pokynů na obrazovce importujte řešení.

## <a name="install-the-inventory-visibility-add-in"></a><a name="install-add-in"></a>Instalace doplňku Viditelnost zásob

Před instalací doplňku zaregistrujte aplikaci a přidejte tajný kód klienta do Azure Active Directory (Azure AD) v rámci vašeho předplatného Azure. Pokyny viz [Zaregistrujte aplikaci](/azure/active-directory/develop/quickstart-register-app) a [Přidejte tajný kód klienta](/azure/active-directory/develop/quickstart-register-app#add-a-certificate). Nezapomeňte si poznamenat **ID aplikace (klienta)**, **Tajný kód klienta** a **ID klienta**, protože je budete později potřebovat.

Po registraci aplikace a přidání tajného kódu klienta do Azure AD nainstalujte doplněk Viditelnost zásob podle těchto kroků.

1. Přihlaste se do [LCS](https://lcs.dynamics.com/Logon/Index).
1. Na domovské stránce vyberte projekt, kde je nasazeno vaše prostředí.
1. Na stránce projektu vyberte prostředí, do kterého chcete doplněk nainstalovat.
1. Na stránce prostředí přejděte dolů, dokud neuvidíte část **Doplňky prostředí** v části **Integrace Power Platform**, kde najdete název prostředí . Tam najdete název prostředí Dataverse.
1. V sekci **Doplňky prostředí** vyberte **Nainstalovat nový doplněk**.

    ![Stránka prostředí v LCS](media/inventory-visibility-environment.png "Stránka prostředí v LCS")

1. Vyberte odkaz **Nainstalovat nový doplněk**. Objeví se seznam dostupných doplňků.
1. V seznamu vyberte možnost **Viditelnost zásob**.
1. Nastavte následující pole pro vaše prostředí:

    - **ID aplikace AAD (klienta)** – Zadejte ID aplikace Azure AD, které jste vytvořili a poznamenali si dříve.
    - **ID klienta AAD** - Zadejte ID klienta, který jste si dříve poznamenali.

    ![Stránka nastavení doplňku](media/inventory-visibility-setup.png "Stránka nastavení doplňku")

1. Odsouhlaste smluvní podmínky výběrem zaškrtávacího políčka **Smluvní podmínky**.
1. Vyberte **Instalovat**. Stav doplňku se zobrazí jako **Probíhá instalace**. Po dokončení instalace obnovte stránku. Stav by se měl změnit na **Nainstalováno**.

## <a name="uninstall-the-inventory-visibility-add-in"></a><a name="uninstall-add-in"></a>Odinstalace doplňku Viditelnost zásob

Chcete-li odinstalovat doplněk Viditelnost zásob, vyberte **Odinstalovat** na stránce LCS. Proces odinstalace ukončí doplněk Viditelnost zásob, zruší registraci doplňku z LCS a odstraní všechna dočasná data uložená v mezipaměti dat doplňku Viditelnost zásob. Primární data zádob, která jsou uložena ve vašem předplatném Dataverse však nejsou smazána.

Chcete-li odinstalovat data zásob, která jsou uložena ve vašem předplatném Dataverse, otevřete [Power Apps](https://make.powerapps.com), vyberte **Prostředí** na navigačním panelu a vyberte prostředí Dataverse, které je spojeno s vaším prostředím LCS. Pak přejděte na **Řešení** a odstraňte následujících pět řešení:

- Ukotvení řešení pro aplikaci Viditelnost zásob v řešeních Dynamics 365
- Řešení aplikací Viditelnost zásob Dynamics 365 FNO SCM
- Konfigurace služeb zásob
- Samostatná Viditelnost zásob
- Řešení aplikací Viditelnost zásob Dynamics 365 FNO SCM

Po odstranění těchto řešení budou odstraněna také data uložená v tabulkách.

## <a name="set-up-supply-chain-management"></a><a name="setup-dynamics-scm"></a>Nastavení Supply Chain Management

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a>Nasaďte integrační balíček Viditelnost zásob

Pokud používáte Supply Chain Management verze 10.0.17 nebo starší, kontaktujte tým podpory doplňku Viditelnost zásob na adrese [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) a vyžádejte si soubor balíčku. Pak nasaďte balíček do LCS.

> [!NOTE]
> Pokud během nasazení dojde k chybě neshody verzí, musíte ručně importovat projekt X++ do vývojového prostředí. Pak vytvořte nasaditelný balíček ve vývojovém prostředí a nasaďte jej ve svém produkčním prostředí.
>
> Kód je součástí Supply Chain Management verze 10.0.18. Pokud používáte tuto verzi nebo novější, nasazení se nevyžaduje.

Zkontrolujte, zda jsou ve vašem prostředí Supply Chain Management zapnuty následující funkce. (Implicitně jsou zapnuté.)

| Popis funkce | Verze kódu | Třída přepnutí |
|---|---|---|
| Povolení nebo zákaz používání dimenzí zásob v tabulce InventSum      | 10.0.11 | InventUseDimOfInventSumToggle      |
| Povolení nebo zákaz používání dimenzí zásob v tabulce InventSumDelta | 10.0.12 | InventUseDimOfInventSumDeltaToggle |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a>Nastavení integrace viditelnosti zásob

1. V aplikaci Supply Chain Management otevřete pracovní prostor **[Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** a zapněte funkci *Integrace viditelnosti zásob*.
1. Přejděte do uzlu **Řízení zásob \> Nastavení \> Parametry integrace viditelnosti zásob** a zadejte adresu URL prostředí, ve kterém je spuštěn doplněk Viditelnost zásob. Více informací najdete v části [Vyhledání koncového bodu služby](inventory-visibility-power-platform.md#get-service-endpoint).
1. Přejděte do uzlu **Řízení zásob \> Periodické \> Integrace viditelnosti zásob** a povolte úlohu. Všechny události změny zásob z aplikace Supply Chain Management budou nyní odeslány do Viditelnosti zásob.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
