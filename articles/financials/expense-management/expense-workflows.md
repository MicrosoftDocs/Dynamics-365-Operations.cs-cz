---
title: "Nastavení workflow pro výdaje"
description: "Můžete nastavit proces workflowu, který se používá ke kontrole a schválení dokumentů cestovného a výdajů."
author: saraschi2
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: ef60fbab0f75ff70206d954e3d098a3866c467b6
ms.contentlocale: cs-cz
ms.lasthandoff: 01/17/2018

---

# <a name="set-up-workflows-for-expense"></a><span data-ttu-id="e2bd0-103">Nastavení workflow pro výdaje</span><span class="sxs-lookup"><span data-stu-id="e2bd0-103">Set up workflows for expense</span></span>

[!include[banner](../includes/banner.md)]<span data-ttu-id="e2bd0-104"> Můžete nastavit proces workflowu, který se používá ke kontrole a schválení dokumentů cestovného a výdajů.</span><span class="sxs-lookup"><span data-stu-id="e2bd0-104"> You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="e2bd0-105">Dokumenty, pro která lze workflow definovat, zahrnují vyúčtování výdajů, cestovní žádanky a požadavky na hotovostní zálohu.</span><span class="sxs-lookup"><span data-stu-id="e2bd0-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="e2bd0-106">Workflow představuje obchodní proces.</span><span class="sxs-lookup"><span data-stu-id="e2bd0-106">A workflow represents a business process.</span></span> <span data-ttu-id="e2bd0-107">Definuje, jakým způsobem dokument prochází systémem a určuje, kdo musí zpracovat úkol nebo schválit dokument.</span><span class="sxs-lookup"><span data-stu-id="e2bd0-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="e2bd0-108">Používání systému workflowu v organizaci má několik výhod:</span><span class="sxs-lookup"><span data-stu-id="e2bd0-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="e2bd0-109">**Konzistentní procesy:** Můžete definovat schvalovací proces pro specifické dokumenty, například nákupní požadavky a vyúčtování výdajů.</span><span class="sxs-lookup"><span data-stu-id="e2bd0-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="e2bd0-110">Používáním systému workflowu lze zajistit, aby byly dokumenty zpracovávány a schvalovány jednotným a efektivním způsobem.</span><span class="sxs-lookup"><span data-stu-id="e2bd0-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="e2bd0-111">Viditelnost procesů: –Můžete sledovat stav, historii a výkonnostní metriku konkrétní instance workflowu.</span><span class="sxs-lookup"><span data-stu-id="e2bd0-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="e2bd0-112">To umožňuje určit, zda je potřeba provést změny workflowu ke zvýšení efektivity.</span><span class="sxs-lookup"><span data-stu-id="e2bd0-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="e2bd0-113">Centralizovaný seznam pracovních položek: Uživatelé mohou zobrazit centralizovaný seznam pracovních položek k zobrazení úkolů workflowu a schválení, která mají přiřazena.</span><span class="sxs-lookup"><span data-stu-id="e2bd0-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="e2bd0-114">**Můžete vytvářet tyto typy pracovního procesu:**</span><span class="sxs-lookup"><span data-stu-id="e2bd0-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="e2bd0-115">V následující tabulce jsou uvedeny typy pracovních procesů, které můžete vytvořit v části **Výdaje**.</span><span class="sxs-lookup"><span data-stu-id="e2bd0-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>

| <span data-ttu-id="e2bd0-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="e2bd0-116">**Type**</span></span>                           | <span data-ttu-id="e2bd0-117">**Tento typ slouží k:**</span><span class="sxs-lookup"><span data-stu-id="e2bd0-117">**Use this type to**</span></span>                                                 |     
|------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="e2bd0-118">**Vyúčtování výdajů**</span><span class="sxs-lookup"><span data-stu-id="e2bd0-118">**Expense report**</span></span>                 | <span data-ttu-id="e2bd0-119">Vytváření workflowů schválení pro sestavy výdajů.</span><span class="sxs-lookup"><span data-stu-id="e2bd0-119">Create approval workflows for expense reports.</span></span>                       |      
| <span data-ttu-id="e2bd0-120">**Automatické zaúčtování sestavy výdajů**</span><span class="sxs-lookup"><span data-stu-id="e2bd0-120">**Expense report auto posting**</span></span>    | <span data-ttu-id="e2bd0-121">Vytváření workflowů automatického zaúčtování pro sestavy výdajů.</span><span class="sxs-lookup"><span data-stu-id="e2bd0-121">Create automatic posting workflows for expense reports.</span></span>              |     
| <span data-ttu-id="e2bd0-122">**Položka řádku výdajů**</span><span class="sxs-lookup"><span data-stu-id="e2bd0-122">**Expense line item**</span></span>              | <span data-ttu-id="e2bd0-123">Vytváření workflowů schválení pro položky řádků na sestavě výdajů.</span><span class="sxs-lookup"><span data-stu-id="e2bd0-123">Create approval workflows for line items on expense reports.</span></span>         |     
| <span data-ttu-id="e2bd0-124">**Automatické zaúčtování položek řádku výdajů**</span><span class="sxs-lookup"><span data-stu-id="e2bd0-124">**Expense line item auto posting**</span></span> | <span data-ttu-id="e2bd0-125">Vytváření workflowů automatického zaúčtování pro položky řádků na sestavě výdajů.</span><span class="sxs-lookup"><span data-stu-id="e2bd0-125">Create automatic posting workflows for line items on expense reports.</span></span>|
| <span data-ttu-id="e2bd0-126">**Cestovní žádanka**</span><span class="sxs-lookup"><span data-stu-id="e2bd0-126">**Travel requisition**</span></span>             | <span data-ttu-id="e2bd0-127">Vytváření workflowů pro cestovní žádanky.</span><span class="sxs-lookup"><span data-stu-id="e2bd0-127">Create approval workflows for travel requisitions.</span></span>                   |    
| <span data-ttu-id="e2bd0-128">**Požadavek na hotovostní zálohu**</span><span class="sxs-lookup"><span data-stu-id="e2bd0-128">**Cash advance request**</span></span>           | <span data-ttu-id="e2bd0-129">Vytvoření workflowů schválení pro požadavky na hotovostní zálohu.</span><span class="sxs-lookup"><span data-stu-id="e2bd0-129">Create approval workflows for cash advance requests.</span></span>                 |     
| <span data-ttu-id="e2bd0-130">**Vratka daně DPH**</span><span class="sxs-lookup"><span data-stu-id="e2bd0-130">**VAT tax recovery**</span></span>               | <span data-ttu-id="e2bd0-131">Vytvoření workflowů schválení pro vratky daně DPH.</span><span class="sxs-lookup"><span data-stu-id="e2bd0-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span> |       

