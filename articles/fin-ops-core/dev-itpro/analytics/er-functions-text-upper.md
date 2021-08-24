---
title: Funkce elektronického výkaznictví UPPER
description: Toto téma obsahuje obecné informace o použití funkce UPPER elektronického výkaznictví.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 3742f490fb87d156e3b3dcebabdcebb85ab76f5d0afd9a60806497d32e5746e6
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6729799"
---
# <a name="upper-er-function"></a>Funkce elektronického výkaznictví UPPER

[!include [banner](../includes/banner.md)]

Funkce `UPPER` vrátí zadaný textový řetězec jako *řetězcovou* hodnotu poté, co byl převeden na velká písmena.

## <a name="syntax"></a>Syntaxe

```vb
UPPER (text )
```

## <a name="arguments"></a>Argumenty

`text`: *řetězec*

Platná cesta ke zdroji dat typu *řetězec*.

## <a name="return-values"></a>Vrácené hodnoty

*Řetězec*

Výsledná textová hodnota.

## <a name="example"></a>Příklad

`UPPER ("Sample")` vrátí **"SAMPLE"**.

## <a name="additional-resources"></a>Další zdroje

[Textové funkce](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]