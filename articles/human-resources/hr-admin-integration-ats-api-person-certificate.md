---
title: Certifikát osoby
description: Tento článek popisuje entitu Certifikát osoby pro Dynamics 365 Human Resources.
author: jaredha
ms.date: 12/15/2022
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
ms.openlocfilehash: 1f9d5a8c83d9714a4d10dec16e66ab87b794b074
ms.sourcegitcommit: 69d7dd6a2d0dc7f2661c7d1f61e8874c7bde1448
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/19/2022
ms.locfileid: "9887310"
---
# <a name="person-certificate"></a>Certifikát osoby


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tento článek popisuje entitu Certifikát osoby pro Dynamics 365 Human Resources.

Fyzický název: mshr_hcmpersoncertificateentity

## <a name="description"></a>popis

Tato entita popisuje profesní certifikáty kandidáta.

## <a name="json-representation"></a>JSON reprezentace

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
| **ID typu certifikátu**<br>mshr_certificatetypeid<br>*Řetězec* | Čtení/zápis<br>Povinná |  Identifikátor typu certifikátu definovaného v Human Resources. |
| **Počáteční datum**<br>mshr_startdate<br>*Datum a čas* | Čtení/zápis<br>Povinný | Datum vystavení certifikátu. |
| **Koncové datum**<br>mshr_enddate<br>*Datum a čas* | Čtení/zápis<br>Volitelné | Datum konce platnosti certifikátu. |
| **Poznámky**<br>mshr_notes<br>*Řetězec* | Čtení/zápis<br>Volitelné | Poznámky určené pro manažery náboru a náboráře. |
| **Číslo strany**<br>mshr_partynumber<br>*Řetězec* | Čtení/zápis<br>Povinný | ID strany (osoby), která je kandidátem. |
| **Primární pole**<br>mshr_primaryfield<br>*Řetězec* | Jen pro čtení<br>Povinný |  Pole, které se použije jako identifikátor záznamu entity. Kombinace čísla strany, ID typu certifikátu a počátečního data. |
| **Hodnota ID typu certifikátu**<br>_mshr_fk_certificatetype_id_value<br>*GUID* | Jen pro čtení<br>Povinná<br>Cizí klíč: mshr_hcmcertificatetypeentityid entity mshr_hcmcertificatetypeentity | Systémem generovaný jedinečný identifikátor typu certifikátu přidružené entity. |
| **Hodnota ID osoby**<br>_mshr_fk_person_id_value<br>*GUID* | Jen pro čtení<br>Povinná<br>Cizí klíč: mshr_dirpersonentityid entity mshr_dirpersonentity | Systémem generovaný jedinečný identifikátor záznamu entity strany (osoby). |
| **ID entity Certifikát osoby**<br>mshr_hcmpersoncertificateentityid<br>*GUID* | Jen pro čtení<br>Povinná | Systémem generovaný jedinečný identifikátor pro záznam entity certifikátu osoby. |




## <a name="see-also"></a>Viz také

[Úvod do rozhraní API pro integraci systému sledování žadatelů](hr-admin-integration-ats-api-introduction.md)<br>
[Příklad dotazu pro entitu Kandidát k přijetí](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
