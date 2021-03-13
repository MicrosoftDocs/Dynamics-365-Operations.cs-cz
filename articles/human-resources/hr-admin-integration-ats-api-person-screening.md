---
title: Prověřování osoby
description: Toto téma popisuje entitu Prověřování osoby pro Dynamics 365 Human Resources.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d76bb57d85ee16f4faa0bb9cfec77047feb7df5f
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125370"
---
# <a name="person-screening"></a>Prověřování osoby

Toto téma popisuje entitu Prověřování osoby pro Dynamics 365 Human Resources.

Fyzický název: mshr_hcmpersonscreeningentity

## <a name="description"></a>popis

Tato entita popisuje prověřování, která kandidát úspěšně absolvoval nebo musí absolvovat kvůli zaměstnání.

## <a name="json-representation"></a>Kód JSON

```json
{
    "mshr_note": "String",
    "mshr_requiredby": "Date",
    "mshr_status": Int,
    "mshr_partynumber": "String",
    "mshr_screeningtypeid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonscreeningentityid": "Guid",
    "mshr_completeddate": "Date"
}
```

## <a name="properties"></a>Vlastnosti

| Vlastnost<br>**Fyzický název**<br>**_Typ_** | Použít | popis |
| --- | --- | --- |
| **ID entity Prověřování osoby**<br>mshr_hcmpersonscreeningentityid<br>*GUID* | Jen pro čtení<br>Povinná<br>Generováno systémem | Jedinečný primární identifikátor pro záznam prověřování osoby. |
| **Číslo strany**<br>mshr_partynumber<br>*Řetězec* | Čtení/zápis<br>Povinná | Číslo strany (osoby) přidružené ke kandidátovi. |
| **Hodnota ID osoby**<br>_mshr_fk_person_id_value<br>*GUID* | Jen pro čtení<br>Povinná<br>Cizí klíč: mshr_dirpersonentityid entity mshr_dirpersonentity | Systémem generovaný jedinečný identifikátor záznamu entity strany (osoby). |
| **ID typu prověřování**<br>mshr_screeningtypeid<br>*Řetězec* | Čtení/zápis<br>Povinná<br>Cizí klíč: ScreeningType | Identifikátor typu prověřování definovaného v Human Resources. |
| **Hodnota ID typu prověřování**<br>_mshr_fk_screeningtype_id_value<br>*GUID* | Jen pro čtení<br>Povinná<br>Cizí klíč: mshr_hcmscreeningtypeentityid entity mshr_hcmscreeningtypeentity | Systémem generovaný identifikátor záznamu typu prověřování přidružené entity. |
| **Požadováno do**<br>mshr_requiredby<br>*Datum a čas* | Čtení/zápis<br>Volitelné | Datum, do kterého je nutné provést prověřování. |
| **Stav**<br>mshr_status<br>*Sada možností mshr_hcmcompletionstatus*<br>Čtení/zápis<br>Povinná | Poskytuje stav kandidáta pro prověřování. |
| **Datum dokončení**<br>mshr_completeddate<br>*Datum a čas* | Čtení/zápis<br>Volitelné | Datum dokončení prověřování. |
| **Poznámky**<br>mshr_note<br>*Řetězec* | Čtení/zápis<br>Volitelné | Poznámky určené pro manažery náboru a náboráře. |

## <a name="see-also"></a>Viz také

[Úvod do rozhraní API pro integraci systému sledování žadatelů](hr-admin-integration-ats-api-introduction.md)<br>
[Příklad dotazu pro entitu Kandidát k přijetí](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

