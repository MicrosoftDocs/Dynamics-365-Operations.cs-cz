--- 
title: "Vytvoření surovin (únor 2016)"
description: "Tato úloha je zaměřena na vytvoření komponent dokončených produktů a polotovarů produktů."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, InventItemPrice
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 091b6edaf43e86e6e3665bf79871648473e284c7
ms.contentlocale: cs-cz
ms.lasthandoff: 09/14/2018

---
# <a name="create-raw-materials-february-2016"></a><span data-ttu-id="b0eea-103">Vytvoření surovin (únor 2016)</span><span class="sxs-lookup"><span data-stu-id="b0eea-103">Create raw materials (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b0eea-104">Tato úloha je zaměřena na vytvoření komponent dokončených produktů a polotovarů produktů.</span><span class="sxs-lookup"><span data-stu-id="b0eea-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="b0eea-105">Je to třetí úloha v řadě Kalkulace kusovníku.</span><span class="sxs-lookup"><span data-stu-id="b0eea-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="b0eea-106">Tento úkol byl vytvořen pomocí ukázkových dat společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="b0eea-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="b0eea-107">Vytvoření prvního materiálu</span><span class="sxs-lookup"><span data-stu-id="b0eea-107">Create the first material</span></span>
1. <span data-ttu-id="b0eea-108">Přejděte na možnosti Řízení informací o produktech > Produkty > Uvolněné produkty.</span><span class="sxs-lookup"><span data-stu-id="b0eea-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="b0eea-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="b0eea-109">Click New.</span></span>
3. <span data-ttu-id="b0eea-110">Zadejte hodnotu do pole Číslo produktu.</span><span class="sxs-lookup"><span data-stu-id="b0eea-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="b0eea-111">V tomto příkladu zadejte ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="b0eea-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="b0eea-112">V poli Skupina modelů zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b0eea-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="b0eea-113">Vyberte volbu „STD“.</span><span class="sxs-lookup"><span data-stu-id="b0eea-113">Select STD.</span></span> <span data-ttu-id="b0eea-114">STD zastupuje standardní náklady a je to nejčastěji používaný model při práci s výpočty nákladů.</span><span class="sxs-lookup"><span data-stu-id="b0eea-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="b0eea-115">V poli Skupina zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b0eea-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="b0eea-116">Vyberte například Audio.</span><span class="sxs-lookup"><span data-stu-id="b0eea-116">For example, select Audio.</span></span> <span data-ttu-id="b0eea-117">To nemá žádný vliv na výpočty nákladů.</span><span class="sxs-lookup"><span data-stu-id="b0eea-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="b0eea-118">V poli Skupina dimenze úložiště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b0eea-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="b0eea-119">Vyberte SiteWH.</span><span class="sxs-lookup"><span data-stu-id="b0eea-119">Select SiteWH.</span></span> <span data-ttu-id="b0eea-120">Pro ukázku se použije pouze Pracoviště a Sklad.</span><span class="sxs-lookup"><span data-stu-id="b0eea-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="b0eea-121">V poli Skupina sledovací dimenze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b0eea-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="b0eea-122">Sledovací dimenze v tomto příkladu nebudou použity.</span><span class="sxs-lookup"><span data-stu-id="b0eea-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="b0eea-123">Zvolte Žádné.</span><span class="sxs-lookup"><span data-stu-id="b0eea-123">Select None.</span></span>  
8. <span data-ttu-id="b0eea-124">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="b0eea-124">Click OK.</span></span>
9. <span data-ttu-id="b0eea-125">V podokně akcí klikněte na možnost Spravovat sklad.</span><span class="sxs-lookup"><span data-stu-id="b0eea-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="b0eea-126">Klikněte na Výchozí nastavení objednávky.</span><span class="sxs-lookup"><span data-stu-id="b0eea-126">Click Default order settings.</span></span>
11. <span data-ttu-id="b0eea-127">V poli Nákupní pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b0eea-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="b0eea-128">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="b0eea-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="b0eea-129">V poli Skladové pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b0eea-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="b0eea-130">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="b0eea-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="b0eea-131">V poli Prodejní pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b0eea-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="b0eea-132">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="b0eea-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="b0eea-133">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b0eea-133">Close the page.</span></span>
15. <span data-ttu-id="b0eea-134">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b0eea-134">Close the page.</span></span>
16. <span data-ttu-id="b0eea-135">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="b0eea-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b0eea-136">Klikněte na ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="b0eea-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="b0eea-137">Rozbalte oblast Správa nákladů.</span><span class="sxs-lookup"><span data-stu-id="b0eea-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="b0eea-138">Zadejte hodnotu do pole Nákladová skupina.</span><span class="sxs-lookup"><span data-stu-id="b0eea-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="b0eea-139">V tomto příkladu zadejte M2.</span><span class="sxs-lookup"><span data-stu-id="b0eea-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="b0eea-140">V podokně akcí klikněte na možnost Spravovat náklady.</span><span class="sxs-lookup"><span data-stu-id="b0eea-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="b0eea-141">Klikněte na možnost Cena položky.</span><span class="sxs-lookup"><span data-stu-id="b0eea-141">Click Item price.</span></span>
21. <span data-ttu-id="b0eea-142">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="b0eea-142">Click New.</span></span>
22. <span data-ttu-id="b0eea-143">V poli Verze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b0eea-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="b0eea-144">V tomto příkladu vyberte 10, což je typ výpočtu standardních nákladů.</span><span class="sxs-lookup"><span data-stu-id="b0eea-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="b0eea-145">V poli Lokalita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b0eea-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="b0eea-146">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="b0eea-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="b0eea-147">Zadejte číslo do pole Cena.</span><span class="sxs-lookup"><span data-stu-id="b0eea-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="b0eea-148">V tomto příkladu zadejte 10.</span><span class="sxs-lookup"><span data-stu-id="b0eea-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="b0eea-149">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b0eea-149">Click Save.</span></span>
26. <span data-ttu-id="b0eea-150">Klikněte na Aktivovat nezpracované ceny.</span><span class="sxs-lookup"><span data-stu-id="b0eea-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="b0eea-151">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b0eea-151">Close the page.</span></span>
28. <span data-ttu-id="b0eea-152">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b0eea-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="b0eea-153">Vytvoření druhého materiálu</span><span class="sxs-lookup"><span data-stu-id="b0eea-153">Create the second material</span></span>
1. <span data-ttu-id="b0eea-154">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="b0eea-154">Click New.</span></span>
2. <span data-ttu-id="b0eea-155">Zadejte hodnotu do pole Číslo produktu.</span><span class="sxs-lookup"><span data-stu-id="b0eea-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="b0eea-156">V tomto příkladu zadejte ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="b0eea-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="b0eea-157">V poli Skupina modelů zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b0eea-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="b0eea-158">Vyberte volbu „STD“.</span><span class="sxs-lookup"><span data-stu-id="b0eea-158">Select STD.</span></span> <span data-ttu-id="b0eea-159">STD zastupuje standardní náklady a je to nejčastěji používaný model při práci s výpočty nákladů.</span><span class="sxs-lookup"><span data-stu-id="b0eea-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="b0eea-160">V poli Skupina zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b0eea-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="b0eea-161">Vyberte například Audio.</span><span class="sxs-lookup"><span data-stu-id="b0eea-161">For example, select Audio.</span></span> <span data-ttu-id="b0eea-162">To nemá žádný vliv na výpočty nákladů.</span><span class="sxs-lookup"><span data-stu-id="b0eea-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="b0eea-163">V poli Skupina dimenze úložiště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b0eea-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="b0eea-164">Vyberte SiteWH.</span><span class="sxs-lookup"><span data-stu-id="b0eea-164">Select SiteWH.</span></span> <span data-ttu-id="b0eea-165">Pro tento příklad se použije pouze Pracoviště a Sklad.</span><span class="sxs-lookup"><span data-stu-id="b0eea-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="b0eea-166">V poli Skupina sledovací dimenze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b0eea-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="b0eea-167">Sledovací dimenze v tomto příkladu nebudou použity.</span><span class="sxs-lookup"><span data-stu-id="b0eea-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="b0eea-168">Zvolte Žádné.</span><span class="sxs-lookup"><span data-stu-id="b0eea-168">Select None.</span></span>  
7. <span data-ttu-id="b0eea-169">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="b0eea-169">Click OK.</span></span>
8. <span data-ttu-id="b0eea-170">V podokně akcí klikněte na možnost Spravovat sklad.</span><span class="sxs-lookup"><span data-stu-id="b0eea-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="b0eea-171">Klikněte na Výchozí nastavení objednávky.</span><span class="sxs-lookup"><span data-stu-id="b0eea-171">Click Default order settings.</span></span>
10. <span data-ttu-id="b0eea-172">V poli Nákupní pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b0eea-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="b0eea-173">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="b0eea-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="b0eea-174">V poli Skladové pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b0eea-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="b0eea-175">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="b0eea-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="b0eea-176">V poli Prodejní pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b0eea-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="b0eea-177">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="b0eea-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="b0eea-178">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b0eea-178">Close the page.</span></span>
14. <span data-ttu-id="b0eea-179">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b0eea-179">Close the page.</span></span>
15. <span data-ttu-id="b0eea-180">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="b0eea-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b0eea-181">Klikněte na ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="b0eea-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="b0eea-182">Rozbalte oblast Správa nákladů.</span><span class="sxs-lookup"><span data-stu-id="b0eea-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="b0eea-183">Zadejte hodnotu do pole Nákladová skupina.</span><span class="sxs-lookup"><span data-stu-id="b0eea-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="b0eea-184">V tomto příkladu zadejte M2.</span><span class="sxs-lookup"><span data-stu-id="b0eea-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="b0eea-185">V podokně akcí klikněte na možnost Spravovat náklady.</span><span class="sxs-lookup"><span data-stu-id="b0eea-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="b0eea-186">Klikněte na možnost Cena položky.</span><span class="sxs-lookup"><span data-stu-id="b0eea-186">Click Item price.</span></span>
20. <span data-ttu-id="b0eea-187">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="b0eea-187">Click New.</span></span>
21. <span data-ttu-id="b0eea-188">V poli Verze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b0eea-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="b0eea-189">V tomto příkladu vyberte 10.</span><span class="sxs-lookup"><span data-stu-id="b0eea-189">For this example, select 10.</span></span> <span data-ttu-id="b0eea-190">Jedná se o typ výpočtu standardních nákladů.</span><span class="sxs-lookup"><span data-stu-id="b0eea-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="b0eea-191">V poli Lokalita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b0eea-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="b0eea-192">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="b0eea-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="b0eea-193">Zadejte číslo do pole Cena.</span><span class="sxs-lookup"><span data-stu-id="b0eea-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="b0eea-194">Pro ukázku zadejte 10.</span><span class="sxs-lookup"><span data-stu-id="b0eea-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="b0eea-195">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b0eea-195">Click Save.</span></span>
25. <span data-ttu-id="b0eea-196">Klikněte na Aktivovat nezpracované ceny.</span><span class="sxs-lookup"><span data-stu-id="b0eea-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="b0eea-197">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b0eea-197">Close the page.</span></span>
27. <span data-ttu-id="b0eea-198">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b0eea-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="b0eea-199">Vytvoření třetího materiálu</span><span class="sxs-lookup"><span data-stu-id="b0eea-199">Create the third material</span></span>
1. <span data-ttu-id="b0eea-200">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="b0eea-200">Click New.</span></span>
2. <span data-ttu-id="b0eea-201">Zadejte hodnotu do pole Číslo produktu.</span><span class="sxs-lookup"><span data-stu-id="b0eea-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="b0eea-202">Pro ukázku zadejte ITEM_C</span><span class="sxs-lookup"><span data-stu-id="b0eea-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="b0eea-203">V poli Skupina modelů zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b0eea-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="b0eea-204">Vyberte volbu „STD“.</span><span class="sxs-lookup"><span data-stu-id="b0eea-204">Select STD.</span></span> <span data-ttu-id="b0eea-205">STD zastupuje standardní náklady a je to nejčastěji používaný model při práci s výpočty nákladů.</span><span class="sxs-lookup"><span data-stu-id="b0eea-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="b0eea-206">V poli Skupina zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b0eea-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="b0eea-207">Vyberte například Audio.</span><span class="sxs-lookup"><span data-stu-id="b0eea-207">For example, select Audio.</span></span> <span data-ttu-id="b0eea-208">To nemá žádný vliv na výpočty nákladů.</span><span class="sxs-lookup"><span data-stu-id="b0eea-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="b0eea-209">V poli Skupina dimenze úložiště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b0eea-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="b0eea-210">Vyberte SiteWH.</span><span class="sxs-lookup"><span data-stu-id="b0eea-210">Select SiteWH.</span></span> <span data-ttu-id="b0eea-211">Pro ukázku se použije pouze Pracoviště a Sklad.</span><span class="sxs-lookup"><span data-stu-id="b0eea-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="b0eea-212">V poli Skupina sledovací dimenze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b0eea-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="b0eea-213">Sledovací dimenze v tomto příkladu nebudou použity.</span><span class="sxs-lookup"><span data-stu-id="b0eea-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="b0eea-214">Zvolte Žádné.</span><span class="sxs-lookup"><span data-stu-id="b0eea-214">Select None.</span></span>  
7. <span data-ttu-id="b0eea-215">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="b0eea-215">Click OK.</span></span>
8. <span data-ttu-id="b0eea-216">V podokně akcí klikněte na možnost Spravovat sklad.</span><span class="sxs-lookup"><span data-stu-id="b0eea-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="b0eea-217">Klikněte na Výchozí nastavení objednávky.</span><span class="sxs-lookup"><span data-stu-id="b0eea-217">Click Default order settings.</span></span>
10. <span data-ttu-id="b0eea-218">V poli Nákupní pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b0eea-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="b0eea-219">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="b0eea-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="b0eea-220">V poli Skladové pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b0eea-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="b0eea-221">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="b0eea-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="b0eea-222">V poli Prodejní pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b0eea-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="b0eea-223">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="b0eea-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="b0eea-224">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b0eea-224">Close the page.</span></span>
14. <span data-ttu-id="b0eea-225">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b0eea-225">Close the page.</span></span>
15. <span data-ttu-id="b0eea-226">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="b0eea-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="b0eea-227">Klikněte na ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="b0eea-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="b0eea-228">Rozbalte oblast Správa nákladů.</span><span class="sxs-lookup"><span data-stu-id="b0eea-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="b0eea-229">Zadejte hodnotu do pole Nákladová skupina.</span><span class="sxs-lookup"><span data-stu-id="b0eea-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="b0eea-230">V tomto příkladu zadejte M1.</span><span class="sxs-lookup"><span data-stu-id="b0eea-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="b0eea-231">V podokně akcí klikněte na možnost Spravovat náklady.</span><span class="sxs-lookup"><span data-stu-id="b0eea-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="b0eea-232">Klikněte na možnost Cena položky.</span><span class="sxs-lookup"><span data-stu-id="b0eea-232">Click Item price.</span></span>
20. <span data-ttu-id="b0eea-233">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="b0eea-233">Click New.</span></span>
21. <span data-ttu-id="b0eea-234">V poli Verze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b0eea-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="b0eea-235">V tomto příkladu vyberte 10.</span><span class="sxs-lookup"><span data-stu-id="b0eea-235">For this example, select 10.</span></span> <span data-ttu-id="b0eea-236">Jedná se o typ výpočtu standardních nákladů.</span><span class="sxs-lookup"><span data-stu-id="b0eea-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="b0eea-237">V poli Lokalita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b0eea-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="b0eea-238">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="b0eea-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="b0eea-239">Zadejte číslo do pole Cena.</span><span class="sxs-lookup"><span data-stu-id="b0eea-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="b0eea-240">V tomto příkladu zadejte 10.</span><span class="sxs-lookup"><span data-stu-id="b0eea-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="b0eea-241">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b0eea-241">Click Save.</span></span>
25. <span data-ttu-id="b0eea-242">Klikněte na Aktivovat nezpracované ceny.</span><span class="sxs-lookup"><span data-stu-id="b0eea-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="b0eea-243">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b0eea-243">Close the page.</span></span>
27. <span data-ttu-id="b0eea-244">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b0eea-244">Close the page.</span></span>


