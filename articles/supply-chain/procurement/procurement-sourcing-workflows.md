---
title: Workflowy zásobování a zdrojů
description: Některé organizace vyžadují, aby nákupní žádanky a nákupní objednávky byly schváleny uživatelem, který se liší od osoby, která transakci vytvořila. Workflow můžete vytvořit za účelem nastavení schvalovacího procesu.
author: RichardLuan
manager: tfehr
ms.date: 12/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2074
ms.assetid: e54a1d59-b9fb-421b-821d-01f32878aa9b
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e591007a1330fe11b3f586185f9daca845798908
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5218458"
---
# <a name="procurement-and-sourcing-workflows"></a><span data-ttu-id="e81f4-104">Workflowy zásobování a zdrojů</span><span class="sxs-lookup"><span data-stu-id="e81f4-104">Procurement and sourcing workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e81f4-105">Některé organizace vyžadují, aby nákupní žádanky a nákupní objednávky byly schváleny uživatelem, který se liší od osoby, která transakci vytvořila.</span><span class="sxs-lookup"><span data-stu-id="e81f4-105">Some organizations require that purchase requisitions and purchase orders are approved by a user other than the person who entered the transaction.</span></span> <span data-ttu-id="e81f4-106">Workflow můžete vytvořit za účelem nastavení schvalovacího procesu.</span><span class="sxs-lookup"><span data-stu-id="e81f4-106">To set up an approval process, you can create a workflow.</span></span>

<span data-ttu-id="e81f4-107">Workflow představuje obchodní proces.</span><span class="sxs-lookup"><span data-stu-id="e81f4-107">A workflow represents a business process.</span></span> <span data-ttu-id="e81f4-108">Definuje, jakým způsobem dokument prochází systémem a určuje, kdo musí zpracovat úkol nebo schválit dokument.</span><span class="sxs-lookup"><span data-stu-id="e81f4-108">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="e81f4-109">Používání systému workflowu v organizaci má několik výhod:</span><span class="sxs-lookup"><span data-stu-id="e81f4-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="e81f4-110">**Konzistentní procesy:** Můžete definovat schvalovací proces pro specifické dokumenty, například nákupní požadavky a vyúčtování výdajů.</span><span class="sxs-lookup"><span data-stu-id="e81f4-110">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="e81f4-111">Používáním systému workflowu lze zajistit, aby byly dokumenty zpracovávány a schvalovány jednotným a efektivním způsobem.</span><span class="sxs-lookup"><span data-stu-id="e81f4-111">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="e81f4-112">**Viditelnost procesů:** –Můžete sledovat stav, historii a výkonnostní metriku konkrétní instance workflowu.</span><span class="sxs-lookup"><span data-stu-id="e81f4-112">**Process visibility** — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="e81f4-113">To umožňuje určit, zda je potřeba provést změny workflowu ke zvýšení efektivity.</span><span class="sxs-lookup"><span data-stu-id="e81f4-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="e81f4-114">**Centralizovaný seznam pracovních položek**: Uživatelé mohou zobrazit centralizovaný seznam pracovních položek, když chtějí zobrazit úkoly workflowu a schválení, která jsou k nim přiřazená v rámci všech workflowů, kterých se účastní.</span><span class="sxs-lookup"><span data-stu-id="e81f4-114">**Centralized work list** — Users can view a centralized work list to view the workflow tasks and approvals assigned to them across all workflows they participate in.</span></span> <span data-ttu-id="e81f4-115">To je k dispozici na stránce Pracovní položky.</span><span class="sxs-lookup"><span data-stu-id="e81f4-115">This is available in the Work items page.</span></span>

## <a name="the-types-of-workflows-that-you-can-create"></a><span data-ttu-id="e81f4-116"> Typy workflowů, které můžete vytvářet</span><span class="sxs-lookup"><span data-stu-id="e81f4-116">The types of workflows that you can create</span></span>

<span data-ttu-id="e81f4-117">Následující typy workflowu jsou k dispozici pro modul Zásobování a zdroje.</span><span class="sxs-lookup"><span data-stu-id="e81f4-117">The following workflow types are available for Procurement and sourcing.</span></span>

| <span data-ttu-id="e81f4-118">Typ</span><span class="sxs-lookup"><span data-stu-id="e81f4-118">Type</span></span> | <span data-ttu-id="e81f4-119">Tento typ slouží k:</span><span class="sxs-lookup"><span data-stu-id="e81f4-119">Use this type to</span></span> |
|---|---|
| <span data-ttu-id="e81f4-120">Kontrola nákupních žádanek</span><span class="sxs-lookup"><span data-stu-id="e81f4-120">Purchase requisition review</span></span> | <span data-ttu-id="e81f4-121">Vytvořte kontrolu a workflow schvalování pro nákupní požadavky</span><span class="sxs-lookup"><span data-stu-id="e81f4-121">Create review and approval workflows for purchase requisitions.</span></span> |
| <span data-ttu-id="e81f4-122">Kontrola řádku nákupní žádanky</span><span class="sxs-lookup"><span data-stu-id="e81f4-122">Purchase requisition line review</span></span> | <span data-ttu-id="e81f4-123">Vytvořte kontrolu a workflow schvalování pro řádky nákupního požadavku.</span><span class="sxs-lookup"><span data-stu-id="e81f4-123">Create review and approval workflows for purchase requisition lines.</span></span> |
| <span data-ttu-id="e81f4-124">Workflow nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="e81f4-124">Purchase order workflow</span></span> | <span data-ttu-id="e81f4-125">Vytváření workflowů kontroly a schvalování pro nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="e81f4-125">Create review and approval workflows for purchase orders.</span></span> |
| <span data-ttu-id="e81f4-126">Workflow řádku nákupní objednávky</span><span class="sxs-lookup"><span data-stu-id="e81f4-126">Purchase order line workflow</span></span> | <span data-ttu-id="e81f4-127">Vytváření workflowů kontroly a schvalování pro řádky nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="e81f4-127">Create review and approve workflows for purchase order lines.</span></span> |
| <span data-ttu-id="e81f4-128">Workflow přihlášky přidání dodavatele</span><span class="sxs-lookup"><span data-stu-id="e81f4-128">Vendor add application workflow</span></span> | <span data-ttu-id="e81f4-129">Vytvořte kontrolu a workflow schvalování pro přidání nových dodavatelů prostřednictvím oslovení dodavatele.</span><span class="sxs-lookup"><span data-stu-id="e81f4-129">Create review and approval workflows for adding new vendors via vendor requests.</span></span> |

> [!IMPORTANT]
> <span data-ttu-id="e81f4-130">Když přidáváte nový pracovní postup, mohou se vám také zobrazit následující zastaralé pracovní postupy uvedené v dialogovém okně **Vytvořit pracovní postup** .</span><span class="sxs-lookup"><span data-stu-id="e81f4-130">When you are adding a new workflow, you might also see the following obsolete workflows listed in the **Create workflow** dialog box.</span></span> <span data-ttu-id="e81f4-131">Ty se vztahují k funkci *potvrzení o přijetí*, která byla k dispozici v [Dynamics AX 2012](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-procurement-and-sourcing-workflows), ale která je nyní zastaralá.</span><span class="sxs-lookup"><span data-stu-id="e81f4-131">These are related to the *confirmation of receipt* functionality that was available in [Dynamics AX 2012](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-procurement-and-sourcing-workflows), but which has now been deprecated.</span></span> <span data-ttu-id="e81f4-132">Tyto pracovní postupy nejsou aktuálně podporovány.</span><span class="sxs-lookup"><span data-stu-id="e81f4-132">These workflows are currently unsupported.</span></span>
> 
> - <span data-ttu-id="e81f4-133">Workflow oznámení data dodání</span><span class="sxs-lookup"><span data-stu-id="e81f4-133">Delivery due date notification workflow</span></span>
> - <span data-ttu-id="e81f4-134">Workflow oznámení přijaté faktury</span><span class="sxs-lookup"><span data-stu-id="e81f4-134">Invoice received notification workflow</span></span>
> - <span data-ttu-id="e81f4-135">Příjemka produktu v oznámení workflowu selhala.</span><span class="sxs-lookup"><span data-stu-id="e81f4-135">Product receipt failed notification workflow</span></span>
> - <span data-ttu-id="e81f4-136">Workflow oznámení o odmítnutí nepotvrzené příjemky produktu</span><span class="sxs-lookup"><span data-stu-id="e81f4-136">Unconfirmed product receipt rejection notification workflow</span></span>

## <a name="creating-a-workflow"></a><span data-ttu-id="e81f4-137">Vytvoření workflowu</span><span class="sxs-lookup"><span data-stu-id="e81f4-137">Creating a workflow</span></span>

<span data-ttu-id="e81f4-138">Chcete-li vytvořit workflow, přejděte do nabídky Zásobování a zdroje &gt; Nastavení &gt; Workflowy zásobování a zdrojů a vytvořte nový workflow tak, že vyberete požadovaný typ workflowu k vytvoření.</span><span class="sxs-lookup"><span data-stu-id="e81f4-138">To create a workflow, go to Procurement and sourcing &gt; Setup &gt; Procurement and sourcing workflows and create a new workflow by selecting the type of workflow you want to create.</span></span> 

<span data-ttu-id="e81f4-139">Na plátně workflowu můžete přetahovat prvky workflowu do návrháře a spojovat prvky do toku</span><span class="sxs-lookup"><span data-stu-id="e81f4-139">In the workflow canvas you can drag workflow elements into the designer and link the elements into a flow.</span></span> <span data-ttu-id="e81f4-140">Prvky workflowu je třeba konfigurovat.</span><span class="sxs-lookup"><span data-stu-id="e81f4-140">The workflow elements should be configured.</span></span> <span data-ttu-id="e81f4-141">Co se týká prvků workflowu pro schválení a úlohy, můžete nastavit, který účastník má provést akci.</span><span class="sxs-lookup"><span data-stu-id="e81f4-141">For approval and task workflow elements you can configure which participant should take action.</span></span>

## <a name="types-of-participants"></a><span data-ttu-id="e81f4-142">Typy účastníků</span><span class="sxs-lookup"><span data-stu-id="e81f4-142">Types of participants</span></span>

<span data-ttu-id="e81f4-143">Můžete přiřadit krok schválení k následujícím skupinám účastníků.</span><span class="sxs-lookup"><span data-stu-id="e81f4-143">You can assign an approval step to the following groups of participants.</span></span>

| <span data-ttu-id="e81f4-144">Skupina uživatelů</span><span class="sxs-lookup"><span data-stu-id="e81f4-144">User group</span></span> | <span data-ttu-id="e81f4-145">Popis</span><span class="sxs-lookup"><span data-stu-id="e81f4-145">Description</span></span> |
|---|---|
| <span data-ttu-id="e81f4-146">Účastník</span><span class="sxs-lookup"><span data-stu-id="e81f4-146">Participant</span></span> | <span data-ttu-id="e81f4-147">Přiřaďte krok schválení členům skupiny nebo role.</span><span class="sxs-lookup"><span data-stu-id="e81f4-147">Assign the approval step to members of a group or role.</span></span> |
| <span data-ttu-id="e81f4-148">Hierarchie</span><span class="sxs-lookup"><span data-stu-id="e81f4-148">Hierarchy</span></span> | <span data-ttu-id="e81f4-149">Přiřaďte krok schválení k uživatelům v určité organizační hierarchii.</span><span class="sxs-lookup"><span data-stu-id="e81f4-149">Assign the approval step to users in a specific organizational hierarchy.</span></span> |
| <span data-ttu-id="e81f4-150">Uživatel workflowu</span><span class="sxs-lookup"><span data-stu-id="e81f4-150">Workflow user</span></span> | <span data-ttu-id="e81f4-151">Přiřaďte krok schválení uživatelům tohoto pracovního postupu.</span><span class="sxs-lookup"><span data-stu-id="e81f4-151">Assign the approval step to users of this workflow.</span></span> |
| <span data-ttu-id="e81f4-152">Fronta</span><span class="sxs-lookup"><span data-stu-id="e81f4-152">Queue</span></span> | <span data-ttu-id="e81f4-153">Přiřaďte kroku schválení frontě pracovních položek.</span><span class="sxs-lookup"><span data-stu-id="e81f4-153">Assign the approval step to a work item queue.</span></span> |
| <span data-ttu-id="e81f4-154">Uživatel</span><span class="sxs-lookup"><span data-stu-id="e81f4-154">User</span></span> | <span data-ttu-id="e81f4-155">Přiřaďte krok schválení konkrétním uživatelům.</span><span class="sxs-lookup"><span data-stu-id="e81f4-155">Assign the approval step to specific users.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="e81f4-156">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="e81f4-156">Additional resources</span></span>

- [<span data-ttu-id="e81f4-157">Definování workflowů pracovních postupů pro nákupní žádanky</span><span class="sxs-lookup"><span data-stu-id="e81f4-157">Defining business process workflows for purchase requisitions</span></span>](https://www.microsoft.com/download/details.aspx?id=101821)
- [<span data-ttu-id="e81f4-158">Workflow nákupní žádanky</span><span class="sxs-lookup"><span data-stu-id="e81f4-158">Purchase requisition workflow</span></span>](purchase-requisitions-workflow.md)
- [<span data-ttu-id="e81f4-159">Nábor dodavatelů</span><span class="sxs-lookup"><span data-stu-id="e81f4-159">Onboard vendors</span></span>](vendor-onboarding.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]