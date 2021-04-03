---
title: Funkce elektronického výkaznictví ALLITEMSQUERY
description: Toto téma obsahuje obecné informace o použití funkce ALLITEMSQUERY elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 56ac956cdfe28d282b8a80d7caec34a50eca5dbe
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559596"
---
# <a name="allitemsquery-er-function"></a>Funkce elektronického výkaznictví ALLITEMSQUERY

[!include [banner](../includes/banner.md)]

Funkce `ALLITEMSQUERY` je spuštěna jako připojený dotaz SQL. Vrátí novou sloučenou hodnotu typu *seznam záznamů*, která se skládá ze seznamu záznamů představujících všechny položky, které odpovídají zadané cestě.

## <a name="syntax"></a>Syntaxe

```vb
ALLITEMSQUERY (path)
```

## <a name="arguments"></a>Argumenty

`path`: *seznam záznamů*

Platná cesta ke zdroji dat typu *seznam záznamů*. Musí obsahovat alespoň jednu relaci.

## <a name="return-values"></a>Vrácené hodnoty

*Seznam záznamů*

Výsledný seznam záznamů.

## <a name="usage-notes"></a>Poznámky k použití

Zadaná cesta musí být definována jako platná cesta zdroje dat k prvku zdroje dat typu *seznam záznamů*. Musí také obsahovat alespoň jednu relaci. Datové prvky, jako je *řetězec* a *datum* cesty, by měly zobrazit chybu v době návrhu v tvůrci výrazů elektronického výkaznictví.

Pokud je tato funkce použita pro zdroje dat typu *seznam záznamů*, které odkazují na objekt aplikace, který lze přímo volat pomocí jazyka SQL (například tabulka, entita nebo dotaz), je spuštěna jako připojený dotaz SQL. V opačném případě běží v paměti jako funkce [ALLITEMS](er-functions-list-allitems.md).

## <a name="example"></a>Příklad

Definujte v mapování modelu následující zdroje dat:

- Zdroj dat **CustInv** typu *záznamy tabulky*, který odkazuje na tabulku CustInvoiceTable
- Zdroj dat **FilteredInv** typu *vypočítané pole*, který obsahuje výraz `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")`
- Zdroj dat **JourLines** typu *vypočítané pole*, který obsahuje výraz `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)`

Při spuštění mapování modelu k volání zdroje dat **JourLines** se spustí příkaz SQL:

```sql
SELECT ... FROM CUSTINVOICETABLE T1 CROSS JOIN CUSTINVOICEJOUR T2 CROSS JOIN
CUSTINVOICETRANS T3 WHERE...
```

## <a name="additional-resources"></a>Další zdroje

[Funkce seznamu](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]