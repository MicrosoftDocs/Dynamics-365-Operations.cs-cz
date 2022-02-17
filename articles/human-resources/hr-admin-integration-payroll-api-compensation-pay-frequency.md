---
title: Interval plateb kompenzace
description: Toto téma poskytuje informace a ukázkový dotaz pro entitu intervalu plateb kompenzace v Dynamics 365 Human Resources.
author: marcelbf
ms.date: 09/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 171b7fb7b361bd1fe2e7e637cd555c88a81a8bcf
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/31/2022
ms.locfileid: "8066136"
---
# <a name="compensation-pay-frequency"></a>Interval plateb kompenzace


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Toto téma popisuje entitu intervalu plateb kompenzace v Dynamics 365 Human Resources.

Fyzický název: mshr_hcmpayrateconversionentity.

### <a name="description"></a>Popis

Tato entita poskytuje informace o přepočtu mzdové sazby pro danou frekvenci výplat kompenzací.

## <a name="properties"></a>Vlastnosti

| Vlastnost</br>**Fyzický název**</br>**_Typ_** | Použít | Popis |
| --- | --- | --- |
| **Přepočet roční mzdové sazby**</br>mshr_annualconversionfactor</br>*Desetinné* | Jen pro čtení | Roční koeficient převodu pro frekvenci plateb |
| **Popis**</br>mshr_description</br>*Řetězec* | Jen pro čtení | Popis převodního kurzu. |
| **Přepočet hodinové mzdové sazby**</br>mshr_hourlyconversionfactor</br>*Desetinné* | Jen pro čtení | Hodinový koeficient převodu pro frekvenci plateb. |
| **Přepočet měsíční mzdové sazby**</br>mshr_monthlyconversionfactor</br>*Desetinné* | Jen pro čtení | Měsíční koeficient převodu pro frekvenci plateb |
| **Převod mzdové sazby**</br>mshr_payrateconversion</br>*Řetězec* | Jen pro čtení | Jedinečný řetězec k identifikaci převodního kurzu. |
| **Období**</br>mshr_period</br>*sada možností období* | Jen pro čtení | Hlavní období pro daný přepočet mzdové sazby. |
| **Přepočet týdenní mzdové sazby**</br>mshr_weeklyconversionfactor</br>*Desetinné* | Jen pro čtení | Týdenní koeficient převodu pro frekvenci plateb. |
| **ID datové oblasti**</br>mshr_dataareaid</br>*Řetězec* | Jen pro čtení | Právnická osoba (společnost). |
| **ID entity frekvence plateb kompenzace**</br>mshr_dirpersonnamehistoricalentityid</br>*GUID* | Generováno systémem | Systémem generovaná hodnota globálně jedinečného identifikátoru (GUID) pro jedinečnou identifikaci záznamu. |

## <a name="example-query-for-payroll-employee"></a>Příklad dotazu pro zaměstnance na výplatní pásce

**Žádost**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_hcmpayrateconversionentities?$filter=mshr_payrateconversion eq 'Annual' and mshr_dataareaid eq 'usmf'
```

**Odezva**

```json
{
    "mshr_annualconversionfactor": 1,
    "mshr_description": "Annual",
    "mshr_hourlyconversionfactor": 0.0004807692,
    "mshr_monthlyconversionfactor": 0.0833333333,
    "mshr_payrateconversion": "Annual",
    "mshr_period": 200000000,
    "mshr_weeklyconversionfactor": 0.0192307692,
    "mshr_dataareaid": "usmf",
    "mshr_hcmpayrateconversionentityid": "0000056e-0000-0000-b027-fef003000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Viz také

[Úvod do rozhraní API integrace mezd](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
