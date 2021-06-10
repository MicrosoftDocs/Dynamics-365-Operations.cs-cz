---
title: Co je nového nebo upraveného v aplikaci Dynamics 365 Human Resources, 5. dubna 2021
description: Tohle téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Human Resources k 5. dubnu 2021.
author: marcelbf
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-04-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 879a500c187e7b0a11d367c4a12618a9c60c98b7
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056461"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-5-2021"></a>Co je nového nebo upraveného v aplikaci Dynamics 365 Human Resources, 5. dubna 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tohle téma popisuje funkce, které jsou nové, byly změněny nebo se brzy objeví v aplikaci Dynamics 365 Human Resources.

Další informace o našem procesu aktualizaci a plánu najdete v tématu [Proces aktualizace](hr-admin-setup-update-process.md).

Další informace o nových funkcích a jejich očekávaných obecných datech dostupnosti najdete v tématu [Přehled 1. vlny vydání Dynamics 365 Human Resources v roce 2021](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>V této vydané verzi

Tato verze obsahuje následující nové funkce a opravené chyby. Změny se vztahují na sestavení číslo 8.1.4074.

### <a name="new-features"></a>Nové funkce

V této verzi jsou všeobecně dostupné následující funkce.

| Funkce | Plán vydání | Dokumentace |
| --- | --- | --- |
| U zaměstnanců můžete omezit jejich upravování podrobností obchodních kontaktů | [U zaměstnanců můžete omezit jejich upravování podrobností obchodních kontaktů](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [Omezení úprav osobních údajů](./hr-employee-self-service-restrict-editing.md)|

### <a name="bug-fixes"></a>Opravy chyb

Tato verze obsahuje následující opravy chyb.

> [!NOTE]
> Naším cílem dostat k vám tyto informace co nejdříve. Tohle téma můžeme aktualizovat, aby obsahovalo opravy chyb, které se dostaly do sestavení poté, co bylo toto téma původně publikováno.

| Číslo problému | Výdej |  popis |
| --- | --- | --- |
| 550852 | Tlačítko **Schválení** se neověří s povinnými poli nastavenými na formuláři **Recenze**. | Když nastavíte pole na formuláři **Recenze** jako povinné a publikujete změny pro roli manažera, formulář se neověří podle očekávání. |
| 559564 | Historické akce pracovníků pro změnu pevné kompenzace způsobují chybu pro ukončené uživatele. | Činnost pracovníka při kompenzaci zaměstnance, který odešel, dává chybu. Po odchodu zaměstnance způsobí akce povýšení pracovníka před ukončením chybu. |
| 560074 | Rozbalovací nabídka kategorie zaměstnání se nefiltruje na **Typ pracovníka** a zobrazuje kategorie pro zaměstnance a dodavatele. | Na formuláři **Zaměstnanec** by se v rozevírací nabídce **Kategorie zaměstnání** měla zobrazit kategorie zaměstnanců nebo dodavatelů na základě typu pracovníka zaměstnance. |
| 567388 | Některé informace o nově vytvořených zaměstnancích se nesynchronizují okamžitě s tabulkou **cdm_worker** v Dataverse. | Při vytváření nového záznamu zaměstnance se nový záznam synchronizuje s tabulkou **cdm_worker** stůl v Dataverse, ale ne všechny vlastnosti jsou zahrnuty do záznamu Dataverse. |
| 563837 | Funkce, které nejsou k dispozici v zobrazení Human Resources. | Ve správě funkcí se zobrazuje několik funkcí, které se nevztahují na Human Resources. Tyto funkce jsou nyní odstraněny ze seznamu funkcí, které jsou k dispozici v Human Resources. |

## <a name="in-preview"></a>Náhled

Verze Preview obsahuje následující nové funkce. Další informace o zapnutí a vypnutí funkcí naleznete v tématu [Správa funkcí](hr-admin-manage-features.md).

| Funkce | Plán vydání | Dokumentace |
| --- | --- | --- |
| Pracovní prostor správy zaměstnaneckých výhod | [Pracovní prostor správy zaměstnaneckých výhod (Preview)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Pracovní prostor správy zaměstnaneckých výhod](hr-benefits-management-workspace.md) |

## <a name="coming-soon"></a>Již brzy

| Funkce | Podrobnosti |
| --- | --- |
| Dovednosti zadané manažery pro své zaměstnance lze automaticky schválit pomocí pracovního postupu | Již brzy. |
| Platform update 10.0.17 (41) | Aktualizace platformy 10.0.17 je naplánována na zavedení s dalším vydáním 19. dubna 2021. Další informace naleznete v části [Aktualizace platformy pro verze 10.0.17 aplikací Finance and Operations (duben 2021)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-17.md). |

Úplný seznam plánovaných funkcí a plánovaných verzí najdete v části [Přehled o 1. vlně vydání Dynamics 365 Human Resources v roce 2021](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Viz také

[Co je nového a co se změnilo v Human Resources](hr-admin-whats-new.md)</br>
[Přehled produktu Dynamics 365 Human Resources vydání 2021 vlny 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Aktualizace procesu](hr-admin-setup-update-process.md)</br>
[Správa funkcí](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]