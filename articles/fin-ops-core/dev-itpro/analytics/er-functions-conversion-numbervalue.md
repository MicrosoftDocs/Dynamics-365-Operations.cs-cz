---
title: Funkce NUMBERVALUE ER
description: Toto téma obsahuje obecné informace o použití funkce NUMBERVALUE elektronického výkaznictví.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 84d7f17f37a83547522cf09047b72100f6f5b859
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755341"
---
# <a name="numbervalue-er-function"></a>Funkce NUMBERVALUE ER

[!include [banner](../includes/banner.md)]

Funkce `NUMBERVALUE` vrací hodnotu *reálné číslo*, která je převedena ze zadané hodnoty *Řetězec*. Během převodu se uvažují určené oddělovače skupin desetinných míst a číslic.

## <a name="syntax"></a>Syntaxe

```vb
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]