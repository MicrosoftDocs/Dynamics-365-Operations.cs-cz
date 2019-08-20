---
title: Přesunutí naplánovaných kanbanových úloh
description: Tento postup se zaměřuje na přesunutí plánovaného zpracování kanbanových úloh do jiného období.
author: ChristianRytt
manager: AnnBe
ms.date: 11/07/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2526c2bd106e35c736e930b5b5114d019718dc5a
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836233"
---
# <a name="move-scheduled-kanban-jobs"></a><span data-ttu-id="eaf86-103">Přesunutí naplánovaných kanbanových úloh</span><span class="sxs-lookup"><span data-stu-id="eaf86-103">Move scheduled kanban jobs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="eaf86-104">Tento postup se zaměřuje na přesunutí plánovaného zpracování kanbanových úloh do jiného období.</span><span class="sxs-lookup"><span data-stu-id="eaf86-104">This procedure focuses on moving planned process kanban jobs to a different period.</span></span> <span data-ttu-id="eaf86-105">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="eaf86-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="eaf86-106">Tento postup je určen pro dílenského nadřízeného nebo plánovače výroby pracujícího s kanbany.</span><span class="sxs-lookup"><span data-stu-id="eaf86-106">This procedure is intended for the shop floor supervisor or production planner working with kanbans.</span></span>

## <a name="select-scheduled-kanban-jobs"></a><span data-ttu-id="eaf86-107">Vyberte naplánované kanbanové úlohy.</span><span class="sxs-lookup"><span data-stu-id="eaf86-107">Select scheduled kanban jobs.</span></span> 

1. <span data-ttu-id="eaf86-108">Přejděte na **Řízení výroby > Kanban > Plánování kanbanové úlohy**.</span><span class="sxs-lookup"><span data-stu-id="eaf86-108">Go to **Production control > Kanban > Kanban job scheduling**.</span></span> 

2. <span data-ttu-id="eaf86-109">V poli **Pracovní buňka** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="eaf86-109">In the **Work cell** field, click the drop-down button to open the lookup.</span></span> 

3. <span data-ttu-id="eaf86-110">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="eaf86-110">In the list, mark the selected row.</span></span> 
   - <span data-ttu-id="eaf86-111">Vyberte pracovní buňku 1250.</span><span class="sxs-lookup"><span data-stu-id="eaf86-111">Select work cell 1250.</span></span> 
4. <span data-ttu-id="eaf86-112">Klepněte na tlačítko **Vybrat**.</span><span class="sxs-lookup"><span data-stu-id="eaf86-112">Click **Select**.</span></span> 

5. <span data-ttu-id="eaf86-113">V poli **Zobrazit stav úlohy** vyberte hodnotu **Plánováno**.</span><span class="sxs-lookup"><span data-stu-id="eaf86-113">In the **Display job status** field, select **Scheduled**.</span></span> <span data-ttu-id="eaf86-114">To vyfiltruje seznam úloh a zobrazí pouze plánované kanbanové úlohy.</span><span class="sxs-lookup"><span data-stu-id="eaf86-114">This filters the job list to display only the scheduled kanban jobs.</span></span> 

## <a name="move-kanban-jobs-to-a-different-period"></a><span data-ttu-id="eaf86-115">Přesuňte kanbanové úlohy do jiného období.</span><span class="sxs-lookup"><span data-stu-id="eaf86-115">Move kanban jobs to a different period.</span></span> 

1. <span data-ttu-id="eaf86-116">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="eaf86-116">In the list, find and select the desired record.</span></span> <span data-ttu-id="eaf86-117">Vyberte úlohu, bude má stav **Plánovaná úloha**, například úlohu naplánovanou v poli **Plánované období** na 20. prosince 2012.</span><span class="sxs-lookup"><span data-stu-id="eaf86-117">Select a job that has the **Planned job** status, for example, a job scheduled on December 20, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="eaf86-118">Poté přesuňte úlohu do předchozího období.</span><span class="sxs-lookup"><span data-stu-id="eaf86-118">Then move the job to the previous period.</span></span> 

2. <span data-ttu-id="eaf86-119">Klikněte na **Předchozí období**.</span><span class="sxs-lookup"><span data-stu-id="eaf86-119">Click **Previous period**.</span></span> 

3. <span data-ttu-id="eaf86-120">Klikněte na **Ukončit** pro přesun úlohy na konec seznamu úloh jako poslední úlohu v předchozím období.</span><span class="sxs-lookup"><span data-stu-id="eaf86-120">Click **End** to move the job to the end of the job list as the last job in the previous period.</span></span> 

4. <span data-ttu-id="eaf86-121">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="eaf86-121">In the list, find and select the desired record.</span></span> <span data-ttu-id="eaf86-122">Vyberte úlohu, bude má stav **Plánovaná úloha**, například úlohu naplánovanou v poli **Plánované období** na 18. prosince 2012.</span><span class="sxs-lookup"><span data-stu-id="eaf86-122">Select a job that has the **Planned job** status, for example, a job scheduled on December 18, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="eaf86-123">Poté přesuňte úlohu do dalšího období.</span><span class="sxs-lookup"><span data-stu-id="eaf86-123">Then move the job to the next period.</span></span> 

5. <span data-ttu-id="eaf86-124">Klikněte na **Následující období**.</span><span class="sxs-lookup"><span data-stu-id="eaf86-124">Click **Next period**.</span></span> 

6. <span data-ttu-id="eaf86-125">Klikněte na **Start** pro přesun úlohy na začátek seznamu úloh jako první úlohu v předchozím období.</span><span class="sxs-lookup"><span data-stu-id="eaf86-125">Click **Start** to move the job to the start of the job list as the first job in the previous period.</span></span> 

## <a name="move-a-job-within-a-period"></a><span data-ttu-id="eaf86-126">Přesuňte úlohu v rámci období</span><span class="sxs-lookup"><span data-stu-id="eaf86-126">Move a job within a period.</span></span> 

1. <span data-ttu-id="eaf86-127">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="eaf86-127">In the list, find and select the desired record.</span></span> <span data-ttu-id="eaf86-128">Vyberte úlohu, bude má stav plánované úlohy, například druhou úlohu naplánovanou v poli **Plánované období** na 19. prosince 2012.</span><span class="sxs-lookup"><span data-stu-id="eaf86-128">Select a job that has the Planned job status, for example, the second job scheduled on December 19, 2012 in the **Planned period** field.</span></span> <span data-ttu-id="eaf86-129">Poté přesuňte úlohu v rámci plánovaného období.</span><span class="sxs-lookup"><span data-stu-id="eaf86-129">Then move the job within the planned period.</span></span> 

2. <span data-ttu-id="eaf86-130">Klikněte na **Vpřed**.</span><span class="sxs-lookup"><span data-stu-id="eaf86-130">Click **Forward**.</span></span> <span data-ttu-id="eaf86-131">Všimněte si, že úloha byla přesunuta o jeden řádek v seznamu dolů.</span><span class="sxs-lookup"><span data-stu-id="eaf86-131">Notice that the job is moved one line down on the list.</span></span> 

3. <span data-ttu-id="eaf86-132">Klikněte na **Vzad**.</span><span class="sxs-lookup"><span data-stu-id="eaf86-132">Click **Backward**.</span></span> <span data-ttu-id="eaf86-133">Všimněte si, že úloha byla přesunuta o jeden řádek v seznamu nahoru.</span><span class="sxs-lookup"><span data-stu-id="eaf86-133">Notice that the job is moved one line up on the list.</span></span>
