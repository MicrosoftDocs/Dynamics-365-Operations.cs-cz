---
title: Přehled hlavních plánů
description: Používání různých hlavních plánů na podporu každodenního provozu své společnosti, simulovat různé strategie plánování,které chcete monitorovat a zavádět podnikovou pravidla, týkající se například zásad interní výkonnosti nebo spokojenosti zákazníka.
author: ChristianRytt
ms.date: 05/28/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ReqParameters, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "7911"
- intro-internal
ms.assetid: a116b7de-3d6d-4321-87ba-5a5d99c2f64e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 03467778025287f3692e171bea37b1bfb2ca1646
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2022
ms.locfileid: "7982347"
---
# <a name="master-plans-overview"></a>Přehled hlavních plánů

[!include [banner](../includes/banner.md)]

Používání různých hlavních plánů na podporu každodenního provozu své společnosti, simulovat různé strategie plánování,které chcete monitorovat a zavádět podnikovou pravidla, týkající se například zásad interní výkonnosti nebo spokojenosti zákazníka.

Hlavní plány můžete nakonfigurovat na stránce **Hlavní plány**.

Existují dva typy plánů:

- **Statický plán** – hlavní plánovací výpočet používá aktuální data pro vygenerování plánu čistých požadavků. Tento plán zůstává nezměněný do následujícího spuštění hlavního plánování nebo ruční změny plánu. Jedná se o operační plán, který může používat různý personál společnosti, například nákupčí nebo plánovač výroby a zakládat na něm svá rozhodnutí a provádět každodenní činnosti.
- **Dynamický plán** – Tento plán začíná se stejným plánem čistých požadavků, který byl vygenerován hlavním plánováním. Dynamický plán však můžete aktualizovat vždy při změně hlavních dat. To může být například při vytvoření nové prodejní objednávky. To vám umožní sledovat síť změnových příkazů dostupnost položky bez narušení statického plánu, který používají ostatní pracovníci pro své pracovní procesy.

Společnost si může vybrat práci pouze s dynamickým plánem nebo používat statický i dynamický plán. Kromě toho můžete nakonfigurovat jakýkoliv hlavní plán a zohlednit tak specifickou strategii nebo vyřešit problém. Příklady jsou následující:

- Nastavení vyšší úrovně skladu na ochranu před vyčerpáním zásob.
- Nastavení delších pojistných dob na ochranu před nespolehlivými dodavateli.

Můžete také nastavit počáteční dynamický plán tak, aby se aktualizoval s novými požadavky při každém spuštění hlavního plánování. Tato nastavení můžete zadat na stránce **Parametry hlavního plánování**.

## <a name="additional-resources"></a>Další zdroje

- [Nastavení distponibility](coverage-settings.md)
- [Oddělení taktického a operativního plánování pro hlavní plánování](https://community.dynamics.com/ax/b/dynamicsaxmanufacturingrdteamblog/posts/separating-tactical-and-operative-planning-for-master-scheduling)
- [Hlavní plánování: Použít statický a dynamický hlavní plán nebo jeden plán?](https://community.dynamics.com/ax/b/msdynaxlessonslearned/archive/2014/01/16/master-planning-use-a-static-and-dynamic-master-plan-or-use-one-plan)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
