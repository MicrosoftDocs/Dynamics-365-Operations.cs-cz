---
title: "Metody odpisů dlouhodobého majetku pro Českou republiku"
description: "Toto téma obsahuje informace o odpisech dlouhodobého majetku pro právnické osoby v České republice."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetDepreciationGroup_W
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 264314
ms.assetid: 185cc4ce-d1b2-429a-9b1b-6b9c4b865da0
ms.search.region: Czech Republic
ms.author: v-elgolu
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 2ffe6e8209048d3e72a3c958021cb9daf1e7acc0
ms.lasthandoff: 03/31/2017


---

# <a name="fixed-assets-depreciation-methods-for-the-czech-republic"></a>Metody odpisů dlouhodobého majetku pro Českou republiku

[!include[banner](../includes/banner.md)]


Toto téma obsahuje informace o odpisech dlouhodobého majetku pro právnické osoby v České republice. 

Odpisy dlouhodobého majetku pro požadavky právních předpisů v České republice patří:

-   Procenta odpisu
-   Odpisové metody, které jsou specifické pro Českou republiku

## <a name="depreciation-percentages-and-coefficients"></a>Procenta odpisu a koeficienty
Podle právních předpisů České republiky jsou seskupeny dlouhodobý majetek do odpisové skupiny. Pro každou odpisovou skupinu definoval právní předpisy specifické hodnoty pro Odpisová sazba pro první rok, Odpisová sazba pro další roky a upravená pořizovací cena. Sazba pro první rok, pro další roky a upravená pořizovací cena musí splňovat požadavky právních předpisů v České republice, různé hodnoty odpisu nastavit v různých odpisových skupin. **Odpisové skupiny** stránku obsahuje následující volby.

| |  |
|-----|------|
| **Field**                                | **Description**|
| **Start date**                           | Zadejte datum zahájení depreciate skupiny.|
| **Depreciation rate for the first year** | Zadejte procento odpisu pro odpisovou metodu pravidelné CZ nebo odpisu koeficient pro zrychlené odpisování CZ používá v prvním roce odpisování této skupiny. |
| **Depreciation rate for next years**     | Zadejte procento odpisu pro pravidelné CZ metoda odpisu a odpisu koeficient pro zrychlené odpisování CZ pro odpis v letech následujících po roce pořízení.|
| **Adjusted acquisition price**           | Zadejte procento odpisu pro odpisovou metodu pravidelné CZ nebo koeficient amortizace pro zrychlenou metodu odpisu CZ rozšířený o opravu pořizovací ceny. Toto procento nebo koeficient platí rok opravy pořizovací ceny. Všechny kladné a záporné úpravy jsou součástí upravená pořizovací cena. |

## <a name="czech-republicspecific-depreciation-methods"></a>České Republicspecific metod odpisů
Pro uživatele v právnických osob v České republice existují další odpisové metody k dispozici. Další pravidla a nastavení se používá ke splnění požadavků účtování konkrétní dlouhodobý majetek. Podle předpisů České republiky jsou v České republice použita následující odpisové metody:

-   Rovnoměrně CZ
-   Zrychleně CZ

Další informace o metody odpisu, viz [odpisy dlouhodobého majetku](../fixed-assets/fixed-asset-depreciation.md).

### <a name="regular-cz-depreciation-method"></a>Běžné metody odpisu CZ

Pravidelné CZ metoda odpisu vypočítá odpisy s použitím následujícího vzorce:

-   Částka odpisu v prvním roce = Pořizovací hodnota \*procento odpisu pro první rok
-   Částka odpisu v příštích let = Pořizovací hodnota \*procento odpisu pro další roky
-   Částka odpisu po úpravě pořízení = (Pořizovací hodnota + úprava pořízení) \*procento odpisu po opravy pořizovací ceny

Následující příklad ukazuje regulární CZ způsob výpočtu odpisů.

|                                                      |                     |
|------------------------------------------------------|---------------------|
| **Field**                                            | **Value**           |
| Pořizovací hodnota                                    | 100 000             |
| Oprava pořizovací ceny                               | 50 000 (v roce 3d) |
| Procento odpisu pro první rok           | 14.2%               |
| Procento odpisu pro další roky           | 28.6%               |
| Procento odpisu po opravy pořizovací ceny | 25.0%               |

Tento příklad ukazuje odpisu vypočteného pomocí pravidelných CZ metoda odpisu.

|                     |                           |
|---------------------|---------------------------|
| **Počet let** | **Calculation**           |
| 1                   | 100 000 \* 14.2% = 14 200 |
| 2                   | 100 000 \* 28.6% = 28 600 |
| 3                   | 150 000 \* 25% = 37 500   |
| 4                   | 150 000 \* 25% = 37 500   |

### <a name="accelerated-cz-depreciation-method"></a>Metoda odpisu Zrychlený CZ

Zrychlenou metodu CZ odmítání příznaku používá koeficienty pro výpočet odpisů pomocí následujících vzorců:

-   Částka odpisu v prvním roce = Pořizovací hodnota / koeficient odpisování v prvním roce
-   Částka odpisu v příštích let = (2 \*zůstatková účetní hodnota) / (odpisu koeficient pro další roky - již odepsán období)
-   Částka odpisu po úpravě pořízení = (2 \*zůstatková účetní hodnota) / (koeficient amortizace po pořízení úpravy – období po určité opravy pořizovací ceny již odepsán)

Následující příklad ukazuje zrychlené CZ způsob výpočtu odpisů.

|                                                       |           |
|-------------------------------------------------------|-----------|
| **Field**                                             | **Value** |
| Pořizovací hodnota                                     | 100 000   |
| Opravy pořizovací ceny (v 3roky $2)                    | 50 000    |
| Opravy pořizovací ceny (do 5let $2)                    | 60 000    |
| Odpis koeficientem pro první rok           | 4         |
| Odpisu koeficient pro další roky           | 5         |
| Koeficient amortizace po opravy pořizovací ceny | 4         |

Tento příklad ukazuje odpisu vypočteného pomocí zrychlené CZ metoda odpisu.

|                     |                                  |
|---------------------|----------------------------------|
| **Počet let** | **Calculation**                  |
| 1                   | 100 000 /4 = 25 000              |
| 2                   | (2 \* 75 000) / (5 - 1) = 37 500 |
| 3                   | (2 \* 87 500) / (4 - 0) = 43 750 |
| 4                   | (2\* 43750) / (4 - 1) = 29 167   |
| 5                   | (2\* 74583) / (4 - 0) = 37 292   |
| 6                   | (2\* 37292) / (4 - 1) = 24 861   |
| 7                   | (2\* 12431) / (4 - 2) = 12 430   |



