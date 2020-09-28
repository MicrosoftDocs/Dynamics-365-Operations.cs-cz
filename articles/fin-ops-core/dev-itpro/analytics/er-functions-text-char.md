---
title: Funkce el. výkaznictví CHAR
description: Toto téma obsahuje obecné informace o použití funkce CHAR elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 63df7b1ac847e12cf429467dd444450552a59162
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744954"
---
# <a name="char-er-function"></a>Funkce el. výkaznictví CHAR

[!include [banner](../includes/banner.md)]

Funkce `CHAR` vrací hodnotu typu *řetězec*, která představuje jeden znak odkazovaný zadaným číslem Unicode.

## <a name="syntax"></a>Syntaxe

```vb
CHAR (number)
```

## <a name="arguments"></a>Argumenty

`number`: *celé číslo*

Číslo, které odpovídá požadovanému znaku.

## <a name="return-values"></a>Vrácené hodnoty

*Řetězec*

Výsledná textová hodnota.

## <a name="usage-notes"></a>Poznámky k použití

Řetězec, který vrací tato funkce, závisí na kódování, které je vybráno v nadřazeném prvku formátu **FILE**. Seznam podporovaných kódování naleznete v části [Třída kódování](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).

## <a name="example"></a>Příklad

`CHAR (255)` vrátí **"ÿ"**.

## <a name="additional-resources"></a>Další zdroje

[Textové funkce](er-functions-category-text.md)
