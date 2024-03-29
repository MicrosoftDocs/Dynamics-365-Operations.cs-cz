---
title: Funkce elektronického výkaznictví WHERE
description: Tento článek obsahuje obecné informace o použití funkce WHERE elektronického výkaznictví.
author: kfend
ms.date: 12/12/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: b3f8b01bffd0c530e5095531fc184c960744e751
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273151"
---
# <a name="where-er-function"></a>Funkce elektronického výkaznictví WHERE

[!include [banner](../includes/banner.md)]

Funkce `WHERE` vrátí zadaný seznam jako hodnotu typu *seznam záznamů* poté, co byl filtrován podle zadané podmínky.

## <a name="syntax"></a>Syntaxe

```vb
WHERE (list, condition)
```

## <a name="arguments"></a>Argumenty

`list`: *seznam záznamů*

Platná cesta ke zdroji dat typu *seznam záznamů*.

`condition`: *logická hodnota*

Platný podmíněný výraz, který slouží k filtrování záznamů zadaného seznamu.

## <a name="return-values"></a>Vrácené hodnoty

*Seznam záznamů*

Výsledný seznam záznamů.

## <a name="usage-notes"></a>Poznámky k použití

Tato funkce se liší od funkce [FILTER](er-functions-list-filter.md), protože zadaná podmínka se použije na každý zdroj dat elektronického výkaznictví typu *seznam záznamů*, který se nachází v paměti.

Pokud argumenty konfigurované pro tuto funkci (`list` a `condition`) umožňují překlad tohoto požadavku na přímé volání SQL, je v době návrhu vyvolána varovná zpráva. Tato zpráva informuje uživatele o tom, že výkon může být zlepšen, pokud je použita funkce [FILTER](er-functions-list-filter.md) namísto funkce `WHERE`.

## <a name="example-1"></a>Příklad 1

Jestliže je položka **Vendor** konfigurována jako zdroj dat elektronického výkaznictví, který odkazuje na tabulku VendTable, výraz `WHERE (Vendors, Vendors.VendGroup = "40")` vrátí seznam pouze dodavatelů patřících do skupiny dodavatelů č. 40.

## <a name="example-2"></a>Příklad 2

Zadáte-li zdroj dat **DS** pro typ *vypočítané pole* a ten obsahuje výraz `SPLIT ("A|B|C", "|")`, výraz `WHERE( DS, DS.Value = "B")` vrátí seznam pouze jednoho záznamu, který obsahuje text **"B"** v poli **Value**.

## <a name="additional-resources"></a>Další zdroje

[Funkce seznamu](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
