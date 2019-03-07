---
title: Vytvoření materiálového plánu pro vedlejší produkty
description: Plánovač výroby naplánuje materiálové požadavky na položky, které jsou vedlejšími produkty receptury.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2958f1e5c2e8a0cfa9cc6312f688d3b11b8e013c
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "337134"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="9cfc8-103">Vytvoření materiálového plánu pro vedlejší produkty</span><span class="sxs-lookup"><span data-stu-id="9cfc8-103">Create a material plan for co products</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9cfc8-104">Plánovač výroby naplánuje materiálové požadavky na položky, které jsou vedlejšími produkty receptury.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="9cfc8-105">K vytvoření tohoto postupu jsou použita ukázková data společnosti USP2.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="9cfc8-106">Vytvoření požadavku pro vedlejší produkt</span><span class="sxs-lookup"><span data-stu-id="9cfc8-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="9cfc8-107">Přejděte na výchozí řídicí panel.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="9cfc8-108">Klikněte na Zpracování a dotaz na prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="9cfc8-109">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-109">Click New.</span></span>
4. <span data-ttu-id="9cfc8-110">Klikněte na Prodejní objednávka.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-110">Click Sales order.</span></span>
5. <span data-ttu-id="9cfc8-111">V poli Účet odběratele zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="9cfc8-112">Příklad: US-001</span><span class="sxs-lookup"><span data-stu-id="9cfc8-112">Example: US-001</span></span>  
6. <span data-ttu-id="9cfc8-113">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-113">Click OK.</span></span>
7. <span data-ttu-id="9cfc8-114">Zadejte hodnotu do pole Číslo zboží.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="9cfc8-115">Příklad: P6003</span><span class="sxs-lookup"><span data-stu-id="9cfc8-115">Example: P6003</span></span>  
8. <span data-ttu-id="9cfc8-116">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="9cfc8-117">Příklad: 50000</span><span class="sxs-lookup"><span data-stu-id="9cfc8-117">Example: 50000</span></span>  
9. <span data-ttu-id="9cfc8-118">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="9cfc8-119">Vytvoření materiálového plánu pro vedlejší produkty</span><span class="sxs-lookup"><span data-stu-id="9cfc8-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="9cfc8-120">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-120">Close the page.</span></span>
2. <span data-ttu-id="9cfc8-121">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-121">Close the page.</span></span>
3. <span data-ttu-id="9cfc8-122">Klikněte na Hlavní plánování.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-122">Click Master planning.</span></span>
4. <span data-ttu-id="9cfc8-123">V poli Plán kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="9cfc8-124">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9cfc8-125">Příklad: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="9cfc8-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="9cfc8-126">Klikněte na položku Spustit.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-126">Click Run.</span></span>
7. <span data-ttu-id="9cfc8-127">Rozbalte nebo sbalte oddíl Záznamy k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="9cfc8-128">Klepněte na tlačítko Filtr.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-128">Click Filter.</span></span>
9. <span data-ttu-id="9cfc8-129">V seznamu vyberte řádek pro pole = číslo položky.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="9cfc8-130">Zadejte hodnotu do pole Kritéria.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="9cfc8-131">Příklad: P6003</span><span class="sxs-lookup"><span data-stu-id="9cfc8-131">Example: P6003</span></span>  
11. <span data-ttu-id="9cfc8-132">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-132">Click OK.</span></span>
12. <span data-ttu-id="9cfc8-133">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-133">Click OK.</span></span>
13. <span data-ttu-id="9cfc8-134">Klikněte na Plánované objednávky.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-134">Click Planned orders.</span></span>
14. <span data-ttu-id="9cfc8-135">Použijte rychlý filtr pro hledání záznamů.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="9cfc8-136">Můžete například filtrovat pole Číslo položky pomocí hodnoty „P6000“.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="9cfc8-137">Filtrujte podle položky receptury, která má vedlejší produkt položky, pro kterou jste vytvořili prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="9cfc8-138">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="9cfc8-139">Vyberte libovolné řádky vrácené filtrem.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="9cfc8-140">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="9cfc8-141">Rozbalte nebo sbalte oddíl Doložení.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="9cfc8-142">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9cfc8-143">Plánovaná objednávka je doložena v prodejní objednávce pro vedlejší produkt.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="9cfc8-144">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="9cfc8-145">Vytvoření požadavku pro vedlejší produkt</span><span class="sxs-lookup"><span data-stu-id="9cfc8-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="9cfc8-146">Přejděte na výchozí řídicí panel.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="9cfc8-147">Klikněte na Zpracování a dotaz na prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="9cfc8-148">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-148">Click New.</span></span>
4. <span data-ttu-id="9cfc8-149">Klikněte na Prodejní objednávka.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-149">Click Sales order.</span></span>
5. <span data-ttu-id="9cfc8-150">V poli Účet odběratele zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="9cfc8-151">Příklad: US-001</span><span class="sxs-lookup"><span data-stu-id="9cfc8-151">Example: US-001</span></span>  
6. <span data-ttu-id="9cfc8-152">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-152">Click OK.</span></span>
7. <span data-ttu-id="9cfc8-153">Zadejte hodnotu do pole Číslo zboží.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="9cfc8-154">Příklad: P6003</span><span class="sxs-lookup"><span data-stu-id="9cfc8-154">Example: P6003</span></span>  
8. <span data-ttu-id="9cfc8-155">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="9cfc8-156">Příklad: 50000</span><span class="sxs-lookup"><span data-stu-id="9cfc8-156">Example: 50000</span></span>  
9. <span data-ttu-id="9cfc8-157">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="9cfc8-158">Vytvoření materiálového plánu pro vedlejší produkty</span><span class="sxs-lookup"><span data-stu-id="9cfc8-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="9cfc8-159">V poli Plán kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="9cfc8-160">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9cfc8-161">Příklad: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="9cfc8-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="9cfc8-162">Klikněte na položku Spustit.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-162">Click Run.</span></span>
4. <span data-ttu-id="9cfc8-163">Rozbalte nebo sbalte oddíl Záznamy k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="9cfc8-164">Klepněte na tlačítko Filtr.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-164">Click Filter.</span></span>
6. <span data-ttu-id="9cfc8-165">V seznamu vyberte řádek pro pole = číslo položky.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="9cfc8-166">Zadejte hodnotu do pole Kritéria.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="9cfc8-167">Příklad: P6003</span><span class="sxs-lookup"><span data-stu-id="9cfc8-167">Example: P6003</span></span>  
8. <span data-ttu-id="9cfc8-168">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-168">Click OK.</span></span>
9. <span data-ttu-id="9cfc8-169">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-169">Click OK.</span></span>
10. <span data-ttu-id="9cfc8-170">Klikněte na Plánované objednávky.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-170">Click Planned orders.</span></span>
11. <span data-ttu-id="9cfc8-171">Použijte rychlý filtr pro hledání záznamů.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="9cfc8-172">Můžete například filtrovat pole Číslo položky pomocí hodnoty „P6000“.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="9cfc8-173">Filtrujte podle položky receptury, která má vedlejší produkt položky, pro kterou jste vytvořili prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="9cfc8-174">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="9cfc8-175">Vyberte libovolné řádky vrácené filtrem.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="9cfc8-176">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="9cfc8-177">Rozbalte nebo sbalte oddíl Doložení.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="9cfc8-178">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9cfc8-179">Plánovaná objednávka je doložena v prodejní objednávce pro vedlejší produkt.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="9cfc8-180">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-180">Close the page.</span></span>
17. <span data-ttu-id="9cfc8-181">Klikněte na Hlavní plánování.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-181">Click Master planning.</span></span>
18. <span data-ttu-id="9cfc8-182">Přejděte na Hlavní plánování > Nastavení > Parametry hlavního plánování.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="9cfc8-183">V poli Zakázat všechny procesy plánování vyberte Ne.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="9cfc8-184">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="9cfc8-184">Close the page.</span></span>

