---
title: Přesunutí naplánovaných kanbanových úloh
description: Tento postup se zaměřuje na přesunutí plánovaného zpracování kanbanových úloh do jiného období.
author: ChristianRytt
manager: tfehr
ms.date: 11/07/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bb95bab2173cb45300560f59c394cd2d558fe69f
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206972"
---
# <a name="move-scheduled-kanban-jobs"></a><span data-ttu-id="5e7fa-103">Přesunutí naplánovaných kanbanových úloh</span><span class="sxs-lookup"><span data-stu-id="5e7fa-103">Move scheduled kanban jobs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5e7fa-104">Tento postup se zaměřuje na přesunutí plánovaného zpracování kanbanových úloh do jiného období.</span><span class="sxs-lookup"><span data-stu-id="5e7fa-104">This procedure focuses on moving planned process kanban jobs to a different period.</span></span> <span data-ttu-id="5e7fa-105">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="5e7fa-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="5e7fa-106">Tento postup je určen pro dílenského nadřízeného nebo plánovače výroby pracujícího s kanbany.</span><span class="sxs-lookup"><span data-stu-id="5e7fa-106">This procedure is intended for the shop floor supervisor or production planner working with kanbans.</span></span>

## <a name="select-scheduled-kanban-jobs"></a><span data-ttu-id="5e7fa-107">Vyberte naplánované kanbanové úlohy.</span><span class="sxs-lookup"><span data-stu-id="5e7fa-107">Select scheduled kanban jobs.</span></span> 

1. <span data-ttu-id="5e7fa-108">Přejděte na **Řízení výroby > Kanban > Plánování kanbanové úlohy**.</span><span class="sxs-lookup"><span data-stu-id="5e7fa-108">Go to **Production control > Kanban > Kanban job scheduling**.</span></span> 

2. <span data-ttu-id="5e7fa-109">V poli **Pracovní buňka** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="5e7fa-109">In the **Work cell** field, click the drop-down button to open the lookup.</span></span> 

3. <span data-ttu-id="5e7fa-110">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="5e7fa-110">In the list, mark the selected row.</span></span> 
   - <span data-ttu-id="5e7fa-111">Vyberte pracovní buňku 1250.</span><span class="sxs-lookup"><span data-stu-id="5e7fa-111">Select work cell 1250.</span></span> 
4. <span data-ttu-id="5e7fa-112">Klepněte na tlačítko **Vybrat**.</span><span class="sxs-lookup"><span data-stu-id="5e7fa-112">Click **Select**.</span></span> 

5. <span data-ttu-id="5e7fa-113">V poli **Zobrazit stav úlohy** vyberte hodnotu **Plánováno**.</span><span class="sxs-lookup"><span data-stu-id="5e7fa-113">In the **Display job status** field, select **Scheduled**.</span></span> <span data-ttu-id="5e7fa-114">To vyfiltruje seznam úloh a zobrazí pouze plánované kanbanové úlohy.</span><span class="sxs-lookup"><span data-stu-id="5e7fa-114">This filters the job list to display only the scheduled kanban jobs.</span></span> 

## <a name="move-kanban-jobs-to-a-different-period"></a><span data-ttu-id="5e7fa-115">Přesuňte kanbanové úlohy do jiného období.</span><span class="sxs-lookup"><span data-stu-id="5e7fa-115">Move kanban jobs to a different period.</span></span> 

1. <span data-ttu-id="5e7fa-116">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="5e7fa-116">In the list, find and select the desired record.</span></span> <span data-ttu-id="5e7fa-117">Vyberte úlohu, bude má stav **Plánovaná úloha**, například úlohu naplánovanou v poli **Plánované období** na 20. prosince 2012.</span><span class="sxs-lookup"><span data-stu-id="5e7fa-117">Select a job that has the **Planned job** status, for example, a job scheduled on December 20, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="5e7fa-118">Poté přesuňte úlohu do předchozího období.</span><span class="sxs-lookup"><span data-stu-id="5e7fa-118">Then move the job to the previous period.</span></span> 

2. <span data-ttu-id="5e7fa-119">Klikněte na **Předchozí období**.</span><span class="sxs-lookup"><span data-stu-id="5e7fa-119">Click **Previous period**.</span></span> 

3. <span data-ttu-id="5e7fa-120">Klikněte na **Ukončit** pro přesun úlohy na konec seznamu úloh jako poslední úlohu v předchozím období.</span><span class="sxs-lookup"><span data-stu-id="5e7fa-120">Click **End** to move the job to the end of the job list as the last job in the previous period.</span></span> 

4. <span data-ttu-id="5e7fa-121">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="5e7fa-121">In the list, find and select the desired record.</span></span> <span data-ttu-id="5e7fa-122">Vyberte úlohu, bude má stav **Plánovaná úloha**, například úlohu naplánovanou v poli **Plánované období** na 18. prosince 2012.</span><span class="sxs-lookup"><span data-stu-id="5e7fa-122">Select a job that has the **Planned job** status, for example, a job scheduled on December 18, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="5e7fa-123">Poté přesuňte úlohu do dalšího období.</span><span class="sxs-lookup"><span data-stu-id="5e7fa-123">Then move the job to the next period.</span></span> 

5. <span data-ttu-id="5e7fa-124">Klikněte na **Následující období**.</span><span class="sxs-lookup"><span data-stu-id="5e7fa-124">Click **Next period**.</span></span> 

6. <span data-ttu-id="5e7fa-125">Klikněte na **Start** pro přesun úlohy na začátek seznamu úloh jako první úlohu v předchozím období.</span><span class="sxs-lookup"><span data-stu-id="5e7fa-125">Click **Start** to move the job to the start of the job list as the first job in the previous period.</span></span> 

## <a name="move-a-job-within-a-period"></a><span data-ttu-id="5e7fa-126">Přesuňte úlohu v rámci období</span><span class="sxs-lookup"><span data-stu-id="5e7fa-126">Move a job within a period.</span></span> 

1. <span data-ttu-id="5e7fa-127">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="5e7fa-127">In the list, find and select the desired record.</span></span> <span data-ttu-id="5e7fa-128">Vyberte úlohu, bude má stav plánované úlohy, například druhou úlohu naplánovanou v poli **Plánované období** na 19. prosince 2012.</span><span class="sxs-lookup"><span data-stu-id="5e7fa-128">Select a job that has the Planned job status, for example, the second job scheduled on December 19, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="5e7fa-129">Poté přesuňte úlohu v rámci plánovaného období.</span><span class="sxs-lookup"><span data-stu-id="5e7fa-129">Then move the job within the planned period.</span></span> 

2. <span data-ttu-id="5e7fa-130">Klikněte na **Vpřed**.</span><span class="sxs-lookup"><span data-stu-id="5e7fa-130">Click **Forward**.</span></span> <span data-ttu-id="5e7fa-131">Všimněte si, že úloha byla přesunuta o jeden řádek v seznamu dolů.</span><span class="sxs-lookup"><span data-stu-id="5e7fa-131">Notice that the job is moved one line down on the list.</span></span> 

3. <span data-ttu-id="5e7fa-132">Klikněte na **Vzad**.</span><span class="sxs-lookup"><span data-stu-id="5e7fa-132">Click **Backward**.</span></span> <span data-ttu-id="5e7fa-133">Všimněte si, že úloha byla přesunuta o jeden řádek v seznamu nahoru.</span><span class="sxs-lookup"><span data-stu-id="5e7fa-133">Notice that the job is moved one line up on the list.</span></span>
