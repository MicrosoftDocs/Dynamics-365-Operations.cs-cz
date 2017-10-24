---
title: "Přidělování dat plánování rozpočtu"
description: "Tento článek popisuje různé metody přidělení, které jsou k dispozici v aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, a jejich použití."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 15191
ms.assetid: 89a918e8-59a4-4711-a2e9-b41989ddd0f1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: fd7ec30c8253f343b3d41d54c78696cd512b2ef7
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="budget-planning-data-allocation"></a><span data-ttu-id="45b55-103">Přidělení dat pro plánování rozpočtu</span><span class="sxs-lookup"><span data-stu-id="45b55-103">Budget planning data allocation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="45b55-104">Tento článek popisuje různé metody přidělení, které jsou k dispozici v aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, a jejich použití.</span><span class="sxs-lookup"><span data-stu-id="45b55-104">This article describes the various allocation methods that are available in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition and how they can be used.</span></span>  

<span data-ttu-id="45b55-105">Data lze rozdělit do plánu rozpočtu různými způsoby za účelem přesného zobrazení předpokládaných částek.</span><span class="sxs-lookup"><span data-stu-id="45b55-105">You can distribute the data in a budget plan in a number of ways to accurately portray the projected amounts.</span></span>

## <a name="allocation-methods"></a><span data-ttu-id="45b55-106">Metody přidělení</span><span class="sxs-lookup"><span data-stu-id="45b55-106">Allocation methods</span></span>
<span data-ttu-id="45b55-107">Tři metody přidělení (Přidělit napříč obdobími, Přidělit k dimenzím a Použít pravidla přidělení hlavní knihy) umožňují vytvořit řádky plánu rozpočtu, které jsou založeny na řádcích ve stejném plánu rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="45b55-107">Three allocation methods (Allocate across periods, Allocate to dimensions, and Use ledger allocation rules) can create budget plan lines that are based on lines in the same budget plan.</span></span> <span data-ttu-id="45b55-108">Tři další metody (Agregovat, Rozdělit a Kopírovat z plánu rozpočtu) umožňují vytvořit řádky plánu rozpočtu v jiných plánech rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="45b55-108">Three other methods (Aggregate, Distribute, and Copy from budget plan) can create budget plan lines in other budget plans.</span></span> <span data-ttu-id="45b55-109">U všech šesti metod přidělení je třeba zadat cílový scénář.</span><span class="sxs-lookup"><span data-stu-id="45b55-109">For all six allocation methods, you specify the destination scenario.</span></span> <span data-ttu-id="45b55-110">Cílový scénář může být buď stejný jako zdrojový scénář, nebo odlišný od zdrojového scénáře.</span><span class="sxs-lookup"><span data-stu-id="45b55-110">The destination scenario can be either the same as the source scenario or different from the source scenario.</span></span> <span data-ttu-id="45b55-111">Dále můžete určit, zda budou nové řádky připojeny k plánu rozpočtu, nebo nahradí aktuální řádky plánu rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="45b55-111">Additionally, you can specify whether new lines are appended to the budget plan or replace the current lines in the budget plan.</span></span>

<span data-ttu-id="45b55-112">[![AllocateAcrossPeriods](./media/allocateacrossperiods-300x259.png)](./media/allocateacrossperiods.png)
**Přidělit napříč obdobími** – kategorie přidělení období slouží k přidělení řádků plánu rozpočtu ze zdrojového scénáře plánu rozpočtu napříč obdobími k cílovému scénáři.</span><span class="sxs-lookup"><span data-stu-id="45b55-112">[![AllocateAcrossPeriods](./media/allocateacrossperiods-300x259.png)](./media/allocateacrossperiods.png)
**Allocate across periods** – A period allocation category is used to allocate the budget plan lines from the source budget plan scenario across periods in the destination scenario.</span></span> <span data-ttu-id="45b55-113">Zdrojová částka je přiřazena k více řádkům v cílovém scénáři na základě procenta a data, které jsou definované v rámci kategorie přidělení období.</span><span class="sxs-lookup"><span data-stu-id="45b55-113">The source amount is assigned to multiple lines in the destination scenario, based on the percentage and date that are defined in the period allocation category.</span></span>         

<span data-ttu-id="45b55-114">[![AllocateToDimensions](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**Přidělit k dimenzím** – řádky plánu rozpočtu jsou přiřazeny ze zdrojového scénáře plánování rozpočtu k jednomu nebo více řádkům v cílovém scénáři na základě procent a finančních dimenzí, které jsou definovány ve vybrané podmínce přidělení rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="45b55-114">[![AllocateToDimensions](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**Allocate to dimensions** – The budget plan lines are allocated from the source budget planning scenario to one or more lines in the destination scenario, based on the percentages and financial dimensions that are defined in a selected budget allocation term.</span></span>           

<span data-ttu-id="45b55-115">![AggregateChart](./media/aggregatechart-300x230.png)
**Agregovat** – řádky plánu rozpočtu jsou agregovány ze zdrojového scénáře plánu rozpočtu v přidružených (podřízených) plánech rozpočtu do cílového scénáře v nadřazeném plánu rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="45b55-115">![AggregateChart](./media/aggregatechart-300x230.png)
**Aggregate** – The budget plan lines are aggregated from the source budget plan scenario in the associated (child) budget plans to the destination scenario in the parent budget plan.</span></span> <span data-ttu-id="45b55-116">Tato metoda umožňuje částky rozpočtu, které jsou připraveny na nižší úrovni v organizaci pro konsolidaci na vyšší úrovni.</span><span class="sxs-lookup"><span data-stu-id="45b55-116">This method enables budget amounts that are prepared at a lower level in the organization to be consolidated at a higher level.</span></span>          

<span data-ttu-id="45b55-117">[![DistributeChart](./media/distributechart-300x230.png)](./media/distributechart.png)
**Rozdělit** – řádky plánu rozpočtu jsou rozděleny ze zdrojového scénáře plánování rozpočtu v nadřazenému plánu rozpočtu do cílového scénáře v přidružených (podřízených) plánech rozpočtu na základě finančních dimenzí organizačních jednotek přidružených plánů.</span><span class="sxs-lookup"><span data-stu-id="45b55-117">[![DistributeChart](./media/distributechart-300x230.png)](./media/distributechart.png)
**Distribute** – The budget plan lines are distributed from the source budget planning scenario in the parent budget plan to the destination scenario in the associated (child) budget plans, based on the financial dimensions of the organization units of the associated plans.</span></span> <span data-ttu-id="45b55-118">Tato metoda umožňuje částky rozpočtu, které jsou připraveny na vyšší úrovni v organizaci k rozšíření pro účely lokalizovanější kontroly.</span><span class="sxs-lookup"><span data-stu-id="45b55-118">This method enables budget amounts that are prepared at a higher level in the organization to be spread out for more localized review.</span></span>           

<span data-ttu-id="45b55-119">[![LedgerAllocationRules](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**Použít pravidla přidělení hlavní knihy** – řádky plánu rozpočtu jsou rozděleny ze zdrojového scénáře plánování rozpočtu do cílového scénáře na základě vybraného pravidla přidělení hlavní knihy.</span><span class="sxs-lookup"><span data-stu-id="45b55-119">[![LedgerAllocationRules](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**Use ledger allocation rules** – The budget plan lines are distributed from the source budget planning scenario to the destination scenario, based on the ledger allocation rule that is selected.</span></span> 

<span data-ttu-id="45b55-120">[![CopyFromBudgetPlan](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**Kopírovat z plánu rozpočtu** – stejně jako u přidělovací metody Rozdělení jsou řádky plánu rozpočtu vytvořeny v cíli na základě řádků v souvisejícím plán rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="45b55-120">[![CopyFromBudgetPlan](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**Copy from budget plan** – As in the Distribute allocation method, budget plan lines are created in the destination, based on lines in a related budget plan.</span></span> <span data-ttu-id="45b55-121">Pro tuto metodu však zdrojový plán rozpočtu nemusí být nadřazený, může však být na libovolné vyšší úrovni v hierarchii plánu rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="45b55-121">However, for this method, the source budget plan doesn't have to be the parent but can be at any higher level in the budget plan hierarchy.</span></span> <span data-ttu-id="45b55-122">Tato metoda přidělení je užitečná, pokud jsou konsolidované částky původně rozpočtované na výrazně vyšší úrovni a předtím, než obdrží schválení vyšší úrovně, musí být převedeny na nižší úroveň organizace pro podrobnou kontrolu a úpravy.</span><span class="sxs-lookup"><span data-stu-id="45b55-122">This allocation method is useful if consolidated amounts are originally budgeted at a much higher level, and must be transferred to a lower level of the organization for detailed review and adjustment before they can receive upper-level approval.</span></span>          

## <a name="using-allocation-methods-in-a-budget-plan"></a><span data-ttu-id="45b55-123">Použití metod přidělení v plánu rozpočtu</span><span class="sxs-lookup"><span data-stu-id="45b55-123">Using allocation methods in a budget plan</span></span>
<span data-ttu-id="45b55-124">Pokud chcete provést přidělení na stránce plánu rozpočtu, vyberte řádky k přidělení a klikněte na tlačítko **Přidělit rozpočet**.</span><span class="sxs-lookup"><span data-stu-id="45b55-124">To perform allocations on the budget plan page, select the lines to allocate, and then click **Allocate budget**.</span></span>

<span data-ttu-id="45b55-125">[![Tlačítko přidělení rozpočtu](./media/allocatebudgetbutton-300x84.png)](./media/allocatebudgetbutton.png)</span><span class="sxs-lookup"><span data-stu-id="45b55-125">[![AllocateBudgetButton](./media/allocatebudgetbutton-300x84.png)](./media/allocatebudgetbutton.png)</span></span> 

<span data-ttu-id="45b55-126">Dále vyberte metodu přidělení.</span><span class="sxs-lookup"><span data-stu-id="45b55-126">Next, select an allocation method.</span></span> <span data-ttu-id="45b55-127">Zbývající pole se poté nastaví na základě metody, kterou jste vybrali.</span><span class="sxs-lookup"><span data-stu-id="45b55-127">The remaining fields are then set, based on the method that you selected.</span></span> <span data-ttu-id="45b55-128">Tato pole zahrnují zdrojová a cílová data plánu rozpočtu a možnosti, které umožňují znásobit zdroj určeným koeficientem při vytváření cílových částek za účelem usnadnění hromadných úprav.</span><span class="sxs-lookup"><span data-stu-id="45b55-128">These fields include the source and destination of the budget plan data, and an option that lets you multiply the source by a specified factor when the destination amounts are created, to simplify bulk adjustment.</span></span> <span data-ttu-id="45b55-129">Můžete také nastavit možnost **Připojit k plánu**.</span><span class="sxs-lookup"><span data-stu-id="45b55-129">You can also set the **Append to plan** option.</span></span> <span data-ttu-id="45b55-130">Výběrem možnosti **Ne** nahraďte existující řádky plánu rozpočtu, nebo výběrem možnosti **Ano** zachovejte existující řádky plánu rozpočtu a přidejte nové řádky pro přidělené částky.</span><span class="sxs-lookup"><span data-stu-id="45b55-130">Select **No** to replace the existing budget plan lines, or select **Yes** to retain the existing budget plan lines and add new lines for the allocated amounts.</span></span>

## <a name="automating-allocations-during-a-workflow"></a><span data-ttu-id="45b55-131">Automatizace přidělení během workflowu</span><span class="sxs-lookup"><span data-stu-id="45b55-131">Automating allocations during a workflow</span></span>
<span data-ttu-id="45b55-132">Jedna výkonná funkce umožňuje přidělení prováděná automaticky jako součást workflowu plánování rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="45b55-132">One powerful feature enables allocations to be performed automatically as part of a budget planning workflow.</span></span> <span data-ttu-id="45b55-133">Jak plán rozpočtu prochází svým workflowem, mohou automatizované úlohy vyvolávat přidělení v určené fázi plánování rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="45b55-133">As a budget plan moves through its workflow, automated tasks can invoke an allocation at a specified budget planning stage.</span></span> 

<span data-ttu-id="45b55-134">Abyste mohli nastavit automatické přidělení, musíte nejprve vytvořit plán přidělení na stránce **Konfigurace plánování rozpočtu**.</span><span class="sxs-lookup"><span data-stu-id="45b55-134">To set up automated allocation, you must first create an allocation schedule on the **Budget planning configuration** page.</span></span> <span data-ttu-id="45b55-135">Plán přidělení definuje metodu přidělení, která se použije při spuštění automatizovaného přidělení, a hodnoty různých možností přidělení (viz popisy v předchozím oddílu).</span><span class="sxs-lookup"><span data-stu-id="45b55-135">The allocation schedule defines the allocation method that will be used when the automated allocation is run, and the values of the various allocation options (see the previous section for descriptions).</span></span> 

<span data-ttu-id="45b55-136">Dále vytvořte přidělení fáze na stránce **Konfigurace plánování rozpočtu**.</span><span class="sxs-lookup"><span data-stu-id="45b55-136">Next, you create a stage allocation on the **Budget planning configuration** page.</span></span> <span data-ttu-id="45b55-137">Přidělení fáze přiřadí plán přidělení pro workflow a fázi plánování rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="45b55-137">The stage allocation assigns an allocation schedule to the budget planning workflow and stage.</span></span> 

<span data-ttu-id="45b55-138">Nakonec přidejte automatizovanou úlohu pro přidělení fáze plánování rozpočtu v požadované fázi workflowu.</span><span class="sxs-lookup"><span data-stu-id="45b55-138">Finally, add an automated task for budget planning stage allocation at the desired workflow stage.</span></span> <span data-ttu-id="45b55-139">V následujícím příkladu byla do workflowu vložena dvě přidělení fází plánování rozpočtu (červený okraj).</span><span class="sxs-lookup"><span data-stu-id="45b55-139">In the following example, two budget planning stage allocations (outlined in red) have been inserted into the workflow.</span></span>

<span data-ttu-id="45b55-140">[![Přidělení fází plánování rozpočtu](./media/budgetplanningstageallocations-300x300.png)](./media/budgetplanningstageallocations.png)</span><span class="sxs-lookup"><span data-stu-id="45b55-140">[![BudgetPlanningStageAllocations](./media/budgetplanningstageallocations-300x300.png)](./media/budgetplanningstageallocations.png)</span></span>




