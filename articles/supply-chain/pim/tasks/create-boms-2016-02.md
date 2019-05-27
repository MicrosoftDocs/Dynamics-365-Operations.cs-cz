---
title: Vytvoření kusovníků (únor 2016)
description: Tato úloha je zaměřena na vytvoření struktury kusovníků pro dokončený produkt a polotovar produktu.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6c5cfb8aae1a61d14f7a7969f688cb282530840d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568551"
---
# <a name="create-boms-february-2016"></a><span data-ttu-id="33972-103">Vytvoření kusovníků (únor 2016)</span><span class="sxs-lookup"><span data-stu-id="33972-103">Create BOMs (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="33972-104">Tato úloha je zaměřena na vytvoření struktury kusovníků pro dokončený produkt a polotovar produktu.</span><span class="sxs-lookup"><span data-stu-id="33972-104">This task focuses on creating the bill of materials structure for a finished product and a semi-finished product.</span></span> <span data-ttu-id="33972-105">Je to čtvrtá úloha v řadě Kalkulace kusovníku.</span><span class="sxs-lookup"><span data-stu-id="33972-105">It is the fourth task in the BOM calculation series.</span></span> <span data-ttu-id="33972-106">Tento úkol byl vytvořen pomocí ukázkových dat společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="33972-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-bom-for-a-semi-finished-product"></a><span data-ttu-id="33972-107">Vytvoření kusovníku pro polotovar produktu</span><span class="sxs-lookup"><span data-stu-id="33972-107">Create BOM for a semi-finished product</span></span>
1. <span data-ttu-id="33972-108">Přejděte na možnosti Řízení informací o produktech > Produkty > Uvolněné produkty.</span><span class="sxs-lookup"><span data-stu-id="33972-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="33972-109">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="33972-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="33972-110">Vyberte číslo položky BOM_2.</span><span class="sxs-lookup"><span data-stu-id="33972-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="33972-111">V podokně akcí klikněte na možnost Analýza.</span><span class="sxs-lookup"><span data-stu-id="33972-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="33972-112">Klepněte na Verze kusovníku.</span><span class="sxs-lookup"><span data-stu-id="33972-112">Click BOM versions.</span></span>
5. <span data-ttu-id="33972-113">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="33972-113">Click New.</span></span>
6. <span data-ttu-id="33972-114">Klikněte na Kusovník a verze kusovníku.</span><span class="sxs-lookup"><span data-stu-id="33972-114">Click BOM and BOM version.</span></span>
7. <span data-ttu-id="33972-115">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="33972-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="33972-116">Zadejte například typ BOM_2.</span><span class="sxs-lookup"><span data-stu-id="33972-116">For example, type BOM_2.</span></span>  
8. <span data-ttu-id="33972-117">V poli Lokalita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="33972-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="33972-118">V tomto příkladu zadejte nebo vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="33972-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="33972-119">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="33972-119">Click OK.</span></span>
10. <span data-ttu-id="33972-120">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="33972-120">Click New.</span></span>
11. <span data-ttu-id="33972-121">Zadejte hodnotu do pole Číslo zboží.</span><span class="sxs-lookup"><span data-stu-id="33972-121">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="33972-122">V tomto příkladu zadejte ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="33972-122">For this example, type ITEM_C.</span></span>  
12. <span data-ttu-id="33972-123">V poli Sklad zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="33972-123">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="33972-124">V tomto příkladu zadejte nebo vyberte 11.</span><span class="sxs-lookup"><span data-stu-id="33972-124">For this example, enter or select 11.</span></span>  
13. <span data-ttu-id="33972-125">Klikněte na Záhlaví.</span><span class="sxs-lookup"><span data-stu-id="33972-125">Click Header.</span></span>
14. <span data-ttu-id="33972-126">Kliknutím na Schválit kusovníky schválíte.</span><span class="sxs-lookup"><span data-stu-id="33972-126">Click Approval to approve bills of materials.</span></span>
15. <span data-ttu-id="33972-127">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="33972-127">Click OK.</span></span>
16. <span data-ttu-id="33972-128">Klepněte na možnost Schválit.</span><span class="sxs-lookup"><span data-stu-id="33972-128">Click Approve.</span></span>
    * <span data-ttu-id="33972-129">Tlačítko Schválit se nachází na panelu nástrojů v části Verze kusovníků.</span><span class="sxs-lookup"><span data-stu-id="33972-129">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="33972-130">Je-li neviditelné, klikněte na Záhlaví v pravém horním rohu stránky Kusovníky, aby se tlačítko Schválit zobrazilo.</span><span class="sxs-lookup"><span data-stu-id="33972-130">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
17. <span data-ttu-id="33972-131">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="33972-131">Click OK.</span></span>
18. <span data-ttu-id="33972-132">Klepněte na tlačítko Aktivovat.</span><span class="sxs-lookup"><span data-stu-id="33972-132">Click Activate.</span></span>
19. <span data-ttu-id="33972-133">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="33972-133">Close the page.</span></span>
20. <span data-ttu-id="33972-134">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="33972-134">Close the page.</span></span>
21. <span data-ttu-id="33972-135">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="33972-135">Close the page.</span></span>

## <a name="create-bom-for-a-finished-product"></a><span data-ttu-id="33972-136">Vytvoření kusovníku pro dokončený produkt</span><span class="sxs-lookup"><span data-stu-id="33972-136">Create BOM for a finished product</span></span>
1. <span data-ttu-id="33972-137">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="33972-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="33972-138">Vyberte číslo položky BOM_1.</span><span class="sxs-lookup"><span data-stu-id="33972-138">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="33972-139">V podokně akcí klikněte na možnost Analýza.</span><span class="sxs-lookup"><span data-stu-id="33972-139">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="33972-140">Klepněte na Verze kusovníku.</span><span class="sxs-lookup"><span data-stu-id="33972-140">Click BOM versions.</span></span>
4. <span data-ttu-id="33972-141">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="33972-141">Click New.</span></span>
5. <span data-ttu-id="33972-142">Klikněte na Kusovník a verze kusovníku.</span><span class="sxs-lookup"><span data-stu-id="33972-142">Click BOM and BOM version.</span></span>
6. <span data-ttu-id="33972-143">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="33972-143">In the Name field, type a value.</span></span>
    * <span data-ttu-id="33972-144">Zadejte například typ BOM_1.</span><span class="sxs-lookup"><span data-stu-id="33972-144">For example, type BOM_1.</span></span>  
7. <span data-ttu-id="33972-145">V poli Lokalita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="33972-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="33972-146">V tomto příkladu zadejte nebo vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="33972-146">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="33972-147">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="33972-147">Click OK.</span></span>
9. <span data-ttu-id="33972-148">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="33972-148">Click New.</span></span>
10. <span data-ttu-id="33972-149">Zadejte hodnotu do pole Číslo zboží.</span><span class="sxs-lookup"><span data-stu-id="33972-149">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="33972-150">V tomto příkladu zadejte ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="33972-150">For this example, type ITEM_A.</span></span>  
11. <span data-ttu-id="33972-151">V poli Sklad zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="33972-151">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="33972-152">V tomto příkladu vyberte 11.</span><span class="sxs-lookup"><span data-stu-id="33972-152">For this example, select 11.</span></span>  
12. <span data-ttu-id="33972-153">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="33972-153">Click New.</span></span>
13. <span data-ttu-id="33972-154">Zadejte hodnotu do pole Číslo zboží.</span><span class="sxs-lookup"><span data-stu-id="33972-154">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="33972-155">V tomto příkladu zadejte ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="33972-155">For this example, type ITEM_B.</span></span>  
14. <span data-ttu-id="33972-156">V poli Sklad zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="33972-156">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="33972-157">V tomto příkladu zadejte nebo vyberte 11.</span><span class="sxs-lookup"><span data-stu-id="33972-157">For this example, enter or select 11.</span></span>  
15. <span data-ttu-id="33972-158">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="33972-158">Click New.</span></span>
16. <span data-ttu-id="33972-159">Zadejte hodnotu do pole Číslo zboží.</span><span class="sxs-lookup"><span data-stu-id="33972-159">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="33972-160">V tomto příkladu zadejte BOM_2.</span><span class="sxs-lookup"><span data-stu-id="33972-160">For this example, type BOM_2.</span></span>  
17. <span data-ttu-id="33972-161">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="33972-161">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="33972-162">V poli Sklad zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="33972-162">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="33972-163">V tomto příkladu zadejte nebo vyberte sklad 11.</span><span class="sxs-lookup"><span data-stu-id="33972-163">For this example, enter or select warehouse 11.</span></span>  
19. <span data-ttu-id="33972-164">Klikněte na Záhlaví.</span><span class="sxs-lookup"><span data-stu-id="33972-164">Click Header.</span></span>
20. <span data-ttu-id="33972-165">Kliknutím na Schválit kusovníky schválíte.</span><span class="sxs-lookup"><span data-stu-id="33972-165">Click Approval to approve bills of materials.</span></span>
21. <span data-ttu-id="33972-166">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="33972-166">Click OK.</span></span>
22. <span data-ttu-id="33972-167">Klepněte na možnost Schválit.</span><span class="sxs-lookup"><span data-stu-id="33972-167">Click Approve.</span></span>
    * <span data-ttu-id="33972-168">Tlačítko Schválit se nachází na panelu nástrojů v části Verze kusovníků.</span><span class="sxs-lookup"><span data-stu-id="33972-168">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="33972-169">Je-li neviditelné, klikněte na Záhlaví v pravém horním rohu stránky Kusovníky, aby se tlačítko Schválit zobrazilo.</span><span class="sxs-lookup"><span data-stu-id="33972-169">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
23. <span data-ttu-id="33972-170">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="33972-170">Click OK.</span></span>
24. <span data-ttu-id="33972-171">Klepněte na tlačítko Aktivovat.</span><span class="sxs-lookup"><span data-stu-id="33972-171">Click Activate.</span></span>
25. <span data-ttu-id="33972-172">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="33972-172">Close the page.</span></span>
26. <span data-ttu-id="33972-173">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="33972-173">Close the page.</span></span>
27. <span data-ttu-id="33972-174">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="33972-174">Close the page.</span></span>

