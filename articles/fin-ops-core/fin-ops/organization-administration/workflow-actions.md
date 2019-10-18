---
title: Akce v procesech schválení workflow
description: V tomto článku jsou vysvětleny akce, které může provést každý účastník v procesu schválení workflowu.
author: sericks007
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56411
ms.assetid: 65fb711c-6474-42d1-81ed-ca657c29bf1f
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6516e8b1e4be83f3450f03c769bca6d158ffb79b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176869"
---
# <a name="actions-in-workflow-approval-processes"></a><span data-ttu-id="5c213-103">Akce v procesech schválení workflow</span><span class="sxs-lookup"><span data-stu-id="5c213-103">Actions in workflow approval processes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5c213-104">V tomto článku jsou vysvětleny akce, které může provést každý účastník v procesu schválení workflowu.</span><span class="sxs-lookup"><span data-stu-id="5c213-104">This article explains the actions that each participant in a workflow approval process can take.</span></span>

<span data-ttu-id="5c213-105">Workflow může zahrnovat několik skupin osob: původce, zmocněnci pro úkol, pracovníci s rozhodovací pravomocí a schvalovatelé.</span><span class="sxs-lookup"><span data-stu-id="5c213-105">A workflow can involve several groups of people: the originator, task assignees, decision makers, and approvers.</span></span> <span data-ttu-id="5c213-106">Například v následujícím workflowu k vyúčtování výdajů je Stanislav původcem, členové fronty jsou zmocněnci pro úkol, Jan je pracovníkem s rozhodovací pravomocí a František, Šárka a Anna jsou schvalovateli.</span><span class="sxs-lookup"><span data-stu-id="5c213-106">For example, in the following expense report workflow, Sam is the originator, the members of the queue are task assignees, John is a decision maker, and Frank, Sue, and Ann are approvers.</span></span>

<span data-ttu-id="5c213-107">[![Workflow\_WithManualDecision](./media/workflow_withmanualdecision.gif)](./media/workflow_withmanualdecision.gif)</span><span class="sxs-lookup"><span data-stu-id="5c213-107">[![Workflow\_WithManualDecision](./media/workflow_withmanualdecision.gif)](./media/workflow_withmanualdecision.gif)</span></span>

<span data-ttu-id="5c213-108">Následující části vysvětlují akce workflowu, které může provést každá skupina.</span><span class="sxs-lookup"><span data-stu-id="5c213-108">The following sections explain the workflow actions that each group can perform.</span></span>

## <a name="actions-that-an-originator-can-perform"></a><span data-ttu-id="5c213-109">Akce, které může provádět původce</span><span class="sxs-lookup"><span data-stu-id="5c213-109">Actions that an originator can perform</span></span>

<span data-ttu-id="5c213-110">Původce zahájí instanci workflowu odesláním dokumentu ke zpracování.</span><span class="sxs-lookup"><span data-stu-id="5c213-110">The originator starts a workflow instance by submitting a document for processing.</span></span> <span data-ttu-id="5c213-111">Stanislav musí například odeslat vyúčtování výdajů kliknutím na tlačítko **Odeslat** na stránce **Vyúčtování výdajů**.</span><span class="sxs-lookup"><span data-stu-id="5c213-111">For example, Sam must click the **Submit** button on the **Expense report** page to submit his expense report.</span></span>

## <a name="actions-that-a-task-assignee-can-perform"></a><span data-ttu-id="5c213-112">Akce, které může provádět zmocněnec</span><span class="sxs-lookup"><span data-stu-id="5c213-112">Actions that a task assignee can perform</span></span>

<span data-ttu-id="5c213-113">Úkol lze přiřadit více osobám nebo frontě pracovních položek, které jsou sledovány více osobami.</span><span class="sxs-lookup"><span data-stu-id="5c213-113">A task can be assigned to multiple people or to a work item queue that is monitored by several people.</span></span> <span data-ttu-id="5c213-114">Dokončit ji však může pouze jediná osoba.</span><span class="sxs-lookup"><span data-stu-id="5c213-114">However, only one person can complete a task.</span></span> <span data-ttu-id="5c213-115">Stanislav například odeslal vyúčtování výdajů a nasměroval své příjemky do oddělení vyúčtování výdajů, aby je jeho pracovníci zkontrolovali.</span><span class="sxs-lookup"><span data-stu-id="5c213-115">For example, Sam has submitted an expense report and has routed his receipts to his organization's Expense Reports department for review.</span></span>

<span data-ttu-id="5c213-116">Členové oddělení vyúčtování výdajů společnosti Adventure Works sledují frontu.</span><span class="sxs-lookup"><span data-stu-id="5c213-116">The members of the Adventure Works Expense Reports department monitor the queue.</span></span> <span data-ttu-id="5c213-117">Júlie, která je členkou tohoto oddělení, přijala úkol kontroly Stanislavova vyúčtování výdajů a příjemek.</span><span class="sxs-lookup"><span data-stu-id="5c213-117">Julie, a member of that department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="5c213-118">Může nyní provést jednu z těchto akcí: dokončení, zamítnutí, delegování, žádost o změnu, změna přiřazení nebo uvolnění.</span><span class="sxs-lookup"><span data-stu-id="5c213-118">She can now perform one of the following actions: complete, reject, delegate, request change, reassign, or release.</span></span>

> [!NOTE]
> <span data-ttu-id="5c213-119">Dostupné akce se budou lišit v závislosti na tom, jak vývojář softwaru úkol navrhnul.</span><span class="sxs-lookup"><span data-stu-id="5c213-119">The actions that are available vary, depending on how the software developer designed the task.</span></span>

### <a name="complete"></a><span data-ttu-id="5c213-120">Dokončení</span><span class="sxs-lookup"><span data-stu-id="5c213-120">Complete</span></span>

<span data-ttu-id="5c213-121">Když uživatel úkol dokončí, je dokument, který byl odeslán ke zpracování, přiřazen dalšímu uživateli ve workflowu (existuje-li takový uživatel).</span><span class="sxs-lookup"><span data-stu-id="5c213-121">When a user completes a task, the document that was submitted for processing is assigned to the next user in the workflow, if there is a next user.</span></span> <span data-ttu-id="5c213-122">Není-li vyžadováno další zpracování, proces workflowu bude ukončen.</span><span class="sxs-lookup"><span data-stu-id="5c213-122">If no additional processing is required, the workflow process ends.</span></span>

<span data-ttu-id="5c213-123">V tomto příkladu Júlie, která je členkou tohoto oddělení, přijala úkol kontroly Stanislavova vyúčtování výdajů a příjemek.</span><span class="sxs-lookup"><span data-stu-id="5c213-123">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="5c213-124">Jakmile Júlie dokončí kontrolu, je dokument přiřazen Janovi.</span><span class="sxs-lookup"><span data-stu-id="5c213-124">After Julie completes her review, the document is assigned to John.</span></span>

### <a name="reject"></a><span data-ttu-id="5c213-125">Zamítnout</span><span class="sxs-lookup"><span data-stu-id="5c213-125">Reject</span></span>

<span data-ttu-id="5c213-126">Když uživatel dokument zamítne, proces workflowu skončí.</span><span class="sxs-lookup"><span data-stu-id="5c213-126">When a user rejects a document, the workflow process ends.</span></span>

<span data-ttu-id="5c213-127">V tomto příkladu Júlie, která je členkou tohoto oddělení, přijala úkol kontroly Stanislavova vyúčtování výdajů a příjemek.</span><span class="sxs-lookup"><span data-stu-id="5c213-127">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="5c213-128">Když Júlie vyúčtování výdajů odmítne, proces workflowu skončí.</span><span class="sxs-lookup"><span data-stu-id="5c213-128">If Julie rejects the expense report, the workflow process ends.</span></span>

<span data-ttu-id="5c213-129">Stanislav může poté vyúčtování výdajů znovu odeslat.</span><span class="sxs-lookup"><span data-stu-id="5c213-129">Sam can then resubmit the expense report.</span></span> <span data-ttu-id="5c213-130">Nejprve může provést změny, anebo může znovu odeslat původní verzi.</span><span class="sxs-lookup"><span data-stu-id="5c213-130">He can make changes first, or he can resubmit the original version.</span></span> <span data-ttu-id="5c213-131">Jestliže Stanislav vyúčtování výdajů znovu odešle, začíná proces workflowu u úlohy ruční kontroly.</span><span class="sxs-lookup"><span data-stu-id="5c213-131">If Sam resubmits the expense report, the workflow process starts at the manual review task.</span></span>

### <a name="delegate"></a><span data-ttu-id="5c213-132">Delegovat</span><span class="sxs-lookup"><span data-stu-id="5c213-132">Delegate</span></span>

<span data-ttu-id="5c213-133">Když uživatel úkol deleguje, je úkole přiřazen jinému uživateli.</span><span class="sxs-lookup"><span data-stu-id="5c213-133">When a user delegates a task, the task is assigned to another user.</span></span>

<span data-ttu-id="5c213-134">V tomto příkladu Júlie, která je členkou tohoto oddělení, přijala úkol kontroly Stanislavova vyúčtování výdajů a příjemek.</span><span class="sxs-lookup"><span data-stu-id="5c213-134">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="5c213-135">Júlie tento úkol deleguje na Teodora, který je jejím asistentem.</span><span class="sxs-lookup"><span data-stu-id="5c213-135">Julie delegates this task to Tim, who is her assistant.</span></span>

<span data-ttu-id="5c213-136">Teodor poté jedná jménem Júlie.</span><span class="sxs-lookup"><span data-stu-id="5c213-136">Tim then acts on behalf of Julie.</span></span> <span data-ttu-id="5c213-137">Jakmile tedy Teodor kontrolu dokončí, bude vyúčtování výdajů přiřazeno Janovi, jako kdyby úkol dokončila Júlie.</span><span class="sxs-lookup"><span data-stu-id="5c213-137">Therefore, when Tim completes his review, the expense report is assigned to John, just as if Julie had completed the task.</span></span>

### <a name="request-change"></a><span data-ttu-id="5c213-138">Požadavek na změnu</span><span class="sxs-lookup"><span data-stu-id="5c213-138">Request change</span></span>

<span data-ttu-id="5c213-139">Když uživatel požaduje provedení změny v dokumentu, který byl odeslán, je dokument vrácen zpět původci.</span><span class="sxs-lookup"><span data-stu-id="5c213-139">When a user requests a change to a document that was submitted, the document is sent back to the originator.</span></span>

<span data-ttu-id="5c213-140">V tomto příkladu Júlie, která je členkou tohoto oddělení, přijala úkol kontroly Stanislavova vyúčtování výdajů a příjemek.</span><span class="sxs-lookup"><span data-stu-id="5c213-140">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="5c213-141">Júlie si ve vyúčtování výdajů všimne několika chyb a požádá o změny.</span><span class="sxs-lookup"><span data-stu-id="5c213-141">Julie notices some errors on the expense report and requests changes.</span></span> <span data-ttu-id="5c213-142">Vyúčtování výdajů se odešle zpět Stanislavovi.</span><span class="sxs-lookup"><span data-stu-id="5c213-142">The expense report is sent back to Sam.</span></span>

<span data-ttu-id="5c213-143">Stanislav může vyúčtování výdajů znovu odeslat.</span><span class="sxs-lookup"><span data-stu-id="5c213-143">Sam can resubmit the expense report.</span></span> <span data-ttu-id="5c213-144">Nejprve může provést požadované změny, anebo může znovu odeslat původní verzi.</span><span class="sxs-lookup"><span data-stu-id="5c213-144">He can make the requested changes first, or he can resubmit the original version.</span></span> <span data-ttu-id="5c213-145">Pokud Stanislav vyúčtování výdajů odešle znovu, je nutné, aby člen fronty pracovních položek znovu zkontroloval vyúčtování výdajů a příjemky.</span><span class="sxs-lookup"><span data-stu-id="5c213-145">If Sam resubmits the expense report, a member of the work item queue must review the expense report and the receipts again.</span></span>

### <a name="reassign"></a><span data-ttu-id="5c213-146">Opětovné přiřazení</span><span class="sxs-lookup"><span data-stu-id="5c213-146">Reassign</span></span>

<span data-ttu-id="5c213-147">Členové fronty pracovních položek mohou dokumenty ve frontě přeřadit do jiné fronty.</span><span class="sxs-lookup"><span data-stu-id="5c213-147">The members of a work item queue can reassign documents that are in that queue to another queue.</span></span>

<span data-ttu-id="5c213-148">V tomto příkladu Júlie, která je členkou oddělení vyúčtování výdajů společnosti Adventure Works, sleduje frontu.</span><span class="sxs-lookup"><span data-stu-id="5c213-148">For example, Julie, a member of the Adventure Works Expense Reports department, is monitoring the queue.</span></span> <span data-ttu-id="5c213-149">Z důvodu vyrovnání pracovního vytížení může vyúčtování výdajů a příjemky, které jsou jeho součástí, přeřadit pro jiné fronty.</span><span class="sxs-lookup"><span data-stu-id="5c213-149">To help balance the workload, she can reassign the expense report, and the receipts that are included with it, to another queue.</span></span>

### <a name="release"></a><span data-ttu-id="5c213-150">Uvolnit</span><span class="sxs-lookup"><span data-stu-id="5c213-150">Release</span></span>

<span data-ttu-id="5c213-151">V některých případech může člen fronty pracovních položek úkol přijmout, ale poté zjistit, že jej nemůže provést.</span><span class="sxs-lookup"><span data-stu-id="5c213-151">Occasionally, a member of a work item queue might accept a task, but then decide that he or she can't complete the task.</span></span> <span data-ttu-id="5c213-152">V takovém případě může osoba, která úkol přijala, uvolnit dokument zpět do fronty pracovních položek.</span><span class="sxs-lookup"><span data-stu-id="5c213-152">In this case, the person who accepted the task can release the document back to the work item queue.</span></span>

<span data-ttu-id="5c213-153">V tomto příkladu Júlie, která je členkou tohoto oddělení, přijala úkol kontroly Stanislavova vyúčtování výdajů a příjemek.</span><span class="sxs-lookup"><span data-stu-id="5c213-153">For example, Julie, a member of the Adventure Works Expense Reports department, has accepted the task of reviewing Sam's expense report and receipts.</span></span> <span data-ttu-id="5c213-154">Júlie se rozhodne, že nemůže úkol dokončit, a tak dokument uvolní.</span><span class="sxs-lookup"><span data-stu-id="5c213-154">If Julie decides that she can't complete the task, she can release the document.</span></span> <span data-ttu-id="5c213-155">Vyúčtování výdajů je vráceno do fronty, takže ostatní členové oddělení vyúčtování nákladů společnosti Adventure Works mohou úkol provést.</span><span class="sxs-lookup"><span data-stu-id="5c213-155">The expense report is returned to the queue, so that other members of the Adventure Works Expense Reports department can complete the task.</span></span>

## <a name="actions-that-a-decision-maker-can-perform"></a><span data-ttu-id="5c213-156">Akce, které může provádět pracovník s rozhodovací pravomocí</span><span class="sxs-lookup"><span data-stu-id="5c213-156">Actions that a decision maker can perform</span></span>

<span data-ttu-id="5c213-157">Dokument bývá obvykle přiřazen pracovníkovi s rozhodovací pravomocí, protože vyvstala otázka, kterou musí rozhodnout pracovník s rozhodovací pravomocí.</span><span class="sxs-lookup"><span data-stu-id="5c213-157">Typically, a document is assigned to a decision maker, because there is a question that the decision maker must answer.</span></span> <span data-ttu-id="5c213-158">Na otázku se obvykle odpovídá možnostmi **Ano** nebo **Ne**, nebo **Pravda** nebo **Nepravda**.</span><span class="sxs-lookup"><span data-stu-id="5c213-158">The answer to the question is typically **Yes** or **No**, or **True** or **False**.</span></span> <span data-ttu-id="5c213-159">Pokud pracovník s rozhodovací pravomocí nevybere některou z těchto možností, může rozhodnutí delegovat.</span><span class="sxs-lookup"><span data-stu-id="5c213-159">If the decision maker doesn't select one of those choices, he or she can delegate the decision.</span></span>

### <a name="choice-1-or-choice-2"></a><span data-ttu-id="5c213-160">\[Volba 1\] nebo \[Volba 2\]</span><span class="sxs-lookup"><span data-stu-id="5c213-160">\[Choice 1\] or \[Choice 2\]</span></span>

<span data-ttu-id="5c213-161">Pracovník s rozhodovací pravomocí musí odpovědět na otázku, která se vztahuje k dokumentu.</span><span class="sxs-lookup"><span data-stu-id="5c213-161">A decision maker must answer a question that is related to the document.</span></span> <span data-ttu-id="5c213-162">Na otázku se obvykle odpovídá možnostmi **Ano** nebo **Ne**, nebo **Pravda** nebo **Nepravda**.</span><span class="sxs-lookup"><span data-stu-id="5c213-162">The answer to the question is typically **Yes** or **No**, or **True** or **False**.</span></span> <span data-ttu-id="5c213-163">Odpověď, kterou pracovník s rozhodovací pravomocí vybere, určuje větev workflowu, která bude použita ke zpracování dokumentu.</span><span class="sxs-lookup"><span data-stu-id="5c213-163">The answer that the decision maker selects determines the workflow branch that is used to process the document.</span></span>

<span data-ttu-id="5c213-164">Stanislavovo vyúčtování výdajů je například přiřazeno Janovi.</span><span class="sxs-lookup"><span data-stu-id="5c213-164">For example, Sam's expense report is assigned to John.</span></span> <span data-ttu-id="5c213-165">Jan musí rozhodnout, zda informace v dokumentu vyžadují hovor se Stanislavovým nadřízeným.</span><span class="sxs-lookup"><span data-stu-id="5c213-165">John must decide whether the information in the document requires a call to Sam's manager.</span></span> <span data-ttu-id="5c213-166">Když Jan rozhodne, že je hovor nutný, je vyúčtování výdajů přiřazeno Adéle, která pak musí zavolat nadřízenému Stanislava.</span><span class="sxs-lookup"><span data-stu-id="5c213-166">If John decides that a call is required, the expense report is assigned to Aretha, who must then call Sam's manager.</span></span> <span data-ttu-id="5c213-167">Pokud Jan rozhodne, že hovor není třeba, vyúčtování výdajů je přiřazeno Františkovi ke schválení.</span><span class="sxs-lookup"><span data-stu-id="5c213-167">If John decides that a call isn't required, the expense report is assigned to Frank for approval.</span></span>

### <a name="delegate"></a><span data-ttu-id="5c213-168">Delegovat</span><span class="sxs-lookup"><span data-stu-id="5c213-168">Delegate</span></span>

<span data-ttu-id="5c213-169">Když pracovník s rozhodovací pravomocí deleguje rozhodnutí, je dokument přiřazen jinému uživateli, který musí rozhodnutí učinit.</span><span class="sxs-lookup"><span data-stu-id="5c213-169">When a decision maker delegates a decision, the document is assigned to another user who must make the decision.</span></span>

<span data-ttu-id="5c213-170">Stanislavovo vyúčtování výdajů je například přiřazeno Janovi.</span><span class="sxs-lookup"><span data-stu-id="5c213-170">For example, Sam's expense report is assigned to John.</span></span> <span data-ttu-id="5c213-171">Jan deleguje rozhodnutí Marii, která je jeho asistentkou.</span><span class="sxs-lookup"><span data-stu-id="5c213-171">John delegates the decision to Maria, who is his assistant.</span></span>

<span data-ttu-id="5c213-172">Marie poté jedná jménem Jana.</span><span class="sxs-lookup"><span data-stu-id="5c213-172">Maria then acts on behalf of John.</span></span> <span data-ttu-id="5c213-173">Když Marie rozhodne, že je hovor se Stanislavovým nadřízeným nutný, je vyúčtování výdajů přiřazeno Adéle, která pak musí zavolat nadřízenému Stanislava.</span><span class="sxs-lookup"><span data-stu-id="5c213-173">If Maria decides that a call to Sam's manager is required, the expense report is assigned to Aretha, who must then call Sam's manager.</span></span> <span data-ttu-id="5c213-174">Pokud Marie rozhodne, že hovor není třeba, vyúčtování výdajů je přiřazeno Františkovi ke schválení.</span><span class="sxs-lookup"><span data-stu-id="5c213-174">If Maria decides that a call isn't required, the expense report is assigned to Frank for approval.</span></span>

## <a name="actions-that-an-approver-can-perform"></a><span data-ttu-id="5c213-175">Akce, které může provádět schvalovatel</span><span class="sxs-lookup"><span data-stu-id="5c213-175">Actions that an approver can perform</span></span>

<span data-ttu-id="5c213-176">Jakmile je dokument přiřazen schvalovateli, může tento schvalovatel provést jednu z následujících akcí: schválení, zamítnutí, delegování nebo žádost o změnu.</span><span class="sxs-lookup"><span data-stu-id="5c213-176">When a document is assigned to an approver, the approver can perform one of the following actions: approve, reject, delegate, or request change.</span></span>

### <a name="approve"></a><span data-ttu-id="5c213-177">Schválení</span><span class="sxs-lookup"><span data-stu-id="5c213-177">Approve</span></span>

<span data-ttu-id="5c213-178">Když schvalovatel dokument schválí, je dokument přiřazen dalšímu uživateli ve workflowu (existuje-li takový uživatel).</span><span class="sxs-lookup"><span data-stu-id="5c213-178">When an approver approves a document, the document is assigned to the next user in the workflow, if there is a next user.</span></span> <span data-ttu-id="5c213-179">Není-li vyžadováno další zpracování, proces workflowu bude ukončen.</span><span class="sxs-lookup"><span data-stu-id="5c213-179">If no additional processing is required, the workflow process ends.</span></span>

<span data-ttu-id="5c213-180">Stanislav například odeslal vyúčtování výdajů na 6 000 USD a tento dokument je přiřazen Františkovi.</span><span class="sxs-lookup"><span data-stu-id="5c213-180">For example, Sam has submitted an expense report for USD 6,000, and this document is assigned to Frank.</span></span> <span data-ttu-id="5c213-181">Když František dokument schválí, je přiřazen Šárce ke schválení.</span><span class="sxs-lookup"><span data-stu-id="5c213-181">When Frank approves the document, it's assigned to Sue for approval.</span></span> <span data-ttu-id="5c213-182">Když Šárka vyúčtování výdajů schválí, proces workflowu skončí.</span><span class="sxs-lookup"><span data-stu-id="5c213-182">When Sue approves the expense report, the workflow process ends.</span></span>

### <a name="reject"></a><span data-ttu-id="5c213-183">Zamítnout</span><span class="sxs-lookup"><span data-stu-id="5c213-183">Reject</span></span>

<span data-ttu-id="5c213-184">Když schvalující dokument zamítne, proces workflowu končí.</span><span class="sxs-lookup"><span data-stu-id="5c213-184">When an approver rejects a document, the workflow process ends.</span></span>

<span data-ttu-id="5c213-185">Stanislav například odeslal vyúčtování výdajů na 12 000 USD a tento dokument je přiřazen Šárce.</span><span class="sxs-lookup"><span data-stu-id="5c213-185">For example, Sam has submitted an expense report for USD 12,000, and this document is assigned to Sue.</span></span> <span data-ttu-id="5c213-186">Když Šárka vyúčtování výdajů zamítne, proces workflowu skončí.</span><span class="sxs-lookup"><span data-stu-id="5c213-186">If Sue rejects the expense report, the workflow process ends.</span></span>

<span data-ttu-id="5c213-187">Stanislav může vyúčtování výdajů znovu odeslat.</span><span class="sxs-lookup"><span data-stu-id="5c213-187">Sam can resubmit the expense report.</span></span> <span data-ttu-id="5c213-188">Nejprve může provést změny, anebo může znovu odeslat původní verzi vyúčtování výdajů.</span><span class="sxs-lookup"><span data-stu-id="5c213-188">He can make changes first, or he can resubmit the original version of the expense report.</span></span> <span data-ttu-id="5c213-189">Pokud Stanislav vyúčtování výdajů znovu odešle, začíná proces workflowu od schvalovacího procesu.</span><span class="sxs-lookup"><span data-stu-id="5c213-189">If Sam resubmits the expense report, the workflow process starts at the approval process.</span></span>

### <a name="delegate"></a><span data-ttu-id="5c213-190">Delegovat</span><span class="sxs-lookup"><span data-stu-id="5c213-190">Delegate</span></span>

<span data-ttu-id="5c213-191">Když schvalující dokument deleguje, je dokument postoupen ke schválení jinému uživateli.</span><span class="sxs-lookup"><span data-stu-id="5c213-191">When an approver delegates a document, the document is assigned to another user for approval.</span></span>

<span data-ttu-id="5c213-192">Stanislav například odeslal vyúčtování výdajů na 12 000 USD a tento dokument je přiřazen Františkovi.</span><span class="sxs-lookup"><span data-stu-id="5c213-192">For example, Sam has submitted an expense report for USD 12,000, and this document is assigned to Frank.</span></span> <span data-ttu-id="5c213-193">František deleguje vyúčtování výdajů na Annu.</span><span class="sxs-lookup"><span data-stu-id="5c213-193">Frank delegates the expense report to Ann.</span></span>

<span data-ttu-id="5c213-194">Anna bude potom jednat jménem Františka.</span><span class="sxs-lookup"><span data-stu-id="5c213-194">Ann then acts on behalf of Frank.</span></span> <span data-ttu-id="5c213-195">To znamená, že když Anna dokument schválí, je dokument přiřazen Šárce ke schválení, jako kdyby ho schválil František.</span><span class="sxs-lookup"><span data-stu-id="5c213-195">Therefore, when Ann approves the document, it's assigned to Sue for approval, just as if Frank had approved it.</span></span> <span data-ttu-id="5c213-196">Jakmile Šárka dokument schválí, je odeslán Anně ke schválení.</span><span class="sxs-lookup"><span data-stu-id="5c213-196">After Sue approves the document, it's sent to Ann for approval.</span></span>

### <a name="request-change"></a><span data-ttu-id="5c213-197">Požadavek na změnu</span><span class="sxs-lookup"><span data-stu-id="5c213-197">Request change</span></span>

<span data-ttu-id="5c213-198">Když schvalující požaduje provedení změny v dokumentu, je dokument odeslán zpět původci.</span><span class="sxs-lookup"><span data-stu-id="5c213-198">When an approver requests a change to a document, the document is sent back to the originator.</span></span>

<span data-ttu-id="5c213-199">Stanislav například odeslal vyúčtování výdajů na 12 000 USD a tento dokument je přiřazen Šárce.</span><span class="sxs-lookup"><span data-stu-id="5c213-199">For example, Sam has submitted an expense report for USD 12,000, and this document is assigned to Sue.</span></span> <span data-ttu-id="5c213-200">Pokud bude Šárka požadovat změnu, bude vyúčtování výdajů odesláno zpět Stanislavovi.</span><span class="sxs-lookup"><span data-stu-id="5c213-200">If Sue requests a change, the expense report is sent back to Sam.</span></span>

<span data-ttu-id="5c213-201">Stanislav může vyúčtování výdajů znovu odeslat.</span><span class="sxs-lookup"><span data-stu-id="5c213-201">Sam can resubmit the expense report.</span></span> <span data-ttu-id="5c213-202">Nejprve může provést požadované změny, anebo může znovu odeslat původní verzi vyúčtování výdajů.</span><span class="sxs-lookup"><span data-stu-id="5c213-202">He can make the requested changes first, or he can resubmit the original version of the expense report.</span></span> <span data-ttu-id="5c213-203">Jestliže Stanislav vyúčtování výdajů znovu odešle, je odesláno Františkovi ke schválení, protože František je prvním schvalovatelem v procesu schvalování.</span><span class="sxs-lookup"><span data-stu-id="5c213-203">If Sam resubmits the expense report, it's sent to Frank for approval, because Frank is the first approver in the approval process.</span></span>
