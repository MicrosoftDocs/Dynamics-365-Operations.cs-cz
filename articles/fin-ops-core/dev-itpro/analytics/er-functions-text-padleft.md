---
title: Funkce el. výkaznictví PADLEFT
description: Tento článek obsahuje obecné informace o použití funkce PADLEFT elektronického výkaznictví.
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
ms.openlocfilehash: 551b508bc6a17b1c6a08e25d5db0094713d9634f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892559"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]