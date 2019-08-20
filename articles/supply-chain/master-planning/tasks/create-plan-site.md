---
title: Vytvoření plánu pro pracoviště
description: Plánovač výroby vypočítá požadovaný materiál a kapacitu pro výrobu určité položky.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqTransPOUrgentFormPart, SysQueryForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: daa185864052849b2c78d975a7eb02e9697cb618
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845156"
---
# <a name="create-a-plan-for-a-site"></a><span data-ttu-id="6d0d9-103">Vytvoření plánu pro pracoviště</span><span class="sxs-lookup"><span data-stu-id="6d0d9-103">Create a plan for a site</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6d0d9-104">Plánovač výroby vypočítá požadovaný materiál a kapacitu pro výrobu určité položky.</span><span class="sxs-lookup"><span data-stu-id="6d0d9-104">The production planner calculates the material and capacity requirements for the production of a specific item.</span></span> <span data-ttu-id="6d0d9-105">Po vytvoření zdrojových návrhy poté vyhledá objednávky pro pracoviště, pro které realizuje plánování a potvrdí objednávky počínaje od těch nejnaléhavějších.</span><span class="sxs-lookup"><span data-stu-id="6d0d9-105">After the sourcing suggestions are created, he finds the orders at the site for which he is planning and firms the orders, starting from the urgent ones.</span></span> <span data-ttu-id="6d0d9-106">Nejvíce naléhavé objednávky jsou ty, které je třeba potvrdit k aktuálnímu datu.</span><span class="sxs-lookup"><span data-stu-id="6d0d9-106">The most urgent orders are the ones that need to be firmed on the current date.</span></span> <span data-ttu-id="6d0d9-107">Pro tyto úkoly použijte ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="6d0d9-107">Use the demo data company USMF to perform these tasks.</span></span>


## <a name="create-a-materials-and-capacity-plan-for-an-item"></a><span data-ttu-id="6d0d9-108">Vytváření materiálů a plánu kapacity pro položku</span><span class="sxs-lookup"><span data-stu-id="6d0d9-108">Create a materials and capacity plan for an item</span></span>
1. <span data-ttu-id="6d0d9-109">Klikněte na Hlavní plánování.</span><span class="sxs-lookup"><span data-stu-id="6d0d9-109">Click Master planning.</span></span>
    * <span data-ttu-id="6d0d9-110">Je nutné přejít na výchozí řídicí panel.</span><span class="sxs-lookup"><span data-stu-id="6d0d9-110">You need to navigate to the default Dashboard.</span></span>  
2. <span data-ttu-id="6d0d9-111">Klikněte na položku Spustit.</span><span class="sxs-lookup"><span data-stu-id="6d0d9-111">Click Run.</span></span>
3. <span data-ttu-id="6d0d9-112">Rozbalte oddíl Záznamy k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="6d0d9-112">Expand the Records to include section.</span></span>
4. <span data-ttu-id="6d0d9-113">Klepněte na tlačítko Filtr.</span><span class="sxs-lookup"><span data-stu-id="6d0d9-113">Click Filter.</span></span>
5. <span data-ttu-id="6d0d9-114">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="6d0d9-114">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="6d0d9-115">Zadejte hodnotu do pole Kritéria.</span><span class="sxs-lookup"><span data-stu-id="6d0d9-115">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="6d0d9-116">Příklad: D0001</span><span class="sxs-lookup"><span data-stu-id="6d0d9-116">Example: D0001</span></span>  
7. <span data-ttu-id="6d0d9-117">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="6d0d9-117">Click OK.</span></span>
8. <span data-ttu-id="6d0d9-118">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="6d0d9-118">Click OK.</span></span>
    * <span data-ttu-id="6d0d9-119">Tento proces může trvat několik minut.</span><span class="sxs-lookup"><span data-stu-id="6d0d9-119">This may take a few minutes.</span></span>  
9. <span data-ttu-id="6d0d9-120">Aktualizujte stránku.</span><span class="sxs-lookup"><span data-stu-id="6d0d9-120">Refresh the page.</span></span>

## <a name="identify-the-urgent-planned-orders-for-the-item"></a><span data-ttu-id="6d0d9-121">Identifikace naléhavých plánovaných objednávek pro položku</span><span class="sxs-lookup"><span data-stu-id="6d0d9-121">Identify the urgent planned orders for the item</span></span>
1. <span data-ttu-id="6d0d9-122">Otevřete filtrování sloupce s číslem položky.</span><span class="sxs-lookup"><span data-stu-id="6d0d9-122">Open Item number column filter.</span></span>
2. <span data-ttu-id="6d0d9-123">Použijte filtr v poli Číslo položky, s hodnotou D0001 a za použití operátoru filtru "začíná".</span><span class="sxs-lookup"><span data-stu-id="6d0d9-123">Apply a filter on the "Item number" field, with a value of "D0001", using the "begins with" filter operator.</span></span>
3. <span data-ttu-id="6d0d9-124">Otevřete filtr sloupce Datum objednávky.</span><span class="sxs-lookup"><span data-stu-id="6d0d9-124">Open Order date column filter.</span></span>
4. <span data-ttu-id="6d0d9-125">Použijte filtr v poli "Datum objednávky" s hodnotou aktuálního data za pomoci operátoru filtru "je přesně".</span><span class="sxs-lookup"><span data-stu-id="6d0d9-125">Apply a filter on the "Order date" field, with a value of current date, using the "is exactly" filter operator.</span></span>

## <a name="firm-all-the-urgent-orders-for-the-item"></a><span data-ttu-id="6d0d9-126">Potvrzení všech naléhavých objednávek pro položku</span><span class="sxs-lookup"><span data-stu-id="6d0d9-126">Firm all the urgent orders for the item</span></span>
1. <span data-ttu-id="6d0d9-127">V seznamu označte všechny řádky nebo jejich označení zrušte.</span><span class="sxs-lookup"><span data-stu-id="6d0d9-127">In the list, mark or unmark all rows.</span></span>
2. <span data-ttu-id="6d0d9-128">Klikněte na položku Potvrdit.</span><span class="sxs-lookup"><span data-stu-id="6d0d9-128">Click Firm.</span></span>
3. <span data-ttu-id="6d0d9-129">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="6d0d9-129">Click OK.</span></span>

