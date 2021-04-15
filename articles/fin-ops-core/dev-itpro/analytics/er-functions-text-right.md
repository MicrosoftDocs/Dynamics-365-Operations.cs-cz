---
title: Funkce elektronického výkaznictví RIGHT
description: Toto téma obsahuje obecné informace o použití funkce RIGHT elektronického výkaznictví.
author: NickSelin
ms.date: 12/10/2019
ms.topic: article
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
ms.openlocfilehash: f59b12f0b3f7b100b953b2072677c83c836746ff
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746116"
---
# <a name="right-er-function"></a>Funkce elektronického výkaznictví RIGHT

[!include [banner](../includes/banner.md)]

Funkce `RIGHT` vrací hodnotu typu *řetězec*, která představuje zadaný počet znaků od konce zadaného řetězce.

## <a name="syntax"></a>Syntaxe

```vb
RIGHT (text, number)
```

## <a name="arguments"></a>Argumenty

`text`: *řetězec*

Hodnota typu *řetězec*, která představuje původní text.

`number`: *celé číslo*

Počet znaků, které mají být vráceny od konce původního textu.

## <a name="return-values"></a>Vrácené hodnoty

*Řetězec*

Výsledná textová hodnota.

## <a name="example"></a>Příklad

`RIGHT ("Sample", 3)` vrátí **"ple"**.

## <a name="additional-resources"></a>Další zdroje

[Textové funkce](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]