---
title: Přehled systému workflow
description: Toto téma popisuje systém workflowu.
author: sericks007
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56381
ms.assetid: 20b78595-e1d9-439a-ae1c-a776a3438919
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6e5e795ca6f7831ecd3fa28be9782f0b287eea6e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189998"
---
# <a name="workflow-system-overview"></a><span data-ttu-id="dfba9-103">Přehled systému workflow</span><span class="sxs-lookup"><span data-stu-id="dfba9-103">Workflow system overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dfba9-104">Toto téma popisuje systém workflowu.</span><span class="sxs-lookup"><span data-stu-id="dfba9-104">This topic describes the workflow system.</span></span>

## <a name="what-is-workflow"></a><span data-ttu-id="dfba9-105">Co je workflow?</span><span class="sxs-lookup"><span data-stu-id="dfba9-105">What is workflow?</span></span>

<span data-ttu-id="dfba9-106">Termín *workflow* lze definovat dvěma způsoby: workflow jako systém a workflow jako obchodní proces.</span><span class="sxs-lookup"><span data-stu-id="dfba9-106">The term *workflow* can be defined in two ways: as a system and as a business process.</span></span>

### <a name="workflow-is-a-system"></a><span data-ttu-id="dfba9-107">Workflow je systém</span><span class="sxs-lookup"><span data-stu-id="dfba9-107">Workflow is a system</span></span>

<span data-ttu-id="dfba9-108">Workflow je systém, který je spuštěn na aplikačním objektovém serveru (AOS).</span><span class="sxs-lookup"><span data-stu-id="dfba9-108">Workflow is a system that runs on the Application Object Server (AOS).</span></span> <span data-ttu-id="dfba9-109">Systém workflowu nabízí funkce, pomocí kterých lze vytvářet individuální workflowy nebo obchodní procesy.</span><span class="sxs-lookup"><span data-stu-id="dfba9-109">The workflow system provides functionality that you can use to create individual workflows, or business processes.</span></span>

### <a name="workflow-is-a-business-process"></a><span data-ttu-id="dfba9-110">Workflow je obchodní proces</span><span class="sxs-lookup"><span data-stu-id="dfba9-110">Workflow is a business process</span></span>

<span data-ttu-id="dfba9-111">Workflow představuje obchodní proces.</span><span class="sxs-lookup"><span data-stu-id="dfba9-111">A workflow represents a business process.</span></span> <span data-ttu-id="dfba9-112">Definuje tok dokumentu nebo jeho procházení systémem zobrazením, kdo musí splnit úkol, provádět rozhodování nebo schválení dokumentu.</span><span class="sxs-lookup"><span data-stu-id="dfba9-112">It defines how a document flows, or moves, through the system by showing who must complete a task, make a decision, or approve a document.</span></span> <span data-ttu-id="dfba9-113">Následující obrázek znázorňuje příklad workflowu pro sestavy výdajů.</span><span class="sxs-lookup"><span data-stu-id="dfba9-113">For example, the following illustration shows a workflow for expense reports.</span></span>

![Workflow s prvky, které jsou přiřazeny uživatelům](./media/workflow_user.gif)

<span data-ttu-id="dfba9-115">Abychom lépe pochopili tento workflow, předpokládejme, že Stanislav odešle vyúčtování výdajů s částkou 7 000 USD.</span><span class="sxs-lookup"><span data-stu-id="dfba9-115">To better understand this workflow, suppose that Sam submits an expense report for USD 7,000.</span></span> <span data-ttu-id="dfba9-116">V tomto scénáři musí Ivan zkontrolovat účtenky, které mu Stanislav předal.</span><span class="sxs-lookup"><span data-stu-id="dfba9-116">In this scenario, Ivan must review the receipts that Sam routes to him.</span></span> <span data-ttu-id="dfba9-117">Poté musí být vyúčtování výdajů schváleno Františkem a Šárkou.</span><span class="sxs-lookup"><span data-stu-id="dfba9-117">Then Frank and Sue must approve the expense report.</span></span> <span data-ttu-id="dfba9-118">Nyní předpokládejme, že Stanislav odešle vyúčtování výdajů s částkou 11 000 USD.</span><span class="sxs-lookup"><span data-stu-id="dfba9-118">Now suppose that Sam submits an expense report for USD 11,000.</span></span> <span data-ttu-id="dfba9-119">V tomto scénáři musí Ivan zkontrolovat účtenky a František, Šárka a Anna musí toto vyúčtování výdajů schválit.</span><span class="sxs-lookup"><span data-stu-id="dfba9-119">In this scenario, Ivan must review the receipts, and Frank, Sue, and Ann must approve the expense report.</span></span>

## <a name="benefits-of-using-the-workflow-system"></a><span data-ttu-id="dfba9-120"> Výhody používání systému workflowu</span><span class="sxs-lookup"><span data-stu-id="dfba9-120">Benefits of using the workflow system</span></span>

<span data-ttu-id="dfba9-121">Používání systému workflowu v organizaci má několik výhod:</span><span class="sxs-lookup"><span data-stu-id="dfba9-121">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="dfba9-122">**Konzistentní procesy:** – Můžete definovat schvalovací proces pro specifické dokumenty, například nákupní požadavky a vyúčtování výdajů.</span><span class="sxs-lookup"><span data-stu-id="dfba9-122">**Consistent processes** – You can define how specific documents, such as purchase requisitions and expense reports, are processed.</span></span> <span data-ttu-id="dfba9-123">Používáním systému workflowu lze zajistit, aby byly dokumenty zpracovávány a schvalovány jednotným a efektivním způsobem.</span><span class="sxs-lookup"><span data-stu-id="dfba9-123">By using the workflow system, you ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="dfba9-124">**Viditelnost procesů:** – Můžete sledovat stav, historii a výkonnostní metriku instancí workflowu.</span><span class="sxs-lookup"><span data-stu-id="dfba9-124">**Process visibility** – You can track the status, history, and performance metrics of workflow instances.</span></span> <span data-ttu-id="dfba9-125">To umožňuje určit, zda je potřeba provést změny workflowu ke zvýšení efektivity.</span><span class="sxs-lookup"><span data-stu-id="dfba9-125">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="dfba9-126">**Centralizovaný seznam pracovních položek** – Uživatelé mohou zobrazit centralizovaný seznam pracovních položek k zobrazení úkolů workflowu a schválení, které mají přiřazeny.</span><span class="sxs-lookup"><span data-stu-id="dfba9-126">**Centralized work list** – Users can view a centralized work list that displays the workflow tasks and approvals that are assigned to them.</span></span>


## <a name="workflow-content"></a><span data-ttu-id="dfba9-127">Obsah workflowu</span><span class="sxs-lookup"><span data-stu-id="dfba9-127">Workflow content</span></span>

+ [<span data-ttu-id="dfba9-128">Architektura workflowu</span><span class="sxs-lookup"><span data-stu-id="dfba9-128">Workflow architecture</span></span>](workflow-system-architecture.md)
+ [<span data-ttu-id="dfba9-129">Prvky workflowu</span><span class="sxs-lookup"><span data-stu-id="dfba9-129">Workflow elements</span></span>](workflow-elements.md)
+ [<span data-ttu-id="dfba9-130">Akce workflowu</span><span class="sxs-lookup"><span data-stu-id="dfba9-130">Workflow actions</span></span>](workflow-actions.md)
+ [<span data-ttu-id="dfba9-131">Vytvoření workflowu</span><span class="sxs-lookup"><span data-stu-id="dfba9-131">Create a workflow</span></span>](create-workflow.md)
+ [<span data-ttu-id="dfba9-132">Konfigurace vlastností workflowu</span><span class="sxs-lookup"><span data-stu-id="dfba9-132">Configure workflow properties</span></span>](configure-workflow-properties.md)
+ [<span data-ttu-id="dfba9-133">Konfigurace ruční úlohy ve workflowu</span><span class="sxs-lookup"><span data-stu-id="dfba9-133">Configure a manual task in a workflow</span></span>](configure-manual-task-workflow.md)
+ [<span data-ttu-id="dfba9-134">Konfigurace automatizované úlohy ve workflowu</span><span class="sxs-lookup"><span data-stu-id="dfba9-134">Configure an automated task in a workflow</span></span>](configure-automated-task-workflow.md)
+ [<span data-ttu-id="dfba9-135">Konfigurace schvalovacího procesu ve workflowu</span><span class="sxs-lookup"><span data-stu-id="dfba9-135">Configure an approval process in a workflow</span></span>](configure-approval-process-workflow.md)
+ [<span data-ttu-id="dfba9-136">Konfigurace schvalovacího kroku ve workflowu</span><span class="sxs-lookup"><span data-stu-id="dfba9-136">Configure an approval step in a workflow</span></span>](configure-approval-step-workflow.md)
+ [<span data-ttu-id="dfba9-137">Konfigurace ručního rozhodnutí ve workflowu</span><span class="sxs-lookup"><span data-stu-id="dfba9-137">Configure a manual decision in a workflow</span></span>](configure-manual-decision-workflow.md)
+ [<span data-ttu-id="dfba9-138">Konfigurace podmíněného rozhodnutí ve workflowu</span><span class="sxs-lookup"><span data-stu-id="dfba9-138">Configure a conditional decision in a workflow</span></span>](configure-conditional-decision-workflow.md)
+ [<span data-ttu-id="dfba9-139">Konfigurace paralelních aktivit ve workflowu</span><span class="sxs-lookup"><span data-stu-id="dfba9-139">Configure a parallel activity in a workflow</span></span>](configure-parallel-activity-workflow.md)
+ [<span data-ttu-id="dfba9-140">Konfigurace paralelní větve ve workflowu</span><span class="sxs-lookup"><span data-stu-id="dfba9-140">Configure a parallel branch in a workflow</span></span>](configure-parallel-branch-workflow.md)
+ [<span data-ttu-id="dfba9-141">Konfigurace workflow položky řádku</span><span class="sxs-lookup"><span data-stu-id="dfba9-141">Configure a line-item workflow</span></span>](configure-line-item-workflow.md)
+ [<span data-ttu-id="dfba9-142">Workflow – Často kladené otázky</span><span class="sxs-lookup"><span data-stu-id="dfba9-142">Workflow FAQ</span></span>](workflow-FAQ.md)
