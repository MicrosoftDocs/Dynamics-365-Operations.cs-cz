---
title: Finanční sestava výkazu příjmu
description: Tento článek popisuje výchozí sestavu pro výsledovky. Popisuje také stavební bloky, které jsou přidruženy k této sestavě.
author: jcart1106
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: roschlom
ms.custom: 12294
ms.assetid: 30820be0-d943-4f8b-8c25-6414ec393b3d
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6ab5e7a2675705cc2265b7f894d9b12d4465aea1
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187813"
---
# <a name="income-statement-financial-report"></a><span data-ttu-id="c51c0-104">Finanční sestava výkazu příjmu</span><span class="sxs-lookup"><span data-stu-id="c51c0-104">Income statement financial report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c51c0-105">Tento článek popisuje výchozí sestavu pro výsledovky.</span><span class="sxs-lookup"><span data-stu-id="c51c0-105">This article describes the default report for income statements.</span></span> <span data-ttu-id="c51c0-106">Popisuje také stavební bloky, které jsou přidruženy k této sestavě.</span><span class="sxs-lookup"><span data-stu-id="c51c0-106">It also describes the building blocks that are associated with this report.</span></span> 

## <a name="default-income-statement-report"></a><span data-ttu-id="c51c0-107">Výchozí sestava výkazu příjmu</span><span class="sxs-lookup"><span data-stu-id="c51c0-107">Default income statement report</span></span>

| <span data-ttu-id="c51c0-108">Výchozí sestava</span><span class="sxs-lookup"><span data-stu-id="c51c0-108">Default report</span></span>             | <span data-ttu-id="c51c0-109">Jak funguje</span><span class="sxs-lookup"><span data-stu-id="c51c0-109">What it does</span></span>                                                                                              |
|----------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c51c0-110">Výkaz příjmu – výchozí</span><span class="sxs-lookup"><span data-stu-id="c51c0-110">Income Statement – Default</span></span> | <span data-ttu-id="c51c0-111">Umožňuje zobrazit ziskovost organizace za aktuální období a také od začátku roku.</span><span class="sxs-lookup"><span data-stu-id="c51c0-111">Provides a view of the organization’s profitability for the current period and also for the year to date.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="c51c0-112">Stavební bloky</span><span class="sxs-lookup"><span data-stu-id="c51c0-112">Building blocks</span></span>
<span data-ttu-id="c51c0-113">Finanční sestava výkazu příjmu používá následující stavební bloky.</span><span class="sxs-lookup"><span data-stu-id="c51c0-113">The income statement financial report uses the following building blocks.</span></span>

| <span data-ttu-id="c51c0-114">Výchozí sestava</span><span class="sxs-lookup"><span data-stu-id="c51c0-114">Default report</span></span>             | <span data-ttu-id="c51c0-115">Definice řádku</span><span class="sxs-lookup"><span data-stu-id="c51c0-115">Row definition</span></span>                     | <span data-ttu-id="c51c0-116">Definice sloupce</span><span class="sxs-lookup"><span data-stu-id="c51c0-116">Column definition</span></span>          |
|----------------------------|------------------------------------|----------------------------|
| <span data-ttu-id="c51c0-117">Výkaz příjmu – výchozí</span><span class="sxs-lookup"><span data-stu-id="c51c0-117">Income Statement - Default</span></span> | <span data-ttu-id="c51c0-118">Souhrnný výkazu příjmu – výchozí</span><span class="sxs-lookup"><span data-stu-id="c51c0-118">Summary Income Statement - Default</span></span> | <span data-ttu-id="c51c0-119">Periodický a od začátku roku – výchozí</span><span class="sxs-lookup"><span data-stu-id="c51c0-119">Periodic and YTD - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="c51c0-120">Definice řádku</span><span class="sxs-lookup"><span data-stu-id="c51c0-120">Row definition</span></span>

<span data-ttu-id="c51c0-121">Definice řádku Souhrnný výkazu příjmu – výchozí obsahuje oddíl pro každou část tradičního výkazu příjmu.</span><span class="sxs-lookup"><span data-stu-id="c51c0-121">The row definition, Summary Income Statement – Default, contains a section for each part of a traditional income statement.</span></span> <span data-ttu-id="c51c0-122">Dimenze kategorie hlavního účtu se používá k vytvoření této definice řádku.</span><span class="sxs-lookup"><span data-stu-id="c51c0-122">The Main Account Category dimension is used to build this row definition.</span></span> <span data-ttu-id="c51c0-123">Z toho vyplývá, že každý může generovat sestavu bez nutnosti provádět změny.</span><span class="sxs-lookup"><span data-stu-id="c51c0-123">Therefore, anyone can generate the report without having to make any modifications.</span></span>

### <a name="column-definition"></a><span data-ttu-id="c51c0-124">Definice sloupce</span><span class="sxs-lookup"><span data-stu-id="c51c0-124">Column Definition</span></span>

<span data-ttu-id="c51c0-125">Definice sloupců obsahují různé typy sloupců, které poskytují různé úrovně podrobností a finanční údaje.</span><span class="sxs-lookup"><span data-stu-id="c51c0-125">The column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="c51c0-126">**Periodický a od začátku roku – výchozí typy sloupce:**</span><span class="sxs-lookup"><span data-stu-id="c51c0-126">**Periodic and YTD – Default column types:**</span></span>
    -   <span data-ttu-id="c51c0-127">**DESC** – popis z definice řádku</span><span class="sxs-lookup"><span data-stu-id="c51c0-127">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="c51c0-128">**FD** – finanční údaje pro aktuální období</span><span class="sxs-lookup"><span data-stu-id="c51c0-128">**FD** – Financial data for the current period</span></span>
    -   <span data-ttu-id="c51c0-129">**FD** – finanční údaje od začátku roku</span><span class="sxs-lookup"><span data-stu-id="c51c0-129">**FD** – Financial data for the year to date</span></span>



## <a name="additional-resources"></a><span data-ttu-id="c51c0-130">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="c51c0-130">Additional resources</span></span>

[<span data-ttu-id="c51c0-131">Přehled finančního výkaznictví</span><span class="sxs-lookup"><span data-stu-id="c51c0-131">Financial reporting overview</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="c51c0-132">Zobrazení finančních sestav</span><span class="sxs-lookup"><span data-stu-id="c51c0-132">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="c51c0-133">Blog o finančním výkaznictví v Dynamics</span><span class="sxs-lookup"><span data-stu-id="c51c0-133">Dynamics Financial Reporting Blog</span></span>](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]