---
title: Profesionální zkušenosti osoby
description: Toto téma popisuje entitu Profesionální zkušenosti osoby pro Dynamics 365 Human Resources.
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
ms.openlocfilehash: cc26e0ae1428811161b3573edec4aa47b46ae16dd8a69d44d2cdd77d49e68193
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6763027"
---
# <a name="person-professional-experience"></a>Profesionální zkušenosti osoby

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Toto téma popisuje entitu Profesionální zkušenosti osoby pro Dynamics 365 Human Resources.

Fyzický název: mshr_hcmpersonprofessionalexperienceentity

## <a name="description"></a>popis

Tato entita popisuje profesionální zkušenosti nebo pracovní historii kandidáta.

## <a name="json-representation"></a>Kód JSON

```json
{
    "mshr_partynumber": "String",
    "mshr_employerposition": "String",
    "mshr_startdate": "Date",
    "mshr_allowcontactemployer": Int,
    "mshr_employerlocation": "String",
    "mshr_employername": "String",
    "mshr_enddate": "Date",
    "mshr_note": "String",
    "mshr_phone": "String",
    "mshr_url": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonprofessionalexperienceentityid": "Guid"
}
```

## <a name="properties"></a>Vlastnosti

| Vlastnost<br>**Fyzický název**<br>**_Typ_** | Použít | popis |
| --- | --- | --- |
| **ID entity Profesionální zkušenosti osoby**<br>mshr_hcmpersonprofessionalexperienceentityid<br>*GUID* | Jen pro čtení<br>Povinná | Systémem generovaný jedinečný identifikátor pro záznam entity. |
| **Číslo strany**<br>mshr_partynumber<br>*Řetězec* | Čtení/zápis<br>Povinná | Jedinečný identifikátor záznamu osoby kandidáta. |
| **Hodnota ID osoby**<br>_mshr_fk_person_id_value<br>*GUID* | Jen pro čtení<br>Povinná<br>Cizí klíč: mshr_dirpersonentityid entity mshr_dirpersonentity | Systémem generovaný jedinečný identifikátor pro záznam entity osoby. |
| **Pozice zaměstnavatele**<br>mshr_employerposition<br>*Řetězec* | Čtení/zápis<br>Povinná | Titul kandidáta podle pozice, kterou zastával během zaměstnaneckého poměru. |
| **Název zaměstnavatele**<br>mshr_employername<br>*Řetězec* | Čtení/zápis<br>Povinná | Název zaměstnavatele. |
| **Umístění zaměstnavatele**<br>mshr_employerlocation<br>*Řetězec* | Čtení/zápis<br>Volitelné | Geografické umístění zaměstnavatele. Max. délka: 60. Není definován ani vyžadován žádný konkrétní formát. |
| **Telefon**<br>mshr_phone<br>*Řetězec* | Čtení/zápis<br>Volitelné | Telefonní číslo zaměstnavatele. |
| **URL**<br>mshr_url<br>*Řetězec* | Čtení/zápis<br>Volitelné | Adresa URL webové stránky zaměstnavatele. |
| **Počáteční datum**<br>mshr_startdate<br>*Datum a čas* | Čtení/zápis<br>Povinná | Počáteční datum zaměstnaneckého poměru kandidáta. |
| **Koncové datum**<br>mshr_enddate<br>*Datum a čas* | Čtení/zápis<br>Volitelné | Koncové datum zaměstnaneckého poměru kandidáta, nebo null, pokud je kandidát zde stále zaměstnán. |
| **Povolit kontaktování zaměstnavatele**<br>mshr_allowcontactemployer<br>*Sada možností mshr_hrmblankyesno* | Čtení/zápis<br>Volitelné | Označuje, zda kandidát souhlasí s kontaktováním předchozího zaměstnavatele. |
| **Poznámky**<br>mshr_note<br>*Řetězec* | Čtení/zápis<br>Volitelné | Poznámky určené pro náboráře nebo manažery náboru. |
| **Primární pole**<br>mshr_primaryfield<br>*Řetězec* | Jen pro čtení<br>Povinná | Pole použité jako primární identifikátor záznamu entity. Kombinace čísla strany, počátečního data, pozice zaměstnavatele a názvu zaměstnavatele. |

## <a name="see-also"></a>Viz také

[Úvod do rozhraní API pro integraci systému sledování žadatelů](hr-admin-integration-ats-api-introduction.md)<br>
[Příklad dotazu pro entitu Kandidát k přijetí](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]