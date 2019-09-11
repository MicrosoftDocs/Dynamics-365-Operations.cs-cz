---
title: Naplánování výrobní zakázky s naplánováním operací a úloh
description: Toto téma je zaměřeno na plánování výrobní zakázky pomocí plánování operací a úloh.
author: ChristianRytt
manager: AnnBe
ms.date: 08/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdSchedule, ProdTable, ProdRouteJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3023d6a6fe09c84b47839a2c4b78c37907754ded
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914877"
---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a><span data-ttu-id="9ddfc-103">Naplánování výrobní zakázky s naplánováním operací a úloh</span><span class="sxs-lookup"><span data-stu-id="9ddfc-103">Schedule a production order with operations and job scheduling</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9ddfc-104">Toto téma je zaměřeno na plánování výrobní zakázky pomocí plánování operací a úloh.</span><span class="sxs-lookup"><span data-stu-id="9ddfc-104">This topic focuses on scheduling a production order with operations scheduling and job scheduling.</span></span> <span data-ttu-id="9ddfc-105">Žádné úlohy se při plánování operací nevytváří, zatímco při plánování úloh se úlohy vytváří.</span><span class="sxs-lookup"><span data-stu-id="9ddfc-105">No jobs are created with operations scheduling whereas jobs are created with job scheduling.</span></span> <span data-ttu-id="9ddfc-106">Tento úkol byl vytvořen pomocí ukázkových dat společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="9ddfc-106">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="9ddfc-107">Tento postup je určen pro vedoucí výroby, výrobní plánovače nebo dílenského vedoucího pracujícího v samostatném výrobním prostředí.</span><span class="sxs-lookup"><span data-stu-id="9ddfc-107">This procedure is intended for the production manager, production planner, or shop floor supervisor working in a discrete manufacturing environment.</span></span>


## <a name="create-a-production-order"></a><span data-ttu-id="9ddfc-108">Vytvoření výrobní zakázky</span><span class="sxs-lookup"><span data-stu-id="9ddfc-108">Create a production order</span></span>
1. <span data-ttu-id="9ddfc-109">V navigačním podokně přejděte na **Moduly > Řízení výroby > Výrobní zakázky > Všechny výrobní zakázky**.</span><span class="sxs-lookup"><span data-stu-id="9ddfc-109">In the navigation pane, go to **Modules > Production control > Production orders > All production orders**.</span></span>
2. <span data-ttu-id="9ddfc-110">Vyberte **Nová výrobní zakázka**.</span><span class="sxs-lookup"><span data-stu-id="9ddfc-110">Select **New production order**.</span></span>
3. <span data-ttu-id="9ddfc-111">V poli **Číslo položky** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="9ddfc-111">In the **Item number** field, enter or select a value.</span></span> <span data-ttu-id="9ddfc-112">Vyberte číslo položky **D0001**.</span><span class="sxs-lookup"><span data-stu-id="9ddfc-112">Select Item number **D0001**.</span></span>  
4. <span data-ttu-id="9ddfc-113">Vyberte **Vytvořit**.</span><span class="sxs-lookup"><span data-stu-id="9ddfc-113">Select **Create**.</span></span>

## <a name="schedule-operations-for-the-production-order"></a><span data-ttu-id="9ddfc-114">Naplánování operací pro výrobní zakázku</span><span class="sxs-lookup"><span data-stu-id="9ddfc-114">Schedule operations for the production order</span></span>
1. <span data-ttu-id="9ddfc-115">Označte nově vytvořený řádek.</span><span class="sxs-lookup"><span data-stu-id="9ddfc-115">Mark the newly created row.</span></span>      
2. <span data-ttu-id="9ddfc-116">V podokně akcí vyberte možnost **Plánovat**.</span><span class="sxs-lookup"><span data-stu-id="9ddfc-116">On the Action Pane, select **Schedule**.</span></span>
3. <span data-ttu-id="9ddfc-117">Vyberte **Plánovat operace**.</span><span class="sxs-lookup"><span data-stu-id="9ddfc-117">Select **Schedule operations**.</span></span>
4. <span data-ttu-id="9ddfc-118">V poli **Způsob plánování** vyberte **Dopředu od data plánování**.</span><span class="sxs-lookup"><span data-stu-id="9ddfc-118">In the **Scheduling direction** field, select **Forward from scheduling date**.</span></span>
5. <span data-ttu-id="9ddfc-119">Do pole **Datum plánování** zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="9ddfc-119">In the **Scheduling date** field, enter a date.</span></span> <span data-ttu-id="9ddfc-120">Vyberte budoucí datum (například dnešní datum plus jeden týden).</span><span class="sxs-lookup"><span data-stu-id="9ddfc-120">Select a future date, for example, today plus one week.</span></span> <span data-ttu-id="9ddfc-121">Po výběru možnosti Způsob plánování bude výrobní zakázka naplánována vpřed od tohoto data.</span><span class="sxs-lookup"><span data-stu-id="9ddfc-121">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
6. <span data-ttu-id="9ddfc-122">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="9ddfc-122">Select **OK**.</span></span>
7. <span data-ttu-id="9ddfc-123">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="9ddfc-123">In the list, mark the selected row.</span></span> <span data-ttu-id="9ddfc-124">Všimněte si, že se stav změní na **Plánováno**.</span><span class="sxs-lookup"><span data-stu-id="9ddfc-124">Note that the status is changed to **Scheduled**.</span></span> 
8. <span data-ttu-id="9ddfc-125">Vyberte **Všechny úlohy**.</span><span class="sxs-lookup"><span data-stu-id="9ddfc-125">Select **All jobs**.</span></span> <span data-ttu-id="9ddfc-126">Všimněte si, že se nevytvoří žádné úlohy při plánování operací.</span><span class="sxs-lookup"><span data-stu-id="9ddfc-126">Note that no jobs are created with operations scheduling.</span></span>  
9. <span data-ttu-id="9ddfc-127">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="9ddfc-127">Close the page.</span></span>

## <a name="schedule-jobs-for-the-production-order"></a><span data-ttu-id="9ddfc-128">Naplánování úloh pro výrobní zakázku</span><span class="sxs-lookup"><span data-stu-id="9ddfc-128">Schedule jobs for the production order</span></span>
1. <span data-ttu-id="9ddfc-129">V podokně akcí vyberte možnost **Plánovat**.</span><span class="sxs-lookup"><span data-stu-id="9ddfc-129">On the Action Pane, select **Schedule**.</span></span>
2. <span data-ttu-id="9ddfc-130">Vyberte **Plánovat úlohy**.</span><span class="sxs-lookup"><span data-stu-id="9ddfc-130">Select **Schedule jobs**.</span></span>
3. <span data-ttu-id="9ddfc-131">V poli **Způsob plánování** vyberte **Dopředu od data plánování**.</span><span class="sxs-lookup"><span data-stu-id="9ddfc-131">In the **Scheduling direction** field, select **Forward from scheduling date**.</span></span>
4. <span data-ttu-id="9ddfc-132">Do pole **Datum plánování** zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="9ddfc-132">In the **Scheduling date** field, enter a date.</span></span> <span data-ttu-id="9ddfc-133">Vyberte budoucí datum (například dnešní datum plus jeden týden).</span><span class="sxs-lookup"><span data-stu-id="9ddfc-133">Select a date in the future, for example, today plus one week.</span></span> <span data-ttu-id="9ddfc-134">Po výběru možnosti Způsob plánování bude výrobní zakázka naplánována vpřed od tohoto data.</span><span class="sxs-lookup"><span data-stu-id="9ddfc-134">With the selected Scheduling direction, the production order will be scheduled forward from this date.</span></span>  
5. <span data-ttu-id="9ddfc-135">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="9ddfc-135">Select **OK**.</span></span>
6. <span data-ttu-id="9ddfc-136">V podokně akcí vyberte možnost **Výrobní zakázka**.</span><span class="sxs-lookup"><span data-stu-id="9ddfc-136">On the Action Pane, select **Production order**.</span></span>
7. <span data-ttu-id="9ddfc-137">Vyberte **Všechny úlohy**.</span><span class="sxs-lookup"><span data-stu-id="9ddfc-137">Select **All jobs**.</span></span> <span data-ttu-id="9ddfc-138">Všimněte si, že na základě aktivní trasy je vytvořeno 5 úloh s plánováním úlohy.</span><span class="sxs-lookup"><span data-stu-id="9ddfc-138">Note that based on the active route, 5 jobs are created with job scheduling.</span></span>  

