---
title: Přecenění měny v konsolidační společnosti
description: Toto téma popisuje, jak přecenit měnu v konsolidační společnosti.
author: roschlom
manager: AnnBe
ms.date: 10/02/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerExchAdjHist
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 33db12388c969b8dadb38bfacf4d9df333b78bd4
ms.sourcegitcommit: 092ef6a45f515b38be2a4481abdbe7518a636f85
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/16/2020
ms.locfileid: "4441325"
---
# <a name="currency-revaluation-in-a-consolidation-company"></a>Přecenění měny v konsolidační společnosti

[!include [banner](../includes/banner.md)]

Při konsolidaci dat z jedné zúčtovací měny na jinou musíte spustit přecenění měny, pokud dojde ke změně směnných kurzů, aby byly správně přehodnoceny zůstatky účtů. Při původní konsolidaci data použijte kartu **Převod měny** k výběru počátečních směnných kurzů pro převod při procesu konsolidace. Po zadání nového směnného kurzu (např. v dalším měsíci) je nutné přecenění zůstatků účtů. Nerealizované zisky nebo ztráty jsou pak odpovídajícím způsobem aktualizovány na základě nového směnného kurzu a data. Následující příklad znázorňuje účetní položky, které jsou vytvořeny během tohoto procesu.

## <a name="company-setup"></a>Nastavení společnosti
-   **Zdrojová/provozní společnost (USMF)** – americké dolary (USD) se používají jako zúčtovací a vykazovací měna.
-   **Konsolidovaná společnost (CON)** – euro (EUR) se používá jako zúčtovací a vykazovací měna.
    -   **Realizovaný zisk** – účet hlavní knihy 801500
    -   **Realizovaná ztráta** – účet hlavní knihy 801600
    -   **Nerealizovaný zisk** – účet hlavní knihy 801600
    -   **Nerealizovaná ztráta** – účet hlavní knihy 801400

## <a name="original-transactions"></a>Původní transakce
### <a name="cash-receipt-transactions-in-usmf"></a>Transakce příjmů v hotovosti v USMF

| Datum       | Účet hlavní knihy               | Měna | Částka |
|------------|------------------------------|----------|--------|
| 11. 10. 2015 | 110110 – Hotovost                | USD      | 500    |
| 11. 10. 2015 | 130100 – Pohledávky | USD      | -500   |

## <a name="exchange-rates"></a>Směnné kurzy

| Z měny | Do měny | Počáteční datum | Směnný kurz |
|---------------|-------------|------------|---------------|
| EUR           | USD         | 1. 10. 2015  | 200           |
| EUR           | USD         | 1. 11. 2015  | 150           |
| EUR           | USD         | 1. 12. 2012  | 100           |

## <a name="perform-the-consolidation-for-october-2015"></a>Provedení konsolidace pro říjen roku 2015
### <a name="balances-in-the-consolidation-company"></a>Zůstatky v konsolidované společnosti

| Účet hlavní knihy | Měna | Částka | Výpočet    |
|----------------|----------|--------|----------------|
| 110110         | EUR      | 250    | 500 USD × 50 %  |
| 130100         | EUR      | -250   | -500 USD × 50 % |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a>Provedení přecenění měny pro účty od 1. října 2015 do 30. listopadu 2015
### <a name="balances-in-the-consolidation-company"></a>Zůstatky v konsolidované společnosti

| Účet hlavní knihy | Měna | Částka  | Výpočet                        |
|----------------|----------|---------|------------------------------------|
| 110110         | EUR      | 333,33  | Původní částka 500 × 66.6667%  |
| 130100         | EUR      | -333,33 | Původní částka -500 × 66.6667% |
| 801400         | EUR      | 83,33   | 333,33 – 250                       |
| 801600         | EUR      | -83,33  | -333,33 – (-250)                   |

Zobrazí se další transakce pro částky v měně vykazování.

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a>Provedení přecenění měny pro účty od 1. října 2015 do 31. prosince 2015
### <a name="balances-in-the-consolidation-company"></a>Zůstatky v konsolidované společnosti

| Účet hlavní knihy | Měna | Částka  | Výpočet                                          |
|----------------|----------|---------|------------------------------------------------------|
| 110110         | EUR      | 500,00  | Původní částka 500 × 1                           |
| 130100         | EUR      | -500,00 | Původní částka -500 × 1                          |
| 801400         | EUR      | 250     | 500 – 333,33 = 166,67 166,67 + 83,33 = 250           |
| 801600         | EUR      | -250    | -500 – (-333,33) = -166,67 -166,67 + (-83,33) = -250 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]