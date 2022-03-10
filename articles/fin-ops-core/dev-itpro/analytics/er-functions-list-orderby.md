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
ms.openlocfilehash: 963d55bcf98a9109c8b6ceb57edf5b55f15a2b0f
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075167"
---
# <a name="orderby-er-function"></a>Funkce elektronického výkaznictví ORDERBY

[!include [banner](../includes/banner.md)]

Funkce `ORDERBY` vrátí zadaný seznam jako hodnotu typu *seznam záznamů* poté, co byl seřazen podle zadaných argumentů. Tyto argumenty lze definovat jako výrazy.

## <a name="syntax-1"></a><a name="syntax-1"></a>Syntaxe 1

```vb
ORDERBY (list, expression 1[, expression 2, …, expression N])
```

## <a name="syntax-2"></a><a name="syntax-2"></a>Syntaxe 2

```vb
ORDERBY (location, list, expression 1[, expression 2, …, expression N])
```

> [!NOTE]
> Tato syntace je podporována Microsoft Dynamics 365 Finance verze 10.0.25 a novější.

## <a name="arguments"></a>Argumenty

`location`: *[Řetězec](er-formula-supported-data-types-primitive.md#string)*

Místo, kde se má řazení spustit. Platné jsou tyto možnosti:

- "Query"
- "InMemory"

`list`: *[Seznam záznamů](er-formula-supported-data-types-composite.md#record-list)*

Platná cesta ke zdroji dat typu *seznam záznamů*.

`expression 1`: *pole*

Platná cesta k poli zdroje dat, na který odkazuje argument `list` volané funkce. Odkazované pole musí být primitivního datového typu. Tento argument je povinný.

`expression N`: *pole*

Platná cesta k poli zdroje dat, na který odkazuje argument `list` volané funkce. Odkazované pole musí být primitivního datového typu. Tyto další argumenty jsou nepovinné.

## <a name="return-values"></a>Vrácené hodnoty

*Seznam záznamů*

Výsledný seznam záznamů.

## <a name="usage-notes"></a>Poznámky k použití

### <a name="syntax-1"></a>Syntaxe 1

Řazení dat se vždy provádí v paměti aplikačního serveru. Další podrobnosti viz [příklad 1](#example-1).

### <a name="syntax-2"></a>Syntaxe 2

### <a name="sorting-in-memory"></a>Řazení v paměti

Když je argument `location` je specifikován jako **InMemory**, řazení dat se provádí v paměti aplikačního serveru. Další podrobnosti viz [příklad 2](#example-2).

### <a name="sorting-in-database"></a>Řazení v databázi

Když je argument `location` specifikován jako **Dotaz**, řazení dat se provádí na úrovni databáze. V tomto případě argument `list` musí ukazovat na jeden z následujících zdrojů dat [elektronického vykazování (ER)](general-electronic-reporting.md), který specifikuje zdroj aplikace, pro který lze vytvořit přímý databázový dotaz:

- Zdroj dat typu *Záznamy tabulky*
- Vztah zdroje dat typu *Záznamy tabulky*
- Zdroj dat typu *Pole výpočtu*

Argumenty `expression 1` a `expression N` musí ukazovat na pole zdroje dat ER, které specifikuje příslušná pole zdroje aplikace, pro který lze vytvořit přímý databázový dotaz:

Pokud nelze navázat přímý dotaz na databázi, dojde v návrháři mapování modelu ER k [chybě](er-components-inspections.md#i18) ověření. Zpráva, kterou obdržíte, uvádí, že výraz ER obsahující funkci `ORDERBY` nelze spustit za běhu programu.

Pro lepší výkon doporučujeme používat možnost **Dotaz**, když je řazení nakonfigurováno pro aplikační zdroje dat, které mohou obsahovat velký počet záznamů (například pro transakční aplikační tabulky).

> [!NOTE]
> Samotnou funkci `ORDEBY` nelze převést na přímý databázový dotaz. Proto zdroj dat ER, který obsahuje tuto funkci, nelze dotazovat. Rovněž ho nelze použít v rámci funkcí ER, jako je např. [FILTER](er-functions-list-filter.md) a [ALLITEMSQUERY](er-functions-list-allitemsquery.md), kde lze použít pouze dotazovatelné zdroje dat.

Další podrobnosti viz [příklad 3](#example-3) a [příklad 4](#example-4).

### <a name="comparability"></a>Srovnatelnost

Protože databázový modul SQL a aplikační server Finance mohou pro jeden znak používat různé hodnoty hodnocení, může se výsledek řazení stejného seznamu záznamů lišit, když se pro řazení používá pole [Řetězec](er-formula-supported-data-types-primitive.md#string). Další podrobnosti viz [příklad 5](#example-5).

## <a name="example-1-in-memory-default-execution"></a><a name="example-1"></a>Příklad 1: Výchozí spuštění v paměti

Pokud zadáte zdroj dat **DS** typu *vypočítané pole* a ten obsahuje výraz `SPLIT ("C|B|A", "|")`, výraz `FIRST( ORDERBY( DS, DS. Value)).Value` vrátí textovou hodnotu **"A"**.

## <a name="example-2-in-memory-explicit-execution"></a><a name="example-2"></a>Příklad 2: Explicitní spuštění v paměti

Jestliže **Dodavatel** nakonfigurován jako zdroj dat ER typu *Záznamy tabulky*, který odkazuje na tabulku **VendTable**, výraz `ORDERBY (Vendor, Vendor.'name()')` i výraz `ORDERBY ("InMemory", Vendor, Vendor.'name()')` vrátí seznam dodavatelů seřazených podle názvu ve vzestupném pořadí.

Když nakonfigurujete výraz `ORDERBY ("Query", Vendor, Vendor.'name()')` v návrháři mapování modelu ER, [chyba](er-components-inspections.md#i8) ověření se vyskytuje v době návrhu, protože cesta `Vendor.'name()'` odkazuje na metodu aplikace, která má logiku, kterou nelze převést na přímý databázový dotaz.

## <a name="example-3-database-query"></a><a name="example-3"></a>Příklad 3: Databázový dotaz

Pokud je **TaxTransaction** nakonfigurováno jako zdroj dat ER typu *Záznamy tabulky*, který odkazuje na tabulku **TaxTrans**, výraz `ORDERBY ("Query", TaxTransaction, TaxTransaction.TaxCode)` seřadí záznamy na úrovni databáze aplikace a vrátí seznam daňových transakcí, který je seřazen vzestupně podle kódu daně.

## <a name="example-4-queryable-data-sources"></a><a name="example-4"></a>Příklad 4: Dotazovatelné zdroje dat

Pokud je **TaxTransaction** nakonfigurováno jako zdroj dat ER typu *Záznamy tabulky*, který odkazuje na tabulku **TaxTrans**, zdroj dat ER **TaxTransactionFiltered** lze nakonfigurovat tak, aby obsahoval výraz `FILTER(TaxTransaction, TaxCode="VAT19")`, který načte transakce pro zadaný daňový kód. Protože nakonfigurovaný zdroj dat ER **TaxTransactionFiltered** je dotazovatelný, výraz `ORDERBY ("Query", TaxTransactionFiltered, TaxTransactionFiltered.TransDate)` lze nakonfigurovat tak, aby vracel seznam filtrovaných daňových transakcí seřazený podle data transakce ve vzestupném pořadí.

Pokud nakonfigurujete **TaxTransactionOrdered** jako zdroj dat ER typu *Počítané pole*, který obsahuje výraz `ORDERBY ("Query", TaxTransaction, TaxTransaction.TransDate)`, a zdroj dat ER typu *Počítané pole*, který obsahuje výraz `FILTER(TaxTransactionOrdered, TaxCode="VAT19")`, dojde k [chybě](er-components-inspections.md#i18) ověření v době návrhu v návrháři mapování modelu ER. K této chybě dochází, protože první argument funkce [FILTER](er-functions-list-filter.md#usage-notes) musí odkazovat na dotazovatelný zdroj dat ER, ale zdroj dat **TaxTransactionOrdered** , který obsahuje funkci `ORDERBY` není dotazovatelný.

## <a name="example-5-comparability"></a><a name="example-5"></a>Příklad 5: Srovnatelnost

### <a name="prerequisites"></a>Předpoklady

1. Zadejte zdroj dat **DS1** typu *Vypočítané pole*, který obsahuje výraz `SPLIT ("D1|_D2|D3", "|")`.
2. Otevřete stránku **[Hodnoty finanční dimenze](../../../finance/general-ledger/financial-dimensions.md)** a vyberte dimenzi **CostCenter**.
3. Zadejte následující hodnoty dimenzí: **D1**, **\_D2** a **D3**.

### <a name="sorting-in-memory"></a>Řazení v paměti

1. Nakonfigurujte zdroj dat **DS2** typu *Počítané pole*, který obsahuje výraz `ORDERBY("InMemory", DS1, DS1.Value)`.
2. Všimněte si, že výraz `FIRST(DS2).Value` vrátí textovou hodnotu **"D1"**, výraz `INDEX(DS2, COUNT(DS2)).Value` vrátí textovou hodnotu **"\_D2"** a výraz `STRINGJOIN(DS2, DS2.Value, "|")` vrátí textovou hodnotu **"D1\|D3\|\_D2"**.

### <a name="sorting-in-database"></a>Řazení v databázi

1. Zadejte zdroj dat **DS3** typu *Záznamy tabulky*, který odkazuje na entitu **FinancialDimensionValueEntity**.
2. Nakonfigurujte zdroj dat **DS4** typu *Počítané pole*, který obsahuje výraz `FILTER(DS3, DS3.FinancialDimension="CostCenter")`.
3. Nakonfigurujte zdroj dat **DS5** typu *Počítané pole*, který obsahuje výraz `ORDERBY(DS4, DS4.DimensionValue)`.
4. Všimněte si, že výraz `FIRST(DS5).Value` vrátí textovou hodnotu **"\_D2"**, výraz `INDEX(DS5, COUNT(DS5)).Value` vrátí textovou hodnotu **"D3"** a výraz `STRINGJOIN(DS5, DS5.Value, "|")` vrátí textovou hodnotu **"\_D2\|D1\|D3"**.

## <a name="additional-resources"></a>Další prostředky

[Funkce seznamu](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
