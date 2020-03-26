---
title: Nastavení správy úvěrů
description: Toto téma popisuje nastavení, které je nezbytné pro správu úvěrů.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 65b1d1a232558efbe05e83d51706a78b12439e47
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124132"
---
# <a name="credit-management-setup"></a>Nastavení správy úvěrů 

[!include [banner](../includes/banner.md)]

## <a name="credit-management-workflows"></a>Workflow správy úvěrů

Chcete-li definovat workflow, která se používají ke správě úprav limitů úvěrů, přejděte na **Úvěr a inkasa \> Nastavení \> Workflow správy úvěru**.

- Můžete vytvořit workflow, které vám umožní schválit dávku úprav limitů úvěru pomocí jediného schválení.
- Můžete přidat workflow na úrovni řádku, aby bylo možné schvalovat opravy limitů úvěrů jednotlivě.
- Můžete vytvořit workflow uvolnění, které automaticky směruje blokování do procesu workflow.

## <a name="blocking-rules"></a>Pravidla blokování

### <a name="ranking-payment-terms"></a>Řazení platebních podmínek

Pokud se platební podmínky objednávky neshodují s výchozími platebními podmínkami pro odběratele, můžete blokovat prodejní objednávku. Někdy se však platební podmínky liší, ale nechcete, aby byla objednávka blokována. Platební podmínky můžete seřadit tak, aby některé z nich měly stejné pořadí, zatímco jiné by měly vyšší nebo nižší pořadí.

Pokud jsou pořadí platebních podmínek aktivní, prodejní objednávky budou blokovány, pokud platební podmínky objednávky mají vyšší pořadí než výchozí platební podmínky pro odběratele.

### <a name="ranking-settlement-discounts"></a>Řazení slev pro vyrovnání

Pokud se platební sleva objednávky neshoduje s výchozí platební slevou pro odběratele, můžete blokovat prodejní objednávku. Někdy se však platební slevy liší, ale nechcete, aby byla objednávka blokována. Platební slevy můžete seřadit tak, aby některé z nich měly stejné pořadí, zatímco jiné by měly vyšší nebo nižší pořadí.

Pokud jsou pořadí platebních slev aktivní, prodejní objednávky budou blokovány, pokud platební sleva objednávky má vyšší pořadí než výchozí platební sleva pro odběratele.

## <a name="reasons"></a>Důvody

Ve správě úvěrů je používáno několik typů důvodů:

- Důvody blokování označují, proč je blokována prodejní objednávka.
- Důvody uvolnění jsou přiřazeny k objednávce, když je uvolněna z blokování.
- Důvody stavu označují, proč byl odběrateli přiřazen stav účtu.

Důvody lze nastavit na stránce **Důvody správy úvěru** (**Správa úvěru \> Nastavení \> Správa úvěru \> Důvody správy úvěru**).

1. V poli **Typ důvodu** vyberte typ důvodu: **Blokování**, **Uvolnění** nebo **Stav**.
2. Do pole **Důvod** zadejte název důvodu.
3. Do pole **Popis** zadejte popis kódu důvodu.

## <a name="credit-management-groups"></a>Skupiny správy úvěrů

Skupiny správy úvěru se používají k označení odběratelů nebo skupin odběratelů, které mají stejné vlastnosti v rámci správy úvěru. Skupiny správy úvěru lze použít například k určení pravidel blokování a vyloučení v rámci správy úvěrů pro odběratele.

Skupiny správy úvěru lze vytvořit na stránce **Skupiny správy úvěru** (**Správa úvěru \> Nastavení> Nastavení skupin \> Skupiny správy úvěru**).

1. Volbou možnosti **Nová položka** vytvořte řádek.
2. Zadejte ID skupiny. ID může obsahovat až 10 znaků.
3. Do pole **Popis** zadejte název skupiny. Název může obsahovat až 60 znaků.

Skupinu správy úvěru lze přiřadit k odběrateli na pevné záložce **Úvěr a inkasa** na stránce **Všichni odběratelé** (**Pohledávky \> Odběratelé \> Všichni odběratelé**).

## <a name="account-statuses"></a>Stavy účtu

Chcete-li identifikovat stav úvěru u účtu odběratele, můžete vytvořit stavy účtu. Můžete definovat stav a jeho dopad na procesy fakturace a blokování dodávky. Stavy účtu lze také použít k určení pravidel blokování pro odběratele.

Stavy účtu můžete vytvořit na stránce **Stavy účtu** (**Správa úvěru \> Nastavení> Nastavení skupin \> Stavy účtu**).

1. Přidejte stav účtu a zadejte popis, který vyjadřuje stav úvěru u odběratele. Například můžete použít popis **Normální** k označení, že je odběratel v dobrém stavu a na otevřené objednávky se vztahuje standardní zpracování v rámci správy úvěru.
2. V polích **Fakturace** a **Blokovaná dodávka** vyberte typ blokování, který by měl být použit u odběratelů s tímto stavem účtu. Je možné blokovat veškeré zpracování, blokovat pouze zpracování faktur nebo neblokovat žádné zpracování při uplatnění pravidel limitu úvěru.

## <a name="scoring-groups"></a>Skupiny skórování

Skupiny podle hodnocení lze nastavit tak, aby definovaly rizikové faktory a kritéria, která jsou použita k jejich měření. V případě použití informací o odběrateli na skupinu podle hodnocení se hodnocení vypočítá pro každý faktor rizika a používá se k umístění odběratele do skupiny podle rizika. Skupinu podle rizika lze použít k označení úvěrové způsobilosti a k výpočtu automatických limitů úvěru.

Skupiny podle hodnocení lze vytvářet na stránce **Skupiny podle hodnocení** (**Správa úvěru \> Nastavení \> Nastavení rizik \> Skupiny podle hodnocení**).

1. Vytvořte skupinu podle hodnocení a zadejte pro ni název.
2. Zadejte popis blíže popisující skupinu podle hodnocení.
3. Vyberte typ skupiny. K dispozici je osm předdefinovaných typů. Je také možné vybrat možnost **Uživatelem definovaný** pro definování typu skupiny, který je vhodnější pro vaši organizaci.
4. Výběrem typu hodnocení definujte způsob, jakým skupina podle hodnocení počítá hodnocení rizika. Existují tyto možnosti:

    - **Rozsah** – Pomocí této možnosti můžete definovat rozsah hodnot, které mají být použity při výpočtu hodnocení.
    - **Uživatelem definovaný** – Tuto možnost použijte, chcete-li ručně definovat seznam hodnot, které mají být použity pro hodnocení.

5. Pokud jste jako typ hodnocení vybrali **Rozsah**, přidejte řádky pro definování rozsahu hodnot a odpovídajících hodnocení.

    1. Do pole **Nejnižší hodnota** zadejte nejnižší hodnotu rozsahu.
    2. Do pole **Nejvyšší hodnota** zadejte nejvyšší hodnotu rozsahu.
    3. Do pole **Hodnocení** zadejte hodnocení, které má být přiřazeno, pokud zadaná hodnota spadá do rozssahu „od/do”.

    Pokud jste jako typ hodnocení vybrali **Definovaný uživatelem**, přidejte řádky pro definování hodnot definovaných uživatelem a odpovídajících hodnocení.

    1. Do pole **Hodnota** zadejte uživatelem definovanou hodnotu, která by měla být poskytnuta z informací o odběrateli.
    2. Do pole **Hodnocení** zadejte hodnocení, které má být přiřazeno, pokud zadaná hodnota spadá do rozssahu „od/do”.

## <a name="risk-assessments"></a>Odhady rizik

Můžete definovat odhady rizik, které lze přiřadit k odběratelům na základě jejich hodnocení rizik. Hodnocení rizika se vypočítá porovnáním informací o odběrateli s každou skupinou podle hodnocení. Hodnocení jsou sečtena a celkové hodnocení je porovnáno s hodnotami v nastavení skupiny podle rizika, aby bylo možné identifikovat skupinu podle rizika, ke které daný odběratel náleží. Hodnocení skupiny podle rizika se pak používá k definování pravidel blokování a vyloučení správy úvěrů pro odběratele.

Skupiny podle rizika můžete nastavit na stránce **Odhady rizik** (**Správa úvěru \> Nastavení \> Nastavení rizika \> Odhady rizik**).

1. Zadejte ID skupiny podle rizika.
2. Zadejte popis blíže vysvětlující skupinu podle rizika.
3. Zadejte rozsah hodnocení, který slouží k určení odběratelů, kteří patří do skupiny podle rizika.
4. Chcete-li zadat symbol reprezentující skupinu podle rizika, vyberte indikátor skupiny podle rizika.

## <a name="guaranteeinsurance-types"></a>Typy záruk/pojištění

Na stránce **Typy záruky/pojištění** (**Správa úvěru \> Nastavení \> Nastavení záruky/pojištění \> Typy záruky/pojištění**) lze nastavit typy záruky/pojištění.

1. Zadejte typ záruky nebo pojištění, který označuje jméno ručitele nebo zprostředkovatele pojištění.
2. Zadejte popis popisující ručitele nebo zprostředkovatele pojištění.

## <a name="coverage-types"></a>Typy pokrytí

Je možné použít typy krytí k další klasifikaci pojistných smluv. Nelze je použít se zárukami.

Typy krytí lze přidat na stránce **Typy krytí** (**Správa úvěru \> Nastavení \> Nastavení záruky/pojištění \> Typy krytí**).

1. Zadejte typ krytí pro určení typu krytí, který má být přidán jako pojištění nebo záruka.
2. Zadejte popis typu krytí.

## <a name="automatic-credit-limits"></a>Automatické úvěrové limity

Na stránce **Automatické limity úvěru** (**Správa úvěru \> Nastavení \> Nastavení rizik \> Automatické limity úvěru**) můžete vytvořit kritéria pro automatické limity úvěru.

1. Vyberte skupinu podle rizika, ke které má být přiřazen automatický limit úvěru.
2. Vyberte měnu pro automatický limit úvěru. Pro stejnou skupinu podle rizika lze vytvořit několik automatických limitů úvěru v různých měnách.
3. Zadejte částku výnosů, která představuje maximální výnosy společnosti, které lze použít pro tento automatický limit úvěru. Při vytvoření limitů úvěru se částka výnosů porovná s hodnotou výnosů, která se nachází na stránce **Finance** (**Pohledávky \> Všichni odběratelé \> Vybrat odběratele \> Obecné \> Statistiky \> Finanční**). Systém používá nejnovější hodnotu v části **Přehled**.

Chcete-li přidat řádky reprezentující limit úvěru, který bude vygenerován na základě vybraných kritérií, postupujte podle následujících kroků.

1. Vyberte skupinu podle hodnocení, která definuje informace o odběrateli, které by měly být použity při výpočtu limitu úvěru.
2. Vyberte operátor pro porovnání, který definuje, jakým způsobem mají být vyhodnocovány informace o skupině podle hodnocení.
3. Zadejte hodnotu, která má být porovnána s hodnotou zadanou pro skupinu podle hodnocení.
4. Zadejte limit úvěru, který má být přiřazen, pokud se informace o odběrateli shodují s hodnotou zadanou pro danou skupinu podle hodnocení. Můžete například vytvořit automatický limit úvěru pro skupinu podle hodnocení **Nízké**. Pokud je jednou ze skupin podle hodnocení počet let podnikání, můžete definovat jeden řádek, který přiřazuje limit úvěru 100 000, pokud odběratel podniká pět let, a další řádek, který přiřazuje limit úvěru 200 000, pokud odběratel podniká 10 let.
