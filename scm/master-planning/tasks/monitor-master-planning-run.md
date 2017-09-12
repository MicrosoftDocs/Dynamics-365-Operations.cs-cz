--- 
title: "Sledování běhu hlavního plánování"
description: "Plánovač výroby chce vědět, zda probíhá hlavní plánování."
author: YuyuScheller
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 1e08d9fd3388561563e6fb982416186a652b4ce2
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---
# <a name="monitor-a-master-planning-run"></a><span data-ttu-id="f0581-103">Sledování běhu hlavního plánování</span><span class="sxs-lookup"><span data-stu-id="f0581-103">Monitor a master planning run</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f0581-104">Plánovač výroby chce vědět, zda probíhá hlavní plánování.</span><span class="sxs-lookup"><span data-stu-id="f0581-104">The production planner wants to see if a master planning run is in progress.</span></span> <span data-ttu-id="f0581-105">K dokončení tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="f0581-105">Use the demo data company USMF to complete this procedure.</span></span>


## <a name="run-master-planning"></a><span data-ttu-id="f0581-106">Spuštění hlavního plánování</span><span class="sxs-lookup"><span data-stu-id="f0581-106">Run master planning</span></span>
1. <span data-ttu-id="f0581-107">Klikněte na Hlavní plánování.</span><span class="sxs-lookup"><span data-stu-id="f0581-107">Click Master planning.</span></span>
    * <span data-ttu-id="f0581-108">Tento údaj naleznete na výchozím řídicím panelu.</span><span class="sxs-lookup"><span data-stu-id="f0581-108">You'll find this on the default dashboard.</span></span>  
2. <span data-ttu-id="f0581-109">V poli Plán zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="f0581-109">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="f0581-110">Příklad: Statický plán</span><span class="sxs-lookup"><span data-stu-id="f0581-110">Example: StaticPlan</span></span>  
3. <span data-ttu-id="f0581-111">Klikněte na položku Spustit.</span><span class="sxs-lookup"><span data-stu-id="f0581-111">Click Run.</span></span>
4. <span data-ttu-id="f0581-112">V poli Sledovat čas zpracování vyberte hodnotu Ano.</span><span class="sxs-lookup"><span data-stu-id="f0581-112">Select Yes in the Track processing time field.</span></span>
    * <span data-ttu-id="f0581-113">Pokud již je políčko zaškrtnuto, tento krok vynechejte.</span><span class="sxs-lookup"><span data-stu-id="f0581-113">If the field is already selected, skip this step.</span></span>  
5. <span data-ttu-id="f0581-114">Do pole Počet vláken zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="f0581-114">In the Number of threads field, enter a number.</span></span>
6. <span data-ttu-id="f0581-115">Rozbalte oddíl Záznamy k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="f0581-115">Expand the Records to include section.</span></span>
7. <span data-ttu-id="f0581-116">Klepněte na tlačítko Filtr.</span><span class="sxs-lookup"><span data-stu-id="f0581-116">Click Filter.</span></span>
8. <span data-ttu-id="f0581-117">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="f0581-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="f0581-118">Označte řádek, kde Pole = Číslo položky.</span><span class="sxs-lookup"><span data-stu-id="f0581-118">Mark the row where Field = Item number.</span></span>  
9. <span data-ttu-id="f0581-119">V poli Kritéria zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="f0581-119">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="f0581-120">Příklad: T0001</span><span class="sxs-lookup"><span data-stu-id="f0581-120">Example: T0001</span></span>  
10. <span data-ttu-id="f0581-121">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="f0581-121">Click OK.</span></span>
11. <span data-ttu-id="f0581-122">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="f0581-122">Click OK.</span></span>

## <a name="monitor-the-master-planning-run"></a><span data-ttu-id="f0581-123">Sledování běhu hlavního plánování</span><span class="sxs-lookup"><span data-stu-id="f0581-123">Monitor the master planning run</span></span>
1. <span data-ttu-id="f0581-124">Klepněte na tlačítko Historie.</span><span class="sxs-lookup"><span data-stu-id="f0581-124">Click History.</span></span>
2. <span data-ttu-id="f0581-125">Klepněte na možnost Dotazy.</span><span class="sxs-lookup"><span data-stu-id="f0581-125">Click Inquiries.</span></span>
3. <span data-ttu-id="f0581-126">Klikněte na Doba trvání zpracování úkolu.</span><span class="sxs-lookup"><span data-stu-id="f0581-126">Click Process task duration.</span></span>
4. <span data-ttu-id="f0581-127">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="f0581-127">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f0581-128">Pro každou položku můžete získat přehled o době potřebné k dokončení jednotlivých kroků plánování.</span><span class="sxs-lookup"><span data-stu-id="f0581-128">For each item you can get an overview of how long it took to complete each planning step.</span></span>  


