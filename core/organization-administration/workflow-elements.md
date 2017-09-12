---
title: Prvky workflowu
description: "Tento článek popisuje různé prvky, které tvoří workflow."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 56441
ms.assetid: de740262-6ffd-42b9-a325-540eae5cec94
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 5620a91ff9f300bed782170307a295ab79fc5b2e
ms.contentlocale: cs-cz
ms.lasthandoff: 07/18/2017

---

# <a name="workflow-elements"></a><span data-ttu-id="5e054-103">Prvky workflowu</span><span class="sxs-lookup"><span data-stu-id="5e054-103">Workflow elements</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="5e054-104">Tento článek popisuje různé prvky, které tvoří workflow.</span><span class="sxs-lookup"><span data-stu-id="5e054-104">This article describes the various elements that make up a workflow.</span></span>

<span data-ttu-id="5e054-105">Workflow se skládá z jednotlivých prvků.</span><span class="sxs-lookup"><span data-stu-id="5e054-105">A workflow consists of elements.</span></span> <span data-ttu-id="5e054-106">Následující části popisují jednotlivé typy prvků.</span><span class="sxs-lookup"><span data-stu-id="5e054-106">The sections that follow describe each type of element.</span></span>

## <a name="tasks"></a><span data-ttu-id="5e054-107">Úkoly</span><span class="sxs-lookup"><span data-stu-id="5e054-107">Tasks</span></span>
<span data-ttu-id="5e054-108">*Úkol* je jednotka práce, kterou se musí provést.</span><span class="sxs-lookup"><span data-stu-id="5e054-108">A *task* is a unit of work that must be performed.</span></span> <span data-ttu-id="5e054-109">Dva typy úkolů lze přidat do workflowu: ruční a automatizované úlohy.</span><span class="sxs-lookup"><span data-stu-id="5e054-109">Two types of tasks can be added to a workflow: manual tasks and automated tasks.</span></span>

### <a name="manual-task"></a><span data-ttu-id="5e054-110">Ruční úkol</span><span class="sxs-lookup"><span data-stu-id="5e054-110">Manual task</span></span>

<span data-ttu-id="5e054-111">*Ruční úkol* je jednotka práce, kterou musí provést uživatel.</span><span class="sxs-lookup"><span data-stu-id="5e054-111">A *manual task* is a unit of work that must be performed by a user.</span></span> <span data-ttu-id="5e054-112">Workflow vyúčtování výdajů může mít například ruční úkoly, které musí mít přiřazeny uživatele pro dokončení následujících akcí:</span><span class="sxs-lookup"><span data-stu-id="5e054-112">For example, an expense report workflow can have manual tasks that require the assigned users to complete the following actions:</span></span>

-   <span data-ttu-id="5e054-113">Kontrola příjmových dokladů, které byly odeslány společně s vyúčtováním výdajů.</span><span class="sxs-lookup"><span data-stu-id="5e054-113">Review the receipts that are submitted together with an expense report.</span></span>
-   <span data-ttu-id="5e054-114">Kontaktování manažera zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="5e054-114">Call an employee's manager.</span></span>

### <a name="automated-task"></a><span data-ttu-id="5e054-115">Automatizovaný úkol</span><span class="sxs-lookup"><span data-stu-id="5e054-115">Automated task</span></span>

<span data-ttu-id="5e054-116">*Automatizovaný úkol* je jednotka práce, kterou musí provést systém.</span><span class="sxs-lookup"><span data-stu-id="5e054-116">An *automated task* is a unit of work that must be performed by the system.</span></span> <span data-ttu-id="5e054-117">Není požadován lidský zásah.</span><span class="sxs-lookup"><span data-stu-id="5e054-117">No human interaction is required.</span></span> <span data-ttu-id="5e054-118">Workflow prodejní objednávky může mít například automatizované úkoly, které vyžadují systém pro dokončení následujících akcí:</span><span class="sxs-lookup"><span data-stu-id="5e054-118">For example, a sales order workflow can have automated tasks that require the system to complete the following actions:</span></span>

-   <span data-ttu-id="5e054-119">Provedení kontroly úvěru.</span><span class="sxs-lookup"><span data-stu-id="5e054-119">Perform a credit check.</span></span>
-   <span data-ttu-id="5e054-120">Vytvoření záznamu odběratele pro odběratele, pokud záznam již neexistuje.</span><span class="sxs-lookup"><span data-stu-id="5e054-120">Create a customer record for the customer, if a record doesn't already exist.</span></span>

## <a name="approval-processes"></a><span data-ttu-id="5e054-121">Schvalovací procesy</span><span class="sxs-lookup"><span data-stu-id="5e054-121">Approval processes</span></span>
<span data-ttu-id="5e054-122">*Schvalovací proces* je proces, který se skládá ze samostatných kroků.</span><span class="sxs-lookup"><span data-stu-id="5e054-122">An *approval process* is a process that consists of separate steps.</span></span> <span data-ttu-id="5e054-123">V každém schvalovacím kroku může uživatel provádět následující akce:</span><span class="sxs-lookup"><span data-stu-id="5e054-123">At each approval step, the user can perform the following actions:</span></span>

-   <span data-ttu-id="5e054-124">Schválit dokument.</span><span class="sxs-lookup"><span data-stu-id="5e054-124">Approve the document.</span></span>
-   <span data-ttu-id="5e054-125">Odmítnout dokument.</span><span class="sxs-lookup"><span data-stu-id="5e054-125">Reject the document.</span></span>
-   <span data-ttu-id="5e054-126">Zadat požadavek na změnu dokumentu.</span><span class="sxs-lookup"><span data-stu-id="5e054-126">Request a change to the document.</span></span>
-   <span data-ttu-id="5e054-127">Postoupit dokument ke schválení jinému uživateli.</span><span class="sxs-lookup"><span data-stu-id="5e054-127">Assign the document to another user for approval.</span></span>

## <a name="lineitem-workflow-elements"></a><span data-ttu-id="5e054-128">Prvky pracovního procesu řádkové položky</span><span class="sxs-lookup"><span data-stu-id="5e054-128">Lineitem workflow elements</span></span>
<span data-ttu-id="5e054-129">Workflow lze vytvořit pro zpracování dokumentů nebo položek řádku v dokumentu.</span><span class="sxs-lookup"><span data-stu-id="5e054-129">A workflow can be created to process either documents or the line items on a document.</span></span> <span data-ttu-id="5e054-130">Například vytvoříte workflow schválení pro časové rozvrhy.</span><span class="sxs-lookup"><span data-stu-id="5e054-130">For example, you've created an approval workflow for timesheets.</span></span> <span data-ttu-id="5e054-131">(Tento pracovní postup budeme označovat jako *pracovní postup dokumentu*.) K tomuto pracovnímu procesu dokumentu můžete přidat prvek *pracovního postupu řádkové položky*.</span><span class="sxs-lookup"><span data-stu-id="5e054-131">(We will refer to this workflow as the *document workflow*.) You can add a *line-item workflow* element to that document workflow.</span></span> <span data-ttu-id="5e054-132">Při spuštění prvku položky řádku je každá položka řádku v dokumentu odeslána ke zpracování.</span><span class="sxs-lookup"><span data-stu-id="5e054-132">When the line-item element is run, each line item on the document is submitted for processing.</span></span> <span data-ttu-id="5e054-133">Je vhodné řádkové položky zpracovávat ve stejném workflowu položky řádku, nebo můžete každou položku řádku zpracovat jiným workflowem položky řádku.</span><span class="sxs-lookup"><span data-stu-id="5e054-133">You might want all the line items to be processed by the same line-item workflow, or you might want each line item to be processed by a different line-item workflow.</span></span> <span data-ttu-id="5e054-134">Představte si, že zaměstnanec odeslal časový rozvrh, který se podobá na následujícímu obrázku.</span><span class="sxs-lookup"><span data-stu-id="5e054-134">Imagine that an employee has submitted a timesheet that resembles the following figure.</span></span> <span data-ttu-id="5e054-135">![Workflow s položkami řádků](./media/workflow_lineitemworkflow.gif) V takovém případě můžete vytvořit následující workflow položky řádku:</span><span class="sxs-lookup"><span data-stu-id="5e054-135">![Workflow with line items](./media/workflow_lineitemworkflow.gif) In this scenario, you might want to create the following line-item workflows:</span></span>

-   <span data-ttu-id="5e054-136">**Workflow položky řádku 1** – tento workflow slouží pro zpracování položek řádků, ve kterém je ID projektu 1111.</span><span class="sxs-lookup"><span data-stu-id="5e054-136">**Line-item workflow 1** – This workflow is used to process line items where the project ID is 1111.</span></span>
-   <span data-ttu-id="5e054-137">**Workflow položky řádku 2** – tento workflow slouží pro zpracování položek řádků, ve kterém je ID projektu 2222.</span><span class="sxs-lookup"><span data-stu-id="5e054-137">**Line-item workflow 2** – This workflow is used to process line items where the project ID is 2222.</span></span>
-   <span data-ttu-id="5e054-138">**Workflow položky řádku 3** – tento workflow slouží pro zpracování položek řádků, ve kterém je ID projektu 3333.</span><span class="sxs-lookup"><span data-stu-id="5e054-138">**Line-item workflow 3** – This workflow is used to process line items where the project ID is 3333.</span></span>

## <a name="flowcontrol-elements"></a><span data-ttu-id="5e054-139">Prvky ovládání toku</span><span class="sxs-lookup"><span data-stu-id="5e054-139">Flowcontrol elements</span></span>
<span data-ttu-id="5e054-140">Následující prvky umožňují navrhovat workflowy, které mají alternativní větve nebo větve, které běží současně</span><span class="sxs-lookup"><span data-stu-id="5e054-140">The following elements let you design workflows that have alternate branches or branches that run at the same time.</span></span>

### <a name="manual-decision"></a><span data-ttu-id="5e054-141">Ruční rozhodnutí</span><span class="sxs-lookup"><span data-stu-id="5e054-141">Manual decision</span></span>

<span data-ttu-id="5e054-142">*Ruční rozhodnutí* je bod, ve kterém se workflow dělí na dvě větve.</span><span class="sxs-lookup"><span data-stu-id="5e054-142">A *manual decision* is a point where a workflow divides into two branches.</span></span> <span data-ttu-id="5e054-143">Uživatel se musí rozhodnout, a toto rozhodnutí určí, která větev bude použita ke zpracování dokumentu, který byl odeslán.</span><span class="sxs-lookup"><span data-stu-id="5e054-143">A user must make a decision, and this decision determines which branch is used to process the document that was submitted.</span></span>

### <a name="conditional-decision"></a><span data-ttu-id="5e054-144">Podmíněné rozhodnutí</span><span class="sxs-lookup"><span data-stu-id="5e054-144">Conditional decision</span></span>

<span data-ttu-id="5e054-145">*Podmíněné rozhodnutí* je také bod, ve kterém se workflow dělí na dvě větve.</span><span class="sxs-lookup"><span data-stu-id="5e054-145">A *conditional decision* is also a point where a workflow divides into two branches.</span></span> <span data-ttu-id="5e054-146">Systém však rozhodne, která větev bude použita ke zpracování dokumentu, který byl odeslán.</span><span class="sxs-lookup"><span data-stu-id="5e054-146">However, the system decides which branch is used to process the document that was submitted.</span></span> <span data-ttu-id="5e054-147">Pro rozhodování systém vyhodnotí dokument a určí, zda odpovídá zadaným podmínkám.</span><span class="sxs-lookup"><span data-stu-id="5e054-147">To make this decision, the system evaluates the document to determine whether it meets specified conditions.</span></span>

### <a name="parallel-activity"></a><span data-ttu-id="5e054-148">Paralelní aktivita</span><span class="sxs-lookup"><span data-stu-id="5e054-148">Parallel activity</span></span>

<span data-ttu-id="5e054-149">*Paralelní činnost* je prvek workflowu, jenž zahrnuje dvě nebo více větví workflowu, které jsou zpracovávány současně.</span><span class="sxs-lookup"><span data-stu-id="5e054-149">A *parallel activity* is a workflow element that includes two or more workflow branches that run at the same time.</span></span>

### <a name="subworkflow"></a><span data-ttu-id="5e054-150">Dílčí workflow</span><span class="sxs-lookup"><span data-stu-id="5e054-150">Subworkflow</span></span>

<span data-ttu-id="5e054-151">*Dílčí workflow* je workflow, který je spuštěn v kontextu jiného workflowu.</span><span class="sxs-lookup"><span data-stu-id="5e054-151">A *subworkflow* is a workflow that runs in the context of another workflow.</span></span>




