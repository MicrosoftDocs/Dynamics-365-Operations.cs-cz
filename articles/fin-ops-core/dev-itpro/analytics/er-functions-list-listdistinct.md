---
title: Funkce LISTDISTINCT ER
description: Toto téma obsahuje obecné informace o použití funkce LISTDISTINCT elektronického výkaznictví.
author: NickSelin
manager: kfend
ms.date: 7/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 791038981e88d0f52026bfb17d2d1fa381f28c46
ms.sourcegitcommit: 41e165482b9bff4175c0e3b224dbeead13461956
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/11/2020
ms.locfileid: "3688000"
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