---
title: Funkce INT64VALUE ER
description: Toto téma obsahuje obecné informace o použití funkce INT64VALUE elektronického výkaznictví.
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
ms.openlocfilehash: 75df802b75454baeea75a8ceb32d5d045a77a3a0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916538"
---
# <a name="INT64VALUE">Funkce INT64VALUE ER</a>

[!include [banner](../includes/banner.md)]

Funkce `INT64VALUE` vrátí hodnotu *Int64*, která představuje zadaný řetězec.

## <a name="syntax-1"></a>Syntaxe 1

```
INT64VALUE (text)
```

## <a name="syntax-2"></a>Syntaxe 2

```
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
