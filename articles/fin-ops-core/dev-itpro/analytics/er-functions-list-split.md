---
title: Funkce elektronického výkaznictví SPLIT
description: Tento článek obsahuje obecné informace o použití funkce SPLIT elektronického výkaznictví.
author: kfend
ms.date: 04/01/2021
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
ms.openlocfilehash: e95ecaae46ee73899736b1d5729d7f9639fc6803
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273991"
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

## <a name="example-3"></a>Příklad 3

Můžete použít funkci [INDEX](er-functions-list-index.md) pro přístup k jednotlivým prvkům zadaného vstupního řetězce. Pokud zadáte zdroj dat **MyList** typu **vypočítané pole** a nakonfigurujete pro něj výraz `SPLIT("abc", 1)`, výraz `INDEX(MyList,2).Value` vrátí textovou hodnotu **"b"**.

## <a name="example-4"></a>Příklad 4

Funkce [ENUMERATE](er-functions-list-enumerate.md) vám také může pomoci s přístupem k jednotlivým prvkům zadaného vstupního řetězce. Pokud nejprve zadáte zdroj dat **MyList** typu **Vypočítané pole** a nakonfigurujte pro něj výraz `SPLIT("abc", 1)` a poté zadáte zdroj dat **EnumeratedList** typu **Vypočítané pole** a nakonfigurujte pro něj výraz `ENUMERATE(MyList)`, výraz `FIRSTORNULL(WHERE(EnumeratedList, EnumeratedList.Number=2)).Value` vrátí textovou hodnotu **"b"**.

## <a name="additional-resources"></a>Další prostředky

[Funkce seznamu](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
