---
title: Přehled optimalizace plánování
description: Toto téma obsahuje přehled optimalizace plánování.
author: ChristianRytt
manager: tfehr
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: f88ee8067fdd816ba6890ee28bafe8fa4d3b3ac5
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208724"
---
# <a name="planning-optimization-overview"></a><span data-ttu-id="90407-103">Přehled optimalizace plánování</span><span class="sxs-lookup"><span data-stu-id="90407-103">Planning Optimization overview</span></span>

[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="90407-104">Doplněk optimalizace plánování pro Microsoft Dynamics 365 Supply Chain Management umožňuje, byl výpočet hlavního plánování proveden mimo Dynamics 365 Supply Chain Management a související databázi SQL.</span><span class="sxs-lookup"><span data-stu-id="90407-104">The Planning Optimization Add-in for Microsoft Dynamics 365 Supply Chain Management enables master planning calculation to occur outside Dynamics 365 Supply Chain Management and the related SQL database.</span></span> <span data-ttu-id="90407-105">Výhody, které jsou přidruženy k funkcím optimalizace plánování, zahrnují lepší výkon a minimální dopad na databázi SQL během spuštění hlavního plánování.</span><span class="sxs-lookup"><span data-stu-id="90407-105">The benefits that are associated with the Planning Optimization functionality include improved performance and minimal impact on SQL database during master planning runs.</span></span> <span data-ttu-id="90407-106">Rychlé plánování lze provést i v průběhu pracovní doby, aby plánovači mohli ihned reagovat na požadavky nebo změny parametrů.</span><span class="sxs-lookup"><span data-stu-id="90407-106">Quick planning runs can be done even during office hours, so that planners can immediately react to demand or parameter changes.</span></span>

<span data-ttu-id="90407-107">Chcete-li použít optimalizaci plánování, je nutné nainstalovat doplněk pro optimalizaci plánování z projektu do služby Microsoft Dynamics Lifecycle Services (LCS) a zapnout funkci optimalizace plánování ve správě dodavatelských řetězců.</span><span class="sxs-lookup"><span data-stu-id="90407-107">To use Planning Optimization, you must install the Planning Optimization Add-in from your project in Microsoft Dynamics Lifecycle Services (LCS) and turn on the Planning Optimization functionality in Supply Chain Management.</span></span> <span data-ttu-id="90407-108">Další informace naleznete v tématu [Začínáme s optimalizací plánování](get-started.md)</span><span class="sxs-lookup"><span data-stu-id="90407-108">For more information, see [Get started with Planning Optimization](get-started.md).</span></span>

<span data-ttu-id="90407-109">Na následujícím obrázku je znázorněna výhoda spuštění optimalizace plánování během pracovní doby.</span><span class="sxs-lookup"><span data-stu-id="90407-109">The following illustration shows the advantage of running Planning Optimization during office hours.</span></span>

![Výhoda spuštění optimalizace plánování během pracovní doby](media/PlanningOptimization1.png)

## <a name="improved-performance"></a><span data-ttu-id="90407-111">Zlepšení výkonu</span><span class="sxs-lookup"><span data-stu-id="90407-111">Improved performance</span></span>

<span data-ttu-id="90407-112">Optimalizaci plánování lze použít ve scénářích, které zahrnují dlouhodobé průběžné hlavní plány.</span><span class="sxs-lookup"><span data-stu-id="90407-112">Planning Optimization can be used in scenarios that involve long-running master plans.</span></span> <span data-ttu-id="90407-113">Je speciálně navržena pro velmi rychlé výpočty, které zahrnují velmi velké objemy dat.</span><span class="sxs-lookup"><span data-stu-id="90407-113">It's specifically designed for very fast calculations that involve very large volumes of data.</span></span> <span data-ttu-id="90407-114">Protože je postaven jako hyperškálovatelná technologie, může více instancí současně spolupracovat při výpočtu plánu.</span><span class="sxs-lookup"><span data-stu-id="90407-114">Because it's built as a hyper-scalable multitenant service, multiple instances can work together simultaneously to calculate the plan.</span></span> <span data-ttu-id="90407-115">Kromě toho služba plánování odebere z vašeho systému vytížení hlavního plánování a spolupracuje s datovým proudem, který minimalizuje objem vytížení serveru.</span><span class="sxs-lookup"><span data-stu-id="90407-115">Additionally, the planning service removes the load of master planning from your system and works with a data stream that minimizes the server load.</span></span>

<span data-ttu-id="90407-116">Optimalizace plánování vám může pomoci dosáhnout následujících cílů:</span><span class="sxs-lookup"><span data-stu-id="90407-116">Planning Optimization can help you achieve the following goals:</span></span>

- <span data-ttu-id="90407-117">Zlepšení výkonnosti plánování díky kratší době realizace.</span><span class="sxs-lookup"><span data-stu-id="90407-117">Improve planning performance through a shorter runtime.</span></span>
- <span data-ttu-id="90407-118">Snížení dopadu na jiné procesy během spuštění hlavního plánování.</span><span class="sxs-lookup"><span data-stu-id="90407-118">Reduce the impact on other processes during the master planning run.</span></span>
- <span data-ttu-id="90407-119">Častější spouštění plánování.</span><span class="sxs-lookup"><span data-stu-id="90407-119">Do more frequent planning runs.</span></span> <span data-ttu-id="90407-120">(Nemáte omezení na denní spuštění.)</span><span class="sxs-lookup"><span data-stu-id="90407-120">(You aren't limited to daily runs.)</span></span>
- <span data-ttu-id="90407-121">Nezapomeňte, že budoucí růst obchodu nebude systém plánování přetěžovat.</span><span class="sxs-lookup"><span data-stu-id="90407-121">Be confident that future business growth won't overload the planning system.</span></span>

## <a name="architecture-and-data-flow"></a><span data-ttu-id="90407-122">Architektura a tok dat</span><span class="sxs-lookup"><span data-stu-id="90407-122">Architecture and data flow</span></span>

<span data-ttu-id="90407-123">Po instalaci doplňku pro optimalizaci plánování z LCS bude navázáno zabezpečené připojení ke službě optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="90407-123">When the Planning Optimization Add-in is installed from LCS, a secure connection to the Planning Optimization service is established.</span></span> <span data-ttu-id="90407-124">Služba se nachází ve stejné zemi nebo oblasti datového střediska jako související instance Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="90407-124">The service is located in the same data center country or region as the related Supply Chain Management instance.</span></span> <span data-ttu-id="90407-125">Po nastavení optimalizace plánování jsou při spuštění hlavního plánování odeslána hlavní data a transakční data z modulu Supply Chain Management do služby Optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="90407-125">After Planning Optimization is set up, when master planning is run, master data and transactional data are sent from Supply Chain Management to the Planning Optimization service.</span></span>

<span data-ttu-id="90407-126">Pokud dojde k odinstalaci doplňku optimalizace plánování, budou všechna související data ve službě optimalizace plánování odebrána.</span><span class="sxs-lookup"><span data-stu-id="90407-126">If the Planning Optimization Add-in is uninstalled, all related data in the Planning Optimization service is removed.</span></span>

### <a name="high-level-data-flow-for-regeneration-runs"></a><span data-ttu-id="90407-127">Tok dat na vysoké úrovni pro spuštění regenerace</span><span class="sxs-lookup"><span data-stu-id="90407-127">High-level data flow for regeneration runs</span></span>

1. <span data-ttu-id="90407-128">Klient Supply Chain Management odešle signál, aby vyžádal spuštění plánování z optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="90407-128">The Supply Chain Management client sends a signal to request a planning run from Planning Optimization.</span></span>
2. <span data-ttu-id="90407-129">Optimalizace plánování požaduje povinná data prostřednictvím integrovaného konektoru.</span><span class="sxs-lookup"><span data-stu-id="90407-129">Planning Optimization requests the required data via the integrated connector.</span></span>
3. <span data-ttu-id="90407-130">Databáze SQL odesílá požadované informace o nastavení, hlavních a transakčních datech pro optimalizaci plánování prostřednictvím konektoru.</span><span class="sxs-lookup"><span data-stu-id="90407-130">The SQL database sends the requested information about setup, master, and transactional data to Planning Optimization via the connector.</span></span> <span data-ttu-id="90407-131">Konektor převádí informace mezi správou Supply Chain Management a službou optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="90407-131">The connector translates information between Supply Chain Management and the Planning Optimization service.</span></span>
4. <span data-ttu-id="90407-132">Služba optimalizace plánování obsahuje data týkající se plánování v paměti a provádí požadované výpočty.</span><span class="sxs-lookup"><span data-stu-id="90407-132">The Planning Optimization service holds planning-related data in memory and does the required calculations.</span></span>
5. <span data-ttu-id="90407-133">Výsledek plánování je odeslán do databáze správy zásobovacího řetězce prostřednictvím konektoru.</span><span class="sxs-lookup"><span data-stu-id="90407-133">The planning result is sent to the Supply Chain Management database via the connector.</span></span> <span data-ttu-id="90407-134">Výsledky zahrnují například informace o plánovaných objednávkách a informacích o doložení.</span><span class="sxs-lookup"><span data-stu-id="90407-134">The results include information such as planned orders and pegging information.</span></span> <span data-ttu-id="90407-135">Optimalizace plánování odešle signál do Supply Chain Management s cílem označit, že spuštění plánování bylo dokončeno.</span><span class="sxs-lookup"><span data-stu-id="90407-135">Planning Optimization sends a signal to Supply Chain Management to indicate that the planning run has been completed.</span></span> <span data-ttu-id="90407-136">Dále budou odeslány všechny příslušné zprávy a upozornění.</span><span class="sxs-lookup"><span data-stu-id="90407-136">It also sends any relevant messages and warnings.</span></span>

<span data-ttu-id="90407-137">Následující obrázek znázorňuje tok dat.</span><span class="sxs-lookup"><span data-stu-id="90407-137">The following illustration shows the data flow.</span></span>

![Tok dat pro spuštění regenerace](media/PlanningOptimization2.png)

## <a name="related-resources"></a><span data-ttu-id="90407-139">Související prostředky</span><span class="sxs-lookup"><span data-stu-id="90407-139">Related resources</span></span>

[<span data-ttu-id="90407-140">Začínáme s optimalizací plánování</span><span class="sxs-lookup"><span data-stu-id="90407-140">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="90407-141">Analýza přizpůsobení pro optimalizaci plánování</span><span class="sxs-lookup"><span data-stu-id="90407-141">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="90407-142">Zobrazení historie plánu a protokolů plánování</span><span class="sxs-lookup"><span data-stu-id="90407-142">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="90407-143">Použití filtrů v plánu</span><span class="sxs-lookup"><span data-stu-id="90407-143">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="90407-144">Zrušení úlohy plánování</span><span class="sxs-lookup"><span data-stu-id="90407-144">Cancel a planning job</span></span>](cancel-planning-job.md)
