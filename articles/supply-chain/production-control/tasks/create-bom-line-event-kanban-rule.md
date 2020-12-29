---
title: Vytvoření kanbanového pravidla události řádku kusovníku
description: Tato úloha je zaměřena na nastavení potřebné k vytvoření kanbanového pravidla události s cílem zajistit zásobování pro řádky výrobního kusovníku v kombinovaném provozním prostředí štíhlé a klasické výroby.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdTable, ProdBOM, ProdParmCostEstimation
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 698b7af3bc8e2146aaf86fb5e04dd123ea6d5153
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423537"
---
# <a name="create-a-bom-line-event-kanban-rule"></a><span data-ttu-id="51410-103">Vytvoření kanbanového pravidla události řádku kusovníku</span><span class="sxs-lookup"><span data-stu-id="51410-103">Create a BOM line event kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="51410-104">Tato úloha je zaměřena na nastavení potřebné k vytvoření kanbanového pravidla události s cílem zajistit zásobování pro řádky výrobního kusovníku v kombinovaném provozním prostředí štíhlé a klasické výroby.</span><span class="sxs-lookup"><span data-stu-id="51410-104">This task focuses on the setup needed to create an event kanban rule to ensure supply for production BOM lines in a mixed lean and classic production environment.</span></span> <span data-ttu-id="51410-105">Tento úkol byl vytvořen pomocí ukázkových dat společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="51410-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="51410-106">Tento postup je určen pro technologa výrobních procesů nebo správce hodnotového proudu, kteří připravují výrobu nového nebo změněného výrobku.</span><span class="sxs-lookup"><span data-stu-id="51410-106">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="51410-107">Vytvořit nové kanbanové pravidlo</span><span class="sxs-lookup"><span data-stu-id="51410-107">Create a new kanban rule</span></span>
1. <span data-ttu-id="51410-108">Přejděte na Řízení výroby > Pravidelné úlohy > Výpočet kanbanového množství > Kanbanová pravidla.</span><span class="sxs-lookup"><span data-stu-id="51410-108">Go to Production control > Periodic tasks > Kanban quantity calculation > Kanban rules.</span></span>
2. <span data-ttu-id="51410-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="51410-109">Click New.</span></span>
3. <span data-ttu-id="51410-110">V poli Typ vyberte Výběr.</span><span class="sxs-lookup"><span data-stu-id="51410-110">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="51410-111">Typ Výběr se používá k vytvoření kanbanů převodu.</span><span class="sxs-lookup"><span data-stu-id="51410-111">The Withdrawal type is used to create transfer kanbans.</span></span>  
4. <span data-ttu-id="51410-112">V poli Strategie doplnění vyberte „Událost“.</span><span class="sxs-lookup"><span data-stu-id="51410-112">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="51410-113">Strategie Událost je vybrána s cílem vytvořit převod kanbanů na základě události.</span><span class="sxs-lookup"><span data-stu-id="51410-113">The Event strategy is selected to create the transfer of kanbans based on an event.</span></span> <span data-ttu-id="51410-114">Později v rámci průvodce úkolu ji spustíme odhadem výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="51410-114">Later in the task guide, we will trigger it by estimating a production order.</span></span>  
5. <span data-ttu-id="51410-115">V poli První aktivita plánu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="51410-115">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="51410-116">Zadejte nebo vyberte ReplenishSpeakerComponents.</span><span class="sxs-lookup"><span data-stu-id="51410-116">Enter or select ReplenishSpeakerComponents.</span></span> <span data-ttu-id="51410-117">Tato aktivita převodu má přijímací sklad (výstupní) a umístění 12, což znamená, že materiál se přesune do umístění 12 ve skladu 12.</span><span class="sxs-lookup"><span data-stu-id="51410-117">This transfer activity has receipt (output) warehouse and location 12, which means that material will be moved to location 12 in warehouse 12.</span></span>  
6. <span data-ttu-id="51410-118">Rozbalte sekci Podrobnosti.</span><span class="sxs-lookup"><span data-stu-id="51410-118">Expand the Details section.</span></span>
7. <span data-ttu-id="51410-119">V poli Produkt zadejte nebo vyberte M0001.</span><span class="sxs-lookup"><span data-stu-id="51410-119">In the Product field, enter or select M0001.</span></span>
8. <span data-ttu-id="51410-120">Rozbalte sekci Události.</span><span class="sxs-lookup"><span data-stu-id="51410-120">Expand the Events section.</span></span>
9. <span data-ttu-id="51410-121">V poli Událost řádku kusovníku vyberte možnost „Automatická“.</span><span class="sxs-lookup"><span data-stu-id="51410-121">In the BOM line event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="51410-122">Pokud je pole Událost řádku kusovníku nastavena na Automaticky, vytvoří se kanban pro splnění požadavků na materiál pro řádky Kusovník výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="51410-122">With the BOM line event field set to Automatic, kanban will be created to fulfill material needs for production order BOM lines.</span></span>  
10. <span data-ttu-id="51410-123">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="51410-123">Close the page.</span></span>

## <a name="create-and-modify-a-new-production-order"></a><span data-ttu-id="51410-124">Vytvoření a úprava nové výrobní zakázky</span><span class="sxs-lookup"><span data-stu-id="51410-124">Create and modify a new production order</span></span>
1. <span data-ttu-id="51410-125">Přejděte na Řízení výroby > Výrobní zakázky > Všechny výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="51410-125">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="51410-126">Klikněte na možnost Nová výrobní zakázka.</span><span class="sxs-lookup"><span data-stu-id="51410-126">Click New production order.</span></span>
3. <span data-ttu-id="51410-127">V poli Číslo zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="51410-127">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="51410-128">Zadejte nebo vyberte hodnotu „L0001“.</span><span class="sxs-lookup"><span data-stu-id="51410-128">Enter or select 'L0001'.</span></span> <span data-ttu-id="51410-129">Použijeme položku L0001, protože položka M0001 je zahrnuta v kusovníku pro položku L0001.</span><span class="sxs-lookup"><span data-stu-id="51410-129">We use item L0001 because item M0001 is included in the BOM for item L0001.</span></span>  
4. <span data-ttu-id="51410-130">Klikněte na položku Vytvořit.</span><span class="sxs-lookup"><span data-stu-id="51410-130">Click Create.</span></span>
5. <span data-ttu-id="51410-131">V seznamu klikněte na odkaz na řádku pro L0001</span><span class="sxs-lookup"><span data-stu-id="51410-131">In the list, click the link in the row for L0001</span></span>
6. <span data-ttu-id="51410-132">Klikněte na položku Kusovník.</span><span class="sxs-lookup"><span data-stu-id="51410-132">Click BOM.</span></span>
7. <span data-ttu-id="51410-133">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="51410-133">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="51410-134">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="51410-134">Click Edit.</span></span>
9. <span data-ttu-id="51410-135">V poli Typ řádku vyberte „Doložená dodávka“.</span><span class="sxs-lookup"><span data-stu-id="51410-135">In the Line type field, select 'Pegged supply'.</span></span>
    * <span data-ttu-id="51410-136">Doložená dodávka je vybrána k aktivaci vytvoření dodávek pro kanban.</span><span class="sxs-lookup"><span data-stu-id="51410-136">Pegged supply is selected to trigger the supply creation of a kanban.</span></span>  
10. <span data-ttu-id="51410-137">Vyberte Ne v poli Spotřeba prostředku.</span><span class="sxs-lookup"><span data-stu-id="51410-137">Select No in the Resource consumption field.</span></span>
    * <span data-ttu-id="51410-138">Zrušením zaškrtnutí políčka Spotřeba prostředku umožňuje změnit sklad.</span><span class="sxs-lookup"><span data-stu-id="51410-138">Clearing the check box of Resource consumption lets us change the warehouse.</span></span>  
11. <span data-ttu-id="51410-139">Rozbalte oblast Dimenze zásob.</span><span class="sxs-lookup"><span data-stu-id="51410-139">Expand the Inventory dimensions section.</span></span>
12. <span data-ttu-id="51410-140">Zadejte hodnotu 12 do pole Sklad.</span><span class="sxs-lookup"><span data-stu-id="51410-140">In the Warehouse field, type '12'.</span></span>
    * <span data-ttu-id="51410-141">Sklad je nastaven na 12, protože se jedná o výstupní sklad pro aktivitu Výběr.</span><span class="sxs-lookup"><span data-stu-id="51410-141">Warehouse is set to 12 because this is the output warehouse for the withdrawal activity.</span></span>  
13. <span data-ttu-id="51410-142">Zadejte hodnotu 12 do pole Umístění.</span><span class="sxs-lookup"><span data-stu-id="51410-142">In the Location field, type '12'.</span></span>
    * <span data-ttu-id="51410-143">Umístění je nastaveno na 12, protože se jedná o výstupní umístění pro aktivitu Výběr.</span><span class="sxs-lookup"><span data-stu-id="51410-143">Location is set to 12 because this is the output location of the withdrawal activity.</span></span>  
14. <span data-ttu-id="51410-144">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="51410-144">Close the page.</span></span>
15. <span data-ttu-id="51410-145">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="51410-145">Close the page.</span></span>

## <a name="estimate-the-production-order-and-view-the-kanban-created"></a><span data-ttu-id="51410-146">Odhad výrobní zakázky a zobrazení vytvořeného kanbanu</span><span class="sxs-lookup"><span data-stu-id="51410-146">Estimate the production order and view the kanban created</span></span>
1. <span data-ttu-id="51410-147">Klepněte na Odhad.</span><span class="sxs-lookup"><span data-stu-id="51410-147">Click Estimate.</span></span>
    * <span data-ttu-id="51410-148">Odhadování výrobní zakázky spustí vytváření přidruženého kanbanu a poskytnutí zboží M0001.</span><span class="sxs-lookup"><span data-stu-id="51410-148">Estimating the production order will trigger the creation of the associated kanban to supply item M0001.</span></span>  
2. <span data-ttu-id="51410-149">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="51410-149">Click OK.</span></span>
3. <span data-ttu-id="51410-150">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="51410-150">Close the page.</span></span>
4. <span data-ttu-id="51410-151">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="51410-151">Close the page.</span></span>
5. <span data-ttu-id="51410-152">Přejděte k Řízení informací o produktech > Lean manufacturing > Kanbanová pravidla.</span><span class="sxs-lookup"><span data-stu-id="51410-152">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
6. <span data-ttu-id="51410-153">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="51410-153">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="51410-154">Vyberte kanbanové pravidlo události vytvořené pro zboží M0001.</span><span class="sxs-lookup"><span data-stu-id="51410-154">Select the event kanban rule created for item M0001.</span></span>  
7. <span data-ttu-id="51410-155">Rozbalte sekci Kanbany.</span><span class="sxs-lookup"><span data-stu-id="51410-155">Expand the Kanbans section.</span></span>
8. <span data-ttu-id="51410-156">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="51410-156">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="51410-157">Všimněte si kanbanu vytvořeného pro dodání zboží M0001 pro odhadovanou výrobní zakázku.</span><span class="sxs-lookup"><span data-stu-id="51410-157">Notice the kanban created to supply M0001 for the estimated production order.</span></span>  
    * <span data-ttu-id="51410-158">Poslední krok!</span><span class="sxs-lookup"><span data-stu-id="51410-158">This is the last step!</span></span>  

