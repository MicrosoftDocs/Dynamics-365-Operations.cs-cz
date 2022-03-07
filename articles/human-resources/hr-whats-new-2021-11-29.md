---
title: Co je nového nebo co se změnilo v aplikaci Dynamics 365 Human Resources 19. listopadu 2021
description: Tohle téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Human Resources k 19. listopadu 2021.
author: marcelbf
ms.date: 12/03/2021
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
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3a86c1c24fbc758f4e3d0fd8b052e02078bee41e
ms.sourcegitcommit: 88f8a0369ce66b82314db9639491b695e18a7e5c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/09/2021
ms.locfileid: "7902597"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-november-19-2021"></a>Co je nového nebo co se změnilo v aplikaci Dynamics 365 Human Resources 19. listopadu 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Tohle téma popisuje funkce, které jsou nové, byly změněny nebo se brzy objeví v aplikaci Microsoft Dynamics 365 Human Resources.

Další informace o našem procesu aktualizaci a plánu najdete v tématu [Proces aktualizace](hr-admin-setup-update-process.md).

Další informace o nových funkcích a jejich očekávaných obecných datech dostupnosti najdete v tématu [2. vlna vydání Dynamics 365 Human Resources v roce 2021](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>V této vydané verzi

Toto vydání obsahuje následující opravy chyb. Změny se vztahují na sestavení číslo 8.1.4591.

### <a name="bug-fixes"></a>Opravy chyb

Tato verze obsahuje následující opravy chyb.

> [!NOTE]
> Naším cílem dostat k vám tyto informace co nejdříve. Tohle téma můžeme aktualizovat, aby obsahovalo opravy chyb, které se dostaly do sestavení poté, co bylo toto téma původně publikováno.

| Číslo problému | Problém | Popis |
|---|---|---|
| 626178 | Na dlaždicích pracovníků v **samoobsluze pro manažery** chybí navigace | Tento problém je nyní vyřešen. Navigace je k dispozici pro zobrazení podrobností sestavy v **samoobsluze pro manažery**. |
| 632573 | Při ukládání **kurzu** nedochází k chybě ověření | Tento problém je nyní vyřešen. Při vytváření kurzu s **minimálním počtem účastníků** větším než 0 bylo stále povoleno ukládání, i když **Maximální počet účastníků** byl 0. |
| 615955 | Chyba „Pole **Účel** musí být vyplněno“ při vytváření nového místa požadavku na nábor. | Při vytváření adresy pro nové místo požadavku na nábor se zobrazuje chyba: „Pole Účel musí být vyplněno“. Nicméně pole **Účel** není dostupné na stránce. |
| 620797 | Chyba Prázdné pole **Pohlaví** je zavádějící | Pokud u osobního kontaktu není zadáno pohlaví, ve zprávě se zobrazí „Kliknutím nebo klepnutím sem zadejte text“ – to je zavádějící, protože do pole nelze nic zadat. |
| 620800 | Odkaz na Výkaz zaměstnaneckých výhod je skrytý | Výkaz zaměstnaneckých výhod není ve výchozím nastavení viditelný v **samoobsluze pro zaměstnance**.  Na pravou stranu **samoobsluhy pro zaměstnance** v sekci **Odkazy** byl přidán odkaz |
| 629778 | Problém s výkonem při integraci CDS. | Požadavek související s autorizací způsobil problém s výkonem. |

## <a name="in-preview"></a>Náhled

Verze Preview obsahuje následující nové funkce. Další informace o zapnutí a vypnutí funkcí naleznete v tématu [Správa funkcí](hr-admin-manage-features.md).

| Funkce | Plán vydání | Dokumentace |
|---|---|---|
| Pracovní prostor správy zaměstnaneckých výhod | [Pracovní prostor správy zaměstnaneckých výhod (Preview)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Pracovní prostor správy zaměstnaneckých výhod](hr-benefits-management-workspace.md) |


## <a name="coming-soon"></a>Již brzy
Úplný seznam plánovaných funkcí a plánovaných verzí najdete v části [Dynamics 365 a průmyslová cloudová řešení: Plán 2. vlny vydání v roce 2021](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
