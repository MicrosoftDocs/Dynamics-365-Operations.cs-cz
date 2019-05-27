---
title: Nastavení vytváření kontejnerů
description: Tento postup popisuje postup automatizace vytváření kontejnerů vytížení v modulu Řízení skladu.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 56fc6adc2a0eeb5b824089ff4b1b781f3a99a34c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558049"
---
# <a name="set-up-containerization"></a><span data-ttu-id="4bec7-103">Nastavení vytváření kontejnerů</span><span class="sxs-lookup"><span data-stu-id="4bec7-103">Set up containerization</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4bec7-104">Tento postup popisuje postup automatizace vytváření kontejnerů vytížení v modulu Řízení skladu.</span><span class="sxs-lookup"><span data-stu-id="4bec7-104">This procedure describes how to automate the containerization of loads in Warehouse management.</span></span> <span data-ttu-id="4bec7-105">Automatické vytváření kontejnerů vytvoří kontejnery a výdejovou práci pro dodávky při zpracování vlny, a řádky práce lze rozdělit na množství, které se vejde do kontejnerů.</span><span class="sxs-lookup"><span data-stu-id="4bec7-105">Automated containerization creates containers and the picking work for shipments when a wave is processed and work lines can be split into quantities that fit the containers.</span></span> <span data-ttu-id="4bec7-106">To pomáhá pracovníkům skladu vyzvednout položky přímo do zvoleného kontejneru.</span><span class="sxs-lookup"><span data-stu-id="4bec7-106">This helps warehouse workers to pick the items directly into the chosen container.</span></span> <span data-ttu-id="4bec7-107">Ve srovnání s procesem ručního balení jsou úlohy, jako je vytváření kontejnerů, přiřazování položek nebo uzavření kontejnerů automatizované systémem.</span><span class="sxs-lookup"><span data-stu-id="4bec7-107">Compared to the manual packing process, tasks such as creating containers, assigning items, and closing containers are automated by the system.</span></span> <span data-ttu-id="4bec7-108">Tento postup používá ukázkovou společnost USMF a provádí jej vedoucí skladu.</span><span class="sxs-lookup"><span data-stu-id="4bec7-108">This procedure uses the USMF demo company and is performed by a Warehouse manager.</span></span>


## <a name="set-up-a-wave-template"></a><span data-ttu-id="4bec7-109">Nastavení šablony vlny</span><span class="sxs-lookup"><span data-stu-id="4bec7-109">Set up a wave template</span></span>
1. <span data-ttu-id="4bec7-110">Přejděte do nabídky Řízení skladu > Nastavení > Vlny > Šablony vlny.</span><span class="sxs-lookup"><span data-stu-id="4bec7-110">Go to Warehouse management > Setup > Waves > Wave templates.</span></span>
2. <span data-ttu-id="4bec7-111">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="4bec7-111">Click New.</span></span>
3. <span data-ttu-id="4bec7-112">Zadejte hodnotu do pole Název šablony vlny.</span><span class="sxs-lookup"><span data-stu-id="4bec7-112">In the Wave template name field, type a value.</span></span>
4. <span data-ttu-id="4bec7-113">Zadejte hodnotu do pole Popis šablony vlny.</span><span class="sxs-lookup"><span data-stu-id="4bec7-113">In the Wave template description field, type a value.</span></span>
5. <span data-ttu-id="4bec7-114">V poli Lokalita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="4bec7-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="4bec7-115">V poli Sklad zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="4bec7-115">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="4bec7-116">Rozbalte sekci Způsoby.</span><span class="sxs-lookup"><span data-stu-id="4bec7-116">Expand the Methods section.</span></span>
    * <span data-ttu-id="4bec7-117">Podokno Vybrané metody bude obsahovat metody pro vybraný typ šablony vlny.</span><span class="sxs-lookup"><span data-stu-id="4bec7-117">The Selected methods pane lists the methods for the selected wave template type.</span></span> <span data-ttu-id="4bec7-118">Šablona vlny musí zahrnovat metodu rozdělení do kontejnerů.</span><span class="sxs-lookup"><span data-stu-id="4bec7-118">The wave template must include the containerize method.</span></span>  
8. <span data-ttu-id="4bec7-119">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="4bec7-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="4bec7-120">Zadejte hodnotu do pole Kód kroku vlny.</span><span class="sxs-lookup"><span data-stu-id="4bec7-120">In the Wave step code field, type a value.</span></span>
    * <span data-ttu-id="4bec7-121">Zadejte kód kroku vlny pro přidaný způsob, který může být tvořen libovolným kódem.</span><span class="sxs-lookup"><span data-stu-id="4bec7-121">Enter a Wave step code for the added method, which can be any code.</span></span> <span data-ttu-id="4bec7-122">Je možné přidat metodu vícekrát a přiřadit různé kódy kroku vlny.</span><span class="sxs-lookup"><span data-stu-id="4bec7-122">It’s possible to add the method more than once and assign different wave step codes.</span></span> <span data-ttu-id="4bec7-123">K tomu vyberte na stránce Metody zpracování vlny možnost Opakovatelné pro tuto metodu.</span><span class="sxs-lookup"><span data-stu-id="4bec7-123">To do this, select Repeatable for this method in the Wave process methods page.</span></span>  
10. <span data-ttu-id="4bec7-124">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="4bec7-124">Click Save.</span></span>
11. <span data-ttu-id="4bec7-125">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="4bec7-125">Close the page.</span></span>

## <a name="set-up-a-container-type"></a><span data-ttu-id="4bec7-126">Nastavení typu kontejneru</span><span class="sxs-lookup"><span data-stu-id="4bec7-126">Set up a container type</span></span>
1. <span data-ttu-id="4bec7-127">Přejděte na Řízení skladu > Nastavení > Kontejnery > Typy kontejnerů.</span><span class="sxs-lookup"><span data-stu-id="4bec7-127">Go to Warehouse management > Setup > Containers > Container types.</span></span>
    * <span data-ttu-id="4bec7-128">Kontejnery můžete definovat na stránce Typy kontejneru.</span><span class="sxs-lookup"><span data-stu-id="4bec7-128">You can define your containers in the Container types page.</span></span> <span data-ttu-id="4bec7-129">Můžete konfigurovat fyzické dimenze kontejnerů, včetně hmotnosti obalu, maximální hmotnosti, maximálního objemu, délky, šířky a výšky.</span><span class="sxs-lookup"><span data-stu-id="4bec7-129">You can configure the physical dimensions of containers including tare weight, maximum weight, maximum volume, length, width, and height.</span></span> <span data-ttu-id="4bec7-130">V tomto příkladu máme tři různé velikosti balení.</span><span class="sxs-lookup"><span data-stu-id="4bec7-130">In this example, we have three different sizes of boxes.</span></span>  
2. <span data-ttu-id="4bec7-131">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="4bec7-131">Click New.</span></span>
3. <span data-ttu-id="4bec7-132">Zadejte hodnotu do pole Typ kódu kontejneru.</span><span class="sxs-lookup"><span data-stu-id="4bec7-132">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="4bec7-133">V poli Váha obalu zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="4bec7-133">In the Tare weight field, enter a number.</span></span>
5. <span data-ttu-id="4bec7-134">Zadejte číslo do pole Maximální hmotnost.</span><span class="sxs-lookup"><span data-stu-id="4bec7-134">In the Maximum weight field, enter a number.</span></span>
6. <span data-ttu-id="4bec7-135">V poli Objem zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="4bec7-135">In the Volume field, enter a number.</span></span>
7. <span data-ttu-id="4bec7-136">Do pole Délka zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="4bec7-136">In the Length field, enter a number.</span></span>
8. <span data-ttu-id="4bec7-137">V poli Šířka zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="4bec7-137">In the Width field, enter a number.</span></span>
9. <span data-ttu-id="4bec7-138">V poli Výška zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="4bec7-138">In the Height field, enter a number.</span></span>
10. <span data-ttu-id="4bec7-139">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="4bec7-139">In the Description field, type a value.</span></span>
11. <span data-ttu-id="4bec7-140">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="4bec7-140">Click Save.</span></span>
12. <span data-ttu-id="4bec7-141">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="4bec7-141">Click New.</span></span>
13. <span data-ttu-id="4bec7-142">Zadejte hodnotu do pole Typ kódu kontejneru.</span><span class="sxs-lookup"><span data-stu-id="4bec7-142">In the Container type code field, type a value.</span></span>
14. <span data-ttu-id="4bec7-143">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="4bec7-143">In the Description field, type a value.</span></span>
15. <span data-ttu-id="4bec7-144">V poli Váha obalu zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="4bec7-144">In the Tare weight field, enter a number.</span></span>
16. <span data-ttu-id="4bec7-145">Zadejte číslo do pole Maximální hmotnost.</span><span class="sxs-lookup"><span data-stu-id="4bec7-145">In the Maximum weight field, enter a number.</span></span>
17. <span data-ttu-id="4bec7-146">V poli Objem zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="4bec7-146">In the Volume field, enter a number.</span></span>
18. <span data-ttu-id="4bec7-147">Do pole Délka zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="4bec7-147">In the Length field, enter a number.</span></span>
19. <span data-ttu-id="4bec7-148">V poli Šířka zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="4bec7-148">In the Width field, enter a number.</span></span>
20. <span data-ttu-id="4bec7-149">V poli Výška zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="4bec7-149">In the Height field, enter a number.</span></span>
21. <span data-ttu-id="4bec7-150">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="4bec7-150">Click Save.</span></span>
22. <span data-ttu-id="4bec7-151">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="4bec7-151">Click New.</span></span>
23. <span data-ttu-id="4bec7-152">Zadejte hodnotu do pole Typ kódu kontejneru.</span><span class="sxs-lookup"><span data-stu-id="4bec7-152">In the Container type code field, type a value.</span></span>
24. <span data-ttu-id="4bec7-153">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="4bec7-153">In the Description field, type a value.</span></span>
25. <span data-ttu-id="4bec7-154">V poli Váha obalu zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="4bec7-154">In the Tare weight field, enter a number.</span></span>
26. <span data-ttu-id="4bec7-155">Zadejte číslo do pole Maximální hmotnost.</span><span class="sxs-lookup"><span data-stu-id="4bec7-155">In the Maximum weight field, enter a number.</span></span>
27. <span data-ttu-id="4bec7-156">V poli Objem zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="4bec7-156">In the Volume field, enter a number.</span></span>
28. <span data-ttu-id="4bec7-157">Do pole Délka zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="4bec7-157">In the Length field, enter a number.</span></span>
29. <span data-ttu-id="4bec7-158">V poli Šířka zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="4bec7-158">In the Width field, enter a number.</span></span>
30. <span data-ttu-id="4bec7-159">V poli Výška zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="4bec7-159">In the Height field, enter a number.</span></span>
31. <span data-ttu-id="4bec7-160">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="4bec7-160">Click Save.</span></span>
32. <span data-ttu-id="4bec7-161">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="4bec7-161">Close the page.</span></span>

## <a name="set-up-a-container-group"></a><span data-ttu-id="4bec7-162">Nastavení skupin kontejneru</span><span class="sxs-lookup"><span data-stu-id="4bec7-162">Set up a container group</span></span>
1. <span data-ttu-id="4bec7-163">Přejděte na Řízení skladu > Nastavení > Kontejnery > Skupiny kontejnerů.</span><span class="sxs-lookup"><span data-stu-id="4bec7-163">Go to Warehouse management > Setup > Containers > Container groups.</span></span>
2. <span data-ttu-id="4bec7-164">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="4bec7-164">Click New.</span></span>
    * <span data-ttu-id="4bec7-165">Můžete nastavit skupiny kontejnerů logických skupin.</span><span class="sxs-lookup"><span data-stu-id="4bec7-165">You can set up logical groups of container types.</span></span> <span data-ttu-id="4bec7-166">Pro každou skupinu můžete určit pořadí, v němž mají být zabaleny kontejnery a procento zaplnění kontejnerů. Dimenze velikosti se používá k určení, zda bude pasovat do kontejneru.</span><span class="sxs-lookup"><span data-stu-id="4bec7-166">For each group, you can specify the sequence in which to pack the containers and the percentage of the containers to fill.The size dimensions of the item is used to determine whether it will fit in a container.</span></span> <span data-ttu-id="4bec7-167">Použije se kontejner, který nejlépe odpovídá dimenzím velikosti.</span><span class="sxs-lookup"><span data-stu-id="4bec7-167">The container that is closest to the size dimensions of the item is used.</span></span> <span data-ttu-id="4bec7-168">Pokud máte více typů kontejnerů ve skupině, doporučujeme, abyste uspořádali pořadí podle velikosti tak, aby největší kontejner byl první (číslo 1 v číselné řadě) a nejmenší kontejner byl poslední.</span><span class="sxs-lookup"><span data-stu-id="4bec7-168">If you have multiple container types in a group, we recommend that you arrange the sequence by size, so that the largest container is first, number 1 in the sequence, and the smallest container is last.</span></span>    
3. <span data-ttu-id="4bec7-169">Zadejte hodnotu do pole ID skupiny kontejnerů.</span><span class="sxs-lookup"><span data-stu-id="4bec7-169">In the Container group ID field, type a value.</span></span>
4. <span data-ttu-id="4bec7-170">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="4bec7-170">In the Description field, type a value.</span></span>
5. <span data-ttu-id="4bec7-171">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="4bec7-171">Click New.</span></span>
6. <span data-ttu-id="4bec7-172">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="4bec7-172">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="4bec7-173">V poli Typ kontejneru zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="4bec7-173">In the Container type field, enter or select a value.</span></span>
8. <span data-ttu-id="4bec7-174">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="4bec7-174">Click New.</span></span>
9. <span data-ttu-id="4bec7-175">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="4bec7-175">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="4bec7-176">V poli Typ kontejneru zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="4bec7-176">In the Container type field, enter or select a value.</span></span>
11. <span data-ttu-id="4bec7-177">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="4bec7-177">Click New.</span></span>
12. <span data-ttu-id="4bec7-178">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="4bec7-178">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="4bec7-179">V poli Typ kontejneru zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="4bec7-179">In the Container type field, enter or select a value.</span></span>
14. <span data-ttu-id="4bec7-180">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="4bec7-180">Click Save.</span></span>
15. <span data-ttu-id="4bec7-181">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="4bec7-181">Close the page.</span></span>

## <a name="set-up-a-container-build-template"></a><span data-ttu-id="4bec7-182">Nastavení šablony sestavení kontejneru</span><span class="sxs-lookup"><span data-stu-id="4bec7-182">Set up a container build template</span></span>
1. <span data-ttu-id="4bec7-183">Přejděte na Řízení skladu > Nastavení > Kontejnery > Šablony sestavení kontejneru.</span><span class="sxs-lookup"><span data-stu-id="4bec7-183">Go to Warehouse management > Setup > Containers > Container build templates.</span></span>
2. <span data-ttu-id="4bec7-184">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="4bec7-184">Click New.</span></span>
    * <span data-ttu-id="4bec7-185">Šablona sestavení kontejneru je založena na tom, které procesy rozdělení do kontejnerů proběhnou.</span><span class="sxs-lookup"><span data-stu-id="4bec7-185">The container build template is based on which of the containerization processes are performed.</span></span> <span data-ttu-id="4bec7-186">Každá šablona sestavení kontejneru definuje jeden proces rozdělení do kontejnerů, který šablona vlny použije.</span><span class="sxs-lookup"><span data-stu-id="4bec7-186">Each container build template defines one containerization process that will be used by a wave template.</span></span> <span data-ttu-id="4bec7-187">Možnosti Upravit dotaz umožňuje definovat podmínky, pro které budou vybrané šablony zpracovány.</span><span class="sxs-lookup"><span data-stu-id="4bec7-187">The Edit query option allows you to define the conditions on which the selected template will be processed.</span></span> <span data-ttu-id="4bec7-188">Například můžete spustit rozdělení do kontejnerů jen pro určité odběratele, produkty nebo sklady, nebo můžete přidat odpovídající rozsahy dotazu do šablony.</span><span class="sxs-lookup"><span data-stu-id="4bec7-188">For example, you may want to only run containerization for specific customers, products, or warehouses or you can add the corresponding query ranges to the template.</span></span> <span data-ttu-id="4bec7-189">Pole Kód kroku vlny popisuje, jak je šablona sestavení kontejneru propojena s kroky v šabloně vlny.</span><span class="sxs-lookup"><span data-stu-id="4bec7-189">The Wave step code field is how a container build template is linked to steps in a wave template.</span></span> <span data-ttu-id="4bec7-190">Při spuštění vlny určuje, které šablony sestavení kontejneru se používají k zahájení rozdělení do kontejnerů.</span><span class="sxs-lookup"><span data-stu-id="4bec7-190">When a wave is executed, it determines which container build template(s) are used to initiate containerization.</span></span> <span data-ttu-id="4bec7-191">Pole Základní typy dotazů určuje, co bude zabaleno, a na čem založit dotaz filtru.</span><span class="sxs-lookup"><span data-stu-id="4bec7-191">The Base query type field determines what to pack and what to base the filter query on.</span></span>  
3. <span data-ttu-id="4bec7-192">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="4bec7-192">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="4bec7-193">Zadejte hodnotu do pole ID šablony kontejneru.</span><span class="sxs-lookup"><span data-stu-id="4bec7-193">In the Container template ID field, type a value.</span></span>
5. <span data-ttu-id="4bec7-194">V poli ID skupiny kontejnerů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="4bec7-194">In the Container group ID field, enter or select a value.</span></span>
6. <span data-ttu-id="4bec7-195">Zadejte hodnotu do pole Kód kroku vlny.</span><span class="sxs-lookup"><span data-stu-id="4bec7-195">In the Wave step code field, type a value.</span></span>
7. <span data-ttu-id="4bec7-196">Zaškrtněte políčko Povolit rozdělení výdeje.</span><span class="sxs-lookup"><span data-stu-id="4bec7-196">Select the Allow split picks check box.</span></span>
8. <span data-ttu-id="4bec7-197">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="4bec7-197">Click Save.</span></span>
9. <span data-ttu-id="4bec7-198">Klikněte na Omezení kombinování obsahu kontejnerů.</span><span class="sxs-lookup"><span data-stu-id="4bec7-198">Click Containier mixing constraints.</span></span>
    * <span data-ttu-id="4bec7-199">Přerušení smíšené logiky umožňuje nastavit pravidla pro řádky přidělení balení do kontejnerů.</span><span class="sxs-lookup"><span data-stu-id="4bec7-199">Mixing logic breaks allows you to set up rules for packing allocation lines in containers.</span></span> <span data-ttu-id="4bec7-200">Například pokud chcete přidat pole Číslo položky, když jsou položky přiřazeny do kontejnerů, bude při vygenerování nového čísla položky vytvořen nový kontejner.</span><span class="sxs-lookup"><span data-stu-id="4bec7-200">For example, if you add the Item number field, when items are assigned to containers, a new container will be created when there is a new item number.</span></span> <span data-ttu-id="4bec7-201">To zabrání pracovníkům přibalit přidělovací řádky pro dva různé zákazníky do stejného kontejneru.</span><span class="sxs-lookup"><span data-stu-id="4bec7-201">This is will prevent workers from packing allocations lines for two different customers in the same container.</span></span>  
10. <span data-ttu-id="4bec7-202">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="4bec7-202">Click New.</span></span>
11. <span data-ttu-id="4bec7-203">Vyberte volbu v poli Tabulka.</span><span class="sxs-lookup"><span data-stu-id="4bec7-203">In the Table field, select an option.</span></span>
12. <span data-ttu-id="4bec7-204">V poli Výběr pole zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="4bec7-204">In the Field Select field, enter or select a value.</span></span>
13. <span data-ttu-id="4bec7-205">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="4bec7-205">Click OK.</span></span>

