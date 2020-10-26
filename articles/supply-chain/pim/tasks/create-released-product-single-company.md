---
title: Vytvoření uvolněného produktu pro jednu společnost
description: Tento postup vás provede vytvořením jednoho uvolněného produktu v kontextu jedné právnické jednotky.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, UnitOfMeasureLookup, DimensionLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 90924c853793a3d70f2f2d46d8a154a19bd7d6bb
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/10/2020
ms.locfileid: "3985502"
---
# <a name="create-a-released-product-for-a-single-company"></a><span data-ttu-id="81d35-103">Vytvoření uvolněného produktu pro jednu společnost</span><span class="sxs-lookup"><span data-stu-id="81d35-103">Create a released product for a single company</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="81d35-104">Tento postup vás provede vytvořením jednoho uvolněného produktu v kontextu jedné právnické jednotky.</span><span class="sxs-lookup"><span data-stu-id="81d35-104">This procedure walks through how to create a single released product in the context of a single legal unit.</span></span> <span data-ttu-id="81d35-105">Po vytvoření uvolněného produktu je produkt okamžitě k dispozici pouze v této jednotce.</span><span class="sxs-lookup"><span data-stu-id="81d35-105">After the released product is created,  it's immediately available in this unit only.</span></span> <span data-ttu-id="81d35-106">Tento postup můžete projít v ukázkových datech společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="81d35-106">You can walk through this procedure in demo data company USMF.</span></span> <span data-ttu-id="81d35-107">Tato úloha je obvykle prováděna návrhářem produktu.</span><span class="sxs-lookup"><span data-stu-id="81d35-107">This task is usually performed by a product designer.</span></span>


## <a name="create-a-released-product"></a><span data-ttu-id="81d35-108">Vytvoření uvolněného produktu</span><span class="sxs-lookup"><span data-stu-id="81d35-108">Create a released product</span></span>
1. <span data-ttu-id="81d35-109">Přejděte na Uvolněné produkty.</span><span class="sxs-lookup"><span data-stu-id="81d35-109">Go to Released products.</span></span>
2. <span data-ttu-id="81d35-110">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="81d35-110">Click New.</span></span>
3. <span data-ttu-id="81d35-111">Zadejte hodnotu do pole Číslo produktu.</span><span class="sxs-lookup"><span data-stu-id="81d35-111">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="81d35-112">Pokud číslo produktu není do pole Číslo produktu zadáno automaticky, zadejte jedinečné číslo produktu.</span><span class="sxs-lookup"><span data-stu-id="81d35-112">If a product number is not automatically entered in the Product number field, type a unique product number.</span></span> <span data-ttu-id="81d35-113">Tento krok je vyžadován, jen pokud nebyla nastavena žádná číselná řada pro čísla produktů.</span><span class="sxs-lookup"><span data-stu-id="81d35-113">This step is only  required if no number sequence has been set up for product numbers.</span></span>  
4. <span data-ttu-id="81d35-114">Do pole Název produktu zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="81d35-114">In the Product name field, type a value.</span></span>
    * <span data-ttu-id="81d35-115">Vyhledávací název je výchozí hodnota pro název produktu.</span><span class="sxs-lookup"><span data-stu-id="81d35-115">The Product name is defaulted to the search name.</span></span> <span data-ttu-id="81d35-116">V případě potřeby můžete vyhledávací název změnit.</span><span class="sxs-lookup"><span data-stu-id="81d35-116">If needed, you can select to change the search name.</span></span>  
5. <span data-ttu-id="81d35-117">V poli Skupina modelů položek kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="81d35-117">In the Item model group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="81d35-118">Skupiny modelů zboží obsahují nastavení určující, jak jsou položky řízeny a zpracovávány při příjmu a výdeji zboží.</span><span class="sxs-lookup"><span data-stu-id="81d35-118">The item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="81d35-119">Nastavení také určuje způsob výpočtu spotřeby položek.</span><span class="sxs-lookup"><span data-stu-id="81d35-119">The settings also determine how the consumption of items are calculated.</span></span>  
6. <span data-ttu-id="81d35-120">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="81d35-120">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="81d35-121">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="81d35-121">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="81d35-122">V poli Skupina položek kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="81d35-122">In the Item group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="81d35-123">Skupiny zboží se používají ke správě skladových zásob tak, že se skladové položky na základě svých vlastností rozdělí na skupiny.</span><span class="sxs-lookup"><span data-stu-id="81d35-123">Item groups are used to manage inventory by dividing inventory items into groups based on item characteristics.</span></span> <span data-ttu-id="81d35-124">Pokud například chcete spravovat způsob, jakým jsou zaúčtovány informace do hlavních účtů, můžete vytvořit řadu různých skupin zboží, které jsou přiřazeny ke konkrétním hlavním účtům.</span><span class="sxs-lookup"><span data-stu-id="81d35-124">For example, to manage how information is posted to main accounts, you can create a series of different item groups that are associated with specific main accounts.</span></span> <span data-ttu-id="81d35-125">Tímto způsobem lze sledovat v různých fázích hodnotu zásob zboží.</span><span class="sxs-lookup"><span data-stu-id="81d35-125">This lets you track the inventory value of items at different stages.</span></span>  
9. <span data-ttu-id="81d35-126">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="81d35-126">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="81d35-127">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="81d35-127">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="81d35-128">V poli Skupina dimenze úložiště kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="81d35-128">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="81d35-129">Dimenze uskladnění řídí způsob uložení položek ve skladu a jejich vydávání.</span><span class="sxs-lookup"><span data-stu-id="81d35-129">The storage dimensions help you control how items are stored and taken from inventory.</span></span> <span data-ttu-id="81d35-130">Dimenze uskladnění mohou například zahrnovat pracoviště a sklad.</span><span class="sxs-lookup"><span data-stu-id="81d35-130">For example, a storage dimension can be Site and Warehouse.</span></span>  
12. <span data-ttu-id="81d35-131">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="81d35-131">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="81d35-132">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="81d35-132">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="81d35-133">V poli Skupina sledovací dimenze kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="81d35-133">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="81d35-134">Skupina sledovacích dimenzí určuje sledovací dimenze, které je možné přidat k produktu.</span><span class="sxs-lookup"><span data-stu-id="81d35-134">The tracking dimension group determines which tracking dimensions you can add to a product.</span></span> <span data-ttu-id="81d35-135">Například číslo dávky a sériové číslo slouží ke sledování skladových položek.</span><span class="sxs-lookup"><span data-stu-id="81d35-135">For example, the batch number and serial number are used to track inventory items.</span></span>  
15. <span data-ttu-id="81d35-136">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="81d35-136">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="81d35-137">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="81d35-137">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="81d35-138">V poli Skladová jednotka kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="81d35-138">In the Inventory unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="81d35-139">Skladová položka určuje, jak je produkt kvantifikován při uložení ve skladu.</span><span class="sxs-lookup"><span data-stu-id="81d35-139">The inventory unit determines how the product is quantified when it's stored in inventory.</span></span>  
18. <span data-ttu-id="81d35-140">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="81d35-140">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="81d35-141">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="81d35-141">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="81d35-142">V poli Nákupní jednotka kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="81d35-142">In the Purchase unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="81d35-143">Nákupní jednotka určuje, jak je produkt kvantifikován při nákupu od dodavatele.</span><span class="sxs-lookup"><span data-stu-id="81d35-143">The purchase unit determines how the product is quantified when it's purchased from a vendor.</span></span>  
21. <span data-ttu-id="81d35-144">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="81d35-144">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="81d35-145">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="81d35-145">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="81d35-146">V poli Prodejní jednotka kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="81d35-146">In the Sales unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="81d35-147">Prodejní jednotka určuje, jak je produkt kvantifikován při prodeji odběrateli.</span><span class="sxs-lookup"><span data-stu-id="81d35-147">The sales unit determines how the product is quantified when it's sold to a customer.</span></span>  
24. <span data-ttu-id="81d35-148">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="81d35-148">In the list, find and select the desired record.</span></span>
25. <span data-ttu-id="81d35-149">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="81d35-149">In the list, click the link in the selected row.</span></span>
26. <span data-ttu-id="81d35-150">V poli Jedn.kusov. kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="81d35-150">In the BOM unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="81d35-151">Jedn.kusov. určuje, jak je produkt kvantifikován při jeho zahrnutí do kusovníku (BOM).</span><span class="sxs-lookup"><span data-stu-id="81d35-151">The BOM unit determines how the product is quantified when including it in a bill of materials (BOM).</span></span>  
27. <span data-ttu-id="81d35-152">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="81d35-152">In the list, find and select the desired record.</span></span>
28. <span data-ttu-id="81d35-153">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="81d35-153">In the list, click the link in the selected row.</span></span>
29. <span data-ttu-id="81d35-154">V poli Skupina DPH zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="81d35-154">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="81d35-155">Skupina DPH položky ve skupině zdanění prodeje určuje způsob výpočtu DPH pro každou položku.</span><span class="sxs-lookup"><span data-stu-id="81d35-155">The item sales tax group in the Sales taxation group determines how sales tax is calculated for each item.</span></span>  
30. <span data-ttu-id="81d35-156">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="81d35-156">In the list, find and select the desired record.</span></span>
31. <span data-ttu-id="81d35-157">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="81d35-157">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="81d35-158">V poli Skupina DPH zboží kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="81d35-158">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="81d35-159">Skupina DPH položky ve skupině zdanění nákupu určuje způsob výpočtu nákupní daně pro každou položku.</span><span class="sxs-lookup"><span data-stu-id="81d35-159">The item sales tax group in the Purchase taxation group determines how purchase tax is calculated for each item.</span></span>  
33. <span data-ttu-id="81d35-160">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="81d35-160">In the list, find and select the desired record.</span></span>
34. <span data-ttu-id="81d35-161">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="81d35-161">In the list, click the link in the selected row.</span></span>
35. <span data-ttu-id="81d35-162">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="81d35-162">Click OK.</span></span>

## <a name="add-product-characteristics"></a><span data-ttu-id="81d35-163">Přidání vlastností produktu</span><span class="sxs-lookup"><span data-stu-id="81d35-163">Add product characteristics</span></span>
1. <span data-ttu-id="81d35-164">Rozbalte nebo sbalte oddíl Spravovat sklad.</span><span class="sxs-lookup"><span data-stu-id="81d35-164">Expand or collapse the Manage inventory section.</span></span>
2. <span data-ttu-id="81d35-165">V poli Čistá hmotnost zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="81d35-165">In the Net weight field, enter a number.</span></span>
3. <span data-ttu-id="81d35-166">V poli Váha obalu zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="81d35-166">In the Tare weight field, enter a number.</span></span>
4. <span data-ttu-id="81d35-167">V poli Celková hloubka zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="81d35-167">In the Gross depth field, enter a number.</span></span>
5. <span data-ttu-id="81d35-168">V poli Celková šířka zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="81d35-168">In the Gross width field, enter a number.</span></span>
6. <span data-ttu-id="81d35-169">V poli Celková výška zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="81d35-169">In the Gross height field, enter a number.</span></span>
7. <span data-ttu-id="81d35-170">V poli Objem zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="81d35-170">In the Volume field, enter a number.</span></span>

## <a name="add-financial-dimensions"></a><span data-ttu-id="81d35-171">Přidání finančních dimenzí</span><span class="sxs-lookup"><span data-stu-id="81d35-171">Add financial dimensions</span></span>
1. <span data-ttu-id="81d35-172">Rozbalte nebo sbalte oddíl Finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="81d35-172">Expand or collapse the Financial dimensions section.</span></span>
2. <span data-ttu-id="81d35-173">V poli Obchodní jednotka kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="81d35-173">In the BusinessUnit field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="81d35-174">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="81d35-174">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="81d35-175">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="81d35-175">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="81d35-176">V poli Nákladové středisko kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="81d35-176">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="81d35-177">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="81d35-177">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="81d35-178">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="81d35-178">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="81d35-179">V poli Oddělení kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="81d35-179">In the Department field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="81d35-180">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="81d35-180">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="81d35-181">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="81d35-181">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="81d35-182">V poli Skupina položek kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="81d35-182">In the ItemGroup field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="81d35-183">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="81d35-183">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="81d35-184">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="81d35-184">In the list, click the link in the selected row.</span></span>

