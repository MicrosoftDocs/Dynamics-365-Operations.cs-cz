---
title: Funkce el. výkaznictví IF
description: Toto téma obsahuje obecné informace o použití funkce IF elektronického výkaznictví.
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
ms.openlocfilehash: b29302ffe534f2439519e57c6a6b8c94c1df8d62
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917136"
---
# <a name="IF">Funkce el. výkaznictví IF</a>

[!include [banner](../includes/banner.md)]

Při splnění dané podmínky vrátí funkce `IF` první zadanou hodnotu. V opačném případě vrátí druhou zadanou hodnotu. Vrácená hodnota může být libovolného podporovaného datového typu.

## <a name="syntax"></a>Syntaxe

```
IF (condition, first value, second value) as any of the supported data types
```

## <a name="arguments"></a>Argumenty

`condition`: *logická hodnota*

Platný podmíněný výraz, který má být testován.

`first value`: *kterýkoli z podporovaných datových typů*

Výsledek, který je vrácen, pokud je podmínka splněna.

`second value`: *kterýkoli z podporovaných datových typů*

Výsledek, který je vrácen, pokud podmínka není splněna.

## <a name="return-values"></a>Vrácené hodnoty

*kterýkoli z podporovaných datových typů*

Výsledná hodnota některého z podporovaných datových typů.

## <a name="usage-notes"></a>Poznámky k použití

Zadané argumenty `first value` a `second value` musejí mít stejný datový typ. Výjimka je vyvolána v době návrhu, pokud se datové typy konfigurovaných hodnot neshodují.

Jsou-li první a druhá hodnota datového typu *kontejner (záznam)* nebo *seznam záznamů*, výsledek obsahuje pouze pole, která existují v obou hodnotách.

## <a name="example"></a>Příklad

`IF (1=2, "condition is met", "condition is not met")` vrátí řetězec **"podmínka není splněna"**.

## <a name="additional-resources"></a>Další zdroje

[Logické funkce](er-functions-category-logical.md)
