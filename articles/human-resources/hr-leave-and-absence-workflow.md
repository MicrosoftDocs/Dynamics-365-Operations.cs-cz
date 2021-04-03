---
title: Vytvoření workflowu žádosti o pracovní volno
description: Vytvoření workflowu žádosti o pracovní volno a absenci pro konzistentní správu žádostí o pracovní volno v Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 05/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c2c2020c68c4aca3594a2532d32f968ab76f6b7b
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/17/2021
ms.locfileid: "5463303"
---
# <a name="create-a-leave-request-workflow"></a><span data-ttu-id="7a2d3-103">Vytvoření workflowu žádosti o pracovní volno</span><span class="sxs-lookup"><span data-stu-id="7a2d3-103">Create a leave request workflow</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="7a2d3-104">Workflow v Dynamics 365 Human Resources můžete vytvořit pro účely konzistentní správy žádostí o pracovní volno a absenci.</span><span class="sxs-lookup"><span data-stu-id="7a2d3-104">You can create a workflow in Dynamics 365 Human Resources to consistently manage your leave and absence requests.</span></span> <span data-ttu-id="7a2d3-105">Workflow **pracovní volno a absence** vám umožňuje:</span><span class="sxs-lookup"><span data-stu-id="7a2d3-105">A **Leave and absence** workflow lets you:</span></span>

- <span data-ttu-id="7a2d3-106">Definovat úkoly</span><span class="sxs-lookup"><span data-stu-id="7a2d3-106">Define tasks</span></span>
- <span data-ttu-id="7a2d3-107">Určit, kdo musí dokončit úkoly</span><span class="sxs-lookup"><span data-stu-id="7a2d3-107">Determine who must complete the tasks</span></span>
- <span data-ttu-id="7a2d3-108">Určit, kdo může schvalovat nebo zamítnout požadavky</span><span class="sxs-lookup"><span data-stu-id="7a2d3-108">Specify who can approve or reject requests</span></span>

## <a name="create-a-leave-and-absence-request-workflow"></a><span data-ttu-id="7a2d3-109">Vytvoření workflow žádosti o pracovní volno a absenci</span><span class="sxs-lookup"><span data-stu-id="7a2d3-109">Create a Leave and absence request workflow</span></span>

1. <span data-ttu-id="7a2d3-110">Na stránce **Pracovní volno a absence** klikněte na kartu **Odkazy**.</span><span class="sxs-lookup"><span data-stu-id="7a2d3-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="7a2d3-111">V části **Nastavení** vyberte **Workflowy lidských zdrojů**.</span><span class="sxs-lookup"><span data-stu-id="7a2d3-111">Under **Setup**, select **Human resource workflows**.</span></span>

3. <span data-ttu-id="7a2d3-112">Vyberte **Nový** a poté vyberte **Žádost o pracovní volno a absenci**.</span><span class="sxs-lookup"><span data-stu-id="7a2d3-112">Select **New**, and then select **Leave and absence request**.</span></span> 

4. <span data-ttu-id="7a2d3-113">Když se zobrazí pole se zprávou **Otevřít tento soubor?**, vyberte **Otevřít** a přihlaste se pomocí svých přihlašovacích údajů.</span><span class="sxs-lookup"><span data-stu-id="7a2d3-113">When the **Open this file?** message box appears, select **Open** and sign in with your company credentials.</span></span>

5. <span data-ttu-id="7a2d3-114">Pomocí editoru workflowu vytvořte workflow žádosti o pracovní volno.</span><span class="sxs-lookup"><span data-stu-id="7a2d3-114">Use the workflow editor to create a workflow for your leave requests.</span></span> <span data-ttu-id="7a2d3-115">Další informace o práci s workflowy naleznete v tématu [Vytvoření přehledu workflowů](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span><span class="sxs-lookup"><span data-stu-id="7a2d3-115">For more information about working with workflows, see [Create workflows overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span></span>

## <a name="leave-and-absence-request-workflow-data-elements"></a><span data-ttu-id="7a2d3-116">Vytvoření datových prvků workflow žádosti o pracovní volno a absenci</span><span class="sxs-lookup"><span data-stu-id="7a2d3-116">Leave and absence request workflow data elements</span></span>

<span data-ttu-id="7a2d3-117">Následující datové prvky můžete použít k vytvoření podmíněných nebo automatických schválení v pracovních postupech pro žádosti o dovolenou a nepřítomnost:</span><span class="sxs-lookup"><span data-stu-id="7a2d3-117">You can use the following data elements to create conditional or automatic approvals in workflows for leave and absence requests:</span></span>

- <span data-ttu-id="7a2d3-118">**Částka**</span><span class="sxs-lookup"><span data-stu-id="7a2d3-118">**Amount**</span></span>
- <span data-ttu-id="7a2d3-119">**Komentář**</span><span class="sxs-lookup"><span data-stu-id="7a2d3-119">**Comment**</span></span>
- <span data-ttu-id="7a2d3-120">**Společnost**</span><span class="sxs-lookup"><span data-stu-id="7a2d3-120">**Company**</span></span>
- <span data-ttu-id="7a2d3-121">**Vytvořil/a**</span><span class="sxs-lookup"><span data-stu-id="7a2d3-121">**Created by**</span></span>
- <span data-ttu-id="7a2d3-122">**Datum a čas vytvoření**</span><span class="sxs-lookup"><span data-stu-id="7a2d3-122">**Created date and time**</span></span>
- <span data-ttu-id="7a2d3-123">**Datum ukončení**</span><span class="sxs-lookup"><span data-stu-id="7a2d3-123">**End date**</span></span>
- <span data-ttu-id="7a2d3-124">**Typ volna**</span><span class="sxs-lookup"><span data-stu-id="7a2d3-124">**Leave type**</span></span>
- <span data-ttu-id="7a2d3-125">**Změnil(a)**</span><span class="sxs-lookup"><span data-stu-id="7a2d3-125">**Modified by**</span></span>
- <span data-ttu-id="7a2d3-126">**Datum a čas úpravy**</span><span class="sxs-lookup"><span data-stu-id="7a2d3-126">**Modified date and time**</span></span>
- <span data-ttu-id="7a2d3-127">**Kód důvodu**</span><span class="sxs-lookup"><span data-stu-id="7a2d3-127">**Reason code**</span></span>
- <span data-ttu-id="7a2d3-128">**ID požadavku**</span><span class="sxs-lookup"><span data-stu-id="7a2d3-128">**Request ID**</span></span>
- <span data-ttu-id="7a2d3-129">**Datum zahájení**</span><span class="sxs-lookup"><span data-stu-id="7a2d3-129">**Start date**</span></span>
- <span data-ttu-id="7a2d3-130">**Stav**</span><span class="sxs-lookup"><span data-stu-id="7a2d3-130">**Status**</span></span> 
- <span data-ttu-id="7a2d3-131">**Datum odeslání**</span><span class="sxs-lookup"><span data-stu-id="7a2d3-131">**Submission date**</span></span>
- <span data-ttu-id="7a2d3-132">**Odeslal**</span><span class="sxs-lookup"><span data-stu-id="7a2d3-132">**Submitted by**</span></span>
- <span data-ttu-id="7a2d3-133">**Odesláno personálním oddělením**</span><span class="sxs-lookup"><span data-stu-id="7a2d3-133">**Submitted by Human resources**</span></span>
- <span data-ttu-id="7a2d3-134">**Odesláno manažerem**</span><span class="sxs-lookup"><span data-stu-id="7a2d3-134">**Submitted by Manager**</span></span>
- <span data-ttu-id="7a2d3-135">**Zadáno jménem**</span><span class="sxs-lookup"><span data-stu-id="7a2d3-135">**Submitted on behalf**</span></span>
- <span data-ttu-id="7a2d3-136">**Pracovní podproces**</span><span class="sxs-lookup"><span data-stu-id="7a2d3-136">**Worker**</span></span>
- <span data-ttu-id="7a2d3-137">**Typ pracovníka**</span><span class="sxs-lookup"><span data-stu-id="7a2d3-137">**Worker type**</span></span>

<span data-ttu-id="7a2d3-138">Tyto příklady ukazují, jak lze pomocí různých datových prvků vytvořit různé typy podmínek pracovního postupu:</span><span class="sxs-lookup"><span data-stu-id="7a2d3-138">These examples show how you can create different types of workflow conditions by using these data elements:</span></span>

- <span data-ttu-id="7a2d3-139">Použijte **Kód důvodu** v podmíněném prohlášení pro směrování žádostí o nemocenskou dovolenou s kódem důvodu **Chirurgická operace** pro předložení HR ke schválení. Všechny ostatní kódy důvodu předkládejte vedoucímu.</span><span class="sxs-lookup"><span data-stu-id="7a2d3-139">Use **Reason code** in a conditional statement to route sick leave requests with the reason code **Surgery** to HR for approval, while routing all other reason codes to the manager.</span></span> <span data-ttu-id="7a2d3-140">Další informace o podmíněných příkazech získáte v tématu [Konfigurace podmíněných rozhodnutí ve workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow).</span><span class="sxs-lookup"><span data-stu-id="7a2d3-140">For more information about conditional statements, see [Configure conditional decisions in a workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow).</span></span> 

- <span data-ttu-id="7a2d3-141">Volby **Předloženo personálním oddělením** a **Předloženo manažerem** v automatické akci použijte k automatickému schvalování žádostí o dovolenou, které tyto role předkládají jménem zaměstnanců.</span><span class="sxs-lookup"><span data-stu-id="7a2d3-141">Use **Submitted by Human resources** and **Submitted by manager** in an automatic action to automatically approve leave requests that these roles submit on behalf of employees.</span></span> <span data-ttu-id="7a2d3-142">Další informace o automatických akcích naleznete v tématu [Konfigurace procesů schvalování ve workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span><span class="sxs-lookup"><span data-stu-id="7a2d3-142">For more information about automatic actions, see [Configure approval processes in a workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span></span>

- <span data-ttu-id="7a2d3-143">Pomocí příkazu **Typ dovolené** v podmíněném příkazu nebo automatické akci určete, jak workflow směruje požadavky u určitých typů dovolené.</span><span class="sxs-lookup"><span data-stu-id="7a2d3-143">Use **Leave type** in a conditional statement or automatic action to control how the workflow routes requests with certain leave types.</span></span>

## <a name="see-also"></a><span data-ttu-id="7a2d3-144">Viz také</span><span class="sxs-lookup"><span data-stu-id="7a2d3-144">See also</span></span>

- [<span data-ttu-id="7a2d3-145">Přehled pracovního volna a absencí</span><span class="sxs-lookup"><span data-stu-id="7a2d3-145">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]