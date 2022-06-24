---
title: Vzdělání osoby
description: Tento článek popisuje entitu Vzdělání osoby pro Dynamics 365 Human Resources.
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
ms.openlocfilehash: 0fbbb467852d2aeb070c7732c9aa3108fd504de0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893896"
---
# <a name="person-education"></a>Vzdělání osoby


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tento článek popisuje entitu Vzdělání osoby pro Dynamics 365 Human Resources.

Fyzický název: mshr_hcmpersoneducationentity

## <a name="description"></a>popis

Tato entita obsahuje historii vzdělávání osoby, která je kandidátem. Vzdělání je spojeno s osobním záznamem, což umožňuje, aby bylo vzdělání přidruženo k jakýmkoli dalším rolím vytvořeným pro danou osobu dodatečně k záznamu o kandidátovi (pracovník, dodavatel atd.).

## <a name="json-representation"></a>Kód JSON

```json
{
    "mshr_creditbasis": Int,
    "mshr_creditscompleted": Decimal,
    "mshr_creditsearned": Decimal,
    "mshr_creditsneeded": Decimal,
    "mshr_description": "String",
    "mshr_duration": Decimal,
    "mshr_durationunit": Int,
    "mshr_educationdisciplineid": "String",
    "mshr_educationinstitutionid": "String",
    "mshr_educationlevelid": "String",
    "mshr_enddate": "Date",
    "mshr_gradepointaverage": Decimal,
    "mshr_gradescale": "String",
    "mshr_notes": "String",
    "mshr_secondaryemphasis": "String",
    "mshr_startdate": "Date",
    "mshr_partynumber": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_educationdiscipline_id_value": "Guid",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_educationinstitution_id_value": "Guid",
    "_mshr_fk_educationlevel_id_value": "Guid",
    "mshr_hcmpersoneducationentityid": "Guid"
}
```

## <a name="properties"></a>Vlastnosti

| Vlastnost<br>**Fyzický název**<br>**_Typ_** | Použít | popis |
| --- | --- | --- |
| **ID entity Vzdělání osoby**<br>mshr_hcmpersoneducationentityid<br>*GUID* | Jen pro čtení<br>Povinná | Systémem generovaný jedinečný identifikátor pro záznam entity vzdělání osoby. |
| **Číslo strany**<br>mshr_partynumber<br>*Řetězec* | Čtení/zápis<br>Povinná | Jedinečný identifikátor záznamu strany (osoby) pro kandidáta. |
| **Hodnota ID osoby**<br>_mshr_fk_person_id_value<br>*GUID* | Jen pro čtení<br>Povinná<br>Cizí klíč: mshr_dirpersonentityid entity mshr_dirpersonentity | Systémem generovaný jedinečný identifikátor pro záznam osoby kandidáta. |
| **Základ kreditů**<br>mshr_creditbasis<br>*Sada možností mshr_hcmeducationcreditbasis* | Čtení/zápis<br>Volitelné | Základ kreditů pro stupeň vzdělání. |
| **Splněné kredity**<br>mshr_creditscompleted<br>*Des. místo* | Čtení/zápis<br>Volitelné | Počet kreditů získaných za vzdělávání. |
| **Získané kredity**<br>mshr_creditsearned<br>*Des. místo* | Čtení/zápis<br>Volitelné | Počet kreditů získaných pro záznam vzdělání u probíhajícího stupně vzdělání. |
| **Potřebné kredity**<br>mshr_creditsneededed<br>*Des. místo* | Čtení/zápis<br>Volitelné | Počet kreditů požadovaných pro probíhající stupeň vzdělání. |
| **Popis**<br>mshr_description<br>*Řetězec* | Čtení/zápis<br>Volitelné | Popis stupně vzdělání kandidáta. |
| **ID úrovně vzdělání**<br>mshr_educationlevelid<br>*Řetězec* | Čtení/zápis<br>Volitelné | ID úrovně vzdělání. | 
| **Hodnota ID úrovně vzdělání**<br>_mshr_fk_educationlevel_id_value<br>*GUID* | Jen pro čtení<br>Volitelné<br>Cizí klíč: mshr_hcmeducationdegreeentityid entity mshr_hcmeducationdegreeentity | Systémem generovaný jedinečný identifikátor pro záznam stupně vzdělání. Tento identifikátor poskytuje stupně a úrovně vzdělání definované pro organizaci. |
| **ID oboru vzdělání**<br>mshr_educationdisciplineid<br>*Řetězec* | Čtení/zápis<br>Povinná<br>Cizí klíč: EducationDiscipline | ID oboru vzdělání. |
| **Hodnota ID oboru vzdělání**<br>_mshr_fk_educationdiscipline_id_value<br>*GUID* | Jen pro čtení<br>Povinná<br>Cizí klíč: mshr_hcmeducationdisciplineentityid entity mshr_hcmeducationdisciplineentity | Systémem generovaný jedinečný identifikátor oboru vzdělání pro záznam vzdělání. |
| **Druhotný důraz**<br>mshr_secondaryemphasis<br>*Řetězec* | Čtení/zápis<br>Volitelné | Sekundární důraz získaného stupně vzdělání. |
| **ID vzdělávací instituce**<br>mshr_educationinstitutionid<br>*Řetězec* | Čtení/zápis<br>Volitelné | ID navštěvované vzdělávací instituce. |
| **Hodnota ID vzdělávací instituce**<br>_mshr_fk_educationinstitution_id_value<br>*GUID* | Jen pro čtení<br>Volitelné<br>Cizí klíč: mshr_hcmeducationinstitutionentityid entity mshr_hcmeducationinstitutionentity | Systémem generovaný identifikátor vzdělávací instituce. |
| **Počáteční datum**<br>mshr_startdate<br>*Datum a čas* | Čtení/zápis<br>Volitelné | Počáteční datum vzdělávání pro získaný stupeň vzdělání. |
| **Koncové datum**<br>mshr_enddate<br>*Datum a čas* | Čtení/zápis<br>Povinná | Datum vystavení referencí. |
| **Doba trvání**<br>mshr_duration<br>*Des. místo* | Čtení/zápis<br>Volitelné | Doba trvání záznamu o vzdělání. |
| **Jednotka doby trvání**<br>mshr_durationunit<br>*Sada možností mshr_periodunit* | Čtení/zápis<br>Volitelné | Jednotka času přidružená k době trvání záznamu o vzdělání. |
| **Průměr školních známek**<br>mshr_gradepointaverage<br>*Des. místo* | Čtení/zápis<br>Volitelné | Získaný průměr studijních výsledků pro daný stupeň vzdělání. |
| **Klasifikační stupnice**<br>mshr_gradescale<br>*Řetězec* | Čtení/zápis<br>Volitelné | Stupnice použitá pro průměr studijních výsledků. |
| **Poznámky**<br>mshr_notes<br>*Řetězec* | Čtení/zápis<br>Volitelné | Poznámky určené pro náboráře nebo manažery náboru. |
| **Primární pole**<br>mshr_primaryfield<br>*Řetězec* | Jen pro čtení<br>Povinná | Pole použité jako další primární identifikátor záznamu entity. Kombinace čísla strany, ID ooru vzdělání, ID vzdělávací instituce a ID úrovně vzdělání. |

## <a name="see-also"></a>Viz také

[Úvod do rozhraní API pro integraci systému sledování žadatelů](hr-admin-integration-ats-api-introduction.md)<br>
[Příklad dotazu pro entitu Kandidát k přijetí](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
