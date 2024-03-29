---
title: Funkce el. výkaznictví TRANSLATE
description: Tento článek obsahuje obecné informace o použití funkce TRANSLATE elektronického výkaznictví.
author: kfend
ms.date: 04/02/2020
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
ms.openlocfilehash: 7a15a28f6efa5333b54aa34938d22a9d6e404cec
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278434"
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
