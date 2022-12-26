---
title: Prověřování osoby
description: Tento článek popisuje entitu Prověřování osoby pro Dynamics 365 Human Resources.
author: jaredha
ms.date: 12/05/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3c316e0381f4d407ed7c4c39b5949717b71477bd
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831883"
---
# <a name="person-screening"></a>Prověřování osoby


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tento článek popisuje entitu Prověřování osoby pro Dynamics 365 Human Resources.

Fyzický název: mshr_hcmpersonscreeningentity

## <a name="description"></a>popis

Tato entita popisuje prověřování, která kandidát úspěšně absolvoval nebo musí absolvovat kvůli zaměstnání.

## <a name="json-representation"></a>JSON reprezentace

```json
{
    "mshr_note": "String",
    "mshr_requiredby": "Date",
    "mshr_status": Int,
    "mshr_partynumber": "String",
    "mshr_screeningtypeid": "String",
    "_mshr_fk_screeningtype_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonscreeningentityid": "Guid",
    "mshr_completeddate": "Date"
}
```

## <a name="properties"></a>Vlastnosti

| Vlastnost<br>**Fyzický název**<br>**_Typ_** | Použít | popis |
| --- | --- | --- |
| **Poznámky**<br>mshr_note<br>*Řetězec* | Čtení/zápis<br>Volitelné | Poznámky určené pro manažery náboru a náboráře. |
| **Požadováno do**<br>mshr_requiredby<br>*Datum a čas* | Čtení/zápis<br>Volitelné | Datum, do kterého je nutné provést prověřování. |
| **Stav**<br>mshr_status<br>*Sada možností mshr_hcmcompletionstatus*|Čtení/zápis<br>Povinný | Poskytuje stav kandidáta pro prověřování. |
| **Číslo strany**<br>mshr_partynumber<br>*Řetězec* | Čtení/zápis<br>Povinný | Číslo strany (osoby) přidružené ke kandidátovi. |
| **ID typu prověřování**<br>mshr_screeningtypeid<br>*Řetězec* | Čtení/zápis<br>Povinná<br>Cizí klíč: ScreeningType | Identifikátor typu prověřování definovaného v Human Resources. |
| **Hodnota ID typu prověřování**<br>_mshr_fk_screeningtype_id_value<br>*GUID* | Jen pro čtení<br>Povinná<br>Cizí klíč: mshr_hcmscreeningtypeentityid entity mshr_hcmscreeningtypeentity | Systémem generovaný identifikátor záznamu typu prověřování přidružené entity. |
| **Primární pole**<br>mshr_primaryfield<br>*Řetězec* |  Jen pro čtení<br>Povinný | Pole, které se použije jako identifikátor záznamu entity. |
| **Hodnota ID osoby**<br>_mshr_fk_person_id_value<br>*GUID* | Jen pro čtení<br>Povinná<br>Cizí klíč: mshr_dirpersonentityid entity mshr_dirpersonentity | Systémem generovaný jedinečný identifikátor záznamu entity strany (osoby). |
| **ID entity Prověřování osoby**<br>mshr_hcmpersonscreeningentityid<br>*GUID* | Jen pro čtení<br>Povinná<br>Generováno systémem| Jedinečný primární identifikátor pro záznam prověřování osoby. |
| **Datum dokončení**<br>mshr_completeddate<br>*Datum a čas* | Čtení/zápis<br>Volitelné | Datum dokončení prověřování. |


## <a name="see-also"></a>Viz také

[Úvod do rozhraní API pro integraci systému sledování žadatelů](hr-admin-integration-ats-api-introduction.md)<br>
[Příklad dotazu pro entitu Kandidát k přijetí](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
