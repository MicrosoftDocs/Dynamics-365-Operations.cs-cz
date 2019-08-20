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
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0087c53d9cdc3bb65e6fa446c193c752d0f9b4fc
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845075"
---
# <a name="create-boms-february-2016"></a><span data-ttu-id="d8165-103">Vytvoření kusovníků (únor 2016)</span><span class="sxs-lookup"><span data-stu-id="d8165-103">Create BOMs (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d8165-104">Tato úloha je zaměřena na vytvoření struktury kusovníků pro dokončený produkt a polotovar produktu.</span><span class="sxs-lookup"><span data-stu-id="d8165-104">This task focuses on creating the bill of materials structure for a finished product and a semi-finished product.</span></span> <span data-ttu-id="d8165-105">Je to čtvrtá úloha v řadě Kalkulace kusovníku.</span><span class="sxs-lookup"><span data-stu-id="d8165-105">It is the fourth task in the BOM calculation series.</span></span> <span data-ttu-id="d8165-106">Tento úkol byl vytvořen pomocí ukázkových dat společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="d8165-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-bom-for-a-semi-finished-product"></a><span data-ttu-id="d8165-107">Vytvoření kusovníku pro polotovar produktu</span><span class="sxs-lookup"><span data-stu-id="d8165-107">Create BOM for a semi-finished product</span></span>
1. <span data-ttu-id="d8165-108">Přejděte na možnosti Řízení informací o produktech > Produkty > Uvolněné produkty.</span><span class="sxs-lookup"><span data-stu-id="d8165-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="d8165-109">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="d8165-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="d8165-110">Vyberte číslo položky BOM_2.</span><span class="sxs-lookup"><span data-stu-id="d8165-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="d8165-111">V podokně akcí klikněte na možnost Analýza.</span><span class="sxs-lookup"><span data-stu-id="d8165-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="d8165-112">Klepněte na Verze kusovníku.</span><span class="sxs-lookup"><span data-stu-id="d8165-112">Click BOM versions.</span></span>
5. <span data-ttu-id="d8165-113">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="d8165-113">Click New.</span></span>
6. <span data-ttu-id="d8165-114">Klikněte na Kusovník a verze kusovníku.</span><span class="sxs-lookup"><span data-stu-id="d8165-114">Click BOM and BOM version.</span></span>
7. <span data-ttu-id="d8165-115">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="d8165-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="d8165-116">Zadejte například typ BOM_2.</span><span class="sxs-lookup"><span data-stu-id="d8165-116">For example, type BOM_2.</span></span>  
8. <span data-ttu-id="d8165-117">V poli Lokalita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d8165-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="d8165-118">V tomto příkladu zadejte nebo vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="d8165-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="d8165-119">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="d8165-119">Click OK.</span></span>
10. <span data-ttu-id="d8165-120">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="d8165-120">Click New.</span></span>
11. <span data-ttu-id="d8165-121">Zadejte hodnotu do pole Číslo zboží.</span><span class="sxs-lookup"><span data-stu-id="d8165-121">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="d8165-122">V tomto příkladu zadejte ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="d8165-122">For this example, type ITEM_C.</span></span>  
12. <span data-ttu-id="d8165-123">V poli Sklad zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d8165-123">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="d8165-124">V tomto příkladu zadejte nebo vyberte 11.</span><span class="sxs-lookup"><span data-stu-id="d8165-124">For this example, enter or select 11.</span></span>  
13. <span data-ttu-id="d8165-125">Klikněte na Záhlaví.</span><span class="sxs-lookup"><span data-stu-id="d8165-125">Click Header.</span></span>
14. <span data-ttu-id="d8165-126">Kliknutím na Schválit kusovníky schválíte.</span><span class="sxs-lookup"><span data-stu-id="d8165-126">Click Approval to approve bills of materials.</span></span>
15. <span data-ttu-id="d8165-127">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="d8165-127">Click OK.</span></span>
16. <span data-ttu-id="d8165-128">Klepněte na možnost Schválit.</span><span class="sxs-lookup"><span data-stu-id="d8165-128">Click Approve.</span></span>
    * <span data-ttu-id="d8165-129">Tlačítko Schválit se nachází na panelu nástrojů v části Verze kusovníků.</span><span class="sxs-lookup"><span data-stu-id="d8165-129">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="d8165-130">Je-li neviditelné, klikněte na Záhlaví v pravém horním rohu stránky Kusovníky, aby se tlačítko Schválit zobrazilo.</span><span class="sxs-lookup"><span data-stu-id="d8165-130">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
17. <span data-ttu-id="d8165-131">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="d8165-131">Click OK.</span></span>
18. <span data-ttu-id="d8165-132">Klepněte na tlačítko Aktivovat.</span><span class="sxs-lookup"><span data-stu-id="d8165-132">Click Activate.</span></span>
19. <span data-ttu-id="d8165-133">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="d8165-133">Close the page.</span></span>
20. <span data-ttu-id="d8165-134">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="d8165-134">Close the page.</span></span>
21. <span data-ttu-id="d8165-135">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="d8165-135">Close the page.</span></span>

## <a name="create-bom-for-a-finished-product"></a><span data-ttu-id="d8165-136">Vytvoření kusovníku pro dokončený produkt</span><span class="sxs-lookup"><span data-stu-id="d8165-136">Create BOM for a finished product</span></span>
1. <span data-ttu-id="d8165-137">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="d8165-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="d8165-138">Vyberte číslo položky BOM_1.</span><span class="sxs-lookup"><span data-stu-id="d8165-138">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="d8165-139">V podokně akcí klikněte na možnost Analýza.</span><span class="sxs-lookup"><span data-stu-id="d8165-139">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="d8165-140">Klepněte na Verze kusovníku.</span><span class="sxs-lookup"><span data-stu-id="d8165-140">Click BOM versions.</span></span>
4. <span data-ttu-id="d8165-141">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="d8165-141">Click New.</span></span>
5. <span data-ttu-id="d8165-142">Klikněte na Kusovník a verze kusovníku.</span><span class="sxs-lookup"><span data-stu-id="d8165-142">Click BOM and BOM version.</span></span>
6. <span data-ttu-id="d8165-143">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="d8165-143">In the Name field, type a value.</span></span>
    * <span data-ttu-id="d8165-144">Zadejte například typ BOM_1.</span><span class="sxs-lookup"><span data-stu-id="d8165-144">For example, type BOM_1.</span></span>  
7. <span data-ttu-id="d8165-145">V poli Lokalita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d8165-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="d8165-146">V tomto příkladu zadejte nebo vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="d8165-146">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="d8165-147">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="d8165-147">Click OK.</span></span>
9. <span data-ttu-id="d8165-148">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="d8165-148">Click New.</span></span>
10. <span data-ttu-id="d8165-149">Zadejte hodnotu do pole Číslo zboží.</span><span class="sxs-lookup"><span data-stu-id="d8165-149">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="d8165-150">V tomto příkladu zadejte ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="d8165-150">For this example, type ITEM_A.</span></span>  
11. <span data-ttu-id="d8165-151">V poli Sklad zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d8165-151">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="d8165-152">V tomto příkladu vyberte 11.</span><span class="sxs-lookup"><span data-stu-id="d8165-152">For this example, select 11.</span></span>  
12. <span data-ttu-id="d8165-153">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="d8165-153">Click New.</span></span>
13. <span data-ttu-id="d8165-154">Zadejte hodnotu do pole Číslo zboží.</span><span class="sxs-lookup"><span data-stu-id="d8165-154">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="d8165-155">V tomto příkladu zadejte ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="d8165-155">For this example, type ITEM_B.</span></span>  
14. <span data-ttu-id="d8165-156">V poli Sklad zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d8165-156">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="d8165-157">V tomto příkladu zadejte nebo vyberte 11.</span><span class="sxs-lookup"><span data-stu-id="d8165-157">For this example, enter or select 11.</span></span>  
15. <span data-ttu-id="d8165-158">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="d8165-158">Click New.</span></span>
16. <span data-ttu-id="d8165-159">Zadejte hodnotu do pole Číslo zboží.</span><span class="sxs-lookup"><span data-stu-id="d8165-159">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="d8165-160">V tomto příkladu zadejte BOM_2.</span><span class="sxs-lookup"><span data-stu-id="d8165-160">For this example, type BOM_2.</span></span>  
17. <span data-ttu-id="d8165-161">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="d8165-161">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="d8165-162">V poli Sklad zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d8165-162">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="d8165-163">V tomto příkladu zadejte nebo vyberte sklad 11.</span><span class="sxs-lookup"><span data-stu-id="d8165-163">For this example, enter or select warehouse 11.</span></span>  
19. <span data-ttu-id="d8165-164">Klikněte na Záhlaví.</span><span class="sxs-lookup"><span data-stu-id="d8165-164">Click Header.</span></span>
20. <span data-ttu-id="d8165-165">Kliknutím na Schválit kusovníky schválíte.</span><span class="sxs-lookup"><span data-stu-id="d8165-165">Click Approval to approve bills of materials.</span></span>
21. <span data-ttu-id="d8165-166">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="d8165-166">Click OK.</span></span>
22. <span data-ttu-id="d8165-167">Klepněte na možnost Schválit.</span><span class="sxs-lookup"><span data-stu-id="d8165-167">Click Approve.</span></span>
    * <span data-ttu-id="d8165-168">Tlačítko Schválit se nachází na panelu nástrojů v části Verze kusovníků.</span><span class="sxs-lookup"><span data-stu-id="d8165-168">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="d8165-169">Je-li neviditelné, klikněte na Záhlaví v pravém horním rohu stránky Kusovníky, aby se tlačítko Schválit zobrazilo.</span><span class="sxs-lookup"><span data-stu-id="d8165-169">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
23. <span data-ttu-id="d8165-170">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="d8165-170">Click OK.</span></span>
24. <span data-ttu-id="d8165-171">Klepněte na tlačítko Aktivovat.</span><span class="sxs-lookup"><span data-stu-id="d8165-171">Click Activate.</span></span>
25. <span data-ttu-id="d8165-172">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="d8165-172">Close the page.</span></span>
26. <span data-ttu-id="d8165-173">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="d8165-173">Close the page.</span></span>
27. <span data-ttu-id="d8165-174">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="d8165-174">Close the page.</span></span>

