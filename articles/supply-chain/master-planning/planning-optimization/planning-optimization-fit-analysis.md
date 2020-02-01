---
title: Analýza přizpůsobení pro optimalizaci plánování
description: V tomto tématu je vysvětleno, jak ověřit aktuální nastavení a data proti funkcím funkce optimalizace plánování.
author: ChristianRytt
manager: AnnBe
ms.date: 10/30/2019
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
ms.openlocfilehash: a61529da63bc20fdd591afc94db960b05c284bb9
ms.sourcegitcommit: b806f0c94d703bec39680fead827733361d47045
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/07/2020
ms.locfileid: "2935868"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="planning-optimization-fit-analysis"></a><span data-ttu-id="c97bc-103">Analýza přizpůsobení pro optimalizaci plánování</span><span class="sxs-lookup"><span data-stu-id="c97bc-103">Planning Optimization fit analysis</span></span>

<span data-ttu-id="c97bc-104">Chcete-li zjistit, jakým způsobem jsou aktuální nastavení a data kompatibilní s funkcí Optimalizace plánování, přejděte na **Hlavní plánování** \> **Nastavení** \> **Analýza shody optimalizace plánování** a vyberte **Spustit analýzu**.</span><span class="sxs-lookup"><span data-stu-id="c97bc-104">To see how compatible your current setup and data are with the Planning Optimization functionality, go to **Master planning** \> **Setup** \> **Planning Optimization fit analysis**, and then select **Run analysis**.</span></span> <span data-ttu-id="c97bc-105">Pokud analýza nalezne nějaké nekonzistence, budou uvedeny na stejné stránce.</span><span class="sxs-lookup"><span data-stu-id="c97bc-105">If the analysis finds any inconsistencies, they are listed on the same page.</span></span> <span data-ttu-id="c97bc-106">(Provádění analýzy může trvat několik minut.)</span><span class="sxs-lookup"><span data-stu-id="c97bc-106">(The analysis can take a few minutes to run.)</span></span>

> [!NOTE]
> <span data-ttu-id="c97bc-107">Pokud jsou nalezeny nekonzistence, můžete stále používat optimalizaci plánování.</span><span class="sxs-lookup"><span data-stu-id="c97bc-107">If inconsistencies are found, you can still use Planning Optimization.</span></span> <span data-ttu-id="c97bc-108">Výsledky analýzy přizpůsobení zobrazují pouze místa, kde plánovací služba nerespektuje vaše aktuální nastavení.</span><span class="sxs-lookup"><span data-stu-id="c97bc-108">The results of the fit analysis just show places where the planning service won't honor your current setup.</span></span> <span data-ttu-id="c97bc-109">Jinými slovy, zobrazují místa, kde některé procesy mohou být ignorovány nebo nejsou podporovány.</span><span class="sxs-lookup"><span data-stu-id="c97bc-109">In other words, they show places where some processes might be ignored or might not be supported.</span></span>

## <a name="analysis-results-example-1"></a><span data-ttu-id="c97bc-110">Výsledky analýzy: Příklad 1</span><span class="sxs-lookup"><span data-stu-id="c97bc-110">Analysis results: Example 1</span></span>

- <span data-ttu-id="c97bc-111">**Funkce:** Výroba</span><span class="sxs-lookup"><span data-stu-id="c97bc-111">**Feature:** Production</span></span>
- <span data-ttu-id="c97bc-112">**Problém:** Položky s úrovní kusovníku větší než nula: 56</span><span class="sxs-lookup"><span data-stu-id="c97bc-112">**Issue:** Items with BOM level greater than zero: 56</span></span>
- <span data-ttu-id="c97bc-113">**Vysvětlení:** Analýza přizpůsobení nalezla 56 položek, které mají pro výrobu nastaven kusovník.</span><span class="sxs-lookup"><span data-stu-id="c97bc-113">**Explanation:** The fit analysis found 56 items that have a bill of materials (BOM) setup for production.</span></span> <span data-ttu-id="c97bc-114">Vzhledem k tomu, že aktuální verze optimalizace plánování nepodporuje výrobu, optimalizace plánování vygeneruje plánované nákupní objednávky namísto plánovaných výrobních zakázek.</span><span class="sxs-lookup"><span data-stu-id="c97bc-114">Because the current version of Planning Optimization doesn't support production, Planning Optimization will generate planned purchase orders instead of planned production orders.</span></span> <span data-ttu-id="c97bc-115">Zobrazí se také upozornění, které obsahuje seznam ovlivněných položek.</span><span class="sxs-lookup"><span data-stu-id="c97bc-115">It will also show a warning that lists the affected items.</span></span>

### <a name="analysis-results-example-2"></a><span data-ttu-id="c97bc-116">Výsledky analýzy: Příklad 2</span><span class="sxs-lookup"><span data-stu-id="c97bc-116">Analysis results: Example 2</span></span>

- <span data-ttu-id="c97bc-117">**Funkce:** Akce</span><span class="sxs-lookup"><span data-stu-id="c97bc-117">**Feature:** Actions</span></span>
- <span data-ttu-id="c97bc-118">**Problém:** Skupiny disponibility s povolenou kalkulací akcí: 6</span><span class="sxs-lookup"><span data-stu-id="c97bc-118">**Issue:** Coverage groups with actions calculation enabled: 6</span></span>
- <span data-ttu-id="c97bc-119">**Vysvětlení:** Analýza přizpůsobení našla šest skupin disponibility, kde je zapnut výpočet akce.</span><span class="sxs-lookup"><span data-stu-id="c97bc-119">**Explanation:** The fit analysis found six coverage groups where action calculation is turned on.</span></span> <span data-ttu-id="c97bc-120">Vzhledem k tomu, že aktuální verze optimalizace plánování nepodporuje akce, nebudou při hlavním plánování generovány žádné akce.</span><span class="sxs-lookup"><span data-stu-id="c97bc-120">Because the current version of Planning Optimization doesn't support actions, no actions will be generated during master planning.</span></span>

## <a name="related-resources"></a><span data-ttu-id="c97bc-121">Související prostředky</span><span class="sxs-lookup"><span data-stu-id="c97bc-121">Related resources</span></span>

[<span data-ttu-id="c97bc-122">Přehled optimalizace plánování</span><span class="sxs-lookup"><span data-stu-id="c97bc-122">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="c97bc-123">Začínáme s optimalizací plánování</span><span class="sxs-lookup"><span data-stu-id="c97bc-123">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="c97bc-124">Zobrazení historie plánu a protokolů plánování</span><span class="sxs-lookup"><span data-stu-id="c97bc-124">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="c97bc-125">Použití filtrů v plánu</span><span class="sxs-lookup"><span data-stu-id="c97bc-125">Apply filters to a plan</span></span>](plan-filters.md)

[<span data-ttu-id="c97bc-126">Zrušení úlohy plánování</span><span class="sxs-lookup"><span data-stu-id="c97bc-126">Cancel a planning job</span></span>](cancel-planning-job.md)