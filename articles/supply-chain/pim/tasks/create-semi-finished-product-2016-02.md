--- 
title: "Vytvoření polotovaru produktu (únor 2016)"
description: "Tato úloha je zaměřena na vytvoření polotovaru produktu."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, InventItemPrice
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 9caeae552471eed1cb1d8630f387ca31107fcece
ms.contentlocale: cs-cz
ms.lasthandoff: 09/14/2018

---
# <a name="create-a-semi-finished-product-february-2016"></a><span data-ttu-id="dc73b-103">Vytvoření polotovaru produktu (únor 2016)</span><span class="sxs-lookup"><span data-stu-id="dc73b-103">Create a semi-finished product (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dc73b-104">Tato úloha je zaměřena na vytvoření polotovaru produktu.</span><span class="sxs-lookup"><span data-stu-id="dc73b-104">This task focuses on creating a semi-finished product.</span></span> <span data-ttu-id="dc73b-105">Je to druhá úloha v řadě Kalkulace kusovníku.</span><span class="sxs-lookup"><span data-stu-id="dc73b-105">It is the second task in the BOM calculation series.</span></span> <span data-ttu-id="dc73b-106">Tento úkol byl vytvořen pomocí ukázkových dat společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="dc73b-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="dc73b-107">Přejděte na možnosti Řízení informací o produktech > Produkty > Uvolněné produkty.</span><span class="sxs-lookup"><span data-stu-id="dc73b-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="dc73b-108">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="dc73b-108">Click New.</span></span>
3. <span data-ttu-id="dc73b-109">Zadejte hodnotu do pole Číslo produktu.</span><span class="sxs-lookup"><span data-stu-id="dc73b-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="dc73b-110">V tomto příkladu zadejte BOM_2.</span><span class="sxs-lookup"><span data-stu-id="dc73b-110">For this example, type BOM_2.</span></span>  
4. <span data-ttu-id="dc73b-111">V poli Skupina modelů zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="dc73b-111">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="dc73b-112">Vyberte volbu „STD“.</span><span class="sxs-lookup"><span data-stu-id="dc73b-112">Select STD.</span></span> <span data-ttu-id="dc73b-113">STD zastupuje standardní náklady a je to nejčastěji používaný model při práci s výpočty nákladů.</span><span class="sxs-lookup"><span data-stu-id="dc73b-113">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="dc73b-114">V poli Skupina zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="dc73b-114">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="dc73b-115">Vyberte například Audio.</span><span class="sxs-lookup"><span data-stu-id="dc73b-115">For example, select Audio.</span></span> <span data-ttu-id="dc73b-116">To nemá žádný vliv na výpočty nákladů.</span><span class="sxs-lookup"><span data-stu-id="dc73b-116">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="dc73b-117">V poli Skupina dimenze úložiště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="dc73b-117">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="dc73b-118">Vyberte SiteWH.</span><span class="sxs-lookup"><span data-stu-id="dc73b-118">Select SiteWH.</span></span> <span data-ttu-id="dc73b-119">Pro tento příklad se použije pouze Pracoviště a Sklad.</span><span class="sxs-lookup"><span data-stu-id="dc73b-119">Only Site and Warehouse will be used for this example.</span></span>  
7. <span data-ttu-id="dc73b-120">V poli Skupina sledovací dimenze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="dc73b-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="dc73b-121">Sledovací dimenze v tomto příkladu nebudou použity, vyberte Žádné.</span><span class="sxs-lookup"><span data-stu-id="dc73b-121">Tracking dimensions will not be used for this example, select None.</span></span>  
8. <span data-ttu-id="dc73b-122">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="dc73b-122">Click OK.</span></span>
9. <span data-ttu-id="dc73b-123">V podokně akcí klikněte na možnost Spravovat sklad.</span><span class="sxs-lookup"><span data-stu-id="dc73b-123">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="dc73b-124">Klikněte na Výchozí nastavení objednávky.</span><span class="sxs-lookup"><span data-stu-id="dc73b-124">Click Default order settings.</span></span>
11. <span data-ttu-id="dc73b-125">V poli Výchozí typ objednávky vyberte Výroba.</span><span class="sxs-lookup"><span data-stu-id="dc73b-125">In the Default order type field, select 'Production'.</span></span>
    * <span data-ttu-id="dc73b-126">Protože se jedná o polotovar produktu, který bude vyroben, zvolte Výroba.</span><span class="sxs-lookup"><span data-stu-id="dc73b-126">Because this is a semi-finished product that will be produced, select Production.</span></span>  
12. <span data-ttu-id="dc73b-127">V poli Nákupní pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="dc73b-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="dc73b-128">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="dc73b-128">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="dc73b-129">V poli Skladové pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="dc73b-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="dc73b-130">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="dc73b-130">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="dc73b-131">V poli Prodejní pracoviště zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="dc73b-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="dc73b-132">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="dc73b-132">For this example, select Site 1.</span></span>  
15. <span data-ttu-id="dc73b-133">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="dc73b-133">Close the page.</span></span>
16. <span data-ttu-id="dc73b-134">V podokně akcí klikněte na možnost Spravovat náklady.</span><span class="sxs-lookup"><span data-stu-id="dc73b-134">On the Action Pane, click Manage costs.</span></span>
17. <span data-ttu-id="dc73b-135">Klikněte na možnost Cena položky.</span><span class="sxs-lookup"><span data-stu-id="dc73b-135">Click Item price.</span></span>
18. <span data-ttu-id="dc73b-136">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="dc73b-136">Click New.</span></span>
19. <span data-ttu-id="dc73b-137">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="dc73b-137">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="dc73b-138">V poli Verze zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="dc73b-138">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="dc73b-139">V tomto příkladu vyberte Verze 10.</span><span class="sxs-lookup"><span data-stu-id="dc73b-139">For this example, select Version 10.</span></span>  
21. <span data-ttu-id="dc73b-140">V poli Lokalita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="dc73b-140">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="dc73b-141">V tomto příkladu vyberte Pracoviště 1.</span><span class="sxs-lookup"><span data-stu-id="dc73b-141">For this example, select Site 1.</span></span>  
22. <span data-ttu-id="dc73b-142">Nastavte cenu na 10.</span><span class="sxs-lookup"><span data-stu-id="dc73b-142">Set Price to '10'.</span></span>
    * <span data-ttu-id="dc73b-143">V tomto příkladu zadejte nákladovou cenu 10.</span><span class="sxs-lookup"><span data-stu-id="dc73b-143">For this example, type a cost price of 10.</span></span>  
23. <span data-ttu-id="dc73b-144">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="dc73b-144">Click Save.</span></span>
24. <span data-ttu-id="dc73b-145">Klikněte na Aktivovat nezpracované ceny.</span><span class="sxs-lookup"><span data-stu-id="dc73b-145">Click Activate pending price(s).</span></span>
25. <span data-ttu-id="dc73b-146">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="dc73b-146">Close the page.</span></span>
26. <span data-ttu-id="dc73b-147">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="dc73b-147">Close the page.</span></span>
27. <span data-ttu-id="dc73b-148">Klikněte na BOM_2 a otevřete tuto možnost.</span><span class="sxs-lookup"><span data-stu-id="dc73b-148">Click BOM_2 to open it.</span></span>
28. <span data-ttu-id="dc73b-149">Rozbalte oblast Správa nákladů.</span><span class="sxs-lookup"><span data-stu-id="dc73b-149">Expand the Manage costs section.</span></span>
29. <span data-ttu-id="dc73b-150">V poli Nákladová skupina zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="dc73b-150">In the Cost group field, enter or select a value.</span></span>
    * <span data-ttu-id="dc73b-151">V tomto příkladu vyberte Nákladová skupina M1.</span><span class="sxs-lookup"><span data-stu-id="dc73b-151">For this example, select Cost group M1.</span></span>  
30. <span data-ttu-id="dc73b-152">Použijte zástupce pro uložení záznamu.</span><span class="sxs-lookup"><span data-stu-id="dc73b-152">Use the shortcut for saving a record.</span></span>
31. <span data-ttu-id="dc73b-153">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="dc73b-153">Close the page.</span></span>


