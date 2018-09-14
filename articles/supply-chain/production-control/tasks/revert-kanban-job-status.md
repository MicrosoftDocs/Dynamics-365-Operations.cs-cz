--- 
title: "Vrátit stav kanbanové úlohy"
description: "Tato procedura se zaměřuje na vrácení zpět nesprávného stavu kanbanové úlohy."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 27874f89cede151b52b869fa0d58e320d548e6d3
ms.contentlocale: cs-cz
ms.lasthandoff: 09/14/2018

---
# <a name="revert-kanban-job-status"></a><span data-ttu-id="cccc2-103">Vrátit stav kanbanové úlohy</span><span class="sxs-lookup"><span data-stu-id="cccc2-103">Revert kanban job status</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cccc2-104">Tato procedura se zaměřuje na vrácení zpět nesprávného stavu kanbanové úlohy.</span><span class="sxs-lookup"><span data-stu-id="cccc2-104">This procedure focuses on reverting an incorrect kanban job status.</span></span> <span data-ttu-id="cccc2-105">To je užitečné v případě, že operátor stroje aktualizuje nesprávné úlohu nebo omylem nastaví nesprávný stav.</span><span class="sxs-lookup"><span data-stu-id="cccc2-105">This is useful in case the machine operator updates the wrong job, or sets the wrong status by mistake.</span></span> <span data-ttu-id="cccc2-106">V tomto postupu kanbanová úloha je registrována jako připravená omylem a stav se vrátí.</span><span class="sxs-lookup"><span data-stu-id="cccc2-106">In this procedure, a kanban job is registered as prepared by mistake, and the status is reverted.</span></span> <span data-ttu-id="cccc2-107">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="cccc2-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="cccc2-108">Tato procedura je určena pro vedoucího dílny nebo operátora stroje pracující ve společnosti s lean manufacturing.</span><span class="sxs-lookup"><span data-stu-id="cccc2-108">This procedure is intended for the shop supervisor or machine operator working in a lean manufacturing company.</span></span>


## <a name="open-process-board-for-the-work-cell"></a><span data-ttu-id="cccc2-109">Otevřít desku procesů pro pracovní buňku</span><span class="sxs-lookup"><span data-stu-id="cccc2-109">Open process board for the work cell</span></span>
1. <span data-ttu-id="cccc2-110">Přejděte na kanbanovou desku pro úlohy procesu.</span><span class="sxs-lookup"><span data-stu-id="cccc2-110">Go to Kanban board for process jobs.</span></span>
2. <span data-ttu-id="cccc2-111">V poli Pracovní buňka zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="cccc2-111">In the Work cell field, enter or select a value.</span></span>
    * <span data-ttu-id="cccc2-112">Vyberte pracovní buňku 1260.</span><span class="sxs-lookup"><span data-stu-id="cccc2-112">Select work cell 1260.</span></span>  

## <a name="prepare-kanban-job"></a><span data-ttu-id="cccc2-113">Připravit kanbanovou úlohu</span><span class="sxs-lookup"><span data-stu-id="cccc2-113">Prepare kanban job</span></span>
1. <span data-ttu-id="cccc2-114">Klepněte na Připravit.</span><span class="sxs-lookup"><span data-stu-id="cccc2-114">Click Prepare.</span></span>
    * <span data-ttu-id="cccc2-115">Pokud nemůžete kliknout na Připravit, protože se možnost zobrazuje šedě, zajistěte, aby vybraná kanbanová úloha měla stav Plánováno, který je označen ikonou prázdného kanbanu.</span><span class="sxs-lookup"><span data-stu-id="cccc2-115">If you can't click Prepare because it is grayed out, make sure that the selected kanban job has status Planned, which is indicated by the empty kanban icon.</span></span> <span data-ttu-id="cccc2-116">Pokud se příprava nezdaří, zkontrolujte, zda jsou všechny materiály k dispozici na výdejce.</span><span class="sxs-lookup"><span data-stu-id="cccc2-116">If Prepare fails, make sure that all materials in the Picking list are available.</span></span>  
2. <span data-ttu-id="cccc2-117">Vyberte připravenou úlohu na seznamu.</span><span class="sxs-lookup"><span data-stu-id="cccc2-117">In the list, select the prepared job.</span></span>
    * <span data-ttu-id="cccc2-118">Vyberte první úlohu, kterou jste právě připravili.</span><span class="sxs-lookup"><span data-stu-id="cccc2-118">Select the first job that you have just prepared.</span></span>  
    * <span data-ttu-id="cccc2-119">Všimněte si, že jsou připraveny úlohy stavu, které jsou označeny trojúhelníkem uvnitř ikony kanbanu.</span><span class="sxs-lookup"><span data-stu-id="cccc2-119">Notice that the jobs status is prepared, which is indicated with a triangle inside the kanban icon.</span></span>  

## <a name="revert-the-status-of-the-prepared-kanban-job"></a><span data-ttu-id="cccc2-120">Vrátit zpět stav připravené kanbanové úlohy</span><span class="sxs-lookup"><span data-stu-id="cccc2-120">Revert the status of the prepared kanban job</span></span>
1. <span data-ttu-id="cccc2-121">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="cccc2-121">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="cccc2-122">Vyberte první úlohu, která byla připravena.</span><span class="sxs-lookup"><span data-stu-id="cccc2-122">Select the first job that was prepared.</span></span>  
2. <span data-ttu-id="cccc2-123">V podokně akcí klikněte na možnost Vyrobit.</span><span class="sxs-lookup"><span data-stu-id="cccc2-123">On the Action Pane, click Manufacture.</span></span>
3. <span data-ttu-id="cccc2-124">Klikněte na Vrátit na stav zpět.</span><span class="sxs-lookup"><span data-stu-id="cccc2-124">Click Revert status.</span></span>
    * <span data-ttu-id="cccc2-125">Můžete vybrat alternativní kanbanové pravidlo při splnění následujících podmínek:  - Strategie doplnění je stejná pro obě pravidla.</span><span class="sxs-lookup"><span data-stu-id="cccc2-125">You can use an alternative kanban rule when the following conditions are true:  - The replenishment strategy is the same for both rules.</span></span>  <span data-ttu-id="cccc2-126">- Verze výrobního toku je stejná pro obě pravidla.</span><span class="sxs-lookup"><span data-stu-id="cccc2-126">- The version of the production flow is the same for both rules.</span></span>  <span data-ttu-id="cccc2-127">- Produkt, který se dodává, je stejný pro obě pravidla.</span><span class="sxs-lookup"><span data-stu-id="cccc2-127">- The product that is supplied is the same for both rules.</span></span>  <span data-ttu-id="cccc2-128">- Všechny podřízené činnosti, které jsou konfigurovány pro poslední aktivitu kanbanových pravidel musí být stejné pro obě pravidla.</span><span class="sxs-lookup"><span data-stu-id="cccc2-128">- Any downstream activities that are configured for the last activity of the kanban rules must be the same for both rules.</span></span>  <span data-ttu-id="cccc2-129">- Stejné zadané dimenze zásob musí být nakonfigurovány pro obě pravidla.</span><span class="sxs-lookup"><span data-stu-id="cccc2-129">- The same supplied inventory dimensions must be configured for both rules.</span></span>  <span data-ttu-id="cccc2-130">- Stav manipulační jednotky musí být Nepřiřazeno.</span><span class="sxs-lookup"><span data-stu-id="cccc2-130">- The status of the handling unit must be Not assigned.</span></span>  <span data-ttu-id="cccc2-131">- Konfigurace pro kanbany událostí se musí shodovat.</span><span class="sxs-lookup"><span data-stu-id="cccc2-131">- The configuration for event kanbans must be the same.</span></span>  
    * <span data-ttu-id="cccc2-132">Ujistěte se, že nový stav je Plánováno.</span><span class="sxs-lookup"><span data-stu-id="cccc2-132">Ensure that the new status is Planned.</span></span>  
4. <span data-ttu-id="cccc2-133">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="cccc2-133">Click OK.</span></span>
5. <span data-ttu-id="cccc2-134">Odznačte vybraný řádek na seznamu.</span><span class="sxs-lookup"><span data-stu-id="cccc2-134">In the list, unmark the selected row.</span></span>
    * <span data-ttu-id="cccc2-135">Vyberte stejnou úlohu.</span><span class="sxs-lookup"><span data-stu-id="cccc2-135">Select the same job.</span></span>  
    * <span data-ttu-id="cccc2-136">Všimněte si, že stav úlohy pro kanbanovou úlohu bude vrácen zpět na Plánováno, což je označeno ikonou prázdného kanbanu.</span><span class="sxs-lookup"><span data-stu-id="cccc2-136">Notice that the job status for the kanban job is reverted to Planned, which is indicated by an empty kanban icon.</span></span>  


