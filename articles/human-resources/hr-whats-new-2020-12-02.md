---
title: Co je nového a co se změnilo v aplikaci Dynamics 365 Human Resources (2. prosince 2020)
description: Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Human Resources k 2. prosinci 2020.
author: marcelbf
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cecef6d2e73b42126b1be100dca52ebd8d9270fc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8848100"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-december-2-2020"></a>Co je nového a co se změnilo v aplikaci Dynamics 365 Human Resources (2. prosince 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tento článek popisuje funkce, které jsou nové, změnily se nebo brzy dorazí do aplikace Dynamics 365 Human Resources.

Další informace o našem procesu aktualizaci a plánu najdete v tématu [Proces aktualizace](hr-admin-setup-update-process.md).

Další informace o nových funkcích a jejich očekávaných obecných datech dostupnosti najdete v tématu [Přehled 2. vlny vydání Dynamics 365 Human Resources v roce 2020](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>V této vydané verzi

Tato verze obsahuje následující nové funkce a opravené chyby. Změny se vztahují na sestavení číslo 8.1.3788.

### <a name="new-features"></a>Nové funkce

V této verzi jsou všeobecně dostupné následující funkce.

| Funkce | Plán vydání | Dokumentace |
| --- | --- | --- |
| Manažeři mohou odesílat žádosti o nábor na volné pozice | [Manažeři mohou odesílat žádosti o nábor na volné pozice](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [Přidání žádosti o nábor](./hr-personnel-recruit.md#add-a-recruiting-request) |
| Vylepšený profil kandidáta ve správě zaměstnanců | [Vylepšený profil kandidáta ve správě zaměstnanců](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [Přidání nebo úprava profilu kandidáta](./hr-personnel-recruit.md#add-or-edit-a-candidate-profile) |
| Povolení zjednodušených integrací s poskytovateli náboru | [Povolení zjednodušených integrací s poskytovateli náboru](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [Nábor uchazečů o práci](./hr-personnel-recruit.md) |
| Vlastní odkazy v samoobsluze pro manažery | [Vlastní odkazy v samoobsluze pro manažery](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service) | [Vlastní odkazy v samoobsluze pro manažery](./hr-employee-manager-self-service-custom-links.md) |


### <a name="bug-fixes"></a>Opravy chyb

Tato verze obsahuje následující opravy chyb.

> [!NOTE]
> Naším cílem dostat k vám tyto informace co nejdříve. Tento článek můžeme aktualizovat, aby obsahovalo opravy chyb, které se dostaly do sestavení poté, co byl tento článek původně publikován.

| Číslo problému | Problém | Popis |
| --- | --- | --- |
| 514087 | Entita BenefitEligibilityProcessResult by měla zahrnovat datum a čas, který byl použit při zpracování. | Výsledek zpracování BenefitEligibity nyní obsahuje značku data a času posledního zpracování, která dříve chyběla. |
| 526903 | Registrace zaměstnaneckých výhod selže u plánů se závislými prvky, když **Automatický výběr pověřených osob** je zapnutý v části **Sdílené parametry Human Resources**. | Opravili jsme problém, kdy registrace zaměstnaneckých výhod selhala pro závislé prvky, když byla možnost **Automatický výběr pověřených osob** zapnuta pro výchozí pověřené osoby. |
| 521922 | Parametr **Zobrazit absenci bez podrobností** zobrazuje podrobnosti požadavků na volno v kalendáři absencí týmu. | Typ pracovního volna, barva typu pracovního volna a podrobnosti dne se zobrazovaly v kalendáři absencí týmu, když byla možnost **Zobrazit absenci bez podrobností** nastavena na **Ano** v části **Parametry pracovního volna a absence**. To bylo vyřešeno a nyní se typ pracovního volna nezobrazuje a pro všechny typy pracovního volna v kalendáři absencí týmu se používá výchozí barva typu pracovního volna (tmavě modrá). |
| 527316 | Změny nadpisů u oznámení práce, pozice a pracovníka se nesynchronizují. | Vztah Nadpis byl původně přidán do entit Práce, Pozice a Pracovník. Synchronizace tohoto vztahu funguje při synchronizaci z Human Resources do Dataverse, ale nefungovala pro oznámení z Dataverse. To bylo vyřešeno. |
| 512275 | Odebrány možnosti barev z části **Parametry pracovního volna a absence**. | Nyní, když jsou barvy definovány pro typ pracovního volna, možnosti barev již nejsou potřeba v části **Parametry pracovního volna a absence**, takže byly odstraněny. |
| 437112 | Zavádějící text chybové zprávy během přiřazování pozice zaměstnance. | Aktualizována chybová zpráva při najímání pracovníka a pokusu o přiřazení pracovníka k pozici, která není aktivní. Aktualizovaná zpráva **Zadaná pozice není aktivní k počátečnímu datu zaměstnání. Zkontrolujte dobu trvání této pozice.** |
| 527816 | Problémy s výkonem na stránce **Volno**. | Výkon byl vylepšen na stránce **Volno**. |
| 523158 | BenefitPeriodMigrationUpgrade a BenefitPlanMigrationUpgrade se neprovádějí. | Opraveny problémy s úlohami migrace zaměstnaneckých výhod souvisejících s položkami **Doba** a **Plán**, které se neprováděly správně. |

## <a name="in-preview"></a>Náhled

Verze Preview obsahuje následující nové funkce. Další informace o zapnutí a vypnutí funkcí naleznete v tématu [Správa funkcí](hr-admin-manage-features.md).

| Funkce | Plán vydání | Dokumentace |
| --- | --- | --- |
| Aplikace Human Resources v Microsoft Teams | [Dovolená a nepřítomnost zaměstnanců v Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Aplikace Human Resources v Teams](./hr-admin-teams-leave-app.md)<br>[Správa žádostí o dovolenou v aplikaci Teams](hr-teams-leave-app.md) |
| Vylepšené požadavky a schválení pracovního toku | [Vylepšení prostředí pracovního postupu pro správu organizace a personálu](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Možnost konfigurace pro umístění seznamu Pracovní položky přiřazené mně](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| Integrace s LinkedIn Talent Hub | [Integrace s LinkedIn Talent Hub](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [Integrace s LinkedIn Talent Hub](./hr-admin-integration-linkedin.md) |
|Zobrazení pracovního volna manažery napříč společnostmi | [Zobrazení pracovního volna zaměstnanců manažery napříč společnostmi](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Konfigurace parametrů pracovního volna a absence](./hr-leave-and-absence-parameters.md) |
|Poskytnutí dalších přehledů zůstatků pracovního volna| [Poskytnutí dalších přehledů zůstatků pracovního volna](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/provide-additional-insight-into-leave-balances) | [Správa pracovního volna zaměstnanců](./hr-leave-and-absence-manage-employee-leave.md) |
| Manažeři mohou odesílat žádosti o nábor na volné pozice | [Manažeři mohou odesílat žádosti o nábor na volné pozice](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [Přidání žádosti o nábor](./hr-personnel-recruit.md#add-a-recruiting-request) |
| Vylepšený profil kandidáta ve správě zaměstnanců | [Vylepšený profil kandidáta ve správě zaměstnanců](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [Přidání nebo úprava profilu kandidáta](./hr-personnel-recruit.md#add-or-edit-a-candidate-profile) |
| Povolení zjednodušených integrací s poskytovateli náboru | [Povolení zjednodušených integrací s poskytovateli náboru](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [Nábor uchazečů o práci](./hr-personnel-recruit.md) |

## <a name="coming-soon"></a>Již brzy

Úplný seznam plánovaných funkcí a plánovaných verzí najdete v části [Přehled o 2. vlně vydání Dynamics 365 Human Resources v roce 2020](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Viz také

[Co je nového a co se změnilo v Human Resources](hr-admin-whats-new.md)</br>
[Přehled produktu Dynamics 365 Human Resources vydání 2020 vlny 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[Aktualizace procesu](hr-admin-setup-update-process.md)</br>
[Správa funkcí](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]