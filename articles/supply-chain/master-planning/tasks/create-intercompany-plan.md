--- 
title: "Vytvoření mezipodnikového plánu"
description: "Tato procedura ukazuje, jak vytvořit mezipodnikový plán."
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: da186f7ad74bb607fd6e7220d77c2f414789f29c
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="create-an-intercompany-plan"></a><span data-ttu-id="074ed-103">Vytvoření mezipodnikového plánu</span><span class="sxs-lookup"><span data-stu-id="074ed-103">Create an intercompany plan</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="074ed-104">Tato procedura ukazuje, jak vytvořit mezipodnikový plán.</span><span class="sxs-lookup"><span data-stu-id="074ed-104">This procedure shows how to create an intercompany plan.</span></span> <span data-ttu-id="074ed-105">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="074ed-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-an-intercompany-planning-group"></a><span data-ttu-id="074ed-106">Nastavení skupiny mezipodnikového plánování</span><span class="sxs-lookup"><span data-stu-id="074ed-106">Set up an intercompany planning group</span></span> 
1. <span data-ttu-id="074ed-107">Přejděte na Skupiny mezipodnikového plánování.</span><span class="sxs-lookup"><span data-stu-id="074ed-107">Go to Intercompany planning groups.</span></span>
    * <span data-ttu-id="074ed-108">Hlavní plánování > Nastavení > Skupiny mezipodnikového plánování</span><span class="sxs-lookup"><span data-stu-id="074ed-108">Master planning > Setup > Intercompany planning groups</span></span>  
2. <span data-ttu-id="074ed-109">Použijte rychlý filtr pro hledání záznamů.</span><span class="sxs-lookup"><span data-stu-id="074ed-109">Use the Quick Filter to find records.</span></span> <span data-ttu-id="074ed-110">Můžete například filtrovat v poli Jméno pomocí hodnoty „10“.</span><span class="sxs-lookup"><span data-stu-id="074ed-110">For example, filter on the Name field with a value of '10'.</span></span>
3. <span data-ttu-id="074ed-111">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="074ed-111">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="074ed-112">Klepněte na tlačítko Odstranit.</span><span class="sxs-lookup"><span data-stu-id="074ed-112">Click Delete.</span></span>
    * <span data-ttu-id="074ed-113">Tento krok je nezbytný pro účely zkrácení mezipodnikového plánování.</span><span class="sxs-lookup"><span data-stu-id="074ed-113">This step is necessary in order to shorten the intercompany planning run.</span></span>   <span data-ttu-id="074ed-114">Mezipodnikové plánování spustí hlavní plánování ve všech společnostech ve skupině plánování, počínaje nejnižší sekvencí plánování.</span><span class="sxs-lookup"><span data-stu-id="074ed-114">Intercompany planning will run master planning in all the companies in a planning group, starting from the lowest scheduling sequence.</span></span>  
5. <span data-ttu-id="074ed-115">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="074ed-115">Click Yes.</span></span>
6. <span data-ttu-id="074ed-116">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="074ed-116">Close the page.</span></span>

## <a name="create-an-intercompany-plan"></a><span data-ttu-id="074ed-117">Vytvoření mezipodnikového plánu</span><span class="sxs-lookup"><span data-stu-id="074ed-117">Create an intercompany plan</span></span>
1. <span data-ttu-id="074ed-118">Klikněte na Mezipodnikové hlavní plánování.</span><span class="sxs-lookup"><span data-stu-id="074ed-118">Click Intercompany master planning.</span></span>
    * <span data-ttu-id="074ed-119">Jedná se o pracovní prostor hlavního plánování.</span><span class="sxs-lookup"><span data-stu-id="074ed-119">This is on the Master planning workspace.</span></span>  
2. <span data-ttu-id="074ed-120">V poli Skupina mezipodnikového plánování kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="074ed-120">In the Intercompany planning group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="074ed-121">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="074ed-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="074ed-122">Vyberte skupinu 10 mezipodnikového plánování.</span><span class="sxs-lookup"><span data-stu-id="074ed-122">Select intercompany planning group 10.</span></span>  
4. <span data-ttu-id="074ed-123">V poli Počet iterací mezipodnikového plánování zadejte 2.</span><span class="sxs-lookup"><span data-stu-id="074ed-123">In the Number of intercompany planning iterations field, enter '2'.</span></span>
    * <span data-ttu-id="074ed-124">Skupina 10 mezipodnikového plánování má dva členy.</span><span class="sxs-lookup"><span data-stu-id="074ed-124">Intercompany planning group 10 has two members.</span></span> <span data-ttu-id="074ed-125">K rozšíření propagace zpoždění ze zdrojové společnosti (USMF) vůči společnosti zákazníka (DEMF) je třeba spustit dvakrát mezipodnikové plánování v obou společnostech dvakrát.</span><span class="sxs-lookup"><span data-stu-id="074ed-125">In order to propagate the delays from the source company (USMF) to the customer company (DEMF), you will need to run intercompany in both companies two times.</span></span> <span data-ttu-id="074ed-126">První iterace bude rozšiřovat poptávku a identifikovat zpoždění ve zdrojové společnosti (USMF).</span><span class="sxs-lookup"><span data-stu-id="074ed-126">The first iteration will propagate the demand and identify the delays in the source company (USMF).</span></span> <span data-ttu-id="074ed-127">Druhá iterace rozšíří zpoždění z USMF na DEMF.</span><span class="sxs-lookup"><span data-stu-id="074ed-127">The second iteration will propagate the delays from USMF to DEMF.</span></span>  
5. <span data-ttu-id="074ed-128">Vyberte volbu v poli První iterace.</span><span class="sxs-lookup"><span data-stu-id="074ed-128">In the First iteration field, select an option.</span></span>
6. <span data-ttu-id="074ed-129">V poli První iterace vyberte Obnovení.</span><span class="sxs-lookup"><span data-stu-id="074ed-129">In the First iteration field, select 'Regeneration'.</span></span>
7. <span data-ttu-id="074ed-130">V poli Další iterace vyberte "Regenerace".</span><span class="sxs-lookup"><span data-stu-id="074ed-130">In the Subsequent iterations field, select 'Regeneration'.</span></span>
8. <span data-ttu-id="074ed-131">Do pole Počet vláken zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="074ed-131">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="074ed-132">To představuje počet paralelních podprocesů použitých pro plánování.</span><span class="sxs-lookup"><span data-stu-id="074ed-132">This represents the number of parallel threads used for planning.</span></span>  
9. <span data-ttu-id="074ed-133">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="074ed-133">Click OK.</span></span>

## <a name="view-the-result-of-the-plan"></a><span data-ttu-id="074ed-134">Zobrazení výsledku plánování</span><span class="sxs-lookup"><span data-stu-id="074ed-134">View the result of the plan</span></span>
1. <span data-ttu-id="074ed-135">V poli Plán kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="074ed-135">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="074ed-136">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="074ed-136">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="074ed-137">Klepněte na odkaz StaticPlan.</span><span class="sxs-lookup"><span data-stu-id="074ed-137">Click the link for StaticPlan.</span></span> <span data-ttu-id="074ed-138">Musíte být ve společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="074ed-138">You need to be in company USMF.</span></span>  
3. <span data-ttu-id="074ed-139">Klikněte na Plánované objednávky.</span><span class="sxs-lookup"><span data-stu-id="074ed-139">Click Planned orders.</span></span>


