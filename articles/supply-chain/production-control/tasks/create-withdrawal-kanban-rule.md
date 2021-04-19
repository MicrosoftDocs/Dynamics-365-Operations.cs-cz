---
title: Vytvoření nového kanbanového pravidla odběru
description: Tento postup popisuje nastavení, které je třeba pro vytvoření kanbanového pravidla výběru pro převod materiálu v prostředí štíhlé výroby.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, UnitOfMeasureLookup, KanbanCreate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2adbcdbb2d278b25dce1d8c027e66367e9c0930e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828819"
---
# <a name="create-a-withdrawal-kanban-rule"></a><span data-ttu-id="4b77c-103">Vytvoření nového kanbanového pravidla odběru</span><span class="sxs-lookup"><span data-stu-id="4b77c-103">Create a withdrawal kanban rule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4b77c-104">Tento postup popisuje nastavení, které je třeba pro vytvoření kanbanového pravidla výběru pro převod materiálu v prostředí štíhlé výroby.</span><span class="sxs-lookup"><span data-stu-id="4b77c-104">This procedure shows the setup that is needed to create a withdrawal kanban rule for transferring material in a lean environment.</span></span> <span data-ttu-id="4b77c-105">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="4b77c-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="4b77c-106">Tento postup je určen pro technologa výrobních procesů nebo správce hodnotového proudu, kteří připravují doplnění nového nebo změněného materiálu.</span><span class="sxs-lookup"><span data-stu-id="4b77c-106">This procedure is intended for the Process Engineer or the Value Stream Manager, as they prepare replenishment of new or modified material.</span></span>


## <a name="create-new-kanban-rule"></a><span data-ttu-id="4b77c-107">Vytvořit nové kanbanové pravidlo</span><span class="sxs-lookup"><span data-stu-id="4b77c-107">Create new kanban rule</span></span>
1. <span data-ttu-id="4b77c-108">Otevřete Kanbanová pravidla.</span><span class="sxs-lookup"><span data-stu-id="4b77c-108">Go to Kanban rules.</span></span>
2. <span data-ttu-id="4b77c-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="4b77c-109">Click New.</span></span>
3. <span data-ttu-id="4b77c-110">V poli Typ vyberte Výběr.</span><span class="sxs-lookup"><span data-stu-id="4b77c-110">In the Type field, select 'Withdrawal'.</span></span>
    * <span data-ttu-id="4b77c-111">Typ Výběr se používá pro kanbanová pravidla zaměřená na převod materiálu nebo zboží.</span><span class="sxs-lookup"><span data-stu-id="4b77c-111">The Withdrawal type is used for kanban rules to transfer material or goods.</span></span>  
4. <span data-ttu-id="4b77c-112">V poli První aktivita plánu zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="4b77c-112">In the First plan activity field, enter or select a value.</span></span>
    * <span data-ttu-id="4b77c-113">Vyberte ReplenishSpeakerComponents.</span><span class="sxs-lookup"><span data-stu-id="4b77c-113">Select ReplenishSpeakerComponents.</span></span>   <span data-ttu-id="4b77c-114">Tato aktivita je nastavena na přesun součástí ze skladu 11 v umístění 11 do skladu 12 v umístění 12.</span><span class="sxs-lookup"><span data-stu-id="4b77c-114">This activity is set up to move components from warehouse 11, location 11 to warehouse 12, and location 12.</span></span>  
5. <span data-ttu-id="4b77c-115">V poli Produkt zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="4b77c-115">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="4b77c-116">Vyberte volbu „M0007“.</span><span class="sxs-lookup"><span data-stu-id="4b77c-116">Select M0007.</span></span>  
6. <span data-ttu-id="4b77c-117">Do pole Doba realizace zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="4b77c-117">In the Lead time field, enter a number.</span></span>
    * <span data-ttu-id="4b77c-118">Například 60.</span><span class="sxs-lookup"><span data-stu-id="4b77c-118">For example, 60.</span></span>  
7. <span data-ttu-id="4b77c-119">V poli Měrná jednotka zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="4b77c-119">In the Unit of measure field, enter or select a value.</span></span>
    * <span data-ttu-id="4b77c-120">Například Minuty.</span><span class="sxs-lookup"><span data-stu-id="4b77c-120">For example, Minutes.</span></span>  

## <a name="set-quantities-for-kanban"></a><span data-ttu-id="4b77c-121">Nastavte množství pro kanban</span><span class="sxs-lookup"><span data-stu-id="4b77c-121">Set quantities for kanban</span></span>
1. <span data-ttu-id="4b77c-122">Nastavte výchozí množství na „5“.</span><span class="sxs-lookup"><span data-stu-id="4b77c-122">Set Default quantity to '5'.</span></span>
    * <span data-ttu-id="4b77c-123">Jedná se o množství, které bude přeneseno pro každý kanban.</span><span class="sxs-lookup"><span data-stu-id="4b77c-123">This is the quantity that will be transferred for each kanban.</span></span>  
2. <span data-ttu-id="4b77c-124">Zadejte 2 do pole Pevné kanbanové množství.</span><span class="sxs-lookup"><span data-stu-id="4b77c-124">In the Fixed kanban quantity field, enter '2'.</span></span>
    * <span data-ttu-id="4b77c-125">To je počet kanbanů, které mají být aktivní.</span><span class="sxs-lookup"><span data-stu-id="4b77c-125">This is the amount of kanbans that should be active.</span></span> <span data-ttu-id="4b77c-126">V tomto případě 2 kanbany přenáší vždy každý 5.</span><span class="sxs-lookup"><span data-stu-id="4b77c-126">In this case, 2 kanbans transferring 5 each.</span></span>  
3. <span data-ttu-id="4b77c-127">V poli Minimální hranice výstrahy zadejte hodnotu „1“.</span><span class="sxs-lookup"><span data-stu-id="4b77c-127">In the Alert boundary minimum field, enter '1'.</span></span>
    * <span data-ttu-id="4b77c-128">Slouží ke sledování minimálního množství plných kanbanů, které mají být na místě určení.</span><span class="sxs-lookup"><span data-stu-id="4b77c-128">Used to keep track of the minimum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="4b77c-129">Toto se například používá na přehled kanbanového množství.</span><span class="sxs-lookup"><span data-stu-id="4b77c-129">For example, this is used on the kanban quantity overview.</span></span>  
4. <span data-ttu-id="4b77c-130">V poli Maximální hranice výstrahy zadejte hodnotu „2“.</span><span class="sxs-lookup"><span data-stu-id="4b77c-130">In the Alert boundary maximum field, enter '2'.</span></span>
    * <span data-ttu-id="4b77c-131">Slouží ke sledování maximálního množství plných kanbanů, které mají být na místě určení.</span><span class="sxs-lookup"><span data-stu-id="4b77c-131">Used to keep track of the maximum amount of full kanbans that should be at the destination.</span></span> <span data-ttu-id="4b77c-132">Toto se například používá na přehled kanbanového množství.</span><span class="sxs-lookup"><span data-stu-id="4b77c-132">For example, this is used on the kanban quantity overview.</span></span>  

## <a name="create-kanbans"></a><span data-ttu-id="4b77c-133">Vytvořit kanbany</span><span class="sxs-lookup"><span data-stu-id="4b77c-133">Create kanbans</span></span>
1. <span data-ttu-id="4b77c-134">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="4b77c-134">Click Save.</span></span>
    * <span data-ttu-id="4b77c-135">Kanbanové pravidlo je třeba uložit, aby bylo možné vytvořit kanbany.</span><span class="sxs-lookup"><span data-stu-id="4b77c-135">The kanban rule needs to be saved before kanbans can be created.</span></span>  
2. <span data-ttu-id="4b77c-136">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="4b77c-136">Click Add.</span></span>
    * <span data-ttu-id="4b77c-137">Všimněte si, že neexistují žádné aktivní kanbany, protože navrhovaný „Počet nových kanbanů“ je 2. Toto se rovná „Pevnému kanbanovému množství“.</span><span class="sxs-lookup"><span data-stu-id="4b77c-137">Note that there are no active kanbans because the suggested 'Number of new kanbans' is 2, which is equal to the 'Fixed kanban quantity'.</span></span>  
3. <span data-ttu-id="4b77c-138">Klikněte na položku Vytvořit.</span><span class="sxs-lookup"><span data-stu-id="4b77c-138">Click Create.</span></span>
    * <span data-ttu-id="4b77c-139">Dojde k vytvoření 2 kanbanů.</span><span class="sxs-lookup"><span data-stu-id="4b77c-139">This will create two kanbans.</span></span>  
    * <span data-ttu-id="4b77c-140">Všimněte si, že 2 kanbany po 5 byly vytvořeny pro toto kanbanové pravidlo výběru.</span><span class="sxs-lookup"><span data-stu-id="4b77c-140">Note that 2 kanbans, for 5 each, was created for this withdrawal kanban rule.</span></span>  <span data-ttu-id="4b77c-141">Tento krok je posledním krokem v tomto postupu.</span><span class="sxs-lookup"><span data-stu-id="4b77c-141">This is the last step in this procedure.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]