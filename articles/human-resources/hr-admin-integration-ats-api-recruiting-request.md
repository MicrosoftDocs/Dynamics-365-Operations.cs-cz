---
title: Požadavek na nábor
description: Toto téma popisuje entitu Žádost o nábor pro Dynamics 365 Human Resources.
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
ms.openlocfilehash: a1f160d828c8fe5babb96d39afd911052767f67b
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068577"
---
# <a name="recruiting-request"></a>Požadavek na nábor


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Toto téma popisuje entitu Žádost o nábor pro Dynamics 365 Human Resources.

Fyzický název: mshr_hcmrecruitingrequestentity

### <a name="description"></a>popis

Popisuje požadavek na nábor pro práci.

### <a name="json-representation"></a>Kód JSON

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_hiringmanagerpersonnelnumber": "String",
    "mshr_recruiterpartynumber": "String",
    "mshr_status": Int,
    "mshr_description": "String",
    "mshr_recruitingrequestlocationid": "String",
    "mshr_comments": "String",
    "mshr_jobid": "String",
    "mshr_titleid": "String",
    "mshr_jobfunctionid": "String",
    "mshr_defaultfulltimeequivalency": Decimal,
    "mshr_regulatoryjobcategory": Int,
    "mshr_jobtypeid": "String",
    "mshr_exemptstatus": Int,
    "mshr_estimatedstartdate": "Date",
    "mshr_externaldescription": "String",
    "mshr_compensationlevelid": "String",
    "mshr_compensationlowthreshold": Decimal,
    "mshr_compensationcontrolpoint": Decimal,
    "mshr_compensationhighthreshold": Decimal,
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "_mshr_fk_hiringmanager_id_value": "Guid",
    "_mshr_fk_recruiter_id_value": "Guid",
    "_mshr_fk_job_id_value": "Guid",
    "_mshr_fk_title_id_value": "Guid",
    "_mshr_fk_jobtype_id_value": "Guid",
    "_mshr_fk_compensationlevel_id_value": "Guid",
    "mshr_hcmrecruitingrequestentityid": "Guid",
    "_mshr_fk_recruitingrequestlocation_id_value": “Guid”
}
```

### <a name="properties"></a>Vlastnosti

| Vlastnost<br>**Fyzický název**<br>**_Typ_** | Použít | popis |
| --- | --- | --- |
| **ID požadavku na nábor**<br>mshr_recruitingrequestid<br>*Řetězec* | Jen pro čtení<br>Povinná<br>Generováno systémem | Uživatelsky čitelný jedinečný identifikátor pro žádost zobrazenou v aplikaci HR. Číselná řada. |
| **ID entity Žádost o nábor**<br>mshr_hcmrecruitingrequestentityid<br>*GUID* | Jen pro čtení<br>Povinná<br>Generováno systémem | Systémem generovaná hodnota GUID pro jedinečnou identifikaci žádosti o nábor. |
| **ID datové oblasti**<br>mshr_dataareaid<br>*Řetězec* | Čtení/zápis<br>Volitelné<br> | Určuje právnickou osobu (společnost) pro žádost o nábor. |
| **Hodnota ID datové oblasti**<br>_mshr_dataareaid_id_value<br>*GUID*<br> | Jen pro čtení<br>Volitelné<br>Cizí klíč: cdm_companyid entity cdm_company | Systémem generovaná hodnota GUID identifikující právnickou osobu (společnost) pro žádost o nábor. |
| **Osobní číslo náborového manažera**<br>mshr_hiringmanagerpersonnelnumber<br>*Řetězec* | Čtení/zápis<br>Volitelné | Osobní číslo náborového manažera přidružené k této žádosti o nábor. |
| **Hodnota ID náborového manažera**<br>_mshr_fk_hiringmanager_id_value<br>*GUID* | Jen pro čtení<br>Volitelné<br>Cizí klíč: mshr_hcmworkerbaseentityid entity mshr_hcmworkerbaseentity | Systémem generovaná hodnota GUID k identifikaci manažera přidruženého k žádosti o nábor. |
| **Číslo strany náboráře**<br>mshr_recruiterpartynumber<br>*Řetězec* | Čtení/zápis<br>Volitelné | Číslo osoby (strany) náboráře vybraného pro danou žádost. |
| **Hodnota ID náboráře**<br>_mshr_fk_recruiter_id_value<br>*GUID* | Jen pro čtení<br>Volitelné<br>Cizí klíč: mshr_dirpersonentityid entity mshr_dirpersonentity | Systémem generovaná hodnota GUID k identifikaci náboráře přidruženého k žádosti o nábor. |
| **Stav**<br>mshr_status<br>Sada možností *RecruitingRequestStatus* | Čtení/zápis<br>Povinná<br> | Označuje stav žádosti na nábor. |
| **Popis**<br>mshr_description<br>*Řetězec* | Čtení/zápis<br>Povinná | Popisuje žádost. |
| **ID místa žádosti o nábor**<br>mshr_recruitingrequestlocationid<br>*Řetězec* | Čtení/zápis<br>Volitelné | Uživatelsky čitelný jedinečný identifikátor místa výkonu práce přidruženého k této žádosti. |
| **Hodnota ID místa náboru**<br>_mshr_fk_recruitinglocation_id_value<br>*GUID* | Jen pro čtení<br>Volitelné<br>Cizí klíč: mshr_hcmrecruitingrequestlocationentityid entity mshr_hcmrecruitingrequestlocationentity | Systémem generovaná hodnota GUID k identifikaci místa náboru vybraného pro žádost o nábor. |
| **Komentáře**<br>mshr_comments<br>*Řetězec* | Čtení/zápis<br>Volitelné | Komentáře k žádosti určené pro náborové manažery a náboráře. |
| **ID úlohy**<br>mshr_jobid<br>*Řetězec* | Jeden zápis<br>Povinná |   Uživatelsky čitelný, jedinečný identifikátor práce sdílené všemi pozicemi přidruženým k této žádosti. |
| **Hodnota ID práce**<br>_mshr_fk_job_id_value<br>*GUID* | Jen pro čtení<br>Povinná<br>Cizí klíč: mshr_hcmjobentityid entity mshr_hcmjobentity | Systémem generovaný, jedinečný identifikátor práce sdílené všemi pozicemi přidruženým k žádosti o nábor. |
| **ID titulu**<br>mshr_titleid<br>*Řetězec* | Jen pro čtení<br>Povinná | Uživatelsky čitelný, jedinečný identifikátor titulu práce přidruženého k této žádosti. |
| **Hodnota ID titulu**<br>_mshr_fk_title_id_value<br>*GUID* | Jen pro čtení<br>Povinná<br>Cizí klíč: mshr_hcmtitleid entity mshr_hcmtitleentity | Systémem generovaný, jedinečný identifikátor titulu práce vybraného pro žádost o nábor. |
| **ID pracovní funkce**<br>mshr_jobfunctionid<br>*Řetězec* | Jen pro čtení<br>Povinná<br>Cizí klíč: mshr_jobfunctionid entity mshr_hcmjobfunctionentity | Uživatelem čitelný, jedinečný identifikátor pracovní funkce přidružené k této žádosti. |
| **Výchozí ekvivalent plného úvazku**<br>mshr_defaultfulltimeequivalency<br>*Dvojité* | Jen pro čtení<br>Povinná | Hodnota ekvivalentu na plný úvazek pro práci, kde 1,0 představuje pracovníka na plný úvazek. |
| **Regulační kategorie pracovních míst**<br>mshr_regulatoryjobcategory<br>Sada možností *RegulatoryJobCategory* | Jen pro čtení<br>Volitelné | Kategorie práce EEO pracovní funkce vybrané pro práci. Platné hodnoty obsažené v sadě možností HcmRegulatoryJobCatetory (mshr_hcmregulatoryjobcategory). |
| **ID typu práce**<br>mshr_jobtypeid<br>*Řetězec* | Jen pro čtení<br>Volitelné | Typ práce přidružený k pozici. Typy práce jsou uživatelem definované hodnoty dostupné v entitě mshr_hcmjobtypeentity. |
| **Hodnota ID typu práce**<br>_mshr_fk_jobtype_id_value<br>*GUID* | Jen pro čtení<br>Volitelné<br>Cizí klíč: mshr_hcmjobtypeentityid entity mshr_hcmjobtypenentity | Systémem generovaný, jedinečný identifikátor typu práce přidruženého k práci pro žádost o nábor. |
| **Stav osvobození od daně**<br>mshr_exemptstatus<br>Sada možností *JobExemptStatus* | Jen pro čtení<br>Volitelné | Stav osvobození FLSA na základě typu práce. |
| **Odhadované počáteční datum**<br>mshr_estimatedstartdate<br>*Datum* | Čtení/zápis<br>Povinná | Odhadované datum, kdy kandidát začne pracovat. |
| **Externí popis**<br>mshr_externaldescription<br>*Řetězec* | Čtení/zápis<br>Volitelné | Popis práce/pozice vystavený kandidátovi. | 
| **Dolní prahová hodnota kompenzace**<br>mshr_compensationlowthreshold<br>*Dvojité* | Čtení/zápis<br>Volitelné | Dolní mez úrovně kompenzace. |
| **Kontrolní bod kompenzace**<br>mshr_compensationcontrolpoint<br>*Dvojité* | Čtení/zápis<br>Volitelné | Kontrolní bod úrovně kompenzace. |
| **Horní prahová hodnota kompenzace**<br>mshr_compensationhighthreshold<br>*Dvojité* | Čtení/zápis<br>Volitelné | Horní mez úrovně kompenzace. |
| **Úroveň kompenzace**<br>mshr_compensationlevelid<br>*Řetězec* | Čtení/zápis<br>Volitelné | Úroveň kompenzace práce. Pro práci lze nastavit několik úrovní kompenzace. Tento atribut označuje vybranou úroveň kompenzace práce pro tento požadavek. |
| **ID kompenzace práce**<br>_mshr_fk_jobcompensation_id_value<br>*GUID* | Jen pro čtení<br>Volitelné<br>Cizí klíč: mshr_hcmjobcompensationentityid entity mshr_hcmjobcompensationentity | Systémem generovaný, jedinečný identifikátor pro úroveň kompenzace přidruženou k práci dané žádosti o nábor. |

## <a name="see-also"></a>Viz také

[Úvod do rozhraní API pro integraci systému sledování žadatelů](hr-admin-integration-ats-api-introduction.md)<br>
[Příklad dotazu na žádost o nábor](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
