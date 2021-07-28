---
title: Adresa pracovníka na výplatní listině
description: Toto téma poskytuje informace a ukázkový dotaz pro entitu adresy pracovníka na výplatní listině v Dynamics 365 Human Resources.
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1ff65a0518232275f7c5d0b4a70d04f77e4936c5
ms.sourcegitcommit: 89bb2a7f402deed32998eddc1e56e75250e3d15e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/29/2021
ms.locfileid: "6314106"
---
# <a name="payroll-worker-address"></a>Adresa pracovníka na výplatní listině

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Toto téma popisuje entitu Adresa pracovníka se mzdou pro Dynamics 365 Human Resources.

Fyzický název: mshr_payrollworkeraddressentity.

### <a name="description"></a>popis

Tato entita poskytuje místo bydliště a místo práce mzdy pro daného zaměstnance.

## <a name="properties"></a>Vlastnosti

| Vlastnost</br>**Fyzický název**</br>**_Typ_** | Použít | popis |
| --- | --- | --- |
| **Město**</br>mshr_city</br>*Řetězec* | Jen pro čtení</br>Povinná | Město definované pro adresu.   |
| **Číslo pracovníka**</br>mshr_personnelnumber</br>*Řetězec* | Jen pro čtení</br>Povinná | Jedinečné osobní číslo zaměstnance.  |
| **Oblast země**</br>mshr_countryregionid</br>*Řetězec* | Jen pro čtení</br>Povinná | Oblast země definovaná pro adresu.  |
| **Platné od**</br>mshr_postaladdressvalidfrom</br>*Posun data a času* | Jen pro čtení </br>Povinná | Datum, odkdy je adresa platná. |
| **Pracoval(a) na adrese** </br> mshr_isworkedinaddressbr </br>*[Nastavená možnost mshr_NoYes](hr-admin-integration-payroll-api-no-yes.md)* | Jen pro čtení</br>Povinná | Označuje, zda je adresa tam, kde zaměstnanec pracuje. |
| **Okres**</br>mshr_county</br>*Řetězec* | Jen pro čtení</br>Povinná | Kraj definovaný pro adresu.  |
| **ID adresy pracovníka na výplatní listině**</br>mshr_payrollworkeraddressentityid</br>*GUID* | Povinná</br>Generováno systémem | Systémem generovaná hodnota GUID pro jedinečnou identifikaci adresy.  |
| **Primární pole**</br>mshr_primaryfield</br>*Řetězec* | Jen pro čtení</br>Povinná |  |
| **Ulice**</br>mshr_street</br>*Řetězec* | Jen pro čtení</br>Povinná | Ulice definovaná pro adresu. |
| **Platné do**</br>mshr_postaladdressvalidto</br>*Posun data a času* | Jen pro čtení </br>Povinná | Datum, dokdy je adresa platná.  |
| **ID umístění**</br>mshr_locationidbr>*Řetězec* | Jen pro čtení <br>Povinná | ID adresy.  |
| **PSČ**</br>mshr_zipcode<br>*Řetězec* | Jen pro čtení <br>Povinná |Identifikační číslo definované pro zaměstnance.  |
| **Bydlel(a) na adrese**</br>mshr_islivedinaddressbr </br> *[Nastavená možnost mshr_NoYes](hr-admin-integration-payroll-api-no-yes.md)* | Jen pro čtení</br>Povinná | Označuje, zda je adresa tam, kde zaměstnanec bydlí. |
| **Kraj**</br>mshr_state</br>*Řetězec* | Jen pro čtení</br>Povinná | Stát definovaná pro adresu.  |

## <a name="example-query"></a>Ukázkový dotaz

**Žádost**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollworkeraddressentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_postaladdressvalidfrom le @asofdate and mshr_postaladdressvalidto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

**Odezva**

```json
{
    "mshr_personnelnumber": "000041",
    "mshr_locationid": "000000538",
    "mshr_islivedinaddress": 200000001,
    "mshr_isworkedinaddress": 200000000,
    "mshr_countryregionid": "USA",
    "mshr_zipcode": "99025",
    "mshr_street": "6543 Cypress Ave",
    "mshr_city": "Tacoma",
    "mshr_state": "WA",
    "mshr_county": "KING",
    "mshr_postaladdressvalidfrom": "2012-09-20T20:14:27Z",
    "mshr_postaladdressvalidto": "2154-12-31T23:59:59Z",
    "mshr_primaryfield": "000041 | 000000538 | 9/20/2012 08:14:27 pm",
    "_mshr_fk_worker_id_value": "00000d3c-0000-0000-d5ff-004105000000",
    "mshr_payrollworkeraddressentityid": "000006f0-0000-0000-f90f-014105000000"

}
```

## <a name="see-also"></a>Viz také

[Úvod do rozhraní API integrace mezd](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
