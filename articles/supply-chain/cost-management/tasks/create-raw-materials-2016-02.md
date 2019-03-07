---
title: Vytváření surovin (je ve verzi z února 2016)
description: Tato úloha je zaměřena na vytvoření komponent dokončených produktů a polotovarů produktů.
author: ShylaThompson
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 869acddf6f7e9754bb4952176ded4b22c74eaffd
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "327290"
---
# <a name="create-raw-materials-february-2016-only"></a><span data-ttu-id="ce2f2-103">Vytváření surovin (je ve verzi z února 2016)</span><span class="sxs-lookup"><span data-stu-id="ce2f2-103">Create raw materials (February 2016 only)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ce2f2-104">Tato úloha je zaměřena na vytvoření komponent dokončených produktů a polotovarů produktů.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="ce2f2-105">Je to třetí úloha v řadě Kalkulace kusovníku.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="ce2f2-106">Tento úkol byl vytvořen pomocí ukázkových dat společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="ce2f2-107">Vytvoření prvního materiálu</span><span class="sxs-lookup"><span data-stu-id="ce2f2-107">Create the first material</span></span>
1. <span data-ttu-id="ce2f2-108">Přejděte na možnosti Řízení informací o produktech > Produkty > Uvolněné produkty.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="ce2f2-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-109">Click New.</span></span>
3. <span data-ttu-id="ce2f2-110">Zadejte hodnotu do pole Číslo produktu.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="ce2f2-111">V tomto příkladu zadejte ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="ce2f2-112">V poli Skupina modelů zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="ce2f2-113">Vyberte volbu „STD“.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-113">Select STD.</span></span> <span data-ttu-id="ce2f2-114">STD zastupuje standardní náklady a je to nejčastěji používaný model při práci s výpočty nákladů.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="ce2f2-115">V poli Skupina zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="ce2f2-116">Vyberte například Audio.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-116">For example, select Audio.</span></span> <span data-ttu-id="ce2f2-117">To nemá žádný vliv na výpočty nákladů.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="ce2f2-118">V poli Skupina dimenze úložiště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="ce2f2-119">Vyberte SiteWH.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-119">Select SiteWH.</span></span> <span data-ttu-id="ce2f2-120">Pro ukázku se použije pouze Pracoviště a Sklad.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="ce2f2-121">V poli Skupina sledovací dimenze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="ce2f2-122">Sledovací dimenze v tomto příkladu nebudou použity.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="ce2f2-123">Zvolte Žádné.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-123">Select None.</span></span>  
8. <span data-ttu-id="ce2f2-124">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-124">Click OK.</span></span>
9. <span data-ttu-id="ce2f2-125">V podokně akcí klikněte na možnost Spravovat sklad.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="ce2f2-126">Klikněte na Výchozí nastavení objednávky.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-126">Click Default order settings.</span></span>
11. <span data-ttu-id="ce2f2-127">V poli Nákupní pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="ce2f2-128">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="ce2f2-129">V poli Skladové pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="ce2f2-130">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="ce2f2-131">V poli Prodejní pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="ce2f2-132">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="ce2f2-133">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-133">Close the page.</span></span>
15. <span data-ttu-id="ce2f2-134">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-134">Close the page.</span></span>
16. <span data-ttu-id="ce2f2-135">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ce2f2-136">Klikněte na ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="ce2f2-137">Rozbalte oblast Správa nákladů.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="ce2f2-138">Zadejte hodnotu do pole Nákladová skupina.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="ce2f2-139">V tomto příkladu zadejte M2.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="ce2f2-140">V podokně akcí klikněte na možnost Spravovat náklady.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="ce2f2-141">Klikněte na možnost Cena položky.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-141">Click Item price.</span></span>
21. <span data-ttu-id="ce2f2-142">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-142">Click New.</span></span>
22. <span data-ttu-id="ce2f2-143">V poli Verze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="ce2f2-144">V tomto příkladu vyberte 10, což je typ výpočtu standardních nákladů.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="ce2f2-145">V poli Lokalita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="ce2f2-146">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="ce2f2-147">Zadejte číslo do pole Cena.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="ce2f2-148">V tomto příkladu zadejte 10.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="ce2f2-149">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-149">Click Save.</span></span>
26. <span data-ttu-id="ce2f2-150">Klikněte na Aktivovat nezpracované ceny.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="ce2f2-151">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-151">Close the page.</span></span>
28. <span data-ttu-id="ce2f2-152">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="ce2f2-153">Vytvoření druhého materiálu</span><span class="sxs-lookup"><span data-stu-id="ce2f2-153">Create the second material</span></span>
1. <span data-ttu-id="ce2f2-154">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-154">Click New.</span></span>
2. <span data-ttu-id="ce2f2-155">Zadejte hodnotu do pole Číslo produktu.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="ce2f2-156">V tomto příkladu zadejte ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="ce2f2-157">V poli Skupina modelů zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="ce2f2-158">Vyberte volbu „STD“.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-158">Select STD.</span></span> <span data-ttu-id="ce2f2-159">STD zastupuje standardní náklady a je to nejčastěji používaný model při práci s výpočty nákladů.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="ce2f2-160">V poli Skupina zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="ce2f2-161">Vyberte například Audio.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-161">For example, select Audio.</span></span> <span data-ttu-id="ce2f2-162">To nemá žádný vliv na výpočty nákladů.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="ce2f2-163">V poli Skupina dimenze úložiště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="ce2f2-164">Vyberte SiteWH.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-164">Select SiteWH.</span></span> <span data-ttu-id="ce2f2-165">Pro tento příklad se použije pouze Pracoviště a Sklad.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="ce2f2-166">V poli Skupina sledovací dimenze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="ce2f2-167">Sledovací dimenze v tomto příkladu nebudou použity.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="ce2f2-168">Zvolte Žádné.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-168">Select None.</span></span>  
7. <span data-ttu-id="ce2f2-169">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-169">Click OK.</span></span>
8. <span data-ttu-id="ce2f2-170">V podokně akcí klikněte na možnost Spravovat sklad.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="ce2f2-171">Klikněte na Výchozí nastavení objednávky.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-171">Click Default order settings.</span></span>
10. <span data-ttu-id="ce2f2-172">V poli Nákupní pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="ce2f2-173">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="ce2f2-174">V poli Skladové pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="ce2f2-175">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="ce2f2-176">V poli Prodejní pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="ce2f2-177">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="ce2f2-178">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-178">Close the page.</span></span>
14. <span data-ttu-id="ce2f2-179">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-179">Close the page.</span></span>
15. <span data-ttu-id="ce2f2-180">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ce2f2-181">Klikněte na ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="ce2f2-182">Rozbalte oblast Správa nákladů.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="ce2f2-183">Zadejte hodnotu do pole Nákladová skupina.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="ce2f2-184">V tomto příkladu zadejte M2.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="ce2f2-185">V podokně akcí klikněte na možnost Spravovat náklady.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="ce2f2-186">Klikněte na možnost Cena položky.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-186">Click Item price.</span></span>
20. <span data-ttu-id="ce2f2-187">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-187">Click New.</span></span>
21. <span data-ttu-id="ce2f2-188">V poli Verze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="ce2f2-189">V tomto příkladu vyberte 10.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-189">For this example, select 10.</span></span> <span data-ttu-id="ce2f2-190">Jedná se o typ výpočtu standardních nákladů.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="ce2f2-191">V poli Lokalita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="ce2f2-192">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="ce2f2-193">Zadejte číslo do pole Cena.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="ce2f2-194">Pro ukázku zadejte 10.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="ce2f2-195">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-195">Click Save.</span></span>
25. <span data-ttu-id="ce2f2-196">Klikněte na Aktivovat nezpracované ceny.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="ce2f2-197">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-197">Close the page.</span></span>
27. <span data-ttu-id="ce2f2-198">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="ce2f2-199">Vytvoření třetího materiálu</span><span class="sxs-lookup"><span data-stu-id="ce2f2-199">Create the third material</span></span>
1. <span data-ttu-id="ce2f2-200">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-200">Click New.</span></span>
2. <span data-ttu-id="ce2f2-201">Zadejte hodnotu do pole Číslo produktu.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="ce2f2-202">Pro ukázku zadejte ITEM_C</span><span class="sxs-lookup"><span data-stu-id="ce2f2-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="ce2f2-203">V poli Skupina modelů zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="ce2f2-204">Vyberte volbu „STD“.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-204">Select STD.</span></span> <span data-ttu-id="ce2f2-205">STD zastupuje standardní náklady a je to nejčastěji používaný model při práci s výpočty nákladů.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="ce2f2-206">V poli Skupina zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="ce2f2-207">Vyberte například Audio.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-207">For example, select Audio.</span></span> <span data-ttu-id="ce2f2-208">To nemá žádný vliv na výpočty nákladů.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="ce2f2-209">V poli Skupina dimenze úložiště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="ce2f2-210">Vyberte SiteWH.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-210">Select SiteWH.</span></span> <span data-ttu-id="ce2f2-211">Pro ukázku se použije pouze Pracoviště a Sklad.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="ce2f2-212">V poli Skupina sledovací dimenze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="ce2f2-213">Sledovací dimenze v tomto příkladu nebudou použity.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="ce2f2-214">Zvolte Žádné.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-214">Select None.</span></span>  
7. <span data-ttu-id="ce2f2-215">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-215">Click OK.</span></span>
8. <span data-ttu-id="ce2f2-216">V podokně akcí klikněte na možnost Spravovat sklad.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="ce2f2-217">Klikněte na Výchozí nastavení objednávky.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-217">Click Default order settings.</span></span>
10. <span data-ttu-id="ce2f2-218">V poli Nákupní pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="ce2f2-219">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="ce2f2-220">V poli Skladové pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="ce2f2-221">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="ce2f2-222">V poli Prodejní pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="ce2f2-223">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="ce2f2-224">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-224">Close the page.</span></span>
14. <span data-ttu-id="ce2f2-225">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-225">Close the page.</span></span>
15. <span data-ttu-id="ce2f2-226">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ce2f2-227">Klikněte na ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="ce2f2-228">Rozbalte oblast Správa nákladů.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="ce2f2-229">Zadejte hodnotu do pole Nákladová skupina.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="ce2f2-230">V tomto příkladu zadejte M1.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="ce2f2-231">V podokně akcí klikněte na možnost Spravovat náklady.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="ce2f2-232">Klikněte na možnost Cena položky.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-232">Click Item price.</span></span>
20. <span data-ttu-id="ce2f2-233">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-233">Click New.</span></span>
21. <span data-ttu-id="ce2f2-234">V poli Verze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="ce2f2-235">V tomto příkladu vyberte 10.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-235">For this example, select 10.</span></span> <span data-ttu-id="ce2f2-236">Jedná se o typ výpočtu standardních nákladů.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="ce2f2-237">V poli Lokalita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="ce2f2-238">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="ce2f2-239">Zadejte číslo do pole Cena.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="ce2f2-240">V tomto příkladu zadejte 10.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="ce2f2-241">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-241">Click Save.</span></span>
25. <span data-ttu-id="ce2f2-242">Klikněte na Aktivovat nezpracované ceny.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="ce2f2-243">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-243">Close the page.</span></span>
27. <span data-ttu-id="ce2f2-244">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ce2f2-244">Close the page.</span></span>

