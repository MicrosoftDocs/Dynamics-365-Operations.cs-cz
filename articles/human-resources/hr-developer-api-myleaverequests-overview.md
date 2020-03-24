---
title: Přehled MyLeaveRequests
description: Entita MyLeaveRequests v Microsoft Dynamics 365 Human Resources poskytuje seznam požadavků na pracovní volno v systému (omezen) na požadavky, které jsou přístupné aktuálnímu uživateli při zadávání dotazu na entitu.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4bf3b298af9eb39e03514a4005afb43a42908e47
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092030"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="6fedb-103">Přehled MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="6fedb-103">MyLeaveRequests overview</span></span>

<span data-ttu-id="6fedb-104">Entita MyLeaveRequests v Microsoft Dynamics 365 Human Resources poskytuje seznam požadavků na pracovní volno v systému (omezen) na požadavky, které jsou přístupné aktuálnímu uživateli při zadávání dotazu na entitu.</span><span class="sxs-lookup"><span data-stu-id="6fedb-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="6fedb-105">Klíč</span><span class="sxs-lookup"><span data-stu-id="6fedb-105">Key</span></span>

  | <span data-ttu-id="6fedb-106">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="6fedb-106">Property Name</span></span> | <span data-ttu-id="6fedb-107">Datový typ</span><span class="sxs-lookup"><span data-stu-id="6fedb-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="6fedb-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="6fedb-108">dataAreaId</span></span>    | <span data-ttu-id="6fedb-109">Řetězec</span><span class="sxs-lookup"><span data-stu-id="6fedb-109">String</span></span>    |
  | <span data-ttu-id="6fedb-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="6fedb-110">RequestId</span></span>     | <span data-ttu-id="6fedb-111">Řetězec</span><span class="sxs-lookup"><span data-stu-id="6fedb-111">String</span></span>    |
  | <span data-ttu-id="6fedb-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="6fedb-112">LeaveType</span></span>     | <span data-ttu-id="6fedb-113">Řetězec</span><span class="sxs-lookup"><span data-stu-id="6fedb-113">String</span></span>    |
  | <span data-ttu-id="6fedb-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="6fedb-114">LeaveDate</span></span>     | <span data-ttu-id="6fedb-115">Datum</span><span class="sxs-lookup"><span data-stu-id="6fedb-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="6fedb-116">Vlastnosti</span><span class="sxs-lookup"><span data-stu-id="6fedb-116">Properties</span></span>

  | <span data-ttu-id="6fedb-117">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="6fedb-117">Property Name</span></span>     | <span data-ttu-id="6fedb-118">Datový typ</span><span class="sxs-lookup"><span data-stu-id="6fedb-118">Data Type</span></span> | <span data-ttu-id="6fedb-119">Povinné</span><span class="sxs-lookup"><span data-stu-id="6fedb-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="6fedb-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="6fedb-120">dataAreaId</span></span>        | <span data-ttu-id="6fedb-121">Řetězec</span><span class="sxs-lookup"><span data-stu-id="6fedb-121">String</span></span>    | <span data-ttu-id="6fedb-122">X</span><span class="sxs-lookup"><span data-stu-id="6fedb-122">X</span></span>        |
  | <span data-ttu-id="6fedb-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="6fedb-123">RequestId</span></span>         | <span data-ttu-id="6fedb-124">Řetězec</span><span class="sxs-lookup"><span data-stu-id="6fedb-124">String</span></span>    | <span data-ttu-id="6fedb-125">X</span><span class="sxs-lookup"><span data-stu-id="6fedb-125">X</span></span>        |
  | <span data-ttu-id="6fedb-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="6fedb-126">LeaveType</span></span>         | <span data-ttu-id="6fedb-127">Řetězec</span><span class="sxs-lookup"><span data-stu-id="6fedb-127">String</span></span>    | <span data-ttu-id="6fedb-128">X</span><span class="sxs-lookup"><span data-stu-id="6fedb-128">X</span></span>        |
  | <span data-ttu-id="6fedb-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="6fedb-129">LeaveDate</span></span>         | <span data-ttu-id="6fedb-130">Datum</span><span class="sxs-lookup"><span data-stu-id="6fedb-130">Date</span></span>      | <span data-ttu-id="6fedb-131">X</span><span class="sxs-lookup"><span data-stu-id="6fedb-131">X</span></span>        |
  | <span data-ttu-id="6fedb-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="6fedb-132">ReasonCodeId</span></span>      | <span data-ttu-id="6fedb-133">Řetězec</span><span class="sxs-lookup"><span data-stu-id="6fedb-133">String</span></span>    |          |
  | <span data-ttu-id="6fedb-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="6fedb-134">PersonnelNumber</span></span>   | <span data-ttu-id="6fedb-135">Řetězec</span><span class="sxs-lookup"><span data-stu-id="6fedb-135">String</span></span>    | <span data-ttu-id="6fedb-136">X</span><span class="sxs-lookup"><span data-stu-id="6fedb-136">X</span></span>        |
  | <span data-ttu-id="6fedb-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="6fedb-137">RequestDate</span></span>       | <span data-ttu-id="6fedb-138">Datum</span><span class="sxs-lookup"><span data-stu-id="6fedb-138">Date</span></span>      | <span data-ttu-id="6fedb-139">X</span><span class="sxs-lookup"><span data-stu-id="6fedb-139">X</span></span>        |
  | <span data-ttu-id="6fedb-140">Komentář</span><span class="sxs-lookup"><span data-stu-id="6fedb-140">Comment</span></span>           | <span data-ttu-id="6fedb-141">Řetězec</span><span class="sxs-lookup"><span data-stu-id="6fedb-141">String</span></span>    |          |
  | <span data-ttu-id="6fedb-142">Stav</span><span class="sxs-lookup"><span data-stu-id="6fedb-142">Status</span></span>            | <span data-ttu-id="6fedb-143">Výčet</span><span class="sxs-lookup"><span data-stu-id="6fedb-143">Enum</span></span>      | <span data-ttu-id="6fedb-144">X</span><span class="sxs-lookup"><span data-stu-id="6fedb-144">X</span></span>        |
  | <span data-ttu-id="6fedb-145">Množství</span><span class="sxs-lookup"><span data-stu-id="6fedb-145">Amount</span></span>            | <span data-ttu-id="6fedb-146">Reálný</span><span class="sxs-lookup"><span data-stu-id="6fedb-146">Real</span></span>      |          |
  | <span data-ttu-id="6fedb-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="6fedb-147">HalfDayDefinition</span></span> | <span data-ttu-id="6fedb-148">Výčet</span><span class="sxs-lookup"><span data-stu-id="6fedb-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="6fedb-149">Akce</span><span class="sxs-lookup"><span data-stu-id="6fedb-149">Actions</span></span>

 | <span data-ttu-id="6fedb-150">Název akce</span><span class="sxs-lookup"><span data-stu-id="6fedb-150">Action Name</span></span>                               | <span data-ttu-id="6fedb-151">Popis</span><span class="sxs-lookup"><span data-stu-id="6fedb-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="6fedb-152">odeslat</span><span class="sxs-lookup"><span data-stu-id="6fedb-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="6fedb-153">Odešlete požadavek ke zpracování pomocí workflowu.</span><span class="sxs-lookup"><span data-stu-id="6fedb-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="6fedb-154">Viz také</span><span class="sxs-lookup"><span data-stu-id="6fedb-154">See also</span></span>

- [<span data-ttu-id="6fedb-155">Odeslání žádosti o volno do workflow</span><span class="sxs-lookup"><span data-stu-id="6fedb-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="6fedb-156">Ověřování</span><span class="sxs-lookup"><span data-stu-id="6fedb-156">Authentication</span></span>](hr-developer-api-authentication.md)