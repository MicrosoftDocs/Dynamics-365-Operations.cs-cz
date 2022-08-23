---
title: Funkce LISTDISTINCT ER
description: Tento článek obsahuje obecné informace o použití funkce LISTDISTINCT elektronického výkaznictví.
author: kfend
ms.date: 07/30/2020
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.custom: ''
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: cd773f3455af1be1e952cb3852a648436670ce0f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285268"
---
# <a name="listdistinct-er-function"></a>Funkce LISTDISTINCT ER

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Funkce `LISTDISTINCT` vypočítá zadaný výraz jako selektor pro každý záznam zadaného seznamu. Vrací novou hodnotu *Seznam záznamů*, která obsahuje jeden záznam pro každou jedinečnou hodnotu selektoru.

## <a name="syntax"></a>Syntaxe

```
LISTDISTINCT (list, selector)
```

## <a name="arguments"></a>Argumenty

`list`: *seznam záznamů*

Platná cesta ke zdroji dat typu *seznam záznamů*.

`selector`: *Typ primitivních dat*

Platný výraz, který se používá pro výpočet hodnoty selektoru pro každý záznam v určeném seznamu.

Pro tento parametr jsou podporovány následující typy dat:

- Boolean
- Datum
- Datum a čas
- GUID
- Celé číslo
- Int64
- Reálný
- Řetězec

## <a name="return-values"></a>Vrácené hodnoty

*Seznam záznamů*

Výsledný seznam záznamů.

## <a name="usage-notes"></a>Poznámky k použití

Struktura vytvořeného seznamu odpovídá struktuře zadaného seznamu.

Stejná hodnota selektoru může být vypočtena pro více záznamů v určeném seznamu. V tomto případě se hodnoty pole odpovídajícího záznamu ve vytvořeném seznamu shodují s hodnotami prvního záznamu ze zadaného seznamu, pro který je hodnota selektoru vypočtena.

Provedení této funkce se provádí na jakémkoli [Elektronickém výkaznictví (ER)](general-electronic-reporting.md) zdroji dat typu *Seznam záznamů*, který je v paměti.

**GROUPBY** zdroj dat lze také použít k vygenerování seznamu záznamů, pro které je selektor, který má odlišné hodnoty, vypočítán. Z hlediska výkonu a využití paměti je však lepší používat `LISTDISTINCT` funkci než **groupby** zdroj dat, protože funkce se provádí v paměti.

## <a name="example"></a>Příklad

Následující příklad ukazuje, jak můžete získat seznam jedinečných čísel zákaznických účtů, ke kterým byla během konkrétního období vystavena alespoň jedna prodejní faktura nebo projektová faktura.

1. Zadejte **SalesInvoice** zdroj dat typu `Record list`, který odkazuje na **CustInvoiceJour** tabulku aplikací a filtruje prodejní faktury za konkrétní období.

    `InvoiceAccount` pole tohoto zdroje dat vrátí číslo účtu fakturovaného zákazníka.

2. Zadejte **ProjectInvoice** zdroj dat typu `Record list`, který odkazuje na **ProjInvoiceJour** tabulku aplikací a filtruje faktury projektů za konkrétní období.

    `InvoiceAccount` pole tohoto zdroje dat vrátí číslo účtu fakturovaného zákazníka.

3. Konfigurace **AllInvoices** zdroje dat `Calculated field` který obsahuje výraz `LISTJOIN(SalesInvoice, ProjectInvoice)`.

    Tento zdroj dat vrací spojený seznam prodejních faktur a projektových faktur.

4. Konfigurace **InvoicedCustomer** zdroje dat `Record list` který obsahuje výraz `LISTDISTINCT(AllInvoices, AllInvoices.InvoiceAccount)`.

    Tento zdroj dat vrací nový seznam, který obsahuje jeden záznam pro každého jedinečného zákazníka, který byl fakturován během definovaného období. `InvoiceAccount` pole tohoto seznamu obsahuje číslo zákaznického účtu.

## <a name="additional-resources"></a>Další prostředky

[Funkce seznamu](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
