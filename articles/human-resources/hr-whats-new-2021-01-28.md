---
title: Co je nového nebo změněného v aplikaci Dynamics 365 Human Resources 28 leden 2021
description: Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Human Resources k 28. lednu 2021.
author: marcelbf
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 46bbda21c3eb2b32030b93afc2a40785c22b124e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909752"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-january-28-2021"></a>Co je nového nebo změněného v aplikaci Dynamics 365 Human Resources 28 leden 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tento článek popisuje funkce, které jsou nové, změnily se nebo brzy dorazí do aplikace Dynamics 365 Human Resources.

Další informace o našem procesu aktualizaci a plánu najdete v tématu [Proces aktualizace](hr-admin-setup-update-process.md).

Další informace o nových funkcích a jejich očekávaných obecných datech dostupnosti najdete v tématu [Přehled 1. vlny vydání Dynamics 365 Human Resources v roce 2021](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>V této vydané verzi

Tato verze obsahuje následující nové funkce a opravené chyby. Změny se vztahují na sestavení číslo 8.1.3906.

### <a name="new-features"></a>Nové funkce

V této verzi jsou všeobecně dostupné následující funkce.

| Funkce | Plán vydání | Dokumentace |
| --- | --- | --- |
| Integrace kódů důvodů zaměstnaneckých výhod s pracovním prostorem **Správa zaměstnanců** | -- | [Nastavení kódů důvodů](hr-benefits-setup-reason-codes.md) |

### <a name="bug-fixes"></a>Opravy chyb

Tato verze obsahuje následující opravy chyb.

> [!NOTE]
> Naším cílem dostat k vám tyto informace co nejdříve. Tento článek můžeme aktualizovat, aby obsahovalo opravy chyb, které se dostaly do sestavení poté, co byl tento článek původně publikován.


| Číslo problému | Problém |  Popis |
| --- | --- | --- |
| 539456 | Kalendář zobrazuje text typ dovolené při najetí myši, pokud je povolený parametr **Zobrazit pouze nepřítomnost bez podrobností**. | Když jepovolena možost **Zobrazit pouze nepřítomnost bez podrobností**, datum požadavku se nyní zobrazí při najetí myší. |
| 528907 | Udělení přístupu právnické osobě k roli zaměstnance vede k tomu, že manažeři nebudou moci vidět aktivitu zůstatku dovolené pro zaměstnance v oblasti **Můj tým** samoobsluhy zaměstnanců. |Nastavení této možnosti nyní umožňuje manažerům nadále vidět aktivitu zůstatku dovolené. |
| 526280 | Chyba oprávnění u HcmWorkerEntity, HcmEmployeeEntity a HcmContractorEntity. | Uživatelé v roli jiného než systémového správce nebyli schopni exportovat entity uvedené v seznamu kvůli chybě oprávnění v poli NationalityCountryRegion. Uživatelé budou i nadále potřebovat následující oprávnění k exportu těchto informací: HcmWorkerEntityMaintain, HcmWorkerEntityView, HcmEmployeeEntityMaintain, HcmEmployeeEntityMaintain, HcmEmployeeEntityView, HcmContractorEntityMaintain a HCMContractorEntityView. |
| 542147 | Pole **Číslo bankovního účtu** a **Směrový kód banky** jsou povinná při přidávání bankovního účtu prostřednictvím samoobslužné služby pro zaměstnance. | Opravili jsme chybu, kdy byli zaměstnanci povinni vyplnit pole **Číslo bankovního účtu** a **Směrový kód banky** při zadávání údajů o bankovním účtu. Tato pole již nejsou povinná při ukládání informací o novém bankovním účtu. |
| 543641 | PSČ se při elektronickém hlášení neuvádí. | Opravená chyba, kdy se PSČ ve zprávě ACA nenacházelo pro kódy pokrytí L až Q. |
| 545402 | Přidejte změnu směrování pro soubor UserBranding.js a odstraňte chyby 404. | Uživatel by již neměl v konzoli vidět chyby 404. |

## <a name="in-preview"></a>Náhled   

Verze Preview obsahuje následující nové funkce. Další informace o zapnutí a vypnutí funkcí naleznete v tématu [Správa funkcí](hr-admin-manage-features.md).

| Funkce | Plán vydání | Dokumentace |
| --- | --- | --- |
| Aplikace Human Resources v Microsoft Teams | [Dovolená a nepřítomnost zaměstnanců v Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Aplikace Human Resources v Teams](./hr-admin-teams-leave-app.md)<br>[Správa žádostí o dovolenou v aplikaci Teams](hr-teams-leave-app.md) |
| Zobrazení pracovního volna manažery napříč společnostmi | [Zobrazení pracovního volna zaměstnanců manažery napříč společnostmi](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Konfigurace parametrů pracovního volna a absence](./hr-leave-and-absence-parameters.md) |

## <a name="coming-soon"></a>Již brzy

| Funkce | Podrobnosti |
| --- | --- |
| E-mailové potvrzení pro registrace zaměstnaneckých výhod | Tato funkce zajistí možnost odeslat zaměstnancům potvrzovací e-mail, když se registrují k zaměstnaneckým výhodám v samoobsluze pro zaměstnance. Tato funkce bude k dispozici 1. února. Další informace viz [Konfigurace parametrů správy zaměstnaneckých výhod podle společnosti](hr-benefits-setup-parameters-per-company.md). |
| Dovednosti zadané manažery pro své zaměstnance lze automaticky schválit pomocí pracovního postupu | Již brzy. |

Úplný seznam plánovaných funkcí a plánovaných verzí najdete v části [Přehled o 1. vlně vydání Dynamics 365 Human Resources v roce 2021](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="terminology-updates-for-microsoft-dataverse"></a>Aktualizace terminologie pro Microsoft Dataverse

S platností od listopadu 2020 byl Common Data Service přejmenován na [Microsoft Dataverse](/powerapps/maker/data-platform/data-platform-intro). Viz [oficiální oznámení](https://powerapps.microsoft.com/blog/reshape-the-future-of-work-with-microsoft-dataverse-for-teams-now-generally-available/) na blogu Power Apps, kde se dozvíte více. V souvislosti s touto změnou názvu byla provedena aktualizace terminologie v Dataverse. Například *entita* je nyní *tabulka* a *pole* je nyní *sloupec*. Další informace viz [aktualizace terminologie](/powerapps/maker/data-platform/data-platform-intro#terminology-updates).

V této verzi byla terminologie související s integrací Dynamics 365 Human Resources s Dataverse v celé aplikaci aktualizována, aby odrážela tyto změny. Například formulář **Integrace Common Data Service** formulář je nyní **Integrace Microsoft Dataverse**.

Chcete-li se dozvědět více o integraci Dynamics 365 Human Resources s Microsoft Dataverse, přečtěte si [Konfigurace integrace Microsoft Dataverse](./hr-admin-integration-common-data-service.md) a [Konfigurace virtuálních tabulek Microsoft Dataverse](./hr-admin-integration-common-data-service-virtual-entities.md).

## <a name="see-also"></a>Viz také

[Co je nového a co se změnilo v Human Resources](hr-admin-whats-new.md)</br>
[Přehled produktu Dynamics 365 Human Resources vydání 2021 vlny 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Aktualizace procesu](hr-admin-setup-update-process.md)</br>
[Správa funkcí](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]