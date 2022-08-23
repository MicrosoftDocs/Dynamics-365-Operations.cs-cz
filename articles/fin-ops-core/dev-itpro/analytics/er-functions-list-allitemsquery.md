---
title: Funkce elektronického výkaznictví ALLITEMSQUERY
description: Tento článek obsahuje obecné informace o použití funkce ALLITEMSQUERY elektronického výkaznictví.
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
ms.openlocfilehash: e350dfbe800ddc3e7b1f388fb951d091a283f4e3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285298"
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
