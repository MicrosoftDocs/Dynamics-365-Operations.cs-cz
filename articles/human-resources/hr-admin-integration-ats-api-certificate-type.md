---
title: Typ certifikátu
description: Toto téma popisuje entitu typu Certifikát pro Dynamics 365 Human Resources.
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
ms.openlocfilehash: fe5713b6b5f38ad7f6857b36c6b2f63a1dc0c320
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798385"
---
# <a name="certificate-type"></a>Typ certifikátu

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Toto téma popisuje entitu typu Certifikát pro Dynamics 365 Human Resources.

Fyzický název: mshr_hcmcertificatetypeentity

## <a name="description"></a>popis

Tato entita definuje seznam typů profesionálních certifikátů nastavených v Human Resources. Entita není specifická pro právnickou osobu (společnost).

## <a name="json-representation"></a>Kód JSON

```json
{
    "mshr_certificatetype": "String",
    "mshr_description": "String",
    "mshr_requirerenewal": Int,
    "mshr_hcmcertificatetypeentityid": "Guid"
}
```

## <a name="properties"></a>Vlastnosti

| Vlastnost<br>**Fyzický název**<br>**_Typ_** | Použít | popis |
| --- | --- | --- |
| **ID entity typu certifikátu**<br>mshr_hcmcertificatetypeentityid<br>*GUID* | Jen pro čtení<br>Povinná 
Generováno systémem | Jedinečný primární identifikátor pro záznam typu certifikátu. |
| **Typ certifikátu**<br>mshr_certificatetype<br>*Řetězec* | Čtení/zápis<br>Povinná | Jedinečný, uživatelem čitelný identifikátor pro typ certifikátu. |
| **Popis**<br>mshr_description<br>*Řetězec* | Čtení/zápis<br>Povinná | Popis typu certifikátu. |
| **Vyžaduje obnovení**<br>mshr_requirerenewal<br>*Sada možností mshr_noyes* | Čtení/zápis<br>Volitelné | Označuje, zda je pro certifikát vyžadováno obnovení. |

## <a name="see-also"></a>Viz také

[Úvod do rozhraní API pro integraci systému sledování žadatelů](hr-admin-integration-ats-api-introduction.md)<br>
[Příklad dotazu pro entitu Kandidát k přijetí](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]