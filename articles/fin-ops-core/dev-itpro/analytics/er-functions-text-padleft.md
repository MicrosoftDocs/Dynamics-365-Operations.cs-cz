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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d11e2d8b46614085156228ab1001d1f9340a05b0
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040956"
---
# <a name="PADLEFT">Funkce el. výkaznictví PADLEFT</a>

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
