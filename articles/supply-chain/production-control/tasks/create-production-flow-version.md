--- 
title: "Vytvoření verze výrobního toku"
description: "Tento postup se zaměřuje na vytvoření nové verze výrobního toku."
author: cvocph
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 58b3c9cd265b97a814541315e4ba8378010eb2b2
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-production-flow-version"></a><span data-ttu-id="75ff2-103">Vytvoření verze výrobního toku</span><span class="sxs-lookup"><span data-stu-id="75ff2-103">Create a production flow version</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="75ff2-104">Tento postup se zaměřuje na vytvoření nové verze výrobního toku.</span><span class="sxs-lookup"><span data-stu-id="75ff2-104">This procedure focuses on creating a new production flow version.</span></span> <span data-ttu-id="75ff2-105">Pro tuto proceduru musí být definovány výrobní parametry pro Lean manufacturing a jednotky měření pro čas třídy.</span><span class="sxs-lookup"><span data-stu-id="75ff2-105">For this procedure, the production parameters for lean manufacturing and the units of measurement for class time must be defined.</span></span> <span data-ttu-id="75ff2-106">Je třeba také definovat hodnotový proud a skupinu výroby.</span><span class="sxs-lookup"><span data-stu-id="75ff2-106">You also need to define a value stream and a production group.</span></span> <span data-ttu-id="75ff2-107">Další informace o výrobních tocích a aktivitách v lean manufacturingu naleznete v dokumentech white paper pro Lean manufacturing aplikace Microsoft Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="75ff2-107">To learn more about production flows and activities in lean manufacturing, see the white papers on Lean manufacturing for Microsoft Dynamics AX.</span></span> <span data-ttu-id="75ff2-108">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="75ff2-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-production-flow"></a><span data-ttu-id="75ff2-109">Vytvoření výrobního toku</span><span class="sxs-lookup"><span data-stu-id="75ff2-109">Create a production flow</span></span>
1. <span data-ttu-id="75ff2-110">Přejděte na Řízení výroby > Nastavení > Tok štíhlé výroby > Výrobního toky.</span><span class="sxs-lookup"><span data-stu-id="75ff2-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="75ff2-111">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="75ff2-111">Click New.</span></span>
3. <span data-ttu-id="75ff2-112">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="75ff2-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="75ff2-113">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="75ff2-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="75ff2-114">V poli Název kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="75ff2-114">In the Name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="75ff2-115">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="75ff2-115">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="75ff2-116">Vyberte provozní jednotku typu hodnotového proudu.</span><span class="sxs-lookup"><span data-stu-id="75ff2-116">Select an operating unit of type value stream.</span></span> <span data-ttu-id="75ff2-117">Hodnotový proud je provozní jednotka, která pokrývá všechny aktivity a toky hodnotového proudu.</span><span class="sxs-lookup"><span data-stu-id="75ff2-117">A value stream is an operating unit that spans all activities and flows of the value stream.</span></span> <span data-ttu-id="75ff2-118">V této fázi provozní jednotky jsou omezeny právnickou osobou a nemají žádné další funkce.</span><span class="sxs-lookup"><span data-stu-id="75ff2-118">At this stage, operating units are limited to a legal entity and have no further functionality.</span></span>  
7. <span data-ttu-id="75ff2-119">V poli Výrobní skupina klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="75ff2-119">In the Production group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="75ff2-120">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="75ff2-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="75ff2-121">Vyberte skupinu výroby pro výrobní tok.</span><span class="sxs-lookup"><span data-stu-id="75ff2-121">Select a production group for the production flow.</span></span> <span data-ttu-id="75ff2-122">Výrobní skupiny umožňují definici materiálu, práce, a účtů nedokončené výroby pro výrobní proces.</span><span class="sxs-lookup"><span data-stu-id="75ff2-122">Production groups allow the definition of material, labour, and WIP accounts for a production process.</span></span> <span data-ttu-id="75ff2-123">Pro přidružení kontextu účetnictví k výrobnímu toku je nutné vybrat výrobní skupinu.</span><span class="sxs-lookup"><span data-stu-id="75ff2-123">To associate the accounting context to a production flow, a production group must be selected.</span></span>  
9. <span data-ttu-id="75ff2-124">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="75ff2-124">Click Save.</span></span>

## <a name="create-a-production-flow-version"></a><span data-ttu-id="75ff2-125">Vytvoření verze výrobního toku</span><span class="sxs-lookup"><span data-stu-id="75ff2-125">Create a production flow version</span></span>
1. <span data-ttu-id="75ff2-126">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="75ff2-126">Click Add.</span></span>
2. <span data-ttu-id="75ff2-127">Do pole Datum vypršení platnosti zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="75ff2-127">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="75ff2-128">V případě potřeby definujte Datum vypršení platnosti pro verzi.</span><span class="sxs-lookup"><span data-stu-id="75ff2-128">If required, define an Expiration date for the version.</span></span> <span data-ttu-id="75ff2-129">Můžete ho kdykoli aktualizovat, a to dokonce i pro aktivní verze.</span><span class="sxs-lookup"><span data-stu-id="75ff2-129">You can update it at any given time, even for active versions.</span></span> <span data-ttu-id="75ff2-130">Můžete ho využít pro plánování verze mimo fázi.</span><span class="sxs-lookup"><span data-stu-id="75ff2-130">You can use it to plan to phase out a version.</span></span>  
3. <span data-ttu-id="75ff2-131">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="75ff2-131">Click OK.</span></span>
4. <span data-ttu-id="75ff2-132">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="75ff2-132">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="75ff2-133">Zadejte hodnotu do pole Jednotka.</span><span class="sxs-lookup"><span data-stu-id="75ff2-133">In the Unit field, type a value.</span></span>
6. <span data-ttu-id="75ff2-134">Vyřešit změny jednotky taktu.</span><span class="sxs-lookup"><span data-stu-id="75ff2-134">ResolveChanges the Takt unit.</span></span>
7. <span data-ttu-id="75ff2-135">Do pole Průměrná doba výrobního taktu zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="75ff2-135">In the Average takt time field, enter a number.</span></span>
    * <span data-ttu-id="75ff2-136">Definujte Průměrnou délku výrobního taktu verze.</span><span class="sxs-lookup"><span data-stu-id="75ff2-136">Define the Average takt time of the version.</span></span> <span data-ttu-id="75ff2-137">Definujte cílovou průměrnou délku výrobního taktu pro ovládání taktu verze výrobního toku.</span><span class="sxs-lookup"><span data-stu-id="75ff2-137">For the takt control of the production flow version, define a targeted average takt time.</span></span> <span data-ttu-id="75ff2-138">Takt je definován jako množství za časové období.</span><span class="sxs-lookup"><span data-stu-id="75ff2-138">The takt is defined as quantity per time period.</span></span> <span data-ttu-id="75ff2-139">V tomto příkladu je délka výrobního taktu 0,2 hodin na 10 kusů.</span><span class="sxs-lookup"><span data-stu-id="75ff2-139">In the example, the takt time is 0.2 hours per 10 pieces.</span></span> <span data-ttu-id="75ff2-140">8hodinová pracovní doba odpovídá denní kapacitě prostupnosti 400 kusů.</span><span class="sxs-lookup"><span data-stu-id="75ff2-140">For a working time of 8 hours, this corresponds to a daily throughput capacity of 400 pieces.</span></span>  
8. <span data-ttu-id="75ff2-141">V poli Množství na cyklus zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="75ff2-141">In the Quantity per cycle field, enter a number.</span></span>
    * <span data-ttu-id="75ff2-142">Určete množství za cyklus ve vztahu k průměrné délce výrobního taktu.</span><span class="sxs-lookup"><span data-stu-id="75ff2-142">Define the quantity per cycle related to the Average takt time.</span></span>  
9. <span data-ttu-id="75ff2-143">Přepněte rozšíření oddílu Podrobnosti verze.</span><span class="sxs-lookup"><span data-stu-id="75ff2-143">Toggle the expansion of the Version details section.</span></span>
10. <span data-ttu-id="75ff2-144">Do pole Minimální doba výrobního taktu zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="75ff2-144">In the Minimum takt time field, enter a number.</span></span>
    * <span data-ttu-id="75ff2-145">Určete minimální délku výrobního taktu.</span><span class="sxs-lookup"><span data-stu-id="75ff2-145">Define the minimum takt time.</span></span> <span data-ttu-id="75ff2-146">Minimální délka výrobního taktu musí být menší nebo rovna průměrné délce výrobního taktu.</span><span class="sxs-lookup"><span data-stu-id="75ff2-146">The minimum takt time must be less than or equal to the average takt time.</span></span>  
11. <span data-ttu-id="75ff2-147">Do pole Maximální doba výrobního taktu zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="75ff2-147">In the Maximum takt time field, enter a number.</span></span>
    * <span data-ttu-id="75ff2-148">Maximální délka výrobního taktu musí být vyšší nebo rovna průměrné délce výrobního taktu.</span><span class="sxs-lookup"><span data-stu-id="75ff2-148">The maximum takt time must be higher than or equal to the Average takt time.</span></span>  
12. <span data-ttu-id="75ff2-149">Do pole Období skutečného času cyklu (dny) zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="75ff2-149">In the Period for actual cycle time (days) field, enter a number.</span></span>
    * <span data-ttu-id="75ff2-150">Zadejte počet dní v období skutečného času cyklu.</span><span class="sxs-lookup"><span data-stu-id="75ff2-150">Enter the number of days in the Period for actual cycle time.</span></span> <span data-ttu-id="75ff2-151">Období skutečného času cyklu je počet dnů, jejichž úlohy jsou zpětně seskupeny od aktuální minuty pro výpočet skutečného času cyklu.</span><span class="sxs-lookup"><span data-stu-id="75ff2-151">The period for actual cycle time is the number of days that jobs are aggregated from the actual minute backwards to calculate the actual cycle time.</span></span> <span data-ttu-id="75ff2-152">Hodnota může být změněna kdykoli a je použita pouze pro výpočet skutečného času cyklu.</span><span class="sxs-lookup"><span data-stu-id="75ff2-152">The value can be changed at any time and is only used for the calculation of the actual cycle times.</span></span>  
13. <span data-ttu-id="75ff2-153">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="75ff2-153">Click Save.</span></span>


