---
title: Metody odpisu dlouhodobého majetku pro Českou republiku
description: Toto téma obsahuje informace o odpisech dlouhodobého majetku pro právnické osoby v České republice.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationGroup_W
audience: Application User
ms.reviewer: kfend
ms.custom: 264314
ms.search.region: Czech Republic
ms.author: kfend
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 2bd539834288b22c36342d80d106c98267e54ebd3444415a607368a74786e46c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6771594"
---
# <a name="fixed-assets-depreciation-methods-for-the-czech-republic"></a>Metody odpisu dlouhodobého majetku pro Českou republiku

[!include [banner](../includes/banner.md)]

Toto téma obsahuje informace o odpisech dlouhodobého majetku pro právnické osoby v České republice. 

Odpis dlouhodobého majetku pro požadavky právních předpisů v České republice zahrnuje:

-   Procentuální hodnota odpisu
-   Metody odpisu, které jsou specifické pro Českou republiku

## <a name="depreciation-percentages-and-coefficients"></a>Procenta odpisu a koeficienty
Podle právních předpisů České republiky je dlouhodobý majetek seskupen do odpisových skupin. Pro každou odpisovou skupinu definují právní předpisy specifické hodnoty pro odpisovou sazbu za první rok, odpisovou sazbu za další roky a upravenou pořizovací cenu. Pro splnění právních požadavků v České republice je třeba nastavit různé hodnoty odpisové sazby za první rok, za další roky a za upravenou pořizovací cenu v různých odpisových skupinách. Stránka **Odpisové skupiny** obsahuje následující volby.

| Pole                                | popis |
|-----|------|
| **Počáteční datum**                           | Zadejte datum, kdy začne odpisová skupina|
| **Míra odpisu za první rok** | Zadejte procento odpisu pro běžnou českou odpisovou metodu nebo koeficient odpisu pro zrychlenou českou odpisovou metodu používané v prvním roce odpisování této skupiny. |
| **Odpisová sazba pro další roky**     | Zadejte procento odpisu pro běžnou českou odpisovou metodu nebo koeficient odpisu pro zrychlenou českou odpisovou metodu používané v dalších letech po roce pořízení.|
| **Upravená pořizovací cena**           | Zadejte procento odpisu pro běžnou českou odpisovou metodu nebo koeficient odpisu pro zrychlenou českou odpisovou metodu, rozšířené o úpravu pořizovací ceny. Toto procento nebo koeficient platí od roku úpravy pořizovací ceny. Všechny kladné a záporné úpravy jsou součástí upravené pořizovací ceny. |

## <a name="czech-republicspecific-depreciation-methods"></a>Odpisové metody specifické pro Českou republiku
Pro uživatele v právnických osobách v České republice existují další odpisové metody. Další pravidla a nastavení se používají ke splnění specifických požadavků účtování dlouhodobého majetku. Podle předpisů České republiky se v České republice používají následující odpisové metody:

-   Rovnoměrně CZ
-   Zrychleně CZ

Další informace o metodách odpisu naleznete v tématu [Odpisy dlouhodobého majetku](../fixed-assets/fixed-asset-depreciation.md).

### <a name="regular-cz-depreciation-method"></a>Běžná česká metoda odpisování

Běžná česká metoda odpisování vypočítá odpisy s použitím následujícího vzorce:

-   Částka odpisu v prvním roce = Pořizovací hodnota \* procento odpisu za první rok
-   Částka odpisu v dalších letech = Pořizovací hodnota \* procento odpisu za další roky
-   Částka odpisu po úpravě pořizovací ceny = (Pořizovací hodnota + Úprava pořizovací ceny) \* procento odpisu po úpravě pořizovací ceny

Následující příklad ukazuje výpočet běžné české metody odpisu.

| Pole                                                | Hodnota           |
|------------------------------------------------------|---------------------|
| Pořizovací hodnota                                    | 100 000             |
| Oprava pořizovací ceny                               | 50 000 (ve třetím roce) |
| Procento odpisu za první rok           | 14,2 %               |
| Procento odpisu za další roky           | 28,6 %               |
| Procento odpisu po úpravě pořizovací ceny | 25,0 %               |

Tento příklad ukazuje odpis vypočítaný pomocí běžné české metody odpisu.

| Počet roků     | Výpočet               |
|---------------------|---------------------------|
| 1                   | 100 000 \* 14 2 % = 14 200 |
| 2                   | 100 000 \* 28,6 % = 28 600 |
| 3                   | 150 000 \* 25 % = 37 500   |
| 4                   | 150 000 \* 25 % = 37 500   |

### <a name="accelerated-cz-depreciation-method"></a>Zrychlená česká metoda odpisování

Zrychlená česká metoda odpisu používá koeficienty pro výpočet odpisů pomocí následujících vzorců:

-   Částka odpisu v prvním roce = Pořizovací hodnota / koeficient odpisu za první rok
-   Částka odpisu v dalších letech = (2 \* Zůstatková účetní hodnota) / (koeficient odpisu za další roky - již odepsaná období)
-   Částka odpisu po úpravě pořizovací ceny = (2 \* Zůstatková účetní hodnota) / (koeficient odpisu po úpravě pořizovací ceny – již odepsaná období po určité úpravě pořizovací ceny)

Následující příklad ukazuje výpočet zrychlené české metody odpisu.

| Pole                                                 | Hodnota     |
|-------------------------------------------------------|-----------|
| Pořizovací hodnota                                     | 100 000   |
| Úpravy pořizovací ceny (ve třetím roce)                    | 50 000    |
| Úpravy pořizovací ceny (ve pátém roce)                    | 60 000    |
| Koeficient odpisu za první rok           | 4         |
| Koeficient odpisu za další roky           | 5         |
| Koeficient odpisu po úpravě pořizovací ceny | 4         |

Tento příklad ukazuje odpis vypočítaný pomocí zrychlené české metody odpisu.

| Počet roků     | Výpočet                      |
|---------------------|----------------------------------|
| 1                   | 100 000 /4 = 25 000              |
| 2                   | (2 \* 75 000) / (5 - 1) = 37 500 |
| 3                   | (2 \* 87 500) / (4 - 0) = 43 750 |
| 4                   | (2\* 43750) / (4 - 1) = 29 167   |
| 5                   | (2\* 74583) / (4 - 0) = 37 292   |
| 6                   | (2\* 37292) / (4 - 1) = 24 861   |
| 7                   | (2\* 12431) / (4 - 2) = 12 430   |




[!INCLUDE[footer-include](../../includes/footer-banner.md)]