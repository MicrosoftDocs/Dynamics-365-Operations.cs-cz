---
title: Co je nového nebo změněného v aplikaci Dynamics 365 Human Resources, 20. května 2021
description: Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Human Resources k 20. květnu 2021.
author: marcelbf
ms.date: 05/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-05-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3a399e1c7ccbd85b58286ec4f3d294f80332c3fd
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8891285"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-20-2021"></a>Co je nového nebo změněného v aplikaci Dynamics 365 Human Resources, 20. května 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tento článek popisuje funkce, které jsou nové, změnily se nebo brzy dorazí do aplikace Dynamics 365 Human Resources.

Další informace o našem procesu aktualizaci a plánu najdete v tématu [Proces aktualizace](hr-admin-setup-update-process.md).

Další informace o nových funkcích a jejich očekávaných obecných datech dostupnosti najdete v tématu [Přehled 1. vlny vydání Dynamics 365 Human Resources v roce 2021](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>V této vydané verzi

Tato verze obsahuje následující nové funkce a opravené chyby. Změny se vztahují na sestavení číslo 8.1.4189.

### <a name="new-features"></a>Nové funkce

V této verzi jsou všeobecně dostupné následující funkce.

| Funkce | Plán vydání | Dokumentace |
| --- | --- | --- |
| Platform update 10.0.18 (42) | -- | [Aktualizace platformy pro verze 10.0.18 finančních a provozních aplikací (květen 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-18) |
| Aplikace Human Resources pro Microsoft Teams nyní podporuje definice půldnů a schopnost rozdělit den | -- | [Správa žádostí o dovolenou v aplikaci Teams](/dynamics365/human-resources/hr-teams-leave-app#create-a-new-request) |

### <a name="bug-fixes"></a>Opravy chyb

Tato verze obsahuje následující opravy chyb.

> [!NOTE]
> Naším cílem dostat k vám tyto informace co nejdříve. Tento článek můžeme aktualizovat, aby obsahovalo opravy chyb, které se dostaly do sestavení poté, co byl tento článek původně publikován.

| Číslo problému | Problém |  Popis |
| --- | --- | --- |
| 583776 | Hromadné registrace zaměstnanců do plánů dovolené způsobují chybu duplicitního záznamu | Tato chyba byla opravena v nejnovější verzi a registrace hromadného volného plánu by měly být úspěšně zpracovány. |
| 582263 | Nelze spustit zpracování životních událostí pro všechny pracovníky najednou | Když je pole **Pracovník** ponecháno prázdné pro zpracování životních událostí, budou zpracováni všichni pracovníci. |
| 558383 | Primární příjemce není označen jako 100%, pokud není vybrán výchozí zástupce | Chyba byla opravena, takže uživatel musí pouze přepínat výběr primárního příjemce.|
| 509404 | Analýza počtu zaměstnanců oddělení nezohledňuje pohyb zaměstnanců mezi odděleními |Analýzy byly aktualizovány tak, aby zahrnovaly převody zaměstnanců mezi odděleními|
| 579420 | Funkce zmrazení sloupců v mřížkách by zatím neměla být k dispozici | Funkce **Zmrazení sloupců v mřížkách**, která není k dispozici v Human Resources, byla uvedena jako dostupná ve Správě funkcí. Funkce byla odstraněna ze seznamu funkcí, které chcete povolit. |

## <a name="in-preview"></a>Náhled

Verze Preview obsahuje následující nové funkce. Další informace o zapnutí a vypnutí funkcí naleznete v tématu [Správa funkcí](hr-admin-manage-features.md).

| Funkce | Plán vydání | Dokumentace |
| --- | --- | --- |
| Podpora vlastních polí v pravidlech nároku ve správě výhod | [Vlastní podpora pole pro zpracování způsobilosti](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |[Konfigurace pravidel způsobilosti](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules) |
| Pracovní prostor správy zaměstnaneckých výhod | [Pracovní prostor správy zaměstnaneckých výhod (Preview)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Pracovní prostor správy zaměstnaneckých výhod](hr-benefits-management-workspace.md) |
| Vylepšení workflowu s odchodem a nepřítomností | [Vylepšení workflowu s odchodem a nepřítomností](https://go.microsoft.com/fwlink/?linkid=2147528) | [Požádat o volno](hr-employee-self-service-request-time-off.md)|
| Povolit zjednodušenou integraci mezd (API pro integraci mezd) | [Povolení zjednodušených integrací s poskytovateli mezd](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Rozhraní API integrace mezd](hr-admin-integration-payroll-api-introduction.md)|
| Audit transakce časového rozlišení pracovního volna | - | [Audit transakce časového rozlišení pracovního volna](hr-leave-and-absence-accrue.md)|

## <a name="coming-soon"></a>Již brzy

| Funkce | Podrobnosti |
| --- | --- |
|  Povolit správci nepřítomnosti správu dovolené | [Povolit správci nepřítomnosti správu dovolené](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) |

Úplný seznam plánovaných funkcí a plánovaných verzí najdete v části [Přehled o 1. vlně vydání Dynamics 365 Human Resources v roce 2021](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Viz také

[Co je nového a co se změnilo v Human Resources](hr-admin-whats-new.md)</br>
[Přehled produktu Dynamics 365 Human Resources vydání 2021 vlny 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Aktualizace procesu](hr-admin-setup-update-process.md)</br>
[Správa funkcí](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
