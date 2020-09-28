---
title: Funkce el. výkaznictví NUMBERFORMAT
description: Toto téma obsahuje obecné informace o použití funkce NUMBERFORMAT elektronického výkaznictví.
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
ms.openlocfilehash: 8a431414044846bf4e79e6b9f0e5b27281ea8f46
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744400"
---
# <a name="numberformat-er-function"></a>Funkce el. výkaznictví NUMBERFORMAT

[!include [banner](../includes/banner.md)]

Funkce `NUMBERFORMAT` vrátí hodnotu typu *řetězec*, která představuje zadané číslo jako text v určeném formátu a ve volitelně zadané [jazykové verzi](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes). Informace o podporovaných formátech: [standardní](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) a [vlastní](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).

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
