---
title: Funkce el. výkaznictví LEFT
description: Toto téma obsahuje obecné informace o použití funkce LEFT elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 9e9cdff9bb5c22c74803cf17c056c0ff1af5ef43
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685876"
---
# <a name="left-er-function"></a>Funkce el. výkaznictví LEFT

[!include [banner](../includes/banner.md)]

Funkce `LEFT` vrátí hodnotu typu *řetězec*, která představuje zadaný počet znaků od počátku zadaného řetězce.

## <a name="syntax"></a>Syntaxe

```vb
LEFT (text, number)
```

## <a name="arguments"></a>Argumenty

`text`: *řetězec*

Hodnota typu *řetězec*, která představuje původní text.

`number`: *celé číslo*

Počet znaků, které mají být vráceny od začátku původního textu.

## <a name="return-values"></a>Vrácené hodnoty

*Řetězec*

Výsledná textová hodnota.

## <a name="example"></a>Příklad

`LEFT ("Sample", 3)` vrátí **"Sam"**.

## <a name="additional-resources"></a>Další zdroje

[Textové funkce](er-functions-category-text.md)
