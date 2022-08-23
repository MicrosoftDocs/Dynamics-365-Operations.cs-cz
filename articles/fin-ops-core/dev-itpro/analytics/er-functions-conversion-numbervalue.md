---
title: Funkce NUMBERVALUE ER
description: Tento článek obsahuje obecné informace o použití funkce NUMBERVALUE elektronického výkaznictví.
author: kfend
ms.date: 12/05/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 2e39cf59cabd44583e78ff2c35a7ae4d6edbd7ee
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282584"
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
