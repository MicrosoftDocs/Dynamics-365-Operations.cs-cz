--- 
title: "Vytvoření postupů (únor 2016)"
description: "Tato úloha je zaměřena na vytvoření výrobních postupů pro dokončený produkt a polotovar produktu."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, RouteInventProd, RouteGroup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 965826f5fddc2f53f33157434929eb265979376e
ms.openlocfilehash: a68b28c0e0ee14429a23d3241cabdae948d706d2
ms.contentlocale: cs-cz
ms.lasthandoff: 09/17/2018

---
# <a name="create-routes-february-2016"></a><span data-ttu-id="e860d-103">Vytvoření postupů (únor 2016)</span><span class="sxs-lookup"><span data-stu-id="e860d-103">Create routes (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e860d-104">Tato úloha je zaměřena na vytvoření výrobních postupů pro dokončený produkt a polotovar produktu.</span><span class="sxs-lookup"><span data-stu-id="e860d-104">This task focuses on creating the production routes for a finished product and a semi-finished product.</span></span> <span data-ttu-id="e860d-105">Je to pátá úloha v řadě Kalkulace kusovníku.</span><span class="sxs-lookup"><span data-stu-id="e860d-105">It is the fifth task in the BOM calculation series.</span></span> <span data-ttu-id="e860d-106">Tento úkol byl vytvořen pomocí ukázkových dat společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="e860d-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-route-for-a-semi-finished-product"></a><span data-ttu-id="e860d-107">Vytvoření postupu pro polotovar produktu</span><span class="sxs-lookup"><span data-stu-id="e860d-107">Create a route for a semi-finished product</span></span>
1. <span data-ttu-id="e860d-108">Přejděte na možnosti Řízení informací o produktech > Produkty > Uvolněné produkty.</span><span class="sxs-lookup"><span data-stu-id="e860d-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="e860d-109">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="e860d-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e860d-110">Vyberte číslo položky BOM_2.</span><span class="sxs-lookup"><span data-stu-id="e860d-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="e860d-111">V podokně akcí klikněte na možnost Analýza.</span><span class="sxs-lookup"><span data-stu-id="e860d-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="e860d-112">Klikněte na Postup.</span><span class="sxs-lookup"><span data-stu-id="e860d-112">Click Route.</span></span>
5. <span data-ttu-id="e860d-113">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="e860d-113">Click New.</span></span>
6. <span data-ttu-id="e860d-114">Klikněte na Postup a verze postupu.</span><span class="sxs-lookup"><span data-stu-id="e860d-114">Click Route and route version.</span></span>
7. <span data-ttu-id="e860d-115">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="e860d-115">In the Description field, type a value.</span></span>
    * <span data-ttu-id="e860d-116">Zadejte například ROUTE_2.</span><span class="sxs-lookup"><span data-stu-id="e860d-116">For example, type ROUTE_2.</span></span>  
8. <span data-ttu-id="e860d-117">V poli Lokalita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e860d-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="e860d-118">V tomto příkladu zadejte nebo vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="e860d-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="e860d-119">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="e860d-119">Click OK.</span></span>
10. <span data-ttu-id="e860d-120">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="e860d-120">Click New.</span></span>
11. <span data-ttu-id="e860d-121">V poli Operace zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e860d-121">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="e860d-122">V tomto příkladu vyberte Sestavení.</span><span class="sxs-lookup"><span data-stu-id="e860d-122">For this example, select Assembly.</span></span>  
12. <span data-ttu-id="e860d-123">Do pole Operační čas zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="e860d-123">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="e860d-124">Zadejte například 1.</span><span class="sxs-lookup"><span data-stu-id="e860d-124">For example, type 1.</span></span> <span data-ttu-id="e860d-125">Operační časy jsou často zahrnuté v ceně vypočtené pro položku.</span><span class="sxs-lookup"><span data-stu-id="e860d-125">Run times are often part of the price that is calculated for an item.</span></span>  
13. <span data-ttu-id="e860d-126">V poli Skupina postupů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e860d-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="e860d-127">V tomto příkladu vyberte Std.</span><span class="sxs-lookup"><span data-stu-id="e860d-127">For this example, select Std.</span></span>  
14. <span data-ttu-id="e860d-128">Klikněte na záložku Nastavení.</span><span class="sxs-lookup"><span data-stu-id="e860d-128">Click the Setup tab.</span></span>
15. <span data-ttu-id="e860d-129">V poli Kategorie nastavení zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e860d-129">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="e860d-130">V tomto příkladu vyberte Sestavení.</span><span class="sxs-lookup"><span data-stu-id="e860d-130">For this example, select Assembly.</span></span>  
16. <span data-ttu-id="e860d-131">Klepněte na kartu Časy.</span><span class="sxs-lookup"><span data-stu-id="e860d-131">Click the Times tab.</span></span>
17. <span data-ttu-id="e860d-132">Do pole Přípravný čas zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="e860d-132">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="e860d-133">V tomto příkladu zadejte 1.</span><span class="sxs-lookup"><span data-stu-id="e860d-133">For this example, type 1.</span></span> <span data-ttu-id="e860d-134">Přípravný čas je často zahrnutý v ceně vypočtené pro položku.</span><span class="sxs-lookup"><span data-stu-id="e860d-134">Setup times are often part of the price that is calculated for an item.</span></span>  
18. <span data-ttu-id="e860d-135">V podokně akcí klikněte na možnost Verze postupu.</span><span class="sxs-lookup"><span data-stu-id="e860d-135">On the Action Pane, click Route version.</span></span>
19. <span data-ttu-id="e860d-136">Klepněte na možnost Schválit.</span><span class="sxs-lookup"><span data-stu-id="e860d-136">Click Approve.</span></span>
20. <span data-ttu-id="e860d-137">Vyberte Ano v poli Chcete postup také schválit? .</span><span class="sxs-lookup"><span data-stu-id="e860d-137">Select Yes in the Do you also want to approve the route? field.</span></span>
21. <span data-ttu-id="e860d-138">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="e860d-138">Click OK.</span></span>
22. <span data-ttu-id="e860d-139">V podokně akcí klikněte na možnost Verze postupu.</span><span class="sxs-lookup"><span data-stu-id="e860d-139">On the Action Pane, click Route version.</span></span>
23. <span data-ttu-id="e860d-140">Klepněte na tlačítko Aktivovat.</span><span class="sxs-lookup"><span data-stu-id="e860d-140">Click Activate.</span></span>
24. <span data-ttu-id="e860d-141">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="e860d-141">Close the page.</span></span>
25. <span data-ttu-id="e860d-142">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="e860d-142">Close the page.</span></span>

## <a name="create-a-route-for-a-finished-product"></a><span data-ttu-id="e860d-143">Vytvoření postupu pro dokončený produkt</span><span class="sxs-lookup"><span data-stu-id="e860d-143">Create a route for a finished product</span></span>
1. <span data-ttu-id="e860d-144">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="e860d-144">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e860d-145">Vyberte číslo položky BOM_1.</span><span class="sxs-lookup"><span data-stu-id="e860d-145">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="e860d-146">V podokně akcí klikněte na možnost Analýza.</span><span class="sxs-lookup"><span data-stu-id="e860d-146">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="e860d-147">Klikněte na Postup.</span><span class="sxs-lookup"><span data-stu-id="e860d-147">Click Route.</span></span>
4. <span data-ttu-id="e860d-148">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="e860d-148">Click New.</span></span>
5. <span data-ttu-id="e860d-149">Klikněte na Postup a verze postupu.</span><span class="sxs-lookup"><span data-stu-id="e860d-149">Click Route and route version.</span></span>
6. <span data-ttu-id="e860d-150">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="e860d-150">In the Description field, type a value.</span></span>
    * <span data-ttu-id="e860d-151">Pro tento příklad zadejte ROUTE_1.</span><span class="sxs-lookup"><span data-stu-id="e860d-151">For this example, type ROUTE_1.</span></span>  
7. <span data-ttu-id="e860d-152">V poli Lokalita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e860d-152">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="e860d-153">V tomto příkladu zadejte nebo vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="e860d-153">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="e860d-154">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="e860d-154">Click OK.</span></span>
9. <span data-ttu-id="e860d-155">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="e860d-155">Click New.</span></span>
10. <span data-ttu-id="e860d-156">V poli Operace zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e860d-156">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="e860d-157">V tomto příkladu vyberte Balení.</span><span class="sxs-lookup"><span data-stu-id="e860d-157">For this example, select Packing.</span></span>  
11. <span data-ttu-id="e860d-158">Do pole Operační čas zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="e860d-158">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="e860d-159">V tomto příkladu zadejte 1.</span><span class="sxs-lookup"><span data-stu-id="e860d-159">For this example, type 1.</span></span>  
12. <span data-ttu-id="e860d-160">V poli Skupina postupů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e860d-160">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="e860d-161">V tomto příkladu vyberte Std.</span><span class="sxs-lookup"><span data-stu-id="e860d-161">For this example, select Std.</span></span>  
13. <span data-ttu-id="e860d-162">Klikněte na záložku Nastavení.</span><span class="sxs-lookup"><span data-stu-id="e860d-162">Click the Setup tab.</span></span>
14. <span data-ttu-id="e860d-163">V poli Kategorie nastavení zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="e860d-163">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="e860d-164">V tomto příkladu vyberte Balení.</span><span class="sxs-lookup"><span data-stu-id="e860d-164">For this example, select Packing.</span></span>  
15. <span data-ttu-id="e860d-165">Klepněte na kartu Časy.</span><span class="sxs-lookup"><span data-stu-id="e860d-165">Click the Times tab.</span></span>
16. <span data-ttu-id="e860d-166">Do pole Přípravný čas zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="e860d-166">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="e860d-167">V tomto příkladu zadejte 1.</span><span class="sxs-lookup"><span data-stu-id="e860d-167">For this example, type 1.</span></span>  
17. <span data-ttu-id="e860d-168">V podokně akcí klikněte na možnost Verze postupu.</span><span class="sxs-lookup"><span data-stu-id="e860d-168">On the Action Pane, click Route version.</span></span>
18. <span data-ttu-id="e860d-169">Klepněte na možnost Schválit.</span><span class="sxs-lookup"><span data-stu-id="e860d-169">Click Approve.</span></span>
19. <span data-ttu-id="e860d-170">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="e860d-170">Click OK.</span></span>
20. <span data-ttu-id="e860d-171">V podokně akcí klikněte na možnost Verze postupu.</span><span class="sxs-lookup"><span data-stu-id="e860d-171">On the Action Pane, click Route version.</span></span>
21. <span data-ttu-id="e860d-172">Klepněte na tlačítko Aktivovat.</span><span class="sxs-lookup"><span data-stu-id="e860d-172">Click Activate.</span></span>
22. <span data-ttu-id="e860d-173">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="e860d-173">Close the page.</span></span>
23. <span data-ttu-id="e860d-174">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="e860d-174">Close the page.</span></span>

## <a name="enable-automatic-consumption-of-setup-time"></a><span data-ttu-id="e860d-175">Aktivace automatické spotřeby přípravného času</span><span class="sxs-lookup"><span data-stu-id="e860d-175">Enable automatic consumption of setup time</span></span>
1. <span data-ttu-id="e860d-176">Přejděte k Řízení výroby > Nastavení > Postupy > Skupiny postupu.</span><span class="sxs-lookup"><span data-stu-id="e860d-176">Go to Production control > Setup > Routes > Route groups.</span></span>
2. <span data-ttu-id="e860d-177">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="e860d-177">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e860d-178">V seznamu vyberte položku Std.</span><span class="sxs-lookup"><span data-stu-id="e860d-178">Select Std in the list.</span></span>  
3. <span data-ttu-id="e860d-179">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="e860d-179">Click Edit.</span></span>
4. <span data-ttu-id="e860d-180">Vyberte Ano v poli Přípravný čas.</span><span class="sxs-lookup"><span data-stu-id="e860d-180">Select Yes in the Setup time field.</span></span>
    * <span data-ttu-id="e860d-181">Přípravný čas je často zahrnutý v ceně vypočtené pro položku.</span><span class="sxs-lookup"><span data-stu-id="e860d-181">Setup times are often part of the price that is calculated for an item.</span></span>  
5. <span data-ttu-id="e860d-182">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="e860d-182">Click Save.</span></span>
6. <span data-ttu-id="e860d-183">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="e860d-183">Close the page.</span></span>


