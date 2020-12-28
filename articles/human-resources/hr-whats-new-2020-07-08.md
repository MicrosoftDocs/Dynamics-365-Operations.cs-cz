---
title: Co je nového nebo co se změnilo v aplikaci Dynamics 365 Human Resources (08. července 2020)
description: Tohle téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Human Resources k 8. červenci 2020.
author: Darinkramer
manager: AnnBe
ms.date: 07/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ba0bb54b44f66aa73056667a93a3f8e6f7f618ee
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528466"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-8-2020"></a>Co je nového nebo co se změnilo v aplikaci Dynamics 365 Human Resources (8. července 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Human Resources. Změny se vztahují na sestavení číslo 8.1.3382. Čísla v závorkách v některých záhlavích se vztahují na čísla podpory v Lifecycle Services (LCS) pro referenci.

## <a name="database-logging"></a>Protokolování databáze

Protokolování databáze umožňuje určit, které tabulky a pole mají být monitorovány. Umožňuje také určit události, které by měly spustit sledování změn. Pomocí funkcí protokolování databáze se můžete podívat na tyto změny v průběhu času. Další informace získáte v rématu [Konfigurace a správa protokolování databáze](hr-admin-database-logging.md).

## <a name="configure-the-name-of-employee-self-service"></a>Konfigurace samoobsluhy pro zaměstnance

V **Parametry lidských zdrojů** můžete nyní změnit název pracovního prostoru **Zaměstnanecká samoobsluha** na **Samoobsluha**. Další informace naleznete v tématu [Změna názvu pracovního prostoru samoobsluhy pro zaměstnance](hr-employee-self-service-workspace-name.md)

## <a name="benefits-management-open-enrollment-access-outside-of-period"></a>Oevřený přístup k zápisu správy zaměstnaneckých výhod mimo období

Toto vydání opravuje chybu, kdy zaměstnanci měli přístup k výhodám otevřeného zápisu mimo období zápisu nebo bez životní události. V důsledku toho, pokud potřebujete ukázat otevřený zápis do samoobslužné služby zaměstnance, musíte upravit data otevřeného zápisu na dnešek (nebo dříve), abyste je zpřístupnili. Toto nastavení můžete změnit pod **Správa výhod > Období pravidel a možností**.

## <a name="email-employee-enrollment-confirmation"></a>E-mail s potvrzením o registraci zaměstnance

Po dokončení výběru výhod nyní můžete zaměstnancům zasílat e-maily. Můžete buď odeslat výchozí zprávu, nebo použít šablonu e-mailu organizace. Tato nastavení jsou pod **Parametry lidských zdrojů > Správa zaměstnaneckých výhod**.

## <a name="canceled-leave-still-appears-in-upcoming-time-off-on-people-workspace-441358"></a>Zrušená dovolená se stále zobrazuje v nadcházejícím pracovním volnu v pracovním prostoru Lidé (441358)

Zrušená dovolená se již nezobrazuje jako nadcházející volno na kartách volna v pracovním prostoru **Lidé**.

## <a name="unable-to-use-the-department-entity-property-in-the-positionv2-entity-456486"></a>Nelze použít vlastnost entity oddělení v entitě PositionV2 (456486)

Nyní můžete přidat oddělení bez vytvoření duplicitního vztahu.

## <a name="payrollworkerenrolledbenefitdetailentity-should-only-use-calculated-field-for-retirement-plans-459779"></a>PayrollWorkerEnrolledBenefitDetailEntity by měl používat vypočítané pole pouze pro penzijní plány (459779)

Při exportu entity **PayrollWorkerEnrolledBenefitDetailEntity** určuje export, zda by měl použít vypočtené pole na základě tabulky sazeb nebo použít pole **ContributionAmountCur** ze záložní tabulky. Logika použitá datovou entitou používá tabulku sazeb v situacích, kdy aplikace normálně ne. Tato logika způsobí, že export entity vrátí nulovou hodnotu pro tento sloupec, protože neexistuje žádná tabulka sazeb výpočtu a produkt neumožňuje zákazníkovi specifikovat jednu.
 
## <a name="confusing-translations-in-czech-language-in-personnel-management-and-employee-self-service-400276"></a>Zmatení překladů v českém jazyce ve Správě zaměstnanců a Samoobsluze zaměstnanců (400276)

Toto vydání opravuje překlady pro **Adresář společnosti**, **Další zaregistrovaný kurz**, **Úloha** a **Pozice**.
 
## <a name="the-workcalendaremployment-table-doesnt-have-the-created-and-modified-system-fields-enabled-460171"></a>Tabulka WorkCalendarEmployment nemá vytvořená a upravená systémová pole povolena (460171)

Vytvořená a upravená systémová pole jsou nyní povolena v tabulce **WorkCalendarEmployment** v Human Resources.
 
## <a name="null-reference-exception-for-hire-and-add-details-for-future-employee-455475"></a>Nulová referenční výjimka pro Přijetí a přidejte podrobnosti pro budoucího zaměstnance (455475)

Toto vydání opravuje chybu (nulová reference) v zjednodušeném záznamu zaměstnance, když přijmete zaměstnance pomocí možnosti **Příjem a přidání podrobností**.

## <a name="changes-made-in-the-common-data-service-worker-entity-dont-reflect-in-human-resources-455652"></a>Změny provedené v entitě Common Data Service Pracovník se neodráží v Human Resources (455652)

Změny provedené v následujících polích v entitě **Pracovník** v Common Data Service se nyní objeví v Human Resources:

- **Práce z domu**
- **Datum služebního věku**
- **Datum výročí**
- **Datum původního přijetí**

## <a name="correct-compensation-level-doesnt-default-based-on-the-job-assigned-to-the-position-394136"></a>Správná úroveň kompenzace není výchozí na základě úlohy přiřazené k dané pozici (394136)

S touto změnou je výchozí úroveň správné úrovně kompenzace na základě záznamů **Datum platnosti** pro **Detaily pozice** a **Počáteční datum** z **Přiřazení kompenzačního plánu**.

## <a name="in-preview"></a>Náhled

## <a name="mandatory-fields"></a>Povinná pole 

Nyní můžete změnit pole na povinná pomocí personalizačních funkcí systému lidských zdrojů. Tato funkce vyžaduje **Uložená zobrazení**.

## <a name="human-resources-application-in-teams"></a>Aplikace Human Resources v Teams

Zaměstnanci mohou prohlížet a požadovat pracovní volno v rámci Microsoft Teams. Mohou interagovat s robotem a vytvářet žádosti o dovolenou. Další informace viz [Aplikace Human Resources v Teams](https://go.microsoft.com/fwlink/?linkid=2127841). 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>Entity právy datových rámců (DMF) pro správu zaměstnaneckých výhod
 
Zvýhodněné účetní jednotky se uvolňují. Entity DMF umožňují import a export dat pro snadnou konfiguraci správy výhod. K přesunutí dat bude k dispozici šablona správy výhod. Šablona exportuje a importuje data sekvenčně, aby respektovala datové závislosti.

## <a name="buy-and-sell-leave"></a>Nákup a prodej pracovního volna 

Některé organizace poskytují výhodu, která zaměstnancům umožňuje nakupovat nebo prodávat dovolenou. Tento proces je často řízen ručně. Tato funkce automatizuje správu zásad a požadavků oddělení lidských zdrojů. Usnadňuje proces správy dovolených a pomáhá eliminovat chyby. Další informace naleznete zde:

- [Správa zásad nákupu a prodeje pracovního volna](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [Nákup a prodej pracovního volna](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a>Časové rozlišení pracovního volna pro jednu společnost nebo jeden plán

Zákazníci mohou zpracovat časové rozlišení pro jednu společnost nebo jeden plán dovolené a nepřítomnosti. Tato schopnost objasňuje proces časového rozlišení pro zákazníky s různými roky dovolené nebo zásadami časového rozlišení dovolené. Další informace získáte v části [Časové rozlišení dovolené podle společnosti nebo plánu dovolených](hr-leave-and-absence-accrue.md).

## <a name="add-attachments-to-time-off-requests"></a>Přidání příloh k požadavkům na volno

Schopnost přidávat přílohy ke schváleným požadavkům na dovolenou je v současném prostředí COVID-19 kritická. Zaměstnanci nyní mohou tyto přílohy přidávat. Mají také podrobnější přehled o tom, jak jsou aktualizovány žádosti o dovolenou. Další informace získáte v části [Přidání přílohy k existující žádosti](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).

## <a name="add-reason-code-to-accrual-suspensions"></a>Přidání kódu důvodu k časově rozlišeným pozastavením 

K akruálnímu pozastavení byly přidány kódy důvodů.

## <a name="carry-forward-rules"></a>Pravidla pro převod do dalšího období 

Můžete určit typ převodu pracovního volna do dalšího období pro převod zůstatků, kde byly převedeny úpravy převodu do dalšího období. Pokud například zaměstnanec přenese deset dní dopředu, můžete pro tyto 10 dny vybrat jiný typ pracovního volna. Další informace naleznete v tématu [Konfigurace typů pracovního volna a absence](hr-leave-and-absence-types.md).

## <a name="suspend-leave-accrual-for-specified-leave-types"></a>Časové rozlišení pozastavení dovolené pro zadané typy dovolené

Můžete vytvořit pravidlo pro pozastavení přírůstků dovolené pro zaměstnance s požadavky na dovolenou zadanými pro neplacenou dovolenou. Neplacená dovolená může být zadána, ale nemusí. Dovolenou můžete pozastavit na základě jiného typu dovolené.

## <a name="dmf-entity-available-for-accrual-suspensions"></a>Entita DMF dostupná pro pozastavení časového rozlišení 

Entita DMF je nyní k dispozici pro akruální pozastavení

## <a name="coming-soon"></a>Již brzy

## <a name="checklist-entities-included-in-common-data-service"></a>Položky kontrolního seznamu zahrnuté do Common Data Service

Položky kontrolního seznamu pro onboarding, offboarding, převody a obchodní procesy budou v systému Common Data Service k dispozici již brzy.

## <a name="see-also"></a>Viz také

[Co je nového a co se změnilo v Human Resources](hr-admin-whats-new.md)</br>
[Přehled produktu Dynamics 365 Human Resources vydání 2019 vlny 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Aktualizace procesu](hr-admin-setup-update-process.md)</br>
[Správa funkcí](hr-admin-manage-features.md)
