---
title: Funkce elektronického výkaznictví SESSIONTODAY
description: Tento článek obsahuje obecné informace o použití funkce SESSIONTODAY elektronického výkaznictví.
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
ms.openlocfilehash: 0eeb4fcc449b565774cc79b767a2d157557d5b98
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274882"
---
# <a name="sessiontoday-er-function"></a>Funkce elektronického výkaznictví SESSIONTODAY

[!include [banner](../includes/banner.md)]

Funkce `SESSIONTODAY` vrátí hodnotu typu *datum*, která představuje aktuální datum relace aplikace.

## <a name="syntax"></a>Syntaxe

```vb
SESSIONTODAY ()
```

## <a name="return-values"></a>Vrácené hodnoty

*Datum*

Výsledná hodnota data.

## <a name="example"></a>Příklad

`DATEFORMAT (SESSIONTODAY (), "d", "DE")` vrátí aktuální datum relace aplikace, 24. prosince 2015, jako řetězec **"24-12-2015"** na základě vybrané německé jazykové verze a zadaného formátu.

## <a name="additional-resources"></a>Další zdroje

[Funkce data a času](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
