---
title: Přehled optimalizace plánování
description: Toto téma obsahuje přehled optimalizace plánování.
author: ChristianRytt
manager: AnnBe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: aae9ea56fc2174df56274776993c68b11c0521d0
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773916"
---
[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

# <a name="planning-optimization-overview"></a>Přehled optimalizace plánování

Doplněk optimalizace plánování pro Microsoft Dynamics 365 Supply Chain Management umožňuje, byl výpočet hlavního plánování proveden mimo Dynamics 365 Supply Chain Management a související databázi SQL. Výhody, které jsou přidruženy k funkcím optimalizace plánování, zahrnují lepší výkon a minimální dopad na databázi SQL během spuštění hlavního plánování. Rychlé plánování lze provést i v průběhu pracovní doby, aby plánovači mohli ihned reagovat na požadavky nebo změny parametrů.

Chcete-li použít optimalizaci plánování, je nutné nainstalovat doplněk pro optimalizaci plánování z projektu do služby Microsoft Dynamics Lifecycle Services (LCS) a zapnout funkci optimalizace plánování ve správě dodavatelských řetězců. Další informace naleznete v tématu [Začínáme s optimalizací plánování](get-started.md)

Na následujícím obrázku je znázorněna výhoda spuštění optimalizace plánování během pracovní doby.

![Výhoda spuštění optimalizace plánování během pracovní doby](media/PlanningOptimization1.png)

## <a name="improved-performance"></a>Zlepšení výkonu

Optimalizaci plánování lze použít ve scénářích, které zahrnují dlouhodobé průběžné hlavní plány. Je speciálně navržena pro velmi rychlé výpočty, které zahrnují velmi velké objemy dat. Protože je postaven jako hyperškálovatelná technologie, může více instancí současně spolupracovat při výpočtu plánu. Kromě toho služba plánování odebere z vašeho systému vytížení hlavního plánování a spolupracuje s datovým proudem, který minimalizuje objem vytížení serveru.

Optimalizace plánování vám může pomoci dosáhnout následujících cílů:

- Zlepšení výkonnosti plánování díky kratší době realizace.
- Snížení dopadu na jiné procesy během spuštění hlavního plánování.
- Častější spouštění plánování. (Nemáte omezení na denní spuštění.)
- Nezapomeňte, že budoucí růst obchodu nebude systém plánování přetěžovat.

## <a name="architecture-and-data-flow"></a>Architektura a tok dat

Po instalaci doplňku pro optimalizaci plánování z LCS bude navázáno zabezpečené připojení ke službě optimalizace plánování. Služba se nachází ve stejné zemi nebo oblasti datového střediska jako související instance Supply Chain Management. Po nastavení optimalizace plánování jsou při spuštění hlavního plánování odeslána hlavní data a transakční data z modulu Supply Chain Management do služby Optimalizace plánování.

Pokud dojde k odinstalaci doplňku optimalizace plánování, budou všechna související data ve službě optimalizace plánování odebrána.

### <a name="high-level-data-flow-for-regeneration-runs"></a>Tok dat na vysoké úrovni pro spuštění regenerace

1. Klient Supply Chain Management odešle signál, aby vyžádal spuštění plánování z optimalizace plánování.
2. Optimalizace plánování požaduje povinná data prostřednictvím integrovaného konektoru.
3. Databáze SQL odesílá požadované informace o nastavení, hlavních a transakčních datech pro optimalizaci plánování prostřednictvím konektoru. Konektor převádí informace mezi správou Supply Chain Management a službou optimalizace plánování.
4. Služba optimalizace plánování obsahuje data týkající se plánování v paměti a provádí požadované výpočty.
5. Výsledek plánování je odeslán do databáze správy zásobovacího řetězce prostřednictvím konektoru. Výsledky zahrnují například informace o plánovaných objednávkách a informacích o doložení. Optimalizace plánování odešle signál do Supply Chain Management s cílem označit, že spuštění plánování bylo dokončeno. Dále budou odeslány všechny příslušné zprávy a upozornění.

Následující obrázek znázorňuje tok dat.

![Tok dat pro spuštění regenerace](media/PlanningOptimization2.png)

## <a name="related-resources"></a>Související prostředky

[Začínáme s optimalizací plánování](get-started.md)

[Analýza přizpůsobení pro optimalizaci plánování](planning-optimization-fit-analysis.md)

[Zobrazení historie plánu a protokolů plánování](plan-history-logs.md)

[Použití filtrů v plánu](plan-filters.md)

[Zrušení úlohy plánování](cancel-planning-job.md)
