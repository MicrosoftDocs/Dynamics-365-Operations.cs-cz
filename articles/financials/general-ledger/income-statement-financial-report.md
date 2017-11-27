---
title: "Finanční sestava výkazu příjmu"
description: "Tento článek popisuje výchozí sestavu pro výsledovky. Popisuje také stavební bloky, které jsou přidruženy k této sestavě."
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8ca90b949a1a2b5af4a0fd78ddf80d5add2565b9
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="income-statement-financial-report"></a><span data-ttu-id="d6b18-104">Finanční sestava výkazu příjmu</span><span class="sxs-lookup"><span data-stu-id="d6b18-104">Income statement financial report</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d6b18-105">Tento článek popisuje výchozí sestavu pro výsledovky.</span><span class="sxs-lookup"><span data-stu-id="d6b18-105">This article describes the default report for income statements.</span></span> <span data-ttu-id="d6b18-106">Popisuje také stavební bloky, které jsou přidruženy k této sestavě.</span><span class="sxs-lookup"><span data-stu-id="d6b18-106">It also describes the building blocks that are associated with this report.</span></span> 

<a name="default-income-statement-report"></a><span data-ttu-id="d6b18-107">Výchozí sestava výkazu příjmu</span><span class="sxs-lookup"><span data-stu-id="d6b18-107">Default income statement report</span></span>
-------------------------------

| <span data-ttu-id="d6b18-108">Výchozí sestava</span><span class="sxs-lookup"><span data-stu-id="d6b18-108">Default report</span></span>             | <span data-ttu-id="d6b18-109">Jak funguje</span><span class="sxs-lookup"><span data-stu-id="d6b18-109">What it does</span></span>                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6b18-110">Výkaz příjmu – výchozí</span><span class="sxs-lookup"><span data-stu-id="d6b18-110">Income Statement – Default</span></span> | <span data-ttu-id="d6b18-111">Umožňuje zobrazit ziskovost organizace za aktuální období a také od začátku roku.</span><span class="sxs-lookup"><span data-stu-id="d6b18-111">Provides a view of the organization’s profitability for the current period and also for the year to date.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="d6b18-112">Stavební bloky</span><span class="sxs-lookup"><span data-stu-id="d6b18-112">Building blocks</span></span>
<span data-ttu-id="d6b18-113">Finanční sestava výkazu příjmu používá následující stavební bloky.</span><span class="sxs-lookup"><span data-stu-id="d6b18-113">The income statement financial report uses the following building blocks.</span></span>

| <span data-ttu-id="d6b18-114">Výchozí sestava</span><span class="sxs-lookup"><span data-stu-id="d6b18-114">Default report</span></span>             | <span data-ttu-id="d6b18-115">Definice řádku</span><span class="sxs-lookup"><span data-stu-id="d6b18-115">Row definition</span></span>                     | <span data-ttu-id="d6b18-116">Definice sloupce</span><span class="sxs-lookup"><span data-stu-id="d6b18-116">Column definition</span></span>          |
|----------------------------|------------------------------------|----------------------------|
| <span data-ttu-id="d6b18-117">Výkaz příjmu – výchozí</span><span class="sxs-lookup"><span data-stu-id="d6b18-117">Income Statement - Default</span></span> | <span data-ttu-id="d6b18-118">Souhrnný výkazu příjmu – výchozí</span><span class="sxs-lookup"><span data-stu-id="d6b18-118">Summary Income Statement - Default</span></span> | <span data-ttu-id="d6b18-119">Periodický a od začátku roku – výchozí</span><span class="sxs-lookup"><span data-stu-id="d6b18-119">Periodic and YTD - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="d6b18-120">Definice řádku</span><span class="sxs-lookup"><span data-stu-id="d6b18-120">Row definition</span></span>

<span data-ttu-id="d6b18-121">Definice řádku Souhrnný výkazu příjmu – výchozí obsahuje oddíl pro každou část tradičního výkazu příjmu.</span><span class="sxs-lookup"><span data-stu-id="d6b18-121">The row definition, Summary Income Statement – Default, contains a section for each part of a traditional income statement.</span></span> <span data-ttu-id="d6b18-122">Dimenze kategorie hlavního účtu se používá k vytvoření této definice řádku.</span><span class="sxs-lookup"><span data-stu-id="d6b18-122">The Main Account Category dimension is used to build this row definition.</span></span> <span data-ttu-id="d6b18-123">Z toho vyplývá, že každý může generovat sestavu bez nutnosti provádět změny.</span><span class="sxs-lookup"><span data-stu-id="d6b18-123">Therefore, anyone can generate the report without having to make any modifications.</span></span>

### <a name="column-definition"></a><span data-ttu-id="d6b18-124">Definice sloupce</span><span class="sxs-lookup"><span data-stu-id="d6b18-124">Column Definition</span></span>

<span data-ttu-id="d6b18-125">Definice sloupců obsahují různé typy sloupců, které poskytují různé úrovně podrobností a finanční údaje.</span><span class="sxs-lookup"><span data-stu-id="d6b18-125">The column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="d6b18-126">**Periodický a od začátku roku – výchozí typy sloupce:**</span><span class="sxs-lookup"><span data-stu-id="d6b18-126">**Periodic and YTD – Default column types:**</span></span>
    -   <span data-ttu-id="d6b18-127">**DESC** – popis z definice řádku</span><span class="sxs-lookup"><span data-stu-id="d6b18-127">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="d6b18-128">**FD** – finanční údaje pro aktuální období</span><span class="sxs-lookup"><span data-stu-id="d6b18-128">**FD** – Financial data for the current period</span></span>
    -   <span data-ttu-id="d6b18-129">**FD** – finanční údaje od začátku roku</span><span class="sxs-lookup"><span data-stu-id="d6b18-129">**FD** – Financial data for the year to date</span></span>

 

<a name="see-also"></a><span data-ttu-id="d6b18-130">Viz také</span><span class="sxs-lookup"><span data-stu-id="d6b18-130">See also</span></span>
--------

[<span data-ttu-id="d6b18-131">Finanční výkaznictví</span><span class="sxs-lookup"><span data-stu-id="d6b18-131">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="d6b18-132">Zobrazení finančních sestav</span><span class="sxs-lookup"><span data-stu-id="d6b18-132">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="d6b18-133">Blog o finančním výkaznictví v Dynamics</span><span class="sxs-lookup"><span data-stu-id="d6b18-133">Dynamics Financial Reporting Blog</span></span>](http://blogs.msdn.com/b/dynamics_financial_reporting/)




