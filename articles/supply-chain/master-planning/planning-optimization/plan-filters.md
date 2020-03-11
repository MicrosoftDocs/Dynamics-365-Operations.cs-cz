---
title: Použití filtrů v plánu
description: Toto téma vysvětluje způsob použití filtrů v plánu při použití funkce Optimalizace plánování.
author: ChristianRytt
manager: AnnBe
ms.date: 01/08/2020
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
ms.openlocfilehash: ca28953846b4f1978a453d2ab2aa9759e4f45221
ms.sourcegitcommit: a688c864fc609e35072ad8fd2c01d71f6a5ee7b9
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/20/2020
ms.locfileid: "3076102"
---
# <a name="apply-filters-to-a-plan"></a><span data-ttu-id="b0a84-103">Použití filtrů v plánu</span><span class="sxs-lookup"><span data-stu-id="b0a84-103">Apply filters to a plan</span></span>

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b0a84-104">Při použití funkce Optimalizace plánování můžete aplikovat filtr na plán.</span><span class="sxs-lookup"><span data-stu-id="b0a84-104">When the Planning Optimization functionality is used, you can apply a filter to a plan.</span></span> <span data-ttu-id="b0a84-105">**Filtr plánu** bude vždy použit při spuštění hlavního plánování.</span><span class="sxs-lookup"><span data-stu-id="b0a84-105">The **Plan filter** will always be applied during a master planning run.</span></span> <span data-ttu-id="b0a84-106">**Filtr plánu** je užitečný v případě, že chcete omezit plán na určitou skupinu položek a ujistit se, že jako součást výsledného hlavního plánování nejsou zahrnuty žádné další položky.</span><span class="sxs-lookup"><span data-stu-id="b0a84-106">A **Plan filter** is useful when you want to limit a plan to a specific group of items and make sure that no other items are included as part of the resulting master planning.</span></span>

<span data-ttu-id="b0a84-107">Pokud je použit **Filtr plánu** a v průběhu spuštění hlavního plánování je také použit filtr běhu, je do spuštění plánování zahrnut pouze průnik těchto dvou filtrů.</span><span class="sxs-lookup"><span data-stu-id="b0a84-107">If a **Plan filter** is applied, and a runtime filter is also applied during the master planning run, only the intersection of the two filters is included in the planning run.</span></span>

<span data-ttu-id="b0a84-108">K **Filtru plánu** se lze dostat z **Hlavních plánů** při použití Optimalizace plánování.</span><span class="sxs-lookup"><span data-stu-id="b0a84-108">The **Plan filter** can be accessed from **Master plans** when Planning Optimization is used.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="b0a84-109">Příklad</span><span class="sxs-lookup"><span data-stu-id="b0a84-109">Example scenario</span></span>

<span data-ttu-id="b0a84-110">Je nastaven filtr plánu, který zahrnuje položky A, B a C. Běhy hlavního plánování se potom spustí pro stejný plán, ale jsou použity různé běhové filtry:</span><span class="sxs-lookup"><span data-stu-id="b0a84-110">A plan filter is set up that includes items A, B, and C. Master planning runs are then run for the same plan, but different runtime filters are applied:</span></span>

- <span data-ttu-id="b0a84-111">**Běhový filtr, který zahrnuje položku D:** žádné položky nejsou plánovány, protože mezi filtrem plánu a běhovým filtrem nejsou žádné průniky.</span><span class="sxs-lookup"><span data-stu-id="b0a84-111">**Runtime filter that includes item D:** No items are planned, because there is no intersection between the plan filter and the runtime filter.</span></span>
- <span data-ttu-id="b0a84-112">**Běhový filtr který zahrnuje položky A a D**: v běhu plánování je zahrnuta pouze položka A, protože položka D není součástí filtru plánu.</span><span class="sxs-lookup"><span data-stu-id="b0a84-112">**Runtime filter that includes item A and D:** Only item A is included in the planning run, because item D isn't part of the plan filter.</span></span>
- <span data-ttu-id="b0a84-113">**Běhový filtr který zahrnuje položku B**: v běhu plánování je zahrnuta pouze položka B a je zachován předchozí výstup plánování pro položku A.</span><span class="sxs-lookup"><span data-stu-id="b0a84-113">**Runtime filter that includes item B:** Only item B is included in the planning run, and the previous planning output for item A is kept.</span></span>
- <span data-ttu-id="b0a84-114">**Běhový filtr, který zahrnuje všechny položky (prázdný filtr):** položky a, B a C jsou zahrnuty do spuštění plánování a předchozí výstup plánování pro položky A a B bude přepsán.</span><span class="sxs-lookup"><span data-stu-id="b0a84-114">**Runtime filter that includes all items (blank filter):** Items A, B, and C are included in the planning run, and the previous planning output for items A and B is overwritten.</span></span>

> [!NOTE]
> <span data-ttu-id="b0a84-115">Neměli byste nastavovat filtr plánu v plánu, který je vybrán jako **Aktuální dynamický hlavní plán** na stránce **parametry hlavního plánování**.</span><span class="sxs-lookup"><span data-stu-id="b0a84-115">You should avoid setting a plan filter on the plan that is selected as **Current dynamic master plan** on the **Master planning parameters** page.</span></span> <span data-ttu-id="b0a84-116">V opačném případě bude funkce dynamického hlavního plánu omezena na filtrované položky.</span><span class="sxs-lookup"><span data-stu-id="b0a84-116">Otherwise, the dynamic master plan functionality will be limited to the filtered items.</span></span> <span data-ttu-id="b0a84-117">Jsou-li například aktualizovány požadavky netto pro položku, která není součástí filtru plánu, nebudou vygenerovány žádné výsledky.</span><span class="sxs-lookup"><span data-stu-id="b0a84-117">For example, if the net requirements are updated for an item that isn't part of the plan filter, no result will be generated.</span></span>

## <a name="related-resources"></a><span data-ttu-id="b0a84-118">Související prostředky</span><span class="sxs-lookup"><span data-stu-id="b0a84-118">Related resources</span></span>

[<span data-ttu-id="b0a84-119">Přehled optimalizace plánování</span><span class="sxs-lookup"><span data-stu-id="b0a84-119">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="b0a84-120">Začínáme s optimalizací plánování</span><span class="sxs-lookup"><span data-stu-id="b0a84-120">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="b0a84-121">Analýza přizpůsobení pro optimalizaci plánování</span><span class="sxs-lookup"><span data-stu-id="b0a84-121">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="b0a84-122">Zobrazení historie plánu a protokolů plánování</span><span class="sxs-lookup"><span data-stu-id="b0a84-122">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="b0a84-123">Zrušení úlohy plánování</span><span class="sxs-lookup"><span data-stu-id="b0a84-123">Cancel a planning job</span></span>](cancel-planning-job.md)
