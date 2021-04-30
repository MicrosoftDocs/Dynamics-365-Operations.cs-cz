---
title: Funkce intervalu úročení
description: Toto téma poskytuje informace, které vám pomohou vybrat si mezi měsíčními, čtvrtletními, pololetními a ročními intervaly úročení.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeaseDetail
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: f8c19a523251b0f1c90de746e380f58be4851ddd
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881293"
---
# <a name="compounding-interval-functionality"></a>Funkce intervalu úročení

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Toto téma poskytuje informace, které vám pomohou vybrat si mezi měsíčními, čtvrtletními, pololetními a ročními intervaly úročení. Funkce intervalu úročení se používá k určení počtu období úročení za rok v platebním kalendáři leasingu. Každý ze čtyř příkladů v tomto tématu ukazuje, jak bude platební kalendář leasingu vypadat pro jiný interval.

Nemůžete vybrat interval úročení, který je méně častý než frekvence plateb leasingu. Například čtvrtletní interval úročení nelze použít s měsíční frekvencí plateb a roční interval úročení nelze použít s pololetní platební frekvencí. Pokud zkusíte vybrat interval úročení, který je méně častý než frekvence plateb leasingu, zobrazí se chybová zpráva.

> [!NOTE]
> Ve všech čtyřech příkladech v tomto tématu se interval úročení shoduje s frekvencí plateb.

## <a name="examples"></a>Příklad

### <a name="setup-for-all-four-leases"></a>Nastavení pro všechny čtyři leasingy

Následující tabulky ukazují hodnoty, které jsou nastaveny na kartách **Obecné** a **Řádky platebního kalendáře** pro čtyři leasingy použité v těchto příkladech.

**Karta Obecné**

| Pole                      | Hodnota                        |
|----------------------------|------------------------------|
| Přírůstková výpůjční úroková sazba | **5 %**                       |
| Typ anuity               | **Běžná anuita**         |
| Interval úročení       | Viz jednotlivé příklady. |
| Četnost plateb          | **Měsíčně**                  |
| Datum zahájení          | **1. 1. 2020**                 |

**Karta Řádky platebního kalendáře**

| Pole             | Hodnota                        |
|-------------------|------------------------------|
| Počáteční datum        | **1. 1. 2020**                 |
| Období           | **120**                      |
| Interval období   | **Měsíce**                   |
| Koncové datum          | **31. 12. 2029**               |
| Četnost plateb | Viz jednotlivé příklady. |
| Částka platby    | **50,000**                   |

### <a name="lease-1-monthly-compounding-interval-and-monthly-payment-frequency"></a>Leasing 1: Měsíční interval úročení a měsíční frekvence plateb

V následující tabulce je uveden seznam prvních 12 měsíců platebního kalendáře. Mějte na paměti následující podrobnosti:

- Hodnota ve sloupci „Období“ se každý měsíc zvyšuje o 1, protože každý měsíc je novým intervalem úročení.
- Ve vzorci ve sloupci „Současná hodnota“ je sazba vydělena 12, protože existuje 12 období úročení za rok. Exponent (tj. horní index) se rovná hodnotě ve sloupci „Období“.

| Období | Měsíc | Datum       | Částka platby | Současná hodnota                                       |
|--------|-------|------------|----------------|-----------------------------------------------------|
| 1      | 1     | 31. 1. 2020  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>1</sup> = 49 792,53  |
| 2      | 2     | 29. 2. 2020  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>2</sup> = 49 585,92  |
| 3      | 3     | 31. 3. 2020  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>3</sup> = 49 380,17  |
| 4      | 4     | 30. 4. 2020  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>4</sup> = 49 175,28  |
| 5      | 5     | 31. 5. 2020  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>5</sup> = 48 971,23  |
| 6      | 6     | 30. 6. 2020  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>6</sup> = 48 768,03  |
| 7      | 7     | 31. 7. 2020  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>7</sup> = 48 565,67  |
| 8      | 8     | 31. 8. 2020  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>8</sup> = 48 364,15  |
| 9      | 9     | 30. 9. 2020  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>9</sup> = 48 163,47  |
| 10     | 10    | 31. 10. 2020 | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>10</sup> = 47 963,62 |
| 11     | 11    | 30. 11. 2020 | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>11</sup> = 47 764,61 |
| 12     | 12    | 31. 12. 2020 | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 12\])<sup>12</sup> = 47 566,41 |

### <a name="lease-2-quarterly-compounding-interval-and-quarterly-payment-frequency"></a>Leasing 2: Čtvrtletní interval úročení a čtvrtletní frekvence plateb

V následující tabulce je uveden seznam prvních 12 měsíců platebního kalendáře. Mějte na paměti následující podrobnosti:

- Hodnota ve sloupci „Období“ se každé tři měsíce (tedy každé čtvrtletí) zvyšuje o 1, protože každé čtvrtletí je novým intervalem úročení.
- Ve vzorci ve sloupci „Současná hodnota“ je sazba vydělena 4, protože existují 4 období úročení za rok. Exponent se rovná hodnotě ve sloupci „Období“.

| Období | Měsíc | Datum       | Částka platby | Současná hodnota                                     |
|--------|-------|------------|----------------|---------------------------------------------------|
| 1      | 1     | 31. 1. 2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 4\])<sup>1</sup> = 0           |
| 1      | 2     | 29. 2. 2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 4\])<sup>1</sup> = 0           |
| 1      | 3     | 31. 3. 2020  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 4\])<sup>1</sup> = 49 382,72 |
| 2      | 4     | 30. 4. 2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 4\])<sup>2</sup> = 0           |
| 2      | 5     | 31. 5. 2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 4\])<sup>2</sup> = 0           |
| 2      | 6     | 30. 6. 2020  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 4\])<sup>2</sup> = 48 773,05 |
| 3      | 7     | 31. 7. 2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 4\])<sup>3</sup> = 0           |
| 3      | 8     | 31. 8. 2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 4\])<sup>3</sup> = 0           |
| 3      | 9     | 30. 9. 2020  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 4\])<sup>3</sup> = 48 170,92 |
| 4      | 10    | 31. 10. 2020 | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 4\])<sup>4</sup> = 0           |
| 4      | 11    | 30. 11. 2020 | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 4\])<sup>4</sup> = 0           |
| 4      | 12    | 31. 12. 2020 | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 4\])<sup>4</sup> = 47 576,21 |

> [!NOTE]
> Pokud se typ anuity změní na **Splatná anuita**, bude platba provedena na začátku čtvrtletí místo na konci čtvrtletí.

### <a name="lease-3-semiannual-compounding-interval-and-semiannual-payment-frequency"></a>Leasing 3: Pololetní interval úročení a pololetní frekvence plateb

V následující tabulce je uveden seznam prvních 12 měsíců platebního kalendáře. Mějte na paměti následující podrobnosti:

- Hodnota ve sloupci „Období“ se každých šest měsíců (tedy pololetně) zvyšuje o 1, protože každé pololetí je novým intervalem úročení.
- Ve vzorci ve sloupci „Současná hodnota“ je sazba vydělena 2, protože existují dvě období úročení za rok. Exponent se rovná hodnotě ve sloupci „Období“.

| Období | Měsíc | Datum       | Částka platby | Současná hodnota                                     |
|--------|-------|------------|----------------|---------------------------------------------------|
| 1      | 1     | 31. 1. 2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 2\])<sup>1</sup> = 0           |
| 1      | 2     | 29. 2. 2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 2\])<sup>1</sup> = 0           |
| 1      | 3     | 31. 3. 2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 2\])<sup>1</sup> = 0           |
| 1      | 4     | 30. 4. 2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 2\])<sup>1</sup> = 0           |
| 1      | 5     | 31. 5. 2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 2\])<sup>1</sup> = 0           |
| 1      | 6     | 30. 6. 2020  | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 2\])<sup>1</sup> = 48 780,49 |
| 2      | 7     | 31. 7. 2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 2\])<sup>2</sup> = 0           |
| 2      | 8     | 31. 8. 2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 2\])<sup>2</sup> = 0           |
| 2      | 9     | 30. 9. 2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 2\])<sup>2</sup> = 0           |
| 2      | 10    | 31. 10. 2020 | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 2\])<sup>2</sup> = 0           |
| 2      | 11    | 30. 11. 2020 | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 2\])<sup>2</sup> = 0           |
| 2      | 12    | 31. 12. 2020 | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 2\])<sup>2</sup> = 47 590,72 |

> [!NOTE]
> Pokud se typ anuity změní na **Splatná anuita**, platba proběhne v lednu a červenci místo v červnu a prosinci.

### <a name="lease-4-annual-compounding-interval-and-annual-payment-frequency"></a>Leasing 4: Roční interval úročení a roční frekvence plateb

V následující tabulce je uveden seznam prvních 12 měsíců platebního kalendáře. Mějte na paměti následující podrobnosti:

- Hodnota ve sloupci „Období“ se každých 12 měsíců (tedy ročně) zvyšuje o 1, protože každý rok je novým intervalem úročení.
- Ve vzorci ve sloupci „Současná hodnota“ je sazba vydělena 1, protože existuje jedno období úročení za rok. Exponent se rovná hodnotě ve sloupci „Období“.

| Období | Měsíc | Datum       | Částka platby | Současná hodnota                                     |
|--------|-------|------------|----------------|---------------------------------------------------|
| 1      | 1     | 31. 1. 2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 2     | 29. 2. 2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 3     | 31. 3. 2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 4     | 30. 4. 2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 5     | 31. 5. 2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 6     | 30. 6. 2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 7     | 31. 7. 2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 8     | 31. 8. 2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 9     | 30. 9. 2020  | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 10    | 31. 10. 2020 | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 11    | 30. 11. 2020 | 0,00           | 0,00 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 0           |
| 1      | 12    | 31. 12. 2020 | 50,000.00      | 50 000 ÷ (1 + \[5 % ÷ 1\])<sup>1</sup> = 47 619,05 |

> [!NOTE]
> Pokud se typ anuity změní na **Splatná anuita**, platba proběhne v lednu místo v prosinci.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
