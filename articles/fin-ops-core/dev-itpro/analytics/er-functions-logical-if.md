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
ms.openlocfilehash: 87e252a2751beeecb51e512cae38b271c1456fae
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744688"
---
# <a name="if-er-function"></a>Funkce el. výkaznictví IF

[!include [banner](../includes/banner.md)]

Při splnění dané podmínky vrátí funkce `IF` první zadanou hodnotu. V opačném případě vrátí druhou zadanou hodnotu. Vrácená hodnota může být libovolného podporovaného datového typu.

## <a name="syntax"></a>Syntaxe

```vb
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
