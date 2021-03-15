---
title: Co je nového a co se změnilo v aplikaci Dynamics 365 Human Resources (26. září 2020)
description: Tohle téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Human Resources k 26. září 2020.
author: jcart1106
manager: tfehr
ms.date: 09/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ac72489c3b2dacfde280606a83221e8514793701
ms.sourcegitcommit: 2190be6c205d7d9e43bdb99b9190cc0112f9f093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/10/2021
ms.locfileid: "5152190"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-26-2020"></a>Co je nového a co se změnilo v aplikaci Dynamics 365 Human Resources (26. září 2020)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Tohle téma popisuje funkce, které jsou nové, byly změněny nebo se brzy objeví v aplikaci Dynamics 365 Human Resources. Další informace o našem procesu aktualizaci a plánu najdete v tématu [Proces aktualizace](hr-admin-setup-update-process.md).

Další informace o nových funkcích a jejich očekávaných obecných datech dostupnosti najdete v tématu [Přehled 2. vlny vydání Dynamics 365 Human Resources v roce 2020](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>V této vydané verzi

Tato verze obsahuje následující nové funkce a opravené chyby. Změny se vztahují na sestavení číslo 8.1.3589-hf.3.

### <a name="new-features"></a>Nové funkce

V této verzi je všeobecně dostupná následující funkce:

- **Aktualizace platformy 10.0.13 je nyní k dispozici**: Další informace o aktualizaci viz [Aktualizace platformy pro verzi 10.0.13 aplikací Finance and Operations (říjen 2020)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-13).

### <a name="bug-fixes"></a>Opravy chyb

Tato verze obsahuje následující opravy chyb.

> [!NOTE]
> Naším cílem je k vám dostat tyto informace co nejdříve. Mohou existovat aktualizace tohoto tématu zahrnující opravy chyb, které se dostaly do sestavení poté, co bylo toto téma původně publikováno.

| Číslo problému | Výdej | popis |
| --- | --- | --- |
| 469495 | Aktualizace výchozí mřížky a dialogového okna finančních dimenzí | Mřížka a dialogové okno finančních dimenzí jsou v aplikaci Human Resources aktualizovány. |
| 474887 | Pracovní položka žádosti o pracovní volno otevře nesprávný odkaz v ručním rozhodnutí | Pokud konfigurace pracovního postupu obsahuje ruční rozhodnutí, přechod na žádost o pracovní volno z části **Pracovní položky přiřazené mně** otevře nesprávný odkaz a zobrazí buď prázdný formulář nebo žádost o pracovní volno vytvořenou aktuálním uživatelem namísto toho, který jim byl přidělen pro ruční rozhodnutí. |
| 474962 | Entita parametrů pracovního volna a absence obsahuje pole s nejednoznačnými popisky | Popisky entity parametrů pracovního volna a absence jsou aktualizovány, aby byly srozumitelnější. |
| 481401 | Zpracování časového rozlišení přestane reagovat, pokud je základ data časového rozlišení po počátečním datu časového rozlišení a na konci měsíce | Zpracování časového rozlišení je aktualizováno tak, aby nemělo zpoždění, pokud je základ časového rozlišení po počátečním datu časového rozlišení a na konci měsíce. |
| 447167 | Seznamy záznamů s končící platností obsahují neaktivní pracovníky | Karta **Záznamy s končící platností** v sekci **Správa zaměstnanců** obsahovala neaktivních pracovníky. Nyní obsahuje pouze aktivní pracovníky. |
| 486840 | Ze sekce **Pracovní položky přiřazené mně** se otevírá chybná žádost o pracovní volno | Výběr žádosti o pracovní volno ze sekce **Pracovní položky přiřazené mně** již neotevře poslední žádost o pracovní volno nebo absenci přiřazenou aktuálnímu uživateli. |
| 506868 | Pole **Funkce** pro Dataverse není nastaveno na entitu **Pracovní pozice** | Pole **Funkce** v entitách **Pozice** a **Pracovní pozice** se zobrazovalo jako nezadané. Pole **Funkce** se nyní zobrazuje. |
| 430359 | Nelze přistupovat k úkolům kontrolního seznamu pro zrušení zprovoznění s přiřazenými rolemi manažera a zaměstnance | Pracovníci s budoucím datem ukončení pracovního poměru neměli přístup k úkolům kontrolního seznamu, pokud měli pouze roli zaměstnance nebo manažera. Nyní mohou k úkolům pro zrušení zprovoznění přistupovat uživatelé pouze s rolí zaměstnance nebo manažera s budoucím datem ukončení pracovního poměru. |
| 458102 | Nový zaměstnanec se neobjeví v entitě **Informace o mzdách pracovníka** při jejím vytvoření | Noví zaměstnanci jsou zahrnuti do entity informací o mzdách pracovníků, aniž by museli před exportem entity pro zaměstnance otevírat informace o mzdě. |

## <a name="in-preview"></a>Náhled

Verze Preview obsahuje následující nové funkce. Další informace o zapnutí a vypnutí funkcí naleznete v tématu [Správa funkcí](hr-admin-manage-features.md).

| Funkce | Plán vydání | Dokumentace |
| --- | --- | --- |
| Aplikace Human Resources v Microsoft Teams | [Dovolená a nepřítomnost zaměstnanců v Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Aplikace Human Resources v Teams](https://go.microsoft.com/fwlink/?linkid=2127841)<br>[Správa žádostí o dovolenou v aplikaci Teams](hr-teams-leave-app.md) |
| Vylepšené požadavky a schválení pracovního toku | [Vylepšení prostředí pracovního postupu pro správu organizace a personálu](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Možnost konfigurace pro umístění seznamu Pracovní položky přiřazené mně](https://docs.microsoft.com/dynamics365/human-resources/hr-whats-new-2020-09-03#configuration-option-to-position-work-items-assigned-to-me-list-477004) |

## <a name="coming-soon"></a>Již brzy

Následující nová funkce je naplánována do budoucího vydání:

- [Vlastní odkazy v samoobsluze pro manažery](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service)

Úplný seznam plánovaných funkcí a plánovaných verzí najdete v části [Přehled o 2. vlně vydání Dynamics 365 Human Resources v roce 2019](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/).

## <a name="additional-resources"></a>Další prostředky

[Co je nového nebo co se změnilo v Human Resources](hr-admin-whats-new.md)
[Přehled 2. vlny vydání Dynamics 365 Human Resources v roce 2020](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)
[Proces aktualizace](hr-admin-setup-update-process.md)
[Správa funkcí](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]