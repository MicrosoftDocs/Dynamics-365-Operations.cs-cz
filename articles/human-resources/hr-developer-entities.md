---
title: Tabulky Dataverse
description: Microsoft Dynamics 365 Human Resources používá Dataverse k povolení scénářů rozšiřitelnosti a integrace.
author: twheeloc
ms.date: 12/08/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 51be30f10c8e5f5e962f54f720f66c712a785835
ms.sourcegitcommit: bdee5e642d417a13abdb778c14ec5f2dbbf8dee7
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/09/2022
ms.locfileid: "9838575"
---
# <a name="dataverse-tables"></a>Tabulky Dataverse


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Microsoft Dynamics 365 Human Resources používá Dataverse k povolení scénářů rozšiřitelnosti a integrace.

> [!NOTE]
> Entity Human Resources odpovídají Dataverse tabulkám. Pro více informací o Dataverse (dříve Common Data Service) a aktualizacích terminologie, viz [Co je Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)

Následující tabulky Dataverse jsou k dispozici na základě entit lidských zdrojů.

Další informace o známých problémech viz [Hledání problémů ve službě Lifecycle Services (LCS)](/dev-itpro/lifecycle-services/issue-search-lcs).

## <a name="benefit-tables"></a>Tabulky výhod

| Název | Tabulka | Známé problémy  | Stav |
| --- | --- |    --------|----------  |
| Frekvence výpočtu zaměstnaneckých výhod | cdm_benefitcalculationfrequency |     |     |
| Platební období – interval provádění výpočtu zaměstnaneckých výhod | cdm_benefitcalculationfrequencypayperiod |     |     |
| Sazba výpočtu zaměstnanecké výhody | cdm_benefitcalculationrate |    |     |
| Podrobnosti sazby výpočtu zaměstnanecké výhody | cdm_benefitcalculationratedetail |753225 | Vyřešeno  |
| Možnost zaměstnaneckých výhod | cdm_benefitoption |    |     |
| Plán zaměstnaneckých výhod | cdm_benefitplan (není povoleno pro podporu vlastních polí) |    |     |
| Typ zaměstnanecké výhody | cdm_benefittype |    |     |

## <a name="business-process-tasks-tables"></a>Tabulky úkolů obchodního procesu

| Název | Tabulka |Známé problémy  | Stav |
| --- | --- |   --------|----------   |
| Kalendář obchodních procesů | cdm_businessprocesscalendar | 751867 | Vyřešeno |
| Přiřazení skupiny obchodních procesů | cdm_businessprocessgroupassignment | 751869  751863 | Aktivní|
| Skupina úkolů knihovny obchodních procesů | cdm_businessprocesslibrarytaskgroup |751866 | Zavřeno |
| Fáze obchodního procesu | cdm_businessprocessstage |      |     |
| Záhlaví šablony kontrolního seznamu | cdm_businessprocesstemplateheader |     |     |
| Úkol šablony kontrolního seznamu | cdm_businessprocesstemplatetask |      |     |

## <a name="compensation-tables"></a>Tabulky Kompenzace

| Název | Tabulka |Známé problémy  | Stav |
| --- | --- | ----------      | -------    |
| Fixní plán kompenzace | cdm_compensationfixedplan |754453 | Zavřeno |
| Mřížka kompenzace | cdm_compensationgrid |             |     |
| Úroveň kompenzace | cdm_compensationlevel |           |     |
| Interval plateb kompenzace | cdm_compensationpayfrequency |                  |     |
| Nastavení referenčního bodu kompenzace | cdm_compensationreferencepointsetup |               |     |
| Linie nastavení referenčního bodu kompenzace | cdm_compensationreferencepointsetupline |             |     |
| Oblast kompenzace | cdm_compensationregion |                   |     |
| Struktura kompenzací | cdm_compensationstructure |    754456        | Zavřeno    |
| Plán variabilní kompenzace | cdm_compensationvariableplan |               |     |
| Úroveň plánu variabilní kompenzace | cdm_compensationvariableplanlevel |                |     |
| Typ plánu variabilní kompenzace | cdm_compensationvariableplantype |               |     |
| Událost fixní kompenzace | cdm_fixedcompensationevent |               |     |
| Pravidlo připsání | cdm_vestingrule |              |     |
| Fixní kompenzace pracovníka | cdm_workerfixedcompensation |              |     |

## <a name="organization-tables"></a>Organizační tabulky

| Název | Tabulka |Známé problémy  | Stav |
| --- | --- | ----------      | -------    |
| Oddělení | cdm_department |  752194    | Zavřeno    |
| Zaměstnání | cdm_employment | 762414  |  Zavřeno  |
| Společnost | cdm_company |  |     |
| Pozice | cdm_job |  |     |
| Pracovní funkce | cdm_jobfunction |        |     |
| Pracovní pozice | cdm_jobposition | 752214      | Zavřeno    |
| Typ pozice | cdm_positiontype |            |     |
| Přiřazení pracovníka k pozici | cdm_positionworkerassignmentmap | 752224    |  Zavřeno   |
| Dimenze pracovních pozic | cdm_jobpositiondimension|       |     |
| Typ práce | cdm_jobtype |      |     |
| Jazyk | cdm_language |        |     |
| Pozice | cdm_title |       |     |

> [!NOTE]
> Finanční dimenze pro **Typ pozice**, **Přiřazení pracovníka poziec** a **Zaměstnání** poskytují integraci v jediném směru do Dataverse. Aktualizace finančních dimenzí nelze v současné době synchronizovat z Dataverse do modulu Human Resources. 

## <a name="leave-and-absence-tables"></a>Tabulky Pracovní volno a absence

| Název | Tabulka | Známé problémy  | Stav |
| --- | --- |   ----------      | -------    |
| Transakce fondu pracovního volna | cdm_leavebanktransaction |  752252    |    Vyřešeno |
| Registrace pracovního volna | cdm_leaveenrollment |  752934    |Zavřeno     |
| Plán pracovního volna | cdm_leaveplan |   752232   |   Zavřeno  |
| Žádost o pracovní volno | cdm_leaverequest | 753207     | Zavřeno    |
| Podrobnosti o požadavku na dovolenou | cdm_leaverequestdetail | 753207     |   Zavřeno  |
| Typ pracovního volna | cdm_leavetype |      |     |
| Kód důvodu typu volna | cdm_leavetypereasoncode |         |     |

>[!NOTE]
>Integrace prostřednictvím duálního zápisu pomocí tabulek Dataverse pro pracovní volno a nepřítomnost je k dispozici pouze v případě, že je povolena funkce **Konfigurovat více typů pracovního volna v jednom plánu pracovního volna** v Microsoft Dynamics 365 Finance pomocí **Správy funkcí**. 

## <a name="payroll-tables"></a>Výplatní tabulky

| Název | Tabulka |Známé problémy  | Stav |
| --- | --- |  ----------      | -------    |
| Platební cyklus | cdm_paycycle |    |     |
| Platební období | cdm_payperiod |          |     |
| Kód příjmů mzdy | cdm_payrollearningcode |   754458        |   Zavřeno  |
| Úhrady na bankovní účet | cdm_bankaccountdisbursement |    751904     |   Zavřeno  |
| Daňová oblast | cdm_taxregion |          |     |

## <a name="worker-tables"></a>Tabulky pracovníků

| Název | Tabulka |Známé problémy  | Stav |
| --- | --- |----------      | -------    |
| Pracovník | cdm_worker |    751906    |    Zavřeno |
| Adresa pracovníka | cdm_workeraddress |   754465     |Zavřeno     |
| Osobní údaj pracovníka | cdm_workerpersonaldetail |   751906     |   Zavřeno  |
| Osobní identifikační číslo pracovníka | cdm_workerpersonidentificationnumber |  766704      |   Zavřeno  |
| Typ osobní identifikace pracovníka | cdm_workerpersonidentificationtype |        |     |
| Pracovní kalendář | cdm_workcalendar |        |     |
| Datum pracovního kalendáře | cdm_workcalendarday |        |     |
| Svátek pracovního kalendáře |cdm_workcalendarholiday |        |     |
| Řádek data pracovního kalendáře | cdm_workcalendarholidayline |        |     |
| Časový interval pracovního kalenáře | cdm_workcalendartimeinterval (není povoleno pro podporu vlastních polí) |        |     |
| Bankovní účet pracovníka | cdm_workerbankaccount |        |     |

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

![Pracovník](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a>Práce a pracovní pozice

![Práce a pracovní pozice.](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a>Zam. výhody

![Zam. výhody.](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a>Kompenzace

![Kompenzace.](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a>Pracovní volno

![Pracovní volno.](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a>Pracovní kalendář

![Pracovní kalendář.](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a>Viz také

[Volba technologie integrace dat](hr-admin-integration-choose-technology.md)<br>
[Konfigurace integrace s Dataverse](hr-admin-integration-common-data-service.md)<br>
[Konfigurace virtuálních tabulek Dataverse](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[Virtuální tabulky lidských zdrojů - časté dotazy](hr-admin-virtual-entity-faq.md)<br>
[Co je Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Aktualizace terminologie](/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
