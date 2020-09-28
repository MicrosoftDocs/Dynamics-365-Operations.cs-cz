---
title: Funkce elektronického výkaznictví SPLIT
description: Toto téma obsahuje obecné informace o použití funkce SPLIT elektronického výkaznictví.
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
ms.openlocfilehash: c171509353fed92b14ca0d7473742e4a9a54bad1
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745266"
---
# <a name="split-er-function"></a>Funkce elektronického výkaznictví SPLIT

[!include [banner](../includes/banner.md)]

Funkce `SPLIT` rozdělí zadaný vstupní řetězec do podřetězců a vrátí výsledek jako novou hodnotu typu *seznam záznamů*.

## <a name="syntax-1"></a>Syntaxe 1

```vb
SPLIT (input, length)
```

Tato syntaxe rozdělí zadaný vstupní řetězec na podřetězce, přičemž každý má zadanou délku.

## <a name="syntax-2"></a>Syntaxe 2

```vb
SPLIT (input, delimiter)
```

Tato syntaxe rozdělí zadaný vstupní řetězec na podřetězce na základě určeného oddělovače.

## <a name="arguments"></a>Argumenty

`input`: *řetězec*

Text, který má být rozdělen.

`length`: *celé číslo*

Maximální délka jednoho podřetězce.

`delimiter`: *řetězec*

Oddělovač k oddělení dílčích řetězců.

## <a name="return-values"></a>Vrácené hodnoty

*Seznam záznamů*

Výsledný seznam záznamů.

## <a name="usage-notes"></a>Poznámky k použití

Struktura záznamů ve vráceném seznamu se skládá z pole **Value** typu *řetězec*. Každý záznam ve vráceném seznamu obsahuje vygenerované podřetězce v tomto poli.

Je-li argument `delimiter` prázdný, vrátí se nový seznam, který se skládá z jednoho záznamu obsahujícího pole **Value** typu *řetězec*. Toto pole obsahuje vstupní text.

Pokud je argument `input` prázdný, vrátí se nový prázdný seznam. Pokud není zadán argument `input` nebo argument `delimiter`, dojde k výjimce aplikace.

## <a name="example-1"></a>Příklad 1

`SPLIT ("abcd", 3)` vrátí nový seznam obsahující dva záznamy s polem **Value** typu *řetězec*. Pole **Value** v prvním záznamu obsahuje text **"abc"** a pole **Value** v druhém záznamu obsahuje text **"d"**.

## <a name="example-2"></a>Příklad 2

`SPLIT ("XAb aBy", "aB")` vrátí nový seznam obsahující tři záznamy s poleem **Value** typu *řetězec*. Pole **Value** v prvním záznamu obsahuje text **"X"**, pole **Value** v druhém záznamu obsahuje text **"&nbsp;"**, a pole **Value** v třetím záznamu obsahuje text **"y"**. 

## <a name="additional-resources"></a>Další zdroje

[Funkce seznamu](er-functions-category-list.md)
