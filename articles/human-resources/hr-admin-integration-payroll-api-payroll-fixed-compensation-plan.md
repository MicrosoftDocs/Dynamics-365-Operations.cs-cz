---
title: Mzdový plán fixní kompenzace
description: Toto téma poskytuje informace a ukázkový dotaz pro entitu pevného plánu kompenzace v Dynamics 365 Human Resources.
author: jcart
ms.date: 08/25/2021
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
ms.openlocfilehash: dcb253fabbb183003048119c7a627bf0ab960050
ms.sourcegitcommit: 4d11061f5de0ddba1f968bd5c3fd694a8b104ccc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/26/2021
ms.locfileid: "7429212"
---
# <a name="payroll-fixed-compensation-plan"></a>Mzdový plán fixní kompenzace

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Toto téma popisuje entitu mzdového plánu pevné kompenzace pro Dynamics 365 Human Resources.

### <a name="description"></a>popis

Tato entita poskytuje plán pevné kompenzace přiřazený pro danou pozici zaměstnance.

Fyzický název: mshr_payrollfixedcompensationplanentity.

## <a name="properties"></a>Vlastnosti

| Vlastnost</br>**Fyzický název**</br>**_Typ_** | Použít | popis |
| --- | --- | --- |
| **ID plánu**</br>mshr_planid</br>*Řetězec* | Jen pro čtení | Určuje plán kompenzace.  |
| **Číslo pracovníka**</br>mshr_personnelnumber</br>*Řetězec* | Jen pro čtení | Jedinečné osobní číslo zaměstnance. |
| **Mzdová sazba**</br>mshr_payrate</br>*Desetinné* | Jen pro čtení | Mzdová sazba definovaná v plánu pevné kompenzace. |
| **ID pozice**</br>mshr_positionid</br>*Řetězec* | Jen pro čtení | ID pozice spojené s registrací zaměstnance a plánu pevné kompenzace. |
| **Platné od**</br>mshr_validfrom</br>*Posun data a času* |  Jen pro čtení | Datum začátku platnosti pevné kompenzace zaměstnance.  |
| **Platné do**</br>mshr_validto</br>*Posun data a času* | Jen pro čtení | Datum konce platnosti pevné kompenzace zaměstnance. |
| **Interval plateb**</br>mshr_payfrequency</br>*Řetězec* | Jen pro čtení | Četnost, kdy bude zaměstnanec placen.  |
| **Měna**</br>mshr_currency</br>*Řetězec* | Jen pro čtení | Měna definovaná pro plán pevné kompenzace. |
| **Entita mzdového plánu fixní kompenzace**</br>mshr_payrollfixedcompensationplanentityid</br>*GUID* | Generováno systémem | Systémem generovaná hodnota GUID pro jedinečnou identifikaci plánu kompenzace. |

## <a name="relations"></a>Vztahy

|Hodnota vlastnosti | Související entita | Navigační vlastnost | Typ kolekce |
| --- | --- | --- | --- |
| _mshr_fk_employee_id_value | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | mshr_FK_Employee_id | mshr_FK_PayrollEmployeeEntity_FixedCompPlan |
| _mshr_fk_job_id_value | [mshr_payrollpositionjobentity](hr-admin-integration-payroll-api-payroll-position-job.md) | mshr_FK_Job_id | mshr_FK_PayrollPositionJobEntity_FixedCompPlan |
| _mshr_fk_payrollposition_id_value | [mshr_payrollpositionentity](hr-admin-integration-payroll-api-payroll-position.md) | mshr_FK_PayrollPosition_id | mshr_FK_PayrollPositionEntity_FixedCompPlan |
| _mshr_fk_plan_id_value | mshr_hcmcompfixedplantableentity | mshr_FK_Plan_id | - |
| _mshr_fk_variablecompaward_id_value | [mshr_payrollvariablecompensationawardentity](hr-admin-integration-payroll-api-payroll-variable-compensation-plan.md) | mshr_FK_VariableCompAward_id | mshr_FK_PayrollVariableCompensationAwardEntity_FixedComp |

## <a name="example-query"></a>Ukázkový dotaz

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

## <a name="see-also"></a>Viz také

[Úvod do rozhraní API integrace mezd](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
