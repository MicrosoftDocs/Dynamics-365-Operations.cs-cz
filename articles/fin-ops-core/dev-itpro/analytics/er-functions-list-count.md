---
title: Funkce elektronického výkaznictví COUNT
description: Toto téma obsahuje obecné informace o použití funkce COUNT elektronického výkaznictví.
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
ms.openlocfilehash: 2d29b82a8c3b108f7651e6d593cb17e7ec8ca872
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916239"
---
# <a name="COUNT">Funkce elektronického výkaznictví COUNT</a>

[!include [banner](../includes/banner.md)]

Funkce `COUNT` vrátí hodnotu typu *celé číslo*, která představuje počet záznamů v zadaném seznamu, pokud seznam není prázdný. Pokud je seznam prázdný, tato funkce vrátí hodnotu **0** (nula).

## <a name="syntax"></a>Syntaxe

```
COUNT (list)
```

## <a name="arguments"></a>Argumenty

`list`: *seznam záznamů*

Platná cesta ke zdroji dat typu *seznam záznamů*.

## <a name="return-values"></a>Vrácené hodnoty

*Celé číslo*

Výsledná číselná hodnota.

## <a name="example"></a>Příklad

`COUNT (SPLIT("abcd" , 3))` vrátí hodnotu **2**, protože funkce `SPLIT` použitá v tomto příkladu vytvoří seznam obsahující dva záznamy.

## <a name="additional-resources"></a>Další zdroje

[Funkce seznamu](er-functions-category-list.md)
