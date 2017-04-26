---
title: "Hlavní plány"
description: "Použijte různé hlavní plány pro podporu každodenního provozu své společnosti, simulovat různé strategie plánování, které chcete sledovat a implementovat zásady společnosti, jako jsou zásady o vnitřní spokojenosti výkonu nebo zákazníka."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqParameters, ReqPlanSched
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 7911
ms.assetid: a116b7de-3d6d-4321-87ba-5a5d99c2f64e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 29bb560c11e63938bea73ed8471c27563b546f8f
ms.lasthandoff: 03/31/2017


---

# <a name="master-plans"></a>Hlavní plány

[!include[banner](../includes/banner.md)]


Použijte různé hlavní plány pro podporu každodenního provozu své společnosti, simulovat různé strategie plánování, které chcete sledovat a implementovat zásady společnosti, jako jsou zásady o vnitřní spokojenosti výkonu nebo zákazníka. 

Hlavní plány můžete nakonfigurovat na stránce **Hlavní plány**.

Existují dva typy plánů:
-   **Statický plán** – hlavní plánovací výpočet používá aktuální data pro vygenerování plánu čistých požadavků. Tento plán zůstává nezměněný do následujícího spuštění hlavního plánování. Jedná se o operační plán, který může používat různý personál společnosti, například nákupčí nebo plánovač výroby a zakládat na něm svá rozhodnutí a provádět každodenní úkoly a činnosti.
-   **Dynamický plán** – Tento plán začíná se stejným plánem čistých požadavků, který byl vygenerován hlavním plánováním. Dynamický plán však můžete aktualizovat vždy při změně hlavních dat. To může být například při vytvoření nové prodejní objednávky. To vám umožní sledovat síť změnových příkazů dostupnost položky bez narušení statického plánu, který používají ostatní pracovníci pro své pracovní procesy.

Společnost si může vybrat práci pouze s dynamickým plánem nebo používat statický i dynamický plán. Kromě toho můžete nakonfigurovat jakýkoliv hlavní plán a zohlednit tak specifickou strategii nebo vyřešit problém. Příklady jsou následující:
-   Nastavení vyšší úrovně skladu na ochranu před vyčerpáním zásob.
-   Nastavení delších pojistných dob na ochranu před nespolehlivými dodavateli.

Můžete také nastavit počáteční dynamický plán tak, aby se aktualizoval s novými požadavky při každém spuštění hlavního plánování. Tato nastavení můžete zadat na stránce **Parametry hlavního plánování**.



<a name="see-also"></a>Viz také
--------

[Nastavení pokrytí](coverage-settings.md)

[Oddělení, taktické a operativní plánování pro hlavní plánování](http://blogs.msdn.com/b/axmfg/archive/2012/10/12/separating-tactical-and-operative-planning-for-master-scheduling.aspx)

[Hlavní plánování: Použijte statický a dynamický hlavní plán nebo jeden plán?](https://community.dynamics.com/ax/b/msdynaxlessonslearned/archive/2014/01/16/master-planning-use-a-static-and-dynamic-master-plan-or-use-one-plan)




