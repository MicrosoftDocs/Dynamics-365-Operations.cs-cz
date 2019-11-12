---
title: Integrovaná hlavní data odběratelů
description: Toto téma popisuje integraci dat odběratele mezi aplikacemi Finance and Operations a Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: a66beb6338ea593247c79a11feb7f301d56f32a9
ms.sourcegitcommit: 6e0909e95f38b7487a4b7f68cc62b723f8b59bd4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/10/2019
ms.locfileid: "2572511"
---
# <a name="integrated-customer-master"></a>Integrovaná hlavní data odběratelů

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Pro záznamy zákazníků je typické, že je možné je řídit ve více než jedné aplikaci. Prodejní aktivita může například přinést záznamy komerčních zákazníků prostřednictvím aplikace Sales a elektronický obchod nebo maloobchodní prodej mohou přinést záznamy zákazníků v rámci aplikace Finance and Operations. Bez ohledu na to, odkud záznam odběratele pochází, je integrován v pozadí mezi hranicemi aplikace a rozdíly v infrastruktuře. Integrované řízení zákazníků pomáhá zvládat scénáře vícenásobného řízení a poskytuje komplexní přehled o zákaznících do sady aplikací Dynamics 365.

## <a name="customer-data-flow"></a>Tok dat odběratele

*Odběratel* je dobře definovaný koncept v aplikacích. Proto integrace zákaznických dat pouze zahrnuje harmonizaci koncepce zákazníků mezi těmito dvěmi aplikacemi. Následující obrázek znázorňuje tok dat odběratele.

![Tok dat odběratele](media/dual-write-customer-data-flow.png)

Zákazníci mohou být široce řazeni do dvou typů: obchodní/organizační zákazníci a spotřebitelé/koncoví uživatelé. Tyto dva typy zákazníků jsou ukládány a zpracovávány odlišně v aplikacích Finance and Operations a Common Data Service.

V aplikaci Finance and Operations jsou obchodní/organizační zákazníci i spotřebitelé/koncoví uživatelé řízeni v jedné tabulce s názvem **CustTable** (CustomerCustomerV3Entity) a jsou klasifikováni podle atributu **Typ**. (Je -li **Typ** nastaven na **Organizace**, je zákazníkem obchodní/organizační zákazník a pokud je **Typ** nastaven na **Osoba**, je zákazníkem zákazník/koncový uživatel.) Informace o primární kontaktní osobě jsou zpracovány prostřednictvím entity SMMContactPersonEntity.

V Common Data Service jsou obchodní/organizační zákazníci ovládáni entitou obchodní vztah a jsou identifikováni jako zákazníci, když je atribut **RelationshipType** nastaven na **Odběratel**. Entita kontakt reprezentuje spotřebitele/koncové uživatele i kontaktní osobu. Chcete-li zajistit jasné oddělení mezi spotřebitelem/koncovým uživatelem a kontaktní osobou, má entita **Kontakt** logický příznak, který se jmenuje **Prodejné**. Pokud je **Prodejné** je **True** je kontaktem spotřebitel/koncový uživatel a nabídky a objednávky lze vytvořit pro kontakt. Je-li **Prodejné** je **False** je kontaktem pouze primární kontaktní osoba zákazníka.

Pokud se procesu nabídky nebo objednávky účastní neprodejný kontakt, je **Prodejné** nastaveno na **True** pro označení kontaktu jako prodejného. Kontakt, který se stal prodejním kontaktem, zůstává prodejním kontaktem.

## <a name="templates"></a>Šablony

Data odběratele zahrnují všechny informace o odběrateli, například skupinu odběratelů, adresy, kontaktní informace, platební profil a profil faktury a věrnostní stav. Kolekce mapování entit pracuje společně během interakce s daty odběratele, jak je uvedeno v následující tabulce.

Aplikace Finance and Operations    | Jiné aplikace Dynamics 365
--------------------------|---------------------------------
Odběratel V3               | Účet
Odběratel V3               | Kontakt
CDS kontakty V2           | Kontakt
Skupiny odběratelů           | Msdyn\_customergroups
Způsob platby odběratele   | Msdyn\_customerpaymentmethods
Věrnostní karta              | Msdyn\_loyaltycards
Platební kalendář          | Msdyn\_paymentschedules
Platební kalendář          | Msdyn\_paymentschedulelines
Den platby CDS           | Msdyn\_paymentdays
Řádky dnů platby CDS     | Msdyn\_paymentdaylines
Platební podmínky          | Msdyn\_paymentterms
Přípony názvu              | Msdyn\_nameaffixes

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="customer-v3-to-account"></a>Odběratel V3 na obchodní vztah

Tato šablona synchronizuje hlavní informace o zákaznících pro komerční a organizační zákazníky mezi aplikacemi Finance and Operations a Common Data Service.

<!-- ![](media/dual-write-account-1.png) -->

<!-- ![](media/dual-write-account-2.png) -->

Zdrojové pole | Typ mapování | Cílové pole
---|---|---
CUSTOMERACCOUNT | = | accountnumber
INVOICEADDRESSCITY | = | address2\_city
INVOICEADDRESSCOUNTRYREGIONISOCODE | = | address2\_country
INVOICEADDRESSCOUNTY | = | address2\_county
INVOICEADDRESSLATITUDE | \> | address2\_latitude
INVOICEADDRESSLONGITUDE | \> | address2\_longitude
INVOICEADDRESSSTATE | = | address2\_stateorprovince
INVOICEADDRESSSTREET | = | address2\_line1
INVOICEADDRESSZIPCODE | = | address2\_postalcode
CREDITLIMIT | = | creditlimit
DELIVERYADDRESSCITY | = | address1\_city
DELIVERYADDRESSCOUNTRYREGIONISOCODE | = | address1\_country
DELIVERYADDRESSCOUNTY | = | address1\_county
DELIVERYADDRESSLATITUDE | \> | address1\_latitude
DELIVERYADDRESSLONGITUDE | \> | address1\_longitude
DELIVERYADDRESSZIPCODE | = | address1\_postalcode
ORGANIZATIONNAME | = | název
ORGANIZATIONNUMBEROFEMPLOYEES | = | numberofemployees
PRIMARYCONTACTEMAIL | = | emailaddress1
PRIMARYCONTACTFAX | = | fax
PRIMARYCONTACTPHONE | = | telephone1
PRIMARYCONTACTTWITTER | = | primarytwitterid
PRIMARYCONTACTURL | = | websiteurl
SALESCURRENCYCODE | = | transactioncurrencyid.isocurrencycode
SALESMEMO | = | popis
CREDITLIMITISMANDATORY | \>\< | msdyn\_creditlimitismandatory
CREDITRATING | = | msdyn\_creditrating
CUSTOMERGROUPID | = | msdyn\_customergroupid.msdyn\_groupid
IDENTIFICATIONNUMBER | = | msdyn\_identificationnumber
INVOICEACCOUNT | = | msdyn\_billingaccount.accountnumber
INVOICEADDRESS | \>\< | msdyn\_invoiceaddress
ISONETIMECUSTOMER | \>\< | msdyn\_onetimecustomer
ONHOLDSTATUS | \>\< | msdyn\_onholdstatus
PARTYCOUNTRY | = | msdyn\_partycountry
PARTYSTATE | = | msdyn\_partystateprovince
PAYMENTDAY | = | msdyn\_paymentday.msdyn\_name
PAYMENTMETHOD | = | msdyn\_customerpaymentmethod.msdyn\_name
PAYMENTSCHEDULE | = | msdyn\_paymentschedule.msdyn\_name
PAYMENTTERMS | = | msdyn\_paymentterm.msdyn\_name
PAYMENTTERMSBASEDAYS | = | msdyn\_paymenttermsbasedays
PRIMARYCONTACTFACEBOOK | = | msdyn\_primaryfacebookid
PRIMARYCONTACTFAXEXTENSION | = | msdyn\_faxextension
PRIMARYCONTACTLINKEDIN | = | msdyn\_primarylinkedinid
TAXEXEMPTNUMBER | = | msdyn\_taxexemptnumber
VENDORACCOUNT | = | msdyn\_vendor.msdyn\_vendoraccountnumber
PRIMARYCONTACTEMAILDESCRIPTION | = | msdyn\_emailaddress1description
PRIMARYCONTACTFACEBOOKDESCRIPTION | = | msdyn\_primaryfacebookdescription
PRIMARYCONTACTFAXDESCRIPTION | = | msdyn\_faxdescription
PRIMARYCONTACTLINKEDINDESCRIPTION | = | msdyn\_primarylinkedindescrption
PRIMARYCONTACTEMAILDESCRIPTION | = | msdyn\_telephone1description
PRIMARYCONTACTPHONEEXTENSION | = | msdyn\_telephone1extension
PRIMARYCONTACTTWITTERDESCRIPTION | = | msdyn\_primarytwitteriddescription
PRIMARYCONTACTURLDESCRIPTION | = | msdyn\_websiteurldescription
LANGUAGEID | \<\< | žádná
DELIVERYADDRESSSTREET | = | address1\_line1
DELIVERYADDRESSSTATE | = | address1\_stateorprovince
žádná | \>\> | address1\_addresstypecode
žádná | \>\> | customertypecode
PARTYTYPE | \<\< | žádná
PARTYNUMBER | = | msdyn\_partynumber

## <a name="customer-v3-to-contact"></a>Odběratel V3 na kontakt

Tato šablona synchronizuje hlavní data o zákaznících pro spotřebitele a koncové uživatele mezi aplikacemi Finance and Operations a dalšími aplikacemi Dynamics 365.

<!-- ![](media/dual-write-contact-1.png) -->
<!-- ![](media/dual-write-contact-2.png) -->

Zdrojové pole | Typ mapování | Cílové pole
---|---|---
žádná | \>\> | msdyn\_sellable
PARTYTYPE | \<\< | žádná
PARTYNUMBER | = | msdyn\_partynumber
CUSTOMERACCOUNT | = | msdyn\_contactpersonid
CUSTOMERGROUPID | = | msdyn\_customergroupid.msdyn\_groupid
PERSONFIRSTNAME | = | firstname
PERSONLASTNAME | = | lastname
PERSONMIDDLENAME | = | middlename
PERSONPROFESSIONALTITLE | = | jobtitle
PERSONGENDER | \>\< | gendercode
PERSONMARITALSTATUS | \>\< | familystatuscode
LANGUAGEID | \<\< | žádná
ADDRESSCITY | = | address1\_city
ADDRESSCOUNTRYREGIONISOCODE | = | address1\_country
ADDRESSCOUNTY | = | address1\_county
ADDRESSLATITUDE | \> | address1\_latitude
ADDRESSLONGITUDE | \> | address1\_longitude
ADDRESSLOCATIONROLES | \<\< | žádná
ADDRESSSTATE | = | address1\_stateorprovince
ADDRESSSTREET | = | address1\_line1
ADDRESSZIPCODE | = | address1\_postalcode
ADDRESSPOSTBOX | = | address1\_postofficebox
žádná | \>\> | address1\_addresstypecode
INVOICEADDRESSCITY | = | address2\_city
INVOICEADDRESSCOUNTRYREGIONISOCODE | = | address2\_country
INVOICEADDRESSCOUNTY | = | address2\_county
INVOICEADDRESSLATITUDE | \> | address2\_latitude
INVOICEADDRESSLONGITUDE | \> | address2\_longitude
INVOICEADDRESSSTATE | = | address2\_stateorprovince
INVOICEADDRESSSTREET | = | address2\_line1
INVOICEADDRESSZIPCODE | = | address2\_postalcode
žádná | \>\> | address2\_addresstypecode
DELIVERYADDRESSCITY | = | address3\_city
DELIVERYADDRESSCOUNTRYREGIONISOCODE | = | address3\_country
DELIVERYADDRESSCOUNTY | = | address3\_county
DELIVERYADDRESSLATITUDE | \> | address3\_latitude
DELIVERYADDRESSLONGITUDE | \>\> | address3\_longitude
DELIVERYADDRESSSTATE | = | address3\_stateorprovince
DELIVERYADDRESSSTREET | = | address3\_line1
DELIVERYADDRESSZIPCODE | = | address3\_postalcode
žádná | \>\> | address3\_addresstypecode
PRIMARYCONTACTEMAIL | = | emailaddress1
PRIMARYCONTACTEMAILDESCRIPTION | = | msdyn\_emailaddress1description
PRIMARYCONTACTFAX | = | fax
PRIMARYCONTACTFAXDESCRIPTION | = | msdyn\_faxdescription
PRIMARYCONTACTFAXEXTENSION | = | msdyn\_faxextension
IDENTIFICATIONNUMBER | = | msdyn\_identificationnumber
PARTYCOUNTRY | = | msdyn\_partycountry
PARTYSTATE | = | msdyn\_partystateprovince
PRIMARYCONTACTFACEBOOK | = | msdyn\_primaryfacebookid
PRIMARYCONTACTFACEBOOKDESCRIPTION | = | msdyn\_primaryfacebookdescription
PRIMARYCONTACTLINKEDIN | = | msdyn\_primaryinkedinid
PRIMARYCONTACTLINKEDINDESCRIPTION | = | msdyn\_primarylinkedindescrption
PRIMARYCONTACTPHONE | = | telephone1
PRIMARYCONTACTEMAILDESCRIPTION | = | msdyn\_telephone1description
PRIMARYCONTACTPHONEEXTENSION | = | msdyn\_telephone1extension
PRIMARYCONTACTTWITTER | = | msdyn\_primarytwitterid
PRIMARYCONTACTTWITTERDESCRIPTION | = | msdyn\_primarytwitteriddescription
PRIMARYCONTACTURL | = | websiteurl
PRIMARYCONTACTURLDESCRIPTION | = | msdyn\_websiteurldescription
SALESCURRENCYCODE | = | transactioncurrencyid.isocurrencycode
SALESMEMO | = | popis

## <a name="contacts"></a>Kontakty

Tato šablona synchronizuje všechny informace o primárních, sekundárních a terciárních kontaktech pro zákazníky i dodavatele, mezi aplikacemi Finance and Operations a dalšími aplikacemi Dynamics 365.

<!-- ![](media/dual-write-contacts.png) -->

Zdrojové pole | Typ mapování | Cílové pole
---|---|---
CONTACTPERSONPARTYNUMBER | = | msdyn\_partynumber
ASSOCIATEDCONTACTTYPE | \<\< | žádná
FIRSTNAME | = | firstname
MIDDLENAME | = | middlename
LASTNAME | = | lastname
ASSOCIATEDCONTACTNUMBER | = | msdyn\_vendorcontactid.msdyn\_vendoraccountnumber
PRIMARYADDRESSCITY | = | address1\_city
PRIMARYADDRESSCOUNTRYREGIONID | = | address1\_country
PRIMARYADDRESSCOUNTYID | = | address1\_county
PRIMARYFAXNUMBER | = | fax
PRIMARYADDRESSSTATEID | = | address1\_stateorprovince
PRIMARYADDRESSSTREET | = | address1\_line1
PRIMARYADDRESSZIPCODE | = | address1\_postalcode
PRIMARYPHONENUMBER | = | telephone1
PRIMARYEMAILADDRESS | = | emailaddress1
EMPLOYMENTDEPARTMENT | = | department
NOTES | = | popis
GENDER | \>\< | gendercode
GOVERNMENTIDENTIFICATIONNUMBER | = | governmentid
PRIMARYURL | = | websiteurl
MARITALSTATUS | \>\< | familystatuscode
ISRECEIVINGDIRECTMAIL | \>\< | donotemail
EMPLOYMENTPROFESSION | = | jobtitle
SPOUSENAME | = | spousesname
žádná | \>\> | msdyn\_contactforvendor
žádná | \>\> | msdyn\_contactpersonid

## <a name="customer-groups"></a>Skupiny odběratelů

Tato šablona synchronizuje informace o skupinách odběratelů mezi Finance and Operations a dalšími aplikacemi Dynamics 365.

<!-- ![](media/dual-write-customer-groups.png) -->

Zdrojové pole | Typ mapování | Cílové pole
---|---|---
CUSTOMERGROUPID | = | msdyn\_groupid
POPIS | = | msdyn\_description
ISSALESTAXINCLUDEDINPRICE | \>\< | msdyn\_issalestaxincludedinprice
PAYMENTTERMID | = | msdyn\_paymenttermid.msdyn\_name
CLEARINGPERIODPAYMENTTERMNAME | = | msdyn\_clearingperiodpaymenttermname.msdyn\_name

## <a name="customer-payment-methods"></a>Způsob platby odběratele

Tato šablona synchronizuje informace o způsoby platby odběratelů mezi Finance and Operations a dalšími aplikacemi Dynamics 365.

<!-- ![](media/dual-write-customer-payment-methods.png) -->

Zdrojové pole | Typ mapování | Cílové pole
---|---|---
NÁZEV | = | msdyn\_name
ACCOUNTTYPE | \>\< | msdyn\_accounttype
DISCOUNTGRACEPERIODDAYS | = | msdyn\_discountgraceperioddays
BRIDGINGPOSTINGENABLED | \>\< | msdyn\_bridgingpostingenabled
ISSEPA | \>\< | msdyn\_issepa
LASTFILENUMBER | = | msdyn\_lastfilenumber
LASTFILENUMBERTODAY | = | msdyn\_lastfilenumbertoday
POPIS | = | msdyn\_description
PAYMENTTYPE | \>\< | msdyn\_paymenttype
CREATEANDDRAWBILLOFEXCHANGEDURINGINVOICEPOSTING | \>\< | msdyn\_invoiceupdate
PAYMENTSTATUS | \>\< | msdyn\_paymentstatus
SUMBYPERIOD | \>\< | msdyn\_sumbyperiod
ENABLEPOSTDATEDCHECKCLEARINGPOSTING | \>\< | msdyn\_enablepostdatescheckclearingposting
BILLOFEXCHANGEDRAFTTYPE | \>\< | msdyn\_billofexchangedrafttype
DIRECTDEBIT | \>\< | msdyn\_directdebit

## <a name="loyalty-cards"></a>Věrnostní karty

Tato šablona synchronizuje informace o věrnostních kartách odběratelů mezi Finance and Operations a dalšími aplikacemi Dynamics 365.

<!-- ![](media/dual-write-loyalty-cards.png) -->

Zdrojové pole | Typ mapování | Cílové pole
---|---|---
CARDNUMBER | = | msdyn\_cardnumber
CARDTENDERTYPE | \>\< | msdyn\_cardtendertype
PARTYNUMBER | = | msdyn\_partynumber
REPLACEMENTCARDNUMBER | \> | msdyn\_replacementcardnumber
OMOPERATINGUNITNUMBER | = | msdyn\_operatingunitnumber
LOYALTYENROLLMENTDATE | = | msdyn\_enrollmentdate

## <a name="payment-schedules"></a>Platební kalendáře

Tato šablona synchronizuje referenční data platebního kalendáře pro spotřebitele a dodavatele mezi aplikacemi Finance and Operations a dalšími aplikacemi Dynamics 365.

<!-- ![](media/dual-write-payment-schedules.png) -->

Zdrojové pole | Typ mapování | Cílové pole
---|---|---
NÁZEV | = | msdyn\_name
POPIS | = | msdyn\_description
ALLOCATIONMETHOD | \>\< | msdyn\_allocationmethod
PAYMENTFREQUENCYUNITS | \>\< | msdyn\_paymentfrequencyunit
PAYMENTFREQUENCY | = | msdyn\_paymentfrequency
NUMBEROFPAYMENTS | = | msdyn\_numberofpayments
FIXEDPAYMENTAMOUNT | = | msdyn\_fixedpaymentamount
MINIMUMPAYMENTAMOUNT | = | msdyn\_minimumpaymentamount
SALESTAXALLOCATIONMETHOD | \>\< | msdyn\_salestaxallocationmethod
NOTES | = | msdyn\_note

## <a name="payment-schedule-lines"></a>Řádky platebního kalendáře

Synchronizuje referenční data řádků platebního kalendáře pro spotřebitele a dodavatele mezi aplikacemi Finance and Operations a dalšími aplikacemi Dynamics 365.

<!-- ![](media/dual-write-payment-schedule-lines.png) -->

Zdrojové pole | Typ mapování | Cílové pole
---|---|---
PAYMENTSCHEDULENAME | = | msdyn\_paymentschedule.msdyn\_name
PAYMENTSCHEDULENAME | \> | msdyn\_name
LINENUMBER | = | msdyn\_linenumber
PERIODSAFTERDUEDATE | = | msdyn\_periodsafterduedate
PERCENTORAMOUNT | \>\< | msdyn\_percentoramount
PERCENTORAMOUNTVALUE | = | msdyn\_percentoramountvalue

## <a name="payment-days"></a>Dny platby

Tato šablona synchronizuje referenční data dnů platby pro spotřebitele a dodavatele mezi aplikacemi Finance and Operations a dalšími aplikacemi Dynamics 365.

<!-- ![](media/dual-write-payment-days.png) -->

Zdrojové pole | Typ mapování | Cílové pole
---|---|---
NÁZEV | = | msdyn\_name
POPIS | = | msdyn\_description

## <a name="payment-day-lines"></a>Řádky denní platby

Tato šablona synchronizuje referenční data řádků dně platby pro spotřebitele a dodavatele mezi aplikacemi Finance and Operations a dalšími aplikacemi Dynamics 365.

<!-- ![](media/dual-write-payment-day-lines.png) -->

Zdrojové pole | Typ mapování | Cílové pole
---|---|---
CDSINTEGRATIONKEY | = | msdyn\_paymentdaylineid
FREQUENCY | \>\< | msdyn\_frequency
DAYOFWEEK | \>\< | msdyn\_dayofweek
DAYOFMONTH | = | msdyn\_dayofmonth
NÁZEV | = | msdyn\_paymentday.msdyn\_name

## <a name="payment-terms"></a>Platební podmínky

Tato šablona synchronizuje referenční data platebních podmínek pro spotřebitele a dodavatele mezi aplikacemi Finance and Operations a dalšími aplikacemi Dynamics 365.

<!-- ![](media/dual-write-payment-terms.png) -->

Zdrojové pole | Typ mapování | Cílové pole
---|---|---
POPIS | = | msdyn\_description
NÁZEV | = | msdyn\_name
NUMBEROFMONTHS | = | msdyn\_numberofmonth
CUTOFFDAYOFMONTH | = | msdyn\_cutoffdayofmonth
ISCASHPAYMENT | \>\< | msdyn\_iscashpayment
NUMBEROFDAYS | = | msdyn\_days
ISCERTIFIEDCOMPANYCHECK | \>\< | msdyn\_iscertifiedcompanycheck
ISDEFAULTPAYMENTTERM | \>\< | msdyn\_isdefaultpaymentterm
CREDITCARDPAYMENTTYPE | \>\< | msdyn\_creditcardpaymenttype
CREDITCARDCREDITCHECKTYPE | \>\< | msdyn\_creditcardcreditchecktype
PAYMENTDAYNAME | = | msdyn\_paymentdayname.msdyn\_name
PAYMENTMETHODTYPE | \>\< | msdyn\_paymentmethodtype
PAYMENTSCHEDULENAME | = | msdyn\_paymentschedulename.msdyn\_name

## <a name="name-affixes"></a>Přípony názvů

Tato šablona synchronizuje referenční data přípon názvů pro spotřebitele a dodavatele mezi aplikacemi Finance and Operations a dalšími aplikacemi Dynamics 365.

<!-- ![](media/dual-write-name-affixes.png) -->

Zdrojové pole | Typ mapování | Cílové pole
---|---|---
AFFIX | = | msdyn\_affix
TYP | \>\< | msdyn\_affixtype
POPIS | = | msdyn\_description
