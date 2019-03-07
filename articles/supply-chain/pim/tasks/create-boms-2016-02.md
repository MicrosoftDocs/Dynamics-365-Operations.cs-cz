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
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "333201"
---
# <a name="create-boms-february-2016"></a><span data-ttu-id="1cb23-103">Vytvoření kusovníků (únor 2016)</span><span class="sxs-lookup"><span data-stu-id="1cb23-103">Create BOMs (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1cb23-104">Tato úloha je zaměřena na vytvoření struktury kusovníků pro dokončený produkt a polotovar produktu.</span><span class="sxs-lookup"><span data-stu-id="1cb23-104">This task focuses on creating the bill of materials structure for a finished product and a semi-finished product.</span></span> <span data-ttu-id="1cb23-105">Je to čtvrtá úloha v řadě Kalkulace kusovníku.</span><span class="sxs-lookup"><span data-stu-id="1cb23-105">It is the fourth task in the BOM calculation series.</span></span> <span data-ttu-id="1cb23-106">Tento úkol byl vytvořen pomocí ukázkových dat společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="1cb23-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-bom-for-a-semi-finished-product"></a><span data-ttu-id="1cb23-107">Vytvoření kusovníku pro polotovar produktu</span><span class="sxs-lookup"><span data-stu-id="1cb23-107">Create BOM for a semi-finished product</span></span>
1. <span data-ttu-id="1cb23-108">Přejděte na možnosti Řízení informací o produktech > Produkty > Uvolněné produkty.</span><span class="sxs-lookup"><span data-stu-id="1cb23-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="1cb23-109">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="1cb23-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="1cb23-110">Vyberte číslo položky BOM_2.</span><span class="sxs-lookup"><span data-stu-id="1cb23-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="1cb23-111">V podokně akcí klikněte na možnost Analýza.</span><span class="sxs-lookup"><span data-stu-id="1cb23-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="1cb23-112">Klepněte na Verze kusovníku.</span><span class="sxs-lookup"><span data-stu-id="1cb23-112">Click BOM versions.</span></span>
5. <span data-ttu-id="1cb23-113">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="1cb23-113">Click New.</span></span>
6. <span data-ttu-id="1cb23-114">Klikněte na Kusovník a verze kusovníku.</span><span class="sxs-lookup"><span data-stu-id="1cb23-114">Click BOM and BOM version.</span></span>
7. <span data-ttu-id="1cb23-115">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="1cb23-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="1cb23-116">Zadejte například typ BOM_2.</span><span class="sxs-lookup"><span data-stu-id="1cb23-116">For example, type BOM_2.</span></span>  
8. <span data-ttu-id="1cb23-117">V poli Lokalita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1cb23-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="1cb23-118">V tomto příkladu zadejte nebo vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="1cb23-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="1cb23-119">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="1cb23-119">Click OK.</span></span>
10. <span data-ttu-id="1cb23-120">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="1cb23-120">Click New.</span></span>
11. <span data-ttu-id="1cb23-121">Zadejte hodnotu do pole Číslo zboží.</span><span class="sxs-lookup"><span data-stu-id="1cb23-121">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="1cb23-122">V tomto příkladu zadejte ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="1cb23-122">For this example, type ITEM_C.</span></span>  
12. <span data-ttu-id="1cb23-123">V poli Sklad zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1cb23-123">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="1cb23-124">V tomto příkladu zadejte nebo vyberte 11.</span><span class="sxs-lookup"><span data-stu-id="1cb23-124">For this example, enter or select 11.</span></span>  
13. <span data-ttu-id="1cb23-125">Klikněte na Záhlaví.</span><span class="sxs-lookup"><span data-stu-id="1cb23-125">Click Header.</span></span>
14. <span data-ttu-id="1cb23-126">Kliknutím na Schválit kusovníky schválíte.</span><span class="sxs-lookup"><span data-stu-id="1cb23-126">Click Approval to approve bills of materials.</span></span>
15. <span data-ttu-id="1cb23-127">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="1cb23-127">Click OK.</span></span>
16. <span data-ttu-id="1cb23-128">Klepněte na možnost Schválit.</span><span class="sxs-lookup"><span data-stu-id="1cb23-128">Click Approve.</span></span>
    * <span data-ttu-id="1cb23-129">Tlačítko Schválit se nachází na panelu nástrojů v části Verze kusovníků.</span><span class="sxs-lookup"><span data-stu-id="1cb23-129">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="1cb23-130">Je-li neviditelné, klikněte na Záhlaví v pravém horním rohu stránky Kusovníky, aby se tlačítko Schválit zobrazilo.</span><span class="sxs-lookup"><span data-stu-id="1cb23-130">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
17. <span data-ttu-id="1cb23-131">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="1cb23-131">Click OK.</span></span>
18. <span data-ttu-id="1cb23-132">Klepněte na tlačítko Aktivovat.</span><span class="sxs-lookup"><span data-stu-id="1cb23-132">Click Activate.</span></span>
19. <span data-ttu-id="1cb23-133">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="1cb23-133">Close the page.</span></span>
20. <span data-ttu-id="1cb23-134">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="1cb23-134">Close the page.</span></span>
21. <span data-ttu-id="1cb23-135">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="1cb23-135">Close the page.</span></span>

## <a name="create-bom-for-a-finished-product"></a><span data-ttu-id="1cb23-136">Vytvoření kusovníku pro dokončený produkt</span><span class="sxs-lookup"><span data-stu-id="1cb23-136">Create BOM for a finished product</span></span>
1. <span data-ttu-id="1cb23-137">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="1cb23-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="1cb23-138">Vyberte číslo položky BOM_1.</span><span class="sxs-lookup"><span data-stu-id="1cb23-138">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="1cb23-139">V podokně akcí klikněte na možnost Analýza.</span><span class="sxs-lookup"><span data-stu-id="1cb23-139">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="1cb23-140">Klepněte na Verze kusovníku.</span><span class="sxs-lookup"><span data-stu-id="1cb23-140">Click BOM versions.</span></span>
4. <span data-ttu-id="1cb23-141">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="1cb23-141">Click New.</span></span>
5. <span data-ttu-id="1cb23-142">Klikněte na Kusovník a verze kusovníku.</span><span class="sxs-lookup"><span data-stu-id="1cb23-142">Click BOM and BOM version.</span></span>
6. <span data-ttu-id="1cb23-143">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="1cb23-143">In the Name field, type a value.</span></span>
    * <span data-ttu-id="1cb23-144">Zadejte například typ BOM_1.</span><span class="sxs-lookup"><span data-stu-id="1cb23-144">For example, type BOM_1.</span></span>  
7. <span data-ttu-id="1cb23-145">V poli Lokalita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1cb23-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="1cb23-146">V tomto příkladu zadejte nebo vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="1cb23-146">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="1cb23-147">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="1cb23-147">Click OK.</span></span>
9. <span data-ttu-id="1cb23-148">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="1cb23-148">Click New.</span></span>
10. <span data-ttu-id="1cb23-149">Zadejte hodnotu do pole Číslo zboží.</span><span class="sxs-lookup"><span data-stu-id="1cb23-149">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="1cb23-150">V tomto příkladu zadejte ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="1cb23-150">For this example, type ITEM_A.</span></span>  
11. <span data-ttu-id="1cb23-151">V poli Sklad zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1cb23-151">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="1cb23-152">V tomto příkladu vyberte 11.</span><span class="sxs-lookup"><span data-stu-id="1cb23-152">For this example, select 11.</span></span>  
12. <span data-ttu-id="1cb23-153">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="1cb23-153">Click New.</span></span>
13. <span data-ttu-id="1cb23-154">Zadejte hodnotu do pole Číslo zboží.</span><span class="sxs-lookup"><span data-stu-id="1cb23-154">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="1cb23-155">V tomto příkladu zadejte ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="1cb23-155">For this example, type ITEM_B.</span></span>  
14. <span data-ttu-id="1cb23-156">V poli Sklad zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1cb23-156">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="1cb23-157">V tomto příkladu zadejte nebo vyberte 11.</span><span class="sxs-lookup"><span data-stu-id="1cb23-157">For this example, enter or select 11.</span></span>  
15. <span data-ttu-id="1cb23-158">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="1cb23-158">Click New.</span></span>
16. <span data-ttu-id="1cb23-159">Zadejte hodnotu do pole Číslo zboží.</span><span class="sxs-lookup"><span data-stu-id="1cb23-159">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="1cb23-160">V tomto příkladu zadejte BOM_2.</span><span class="sxs-lookup"><span data-stu-id="1cb23-160">For this example, type BOM_2.</span></span>  
17. <span data-ttu-id="1cb23-161">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="1cb23-161">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="1cb23-162">V poli Sklad zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1cb23-162">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="1cb23-163">V tomto příkladu zadejte nebo vyberte sklad 11.</span><span class="sxs-lookup"><span data-stu-id="1cb23-163">For this example, enter or select warehouse 11.</span></span>  
19. <span data-ttu-id="1cb23-164">Klikněte na Záhlaví.</span><span class="sxs-lookup"><span data-stu-id="1cb23-164">Click Header.</span></span>
20. <span data-ttu-id="1cb23-165">Kliknutím na Schválit kusovníky schválíte.</span><span class="sxs-lookup"><span data-stu-id="1cb23-165">Click Approval to approve bills of materials.</span></span>
21. <span data-ttu-id="1cb23-166">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="1cb23-166">Click OK.</span></span>
22. <span data-ttu-id="1cb23-167">Klepněte na možnost Schválit.</span><span class="sxs-lookup"><span data-stu-id="1cb23-167">Click Approve.</span></span>
    * <span data-ttu-id="1cb23-168">Tlačítko Schválit se nachází na panelu nástrojů v části Verze kusovníků.</span><span class="sxs-lookup"><span data-stu-id="1cb23-168">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="1cb23-169">Je-li neviditelné, klikněte na Záhlaví v pravém horním rohu stránky Kusovníky, aby se tlačítko Schválit zobrazilo.</span><span class="sxs-lookup"><span data-stu-id="1cb23-169">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
23. <span data-ttu-id="1cb23-170">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="1cb23-170">Click OK.</span></span>
24. <span data-ttu-id="1cb23-171">Klepněte na tlačítko Aktivovat.</span><span class="sxs-lookup"><span data-stu-id="1cb23-171">Click Activate.</span></span>
25. <span data-ttu-id="1cb23-172">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="1cb23-172">Close the page.</span></span>
26. <span data-ttu-id="1cb23-173">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="1cb23-173">Close the page.</span></span>
27. <span data-ttu-id="1cb23-174">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="1cb23-174">Close the page.</span></span>

