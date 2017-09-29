---
title: "Finanční sestavy rozvah"
description: "Tento článek popisuje výchozí sestavy pro rozvahy. Popisuje také stavební bloky, které jsou přidruženy k těmto sestavám."
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 12274
ms.assetid: 52f78229-f531-4d16-b337-e2628994acb6
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6323a2bf40a853edff4b3cef31eea7e95542a92e
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---

# <a name="balance-sheet-financial-reports"></a><span data-ttu-id="5840a-104">Finanční sestavy rozvah</span><span class="sxs-lookup"><span data-stu-id="5840a-104">Balance sheet financial reports</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="5840a-105">Tento článek popisuje výchozí sestavy pro rozvahy.</span><span class="sxs-lookup"><span data-stu-id="5840a-105">This article describes the default reports for balance sheets.</span></span> <span data-ttu-id="5840a-106">Popisuje také stavební bloky, které jsou přidruženy k těmto sestavám.</span><span class="sxs-lookup"><span data-stu-id="5840a-106">It also describes the building blocks that are associated with these reports.</span></span> 

<a name="default-balance-sheet-reports"></a><span data-ttu-id="5840a-107">Výchozí finanční sestavy rozvah</span><span class="sxs-lookup"><span data-stu-id="5840a-107">Default balance sheet reports</span></span>
-----------------------------

<span data-ttu-id="5840a-108">Existují dvě výchozí finanční sestavy rozvah.</span><span class="sxs-lookup"><span data-stu-id="5840a-108">There are two default balance sheet reports.</span></span> <span data-ttu-id="5840a-109">V jedné sestavě jsou oddíly nad sebou.</span><span class="sxs-lookup"><span data-stu-id="5840a-109">On one report, the sections are stacked.</span></span> <span data-ttu-id="5840a-110">Ve druhé jsou oddíly vedle sebe.</span><span class="sxs-lookup"><span data-stu-id="5840a-110">On the other report, the sections are side by side.</span></span>

| <span data-ttu-id="5840a-111">Výchozí sestava</span><span class="sxs-lookup"><span data-stu-id="5840a-111">Default report</span></span>                       | <span data-ttu-id="5840a-112">Jak funguje</span><span class="sxs-lookup"><span data-stu-id="5840a-112">What it does</span></span>                                                                                                                           |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5840a-113">Rozvaha – výchozí</span><span class="sxs-lookup"><span data-stu-id="5840a-113">Balance Sheet – Default</span></span>              | <span data-ttu-id="5840a-114">Poskytuje přehled finanční pozice organizace pro rok.</span><span class="sxs-lookup"><span data-stu-id="5840a-114">Provides a view of the organization's financial position for the year.</span></span>                                                                 |
| <span data-ttu-id="5840a-115">Rozvaha vedle sebe – výchozí</span><span class="sxs-lookup"><span data-stu-id="5840a-115">Side by Side Balance Sheet – Default</span></span> | <span data-ttu-id="5840a-116">Poskytuje přehled finanční pozice organizace pro rok.</span><span class="sxs-lookup"><span data-stu-id="5840a-116">Provides a view of the organization's financial position for the year.</span></span> <span data-ttu-id="5840a-117">Aktiva a pasiva a jmění akcionářů jsou vedle sebe.</span><span class="sxs-lookup"><span data-stu-id="5840a-117">Assets and liability and shareholder’s equity are side by side.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="5840a-118">Stavební bloky</span><span class="sxs-lookup"><span data-stu-id="5840a-118">Building blocks</span></span>
<span data-ttu-id="5840a-119">Finanční sestavy rozvahy používají následující stavební bloky.</span><span class="sxs-lookup"><span data-stu-id="5840a-119">The balance sheet financial reports use the following building blocks.</span></span>

| <span data-ttu-id="5840a-120">Výchozí sestava</span><span class="sxs-lookup"><span data-stu-id="5840a-120">Default report</span></span>                       | <span data-ttu-id="5840a-121">Definice řádku</span><span class="sxs-lookup"><span data-stu-id="5840a-121">Row definition</span></span>                       | <span data-ttu-id="5840a-122">Definice sloupce</span><span class="sxs-lookup"><span data-stu-id="5840a-122">Column definition</span></span>             |
|--------------------------------------|--------------------------------------|-------------------------------|
| <span data-ttu-id="5840a-123">Rozvaha – výchozí</span><span class="sxs-lookup"><span data-stu-id="5840a-123">Balance Sheet - Default</span></span>              | <span data-ttu-id="5840a-124">Rozvaha – výchozí</span><span class="sxs-lookup"><span data-stu-id="5840a-124">Balance Sheet - Default</span></span>              | <span data-ttu-id="5840a-125">Od začátku roku a odchylka – výchozí</span><span class="sxs-lookup"><span data-stu-id="5840a-125">YTD and Variance - Default</span></span>    |
| <span data-ttu-id="5840a-126">Rozvaha vedle sebe – výchozí</span><span class="sxs-lookup"><span data-stu-id="5840a-126">Side by Side Balance Sheet – Default</span></span> | <span data-ttu-id="5840a-127">Rozvaha vedle sebe – výchozí</span><span class="sxs-lookup"><span data-stu-id="5840a-127">Side by Side Balance Sheet – Default</span></span> | <span data-ttu-id="5840a-128">Sloupec od začátku roku – výchozí</span><span class="sxs-lookup"><span data-stu-id="5840a-128">Year to Date Column - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="5840a-129">Definice řádku</span><span class="sxs-lookup"><span data-stu-id="5840a-129">Row definition</span></span>

<span data-ttu-id="5840a-130">Definice řádku pro obě sestavy rozvahy obsahují oddíly pro každou součást tradiční rozvahy.</span><span class="sxs-lookup"><span data-stu-id="5840a-130">The row definitions for both balance sheet reports contain sections for each part of a traditional balance sheet.</span></span> <span data-ttu-id="5840a-131">Sestava vedle sebe obsahuje zalomení sloupce, takže odpovědnosti a vlastní jmění společnosti se zobrazují vedle majetku.</span><span class="sxs-lookup"><span data-stu-id="5840a-131">The side-by-side report includes a column break, so that liability and the owner’s equity appear next to assets.</span></span> <span data-ttu-id="5840a-132">Dimenze kategorie hlavního účtu se používá k vytvoření obou definic řádku.</span><span class="sxs-lookup"><span data-stu-id="5840a-132">The Main Account Category dimension is used to build both row definitions.</span></span> <span data-ttu-id="5840a-133">Z toho vyplývá, že každý může generovat sestavy bez nutnosti provádět změny.</span><span class="sxs-lookup"><span data-stu-id="5840a-133">Therefore, anyone can generate the reports without having to make any modifications.</span></span>

### <a name="column-definition"></a><span data-ttu-id="5840a-134">Definice sloupce</span><span class="sxs-lookup"><span data-stu-id="5840a-134">Column definition</span></span>

<span data-ttu-id="5840a-135">Definice sloupců obsahují různé typy sloupců, které poskytují různé úrovně podrobností a finanční údaje.</span><span class="sxs-lookup"><span data-stu-id="5840a-135">The column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="5840a-136">**Od začátku roku a odchylka – výchozí typy sloupce:**</span><span class="sxs-lookup"><span data-stu-id="5840a-136">**YTD and Variance – Default column types:**</span></span>
    -   <span data-ttu-id="5840a-137">**DESC** – popis z definice řádku</span><span class="sxs-lookup"><span data-stu-id="5840a-137">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="5840a-138">**FD** – Finanční data od začátku roku pro aktuální rok</span><span class="sxs-lookup"><span data-stu-id="5840a-138">**FD** – Year-to-date financial data for the current year</span></span>
    -   <span data-ttu-id="5840a-139">**FD** – Finanční data od začátku roku pro minulý rok</span><span class="sxs-lookup"><span data-stu-id="5840a-139">**FD** – Year-to-date financial data for the last year</span></span>
    -   <span data-ttu-id="5840a-140">**CALC** – odchylky od odečtení minulého roku z tohoto roku</span><span class="sxs-lookup"><span data-stu-id="5840a-140">**CALC** – The variance from subtracting last year from this year</span></span>

<!-- -->

-   <span data-ttu-id="5840a-141">**Sloupec od začátku roku – výchozí:**</span><span class="sxs-lookup"><span data-stu-id="5840a-141">**Year to Date Column – Default:**</span></span>
    -   <span data-ttu-id="5840a-142">**DESC** – popis z definice řádku</span><span class="sxs-lookup"><span data-stu-id="5840a-142">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="5840a-143">**FD** – Finanční data od začátku roku pro aktuální rok</span><span class="sxs-lookup"><span data-stu-id="5840a-143">**FD** – Year-to-date financial data for the current year</span></span>

 

<a name="see-also"></a><span data-ttu-id="5840a-144">Viz také</span><span class="sxs-lookup"><span data-stu-id="5840a-144">See also</span></span>
--------

[<span data-ttu-id="5840a-145">Finanční výkaznictví</span><span class="sxs-lookup"><span data-stu-id="5840a-145">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="5840a-146">Zobrazit finanční sestavy</span><span class="sxs-lookup"><span data-stu-id="5840a-146">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="5840a-147">Blog o finančním výkaznictví v Dynamics</span><span class="sxs-lookup"><span data-stu-id="5840a-147">Dynamics Financial Reporting Blog</span></span>](http://blogs.msdn.com/b/dynamics_financial_reporting/)




