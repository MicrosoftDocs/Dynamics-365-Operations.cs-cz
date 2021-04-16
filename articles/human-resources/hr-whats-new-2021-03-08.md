---
title: Co je nového nebo změněného v aplikaci Dynamics 365 Human Resources, 8. března 2021
description: Tohle téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Human Resources k 8. březnu 2021.
author: marcelbf
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7029f1dab1f10c2b237fafb7b5d8eeff9fa7a543
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5790277"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-08-2021"></a>Co je nového nebo změněného v aplikaci Dynamics 365 Human Resources, 08. března 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tohle téma popisuje funkce, které jsou nové, byly změněny nebo se brzy objeví v aplikaci Dynamics 365 Human Resources.

Další informace o našem procesu aktualizaci a plánu najdete v tématu [Proces aktualizace](hr-admin-setup-update-process.md).

Další informace o nových funkcích a jejich očekávaných obecných datech dostupnosti najdete v tématu [Přehled 1. vlny vydání Dynamics 365 Human Resources v roce 2021](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>V této vydané verzi

Tato verze obsahuje následující nové funkce a opravené chyby. Změny se vztahují na sestavení číslo 8.1.4017.

### <a name="new-features"></a>Nové funkce

V této verzi jsou všeobecně dostupné následující funkce.

| Funkce | Plán vydání | Dokumentace |
| --- | --- | --- |
| Zobrazení pracovního volna manažery napříč společnostmi | [Zobrazení pracovního volna zaměstnanců manažery napříč společnostmi](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Konfigurace parametrů pracovního volna a absence](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-parameters) |

### <a name="bug-fixes"></a>Opravy chyb

Tato verze obsahuje následující opravy chyb.

> [!NOTE]
> Naším cílem dostat k vám tyto informace co nejdříve. Tohle téma můžeme aktualizovat, aby obsahovalo opravy chyb, které se dostaly do sestavení poté, co bylo toto téma původně publikováno.

| Číslo problému | Výdej |  popis |
| --- | --- | --- |
| 486611 | Volno je zobrazeno v kalendáři pracovního volna, když je povolena možnost **Zakázat volno ve všech kalendářích** | Když je povolena možnost **Zakázat volno ve všech kalendářích**, informace o volnu se nezobrazují, když je povolena funkce vylepšení kalendáře volna a nepřítomnosti.|
| 508972 | U entity Transakce fondu pracovního volna a absence chybí ověření registrace | Při použití entity Transakce fondu pracovního volna a absence již nelze importovat zaměstnance, kteří nejsou zaregistrováni do plánu. |
| 554854 | Aktualizace kalendáře v entitě Zaměstnání skončí chybou, pokud je výchozí Právní entita v možnostech uživatele jiná | Použití entity Zaměstnání k aktualizaci kalendáře zaměstnance již nekončí chybou, pokud se výchozí právnická osoba v možnostech uživatele liší. |
| 558347 | Při načítání úvodní stránky se zobrazí zpráva „Nelze vytvořit záznam v konfiguracích formulářů (FormRunConfiguration)“. | Individuální nastavení způsobí chybu „Nelze vytvořit záznam v konfiguracích formulářů (FormRunConfiguration)“, která se zobrazí při načítání úvodní stránky. |
| 557327 | Pracovní prostor správy zaměstnaneckých výhod: Nad mřížkou se objeví mezera. | Opraven problém zkušenosti uživatelů s nezamýšlenou mezerou, která se objevila na okrajích mřížky tabulky v pracovním prostoru zaměstnaneckých výhod. |
| 557334 | Pracovní prostor správy zaměstnaneckých výhod: rozevírací seznam pro výběr **Období** by se měl zobrazit pouze na kartě **Souhrn** | Rozbalovací nabídka pro výběr **Období** v prostoru výhod se nyní zobrazí pouze v případě, kdy karta **Souhrn** je aktivní v pracovním prostoru Výhody, nikoli v částech **Zpracovat výsledky** a **Odkazy**. |
| 557336 | Pracovní prostor správy zaměstnaneckých výhod: text **Otevřít registraci s rezervovanými plány** je v zobrazení dlaždic zkrácen | Text v zobrazení dlaždic byl změněn na **Rezervované plány ... otevřít registraci**, aby nedošlo k oříznutí nezbytného kontextu. |

## <a name="in-preview"></a>Náhled

Verze Preview obsahuje následující nové funkce. Další informace o zapnutí a vypnutí funkcí naleznete v tématu [Správa funkcí](hr-admin-manage-features.md).

| Funkce | Plán vydání | Dokumentace |
| --- | --- | --- |
| Pracovní prostor správy zaměstnaneckých výhod | [Pracovní prostor správy zaměstnaneckých výhod (Preview)](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Pracovní prostor správy zaměstnaneckých výhod](hr-benefits-management-workspace.md) |
| U zaměstnanců můžete omezit jejich upravování podrobností obchodních kontaktů | [U zaměstnanců můžete omezit jejich upravování podrobností obchodních kontaktů](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [Omezení úpravy osobních údajů](hr-employee-self-service-restrict-editing.md)|

## <a name="coming-soon"></a>Již brzy

| Funkce | Podrobnosti |
| --- | --- |
| Dovednosti zadané manažery pro své zaměstnance lze automaticky schválit pomocí pracovního postupu | Již brzy. |

Úplný seznam plánovaných funkcí a plánovaných verzí najdete v části [Přehled o 1. vlně vydání Dynamics 365 Human Resources v roce 2021](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Viz také

[Co je nového a co se změnilo v Human Resources](hr-admin-whats-new.md)</br>
[Přehled produktu Dynamics 365 Human Resources vydání 2021 vlny 1](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Aktualizace procesu](hr-admin-setup-update-process.md)</br>
[Správa funkcí](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
