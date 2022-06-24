---
title: Funkce elektronického výkaznictví EMPTYRECORD
description: Tento článek obsahuje obecné informace o použití funkce EMPTYRECORD elektronického výkaznictví.
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
ms.openlocfilehash: 6f339347187f145b90f14d56017097ff3d7712e8
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886813"
---
# <a name="emptyrecord-er-function"></a>Funkce elektronického výkaznictví EMPTYRECORD

[!include [banner](../includes/banner.md)]

Funkce `EMPTYRECORD` vrací prázdnou hodnotu typu *kontejner (záznam)*, která má stejnou strukturu jako zadaný seznam záznamů nebo záznam.

## <a name="syntax"></a>Syntaxe

```vb
EMPTYRECORD (list)
```

## <a name="arguments"></a>Argumenty

`list`: *seznam záznamů* nebo *kontejner (záznam)*

Platná cesta ke zdroji dat buď typu *seznam záznamů* nebo *kontejner (záznam)*.

## <a name="return-values"></a>Vrácené hodnoty

*Kontejner (záznam)*

Výsledná hodnota atributu.

## <a name="usage-notes"></a>Poznámky k použití

> [!NOTE] 
> Záznam null je záznam, kde všechna pole mají prázdnou hodnotu. Prázdná hodnota je **0** (nula) pro čísla, prázdný řetězec pro řetězce atd.

## <a name="example"></a>Příklad

`EMPTYRECORD (SPLIT ("abc", 1))` vrátí nový prázdný záznam, který má stejnou strukturu jako seznam vrácený funkcí `SPLIT`. Další informace naleznete v tématu [SPLIT](er-functions-list-split.md)

## <a name="additional-resources"></a>Další zdroje

[Funkce záznamu](er-functions-category-record.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]