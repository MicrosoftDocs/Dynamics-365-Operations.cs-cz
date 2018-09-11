--- 
title: "Seřazení výrobních úloh pro procesní výrobu"
description: "Tento postup používá barevné výrobky jako příklad popisující to, jak seřadit plánované objednávky podle priority barvy a velikosti obalu."
author: ChristianRytt
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransPo, PMFSeqReqRouteChangesListPage
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: ee2606bcd24aefc2fa5fc9d11e8a9640db366f91
ms.contentlocale: cs-cz
ms.lasthandoff: 09/11/2018

---
# <a name="sequence-production-jobs-for-process-manufacturing"></a><span data-ttu-id="f999e-103">Seřazení výrobních úloh pro procesní výrobu</span><span class="sxs-lookup"><span data-stu-id="f999e-103">Sequence production jobs for process manufacturing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f999e-104">Tento postup používá barevné výrobky jako příklad popisující to, jak seřadit plánované objednávky podle priority barvy a velikosti obalu.</span><span class="sxs-lookup"><span data-stu-id="f999e-104">This procedure uses paint products as an example to show how to sequence planned orders according to the priority of color and package size.</span></span> <span data-ttu-id="f999e-105">K vytvoření tohoto postupu jsou použita ukázková data společnosti USPI.</span><span class="sxs-lookup"><span data-stu-id="f999e-105">The demo data company used to create this procedure is USPI.</span></span> <span data-ttu-id="f999e-106">Tento postup je určen pro plánujícího produkce.</span><span class="sxs-lookup"><span data-stu-id="f999e-106">This procedure is intended for the production planner.</span></span>


## <a name="run-master-planning-for-uspi"></a><span data-ttu-id="f999e-107">Spuštění hlavního plánování pro USPI</span><span class="sxs-lookup"><span data-stu-id="f999e-107">Run master planning for USPI</span></span>
1. <span data-ttu-id="f999e-108">Přejděte na Hlavní plánování > Hlavní plánování > Spustit > Hlavní plánování.</span><span class="sxs-lookup"><span data-stu-id="f999e-108">Go to Master planning > Master planning > Run > Master planning.</span></span>
2. <span data-ttu-id="f999e-109">V poli Hlavní plán kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="f999e-109">In the Master plan field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="f999e-110">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="f999e-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f999e-111">Vyberte MasterPlan.</span><span class="sxs-lookup"><span data-stu-id="f999e-111">Select MasterPlan.</span></span>  
4. <span data-ttu-id="f999e-112">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="f999e-112">Click OK.</span></span>
    * <span data-ttu-id="f999e-113">Tím se spustí hlavní plánování, včetně zpracování pořadí.</span><span class="sxs-lookup"><span data-stu-id="f999e-113">This starts Master Planning, including the sequence process.</span></span> <span data-ttu-id="f999e-114">Tento proces může trvat několik minut.</span><span class="sxs-lookup"><span data-stu-id="f999e-114">This process can take a few minutes.</span></span>  

## <a name="view-planned-orders-for-the-paint-products"></a><span data-ttu-id="f999e-115">Zobrazení plánovaných objednávek pro barevné výrobky</span><span class="sxs-lookup"><span data-stu-id="f999e-115">View planned orders for the paint products</span></span>
1. <span data-ttu-id="f999e-116">Přejděte na Hlavní plánování > Hlavní plánování > Plánované objednávky.</span><span class="sxs-lookup"><span data-stu-id="f999e-116">Go to Master planning > Master planning > Planned orders.</span></span>
2. <span data-ttu-id="f999e-117">Rozbalte okno s fakty Podrobnosti o zboží.</span><span class="sxs-lookup"><span data-stu-id="f999e-117">Expand the Item details FactBox.</span></span>
3. <span data-ttu-id="f999e-118">Rozbalte okno s fakty Podrobnosti plánu.</span><span class="sxs-lookup"><span data-stu-id="f999e-118">Expand the Schedule details FactBox.</span></span>
4. <span data-ttu-id="f999e-119">V poli Plán kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="f999e-119">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="f999e-120">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="f999e-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f999e-121">Vyberte MasterPlan.</span><span class="sxs-lookup"><span data-stu-id="f999e-121">Select MasterPlan.</span></span>  
6. <span data-ttu-id="f999e-122">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="f999e-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="f999e-123">Použijte rychlý filtr k filtrování v poli Číslo položky na základě hodnoty P300.</span><span class="sxs-lookup"><span data-stu-id="f999e-123">Use the Quick Filter to filter on the Item number field with a value of 'P300'.</span></span>
    * <span data-ttu-id="f999e-124">Po odemknutí se přesuňte doprava a prohlédněte si datum objednávky a datum dodání.</span><span class="sxs-lookup"><span data-stu-id="f999e-124">Unlock to scroll to the right to see the order date and delivery date.</span></span> <span data-ttu-id="f999e-125">Všimněte si, že tyto položky mají datum objednávky Dnes, a data dodání pro plánované objednávky nejsou klasifikovány po prioritě barvy a velikosti balení, jak je uvedeno v názvu produktu.</span><span class="sxs-lookup"><span data-stu-id="f999e-125">Notice that these items have an order date of Today and the delivery dates for the planned orders are not sequenced after the priority of color and package size, as shown in the product name.</span></span> <span data-ttu-id="f999e-126">Můžete ponechat číslo položky a zobrazit tak název produktu a prioritu.</span><span class="sxs-lookup"><span data-stu-id="f999e-126">You can hover over an item number to see the product name and priority.</span></span>  

## <a name="sequence-planned-orders-for-paint"></a><span data-ttu-id="f999e-127">Seřazení plánovaných objednávek pro barvu</span><span class="sxs-lookup"><span data-stu-id="f999e-127">Sequence planned orders for paint</span></span>
1. <span data-ttu-id="f999e-128">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="f999e-128">Close the page.</span></span>
2. <span data-ttu-id="f999e-129">Přejděte na Hlavní plánování > Hlavní plánování > Plánovaná objednávka s klasifikací.</span><span class="sxs-lookup"><span data-stu-id="f999e-129">Go to Master planning > Master planning > Sequenced planned orders.</span></span>
3. <span data-ttu-id="f999e-130">Rozbalte okno s fakty Podrobnosti o zboží.</span><span class="sxs-lookup"><span data-stu-id="f999e-130">Expand the Item details FactBox.</span></span>
4. <span data-ttu-id="f999e-131">Rozbalte okno s fakty Podrobnosti plánu.</span><span class="sxs-lookup"><span data-stu-id="f999e-131">Expand the Schedule details FactBox.</span></span>
    * <span data-ttu-id="f999e-132">Poznámka: v této části můžete vidět, že Počáteční datum a čas pro plánované objednávky je klasifikován podle barvy a velikosti obalu v rámci období intervalu 28 dnů.</span><span class="sxs-lookup"><span data-stu-id="f999e-132">Note: Here you see that the Start date/time for the planned orders are sequenced according to color and package size within a bucket period of 28 days.</span></span> <span data-ttu-id="f999e-133">Tato období jsou definovány číslem v poli Kampaň.</span><span class="sxs-lookup"><span data-stu-id="f999e-133">These periods are defined by a number in the field Campaign.</span></span> <span data-ttu-id="f999e-134">Formulář plánované objednávky s klasifikací funguje stejně jako typický formulář pro plánované objednávky, a plánovač výroby lze může potvrdit plánované objednávky.</span><span class="sxs-lookup"><span data-stu-id="f999e-134">The sequenced planned order form acts like the typical planned order form, and the production planner can firm the planned orders here.</span></span>  
5. <span data-ttu-id="f999e-135">Označte všechny řádky.</span><span class="sxs-lookup"><span data-stu-id="f999e-135">Mark all rows.</span></span>
6. <span data-ttu-id="f999e-136">Klepněte na možnost Akceptovat.</span><span class="sxs-lookup"><span data-stu-id="f999e-136">Click Accept.</span></span>
    * <span data-ttu-id="f999e-137">Dojde k aktualizaci plánovaných objednávek s vybranou akcí posloupnosti Odklady nebo Zálohy.</span><span class="sxs-lookup"><span data-stu-id="f999e-137">This will update the planned orders with the selected sequence action of either Postpone or Advance.</span></span>  

## <a name="verify-the-sequence-of-the-planned-orders"></a><span data-ttu-id="f999e-138">Kontrola seřazení plánovaných objednávek</span><span class="sxs-lookup"><span data-stu-id="f999e-138">Verify the sequence of the planned orders</span></span>
1. <span data-ttu-id="f999e-139">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="f999e-139">Close the page.</span></span>
2. <span data-ttu-id="f999e-140">Přejděte na Hlavní plánování > Hlavní plánování > Plánované objednávky.</span><span class="sxs-lookup"><span data-stu-id="f999e-140">Go to Master planning > Master planning > Planned orders.</span></span>
3. <span data-ttu-id="f999e-141">Rozbalte okno s fakty Podrobnosti o zboží.</span><span class="sxs-lookup"><span data-stu-id="f999e-141">Expand the Item details FactBox.</span></span>
4. <span data-ttu-id="f999e-142">Rozbalte okno s fakty Podrobnosti plánu.</span><span class="sxs-lookup"><span data-stu-id="f999e-142">Expand the Schedule details FactBox.</span></span>
5. <span data-ttu-id="f999e-143">V poli Plán kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="f999e-143">In the Plan field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="f999e-144">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="f999e-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f999e-145">Vyberte MasterPlan.</span><span class="sxs-lookup"><span data-stu-id="f999e-145">Select MasterPlan.</span></span>  
7. <span data-ttu-id="f999e-146">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="f999e-146">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="f999e-147">Použijte rychlý filtr k filtrování v poli Číslo položky na základě hodnoty P300.</span><span class="sxs-lookup"><span data-stu-id="f999e-147">Use the Quick Filter to filter on the Item number field with a value of 'P300'.</span></span>
    * <span data-ttu-id="f999e-148">Všimněte si, že objednávky nyní jsou seřazeny podle priority barev a velikostí, a plánované objednávky začínají k prvnímu datu objednání a datu dodání.</span><span class="sxs-lookup"><span data-stu-id="f999e-148">Notice that the orders now are sequenced according to the priority of color and size and the planned orders start at the earliest order date and delivery date.</span></span> <span data-ttu-id="f999e-149">Ověřte údaje ve sloupci Datum objednávky nebo Počáteční datum v okně s fakty Podrobnosti plánu.</span><span class="sxs-lookup"><span data-stu-id="f999e-149">Validate the Order date column or the Start date in the Schedule details FactBbox.</span></span>  


