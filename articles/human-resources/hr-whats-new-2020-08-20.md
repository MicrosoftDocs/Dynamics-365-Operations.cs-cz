---
title: Co je nového a co se změnilo v aplikaci Dynamics 365 Human Resources (20. srpna 2020)
description: Tohle téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Human Resources k 20. srpnu 2020.
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 69304cbffafa4c20dbbbb31d5c19920f669761b9
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800158"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-20-2020"></a>Co je nového a co se změnilo v aplikaci Dynamics 365 Human Resources (20. srpna 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Human Resources. Změny se vztahují na sestavení číslo 8.1.3478. Čísla v závorkách v některých záhlavích se vztahují na čísla podpory pro referenci v Lifecycle Services (LCS).

## <a name="show-upcoming-and-pending-leave-of-absence-information-to-cards-in-people-workspace"></a>Zobrazení nadcházejících a nevyřízených informací o absencích na kartách v pracovním prostoru Lidé

Možnosti čekajícího a nadcházejícího požadavku na pracovní volno jsou nyní k dispozici na kartách Pracovní volno a absence v pracovním prostoru **Lidé**.

## <a name="private-field-isnt-yes-by-default-for-employee-role-in-employee-self-service-477106"></a>Pole Soukromé není ve výchozím nastavení Ano pro roli zaměstnance v samoobslužné službě zaměstnance (477106)

Výchozí hodnota pole **Soukromé** je nyní **Ano**, když zaměstnanci přidávají nové záznamy adres prostřednictvím stránky **Osobní informace** v samoobsluze zaměstnanců. 

## <a name="candidates-to-hire-fasttab-in-personnel-management-shows-an-incorrect-count-of-candidates-470110"></a>Záložka s náhledem Uchazeči o pracovní místo na stránce Správa zaměstnanců ukazuje nesprávný počet kandidátů (470110)

Stránka **Správa zaměstnanců** nyní přesně zobrazuje počet uchazečů o pracovní místo. 

## <a name="cant-enter-sickness-for-terminated-employee-when-accrual-is-set-to-zero-446195"></a>Nelze zadat nemoc pro propuštěného zaměstnance, když je časové rozlišení nastaveno na nulu (446195)

Transakce pracovního volna jsou nyní povoleny pro zaměstnance, kteří budou v budoucnu propuštěni a časové rozlišení je nastaveno na nulu. Transakce pracovního volna lze zadat až do data propuštění zaměstnance. 

## <a name="adding-custom-fields-to-the-new-worker-form-disables-the-fields-in-the-action-pane-for-manage-leave-473314"></a>Přidání vlastních polí do nového formuláře Pracovník zakáže pole v podokně akcí pro správu pracovního volna (473314)

Možnosti podokna akcí na novém formuláři **Pracovník** na stránce **Správa pracovního volna** již nebudou deaktivovány, pokud byla do nového formuláře **Pracovník** přidána vlastní pole.

## <a name="making-the-leave-comment-field-mandatory-allows-a-leave-request-to-be-submitted-when-no-comment-is-entered-473543"></a>Pokud je pole Zanechte komentář povinné, lze odeslat žádost o pracovní volno, i když není zadán žádný komentář (473543)

Pole pro komentář mohou být nyní povinná a žádosti o pracovní volno respektují tohle nastavení. Povinná pole je funkce Preview.

### <a name="dmf-entity-available-for-accrual-suspensions"></a>Entita DMF dostupná pro pozastavení časového rozlišení

Entita DMF je nyní k dispozici pro akruální pozastavení

## <a name="in-preview"></a>Náhled

### <a name="mandatory-fields"></a>Povinná pole

Nyní můžete změnit pole na povinná pomocí personalizačních funkcí systému lidských zdrojů. Tato funkce vyžaduje **Uložená zobrazení**. Další informace o uložených zobrazeních naleznete v tématu:

- [Uložená zobrazení - obecná dostupnost](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability) v plánu 2. vlny vydání v Dynamics 365 2020
- [Vytváření formulářů, které plně využívají uložená zobrazení](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/user-interface/understanding-saved-views)

### <a name="human-resources-application-in-teams"></a>Aplikace Human Resources v Teams

Zaměstnanci mohou prohlížet a požadovat pracovní volno v rámci Microsoft Teams. Mohou interagovat s robotem a vytvářet žádosti o dovolenou. Další informace naleznete zde:

- [Dovolená a nepřítomnost zaměstnanců v Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) v plánu 1. vlny vydání v Dynamics 365 2020
- [Aplikace Human Resources v Teams](https://go.microsoft.com/fwlink/?linkid=2127841)

## <a name="coming-soon"></a>Již brzy

### <a name="human-resources-app-in-teams-preview-features"></a>Funkce preview aplikace Human Resources v Teams
 
-  **Oznámení**: Odesílatelé a schvalovatelé žádostí o volno budou upozorněni v aplikaci Human Resources v Teams. Schvalovatelé budou moci schválit nebo zamítnout žádosti o volno a odesílatelé budou informováni, pokud je požadavek schválen nebo zamítnut.
 
- **Kalendář volna manažera**: Manažeři budou moci vidět schválené a nevyřízené volno pro jejich přímé podřízené v zobrazení kalendáře. Tohle zobrazení umožňuje snadné pochopení, kdy jsou členové jejich týmu mimo práci.

### <a name="checklist-entities-included-in-dataverse"></a>Položky kontrolního seznamu zahrnuté do Dataverse

Položky kontrolního seznamu pro onboarding, offboarding, převody a obchodní procesy budou v systému Dataverse k dispozici již brzy.

## <a name="known-issues"></a>Známé problémy

Ve **Správa funkcí** pracovním prostoru mohou být zobrazeny funkce, které jsou deaktivovány jako funkce náhledu, pokud jsou obecně dostupné. Níže je uveden seznam obecně dostupných funkcí, které vykazují nesprávný stav. 

- Správa zaměstnaneckých výhod
- Správa případů
- Protokolování databáze (auditování)
- Časové rozlišení pracovního volna pro jednu společnost nebo jeden plán
- Přerušení časového rozlišení pracovního volna a absence
- Kód důvodu úpravy zůstatku a komentář
- Nákup a prodej pracovního volna
- Kalendář pracovního volna a absence
- Ponechat pravidla převodu
- Audit časového rozlišení pracovního volna
- Odstranění časového rozlišení pracovního volna
- Zaokrouhlování časového rozlišení pracovního volna
- Konfigurovat více typů pracovního volna v jednom plánu pracovního volna
- Rozšíření aktualizace volna
- Použít ekvivalent plného úvazku zaměstnance pro časové rozlišení
- Zobrazit kompenzaci mezi společnostmi
- Tisk kontrol výkonnosti
- Oprava svátků při časovém rozlišení pracovního volna

### <a name="benefit-plan-employee-entity"></a>Entita plánu zaměstnaneckých výhod 

Nedávno jsme objevili dva problémy týkající se entity **BenefitsPlanEmployee**. Při importu registrací pracovníků jsou **Kód pokrytí** a **Kód typu plánu** nastaveny nesprávně. Tento problém způsobí, že se plány zaměstnaneckých výhod ve formulářích **Plán zaměstnaneckých výhod** a **Otevřená registrace** v samoobsluze zaměstnanců nezobrazují správně. Tento problém může také ovlivnit schopnost zaměstnance vybírat plány v samoobslužné službě pro zaměstnance. V současné době neexistuje řešení. Opravu tohoto problému považujeme za prioritu a bude součástí příštího vydání.

## <a name="see-also"></a>Viz také

[Co je nového a co se změnilo v Human Resources](hr-admin-whats-new.md)</br>
[Přehled produktu Dynamics 365 Human Resources vydání 2019 vlny 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Aktualizace procesu](hr-admin-setup-update-process.md)</br>
[Správa funkcí](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]