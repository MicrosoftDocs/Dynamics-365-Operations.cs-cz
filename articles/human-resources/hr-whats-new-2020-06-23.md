---
title: Co je nového a co se změnilo v aplikaci Dynamics 365 Human Resources (25. června 2020)
description: Tohle téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Human Resources k 23. červnu 2020.
author: andreabichsel
manager: tfehr
ms.date: 06/25/2020
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
ms.author: jaredha
ms.search.validFrom: 2020-06-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ad80e53c0a24d602ac446d3e0765f397dd0fc2d9
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127490"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-23-2020"></a>Co je nového a co se změnilo v aplikaci Dynamics 365 Human Resources (23. června 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Human Resources. Změny se vztahují na sestavení číslo 8.1.3347. Čísla v závorkách v některých záhlavích se vztahují na čísla podpory v Lifecycle Services (LCS) pro referenci.

## <a name="when-an-enrollment-is-expired-for-a-terminated-employee-the-leave-type-balance-and-amount-are-all-cleared-in-the-leave-enrollment-form-444867"></a>Když skončí platnost prováděcí smlouvy zaměstnance po rozvázání pracovního poměru, položky typ dovolené, zůstatek a částka se z formuláře registrace dovolené vymažou (444867)

Hodnoty v polích **Typ dovolené**, **Zůstatek** a **Množství** se nyní při provedení tohoto výběru zachovají (nebudou vymazány).

## <a name="incorrect-forecasted-balance-when-new-feature-leave-accrual-for-a-single-company-or-a-single-plan-is-enabled-456553"></a>Nesprávný odhadovaný zůstatek, když je aktivována nová funkce (Časové rozlišení pracovního volna pro jednu společnost nebo jeden plán) (456553)

Správný odhadovaný zůstatek se nyní zobrazí, když je aktivováno časové rozlišení pracovního volna pro jednu společnost nebo jeden plán.

## <a name="entities-with-relations-that-result-in-duplicate-navigation-properties-456486"></a>Subjekty se vztahy, které vedou k duplicitě navigačních vlastností (456486)

Tato vydaná verze opravuje problém s navigačními vlastnostmi (vztahy) více subjektů. Jsou detekovány duplicitní vztahy. Všechny tyto scénáře byly opraveny.
 
## <a name="cross-company-comments-on-performance-review-455536"></a>Mezipodnikové komentáře k přehledu výkonů (455536)

Po této opravě jsou nyní v přehledech výkonů viditelné mezipodnikové komentáře. Tato změna opravuje zobrazení komentářů kontrolora zadaných v různých společnostech v rámci stejné kontroly výkonu.
 
## <a name="inconsistency-in-showing-compensation-management-data-432562"></a>Nekonzistence při zobrazování údajů správy kompenzací (432562)

V samoobsluze pro manažery je nyní zachováno konzistentní zobrazení údajů o kompenzacích. V závislosti na tom, jak přejdete k **Podrobnostem o kompenzaci** pracovníka se nyní manažerům zobrazují údaje o kompenzaci konzistentně.
 
## <a name="fixed-compensation-plans-effective-date-defaults-to-todays-date-411994"></a>Výchozí datum účinnosti plánu fixní kompenzace je dnešní datum (411994)

Počáteční datum kompenzace nyní vychází z počátečního data pozice, jež je zaměstnanci přiřazena.

## <a name="leave-and-absence-form-enable-half-day-definition-is-disabled-when-form-opens-452607"></a>Formulář pracovního volna a absence: při otevření formuláře je pole Povolit definici poloviny dne deaktivováno (452607)

Na základě této změny bude pole **Povolit definici poloviny dne** povoleno do doby vzniku nové transakce pracovního volna. 

## <a name="unable-to-publish-to-hcmdiscussionentity-via-excel-totalratingscore-field-error-453899"></a>Nelze publikovat do HcmDiscussionEntity prostřednictvím aplikace Excel; chyba pole TotalRatingScore (453899)

Nyní můžete pole **TotalRatingScore** aktualizovat pomocí položky **HCMDiskuseEntity** v nástroji pro návrh sešitů Excel.

## <a name="in-preview"></a>Náhled

## <a name="database-logging"></a>Protokolování databáze

Protokolování databáze umožňuje určit, které tabulky a pole mají být monitorovány. Umožňuje také určit události, které by měly spustit sledování změn. Pomocí funkcí protokolování databáze se můžete podívat na tyto změny v průběhu času. Další informace získáte v rématu [Konfigurace a správa protokolování databáze](hr-admin-database-logging.md).

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

## <a name="configure-the-name-of-employee-self-service"></a>Konfigurace samoobsluhy pro zaměstnance

V **parametrech lidských zdrojů** bude k dispozici nová možnost aktualizace názvu pracovního prostoru Zaměstnanecká samoobsluha na Samoobsluha.

## <a name="checklist-entities-included-in-dataverse"></a>Položky kontrolního seznamu zahrnuté do Dataverse

Položky kontrolního seznamu pro onboarding, offboarding, převody a obchodní procesy budou v systému Dataverse k dispozici již brzy.

## <a name="see-also"></a>Viz také

[Co je nového a co se změnilo v Human Resources](hr-admin-whats-new.md)</br>
[Přehled produktu Dynamics 365 Human Resources vydání 2019 vlny 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Aktualizace procesu](hr-admin-setup-update-process.md)</br>
[Správa funkcí](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]