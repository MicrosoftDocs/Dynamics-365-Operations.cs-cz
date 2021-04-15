---
title: Odeslání žádosti o volno do workflow
description: V Microsoft Dynamics 365 Human Resources můžete pomocí rozhraní API MyLeaveRequests Submit() odeslat žádost o pracovní volno do workflowu.
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
ms.openlocfilehash: bd82bef29e5d1d33c1dc1aa3a039833741c1fdaf
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793626"
---
# <a name="submit-a-leave-request-to-workflow"></a>Odeslání žádosti o volno do workflow

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

V Microsoft Dynamics 365 Human Resources můžete pomocí rozhraní API MyLeaveRequests Submit() odeslat žádost o pracovní volno do workflowu. Toto rozhraní API je vystaveno jako akce pro entitu OData MyLeaveRequests.

## <a name="prerequisites"></a>Předpoklady

Žádost o pracovní volno musí být uložena v databázi a musí být možné ji získat prostřednictvím entity MyLeaveRequests.

## <a name="permissions"></a>Oprávnění

K volání tohoto rozhraní API jsou vyžadována některá z následujících oprávnění. Další informace o oprávněních a způsobu jejich výběru získáte v části [Ověřování](hr-developer-api-authentication.md).

| Typ oprávnění                    | Oprávnění (od nejnižšího k nejvyššímu) |
|------------------------------------|--------------------------------------------------------|
| Delegované (pracovní nebo školní účet) | uživatel\_zosobnění                                    |

## <a name="https-request"></a>Požadavek HTTPS

<!-- { "blockType": "ignored" } -->
```HTTP
POST https://{cluster}.hr.talent.dynamics.com/namespaces/{namespace_guid}/data/MyLeaveRequests(RequestId='{requestId}', LeaveType='{leaveType}', LeaveDate={leaveDate}, dataAreaId={dataArea})/Microsoft.Dynamics.DataEntities.submit?cross-company=true
```

Požadavek odpovídá standardům OData. Parametry {requestId}, {leaveType}, {leaveDate} a {dataArea} odkazují na pole, která tvoří složený přirozený klíč pro entitu MyLeaveRequests.

> [!NOTE]
> Zatímco pole pro entitu MyLeaveRequests odkazují na jednotlivé řádky žádosti o pracovní volno, volání rozhraní API pro odeslání odešle do workflowu celou žádost o pracovní volno (všechny řádky).

### <a name="request-headers"></a>Záhlaví požadavku

| Záhlaví         | Value                     |
|----------------|---------------------------|
| Autorizace  | Nosič {token} (povinný) |
| Content-Type   | žádost/json          |

### <a name="request-body"></a>Tělo žádosti

Nepřidávejte tělo požadavku pro tuto metodu.

### <a name="response"></a>Odezva

Úspěšná odpověď je vždy **204 No Content**.

Neoprávnění volající obdrží odpověď **401 Unauthorized** nebo **403 Forbidden**.

Pokud je odeslání neúspěšné (například z důvodu ověření), odpověď bude **500 Server Error** a tělo odpovědi bude obsahovat objekt JSON s dalšími podrobnostmi.

## <a name="example"></a>Příklad

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

## <a name="validation-and-error-messages"></a>Chyby ověření a chybové zprávy

Při volání rozhraní API pro odesílání provádí aplikace Human Resources ověření obchodní logiky před odesláním, což zaručuje, že žádost o pracovní volno je v platném stavu pro odeslání. Možné chybové zprávy, které se mohou zobrazit v odpovědi v případě selhání ověření:

 - Požadavek by způsobil, že zůstatek {LeaveTypeId} klesne pod povolené minimum zůstatku {date}.
 - Žádost o pracovní volno ve stavu Dokončeno nelze odeslat.
 - Žádost nelze odeslat nebo uložit, protože nebyly provedeny žádné změny. Přidejte nebo aktualizujte částku nebo typ pracovního volna a zkuste to znovu.
 - Zadaný požadavek na volno obsahuje jeden nebo více dnů se stejným datem a tento typ ponechá jako existující požadavek čekající na vyřízení. Chcete-li provést změny, vyvolejte existující žádost o provedení změn.
 - Kód důvodu {ReasonCodeId} se nevztahuje na žádný typ pracovního volna v požadavku.
 - Typ pracovního volna {LeaveTypeId} vyžaduje kód důvodu. Vyberte příslušný typ a kód důvodu.
 - Volno nebylo úspěšně odesláno. Časové volno bylo uloženo jako koncept žádosti.

## <a name="see-also"></a>Viz také

- [Přehled MyLeaveRequests](hr-developer-api-myleaverequests-overview.md)
- [Ověřování](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]