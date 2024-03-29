---
title: Co je nového nebo změněného v aplikaci Dynamics 365 Human Resources 21 leden 2021
description: Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Human Resources k 21. lednu 2021.
author: marcelbf
ms.date: 01/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-01-21
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1f1daf630d3a9354012db9b5b487d8a5ed11e0ed
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/29/2022
ms.locfileid: "9066693"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-january-21-2021"></a>Co je nového nebo změněného v aplikaci Dynamics 365 Human Resources 21 leden 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tento článek popisuje funkce, které jsou nové, změnily se nebo brzy dorazí do aplikace Dynamics 365 Human Resources.

Další informace o našem procesu aktualizaci a plánu najdete v tématu [Proces aktualizace](hr-admin-setup-update-process.md).

Další informace o nových funkcích a jejich očekávaných obecných datech dostupnosti najdete v tématu [Přehled 2. vlny vydání Dynamics 365 Human Resources v roce 2020](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).


## <a name="in-this-release"></a>V této vydané verzi

Tato verze obsahuje následující nové funkce a opravené chyby. Změny se vztahují na sestavení číslo 8.1.3866.

### <a name="new-features"></a>Nové funkce

V této verzi jsou všeobecně dostupné následující funkce.

| Funkce | Plán vydání | Dokumentace |
| --- | --- | --- |
| Platform update 10.0.16(40) | -- | [Aktualizace platformy pro verze 10.0.16 finančních a provozních aplikací (únor 2021)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-16.md) |
| Vylepšené požadavky a schválení pracovního toku | [Vylepšení prostředí pracovního postupu pro správu organizace a personálu](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Možnost konfigurace pro umístění seznamu Pracovní položky přiřazené mně](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| Aktualizace souladu zákona Affordable Care Act (ACA) pro formulář 1095-C, formulář 1095-B a elektronické hlášení ve starší verzi Benefits | -- | -- | 
| Správa zaměstnaneckých výhod nyní podporuje podávání zpráv o shodě s ACA pro právnické osoby se sídlem v USA | -- | [Generujte zprávy ACA ve Správě zaměstnaneckých výhod](hr-benefits-management-aca-reports.md) |
| Správa zaměstnaneckých výhod má nyní vystaveny úrovně sazeb výhod a entity s dvojí úrovní výhod  | -- | -- |

### <a name="bug-fixes"></a>Opravy chyb

Tato verze obsahuje následující opravy chyb.

> [!NOTE]
> Naším cílem dostat k vám tyto informace co nejdříve. Tento článek můžeme aktualizovat, aby obsahovalo opravy chyb, které se dostaly do sestavení poté, co byl tento článek původně publikován.

| Číslo problému | Problém |  Popis |
| --- | --- | --- |
| 533079 | Chyba navigace „Formulář byl volán nesprávně“, když se pokoušíme zjistit odpočty. | Opravená chyba při pohledu na odpočty výhod se zobrazení **K datu**. |
| 543641 | PSČ se při elektronickém hlášení neuvádí.  | Opravená interní chyba na PSČ, který se nezobrazoval v elektronických zprávách ACA pro správu výhod, když je kód pokrytí M až Q. |
| 542815 | Obrazovka osobních kontaktů v samoobsluze zaměstnanců umožňuje zaměstnancům vidět osobní kontakty ostatních. | Opravená chyba, kdy formulář **Upravit** pro samoobslužné osobní kontakty zaměstnanců neomezuje svoje dotazy natolik, aby zaručil, že se načte pouze jeden osobní kontakt, což uživateli umožňuje používat klávesové zkratky k zobrazení kontaktů jiných lidí. |
| 536157 | Nelze otevřít stránku **Integrace Microsoft Dataverse** ve Správě systému kvůli volání IsVirtualEntityPackageInstalled(). | Problém brání stránce **Integrace Microsoft Dataverse** v načítání v Human Resources. |
| 533079 | Chyba navigace „Formulář byl volán nesprávně“, když se pokoušíme zjistit odpočty. | Opravená chyba formuláře **Odpočty** pro správu zaměstnaneckých výhod při prohlížení **K datu**. |
| 537264 | Pevná záložka **Osobní informace** v záznamu kandidáta chybí. | Osobní údaje kandidáta jsou nyní k dispozici v záznamu kandidáta. |
| 537267 | **Profesionální zkušenosti** se nezobrazují na interních záznamech kandidátů. | Pevná záložka **Profesionální zkušenosti** se nyní zobrazují v interních záznamech kandidátů. Dříve, pokud byl kandidát interní, **Profesionální zkušenosti** byly nahrazen **Historií zaměstnání**, což je historie zaměstnání kandidáta v rámci organizace. Oba jsou použitelné a musí se zobrazovat pro interní kandidáty. |
| 537067 | **Povoleno kontaktovat zaměstnavatele** se nezobrazuje. | Ovládací prvek **Povoleno kontaktovat zaměstnavatele** byl přidána do podokna **Upravit profesionální zkušenosti** pro záznam kandidáta. |
| 525957 | **Stav kandidáta** se po dokončení přenosu neaktualizuje na interních kandidátech. | Po dokončení přenosu (je vybráno tlačítko **Změit pozici** nebo **Pokračovat** na stránce **Přenést pracovníka na nové přiřazení pozice**), **Stav** v záznamu kandidáta se musí změnit na **Zařazen**. |
| 537051 | Symboly měny pro indickou rupii a tureckou liru se nesynchronizují správně v Dataverse | Symboly měny pro indickou rupii a tureckou liru se nyní synchronizují správně v Dataverse. |
| 534846 | Pro správu dat musí být povoleny náborové tabulky. | Nové tabulky vytvořené pro žádosti o nábor a kandidáty jsou nyní povoleny pro Správu dat. To umožňuje povolit sledování změn u tabulek, což umožňuje sledování změn OData ve virtuálních tabulkách Dataverse. |
| 533474 | Opravte chybějící odkaz na Microsoft.SqlServer.XEvent.dll. | Výjimky načtení sestavy pro Microsoft.SqlServer.XEvent.dll blokovaly nastavení virtuálních tabulek Dataverse v některých prostředích. |
| 481122 | Pracovní prostor **Lidé** zobrazují vyřazení pozice. | Vyřazené pozice byly zobrazeny jako otevřené pozice v pracovním prostoru **Lidé**. Vyřazené pozice se již nezobrazují. | 
| 541978 | Přidejte primární e-mailovou adresu do entity BaseWorker. | Tato změna přidala primární e-mailovou adresu pracovníka do HcmWorkerBaseEntity. |

## <a name="in-preview"></a>Náhled

Verze Preview obsahuje následující nové funkce. Další informace o zapnutí a vypnutí funkcí naleznete v tématu [Správa funkcí](hr-admin-manage-features.md).

| Funkce | Plán vydání | Dokumentace |
| --- | --- | --- |
| Aplikace Human Resources v Microsoft Teams | [Dovolená a nepřítomnost zaměstnanců v Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Aplikace Human Resources v Teams](./hr-admin-teams-leave-app.md)<br>[Správa žádostí o dovolenou v aplikaci Teams](hr-teams-leave-app.md) |
| Integrace s LinkedIn Talent Hub | [Integrace s LinkedIn Talent Hub](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [Integrace s LinkedIn Talent Hub](./hr-admin-integration-linkedin.md) |
| Zobrazení pracovního volna manažery napříč společnostmi | [Zobrazení pracovního volna zaměstnanců manažery napříč společnostmi](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Konfigurace parametrů pracovního volna a absence](./hr-leave-and-absence-parameters.md) |
|Poskytnutí dalších přehledů zůstatků pracovního volna| [Poskytnutí dalších přehledů zůstatků pracovního volna](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/provide-additional-insight-into-leave-balances) | [Správa pracovního volna zaměstnanců](./hr-leave-and-absence-manage-employee-leave.md) |
| Manažeři mohou odesílat žádosti o nábor na volné pozice | [Manažeři mohou odesílat žádosti o nábor na volné pozice](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [Přidání žádosti o nábor](./hr-personnel-recruit.md#add-a-recruiting-request) |
| Vylepšený profil kandidáta ve správě zaměstnanců | [Vylepšený profil kandidáta ve správě zaměstnanců](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [Přidání nebo úprava profilu kandidáta](./hr-personnel-recruit.md#add-or-edit-a-candidate-profile) |
| Povolení zjednodušených integrací s poskytovateli náboru | [Povolení zjednodušených integrací s poskytovateli náboru](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [Nábor uchazečů o práci](./hr-personnel-recruit.md) |

## <a name="coming-soon"></a>Již brzy
| Funkce | Podrobnosti |
| --- | --- |
| E-mailové potvrzení pro registrace zaměstnaneckých výhod | Tato funkce zajistí možnost odeslat zaměstnancům potvrzovací e-mail, když se registrují k zaměstnaneckým výhodám v samoobsluze pro zaměstnance. Další informace viz [Konfigurace parametrů správy zaměstnaneckých výhod podle společnosti](hr-benefits-setup-parameters-per-company.md). |
| Dovednosti zadané manažery pro své zaměstnance lze automaticky schválit pomocí pracovního postupu | Již brzy. |

Úplný seznam plánovaných funkcí a plánovaných verzí najdete v části [Přehled o 2. vlně vydání Dynamics 365 Human Resources v roce 2020](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="terminology-updates-for-microsoft-dataverse"></a>Aktualizace terminologie pro Microsoft Dataverse

S platností od listopadu 2020 byl Common Data Service přejmenován na [Microsoft Dataverse](/powerapps/maker/data-platform/data-platform-intro). Viz [oficiální oznámení](https://powerapps.microsoft.com/blog/reshape-the-future-of-work-with-microsoft-dataverse-for-teams-now-generally-available/) na blogu Power Apps, kde se dozvíte více. V souvislosti s touto změnou názvu byla provedena aktualizace terminologie v Dataverse. Například *entita* je nyní *tabulka* a *pole* je nyní *sloupec*. Další informace viz [aktualizace terminologie](/powerapps/maker/data-platform/data-platform-intro#terminology-updates).

V této verzi byla terminologie související s integrací Dynamics 365 Human Resources s Dataverse v celé aplikaci aktualizována, aby odrážela tyto změny. Například formulář **Integrace Common Data Service** formulář je nyní **Integrace Microsoft Dataverse**.

Chcete-li se dozvědět více o integraci Dynamics 365 Human Resources s Microsoft Dataverse, přečtěte si [Konfigurace integrace Microsoft Dataverse](./hr-admin-integration-common-data-service.md) a [Konfigurace virtuálních tabulek Microsoft Dataverse](./hr-admin-integration-common-data-service-virtual-entities.md).

## <a name="see-also"></a>Viz také

[Co je nového a co se změnilo v Human Resources](hr-admin-whats-new.md)</br>
[Přehled produktu Dynamics 365 Human Resources vydání 2020 vlny 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[Aktualizace procesu](hr-admin-setup-update-process.md)</br>
[Správa funkcí](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
