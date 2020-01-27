---
title: Funkce elektronického výkaznictví LISTOFFIRSTITEM
description: Toto téma obsahuje obecné informace o použití funkce LISTOFFIRSTITEM elektronického výkaznictví.
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
ms.openlocfilehash: 4d985ef5015bc104a83260b64418821cc715e8cb
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917251"
---
# <a name="LISTOFFIRSTITEM">Funkce elektronického výkaznictví LISTOFFIRSTITEM</a>

[!include [banner](../includes/banner.md)]

Funkce `LISTOFFIRSTITEM` vrátí hodnotu typu *seznam záznamů*, která obsahuje pouze první záznam zadaného seznamu.

## <a name="syntax"></a>Syntaxe

```
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
