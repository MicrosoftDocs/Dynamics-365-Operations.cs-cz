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
# <a name="listdistinct-er-function"></a><span data-ttu-id="38b02-103">Funkce LISTDISTINCT ER</span><span class="sxs-lookup"><span data-stu-id="38b02-103">LISTDISTINCT ER Function</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="38b02-104">Funkce `LISTDISTINCT` vypočítá zadaný výraz jako selektor pro každý záznam zadaného seznamu.</span><span class="sxs-lookup"><span data-stu-id="38b02-104">The `LISTDISTINCT` function calculates the specified expression as a selector for every record of the specified list.</span></span> <span data-ttu-id="38b02-105">Vrací novou hodnotu *Seznam záznamů*, která obsahuje jeden záznam pro každou jedinečnou hodnotu selektoru.</span><span class="sxs-lookup"><span data-stu-id="38b02-105">It returns a new *Record list* value that contains a single record for each unique selector value.</span></span>

## <a name="syntax"></a><span data-ttu-id="38b02-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="38b02-106">Syntax</span></span>

```
LISTDISTINCT (list, selector)
```

## <a name="arguments"></a><span data-ttu-id="38b02-107">Argumenty</span><span class="sxs-lookup"><span data-stu-id="38b02-107">Arguments</span></span>

<span data-ttu-id="38b02-108">`list`: *seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="38b02-108">`list`: *Record list*</span></span>

<span data-ttu-id="38b02-109">Platná cesta ke zdroji dat typu *seznam záznamů*.</span><span class="sxs-lookup"><span data-stu-id="38b02-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="38b02-110">`selector`: *Typ primitivních dat*</span><span class="sxs-lookup"><span data-stu-id="38b02-110">`selector`: *Primitive data type*</span></span>

<span data-ttu-id="38b02-111">Platný výraz, který se používá pro výpočet hodnoty selektoru pro každý záznam v určeném seznamu.</span><span class="sxs-lookup"><span data-stu-id="38b02-111">A valid expression that is used to calculate a selector value for every record in the specified list.</span></span>

<span data-ttu-id="38b02-112">Pro tento parametr jsou podporovány následující typy dat:</span><span class="sxs-lookup"><span data-stu-id="38b02-112">The following data types are supported for this parameter:</span></span>

- <span data-ttu-id="38b02-113">Boolean</span><span class="sxs-lookup"><span data-stu-id="38b02-113">Boolean</span></span>
- <span data-ttu-id="38b02-114">Datum</span><span class="sxs-lookup"><span data-stu-id="38b02-114">Date</span></span>
- <span data-ttu-id="38b02-115">Datum a čas</span><span class="sxs-lookup"><span data-stu-id="38b02-115">DateTime</span></span>
- <span data-ttu-id="38b02-116">GUID</span><span class="sxs-lookup"><span data-stu-id="38b02-116">GUID</span></span>
- <span data-ttu-id="38b02-117">Celé číslo</span><span class="sxs-lookup"><span data-stu-id="38b02-117">Integer</span></span>
- <span data-ttu-id="38b02-118">Int64</span><span class="sxs-lookup"><span data-stu-id="38b02-118">Int64</span></span>
- <span data-ttu-id="38b02-119">Reálný</span><span class="sxs-lookup"><span data-stu-id="38b02-119">Real</span></span>
- <span data-ttu-id="38b02-120">Řetězec</span><span class="sxs-lookup"><span data-stu-id="38b02-120">String</span></span>

## <a name="return-values"></a><span data-ttu-id="38b02-121">Vrácené hodnoty</span><span class="sxs-lookup"><span data-stu-id="38b02-121">Return values</span></span>

<span data-ttu-id="38b02-122">*Seznam záznamů*</span><span class="sxs-lookup"><span data-stu-id="38b02-122">*Record list*</span></span>

<span data-ttu-id="38b02-123">Výsledný seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="38b02-123">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="38b02-124">Poznámky k použití</span><span class="sxs-lookup"><span data-stu-id="38b02-124">Usage notes</span></span>

<span data-ttu-id="38b02-125">Struktura vytvořeného seznamu odpovídá struktuře zadaného seznamu.</span><span class="sxs-lookup"><span data-stu-id="38b02-125">The structure of the list that is created matches the structure of the specified list.</span></span>

<span data-ttu-id="38b02-126">Stejná hodnota selektoru může být vypočtena pro více záznamů v určeném seznamu.</span><span class="sxs-lookup"><span data-stu-id="38b02-126">The same selector value might be calculated for multiple records in the specified list.</span></span> <span data-ttu-id="38b02-127">V tomto případě se hodnoty pole odpovídajícího záznamu ve vytvořeném seznamu shodují s hodnotami prvního záznamu ze zadaného seznamu, pro který je hodnota selektoru vypočtena.</span><span class="sxs-lookup"><span data-stu-id="38b02-127">In this case, field values of the corresponding record in the created list equal the values of the first record from the specified list that the selector value is calculated for.</span></span>

<span data-ttu-id="38b02-128">Provedení této funkce se provádí na jakémkoli [Elektronickém výkaznictví (ER)](general-electronic-reporting.md) zdroji dat typu *Seznam záznamů*, který je v paměti.</span><span class="sxs-lookup"><span data-stu-id="38b02-128">The execution of this function is done on any [Electronic reporting (ER)](general-electronic-reporting.md) data source of the *Record list* type that is present in memory.</span></span>

<span data-ttu-id="38b02-129">**GROUPBY** zdroj dat lze také použít k vygenerování seznamu záznamů, pro které je selektor, který má odlišné hodnoty, vypočítán.</span><span class="sxs-lookup"><span data-stu-id="38b02-129">The **GROUPBY** data source can also be used to generate the list of records that the selector that has distinct values is calculated for.</span></span> <span data-ttu-id="38b02-130">Z hlediska výkonu a využití paměti je však lepší používat `LISTDISTINCT` funkci než **groupby** zdroj dat, protože funkce se provádí v paměti.</span><span class="sxs-lookup"><span data-stu-id="38b02-130">However, from a performance and memory consumption perspective, it's better to use the `LISTDISTINCT` function than the **GROUPBY** data source, because the execution of the function is done in memory.</span></span>

## <a name="example"></a><span data-ttu-id="38b02-131">Příklad</span><span class="sxs-lookup"><span data-stu-id="38b02-131">Example</span></span>

<span data-ttu-id="38b02-132">Následující příklad ukazuje, jak můžete získat seznam jedinečných čísel zákaznických účtů, ke kterým byla během konkrétního období vystavena alespoň jedna prodejní faktura nebo projektová faktura.</span><span class="sxs-lookup"><span data-stu-id="38b02-132">The following example shows how you can get the list of unique customer account numbers that at least one sales invoice or project invoice has been issued to during a specific period.</span></span>

1. <span data-ttu-id="38b02-133">Zadejte **SalesInvoice** zdroj dat typu `Record list`, který odkazuje na **CustInvoiceJour** tabulku aplikací a filtruje prodejní faktury za konkrétní období.</span><span class="sxs-lookup"><span data-stu-id="38b02-133">Enter the **SalesInvoice** data source of the `Record list` type that refers to the **CustInvoiceJour** application table and filters sales invoices for specific periods.</span></span>

    <span data-ttu-id="38b02-134">`InvoiceAccount` pole tohoto zdroje dat vrátí číslo účtu fakturovaného zákazníka.</span><span class="sxs-lookup"><span data-stu-id="38b02-134">The `InvoiceAccount` field of this data source returns the account number of an invoiced customer.</span></span>

2. <span data-ttu-id="38b02-135">Zadejte **ProjectInvoice** zdroj dat typu `Record list`, který odkazuje na **ProjInvoiceJour** tabulku aplikací a filtruje faktury projektů za konkrétní období.</span><span class="sxs-lookup"><span data-stu-id="38b02-135">Enter the **ProjectInvoice** data source of the `Record list` type that refers to the **ProjInvoiceJour** application table and filters project invoices for specific periods.</span></span>

    <span data-ttu-id="38b02-136">`InvoiceAccount` pole tohoto zdroje dat vrátí číslo účtu fakturovaného zákazníka.</span><span class="sxs-lookup"><span data-stu-id="38b02-136">The `InvoiceAccount` field of this data source returns the account number of an invoiced customer.</span></span>

3. <span data-ttu-id="38b02-137">Konfigurace **AllInvoices** zdroje dat `Calculated field` který obsahuje výraz `LISTJOIN(SalesInvoice, ProjectInvoice)`.</span><span class="sxs-lookup"><span data-stu-id="38b02-137">Configure the **AllInvoices** data source of the `Calculated field` type that contains the expression `LISTJOIN(SalesInvoice, ProjectInvoice)`.</span></span>

    <span data-ttu-id="38b02-138">Tento zdroj dat vrací spojený seznam prodejních faktur a projektových faktur.</span><span class="sxs-lookup"><span data-stu-id="38b02-138">This data source returns the joined list of sales invoices and project invoices.</span></span>

4. <span data-ttu-id="38b02-139">Konfigurace **InvoicedCustomer** zdroje dat `Record list` který obsahuje výraz `LISTDISTINCT(AllInvoices, AllInvoices.InvoiceAccount)`.</span><span class="sxs-lookup"><span data-stu-id="38b02-139">Configure the **InvoicedCustomer** data source of the `Record list` type that contains the expression `LISTDISTINCT(AllInvoices, AllInvoices.InvoiceAccount)`.</span></span>

    <span data-ttu-id="38b02-140">Tento zdroj dat vrací nový seznam, který obsahuje jeden záznam pro každého jedinečného zákazníka, který byl fakturován během definovaného období.</span><span class="sxs-lookup"><span data-stu-id="38b02-140">This data source returns a new list that contains a single record for every unique customer that has been invoiced during the defined period.</span></span> <span data-ttu-id="38b02-141">`InvoiceAccount` pole tohoto seznamu obsahuje číslo zákaznického účtu.</span><span class="sxs-lookup"><span data-stu-id="38b02-141">The `InvoiceAccount` field of this list contains a customer account number.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="38b02-142">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="38b02-142">Additional resources</span></span>

[<span data-ttu-id="38b02-143">Funkce seznamu</span><span class="sxs-lookup"><span data-stu-id="38b02-143">List functions</span></span>](er-functions-category-list.md)
