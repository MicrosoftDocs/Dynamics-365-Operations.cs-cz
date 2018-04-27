--- 
title: "Vytváření kusovníků (jen ve verzi z února 2016)"
description: "Tato úloha je zaměřena na vytvoření struktury kusovníků pro dokončený produkt a polotovar produktu."
author: YuyuScheller
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 0cd8d9b90cffe2794b785b2bb391e21ae3b11cf7
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---
# <a name="create-boms-february-2016-only"></a><span data-ttu-id="cde49-103">Vytváření kusovníků (jen ve verzi z února 2016)</span><span class="sxs-lookup"><span data-stu-id="cde49-103">Create BOMs (February 2016 only)</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cde49-104">Tato úloha je zaměřena na vytvoření struktury kusovníků pro dokončený produkt a polotovar produktu.</span><span class="sxs-lookup"><span data-stu-id="cde49-104">This task focuses on creating the bill of materials structure for a finished product and a semi-finished product.</span></span> <span data-ttu-id="cde49-105">Je to čtvrtá úloha v řadě Kalkulace kusovníku.</span><span class="sxs-lookup"><span data-stu-id="cde49-105">It is the fourth task in the BOM calculation series.</span></span> <span data-ttu-id="cde49-106">Tento úkol byl vytvořen pomocí ukázkových dat společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="cde49-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-bom-for-a-semi-finished-product"></a><span data-ttu-id="cde49-107">Vytvoření kusovníku pro polotovar produktu</span><span class="sxs-lookup"><span data-stu-id="cde49-107">Create BOM for a semi-finished product</span></span>
1. <span data-ttu-id="cde49-108">Přejděte na možnosti Řízení informací o produktech > Produkty > Uvolněné produkty.</span><span class="sxs-lookup"><span data-stu-id="cde49-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="cde49-109">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="cde49-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="cde49-110">Vyberte číslo položky BOM_2.</span><span class="sxs-lookup"><span data-stu-id="cde49-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="cde49-111">V podokně akcí klikněte na možnost Analýza.</span><span class="sxs-lookup"><span data-stu-id="cde49-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="cde49-112">Klepněte na Verze kusovníku.</span><span class="sxs-lookup"><span data-stu-id="cde49-112">Click BOM versions.</span></span>
5. <span data-ttu-id="cde49-113">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="cde49-113">Click New.</span></span>
6. <span data-ttu-id="cde49-114">Klikněte na Kusovník a verze kusovníku.</span><span class="sxs-lookup"><span data-stu-id="cde49-114">Click BOM and BOM version.</span></span>
7. <span data-ttu-id="cde49-115">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="cde49-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="cde49-116">Zadejte například typ BOM_2.</span><span class="sxs-lookup"><span data-stu-id="cde49-116">For example, type BOM_2.</span></span>  
8. <span data-ttu-id="cde49-117">V poli Lokalita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="cde49-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="cde49-118">V tomto příkladu zadejte nebo vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="cde49-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="cde49-119">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="cde49-119">Click OK.</span></span>
10. <span data-ttu-id="cde49-120">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="cde49-120">Click New.</span></span>
11. <span data-ttu-id="cde49-121">Zadejte hodnotu do pole Číslo zboží.</span><span class="sxs-lookup"><span data-stu-id="cde49-121">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="cde49-122">V tomto příkladu zadejte ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="cde49-122">For this example, type ITEM_C.</span></span>  
12. <span data-ttu-id="cde49-123">V poli Sklad zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="cde49-123">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="cde49-124">V tomto příkladu zadejte nebo vyberte 11.</span><span class="sxs-lookup"><span data-stu-id="cde49-124">For this example, enter or select 11.</span></span>  
13. <span data-ttu-id="cde49-125">Klikněte na Záhlaví.</span><span class="sxs-lookup"><span data-stu-id="cde49-125">Click Header.</span></span>
14. <span data-ttu-id="cde49-126">Kliknutím na Schválit kusovníky schválíte.</span><span class="sxs-lookup"><span data-stu-id="cde49-126">Click Approval to approve bills of materials.</span></span>
15. <span data-ttu-id="cde49-127">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="cde49-127">Click OK.</span></span>
16. <span data-ttu-id="cde49-128">Klepněte na možnost Schválit.</span><span class="sxs-lookup"><span data-stu-id="cde49-128">Click Approve.</span></span>
    * <span data-ttu-id="cde49-129">Tlačítko Schválit se nachází na panelu nástrojů v části Verze kusovníků.</span><span class="sxs-lookup"><span data-stu-id="cde49-129">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="cde49-130">Je-li neviditelné, klikněte na Záhlaví v pravém horním rohu stránky Kusovníky, aby se tlačítko Schválit zobrazilo.</span><span class="sxs-lookup"><span data-stu-id="cde49-130">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
17. <span data-ttu-id="cde49-131">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="cde49-131">Click OK.</span></span>
18. <span data-ttu-id="cde49-132">Klepněte na tlačítko Aktivovat.</span><span class="sxs-lookup"><span data-stu-id="cde49-132">Click Activate.</span></span>
19. <span data-ttu-id="cde49-133">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="cde49-133">Close the page.</span></span>
20. <span data-ttu-id="cde49-134">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="cde49-134">Close the page.</span></span>
21. <span data-ttu-id="cde49-135">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="cde49-135">Close the page.</span></span>

## <a name="create-bom-for-a-finished-product"></a><span data-ttu-id="cde49-136">Vytvoření kusovníku pro dokončený produkt</span><span class="sxs-lookup"><span data-stu-id="cde49-136">Create BOM for a finished product</span></span>
1. <span data-ttu-id="cde49-137">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="cde49-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="cde49-138">Vyberte číslo položky BOM_1.</span><span class="sxs-lookup"><span data-stu-id="cde49-138">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="cde49-139">V podokně akcí klikněte na možnost Analýza.</span><span class="sxs-lookup"><span data-stu-id="cde49-139">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="cde49-140">Klepněte na Verze kusovníku.</span><span class="sxs-lookup"><span data-stu-id="cde49-140">Click BOM versions.</span></span>
4. <span data-ttu-id="cde49-141">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="cde49-141">Click New.</span></span>
5. <span data-ttu-id="cde49-142">Klikněte na Kusovník a verze kusovníku.</span><span class="sxs-lookup"><span data-stu-id="cde49-142">Click BOM and BOM version.</span></span>
6. <span data-ttu-id="cde49-143">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="cde49-143">In the Name field, type a value.</span></span>
    * <span data-ttu-id="cde49-144">Zadejte například typ BOM_1.</span><span class="sxs-lookup"><span data-stu-id="cde49-144">For example, type BOM_1.</span></span>  
7. <span data-ttu-id="cde49-145">V poli Lokalita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="cde49-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="cde49-146">V tomto příkladu zadejte nebo vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="cde49-146">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="cde49-147">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="cde49-147">Click OK.</span></span>
9. <span data-ttu-id="cde49-148">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="cde49-148">Click New.</span></span>
10. <span data-ttu-id="cde49-149">Zadejte hodnotu do pole Číslo zboží.</span><span class="sxs-lookup"><span data-stu-id="cde49-149">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="cde49-150">V tomto příkladu zadejte ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="cde49-150">For this example, type ITEM_A.</span></span>  
11. <span data-ttu-id="cde49-151">V poli Sklad zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="cde49-151">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="cde49-152">V tomto příkladu vyberte 11.</span><span class="sxs-lookup"><span data-stu-id="cde49-152">For this example, select 11.</span></span>  
12. <span data-ttu-id="cde49-153">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="cde49-153">Click New.</span></span>
13. <span data-ttu-id="cde49-154">Zadejte hodnotu do pole Číslo zboží.</span><span class="sxs-lookup"><span data-stu-id="cde49-154">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="cde49-155">V tomto příkladu zadejte ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="cde49-155">For this example, type ITEM_B.</span></span>  
14. <span data-ttu-id="cde49-156">V poli Sklad zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="cde49-156">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="cde49-157">V tomto příkladu zadejte nebo vyberte 11.</span><span class="sxs-lookup"><span data-stu-id="cde49-157">For this example, enter or select 11.</span></span>  
15. <span data-ttu-id="cde49-158">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="cde49-158">Click New.</span></span>
16. <span data-ttu-id="cde49-159">Zadejte hodnotu do pole Číslo zboží.</span><span class="sxs-lookup"><span data-stu-id="cde49-159">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="cde49-160">V tomto příkladu zadejte BOM_2.</span><span class="sxs-lookup"><span data-stu-id="cde49-160">For this example, type BOM_2.</span></span>  
17. <span data-ttu-id="cde49-161">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="cde49-161">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="cde49-162">V poli Sklad zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="cde49-162">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="cde49-163">V tomto příkladu zadejte nebo vyberte sklad 11.</span><span class="sxs-lookup"><span data-stu-id="cde49-163">For this example, enter or select warehouse 11.</span></span>  
19. <span data-ttu-id="cde49-164">Klikněte na Záhlaví.</span><span class="sxs-lookup"><span data-stu-id="cde49-164">Click Header.</span></span>
20. <span data-ttu-id="cde49-165">Kliknutím na Schválit kusovníky schválíte.</span><span class="sxs-lookup"><span data-stu-id="cde49-165">Click Approval to approve bills of materials.</span></span>
21. <span data-ttu-id="cde49-166">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="cde49-166">Click OK.</span></span>
22. <span data-ttu-id="cde49-167">Klepněte na možnost Schválit.</span><span class="sxs-lookup"><span data-stu-id="cde49-167">Click Approve.</span></span>
    * <span data-ttu-id="cde49-168">Tlačítko Schválit se nachází na panelu nástrojů v části Verze kusovníků.</span><span class="sxs-lookup"><span data-stu-id="cde49-168">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="cde49-169">Je-li neviditelné, klikněte na Záhlaví v pravém horním rohu stránky Kusovníky, aby se tlačítko Schválit zobrazilo.</span><span class="sxs-lookup"><span data-stu-id="cde49-169">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
23. <span data-ttu-id="cde49-170">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="cde49-170">Click OK.</span></span>
24. <span data-ttu-id="cde49-171">Klepněte na tlačítko Aktivovat.</span><span class="sxs-lookup"><span data-stu-id="cde49-171">Click Activate.</span></span>
25. <span data-ttu-id="cde49-172">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="cde49-172">Close the page.</span></span>
26. <span data-ttu-id="cde49-173">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="cde49-173">Close the page.</span></span>
27. <span data-ttu-id="cde49-174">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="cde49-174">Close the page.</span></span>


