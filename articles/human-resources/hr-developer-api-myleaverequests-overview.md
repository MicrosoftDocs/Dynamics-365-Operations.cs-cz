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
ms.openlocfilehash: 0ca5bc225400338e76faee41a279e91fc00ce570
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115529"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="069e9-103">Přehled MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="069e9-103">MyLeaveRequests overview</span></span>

<span data-ttu-id="069e9-104">Entita MyLeaveRequests v Microsoft Dynamics 365 Human Resources poskytuje seznam požadavků na pracovní volno v systému (omezen) na požadavky, které jsou přístupné aktuálnímu uživateli při zadávání dotazu na entitu.</span><span class="sxs-lookup"><span data-stu-id="069e9-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="069e9-105">Klíč</span><span class="sxs-lookup"><span data-stu-id="069e9-105">Key</span></span>

  | <span data-ttu-id="069e9-106">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="069e9-106">Property Name</span></span> | <span data-ttu-id="069e9-107">Datový typ</span><span class="sxs-lookup"><span data-stu-id="069e9-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="069e9-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="069e9-108">dataAreaId</span></span>    | <span data-ttu-id="069e9-109">Řetězec</span><span class="sxs-lookup"><span data-stu-id="069e9-109">String</span></span>    |
  | <span data-ttu-id="069e9-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="069e9-110">RequestId</span></span>     | <span data-ttu-id="069e9-111">Řetězec</span><span class="sxs-lookup"><span data-stu-id="069e9-111">String</span></span>    |
  | <span data-ttu-id="069e9-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="069e9-112">LeaveType</span></span>     | <span data-ttu-id="069e9-113">Řetězec</span><span class="sxs-lookup"><span data-stu-id="069e9-113">String</span></span>    |
  | <span data-ttu-id="069e9-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="069e9-114">LeaveDate</span></span>     | <span data-ttu-id="069e9-115">Datum</span><span class="sxs-lookup"><span data-stu-id="069e9-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="069e9-116">Vlastnosti</span><span class="sxs-lookup"><span data-stu-id="069e9-116">Properties</span></span>

  | <span data-ttu-id="069e9-117">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="069e9-117">Property Name</span></span>     | <span data-ttu-id="069e9-118">Datový typ</span><span class="sxs-lookup"><span data-stu-id="069e9-118">Data Type</span></span> | <span data-ttu-id="069e9-119">Povinné</span><span class="sxs-lookup"><span data-stu-id="069e9-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="069e9-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="069e9-120">dataAreaId</span></span>        | <span data-ttu-id="069e9-121">Řetězec</span><span class="sxs-lookup"><span data-stu-id="069e9-121">String</span></span>    | <span data-ttu-id="069e9-122">X</span><span class="sxs-lookup"><span data-stu-id="069e9-122">X</span></span>        |
  | <span data-ttu-id="069e9-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="069e9-123">RequestId</span></span>         | <span data-ttu-id="069e9-124">Řetězec</span><span class="sxs-lookup"><span data-stu-id="069e9-124">String</span></span>    | <span data-ttu-id="069e9-125">X</span><span class="sxs-lookup"><span data-stu-id="069e9-125">X</span></span>        |
  | <span data-ttu-id="069e9-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="069e9-126">LeaveType</span></span>         | <span data-ttu-id="069e9-127">Řetězec</span><span class="sxs-lookup"><span data-stu-id="069e9-127">String</span></span>    | <span data-ttu-id="069e9-128">X</span><span class="sxs-lookup"><span data-stu-id="069e9-128">X</span></span>        |
  | <span data-ttu-id="069e9-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="069e9-129">LeaveDate</span></span>         | <span data-ttu-id="069e9-130">Datum</span><span class="sxs-lookup"><span data-stu-id="069e9-130">Date</span></span>      | <span data-ttu-id="069e9-131">X</span><span class="sxs-lookup"><span data-stu-id="069e9-131">X</span></span>        |
  | <span data-ttu-id="069e9-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="069e9-132">ReasonCodeId</span></span>      | <span data-ttu-id="069e9-133">Řetězec</span><span class="sxs-lookup"><span data-stu-id="069e9-133">String</span></span>    |          |
  | <span data-ttu-id="069e9-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="069e9-134">PersonnelNumber</span></span>   | <span data-ttu-id="069e9-135">Řetězec</span><span class="sxs-lookup"><span data-stu-id="069e9-135">String</span></span>    | <span data-ttu-id="069e9-136">X</span><span class="sxs-lookup"><span data-stu-id="069e9-136">X</span></span>        |
  | <span data-ttu-id="069e9-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="069e9-137">RequestDate</span></span>       | <span data-ttu-id="069e9-138">Datum</span><span class="sxs-lookup"><span data-stu-id="069e9-138">Date</span></span>      | <span data-ttu-id="069e9-139">X</span><span class="sxs-lookup"><span data-stu-id="069e9-139">X</span></span>        |
  | <span data-ttu-id="069e9-140">Komentář</span><span class="sxs-lookup"><span data-stu-id="069e9-140">Comment</span></span>           | <span data-ttu-id="069e9-141">Řetězec</span><span class="sxs-lookup"><span data-stu-id="069e9-141">String</span></span>    |          |
  | <span data-ttu-id="069e9-142">Stav</span><span class="sxs-lookup"><span data-stu-id="069e9-142">Status</span></span>            | <span data-ttu-id="069e9-143">Výčet</span><span class="sxs-lookup"><span data-stu-id="069e9-143">Enum</span></span>      | <span data-ttu-id="069e9-144">X</span><span class="sxs-lookup"><span data-stu-id="069e9-144">X</span></span>        |
  | <span data-ttu-id="069e9-145">Množství</span><span class="sxs-lookup"><span data-stu-id="069e9-145">Amount</span></span>            | <span data-ttu-id="069e9-146">Reálný</span><span class="sxs-lookup"><span data-stu-id="069e9-146">Real</span></span>      |          |
  | <span data-ttu-id="069e9-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="069e9-147">HalfDayDefinition</span></span> | <span data-ttu-id="069e9-148">Výčet</span><span class="sxs-lookup"><span data-stu-id="069e9-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="069e9-149">Akce</span><span class="sxs-lookup"><span data-stu-id="069e9-149">Actions</span></span>

 | <span data-ttu-id="069e9-150">Název akce</span><span class="sxs-lookup"><span data-stu-id="069e9-150">Action Name</span></span>                               | <span data-ttu-id="069e9-151">Popis</span><span class="sxs-lookup"><span data-stu-id="069e9-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="069e9-152">odeslat</span><span class="sxs-lookup"><span data-stu-id="069e9-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="069e9-153">Odešlete požadavek ke zpracování pomocí workflowu.</span><span class="sxs-lookup"><span data-stu-id="069e9-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="069e9-154">Viz také</span><span class="sxs-lookup"><span data-stu-id="069e9-154">See also</span></span>

- [<span data-ttu-id="069e9-155">Odeslání žádosti o volno do workflow</span><span class="sxs-lookup"><span data-stu-id="069e9-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="069e9-156">Ověřování</span><span class="sxs-lookup"><span data-stu-id="069e9-156">Authentication</span></span>](hr-developer-api-authentication.md)