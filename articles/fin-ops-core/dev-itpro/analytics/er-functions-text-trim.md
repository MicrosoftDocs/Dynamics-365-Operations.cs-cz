---
title: Funkce el. výkaznictví TRIM
description: Tento článek obsahuje obecné informace o použití funkce TRIM elektronického výkaznictví.
author: NickSelin
ms.date: 02/28/2022
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
ms.openlocfilehash: deadf89641771efa864e701af9dad57c5e62ea37
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864635"
---
# <a name="trim-er-function"></a>Funkce el. výkaznictví TRIM

[!include [banner](../includes/banner.md)]

Funkce `TRIM` vrátí zadaný textový řetězec jako hodnotu *Řetězec* poté, co tabulátor, návrat vozíku, posun řádku a posun formuláře byly nahrazeny jednou mezerou, po zkrácení úvodní a koncové mezery a po odstranění více mezer mezi slovy.

## <a name="syntax"></a>Syntaxe

```vb
TRIM (text)
```

## <a name="arguments"></a>Argumenty

`text`: *řetězec*

Platná cesta ke zdroji dat typu *řetězec*.

## <a name="return-values"></a>Vrácené hodnoty

*Řetězec*

Výsledná textová hodnota.

## <a name="usage-notes"></a>Poznámky k použití

V některých případech možná budete chtít zkrátit úvodní a koncové mezery, ale raději zachovat formátování určeného textu. Pokud například tento text představuje adresu, kterou lze zadat do víceřádkového textového pole a může obsahovat odřádkování a formátování konce řádku. V tomto případě použijte následující výraz: `REPLACE(text,"^[ \t]+|[ \t]+$","", true)`, kde `text` je argument, který odkazuje na zadaný textový řetězec.

## <a name="example-1"></a>Příklad 1

`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` vrátí **"Sample text"**.

## <a name="example-2"></a>Příklad 2

`TRIM (CONCATENATE (CHAR(10), "`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`", CHAR(9),"`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`", CHAR(13)))` vrátí **"Sample text"**.

## <a name="additional-resources"></a>Další prostředky

[Textové funkce](er-functions-category-text.md)

[Funkce elektronického výkaznictví REPLACE](er-functions-text-replace.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
