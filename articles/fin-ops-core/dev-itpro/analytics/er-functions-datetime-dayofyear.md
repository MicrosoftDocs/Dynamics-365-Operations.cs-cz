---
title: Funkce el. výkaznictví DAYOFYEAR
description: Toto téma obsahuje obecné informace o použití funkce DAYOFYEAR elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 755f5f1de28f95ed682648caf47155ad71c8f4b0
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745482"
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
