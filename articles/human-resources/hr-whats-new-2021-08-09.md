---
title: Co je nového a co se změnilo v aplikaci Dynamics 365 Human Resources, 9. srpna 2021
description: Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Human Resources k 9. srpnu 2021.
author: marcelbf
ms.date: 08/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-08-09
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 58926e5a6c1476db84fa41945dc92196eb24f4bf
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/29/2022
ms.locfileid: "9068447"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-9-2021"></a>Co je nového a co se změnilo v aplikaci Dynamics 365 Human Resources, 9. srpna 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tento článek popisuje funkce, které jsou nové, změnily se nebo se brzy objeví v aplikaci Microsoft Dynamics 365 Human Resources.

Další informace o našem procesu aktualizaci a plánu najdete v tématu [Proces aktualizace](hr-admin-setup-update-process.md).

Další informace o nových funkcích a jejich očekávaných obecných datech dostupnosti najdete v tématu [Přehled 2. vlny vydání Dynamics 365 Human Resources v roce 2021](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>V této vydané verzi

Tato verze obsahuje následující nové funkce a opravené chyby. Změny se vztahují na sestavení číslo 8.1.4393.

### <a name="bug-fixes"></a>Opravy chyb

Tato verze obsahuje následující opravy chyb.

> [!NOTE]
> Naším cílem dostat k vám tyto informace co nejdříve. Tento článek můžeme aktualizovat, aby obsahovalo opravy chyb, které se dostaly do sestavení poté, co byl tento článek původně publikován.

| Číslo problému | Problém | Popis |
| --- | --- | --- |
| 558385 | Výchozí pověřená osoba není vybrána, když je možnost **Automatický výběr pověřených osob** zapnutá u výchozích návrhů. | Tento problém je nyní vyřešen. U plánů splňujících podmínky se automaticky vybere více výchozích pověřených osob, když je zapnutá možnost **Automatický výběr pověřených osob** na stránce **Sdílené parametry lidských zdrojů**. |
| 589617 | Na stránce **Volno** jsou zůstatky **K dispozici ke koupi** a **K dispozici k prodeji** prázdné, pokud je přístup omezen na konkrétní společnost. | Tento problém je nyní vyřešen. Stránka **Volno** ukazuje správné zůstatky **K dispozici ke koupi** a **K dispozici k prodeji**, pokud je uživatel omezen na konkrétní společnost. |

## <a name="in-preview"></a>Náhled

Verze Preview obsahuje následující nové funkce. Další informace o zapnutí a vypnutí funkcí naleznete v tématu [Správa funkcí](hr-admin-manage-features.md).

| Funkce | Plán vydání | Dokumentace |
| --- | --- | --- |
| Pracovní prostor správy zaměstnaneckých výhod | [Pracovní prostor správy zaměstnaneckých výhod (Preview)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Pracovní prostor správy zaměstnaneckých výhod](hr-benefits-management-workspace.md) |
| Povolit zjednodušenou integraci mezd (API pro integraci mezd) | [Povolení zjednodušených integrací s poskytovateli mezd](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Rozhraní API integrace mezd](hr-admin-integration-payroll-api-introduction.md)|
| Povolit správci nepřítomnosti správu dovolené | [Povolit správci nepřítomnosti správu dovolené](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | V této verzi aktualizujeme zobrazení pracovního prostoru správce nepřítomnosti. Další informace naleznete v tématu [Konfigurace role správce nepřítomnosti](https://go.microsoft.com/fwlink/?linkid=2168107). |
| Nakonfigurujte požadovanou přílohu podle typu dovolené | [Nakonfigurujte požadovanou přílohu podle typu dovolené](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) |[Konfigurace typů pracovního volna a absence](https://go.microsoft.com/fwlink/?linkid=2168108)|
| Nakonfigurovat jednotky pracovního volna podle typu pracovního volna | [Nakonfigurovat jednotky pracovního volna podle typu pracovního volna](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) |[Konfigurace typů pracovního volna a absence](https://go.microsoft.com/fwlink/?linkid=2168215)|
| Umožněte zaměstnancům, aby byli označeni jako připraveni k výplatě | [Umožněte zaměstnancům, aby byli označeni jako připraveni k výplatě](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Připraveno k platbě](/dynamics365/human-resources/hr-compensation-payroll) |

## <a name="coming-soon"></a>Již brzy

Úplný seznam plánovaných funkcí a plánovaných verzí najdete v části [Přehled o 2. vlně vydání Dynamics 365 Human Resources v roce 2021](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

| Funkce | Podrobnosti |
| --- | --- |
| Platform update 10.0.21 (45) | Vydání aktualizace platformy 10.0.21 je naplánováno spolu se servisním vydáním 4. října 2021. Další informace naleznete v tématu [Aktualizace platformy pro verze 10.0.21 finančních a provozních aplikací (říjen 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21). |

## <a name="see-also"></a>Viz také

[Co je nového a co se změnilo v aplikaci Human Resources](hr-admin-whats-new.md)</br>
[Přehled produktu Dynamics 365 Human Resources vydání 2021 vlny 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Aktualizace procesu](hr-admin-setup-update-process.md)</br>
[Správa funkcí](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

