--- 
title: "Vytvoření nahrazujícího kanbanového pravidla"
description: "Tento postup se zaměřuje na nahrazení existujícího kanbanového pravidla za nové kanbanové pravidlo k určitému datu."
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 12df41f14973628063b11f20f7368f47b2ad3488
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-replacement-kanban-rule"></a><span data-ttu-id="a7ec2-103">Vytvoření nahrazujícího kanbanového pravidla</span><span class="sxs-lookup"><span data-stu-id="a7ec2-103">Create a replacement kanban rule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a7ec2-104">Tento postup se zaměřuje na nahrazení existujícího kanbanového pravidla za nové kanbanové pravidlo k určitému datu.</span><span class="sxs-lookup"><span data-stu-id="a7ec2-104">This procedure focuses on replacing an existing kanban rule with a new kanban rule on a specific date.</span></span> <span data-ttu-id="a7ec2-105">To je užitečné, pokud je potřeba změny v pravidlech výrobního toku nebo doplnění spravovat nebo naplánovat.</span><span class="sxs-lookup"><span data-stu-id="a7ec2-105">This is useful when changes in the production flow or replenishment rules need to be coordinated and scheduled.</span></span> <span data-ttu-id="a7ec2-106">Použitá ukázková data společnosti USMF k vytvoření postupu.</span><span class="sxs-lookup"><span data-stu-id="a7ec2-106">The demo data company used to create procedure is USMF.</span></span> <span data-ttu-id="a7ec2-107">Tento postup je určen pro technologa výrobních procesů nebo správce hodnotového proudu, kteří připravují výrobu změněného výrobního toku nebo nového pravidla doplnění.</span><span class="sxs-lookup"><span data-stu-id="a7ec2-107">This procedure is intended for the process engineer or the value stream manager when they prepare production for a changed production flow or a new replenishment rule.</span></span> <span data-ttu-id="a7ec2-108">Tato úloha nahradí kanbanové pravidlo 000022 za nové pravidlo a zvýší maximální množství z 48 na 100 pro nové pravidlo.</span><span class="sxs-lookup"><span data-stu-id="a7ec2-108">This task replaces kanban rule 000022 with a new rule and increases the maximum quantity from 48 to 100 for the new rule.</span></span>


## <a name="select-a-kanban-rule-to-replace"></a><span data-ttu-id="a7ec2-109">Výběr kanbanového pravidla, které chcete nahradit</span><span class="sxs-lookup"><span data-stu-id="a7ec2-109">Select a kanban rule to replace</span></span>
1. <span data-ttu-id="a7ec2-110">Otevřete Kanbanová pravidla.</span><span class="sxs-lookup"><span data-stu-id="a7ec2-110">Go to Kanban rules.</span></span>
2. <span data-ttu-id="a7ec2-111">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="a7ec2-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a7ec2-112">Vyberte kanbanové pravidlo 000022.</span><span class="sxs-lookup"><span data-stu-id="a7ec2-112">Select kanban rule 000022.</span></span>  

## <a name="create-a-replacement-kanban-rule"></a><span data-ttu-id="a7ec2-113">Vytvoření nahrazujícího kanbanového pravidla</span><span class="sxs-lookup"><span data-stu-id="a7ec2-113">Create a replacement kanban rule</span></span>
1. <span data-ttu-id="a7ec2-114">Klikněte na Nahradit kanbanové pravidlo.</span><span class="sxs-lookup"><span data-stu-id="a7ec2-114">Click Replace kanban rule.</span></span>
2. <span data-ttu-id="a7ec2-115">Do pole Datum platnosti zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="a7ec2-115">In the Effective date field, enter a date and time.</span></span>
    * <span data-ttu-id="a7ec2-116">Vyberte datum v budoucnosti, jako například jeden týden ode dneška.</span><span class="sxs-lookup"><span data-stu-id="a7ec2-116">Select a date in the future, such as one week from now.</span></span> <span data-ttu-id="a7ec2-117">Jedná se o datum a čas, kdy se nové kanbanové pravidlo stane aktivní a nahradí původní kanbanové pravidlo.</span><span class="sxs-lookup"><span data-stu-id="a7ec2-117">This is the date and time when the new kanban rule becomes active and replaces the old kanban rule.</span></span>  
    * <span data-ttu-id="a7ec2-118">Pokud kanbanové pravidlo změní cestu ve výrobním toku, lze vybrat jinou aktivitu.</span><span class="sxs-lookup"><span data-stu-id="a7ec2-118">If the kanban rule changes the path in the production flow,  another activity can be selected.</span></span>  <span data-ttu-id="a7ec2-119">V tomto postupu doporučujeme zachovat aktivitu beze změny.</span><span class="sxs-lookup"><span data-stu-id="a7ec2-119">In this procedure, we will keep the activity untouched.</span></span>  
3. <span data-ttu-id="a7ec2-120">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="a7ec2-120">Click OK.</span></span>
    * <span data-ttu-id="a7ec2-121">Všimněte si, že dojde k vytvoření nového kanbanového pravidla, které nahradí kanbanové pravidlo 000022.</span><span class="sxs-lookup"><span data-stu-id="a7ec2-121">Notice that a new kanban rule is created to replace kanban rule 000022.</span></span>  
    * <span data-ttu-id="a7ec2-122">Platné datum je nastaveno podle data vybraného při nahrazení kanbanového pravidla.</span><span class="sxs-lookup"><span data-stu-id="a7ec2-122">The effective date is set according to the date chosen when you replace the kanban rule.</span></span>  
4. <span data-ttu-id="a7ec2-123">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="a7ec2-123">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a7ec2-124">Vyberte nahrazené kanbanové pravidlo 000022.</span><span class="sxs-lookup"><span data-stu-id="a7ec2-124">Select the replaced kanban rule 000022.</span></span>  
    * <span data-ttu-id="a7ec2-125">Povšimněte si, že nahrazené kanbanové pravidlo má stejné datum, jako datum vypršení platnosti, protože se jedná o datum, kdy platnost vyprší.</span><span class="sxs-lookup"><span data-stu-id="a7ec2-125">Notice that the replaced kanban rule has the same date as the Expiration date because this is the date when it will expire.</span></span>  
5. <span data-ttu-id="a7ec2-126">Vyberte ze seznamu řádek 1.</span><span class="sxs-lookup"><span data-stu-id="a7ec2-126">In the list, select row 1.</span></span>
    * <span data-ttu-id="a7ec2-127">Vyberte nové kanbanové pravidlo na začátku na seznamu.</span><span class="sxs-lookup"><span data-stu-id="a7ec2-127">Select the new kanban rule on top of the list.</span></span> <span data-ttu-id="a7ec2-128">Jedná se o kanbanové pravidlo s nejvyšším číslem kanbanového pravidla.</span><span class="sxs-lookup"><span data-stu-id="a7ec2-128">This is the kanban rule with the highest kanban rule number.</span></span>  
6. <span data-ttu-id="a7ec2-129">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="a7ec2-129">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a7ec2-130">Klikněte na číslo kanbanového pravidla a otevřete tak kanbanové pravidlo.</span><span class="sxs-lookup"><span data-stu-id="a7ec2-130">Click the kanban rule number to open the kanban rule.</span></span>  

## <a name="modify-maximum-quantity-for-the-replacement-kanban-rule"></a><span data-ttu-id="a7ec2-131">Úprava maximálního množství pro náhradní kanbanové pravidlo</span><span class="sxs-lookup"><span data-stu-id="a7ec2-131">Modify maximum quantity for the replacement kanban rule</span></span>
1. <span data-ttu-id="a7ec2-132">Nastavte Maximální množství na „100“.</span><span class="sxs-lookup"><span data-stu-id="a7ec2-132">Set Maximum quantity to '100'.</span></span>
    * <span data-ttu-id="a7ec2-133">Rozbalte pevnou záložku Množství a prohlédněte si pole Maximální množství.</span><span class="sxs-lookup"><span data-stu-id="a7ec2-133">Expand the Quantities FastTab to see the Maximum quantity field.</span></span> <span data-ttu-id="a7ec2-134">Změna maximálního množství na hodnotu 100 vám umožní zpracovat až 100 kanbanů.</span><span class="sxs-lookup"><span data-stu-id="a7ec2-134">Changing the maximum quantity to 100 will allow up to 100 kanbans to be processed.</span></span>    <span data-ttu-id="a7ec2-135">Tento krok je posledním krokem v tomto postupu.</span><span class="sxs-lookup"><span data-stu-id="a7ec2-135">This is the last step in this task.</span></span>  


