---
title: Vytvoření kanbanového pravidla pro více aktivit
description: Tento postup popisuje, jak vytvořit kanbanové pravidlo, které zahrnuje více aktivit z výrobního toku.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, KanbanFlowSelection, InventItemIdLookupSimple, KanbanCreateScheduled, Kanban
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bcf507611d7f85800b2012e8372d5f91bbc8d724
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255173"
---
# <a name="create-a-kanban-rule-for-multiple-activities"></a><span data-ttu-id="9851b-103">Vytvoření kanbanového pravidla pro více aktivit</span><span class="sxs-lookup"><span data-stu-id="9851b-103">Create a kanban rule for multiple activities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9851b-104">Tento postup popisuje, jak vytvořit kanbanové pravidlo, které zahrnuje více aktivit z výrobního toku.</span><span class="sxs-lookup"><span data-stu-id="9851b-104">This procedure shows how to create a kanban rule that includes multiple activities from a production flow.</span></span> <span data-ttu-id="9851b-105">Tento úkol byl vytvořen pomocí ukázkových dat společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="9851b-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="9851b-106">Tento úkol je určen pro technologa výrobních procesů nebo správce hodnotového proudu, kteří připravují výrobu nového nebo změněného výrobku v prostředí štíhlé výroby.</span><span class="sxs-lookup"><span data-stu-id="9851b-106">This task is intended for the process engineer or the value stream manager, as they prepare production of a new or modified product in a lean environment.</span></span>


## <a name="create-a-new-kanban-rule"></a><span data-ttu-id="9851b-107">Vytvořit nové kanbanové pravidlo</span><span class="sxs-lookup"><span data-stu-id="9851b-107">Create a new kanban rule</span></span>
1. <span data-ttu-id="9851b-108">Přejděte k Řízení informací o produktech > Lean manufacturing > Kanbanová pravidla.</span><span class="sxs-lookup"><span data-stu-id="9851b-108">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="9851b-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="9851b-109">Click New.</span></span>
3. <span data-ttu-id="9851b-110">V poli Strategie doplnění vyberte „Plánováno“.</span><span class="sxs-lookup"><span data-stu-id="9851b-110">In the Replenishment strategy field, select 'Scheduled'.</span></span>
4. <span data-ttu-id="9851b-111">V poli První aktivita plánu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="9851b-111">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="9851b-112">Vyberte možnost SpeakerAssemblyAndPolish.</span><span class="sxs-lookup"><span data-stu-id="9851b-112">Select SpeakerAssemblyAndPolish.</span></span>  
5. <span data-ttu-id="9851b-113">Označte pole Více aktivit.</span><span class="sxs-lookup"><span data-stu-id="9851b-113">Select the Multiple activities check box.</span></span>
    * <span data-ttu-id="9851b-114">Cílem je zahrnout více než jednu aktivitu v kanbanovém pravidle.</span><span class="sxs-lookup"><span data-stu-id="9851b-114">The purpose is to include more than one activity in the kanban rule.</span></span> <span data-ttu-id="9851b-115">Cestu ve výrobním toku zvolíte při výběru poslední aktivity plánu.</span><span class="sxs-lookup"><span data-stu-id="9851b-115">You choose a path in the production flow when you select the last plan activity.</span></span>  
6. <span data-ttu-id="9851b-116">V poli Poslední aktivita plánu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="9851b-116">In the Last plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="9851b-117">Vyberte hodnotu „SpeakerTestAndPackaging“.</span><span class="sxs-lookup"><span data-stu-id="9851b-117">Select SpeakerTestAndPackaging.</span></span> <span data-ttu-id="9851b-118">Po výběru hodnoty se automaticky otevře stránka.</span><span class="sxs-lookup"><span data-stu-id="9851b-118">After you select the value, a page automatically opens.</span></span> <span data-ttu-id="9851b-119">Vybrat kanbanový tok SpeakerAssemblyAndPolish > SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="9851b-119">Select the kanban flow SpeakerAssemblyAndPolish > SpeakerTestAndPackaging.</span></span> <span data-ttu-id="9851b-120">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="9851b-120">Click OK.</span></span>  
7. <span data-ttu-id="9851b-121">Rozbalte sekci Podrobnosti.</span><span class="sxs-lookup"><span data-stu-id="9851b-121">Expand the Details section.</span></span>
8. <span data-ttu-id="9851b-122">V poli Produkt zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="9851b-122">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="9851b-123">Vyberte položku L0006.</span><span class="sxs-lookup"><span data-stu-id="9851b-123">Select Item L0006.</span></span>  

## <a name="create-kanban-and-view-jobs"></a><span data-ttu-id="9851b-124">Vytvoření kanbanu a zobrazení úloh</span><span class="sxs-lookup"><span data-stu-id="9851b-124">Create kanban and view jobs</span></span>
1. <span data-ttu-id="9851b-125">Rozbalte sekci Kanbany.</span><span class="sxs-lookup"><span data-stu-id="9851b-125">Expand the Kanbans section.</span></span>
2. <span data-ttu-id="9851b-126">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="9851b-126">Click Add.</span></span>
3. <span data-ttu-id="9851b-127">Do pole Počet nových kanbanů zadejte „1“.</span><span class="sxs-lookup"><span data-stu-id="9851b-127">In the Number of new kanbans field, enter '1'.</span></span>
    * <span data-ttu-id="9851b-128">Dojde k vytvoření 1 kanbanu.</span><span class="sxs-lookup"><span data-stu-id="9851b-128">This will create one kanban.</span></span>  
4. <span data-ttu-id="9851b-129">Nastavte Celkové množství produktu na 3.</span><span class="sxs-lookup"><span data-stu-id="9851b-129">Set Product quantity to '3'.</span></span>
    * <span data-ttu-id="9851b-130">Kanban zpracuje 3 produkty.</span><span class="sxs-lookup"><span data-stu-id="9851b-130">Kanban will process 3 products.</span></span>  
5. <span data-ttu-id="9851b-131">Do pole Datum/čas splatnosti zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="9851b-131">In the Due date/time field, enter a date and time.</span></span>
    * <span data-ttu-id="9851b-132">Lze zadat hodnotu Dnes.</span><span class="sxs-lookup"><span data-stu-id="9851b-132">You can enter Today.</span></span>  
6. <span data-ttu-id="9851b-133">Klikněte na položku Vytvořit.</span><span class="sxs-lookup"><span data-stu-id="9851b-133">Click Create.</span></span>
7. <span data-ttu-id="9851b-134">Klepněte na možnost Podrobnosti.</span><span class="sxs-lookup"><span data-stu-id="9851b-134">Click Details.</span></span>
    * <span data-ttu-id="9851b-135">Všimněte si, že kanban má od výrobního toku dvě úlohy pro zpracování.</span><span class="sxs-lookup"><span data-stu-id="9851b-135">Notice that the kanban has two process jobs from the production flow.</span></span> <span data-ttu-id="9851b-136">První je SpeakerAssemblyAndPolish a druhá SpeakerTestAndPackaging.</span><span class="sxs-lookup"><span data-stu-id="9851b-136">The first one is SpeakerAssemblyAndPolish, and the second one is SpeakerTestAndPackaging.</span></span>  
    * <span data-ttu-id="9851b-137">Poslední krok!</span><span class="sxs-lookup"><span data-stu-id="9851b-137">This is the last step!</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]