---
title: Typ pracovního volna
description: Tento článek poskytuje informace a ukázkový dotaz pro entitu typu dovolené v Dynamics 365 Human Resources.
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
ms.openlocfilehash: 6e7905989df92e943b86f86194c87dcb2a7b1446
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893779"
---
# <a name="leave-type"></a>Typ pracovního volna


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tento článek popisuje entitu entity dovolené pro Dynamics 365 Human Resources.

### <a name="description"></a>Popis

Tato entita poskytuje informace pro daný typ dovolené.

Fyzický název: mshr_essleavetypeentity.

## <a name="properties"></a>Vlastnosti

| Vlastnost</br>**Fyzický název**</br>**_Typ_** | Použít | popis |
| --- | --- | --- |
| **ID typu dovolené**</br>mshr_leavetypeid</br>*Řetězec* | Jen pro čtení | ID typu dovolené. |
| **Popis**</br>mshr_description</br>*Řetězec* | Jen pro čtení | Popis typu dovolené. |
| **Kategorie**</br>mshr_category</br>*Nastavena možnost mshr_LeaveTypeCategory* | Jen pro čtení | Kategorie typu dovolené. |
| **Požadován kód důvodu**</br>mshr_isreasoncoderequired</br>*Nastavení možnost mshr_NoYes* | Jen pro čtení | Definuje, zda je pro typ dovolené vyžadován kód důvodu. |
| **Jednotka dovolené**</br>mshr_leaveamountunit</br>*Nastavení možnosti mshr_LeaveAmountUnit* | Jen pro čtení | Jednotka tohoto typu dovolené. |
| **Povolit půldenní**</br>mshr_enablehalfdaydefinition</br>*Nastavení možnost mshr_NoYes* | Určuje, zda je pro typ dovolené povolen půlden. |
| **ID datové oblasti**</br>mshr_dataareaid_id</br>*Řetězec* | Jen pro čtení | Určuje právnickou osobu (společnost). |
| **Entita typu dovolená**</br>mshr_essleavetypeentityid</br>*GUID* | Generováno systémem | Systémem generovaná hodnota GUID pro jedinečnou identifikaci typu dovolené. |

## <a name="example-query"></a>Ukázkový dotaz

**Žádost**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_essleavetypeentities?$filter=mshr_leavetypeid eq 'PTO'
```

**Odezva**

```json
{
    "mshr_leavetypeid": "PTO",
    "mshr_description": "Paid time off",
    "mshr_category": 200000000,
    "mshr_isreasoncoderequired": 200000000,
    "mshr_leaveamountunit": 200000000,
    "mshr_enablehalfdaydefinition": 200000000,
    "mshr_dataareaid": "usmf",
    "mshr_essleavetypeentityid": "00000a6c-0000-0000-0000-005001000000",
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Viz také

[Úvod do rozhraní API integrace mezd](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
