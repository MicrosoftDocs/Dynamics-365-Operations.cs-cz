---
title: Kandidát k přijetí
description: Toto téma popisuje entitu Kandidát k přijetí pro Dynamics 365 Human Resources.
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
ms.openlocfilehash: aef9f4889d17811026fc36091bb98494412dacd898f847ac661333628e8e32e7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742817"
---
# <a name="candidate-to-hire"></a>Kandidát k přijetí

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Toto téma popisuje entitu Kandidát k přijetí pro Dynamics 365 Human Resources.

Fyzický název: mshr_hcmcandidatetohireentity

## <a name="description"></a>popis

Tato entita poskytuje podrobnosti o kandidátovi použité k vytvoření pracovníka v Dynamics 365 Human Resources. Používá se ke čtení všech záznamů kandidátů a vytváření interních a externích záznamů kandidátů, což vám umožňuje vytvářet osobní údaje pro nového kandidáta.

Když vytvoříte záznam externího kandidáta, který bude v systému záznamem nové osoby, nemusíte definovat číslo strany (osoby) pro záznam nového kandidáta. Záznam entity nové osoby je vytvořen se záznamem nového kandidáta.

Když vytvoříte interní záznam kandidáta (kandidát na pozici, který již má ve společnosti záznam zaměstnance), definujte číslo strany (osoby) záznamu, který již existuje pro osobu pro vlastnost mshr_partynumber v záznamu kandidáta, místo definování osobních údajů (například jméno, pohlaví nebo datum narození), které by byly použity k vytvoření nového záznamu osoby.

## <a name="json-representation"></a>Kód JSON

```json
        {
            "mshr_candidateid": "String",
            "mshr_partynumber": "String",
            "mshr_partytype": "String",
            "mshr_recruitingrequestid": "String",
            "mshr_positionid": "String",
            "mshr_firstname": "String",
            "mshr_middlename": "String",
            "mshr_lastnameprefix": "String",
            "mshr_lastname": "String",
            "mshr_gender": Int,
            "mshr_birthdate": "Date",
            "mshr_citizenshipcountrycode": "String",
            "mshr_veteranstatusid": "String",
            "mshr_isdisabledveteran": Int,
            "mshr_availabilitydate": "Date",
            "mshr_iswillingtorelocate": Int,
            "mshr_comments": "String",
            "mshr_applicantintegrationresult": Int,
            "mshr_donothirereasoncodeid": "String",
            "mshr_dataareaid": "String",
            "_mshr_dataareaid_id_value": "Guid",
            "_mshr_fk_person_id_value": "Guid",
            "_mshr_fk_recruitingrequest_id_value": "Guid",
            "_mshr_fk_position_id_value": "Guid",
            "mshr_hcmcandidatetohireentityid": "Guid",
            "_mshr_fk_veteranstatus_id_value": "Guid",
            "_mshr_fk_reasoncode_id_value": "Guid",
            "mshr_militaryserviceenddate": "Guid",
            "mshr_militaryservicestartdate": "Guid"
        }
```

## <a name="properties"></a>Vlastnosti

| Vlastnost<br>**Fyzický název**<br>**_Typ_** | Použít | popis |
| --- | --- | --- |
| **ID entity Kandidát k přijetí**<br>mshr_hcmcandidatetohireentityid<br>GUID | Jen pro čtení<br>Povinná<br>Generováno systémem | Systémem generovaný jedinečný identifikátor pro záznam entity. |
| **ID kandidáta**<br>mshr_candidateid<br>Řetězec | Jen pro čtení<br>Povinná<br>Generováno systémem | Jedinečný identifikátor entity. |
| **Číslo strany**<br>mshr_partynumber<br>Řetězec | Jen pro čtení<br>Povinná | Číslo strany (osoby) záznamu osoby kandidáta. |
| **Hodnota ID osoby**<br>_mshr_fk_person_id_value<br>GUID | Jen pro čtení<br>Povinná<br>Cizí klíč: mshr_dirpersonentityid entity mshr_direpersonentity | Systémem generovaný jedinečný identifikátor pro záznam strany (osoby) kandidáta. |
| **Typ strany**<br>mshr_partytype<br>Sada možností mshr_dirpartytype | Jen pro čtení<br>Povinná | Typ strany záznamu, jak je definován v sadě možností mshr_dirpartytype. U této entity bude typ vždy „Osoba“. |
| **ID požadavku na nábor**<br>mshr_recruitingrequestid<br>Řetězec | Jeden zápis<br>Volitelné | Odkazy na žádost o nábor, kterou tento kandidát splňuje. |
| **Hodnota ID požadavku na nábor**<br>_mshr_fk_recruitingrequest_id_value<br>GUID | Čtení/zápis<br>Volitelné<br>Cizí klíč: mshr_hcmrecruitingrequestentityid entity mshr_hcmrecruitingrequestentity | Systémem generovaný jedinečný identifikátor žádosti o nábor, kterou tento kandidát splňuje. |
| **ID pozice**<br>mshr_positionid<br>Řetězec | Čtení/zápis<br>Volitelné | ID pozice, pro kterou je kandidát zvažován. |
| **Hodnota ID pozice**<br>_mshr_fk_position_if_value<br>GUID | Jen pro čtení<br>Volitelné<br>Cizí klíč: mshr_hcmpositionv2entityid entity mshr_hcmpositionv2entity | Systémem generovaný identifikátor pozice, pro kterou je kandidát zvažován. |
| **Jméno**<br>mshr_firstname<br>Řetězec | Čtení/zápis<br>Povinná | Křestní jméno kandidáta. |
| **Druhé jméno**<br>mshr_middlename<br>Řetězec | Čtení/zápis<br>Volitelné | Druhé jméno kandidáta. |
| **Předpona příjmení**<br>mshr_lastnameprefix<br>Řetězec | Čtení/zápis<br>Volitelné | Předpona příjmení kandidáta. |
| **Příjmení**<br>mshr_lastname<br>Řetězec | Čtení/zápis<br>Volitelné | Příjmení kandidáta. |
| **Rod**<br>mshr_gender<br>Sada možností mshr_hcmpersongender | Čtení/zápis<br>Volitelné | Pohlaví kandidáta. |
| **Datum narození**<br>mshr_birthdate<br>Datum a čas | Čtení/zápis<br>Volitelné | Datum narození kandidáta. |
| **Kód země státního občanství**<br>mshr_citizenshipcountrycode<br>Řetězec | Čtení/zápis<br>Volitelné | Určuje zemi, kde má kandidát občanství. Platné kódy zemí jsou v entitě mshr_logisticaddresscountryregionentity. |
| **ID statutu veterána**<br>mshr_veteranstatusid<br>Řetězec | Čtení/zápis<br>Volitelné | Označuje, že kandidát má status veterána. |
| **Hodnota ID statutu veterána**<br>_mshr_fk_veteranstatus_id_value<br>GUID | Jen pro čtení<br>Volitelné<br>Cizí klíč: mshr_hcmveteranstatusentityid entity mshr_hcmveteranstatusentity | Systémem generovaný jedinečný identifikátor pro záznam entity statutu veterána. |
| **Datum nástupu vojenské služby**<br>mshr_militaryservicestartdate<br>Datum a čas | Čtení/zápis<br>Volitelné | Počáteční datum vojenské služby kandidáta. |
| **Datum odchodu z vojenské služby**<br>mshr_militaryserviceenddate<br>Datum a čas | Čtení/zápis<br>Volitelné | Koncové datum vojenské služby kandidáta. |
| **Je válečný invalida**<br>mshr_isdisabledveteran<br>Sada možností mshr_noyes | Čtení/zápis<br>Volitelné | Označuje, že kandidát má status válečného invalidy. |
| **Datum dostupnosti**<br>mshr_availabilitydate<br>Datum a čas | Čtení/zápis<br>Volitelné | Nejbližší datum, kdy bude kandidát k dispozici pro práci. |
| **Je ochoten se přestěhovat**<br>mshr_iswillingtorelocate<br>Sada možností mshr_noyes | Čtení/zápis<br>Volitelné | Označuje, zda je kandidát ochoten se přestěhovat. |
| **Komentáře**<br>mshr_comments<br>Řetězec | Čtení/zápis<br>Volitelné | Komentáře, které použije náborář nebo náborový manažer. |
| **Výsledek integrace aplikace**<br>mshr_applcantintegrationresult<br>Sada možností mshr_applicantintegrationresult | Čtení/zápis<br>Povinná | Stav kandidáta během náborového procesu souvisejícího s integrací. |
| **ID kódu důvodu Nepřijmout**<br>mshr_donothirereasoncodeid<br>Řetězec | Čtení/zápis<br>Volitelné | Kód důvodu, který je volitelně zadán, když je stav (výsledek integrace aplikace) nastaven na „Nepřijatý“. |
| **Hodnota ID kódu důvodu**<br>_mshr_fk_reasoncode_id_value<br>GUID | Jen pro čtení<br>Volitelné<br>Cizí klíč: mshr_hcmreasoncodeentityid entity mshr_hcmreasoncodeentity | Systémem generovaný jedinečný identifikátor pro kód důvodu **Nepřijmout**. |
| **ID datové oblasti**<br>mshr_dataareaid<br>Řetězec | Čtení/zápis<br>Volitelné |  Určuje právnickou osobu (společnost). |
| **Hodnota ID datové oblasti**<br>_mshr_dataareaid_id_value<br>GUID | Jen pro čtení<br>Volitelné<br>Cizí klíč: cdm_companyid entity cdm_company | Systémem generovaná hodnota GUID identifikující právnickou osobu (společnost). |

## <a name="see-also"></a>Viz také

[Úvod do rozhraní API pro integraci systému sledování žadatelů](hr-admin-integration-ats-api-introduction.md)<br>
[Příklad dotazu pro entitu Kandidát k přijetí](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]