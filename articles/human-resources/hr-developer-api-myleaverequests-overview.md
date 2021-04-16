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
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 44e23a076733bac782a0366aeba3456911522abe
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803626"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="8a61c-103">Přehled MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="8a61c-103">MyLeaveRequests overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="8a61c-104">Entita MyLeaveRequests v Microsoft Dynamics 365 Human Resources poskytuje seznam požadavků na pracovní volno v systému (omezen) na požadavky, které jsou přístupné aktuálnímu uživateli při zadávání dotazu na entitu.</span><span class="sxs-lookup"><span data-stu-id="8a61c-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="8a61c-105">Klíč</span><span class="sxs-lookup"><span data-stu-id="8a61c-105">Key</span></span>

  | <span data-ttu-id="8a61c-106">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="8a61c-106">Property Name</span></span> | <span data-ttu-id="8a61c-107">Datový typ</span><span class="sxs-lookup"><span data-stu-id="8a61c-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="8a61c-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="8a61c-108">dataAreaId</span></span>    | <span data-ttu-id="8a61c-109">Řetězec</span><span class="sxs-lookup"><span data-stu-id="8a61c-109">String</span></span>    |
  | <span data-ttu-id="8a61c-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="8a61c-110">RequestId</span></span>     | <span data-ttu-id="8a61c-111">Řetězec</span><span class="sxs-lookup"><span data-stu-id="8a61c-111">String</span></span>    |
  | <span data-ttu-id="8a61c-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="8a61c-112">LeaveType</span></span>     | <span data-ttu-id="8a61c-113">Řetězec</span><span class="sxs-lookup"><span data-stu-id="8a61c-113">String</span></span>    |
  | <span data-ttu-id="8a61c-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="8a61c-114">LeaveDate</span></span>     | <span data-ttu-id="8a61c-115">Datum</span><span class="sxs-lookup"><span data-stu-id="8a61c-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="8a61c-116">Vlastnosti</span><span class="sxs-lookup"><span data-stu-id="8a61c-116">Properties</span></span>

  | <span data-ttu-id="8a61c-117">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="8a61c-117">Property Name</span></span>     | <span data-ttu-id="8a61c-118">Datový typ</span><span class="sxs-lookup"><span data-stu-id="8a61c-118">Data Type</span></span> | <span data-ttu-id="8a61c-119">Povinné</span><span class="sxs-lookup"><span data-stu-id="8a61c-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="8a61c-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="8a61c-120">dataAreaId</span></span>        | <span data-ttu-id="8a61c-121">Řetězec</span><span class="sxs-lookup"><span data-stu-id="8a61c-121">String</span></span>    | <span data-ttu-id="8a61c-122">X</span><span class="sxs-lookup"><span data-stu-id="8a61c-122">X</span></span>        |
  | <span data-ttu-id="8a61c-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="8a61c-123">RequestId</span></span>         | <span data-ttu-id="8a61c-124">Řetězec</span><span class="sxs-lookup"><span data-stu-id="8a61c-124">String</span></span>    | <span data-ttu-id="8a61c-125">X</span><span class="sxs-lookup"><span data-stu-id="8a61c-125">X</span></span>        |
  | <span data-ttu-id="8a61c-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="8a61c-126">LeaveType</span></span>         | <span data-ttu-id="8a61c-127">Řetězec</span><span class="sxs-lookup"><span data-stu-id="8a61c-127">String</span></span>    | <span data-ttu-id="8a61c-128">X</span><span class="sxs-lookup"><span data-stu-id="8a61c-128">X</span></span>        |
  | <span data-ttu-id="8a61c-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="8a61c-129">LeaveDate</span></span>         | <span data-ttu-id="8a61c-130">Datum</span><span class="sxs-lookup"><span data-stu-id="8a61c-130">Date</span></span>      | <span data-ttu-id="8a61c-131">X</span><span class="sxs-lookup"><span data-stu-id="8a61c-131">X</span></span>        |
  | <span data-ttu-id="8a61c-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="8a61c-132">ReasonCodeId</span></span>      | <span data-ttu-id="8a61c-133">Řetězec</span><span class="sxs-lookup"><span data-stu-id="8a61c-133">String</span></span>    |          |
  | <span data-ttu-id="8a61c-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="8a61c-134">PersonnelNumber</span></span>   | <span data-ttu-id="8a61c-135">Řetězec</span><span class="sxs-lookup"><span data-stu-id="8a61c-135">String</span></span>    | <span data-ttu-id="8a61c-136">X</span><span class="sxs-lookup"><span data-stu-id="8a61c-136">X</span></span>        |
  | <span data-ttu-id="8a61c-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="8a61c-137">RequestDate</span></span>       | <span data-ttu-id="8a61c-138">Datum</span><span class="sxs-lookup"><span data-stu-id="8a61c-138">Date</span></span>      | <span data-ttu-id="8a61c-139">X</span><span class="sxs-lookup"><span data-stu-id="8a61c-139">X</span></span>        |
  | <span data-ttu-id="8a61c-140">Komentář</span><span class="sxs-lookup"><span data-stu-id="8a61c-140">Comment</span></span>           | <span data-ttu-id="8a61c-141">Řetězec</span><span class="sxs-lookup"><span data-stu-id="8a61c-141">String</span></span>    |          |
  | <span data-ttu-id="8a61c-142">Stav</span><span class="sxs-lookup"><span data-stu-id="8a61c-142">Status</span></span>            | <span data-ttu-id="8a61c-143">Výčet</span><span class="sxs-lookup"><span data-stu-id="8a61c-143">Enum</span></span>      | <span data-ttu-id="8a61c-144">X</span><span class="sxs-lookup"><span data-stu-id="8a61c-144">X</span></span>        |
  | <span data-ttu-id="8a61c-145">Množství</span><span class="sxs-lookup"><span data-stu-id="8a61c-145">Amount</span></span>            | <span data-ttu-id="8a61c-146">Reálný</span><span class="sxs-lookup"><span data-stu-id="8a61c-146">Real</span></span>      |          |
  | <span data-ttu-id="8a61c-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="8a61c-147">HalfDayDefinition</span></span> | <span data-ttu-id="8a61c-148">Výčet</span><span class="sxs-lookup"><span data-stu-id="8a61c-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="8a61c-149">Akce</span><span class="sxs-lookup"><span data-stu-id="8a61c-149">Actions</span></span>

 | <span data-ttu-id="8a61c-150">Název akce</span><span class="sxs-lookup"><span data-stu-id="8a61c-150">Action Name</span></span>                               | <span data-ttu-id="8a61c-151">Popis</span><span class="sxs-lookup"><span data-stu-id="8a61c-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="8a61c-152">odeslat</span><span class="sxs-lookup"><span data-stu-id="8a61c-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="8a61c-153">Odešlete požadavek ke zpracování pomocí workflowu.</span><span class="sxs-lookup"><span data-stu-id="8a61c-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="8a61c-154">Viz také</span><span class="sxs-lookup"><span data-stu-id="8a61c-154">See also</span></span>

- [<span data-ttu-id="8a61c-155">Odeslání žádosti o volno do workflow</span><span class="sxs-lookup"><span data-stu-id="8a61c-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="8a61c-156">Ověřování</span><span class="sxs-lookup"><span data-stu-id="8a61c-156">Authentication</span></span>](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]