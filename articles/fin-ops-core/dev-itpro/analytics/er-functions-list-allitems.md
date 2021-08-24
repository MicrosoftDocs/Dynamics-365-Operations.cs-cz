---
title: Funkce elektronického výkaznictví ALLITEMS
description: Toto téma obsahuje obecné informace o použití funkce ALLITEMS elektronického výkaznictví.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: cf1e05e9377ba18ad0269a48b13bd242a8e5356f4a52ea3723e347dcf5e138e0
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719841"
---
# <a name="allitems-er-function"></a>Funkce elektronického výkaznictví ALLITEMS

[!include [banner](../includes/banner.md)]

Funkce `ALLITEMS` je spuštěna jako výběr v paměti a vrací novou sloučenou hodnotu typu *seznam záznamů* jako seznam záznamů, který představuje všechny položky odpovídající zadané cestě.

## <a name="syntax"></a>Syntaxe

```vb
ALLITEMS (path)
```

## <a name="arguments"></a>Argumenty

`path`: *seznam záznamů*

Platná cesta ke zdroji dat typu *seznam záznamů*.

## <a name="return-values"></a>Vrácené hodnoty

*Seznam záznamů*

Výsledný seznam záznamů.

## <a name="usage-notes"></a>Poznámky k použití

Cesta musí být definována jako platná cesta zdroje dat k prvku zdroje dat typu *seznam záznamů*. Datové prvky, jako je řetězec a datum cesty, by měly zobrazit chybu v době návrhu v tvůrci výrazů elektronického výkaznictví.

Nedoporučujeme používat tuto funkci pro transakční zdroje dat, které mohou obsahovat velký objem dat. Místo toho zvažte použití funkce [ALLTEMSQUERY](er-functions-list-allitemsquery.md).

## <a name="example-1"></a>Příklad 1

Když zadáte `SPLIT("abcdef" , 2)` jako zdroj dat **DS**, výraz `COUNT( ALLITEMS (DS))` vrátí **"3"**.

## <a name="example-2"></a>Příklad 2

Pokud zadáte **Vend** jako zdroj dat datového typu *seznam záznamů*, který odkazuje na tabulku aplikace VendTable, výraz `ALLITEMS (Vend.'<Relations'.ContactPerson)` vrátí sloučený seznam záznamů, který má strukturu tabulky **ContactPerson** a obsahuje všechny kontaktní osoby, ke kterým lze získat přístup pomocí relace **ContactPerson.ContactForParty == VendTable.Party**, a který je k dispozici všem dodavatelům (vendors) z odkazované tabulky dodavatelů.

## <a name="additional-resources"></a>Další zdroje

[Funkce seznamu](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]