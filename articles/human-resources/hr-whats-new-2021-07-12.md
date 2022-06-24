---
title: Co je nového nebo co se změnilo v aplikaci Dynamics 365 Human Resources 12. července 2021
description: Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Human Resources k 12. červenci 2021.
author: marcelbf
ms.date: 07/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-07-12
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 259004773c4e5a7d8865d563da9bcfea3a116632
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870951"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-12-2021"></a>Co je nového nebo co se změnilo v aplikaci Dynamics 365 Human Resources 12. července 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tento článek popisuje funkce, které jsou nové, změnily se nebo brzy dorazí do aplikace Dynamics 365 Human Resources.

Další informace o našem procesu aktualizaci a plánu najdete v tématu [Proces aktualizace](hr-admin-setup-update-process.md).

Další informace o nových funkcích a jejich očekávaných obecných datech dostupnosti najdete v tématu [Přehled 1. vlny vydání Dynamics 365 Human Resources v roce 2021](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>V této vydané verzi

Tato verze obsahuje následující nové funkce a opravené chyby. Změny se vztahují na sestavení číslo 8.1.4353.

### <a name="new-features"></a>Nové funkce

V této verzi jsou všeobecně dostupné následující funkce.

| Funkce | Plán vydání | Dokumentace |
| --- | --- | --- |
|  Přepínání zobrazení počtu let ve společnosti | |Tato funkce poskytuje možnost použít různá data k výpočtu let služby ve společnosti zobrazených na stránce **Zjednodušené zadávání zaměstnance** a na stránce **Lidé**.  To bude k dispozici v [parametrech Human Resources](/dynamics365/human-resources/hr-setup-parameters). |


### <a name="bug-fixes"></a>Opravy chyb

Tato verze obsahuje následující opravy chyb.

> [!NOTE]
> Naším cílem dostat k vám tyto informace co nejdříve. Tento článek můžeme aktualizovat, aby obsahovalo opravy chyb, které se dostaly do sestavení poté, co byl tento článek původně publikován.

| Číslo problému | Problém |  Popis |
| --- | --- | --- |
| 595871 | Podokno Informace v Human Resources obsahuje nesprávnou terminologii Dataverse | S rebrandingem Common Data Service na Dataverse byla aktualizována terminologie v informačním podokně Microsoft Dynamics 365 Human Resources (**Nápověda a podpora > O aplikaci**). |
| 598676 | Zjednodušený formulář pro přepsání vstupu zaměstnance může při použití se uloženým pohledem vytvořit chybu| Na stránce **Pracovník**, pokud je zapnuta funkce „Zjednodušený vstup zaměstnanců“, aplikace může selhat, pokud je možnost **Vždy otevřené pro úpravy** nastavena na uložené zobrazení. |
| 592344 |Sekce kompenzace pracovníků na pozici by měla být načtena, pouze pokud je povolena správa výhod | Informace o kompenzaci pracovníků se vytvářejí pomocí funkce starších výhod.  Když je povolena správa výhod, pole budou pouze pro čtení. Když je zapnuta správa výhod a možnost **Skrýt starší formuláře výhod** je nastavena na **Ano** v sdílených parametrech HR, karta **Kompenzace pracovníků** bude skryta. |
| 598617 | Aktivační karta formuláře **HcmDiscussion** způsobí nekonečnou smyčku, když se použijí personalizace | Když má mřížka i zobrazení podrobností zapnutou možnost **Vždy otevřené pro úpravy**, kód aktivující kartu v metodě přepsané úlohy je v konfliktu s personalizací o tom, jaký ovládací prvek by měl mít fokus, a vytváří nekonečnou smyčku. |
| 593553 | Pole Datum deníku v deníku výkonu se zobrazuje v UTC | Pole **Datum deníku** pro deníky výkonu se zobrazuje v časovém pásmu UTC, nikoli v časovém pásmu definovaném v nastavení systémového data, což u některých časových pásem způsobuje nesprávné datum. |
| 586930 | Otevření aktivit pro výkonnostní cíle otevírá úplně jiný záznam | Když je ve Správě funkcí povolena funkce „Zobrazení rozšířených přehledů výkonnostních deníků", výběr výkonnostních cílů pro rozšířené zprávy na kartě **Můj tým** v **Samoobsluze zaměstnanců** otevře cíle pro zaměstnance namísto vybraného zaměstnance. |
| 569959 |  Entita HcmPositionWorkerAssignmentV2 nepřiděluje pracovníka na pozici | Uživatelé obdrželi chybu při přidávání záznamu přiřazení polohy prostřednictvím entity a publikování se nezdařilo. |
| 582259 | Zpráva VETS 4212 používá místo formuláře 2020 formulář 2017 | Aktualizováno na formát 2020.  Chcete-li načíst nový formát, přejděte na **Konfigurace sestavy** a odstraňte přehled VETS-4212 v levém sloupci. Přejděte na **Elektronické hlášení - Úložiště - HR zdroje** a vyberte **Otevřít**.  Vyberte **Tisk PDF VETS-4212** a poté vyberte **Import**.|


## <a name="in-preview"></a>Náhled

Verze Preview obsahuje následující nové funkce. Další informace o zapnutí a vypnutí funkcí naleznete v tématu [Správa funkcí](hr-admin-manage-features.md).

| Funkce | Plán vydání | Dokumentace |
| --- | --- | --- |
| Pracovní prostor správy zaměstnaneckých výhod | [Pracovní prostor správy zaměstnaneckých výhod (Preview)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Pracovní prostor správy zaměstnaneckých výhod](hr-benefits-management-workspace.md) |
| Povolit zjednodušenou integraci mezd (API pro integraci mezd) | [Povolení zjednodušených integrací s poskytovateli mezd](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Rozhraní API integrace mezd](hr-admin-integration-payroll-api-introduction.md)|
|  Povolit správci nepřítomnosti správu dovolené | [Povolit správci nepřítomnosti správu dovolené](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | [Nakonfigurujte roli správce nepřítomnosti](https://go.microsoft.com/fwlink/?linkid=2168107)|
|  Nakonfigurujte požadovanou přílohu podle typu dovolené | [Nakonfigurujte požadovanou přílohu podle typu dovolené](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) |[Konfigurace typů pracovního volna a absence](https://go.microsoft.com/fwlink/?linkid=2168108)|
|  Nakonfigurovat jednotky pracovního volna podle typu pracovního volna | [Nakonfigurovat jednotky pracovního volna podle typu pracovního volna](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) |[Konfigurace typů pracovního volna a absence](https://go.microsoft.com/fwlink/?linkid=2168215)|
| Umožněte zaměstnancům, aby byli označeni jako připraveni k výplatě | [Umožněte zaměstnancům, aby byli označeni jako připraveni k výplatě](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Připraveno k platbě](/dynamics365/human-resources/hr-compensation-payroll) |

## <a name="coming-soon"></a>Již brzy

| Funkce | Podrobnosti |
| --- | --- |
| Platform update 10.0.20 (44) | Aktualizace platformy 10.0.20 je naplánována na zavedení se servisním vydáním 26. července 2021. Další informace naleznete v tématu [Aktualizace platformy pro verze 10.0.20 finančních a provozních aplikací (srpen 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-20). |

Úplný seznam plánovaných funkcí a plánovaných verzí najdete v části [Přehled o 1. vlně vydání Dynamics 365 Human Resources v roce 2021](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Viz také

[Co je nového a co se změnilo v Human Resources](hr-admin-whats-new.md)</br>
[Přehled produktu Dynamics 365 Human Resources vydání 2021 vlny 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Aktualizace procesu](hr-admin-setup-update-process.md)</br>
[Správa funkcí](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
