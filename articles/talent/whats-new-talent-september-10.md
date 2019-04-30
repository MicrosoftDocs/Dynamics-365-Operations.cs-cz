---
title: Co je nového nebo upraveného v aplikaci Dynamics 365 for Talent Core HR (10. září 2018)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-09-06
ms.dyn365.ops.version: Talent September 10, 2018 update
ms.openlocfilehash: 6682e4d013f006696b45e644b7b4861b34faa9bf
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/19/2019
ms.locfileid: "857400"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-september-10-2018"></a>Co je nového nebo upraveného v aplikaci Dynamics 365 for Talent Core HR (10. září 2018)

[!include [banner](includes/banner.md)]

**Sestavení 8.1.138.0**

Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 for Talent Core HR.

## <a name="allow-specific-time-of-day-on-time-off-requests-half-days"></a>Povolení specifického času ze dne na požadavku o volno (půlden)

Pokud jsou pracovní volno a absence nastaveny tak, aby bylo volno zadáváno ve dnech, můžete teď rovněž povolit definici půldne. Když uživatelé odešlou požadavky na volno, mohou určit, zda žádají volno na první nebo druhou polovinu dne.

Ve výchozím nastavení je tato možnost vypnuta. U zaměstnanců, kteří mohou požádat o volno pouze na první nebo druhou polovinu dne, musíte zapnout tuto možnost v oblasti **Pracovní volno a absence** parametrů lidských zdrojů.

Oprávnění zabezpečení pro tuto funkci je Udržovat parametry lidských zdrojů.

## <a name="validation-of-leave-and-absence-entries"></a>Ověření zadání pracovního volna a absence

V závislosti na konfiguraci pracovního volna zaměstnanci, kteří se pokusí odeslat požadavek na volno, které je delší než jejich pracovní den, obdrží zprávu s upozorněním. Jinak řečeno, jsou upozorněni v případě, že se pokusí vzít více než jeden celý den volna v jakékoliv dané datum.

Toto ověření je vždy zapnuto. Pokaždé, když zaměstnanec překročí definovanou prahovou hodnotu dnů, dostane upozornění ve svém požadavku na volno.

## <a name="additional-fields-for-conditional-statements-in-workflows"></a>Další pole pro podmíněné příkazy ve workflow

Další pole byla přidána do podmíněných příkazů a zástupných textů pro některá workflow v Core HR.

Následující pole byla přidána do workflow kompenzací, ukončení a převodu:

- EmploymentType
- LegalEntity
- AdjustedWorkerStartDate
- EmployerNoticeAmount
- EmployerUnitOfNotice
- TransitionDate
- WorkerNoticeAmount
- WorkerStartDate
- WorkerUnitOfNotice
- ProbationEndDate
- Pozice
- Sjednocení
- Oddělení
- PositionType
- CompLocation
- Pozice
- Práce
- JobType
- JobFamily
- JobFunction

Následující pole byla přidána do workflow pozic:

- Pozice
- Sjednocení
- Oddělení
- PositionType
- CompLocation
- Pozice
- Práce
- JobType
- JobFamily
- JobFunction

Pole v podmíněných příkazech a zástupných textech jsou dostupná pro všechny uživatele, kteří mají přístup ke konfiguraci výše zmíněných workflow.

## <a name="navigation-to-attract-from-personnel-management"></a>Navigace do aplikace Attract ze správy personálu

Pokud nebyla aplikace Attract nastavena, část **Kandidáti k přjetí** přesměruje uživatele na spuštění aplikace Attract, namísto zobrazení zprávy „Nenašli jsme tady nic k zobrazení“.

## <a name="other-changes"></a>Další změny

Toto vydání obsahuje několik dalších oprav chyb:

- Když je přijat dodavatel, karta **Kompenzace** by neměla být k dispozici na stránce požadavku/akce.
- V průběhu procesu ukončení požadavku nelze pokračovat, dokud všechna povinná pole neobsahují data.
- Problémy s pořadím řazení a zobrazením dat v analýze správy personálu byly vyřešeny.
