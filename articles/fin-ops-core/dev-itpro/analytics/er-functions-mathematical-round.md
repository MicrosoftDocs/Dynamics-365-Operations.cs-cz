---
title: Funkce elektronického výkaznictví ROUND
description: Toto téma obsahuje obecné informace o použití funkce ROUND elektronického výkaznictví.
author: NickSelin
ms.date: 10/21/2020
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
ms.openlocfilehash: b0c28ba2faebf117aa008106f8a77f79af8f4de3122df858825aa15a6dae3616
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6744403"
---
# <a name="round-er-function"></a>Funkce elektronického výkaznictví ROUND

[!include [banner](../includes/banner.md)]

Funkce `ROUND` vrátí zadané číslo, poté, co je zaokrouhleno na hodnotu typu *reálné číslo* po zaokrouhlení na zadaný počet desetinných míst.

## <a name="syntax"></a>Syntaxe

```vb
ROUND (number, decimals)
```

## <a name="arguments"></a>Argumenty

`number`: *reálné číslo*

Číselná hodnota, která má být zaokrouhlena.

`decimals`: *celé číslo*

Číselná hodnota, která představuje počet desetinných míst.

## <a name="return-values"></a>Vrácené hodnoty

*Reálný*

Výsledná číselná hodnota.

## <a name="usage-notes"></a>Poznámky k použití

Pokud je hodnota argumentu `decimals` vyšší než 0 (nula), zadané číslo je zaokrouhleno na tento počet desetinných míst.

Pokud má argument `decimals` hodnotu **0** (nula), zadané číslo je zaokrouhleno na nejbližší sudé celé číslo.

Pokud je hodnota argumentu `decimals` nižší než 0 (nula), zadané číslo je zaokrouhleno vlevo od oddělovače desetinných míst.

## <a name="example-1"></a>Příklad 1

`ROUND (1200.767, 2)` zaokrouhlí na dvě desetinná místa a vrátí hodnotu **1200.77**.

## <a name="example-2"></a>Příklad 2

`ROUND (1200.767, -3)` zaokrouhlí na nejbližší násobek 1 000 a vrátí hodnotu **1000**.

## <a name="example-3"></a>Příklad 3

`ROUND (1200.5, 0)` zaokrouhlí na nejbližší sudé celé číslo a vrátí **1200**, zatímco `ROUND (1201.5, 0)` udělá totéž a vrátí **1202**.

## <a name="additional-resources"></a>Další prostředky

[Matematické funkce](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]