---
title: Funkce INTVALUE ER
description: Tento článek obsahuje obecné informace o použití funkce INTVALUE elektronického výkaznictví.
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
ms.openlocfilehash: eccee60c40bfc96f1fd93e7177207a1dd1888dc6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282614"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
