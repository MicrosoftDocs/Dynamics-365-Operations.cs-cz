---
title: Funkce elektronického výkaznictví COUNT
description: Toto téma obsahuje obecné informace o použití funkce COUNT elektronického výkaznictví.
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
ms.openlocfilehash: 0fc122dafd6be90d090ba3b79a8c2eccab74d77441f82db71cb5e08d13d13518
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6753639"
---
# <a name="count-er-function"></a>Funkce elektronického výkaznictví COUNT

[!include [banner](../includes/banner.md)]

Funkce `COUNT` vrátí hodnotu typu *celé číslo*, která představuje počet záznamů v zadaném seznamu, pokud seznam není prázdný. Pokud je seznam prázdný, tato funkce vrátí hodnotu **0** (nula).

## <a name="syntax"></a>Syntaxe

```vb
COUNT (list)
```

## <a name="arguments"></a>Argumenty

`list`: *seznam záznamů*

Platná cesta ke zdroji dat typu *seznam záznamů*.

## <a name="return-values"></a>Vrácené hodnoty

*Celé číslo*

Výsledná číselná hodnota.

## <a name="example"></a>Příklad

`COUNT (SPLIT("abcd" , 3))` vrátí hodnotu **2**, protože funkce `SPLIT` použitá v tomto příkladu vytvoří seznam obsahující dva záznamy.

## <a name="additional-resources"></a>Další zdroje

[Funkce seznamu](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]