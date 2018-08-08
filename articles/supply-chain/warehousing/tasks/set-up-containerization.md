--- 
title: "Nastavení vytváření kontejnerů"
description: "Tento postup popisuje postup automatizace vytváření kontejnerů vytížení v modulu Řízení skladu."
author: ShylaThompson
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 387caf5b8882b768993dbdcfb2b0b10131640dfa
ms.contentlocale: cs-cz
ms.lasthandoff: 08/07/2018

---
# <a name="set-up-containerization"></a><span data-ttu-id="13bc8-103">Nastavení vytváření kontejnerů</span><span class="sxs-lookup"><span data-stu-id="13bc8-103">Set up containerization</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="13bc8-104">Tento postup popisuje postup automatizace vytváření kontejnerů vytížení v modulu Řízení skladu.</span><span class="sxs-lookup"><span data-stu-id="13bc8-104">This procedure describes how to automate the containerization of loads in Warehouse management.</span></span> <span data-ttu-id="13bc8-105">Automatické vytváření kontejnerů vytvoří kontejnery a výdejovou práci pro dodávky při zpracování vlny, a řádky práce lze rozdělit na množství, které se vejde do kontejnerů.</span><span class="sxs-lookup"><span data-stu-id="13bc8-105">Automated containerization creates containers and the picking work for shipments when a wave is processed and work lines can be split into quantities that fit the containers.</span></span> <span data-ttu-id="13bc8-106">To pomáhá pracovníkům skladu vyzvednout položky přímo do zvoleného kontejneru.</span><span class="sxs-lookup"><span data-stu-id="13bc8-106">This helps warehouse workers to pick the items directly into the chosen container.</span></span> <span data-ttu-id="13bc8-107">Ve srovnání s procesem ručního balení jsou úlohy, jako je vytváření kontejnerů, přiřazování položek nebo uzavření kontejnerů automatizované systémem.</span><span class="sxs-lookup"><span data-stu-id="13bc8-107">Compared to the manual packing process, tasks such as creating containers, assigning items, and closing containers are automated by the system.</span></span> <span data-ttu-id="13bc8-108">Tento postup používá ukázkovou společnost USMF a provádí jej vedoucí skladu.</span><span class="sxs-lookup"><span data-stu-id="13bc8-108">This procedure uses the USMF demo company and is performed by a Warehouse manager.</span></span>


## <a name="set-up-a-wave-template"></a><span data-ttu-id="13bc8-109">Nastavení šablony vlny</span><span class="sxs-lookup"><span data-stu-id="13bc8-109">Set up a wave template</span></span>
1. <span data-ttu-id="13bc8-110">Přejděte do nabídky Řízení skladu > Nastavení > Vlny > Šablony vlny.</span><span class="sxs-lookup"><span data-stu-id="13bc8-110">Go to Warehouse management > Setup > Waves > Wave templates.</span></span>
2. <span data-ttu-id="13bc8-111">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="13bc8-111">Click New.</span></span>
3. <span data-ttu-id="13bc8-112">Zadejte hodnotu do pole Název šablony vlny.</span><span class="sxs-lookup"><span data-stu-id="13bc8-112">In the Wave template name field, type a value.</span></span>
4. <span data-ttu-id="13bc8-113">Zadejte hodnotu do pole Popis šablony vlny.</span><span class="sxs-lookup"><span data-stu-id="13bc8-113">In the Wave template description field, type a value.</span></span>
5. <span data-ttu-id="13bc8-114">V poli Lokalita zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="13bc8-114">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="13bc8-115">V poli Sklad zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="13bc8-115">In the Warehouse field, enter or select a value.</span></span>
7. <span data-ttu-id="13bc8-116">Rozbalte sekci Způsoby.</span><span class="sxs-lookup"><span data-stu-id="13bc8-116">Expand the Methods section.</span></span>
    * <span data-ttu-id="13bc8-117">Podokno Vybrané metody bude obsahovat metody pro vybraný typ šablony vlny.</span><span class="sxs-lookup"><span data-stu-id="13bc8-117">The Selected methods pane lists the methods for the selected wave template type.</span></span> <span data-ttu-id="13bc8-118">Šablona vlny musí zahrnovat metodu rozdělení do kontejnerů.</span><span class="sxs-lookup"><span data-stu-id="13bc8-118">The wave template must include the containerize method.</span></span>  
8. <span data-ttu-id="13bc8-119">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="13bc8-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="13bc8-120">Zadejte hodnotu do pole Kód kroku vlny.</span><span class="sxs-lookup"><span data-stu-id="13bc8-120">In the Wave step code field, type a value.</span></span>
    * <span data-ttu-id="13bc8-121">Zadejte kód kroku vlny pro přidaný způsob, který může být tvořen libovolným kódem.</span><span class="sxs-lookup"><span data-stu-id="13bc8-121">Enter a Wave step code for the added method, which can be any code.</span></span> <span data-ttu-id="13bc8-122">Je možné přidat metodu vícekrát a přiřadit různé kódy kroku vlny.</span><span class="sxs-lookup"><span data-stu-id="13bc8-122">It’s possible to add the method more than once and assign different wave step codes.</span></span> <span data-ttu-id="13bc8-123">K tomu vyberte na stránce Metody zpracování vlny možnost Opakovatelné pro tuto metodu.</span><span class="sxs-lookup"><span data-stu-id="13bc8-123">To do this, select Repeatable for this method in the Wave process methods page.</span></span>  
10. <span data-ttu-id="13bc8-124">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="13bc8-124">Click Save.</span></span>
11. <span data-ttu-id="13bc8-125">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="13bc8-125">Close the page.</span></span>

## <a name="set-up-a-container-type"></a><span data-ttu-id="13bc8-126">Nastavení typu kontejneru</span><span class="sxs-lookup"><span data-stu-id="13bc8-126">Set up a container type</span></span>
1. <span data-ttu-id="13bc8-127">Přejděte na Řízení skladu > Nastavení > Kontejnery > Typy kontejnerů.</span><span class="sxs-lookup"><span data-stu-id="13bc8-127">Go to Warehouse management > Setup > Containers > Container types.</span></span>
    * <span data-ttu-id="13bc8-128">Kontejnery můžete definovat na stránce Typy kontejneru.</span><span class="sxs-lookup"><span data-stu-id="13bc8-128">You can define your containers in the Container types page.</span></span> <span data-ttu-id="13bc8-129">Můžete konfigurovat fyzické dimenze kontejnerů, včetně hmotnosti obalu, maximální hmotnosti, maximálního objemu, délky, šířky a výšky.</span><span class="sxs-lookup"><span data-stu-id="13bc8-129">You can configure the physical dimensions of containers including tare weight, maximum weight, maximum volume, length, width, and height.</span></span> <span data-ttu-id="13bc8-130">V tomto příkladu máme tři různé velikosti balení.</span><span class="sxs-lookup"><span data-stu-id="13bc8-130">In this example, we have three different sizes of boxes.</span></span>  
2. <span data-ttu-id="13bc8-131">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="13bc8-131">Click New.</span></span>
3. <span data-ttu-id="13bc8-132">Zadejte hodnotu do pole Typ kódu kontejneru.</span><span class="sxs-lookup"><span data-stu-id="13bc8-132">In the Container type code field, type a value.</span></span>
4. <span data-ttu-id="13bc8-133">V poli Váha obalu zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="13bc8-133">In the Tare weight field, enter a number.</span></span>
5. <span data-ttu-id="13bc8-134">Zadejte číslo do pole Maximální hmotnost.</span><span class="sxs-lookup"><span data-stu-id="13bc8-134">In the Maximum weight field, enter a number.</span></span>
6. <span data-ttu-id="13bc8-135">V poli Objem zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="13bc8-135">In the Volume field, enter a number.</span></span>
7. <span data-ttu-id="13bc8-136">Do pole Délka zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="13bc8-136">In the Length field, enter a number.</span></span>
8. <span data-ttu-id="13bc8-137">V poli Šířka zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="13bc8-137">In the Width field, enter a number.</span></span>
9. <span data-ttu-id="13bc8-138">V poli Výška zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="13bc8-138">In the Height field, enter a number.</span></span>
10. <span data-ttu-id="13bc8-139">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="13bc8-139">In the Description field, type a value.</span></span>
11. <span data-ttu-id="13bc8-140">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="13bc8-140">Click Save.</span></span>
12. <span data-ttu-id="13bc8-141">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="13bc8-141">Click New.</span></span>
13. <span data-ttu-id="13bc8-142">Zadejte hodnotu do pole Typ kódu kontejneru.</span><span class="sxs-lookup"><span data-stu-id="13bc8-142">In the Container type code field, type a value.</span></span>
14. <span data-ttu-id="13bc8-143">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="13bc8-143">In the Description field, type a value.</span></span>
15. <span data-ttu-id="13bc8-144">V poli Váha obalu zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="13bc8-144">In the Tare weight field, enter a number.</span></span>
16. <span data-ttu-id="13bc8-145">Zadejte číslo do pole Maximální hmotnost.</span><span class="sxs-lookup"><span data-stu-id="13bc8-145">In the Maximum weight field, enter a number.</span></span>
17. <span data-ttu-id="13bc8-146">V poli Objem zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="13bc8-146">In the Volume field, enter a number.</span></span>
18. <span data-ttu-id="13bc8-147">Do pole Délka zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="13bc8-147">In the Length field, enter a number.</span></span>
19. <span data-ttu-id="13bc8-148">V poli Šířka zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="13bc8-148">In the Width field, enter a number.</span></span>
20. <span data-ttu-id="13bc8-149">V poli Výška zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="13bc8-149">In the Height field, enter a number.</span></span>
21. <span data-ttu-id="13bc8-150">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="13bc8-150">Click Save.</span></span>
22. <span data-ttu-id="13bc8-151">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="13bc8-151">Click New.</span></span>
23. <span data-ttu-id="13bc8-152">Zadejte hodnotu do pole Typ kódu kontejneru.</span><span class="sxs-lookup"><span data-stu-id="13bc8-152">In the Container type code field, type a value.</span></span>
24. <span data-ttu-id="13bc8-153">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="13bc8-153">In the Description field, type a value.</span></span>
25. <span data-ttu-id="13bc8-154">V poli Váha obalu zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="13bc8-154">In the Tare weight field, enter a number.</span></span>
26. <span data-ttu-id="13bc8-155">Zadejte číslo do pole Maximální hmotnost.</span><span class="sxs-lookup"><span data-stu-id="13bc8-155">In the Maximum weight field, enter a number.</span></span>
27. <span data-ttu-id="13bc8-156">V poli Objem zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="13bc8-156">In the Volume field, enter a number.</span></span>
28. <span data-ttu-id="13bc8-157">Do pole Délka zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="13bc8-157">In the Length field, enter a number.</span></span>
29. <span data-ttu-id="13bc8-158">V poli Šířka zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="13bc8-158">In the Width field, enter a number.</span></span>
30. <span data-ttu-id="13bc8-159">V poli Výška zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="13bc8-159">In the Height field, enter a number.</span></span>
31. <span data-ttu-id="13bc8-160">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="13bc8-160">Click Save.</span></span>
32. <span data-ttu-id="13bc8-161">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="13bc8-161">Close the page.</span></span>

## <a name="set-up-a-container-group"></a><span data-ttu-id="13bc8-162">Nastavení skupin kontejneru</span><span class="sxs-lookup"><span data-stu-id="13bc8-162">Set up a container group</span></span>
1. <span data-ttu-id="13bc8-163">Přejděte na Řízení skladu > Nastavení > Kontejnery > Skupiny kontejnerů.</span><span class="sxs-lookup"><span data-stu-id="13bc8-163">Go to Warehouse management > Setup > Containers > Container groups.</span></span>
2. <span data-ttu-id="13bc8-164">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="13bc8-164">Click New.</span></span>
    * <span data-ttu-id="13bc8-165">Můžete nastavit skupiny kontejnerů logických skupin.</span><span class="sxs-lookup"><span data-stu-id="13bc8-165">You can set up logical groups of container types.</span></span> <span data-ttu-id="13bc8-166">Pro každou skupinu můžete určit pořadí, v němž dojde k zabalení kontejnerů, a vyžadované procento naplnění kontejnerů.</span><span class="sxs-lookup"><span data-stu-id="13bc8-166">For each group, you can specify the sequence in which to pack the containers and the percentage of the containers to fill.</span></span> <span data-ttu-id="13bc8-167">Používá se dimenze velikosti pro položky k určení toho, zda budou odpovídat kontejneru.</span><span class="sxs-lookup"><span data-stu-id="13bc8-167">The size dimensions of the item is used to determine whether it will fit in a container.</span></span> <span data-ttu-id="13bc8-168">Použije se kontejner, který nejlépe odpovídá dimenzím velikosti.</span><span class="sxs-lookup"><span data-stu-id="13bc8-168">The container that is closest to the size dimensions of the item is used.</span></span> <span data-ttu-id="13bc8-169">Pokud máte více typů kontejnerů ve skupině, doporučujeme, abyste uspořádali pořadí podle velikosti tak, aby největší kontejner byl první (číslo 1 v číselné řadě) a nejmenší kontejner byl poslední.</span><span class="sxs-lookup"><span data-stu-id="13bc8-169">If you have multiple container types in a group, we recommend that you arrange the sequence by size, so that the largest container is first, number 1 in the sequence, and the smallest container is last.</span></span>    
3. <span data-ttu-id="13bc8-170">Zadejte hodnotu do pole ID skupiny kontejnerů.</span><span class="sxs-lookup"><span data-stu-id="13bc8-170">In the Container group ID field, type a value.</span></span>
4. <span data-ttu-id="13bc8-171">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="13bc8-171">In the Description field, type a value.</span></span>
5. <span data-ttu-id="13bc8-172">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="13bc8-172">Click New.</span></span>
6. <span data-ttu-id="13bc8-173">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="13bc8-173">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="13bc8-174">V poli Typ kontejneru zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="13bc8-174">In the Container type field, enter or select a value.</span></span>
8. <span data-ttu-id="13bc8-175">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="13bc8-175">Click New.</span></span>
9. <span data-ttu-id="13bc8-176">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="13bc8-176">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="13bc8-177">V poli Typ kontejneru zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="13bc8-177">In the Container type field, enter or select a value.</span></span>
11. <span data-ttu-id="13bc8-178">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="13bc8-178">Click New.</span></span>
12. <span data-ttu-id="13bc8-179">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="13bc8-179">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="13bc8-180">V poli Typ kontejneru zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="13bc8-180">In the Container type field, enter or select a value.</span></span>
14. <span data-ttu-id="13bc8-181">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="13bc8-181">Click Save.</span></span>
15. <span data-ttu-id="13bc8-182">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="13bc8-182">Close the page.</span></span>

## <a name="set-up-a-container-build-template"></a><span data-ttu-id="13bc8-183">Nastavení šablony sestavení kontejneru</span><span class="sxs-lookup"><span data-stu-id="13bc8-183">Set up a container build template</span></span>
1. <span data-ttu-id="13bc8-184">Přejděte na Řízení skladu > Nastavení > Kontejnery > Šablony sestavení kontejneru.</span><span class="sxs-lookup"><span data-stu-id="13bc8-184">Go to Warehouse management > Setup > Containers > Container build templates.</span></span>
2. <span data-ttu-id="13bc8-185">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="13bc8-185">Click New.</span></span>
    * <span data-ttu-id="13bc8-186">Šablona sestavení kontejneru je založena na tom, které procesy rozdělení do kontejnerů proběhnou.</span><span class="sxs-lookup"><span data-stu-id="13bc8-186">The container build template is based on which of the containerization processes are performed.</span></span> <span data-ttu-id="13bc8-187">Každá šablona sestavení kontejneru definuje jeden proces rozdělení do kontejnerů, který šablona vlny použije.</span><span class="sxs-lookup"><span data-stu-id="13bc8-187">Each container build template defines one containerization process that will be used by a wave template.</span></span> <span data-ttu-id="13bc8-188">Možnosti Upravit dotaz umožňuje definovat podmínky, pro které budou vybrané šablony zpracovány.</span><span class="sxs-lookup"><span data-stu-id="13bc8-188">The Edit query option allows you to define the conditions on which the selected template will be processed.</span></span> <span data-ttu-id="13bc8-189">Například můžete spustit rozdělení do kontejnerů jen pro určité odběratele, produkty nebo sklady, nebo můžete přidat odpovídající rozsahy dotazu do šablony.</span><span class="sxs-lookup"><span data-stu-id="13bc8-189">For example, you may want to only run containerization for specific customers, products, or warehouses or you can add the corresponding query ranges to the template.</span></span> <span data-ttu-id="13bc8-190">Pole Kód kroku vlny popisuje, jak je šablona sestavení kontejneru propojena s kroky v šabloně vlny.</span><span class="sxs-lookup"><span data-stu-id="13bc8-190">The Wave step code field is how a container build template is linked to steps in a wave template.</span></span> <span data-ttu-id="13bc8-191">Při spuštění vlny určuje, které šablony sestavení kontejneru se používají k zahájení rozdělení do kontejnerů.</span><span class="sxs-lookup"><span data-stu-id="13bc8-191">When a wave is executed, it determines which container build template(s) are used to initiate containerization.</span></span> <span data-ttu-id="13bc8-192">Pole Základní typy dotazů určuje, co bude zabaleno, a na čem založit dotaz filtru.</span><span class="sxs-lookup"><span data-stu-id="13bc8-192">The Base query type field determines what to pack and what to base the filter query on.</span></span>  
3. <span data-ttu-id="13bc8-193">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="13bc8-193">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="13bc8-194">Zadejte hodnotu do pole ID šablony kontejneru.</span><span class="sxs-lookup"><span data-stu-id="13bc8-194">In the Container template ID field, type a value.</span></span>
5. <span data-ttu-id="13bc8-195">V poli ID skupiny kontejnerů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="13bc8-195">In the Container group ID field, enter or select a value.</span></span>
6. <span data-ttu-id="13bc8-196">Zadejte hodnotu do pole Kód kroku vlny.</span><span class="sxs-lookup"><span data-stu-id="13bc8-196">In the Wave step code field, type a value.</span></span>
7. <span data-ttu-id="13bc8-197">Zaškrtněte políčko Povolit rozdělení výdeje.</span><span class="sxs-lookup"><span data-stu-id="13bc8-197">Select the Allow split picks check box.</span></span>
8. <span data-ttu-id="13bc8-198">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="13bc8-198">Click Save.</span></span>
9. <span data-ttu-id="13bc8-199">Klikněte na Omezení kombinování obsahu kontejnerů.</span><span class="sxs-lookup"><span data-stu-id="13bc8-199">Click Container mixing constraints.</span></span>
    * <span data-ttu-id="13bc8-200">Přerušení smíšené logiky umožňuje nastavit pravidla pro řádky přidělení balení do kontejnerů.</span><span class="sxs-lookup"><span data-stu-id="13bc8-200">Mixing logic breaks allows you to set up rules for packing allocation lines in containers.</span></span> <span data-ttu-id="13bc8-201">Například pokud chcete přidat pole Číslo položky, když jsou položky přiřazeny do kontejnerů, bude při vygenerování nového čísla položky vytvořen nový kontejner.</span><span class="sxs-lookup"><span data-stu-id="13bc8-201">For example, if you add the Item number field, when items are assigned to containers, a new container will be created when there is a new item number.</span></span> <span data-ttu-id="13bc8-202">To zabrání pracovníkům přibalit přidělovací řádky pro dva různé zákazníky do stejného kontejneru.</span><span class="sxs-lookup"><span data-stu-id="13bc8-202">This is will prevent workers from packing allocations lines for two different customers in the same container.</span></span>  
10. <span data-ttu-id="13bc8-203">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="13bc8-203">Click New.</span></span>
11. <span data-ttu-id="13bc8-204">Vyberte volbu v poli Tabulka.</span><span class="sxs-lookup"><span data-stu-id="13bc8-204">In the Table field, select an option.</span></span>
12. <span data-ttu-id="13bc8-205">V poli Výběr pole zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="13bc8-205">In the Field Select field, enter or select a value.</span></span>
13. <span data-ttu-id="13bc8-206">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="13bc8-206">Click OK.</span></span>


