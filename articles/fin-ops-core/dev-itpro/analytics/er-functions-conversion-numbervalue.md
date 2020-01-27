---
title: Funkce NUMBERVALUE ER
description: Toto téma obsahuje obecné informace o použití funkce NUMBERVALUE elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 80f0606dc3842cdfa56d41e2815eccd7518218b8
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916515"
---
# <a name="NUMBERVALUE">Funkce NUMBERVALUE ER</a>

[!include [banner](../includes/banner.md)]

Funkce `NUMBERVALUE` vrací hodnotu *reálné číslo*, která je převedena ze zadané hodnoty *Řetězec*. Během převodu se uvažují určené oddělovače skupin desetinných míst a číslic.

## <a name="syntax"></a>Syntaxe

```
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a>Argumenty

`text`: *řetězec*

Textová hodnota, která musí být převedena na *reálné* číslo.

`decimal separator`: řetězec

Desetinný oddělovač. Používá se k oddělení celého čísla a zlomkových částí desetinného čísla.

`digit grouping separator`: *řetězec*

Oddělovač skupin číslic. Používá se jako oddělovač tisíců.

## <a name="return-values"></a>Vrácené hodnoty

*Reálný*

Výsledná číselná hodnota.

## <a name="example"></a>Příklad

`NUMBERVALUE( "1 234,56", ",", " ")` vrací **1234.56**.

## <a name="additional-resources"></a>Další zdroje

[Funkce převodu typu](er-functions-category-type-conversion.md)
