---
title: Podrobnosti mzdy pro pozice
description: Toto téma poskytuje informace a ukázkový dotaz pro entitu detailů výplatní listiny pro pozice v Dynamics 365 Human Resources.
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
ms.openlocfilehash: 05e9d6441cf99dce3f4663b9d5ba57e2b386e8c2f3060f75550270083f3b98b3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741446"
---
# <a name="payroll-position"></a>Pozice mzdy

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Toto téma popisuje entitu Pozice mzdy v Dynamics 365 Human Resources.

Fyzický název: mshr_payrollpositionentity.

### <a name="description"></a>popis

Tato entita poskytuje informace týkající se pozice pro daného zaměstnance.

Fyzický název: 

## <a name="properties"></a>Vlastnosti

| Vlastnost<br>**Fyzický název**<br>**_Typ_** | Použít | popis |
| --- | --- | --- |
| **Roční normální hodiny**<br>annualregularhours<br>*Des. místo* | Jen pro čtení<br>Povinná | Roční řádné hodiny definované na pozici.  |
| **ID entity detailů pozice na výplatní listině**<br>payrollpositiondetailsentityid<br>*Guid* | Povinná<br>Generováno systémem. | Systémem generovaná hodnota GUID pro jedinečnou identifikaci pozice.  |
| **Primární pole**<br>mshr_primaryfield<br>*Řetězec* | Povinná<br>Generováno systémem |  |
| **Hodnota ID pracovní pozice**<br>_mshr_fk_positionjob_id_value<br>*GUID* | Jen pro čtení<br>Povinná<br>Cizí klíč: mshr_PayrollPositionJobEntity mshr_payrollpositionjobentity |ID práce přidružené k pozici.|
| **Hodnota ID pevného plánu kompenzace**<br>_mshr_fk_fixedcompplan_id_value<br>*GUID* | Jen pro čtení<br>Povinná<br>Cizí klíč: mshr_FixedCompPlan_id z mshr_payrollfixedcompensationplanentity  | ID plánu pevné kompenzace přidruženého k pozici. |
| **ID platebního cyklu**<br>mshr_primaryfield<br>*Řetězec* | Jen pro čtení<br>Povinná | Platební cyklus definovaný na pozici. |
| **Placené právnickou osobu**<br>paidbylegalentity<br>*Řetězec* | Jen pro čtení<br>Povinná | Právnická osoba definovaná na pozici odpovědné za vystavení platby. |
| **ID pozice**<br>mshr_positionid<br>*Řetězec* | Jen pro čtení<br>Povinná | Identifikace pozice. |
| **Platné do**<br>validto<br>*Posun data a času* | Jen pro čtení<br>Povinná |Datum, od kterého jsou údaje o poloze platné.  |
| **Platné od**<br>validfrom<br>*Posun data a času* | Jen pro čtení<br>Povinná |Datum, do kterého jsou údaje o poloze platné.  |

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
