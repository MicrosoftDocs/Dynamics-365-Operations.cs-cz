--- 
title: "Nastavit kompenzační mřížky"
description: "Kompenzační mřížky umožňují definovat a spravovat struktury plateb pro plány fixní kompenzace."
author: kherr75
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a9d0d9a3f278a09e89311ee75b6f95fb4f3b04cb
ms.openlocfilehash: 39655850c1d54c56737881363bf5f805079fac89
ms.contentlocale: cs-cz
ms.lasthandoff: 02/02/2018

---
# <a name="set-up-compensation-grids"></a><span data-ttu-id="ca81c-103">Nastavit kompenzační mřížky</span><span class="sxs-lookup"><span data-stu-id="ca81c-103">Set up compensation grids</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ca81c-104">Kompenzační mřížky umožňují definovat a spravovat struktury plateb pro plány fixní kompenzace.</span><span class="sxs-lookup"><span data-stu-id="ca81c-104">Compensation grids are used to define and maintain the pay structures for fixed compensation plans.</span></span> <span data-ttu-id="ca81c-105">Kompenzační mřížky můžete sdílet mezi několika plány nebo zkopírovat při vytvoření nového plánu kompenzace.</span><span class="sxs-lookup"><span data-stu-id="ca81c-105">Compensation grids can be shared between multiple plans or copied when creating a new compensation plan.</span></span>  <span data-ttu-id="ca81c-106">Před vytvořením kompenzační mřížky, je nutné nastavit úrovně a referenční body.</span><span class="sxs-lookup"><span data-stu-id="ca81c-106">Before creating a compensation grid, Levels and Reference points must be set up.</span></span> <span data-ttu-id="ca81c-107">V tomto příkladu vytvoříme nový typ třídy kompenzační mřížky pomocí ukázkových dat pro úrovně a referenční body.</span><span class="sxs-lookup"><span data-stu-id="ca81c-107">This example will create a new Grade type of compensation grid using demo data for the Levels and Reference points.</span></span> <span data-ttu-id="ca81c-108">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="ca81c-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-information-about-the-compensation-grid"></a><span data-ttu-id="ca81c-109">Nastavit informace o kompenzační mřížce</span><span class="sxs-lookup"><span data-stu-id="ca81c-109">Set up information about the compensation grid</span></span>
1. <span data-ttu-id="ca81c-110">Přejděte do nabídky Lidské zdroje > Kompenzace > Fixní kompenzace > Kompenzační mřížky.</span><span class="sxs-lookup"><span data-stu-id="ca81c-110">Go to Human resources > Compensation > Fixed compensation > Compensation grids.</span></span>
2. <span data-ttu-id="ca81c-111">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="ca81c-111">Click New.</span></span>
3. <span data-ttu-id="ca81c-112">Zadejte hodnotu do pole Mřížka.</span><span class="sxs-lookup"><span data-stu-id="ca81c-112">In the Grid field, type a value.</span></span>
4. <span data-ttu-id="ca81c-113">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="ca81c-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ca81c-114">Vyberte volbu v poli Typ.</span><span class="sxs-lookup"><span data-stu-id="ca81c-114">In the Type field, select an option.</span></span>
6. <span data-ttu-id="ca81c-115">V poli Nastavení reference zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ca81c-115">In the Reference setup field, enter or select a value.</span></span>
7. <span data-ttu-id="ca81c-116">V poli Měna zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ca81c-116">In the Currency field, enter or select a value.</span></span>
8. <span data-ttu-id="ca81c-117">Zadejte hodnotu do pole Měna.</span><span class="sxs-lookup"><span data-stu-id="ca81c-117">In the Currency field, type a value.</span></span>
9. <span data-ttu-id="ca81c-118">Zadejte datum do pole Datum platnosti.</span><span class="sxs-lookup"><span data-stu-id="ca81c-118">In the Effective date field, enter a date.</span></span>

## <a name="add-levels-to-the-compensation-structure"></a><span data-ttu-id="ca81c-119">Přidání úrovní do kompenzační struktury</span><span class="sxs-lookup"><span data-stu-id="ca81c-119">Add levels to the compensation structure</span></span>
1. <span data-ttu-id="ca81c-120">Klikněte na možnost Struktura kompenzací.</span><span class="sxs-lookup"><span data-stu-id="ca81c-120">Click Compensation structure.</span></span>
2. <span data-ttu-id="ca81c-121">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="ca81c-121">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="ca81c-122">V poli Úroveň zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ca81c-122">In the Level field, enter or select a value.</span></span>
4. <span data-ttu-id="ca81c-123">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="ca81c-123">Click New.</span></span>
5. <span data-ttu-id="ca81c-124">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="ca81c-124">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="ca81c-125">V poli Úroveň zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ca81c-125">In the Level field, enter or select a value.</span></span>
7. <span data-ttu-id="ca81c-126">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="ca81c-126">Click New.</span></span>
8. <span data-ttu-id="ca81c-127">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="ca81c-127">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="ca81c-128">V poli Úroveň zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ca81c-128">In the Level field, enter or select a value.</span></span>
10. <span data-ttu-id="ca81c-129">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="ca81c-129">Click New.</span></span>
11. <span data-ttu-id="ca81c-130">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="ca81c-130">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="ca81c-131">V poli Úroveň zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ca81c-131">In the Level field, enter or select a value.</span></span>
13. <span data-ttu-id="ca81c-132">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="ca81c-132">Click New.</span></span>
14. <span data-ttu-id="ca81c-133">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="ca81c-133">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="ca81c-134">V poli Úroveň zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ca81c-134">In the Level field, enter or select a value.</span></span>

## <a name="fill-in-the-compensation-structure-with-values"></a><span data-ttu-id="ca81c-135">Vyplňte hodnoty do kompenzační struktury</span><span class="sxs-lookup"><span data-stu-id="ca81c-135">Fill in the compensation structure with values</span></span>
1. <span data-ttu-id="ca81c-136">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="ca81c-136">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="ca81c-137">V tomto okamžiku lze zadat ručně náhradní hodnoty do každého pole tabulky, nebo lze použít funkci hromadné změny ke snadnému vyplnění více polí a provádění základních výpočtů.</span><span class="sxs-lookup"><span data-stu-id="ca81c-137">At this point, compensation values can manually be entered into each field in the table, or the Mass change functionality can be used to easily fill in multiple fields and perform basic calculations.</span></span>  
2. <span data-ttu-id="ca81c-138">Klikněte na Hromadná změna.</span><span class="sxs-lookup"><span data-stu-id="ca81c-138">Click Mass change.</span></span>
    * <span data-ttu-id="ca81c-139">U této tabulky nejprve použijeme hodnotu pro středový bod první úrovně ke všem polím v tabulce.</span><span class="sxs-lookup"><span data-stu-id="ca81c-139">For this grid, we'll first apply the value for the midpoint of the first level's to all the fields in the table.</span></span> <span data-ttu-id="ca81c-140">To bude základem pro kompenzační matici.</span><span class="sxs-lookup"><span data-stu-id="ca81c-140">This will be the basis for the compensation matrix.</span></span>  
3. <span data-ttu-id="ca81c-141">V poli Typ úprav vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="ca81c-141">In the Adjustment type field, select an option.</span></span>
4. <span data-ttu-id="ca81c-142">Zadejte číslo do pole Částka úpravy.</span><span class="sxs-lookup"><span data-stu-id="ca81c-142">In the Adjustment amount field, enter a number.</span></span>
5. <span data-ttu-id="ca81c-143">V seznamu označte všechny řádky nebo jejich označení zrušte.</span><span class="sxs-lookup"><span data-stu-id="ca81c-143">In the list, mark or unmark all rows.</span></span>
6. <span data-ttu-id="ca81c-144">Klikněte na Použít na mřížku.</span><span class="sxs-lookup"><span data-stu-id="ca81c-144">Click Apply to grid.</span></span>
    * <span data-ttu-id="ca81c-145">Nyní použijeme funkci hromadné změny ke zvýšení částek v jednotlivých úrovních určitým procentem nebo částkou.</span><span class="sxs-lookup"><span data-stu-id="ca81c-145">Now we'll use the mass change function to increment the amounts in each subsequent level by a certain percentage or amount.</span></span> <span data-ttu-id="ca81c-146">V tomto příkladu bude mít každá třída rozšíření 12,5 % mezi jejich středními body.</span><span class="sxs-lookup"><span data-stu-id="ca81c-146">In this example, each grade will have a 12.5% spread between their midpoints.</span></span>  
7. <span data-ttu-id="ca81c-147">V poli Typ úprav vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="ca81c-147">In the Adjustment type field, select an option.</span></span>
8. <span data-ttu-id="ca81c-148">Zadejte číslo do pole Částka úpravy.</span><span class="sxs-lookup"><span data-stu-id="ca81c-148">In the Adjustment amount field, enter a number.</span></span>
9. <span data-ttu-id="ca81c-149">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="ca81c-149">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="ca81c-150">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="ca81c-150">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="ca81c-151">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="ca81c-151">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="ca81c-152">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="ca81c-152">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="ca81c-153">Klikněte na Použít na mřížku.</span><span class="sxs-lookup"><span data-stu-id="ca81c-153">Click Apply to grid.</span></span>
14. <span data-ttu-id="ca81c-154">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="ca81c-154">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="ca81c-155">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="ca81c-155">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="ca81c-156">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="ca81c-156">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="ca81c-157">Klikněte na Použít na mřížku.</span><span class="sxs-lookup"><span data-stu-id="ca81c-157">Click Apply to grid.</span></span>
18. <span data-ttu-id="ca81c-158">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="ca81c-158">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="ca81c-159">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="ca81c-159">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="ca81c-160">Klikněte na Použít na mřížku.</span><span class="sxs-lookup"><span data-stu-id="ca81c-160">Click Apply to grid.</span></span>
21. <span data-ttu-id="ca81c-161">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="ca81c-161">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="ca81c-162">Klikněte na Použít na mřížku.</span><span class="sxs-lookup"><span data-stu-id="ca81c-162">Click Apply to grid.</span></span>
    * <span data-ttu-id="ca81c-163">Nyní použijeme funkci hromadné změny pro úpravu minimálních a maximálních referenčních bodů pro každou úroveň.</span><span class="sxs-lookup"><span data-stu-id="ca81c-163">Now we'll use the mass change function to adjust the Minimum and Maximum reference points for each level.</span></span> <span data-ttu-id="ca81c-164">V tomto příkladu použijeme 50% rozložení, takže minimální referenční bod bude upraven na hodnotou -20 % a maximum bude upraveno na +20 %.</span><span class="sxs-lookup"><span data-stu-id="ca81c-164">This example will use a 50% spread so the Minimum reference point will be adjusted -20% and the Maximum will be adjusted +20%.</span></span>  
23. <span data-ttu-id="ca81c-165">Zadejte číslo do pole Částka úpravy.</span><span class="sxs-lookup"><span data-stu-id="ca81c-165">In the Adjustment amount field, enter a number.</span></span>
24. <span data-ttu-id="ca81c-166">V poli Referenční bod zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ca81c-166">In the Reference point field, enter or select a value.</span></span>
25. <span data-ttu-id="ca81c-167">V seznamu označte všechny řádky nebo jejich označení zrušte.</span><span class="sxs-lookup"><span data-stu-id="ca81c-167">In the list, mark or unmark all rows.</span></span>
26. <span data-ttu-id="ca81c-168">Klikněte na Použít na mřížku.</span><span class="sxs-lookup"><span data-stu-id="ca81c-168">Click Apply to grid.</span></span>
27. <span data-ttu-id="ca81c-169">Zadejte číslo do pole Částka úpravy.</span><span class="sxs-lookup"><span data-stu-id="ca81c-169">In the Adjustment amount field, enter a number.</span></span>
28. <span data-ttu-id="ca81c-170">V poli Referenční bod zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ca81c-170">In the Reference point field, enter or select a value.</span></span>
29. <span data-ttu-id="ca81c-171">V seznamu označte všechny řádky nebo jejich označení zrušte.</span><span class="sxs-lookup"><span data-stu-id="ca81c-171">In the list, mark or unmark all rows.</span></span>
30. <span data-ttu-id="ca81c-172">Klikněte na Použít na mřížku.</span><span class="sxs-lookup"><span data-stu-id="ca81c-172">Click Apply to grid.</span></span>


