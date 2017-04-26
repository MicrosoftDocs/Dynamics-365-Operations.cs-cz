---
title: "Přecenění cizí měny pro hlavní knihu"
description: "Toto téma obsahuje přehled následující hlavní knihy procesu přecenění cizí měny - instalace, spuštění procesu výpočtu pro proces a jak Stornovat transakce přecenění v případě potřeby."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CurrencyLedgerGainLossAccount
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62153
ms.assetid: 842e8561-560f-4cc6-8668-70cca60b1ba3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: 5d6d13fe44eef7766b4dcaf274c3522bce3da816
ms.lasthandoff: 03/31/2017


---

# <a name="foreign-currency-revaluation-for-general-ledger"></a>Přecenění cizí měny pro hlavní knihu

[!include[banner](../includes/banner.md)]


Toto téma obsahuje přehled následující hlavní knihy procesu přecenění cizí měny - instalace, spuštění procesu výpočtu pro proces a jak Stornovat transakce přecenění v případě potřeby. 

V rámci uzávěrky období vyžadují účetní konvence přecenění zůstatků účtů hlavní knihy v cizích měnách pomocí různých typů směnných kurzů (aktuální, historický, průměrný atd.). Například jedna účetní konvence vyžaduje přecenění aktiv a pasiv při aktuálním směnném kurzu, dlouhodobého majetku s historickým směnným kurzem a účty zisků a ztrát v měsíčním průměru. Přecenění cizí měny v hlavní knize může být použito k přecenění rozvahy a účtu zisků a ztrát. 

> [!NOTE]
> Přecenění cizí měny je také k dispozici v účty pohledávek (AR) a závazků (AP). Pokud používáte tyto moduly, zbývající transakce by oceňují pomocí přecenění cizí měny v těchto modulech. Přecenění cizí měny pohledávek a závazků vytvoří v hlavní knize účetní záznam odrážející nerealizované zisky nebo ztráty. To zajistí, že můžete odsouhlasit vedlejší a hlavní knihy. Vzhledem k tomu, že k přecenění cizí měny pohledávek a závazků se vytvoří účetní položky v modulu hlavní knihy, hlavní účty pohledávek a závazků mají být vyloučeny z přecenění cizí měny hlavní knihy. 

Po spuštění procesu přecenění budou zůstatky na jednotlivých hlavních účtech zaúčtované v cizích měnách přeceněny. Transakce nerealizovaných zisků nebo ztrát, které byly vytvořeny během procesu přecenění, jsou generovány systémem. Dvě transakce může být vytvořen, jeden pro zúčtovací měnu a druhý pro sekundární měnu podle potřeby. Každá účetní položka bude účtovat nerealizovaný zisk nebo ztrátu a hlavní účet byly přehodnoceny.

## <a name="prepare-to-run-foreign-currency-revaluation"></a>Příprava na spuštění přecenění cizí měny
Před spuštěním procesu přecenění je nutné provést následující nastavení.

-   Na stránce **Hlavní účet** proveďte toto:
-   Pokud má být hlavní účet přeceněn v hlavní knize, vyberte možnost **Přecenění cizí měny**. Pokud by neměl být hlavní účet přeceněn (například konkrétní pohledávky a závazky, pokud jsou přeceněny ve vedlejších knihách), zrušte zaškrtnutí tohoto políčka.
-   Pokud je označen hlavní účet pro přecenění, zadejte **typ směnného kurzu**. Tento typ směnného kurzu se použije pro přecenění hlavního účtu. Po finanční vykazování je k dispozici samostatné pole **Typ směnného kurzu finančního výkaznictví**. Tato dvě pole nejsou synchronizována, což umožňuje použití různých typů směnných kurzů pro přecenění a vykazování.

-   Na stránce **Hlavní kniha** udělejte toto:
-   Určete **Typ směnného kurzu**. Pokud není definován typ směnného kurzu pro hlavní účet, použije se tento typ směnného kurzu při přecenění cizí měny.
-   Zadejte účty pro realizovaný zisk, realizovanou ztrátu, nerealizovaný zisk a nerealizovanou ztrátu k přecenění měny. Účty pro realizovaný zisk a realizovanou ztrátu se používají při vypořádávání transakcí pohledávek a závazků a účty pro nerealizovaný zisk a nerealizovanou ztrátu se používají pro přecenění otevřených transakcí a hlavních účtů hlavní knihy.

-   Na stránce **Účty přecenění měny** udělejte toto:
-   Vyberte různé účty přecenění měny pro každou měnu a společnosti. Pokud nejsou definovány žádné účty, budou použity účty ze stránky **Hlavní kniha**.

## <a name="process-foreign-currency-revaluation"></a>Zpracování přecenění cizí měny
Po dokončení nastavení použijte stránku **Přecenění cizí měny** k přecenění transakcí a zůstatků na hlavních účtech. Proces můžete spustit v reálném čase nebo naplánovat jeho spuštění použitím dávky. 

Na stránce **Přecenění cizí měny** se zobrazí historie pro každý proces přecenění včetně údaje, kdy byl proces spuštěn, jaká kritéria byla definována, odkazu na doklad vytvořený pro přecenění a záznam, pokud předchozí přecenění byla stornována. Spusťte proces přecenění klepnutím na tlačítko **Přecenění cizí měny**. 

Hodnoty **Od data** a **Do data** definují interval dat pro výpočet zůstatku cizí měny, který bude přeceněný. Při přeceňování účtů zisků a ztrát jsou přeceněny všechny transakce (součet) provedené v časovém intervalu. Pokud přeceňujete rozvahové účty, počáteční datum je ignorováno. Místo toho je určen zůstatek k přecenění od začátku fiskálního roku dosud. 

**Datum sazby** lze použít k definování datum, pro které by výchozí směnný kurz. Například můžete přecenit zůstatky mezi datum rozsahu z leden 1 k 31, ale pomocí směnného kurzu definovaného pro dne 1. 

Vyberte hlavní účty k přecenění: všechny, rozvahový účet nebo účet zisků a ztrát. Pouze hlavní účty označené pro přecenění (na hlavní stránce účtu) budou přehodnoceny. Pokud chcete dále omezit rozsah hlavních účtů použít záznamy **Chcete-li zahrnout** kartu můžete definovat rozsah hlavních účtů nebo jednotlivé hlavní účty. 

Přecenění proces lze spustit pro jednu nebo více právnických osob. Vyhledávání se zobrazí pouze právnické osoby, ke kterým máte přístup. Vyberte právnické osoby, pro které chcete spustit proces přecenění. 

Přecenění lze spustit pro jednu nebo více cizích měn. Vyhledávání bude obsahovat všechny měny, které byly zaúčtovány do rozsahu data relevantní pro daný typ hlavního účtu právnické osoby, které jsou vybrány k přecenění (rozvaha nebo zisk a ztráta). Zúčtovací měna bude zařazena do seznamu, ale nic se oceňují, pokud je vybrána v zúčtovací měně. 

Nastavit **náhled před zaúčtováním** k **Ano** Pokud byste chtěli zkontrolovat výsledek přecenění hlavní knihy. Náhled v hlavní knize se liší od simulace v cizí měně přecenění pohledávek a závazků. Simulace v AR a AP se jedná o sestavu, ale hlavní knihy má náhled, které lze zaúčtovat, aniž by bylo nutné znovu spustit proces přecenění. Náhled výsledků lze exportovat do aplikace Microsoft Excel, chcete-li uchovat historii způsobu výpočtu částek. Nelze použít dávkové zpracování, pokud chcete zobrazit výsledky přecenění. Z náhledu má uživatel možnost zaúčtovat výsledky všech právnických osob pomocí tlačítka **Zaúčtovat**. Pokud existuje problém s výsledky pro právnickou osobu, uživatel má možnost zaúčtovat dílčí sadu právnických osob pomocí tlačítka **Vybrat právnické osoby k zaúčtování**. 

Po dokončení procesu přecenění cizí měny, bude sledovat historii každé spuštění vytvořen záznam.  Bude vytvořen samostatný záznam pro každou právnickou osobu a účtovací vrstvu.

## <a name="calculate-unrealized-gainloss"></a>Výpočet nerealizovaných zisků/ztrát
Transakce nerealizovaných zisků/ztrát jsou vytvořeny odlišně mezi přeceněním hlavní knihy a procese přecenění pohledávek a závazků. V pohledávkách a závazcích jsou předchozí přecenění zcela stornována (za předpokladu, že není dosud vyrovnána transakce) a je vytvořena nová transakce přecenění pro nerealizované zisky/ztráty podle nového směnného kurzu. Je to proto, že přeceňujeme každou jednotlivou transakce pohledávek a závazků. V hlavní knize není vrátit zpět předchozí přecenění. Místo toho transakce je vytvořen pro rozdíl mezi zůstatek hlavního účtu, včetně všech předchozích přecenění částek a novou hodnotu podle směnného kurzu pro datum kurzu. 

**Příklad** existují následující zůstatky pro hlavní účet 110110.

|            |                    |                        |                       |
|------------|--------------------|------------------------|-----------------------|
| **Datum**   | **Účet hlavní knihy** | **Částka transakce** | **Účetní částka** |
| 20. leden | 110110 (hotovost)      | 500 EUR (Má dáti)        | 1000 USD (Dal)      |

Hlavní účet přecenění na dne 31.  Nerealizovaný zisk nebo ztráta se vypočte takto:

|                                             |                                            |                                  |                                    |                             |
|---------------------------------------------|--------------------------------------------|----------------------------------|------------------------------------|-----------------------------|
| **Aktuální zůsatek v měně transakce** | **Aktuální zůstatek v zúčtovací měně** | **Směnný kurz při přecenění** | **Nová částka v zúčtovací měně** | **Nerealizovaný zisk/ztráta**    |
| 500 EUR                                     | 1000 USD                                   | 166.6667                         | 833,33 EUR (500 x 1,666667)        | 166,67 ztráta (833,33 – 1000) |

Bude vytvořena následující účetní položka.

|            |                          |           |            |
|------------|--------------------------|-----------|------------|
| **Datum**   | **Účet hlavní knihy**       | **Má Dáti** | **Kreditní** |
| 31. leden | 110110 (hotovost)            |           | 166.67     |
| 31. leden | 801400 (Nerealizovaná ztráta) | 166.67    |            |

Žádné nové transakce jsou zaúčtovány v měsíci únoru.  Hlavní účet přecenění na dne 28.

|                                             |                                            |                                  |                                    |                             |
|---------------------------------------------|--------------------------------------------|----------------------------------|------------------------------------|-----------------------------|
| **Aktuální zůsatek v měně transakce** | **Aktuální zůstatek v zúčtovací měně** | **Směnný kurz při přecenění** | **Nová částka v zúčtovací měně** | **Nerealizovaný zisk/ztráta**    |
| 500 EUR                                     | 833,33 USD (1000 - 166,67)                 | 250.0000                         | 1250 USD (500 x 2,5)               | Zisk 416,67 (1250 – 833.33) |

Bude vytvořena následující účetní položka.

|             |                          |           |            |
|-------------|--------------------------|-----------|------------|
| **Datum**    | **Účet hlavní knihy**       | **Má Dáti** | **Kreditní** |
| 28. únor | 110110 (hotovost)            | 416.67    |            |
| 28. únor | 801600 (Nerealizovaný zisk) |           | 416.67     |

## <a name="reverse-foreign-currency-revaluation"></a>Stornování přecenění cizí měny
Pokud potřebujete stornovat transakci přecenění, vyberte tlačítko **Stornovat transakci** na stránce  **Přecenění cizí měny**. Nový historický záznam přecenění cizí měny bude vytvořen k udržování historického kontrolního záznamu, kdy bylo přecenění vytvořeno nebo stornováno. 

Výsledek přecenění mimo pořadí dat lze zrušit, ale je nutné změnit také aktuálnější přecenění k zajištění správné zůstatky pro každý hlavní účet, přecenění. Protože neexistuje žádný způsob, jak ovládat hlavní účty, které jsou přehodnoceny a kdy jsou přehodnoceny frekvence, může dojít storna aktuální pořadí. Organizace mohou rozhodnout přecenit své hlavní účty hotovosti čtvrtletně, ale všechny hlavní účty každý měsíc.




