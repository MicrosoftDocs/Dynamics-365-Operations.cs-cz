---
title: Funkce elektronického výkaznictví ROUNDUP
description: Toto téma obsahuje obecné informace o použití funkce ROUNDUP elektronického výkaznictví.
author: NickSelin
ms.date: 12/17/2019
ms.topic: article
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
ms.openlocfilehash: 4898f596108ff3c563da55a567a10da987d62d33
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744432"
---
# <a name="roundup-er-function"></a>Funkce elektronického výkaznictví ROUNDUP

[!include [banner](../includes/banner.md)]

Funkce `ROUNDUP` vrátí zadané číslo, poté, co je zaokrouhleno na hodnotu typu *reálné číslo* po zaokrouhlení nahoru na zadaný počet desetinných míst.

## <a name="syntax"></a>Syntaxe

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a>Argumenty

`number`: *reálné číslo*

Číselná hodnota, která má být zaokrouhlena nahoru.

`decimals`: *celé číslo*

Číselná hodnota, která představuje počet desetinných míst.

## <a name="return-values"></a>Vrácené hodnoty

*Reálný*

Výsledná číselná hodnota.

## <a name="usage-notes"></a>Poznámky k použití

Tato funkce se chová jako [ROUND](er-functions-mathematical-round.md), ale vždy zaokrouhluje zadané číslo směrem nahoru (směrem od nuly).

## <a name="example-1"></a>Příklad 1

`ROUNDUP (1200.763, 2)` zaokrouhlí směrem nahoru na dvě desetinná místa a vrátí hodnotu **1200.77**.

## <a name="example-2"></a>Příklad 2

`ROUNDUP (1200.767, -3)` zaokrouhlí směrem nahoru na nejbližší násobek 1 000 a vrátí hodnotu **2000**.

## <a name="additional-resources"></a>Další zdroje

[Matematické funkce](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]