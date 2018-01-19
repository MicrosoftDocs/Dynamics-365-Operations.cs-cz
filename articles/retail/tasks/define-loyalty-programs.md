--- 
title: " Definování věrnostních programů"
description: "Tato procedura popisuje, jak nastavit věrnostní program pomocí dvou věrnostních úrovní."
author: jashanno
manager: AnnBe
ms.date: 11/14/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: f57778078430932f73a6b55c9602d28a938234b1
ms.contentlocale: cs-cz
ms.lasthandoff: 01/19/2018

---
# <a name="define-loyalty-programs"></a><span data-ttu-id="1d41e-103"> Definování věrnostních programů</span><span class="sxs-lookup"><span data-stu-id="1d41e-103">Define loyalty programs</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="1d41e-104">Tato procedura popisuje, jak nastavit věrnostní program pomocí dvou věrnostních úrovní.</span><span class="sxs-lookup"><span data-stu-id="1d41e-104">This procedure shows how to set up a loyalty program with two loyalty tiers.</span></span> <span data-ttu-id="1d41e-105">Tato procedura používá data ukázkové společnosti USRT.</span><span class="sxs-lookup"><span data-stu-id="1d41e-105">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="1d41e-106">Přejděte na Maloobchodní a velkoobchodní prodej > ..</span><span class="sxs-lookup"><span data-stu-id="1d41e-106">Go to Retail and commerce > ..</span></span> <span data-ttu-id="1d41e-107">> Věrnostní programy.</span><span class="sxs-lookup"><span data-stu-id="1d41e-107">> Loyalty programs.</span></span>
2. <span data-ttu-id="1d41e-108">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="1d41e-108">Click New.</span></span>
3. <span data-ttu-id="1d41e-109">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="1d41e-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="1d41e-110">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="1d41e-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="1d41e-111">Klikněte na Přidat řádek.</span><span class="sxs-lookup"><span data-stu-id="1d41e-111">Click Add line.</span></span>
6. <span data-ttu-id="1d41e-112">Do pole Úroveň zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="1d41e-112">In the Level field, enter a number.</span></span>
7. <span data-ttu-id="1d41e-113">Do pole Úroveň zadejte název věrnostní úrovně.</span><span class="sxs-lookup"><span data-stu-id="1d41e-113">In the Tier field, enter a name for the loyalty tier.</span></span>
8. <span data-ttu-id="1d41e-114">Zadejte hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="1d41e-114">In the Description field, type a value.</span></span>
9. <span data-ttu-id="1d41e-115">V poli Časový interval kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="1d41e-115">In the Date interval field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="1d41e-116">Tento časový interval musí být rozšířen do budoucna.</span><span class="sxs-lookup"><span data-stu-id="1d41e-116">This date interval should extend into the future.</span></span> <span data-ttu-id="1d41e-117">Pokud je například časový interval vybraný pro zlatou úroveň jeden rok, kterýkoli odběratel, který je oprávněn pro zlatou úroveň, může získat odměny, které jsou zlaté úrovni přiřazeny, po dobu jednoho roku.</span><span class="sxs-lookup"><span data-stu-id="1d41e-117">For example, if the date interval that is selected for gold tier is a one-year period, any customer who qualifies for the gold tier can receive the rewards that are assigned to the gold tier for one year.</span></span> <span data-ttu-id="1d41e-118">Pokud se odběratel znovu kvalifikuje pro zlatou úroveň, když je na této úrovni, datum vypršení jeho stavu bude prodlouženo o další rok od data opětovné kvalifikace.</span><span class="sxs-lookup"><span data-stu-id="1d41e-118">If the customer re-qualifies for the gold tier while they are in the tier, the date that the tier expires is extended by another year from the date when they re-qualify.</span></span>  
10. <span data-ttu-id="1d41e-119">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="1d41e-119">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="1d41e-120">Klikněte na položku Přidat řádek.</span><span class="sxs-lookup"><span data-stu-id="1d41e-120">Click Add line.</span></span>
12. <span data-ttu-id="1d41e-121">Do pole Úroveň zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="1d41e-121">In the Level field, enter a number.</span></span>
13. <span data-ttu-id="1d41e-122">Do pole Úroveň zadejte název věrnostní úrovně.</span><span class="sxs-lookup"><span data-stu-id="1d41e-122">In the Tier field, enter a name for the loyalty tier.</span></span>
14. <span data-ttu-id="1d41e-123">Zadejte hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="1d41e-123">In the Description field, type a value.</span></span>
15. <span data-ttu-id="1d41e-124">V poli Časový interval kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="1d41e-124">In the Date interval field, click the drop-down button to open the lookup.</span></span>
16. <span data-ttu-id="1d41e-125">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="1d41e-125">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="1d41e-126">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="1d41e-126">Click Save.</span></span>
18. <span data-ttu-id="1d41e-127">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="1d41e-127">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="1d41e-128">Pravidla úrovně definují minimální počet bodů odměny potřebný k získání během časového období pro získání úrovně.</span><span class="sxs-lookup"><span data-stu-id="1d41e-128">Tier rules define the minimum number of a reward point needed to be earned during a time period to qualify for the tier.</span></span>  
19. <span data-ttu-id="1d41e-129">Přepněte rozšíření oddílu Pravidla úrovně.</span><span class="sxs-lookup"><span data-stu-id="1d41e-129">Toggle the expansion of the Tier rules section.</span></span>
20. <span data-ttu-id="1d41e-130">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="1d41e-130">Click New.</span></span>
    * <span data-ttu-id="1d41e-131">Pro každou úroveň můžete uchovávat více než jedno pravidlo úrovně.</span><span class="sxs-lookup"><span data-stu-id="1d41e-131">You can have more than one tier rule per tier.</span></span> <span data-ttu-id="1d41e-132">Můžete mít například tři různá kritéria pro získání úrovně; útratu 500 USD v jednom měsíci, útratu 1 000 USD během jednoho roku a provedením 20 transakcí za jeden rok.</span><span class="sxs-lookup"><span data-stu-id="1d41e-132">For example, you could have three different criteria to earn a tier; by spending $500 in one month, by spending $1000 over one year, and by having 20 transactions in one year.</span></span> <span data-ttu-id="1d41e-133">Chcete-li to provést, je nutné vytvořit tři pravidla úrovní.</span><span class="sxs-lookup"><span data-stu-id="1d41e-133">To do this, you would need to create three tier rules.</span></span>  
21. <span data-ttu-id="1d41e-134">V poli Bod odměny kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="1d41e-134">In the Reward point field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="1d41e-135">Tento bod věrnostní odměny by měl být neuplatnitelný.</span><span class="sxs-lookup"><span data-stu-id="1d41e-135">This should be a non-redeemable loyalty reward point.</span></span>  
22. <span data-ttu-id="1d41e-136">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="1d41e-136">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="1d41e-137">V poli Minimální počet vydaných bodů zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="1d41e-137">In the Minimum issued points field, enter a number.</span></span>
    * <span data-ttu-id="1d41e-138">Pokud se na nejnižší věrnostní úroveň mohou kvalifikovat všichni zákazníci pouhou účastí v programu, zadejte hodnotu „0“.</span><span class="sxs-lookup"><span data-stu-id="1d41e-138">For the lowest level tier, if all customers qualify simply by participating in the program, enter '0'.</span></span>  
24. <span data-ttu-id="1d41e-139">V poli Interval data hodnocení kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="1d41e-139">In the Evaluation date interval field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="1d41e-140">Tento časový interval musí být rozšířen do minulosti.</span><span class="sxs-lookup"><span data-stu-id="1d41e-140">This date interval should extend into the past.</span></span> <span data-ttu-id="1d41e-141">K dosažení minimální hodnoty vydaných bodů budou započítány pouze body získaných v tomto časovém intervalu.</span><span class="sxs-lookup"><span data-stu-id="1d41e-141">Only points earned during this date interval will be counted towards reaching the minimum issued points value.</span></span>  
25. <span data-ttu-id="1d41e-142">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="1d41e-142">In the list, click the link in the selected row.</span></span>
26. <span data-ttu-id="1d41e-143">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="1d41e-143">Click Save.</span></span>
27. <span data-ttu-id="1d41e-144">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="1d41e-144">In the list, find and select the desired record.</span></span>
28. <span data-ttu-id="1d41e-145">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="1d41e-145">Click New.</span></span>
29. <span data-ttu-id="1d41e-146">V poli Bod odměny kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="1d41e-146">In the Reward point field, click the drop-down button to open the lookup.</span></span>
30. <span data-ttu-id="1d41e-147">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="1d41e-147">In the list, click the link in the selected row.</span></span>
31. <span data-ttu-id="1d41e-148">V poli Minimální počet vydaných bodů zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="1d41e-148">In the Minimum issued points field, enter a number.</span></span>
32. <span data-ttu-id="1d41e-149">V poli Interval data hodnocení kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="1d41e-149">In the Evaluation date interval field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="1d41e-150">Tento časový interval musí být rozšířen do minulosti.</span><span class="sxs-lookup"><span data-stu-id="1d41e-150">This date interval should extend into the past.</span></span>  
33. <span data-ttu-id="1d41e-151">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="1d41e-151">In the list, click the link in the selected row.</span></span>
34. <span data-ttu-id="1d41e-152">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="1d41e-152">Click Save.</span></span>
35. <span data-ttu-id="1d41e-153">Klikněte na možnost Cenové skupiny.</span><span class="sxs-lookup"><span data-stu-id="1d41e-153">Click Price groups.</span></span>
    * <span data-ttu-id="1d41e-154">Pokud chcete udělit věrnostní slevy odběratelům.</span><span class="sxs-lookup"><span data-stu-id="1d41e-154">If you want to give loyalty customers discounts.</span></span> <span data-ttu-id="1d41e-155">je nutné přiřadit jednu nebo více cenových skupin do věrnostního programu a přiřadit cenové skupiny slevám.</span><span class="sxs-lookup"><span data-stu-id="1d41e-155">you'll need to assign one or more price groups to the loyalty program and assign the price groups to discounts.</span></span> <span data-ttu-id="1d41e-156">Je nejvhodnější pro různé entity typů slev nemíchat cenové skupiny.</span><span class="sxs-lookup"><span data-stu-id="1d41e-156">It is a best practice to not mix price groups across different types of discounting entities.</span></span>  <span data-ttu-id="1d41e-157">Například nepoužívejte stejnou cenovou skupinu pro věrnostní slevy a slevu kanálu.</span><span class="sxs-lookup"><span data-stu-id="1d41e-157">For example, don't use the same price group for a loyalty discount and a channel discount.</span></span>  
36. <span data-ttu-id="1d41e-158">V poli Cenová skupina kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="1d41e-158">In the Price group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="1d41e-159">Propojení Cenové skupiny v horní části stránky je pro věrnostní program.</span><span class="sxs-lookup"><span data-stu-id="1d41e-159">The Price groups link at the top of the page is for the loyalty program.</span></span> <span data-ttu-id="1d41e-160">Propojení Cenové skupiny na pevné záložce Úrovně programu je určeno pouze konkrétní věrnostní úroveň.</span><span class="sxs-lookup"><span data-stu-id="1d41e-160">The Price groups link in the Program tiers fasttab is for a specific loyalty tier only.</span></span>  
37. <span data-ttu-id="1d41e-161">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="1d41e-161">In the list, click the link in the selected row.</span></span>
38. <span data-ttu-id="1d41e-162">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="1d41e-162">Click Save.</span></span>
39. <span data-ttu-id="1d41e-163">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="1d41e-163">Close the page.</span></span>
40. <span data-ttu-id="1d41e-164">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="1d41e-164">Click Save.</span></span>


