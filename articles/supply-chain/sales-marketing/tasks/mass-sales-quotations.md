---
title: Hromadně vytvořit prodejní nabídky
description: Tento postup ukazuje, jak účinně vytvářet prodejní nabídky nabízející sadu produktů nebo služeb, které mají být zaslány více zákazníkům.
author: omulvad
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesQuotationTemplateGroup, SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SysQueryForm, SalesQuickQuote
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0ea50500ed52069ab9f6aae0dfb2d6cffc47cbff
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006833"
---
# <a name="mass-create-sales-quotations"></a><span data-ttu-id="65801-103">Hromadně vytvořit prodejní nabídky</span><span class="sxs-lookup"><span data-stu-id="65801-103">Mass create sales quotations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="65801-104">Tento postup ukazuje, jak účinně vytvářet prodejní nabídky nabízející sadu produktů nebo služeb, které mají být zaslány více zákazníkům.</span><span class="sxs-lookup"><span data-stu-id="65801-104">This procedure demonstrates how to efficiently create quotations offering a set of products or services that are to be sent to multiple customers.</span></span> <span data-ttu-id="65801-105">Toto hromadné vytvoření nabídky vychází z šablon nabídek.</span><span class="sxs-lookup"><span data-stu-id="65801-105">This mass quotation creation is based on quotation templates.</span></span> <span data-ttu-id="65801-106">Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="65801-106">You can run this procedure on your own data or in demo data company USMF.</span></span>


## <a name="create-a-quotation-template"></a><span data-ttu-id="65801-107">Vytvoření šablony nabídek</span><span class="sxs-lookup"><span data-stu-id="65801-107">Create a quotation template</span></span>
1. <span data-ttu-id="65801-108">Přejděte na Prodej a marketing > Nastavení > Nabídky > Skupiny šablon.</span><span class="sxs-lookup"><span data-stu-id="65801-108">Go to Sales and marketing > Setup > Quotations > Template groups.</span></span>
2. <span data-ttu-id="65801-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="65801-109">Click New.</span></span>
3. <span data-ttu-id="65801-110">V poli ID skupiny zadejte ID podle vašeho výběru.</span><span class="sxs-lookup"><span data-stu-id="65801-110">In the Group ID field, type an ID of your choice.</span></span>
4. <span data-ttu-id="65801-111">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="65801-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="65801-112">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="65801-112">Click Save.</span></span>
6. <span data-ttu-id="65801-113">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="65801-113">Close the page.</span></span>
7. <span data-ttu-id="65801-114">Přejděte na Prodej a marketing > Prodejní nabídky > Všechny nabídky.</span><span class="sxs-lookup"><span data-stu-id="65801-114">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
8. <span data-ttu-id="65801-115">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="65801-115">Click New.</span></span>
9. <span data-ttu-id="65801-116">V poli Typ účtu vyberte možnost Odběratel.</span><span class="sxs-lookup"><span data-stu-id="65801-116">In the Account type field, select 'Customer'.</span></span>
10. <span data-ttu-id="65801-117">V poli Účet odběratele zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="65801-117">In the Customer account field, enter or select a value.</span></span>
11. <span data-ttu-id="65801-118">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="65801-118">Click OK.</span></span>
    * <span data-ttu-id="65801-119">Chcete-li z nabídky vytvořit šablonu, je třeba provést nastavení v záhlaví nabídky.</span><span class="sxs-lookup"><span data-stu-id="65801-119">For a quotation to become a template you must carry out  setup steps on the quotation header.</span></span> <span data-ttu-id="65801-120">Musíte tak učinit dříve, než do nabídky přidáte řádky.</span><span class="sxs-lookup"><span data-stu-id="65801-120">This must be done before you add lines to the quotation.</span></span>   
12. <span data-ttu-id="65801-121">V podokně akcí klikněte na Možnosti.</span><span class="sxs-lookup"><span data-stu-id="65801-121">On the Action Pane, click Options.</span></span>
13. <span data-ttu-id="65801-122">Klikněte na tlačítko Změnit zobrazení.</span><span class="sxs-lookup"><span data-stu-id="65801-122">Click Change view.</span></span>
14. <span data-ttu-id="65801-123">Klikněte na možnost Zobrazení záhlaví.</span><span class="sxs-lookup"><span data-stu-id="65801-123">Click Header view.</span></span>
15. <span data-ttu-id="65801-124">Rozbalte sekci Nastavení.</span><span class="sxs-lookup"><span data-stu-id="65801-124">Expand the Setup section.</span></span>
16. <span data-ttu-id="65801-125">V poli ID skupiny zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="65801-125">In the Group ID field, enter or select a value.</span></span>
17. <span data-ttu-id="65801-126">Zadejte hodnotu do pole Název šablony.</span><span class="sxs-lookup"><span data-stu-id="65801-126">In the Template name field, type a value.</span></span>
18. <span data-ttu-id="65801-127">Vyberte Ano v poli Aktivní.</span><span class="sxs-lookup"><span data-stu-id="65801-127">Select Yes in the Active field.</span></span>
    * <span data-ttu-id="65801-128">Pouze aktivní šablony lze použít při použití šablony na novou prodejní nabídku.</span><span class="sxs-lookup"><span data-stu-id="65801-128">Only active templates can be used when you apply a template to a new sales quotation.</span></span>  
19. <span data-ttu-id="65801-129">V podokně akcí klikněte na Možnosti.</span><span class="sxs-lookup"><span data-stu-id="65801-129">On the Action Pane, click Options.</span></span>
20. <span data-ttu-id="65801-130">Klikněte na tlačítko Změnit zobrazení.</span><span class="sxs-lookup"><span data-stu-id="65801-130">Click Change view.</span></span>
21. <span data-ttu-id="65801-131">Klepněte na možnost Řádkové zobrazení.</span><span class="sxs-lookup"><span data-stu-id="65801-131">Click Line view.</span></span>
22. <span data-ttu-id="65801-132">V poli Zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="65801-132">In the Item field, enter or select a value.</span></span>
23. <span data-ttu-id="65801-133">Zadejte hodnotu do pole Zboží.</span><span class="sxs-lookup"><span data-stu-id="65801-133">In the Item field, type a value.</span></span>
24. <span data-ttu-id="65801-134">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="65801-134">Close the page.</span></span>
25. <span data-ttu-id="65801-135">V poli Procento slevy zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="65801-135">In the Discount percent field, enter a number.</span></span>
26. <span data-ttu-id="65801-136">Klikněte na Přidat řádek.</span><span class="sxs-lookup"><span data-stu-id="65801-136">Click Add line.</span></span>
27. <span data-ttu-id="65801-137">V poli Zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="65801-137">In the Item field, enter or select a value.</span></span>
28. <span data-ttu-id="65801-138">Zadejte hodnotu do pole Zboží.</span><span class="sxs-lookup"><span data-stu-id="65801-138">In the Item field, type a value.</span></span>
29. <span data-ttu-id="65801-139">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="65801-139">Close the page.</span></span>
30. <span data-ttu-id="65801-140">V poli Jednotková cena zadejte novou cenu nebo změňte stávající.</span><span class="sxs-lookup"><span data-stu-id="65801-140">In the Unit price field, enter a new price or change the current one.</span></span>
31. <span data-ttu-id="65801-141">Klikněte na Přidat řádek.</span><span class="sxs-lookup"><span data-stu-id="65801-141">Click Add line.</span></span>
32. <span data-ttu-id="65801-142">V poli Zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="65801-142">In the Item field, enter or select a value.</span></span>
33. <span data-ttu-id="65801-143">Zadejte hodnotu do pole Zboží.</span><span class="sxs-lookup"><span data-stu-id="65801-143">In the Item field, type a value.</span></span>
34. <span data-ttu-id="65801-144">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="65801-144">Close the page.</span></span>
35. <span data-ttu-id="65801-145">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="65801-145">In the Quantity field, enter a number.</span></span>
36. <span data-ttu-id="65801-146">V poli Sleva zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="65801-146">In the Discount field, enter a number.</span></span>
37. <span data-ttu-id="65801-147">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="65801-147">Click Save.</span></span>

## <a name="apply-the-template-to-create-a-single-quotation"></a><span data-ttu-id="65801-148">Použití šablony pro vytvoření jednotlivých nabídek</span><span class="sxs-lookup"><span data-stu-id="65801-148">Apply the template to create a single quotation</span></span>
1. <span data-ttu-id="65801-149">Přejděte na Prodej a marketing > Prodejní nabídky > Všechny nabídky.</span><span class="sxs-lookup"><span data-stu-id="65801-149">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="65801-150">Všimněte si, že nabídka, kterou jste právě vytvořili, je označena jako šablona.</span><span class="sxs-lookup"><span data-stu-id="65801-150">Note that the quotation you have just created is marked as template.</span></span>  
2. <span data-ttu-id="65801-151">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="65801-151">Click New.</span></span>
3. <span data-ttu-id="65801-152">V poli Typ účtu vyberte možnost Odběratel.</span><span class="sxs-lookup"><span data-stu-id="65801-152">In the Account type field, select 'Customer'.</span></span>
4. <span data-ttu-id="65801-153">V poli Účet odběratele zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="65801-153">In the Customer account field, enter or select a value.</span></span>
5. <span data-ttu-id="65801-154">Rozbalte sekci Šablona.</span><span class="sxs-lookup"><span data-stu-id="65801-154">Expand the Template section.</span></span>
6. <span data-ttu-id="65801-155">V poli ID skupiny zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="65801-155">In the Group ID field, enter or select a value.</span></span>
7. <span data-ttu-id="65801-156">V poli Název šablony nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="65801-156">In the Template name field, enter or select a value.</span></span>
8. <span data-ttu-id="65801-157">V poli Metoda výpočtu vyberte „Podle hodnot šablony“.</span><span class="sxs-lookup"><span data-stu-id="65801-157">In the Calculation method field, select 'Based on template values'.</span></span>
9. <span data-ttu-id="65801-158">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="65801-158">Click OK.</span></span>
    * <span data-ttu-id="65801-159">Nová nabídka byla nyní vytvořena, na základě dat a podmínek šablony.</span><span class="sxs-lookup"><span data-stu-id="65801-159">The new quotation has now been created, based on the data and terms of the template.</span></span>  
10. <span data-ttu-id="65801-160">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="65801-160">Close the page.</span></span>
11. <span data-ttu-id="65801-161">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="65801-161">Close the page.</span></span>

## <a name="apply-the-template-to-mass-create-quotations"></a><span data-ttu-id="65801-162">Použití šablony pro hromadné vytvoření nabídek</span><span class="sxs-lookup"><span data-stu-id="65801-162">Apply the template to mass create quotations</span></span>
1. <span data-ttu-id="65801-163">Přejděte na Prodej a marketing > Prodejní nabídky > Aktualizace nabídky > Hromadné vytvoření nabídek.</span><span class="sxs-lookup"><span data-stu-id="65801-163">Go to Sales and marketing > Sales quotations > Quotation update > Mass create quotations.</span></span>
2. <span data-ttu-id="65801-164">V poli Typ účtu vyberte možnost Odběratel.</span><span class="sxs-lookup"><span data-stu-id="65801-164">In the Account type field, select 'Customer'.</span></span>
3. <span data-ttu-id="65801-165">V poli ID skupiny zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="65801-165">In the Group ID field, enter or select a value.</span></span>
4. <span data-ttu-id="65801-166">V poli Název šablony nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="65801-166">In the Template name field, enter or select a value.</span></span>
5. <span data-ttu-id="65801-167">V poli Metoda výpočtu vyberte „Podle hodnot šablony“.</span><span class="sxs-lookup"><span data-stu-id="65801-167">In the Calculation method field, select 'Based on template values'.</span></span>
6. <span data-ttu-id="65801-168">Rozbalte oddíl Záznamy k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="65801-168">Expand the Records to include section.</span></span>
7. <span data-ttu-id="65801-169">Klepněte na tlačítko Filtr.</span><span class="sxs-lookup"><span data-stu-id="65801-169">Click Filter.</span></span>
8. <span data-ttu-id="65801-170">Do pole Kritéria nastavte filtr pro pokrytí rozsahu odběratelů, které chcete zahrnout do tohoto vytvoření hromadné nabídky.</span><span class="sxs-lookup"><span data-stu-id="65801-170">In the Criteria field, set the filter to cover a range of customers you want to include in this mass quotation creation.</span></span> <span data-ttu-id="65801-171">Použijte následující formát „Zákazník1…zákazníkN“.</span><span class="sxs-lookup"><span data-stu-id="65801-171">Use the following format "Customer1..CustomerN.</span></span>
    * <span data-ttu-id="65801-172">Můžete například nastavit filtr na: US-001…US-004</span><span class="sxs-lookup"><span data-stu-id="65801-172">For example, you could set the filter to: US-001..US-004</span></span>  
9. <span data-ttu-id="65801-173">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="65801-173">Click OK.</span></span>
10. <span data-ttu-id="65801-174">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="65801-174">Click OK.</span></span>
11. <span data-ttu-id="65801-175">Přejděte na Prodej a marketing > Prodejní nabídky > Všechny nabídky.</span><span class="sxs-lookup"><span data-stu-id="65801-175">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
    * <span data-ttu-id="65801-176">Ověřte, zda nabídky byly vytvořeny pro všechny odběratele určené v rutinní hromadné aktualizaci, jak bylo nastaveno ve vybrané šabloně.</span><span class="sxs-lookup"><span data-stu-id="65801-176">Verify that quotations have been created for all the customers specified in the mass update routine, as based on the selected template.</span></span>  

