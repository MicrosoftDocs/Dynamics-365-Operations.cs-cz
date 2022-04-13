---
title: Historie jména osoby
description: Toto téma poskytuje informace a ukázkový dotaz pro entitu historie jména osoby na výplatní listině v Dynamics 365 Human Resources.
author: twheeloc
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: db22a602c782cef15b6e5769b9c0726dff158160
ms.sourcegitcommit: d67f7edaf1a50077c2a7dd105e774f86fc586495
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2022
ms.locfileid: "8533591"
---
# <a name="person-name-history"></a>Historie jména osoby


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Toto téma popisuje entitu Historie jména osoby v Dynamics 365 Human Resources.

Fyzický název: mshr_dirpersonnamehistoricalentity.

### <a name="description"></a>Popis

Tato entita poskytuje informace o historii jména dané osoby.

> [!IMPORTANT] 
> Pole **FirstName**, **MiddleName**, **LastName**, **NameValidFrom** a **NameValidTo** již nejsou v entitě Zaměstnanec na výplatní listině dostupná. Byla odebrána, aby bylo zajištěno, že existuje pouze jeden datový zdroj data platnosti, který podporuje tuto entitu.

## <a name="properties"></a>Vlastnosti

| Vlastnost</br>**Fyzický název**</br>**_Typ_** | Použít | Popis |
| --- | --- | --- |
| **Jméno**</br>mshr_firstname</br>*Řetězec* | Jen pro čtení | Jméno. |
| **Předpona příjmení**</br>mshr_lastnameprefix</br>*Řetězec*) | Jen pro čtení | Předpona příjmení. |
| **Příjmení**</br>mshr_lastname</br>*Řetězec*) | Jen pro čtení | Příjmení. |
| **Druhé jméno**</br>mshr_middlename</br>*Řetězec*) | Jen pro čtení | Druhé jméno. |
| **Platné do**</br>mshr_validto</br>*Řetězec*) | Jen pro čtení | Datum, dokdy je jméno platné. |
| **Číslo strany**</br>mshr_partynumber</br>*Řetězec* | Jen pro čtení | Uživatelem čitelný, systémem generovaný jedinečný identifikátor osoby. |
| **Primární pole**</br>mshr_primaryfield</br>*Řetězec* | Jen pro čtení | Jedinečný identifikátor záznamu. |
| **ID entity historie jména osoby**</br>mshr_dirpersonnamehistoricalentityid</br>*GUID* | Generováno systémem | Systémem generovaná hodnota globálně jedinečného identifikátoru (GUID) pro jedinečnou identifikaci záznamu. |

## <a name="relations"></a>Vztahy

| Hodnota vlastnosti | Související entita | Navigační vlastnost | Typ kolekce |
| --- | --- | --- | --- |
| Nelze použít | [mshr_payrollemployeeentity](hr-admin-integration-payroll-api-payroll-employee.md) | Nelze použít | mshr_FK_PayrollEmployeeEntity_Name |

## <a name="example-query-for-payroll-employee"></a>Příklad dotazu pro zaměstnance na výplatní pásce

**Žádost**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_dirpersonnamehistoricalentities?$filter=mshr_partynumber eq 'HR000001606'
```

**Odezva**

```json
{
    "mshr_firstname": "Agustina",
    "mshr_lastnameprefix": "",
    "mshr_lastname": "Fierro",
    "mshr_middlename": "middle",
    "mshr_validto": "2021-09-10T21:23:53Z",
    "mshr_partynumber": "HR000001606",
    "mshr_primaryfield": "HR000001606 | ",
    "mshr_dirpersonnamehistoricalentityid": "00000832-0000-0000-c12b-014105000000",
    "mshr_validfrom": null
},
{
    "mshr_firstname": "Agustina",
    "mshr_lastnameprefix": "",
    "mshr_lastname": "Fierro",
    "mshr_middlename": "",
    "mshr_validto": "2154-12-31T23:59:59Z",
    "mshr_partynumber": "HR000001606",
    "mshr_primaryfield": "HR000001606 | 9/10/2021 09:23:54 pm",
    "mshr_dirpersonnamehistoricalentityid": "00000832-0000-0000-d20b-000010000000",
    "mshr_validfrom": "2021-09-10T21:23:54Z"
}
```

## <a name="see-also"></a>Viz také

[Úvod do rozhraní API integrace mezd](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
