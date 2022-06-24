---
title: Pozice požadavků na nábor
description: Tento článek popisuje entitu pozici žádosti o nábor Dynamics 365 Human Resources.
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
ms.openlocfilehash: 0996532edf09ea5159e143d92fb2a93c4d6f826d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904239"
---
# <a name="recruiting-request-position"></a>Pozice požadavků na nábor


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tento článek popisuje entitu pozici žádosti o nábor Dynamics 365 Human Resources.

Fyzický název: mshr_hcmrecruitingrequestpositionentity

### <a name="description"></a>popis

Popisuje pozici nebo pozice, které se mají vyplnit pro požadavek na nábor. Přidání pozice k požadavku na nábor je volitelné. Vlastnosti pozice jsou jen pro čtení, protože vlastnosti pozice by se neměly lišit v požadavku na nábor, než jsou v hlavním záznamu pozice. Pokud se vlastnosti musí změnit, mělo by to být provedeno v hlavním záznamu polohy před přidáním pozice do požadavku na nábor.

### <a name="json-representation"></a>JSON reprezentace
```json
{
    "mshr_recruitingrequestid": "String",
    "mshr_positionid": "String",
    "mshr_description": "String",
    "mshr_positiontypeid": "String",
    "mshr_status": Int,
    "mshr_departmentnumber": "String",
    "mshr_reportstopositionid": "String",
    "mshr_reportstopersonnelnumber": "String",
    "mshr_financialdimension": "String",
    "mshr_dataareaid": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_primaryfield": "String",
    "_mshr_fk_recruitingrequest_id_value": "Guid",
    "_mshr_fk_position_id_value": "Guid",
    "_mshr_fk_positiontype_id_value": "Guid",
    "_mshr_fk_department_id_value": "Guid",
    "_mshr_fk_reportstoposition_id_value": "Guid",
    "_mshr_fk_reportstoworker_id_value": "Guid",
    "mshr_hcmrecruitingrequestpositionentityid": "Guid"
}
```

### <a name="properties"></a>Vlastnosti

| Vlastnost<br>**Fyzický název**<br>**_Typ_** | Použít | popis |
| --- | --- | --- |
| **ID entity pozice žádosti**<br>mshr_hcmrecruitingrequestpositionentityid<br>*GUID* | Jen pro čtení<br>Povinná |    Systémem generovaný identifikátor záznamu pozice požadavku na nábor. |
| **ID požadavku na nábor**<br>mshr_recruitingrequestid<br>*Řetězec* | Zapisovatelné jednou<br>Povinná | Uživatelsky čitelný jedinečný identifikátor požadavku na nábor. |
| **Hodnota ID požadavku na nábor**<br>_mshr_fk_recruitingrequest_id_value<br>*GUID* | Jen pro čtení<br>Povinná<br>Cizí klíč: mshr_hcmrecruitingrequestentityid entity mshr_hcmrecruitingrequestentity | Systémem generovaný identifikátor záznamu požadavku na nábor, ke kterému je pozice přidělena. |
| **ID pozice**<br>mshr_positionid<br>*Řetězec* | Zapisovatelné jednou<br>Povinná | Uživatelsky čitelný jedinečný identifikátor pozice. |
| **Hodnota ID pozice**<br>_mshr_fk_position_id_value<br>*GUID* | Jen pro čtení<br>Povinná<br>Cizí klíč: mshr_hcmpositionv2entityid entity mshr_hcmpositionv2entity | Systémem generovaný identifikátor pozice. |
| **Popis**<br>mshr_description<br>*Řetězec* | Jen pro čtení<br>Povinná | Popis pozice. |
| **ID typu pozice**<br>mshr_positiontypeid<br>*Řetězec* | Jen pro čtení<br>Volitelné | Uživatelsky čitelný jedinečný identifikátor typu pozice pro tuto pozici. |
| **Hodnota ID typu pozice**<br>_mshr_fk_positiontype_id_value<br>*GUID* | Jen pro čtení<br>Volitelné<br>Cizí klíč: mshr_hcmpositiontypeentityid entity mshr_hcmpositiontypeentity | Systémem generovaný jedinečný identifikátor typu pozice pro tuto pozici. |
| **Stav**<br>mshr_status<br>Sada možností *RecruitingRequestPositionStatus* | Čtení/zápis<br>Povinná | Stav pozice pro tuto žádost na nábor. |
| **Číslo oddělení**<br>mshr_departmentnumber<br>*Řetězec* | Jen pro čtení<br>Volitelné<br> | Číslo oddělení pozice. |
| **Hodnota ID oddělení**<br>_mshr_fk_department_id_value<br>*GUID* | Jen pro čtení<br>Volitelné<br>Cizí klíč: mshr_omdepartmententityid entity mshr_omdepartmententity | Systémem generovaný jedinečný identifikátor oddělení pozice. |
| **ID podřízených pozici**<br>mshr_reportstopositionid<br>*Řetězec* | Jen pro čtení<br>Povinná | Uživatelsky čitelné ID pozice, na kterou se rekrutovaná pozice hlásí v hierarchii organizace. |
| **Hodnota ID podřízených pozici**<br>_mshr_fk_reportstoposition_id_value<br>*GUID* | Jen pro čtení<br>Povinná<br>Cizí klíč: mshr_hcmpositionv2entityid entity mshr_hcmpositionv2entity | Systémem generované ID pozice, na kterou se rekrutovaná pozice hlásí. |
| **Podřízení osobního čísla**<br>mshr_reportstopersonnelnumber<br>*Řetězec* | Jen pro čtení<br>Povinná | ID pracovníka, kterému bude najatý kandidát podřízený. |
| **Hodnota ID podřízených pracovníků**<br>_mshr_fk_reportstoworker_id_value<br>*GUID* | Jen pro čtení<br>Povinná<br>Cizí klíč: mshr_hcmworkerbaseentityid entity mshr_hcmworkerbaseentity | Systémem generované ID pracovníka, kterému bude najatý kandidát podřízený. |
| **Finanční dimenze**<br>mshr_financialdimension<br>*Řetězec* | Jen pro čtení<br>Volitelné | Finanční dimenze (například nákladové středisko) přiřazená pozici. Finanční dimenze je přiřazena každé pozici podle právnické osoby. Nákladová střediska, která jsou definována v dimenzích, jsou přístupná prostřednictvím entity mshr_dimattributeomcostcenterentity. |
| **ID datové oblasti**<br>mshr_dataareaid<br>*Řetězec* | Čtení/zápis<br>Volitelné | Určuje právnickou osobu (společnost) pro pozici požadavku na nábor. |
| **Hodnota ID datové oblasti**<br>_mshr_dataareaid_id_value<br>*GUID* | Jen pro čtení<br>Volitelné<br>Cizí klíč: cdm_companyid entity cdm_company | Systémem generovaná hodnota GUID identifikující právnickou osobu (společnost) pro pozici požadavku na nábor. |
| **Primární pole**<br>mshr_primaryfield<br>*Řetězec* | Jen pro čtení<br>Povinná | Zřetězení hodnoty požadavku na nábor, ID pozice a ID vzdělávací disciplíny jako další metoda k jedinečné identifikaci záznamu. |

## <a name="see-also"></a>Viz také

[Úvod do rozhraní API pro integraci systému sledování žadatelů](hr-admin-integration-ats-api-introduction.md)<br>
[Příklad dotazu na žádost o nábor](hr-admin-integration-ats-api-recruiting-request-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
