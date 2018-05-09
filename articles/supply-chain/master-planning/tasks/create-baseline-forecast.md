--- 
title: "Vytvoření základní prognózy"
description: "Plánovač výroby může vytvořit základní prognózu pomocí modelů prognózování časových řad nebo zkopírováním historické poptávky."
author: YuyuScheller
manager: AnnBe
ms.date: 111/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: bd3cf1118d848fe4f95ec92bee3f5d1abe3d3a7c
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-baseline-forecast"></a><span data-ttu-id="282c6-103">Vytvoření základní prognózy</span><span class="sxs-lookup"><span data-stu-id="282c6-103">Create a baseline forecast</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="282c6-104">Plánovač výroby může vytvořit základní prognózu pomocí modelů prognózování časových řad nebo zkopírováním historické poptávky.</span><span class="sxs-lookup"><span data-stu-id="282c6-104">A production planner can create a baseline forecast either by using time series forecast models or by copying the historical demand.</span></span> <span data-ttu-id="282c6-105">Tento postup popisuje, jak zkopírováním historické poptávky vytvořit základní prognózu pro všechny produkty použitím jednoho alokačního klíče položky.</span><span class="sxs-lookup"><span data-stu-id="282c6-105">This procedure shows how to copy the historical demand to create a baseline forecast for all products using one item allocation key.</span></span> 


## <a name="set-up-an-item-allocation-key"></a><span data-ttu-id="282c6-106">Nastavení alokačního klíče</span><span class="sxs-lookup"><span data-stu-id="282c6-106">Set up an item allocation key</span></span>
1. <span data-ttu-id="282c6-107">Přejděte na Hlavní plánování > Nastavení > Skupiny mezipodnikového plánování.</span><span class="sxs-lookup"><span data-stu-id="282c6-107">Go to Master planning > Setup > Intercompany planning groups.</span></span>
2. <span data-ttu-id="282c6-108">Použijte rychlý filtr pro hledání záznamů.</span><span class="sxs-lookup"><span data-stu-id="282c6-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="282c6-109">Můžete například filtrovat v poli Jméno pomocí hodnoty „10“.</span><span class="sxs-lookup"><span data-stu-id="282c6-109">For example, filter on the Name field with a value of '10'.</span></span>
    * <span data-ttu-id="282c6-110">Prognóza poptávky se provádí mezi právnickými osobami.</span><span class="sxs-lookup"><span data-stu-id="282c6-110">Demand forecasting runs across legal entities.</span></span> <span data-ttu-id="282c6-111">Proto je nutné nastavit všechny společnosti, pro které chcete vygenerovat prognózy v jedné skupině mezipodnikového plánování.</span><span class="sxs-lookup"><span data-stu-id="282c6-111">That's why you need to set up all the companies for which you want to generate forecasts in one intercompany planning group.</span></span>  
3. <span data-ttu-id="282c6-112">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="282c6-112">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="282c6-113">Klikněte na Alokační klíče položek.</span><span class="sxs-lookup"><span data-stu-id="282c6-113">Click Item allocation keys.</span></span>
    * <span data-ttu-id="282c6-114">Vyberte všechny alokační klíče položky, pro které chcete vytvořit prognózy.</span><span class="sxs-lookup"><span data-stu-id="282c6-114">Select all the item allocation keys for which you want to create forecasts.</span></span>  
5. <span data-ttu-id="282c6-115">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="282c6-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="282c6-116">Vyberte alokační klíč položky D_Aloc.</span><span class="sxs-lookup"><span data-stu-id="282c6-116">Select D_Aloc item allocation key.</span></span>  
6. <span data-ttu-id="282c6-117">Klepněte na >.</span><span class="sxs-lookup"><span data-stu-id="282c6-117">Click >.</span></span>
7. <span data-ttu-id="282c6-118">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="282c6-118">Close the page.</span></span>
8. <span data-ttu-id="282c6-119">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="282c6-119">Close the page.</span></span>

## <a name="set-up-the-demand-forecasting-parameters"></a><span data-ttu-id="282c6-120">Nastavení parametrů prognózy poptávky</span><span class="sxs-lookup"><span data-stu-id="282c6-120">Set up the demand forecasting parameters</span></span>
1. <span data-ttu-id="282c6-121">Přejděte na Hlavní plánování > Nastavení > Prognóza poptávky > Parametry tvorby prognóz poptávky.</span><span class="sxs-lookup"><span data-stu-id="282c6-121">Go to Master planning > Setup > Demand forecasting > Demand forecasting parameters.</span></span>
2. <span data-ttu-id="282c6-122">Rozbalte část Parametry algoritmu prognózy.</span><span class="sxs-lookup"><span data-stu-id="282c6-122">Expand the Forecast algorithm parameters section.</span></span>
3. <span data-ttu-id="282c6-123">V poli Strategie generování prognózy vyberte "Kopírování mezi historickými poptávkami".</span><span class="sxs-lookup"><span data-stu-id="282c6-123">In the Forecast generation strategy field, select 'Copy over historical demand'.</span></span>
4. <span data-ttu-id="282c6-124">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="282c6-124">Click Save.</span></span>

## <a name="create-a-baseline-forecast"></a><span data-ttu-id="282c6-125">Vytvoření základní prognózy</span><span class="sxs-lookup"><span data-stu-id="282c6-125">Create a baseline forecast</span></span>
1. <span data-ttu-id="282c6-126">Přejděte na Hlavní plánování > Prognózování > Prognóza poptávky > Generovat statistickou základní prognózu.</span><span class="sxs-lookup"><span data-stu-id="282c6-126">Go to Master planning > Forecasting > Demand forecasting > Generate statistical baseline forecast.</span></span>
2. <span data-ttu-id="282c6-127">Zadejte datum do pole Od data.</span><span class="sxs-lookup"><span data-stu-id="282c6-127">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="282c6-128">Pokud prodejní objednávky začínají od 1. ledna 2015, zadejte toto datum.</span><span class="sxs-lookup"><span data-stu-id="282c6-128">If you have sales orders starting from January 1, 2015, enter this date.</span></span> <span data-ttu-id="282c6-129">V opačném případě zadejte nejdřívější datum prodejních objednávek.</span><span class="sxs-lookup"><span data-stu-id="282c6-129">If you don't, enter the earliest date of your sales orders.</span></span>  
3. <span data-ttu-id="282c6-130">Do pole Do data zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="282c6-130">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="282c6-131">Zadejte poslední datum prodejních objednávek (např. '2015-03-31').</span><span class="sxs-lookup"><span data-stu-id="282c6-131">Enter the last date of your sales orders, for example '2015-03-31'.</span></span>  
4. <span data-ttu-id="282c6-132">Zadejte datum do pole Od data.</span><span class="sxs-lookup"><span data-stu-id="282c6-132">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="282c6-133">Zadejte '2015-04-01'.</span><span class="sxs-lookup"><span data-stu-id="282c6-133">Enter '2015-04-01'.</span></span> <span data-ttu-id="282c6-134">Toto datum se vypočítá automaticky jako počáteční datum následujícího intervalu prognózy.</span><span class="sxs-lookup"><span data-stu-id="282c6-134">This date will be automatically calculated as the start date of the next forecasting bucket.</span></span>  
5. <span data-ttu-id="282c6-135">Rozbalte oddíl Záznamy k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="282c6-135">Expand the Records to include section.</span></span>
6. <span data-ttu-id="282c6-136">Klepněte na tlačítko Filtr.</span><span class="sxs-lookup"><span data-stu-id="282c6-136">Click Filter.</span></span>
7. <span data-ttu-id="282c6-137">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="282c6-137">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="282c6-138">Označte řádek, kde pole = skupina mezipodnikového plánování.</span><span class="sxs-lookup"><span data-stu-id="282c6-138">Mark the row where Field = Intercompany planning group.</span></span>  
8. <span data-ttu-id="282c6-139">Zadejte hodnotu do pole Kritéria.</span><span class="sxs-lookup"><span data-stu-id="282c6-139">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="282c6-140">Zadejte skupinu vnitropodnikového plánování, například „10“, kterou používáte v prvním úkolu.</span><span class="sxs-lookup"><span data-stu-id="282c6-140">Type the intercompany planning group, for example, 10, that you used in the first task.</span></span>  
9. <span data-ttu-id="282c6-141">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="282c6-141">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="282c6-142">Vyberte řádek, kde pole = alokační klíč položky.</span><span class="sxs-lookup"><span data-stu-id="282c6-142">Select the row where Field = Item allocation key.</span></span>  
10. <span data-ttu-id="282c6-143">Zadejte hodnotu do pole Kritéria.</span><span class="sxs-lookup"><span data-stu-id="282c6-143">In the Criteria field, type a value.</span></span>
11. <span data-ttu-id="282c6-144">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="282c6-144">Click OK.</span></span>
12. <span data-ttu-id="282c6-145">Rozbalte sekci Rozšířené parametry.</span><span class="sxs-lookup"><span data-stu-id="282c6-145">Expand the Advanced parameters section.</span></span>
13. <span data-ttu-id="282c6-146">V poli Interval prognózy vyberte Měsíc.</span><span class="sxs-lookup"><span data-stu-id="282c6-146">In the Forecast bucket field, select 'Month'.</span></span>
14. <span data-ttu-id="282c6-147">V poli Horizont prognózy zadejte „3“.</span><span class="sxs-lookup"><span data-stu-id="282c6-147">In the Forecast horizon field, enter '3'.</span></span>
15. <span data-ttu-id="282c6-148">V poli Ochranná doba zablokování zadejte číslo 1.</span><span class="sxs-lookup"><span data-stu-id="282c6-148">In the Freeze time fence field, enter '1'.</span></span>
16. <span data-ttu-id="282c6-149">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="282c6-149">Click OK.</span></span>

## <a name="visualize-the-demand-forecast"></a><span data-ttu-id="282c6-150">Vizualizace prognózy poptávky</span><span class="sxs-lookup"><span data-stu-id="282c6-150">Visualize the demand forecast</span></span>
1. <span data-ttu-id="282c6-151">Přejděte na Hlavní plánování > Prognózování > Prognóza poptávky > Upravená prognóza poptávky.</span><span class="sxs-lookup"><span data-stu-id="282c6-151">Go to Master planning > Forecasting > Demand forecasting > Adjusted demand forecast.</span></span>
2. <span data-ttu-id="282c6-152">V tabulce agregovaného zobrazení vyberte buňku na řádku 1, ve sloupci 2.</span><span class="sxs-lookup"><span data-stu-id="282c6-152">In the aggregated view table, select the cell in row 1, column 2.</span></span> <span data-ttu-id="282c6-153">Jedná se o druhé měsíc, pro který jste vytvořili prognózu.</span><span class="sxs-lookup"><span data-stu-id="282c6-153">This is the second month for which you have created forecast.</span></span>
3. <span data-ttu-id="282c6-154">Nastavte QtyCell na '400'.</span><span class="sxs-lookup"><span data-stu-id="282c6-154">Set QtyCell to '400'.</span></span>
    * <span data-ttu-id="282c6-155">V buňce zadejte jiné číslo než to, který bylo předvídáno, například 400.</span><span class="sxs-lookup"><span data-stu-id="282c6-155">In the cell, enter a different number than the one that was forecasted, for example, 400.</span></span>  
4. <span data-ttu-id="282c6-156">Právě jste provedli ruční úpravu prognózy.</span><span class="sxs-lookup"><span data-stu-id="282c6-156">You have made a manual adjustment to the forecast.</span></span> <span data-ttu-id="282c6-157">Všimněte si grafické indikace v dalším kroku.</span><span class="sxs-lookup"><span data-stu-id="282c6-157">Notice the graphical indication in the next step.</span></span>
5. <span data-ttu-id="282c6-158">Klikněte na Podrobnosti o řádcích prognózy.</span><span class="sxs-lookup"><span data-stu-id="282c6-158">Click Forecast line details.</span></span>
    * <span data-ttu-id="282c6-159">Na této stránce můžete zobrazit hodnoty přesnosti, historické poptávky a prognózu.</span><span class="sxs-lookup"><span data-stu-id="282c6-159">On this page, you can see the accuracy values, historical demand, and forecast.</span></span> <span data-ttu-id="282c6-160">Podle potřeby můžete upravit také prognózu.</span><span class="sxs-lookup"><span data-stu-id="282c6-160">You can make changes to the forecast as well.</span></span>  


