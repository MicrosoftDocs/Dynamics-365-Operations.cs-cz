---
title: Funkce elektronického výkaznictví REPLACE
description: Toto téma obsahuje obecné informace o použití funkce REPLACE elektronického výkaznictví.
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
ms.openlocfilehash: ba2590635ba465dae9ea50d3e4da989365548f3b
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040979"
---
# <a name="REPLACE">Funkce elektronického výkaznictví REPLACE</a>

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

Pokud má argument `regular expression flag` hodnotu **NEPRAVDA**, chová se tato funkce stejně jako funkce [TRANSLATE](er-functions-text-translate.md). Znaky zadané argumentem `replacement` se použijí k nahrazení nalezených znaků. 

## <a name="example-1"></a>Příklad 1

`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` použije regulární výraz, který odebere všechny nenumerické symboly a vrátí **"19234564971"**. 

## <a name="example-2"></a>Příklad 2

`REPLACE ("abcdef", "cd", "GH", false)` nahradí vzor **"cd"** řetězcem **"GH"** a vrátí **"abGHef"**.

## <a name="additional-resources"></a>Další zdroje

[Textové funkce](er-functions-category-text.md)
