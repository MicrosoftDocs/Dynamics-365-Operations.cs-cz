---
title: Funkce elektronického výkaznictví FILTER
description: Toto téma obsahuje obecné informace o použití funkce FILTER elektronického výkaznictví.
author: NickSelin
ms.date: 12/14/2021
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
ms.openlocfilehash: e857306574dda7bad5dd25fc7708514997d8e86f
ms.sourcegitcommit: b1c758ec4abfcf3bf9e50f18c1102d4a9c1316d0
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/15/2021
ms.locfileid: "7922416"
---
# <a name="filter-er-function"></a>Funkce elektronického výkaznictví FILTER

[!include [banner](../includes/banner.md)]

Funkce `FILTER` vrátí zadaný seznam jako hodnotu typu *seznam záznamů* po změně dotazu, který jej filtruje podle zadané podmínky.

## <a name="syntax"></a>Syntaxe

```vb
FILTER (list, condition)
```

## <a name="arguments"></a>Argumenty

`list`: *seznam záznamů*

Platná cesta ke zdroji dat typu *seznam záznamů*.

`condition`: *logická hodnota*

Platný podmíněný výraz, který slouží k filtrování záznamů zadaného seznamu.

## <a name="return-values"></a>Vrácené hodnoty

*Seznam záznamů*

Výsledný seznam záznamů.

## <a name="usage-notes"></a><a name="usage-notes"></a>Poznámky k použití

Tato funkce se liší od funkce [WHERE](er-functions-list-where.md), protože zadaná podmínka je použita u jakéhokoli zdroje dat elektronického výkaznictví typu *Záznamy tabulky* na úrovni databáze. Seznam a podmínku lze definovat pomocí tabulek a relací.

Pokud jeden či více argumentů konfigurovaných pro tuto funkci (`list` a `condition`) neumožňuje překlad tohoto požadavku na přímé volání SQL, dojde v době návrhu k výjimce. Tato výjimka informuje uživatele, že k dotazování databáze nelze použít `list` nebo `condition`.

> [!NOTE]
> Když je k zadání kritérií výběru použita funkce [`VALUEIN`](er-functions-logical-valuein.md), funkce `FILTER` se chová jinak než funkce `WHERE`.
> 
> - Pokud je funkce `VALUEIN` použita v rozsahu funkce `WHERE` a druhý argument funkce `VALUEIN` odkazuje na zdroj dat, který nevrací žádné záznamy, zváží se logická hodnota *[False](er-formula-supported-data-types-primitive.md#boolean)* vrácená funkcí `VALUEIN`. Proto výraz `WHERE(Vendors, VALUEIN(Vendors.VendGroup, VendGroups, VendGroups.VendGroup))` nevrací žádné záznamy dodavate, pokud zdroj dat **VendGroups** nevrací žádné záznamy skupiny dodavatelů.
> - Pokud je funkce `VALUEIN` použita v rozsahu funkce `FILTER` a druhý argument funkce `VALUEIN` odkazuje na zdroj dat, který nevrací žádné záznamy, ignoruje se logická hodnota *[False](er-formula-supported-data-types-primitive.md#boolean)* vrácená funkcí `VALUEIN`. Proto výraz `FILTER(Vendors, VALUEIN(Vendors.VendGroup, VendGroups, VendGroups.VendGroup))` vrátí všechny záznamy dodavate zdroje dat **Vendors**, i když zdroj dat **VendGroups** nevrací žádné záznamy skupiny dodavatelů.

## <a name="example-1"></a>Příklad 1

Jestliže je položka **Vendor** konfigurována jako zdroj dat elektronického výkaznictví, který odkazuje na tabulku VendTable, výraz `FILTER (Vendors, Vendors.VendGroup = "40")` vrátí seznam pouze dodavatelů patřících do skupiny dodavatelů č. 40.

## <a name="example-2"></a>Příklad 2

Pokud je položka **Vendor** konfigurována jako zdroj dat elektronického výkaznictví, který se vztahuje k tabulce VendTable a pokud je parametr **parmVendorBankGroup** konfigurován jako zdroj dat elektronického výkaznictví, který vrací hodnotu datového typu *řetězec*, výraz `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` vrátí seznam pouze těch dodavatelských účtů, které patří ke konkrétní bankovní skupině.

## <a name="example-3"></a>Příklad 3

Zadáte zdroj dat **DS** typu *vypočítané pole* a ten obsahuje výraz `SPLIT ("A,B,C", ",")`. Potom zadáte jiný výraz `FILTER( DS, DS.Value = "B")`. Při pokusu o uložení tohoto výrazu v návrháři receptur elektronického výkaznictví je vyvolána následující výjimka: „Chyba ověření: na výraz seznamu funkce FILTER se nelze dotazovat.“

## <a name="additional-resources"></a>Další zdroje

[Funkce seznamu](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
