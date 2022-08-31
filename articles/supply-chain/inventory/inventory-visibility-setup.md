---
title: Instalace doplňku Viditelnost zásob
description: Tento článek popisuje, jak nainstalovat doplněk Viditelnost zásob pro Microsoft Dynamics 365 Supply Chain Management.
author: yufeihuang
ms.date: 05/27/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 42c2c287e2a813f8bb07ce0c7f21f4224a217946
ms.sourcegitcommit: f2175fe5e900d39f34167d671aab5074b09cc1b8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/17/2022
ms.locfileid: "9306047"
---
# <a name="install-and-set-up-inventory-visibility"></a>Instalace a nastavení Inventory Visibility

[!include [banner](../includes/banner.md)]

Tento článek popisuje, jak nainstalovat doplněk Viditelnost zásob pro Microsoft Dynamics 365 Supply Chain Management.

Musíte nainstalovat doplněk Viditelnost zásob pomocí Microsoft Dynamics Lifecycle Services (LCS). LCS je portál pro spolupráci, který poskytuje prostředí a sadu pravidelně aktualizovaných služeb, které vám pomohou spravovat životní cyklus aplikace vašich finančních a provozních aplikací. Další informace naleznete v tématu [Zdroje Lifecycle Services](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

> [!TIP]
> Doporučujeme, abyste se připojili k uživatelské skupině doplňku Viditelnost zásob, kde můžete najít užitečné průvodce, získat nejnovější aktualizace a zveřejnit jakékoli dotazy týkající se používání Viditelnost zásob. Chcete-li se připojit, pošlete e-mail produktovému týmu Viditelnosti zásob na adresu [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) a zahrňte své ID prostředí Supply Chain Management.

## <a name="inventory-visibility-prerequisites"></a>Předpoklady pro Viditelnost zásob

Před instalací doplňku Viditelnost zásob musíte provést následující úkoly:

- Získejte implementační projekt LCS s alespoň jedním nasazeným prostředím.
- Ujistěte se, že byly splněny předpoklady pro nastavení doplňků. Další informace o těchto prerekvizitách naleznete v tématu [Přehled doplňků](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Viditelnost zásob nevyžaduje propojení duálního zápisu.

> [!NOTE]
> Mezi státy a regiony, které jsou v současné době podporovány, patří Kanada (CCA, ECA), Spojené státy (WUS, EUS), Evropská unie (NEU, WEU), Spojené království (SUK, WUK), Austrálie (EAU, SEAU), Japonsko (EJP, WJP) a Brazílie (SBR, SCUS).

Máte-li jakékoli dotazy týkající se těchto předpokladů, obraťte se na produktový tým doplňku Viditelnost zásob na adrese [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com).

## <a name="install-the-inventory-visibility-add-in"></a><a name="install-add-in"></a>Instalace doplňku Viditelnost zásob

Před instalací doplňku zaregistrujte aplikaci a přidejte tajný kód klienta do Azure Active Directory (Azure AD) v rámci vašeho předplatného Azure. Pokyny viz [Zaregistrujte aplikaci](/azure/active-directory/develop/quickstart-register-app) a [Přidejte tajný kód klienta](/azure/active-directory/develop/quickstart-register-app#add-a-certificate). Nezapomeňte si poznamenat **ID aplikace (klienta)**, **Tajný kód klienta** a **ID klienta**, protože je budete později potřebovat.

> [!IMPORTANT]
> Pokud máte více než jedno prostředí LCS, vytvořte jinou aplikaci Azure AD pro každé z nich. Pokud k instalaci doplňku Viditelnost zásob pro různá prostředí použijete stejné ID aplikace a ID klienta, u starších prostředí dojde k problému s tokenem. V důsledku toho bude platný pouze ten poslední, který byl nainstalován.

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

> [!NOTE]
> Pokud instalace ze stránky LCS trvá déle než hodinu, váš uživatelský účet pravděpodobně nemá oprávnění k instalaci řešení prostředí Dataverse. Chcete-li opravit problém, postupujte následovně:
>
> 1. Zrušte proces instalace doplňku Viditelnost zásob ze stránky LCS.
> 1. Přihlaste se do [centra pro správu Microsoft 365](https://admin.microsoft.com) a ujistěte se, že uživatelský účet, který chcete použít k instalaci doplňku, má přidělenou licenci „Plán Dynamics 365 Unified Operations“. V případě potřeby přidělte licenci.
> 1. Přihlaste se do [centra pro správu Power Platform](https://admin.powerplatform.microsoft.com) pomocí příslušného uživatelského účtu. Poté nainstalujte doplněk Viditelnost zásob následujícím postupem:
>     1. Vyberte prostředí, do kterého chcete doplněk nainstalovat.
>     1. Vyberte **Aplikace Dynamics 365**.
>     1. Vyberte **Nainstalovat aplikaci**.
>     1. Vyberte **Viditelnost zásob**
>
> 1. Po dokončení instalace se vraťte na stránku LCS a zkuste znovu nainstalovat doplněk **Viditelnost zásob**.

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
    - **Modifikátor ofsetu rezervace** - Vyberte stav transakce zásob, který bude kompenzovat rezervace provedené ve službě Viditelnost zásob. Toto nastavení určuje fázi zpracování objednávky, která spouští offsety. Fáze je sledována podle stavu transakcí zásob objednávky. Vyberte některou z následujících možností:
        - *Při objednávce* - Pro stav *Při transakci* objednávka odešle po vytvoření požadavek na vyrovnání. Ofsetové množství bude množství vytvořené objednávky.
        - *Rezervovat* - Pro stav *Rezervovat objednanou transakci* objednávka odešle požadavek na vyrovnání, pokud je rezervována, vyskladněna, zaúčtována dodacím listem nebo fakturována. Požadavek bude spuštěn pouze jednou, v prvním kroku, když nastane zmíněný proces. Ofsetové množství bude množství, ze kterého se změnil stav transakce zásob *V pořadí* na *Rezervováno objednáno* (nebo pozdější stav) na příslušném řádku objednávky.

1. Přejděte do uzlu **Řízení zásob \> Periodické \> Integrace viditelnosti zásob** a povolte úlohu. Všechny události změny zásob z aplikace Supply Chain Management budou nyní odeslány do Viditelnosti zásob.

## <a name="uninstall-the-inventory-visibility-add-in"></a><a name="uninstall-add-in"></a>Odinstalace doplňku Viditelnost zásob

Pro odinstalaci doplňku Viditelnost zásob proveďte následující:

1. Přihlaste se k aplikaci Supply Chain Management.
1. Přejděte do uzlu **Řízení zásob \> Periodické \> Integrace viditelnosti zásob** a zakažte úlohu.
1. Přejděte na LCS a otevřete stránku pro prostředí, ze kterého chcete doplněk odinstalovat (viz také [Nainstalujte doplněk Inventory Visibility Add-in](#install-add-in)).
1. Vyberte **Odinstalovat**.
1. Proces odinstalace nyní ukončí doplněk Viditelnost zásob, zruší registraci doplňku z LCS a odstraní všechna dočasná data uložená v mezipaměti dat doplňku Viditelnost zásob. Primární data zádob, která byla synchronizována s vaším předplatným Dataverse jsou zde však stále uložena. Chcete-li odstranit tato data, dokončete tento postup.
1. Otevřete [Power Apps](https://make.powerapps.com).
1. Vyberte **Prostředí** na navigační liště
1. Vyberte prostředí Dataverse, které je propojeno s vaším prostředím LCS.
1. Přejděte na **Řešení** a odstraňte následující řešení v následujícím pořadí:
    1. Ukotvit řešení pro aplikaci viditelnost zásob v řešeních Dynamics 365
    1. Řešení aplikací Viditelnost zásob Dynamics 365 FNO SCM
    1. Konfigurace služeb zásob
    1. Samostatná Viditelnost zásob
    1. Řešení aplikací Viditelnost zásob Dynamics 365 FNO SCM

    Po odstranění těchto řešení budou odstraněna také data uložená v tabulkách.

> [!NOTE]
> Pokud po odinstalaci doplňku Viditelnost zásob obnovíte databázi Supply Chain Management a poté chcete doplněk znovu nainstalovat, ujistěte se, že jste odstranili stará data Viditelnosti zásob, která jsou uložena ve vašem předplatném Dataverse před opětovnou instalací doplňku (jak je popsáno v předchozím postupu). Předejdete tak problémům s nekonzistencí dat, ke kterým by jinak mohlo dojít.

## <a name="clean-inventory-visibility-data-from-dataverse-before-restoring-the-supply-chain-management-database"></a><a name="restore-environment-database"></a>Vyčistěte data viditelnosti zásob z Dataverse před obnovením databáze Supply Chain Management

Pokud jste používali Viditelnost zásob a poté obnovili databázi Supply Chain Management, může obnovená databáze obsahovat data, která již nejsou konzistentní s daty dříve synchronizovanými pomocí Viditelnosti zásob v Dataverse. Tato nekonzistence dat může způsobit systémové chyby a další problémy. Proto je důležité, abyste vždy vyčistili všechna data viditelnosti zásob z Dataverse před obnovením databáze Supply Chain Management.

Pokud potřebujete obnovit databázi Supply Chain Management, použijte následující postup:

1. Odinstalujte doplněk Viditelnost zásob a odeberte všechna související data v Dataverse podle popisu v tématu [Odinstalace doplňku Viditelnost zásob](#uninstall-add-in).
1. Obnovte databázi Supply Chain Management, například jak je popsáno v tématu [Obnova databáze k bodu v čase (PITR)](../../fin-ops-core/dev-itpro/database/database-point-in-time-restore.md) nebo [Obnova produkční databáze k bodu v čase do prostředí sandbox](../../fin-ops-core/dev-itpro/database/database-pitr-prod-sandbox.md).
1. Pokud ji přesto chcete používat, přeinstalujte a nastavte doplněk Viditelnost zásob, jak je popsáno v [Nainstalujte doplněk Viditelnost zásob](#install-add-in) a [Nastavte integraci viditelnosti zásob](#setup-inventory-visibility-integration)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
