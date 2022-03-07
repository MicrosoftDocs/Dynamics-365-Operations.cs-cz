---
title: Úpravy kurzů
description: Toto téma uvádí informace o funkci úpravy směnného kurzu, která umožňuje uživatelům v právnickým osobách v Estonsku, Maďarsku, Litvě, České republice, Maďarsku, Lotyšku, Polsku a Rusku provádět hotovostní operace v systému.
author: ShylaThompson
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters
audience: Application User
ms.reviewer: kfend
ms.custom: 272683
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: kfend
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: df71afd293edf9bec51f4bb337516bb1ee8e2c33
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5002987"
---
# <a name="exchange-rate-adjustments"></a>Úpravy kurzů

[!include [banner](../includes/banner.md)]

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

### <a name="invoice"></a>Faktura

| Datum                             | Má dáti / Dal | Částky               | Účet hlavní knihy (HK)    | typ transakce             | Typ zaúčtování       | Kreditní | Oprava |
|----------------------------------|--------------|-----------------------|--------------------------------|------------------------------|--------------------|--------|------------|
| 1-Pro-12                         | Má Dáti        | 10,000 CAD/40,000 USD | Pohledávky                             | Faktura                      | Zůstatek odběratele   |        |            |
| 1-Pro-12                         | Kreditní       | 10,000 CAD/40,000 USD | Protiúčet                         | Faktura                      | Deník hlavní knihy     | X      |

### <a name="payment"></a>Platba

| Datum                             | Má dáti / Dal | Částky               | Účet hlavní knihy (HK)    | typ transakce             | Typ zaúčtování       | Kreditní | Oprava |
|----------------------------------|--------------|-----------------------|--------------------------------|------------------------------|--------------------|--------|------------|
| 3-led-13                         | Má Dáti        | 10,000 CAD/42,000 USD | Protiúčet                         | Platba                      | Deník hlavní knihy     |        |            |
| 3-led-13                         | Kreditní       | 10,000 CAD/42,000 USD | Pohledávky                             | Platba                      | Zůstatek odběratele   | X      |            |

### <a name="settlement"></a>Vyrovnání

| Datum                             | Má dáti / Dal | Částky               | Účet hlavní knihy (HK)    | typ transakce             | Typ zaúčtování       | Kreditní | Oprava |
|----------------------------------|--------------|-----------------------|--------------------------------|------------------------------|--------------------|--------|------------|
|3. ledna 2013 (= datum platby) | Má Dáti        | 0 CAD/2,000 USD       | Pohledávky                             | Zákazník                     | Zisk ze směnného kurzu |        |            |
3. ledna 2013 (= datum platby) | Kreditní       | 0 CAD/2,000 USD       | Zisk po úpravě v realizované měně   | Zákazník                     | Zisk ze směnného kurzu | X      |            |


### <a name="revaluation--standard-method-date--december-31-2012"></a>Přecenění (standardní metodou, datum = 31. prosince 2012)
Například u tohoto přecenění si všimněte, že položka ze 3. ledna 2013 je přímým stornem položky z 31. prosince 2012. Dokonce účty hlavní knihy a typy zaúčtování jsou shodné. Dále si všimněte, že byl nastaven příznak **Oprava**.

| Datum                             | Má dáti / Dal | Částky               | Účet hlavní knihy (HK)    | typ transakce             | Typ zaúčtování       | Kreditní | Oprava |
|----------------------------------|--------------|-----------------------|--------------------------------|------------------------------|--------------------|--------|------------|
| 31-Pro-12           | Má Dáti        | 0 CAD/5,000 USD       | Pohledávky                             | Přecenění cizí měny | Zisk ze směnného kurzu |        |            |
| 31-Pro-12           | Kreditní       | 0 CAD/5,000 USD       | Zisk po úpravě v nerealizované měně | Přecenění cizí měny | Zisk ze směnného kurzu | X      |            |
| 3-led-13            | Má Dáti        | 0 CAD/5,000 USD       | Pohledávky                             | Přecenění cizí měny | Zisk ze směnného kurzu |        | X          |
 3-led-13            | Kreditní       | 0 CAD/5,000 USD       | Zisk po úpravě v nerealizované měně | Přecenění cizí měny | Zisk ze směnného kurzu | X      | X          |


### <a name="revaluation-invoice-date-method-date--january-1-2013"></a>Přecenění (metoda data faktury, datum = 1. ledna 2013)
Například u tohoto přecenění si všimněte, že položka ze 1. ledna 2013 je přímým stornem položky z 3. ledna 2013. Dokonce účty hlavní knihy a typy zaúčtování jsou shodné. Dále si všimněte, že byl nastaven příznak **Oprava**.

| Datum   | Má dáti / Dal | Částky | Účet hlavní knihy (HK)| typ transakce| Typ zaúčtování| Kreditní | Oprava |
|--------|--------------|---------|----------------------------|----------------|--------|------------|--------------|
|1-led-13 | Má Dáti  | 0 CAD/5,000 USD | Pohledávky                             | Přecenění cizí měny | Zisk ze směnného kurzu |   | X |
|1-led-13 | Kreditní | 0 CAD/5,000 USD | Zisk po úpravě v nerealizované měně | Přecenění cizí měny | Zisk ze směnného kurzu | X | X |
|3-led-13 | Má Dáti  | 0 CAD/5,000 USD | Pohledávky                             | Přecenění cizí měny | Zisk ze směnného kurzu |   |   |
|3-led-13 | Kreditní | 0 CAD/5,000 USD | Zisk po úpravě v nerealizované měně | Přecenění cizí měny | Zisk ze směnného kurzu | X |   |

Chování systému je stejné bez ohledu na to, zda je volba **Oprava** v části **Storno transakce** na stránce **Parametry hlavní knihy** nastavená na **Ano** nebo **Ne**.



