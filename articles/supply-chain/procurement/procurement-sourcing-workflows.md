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
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "330073"
---
# <a name="procurement-and-sourcing-workflows"></a><span data-ttu-id="75c7e-104">Workflowy zásobování a zdrojů</span><span class="sxs-lookup"><span data-stu-id="75c7e-104">Procurement and sourcing workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="75c7e-105">Některé organizace vyžadují, aby nákupní žádanky a nákupní objednávky byly schváleny uživatelem, který se liší od osoby, která transakci vytvořila.</span><span class="sxs-lookup"><span data-stu-id="75c7e-105">Some organizations require that purchase requisitions and purchase orders are approved by a user other than the person who entered the transaction.</span></span> <span data-ttu-id="75c7e-106">Workflow můžete vytvořit za účelem nastavení schvalovacího procesu.</span><span class="sxs-lookup"><span data-stu-id="75c7e-106">To set up an approval process, you can create a workflow.</span></span>

<span data-ttu-id="75c7e-107">Workflow představuje obchodní proces.</span><span class="sxs-lookup"><span data-stu-id="75c7e-107">A workflow represents a business process.</span></span> <span data-ttu-id="75c7e-108">Definuje, jakým způsobem dokument prochází systémem a určuje, kdo musí zpracovat úkol nebo schválit dokument.</span><span class="sxs-lookup"><span data-stu-id="75c7e-108">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="75c7e-109">Používání systému workflowu v organizaci má několik výhod:</span><span class="sxs-lookup"><span data-stu-id="75c7e-109">There are several benefits of using the workflow system in your organization:</span></span>
-   <span data-ttu-id="75c7e-110">**Konzistentní procesy:** Můžete definovat schvalovací proces pro specifické dokumenty, například nákupní požadavky a vyúčtování výdajů.</span><span class="sxs-lookup"><span data-stu-id="75c7e-110">**Consistent processes**— You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="75c7e-111">Používáním systému workflowu lze zajistit, aby byly dokumenty zpracovávány a schvalovány jednotným a efektivním způsobem.</span><span class="sxs-lookup"><span data-stu-id="75c7e-111">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
-   <span data-ttu-id="75c7e-112">**Viditelnost procesů:** –Můžete sledovat stav, historii a výkonnostní metriku konkrétní instance workflowu.</span><span class="sxs-lookup"><span data-stu-id="75c7e-112">**Process visibility**— You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="75c7e-113">To umožňuje určit, zda je potřeba provést změny workflowu ke zvýšení efektivity.</span><span class="sxs-lookup"><span data-stu-id="75c7e-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
-   <span data-ttu-id="75c7e-114">**Centralizovaný seznam pracovních položek**: Uživatelé mohou zobrazit centralizovaný seznam pracovních položek, když chtějí zobrazit úkoly workflowu a schválení, která jsou k nim přiřazená v rámci všech workflowů, kterých se účastní.</span><span class="sxs-lookup"><span data-stu-id="75c7e-114">**Centralized work list**— Users can view a centralized work list to view the workflow tasks and approvals assigned to them across all workflows they participate in.</span></span> <span data-ttu-id="75c7e-115">To je k dispozici na stránce Pracovní položky.</span><span class="sxs-lookup"><span data-stu-id="75c7e-115">This is available in the Work items page.</span></span>

## <a name="the-types-of-workflows-that-you-can-create"></a><span data-ttu-id="75c7e-116"> Typy workflowů, které můžete vytvářet</span><span class="sxs-lookup"><span data-stu-id="75c7e-116">The types of workflows that you can create</span></span>
<span data-ttu-id="75c7e-117">Následující typy workflowu jsou k dispozici pro modul Zásobování a zdroje.</span><span class="sxs-lookup"><span data-stu-id="75c7e-117">The following workflow types are available for Procurement and sourcing.</span></span>

|                                  |                                                               |
|----------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="75c7e-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="75c7e-118">**Type**</span></span>                         | <span data-ttu-id="75c7e-119">**Tento typ slouží k:**</span><span class="sxs-lookup"><span data-stu-id="75c7e-119">**Use this type to**</span></span>                                          |
| <span data-ttu-id="75c7e-120">Kontrola nákupních žádanek</span><span class="sxs-lookup"><span data-stu-id="75c7e-120">Purchase requisition review</span></span>      | <span data-ttu-id="75c7e-121">Vytvořte kontrolu a workflow schvalování pro nákupní požadavky</span><span class="sxs-lookup"><span data-stu-id="75c7e-121">Create review and approval workflows for purchase requisitions.</span></span>            |
| <span data-ttu-id="75c7e-122">Kontrola řádku nákupní žádanky</span><span class="sxs-lookup"><span data-stu-id="75c7e-122">Purchase requisition line review</span></span> | <span data-ttu-id="75c7e-123">Vytvořte kontrolu a workflow schvalování pro řádky nákupního požadavku.</span><span class="sxs-lookup"><span data-stu-id="75c7e-123">Create review and approval workflows for purchase requisition lines.</span></span>       |
| <span data-ttu-id="75c7e-124">Workflow nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="75c7e-124">Purchase order workflow</span></span>          | <span data-ttu-id="75c7e-125">Vytváření workflowů kontroly a schvalování pro nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="75c7e-125">Create review and approval workflows for purchase orders.</span></span>     |
| <span data-ttu-id="75c7e-126">Workflow řádku nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="75c7e-126">Purchase order line workflow</span></span>     | <span data-ttu-id="75c7e-127">Vytváření workflowů kontroly a schvalování pro řádky nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="75c7e-127">Create review and approve workflows for purchase order lines.</span></span> |
| <span data-ttu-id="75c7e-128">Workflow přihlášky přidání dodavatele</span><span class="sxs-lookup"><span data-stu-id="75c7e-128">Vendor add application workflow</span></span>  | <span data-ttu-id="75c7e-129">Vytvořte kontrolu a workflow schvalování pro přidání nových dodavatelů prostřednictvím oslovení dodavatele.</span><span class="sxs-lookup"><span data-stu-id="75c7e-129">Create review and approval workflows for adding new vendors via vendor requests.</span></span> |

## <a name="creating-a-workflow"></a><span data-ttu-id="75c7e-130">Vytvoření workflowu</span><span class="sxs-lookup"><span data-stu-id="75c7e-130">Creating a workflow</span></span>

<span data-ttu-id="75c7e-131">Chcete-li vytvořit workflow, přejděte do nabídky Zásobování a zdroje &gt; Nastavení &gt; Workflowy zásobování a zdrojů a vytvořte nový workflow tak, že vyberete požadovaný typ workflowu k vytvoření.</span><span class="sxs-lookup"><span data-stu-id="75c7e-131">To create a workflow, go to Procurement and sourcing &gt; Setup &gt; Procurement and sourcing workflows and create a new workflow by selecting the type of workflow you want to create.</span></span>  

<span data-ttu-id="75c7e-132">Na plátně workflowu můžete přetahovat prvky workflowu do návrháře a spojovat prvky do toku</span><span class="sxs-lookup"><span data-stu-id="75c7e-132">In the workflow canvas you can drag workflow elements into the designer and link the elements into a flow.</span></span> <span data-ttu-id="75c7e-133">Prvky workflowu je třeba konfigurovat.</span><span class="sxs-lookup"><span data-stu-id="75c7e-133">The workflow elements should be configured.</span></span> <span data-ttu-id="75c7e-134">Co se týká prvků workflowu pro schválení a úlohy, můžete nastavit, který účastník má provést akci.</span><span class="sxs-lookup"><span data-stu-id="75c7e-134">For approval and task workflow elements you can configure which participant should take action.</span></span>

## <a name="types-of-participants"></a><span data-ttu-id="75c7e-135">Typy účastníků</span><span class="sxs-lookup"><span data-stu-id="75c7e-135">Types of participants</span></span>

<span data-ttu-id="75c7e-136">Můžete přiřadit krok schválení k následujícím skupinám účastníků.</span><span class="sxs-lookup"><span data-stu-id="75c7e-136">You can assign an approval step to the following groups of participants.</span></span>

| <span data-ttu-id="75c7e-137">Skupina uživatelů</span><span class="sxs-lookup"><span data-stu-id="75c7e-137">User group</span></span>    | <span data-ttu-id="75c7e-138">Popis</span><span class="sxs-lookup"><span data-stu-id="75c7e-138">Description</span></span>                                                               |
|---------------|---------------------------------------------------------------------------|
| <span data-ttu-id="75c7e-139">Účastník</span><span class="sxs-lookup"><span data-stu-id="75c7e-139">Participant</span></span>   | <span data-ttu-id="75c7e-140">Přiřaďte krok schválení členům skupiny nebo role.</span><span class="sxs-lookup"><span data-stu-id="75c7e-140">Assign the approval step to members of a group or role.</span></span>                   |
| <span data-ttu-id="75c7e-141">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="75c7e-141">Hierarchy</span></span>     | <span data-ttu-id="75c7e-142">Přiřaďte krok schválení k uživatelům v určité organizační hierarchii.</span><span class="sxs-lookup"><span data-stu-id="75c7e-142">Assign the approval step to users in a specific organizational hierarchy.</span></span> |
| <span data-ttu-id="75c7e-143">Uživatel workflowu</span><span class="sxs-lookup"><span data-stu-id="75c7e-143">Workflow user</span></span> | <span data-ttu-id="75c7e-144">Přiřaďte krok schválení uživatelům tohoto pracovního postupu.</span><span class="sxs-lookup"><span data-stu-id="75c7e-144">Assign the approval step to users of this workflow.</span></span>                       |
| <span data-ttu-id="75c7e-145">Fronta</span><span class="sxs-lookup"><span data-stu-id="75c7e-145">Queue</span></span>         | <span data-ttu-id="75c7e-146">Přiřaďte kroku schválení frontě pracovních položek.</span><span class="sxs-lookup"><span data-stu-id="75c7e-146">Assign the approval step to a work item queue.</span></span>                            |
| <span data-ttu-id="75c7e-147">Uživatel</span><span class="sxs-lookup"><span data-stu-id="75c7e-147">User</span></span>          | <span data-ttu-id="75c7e-148">Přiřaďte krok schválení konkrétním uživatelům.</span><span class="sxs-lookup"><span data-stu-id="75c7e-148">Assign the approval step to specific users.</span></span>                               |



## <a name="additional-resources"></a><span data-ttu-id="75c7e-149">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="75c7e-149">Additional resources</span></span>

- [<span data-ttu-id="75c7e-150">Definování workflowů pracovních postupů pro nákupní žádanky</span><span class="sxs-lookup"><span data-stu-id="75c7e-150">Defining business process workflows for purchase requisitions</span></span>](https://mbs.microsoft.com/customersource/Global/AX/learning/documentation/white-papers/Defining_business_process_workflows_for_purchase_requisitions)

- [<span data-ttu-id="75c7e-151">Workflow nákupního požadavku</span><span class="sxs-lookup"><span data-stu-id="75c7e-151">Purchase requisition workflow</span></span>](purchase-requisitions-workflow.md)

- [<span data-ttu-id="75c7e-152">Nabírání dodavatelů</span><span class="sxs-lookup"><span data-stu-id="75c7e-152">Onboarding vendors</span></span>](vendor-onboarding.md)

