---
title: Funkce el. výkaznictví TRANSLATE
description: Toto téma obsahuje obecné informace o použití funkce TRANSLATE elektronického výkaznictví.
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
ms.openlocfilehash: 07fe19c5f66c33e336f76f3a72d3bbda0c7e8d86
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040909"
---
# <a name="TRANSLATE">Funkce el. výkaznictví TRANSLATE</a>

[!include [banner](../includes/banner.md)]

Funkce `TRANSLATE` vrátí zadaný textový řetězec jako hodnotu typu *řetězec* po nahrazení celého řetězce nebo jeho části jiným řetězcem.

## <a name="syntax"></a>Syntaxe

```vb
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a>Argumenty

`text`: *řetězec*

Platná cesta ke zdroji dat typu *řetězec*.

`pattern`: *řetězec*

Text, který má být nahrazen.

`replacement`: *řetězec*

Text, který má být použit jako náhrada.

## <a name="return-values"></a>Vrácené hodnoty

*Řetězec*

Výsledná textová hodnota.

## <a name="example"></a>Příklad

`TRANSLATE ("abcdef", "cd", "GH")` nahradí vzor **"cd"** řetězcem **"GH"** a vrátí **"abGHef"**.

## <a name="additional-resources"></a>Další zdroje

[Textové funkce](er-functions-category-text.md)
