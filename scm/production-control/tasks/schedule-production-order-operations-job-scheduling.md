--- 
title: "Naplánování výrobní zakázky s naplánováním operací a úloh"
description: "Tento postup je zaměřen na plánování výrobní zakázky pomocí plánování operací a úloh."
author: ChristianRytt
manager: AnnBe
ms.date: 10/27/2016
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
ms.openlocfilehash: d4aac437876862e9f776264fc81f246c820bdf45
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a><span data-ttu-id="8c4fb-103">Naplánování výrobní zakázky s naplánováním operací a úloh</span><span class="sxs-lookup"><span data-stu-id="8c4fb-103">Schedule a production order with operations and job scheduling</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8c4fb-104">Tento postup je zaměřen na plánování výrobní zakázky pomocí plánování operací a úloh.</span><span class="sxs-lookup"><span data-stu-id="8c4fb-104">This procedure focuses on scheduling a production order with operations scheduling and job scheduling.</span></span> <span data-ttu-id="8c4fb-105">Žádné úlohy se při plánování operací nevytváří, zatímco při plánování úloh se úlohy vytváří.</span><span class="sxs-lookup"><span data-stu-id="8c4fb-105">No jobs are created with operations scheduling whereas jobs are created with job scheduling.</span></span> <span data-ttu-id="8c4fb-106">Tento úkol byl vytvořen pomocí ukázkových dat společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="8c4fb-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="8c4fb-107">Tento postup je určen pro vedoucí výroby, výrobní plánovače nebo dílenského vedoucího pracujícího v samostatném výrobním prostředí.</span><span class="sxs-lookup"><span data-stu-id="8c4fb-107">This procedure is intended for the production manager, production planner, or shop floor supervisor working in a discrete manufacturing environment.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="8c4fb-108">Vytvoření výrobní zakázky</span><span class="sxs-lookup"><span data-stu-id="8c4fb-108">Create a production order</span></span>
1. <span data-ttu-id="8c4fb-109">Přejděte na Řízení výroby > Výrobní zakázky > Všechny výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="8c4fb-109">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="8c4fb-110">Klikněte na možnost Nová výrobní zakázka.</span><span class="sxs-lookup"><span data-stu-id="8c4fb-110">Click New production order.</span></span>
3. <span data-ttu-id="8c4fb-111">V poli Číslo zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="8c4fb-111">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="8c4fb-112">Vyberte číslo položky D0001.</span><span class="sxs-lookup"><span data-stu-id="8c4fb-112">Select Item number D0001.</span></span>  
4. <span data-ttu-id="8c4fb-113">Klikněte na položku Vytvořit.</span><span class="sxs-lookup"><span data-stu-id="8c4fb-113">Click Create.</span></span>

## <a name="schedule-operations-for-the-production-order"></a><span data-ttu-id="8c4fb-114">Naplánování operací pro výrobní zakázku</span><span class="sxs-lookup"><span data-stu-id="8c4fb-114">Schedule operations for the production order</span></span>
1. <span data-ttu-id="8c4fb-115">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="8c4fb-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="8c4fb-116">Vyberte výrobní zakázku, kterou jste právě vytvořili.</span><span class="sxs-lookup"><span data-stu-id="8c4fb-116">Select the production order that you have just created.</span></span> <span data-ttu-id="8c4fb-117">Měla by být v horní části seznamu.</span><span class="sxs-lookup"><span data-stu-id="8c4fb-117">It should be at the top of the list.</span></span>      
2. <span data-ttu-id="8c4fb-118">V podokně akcí klikněte na možnost Plán.</span><span class="sxs-lookup"><span data-stu-id="8c4fb-118">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="8c4fb-119">Klikněte na Plánovat operace.</span><span class="sxs-lookup"><span data-stu-id="8c4fb-119">Click Schedule operations.</span></span>
4. <span data-ttu-id="8c4fb-120">V poli Způsob plánování vyberte „Dopředu od data plánování“.</span><span class="sxs-lookup"><span data-stu-id="8c4fb-120">In the Scheduling direction field, select 'Forward from scheduling date'.</span></span>
5. <span data-ttu-id="8c4fb-121">Do pole Datum plánování zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="8c4fb-121">In the Scheduling date field, enter a date.</span></span>
    * <span data-ttu-id="8c4fb-122">Vyberte budoucí datum (například dnešní datum plus jeden týden).</span><span class="sxs-lookup"><span data-stu-id="8c4fb-122">Select a future date, for example, today plus one week.</span></span> <span data-ttu-id="8c4fb-123">Po výběru možnosti Způsob plánování bude výrobní zakázka naplánována vpřed od tohoto data.</span><span class="sxs-lookup"><span data-stu-id="8c4fb-123">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
6. <span data-ttu-id="8c4fb-124">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="8c4fb-124">Click OK.</span></span>
7. <span data-ttu-id="8c4fb-125">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="8c4fb-125">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="8c4fb-126">Všimněte si, že se stav změní na Plánováno.</span><span class="sxs-lookup"><span data-stu-id="8c4fb-126">Note that the status is changed to Scheduled.</span></span>  
8. <span data-ttu-id="8c4fb-127">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="8c4fb-127">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="8c4fb-128">Klikněte na Všechny úlohy.</span><span class="sxs-lookup"><span data-stu-id="8c4fb-128">Click All jobs.</span></span>
    * <span data-ttu-id="8c4fb-129">Všimněte si, že se nevytvoří žádné úlohy při plánování operací.</span><span class="sxs-lookup"><span data-stu-id="8c4fb-129">Note that no jobs are created with operations scheduling.</span></span>  
10. <span data-ttu-id="8c4fb-130">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="8c4fb-130">Close the page.</span></span>

## <a name="schedule-jobs-for-the-production-order"></a><span data-ttu-id="8c4fb-131">Naplánování úloh pro výrobní zakázku</span><span class="sxs-lookup"><span data-stu-id="8c4fb-131">Schedule jobs for the production order</span></span>
1. <span data-ttu-id="8c4fb-132">V podokně akcí klikněte na možnost Plán.</span><span class="sxs-lookup"><span data-stu-id="8c4fb-132">On the Action Pane, click Schedule.</span></span>
2. <span data-ttu-id="8c4fb-133">Klikněte na Plánovat úlohy.</span><span class="sxs-lookup"><span data-stu-id="8c4fb-133">Click Schedule jobs.</span></span>
3. <span data-ttu-id="8c4fb-134">V poli Způsob plánování vyberte „Dopředu od data plánování“.</span><span class="sxs-lookup"><span data-stu-id="8c4fb-134">In the Scheduling direction field, select 'Forward from scheduling date'.</span></span>
4. <span data-ttu-id="8c4fb-135">Do pole Datum plánování zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="8c4fb-135">In the Scheduling date field, enter a date.</span></span>
    * <span data-ttu-id="8c4fb-136">Vyberte budoucí datum (například dnešní datum plus jeden týden).</span><span class="sxs-lookup"><span data-stu-id="8c4fb-136">Select a date in the future, for example, today plus one week.</span></span> <span data-ttu-id="8c4fb-137">Po výběru možnosti Způsob plánování bude výrobní zakázka naplánována vpřed od tohoto data.</span><span class="sxs-lookup"><span data-stu-id="8c4fb-137">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
5. <span data-ttu-id="8c4fb-138">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="8c4fb-138">Click OK.</span></span>
6. <span data-ttu-id="8c4fb-139">V podokně akcí klikněte na položku Výrobní zakázka.</span><span class="sxs-lookup"><span data-stu-id="8c4fb-139">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="8c4fb-140">Klikněte na Všechny úlohy.</span><span class="sxs-lookup"><span data-stu-id="8c4fb-140">Click All jobs.</span></span>
    * <span data-ttu-id="8c4fb-141">Všimněte si, že na základě aktivní trasy je vytvořeno 5 úloh s plánováním úlohy.</span><span class="sxs-lookup"><span data-stu-id="8c4fb-141">Note that based on the active route, 5 jobs are created with job scheduling.</span></span>  


