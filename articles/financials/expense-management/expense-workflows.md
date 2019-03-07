---
title: Nastavení workflow pro výdaje
description: Můžete nastavit proces workflowu, který se používá ke kontrole a schválení dokumentů cestovného a výdajů.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8294aaa344e3cb6b79fa4f33f368258ca19c8205
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "355718"
---
# <a name="set-up-workflows-for-expense"></a><span data-ttu-id="b83cd-103">Nastavení workflow pro výdaje</span><span class="sxs-lookup"><span data-stu-id="b83cd-103">Set up workflows for expense</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b83cd-104"> Můžete nastavit proces workflowu, který se používá ke kontrole a schválení dokumentů cestovného a výdajů.</span><span class="sxs-lookup"><span data-stu-id="b83cd-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="b83cd-105">Dokumenty, pro která lze workflow definovat, zahrnují vyúčtování výdajů, cestovní žádanky a požadavky na hotovostní zálohu.</span><span class="sxs-lookup"><span data-stu-id="b83cd-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="b83cd-106">Workflow představuje obchodní proces.</span><span class="sxs-lookup"><span data-stu-id="b83cd-106">A workflow represents a business process.</span></span> <span data-ttu-id="b83cd-107">Definuje, jakým způsobem dokument prochází systémem a určuje, kdo musí zpracovat úkol nebo schválit dokument.</span><span class="sxs-lookup"><span data-stu-id="b83cd-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="b83cd-108">Používání systému workflowu v organizaci má několik výhod:</span><span class="sxs-lookup"><span data-stu-id="b83cd-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="b83cd-109">**Konzistentní procesy:** Můžete definovat schvalovací proces pro specifické dokumenty, například nákupní požadavky a vyúčtování výdajů.</span><span class="sxs-lookup"><span data-stu-id="b83cd-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="b83cd-110">Používáním systému workflowu lze zajistit, aby byly dokumenty zpracovávány a schvalovány jednotným a efektivním způsobem.</span><span class="sxs-lookup"><span data-stu-id="b83cd-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="b83cd-111">Viditelnost procesů: –Můžete sledovat stav, historii a výkonnostní metriku konkrétní instance workflowu.</span><span class="sxs-lookup"><span data-stu-id="b83cd-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="b83cd-112">To umožňuje určit, zda je potřeba provést změny workflowu ke zvýšení efektivity.</span><span class="sxs-lookup"><span data-stu-id="b83cd-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="b83cd-113">Centralizovaný seznam pracovních položek: Uživatelé mohou zobrazit centralizovaný seznam pracovních položek k zobrazení úkolů workflowu a schválení, která mají přiřazena.</span><span class="sxs-lookup"><span data-stu-id="b83cd-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="b83cd-114">**Můžete vytvářet tyto typy pracovního procesu:**</span><span class="sxs-lookup"><span data-stu-id="b83cd-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="b83cd-115">V následující tabulce jsou uvedeny typy pracovních procesů, které můžete vytvořit v části **Výdaje**.</span><span class="sxs-lookup"><span data-stu-id="b83cd-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="b83cd-116"><strong>Typ</strong></span><span class="sxs-lookup"><span data-stu-id="b83cd-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="b83cd-117"><strong>Tento typ slouží k:</strong></span><span class="sxs-lookup"><span data-stu-id="b83cd-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="b83cd-118"><strong>Vyúčtování výdajů</strong></span><span class="sxs-lookup"><span data-stu-id="b83cd-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="b83cd-119">Vytváření workflowů schválení pro sestavy výdajů.</span><span class="sxs-lookup"><span data-stu-id="b83cd-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="b83cd-120"><strong>Automatické zaúčtování sestavy výdajů</strong></span><span class="sxs-lookup"><span data-stu-id="b83cd-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="b83cd-121">Vytváření workflowů automatického zaúčtování pro sestavy výdajů.</span><span class="sxs-lookup"><span data-stu-id="b83cd-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="b83cd-122"><strong>Položka řádku výdajů</strong></span><span class="sxs-lookup"><span data-stu-id="b83cd-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="b83cd-123">Vytváření workflowů schválení pro položky řádků na sestavě výdajů.</span><span class="sxs-lookup"><span data-stu-id="b83cd-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="b83cd-124"><strong>Automatické zaúčtování položek řádku výdajů</strong></span><span class="sxs-lookup"><span data-stu-id="b83cd-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="b83cd-125">Vytváření workflowů automatického zaúčtování pro položky řádků na sestavě výdajů.</span><span class="sxs-lookup"><span data-stu-id="b83cd-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="b83cd-126"><strong>Cestovní žádanka</strong></span><span class="sxs-lookup"><span data-stu-id="b83cd-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="b83cd-127">Vytváření workflowů pro cestovní žádanky.</span><span class="sxs-lookup"><span data-stu-id="b83cd-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="b83cd-128"><strong>Požadavek na hotovostní zálohu</strong></span><span class="sxs-lookup"><span data-stu-id="b83cd-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="b83cd-129">Vytvoření workflowů schválení pro požadavky na hotovostní zálohu.</span><span class="sxs-lookup"><span data-stu-id="b83cd-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="b83cd-130"><strong>Vratka daně DPH</strong></span><span class="sxs-lookup"><span data-stu-id="b83cd-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="b83cd-131">Vytvoření workflowů schválení pro vratky daně DPH.</span><span class="sxs-lookup"><span data-stu-id="b83cd-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |

