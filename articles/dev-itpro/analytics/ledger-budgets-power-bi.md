---
title: "Obsah Power BI pro porovnání skutečné situace s rozpočtem"
description: "Toto téma popisuje obsah Power BI pro porovnání skutečné situace s rozpočtem. Popisuje, jak získat přístup k sestavám, které jsou obsaženy v obsahu, a uvádí informace o datovém modelu a entitách, které se používají k vytváření obsahu."
author: ryansandness
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetTrackingWorkspace
audience: Application user, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 6a01d28d642ab3846c18955a1fced0dbabfb85d4
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---

# <a name="actual-vs-budget-power-bi-content"></a><span data-ttu-id="76d96-104">Obsah Power BI pro porovnání skutečné situace s rozpočtem</span><span class="sxs-lookup"><span data-stu-id="76d96-104">Actual vs budget Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="76d96-105">Toto téma popisuje obsah Microsoft Power BI **Skutečnost a rozpočet**.</span><span class="sxs-lookup"><span data-stu-id="76d96-105">This topic describes the **Actual vs budget** Microsoft Power BI content.</span></span> <span data-ttu-id="76d96-106">Vysvětluje přístup k sestavám Power BI a poskytuje informace o datovém modelu a entitách, které byly použity k sestavení obsahu.</span><span class="sxs-lookup"><span data-stu-id="76d96-106">It explains how to access the Power BI reports, and provides information about the data model and entities that were used to build the content.</span></span> 

## <a name="overview"></a><span data-ttu-id="76d96-107">Přehled</span><span class="sxs-lookup"><span data-stu-id="76d96-107">Overview</span></span>

<span data-ttu-id="76d96-108">Obsah Power BI **Skutečnost a rozpočet** byl vytvořen pro uživatele, kteří odpovídají za sledování a porovnávání skutečných výsledků s rozpočtem v rámci organizace.</span><span class="sxs-lookup"><span data-stu-id="76d96-108">The **Actual vs budget** Power BI content was created for individuals who are responsible for monitoring actual versus budget performance in their organization.</span></span> <span data-ttu-id="76d96-109">Obsah Power BI **Skutečnost a rozpočet** usnadňuje kontrolu odchylek rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="76d96-109">The **Actual vs budget** Power BI content provides visibility into your budget variances.</span></span> <span data-ttu-id="76d96-110">Můžete analyzovat rozpočet pro aktuální rok podle kategorie účtu, kódu rozpočtu, hlavního účtu, popisu hlavního účtu nebo fiskálního období a získat užitečné informace o příčinách odchylek.</span><span class="sxs-lookup"><span data-stu-id="76d96-110">You can analyze budget for the current year by account category, budget code, main account, main account descriptions, or fiscal period to get a better understanding of the cause of any variances.</span></span> 

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="76d96-111">Přístup k obsahu Power BI</span><span class="sxs-lookup"><span data-stu-id="76d96-111">Accessing the Power BI content</span></span>
<span data-ttu-id="76d96-112">Sestavy z obsahu Power BI **Skutečnost a rozpočet** se zobrazují v pracovních prostorech **Rozpočty hlavní knihy a prognózy** a **CFO**.</span><span class="sxs-lookup"><span data-stu-id="76d96-112">Reports from the **Actual vs budget** Power BI content are shown in the **Ledger budget and forecasts** and **CFO** workspaces.</span></span>

## <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="76d96-113">Sestavy, které jsou součástí obsahu Power BI</span><span class="sxs-lookup"><span data-stu-id="76d96-113">Reports that are included in the Power BI content</span></span>
<span data-ttu-id="76d96-114">Následující tabulka obsahuje podrobnosti o metrikách, které jsou k dispozici na každé stránce sestavy obsahu Power BI **Skutečnost a rozpočet**.</span><span class="sxs-lookup"><span data-stu-id="76d96-114">The following table provides details about the metrics that are found on each report page in the **Actual vs budget** Power BI content.</span></span>


|           <span data-ttu-id="76d96-115">Sestava</span><span class="sxs-lookup"><span data-stu-id="76d96-115">Report</span></span>            |                                       <span data-ttu-id="76d96-116">Metrika</span><span class="sxs-lookup"><span data-stu-id="76d96-116">Metrics</span></span>                                        |
|-----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="76d96-117">Výdaje - Skutečné a rozpočtové</span><span class="sxs-lookup"><span data-stu-id="76d96-117">Expenses - Actual vs budget</span></span> |  <ul><li><span data-ttu-id="76d96-118">Celkové výdaje za tento rok</span><span class="sxs-lookup"><span data-stu-id="76d96-118">Total expenses this year</span></span></li><li><span data-ttu-id="76d96-119">Celkové výdaje v rozpočtu za tento rok</span><span class="sxs-lookup"><span data-stu-id="76d96-119">Budget total expenses this year</span></span></li></ul>  |
| <span data-ttu-id="76d96-120">Výnosy - Skutečné a rozpočtové</span><span class="sxs-lookup"><span data-stu-id="76d96-120">Revenue - Actual vs budget</span></span>  |   <ul><li><span data-ttu-id="76d96-121">Celkové výnosy za tento rok</span><span class="sxs-lookup"><span data-stu-id="76d96-121">Total revenue this year</span></span></li><li><span data-ttu-id="76d96-122">Celkové výnosy v rozpočtu za tento rok</span><span class="sxs-lookup"><span data-stu-id="76d96-122">Budget total revenue this year</span></span></li><ul>    |
|           <span data-ttu-id="76d96-123">Výdaj</span><span class="sxs-lookup"><span data-stu-id="76d96-123">Expense</span></span>           | <ul><li><span data-ttu-id="76d96-124">Celkové výdaje za tento rok</span><span class="sxs-lookup"><span data-stu-id="76d96-124">Total expenses this year</span></span></li><li><span data-ttu-id="76d96-125">Cílová výše výdajů podle rozpočtu</span><span class="sxs-lookup"><span data-stu-id="76d96-125">Goal for expenses based on budget</span></span> </li><ul> |
|           <span data-ttu-id="76d96-126">Výnosy</span><span class="sxs-lookup"><span data-stu-id="76d96-126">Revenue</span></span>           |  <ul><li><span data-ttu-id="76d96-127">Celkové výnosy za tento rok</span><span class="sxs-lookup"><span data-stu-id="76d96-127">Total revenue this year</span></span></li><li><span data-ttu-id="76d96-128">Cílová výše výnosů podle rozpočtu</span><span class="sxs-lookup"><span data-stu-id="76d96-128">Goal for revenue based on budget</span></span> </li><ul>  |
|         <span data-ttu-id="76d96-129">Čistý příjem</span><span class="sxs-lookup"><span data-stu-id="76d96-129">Net income</span></span>          |  <ul><li><span data-ttu-id="76d96-130">Čistý příjem za tento rok</span><span class="sxs-lookup"><span data-stu-id="76d96-130">Net income this year</span></span></li><li><span data-ttu-id="76d96-131">Cílová výše čistého příjmu podle rozpočtu</span><span class="sxs-lookup"><span data-stu-id="76d96-131">Goal for net income based on budget</span></span> </li><ul>  |

## <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="76d96-132">Informace o datovém modelu a entitách</span><span class="sxs-lookup"><span data-stu-id="76d96-132">Understanding the data model and entities</span></span>

|          <span data-ttu-id="76d96-133">Celek</span><span class="sxs-lookup"><span data-stu-id="76d96-133">Entity</span></span>           |                                     <span data-ttu-id="76d96-134">Obsah</span><span class="sxs-lookup"><span data-stu-id="76d96-134">Contents</span></span>                                     |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="76d96-135">Aktivity hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="76d96-135">General Ledger Activities</span></span> |                    <span data-ttu-id="76d96-136">Částky transakcí pro hlavní knihu</span><span class="sxs-lookup"><span data-stu-id="76d96-136">Transaction amounts for the general ledger</span></span>                    |
|     <span data-ttu-id="76d96-137">Aktivity rozpočtu</span><span class="sxs-lookup"><span data-stu-id="76d96-137">Budget Activities</span></span>     |                   <span data-ttu-id="76d96-138">Částky transakcí pro registr rozpočtu</span><span class="sxs-lookup"><span data-stu-id="76d96-138">Transaction amounts for the budget register</span></span>                    |
|       <span data-ttu-id="76d96-139">Hlavní účty</span><span class="sxs-lookup"><span data-stu-id="76d96-139">Main Accounts</span></span>       |                        <span data-ttu-id="76d96-140">Hlavní účty pro filtrování sestav</span><span class="sxs-lookup"><span data-stu-id="76d96-140">Main accounts to filter reports by</span></span>                        |
|     <span data-ttu-id="76d96-141">Fiskální kalendáře</span><span class="sxs-lookup"><span data-stu-id="76d96-141">Fiscal Calendars</span></span>      |                      <span data-ttu-id="76d96-142">Fiskální kalendáře pro filtrování sestav</span><span class="sxs-lookup"><span data-stu-id="76d96-142">Fiscal calendars to filter reports by</span></span>                       |
|          <span data-ttu-id="76d96-143">Hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="76d96-143">Ledgers</span></span>          |       <span data-ttu-id="76d96-144">Hlavní knihy, které lze použít k filtrování sestavy u aktuální hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="76d96-144">Ledgers that can be used to filter the report to the current ledger</span></span>        |
|       <span data-ttu-id="76d96-145">Kódy rozpočtu</span><span class="sxs-lookup"><span data-stu-id="76d96-145">Budget Codes</span></span>        |                        <span data-ttu-id="76d96-146">Kódy rozpočtu pro filtrování sestav</span><span class="sxs-lookup"><span data-stu-id="76d96-146">Budget codes to filter reports by</span></span>                         |
|      <span data-ttu-id="76d96-147">Právnické osoby</span><span class="sxs-lookup"><span data-stu-id="76d96-147">Legal Entities</span></span>       | <span data-ttu-id="76d96-148">Právnické osoby, které lze použít k filtrování sestavy u aktuální právnické osoby</span><span class="sxs-lookup"><span data-stu-id="76d96-148">Legal entities that can be used to filter the report to the current legal entity</span></span> |


