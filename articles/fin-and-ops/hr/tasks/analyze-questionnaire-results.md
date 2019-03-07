---
title: Analýza výsledků dotazníku
description: Statistiky dotazníku slouží k výpočtu průměrné hodnoty, součtů a procentuální hodnoty na základě demografických údajů.
author: ShielaSogge
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMQuestionnaireStatistics, KMQuestionnaireStatisticsLine
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a70ea145d8c7134a32e8f0fc6980daca9a010bb0
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "332741"
---
# <a name="analyzing-questionnaire-results"></a><span data-ttu-id="836c4-103">Analýza výsledků dotazníku</span><span class="sxs-lookup"><span data-stu-id="836c4-103">Analyzing questionnaire results</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="836c4-104">Statistiky dotazníku slouží k výpočtu průměrné hodnoty, součtů a procentuální hodnoty na základě demografických údajů.</span><span class="sxs-lookup"><span data-stu-id="836c4-104">Questionnaire statistics can be used to calculate averages, totals, and percentages based on a set of demographic data.</span></span> <span data-ttu-id="836c4-105">Chcete-li celý postup spustit, přejděte na Dotazník > Zobrazit a analyzovat výsledky > Statistiky dotazníků.</span><span class="sxs-lookup"><span data-stu-id="836c4-105">To begin this procedure, go to Questionnaire > View and analyze results > Questionnaire statistics.</span></span> <span data-ttu-id="836c4-106">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="836c4-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-questionnaire-statistics-record"></a><span data-ttu-id="836c4-107">Vytvoření záznamu statistik pro dotazník</span><span class="sxs-lookup"><span data-stu-id="836c4-107">Create a Questionnaire statistics record</span></span>
1. <span data-ttu-id="836c4-108">Přejděte na Statistika dotazníků.</span><span class="sxs-lookup"><span data-stu-id="836c4-108">Go to Questionnaire statistics.</span></span>
2. <span data-ttu-id="836c4-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="836c4-109">Click New.</span></span>
3. <span data-ttu-id="836c4-110">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="836c4-110">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="836c4-111">Zadejte hodnotu do pole Statistika.</span><span class="sxs-lookup"><span data-stu-id="836c4-111">In the Statistics field, type a value.</span></span>
5. <span data-ttu-id="836c4-112">Zadejte hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="836c4-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="836c4-113">V poli Dotazník kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="836c4-113">In the Questionnaire field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="836c4-114">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="836c4-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="836c4-115">Klikněte na záložku Obecné.</span><span class="sxs-lookup"><span data-stu-id="836c4-115">Click the General tab.</span></span>
    * <span data-ttu-id="836c4-116">Vyberte, zda chcete zahrnout anonymní výsledky nebo výsledky pracovníků, kontaktů a uchazečů.</span><span class="sxs-lookup"><span data-stu-id="836c4-116">Select if you want to include anonymous results or results from workers, contacts, and applicants.</span></span>  
9. <span data-ttu-id="836c4-117">Zaškrtněte políčko Pracovník nebo jeho zaškrtnutí zrušte.</span><span class="sxs-lookup"><span data-stu-id="836c4-117">Select or clear the Worker check box.</span></span>
    * <span data-ttu-id="836c4-118">Pokud budete výsledky prohlížet podle služebního věku nebo věku, zadejte intervaly, které chcete používat k seskupování výsledků.</span><span class="sxs-lookup"><span data-stu-id="836c4-118">If you will be viewing the results by seniority or age, specify the intervals that you would like to use for grouping the results.</span></span>  
    * <span data-ttu-id="836c4-119">Zadáním 5 pro věkový interval způsobíte seskupení výsledků na základě věkového intervalu pěti let.</span><span class="sxs-lookup"><span data-stu-id="836c4-119">Entering a 5 for the age interval will group the results based on five-year age intervals.</span></span>  
10. <span data-ttu-id="836c4-120">V poli Věk zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="836c4-120">In the Age field, enter a number.</span></span>
    * <span data-ttu-id="836c4-121">Vyberte, zda chcete spustit výpočet v rámci celého dotazníku, pro každou skupinu výsledků, pro každou otázku nebo pro každý řádek dotazů.</span><span class="sxs-lookup"><span data-stu-id="836c4-121">Select if you want to run the calculation against the entire questionnaire, for each result group, for each question, or for each question row.</span></span>  
    * <span data-ttu-id="836c4-122">Vyberte, jak si přejete seskupit výsledky.</span><span class="sxs-lookup"><span data-stu-id="836c4-122">Select how you would like to group the results.</span></span>  
    * <span data-ttu-id="836c4-123">Například při výpočtu průměrných bodů za otázku můžete zobrazit otázky, které jsou seskupeny podle hodnoty Skupina výsledků.</span><span class="sxs-lookup"><span data-stu-id="836c4-123">For example, if you calculate the average points per question, you may want to see the questions grouped by Result group.</span></span>  
    * <span data-ttu-id="836c4-124">Vyberte data, na kterých chcete založit výpočet.</span><span class="sxs-lookup"><span data-stu-id="836c4-124">Select the data to base the calculation on.</span></span>  
    * <span data-ttu-id="836c4-125">Pokud například chcete zobrazit průměrné získané procento v dotazníku mezi pracovníci ve srovnání s průměrným počtem bodů obdržených vašimi pracovníky.</span><span class="sxs-lookup"><span data-stu-id="836c4-125">For example, if you want to see the average percent received on the questionnaire across your workers versus the average number of points achieved across your workers.</span></span>  
11. <span data-ttu-id="836c4-126">Klikněte na kartu Rozsah.</span><span class="sxs-lookup"><span data-stu-id="836c4-126">Click the Range tab.</span></span>
    * <span data-ttu-id="836c4-127">Používejte rozsahy pro omezení sady výsledků pouze na ty, které splňují kritéria rozsahu.</span><span class="sxs-lookup"><span data-stu-id="836c4-127">Use ranges to limit your result set to only those meeting the Range criteria.</span></span>  
12. <span data-ttu-id="836c4-128">Klikněte na kartu Seskupení podle.</span><span class="sxs-lookup"><span data-stu-id="836c4-128">Click the Grouping by tab.</span></span>
    * <span data-ttu-id="836c4-129">Seskupení slouží k určení toho, jak mají být výsledky zobrazeny.</span><span class="sxs-lookup"><span data-stu-id="836c4-129">Use Groupings to determine how the results should be displayed.</span></span>  
    * <span data-ttu-id="836c4-130">Například můžete seskupit výsledky podle pohlaví a pak podle věku.</span><span class="sxs-lookup"><span data-stu-id="836c4-130">For example, group the results first by gender, then by age.</span></span>  
13. <span data-ttu-id="836c4-131">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="836c4-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="836c4-132">Přesuňte seskupení do vybrané strany a umístěte je požadovaným způsobem.</span><span class="sxs-lookup"><span data-stu-id="836c4-132">Move the groupings into the Selected side and place them in the desired order.</span></span>  

## <a name="execute-the-statistics-calculation"></a><span data-ttu-id="836c4-133">Provedení výpočtu statistik</span><span class="sxs-lookup"><span data-stu-id="836c4-133">Execute the statistics calculation</span></span>
1. <span data-ttu-id="836c4-134">Klikněte na tlačítko Spustit.</span><span class="sxs-lookup"><span data-stu-id="836c4-134">Click Execute.</span></span>
    * <span data-ttu-id="836c4-135">Vyberte funkce výpočtu, které chcete provést u výsledků.</span><span class="sxs-lookup"><span data-stu-id="836c4-135">Select which calculation function you would like to perform on the results.</span></span>  
    * <span data-ttu-id="836c4-136">Můžete například vytvořit výpočet procentuálního průměru v rámci dotazníku pro vybraná seskupení, nebo celkové body v rámci skupiny výsledků pro vybraná seskupení.</span><span class="sxs-lookup"><span data-stu-id="836c4-136">For example, calculate the average percentages across the questionnaire for the selected groupings or total the points across the result groups for the selected groupings.</span></span>  
2. <span data-ttu-id="836c4-137">Zaškrtněte nebo zrušte zaškrtnutí políčka Odstranit předchozí výběry.</span><span class="sxs-lookup"><span data-stu-id="836c4-137">Select or clear the Delete previous searches check box.</span></span>
3. <span data-ttu-id="836c4-138">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="836c4-138">Click OK.</span></span>

## <a name="view-the-results-of-the-questionnaire-statistics-run"></a><span data-ttu-id="836c4-139">Zobrazte výsledky provedené statistiky dotazníku.</span><span class="sxs-lookup"><span data-stu-id="836c4-139">View the results of the questionnaire statistics run.</span></span>
1. <span data-ttu-id="836c4-140">Klikněte na možnost Výsledky.</span><span class="sxs-lookup"><span data-stu-id="836c4-140">Click Result.</span></span>
2. <span data-ttu-id="836c4-141">Klikněte na možnost Výsledky.</span><span class="sxs-lookup"><span data-stu-id="836c4-141">Click Result.</span></span>
3. <span data-ttu-id="836c4-142">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="836c4-142">Close the page.</span></span>

