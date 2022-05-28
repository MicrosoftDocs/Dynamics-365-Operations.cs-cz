---
title: Co je nového a co se změnilo v aplikaci Dynamics 365 Human Resources (06. srpna 2020)
description: Tohle téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Human Resources k 6. srpnu 2020.
author: andreabichsel
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-08-06
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a8058c1acdde20a1b48130fa1e8b75aa415bafce
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2022
ms.locfileid: "8691967"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-06-2020"></a>Co je nového a co se změnilo v aplikaci Dynamics 365 Human Resources (06. srpna 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Human Resources. Změny se vztahují na sestavení číslo 8.1.3444. Čísla v závorkách v některých záhlavích se vztahují na čísla podpory v Lifecycle Services (LCS) pro referenci.

## <a name="platform-update-1001236-is-now-available"></a>Nyní je k dispozici aktualizace platformy 10.0.12(36).

Další informace naleznete v tématu [Aktualizace platformy pro verze 10.0.12 finančních a provozních aplikací (srpen 2020)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-10-0-12.md).

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a>Entity právy datových rámců (DMF) pro správu zaměstnaneckých výhod
 
Zvýhodněné účetní jednotky se uvolňují. Entity DMF umožňují import a export dat pro snadnou konfiguraci správy výhod. K přesunutí dat bude k dispozici šablona správy výhod. Šablona exportuje a importuje data sekvenčně, aby respektovala datové závislosti. Další informace naleznete zde:

- [Podpora entit DMF](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/dmf-entity-support) v plánu 1. vlny vydání v r. 2020 programu Dynamics 365
- [Přehled správy dat](../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md)


## <a name="claire-creates-a-workflow-for-buying-and-selling-leave-requests-446557"></a>Claire vytváří pracovní postup pro nákup a prodej žádostí o dovolenou (446557)

Další informace naleznete zde:

- [Umožněte zaměstnancům nakupovat a prodávat dovolenou](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/allow-employees-buy-sell-leave) v plánu 2. vlny vydání v Dynamics 365 2020
- [Správa zásad nákupu a prodeje pracovního volna](./hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [Nákup a prodej pracovního volna](./hr-employee-self-service-buy-sell-leave.md)


## <a name="worker-postal-addresses-v2-entity-has-access-across-legal-entities-with-restricted-access-459126"></a>V2 entita poštovní adresy pracovníka má přístup napříč právnickými osobami s omezeným přístupem (459126)

S touto změnou, entita **Poštovní adresa pracovníka V2** bude omezena na základě přístupu právnické osoby k uživateli.

## <a name="workflow-email-hyperlink-fails-to-open-relevant-reviews-437398"></a>Hypertextový odkaz e-mailu pracovního postupu neotevře relevantní recenze (437398)

Použijete-li zástupný symbol k otevření kontroly výkonnosti ve workflow kontroly, hypertextový odkaz vygenerovaný v e-mailu nyní otevře vybraný záznam.

## <a name="new-entities-for-buying-and-selling-leave-473180"></a>Nové entity pro nákup a prodej dovolené (473180)

Entity správy datových rámců jsou nyní k dispozici pro nákup a prodej dovolené. Další informace naleznete v tématu [Přehled správy dat](../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).

## <a name="when-viewing-record-information-and-using-advanced-filters-a-user-could-gain-access-to-other-employees-records-472490"></a>Při prohlížení informací o záznamu a používání pokročilých filtrů uživatel mohl získat přístup k záznamům jiných zaměstnanců (472490)

S touto změnou mohou uživatelé zaměstnanecké samoobsluhy přistupovat ke svým vlastním záznamům pouze při používání zaměstnanecké samoobsluhy. Prohlížení informací o záznamu při změně možnosti filtrování již nevystavuje další data.

## <a name="personnel-management-analytics-include-exited-worker-records-382893"></a>Analytiky správy zaměstnanců zahrnují ukončené záznamy pracovníků (382893)

S touto verzí nyní analytika správy zaměstnanců zahrnuje pouze aktivní pracovníky. 
 
## <a name="unable-to-process-a-merit-increase-for-an-employee-473125"></a>Nelze zpracovat zvýšení zásluh zaměstnance (473125)

Tato změna umožňuje zadat zvýšení zásluhy, když změníte datum účinnosti nového zvýšení zásluhy.

## <a name="review-workflow-can-be-started-more-than-once-467541"></a>Pracovní postup přezkoumání lze spustit vícekrát (467541)

S touto změnou můžete pracovní postup přezkoumání výkonu spustit pouze jednou. Stav správce již nezobrazuje možnost zahájit přezkoumání.

## <a name="leave-request-work-flow-ends-in-error-when-canceling-an-approved-leave-request-472063"></a>Při rušení schválené žádosti o dovolenou končí pracovní postup požadavku na dovolenou chybou (472063)

Když v této verzi zrušíte schválenou žádost o dovolenou, stav žádosti již nadále nebude schválen a pracovní postup bude pokračovat.

## <a name="system-suggests-exited-workers-when-creating-a-new-review-form-the-template-460624"></a>Systém navrhuje ukončené pracovníky při vytváření nového přezkoumání ze šablony (460624)

Díky této změně jsou již nejsou ukončení pracovníci k dispozici při vytváření nových recenzí ze šablony. Nemůžete vytvářet přezkoumání pro zaměstnance, kteří jsou mimo datum svého zaměstnání.

## <a name="position-hierarchy-circular-reference-detection-415879"></a>Detekce polohy kruhových odkazů referenční hierarchie (415879)

S touto změnou je detekce kruhových odkazů pozic hierarchie omezena na jeden časový bod. Chcete-li ověřit, že struktura hlášení nemá žádné kruhové odkazy, můžete spustit detekci kruhových odkazů pro různá data.

## <a name="buy-and-sell-leave"></a>Nákup a prodej pracovního volna 

Některé organizace poskytují výhodu, která zaměstnancům umožňuje nakupovat nebo prodávat dovolenou. Tento proces je často řízen ručně. Tato funkce automatizuje správu zásad a požadavků oddělení lidských zdrojů. Usnadňuje proces správy dovolených a pomáhá eliminovat chyby. Další informace naleznete zde:

- [Umožněte zaměstnancům nakupovat a prodávat dovolenou](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/allow-employees-buy-sell-leave) v plánu 2. vlny vydání v Dynamics 365 2020
- [Správa zásad nákupu a prodeje pracovního volna](./hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [Nákup a prodej pracovního volna](./hr-employee-self-service-buy-sell-leave.md)

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

## <a name="in-preview"></a>Náhled

### <a name="mandatory-fields"></a>Povinná pole

Nyní můžete změnit pole na povinná pomocí personalizačních funkcí systému lidských zdrojů. Tato funkce vyžaduje **Uložená zobrazení**. Další informace o uložených zobrazeních naleznete v tématu:

- [Uložená zobrazení - obecná dostupnost](/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability) v plánu 2. vlny vydání v Dynamics 365 2020
- [Vytváření formulářů, které plně využívají uložená zobrazení](../fin-ops-core/dev-itpro/user-interface/understanding-saved-views.md)

### <a name="human-resources-application-in-teams"></a>Aplikace Human Resources v Teams

Zaměstnanci mohou prohlížet a požadovat pracovní volno v rámci Microsoft Teams. Mohou interagovat s robotem a vytvářet žádosti o dovolenou. Další informace naleznete zde:

- [Dovolená a nepřítomnost zaměstnanců v Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) v plánu 1. vlny vydání v Dynamics 365 2020
- [Aplikace Human Resources v Teams](./hr-admin-teams-leave-app.md)

### <a name="dmf-entity-available-for-accrual-suspensions"></a>Entita DMF dostupná pro pozastavení časového rozlišení

Entita DMF je nyní k dispozici pro akruální pozastavení

## <a name="coming-soon"></a>Již brzy

## <a name="checklist-entities-included-in-dataverse"></a>Položky kontrolního seznamu zahrnuté do Dataverse

Položky kontrolního seznamu pro onboarding, offboarding, převody a obchodní procesy budou v systému Dataverse k dispozici již brzy.

## <a name="known-issues"></a>Známé problémy

Ve **Správa funkcí** pracovním prostoru mohou být zobrazeny funkce, které jsou deaktivovány jako funkce náhledu, pokud jsou obecně dostupné. Níže je uveden seznam obecně dostupných funkcí, které vykazují nesprávný stav. 

1.  Správa zaměstnaneckých výhod
2.  Správa případů
3.  Protokolování databáze (auditování)
4.  Časové rozlišení pracovního volna pro jednu společnost nebo jeden plán
5.  Přerušení časového rozlišení pracovního volna a absence
6.  Kód důvodu úpravy zůstatku a komentář
7.  Nákup a prodej pracovního volna
8.  Kalendář pracovního volna a absence
9.  Ponechat pravidla převodu
10. Audit časového rozlišení pracovního volna
11. Odstranění časového rozlišení pracovního volna
12. Zaokrouhlování časového rozlišení pracovního volna
13. Konfigurovat více typů pracovního volna v jednom plánu pracovního volna
14. Rozšíření aktualizace volna
15. Použít ekvivalent plného úvazku zaměstnance pro časové rozlišení
16. Zobrazit kompenzaci mezi společnostmi
17. Tisk kontrol výkonnosti
18. Oprava svátků při časovém rozlišení pracovního volna

## <a name="see-also"></a>Viz také

[Co je nového a co se změnilo v Human Resources](hr-admin-whats-new.md)</br>
[Přehled produktu Dynamics 365 Human Resources vydání 2019 vlny 2](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Aktualizace procesu](hr-admin-setup-update-process.md)</br>
[Správa funkcí](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]