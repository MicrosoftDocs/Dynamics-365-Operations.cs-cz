---
title: Tabulky Dataverse
description: Microsoft Dynamics 365 Human Resources používá Dataverse k povolení scénářů rozšiřitelnosti a integrace.
author: andreabichsel
manager: tfehr
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: caf8b0a5d0b24ef3619f45a6d236acae6d29c8ab
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465215"
---
# <a name="dataverse-tables"></a>Tabulky Dataverse

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dynamics 365 Human Resources používá Dataverse k povolení scénářů rozšiřitelnosti a integrace.

> [!NOTE]
> Entity Human Resources odpovídají Dataverse tabulkám. Pro více informací o Dataverse (dříve Common Data Service) a aktualizacích terminologie, viz [Co je Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)

Následující tabulky Dataverse jsou k dispozici na základě entit lidských zdrojů.

## <a name="benefit-tables"></a>Tabulky výhod

| Jméno | Tabulka |
| --- | --- |
| Frekvence výpočtu zaměstnaneckých výhod | cdm_benefitcalculationfrequency |
| Platební období – interval provádění výpočtu zaměstnaneckých výhod | cdm_benefitcalculationfrequencypayperiod |
| Sazba výpočtu zaměstnanecké výhody | cdm_benefitcalculationrate |
| Podrobnosti sazby výpočtu zaměstnanecké výhody | cdm_benefitcalculationratedetail |
| Možnost zaměstnaneckých výhod | cdm_benefitoption |
| Plán zaměstnaneckých výhod | cdm_benefitplan (není povoleno pro podporu vlastních polí) |
| Typ zaměstnanecké výhody | cdm_benefittype |

## <a name="business-process-tasks-tables"></a>Tabulky úkolů obchodního procesu

| Jméno | Tabulka |
| --- | --- |
| Kalendář obchodních procesů | cdm_businessprocesscalendar |
| Přiřazení skupiny obchodních procesů | cdm_businessprocessgroupassignment |
| Skupina úkolů knihovny obchodních procesů | cdm_businessprocesslibrarytaskgroup |
| Fáze obchodního procesu | cdm_businessprocessstage |
| Záhlaví šablony kontrolního seznamu | cdm_businessprocesstemplateheader |
| Úkol šablony kontrolního seznamu | cdm_businessprocesstemplatetask |

## <a name="compensation-tables"></a>Tabulky Kompenzace

| Jméno | Tabulka |
| --- | --- |
| Fixní plán kompenzace | cdm_compensationfixedplan |
| Mřížka kompenzace | cdm_compensationgrid |
| Úroveň kompenzace | cdm_compensationlevel |
| Interval plateb kompenzace | cdm_compensationpayfrequency |
| Nastavení referenčního bodu kompenzace | cdm_compensationreferencepointsetup |
| Linie nastavení referenčního bodu kompenzace | cdm_compensationreferencepointsetupline |
| Oblast kompenzace | cdm_compensationregion |
| Struktura kompenzací | cdm_compensationstructure |
| Plán variabilní kompenzace | cdm_compensationvariableplan |
| Úroveň plánu variabilní kompenzace | cdm_compensationvariableplanlevel |
| Typ plánu variabilní kompenzace | cdm_compensationvariableplantype |
| Událost fixní kompenzace | cdm_fixedcompensationevent |
| Pravidlo připsání | cdm_vestingrule |
| Fixní kompenzace pracovníka | cdm_workerfixedcompensation |

## <a name="organization-tables"></a>Organizační tabulky

| Jméno | Tabulka |
| --- | --- |
| Oddělení | cdm_department |
| Zaměstnání | cdm_employment |
| Společnost | cdm_company |
| Pozice | cdm_job |
| Pracovní funkce | cdm_jobfunction |
| Pracovní pozice | cdm_jobposition |
| Typ pozice | cdm_positiontype |
| Přiřazení pracovníka k pozici | cdm_positionworkerassignmentmap |
| Dimenze pracovních pozic | cdm_jobpositiondimension|
| Typ práce | cdm_jobtype |
| Jazyk | cdm_language |
| Pozice | cdm_title |

> [!NOTE]
> Finanční dimenze pro **Typ pozice**, **Přiřazení pracovníka poziec** a **Zaměstnání** poskytují integraci v jediném směru do Dataverse. Aktualizace finančních dimenzí nelze v současné době synchronizovat z Dataverse do modulu Human Resources. 

## <a name="leave-and-absence-tables"></a>Tabulky Pracovní volno a absence

| Jméno | Tabulka |
| --- | --- |
| Transakce fondu pracovního volna | cdm_leavebanktransaction |
| Registrace pracovního volna | cdm_leaveenrollment |
| Plán pracovního volna | cdm_leaveplan |
| Žádost o pracovní volno | cdm_leaverequest |
| Podrobnosti o požadavku na dovolenou | cdm_leaverequestdetail |
| Typ pracovního volna | cdm_leavetype |
| Kód důvodu typu volna | cdm_leavetypereasoncode |

## <a name="payroll-tables"></a>Výplatní tabulky

| Jméno | Tabulka |
| --- | --- |
| Platební cyklus | cdm_paycycle |
| Platební období | cdm_payperiod |
| Kód příjmů mzdy | cdm_payrollearningcode |
| Úhrady na bankovní účet | cdm_bankaccountdisbursement |
| Daňová oblast | cdm_taxregion |

## <a name="worker-tables"></a>Tabulky pracovníků

| Jméno | Tabulka |
| --- | --- |
| Pracovní podproces | cdm_worker |
| Adresa pracovníka | cdm_workeraddress |
| Osobní údaj pracovníka | cdm_workerpersonaldetail |
| Osobní identifikační číslo pracovníka | cdm_workerpersonidentificationnumber |
| Typ osobní identifikace pracovníka | cdm_workerpersonidentificationtype |
| Pracovní kalendář | cdm_workcalendar |
| Datum pracovního kalendáře | cdm_workcalendarday |
| Svátek pracovního kalendáře |cdm_workcalendarholiday |
| Řádek data pracovního kalendáře | cdm_workcalendarholidayline |
| Časový interval pracovního kalenáře | cdm_workcalendartimeinterval (není povoleno pro podporu vlastních polí) |
| Bankovní účet pracovníka | cdm_workerbankaccount |

## <a name="worker-setup-tables"></a>Tabulky nastavení pracovníků

| Jméno | Tabulka |
| --- | --- |
| Stav veterána | cdm_veteranstatus |
| Etnický původ | cdm_ethnicorigin |
| Kód důvodu | cdm_reasoncode |
| Úřad vydávající identifikaci osoby | cdm_personidentificationissuingagency |

## <a name="competency-tables"></a>Tabulky kompetencí

| Jméno | Tabulka |
| --- | --- |
| Typ dovednosti | cdm_skilltype |

## <a name="table-relationship-models"></a>Modely vztahů tabulek

### <a name="worker"></a>Pracovní podproces

![Pracovní podproces](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a>Práce a pracovní pozice

![Práce a pracovní pozice](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a>Zaměstnanecké výhody

![Zaměstnanecké výhody](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a>Kompenzace

![Kompenzace](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a>Odejít

![Odejít](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a>Pracovní kalendář

![Pracovní kalendář](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a>Viz také

[Volba technologie integrace dat](hr-admin-integration-choose-technology.md)<br>
[Konfigurace integrace s Dataverse](hr-admin-integration-common-data-service.md)<br>
[Konfigurace virtuálních tabulek Dataverse](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Virtuální tabulky lidských zdrojů - časté dotazy](hr-admin-virtual-entity-faq.md)<br>
[Co je Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[Aktualizace terminologie](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]