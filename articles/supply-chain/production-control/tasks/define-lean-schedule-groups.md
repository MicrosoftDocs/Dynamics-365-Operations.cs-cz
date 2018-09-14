--- 
title: "Definování skupin štíhlého plánu"
description: "Skupiny štíhlého plánu jsou definovány pro rozdělení do skupin a rozlišení produkty v plánování kanbanu."
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LeanScheduleGroup, GanttColorTableLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 787694b094f343445cca784d035554a8bfa25f5a
ms.contentlocale: cs-cz
ms.lasthandoff: 09/14/2018

---
# <a name="define-lean-schedule-groups"></a><span data-ttu-id="b131a-103">Definování skupin štíhlého plánu</span><span class="sxs-lookup"><span data-stu-id="b131a-103">Define lean schedule groups</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b131a-104">Skupiny štíhlého plánu jsou definovány pro rozdělení do skupin a rozlišení produkty v plánování kanbanu.</span><span class="sxs-lookup"><span data-stu-id="b131a-104">Lean schedule groups are defined to group and distinguish products in kanban scheduling.</span></span> <span data-ttu-id="b131a-105">Seskupení lze provést jako obecné přidružení společností nebo jako specifické k pracovní buňce.</span><span class="sxs-lookup"><span data-stu-id="b131a-105">The grouping can be done as generic association per company or specific to a work cell.</span></span> <span data-ttu-id="b131a-106">Každá skupina má barevný kód přiřazeny pro vizuální označení na stránce se seznamem plánování kanbanu.</span><span class="sxs-lookup"><span data-stu-id="b131a-106">Each group has a color code assigned for visual indication in the kanban scheduling listpage.</span></span> <span data-ttu-id="b131a-107">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="b131a-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="define-lean-scheduling-group"></a><span data-ttu-id="b131a-108">Definování skupiny štíhlého plánování</span><span class="sxs-lookup"><span data-stu-id="b131a-108">Define lean scheduling group</span></span>
1. <span data-ttu-id="b131a-109">Přejděte k Řízení informací o produktech > Lean manufacturing > Skupiny štíhlého plánu.</span><span class="sxs-lookup"><span data-stu-id="b131a-109">Go to Product information management > Lean manufacturing > Lean schedule groups.</span></span>
2. <span data-ttu-id="b131a-110">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="b131a-110">Click New.</span></span>
3. <span data-ttu-id="b131a-111">Zadejte hodnotu do pole Skupina plánu.</span><span class="sxs-lookup"><span data-stu-id="b131a-111">In the Schedule group field, type a value.</span></span>
    * <span data-ttu-id="b131a-112">Skupina plánu může být definována jako globální skupina nebo specifická pro pracovní buňku.</span><span class="sxs-lookup"><span data-stu-id="b131a-112">A schedule group can be defined as global group or specific to a work cell.</span></span> <span data-ttu-id="b131a-113">V tomto jednoduchém příkladu budeme definovat globální skupinu a pracovní buňka zůstane prázdná.</span><span class="sxs-lookup"><span data-stu-id="b131a-113">In this simple example, we define a global group, and the work cell is kept empty.</span></span> <span data-ttu-id="b131a-114">Nastavení této skupiny se vztahují na všechny pracovní buňky, které nemají konkrétní skupiny plánu.</span><span class="sxs-lookup"><span data-stu-id="b131a-114">The settings of this group apply to all work cells that do not have specific schedule groups.</span></span>  
4. <span data-ttu-id="b131a-115">Z výběr barvy vyberte barvu.</span><span class="sxs-lookup"><span data-stu-id="b131a-115">Select a color from the color selection.</span></span>
    * <span data-ttu-id="b131a-116">Barvy jsou použity k označení úloh na stránce se seznamem kanbanového plánu nebo na kanbanové desce procesu.</span><span class="sxs-lookup"><span data-stu-id="b131a-116">The colors are used to highlight the jobs on the kanban schedule list page or the kanban process board.</span></span>  
5. <span data-ttu-id="b131a-117">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="b131a-117">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="b131a-118">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="b131a-118">In the list, click the link in the selected row.</span></span>

## <a name="associate-product"></a><span data-ttu-id="b131a-119">Přidružení produktu</span><span class="sxs-lookup"><span data-stu-id="b131a-119">Associate product</span></span>
1. <span data-ttu-id="b131a-120">Přidružení specifického produktu</span><span class="sxs-lookup"><span data-stu-id="b131a-120">Associate a specific product</span></span>
    * <span data-ttu-id="b131a-121">Existují dva způsoby přidružení produktů ke skupinám štíhlého plánu, buď jako specifického produktu (typ vztahu položky = zboží), nebo jako části alokačního klíče položky (typ vztahu položky = skupina).</span><span class="sxs-lookup"><span data-stu-id="b131a-121">There are two ways to associate products to lean schedule groups, either as a specific product (Item relation type = Item) or as part of an item allocation key (item relation type = group).</span></span>    
2. <span data-ttu-id="b131a-122">V poli Vztah položky vyberte Položka.</span><span class="sxs-lookup"><span data-stu-id="b131a-122">In the Item relation type field, select Item</span></span>
3. <span data-ttu-id="b131a-123">Zadejte hodnotu do pole Číslo zboží.</span><span class="sxs-lookup"><span data-stu-id="b131a-123">In the Item number field, type a value.</span></span>
4. <span data-ttu-id="b131a-124">V poli Poměr propustnosti zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="b131a-124">In the Throughput ratio field, enter a number.</span></span>
    * <span data-ttu-id="b131a-125">Poměr výchozí propustnosti je 1, což znamená, že související produkty spotřebovávají přesně kapacitu stanovenou v aktivitách procesu výrobních toků.</span><span class="sxs-lookup"><span data-stu-id="b131a-125">The default Throughput ratio is 1, which means that the related products consume exactly the capacity specified in the process activites of the production flows.</span></span> <span data-ttu-id="b131a-126">Poměr propustnosti > 1 definuje vyšší spotřebu prostředků, poměr propustnosti < 1 definuje nižší spotřebu prostředků.</span><span class="sxs-lookup"><span data-stu-id="b131a-126">Throughput ratio > 1 defines a higher resource consumption, Throughput ratio < 1 defines a lower resource consumption.</span></span> <span data-ttu-id="b131a-127">Poměr se používá při výpočtu nákladů a při výpočtu spotřeby kanbanové úlohy.</span><span class="sxs-lookup"><span data-stu-id="b131a-127">The ratio is used in the cost calculation and in the calculation of the kanban job consumption.</span></span>  

## <a name="associate-item-allocation-key"></a><span data-ttu-id="b131a-128">Přiřazení alokačního klíče položky</span><span class="sxs-lookup"><span data-stu-id="b131a-128">Associate item allocation key</span></span>
1. <span data-ttu-id="b131a-129">Přiřazení alokačního klíče položky</span><span class="sxs-lookup"><span data-stu-id="b131a-129">Associate an item allocation key</span></span>
    * <span data-ttu-id="b131a-130">Přidejte přidružení k alokačnímu klíče položky použitím skupiny typ vztahu položky.</span><span class="sxs-lookup"><span data-stu-id="b131a-130">Add an association to an item allocation key by using the Item relation type Group.</span></span>   <span data-ttu-id="b131a-131">Všimněte si, že v tomto postupu je nutné mít ve svých datech definovanou prognózu alokačního klíče položky.</span><span class="sxs-lookup"><span data-stu-id="b131a-131">Note that for this process, you need a forecast item alllocation key defined in your data.</span></span>  
2. <span data-ttu-id="b131a-132">V poli Vztah položky vyberte Skupina.</span><span class="sxs-lookup"><span data-stu-id="b131a-132">In the Item relation type field, select Group</span></span>
3. <span data-ttu-id="b131a-133">V poli Alokační klíč položky klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="b131a-133">In the Item allocation key field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="b131a-134">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="b131a-134">In the list, click the link in the selected row.</span></span>


