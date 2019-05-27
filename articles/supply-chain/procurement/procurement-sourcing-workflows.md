---
title: Workflowy zásobování a zdrojů
description: Některé organizace vyžadují, aby nákupní žádanky a nákupní objednávky byly schváleny uživatelem, který se liší od osoby, která transakci vytvořila. Workflow můžete vytvořit za účelem nastavení schvalovacího procesu.
author: mkirknel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d25ca64fb6a3fa7d7898ec68568703f3de7b1595
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1572712"
---
# <a name="procurement-and-sourcing-workflows"></a><span data-ttu-id="21f1f-104">Workflowy zásobování a zdrojů</span><span class="sxs-lookup"><span data-stu-id="21f1f-104">Procurement and sourcing workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="21f1f-105">Některé organizace vyžadují, aby nákupní žádanky a nákupní objednávky byly schváleny uživatelem, který se liší od osoby, která transakci vytvořila.</span><span class="sxs-lookup"><span data-stu-id="21f1f-105">Some organizations require that purchase requisitions and purchase orders are approved by a user other than the person who entered the transaction.</span></span> <span data-ttu-id="21f1f-106">Workflow můžete vytvořit za účelem nastavení schvalovacího procesu.</span><span class="sxs-lookup"><span data-stu-id="21f1f-106">To set up an approval process, you can create a workflow.</span></span>

<span data-ttu-id="21f1f-107">Workflow představuje obchodní proces.</span><span class="sxs-lookup"><span data-stu-id="21f1f-107">A workflow represents a business process.</span></span> <span data-ttu-id="21f1f-108">Definuje, jakým způsobem dokument prochází systémem a určuje, kdo musí zpracovat úkol nebo schválit dokument.</span><span class="sxs-lookup"><span data-stu-id="21f1f-108">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="21f1f-109">Používání systému workflowu v organizaci má několik výhod:</span><span class="sxs-lookup"><span data-stu-id="21f1f-109">There are several benefits of using the workflow system in your organization:</span></span>
-   <span data-ttu-id="21f1f-110">**Konzistentní procesy:** Můžete definovat schvalovací proces pro specifické dokumenty, například nákupní požadavky a vyúčtování výdajů.</span><span class="sxs-lookup"><span data-stu-id="21f1f-110">**Consistent processes**— You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="21f1f-111">Používáním systému workflowu lze zajistit, aby byly dokumenty zpracovávány a schvalovány jednotným a efektivním způsobem.</span><span class="sxs-lookup"><span data-stu-id="21f1f-111">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
-   <span data-ttu-id="21f1f-112">**Viditelnost procesů:** –Můžete sledovat stav, historii a výkonnostní metriku konkrétní instance workflowu.</span><span class="sxs-lookup"><span data-stu-id="21f1f-112">**Process visibility**— You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="21f1f-113">To umožňuje určit, zda je potřeba provést změny workflowu ke zvýšení efektivity.</span><span class="sxs-lookup"><span data-stu-id="21f1f-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
-   <span data-ttu-id="21f1f-114">**Centralizovaný seznam pracovních položek**: Uživatelé mohou zobrazit centralizovaný seznam pracovních položek, když chtějí zobrazit úkoly workflowu a schválení, která jsou k nim přiřazená v rámci všech workflowů, kterých se účastní.</span><span class="sxs-lookup"><span data-stu-id="21f1f-114">**Centralized work list**— Users can view a centralized work list to view the workflow tasks and approvals assigned to them across all workflows they participate in.</span></span> <span data-ttu-id="21f1f-115">To je k dispozici na stránce Pracovní položky.</span><span class="sxs-lookup"><span data-stu-id="21f1f-115">This is available in the Work items page.</span></span>

## <a name="the-types-of-workflows-that-you-can-create"></a><span data-ttu-id="21f1f-116"> Typy workflowů, které můžete vytvářet</span><span class="sxs-lookup"><span data-stu-id="21f1f-116">The types of workflows that you can create</span></span>
<span data-ttu-id="21f1f-117">Následující typy workflowu jsou k dispozici pro modul Zásobování a zdroje.</span><span class="sxs-lookup"><span data-stu-id="21f1f-117">The following workflow types are available for Procurement and sourcing.</span></span>

|                                  |                                                               |
|----------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="21f1f-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="21f1f-118">**Type**</span></span>                         | <span data-ttu-id="21f1f-119">**Tento typ slouží k:**</span><span class="sxs-lookup"><span data-stu-id="21f1f-119">**Use this type to**</span></span>                                          |
| <span data-ttu-id="21f1f-120">Kontrola nákupních žádanek</span><span class="sxs-lookup"><span data-stu-id="21f1f-120">Purchase requisition review</span></span>      | <span data-ttu-id="21f1f-121">Vytvořte kontrolu a workflow schvalování pro nákupní požadavky</span><span class="sxs-lookup"><span data-stu-id="21f1f-121">Create review and approval workflows for purchase requisitions.</span></span>            |
| <span data-ttu-id="21f1f-122">Kontrola řádku nákupní žádanky</span><span class="sxs-lookup"><span data-stu-id="21f1f-122">Purchase requisition line review</span></span> | <span data-ttu-id="21f1f-123">Vytvořte kontrolu a workflow schvalování pro řádky nákupního požadavku.</span><span class="sxs-lookup"><span data-stu-id="21f1f-123">Create review and approval workflows for purchase requisition lines.</span></span>       |
| <span data-ttu-id="21f1f-124">Workflow nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="21f1f-124">Purchase order workflow</span></span>          | <span data-ttu-id="21f1f-125">Vytváření workflowů kontroly a schvalování pro nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="21f1f-125">Create review and approval workflows for purchase orders.</span></span>     |
| <span data-ttu-id="21f1f-126">Workflow řádku nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="21f1f-126">Purchase order line workflow</span></span>     | <span data-ttu-id="21f1f-127">Vytváření workflowů kontroly a schvalování pro řádky nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="21f1f-127">Create review and approve workflows for purchase order lines.</span></span> |
| <span data-ttu-id="21f1f-128">Workflow přihlášky přidání dodavatele</span><span class="sxs-lookup"><span data-stu-id="21f1f-128">Vendor add application workflow</span></span>  | <span data-ttu-id="21f1f-129">Vytvořte kontrolu a workflow schvalování pro přidání nových dodavatelů prostřednictvím oslovení dodavatele.</span><span class="sxs-lookup"><span data-stu-id="21f1f-129">Create review and approval workflows for adding new vendors via vendor requests.</span></span> |

## <a name="creating-a-workflow"></a><span data-ttu-id="21f1f-130">Vytvoření workflowu</span><span class="sxs-lookup"><span data-stu-id="21f1f-130">Creating a workflow</span></span>

<span data-ttu-id="21f1f-131">Chcete-li vytvořit workflow, přejděte do nabídky Zásobování a zdroje &gt; Nastavení &gt; Workflowy zásobování a zdrojů a vytvořte nový workflow tak, že vyberete požadovaný typ workflowu k vytvoření.</span><span class="sxs-lookup"><span data-stu-id="21f1f-131">To create a workflow, go to Procurement and sourcing &gt; Setup &gt; Procurement and sourcing workflows and create a new workflow by selecting the type of workflow you want to create.</span></span>  

<span data-ttu-id="21f1f-132">Na plátně workflowu můžete přetahovat prvky workflowu do návrháře a spojovat prvky do toku</span><span class="sxs-lookup"><span data-stu-id="21f1f-132">In the workflow canvas you can drag workflow elements into the designer and link the elements into a flow.</span></span> <span data-ttu-id="21f1f-133">Prvky workflowu je třeba konfigurovat.</span><span class="sxs-lookup"><span data-stu-id="21f1f-133">The workflow elements should be configured.</span></span> <span data-ttu-id="21f1f-134">Co se týká prvků workflowu pro schválení a úlohy, můžete nastavit, který účastník má provést akci.</span><span class="sxs-lookup"><span data-stu-id="21f1f-134">For approval and task workflow elements you can configure which participant should take action.</span></span>

## <a name="types-of-participants"></a><span data-ttu-id="21f1f-135">Typy účastníků</span><span class="sxs-lookup"><span data-stu-id="21f1f-135">Types of participants</span></span>

<span data-ttu-id="21f1f-136">Můžete přiřadit krok schválení k následujícím skupinám účastníků.</span><span class="sxs-lookup"><span data-stu-id="21f1f-136">You can assign an approval step to the following groups of participants.</span></span>

| <span data-ttu-id="21f1f-137">Skupina uživatelů</span><span class="sxs-lookup"><span data-stu-id="21f1f-137">User group</span></span>    | <span data-ttu-id="21f1f-138">Popis</span><span class="sxs-lookup"><span data-stu-id="21f1f-138">Description</span></span>                                                               |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="21f1f-139">Účastník</span><span class="sxs-lookup"><span data-stu-id="21f1f-139">Participant</span></span>   | <span data-ttu-id="21f1f-140">Přiřaďte krok schválení členům skupiny nebo role.</span><span class="sxs-lookup"><span data-stu-id="21f1f-140">Assign the approval step to members of a group or role.</span></span>                   |
| <span data-ttu-id="21f1f-141">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="21f1f-141">Hierarchy</span></span>     | <span data-ttu-id="21f1f-142">Přiřaďte krok schválení k uživatelům v určité organizační hierarchii.</span><span class="sxs-lookup"><span data-stu-id="21f1f-142">Assign the approval step to users in a specific organizational hierarchy.</span></span> |
| <span data-ttu-id="21f1f-143">Uživatel workflowu</span><span class="sxs-lookup"><span data-stu-id="21f1f-143">Workflow user</span></span> | <span data-ttu-id="21f1f-144">Přiřaďte krok schválení uživatelům tohoto pracovního postupu.</span><span class="sxs-lookup"><span data-stu-id="21f1f-144">Assign the approval step to users of this workflow.</span></span>                       |
| <span data-ttu-id="21f1f-145">Fronta</span><span class="sxs-lookup"><span data-stu-id="21f1f-145">Queue</span></span>         | <span data-ttu-id="21f1f-146">Přiřaďte kroku schválení frontě pracovních položek.</span><span class="sxs-lookup"><span data-stu-id="21f1f-146">Assign the approval step to a work item queue.</span></span>                            |
| <span data-ttu-id="21f1f-147">Uživatel</span><span class="sxs-lookup"><span data-stu-id="21f1f-147">User</span></span>          | <span data-ttu-id="21f1f-148">Přiřaďte krok schválení konkrétním uživatelům.</span><span class="sxs-lookup"><span data-stu-id="21f1f-148">Assign the approval step to specific users.</span></span>                               |



## <a name="additional-resources"></a><span data-ttu-id="21f1f-149">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="21f1f-149">Additional resources</span></span>

- [<span data-ttu-id="21f1f-150">Definování workflowů pracovních postupů pro nákupní žádanky</span><span class="sxs-lookup"><span data-stu-id="21f1f-150">Defining business process workflows for purchase requisitions</span></span>](https://mbs.microsoft.com/customersource/Global/AX/learning/documentation/white-papers/Defining_business_process_workflows_for_purchase_requisitions)

- [<span data-ttu-id="21f1f-151">Workflow nákupního požadavku</span><span class="sxs-lookup"><span data-stu-id="21f1f-151">Purchase requisition workflow</span></span>](purchase-requisitions-workflow.md)

- [<span data-ttu-id="21f1f-152">Nabírání dodavatelů</span><span class="sxs-lookup"><span data-stu-id="21f1f-152">Onboarding vendors</span></span>](vendor-onboarding.md)

