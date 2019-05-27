---
title: Vytvoření kanbanového pravidla s použitím události pro minimální úroveň zásob
description: Tento postup se zaměřuje na nastavení potřebné k vytvoření kanbanového pravidlo pomocí události pro minimální úroveň zásob, aby tak bylo jisté, že bude konkrétní produkt v určitém místě vždy k dispozici.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable, InventLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2a9ba8ec2abb26e3b9ee7e14bdf882c1ffcb205b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558519"
---
# <a name="create-a-kanban-rule-using-a-minimum-stock-event"></a><span data-ttu-id="9c5fd-103">Vytvoření kanbanového pravidla s použitím události pro minimální úroveň zásob</span><span class="sxs-lookup"><span data-stu-id="9c5fd-103">Create a kanban rule using a minimum stock event</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9c5fd-104">Tento postup se zaměřuje na nastavení potřebné k vytvoření kanbanového pravidlo pomocí události pro minimální úroveň zásob, aby tak bylo jisté, že bude konkrétní produkt v určitém místě vždy k dispozici.</span><span class="sxs-lookup"><span data-stu-id="9c5fd-104">This procedure focuses on the setup needed to create a kanban rule using a minimum stock event to ensure that a specific product is always available at a specific location.</span></span> <span data-ttu-id="9c5fd-105">Je vytvořeno kanbanové pravidlo, které při poklesu úrovně zásob pod 200 kusů převede materiál do skladového místa.</span><span class="sxs-lookup"><span data-stu-id="9c5fd-105">A kanban rule is created to transfer material to the location when the inventory level drops below 200 pieces.</span></span> <span data-ttu-id="9c5fd-106">Spuštěním zpracování události požadavku dojde k vytvoření potřebných kanbanů.</span><span class="sxs-lookup"><span data-stu-id="9c5fd-106">By running the Pegging event processing, the needed kanbans are created.</span></span> <span data-ttu-id="9c5fd-107">Tento úkol byl vytvořen pomocí ukázkových dat společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="9c5fd-107">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="9c5fd-108">Tento úkol je určen pro technologa výrobních procesů nebo správce hodnotového proudu, kteří připravují výrobu nového nebo změněného výrobku v prostředí štíhlé výroby.</span><span class="sxs-lookup"><span data-stu-id="9c5fd-108">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="9c5fd-109">Vytvořit nové kanbanové pravidlo</span><span class="sxs-lookup"><span data-stu-id="9c5fd-109">Create a new kanban rule</span></span>
1. <span data-ttu-id="9c5fd-110">Přejděte k Řízení informací o produktech > Lean manufacturing > Kanbanová pravidla.</span><span class="sxs-lookup"><span data-stu-id="9c5fd-110">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="9c5fd-111">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="9c5fd-111">Click New.</span></span>
3. <span data-ttu-id="9c5fd-112">V poli Typ vyberte Výběr.</span><span class="sxs-lookup"><span data-stu-id="9c5fd-112">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="9c5fd-113">Tento typ se používá k vytvoření kanbanů převodu.</span><span class="sxs-lookup"><span data-stu-id="9c5fd-113">This type is used to create transfer kanbans.</span></span>  
4. <span data-ttu-id="9c5fd-114">V poli Strategie doplnění vyberte „Událost“.</span><span class="sxs-lookup"><span data-stu-id="9c5fd-114">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="9c5fd-115">Strategie Událost se používá s cílem vytvořit převod kanbanů na základě události.</span><span class="sxs-lookup"><span data-stu-id="9c5fd-115">The Event strategy is used to create the transfer kanbans based on an event.</span></span> <span data-ttu-id="9c5fd-116">Dále v postupu spustíte kanbany převodu pomocí doplnění skladu.</span><span class="sxs-lookup"><span data-stu-id="9c5fd-116">Later in the procedure, you will trigger transfer kanbans by using stock replenishment.</span></span>  
5. <span data-ttu-id="9c5fd-117">V poli První aktivita plánu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="9c5fd-117">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="9c5fd-118">Zadejte nebo vyberte ReplenishSpeakerComponents.</span><span class="sxs-lookup"><span data-stu-id="9c5fd-118">Enter or select ReplenishSpeakerComponents.</span></span> <span data-ttu-id="9c5fd-119">Tato aktivita převodu má přijímací sklad (výstupní) a umístění 12, což znamená, že materiál se přesune do umístění 12 ve skladu 12.</span><span class="sxs-lookup"><span data-stu-id="9c5fd-119">This transfer activity has receipt (output) warehouse and location 12, which means that materials will be moved to location 12 in warehouse 12.</span></span>  
6. <span data-ttu-id="9c5fd-120">Rozbalte sekci Podrobnosti.</span><span class="sxs-lookup"><span data-stu-id="9c5fd-120">Expand the Details section.</span></span>
7. <span data-ttu-id="9c5fd-121">V poli Produkt zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="9c5fd-121">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="9c5fd-122">Vyberte volbu „M0007“.</span><span class="sxs-lookup"><span data-stu-id="9c5fd-122">Select M0007.</span></span>  
8. <span data-ttu-id="9c5fd-123">Rozbalte sekci Události.</span><span class="sxs-lookup"><span data-stu-id="9c5fd-123">Expand the Events section.</span></span>
9. <span data-ttu-id="9c5fd-124">V poli Událost doplnění skladu vyberte „Dávka“.</span><span class="sxs-lookup"><span data-stu-id="9c5fd-124">In the Stock replenishment event field, select 'Batch'.</span></span>
    * <span data-ttu-id="9c5fd-125">Tímto krokem se vytvoří kanbany pro splnění požadavků na materiál v souvisejícím umístění během zpracování události požadavku.</span><span class="sxs-lookup"><span data-stu-id="9c5fd-125">This creates kanbans to fulfill material needs at the related location during Pegging event processing.</span></span>  

## <a name="set-the-minimum-quantity-for-the-item"></a><span data-ttu-id="9c5fd-126">Nastavení minimálního množství pro zboží</span><span class="sxs-lookup"><span data-stu-id="9c5fd-126">Set the minimum quantity for the item</span></span>
1. <span data-ttu-id="9c5fd-127">Kliknutím přejdete na odkaz v poli Produkt.</span><span class="sxs-lookup"><span data-stu-id="9c5fd-127">Click to follow the link in the Product field.</span></span>
2. <span data-ttu-id="9c5fd-128">Kliknutím přejdete na odkaz v poli Číslo položky.</span><span class="sxs-lookup"><span data-stu-id="9c5fd-128">Click to follow the link in the Item number field.</span></span>
3. <span data-ttu-id="9c5fd-129">Rozbalte okno s fakty Obrázek produktu.</span><span class="sxs-lookup"><span data-stu-id="9c5fd-129">Expand the Product image FactBox.</span></span>
4. <span data-ttu-id="9c5fd-130">V podokně akcí klikněte na položku Plán.</span><span class="sxs-lookup"><span data-stu-id="9c5fd-130">On the Action Pane, click Plan.</span></span>
5. <span data-ttu-id="9c5fd-131">Klikněte na Disponibilita položky.</span><span class="sxs-lookup"><span data-stu-id="9c5fd-131">Click Item coverage.</span></span>
6. <span data-ttu-id="9c5fd-132">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="9c5fd-132">Click New.</span></span>
7. <span data-ttu-id="9c5fd-133">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="9c5fd-133">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="9c5fd-134">V poli Sklad zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="9c5fd-134">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="9c5fd-135">Nastavte sklad na 12.</span><span class="sxs-lookup"><span data-stu-id="9c5fd-135">Set Warehouse to 12.</span></span>  
9. <span data-ttu-id="9c5fd-136">Nastavte Minimum na "200".</span><span class="sxs-lookup"><span data-stu-id="9c5fd-136">Set Minimum to '200'.</span></span>

## <a name="run-the-batch-event-creation-job"></a><span data-ttu-id="9c5fd-137">Spuštění dávkové úlohy pro vytvoření události</span><span class="sxs-lookup"><span data-stu-id="9c5fd-137">Run the batch event creation job</span></span>
1. <span data-ttu-id="9c5fd-138">Přejděte na Řízení výroby > Pravidelné úlohy > Dávkové zpracování kanbanových úloh > Zpracování události požadavku.</span><span class="sxs-lookup"><span data-stu-id="9c5fd-138">Go to Production control > Periodic tasks > Kanban job batch processing > Pegging event processing.</span></span>
2. <span data-ttu-id="9c5fd-139">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="9c5fd-139">Click OK.</span></span>
3. <span data-ttu-id="9c5fd-140">Přejděte k Řízení informací o produktech > Lean manufacturing > Kanbanová pravidla.</span><span class="sxs-lookup"><span data-stu-id="9c5fd-140">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
4. <span data-ttu-id="9c5fd-141">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="9c5fd-141">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9c5fd-142">Vyberte kanbanové pravidlo, které bylo vytvořeno dříve.</span><span class="sxs-lookup"><span data-stu-id="9c5fd-142">Select the kanban rule that you created earlier.</span></span>  
5. <span data-ttu-id="9c5fd-143">Rozbalte sekci Kanbany.</span><span class="sxs-lookup"><span data-stu-id="9c5fd-143">Expand the Kanbans section.</span></span>
    * <span data-ttu-id="9c5fd-144">Všimněte si, že kanban byl vytvořen pro přenos potřebného materiálu do skladu 12.</span><span class="sxs-lookup"><span data-stu-id="9c5fd-144">Notice that a kanban was created to transfer the needed material to warehouse 12.</span></span>  

