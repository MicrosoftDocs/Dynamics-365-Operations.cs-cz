---
title: Funkce elektronického výkaznictví STRINGJOIN
description: Toto téma obsahuje obecné informace o použití funkce STRINGJOIN elektronického výkaznictví.
author: NickSelin
ms.date: 12/12/2019
ms.topic: article
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
ms.openlocfilehash: ac21651e0f5b5a1579b9335bb7f3217370c4d5a1
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745514"
---
# <a name="stringjoin-er-function"></a>Funkce elektronického výkaznictví STRINGJOIN

[!include [banner](../includes/banner.md)]

Funkce `STRINGJOIN` vrátí hodnotu typu *řetězec*, která se skládá ze zřetězených hodnot zadaného pole ze zadaného seznamu. Hodnoty mohou být odděleny určeným oddělovačem.

## <a name="syntax"></a>Syntaxe

```vb
STRINGJOIN (list, field, delimiter)
```

## <a name="arguments"></a>Argumenty

`list`: *seznam záznamů*

Platná cesta ke zdroji dat typu *seznam záznamů*.

`field`: *pole*

Platná cesta k poli datového typu *řetězec* v zadaném seznamu.

`delimiter`: *řetězec*

Oddělovač k oddělení dílčích řetězců.

## <a name="return-values"></a>Vrácené hodnoty

*Řetězec*

Výsledná textová hodnota.

## <a name="example"></a>Příklad

Když zadáte `SPLIT("abc" , 1)` jako zdroj dat **DS**, výraz `STRINGJOIN (DS, DS.Value, "-")` vrátí **"a-b-c"**.

## <a name="additional-resources"></a>Další zdroje

[Funkce seznamu](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]