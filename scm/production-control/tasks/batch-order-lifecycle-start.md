--- 
title: "Životní cyklus dávkové objednávky od vytvoření po spuštění"
description: "Tento proces vás provede první částí životního cyklu dávkové objednávky."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 418bf29aff3ff03455b4be150409fc9b55e965c9
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---
# <a name="batch-order-lifecycle-from-create-to-start"></a><span data-ttu-id="47337-103">Životní cyklus dávkové objednávky od vytvoření po spuštění</span><span class="sxs-lookup"><span data-stu-id="47337-103">Batch order lifecycle from create to start</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="47337-104">Tento proces vás provede první částí životního cyklu dávkové objednávky.</span><span class="sxs-lookup"><span data-stu-id="47337-104">This procedure takes you through the first part of the life cycle of a batch order.</span></span>

<span data-ttu-id="47337-105">Z vytvoření, odhadu ceny a ukončení plánování výrobní úlohy k vlastnímu spuštění dávkové objednávky.</span><span class="sxs-lookup"><span data-stu-id="47337-105">From creation, cost estimation, and over production job scheduling to the actual start of a batch order.</span></span>



<span data-ttu-id="47337-106">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="47337-106">The demo data company used to create this procedure is USMF.</span></span> 



<span data-ttu-id="47337-107">Předpoklady pro spuštění procedury s jinou sadou dat je uvolněný produkt s aktivní verzí receptury a postupu.</span><span class="sxs-lookup"><span data-stu-id="47337-107">The prerequisites for running the procedure with another dataset are a released product with an active formula and route version.</span></span>


## <a name="create-a-batch-order"></a><span data-ttu-id="47337-108">Vytvoření dávkové objednávky</span><span class="sxs-lookup"><span data-stu-id="47337-108">Create a batch order</span></span>
1. <span data-ttu-id="47337-109">Přejděte na možnost Všechny výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="47337-109">Go to All production orders.</span></span>
2. <span data-ttu-id="47337-110">Klikněte na možnost Nová dávková objednávka.</span><span class="sxs-lookup"><span data-stu-id="47337-110">Click New batch order.</span></span>
3. <span data-ttu-id="47337-111">V poli Číslo zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="47337-111">In the Item number field, enter or select a value.</span></span>
4. <span data-ttu-id="47337-112">Klepněte na volbu Nový.</span><span class="sxs-lookup"><span data-stu-id="47337-112">Click Create.</span></span>
5. <span data-ttu-id="47337-113">Použijte rychlý filtr k filtrování v poli Výroba s hodnotou „b“.</span><span class="sxs-lookup"><span data-stu-id="47337-113">Use the Quick Filter to filter on the Production field with a value of 'b'.</span></span>

## <a name="view-production-formula-and-expected-co-products"></a><span data-ttu-id="47337-114">Zobrazení výrobní receptury a očekávaných souběžných produktů</span><span class="sxs-lookup"><span data-stu-id="47337-114">View production formula and expected co-products</span></span>
1. <span data-ttu-id="47337-115">V podokně akcí klikněte na položku Výrobní zakázka.</span><span class="sxs-lookup"><span data-stu-id="47337-115">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="47337-116">Klepněte na možnost Receptura.</span><span class="sxs-lookup"><span data-stu-id="47337-116">Click Formula.</span></span>
3. <span data-ttu-id="47337-117">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="47337-117">Close the page.</span></span>
4. <span data-ttu-id="47337-118">Klepněte na možnost Souběžné produkty.</span><span class="sxs-lookup"><span data-stu-id="47337-118">Click Co-products.</span></span>
5. <span data-ttu-id="47337-119">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="47337-119">Close the page.</span></span>

## <a name="estimate-the-batch-order"></a><span data-ttu-id="47337-120">Odhad dávkové objednávky</span><span class="sxs-lookup"><span data-stu-id="47337-120">Estimate the batch order</span></span>
1. <span data-ttu-id="47337-121">Klepněte na Odhad.</span><span class="sxs-lookup"><span data-stu-id="47337-121">Click Estimate.</span></span>
2. <span data-ttu-id="47337-122">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="47337-122">Click OK.</span></span>
3. <span data-ttu-id="47337-123">V podokně akcí klikněte na možnost Spravovat náklady.</span><span class="sxs-lookup"><span data-stu-id="47337-123">On the Action Pane, click Manage costs.</span></span>
4. <span data-ttu-id="47337-124">Klepněte na Zobrazit podrobnosti výpočtu.</span><span class="sxs-lookup"><span data-stu-id="47337-124">Click View calculation details.</span></span>
5. <span data-ttu-id="47337-125">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="47337-125">Close the page.</span></span>

## <a name="release-the-batch-order"></a><span data-ttu-id="47337-126">Uvolnění dávkové objednávky</span><span class="sxs-lookup"><span data-stu-id="47337-126">Release the batch order</span></span>
1. <span data-ttu-id="47337-127">V podokně akcí klikněte na položku Výrobní zakázka.</span><span class="sxs-lookup"><span data-stu-id="47337-127">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="47337-128">Klikněte na položku Uvolnit.</span><span class="sxs-lookup"><span data-stu-id="47337-128">Click Release.</span></span>
3. <span data-ttu-id="47337-129">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="47337-129">Click OK.</span></span>

## <a name="schedule-production-jobs"></a><span data-ttu-id="47337-130">Úlohy plánu výroby</span><span class="sxs-lookup"><span data-stu-id="47337-130">Schedule production jobs</span></span>
1. <span data-ttu-id="47337-131">V podokně akcí klikněte na možnost Plán.</span><span class="sxs-lookup"><span data-stu-id="47337-131">On the Action Pane, click Schedule.</span></span>
2. <span data-ttu-id="47337-132">Klikněte na Plánovat úlohy.</span><span class="sxs-lookup"><span data-stu-id="47337-132">Click Schedule jobs.</span></span>
3. <span data-ttu-id="47337-133">Vyberte Ne v poli Omezená kapacita.</span><span class="sxs-lookup"><span data-stu-id="47337-133">Select No in the Finite capacity field.</span></span>
4. <span data-ttu-id="47337-134">Vyberte Ne v poli Omezený materiál.</span><span class="sxs-lookup"><span data-stu-id="47337-134">Select No in the Finite material field.</span></span>
5. <span data-ttu-id="47337-135">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="47337-135">Click OK.</span></span>
6. <span data-ttu-id="47337-136">V podokně akcí klikněte na položku Výrobní zakázka.</span><span class="sxs-lookup"><span data-stu-id="47337-136">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="47337-137">Klikněte na Všechny úlohy.</span><span class="sxs-lookup"><span data-stu-id="47337-137">Click All jobs.</span></span>
8. <span data-ttu-id="47337-138">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="47337-138">Close the page.</span></span>

## <a name="start-the-batch-order"></a><span data-ttu-id="47337-139">Spuštění dávkové objednávky</span><span class="sxs-lookup"><span data-stu-id="47337-139">Start the batch order</span></span>
1. <span data-ttu-id="47337-140">Klikněte na položku Spustit.</span><span class="sxs-lookup"><span data-stu-id="47337-140">Click Start.</span></span>
2. <span data-ttu-id="47337-141">Klikněte na záložku Obecné.</span><span class="sxs-lookup"><span data-stu-id="47337-141">Click the General tab.</span></span>
3. <span data-ttu-id="47337-142">V poli Zaúčtovat výdejku vyberte možnost Ne.</span><span class="sxs-lookup"><span data-stu-id="47337-142">Select No in the Post picking list now field.</span></span>
4. <span data-ttu-id="47337-143">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="47337-143">Click OK.</span></span>
5. <span data-ttu-id="47337-144">V podokně akcí klikněte na možnost Zobrazit.</span><span class="sxs-lookup"><span data-stu-id="47337-144">On the Action Pane, click View.</span></span>
6. <span data-ttu-id="47337-145">Klepněte na Výdejka.</span><span class="sxs-lookup"><span data-stu-id="47337-145">Click Picking list.</span></span>
7. <span data-ttu-id="47337-146">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="47337-146">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="47337-147">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="47337-147">Close the page.</span></span>
9. <span data-ttu-id="47337-148">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="47337-148">Close the page.</span></span>
10. <span data-ttu-id="47337-149">Klepněte na Karta postupu.</span><span class="sxs-lookup"><span data-stu-id="47337-149">Click Route card.</span></span>
11. <span data-ttu-id="47337-150">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="47337-150">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="47337-151">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="47337-151">Close the page.</span></span>
13. <span data-ttu-id="47337-152">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="47337-152">Close the page.</span></span>


