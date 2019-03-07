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
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 091b6edaf43e86e6e3665bf79871648473e284c7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "351049"
---
# <a name="create-raw-materials-february-2016"></a><span data-ttu-id="50acd-103">Vytvoření surovin (únor 2016)</span><span class="sxs-lookup"><span data-stu-id="50acd-103">Create raw materials (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="50acd-104">Tato úloha je zaměřena na vytvoření komponent dokončených produktů a polotovarů produktů.</span><span class="sxs-lookup"><span data-stu-id="50acd-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="50acd-105">Je to třetí úloha v řadě Kalkulace kusovníku.</span><span class="sxs-lookup"><span data-stu-id="50acd-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="50acd-106">Tento úkol byl vytvořen pomocí ukázkových dat společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="50acd-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="50acd-107">Vytvoření prvního materiálu</span><span class="sxs-lookup"><span data-stu-id="50acd-107">Create the first material</span></span>
1. <span data-ttu-id="50acd-108">Přejděte na možnosti Řízení informací o produktech > Produkty > Uvolněné produkty.</span><span class="sxs-lookup"><span data-stu-id="50acd-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="50acd-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="50acd-109">Click New.</span></span>
3. <span data-ttu-id="50acd-110">Zadejte hodnotu do pole Číslo produktu.</span><span class="sxs-lookup"><span data-stu-id="50acd-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="50acd-111">V tomto příkladu zadejte ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="50acd-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="50acd-112">V poli Skupina modelů zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="50acd-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="50acd-113">Vyberte volbu „STD“.</span><span class="sxs-lookup"><span data-stu-id="50acd-113">Select STD.</span></span> <span data-ttu-id="50acd-114">STD zastupuje standardní náklady a je to nejčastěji používaný model při práci s výpočty nákladů.</span><span class="sxs-lookup"><span data-stu-id="50acd-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="50acd-115">V poli Skupina zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="50acd-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="50acd-116">Vyberte například Audio.</span><span class="sxs-lookup"><span data-stu-id="50acd-116">For example, select Audio.</span></span> <span data-ttu-id="50acd-117">To nemá žádný vliv na výpočty nákladů.</span><span class="sxs-lookup"><span data-stu-id="50acd-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="50acd-118">V poli Skupina dimenze úložiště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="50acd-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="50acd-119">Vyberte SiteWH.</span><span class="sxs-lookup"><span data-stu-id="50acd-119">Select SiteWH.</span></span> <span data-ttu-id="50acd-120">Pro ukázku se použije pouze Pracoviště a Sklad.</span><span class="sxs-lookup"><span data-stu-id="50acd-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="50acd-121">V poli Skupina sledovací dimenze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="50acd-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="50acd-122">Sledovací dimenze v tomto příkladu nebudou použity.</span><span class="sxs-lookup"><span data-stu-id="50acd-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="50acd-123">Zvolte Žádné.</span><span class="sxs-lookup"><span data-stu-id="50acd-123">Select None.</span></span>  
8. <span data-ttu-id="50acd-124">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="50acd-124">Click OK.</span></span>
9. <span data-ttu-id="50acd-125">V podokně akcí klikněte na možnost Spravovat sklad.</span><span class="sxs-lookup"><span data-stu-id="50acd-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="50acd-126">Klikněte na Výchozí nastavení objednávky.</span><span class="sxs-lookup"><span data-stu-id="50acd-126">Click Default order settings.</span></span>
11. <span data-ttu-id="50acd-127">V poli Nákupní pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="50acd-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="50acd-128">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="50acd-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="50acd-129">V poli Skladové pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="50acd-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="50acd-130">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="50acd-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="50acd-131">V poli Prodejní pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="50acd-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="50acd-132">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="50acd-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="50acd-133">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="50acd-133">Close the page.</span></span>
15. <span data-ttu-id="50acd-134">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="50acd-134">Close the page.</span></span>
16. <span data-ttu-id="50acd-135">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="50acd-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="50acd-136">Klikněte na ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="50acd-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="50acd-137">Rozbalte oblast Správa nákladů.</span><span class="sxs-lookup"><span data-stu-id="50acd-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="50acd-138">Zadejte hodnotu do pole Nákladová skupina.</span><span class="sxs-lookup"><span data-stu-id="50acd-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="50acd-139">V tomto příkladu zadejte M2.</span><span class="sxs-lookup"><span data-stu-id="50acd-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="50acd-140">V podokně akcí klikněte na možnost Spravovat náklady.</span><span class="sxs-lookup"><span data-stu-id="50acd-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="50acd-141">Klikněte na možnost Cena položky.</span><span class="sxs-lookup"><span data-stu-id="50acd-141">Click Item price.</span></span>
21. <span data-ttu-id="50acd-142">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="50acd-142">Click New.</span></span>
22. <span data-ttu-id="50acd-143">V poli Verze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="50acd-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="50acd-144">V tomto příkladu vyberte 10, což je typ výpočtu standardních nákladů.</span><span class="sxs-lookup"><span data-stu-id="50acd-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="50acd-145">V poli Lokalita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="50acd-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="50acd-146">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="50acd-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="50acd-147">Zadejte číslo do pole Cena.</span><span class="sxs-lookup"><span data-stu-id="50acd-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="50acd-148">V tomto příkladu zadejte 10.</span><span class="sxs-lookup"><span data-stu-id="50acd-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="50acd-149">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="50acd-149">Click Save.</span></span>
26. <span data-ttu-id="50acd-150">Klikněte na Aktivovat nezpracované ceny.</span><span class="sxs-lookup"><span data-stu-id="50acd-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="50acd-151">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="50acd-151">Close the page.</span></span>
28. <span data-ttu-id="50acd-152">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="50acd-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="50acd-153">Vytvoření druhého materiálu</span><span class="sxs-lookup"><span data-stu-id="50acd-153">Create the second material</span></span>
1. <span data-ttu-id="50acd-154">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="50acd-154">Click New.</span></span>
2. <span data-ttu-id="50acd-155">Zadejte hodnotu do pole Číslo produktu.</span><span class="sxs-lookup"><span data-stu-id="50acd-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="50acd-156">V tomto příkladu zadejte ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="50acd-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="50acd-157">V poli Skupina modelů zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="50acd-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="50acd-158">Vyberte volbu „STD“.</span><span class="sxs-lookup"><span data-stu-id="50acd-158">Select STD.</span></span> <span data-ttu-id="50acd-159">STD zastupuje standardní náklady a je to nejčastěji používaný model při práci s výpočty nákladů.</span><span class="sxs-lookup"><span data-stu-id="50acd-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="50acd-160">V poli Skupina zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="50acd-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="50acd-161">Vyberte například Audio.</span><span class="sxs-lookup"><span data-stu-id="50acd-161">For example, select Audio.</span></span> <span data-ttu-id="50acd-162">To nemá žádný vliv na výpočty nákladů.</span><span class="sxs-lookup"><span data-stu-id="50acd-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="50acd-163">V poli Skupina dimenze úložiště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="50acd-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="50acd-164">Vyberte SiteWH.</span><span class="sxs-lookup"><span data-stu-id="50acd-164">Select SiteWH.</span></span> <span data-ttu-id="50acd-165">Pro tento příklad se použije pouze Pracoviště a Sklad.</span><span class="sxs-lookup"><span data-stu-id="50acd-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="50acd-166">V poli Skupina sledovací dimenze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="50acd-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="50acd-167">Sledovací dimenze v tomto příkladu nebudou použity.</span><span class="sxs-lookup"><span data-stu-id="50acd-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="50acd-168">Zvolte Žádné.</span><span class="sxs-lookup"><span data-stu-id="50acd-168">Select None.</span></span>  
7. <span data-ttu-id="50acd-169">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="50acd-169">Click OK.</span></span>
8. <span data-ttu-id="50acd-170">V podokně akcí klikněte na možnost Spravovat sklad.</span><span class="sxs-lookup"><span data-stu-id="50acd-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="50acd-171">Klikněte na Výchozí nastavení objednávky.</span><span class="sxs-lookup"><span data-stu-id="50acd-171">Click Default order settings.</span></span>
10. <span data-ttu-id="50acd-172">V poli Nákupní pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="50acd-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="50acd-173">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="50acd-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="50acd-174">V poli Skladové pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="50acd-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="50acd-175">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="50acd-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="50acd-176">V poli Prodejní pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="50acd-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="50acd-177">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="50acd-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="50acd-178">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="50acd-178">Close the page.</span></span>
14. <span data-ttu-id="50acd-179">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="50acd-179">Close the page.</span></span>
15. <span data-ttu-id="50acd-180">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="50acd-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="50acd-181">Klikněte na ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="50acd-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="50acd-182">Rozbalte oblast Správa nákladů.</span><span class="sxs-lookup"><span data-stu-id="50acd-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="50acd-183">Zadejte hodnotu do pole Nákladová skupina.</span><span class="sxs-lookup"><span data-stu-id="50acd-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="50acd-184">V tomto příkladu zadejte M2.</span><span class="sxs-lookup"><span data-stu-id="50acd-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="50acd-185">V podokně akcí klikněte na možnost Spravovat náklady.</span><span class="sxs-lookup"><span data-stu-id="50acd-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="50acd-186">Klikněte na možnost Cena položky.</span><span class="sxs-lookup"><span data-stu-id="50acd-186">Click Item price.</span></span>
20. <span data-ttu-id="50acd-187">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="50acd-187">Click New.</span></span>
21. <span data-ttu-id="50acd-188">V poli Verze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="50acd-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="50acd-189">V tomto příkladu vyberte 10.</span><span class="sxs-lookup"><span data-stu-id="50acd-189">For this example, select 10.</span></span> <span data-ttu-id="50acd-190">Jedná se o typ výpočtu standardních nákladů.</span><span class="sxs-lookup"><span data-stu-id="50acd-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="50acd-191">V poli Lokalita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="50acd-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="50acd-192">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="50acd-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="50acd-193">Zadejte číslo do pole Cena.</span><span class="sxs-lookup"><span data-stu-id="50acd-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="50acd-194">Pro ukázku zadejte 10.</span><span class="sxs-lookup"><span data-stu-id="50acd-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="50acd-195">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="50acd-195">Click Save.</span></span>
25. <span data-ttu-id="50acd-196">Klikněte na Aktivovat nezpracované ceny.</span><span class="sxs-lookup"><span data-stu-id="50acd-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="50acd-197">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="50acd-197">Close the page.</span></span>
27. <span data-ttu-id="50acd-198">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="50acd-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="50acd-199">Vytvoření třetího materiálu</span><span class="sxs-lookup"><span data-stu-id="50acd-199">Create the third material</span></span>
1. <span data-ttu-id="50acd-200">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="50acd-200">Click New.</span></span>
2. <span data-ttu-id="50acd-201">Zadejte hodnotu do pole Číslo produktu.</span><span class="sxs-lookup"><span data-stu-id="50acd-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="50acd-202">Pro ukázku zadejte ITEM_C</span><span class="sxs-lookup"><span data-stu-id="50acd-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="50acd-203">V poli Skupina modelů zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="50acd-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="50acd-204">Vyberte volbu „STD“.</span><span class="sxs-lookup"><span data-stu-id="50acd-204">Select STD.</span></span> <span data-ttu-id="50acd-205">STD zastupuje standardní náklady a je to nejčastěji používaný model při práci s výpočty nákladů.</span><span class="sxs-lookup"><span data-stu-id="50acd-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="50acd-206">V poli Skupina zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="50acd-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="50acd-207">Vyberte například Audio.</span><span class="sxs-lookup"><span data-stu-id="50acd-207">For example, select Audio.</span></span> <span data-ttu-id="50acd-208">To nemá žádný vliv na výpočty nákladů.</span><span class="sxs-lookup"><span data-stu-id="50acd-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="50acd-209">V poli Skupina dimenze úložiště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="50acd-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="50acd-210">Vyberte SiteWH.</span><span class="sxs-lookup"><span data-stu-id="50acd-210">Select SiteWH.</span></span> <span data-ttu-id="50acd-211">Pro ukázku se použije pouze Pracoviště a Sklad.</span><span class="sxs-lookup"><span data-stu-id="50acd-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="50acd-212">V poli Skupina sledovací dimenze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="50acd-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="50acd-213">Sledovací dimenze v tomto příkladu nebudou použity.</span><span class="sxs-lookup"><span data-stu-id="50acd-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="50acd-214">Zvolte Žádné.</span><span class="sxs-lookup"><span data-stu-id="50acd-214">Select None.</span></span>  
7. <span data-ttu-id="50acd-215">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="50acd-215">Click OK.</span></span>
8. <span data-ttu-id="50acd-216">V podokně akcí klikněte na možnost Spravovat sklad.</span><span class="sxs-lookup"><span data-stu-id="50acd-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="50acd-217">Klikněte na Výchozí nastavení objednávky.</span><span class="sxs-lookup"><span data-stu-id="50acd-217">Click Default order settings.</span></span>
10. <span data-ttu-id="50acd-218">V poli Nákupní pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="50acd-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="50acd-219">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="50acd-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="50acd-220">V poli Skladové pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="50acd-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="50acd-221">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="50acd-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="50acd-222">V poli Prodejní pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="50acd-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="50acd-223">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="50acd-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="50acd-224">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="50acd-224">Close the page.</span></span>
14. <span data-ttu-id="50acd-225">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="50acd-225">Close the page.</span></span>
15. <span data-ttu-id="50acd-226">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="50acd-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="50acd-227">Klikněte na ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="50acd-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="50acd-228">Rozbalte oblast Správa nákladů.</span><span class="sxs-lookup"><span data-stu-id="50acd-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="50acd-229">Zadejte hodnotu do pole Nákladová skupina.</span><span class="sxs-lookup"><span data-stu-id="50acd-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="50acd-230">V tomto příkladu zadejte M1.</span><span class="sxs-lookup"><span data-stu-id="50acd-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="50acd-231">V podokně akcí klikněte na možnost Spravovat náklady.</span><span class="sxs-lookup"><span data-stu-id="50acd-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="50acd-232">Klikněte na možnost Cena položky.</span><span class="sxs-lookup"><span data-stu-id="50acd-232">Click Item price.</span></span>
20. <span data-ttu-id="50acd-233">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="50acd-233">Click New.</span></span>
21. <span data-ttu-id="50acd-234">V poli Verze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="50acd-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="50acd-235">V tomto příkladu vyberte 10.</span><span class="sxs-lookup"><span data-stu-id="50acd-235">For this example, select 10.</span></span> <span data-ttu-id="50acd-236">Jedná se o typ výpočtu standardních nákladů.</span><span class="sxs-lookup"><span data-stu-id="50acd-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="50acd-237">V poli Lokalita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="50acd-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="50acd-238">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="50acd-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="50acd-239">Zadejte číslo do pole Cena.</span><span class="sxs-lookup"><span data-stu-id="50acd-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="50acd-240">V tomto příkladu zadejte 10.</span><span class="sxs-lookup"><span data-stu-id="50acd-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="50acd-241">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="50acd-241">Click Save.</span></span>
25. <span data-ttu-id="50acd-242">Klikněte na Aktivovat nezpracované ceny.</span><span class="sxs-lookup"><span data-stu-id="50acd-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="50acd-243">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="50acd-243">Close the page.</span></span>
27. <span data-ttu-id="50acd-244">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="50acd-244">Close the page.</span></span>

