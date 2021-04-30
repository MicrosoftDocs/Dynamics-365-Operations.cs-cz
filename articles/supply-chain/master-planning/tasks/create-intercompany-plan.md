---
title: Vytvoření mezipodnikového plánu
description: Tato procedura ukazuje, jak vytvořit mezipodnikový plán.
author: ChristianRytt
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f8cf4ed879b6b2202d0b0f1f45052f5e21452967
ms.sourcegitcommit: 9b07d536b4bd8addfbdba42d2429c9fedb664635
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867343"
---
# <a name="create-an-intercompany-plan"></a><span data-ttu-id="3f075-103">Vytvoření mezipodnikového plánu</span><span class="sxs-lookup"><span data-stu-id="3f075-103">Create an intercompany plan</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3f075-104">Tato procedura ukazuje, jak vytvořit mezipodnikový plán.</span><span class="sxs-lookup"><span data-stu-id="3f075-104">This procedure shows how to create an intercompany plan.</span></span> <span data-ttu-id="3f075-105">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="3f075-105">The demo data company used to create this procedure is USMF.</span></span>

## <a name="set-up-an-intercompany-planning-group"></a><span data-ttu-id="3f075-106">Nastavení skupiny mezipodnikového plánování</span><span class="sxs-lookup"><span data-stu-id="3f075-106">Set up an intercompany planning group</span></span>

1. <span data-ttu-id="3f075-107">V **navigačním podokně** přejděte na **Modules > Hlavní plánování > Nastavení > Skupiny mezipodnikového plánování**.</span><span class="sxs-lookup"><span data-stu-id="3f075-107">In the **Navigation pane**, go to **Modules > Master planning > Setup > Intercompany planning groups**.</span></span>
2. <span data-ttu-id="3f075-108">Použijte rychlý filtr pro hledání záznamů.</span><span class="sxs-lookup"><span data-stu-id="3f075-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="3f075-109">Můžete například filtrovat v poli Jméno pomocí hodnoty „10“.</span><span class="sxs-lookup"><span data-stu-id="3f075-109">For example, filter on the Name field with a value of '10'.</span></span>
3. <span data-ttu-id="3f075-110">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="3f075-110">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="3f075-111">Zvolte **Odstranit**.</span><span class="sxs-lookup"><span data-stu-id="3f075-111">Select **Delete**.</span></span> <span data-ttu-id="3f075-112">Tento krok je nezbytný pro účely zkrácení mezipodnikového plánování.</span><span class="sxs-lookup"><span data-stu-id="3f075-112">This step is necessary in order to shorten the intercompany planning run.</span></span>   <span data-ttu-id="3f075-113">Mezipodnikové plánování spustí hlavní plánování ve všech společnostech ve skupině plánování, počínaje nejnižší sekvencí plánování.</span><span class="sxs-lookup"><span data-stu-id="3f075-113">Intercompany planning will run master planning in all the companies in a planning group, starting from the lowest scheduling sequence.</span></span>  
5. <span data-ttu-id="3f075-114">Vyberte **Ano**.</span><span class="sxs-lookup"><span data-stu-id="3f075-114">Select **Yes**.</span></span>
6. <span data-ttu-id="3f075-115">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="3f075-115">Close the page.</span></span>

## <a name="create-an-intercompany-master-plan"></a><span data-ttu-id="3f075-116">Vytvoření mezipodnikového hlavního plánu</span><span class="sxs-lookup"><span data-stu-id="3f075-116">Create an intercompany master plan</span></span>

1. <span data-ttu-id="3f075-117">V **navigačním podokně** přejděte na **Modules > Hlavní plánování > Pracovní prostory > Hlavní plánování**.</span><span class="sxs-lookup"><span data-stu-id="3f075-117">In the **Navigation pane**, go to **Modules > Master planning > Workspaces > Master planning**.</span></span>
2. <span data-ttu-id="3f075-118">Vyberte **Mezipodnikové hlavní plánování**.</span><span class="sxs-lookup"><span data-stu-id="3f075-118">Select **Intercompany master planning**.</span></span>  
3. <span data-ttu-id="3f075-119">V poli **Skupina mezipodnikového plánování** zvolením tlačítka rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="3f075-119">In the **Intercompany planning group** field, select the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="3f075-120">Vyberte odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="3f075-120">In the list, select the link in the selected row.</span></span> <span data-ttu-id="3f075-121">Vyberte skupinu 10 mezipodnikového plánování.</span><span class="sxs-lookup"><span data-stu-id="3f075-121">Select intercompany planning group 10.</span></span>  
5. <span data-ttu-id="3f075-122">V poli **Počet iterací mezipodnikového plánování** zadejte 2.</span><span class="sxs-lookup"><span data-stu-id="3f075-122">In the **Number of intercompany planning iterations** field, enter '2'.</span></span> <span data-ttu-id="3f075-123">Skupina 10 mezipodnikového plánování má dva členy.</span><span class="sxs-lookup"><span data-stu-id="3f075-123">Intercompany planning group 10 has two members.</span></span> <span data-ttu-id="3f075-124">K rozšíření propagace zpoždění ze zdrojové společnosti (USMF) vůči společnosti zákazníka (DEMF) je třeba spustit dvakrát mezipodnikové plánování v obou společnostech dvakrát.</span><span class="sxs-lookup"><span data-stu-id="3f075-124">In order to propagate the delays from the source company (USMF) to the customer company (DEMF), you will need to run intercompany in both companies two times.</span></span> <span data-ttu-id="3f075-125">První iterace bude rozšiřovat poptávku a identifikovat zpoždění ve zdrojové společnosti (USMF).</span><span class="sxs-lookup"><span data-stu-id="3f075-125">The first iteration will propagate the demand and identify the delays in the source company (USMF).</span></span> <span data-ttu-id="3f075-126">Druhá iterace rozšíří zpoždění z USMF na DEMF.</span><span class="sxs-lookup"><span data-stu-id="3f075-126">The second iteration will propagate the delays from USMF to DEMF.</span></span>  
6. <span data-ttu-id="3f075-127">V poli **První iterace** vyberte Obnovení.</span><span class="sxs-lookup"><span data-stu-id="3f075-127">In the **First iteration** field, select 'Regeneration'.</span></span>
7. <span data-ttu-id="3f075-128">V poli **Další iterace** vyberte "Regenerace".</span><span class="sxs-lookup"><span data-stu-id="3f075-128">In the **Subsequent iterations** field, select 'Regeneration'.</span></span>
8. <span data-ttu-id="3f075-129">Do pole **Počet vláken** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="3f075-129">In the **Number of threads** field, enter a number.</span></span> <span data-ttu-id="3f075-130">To představuje počet paralelních podprocesů použitých pro plánování.</span><span class="sxs-lookup"><span data-stu-id="3f075-130">This represents the number of parallel threads used for planning.</span></span>  
9. <span data-ttu-id="3f075-131">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="3f075-131">Select **OK**.</span></span>

## <a name="view-the-result-of-the-plan"></a><span data-ttu-id="3f075-132">Zobrazení výsledku plánování</span><span class="sxs-lookup"><span data-stu-id="3f075-132">View the result of the plan</span></span>

1. <span data-ttu-id="3f075-133">V poli **Plán** zvolením tlačítka rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="3f075-133">In the **Plan** field, select the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="3f075-134">Vyberte odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="3f075-134">In the list, select the link in the selected row.</span></span> <span data-ttu-id="3f075-135">Vyberte odkaz pro StaticPlan.</span><span class="sxs-lookup"><span data-stu-id="3f075-135">Select the link for StaticPlan.</span></span> <span data-ttu-id="3f075-136">Musíte být ve společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="3f075-136">You need to be in company USMF.</span></span>  
3. <span data-ttu-id="3f075-137">Vyberte **Plánované objednávky**.</span><span class="sxs-lookup"><span data-stu-id="3f075-137">Select **Planned orders**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]