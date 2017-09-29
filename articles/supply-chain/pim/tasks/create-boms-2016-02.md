--- 
title: "Vytváření kusovníků (jen ve verzi z února 2016)"
description: "Tato úloha je zaměřena na vytvoření struktury kusovníků pro dokončený produkt a polotovar produktu."
author: BibiSp
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: f8ad4b0e230fb0f018355e486e3b898895a61f28
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---
# <a name="create-boms-february-2016-only"></a><span data-ttu-id="ef630-103">Vytváření kusovníků (jen ve verzi z února 2016)</span><span class="sxs-lookup"><span data-stu-id="ef630-103">Create BOMs (February 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ef630-104">Tato úloha je zaměřena na vytvoření struktury kusovníků pro dokončený produkt a polotovar produktu.</span><span class="sxs-lookup"><span data-stu-id="ef630-104">This task focuses on creating the bill of materials structure for a finished product and a semi-finished product.</span></span> <span data-ttu-id="ef630-105">Je to čtvrtá úloha v řadě Kalkulace kusovníku.</span><span class="sxs-lookup"><span data-stu-id="ef630-105">It is the fourth task in the BOM calculation series.</span></span> <span data-ttu-id="ef630-106">Tento úkol byl vytvořen pomocí ukázkových dat společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="ef630-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-bom-for-a-semi-finished-product"></a><span data-ttu-id="ef630-107">Vytvoření kusovníku pro polotovar produktu</span><span class="sxs-lookup"><span data-stu-id="ef630-107">Create BOM for a semi-finished product</span></span>
1. <span data-ttu-id="ef630-108">Přejděte na možnosti Řízení informací o produktech > Produkty > Uvolněné produkty.</span><span class="sxs-lookup"><span data-stu-id="ef630-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="ef630-109">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="ef630-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ef630-110">Vyberte číslo položky BOM_2.</span><span class="sxs-lookup"><span data-stu-id="ef630-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="ef630-111">V podokně akcí klikněte na možnost Analýza.</span><span class="sxs-lookup"><span data-stu-id="ef630-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="ef630-112">Klepněte na Verze kusovníku.</span><span class="sxs-lookup"><span data-stu-id="ef630-112">Click BOM versions.</span></span>
5. <span data-ttu-id="ef630-113">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="ef630-113">Click New.</span></span>
6. <span data-ttu-id="ef630-114">Klikněte na Kusovník a verze kusovníku.</span><span class="sxs-lookup"><span data-stu-id="ef630-114">Click BOM and BOM version.</span></span>
7. <span data-ttu-id="ef630-115">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="ef630-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="ef630-116">Zadejte například typ BOM_2.</span><span class="sxs-lookup"><span data-stu-id="ef630-116">For example, type BOM_2.</span></span>  
8. <span data-ttu-id="ef630-117">V poli Lokalita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ef630-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="ef630-118">V tomto příkladu zadejte nebo vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="ef630-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="ef630-119">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="ef630-119">Click OK.</span></span>
10. <span data-ttu-id="ef630-120">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="ef630-120">Click New.</span></span>
11. <span data-ttu-id="ef630-121">Zadejte hodnotu do pole Číslo zboží.</span><span class="sxs-lookup"><span data-stu-id="ef630-121">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="ef630-122">V tomto příkladu zadejte ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="ef630-122">For this example, type ITEM_C.</span></span>  
12. <span data-ttu-id="ef630-123">V poli Sklad zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ef630-123">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="ef630-124">V tomto příkladu zadejte nebo vyberte 11.</span><span class="sxs-lookup"><span data-stu-id="ef630-124">For this example, enter or select 11.</span></span>  
13. <span data-ttu-id="ef630-125">Klikněte na Záhlaví.</span><span class="sxs-lookup"><span data-stu-id="ef630-125">Click Header.</span></span>
14. <span data-ttu-id="ef630-126">Kliknutím na Schválit kusovníky schválíte.</span><span class="sxs-lookup"><span data-stu-id="ef630-126">Click Approval to approve bills of materials.</span></span>
15. <span data-ttu-id="ef630-127">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="ef630-127">Click OK.</span></span>
16. <span data-ttu-id="ef630-128">Klepněte na možnost Schválit.</span><span class="sxs-lookup"><span data-stu-id="ef630-128">Click Approve.</span></span>
    * <span data-ttu-id="ef630-129">Tlačítko Schválit se nachází na panelu nástrojů v části Verze kusovníků.</span><span class="sxs-lookup"><span data-stu-id="ef630-129">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="ef630-130">Je-li neviditelné, klikněte na Záhlaví v pravém horním rohu stránky Kusovníky, aby se tlačítko Schválit zobrazilo.</span><span class="sxs-lookup"><span data-stu-id="ef630-130">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
17. <span data-ttu-id="ef630-131">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="ef630-131">Click OK.</span></span>
18. <span data-ttu-id="ef630-132">Klepněte na tlačítko Aktivovat.</span><span class="sxs-lookup"><span data-stu-id="ef630-132">Click Activate.</span></span>
19. <span data-ttu-id="ef630-133">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ef630-133">Close the page.</span></span>
20. <span data-ttu-id="ef630-134">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ef630-134">Close the page.</span></span>
21. <span data-ttu-id="ef630-135">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ef630-135">Close the page.</span></span>

## <a name="create-bom-for-a-finished-product"></a><span data-ttu-id="ef630-136">Vytvoření kusovníku pro dokončený produkt</span><span class="sxs-lookup"><span data-stu-id="ef630-136">Create BOM for a finished product</span></span>
1. <span data-ttu-id="ef630-137">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="ef630-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ef630-138">Vyberte číslo položky BOM_1.</span><span class="sxs-lookup"><span data-stu-id="ef630-138">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="ef630-139">V podokně akcí klikněte na možnost Analýza.</span><span class="sxs-lookup"><span data-stu-id="ef630-139">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="ef630-140">Klepněte na Verze kusovníku.</span><span class="sxs-lookup"><span data-stu-id="ef630-140">Click BOM versions.</span></span>
4. <span data-ttu-id="ef630-141">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="ef630-141">Click New.</span></span>
5. <span data-ttu-id="ef630-142">Klikněte na Kusovník a verze kusovníku.</span><span class="sxs-lookup"><span data-stu-id="ef630-142">Click BOM and BOM version.</span></span>
6. <span data-ttu-id="ef630-143">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="ef630-143">In the Name field, type a value.</span></span>
    * <span data-ttu-id="ef630-144">Zadejte například typ BOM_1.</span><span class="sxs-lookup"><span data-stu-id="ef630-144">For example, type BOM_1.</span></span>  
7. <span data-ttu-id="ef630-145">V poli Lokalita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ef630-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="ef630-146">V tomto příkladu zadejte nebo vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="ef630-146">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="ef630-147">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="ef630-147">Click OK.</span></span>
9. <span data-ttu-id="ef630-148">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="ef630-148">Click New.</span></span>
10. <span data-ttu-id="ef630-149">Zadejte hodnotu do pole Číslo zboží.</span><span class="sxs-lookup"><span data-stu-id="ef630-149">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="ef630-150">V tomto příkladu zadejte ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="ef630-150">For this example, type ITEM_A.</span></span>  
11. <span data-ttu-id="ef630-151">V poli Sklad zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ef630-151">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="ef630-152">V tomto příkladu vyberte 11.</span><span class="sxs-lookup"><span data-stu-id="ef630-152">For this example, select 11.</span></span>  
12. <span data-ttu-id="ef630-153">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="ef630-153">Click New.</span></span>
13. <span data-ttu-id="ef630-154">Zadejte hodnotu do pole Číslo zboží.</span><span class="sxs-lookup"><span data-stu-id="ef630-154">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="ef630-155">V tomto příkladu zadejte ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="ef630-155">For this example, type ITEM_B.</span></span>  
14. <span data-ttu-id="ef630-156">V poli Sklad zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ef630-156">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="ef630-157">V tomto příkladu zadejte nebo vyberte 11.</span><span class="sxs-lookup"><span data-stu-id="ef630-157">For this example, enter or select 11.</span></span>  
15. <span data-ttu-id="ef630-158">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="ef630-158">Click New.</span></span>
16. <span data-ttu-id="ef630-159">Zadejte hodnotu do pole Číslo zboží.</span><span class="sxs-lookup"><span data-stu-id="ef630-159">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="ef630-160">V tomto příkladu zadejte BOM_2.</span><span class="sxs-lookup"><span data-stu-id="ef630-160">For this example, type BOM_2.</span></span>  
17. <span data-ttu-id="ef630-161">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="ef630-161">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="ef630-162">V poli Sklad zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ef630-162">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="ef630-163">V tomto příkladu zadejte nebo vyberte sklad 11.</span><span class="sxs-lookup"><span data-stu-id="ef630-163">For this example, enter or select warehouse 11.</span></span>  
19. <span data-ttu-id="ef630-164">Klikněte na Záhlaví.</span><span class="sxs-lookup"><span data-stu-id="ef630-164">Click Header.</span></span>
20. <span data-ttu-id="ef630-165">Kliknutím na Schválit kusovníky schválíte.</span><span class="sxs-lookup"><span data-stu-id="ef630-165">Click Approval to approve bills of materials.</span></span>
21. <span data-ttu-id="ef630-166">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="ef630-166">Click OK.</span></span>
22. <span data-ttu-id="ef630-167">Klepněte na možnost Schválit.</span><span class="sxs-lookup"><span data-stu-id="ef630-167">Click Approve.</span></span>
    * <span data-ttu-id="ef630-168">Tlačítko Schválit se nachází na panelu nástrojů v části Verze kusovníků.</span><span class="sxs-lookup"><span data-stu-id="ef630-168">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="ef630-169">Je-li neviditelné, klikněte na Záhlaví v pravém horním rohu stránky Kusovníky, aby se tlačítko Schválit zobrazilo.</span><span class="sxs-lookup"><span data-stu-id="ef630-169">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
23. <span data-ttu-id="ef630-170">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="ef630-170">Click OK.</span></span>
24. <span data-ttu-id="ef630-171">Klepněte na tlačítko Aktivovat.</span><span class="sxs-lookup"><span data-stu-id="ef630-171">Click Activate.</span></span>
25. <span data-ttu-id="ef630-172">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ef630-172">Close the page.</span></span>
26. <span data-ttu-id="ef630-173">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ef630-173">Close the page.</span></span>
27. <span data-ttu-id="ef630-174">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ef630-174">Close the page.</span></span>


