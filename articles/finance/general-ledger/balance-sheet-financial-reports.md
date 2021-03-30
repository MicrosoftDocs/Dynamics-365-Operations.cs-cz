---
title: Finanční sestavy rozvah
description: Tento článek popisuje výchozí sestavy pro rozvahy. Popisuje také stavební bloky, které jsou přidruženy k těmto sestavám.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FinanicalReports
audience: Application User
ms.reviewer: roschlom
ms.custom: 12274
ms.assetid: 52f78229-f531-4d16-b337-e2628994acb6
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bcfb8e8fd28224ac9fe9a4919f4252dcd01ce360
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5212390"
---
# <a name="balance-sheet-financial-reports"></a><span data-ttu-id="549d1-104">Finanční sestavy rozvah</span><span class="sxs-lookup"><span data-stu-id="549d1-104">Balance sheet financial reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="549d1-105">Tento článek popisuje výchozí sestavy pro rozvahy.</span><span class="sxs-lookup"><span data-stu-id="549d1-105">This article describes the default reports for balance sheets.</span></span> <span data-ttu-id="549d1-106">Popisuje také stavební bloky, které jsou přidruženy k těmto sestavám.</span><span class="sxs-lookup"><span data-stu-id="549d1-106">It also describes the building blocks that are associated with these reports.</span></span> 

<a name="default-balance-sheet-reports"></a><span data-ttu-id="549d1-107">Výchozí finanční sestavy rozvah</span><span class="sxs-lookup"><span data-stu-id="549d1-107">Default balance sheet reports</span></span>
-----------------------------

<span data-ttu-id="549d1-108">Existují dvě výchozí finanční sestavy rozvah.</span><span class="sxs-lookup"><span data-stu-id="549d1-108">There are two default balance sheet reports.</span></span> <span data-ttu-id="549d1-109">V jedné sestavě jsou oddíly nad sebou.</span><span class="sxs-lookup"><span data-stu-id="549d1-109">On one report, the sections are stacked.</span></span> <span data-ttu-id="549d1-110">Ve druhé jsou oddíly vedle sebe.</span><span class="sxs-lookup"><span data-stu-id="549d1-110">On the other report, the sections are side by side.</span></span>

| <span data-ttu-id="549d1-111">Výchozí sestava</span><span class="sxs-lookup"><span data-stu-id="549d1-111">Default report</span></span>                       | <span data-ttu-id="549d1-112">Jak funguje</span><span class="sxs-lookup"><span data-stu-id="549d1-112">What it does</span></span>                                                                                                                           |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="549d1-113">Rozvaha – výchozí</span><span class="sxs-lookup"><span data-stu-id="549d1-113">Balance Sheet – Default</span></span>              | <span data-ttu-id="549d1-114">Poskytuje přehled finanční pozice organizace pro rok.</span><span class="sxs-lookup"><span data-stu-id="549d1-114">Provides a view of the organization's financial position for the year.</span></span>                                                                 |
| <span data-ttu-id="549d1-115">Rozvaha vedle sebe – výchozí</span><span class="sxs-lookup"><span data-stu-id="549d1-115">Side by Side Balance Sheet – Default</span></span> | <span data-ttu-id="549d1-116">Poskytuje přehled finanční pozice organizace pro rok.</span><span class="sxs-lookup"><span data-stu-id="549d1-116">Provides a view of the organization's financial position for the year.</span></span> <span data-ttu-id="549d1-117">Aktiva a pasiva a jmění akcionářů jsou vedle sebe.</span><span class="sxs-lookup"><span data-stu-id="549d1-117">Assets and liability and shareholder’s equity are side by side.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="549d1-118">Stavební bloky</span><span class="sxs-lookup"><span data-stu-id="549d1-118">Building blocks</span></span>
<span data-ttu-id="549d1-119">Finanční sestavy rozvahy používají následující stavební bloky.</span><span class="sxs-lookup"><span data-stu-id="549d1-119">The balance sheet financial reports use the following building blocks.</span></span>

| <span data-ttu-id="549d1-120">Výchozí sestava</span><span class="sxs-lookup"><span data-stu-id="549d1-120">Default report</span></span>                       | <span data-ttu-id="549d1-121">Definice řádku</span><span class="sxs-lookup"><span data-stu-id="549d1-121">Row definition</span></span>                       | <span data-ttu-id="549d1-122">Definice sloupce</span><span class="sxs-lookup"><span data-stu-id="549d1-122">Column definition</span></span>             |
|--------------------------------------|--------------------------------------|-------------------------------|
| <span data-ttu-id="549d1-123">Rozvaha – výchozí</span><span class="sxs-lookup"><span data-stu-id="549d1-123">Balance Sheet - Default</span></span>              | <span data-ttu-id="549d1-124">Rozvaha – výchozí</span><span class="sxs-lookup"><span data-stu-id="549d1-124">Balance Sheet - Default</span></span>              | <span data-ttu-id="549d1-125">Od začátku roku a odchylka – výchozí</span><span class="sxs-lookup"><span data-stu-id="549d1-125">YTD and Variance - Default</span></span>    |
| <span data-ttu-id="549d1-126">Rozvaha vedle sebe – výchozí</span><span class="sxs-lookup"><span data-stu-id="549d1-126">Side by Side Balance Sheet – Default</span></span> | <span data-ttu-id="549d1-127">Rozvaha vedle sebe – výchozí</span><span class="sxs-lookup"><span data-stu-id="549d1-127">Side by Side Balance Sheet – Default</span></span> | <span data-ttu-id="549d1-128">Sloupec od začátku roku – výchozí</span><span class="sxs-lookup"><span data-stu-id="549d1-128">Year to Date Column - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="549d1-129">Definice řádku</span><span class="sxs-lookup"><span data-stu-id="549d1-129">Row definition</span></span>

<span data-ttu-id="549d1-130">Definice řádku pro obě sestavy rozvahy obsahují oddíly pro každou součást tradiční rozvahy.</span><span class="sxs-lookup"><span data-stu-id="549d1-130">The row definitions for both balance sheet reports contain sections for each part of a traditional balance sheet.</span></span> <span data-ttu-id="549d1-131">Sestava vedle sebe obsahuje zalomení sloupce, takže odpovědnosti a vlastní jmění společnosti se zobrazují vedle majetku.</span><span class="sxs-lookup"><span data-stu-id="549d1-131">The side-by-side report includes a column break, so that liability and the owner’s equity appear next to assets.</span></span> <span data-ttu-id="549d1-132">Dimenze kategorie hlavního účtu se používá k vytvoření obou definic řádku.</span><span class="sxs-lookup"><span data-stu-id="549d1-132">The Main Account Category dimension is used to build both row definitions.</span></span> <span data-ttu-id="549d1-133">Z toho vyplývá, že každý může generovat sestavy bez nutnosti provádět změny.</span><span class="sxs-lookup"><span data-stu-id="549d1-133">Therefore, anyone can generate the reports without having to make any modifications.</span></span>

### <a name="column-definition"></a><span data-ttu-id="549d1-134">Definice sloupce</span><span class="sxs-lookup"><span data-stu-id="549d1-134">Column definition</span></span>

<span data-ttu-id="549d1-135">Definice sloupců obsahují různé typy sloupců, které poskytují různé úrovně podrobností a finanční údaje.</span><span class="sxs-lookup"><span data-stu-id="549d1-135">The column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="549d1-136">**Od začátku roku a odchylka – výchozí typy sloupce:**</span><span class="sxs-lookup"><span data-stu-id="549d1-136">**YTD and Variance – Default column types:**</span></span>
    -   <span data-ttu-id="549d1-137">**DESC** – popis z definice řádku</span><span class="sxs-lookup"><span data-stu-id="549d1-137">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="549d1-138">**FD** – Finanční data od začátku roku pro aktuální rok</span><span class="sxs-lookup"><span data-stu-id="549d1-138">**FD** – Year-to-date financial data for the current year</span></span>
    -   <span data-ttu-id="549d1-139">**FD** – Finanční data od začátku roku pro minulý rok</span><span class="sxs-lookup"><span data-stu-id="549d1-139">**FD** – Year-to-date financial data for the last year</span></span>
    -   <span data-ttu-id="549d1-140">**CALC** – odchylky od odečtení minulého roku z tohoto roku</span><span class="sxs-lookup"><span data-stu-id="549d1-140">**CALC** – The variance from subtracting last year from this year</span></span>

<!-- -->

-   <span data-ttu-id="549d1-141">**Sloupec od začátku roku – výchozí:**</span><span class="sxs-lookup"><span data-stu-id="549d1-141">**Year to Date Column – Default:**</span></span>
    -   <span data-ttu-id="549d1-142">**DESC** – popis z definice řádku</span><span class="sxs-lookup"><span data-stu-id="549d1-142">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="549d1-143">**FD** – Finanční data od začátku roku pro aktuální rok</span><span class="sxs-lookup"><span data-stu-id="549d1-143">**FD** – Year-to-date financial data for the current year</span></span>



<a name="additional-resources"></a><span data-ttu-id="549d1-144">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="549d1-144">Additional resources</span></span>
--------

[<span data-ttu-id="549d1-145">Přehled finančního výkaznictví</span><span class="sxs-lookup"><span data-stu-id="549d1-145">Financial reporting overview</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="549d1-146">Zobrazení finančních sestav</span><span class="sxs-lookup"><span data-stu-id="549d1-146">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="549d1-147">Blog o finančním výkaznictví v Dynamics</span><span class="sxs-lookup"><span data-stu-id="549d1-147">Dynamics Financial Reporting Blog</span></span>](https://blogs.msdn.com/b/dynamics_financial_reporting/)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]