---
title: Funkce elektronického výkaznictví STRINGJOIN
description: Toto téma obsahuje obecné informace o použití funkce STRINGJOIN elektronického výkaznictví.
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
ms.openlocfilehash: 99d50313f8097d43b820ffc1c36eef0097e7ec55
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917182"
---
# <a name="STRINGJOIN">Funkce elektronického výkaznictví STRINGJOIN</a>

[!include [banner](../includes/banner.md)]

Funkce `STRINGJOIN` vrátí hodnotu typu *řetězec*, která se skládá ze zřetězených hodnot zadaného pole ze zadaného seznamu. Hodnoty mohou být odděleny určeným oddělovačem.

## <a name="syntax"></a>Syntaxe

```
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
