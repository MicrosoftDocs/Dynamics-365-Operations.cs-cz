---
title: Co je nového nebo změněného v aplikaci Dynamics 365 Human Resources, 3. května 2021
description: Tohle téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Human Resources k 3. květnu 2021.
author: marcelbf
ms.date: 05/03/2021
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
ms.search.validFrom: 2021-05-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8cee60750d3c451024466109acbdc5924074a11f
ms.sourcegitcommit: baad2723291774f610324a8054fc14abf3287fe1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/14/2021
ms.locfileid: "6559953"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-3-2021"></a>Co je nového nebo změněného v aplikaci Dynamics 365 Human Resources, 3. května 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tohle téma popisuje funkce, které jsou nové, byly změněny nebo se brzy objeví v aplikaci Dynamics 365 Human Resources.

Další informace o našem procesu aktualizaci a plánu najdete v tématu [Proces aktualizace](hr-admin-setup-update-process.md).

Další informace o nových funkcích a jejich očekávaných obecných datech dostupnosti najdete v tématu [Přehled 1. vlny vydání Dynamics 365 Human Resources v roce 2021](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>V této vydané verzi

Tato verze obsahuje následující nové funkce a opravené chyby. Změny se vztahují na sestavení číslo 8.1.4140.

### <a name="new-features"></a>Nové funkce

V této verzi jsou všeobecně dostupné následující funkce.

| Funkce | Plán vydání | Dokumentace |
| --- | --- | --- |
| Přidejte informační lištu při vytváření životních událostí. | - | Když vytvoříte životní událost, na informačním panelu se zobrazí zpráva označující typ vytvořené životní události.

### <a name="bug-fixes"></a>Opravy chyb

Tato verze obsahuje následující opravy chyb.

> [!NOTE]
> Naším cílem dostat k vám tyto informace co nejdříve. Tohle téma můžeme aktualizovat, aby obsahovalo opravy chyb, které se dostaly do sestavení poté, co bylo toto téma původně publikováno.

| Číslo problému | Výdej |  popis |
| --- | --- | --- |
| 559312 |  Úroveň se nezobrazuje při vytváření plánu pevné odměny pro zaměstnance. |  Když existuje neshoda časového pásma mezi časovým pásmem uživatele a časovým pásmem společnosti, úroveň kompenzace v úloze se nepodařilo přečíst. Dotaz byl aktualizován, aby se načetl na základě času UTC. |
| 573676  | Nelze přidat nové období do formuláře **Plán výhod** . | Formulář byl aktualizován tak, aby tlačítko **Nový** bylo povoleno na pevné záložce **Doba** v **Plánech výhod**. |

## <a name="in-preview"></a>Náhled

Verze Preview obsahuje následující nové funkce. Další informace o zapnutí a vypnutí funkcí naleznete v tématu [Správa funkcí](hr-admin-manage-features.md).

| Funkce | Plán vydání | Dokumentace |
| --- | --- | --- |
| Pracovní prostor správy zaměstnaneckých výhod | [Pracovní prostor správy zaměstnaneckých výhod (Preview)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Pracovní prostor správy zaměstnaneckých výhod](hr-benefits-management-workspace.md) |
| Vylepšení workflowu s odchodem a nepřítomností | [Vylepšení workflowu s odchodem a nepřítomností](https://go.microsoft.com/fwlink/?linkid=2147528) | [Požádat o volno](hr-employee-self-service-request-time-off.md)|
| Povolit zjednodušenou integraci mezd (API pro integraci mezd) | [Povolení zjednodušených integrací s poskytovateli mezd](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Rozhraní API integrace mezd](hr-admin-integration-payroll-api-introduction.md)|
| Audit transakce časového rozlišení pracovního volna | - | [Audit transakce časového rozlišení pracovního volna](hr-leave-and-absence-accrue.md)|

## <a name="coming-soon"></a>Již brzy

| Funkce | Podrobnosti |
| --- | --- |
| Platform update 10.0.18 (42) | Aktualizace platformy 10.0.18 je naplánována na zavedení se servisním vydáním 17. května 2021. Další informace naleznete v části [Aktualizace platformy pro verze 10.0.18 aplikací Finance and Operations (květen 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-18). |
| Podpora vlastních polí v pravidlech nároku ve správě výhod  | [Vlastní podpora pole pro zpracování způsobilosti](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |

Úplný seznam plánovaných funkcí a plánovaných verzí najdete v části [Přehled o 1. vlně vydání Dynamics 365 Human Resources v roce 2021](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Viz také

[Co je nového a co se změnilo v Human Resources](hr-admin-whats-new.md)</br>
[Přehled produktu Dynamics 365 Human Resources vydání 2021 vlny 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Aktualizace procesu](hr-admin-setup-update-process.md)</br>
[Správa funkcí](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
