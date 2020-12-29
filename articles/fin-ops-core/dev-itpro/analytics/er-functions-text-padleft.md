---
title: Funkce el. výkaznictví PADLEFT
description: Toto téma obsahuje obecné informace o použití funkce PADLEFT elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 268941d8bc0bd4dc6de6d2597c05a11c1f530f15
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680139"
---
# <a name="padleft-er-function"></a>Funkce el. výkaznictví PADLEFT

[!include [banner](../includes/banner.md)]

Funkce `PADLEFT` vrátí hodnotu typu *řetězec* zadané délky, kde je začátek zadaného řetězce odsazen určenými znaky.

## <a name="syntax"></a>Syntaxe

```vb
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a>Argumenty

`text`: *řetězec*

Hodnota typu *řetězec*, která představuje původní text.

`length`: *celé číslo*

*Celočíselná* hodnota, která představuje konečný počet znaků odsazeného řetězce.

`padding chars`: *řetězec*

Znaky, které mají být použity pro odsazení.

## <a name="return-values"></a>Vrácené hodnoty

*Řetězec*

Výsledná textová hodnota.

## <a name="example"></a>Příklad

`PADLEFT ("1234", 10, "`&nbsp;`")` vrátí textový řetězec **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**.

## <a name="additional-resources"></a>Další zdroje

[Textové funkce](er-functions-category-text.md)
