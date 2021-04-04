---
title: Prvky workflowu
description: Toto téma popisuje různé prvky, které tvoří workflow.
author: ChrisGarty
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 56441
ms.assetid: de740262-6ffd-42b9-a325-540eae5cec94
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dc8606dbf475c7429d9ded1063e94646c6084ef0
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559351"
---
# <a name="workflow-elements"></a><span data-ttu-id="c547f-103">Prvky workflowu</span><span class="sxs-lookup"><span data-stu-id="c547f-103">Workflow elements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c547f-104">Toto téma popisuje různé prvky, které tvoří workflow.</span><span class="sxs-lookup"><span data-stu-id="c547f-104">This topic describes the various elements that make up a workflow.</span></span>

<span data-ttu-id="c547f-105">Workflow se skládá z jednotlivých prvků.</span><span class="sxs-lookup"><span data-stu-id="c547f-105">A workflow consists of elements.</span></span> <span data-ttu-id="c547f-106">Následující části popisují jednotlivé typy prvků.</span><span class="sxs-lookup"><span data-stu-id="c547f-106">The sections that follow describe each type of element.</span></span>

## <a name="tasks"></a><span data-ttu-id="c547f-107">Úkoly</span><span class="sxs-lookup"><span data-stu-id="c547f-107">Tasks</span></span>

<span data-ttu-id="c547f-108">*Úkol* je jednotka práce, kterou se musí provést.</span><span class="sxs-lookup"><span data-stu-id="c547f-108">A *task* is a unit of work that must be performed.</span></span> <span data-ttu-id="c547f-109">Dva typy úkolů lze přidat do workflowu: ruční a automatizované úlohy.</span><span class="sxs-lookup"><span data-stu-id="c547f-109">Two types of tasks can be added to a workflow: manual tasks and automated tasks.</span></span>

### <a name="manual-task"></a><span data-ttu-id="c547f-110">Ruční úkol</span><span class="sxs-lookup"><span data-stu-id="c547f-110">Manual task</span></span>

<span data-ttu-id="c547f-111">*Ruční úkol* je jednotka práce, kterou musí provést uživatel.</span><span class="sxs-lookup"><span data-stu-id="c547f-111">A *manual task* is a unit of work that must be performed by a user.</span></span> <span data-ttu-id="c547f-112">Workflow vyúčtování výdajů může mít například ruční úkoly, které musí mít přiřazeny uživatele pro dokončení následujících akcí:</span><span class="sxs-lookup"><span data-stu-id="c547f-112">For example, an expense report workflow can have manual tasks that require the assigned users to complete the following actions:</span></span>

- <span data-ttu-id="c547f-113">Kontrola příjmových dokladů, které byly odeslány společně s vyúčtováním výdajů.</span><span class="sxs-lookup"><span data-stu-id="c547f-113">Review the receipts that are submitted together with an expense report.</span></span>
- <span data-ttu-id="c547f-114">Kontaktování manažera zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="c547f-114">Call an employee's manager.</span></span>

### <a name="automated-task"></a><span data-ttu-id="c547f-115">Automatizovaný úkol</span><span class="sxs-lookup"><span data-stu-id="c547f-115">Automated task</span></span>

<span data-ttu-id="c547f-116">*Automatizovaný úkol* je jednotka práce, kterou musí provést systém.</span><span class="sxs-lookup"><span data-stu-id="c547f-116">An *automated task* is a unit of work that must be performed by the system.</span></span> <span data-ttu-id="c547f-117">Není požadován lidský zásah.</span><span class="sxs-lookup"><span data-stu-id="c547f-117">No human interaction is required.</span></span> <span data-ttu-id="c547f-118">Workflow prodejní objednávky může mít například automatizované úkoly, které vyžadují systém pro dokončení následujících akcí:</span><span class="sxs-lookup"><span data-stu-id="c547f-118">For example, a sales order workflow can have automated tasks that require the system to complete the following actions:</span></span>

- <span data-ttu-id="c547f-119">Provedení kontroly úvěru.</span><span class="sxs-lookup"><span data-stu-id="c547f-119">Perform a credit check.</span></span>
- <span data-ttu-id="c547f-120">Vytvoření záznamu odběratele pro odběratele, pokud záznam již neexistuje.</span><span class="sxs-lookup"><span data-stu-id="c547f-120">Create a customer record for the customer, if a record doesn't already exist.</span></span>

## <a name="approval-processes"></a><span data-ttu-id="c547f-121">Schvalovací procesy</span><span class="sxs-lookup"><span data-stu-id="c547f-121">Approval processes</span></span>

<span data-ttu-id="c547f-122">*Schvalovací proces* je proces, který se skládá ze samostatných kroků.</span><span class="sxs-lookup"><span data-stu-id="c547f-122">An *approval process* is a process that consists of separate steps.</span></span> <span data-ttu-id="c547f-123">V každém schvalovacím kroku může uživatel provádět následující akce:</span><span class="sxs-lookup"><span data-stu-id="c547f-123">At each approval step, the user can perform the following actions:</span></span>

- <span data-ttu-id="c547f-124">Schválit dokument.</span><span class="sxs-lookup"><span data-stu-id="c547f-124">Approve the document.</span></span>
- <span data-ttu-id="c547f-125">Odmítnout dokument.</span><span class="sxs-lookup"><span data-stu-id="c547f-125">Reject the document.</span></span>
- <span data-ttu-id="c547f-126">Zadat požadavek na změnu dokumentu.</span><span class="sxs-lookup"><span data-stu-id="c547f-126">Request a change to the document.</span></span>
- <span data-ttu-id="c547f-127">Postoupit dokument ke schválení jinému uživateli.</span><span class="sxs-lookup"><span data-stu-id="c547f-127">Assign the document to another user for approval.</span></span>

## <a name="line-item-workflow-elements"></a><span data-ttu-id="c547f-128">Prvek workflowu položky řádku</span><span class="sxs-lookup"><span data-stu-id="c547f-128">Line-item workflow elements</span></span>

<span data-ttu-id="c547f-129">Workflow lze vytvořit pro zpracování dokumentů nebo položek řádku v dokumentu.</span><span class="sxs-lookup"><span data-stu-id="c547f-129">A workflow can be created to process either documents or the line items on a document.</span></span> <span data-ttu-id="c547f-130">Například vytvoříte workflow schválení pro časové rozvrhy.</span><span class="sxs-lookup"><span data-stu-id="c547f-130">For example, you've created an approval workflow for timesheets.</span></span> <span data-ttu-id="c547f-131">(Tento pracovní postup budeme označovat jako *pracovní postup dokumentu*.) K tomuto pracovnímu procesu dokumentu můžete přidat prvek *pracovního postupu řádkové položky*.</span><span class="sxs-lookup"><span data-stu-id="c547f-131">(We will refer to this workflow as the *document workflow*.) You can add a *line-item workflow* element to that document workflow.</span></span> <span data-ttu-id="c547f-132">Při spuštění prvku položky řádku je každá položka řádku v dokumentu odeslána ke zpracování.</span><span class="sxs-lookup"><span data-stu-id="c547f-132">When the line-item element is run, each line item on the document is submitted for processing.</span></span> <span data-ttu-id="c547f-133">Je vhodné řádkové položky zpracovávat ve stejném workflowu položky řádku, nebo můžete každou položku řádku zpracovat jiným workflowem položky řádku.</span><span class="sxs-lookup"><span data-stu-id="c547f-133">You might want all the line items to be processed by the same line-item workflow, or you might want each line item to be processed by a different line-item workflow.</span></span> <span data-ttu-id="c547f-134">Představte si, že zaměstnanec odeslal časový rozvrh, který se podobá na následujícímu obrázku.</span><span class="sxs-lookup"><span data-stu-id="c547f-134">Imagine that an employee has submitted a timesheet that resembles the following figure.</span></span>

![Workflow položek na řádku](./media/workflow_lineitemworkflow.gif)

<span data-ttu-id="c547f-136">V tomto scénáři může být třeba vytvořit následující workflowy položky řádku:</span><span class="sxs-lookup"><span data-stu-id="c547f-136">In this scenario, you might want to create the following line-item workflows:</span></span>

- <span data-ttu-id="c547f-137">**Workflow položky řádku 1** – tento workflow slouží pro zpracování položek řádků, ve kterém je ID projektu 1111.</span><span class="sxs-lookup"><span data-stu-id="c547f-137">**Line-item workflow 1** – This workflow is used to process line items where the project ID is 1111.</span></span>
- <span data-ttu-id="c547f-138">**Workflow položky řádku 2** – tento workflow slouží pro zpracování položek řádků, ve kterém je ID projektu 2222.</span><span class="sxs-lookup"><span data-stu-id="c547f-138">**Line-item workflow 2** – This workflow is used to process line items where the project ID is 2222.</span></span>
- <span data-ttu-id="c547f-139">**Workflow položky řádku 3** – tento workflow slouží pro zpracování položek řádků, ve kterém je ID projektu 3333.</span><span class="sxs-lookup"><span data-stu-id="c547f-139">**Line-item workflow 3** – This workflow is used to process line items where the project ID is 3333.</span></span>

## <a name="flow-control-elements"></a><span data-ttu-id="c547f-140">Prvky ovládání toku</span><span class="sxs-lookup"><span data-stu-id="c547f-140">Flow-control elements</span></span>

<span data-ttu-id="c547f-141">Následující prvky umožňují navrhovat workflowy, které mají alternativní větve nebo větve, které běží současně</span><span class="sxs-lookup"><span data-stu-id="c547f-141">The following elements let you design workflows that have alternate branches or branches that run at the same time.</span></span>

### <a name="manual-decision"></a><span data-ttu-id="c547f-142">Ruční rozhodnutí</span><span class="sxs-lookup"><span data-stu-id="c547f-142">Manual decision</span></span>

<span data-ttu-id="c547f-143">*Ruční rozhodnutí* je bod, ve kterém se workflow dělí na dvě větve.</span><span class="sxs-lookup"><span data-stu-id="c547f-143">A *manual decision* is a point where a workflow divides into two branches.</span></span> <span data-ttu-id="c547f-144">Uživatel se musí rozhodnout, a toto rozhodnutí určí, která větev bude použita ke zpracování dokumentu, který byl odeslán.</span><span class="sxs-lookup"><span data-stu-id="c547f-144">A user must make a decision, and this decision determines which branch is used to process the document that was submitted.</span></span>

### <a name="conditional-decision"></a><span data-ttu-id="c547f-145">Podmíněné rozhodnutí</span><span class="sxs-lookup"><span data-stu-id="c547f-145">Conditional decision</span></span>

<span data-ttu-id="c547f-146">*Podmíněné rozhodnutí* je také bod, ve kterém se workflow dělí na dvě větve.</span><span class="sxs-lookup"><span data-stu-id="c547f-146">A *conditional decision* is also a point where a workflow divides into two branches.</span></span> <span data-ttu-id="c547f-147">Systém však rozhodne, která větev bude použita ke zpracování dokumentu, který byl odeslán.</span><span class="sxs-lookup"><span data-stu-id="c547f-147">However, the system decides which branch is used to process the document that was submitted.</span></span> <span data-ttu-id="c547f-148">Pro rozhodování systém vyhodnotí dokument a určí, zda odpovídá zadaným podmínkám.</span><span class="sxs-lookup"><span data-stu-id="c547f-148">To make this decision, the system evaluates the document to determine whether it meets specified conditions.</span></span>

### <a name="parallel-activity"></a><span data-ttu-id="c547f-149">Paralelní aktivita</span><span class="sxs-lookup"><span data-stu-id="c547f-149">Parallel activity</span></span>

<span data-ttu-id="c547f-150">*Paralelní činnost* je prvek workflowu, jenž zahrnuje dvě nebo více větví workflowu, které jsou zpracovávány současně.</span><span class="sxs-lookup"><span data-stu-id="c547f-150">A *parallel activity* is a workflow element that includes two or more workflow branches that run at the same time.</span></span>

### <a name="subworkflow"></a><span data-ttu-id="c547f-151">Dílčí workflow</span><span class="sxs-lookup"><span data-stu-id="c547f-151">Subworkflow</span></span>

<span data-ttu-id="c547f-152">*Dílčí workflow* je workflow, který je spuštěn v kontextu jiného workflowu.</span><span class="sxs-lookup"><span data-stu-id="c547f-152">A *subworkflow* is a workflow that runs in the context of another workflow.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]