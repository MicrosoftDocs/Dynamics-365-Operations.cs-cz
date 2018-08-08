--- 
title: "Přesunutí naplánovaných kanbanových úloh"
description: "Tento postup se zaměřuje na přesunutí plánovaného zpracování kanbanových úloh do jiného období."
author: ChristianRytt
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 6461e5638eaddeaeaef82304b7976bad350b331e
ms.contentlocale: cs-cz
ms.lasthandoff: 08/07/2018

---
# <a name="move-scheduled-kanban-jobs"></a><span data-ttu-id="e240f-103">Přesunutí naplánovaných kanbanových úloh</span><span class="sxs-lookup"><span data-stu-id="e240f-103">Move scheduled kanban jobs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e240f-104">Tento postup se zaměřuje na přesunutí plánovaného zpracování kanbanových úloh do jiného období.</span><span class="sxs-lookup"><span data-stu-id="e240f-104">This procedure focuses on moving planned process kanban jobs to a different period.</span></span> <span data-ttu-id="e240f-105">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="e240f-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="e240f-106">Tento postup je určen pro dílenského nadřízeného nebo plánovače výroby pracujícího s kanbany.</span><span class="sxs-lookup"><span data-stu-id="e240f-106">This procedure is intended for the shop floor supervisor or production planner working with kanbans.</span></span>


## <a name="select-scheduled-kanban-jobs"></a><span data-ttu-id="e240f-107">Vyberte naplánované kanbanové úlohy</span><span class="sxs-lookup"><span data-stu-id="e240f-107">Select scheduled kanban jobs</span></span>
1. <span data-ttu-id="e240f-108">Gå til Produktionsstyring > Kanban > Tidsplanlægning af kanban-job.</span><span class="sxs-lookup"><span data-stu-id="e240f-108">Gå til Produktionsstyring > Kanban > Tidsplanlægning af kanban-job.</span></span>
2. <span data-ttu-id="e240f-109">!MtCMR!V poli Pracovní buňka kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="e240f-109">!MtCMR!In the Work cell field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="e240f-110">áçêìõý !</span><span class="sxs-lookup"><span data-stu-id="e240f-110">áçêìõý !</span></span>
3. <span data-ttu-id="e240f-111">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="e240f-111">Markér den valgte række på listen.</span></span>
    * <span data-ttu-id="e240f-112">Vyberte pracovní buňku 1250.</span><span class="sxs-lookup"><span data-stu-id="e240f-112">Select work cell 1250.</span></span>  
4. <span data-ttu-id="e240f-113">Klikněte na Vybrat.</span><span class="sxs-lookup"><span data-stu-id="e240f-113">Klik på Select.</span></span>
5. <span data-ttu-id="e240f-114">Vælg 'Planlagt' i feltet Zobrazit stav úlohy.</span><span class="sxs-lookup"><span data-stu-id="e240f-114">Vælg 'Planlagt' i feltet Display job status.</span></span>
    * <span data-ttu-id="e240f-115">To vyfiltruje seznam úloh a zobrazí pouze plánované kanbanové úlohy.</span><span class="sxs-lookup"><span data-stu-id="e240f-115">This filters the job list to display only the scheduled kanban jobs.</span></span>  

## <a name="move-kanban-jobs-to-a-different-period"></a><span data-ttu-id="e240f-116">Přesunutí kanbanových úloh do jiného období</span><span class="sxs-lookup"><span data-stu-id="e240f-116">Move kanban jobs to a different period</span></span>
1. <span data-ttu-id="e240f-117">Najděte og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="e240f-117">Find og vælg den ønskede post på listen.</span></span>
    * <span data-ttu-id="e240f-118">Vyberte úlohu, bude má stav plánované úlohy, například úlohu naplánovanou v poli Plánované období na 20. prosince 2012.</span><span class="sxs-lookup"><span data-stu-id="e240f-118">Select a job that has the Planned job status, for example, a job scheduled on December 20, 2012  in the Planned period field.</span></span> <span data-ttu-id="e240f-119">Poté přesuňte úlohu do předchozího období.</span><span class="sxs-lookup"><span data-stu-id="e240f-119">Then move the job to the previous period.</span></span>  
2. <span data-ttu-id="e240f-120">Klikněte na Předchozí období.</span><span class="sxs-lookup"><span data-stu-id="e240f-120">Klik på Previous period.</span></span>
3. <span data-ttu-id="e240f-121">Klikněte na Konec.</span><span class="sxs-lookup"><span data-stu-id="e240f-121">Klik på End.</span></span>
    * <span data-ttu-id="e240f-122">To přesune úlohu na konec seznamu úloh jako poslední úlohu v předchozím období.</span><span class="sxs-lookup"><span data-stu-id="e240f-122">This will move the job to the end of the job list as the last job in the previous period.</span></span>  
4. <span data-ttu-id="e240f-123">Najděte og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="e240f-123">Find og vælg den ønskede post på listen.</span></span>
    * <span data-ttu-id="e240f-124">Vyberte úlohu, bude má stav plánované úlohy, například úlohu naplánovanou v poli Plánované období na 18. prosince 2012.</span><span class="sxs-lookup"><span data-stu-id="e240f-124">Select a job that has the Planned job status, for example, a job scheduled on December 18, 2012 in the Planned period field.</span></span> <span data-ttu-id="e240f-125">Poté přesuňte úlohu do dalšího období.</span><span class="sxs-lookup"><span data-stu-id="e240f-125">Then move the job to the next period.</span></span>  
5. <span data-ttu-id="e240f-126">Klikněte na Další období.</span><span class="sxs-lookup"><span data-stu-id="e240f-126">Klik på Next period.</span></span>
6. <span data-ttu-id="e240f-127">Klikněte na Zahájení.</span><span class="sxs-lookup"><span data-stu-id="e240f-127">Klik på Start.</span></span>
    * <span data-ttu-id="e240f-128">To přesune úlohu na začátek seznamu úloh jako první úlohu v předchozím období.</span><span class="sxs-lookup"><span data-stu-id="e240f-128">This will move the job to the start of the job list as the first job in the previous period.</span></span>  

## <a name="task-move-a-job-within-a-period"></a><span data-ttu-id="e240f-129">Úloha: Přesunutí úlohy v rámci období</span><span class="sxs-lookup"><span data-stu-id="e240f-129">Task: Move a job within a period</span></span>
1. <span data-ttu-id="e240f-130">Najděte og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="e240f-130">Find og vælg den ønskede post på listen.</span></span>
    * <span data-ttu-id="e240f-131">Vyberte úlohu, bude má stav plánované úlohy, například druhou úlohu naplánovanou v poli Plánované období na 19. prosince 2012.</span><span class="sxs-lookup"><span data-stu-id="e240f-131">Select a job that has the Planned job status, for example, the second job scheduled on December 19, 2012 in the Planned period field.</span></span> <span data-ttu-id="e240f-132">Poté přesuňte úlohu v rámci plánovaného období.</span><span class="sxs-lookup"><span data-stu-id="e240f-132">Then move the job within the planned period.</span></span>  
2. <span data-ttu-id="e240f-133">Klikněte na Dopředu.</span><span class="sxs-lookup"><span data-stu-id="e240f-133">Klik på Forward.</span></span>
    * <span data-ttu-id="e240f-134">Všimněte si, že úloha byla přesunuta o jeden řádek v seznamu dolů.</span><span class="sxs-lookup"><span data-stu-id="e240f-134">Notice that the job is moved one line down on the list.</span></span>  
3. <span data-ttu-id="e240f-135">Klikněte na Zpět.</span><span class="sxs-lookup"><span data-stu-id="e240f-135">Klik på Backward.</span></span>
    * <span data-ttu-id="e240f-136">Všimněte si, že úloha byla přesunuta o jeden řádek v seznamu nahoru.</span><span class="sxs-lookup"><span data-stu-id="e240f-136">Notice that the job is moved one line up on the list.</span></span>  


