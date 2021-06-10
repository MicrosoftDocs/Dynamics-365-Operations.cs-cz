---
title: Certifikát osoby
description: Toto téma popisuje entitu Certifikát osoby pro Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
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
ms.openlocfilehash: 5cdd742d6d36ccd7136f95e416507ed6e5e5a75a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055189"
---
# <a name="person-certificate"></a>Certifikát osoby

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Toto téma popisuje entitu Certifikát osoby pro Dynamics 365 Human Resources.

Fyzický název: mshr_hcmpersoncertificateentity

## <a name="description"></a>popis

Tato entita popisuje profesní certifikáty kandidáta.

## <a name="json-representation"></a>Kód JSON

```json
{
    "mshr_certificatetypeid": "String",
    "mshr_startdate": "Date",
    "mshr_enddate": "Date",
    "mshr_notes": "String",
    "mshr_partynumber": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_certificatetype_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersoncertificateentityid": "Guid"
}
```

## <a name="properties"></a>Vlastnosti

| Vlastnost<br>**Fyzický název**<br>**_Typ_** | Použít | popis |
| --- | --- | --- |
| **ID entity Certifikát osoby**<br>mshr_hcmpersoncertificateentityid<br>*GUID* | Jen pro čtení<br>Povinná | Systémem generovaný jedinečný identifikátor pro záznam entity certifikátu osoby. |
| **Číslo strany**<br>mshr_partynumber<br>*Řetězec* | Čtení/zápis<br>Povinná | ID strany (osoby), která je kandidátem. |
| **Hodnota ID osoby**<br>_mshr_fk_person_id_value<br>*GUID* | Jen pro čtení<br>Povinná<br>Cizí klíč: mshr_dirpersonentityid entity mshr_dirpersonentity | Systémem generovaný jedinečný identifikátor záznamu entity strany (osoby). |
| **ID typu certifikátu**<br>mshr_certificatetypeid<br>*Řetězec* | Čtení/zápis<br>Povinná |  Identifikátor typu certifikátu definovaného v Human Resources. |
| **Hodnota ID typu certifikátu**<br>_mshr_fk_certificatetype_id_value<br>*GUID* | Jen pro čtení<br>Povinná<br>Cizí klíč: mshr_hcmcertificatetypeentityid entity mshr_hcmcertificatetypeentity | Systémem generovaný jedinečný identifikátor typu certifikátu přidružené entity. |
| **Počáteční datum**<br>mshr_startdate<br>*Datum a čas* | Čtení/zápis<br>Povinná | Datum vystavení certifikátu. |
| **Koncové datum**<br>mshr_enddate<br>*Datum a čas* | Čtení/zápis<br>Volitelné | Datum konce platnosti certifikátu. |
| **Poznámky**<br>mshr_notes<br>*Řetězec* | Čtení/zápis<br>Volitelné | Poznámky určené pro manažery náboru a náboráře. |
| **Primární pole**<br>mshr_primaryfield<br>*Řetězec* | Jen pro čtení<br>Povinná |  Pole, které se použije jako identifikátor záznamu entity. Kombinace čísla strany, ID typu certifikátu a počátečního data. |

## <a name="see-also"></a>Viz také

[Úvod do rozhraní API pro integraci systému sledování žadatelů](hr-admin-integration-ats-api-introduction.md)<br>
[Příklad dotazu pro entitu Kandidát k přijetí](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]