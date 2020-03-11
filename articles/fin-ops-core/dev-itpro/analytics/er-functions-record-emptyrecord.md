---
title: Funkce elektronického výkaznictví EMPTYRECORD
description: Toto téma obsahuje obecné informace o použití funkce EMPTYRECORD elektronického výkaznictví.
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
ms.openlocfilehash: a02cdd085a236065bb3622b36f7d3284144d96e5
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041267"
---
# <a name="EMPTYRECORD">Funkce elektronického výkaznictví EMPTYRECORD</a>

[!include [banner](../includes/banner.md)]

Funkce `EMPTYRECORD` vrací prázdnou hodnotu typu *kontejner (záznam)*, která má stejnou strukturu jako zadaný seznam záznamů nebo záznam.

## <a name="syntax"></a>Syntaxe

```vb
EMPTYRECORD (list)
```

## <a name="arguments"></a>Argumenty

`list`: *seznam záznamů* nebo *kontejner (záznam)*

Platná cesta ke zdroji dat buď typu *seznam záznamů* nebo *kontejner (záznam)*.

## <a name="return-values"></a>Vrácené hodnoty

*Kontejner (záznam)*

Výsledná hodnota atributu.

## <a name="usage-notes"></a>Poznámky k použití

> [!NOTE] 
> Záznam null je záznam, kde všechna pole mají prázdnou hodnotu. Prázdná hodnota je **0** (nula) pro čísla, prázdný řetězec pro řetězce atd.

## <a name="example"></a>Příklad

`EMPTYRECORD (SPLIT ("abc", 1))` vrátí nový prázdný záznam, který má stejnou strukturu jako seznam vrácený funkcí `SPLIT`. Další informace naleznete v tématu [SPLIT](er-functions-list-split.md)

## <a name="additional-resources"></a>Další zdroje

[Funkce záznamu](er-functions-category-record.md)
