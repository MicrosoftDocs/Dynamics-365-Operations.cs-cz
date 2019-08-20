---
title: Ověření výrobního toku a verze
description: Tato procedura popisuje postup při vytvoření nového výrobního toku a první verze pro lean manufacturing.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 523f6414ec212aef48eece487f4199ea2cf4b87e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836137"
---
# <a name="validate-a-production-flow-and-version"></a><span data-ttu-id="87ba8-103">Ověření výrobního toku a verze</span><span class="sxs-lookup"><span data-stu-id="87ba8-103">Validate a production flow and version</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="87ba8-104">Tato procedura popisuje postup při vytvoření nového výrobního toku a první verze pro lean manufacturing.</span><span class="sxs-lookup"><span data-stu-id="87ba8-104">This procedure shows how to create a new production flow and a first version for lean manufacturing.</span></span> <span data-ttu-id="87ba8-105">Předpoklady: Musí být definovány výrobní parametry pro Lean manufacturing a jednotky měření pro čas třídy.</span><span class="sxs-lookup"><span data-stu-id="87ba8-105">Prerequisites: The production parameters for Lean manufacturing and the units of measure for class time must be defined.</span></span> <span data-ttu-id="87ba8-106">Je třeba definovat hodnotový proud a skupinu výroby.</span><span class="sxs-lookup"><span data-stu-id="87ba8-106">You need to define a Value stream and a Production group.</span></span> <span data-ttu-id="87ba8-107">S koncepty výrobních toků a aktivitami se seznámíte v dokumentaci o Lean manufacturingu.</span><span class="sxs-lookup"><span data-stu-id="87ba8-107">Refer to the white papers on Lean manufacturing to familiarize yourself with the concepts of production flows and activities.</span></span> <span data-ttu-id="87ba8-108">Tato procedura se vztahuje k právnické osobě USMF v ukázkových datech.</span><span class="sxs-lookup"><span data-stu-id="87ba8-108">This procedure refers to the legal entity USMF in demo data.</span></span> <span data-ttu-id="87ba8-109">Avšak mohou být použity jiní právnické osoby za předpokladu, že právnická osoba je nakonfigurována pro Lean manufacturing.</span><span class="sxs-lookup"><span data-stu-id="87ba8-109">However, assuming that the legal entity is configured for Lean manufacturing, other legal entities can be used.</span></span>


## <a name="create-a-production-flow"></a><span data-ttu-id="87ba8-110">Vytvoření výrobního toku</span><span class="sxs-lookup"><span data-stu-id="87ba8-110">Create a production flow</span></span>
1. <span data-ttu-id="87ba8-111">Přejděte na Řízení výroby > Nastavení > Tok štíhlé výroby > Výrobního toky.</span><span class="sxs-lookup"><span data-stu-id="87ba8-111">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="87ba8-112">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="87ba8-112">Click New.</span></span>
3. <span data-ttu-id="87ba8-113">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="87ba8-113">In the Name field, type a value.</span></span>
4. <span data-ttu-id="87ba8-114">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="87ba8-114">In the Description field, type a value.</span></span>
5. <span data-ttu-id="87ba8-115">V poli Název kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="87ba8-115">In the Name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="87ba8-116">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="87ba8-116">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="87ba8-117">Hodnotový proud je provozní jednotka, která pokrývá všechny aktivity a toky hodnotového proudu.</span><span class="sxs-lookup"><span data-stu-id="87ba8-117">A value stream is an operating unit that spans over all activities and flows of the value stream.</span></span>   <span data-ttu-id="87ba8-118">V této fázi provozní jednotky jsou omezeny právnickou osobou a nemají žádné další funkce.</span><span class="sxs-lookup"><span data-stu-id="87ba8-118">At this stage, operating units are limited to a legal entity and have no further functionality.</span></span>  
7. <span data-ttu-id="87ba8-119">V poli Výrobní skupina klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="87ba8-119">In the Production group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="87ba8-120">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="87ba8-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="87ba8-121">Výrobní skupiny umožňují definici materiálu, práce, a účtů nedokončené výroby pro výrobní proces.</span><span class="sxs-lookup"><span data-stu-id="87ba8-121">Production groups allow the definition of material, labor, and WIP accounts for a production process.</span></span> <span data-ttu-id="87ba8-122">Pro přidružení kontextu účetnictví k výrobnímu toku je nutné vybrat výrobní skupinu.</span><span class="sxs-lookup"><span data-stu-id="87ba8-122">To associate the accounting context to a production flow, a production group must be selected.</span></span>  
9. <span data-ttu-id="87ba8-123">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="87ba8-123">Click Save.</span></span>

## <a name="create-a-production-flow-version"></a><span data-ttu-id="87ba8-124">Vytvoření verze výrobního toku</span><span class="sxs-lookup"><span data-stu-id="87ba8-124">Create a production flow version</span></span>
1. <span data-ttu-id="87ba8-125">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="87ba8-125">Click Add.</span></span>
2. <span data-ttu-id="87ba8-126">Do pole Datum vypršení platnosti zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="87ba8-126">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="87ba8-127">Datum vypršení platnosti verze lze v každém okamžiku aktualizovat, a to dokonce i aktivní verze.</span><span class="sxs-lookup"><span data-stu-id="87ba8-127">You can update the Expiration date of the version at any given time, even for active versions.</span></span> <span data-ttu-id="87ba8-128">Využijte vypršení platnosti verze k plánování fáze mimo verzi.</span><span class="sxs-lookup"><span data-stu-id="87ba8-128">Use the expiration of the version to plan for a phase out of a version.</span></span>  
3. <span data-ttu-id="87ba8-129">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="87ba8-129">Click OK.</span></span>
4. <span data-ttu-id="87ba8-130">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="87ba8-130">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="87ba8-131">Zadejte hodnotu do pole Jednotka.</span><span class="sxs-lookup"><span data-stu-id="87ba8-131">In the Unit field, type a value.</span></span>
6. <span data-ttu-id="87ba8-132">Vyberte Jednotku taktu.</span><span class="sxs-lookup"><span data-stu-id="87ba8-132">Select the Takt unit.</span></span>
7. <span data-ttu-id="87ba8-133">Do pole Průměrná doba výrobního taktu zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="87ba8-133">In the Average takt time field, enter a number.</span></span>
    * <span data-ttu-id="87ba8-134">Definujte cílovou průměrnou délku výrobního taktu pro ovládání taktu verze výrobního toku.</span><span class="sxs-lookup"><span data-stu-id="87ba8-134">For the takt control of the production flow version, define a targeted average takt time.</span></span>   <span data-ttu-id="87ba8-135">Takt je definován jako množství za časové období.</span><span class="sxs-lookup"><span data-stu-id="87ba8-135">The takt is defined as quantity  per time period.</span></span>  <span data-ttu-id="87ba8-136">V tomto příkladu je délka výrobního taktu 0,2 hodin na 10 kusů.</span><span class="sxs-lookup"><span data-stu-id="87ba8-136">In the given example, the takt time is 0.2 hours per 10 pieces.</span></span> <span data-ttu-id="87ba8-137">8hodinová pracovní doba odpovídá denní kapacitě prostupnosti 400 kusů.</span><span class="sxs-lookup"><span data-stu-id="87ba8-137">For a working time of 8 hours, this corresponds to a daily throughput capacity of 400 pieces.</span></span>  
8. <span data-ttu-id="87ba8-138">V poli Množství na cyklus zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="87ba8-138">In the Quantity per cycle field, enter a number.</span></span>
9. <span data-ttu-id="87ba8-139">Rozbalte nebo sbalte oddíl Podrobnosti verze.</span><span class="sxs-lookup"><span data-stu-id="87ba8-139">Expand or collapse the Version details section.</span></span>
10. <span data-ttu-id="87ba8-140">Do pole Minimální doba výrobního taktu zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="87ba8-140">In the Minimum takt time field, enter a number.</span></span>
    * <span data-ttu-id="87ba8-141">Minimální délka výrobního taktu musí být menší nebo rovna průměrné délce výrobního taktu.</span><span class="sxs-lookup"><span data-stu-id="87ba8-141">The minimum takt time must be less than or equal to the average takt time.</span></span>  
11. <span data-ttu-id="87ba8-142">Do pole Maximální doba výrobního taktu zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="87ba8-142">In the Maximum takt time field, enter a number.</span></span>
    * <span data-ttu-id="87ba8-143">Maximální délka výrobního taktu musí být vyšší nebo rovna průměrné délce výrobního taktu.</span><span class="sxs-lookup"><span data-stu-id="87ba8-143">The maximum takt time must be higher than or equal to the Average takt time.</span></span>  
12. <span data-ttu-id="87ba8-144">Zadejte počet dní v období skutečného času cyklu</span><span class="sxs-lookup"><span data-stu-id="87ba8-144">Enter a number of days in the Period for actual cycle time</span></span>
    * <span data-ttu-id="87ba8-145">Období skutečného času cyklu je počet dnů, jejichž úlohy jsou zpětně seskupeny od aktuální minuty pro výpočet skutečného času cyklu.</span><span class="sxs-lookup"><span data-stu-id="87ba8-145">The period for actual cycle time is the number of days that jobs are aggregated from the actual minute backwards to calculate the actual cycle time.</span></span> <span data-ttu-id="87ba8-146">Hodnota může být změněna kdykoli a je použita pouze pro výpočet skutečného času cyklu.</span><span class="sxs-lookup"><span data-stu-id="87ba8-146">The value can be changed at any time and is only used for the calculation of the actual cycle times.</span></span>  
13. <span data-ttu-id="87ba8-147">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="87ba8-147">Click Save.</span></span>

