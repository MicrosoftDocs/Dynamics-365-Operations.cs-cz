---
title: Mzdový plán fixní kompenzace
description: Toto téma poskytuje informace a ukázkový dotaz pro entitu pevného plánu kompenzace v Dynamics 365 Human Resources.
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
ms.openlocfilehash: 85cfce6f626090adab422ea6c60fc0778fd1ac67
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021289"
---
# <a name="payroll-fixed-compensation-plan"></a>Mzdový plán fixní kompenzace

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Toto téma poskytuje informace a ukázkový dotaz pro entitu pevného plánu kompenzace v Dynamics 365 Human Resources.

## <a name="properties"></a>Vlastnosti

| Vlastnost<br>**Fyzický název**<br>**_Typ_** | Použít | popis |
| --- | --- | --- |
| **ID zaměstnance**<br>mshr_fk_employee_id_value<br>*GUID* | Jen pro čtení<br>Povinná<br>Cizí klíč: mshr_Employee_id z entity mshr_payrollemployeeentity  | ID zaměstnance |
| **Mzdová sazba**<br>mshr_payrate<br>*Des. místo* | Jen pro čtení<br>Povinná | Mzdová sazba definovaná v plánu pevné kompenzace. |
| **ID plánu**<br>mshr_planid<br>*Řetězec* | Jen pro čtení<br>Povinná |Určuje plán kompenzace.  |
| **Platné od**<br>mshr_validfrom<br>*Posun data a času* |  Jen pro čtení<br>Povinná |Datum začátku platnosti pevné kompenzace zaměstnance.  |
| **Entita mzdového plánu fixní kompenzace**<br>mshr_payrollfixedcompensationplanentityid<br>*GUID* | Povinná<br>Generováno systémem | Systémem generovaná hodnota GUID pro jedinečnou identifikaci plánu kompenzace. |
| **Interval plateb**<br>mshr_payfrequency<br>*Řetězec* | Jen pro čtení<br>Povinná |Četnost, kdy bude zaměstnanec placen.  |
| **Platné do**<br>mshr_validto<br>*Posun data a času* | Jen pro čtení <br>Povinná | Datum konce platnosti pevné kompenzace zaměstnance. |
| **ID pozice**<br>mshr_positionid<br>*Řetězec* | Jen pro čtení <br>Povinná | ID pozice spojené s registrací zaměstnance a plánu pevné kompenzace. |
| **Měna**<br>mshr_currency<br>*Řetězec* | Jen pro čtení <br>Povinná |Měna definovaná pro plán pevné kompenzace   |
| **Číslo pracovníka**<br>mshr_personnelnumber<br>*Řetězec* | Jen pro čtení<br>Povinná |Jedinečné osobní číslo zaměstnance.  |

**Dotaz**

**Žádost**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollfixedcompensationplanentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

**Odezva**

```json
{
            "mshr_planid": "GradeC",
            "mshr_personnelnumber": "000041",
            "mshr_payrate": 75200,
            "mshr_positionid": "000276",
            "mshr_validfrom": "2011-04-05T00:00:00Z",
            "mshr_validto": "2154-12-31T00:00:00Z",
            "mshr_payfrequency": "Annual",
            "mshr_currency": "USD",
            "_mshr_fk_employee_id_value": "00000d3c-0000-0000-d5ff-004105000000",
            "_mshr_fk_plan_id_value": "0000070c-0000-0000-b328-fef003000000",
            "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
            "mshr_payrollfixedcompensationplanentityid": "0000029f-0000-0000-d5ff-004105000000",
            "_mshr_fk_payroll_id_value": null
}
```
