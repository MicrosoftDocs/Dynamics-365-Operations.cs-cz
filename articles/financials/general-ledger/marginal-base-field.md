---
title: Sazby DPH na základě polí Základ marže a Metody výpočtu
description: Toto téma vysvětluje, jak hodnoty v poli Základ marže a Metoda výpočtu určují sazby daně v prodejních a nákupních transakcích.
author: ShylaThompson
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 7171
ms.assetid: 381fc309-b32a-4927-b5b8-fa1c31b0bd72
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0128743e608ec56bea2301ac576551065a1ff290
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "366413"
---
# <a name="sales-tax-rates-based-on-the-marginal-base-and-calculation-methods"></a>Sazby DPH na základě polí Základ marže a Metody výpočtu

[!include [banner](../includes/banner.md)]

Toto téma vysvětluje, jak hodnoty v poli Základ marže a Metoda výpočtu určují sazby daně v prodejních a nákupních transakcích.

Základ marže na pevné záložce Výpočet na stránce Kódy DPH určuje částku, která je použita k výběru odpovídající sazby daně ze sazeb na stránce Hodnoty kódu DPH. Typ částky v poli Základ marže v kombinaci s metodu v poli Metoda výpočtu určuje logiku, podle které je hledána správná sazba daně pro transakci. 

Různé kombinace hodnot v těchto polích poskytují velmi rozdílné výpočty DPH, jak je uvedeno v následujících příkladech. V příkladech jsou použity stejné hodnoty daňového období, jaké se nastavují pro každý kód DPH na stránce Hodnoty kódů DPH. Tuto stránku otevřete kliknutím na možnosti Kód prodejní daně &gt; Hodnoty na stránce Kódy DPH.

> [!Important]                                                                                                                  
> Je-li základ marže některého kódu DPH založen na částkách nebo jednotkách řádku, je nutné v poli Metoda výpočtu na stránce Parametry hlavní knihy nastavit hodnotu Řádek. |

## <a name="net-amount-per-line"></a> Čistá částka za řádek
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

Základ marže: **Čistá částka podle řádku** 

Způsob výpočtu: **Interval** 

Koupíte 8 lamp po 25,00 za kus. 

Čistá částka řádku faktury je 200,00. 

Daň se vypočítá následovně: 

Celková DPH = 50 x 30 % + 50 x 20 % + 100 x 10 % = 15 + 10 + 10 = 35,00 

Celková fakturovaná částka = 200,00 + 35,00 = 235,00 

**Odchylka** 

Pokud má faktura dva řádky se čtyřmi položkami na každém řádku, čistá částka na každém řádku je 100 a DPH se vypočítá následovně: 

DPH – řádek 1 = 50 x 30 % + 50 x 20 % = 15 + 10 = 25,00 

DPH - řádek 2 = 50 x 30 % + 50 x 20 % = 15 + 10 = 25,00 

Celková DPH = 25,00 + 25,00 = 50,00 

Celková fakturovaná částka = 200,00 + 50,00 = 250,00

## <a name="net-amount-per-unit"></a> Čistá částka za jednotku
Tuto možnost vyberte k určení sazeb DPH na základě hodnoty jednotlivých jednotek bez jakýchkoliv jiných daní. Je-li vybrán základ marže vycházející z jednotek, je nutné určit jednotku také pro kód DPH.

### <a name="example"></a>Příklad

Sazby DPH jsou nastaveny v následujících intervalech.

| Částka             | Daňová sazba |
|--------------------|----------|
| 0–50             | 30 %      |
| 50–100           | 20 %      |
| 100 - 0 (&gt; 100) | 10 %      |

Základ marže: **Čistá částka podle jednotky** 

Metoda výpočtu: **Celková částka** 

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
| 100 - 0 (&gt; 100) | 10 %      |

Základ marže: **Čistá částka zůstatku faktury** 

Metoda výpočtu: **Interval** Prodejní faktura obsahuje 2 řádky se 4 zářivkami na jednotlivých řádkách pro 25,00 ks. Čistá částka zůstatku faktury je 4 x 25,00 + 4 x 25,00 = 200,00. Daň se vypočítá takto: Celková DPH = 50 x 0,30 + 50 x 0,20 + 100 x 0,10 = 15 + 10 + 10 = 35,00 Celková fakturovaná částka = 200,00 + 35,00 = 235,00

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

Základ marže: **Hrubá částka za řádek** Metoda výpočtu: **Interval** Dále je zde vypočítán jiný kód daně pro zvláštní clo 5,00 na každou lampu. Toto clo je k čisté částce přidáno před výpočtem DPH. Koupíte 8 lamp po 25,00 za kus. Čistá částka řádku faktury je 200,00. Hrubá částka řádku faktury je 8 x 25,00 + 8 x 5,00 = 240,00. Daň se vypočítá takto: Celková DPH = 50 x 0,30 + 50 x 0,20 + 140 x 0,10 = 15 + 20 + 14 = 39,00 Celkové clo = 5,00 x 8 = 40,00 Celková fakturovaná částka = 200,00 + 39,00 + 40,00 = 279,00

**Odchylka** 

Pokud dojde k vytvoření faktury pomocí dvou řádků se čtyřmi položkami na každém řádku, čistá částka na řádek je 100,00. Hrubá částka (včetně cla 4 x 5,00) na každém řádku faktury by byla 120,00 a DPH se vypočte následujícím způsobem: DPH pro řádek faktury 1 = 50 x 0,30 + 50 x 0,20 + 20 x 0,10 = 15 + 10 + 2 = 27,00 DPH pro řádek faktury 2 = 50 x 0,30 + 50 x 0,20 + 20 x 0,10 = 15 + 10 + 2 = 27,00 Celková DPH = 27,00 + 27,00 = 54,00 Celkové clo = 5,00 x 8 = 40,00 Celková fakturovaná částka = 200,00 + 54,00 + 40,00 = 294,00

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
> Ve skupině DPH může být s touto hodnotou v poli Základ marže uveden pouze jeden kód DPH.

### <a name="example"></a>Příklad

Sazby DPH jsou nastaveny v následujících intervalech.

| Částka             | Daňová sazba |
|--------------------|----------|
| 0–50             | 30 %      |
| 50–100           | 20 %      |
| 100 - 0 (&gt; 100) | 10 %      |

Základ marže: **Faktura celkem včetně částek DPH** metoda výpočtu: **Interval**   
Pro každou lampu existuje speciální clo ve výši 5,00 eur. Toto clo je k čisté částce přidáno před výpočtem DPH. Koupíte 8 lamp po 25,00 za kus. Čistá částka faktury je 200,00. Hrubá částka faktury je 200,00 + (8 x 5,00) = 240,00. Daň se vypočítá takto: Celková DPH = 50 x 0,30 + 50 x 0,20 + 140 x 0,10 = 15 + 10 + 14 = 39,00 Celkové clo = 5,00 x 8 = 40,00 Celková fakturovaná částka = 200,00 + 39,00 + 40,00 = 279,00

Další informace viz [Možnost Celková částka a Interval výpočtu pro kódy DPH](whole-amount-interval-options-sales-tax-codes.md) a [Metody výpočtu DPH v poli Zdroj](sales-tax-calculation-methods-origin-field.md).



