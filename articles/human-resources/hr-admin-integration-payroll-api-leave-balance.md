---
title: Zůstatek dovolené
description: Toto téma poskytuje informace a ukázkový dotaz pro entitu zůstatku dovolené v Dynamics 365 Human Resources.
author: marcelbf
ms.date: 06/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ab136e9b40de280387dc3c5207a08a6bb357941feb3a8c736d9671f7850f2bf8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6782676"
---
# <a name="leave-balance"></a>Zůstatek dovolené

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Toto téma popisuje entitu zůstatku dovolené pro Dynamics 365 Human Resources.

### <a name="description"></a>popis

Tato entita poskytuje zůstatek dovolené na typ dovolené pro daného zaměstnance.

Fyzický název: mshr_essleavebalanceentities.

## <a name="properties"></a>Vlastnosti

| Vlastnost</br>**Fyzický název**</br>**_Typ_** | Použít | popis |
| --- | --- | --- |
| **Číslo pracovníka**</br>mshr_personnelnumber</br>*Řetězec* | Jen pro čtení | Jedinečné osobní číslo zaměstnance. |
| **Aktuální zůstatek**</br>mshr_balanceavailable</br>*Des. místo* | Jen pro čtení | Aktuální zůstatek zaměstnance. |
| **Typ**</br>mshr_balanceavailable</br>*Řetězec* | Jen pro čtení | ID typu dovolené. |
| **Míra časového rozlišení**</br>mshr_accrualratedescription</br> | Jen pro čtení | Akruální sazba. |
| **Poslední částka převedená do dalšího období**</br>mshr_lastcarryforwardamount</br>*Des. místo* | Jen pro čtení | Poslední částka převodu do dalšího období. |
| **Vybráno v tomto roce**</br>mshr_takenthisyear</br>*Des. místo* | Jen pro čtení | Výše čerpané dovolené v tomto roce. |
| **Celkově tento rok**</br>mshr_totalthisyear</br>*Des. místo* | Jen pro čtení | Celková částka pro tento rok. |
| **ID datové oblasti**</br>mshr_dataareaid_id</br>*Řetězec* | Jen pro čtení | Určuje právnickou osobu (společnost). |
| **Primární pole**</br>mshr_primaryfield</br>*GUID* | Jen pro čtení</br>Generováno systémem | |
| **ID typu dovolené**</br>_mshr_fk_leavetype_id_value</br>*GUID* | Jen pro čtení</br>Cizí klíč: mshr_essleavetypeentityid entity mshr_essleavetypeentity  | ID typu volna |
| **Entity zůstatku dovolené**</br>mshr_essleavebalanceentityid</br>*GUID* | Generováno systémem | Systémem generovaná hodnota GUID pro jedinečnou identifikaci zůstatku. |

## <a name="example-query"></a>Ukázkový dotaz

**Žádost**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_essleavebalanceentities?$filter=mshr_personnelnumber eq '000013'
```

**Odezva**

```json
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 67.76,
    "mshr_leavetypeid": "PTO",
    "mshr_accrualratedescription": "6.16 hrs / Semimonthly",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 67.76,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | PTO",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-0000-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-2703-005001000000",
    "_mshr_dataareaid_id_value": null
},
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 80,
    "mshr_leavetypeid": "Sick",
    "mshr_accrualratedescription": "80.00 hrs / Annually",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 80,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | Sick",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-ee02-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-3003-005001000000",
    "_mshr_dataareaid_id_value": null
},
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 0,
    "mshr_leavetypeid": "Bereavement",
    "mshr_accrualratedescription": "0.00 hrs / Annually",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 0,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | Bereavement",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-f402-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-4403-005001000000",
    "_mshr_dataareaid_id_value": null
},
{
    "mshr_personnelnumber": "000013",
    "mshr_balanceavailable": 66.65,
    "mshr_leavetypeid": "Vacation",
    "mshr_accrualratedescription": "13.33 hrs / Monthly",
    "mshr_lastcarryforwardamount": 0,
    "mshr_takenthisyear": 0,
    "mshr_totalthisyear": 66.65,
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "000013 | Vacation",
    "_mshr_fk_leavetype_id_value": "00000a6c-0000-0000-f502-005001000000",
    "mshr_essleavebalanceentityid": "0000091f-0000-0000-1009-005001000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Viz také

[Úvod do rozhraní API integrace mezd](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
