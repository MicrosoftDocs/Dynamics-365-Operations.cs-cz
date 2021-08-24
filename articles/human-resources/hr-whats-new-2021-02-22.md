---
title: Co je nového nebo změněného v aplikaci Dynamics 365 Human Resources, 22. února 2021
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Human Resources k 22. únoru 2021.
author: marcelbf
ms.date: 02/22/2021
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
ms.search.validFrom: 2021-02-22
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 379a902489bdccdfa3490a830cc3b0bbf7639e7f0b62079a3ff3a999b0a7c412
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6721552"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-february-22-2021"></a>Co je nového nebo změněného v aplikaci Dynamics 365 Human Resources, 22. února 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tohle téma popisuje funkce, které jsou nové, byly změněny nebo se brzy objeví v aplikaci Dynamics 365 Human Resources.

Další informace o našem procesu aktualizaci a plánu najdete v tématu [Proces aktualizace](hr-admin-setup-update-process.md).

Další informace o nových funkcích a jejich očekávaných obecných datech dostupnosti najdete v tématu [Přehled 1. vlny vydání Dynamics 365 Human Resources v roce 2021](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>V této vydané verzi

Tato verze obsahuje následující nové funkce a opravené chyby. Změny se vztahují na sestavení číslo 8.1.3988.

### <a name="new-features"></a>Nové funkce

V této verzi jsou všeobecně dostupné následující funkce.

| Funkce | Plán vydání | Dokumentace |
| --- | --- | --- |
| Aplikace Dynamics 365 Human Resources pro Microsoft Teams | [Dovolená a nepřítomnost zaměstnanců v Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Aplikace Human Resources v Teams](./hr-admin-teams-leave-app.md)<br>[Správa žádostí o dovolenou v aplikaci Teams](hr-teams-leave-app.md) |

### <a name="bug-fixes"></a>Opravy chyb

Tato verze obsahuje následující opravy chyb.

> [!NOTE]
> Naším cílem dostat k vám tyto informace co nejdříve. Tohle téma můžeme aktualizovat, aby obsahovalo opravy chyb, které se dostaly do sestavení poté, co bylo toto téma původně publikováno.

| Číslo problému | Výdej |  popis |
| --- | --- | --- |
| 529994 | Úpravy pole **Známý jako** ve formuláři **Pracovník** nespustí aktualizaci Dataverse | Opraven problém, kdy se Dataverse neaktualizuje poté, co je pole **Známý jako** ve formuláři **Pracovník** aktualizováno. |
| 532651 | Zpráva PBI pro analýzu kompenzací nepoužívá při výpočtu metrik pro celou společnost převod měn | Opraven problém, kdy zpráva PBI pro analýzu kompenzací neprovedla správně převody měn. |
| 552226 | Zpracování životních událostí několikrát zavře a znovu otevře plány pro jednu životní událost  | Opraven problém, kdy se pro zaměstnance ve více právnických osobách a výskytu životní události generuje záznam životní události pro každou právnickou osobu, ve které se zaměstnanec nachází. Při zpracování životních událostí musí být vybrána právnická osoba ke zpracování. Logika zpracování se však neomezuje pouze na tuto právnickou osobu. Namísto toho probíhá zpracování pro všechny právnické osoby a jsou zavírány a znovu otevírány plány ve vybrané právnické osobě. Tato akce je životní událost, která se má zpracovat vícekrát ve stejné právnické osobě, což má za následek několikanásobné uzavření / opětovné otevření každého plánu ovlivněného životní událostí. |
| 518064 | Pouze jedna závislá osoba vybraná v plánech splňujících podmínky, když je více než jedna osoba označena jako výchozí pověřená | Opraven problém, kdy v plánech splňujících podmínky nebylo automaticky vybráno více výchozích pověřených osob. Nyní můžete také určit primárního příjemce pro osobní kontakt. Primární příjemce je v plánech splňujících podmínky uveden jako 100%, pokud existuje více příjemců. |
| 552365 | Úlohy exportu dat Použití vlastní databáze (BYOD) po upgradu na Platform update 40 selhávají | Opraven problém, kdy exporty BYOD selhaly po použití Platform update 40 na prostředí. |
| 547123 | Omezení počtu úkolů dotazovaných v seznamu úkolů na řídicím panelu | Počet úkolů zobrazených v seznamu úkolů je nyní omezen na 15, aby se vyřešil problém s výkonem způsobený nadměrným počtem úkolů, které se pokoušejí načíst. |

## <a name="in-preview"></a>Náhled

Verze Preview obsahuje následující nové funkce. Další informace o zapnutí a vypnutí funkcí naleznete v tématu [Správa funkcí](hr-admin-manage-features.md).

| Funkce | Plán vydání | Dokumentace |
| --- | --- | --- |
| Zobrazení pracovního volna manažery napříč společnostmi | [Zobrazení pracovního volna zaměstnanců manažery napříč společnostmi](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Konfigurace parametrů pracovního volna a absence](./hr-leave-and-absence-parameters.md) |
| Pracovní prostor správy zaměstnaneckých výhod | [Pracovní prostor správy zaměstnaneckých výhod (Preview)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Pracovní prostor správy zaměstnaneckých výhod](hr-benefits-management-workspace.md) |
| U zaměstnanců můžete omezit jejich upravování podrobností obchodních kontaktů | [U zaměstnanců můžete omezit jejich upravování podrobností obchodních kontaktů](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [Omezení úpravy osobních údajů](hr-employee-self-service-restrict-editing.md)|

## <a name="coming-soon"></a>Již brzy

| Funkce | Podrobnosti |
| --- | --- |
| Dovednosti zadané manažery pro své zaměstnance lze automaticky schválit pomocí pracovního postupu | Již brzy. |

Úplný seznam plánovaných funkcí a plánovaných verzí najdete v části [Přehled o 1. vlně vydání Dynamics 365 Human Resources v roce 2021](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="terminology-updates-for-microsoft-dataverse"></a>Aktualizace terminologie pro Microsoft Dataverse

S platností od listopadu 2020 byl Common Data Service přejmenován na [Microsoft Dataverse](/powerapps/maker/data-platform/data-platform-intro). Viz [oficiální oznámení](https://powerapps.microsoft.com/blog/reshape-the-future-of-work-with-microsoft-dataverse-for-teams-now-generally-available/) na blogu Power Apps, kde se dozvíte více. S touto změnou názvu byla provedena aktualizace terminologie v Dataverse. Například *entita* je nyní *tabulka* a *pole* je nyní *sloupec*. Další informace viz [aktualizace terminologie](/powerapps/maker/data-platform/data-platform-intro#terminology-updates).

V této verzi byla terminologie související s integrací Dynamics 365 Human Resources s Dataverse v celé aplikaci aktualizována, aby odrážela tyto změny. Například formulář **Integrace Common Data Service** formulář je nyní **Integrace Microsoft Dataverse**.

Chcete-li se dozvědět více o integraci Dynamics 365 Human Resources s Microsoft Dataverse, přečtěte si [Konfigurace integrace Microsoft Dataverse](./hr-admin-integration-common-data-service.md) a [Konfigurace virtuálních tabulek Microsoft Dataverse](./hr-admin-integration-common-data-service-virtual-entities.md).

## <a name="updates-to-service-deployment"></a>Aktualizace nasazení služby

Počínaje vydáním z 22. února 2021 upravujeme nasazení našich aktualizací regionálních služeb. Úpravy budou zahrnovat rotaci pořadí, ve kterém globální regiony dostávají aktualizace pro službu Human Resources, a úpravy v době čekání mezi fázemi aktualizace. Tyto změny lépe ladí s postupy bezpečného nasazení (Safe Deployment Practices - SDP) za účelem zlepšení stability, kvality a podpory služeb.

Budeme i nadále dodržovat dvoutýdenní tempo nasazení. Zákazníci si však mohou všimnout, že aktualizace se obvykle používají v jejich prostředích Human Resources v jiný den dvoutýdenního cyklu než v předchozích vydáních.

Další informace o procesu aktualizaci služby najdete v tématu [Proces aktualizace](./hr-admin-setup-update-process.md).

## <a name="see-also"></a>Viz také

[Co je nového a co se změnilo v Human Resources](hr-admin-whats-new.md)</br>
[Přehled produktu Dynamics 365 Human Resources vydání 2021 vlny 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Aktualizace procesu](hr-admin-setup-update-process.md)</br>
[Správa funkcí](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]