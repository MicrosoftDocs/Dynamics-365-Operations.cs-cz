---
title: Funkce elektronického výkaznictví ROUND
description: Toto téma obsahuje obecné informace o použití funkce ROUND elektronického výkaznictví.
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
ms.openlocfilehash: 6751c1321fc71419fa8b153145a057371e0f7af5
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041600"
---
# <a name="ROUND">Funkce elektronického výkaznictví ROUND</a>

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

Pokud je hodnota argumentu `decimals` **0** (nula), zadané číslo je zaokrouhleno na nejbližší celé číslo.

Pokud je hodnota argumentu `decimals` nižší než 0 (nula), zadané číslo je zaokrouhleno vlevo od oddělovače desetinných míst.

## <a name="example-1"></a>Příklad 1

`ROUND (1200.767, 2)` zaokrouhlí na dvě desetinná místa a vrátí hodnotu **1200.77**.

## <a name="example-2"></a>Příklad 2

`ROUND (1200.767, -3)` zaokrouhlí na nejbližší násobek 1 000 a vrátí hodnotu **1000**.

## <a name="additional-resources"></a>Další zdroje

[Matematické funkce](er-functions-category-mathematical.md)
