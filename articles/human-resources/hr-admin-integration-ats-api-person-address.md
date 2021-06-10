---
title: Adresa osoby
description: Toto téma popisuje entitu Adresa osoby pro Dynamics 365 Human Resources.
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
ms.openlocfilehash: 14db209e420770234583add93fa72d086f1b5ea6
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053772"
---
# <a name="person-address"></a>Adresa osoby

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Toto téma popisuje entitu Adresa osoby pro Dynamics 365 Human Resources.

Fyzický název: mshr_hcmpersonaddressentities

## <a name="description"></a>popis

Tato entita obsahuje seznam poštovních adres pro záznamy kandidátů.

## <a name="json-representation"></a>Kód JSON

```json
{
    "mshr_partynumber": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_roles": "String",
    "mshr_countryregionid": "String",
    "mshr_zipcode": "String",
    "mshr_street": "String",
    "mshr_city": "String",
    "mshr_state": "String",
    "mshr_county": "String",
    "mshr_isprimary": Int,
    "mshr_isprivate": Int,
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_countryregion_id_value": "Guid",
    "mshr_hcmpersonaddressentityid": "Guid"
}
```

## <a name="properties"></a>Vlastnosti

| Vlastnost<br>**Fyzický název**<br>**_Typ_** | Použít | popis |
| --- | --- | --- |
| **ID entity Adresa osoby**<br>mshr_hcmpersonaddressentityid<br>*Řetězec* | Jen pro čtení<br>Povinná | Systémem generovaný jedinečný identifikátor pro záznam entity. |
| **Číslo strany**<br>mshr_partynumber<br>*Řetězec* | Čtení/zápis<br>Povinná | ID záznamu přidružené strany (osoby). |
| **Hodnota ID osoby**<br>_mshr_fk_person_id_value<br>*GUID* | Jen pro čtení<br>Povinná<br>Cizí klíč: mshr_dirpersonentityid entity mshr_dirpersonentity | Systémem generovaný jedinečný identifikátor záznamu entity strany (osoby). |
| **ID umístění**<br>mshr_locationid<br>*Řetězec* | Čtení/zápis<br>Povinná | ID místa pro záznam adresy. Nastavte v entitě mshr_logisticspostaladdresslocationcdsentity. |
| **Popis**<br>mshr_description<br>*Řetězec* | Čtení/zápis<br>Povinná | Popis adresy kandidáta. |
| **Role**<br>mshr_roles<br>*Řetězec* | Čtení/zápis<br>Povinná | Role přiřazené k této adrese. Lze přiřadit i více rolí. Každá role musí být oddělena středníkem. Platné hodnoty obsažené v entitě mshr_logisticslocationroleentity. |
| **Ulice**<br>mshr_street<br>*Řetězec* | Čtení/zápis<br>Volitelné | Číslo popisné. |
| **Město**<br>mshr_city<br>*Řetězec* | Čtení/zápis<br>Volitelné | Město adresy. Nastavte v entitě v mshr_logisticsaddresscityentity. |
| **Kraj**<br>mshr_state<br>*Řetězec* | Čtení/zápis<br>Volitelné | Stát v adrese. Nastavte v entitě v mshr_logisticsaddressstateentity. |
| **Okres**<br>mshr_county<br>*Řetězec* | Čtení/zápis<br>Volitelné | Okres adresy. Nastavte v entitě v mshr_logisticsaddresscountyentity. |
| **PSČ**<br>mshr_zipcode<br>*Řetězec* | Čtení/zápis<br>Volitelné | PSČ v adrese. Nastavte v entitě v mshr_logisticsaddresspostalcodeentity. |
| **ID oblasti/země**<br>mshr_countryregionid<br>*Řetězec* | Čtení/zápis<br>Volitelné | Země či oblast adresy. |
| **Hodnota ID oblasti/země**<br>_mshr_fk_countriregion_id_value<br>*GUID* | Jen pro čtení<br>Volitelné<br>Cizí klíč: mshr_logisticaddresscountryregionentityid entity mshr_logisticsaddresscountryregionentity | Systémem generovaný jedinečný identifikátor země/oblasti v adrese. |
| **Je primární**<br>mshr_isprimary<br>*Sada možností mshr_noyes* | Čtení/zápis<br>Povinná | Určuje, zda je tato adresa primární adresou osoby s definovanou rolí. |
| **Je soukromá**<br>mshr_isprivate<br>*Sada možností mshr_noyes* | Čtení/zápis<br>Povinná | Určuje, zda je tato adresa soukromou adresou dané osoby. |
| **Primární pole**<br>mshr_primaryfield<br>*Řetězec* | Jen pro čtení<br>Povinná | Pole použité jako primární identifikátor záznamu entity. Kombinace čísla strany a ID místa. |

## <a name="see-also"></a>Viz také

[Úvod do rozhraní API pro integraci systému sledování žadatelů](hr-admin-integration-ats-api-introduction.md)<br>
[Příklad dotazu pro entitu Kandidát k přijetí](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]