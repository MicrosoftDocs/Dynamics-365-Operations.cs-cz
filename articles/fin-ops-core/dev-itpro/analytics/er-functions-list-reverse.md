---
title: Funkce elektronického výkaznictví REVERSE
description: Tento článek obsahuje obecné informace o použití funkce REVERSE elektronického výkaznictví.
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
ms.openlocfilehash: fce611b755865db15e8877e58d59bdf36bc730fe
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8881512"
---
# <a name="reverse-er-function"></a>Funkce elektronického výkaznictví REVERSE

[!include [banner](../includes/banner.md)]

Funkce `REVERSE` vrátí zadaný seznam jako hodnotu typu *seznam záznamů* v obráceném pořadí.

## <a name="syntax"></a>Syntaxe

```vb
REVERSE (list)
```

## <a name="arguments"></a>Argumenty

`list`: *seznam záznamů*

Platná cesta ke zdroji dat typu *seznam záznamů*.

## <a name="return-values"></a>Vrácené hodnoty

*Seznam záznamů*

Výsledný seznam záznamů.

## <a name="example-1"></a>Příklad 1

Pokud zadáte zdroj dat **DS** typu *vypočítané pole* a ten obsahuje výraz `SPLIT ("C|B|A", "|")`, výraz `FIRST( REVERSE( ORDERBY( DS, DS. Value))).Value` vrátí textovou hodnotu **"C"**.

## <a name="example-2"></a>Příklad 2

Jestliže je položka **Vendor** konfigurována jako zdroj dat elektronického výkaznictví, který odkazuje na tabulku VendTable, výraz `REVERSE (ORDERBY (Vendors, Vendors.'name()'))` vrátí seznamu dodavatelů seřazených podle názvu v sestupném pořadí.

## <a name="additional-resources"></a>Další zdroje

[Funkce seznamu](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]