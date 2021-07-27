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
ms.openlocfilehash: 842c459acd8b5e1a8b6074243b3afa18dc6a13c5
ms.sourcegitcommit: 89bb2a7f402deed32998eddc1e56e75250e3d15e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/29/2021
ms.locfileid: "6314230"
---
# <a name="payroll-position-job"></a>Práce pozice mzdy

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Toto téma popisuje entitu Pracovní pozice mzdy pro Dynamics 365 Human Resources.

### <a name="description"></a>popis

Tato entita poskytuje vztah mezi pozici a pracovní úlohou pro daný plán pevné kompenzace.

Fyzický název: mshr_payrollpositionjobentity.

## <a name="properties"></a>Vlastnosti

| Vlastnost<br>**Fyzický název**<br>**_Typ_** | Použít | popis |
| --- | --- | --- |
| **ID úlohy**<br>mshr_jobid<br>*Řetězec* | Jen pro čtení<br>Povinná |ID úlohy. |
| **Platné od**<br>mshr_validto<br>*Posun data a času* | Jen pro čtení <br>Povinná | Datum, od kterého je pozice a pracovní vztah platné. |
| **Platné do**<br>mshr_validto<br>*Posun data a času* | Jen pro čtení <br>Povinná | Datum, do kterého je pozice a pracovní vztah platné.  |
| **ID pozice**<br>mshr_positionid<br>*Řetězec* | Jen pro čtení<br>Povinná | Identifikace pozice. |
| **Primární pole**<br>mshr_primaryfield<br>*Řetězec* | Povinná<br>Generováno systémem |  |
| **Hodnota ID pracovní pozice**<br>_mshr_fk_positionjob_id_value<br>*GUID* | Jen pro čtení<br>Povinná<br>Cizí klíč: mshr_PayrollPositionJobEntity mshr_payrollpositionjobentity |ID práce přidružené k pozici.|
| **Hodnota ID pevného plánu kompenzace**<br>_mshr_fk_fixedcompplan_id_value<br>*GUID* | Jen pro čtení<br>Povinná<br>Cizí klíč: mshr_FixedCompPlan_id z mshr_payrollfixedcompensationplanentity  | ID plánu pevné kompenzace přidruženého k pozici. |
| **ID entity pracovní pozice na výplatní listině**<br>mshr_payrollpositionjobentityid<br>*Guid* | Povinná<br>Generováno systémem. | Systémem generovaná hodnota GUID pro jedinečnou identifikaci pracovní pozice.  |

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
