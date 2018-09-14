--- 
title: "Definování pravidel disponibility pro položky"
description: "K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqGroup, DefaultDashboard, EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, ReqItemTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 02aa3b2b7924cdf6317225bfce23f182aa390b8c
ms.contentlocale: cs-cz
ms.lasthandoff: 09/14/2018

---
# <a name="define-coverage-rules-for-items"></a><span data-ttu-id="cc909-103">Definování pravidel disponibility pro položky</span><span class="sxs-lookup"><span data-stu-id="cc909-103">Define coverage rules for items</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cc909-104">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="cc909-104">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="cc909-105">Tento postup popisuje, jak vytvořit pravidla disponibility a přepsat nastavení disponibility pro určitou položku.</span><span class="sxs-lookup"><span data-stu-id="cc909-105">This procedure shows how to create coverage rules and override coverage settings for a specific item.</span></span> <span data-ttu-id="cc909-106">Také ukazuje, jak zadat výchozí nastavení skladu.</span><span class="sxs-lookup"><span data-stu-id="cc909-106">It also shows how to specify default inventory settings.</span></span>


## <a name="create-a-coverage-group"></a><span data-ttu-id="cc909-107">Vytvoření skupiny disponibility</span><span class="sxs-lookup"><span data-stu-id="cc909-107">Create a coverage group</span></span>
1. <span data-ttu-id="cc909-108">Přejděte na Skupiny disponibility.</span><span class="sxs-lookup"><span data-stu-id="cc909-108">Go to Coverage groups.</span></span>
2. <span data-ttu-id="cc909-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="cc909-109">Click New.</span></span>
3. <span data-ttu-id="cc909-110">Zadejte hodnotu do pole Skupina disponibility.</span><span class="sxs-lookup"><span data-stu-id="cc909-110">In the Coverage group field, type a value.</span></span>
4. <span data-ttu-id="cc909-111">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="cc909-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="cc909-112">Zadejte hodnotu do pole Kalendář.</span><span class="sxs-lookup"><span data-stu-id="cc909-112">In the Calendar field, type a value.</span></span>
    * <span data-ttu-id="cc909-113">Vyberte kalendář, že který se používá v hlavním plánování k vytvoření návrhu doplnění pro položky v této skupině.</span><span class="sxs-lookup"><span data-stu-id="cc909-113">Choose the calendar that master planning uses to create replenishment suggestions for items in this group.</span></span>  
6. <span data-ttu-id="cc909-114">Vyberte možnost v poli Kód disponibility.</span><span class="sxs-lookup"><span data-stu-id="cc909-114">In the Coverage code field, select an option.</span></span>
    * <span data-ttu-id="cc909-115">Vyberte požadavek pro tento postup.</span><span class="sxs-lookup"><span data-stu-id="cc909-115">Select Requirement for this procedure.</span></span>  
7. <span data-ttu-id="cc909-116">V poli Ochranná doba disponibility (ve dnech) zadejte číslo 90.</span><span class="sxs-lookup"><span data-stu-id="cc909-116">In the Coverage time fence (days) field, enter '90'.</span></span>
    * <span data-ttu-id="cc909-117">Pro položky v této skupině použijte hlavní plánování k vytvoření návrhu doplnění pro až 90 dnů v budoucnosti.</span><span class="sxs-lookup"><span data-stu-id="cc909-117">For items in this group, master planning will create replenishment suggestions for up to 90 days in the future.</span></span>  
8. <span data-ttu-id="cc909-118">V poli Dny zpoždění zadejte číslo 1.</span><span class="sxs-lookup"><span data-stu-id="cc909-118">In the Negative days field, enter '1'.</span></span>
9. <span data-ttu-id="cc909-119">V poli Kladné dny zadejte číslo 1.</span><span class="sxs-lookup"><span data-stu-id="cc909-119">In the Positive days field, enter '1'.</span></span>
10. <span data-ttu-id="cc909-120">Rozbalte nebo sbalte oddíl Jiné.</span><span class="sxs-lookup"><span data-stu-id="cc909-120">Expand or collapse the Other section.</span></span>
11. <span data-ttu-id="cc909-121">V poli Rezerva příjmu přičtená k požadovanému datu zadejte číslo 1.</span><span class="sxs-lookup"><span data-stu-id="cc909-121">In the Receipt margin added to requirement date field, enter '1'.</span></span>
    * <span data-ttu-id="cc909-122">Pokud je například rezerva příjmu nastavena 1 den a řádek nákupní objednávky je naplánován na příjem dne 15. května, hlavní plánování vypočte upravené datum příjmu 16. května.</span><span class="sxs-lookup"><span data-stu-id="cc909-122">For example, if the receipt margin is set to 1 day, and a purchase order line is scheduled for receipt on May 15, master planning calculates the adjusted receipt date as May 16.</span></span>  
12. <span data-ttu-id="cc909-123">V poli Rezerva výdeje odečtená od požadovaného data zadejte číslo 1.</span><span class="sxs-lookup"><span data-stu-id="cc909-123">In the Issue margin deducted from requirement date field, enter '1'.</span></span>
    * <span data-ttu-id="cc909-124">Pokud je například pojistná doba nastavena na 1 den a řádek prodejní objednávky je naplánován na dodání 15. května, hlavní plánování vypočte upravené datum dodání 14. května.</span><span class="sxs-lookup"><span data-stu-id="cc909-124">For example, if the safety margin is set to 1 day, and a sales order line is scheduled for delivery on May 15, master scheduling calculates the adjusted delivery date as May 14.</span></span>  
13. <span data-ttu-id="cc909-125">V poli Rezerva přidaná k době realizace položky zadejte číslo 1.</span><span class="sxs-lookup"><span data-stu-id="cc909-125">In the Reorder margin added to item lead time field, enter '1'.</span></span>
14. <span data-ttu-id="cc909-126">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="cc909-126">Click Save.</span></span>

## <a name="create-a-new-product"></a><span data-ttu-id="cc909-127">Vytvořit nový produkt</span><span class="sxs-lookup"><span data-stu-id="cc909-127">Create a new product</span></span>
1. <span data-ttu-id="cc909-128">Přejděte na Uvolněné produkty.</span><span class="sxs-lookup"><span data-stu-id="cc909-128">Go to Released products.</span></span>
2. <span data-ttu-id="cc909-129">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="cc909-129">Click New.</span></span>
3. <span data-ttu-id="cc909-130">Zadejte hodnotu do pole Číslo produktu.</span><span class="sxs-lookup"><span data-stu-id="cc909-130">In the Product number field, type a value.</span></span>
4. <span data-ttu-id="cc909-131">Do pole Název produktu zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="cc909-131">In the Product name field, type a value.</span></span>
5. <span data-ttu-id="cc909-132">V poli Skupina modelů položek kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="cc909-132">In the Item model group field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="cc909-133">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="cc909-133">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="cc909-134">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="cc909-134">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="cc909-135">V poli Skupina položek kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="cc909-135">In the Item group field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="cc909-136">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="cc909-136">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="cc909-137">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="cc909-137">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="cc909-138">V poli Skupina dimenze úložiště kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="cc909-138">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="cc909-139">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="cc909-139">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="cc909-140">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="cc909-140">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="cc909-141">V poli Skupina sledovací dimenze kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="cc909-141">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="cc909-142">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="cc909-142">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="cc909-143">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="cc909-143">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="cc909-144">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="cc909-144">Click OK.</span></span>

## <a name="setup-default-order-settings"></a><span data-ttu-id="cc909-145">Nastavení výchozího nastavení objednávky</span><span class="sxs-lookup"><span data-stu-id="cc909-145">Setup default order settings</span></span>
1. <span data-ttu-id="cc909-146">V podokně akcí klikněte na položku Plán.</span><span class="sxs-lookup"><span data-stu-id="cc909-146">On the Action Pane, click Plan.</span></span>
2. <span data-ttu-id="cc909-147">Klikněte na Výchozí nastavení objednávky.</span><span class="sxs-lookup"><span data-stu-id="cc909-147">Click Default order settings.</span></span>
3. <span data-ttu-id="cc909-148">Do pole Nákupní pracoviště zadejte pracoviště, které chcete použít jako výchozí při vytvoření nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="cc909-148">In the Purchase site field, type the site used as default when purchase orders are created.</span></span>
4. <span data-ttu-id="cc909-149">Do pole Skladové pracoviště zadejte site, kde je položka uložena.</span><span class="sxs-lookup"><span data-stu-id="cc909-149">In the Inventory site field, type the site where the item is stored.</span></span>
5. <span data-ttu-id="cc909-150">Rozbalte nebo sbalte oddíl Zásoby.</span><span class="sxs-lookup"><span data-stu-id="cc909-150">Expand or collapse the Inventory section.</span></span>
6. <span data-ttu-id="cc909-151">Nastavte Násobek na hodnotu 10.</span><span class="sxs-lookup"><span data-stu-id="cc909-151">Set Multiple to '10'.</span></span>
7. <span data-ttu-id="cc909-152">Nastavte Min.</span><span class="sxs-lookup"><span data-stu-id="cc909-152">Set Min.</span></span> <span data-ttu-id="cc909-153">množství objednávky na 10.</span><span class="sxs-lookup"><span data-stu-id="cc909-153">order quantity to '10'.</span></span>
8. <span data-ttu-id="cc909-154">Nastavte maximální.</span><span class="sxs-lookup"><span data-stu-id="cc909-154">Set Max.</span></span> <span data-ttu-id="cc909-155">množství objednávky na 100.</span><span class="sxs-lookup"><span data-stu-id="cc909-155">order quantity to '100'.</span></span>
9. <span data-ttu-id="cc909-156">Nastavte Standardní množství objednávky na 10.</span><span class="sxs-lookup"><span data-stu-id="cc909-156">Set Standard order quantity to '10'.</span></span>
10. <span data-ttu-id="cc909-157">Do pole Doba realizace nákupu zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="cc909-157">In the Purchase lead time field, enter a number.</span></span>
11. <span data-ttu-id="cc909-158">Zaškrtněte políčko Pracovní dny nebo jeho zaškrtnutí zrušte.</span><span class="sxs-lookup"><span data-stu-id="cc909-158">Select or clear the Working days check box.</span></span>
12. <span data-ttu-id="cc909-159">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="cc909-159">Click Save.</span></span>
13. <span data-ttu-id="cc909-160">V poli Výchozí typ objednávky vyberte možnost Nákupní objednávka.</span><span class="sxs-lookup"><span data-stu-id="cc909-160">In the Default order type field select 'Purchase order'.</span></span>
14. <span data-ttu-id="cc909-161">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="cc909-161">Click Save.</span></span>
15. <span data-ttu-id="cc909-162">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="cc909-162">Close the page.</span></span>
    * <span data-ttu-id="cc909-163">Zavřete stránku Výchozí nastavení objednávky.</span><span class="sxs-lookup"><span data-stu-id="cc909-163">Close the Default order settings page.</span></span>  

## <a name="add-an-item-to-a-coverage-group"></a><span data-ttu-id="cc909-164">Přidání položky do skupiny disponibility</span><span class="sxs-lookup"><span data-stu-id="cc909-164">Add an item to a coverage group</span></span>
1. <span data-ttu-id="cc909-165">Rozbalte nebo sbalte oddíl Plán.</span><span class="sxs-lookup"><span data-stu-id="cc909-165">Expand or collapse the Plan section.</span></span>
2. <span data-ttu-id="cc909-166">V poli Skupina disponibility kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="cc909-166">In the Coverage group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="cc909-167">V seznamu vyhledejte skupiny disponibility, kterou jste vytvořili.</span><span class="sxs-lookup"><span data-stu-id="cc909-167">In the list, find the Coverage group you have created.</span></span>
4. <span data-ttu-id="cc909-168">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="cc909-168">In the list, click the link in the selected row.</span></span>

## <a name="create-item-coverage-rules"></a><span data-ttu-id="cc909-169">Vytvoření pravidel disponibility položky</span><span class="sxs-lookup"><span data-stu-id="cc909-169">Create item coverage rules</span></span>
1. <span data-ttu-id="cc909-170">V podokně akcí klikněte na položku Plán.</span><span class="sxs-lookup"><span data-stu-id="cc909-170">On the Action Pane, click Plan.</span></span>
2. <span data-ttu-id="cc909-171">Klikněte na Disponibilita položky.</span><span class="sxs-lookup"><span data-stu-id="cc909-171">Click Item coverage.</span></span>
3. <span data-ttu-id="cc909-172">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="cc909-172">Click New.</span></span>
4. <span data-ttu-id="cc909-173">Klikněte na záložku Obecné.</span><span class="sxs-lookup"><span data-stu-id="cc909-173">Click the General tab.</span></span>
5. <span data-ttu-id="cc909-174">Zaškrtněte políčko v záhlaví Přepsat nastavení skupiny disponibility.</span><span class="sxs-lookup"><span data-stu-id="cc909-174">Check the box on the header of Override coverage group settings.</span></span>
6. <span data-ttu-id="cc909-175">V poli Ochranná doba disponibility (ve dnech) zadejte číslo 60.</span><span class="sxs-lookup"><span data-stu-id="cc909-175">In the Coverage time fence (days) field, enter '60'.</span></span>
    * <span data-ttu-id="cc909-176">I když jsou položky ve skupině disponibility Požadavky plánované 90 dnů dopředu, tato položka bude plánovaná 60 dní dopředu.</span><span class="sxs-lookup"><span data-stu-id="cc909-176">Although items in coverage group Requiremen are planned 90 days ahead, this item will be planned 60 days ahead.</span></span>  
7. <span data-ttu-id="cc909-177">V poli Dny zpoždění zadejte číslo 2.</span><span class="sxs-lookup"><span data-stu-id="cc909-177">In the Negative days field, enter '2'.</span></span>
8. <span data-ttu-id="cc909-178">V poli Kladné dny zadejte číslo 2.</span><span class="sxs-lookup"><span data-stu-id="cc909-178">In the Positive days field, enter '2'.</span></span>
9. <span data-ttu-id="cc909-179">Klikněte na kartu Doba realizace.</span><span class="sxs-lookup"><span data-stu-id="cc909-179">Click the Lead time tab.</span></span>
10. <span data-ttu-id="cc909-180">Zaškrtněte políčko v záhlaví Nákup.</span><span class="sxs-lookup"><span data-stu-id="cc909-180">Check the box on the header of Purchase.</span></span>
11. <span data-ttu-id="cc909-181">Do pole Čas nákupu zadejte hodnotu 5.</span><span class="sxs-lookup"><span data-stu-id="cc909-181">In the Purchase time field, enter '5'.</span></span>
12. <span data-ttu-id="cc909-182">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="cc909-182">Click Save.</span></span>


