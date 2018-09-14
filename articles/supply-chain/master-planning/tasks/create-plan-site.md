--- 
title: "Vytvoření plánu pro pracoviště"
description: "Plánovač výroby vypočítá požadovaný materiál a kapacitu pro výrobu určité položky."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqTransPOUrgentFormPart, SysQueryForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: f34d694171e690354721c87f07aa81e811ecdfdc
ms.contentlocale: cs-cz
ms.lasthandoff: 09/14/2018

---
# <a name="create-a-plan-for-a-site"></a><span data-ttu-id="ee32f-103">Vytvoření plánu pro pracoviště</span><span class="sxs-lookup"><span data-stu-id="ee32f-103">Create a plan for a site</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ee32f-104">Plánovač výroby vypočítá požadovaný materiál a kapacitu pro výrobu určité položky.</span><span class="sxs-lookup"><span data-stu-id="ee32f-104">The production planner calculates the material and capacity requirements for the production of a specific item.</span></span> <span data-ttu-id="ee32f-105">Po vytvoření zdrojových návrhy poté vyhledá objednávky pro pracoviště, pro které realizuje plánování a potvrdí objednávky počínaje od těch nejnaléhavějších.</span><span class="sxs-lookup"><span data-stu-id="ee32f-105">After the sourcing suggestions are created, he finds the orders at the site for which he is planning and firms the orders, starting from the urgent ones.</span></span> <span data-ttu-id="ee32f-106">Nejvíce naléhavé objednávky jsou ty, které je třeba potvrdit k aktuálnímu datu.</span><span class="sxs-lookup"><span data-stu-id="ee32f-106">The most urgent orders are the ones that need to be firmed on the current date.</span></span> <span data-ttu-id="ee32f-107">Pro tyto úkoly použijte ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="ee32f-107">Use the demo data company USMF to perform these tasks.</span></span>


## <a name="create-a-materials-and-capacity-plan-for-an-item"></a><span data-ttu-id="ee32f-108">Vytváření materiálů a plánu kapacity pro položku</span><span class="sxs-lookup"><span data-stu-id="ee32f-108">Create a materials and capacity plan for an item</span></span>
1. <span data-ttu-id="ee32f-109">Klikněte na Hlavní plánování.</span><span class="sxs-lookup"><span data-stu-id="ee32f-109">Click Master planning.</span></span>
    * <span data-ttu-id="ee32f-110">Je nutné přejít na výchozí řídicí panel.</span><span class="sxs-lookup"><span data-stu-id="ee32f-110">You need to navigate to the default Dashboard.</span></span>  
2. <span data-ttu-id="ee32f-111">Klikněte na položku Spustit.</span><span class="sxs-lookup"><span data-stu-id="ee32f-111">Click Run.</span></span>
3. <span data-ttu-id="ee32f-112">Rozbalte oddíl Záznamy k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="ee32f-112">Expand the Records to include section.</span></span>
4. <span data-ttu-id="ee32f-113">Klepněte na tlačítko Filtr.</span><span class="sxs-lookup"><span data-stu-id="ee32f-113">Click Filter.</span></span>
5. <span data-ttu-id="ee32f-114">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="ee32f-114">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="ee32f-115">Zadejte hodnotu do pole Kritéria.</span><span class="sxs-lookup"><span data-stu-id="ee32f-115">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="ee32f-116">Příklad: D0001</span><span class="sxs-lookup"><span data-stu-id="ee32f-116">Example: D0001</span></span>  
7. <span data-ttu-id="ee32f-117">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="ee32f-117">Click OK.</span></span>
8. <span data-ttu-id="ee32f-118">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="ee32f-118">Click OK.</span></span>
    * <span data-ttu-id="ee32f-119">Tento proces může trvat několik minut.</span><span class="sxs-lookup"><span data-stu-id="ee32f-119">This may take a few minutes.</span></span>  
9. <span data-ttu-id="ee32f-120">Aktualizujte stránku.</span><span class="sxs-lookup"><span data-stu-id="ee32f-120">Refresh the page.</span></span>

## <a name="identify-the-urgent-planned-orders-for-the-item"></a><span data-ttu-id="ee32f-121">Identifikace naléhavých plánovaných objednávek pro položku</span><span class="sxs-lookup"><span data-stu-id="ee32f-121">Identify the urgent planned orders for the item</span></span>
1. <span data-ttu-id="ee32f-122">Otevřete filtrování sloupce s číslem položky.</span><span class="sxs-lookup"><span data-stu-id="ee32f-122">Open Item number column filter.</span></span>
2. <span data-ttu-id="ee32f-123">Použijte filtr v poli Číslo položky, s hodnotou D0001 a za použití operátoru filtru "začíná".</span><span class="sxs-lookup"><span data-stu-id="ee32f-123">Apply a filter on the "Item number" field, with a value of "D0001", using the "begins with" filter operator.</span></span>
3. <span data-ttu-id="ee32f-124">Otevřete filtr sloupce Datum objednávky.</span><span class="sxs-lookup"><span data-stu-id="ee32f-124">Open Order date column filter.</span></span>
4. <span data-ttu-id="ee32f-125">Použijte filtr v poli "Datum objednávky" s hodnotou aktuálního data za pomoci operátoru filtru "je přesně".</span><span class="sxs-lookup"><span data-stu-id="ee32f-125">Apply a filter on the "Order date" field, with a value of current date, using the "is exactly" filter operator.</span></span>

## <a name="firm-all-the-urgent-orders-for-the-item"></a><span data-ttu-id="ee32f-126">Potvrzení všech naléhavých objednávek pro položku</span><span class="sxs-lookup"><span data-stu-id="ee32f-126">Firm all the urgent orders for the item</span></span>
1. <span data-ttu-id="ee32f-127">V seznamu označte všechny řádky nebo jejich označení zrušte.</span><span class="sxs-lookup"><span data-stu-id="ee32f-127">In the list, mark or unmark all rows.</span></span>
2. <span data-ttu-id="ee32f-128">Klikněte na položku Potvrdit.</span><span class="sxs-lookup"><span data-stu-id="ee32f-128">Click Firm.</span></span>
3. <span data-ttu-id="ee32f-129">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="ee32f-129">Click OK.</span></span>


