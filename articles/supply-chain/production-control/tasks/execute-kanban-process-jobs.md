---
title: Provádění úloh kanbanových procesů
description: Tento postup se zaměřuje na realizaci úloh kanbanových procesů.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a1c32b577007c400f3528a110436eb97aaabefe2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423860"
---
# <a name="execute-kanban-process-jobs"></a><span data-ttu-id="90dd7-103">Provádění úloh kanbanových procesů</span><span class="sxs-lookup"><span data-stu-id="90dd7-103">Execute kanban process jobs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="90dd7-104">Tento postup se zaměřuje na realizaci úloh kanbanových procesů.</span><span class="sxs-lookup"><span data-stu-id="90dd7-104">This procedure focuses on executing kanban process jobs.</span></span> <span data-ttu-id="90dd7-105">První úloha je dokončena s očekávaným množstvím a bez chyb.</span><span class="sxs-lookup"><span data-stu-id="90dd7-105">The first job is completed with the expected quantity and has no errors.</span></span> <span data-ttu-id="90dd7-106">Druhá úloha je dokončena s chybami.</span><span class="sxs-lookup"><span data-stu-id="90dd7-106">The second job is completed with errors.</span></span> <span data-ttu-id="90dd7-107">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="90dd7-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="90dd7-108">Tento postup je určen pro operátora stroje.</span><span class="sxs-lookup"><span data-stu-id="90dd7-108">This procedure is intended for the machine operator.</span></span>


## <a name="select-a-kanban-job"></a><span data-ttu-id="90dd7-109">Vyberte kanbanovou úlohu.</span><span class="sxs-lookup"><span data-stu-id="90dd7-109">Select a kanban job</span></span>
1. <span data-ttu-id="90dd7-110">Přejděte na Řízení výroby > Kanban > Kanbanová deska pro úlohy zpracování.</span><span class="sxs-lookup"><span data-stu-id="90dd7-110">Go to Production control > Kanban > Kanban board for process jobs.</span></span>
2. <span data-ttu-id="90dd7-111">V poli Pracovní buňka kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="90dd7-111">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="90dd7-112">Klepněte na řádek se skupinou prostředků 1250.</span><span class="sxs-lookup"><span data-stu-id="90dd7-112">Click the row with resource group 1250.</span></span> <span data-ttu-id="90dd7-113">To způsobí filtrování seznamu úloh a zobrazíte tak pouze úlohy pro pracovní buňku 1250.</span><span class="sxs-lookup"><span data-stu-id="90dd7-113">This filters the Jobs list to display only the jobs for work cell 1250.</span></span>
    * <span data-ttu-id="90dd7-114">Označte řádek, který má stav plánované úlohy.</span><span class="sxs-lookup"><span data-stu-id="90dd7-114">Mark the row that has the Planned job status.</span></span>  

## <a name="complete-a-job-with-expected-quantity"></a><span data-ttu-id="90dd7-115">Dokončení úlohy s očekávaným množstvím</span><span class="sxs-lookup"><span data-stu-id="90dd7-115">Complete a job with expected quantity</span></span>
1. <span data-ttu-id="90dd7-116">Rozbalte nebo sbalte oddíl Podrobnosti.</span><span class="sxs-lookup"><span data-stu-id="90dd7-116">Expand or collapse the Details section.</span></span>
    * <span data-ttu-id="90dd7-117">Tento oddíl uvádí důležité informace o číslu karty, číslu položky, objednaném množství a názvu aktivity.</span><span class="sxs-lookup"><span data-stu-id="90dd7-117">This section displays important information about card number, item number, quantity ordered, and activity name.</span></span>  
2. <span data-ttu-id="90dd7-118">Rozbalte nebo sbalte oddíl Pokyny pro výrobu.</span><span class="sxs-lookup"><span data-stu-id="90dd7-118">Expand or collapse the Production instructions section.</span></span>
    * <span data-ttu-id="90dd7-119">Tyto pokyny popisují výrobní pokyny pro aktivitu.</span><span class="sxs-lookup"><span data-stu-id="90dd7-119">This section displays production instructions for the activity.</span></span> <span data-ttu-id="90dd7-120">Pokyny mohou být text, obrázky, výkresy nebo další dokumenty.</span><span class="sxs-lookup"><span data-stu-id="90dd7-120">The instructions can be text, pictures, drawings, and other documents.</span></span>  
3. <span data-ttu-id="90dd7-121">Klikněte na položku Spustit.</span><span class="sxs-lookup"><span data-stu-id="90dd7-121">Click Start.</span></span>
    * <span data-ttu-id="90dd7-122">Vyberte úlohu, která není dokončena.</span><span class="sxs-lookup"><span data-stu-id="90dd7-122">Select a job that is not completed.</span></span> <span data-ttu-id="90dd7-123">Pomocí ikony Stav v poli Stav úlohy můžete zobrazit stav úlohy.</span><span class="sxs-lookup"><span data-stu-id="90dd7-123">Use status icons in the Job status field to view job status.</span></span>      
4. <span data-ttu-id="90dd7-124">Klikněte na tlačítko Dokončit.</span><span class="sxs-lookup"><span data-stu-id="90dd7-124">Click Complete.</span></span>
    * <span data-ttu-id="90dd7-125">Dokončení úlohy proběhne s očekávanou kvalitou.</span><span class="sxs-lookup"><span data-stu-id="90dd7-125">The job is completed with the expected quality.</span></span>  

## <a name="complete-a-job-with-errors"></a><span data-ttu-id="90dd7-126">Dokončení úlohy s chybami</span><span class="sxs-lookup"><span data-stu-id="90dd7-126">Complete a job with errors</span></span>
1. <span data-ttu-id="90dd7-127">Klikněte na položku Spustit.</span><span class="sxs-lookup"><span data-stu-id="90dd7-127">Click Start.</span></span>
    * <span data-ttu-id="90dd7-128">Po dokončení úlohy se automaticky vybere následující úloha v seznamu.</span><span class="sxs-lookup"><span data-stu-id="90dd7-128">When a job is completed, the next job on the list is selected automatically.</span></span> <span data-ttu-id="90dd7-129">Z tohoto důvodu nemusíte vybírat úlohu před klepnutím na tlačítko Spustit.</span><span class="sxs-lookup"><span data-stu-id="90dd7-129">This is why you don't need to select a job before you click Start.</span></span>  
2. <span data-ttu-id="90dd7-130">V podokně akcí klikněte na možnost Vyrobit.</span><span class="sxs-lookup"><span data-stu-id="90dd7-130">On the Action Pane, click Manufacture.</span></span>
3. <span data-ttu-id="90dd7-131">Klikněte na Dokončení (podrobnosti).</span><span class="sxs-lookup"><span data-stu-id="90dd7-131">Click Complete (details).</span></span>
4. <span data-ttu-id="90dd7-132">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="90dd7-132">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="90dd7-133">V poli Chyba v množství zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="90dd7-133">In the Error quantity field, enter a number.</span></span>
6. <span data-ttu-id="90dd7-134">V poli Bezchybné množství zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="90dd7-134">In the Good quantity field, enter a number.</span></span>
7. <span data-ttu-id="90dd7-135">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="90dd7-135">Click OK.</span></span>

