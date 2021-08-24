---
title: Funkce elektronického výkaznictví LISTOFFIRSTITEM
description: Toto téma obsahuje obecné informace o použití funkce LISTOFFIRSTITEM elektronického výkaznictví.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: e0497a4ee2c44efd4ee8d1551440bd2984ebb0cff9980206b058670a16928986
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6761457"
---
# <a name="listoffirstitem-er-function"></a>Funkce elektronického výkaznictví LISTOFFIRSTITEM

[!include [banner](../includes/banner.md)]

Funkce `LISTOFFIRSTITEM` vrátí hodnotu typu *seznam záznamů*, která obsahuje pouze první záznam zadaného seznamu.

## <a name="syntax"></a>Syntaxe

```vb
LISTOFFIRSTITEM (list)
```

## <a name="arguments"></a>Argumenty

`list`: *seznam záznamů*

Platná cesta ke zdroji dat typu *seznam záznamů*.

## <a name="return-values"></a>Vrácené hodnoty

*Seznam záznamů*

Výsledný seznam záznamů.

## <a name="example"></a>Příklad

Výraz `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` vrátí textovou hodnotu **"A"**.

## <a name="additional-resources"></a>Další zdroje

[Funkce seznamu](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]