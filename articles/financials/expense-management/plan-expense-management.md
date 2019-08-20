---
title: Konfigurace správy výdajů
description: Tento článek popisuje, co je třeba zvážit a jaká rozhodnutí je třeba učinit během procesu plánování před konfigurací oblasti Správa výdajů v aplikaci Microsoft Dynamics 365 for Finance and Operations.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bf0725a368969e8a2f85f38371d9f18f308246a6
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840906"
---
# <a name="configure-expense-management"></a>Konfigurace správy výdajů

[!include [banner](../includes/banner.md)]

Toto téma popisuje, co je třeba zvážit a jaká rozhodnutí je třeba učinit během procesu plánování před konfigurací oblasti Správa výdajů v aplikaci Microsoft Dynamics 365 for Finance and Operations. Ve správě výdajů můžete ukládat informace například o metodách platby, cestovních žádankách, sestavách výdajů, zásadách atd.

Vzhledem k tomu, že mnohá rozhodnutí, která jste učinili při plánování konfigurace pro správu výdajů, vycházejí z hierarchie a finanční struktury organizace, je třeba využít dokumenty plánování pro tyto oblasti.

## <a name="intercompany-expenses"></a>Mezipodnikové výdaje

Při povolení mezipodnikových výdajů povolíte právnickým osobám a zaměstnancům, aby vystavovali výdaje jménem jiné právnické osoby a vybírali platby od právnické osoby zaměstnání v rámci vaší organizace. Například zaměstnanec v právnické osobě A dokončí projekt pro právnickou osobu B a projektu vzniknou cestovní výdaje. Pokud jsou povoleny mezipodnikové výdaje, může zaměstnanec poté vyplnit vyúčtování výdajů, které zaúčtují výdaje právnické osobě B, a výdaje musí být zaplaceny právnickou osobou A. Pokud vaše organizace nezahrnuje více právnických osob, nemusíte povolit mezipodnikové výdaje.

**Rozhodnutí:** Chcete povolit mezipodnikové výdaje?

## <a name="financial-management"></a>Správa financí

Správa výdajů je úzce integrována s finanční správou organizace. Řada konfigurací pro správu výdajů bude založena na rozhodnutích, která jste učinili ohledně financí vaší organizace. Následující oddíly popisují různé oblasti, které vyžadují plánování, a rozhodnutí založená na finančních rozhodnutích organizace a pokynech od týmu vedení.

### <a name="per-diems"></a>Diety

Je nutné definovat diety zaměstnance, které vaše organizace poskytuje. Protože diety jsou obvykle použity k pokrytí výdajů, jako je stravování, ubytování nebo jiné vedlejší náklady, můžete vytvořit pravidla pro náhrady denních diet, které vaše organizace nabízí. Denní diety lze nastavit podle roční doby, cíle cesty nebo podle obojího. Při definování pravidla denní diety můžete zadat, aby bylo procento denní diety strženo, pokud zaměstnanec bude mít zajištěno náhradní stravování nebo jiné služby. Můžete také definovat úrovně sazeb denní diety a nastavit minimální a maximální počet hodin, pro které lze sazby denních diet použít na cestu pracovníka.

**Rozhodnutí:**

- Výchozí pravidla denních diet pro první a poslední den:

    - Jaký je minimální počet hodin, které zaměstnanec může za den nárokovat a stále obdržet diety?
    - Je částka, která je k dispozici na stravování pro první a poslední den, snížena? Pokud dojde ke snížení, jaké je procento snížení?
    - Je částka, která je k dispozici na hotel pro první a poslední den, snížena? Pokud dojde ke snížení, jaké je procento snížení?
    - Je částka, která je k dispozici na další výdaje pro první a poslední den, snížena? Pokud dojde ke snížení, jaké je procento snížení?

- Výchozí pravidla pro diety:

    - Uplatňuje se procento snížení denní diety pro každé jídlo, například pokud je zajištěno jiné jídlo? Pokud dojde ke snížení, jaké je procento snížení pro každé jídlo?
    - Je srážka za jídlo vypočítána za den, cestu nebo počet jídel za den?
    - Mají být částky denních diet zaokrouhleny obvyklým způsobem nebo zaokrouhleny nahoru?
    - Jsou diety vypočítány za období 24 hodin nebo za kalendářní den?

- Pravidla denních diet založená na místě:

    - Liší se sazby denních diet podle místa? Jaká místa jsou zahrnuta?
    - Pokud se sazby denních diet liší podle místa, pro každé místo, jaká procentuální částka je k dispozici pro následující typy nákladů:

        - Jídla
        - Hotel
        - Jiné výdaje

### <a name="expense-management-journals-and-accounts"></a>Deníky a účty správy výdajů

Správa výdajů vyžaduje použití několika deníků a účtů. Je nutné se rozhodnout, například zda se používá stejný účet pro hotovostní zálohy a spory platební karty.

**Rozhodnutí:**

- Do kterého deníku hlavní knihy mají být zaúčtována schválená vyúčtování výdajů.
- Jaký účet se používá pro hotovostní zálohy?
- Mají být hotovostní zálohy zaúčtovány okamžitě?

### <a name="payment-methods"></a>Způsoby platby

Pokud povolíte zaměstnancům vydávat výdaje jménem vaší společnosti, je nutné definovat metody platby, které mohou zaměstnanci používat. Může například zaměstnancům dovolit používat hotovost nebo firemní platební kartu. Můžete také zaměstnancům umožnit používat osobní kreditní karty a potom provést refundaci pro zaměstnance. Je třeba provést následující rozhodnutí pro každý způsob platby, který povolíte.

**Rozhodnutí:**

- Jaké metody platby jsou povoleny?
- Kdo vlastní výdaje metody platby?
- Existuje typ protiúčtu? Pokud existuje typ protiúčtu, jaký je to účet?
- Pokud existuje protiúčet, jaký je účet?
- Pokud je jako způsob platby zvolena kreditní karta, má být způsob platby použit pouze s importovanými transakcemi?

### <a name="expense-categories-and-shared-categories"></a>Kategorie výdajů a sdílené kategorie

Když zaměstnanci vytvoří sestavu výdajů, musí být každý výdaj, který zaznamenají, přidružen ke kategorii výdajů. Kategorie výdajů jsou odvozeny ze sdílených kategorií, které mohou být sdíleny právnickými osobami v rámci dané organizace. Tyto kategorie lze také sdílet v modulu Řízení a účetnictví projektů, v závislosti na tom, jak je definována vaše organizace. Na základě definice organizace a pokynů od implementačního týmu určete, zda mají být kategorie použité ve správě výdajů použity pouze ve správě výdajů nebo zda mají být sdíleny mezi správou projektu a účetnictvím a správou výdajů. Všimněte si, že tyto kategorie lze sdílet mezi projektem a výdaji nebo projektem a výrobou, ale nikoli mezi výdaji a výrobou. Je třeba provést následující rozhodnutí pro každou kategorii výdajů.

**Rozhodnutí:**

- Co je kategorie výdajů? Příklady obsahují kategorie pro lety, hotel a ujeté kilometry.
- Lze kategorii výdajů použít také v modulu Řízení a účetnictví projektů.
- Co je typ výdajů?
- Jaká je výchozí metoda platby pro kategorii výdajů?
- Musí být výdaje v kategorii výdajů rozepsány?
- Jaký je hlavní výchozí účet pro kategorii výdajů?
- Jaká je výchozí skupina DPH zboží pro kategorii výdajů?
- Jsou pro tuto kategorii výdajů povolený další způsoby platby? Pokud jsou povoleny další platební metody, jaké to jsou metody?
- Existují dílčí kategorie v této kategorii výdajů? Pokud existují dílčí kategorie, je nutné provést následující rozhodnutí:

    - Jsou některé dílčí kategorie vyloučeny z vratky daně?
    - Co je skupina DPH zboží dílčích kategorií?

Pokud je kategorie výdajů použita také v modulu Řízení a účetnictví projektů, odpovězte na zbývající otázky. V opačném případě se přesuňte na následující část.

- Jaké nákladové účty budou použity pro následující výdaje?

    - Náklady
    - Přiřazení mezd
    - NV – náklady
    - Náklady – zboží
    - Nedokončená výroba – hodnota nákladů – položka
    - Časově rozlišená ztráta
    - NV – časově rozlišená ztráta

- Jaké účty výnosů budou použity pro následující?

    - Fakturované výnosy
    - Časově rozlišené výnosy – hodnota prodeje
    - NV – hodnota prodeje
    - Časově rozlišené výnosy – výroba
    - NV – výroba
    - Časově rozlišené výnosy – zisk
    - NV – zisk
    - Časově rozlišené výnosy – předplatné
    - NV – předplatné

### <a name="taxes"></a>Daně

U daní souvisejících s výdaji je třeba určit, co je zahrnuto nebo povoleno v sestavách výdajů.

**Rozhodnutí:**

- Je daň z přidané hodnoty zahrnuta v částkách výdajů.
- Má být povolena vratka daně výdajů?

    > [!NOTE]
    > Pokud jste plánovali hlavní knihu a rozhodli jste použít daň z přidané hodnoty pro USA a daňová pravidla, nemůžete povolit vratku daně výdajů. (Chcete-li použít daň z přidané hodnoty pro USA a daňová pravidla, nastavte možnost **Použít daňové předpisy pro DPH** na **Ano**.)

## <a name="policies"></a>Zásady

Vytvořením sestavy výdajů pomůžete své organizaci ušetřit čas a peníze, když zaměstnanci generují výdaje jejím jménem. Zásady zajišťují, že zaměstnanci nepřekročí rozpočet, poskytnou všechny požadované informace a utratí peníze pouze v případě potřeby. Je třeba provést následující rozhodnutí pro každou zásadu sestavy výdajů a každou zásadu schválení sestavy výdajů, kterou vytvoříte.

**Rozhodnutí:**

- Jaký je název zásad?
- K čemu slouží zásady výdajů?
- Pokud jste se dříve rozhodli povolit mezipodnikové výdaje, kterých společností ve vaší organizaci se tyto zásady týkají?
- Kdy zásady začínají platit?
- Kdy platnost zásad vyprší?
- Co je pravidlo zásad?
- Jaký je výstup pravidla zásad?
