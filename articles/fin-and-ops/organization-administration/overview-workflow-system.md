---
title: "Přehled workflowu"
description: "Toto téma popisuje systém workflowu v aplikaci Microsoft Dynamics 365 for Finance and Operations."
author: sericks007
manager: AnnBe
ms.date: 08/17/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f4e2167290618aaf6ad144e7db8274514078388b
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="workflow-overview"></a><span data-ttu-id="9df3f-103">Přehled workflowu</span><span class="sxs-lookup"><span data-stu-id="9df3f-103">Workflow overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="9df3f-104">Toto téma popisuje systém workflowu v aplikaci Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9df3f-104">This topic describes the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

<a name="what-is-workflow"></a><span data-ttu-id="9df3f-105">Co je workflow?</span><span class="sxs-lookup"><span data-stu-id="9df3f-105">What is workflow?</span></span>
-----------------

<span data-ttu-id="9df3f-106">Termín *workflow* lze definovat dvěma způsoby: workflow jako systém a workflow jako obchodní proces.</span><span class="sxs-lookup"><span data-stu-id="9df3f-106">The term *workflow* can be defined in two ways: as a system and as a business process.</span></span>
### <a name="workflow-is-a-system"></a><span data-ttu-id="9df3f-107">Workflow je systém</span><span class="sxs-lookup"><span data-stu-id="9df3f-107">Workflow is a system</span></span>

<span data-ttu-id="9df3f-108">Workflow je systém nainstalovaný s aplikací Finance and Operations a běží na aplikačním objektovém serveru (AOS).</span><span class="sxs-lookup"><span data-stu-id="9df3f-108">Workflow is a system that is installed with Finance and Operations and runs on the Application Object Server (AOS).</span></span> <span data-ttu-id="9df3f-109">Systém workflowu nabízí funkce, pomocí kterých lze vytvářet individuální workflowy nebo obchodní procesy.</span><span class="sxs-lookup"><span data-stu-id="9df3f-109">The workflow system provides functionality that you can use to create individual workflows, or business processes.</span></span>

### <a name="workflow-is-a-business-process"></a><span data-ttu-id="9df3f-110">Workflow je obchodní proces</span><span class="sxs-lookup"><span data-stu-id="9df3f-110">Workflow is a business process</span></span>

<span data-ttu-id="9df3f-111">Workflow představuje obchodní proces.</span><span class="sxs-lookup"><span data-stu-id="9df3f-111">A workflow represents a business process.</span></span> <span data-ttu-id="9df3f-112">Definuje tok dokumentu nebo jeho procházení systémem zobrazením, kdo musí splnit úkol, provádět rozhodování nebo schválení dokumentu.</span><span class="sxs-lookup"><span data-stu-id="9df3f-112">It defines how a document flows, or moves, through the system by showing who must complete a task, make a decision, or approve a document.</span></span> <span data-ttu-id="9df3f-113">Následující obrázek znázorňuje příklad workflowu pro sestavy výdajů.</span><span class="sxs-lookup"><span data-stu-id="9df3f-113">For example, the following illustration shows a workflow for expense reports.</span></span> 

![Workflow s prvky, které jsou přiřazeny uživatelům](./media/workflow_user.gif) 

<span data-ttu-id="9df3f-115">Abychom lépe pochopili tento workflow, předpokládejme, že Stanislav odešle vyúčtování výdajů s částkou 7 000 USD.</span><span class="sxs-lookup"><span data-stu-id="9df3f-115">To better understand this workflow, suppose that Sam submits an expense report for USD 7,000.</span></span> <span data-ttu-id="9df3f-116">V tomto scénáři musí Ivan zkontrolovat účtenky, které mu Stanislav předal.</span><span class="sxs-lookup"><span data-stu-id="9df3f-116">In this scenario, Ivan must review the receipts that Sam routes to him.</span></span> <span data-ttu-id="9df3f-117">Poté musí být vyúčtování výdajů schváleno Františkem a Šárkou.</span><span class="sxs-lookup"><span data-stu-id="9df3f-117">Then Frank and Sue must approve the expense report.</span></span> <span data-ttu-id="9df3f-118">Nyní předpokládejme, že Stanislav odešle vyúčtování výdajů s částkou 11 000 USD.</span><span class="sxs-lookup"><span data-stu-id="9df3f-118">Now suppose that Sam submits an expense report for USD 11,000.</span></span> <span data-ttu-id="9df3f-119">V tomto scénáři musí Ivan zkontrolovat účtenky a František, Šárka a Anna musí toto vyúčtování výdajů schválit.</span><span class="sxs-lookup"><span data-stu-id="9df3f-119">In this scenario, Ivan must review the receipts, and Frank, Sue, and Ann must approve the expense report.</span></span>

## <a name="benefits-of-using-the-workflow-system"></a><span data-ttu-id="9df3f-120"> Výhody používání systému workflowu</span><span class="sxs-lookup"><span data-stu-id="9df3f-120">Benefits of using the workflow system</span></span>

<span data-ttu-id="9df3f-121">Používání systému workflowu v organizaci má několik výhod:</span><span class="sxs-lookup"><span data-stu-id="9df3f-121">There are several benefits of using the workflow system in your organization:</span></span>
-   <span data-ttu-id="9df3f-122">**Konzistentní procesy:** – Můžete definovat schvalovací proces pro specifické dokumenty, například nákupní požadavky a vyúčtování výdajů.</span><span class="sxs-lookup"><span data-stu-id="9df3f-122">**Consistent processes** – You can define how specific documents, such as purchase requisitions and expense reports, are processed.</span></span> <span data-ttu-id="9df3f-123">Používáním systému workflowu lze zajistit, aby byly dokumenty zpracovávány a schvalovány jednotným a efektivním způsobem.</span><span class="sxs-lookup"><span data-stu-id="9df3f-123">By using the workflow system, you ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
-   <span data-ttu-id="9df3f-124">**Viditelnost procesů:** – Můžete sledovat stav, historii a výkonnostní metriku instancí workflowu.</span><span class="sxs-lookup"><span data-stu-id="9df3f-124">**Process visibility** – You can track the status, history, and performance metrics of workflow instances.</span></span> <span data-ttu-id="9df3f-125">To umožňuje určit, zda je potřeba provést změny workflowu ke zvýšení efektivity.</span><span class="sxs-lookup"><span data-stu-id="9df3f-125">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
-   <span data-ttu-id="9df3f-126">**Centralizovaný seznam pracovních položek** – Uživatelé mohou zobrazit centralizovaný seznam pracovních položek k zobrazení úkolů workflowu a schválení, které mají přiřazeny.</span><span class="sxs-lookup"><span data-stu-id="9df3f-126">**Centralized work list** – Users can view a centralized work list that displays the workflow tasks and approvals that are assigned to them.</span></span>


## <a name="workflow-content"></a><span data-ttu-id="9df3f-127">Obsah workflowu</span><span class="sxs-lookup"><span data-stu-id="9df3f-127">Workflow content</span></span>

+ [<span data-ttu-id="9df3f-128">Architektura workflowu</span><span class="sxs-lookup"><span data-stu-id="9df3f-128">Workflow architecture</span></span>](workflow-system-architecture.md)
+ [<span data-ttu-id="9df3f-129">Prvky workflowu</span><span class="sxs-lookup"><span data-stu-id="9df3f-129">Workflow elements</span></span>](workflow-elements.md)
+ [<span data-ttu-id="9df3f-130">Akce workflowu</span><span class="sxs-lookup"><span data-stu-id="9df3f-130">Workflow actions</span></span>](workflow-actions.md)
+ [<span data-ttu-id="9df3f-131">Vytvoření workflowu</span><span class="sxs-lookup"><span data-stu-id="9df3f-131">Create a workflow</span></span>](create-workflow.md)
+ [<span data-ttu-id="9df3f-132">Konfigurace vlastností workflowu</span><span class="sxs-lookup"><span data-stu-id="9df3f-132">Configure workflow properties</span></span>](configure-workflow-properties.md)
+ [<span data-ttu-id="9df3f-133">Konfigurace ruční úlohy ve workflowu</span><span class="sxs-lookup"><span data-stu-id="9df3f-133">Configure a manual task in a workflow</span></span>](configure-manual-task-workflow.md)
+ [<span data-ttu-id="9df3f-134">Konfigurace automatizované úlohy ve workflowu</span><span class="sxs-lookup"><span data-stu-id="9df3f-134">Configure an automated task in a workflow</span></span>](configure-automated-task-workflow.md)
+ [<span data-ttu-id="9df3f-135">Konfigurace schvalovacího procesu ve workflowu</span><span class="sxs-lookup"><span data-stu-id="9df3f-135">Configure an approval process in a workflow</span></span>](configure-approval-process-workflow.md)
+ [<span data-ttu-id="9df3f-136">Konfigurace schvalovacího kroku ve workflowu</span><span class="sxs-lookup"><span data-stu-id="9df3f-136">Configure an approval step in a workflow</span></span>](configure-approval-step-workflow.md)
+ [<span data-ttu-id="9df3f-137">Konfigurace ručního rozhodnutí ve workflowu</span><span class="sxs-lookup"><span data-stu-id="9df3f-137">Configure a manual decision in a workflow</span></span>](configure-manual-decision-workflow.md)
+ [<span data-ttu-id="9df3f-138">Konfigurace podmíněného rozhodnutí ve workflowu</span><span class="sxs-lookup"><span data-stu-id="9df3f-138">Configure a conditional decision in a workflow</span></span>](configure-conditional-decision-workflow.md)
+ [<span data-ttu-id="9df3f-139">Konfigurace paralelních aktivit ve workflowu</span><span class="sxs-lookup"><span data-stu-id="9df3f-139">Configure a parallel activity in a workflow</span></span>](configure-parallel-activity-workflow.md)
+ [<span data-ttu-id="9df3f-140">Konfigurace paralelní větve ve workflowu</span><span class="sxs-lookup"><span data-stu-id="9df3f-140">Configure a parallel branch in a workflow</span></span>](configure-parallel-branch-workflow.md)
+ [<span data-ttu-id="9df3f-141">Konfigurace workflowu položky řádku</span><span class="sxs-lookup"><span data-stu-id="9df3f-141">Configure a line-item workflow</span></span>](configure-line-item-workflow.md)

