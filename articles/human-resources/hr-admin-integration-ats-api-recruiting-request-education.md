---
title: Požadavek na vzdělání při náboru
description: Toto téma popisuje vzdělávací entitu Dynamics 365 Human Resources požadavek na vzdělání.
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
ms.openlocfilehash: 1767edfe67f9c3af4ac67eb5403d63a7f54dcac8
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126067"
---
# <a name="recruiting-request-education"></a>Požadavek na vzdělání při náboru

Toto téma popisuje vzdělávací entitu Dynamics 365 Human Resources požadavek na vzdělání.

Fyzický název: mshr_hcmrecruitingrequesteducationentity

### <a name="description"></a>popis

Popisuje požadavky na vzdělání pro RecruitingRequest.

### <a name="json-representation"></a>JSON reprezentace

```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_educationdisciplineid": "String",
    "mshr_educationdisciplinedescription": "String",
    "mshr_educationlevelid": "String",
    "mshr_educationleveldescription": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_educationdiscipline_id_value": "Guid",
    "_mshr_fk_educationlevel_id_value": "Guid",
    "mshr_hcmrecruitingrequesteducationentityid": "Guid"
}
```

### <a name="properties"></a>Vlastnosti

| Vlastnost<br>**Fyzický název**<br>**_Typ_** | Použít | popis |
| --- | --- | --- |
| **ID entity požadavku na vzdělání**<br>mshr_hcmrecruitingrequesteducationentityid<br>*GUID* | Jen pro čtení<br>Povinná | Systémem generovaný jedinečný identifikátor pro záznam Požadavku na vzdělání |
| **ID požadavku na nábor**<br>mshr_recruitingrequestid<br>*Řetězec* | Zapisovatelné jednou<br>Povinná | Uživatelsky čitelný jedinečný identifikátor souvisejícího požadavku na nábor. |
| **Hodnota ID požadavku na nábor**<br>_mshr_fk_recruitingrequest_id_value<br>*GUID* | Jen pro čtení<br>Povinná<br>Cizí klíč: mshr_hcmrecruitingrequestentityid entity mshr_hcmrecruitingrequestentity | Systémem generovaný jedinečný identifikátor souvisejícího požadavku na nábor. |
| **ID úrovně vzdělání**<br>mshr_educationlevelid<br>*Řetězec* | Zapisovatelné jednou<br>Povinná | Požadovaná úroveň vzdělání. |
| **Hodnota ID úrovně vzdělání**<br>_mshr_fk_educationlevel_id_value<br>*GUID* | Jen pro čtení<br>Povinná<br>Cizí klíč: mshr_hcmeducationlevelentityid entity mshr_hcmeducationlevelentity | Systémem generovaný jedinečný identifikátor požadované úrovně vzdělání. |
| **Popis úrovně vzdělání**<br>mshr_educationleveldescription<br>*Řetězec* | Jen pro čtení<br>Povinná | Popis úrovně požadované pro danou dovednost. |
| **ID oboru vzdělání**<br>mshr_educationdisciplinedescription<br>*Řetězec* | Zapisovatelné jednou<br>Povinná | Přesná oblast vzdělání. |
| **Hodnota ID oboru vzdělání**<br>_mshr_fk_educationdiscipline_id_value<br>*GUID* | Jen pro čtení<br>Povinná<br>Cizí klíč: mshr_hcmeducationdisciplineentityid entity mshr_hcmeducationdisciplineentity | Systémem generovaný jedinečný identifikátor požadovaného přesné oblasti vzdělání. |
| **Popis oboru vzdělání**<br>mshr_educationdisciplinedescription<br>Řetězec | Jen pro čtení<br>Povinná | POpis přesné oblasti vzdělání. |
| **ID datové oblasti**<br>mshr_dataareaid<br>*Řetězec* | Čtení/zápis<br>Volitelné | Určuje právnickou osobu (společnost).|
| **Hodnota ID datové oblasti**<br>_mshr_dataareaid_id_value<br>*GUID* | Jen pro čtení<br>Volitelné<br>Cizí klíč: cdm_companyid entity cdm_company | Systémem generovaná hodnota GUID identifikující právnickou osobu (společnost). |
| **Primární pole**<br>mshr_primaryfield<br>*Řetězec* | Jen pro čtení<br>Povinná | Zřetězení hodnoty požadavku na nábor, ID úrovně vzdělání a ID vzdělávací disciplíny jako další metoda k jedinečné identifikaci záznamu. |

## <a name="see-also"></a>Viz také

[Úvod do rozhraní API pro integraci systému sledování žadatelů](hr-admin-integration-ats-api-introduction.md)<br>
[Příklad dotazu na žádost o nábor](hr-admin-integration-ats-api-recruiting-request-example-query.md)

