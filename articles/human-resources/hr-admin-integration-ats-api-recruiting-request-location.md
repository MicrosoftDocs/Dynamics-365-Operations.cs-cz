---
title: Místo požadavku na nábor
description: Tento článek popisuje entitu umístění požadavku na vzdělání pro Dynamics 365 Human Resources.
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
ms.openlocfilehash: d31af9ab62db310b89fbc7a2d7099621b59a356d
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8893809"
---
# <a name="recruiting-request-location"></a>Místo požadavku na nábor


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tento článek popisuje entitu umístění požadavku na vzdělání pro Dynamics 365 Human Resources.

Fyzický název: mshr_hcmrecruitingrequestlocationentity

### <a name="description"></a>popis

Seznam míst definovaných jako místa, kde budou zaměstnanci náboru pracovat při najímání. Jedná se o místa vytvořená napříč právnickými osobami.

### <a name="json-representation"></a>JSON reprezentace

```
{
    "mshr_recruitingrequestlocationid": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_countryregionid": "String",
    "mshr_zipcode": "String",
    "mshr_street": "String",
    "mshr_city": "String",
    "mshr_state": "String",
    "mshr_county": "String",
    "mshr_telephone": "String",
    "mshr_email": "String",
    "mshr_internetaddress": "String",
    "_mshr_dataareaid_id_value": "Guid",
    "mshr_dataareaid": "String",
    "_mshr_fk_countryregion_id_value": "Guid",
    "mshr_hcmrecruitingrequestlocationentityid": "Guid"
}
```

### <a name="properties"></a>Vlastnosti

| Vlastnost<br>**Fyzický název**<br>**_Typ_** | Použít | popis |
| --- | --- | --- |
| **ID umístění**<br>mshr_locationid<br>*Řetězec* | Zapisovatelné jednou<br>Povinná | Systémem generovaný a uživatelsky čitelný identifikátor pro místo náboru. |
| **Místo požadavku na nábor**<br>mshr_recruitingrequestlocationid<br>*Řetězec* | Zapisovatelné jednou<br>Povinná | Uživatelem definovaný jedinečný identifikátor pro místo náboru. |
| **ID entity umístění žádosti**<br>mshr_hcmrecruitingrequestlocationentityid<br>*GUID* | Jen pro čtení<br>Povinná | Systémem generovaný jedinečný identifikátor pro záznam požadavku na vzdělání |
| **Popis**<br>mshr_description<br>*Řetězec* | Čtení/zápis<br>Povinná | Popis umístění |
| **ID oblasti/země**<br>mshr_countryregionid<br>*Řetězec* | Jen pro čtení<br>Volitelné | Určuje zemi nebo oblast, kde má kandidát občanství. |
| **Hodnota ID oblasti/země**<br>_mshr_fk_countriregion_id_value<br>*GUID* | Jen pro čtení<br>Volitelné<br>Cizí klíč: mshr_logisticaddresscountryregionentityid entity mshr_logisticsaddresscountryregionentity | Systémem generovaný jedinečný identifikátor země/oblasti v adrese. |
| **ZipCode**<br>mshr_zipcode<br>*Řetězec* | Jen pro čtení<br>Volitelné | PSČ. |
| **Ulice**<br>mshr_street<br>*Řetězec* | Jen pro čtení<br>Volitelné | Adresa ulice. |
| **Město**<br>mshr_city<br>*Řetězec* | Jen pro čtení<br>Volitelné | Město. |
| **Kraj**<br>mshr_state<br>*Řetězec* | Jen pro čtení<br>Volitelné | Stát nebo provincie. |
| **Okres**<br>mshr_county<br>*Řetězec* | Jen pro čtení<br>Volitelné | Okres. |
| **Telefon**<br>mshr_telephone<br>*Řetězec* | Čtení/zápis<br>Volitelné | Telefonní číslo místa konání. |
| **E-mail**<br>mshr_email<br>*Řetězec* | Čtení/zápis<br>Volitelné | E-mailová adresa. |
| **InternetAddress**<br>mshr_internetaddress<br>*Řetězec* | Čtení/zápis<br>Volitelné | URL pro web umístění. |
| **ID datové oblasti**<br>mshr_dataareaid<br>*Řetězec* | Čtení/zápis<br>Volitelné | Určuje právnickou osobu (společnost). |
| **Hodnota ID datové oblasti**<br>_mshr_dataareaid_id_value<br>*GUID* | Jen pro čtení<br>Volitelné<br>Cizí klíč: cdm_companyid entity cdm_company | Systémem generovaná hodnota GUID identifikující právnickou osobu (společnost). |

## <a name="see-also"></a>Viz také

[Úvod do rozhraní API pro integraci systému sledování žadatelů](hr-admin-integration-ats-api-introduction.md)<br>
[Příklad dotazu na žádost o nábor](hr-admin-integration-ats-api-recruiting-request-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
