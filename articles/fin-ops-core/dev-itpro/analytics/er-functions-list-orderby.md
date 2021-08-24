---
title: Funkce elektronického výkaznictví ORDERBY
description: Toto téma obsahuje obecné informace o použití funkce ORDERBY elektronického výkaznictví.
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
ms.openlocfilehash: fcacacbf0727fa26350ff23c781c2da54d0ba77262c94dd48d88d01444352947
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776139"
---
# <a name="orderby-er-function"></a>Funkce elektronického výkaznictví ORDERBY

[!include [banner](../includes/banner.md)]

Funkce `ORDERBY` vrátí zadaný seznam jako hodnotu typu *seznam záznamů* poté, co byl seřazen podle zadaných argumentů. Tyto argumenty lze definovat jako výrazy.

## <a name="syntax"></a>Syntaxe

```vb
ORDERBY (list , expression 1[, expression 2, …, expression N])
```

## <a name="arguments"></a>Argumenty

`list`: *seznam záznamů*

Platná cesta ke zdroji dat typu *seznam záznamů*.

`expression 1`: *pole*

Platná cesta k poli zdroje dat, na který odkazuje argument `list` volané funkce. Odkazované pole musí být primitivního datového typu. Tento argument je povinný.

`expression N`: *pole*

Platná cesta k poli zdroje dat, na který odkazuje argument `list` volané funkce. Odkazované pole musí být primitivního datového typu. Tyto další argumenty jsou nepovinné.

## <a name="return-values"></a>Vrácené hodnoty

*Seznam záznamů*

Výsledný seznam záznamů.

## <a name="example-1"></a>Příklad 1

Pokud zadáte zdroj dat **DS** typu *vypočítané pole* a ten obsahuje výraz `SPLIT ("C|B|A", "|")`, výraz `FIRST( ORDERBY( DS, DS. Value)).Value` vrátí textovou hodnotu **"A"**.

## <a name="example-2"></a>Příklad 2

Jestliže je položka **Vendor** konfigurována jako zdroj dat elektronického výkaznictví, který odkazuje na tabulku VendTable, výraz `ORDERBY (Vendors, Vendors.'name()')` vrátí seznamu dodavatelů seřazených podle názvu ve vzestupném pořadí.

## <a name="additional-resources"></a>Další zdroje

[Funkce seznamu](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]