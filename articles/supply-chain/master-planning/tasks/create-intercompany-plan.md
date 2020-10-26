---
title: Vytvoření mezipodnikového plánu
description: Tato procedura ukazuje, jak vytvořit mezipodnikový plán.
author: ShylaThompson
manager: tfehr
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3ae3d8a7c437ffd41a4864bd8548aa84c8ab8f32
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/10/2020
ms.locfileid: "3978266"
---
# <a name="create-an-intercompany-plan"></a><span data-ttu-id="ada0c-103">Vytvoření mezipodnikového plánu</span><span class="sxs-lookup"><span data-stu-id="ada0c-103">Create an intercompany plan</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ada0c-104">Tato procedura ukazuje, jak vytvořit mezipodnikový plán.</span><span class="sxs-lookup"><span data-stu-id="ada0c-104">This procedure shows how to create an intercompany plan.</span></span> <span data-ttu-id="ada0c-105">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="ada0c-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-an-intercompany-planning-group"></a><span data-ttu-id="ada0c-106">Nastavení skupiny mezipodnikového plánování</span><span class="sxs-lookup"><span data-stu-id="ada0c-106">Set up an intercompany planning group</span></span> 
1. <span data-ttu-id="ada0c-107">V **navigačním podokně** přejděte na **Modules > Hlavní plánování > Nastavení > Skupiny mezipodnikového plánování** .</span><span class="sxs-lookup"><span data-stu-id="ada0c-107">In the **Navigation pane** , go to **Modules > Master planning > Setup > Intercompany planning groups** .</span></span> 
2. <span data-ttu-id="ada0c-108">Použijte rychlý filtr pro hledání záznamů.</span><span class="sxs-lookup"><span data-stu-id="ada0c-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="ada0c-109">Můžete například filtrovat v poli Jméno pomocí hodnoty „10“.</span><span class="sxs-lookup"><span data-stu-id="ada0c-109">For example, filter on the Name field with a value of '10'.</span></span>
3. <span data-ttu-id="ada0c-110">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="ada0c-110">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="ada0c-111">Klepněte na tlačítko **Odstranit** .</span><span class="sxs-lookup"><span data-stu-id="ada0c-111">Click **Delete** .</span></span> <span data-ttu-id="ada0c-112">Tento krok je nezbytný pro účely zkrácení mezipodnikového plánování.</span><span class="sxs-lookup"><span data-stu-id="ada0c-112">This step is necessary in order to shorten the intercompany planning run.</span></span>   <span data-ttu-id="ada0c-113">Mezipodnikové plánování spustí hlavní plánování ve všech společnostech ve skupině plánování, počínaje nejnižší sekvencí plánování.</span><span class="sxs-lookup"><span data-stu-id="ada0c-113">Intercompany planning will run master planning in all the companies in a planning group, starting from the lowest scheduling sequence.</span></span>  
5. <span data-ttu-id="ada0c-114">Klepněte na tlačítko **Ano** .</span><span class="sxs-lookup"><span data-stu-id="ada0c-114">Click **Yes** .</span></span>
6. <span data-ttu-id="ada0c-115">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ada0c-115">Close the page.</span></span>

## <a name="create-an-intercompany-plan"></a><span data-ttu-id="ada0c-116">Vytvoření mezipodnikového plánu</span><span class="sxs-lookup"><span data-stu-id="ada0c-116">Create an intercompany plan</span></span>
1. <span data-ttu-id="ada0c-117">V **navigačním podokně** přejděte na **Modules > Hlavní plánování > Pracovní prostory > Hlavní plánování** .</span><span class="sxs-lookup"><span data-stu-id="ada0c-117">In the **Navigation pane** , go to **Modules > Master planning > Workspaces > Master planning** .</span></span>
2. <span data-ttu-id="ada0c-118">Klikněte na **Mezipodnikové hlavní plánování** .</span><span class="sxs-lookup"><span data-stu-id="ada0c-118">Click **Intercompany master planning** .</span></span>  
3. <span data-ttu-id="ada0c-119">V poli **Skupina mezipodnikového plánování** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="ada0c-119">In the **Intercompany planning group** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="ada0c-120">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="ada0c-120">In the list, click the link in the selected row.</span></span> <span data-ttu-id="ada0c-121">Vyberte skupinu 10 mezipodnikového plánování.</span><span class="sxs-lookup"><span data-stu-id="ada0c-121">Select intercompany planning group 10.</span></span>  
5. <span data-ttu-id="ada0c-122">V poli **Počet iterací mezipodnikového plánování** zadejte 2.</span><span class="sxs-lookup"><span data-stu-id="ada0c-122">In the **Number of intercompany planning iterations** field, enter '2'.</span></span> <span data-ttu-id="ada0c-123">Skupina 10 mezipodnikového plánování má dva členy.</span><span class="sxs-lookup"><span data-stu-id="ada0c-123">Intercompany planning group 10 has two members.</span></span> <span data-ttu-id="ada0c-124">K rozšíření propagace zpoždění ze zdrojové společnosti (USMF) vůči společnosti zákazníka (DEMF) je třeba spustit dvakrát mezipodnikové plánování v obou společnostech dvakrát.</span><span class="sxs-lookup"><span data-stu-id="ada0c-124">In order to propagate the delays from the source company (USMF) to the customer company (DEMF), you will need to run intercompany in both companies two times.</span></span> <span data-ttu-id="ada0c-125">První iterace bude rozšiřovat poptávku a identifikovat zpoždění ve zdrojové společnosti (USMF).</span><span class="sxs-lookup"><span data-stu-id="ada0c-125">The first iteration will propagate the demand and identify the delays in the source company (USMF).</span></span> <span data-ttu-id="ada0c-126">Druhá iterace rozšíří zpoždění z USMF na DEMF.</span><span class="sxs-lookup"><span data-stu-id="ada0c-126">The second iteration will propagate the delays from USMF to DEMF.</span></span>  
6. <span data-ttu-id="ada0c-127">V poli **První iterace** vyberte Obnovení.</span><span class="sxs-lookup"><span data-stu-id="ada0c-127">In the **First iteration** field, select 'Regeneration'.</span></span>
7. <span data-ttu-id="ada0c-128">V poli **Další iterace** vyberte "Regenerace".</span><span class="sxs-lookup"><span data-stu-id="ada0c-128">In the **Subsequent iterations** field, select 'Regeneration'.</span></span>
8. <span data-ttu-id="ada0c-129">Do pole **Počet vláken** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="ada0c-129">In the **Number of threads** field, enter a number.</span></span> <span data-ttu-id="ada0c-130">To představuje počet paralelních podprocesů použitých pro plánování.</span><span class="sxs-lookup"><span data-stu-id="ada0c-130">This represents the number of parallel threads used for planning.</span></span>  
9. <span data-ttu-id="ada0c-131">Klikněte na tlačítko **OK** .</span><span class="sxs-lookup"><span data-stu-id="ada0c-131">Click **OK** .</span></span>

## <a name="view-the-result-of-the-plan"></a><span data-ttu-id="ada0c-132">Zobrazení výsledku plánování</span><span class="sxs-lookup"><span data-stu-id="ada0c-132">View the result of the plan</span></span>
1. <span data-ttu-id="ada0c-133">V poli **Plán** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="ada0c-133">In the **Plan** field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="ada0c-134">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="ada0c-134">In the list, click the link in the selected row.</span></span> <span data-ttu-id="ada0c-135">Klepněte na odkaz StaticPlan.</span><span class="sxs-lookup"><span data-stu-id="ada0c-135">Click the link for StaticPlan.</span></span> <span data-ttu-id="ada0c-136">Musíte být ve společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="ada0c-136">You need to be in company USMF.</span></span>  
3. <span data-ttu-id="ada0c-137">Klikněte na **Plánované objednávky** .</span><span class="sxs-lookup"><span data-stu-id="ada0c-137">Click **Planned orders** .</span></span>

