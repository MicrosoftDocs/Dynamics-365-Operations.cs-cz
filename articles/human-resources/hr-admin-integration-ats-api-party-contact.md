---
title: Kontakt strany
description: Toto téma popisuje entitu Kontakt strany pro Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d77f5ebb52c14759918178194fc08b63d27db1f0
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798194"
---
# <a name="party-contact"></a>Kontakt strany

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Toto téma popisuje entitu Kontakt strany pro Dynamics 365 Human Resources.

Fyzický název: mshr_dirpartycontactentities

## <a name="description"></a>popis

Tato entita popisuje kontaktní informace kandidáta, včetně telefonu, e-mailu a sociálních účtů.

## <a name="json-representation"></a>Kód JSON

```json
{
    "mshr_partynumber": "String",
    "mshr_locationid": "String",
    "mshr_description": "String",
    "mshr_type": Int,
    "mshr_countryregioncode": "String",
    "mshr_locator": "String",
    "mshr_locatorextension": "String",
    "mshr_purpose": "String",
    "mshr_ismobilephone": Int,
    "mshr_isinstantmessage": Int,
    "mshr_isprimary": Int,
    "mshr_isprivate": Int,
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "String",
    "mshr_dirpartycontactentityid": "String"
}
```

## <a name="properties"></a>Vlastnosti

| Vlastnost<br>**Fyzický název**<br>**_Typ_** | Použít | popis |
| --- | --- | --- |
| **ID entity kontaktu strany**<br>mshr_dirpartycontactentityid<br>*Řetězec* | Jen pro čtení<br>Povinná | Systémem generovaný jedinečný identifikátor pro záznam entity. |
| **Číslo strany**<br>mshr_partynumber<br>*Řetězec* | Čtení/zápis<br>Povinná | ID záznamu přidružené strany (osoby). |
| **Hodnota ID osoby**<br>_mshr_fk_person_id_value<br>*GUID* | Jen pro čtení<br>Povinná<br>Cizí klíč: mshr_dirpersonentityid entity mshr_dirpersonentity | Systémem generovaný jedinečný identifikátor záznamu entity strany (osoby). |
| **ID umístění**<br>mshr_locationid<br>*Řetězec* | Čtení/zápis<br>Povinná | ID místa pro záznam adresy. Nastavte v entitě mshr_logisticspostaladdresslocationcdsentity. |
| **Popis**<br>mshr_description<br>*Řetězec* | Čtení/zápis<br>Povinná | Popis kontaktních údajů. |
| **Typ**<br>mshr_type<br>*Sada možností mshr_logisticselectronicaddressmethodtype* | Čtení/zápis<br>Povinná | Typ podrobností o kontaktu. |
| **Kód země/oblasti**<br>mshr_countryregioncode<br>*Řetězec* | Čtení/zápis<br>Volitelné | Země či oblast adresy. |
| **Lokátor**<br>mshr_locator<br>*Řetězec* | Čtení/zápis<br>Volitelné | Podrobnosti o kontaktu. Například pokud je typ **E-mailová adresa**, pak toto pole obsahuje e-mailovou adresu kandidáta. |
| **Rozšíření lokátoru**<br>mshr_locatorextension<br>*Řetězec* | Čtení/zápis<br>Volitelné | Rozšíření lokátoru. Například pokud je typ **Telefon**, pak by tato vlastnost obsahovala rozšíření telefonního čísla. |
| **Je mobilní**<br>mshr_ismobile<br>*Sada možností mshr_noyes* | Čtení/zápis<br>Povinná | Určuje, zda je telefon číslem mobilního telefonu. |
| **Je rychlá zpráva**<br>mshr_isinstantmessage<br>*Sada možností mshr_noyes* | Čtení/zápis<br>Povinná | Určuje, zda je telefon povolen pro zasílání rychlých zpráv. |
| **Je primární**<br>mshr_isprimary<br>*Sada možností mshr_noyes* | Čtení/zápis<br>Povinná | Pro typ kontaktu určuje primární kontakt. Na každý typ kontaktu musí být pouze jeden primární záznam. |
| **Je soukromá**<br>mshr_isprivate<br>*Sada možností mshr_noyes* | Čtení/zápis<br>Povinná | Určuje, zda je tato adresa soukromou adresou dané osoby. |
| **Účel**<br>mshr_purpose<br>*Řetězec* | Čtení/zápis<br>Volitelné | Účel/role kontaktních údajů. |
| **Primární pole**<br>mshr_primaryfield<br>*Řetězec* | Jen pro čtení<br>Povinná | Pole použité jako primární identifikátor záznamu entity. Kombinace čísla, typu, popisu a lokátoru strany. |

## <a name="see-also"></a>Viz také

[Úvod do rozhraní API pro integraci systému sledování žadatelů](hr-admin-integration-ats-api-introduction.md)<br>
[Příklad dotazu pro entitu Kandidát k přijetí](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]