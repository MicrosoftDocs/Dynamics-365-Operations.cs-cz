---
title: Mzdový plán variabilní kompenzace
description: Toto téma poskytuje informace a ukázkový dotaz pro entitu plánu variabilní kompenzace v Dynamics 365 Human Resources.
author: twheeloc
ms.date: 06/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-06-15
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c5cc9e02ff2dd49e2eb0c8131fcff2eca4b9c3b1
ms.sourcegitcommit: d67f7edaf1a50077c2a7dd105e774f86fc586495
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2022
ms.locfileid: "8533640"
---
# <a name="payroll-variable-compensation-plan"></a>Mzdový plán variabilní kompenzace


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Toto téma popisuje entitu mzdového plánu variabilní kompenzace pro Dynamics 365 Human Resources.

### <a name="description"></a>popis

Tato entita poskytuje plán variabilní kompenzace přiřazený pro danou pozici zaměstnance.

Fyzický název: mshr_payrollvariablecompensationawardentity.

## <a name="properties"></a>Vlastnosti

| Vlastnost</br>**Fyzický název**</br>**_Typ_** | Použít | popis |
| --- | --- | --- |
| **Číslo pracovníka**</br>mshr_personnelnumber</br>*Řetězec* | Jen pro čtení | Jedinečné osobní číslo zaměstnance.  |
| **Datum odměny**</br>mshr_awarddate</br>*Posun data a času* | Jen pro čtení | Datum odměny. |
| **Typ odměny**</br>mshr_awardtype</br>*[Nastavení možnosti mshr_HrmCompVarAwardEmplType](hr-admin-integration-payroll-api-award-type.md)* | Jen pro čtení | Typ odměny, který je definován pro plán variabilní kompenzace. |
| **Měna**</br>mshr_unitcurrencycode</br>*Řetězec* | Jen pro čtení |Měna definovaná pro plán variabilní kompenzace.   |
| **ID plánu fixní kompenzace**</br>mshr_fixedplanid</br>*Řetězec* | Jen pro čtení | Plán fixní kompenzace, který má být použit jako základ pro výpočet dané odměny. |
| **Hodnota jednotky**</br>mshr_awardamount</br>*Des. místo* | Jen pro čtení | Hodnota jednotky |
| **Typ procesu**</br>mshr_processtype</br>*[Nastavení možnosti mshr_hrmCompProcessType](hr-admin-integration-payroll-api-process-type.md)* | Jen pro čtení | Typ procesu. |
| **Typ plánu variabilní kompenzace**</br>Řetězec</br>*mshr_typeid* | Jen pro čtení | Typ plánu variabilní kompenzace. |
| **ID plánu variabilní kompenzace**</br>Řetězec</br>*mshr_planid* | Jen pro čtení | ID plánu variabilní kompenzace. |
| **Počet jednotek**</br>Desetinné</br>*mshr_numberofunits* | Jen pro čtení | Počet jednotek ocenění. |
| **Primární pole**</br>mshr_primaryfield</br>*GUID* | Jen pro čtení</br>Generováno systémem. | |
| **Entita mzdového plánu variabilní kompenzace**</br>mshr_payrollvariablecompensationawardentityid</br>*GUID* | Generováno systémem | Systémem generovaná hodnota GUID pro jedinečnou identifikaci plánu kompenzace. |

## <a name="relations"></a>Vztahy 

|Hodnota vlastnosti | Související entita | Navigační vlastnost | Typ kolekce |
| --- | --- | --- | --- |
| _mshr_fk_employee_id_value | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | mshr_FK_Employee_id | mshr_FK_PayrollEmployeeEntity_VariableCompAward |
| _mshr_fk_fixedcomp_id_value | [mshr_payrollfixedcompensationplanentity](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md) | mshr_FK_FixedComp_id | mshr_FK_PayrollFixedCompensationPlanEntity_VariableCompAward |

## <a name="example-query"></a>Ukázkový dotaz

**Žádost**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollvariablecompensationawardentities?$filter=mshr_personnelnumber eq '000046'
```

**Odezva**

```json
{
    "mshr_personnelnumber": "000046",
    "mshr_awarddate": "2015-01-15T00:00:00Z",
    "mshr_awardtype": 200000000,
    "mshr_unitcurrencycode": "USD",
    "mshr_fixedplanid": "",
    "mshr_unitvalue": 1,
    "mshr_processtype": 200000003,
    "mshr_typeid": "Bonus",
    "mshr_planid": "MgBonus",
    "mshr_numberofunits": 1500,
    "mshr_primaryfield": "000046 | MgBonus | Bonus | 1/15/2015",
    "_mshr_fk_employee_id_value": "00000666-0000-0000-daff-004105000000",
    "mshr_payrollvariablecompensationawardentityid": "000001a4-0000-0000-0d00-005001000000",
    "_mshr_fk_fixedcomp_id_value": null
}
```

## <a name="see-also"></a>Viz také

[Úvod do rozhraní API integrace mezd](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
