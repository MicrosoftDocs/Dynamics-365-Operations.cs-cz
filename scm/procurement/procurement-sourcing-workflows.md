---
title: "Workflowy zásobování a zdrojů"
description: "Některé organizace vyžadují, aby nákupní žádanky a nákupní objednávky byly schváleny uživatelem, který se liší od osoby, která transakci vytvořila. Workflow můžete vytvořit za účelem nastavení schvalovacího procesu."
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 80853a06e599786e2dcaf049ac733c47dfe4d9a5
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---

# <a name="procurement-and-sourcing-workflows"></a><span data-ttu-id="b2e59-104">Workflowy zásobování a zdrojů</span><span class="sxs-lookup"><span data-stu-id="b2e59-104">Procurement and sourcing workflows</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b2e59-105">Některé organizace vyžadují, aby nákupní žádanky a nákupní objednávky byly schváleny uživatelem, který se liší od osoby, která transakci vytvořila.</span><span class="sxs-lookup"><span data-stu-id="b2e59-105">Some organizations require that purchase requisitions and purchase orders are approved by a user other than the person who entered the transaction.</span></span> <span data-ttu-id="b2e59-106">Workflow můžete vytvořit za účelem nastavení schvalovacího procesu.</span><span class="sxs-lookup"><span data-stu-id="b2e59-106">To set up an approval process, you can create a workflow.</span></span>

<span data-ttu-id="b2e59-107">Workflow představuje obchodní proces.</span><span class="sxs-lookup"><span data-stu-id="b2e59-107">A workflow represents a business process.</span></span> <span data-ttu-id="b2e59-108">Definuje, jakým způsobem dokument prochází systémem a určuje, kdo musí zpracovat úkol nebo schválit dokument.</span><span class="sxs-lookup"><span data-stu-id="b2e59-108">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="b2e59-109">Používání systému workflowu v organizaci má několik výhod:</span><span class="sxs-lookup"><span data-stu-id="b2e59-109">There are several benefits of using the workflow system in your organization:</span></span>
-   <span data-ttu-id="b2e59-110">**Konzistentní procesy:** Můžete definovat schvalovací proces pro specifické dokumenty, například nákupní požadavky a vyúčtování výdajů.</span><span class="sxs-lookup"><span data-stu-id="b2e59-110">**Consistent processes**— You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="b2e59-111">Používáním systému workflowu lze zajistit, aby byly dokumenty zpracovávány a schvalovány jednotným a efektivním způsobem.</span><span class="sxs-lookup"><span data-stu-id="b2e59-111">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
-   <span data-ttu-id="b2e59-112">**Viditelnost procesů:** –Můžete sledovat stav, historii a výkonnostní metriku konkrétní instance workflowu.</span><span class="sxs-lookup"><span data-stu-id="b2e59-112">**Process visibility**— You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="b2e59-113">To umožňuje určit, zda je potřeba provést změny workflowu ke zvýšení efektivity.</span><span class="sxs-lookup"><span data-stu-id="b2e59-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
-   <span data-ttu-id="b2e59-114">**Centralizovaný seznam pracovních položek**: Uživatelé mohou zobrazit centralizovaný seznam pracovních položek, když chtějí zobrazit úkoly workflowu a schválení, která jsou k nim přiřazená v rámci všech workflowů, kterých se účastní.</span><span class="sxs-lookup"><span data-stu-id="b2e59-114">**Centralized work list**— Users can view a centralized work list to view the workflow tasks and approvals assigned to them across all workflows they participate in.</span></span> <span data-ttu-id="b2e59-115">To je k dispozici na stránce Pracovní položky.</span><span class="sxs-lookup"><span data-stu-id="b2e59-115">This is available in the Work items page.</span></span>

## <a name="the-types-of-workflows-that-you-can-create"></a><span data-ttu-id="b2e59-116"> Typy workflowů, které můžete vytvářet</span><span class="sxs-lookup"><span data-stu-id="b2e59-116">The types of workflows that you can create</span></span>
<span data-ttu-id="b2e59-117">Následující typy workflowu jsou k dispozici pro modul Zásobování a zdroje.</span><span class="sxs-lookup"><span data-stu-id="b2e59-117">The following workflow types are available for Procurement and sourcing.</span></span>

|                                  |                                                               |
|----------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="b2e59-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="b2e59-118">**Type**</span></span>                         | <span data-ttu-id="b2e59-119">**Tento typ slouží k:**</span><span class="sxs-lookup"><span data-stu-id="b2e59-119">**Use this type to**</span></span>                                          |
| <span data-ttu-id="b2e59-120">Kontrola nákupních žádanek</span><span class="sxs-lookup"><span data-stu-id="b2e59-120">Purchase requisition review</span></span>      | <span data-ttu-id="b2e59-121">Vytváření workflowů kontroly pro nákupní požadavky.</span><span class="sxs-lookup"><span data-stu-id="b2e59-121">Create review workflows for purchase requisitions.</span></span>            |
| <span data-ttu-id="b2e59-122">Kontrola řádku nákupní žádanky</span><span class="sxs-lookup"><span data-stu-id="b2e59-122">Purchase requisition line review</span></span> | <span data-ttu-id="b2e59-123">Vytváření workflowů kontroly pro řádky nákupní žádanky.</span><span class="sxs-lookup"><span data-stu-id="b2e59-123">Create review workflows for purchase requisition lines.</span></span>       |
| <span data-ttu-id="b2e59-124">Workflow nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="b2e59-124">Purchase order workflow</span></span>          | <span data-ttu-id="b2e59-125">Vytváření workflowů kontroly a schvalování pro nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="b2e59-125">Create review and approval workflows for purchase orders.</span></span>     |
| <span data-ttu-id="b2e59-126">Workflow řádku nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="b2e59-126">Purchase order line workflow</span></span>     | <span data-ttu-id="b2e59-127">Vytváření workflowů kontroly a schvalování pro řádky nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="b2e59-127">Create review and approve workflows for purchase order lines.</span></span> |

## <a name="creating-a-workflow"></a><span data-ttu-id="b2e59-128">Vytvoření workflowu</span><span class="sxs-lookup"><span data-stu-id="b2e59-128">Creating a workflow</span></span>
<span data-ttu-id="b2e59-129">Chcete-li vytvořit workflow, přejděte do nabídky Zásobování a zdroje &gt; Nastavení &gt; Workflowy zásobování a zdrojů a vytvořte nový workflow tak, že vyberete požadovaný typ workflowu k vytvoření.</span><span class="sxs-lookup"><span data-stu-id="b2e59-129">To create a workflow, go to Procurement and sourcing &gt; Setup &gt; Procurement and sourcing workflows and create a new workflow by selecting the type of workflow you want to create.</span></span>  

<span data-ttu-id="b2e59-130">Na plátně workflowu můžete přetahovat prvky workflowu do návrháře a spojovat prvky do toku</span><span class="sxs-lookup"><span data-stu-id="b2e59-130">In the workflow canvas you can drag workflow elements into the designer and link the elements into a flow.</span></span> <span data-ttu-id="b2e59-131">Prvky workflowu je třeba konfigurovat.</span><span class="sxs-lookup"><span data-stu-id="b2e59-131">The workflow elements should be configured.</span></span> <span data-ttu-id="b2e59-132">Co se týká prvků workflowu pro schválení a úlohy, můžete nastavit, který účastník má provést akci.</span><span class="sxs-lookup"><span data-stu-id="b2e59-132">For approval and task workflow elements you can configure which participant should take action.</span></span>
<span data-ttu-id="b2e59-133">Typy účastníků</span><span class="sxs-lookup"><span data-stu-id="b2e59-133">Types of participants</span></span>
----------------------

<span data-ttu-id="b2e59-134">Můžete přiřadit krok schválení k následujícím skupinám účastníků.</span><span class="sxs-lookup"><span data-stu-id="b2e59-134">You can assign an approval step to the following groups of participants.</span></span>

| <span data-ttu-id="b2e59-135">Skupina uživatelů</span><span class="sxs-lookup"><span data-stu-id="b2e59-135">User group</span></span>    | <span data-ttu-id="b2e59-136">Popis</span><span class="sxs-lookup"><span data-stu-id="b2e59-136">Description</span></span>                                                               |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="b2e59-137">Účastník</span><span class="sxs-lookup"><span data-stu-id="b2e59-137">Participant</span></span>   | <span data-ttu-id="b2e59-138">Přiřaďte krok schválení členům skupiny nebo role.</span><span class="sxs-lookup"><span data-stu-id="b2e59-138">Assign the approval step to members of a group or role.</span></span>                   |
| <span data-ttu-id="b2e59-139">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="b2e59-139">Hierarchy</span></span>     | <span data-ttu-id="b2e59-140">Přiřaďte krok schválení k uživatelům v určité organizační hierarchii.</span><span class="sxs-lookup"><span data-stu-id="b2e59-140">Assign the approval step to users in a specific organizational hierarchy.</span></span> |
| <span data-ttu-id="b2e59-141">Uživatel workflowu</span><span class="sxs-lookup"><span data-stu-id="b2e59-141">Workflow user</span></span> | <span data-ttu-id="b2e59-142">Přiřaďte krok schválení uživatelům tohoto pracovního postupu.</span><span class="sxs-lookup"><span data-stu-id="b2e59-142">Assign the approval step to users of this workflow.</span></span>                       |
| <span data-ttu-id="b2e59-143">Fronta</span><span class="sxs-lookup"><span data-stu-id="b2e59-143">Queue</span></span>         | <span data-ttu-id="b2e59-144">Přiřaďte kroku schválení frontě pracovních položek.</span><span class="sxs-lookup"><span data-stu-id="b2e59-144">Assign the approval step to a work item queue.</span></span>                            |
| <span data-ttu-id="b2e59-145">Uživatel</span><span class="sxs-lookup"><span data-stu-id="b2e59-145">User</span></span>          | <span data-ttu-id="b2e59-146">Přiřaďte krok schválení konkrétním uživatelům.</span><span class="sxs-lookup"><span data-stu-id="b2e59-146">Assign the approval step to specific users.</span></span>                               |



<a name="see-also"></a><span data-ttu-id="b2e59-147">Viz také</span><span class="sxs-lookup"><span data-stu-id="b2e59-147">See also</span></span>
--------

[<span data-ttu-id="b2e59-148">Definování workflowů pracovních postupů pro nákupní žádanky</span><span class="sxs-lookup"><span data-stu-id="b2e59-148">Defining business process workflows for purchase requisitions</span></span>](https://mbs.microsoft.com/customersource/Global/AX/learning/documentation/white-papers/Defining_business_process_workflows_for_purchase_requisitions)

[<span data-ttu-id="b2e59-149">Workflow nákupní žádanky</span><span class="sxs-lookup"><span data-stu-id="b2e59-149">Purchase requisition workflow</span></span>](purchase-requisitions-workflow.md)




