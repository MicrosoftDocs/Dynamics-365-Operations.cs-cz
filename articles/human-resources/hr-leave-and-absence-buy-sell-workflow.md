---
title: Vytvoření pracovního postupu žádosti o koupi a prodej pracovního volna
description: Vytvpřte pracovního postupu žádosti o koupi a prodej pracovního volna pro konzistentní správu koupi a prodeje pracovního volna v Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 08/20/2020
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
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4732b5dafc8074c5c59f10f02bbee7e22f51960a
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/04/2021
ms.locfileid: "5116037"
---
# <a name="create-a-buy-and-sell-leave-request-workflow"></a><span data-ttu-id="b9e64-103">Vytvoření pracovního postupu žádosti o koupi a prodej pracovního volna</span><span class="sxs-lookup"><span data-stu-id="b9e64-103">Create a buy and sell leave request workflow</span></span>

<span data-ttu-id="b9e64-104">V aplikaci Dynamics 365 Human Resources můžete vytvořit pracovní postup pro účely konzistentní správy žádostí o koupi a prodej pracovního volna.</span><span class="sxs-lookup"><span data-stu-id="b9e64-104">You can create a workflow in Dynamics 365 Human Resources to consistently manage your buy and sell leave requests.</span></span> <span data-ttu-id="b9e64-105">Pracovní postup **Koupě a prodej pracovního volna** vám umožňuje:</span><span class="sxs-lookup"><span data-stu-id="b9e64-105">A **Buy and sell leave** workflow lets you:</span></span>

- <span data-ttu-id="b9e64-106">Definovat úkoly</span><span class="sxs-lookup"><span data-stu-id="b9e64-106">Define tasks</span></span>
- <span data-ttu-id="b9e64-107">Určit, kdo musí dokončit úkoly</span><span class="sxs-lookup"><span data-stu-id="b9e64-107">Determine who must complete the tasks</span></span>
- <span data-ttu-id="b9e64-108">Určit, kdo může schvalovat nebo zamítnout požadavky</span><span class="sxs-lookup"><span data-stu-id="b9e64-108">Specify who can approve or reject requests</span></span>

## <a name="create-a-buy-and-sell-leave-request-workflow"></a><span data-ttu-id="b9e64-109">Vytvoření pracovního postupu žádosti o koupi a prodej pracovního volna</span><span class="sxs-lookup"><span data-stu-id="b9e64-109">Create a buy and sell leave request workflow</span></span>

1. <span data-ttu-id="b9e64-110">Na stránce **Pracovní volno a absence** klikněte na kartu **Odkazy**.</span><span class="sxs-lookup"><span data-stu-id="b9e64-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="b9e64-111">V části **Nastavení** vyberte **Workflowy lidských zdrojů**.</span><span class="sxs-lookup"><span data-stu-id="b9e64-111">Under **Setup**, select **Human resource workflows**.</span></span>

3. <span data-ttu-id="b9e64-112">Vyberte **Nový** a poté vyberte **Žádost o koupi a prodej pracovního volna**.</span><span class="sxs-lookup"><span data-stu-id="b9e64-112">Select **New**, and then select **Buy and sell leave request**.</span></span> 

4. <span data-ttu-id="b9e64-113">Když se zobrazí pole se zprávou **Otevřít tento soubor?**, vyberte **Otevřít** a přihlaste se pomocí svých přihlašovacích údajů.</span><span class="sxs-lookup"><span data-stu-id="b9e64-113">When the **Open this file?** message box appears, select **Open** and sign in with your company credentials.</span></span>

5. <span data-ttu-id="b9e64-114">Pomocí editoru workflowu vytvořte workflow žádosti o pracovní volno.</span><span class="sxs-lookup"><span data-stu-id="b9e64-114">Use the workflow editor to create a workflow for your leave requests.</span></span> <span data-ttu-id="b9e64-115">Další informace o práci s workflowy naleznete v tématu [Vytvoření přehledu workflowů](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span><span class="sxs-lookup"><span data-stu-id="b9e64-115">For more information about working with workflows, see [Create workflows overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span></span>

## <a name="leave-and-absence-request-workflow-data-elements"></a><span data-ttu-id="b9e64-116">Vytvoření datových prvků workflow žádosti o pracovní volno a absenci</span><span class="sxs-lookup"><span data-stu-id="b9e64-116">Leave and absence request workflow data elements</span></span>

<span data-ttu-id="b9e64-117">Následující datové prvky můžete použít k vytvoření podmíněných nebo automatických schválení v pracovních postupech pro žádosti o koupi a prodej pracovního volna:</span><span class="sxs-lookup"><span data-stu-id="b9e64-117">You can use the following data elements to create conditional or automatic approvals in workflows for buy and sell leave requests:</span></span>

- <span data-ttu-id="b9e64-118">**Částka**</span><span class="sxs-lookup"><span data-stu-id="b9e64-118">**Amount**</span></span>
- <span data-ttu-id="b9e64-119">**Zásady nákupu a prodeje pracovního volna**</span><span class="sxs-lookup"><span data-stu-id="b9e64-119">**Buy and sell leave policy**</span></span>
- <span data-ttu-id="b9e64-120">**Společnost**</span><span class="sxs-lookup"><span data-stu-id="b9e64-120">**Company**</span></span>
- <span data-ttu-id="b9e64-121">**Vytvořil**</span><span class="sxs-lookup"><span data-stu-id="b9e64-121">**Created by**</span></span>
- <span data-ttu-id="b9e64-122">**Datum a čas vytvoření**</span><span class="sxs-lookup"><span data-stu-id="b9e64-122">**Created date and time**</span></span>
- <span data-ttu-id="b9e64-123">**Koncové datum**</span><span class="sxs-lookup"><span data-stu-id="b9e64-123">**End date**</span></span>
- <span data-ttu-id="b9e64-124">**Typ pracovního volna**</span><span class="sxs-lookup"><span data-stu-id="b9e64-124">**Leave type**</span></span>
- <span data-ttu-id="b9e64-125">**Změnil/a**</span><span class="sxs-lookup"><span data-stu-id="b9e64-125">**Modified by**</span></span>
- <span data-ttu-id="b9e64-126">**Datum a čas úpravy**</span><span class="sxs-lookup"><span data-stu-id="b9e64-126">**Modified date and time**</span></span>
- <span data-ttu-id="b9e64-127">**ID požadavku**</span><span class="sxs-lookup"><span data-stu-id="b9e64-127">**Request ID**</span></span>
- <span data-ttu-id="b9e64-128">**Datum zahájení**</span><span class="sxs-lookup"><span data-stu-id="b9e64-128">**Start date**</span></span>
- <span data-ttu-id="b9e64-129">**Stav**</span><span class="sxs-lookup"><span data-stu-id="b9e64-129">**Status**</span></span> 
- <span data-ttu-id="b9e64-130">**Datum odeslání**</span><span class="sxs-lookup"><span data-stu-id="b9e64-130">**Submission date**</span></span>
- <span data-ttu-id="b9e64-131">**Odeslal/a**</span><span class="sxs-lookup"><span data-stu-id="b9e64-131">**Submitted by**</span></span>
- <span data-ttu-id="b9e64-132">**Odesláno personálním oddělením**</span><span class="sxs-lookup"><span data-stu-id="b9e64-132">**Submitted by Human resources**</span></span>
- <span data-ttu-id="b9e64-133">**Odesláno manažerem**</span><span class="sxs-lookup"><span data-stu-id="b9e64-133">**Submitted by Manager**</span></span>
- <span data-ttu-id="b9e64-134">**Zadáno jménem**</span><span class="sxs-lookup"><span data-stu-id="b9e64-134">**Submitted on behalf**</span></span>
- <span data-ttu-id="b9e64-135">**Pracovní podproces**</span><span class="sxs-lookup"><span data-stu-id="b9e64-135">**Worker**</span></span>

## <a name="workflow-examples"></a><span data-ttu-id="b9e64-136">Příklady pracovních postupů</span><span class="sxs-lookup"><span data-stu-id="b9e64-136">Workflow examples</span></span>

<span data-ttu-id="b9e64-137">Tyto příklady ukazují, jak lze pomocí různých datových prvků vytvořit různé typy podmínek pracovního postupu:</span><span class="sxs-lookup"><span data-stu-id="b9e64-137">These examples show how you can create different types of workflow conditions by using these data elements:</span></span>

- <span data-ttu-id="b9e64-138">Volby **Předloženo personálním oddělením** a **Předloženo manažerem** v automatické akci použijte k automatickému schvalování žádostí o koupi a prodej pracovního volna, které tyto role předkládají jménem zaměstnanců.</span><span class="sxs-lookup"><span data-stu-id="b9e64-138">Use **Submitted by Human resources** and **Submitted by manager** in an automatic action to automatically approve buy and sell leave requests that these roles submit on behalf of employees.</span></span> <span data-ttu-id="b9e64-139">Další informace o automatických akcích naleznete v tématu [Konfigurace procesů schvalování ve workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span><span class="sxs-lookup"><span data-stu-id="b9e64-139">For more information about automatic actions, see [Configure approval processes in a workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span></span>

- <span data-ttu-id="b9e64-140">Pomocí příkazu **Typ dovolené** v podmíněném příkazu nebo automatické akci určete, jak workflow směruje požadavky u určitých typů dovolené.</span><span class="sxs-lookup"><span data-stu-id="b9e64-140">Use **Leave type** in a conditional statement or automatic action to control how the workflow routes requests with certain leave types.</span></span>

## <a name="see-also"></a><span data-ttu-id="b9e64-141">Viz také</span><span class="sxs-lookup"><span data-stu-id="b9e64-141">See also</span></span>

[<span data-ttu-id="b9e64-142">Přehled pracovního volna a absencí</span><span class="sxs-lookup"><span data-stu-id="b9e64-142">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)<br>
[<span data-ttu-id="b9e64-143">Správa zásad nákupu a prodeje pracovního volna</span><span class="sxs-lookup"><span data-stu-id="b9e64-143">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)

