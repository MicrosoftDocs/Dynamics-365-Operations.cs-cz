---
title: Přehled MyLeaveRequests
description: ''
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
ms.openlocfilehash: 66f161d6736b1bb544d02871d9d51b2949b1cfa0
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008351"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="847e8-102">Přehled MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="847e8-102">MyLeaveRequests overview</span></span>

<span data-ttu-id="847e8-103">Entita MyLeaveRequests v Microsoft Dynamics 365 Human Resources poskytuje seznam požadavků na pracovní volno v systému (omezen) na požadavky, které jsou přístupné aktuálnímu uživateli při zadávání dotazu na entitu.</span><span class="sxs-lookup"><span data-stu-id="847e8-103">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="847e8-104">Klíč</span><span class="sxs-lookup"><span data-stu-id="847e8-104">Key</span></span>

  | <span data-ttu-id="847e8-105">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="847e8-105">Property Name</span></span> | <span data-ttu-id="847e8-106">Datový typ</span><span class="sxs-lookup"><span data-stu-id="847e8-106">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="847e8-107">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="847e8-107">dataAreaId</span></span>    | <span data-ttu-id="847e8-108">Řetězec</span><span class="sxs-lookup"><span data-stu-id="847e8-108">String</span></span>    |
  | <span data-ttu-id="847e8-109">RequestId</span><span class="sxs-lookup"><span data-stu-id="847e8-109">RequestId</span></span>     | <span data-ttu-id="847e8-110">Řetězec</span><span class="sxs-lookup"><span data-stu-id="847e8-110">String</span></span>    |
  | <span data-ttu-id="847e8-111">LeaveType</span><span class="sxs-lookup"><span data-stu-id="847e8-111">LeaveType</span></span>     | <span data-ttu-id="847e8-112">Řetězec</span><span class="sxs-lookup"><span data-stu-id="847e8-112">String</span></span>    |
  | <span data-ttu-id="847e8-113">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="847e8-113">LeaveDate</span></span>     | <span data-ttu-id="847e8-114">Datum</span><span class="sxs-lookup"><span data-stu-id="847e8-114">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="847e8-115">Vlastnosti</span><span class="sxs-lookup"><span data-stu-id="847e8-115">Properties</span></span>

  | <span data-ttu-id="847e8-116">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="847e8-116">Property Name</span></span>     | <span data-ttu-id="847e8-117">Datový typ</span><span class="sxs-lookup"><span data-stu-id="847e8-117">Data Type</span></span> | <span data-ttu-id="847e8-118">Povinné</span><span class="sxs-lookup"><span data-stu-id="847e8-118">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="847e8-119">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="847e8-119">dataAreaId</span></span>        | <span data-ttu-id="847e8-120">Řetězec</span><span class="sxs-lookup"><span data-stu-id="847e8-120">String</span></span>    | <span data-ttu-id="847e8-121">X</span><span class="sxs-lookup"><span data-stu-id="847e8-121">X</span></span>        |
  | <span data-ttu-id="847e8-122">RequestId</span><span class="sxs-lookup"><span data-stu-id="847e8-122">RequestId</span></span>         | <span data-ttu-id="847e8-123">Řetězec</span><span class="sxs-lookup"><span data-stu-id="847e8-123">String</span></span>    | <span data-ttu-id="847e8-124">X</span><span class="sxs-lookup"><span data-stu-id="847e8-124">X</span></span>        |
  | <span data-ttu-id="847e8-125">LeaveType</span><span class="sxs-lookup"><span data-stu-id="847e8-125">LeaveType</span></span>         | <span data-ttu-id="847e8-126">Řetězec</span><span class="sxs-lookup"><span data-stu-id="847e8-126">String</span></span>    | <span data-ttu-id="847e8-127">X</span><span class="sxs-lookup"><span data-stu-id="847e8-127">X</span></span>        |
  | <span data-ttu-id="847e8-128">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="847e8-128">LeaveDate</span></span>         | <span data-ttu-id="847e8-129">Datum</span><span class="sxs-lookup"><span data-stu-id="847e8-129">Date</span></span>      | <span data-ttu-id="847e8-130">X</span><span class="sxs-lookup"><span data-stu-id="847e8-130">X</span></span>        |
  | <span data-ttu-id="847e8-131">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="847e8-131">ReasonCodeId</span></span>      | <span data-ttu-id="847e8-132">Řetězec</span><span class="sxs-lookup"><span data-stu-id="847e8-132">String</span></span>    |          |
  | <span data-ttu-id="847e8-133">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="847e8-133">PersonnelNumber</span></span>   | <span data-ttu-id="847e8-134">Řetězec</span><span class="sxs-lookup"><span data-stu-id="847e8-134">String</span></span>    | <span data-ttu-id="847e8-135">X</span><span class="sxs-lookup"><span data-stu-id="847e8-135">X</span></span>        |
  | <span data-ttu-id="847e8-136">RequestDate</span><span class="sxs-lookup"><span data-stu-id="847e8-136">RequestDate</span></span>       | <span data-ttu-id="847e8-137">Datum</span><span class="sxs-lookup"><span data-stu-id="847e8-137">Date</span></span>      | <span data-ttu-id="847e8-138">X</span><span class="sxs-lookup"><span data-stu-id="847e8-138">X</span></span>        |
  | <span data-ttu-id="847e8-139">Komentář</span><span class="sxs-lookup"><span data-stu-id="847e8-139">Comment</span></span>           | <span data-ttu-id="847e8-140">Řetězec</span><span class="sxs-lookup"><span data-stu-id="847e8-140">String</span></span>    |          |
  | <span data-ttu-id="847e8-141">Stav</span><span class="sxs-lookup"><span data-stu-id="847e8-141">Status</span></span>            | <span data-ttu-id="847e8-142">Výčet</span><span class="sxs-lookup"><span data-stu-id="847e8-142">Enum</span></span>      | <span data-ttu-id="847e8-143">X</span><span class="sxs-lookup"><span data-stu-id="847e8-143">X</span></span>        |
  | <span data-ttu-id="847e8-144">Množství</span><span class="sxs-lookup"><span data-stu-id="847e8-144">Amount</span></span>            | <span data-ttu-id="847e8-145">Reálný</span><span class="sxs-lookup"><span data-stu-id="847e8-145">Real</span></span>      |          |
  | <span data-ttu-id="847e8-146">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="847e8-146">HalfDayDefinition</span></span> | <span data-ttu-id="847e8-147">Výčet</span><span class="sxs-lookup"><span data-stu-id="847e8-147">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="847e8-148">Akce</span><span class="sxs-lookup"><span data-stu-id="847e8-148">Actions</span></span>

 | <span data-ttu-id="847e8-149">Název akce</span><span class="sxs-lookup"><span data-stu-id="847e8-149">Action Name</span></span>                               | <span data-ttu-id="847e8-150">Popis</span><span class="sxs-lookup"><span data-stu-id="847e8-150">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="847e8-151">odeslat</span><span class="sxs-lookup"><span data-stu-id="847e8-151">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="847e8-152">Odešlete požadavek ke zpracování pomocí workflowu.</span><span class="sxs-lookup"><span data-stu-id="847e8-152">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="847e8-153">Viz také</span><span class="sxs-lookup"><span data-stu-id="847e8-153">See also</span></span>

- [<span data-ttu-id="847e8-154">Odeslání žádosti o volno do workflow</span><span class="sxs-lookup"><span data-stu-id="847e8-154">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="847e8-155">Ověřování</span><span class="sxs-lookup"><span data-stu-id="847e8-155">Authentication</span></span>](hr-developer-api-authentication.md)