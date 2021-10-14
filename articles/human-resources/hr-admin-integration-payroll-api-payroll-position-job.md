---
title: Práce pozice mzdy
description: Toto téma poskytuje informace a ukázkový dotaz pro entitu pracovní pozice na výplatní listině v Dynamics 365 Human Resources.
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c0b70411e6535b22d698545438dcb0b16935e731
ms.sourcegitcommit: 12e26ef25c492e5032260733b50cd642cbd6164d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/28/2021
ms.locfileid: "7559576"
---
# <a name="payroll-position-job"></a>Práce pozice mzdy

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Toto téma popisuje entitu Pracovní pozice mzdy pro Dynamics 365 Human Resources.

### <a name="description"></a>popis

Tato entita poskytuje vztah mezi pozici a pracovní úlohou pro daný plán pevné kompenzace.

Fyzický název: mshr_payrollpositionjobentity.

## <a name="properties"></a>Vlastnosti

| Vlastnost</br>**Fyzický název**</br>**_Typ_** | Použít | Popis |
| --- | --- | --- |
| **ID pozice**</br>mshr_positionid</br>*Řetězec* | Jen pro čtení | Identifikace pozice. |
| **Platné od**</br>mshr_validto</br>*Posun data a času* | Jen pro čtení | Datum, od kterého je pozice a pracovní vztah platné. |
| **Platné do**</br>mshr_validto</br>*Posun data a času* | Jen pro čtení | Datum, do kterého je pozice a pracovní vztah platné. |
| **ID úlohy**</br>mshr_jobid</br>*Řetězec* | Jen pro čtení | ID úlohy. |
| **Primární pole**</br>mshr_primaryfield</br>*Řetězec* | Generováno systémem | Primární pole. |
| **ID entity pracovní pozice na výplatní listině**</br>mshr_payrollpositionjobentityid</br>*Guid* | Generováno systémem. | Systémem generovaná hodnota globálně jedinečného identifikátoru (GUID) pro jedinečnou identifikaci práce. |

## <a name="relations"></a>Vztahy

| Hodnota vlastnosti | Související entita | Navigační vlastnost | Typ kolekce |
| --- | --- | --- | --- |
| _mshr_fk_fixedcompplan_id_value | mshr_payrollfixedcompensationplanentity | mshr_FK_FixedCompPlan_id | mshr_FK_PayrollFixedCompensationPlanEntity_Job |
| _mshr_fk_jobdetail_id_value | mshr_hcmjobdetailentity | mshr_FK_JobDetail_id | Nelze použít |
| _mshr_fk_payroll_id_value | mshr_payrollpositionentity | mshr_FK_Payroll_id | mshr_FK_PayrollPositionEntity_Job |

## <a name="example-query"></a>Ukázkový dotaz

**Žádost**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionjobentities?$filter=mshr_positionid eq '000276'
```

**Odezva**

```json
{
    "mshr_positionid": "000276",
    "mshr_validfrom": "2016-07-06T18:11:33Z",
    "mshr_validto": "2154-12-31T23:59:59Z",
    "mshr_jobid": "Accountant",
    "mshr_primaryfield": "000276 | Accountant | 7/6/2016 06:11:33 pm",
    "_mshr_fk_jobdetail_id_value": "00000b8d-0000-0000-b0ff-004105000000",
    "_mshr_fk_fixedcompplan_id_value": "0000058a-0000-0000-d5ff-004105000000",
    "_mshr_fk_payroll_id_value": "00000427-0000-0000-df00-014105000000",
    "mshr_payrollpositionjobentityid": "00000906-0000-0000-df00-014105000000"
}
```

## <a name="see-also"></a>Viz také

[Úvod do rozhraní API integrace mezd](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
