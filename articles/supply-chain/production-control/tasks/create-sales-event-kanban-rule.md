---
title: Vytvoření kanbanového pravidla události prodeje
description: Tento postup se zaměřuje na potřebné nastavení k vytvoření kanbanového pravidla, které se spustí při vytváření prodejní objednávky.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1759adea6db8120078e2f32bff79178545c2328a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423526"
---
# <a name="create-a-sales-event-kanban-rule"></a><span data-ttu-id="78df6-103">Vytvoření kanbanového pravidla události prodeje</span><span class="sxs-lookup"><span data-stu-id="78df6-103">Create a sales event kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="78df6-104">Tento postup se zaměřuje na potřebné nastavení k vytvoření kanbanového pravidla, které se spustí při vytváření prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="78df6-104">This procedure focuses on the setup needed to create a kanban rule that is triggered during sales order creation.</span></span> <span data-ttu-id="78df6-105">Pravidla kanbanové události doplňuje požadavky, které pocházejí z řádků prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="78df6-105">The event kanban rule replenishes requirements that originate from sales order lines.</span></span> <span data-ttu-id="78df6-106">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="78df6-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="78df6-107">Je to určeno pro technologa výrobních procesů nebo správce hodnotového proudu, kteří připravují výrobu nového nebo změněného výrobku.</span><span class="sxs-lookup"><span data-stu-id="78df6-107">It is intended for the process engineer or the value stream manager as they prepare production of a new or modified product.</span></span>




## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="78df6-108">Vytvořit nové kanbanové pravidlo</span><span class="sxs-lookup"><span data-stu-id="78df6-108">Create a new kanban rule</span></span>
1. <span data-ttu-id="78df6-109">Otevřete Kanbanová pravidla.</span><span class="sxs-lookup"><span data-stu-id="78df6-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="78df6-110">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="78df6-110">Click New.</span></span>
3. <span data-ttu-id="78df6-111">V poli Strategie doplnění vyberte „Událost“.</span><span class="sxs-lookup"><span data-stu-id="78df6-111">In the Replenishment strategy field, select 'Event'.</span></span>
    * <span data-ttu-id="78df6-112">Výběr události znamená, že kanbanové pravidlo je vyvoláno událostí, například vytvořením řádku prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="78df6-112">Selecting Event means that the kanban rule is triggered by an event, for example, creation of a sales order line.</span></span>   <span data-ttu-id="78df6-113">Používá se na oblasti, kde každý kanban by měl pokrývat specifické požadavky.</span><span class="sxs-lookup"><span data-stu-id="78df6-113">This is applied to areas where each kanban should cover a specific demand.</span></span>  
4. <span data-ttu-id="78df6-114">V poli První aktivita plánu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="78df6-114">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="78df6-115">Vyberte Poslední sestavení.</span><span class="sxs-lookup"><span data-stu-id="78df6-115">Select Final assembly.</span></span>  
5. <span data-ttu-id="78df6-116">Rozbalte sekci Podrobnosti.</span><span class="sxs-lookup"><span data-stu-id="78df6-116">Expand the Details section.</span></span>
6. <span data-ttu-id="78df6-117">V poli Produkt zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="78df6-117">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="78df6-118">Vyberte volbu „L0050“.</span><span class="sxs-lookup"><span data-stu-id="78df6-118">Select L0050.</span></span>  

## <a name="define-an-event"></a><span data-ttu-id="78df6-119">Definujte událost</span><span class="sxs-lookup"><span data-stu-id="78df6-119">Define an event</span></span>
1. <span data-ttu-id="78df6-120">Rozbalte sekci Události.</span><span class="sxs-lookup"><span data-stu-id="78df6-120">Expand the Events section.</span></span>
2. <span data-ttu-id="78df6-121">V poli Události prodeje vyberte možnost „Automatická“.</span><span class="sxs-lookup"><span data-stu-id="78df6-121">In the Sales event field, select 'Automatic'.</span></span>
    * <span data-ttu-id="78df6-122">Výběrem automatické události prodeje bude toto kanbanové pravidlo bude aktivováno automaticky při shodě řádku prodeje s umístěním a příjmem produktů.</span><span class="sxs-lookup"><span data-stu-id="78df6-122">By selecting the sales event Automatic, this kanban rule will be triggered automatically when a sales line matches the product and receipt location.</span></span> <span data-ttu-id="78df6-123">V tomto postupu je produkt L0050 ve skladu 13.</span><span class="sxs-lookup"><span data-stu-id="78df6-123">In this procedure, it is product L0050 on warehouse 13.</span></span>  
3. <span data-ttu-id="78df6-124">Nastavte minimální množství události na „50“.</span><span class="sxs-lookup"><span data-stu-id="78df6-124">Set Minimum event quantity to '50'.</span></span>
    * <span data-ttu-id="78df6-125">S minimálním množstvím událostí 50, se bude kanbanové pravidlo pouze spouštět událostmi s množstvím 50 nebo vyšším.</span><span class="sxs-lookup"><span data-stu-id="78df6-125">With a minimum event quantity of 50, the kanban rule will only be triggered by events with a quantity of 50 or more.</span></span>  
4. <span data-ttu-id="78df6-126">Rozbalte položku výrobního toku.</span><span class="sxs-lookup"><span data-stu-id="78df6-126">Expand the Production flow section.</span></span>
    * <span data-ttu-id="78df6-127">Všimněte si, že místo příjmu je sklad 13.</span><span class="sxs-lookup"><span data-stu-id="78df6-127">Notice that the Receipt location is warehouse 13.</span></span> <span data-ttu-id="78df6-128">To znamená, že pro toto místo bude spouštěno toto kanbanové pravidlo.</span><span class="sxs-lookup"><span data-stu-id="78df6-128">This means that this kanban rule will be triggered for this location.</span></span>  
    * <span data-ttu-id="78df6-129">V tomto příkladu řádek prodeje produktu L0050, s množstvím nejméně 50 na skladu 13, se spustí tímto kanbanovým pravidlem.</span><span class="sxs-lookup"><span data-stu-id="78df6-129">In this example, a sales line for product L0050, with a quantity of 50 or more, on warehouse 13, will trigger this kanban rule.</span></span>  

## <a name="create-sales-line-to-trigger-event-kanban-rule"></a><span data-ttu-id="78df6-130">Vytvořte řádek prodeje pro aktivaci události kanbanovým pravidlem</span><span class="sxs-lookup"><span data-stu-id="78df6-130">Create sales line to trigger event kanban rule</span></span>
1. <span data-ttu-id="78df6-131">Přejděte na Všechny prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="78df6-131">Go to All sales orders.</span></span>
    * <span data-ttu-id="78df6-132">Upozornění se zobrazí při uložení kanbanového pravidla, což znamená, že kanbany budou vytvořeny v reálném čase při vytváření prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="78df6-132">A warning is shown when the kanban rule is saved, which means that kanbans will be created in real-time during sales order creation.</span></span>  
2. <span data-ttu-id="78df6-133">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="78df6-133">Click New.</span></span>
3. <span data-ttu-id="78df6-134">V poli Účet odběratele zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="78df6-134">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="78df6-135">Vyberte například US-003.</span><span class="sxs-lookup"><span data-stu-id="78df6-135">For example, select US-003.</span></span>  
4. <span data-ttu-id="78df6-136">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="78df6-136">Click OK.</span></span>
5. <span data-ttu-id="78df6-137">Do pole Číslo položky zadejte L0050.</span><span class="sxs-lookup"><span data-stu-id="78df6-137">In the Item number field, type 'L0050'.</span></span>
6. <span data-ttu-id="78df6-138">Zadejte do pole Místo hodnotu „1“.</span><span class="sxs-lookup"><span data-stu-id="78df6-138">In the Site field, type '1'.</span></span>
    * <span data-ttu-id="78df6-139">Vyberte Místo 1 neboť Sklad 13 je připojen v Místě 1.</span><span class="sxs-lookup"><span data-stu-id="78df6-139">Select Site 1 because Warehouse 13 is on Site 1.</span></span>  
7. <span data-ttu-id="78df6-140">V poli Sklad zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="78df6-140">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="78df6-141">Nastavte sklad na 13.</span><span class="sxs-lookup"><span data-stu-id="78df6-141">Set Warehouse to 13.</span></span>  
8. <span data-ttu-id="78df6-142">Nastavte množství na hodnotu 75.</span><span class="sxs-lookup"><span data-stu-id="78df6-142">Set Quantity to '75'.</span></span>
    * <span data-ttu-id="78df6-143">Zadejte množství 50 nebo vyšší pro aktivaci vytvořeného kanbanového pravidla.</span><span class="sxs-lookup"><span data-stu-id="78df6-143">Enter a quantity of 50 or greater, to trigger the created kanban rule.</span></span>  

## <a name="verify-that-kanban-is-created"></a><span data-ttu-id="78df6-144">Ověřte, že je kanban vytvořen</span><span class="sxs-lookup"><span data-stu-id="78df6-144">Verify that kanban is created</span></span>
1. <span data-ttu-id="78df6-145">Klikněte na Produkt a dodávka.</span><span class="sxs-lookup"><span data-stu-id="78df6-145">Click Product and supply.</span></span>
2. <span data-ttu-id="78df6-146">Klepněte na Zobrazit strom doložení.</span><span class="sxs-lookup"><span data-stu-id="78df6-146">Click View pegging tree.</span></span>
    * <span data-ttu-id="78df6-147">Všimněte si, že kanban je vytvořen stejným množstvím jako řádek prodeje.</span><span class="sxs-lookup"><span data-stu-id="78df6-147">Notice that a kanban with the same quantity as the sales line is created.</span></span> <span data-ttu-id="78df6-148">Můžete také vidět výdej materiálu vyžadovaný k výrobě L0050.</span><span class="sxs-lookup"><span data-stu-id="78df6-148">You can also see the material issues needed to produce L0050.</span></span> <span data-ttu-id="78df6-149">Tento krok je posledním krokem v tomto postupu.</span><span class="sxs-lookup"><span data-stu-id="78df6-149">This is the last step in this procedure.</span></span>  

