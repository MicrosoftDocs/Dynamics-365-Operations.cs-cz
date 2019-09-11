---
title: Vygenerování plánu s omezeními
description: Toto téma vysvětluje způsob vytvoření plánu, který bere v úvahu omezení materiálu a kapacity.
author: ShylaThompson
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6b5d37de41fe68845cec3f2285aed2484ac117aa
ms.sourcegitcommit: a368682f9cf3897347d155f1a2d4b33e555cc2c4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/08/2019
ms.locfileid: "1867166"
---
# <a name="generate-a-constrained-plan"></a><span data-ttu-id="97228-103">Vygenerování plánu s omezeními</span><span class="sxs-lookup"><span data-stu-id="97228-103">Generate a constrained plan</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="97228-104">Toto téma vysvětluje způsob vytvoření plánu, který bere v úvahu omezení materiálu a kapacity.</span><span class="sxs-lookup"><span data-stu-id="97228-104">This topic explains how to create a plan that takes into account both material and capacity constraints.</span></span> <span data-ttu-id="97228-105">Plán zajišťuje, aby se výroba nespustila před zajištěním dostupnosti materiálu, a aby nedošlo k přeplnění prostředků.</span><span class="sxs-lookup"><span data-stu-id="97228-105">The plan ensures that manufacturing doesn't start before materials are available and resources are not overbooked.</span></span> 

<span data-ttu-id="97228-106">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="97228-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="97228-107">Tento postup je určen pro plánujícího produkce.</span><span class="sxs-lookup"><span data-stu-id="97228-107">This procedure is intended for the production planner.</span></span>


## <a name="set-up-a-constrained-plan"></a><span data-ttu-id="97228-108">Vytvoření plánu s omezeními</span><span class="sxs-lookup"><span data-stu-id="97228-108">Set up a constrained plan</span></span>
1. <span data-ttu-id="97228-109">Na domovské stránce vyberte pracovní prostor **Hlavní plánování**.</span><span class="sxs-lookup"><span data-stu-id="97228-109">In the home page, select the **Master planning** workspace.</span></span>
2. <span data-ttu-id="97228-110">Vyberte **Hlavní plány** v seznamu odkazů na úplně pravé straně pracovního prostoru.</span><span class="sxs-lookup"><span data-stu-id="97228-110">Select **Master plans** in the list of links on the far right side of the workspace.</span></span>
3. <span data-ttu-id="97228-111">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="97228-111">In the list, find and select the desired record.</span></span> <span data-ttu-id="97228-112">Příklad: **Statický plán**</span><span class="sxs-lookup"><span data-stu-id="97228-112">Example: **StaticPlan**</span></span>  
4. <span data-ttu-id="97228-113">Vyberte **Ano** v poli **Omezená kapacita**.</span><span class="sxs-lookup"><span data-stu-id="97228-113">Select **Yes** in the **Finite capacity** field.</span></span>
5. <span data-ttu-id="97228-114">Do pole **Omezená kapacita – ochranná doba** zadejte `30`.</span><span class="sxs-lookup"><span data-stu-id="97228-114">In the **Finite capacity time fence** field, enter `30`.</span></span>
6. <span data-ttu-id="97228-115">Rozbalte část **Ochranné doby ve dnech**.</span><span class="sxs-lookup"><span data-stu-id="97228-115">Expand the **Time fences in days** section.</span></span>
7. <span data-ttu-id="97228-116">Vyberte **Ano** v poli **Kapacita**.</span><span class="sxs-lookup"><span data-stu-id="97228-116">Select **Yes** in the **Capacity** field.</span></span>
8. <span data-ttu-id="97228-117">V poli **Ochranná doba plánování kapacity (ve dnech)** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="97228-117">In the **Capacity scheduling time fence (days)** field, enter a number.</span></span> <span data-ttu-id="97228-118">Příklad: `60`</span><span class="sxs-lookup"><span data-stu-id="97228-118">Example: `60`</span></span>  
9. <span data-ttu-id="97228-119">Vyberte možnost **Ano** v poli **Vypočtená zpoždění**.</span><span class="sxs-lookup"><span data-stu-id="97228-119">Select **Yes** in the **Calculated delays** field.</span></span>
10. <span data-ttu-id="97228-120">V poli **Vypočítat pevnou ochrannou dobu zpoždění (ve dnech)** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="97228-120">In the **Calculate delays time fence (days)** field, enter a number.</span></span> <span data-ttu-id="97228-121">Příklad: `60`</span><span class="sxs-lookup"><span data-stu-id="97228-121">Example: `60`</span></span> 
11. <span data-ttu-id="97228-122">Rozbalte část **Vypočtená zpoždění**.</span><span class="sxs-lookup"><span data-stu-id="97228-122">Expand the **Calculated delays** section.</span></span>
12. <span data-ttu-id="97228-123">Vyberte **Ano** v poli **Přidat vypočtené zpoždění k požadovanému datu**.</span><span class="sxs-lookup"><span data-stu-id="97228-123">Select **Yes** in all **Add the calculated delay to the requirement date** fields.</span></span>
13. <span data-ttu-id="97228-124">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="97228-124">Close the page.</span></span>

## <a name="create-a-constrained-plan"></a><span data-ttu-id="97228-125">Vytvoření plánu s omezením</span><span class="sxs-lookup"><span data-stu-id="97228-125">Create a constrained plan</span></span>
1. <span data-ttu-id="97228-126">Vyberte **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="97228-126">Select **Run**.</span></span>
2. <span data-ttu-id="97228-127">V poli **Hlavní plán** zadejte nebo vyberte plán, pro který jste nastavili omezení.</span><span class="sxs-lookup"><span data-stu-id="97228-127">In the **Master plan** field, enter or select the plan for which you have set up constraints.</span></span>  
3. <span data-ttu-id="97228-128">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="97228-128">Select **OK**.</span></span>
4. <span data-ttu-id="97228-129">Vyberte **Plánované objednávky**.</span><span class="sxs-lookup"><span data-stu-id="97228-129">Select **Planned orders**.</span></span>

