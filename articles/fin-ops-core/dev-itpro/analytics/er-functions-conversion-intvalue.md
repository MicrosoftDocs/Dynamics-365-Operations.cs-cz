---
title: Funkce INTVALUE ER
description: Toto téma obsahuje obecné informace o použití funkce INTVALUE elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: c5c3e4c8bd918fa1154d2c111970d2f6d0e90e08
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743632"
---
# <a name="intvalue-er-function"></a>Funkce INTVALUE ER

[!include [banner](../includes/banner.md)]

Funkce `INTVALUE` vrátí hodnotu *Int*, která představuje zadaný řetězec.

## <a name="syntax-1"></a>Syntaxe 1

```vb
INTVALUE (text)
```

## <a name="syntax-2"></a>Syntaxe 2

```vb
INTVALUE (number)
```

## <a name="arguments"></a>Argumenty

`text`: *řetězec*

Textová hodnota, která musí být převedena na číslo *Int*.

`number`: *reálné číslo* nebo *celé číslo*

Číselná hodnota *Reálné* nebo *Celé číslo*, která musí být převedena na číslo *Int*.

## <a name="return-values"></a>Vrácené hodnoty

*Int*

Výsledná číselná hodnota.

## <a name="usage-notes"></a>Poznámky k použití

Desetinná místa jsou oříznuta.

## <a name="example-1"></a>Příklad 1

`INTVALUE ("100.77")` vrátí hodnotu *Int* **100**.

## <a name="example-2"></a>Příklad 2

`INTVALUE (-100.77)` vrátí hodnotu *Int* **-100**.

## <a name="additional-resources"></a>Další zdroje

[Funkce převodu typu](er-functions-category-type-conversion.md)
