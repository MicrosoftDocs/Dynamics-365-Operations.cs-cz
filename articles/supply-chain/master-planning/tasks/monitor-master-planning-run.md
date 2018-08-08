--- 
title: "Sledování běhu hlavního plánování"
description: "Plánovač výroby chce vědět, zda probíhá hlavní plánování."
author: ShylaThompson
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 94a78d79d86cd480528e96bde70b84f870e0e59c
ms.contentlocale: cs-cz
ms.lasthandoff: 08/07/2018

---
# <a name="monitor-a-master-planning-run"></a><span data-ttu-id="14a58-103">Sledování běhu hlavního plánování</span><span class="sxs-lookup"><span data-stu-id="14a58-103">Monitor a master planning run</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="14a58-104">Plánovač výroby chce vědět, zda probíhá hlavní plánování.</span><span class="sxs-lookup"><span data-stu-id="14a58-104">The production planner wants to see if a master planning run is in progress.</span></span> <span data-ttu-id="14a58-105">K dokončení tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="14a58-105">Use the demo data company USMF to complete this procedure.</span></span>


## <a name="run-master-planning"></a><span data-ttu-id="14a58-106">Spuštění hlavního plánování</span><span class="sxs-lookup"><span data-stu-id="14a58-106">Run master planning</span></span>
1. <span data-ttu-id="14a58-107">Klikněte na Hlavní plánování.</span><span class="sxs-lookup"><span data-stu-id="14a58-107">Click Master planning.</span></span>
    * <span data-ttu-id="14a58-108">Tento údaj naleznete na výchozím řídicím panelu.</span><span class="sxs-lookup"><span data-stu-id="14a58-108">You'll find this on the default dashboard.</span></span>  
2. <span data-ttu-id="14a58-109">V poli Plán zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="14a58-109">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="14a58-110">Příklad: Statický plán</span><span class="sxs-lookup"><span data-stu-id="14a58-110">Example: StaticPlan</span></span>  
3. <span data-ttu-id="14a58-111">Klikněte na položku Spustit.</span><span class="sxs-lookup"><span data-stu-id="14a58-111">Click Run.</span></span>
4. <span data-ttu-id="14a58-112">V poli Sledovat čas zpracování vyberte hodnotu Ano.</span><span class="sxs-lookup"><span data-stu-id="14a58-112">Select Yes in the Track processing time field.</span></span>
    * <span data-ttu-id="14a58-113">Pokud již je políčko zaškrtnuto, tento krok vynechejte.</span><span class="sxs-lookup"><span data-stu-id="14a58-113">If the field is already selected, skip this step.</span></span>  
5. <span data-ttu-id="14a58-114">Do pole Počet vláken zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="14a58-114">In the Number of threads field, enter a number.</span></span>
6. <span data-ttu-id="14a58-115">Rozbalte oddíl Záznamy k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="14a58-115">Expand the Records to include section.</span></span>
7. <span data-ttu-id="14a58-116">Klepněte na tlačítko Filtr.</span><span class="sxs-lookup"><span data-stu-id="14a58-116">Click Filter.</span></span>
8. <span data-ttu-id="14a58-117">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="14a58-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="14a58-118">Označte řádek, kde Pole = Číslo položky.</span><span class="sxs-lookup"><span data-stu-id="14a58-118">Mark the row where Field = Item number.</span></span>  
9. <span data-ttu-id="14a58-119">V poli Kritéria zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="14a58-119">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="14a58-120">Příklad: T0001</span><span class="sxs-lookup"><span data-stu-id="14a58-120">Example: T0001</span></span>  
10. <span data-ttu-id="14a58-121">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="14a58-121">Click OK.</span></span>
11. <span data-ttu-id="14a58-122">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="14a58-122">Click OK.</span></span>

## <a name="monitor-the-master-planning-run"></a><span data-ttu-id="14a58-123">Sledování běhu hlavního plánování</span><span class="sxs-lookup"><span data-stu-id="14a58-123">Monitor the master planning run</span></span>
1. <span data-ttu-id="14a58-124">Klepněte na tlačítko Historie.</span><span class="sxs-lookup"><span data-stu-id="14a58-124">Click History.</span></span>
2. <span data-ttu-id="14a58-125">Klepněte na možnost Dotazy.</span><span class="sxs-lookup"><span data-stu-id="14a58-125">Click Inquiries.</span></span>
3. <span data-ttu-id="14a58-126">Klikněte na Doba trvání zpracování úkolu.</span><span class="sxs-lookup"><span data-stu-id="14a58-126">Click Process task duration.</span></span>
4. <span data-ttu-id="14a58-127">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="14a58-127">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="14a58-128">Pro každou položku můžete získat přehled o době potřebné k dokončení jednotlivých kroků plánování.</span><span class="sxs-lookup"><span data-stu-id="14a58-128">For each item you can get an overview of how long it took to complete each planning step.</span></span>  


