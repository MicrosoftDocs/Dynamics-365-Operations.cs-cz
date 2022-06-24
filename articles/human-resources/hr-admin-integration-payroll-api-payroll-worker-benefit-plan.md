---
title: Plán zaměstnaneckých výhod pracovníka na výplatní listině
description: Tento článek poskytuje informace a ukázkový dotaz pro entitu plánu zaměstnanecké výhody pracovníka pro mzdu v Dynamics 365 Human Resources.
author: twheeloc
ms.date: 07/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ef45855d9e60131ac065ae6e2769b71ae3f69537
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902278"
---
# <a name="payroll-worker-benefit-plan"></a>Plán zaměstnaneckých výhod pracovníka na výplatní listině


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tento článek popisuje entitu plánu zaměstnanecké výhody pracovníka pro mzdu Dynamics 365 Human Resources.

Fyzický název: mshr_payrollworkerbenefitplanentities.

### <a name="description"></a>popis

Tato entita poskytuje informace o plánu zaměstnaneckých výhod pro daného pracovníka.

## <a name="properties"></a>Vlastnosti

| Vlastnost</br>**Fyzický název**</br>**_Typ_** | Použít | popis |
| --- | --- | --- |
| **Číslo pracovníka**</br>mshr_personnelnumber</br>*Řetězec* | Jen pro čtení</br>Požadováno | Jedinečné osobní číslo zaměstnance. |
| **ID právnické osoby**</br>mshr_legalentityID</br>*Řetězec* | Jen pro čtení | Určuje právnickou osobu (společnost). |
| **ID období**</br>mshr_periodid</br>*Řetězec* | Jen pro čtení | Identifikátor období. |
| **ID plánu**</br>mshr_planid</br>*Řetězec* | Jen pro čtení | Identifikátor plánu. |
| **Možnost pokrytí**</br>mshr_coverageoptionid</br>*Řetězec* | Jen pro čtení | Identifikace možnosti pokrytí. |
| **Počáteční datum srážek**</br>mshr_deductionstartdatetime</br>*Posun data a času* | Jen pro čtení | Počáteční datum srážek. |
| **Koncové datum srážek**</br>mshr_deductionenddatetime</br>*Posun data a času* | Jen pro čtení | Koncové datum srážek. |
| **Stav**</br>mshr_status</br>*[Sada možností stavu plánu zaměstnaneckých výhod](hr-admin-integration-payroll-api-benefit-employee-plan-status.md)* | Jen pro čtení | Stav plánu zaměstnaneckých výhod. |
| **Platné od**</br>mshr_validfrom</br>*Posun data a času* | Jen pro čtení | Čas, od kterého je tento záznam platný |
| **Platné do**</br>mshr_validto</br>*Posun data a času* |  Jen pro čtení | Čas, do kterého je tento záznam platný |
| **ID typu plánu**</br>mshr_plantypeid</br>*Řetězec* | Jen pro čtení | Identifikátor typu plánu. |
| **Kód typu plánu**</br>mshr_plantypecode</br>*[sada možností pokrytí typu plánu zaměstnaneckých výhod](hr-admin-integration-payroll-api-benefit-plan-type-cover.md)* | Jen pro čtení | Specifikace typu plánu. |
| **Počet platebních období**</br>mshr_payperiod</br>*Celé číslo* | Jen pro čtení | Počet mzdových období, která představují, jak často jsou vypláceni poskytovatelé zaměstnaneckých výhod nebo zaměstnanci. Tato částka bude použita k výpočtu částky roční mzdy zaměstnance. |
| **Částka zaměstnance**</br>mshr_amountemployee</br>*Desetinné* | Jen pro čtení | Částka zaměstnance nebo procento. |
| **Částka zaměstnavatele**</br>mshr_amountemployer</br>*Desetinné* | Jen pro čtení | Částka zaměstnavatele nebo procento. |
| **Primární pole**</br>mshr_primaryfield</br>*Řetězec* | Generováno systémem | Primární pole. |
| **Hodnota ID pracovníka** </br>_mshr_fk_worker_id_value</br>*GUID* | Cizí klíč: mshr_hcmworkerbaseentityid entity mshr_hcmworkerbaseentity. | Systémem generovaný jedinečný identifikátor pracovníka. |
| **Hodnota ID období**</br> _mshr_fk_period_id_value</br>*GUID* | Cizí klíč: mshr_benefitperiodentityid entity mshr_benefitperiodentity. | Systémem generovaný jedinečný identifikátor období. |
| **Hodnota ID plánu**</br> _mshr_fk_plan_id_value</br>*GUID* | Cizí klíč: mshr_benefitplanentityid entity mshr_benefitplanentity. | Systémem generovaný jedinečný identifikátor plánu. |
| **Hodnota ID typu plánu**</br> _mshr_fk_plantype_id_value</br>*GUID* | Cizí klíč: mshr_benefitplantypeentityid entity mshr_benefitplantypeentity. | Systémem generovaný jedinečný identifikátor plánu. |
| **Hodnota ID možnosti pokrytí**</br> _mshr_fk_coverageoption_id_value</br>*GUID* | Cizí klíč: mshr_benefitcoverageoptionentityid entity mshr_benefitcoverageoptionentity. | Systémem generovaný jedinečný identifikátor plánu. |
| **Hodnota ID entity plánu zaměstnanecké výhody pracovníka pro mzdu**</br> mshr_payrollworkerbenefitplanentityid</br>*GUID* | Jen pro čtení </br> Generováno systémem | Systémem generovaný jedinečný identifikátor pro záznam. |

## <a name="example-query-for-payroll-worker-benefit-plan"></a>Příklad dotazu pro plán zaměstnaneckých výhod pracovníka pro mzdu

**Žádost**

```http
GET [Organization URI]/api/data/v9.1/mshr_payrollworkerbenefitplanentities?$filter=mshr_personnelnumber eq '000020'
```

**Odezva**

```json
{
    "mshr_personnelnumber": "000020",
    "mshr_legalentityid": "USMF",
    "mshr_periodid": "2021",
    "mshr_planid": "Dental plan",
    "mshr_coverageoptionid": "Emp Only",
    "mshr_deductionstartdatetime": "2021-01-01T06:00:00Z",
    "mshr_deductionenddatetime": "2021-12-31T06:00:00Z",
    "mshr_status": 200000001,
    "mshr_validfrom": "2021-01-01T06:00:00Z",
    "mshr_validto": "2021-12-31T06:00:00Z",
    "mshr_plantypeid": "Dental",
    "mshr_plantypecode": 200000001,
    "mshr_payperiod": 12,
    "mshr_amountemployee": 47,
    "mshr_amountemployer": 57,
    "mshr_primaryfield": "000020 | USMF | 2021 | Dental plan",
    "_mshr_fk_worker_id_value": "000000ae-0000-0000-bfff-004105000000",
    "_mshr_fk_period_id_value": "00000807-0000-0000-ee02-005001000000",
    "_mshr_fk_plan_id_value": "00000c61-0000-0000-0200-005001000000",
    "_mshr_fk_plantype_id_value": "0000057c-0000-0000-0200-005001000000",
    "_mshr_fk_coverageoption_id_value": "00000391-0000-0000-0b00-005001000000",
    "mshr_payrollworkerbenefitplanentityid": "000006c4-0000-0000-bfff-004105000000"
}
```
## <a name="see-also"></a>Viz také

[Úvod do rozhraní API integrace mezd](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
