---
title: Funkce elektronického výkaznictví ROUNDDOWN
description: Toto téma obsahuje obecné informace o použití funkce ROUNDDOWN elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 9221476c1c12a7cc3fe2367cdee3ad44e5cbe381
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686875"
---
# <a name="rounddown-er-function"></a>Funkce elektronického výkaznictví ROUNDDOWN

[!include [banner](../includes/banner.md)]

Funkce `ROUNDDOWN` vrátí zadané číslo poté, co je zaokrouhleno dolů na hodnotu typu *reálné číslo* na zadaný počet desetinných míst.

## <a name="syntax"></a>Syntaxe

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a>Argumenty

`number`: *reálné číslo*

Číselná hodnota, která má být zaokrouhlena dolů.

`decimals`: *celé číslo*

Číselná hodnota, která představuje počet desetinných míst.

## <a name="return-values"></a>Vrácené hodnoty

*Reálný*

Výsledná číselná hodnota.

## <a name="usage-notes"></a>Poznámky k použití

Tato funkce se chová jako [ROUND](er-functions-mathematical-round.md), ale vždy zaokrouhluje zadané číslo směrem dolů (směrem k nule).

## <a name="example-1"></a>Příklad 1

`ROUNDDOWN (1200.767, 2)` zaokrouhlí směrem dolů na dvě desetinná místa a vrátí hodnotu **1200.76**. 

## <a name="example-2"></a>Příklad 2

`ROUNDDOWN (1700.767, -3)` zaokrouhlí směrem dolů na nejbližší násobek 1 000 a vrátí hodnotu **1000**.

## <a name="additional-resources"></a>Další zdroje

[Matematické funkce](er-functions-category-mathematical.md)
