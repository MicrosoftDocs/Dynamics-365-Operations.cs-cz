---
title: Odhad nákladů výrobní zakázky
description: V tomto článku jsou informace o odhadu výrobních nákladů. Odhad výrobních nákladů poskytuje předpokládané náklady na spotřebu materiálu a kapacity při výrobě položky v plánovaném množství výrobní zakázky.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMCalcTrans, InventCostTrans, ProdCalcTrans, ProdTableJour, ProdTableListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 80633
ms.assetid: b4625d10-c852-4fda-b718-79df458de0d4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 93546fc170757ee2c39144842bae12d78400fd32
ms.sourcegitcommit: 2ebea3cbddfa0a5ef0e0fd13d3693da6152bc288
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/30/2019
ms.locfileid: "350474"
---
# <a name="production-order-cost-estimation"></a><span data-ttu-id="1da0c-104">Odhad nákladů výrobní zakázky</span><span class="sxs-lookup"><span data-stu-id="1da0c-104">Production order cost estimation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1da0c-105">V tomto článku jsou informace o odhadu výrobních nákladů.</span><span class="sxs-lookup"><span data-stu-id="1da0c-105">This article provides information about production cost estimation.</span></span> <span data-ttu-id="1da0c-106">Odhad výrobních nákladů poskytuje předpokládané náklady na spotřebu materiálu a kapacity při výrobě položky v plánovaném množství výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="1da0c-106">Production cost estimation provides the projected material and capacity consumption costs of producing an item in the planned production order quantity.</span></span> 

<span data-ttu-id="1da0c-107">Po vytvoření výrobní zakázky je nutné odhadnout výrobní náklady.</span><span class="sxs-lookup"><span data-stu-id="1da0c-107">After you create a production order, you must estimate production costs.</span></span> <span data-ttu-id="1da0c-108">Účelem je odhad spotřeby položek a postupu pro výrobní proces, protože tyto odhady slouží jako základ následného plánování a výrobních procesů.</span><span class="sxs-lookup"><span data-stu-id="1da0c-108">The purpose is to estimate item and route consumption for the production process, because these estimates are used as the basis for subsequent scheduling and production processes.</span></span>

## <a name="production-cost-estimation"></a><span data-ttu-id="1da0c-109">Odhad výrobních nákladů</span><span class="sxs-lookup"><span data-stu-id="1da0c-109">Production cost estimation</span></span>
<span data-ttu-id="1da0c-110">Odhady výrobních nákladů jsou založeny na následujících informacích:</span><span class="sxs-lookup"><span data-stu-id="1da0c-110">Estimates of production costs are based on the following information:</span></span>

-   <span data-ttu-id="1da0c-111">množství ve výrobní zakázce,</span><span class="sxs-lookup"><span data-stu-id="1da0c-111">The quantity on the production order</span></span>
-   <span data-ttu-id="1da0c-112">součásti ve výrobních kusovnících (BOM),</span><span class="sxs-lookup"><span data-stu-id="1da0c-112">The components on the production bills of materials (BOMs)</span></span>
-   <span data-ttu-id="1da0c-113">operace postupu ve výrobním postupu,</span><span class="sxs-lookup"><span data-stu-id="1da0c-113">The routing operations in the production route</span></span>
-   <span data-ttu-id="1da0c-114">nepřímé náklady, které se týkají součástí a operací,</span><span class="sxs-lookup"><span data-stu-id="1da0c-114">The indirect costs that apply to the components and operations</span></span>
-   <span data-ttu-id="1da0c-115">údaje aktivních nákladů k datu výpočtu.</span><span class="sxs-lookup"><span data-stu-id="1da0c-115">The active cost data as of the calculation date</span></span>

<span data-ttu-id="1da0c-116">Pokud je položka fiktivního řádku ve výrobních kusovnících, budou výpočty odpovídat součástem a operacím postupu fiktivní položky.</span><span class="sxs-lookup"><span data-stu-id="1da0c-116">If there is a phantom line item on the production BOMs, the calculations reflect the phantom’s components and route operations.</span></span> <span data-ttu-id="1da0c-117">Pomocí úlohy odhadu lze přepočítat odhadované náklady, aby odrážely aktualizované údaje.</span><span class="sxs-lookup"><span data-stu-id="1da0c-117">You can use the estimation task to recalculate estimated costs so that they reflect updated information.</span></span> <span data-ttu-id="1da0c-118">Aktualizovanými údaji mohou být například změny v množství výrobní zakázky, komponenty ve výrobních kusovnících, operace ve výrobním postupu, nepřímé náklady, které lze platí pro tyto součásti a operace, nebo údaje aktivních nákladů k datu přepočítání.</span><span class="sxs-lookup"><span data-stu-id="1da0c-118">For example, the updated information might be changes to the quantity on the production order, the components on the production BOMs, the routing operations in the production route, the indirect costs that apply to these components and operations, or the active cost data as of the recalculation date.</span></span> <span data-ttu-id="1da0c-119">Při výpočtech odhadovaných nákladů je také navržena prodejní cena pro výrobní položku na základě přístupu náklady plus přirážka.</span><span class="sxs-lookup"><span data-stu-id="1da0c-119">The calculations of estimated cost also suggest a sales price for the production item, based on a cost-plus-markup approach.</span></span> <span data-ttu-id="1da0c-120">Výpočty odhadovaných nákladů se mohou volitelně týkat referenčních objednávek, které odpovídají jiným výrobním zakázkám připojeným k dané výrobní zakázce.</span><span class="sxs-lookup"><span data-stu-id="1da0c-120">The calculations of estimated cost can optionally apply to reference orders that reflect other production orders that are linked to the production order.</span></span>

## <a name="view-the-estimated-costs"></a><span data-ttu-id="1da0c-121">Zobrazení odhadovaných nákladů</span><span class="sxs-lookup"><span data-stu-id="1da0c-121">View the estimated costs</span></span>
<span data-ttu-id="1da0c-122">Po spuštění odhadu lze výsledky zobrazit na stránce **Kalkulace ceny**.</span><span class="sxs-lookup"><span data-stu-id="1da0c-122">After you run estimation, you can view the results on the **Price calculation** page.</span></span> <span data-ttu-id="1da0c-123">Odhad vypočte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="1da0c-123">The estimation calculates the following values:</span></span>

-   <span data-ttu-id="1da0c-124">**Výrobní náklady**: Výrobní náklady jsou na horním řádku odhadu.</span><span class="sxs-lookup"><span data-stu-id="1da0c-124">**Production cost** – The production cost is the top line of the estimate.</span></span> <span data-ttu-id="1da0c-125">Zobrazuje celkové náklady na spuštění výrobní zakázky a celkovou prodejní cenu produkce.</span><span class="sxs-lookup"><span data-stu-id="1da0c-125">It shows the complete cost of running the production order and the total sales price for the production.</span></span> <span data-ttu-id="1da0c-126">Jedná se o součet všech řádků nákladů v odhadu.</span><span class="sxs-lookup"><span data-stu-id="1da0c-126">It's the sum of all the cost lines on the estimate.</span></span>
-   <span data-ttu-id="1da0c-127">**Náklady na postup nebo prostředek**: Jsou to náklady pro výrobní operace.</span><span class="sxs-lookup"><span data-stu-id="1da0c-127">**Route or resource costs** – Route or resource costs are the costs for the production operations.</span></span> <span data-ttu-id="1da0c-128">Patří mezi ně náklady prvků, jako je například přípravný čas, operační čas a režijní náklady.</span><span class="sxs-lookup"><span data-stu-id="1da0c-128">They include the cost of elements such as setup time, run time, and overhead.</span></span>
-   <span data-ttu-id="1da0c-129">**Náklady na materiál**: Jedná se o náklady a ceny součástí kusovníku vyžadovaných k výrobě položky.</span><span class="sxs-lookup"><span data-stu-id="1da0c-129">**Material costs** – Material costs are the costs and prices of the BOM components that are required in order to produce the item.</span></span> <span data-ttu-id="1da0c-130">Tyto náklady byly zjištěny dříve a zadány do systému.</span><span class="sxs-lookup"><span data-stu-id="1da0c-130">These costs have previously been established and entered into the system.</span></span>

## <a name="other-uses-of-cost-estimation"></a><span data-ttu-id="1da0c-131">Další využití odhadu nákladů</span><span class="sxs-lookup"><span data-stu-id="1da0c-131">Other uses of cost estimation</span></span>
<span data-ttu-id="1da0c-132">Odhad nákladů také poskytuje následující informace:</span><span class="sxs-lookup"><span data-stu-id="1da0c-132">A cost estimate also provides the following information:</span></span>

-   <span data-ttu-id="1da0c-133">smysluplné cenové nabídky,</span><span class="sxs-lookup"><span data-stu-id="1da0c-133">Meaningful price quotations</span></span>
-   <span data-ttu-id="1da0c-134">odhady ziskovosti dané zakázky,</span><span class="sxs-lookup"><span data-stu-id="1da0c-134">Estimates of the profitability of the order</span></span>
-   <span data-ttu-id="1da0c-135">odhady použití surovin,</span><span class="sxs-lookup"><span data-stu-id="1da0c-135">Estimates of raw material usage</span></span>
-   <span data-ttu-id="1da0c-136">porovnání informací o nákladech z předchozí výroby,</span><span class="sxs-lookup"><span data-stu-id="1da0c-136">Comparisons of cost information from previous productions</span></span>
-   <span data-ttu-id="1da0c-137">informace o rozpočtu a prognóze,</span><span class="sxs-lookup"><span data-stu-id="1da0c-137">Budget and forecasting information</span></span>
-   <span data-ttu-id="1da0c-138">odhady objemu výroby vyžadovaného k udržení konkrétních nákladů.</span><span class="sxs-lookup"><span data-stu-id="1da0c-138">Estimates of the production size that is required in order to maintain a particular cost</span></span>




