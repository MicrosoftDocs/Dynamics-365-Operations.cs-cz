---
title: Typ certifikátu
description: Toto téma popisuje entitu typu Certifikát pro Dynamics 365 Human Resources.
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
ms.openlocfilehash: b8e979f242eb689b730b7f8a8684b3e697adbee6
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054685"
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