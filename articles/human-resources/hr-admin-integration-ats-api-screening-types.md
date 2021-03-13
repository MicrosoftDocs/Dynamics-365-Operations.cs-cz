---
title: Typy prověřování
description: Toto téma popisuje entitu typy prověřování pro Dynamics 365 Human Resources.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 227c15acb44e020ea9858961e45c11ad07e18a74
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126163"
---
# <a name="screening-types"></a>Typy prověřování

Toto téma popisuje entitu typy prověřování pro Dynamics 365 Human Resources.

Fyzický název: mshr_hcmscreeningtypeentity

## <a name="description"></a>popis

Tato entita popisuje typy prověřování nastavené společností pro procesy před zaměstnáním a probíhající prověřování zaměstnanců.

## <a name="json-representation"></a>JSON reprezentace

```json
{
    "mshr_description": "String",
    "mshr_frequencyunit": Int,
    "mshr_generatefrom": Int,
    "mshr_frequencyinterval": Int,
    "mshr_screeningtypeid": "String",
    "mshr_hcmscreeningtypeentityid": "Guid"
}
```

## <a name="properties"></a>Vlastnosti

| Vlastnost<br>**Fyzický název**<br>**_Typ_** | Použít | popis |
| --- | --- | --- |
| **ID entity typu prověřování**<br>mshr_hcmscreeningtypeentityid<br>*GUID* | Jen pro čtení<br>Povinná<br>Generováno systémem | Jedinečný primární identifikátor pro záznam typu prověřování. |
| **ID typu prověřování**<br>mshr_screeningtypeid<br>*Řetězec* | Čtení/zápis<br>Povinná | Uživatelem určený jedinečný identifikátor pro typ prověřování. |
| **Popis**<br>mshr_description<br>*Řetězec* | Čtení/zápis<br>Povinná | Popis typu prověřování. |
| **Jednotka četnosti**<br>mshr_frequencyunit<br>*nastavená možnost mshr_hcmfrequencyunit* | Čtení/zápis<br>Povinná | Popisuje frekvenci, s jakou musí být u přiřazené osoby provedeno prověření. |
| **Generovat z**<br>mshr_generatefrom<br>*nastavená možnost mshr_hcmfrequencygeneratefrom* | Čtení-zápis<br>Povinná | Pokud je hodnota četnosti jakákoli jiná hodnota než „Pouze jednorázově“, určuje hodnota GenerateFrom datum, od kterého se má vypočítat další prověřovací událost. |
| **Interval četnosti**<br>mshr_frequencyinterval<br>*Celé číslo* | Čtení-zápis<br>Povinná | Pokud je hodnota četnosti jiná než „Pouze jednorázově“, musíte definovat interval pro jednotky času mezi každou prověřovací událostí. |

## <a name="see-also"></a>Viz také

[Úvod do rozhraní API pro integraci systému sledování žadatelů](hr-admin-integration-ats-api-introduction.md)<br>
[Příklad dotazu pro entitu Kandidát k přijetí](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)
