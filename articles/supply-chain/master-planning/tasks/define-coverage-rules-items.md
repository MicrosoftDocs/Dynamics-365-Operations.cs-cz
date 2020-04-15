---
title: Definování pravidel disponibility pro položky
description: K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.
author: ShylaThompson
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5ecd56c84b232fd7855bf2fb01eaebe3f3bd4440
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150279"
---
# <a name="define-coverage-rules-for-items"></a><span data-ttu-id="25456-103">Definování pravidel disponibility pro položky</span><span class="sxs-lookup"><span data-stu-id="25456-103">Define coverage rules for items</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="25456-104">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="25456-104">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="25456-105">Tento postup popisuje, jak vytvořit pravidla disponibility a přepsat nastavení disponibility pro určitou položku.</span><span class="sxs-lookup"><span data-stu-id="25456-105">This procedure shows how to create coverage rules and override coverage settings for a specific item.</span></span> <span data-ttu-id="25456-106">Také ukazuje, jak zadat výchozí nastavení skladu.</span><span class="sxs-lookup"><span data-stu-id="25456-106">It also shows how to specify default inventory settings.</span></span>


## <a name="create-a-coverage-group"></a><span data-ttu-id="25456-107">Vytvoření skupiny disponibility</span><span class="sxs-lookup"><span data-stu-id="25456-107">Create a coverage group</span></span>
1. <span data-ttu-id="25456-108">Přejděte na **Navigační podokno > Moduly > Hlavní plánování > Nastavení > Skupiny disponibility**.</span><span class="sxs-lookup"><span data-stu-id="25456-108">Go to **Navigation pane > Modules > Master planning > Setup > Coverage groups**.</span></span>
2. <span data-ttu-id="25456-109">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="25456-109">Click **New**.</span></span>
3. <span data-ttu-id="25456-110">Zadejte hodnotu do pole **Skupina disponibility**.</span><span class="sxs-lookup"><span data-stu-id="25456-110">In the **Coverage group** field, type a value.</span></span>
4. <span data-ttu-id="25456-111">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="25456-111">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="25456-112">Zadejte hodnotu do pole **Kalendář**.</span><span class="sxs-lookup"><span data-stu-id="25456-112">In the **Calendar** field, type a value.</span></span> <span data-ttu-id="25456-113">Vyberte kalendář, že který se používá v hlavním plánování k vytvoření návrhu doplnění pro položky v této skupině.</span><span class="sxs-lookup"><span data-stu-id="25456-113">Choose the calendar that master planning uses to create replenishment suggestions for items in this group.</span></span>  
6. <span data-ttu-id="25456-114">Vyberte možnost v poli **Kód disponibility**.</span><span class="sxs-lookup"><span data-stu-id="25456-114">In the **Coverage code** field, select an option.</span></span> <span data-ttu-id="25456-115">Vyberte požadavek pro tento postup.</span><span class="sxs-lookup"><span data-stu-id="25456-115">Select 'Requirement' for this procedure.</span></span>  
7. <span data-ttu-id="25456-116">V poli **Ochranná doba disponibility (ve dnech)** zadejte číslo 90.</span><span class="sxs-lookup"><span data-stu-id="25456-116">In the **Coverage time fence (days) field**, enter '90'.</span></span> <span data-ttu-id="25456-117">Pro položky v této skupině použijte hlavní plánování k vytvoření návrhu doplnění pro až 90 dnů v budoucnosti.</span><span class="sxs-lookup"><span data-stu-id="25456-117">For items in this group, master planning will create replenishment suggestions for up to 90 days in the future.</span></span>  
8. <span data-ttu-id="25456-118">V poli **Dny zpoždění** zadejte číslo 1.</span><span class="sxs-lookup"><span data-stu-id="25456-118">In the **Negative days** field, enter '1'.</span></span>
9. <span data-ttu-id="25456-119">V poli **Kladné dny** zadejte číslo 1.</span><span class="sxs-lookup"><span data-stu-id="25456-119">In the **Positive days** field, enter '1'.</span></span>
10. <span data-ttu-id="25456-120">Rozbalte nebo sbalte oddíl **Jiné**.</span><span class="sxs-lookup"><span data-stu-id="25456-120">Expand or collapse the **Other** section.</span></span>
11. <span data-ttu-id="25456-121">Pod částí **Pojistné doby ve dnech** v poli **Rezerva příjmu přičtená k požadovanému datu** zadejte 1.</span><span class="sxs-lookup"><span data-stu-id="25456-121">Under the **Safety margins in days** section, in the **Receipt margin added to requirement date** field, enter '1'.</span></span> <span data-ttu-id="25456-122">Pokud je například rezerva příjmu nastavena 1 den a řádek nákupní objednávky je naplánován na příjem dne 15. května, hlavní plánování vypočte upravené datum příjmu 16. května.</span><span class="sxs-lookup"><span data-stu-id="25456-122">For example, if the receipt margin is set to 1 day, and a purchase order line is scheduled for receipt on May 15, master planning calculates the adjusted receipt date as May 16.</span></span>  
12. <span data-ttu-id="25456-123">V poli **Rezerva výdeje odečtená od požadovaného data** zadejte číslo 1.</span><span class="sxs-lookup"><span data-stu-id="25456-123">In the **Issue margin deducted from requirement date** field, enter '1'.</span></span> <span data-ttu-id="25456-124">Pokud je například pojistná doba nastavena na 1 den a řádek prodejní objednávky je naplánován na dodání 15. května, hlavní plánování vypočte upravené datum dodání 14. května.</span><span class="sxs-lookup"><span data-stu-id="25456-124">For example, if the safety margin is set to 1 day, and a sales order line is scheduled for delivery on May 15, master scheduling calculates the adjusted delivery date as May 14.</span></span>  
13. <span data-ttu-id="25456-125">V poli **Rezerva přidaná k době realizace položky** zadejte číslo 1.</span><span class="sxs-lookup"><span data-stu-id="25456-125">In the **Reorder margin added to item lead time** field, enter '1'.</span></span>
14. <span data-ttu-id="25456-126">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="25456-126">Click **Save**.</span></span>

## <a name="create-a-new-product"></a><span data-ttu-id="25456-127">Vytvoření nového produktu</span><span class="sxs-lookup"><span data-stu-id="25456-127">Create a new product</span></span>
1. <span data-ttu-id="25456-128">Klikněte na **Navigační podokno > Moduly > Řízení informací o produktech > Produkty > Vydané produkty**.</span><span class="sxs-lookup"><span data-stu-id="25456-128">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="25456-129">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="25456-129">Click **New**.</span></span>
3. <span data-ttu-id="25456-130">Zadejte hodnotu do pole **Číslo produktu**.</span><span class="sxs-lookup"><span data-stu-id="25456-130">In the **Product number** field, type a value.</span></span>
4. <span data-ttu-id="25456-131">Do pole **Název produktu** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="25456-131">In the **Product name** field, type a value.</span></span>
5. <span data-ttu-id="25456-132">V poli **Skupina modelů položek** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="25456-132">In the **Item model group** field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="25456-133">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="25456-133">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="25456-134">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="25456-134">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="25456-135">V poli **Skupina položek** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="25456-135">In the **Item group** field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="25456-136">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="25456-136">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="25456-137">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="25456-137">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="25456-138">V poli **Skupina dimenze úložiště** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="25456-138">In the **Storage dimension group** field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="25456-139">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="25456-139">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="25456-140">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="25456-140">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="25456-141">V poli **Skupina sledovací dimenze** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="25456-141">In the **Tracking dimension group** field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="25456-142">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="25456-142">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="25456-143">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="25456-143">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="25456-144">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="25456-144">Click **OK**.</span></span>

## <a name="setup-default-order-settings"></a><span data-ttu-id="25456-145">Nastavení výchozího nastavení objednávky</span><span class="sxs-lookup"><span data-stu-id="25456-145">Setup default order settings</span></span>
1. <span data-ttu-id="25456-146">V **podokně akcí** klikněte na možnost **Plán**.</span><span class="sxs-lookup"><span data-stu-id="25456-146">On the **Action Pane**, click **Plan**.</span></span>
2. <span data-ttu-id="25456-147">V části **Nastavení objednávky** klikněte na **Výchozí nastavení objednávky**.</span><span class="sxs-lookup"><span data-stu-id="25456-147">Under **Order settings**, click **Default order settings**.</span></span>
3. <span data-ttu-id="25456-148">Do pole **Výchozí pracoviště** v možnosti **Nákupní objednávka** zadejte pracoviště, které chcete použít jako výchozí při vytvoření nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="25456-148">Under **Purchase order**, in the **Default site** field, type the site used as default when purchase orders are created.</span></span>
4. <span data-ttu-id="25456-149">Do pole **Výchozí sklad** zadejte pracoviště, kde je položka uložena.</span><span class="sxs-lookup"><span data-stu-id="25456-149">In the **Default warehouse** field, type the site where the item is stored.</span></span>
5. <span data-ttu-id="25456-150">Rozbalte nebo sbalte oddíl **Zásoby**.</span><span class="sxs-lookup"><span data-stu-id="25456-150">Expand or collapse the **Inventory** section.</span></span>
6. <span data-ttu-id="25456-151">Do pole **Násobek** zadejte 10.</span><span class="sxs-lookup"><span data-stu-id="25456-151">In the **Multiple** field, type '10'.</span></span>
7. <span data-ttu-id="25456-152">Do pole **Min. množství objednávky** zadejte 10.</span><span class="sxs-lookup"><span data-stu-id="25456-152">In the **Min. order quantity** field, type '10'.</span></span>
8. <span data-ttu-id="25456-153">Do pole **Max. množství objednávky** zadejte 100.</span><span class="sxs-lookup"><span data-stu-id="25456-153">In the **Max. order quantity** field, type '100'.</span></span>
9. <span data-ttu-id="25456-154">Do pole **Standardní množství objednávky** zadejte 10.</span><span class="sxs-lookup"><span data-stu-id="25456-154">In the **Standard order quantity**, type '10'.</span></span>
10. <span data-ttu-id="25456-155">Do pole **Doba realizace nákupu** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="25456-155">In the **Purchase lead time** field, enter a number.</span></span>
11. <span data-ttu-id="25456-156">Zaškrtněte políčko **Pracovní dny** nebo jeho zaškrtnutí zrušte.</span><span class="sxs-lookup"><span data-stu-id="25456-156">Select or clear the **Working days** check box.</span></span>
12. <span data-ttu-id="25456-157">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="25456-157">Click **Save**.</span></span>
13. <span data-ttu-id="25456-158">V poli **Výchozí typ objednávky** vyberte možnost Nákupní objednávka.</span><span class="sxs-lookup"><span data-stu-id="25456-158">In the **Default order type** field select 'Purchase order'.</span></span>
14. <span data-ttu-id="25456-159">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="25456-159">Click **Save**.</span></span>
15. <span data-ttu-id="25456-160">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="25456-160">Close the page.</span></span> <span data-ttu-id="25456-161">Zavřete stránku Výchozí nastavení objednávky.</span><span class="sxs-lookup"><span data-stu-id="25456-161">Close the Default order settings page.</span></span>  

## <a name="add-an-item-to-a-coverage-group"></a><span data-ttu-id="25456-162">Přidání položky do skupiny disponibility</span><span class="sxs-lookup"><span data-stu-id="25456-162">Add an item to a coverage group</span></span>
1. <span data-ttu-id="25456-163">Rozbalte nebo sbalte oddíl **Plán**.</span><span class="sxs-lookup"><span data-stu-id="25456-163">Expand or collapse the **Plan** section.</span></span>
2. <span data-ttu-id="25456-164">V poli **Skupina disponibility** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="25456-164">In the **Coverage group** field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="25456-165">V seznamu vyhledejte **skupiny disponibility**, kterou jste vytvořili.</span><span class="sxs-lookup"><span data-stu-id="25456-165">In the list, find the **Coverage group** you have created.</span></span>
4. <span data-ttu-id="25456-166">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="25456-166">In the list, click the link in the selected row.</span></span>

## <a name="create-item-coverage-rules"></a><span data-ttu-id="25456-167">Vytvoření pravidel disponibility položky</span><span class="sxs-lookup"><span data-stu-id="25456-167">Create item coverage rules</span></span>
1. <span data-ttu-id="25456-168">V **podokně akcí** klikněte na možnost **Plán**.</span><span class="sxs-lookup"><span data-stu-id="25456-168">On the **Action Pane**, click **Plan**.</span></span>
2. <span data-ttu-id="25456-169">V části **Disponibilita** klikněte na **Disponibilita položky**.</span><span class="sxs-lookup"><span data-stu-id="25456-169">Under **Coverage**, click **Item coverage**.</span></span>
3. <span data-ttu-id="25456-170">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="25456-170">Click **New**.</span></span>
4. <span data-ttu-id="25456-171">Klepněte na kartu **Obecné**.</span><span class="sxs-lookup"><span data-stu-id="25456-171">Click the **General** tab.</span></span>
5. <span data-ttu-id="25456-172">Zaškrtněte políčko v záhlaví nastavení **Přepsat skupinu disponibility**.</span><span class="sxs-lookup"><span data-stu-id="25456-172">Check the box on the header of **Override coverage group** settings.</span></span>
6. <span data-ttu-id="25456-173">V poli **Ochranná doba disponibility (ve dnech)** zadejte číslo 60.</span><span class="sxs-lookup"><span data-stu-id="25456-173">In the **Coverage time fence (days)** field, enter '60'.</span></span> <span data-ttu-id="25456-174">I když jsou položky ve skupině disponibility Požadavky plánované 90 dnů dopředu, tato položka bude plánovaná 60 dní dopředu.</span><span class="sxs-lookup"><span data-stu-id="25456-174">Although items in coverage group Requiremen are planned 90 days ahead, this item will be planned 60 days ahead.</span></span>  
7. <span data-ttu-id="25456-175">V poli **Dny zpoždění** zadejte číslo 2.</span><span class="sxs-lookup"><span data-stu-id="25456-175">In the **Negative days** field, enter '2'.</span></span>
8. <span data-ttu-id="25456-176">V poli **Kladné dny** zadejte číslo 2.</span><span class="sxs-lookup"><span data-stu-id="25456-176">In the **Positive days** field, enter '2'.</span></span>
9. <span data-ttu-id="25456-177">Klikněte na kartu **Doba realizace**.</span><span class="sxs-lookup"><span data-stu-id="25456-177">Click the **Lead time** tab.</span></span>
10. <span data-ttu-id="25456-178">Zaškrtněte políčko v záhlaví **Nákup**.</span><span class="sxs-lookup"><span data-stu-id="25456-178">Check the box on the header of **Purchase**.</span></span>
11. <span data-ttu-id="25456-179">Do pole **Čas nákupu** zadejte hodnotu 5.</span><span class="sxs-lookup"><span data-stu-id="25456-179">In the **Purchase time** field, enter '5'.</span></span>
12. <span data-ttu-id="25456-180">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="25456-180">Click **Save**.</span></span>

