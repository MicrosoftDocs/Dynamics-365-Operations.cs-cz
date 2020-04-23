---
title: Životní cyklus dávkové objednávky od vytvoření po spuštění
description: Tento proces vás provede první částí životního cyklu dávkové objednávky.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdTableCreate, ProdBOM, PmfProdCoBy, ProdParmCostEstimation, ProdCalcTrans, ProdParmRelease, ProdSchedule, ProdRouteJob, ProdParmStartUp, ProdJournalTransBOM, ProdJournalTransRoute
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 16b55726fdb9ab15e74a9f752cac972b80a98de2
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210978"
---
# <a name="batch-order-lifecycle-from-create-to-start"></a><span data-ttu-id="dfa20-103">Životní cyklus dávkové objednávky od vytvoření po spuštění</span><span class="sxs-lookup"><span data-stu-id="dfa20-103">Batch order lifecycle from create to start</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dfa20-104">Tento proces vás provede první částí životního cyklu dávkové objednávky.</span><span class="sxs-lookup"><span data-stu-id="dfa20-104">This procedure takes you through the first part of the life cycle of a batch order.</span></span>

<span data-ttu-id="dfa20-105">Z vytvoření, odhadu ceny a ukončení plánování výrobní úlohy k vlastnímu spuštění dávkové objednávky.</span><span class="sxs-lookup"><span data-stu-id="dfa20-105">From creation, cost estimation, and over production job scheduling to the actual start of a batch order.</span></span>



<span data-ttu-id="dfa20-106">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="dfa20-106">The demo data company used to create this procedure is USMF.</span></span> 



<span data-ttu-id="dfa20-107">Předpoklady pro spuštění procedury s jinou sadou dat je uvolněný produkt s aktivní verzí receptury a postupu.</span><span class="sxs-lookup"><span data-stu-id="dfa20-107">The prerequisites for running the procedure with another dataset are a released product with an active formula and route version.</span></span>


## <a name="create-a-batch-order"></a><span data-ttu-id="dfa20-108">Vytvoření dávkové objednávky</span><span class="sxs-lookup"><span data-stu-id="dfa20-108">Create a batch order</span></span>
1. <span data-ttu-id="dfa20-109">Přejděte na možnost Všechny výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="dfa20-109">Go to All production orders.</span></span>
2. <span data-ttu-id="dfa20-110">Klikněte na možnost Nová dávková objednávka.</span><span class="sxs-lookup"><span data-stu-id="dfa20-110">Click New batch order.</span></span>
3. <span data-ttu-id="dfa20-111">V poli Číslo zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="dfa20-111">In the Item number field, enter or select a value.</span></span>
4. <span data-ttu-id="dfa20-112">Klepněte na volbu Nový.</span><span class="sxs-lookup"><span data-stu-id="dfa20-112">Click Create.</span></span>
5. <span data-ttu-id="dfa20-113">Použijte rychlý filtr k filtrování v poli Výroba s hodnotou „b“.</span><span class="sxs-lookup"><span data-stu-id="dfa20-113">Use the Quick Filter to filter on the Production field with a value of 'b'.</span></span>

## <a name="view-production-formula-and-expected-co-products"></a><span data-ttu-id="dfa20-114">Zobrazení výrobní receptury a očekávaných souběžných produktů</span><span class="sxs-lookup"><span data-stu-id="dfa20-114">View production formula and expected co-products</span></span>
1. <span data-ttu-id="dfa20-115">V podokně akcí klikněte na položku Výrobní zakázka.</span><span class="sxs-lookup"><span data-stu-id="dfa20-115">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="dfa20-116">Klepněte na možnost Receptura.</span><span class="sxs-lookup"><span data-stu-id="dfa20-116">Click Formula.</span></span>
3. <span data-ttu-id="dfa20-117">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="dfa20-117">Close the page.</span></span>
4. <span data-ttu-id="dfa20-118">Klepněte na možnost Souběžné produkty.</span><span class="sxs-lookup"><span data-stu-id="dfa20-118">Click Co-products.</span></span>
5. <span data-ttu-id="dfa20-119">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="dfa20-119">Close the page.</span></span>

## <a name="estimate-the-batch-order"></a><span data-ttu-id="dfa20-120">Odhad dávkové objednávky</span><span class="sxs-lookup"><span data-stu-id="dfa20-120">Estimate the batch order</span></span>
1. <span data-ttu-id="dfa20-121">Klepněte na Odhad.</span><span class="sxs-lookup"><span data-stu-id="dfa20-121">Click Estimate.</span></span>
2. <span data-ttu-id="dfa20-122">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="dfa20-122">Click OK.</span></span>
3. <span data-ttu-id="dfa20-123">V podokně akcí klikněte na možnost Spravovat náklady.</span><span class="sxs-lookup"><span data-stu-id="dfa20-123">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="dfa20-124">Klepněte na Zobrazit podrobnosti výpočtu.</span><span class="sxs-lookup"><span data-stu-id="dfa20-124">Click View calculation details.</span></span>
5. <span data-ttu-id="dfa20-125">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="dfa20-125">Close the page.</span></span>

## <a name="release-the-batch-order"></a><span data-ttu-id="dfa20-126">Uvolnění dávkové objednávky</span><span class="sxs-lookup"><span data-stu-id="dfa20-126">Release the batch order</span></span>
1. <span data-ttu-id="dfa20-127">V podokně akcí klikněte na položku Výrobní zakázka.</span><span class="sxs-lookup"><span data-stu-id="dfa20-127">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="dfa20-128">Klikněte na položku Uvolnit.</span><span class="sxs-lookup"><span data-stu-id="dfa20-128">Click Release.</span></span>
3. <span data-ttu-id="dfa20-129">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="dfa20-129">Click OK.</span></span>

## <a name="schedule-production-jobs"></a><span data-ttu-id="dfa20-130">Úlohy plánu výroby</span><span class="sxs-lookup"><span data-stu-id="dfa20-130">Schedule production jobs</span></span>
1. <span data-ttu-id="dfa20-131">V podokně akcí klikněte na možnost Plán.</span><span class="sxs-lookup"><span data-stu-id="dfa20-131">On the Action Pane, click Schedule.</span></span>
2. <span data-ttu-id="dfa20-132">Klikněte na Plánovat úlohy.</span><span class="sxs-lookup"><span data-stu-id="dfa20-132">Click Schedule jobs.</span></span>
3. <span data-ttu-id="dfa20-133">Vyberte Ne v poli Omezená kapacita.</span><span class="sxs-lookup"><span data-stu-id="dfa20-133">Select No in the Finite capacity field.</span></span>
4. <span data-ttu-id="dfa20-134">Vyberte Ne v poli Omezený materiál.</span><span class="sxs-lookup"><span data-stu-id="dfa20-134">Select No in the Finite material field.</span></span>
5. <span data-ttu-id="dfa20-135">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="dfa20-135">Click OK.</span></span>
6. <span data-ttu-id="dfa20-136">V podokně akcí klikněte na položku Výrobní zakázka.</span><span class="sxs-lookup"><span data-stu-id="dfa20-136">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="dfa20-137">Klikněte na Všechny úlohy.</span><span class="sxs-lookup"><span data-stu-id="dfa20-137">Click All jobs.</span></span>
8. <span data-ttu-id="dfa20-138">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="dfa20-138">Close the page.</span></span>

## <a name="start-the-batch-order"></a><span data-ttu-id="dfa20-139">Spuštění dávkové objednávky</span><span class="sxs-lookup"><span data-stu-id="dfa20-139">Start the batch order</span></span>
1. <span data-ttu-id="dfa20-140">Klikněte na položku Spustit.</span><span class="sxs-lookup"><span data-stu-id="dfa20-140">Click Start.</span></span>
2. <span data-ttu-id="dfa20-141">Klikněte na záložku Obecné.</span><span class="sxs-lookup"><span data-stu-id="dfa20-141">Click the General tab.</span></span>
3. <span data-ttu-id="dfa20-142">V poli Zaúčtovat výdejku vyberte možnost Ne.</span><span class="sxs-lookup"><span data-stu-id="dfa20-142">Select No in the Post picking list now field.</span></span>
4. <span data-ttu-id="dfa20-143">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="dfa20-143">Click OK.</span></span>
5. <span data-ttu-id="dfa20-144">V podokně akcí klikněte na možnost Zobrazit.</span><span class="sxs-lookup"><span data-stu-id="dfa20-144">On the Action Pane, click View.</span></span>
6. <span data-ttu-id="dfa20-145">Klepněte na Výdejka.</span><span class="sxs-lookup"><span data-stu-id="dfa20-145">Click Picking list.</span></span>
7. <span data-ttu-id="dfa20-146">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="dfa20-146">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="dfa20-147">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="dfa20-147">Close the page.</span></span>
9. <span data-ttu-id="dfa20-148">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="dfa20-148">Close the page.</span></span>
10. <span data-ttu-id="dfa20-149">Klepněte na Karta postupu.</span><span class="sxs-lookup"><span data-stu-id="dfa20-149">Click Route card.</span></span>
11. <span data-ttu-id="dfa20-150">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="dfa20-150">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="dfa20-151">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="dfa20-151">Close the page.</span></span>
13. <span data-ttu-id="dfa20-152">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="dfa20-152">Close the page.</span></span>

