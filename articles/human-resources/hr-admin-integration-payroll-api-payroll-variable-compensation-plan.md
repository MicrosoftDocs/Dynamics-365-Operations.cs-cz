---
title: Mzdový plán variabilní kompenzace
description: Toto téma poskytuje informace a ukázkový dotaz pro entitu plánu variabilní kompenzace v Dynamics 365 Human Resources.
author: marcelbf
ms.date: 06/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-15
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5dc096c08ed808f577c8cdc96ca84000a0b80679
ms.sourcegitcommit: 89bb2a7f402deed32998eddc1e56e75250e3d15e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/29/2021
ms.locfileid: "6314338"
---
# <a name="payroll-variable-compensation-plan"></a>Mzdový plán variabilní kompenzace

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Toto téma popisuje entitu mzdového plánu variabilní kompenzace pro Dynamics 365 Human Resources.

### <a name="description"></a>popis

Tato entita poskytuje plán variabilní kompenzace přiřazený pro danou pozici zaměstnance.

Fyzický název: mshr_payrollvariablecompensationawardentity.

## <a name="properties"></a>Vlastnosti

| Vlastnost</br>**Fyzický název**</br>**_Typ_** | Použít | popis |
| --- | --- | --- |
| **Číslo pracovníka**</br>mshr_personnelnumber</br>*Řetězec* | Jen pro čtení</br>Povinná |Jedinečné osobní číslo zaměstnance.  |
| **Datum odměny**</br>mshr_awarddate</br>*Posun data a času* | Jen pro čtení</br>Povinná | Datum odměny. |
| **Typ odměny**</br>mshr_awardtype</br>*[Nastavení možnosti mshr_HrmCompVarAwardEmplType](hr-admin-integration-payroll-api-award-type.md)* | Jen pro čtení</br>Povinná | Typ odměny, který je definován pro plán variabilní kompenzace. |
| **Měna**</br>mshr_unitcurrencycode</br>*Řetězec* | Jen pro čtení </br>Povinná |Měna definovaná pro plán variabilní kompenzace.   |
| **ID plánu fixní kompenzace**</br>mshr_fixedplanid</br>*Řetězec* | Jen pro čtení | Plán fixní kompenzace, který má být použit jako základ pro výpočet dané odměny. |
| **Hodnota jednotky**</br>mshr_awardamount</br>*Des. místo* | Jen pro čtení | Hodnota jednotky |
| **Typ procesu**</br>mshr_processtype</br>*[Nastavení možnosti mshr_hrmCompProcessType](hr-admin-integration-payroll-api-process-type.md)* | Jen pro čtení | Typ procesu. |
| **Typ plánu variabilní kompenzace**</br>Řetězec</br>*mshr_typeid* | Jen pro čtení | Typ plánu variabilní kompenzace. |
| **ID plánu variabilní kompenzace**</br>Řetězec</br>*mshr_planid* | Jen pro čtení | ID plánu variabilní kompenzace. |
| **Primární pole**</br>mshr_primaryfield</br>*GUID* | Jen pro čtení</br>Generováno systémem. | |
| **ID zaměstnance**</br>mshr_fk_employee_id_value</br>*GUID* | Jen pro čtení</br>Povinná</br>Cizí klíč: mshr_Employee_id z entity mshr_payrollemployeeentity  | ID zaměstnance. |
| **Entita mzdového plánu variabilní kompenzace**</br>mshr_payrollvariablecompensationawardentityid</br>*GUID* | Povinná</br>Generováno systémem | Systémem generovaná hodnota GUID pro jedinečnou identifikaci plánu kompenzace. |


## <a name="example-query"></a>Ukázkový dotaz

**Žádost**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollvariablecompensationawardentities?$filter=mshr_personnelnumber eq '000001'
```

**Odezva**

```json
{
    "mshr_personnelnumber": "000001",
    "mshr_awarddate": "2015-01-15T00:00:00Z",
    "mshr_awardtype": 200000000,
    "mshr_unitcurrencycode": "USD",
    "mshr_fixedplanid": "",
    "mshr_awardamount": 1,
    "mshr_processtype": 200000003,
    "mshr_typeid": "Bonus",
    "mshr_planid": "MgBonus",
    "mshr_primaryfield": "000001 | MgBonus | Bonus | 1/15/2015",
    "_mshr_fk_employee_id_value": "00000655-0000-0000-adff-004105000000",
    "mshr_payrollvariablecompensationawardentityid": "000001a1-0000-0000-adff-004105000000",
    "_mshr_fk_fixedcomp_id_value": null
}
```

## <a name="see-also"></a>Viz také

[Úvod do rozhraní API integrace mezd](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
