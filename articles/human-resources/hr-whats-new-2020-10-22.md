---
title: Co je nového a co se změnilo v aplikaci Dynamics 365 Human Resources (22. října 2020)
description: Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Human Resources k 22. říjnu 2020.
author: jcart1106
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-10-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b183ea08a2decc2696ca3bc3997b5cf7f04652d4
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/29/2022
ms.locfileid: "9068054"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-october-22-2020"></a>Co je nového a co se změnilo v aplikaci Dynamics 365 Human Resources (22. října 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Tento článek popisuje funkce, které jsou nové, změnily se nebo brzy dorazí do aplikace Dynamics 365 Human Resources. Další informace o našem procesu aktualizaci a plánu najdete v tématu [Proces aktualizace](hr-admin-setup-update-process.md).

Další informace o nových funkcích a jejich očekávaných obecných datech dostupnosti najdete v tématu [Přehled 2. vlny vydání Dynamics 365 Human Resources v roce 2020](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>V této vydané verzi

Tato verze obsahuje následující nové funkce a opravené chyby. Změny se vztahují na sestavení číslo 8.1.3680.

### <a name="new-features"></a>Nové funkce

V této verzi jsou všeobecně dostupné následující funkce.

| Funkce | Plán vydání | Dokumentace |
| --- | --- | --- |
| Platform update 10.0.14(38) | -- | [Aktualizace platformy pro verze 10.0.14 finančních a provozních aplikací (listopad 2020)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-14.md) |
| Vylepšení prostředí pracovních postupů pro správu organizace a personálu | [Vylepšení prostředí pracovního postupu pro správu organizace a personálu](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Možnost konfigurace pro umístění seznamu Pracovní položky přiřazené mně](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |


### <a name="bug-fixes"></a>Opravy chyb

Tato verze obsahuje následující opravy chyb.

> [!NOTE]
> Naším cílem dostat k vám tyto informace co nejdříve. Tento článek můžeme aktualizovat, aby obsahovalo opravy chyb, které se dostaly do sestavení poté, co byl tento článek původně publikován.

| Číslo problému| Problém  | Popis|
| --- | --- | --- |
| 437922 | Import hodin FMLA pomocí entity DMF má za následek chybu jen pro čtení. | Použití entity Hodiny FMLA k importu hodin přidružených k případu FMLA se nezdařilo. Přidali jsme logiku, abychom zajistili, že importované hodiny nepřekročí zbývající hodiny pro případ. |
| 512019 | Nesprávné množství **Poslední převod do dalšího období**. | Na stránce **Volno** se při změně hodnoty **K datu** na první den následujícího fiskálního období zobrazila nesprávná částka **Poslední převod do dalšího období** pro typ **Řádná dovolená**. Nyní zobrazuje správnou částku. |
| 458639 | Entita **Kontakty na pracovníky** nepodporuje režim sledování změn. | Aktualizovali jsme entitu **Kontakty na pracovníky**, abyste ji mohli použít při vytváření scénářů vlastní databáze (BYOD).|
| 505347 | Manažeři školení mohli odeslat žádost o pracovní volno pro zaměstnance, když byla povolena funkce Efektivní pracovník. | Jiné role než personální asistent a manažer lidských zdrojů nemají povoleno odesílat žádosti o volno pro zaměstnance. |
| 513490 | Protokolování správy zaměstnaneckých výhod: přidejte protokolování pro plány bez možností pokrytí. | Povolili jsme výsledky protokolování pro **Plán bez možností pokrytí**. Nyní se zobrazují v tabulce **Výsledky zpracování** a jsou seřazeny správně, aby se zobrazily nahoře. |
| 517021 | Nelze vybrat více plánů se stejným kódem **Typ plánu**, pokud **Typ plánu** má pro každý typ jednu registraci. | Změnili jsme omezení pro výběr plánů, kde je povolena pouze jedna registrace. Omezení jsou nyní na úrovni **Kód typu plánu** místo **Typ plánu**. Tato změna umožňuje plány jako HSA a FSA, které jsou stejného typu, ale můžete jim dát samostatný **Kód typu plánu**. Tímto způsobem můžete vybrat oba pro stejné období registrace. |
| 444791 | Nelze zobrazit kompenzaci v samoobsluze zaměstnanců, když je možnost **Omezit přístup** zapnuta v plánu kompenzace. | V samoobsluze pro zaměstnance na kartě **Kompenzace** se aktuální výše kompenzace a procento zvýšení zobrazovaly jako „0“, pokud byl zaměstnanec registrován v plánu se zapnutou možností **Omezit přístup** a přiřazen ke konkrétním rolím. Tento problém jsme vyřešili, takže zaměstnanec a manažer mohou vždy vidět podrobnosti kompenzace pro sebe a své přímé podřízené. |
| 457542 | Při aktualizaci podrobností po ukončení kurzu se neaktualizují také stejné informace pro zaměstnance, který se kurzu zúčastnil. | Informace o zaměstnanci se nyní správně aktualizují, když změníte podrobnosti kurzu po jeho uzavření a opětovném otevření. |
| 515342 | Nelze vložit data pomocí **CDSLeaveRequestDetailEntity**. Společnost nebyla nalezena nebo neexistuje. | Pro vložení dat nyní můžete použít **CDSLeaveRequestDetailEntity**. |
| 514743 | Chyba ve formuláři **Parametr e-mailu** při použití Microsoft Exchange. | Zpráva „Nelze načíst soubory nebo sestavení...“ zobrazená na stránce **Parametry e-mailu**, když byl poskytovatel e-mailu nastaven na **Exchange**. Tato oprava také umožňuje stránce **Parametry e-mailu** načítat a ukládat podle očekávání. |


## <a name="in-preview"></a>Náhled

Verze Preview obsahuje následující nové funkce. Další informace o zapnutí a vypnutí funkcí naleznete v tématu [Správa funkcí](hr-admin-manage-features.md).

| Funkce | Plán vydání | Dokumentace |
| --- | --- | --- |
| Aplikace Human Resources v Microsoft Teams | [Dovolená a nepřítomnost zaměstnanců v Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Aplikace Human Resources v Teams](./hr-admin-teams-leave-app.md)<br>[Správa žádostí o dovolenou v aplikaci Teams](hr-teams-leave-app.md) |
| Vylepšené požadavky a schválení pracovního toku | [Vylepšení prostředí pracovního postupu pro správu organizace a personálu](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Možnost konfigurace pro umístění seznamu Pracovní položky přiřazené mně](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| Virtuální entity v Dataverse pro Human Resources | [Rozšíření základních dat Dynamics 365 Human Resources v Dataverse](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/expand-dynamics-365-human-resources-core-data-common-data-service) | [Konfigurace virtuálních entit Dataverse](hr-admin-integration-common-data-service-virtual-entities.md) |
| Integrace s LinkedIn Talent Hub | [Integrace s LinkedIn Talent Hub](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [Integrace s LinkedIn Talent Hub](./hr-admin-integration-linkedin.md) |
| Vlastní odkazy v samoobsluze pro manažery | [Vlastní odkazy v samoobsluze pro manažery](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service) | [Vlastní odkazy v samoobsluze pro manažery](./hr-employee-manager-self-service-custom-links.md) |

## <a name="coming-soon"></a>Již brzy

Úplný seznam plánovaných funkcí a plánovaných verzí najdete v části [Přehled o 2. vlně vydání Dynamics 365 Human Resources v roce 2020](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).


## <a name="see-also"></a>Viz také

[Co je nového a co se změnilo v Human Resources](hr-admin-whats-new.md)</br>
[Přehled produktu Dynamics 365 Human Resources vydání 2020 vlny 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[Aktualizace procesu](hr-admin-setup-update-process.md)</br>
[Správa funkcí](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
