---
title: Přidání zásad výpočtu kanbanového množství ke kanbanovému pravidlu
description: Tento postup se zaměřuje na vytváření zásad výpočtu kanbanového množství a jejich přidání do kanbanového pravidla pro optimalizaci velikosti a množství kanbanu.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanQuantityPolicy, KanbanRules
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 19f563379a10bbe42681a5f61779fb9e72d1f60c
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3211001"
---
# <a name="add-a-kanban-quantity-calculation-policy-to-a-kanban-rule"></a><span data-ttu-id="f970d-103">Přidání zásad výpočtu kanbanového množství ke kanbanovému pravidlu</span><span class="sxs-lookup"><span data-stu-id="f970d-103">Add a kanban quantity calculation policy to a kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f970d-104">Tento postup se zaměřuje na vytváření zásad výpočtu kanbanového množství a jejich přidání do kanbanového pravidla pro optimalizaci velikosti a množství kanbanu.</span><span class="sxs-lookup"><span data-stu-id="f970d-104">This procedure focuses on creating a kanban quantity calculation policy and adding it to a kanban rule to optimize the kanban size and quantities.</span></span> <span data-ttu-id="f970d-105">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="f970d-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="f970d-106">Tento postup je určen pro vedoucího hodnotového proudu.</span><span class="sxs-lookup"><span data-stu-id="f970d-106">This procedure is intended for the value stream manager.</span></span> <span data-ttu-id="f970d-107">Tento postup je nezbytným předpokladem vytvoření postupu pro výpočet návrhů kanbanového množství.</span><span class="sxs-lookup"><span data-stu-id="f970d-107">This procedure is a prerequisite for creating the procedure Calculate kanban quantity suggestions.</span></span> 


## <a name="create-a-kanban-quantity-calculation-policy"></a><span data-ttu-id="f970d-108">Vytvoření zásady pro výpočet kanbanového množství</span><span class="sxs-lookup"><span data-stu-id="f970d-108">Create a kanban quantity calculation policy</span></span>
1. <span data-ttu-id="f970d-109">Přejít na Řízení výroby > Pravidelné úlohy > Výpočet kanbanového množství > Zásady pro výpočet kanbanového množství.</span><span class="sxs-lookup"><span data-stu-id="f970d-109">Go to Production control > Periodic tasks > Kanban quantity calculation > Kanban quantity calculation policies.</span></span>
2. <span data-ttu-id="f970d-110">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="f970d-110">Click New.</span></span>
3. <span data-ttu-id="f970d-111">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="f970d-111">In the Name field, type a value.</span></span>
    * <span data-ttu-id="f970d-112">Například zadejte Speaker2016.</span><span class="sxs-lookup"><span data-stu-id="f970d-112">For example, type Speaker2016.</span></span>  
4. <span data-ttu-id="f970d-113">V poli Hlavní plán kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="f970d-113">In the Master plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="f970d-114">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="f970d-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f970d-115">Vyberte StaticPlan pro výpočet poptávky.</span><span class="sxs-lookup"><span data-stu-id="f970d-115">Select StaticPlan to calculate demand.</span></span>  
6. <span data-ttu-id="f970d-116">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="f970d-116">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="f970d-117">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="f970d-117">Click Save.</span></span>
8. <span data-ttu-id="f970d-118">Zadejte 1 do pole Minimální kanbanové množství.</span><span class="sxs-lookup"><span data-stu-id="f970d-118">In the Minimum kanban quantity field, enter '1'.</span></span>
    * <span data-ttu-id="f970d-119">Toto je další číslo kanbanu, které je zahrnuto do výpočtu kanbanového množství.</span><span class="sxs-lookup"><span data-stu-id="f970d-119">This is the additional number of kanbans that is included in the kanban quantity calculation.</span></span>  
9. <span data-ttu-id="f970d-120">Nastavte Bezpečnostní koeficient na 1.</span><span class="sxs-lookup"><span data-stu-id="f970d-120">Set Safety factor to '1'.</span></span>
    * <span data-ttu-id="f970d-121">Toto je koeficient používaný k výpočtu dodatečného množství pojistných zásob.</span><span class="sxs-lookup"><span data-stu-id="f970d-121">This is the factor that is used to calculate additional quantity of safety stock.</span></span>  
10. <span data-ttu-id="f970d-122">V poli Počet dní předem zadejte číslo 30.</span><span class="sxs-lookup"><span data-stu-id="f970d-122">In the Days ahead field, enter '30'.</span></span>
    * <span data-ttu-id="f970d-123">Toto je počet dní předcházejících výpočtu kanbanového množství, kde je ve výpočtu zahrnuta poptávka.</span><span class="sxs-lookup"><span data-stu-id="f970d-123">This is the number of days prior to the kanban quantity calculation date that is included in the demand calculation.</span></span>  
11. <span data-ttu-id="f970d-124">V poli Počet dní po zadejte číslo 30.</span><span class="sxs-lookup"><span data-stu-id="f970d-124">In the Days behind field, enter '30'.</span></span>
    * <span data-ttu-id="f970d-125">Toto je počet dní dopředu od data výpočtu kanbanového množství, kde je ve výpočtu zahrnuta poptávka.</span><span class="sxs-lookup"><span data-stu-id="f970d-125">This is the number of days forward from the kanban quantity calculation date that is included in the demand calculation.</span></span>  <span data-ttu-id="f970d-126">Vzorec použitý pro výpočet se zobrazí a bude obsahovat skutečné hodnoty.</span><span class="sxs-lookup"><span data-stu-id="f970d-126">The formula used for the calculation is shown with the actual values.</span></span> <span data-ttu-id="f970d-127">Například: Kanbanové množství = ((průměrná denní poptávka x doba realizace x 2.00) / množství produktu na manipulační jednotku) + 1</span><span class="sxs-lookup"><span data-stu-id="f970d-127">For example,  Kanban quantity = ((Average daily demand x lead time x 2.00) / Product quantity per handling unit) + 1</span></span>  
12. <span data-ttu-id="f970d-128">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="f970d-128">Close the page.</span></span>

## <a name="add-the-kanban-quantity-calculation-policy-to-a-kanban-rule"></a><span data-ttu-id="f970d-129">Přidání zásady pro výpočet kanbanového množství ke kanbanovému pravidlu</span><span class="sxs-lookup"><span data-stu-id="f970d-129">Add the kanban quantity calculation policy to a kanban rule</span></span>
1. <span data-ttu-id="f970d-130">Přejděte k Řízení informací o produktech > Lean manufacturing > Kanbanová pravidla.</span><span class="sxs-lookup"><span data-stu-id="f970d-130">Go to Product information management > Lean manufacturing > Kanban rules.</span></span>
2. <span data-ttu-id="f970d-131">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="f970d-131">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f970d-132">Vyberte kanbanové pravidlo 000020 v tomto postupu.</span><span class="sxs-lookup"><span data-stu-id="f970d-132">Select kanban rule 000020 for this procedure.</span></span>  
3. <span data-ttu-id="f970d-133">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="f970d-133">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="f970d-134">Přepněte rozšíření oddílu Zásady pro výpočet kanbanového množství.</span><span class="sxs-lookup"><span data-stu-id="f970d-134">Toggle the expansion of the Kanban quantity calculation policies section.</span></span>
5. <span data-ttu-id="f970d-135">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="f970d-135">Click Add.</span></span>
    * <span data-ttu-id="f970d-136">Přidejte zásady výpočtu kanbanového množství, které jste právě vytvořili v předchozím podúkolu.</span><span class="sxs-lookup"><span data-stu-id="f970d-136">Add the kanban quantity calculation policy that you have just created in the previous sub-task.</span></span>  
6. <span data-ttu-id="f970d-137">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="f970d-137">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="f970d-138">V poli Název kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="f970d-138">In the Name field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="f970d-139">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="f970d-139">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f970d-140">Vyberte zásadu Speaker2016, kterou jste právě vytvořili v předchozím podúkolu.</span><span class="sxs-lookup"><span data-stu-id="f970d-140">Select the policy Speaker2016 that you have just created in the previous sub-task.</span></span>  

