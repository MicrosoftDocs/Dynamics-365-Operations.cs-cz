--- 
title: "Vytváření surovin (je ve verzi z února 2016)"
description: "Tato úloha je zaměřena na vytvoření komponent dokončených produktů a polotovarů produktů."
author: YuyuScheller
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3d77dcc20fe7402af83dd724e7fef848977e5bf8
ms.openlocfilehash: f6af7b93d8d1d9a6f7474f24177b16e5295e90d6
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="create-raw-materials-february-2016-only"></a><span data-ttu-id="be375-103">Vytváření surovin (je ve verzi z února 2016)</span><span class="sxs-lookup"><span data-stu-id="be375-103">Create raw materials (February 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="be375-104">Tato úloha je zaměřena na vytvoření komponent dokončených produktů a polotovarů produktů.</span><span class="sxs-lookup"><span data-stu-id="be375-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="be375-105">Je to třetí úloha v řadě Kalkulace kusovníku.</span><span class="sxs-lookup"><span data-stu-id="be375-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="be375-106">Tento úkol byl vytvořen pomocí ukázkových dat společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="be375-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="be375-107">Vytvoření prvního materiálu</span><span class="sxs-lookup"><span data-stu-id="be375-107">Create the first material</span></span>
1. <span data-ttu-id="be375-108">Přejděte na možnosti Řízení informací o produktech > Produkty > Uvolněné produkty.</span><span class="sxs-lookup"><span data-stu-id="be375-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="be375-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="be375-109">Click New.</span></span>
3. <span data-ttu-id="be375-110">Zadejte hodnotu do pole Číslo produktu.</span><span class="sxs-lookup"><span data-stu-id="be375-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="be375-111">V tomto příkladu zadejte ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="be375-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="be375-112">V poli Skupina modelů zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="be375-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="be375-113">Vyberte volbu „STD“.</span><span class="sxs-lookup"><span data-stu-id="be375-113">Select STD.</span></span> <span data-ttu-id="be375-114">STD zastupuje standardní náklady a je to nejčastěji používaný model při práci s výpočty nákladů.</span><span class="sxs-lookup"><span data-stu-id="be375-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="be375-115">V poli Skupina zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="be375-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="be375-116">Vyberte například Audio.</span><span class="sxs-lookup"><span data-stu-id="be375-116">For example, select Audio.</span></span> <span data-ttu-id="be375-117">To nemá žádný vliv na výpočty nákladů.</span><span class="sxs-lookup"><span data-stu-id="be375-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="be375-118">V poli Skupina dimenze úložiště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="be375-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="be375-119">Vyberte SiteWH.</span><span class="sxs-lookup"><span data-stu-id="be375-119">Select SiteWH.</span></span> <span data-ttu-id="be375-120">Pro ukázku se použije pouze Pracoviště a Sklad.</span><span class="sxs-lookup"><span data-stu-id="be375-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="be375-121">V poli Skupina sledovací dimenze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="be375-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="be375-122">Sledovací dimenze v tomto příkladu nebudou použity.</span><span class="sxs-lookup"><span data-stu-id="be375-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="be375-123">Zvolte Žádné.</span><span class="sxs-lookup"><span data-stu-id="be375-123">Select None.</span></span>  
8. <span data-ttu-id="be375-124">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="be375-124">Click OK.</span></span>
9. <span data-ttu-id="be375-125">V podokně akcí klikněte na možnost Spravovat sklad.</span><span class="sxs-lookup"><span data-stu-id="be375-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="be375-126">Klikněte na Výchozí nastavení objednávky.</span><span class="sxs-lookup"><span data-stu-id="be375-126">Click Default order settings.</span></span>
11. <span data-ttu-id="be375-127">V poli Nákupní pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="be375-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="be375-128">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="be375-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="be375-129">V poli Skladové pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="be375-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="be375-130">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="be375-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="be375-131">V poli Prodejní pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="be375-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="be375-132">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="be375-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="be375-133">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="be375-133">Close the page.</span></span>
15. <span data-ttu-id="be375-134">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="be375-134">Close the page.</span></span>
16. <span data-ttu-id="be375-135">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="be375-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="be375-136">Klikněte na ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="be375-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="be375-137">Rozbalte oblast Správa nákladů.</span><span class="sxs-lookup"><span data-stu-id="be375-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="be375-138">Zadejte hodnotu do pole Nákladová skupina.</span><span class="sxs-lookup"><span data-stu-id="be375-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="be375-139">V tomto příkladu zadejte M2.</span><span class="sxs-lookup"><span data-stu-id="be375-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="be375-140">V podokně akcí klikněte na možnost Spravovat náklady.</span><span class="sxs-lookup"><span data-stu-id="be375-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="be375-141">Klikněte na možnost Cena položky.</span><span class="sxs-lookup"><span data-stu-id="be375-141">Click Item price.</span></span>
21. <span data-ttu-id="be375-142">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="be375-142">Click New.</span></span>
22. <span data-ttu-id="be375-143">V poli Verze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="be375-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="be375-144">V tomto příkladu vyberte 10, což je typ výpočtu standardních nákladů.</span><span class="sxs-lookup"><span data-stu-id="be375-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="be375-145">V poli Lokalita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="be375-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="be375-146">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="be375-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="be375-147">Zadejte číslo do pole Cena.</span><span class="sxs-lookup"><span data-stu-id="be375-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="be375-148">V tomto příkladu zadejte 10.</span><span class="sxs-lookup"><span data-stu-id="be375-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="be375-149">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="be375-149">Click Save.</span></span>
26. <span data-ttu-id="be375-150">Klikněte na Aktivovat nezpracované ceny.</span><span class="sxs-lookup"><span data-stu-id="be375-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="be375-151">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="be375-151">Close the page.</span></span>
28. <span data-ttu-id="be375-152">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="be375-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="be375-153">Vytvoření druhého materiálu</span><span class="sxs-lookup"><span data-stu-id="be375-153">Create the second material</span></span>
1. <span data-ttu-id="be375-154">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="be375-154">Click New.</span></span>
2. <span data-ttu-id="be375-155">Zadejte hodnotu do pole Číslo produktu.</span><span class="sxs-lookup"><span data-stu-id="be375-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="be375-156">V tomto příkladu zadejte ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="be375-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="be375-157">V poli Skupina modelů zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="be375-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="be375-158">Vyberte volbu „STD“.</span><span class="sxs-lookup"><span data-stu-id="be375-158">Select STD.</span></span> <span data-ttu-id="be375-159">STD zastupuje standardní náklady a je to nejčastěji používaný model při práci s výpočty nákladů.</span><span class="sxs-lookup"><span data-stu-id="be375-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="be375-160">V poli Skupina zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="be375-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="be375-161">Vyberte například Audio.</span><span class="sxs-lookup"><span data-stu-id="be375-161">For example, select Audio.</span></span> <span data-ttu-id="be375-162">To nemá žádný vliv na výpočty nákladů.</span><span class="sxs-lookup"><span data-stu-id="be375-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="be375-163">V poli Skupina dimenze úložiště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="be375-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="be375-164">Vyberte SiteWH.</span><span class="sxs-lookup"><span data-stu-id="be375-164">Select SiteWH.</span></span> <span data-ttu-id="be375-165">Pro tento příklad se použije pouze Pracoviště a Sklad.</span><span class="sxs-lookup"><span data-stu-id="be375-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="be375-166">V poli Skupina sledovací dimenze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="be375-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="be375-167">Sledovací dimenze v tomto příkladu nebudou použity.</span><span class="sxs-lookup"><span data-stu-id="be375-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="be375-168">Zvolte Žádné.</span><span class="sxs-lookup"><span data-stu-id="be375-168">Select None.</span></span>  
7. <span data-ttu-id="be375-169">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="be375-169">Click OK.</span></span>
8. <span data-ttu-id="be375-170">V podokně akcí klikněte na možnost Spravovat sklad.</span><span class="sxs-lookup"><span data-stu-id="be375-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="be375-171">Klikněte na Výchozí nastavení objednávky.</span><span class="sxs-lookup"><span data-stu-id="be375-171">Click Default order settings.</span></span>
10. <span data-ttu-id="be375-172">V poli Nákupní pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="be375-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="be375-173">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="be375-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="be375-174">V poli Skladové pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="be375-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="be375-175">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="be375-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="be375-176">V poli Prodejní pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="be375-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="be375-177">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="be375-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="be375-178">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="be375-178">Close the page.</span></span>
14. <span data-ttu-id="be375-179">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="be375-179">Close the page.</span></span>
15. <span data-ttu-id="be375-180">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="be375-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="be375-181">Klikněte na ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="be375-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="be375-182">Rozbalte oblast Správa nákladů.</span><span class="sxs-lookup"><span data-stu-id="be375-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="be375-183">Zadejte hodnotu do pole Nákladová skupina.</span><span class="sxs-lookup"><span data-stu-id="be375-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="be375-184">V tomto příkladu zadejte M2.</span><span class="sxs-lookup"><span data-stu-id="be375-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="be375-185">V podokně akcí klikněte na možnost Spravovat náklady.</span><span class="sxs-lookup"><span data-stu-id="be375-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="be375-186">Klikněte na možnost Cena položky.</span><span class="sxs-lookup"><span data-stu-id="be375-186">Click Item price.</span></span>
20. <span data-ttu-id="be375-187">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="be375-187">Click New.</span></span>
21. <span data-ttu-id="be375-188">V poli Verze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="be375-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="be375-189">V tomto příkladu vyberte 10.</span><span class="sxs-lookup"><span data-stu-id="be375-189">For this example, select 10.</span></span> <span data-ttu-id="be375-190">Jedná se o typ výpočtu standardních nákladů.</span><span class="sxs-lookup"><span data-stu-id="be375-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="be375-191">V poli Lokalita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="be375-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="be375-192">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="be375-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="be375-193">Zadejte číslo do pole Cena.</span><span class="sxs-lookup"><span data-stu-id="be375-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="be375-194">Pro ukázku zadejte 10.</span><span class="sxs-lookup"><span data-stu-id="be375-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="be375-195">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="be375-195">Click Save.</span></span>
25. <span data-ttu-id="be375-196">Klikněte na Aktivovat nezpracované ceny.</span><span class="sxs-lookup"><span data-stu-id="be375-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="be375-197">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="be375-197">Close the page.</span></span>
27. <span data-ttu-id="be375-198">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="be375-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="be375-199">Vytvoření třetího materiálu</span><span class="sxs-lookup"><span data-stu-id="be375-199">Create the third material</span></span>
1. <span data-ttu-id="be375-200">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="be375-200">Click New.</span></span>
2. <span data-ttu-id="be375-201">Zadejte hodnotu do pole Číslo produktu.</span><span class="sxs-lookup"><span data-stu-id="be375-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="be375-202">Pro ukázku zadejte ITEM_C</span><span class="sxs-lookup"><span data-stu-id="be375-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="be375-203">V poli Skupina modelů zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="be375-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="be375-204">Vyberte volbu „STD“.</span><span class="sxs-lookup"><span data-stu-id="be375-204">Select STD.</span></span> <span data-ttu-id="be375-205">STD zastupuje standardní náklady a je to nejčastěji používaný model při práci s výpočty nákladů.</span><span class="sxs-lookup"><span data-stu-id="be375-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="be375-206">V poli Skupina zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="be375-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="be375-207">Vyberte například Audio.</span><span class="sxs-lookup"><span data-stu-id="be375-207">For example, select Audio.</span></span> <span data-ttu-id="be375-208">To nemá žádný vliv na výpočty nákladů.</span><span class="sxs-lookup"><span data-stu-id="be375-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="be375-209">V poli Skupina dimenze úložiště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="be375-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="be375-210">Vyberte SiteWH.</span><span class="sxs-lookup"><span data-stu-id="be375-210">Select SiteWH.</span></span> <span data-ttu-id="be375-211">Pro ukázku se použije pouze Pracoviště a Sklad.</span><span class="sxs-lookup"><span data-stu-id="be375-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="be375-212">V poli Skupina sledovací dimenze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="be375-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="be375-213">Sledovací dimenze v tomto příkladu nebudou použity.</span><span class="sxs-lookup"><span data-stu-id="be375-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="be375-214">Zvolte Žádné.</span><span class="sxs-lookup"><span data-stu-id="be375-214">Select None.</span></span>  
7. <span data-ttu-id="be375-215">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="be375-215">Click OK.</span></span>
8. <span data-ttu-id="be375-216">V podokně akcí klikněte na možnost Spravovat sklad.</span><span class="sxs-lookup"><span data-stu-id="be375-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="be375-217">Klikněte na Výchozí nastavení objednávky.</span><span class="sxs-lookup"><span data-stu-id="be375-217">Click Default order settings.</span></span>
10. <span data-ttu-id="be375-218">V poli Nákupní pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="be375-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="be375-219">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="be375-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="be375-220">V poli Skladové pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="be375-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="be375-221">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="be375-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="be375-222">V poli Prodejní pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="be375-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="be375-223">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="be375-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="be375-224">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="be375-224">Close the page.</span></span>
14. <span data-ttu-id="be375-225">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="be375-225">Close the page.</span></span>
15. <span data-ttu-id="be375-226">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="be375-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="be375-227">Klikněte na ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="be375-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="be375-228">Rozbalte oblast Správa nákladů.</span><span class="sxs-lookup"><span data-stu-id="be375-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="be375-229">Zadejte hodnotu do pole Nákladová skupina.</span><span class="sxs-lookup"><span data-stu-id="be375-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="be375-230">V tomto příkladu zadejte M1.</span><span class="sxs-lookup"><span data-stu-id="be375-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="be375-231">V podokně akcí klikněte na možnost Spravovat náklady.</span><span class="sxs-lookup"><span data-stu-id="be375-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="be375-232">Klikněte na možnost Cena položky.</span><span class="sxs-lookup"><span data-stu-id="be375-232">Click Item price.</span></span>
20. <span data-ttu-id="be375-233">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="be375-233">Click New.</span></span>
21. <span data-ttu-id="be375-234">V poli Verze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="be375-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="be375-235">V tomto příkladu vyberte 10.</span><span class="sxs-lookup"><span data-stu-id="be375-235">For this example, select 10.</span></span> <span data-ttu-id="be375-236">Jedná se o typ výpočtu standardních nákladů.</span><span class="sxs-lookup"><span data-stu-id="be375-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="be375-237">V poli Lokalita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="be375-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="be375-238">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="be375-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="be375-239">Zadejte číslo do pole Cena.</span><span class="sxs-lookup"><span data-stu-id="be375-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="be375-240">V tomto příkladu zadejte 10.</span><span class="sxs-lookup"><span data-stu-id="be375-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="be375-241">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="be375-241">Click Save.</span></span>
25. <span data-ttu-id="be375-242">Klikněte na Aktivovat nezpracované ceny.</span><span class="sxs-lookup"><span data-stu-id="be375-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="be375-243">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="be375-243">Close the page.</span></span>
27. <span data-ttu-id="be375-244">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="be375-244">Close the page.</span></span>


