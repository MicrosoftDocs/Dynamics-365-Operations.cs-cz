---
title: Funkce el. výkaznictví CASE
description: Toto téma obsahuje obecné informace o použití funkce CASE elektronického výkaznictví.
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
ms.openlocfilehash: 3bba9cd190db61fda3636cc3c8093030f886b9bd
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041761"
---
# <a name="CASE">Funkce el. výkaznictví CASE</a>

[!include [banner](../includes/banner.md)]

Funkce `CASE` vyhodnotí hodnotu zadaného výrazu podle zadaných alternativních možností a vrátí výsledek první možnosti, která se rovná hodnotě zadaného výrazu. V opačném případě vrátí volitelný výchozí výsledek, pokud je výchozí výsledek zadán jako poslední argument volané funkce, jemuž nepředchází nějaká možnost. Vrácená hodnota může být libovolného podporovaného datového typu.

## <a name="syntax"></a>Syntaxe

```vb
CASE (expression, option 1, result 1[, option 2, result 2, …, option N, result N, default result])
```

## <a name="arguments"></a>Argumenty

`expression`: *primitivní datový typ* (logická, číselná nebo textová hodnota)

Platný výraz, který vrací hodnotu primitivního datového typu.

`option 1`: *primitivní datový typ* (logická, číselná nebo textová hodnota)

Platný výraz, který vrací hodnotu stejného primitivního datového typu jako argument `expression` volané funkce. Tento argument je povinný.

`result 1`: *kterýkoli z podporovaných datových typů*

Vrácený výsledek, který odpovídá předcházející možnosti. Tento argument je povinný.

`option N`: *primitivní datový typ* (logická, číselná nebo textová hodnota)

Platný výraz, který vrací hodnotu stejného primitivního datového typu jako argument `expression` volané funkce. Tento argument je volitelný.

`result N`: *kterýkoli z podporovaných datových typů*

Vrácený výsledek, který odpovídá předcházející možnosti. Tento argument je volitelný.

`default result`: *kterýkoli z podporovaných datových typů*

Výsledek, který by měl být vrácen, pokud neexistuje shoda. Tento argument je volitelný.

## <a name="return-values"></a>Vrácené hodnoty

*kterýkoli z podporovaných datových typů*

Výsledná hodnota některého z podporovaných datových typů.

## <a name="usage-notes"></a>Poznámky k použití

Výjimka je vyvolána za běhu, pokud neexistuje shoda a volitelný výchozí výsledek není definován.

Všechny výsledky musí být zadány pomocí stejného datového typu. Výjimka je vyvolána v době návrhu, pokud se datové typy konfigurovaných výsledků neshodují.

Jsou-li první výsledná hodnota a *n*-tá hodnota výsledku hodnoty datového typu *kontejner (záznam)* nebo *seznam záznamů*, výsledek obsahuje pouze pole, která existují v obou hodnotách.

## <a name="example"></a>Příklad

`CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")` vrátí řetězec **"WINTER"** (zima), pokud je aktuální datum relace aplikace mezi říjnem a prosincem. Jinak bude vrácen prázdný řetězec.

## <a name="additional-resources"></a>Další zdroje

[Logické funkce](er-functions-category-logical.md)
