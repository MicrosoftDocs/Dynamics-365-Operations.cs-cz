---
title: Funkce el. výkaznictví TRIM
description: Tento článek obsahuje obecné informace o použití funkce TRIM elektronického výkaznictví.
author: kfend
ms.date: 02/28/2022
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
ms.openlocfilehash: 95b8d2989d705c4998da0af8e683adf567edfe92
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273091"
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
