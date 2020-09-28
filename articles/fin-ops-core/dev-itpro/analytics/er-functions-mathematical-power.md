---
title: Funkce elektronického výkaznictví POWER
description: Toto téma obsahuje obecné informace o použití funkce POWER elektronického výkaznictví.
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
ms.openlocfilehash: 080b2f9b1ada55209c9470386aceab2d3ef456af
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744568"
---
# <a name="power-er-function"></a>Funkce elektronického výkaznictví POWER

[!include [banner](../includes/banner.md)]

Funkce `POWER` vrací hodnotu typu *reálné číslo*, která představuje výsledek umocnění zadaného kladného čísla dle zadané mocniny.

## <a name="syntax"></a>Syntaxe

```vb
POWER (number, power)
```

## <a name="arguments"></a>Argumenty

`number`: *reálné číslo* nebo *celé číslo*

Číselná hodnota, která musí být umoceněna dle zadané mocniny.

`power`: *reálné číslo* nebo *celé číslo*

Číselná hodnota, která představuje zadanou mocninu.

## <a name="return-values"></a>Vrácené hodnoty

*Reálný*

Výsledná číselná hodnota.

## <a name="example-1"></a>Příklad 1

`POWER (10, 2)` vrátí **100**.

## <a name="example-2"></a>Příklad 2

`POWER (4, 0.5)` vrátí **2**.

## <a name="additional-resources"></a>Další zdroje

[Matematické funkce](er-functions-category-mathematical.md)
