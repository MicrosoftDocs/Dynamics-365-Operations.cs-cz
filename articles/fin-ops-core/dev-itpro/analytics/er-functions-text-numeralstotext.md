---
title: Funkce el. výkaznictví NUMERALSTOTEXT
description: Toto téma obsahuje obecné informace o použití funkce NUMERALSTOTEXT elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 459123a66dae7a3d87a22b042e1be6585959ac15
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915618"
---
# <a name="NUMERALSTOTEXT">Funkce el. výkaznictví NUMERALSTOTEXT</a>

[!include [banner](../includes/banner.md)]

Funkce `NUMERALSTOTEXT` vrací zadané číslo jako hodnotu typu *řetězec* poté, co bylo slovně vyjádřeno (tedy převedeno na textový řetězec) v zadaném jazyce.

## <a name="syntax"></a>Syntaxe

```
NUMERALSTOTEXT (number, language, currency, print currency name flag, decimal points)
```

## <a name="arguments"></a>Argumenty

`number`: *celé číslo* nebo *reálné číslo*

Číselná hodnota, která představuje číslo, které má být převedeno na text.

`language`: *řetězec*

Hodnota typu *řetězec*, která představuje kód jazyka.

`currency`: *řetězec*

Hodnota typu *řetězec*, která představuje kód měny.

`print currency name flag`: *logická hodnota*

*Logická hodnota*, která označuje, zda má být k číslu převedenému na text přidán název měny.

`decimal points`: *celé číslo*

*Celočíselná* hodnota označující počet desetinných míst, které má obsahovat číslo převedené na text.

## <a name="return-values"></a>Vrácené hodnoty

*Řetězec*

Výsledná textová hodnota.

## <a name="usage-notes"></a>Poznámky k použití

Kód jazyka je volitelný. Pokud je definován jako prázdný řetězec, použije se kód jazyka pro aktuální kontext. Výchozí kód jazyka je **EN-US**. Kód jazyka pro spuštěný kontext je definován v prvku **Folder** nebo **File** spuštěného formátu elektronického výkaznictví (ER).

Zadaný kód měny je volitelný. Pokud je definován jako prázdný řetězec, použije se měna společnosti pro aktuální kontext.

> [!NOTE] 
> Argumenty `print currency name flag` a `decimal points` jsou analyzovány pouze pro následující kódy jazyka: **CS**, **ET**, **HU**, **LT**, **LV**, **PL** a **RU**. Dále je argument `print currency name flag` analyzován pouze pro společnosti s kontextem země nebo oblasti, který podporuje skloňování názvů měn.

## <a name="example-1"></a>Příklad 1

`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` vrátí **"One Thousand Two Hundred Thirty Four and 56"**.

## <a name="example-2"></a>Příklad 2

`NUMERALSTOTEXT (120, "PL", "", false, 0)` vrátí **"sto dwadzieścia"**. 

## <a name="example-3"></a>Příklad 3

`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` vrátí **"Сто двадцать евро 21 евроцент"**.

## <a name="additional-resources"></a>Další zdroje

[Textové funkce](er-functions-category-text.md)
