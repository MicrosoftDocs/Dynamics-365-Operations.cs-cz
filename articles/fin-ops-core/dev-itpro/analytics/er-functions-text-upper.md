---
title: Funkce elektronického výkaznictví UPPER
description: Tento článek obsahuje obecné informace o použití funkce UPPER elektronického výkaznictví.
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
ms.openlocfilehash: bdea427dda5f09a3903378012679e9dd3fa86be9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275334"
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
