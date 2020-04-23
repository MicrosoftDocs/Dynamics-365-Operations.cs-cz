---
title: Přehled servisních úloh
description: Servisní úlohy lze použít k popisu úloh, které mají být dokončeny v průběhu servisní zakázky. Tyto informace mohou vidět technici a zákazníci.
author: ShylaThompson
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceTask
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c2864b481c67c078df73436d752069a6b6c78640
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206028"
---
# <a name="service-tasks-overview"></a><span data-ttu-id="0c865-104">Přehled servisních úloh</span><span class="sxs-lookup"><span data-stu-id="0c865-104">Service tasks overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0c865-105">Servisní úlohy lze použít k popisu úloh, které mají být dokončeny v průběhu servisní zakázky.</span><span class="sxs-lookup"><span data-stu-id="0c865-105">Use service tasks to describe the task to be completed during a service order.</span></span>
<span data-ttu-id="0c865-106">Tyto informace mohou vidět technici a zákazníci.</span><span class="sxs-lookup"><span data-stu-id="0c865-106">Both technicians and customers can see this information.</span></span>

<span data-ttu-id="0c865-107">K vytváření servisních úloh slouží stránka **Servisní úlohy** lze přidružit k určité servisní smlouvě nebo servisní zakázce pomocí vztahů servisních úloh.</span><span class="sxs-lookup"><span data-stu-id="0c865-107">You create service tasks in the **Service tasks** page, and you associate service tasks with a specific service agreement or service order by creating service task relations.</span></span> <span data-ttu-id="0c865-108">Při vytváření vztahu servisní úlohy můžete vytvořit:</span><span class="sxs-lookup"><span data-stu-id="0c865-108">Every time that you create a service task relation, you can create the following:</span></span>

-  <span data-ttu-id="0c865-109">interní poznámky k úloze, například podrobné technické požadavky, o nichž by měli vědět technici;</span><span class="sxs-lookup"><span data-stu-id="0c865-109">Internal notes for the task, such as detailed technical requests for the task that are important for the technician to know.</span></span>

-  <span data-ttu-id="0c865-110">externí poznámky, které mohou vidět zákazníci.</span><span class="sxs-lookup"><span data-stu-id="0c865-110">External notes that the customer can see.</span></span> <span data-ttu-id="0c865-111">Zde je možné uvést méně technické vysvětlení prováděné úlohy v závislosti na smlouvě mezi zákazníkem a servisní společností.</span><span class="sxs-lookup"><span data-stu-id="0c865-111">These might provide a less technical explanation of the task that is being completed, according to the agreement between the customer and the service company.</span></span>

<span data-ttu-id="0c865-112">Když vytvoříte vztah servisní úlohy mezi servisní úlohou a servisní zakázkou nebo servisní smlouvou, můžete tuto servisní úlohu zadat při vytváření řádků servisní zakázky nebo servisní smlouvy pro aktuální servisní zakázku či smlouvu.</span><span class="sxs-lookup"><span data-stu-id="0c865-112">When you have set up a service task relation between a service task and a service order or service agreement, you can specify this service task when you create service order lines or service agreement lines for the current service order or service agreement.</span></span>

<span data-ttu-id="0c865-113">Pokud na základě servisní smlouvy generujete servisní zakázky, můžete použít servisní úlohy přiřazené k jednotlivým řádkům servisní smlouvy k seskupení řádků servisní zakázky do servisních zakázek.</span><span class="sxs-lookup"><span data-stu-id="0c865-113">When you generate service orders from a service agreement, you can use the service tasks that are assigned to each service agreement line to group service order lines into service orders.</span></span>

## <a name="create-a-service-task"></a><span data-ttu-id="0c865-114">Vytvoření servisní úlohy</span><span class="sxs-lookup"><span data-stu-id="0c865-114">Create a service task</span></span>

1. <span data-ttu-id="0c865-115">Klikněte **Správa servisu** \> **Nastavení** \> **Servisní úlohy**.</span><span class="sxs-lookup"><span data-stu-id="0c865-115">Click **Service management** \> **Setup** \> **Service tasks**.</span></span>
2. <span data-ttu-id="0c865-116">Vytvořit nový řádek.</span><span class="sxs-lookup"><span data-stu-id="0c865-116">Create a new line.</span></span>
3. <span data-ttu-id="0c865-117">Zadejte ID servisu a popis.</span><span class="sxs-lookup"><span data-stu-id="0c865-117">Enter the service ID and description.</span></span>

## <a name="example"></a><span data-ttu-id="0c865-118">Příklad</span><span class="sxs-lookup"><span data-stu-id="0c865-118">Example</span></span>

<span data-ttu-id="0c865-119">Technik má za úkol dokončit dvě práce na převodovce (předmět servisu GB-1234), a to u zákazníka.</span><span class="sxs-lookup"><span data-stu-id="0c865-119">A technician must complete two jobs on a gearbox (service object GB-1234) at a customer site.</span></span> <span data-ttu-id="0c865-120">Pro daného zákazníka je vytvořena servisní smlouva a k uvedeným pracím je přidruženo několik transakcí.</span><span class="sxs-lookup"><span data-stu-id="0c865-120">A service agreement is created for the customer, and several transactions are associated with the jobs.</span></span> <span data-ttu-id="0c865-121">Servisní smlouva a řádky servisní smlouvy pro tyto dvě práce jsou uvedeny dále:</span><span class="sxs-lookup"><span data-stu-id="0c865-121">The service agreement and service agreement lines for the two jobs are as follows:</span></span>

### <a name="service-agreement"></a><span data-ttu-id="0c865-122">Servisní smlouva</span><span class="sxs-lookup"><span data-stu-id="0c865-122">Service agreement</span></span>

| <span data-ttu-id="0c865-123">Project</span><span class="sxs-lookup"><span data-stu-id="0c865-123">Project</span></span> | <span data-ttu-id="0c865-124">Servisní smlouva</span><span class="sxs-lookup"><span data-stu-id="0c865-124">Service agreement</span></span> | <span data-ttu-id="0c865-125">popis</span><span class="sxs-lookup"><span data-stu-id="0c865-125">Description</span></span>                                  | <span data-ttu-id="0c865-126">Seskupit</span><span class="sxs-lookup"><span data-stu-id="0c865-126">Group</span></span>   |
|---------|-------------------|----------------------------------------------|---------|
| <span data-ttu-id="0c865-127">9012</span><span class="sxs-lookup"><span data-stu-id="0c865-127">9012</span></span>    | <span data-ttu-id="0c865-128">000008\_001</span><span class="sxs-lookup"><span data-stu-id="0c865-128">000008\_001</span></span>       | <span data-ttu-id="0c865-129">Kontrola a rutinní výměna – GB-1234</span><span class="sxs-lookup"><span data-stu-id="0c865-129">Inspection and routine replacement – GB-1234</span></span> | <span data-ttu-id="0c865-130">Prémiové</span><span class="sxs-lookup"><span data-stu-id="0c865-130">Premium</span></span> |

### <a name="service-agreement-lines"></a><span data-ttu-id="0c865-131">Řádky servisní smlouvy</span><span class="sxs-lookup"><span data-stu-id="0c865-131">Service agreement lines</span></span>

| <span data-ttu-id="0c865-132">popis</span><span class="sxs-lookup"><span data-stu-id="0c865-132">Description</span></span>             | <span data-ttu-id="0c865-133">typ transakce</span><span class="sxs-lookup"><span data-stu-id="0c865-133">Transaction type</span></span> | <span data-ttu-id="0c865-134">Předmět servisu</span><span class="sxs-lookup"><span data-stu-id="0c865-134">Service object</span></span> | <span data-ttu-id="0c865-135">Servisní úloha</span><span class="sxs-lookup"><span data-stu-id="0c865-135">Service task</span></span> |
|-------------------------|------------------|----------------|--------------|
| <span data-ttu-id="0c865-136">Prohlídka a čištění</span><span class="sxs-lookup"><span data-stu-id="0c865-136">Inspection and cleaning</span></span> | <span data-ttu-id="0c865-137">Hodina</span><span class="sxs-lookup"><span data-stu-id="0c865-137">Hour</span></span>             | <span data-ttu-id="0c865-138">GB-1234</span><span class="sxs-lookup"><span data-stu-id="0c865-138">GB-1234</span></span>        | <span data-ttu-id="0c865-139">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="0c865-139">I/C - GB1234</span></span> |
| <span data-ttu-id="0c865-140">Cestovné</span><span class="sxs-lookup"><span data-stu-id="0c865-140">Travel</span></span>                  | <span data-ttu-id="0c865-141">Expense</span><span class="sxs-lookup"><span data-stu-id="0c865-141">Expense</span></span>          | <span data-ttu-id="0c865-142">GB-1234</span><span class="sxs-lookup"><span data-stu-id="0c865-142">GB-1234</span></span>        | <span data-ttu-id="0c865-143">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="0c865-143">I/C - GB1234</span></span> |
| <span data-ttu-id="0c865-144">Materiály</span><span class="sxs-lookup"><span data-stu-id="0c865-144">Materials</span></span>               | <span data-ttu-id="0c865-145">Zboží</span><span class="sxs-lookup"><span data-stu-id="0c865-145">Item</span></span>             | <span data-ttu-id="0c865-146">GB-1234</span><span class="sxs-lookup"><span data-stu-id="0c865-146">GB-1234</span></span>        | <span data-ttu-id="0c865-147">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="0c865-147">I/C - GB1234</span></span> |
| <span data-ttu-id="0c865-148">Rutinní výměna</span><span class="sxs-lookup"><span data-stu-id="0c865-148">Routine replacement</span></span>     | <span data-ttu-id="0c865-149">Hodina</span><span class="sxs-lookup"><span data-stu-id="0c865-149">Hour</span></span>             | <span data-ttu-id="0c865-150">GB-1234</span><span class="sxs-lookup"><span data-stu-id="0c865-150">GB-1234</span></span>        | <span data-ttu-id="0c865-151">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="0c865-151">RR - GB1234</span></span>  |
| <span data-ttu-id="0c865-152">GR-1</span><span class="sxs-lookup"><span data-stu-id="0c865-152">GR-1</span></span>                    | <span data-ttu-id="0c865-153">Zboží</span><span class="sxs-lookup"><span data-stu-id="0c865-153">Item</span></span>             | <span data-ttu-id="0c865-154">GB-1234</span><span class="sxs-lookup"><span data-stu-id="0c865-154">GB-1234</span></span>        | <span data-ttu-id="0c865-155">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="0c865-155">RR - GB1234</span></span>  |
| <span data-ttu-id="0c865-156">GR-5</span><span class="sxs-lookup"><span data-stu-id="0c865-156">GR-5</span></span>                    | <span data-ttu-id="0c865-157">Zboží</span><span class="sxs-lookup"><span data-stu-id="0c865-157">Item</span></span>             | <span data-ttu-id="0c865-158">GB-1234</span><span class="sxs-lookup"><span data-stu-id="0c865-158">GB-1234</span></span>        | <span data-ttu-id="0c865-159">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="0c865-159">RR - GB1234</span></span>  |

<span data-ttu-id="0c865-160">K řádkům servisní smlouvy pro tyto dvě práce jsou připojeny dvě servisní úlohy.</span><span class="sxs-lookup"><span data-stu-id="0c865-160">The service agreement lines for the two jobs have two service tasks attached to them.</span></span> <span data-ttu-id="0c865-161">Servisní úlohy definují transakce, které náleží k jednotlivým pracím.</span><span class="sxs-lookup"><span data-stu-id="0c865-161">The service tasks determine the transactions that belong to each job.</span></span> <span data-ttu-id="0c865-162">V prvním případě servisní úloha I/C - GB1234 identifikuje všechny řádky servisní smlouvy související s kontrolou a čištěním předmětu GB-1234.</span><span class="sxs-lookup"><span data-stu-id="0c865-162">In the first case, service task I/C - GB1234 identifies all the service agreement lines that are involved in the inspection and cleaning of object GB-1234.</span></span> <span data-ttu-id="0c865-163">V druhém případě servisní úloha RR - GB1234 identifikuje všechny řádky servisní smlouvy související s provedením rutinní výměny.</span><span class="sxs-lookup"><span data-stu-id="0c865-163">In the second case, service task RR - GB1234 identifies all the service agreement lines that are involved in completing a routine replacement job.</span></span>

<span data-ttu-id="0c865-164">Servisní úlohy jsou se specifickou smlouvou propojeny pomocí následujících vztahů servisních úloh:</span><span class="sxs-lookup"><span data-stu-id="0c865-164">The service task relations that connect the service tasks to the specific agreement are as follows:</span></span>

### <a name="service-tasks"></a><span data-ttu-id="0c865-165">Servisní úlohy</span><span class="sxs-lookup"><span data-stu-id="0c865-165">Service tasks</span></span>

| <span data-ttu-id="0c865-166">Servisní úloha</span><span class="sxs-lookup"><span data-stu-id="0c865-166">Service task</span></span> | <span data-ttu-id="0c865-167">Popis</span><span class="sxs-lookup"><span data-stu-id="0c865-167">Description</span></span>                             | <span data-ttu-id="0c865-168">Interní poznámka</span><span class="sxs-lookup"><span data-stu-id="0c865-168">Internal note</span></span>                                                                                                                 | <span data-ttu-id="0c865-169">Externí poznámka</span><span class="sxs-lookup"><span data-stu-id="0c865-169">External note</span></span>                 |
|--------------|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="0c865-170">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="0c865-170">I/C - GB1234</span></span> | <span data-ttu-id="0c865-171">Kontrola převodovky GB-1234</span><span class="sxs-lookup"><span data-stu-id="0c865-171">Inspection of gearbox GB-1234</span></span>           | <span data-ttu-id="0c865-172">Vizuální a mechanická kontrola a čištění převodovky GB-1234.</span><span class="sxs-lookup"><span data-stu-id="0c865-172">Visual and mechanical inspection and cleaning of gearbox GB-1234</span></span>                                                              | <span data-ttu-id="0c865-173">Rutinní kontrola převodovky</span><span class="sxs-lookup"><span data-stu-id="0c865-173">Routine inspection of gearbox</span></span> |
| <span data-ttu-id="0c865-174">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="0c865-174">RR - GB1234</span></span>  | <span data-ttu-id="0c865-175">Rutinní výměna dílů v převodovce GB-1234</span><span class="sxs-lookup"><span data-stu-id="0c865-175">Routine replacement of parts in GB-1234</span></span> | <span data-ttu-id="0c865-176">Rutinní výměna součástí GR-1 a GR-5 (u převodovek vyrobených před rokem 2002 také výměna součásti GR-2)</span><span class="sxs-lookup"><span data-stu-id="0c865-176">Routine service replacement of GR-1 and GR-5 components (for gearboxes manufactured before 2002, also replace GR-2 component)</span></span> | <span data-ttu-id="0c865-177">Rutinní výměna dílů</span><span class="sxs-lookup"><span data-stu-id="0c865-177">Routine replacement of parts</span></span>  |

## <a name="group-service-orders"></a><span data-ttu-id="0c865-178">Seskupení servisních zakázek</span><span class="sxs-lookup"><span data-stu-id="0c865-178">Group service orders</span></span>

<span data-ttu-id="0c865-179">Při automatickém vytváření servisních zakázek můžete použít servisní úlohy jako kritéria seskupení.</span><span class="sxs-lookup"><span data-stu-id="0c865-179">When you create service orders automatically, you can use service tasks as grouping criteria.</span></span> <span data-ttu-id="0c865-180">Chcete-li seskupit servisní zakázky podle servisních úloh, uveďte v servisní smlouvě, že k seskupení servisních zakázek založených na této servisní smlouvě má být jako počáteční kritérium seskupení použito ID servisní úlohy.</span><span class="sxs-lookup"><span data-stu-id="0c865-180">To group service orders by service tasks, define on the service agreement that service orders that are based on the service agreement should be grouped by service task ID as their initial grouping criteria.</span></span>

<span data-ttu-id="0c865-181">**Seskupení podle servisní úlohy**</span><span class="sxs-lookup"><span data-stu-id="0c865-181">**Group by service task**</span></span>

1. <span data-ttu-id="0c865-182">Klikněte na **Správa servisu** \> **Obecné** \> **Servisní smlouvy** \> **Servisní smlouvy**.</span><span class="sxs-lookup"><span data-stu-id="0c865-182">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>
2. <span data-ttu-id="0c865-183">Na kartě **Nastavení** zvolte **Podle servisní úlohy** v poli **Kombinace servisních zakázek**.</span><span class="sxs-lookup"><span data-stu-id="0c865-183">On the **Setup** tab, select **By service task** in the **Combine service orders** field.</span></span>


