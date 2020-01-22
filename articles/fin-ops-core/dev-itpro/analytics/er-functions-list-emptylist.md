---
title: Funkce elektronického výkaznictví EMPTYLIST
description: Toto téma obsahuje obecné informace o použití funkce EMPTYLIST elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: a60bc948ff6223b6e3acccd0ba40bf64f238aac2
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917389"
---
# <a name="EMPTYLIST">Funkce elektronického výkaznictví EMPTYLIST</a>

[!include [banner](../includes/banner.md)]

Funkce `EMPTYLIST` vrátí prázdnou hodnotu typu *seznam záznamů* s použitím zadaného seznamu jako zdroje pro strukturu seznamu.

## <a name="syntax"></a>Syntaxe

```
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
