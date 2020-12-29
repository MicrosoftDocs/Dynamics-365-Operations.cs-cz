---
title: Změna kanbanových pravidel pro úlohu procesu
description: Tato procedura se zaměřuje na změnu použitého kanbanového pravidla pro daný kanban.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, KanbanJobSchedulingListPage, LeanRuleReassignmentWizard, KanbanReassignRuleLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4d4c8fd8251aca2cc53e59afe4c104f2e5198426
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423543"
---
# <a name="change-kanban-rules-for-a-process-job"></a><span data-ttu-id="02ecd-103">Změna kanbanových pravidel pro úlohu procesu</span><span class="sxs-lookup"><span data-stu-id="02ecd-103">Change kanban rules for a process job</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="02ecd-104">Tato procedura se zaměřuje na změnu použitého kanbanového pravidla pro daný kanban.</span><span class="sxs-lookup"><span data-stu-id="02ecd-104">This procedure focuses on changing the used kanban rule for a given kanban.</span></span> <span data-ttu-id="02ecd-105">To je užitečné pro nastavení úrovní prostředků vytížení nebo v případě rozúčtování.</span><span class="sxs-lookup"><span data-stu-id="02ecd-105">This is useful to level load resources or in case of breakdown.</span></span> <span data-ttu-id="02ecd-106">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="02ecd-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="02ecd-107">Tato procedura je určena pro plánovače, který pracuje ve společnosti se štíhlou výrobou a odpovídá za hodnotový proud.</span><span class="sxs-lookup"><span data-stu-id="02ecd-107">This procedure is intended for the planner, working at a lean manufacturing company, responsible for the value stream.</span></span>


## <a name="copy-kanban-rule"></a><span data-ttu-id="02ecd-108">Zkopírujte kanbanové pravidlo</span><span class="sxs-lookup"><span data-stu-id="02ecd-108">Copy kanban rule</span></span>
1. <span data-ttu-id="02ecd-109">Otevřete Kanbanová pravidla.</span><span class="sxs-lookup"><span data-stu-id="02ecd-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="02ecd-110">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="02ecd-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="02ecd-111">Vyberte Kanbanové pravidlo události 000022 pro L0001.</span><span class="sxs-lookup"><span data-stu-id="02ecd-111">Select Event Kanban rule 000022 for L0001.</span></span>  
3. <span data-ttu-id="02ecd-112">Klepněte na Duplicitní kanbanové pravidlo.</span><span class="sxs-lookup"><span data-stu-id="02ecd-112">Click Duplicate kanban rule.</span></span>
4. <span data-ttu-id="02ecd-113">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="02ecd-113">Click OK.</span></span>

## <a name="change-kanban-rule"></a><span data-ttu-id="02ecd-114">Změňte kanbanové pravidlo</span><span class="sxs-lookup"><span data-stu-id="02ecd-114">Change kanban rule</span></span>
1. <span data-ttu-id="02ecd-115">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="02ecd-115">Close the page.</span></span>
2. <span data-ttu-id="02ecd-116">Přejděte na Plánování kanbanové úlohy.</span><span class="sxs-lookup"><span data-stu-id="02ecd-116">Go to Kanban job scheduling.</span></span>
3. <span data-ttu-id="02ecd-117">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="02ecd-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="02ecd-118">Vyberte řádek s kanbanem 000177.</span><span class="sxs-lookup"><span data-stu-id="02ecd-118">Select line with Kanban 000177.</span></span>  
4. <span data-ttu-id="02ecd-119">Klikněte na Použít alternativní kanbanové pravidlo.</span><span class="sxs-lookup"><span data-stu-id="02ecd-119">Click Use alternative kanban rule.</span></span>
5. <span data-ttu-id="02ecd-120">Klepněte na tlačítko Další.</span><span class="sxs-lookup"><span data-stu-id="02ecd-120">Click Next.</span></span>
6. <span data-ttu-id="02ecd-121">V poli Kanbanové pravidlo zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="02ecd-121">In the Kanban rule field, enter or select a value.</span></span>
    * <span data-ttu-id="02ecd-122">Vyberte kanbanové pravidlo, které bylo vytvořeno dříve.</span><span class="sxs-lookup"><span data-stu-id="02ecd-122">Select the kanban rule that was created earlier.</span></span> <span data-ttu-id="02ecd-123">Jedná se o kanbanové pravidlo s nejvyšším číslem.</span><span class="sxs-lookup"><span data-stu-id="02ecd-123">This is the kanban rule with the highest number.</span></span>  
7. <span data-ttu-id="02ecd-124">Klepněte na tlačítko Dokončit.</span><span class="sxs-lookup"><span data-stu-id="02ecd-124">Click Finish.</span></span>
    * <span data-ttu-id="02ecd-125">Kanbanová úloha používá jiné kanbanové pravidlo.</span><span class="sxs-lookup"><span data-stu-id="02ecd-125">Now the kanban job is using an another kanban rule.</span></span> <span data-ttu-id="02ecd-126">To může být užitečné na úrovni pracovních buněk vytížení.</span><span class="sxs-lookup"><span data-stu-id="02ecd-126">This can be useful to level load work cells.</span></span>  

