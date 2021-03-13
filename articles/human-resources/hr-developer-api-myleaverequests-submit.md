---
title: Odeslání žádosti o volno do workflow
description: V Microsoft Dynamics 365 Human Resources můžete pomocí rozhraní API MyLeaveRequests Submit() odeslat žádost o pracovní volno do workflowu.
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
ms.openlocfilehash: 51be70edbe1439340377fd01b9760d49d3a75348
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115505"
---
# <a name="submit-a-leave-request-to-workflow"></a><span data-ttu-id="d2c8c-103">Odeslání žádosti o volno do workflow</span><span class="sxs-lookup"><span data-stu-id="d2c8c-103">Submit a leave request to workflow</span></span>

<span data-ttu-id="d2c8c-104">V Microsoft Dynamics 365 Human Resources můžete pomocí rozhraní API MyLeaveRequests Submit() odeslat žádost o pracovní volno do workflowu.</span><span class="sxs-lookup"><span data-stu-id="d2c8c-104">In Microsoft Dynamics 365 Human Resources, you can use the MyLeaveRequests submit() application programming interface (API) to submit a leave request to workflow.</span></span> <span data-ttu-id="d2c8c-105">Toto rozhraní API je vystaveno jako akce pro entitu OData MyLeaveRequests.</span><span class="sxs-lookup"><span data-stu-id="d2c8c-105">This API is exposed as an action on the MyLeaveRequests OData entity.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d2c8c-106">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="d2c8c-106">Prerequisites</span></span>

<span data-ttu-id="d2c8c-107">Žádost o pracovní volno musí být uložena v databázi a musí být možné ji získat prostřednictvím entity MyLeaveRequests.</span><span class="sxs-lookup"><span data-stu-id="d2c8c-107">The leave request must be saved in the database and must be retrievable through the MyLeaveRequests entity.</span></span>

## <a name="permissions"></a><span data-ttu-id="d2c8c-108">Oprávnění</span><span class="sxs-lookup"><span data-stu-id="d2c8c-108">Permissions</span></span>

<span data-ttu-id="d2c8c-109">K volání tohoto rozhraní API jsou vyžadována některá z následujících oprávnění.</span><span class="sxs-lookup"><span data-stu-id="d2c8c-109">One of the following permissions is required to call this API.</span></span> <span data-ttu-id="d2c8c-110">Další informace o oprávněních a způsobu jejich výběru získáte v části [Ověřování](hr-developer-api-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="d2c8c-110">For more information about permissions and how to select them, see [Authentication](hr-developer-api-authentication.md).</span></span>

| <span data-ttu-id="d2c8c-111">Typ oprávnění</span><span class="sxs-lookup"><span data-stu-id="d2c8c-111">Permission type</span></span>                    | <span data-ttu-id="d2c8c-112">Oprávnění (od nejnižšího k nejvyššímu)</span><span class="sxs-lookup"><span data-stu-id="d2c8c-112">Permissions (from least privileged to most privileged)</span></span> |
|------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="d2c8c-113">Delegované (pracovní nebo školní účet)</span><span class="sxs-lookup"><span data-stu-id="d2c8c-113">Delegated (work or school account)</span></span> | <span data-ttu-id="d2c8c-114">uživatel\_zosobnění</span><span class="sxs-lookup"><span data-stu-id="d2c8c-114">user\_impersonation</span></span>                                    |

## <a name="https-request"></a><span data-ttu-id="d2c8c-115">Požadavek HTTPS</span><span class="sxs-lookup"><span data-stu-id="d2c8c-115">HTTPS request</span></span>

<!-- { "blockType": "ignored" } -->
```HTTP
POST https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/MyLeaveRequests(RequestId='{requestId}', LeaveType='{leaveType}', LeaveDate={leaveDate}, dataAreaId={dataArea})/Microsoft.Dynamics.DataEntities.submit?cross-company=true
```

<span data-ttu-id="d2c8c-116">Požadavek odpovídá standardům OData.</span><span class="sxs-lookup"><span data-stu-id="d2c8c-116">The request conforms to OData standards.</span></span> <span data-ttu-id="d2c8c-117">Parametry {requestId}, {leaveType}, {leaveDate} a {dataArea} odkazují na pole, která tvoří složený přirozený klíč pro entitu MyLeaveRequests.</span><span class="sxs-lookup"><span data-stu-id="d2c8c-117">The {requestId}, {leaveType}, {leaveDate}, and {dataArea} parameters refer to the fields that make up the composite natural key for the MyLeaveRequests entity.</span></span>

> [!NOTE]
> <span data-ttu-id="d2c8c-118">Zatímco pole pro entitu MyLeaveRequests odkazují na jednotlivé řádky žádosti o pracovní volno, volání rozhraní API pro odeslání odešle do workflowu celou žádost o pracovní volno (všechny řádky).</span><span class="sxs-lookup"><span data-stu-id="d2c8c-118">While the fields for the MyLeaveRequests entity refer to an individual line in the leave request, calling the submit API will submit the entire leave request (all lines) to workflow.</span></span>

### <a name="request-headers"></a><span data-ttu-id="d2c8c-119">Záhlaví požadavku</span><span class="sxs-lookup"><span data-stu-id="d2c8c-119">Request headers</span></span>

| <span data-ttu-id="d2c8c-120">Záhlaví</span><span class="sxs-lookup"><span data-stu-id="d2c8c-120">Header</span></span>         | <span data-ttu-id="d2c8c-121">Value</span><span class="sxs-lookup"><span data-stu-id="d2c8c-121">Value</span></span>                     |
|----------------|---------------------------|
| <span data-ttu-id="d2c8c-122">Autorizace</span><span class="sxs-lookup"><span data-stu-id="d2c8c-122">Authorization</span></span>  | <span data-ttu-id="d2c8c-123">Nosič {token} (povinný)</span><span class="sxs-lookup"><span data-stu-id="d2c8c-123">Bearer {token} (required)</span></span> |
| <span data-ttu-id="d2c8c-124">Content-Type</span><span class="sxs-lookup"><span data-stu-id="d2c8c-124">Content-Type</span></span>   | <span data-ttu-id="d2c8c-125">žádost/json</span><span class="sxs-lookup"><span data-stu-id="d2c8c-125">application/json</span></span>          |

### <a name="request-body"></a><span data-ttu-id="d2c8c-126">Tělo žádosti</span><span class="sxs-lookup"><span data-stu-id="d2c8c-126">Request body</span></span>

<span data-ttu-id="d2c8c-127">Nepřidávejte tělo požadavku pro tuto metodu.</span><span class="sxs-lookup"><span data-stu-id="d2c8c-127">Don't supply a request body for this method.</span></span>

### <a name="response"></a><span data-ttu-id="d2c8c-128">Odezva</span><span class="sxs-lookup"><span data-stu-id="d2c8c-128">Response</span></span>

<span data-ttu-id="d2c8c-129">Úspěšná odpověď je vždy **204 No Content**.</span><span class="sxs-lookup"><span data-stu-id="d2c8c-129">A successful response is always a **204 No Content** response.</span></span>

<span data-ttu-id="d2c8c-130">Neoprávnění volající obdrží odpověď **401 Unauthorized** nebo **403 Forbidden**.</span><span class="sxs-lookup"><span data-stu-id="d2c8c-130">Unauthorized callers will receive a **401 Unauthorized** or a **403 Forbidden** response.</span></span>

<span data-ttu-id="d2c8c-131">Pokud je odeslání neúspěšné (například z důvodu ověření), odpověď bude **500 Server Error** a tělo odpovědi bude obsahovat objekt JSON s dalšími podrobnostmi.</span><span class="sxs-lookup"><span data-stu-id="d2c8c-131">If submission is unsuccessful (because of validation, for example), the response will be a **500 Server Error**, and the response body will include a JSON object with further details.</span></span>

## <a name="example"></a><span data-ttu-id="d2c8c-132">Příklad</span><span class="sxs-lookup"><span data-stu-id="d2c8c-132">Example</span></span>

```http
POST https://aos-rts-sf-550e5c091f6-prod-westus2.hr.talent.dynamics.com/namespaces/b2eb8003-334f-4a84-ab63-edbe23569090/data/MyLeaveRequests(RequestId='USMF-000065', LeaveType='Vacation', LeaveDate=2019-10-04T12:00:00Z, dataAreaId='USMF')/Microsoft.Dynamics.DataEntities.submit
```

```json
{
  "error": {
    "code": "",
    "message": "An error has occurred.",
    "innererror": {
      "message": "Exception occurred while executing action submit on Entity MyLeaveRequest: The request would put the 'Vacation' balance below the allowed minimum balance on 9/10/2019.",
      "type": "System.InvalidOperationException",
      "stacktrace": "   at Microsoft.Dynamics.Platform.Integration.Services.OData.Action.ActionInvokable.Invoke()   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateProcessor.ActionInvocation(ChangeOperationContext context, ActionInvokable action)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateManager.<>c__DisplayClass13_0.<ScheduleInvokable>b__0(ChangeOperationContext context)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.ChangeInfo.ExecuteActionsInCompanyContext(IEnumerable`1 actionList, ChangeOperationContext operationContext)\r\n   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.ChangeInfo.ExecuteActions(ChangeOperationContext context)   at Microsoft.Dynamics.Platform.Integration.Services.OData.Update.UpdateManager.SaveChanges()   at Microsoft.Dynamics.Platform.Integration.Services.OData.AxODataDelegatingHandler.<SaveChangesAsync>d__3.MoveNext()"
    }
  }
}
```

## <a name="validation-and-error-messages"></a><span data-ttu-id="d2c8c-133">Chyby ověření a chybové zprávy</span><span class="sxs-lookup"><span data-stu-id="d2c8c-133">Validation and error messages</span></span>

<span data-ttu-id="d2c8c-134">Při volání rozhraní API pro odesílání provádí aplikace Human Resources ověření obchodní logiky před odesláním, což zaručuje, že žádost o pracovní volno je v platném stavu pro odeslání.</span><span class="sxs-lookup"><span data-stu-id="d2c8c-134">As part of the call to the submit API, Human Resources performs business logic validation before submission, which ensures the leave request is in a valid state for submission.</span></span> <span data-ttu-id="d2c8c-135">Možné chybové zprávy, které se mohou zobrazit v odpovědi v případě selhání ověření:</span><span class="sxs-lookup"><span data-stu-id="d2c8c-135">The possible error messages you may receive in the response if validations fail are:</span></span>

 - <span data-ttu-id="d2c8c-136">Požadavek by způsobil, že zůstatek {LeaveTypeId} klesne pod povolené minimum zůstatku {date}.</span><span class="sxs-lookup"><span data-stu-id="d2c8c-136">The request would put the '{LeaveTypeId}' balance below the allowed minimum balance on {date}.</span></span>
 - <span data-ttu-id="d2c8c-137">Žádost o pracovní volno ve stavu Dokončeno nelze odeslat.</span><span class="sxs-lookup"><span data-stu-id="d2c8c-137">Time off request in Completed state cannot be submitted.</span></span>
 - <span data-ttu-id="d2c8c-138">Žádost nelze odeslat nebo uložit, protože nebyly provedeny žádné změny.</span><span class="sxs-lookup"><span data-stu-id="d2c8c-138">Unable to submit or save request as no changes have been made.</span></span> <span data-ttu-id="d2c8c-139">Přidejte nebo aktualizujte částku nebo typ pracovního volna a zkuste to znovu.</span><span class="sxs-lookup"><span data-stu-id="d2c8c-139">Add or update the amount or the leave type and try again.</span></span>
 - <span data-ttu-id="d2c8c-140">Zadaný požadavek na volno obsahuje jeden nebo více dnů se stejným datem a tento typ ponechá jako existující požadavek čekající na vyřízení.</span><span class="sxs-lookup"><span data-stu-id="d2c8c-140">The time off request entered contains one or more days with the same date and leave type as an existing pending request.</span></span> <span data-ttu-id="d2c8c-141">Chcete-li provést změny, vyvolejte existující žádost o provedení změn.</span><span class="sxs-lookup"><span data-stu-id="d2c8c-141">Please recall the existing request to make changes.</span></span>
 - <span data-ttu-id="d2c8c-142">Kód důvodu {ReasonCodeId} se nevztahuje na žádný typ pracovního volna v požadavku.</span><span class="sxs-lookup"><span data-stu-id="d2c8c-142">Reason code '{ReasonCodeId}' doesn't apply to any of the leave types in the request.</span></span>
 - <span data-ttu-id="d2c8c-143">Typ pracovního volna {LeaveTypeId} vyžaduje kód důvodu.</span><span class="sxs-lookup"><span data-stu-id="d2c8c-143">Leave type '{LeaveTypeId}' requires a reason code.</span></span> <span data-ttu-id="d2c8c-144">Vyberte příslušný typ a kód důvodu.</span><span class="sxs-lookup"><span data-stu-id="d2c8c-144">Select the appropriate type and reason code.</span></span>
 - <span data-ttu-id="d2c8c-145">Volno nebylo úspěšně odesláno.</span><span class="sxs-lookup"><span data-stu-id="d2c8c-145">The time off was not submitted successfully.</span></span> <span data-ttu-id="d2c8c-146">Časové volno bylo uloženo jako koncept žádosti.</span><span class="sxs-lookup"><span data-stu-id="d2c8c-146">The time off has been saved as a draft request.</span></span>

## <a name="see-also"></a><span data-ttu-id="d2c8c-147">Viz také</span><span class="sxs-lookup"><span data-stu-id="d2c8c-147">See also</span></span>

- [<span data-ttu-id="d2c8c-148">Přehled MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="d2c8c-148">MyLeaveRequests overview</span></span>](hr-developer-api-myleaverequests-overview.md)
- [<span data-ttu-id="d2c8c-149">Ověřování</span><span class="sxs-lookup"><span data-stu-id="d2c8c-149">Authentication</span></span>](hr-developer-api-authentication.md)