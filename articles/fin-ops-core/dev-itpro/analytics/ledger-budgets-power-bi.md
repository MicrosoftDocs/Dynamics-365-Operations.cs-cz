---
title: Obsah porovnání skutečnosti a rozpočtu v Power BI
description: Toto téma popisuje obsah Power BI pro porovnání skutečné situace s rozpočtem. Vysvětluje, jak přistupovat k sestavám, a poskytuje informace o datovém modelu.
author: panolte
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BudgetTrackingWorkspace
audience: Application user, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: f3e2f62b666559ba9a356e4948c2033da9cc95d5
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568566"
---
# <a name="actual-vs-budget-power-bi-content"></a><span data-ttu-id="115ff-104">Obsah porovnání skutečnosti a rozpočtu v Power BI</span><span class="sxs-lookup"><span data-stu-id="115ff-104">Actual vs budget Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="115ff-105">Toto téma popisuje obsah **pro porovnání skutečné situace s rozpočtem** v Microsoft Power BI.</span><span class="sxs-lookup"><span data-stu-id="115ff-105">This topic describes the **Actual vs budget** Microsoft Power BI content.</span></span> <span data-ttu-id="115ff-106">Vysvětluje přístup k sestavám Power BI a poskytuje informace o datovém modelu a entitách, které byly použity k sestavení obsahu.</span><span class="sxs-lookup"><span data-stu-id="115ff-106">It explains how to access the Power BI reports, and provides information about the data model and entities that were used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="115ff-107">Přehled</span><span class="sxs-lookup"><span data-stu-id="115ff-107">Overview</span></span>

<span data-ttu-id="115ff-108">Obsah **skutečnost a rozpočet** v Power BI byl vytvořen pro uživatele, kteří odpovídají za sledování a porovnávání skutečných výsledků s rozpočtem v rámci organizace.</span><span class="sxs-lookup"><span data-stu-id="115ff-108">The **Actual vs budget** Power BI content was created for individuals who are responsible for monitoring actual versus budget performance in their organization.</span></span> <span data-ttu-id="115ff-109">Obsah **Skutečnost a rozpočet** v Power BI usnadňuje kontrolu odchylek rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="115ff-109">The **Actual vs budget** Power BI content provides visibility into your budget variances.</span></span> <span data-ttu-id="115ff-110">Můžete analyzovat rozpočet pro aktuální rok podle kategorie účtu, kódu rozpočtu, hlavního účtu, popisu hlavního účtu nebo fiskálního období a získat užitečné informace o příčinách odchylek.</span><span class="sxs-lookup"><span data-stu-id="115ff-110">You can analyze budget for the current year by account category, budget code, main account, main account descriptions, or fiscal period to get a better understanding of the cause of any variances.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="115ff-111">Přístup k obsahu Power BI</span><span class="sxs-lookup"><span data-stu-id="115ff-111">Accessing the Power BI content</span></span>
<span data-ttu-id="115ff-112">Sestavy z obsahu **Skutečnost a rozpočet** v Power BI se zobrazují v pracovních prostorech **Rozpočty hlavní knihy a prognózy** a **CFO**.</span><span class="sxs-lookup"><span data-stu-id="115ff-112">Reports from the **Actual vs budget** Power BI content are shown in the **Ledger budget and forecasts** and **CFO** workspaces.</span></span>

## <a name="reports-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="115ff-113">Sestavy, které jsou součástí obsahu Power BI</span><span class="sxs-lookup"><span data-stu-id="115ff-113">Reports that are included in the Power BI content</span></span>
<span data-ttu-id="115ff-114">Následující tabulka obsahuje podrobnosti o metrikách, které jsou k dispozici na každé stránce sestavy obsahu **Skutečnost a rozpočet** v Power BI.</span><span class="sxs-lookup"><span data-stu-id="115ff-114">The following table provides details about the metrics that are found on each report page in the **Actual vs budget** Power BI content.</span></span>

| <span data-ttu-id="115ff-115">Sestava</span><span class="sxs-lookup"><span data-stu-id="115ff-115">Report</span></span>                      | <span data-ttu-id="115ff-116">Metrika</span><span class="sxs-lookup"><span data-stu-id="115ff-116">Metrics</span></span>                                                                             |
|-----------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="115ff-117">Výdaje - Skutečné a rozpočtové</span><span class="sxs-lookup"><span data-stu-id="115ff-117">Expenses - Actual vs budget</span></span> | <ul><li><span data-ttu-id="115ff-118">Celkové výdaje za tento rok</span><span class="sxs-lookup"><span data-stu-id="115ff-118">Total expenses this year</span></span></li><li><span data-ttu-id="115ff-119">Celkové výdaje v rozpočtu za tento rok</span><span class="sxs-lookup"><span data-stu-id="115ff-119">Budget total expenses this year</span></span></li></ul>  |
| <span data-ttu-id="115ff-120">Výnosy - Skutečné a rozpočtové</span><span class="sxs-lookup"><span data-stu-id="115ff-120">Revenue - Actual vs budget</span></span>  | <ul><li><span data-ttu-id="115ff-121">Celkové výnosy za tento rok</span><span class="sxs-lookup"><span data-stu-id="115ff-121">Total revenue this year</span></span></li><li><span data-ttu-id="115ff-122">Celkové výnosy v rozpočtu za tento rok</span><span class="sxs-lookup"><span data-stu-id="115ff-122">Budget total revenue this year</span></span></li><ul>     |
| <span data-ttu-id="115ff-123">Výdaj</span><span class="sxs-lookup"><span data-stu-id="115ff-123">Expense</span></span>                     | <ul><li><span data-ttu-id="115ff-124">Celkové výdaje za tento rok</span><span class="sxs-lookup"><span data-stu-id="115ff-124">Total expenses this year</span></span></li><li><span data-ttu-id="115ff-125">Cílová výše výdajů podle rozpočtu</span><span class="sxs-lookup"><span data-stu-id="115ff-125">Goal for expenses based on budget</span></span></li><ul> |
| <span data-ttu-id="115ff-126">Výnosy</span><span class="sxs-lookup"><span data-stu-id="115ff-126">Revenue</span></span>                     | <ul><li><span data-ttu-id="115ff-127">Celkové výnosy za tento rok</span><span class="sxs-lookup"><span data-stu-id="115ff-127">Total revenue this year</span></span></li><li><span data-ttu-id="115ff-128">Cílová výše výnosů podle rozpočtu</span><span class="sxs-lookup"><span data-stu-id="115ff-128">Goal for revenue based on budget</span></span></li><ul>   |
| <span data-ttu-id="115ff-129">Čistý příjem</span><span class="sxs-lookup"><span data-stu-id="115ff-129">Net income</span></span>                  | <ul><li><span data-ttu-id="115ff-130">Čistý příjem za tento rok</span><span class="sxs-lookup"><span data-stu-id="115ff-130">Net income this year</span></span></li><li><span data-ttu-id="115ff-131">Cílová výše čistého příjmu podle rozpočtu</span><span class="sxs-lookup"><span data-stu-id="115ff-131">Goal for net income based on budget</span></span></li><ul>   |

## <a name="understanding-the-data-model-and-entities"></a><span data-ttu-id="115ff-132">Informace o datovém modelu a entitách</span><span class="sxs-lookup"><span data-stu-id="115ff-132">Understanding the data model and entities</span></span>

| <span data-ttu-id="115ff-133">Celek</span><span class="sxs-lookup"><span data-stu-id="115ff-133">Entity</span></span>                    | <span data-ttu-id="115ff-134">Obsah</span><span class="sxs-lookup"><span data-stu-id="115ff-134">Contents</span></span>                                                                         |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="115ff-135">Aktivity hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="115ff-135">General Ledger Activities</span></span> | <span data-ttu-id="115ff-136">Částky transakcí pro hlavní knihu</span><span class="sxs-lookup"><span data-stu-id="115ff-136">Transaction amounts for the general ledger</span></span>                                       |
| <span data-ttu-id="115ff-137">Aktivity rozpočtu</span><span class="sxs-lookup"><span data-stu-id="115ff-137">Budget Activities</span></span>         | <span data-ttu-id="115ff-138">Částky transakcí pro registr rozpočtu</span><span class="sxs-lookup"><span data-stu-id="115ff-138">Transaction amounts for the budget register</span></span>                                      |
| <span data-ttu-id="115ff-139">Hlavní účty</span><span class="sxs-lookup"><span data-stu-id="115ff-139">Main Accounts</span></span>             | <span data-ttu-id="115ff-140">Hlavní účty pro filtrování sestav</span><span class="sxs-lookup"><span data-stu-id="115ff-140">Main accounts to filter reports by</span></span>                                               |
| <span data-ttu-id="115ff-141">Fiskální kalendáře</span><span class="sxs-lookup"><span data-stu-id="115ff-141">Fiscal Calendars</span></span>          | <span data-ttu-id="115ff-142">Fiskální kalendáře pro filtrování sestav</span><span class="sxs-lookup"><span data-stu-id="115ff-142">Fiscal calendars to filter reports by</span></span>                                            |
| <span data-ttu-id="115ff-143">Hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="115ff-143">Ledgers</span></span>                   | <span data-ttu-id="115ff-144">Hlavní knihy, které lze použít k filtrování sestavy u aktuální hlavní knihy</span><span class="sxs-lookup"><span data-stu-id="115ff-144">Ledgers that can be used to filter the report to the current ledger</span></span>              |
| <span data-ttu-id="115ff-145">Kódy rozpočtu</span><span class="sxs-lookup"><span data-stu-id="115ff-145">Budget Codes</span></span>              | <span data-ttu-id="115ff-146">Kódy rozpočtu pro filtrování sestav</span><span class="sxs-lookup"><span data-stu-id="115ff-146">Budget codes to filter reports by</span></span>                                                |
| <span data-ttu-id="115ff-147">Právnické osoby</span><span class="sxs-lookup"><span data-stu-id="115ff-147">Legal Entities</span></span>            | <span data-ttu-id="115ff-148">Právnické osoby, které lze použít k filtrování sestavy u aktuální právnické osoby</span><span class="sxs-lookup"><span data-stu-id="115ff-148">Legal entities that can be used to filter the report to the current legal entity</span></span> |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]