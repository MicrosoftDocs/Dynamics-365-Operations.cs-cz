---
title: Výpočet a zaokrouhlování DPH
description: Tento článek poskytuje přehled výpočtu a zaokrouhlování DPH a vysvětluje parametry výpočtu DPH a nastavení zaokrouhlování.
author: wangchen
ms.date: 06/01/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: kfend
ms.custom:
- "13111"
- intro-internal
ms.assetid: fe5fdc7f-9834-49fb-a611-1dd9c289619d
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2022-05-31
ms.dyn365.ops.version: AX 10.0.28
ms.openlocfilehash: aa3564f0fcf4a958637ba4a5cdcc497bffc50000
ms.sourcegitcommit: 8b716849707ec96d1cb4cac85b9e782dc25f5a70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/07/2022
ms.locfileid: "8939226"
---
# <a name="sales-tax-calculation-and-rounding"></a>Výpočet a zaokrouhlování DPH

[!include [banner](../includes/banner.md)]

Tento článek poskytuje přehled výpočtu a zaokrouhlování DPH v Microsoft Dynamics 365 Finance. Vysvětluje také parametry, které se používají v nastavení pro výpočet a zaokrouhlování DPH, a jak tyto parametry spolupracují.

## <a name="parameters"></a>Parametry

Výpočet a zaokrouhlování řídí několik parametrů:

- **Metoda výpočtu** – Tento parametr se nastavuje na stránce **Parametry hlavní knihy** a definuje, zda se částka základu daně počítá na doklad nebo na řádek. Pokud je parametr **Základ marže** pro kód DPH nastaven na **Čistá částka zůstatku faktury**, částka základu daně se počítá vždy na doklad, bez ohledu na nastavení tohoto parametru.
- **Zaokrouhlení** – Tento parametr se nastavuje pro skupinu DPH a definuje, zda se částka daně zaokrouhlí podle kódu DPH nebo podle kombinace kódů DPH.
- **Původ** – Tento parametr se nastavuje pro kód DPH a definuje způsob výpočtu částky daně. Více informací najdete v části [Metody výpočtu DPH v poli Původ](sales-tax-calculation-methods-origin-field.md).
- **Základ marže** - Tento parametr je nastaven na kód DPH u určuje částku, která je použita k výběru odpovídající sazby daně ze sazeb na stránce **Hodnoty kódů DPH**. Více informací najdete v části [Sazby DPH na základě polí Základ marže a Metody výpočtu](marginal-base-field.md).
- **Pravidlo zaokrouhlování DPH** – Tento parametr se nastavuje pro kód DPH a definuje způsob zaokrouhlení stanovené částky DPH, včetně přesnosti zaokrouhlení a způsobu zaokrouhlení.

Zbytek tohoto článku představuje některé typické příklady výpočtu a zaokrouhlování DPH, které využívají kombinaci předchozích parametrů.

## <a name="scenario-for-the-examples"></a>Scénář pro příklady

- Na zdanitelném dokladu jsou dva řádky a částka základu daně pro každý řádek je 42,42.
- Pro každý řádek jsou definovány dva kódy DPH: kód DPH 1 a kód DPH 2.
- Daňová sazba pro daňový kód 1 i daňový kód 2 je 10 procent.
- Cena neobsahuje daň.
- Přesnost zaokrouhlení je 0,01.
- Metoda zaokrouhlení je **Zaokrouhlit nahoru**.

## <a name="example-1"></a>Příklad 1

### <a name="parameter-values"></a>Hodnoty parametrů

| Metoda výpočtu | Zaokrouhlení    | Původ                   | Základ marže       |
| ------------------ | -------------- | ------------------------ | ------------------- |
| Řádek               | Kód DPH | Procento z čisté částky | Čistá částka za řádek |

### <a name="calculation-and-rounding-behavior"></a>Chování výpočtu a zaokrouhlení

| Číslo řádku | Kód DPH | Původní částka | Částka prodejní daně |
| ------------| ---------------| --------------| -----------------|
| 1           | Kód 1         | 42.42         | 4.25             |
| 1           | Kód 2         | 42.42         | 4.25             |
| 2           | Kód 1         | 42.42         | 4.25             |
| 2           | Kód 2         | 42.42         | 4.25             |

Částka základu daně se počítá po řádcích:

- **Řádek 1:** 42,42
- **Řádek 2:** 42,42

Částka daně se počítá podle kódu DPH:

- **Řádek 1:**

    - Částka daně pro kód DPH 1 = 42,42 &times; 10 procent = 4,242
    - Částka daně pro kód DPH 2 = 42,42 &times; 10 procent = 4,242

- **Řádek 2:**

    - Částka daně pro kód DPH 1 = 42,42 &times; 10 procent = 4,242
    - Částka daně pro kód DPH 2 = 42,42 &times; 10 procent = 4,242

Částka daně se zaokrouhluje podle kódu DPH:

- **Řádek 1:**

    - Zaokrouhlená částka daně pro kód DPH 1 = 4,25
    - Zaokrouhlená částka daně pro kód DPH 2 = 4,25

- **Řádek 2:**

    - Zaokrouhlená částka daně pro kód DPH 1 = 4,25
    - Zaokrouhlená částka daně pro kód DPH 2 = 4,25

## <a name="example-2"></a>Příklad 2

### <a name="parameter-values"></a>Hodnoty parametrů

| Metoda výpočtu | Zaokrouhlení    | Původ                   | Základ marže                 |
| ------------------ | -------------- | ------------------------ | ----------------------------- |
| Řádek/celkem         | Kód DPH | Procento z čisté částky | Čistá částka zůstatku faktury |

### <a name="calculation-and-rounding-behavior"></a>Chování výpočtu a zaokrouhlení

| Číslo řádku | Kód DPH | Původní částka | Částka prodejní daně |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kód 1         | 42.42         | 4.25             |
| 1           | Kód 2         | 42.42         | 4.25             |
| 2           | Kód 1         | 42.42         | 4.24             |
| 2           | Kód 2         | 42.42         | 4.24             |

Částka základu daně se počítá na základě dokumentu:

- Částka základu daně = 42,42 + 42,42 = 84,84

Částka daně se počítá podle kódu DPH:

- Částka daně pro kód DPH 1 = 84,84 &times; 10 procent = 8,484
- Částka daně pro kód DPH 2 = 84,84 &times; 10 procent = 8,484

Částka daně se zaokrouhluje podle kódu DPH:

- Zaokrouhlená částka daně pro kód DPH 1 = 8,49
- Zaokrouhlená částka daně pro kód DPH 2 = 8,49

Zaokrouhlená částka daně se přidělí každému řádku podle kódu DPH:

- Zaokrouhlenou částku daně pro kód daně z obratu 1 (8,49) přidělte na řádek 1 (4,25) a řádek 2 (4,24).
- Zaokrouhlenou částku daně pro kód daně z obratu 2 (8,49) přidělte na řádek 1 (4,25) a řádek 2 (4,24).

## <a name="example-3"></a>Příklad 3

### <a name="parameter-values"></a>Hodnoty parametrů

| Metoda výpočtu | Zaokrouhlení    | Původ                              | Základ marže       |
| ------------------ | -------------- | ----------------------------------- | ------------------- |
| Řádek               | Kód DPH | Vypočtené procento čisté částky | Čistá částka za řádek |

### <a name="calculation-and-rounding-behavior"></a>Chování výpočtu a zaokrouhlení

| Číslo řádku | Kód DPH | Původní částka | Částka prodejní daně |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kód 1         | 42.42         | 4.72             |
| 1           | Kód 2         | 42.42         | 4.72             |
| 2           | Kód 1         | 42.42         | 4.72             |
| 2           | Kód 2         | 42.42         | 4.72             |

Částka základu daně se počítá po řádcích:

- **Řádek 1:** 42,42
- **Řádek 2:** 42,42

Částka daně se počítá podle kódu DPH:

- **Řádek 1:**

    - Částka daně pro kód DPH 1 = 42,42 &times; 10 procent &divide; (1 - 10 procent) = 4,7133
    - Částka daně pro kód DPH 2 = 42,42 &times; 10 procent &divide; (1 - 10 procent) = 4,7133

- **Řádek 2:**

    - Částka daně pro kód DPH 1 = 42,42 &times; 10 procent &divide; (1 - 10 procent) = 4,7133
    - Částka daně pro kód DPH 2 = 42,42 &times; 10 procent &divide; (1 - 10 procent) = 4,7133

Částka daně se zaokrouhluje podle kódu DPH:

- **Řádek 1:**

    - Zaokrouhlená částka daně pro kód DPH 1 = 4,72
    - Zaokrouhlená částka daně pro kód DPH 2 = 4,72

- **Řádek 2:**

    - Zaokrouhlená částka daně pro kód DPH 1 = 4,72
    - Zaokrouhlená částka daně pro kód DPH 2 = 4,72

## <a name="example-4"></a>Příklad 4

### <a name="parameter-values"></a>Hodnoty parametrů

| Metoda výpočtu | Zaokrouhlení    | Původ                              | Základ marže                 |
| ------------------ | -------------- | ----------------------------------- | ----------------------------- |
| Řádek/celkem         | Kód DPH | Vypočtené procento čisté částky | Čistá částka zůstatku faktury |

### <a name="calculation-and-rounding-behavior"></a>Chování výpočtu a zaokrouhlení

| Číslo řádku | Kód DPH | Původní částka | Částka prodejní daně |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kód 1         | 42.42         | 4.72             |
| 1           | Kód 2         | 42.42         | 4.72             |
| 2           | Kód 1         | 42.42         | 4.71             |
| 2           | Kód 2         | 42.42         | 4.71             |

Částka základu daně se počítá na základě dokumentu:

- Částka základu daně = 42,42 + 42,42 = 84,84

Částka daně se počítá podle kódu DPH:

- Částka daně pro kód DPH 1 = 84,84 &times; 10 procent &divide; (1 - 10 procent) = 9,4267
- Částka daně pro kód DPH 2 = 84,84 &times; 10 procent &divide; (1 - 10 procent) = 9,4267

Částka daně se zaokrouhluje podle kódu DPH:

- Zaokrouhlená částka daně pro kód DPH 1 = 9,43
- Zaokrouhlená částka daně pro kód DPH 2 = 9,43

Zaokrouhlená částka daně se přidělí každému řádku podle kódu DPH:

- Částku daně pro kód daně z obratu 1 (9,43) přidělte na řádek 1 (4,72) a řádek 2 (4,71).
- Částku daně pro kód daně z obratu 2 (9,43) přidělte na řádek 1 (4,72) a řádek 2 (4,71).

## <a name="example-5"></a>Příklad 5

### <a name="parameter-values"></a>Hodnoty parametrů

| Metoda výpočtu | Zaokrouhlení                | Původ                   | Základ marže       |
| ------------------ | -------------------------- | ------------------------ | ------------------- |
| Řádek               | Kombinace kódu DPH | Procento z čisté částky | Čistá částka za řádek |

### <a name="calculation-and-rounding-behavior"></a>Chování výpočtu a zaokrouhlení

| Číslo řádku | Kód DPH | Původní částka | Částka prodejní daně |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kód 1         | 42.42         | 4.25             |
| 1           | Kód 2         | 42.42         | 4.24             |
| 2           | Kód 1         | 42.42         | 4.24             |
| 2           | Kód 2         | 42.42         | 4.24             |

Částka základu daně se počítá po řádcích:

- **Řádek 1:** 42,42
- **Řádek 2:** 42,42

Částka daně se počítá podle kódu DPH:

- **Řádek 1:**

    - Částka daně pro kód DPH 1 = 42,42 &times; 10 procent = 4,242
    - Částka daně pro kód DPH 2 = 42,42 &times; 10 procent = 4,242

- **Řádek 2:**

    - Částka daně pro kód DPH 1 = 42,42 &times; 10 procent = 4,242
    - Částka daně pro kód DPH 2 = 42,42 &times; 10 procent = 4,242

Částka daně se zaokrouhluje podle kombinace kódů DPH:

- Celková částka DPH = 4,242 + 4,242 + 4,242 + 4,242 = 16,968, což se zaokrouhlí nahoru na 16,97

Zaokrouhlená částka daně se přidělí každému řádku podle kódu DPH:

- Přidělte částku DPH (16,97) na řádek 1 a řádek 2:

    - **Řádek 1:**

        - Částka daně pro kód DPH 1 = 4,25
        - Částka daně pro kód DPH 2 = 4,24

    - **Řádek 2:**

        - Částka daně pro kód DPH 1 = 4,24
        - Částka daně pro kód DPH 2 = 4,24

## <a name="example-6"></a>Příklad 6

### <a name="parameter-values"></a>Hodnoty parametrů

| Metoda výpočtu | Zaokrouhlení                | Původ                   | Základ marže                 |
| ------------------ | -------------------------- | ------------------------ | ----------------------------- |
| Řádek/celkem         | Kombinace kódu DPH | Procento z čisté částky | Čistá částka zůstatku faktury |

### <a name="calculation-and-rounding-behavior"></a>Chování výpočtu a zaokrouhlení

| Číslo řádku | Kód DPH | Původní částka | Částka prodejní daně |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kód 1         | 42.42         | 4.25             |
| 1           | Kód 2         | 42.42         | 4.24             |
| 2           | Kód 1         | 42.42         | 4.24             |
| 2           | Kód 2         | 42.42         | 4.24             |

Částka základu daně se počítá na základě dokumentu:

- Částka základu daně = 42,42 + 42,42 = 84,84

Částka daně se počítá podle kódu DPH:

- Částka daně pro kód DPH 1 = 84,84 &times; 10 procent = 8,484
- Částka daně pro kód DPH 2 = 84,84 &times; 10 procent = 8,484

Částka daně se zaokrouhluje podle kombinace kódů DPH:

- Celková částka DPH = 8,484 + 8,484 = 16,968, což se zaokrouhlí nahoru na 16,97

Zaokrouhlená částka daně se přidělí každému řádku podle kódu DPH:

- Přidělte částku DPH (16,97) na řádek 1 a řádek 2:

    - **Řádek 1:**

        - Částka daně pro kód DPH 1 = 4,25
        - Částka daně pro kód DPH 2 = 4,24

    - **Řádek 2:**

        - Částka daně pro kód DPH 1 = 4,24
        - Částka daně pro kód DPH 2 = 4,24

## <a name="example-7"></a>Příklad 7

### <a name="parameter-values"></a>Hodnoty parametrů

| Metoda výpočtu | Zaokrouhlení                | Původ                              | Základ marže       |
| ------------------ | -------------------------- | ----------------------------------- | ------------------- |
| Řádek               | Kombinace kódu DPH | Vypočtené procento čisté částky | Čistá částka za řádek |

### <a name="calculation-and-rounding-behavior"></a>Chování výpočtu a zaokrouhlení

| Číslo řádku | Kód DPH | Původní částka | Částka prodejní daně |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kód 1         | 42.42         | 4.72             |
| 1           | Kód 2         | 42.42         | 4.71             |
| 2           | Kód 1         | 42.42         | 4.71             |
| 2           | Kód 2         | 42.42         | 4.72             |

Částka základu daně se počítá po řádcích:

- **Řádek 1:** 42,42
- **Řádek 2:** 42,42

Částka daně se počítá podle kódu DPH:

- **Řádek 1:**

    - Částka daně pro kód DPH 1 = 42,42 &times; 10 procent &divide; (1 - 10 procent) = 4,7133
    - Částka daně pro kód DPH 2 = 42,42 &times; 10 procent &divide; (1 - 10 procent) = 4,7133

- **Řádek 2:**

    - Částka daně pro kód DPH 1 = 42,42 &times; 10 procent &divide; (1 - 10 procent) = 4,7133
    - Částka daně pro kód DPH 2 = 42,42 &times; 10 procent &divide; (1 - 10 procent) = 4,7133

Částka daně se zaokrouhluje podle kombinace kódů DPH:

- Celková částka DPH = 4,7133 + 4,7133 + 4,7133 + 4,7133 = 18,8532, což se zaokrouhlí nahoru na 18,86

Zaokrouhlená částka daně se přidělí každému řádku podle kódu DPH:

- Přidělte částku DPH (18,86) na řádek 1 a řádek 2:

    - **Řádek 1:**

        - Částka daně pro kód DPH 1 = 4,72
        - Částka daně pro kód DPH 2 = 4,71

    - **Řádek 2:**

        - Částka daně pro kód DPH 1 = 4,71
        - Částka daně pro kód DPH 2 = 4,72

## <a name="example-8"></a>Příklad 8

### <a name="parameter-values"></a>Hodnoty parametrů

| Metoda výpočtu | Zaokrouhlení                | Původ                              | Základ marže                 |
| ------------------ | -------------------------- | ----------------------------------- | ----------------------------- |
| Řádek/celkem         | Kombinace kódu DPH | Vypočtené procento čisté částky | Čistá částka zůstatku faktury |

### <a name="calculation-and-rounding-behavior"></a>Chování výpočtu a zaokrouhlení

| Číslo řádku | Kód DPH | Původní částka | Částka prodejní daně |
| ----------- | -------------- | ------------- | ---------------- |
| 1           | Kód 1         | 42.42         | 4.72             |
| 1           | Kód 2         | 42.42         | 4.71             |
| 2           | Kód 1         | 42.42         | 4.71             |
| 2           | Kód 2         | 42.42         | 4.72             |

Částka základu daně se počítá na základě dokumentu:

- Částka základu daně = 42,42 + 42,42 = 84,84

Částka daně se počítá podle kódu DPH:

- Částka daně pro kód DPH 1 = 84,84 &times; 10 procent &divide; (1 - 10 procent) = 9,4267
- Částka daně pro kód DPH 2 = 84,84 &times; 10 procent &divide; (1 - 10 procent) = 9,4267

Částka daně se zaokrouhluje podle kombinace kódů DPH:

- Celková částka DPH = 9,4267 + 9,4267 = 18,8534, což se zaokrouhlí nahoru na 18,86

Zaokrouhlená částka daně se přidělí každému řádku podle kódu DPH:

- Přidělte částku DPH (18,86) na řádek 1 a řádek 2:

    - **Řádek 1:**

        - Částka daně pro kód DPH 1 = 4,72
        - Částka daně pro kód DPH 2 = 4,71

    - **Řádek 2:**

        - Částka daně pro kód DPH 1 = 4,71
        - Částka daně pro kód DPH 2 = 4,72

## <a name="additional-resources"></a>Další prostředky

- [Metody výpočtu DPH v poli Zdroj](sales-tax-calculation-methods-origin-field.md)
- [Sazby DPH na základě polí Základ marže a Metody výpočtu](marginal-base-field.md)
- [Možnosti výpočtu celé částky a intervalu pro kódy daně z prodeje](whole-amount-interval-options-sales-tax-codes.md)
