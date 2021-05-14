---
title: Vytvoření materiálového plánu pro vedlejší produkty
description: Plánovač výroby naplánuje materiálové požadavky na položky, které jsou vedlejšími produkty receptury.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b51e4b4d00da2babb5128d8c4c22139b0c1853d4
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920722"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="21e8e-103">Vytvoření materiálového plánu pro vedlejší produkty</span><span class="sxs-lookup"><span data-stu-id="21e8e-103">Create a material plan for co products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="21e8e-104">Plánovač výroby naplánuje materiálové požadavky na položky, které jsou vedlejšími produkty receptury.</span><span class="sxs-lookup"><span data-stu-id="21e8e-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="21e8e-105">K vytvoření tohoto postupu jsou použita ukázková data společnosti USP2.</span><span class="sxs-lookup"><span data-stu-id="21e8e-105">The demo data company used to create this procedure is USP2.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="21e8e-106">Vytvoření požadavku pro vedlejší produkt</span><span class="sxs-lookup"><span data-stu-id="21e8e-106">Create requirement for a co-product</span></span>

1. <span data-ttu-id="21e8e-107">Přejděte do **Prodej a marketing \> Pracovní prostory \> Zpracování a poptávka prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="21e8e-107">Go to **Sales and marketing \> Workspaces \> Sales order processing and inquiry**.</span></span>
1. <span data-ttu-id="21e8e-108">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="21e8e-108">Select **New**.</span></span>
1. <span data-ttu-id="21e8e-109">Vyberte **Prodejní objednávka**.</span><span class="sxs-lookup"><span data-stu-id="21e8e-109">Select **Sales order**.</span></span>
1. <span data-ttu-id="21e8e-110">V poli **Účet odběratele** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="21e8e-110">In the **Customer account** field, type a value.</span></span>
    * <span data-ttu-id="21e8e-111">Příklad: US-001</span><span class="sxs-lookup"><span data-stu-id="21e8e-111">Example: US-001</span></span>  
1. <span data-ttu-id="21e8e-112">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="21e8e-112">Select **OK**.</span></span>
1. <span data-ttu-id="21e8e-113">Zadejte hodnotu do pole **Číslo zboží**.</span><span class="sxs-lookup"><span data-stu-id="21e8e-113">In the **Item number** field, type a value.</span></span>
    * <span data-ttu-id="21e8e-114">Příklad: P6003</span><span class="sxs-lookup"><span data-stu-id="21e8e-114">Example: P6003</span></span>  
1. <span data-ttu-id="21e8e-115">Zadejte číslo do pole **Množství**.</span><span class="sxs-lookup"><span data-stu-id="21e8e-115">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="21e8e-116">Příklad: 50000</span><span class="sxs-lookup"><span data-stu-id="21e8e-116">Example: 50000</span></span>  
1. <span data-ttu-id="21e8e-117">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="21e8e-117">Select **Save**.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="21e8e-118">Vytvoření materiálového plánu pro vedlejší produkty</span><span class="sxs-lookup"><span data-stu-id="21e8e-118">Create a material plan for co-products</span></span>

1. <span data-ttu-id="21e8e-119">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="21e8e-119">Close the page.</span></span>
1. <span data-ttu-id="21e8e-120">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="21e8e-120">Close the page.</span></span>
1. <span data-ttu-id="21e8e-121">Vyberte **Hlavní plánování**.</span><span class="sxs-lookup"><span data-stu-id="21e8e-121">Select **Master planning**.</span></span>
1. <span data-ttu-id="21e8e-122">V poli **Plán** zvolením tlačítka rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="21e8e-122">In the **Plan** field, select the drop-down button to open the lookup.</span></span>
1. <span data-ttu-id="21e8e-123">Vyberte odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="21e8e-123">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="21e8e-124">Příklad: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="21e8e-124">Example: MasterPlan</span></span>  
1. <span data-ttu-id="21e8e-125">Vyberte **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="21e8e-125">Select **Run**.</span></span>
1. <span data-ttu-id="21e8e-126">Rozbalte nebo sbalte oddíl **Záznamy k zahrnutí**.</span><span class="sxs-lookup"><span data-stu-id="21e8e-126">Expand or collapse the **Records to include** section.</span></span>
1. <span data-ttu-id="21e8e-127">Vyberte **Filtr**.</span><span class="sxs-lookup"><span data-stu-id="21e8e-127">Select **Filter**.</span></span>
1. <span data-ttu-id="21e8e-128">V seznamu vyberte řádek pro **Pole** = *číslo položky*.</span><span class="sxs-lookup"><span data-stu-id="21e8e-128">In the list, select the row for **Field** = *Item number*.</span></span>
1. <span data-ttu-id="21e8e-129">Zadejte hodnotu do pole **Kritéria**.</span><span class="sxs-lookup"><span data-stu-id="21e8e-129">In the **Criteria** field, type a value.</span></span>
    * <span data-ttu-id="21e8e-130">Příklad: P6003</span><span class="sxs-lookup"><span data-stu-id="21e8e-130">Example: P6003</span></span>  
1. <span data-ttu-id="21e8e-131">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="21e8e-131">Select **OK**.</span></span>
1. <span data-ttu-id="21e8e-132">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="21e8e-132">Select **OK**.</span></span>
1. <span data-ttu-id="21e8e-133">Vyberte **Plánované objednávky**.</span><span class="sxs-lookup"><span data-stu-id="21e8e-133">Select **Planned orders**.</span></span>
1. <span data-ttu-id="21e8e-134">Použijte rychlý filtr pro hledání záznamů.</span><span class="sxs-lookup"><span data-stu-id="21e8e-134">Use the Quick Filter to find records.</span></span> <span data-ttu-id="21e8e-135">Můžete například filtrovat pole **Číslo položky** pomocí hodnoty „P6000“.</span><span class="sxs-lookup"><span data-stu-id="21e8e-135">For example, filter on the **Item number** field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="21e8e-136">Filtrujte podle položky receptury, která má vedlejší produkt položky, pro kterou jste vytvořili prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="21e8e-136">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
1. <span data-ttu-id="21e8e-137">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="21e8e-137">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="21e8e-138">Vyberte libovolné řádky vrácené filtrem.</span><span class="sxs-lookup"><span data-stu-id="21e8e-138">Select any of the rows returned by the filter.</span></span>  
1. <span data-ttu-id="21e8e-139">Vyberte odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="21e8e-139">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="21e8e-140">Rozbalte sekci **Doložení**.</span><span class="sxs-lookup"><span data-stu-id="21e8e-140">Expand the **Pegging** section.</span></span>
1. <span data-ttu-id="21e8e-141">Vyberte odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="21e8e-141">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="21e8e-142">Plánovaná objednávka je doložena v prodejní objednávce pro vedlejší produkt.</span><span class="sxs-lookup"><span data-stu-id="21e8e-142">The planned order is pegged to the sales order for the co-product.</span></span>  
1. <span data-ttu-id="21e8e-143">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="21e8e-143">Close the page.</span></span>

## <a name="create-a-second-requirement-for-a-co-product"></a><span data-ttu-id="21e8e-144">Vytvoření druhého požadavku pro vedlejší produkt</span><span class="sxs-lookup"><span data-stu-id="21e8e-144">Create a second requirement for a co-product</span></span>

1. <span data-ttu-id="21e8e-145">Přejděte do **Prodej a marketing \> Pracovní prostory \> Zpracování a poptávka prodejní objednávky**.</span><span class="sxs-lookup"><span data-stu-id="21e8e-145">Go to **Sales and marketing \> Workspaces \> Sales order processing and inquiry**.</span></span>
1. <span data-ttu-id="21e8e-146">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="21e8e-146">Select **New**.</span></span>
1. <span data-ttu-id="21e8e-147">Vyberte **Prodejní objednávka**.</span><span class="sxs-lookup"><span data-stu-id="21e8e-147">Select **Sales order**.</span></span>
1. <span data-ttu-id="21e8e-148">V poli **Účet odběratele** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="21e8e-148">In the **Customer account** field, type a value.</span></span>
    * <span data-ttu-id="21e8e-149">Příklad: US-001</span><span class="sxs-lookup"><span data-stu-id="21e8e-149">Example: US-001</span></span>  
1. <span data-ttu-id="21e8e-150">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="21e8e-150">Select **OK**.</span></span>
1. <span data-ttu-id="21e8e-151">Zadejte hodnotu do pole **Číslo zboží**.</span><span class="sxs-lookup"><span data-stu-id="21e8e-151">In the **Item number** field, type a value.</span></span>
    * <span data-ttu-id="21e8e-152">Příklad: P6003</span><span class="sxs-lookup"><span data-stu-id="21e8e-152">Example: P6003</span></span>  
1. <span data-ttu-id="21e8e-153">Zadejte číslo do pole **Množství**.</span><span class="sxs-lookup"><span data-stu-id="21e8e-153">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="21e8e-154">Příklad: 50000</span><span class="sxs-lookup"><span data-stu-id="21e8e-154">Example: 50000</span></span>  
1. <span data-ttu-id="21e8e-155">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="21e8e-155">Select **Save**.</span></span>

## <a name="create-a-second-material-plan-for-co-products"></a><span data-ttu-id="21e8e-156">Vytvoření druhého materiálového plánu pro vedlejší produkty</span><span class="sxs-lookup"><span data-stu-id="21e8e-156">Create a second material plan for co-products</span></span>

1. <span data-ttu-id="21e8e-157">V poli **Plán** zvolením tlačítka rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="21e8e-157">In the **Plan** field, select the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="21e8e-158">Vyberte odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="21e8e-158">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="21e8e-159">Příklad: MasterPlan</span><span class="sxs-lookup"><span data-stu-id="21e8e-159">Example: MasterPlan</span></span>  
3. <span data-ttu-id="21e8e-160">Vyberte **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="21e8e-160">Select **Run**.</span></span>
4. <span data-ttu-id="21e8e-161">Rozbalte nebo sbalte oddíl **Záznamy k zahrnutí**.</span><span class="sxs-lookup"><span data-stu-id="21e8e-161">Expand or collapse the **Records to include** section.</span></span>
5. <span data-ttu-id="21e8e-162">Vyberte **Filtr**.</span><span class="sxs-lookup"><span data-stu-id="21e8e-162">Select **Filter**.</span></span>
6. <span data-ttu-id="21e8e-163">V seznamu vyberte řádek pro **Pole** = *číslo položky*.</span><span class="sxs-lookup"><span data-stu-id="21e8e-163">In the list, select the row for **Field** = *Item number*.</span></span>
7. <span data-ttu-id="21e8e-164">Zadejte hodnotu do pole *Kritéria*.</span><span class="sxs-lookup"><span data-stu-id="21e8e-164">In the *Criteria* field, type a value.</span></span>
    * <span data-ttu-id="21e8e-165">Příklad: P6003</span><span class="sxs-lookup"><span data-stu-id="21e8e-165">Example: P6003</span></span>  
8. <span data-ttu-id="21e8e-166">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="21e8e-166">Select **OK**.</span></span>
9. <span data-ttu-id="21e8e-167">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="21e8e-167">Select **OK**.</span></span>
10. <span data-ttu-id="21e8e-168">Vyberte **Plánované objednávky**.</span><span class="sxs-lookup"><span data-stu-id="21e8e-168">Select **Planned orders**.</span></span>
11. <span data-ttu-id="21e8e-169">Použijte rychlý filtr pro hledání záznamů.</span><span class="sxs-lookup"><span data-stu-id="21e8e-169">Use the Quick Filter to find records.</span></span> <span data-ttu-id="21e8e-170">Můžete například filtrovat pole **Číslo položky** pomocí hodnoty „P6000“.</span><span class="sxs-lookup"><span data-stu-id="21e8e-170">For example, filter on the **Item number** field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="21e8e-171">Filtrujte podle položky receptury, která má vedlejší produkt položky, pro kterou jste vytvořili prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="21e8e-171">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="21e8e-172">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="21e8e-172">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="21e8e-173">Vyberte libovolné řádky vrácené filtrem.</span><span class="sxs-lookup"><span data-stu-id="21e8e-173">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="21e8e-174">Vyberte odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="21e8e-174">In the list, select the link in the selected row.</span></span>
14. <span data-ttu-id="21e8e-175">Rozbalte nebo sbalte oddíl **Doložení**.</span><span class="sxs-lookup"><span data-stu-id="21e8e-175">Expand or collapse the **Pegging** section.</span></span>
15. <span data-ttu-id="21e8e-176">Vyberte odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="21e8e-176">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="21e8e-177">Plánovaná objednávka je doložena v prodejní objednávce pro vedlejší produkt.</span><span class="sxs-lookup"><span data-stu-id="21e8e-177">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="21e8e-178">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="21e8e-178">Close the page.</span></span>
17. <span data-ttu-id="21e8e-179">Vyberte **Hlavní plánování**.</span><span class="sxs-lookup"><span data-stu-id="21e8e-179">Select **Master planning**.</span></span>
18. <span data-ttu-id="21e8e-180">Přejděte na **Hlavní plánování \> Nastavení \> Parametry hlavního plánování**.</span><span class="sxs-lookup"><span data-stu-id="21e8e-180">Go to **Master planning \> Setup \> Master planning parameters**.</span></span>
19. <span data-ttu-id="21e8e-181">V poli **Zakázat všechny procesy plánování** vyberte *Ne*.</span><span class="sxs-lookup"><span data-stu-id="21e8e-181">Select *No* in the **Disable all planning processes** field.</span></span>
20. <span data-ttu-id="21e8e-182">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="21e8e-182">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]