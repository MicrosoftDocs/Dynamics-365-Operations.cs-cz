---
title: Funkce el. výkaznictví MID
description: Tento článek obsahuje obecné informace o použití funkce MID elektronického výkaznictví.
author: NickSelin
ms.date: 12/10/2019
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ca5dbfb6de3057ad2c4a6dcc7ecce3d0ddc69595
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867633"
---
# <a name="mid-er-function"></a>Funkce el. výkaznictví MID

[!include [banner](../includes/banner.md)]

Funkce `MID` vrátí hodnotu typu *řetězec*, která představuje zadaný počet znaků ze zadaného řetězce počínaje zadanou pozicí.

## <a name="syntax"></a>Syntaxe

```vb
MID (text, starting position, number of characters)
```

## <a name="arguments"></a>Argumenty

`text`: *řetězec*

Hodnota typu *řetězec* určující text, ze kterého se budou vracet znaky.

`starting position`: *celé číslo*

Hodnota typu *celé číslo*, která určuje pozici prvního znaku, který má být vrácen ze zadaného textu.

`number of characters`: *celé číslo*

Hodnota typu *celé číslo*, která určuje počet znaků, které mají být vráceny počínaje zadanou počáteční pozicí.

## <a name="return-values"></a>Vrácené hodnoty

*Řetězec*

Výsledná textová hodnota.

## <a name="usage-notes"></a>Poznámky k použití

Pokud je hodnota argumentu `starting position` menší než 0 (nula), jsou vracené znaky počítány od první pozice v zadaném řetězci.

Pokud hodnota argumentu `starting position` přesahuje délku zadaného řetězce, je vrácen prázdný řetězec.

## <a name="example"></a>Příklad

`MID ("Sample", 2, 3)` vrátí hodnotu **"amp"**.

## <a name="additional-resources"></a>Další zdroje

[Textové funkce](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]