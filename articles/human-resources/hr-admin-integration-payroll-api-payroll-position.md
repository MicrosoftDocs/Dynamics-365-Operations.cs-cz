---
title: Podrobnosti mzdy pro pozice
description: Tento článek poskytuje informace a ukázkový dotaz pro entitu detailů výplatní listiny pro pozice v Dynamics 365 Human Resources.
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
ms.openlocfilehash: ac36b0386312e1631528b8ab5976db2cb3924caf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904123"
---
# <a name="payroll-position"></a>Pozice mzdy


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tento článek popisuje entitu Pozice mzdy v Dynamics 365 Human Resources.

Fyzický název: mshr_payrollpositionentity.

### <a name="description"></a>popis

Tato entita poskytuje informace týkající se pozice pro daného zaměstnance.

Fyzický název: mshr_payrollpositionentity.

## <a name="properties"></a>Vlastnosti

| Vlastnost</br>**Fyzický název**</br>**_Typ_** | Použít | Popis |
| --- | --- | --- |
| **ID pozice**</br>mshr_positionid</br>*Řetězec* | Jen pro čtení | Identifikace pozice. |
| **ID platebního cyklu**</br>mshr_paycycleid</br>*Řetězec* | Jen pro čtení | Platební cyklus definovaný na pozici. |
| **Roční normální hodiny**</br>annualregularhours</br>*Desetinné* | Jen pro čtení | Roční řádné hodiny definované na pozici. |
| **Placené právnickou osobu**</br>paidbylegalentity</br>*Řetězec* | Jen pro čtení | Právnická osoba definovaná na pozici a odpovědná za vystavení platby. |
| **Platné do**</br>validto</br>*Posun data a času* | Jen pro čtení | Datum, do kterého jsou údaje o poloze platné. |
| **Platné od**</br>validfrom</br>*Posun data a času* | Jen pro čtení | Datum, od kterého jsou údaje o poloze platné. |
| **Primární pole**</br>mshr_primaryfield</br>*Řetězec* | Generováno systémem | Primární pole. |
| **ID entity detailů pozice na výplatní listině**</br>payrollpositiondetailsentityid</br>*Guid* | Požadováno</br>Generováno systémem. | Systémem generovaná hodnota globálně jedinečného identifikátoru (GUID) pro jedinečnou identifikaci pozice. |

## <a name="relations"></a>Vztahy

| Hodnota vlastnosti | Související entita | Navigační vlastnost | Typ kolekce |
| --- | --- | --- | --- |
| _mshr_fk_fixedcompplan_id_value | [mshr_payrollfixedcompensationplanentity](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md) | mshr_FK_FixedCompPlan_id | mshr_FK_PayrollFixedCompensationPlanEntity_PayrollPosition |
| _mshr_fk_hcmpositionhierarchy_id_value | mshr_hcmpositionhierarchyentity | mshr_FK_HcmPositionHierarchy_id | Nelze použít |
| _mshr_fk_job_id_value | mshr_payrollpositionjobentity | mshr_FK_Job_id | mshr_FK_PayrollPositionJobEntity_Payroll |
| _mshr_fk_positionassignmentv2_id_value | mshr_hcmpositionworkerassignmentv2entity | mshr_FK_PositionAssignmentV2_id | Nelze použít |

## <a name="example-query"></a>Ukázkový dotaz

**Žádost**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionentities?$filter=mshr_positionid eq @positionid and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@positionid='000276'&@asofdate=2021-04-01
```

**Odezva**

```json
{
    "mshr_positionid": "000276",
    "mshr_paycycleid": "w",
    "mshr_annualregularhours": 3000,
    "mshr_paidbylegalentity": "USMF",
    "mshr_validfrom": "2021-03-14T00:00:00Z",
    "mshr_validto": "2154-12-31T00:00:00Z",
    "mshr_primaryfield": "000276 | 3/14/2021",
    "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
    "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
    "mshr_payrollpositionentityid": "00010097-0000-0000-df00-014105000000"
}
```

## <a name="see-also"></a>Viz také

[Úvod do rozhraní API integrace mezd](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
