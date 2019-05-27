---
title: Vygenerování plánu s omezeními
description: Tento postup popisuje způsob vytvoření plánu, který bere v úvahu omezení materiálu a kapacity.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0e2265f7788fd2a4a37f6fb96d7562649dbc5b1c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1556016"
---
# <a name="generate-a-constrained-plan"></a><span data-ttu-id="4155a-103">Vygenerování plánu s omezeními</span><span class="sxs-lookup"><span data-stu-id="4155a-103">Generate a constrained plan</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4155a-104">Tento postup popisuje způsob vytvoření plánu, který bere v úvahu omezení materiálu a kapacity.</span><span class="sxs-lookup"><span data-stu-id="4155a-104">This procedure shows how to create a plan that takes into account both material and capacity constraints.</span></span> <span data-ttu-id="4155a-105">Plán zajišťuje, aby se výroba nespustila před zajištěním dostupnosti materiálu, a aby nedošlo k přeplnění prostředků.</span><span class="sxs-lookup"><span data-stu-id="4155a-105">The plan ensures that manufacturing doesn't start before materials are available and resources are not overbooked.</span></span> 

<span data-ttu-id="4155a-106">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="4155a-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="4155a-107">Tento postup je určen pro plánujícího produkce.</span><span class="sxs-lookup"><span data-stu-id="4155a-107">This procedure is intended for the production planner.</span></span>


## <a name="set-up-a-constrained-plan"></a><span data-ttu-id="4155a-108">Vytvoření plánu s omezeními</span><span class="sxs-lookup"><span data-stu-id="4155a-108">Set up a constrained plan</span></span>
1. <span data-ttu-id="4155a-109">Klikněte na Hlavní plánování.</span><span class="sxs-lookup"><span data-stu-id="4155a-109">Click Master planning.</span></span>
2. <span data-ttu-id="4155a-110">Klikněte na Hlavní plány.</span><span class="sxs-lookup"><span data-stu-id="4155a-110">Click Master plans.</span></span>
3. <span data-ttu-id="4155a-111">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="4155a-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4155a-112">Příklad: Statický plán</span><span class="sxs-lookup"><span data-stu-id="4155a-112">Example: StaticPlan</span></span>  
4. <span data-ttu-id="4155a-113">Vyberte Ano v poli Omezená kapacita.</span><span class="sxs-lookup"><span data-stu-id="4155a-113">Select Yes in the Finite capacity field.</span></span>
5. <span data-ttu-id="4155a-114">Do pole Omezená kapacita – ochranná doba zadejte 30.</span><span class="sxs-lookup"><span data-stu-id="4155a-114">In the Finite capacity time fence field, enter '30'.</span></span>
6. <span data-ttu-id="4155a-115">Rozbalte část Ochranné doby ve dnech.</span><span class="sxs-lookup"><span data-stu-id="4155a-115">Expand the Time fences in days section.</span></span>
7. <span data-ttu-id="4155a-116">Vyberte Ano v poli Kapacita.</span><span class="sxs-lookup"><span data-stu-id="4155a-116">Select Yes in the Capacity field.</span></span>
8. <span data-ttu-id="4155a-117">V poli Ochranná doba plánování kapacity (ve dnech) zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="4155a-117">In the Capacity scheduling time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="4155a-118">Příklad: 60</span><span class="sxs-lookup"><span data-stu-id="4155a-118">Example: 60</span></span>  
9. <span data-ttu-id="4155a-119">Vyberte možnost Ano v poli Vypočtená zpoždění.</span><span class="sxs-lookup"><span data-stu-id="4155a-119">Select Yes in the Calculated delays field.</span></span>
10. <span data-ttu-id="4155a-120">V poli Vypočítat pevnou ochrannou dobu zpoždění (ve dnech) zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="4155a-120">In the Calculate delays time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="4155a-121">Příklad: 60</span><span class="sxs-lookup"><span data-stu-id="4155a-121">Example: 60</span></span>  
11. <span data-ttu-id="4155a-122">Rozbalte část Vypočtená zpoždění.</span><span class="sxs-lookup"><span data-stu-id="4155a-122">Expand the Calculated delays section.</span></span>
12. <span data-ttu-id="4155a-123">Vyberte Ano v poli Přidat vypočtené zpoždění k požadovanému datu.</span><span class="sxs-lookup"><span data-stu-id="4155a-123">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
13. <span data-ttu-id="4155a-124">Vyberte Ano v poli Přidat vypočtené zpoždění k požadovanému datu.</span><span class="sxs-lookup"><span data-stu-id="4155a-124">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
14. <span data-ttu-id="4155a-125">Vyberte Ano v poli Přidat vypočtené zpoždění k požadovanému datu.</span><span class="sxs-lookup"><span data-stu-id="4155a-125">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
15. <span data-ttu-id="4155a-126">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="4155a-126">Close the page.</span></span>

## <a name="create-a-constrained-plan"></a><span data-ttu-id="4155a-127">Vytvoření plánu s omezením</span><span class="sxs-lookup"><span data-stu-id="4155a-127">Create a constrained plan</span></span>
1. <span data-ttu-id="4155a-128">Klikněte na položku Spustit.</span><span class="sxs-lookup"><span data-stu-id="4155a-128">Click Run.</span></span>
2. <span data-ttu-id="4155a-129">V poli Hlavní plán zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="4155a-129">In the Master plan field, enter or select a value.</span></span>
    * <span data-ttu-id="4155a-130">Vyberte plán, pro který jste nastavili omezení.</span><span class="sxs-lookup"><span data-stu-id="4155a-130">Select the plan for which you have set up constraints.</span></span>  
3. <span data-ttu-id="4155a-131">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="4155a-131">Click OK.</span></span>
    * <span data-ttu-id="4155a-132">Tato operace může chvíli trvat.</span><span class="sxs-lookup"><span data-stu-id="4155a-132">This may take a while.</span></span>  
4. <span data-ttu-id="4155a-133">Klikněte na Plánované objednávky.</span><span class="sxs-lookup"><span data-stu-id="4155a-133">Click Planned orders.</span></span>

