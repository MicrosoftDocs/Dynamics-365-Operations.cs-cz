---
title: Osoba
description: Toto téma popisuje entitu Osoba pro Dynamics 365 Human Resources.
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
ms.openlocfilehash: ab3dd62785e6f4d94d5bd6faeed5dbc965a7a0573eaeee1c880062ab69b2dc21
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6778813"
---
# <a name="person"></a>Osoba

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Toto téma popisuje entitu Osoba pro Dynamics 365 Human Resources.

Fyzický název: mshr_dirpersonentity

### <a name="description"></a>popis

Tato entita poskytuje osobní údaje kandidáta.

## <a name="json-representation"></a>Kód JSON

```json
{
    "mshr_partynumber": "String",
    "mshr_name": "String",
    "mshr_namealias": "String",
    "mshr_knownas": "String",
    "mshr_languageid": "String",
    "mshr_addressbooks": "String",
    "mshr_anniversaryday": Int,
    "mshr_anniversarymonth": Int,
    "mshr_anniversaryyear": Int,
    "mshr_birthday": Int,
    "mshr_birthmonth": Int,
    "mshr_birthyear": Int,
    "mshr_childrennames": "String",
    "mshr_gender": Int,
    "mshr_hobbies": "String",
    "mshr_initials": "String",
    "mshr_maritalstatus": Int,
    "mshr_phoneticfirstname": "String",
    "mshr_phoneticlastname": "String",
    "mshr_phoneticmiddlename": "String",
    "mshr_personalsuffix": "String",
    "mshr_personaltitle": "String",
    "mshr_professionalsuffix": "String",
    "mshr_professionaltitle": "String",
    "mshr_fullprimaryaddress": "String",
    "mshr_addresscity": "String",
    "mshr_addresscountryregionid": "String",
    "mshr_addresscountryregionisocode": "String",
    "mshr_addresscounty": "String",
    "mshr_addressdistrictname": "String",
    "mshr_addresslatitude": Decimal,
    "mshr_addresslocationid": "000003212",
    "mshr_addresslocationroles": "Home",
    "mshr_addresslongitude": Decimal,
    "mshr_addressstate": "String",
    "mshr_addressstreet": "String",
    "mshr_addressvalidfrom": "Date",
    "mshr_addressvalidto": "Date",
    "mshr_addresszipcode": "String",
    "mshr_addressisprivate": Int,
    "mshr_addressdescription": "String",
    "mshr_primarycontactemail": "String",
    "mshr_primarycontactemaildescription": "String",
    "mshr_primarycontactemailisim": Int,
    "mshr_primarycontactemailpurpose": "String",
    "mshr_primarycontactfax": "String",
    "mshr_primarycontactfaxdescription": "String",
    "mshr_primarycontactfaxextension": "String",
    "mshr_primarycontactfaxpurpose": "String",
    "mshr_primarycontactphone": "String",
    "mshr_primarycontactphonedescription": "String",
    "mshr_primarycontactphoneextension": "String",
    "mshr_primarycontactphoneismobile": Int,
    "mshr_primarycontactphonepurpose": "String",
    "mshr_primarycontacttelex": "String",
    "mshr_primarycontacttelexdescription": "String",
    "mshr_primarycontacttelexpurpose": "String",
    "mshr_primarycontacturl": "String",
    "mshr_primarycontacturldescription": "String",
    "mshr_primarycontacturlpurpose": "String",
    "mshr_primarycontactfacebook": "String",
    "mshr_primarycontactfacebookdescription": "String",
    "mshr_primarycontactfacebookisprivate": Int,
    "mshr_primarycontactfacebookpurpose": "String",
    "mshr_primarycontactlinkedin": "String",
    "mshr_primarycontactlinkedindescription": "String",
    "mshr_primarycontactlinkedinisprivate": Int,
    "mshr_primarycontactlinkedinpurpose": "String",
    "mshr_primarycontacttwitter": "String",
    "mshr_primarycontacttwitterdescription": "String",
    "mshr_primarycontacttwitterisprivate": Int,
    "mshr_primarycontacttwitterpurpose": "String",
    "mshr_partytype": "String",
    "mshr_namesequencedisplayas": "String",
    "mshr_firstname": "String",
    "mshr_lastnameprefix": "String",
    "mshr_lastname": "String",
    "mshr_middlename": "String",
    "mshr_electroniclocationid": "String",
    "mshr_dirpersonentityid": "Guid",
    "mshr_addresstimezone": Int
}
```

## <a name="properties"></a>Vlastnosti

| Vlastnost<br>**Fyzický název**<br>**_Typ_** | Použít | popis |
| --- | --- | --- |
| **ID entity Osoba**<br>mshr_dirpersonentityid<br>*GUID* | Jen pro čtení<br>Povinná<br>Generováno systémem | Systémem generovaný jedinečný identifikátor pro záznam entity. |
| **Číslo strany**<br>mshr_partynumber<br>*Řetězec* | Jen pro čtení<br>Povinná<br>Generováno systémem | Uživatelem čitelný, systémem generovaný jedinečný identifikátor osoby.  |
| **Jméno**<br>mshr_name<br>*Řetězec* | Jen pro čtení<br>Povinná | Hodnota pole je zřetězením křestního jména, druhého jména, předpony příjmení a příjmení v pořadí definovaném v poli **Zobrazit pořadí názvů jako**. |
| **Alias jména**<br>mshr_namealias<br>*Řetězec* | Čtení/zápis<br>Volitelné | Alias jména, který lze nabídnout dané osobě. |
| **Známá jako**<br>mshr_knownas<br>*Řetězec* | Čtení/zápis<br>Volitelné | Jméno, které lze pro danou osobu použít, je-li obvykle známá pod jiným jménem. |
| **ID jazyka**<br>mshr_languageid<br>*Řetězec* | Čtení/zápis<br>Volitelné | ID jazyka primárního jazyka osoby, jak je definováno ve formátu ISO 639-1. |
| **Adresáře**<br>mshr_addressbooks<br>*Řetězec* | Čtení/zápis<br>Volitelné | Adresář, do kterého lze osobu přiřadit. Adresáře, které byly vytvořeny pro organizaci, jsou uvedeny v entitě mshr_diraddressbooksentity. |
| **Den výročí**<br>mshr_anniversaryday<br>*Int* | Čtení/zápis<br>Volitelné | Den výročí osoby. |
| **Měsíc výročí**<br>mshr_anniversarymonth<br>*Sada možností mshr_monthsofyear* | Čtení/zápis<br>Volitelné | Měsíc výročí osoby. |
| **Rok výročí**<br>mshr_anniversaryyear<br>*Int* | Čtení/zápis<br>Volitelné | Rok výročí osoby. |
| **Den narození**<br>mshr_birthday<br>*Int* | Čtení/zápis<br>Volitelné | Datum narození osoby. |
| **Měsíc narození**<br>mshr_birthmonth<br>*Sada možností mshr_monthsofyear* | Čtení/zápis<br>Volitelné | Měsíc narození osoby. |
| **Rok narození**<br>mshr_birthyear<br>*Int* | Čtení/zápis<br>Volitelné | Rok narození osoby. |
| **Jména dětí**<br>mshr_childrennames<br>*Řetězec* | Čtení/zápis<br>Volitelné | Řetězec se jmény dětí dané osoby. Není je třeba oddělovat. |
| **Rod**<br>mshr_gender<br>*Sada možností mshr_hcmpersongender* | Čtení/zápis<br>Volitelné | Pohlaví osoby. |
| **Záliby**<br>mshr_hobbies<br>*Řetězec* | Čtení/zápis<br>Volitelné | Záliby dané osoby. |
| **Iniciály**<br>mshr_initials<br>*Řetězec* | Čtení/zápis<br>Volitelné | Iniciály jména osoby. |
| **Rodinný stav**<br>mshr_maritalstatus<br>*Sada možností mshr_hcmpersonmaritalstatus* | Čtení/zápis<br>Volitelné | Rodinný stav osoby. |
| **Křestní jméno foneticky**<br>mshr_phoneticfirstname<br>*Řetězec* | Čtení/zápis<br>Volitelné | Fonetická výslovnost křestního jména osoby. |
| **Příjmení foneticky**<br>mshr_phoneticlastname<br>*Řetězec* | Čtení/zápis<br>Volitelné | Fonetická výslovnost příjmení osoby. |
| **Druhé jméno foneticky**<br>mshr_phoneticmiddlename<br>*Řetězec* | Čtení/zápis<br>Volitelné | Fonetická výslovnost příjmení osoby. |
| **Osobní přípona**<br>mshr_personalsuffix<br>*Řetězec* | Čtení/zápis<br>Volitelné | Osobní přípona osoby. Platné hodnoty v entitě mshr_dirnameaffixentity, kde mshr_type je přípona (200000001). |
| **Osobní titul**<br>mshr_personaltitle<br>*Řetězec* | Čtení/zápis<br>Volitelné | Osobní titul osoby. Platné hodnoty v entitě mshr_dirnameaffixentity, kde mshr_type je titul (200000000).
| **Profesní přípona**<br>mshr_professionalsuffix<br>*Řetězec* | Čtení/zápis<br>Volitelné | Profesní přípona. |
| **Profesní titul**<br>mshr_professionaltitle<br>*Řetězec* | Čtení/zápis<br>Volitelné | Profesní titul. |
| **Úplná primární adresa**<br>mshr_fullprimaryaddress<br>*Řetězec* | Čtení/zápis<br>Volitelné | Úplná primární adresa osoby, zřetězení polí primární adresy. |
| **Adresa – město**<br>mshr_addresscity<br>*Řetězec* | Čtení/zápis<br>Volitelné | Město v primární adrese osoby. Nastavte v entitě v mshr_logisticsaddresscityentity. |
| **Oblast/země v adrese**<br>mshr_addresscountryregionid<br>*Řetězec* | Čtení/zápis<br>Volitelné | Země/oblast v primární adrese osoby. Platné hodnoty v entitě mshr_logisticsaddresscountryregionentity. |
| **Kód ISO oblasti/země v adrese**<br>mshr_addresscountryregionisocode<br>*Řetězec* | Čtení/zápis<br>Volitelné | Kód ISO země/oblasti v primární adrese osoby. |
| **Okres v adrese**<br>mshr_addresscounty<br>*Řetězec* | Čtení/zápis<br>Volitelné | Okres v primární adrese osoby. Nastavte v entitě v mshr_logisticsaddresscountyentity. |
| **Název kraje adresy**<br>mshr_addressdistrictname<br>*Řetězec* | Čtení/zápis<br>Volitelné | Kraj primární adresy osoby. Nastavte v entitě v mshr_logisticsaddressdistrictentity. |
| **Zeměpisná šířka adresy**<br>mshr_addresslatitude<br>*Řetězec* | Čtení/zápis<br>Volitelné | Zeměpisná šířka primární adresy osoby. |
| **ID místa adresy**<br>mshr_addresslocationid<br>*Řetězec* | Čtení/zápis<br>Volitelné | Jedinečný identifikátor pro umístění primární adresy osoby. Platné hodnoty v entitě mshr_logisticspostaladdresslocationcdsentity. |
| **Role místa adresy**<br>mshr_addresslocationroles<br>*Řetězec* | Čtení/zápis<br>Volitelné | Role místa primární adresy osoby. Nastavte v entitě mshr_logisticslocationrolecdsentity. |
| **Zeměpisná délka**<br>mshr_addresslongitude<br>*Řetězec* |  Čtení/zápis<br>Volitelné | Zeměpisná délka primární adresy osoby. |
| **Stát v adrese**<br>mshr_addressstate<br>*Řetězec* | Čtení/zápis<br>Volitelné | Stát v primární adrese osoby. Nastavte v entitě v mshr_logisticsaddressstateentity. |
| **Ulice v adrese**<br>mshr_addressstreet<br>*Řetězec* | Čtení/zápis<br>Volitelné | Ulice v primární adrese osoby. |
| **Adresa platná od**<br>mshr_addressvalidfrom<br>*Datum* | Čtení/zápis<br>Volitelné | Datum, od kterého je platná primární adresa osoby. |
| **Adresa platná do**<br>mshr_addressvalidto<br>*Datum* | Čtení/zápis<br>Volitelné | Datum, do kterého je platná primární adresa osoby. |
| **PSČ v adrese**<br>mshr_addresszipcode<br>*Řetězec* | Čtení/zápis<br>Volitelné | PSČ primární adresy osoby. Nastavte v entitě v mshr_logisticsaddresspostalcodeentity. |
| **Adresa je soukromá**<br>mshr_addressisprivate<br>*Sada možností mshr_noyes* | Čtení/zápis<br>Volitelné | Určuje, zda je primární adresa osoby sdílena s ostatními v organizaci. |
| **Popis adresy**<br>mshr_addressdescription<br>*Řetězec* | Čtení/zápis<br>Volitelné | Popis primární adresy osoby. |
| **Primární kontaktní e-mail**<br>mshr_primarycontactemail<br>*Řetězec* | Čtení/zápis<br>Volitelné | Primární e-mailová adresa osoby. |
| **Popis primárního kontaktního e-mailu**<br>mshr_primarycontactemaildescription<br>*Řetězec* | Čtení/zápis<br>Volitelné | Popis primární e-mailové adresy. |
| **Primární kontaktní e-mail podporuje zasílání rychlých zpráv**<br>mshr_primarycontactemailisim<br>*Sada možností mshr_noyes* | Čtení/zápis<br>Volitelné | Určuje, zda primární e-mailová adresa podporuje zasílání rychlých zpráv. |
| **Účel primárního kontaktního e-mailu**<br>mshr_primarycontactemailpurpose<br>*Řetězec* | Čtení/zápis<br>Volitelné | Účel primární e-mailové adresy. Nastavte v entitě mshr_logisticslocationroleentity. |
| **Primární kontaktní fax**<br>mshr_primarycontactfax<br>*Řetězec* | Čtení/zápis<br>Volitelné | Číslo primárního faxu. |
| **Popis primárního kontaktního faxu**<br>mshr_primarycontactfaxdescription<br>*Řetězec* | Čtení/zápis<br>Volitelné | Popis poskytnutého primárního čísla faxu. |
| **Rozšíření primárního kontaktního faxu**<br>mshr_primarycontactfaxextension<br>*Řetězec* | Čtení/zápis<br>Volitelné | Rozšíření primárního faxového čísla. |
| **Účel primárního kontaktního faxu**<br>mshr_primarycontactfaxpurpose<br>*Řetězec* | Čtení/zápis<br>Volitelné | Účel primárního faxového čísla. Nastavte v entitě mshr_logisticslocationroleentity.
| **Primární kontaktní telefon**<br>mshr_primarycontactphone<br>*Řetězec* | Čtení/zápis<br>Volitelné | Primární telefonní číslo |
| **Popis primárního kontaktního telefonu**<br>mshr_primarycontactphonedescription<br>*Řetězec* | Čtení/zápis<br>Volitelné | Popis poskytnutého primárního čísla telefonu. |
| **Rozšíření primárního kontaktního telefonu**<br>mshr_primarycontactphoneextension<br>*Řetězec* | Čtení/zápis<br>Volitelné | Rozšíření primárního telefonního čísla. |
| **Primárního kontaktní telefon je mobilní**<br>mshr_primarycontactphoneismobile<br>*Sada možností mshr_noyes* | Čtení/zápis<br>Volitelné | Určuje, zda je primární telefonní číslo na mobilní telefon. |
| **Účel primárního kontaktního telefonu**<br>mshr_primarycontactphonepurpose<br>*Řetězec* | Čtení/zápis<br>Volitelné | Účel primárního telefonního čísla. Nastavte v entitě mshr_logisticslocationroleentity. |
| **Primární kontaktní telex**<br>mshr_primarycontacttelex<br>*Řetězec* | Čtení/zápis<br>Volitelné | Číslo primárního telexu. |
| **Popis primárního kontaktního telexu**<br>mshr_primarycontacttelexdescription<br>*Řetězec* | Čtení/zápis<br>Volitelné | Popis poskytnutého primárního čísla telexu osoby. |
| **Účel primárního kontaktního telexu**<br>mshr_primarycontacttelexpurpose<br>*Řetězec* | Čtení/zápis<br>Volitelné | Účel primárního čísla telexu osoby. Nastavte v entitě mshr_logisticslocationroleentity. |
| **Primární kontaktní adresa URL**<br>mshr_primarycontacturl<br>*Řetězec* | Čtení/zápis<br>Volitelné | Primární adresa URL. |
| **Popis primární kontaktní adresy URL**<br>mshr_primarycontacturldescription<br>*Řetězec* | Čtení/zápis<br>Volitelné | Popis poskytnuté primární adresy URL osoby. |
| **Účel primární kontaktní adresy URL**<br>mshr_primarycontacturldescription<br>*Řetězec* | Čtení/zápis<br>Volitelné | Účel primární adresy URL osoby. Nastavte v entitě mshr_logisticslocationroleentity. |
| **Primární kontaktní účet Facebook**<br>mshr_primarycontactfacebook<br>*Řetězec* | Čtení/zápis<br>Volitelné | Primární účet ve službě Facebook. Identifikován podle ID uživatele. |
| **Popis primárního kontaktního účtu Facebook**<br>mshr_primarycontactfacebookdescription<br>*Řetězec* | Čtení/zápis<br>Volitelné | Popis poskytnutého primárního účtu Facebook osoby. |
| **Primární kontaktní účet Facebook je soukromý**<br>mshr_primarycontactfacebookisprivate<br>*Sada možností mshr_noyes* | Čtení/zápis<br>Volitelné | Určuje, zda je primární účet Facebook viditelný ostatním uživatelům. |
| **Účel primárního kontaktního účtu Facebook**<br>mshr_primarycontactfacebookpurpose<br>*Řetězec* | Čtení/zápis<br>Volitelné | Účel primárního účtu Facebook osoby. Nastavte v entitě mshr_logisticslocationroleentity. |
| **Primární kontaktní účet LinkedIn**<br>mshr_primarycontactlinkedin<br>*Řetězec* | Čtení/zápis<br>Volitelné | Primární účet LinkedIn. Identifikován podle uživatelského jména. |
| **Popis primárního kontaktního účtu LinkedIn**<br>mshr_primarycontactlinkedindescription<br>*Řetězec* | Čtení/zápis<br>Volitelné | Popis poskytnutého primárního účtu LinkedIn osoby. |
| **Primární kontaktní účet LinkedIn je soukromý**<br>mshr_primarycontactlinkedinisprivate<br>*Sada možností mshr_noyes* | Čtení/zápis<br>Volitelné | Určuje, zda jsou informace o primárním účtu LinkedIn sdílen s ostatními uživateli. |
| **Účel primárního kontaktního účtu LinkedIn**<br>mshr_primarycontactlinkedinpurpose<br>*Řetězec* | Čtení/zápis<br>Volitelné | Účel primárního účtu LinkedIn osoby. Nastavte v entitě mshr_logisticslocationroleentity. |
| **Primární kontaktní účet Twitter**<br>mshr_primarycontacttwitter<br>*Řetězec* | Čtení/zápis<br>Volitelné | Primární účet Twitter dané osoby. Identifikován pomocí @uživatelské_jméno. |
| **Popis primárního kontaktního účtu Twitter**<br>mshr_primarycontacttwitterdescription<br>*Řetězec* | Čtení/zápis<br>Volitelné | Popis poskytnutého primárního účtu Twitter osoby. |
| **Primární kontaktní účet Twitter je soukromý**<br>mshr_primarycontacttwitterisprivate<br>*Sada možností mshr_noyes* | Čtení/zápis<br>Volitelné | Určuje, zda jsou informace o primárním účtu Twitter sdílen s ostatními uživateli. |
| **Účel primárního kontaktního účtu Twitter**<br>mshr_primarycontacttwitterpurpose<br>*Řetězec* | Čtení/zápis<br>Volitelné | Účel primárního účtu Twitter osoby. Nastavte v entitě mshr_logisticslocationroleentity. |
| **Typ strany**<br>mshr_partytype<br>*Řetězec* | Čtení/zápis<br>Volitelné | Typ strany osoby. Pro kandidáty to vždy bude **Osoba**. |
| **Zobrazit pořadí názvů jako**<br>mshr_namesequencedisplayas<br>*Řetězec* | Čtení/zápis<br>Volitelné | Pořadí, ve kterém jsou zřetězeny vlastnosti jména osoby do hodnoty vlastnosti Jméno (mshr_name). |
| **Jméno**<br>mshr_firstname<br>*Řetězec* | Čtení/zápis<br>Povinná | Křestní jméno osoby. |
| **Druhé jméno**<br>mshr_middlename<br>*Řetězec* | Čtení/zápis<br>Volitelné | Druhé jméno osoby. |
| **Předpona příjmení**<br>mshr_lastnameprefix<br>*Řetězec* | Čtení/zápis<br>Volitelné | Předpona příjmení osoby. |
| **Příjmení**<br>mshr_lastname<br>*Řetězec* | Čtení/zápis<br>Volitelné | Příjmení osoby. |
| **ID elektronické polohy**<br>mshr_electroniclocationid<br>*Řetězec* | Čtení/zápis<br>Volitelné | ID elektronické polohy osoby. |
| **Časové pásmo adresy**<br>mshr_addresstimezone<br>*Int* | Čtení/zápis<br>Volitelné | Časové pásmo primární adresy osoby. |

## <a name="see-also"></a>Viz také

[Úvod do rozhraní API pro integraci systému sledování žadatelů](hr-admin-integration-ats-api-introduction.md)<br>
[Příklad dotazu pro entitu Kandidát k přijetí](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]