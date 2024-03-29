---
title: Příklad dotazu pro entitu Kandidát k přijetí
description: Tento článek poskytuje ukázkový dotaz pro entitu Kandidát k přijetí v Dynamics 365 Human Resources.
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
ms.openlocfilehash: 2dd744665d4f0b6c64f4ee45a01c237081018514
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848335"
---
# <a name="example-query-for-candidate-to-hire"></a>Příklad dotazu pro entitu Kandidát k přijetí


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tento článek poskytuje ukázkový dotaz pro entitu Kandidát k přijetí v Dynamics 365 Human Resources.

Tento článek poskytuje příklad, který ukazuje, jak můžete použít *hluboké vložení* k vytvoření všech podrobností záznamu nového kandidáta v jediné operaci rozhraní API. Další informace o hlubokém vložení najdete v části [Vytvoření záznamů související entity v jedné operaci](/powerapps/developer/data-platform/webapi/create-entity-web-api#create-related-entity-records-in-one-operation).

Entita **mshr_hcmcandidatetohireentity** je jedinečná svým vztahem k entitě **mshr_dirpersonentity**. Mnoho vlastností entity **mshr_hcmcandidatetohireentity** (například **mshr_firstname**, **mshr_lastname** a **mshr_birthdate**) je odvozeno ze záznamu **mshr_dirpersonentity**. Pokud zveřejníte záznam nového kandidáta v entitě **mshr_hcmcandidatetohireentity** bez použití hlubokého vložení, můžete definovat hodnoty těchto vlastností přímo v záznamu **mshr_hcmcandidatetohireentity**. Přidružený záznam **mshr_dirpersonentity** je vytvořen implicitně s definovanými hodnotami vlastností. Poté můžete vytvořit jakékoli další záznamy souvisejících entit (například dovednosti nebo vzdělání) jako samostatná volání rozhraní API.

Pokud však chcete použít hluboké vložení k vytvoření všech souvisejících entit v jedné operaci, vlastnosti specifické pro entitu **mshr_dirpersonentity** musí být definovány na této vnořené úrovni operace.

Tento příklad ukazuje, jak můžete vytvořit záznam kandidáta, záznam přidružené osoby a dovednosti a vzdělání dané osoby ve třech vnořených úrovních pomocí hlubokého vložení v jedné operaci rozhraní API.

> [!NOTE]
> Příklad se netýká všech vlastností každé z entit rozhraní API. Je zjednodušen pro demonstrativní účely.

**Žádost**

```http

POST [Organization URI]/api/data/v9.1/mshr_hcmcandidatetohireentities
Content-Type: application/json; charset=utf-8
OData-MaxVersion: 4.0
OData-Version: 4.0
Accept: application/json

{
    "mshr_dataareaid": "usmf",
    "mshr_recruitingrequestid": "USMF-000141",
    "mshr_positionid": "000601",
    "mshr_iswillingtorelocate": 200000000,
    "mshr_availabilitydate": "2021-03-18",
    "mshr_comments": "Evelyn's experience is exactly what we need for this position.",
    "mshr_FK_Person_id":
        {
            "mshr_firstname": "Evelyn",
            "mshr_lastname": "Chambers",
            "mshr_namesequencedisplayas": "FirstMiddleLast",
            "mshr_FK_HcmPersonSkillEntity_Person":
            [
                {
                    "mshr_skillid": "CustFocus",
                    "mshr_ratingid": "Skills",
                    "mshr_levelid": "4",
                    "mshr_ratinglevelexaminer": "",
                    "mshr_leveltype": 200000000,
                    "mshr_yearsofexperience": 0,
                    "mshr_verified": 200000000,
                    "mshr_leveldate": "2013-01-01T00:00:00Z"
                },
                {
                    "mshr_skillid": "CashFlow",
                    "mshr_ratingid": "Skills",
                    "mshr_levelid": "4",
                    "mshr_ratinglevelexaminer": "",
                    "mshr_leveltype": 200000000,
                    "mshr_yearsofexperience": 0,
                    "mshr_verified": 200000000,
                    "mshr_leveldate": "2013-01-01T00:00:00Z"
                }
            ],
            "mshr_FK_HcmPersonEducationEntity_Person": [
                {
                    "mshr_creditbasis": 200000000,
                    "mshr_enddate": "2021-02-22T00:00:00Z",
                    "mshr_educationlevelid": "Bachelor",
                    "mshr_creditsearned": 0,
                    "mshr_startdate": "2017-02-21T00:00:00Z",
                    "mshr_creditscompleted": 0,
                    "mshr_educationinstitutionid": "Cottonwood Univ",
                    "mshr_educationdisciplineid": "Business Mgmt",
                    "mshr_durationunit": 200000000
                }              
            ]
        }
}
```

**Odezva**

```http

HTTP/1/1 204 No Content
OData-Version: 4.0
OData-EntityId: [Organization URI]/api/data/v9.1/mshr_hcmcandidatetohireentities(00000d2d-0000-0000-7317-005001000000)

```

## <a name="see-also"></a>Viz také

[Úvod do rozhraní API pro integraci systému sledování žadatelů](hr-admin-integration-ats-api-introduction.md)<br>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
