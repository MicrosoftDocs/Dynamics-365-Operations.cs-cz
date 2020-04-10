---
title: Entity Common Data Service
description: Microsoft Dynamics 365 Human Resources používá Common Data Service k povolení scénářů rozšiřitelnosti a integrace.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: c8e0288da16829c04a9b97c0a52caa8bd27cddf8
ms.sourcegitcommit: fde8045ea49d0cf26d5e7ac5a0da5c0d3d69d5bc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/26/2020
ms.locfileid: "3166491"
---
# <a name="common-data-service-entities"></a>Entity Common Data Service

Microsoft Dynamics 365 Human Resources používá Common Data Service k povolení scénářů rozšiřitelnosti a integrace.

Další informace týkající se Common Data Service získáte v tématu [Co je Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).

V Common Data Service jsou k dispozici následující entity lidských zdrojů.

## <a name="benefit-entities"></a>Entity zaměstnaneckých výhod

| Název | Celek |
| --- | --- |
| Interval provádění výpočtu zaměstnaneckých výhod | cdm_benefitcalculationfrequency |
| Platební období – interval provádění výpočtu zaměstnaneckých výhod | cdm_benefitcalculationfrequencypayperiod |
| Sazba výpočtu zaměstnanecké výhody | cdm_benefitcalculationrate |
| Podrobnosti sazby výpočtu zaměstnanecké výhody | cdm_benefitcalculationratedetail |
| Možnost zaměstnaneckých výhod | cdm_benefitoption |
| Plán zaměstnaneckých výhod | cdm_benefitplan (není povoleno pro podporu vlastních polí) |
| Typ zaměstnanecké výhody | cdm_benefittype |

## <a name="business-process-tasks-entities"></a>Entity úkolů obchodního procesu

| Název | Celek |
| --- | --- |
| Kalendář obchodních procesů | cdm_businessprocesscalendar |
| Přiřazení skupiny obchodních procesů | cdm_businessprocessgroupassignment |
| Skupina úkolů knihovny obchodních procesů | cdm_businessprocesslibrarytaskgroup |
| Fáze obchodního procesu | cdm_businessprocessstage |
| Záhlaví šablony kontrolního seznamu | cdm_businessprocesstemplateheader |
| Úkol šablony kontrolního seznamu | cdm_businessprocesstemplatetask |

## <a name="compensation-entities"></a>Entity kompenzace

| Název | Celek |
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

## <a name="organization-entities"></a>Entity organizace

| Název | Celek |
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
> Finanční dimenze pro **Typ pozice**, **Přiřazení pracovníka poziec** a **Zaměstnání** poskytují integraci v jediném směru do Common Data Service. Aktualizace finančních dimenzí nelze v současné době synchronizovat z Common Data Service do modulu Human Resources. 

## <a name="leave-and-absence-entities"></a>Entity pracovního volna a absence

| Jméno | Celek |
| --- | --- |
| Transakce fondu pracovního volna | cdm_leavebanktransaction |
| Opustit zápis | cdm_leaveenrollment |
| Plán pracovního volna | cdm_leaveplan |
| Žádost o pracovní volno | cdm_leaverequest |
| Podrobnosti o požadavku na dovolenou | cdm_leaverequestdetail |
| Typ pracovního volna | cdm_leavetype |
| Kód důvodu typu volna | cdm_leavetypereasoncode |

## <a name="payroll-entities"></a>Entita mzdy

| Název | Celek |
| --- | --- |
| Platební cyklus | cdm_paycycle |
| Mzdové období | cdm_payperiod |
| Kód příjmů mzdy | cdm_payrollearningcode |
| Úhrady na bankovní účet | cdm_bankaccountdisbursement |
| Daňová oblast | cdm_taxregion |

## <a name="worker-entities"></a>Entity pracovníků

| Název | Celek |
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

## <a name="worker-setup-entities"></a>Entity nastavení pracovníků

| Název | Celek |
| --- | --- |
| Stav veterána | cdm_veteranstatus |
| Etnický původ | cdm_ethnicorigin |
| Kód důvodu | cdm_reasoncode |
| Subjekt vydávající identifikaci osob | cdm_personidentificationissuingagency |

## <a name="competency-entities"></a>Entity kompetence

| Název | Celek |
| --- | --- |
| Typ dovednosti | cdm_skilltype |

## <a name="entity-relationship-models"></a>Modely vztahu entity

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

[Volba technologie integrace dat](hr-admin-integration-choose-technology.md)</br>
[Konfigurace integrace s Common Data Service](hr-admin-integration-common-data-service.md)
