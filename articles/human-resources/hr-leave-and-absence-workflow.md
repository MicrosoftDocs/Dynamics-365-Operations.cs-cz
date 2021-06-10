---
title: Vytvoření workflowu žádosti o pracovní volno
description: Vytvoření workflowu žádosti o pracovní volno a absenci pro konzistentní správu žádostí o pracovní volno v Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 05/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5580b4b07b2d335ad9444a064c726bc4aca1db6a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056533"
---
# <a name="create-a-leave-request-workflow"></a><span data-ttu-id="67d04-103">Vytvoření workflowu žádosti o pracovní volno</span><span class="sxs-lookup"><span data-stu-id="67d04-103">Create a leave request workflow</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="67d04-104">Workflow v Dynamics 365 Human Resources můžete vytvořit pro účely konzistentní správy žádostí o pracovní volno a absenci.</span><span class="sxs-lookup"><span data-stu-id="67d04-104">You can create a workflow in Dynamics 365 Human Resources to consistently manage your leave and absence requests.</span></span> <span data-ttu-id="67d04-105">Workflow **pracovní volno a absence** vám umožňuje:</span><span class="sxs-lookup"><span data-stu-id="67d04-105">A **Leave and absence** workflow lets you:</span></span>

- <span data-ttu-id="67d04-106">Definovat úkoly</span><span class="sxs-lookup"><span data-stu-id="67d04-106">Define tasks</span></span>
- <span data-ttu-id="67d04-107">Určit, kdo musí dokončit úkoly</span><span class="sxs-lookup"><span data-stu-id="67d04-107">Determine who must complete the tasks</span></span>
- <span data-ttu-id="67d04-108">Určit, kdo může schvalovat nebo zamítnout požadavky</span><span class="sxs-lookup"><span data-stu-id="67d04-108">Specify who can approve or reject requests</span></span>

## <a name="create-a-leave-and-absence-request-workflow"></a><span data-ttu-id="67d04-109">Vytvoření workflow žádosti o pracovní volno a absenci</span><span class="sxs-lookup"><span data-stu-id="67d04-109">Create a Leave and absence request workflow</span></span>

1. <span data-ttu-id="67d04-110">Na stránce **Pracovní volno a absence** klikněte na kartu **Odkazy**.</span><span class="sxs-lookup"><span data-stu-id="67d04-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="67d04-111">V části **Nastavení** vyberte **Workflowy lidských zdrojů**.</span><span class="sxs-lookup"><span data-stu-id="67d04-111">Under **Setup**, select **Human resource workflows**.</span></span>

3. <span data-ttu-id="67d04-112">Vyberte **Nový** a poté vyberte **Žádost o pracovní volno a absenci**.</span><span class="sxs-lookup"><span data-stu-id="67d04-112">Select **New**, and then select **Leave and absence request**.</span></span> 

4. <span data-ttu-id="67d04-113">Když se zobrazí pole se zprávou **Otevřít tento soubor?**, vyberte **Otevřít** a přihlaste se pomocí svých přihlašovacích údajů.</span><span class="sxs-lookup"><span data-stu-id="67d04-113">When the **Open this file?** message box appears, select **Open** and sign in with your company credentials.</span></span>

5. <span data-ttu-id="67d04-114">Pomocí editoru workflowu vytvořte workflow žádosti o pracovní volno.</span><span class="sxs-lookup"><span data-stu-id="67d04-114">Use the workflow editor to create a workflow for your leave requests.</span></span> <span data-ttu-id="67d04-115">Další informace o práci s workflowy naleznete v tématu [Vytvoření přehledu workflowů](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)</span><span class="sxs-lookup"><span data-stu-id="67d04-115">For more information about working with workflows, see [Create workflows overview](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)</span></span>

## <a name="leave-and-absence-request-workflow-data-elements"></a><span data-ttu-id="67d04-116">Vytvoření datových prvků workflow žádosti o pracovní volno a absenci</span><span class="sxs-lookup"><span data-stu-id="67d04-116">Leave and absence request workflow data elements</span></span>

<span data-ttu-id="67d04-117">Následující datové prvky můžete použít k vytvoření podmíněných nebo automatických schválení v pracovních postupech pro žádosti o dovolenou a nepřítomnost:</span><span class="sxs-lookup"><span data-stu-id="67d04-117">You can use the following data elements to create conditional or automatic approvals in workflows for leave and absence requests:</span></span>

- <span data-ttu-id="67d04-118">**Částka**</span><span class="sxs-lookup"><span data-stu-id="67d04-118">**Amount**</span></span>
- <span data-ttu-id="67d04-119">**Komentář**</span><span class="sxs-lookup"><span data-stu-id="67d04-119">**Comment**</span></span>
- <span data-ttu-id="67d04-120">**Společnost**</span><span class="sxs-lookup"><span data-stu-id="67d04-120">**Company**</span></span>
- <span data-ttu-id="67d04-121">**Vytvořil/a**</span><span class="sxs-lookup"><span data-stu-id="67d04-121">**Created by**</span></span>
- <span data-ttu-id="67d04-122">**Datum a čas vytvoření**</span><span class="sxs-lookup"><span data-stu-id="67d04-122">**Created date and time**</span></span>
- <span data-ttu-id="67d04-123">**Datum ukončení**</span><span class="sxs-lookup"><span data-stu-id="67d04-123">**End date**</span></span>
- <span data-ttu-id="67d04-124">**Typ volna**</span><span class="sxs-lookup"><span data-stu-id="67d04-124">**Leave type**</span></span>
- <span data-ttu-id="67d04-125">**Změnil(a)**</span><span class="sxs-lookup"><span data-stu-id="67d04-125">**Modified by**</span></span>
- <span data-ttu-id="67d04-126">**Datum a čas úpravy**</span><span class="sxs-lookup"><span data-stu-id="67d04-126">**Modified date and time**</span></span>
- <span data-ttu-id="67d04-127">**Kód důvodu**</span><span class="sxs-lookup"><span data-stu-id="67d04-127">**Reason code**</span></span>
- <span data-ttu-id="67d04-128">**ID požadavku**</span><span class="sxs-lookup"><span data-stu-id="67d04-128">**Request ID**</span></span>
- <span data-ttu-id="67d04-129">**Datum zahájení**</span><span class="sxs-lookup"><span data-stu-id="67d04-129">**Start date**</span></span>
- <span data-ttu-id="67d04-130">**Stav**</span><span class="sxs-lookup"><span data-stu-id="67d04-130">**Status**</span></span> 
- <span data-ttu-id="67d04-131">**Datum odeslání**</span><span class="sxs-lookup"><span data-stu-id="67d04-131">**Submission date**</span></span>
- <span data-ttu-id="67d04-132">**Odeslal**</span><span class="sxs-lookup"><span data-stu-id="67d04-132">**Submitted by**</span></span>
- <span data-ttu-id="67d04-133">**Odesláno personálním oddělením**</span><span class="sxs-lookup"><span data-stu-id="67d04-133">**Submitted by Human resources**</span></span>
- <span data-ttu-id="67d04-134">**Odesláno manažerem**</span><span class="sxs-lookup"><span data-stu-id="67d04-134">**Submitted by Manager**</span></span>
- <span data-ttu-id="67d04-135">**Zadáno jménem**</span><span class="sxs-lookup"><span data-stu-id="67d04-135">**Submitted on behalf**</span></span>
- <span data-ttu-id="67d04-136">**Pracovní podproces**</span><span class="sxs-lookup"><span data-stu-id="67d04-136">**Worker**</span></span>
- <span data-ttu-id="67d04-137">**Typ pracovníka**</span><span class="sxs-lookup"><span data-stu-id="67d04-137">**Worker type**</span></span>

<span data-ttu-id="67d04-138">Tyto příklady ukazují, jak lze pomocí různých datových prvků vytvořit různé typy podmínek pracovního postupu:</span><span class="sxs-lookup"><span data-stu-id="67d04-138">These examples show how you can create different types of workflow conditions by using these data elements:</span></span>

- <span data-ttu-id="67d04-139">Použijte **Kód důvodu** v podmíněném prohlášení pro směrování žádostí o nemocenskou dovolenou s kódem důvodu **Chirurgická operace** pro předložení HR ke schválení. Všechny ostatní kódy důvodu předkládejte vedoucímu.</span><span class="sxs-lookup"><span data-stu-id="67d04-139">Use **Reason code** in a conditional statement to route sick leave requests with the reason code **Surgery** to HR for approval, while routing all other reason codes to the manager.</span></span> <span data-ttu-id="67d04-140">Další informace o podmíněných příkazech získáte v tématu [Konfigurace podmíněných rozhodnutí ve workflow](../fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="67d04-140">For more information about conditional statements, see [Configure conditional decisions in a workflow](../fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow.md).</span></span> 

- <span data-ttu-id="67d04-141">Volby **Předloženo personálním oddělením** a **Předloženo manažerem** v automatické akci použijte k automatickému schvalování žádostí o dovolenou, které tyto role předkládají jménem zaměstnanců.</span><span class="sxs-lookup"><span data-stu-id="67d04-141">Use **Submitted by Human resources** and **Submitted by manager** in an automatic action to automatically approve leave requests that these roles submit on behalf of employees.</span></span> <span data-ttu-id="67d04-142">Další informace o automatických akcích naleznete v tématu [Konfigurace procesů schvalování ve workflow](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="67d04-142">For more information about automatic actions, see [Configure approval processes in a workflow](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md).</span></span>

- <span data-ttu-id="67d04-143">Pomocí příkazu **Typ dovolené** v podmíněném příkazu nebo automatické akci určete, jak workflow směruje požadavky u určitých typů dovolené.</span><span class="sxs-lookup"><span data-stu-id="67d04-143">Use **Leave type** in a conditional statement or automatic action to control how the workflow routes requests with certain leave types.</span></span>

## <a name="see-also"></a><span data-ttu-id="67d04-144">Viz také</span><span class="sxs-lookup"><span data-stu-id="67d04-144">See also</span></span>

- [<span data-ttu-id="67d04-145">Přehled pracovního volna a absencí</span><span class="sxs-lookup"><span data-stu-id="67d04-145">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]