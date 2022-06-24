---
title: Žádost o pracovní volno
description: Tento článek poskytuje informace a ukázkový dotaz pro entitu žádosti o dovolenou v Dynamics 365 Human Resources.
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
ms.openlocfilehash: 47a652d9b7dec15124fc8b62d3c7d0402f88e093
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899665"
---
# <a name="leave-request"></a>Žádost o pracovní volno


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tento článek popisuje entitu žádosti o dovolenou pro Dynamics 365 Human Resources.

### <a name="description"></a>Popis

Tato entita poskytuje informace pro žádost o dovolenou.

Fyzický název: mshr_essleaverequestentity.

## <a name="properties"></a>Vlastnosti

| Vlastnost</br>**Fyzický název**</br>**_Typ_** | Použít | popis |
| --- | --- | --- |
| **ID požadavku**</br>mshr_requestid</br>*Řetězec* | Jen pro čtení | ID požadavku. |
| **ID typu dovolené**</br>mshr_leavetypeid</br>*Řetězec* | Jen pro čtení | ID typu dovolené. |
| **Datum**</br>mshr_leavedate</br>*Posun data a času* | Jen pro čtení | Datum žádosti o dovolenou. |
| **Částka**</br>mshr_amount</br>*Des. místo* | Jen pro čtení | Částka žádosti o dovolenou. |
| **Půldenní typ**</br>mshr_halfdaydefinition</br>*Nastavení možnosti mshr_LeaveHalfDayDefinition* | Jen pro čtení | Typ půldenní dovolené. |
| **Komentář**</br>mshr_comment</br>*Řetězec* | Jen pro čtení | Komentář k žádosti. |
| **Stav**</br>mshr_status</br>*Sada možností mshr_status* | Jen pro čtení | Stav požadavku. |
| **Datum**</br>mshr_requestdate</br>*Posun data a času* | Jen pro čtení | Datum žádosti. |
| **Číslo pracovníka**</br>mshr_personnelnumber</br>*Řetězec* | Jen pro čtení | Jedinečné osobní číslo zaměstnance. |
| **ID kódu důvodu**</br>mshr_reasoncodeid</br>*Řetězec* | Jen pro čtení | ID kódu důvodu. |
| **ID datové oblasti**</br>mshr_dataareaid</br>*Řetězec* | Jen pro čtení | Určuje právnickou osobu (společnost). |
| **Primární pole**</br>mshr_primaryfield</br>*GUID* | Jen pro čtení</br>Generováno systémem | |
| **Entita typu dovolená**</br>mshr_essleaverequestentityid</br>*GUID* | Generováno systémem | Systémem generovaná hodnota GUID pro jedinečnou identifikaci žádosti o dovolenou. |

## <a name="example-query"></a>Ukázkový dotaz

**Žádost**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_essleaverequestentities?$filter=mshr_personnelnumber eq '000020'
```

**Odezva**

```json
{
    "mshr_requestid": "USMF-000001",
    "mshr_leavetype": "PTO",
    "mshr_leavedate": "2017-01-02T00:00:00Z",
    "mshr_amount": 8,
    "mshr_halfdaydefinition": 200000000,
    "mshr_comment": "Taking a week off to relax",
    "mshr_status": 200000009,
    "mshr_requestdate": "2017-07-31T00:00:00Z",
    "mshr_personnelnumber": "000020",
    "mshr_reasoncodeid": "",
    "mshr_dataareaid": "usmf",
    "mshr_primaryfield": "USMF-000001 | PTO | 1/2/2017",
    "mshr_essleaverequestentityid": "000004dd-0000-0000-0f00-005001000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Viz také

[Úvod do rozhraní API integrace mezd](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
