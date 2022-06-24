---
title: Požadavky na dovednosti pro nábor
description: Tento článek popisuje entitu požadované dovednosti pro nábor Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b17bbdfbc977112344302deada085681ceca9bb6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8856389"
---
# <a name="recruiting-request-skill"></a>Požadavky na dovednosti pro nábor


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tento článek popisuje entitu požadované dovednosti pro nábor Dynamics 365 Human Resources.

Fyzický název: mshr_hcmrecruitingrequestskillentity

### <a name="description"></a>popis

Popisuje požadavky na dovednosti pro RecruitingRequest.

### <a name="json-representation"></a>JSON reprezentace

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_skillid": "String",
    "mshr_skilldescription": "String",
    "mshr_ratinglevelid": "String",
    "mshr_ratingmodelid": "String",
    "mshr_ratingleveldescription": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_skill_id_value": "Guid",
    "_mshr_fk_ratinglevel_id_value": "Guid",
    "_mshr_fk_ratingmodel_id_value": "Guid",
    "mshr_hcmrecruitingrequestskillentityid": "Guid"
}
```

### <a name="properties"></a>Vlastnosti

| Vlastnost<br>**Fyzický název**<br>**_Typ_** | Použít | popis |
| --- | --- | --- |
| **ID entity požadovaných zkušeností**<br>mshr_hcmrecruitingrequestskillentityid<br>*GUID* | Jen pro čtení<br>Povinná | Systémem generovaný jedinečný identifikátor pro **Záznam požadavku na dovednosti**. |
| **ID požadavku na nábor**<br>mshr_recruitingrequestid<br>*Řetězec* | Zapisovatelné jednou<br>Povinná | Uživatelsky čitelný jedinečný identifikátor přiřazeného požadavku na nábor. |
| **Hodnota ID požadavku na nábor**<br>_mshr_fk_recruitingrequest_id_value<br>*GUID* | Jen pro čtení<br>Povinná<br> Cizí klíč: mshr_hcmrecruitingrequestentityid entity mshr_hcmrecruitingrequestentity | Systémem generovaný jedinečný identifikátor přiřazeného požadavku na nábor. |
| **ID dovednosti**<br>mshr_skillid<br>*Řetězec*<br> | Zapisovatelné jednou<br>Povinná | Uživatelsky čitelný jedinečný identifikátor požadavku na dovednosti. |
| **Hodnota ID dovednosti**<br>_mshr_fk_skill_id_value<br>*GUID* | Jen pro čtení<br>Povinná<br>Cizí klíč: mshr_hcmskillentityid entity mshr_hcmskillentity | Systémem generovaný jedinečný identifikátor požadované dovednosti. |
| **ID úrovně hodnocení**<br>mshr_ratinglevelid<br>*Řetězec* | Zapisovatelné jednou<br>Volitelné | Požadovaná hodnota úrovně dovednosti vybraná pro úlohu na základě modelu hodnocení přiřazeného ke dovednosti. |
| **Hodnota ID úrovně hodnocení**<br>_mshr_fk_ratinglevel_id_value<br>*GUID* | Jen pro čtení<br>Volitelné<br>Cizí klíč: mshr_hcmratinglevelentityid entity mshr_hcmratinglevelentity | Systémem generovaný jedinečný identifikátor úrovně. |
| **Popis dovednosti**<br>mshr_skilldescription<br>*Řetězec* | Jen pro čtení<br>Povinná | Popis dovednosti. |
| **Popis úrovně hodnocení**<br>mshr_ratingleveldescription<br>*Řetězec* | Jen pro čtení<br>Volitelné | Popis vybrané úrovně dovednosti. |
| **ID datové oblasti**<br>mshr_dataareaid<br>*Řetězec* | Čtení/zápis<br>Volitelné | Určuje právnickou osobu (společnost). |
| **Hodnota ID datové oblasti**<br>_mshr_dataareaid_id_value<br>*GUID* | Jen pro čtení<br>Volitelné<br>Cizí klíč: cdm_companyid entity cdm_company | Systémem generovaná hodnota GUID identifikující právnickou osobu (společnost). |
| **Primární pole**<br>mshr_primaryfield<br>*Řetězec* | Jen pro čtení<br>Povinná | Zřetězení hodnoty požadavku na nábor, ID dovednosti a ID vzdělávací disciplíny jako další metoda k jedinečné identifikaci záznamu. |
| **ID modelu hodnocení**<br>mshr_ratingmodelid<br>*Řetězec* | Čtení-zápis<br>Povinná | Model hodnocení používaný k hodnocení dovednosti. |
| **Hodnota ID modelu hodnocení**<br>_mshr_fk_hcmratingmodel_id_value<br>*GUID* | Jen pro čtení<br>Povinná<br>Cizí klíč: mshr_hcmratingmodelentityid entity mshr_hcmratingmodelentity | Systémem generovaný jedinečný identifikátor ratingového modelu použitého k ohodnocení dovednosti. |

## <a name="see-also"></a>Viz také

[Úvod do rozhraní API pro integraci systému sledování žadatelů](hr-admin-integration-ats-api-introduction.md)<br>
[Příklad dotazu na žádost o nábor](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
