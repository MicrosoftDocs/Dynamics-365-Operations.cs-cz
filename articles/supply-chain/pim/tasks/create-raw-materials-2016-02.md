---
title: Vytvoření surovin (únor 2016)
description: Tato úloha je zaměřena na vytvoření komponent dokončených produktů a polotovarů produktů.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, InventItemPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9e20abf8a1b211bff2bc73d1a36a1e5c917ffaab
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844578"
---
# <a name="create-raw-materials-february-2016"></a><span data-ttu-id="52797-103">Vytvoření surovin (únor 2016)</span><span class="sxs-lookup"><span data-stu-id="52797-103">Create raw materials (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="52797-104">Tato úloha je zaměřena na vytvoření komponent dokončených produktů a polotovarů produktů.</span><span class="sxs-lookup"><span data-stu-id="52797-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="52797-105">Je to třetí úloha v řadě Kalkulace kusovníku.</span><span class="sxs-lookup"><span data-stu-id="52797-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="52797-106">Tento úkol byl vytvořen pomocí ukázkových dat společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="52797-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="52797-107">Vytvoření prvního materiálu</span><span class="sxs-lookup"><span data-stu-id="52797-107">Create the first material</span></span>
1. <span data-ttu-id="52797-108">Přejděte na možnosti Řízení informací o produktech > Produkty > Uvolněné produkty.</span><span class="sxs-lookup"><span data-stu-id="52797-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="52797-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="52797-109">Click New.</span></span>
3. <span data-ttu-id="52797-110">Zadejte hodnotu do pole Číslo produktu.</span><span class="sxs-lookup"><span data-stu-id="52797-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="52797-111">V tomto příkladu zadejte ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="52797-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="52797-112">V poli Skupina modelů zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="52797-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="52797-113">Vyberte volbu „STD“.</span><span class="sxs-lookup"><span data-stu-id="52797-113">Select STD.</span></span> <span data-ttu-id="52797-114">STD zastupuje standardní náklady a je to nejčastěji používaný model při práci s výpočty nákladů.</span><span class="sxs-lookup"><span data-stu-id="52797-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="52797-115">V poli Skupina zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="52797-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="52797-116">Vyberte například Audio.</span><span class="sxs-lookup"><span data-stu-id="52797-116">For example, select Audio.</span></span> <span data-ttu-id="52797-117">To nemá žádný vliv na výpočty nákladů.</span><span class="sxs-lookup"><span data-stu-id="52797-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="52797-118">V poli Skupina dimenze úložiště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="52797-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="52797-119">Vyberte SiteWH.</span><span class="sxs-lookup"><span data-stu-id="52797-119">Select SiteWH.</span></span> <span data-ttu-id="52797-120">Pro ukázku se použije pouze Pracoviště a Sklad.</span><span class="sxs-lookup"><span data-stu-id="52797-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="52797-121">V poli Skupina sledovací dimenze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="52797-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="52797-122">Sledovací dimenze v tomto příkladu nebudou použity.</span><span class="sxs-lookup"><span data-stu-id="52797-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="52797-123">Zvolte Žádné.</span><span class="sxs-lookup"><span data-stu-id="52797-123">Select None.</span></span>  
8. <span data-ttu-id="52797-124">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="52797-124">Click OK.</span></span>
9. <span data-ttu-id="52797-125">V podokně akcí klikněte na možnost Spravovat sklad.</span><span class="sxs-lookup"><span data-stu-id="52797-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="52797-126">Klikněte na Výchozí nastavení objednávky.</span><span class="sxs-lookup"><span data-stu-id="52797-126">Click Default order settings.</span></span>
11. <span data-ttu-id="52797-127">V poli Nákupní pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="52797-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="52797-128">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="52797-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="52797-129">V poli Skladové pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="52797-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="52797-130">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="52797-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="52797-131">V poli Prodejní pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="52797-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="52797-132">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="52797-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="52797-133">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="52797-133">Close the page.</span></span>
15. <span data-ttu-id="52797-134">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="52797-134">Close the page.</span></span>
16. <span data-ttu-id="52797-135">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="52797-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="52797-136">Klikněte na ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="52797-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="52797-137">Rozbalte oblast Správa nákladů.</span><span class="sxs-lookup"><span data-stu-id="52797-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="52797-138">Zadejte hodnotu do pole Nákladová skupina.</span><span class="sxs-lookup"><span data-stu-id="52797-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="52797-139">V tomto příkladu zadejte M2.</span><span class="sxs-lookup"><span data-stu-id="52797-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="52797-140">V podokně akcí klikněte na možnost Spravovat náklady.</span><span class="sxs-lookup"><span data-stu-id="52797-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="52797-141">Klikněte na možnost Cena položky.</span><span class="sxs-lookup"><span data-stu-id="52797-141">Click Item price.</span></span>
21. <span data-ttu-id="52797-142">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="52797-142">Click New.</span></span>
22. <span data-ttu-id="52797-143">V poli Verze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="52797-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="52797-144">V tomto příkladu vyberte 10, což je typ výpočtu standardních nákladů.</span><span class="sxs-lookup"><span data-stu-id="52797-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="52797-145">V poli Lokalita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="52797-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="52797-146">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="52797-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="52797-147">Zadejte číslo do pole Cena.</span><span class="sxs-lookup"><span data-stu-id="52797-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="52797-148">V tomto příkladu zadejte 10.</span><span class="sxs-lookup"><span data-stu-id="52797-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="52797-149">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="52797-149">Click Save.</span></span>
26. <span data-ttu-id="52797-150">Klikněte na Aktivovat nezpracované ceny.</span><span class="sxs-lookup"><span data-stu-id="52797-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="52797-151">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="52797-151">Close the page.</span></span>
28. <span data-ttu-id="52797-152">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="52797-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="52797-153">Vytvoření druhého materiálu</span><span class="sxs-lookup"><span data-stu-id="52797-153">Create the second material</span></span>
1. <span data-ttu-id="52797-154">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="52797-154">Click New.</span></span>
2. <span data-ttu-id="52797-155">Zadejte hodnotu do pole Číslo produktu.</span><span class="sxs-lookup"><span data-stu-id="52797-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="52797-156">V tomto příkladu zadejte ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="52797-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="52797-157">V poli Skupina modelů zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="52797-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="52797-158">Vyberte volbu „STD“.</span><span class="sxs-lookup"><span data-stu-id="52797-158">Select STD.</span></span> <span data-ttu-id="52797-159">STD zastupuje standardní náklady a je to nejčastěji používaný model při práci s výpočty nákladů.</span><span class="sxs-lookup"><span data-stu-id="52797-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="52797-160">V poli Skupina zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="52797-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="52797-161">Vyberte například Audio.</span><span class="sxs-lookup"><span data-stu-id="52797-161">For example, select Audio.</span></span> <span data-ttu-id="52797-162">To nemá žádný vliv na výpočty nákladů.</span><span class="sxs-lookup"><span data-stu-id="52797-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="52797-163">V poli Skupina dimenze úložiště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="52797-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="52797-164">Vyberte SiteWH.</span><span class="sxs-lookup"><span data-stu-id="52797-164">Select SiteWH.</span></span> <span data-ttu-id="52797-165">Pro tento příklad se použije pouze Pracoviště a Sklad.</span><span class="sxs-lookup"><span data-stu-id="52797-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="52797-166">V poli Skupina sledovací dimenze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="52797-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="52797-167">Sledovací dimenze v tomto příkladu nebudou použity.</span><span class="sxs-lookup"><span data-stu-id="52797-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="52797-168">Zvolte Žádné.</span><span class="sxs-lookup"><span data-stu-id="52797-168">Select None.</span></span>  
7. <span data-ttu-id="52797-169">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="52797-169">Click OK.</span></span>
8. <span data-ttu-id="52797-170">V podokně akcí klikněte na možnost Spravovat sklad.</span><span class="sxs-lookup"><span data-stu-id="52797-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="52797-171">Klikněte na Výchozí nastavení objednávky.</span><span class="sxs-lookup"><span data-stu-id="52797-171">Click Default order settings.</span></span>
10. <span data-ttu-id="52797-172">V poli Nákupní pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="52797-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="52797-173">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="52797-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="52797-174">V poli Skladové pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="52797-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="52797-175">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="52797-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="52797-176">V poli Prodejní pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="52797-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="52797-177">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="52797-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="52797-178">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="52797-178">Close the page.</span></span>
14. <span data-ttu-id="52797-179">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="52797-179">Close the page.</span></span>
15. <span data-ttu-id="52797-180">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="52797-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="52797-181">Klikněte na ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="52797-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="52797-182">Rozbalte oblast Správa nákladů.</span><span class="sxs-lookup"><span data-stu-id="52797-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="52797-183">Zadejte hodnotu do pole Nákladová skupina.</span><span class="sxs-lookup"><span data-stu-id="52797-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="52797-184">V tomto příkladu zadejte M2.</span><span class="sxs-lookup"><span data-stu-id="52797-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="52797-185">V podokně akcí klikněte na možnost Spravovat náklady.</span><span class="sxs-lookup"><span data-stu-id="52797-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="52797-186">Klikněte na možnost Cena položky.</span><span class="sxs-lookup"><span data-stu-id="52797-186">Click Item price.</span></span>
20. <span data-ttu-id="52797-187">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="52797-187">Click New.</span></span>
21. <span data-ttu-id="52797-188">V poli Verze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="52797-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="52797-189">V tomto příkladu vyberte 10.</span><span class="sxs-lookup"><span data-stu-id="52797-189">For this example, select 10.</span></span> <span data-ttu-id="52797-190">Jedná se o typ výpočtu standardních nákladů.</span><span class="sxs-lookup"><span data-stu-id="52797-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="52797-191">V poli Lokalita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="52797-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="52797-192">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="52797-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="52797-193">Zadejte číslo do pole Cena.</span><span class="sxs-lookup"><span data-stu-id="52797-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="52797-194">Pro ukázku zadejte 10.</span><span class="sxs-lookup"><span data-stu-id="52797-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="52797-195">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="52797-195">Click Save.</span></span>
25. <span data-ttu-id="52797-196">Klikněte na Aktivovat nezpracované ceny.</span><span class="sxs-lookup"><span data-stu-id="52797-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="52797-197">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="52797-197">Close the page.</span></span>
27. <span data-ttu-id="52797-198">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="52797-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="52797-199">Vytvoření třetího materiálu</span><span class="sxs-lookup"><span data-stu-id="52797-199">Create the third material</span></span>
1. <span data-ttu-id="52797-200">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="52797-200">Click New.</span></span>
2. <span data-ttu-id="52797-201">Zadejte hodnotu do pole Číslo produktu.</span><span class="sxs-lookup"><span data-stu-id="52797-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="52797-202">Pro ukázku zadejte ITEM_C</span><span class="sxs-lookup"><span data-stu-id="52797-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="52797-203">V poli Skupina modelů zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="52797-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="52797-204">Vyberte volbu „STD“.</span><span class="sxs-lookup"><span data-stu-id="52797-204">Select STD.</span></span> <span data-ttu-id="52797-205">STD zastupuje standardní náklady a je to nejčastěji používaný model při práci s výpočty nákladů.</span><span class="sxs-lookup"><span data-stu-id="52797-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="52797-206">V poli Skupina zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="52797-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="52797-207">Vyberte například Audio.</span><span class="sxs-lookup"><span data-stu-id="52797-207">For example, select Audio.</span></span> <span data-ttu-id="52797-208">To nemá žádný vliv na výpočty nákladů.</span><span class="sxs-lookup"><span data-stu-id="52797-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="52797-209">V poli Skupina dimenze úložiště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="52797-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="52797-210">Vyberte SiteWH.</span><span class="sxs-lookup"><span data-stu-id="52797-210">Select SiteWH.</span></span> <span data-ttu-id="52797-211">Pro ukázku se použije pouze Pracoviště a Sklad.</span><span class="sxs-lookup"><span data-stu-id="52797-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="52797-212">V poli Skupina sledovací dimenze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="52797-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="52797-213">Sledovací dimenze v tomto příkladu nebudou použity.</span><span class="sxs-lookup"><span data-stu-id="52797-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="52797-214">Zvolte Žádné.</span><span class="sxs-lookup"><span data-stu-id="52797-214">Select None.</span></span>  
7. <span data-ttu-id="52797-215">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="52797-215">Click OK.</span></span>
8. <span data-ttu-id="52797-216">V podokně akcí klikněte na možnost Spravovat sklad.</span><span class="sxs-lookup"><span data-stu-id="52797-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="52797-217">Klikněte na Výchozí nastavení objednávky.</span><span class="sxs-lookup"><span data-stu-id="52797-217">Click Default order settings.</span></span>
10. <span data-ttu-id="52797-218">V poli Nákupní pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="52797-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="52797-219">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="52797-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="52797-220">V poli Skladové pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="52797-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="52797-221">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="52797-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="52797-222">V poli Prodejní pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="52797-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="52797-223">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="52797-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="52797-224">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="52797-224">Close the page.</span></span>
14. <span data-ttu-id="52797-225">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="52797-225">Close the page.</span></span>
15. <span data-ttu-id="52797-226">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="52797-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="52797-227">Klikněte na ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="52797-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="52797-228">Rozbalte oblast Správa nákladů.</span><span class="sxs-lookup"><span data-stu-id="52797-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="52797-229">Zadejte hodnotu do pole Nákladová skupina.</span><span class="sxs-lookup"><span data-stu-id="52797-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="52797-230">V tomto příkladu zadejte M1.</span><span class="sxs-lookup"><span data-stu-id="52797-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="52797-231">V podokně akcí klikněte na možnost Spravovat náklady.</span><span class="sxs-lookup"><span data-stu-id="52797-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="52797-232">Klikněte na možnost Cena položky.</span><span class="sxs-lookup"><span data-stu-id="52797-232">Click Item price.</span></span>
20. <span data-ttu-id="52797-233">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="52797-233">Click New.</span></span>
21. <span data-ttu-id="52797-234">V poli Verze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="52797-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="52797-235">V tomto příkladu vyberte 10.</span><span class="sxs-lookup"><span data-stu-id="52797-235">For this example, select 10.</span></span> <span data-ttu-id="52797-236">Jedná se o typ výpočtu standardních nákladů.</span><span class="sxs-lookup"><span data-stu-id="52797-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="52797-237">V poli Lokalita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="52797-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="52797-238">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="52797-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="52797-239">Zadejte číslo do pole Cena.</span><span class="sxs-lookup"><span data-stu-id="52797-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="52797-240">V tomto příkladu zadejte 10.</span><span class="sxs-lookup"><span data-stu-id="52797-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="52797-241">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="52797-241">Click Save.</span></span>
25. <span data-ttu-id="52797-242">Klikněte na Aktivovat nezpracované ceny.</span><span class="sxs-lookup"><span data-stu-id="52797-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="52797-243">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="52797-243">Close the page.</span></span>
27. <span data-ttu-id="52797-244">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="52797-244">Close the page.</span></span>

