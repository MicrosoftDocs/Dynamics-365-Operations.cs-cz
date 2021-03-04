---
title: Funkce elektronického výkaznictví INDEX
description: Toto téma obsahuje obecné informace o použití funkce INDEX elektronického výkaznictví.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a49def8aaa5398fbc7e0f06cc26df8a745207c93
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687984"
---
# <a name="index-er-function"></a>Funkce elektronického výkaznictví INDEX

[!include [banner](../includes/banner.md)]

Funkce `INDEX` vrátí hodnotu typu *kontejner (záznam)*, která je vybrána pomocí zadaného číselného indexu v zadaném seznamu. Pokud index je mimo rozsah záznamů v zadaném seznamu, dojde k výjimce.

## <a name="syntax"></a>Syntaxe

```vb
INDEX (list, index)
```

## <a name="arguments"></a>Argumenty

`list`: *seznam záznamů*

Platná cesta ke zdroji dat typu *seznam záznamů*.

`index`: *celé číslo*

Číselný index označující pozici požadovaného záznamu v zadaném seznamu.

## <a name="return-values"></a>Vrácené hodnoty

*Kontejner (záznam)*

Výsledná hodnota atributu.

## <a name="example-1"></a>Příklad 1

Zadáte-li zdroj dat **DS** pro typ *vypočítané pole* a ten obsahuje výraz `SPLIT ("A|B|C", "|")`, výraz `DS.Value` vrátí textovou hodnotu **"B"** pro druhý záznam tohoto seznamu záznamů. Výraz `INDEX (SPLIT ("A|B|C", "|"), 2).Value` také vrátí textovou hodnotu **"B"**.

## <a name="example-2"></a>Příklad 2

Pokud zadáte zdroj dat **DS** typu *vypočítané pole* a ten obsahuje výraz `SPLIT ("A|B|C", "|")`, výraz `INDEX (SPLIT ("A|B|C", "|"), 4).Value` způsobí výjimku běhu programu.

## <a name="additional-resources"></a>Další zdroje

[Funkce seznamu](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]