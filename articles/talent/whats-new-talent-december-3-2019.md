---
title: Co je nového nebo upraveného v aplikaci Dynamics 365 Talent (3. prosince 2019)
description: Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 12/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-12-03
ms.dyn365.ops.version: Talent
ms.openlocfilehash: b1ed998302762203bad736161a27a48152de65f7
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/06/2019
ms.locfileid: "2897711"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-december-3-2019"></a>Co je nového nebo upraveného v aplikaci Dynamics 365 Talent (3. prosince 2019)

Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Změny v aplikaci Attract

Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Změny v aplikaci Onboard

Tato verze obsahuje dílčí opravy chyb pro aplikaci Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Změny v Core HR

Změny popsané v této části se vztahují na číslo sestavení 8.1.2646. Čísla v závorkách v některých záhlavích se vztahují na čísla podpory v Microsoft Dynamics Lifecycle Services (LCS).

### <a name="feature-management-workspace"></a>Pracovní prostor Správa funkcí

Pracovní prostor **Správa funkcí** uvádí seznam funkcí dodaných v jednotlivých vydáních. Ve výchozím nastavení jsou nové funkce vypnuté. Pracovní prostor slouží k jejich zapnutí a zobrazení odpovídající dokumentace. Další informace o aktivaci správy funkcí naleznete v tématu [Přehled správy funkcí](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Všechny nové funkce zůstanou v náhledu nejméně 30 dnů a obvykle jsou zde 30-60 dní. Hlavní funkce jsou obvykle k dispozici v říjnu a dubnu každého roku po období náhledu. Jakmile se v pracovním prostoru **Správa funkcí** zobrazí nové funkce, můžete je zapnout. Některé funkce mohou být ve výchozím nastavení zapnuty.
 
V některých případech bude ve výchozím nastavení zapnuta integrální funkce a nelze ji vypnout (například pracovní prostor **Správa funkcí**).
 
Jakmile je funkce obecně k dispozici, může být zapnuta nebo vypnuta v provozních prostředích. Pracovní prostor **Správa funkcí** označuje, kdy bude funkce náhledu povinná. Toto datum je obvykle 1. října nebo 1. ledna, aby bylo možné vyrovnat je s pololetními plány vydávání. Nemůžete zapínat a vypínat povinné funkce. Dokud nebude povinná, můžete funkci zapnout nebo vypnout ve všech prostředích.

### <a name="add-automatic-scheduling-of-batch-job-history-cleanup-332528"></a>Přidat automatické plánování čištění historie dávkových úloh (332528)

Pomocí této změny se **Historie dávkových úloh** spouští každou noc a odstraňuje položky historie dávkových úloh starší 30 dnů.

### <a name="talent-doesnt-respond-in-worker-actions-when-identification-number-length-doesnt-match-the-identification-type-390971"></a>Talent nereaguje na akce zaměstnanců, pokud délka identifikačního čísla neodpovídá identifikačnímu typu (390971)

Tato verze opravuje problém, který se vynořil, pokud délka identifikačního čísla neodpovídá definici v rámci identifikačního typu. 

### <a name="fixed-compensation-doesnt-update-level-with-changes-to-position-details--348085"></a>Fixní kompenzace neaktualizuje úroveň s změnami na detaily pozice (348085)

Při vydání tohoto týdne určuje **Počáteční datum kompenzace** úlohu spojenou s pozicí v daném okamžiku při vytváření nového záznamu fixní kompenzace pro zaměstnance.

### <a name="workers-employees-and-contractors-lists-show-worker-type-as-both-when-they-should-only-be-worker-or-contractor-384473"></a>Seznamy pracovníků, zaměstnanců a dodavatelů zobrazují typ pracovníka jako obojí, pokud mají být pouze pracovník nebo dodavatel (384473)

Tato změna přesně odráží typ zadaného pracovníka (dodavatele nebo zaměstnance).

### <a name="email-notifications-for-new-hire-actions-dont-contain-name-information-due-to-security-policies-383402"></a>Upozornění e-mailem pro nové akce přijetí neobsahují informace o názvech z důvodu zásad zabezpečení (383402)

Tato změna opraví informace zobrazené v poli křestní jméno nebo příjmení v zástupných symbolech pro pracovní postup, pokud je rozšířené zabezpečení povoleno.

### <a name="system-allows-two-full-day-leave-requests-for-the-same-day-379284"></a>Systém umožňuje dvě žádosti o celodenní dovolenou za tentýž den (379284)

Při této změně nemůžete vydat dvě žádosti o volno na tentýž den. 

### <a name="address-changes-list-should-be-sorted-by-effective-date-352798"></a>Seznam změn adres by měl být seřazen podle data platnosti (352798)

Při této změně je nyní seznam změn adres seřazen podle **Data platnosti**.

### <a name="leave-requests-should-allow-deletes-from-common-data-service-to-talent-376999"></a>Požadavky na dovolenou by měly umožnit odstranění z Common Data Service do Talentu (376999)

Při této změně mohou být vytvořené a zrušené požadavky na dovolenou smazány z Common Data Service a pak odstraněny z Talentu.

### <a name="delete-earning-codes-is-allowed-when-the-same-earning-code-is-assigned-to-an-employee-371792"></a>Pokud je přiřazen stejný kód pro zaměstnance (371792), je povoleno odstranit kódy příjmů.

V této verzi musíte nejprve odstranit kód příjmu od zaměstnance a teprve potom odstranit kód příjmu ze systému.

### <a name="leave-and-absence-workflow-with-two-approval-stages-fails-to-complete--391116"></a>Dokončení pracovního postupu pro dovolenou a absenci se dvěma etapami schválení (391116)

Při této změně pracovní postup pro dovolenou a absenci pokračuje všemi kroky, pokud je pro požadavek nakonfigurována více než jedna fáze schválení.

### <a name="issue-date-doesnt-sync-to-common-data-service-when-updated-or-entered-in-talent-397361"></a>Datum výdeje není synchronizováno s Common Data Service, pokud je aktualizováno nebo zadáno jako Talent (397361)

Tato změna opravuje problém, kdy se datum vydání záznamů **Identifikace osob** nesynchronizuje s Common Data Service z Talentu.

### <a name="hierarchy-circular-reference-error-issued-when-assigning-a-manager-to-a-position-386659"></a>Při přiřazování manažera k pozici (386659) byla vydána hierarchická cyklická referenční chyba.

Tato změna opravuje jedinečný scénář, ve kterém se při přiřazení nového manažera k pozici zobrazí cyklická referenční chyba.

### <a name="common-data-service-entities-that-now-support-custom-fields"></a>Entity Common Data Service, které nyní podporují vlastní pole

Následující entity Common Data Service nyní podporují vlastní pole:

| Název | Celek |
| --- | --- |
| Úhrady na bankovní účet | cdm_bankaccountdisbursement |
| Interval provádění výpočtu zaměstnaneckých výhod | cdm_benefitcalculationfrequency |
| Platební období – interval provádění výpočtu zaměstnaneckých výhod | cdm_benefitcalculationfrequencypayperiod |
| Sazba výpočtu zaměstnanecké výhody | cdm_benefitcalculationrate |
| Podrobnosti sazby výpočtu zaměstnanecké výhody | cdm_benefitcalculationratedetail |
| Možnost zaměstnaneckých výhod | cdm_benefitoption |
| Plán zaměstnaneckých výhod | cdm_benefitplan (není povoleno pro podporu vlastních polí) |
| Typ zaměstnanecké výhody | cdm_benefittype |
| Kalendář obchodních procesů | cdm_businessprocesscalendar |
| Přiřazení skupiny obchodních procesů | cdm_businessprocessgroupassignment |
| Skupina úkolů knihovny obchodních procesů | cdm_businessprocesslibrarytaskgroup |
| Fáze obchodního procesu | cdm_businessprocessstage |
| Záhlaví šablony kontrolního seznamu | cdm_businessprocesstemplateheader |
| Úkol šablony kontrolního seznamu | cdm_businessprocesstemplatetask |
| Společnost | cdm_company |
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
| Oddělení | cdm_department |
| Zaměstnání | cdm_employment |
| Etnický původ | cdm_ethnicorigin |
| Událost fixní kompenzace | cdm_fixedcompensationevent |
| Pozice | cdm_job |
| Pracovní funkce | cdm_jobfunction |
| Pracovní pozice | cdm_jobposition |
| Typ práce | cdm_jobtype |
| Jazyk | cdm_language |
| Opustit bankovní transakci | cdm_leavebanktransaction |
| Opustit zápis | cdm_leaveenrollment |
| Plán pracovního volna | cdm_leaveplan |
| Žádost o pracovní volno | cdm_leaverequest |
| Podrobnosti o požadavku na dovolenou | cdm_leaverequestdetail |
| Typ pracovního volna | cdm_leavetype |
| Kód důvodu typu volna | cdm_leavetypereasoncode |
| Platební cyklus | cdm_paycycle |
| Mzdové období | cdm_payperiod |
| Kód příjmů mzdy | cdm_payrollearningcode |
| Subjekt vydávající identifikaci osob | cdm_personidentificationissuingagency |
| Typ pozice | cdm_positiontype |
| Přiřazení pracovníka k pozici | cdm_positionworkerassignmentmap |
| Kód důvodu | cdm_reasoncode |
| Typ dovednosti | cdm_skilltype |
| Daňová oblast | cdm_taxregion |
| Pravidlo připsání | cdm_vestingrule |
| Stav veterána | cdm_veteranstatus |
| Pracovní kalendář | cdm_workcalendar |
| Datum pracovního kalendáře | cdm_workcalendarday |
| Svátek pracovního kalendáře |cdm_workcalendarholiday |
| Řádek data pracovního kalendáře | cdm_workcalendarholidayline |
| Časový interval pracovního kalenáře | cdm_workcalendartimeinterval (není povoleno pro podporu vlastních polí) |
| Pracovní podproces | cdm_worker |
| Adresa pracovníka | cdm_workeraddress |
| Bankovní účet pracovníka | cdm_workerbankaccount |
| Fixní kompenzace pracovníka | cdm_workerfixedcompensation |
| Osobní údaj pracovníka | cdm_workerpersonaldetail |
| Osobní identifikační číslo pracovníka | cdm_workerpersonidentificationnumber |
| Typ osobní identifikace pracovníka | cdm_workerpersonidentificationtype |

## <a name="in-preview"></a>Náhled

Funkce náhledu jsou k dispozici pouze v prostředích **Sandbox**.

### <a name="print-performance-reviews"></a>Tisk kontrol výkonnosti

Viz [Tisk shrnutí výkonu](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) v plánu Dynamics 365: 2019 release wave 2.
