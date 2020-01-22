---
title: Funkce elektronického výkaznictví ALLITEMS
description: Toto téma obsahuje obecné informace o použití funkce ALLITEMS elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 79c43b6ecdb307433b0c2091840c21a5ada3a689
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917435"
---
# <a name="ALLITEMS">Funkce elektronického výkaznictví ALLITEMS</a>

[!include [banner](../includes/banner.md)]

Funkce `ALLITEMS` je spuštěna jako výběr v paměti a vrací novou sloučenou hodnotu typu *seznam záznamů* jako seznam záznamů, který představuje všechny položky odpovídající zadané cestě.

## <a name="syntax"></a>Syntaxe

```
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
