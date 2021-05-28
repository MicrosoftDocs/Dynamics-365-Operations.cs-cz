---
title: Co je nového nebo upraveného v aplikaci Dynamics 365 Human Resources, 19. dubna 2021
description: Tohle téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Human Resources k 19. dubnu 2021.
author: marcelbf
ms.date: 04/19/2021
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
ms.author: marcelbf
ms.search.validFrom: 2021-04-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d0a908a6c1c8d8e08be61b684d29e9b37468ef80
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019243"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-19-2021"></a>Co je nového nebo upraveného v aplikaci Dynamics 365 Human Resources, 19. dubna 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tohle téma popisuje funkce, které jsou nové, byly změněny nebo se brzy objeví v aplikaci Dynamics 365 Human Resources.

Další informace o našem procesu aktualizaci a plánu najdete v tématu [Proces aktualizace](hr-admin-setup-update-process.md).

Další informace o nových funkcích a jejich očekávaných obecných datech dostupnosti najdete v tématu [Přehled 1. vlny vydání Dynamics 365 Human Resources v roce 2021](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>V této vydané verzi

Tato verze obsahuje následující nové funkce a opravené chyby. Změny se vztahují na sestavení číslo 8.1.4113.

### <a name="new-features"></a>Nové funkce

V této verzi jsou všeobecně dostupné následující funkce.

| Funkce | Plán vydání | Dokumentace |
| --- | --- | --- |
| Platform update 10.0.17 (41) | -- | [Platform Update pro verzi 10.0.17 aplikací Finance and Operations (duben 2021)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-17.md) |
| Podpora vlastních polí ve formulářích pro správu výhod | [Podpora vlastních polí ve správě výhod](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-benefits-management)| [Přehled správy zaměstnaneckých výhod](hr-benefits-management-overview.md)|

### <a name="bug-fixes"></a>Opravy chyb

Tato verze obsahuje následující opravy chyb.

> [!NOTE]
> Naším cílem dostat k vám tyto informace co nejdříve. Tohle téma můžeme aktualizovat, aby obsahovalo opravy chyb, které se dostaly do sestavení poté, co bylo toto téma původně publikováno.

| Číslo problému | Výdej |  popis |
| --- | --- | --- |
| 552164 | **Uložené zobrazení** na **Zaměstnanecká samoobsluha > Otevřené kurzy** nefunguje pro kurzy, které obsahují agendu | Pokud se na otevřených kurzech (ESS) používá uložené zobrazení a k jednomu z kurzů je připojena Agenda, pak se u daného kurzu již nebude zobrazovat více řádků |
| 560614 | **Výhody > Možnosti životních událostí** zobrazují nesrovnalosti v dokumentaci popisku nástroje a chování kódu. | Aktualizované popisy v **Možnostech životních událostí** k zobrazení správného chování. |
| 560616 | **Výhody > Možnosti životních událostí** jsou upravitelné v plánu zaměstnaneckých výhod, ale změny nejsou ovlivněny. | Aktualizované chování možnosti životních událostí přepne na zapnout nebo zakázat na základě závislých možností dokumentaci nápovědy. |
| 565054 | Nelze zobrazit obsah seznamu **Pracovníci bez zaměstnání**, když je zapnutý **Pokročilý přístup**. | Toto vydání opravuje problém, kdy když byl zapnut **Pokročilý přístup**, obsah seznamu **Pracovníci bez zaměstnání** mohli zobrazit pouze správci systému. Protože tato oprava představuje změnu zabezpečení, budete se k ní muset přihlásit ve správě funkcí. Jakmile je funkce zapnutá, ty role, které mají přístup k formuláři, uvidí obsah, i když je zapnutý rozšířený přístup. Další informace viz [Pracovníci bez zaměstnání](hr-personnel-workers-without-employment.md). |
| 570586 | Ověření požadavku na dovolenou se nezdaří, když zaměstnání skončí před poslední transakcí daného pracovníka ve všech plánech dovolené. | Po skončení pracovního poměru se nezdaří ověření žádosti o dovolenou na základě transakcí s odchodem zaměstnance.|
| 570783 | Povolení a zakázání mezipodnikové dovolené ve sdílených parametrech lidských zdrojů mění to, co zaměstnanci zaměstnaní v jedné společnosti vidí v žádostech o dovolenou. | Zaměstnanci zaměstnaní v jedné společnosti nevidí žádné změny v požadavcích na volno, pokud je parametr povolen nebo zakázán. |
| 572343 | Kód požadované příčiny se nezobrazí, pokud je povolena funkce zobrazení mezipodnikové dovolené. | Pokud je povolena funkce zobrazení mezipodnikové dovolené, kód důvodu se nyní zobrazí podle očekávání. |
| 573676 | Nelze přidat **Doba** do **Správa výhod > Odkazy > Plány výhod**. | Opravené chyby, kde možnost **Doba** nelze přidat nebo aktualizovat na stávajícími formuláři **Plán výhod**. |

## <a name="in-preview"></a>Náhled

Verze Preview obsahuje následující nové funkce. Další informace o zapnutí a vypnutí funkcí naleznete v tématu [Správa funkcí](hr-admin-manage-features.md).

| Funkce | Plán vydání | Dokumentace |
| --- | --- | --- |
| Pracovní prostor správy zaměstnaneckých výhod | [Pracovní prostor správy zaměstnaneckých výhod (Preview)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Pracovní prostor správy zaměstnaneckých výhod](hr-benefits-management-workspace.md) |
| Vylepšení workflowu s odchodem a nepřítomností | [Vylepšení workflowu s odchodem a nepřítomností](https://go.microsoft.com/fwlink/?linkid=2147528) | [Požádat o volno](hr-employee-self-service-request-time-off.md)|
| Povolit zjednodušenou integraci mezd (API pro integraci mezd) | [Povolení zjednodušených integrací s poskytovateli mezd](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Rozhraní API integrace mezd](hr-admin-integration-payroll-api-introduction.md)|

## <a name="coming-soon"></a>Již brzy

| Funkce | Podrobnosti |
| --- | --- |
| Dovednosti zadané manažery pro své zaměstnance lze automaticky schválit pomocí pracovního postupu | Již brzy. |
| Platform update 10.0.18 (42) | Aktualizace platformy 10.0.18 je naplánována na zavedení se servisním vydáním 17. května 2021. Další informace naleznete v části [Aktualizace platformy pro verze 10.0.18 aplikací Finance and Operations (květen 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-18). |
| Podpora vlastních polí v pravidlech nároku ve správě výhod  | [Vlastní podpora pole pro zpracování způsobilosti](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |

Úplný seznam plánovaných funkcí a plánovaných verzí najdete v části [Přehled o 1. vlně vydání Dynamics 365 Human Resources v roce 2021](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Viz také

[Co je nového a co se změnilo v Human Resources](hr-admin-whats-new.md)</br>
[Přehled produktu Dynamics 365 Human Resources vydání 2021 vlny 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Aktualizace procesu](hr-admin-setup-update-process.md)</br>
[Správa funkcí](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
