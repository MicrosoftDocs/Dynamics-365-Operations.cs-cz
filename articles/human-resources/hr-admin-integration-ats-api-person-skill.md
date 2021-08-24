---
title: Dovednost osoby
description: Toto téma popisuje entitu Dovednost osoby pro Dynamics 365 Human Resources.
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
ms.openlocfilehash: d2721e3eace401537e85e57b5895d508317e6c4b71d481d15ff176b786a937e4
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756189"
---
# <a name="person-skill"></a>Dovednost osoby

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Toto téma popisuje entitu Dovednost osoby pro Dynamics 365 Human Resources.

Fyzický název: mshr_hcmpersonskillentity

## <a name="description"></a>popis

Tato entita popisuje dovednosti kandidáta.

## <a name="json-representation"></a>Kód JSON

```json
{
    "mshr_certifier": "String",
    "mshr_partynumber": "String",
    "mshr_levelid": "String",
    "mshr_ratinglevelexaminer": "String",
    "mshr_skillid": "String",
    "mshr_ratingid": "String",
    "mshr_leveltype": Int,
    "mshr_yearsofexperience": Decimal,
    "mshr_verified": Int,
    "mshr_leveldate": "Date",
    "mshr_primaryfield": "String",
    "_mshr_fk_certifier_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_ratinglevel_id_value": "Guid",
    "_mshr_fk_ratinglevelexaminer_id_value": "Guid",
    "_mshr_fk_skill_id_value": "Guid",
    "mshr_hcmpersonskillentityid": "Guid"
}
```

## <a name="properties"></a>Vlastnosti

| Vlastnost<br>**Fyzický název**<br>**_Typ_** | Použít | popis |
| --- | --- | --- |
| **ID entity Dovednost osoby**<br>mshr_hcmpersonskillentityid<br>*GUID* | Jen pro čtení<br>Povinná | Systémem generovaný jedinečný identifikátor pro záznam entity. |
| **Číslo strany**<br>mshr_partynumber<br>*Řetězec* | Čtení/zápis<br>Povinná |   ID záznamu přidružené strany (osoby). |
| **Hodnota ID osoby**<br>_mshr_fk_person_id_value<br>*GUID* | Jen pro čtení<br>Povinná<br>Cizí klíč: mshr_dirpersonentityid entity mshr_dirpersonentity | Systémem generovaný jedinečný identifikátor záznamu entity strany (osoby). |
| **Certifikátor**<br>mshr_certifikátor<br>*Řetězec* | Čtení/zápis<br>Volitelné | Osobní číslo pracovníka, který tuto dovednost certifikoval. |
| **Hodnota ID certifikátora**<br>_mshr_fk_certifier_id_value<br>*GUID* | Jen pro čtení<br>Volitelné<br>Cizí klíč: mshr_hcmworkerentityid entity mshr_hcmworkerentity | Systémem generovaný jedinečný identifikátor záznamu pracovníka, který certifikoval dovednost. |
| **ID dovednosti**<br>mshr_skillid<br>*Řetězec* | Čtení/zápis<br>Povinná | Identifikátor dovednosti definované v Human Resources. |
| **Hodnota ID dovednosti**<br>_mshr_fk_skill_id_value<br>*GUID* | Jen pro čtení<br>Povinná<br>Cizí klíč: mshr_hcmskillentityid entity mshr_hcmskillentity | Systémem generovaný identifikátor vybrané dovednosti. |
| **Roky praxe**<br>mshr_yearsofexperience<br>*Des. místo* | Čtení/zápis<br>Volitelné | Roky zkušeností, které má kandidát s touto dovedností. |
| **ID hodnocení**<br>mshr_ratingid<br>*Řetězec* | Čtení/zápis<br>Povinná | Typ stupnice hodnocení. Pro tuto entitu je hodnota **Dovednosti**. |
| **Typ úrovně**<br>mshr_leveltype<br>*Sada možností mshr_hrmskillleveltype* | Čtení/zápis<br>Povinná | Kategorizace typů pro úroveň přiřazenou dané dovednosti. |
| **ID úrovně**<br>mshr_levelid<br>*Řetězec* | Čtení/zápis<br>Povinná | ID úrovně hodnocení, kterou má kandidát pro tuto dovednost. |
| **Hodnota ID úrovně hodnocení**<br>_mshr_fk_ratinglevel_id_value<br>*GUID* | Jen pro čtení<br>Povinná<br>Cizí klíč: mshr_hcmratinglevelentityid entity mshr_hcmratinglevelentity | Systémem generovaný identifikátor úrovně hodnocení. |
| **Datum úrovně**<br>mshr_leveldate<br>*Datum a čas* | Čtení/zápis<br>Povinná | Datum, kdy byl kandidát ohodnocen v této dovednosti. |
| **Úroveň hodnocení – zkoušející**<br>mshr_ratinglevelexaminer<br>*Řetězec* | Čtení/zápis<br>Volitelné | Osobní číslo pracovníka, který ohodnotil kandidáta. |
| **Hodnota ID úrovně hodnocení – zkoušející**<br>_mshr_fk_ratinglevelexaminer_id_value<br>*GUID* | Jen pro čtení<br>Volitelné<br>Cizí klíč: mshr_hcmworkerentityid entity mshr_hcmworkerentity | Systémem generovaný identifikátor pracovníka, který zkoušel úroveň dovednosti kandidáta. |
| **Ověřeno**<br>mshr_verified<br>*Sada možností mshr_noyes* | Čtení/zápis<br>Povinná | Označuje, zda byla ověřena úroveň posouzené dovednosti. |
| **Primární pole**<br>mshr_primaryfield<br>*Řetězec* | Jen pro čtení<br>Povinná | Pole, které se použije jako identifikátor záznamu entity. Kombinace čísla strany, typu úrovně, ID dovednosti a data úrovně. |

## <a name="see-also"></a>Viz také

[Úvod do rozhraní API pro integraci systému sledování žadatelů](hr-admin-integration-ats-api-introduction.md)<br>
[Příklad dotazu pro entitu Kandidát k přijetí](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]