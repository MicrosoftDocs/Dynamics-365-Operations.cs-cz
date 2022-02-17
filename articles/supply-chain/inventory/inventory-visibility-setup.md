---
title: Instalace doplňku Viditelnost zásob
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
ms.openlocfilehash: a49f35211f30cdb76104cc5be78f5b114320a228
ms.sourcegitcommit: 4be1473b0a4ddfc0ba82c07591f391e89538f1c3
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/31/2022
ms.locfileid: "8062643"
---
# <a name="install-and-set-up-inventory-visibility"></a>Instalace a nastavení viditelnosti zásob

[!include [banner](../includes/banner.md)]


Toto téma popisuje, jak nainstalovat doplněk Viditelnost zásob pro Microsoft Dynamics 365 Supply Chain Management.

Musíte nainstalovat doplněk Viditelnost zásob pomocí Microsoft Dynamics Lifecycle Services (LCS). LCS je portál pro spolupráci, který poskytuje prostředí a sadu pravidelně aktualizovaných služeb, které vám pomohou spravovat životní cyklus aplikace vašich finančních a provozních aplikací.

Další informace naleznete v tématu [Zdroje Lifecycle Services](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

## <a name="inventory-visibility-prerequisites"></a>Předpoklady pro Viditelnost zásob

Před instalací doplňku Viditelnost zásob musíte provést následující úkoly:

- Získejte implementační projekt LCS s alespoň jedním nasazeným prostředím.
- Ujistěte se, že byly splněny předpoklady pro nastavení doplňků. Další informace o těchto prerekvizitách naleznete v tématu [Přehled doplňků](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Viditelnost zásob nevyžaduje propojení duálního zápisu.

> [!NOTE]
> Mezi státy a regiony, které jsou v současné době podporovány, patří Kanada (CCA, ECA), Spojené státy (WUS, EUS), Evropská unie (NEU, WEU), Spojené království (SUK, WUK), Austrálie (EAU, SEAU), Japonsko (EJP, WJP) a Brazílie (SBR, SCUS).

Máte-li jakékoli dotazy týkající se těchto předpokladů, obraťte se na produktový tým doplňku Viditelnost zásob na adrese [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com).

## <a name="install-the-inventory-visibility-add-in"></a><a name="install-add-in"></a>Instalace doplňku Viditelnost zásob

Před instalací doplňku zaregistrujte aplikaci a přidejte tajný kód klienta do Azure Active Directory (Azure AD) v rámci vašeho předplatného Azure. Pokyny viz [Zaregistrujte aplikaci](/azure/active-directory/develop/quickstart-register-app) a [Přidejte tajný kód klienta](/azure/active-directory/develop/quickstart-register-app#add-a-certificate). Nezapomeňte si poznamenat **ID aplikace (klienta)**, **Tajný kód klienta** a **ID klienta**, protože je budete později potřebovat.

Po registraci aplikace a přidání tajného kódu klienta do Azure AD nainstalujte doplněk Viditelnost zásob podle těchto kroků.

1. Přihlaste se do [LCS](https://lcs.dynamics.com/Logon/Index).
1. Na domovské stránce vyberte projekt, kde je nasazeno vaše prostředí.
1. Na stránce projektu vyberte prostředí, do kterého chcete doplněk nainstalovat.
1. Na stránce prostředí přejděte dolů, dokud neuvidíte část **Doplňky prostředí** v části **Integrace Power Platform**, kde najdete název prostředí . Tam najdete název prostředí Dataverse. Potvrďte, že název prostředí Dataverse je ten, který chcete použít pro Viditelnost zásob.

    > [!NOTE]
    > V současné době jsou podporována pouze prostředí Dataverse, která byla vytvořena pomocí LCS. Pokud vaše prostředí Dataverse bylo vytvořeno jiným způsobem (například pomocí centra pro správu Power Apps) a pokud je propojeno s vaším prostředím Supply Chain Management, musíte nejprve kontaktovat produktový tým Viditelnosti zásob na adrese [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) a vyřešit problém s mapováním. Pak můžete instalovat doplněk Viditelnost zásob.

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
1. V Dataverse vyberte oblast **Aplikace** v levém navigačním panelu a ověřte, že doplněk **Viditelnost zásob** Power Apps je úspěšně nainstalován. Pokud oblast **Aplikace** neexistuje, kontaktujte produktový tým doplňku Viditelnost zásob na adrese [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com).

> [!TIP]
> Doporučujeme, abyste se připojili k uživatelské skupině doplňku Viditelnost zásob, kde můžete najít užitečné průvodce, získat nejnovější aktualizace a zveřejnit jakékoli dotazy týkající se používání Viditelnost zásob. Chcete-li se připojit, pošlete e-mail produktovému týmu Viditelnosti zásob na adresu [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) a zahrňte své ID prostředí Supply Chain Management.

> [!IMPORTANT]
> Pokud máte více než jedno prostředí LCS, vytvořte jinou aplikaci Azure AD pro každé prostředí. Pokud k instalaci doplňku Viditelnost zásob pro různá prostředí použijete stejné ID aplikace a ID klienta, u starších prostředí dojde k problému s tokenem. Platný bude pouze ten poslední, který byl nainstalován.

## <a name="uninstall-the-inventory-visibility-add-in"></a><a name="uninstall-add-in"></a>Odinstalace doplňku Viditelnost zásob

Chcete-li odinstalovat doplněk Viditelnost zásob, vyberte **Odinstalovat** na stránce LCS. Proces odinstalace ukončí doplněk Viditelnost zásob, zruší registraci doplňku z LCS a odstraní všechna dočasná data uložená v mezipaměti dat doplňku Viditelnost zásob. Primární data zádob, která jsou uložena ve vašem předplatném Dataverse však nejsou smazána.

Chcete-li odinstalovat data zásob, která jsou uložena ve vašem předplatném Dataverse, otevřete [Power Apps](https://make.powerapps.com), vyberte **Prostředí** na navigačním panelu a vyberte prostředí Dataverse, které je spojeno s vaším prostředím LCS. Pak přejděte na **Řešení** a odstraňte následujících pět řešení v tomto pořadí:

1. Ukotvení řešení pro aplikaci Viditelnost zásob v řešeních Dynamics 365
1. Řešení aplikací Viditelnost zásob Dynamics 365 FNO SCM
1. Konfigurace služeb zásob
1. Samostatná Viditelnost zásob
1. Řešení aplikací Viditelnost zásob Dynamics 365 FNO SCM

Po odstranění těchto řešení budou odstraněna také data uložená v tabulkách.

## <a name="set-up-inventory-visibility-in-supply-chain-management"></a><a name="setup-dynamics-scm"></a>Nastavení viditelnosti zásob v Supply Chain Management

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

Jakmile si doplněk nainstalujete, připravte systém Supply Chain Management, aby s ním pracoval, a to následujícím způsobem.

1. V aplikaci Supply Chain Management otevřete pracovní prostor **[Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** a zapněte následující funkce:
    - *Nastavení integrace viditelnosti zásob* - povinné.
    - *Integrace viditelnosti zásob s posunem rezervace* - Doporučeno, ale volitelně. Vyžaduje verzi 10.0.22 nebo novější. Další informace viz [Rezervace ve Viditelnosti zásob](inventory-visibility-reservations.md).

1. Přejděte do nabídky **Řízení zásob \> Nastavení \> Parametry integrace Viditelnost zásob**.
1. Otevřete kartu **Obecné** a vytvořte následující nastavení:
    - **Koncový bod viditelnosti zásob** - Zadejte adresu URL prostředí, ve kterém používáte Viditelnost zásob. Více informací najdete v části [Vyhledání koncového bodu služby](inventory-visibility-configuration.md#get-service-endpoint).
    - **Maximální počet záznamů v jednom požadavku** - Nastavte na maximální počet záznamů, které chcete zahrnout do jednoho požadavku. Musíte zadat kladné celé číslo menší nebo rovné 1000. Výchozí hodnota je 512. Důrazně doporučujeme ponechat výchozí hodnotu, pokud jste neobdrželi radu od podpory společnosti Microsoft nebo si nejste jisti, že ji potřebujete změnit.

1. Pokud jste povolili volitelnou funkci *Integrace viditelnosti zásob s posunem rezervace*, otevřete kartu **Posun rezervace** a vytvořte následující nastavení:
    - **Povolit posun rezervace** - Nastavením na *Ano* povolíte tuto funkci.
    - **Modifikátor ofsetu rezervace** - Vyberte stav transakce zásob, který bude kompenzovat rezervace provedené ve službě Viditelnost zásob. Toto nastavení určuje fázi zpracování objednávky, která spouští offsety. Fáze je sledována podle stavu transakcí zásob objednávky. Vyberte jednu z následujících možností:
        - *Při objednávce* - Pro stav *Při transakci* objednávka odešle po vytvoření požadavek na vyrovnání. Ofsetové množství bude množství vytvořené objednávky.
        - *Rezervovat* - Pro stav *Rezervovat objednanou transakci* objednávka odešle požadavek na vyrovnání, pokud je rezervována, vyskladněna, zaúčtována dodacím listem nebo fakturována. Požadavek bude spuštěn pouze jednou, v prvním kroku, když nastane zmíněný proces. Ofsetové množství bude množství, ze kterého se změnil stav transakce zásob *V pořadí* na *Rezervováno objednáno* (nebo pozdější stav) na příslušném řádku objednávky.

1. Přejděte do uzlu **Řízení zásob \> Periodické \> Integrace viditelnosti zásob** a povolte úlohu. Všechny události změny zásob z aplikace Supply Chain Management budou nyní odeslány do Viditelnosti zásob.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
