---
title: Časové rozlišení volna na základě odpracovaných hodin
description: Toto téma popisuje, jak lze nakonfigurovat plány pracovního vlna pro časové rozlišení volna na základě odpracovaných hodin.
author: andreabichsel
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-09-17
ms.dyn365.ops.version: ''
ms.openlocfilehash: 229ae14b9e2dedcd0ade094a772f16c0524d32a7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460593"
---
# <a name="accrue-time-off-based-on-hours-worked"></a>Časové rozlišení volna na základě odpracovaných hodin

## <a name="overview"></a>Přehled

Organizace se zaměstnanci s hodinovou mzdou mohou přidělit volno na základě odpracovaných hodin, namísto odpracovaných let v organizaci. Data odpracovaných hodin se obvykle ukládají v systému času a docházky. 

## <a name="leave-plans"></a>Plány pracovního volna

V rámci plánu pracovního volna mohou být typem časového rozlišení buď odpracované měsíce nebo odpracované hodiny. Při výběru odpracovaných hodin existují dva typy hodin, které lze použít pro časové rozlišení: pravidelné a přesčasové.

K nastavení plánu pracovního volna pro použití odpracovaných hodin postupujte takto:

1. Na stránce **Plány pracovního volna a absence** klikněte na **Vytvořit nový plán**.
2. Zadejte název pro plán pracovního volna.
3. Zvolte frekvenci časového rozlišení pro plán.
5. Vyberte počáteční datum plánu.
6. Zvolte základ období časového rozlišení a zvolte podle potřeby datum specifické pro zaměstnance.
7. Pro plán časového rozlišení zvolte **Odpracované hodiny** pro typ časového rozlišení.
8. Zvolte typ hodin, který se použije pro časové rozlišení.
9. Zadejte počet odpracovaných hodin a přidruženou časově rozlišenou částku, minimální zůstatek a maximální částku pro převedení.

Zpracování časového rozlišení pro plány odpracovaných hodin používají frekvenci časového rozlišení, spolu se základem období časového rozlišení, pro určení hodin, které mají být časově rozlišeny.

## <a name="annual-accrual-frequency"></a>Roční frekvence časového rozlišení

| Datum udělení časového rozlišení    | Úroveň odpracovaných hodin    | Částka časového rozlišení        | Data odpracovaných hodin   | Skutečné hodnoty odpracovaných hodin| Odměna               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 31. 12. 2018            | 2080                 | 144                   | 1 1. 2018 - 31. 12. 2018  | 2085                | 144                 |        
| 31. 12. 2018            | 2080                 | 144                   | 1 1. 2018 - 31. 12. 2018  | 2000                | 0                 |


## <a name="monthly-accrual-frequency"></a>Měsíční frekvence časového rozlišení

| Datum udělení časového rozlišení    | Úroveň odpracovaných hodin    | Částka časového rozlišení        | Data odpracovaných hodin   | Skutečné hodnoty odpracovaných hodin| Odměna               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 31. 8. 2018             | 160                  | 12                    | 1. 8. 2018 - 31. 8. 2018   | 184                 | 12                  |        
| 31. 8. 2018             | 160                  | 3                     | 1. 8. 2018 - 31. 8. 2018   | 184                 | 3                   |

## <a name="semi-monthly-accrual-frequency"></a>Čtrnáctidenní frekvence časového rozlišení

| Datum udělení časového rozlišení    | Úroveň odpracovaných hodin    | Částka časového rozlišení        | Data odpracovaných hodin   | Skutečné hodnoty odpracovaných hodin| Odměna               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 31. 8. 2018             | 80                   | 6                     | 16. 8. 2018 - 31. 8. 2018  | 81                  | 6                  |        
| 31. 8. 2018             | 80                   | 6                     | 16. 8. 2018 - 31. 8. 2018  | 75                  | 0                   |

## <a name="weekly-accrual-frequency"></a>Týdenní frekvence časového rozlišení

| Datum udělení časového rozlišení    | Úroveň odpracovaných hodin    | Částka časového rozlišení        | Data odpracovaných hodin   | Skutečné hodnoty odpracovaných hodin| Odměna               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 31. 8. 2018             | 40                   | 3                     | 27. 8. 2018 - 31. 8. 2018  | 42                  | 3                  |        
| 31. 8. 2018             | 40                   | 3                     | 27. 8. 2018 - 31. 8. 2018  | 35                  | 0                   |

## <a name="employee-assigned-leave-plans"></a>Plány pracovního volna přiřazené zaměstnanci

U přiřazených plánů pracovního volna zaměstnance je základ úrovně a typ hodin zobrazený pro plány, kde jsou odpracované hodiny definované jako typ časového rozlišení. U aktivních plánů se pro informaci zobrazí rovněž skutečné odpracované hodiny pro období časového rozlišení od aktuálního data. 

## <a name="loading-data"></a>Načítání dat

Skutečné hodiny lze importovat pomocí entity odpracovaných hodin pracovního volna a absence ve správě dat. Pokud používáte kalendáře pracovní doby, import ověří, že pravidelné odpracované hodiny nepřekročí naplánované hodiny v den definovaný kalendářem. Import také ověří, že odpracované hodiny pro daný den nepřekročí 24 hodin. 

Pro import skutečných hodin, které mají být použity v procesu časového rozlišení pracovního volna, jsou třeba následující informace:

+ Číslo pracovníka 
+ Datum pracovního dne
+ Typ
+ Pracovní doba

Jedno datum může mít přidružený pouze jeden z každého typu.

| PERSONNELNUMBER       | DATEWORKED           | TYP                  | HOURS                |
| --------------------- | -------------------- | --------------------- | -------------------- |
| 000337                | 6. 8. 2018             | Řádné               | 8                    |       
| 000337                | 7. 8. 2018             | Řádné               | 8                    |
| 000337                | 7. 8. 2018             | Přesčas              | 3                    |
| 000337                | 8. 8. 2018             | Řádné               | 8                    |
| 000337                | 7. 8. 2018             | Řádné               | 8                    |
| 000337                | 9. 8. 2018             | Řádné               | 8                    |
