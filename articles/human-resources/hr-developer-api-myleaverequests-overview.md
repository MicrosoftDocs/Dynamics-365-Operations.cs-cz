---
title: Přehled MyLeaveRequests
description: Entita MyLeaveRequests v Microsoft Dynamics 365 Human Resources poskytuje seznam požadavků na pracovní volno v systému (omezen) na požadavky, které jsou přístupné aktuálnímu uživateli při zadávání dotazu na entitu.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f29d5cf1469b58b4ea1837dc82b9513f5c002609
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054949"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="ce4fd-103">Přehled MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="ce4fd-103">MyLeaveRequests overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="ce4fd-104">Entita MyLeaveRequests v Microsoft Dynamics 365 Human Resources poskytuje seznam požadavků na pracovní volno v systému (omezen) na požadavky, které jsou přístupné aktuálnímu uživateli při zadávání dotazu na entitu.</span><span class="sxs-lookup"><span data-stu-id="ce4fd-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="ce4fd-105">Klíč</span><span class="sxs-lookup"><span data-stu-id="ce4fd-105">Key</span></span>

  | <span data-ttu-id="ce4fd-106">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="ce4fd-106">Property Name</span></span> | <span data-ttu-id="ce4fd-107">Datový typ</span><span class="sxs-lookup"><span data-stu-id="ce4fd-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="ce4fd-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="ce4fd-108">dataAreaId</span></span>    | <span data-ttu-id="ce4fd-109">Řetězec</span><span class="sxs-lookup"><span data-stu-id="ce4fd-109">String</span></span>    |
  | <span data-ttu-id="ce4fd-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="ce4fd-110">RequestId</span></span>     | <span data-ttu-id="ce4fd-111">Řetězec</span><span class="sxs-lookup"><span data-stu-id="ce4fd-111">String</span></span>    |
  | <span data-ttu-id="ce4fd-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="ce4fd-112">LeaveType</span></span>     | <span data-ttu-id="ce4fd-113">Řetězec</span><span class="sxs-lookup"><span data-stu-id="ce4fd-113">String</span></span>    |
  | <span data-ttu-id="ce4fd-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="ce4fd-114">LeaveDate</span></span>     | <span data-ttu-id="ce4fd-115">Datum</span><span class="sxs-lookup"><span data-stu-id="ce4fd-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="ce4fd-116">Vlastnosti</span><span class="sxs-lookup"><span data-stu-id="ce4fd-116">Properties</span></span>

  | <span data-ttu-id="ce4fd-117">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="ce4fd-117">Property Name</span></span>     | <span data-ttu-id="ce4fd-118">Datový typ</span><span class="sxs-lookup"><span data-stu-id="ce4fd-118">Data Type</span></span> | <span data-ttu-id="ce4fd-119">Povinné</span><span class="sxs-lookup"><span data-stu-id="ce4fd-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="ce4fd-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="ce4fd-120">dataAreaId</span></span>        | <span data-ttu-id="ce4fd-121">Řetězec</span><span class="sxs-lookup"><span data-stu-id="ce4fd-121">String</span></span>    | <span data-ttu-id="ce4fd-122">X</span><span class="sxs-lookup"><span data-stu-id="ce4fd-122">X</span></span>        |
  | <span data-ttu-id="ce4fd-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="ce4fd-123">RequestId</span></span>         | <span data-ttu-id="ce4fd-124">Řetězec</span><span class="sxs-lookup"><span data-stu-id="ce4fd-124">String</span></span>    | <span data-ttu-id="ce4fd-125">X</span><span class="sxs-lookup"><span data-stu-id="ce4fd-125">X</span></span>        |
  | <span data-ttu-id="ce4fd-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="ce4fd-126">LeaveType</span></span>         | <span data-ttu-id="ce4fd-127">Řetězec</span><span class="sxs-lookup"><span data-stu-id="ce4fd-127">String</span></span>    | <span data-ttu-id="ce4fd-128">X</span><span class="sxs-lookup"><span data-stu-id="ce4fd-128">X</span></span>        |
  | <span data-ttu-id="ce4fd-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="ce4fd-129">LeaveDate</span></span>         | <span data-ttu-id="ce4fd-130">Datum</span><span class="sxs-lookup"><span data-stu-id="ce4fd-130">Date</span></span>      | <span data-ttu-id="ce4fd-131">X</span><span class="sxs-lookup"><span data-stu-id="ce4fd-131">X</span></span>        |
  | <span data-ttu-id="ce4fd-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="ce4fd-132">ReasonCodeId</span></span>      | <span data-ttu-id="ce4fd-133">Řetězec</span><span class="sxs-lookup"><span data-stu-id="ce4fd-133">String</span></span>    |          |
  | <span data-ttu-id="ce4fd-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="ce4fd-134">PersonnelNumber</span></span>   | <span data-ttu-id="ce4fd-135">Řetězec</span><span class="sxs-lookup"><span data-stu-id="ce4fd-135">String</span></span>    | <span data-ttu-id="ce4fd-136">X</span><span class="sxs-lookup"><span data-stu-id="ce4fd-136">X</span></span>        |
  | <span data-ttu-id="ce4fd-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="ce4fd-137">RequestDate</span></span>       | <span data-ttu-id="ce4fd-138">Datum</span><span class="sxs-lookup"><span data-stu-id="ce4fd-138">Date</span></span>      | <span data-ttu-id="ce4fd-139">X</span><span class="sxs-lookup"><span data-stu-id="ce4fd-139">X</span></span>        |
  | <span data-ttu-id="ce4fd-140">Komentář</span><span class="sxs-lookup"><span data-stu-id="ce4fd-140">Comment</span></span>           | <span data-ttu-id="ce4fd-141">Řetězec</span><span class="sxs-lookup"><span data-stu-id="ce4fd-141">String</span></span>    |          |
  | <span data-ttu-id="ce4fd-142">Stav</span><span class="sxs-lookup"><span data-stu-id="ce4fd-142">Status</span></span>            | <span data-ttu-id="ce4fd-143">Výčet</span><span class="sxs-lookup"><span data-stu-id="ce4fd-143">Enum</span></span>      | <span data-ttu-id="ce4fd-144">X</span><span class="sxs-lookup"><span data-stu-id="ce4fd-144">X</span></span>        |
  | <span data-ttu-id="ce4fd-145">Množství</span><span class="sxs-lookup"><span data-stu-id="ce4fd-145">Amount</span></span>            | <span data-ttu-id="ce4fd-146">Reálný</span><span class="sxs-lookup"><span data-stu-id="ce4fd-146">Real</span></span>      |          |
  | <span data-ttu-id="ce4fd-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="ce4fd-147">HalfDayDefinition</span></span> | <span data-ttu-id="ce4fd-148">Výčet</span><span class="sxs-lookup"><span data-stu-id="ce4fd-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="ce4fd-149">Akce</span><span class="sxs-lookup"><span data-stu-id="ce4fd-149">Actions</span></span>

 | <span data-ttu-id="ce4fd-150">Název akce</span><span class="sxs-lookup"><span data-stu-id="ce4fd-150">Action Name</span></span>                               | <span data-ttu-id="ce4fd-151">Popis</span><span class="sxs-lookup"><span data-stu-id="ce4fd-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="ce4fd-152">odeslat</span><span class="sxs-lookup"><span data-stu-id="ce4fd-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="ce4fd-153">Odešlete požadavek ke zpracování pomocí workflowu.</span><span class="sxs-lookup"><span data-stu-id="ce4fd-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="ce4fd-154">Viz také</span><span class="sxs-lookup"><span data-stu-id="ce4fd-154">See also</span></span>

- [<span data-ttu-id="ce4fd-155">Odeslání žádosti o volno do workflow</span><span class="sxs-lookup"><span data-stu-id="ce4fd-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="ce4fd-156">Ověřování</span><span class="sxs-lookup"><span data-stu-id="ce4fd-156">Authentication</span></span>](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]