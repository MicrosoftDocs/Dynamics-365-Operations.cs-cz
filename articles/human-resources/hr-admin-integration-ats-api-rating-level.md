---
title: Úroveň hodnocení
description: Toto téma popisuje entitu Úroveň hodnocení pro Dynamics 365 Human Resources.
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
ms.openlocfilehash: 1ad37c7a5b961bb03d37775168dac91e606d2b08
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125250"
---
# <a name="rating-level"></a>Úroveň hodnocení

Toto téma popisuje entitu Úroveň hodnocení pro Dynamics 365 Human Resources.

Fyzický název: mshr_hcmratinglevelentity

## <a name="description"></a>popis

Tato entita poskytuje dostupné úrovně hodnocení dovedností. Úrovně hodnocení platí pro všechny právnické osoby.

## <a name="json-representation"></a>Kód JSON

```json
{
    "mshr_description": "String",
    "mshr_factor": Int,
    "mshr_note": "String",
    "mshr_ratinglevelid": "String",
    "mshr_ratingmodelid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_ratingmodelentity_id_value": "Guid",
    "mshr_hcmratinglevelentityid": "Guid"
}
```

## <a name="properties"></a>Vlastnosti

| Vlastnost<br>**Fyzický název**<br>**_Typ_** | Použít | popis |
| --- | --- | --- |
| **ID entity úrovně hodnocení**<br>mshr_hcmratinglevelentityid<br>*GUID* | Jen pro čtení<br>Povinná<br>Generováno systémem | Systémem generovaný jedinečný identifikátor úrovně. |
| **ID úrovně hodnocení**<br>mshr_ratinglevelid<br>*Řetězec* | Čtení/zápis<br>Povinná | Jedinečný, uživatelem čitelný identifikátor úrovně. |
| **ID modelu hodnocení**<br>mshr_ratingmodelid<br>*Řetězec* | Čtení/zápis<br>Povinná | Model hodnocení, ke kterému patří úroveň hodnocení. |
| **ID entity modelu hodnocení**<br>_mshr_fk_ratingmodelentity_id_value<br>*GUID* | Jen pro čtení<br>Povinná<br>Cizí klíč: mshr_hcmratingmodelentityid entity mshr_hcmratingmodelentity | Systémem generovaný identifikátor pro model hodnocení, ke kterému patří úroveň hodnocení. |
| **Popis**<br>mshr_description<br>*Řetězec* | Čtení/zápis<br>Povinná | Popis vybrané úrovně hodnocení. |
| **Koeficient**<br>mshr_factor<br>*Celé číslo* | Čtení/zápis<br>Povinná | Koeficient pro úroveň hodnocení. Při porovnání položek s různým počtem úrovní hodnocení je možné vyrovnávat stav pomocí koeficientu. Hodnota musí být celé číslo mezi 0 a 9. |
| **Poznámka**<br>mshr_note<br>*Řetězec* | Čtení/zápis<br>Volitelné | Jakékoli poznámky přidružené k úrovni hodnocení. |
| **Primární pole**<br>mshr_primaryfield<br>*Řetězec* | Jen pro čtení<br>Povinná | Pole, které se použije jako identifikátor záznamu entity. Kombinace ID úrovně hodnocení a ID modelu hodnocení. |

## <a name="see-also"></a>Viz také

[Úvod do rozhraní API pro integraci systému sledování žadatelů](hr-admin-integration-ats-api-introduction.md)<br>
[Příklad dotazu pro entitu Kandidát k přijetí](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

