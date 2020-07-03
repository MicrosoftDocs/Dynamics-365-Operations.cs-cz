---
title: Konfigurace integrace s aplikací Finance
description: Tento článek popisuje funkce, které jsou k dispozici pro integraci z aplikace Dynamics 365 Human Resources a Dynamics 365 Finance.
author: andreabichsel
manager: AnnBe
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f542bb12910e3a4884c38a2fb24831c42a545908
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431261"
---
# <a name="configure-integration-with-finance"></a>Konfigurace integrace s aplikací Finance

Chcete-li integrovat Dynamics 365 Human Resources s Dynamics 365 Finance, můžete použít šablonu Human Resources do Finance v [Integrátoru dat](https://docs.microsoft.com/powerapps/administrator/data-integrator). Šablona Human Resources do Finance umožňuje tok dat pro úlohy, pozice a pracovníky. Šablona umožňuje tok dat z Human Resources do Finance, ale neumožňuje data tok z Finance do Human Resources.

![Tok integrace z Human Resources do Finance](./media/hr-admin-integration-finance-flow.png)

Řešení Human Resources do Finance poskytuje následující typy synchronizace dat:

- Udržujte úlohy v Human Resources a synchronizujte je z Human Resources do Finance
- Udržujte pozice a přiřazení pozice v Human Resources a synchronizujte je z Human Resources do Finance
- Udržujte zaměstnání v Human Resources a synchronizujte je z Human Resources do Finance
- Udržujte pracovníky a adresy pracovníků v Human Resources a synchronizujte je z Human Resources do Finance

## <a name="system-requirements-for-human-resources"></a>Systémové požadavky pro Human Resources

Řešení integrace vyžaduje následující verze aplikací Human Resources a Finance: 

- Dynamics 365 Human Resources u Common Data Service
- Dynamics 365 Finance verze 7.2 a novější

## <a name="template-and-tasks"></a>Šablona a úkoly

Chcete-li získat přístup k Human Resources do Finance.

1. Otevřete [centrum pro správu Power Apps](https://admin.powerapps.com/). 

2. Vyberte **Projekty** a poté v pravém horním rohu vyberte možnost **Nový projekt**. Vytvořte nový projekt pro každou právnickou osobu, kterou chcete integrovat do aplikace Finance.

3. Vyberte **Human Resources (Human Resources Common Data Service do Finance**), chcete-li synchronizovat záznamy z modulu Human Resources do Finance.

Následující šablony používají základní úlohy k synchronizaci záznamů z Human Resources do Finance:

- **Pracovní funkce do pracovní funkce kompenzace**
- **Oddělení do provozní jednotky**
- **Typy práce do typu práce kompenzace**
- **Práce do prací**
- **Práce do podrobnosti práce**
- **Typy pozic do typu pozice**
- **Pracovní pozice do základní pozice**
- **Pracovní pozice do podrobností pozice**
- **Pracovní pozice do trvání pozice**
- **Pracovní pozice do hierarchií pozic**
- **Pracovníci do pracovníka**
- **Zaměstnání do zaměstnání**
- **Zaměstnání do podrobnosti zaměstnání**
- **Přiřazení pracovníka pozice do přiřazení pracovníka pozice**
- **Adresy pracovníka na poštovní adresu pracovníka V2**

## <a name="template-mappings"></a>Mapování šablony

V následujících tabulkách mapování šablony název úlohy obsahuje entity použité v jednotlivých aplikacích. Zdroj (Human Resources) je nalevo a cíl (Finance) je napravo.

### <a name="job-functions-to-compensation-job-function"></a>Pracovní funkce do pracovní funkce kompenzace

| Entita Common Data Service (zdroj) | Entita Finance (cíl) |
|-------------------------------------|---------------------------------------------|
| cdm_name (cdm_Job   Název funkce)  | JOBFUNCTIONID   (JOBFUNCTIONID)            |
| cdm_description   (cdm_description) | DESCRIPTION   (DESCRIPTION)                 |

### <a name="departments-to-operating-unit"></a>Oddělení do provozní jednotky

| Entita Common Data Service (zdroj)           | Entita Finance (cíl) |
|-----------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                           | NAME (NÁZEV)                                 |
| cdm_departmentnumber   (cdm_departmentnumber) | OPERATINGUNITNUMBER   (OPERATINGUNITNUMBER) |
|                                               | OPERATINGUNITTYPE   (OPERATINGUNITTYPE)     |
| cdm_description   (cdm_description)           | NAMEALIAS   (NAMEALIAS)                     |

### <a name="job-types-to-compensation-job-type"></a>Typy práce do typu práce kompenzace

| Entita Common Data Service (zdroj)   | Entita Finance (cíl) |
|---------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                   | JOBTYPEID   (JOBTYPEID)                     |
| cdm_description   (cdm_description)   | DESCRIPTION   (POPIS)                 |
| cdm_exemptstatus   (cdm_exemptstatus) | EXEMPTSTATUS   (EXEMPTSTATUS)               |

### <a name="jobs-to-jobs"></a>Práce do prací

| Entita Common Data Service (zdroj)                           | Entita Finance (cíl)           |
|---------------------------------------------------------------|-------------------------------------------------------|
| cdm_name (cdm_name)                                           | JOBID (JOBID)                                         |
| cdm_maximumnumberofpositions   (cdm_maximumnumberofpositions) | MAXIMUMNUMBEROFPOSITIONS   (MAXIMUMNUMBEROFPOSITIONS) |
| cdm_allowedunlimitedpositions   (cdm_allowunlimitedpositions) | ALLOWUNLIMITEDPOSITIONS   (ALLOWUNLIMITEDPOSITIONS)   |
| cdm_description   (cdm_description)                           | DESCRIPTION   (POPIS)                           |
| cdm_jobdescription   (cdm_jobdescription)                     | JOBDESCRIPTION   (JOBDESCRIPTIONS)                    |

### <a name="jobs-to-job-detail"></a>Práce do podrobnosti práce

| Entita Common Data Service (zdroj)                             | Entita Finance (cíl) |
|-----------------------------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                                             | JOBID (JOBID)                               |
| cdm_jobtypeid.cdm_name   (Job Type (Job Type Name))             | JOBTYPEID   (JOBTYPEID)                     |
| cdm_jobfunctionid.cdm_name   (Pracovní funkce (Název pracovní funkce)) | FUNCTIONID   (FUCNTIONID)                   |
| cdm_validfrom   (Valid From)                                    | VALIDFROM   (VALIDFROM)                     |
| cdm_validto (Valid To)                                        | VALIDTO (VALIDTO)                           |
| cdm_defaultfulltimeequivalent   (Default Full-time Equivalent)   | FULLTIMEEQUIVALENT   (FULLTIMEEQUIVALENT)   |

### <a name="position-types-to-position-type"></a>Typy pozic do typu pozice

| Entita Common Data Service (zdroj)       | Entita Finance (cíl) |
|-------------------------------------------|---------------------------------------------|
| cdm_name (cdm_name)                       | POSITIONTYPEID   (POSITIONTYPEID)           |
| cdm_description   (cdm_description)       | DESCRIPTION   (DESCRIPTION)                 |
| cdm_classification   (cdm_classification) | CLASSIFICATION   (CLASSIFICATION)           |

### <a name="job-positions-to-base-position"></a>Pracovní pozice do základní pozice

| Entita Common Data Service (zdroj)           | Entita Finance (cíl) |
|-----------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber   (Job Position Number) | POSITIONID (POSITIONID)                      |

### <a name="job-positions-to-position-details"></a>Pracovní pozice do podrobností pozice

| Entita Common Data Service (zdroj)              | Entita Finance (cíl)       |
|--------------------------------------------------------------------------|---------------------------------------------------|
| cdm_jobpositionnumber  (Job Position Number)                            | POSITIONID (POSITIONID)                             |
| cdm_jobid.cdm_name   (Job (Name))                                        | JOBID (JOBID)                                    |
| cdm_description   (cdm_description)                                        | DESCRIPTION   (DESCRIPTION)                       |
| cdm_departmentid.cdm_departmentnumber   (Oddělení (číslo oddělení)) | DEPARTMENTNUMBER   (DEPARTMENTNUMBER)             |
| cdm_positiontypeid.cdm_name   (Typ pozice (Název))                     | POSITIONTYPEID   (POSITIONTYPEID)                 |
| cdm_avaialableforassignment   (Dostupné pro přiřazení)                 | AVAILABLEFORASSIGNMENT   (AVAILABLEFORASSIGNMENT) |
| cdm_validfrom   (platnost od)                                            | VALIDFROM   (VALIDFROM)                           |
| cdm_validto (platnost do)                                                 | VALIDTO (VALIDTO)                               |
| cdm_fulltimeequivalent   (Ekvivalent plného úvazku)                           | FULLTIMEEQUIVALENT   (FULLTIMEEQUIVALENT)         |

### <a name="job-positions-to-position-durations"></a>Pracovní pozice do trvání pozice

| Entita Common Data Service (zdroj)             | Entita Finance (cíl) |
|-------------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber   (Job Position Number)   | POSITIONID (POSITIONID)                      |
| Calculated   Activation (Vypočtená aktivace) | VALIDFROM (VALIDFROM)                        |
| Calculated   Retirement (vypočtený důchod) | VALIDTO (VALIDTO)                         |

### <a name="job-positions-to-position-hierarchies"></a>Pracovní pozice do hierarchií pozic

| Entita Common Data Service (zdroj)        | Entita Finance (cíl) |
|-----------------------------------------------------------------------------------------------|---------------------------------------------|
| cdm_jobpositionnumber   (Job Position Number)                                                 | POSITIONID(POSITIONID)                      |
| cdm_parentjobpositionid.cdmjobpositionnumber   (cdm_parentjobpositionid.cdmjobpositionnumber) | PARENTPOSITIONID (PARENTPOSITIONID)         |
| cdm_validfrom   (platnost od)                                                                  | VALIDFROM   (VALIDFROM)                     |
| cdm_validto (platnost do)                                                                      | VALIDTO (VALIDTO)                           |
| HIERARCHYTYPENAME   (HIERARCHYTYPENAME)                                                       | HIERARCHYTYPENAME   (HIERARCHYTYPENAME)     |


### <a name="workers-to-worker"></a>Pracovníci do pracovníka
| Entita Common Data Service (zdroj)           | Entita Finance (cíl)       |
|-----------------------------------------------|---------------------------------------------------|
| cdm_birthdate   (cdm_birthdate)               | BIRTHDATE   (BIRTHDATE)                           |
| cdm_gender   (cdm_gender)                     | GENDER (POHLAVÍ)                                   |
| cdm_primaryaddress   (cdm_primaryaddress)     | PRIMARYCONTACTEMAIL   (PRIMARYCONTACTEMAIL )      |
| cdm_primarytelephone   (cdm_primarytelephone) | PRIMARYCONTACTPHONE   (PRIMARYCONTACTPHONE)       |
| cdm_facebookidentity   (cdm_facebookidentity) | PRIMARYCONTACTFACEBOOK   (PRIMARYCONTACTFACEBOOK) |
| cdm_twitteridentity   (cdm_twitteridentity)   | PRIMARYCONTACTTWITTER   (PRIMARYCONTACTTWITTER)   |
| cdm_linkedinIdentity   (cdm_linkedinIdentity) | PRIMARYCONTACTLINKEDIN   (PRIMARYCONTACTLINKEDIN) |
| cdm_websiteurl   (cdm_websiteurl)             | PRIMARYCONTACTURL   (PRIMARYCONTACTURL)           |
| cdm_firstname   (cdm_firstname)               | FIRSTNAME   (FIRSTNAME)                           |
| cdm_middlename   (cdm_middlename)             | MIDDLENAME   (MIDDLENAME)                         |
| cdm_lastname   (cdm_lastname)                 | LASTNAME (LASTNAME)                               |
| cdm_workernumber   (cdm_workernumber)         | PERSONNELNUMBER   (PERSONNELNUMBER)               |
| cdm_type (cdm_type)                           | WORKERTYPE   (WORKERTYPE)                         |
| cdm_state   (cdm_state)                       | WORKSTATUS   (WORKERSTATUS)                       |

### <a name="employments-to-employment"></a>Zaměstnání do zaměstnání

| Entita Common Data Service (zdroj)                             | Entita Finance (cíl) |
|-----------------------------------------------------------------|---------------------------------------------|
| cdm_employmentstartdate   (cdm_employmentstartdate)             | EMPLOYMENTSTARTDATE   (EMPLOYMENTSTARTDATE) |
| cdm_employmentenddate   (cdm_employmentenddate)                 | EMPLOYMENTENDDATE   (EMPLOYMENTENDDATE)     |
| cdm_workertype   (cdm_workertype)                               | WORKERTYPE   (WORKERTYPE)                   |
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)         |
| cdm_companyid.cdm_companycode   (cdm_companyid.cdm_companycode) | LEGALENTITYID   (LEGALENTITYID)             |

### <a name="employments-to-employment-detail"></a>Zaměstnání do podrobnosti zaměstnání

| Entita Common Data Service (zdroj)                             | Entita Finance (cíl)   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_employmentstartdate   (cdm_employmentstartdate)             | EMPLOYMENTSTARTDATE   (EMPLOYMENTSTARTDATE)   |
| cdm_employmentenddate   (cdm_employmentenddate)                 | EMPLOYMENTENDDATE   (EMPLOYMENTENDDATE)       |
| cdm_validfrom   (platnost od)                                    | VALIDFROM   (VALIDFROM)                       |
| cdm_validto (platnost do)                                        | VALIDTO (VALIDTO)                             |
| cdm_workerstartdate   (cdm_workerstartdate)                     | WORKERSTARTDATE   (WORKERSTARTDATE)           |
| cdm_lastdateworked   (cdm_lastdateworked)                       | LASTDATEWORKED   (LASTDATEWORKED)             |
| cdm_transitiondate   (cdm_transitiondate)                       | TRANSITIONDATE   (TRANSITIONDATE)             |
| cdm_employerunitofnotice   (cdm_employerunitofnotice)           | EMPLOYERUNITOFNOTICE   (EMPLOYERUNITOFNOTICE) |
| cdm_workerunitofnotice   (cdm_workerunitofnotice)               | WORKERUNITOFNOTICE   (WORKERUNITOFNOTICE)     |
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)           |
| cdm_companyid.cdm_companycode   (cdm_companyid.cdm_companycode) | LEGALENTITYID   (LEGALENTITYID)               |
| cdm_employernoticeamount   (cdm_employernoticeamount)           | EMPLOYERNOTICEAMOUNT   (EMPLOYERNOTICEAMOUNT) |
| cdm_workernoticeamount   (cdm_workernoticeamount )              | WORKERNOTICEAMOUNT   (WORKERNOTICEAMOUNT)     |

### <a name="position-worker-assignment-to-position-worker-assignments"></a>Přiřazení pracovníka pozice do přiřazení pracovníka pozice

| Entita Common Data Service (zdroj)                             | Entita Finance (cíl)   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)           |
| cdm_jobpositionnumber   (Job Position Number)                   | POSITIONID(POSITIONID)                        |
| cdm_validfrom   (platnost od)                                    | VALIDFROM   (VALIDFROM)                       |
| cdm_validto (platnost do)                                        | VALIDTO (VALIDTO)                             |

### <a name="worker-addresses-to-worker-postal-address-v2"></a>Adresy pracovníka na poštovní adresu pracovníka V2

| Entita Common Data Service (zdroj)                             | Entita Finance (cíl)   |
|-----------------------------------------------------------------|-----------------------------------------------|
| cdm_workerid.cdm_workernumber   (cdm_workerid.cdm_workernumber) | PERSONNELNUMBER   (PERSONNELNUMBER)           |
| cdm_addresstype   (cdm_addresstype)                             | ADDRESSLOCATIONROLES   (ADDRESSLOCATIONROLES) |
| cdm_line1   (cdm_line1)                                         | ADDRESSSTREET   (ADDRESSSTREET)               |
| cdm_city (cdm_city)                                             | ADDRESSCITY   (ADDRESSCITY)                   |
| cdm_stateorprovince   (cdm_stateorprovince)                     | ADDRESSSTATE   (ADDRESSSTATE)                 |
| cdm_postalcode   (cdm_postalcode)                               | ADDRESSZIPCODE(ADDRESSZIPCODE)                |
| cdm_countryregion   (cdm_countryregion)                         | ADDRESSCOUNTRYREGION(ADDRESSCOUNTRYREGION)    |
| cdm_addressnumber   (cdm_addressnumber)                         | ADDRESSLOCATIONID(ADDRESSLOCATIONID)          |
| cdm_ispreferred   (cdm_ispreferred)                             | ISPRIMARY   (ISPRIMARY)                       |
| cdm_county   (cdm_county)                                       | ADDRESSCOUNTYID(ADDRESSCOUNTYID)              |
| cdm_addresstype   (cdm_addresstype)                             | ADDRESSDESCRIPTION(ADDRESSDESCRIPTION)        |

## <a name="integration-considerations"></a>Předpoklady integrace

Integrace dat z Human Resources do Finance se pokusí spárovat záznamy na základě ID. Pokud dojde ke shodě, budou data v aplikaci Finance budou přepsána hodnotami v aplikaci Human Resources. K problému však může dojít, pokud se jedná o různé záznamy a bylo vygenerováno stejné ID v Human Resources nebo Finance na základě příslušné číselné řady.

Problém může nastat u **Pracovníka**, který používá **Osobní číslo** k provedení párování, a **Pozic**. Práce nepoužívají číselné řady. V důsledku toho, pokud stejné ID práce existuje jak v Human Resources, tak ve Finance, informace z Human Resources tyto informace Dynamics 365 Finance přepíší. 

Chcete-li zabránit problémům s duplicitními ID, můžete buď přidat předponu k [číselné řadě](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/number-sequence-overview?toc=/dynamics365/unified-operations/talent/toc.json), nebo nastavit počáteční číslo pro číselnou řadu, která je nad rozsahem jiného systému. 

ID místa použité pro adresu pracovníka není součástí číselné řady. Je-li adresa pracovníka integrována z Human Resources do Finance, může být vytvořen duplicitní záznam adresy v modulu Finance. 

Na následujícím obrázku je příklad mapování šablony v integrátoru dat. 

![Mapování šablony](./media/IntegrationMapping.png)