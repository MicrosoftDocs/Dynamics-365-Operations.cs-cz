--- 
title: "Vytváření postupů (jen ve verzi z února 2016)"
description: "Tato úloha je zaměřena na vytvoření výrobních postupů pro dokončený produkt a polotovar produktu."
author: YuyuScheller
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 002d0b72322c6a02fe1fcdbe6392fdb6c5c88747
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---
# <a name="create-routes-february-2016-only"></a><span data-ttu-id="ef06a-103">Vytváření postupů (jen ve verzi z února 2016)</span><span class="sxs-lookup"><span data-stu-id="ef06a-103">Create routes (February 2016 only)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ef06a-104">Tato úloha je zaměřena na vytvoření výrobních postupů pro dokončený produkt a polotovar produktu.</span><span class="sxs-lookup"><span data-stu-id="ef06a-104">This task focuses on creating the production routes for a finished product and a semi-finished product.</span></span> <span data-ttu-id="ef06a-105">Je to pátá úloha v řadě Kalkulace kusovníku.</span><span class="sxs-lookup"><span data-stu-id="ef06a-105">It is the fifth task in the BOM calculation series.</span></span> <span data-ttu-id="ef06a-106">Tento úkol byl vytvořen pomocí ukázkových dat společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="ef06a-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-route-for-a-semi-finished-product"></a><span data-ttu-id="ef06a-107">Vytvoření postupu pro polotovar produktu</span><span class="sxs-lookup"><span data-stu-id="ef06a-107">Create a route for a semi-finished product</span></span>
1. <span data-ttu-id="ef06a-108">Přejděte na možnosti Řízení informací o produktech > Produkty > Uvolněné produkty.</span><span class="sxs-lookup"><span data-stu-id="ef06a-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="ef06a-109">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="ef06a-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ef06a-110">Vyberte číslo položky BOM_2.</span><span class="sxs-lookup"><span data-stu-id="ef06a-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="ef06a-111">V podokně akcí klikněte na možnost Analýza.</span><span class="sxs-lookup"><span data-stu-id="ef06a-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="ef06a-112">Klikněte na Postup.</span><span class="sxs-lookup"><span data-stu-id="ef06a-112">Click Route.</span></span>
5. <span data-ttu-id="ef06a-113">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="ef06a-113">Click New.</span></span>
6. <span data-ttu-id="ef06a-114">Klikněte na Postup a verze postupu.</span><span class="sxs-lookup"><span data-stu-id="ef06a-114">Click Route and route version.</span></span>
7. <span data-ttu-id="ef06a-115">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="ef06a-115">In the Description field, type a value.</span></span>
    * <span data-ttu-id="ef06a-116">Zadejte například ROUTE_2.</span><span class="sxs-lookup"><span data-stu-id="ef06a-116">For example, type ROUTE_2.</span></span>  
8. <span data-ttu-id="ef06a-117">V poli Lokalita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ef06a-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="ef06a-118">V tomto příkladu zadejte nebo vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="ef06a-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="ef06a-119">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="ef06a-119">Click OK.</span></span>
10. <span data-ttu-id="ef06a-120">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="ef06a-120">Click New.</span></span>
11. <span data-ttu-id="ef06a-121">V poli Operace zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ef06a-121">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="ef06a-122">V tomto příkladu vyberte Sestavení.</span><span class="sxs-lookup"><span data-stu-id="ef06a-122">For this example, select Assembly.</span></span>  
12. <span data-ttu-id="ef06a-123">Do pole Operační čas zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="ef06a-123">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="ef06a-124">Zadejte například 1.</span><span class="sxs-lookup"><span data-stu-id="ef06a-124">For example, type 1.</span></span> <span data-ttu-id="ef06a-125">Operační časy jsou často zahrnuté v ceně vypočtené pro položku.</span><span class="sxs-lookup"><span data-stu-id="ef06a-125">Run times are often part of the price that is calculated for an item.</span></span>  
13. <span data-ttu-id="ef06a-126">V poli Skupina postupů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ef06a-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="ef06a-127">V tomto příkladu vyberte Std.</span><span class="sxs-lookup"><span data-stu-id="ef06a-127">For this example, select Std.</span></span>  
14. <span data-ttu-id="ef06a-128">Klikněte na záložku Nastavení.</span><span class="sxs-lookup"><span data-stu-id="ef06a-128">Click the Setup tab.</span></span>
15. <span data-ttu-id="ef06a-129">V poli Kategorie nastavení zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ef06a-129">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="ef06a-130">V tomto příkladu vyberte Sestavení.</span><span class="sxs-lookup"><span data-stu-id="ef06a-130">For this example, select Assembly.</span></span>  
16. <span data-ttu-id="ef06a-131">Klepněte na kartu Časy.</span><span class="sxs-lookup"><span data-stu-id="ef06a-131">Click the Times tab.</span></span>
17. <span data-ttu-id="ef06a-132">Do pole Přípravný čas zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="ef06a-132">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="ef06a-133">V tomto příkladu zadejte 1.</span><span class="sxs-lookup"><span data-stu-id="ef06a-133">For this example, type 1.</span></span> <span data-ttu-id="ef06a-134">Přípravný čas je často zahrnutý v ceně vypočtené pro položku.</span><span class="sxs-lookup"><span data-stu-id="ef06a-134">Setup times are often part of the price that is calculated for an item.</span></span>  
18. <span data-ttu-id="ef06a-135">V podokně akcí klikněte na možnost Verze postupu.</span><span class="sxs-lookup"><span data-stu-id="ef06a-135">On the Action Pane, click Route version.</span></span>
19. <span data-ttu-id="ef06a-136">Klepněte na možnost Schválit.</span><span class="sxs-lookup"><span data-stu-id="ef06a-136">Click Approve.</span></span>
20. <span data-ttu-id="ef06a-137">Vyberte Ano v poli Chcete postup také schválit? .</span><span class="sxs-lookup"><span data-stu-id="ef06a-137">Select Yes in the Do you also want to approve the route? field.</span></span>
21. <span data-ttu-id="ef06a-138">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="ef06a-138">Click OK.</span></span>
22. <span data-ttu-id="ef06a-139">V podokně akcí klikněte na možnost Verze postupu.</span><span class="sxs-lookup"><span data-stu-id="ef06a-139">On the Action Pane, click Route version.</span></span>
23. <span data-ttu-id="ef06a-140">Klepněte na tlačítko Aktivovat.</span><span class="sxs-lookup"><span data-stu-id="ef06a-140">Click Activate.</span></span>
24. <span data-ttu-id="ef06a-141">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ef06a-141">Close the page.</span></span>
25. <span data-ttu-id="ef06a-142">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ef06a-142">Close the page.</span></span>

## <a name="create-a-route-for-a-finished-product"></a><span data-ttu-id="ef06a-143">Vytvoření postupu pro dokončený produkt</span><span class="sxs-lookup"><span data-stu-id="ef06a-143">Create a route for a finished product</span></span>
1. <span data-ttu-id="ef06a-144">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="ef06a-144">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ef06a-145">Vyberte číslo položky BOM_1.</span><span class="sxs-lookup"><span data-stu-id="ef06a-145">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="ef06a-146">V podokně akcí klikněte na možnost Analýza.</span><span class="sxs-lookup"><span data-stu-id="ef06a-146">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="ef06a-147">Klikněte na Postup.</span><span class="sxs-lookup"><span data-stu-id="ef06a-147">Click Route.</span></span>
4. <span data-ttu-id="ef06a-148">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="ef06a-148">Click New.</span></span>
5. <span data-ttu-id="ef06a-149">Klikněte na Postup a verze postupu.</span><span class="sxs-lookup"><span data-stu-id="ef06a-149">Click Route and route version.</span></span>
6. <span data-ttu-id="ef06a-150">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="ef06a-150">In the Description field, type a value.</span></span>
    * <span data-ttu-id="ef06a-151">Pro tento příklad zadejte ROUTE_1.</span><span class="sxs-lookup"><span data-stu-id="ef06a-151">For this example, type ROUTE_1.</span></span>  
7. <span data-ttu-id="ef06a-152">V poli Lokalita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ef06a-152">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="ef06a-153">V tomto příkladu zadejte nebo vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="ef06a-153">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="ef06a-154">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="ef06a-154">Click OK.</span></span>
9. <span data-ttu-id="ef06a-155">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="ef06a-155">Click New.</span></span>
10. <span data-ttu-id="ef06a-156">V poli Operace zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ef06a-156">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="ef06a-157">V tomto příkladu vyberte Balení.</span><span class="sxs-lookup"><span data-stu-id="ef06a-157">For this example, select Packing.</span></span>  
11. <span data-ttu-id="ef06a-158">Do pole Operační čas zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="ef06a-158">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="ef06a-159">V tomto příkladu zadejte 1.</span><span class="sxs-lookup"><span data-stu-id="ef06a-159">For this example, type 1.</span></span>  
12. <span data-ttu-id="ef06a-160">V poli Skupina postupů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ef06a-160">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="ef06a-161">V tomto příkladu vyberte Std.</span><span class="sxs-lookup"><span data-stu-id="ef06a-161">For this example, select Std.</span></span>  
13. <span data-ttu-id="ef06a-162">Klikněte na záložku Nastavení.</span><span class="sxs-lookup"><span data-stu-id="ef06a-162">Click the Setup tab.</span></span>
14. <span data-ttu-id="ef06a-163">V poli Kategorie nastavení zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ef06a-163">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="ef06a-164">V tomto příkladu vyberte Balení.</span><span class="sxs-lookup"><span data-stu-id="ef06a-164">For this example, select Packing.</span></span>  
15. <span data-ttu-id="ef06a-165">Klepněte na kartu Časy.</span><span class="sxs-lookup"><span data-stu-id="ef06a-165">Click the Times tab.</span></span>
16. <span data-ttu-id="ef06a-166">Do pole Přípravný čas zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="ef06a-166">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="ef06a-167">V tomto příkladu zadejte 1.</span><span class="sxs-lookup"><span data-stu-id="ef06a-167">For this example, type 1.</span></span>  
17. <span data-ttu-id="ef06a-168">V podokně akcí klikněte na možnost Verze postupu.</span><span class="sxs-lookup"><span data-stu-id="ef06a-168">On the Action Pane, click Route version.</span></span>
18. <span data-ttu-id="ef06a-169">Klepněte na možnost Schválit.</span><span class="sxs-lookup"><span data-stu-id="ef06a-169">Click Approve.</span></span>
19. <span data-ttu-id="ef06a-170">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="ef06a-170">Click OK.</span></span>
20. <span data-ttu-id="ef06a-171">V podokně akcí klikněte na možnost Verze postupu.</span><span class="sxs-lookup"><span data-stu-id="ef06a-171">On the Action Pane, click Route version.</span></span>
21. <span data-ttu-id="ef06a-172">Klepněte na tlačítko Aktivovat.</span><span class="sxs-lookup"><span data-stu-id="ef06a-172">Click Activate.</span></span>
22. <span data-ttu-id="ef06a-173">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ef06a-173">Close the page.</span></span>
23. <span data-ttu-id="ef06a-174">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ef06a-174">Close the page.</span></span>

## <a name="enable-automatic-consumption-of-setup-time"></a><span data-ttu-id="ef06a-175">Aktivace automatické spotřeby přípravného času</span><span class="sxs-lookup"><span data-stu-id="ef06a-175">Enable automatic consumption of setup time</span></span>
1. <span data-ttu-id="ef06a-176">Přejděte k Řízení výroby > Nastavení > Postupy > Skupiny postupu.</span><span class="sxs-lookup"><span data-stu-id="ef06a-176">Go to Production control > Setup > Routes > Route groups.</span></span>
2. <span data-ttu-id="ef06a-177">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="ef06a-177">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ef06a-178">V seznamu vyberte položku Std.</span><span class="sxs-lookup"><span data-stu-id="ef06a-178">Select Std in the list.</span></span>  
3. <span data-ttu-id="ef06a-179">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="ef06a-179">Click Edit.</span></span>
4. <span data-ttu-id="ef06a-180">Vyberte Ano v poli Přípravný čas.</span><span class="sxs-lookup"><span data-stu-id="ef06a-180">Select Yes in the Setup time field.</span></span>
    * <span data-ttu-id="ef06a-181">Přípravný čas je často zahrnutý v ceně vypočtené pro položku.</span><span class="sxs-lookup"><span data-stu-id="ef06a-181">Setup times are often part of the price that is calculated for an item.</span></span>  
5. <span data-ttu-id="ef06a-182">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="ef06a-182">Click Save.</span></span>
6. <span data-ttu-id="ef06a-183">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ef06a-183">Close the page.</span></span>


