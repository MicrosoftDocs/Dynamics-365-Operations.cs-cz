---
title: Osobní identifikační číslo
description: Tento článek popisuje entitu Osobní identifikační číslo pro Dynamics 365 Human Resources.
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
ms.openlocfilehash: 2d3641ffede29b7fda904ffb6cd70cb33d7800d4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858265"
---
# <a name="person-identification-number"></a>Osobní identifikační číslo


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tento článek popisuje entitu Osobní identifikační číslo pro Dynamics 365 Human Resources.

Fyzický název: mshr_hcmpersonidentificationnumberentity

## <a name="description"></a>popis

Tato entita popisuje identifikační čísla kandidáta. Umožňuje spotřebiteli rozhraní API zapsat identifikační čísla, jako čísla sociálního zabezpečení nebo čísla pasů, do záznamu kandidáta. Identifikační čísla jsou dostupná v záznamu pracovníka, ale ne v záznamu kandidáta. Integrující aplikace může zapsat hodnoty do databáze Human Resources, ale čísla nebudou viditelná v modulu Humanr Resources, dokud nebude vytvořen záznam pracovníka pro kandidáta.

## <a name="json-representation"></a>Kód JSON

```json
{
    "mshr_entrytype": "String",
    "mshr_description": "String",
    "mshr_expirationdate": "Datetime",
    "mshr_isprimary": Int,
    "mshr_identificationnumber": "String",
    "mshr_partynumber": "String",
    "mshr_identificationtypeid": "String",
    "mshr_issuingagencyid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "_mshr_fk_issuingagency_id_value": "Guid",
    "_mshr_fk_identificationtype_id_value": "Guid",
    "mshr_hcmpersonidentificationnumberentityid": "Guid",
    "mshr_issueddate": "Datetime"
}
```

## <a name="properties"></a>Vlastnosti

| Vlastnost<br>**Fyzický název**<br>**_Typ_** | Použít | popis |
| --- | --- | --- |
| **ID entity Osobní identifikační číslo**<br>mshr_hcmpersonidentificationnumberentityid<br>*GUID* | Jen pro čtení<br>Povinná<br>Generováno systémem | Jedinečný primární identifikátor pro záznam identifikačního čísla osoby. |
| **Typ položky**<br>mshr_entrytype<br>*Řetězec* | Čtení-zápis<br>Volitelné | Volná hodnota odkazující na typ záznamu identifikačního čísla. |
| **Popis**<br>mshr_description<br>*Řetězec* | Čtení-zápis<br>Volitelné | Popis identifikačního čísla. |
| **Datum vypršení platnosti**<br>mshr_expirationdate<br>*Datum a čas* | Čtení-zápis<br>Volitelné | Datum, kdy vyprší platnost identifikačního čísla nebo souvisejícího dokumentu. |
| **Je primární**<br>mshr_isprimary<br>*Sada možností mshr_noyes* | Čtení-zápis<br>Volitelné | Definuje, zda je identifikační číslo primárním záznamem osoby pro tento typ identifikace. |
| **Identifikační číslo**<br>mshr_identificationnumber<br>*Řetězec* | Čtení-zápis<br>Povinná | Identifikační číslo. |
| **Číslo strany**<br>mshr_partynumber<br>*Řetězec* | Čtení-zápis<br>Povinná | Identifikátor strany (osoby) vlastnící identifikační číslo. |
| **Hodnota ID osoby**<br>_mshr_fk_person_id_value<br>*GUID* | Jen pro čtení<br>Povinná<br>Cizí klíč: mshr_dirpersonentityid entity mshr_dirpersonentity | Jedinečný identifikátor strany (osoby). |
| **ID typu identifikace**<br>mshr_identificationtypeid<br>*Řetězec* | Čtení-zápis<br>Povinná | Typ identifikačního čísla. |
| **Hodnota ID typu identifikace**<br>_mshr_fk_identificationtype_id_value<br>*GUID* | Jen pro čtení<br>Povinná<br>Cizí klíč: mshr_hcmidentificationtypeentityid entity mshr_hcmidentificationtypeentity | Systémem generovaný jedinečný identifikátor typu identifikace. |
| **ID vydávajícího úřadu**<br>mshr_issuingagencyid<br>*Řetězec* | Čtení-zápis<br>Volitelné | Agentura nebo organizace vydávající identifikační číslo. |
| **Hodnota ID vydávajícího úřadu**<br>_mshr_fk_issuingagency_id_value<br>*GUID* | Jen pro čtení<br>Volitelné<br>Cizí klíč: mshr_hcmissuingagencyentityid entity mshr_hcmissuingagencyentity | Systémem generovaný jedinečný identifikátor identifikačního čísla vydávajícího úřadu. |
| **Primární pole**<br>mshr_primaryfield<br>*Řetězec* | Jen pro čtení<br>Povinná | Pole, které se použije jako identifikátor záznamu entity. Kombinace čísla strany, ID typu identifikace a identifikačního čísla. |
| **Datum vydání**<br>mshr_issuedate<br>*Datum* | Čtení-zápis<br>Volitelné | Datum vystavení identifikačního čísla. |

## <a name="see-also"></a>Viz také

[Úvod do rozhraní API pro integraci systému sledování žadatelů](hr-admin-integration-ats-api-introduction.md)<br>
[Příklad dotazu pro entitu Kandidát k přijetí](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
