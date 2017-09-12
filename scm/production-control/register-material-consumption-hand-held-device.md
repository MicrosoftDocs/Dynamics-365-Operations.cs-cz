---
title: "Registrace spotřeby materiálu pomocí mobilního zařízení"
description: "Toto téma popisuje workflow, který umožňuje registraci spotřeby surovin ve výrobě pomocí ručního zařízení."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: AX 7.0.0, Operations, UnifiedOperations
ms.custom: 1706093
ms.assetid: 75ee68e0-4b9f-4f4d-b286-f498e0eb73fa
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 97d374230cc6e833b9f585de000e1252f2a78b9d
ms.openlocfilehash: 83703d962d6099ba8ac107548a569c8d1f34882f
ms.contentlocale: cs-cz
ms.lasthandoff: 08/30/2017

---

# <a name="register-material-consumption-using-a-mobile-device"></a><span data-ttu-id="23a63-103">Registrace spotřeby materiálu pomocí mobilního zařízení</span><span class="sxs-lookup"><span data-stu-id="23a63-103">Register material consumption using a mobile device</span></span>
<span data-ttu-id="23a63-104">Toto téma popisuje workflow, který umožňuje registraci spotřeby surovin ve výrobě pomocí ručního zařízení.</span><span class="sxs-lookup"><span data-stu-id="23a63-104">This topic describes a workflow that enables registration of raw material consumption in production by using a handheld device.</span></span>

<a name="introduction"></a><span data-ttu-id="23a63-105">Úvod</span><span class="sxs-lookup"><span data-stu-id="23a63-105">Introduction</span></span>
------------

<span data-ttu-id="23a63-106">Tento workflow platí v případě, že existují přísné požadavky na sledování materiálu.</span><span class="sxs-lookup"><span data-stu-id="23a63-106">This workflow is relevant if there is a strict requirement for material traceability.</span></span> <span data-ttu-id="23a63-107">V těchto případech musí být vykázán přesný stav spotřeby pro účely zachování sledovatelnosti materiálů.</span><span class="sxs-lookup"><span data-stu-id="23a63-107">In those cases, to maintain traceability of the materials, the exact time and quantity must be reported for the consumption.</span></span> <span data-ttu-id="23a63-108">Na tento proces lze nazírat jako na opačný proces, než jsou operace vyprázdnění předem nebo následně, kdy existuje posun mezi časem registrace a časem, kdy proběhne skutečná spotřeba.</span><span class="sxs-lookup"><span data-stu-id="23a63-108">This process can be seen as opposed to pre- or back-flushing operations, where there is an offset between the time of registration and the time when the actual consumption takes place.</span></span> <span data-ttu-id="23a63-109">To vysvětluje, proč nelze pro některé materiály použít strategii sledování automatické spotřeby.</span><span class="sxs-lookup"><span data-stu-id="23a63-109">This explains why a strategy of automatic consumption cannot be used for some materials with traceability requirements.</span></span> <span data-ttu-id="23a63-110">Podívejme se na jednoduchý scénář, který vysvětluje postup při nastavování workflowu s povolením registrace spotřeby surovin ve výrobě pomocí ručního zařízení.</span><span class="sxs-lookup"><span data-stu-id="23a63-110">Let’s look at a simple scenario that explains how to set up a workflow to enable registration of raw material consumption in production by using a handheld device.</span></span> [![](./media/scenario3.png)](./media/scenario3.png)

### <a name="scenario-details"></a><span data-ttu-id="23a63-111">Podrobnosti scénáře</span><span class="sxs-lookup"><span data-stu-id="23a63-111">Scenario details</span></span>

<span data-ttu-id="23a63-112">Proces souvislé výroby (5) spotřebovává surovinu RM-100 řízenou dávkou.</span><span class="sxs-lookup"><span data-stu-id="23a63-112">A continuous production process (5) consumes the batch-controlled raw material RM-100.</span></span> <span data-ttu-id="23a63-113">Materiál je k dispozici v umístění Bulk-001 (1) pro registrační značku vozidla PL-1 se dvěma dávkami, B1 a B2, z nichž obě mají množství 100 kg.</span><span class="sxs-lookup"><span data-stu-id="23a63-113">The material is on-hand on location Bulk-001 (1) on license plate PL-1 with two batches, B1 and B2, both with a quantity of 100 lbs.</span></span> <span data-ttu-id="23a63-114">Práce ve skladu (2) je uvolněna a zpracována pro RM-100 a materiál je vyzvednut ze skladu Bulk-001 do vstupního místa výroby PIL-01 (3), které je definováno jako místo neřízené registrační značkou.</span><span class="sxs-lookup"><span data-stu-id="23a63-114">Warehouse work (2) is released and processed for RM-100, and the material is picked from Bulk-001 to the production input location PIL-01 (3), which is defined as non-license plate controlled.</span></span> <span data-ttu-id="23a63-115">Obsluha stroje zváží materiál ze vstupního místa výroby (3) a registruje hmotnost a číslo dávky jako spotřebované (4).</span><span class="sxs-lookup"><span data-stu-id="23a63-115">The machine operator weighs out material from the production input location (3) and registers the weight and batch number as consumed (4).</span></span> <span data-ttu-id="23a63-116">Ze vstupního místa výroby je část materiálu ručně vložena do výrobního procesu v definovaných časových intervalech.</span><span class="sxs-lookup"><span data-stu-id="23a63-116">From the production input location, a portion of the material is manually added to the production process in defined time intervals.</span></span> <span data-ttu-id="23a63-117">Když obsluha stroje přidá materiál, je zvážen na váze a zaregistruje se číslo dávky.</span><span class="sxs-lookup"><span data-stu-id="23a63-117">When the machine operator adds material, it is weighed on a scale and the batch number is registered.</span></span>

## <a name="set-up-the-workflow-to-register-consumption-using-a-handheld-device"></a><span data-ttu-id="23a63-118">Nastavení workflowu při registraci spotřeby pomocí ručního zařízení</span><span class="sxs-lookup"><span data-stu-id="23a63-118">Set up the workflow to register consumption using a handheld device</span></span>
<span data-ttu-id="23a63-119">Vytvořte produkt dokončené výroby FG-100 s kusovníkem, kde je surovina řízenou dávkou RM-100.</span><span class="sxs-lookup"><span data-stu-id="23a63-119">Create a finished-good product, FG-100, with a bill of material that has the batch-controlled raw material RM-100.</span></span> <span data-ttu-id="23a63-120">Přidejte dvě dávky B1 a B2 RM-100 v množství 100 do umístění: Bulk-001 s registrační značkou: PL-1.</span><span class="sxs-lookup"><span data-stu-id="23a63-120">Add two batches, B1 and B2, of RM-100 in a quantity of 100 to location: Bulk-001 on license plate: PL-1.</span></span> <span data-ttu-id="23a63-121">Princip vyprazdňování na řádku kusovníku pro RM-100 kusovníku je nastaven na **ruční**.</span><span class="sxs-lookup"><span data-stu-id="23a63-121">The flushing principle on the bill of material line for RM-100 is set to **Manual**.</span></span> <span data-ttu-id="23a63-122">Nastavte výchozí umístění výrobního vstupu na PIL-01.</span><span class="sxs-lookup"><span data-stu-id="23a63-122">Set  the production input location to PIL-01.</span></span> <span data-ttu-id="23a63-123">To můžete provést výběrem tohoto skladového místa jako vstupního místa výroby ve skladu 51.</span><span class="sxs-lookup"><span data-stu-id="23a63-123">You can do that by selecting this location as the default production input location on warehouse 51.</span></span>

1.  <span data-ttu-id="23a63-124">Vytvoření nové položky nabídky mobilních zařízení:</span><span class="sxs-lookup"><span data-stu-id="23a63-124">Create a new mobile device menu item:</span></span> 

-    <span data-ttu-id="23a63-125">**Název položky nabídky** – zaregistrujte spotřebu materiálu.</span><span class="sxs-lookup"><span data-stu-id="23a63-125">**Menu item name** - Register material consumption.</span></span> 
-    <span data-ttu-id="23a63-126">**Název** - Zaregistrovat spotřebu materiálu</span><span class="sxs-lookup"><span data-stu-id="23a63-126">**Title** - Register material consumption.</span></span> 
-    <span data-ttu-id="23a63-127">**Režim** – nepřímé.</span><span class="sxs-lookup"><span data-stu-id="23a63-127">**Mode** - Indirect.</span></span> 
-    <span data-ttu-id="23a63-128">**Kód činnosti** - Zaregistrovat spotřebu materiálu</span><span class="sxs-lookup"><span data-stu-id="23a63-128">**Activity code** - Register material consumption.</span></span>

2.  <span data-ttu-id="23a63-129">Přidejte položku nabídky do nabídky zařízení **Mobilní výroba**.</span><span class="sxs-lookup"><span data-stu-id="23a63-129">Add the menu item to the **Production Mobile** device menu.</span></span>
3.  <span data-ttu-id="23a63-130">Vytvořte výrobní zakázku dokončeného produktu:</span><span class="sxs-lookup"><span data-stu-id="23a63-130">Create a production order for the finished product:</span></span> 

-    <span data-ttu-id="23a63-131">**Číslo položky** - FG-100</span><span class="sxs-lookup"><span data-stu-id="23a63-131">**Item number** - FG-100</span></span> 
-    <span data-ttu-id="23a63-132">**Lokalita** - 5</span><span class="sxs-lookup"><span data-stu-id="23a63-132">**Site** - 5</span></span> 
-    <span data-ttu-id="23a63-133">**Sklad** - 51</span><span class="sxs-lookup"><span data-stu-id="23a63-133">**Warehouse** - 51</span></span> 
-    <span data-ttu-id="23a63-134">**Množství** - 150</span><span class="sxs-lookup"><span data-stu-id="23a63-134">**Quantity** - 150</span></span>

<span data-ttu-id="23a63-135">Výrobní zakázka je **odhad** a **Uvolněno** a je vytvořena práce ve skladu.</span><span class="sxs-lookup"><span data-stu-id="23a63-135">The production order is **Estimated** and **Released** and warehouse work is created.</span></span>

4.  <span data-ttu-id="23a63-136">Dokončete práci pomocí workflowu pro vyzvednutí surovin pro přenosná zařízení pro výdej.</span><span class="sxs-lookup"><span data-stu-id="23a63-136">Complete the work using the workflow for raw material picking for the handheld device.</span></span>

<span data-ttu-id="23a63-137">To přenese materiál z velkoskladu do vstupního místa výroby PIL 01.</span><span class="sxs-lookup"><span data-stu-id="23a63-137">This will bring the material from the bulk location to the production input location PIL-01.</span></span> <span data-ttu-id="23a63-138">Po dokončení práce má materiál stav **vydáno na vstupní místo výroby**.</span><span class="sxs-lookup"><span data-stu-id="23a63-138">After the work is completed, the material has the status **Picked on the production input location**.</span></span> <span data-ttu-id="23a63-139">Stav poté, co byla práce zpracována, může být buď **vyskladněno** nebo **Rezervované – fyzicky**.</span><span class="sxs-lookup"><span data-stu-id="23a63-139">The status after work has been processed can be either **Picked** or **Reserved physical**.</span></span> <span data-ttu-id="23a63-140">To je nakonfigurováno s parametrem **stav výdeje po vložení ve formuláři skladu**.</span><span class="sxs-lookup"><span data-stu-id="23a63-140">This is configured with the parameter **Issue status after put on the warehouse form**.</span></span>

5.  <span data-ttu-id="23a63-141">Spusťte výrobní zakázku z klienta nebo v ručního zařízení spuštění pomocí položky nabídky **zahájení výroby**.</span><span class="sxs-lookup"><span data-stu-id="23a63-141">Start the production order either from the client or from the handheld device by using the **Production start** menu item.</span></span>

<span data-ttu-id="23a63-142">Po spuštění výrobní zakázky můžete zaregistrovat spotřeby materiálu s workflowem pro ručním zařízení.</span><span class="sxs-lookup"><span data-stu-id="23a63-142">After the production order has been started, you can register material consumption with the workflow for the handheld device.</span></span> <span data-ttu-id="23a63-143">Začněme registrací spotřeby 25 kg dávky B1.</span><span class="sxs-lookup"><span data-stu-id="23a63-143">Let's start by registering consumption of 25 lbs of batch B1.</span></span>

6.  <span data-ttu-id="23a63-144">Vyberte položku nabídky **Zaregistrovat materiál** **spotřeba** pro ruční zařízení a zadejte následující informace:</span><span class="sxs-lookup"><span data-stu-id="23a63-144">Select the **Register material** **consumption** menu item in the menu for the hand held device, enter the following details:</span></span> 

-    <span data-ttu-id="23a63-145">Číslo výrobní zakázky </span><span class="sxs-lookup"><span data-stu-id="23a63-145">The production order number.</span></span> 
-    <span data-ttu-id="23a63-146">Skladové místo, ve kterém se bude materiál spotřebovávat, je v tomto případě PIL-01.</span><span class="sxs-lookup"><span data-stu-id="23a63-146">The location on which the material is going to be consumed, in this case PIL-01.</span></span> 
-    <span data-ttu-id="23a63-147">Číslo položky RM-100.</span><span class="sxs-lookup"><span data-stu-id="23a63-147">Item number RM-100.</span></span> 
-    <span data-ttu-id="23a63-148">Číslo dávky B1.</span><span class="sxs-lookup"><span data-stu-id="23a63-148">Batch number B1.</span></span> 
-    <span data-ttu-id="23a63-149">Množství 25.</span><span class="sxs-lookup"><span data-stu-id="23a63-149">A quantity of 25.</span></span>

7.  <span data-ttu-id="23a63-150">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="23a63-150">Select **OK**.</span></span>

<span data-ttu-id="23a63-151">Všimněte si, že se na displeji zobrazí zpráva "Vytvoření řádku deníku".</span><span class="sxs-lookup"><span data-stu-id="23a63-151">Note that the message "Journal line is created" appears on the display.</span></span> <span data-ttu-id="23a63-152">Ve výrobní zakázce se vytvoří otevřený deník typu **výrobní výdejka** pro číslo položky RM-100 a číslo dávky B1.</span><span class="sxs-lookup"><span data-stu-id="23a63-152">On the production order there is an open journal of the type **Production picking list** for item number RM-100 and batch number B1.</span></span> 

<span data-ttu-id="23a63-153">Nyní můžete pokračovat v registraci, například v čísle dávky B2 a pokaždé, když vyberete **OK**, se do otevřeného deníku přidá nový řádek deníku.</span><span class="sxs-lookup"><span data-stu-id="23a63-153">You can now choose to continue your registration, for example on batch number B2, and each time you select **OK,** a new journal line is added to the open journal.</span></span> 

<span data-ttu-id="23a63-154">Po dokončení registrace vyberte možnost **Hotovo** k zaúčtování deníku a ukončení workflowu.</span><span class="sxs-lookup"><span data-stu-id="23a63-154">After you have finished your registration, select **Done** to post the journal and end the workflow.</span></span>

### <a name="additional-comments"></a><span data-ttu-id="23a63-155">Další komentáře</span><span class="sxs-lookup"><span data-stu-id="23a63-155">Additional comments</span></span> 

-   <span data-ttu-id="23a63-156">Pokud uživatel zruší workflow po vytvoření řádku deníku, tento deník je ve stavu nezaúčtované, ale jestli uživatel později použije workflow pro stejnou výrobní zakázku, budou řádky přidány do otevřeného deníku, nikoli do nového deníku.</span><span class="sxs-lookup"><span data-stu-id="23a63-156">If a user cancels the workflow after a journal line is created, the journal is in an unposted state but if the user at a later point uses the workflow for the same production order, then the lines will be added to the open journal rather than to a new journal.</span></span>
-   <span data-ttu-id="23a63-157">Nový workflow podporuje také registrace sériového čísla.</span><span class="sxs-lookup"><span data-stu-id="23a63-157">The new workflow also supports the registration of serial numbers.</span></span>
-   <span data-ttu-id="23a63-158">Je možné registrovat číslo položky, která je definováno v kusovníku nebo v receptuře pro vybranou výrobní zakázku nebo dávkovou objednávku.</span><span class="sxs-lookup"><span data-stu-id="23a63-158">It is only possible to register an item number that is defined in the bill of material or in the formula for the selected production order or batch order.</span></span>
-   <span data-ttu-id="23a63-159">Může dojít k vyčerpání materiálu.</span><span class="sxs-lookup"><span data-stu-id="23a63-159">Material can be overconsumed.</span></span> <span data-ttu-id="23a63-160">Například pokud má být spotřebováno množství 100 kg materiálu, poté ji může být vyčerpán, pokud je množství například 105 kg.</span><span class="sxs-lookup"><span data-stu-id="23a63-160">For example, if the material is estimated to be consumed with the quantity of 100 lbs, then it can be overconsumed with a quantity of, for example, 105 lbs.</span></span>



