---
title: Funkce el. výkaznictví DAYOFYEAR
description: Toto téma obsahuje obecné informace o použití funkce DAYOFYEAR elektronického výkaznictví.
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
ms.openlocfilehash: ab252b6194267836ba9e1d85f3b96fb100c9f598c783bd9c849c6490c2e54e21
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6712302"
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