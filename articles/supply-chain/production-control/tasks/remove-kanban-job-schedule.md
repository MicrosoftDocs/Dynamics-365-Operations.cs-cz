--- 
title: "Odebrání kanbanové úlohy z plánu"
description: "Tento postup se zaměřuje na odebrání plánovaného zpracování kanbanové úlohy z plánu pomocí změny stavu úlohy na Neplánováno."
author: ChristianRytt
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
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 9a0f246bfe42dde0befdf5c4f01d2ad1e1200b12
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---
# <a name="remove-a-kanban-job-from-the-schedule"></a><span data-ttu-id="06b27-103">Odebrání kanbanové úlohy z plánu</span><span class="sxs-lookup"><span data-stu-id="06b27-103">Remove a kanban job from the schedule</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="06b27-104">Tento postup se zaměřuje na odebrání plánovaného zpracování kanbanové úlohy z plánu pomocí změny stavu úlohy na Neplánováno.</span><span class="sxs-lookup"><span data-stu-id="06b27-104">This procedure focuses on removing a planned process kanban job from the schedule by reverting the job status to Not planned.</span></span> <span data-ttu-id="06b27-105">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="06b27-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="06b27-106">Tento postup je určen pro dílenského nadřízeného nebo plánovače výroby.</span><span class="sxs-lookup"><span data-stu-id="06b27-106">This procedure is intended for the shop floor supervisor or production planner.</span></span>


## <a name="find-a-planned-kanban-job"></a><span data-ttu-id="06b27-107">Vyhledání plánované kanbanové úlohy</span><span class="sxs-lookup"><span data-stu-id="06b27-107">Find a planned kanban job</span></span>
1. <span data-ttu-id="06b27-108">Přejděte na Řízení výroby > Kanban > Plánování kanbanové úlohy.</span><span class="sxs-lookup"><span data-stu-id="06b27-108">Go to Production control > Kanban > Kanban job scheduling.</span></span>
2. <span data-ttu-id="06b27-109">V poli Pracovní buňka kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="06b27-109">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="06b27-110">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="06b27-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="06b27-111">Vyberte pracovní buňku 1250.</span><span class="sxs-lookup"><span data-stu-id="06b27-111">Select work cell 1250.</span></span>  
4. <span data-ttu-id="06b27-112">Klepněte na tlačítko Vybrat.</span><span class="sxs-lookup"><span data-stu-id="06b27-112">Click Select.</span></span>
5. <span data-ttu-id="06b27-113">V poli Zobrazit stav úlohy vyberte hodnotu Plánováno.</span><span class="sxs-lookup"><span data-stu-id="06b27-113">In the Display job status field, select 'Scheduled'.</span></span>

## <a name="remove-the-planned-kanban-job-from-the-schedule"></a><span data-ttu-id="06b27-114">Odebrání plánované kanbanové úlohy z plánu</span><span class="sxs-lookup"><span data-stu-id="06b27-114">Remove the planned kanban job from the schedule</span></span>
1. <span data-ttu-id="06b27-115">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="06b27-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="06b27-116">Vyberte úlohu se stavem Plánováno, například práci ze dne 19. prosince 2012.</span><span class="sxs-lookup"><span data-stu-id="06b27-116">Select a job that has the Planned status, for example, a job from December 19, 2012.</span></span>  
2. <span data-ttu-id="06b27-117">V podokně akcí klikněte na položku Plán.</span><span class="sxs-lookup"><span data-stu-id="06b27-117">On the Action Pane, click Plan.</span></span>
3. <span data-ttu-id="06b27-118">Klikněte na Vrátit stav úlohy.</span><span class="sxs-lookup"><span data-stu-id="06b27-118">Click Revert job status.</span></span>
4. <span data-ttu-id="06b27-119">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="06b27-119">Click OK.</span></span>
    * <span data-ttu-id="06b27-120">Tím vrátíte aktuální stav úlohy ze stavu Plánováno na Neplánováno a odeberete ji z panelu procesů.</span><span class="sxs-lookup"><span data-stu-id="06b27-120">This will revert the current job status from 'Planned' to 'Not planned' and remove it from the process board.</span></span>   


