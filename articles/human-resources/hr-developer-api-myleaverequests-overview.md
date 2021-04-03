---
title: Přehled MyLeaveRequests
description: Entita MyLeaveRequests v Microsoft Dynamics 365 Human Resources poskytuje seznam požadavků na pracovní volno v systému (omezen) na požadavky, které jsou přístupné aktuálnímu uživateli při zadávání dotazu na entitu.
author: andreabichsel
manager: tfehr
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
ms.openlocfilehash: c2c14a0cc935ad166a2c6600f1e96c3e09ab16ca
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465503"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="a608e-103">Přehled MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="a608e-103">MyLeaveRequests overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="a608e-104">Entita MyLeaveRequests v Microsoft Dynamics 365 Human Resources poskytuje seznam požadavků na pracovní volno v systému (omezen) na požadavky, které jsou přístupné aktuálnímu uživateli při zadávání dotazu na entitu.</span><span class="sxs-lookup"><span data-stu-id="a608e-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="a608e-105">Klíč</span><span class="sxs-lookup"><span data-stu-id="a608e-105">Key</span></span>

  | <span data-ttu-id="a608e-106">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="a608e-106">Property Name</span></span> | <span data-ttu-id="a608e-107">Datový typ</span><span class="sxs-lookup"><span data-stu-id="a608e-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="a608e-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="a608e-108">dataAreaId</span></span>    | <span data-ttu-id="a608e-109">Řetězec</span><span class="sxs-lookup"><span data-stu-id="a608e-109">String</span></span>    |
  | <span data-ttu-id="a608e-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="a608e-110">RequestId</span></span>     | <span data-ttu-id="a608e-111">Řetězec</span><span class="sxs-lookup"><span data-stu-id="a608e-111">String</span></span>    |
  | <span data-ttu-id="a608e-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="a608e-112">LeaveType</span></span>     | <span data-ttu-id="a608e-113">Řetězec</span><span class="sxs-lookup"><span data-stu-id="a608e-113">String</span></span>    |
  | <span data-ttu-id="a608e-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="a608e-114">LeaveDate</span></span>     | <span data-ttu-id="a608e-115">Datum</span><span class="sxs-lookup"><span data-stu-id="a608e-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="a608e-116">Vlastnosti</span><span class="sxs-lookup"><span data-stu-id="a608e-116">Properties</span></span>

  | <span data-ttu-id="a608e-117">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="a608e-117">Property Name</span></span>     | <span data-ttu-id="a608e-118">Datový typ</span><span class="sxs-lookup"><span data-stu-id="a608e-118">Data Type</span></span> | <span data-ttu-id="a608e-119">Povinné</span><span class="sxs-lookup"><span data-stu-id="a608e-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="a608e-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="a608e-120">dataAreaId</span></span>        | <span data-ttu-id="a608e-121">Řetězec</span><span class="sxs-lookup"><span data-stu-id="a608e-121">String</span></span>    | <span data-ttu-id="a608e-122">X</span><span class="sxs-lookup"><span data-stu-id="a608e-122">X</span></span>        |
  | <span data-ttu-id="a608e-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="a608e-123">RequestId</span></span>         | <span data-ttu-id="a608e-124">Řetězec</span><span class="sxs-lookup"><span data-stu-id="a608e-124">String</span></span>    | <span data-ttu-id="a608e-125">X</span><span class="sxs-lookup"><span data-stu-id="a608e-125">X</span></span>        |
  | <span data-ttu-id="a608e-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="a608e-126">LeaveType</span></span>         | <span data-ttu-id="a608e-127">Řetězec</span><span class="sxs-lookup"><span data-stu-id="a608e-127">String</span></span>    | <span data-ttu-id="a608e-128">X</span><span class="sxs-lookup"><span data-stu-id="a608e-128">X</span></span>        |
  | <span data-ttu-id="a608e-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="a608e-129">LeaveDate</span></span>         | <span data-ttu-id="a608e-130">Datum</span><span class="sxs-lookup"><span data-stu-id="a608e-130">Date</span></span>      | <span data-ttu-id="a608e-131">X</span><span class="sxs-lookup"><span data-stu-id="a608e-131">X</span></span>        |
  | <span data-ttu-id="a608e-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="a608e-132">ReasonCodeId</span></span>      | <span data-ttu-id="a608e-133">Řetězec</span><span class="sxs-lookup"><span data-stu-id="a608e-133">String</span></span>    |          |
  | <span data-ttu-id="a608e-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="a608e-134">PersonnelNumber</span></span>   | <span data-ttu-id="a608e-135">Řetězec</span><span class="sxs-lookup"><span data-stu-id="a608e-135">String</span></span>    | <span data-ttu-id="a608e-136">X</span><span class="sxs-lookup"><span data-stu-id="a608e-136">X</span></span>        |
  | <span data-ttu-id="a608e-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="a608e-137">RequestDate</span></span>       | <span data-ttu-id="a608e-138">Datum</span><span class="sxs-lookup"><span data-stu-id="a608e-138">Date</span></span>      | <span data-ttu-id="a608e-139">X</span><span class="sxs-lookup"><span data-stu-id="a608e-139">X</span></span>        |
  | <span data-ttu-id="a608e-140">Komentář</span><span class="sxs-lookup"><span data-stu-id="a608e-140">Comment</span></span>           | <span data-ttu-id="a608e-141">Řetězec</span><span class="sxs-lookup"><span data-stu-id="a608e-141">String</span></span>    |          |
  | <span data-ttu-id="a608e-142">Stav</span><span class="sxs-lookup"><span data-stu-id="a608e-142">Status</span></span>            | <span data-ttu-id="a608e-143">Výčet</span><span class="sxs-lookup"><span data-stu-id="a608e-143">Enum</span></span>      | <span data-ttu-id="a608e-144">X</span><span class="sxs-lookup"><span data-stu-id="a608e-144">X</span></span>        |
  | <span data-ttu-id="a608e-145">Množství</span><span class="sxs-lookup"><span data-stu-id="a608e-145">Amount</span></span>            | <span data-ttu-id="a608e-146">Reálný</span><span class="sxs-lookup"><span data-stu-id="a608e-146">Real</span></span>      |          |
  | <span data-ttu-id="a608e-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="a608e-147">HalfDayDefinition</span></span> | <span data-ttu-id="a608e-148">Výčet</span><span class="sxs-lookup"><span data-stu-id="a608e-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="a608e-149">Akce</span><span class="sxs-lookup"><span data-stu-id="a608e-149">Actions</span></span>

 | <span data-ttu-id="a608e-150">Název akce</span><span class="sxs-lookup"><span data-stu-id="a608e-150">Action Name</span></span>                               | <span data-ttu-id="a608e-151">Popis</span><span class="sxs-lookup"><span data-stu-id="a608e-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="a608e-152">odeslat</span><span class="sxs-lookup"><span data-stu-id="a608e-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="a608e-153">Odešlete požadavek ke zpracování pomocí workflowu.</span><span class="sxs-lookup"><span data-stu-id="a608e-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="a608e-154">Viz také</span><span class="sxs-lookup"><span data-stu-id="a608e-154">See also</span></span>

- [<span data-ttu-id="a608e-155">Odeslání žádosti o volno do workflow</span><span class="sxs-lookup"><span data-stu-id="a608e-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="a608e-156">Ověřování</span><span class="sxs-lookup"><span data-stu-id="a608e-156">Authentication</span></span>](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]