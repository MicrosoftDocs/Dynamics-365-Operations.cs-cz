---
title: Co je nového a co se změnilo v aplikaci Dynamics 365 Human Resources (5. října 2021)
description: Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Human Resources k 5. říjnu 2021.
author: marcelbf
ms.date: 10/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ba24afd16a471abb36a6f7bc9a8610acec374190
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/29/2022
ms.locfileid: "9067964"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-october-5-2021"></a>Co je nového a co se změnilo v aplikaci Dynamics 365 Human Resources (5. října 2021)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tento článek popisuje funkce, které jsou nové, změnily se nebo se brzy objeví v aplikaci Microsoft Dynamics 365 Human Resources.

Další informace o našem procesu aktualizaci a plánu najdete v tématu [Proces aktualizace](hr-admin-setup-update-process.md).

Další informace o nových funkcích a jejich očekávaných obecných datech dostupnosti najdete v tématu [Přehled 2. vlny vydání Dynamics 365 Human Resources v roce 2021](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>V této vydané verzi

Tato verze obsahuje následující nové funkce a opravené chyby. Změny se vztahují na sestavení číslo 8.1.4485.

### <a name="new-features"></a>Nové funkce

V této verzi jsou všeobecně dostupné následující funkce.

| Funkce | Plán vydání | Dokumentace |
|---|---|---|
| Platform update 10.0.21 (45) | -- | [Aktualizace platformy pro verze 10.0.21 finančních a provozních aplikací (říjen 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21) |


### <a name="bug-fixes"></a>Opravy chyb

Tato verze obsahuje následující opravy chyb.

> [!NOTE]
> Naším cílem dostat k vám tyto informace co nejdříve. Tento článek můžeme aktualizovat, aby obsahovalo opravy chyb, které se dostaly do sestavení poté, co byl tento článek původně publikován.

| Číslo problému | Problém | Popis |
|---|---|---|
| 598896 | Částka zaměstnance se zobrazí až poté, co zaměstnanec dokončí registraci | Na stránce **Samoobsluha zaměstnanců** se částka zaměstnance za zaměstnaneckou výhodu se nezobrazila. Částka zaměstnance se nyní zobrazuje na stránce **Samoobsluha zaměstnaneckých výhod**.  |
| 613440 | Nelze exportovat data z části **Správa dat** | Při exportu dat pro projekt v části **Správa dat** se export neočekávaně nezdaří. |
| 618327 | Uzavřená a budoucí období jsou zobrazena na stránce **Parametry sestavy** výkazu výhod | Při přechodu na **Výkaz výhod** v **Samoobsluze zaměstnanců** stránka **Parametry sestavy** zobrazí záložky **Záznamy k zahrnutí** a **Spustit na pozadí**. Tyto sekce byly odstraněny.|
| 618326 | Zobrazí se nesprávná stránka **Parametry hlášení** v **Samoobsluze zaměstnanců** pro výkaz zaměstnaneckých výhod.| Při přechodu na cílovou stránku **Sestava výkazu výhod** si uživatel mohl vybrat období plánů výhod, které jsou uzavřeny nebo jsou datovány do budoucna, což má za následek zobrazení prázdné stránky. V seznamu by se mělo zobrazit pouze aktuální období plánu výhod. |

## <a name="in-preview"></a>Náhled

Verze Preview obsahuje následující nové funkce. Další informace o zapnutí a vypnutí funkcí naleznete v tématu [Správa funkcí](hr-admin-manage-features.md).

| Funkce | Plán vydání | Dokumentace |
|---|---|---|
| Pracovní prostor správy zaměstnaneckých výhod | [Pracovní prostor správy zaměstnaneckých výhod (Preview)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Pracovní prostor správy zaměstnaneckých výhod](hr-benefits-management-workspace.md) |
| Vlastní pole ve Způsobilosti |[Podpora vlastních polí ve zpracování způsobilosti](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-benefits-management) | [Použití vlastních polí ve zpracování způsobilosti](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules#using-custom-fields-in-eligibility-rules) |
| Výkaz zaměstnaneckých výhod |[Výkaz zaměstnaneckých výhod](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/benefits-summary-statement) | [Výkaz zaměstnaneckých výhod](hr-benefits-statement.md) |

### <a name="benefits-statement-known-issues"></a>Známé problémy u výkazu zaměstnaneckých výhod

| Problém | Popis |
|---|---|
|Chyba při odesílání sestavy e-mailem pomocí **cíle sestavy GER**. | Výkaz výhod lze nastavit tak, aby používal parametry e-mailu v rámci stránky **Cíle sestavy GER**. Po dokončení nastavení a tisku sestavy se uživateli zobrazí chyba formátování a výkaz výhod nebude odeslán.|

## <a name="feature-management-changes"></a>Změny správy funkcí

| Funkce | Popis |
|---|---|
|Zobrazení rozšířených sestav deníků výkonu | Tato funkce bude v tomto vydání ve výchozím nastavení povolena. |

## <a name="coming-soon"></a>Již brzy

Úplný seznam plánovaných funkcí a plánovaných verzí najdete v části [Přehled o 2. vlně vydání Dynamics 365 Human Resources v roce 2021](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

| Funkce | Podrobnosti |
|---|---|
| Platform update 10.0.22 (46) | Vydání aktualizace platformy 10.0.22 je naplánováno spolu se servisním vydáním 1. listopad 2021. Další informace naleznete v tématu [Aktualizace platformy pro verze 10.0.22 finančních a provozních aplikací (listopad 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-22). |



## <a name="see-also"></a>Viz také

[Co je nového a co se změnilo v aplikaci Human Resources](hr-admin-whats-new.md)</br>
[Přehled produktu Dynamics 365 Human Resources vydání 2021 vlny 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Aktualizace procesu](hr-admin-setup-update-process.md)</br>
[Správa funkcí](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

