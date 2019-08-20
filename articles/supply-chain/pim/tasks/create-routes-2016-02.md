---
title: Vytvoření postupů (únor 2016)
description: Tato úloha je zaměřena na vytvoření výrobních postupů pro dokončený produkt a polotovar produktu.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, RouteInventProd, RouteGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5aa7db4ed66e7201d8d480d948a4249e43febde7
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844554"
---
# <a name="create-routes-february-2016"></a><span data-ttu-id="0e01e-103">Vytvoření postupů (únor 2016)</span><span class="sxs-lookup"><span data-stu-id="0e01e-103">Create routes (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0e01e-104">Tato úloha je zaměřena na vytvoření výrobních postupů pro dokončený produkt a polotovar produktu.</span><span class="sxs-lookup"><span data-stu-id="0e01e-104">This task focuses on creating the production routes for a finished product and a semi-finished product.</span></span> <span data-ttu-id="0e01e-105">Je to pátá úloha v řadě Kalkulace kusovníku.</span><span class="sxs-lookup"><span data-stu-id="0e01e-105">It is the fifth task in the BOM calculation series.</span></span> <span data-ttu-id="0e01e-106">Tento úkol byl vytvořen pomocí ukázkových dat společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="0e01e-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-route-for-a-semi-finished-product"></a><span data-ttu-id="0e01e-107">Vytvoření postupu pro polotovar produktu</span><span class="sxs-lookup"><span data-stu-id="0e01e-107">Create a route for a semi-finished product</span></span>
1. <span data-ttu-id="0e01e-108">Přejděte na možnosti Řízení informací o produktech > Produkty > Uvolněné produkty.</span><span class="sxs-lookup"><span data-stu-id="0e01e-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="0e01e-109">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="0e01e-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="0e01e-110">Vyberte číslo položky BOM_2.</span><span class="sxs-lookup"><span data-stu-id="0e01e-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="0e01e-111">V podokně akcí klikněte na možnost Analýza.</span><span class="sxs-lookup"><span data-stu-id="0e01e-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="0e01e-112">Klikněte na Postup.</span><span class="sxs-lookup"><span data-stu-id="0e01e-112">Click Route.</span></span>
5. <span data-ttu-id="0e01e-113">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="0e01e-113">Click New.</span></span>
6. <span data-ttu-id="0e01e-114">Klikněte na Postup a verze postupu.</span><span class="sxs-lookup"><span data-stu-id="0e01e-114">Click Route and route version.</span></span>
7. <span data-ttu-id="0e01e-115">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="0e01e-115">In the Description field, type a value.</span></span>
    * <span data-ttu-id="0e01e-116">Zadejte například ROUTE_2.</span><span class="sxs-lookup"><span data-stu-id="0e01e-116">For example, type ROUTE_2.</span></span>  
8. <span data-ttu-id="0e01e-117">V poli Lokalita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="0e01e-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="0e01e-118">V tomto příkladu zadejte nebo vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="0e01e-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="0e01e-119">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="0e01e-119">Click OK.</span></span>
10. <span data-ttu-id="0e01e-120">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="0e01e-120">Click New.</span></span>
11. <span data-ttu-id="0e01e-121">V poli Operace zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="0e01e-121">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="0e01e-122">V tomto příkladu vyberte Sestavení.</span><span class="sxs-lookup"><span data-stu-id="0e01e-122">For this example, select Assembly.</span></span>  
12. <span data-ttu-id="0e01e-123">Do pole Operační čas zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="0e01e-123">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="0e01e-124">Zadejte například 1.</span><span class="sxs-lookup"><span data-stu-id="0e01e-124">For example, type 1.</span></span> <span data-ttu-id="0e01e-125">Operační časy jsou často zahrnuté v ceně vypočtené pro položku.</span><span class="sxs-lookup"><span data-stu-id="0e01e-125">Run times are often part of the price that is calculated for an item.</span></span>  
13. <span data-ttu-id="0e01e-126">V poli Skupina postupů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="0e01e-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="0e01e-127">V tomto příkladu vyberte Std.</span><span class="sxs-lookup"><span data-stu-id="0e01e-127">For this example, select Std.</span></span>  
14. <span data-ttu-id="0e01e-128">Klikněte na záložku Nastavení.</span><span class="sxs-lookup"><span data-stu-id="0e01e-128">Click the Setup tab.</span></span>
15. <span data-ttu-id="0e01e-129">V poli Kategorie nastavení zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="0e01e-129">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="0e01e-130">V tomto příkladu vyberte Sestavení.</span><span class="sxs-lookup"><span data-stu-id="0e01e-130">For this example, select Assembly.</span></span>  
16. <span data-ttu-id="0e01e-131">Klepněte na kartu Časy.</span><span class="sxs-lookup"><span data-stu-id="0e01e-131">Click the Times tab.</span></span>
17. <span data-ttu-id="0e01e-132">Do pole Přípravný čas zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="0e01e-132">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="0e01e-133">V tomto příkladu zadejte 1.</span><span class="sxs-lookup"><span data-stu-id="0e01e-133">For this example, type 1.</span></span> <span data-ttu-id="0e01e-134">Přípravný čas je často zahrnutý v ceně vypočtené pro položku.</span><span class="sxs-lookup"><span data-stu-id="0e01e-134">Setup times are often part of the price that is calculated for an item.</span></span>  
18. <span data-ttu-id="0e01e-135">V podokně akcí klikněte na možnost Verze postupu.</span><span class="sxs-lookup"><span data-stu-id="0e01e-135">On the Action Pane, click Route version.</span></span>
19. <span data-ttu-id="0e01e-136">Klepněte na možnost Schválit.</span><span class="sxs-lookup"><span data-stu-id="0e01e-136">Click Approve.</span></span>
20. <span data-ttu-id="0e01e-137">Vyberte Ano v poli Chcete postup také schválit? .</span><span class="sxs-lookup"><span data-stu-id="0e01e-137">Select Yes in the Do you also want to approve the route? field.</span></span>
21. <span data-ttu-id="0e01e-138">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="0e01e-138">Click OK.</span></span>
22. <span data-ttu-id="0e01e-139">V podokně akcí klikněte na možnost Verze postupu.</span><span class="sxs-lookup"><span data-stu-id="0e01e-139">On the Action Pane, click Route version.</span></span>
23. <span data-ttu-id="0e01e-140">Klepněte na tlačítko Aktivovat.</span><span class="sxs-lookup"><span data-stu-id="0e01e-140">Click Activate.</span></span>
24. <span data-ttu-id="0e01e-141">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="0e01e-141">Close the page.</span></span>
25. <span data-ttu-id="0e01e-142">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="0e01e-142">Close the page.</span></span>

## <a name="create-a-route-for-a-finished-product"></a><span data-ttu-id="0e01e-143">Vytvoření postupu pro dokončený produkt</span><span class="sxs-lookup"><span data-stu-id="0e01e-143">Create a route for a finished product</span></span>
1. <span data-ttu-id="0e01e-144">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="0e01e-144">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="0e01e-145">Vyberte číslo položky BOM_1.</span><span class="sxs-lookup"><span data-stu-id="0e01e-145">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="0e01e-146">V podokně akcí klikněte na možnost Analýza.</span><span class="sxs-lookup"><span data-stu-id="0e01e-146">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="0e01e-147">Klikněte na Postup.</span><span class="sxs-lookup"><span data-stu-id="0e01e-147">Click Route.</span></span>
4. <span data-ttu-id="0e01e-148">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="0e01e-148">Click New.</span></span>
5. <span data-ttu-id="0e01e-149">Klikněte na Postup a verze postupu.</span><span class="sxs-lookup"><span data-stu-id="0e01e-149">Click Route and route version.</span></span>
6. <span data-ttu-id="0e01e-150">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="0e01e-150">In the Description field, type a value.</span></span>
    * <span data-ttu-id="0e01e-151">Pro tento příklad zadejte ROUTE_1.</span><span class="sxs-lookup"><span data-stu-id="0e01e-151">For this example, type ROUTE_1.</span></span>  
7. <span data-ttu-id="0e01e-152">V poli Lokalita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="0e01e-152">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="0e01e-153">V tomto příkladu zadejte nebo vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="0e01e-153">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="0e01e-154">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="0e01e-154">Click OK.</span></span>
9. <span data-ttu-id="0e01e-155">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="0e01e-155">Click New.</span></span>
10. <span data-ttu-id="0e01e-156">V poli Operace zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="0e01e-156">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="0e01e-157">V tomto příkladu vyberte Balení.</span><span class="sxs-lookup"><span data-stu-id="0e01e-157">For this example, select Packing.</span></span>  
11. <span data-ttu-id="0e01e-158">Do pole Operační čas zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="0e01e-158">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="0e01e-159">V tomto příkladu zadejte 1.</span><span class="sxs-lookup"><span data-stu-id="0e01e-159">For this example, type 1.</span></span>  
12. <span data-ttu-id="0e01e-160">V poli Skupina postupů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="0e01e-160">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="0e01e-161">V tomto příkladu vyberte Std.</span><span class="sxs-lookup"><span data-stu-id="0e01e-161">For this example, select Std.</span></span>  
13. <span data-ttu-id="0e01e-162">Klikněte na záložku Nastavení.</span><span class="sxs-lookup"><span data-stu-id="0e01e-162">Click the Setup tab.</span></span>
14. <span data-ttu-id="0e01e-163">V poli Kategorie nastavení zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="0e01e-163">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="0e01e-164">V tomto příkladu vyberte Balení.</span><span class="sxs-lookup"><span data-stu-id="0e01e-164">For this example, select Packing.</span></span>  
15. <span data-ttu-id="0e01e-165">Klepněte na kartu Časy.</span><span class="sxs-lookup"><span data-stu-id="0e01e-165">Click the Times tab.</span></span>
16. <span data-ttu-id="0e01e-166">Do pole Přípravný čas zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="0e01e-166">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="0e01e-167">V tomto příkladu zadejte 1.</span><span class="sxs-lookup"><span data-stu-id="0e01e-167">For this example, type 1.</span></span>  
17. <span data-ttu-id="0e01e-168">V podokně akcí klikněte na možnost Verze postupu.</span><span class="sxs-lookup"><span data-stu-id="0e01e-168">On the Action Pane, click Route version.</span></span>
18. <span data-ttu-id="0e01e-169">Klepněte na možnost Schválit.</span><span class="sxs-lookup"><span data-stu-id="0e01e-169">Click Approve.</span></span>
19. <span data-ttu-id="0e01e-170">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="0e01e-170">Click OK.</span></span>
20. <span data-ttu-id="0e01e-171">V podokně akcí klikněte na možnost Verze postupu.</span><span class="sxs-lookup"><span data-stu-id="0e01e-171">On the Action Pane, click Route version.</span></span>
21. <span data-ttu-id="0e01e-172">Klepněte na tlačítko Aktivovat.</span><span class="sxs-lookup"><span data-stu-id="0e01e-172">Click Activate.</span></span>
22. <span data-ttu-id="0e01e-173">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="0e01e-173">Close the page.</span></span>
23. <span data-ttu-id="0e01e-174">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="0e01e-174">Close the page.</span></span>

## <a name="enable-automatic-consumption-of-setup-time"></a><span data-ttu-id="0e01e-175">Aktivace automatické spotřeby přípravného času</span><span class="sxs-lookup"><span data-stu-id="0e01e-175">Enable automatic consumption of setup time</span></span>
1. <span data-ttu-id="0e01e-176">Přejděte k Řízení výroby > Nastavení > Postupy > Skupiny postupu.</span><span class="sxs-lookup"><span data-stu-id="0e01e-176">Go to Production control > Setup > Routes > Route groups.</span></span>
2. <span data-ttu-id="0e01e-177">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="0e01e-177">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0e01e-178">V seznamu vyberte položku Std.</span><span class="sxs-lookup"><span data-stu-id="0e01e-178">Select Std in the list.</span></span>  
3. <span data-ttu-id="0e01e-179">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="0e01e-179">Click Edit.</span></span>
4. <span data-ttu-id="0e01e-180">Vyberte Ano v poli Přípravný čas.</span><span class="sxs-lookup"><span data-stu-id="0e01e-180">Select Yes in the Setup time field.</span></span>
    * <span data-ttu-id="0e01e-181">Přípravný čas je často zahrnutý v ceně vypočtené pro položku.</span><span class="sxs-lookup"><span data-stu-id="0e01e-181">Setup times are often part of the price that is calculated for an item.</span></span>  
5. <span data-ttu-id="0e01e-182">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="0e01e-182">Click Save.</span></span>
6. <span data-ttu-id="0e01e-183">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="0e01e-183">Close the page.</span></span>

