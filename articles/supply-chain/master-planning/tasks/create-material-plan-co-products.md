--- 
title: "Vytvoření materiálového plánu pro vedlejší produkty"
description: "Plánovač výroby naplánuje materiálové požadavky na položky, které jsou vedlejšími produkty receptury."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 2958f1e5c2e8a0cfa9cc6312f688d3b11b8e013c
ms.contentlocale: cs-cz
ms.lasthandoff: 09/14/2018

---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="26832-103">Vytvoření materiálového plánu pro vedlejší produkty</span><span class="sxs-lookup"><span data-stu-id="26832-103">Create a material plan for co products</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="26832-104">Plánovač výroby naplánuje materiálové požadavky na položky, které jsou vedlejšími produkty receptury.</span><span class="sxs-lookup"><span data-stu-id="26832-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="26832-105">K vytvoření tohoto postupu jsou použita ukázková data společnosti USP2.</span><span class="sxs-lookup"><span data-stu-id="26832-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="26832-106">Vytvoření požadavku pro vedlejší produkt</span><span class="sxs-lookup"><span data-stu-id="26832-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="26832-107">Přejděte na výchozí řídicí panel.</span><span class="sxs-lookup"><span data-stu-id="26832-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="26832-108">Klikněte na Zpracování a dotaz na prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="26832-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="26832-109">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="26832-109">Click New.</span></span>
4. <span data-ttu-id="26832-110">Klikněte na Prodejní objednávka.</span><span class="sxs-lookup"><span data-stu-id="26832-110">Click Sales order.</span></span>
5. <span data-ttu-id="26832-111">V poli Účet odběratele zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="26832-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="26832-112">Příklad: US-001</span><span class="sxs-lookup"><span data-stu-id="26832-112">Example: US-001</span></span>  
6. <span data-ttu-id="26832-113">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="26832-113">Click OK.</span></span>
7. <span data-ttu-id="26832-114">Zadejte hodnotu do pole Číslo zboží.</span><span class="sxs-lookup"><span data-stu-id="26832-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="26832-115">Příklad: P6003</span><span class="sxs-lookup"><span data-stu-id="26832-115">Example: P6003</span></span>  
8. <span data-ttu-id="26832-116">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="26832-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="26832-117">Příklad: 50000</span><span class="sxs-lookup"><span data-stu-id="26832-117">Example: 50000</span></span>  
9. <span data-ttu-id="26832-118">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="26832-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="26832-119">Vytvoření materiálového plánu pro vedlejší produkty</span><span class="sxs-lookup"><span data-stu-id="26832-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="26832-120">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="26832-120">Close the page.</span></span>
2. <span data-ttu-id="26832-121">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="26832-121">Close the page.</span></span>
3. <span data-ttu-id="26832-122">Klikněte na Hlavní plánování.</span><span class="sxs-lookup"><span data-stu-id="26832-122">Click Master planning.</span></span>
4. <span data-ttu-id="26832-123">V poli Plán kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="26832-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="26832-124">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="26832-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="26832-125">Příklad: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="26832-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="26832-126">Klikněte na položku Spustit.</span><span class="sxs-lookup"><span data-stu-id="26832-126">Click Run.</span></span>
7. <span data-ttu-id="26832-127">Rozbalte nebo sbalte oddíl Záznamy k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="26832-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="26832-128">Klepněte na tlačítko Filtr.</span><span class="sxs-lookup"><span data-stu-id="26832-128">Click Filter.</span></span>
9. <span data-ttu-id="26832-129">V seznamu vyberte řádek pro pole = číslo položky.</span><span class="sxs-lookup"><span data-stu-id="26832-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="26832-130">Zadejte hodnotu do pole Kritéria.</span><span class="sxs-lookup"><span data-stu-id="26832-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="26832-131">Příklad: P6003</span><span class="sxs-lookup"><span data-stu-id="26832-131">Example: P6003</span></span>  
11. <span data-ttu-id="26832-132">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="26832-132">Click OK.</span></span>
12. <span data-ttu-id="26832-133">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="26832-133">Click OK.</span></span>
13. <span data-ttu-id="26832-134">Klikněte na Plánované objednávky.</span><span class="sxs-lookup"><span data-stu-id="26832-134">Click Planned orders.</span></span>
14. <span data-ttu-id="26832-135">Použijte rychlý filtr pro hledání záznamů.</span><span class="sxs-lookup"><span data-stu-id="26832-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="26832-136">Můžete například filtrovat pole Číslo položky pomocí hodnoty „P6000“.</span><span class="sxs-lookup"><span data-stu-id="26832-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="26832-137">Filtrujte podle položky receptury, která má vedlejší produkt položky, pro kterou jste vytvořili prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="26832-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="26832-138">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="26832-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="26832-139">Vyberte libovolné řádky vrácené filtrem.</span><span class="sxs-lookup"><span data-stu-id="26832-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="26832-140">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="26832-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="26832-141">Rozbalte nebo sbalte oddíl Doložení.</span><span class="sxs-lookup"><span data-stu-id="26832-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="26832-142">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="26832-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="26832-143">Plánovaná objednávka je doložena v prodejní objednávce pro vedlejší produkt.</span><span class="sxs-lookup"><span data-stu-id="26832-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="26832-144">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="26832-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="26832-145">Vytvoření požadavku pro vedlejší produkt</span><span class="sxs-lookup"><span data-stu-id="26832-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="26832-146">Přejděte na výchozí řídicí panel.</span><span class="sxs-lookup"><span data-stu-id="26832-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="26832-147">Klikněte na Zpracování a dotaz na prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="26832-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="26832-148">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="26832-148">Click New.</span></span>
4. <span data-ttu-id="26832-149">Klikněte na Prodejní objednávka.</span><span class="sxs-lookup"><span data-stu-id="26832-149">Click Sales order.</span></span>
5. <span data-ttu-id="26832-150">V poli Účet odběratele zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="26832-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="26832-151">Příklad: US-001</span><span class="sxs-lookup"><span data-stu-id="26832-151">Example: US-001</span></span>  
6. <span data-ttu-id="26832-152">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="26832-152">Click OK.</span></span>
7. <span data-ttu-id="26832-153">Zadejte hodnotu do pole Číslo zboží.</span><span class="sxs-lookup"><span data-stu-id="26832-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="26832-154">Příklad: P6003</span><span class="sxs-lookup"><span data-stu-id="26832-154">Example: P6003</span></span>  
8. <span data-ttu-id="26832-155">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="26832-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="26832-156">Příklad: 50000</span><span class="sxs-lookup"><span data-stu-id="26832-156">Example: 50000</span></span>  
9. <span data-ttu-id="26832-157">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="26832-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="26832-158">Vytvoření materiálového plánu pro vedlejší produkty</span><span class="sxs-lookup"><span data-stu-id="26832-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="26832-159">V poli Plán kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="26832-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="26832-160">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="26832-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="26832-161">Příklad: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="26832-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="26832-162">Klikněte na položku Spustit.</span><span class="sxs-lookup"><span data-stu-id="26832-162">Click Run.</span></span>
4. <span data-ttu-id="26832-163">Rozbalte nebo sbalte oddíl Záznamy k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="26832-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="26832-164">Klepněte na tlačítko Filtr.</span><span class="sxs-lookup"><span data-stu-id="26832-164">Click Filter.</span></span>
6. <span data-ttu-id="26832-165">V seznamu vyberte řádek pro pole = číslo položky.</span><span class="sxs-lookup"><span data-stu-id="26832-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="26832-166">Zadejte hodnotu do pole Kritéria.</span><span class="sxs-lookup"><span data-stu-id="26832-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="26832-167">Příklad: P6003</span><span class="sxs-lookup"><span data-stu-id="26832-167">Example: P6003</span></span>  
8. <span data-ttu-id="26832-168">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="26832-168">Click OK.</span></span>
9. <span data-ttu-id="26832-169">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="26832-169">Click OK.</span></span>
10. <span data-ttu-id="26832-170">Klikněte na Plánované objednávky.</span><span class="sxs-lookup"><span data-stu-id="26832-170">Click Planned orders.</span></span>
11. <span data-ttu-id="26832-171">Použijte rychlý filtr pro hledání záznamů.</span><span class="sxs-lookup"><span data-stu-id="26832-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="26832-172">Můžete například filtrovat pole Číslo položky pomocí hodnoty „P6000“.</span><span class="sxs-lookup"><span data-stu-id="26832-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="26832-173">Filtrujte podle položky receptury, která má vedlejší produkt položky, pro kterou jste vytvořili prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="26832-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="26832-174">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="26832-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="26832-175">Vyberte libovolné řádky vrácené filtrem.</span><span class="sxs-lookup"><span data-stu-id="26832-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="26832-176">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="26832-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="26832-177">Rozbalte nebo sbalte oddíl Doložení.</span><span class="sxs-lookup"><span data-stu-id="26832-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="26832-178">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="26832-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="26832-179">Plánovaná objednávka je doložena v prodejní objednávce pro vedlejší produkt.</span><span class="sxs-lookup"><span data-stu-id="26832-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="26832-180">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="26832-180">Close the page.</span></span>
17. <span data-ttu-id="26832-181">Klikněte na Hlavní plánování.</span><span class="sxs-lookup"><span data-stu-id="26832-181">Click Master planning.</span></span>
18. <span data-ttu-id="26832-182">Přejděte na Hlavní plánování > Nastavení > Parametry hlavního plánování.</span><span class="sxs-lookup"><span data-stu-id="26832-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="26832-183">V poli Zakázat všechny procesy plánování vyberte Ne.</span><span class="sxs-lookup"><span data-stu-id="26832-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="26832-184">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="26832-184">Close the page.</span></span>


