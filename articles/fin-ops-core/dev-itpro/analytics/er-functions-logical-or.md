---
title: Funkce el. výkaznictví OR
description: Toto téma obsahuje obecné informace o použití funkce OR elektronického výkaznictví.
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: faf07c5d8b30cd3babe8a6a55ae7effe5ce457a0
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744616"
---
# <a name="or-er-function"></a>Funkce el. výkaznictví OR

[!include [banner](../includes/banner.md)]

Funkce `OR` vrátí *logickou hodnotu* **FALSE**, pokud nejsou splněny všechny zadané podmínky. Tato funkce vrátí *logickou* hodnotu **PRAVDA**, pokud je splněna libovolná uvedená podmínka.

## <a name="syntax"></a>Syntaxe

```vb
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a>Argumenty

`condition 1`: *logická hodnota*

Platný podmíněný výraz, který má být testován. Tento argument je povinný.

`condition N`: *logická hodnota*

Platný podmíněný výraz, který má být testován. Tyto další argumenty jsou nepovinné.

## <a name="return-values"></a>Vrácené hodnoty

*Logická hodnota*

Výsledná *logická hodnota*.

## <a name="example"></a>Příklad

`OR (1=2, "a"="a")` vrátí **TRUE**.

## <a name="additional-resources"></a>Další zdroje

[Logické funkce](er-functions-category-logical.md)
