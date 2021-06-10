---
title: Funkce elektronického výkaznictví INDEX
description: Toto téma obsahuje obecné informace o použití funkce INDEX elektronického výkaznictví.
author: NickSelin
ms.date: 05/20/2021
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
ms.openlocfilehash: 5a0fdb8958670efe8e2a37cee183bf836fa6c7e8
ms.sourcegitcommit: 047b0503868cc7d7b21868e24405d76af35db747
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/21/2021
ms.locfileid: "6087744"
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

> [!NOTE]
> Protože se pro tuto funkci používá číslování založené na čísle 1, zadejte hodnotu **1** pro návrat prvního záznamu ze zadaného seznamu.

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
