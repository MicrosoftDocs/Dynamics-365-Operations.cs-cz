---
title: Vytvoření mezipodnikového plánu
description: Tato procedura ukazuje, jak vytvořit mezipodnikový plán.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d378a89bbb4de6d67db0019dc72a27945d50c4e9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "333730"
---
# <a name="create-an-intercompany-plan"></a><span data-ttu-id="f0480-103">Vytvoření mezipodnikového plánu</span><span class="sxs-lookup"><span data-stu-id="f0480-103">Create an intercompany plan</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f0480-104">Tato procedura ukazuje, jak vytvořit mezipodnikový plán.</span><span class="sxs-lookup"><span data-stu-id="f0480-104">This procedure shows how to create an intercompany plan.</span></span> <span data-ttu-id="f0480-105">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="f0480-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-an-intercompany-planning-group"></a><span data-ttu-id="f0480-106">Nastavení skupiny mezipodnikového plánování</span><span class="sxs-lookup"><span data-stu-id="f0480-106">Set up an intercompany planning group</span></span> 
1. <span data-ttu-id="f0480-107">Přejděte na Skupiny mezipodnikového plánování.</span><span class="sxs-lookup"><span data-stu-id="f0480-107">Go to Intercompany planning groups.</span></span>
    * <span data-ttu-id="f0480-108">Hlavní plánování > Nastavení > Skupiny mezipodnikového plánování</span><span class="sxs-lookup"><span data-stu-id="f0480-108">Master planning > Setup > Intercompany planning groups</span></span>  
2. <span data-ttu-id="f0480-109">Použijte rychlý filtr pro hledání záznamů.</span><span class="sxs-lookup"><span data-stu-id="f0480-109">Use the Quick Filter to find records.</span></span> <span data-ttu-id="f0480-110">Můžete například filtrovat v poli Jméno pomocí hodnoty „10“.</span><span class="sxs-lookup"><span data-stu-id="f0480-110">For example, filter on the Name field with a value of '10'.</span></span>
3. <span data-ttu-id="f0480-111">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="f0480-111">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="f0480-112">Klepněte na tlačítko Odstranit.</span><span class="sxs-lookup"><span data-stu-id="f0480-112">Click Delete.</span></span>
    * <span data-ttu-id="f0480-113">Tento krok je nezbytný pro účely zkrácení mezipodnikového plánování.</span><span class="sxs-lookup"><span data-stu-id="f0480-113">This step is necessary in order to shorten the intercompany planning run.</span></span>   <span data-ttu-id="f0480-114">Mezipodnikové plánování spustí hlavní plánování ve všech společnostech ve skupině plánování, počínaje nejnižší sekvencí plánování.</span><span class="sxs-lookup"><span data-stu-id="f0480-114">Intercompany planning will run master planning in all the companies in a planning group, starting from the lowest scheduling sequence.</span></span>  
5. <span data-ttu-id="f0480-115">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="f0480-115">Click Yes.</span></span>
6. <span data-ttu-id="f0480-116">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="f0480-116">Close the page.</span></span>

## <a name="create-an-intercompany-plan"></a><span data-ttu-id="f0480-117">Vytvoření mezipodnikového plánu</span><span class="sxs-lookup"><span data-stu-id="f0480-117">Create an intercompany plan</span></span>
1. <span data-ttu-id="f0480-118">Klikněte na Mezipodnikové hlavní plánování.</span><span class="sxs-lookup"><span data-stu-id="f0480-118">Click Intercompany master planning.</span></span>
    * <span data-ttu-id="f0480-119">Jedná se o pracovní prostor hlavního plánování.</span><span class="sxs-lookup"><span data-stu-id="f0480-119">This is on the Master planning workspace.</span></span>  
2. <span data-ttu-id="f0480-120">V poli Skupina mezipodnikového plánování kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="f0480-120">In the Intercompany planning group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="f0480-121">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="f0480-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f0480-122">Vyberte skupinu 10 mezipodnikového plánování.</span><span class="sxs-lookup"><span data-stu-id="f0480-122">Select intercompany planning group 10.</span></span>  
4. <span data-ttu-id="f0480-123">V poli Počet iterací mezipodnikového plánování zadejte 2.</span><span class="sxs-lookup"><span data-stu-id="f0480-123">In the Number of intercompany planning iterations field, enter '2'.</span></span>
    * <span data-ttu-id="f0480-124">Skupina 10 mezipodnikového plánování má dva členy.</span><span class="sxs-lookup"><span data-stu-id="f0480-124">Intercompany planning group 10 has two members.</span></span> <span data-ttu-id="f0480-125">K rozšíření propagace zpoždění ze zdrojové společnosti (USMF) vůči společnosti zákazníka (DEMF) je třeba spustit dvakrát mezipodnikové plánování v obou společnostech dvakrát.</span><span class="sxs-lookup"><span data-stu-id="f0480-125">In order to propagate the delays from the source company (USMF) to the customer company (DEMF), you will need to run intercompany in both companies two times.</span></span> <span data-ttu-id="f0480-126">První iterace bude rozšiřovat poptávku a identifikovat zpoždění ve zdrojové společnosti (USMF).</span><span class="sxs-lookup"><span data-stu-id="f0480-126">The first iteration will propagate the demand and identify the delays in the source company (USMF).</span></span> <span data-ttu-id="f0480-127">Druhá iterace rozšíří zpoždění z USMF na DEMF.</span><span class="sxs-lookup"><span data-stu-id="f0480-127">The second iteration will propagate the delays from USMF to DEMF.</span></span>  
5. <span data-ttu-id="f0480-128">Vyberte volbu v poli První iterace.</span><span class="sxs-lookup"><span data-stu-id="f0480-128">In the First iteration field, select an option.</span></span>
6. <span data-ttu-id="f0480-129">V poli První iterace vyberte Obnovení.</span><span class="sxs-lookup"><span data-stu-id="f0480-129">In the First iteration field, select 'Regeneration'.</span></span>
7. <span data-ttu-id="f0480-130">V poli Další iterace vyberte "Regenerace".</span><span class="sxs-lookup"><span data-stu-id="f0480-130">In the Subsequent iterations field, select 'Regeneration'.</span></span>
8. <span data-ttu-id="f0480-131">Do pole Počet vláken zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="f0480-131">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="f0480-132">To představuje počet paralelních podprocesů použitých pro plánování.</span><span class="sxs-lookup"><span data-stu-id="f0480-132">This represents the number of parallel threads used for planning.</span></span>  
9. <span data-ttu-id="f0480-133">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="f0480-133">Click OK.</span></span>

## <a name="view-the-result-of-the-plan"></a><span data-ttu-id="f0480-134">Zobrazení výsledku plánování</span><span class="sxs-lookup"><span data-stu-id="f0480-134">View the result of the plan</span></span>
1. <span data-ttu-id="f0480-135">V poli Plán kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="f0480-135">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="f0480-136">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="f0480-136">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f0480-137">Klepněte na odkaz StaticPlan.</span><span class="sxs-lookup"><span data-stu-id="f0480-137">Click the link for StaticPlan.</span></span> <span data-ttu-id="f0480-138">Musíte být ve společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="f0480-138">You need to be in company USMF.</span></span>  
3. <span data-ttu-id="f0480-139">Klikněte na Plánované objednávky.</span><span class="sxs-lookup"><span data-stu-id="f0480-139">Click Planned orders.</span></span>

