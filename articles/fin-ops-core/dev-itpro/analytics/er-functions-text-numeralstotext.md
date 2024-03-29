---
title: Funkce el. výkaznictví NUMERALSTOTEXT
description: Tento článek obsahuje obecné informace o použití funkce NUMERALSTOTEXT elektronického výkaznictví.
author: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 172693583699edfad7deeb16f8fc081abb6119d5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287981"
---
# <a name="numeralstotext-er-function"></a>Funkce el. výkaznictví NUMERALSTOTEXT

[!include [banner](../includes/banner.md)]

Funkce `NUMERALSTOTEXT` vrací zadané číslo jako hodnotu typu *řetězec* poté, co bylo slovně vyjádřeno (tedy převedeno na textový řetězec) v zadaném jazyce.

## <a name="syntax"></a>Syntaxe

```vb
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
