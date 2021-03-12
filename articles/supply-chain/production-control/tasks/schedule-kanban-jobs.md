---
title: Plánování kanbanových úloh
description: Tento postup se zaměřuje na plánování zpracování kanbanových úloh pro konkrétní pracovní buňku.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, KanbanPeriodCapacityPart, SysLookupMultiSelectGrid, KanbanBoardScheduleJobForward
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f97b88a2637e661146e8150cd6535ff32745227a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4996794"
---
# <a name="schedule-kanban-jobs"></a><span data-ttu-id="67e5d-103">Plánování kanbanových úloh</span><span class="sxs-lookup"><span data-stu-id="67e5d-103">Schedule kanban jobs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="67e5d-104">Tento postup se zaměřuje na plánování zpracování kanbanových úloh pro konkrétní pracovní buňku.</span><span class="sxs-lookup"><span data-stu-id="67e5d-104">This procedure focuses on scheduling process kanban jobs for a specific work cell.</span></span> <span data-ttu-id="67e5d-105">Postup "Příprava procesní kanbanové úlohy, pokud nejsou materiály k dispozici" je předpokladem pro vytvoření tohoto postupu.</span><span class="sxs-lookup"><span data-stu-id="67e5d-105">The procedure "Prepare a process kanban job when materials are not available" is a prerequisite for creating this procedure.</span></span> <span data-ttu-id="67e5d-106">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="67e5d-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="67e5d-107">Tato úloha je určena pro dílenského nadřízeného a plánovače výroby pracujícího s kanbany.</span><span class="sxs-lookup"><span data-stu-id="67e5d-107">This task is intended for the shop floor supervisor and production planner working with kanbans.</span></span>


## <a name="select-kanban-jobs-for-a-work-cell"></a><span data-ttu-id="67e5d-108">Vyberte kanbanové úlohy pro pracovní buňku</span><span class="sxs-lookup"><span data-stu-id="67e5d-108">Select kanban jobs for a work cell</span></span>
1. <span data-ttu-id="67e5d-109">Přejděte na Řízení výroby > Kanban > Plánování kanbanové úlohy.</span><span class="sxs-lookup"><span data-stu-id="67e5d-109">Go to Production control > Kanban > Kanban job scheduling.</span></span>
2. <span data-ttu-id="67e5d-110">Rozbalte okno s fakty Kapacita období</span><span class="sxs-lookup"><span data-stu-id="67e5d-110">Expand the Period capacity fact box</span></span>
    * <span data-ttu-id="67e5d-111">Rozbalte okno s fakty pro kanban.</span><span class="sxs-lookup"><span data-stu-id="67e5d-111">Expand the Kanban FactBox.</span></span>  
3. <span data-ttu-id="67e5d-112">V poli Pracovní buňka kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="67e5d-112">In the Work cell field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="67e5d-113">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="67e5d-113">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="67e5d-114">Vyberte pracovní buňku 1250.</span><span class="sxs-lookup"><span data-stu-id="67e5d-114">Select work cell 1250.</span></span> <span data-ttu-id="67e5d-115">To způsobí filtrování zobrazení a zobrazíte tak pouze úlohy pro pracovní buňku 1250.</span><span class="sxs-lookup"><span data-stu-id="67e5d-115">This will filter the view to display only the jobs for work cell 1250.</span></span>  
5. <span data-ttu-id="67e5d-116">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="67e5d-116">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="67e5d-117">Klepněte na tlačítko Vybrat.</span><span class="sxs-lookup"><span data-stu-id="67e5d-117">Click Select.</span></span>

## <a name="schedule-a-kanban-job-in-the-first-available-period"></a><span data-ttu-id="67e5d-118">Naplánování kanbanové úlohy v prvním dostupném období</span><span class="sxs-lookup"><span data-stu-id="67e5d-118">Schedule a kanban job in the first available period</span></span>
1. <span data-ttu-id="67e5d-119">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="67e5d-119">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="67e5d-120">Vyberte první řádek v seznamu, který má stav Neplánováno.</span><span class="sxs-lookup"><span data-stu-id="67e5d-120">Select the first row in the list that has the Not planned status.</span></span> <span data-ttu-id="67e5d-121">Tečkovaná ikona v poli Stav úlohy označuje neplánovanou úlohu.</span><span class="sxs-lookup"><span data-stu-id="67e5d-121">The dotted icon in the Job status field indicates not planned.</span></span>  
2. <span data-ttu-id="67e5d-122">Klikněte na Plánovat.</span><span class="sxs-lookup"><span data-stu-id="67e5d-122">Click Schedule.</span></span>
    * <span data-ttu-id="67e5d-123">To způsobí naplánování kanbanové úlohy v prvním dostupném období.</span><span class="sxs-lookup"><span data-stu-id="67e5d-123">This will schedule the kanban job in the first available period.</span></span>  
    * <span data-ttu-id="67e5d-124">Všimněte si, že kanbanová úloha se přesunula na konec seznamu, protože byla přidána k období počínajícího dnešním dnem.</span><span class="sxs-lookup"><span data-stu-id="67e5d-124">Notice that the kanban job is moved to the end of the list because it has been added to the period starting from today.</span></span>  
    * <span data-ttu-id="67e5d-125">Pokud období začínající dneškem je plně rezervováno, úloha bude přesunuta do prvního volného období.</span><span class="sxs-lookup"><span data-stu-id="67e5d-125">If the period starting from today is fully booked, the job will be moved to the first available period.</span></span>  

## <a name="schedule-two-kanban-jobs-for-a-specific-day"></a><span data-ttu-id="67e5d-126">Naplánování dvou kanbanových úloh na určitý den</span><span class="sxs-lookup"><span data-stu-id="67e5d-126">Schedule two kanban jobs for a specific day</span></span>
1. <span data-ttu-id="67e5d-127">Vyberte ze seznamu řádek 1.</span><span class="sxs-lookup"><span data-stu-id="67e5d-127">In the list, select row 1.</span></span>
    * <span data-ttu-id="67e5d-128">Měli byste dohlédnout na to, aby první řádek měl stav Neplánováno v poli Stav úlohy.</span><span class="sxs-lookup"><span data-stu-id="67e5d-128">You should see that the first row has the Not planned status in the Job status field.</span></span>  
2. <span data-ttu-id="67e5d-129">Vyberte ze seznamu řádek 2.</span><span class="sxs-lookup"><span data-stu-id="67e5d-129">In the list, select row 2.</span></span>
    * <span data-ttu-id="67e5d-130">Měli byste dohlédnout na to, aby druhý řádek měl stav Neplánováno v poli Stav úlohy.</span><span class="sxs-lookup"><span data-stu-id="67e5d-130">You should see that the second row has the Not planned status in the Job status field.</span></span> <span data-ttu-id="67e5d-131">Nyní máte vybrané první dvě úlohy.</span><span class="sxs-lookup"><span data-stu-id="67e5d-131">Now you have the first two jobs selected.</span></span>  
3. <span data-ttu-id="67e5d-132">Kliknutím na Plánováno od data otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="67e5d-132">Click Schedule from date to open the drop dialog.</span></span>
4. <span data-ttu-id="67e5d-133">Označte nebo odznačte pole Přepsat reakci na nedostatek kapacity.</span><span class="sxs-lookup"><span data-stu-id="67e5d-133">Check or uncheck the Override capacity shortage reaction box.</span></span>
    * <span data-ttu-id="67e5d-134">Tato možnost umožňuje přepsat výchozí reakci na nedostatek kapacity.</span><span class="sxs-lookup"><span data-stu-id="67e5d-134">This option allows you to override the default capacity shortage reaction.</span></span>  
5. <span data-ttu-id="67e5d-135">V poli Reakce na nedostatek kapacity vyberte Přidat do požadovaného období.</span><span class="sxs-lookup"><span data-stu-id="67e5d-135">In the Capacity shortage reaction field, select 'Add to the requested period'.</span></span>
    * <span data-ttu-id="67e5d-136">Touto možností zajistíte, aby úloha byla přidána do požadovaného období bez ohledu na to, zda je pracovní buňka přetížena.</span><span class="sxs-lookup"><span data-stu-id="67e5d-136">This option will ensure that the job is added to the requested period, regardless if the work cell might be overloaded.</span></span>  
6. <span data-ttu-id="67e5d-137">Klikněte na Plánovat.</span><span class="sxs-lookup"><span data-stu-id="67e5d-137">Click Schedule.</span></span>
    * <span data-ttu-id="67e5d-138">Všimněte si, že obě úlohy jsou přidány do požadovaného období.</span><span class="sxs-lookup"><span data-stu-id="67e5d-138">Notice that both jobs are added to the desired period.</span></span>  
    * <span data-ttu-id="67e5d-139">V části Kapacita období můžete vidět zatížení pro jednotlivá období.</span><span class="sxs-lookup"><span data-stu-id="67e5d-139">In the Period capacity section, you can see the load for each period.</span></span> <span data-ttu-id="67e5d-140">Pole Spotřeba zobrazí plánovanou spotřebu v tomto období.</span><span class="sxs-lookup"><span data-stu-id="67e5d-140">The Consumption field shows the scheduled consumption in this period.</span></span> <span data-ttu-id="67e5d-141">Pokud je plánovaná spotřeba větší, než kapacita dostupná v tomto období, bude vybrán stav Přetížení spotřeby.</span><span class="sxs-lookup"><span data-stu-id="67e5d-141">If the scheduled consumption is higher than the available capacity in this period, the overloaded consumption will be selected.</span></span>  

