---
title: Funkce el. výkaznictví CASE
description: Tento článek obsahuje obecné informace o použití funkce CASE elektronického výkaznictví.
author: kfend
ms.date: 12/17/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 702648e14abe980d246b92b0fe512bba07717e45
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274852"
---
# <a name="case-er-function"></a>Funkce el. výkaznictví CASE

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
