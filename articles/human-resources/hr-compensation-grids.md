---
title: Nastavit kompenzační mřížky
description: Kompenzační mřížky umožňují definovat a spravovat struktury plateb pro plány fixní kompenzace.
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRCCompGrid, HRCCompGridView, HcmCompensationWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c393dc3393b5331b5594e39254ffe208ff439bc7
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800944"
---
# <a name="set-up-compensation-grids"></a><span data-ttu-id="43c25-103">Nastavit kompenzační mřížky</span><span class="sxs-lookup"><span data-stu-id="43c25-103">Set up compensation grids</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="43c25-104">Kompenzační mřížky umožňují definovat a spravovat struktury plateb pro plány fixní kompenzace.</span><span class="sxs-lookup"><span data-stu-id="43c25-104">Compensation grids are used to define and maintain the pay structures for fixed compensation plans.</span></span> <span data-ttu-id="43c25-105">Kompenzační mřížky můžete sdílet mezi několika plány nebo zkopírovat při vytvoření nového plánu kompenzace.</span><span class="sxs-lookup"><span data-stu-id="43c25-105">Compensation grids can be shared between multiple plans or copied when creating a new compensation plan.</span></span>  <span data-ttu-id="43c25-106">Před vytvořením kompenzační mřížky, je nutné nastavit úrovně a referenční body.</span><span class="sxs-lookup"><span data-stu-id="43c25-106">Before creating a compensation grid, Levels and Reference points must be set up.</span></span> <span data-ttu-id="43c25-107">V tomto příkladu vytvoříme nový typ třídy kompenzační mřížky pomocí ukázkových dat pro úrovně a referenční body.</span><span class="sxs-lookup"><span data-stu-id="43c25-107">This example will create a new Grade type of compensation grid using demo data for the Levels and Reference points.</span></span> <span data-ttu-id="43c25-108">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="43c25-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-information-about-the-compensation-grid"></a><span data-ttu-id="43c25-109">Nastavit informace o kompenzační mřížce</span><span class="sxs-lookup"><span data-stu-id="43c25-109">Set up information about the compensation grid</span></span>
1. <span data-ttu-id="43c25-110">Přejděte do nabídky Lidské zdroje > Kompenzace > Fixní kompenzace > Kompenzační mřížky.</span><span class="sxs-lookup"><span data-stu-id="43c25-110">Go to Human resources > Compensation > Fixed compensation > Compensation grids.</span></span>
2. <span data-ttu-id="43c25-111">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="43c25-111">Click New.</span></span>
3. <span data-ttu-id="43c25-112">Zadejte hodnotu do pole Mřížka.</span><span class="sxs-lookup"><span data-stu-id="43c25-112">In the Grid field, type a value.</span></span>
4. <span data-ttu-id="43c25-113">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="43c25-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="43c25-114">Vyberte volbu v poli Typ.</span><span class="sxs-lookup"><span data-stu-id="43c25-114">In the Type field, select an option.</span></span>
6. <span data-ttu-id="43c25-115">V poli Nastavení reference zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="43c25-115">In the Reference setup field, enter or select a value.</span></span>
7. <span data-ttu-id="43c25-116">V poli Měna zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="43c25-116">In the Currency field, enter or select a value.</span></span>
8. <span data-ttu-id="43c25-117">Zadejte hodnotu do pole Měna.</span><span class="sxs-lookup"><span data-stu-id="43c25-117">In the Currency field, type a value.</span></span>
9. <span data-ttu-id="43c25-118">Zadejte datum do pole Datum platnosti.</span><span class="sxs-lookup"><span data-stu-id="43c25-118">In the Effective date field, enter a date.</span></span>

## <a name="add-levels-to-the-compensation-structure"></a><span data-ttu-id="43c25-119">Přidání úrovní do kompenzační struktury</span><span class="sxs-lookup"><span data-stu-id="43c25-119">Add levels to the compensation structure</span></span>
1. <span data-ttu-id="43c25-120">Klikněte na možnost Struktura kompenzací.</span><span class="sxs-lookup"><span data-stu-id="43c25-120">Click Compensation structure.</span></span>
2. <span data-ttu-id="43c25-121">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="43c25-121">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="43c25-122">V poli Úroveň zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="43c25-122">In the Level field, enter or select a value.</span></span>
4. <span data-ttu-id="43c25-123">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="43c25-123">Click New.</span></span>
5. <span data-ttu-id="43c25-124">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="43c25-124">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="43c25-125">V poli Úroveň zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="43c25-125">In the Level field, enter or select a value.</span></span>
7. <span data-ttu-id="43c25-126">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="43c25-126">Click New.</span></span>
8. <span data-ttu-id="43c25-127">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="43c25-127">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="43c25-128">V poli Úroveň zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="43c25-128">In the Level field, enter or select a value.</span></span>
10. <span data-ttu-id="43c25-129">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="43c25-129">Click New.</span></span>
11. <span data-ttu-id="43c25-130">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="43c25-130">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="43c25-131">V poli Úroveň zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="43c25-131">In the Level field, enter or select a value.</span></span>
13. <span data-ttu-id="43c25-132">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="43c25-132">Click New.</span></span>
14. <span data-ttu-id="43c25-133">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="43c25-133">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="43c25-134">V poli Úroveň zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="43c25-134">In the Level field, enter or select a value.</span></span>

## <a name="fill-in-the-compensation-structure-with-values"></a><span data-ttu-id="43c25-135">Vyplňte hodnoty do kompenzační struktury</span><span class="sxs-lookup"><span data-stu-id="43c25-135">Fill in the compensation structure with values</span></span>
1. <span data-ttu-id="43c25-136">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="43c25-136">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="43c25-137">V tomto okamžiku lze zadat ručně náhradní hodnoty do každého pole tabulky, nebo lze použít funkci hromadné změny ke snadnému vyplnění více polí a provádění základních výpočtů.</span><span class="sxs-lookup"><span data-stu-id="43c25-137">At this point, compensation values can manually be entered into each field in the table, or the Mass change functionality can be used to easily fill in multiple fields and perform basic calculations.</span></span>  
2. <span data-ttu-id="43c25-138">Klikněte na Hromadná změna.</span><span class="sxs-lookup"><span data-stu-id="43c25-138">Click Mass change.</span></span>
    * <span data-ttu-id="43c25-139">U této tabulky nejprve použijeme hodnotu pro středový bod první úrovně ke všem polím v tabulce.</span><span class="sxs-lookup"><span data-stu-id="43c25-139">For this grid, we'll first apply the value for the midpoint of the first level's to all the fields in the table.</span></span> <span data-ttu-id="43c25-140">To bude základem pro kompenzační matici.</span><span class="sxs-lookup"><span data-stu-id="43c25-140">This will be the basis for the compensation matrix.</span></span>  
3. <span data-ttu-id="43c25-141">V poli Typ úprav vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="43c25-141">In the Adjustment type field, select an option.</span></span>
4. <span data-ttu-id="43c25-142">Zadejte číslo do pole Částka úpravy.</span><span class="sxs-lookup"><span data-stu-id="43c25-142">In the Adjustment amount field, enter a number.</span></span>
5. <span data-ttu-id="43c25-143">V seznamu označte všechny řádky nebo jejich označení zrušte.</span><span class="sxs-lookup"><span data-stu-id="43c25-143">In the list, mark or unmark all rows.</span></span>
6. <span data-ttu-id="43c25-144">Klikněte na Použít na mřížku.</span><span class="sxs-lookup"><span data-stu-id="43c25-144">Click Apply to grid.</span></span>
    * <span data-ttu-id="43c25-145">Nyní použijeme funkci hromadné změny ke zvýšení částek v jednotlivých úrovních určitým procentem nebo částkou.</span><span class="sxs-lookup"><span data-stu-id="43c25-145">Now we'll use the mass change function to increment the amounts in each subsequent level by a certain percentage or amount.</span></span> <span data-ttu-id="43c25-146">V tomto příkladu bude mít každá třída rozšíření 12,5 % mezi jejich středními body.</span><span class="sxs-lookup"><span data-stu-id="43c25-146">In this example, each grade will have a 12.5% spread between their midpoints.</span></span>  
7. <span data-ttu-id="43c25-147">V poli Typ úprav vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="43c25-147">In the Adjustment type field, select an option.</span></span>
8. <span data-ttu-id="43c25-148">Zadejte číslo do pole Částka úpravy.</span><span class="sxs-lookup"><span data-stu-id="43c25-148">In the Adjustment amount field, enter a number.</span></span>
9. <span data-ttu-id="43c25-149">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="43c25-149">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="43c25-150">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="43c25-150">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="43c25-151">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="43c25-151">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="43c25-152">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="43c25-152">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="43c25-153">Klikněte na Použít na mřížku.</span><span class="sxs-lookup"><span data-stu-id="43c25-153">Click Apply to grid.</span></span>
14. <span data-ttu-id="43c25-154">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="43c25-154">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="43c25-155">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="43c25-155">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="43c25-156">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="43c25-156">In the list, find and select the desired record.</span></span>
17. <span data-ttu-id="43c25-157">Klikněte na Použít na mřížku.</span><span class="sxs-lookup"><span data-stu-id="43c25-157">Click Apply to grid.</span></span>
18. <span data-ttu-id="43c25-158">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="43c25-158">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="43c25-159">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="43c25-159">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="43c25-160">Klikněte na Použít na mřížku.</span><span class="sxs-lookup"><span data-stu-id="43c25-160">Click Apply to grid.</span></span>
21. <span data-ttu-id="43c25-161">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="43c25-161">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="43c25-162">Klikněte na Použít na mřížku.</span><span class="sxs-lookup"><span data-stu-id="43c25-162">Click Apply to grid.</span></span>
    * <span data-ttu-id="43c25-163">Nyní použijeme funkci hromadné změny pro úpravu minimálních a maximálních referenčních bodů pro každou úroveň.</span><span class="sxs-lookup"><span data-stu-id="43c25-163">Now we'll use the mass change function to adjust the Minimum and Maximum reference points for each level.</span></span> <span data-ttu-id="43c25-164">V tomto příkladu použijeme 50% rozložení, takže minimální referenční bod bude upraven na hodnotou -20 % a maximum bude upraveno na +20 %.</span><span class="sxs-lookup"><span data-stu-id="43c25-164">This example will use a 50% spread so the Minimum reference point will be adjusted -20% and the Maximum will be adjusted +20%.</span></span>  
23. <span data-ttu-id="43c25-165">Zadejte číslo do pole Částka úpravy.</span><span class="sxs-lookup"><span data-stu-id="43c25-165">In the Adjustment amount field, enter a number.</span></span>
24. <span data-ttu-id="43c25-166">V poli Referenční bod zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="43c25-166">In the Reference point field, enter or select a value.</span></span>
25. <span data-ttu-id="43c25-167">V seznamu označte všechny řádky nebo jejich označení zrušte.</span><span class="sxs-lookup"><span data-stu-id="43c25-167">In the list, mark or unmark all rows.</span></span>
26. <span data-ttu-id="43c25-168">Klikněte na Použít na mřížku.</span><span class="sxs-lookup"><span data-stu-id="43c25-168">Click Apply to grid.</span></span>
27. <span data-ttu-id="43c25-169">Zadejte číslo do pole Částka úpravy.</span><span class="sxs-lookup"><span data-stu-id="43c25-169">In the Adjustment amount field, enter a number.</span></span>
28. <span data-ttu-id="43c25-170">V poli Referenční bod zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="43c25-170">In the Reference point field, enter or select a value.</span></span>
29. <span data-ttu-id="43c25-171">V seznamu označte všechny řádky nebo jejich označení zrušte.</span><span class="sxs-lookup"><span data-stu-id="43c25-171">In the list, mark or unmark all rows.</span></span>
30. <span data-ttu-id="43c25-172">Klikněte na Použít na mřížku.</span><span class="sxs-lookup"><span data-stu-id="43c25-172">Click Apply to grid.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]