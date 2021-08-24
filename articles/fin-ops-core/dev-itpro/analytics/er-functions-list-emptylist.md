---
title: Funkce elektronického výkaznictví EMPTYLIST
description: Toto téma obsahuje obecné informace o použití funkce EMPTYLIST elektronického výkaznictví.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: fe2c72eddbb7f9227691ba29b19743c03aedfeb0d841e1a2466a159fa3afdf56
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6734785"
---
# <a name="emptylist-er-function"></a>Funkce elektronického výkaznictví EMPTYLIST

[!include [banner](../includes/banner.md)]

Funkce `EMPTYLIST` vrátí prázdnou hodnotu typu *seznam záznamů* s použitím zadaného seznamu jako zdroje pro strukturu seznamu.

## <a name="syntax"></a>Syntaxe

```vb
EMPTYLIST (list)
```

## <a name="arguments"></a>Argumenty

`list`: *seznam záznamů*

Platná cesta ke zdroji dat typu *seznam záznamů*.

## <a name="return-values"></a>Vrácené hodnoty

*Seznam záznamů*

Výsledný seznam záznamů.

## <a name="example"></a>Příklad

`EMPTYLIST (SPLIT ("abc", 1))` vrátí nový prázdný seznam, který má stejnou strukturu jako seznam vrácený funkcí `SPLIT`, který je používán.

## <a name="additional-resources"></a>Další zdroje

[Funkce seznamu](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]