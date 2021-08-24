---
title: Funkce el. výkaznictví CHAR
description: Toto téma obsahuje obecné informace o použití funkce CHAR elektronického výkaznictví.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: e422ccc406e919b2191f4bccb1ac8198bba84b09e9f01f6971876e2c6507d6d3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6754359"
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

Řetězec, který vrací tato funkce, závisí na kódování, které je vybráno v nadřazeném prvku formátu **FILE**. Seznam podporovaných kódování naleznete v části [Třída kódování](/dotnet/api/system.text.encoding).

## <a name="example"></a>Příklad

`CHAR (255)` vrátí **"ÿ"**.

## <a name="additional-resources"></a>Další zdroje

[Textové funkce](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]