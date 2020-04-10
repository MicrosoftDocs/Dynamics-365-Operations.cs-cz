---
title: Workflow správy výdajů
description: Toto téma vysvětluje, jak můžete použít systém workflow v aplikaci Microsoft Dynamics 365 Finance pro nastavení procesu kontroly pro sestavy výdajů v modulu Správa výdajů.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5207be92cb58d8ab2658096b3e0f3fc81d73d91e
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/21/2020
ms.locfileid: "3153964"
---
# <a name="expense-management-workflow"></a><span data-ttu-id="d8cbf-103">Workflow správy výdajů</span><span class="sxs-lookup"><span data-stu-id="d8cbf-103">Expense management workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d8cbf-104">Můžete použít systém workflow pro nastavení procesu kontroly pro sestavy výdajů v modulu Správa výdajů.</span><span class="sxs-lookup"><span data-stu-id="d8cbf-104">You can use the workflow system to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="d8cbf-105">Můžete nastavit workflow, které používá k určení osoby schvalující sestavy výdajů následující kritéria:</span><span class="sxs-lookup"><span data-stu-id="d8cbf-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="d8cbf-106">Hierarchie nadřízenosti zaměstnanců a předdefinované schvalovací limity</span><span class="sxs-lookup"><span data-stu-id="d8cbf-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="d8cbf-107">Víceúrovňové schválení, které podporuje prozatímního schvalovatele a výsledného schvalovatele</span><span class="sxs-lookup"><span data-stu-id="d8cbf-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="d8cbf-108">Finanční dimenze a odpovědnost za projekt</span><span class="sxs-lookup"><span data-stu-id="d8cbf-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="d8cbf-109">Přiřazení pro určité uživatele či skupiny uživatelů</span><span class="sxs-lookup"><span data-stu-id="d8cbf-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="d8cbf-110">Schválení workflowu lze vytvořit pro vyúčtování výdajů, cestovní žádanky, hotovostní zálohy a vratky daně z přidané hodnoty (DPH).</span><span class="sxs-lookup"><span data-stu-id="d8cbf-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="d8cbf-111">**Příklad**</span><span class="sxs-lookup"><span data-stu-id="d8cbf-111">**Example**</span></span>

<span data-ttu-id="d8cbf-112">Následující proces je příkladem workflowu správy výdajů pro vyúčtování výdajů.</span><span class="sxs-lookup"><span data-stu-id="d8cbf-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="d8cbf-113">Zaměstnanec vytvoří a uloží vyúčtování výdajů.</span><span class="sxs-lookup"><span data-stu-id="d8cbf-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="d8cbf-114">Zaměstnanec odešle vyúčtování výdajů ke schválení.</span><span class="sxs-lookup"><span data-stu-id="d8cbf-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="d8cbf-115">Schvalovatel je určen na základě pravidel definovaných při nastavení workflowu.</span><span class="sxs-lookup"><span data-stu-id="d8cbf-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="d8cbf-116">Schvalovatel obdrží oznámení o tom, že vyúčtování výdajů je připraveno ke schválení.</span><span class="sxs-lookup"><span data-stu-id="d8cbf-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="d8cbf-117">Schvalovatel zkontroluje vyúčtování výdajů a ověří, zda jsou splněny následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="d8cbf-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="d8cbf-118">Výdaje neporušují žádné zásady výdajů.</span><span class="sxs-lookup"><span data-stu-id="d8cbf-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="d8cbf-119">Pokud výdaje porušují nějakou zásadu, schvalující ověří, že vyúčtování výdajů obsahuje platné obchodní odůvodnění.</span><span class="sxs-lookup"><span data-stu-id="d8cbf-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="d8cbf-120">Elektronické příjemky jsou připojeny k sestavě výdajů.</span><span class="sxs-lookup"><span data-stu-id="d8cbf-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="d8cbf-121">Schvalovatel schválí vyúčtování výdajů.</span><span class="sxs-lookup"><span data-stu-id="d8cbf-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="d8cbf-122">Vyúčtování výdajů je přiřazeno koordinátoru závazků k zaúčtování.</span><span class="sxs-lookup"><span data-stu-id="d8cbf-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="d8cbf-123">V závislosti na tom, zda je nakonfigurováno automatické zaúčtování, dojde k jednomu z následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="d8cbf-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="d8cbf-124">Pokud je nakonfigurováno automatické zaúčtování, vyúčtování výdajů se zpracovává pro platbu a stav vyúčtování výdajů se zaktualizuje.</span><span class="sxs-lookup"><span data-stu-id="d8cbf-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="d8cbf-125">Pokud není automatické zaúčtování nakonfigurováno, koordinátor závazků ověří, že všechny originály příjemek byly odeslány a že jsou příjemky ve shodě s výdaji na vyúčtování výdajů.</span><span class="sxs-lookup"><span data-stu-id="d8cbf-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="d8cbf-126">Všechny kódy daně, které jsou zadány ve vyúčtování výdajů, musí být ověřeny ohledně správnosti.</span><span class="sxs-lookup"><span data-stu-id="d8cbf-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="d8cbf-127">Po ověření těchto požadavků dojde k zaúčtování výdajů.</span><span class="sxs-lookup"><span data-stu-id="d8cbf-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="d8cbf-128">Po zaúčtování výdajů se autorizuje platba za výdaje a zaměstnanci je vyplacena úhrada.</span><span class="sxs-lookup"><span data-stu-id="d8cbf-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>
