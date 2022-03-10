---
title: Funkce elektronického výkaznictví REPLACE
description: Toto téma obsahuje obecné informace o použití funkce REPLACE elektronického výkaznictví.
author: NickSelin
ms.date: 04/02/2020
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e7bee3ed0531df64e813423f7280a62fd2afe77432ae05c1fb21264578c9e4ca
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719362"
---
# <a name="replace-er-function"></a>Funkce elektronického výkaznictví REPLACE

[!include [banner](../includes/banner.md)]

Funkce `REPLACE` vrátí zadaný textový řetězec jako hodnotu typu *řetězec* po nahrazení celého řetězce nebo jeho části jiným řetězcem.

## <a name="syntax"></a>Syntaxe

```vb
REPLACE (text, pattern, replacement, regular expression flag)
```

## <a name="arguments"></a>Argumenty

`text`: *řetězec*

Platná cesta ke zdroji dat typu *řetězec*.

`pattern`: *řetězec*

Pokud je argument `regular expression flag` **FALSE**, obsahuje tento argument text, který je třeba nahradit.

Je-li argument `regular expression flag` **TRUE**, obsahuje tento argument regulární výraz, který definuje jak vyhledávací vzor, tak i nahrazující text.

`replacement`: *řetězec*

Pokud je argument `regular expression flag` **FALSE**, obsahuje tento argument text, který se použije jako náhradní.

Je-li argument `regular expression flag` **TRUE**, tento argument se nepoužije.

`regular expression flag`: *logická hodnota*

*Logická hodnota* udává, zda se k nahrazení použje regulární výraz.

## <a name="return-values"></a>Vrácené hodnoty

*Řetězec*

Výsledná textová hodnota.

## <a name="usage-notes"></a>Poznámky k použití

Pokud má argument `regular expression flag` hodnotu **TRUE**, vrátí tato funkce zadaný řetězec poté, co byl změněn aplikováním regulárního výrazu, který je určen argumentem `pattern`. Regulární výraz slouží k vyhledání znaků, které je třeba nahradit.

Pokud má `regular expression flag` argument hodnotu **NEPRAVDA**, vrátí tato funkce zadaný řetězec po provedení sady znaků definovaných v argumentu `pattern`, které byly nahrazeny znaky argumentu `replacement`. 

## <a name="example-1"></a>Příklad 1

`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` použije regulární výraz, který odebere všechny nenumerické symboly a vrátí **"19234564971"**. 

## <a name="example-2"></a>Příklad 2

`REPLACE ("abcdef", "cd", "GH", false)` nahradí vzor **"cd"** řetězcem **"GH"** a vrátí **"abGHef"**.

## <a name="additional-resources"></a>Další zdroje

[Textové funkce](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]