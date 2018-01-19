---
title: "Workflow výdajů"
description: "Toto téma vysvětluje, jak můžete použít systém workflow v aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition pro nastavení procesu kontroly pro sestavy výdajů v modulu Správa výdajů."
author: saraschi2
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 25fc9b5bac4a63cdf24cca10ef3a683a3b02b527
ms.contentlocale: cs-cz
ms.lasthandoff: 01/19/2018

---

# <a name="expense-workflow"></a><span data-ttu-id="7f096-103">Workflow výdajů</span><span class="sxs-lookup"><span data-stu-id="7f096-103">Expense workflow</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7f096-104">Můžete použít systém workflow v aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition pro nastavení procesu kontroly pro sestavy výdajů v modulu Správa výdajů.</span><span class="sxs-lookup"><span data-stu-id="7f096-104">You can use the workflow system in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="7f096-105">Můžete nastavit workflow, které používá k určení osoby schvalující sestavy výdajů následující kritéria:</span><span class="sxs-lookup"><span data-stu-id="7f096-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="7f096-106">Hierarchie nadřízenosti zaměstnanců a předdefinované schvalovací limity</span><span class="sxs-lookup"><span data-stu-id="7f096-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="7f096-107">Víceúrovňové schválení, které podporuje prozatímního schvalovatele a výsledného schvalovatele</span><span class="sxs-lookup"><span data-stu-id="7f096-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="7f096-108">Finanční dimenze a odpovědnost za projekt</span><span class="sxs-lookup"><span data-stu-id="7f096-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="7f096-109">Přiřazení pro určité uživatele či skupiny uživatelů</span><span class="sxs-lookup"><span data-stu-id="7f096-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="7f096-110">Schválení workflowu lze vytvořit pro vyúčtování výdajů, cestovní žádanky, hotovostní zálohy a vratky daně z přidané hodnoty (DPH).</span><span class="sxs-lookup"><span data-stu-id="7f096-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="7f096-111">**Příklad**</span><span class="sxs-lookup"><span data-stu-id="7f096-111">**Example**</span></span>

<span data-ttu-id="7f096-112">Následující proces je příkladem workflowu správy výdajů pro vyúčtování výdajů.</span><span class="sxs-lookup"><span data-stu-id="7f096-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="7f096-113">Zaměstnanec vytvoří a uloží vyúčtování výdajů.</span><span class="sxs-lookup"><span data-stu-id="7f096-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="7f096-114">Zaměstnanec odešle vyúčtování výdajů ke schválení.</span><span class="sxs-lookup"><span data-stu-id="7f096-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="7f096-115">Schvalovatel je určen na základě pravidel definovaných při nastavení workflowu.</span><span class="sxs-lookup"><span data-stu-id="7f096-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="7f096-116">Schvalovatel obdrží oznámení o tom, že vyúčtování výdajů je připraveno ke schválení.</span><span class="sxs-lookup"><span data-stu-id="7f096-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="7f096-117">Schvalovatel zkontroluje vyúčtování výdajů a ověří, zda jsou splněny následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="7f096-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="7f096-118">Výdaje neporušují žádné zásady výdajů.</span><span class="sxs-lookup"><span data-stu-id="7f096-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="7f096-119">Pokud výdaje porušují nějakou zásadu, schvalující ověří, že vyúčtování výdajů obsahuje platné obchodní odůvodnění.</span><span class="sxs-lookup"><span data-stu-id="7f096-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="7f096-120">Elektronické příjemky jsou připojeny k sestavě výdajů.</span><span class="sxs-lookup"><span data-stu-id="7f096-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="7f096-121">Schvalovatel schválí vyúčtování výdajů.</span><span class="sxs-lookup"><span data-stu-id="7f096-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="7f096-122">Vyúčtování výdajů je přiřazeno koordinátoru závazků k zaúčtování.</span><span class="sxs-lookup"><span data-stu-id="7f096-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="7f096-123">V závislosti na tom, zda je nakonfigurováno automatické zaúčtování, dojde k jednomu z následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="7f096-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="7f096-124">Pokud je nakonfigurováno automatické zaúčtování, vyúčtování výdajů se zpracovává pro platbu a stav vyúčtování výdajů se zaktualizuje.</span><span class="sxs-lookup"><span data-stu-id="7f096-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="7f096-125">Pokud není automatické zaúčtování nakonfigurováno, koordinátor závazků ověří, že všechny originály příjemek byly odeslány a že jsou příjemky ve shodě s výdaji na vyúčtování výdajů.</span><span class="sxs-lookup"><span data-stu-id="7f096-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="7f096-126">Všechny kódy daně, které jsou zadány ve vyúčtování výdajů, musí být ověřeny ohledně správnosti.</span><span class="sxs-lookup"><span data-stu-id="7f096-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="7f096-127">Po ověření těchto požadavků dojde k zaúčtování výdajů.</span><span class="sxs-lookup"><span data-stu-id="7f096-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="7f096-128">Po zaúčtování výdajů se autorizuje platba za výdaje a zaměstnanci je vyplacena úhrada.</span><span class="sxs-lookup"><span data-stu-id="7f096-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>

