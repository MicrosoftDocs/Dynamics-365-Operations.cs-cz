---
title: Co je nového a co se změnilo v aplikaci Dynamics 365 Human Resources 22. června 2021
description: Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Human Resources k 22. červnu 2021.
author: marcelbf
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-22
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 61c457abf87ce2da554ddb1472512416159c4dca
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/29/2022
ms.locfileid: "9068417"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-22-2021"></a>Co je nového a co se změnilo v aplikaci Dynamics 365 Human Resources 22. června 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tento článek popisuje funkce, které jsou nové, změnily se nebo brzy dorazí do aplikace Dynamics 365 Human Resources.

Další informace o našem procesu aktualizaci a plánu najdete v tématu [Proces aktualizace](hr-admin-setup-update-process.md).

Další informace o nových funkcích a jejich očekávaných obecných datech dostupnosti najdete v tématu [Přehled 1. vlny vydání Dynamics 365 Human Resources v roce 2021](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>V této vydané verzi

Tato verze obsahuje následující nové funkce a opravené chyby. Změny se vztahují na sestavení číslo 8.1.4258.

### <a name="new-features"></a>Nové funkce

V této verzi jsou všeobecně dostupné následující funkce.

| Funkce | Plán vydání | Dokumentace |
| --- | --- | --- |
| Informovat uživatele pracovníků bez funkce zaměstnání - Když je zapnutý rozšířený přístup a funkce **Zobrazit všechny pracovníky bez zaměstnání** je ve správě funkcí zakázána, ve formuláři pracovníků bez zaměstnání se zobrazí banner. Banner nasměruje uživatele k zapnutí funkce **Zobrazit všechny pracovníky bez zaměstnání**. | Nelze použít| [Pracovníci bez zaměstnání](/dynamics365/human-resources/hr-personnel-workers-without-employment)|
| Podpora vlastních polí v pravidlech nároku ve správě výhod | [Vlastní podpora pole pro zpracování způsobilosti](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |[Konfigurace pravidel způsobilosti](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules) |
| Audit transakce časového rozlišení pracovního volna | Nelze použít | [Audit transakce časového rozlišení pracovního volna](hr-leave-and-absence-accrue.md)|
| Vylepšení workflowu s odchodem a nepřítomností | [Vylepšení workflowu s odchodem a nepřítomností](https://go.microsoft.com/fwlink/?linkid=2147528) | [Požádat o volno](hr-employee-self-service-request-time-off.md)|

### <a name="bug-fixes"></a>Opravy chyb

Tato verze obsahuje následující opravy chyb.

> [!NOTE]
> Naším cílem dostat k vám tyto informace co nejdříve. Tento článek můžeme aktualizovat, aby obsahovalo opravy chyb, které se dostaly do sestavení poté, co byl tento článek původně publikován.

| Číslo problému | Problém |  Popis |
| --- | --- | --- |
| 583052 | Zpětná vazba od uživatele může upravovat přijatou zpětnou vazbu | Když zaměstnanec, který obdrží zpětnou vazbu o deníku výkonu, vybere **Přidat externí odkaz**, formulář se stane upravitelným a umožní zaměstnanci upravit zpětnou vazbu k výkonu, kterou obdržel. |
| 522281 | Výběr počtu zaměstnanců na dlaždicích struktury kompenzace ve správě kompenzací vede k nesprávným výsledkům| Při přechodu do plánů odměn z pracovního prostoru odměňování se nyní zobrazuje správný počet zaměstnanců. |
| 580683 | Uživatelé přiřazení k rolím zaměstnanců a manažerů nemohou připojit poznámky nebo aktualizovat deník výkonu | Uživatelé přiřazení k rolím zaměstnanců a manažerů nemohou připojit poznámky nebo aktualizovat deník výkonu. Uživatel obdrží chybu „Nelze vytvořit záznam v záznamu deníku výkonu (HcmPerfJournal). Oprávnění zásad zabezpečení bylo odepřeno." |
| 583077 | Datum narození zaměstnance ve firemním kalendáři dovolené a nepřítomnosti zobrazuje nesprávné datum | Uživatelé budou moci zobrazit správné datum narození zaměstnanců ve firemním kalendáři dovolené a nepřítomnosti. |
| 586996 | Funkce zobrazení dovolené mezi společnostmi způsobí, že zůstatky budou prázdné, pokud je přístup omezen na jednu společnost | Uživatelé mohou správně zobrazit zůstatky budoucích dovolené zaměstnance, když je povoleno zobrazení dovolené mezi společnostmi. |
| 581014 | Povolení zobrazení mezipodnikové dovolené a absence způsobí chybu při prohlížení budoucích zůstatků | Byly opraveny chyby, když si uživatelé prohlíželi zůstatky budoucích dovolené se zapnutým zobrazením dovolené mezi společnostmi. |
| 509404 | Analýza počtu zaměstnanců oddělení nezohledňuje pohyb zaměstnanců mezi odděleními. | Když zaměstnanec migruje z jednoho oddělení do druhého, údaje o počtu zaměstnanců oddělení neodrážejí staré oddělení, ze kterého je zaměstnanec přepnut, pokud v aktuálním roce vypršela platnost podrobností o pozici. |
| 584851 | Pravidlo poměrného rozložení kreditu zaměstnaneckých výhod "Žádné“ nikdy neposkytuje kredit |Pravidlo flexibilního přerozdělování kreditů „Žádné“ vedlo k tomu, že zaměstnanci dostávali nulové kredity za období výhod bez ohledu na to, kdy byli přijati. To bylo opraveno tak, že zaměstnanec by měl dostat plné flexibilní kredity, pokud jsou najati před začátkem období výhod, a žádný, pokud jsou najati po začátku období. |
| 584897 | Duplikování povinnosti „Použít základní externí funkce“ má za následek chybu | Při pokusu o duplikování povinnosti „Použít základní externí funkkce“ se uživateli zobrazila chyba „Nelze najít objekt s identifikátorem UserDefinedAppHostDialogView.“ |
| 575692 | Časově rozlišené pracovní volno a nepřítomnost pro čekající pracovníky není k dispozici | Časové rozlišení volna a nepřítomnosti lze spustit u budoucích zaměstnanců, když je povolen **Zjednodušené zadávání zaměstnance**. |
| 580110 | Přidání společnosti k integraci mezd resetuje integraci tak, aby používala všechny entity, i když je nastavena možnost neaktualizovat projekt | Pokud zákazník odstranil entity nebo změnil datový projekt pro integraci mezd a má nastavenou možnost zabránit automatickému obnovení projektu, přidání nové společnosti do integrace nastavení ignoruje a aktualizuje projekt.  |
| 584518 |Problém s výkonem zpracování registrace zaměstnaneckých výhod | Tato chyba řešila problémy s výkonem ve starším procesu registrace zaměstnaneckých výhod. |

## <a name="in-preview"></a>Náhled

Verze Preview obsahuje následující nové funkce. Další informace o zapnutí a vypnutí funkcí naleznete v tématu [Správa funkcí](hr-admin-manage-features.md).

| Funkce | Plán vydání | Dokumentace |
| --- | --- | --- |
| Pracovní prostor správy zaměstnaneckých výhod | [Pracovní prostor správy zaměstnaneckých výhod (Preview)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Pracovní prostor správy zaměstnaneckých výhod](hr-benefits-management-workspace.md) |
| Povolit zjednodušenou integraci mezd (API pro integraci mezd) | [Povolení zjednodušených integrací s poskytovateli mezd](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Rozhraní API integrace mezd](hr-admin-integration-payroll-api-introduction.md)|


## <a name="coming-soon"></a>Již brzy

| Funkce | Podrobnosti |
| --- | --- |
| Platform update 10.0.19 (43) | Aktualizace platformy 10.0.19 je naplánována na zavedení se servisním vydáním 28. června 2021. Další informace naleznete v tématu [Aktualizace platformy pro verze 10.0.19 finančních a provozních aplikací (červen 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-19). |
|  Přepínání zobrazení počtu let ve společnosti | Tato funkce poskytuje možnost použít různá data k výpočtu let služby ve společnosti zobrazených ve formuláři **Zjednodušené zadávání zaměstnance** a ve formuláři **Lidé**.  To bude k dispozici v parametrech Human Resources. |
|  Povolit správci nepřítomnosti správu dovolené | [Povolit správci nepřítomnosti správu dovolené](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) |
|  Přílohy zmocnění pro konkrétní typy pracovního volna | Tato funkce umožňuje správcům nařídit přidání příloh při odesílání žádostí o pracovní volno u konkrétních typů pracovního volna. |
|  Nakonfigurovat jednotky pracovního volna podle typu pracovního volna | Tato funkce umožňuje správcům konfigurovat jednotky dovolené (hodiny nebo dny) pro každý typ dovolené.  |
| Umožněte zaměstnancům, aby byli označeni jako připraveni k výplatě | [Umožněte zaměstnancům, aby byli označeni jako připraveni k výplatě](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) |

Úplný seznam plánovaných funkcí a plánovaných verzí najdete v části [Přehled o 1. vlně vydání Dynamics 365 Human Resources v roce 2021](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Viz také

[Co je nového a co se změnilo v Human Resources](hr-admin-whats-new.md)</br>
[Přehled produktu Dynamics 365 Human Resources vydání 2021 vlny 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Aktualizace procesu](hr-admin-setup-update-process.md)</br>
[Správa funkcí](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

