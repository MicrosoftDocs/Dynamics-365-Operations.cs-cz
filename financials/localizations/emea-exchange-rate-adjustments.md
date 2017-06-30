---
title: "Úpravy kurzů"
description: "Toto téma uvádí informace o funkci úpravy směnného kurzu, která umožňuje uživatelům v právnickým osobách v Estonsku, Maďarsku, Litvě, České republice, Maďarsku, Lotyšku, Polsku a Rusku provádět hotovostní operace v systému."
author: ShylaThompson
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 272683
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-elgolu
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: f78be567be1f151ab8fcd4e4b721e5c39be4d7ea
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="exchange-rate-adjustments"></a>Úpravy kurzů

[!include[banner](../includes/banner.md)]


Toto téma uvádí informace o funkci úpravy směnného kurzu, která umožňuje uživatelům v právnickým osobách v Estonsku, Maďarsku, Litvě, České republice, Maďarsku, Lotyšku, Polsku a Rusku provádět hotovostní operace v systému.

Funkce pro vyrovnání kurzových rozdílů pro Estonsko, Maďarsko, Českou republiku, Litvu, Lotyšsko, Polsko a Rusko zahrnuje následující rozšíření, která jsou relevantní pro pohledávky a závazky:

-   Zaúčtování vyrovnání kurzových rozdílů může být stornováno jako opravy (záporné částky) pro původní úpravy.
-   Při zaúčtování po sobě jdoucích nerealizovaných úprav se používá stejný typ zúčtovacího účtu a transakce bez ohledu na to, zda úpravy představují zisk nebo ztrátu.
-   Vypočtené kurzové zisky se vždy zaúčtovávají na účty zisků a vypočítané kurzové ztráty na účty ztrát.

Právnické osoby, které mají primární adresu v rámci České republiky, mohou využít zvláštní metodu vyrovnání kurzových rozdílů. Tato metoda se nazývá přírůstková metoda. Po zapnutí této metody změny nejsou použity změny které aktuální funkce zavedla. Nerealizované a realizované zisky nebo ztráty se počítají na základě posledního použitého směnného kurzu. Opravená částka se použije namísto původní částky jako základ pro výpočet. Pokud chcete přejít na metodu úpravy přírůstkového směnného kurzu, na stránce **Parametry hlavní knihy** v části **Přecenění cizí měny** v poli **Metoda výpočtu** vyberte **Přírůstkové**. Následující příklad ukazuje, jak funkce úpravy směnného kurzu funguje pro Estonsko, Maďarsko, Českou republiku, Litvu, Lotyšsko, Polsko a Rusko. Tady je obchodní scénář pro tento příklad:

-   Faktura v cizí měně je zaúčtována 1. prosince 2012.
-   Platba v cizí měně je zaúčtována 3. ledna 2013
-   Je provedeno vyrovnání pro použití platby u faktury.
-   Úprava směnného kurzu se provede 31. prosince 2012 (metoda = Standardní).
-   Úprava směnného kurzu se provede 1. ledna 2013 (metoda = datum na faktuře).

Zde jsou směnné kurzy pro kanadské dolary (CAD) americké dolary (USD) pro tento příklad:

-   1. prosince 2012: 400,0000
-   31. prosince 2012: 450,0000
-   3. ledna 2013: 420,0000

| Událost                                       | Datum                             | Má dáti / Dal | Částky               | Účet hlavní knihy (HK)    | typ transakce             | Typ zaúčtování       | Kreditní | Oprava |
|---------------------------------------------|----------------------------------|--------------|-----------------------|--------------------------------|------------------------------|--------------------|--------|------------|
| Faktura                                     | 1-Pro-12                         | Má Dáti        | 10,000 CAD/40,000 USD | Pohledávky                             | Faktura                      | Zůstatek odběratele   |        |            |
| Faktura                                     | 1-Pro-12                         | Kreditní       | 10,000 CAD/40,000 USD | Protiúčet                         | Faktura                      | Deník hlavní knihy     | X      |            |
| Platba                                     | 3-led-13                         | Má Dáti        | 10,000 CAD/42,000 USD | Protiúčet                         | Platba                      | Deník hlavní knihy     |        |            |
| Platba                                     | 3-led-13                         | Kreditní       | 10,000 CAD/42,000 USD | Pohledávky                             | Platba                      | Zůstatek odběratele   | X      |            |
| Vyrovnání                                  | 3. ledna 2013 (= datum platby) | Má Dáti        | 0 CAD/2,000 USD       | Pohledávky                             | Zákazník                     | Zisk ze směnného kurzu |        |            |
| Vyrovnání                                  | 3. ledna 2013 (= datum platby) | Kreditní       | 0 CAD/2,000 USD       | Zisk po úpravě v realizované měně   | Zákazník                     | Zisk ze směnného kurzu | X      |            |
| Přecenění (standardní metodou, datum = 31. prosince 2012) | 31-Pro-12           | Má Dáti        | 0 CAD/5,000 USD       | Pohledávky                             | Přecenění cizí měny | Zisk ze směnného kurzu |        |            |
| Přecenění (standardní metodou, datum = 31. prosince 2012) | 31-Pro-12           | Kreditní       | 0 CAD/5,000 USD       | Zisk po úpravě v nerealizované měně | Přecenění cizí měny | Zisk ze směnného kurzu | X      |            |
| Přecenění (standardní metodou, datum = 31. prosince 2012) | 3-led-13            | Má Dáti        | 0 CAD/5,000 USD       | Pohledávky                             | Přecenění cizí měny | Zisk ze směnného kurzu |        | X          |
| Přecenění (standardní metodou, datum = 31. prosince 2012) | 3-led-13            | Kreditní       | 0 CAD/5,000 USD       | Zisk po úpravě v nerealizované měně | Přecenění cizí měny | Zisk ze směnného kurzu | X      | X          |



U předchozího přecenění si všimněte, že položka ze 3. ledna 2013 je přímým stornem položky nad sebou (od 31. prosince 2012). Dokonce účty hlavní knihy a typy zaúčtování jsou shodné. Dále si všimněte, že byl nastaven příznak **Oprava**.
||||||||||
|-----------------------------------------------------------|----------|--------|-----------------|--------------------------------|------------------------------|--------------------|---|---|
|Přecenění (metoda data faktury, datum = 1. ledna 2013)  | 1-led-13 | Má Dáti  | 0 CAD/5,000 USD | Pohledávky                             | Přecenění cizí měny | Zisk ze směnného kurzu |   | X |
| Přecenění (metoda data faktury, datum = 1. ledna 2013) | 1-led-13 | Kreditní | 0 CAD/5,000 USD | Zisk po úpravě v nerealizované měně | Přecenění cizí měny | Zisk ze směnného kurzu | X | X |
| Přecenění (metoda data faktury, datum = 1. ledna 2013) | 3-led-13 | Má Dáti  | 0 CAD/5,000 USD | Pohledávky                             | Přecenění cizí měny | Zisk ze směnného kurzu |   |   |
| Přecenění (metoda data faktury, datum = 1. ledna 2013) | 3-led-13 | Kreditní | 0 CAD/5,000 USD | Zisk po úpravě v nerealizované měně | Přecenění cizí měny | Zisk ze směnného kurzu | X |   |

U předchozího přecenění si všimněte, že položka z 1. ledna 2013 je přímým stornem položky pod sebou (od 3. ledna 2013). Dokonce účty hlavní knihy a typy zaúčtování jsou shodné. Dále si všimněte, že byl nastaven příznak **Oprava**.

Chování systému je stejné bez ohledu na to, zda je volba **Oprava** v části **Storno transakce** na stránce **Parametry hlavní knihy** nastavená na **Ano** nebo **Ne**.





