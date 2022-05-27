---
title: Co je nového a co se změnilo v aplikaci Dynamics 365 Human Resources (6. září 2021)
description: Tohle téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Human Resources k 6. září 2021.
author: marcelbf
ms.date: 09/06/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-09-06
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 314d836db9b7560c2ed95ad1b9d2eba753e39d2b
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2022
ms.locfileid: "8690575"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-6-2021"></a>Co je nového a co se změnilo v aplikaci Dynamics 365 Human Resources (6. září 2021)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tohle téma popisuje funkce, které jsou nové, byly změněny nebo se brzy objeví v aplikaci Microsoft Dynamics 365 Human Resources.

Další informace o našem procesu aktualizaci a plánu najdete v tématu [Proces aktualizace](hr-admin-setup-update-process.md).

Další informace o nových funkcích a jejich očekávaných obecných datech dostupnosti najdete v tématu [Přehled 2. vlny vydání Dynamics 365 Human Resources v roce 2021](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>V této vydané verzi

Tato verze obsahuje následující nové funkce a opravené chyby. Změny se vztahují na sestavení číslo 8.1.4443.

### <a name="new-features"></a>Nové funkce

V této verzi jsou všeobecně dostupné následující funkce.

| Funkce | Plán vydání | Dokumentace |
|---|---|---|
| Povolit správci nepřítomnosti správu dovolené | [Povolit správci nepřítomnosti správu dovolené](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | V této verzi aktualizujeme zobrazení pracovního prostoru správce nepřítomnosti. Další informace naleznete v tématu [Konfigurace role správce nepřítomnosti](https://go.microsoft.com/fwlink/?linkid=2168107). |
| Nakonfigurujte požadovanou přílohu podle typu dovolené | [Nakonfigurujte požadovanou přílohu podle typu dovolené](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) | [Konfigurace typů pracovního volna a absence](https://go.microsoft.com/fwlink/?linkid=2168108) |
| Nakonfigurovat jednotky pracovního volna podle typu pracovního volna | [Nakonfigurovat jednotky pracovního volna podle typu pracovního volna](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) | [Konfigurace typů pracovního volna a absence](https://go.microsoft.com/fwlink/?linkid=2168215) |

### <a name="bug-fixes"></a>Opravy chyb

Tato verze obsahuje následující opravy chyb.

> [!NOTE]
> Naším cílem dostat k vám tyto informace co nejdříve. Tohle téma můžeme aktualizovat, aby obsahovalo opravy chyb, které se dostaly do sestavení poté, co bylo toto téma původně publikováno.

| Číslo problému | Problém | popis |
|---|---|---|
| 610128 | Chyba při publikování dat při použití HcmDiscussionOverallCommentEntity | Při publikování dat ze sešitu aplikace Excel do entity HcmDiscussionOverralCommentEntity dojde k následující chybě: "Cannot locate data source record of type HcmTopicOverrall." (Nelze najít záznam zdroje dat typu HcmTopicOverrall.) |
| 589073 | Sestava EEO-1 počítá „nespecifické“ a prázdné hodnoty pro pole **Rod** jako hodnotu „Žena“. | Není-li zadána hodnota **Muž** pro pole **Rod**, generuje se v sestavě EEO-1 výchozí hodnota **Žena**. |
| 589617 | Karta Stav volna a pole K dispozici ke koupi a K dispozici k prodeji nezobrazují zůstatky, pokud jsou uživatelské role omezeny na konkrétní právnickou osobu. | Pokud je uživatel (role zaměstnance) omezen na konkrétní právnickou osobu, zůstatky se nezobrazí správně na kartě **Stav volna** a v polích **K dispozici ke koupi** a **K dispozici k prodeji**. |
| 604310 | Pokud uživatel nemá přiřazenou hierarchii nepřítomnosti, měla by být karta správce nepřítomnosti skrytá. | Pro danou právnickou osobu by karta **Správce nepřítomnosti** měla být skrytá v samoobslužném portálu, pokud není povolen parametr Mezi firmami a pokud je uživateli přiřazena alespoň jedna hierarchie absence. |

## <a name="in-preview"></a>Náhled

Verze Preview obsahuje následující nové funkce. Další informace o zapnutí a vypnutí funkcí naleznete v tématu [Správa funkcí](hr-admin-manage-features.md).

| Funkce | Plán vydání | Dokumentace |
|---|---|---|
| Povolit zjednodušenou integraci mezd (API pro integraci mezd) | [Povolení zjednodušených integrací s poskytovateli mezd](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Rozhraní API integrace mezd](hr-admin-integration-payroll-api-introduction.md) |
| Pracovní prostor správy zaměstnaneckých výhod | [Pracovní prostor správy zaměstnaneckých výhod (Preview)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Pracovní prostor správy zaměstnaneckých výhod](hr-benefits-management-workspace.md) |
| Umožněte zaměstnancům, aby byli označeni jako připraveni k výplatě | [Umožněte zaměstnancům, aby byli označeni jako připraveni k výplatě](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Připraveno k platbě](/dynamics365/human-resources/hr-compensation-payroll) |
| Vlastní pole ve Způsobilosti |[Podpora vlastních polí ve zpracování způsobilosti](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-benefits-management) | [Použití vlastních polí ve zpracování způsobilosti](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules#using-custom-fields-in-eligibility-rules) |

## <a name="coming-soon"></a>Již brzy

Úplný seznam plánovaných funkcí a plánovaných verzí najdete v části [Přehled o 2. vlně vydání Dynamics 365 Human Resources v roce 2021](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

| Funkce | Podrobnosti |
|---|---|
| Platform update 10.0.21 (45) | Vydání aktualizace platformy 10.0.21 je naplánováno spolu se servisním vydáním 4. října 2021. Další informace naleznete v tématu [Aktualizace platformy pro verze 10.0.21 finančních a provozních aplikací (říjen 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21). |
| Výkaz zaměstnaneckých výhod | Výkaz zaměstnaneckých výhod pro zobrazení aktuálních výběrů zaměstnaneckých výhod. Další informace viz [Výkaz zaměstnaneckých výhod](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/benefits-summary-statement) v dokumentu uvolnění vlny. |

## <a name="see-also"></a>Viz také

[Co je nového a co se změnilo v aplikaci Human Resources](hr-admin-whats-new.md)</br>
[Přehled produktu Dynamics 365 Human Resources vydání 2021 vlny 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Aktualizace procesu](hr-admin-setup-update-process.md)</br>
[Správa funkcí](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
