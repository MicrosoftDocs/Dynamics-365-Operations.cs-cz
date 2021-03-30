---
title: Odebrání kanbanové úlohy z plánu
description: Tento postup se zaměřuje na odebrání plánovaného zpracování kanbanové úlohy z plánu pomocí změny stavu úlohy na Neplánováno.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanJobSchedulingListPage, SysLookupMultiSelectGrid, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 566a174c631391577441e0f890bd9553dac0891c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5204513"
---
# <a name="remove-a-kanban-job-from-the-schedule"></a><span data-ttu-id="abac7-103">Odebrání kanbanové úlohy z plánu</span><span class="sxs-lookup"><span data-stu-id="abac7-103">Remove a kanban job from the schedule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="abac7-104">Tento postup se zaměřuje na odebrání plánovaného zpracování kanbanové úlohy z plánu pomocí změny stavu úlohy na Neplánováno.</span><span class="sxs-lookup"><span data-stu-id="abac7-104">This procedure focuses on removing a planned process kanban job from the schedule by reverting the job status to Not planned.</span></span> <span data-ttu-id="abac7-105">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="abac7-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="abac7-106">Tento postup je určen pro dílenského nadřízeného nebo plánovače výroby.</span><span class="sxs-lookup"><span data-stu-id="abac7-106">This procedure is intended for the shop floor supervisor or production planner.</span></span>


## <a name="find-a-planned-kanban-job"></a><span data-ttu-id="abac7-107">Vyhledání plánované kanbanové úlohy</span><span class="sxs-lookup"><span data-stu-id="abac7-107">Find a planned kanban job</span></span>
1. <span data-ttu-id="abac7-108">Přejděte na Řízení výroby > Kanban > Plánování kanbanové úlohy.</span><span class="sxs-lookup"><span data-stu-id="abac7-108">Go to Production control > Kanban > Kanban job scheduling.</span></span>
2. <span data-ttu-id="abac7-109">V poli Pracovní buňka kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="abac7-109">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="abac7-110">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="abac7-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="abac7-111">Vyberte pracovní buňku 1250.</span><span class="sxs-lookup"><span data-stu-id="abac7-111">Select work cell 1250.</span></span>  
4. <span data-ttu-id="abac7-112">Klepněte na tlačítko Vybrat.</span><span class="sxs-lookup"><span data-stu-id="abac7-112">Click Select.</span></span>
5. <span data-ttu-id="abac7-113">V poli Zobrazit stav úlohy vyberte hodnotu Plánováno.</span><span class="sxs-lookup"><span data-stu-id="abac7-113">In the Display job status field, select 'Scheduled'.</span></span>

## <a name="remove-the-planned-kanban-job-from-the-schedule"></a><span data-ttu-id="abac7-114">Odebrání plánované kanbanové úlohy z plánu</span><span class="sxs-lookup"><span data-stu-id="abac7-114">Remove the planned kanban job from the schedule</span></span>
1. <span data-ttu-id="abac7-115">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="abac7-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="abac7-116">Vyberte úlohu se stavem Plánováno, například práci ze dne 19. prosince 2012.</span><span class="sxs-lookup"><span data-stu-id="abac7-116">Select a job that has the Planned status, for example, a job from December 19, 2012.</span></span>  
2. <span data-ttu-id="abac7-117">V podokně akcí klikněte na položku Plán.</span><span class="sxs-lookup"><span data-stu-id="abac7-117">On the Action Pane, click Plan.</span></span>
3. <span data-ttu-id="abac7-118">Klikněte na Vrátit stav úlohy.</span><span class="sxs-lookup"><span data-stu-id="abac7-118">Click Revert job status.</span></span>
4. <span data-ttu-id="abac7-119">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="abac7-119">Click OK.</span></span>
    * <span data-ttu-id="abac7-120">Tím vrátíte aktuální stav úlohy ze stavu Plánováno na Neplánováno a odeberete ji z panelu procesů.</span><span class="sxs-lookup"><span data-stu-id="abac7-120">This will revert the current job status from 'Planned' to 'Not planned' and remove it from the process board.</span></span>   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]