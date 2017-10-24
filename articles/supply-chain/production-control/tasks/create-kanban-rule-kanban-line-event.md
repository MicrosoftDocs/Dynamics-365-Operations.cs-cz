--- 
title: "Vytvoření kanbanového pravidla s použitím události řádku kanbanu"
description: "Tímto postupem vytvoříte kanbanové pravidlo pomocí nastavení události řádku kanbanu s cílem spustit vyžádání z aktivity procesu."
author: ChristianRytt
manager: AnnBe
ms.date: 08/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 9ef7b8e920d22cbc4f96676e68a263f2da7f232c
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-kanban-rule-using-a-kanban-line-event"></a><span data-ttu-id="7980d-103">Vytvoření kanbanového pravidla s použitím události řádku kanbanu</span><span class="sxs-lookup"><span data-stu-id="7980d-103">Create a kanban rule using a kanban line event</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7980d-104">Tímto postupem vytvoříte kanbanové pravidlo pomocí nastavení události řádku kanbanu s cílem spustit vyžádání z aktivity procesu.</span><span class="sxs-lookup"><span data-stu-id="7980d-104">This procedure creates a kanban rule by using the kanban line event setting to trigger pull from a process activity.</span></span> <span data-ttu-id="7980d-105">Kanbanové pravidlo je spuštěno aktivitou procesu kanbanu s množstvím vždy rovným nebo větším, než 25.</span><span class="sxs-lookup"><span data-stu-id="7980d-105">The kanban rule is triggered by a kanban process activity, with a quantity equal to or greater than 25 each.</span></span> <span data-ttu-id="7980d-106">Tento úkol byl vytvořen pomocí ukázkových dat společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="7980d-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="7980d-107">Tento úkol je určen pro technologa výrobních procesů nebo správce hodnotového proudu, kteří připravují výrobu nového nebo změněného výrobku v prostředí štíhlé výroby.</span><span class="sxs-lookup"><span data-stu-id="7980d-107">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-kanban-rule"></a><span data-ttu-id="7980d-108">Vytvoření kanbanového pravidla</span><span class="sxs-lookup"><span data-stu-id="7980d-108">Create a kanban rule</span></span>
1. <span data-ttu-id="7980d-109">Přejděte k Řízení informací o produktech > Lean manufacturing > Kanbanová pravidla.</span><span class="sxs-lookup"><span data-stu-id="7980d-109">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="7980d-110">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="7980d-110">Click New.</span></span>
3. <span data-ttu-id="7980d-111">V poli Strategie doplnění vyberte „Událost“.</span><span class="sxs-lookup"><span data-stu-id="7980d-111">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="7980d-112">Tím se vygenerují kanbany přímo z poptávky.</span><span class="sxs-lookup"><span data-stu-id="7980d-112">This generates kanbans directly from demand.</span></span> <span data-ttu-id="7980d-113">Ty slouží k nastavení pravidel definující scénář režimu rozpadu pro objednávku.</span><span class="sxs-lookup"><span data-stu-id="7980d-113">It is used to set up rules that define a make-to-order scenario.</span></span>  
4. <span data-ttu-id="7980d-114">V poli První aktivita plánu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="7980d-114">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="7980d-115">Zadejte nebo vyberte možnost SpeakerAssemblyAndPolish.</span><span class="sxs-lookup"><span data-stu-id="7980d-115">Enter or select SpeakerAssemblyAndPolish.</span></span> <span data-ttu-id="7980d-116">První aktivita pravidla výrobního kanbanu musí být aktivita procesu ve výrobním toku.</span><span class="sxs-lookup"><span data-stu-id="7980d-116">The first activity of a manufacturing kanban rule is a process activity in the production flow.</span></span> <span data-ttu-id="7980d-117">Vyberete-li aktivitu, data platnosti aktivity budou zkopírovány do dat platnosti kanbanového pravidla.</span><span class="sxs-lookup"><span data-stu-id="7980d-117">When you select the activity, the validity dates of the activity are copied to the validity dates of the kanban rule.</span></span>  
5. <span data-ttu-id="7980d-118">Rozbalte sekci Podrobnosti.</span><span class="sxs-lookup"><span data-stu-id="7980d-118">Expand the Details section.</span></span>
6. <span data-ttu-id="7980d-119">Zadejte hodnotu L0001 do pole Produkt.</span><span class="sxs-lookup"><span data-stu-id="7980d-119">In the Product field, type 'L0001'.</span></span>
7. <span data-ttu-id="7980d-120">Rozbalte sekci Události.</span><span class="sxs-lookup"><span data-stu-id="7980d-120">Expand the Events section.</span></span>
8. <span data-ttu-id="7980d-121">V poli Událost řádku kanban vyberte možnost „Automatická“.</span><span class="sxs-lookup"><span data-stu-id="7980d-121">In the Kanban line event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="7980d-122">To generuje kanbany události na vyžádání.</span><span class="sxs-lookup"><span data-stu-id="7980d-122">This generates event kanbans on demand.</span></span>  <span data-ttu-id="7980d-123">Toto pole slouží ke konfiguraci kanbanových pravidel, která doplní materiál potřebný pro navazující aktivitu procesu.</span><span class="sxs-lookup"><span data-stu-id="7980d-123">The field is used to configure kanban rules that replenish material that is required for a downstream process activity.</span></span> <span data-ttu-id="7980d-124">Vyberete-li Automaticky, kanbany události jsou vytvořeny s poptávky.</span><span class="sxs-lookup"><span data-stu-id="7980d-124">When you select Automatic, the event kanbans are created with the demand.</span></span> <span data-ttu-id="7980d-125">Toto nastavení se doporučuje při spuštění výroby ve stejný den.</span><span class="sxs-lookup"><span data-stu-id="7980d-125">This setting is recommended if you expect to execute production on the same day.</span></span>  
9. <span data-ttu-id="7980d-126">Nastavte minimální množství události na „25“.</span><span class="sxs-lookup"><span data-stu-id="7980d-126">Set Minimum event quantity to '25'.</span></span>
    * <span data-ttu-id="7980d-127">Kanbany události jsou generovány, když je výše požadavku rovna nebo vyšší než v tomto poli.</span><span class="sxs-lookup"><span data-stu-id="7980d-127">Event kanbans are generated when the demand quantity is equal to or more than this field.</span></span> <span data-ttu-id="7980d-128">To je užitečné, když se mají v jednom stroji generovat množství objednávky nižší, než v tomto poli, a v jiném stroji vyšší, než v tomto poli.</span><span class="sxs-lookup"><span data-stu-id="7980d-128">This is useful if you want to produce an order quantity less than this field on one machine and more than this field on another machine.</span></span>  
10. <span data-ttu-id="7980d-129">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="7980d-129">Click Save.</span></span>

## <a name="create-sales-order-and-trigger-kanban-chain"></a><span data-ttu-id="7980d-130">Vytvoření prodejní objednávky a spuštění kanbanu řetězce</span><span class="sxs-lookup"><span data-stu-id="7980d-130">Create sales order and trigger kanban chain</span></span>
1. <span data-ttu-id="7980d-131">Přejděte na Prodej a marketing > Prodejní objednávky > Všechny prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="7980d-131">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="7980d-132">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="7980d-132">Click New.</span></span>
3. <span data-ttu-id="7980d-133">V poli Účet odběratele zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="7980d-133">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="7980d-134">Vyberte účet odběratele US-003, Forest Wholesales.</span><span class="sxs-lookup"><span data-stu-id="7980d-134">Select Customer account US-003, Forest Wholesales.</span></span>  
4. <span data-ttu-id="7980d-135">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="7980d-135">Click OK.</span></span>
5. <span data-ttu-id="7980d-136">Do pole Číslo položky zadejte L0001.</span><span class="sxs-lookup"><span data-stu-id="7980d-136">In the Item number field, type 'L0001'.</span></span>
    * <span data-ttu-id="7980d-137">L0001 je zboží, pro které jste vytvořili kanbanové pravidlo.</span><span class="sxs-lookup"><span data-stu-id="7980d-137">L0001 is the item for which you created the kanban rule.</span></span>  
6. <span data-ttu-id="7980d-138">Nastavte množství na hodnotu 27.</span><span class="sxs-lookup"><span data-stu-id="7980d-138">Set Quantity to '27'.</span></span>
    * <span data-ttu-id="7980d-139">Protože 27 je vyšší, než minimální množství 25 v kanbanovém pravidle, spustí se tak kanbanová událost.</span><span class="sxs-lookup"><span data-stu-id="7980d-139">Because 27 is higher than the minimum quantity of 25 on the kanban rule, this will trigger an event kanban.</span></span>  
7. <span data-ttu-id="7980d-140">Zadejte do pole Místo hodnotu „1“.</span><span class="sxs-lookup"><span data-stu-id="7980d-140">In the Site field, type '1'.</span></span>
8. <span data-ttu-id="7980d-141">V poli Sklad zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="7980d-141">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="7980d-142">Vyberte sklad 13.</span><span class="sxs-lookup"><span data-stu-id="7980d-142">Select warehouse 13.</span></span>  
9. <span data-ttu-id="7980d-143">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="7980d-143">Click Save.</span></span>

## <a name="view-the-kanban-generated-by-the-kanban-rule"></a><span data-ttu-id="7980d-144">Zobrazení kanbanu generovaného pravidlem kanbanu</span><span class="sxs-lookup"><span data-stu-id="7980d-144">View the kanban generated by the kanban rule</span></span>
1. <span data-ttu-id="7980d-145">Přejděte k Řízení informací o produktech > Lean manufacturing > Kanbanová pravidla.</span><span class="sxs-lookup"><span data-stu-id="7980d-145">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="7980d-146">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="7980d-146">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="7980d-147">Rozbalte sekci Kanbany.</span><span class="sxs-lookup"><span data-stu-id="7980d-147">Expand the Kanbans section.</span></span>
    * <span data-ttu-id="7980d-148">Všimněte si, že kanban pro 27 byl vytvořen pro zpracování aktivity na základě vytvořeného kanbanového pravidla.</span><span class="sxs-lookup"><span data-stu-id="7980d-148">Notice that a kanban for 27 was created to process the  activity based on the created kanban rule.</span></span>  
    * <span data-ttu-id="7980d-149">Jde o poslední krok.</span><span class="sxs-lookup"><span data-stu-id="7980d-149">This is the last step.</span></span>  


