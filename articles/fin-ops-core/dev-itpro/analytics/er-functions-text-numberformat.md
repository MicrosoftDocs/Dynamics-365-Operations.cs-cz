---
title: Funkce el. výkaznictví NUMBERFORMAT
description: Toto téma obsahuje obecné informace o použití funkce NUMBERFORMAT elektronického výkaznictví.
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
ms.openlocfilehash: 4a383b3f7c0ca7c4e5afc609cc8a7b1b07021b02
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890376"
---
# <a name="numberformat-er-function"></a>Funkce el. výkaznictví NUMBERFORMAT

[!include [banner](../includes/banner.md)]

Funkce `NUMBERFORMAT` vrátí hodnotu typu *řetězec*, která představuje zadané číslo jako text v určeném formátu a ve volitelně zadané [jazykové verzi](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes). Informace o podporovaných formátech: [standardní](/dotnet/standard/base-types/standard-numeric-format-strings) a [vlastní](/dotnet/standard/base-types/custom-numeric-format-strings).

## <a name="syntax-1"></a>Syntaxe 1

```vb
NUMBERFORMAT (number, format)
```

## <a name="syntax-2"></a>Syntaxe 2

```vb
NUMBERFORMAT (number, format, culture)
```

## <a name="arguments"></a>Argumenty

`number`: *celé číslo* nebo *reálné číslo*

Číselná hodnota, která představuje číslo, které má být formátováno.

`format`: *řetězec*

Hodnota typu *řetězec*, která představuje formát.

`culture`: *řetězec*

Hodnota typu *řetězec* představující jazykovou verzi, která má být použita pro formátování.

## <a name="return-values"></a>Vrácené hodnoty

*Řetězec*

Výsledná textová hodnota.

## <a name="usage-notes"></a>Poznámky k použití

Pokud jazyková verze není definována jako argument volané funkce, kontext, ve kterém je tato funkce spuštěna, určuje jazykovou verzi, která se používá k formátování čísel.

## <a name="example-1"></a>Příklad 1

Pro jazykovou verzi **EN-US** vrátí `NUMBERFORMAT (0.45, "p")` hodnotu **"45.00 %"** a `NUMBERFORMAT (10.45, "#")` vrátí hodnotu **"10"**.

## <a name="example-2"></a>Příklad 2

`NUMBERFORMAT (10/3, "F2", "de")` vrátí hodnotu **3,33**, zatímco `NUMBERFORMAT (10/3, "F2", "en-us")` vrátí **3.33**.

## <a name="additional-resources"></a>Další zdroje

[Textové funkce](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]