---
title: "Konfigurace správy výdajů"
description: "Tento článek popisuje, co je třeba zvážit a jaká rozhodnutí je třeba učinit během procesu plánování před konfigurací oblasti Správa výdajů v aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise edition. V oblasti Správa výdajů můžete ukládat informace například o metodách platby, cestovních žádankách, sestavách výdajů a zásadách."
author: KimANelson
manager: AnnBe
ms.date: 06/08/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: edd3d8ca760c1453ae7cf8d5ff2fdfdedbb022c4
ms.contentlocale: cs-cz
ms.lasthandoff: 06/13/2017


---

# <a name="configure-expense-management"></a>Konfigurace správy výdajů

[!include[banner](../includes/banner.md)]


Tento článek popisuje, co je třeba zvážit a jaká rozhodnutí je třeba učinit během procesu plánování před konfigurací oblasti Správa výdajů v aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise edition. V oblasti Správa výdajů můžete ukládat informace například o metodách platby, cestovních žádankách, sestavách výdajů a zásadách. 

Vzhledem k tomu, že mnohá rozhodnutí, která jste učinili při plánování konfigurace pro správu výdajů, vycházejí z hierarchie a finanční struktury organizace, je třeba využít dokumenty plánování pro tyto oblasti.

## <a name="intercompany-expenses"></a>Mezipodnikové výdaje
Při povolení mezipodnikových výdajů povolte právnickým osobám a zaměstnancům, aby vystavovali výdaje jménem a vybírali platby od jakékoli právnické osoby v rámci vaší organizace. Například zaměstnanec právnické osoby A dokončí projekt pro právnickou osobu B. Pokud jsou povoleny mezipodnikové výdaje, může zaměstnanec poté vydat časový rozvrh, který má být zaplacen právnickou osobou B. Pokud vaše organizace nezahrnuje více právnických osob, nemusíte povolit mezipodnikové výdaje. **Rozhodnutí:** Chcete povolit mezipodnikové výdaje?

## <a name="financial-management"></a>Správa financí
Správa výdajů je úzce integrována s finanční správou organizace. Řada konfigurací pro správu výdajů bude založena na rozhodnutí, které jste učinili ohledně financí vaší organizace. Následující oddíly popisují různé oblasti, které vyžadují plánování, a rozhodnutí založená na finančních rozhodnutích organizace a pokynech od týmu vedení.

### <a name="per-diems"></a>Diety

Je nutné definovat diety zaměstnance, které vaše organizace poskytuje. Protože diety jsou obvykle použity k pokrytí výdajů, jako je stravování, ubytování nebo jiné vedlejší náklady, můžete vytvořit pravidla pro náhrady denních diet, které vaše organizace nabízí. Denní diety lze nastavit podle roční doby, cíle cesty nebo podle obojího. Při definování pravidla denní diety můžete zadat, aby bylo procento denní diety strženo, pokud zaměstnanec bude mít zajištěno náhradní stravování nebo jiné služby. Můžete také definovat úrovně sazeb denní diety a nastavit minimální a maximální počet hodin, pro které lze sazby denních diet použít na cestu pracovníka. **Rozhodnutí:**

-   Výchozí pravidla denních diet pro první a poslední den:
    -   Jaký je minimální počet hodin, které zaměstnanec může za den nárokovat a stále obdržet diety?
    -   Je částka, která je k dispozici na stravování pro první a poslední den, snížena? Pokud ano, jaké je procento snížení?
    -   Je částka, která je k dispozici na hotel pro první a poslední den, snížena? Pokud ano, jaké je procento snížení?
    -   Je částka, která je k dispozici na další výdaje pro první a poslední den, snížena? Pokud ano, jaké je procento snížení?
-   Výchozí pravidla pro diety:
    -   Uplatňuje se procento snížení denní diety pro každé jídlo, například pokud je zajištěno jiné jídlo? Pokud ano, jaké je procento snížení pro každé jídlo?
    -   Je srážka za jídlo vypočítána za den, cestu nebo počet jídel za den?
    -   Mají být částky denních diet zaokrouhleny normálně nebo nahoru?
    -   Jsou diety vypočítány za období 24 hodin nebo za kalendářní den?
-   Pravidla denních diet založená na poloze
    -   Liší se sazby denních diet v závislosti na poloze a jaké polohy jsou zahrnuty?
    -   Pokud se sazba denních diet liší podle polohy, jaké procento je pro každou polohu poskytováno:
        -   jídla
        -   hotel
        -   jiné výdaje

### <a name="expense-management-journals-and-accounts"></a>Deníky a účty správy výdajů

Správa výdajů vyžaduje použití několika deníků a účtů. Je nutné se rozhodnout, například zda se používá stejný účet pro hotovostní zálohy a spory platební karty. **Rozhodnutí:**

-   Do kterého deníku hlavní knihy mají být zaúčtována schválená vyúčtování výdajů.
-   Jaký účet se používá pro hotovostní zálohy?
-   Mají být hotovostní zálohy zaúčtovány okamžitě?

### <a name="payment-methods"></a>Způsoby platby

Pokud povolíte zaměstnancům vydávat výdaje jménem vaší společnosti, je nutné definovat metody platby, které mohou zaměstnanci používat. Může například zaměstnancům dovolit používat hotovost nebo firemní platební kartu. Můžete také zaměstnancům umožnit používat osobní kreditní karty a potom provést refundaci pro zaměstnance. Je třeba provést následující rozhodnutí pro každý způsob platby, který povolíte. **Rozhodnutí:**

-   Jaké metody platby jsou povoleny?
-   Kdo vlastní výdaje metody platby?
-   Existuje typ protiúčtu? Pokud ano, jaký?
-   Pokud existuje protiúčet, jaký je účet?
-   Pokud je jako způsob platby zvolena kreditní karta, má být způsob platby použit pouze s importovanými transakcemi?

### <a name="expense-categories-and-shared-categories"></a>Kategorie výdajů a sdílené kategorie

Když zaměstnanci vytvoří sestavu výdajů, musí být každý výdaj, který zaznamenají, přidružen ke kategorii výdajů. Kategorie výdajů jsou odvozeny ze sdílených kategorií, které mohou být sdíleny právnickými osobami v rámci dané organizace. Tyto kategorie lze také sdílet v modulu Řízení a účetnictví projektů, v závislosti na tom, jak je definována vaše organizace. Na základě definice organizace a pokynů implementačním týmem určete, zda mají být kategorie použité ve správě výdajů použity pouze ve výdajích nebo zda mají být sdíleny mezi projektem a výdaji. Všimněte si, že tyto kategorie lze sdílet mezi projektem a výdaji nebo projektem a výrobou, ale nikoli mezi výdaji a výrobou. Je třeba provést následující rozhodnutí pro každou kategorii výdajů. **Rozhodnutí:**

-   Co je kategorie výdajů? Například lety, hotel a počet ujetých kilometrů.
-   Lze tuto kategorii výdajů použít také v modulu Řízení a účetnictví projektů.
-   Co je typ výdajů?
-   Jaká je výchozí metoda platby pro kategorii výdajů?
-   Je nutné výdaje v této kategorii rozepsat?
-   Jaký je hlavní výchozí účet pro kategorii výdajů?
-   Jaká je výchozí skupina DPH zboží pro kategorii výdajů?
-   Jsou pro tuto kategorii výdajů povolený další způsoby platby? Pokud ano, jaké?
-   Existují dílčí kategorie v této kategorii výdajů? Pokud ano:
    -   Jsou některé dílčí kategorie vyloučeny z vratky daně?
    -   Co je skupina DPH zboží dílčích kategorií?

    Pokud je tato kategorie výdajů použita také v modulu Řízení a účetnictví projektů, odpovězte na na zbývající otázky. V opačném případě jste v této části skončili.
-   Jaké nákladové účty budou použity pro následující?
    -   Náklady
    -   Přiřazení mezd
    -   NV – náklady
    -   Náklady – zboží
    -   Nedokončená výroba – hodnota nákladů – položka
    -   Časově rozlišená ztráta
    -   NV – časově rozlišená ztráta
-   Jaké účty výnosů budou použity pro následující?
    -   Fakturované výnosy
    -   Časově rozlišené výnosy – hodnota prodeje
    -   NV – hodnota prodeje
    -   Časově rozlišené výnosy – výroba
    -   NV – výroba
    -   Časově rozlišené výnosy – zisk
    -   NV – zisk
    -   Časově rozlišené výnosy – předplatné
    -   NV – předplatné

 

### <a name="taxes"></a>Daně

U daní souvisejících s výdaji je třeba určit, co je zahrnuto nebo povoleno v sestavách výdajů. **Rozhodnutí:**

-   Je daň z přidané hodnoty zahrnuta v částkách výdajů.
-   Má být povolena vratka daně výdajů?

Všimněte si, že pokud jste se při plánování hlavní knihy rozhodli použít DPH a daňová pravidla USA, což lze provést přepnutím pole **Použít daňové předpisy pro DPH** na hodnotu Ano, nelze obnovit vratku daně výdajů.

## <a name="policies"></a>Zásady
Lze vytvořit zásady sestavy výdajů, aby vaše organizace mohla ušetřit čas a peníze, když zaměstnanci vydají výdaje jejím jménem. Zásady zajišťují, že zaměstnanci nepřekročí rozpočet, poskytnou všechny požadované informace a utratí peníze pouze v případě potřeby. Je třeba provést následující rozhodnutí pro každou zásadu sestavy výdajů a každou zásadu schválení sestavy výdajů, kterou vytvoříte. **Rozhodnutí:**

-   Jaký je název zásad?
-   K čemu slouží zásady výdajů?
-   Pokud jste se dříve rozhodli povolit mezipodnikové výdaje, kterých společností ve vaší organizaci se tyto zásady týkají?
-   Kdy zásady začínají platit?
-   Kdy platnost zásad vyprší?
-   Co je pravidlo zásad?
-   Jaký je výstup pravidla zásad?





