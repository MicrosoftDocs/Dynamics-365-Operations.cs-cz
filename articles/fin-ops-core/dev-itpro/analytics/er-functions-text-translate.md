---
title: Funkce el. výkaznictví TRANSLATE
description: Toto téma obsahuje obecné informace o použití funkce TRANSLATE elektronického výkaznictví.
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
ms.openlocfilehash: 0b43c1edb2a26ebe01e8d5cf69e1ff377c6c8bf84e889b6bb3d1828d3dc84b53
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6721921"
---
# <a name="translate-er-function"></a>Funkce el. výkaznictví TRANSLATE

[!include [banner](../includes/banner.md)]

Funkce `TRANSLATE` vrací *řetězcovou* hodnotu, která obsahuje výsledek nahrazení znaku zadaného textu znaky jiné zadané sady.

## <a name="syntax"></a>Syntaxe

```vb
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a>Argumenty

`text`: *řetězec*

Platná cesta ke zdroji dat typu *řetězec*.

`pattern`: *řetězec*

Text, který má být nahrazen.

`replacement`: *řetězec*

Text, který má být použit jako náhrada.

## <a name="return-values"></a>Vrácené hodnoty

*Řetězec*

Výsledná textová hodnota.

## <a name="usage-notes"></a>Poznámky k použití

Funkce `TRANSLATE` nahradí vždy jeden znak. Funkce nahradí první znak argumentu `text` prvním znakem argumentu `pattern` a poté druhým znakem a následuje stejný tok až do dokončení. Pokud se znak z argumentů `text` a `pattern` shoduje, je nahrazen znakem z argumentu `replacement`, který se nachází ve stejné pozici jako znak z argumentu `pattern`. Pokud se v argumentu `pattern` několikrát objevuje znak, použije se mapování argumentů `replacement`, které odpovídá prvnímu výskytu tohoto znaku.

## <a name="example-1"></a>Příklad 1

`TRANSLATE ("abcdef", "cd", "GH")` nahradí znak **"c"** zadaného textu **“abcdef”** znakem **"G"** textu `replacement` z následujích důvodů:
-   Znak **"c"** je uveden v textu `pattern` v první pozici.
-   První pozice textu `replacement` obsahuje znak **"G"**.

## <a name="example-2"></a>Příklad 2

`TRANSLATE ("abcdef", "ccd", "GH")` vrátí **"abGdef"**.

## <a name="example-3"></a>Příklad 3

`TRANSLATE ("abccba", "abc", "123")` vrátí **"123321"**.

## <a name="additional-resources"></a>Další prostředky

[Textové funkce](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]