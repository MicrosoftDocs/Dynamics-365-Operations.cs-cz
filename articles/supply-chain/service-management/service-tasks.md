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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9dfeddcf754ccaf1f5fb5d3f20ca771145c5f2a1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5223307"
---
# <a name="service-tasks-overview"></a><span data-ttu-id="a77f7-104">Přehled servisních úloh</span><span class="sxs-lookup"><span data-stu-id="a77f7-104">Service tasks overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a77f7-105">Servisní úlohy lze použít k popisu úloh, které mají být dokončeny v průběhu servisní zakázky.</span><span class="sxs-lookup"><span data-stu-id="a77f7-105">Use service tasks to describe the task to be completed during a service order.</span></span>
<span data-ttu-id="a77f7-106">Tyto informace mohou vidět technici a zákazníci.</span><span class="sxs-lookup"><span data-stu-id="a77f7-106">Both technicians and customers can see this information.</span></span>

<span data-ttu-id="a77f7-107">K vytváření servisních úloh slouží stránka **Servisní úlohy** lze přidružit k určité servisní smlouvě nebo servisní zakázce pomocí vztahů servisních úloh.</span><span class="sxs-lookup"><span data-stu-id="a77f7-107">You create service tasks in the **Service tasks** page, and you associate service tasks with a specific service agreement or service order by creating service task relations.</span></span> <span data-ttu-id="a77f7-108">Při vytváření vztahu servisní úlohy můžete vytvořit:</span><span class="sxs-lookup"><span data-stu-id="a77f7-108">Every time that you create a service task relation, you can create the following:</span></span>

-  <span data-ttu-id="a77f7-109">interní poznámky k úloze, například podrobné technické požadavky, o nichž by měli vědět technici;</span><span class="sxs-lookup"><span data-stu-id="a77f7-109">Internal notes for the task, such as detailed technical requests for the task that are important for the technician to know.</span></span>

-  <span data-ttu-id="a77f7-110">externí poznámky, které mohou vidět zákazníci.</span><span class="sxs-lookup"><span data-stu-id="a77f7-110">External notes that the customer can see.</span></span> <span data-ttu-id="a77f7-111">Zde je možné uvést méně technické vysvětlení prováděné úlohy v závislosti na smlouvě mezi zákazníkem a servisní společností.</span><span class="sxs-lookup"><span data-stu-id="a77f7-111">These might provide a less technical explanation of the task that is being completed, according to the agreement between the customer and the service company.</span></span>

<span data-ttu-id="a77f7-112">Když vytvoříte vztah servisní úlohy mezi servisní úlohou a servisní zakázkou nebo servisní smlouvou, můžete tuto servisní úlohu zadat při vytváření řádků servisní zakázky nebo servisní smlouvy pro aktuální servisní zakázku či smlouvu.</span><span class="sxs-lookup"><span data-stu-id="a77f7-112">When you have set up a service task relation between a service task and a service order or service agreement, you can specify this service task when you create service order lines or service agreement lines for the current service order or service agreement.</span></span>

<span data-ttu-id="a77f7-113">Pokud na základě servisní smlouvy generujete servisní zakázky, můžete použít servisní úlohy přiřazené k jednotlivým řádkům servisní smlouvy k seskupení řádků servisní zakázky do servisních zakázek.</span><span class="sxs-lookup"><span data-stu-id="a77f7-113">When you generate service orders from a service agreement, you can use the service tasks that are assigned to each service agreement line to group service order lines into service orders.</span></span>

## <a name="create-a-service-task"></a><span data-ttu-id="a77f7-114">Vytvoření servisní úlohy</span><span class="sxs-lookup"><span data-stu-id="a77f7-114">Create a service task</span></span>

1. <span data-ttu-id="a77f7-115">Klikněte **Správa servisu** \> **Nastavení** \> **Servisní úlohy**.</span><span class="sxs-lookup"><span data-stu-id="a77f7-115">Click **Service management** \> **Setup** \> **Service tasks**.</span></span>
2. <span data-ttu-id="a77f7-116">Vytvořit nový řádek.</span><span class="sxs-lookup"><span data-stu-id="a77f7-116">Create a new line.</span></span>
3. <span data-ttu-id="a77f7-117">Zadejte ID servisu a popis.</span><span class="sxs-lookup"><span data-stu-id="a77f7-117">Enter the service ID and description.</span></span>

## <a name="example"></a><span data-ttu-id="a77f7-118">Příklad</span><span class="sxs-lookup"><span data-stu-id="a77f7-118">Example</span></span>

<span data-ttu-id="a77f7-119">Technik má za úkol dokončit dvě práce na převodovce (předmět servisu GB-1234), a to u zákazníka.</span><span class="sxs-lookup"><span data-stu-id="a77f7-119">A technician must complete two jobs on a gearbox (service object GB-1234) at a customer site.</span></span> <span data-ttu-id="a77f7-120">Pro daného zákazníka je vytvořena servisní smlouva a k uvedeným pracím je přidruženo několik transakcí.</span><span class="sxs-lookup"><span data-stu-id="a77f7-120">A service agreement is created for the customer, and several transactions are associated with the jobs.</span></span> <span data-ttu-id="a77f7-121">Servisní smlouva a řádky servisní smlouvy pro tyto dvě práce jsou uvedeny dále:</span><span class="sxs-lookup"><span data-stu-id="a77f7-121">The service agreement and service agreement lines for the two jobs are as follows:</span></span>

### <a name="service-agreement"></a><span data-ttu-id="a77f7-122">Servisní smlouva</span><span class="sxs-lookup"><span data-stu-id="a77f7-122">Service agreement</span></span>

| <span data-ttu-id="a77f7-123">Project</span><span class="sxs-lookup"><span data-stu-id="a77f7-123">Project</span></span> | <span data-ttu-id="a77f7-124">Servisní smlouva</span><span class="sxs-lookup"><span data-stu-id="a77f7-124">Service agreement</span></span> | <span data-ttu-id="a77f7-125">popis</span><span class="sxs-lookup"><span data-stu-id="a77f7-125">Description</span></span>                                  | <span data-ttu-id="a77f7-126">Seskupit</span><span class="sxs-lookup"><span data-stu-id="a77f7-126">Group</span></span>   |
|---------|-------------------|----------------------------------------------|---------|
| <span data-ttu-id="a77f7-127">9012</span><span class="sxs-lookup"><span data-stu-id="a77f7-127">9012</span></span>    | <span data-ttu-id="a77f7-128">000008\_001</span><span class="sxs-lookup"><span data-stu-id="a77f7-128">000008\_001</span></span>       | <span data-ttu-id="a77f7-129">Kontrola a rutinní výměna – GB-1234</span><span class="sxs-lookup"><span data-stu-id="a77f7-129">Inspection and routine replacement – GB-1234</span></span> | <span data-ttu-id="a77f7-130">Prémiové</span><span class="sxs-lookup"><span data-stu-id="a77f7-130">Premium</span></span> |

### <a name="service-agreement-lines"></a><span data-ttu-id="a77f7-131">Řádky servisní smlouvy</span><span class="sxs-lookup"><span data-stu-id="a77f7-131">Service agreement lines</span></span>

| <span data-ttu-id="a77f7-132">popis</span><span class="sxs-lookup"><span data-stu-id="a77f7-132">Description</span></span>             | <span data-ttu-id="a77f7-133">typ transakce</span><span class="sxs-lookup"><span data-stu-id="a77f7-133">Transaction type</span></span> | <span data-ttu-id="a77f7-134">Předmět servisu</span><span class="sxs-lookup"><span data-stu-id="a77f7-134">Service object</span></span> | <span data-ttu-id="a77f7-135">Servisní úloha</span><span class="sxs-lookup"><span data-stu-id="a77f7-135">Service task</span></span> |
|-------------------------|------------------|----------------|--------------|
| <span data-ttu-id="a77f7-136">Prohlídka a čištění</span><span class="sxs-lookup"><span data-stu-id="a77f7-136">Inspection and cleaning</span></span> | <span data-ttu-id="a77f7-137">Hodina</span><span class="sxs-lookup"><span data-stu-id="a77f7-137">Hour</span></span>             | <span data-ttu-id="a77f7-138">GB-1234</span><span class="sxs-lookup"><span data-stu-id="a77f7-138">GB-1234</span></span>        | <span data-ttu-id="a77f7-139">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="a77f7-139">I/C - GB1234</span></span> |
| <span data-ttu-id="a77f7-140">Cestovné</span><span class="sxs-lookup"><span data-stu-id="a77f7-140">Travel</span></span>                  | <span data-ttu-id="a77f7-141">Expense</span><span class="sxs-lookup"><span data-stu-id="a77f7-141">Expense</span></span>          | <span data-ttu-id="a77f7-142">GB-1234</span><span class="sxs-lookup"><span data-stu-id="a77f7-142">GB-1234</span></span>        | <span data-ttu-id="a77f7-143">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="a77f7-143">I/C - GB1234</span></span> |
| <span data-ttu-id="a77f7-144">Materiály</span><span class="sxs-lookup"><span data-stu-id="a77f7-144">Materials</span></span>               | <span data-ttu-id="a77f7-145">Zboží</span><span class="sxs-lookup"><span data-stu-id="a77f7-145">Item</span></span>             | <span data-ttu-id="a77f7-146">GB-1234</span><span class="sxs-lookup"><span data-stu-id="a77f7-146">GB-1234</span></span>        | <span data-ttu-id="a77f7-147">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="a77f7-147">I/C - GB1234</span></span> |
| <span data-ttu-id="a77f7-148">Rutinní výměna</span><span class="sxs-lookup"><span data-stu-id="a77f7-148">Routine replacement</span></span>     | <span data-ttu-id="a77f7-149">Hodina</span><span class="sxs-lookup"><span data-stu-id="a77f7-149">Hour</span></span>             | <span data-ttu-id="a77f7-150">GB-1234</span><span class="sxs-lookup"><span data-stu-id="a77f7-150">GB-1234</span></span>        | <span data-ttu-id="a77f7-151">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="a77f7-151">RR - GB1234</span></span>  |
| <span data-ttu-id="a77f7-152">GR-1</span><span class="sxs-lookup"><span data-stu-id="a77f7-152">GR-1</span></span>                    | <span data-ttu-id="a77f7-153">Zboží</span><span class="sxs-lookup"><span data-stu-id="a77f7-153">Item</span></span>             | <span data-ttu-id="a77f7-154">GB-1234</span><span class="sxs-lookup"><span data-stu-id="a77f7-154">GB-1234</span></span>        | <span data-ttu-id="a77f7-155">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="a77f7-155">RR - GB1234</span></span>  |
| <span data-ttu-id="a77f7-156">GR-5</span><span class="sxs-lookup"><span data-stu-id="a77f7-156">GR-5</span></span>                    | <span data-ttu-id="a77f7-157">Zboží</span><span class="sxs-lookup"><span data-stu-id="a77f7-157">Item</span></span>             | <span data-ttu-id="a77f7-158">GB-1234</span><span class="sxs-lookup"><span data-stu-id="a77f7-158">GB-1234</span></span>        | <span data-ttu-id="a77f7-159">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="a77f7-159">RR - GB1234</span></span>  |

<span data-ttu-id="a77f7-160">K řádkům servisní smlouvy pro tyto dvě práce jsou připojeny dvě servisní úlohy.</span><span class="sxs-lookup"><span data-stu-id="a77f7-160">The service agreement lines for the two jobs have two service tasks attached to them.</span></span> <span data-ttu-id="a77f7-161">Servisní úlohy definují transakce, které náleží k jednotlivým pracím.</span><span class="sxs-lookup"><span data-stu-id="a77f7-161">The service tasks determine the transactions that belong to each job.</span></span> <span data-ttu-id="a77f7-162">V prvním případě servisní úloha I/C - GB1234 identifikuje všechny řádky servisní smlouvy související s kontrolou a čištěním předmětu GB-1234.</span><span class="sxs-lookup"><span data-stu-id="a77f7-162">In the first case, service task I/C - GB1234 identifies all the service agreement lines that are involved in the inspection and cleaning of object GB-1234.</span></span> <span data-ttu-id="a77f7-163">V druhém případě servisní úloha RR - GB1234 identifikuje všechny řádky servisní smlouvy související s provedením rutinní výměny.</span><span class="sxs-lookup"><span data-stu-id="a77f7-163">In the second case, service task RR - GB1234 identifies all the service agreement lines that are involved in completing a routine replacement job.</span></span>

<span data-ttu-id="a77f7-164">Servisní úlohy jsou se specifickou smlouvou propojeny pomocí následujících vztahů servisních úloh:</span><span class="sxs-lookup"><span data-stu-id="a77f7-164">The service task relations that connect the service tasks to the specific agreement are as follows:</span></span>

### <a name="service-tasks"></a><span data-ttu-id="a77f7-165">Servisní úlohy</span><span class="sxs-lookup"><span data-stu-id="a77f7-165">Service tasks</span></span>

| <span data-ttu-id="a77f7-166">Servisní úloha</span><span class="sxs-lookup"><span data-stu-id="a77f7-166">Service task</span></span> | <span data-ttu-id="a77f7-167">Popis</span><span class="sxs-lookup"><span data-stu-id="a77f7-167">Description</span></span>                             | <span data-ttu-id="a77f7-168">Interní poznámka</span><span class="sxs-lookup"><span data-stu-id="a77f7-168">Internal note</span></span>                                                                                                                 | <span data-ttu-id="a77f7-169">Externí poznámka</span><span class="sxs-lookup"><span data-stu-id="a77f7-169">External note</span></span>                 |
|--------------|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="a77f7-170">I/C - GB1234</span><span class="sxs-lookup"><span data-stu-id="a77f7-170">I/C - GB1234</span></span> | <span data-ttu-id="a77f7-171">Kontrola převodovky GB-1234</span><span class="sxs-lookup"><span data-stu-id="a77f7-171">Inspection of gearbox GB-1234</span></span>           | <span data-ttu-id="a77f7-172">Vizuální a mechanická kontrola a čištění převodovky GB-1234.</span><span class="sxs-lookup"><span data-stu-id="a77f7-172">Visual and mechanical inspection and cleaning of gearbox GB-1234</span></span>                                                              | <span data-ttu-id="a77f7-173">Rutinní kontrola převodovky</span><span class="sxs-lookup"><span data-stu-id="a77f7-173">Routine inspection of gearbox</span></span> |
| <span data-ttu-id="a77f7-174">RR - GB1234</span><span class="sxs-lookup"><span data-stu-id="a77f7-174">RR - GB1234</span></span>  | <span data-ttu-id="a77f7-175">Rutinní výměna dílů v převodovce GB-1234</span><span class="sxs-lookup"><span data-stu-id="a77f7-175">Routine replacement of parts in GB-1234</span></span> | <span data-ttu-id="a77f7-176">Rutinní výměna součástí GR-1 a GR-5 (u převodovek vyrobených před rokem 2002 také výměna součásti GR-2)</span><span class="sxs-lookup"><span data-stu-id="a77f7-176">Routine service replacement of GR-1 and GR-5 components (for gearboxes manufactured before 2002, also replace GR-2 component)</span></span> | <span data-ttu-id="a77f7-177">Rutinní výměna dílů</span><span class="sxs-lookup"><span data-stu-id="a77f7-177">Routine replacement of parts</span></span>  |

## <a name="group-service-orders"></a><span data-ttu-id="a77f7-178">Seskupení servisních zakázek</span><span class="sxs-lookup"><span data-stu-id="a77f7-178">Group service orders</span></span>

<span data-ttu-id="a77f7-179">Při automatickém vytváření servisních zakázek můžete použít servisní úlohy jako kritéria seskupení.</span><span class="sxs-lookup"><span data-stu-id="a77f7-179">When you create service orders automatically, you can use service tasks as grouping criteria.</span></span> <span data-ttu-id="a77f7-180">Chcete-li seskupit servisní zakázky podle servisních úloh, uveďte v servisní smlouvě, že k seskupení servisních zakázek založených na této servisní smlouvě má být jako počáteční kritérium seskupení použito ID servisní úlohy.</span><span class="sxs-lookup"><span data-stu-id="a77f7-180">To group service orders by service tasks, define on the service agreement that service orders that are based on the service agreement should be grouped by service task ID as their initial grouping criteria.</span></span>

<span data-ttu-id="a77f7-181">**Seskupení podle servisní úlohy**</span><span class="sxs-lookup"><span data-stu-id="a77f7-181">**Group by service task**</span></span>

1. <span data-ttu-id="a77f7-182">Klikněte na **Správa servisu** \> **Obecné** \> **Servisní smlouvy** \> **Servisní smlouvy**.</span><span class="sxs-lookup"><span data-stu-id="a77f7-182">Click **Service management** \> **Common** \> **Service agreements** \> **Service agreements**.</span></span>
2. <span data-ttu-id="a77f7-183">Na kartě **Nastavení** zvolte **Podle servisní úlohy** v poli **Kombinace servisních zakázek**.</span><span class="sxs-lookup"><span data-stu-id="a77f7-183">On the **Setup** tab, select **By service task** in the **Combine service orders** field.</span></span>




[!INCLUDE[footer-include](../../includes/footer-banner.md)]