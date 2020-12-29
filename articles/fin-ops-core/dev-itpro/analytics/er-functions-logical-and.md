---
title: Funkce el. výkaznictví AND
description: Toto téma obsahuje obecné informace o použití funkce AND elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 8ccb7feb1d0f6836e7e8001870034900f6a1f598
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687067"
---
# <a name="and-er-function"></a>Funkce el. výkaznictví AND

[!include [banner](../includes/banner.md)]

Funce `AND` vrátí *logickou hodnotu* **TRUE**, jsou-li splněny všechny zadané podmínky. V opačném případě výraz vrátí *logickou hodnotu* **FALSE**.

## <a name="syntax"></a>Syntaxe

```vb
AND (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a>Argumenty

`condition 1`: *logická hodnota*

Platný podmíněný výraz, který má být testován. Tento argument je povinný.

`condition N`: *logická hodnota*

Platný podmíněný výraz, který má být testován. Tyto další argumenty jsou nepovinné.

## <a name="return-values"></a>Vrácené hodnoty

*Logická hodnota*

Výsledná *logická hodnota*.

## <a name="usage-notes"></a>Poznámky k použití

V argumentech logických funkcí můžete použít odkazy na zdroje dat, číselné a textové hodnoty, logické hodnoty, relační operátory a jiné funkce elektronického výkaznictví (ER). Všechny argumenty je však nutné vyhodnotit na *logickou hodnotu* **TRUE** nebo **FALSE**.

## <a name="example"></a>Příklad

`AND (1=1, "a"="a")` vrátí **TRUE**.

`AND (1=2, "a"="a")` vrátí **FALSE**.

## <a name="additional-resources"></a>Další zdroje

[Logické funkce](er-functions-category-logical.md)
