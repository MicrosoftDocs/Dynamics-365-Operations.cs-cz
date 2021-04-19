---
title: Výpočet návrhů kanbanového množství
description: Tento postup se zaměřuje na optimalizaci velikosti a množství kanbanu u konkrétních kanbanových pravidel pomocí výpočtu kanbanového množství.
author: ChristianRytt
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 93845129e057b8729e676123967efefb6bca66f2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829323"
---
# <a name="calculate-kanban-quantity-suggestions"></a><span data-ttu-id="eaba9-103">Výpočet návrhů kanbanového množství</span><span class="sxs-lookup"><span data-stu-id="eaba9-103">Calculate kanban quantity suggestions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="eaba9-104">Tento postup se zaměřuje na optimalizaci velikosti a množství kanbanu u konkrétních kanbanových pravidel pomocí výpočtu kanbanového množství.</span><span class="sxs-lookup"><span data-stu-id="eaba9-104">This procedure focuses on optimizing the kanban size and quantities for a specific kanban rule by using the kanban quantity calculation.</span></span> <span data-ttu-id="eaba9-105">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="eaba9-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="eaba9-106">Tento postup je určen pro vedoucího hodnotového proudu.</span><span class="sxs-lookup"><span data-stu-id="eaba9-106">This procedure is intended for the value stream manager.</span></span> <span data-ttu-id="eaba9-107">Je nutné, abyste dokončili postup Přidání zásad výpočtu kanbanového množství ke kanbanovému pravidlu.</span><span class="sxs-lookup"><span data-stu-id="eaba9-107">It is a prerequisite that you have completed the procedure Add a new kanban quantity calculation policy to a kanban rule.</span></span>


## <a name="create-a-kanban-quantity-calculation"></a><span data-ttu-id="eaba9-108">Vytvoření výpočtu kanbanového množství</span><span class="sxs-lookup"><span data-stu-id="eaba9-108">Create a kanban quantity calculation</span></span>
1. <span data-ttu-id="eaba9-109">Přejít na Řízení výroby > Pravidelné úlohy > Výpočet kanbanového množství > Vypočítat kanbanové množství.</span><span class="sxs-lookup"><span data-stu-id="eaba9-109">Go to Production control > Periodic tasks > Kanban quantity calculation > Calculate kanban quantity.</span></span>
2. <span data-ttu-id="eaba9-110">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="eaba9-110">Click New.</span></span>
3. <span data-ttu-id="eaba9-111">Zadejte Speaker2016 do pole Název.</span><span class="sxs-lookup"><span data-stu-id="eaba9-111">In the Name field, type 'Speaker2016'.</span></span>
4. <span data-ttu-id="eaba9-112">V poli Název kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="eaba9-112">In the Name field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="eaba9-113">Vyberte pravidlo, které jste vytvořili v postupu Přidání zásad výpočtu kanbanového množství ke kanbanovému pravidlu.</span><span class="sxs-lookup"><span data-stu-id="eaba9-113">Select the policy that you have created in the procedure Add a new kanban quantity calculation policy to a kanban rule.</span></span> <span data-ttu-id="eaba9-114">Například Speaker2016.</span><span class="sxs-lookup"><span data-stu-id="eaba9-114">For example, Speaker2016.</span></span>  
5. <span data-ttu-id="eaba9-115">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="eaba9-115">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="eaba9-116">V poli Pravidlo aktivní ode dne nastavte datum a čas na 2012-12-17T08:00:00.</span><span class="sxs-lookup"><span data-stu-id="eaba9-116">In the Rule active as of date field, set the date and time to '2012-12-17T08:00:00'.</span></span>
    * <span data-ttu-id="eaba9-117">Toto datum slouží jako základ pro určení pevných kanbanových pravidel, která jsou zahrnuta do výpočtu kanbanového množství.</span><span class="sxs-lookup"><span data-stu-id="eaba9-117">This date serves as the basis for determining which fixed kanban rules are included in the kanban quantity calculation.</span></span>  
7. <span data-ttu-id="eaba9-118">Do pole Datum začátku období splněné poptávky nastavte datum a čas na 2012-11-17T09:00:00.</span><span class="sxs-lookup"><span data-stu-id="eaba9-118">In the Fulfilled demand period start date field, set the date and time to '2012-11-17T09:00:00'.</span></span>
    * <span data-ttu-id="eaba9-119">Počáteční datum zahrnutí dřívějších transakcí poptávky pro výpočet kanbanového množství.</span><span class="sxs-lookup"><span data-stu-id="eaba9-119">The date from when past demand transactions are included to calculate the kanban quantity.</span></span>  
8. <span data-ttu-id="eaba9-120">Do pole Datum konce období splněné poptávky nastavte datum a čas na 2012-12-17T07:59:59.</span><span class="sxs-lookup"><span data-stu-id="eaba9-120">In the Fulfilled demand period end date field, set the date and time to '2012-12-17T07:59:59'.</span></span>
    * <span data-ttu-id="eaba9-121">Koncové datum zahrnutí dřívějších transakcí poptávky pro výpočet kanbanového množství.</span><span class="sxs-lookup"><span data-stu-id="eaba9-121">The date until when past demand transactions are included to calculate the kanban quantity.</span></span>  
9. <span data-ttu-id="eaba9-122">Do pole Datum začátku období poptávky nastavte datum a čas na 2012-12-17T08:00:00.</span><span class="sxs-lookup"><span data-stu-id="eaba9-122">In the Demand period start date field, set the date and time to '2012-12-17T08:00:00'.</span></span>
    * <span data-ttu-id="eaba9-123">Počáteční datum zahrnutí aktuálních transakcí poptávky pro výpočet kanbanového množství.</span><span class="sxs-lookup"><span data-stu-id="eaba9-123">The date from when current demand transactions are included to calculate the kanban quantity.</span></span>  
10. <span data-ttu-id="eaba9-124">Do pole Datum konce období poptávky nastavte datum a čas na 2013-01-16T07:59:59.</span><span class="sxs-lookup"><span data-stu-id="eaba9-124">In the Demand period end date field, set the date and time to '2013-01-16T07:59:59'.</span></span>
    * <span data-ttu-id="eaba9-125">Koncové datum zahrnutí aktuálních transakcí poptávky pro výpočet kanbanového množství.</span><span class="sxs-lookup"><span data-stu-id="eaba9-125">The date until when current demand transactions are included to calculate the kanban quantity.</span></span>  

## <a name="generate-kanban-quantity-proposal"></a><span data-ttu-id="eaba9-126">Generování návrhu kanbanového množství</span><span class="sxs-lookup"><span data-stu-id="eaba9-126">Generate kanban quantity proposal</span></span>
1. <span data-ttu-id="eaba9-127">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="eaba9-127">Click Save.</span></span>
2. <span data-ttu-id="eaba9-128">Klepněte na tlačítko Generovat.</span><span class="sxs-lookup"><span data-stu-id="eaba9-128">Click Generate.</span></span>
    * <span data-ttu-id="eaba9-129">Tímto vytvoříte řádek návrhu kanbanového množství pro kanbanové pravidlo 000020.</span><span class="sxs-lookup"><span data-stu-id="eaba9-129">This generates a kanban quantity proposal line for the kanban rule 000020.</span></span>  

## <a name="run-kanban-quantity-calculation"></a><span data-ttu-id="eaba9-130">Spuštění výpočtu kanbanového množství</span><span class="sxs-lookup"><span data-stu-id="eaba9-130">Run kanban quantity calculation</span></span>
1. <span data-ttu-id="eaba9-131">Klikněte na tlačítko Vypočítat.</span><span class="sxs-lookup"><span data-stu-id="eaba9-131">Click Calculate.</span></span>
    * <span data-ttu-id="eaba9-132">Tímto vypočítáte návrh kanbanového množství.</span><span class="sxs-lookup"><span data-stu-id="eaba9-132">This calculates the kanban quantity proposal.</span></span>  
2. <span data-ttu-id="eaba9-133">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="eaba9-133">Click OK.</span></span>
3. <span data-ttu-id="eaba9-134">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="eaba9-134">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="eaba9-135">Všimněte si, že navrhované kanbanové množství je „2“.</span><span class="sxs-lookup"><span data-stu-id="eaba9-135">Notice the suggested kanban quantity is 2.</span></span>  

## <a name="change-product-quantity-and-calculate-again"></a><span data-ttu-id="eaba9-136">Změna množství produktu a opětovné provedení výpočtu</span><span class="sxs-lookup"><span data-stu-id="eaba9-136">Change product quantity and calculate again</span></span>
1. <span data-ttu-id="eaba9-137">Nastavte Celkové množství produktu na 5.</span><span class="sxs-lookup"><span data-stu-id="eaba9-137">Set Product quantity to '5'.</span></span>
2. <span data-ttu-id="eaba9-138">Klikněte na tlačítko Vypočítat.</span><span class="sxs-lookup"><span data-stu-id="eaba9-138">Click Calculate.</span></span>
3. <span data-ttu-id="eaba9-139">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="eaba9-139">Click OK.</span></span>
    * <span data-ttu-id="eaba9-140">Všimněte si, že s kanbanovým množstvím „5“ se návrh změní na kanbanové množství „4“.</span><span class="sxs-lookup"><span data-stu-id="eaba9-140">Notice that with a kanban quantity of 5, the suggestion is changed to a kanban quantity of 4.</span></span>  
    * <span data-ttu-id="eaba9-141">Důvodem je skutečnost, že se sníženým množstvím produktu je zapotřebí více kanbanu ke splnění požadavku.</span><span class="sxs-lookup"><span data-stu-id="eaba9-141">This is caused by the fact that with a lower product quantity, we need more kanbans to fulfill the demand.</span></span>  

## <a name="update-kanban-rule"></a><span data-ttu-id="eaba9-142">Aktualizace kanbanového pravidla</span><span class="sxs-lookup"><span data-stu-id="eaba9-142">Update kanban rule</span></span>
1. <span data-ttu-id="eaba9-143">Do pole Datum účinnosti pravidla zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="eaba9-143">In the Rule effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="eaba9-144">Nastavte Pravidlo aktivní ode dne na datum v budoucnosti.</span><span class="sxs-lookup"><span data-stu-id="eaba9-144">Set the 'Rule active as of date' to a date in the future.</span></span> <span data-ttu-id="eaba9-145">Například dnes + jeden rok.</span><span class="sxs-lookup"><span data-stu-id="eaba9-145">For example, today + one year.</span></span>  
2. <span data-ttu-id="eaba9-146">Klepněte na položku Aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="eaba9-146">Click Update.</span></span>
3. <span data-ttu-id="eaba9-147">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="eaba9-147">Click OK.</span></span>
4. <span data-ttu-id="eaba9-148">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="eaba9-148">Close the page.</span></span>

## <a name="validate-change-on-kanban-rule"></a><span data-ttu-id="eaba9-149">Ověření změny v kanbanovém pravidle</span><span class="sxs-lookup"><span data-stu-id="eaba9-149">Validate change on kanban rule</span></span>
1. <span data-ttu-id="eaba9-150">Přejděte k Řízení informací o produktech > Lean manufacturing > Kanbanová pravidla.</span><span class="sxs-lookup"><span data-stu-id="eaba9-150">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="eaba9-151">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="eaba9-151">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="eaba9-152">Vyberte kanbanové pravidlo vytvořené v předchozím podúkolu.</span><span class="sxs-lookup"><span data-stu-id="eaba9-152">Select the kanban rule that was created in the previous sub-task.</span></span> <span data-ttu-id="eaba9-153">Toto by mělo být první kanbanové pravidlo v seznamu roztříděném podle čísla.</span><span class="sxs-lookup"><span data-stu-id="eaba9-153">This should be the first kanban rule in the list sorted by number.</span></span>  
3. <span data-ttu-id="eaba9-154">Přepněte rozšíření oddílu Podrobnosti.</span><span class="sxs-lookup"><span data-stu-id="eaba9-154">Toggle the expansion of the Details section.</span></span>
    * <span data-ttu-id="eaba9-155">Všimněte si data platnosti, které znamená, že toto pravidlo není až do tohoto data aktivováno.</span><span class="sxs-lookup"><span data-stu-id="eaba9-155">Notice the effective date, which means that this rule is not activated until this date.</span></span>  
4. <span data-ttu-id="eaba9-156">Přepněte rozšíření oddílu Množství.</span><span class="sxs-lookup"><span data-stu-id="eaba9-156">Toggle the expansion of the Quantities section.</span></span>
    * <span data-ttu-id="eaba9-157">Všimněte si, že se jedná o výchozí množství, které jste zadali ve výpočtu kanbanového množství.</span><span class="sxs-lookup"><span data-stu-id="eaba9-157">Notice this is the default quantity that you entered on the kanban quantity calculation.</span></span>  
    * <span data-ttu-id="eaba9-158">Všimněte si, že se že jedná o pevné kanbanové množství „4“ z výpočtu kanbanového množství.</span><span class="sxs-lookup"><span data-stu-id="eaba9-158">Notice this is the fixed kanban quantity of 4 from the kanban quantity calculation.</span></span>  
5. <span data-ttu-id="eaba9-159">Klikněte na kartu Panel seznamu.</span><span class="sxs-lookup"><span data-stu-id="eaba9-159">Click the ListPanel tab.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]