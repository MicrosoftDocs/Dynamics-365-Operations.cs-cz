---
title: Co je nového nebo změněného v aplikaci Dynamics 365 Human Resources, 22. března 2021
description: Tohle téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Human Resources k 22. březnu 2021.
author: marcelbf
ms.date: 03/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-03-22
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 13520ca55c98fb1acb6185af393550b12fbc2072
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2022
ms.locfileid: "8693521"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-22-2021"></a>Co je nového nebo změněného v aplikaci Dynamics 365 Human Resources, 22. března 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tohle téma popisuje funkce, které jsou nové, byly změněny nebo se brzy objeví v aplikaci Dynamics 365 Human Resources.

Další informace o našem procesu aktualizaci a plánu najdete v tématu [Proces aktualizace](hr-admin-setup-update-process.md).

Další informace o nových funkcích a jejich očekávaných obecných datech dostupnosti najdete v tématu [Přehled 1. vlny vydání Dynamics 365 Human Resources v roce 2021](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>V této vydané verzi

Tato verze obsahuje následující nové funkce a opravené chyby. Změny se vztahují na sestavení číslo 8.1.4049.

### <a name="new-features"></a>Nové funkce

V této verzi jsou všeobecně dostupné následující funkce.

| Funkce | Plán vydání | Dokumentace |
| --- | --- | --- |
| Možnost vynutit zrušení a resetování zaseknutých dávkových úloh (560976) | NA | [Reset zablokovaných dávkových úloh](./hr-admin-troubleshooting-batch-execution.md) |
| Drobné aktualizace uživatelských zkušeností (UX) při vytváření nového plánu zaměstnaneckých výhod (419941) | NA | [Vytvoření plánu zaměstnaneckých výhod](hr-benefits-plans-setup.md) |

### <a name="bug-fixes"></a>Opravy chyb

Tato verze obsahuje následující opravy chyb.

> [!NOTE]
> Naším cílem dostat k vám tyto informace co nejdříve. Tohle téma můžeme aktualizovat, aby obsahovalo opravy chyb, které se dostaly do sestavení poté, co bylo toto téma původně publikováno.

| Číslo problému | Výdej |  popis |
| --- | --- | --- |
| 554239 | Vylepšení výkonu u entit souvisejících s tabulkou **BusinessProcessTaskAssignment** | Zlepšení výkonnosti entit souvisejících s tabulkou **BusinessProcessTaskAssignment** přidáním doporučených indexů do tabulky. |
| 566061 | Odebrání záložního kódu entit V2 z noční synchronizace | Odebrání záložního kódu V2 pro noční synchronizace Dataverse. Záložní řešení již není nutné a brání filtrované synchronizaci pracovat podle očekávání. Tato změna zvyšuje konzistenci synchronizace dat Dataverse. |
| 538024 | Plány zaměstnaneckých výhod pracovníka > Odebrat vyvolání chyby pokladny | Opravená chyba při odebírání pokladny pro možnost Plán zaměstnaneckých výhod ve formuláři Zaměstnanecké výhody. |
| 557965 | Pracovní prostor **Výhody**: odkaz **Aktivní životní události** by měl být vždy viditelný v části **Odkazy** | Opraven problém, kdy odkaz **Aktivní životní události** byl viditelný v části **Odkazy**, ale vyvolával chybu při pokusu o přechod na něj, pokud není povolena funkce **(Náhled) Pracovní prostor pro správu výhod**. Další informace o povolení pracovního prostoru najdete v tématu [Pracovní prostor pro správu výhod](hr-benefits-management-workspace.md). |
| 556672 | Nelze zpracovat časové rozlišení pro ukončeného zaměstnance, když je ve správě funkcí povolena možnost **Zjednodušené zadávání zaměstnance** | Byla přidána možnost časového rozlišení plánů pracovního volna a absence do části **Další možnosti** v části **Historie práce** pro zaměstnance, když je ve správě funkcí povolena možnost **Zjednodušené zadávání zaměstnance**. |
| 562656 | Položka nabídky **SysRecordChangeLogValidTimeState** by měla být zahrnuta do oprávnění zabezpečení a rozšíření funkčního oprávnění zabezpečení **SystemExternalBasicMaintain** | U rolí nesystémových správců chybělo tlačítko **Zobrazit změny** ve formulářích správce dat. |
| 505989 | Zpracování životních událostí: Změna způsobilosti nebyla zpracována správně kvůli použitému datu | Opraven problém, kdy změna ve zpracování způsobilosti závisela na počátečním datu pozice a nejenom na aktuální pozici. |
| 562286 | Ukončení pracovníka odešle více aktualizací do Dataverse | Když je pracovní poměr ukončen, je odeslána více než jedna operace aktualizace do Dataverse, což má za následek dvě oznámení o aktualizaci pro stejnou změnu. To může způsobit vyvolání více triggerů, pokud je tok Power Automate nakonfigurován na spuštění z akce. |
| 527340 | Při otevírání registrace pracovního volna a absence se zobrazí chyba „Nevyjádřitelný datum a čas“ | Při výběru registrace pracovního volna a absence se chyba již nezobrazí. |
| 561663 | Prodloužený interval čekání na zřizování clusteru | Zlepšená stabilita infrastruktury a konzistence zajišťování pomocí aktualizací zajišťování klastrů. |
| 486129 | Nelze upravit vlastní pole v nabídce **Pozice> Spravovat změny** | Opraven problém, kdy nebylo možné upravovat vlastní pole na kartě **Spravovat změny** pro **Pozice**. |

## <a name="in-preview"></a>Náhled

Verze Preview obsahuje následující nové funkce. Další informace o zapnutí a vypnutí funkcí naleznete v tématu [Správa funkcí](hr-admin-manage-features.md).

| Funkce | Plán vydání | Dokumentace |
| --- | --- | --- |
| Pracovní prostor správy zaměstnaneckých výhod | [Pracovní prostor správy zaměstnaneckých výhod (Preview)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Pracovní prostor správy zaměstnaneckých výhod](hr-benefits-management-workspace.md) |
| U zaměstnanců můžete omezit jejich upravování podrobností obchodních kontaktů | [U zaměstnanců můžete omezit jejich upravování podrobností obchodních kontaktů](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [Omezení úpravy osobních údajů](hr-employee-self-service-restrict-editing.md)|

## <a name="coming-soon"></a>Již brzy

| Funkce | Podrobnosti |
| --- | --- |
| Dovednosti zadané manažery pro své zaměstnance lze automaticky schválit pomocí pracovního postupu | Již brzy. |

Úplný seznam plánovaných funkcí a plánovaných verzí najdete v části [Přehled o 1. vlně vydání Dynamics 365 Human Resources v roce 2021](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Viz také

[Co je nového a co se změnilo v Human Resources](hr-admin-whats-new.md)</br>
[Přehled produktu Dynamics 365 Human Resources vydání 2021 vlny 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Aktualizace procesu](hr-admin-setup-update-process.md)</br>
[Správa funkcí](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]