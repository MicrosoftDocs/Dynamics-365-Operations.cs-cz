---
title: Funkce elektronického výkaznictví ROUNDUP
description: Toto téma obsahuje obecné informace o použití funkce ROUNDUP elektronického výkaznictví.
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
ms.openlocfilehash: 84a62639b49db17fef1abcda75bc5ad7f08d1005
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917044"
---
# <a name="ROUNDUP">Funkce elektronického výkaznictví ROUNDUP</a>

[!include [banner](../includes/banner.md)]

Funkce `ROUNDUP` vrátí zadané číslo, poté, co je zaokrouhleno na hodnotu typu *reálné číslo* po zaokrouhlení nahoru na zadaný počet desetinných míst.

## <a name="syntax"></a>Syntaxe

```
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
