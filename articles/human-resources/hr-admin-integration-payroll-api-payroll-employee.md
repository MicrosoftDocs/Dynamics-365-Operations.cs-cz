---
title: Zaměstnanec na výplatní listině
description: Toto téma poskytuje informace a ukázkový dotaz pro entitu zaměstnance na výplatní listině v Dynamics 365 Human Resources.
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0cd37a7323c0dd0dc6e60ff0495f827e9a8582c1
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019363"
---
# <a name="payroll-employee"></a>Zaměstnanec na výplatní listině

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Toto téma poskytuje informace a ukázkový dotaz pro entitu zaměstnance na výplatní listině v Dynamics 365 Human Resources.

## <a name="properties"></a>Vlastnosti

| Vlastnost<br>**Fyzický název**<br>**_Typ_** | Použít | popis |
| --- | --- | --- |
| **Číslo pracovníka**<br>mshr_personnelnumber<br>*Řetězec* | Jen pro čtení<br>Povinná | Jedinečné osobní číslo zaměstnance. |
| **Primární pole**<br>mshr_primaryfield<br>*Řetězec* | Povinná<br>Generováno systémem |  |
| **Příjmení**<br>mshr_lastname<br>*Řetězec* | Jen pro čtení<br>Povinná | Příjmení zaměstnance. |
| **ID právnické osoby**<br>mshr_legalentityID<br>*Řetězec* | Jen pro čtení<br>Povinná | Určuje právnickou osobu (společnost). |
| **Platné od**<br>mshr_namevalidfrom<br>*Posun data a času* | Jen pro čtení <br>Povinná | Datum začátku platnosti informací o zaměstnanci.  |
| **Rod**<br>mshr_gender<br>*Int32* | Jen pro čtení<br>Povinná | Pohlaví zaměstnance. |
| **ID entity zaměstnance na výplatní listině**<br>mshr_payrollemployeeentityid<br>*GUID* | Povinná<br>Generováno systémem | Systémem generovaná hodnota GUID pro jedinečnou identifikaci zaměstnance. |
| **Počáteční datum zaměstnání**<br>mshr_employmentstartdate<br>*Posun data a času* | Jen pro čtení<br>Povinná | Počáteční datum zaměstnaneckého poměru zaměstnance. |
| **ID typu identifikace**<br>mshr_identificationtypeid<br>*Řetězec* |Jen pro čtení<br>Povinná | Typ identifikace definovaný pro zaměstnance. |
| **Koncové datum zaměstnání**<br>mshr_employmentenddate<br>*Posun data a času* | Jen pro čtení<br>Povinná |Koncové datum zaměstnaneckého poměru zaměstnance.  |
| **ID datové oblasti**<br>mshr_dataareaid_id<br>*GUID* | Povinná <br>Generováno systémem | Systémem generovaná hodnota GUID identifikující právnickou osobu (společnost). |
| **Platné do**<br>mshr_namevalidto<br>*Posun data a času* |  Jen pro čtení<br>Povinná | Datum konce platnosti informací o zaměstnanci. |
| **Datum narození**<br>mshr_birthdate<br>*Posun data a času* | Jen pro čtení <br>Povinná | Datum narození zaměstnance |
| **Identifikační číslo do**<br>mshr_identificationnumber<br>*Řetězec* | Jen pro čtení <br>Povinná |Identifikační číslo definované pro zaměstnance.  |
| **Křestní jméno**<br>mshr_firstname<br>*Řetězec* | Jen pro čtení<br>Povinná | Jméno zaměstnance. |
| **Druhé jméno**<br>mshr_middlename<br>*Řetězec* | Jen pro čtení<br>Povinná |Druhé jméno zaměstnance.  |

## <a name="example-query-for-payroll-employee"></a>Příklad dotazu pro zaměstnance na výplatní pásce

**Žádost**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollemployeeentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_identificationtypeid eq @idtype and mshr_namevalidfrom le @asofdate and mshr_namevalidto ge @asofdate&@personnelnumber='000041'&@idtype='SSN'&@asofdate=2021-04-01
```

**Odezva**

```json
{
         "mshr_legalentityid": "USMF",
            "mshr_personnelnumber": "000041",
            "mshr_employmentstartdate": "2011-04-05T07:00:00Z",
            "mshr_employmentenddate": "2154-12-31T23:59:59Z",
            "mshr_firstname": "Cassie",
            "mshr_middlename": "Lassie",
            "mshr_lastname": "Hicks",
            "mshr_namevalidfrom": "2021-03-12T20:34:25Z",
            "mshr_namevalidto": "2154-12-31T23:59:59Z",
            "mshr_birthdate": "1987-09-12T00:00:00Z",
            "mshr_gender": 200000002,
            "mshr_identificationtypeid": "SSN",
            "mshr_identificationnumber": "888-99-9342",
            "mshr_dataareaid": "USMF",
            "mshr_primaryfield": "000041 | USMF | 4/5/2011 07:00:00 am",
            "_mshr_fk_worker_id_value": "000000ad-0000-0000-d5ff-004105000000",
            "_mshr_fk_employment_id_value": "00000d0d-0000-0000-0600-014105000000",
            "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
            "mshr_payrollemployeeentityid": "00000d3c-0000-0000-d5ff-004105000000",
            "_mshr_dataareaid_id_value": null
}
```
