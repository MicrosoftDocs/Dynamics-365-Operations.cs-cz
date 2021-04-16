---
title: Vytvoření pracovního postupu žádosti o koupi a prodej pracovního volna
description: Vytvpřte pracovního postupu žádosti o koupi a prodej pracovního volna pro konzistentní správu koupi a prodeje pracovního volna v Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: a0ddb3ea3aa7f1941ff486d7a3e1db5846fac3eb
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5790541"
---
# <a name="create-a-buy-and-sell-leave-request-workflow"></a><span data-ttu-id="dc8eb-103">Vytvoření pracovního postupu žádosti o koupi a prodej pracovního volna</span><span class="sxs-lookup"><span data-stu-id="dc8eb-103">Create a buy and sell leave request workflow</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="dc8eb-104">V aplikaci Dynamics 365 Human Resources můžete vytvořit pracovní postup pro účely konzistentní správy žádostí o koupi a prodej pracovního volna.</span><span class="sxs-lookup"><span data-stu-id="dc8eb-104">You can create a workflow in Dynamics 365 Human Resources to consistently manage your buy and sell leave requests.</span></span> <span data-ttu-id="dc8eb-105">Pracovní postup **Koupě a prodej pracovního volna** vám umožňuje:</span><span class="sxs-lookup"><span data-stu-id="dc8eb-105">A **Buy and sell leave** workflow lets you:</span></span>

- <span data-ttu-id="dc8eb-106">Definovat úkoly</span><span class="sxs-lookup"><span data-stu-id="dc8eb-106">Define tasks</span></span>
- <span data-ttu-id="dc8eb-107">Určit, kdo musí dokončit úkoly</span><span class="sxs-lookup"><span data-stu-id="dc8eb-107">Determine who must complete the tasks</span></span>
- <span data-ttu-id="dc8eb-108">Určit, kdo může schvalovat nebo zamítnout požadavky</span><span class="sxs-lookup"><span data-stu-id="dc8eb-108">Specify who can approve or reject requests</span></span>

## <a name="create-a-buy-and-sell-leave-request-workflow"></a><span data-ttu-id="dc8eb-109">Vytvoření pracovního postupu žádosti o koupi a prodej pracovního volna</span><span class="sxs-lookup"><span data-stu-id="dc8eb-109">Create a buy and sell leave request workflow</span></span>

1. <span data-ttu-id="dc8eb-110">Na stránce **Pracovní volno a absence** klikněte na kartu **Odkazy**.</span><span class="sxs-lookup"><span data-stu-id="dc8eb-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="dc8eb-111">V části **Nastavení** vyberte **Workflowy lidských zdrojů**.</span><span class="sxs-lookup"><span data-stu-id="dc8eb-111">Under **Setup**, select **Human resource workflows**.</span></span>

3. <span data-ttu-id="dc8eb-112">Vyberte **Nový** a poté vyberte **Žádost o koupi a prodej pracovního volna**.</span><span class="sxs-lookup"><span data-stu-id="dc8eb-112">Select **New**, and then select **Buy and sell leave request**.</span></span> 

4. <span data-ttu-id="dc8eb-113">Když se zobrazí pole se zprávou **Otevřít tento soubor?**, vyberte **Otevřít** a přihlaste se pomocí svých přihlašovacích údajů.</span><span class="sxs-lookup"><span data-stu-id="dc8eb-113">When the **Open this file?** message box appears, select **Open** and sign in with your company credentials.</span></span>

5. <span data-ttu-id="dc8eb-114">Pomocí editoru workflowu vytvořte workflow žádosti o pracovní volno.</span><span class="sxs-lookup"><span data-stu-id="dc8eb-114">Use the workflow editor to create a workflow for your leave requests.</span></span> <span data-ttu-id="dc8eb-115">Další informace o práci s workflowy naleznete v tématu [Vytvoření přehledu workflowů](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span><span class="sxs-lookup"><span data-stu-id="dc8eb-115">For more information about working with workflows, see [Create workflows overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span></span>

## <a name="leave-and-absence-request-workflow-data-elements"></a><span data-ttu-id="dc8eb-116">Vytvoření datových prvků workflow žádosti o pracovní volno a absenci</span><span class="sxs-lookup"><span data-stu-id="dc8eb-116">Leave and absence request workflow data elements</span></span>

<span data-ttu-id="dc8eb-117">Následující datové prvky můžete použít k vytvoření podmíněných nebo automatických schválení v pracovních postupech pro žádosti o koupi a prodej pracovního volna:</span><span class="sxs-lookup"><span data-stu-id="dc8eb-117">You can use the following data elements to create conditional or automatic approvals in workflows for buy and sell leave requests:</span></span>

- <span data-ttu-id="dc8eb-118">**Částka**</span><span class="sxs-lookup"><span data-stu-id="dc8eb-118">**Amount**</span></span>
- <span data-ttu-id="dc8eb-119">**Zásady nákupu a prodeje pracovního volna**</span><span class="sxs-lookup"><span data-stu-id="dc8eb-119">**Buy and sell leave policy**</span></span>
- <span data-ttu-id="dc8eb-120">**Společnost**</span><span class="sxs-lookup"><span data-stu-id="dc8eb-120">**Company**</span></span>
- <span data-ttu-id="dc8eb-121">**Vytvořil**</span><span class="sxs-lookup"><span data-stu-id="dc8eb-121">**Created by**</span></span>
- <span data-ttu-id="dc8eb-122">**Datum a čas vytvoření**</span><span class="sxs-lookup"><span data-stu-id="dc8eb-122">**Created date and time**</span></span>
- <span data-ttu-id="dc8eb-123">**Koncové datum**</span><span class="sxs-lookup"><span data-stu-id="dc8eb-123">**End date**</span></span>
- <span data-ttu-id="dc8eb-124">**Typ pracovního volna**</span><span class="sxs-lookup"><span data-stu-id="dc8eb-124">**Leave type**</span></span>
- <span data-ttu-id="dc8eb-125">**Změnil/a**</span><span class="sxs-lookup"><span data-stu-id="dc8eb-125">**Modified by**</span></span>
- <span data-ttu-id="dc8eb-126">**Datum a čas úpravy**</span><span class="sxs-lookup"><span data-stu-id="dc8eb-126">**Modified date and time**</span></span>
- <span data-ttu-id="dc8eb-127">**ID požadavku**</span><span class="sxs-lookup"><span data-stu-id="dc8eb-127">**Request ID**</span></span>
- <span data-ttu-id="dc8eb-128">**Datum zahájení**</span><span class="sxs-lookup"><span data-stu-id="dc8eb-128">**Start date**</span></span>
- <span data-ttu-id="dc8eb-129">**Stav**</span><span class="sxs-lookup"><span data-stu-id="dc8eb-129">**Status**</span></span> 
- <span data-ttu-id="dc8eb-130">**Datum odeslání**</span><span class="sxs-lookup"><span data-stu-id="dc8eb-130">**Submission date**</span></span>
- <span data-ttu-id="dc8eb-131">**Odeslal/a**</span><span class="sxs-lookup"><span data-stu-id="dc8eb-131">**Submitted by**</span></span>
- <span data-ttu-id="dc8eb-132">**Odesláno personálním oddělením**</span><span class="sxs-lookup"><span data-stu-id="dc8eb-132">**Submitted by Human resources**</span></span>
- <span data-ttu-id="dc8eb-133">**Odesláno manažerem**</span><span class="sxs-lookup"><span data-stu-id="dc8eb-133">**Submitted by Manager**</span></span>
- <span data-ttu-id="dc8eb-134">**Zadáno jménem**</span><span class="sxs-lookup"><span data-stu-id="dc8eb-134">**Submitted on behalf**</span></span>
- <span data-ttu-id="dc8eb-135">**Pracovní podproces**</span><span class="sxs-lookup"><span data-stu-id="dc8eb-135">**Worker**</span></span>

## <a name="workflow-examples"></a><span data-ttu-id="dc8eb-136">Příklady pracovních postupů</span><span class="sxs-lookup"><span data-stu-id="dc8eb-136">Workflow examples</span></span>

<span data-ttu-id="dc8eb-137">Tyto příklady ukazují, jak lze pomocí různých datových prvků vytvořit různé typy podmínek pracovního postupu:</span><span class="sxs-lookup"><span data-stu-id="dc8eb-137">These examples show how you can create different types of workflow conditions by using these data elements:</span></span>

- <span data-ttu-id="dc8eb-138">Volby **Předloženo personálním oddělením** a **Předloženo manažerem** v automatické akci použijte k automatickému schvalování žádostí o koupi a prodej pracovního volna, které tyto role předkládají jménem zaměstnanců.</span><span class="sxs-lookup"><span data-stu-id="dc8eb-138">Use **Submitted by Human resources** and **Submitted by manager** in an automatic action to automatically approve buy and sell leave requests that these roles submit on behalf of employees.</span></span> <span data-ttu-id="dc8eb-139">Další informace o automatických akcích naleznete v tématu [Konfigurace procesů schvalování ve workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span><span class="sxs-lookup"><span data-stu-id="dc8eb-139">For more information about automatic actions, see [Configure approval processes in a workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span></span>

- <span data-ttu-id="dc8eb-140">Pomocí příkazu **Typ dovolené** v podmíněném příkazu nebo automatické akci určete, jak workflow směruje požadavky u určitých typů dovolené.</span><span class="sxs-lookup"><span data-stu-id="dc8eb-140">Use **Leave type** in a conditional statement or automatic action to control how the workflow routes requests with certain leave types.</span></span>

## <a name="see-also"></a><span data-ttu-id="dc8eb-141">Viz také</span><span class="sxs-lookup"><span data-stu-id="dc8eb-141">See also</span></span>

[<span data-ttu-id="dc8eb-142">Přehled pracovního volna a absencí</span><span class="sxs-lookup"><span data-stu-id="dc8eb-142">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)<br>
[<span data-ttu-id="dc8eb-143">Správa zásad nákupu a prodeje pracovního volna</span><span class="sxs-lookup"><span data-stu-id="dc8eb-143">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]