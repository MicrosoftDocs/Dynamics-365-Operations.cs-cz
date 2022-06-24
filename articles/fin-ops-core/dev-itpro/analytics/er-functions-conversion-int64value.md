---
title: Funkce INT64VALUE ER
description: Tento článek obsahuje obecné informace o použití funkce INT64VALUE elektronického výkaznictví.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 37fae9cdc5a833009b0ca1cbeb851e5e6e1b6608
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892157"
---
# <a name="int64value-er-function"></a>Funkce INT64VALUE ER

[!include [banner](../includes/banner.md)]

Funkce `INT64VALUE` vrátí hodnotu *Int64*, která představuje zadaný řetězec.

## <a name="syntax-1"></a>Syntaxe 1

```vb
INT64VALUE (text)
```

## <a name="syntax-2"></a>Syntaxe 2

```vb
INT64VALUE (number)
```

## <a name="arguments"></a>Argumenty

`text`: *řetězec*

Textová hodnota, která musí být převedena na číslo *Int64*.

`number`: *reálné číslo* nebo *celé číslo*

Číselná hodnota *Reálné* nebo *Celé číslo*, která musí být převedena na číslo *Int64*.

## <a name="return-values"></a>Vrácené hodnoty

*Int64*

Výsledná číselná hodnota.

## <a name="usage-notes"></a>Poznámky k použití

Desetinná místa jsou oříznuta.

## <a name="example-1"></a>Příklad 1

`INT64VALUE ("22565422744")` vrátí hodnotu *Int64* **22565422744**.

## <a name="example-2"></a>Příklad 2

`INT64VALUE ( VALUE("22565422744.77"))` vrátí hodnotu *Int64* **22565422744**.

## <a name="additional-resources"></a>Další zdroje

[Funkce převodu typu](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]