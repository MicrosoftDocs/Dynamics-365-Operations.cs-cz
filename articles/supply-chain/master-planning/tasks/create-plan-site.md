---
title: Vytvoření plánu pro pracoviště
description: Plánovač výroby vypočítá požadovaný materiál a kapacitu pro výrobu určité položky.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqTransPOUrgentFormPart, SysQueryForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bf3016e289248acafc3bc6b79d853fd9de8c5417
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5841640"
---
# <a name="create-a-plan-for-a-site"></a><span data-ttu-id="98306-103">Vytvoření plánu pro pracoviště</span><span class="sxs-lookup"><span data-stu-id="98306-103">Create a plan for a site</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="98306-104">Plánovač výroby vypočítá požadovaný materiál a kapacitu pro výrobu určité položky.</span><span class="sxs-lookup"><span data-stu-id="98306-104">The production planner calculates the material and capacity requirements for the production of a specific item.</span></span> <span data-ttu-id="98306-105">Po vytvoření zdrojových návrhy poté vyhledá objednávky pro pracoviště, pro které realizuje plánování a potvrdí objednávky počínaje od těch nejnaléhavějších.</span><span class="sxs-lookup"><span data-stu-id="98306-105">After the sourcing suggestions are created, he finds the orders at the site for which he is planning and firms the orders, starting from the urgent ones.</span></span> <span data-ttu-id="98306-106">Nejvíce naléhavé objednávky jsou ty, které je třeba potvrdit k aktuálnímu datu.</span><span class="sxs-lookup"><span data-stu-id="98306-106">The most urgent orders are the ones that need to be firmed on the current date.</span></span> <span data-ttu-id="98306-107">Pro tyto úkoly použijte ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="98306-107">Use the demo data company USMF to perform these tasks.</span></span>


## <a name="create-a-materials-and-capacity-plan-for-an-item"></a><span data-ttu-id="98306-108">Vytváření materiálů a plánu kapacity pro položku</span><span class="sxs-lookup"><span data-stu-id="98306-108">Create a materials and capacity plan for an item</span></span>
1. <span data-ttu-id="98306-109">Klikněte na Hlavní plánování.</span><span class="sxs-lookup"><span data-stu-id="98306-109">Click Master planning.</span></span>
    * <span data-ttu-id="98306-110">Je nutné přejít na výchozí řídicí panel.</span><span class="sxs-lookup"><span data-stu-id="98306-110">You need to navigate to the default Dashboard.</span></span>  
2. <span data-ttu-id="98306-111">Klikněte na položku Spustit.</span><span class="sxs-lookup"><span data-stu-id="98306-111">Click Run.</span></span>
3. <span data-ttu-id="98306-112">Rozbalte oddíl Záznamy k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="98306-112">Expand the Records to include section.</span></span>
4. <span data-ttu-id="98306-113">Klepněte na tlačítko Filtr.</span><span class="sxs-lookup"><span data-stu-id="98306-113">Click Filter.</span></span>
5. <span data-ttu-id="98306-114">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="98306-114">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="98306-115">Zadejte hodnotu do pole Kritéria.</span><span class="sxs-lookup"><span data-stu-id="98306-115">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="98306-116">Příklad: D0001</span><span class="sxs-lookup"><span data-stu-id="98306-116">Example: D0001</span></span>  
7. <span data-ttu-id="98306-117">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="98306-117">Click OK.</span></span>
8. <span data-ttu-id="98306-118">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="98306-118">Click OK.</span></span>
    * <span data-ttu-id="98306-119">Tento proces může trvat několik minut.</span><span class="sxs-lookup"><span data-stu-id="98306-119">This may take a few minutes.</span></span>  
9. <span data-ttu-id="98306-120">Aktualizujte stránku.</span><span class="sxs-lookup"><span data-stu-id="98306-120">Refresh the page.</span></span>

## <a name="identify-the-urgent-planned-orders-for-the-item"></a><span data-ttu-id="98306-121">Identifikace naléhavých plánovaných objednávek pro položku</span><span class="sxs-lookup"><span data-stu-id="98306-121">Identify the urgent planned orders for the item</span></span>
1. <span data-ttu-id="98306-122">Otevřete filtrování sloupce s číslem položky.</span><span class="sxs-lookup"><span data-stu-id="98306-122">Open Item number column filter.</span></span>
2. <span data-ttu-id="98306-123">Použijte filtr v poli Číslo položky, s hodnotou D0001 a za použití operátoru filtru "začíná".</span><span class="sxs-lookup"><span data-stu-id="98306-123">Apply a filter on the "Item number" field, with a value of "D0001", using the "begins with" filter operator.</span></span>
3. <span data-ttu-id="98306-124">Otevřete filtr sloupce Datum objednávky.</span><span class="sxs-lookup"><span data-stu-id="98306-124">Open Order date column filter.</span></span>
4. <span data-ttu-id="98306-125">Použijte filtr v poli "Datum objednávky" s hodnotou aktuálního data za pomoci operátoru filtru "je přesně".</span><span class="sxs-lookup"><span data-stu-id="98306-125">Apply a filter on the "Order date" field, with a value of current date, using the "is exactly" filter operator.</span></span>

## <a name="firm-all-the-urgent-orders-for-the-item"></a><span data-ttu-id="98306-126">Potvrzení všech naléhavých objednávek pro položku</span><span class="sxs-lookup"><span data-stu-id="98306-126">Firm all the urgent orders for the item</span></span>
1. <span data-ttu-id="98306-127">V seznamu označte všechny řádky nebo jejich označení zrušte.</span><span class="sxs-lookup"><span data-stu-id="98306-127">In the list, mark or unmark all rows.</span></span>
2. <span data-ttu-id="98306-128">Klikněte na položku Potvrdit.</span><span class="sxs-lookup"><span data-stu-id="98306-128">Click Firm.</span></span>
3. <span data-ttu-id="98306-129">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="98306-129">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]