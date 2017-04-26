---
title: "Na základě základ marže a metod výpočtu sazby DPH"
description: "Tento článek vysvětluje, jak hodnoty v poli Základ marže a Metoda výpočtu určují sazby daně v prodejních a nákupních transakcích."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: TaxTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 7171
ms.assetid: 381fc309-b32a-4927-b5b8-fa1c31b0bd72
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 114dee90b0fe525f0b3efabbf651d2804a22dd7d
ms.openlocfilehash: ad731401fe553cdc50665cc87aaac64dc48813f2
ms.lasthandoff: 03/31/2017


---

# <a name="sales-tax-rates-based-on-the-marginal-base-and-calculation-methods"></a>Na základě základ marže a metod výpočtu sazby DPH

[!include[banner](../includes/banner.md)]


Tento článek vysvětluje, jak hodnoty v poli Základ marže a Metoda výpočtu určují sazby daně v prodejních a nákupních transakcích.

Základ marže na pevné záložce Výpočet na stránce Kódy DPH určuje částku, která je použita k výběru odpovídající sazby daně ze sazeb na stránce Hodnoty kódu DPH. Typ částky v poli Základ marže v kombinaci s metodu v poli Metoda výpočtu určuje logiku, podle které je hledána správná sazba daně pro transakci. 

Různé kombinace hodnot v těchto polích poskytují velmi rozdílné výpočty DPH, jak je uvedeno v následujících příkladech. V příkladech jsou použity stejné hodnoty daňového období, jaké se nastavují pro každý kód DPH na stránce Hodnoty kódů DPH. Chcete-li tuto stránku otevřít, klepněte na tlačítko kód DPH &gt;hodnoty na stránce kódy DPH.

> [!Important]                                                                                                                  
> Je-li základ marže některého kódu DPH založen na částkách nebo jednotkách řádku, je nutné v poli Metoda výpočtu na stránce Parametry hlavní knihy nastavit hodnotu Řádek. |

## <a name="net-amount-per-line"></a>Čistá částka za řádek
Tuto možnost vyberte k určení sazeb DPH na základě čisté částky na řádcích faktury bez jakýchkoliv jiných daní.

### <a name="example"></a>Příklad

Sazby DPH jsou nastaveny v následujících intervalech.

| Intervaly pro částky    | Daňová sazba |
|--------------------|----------|
| 0–50             | 30 %      |
| 50–100           | 20 %      |
| 100 - 0 (&gt; 100) | 10 %      |

> [!NOTE]                                                                                                             
> Horní limit 0 v posledním intervalu značí zahrnutí všech částek větších než 100 do intervalu.

Základ marže: **čistá částka za řádek** 

Metoda výpočtu: **Interval** 

Koupíte 8 lamp po 25,00 za kus. 

Čistá částka řádku faktury je 200,00. 

Daň se vypočítá následovně: 

Celkové DPH = 50 x 30 % + 50 x 20 % + 100 x 10 % = 15 + 10 + 10 = 35.00 

Celková částka faktury = 200,00 + 35.00 = 235.00 

**Variation** 

Jestliže faktura obsahuje dva řádky se čtyřmi položkami na každém řádku, je čistá částka na každém řádku 100,00 a DPH se vypočítá takto: 

DPH řádku % 1 = 50 x 30 + 50 x 20 % = 15 + 10 = 25,00 

DPH, řádek % 2 = 50 x 30 + 50 x 20 % = 15 + 10 = 25,00 

Celkové DPH = 25,00 + 25,00 = 50,00 

Celková částka faktury = 200,00 + 50,00 = 250,00

## <a name="net-amount-per-unit"></a> Čistá částka za jednotku
Tuto možnost vyberte k určení sazeb DPH na základě hodnoty jednotlivých jednotek bez jakýchkoliv jiných daní. Je-li vybrán základ marže vycházející z jednotek, je nutné určit jednotku také pro kód DPH.

### <a name="example"></a>Příklad

Sazby DPH jsou nastaveny v následujících intervalech.

| Částka             | Daňová sazba |
|--------------------|----------|
| 0–50             | 30 %      |
| 50–100           | 20 %      |
| 100 - 0 (&gt; 100) | 10 %      |

Základ marže: **čistá částka za jednotku** 

Metoda výpočtu: **celá částka** 

Koupíte 8 lamp po 25,00 za kus. 

Čistá částka řádku faktury je 200,00. 

Daň se vypočítá takto: DPH za jednotku = 25,00 x 30 % = 7,50 Celková DPH = 7,50 x 8 jednotek = 60,00 Celková fakturovaná částka = 200,00 + 60,00 = 260,00

## <a name="net-amount-of-invoice-balance"></a> Čistá částka zůstatku faktury

Tuto možnost vyberte k určení sazeb DPH na základě celkové hodnoty faktury bez jakýchkoliv jiných daní.

### <a name="example"></a>Příklad

Sazby DPH jsou nastaveny v následujících intervalech.

| Částka            | Daňová sazba |
|-------------------|----------|
| 0–50            | 30 %      |
| 50–100          | 20 %      |
| 100 -0 (&gt; 100) | 10 %      |

Základ marže: **čistá částka zůstatku faktury** 

Metoda výpočtu: **Interval** prodejní faktury obsahuje 2 řádky se 4 zářivky na jednotlivé řádky pro 25,00 každý. Čistá částka zůstatku faktury je 4 x 25,00 + 4 x 25,00 = 200,00. Daň se vypočítá takto: Celková DPH = 50 x 0,30 + 50 x 0,20 + 100 x 0,10 = 15 + 10 + 10 = 35,00 Celková fakturovaná částka = 200,00 + 35,00 = 235,00

## <a name="gross-amount-per-line"></a> Hrubá částka za řádek

Tuto možnost vyberte k určení sazeb DPH na základě hodnoty řádku včetně jakýchkoliv jiných daní pro daný řádek.

> [!NOTE]
> Ve skupině DPH může být s touto hodnotou v poli Základ marže uveden pouze jeden kód DPH.

### <a name="example"></a>Příklad

Sazby DPH jsou nastaveny v následujících intervalech.

| Částka             | Daňová sazba |
|--------------------|----------|
| 0–50             | 30 %      |
| 50–100           | 20 %      |
| 100 - 0 (&gt; 100) | 10 %      |

Základ marže: **Hrubá částka za řádek** Metoda výpočtu: **Interval** Dále je zde vypočítán jiný kód daně pro zvláštní clo 5,00 na každou lampu. Toto clo je k čisté částce přidáno před výpočtem DPH. Koupíte 8 lamp po 25,00 za kus. Čistá částka řádku faktury je 200,00. Hrubá částka řádku faktury je 8 x 25,00 + 8 x 5,00 = 240,00. Daň se vypočte takto: celkové DPH = 50 x 0,30 + 50 x 0,20 + 140 x 0,10 = 15 + 20 + 14 = 39.00 celkem clo = 5,00 x 8 = 40,00 celková částka faktury = 200,00 + 39.00 + 40,00 = 279.00

**Variation** 

Pokud faktura je vytvořena pomocí 2 řádky faktury s 4 položky na každém řádku, je čistá částka za řádek faktury 100,00. Hrubá částka (včetně cla 4 x 5,00) na každém řádku faktury by byla 120,00 a DPH se vypočte následujícím způsobem: DPH pro řádek faktury 1 = 50 x 0,30 + 50 x 0,20 + 20 x 0,10 = 15 + 10 + 2 = 27,00 DPH pro řádek faktury 2 = 50 x 0,30 + 50 x 0,20 + 20 x 0,10 = 15 + 10 + 2 = 27,00 Celková DPH = 27,00 + 27,00 = 54,00 Celkové clo = 5,00 x 8 = 40,00 Celková fakturovaná částka = 200,00 + 54,00 + 40,00 = 294,00

## <a name="gross-amount-per-unit"></a> Hrubá částka za jednotku

Tuto možnost vyberte k určení sazeb DPH na základě hodnoty jednotky včetně jakýchkoliv jiných daní.

> [!NOTE]
> Ve skupině DPH může být s touto hodnotou v poli Základ marže uveden pouze jeden kód DPH.

### <a name="example"></a>Příklad

Sazby DPH jsou nastaveny v následujících intervalech.

| Částka             | Daňová sazba |
|--------------------|----------|
| 0–50             | 30 %      |
| 50–100           | 20 %      |
| 100 - 0 (&gt; 100) | 10 %      |

Základ marže: **Hrubá částka za jednotku** Je uloženo zvláštní clo 5,00 na každou lampu. Toto clo je k čisté částce přidáno před výpočtem DPH. Koupíte 8 lamp po 25,00 za kus. Hrubá částka na jednotku je 30,00. Daň se vypočítá takto: DPH za jednotku = 30 x 30 % = 9,00 Celková DPH = 9,00 x 8 = 72,00 Celkové clo= 5,00 x 8 = 40,00 Celková fakturovaná částka = 200,00 + 72,00 + 40,00 = 312,00

## <a name="invoice-total-incl-other-sales-tax-amounts"></a> Celková fakturovaná částka, včetně částek DPH

Tuto možnost vyberte k určení sazeb DPH na základě celkové hodnoty faktury včetně jakýchkoliv jiných daní.
> [!NOTE]
> Ve skupině DPH můžete mít pouze jeden kód DPH s Tento výběr marginální základní pole

### <a name="example"></a>Příklad

Sazby DPH jsou nastaveny v následujících intervalech.

| Částka             | Daňová sazba |
|--------------------|----------|
| 0–50             | 30 %      |
| 50–100           | 20 %      |
| 100 - 0 (&gt; 100) | 10 %      |

Základ marže: **Faktura celkem včetně částek DPH** metoda výpočtu: **Interval**   
Existuje zvláštní clo 5.00 na každého světlometu nebo svítilny. Toto clo je k čisté částce přidáno před výpočtem DPH. Koupíte 8 lamp po 25,00 za kus. Čistá částka faktury je 200,00. Hrubá částka faktury je 200,00 + (8 x 5,00) = 240,00. Daň se vypočítá takto: Celková DPH = 50 x 0,30 + 50 x 0,20 + 140 x 0,10 = 15 + 10 + 14 = 39,00 Celkové clo = 5,00 x 8 = 40,00 Celková fakturovaná částka = 200,00 + 39,00 + 40,00 = 279,00

Další informace naleznete v tématu [celá částka a Interval možnosti výpočtů pro kódy DPH](whole-amount-interval-options-sales-tax-codes.md) a [metody výpočtu DPH v poli Původ](sales-tax-calculation-methods-origin-field.md).




