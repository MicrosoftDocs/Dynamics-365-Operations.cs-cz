---
title: Funkce elektronického výkaznictví FIRSTORNULL
description: Toto téma popisuje použití funkce FIRSTORNULL elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 11/29/2019
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
ms.openlocfilehash: e360812c5b0dbfb8df4ab279bf3e0050acebbb25
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745189"
---
# <a name="firstornull-er-function"></a>Funkce elektronického výkaznictví FIRSTORNULL

[!include [banner](../includes/banner.md)]

Funkce `FIRSTORNULL` vrátí první záznam zadaného seznamu jako hodnotu typu *kontejner (záznam)*, pokud tento záznam není prázdný. Je-li záznam prázdný, vrátí tato funkce hodnotu typu *kontejner (záznam)* s hodnotou null.

## <a name="syntax"></a>Syntaxe

```vb
FIRSTORNULL (list)
```

## <a name="arguments"></a>Argumenty

`list`: *seznam záznamů*

Platná cesta ke zdroji dat typu *seznam záznamů*.

## <a name="return-values"></a>Vrácené hodnoty

*Kontejner (záznam)*

Výsledná hodnota atributu.

## <a name="example"></a>Příklad

Výraz `FIRSTORNULL(SPLIT("",1)).Value` vrátí prázdný řetězec (**""**).

## <a name="additional-resources"></a>Další zdroje

[Funkce seznamu](er-functions-category-list.md)
