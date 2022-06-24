---
title: Funkce el. výkaznictví DAYOFYEAR
description: Tento článek obsahuje obecné informace o použití funkce DAYOFYEAR elektronického výkaznictví.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: fc4d1d3293c31b1b89a7390c8ac313e1407d433e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848773"
---
# <a name="dayofyear-er-function"></a>Funkce el. výkaznictví DAYOFYEAR

[!include [banner](../includes/banner.md)]

Funkce `DAYOFYEAR` vrátí hodnotu typu *celé číslo*, které představuje počet dní mezi 1. lednem a zadaným datem.

## <a name="syntax"></a>Syntaxe

```vb
DAYOFYEAR (date) as Integer
```

## <a name="arguments"></a>Argumenty

`date`: *datum*

Hodnota kalendářního data, která představuje datum, které má být použito pro výpočet počtu dní.

## <a name="return-values"></a>Vrácené hodnoty

*Celé číslo*

Výsledná číselná hodnota.

## <a name="example-1"></a>Příklad 1

`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` vrací **61**.

## <a name="example-2"></a>Příklad 2

`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` vrací **1**.

## <a name="additional-resources"></a>Další zdroje

[Funkce data a času](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]