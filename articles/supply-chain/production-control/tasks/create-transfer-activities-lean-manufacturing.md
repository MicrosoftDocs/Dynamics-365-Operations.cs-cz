--- 
title: "Vytváření aktivit převodu pro lean manufacturing"
description: "Vytvořte aktivitu převodu pro lean manufacturing."
author: cvocph
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 7fed5129a963d4c911ffe0b007dce342837ebb65
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---
# <a name="create-transfer-activities-for-lean-manufacturing"></a><span data-ttu-id="0183a-103">Vytváření aktivit převodu pro lean manufacturing</span><span class="sxs-lookup"><span data-stu-id="0183a-103">Create transfer activities for lean manufacturing</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0183a-104">Vytvořte aktivitu převodu pro lean manufacturing.</span><span class="sxs-lookup"><span data-stu-id="0183a-104">Create a transfer activity for lean manufacturing.</span></span> 

<span data-ttu-id="0183a-105">Požadavky:</span><span class="sxs-lookup"><span data-stu-id="0183a-105">Prerequisites:</span></span> 

1. <span data-ttu-id="0183a-106">Je nutné vytvořit výrobní tok a verzi, která není aktivní.</span><span class="sxs-lookup"><span data-stu-id="0183a-106">A production flow and version that is not active must be created.</span></span>

2. <span data-ttu-id="0183a-107">Je nutné pro sklad a umístění vytvořit časový rozsah od a do.</span><span class="sxs-lookup"><span data-stu-id="0183a-107">The from and to warehouse and locations must be created.</span></span> <span data-ttu-id="0183a-108">V případě potřeby by měla být vytvořeno doplňování nebo doplněná pracovní buňka.</span><span class="sxs-lookup"><span data-stu-id="0183a-108">Optionally, the replenishing or the replenished work cell should be created.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="0183a-109">Najděte verzi výrobního toku</span><span class="sxs-lookup"><span data-stu-id="0183a-109">Find the production flow version</span></span>
1. <span data-ttu-id="0183a-110">Přejděte na Řízení výroby > Nastavení > Tok štíhlé výroby > Výrobního toky.</span><span class="sxs-lookup"><span data-stu-id="0183a-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="0183a-111">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="0183a-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0183a-112">Nezapomeňte, že výrobní tok musí mít verzi ve stavu konceptu.</span><span class="sxs-lookup"><span data-stu-id="0183a-112">Note that the production flow must have a version in draft status.</span></span>  
3. <span data-ttu-id="0183a-113">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="0183a-113">In the list, click the link in the selected row.</span></span>

## <a name="create-a-new-activity"></a><span data-ttu-id="0183a-114">Vytvořte novou aktivitu</span><span class="sxs-lookup"><span data-stu-id="0183a-114">Create a new activity</span></span>
1. <span data-ttu-id="0183a-115">Klepněte na aktivity.</span><span class="sxs-lookup"><span data-stu-id="0183a-115">Click Activities.</span></span>
    * <span data-ttu-id="0183a-116">Ujistěte se, že vybraný výrobní tok má verzi v konceptu a tuto verzi vyberte.</span><span class="sxs-lookup"><span data-stu-id="0183a-116">Ensure that the selected production flow has a version in draft and select that version.</span></span>  
2. <span data-ttu-id="0183a-117">Klepněte na Vytvořit novou aktivitu plánu.</span><span class="sxs-lookup"><span data-stu-id="0183a-117">Click Create new plan activity.</span></span>
3. <span data-ttu-id="0183a-118">Klepněte na tlačítko Další.</span><span class="sxs-lookup"><span data-stu-id="0183a-118">Click Next.</span></span>
4. <span data-ttu-id="0183a-119">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="0183a-119">In the Name field, type a value.</span></span>
5. <span data-ttu-id="0183a-120">V poli Aktivita vyberte položku „Převod“.</span><span class="sxs-lookup"><span data-stu-id="0183a-120">In the Activity type field, select 'Transfer'.</span></span>
6. <span data-ttu-id="0183a-121">V poli Množství procesu zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="0183a-121">In the Process quantity field, enter a number.</span></span>
7. <span data-ttu-id="0183a-122">Klepněte na tlačítko Další.</span><span class="sxs-lookup"><span data-stu-id="0183a-122">Click Next.</span></span>

## <a name="select-the-work-cells"></a><span data-ttu-id="0183a-123">Vyberte pracovní buňky</span><span class="sxs-lookup"><span data-stu-id="0183a-123">Select the Work cells</span></span>
1. <span data-ttu-id="0183a-124">V poli Doplňování klepnutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="0183a-124">In the Replenishing field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="0183a-125">Chcete-li používat výstupní místo pracovní buňky jako z umístění v aktivitě převodu, vyberte pracovní buňku.</span><span class="sxs-lookup"><span data-stu-id="0183a-125">To use the work cell output location as the from location in the transfer activity, select a work cell.</span></span> <span data-ttu-id="0183a-126">Totéž lze provést s doplněnou pracovní buňkou, která nastavuje cílové umístění aktivit převodu.</span><span class="sxs-lookup"><span data-stu-id="0183a-126">The same can be done with the replenished work cell, which sets the target location of the transfer activity.</span></span>  
2. <span data-ttu-id="0183a-127">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="0183a-127">In the list, click the link in the selected row.</span></span>

## <a name="define-the-inventory-updates"></a><span data-ttu-id="0183a-128">Definujte aktualizace zásob</span><span class="sxs-lookup"><span data-stu-id="0183a-128">Define the inventory updates</span></span>
1. <span data-ttu-id="0183a-129">Vyberte možnost v poli Typ produktu.</span><span class="sxs-lookup"><span data-stu-id="0183a-129">In the Product type field, select an option.</span></span>
    * <span data-ttu-id="0183a-130">Nezapomeňte, že převod nemění typ produktu.</span><span class="sxs-lookup"><span data-stu-id="0183a-130">Note that a transfer does not change the type of product.</span></span> <span data-ttu-id="0183a-131">Můžete převést hotové výrobky nebo polotovary (převod mezi dvěma aktivitami výrobního toku a případně kanbanového toku).</span><span class="sxs-lookup"><span data-stu-id="0183a-131">You can transfer finished products or semi-finished products (transfer between two activities of a production flow and possibly a kanban flow).</span></span>     <span data-ttu-id="0183a-132">Při převodu hotových výrobků můžete vybrat výdej nebo příjem výsledků ve skladové transakci.</span><span class="sxs-lookup"><span data-stu-id="0183a-132">When transferring finished products, you can select if picking or receiving results in an inventory transaction.</span></span>  

## <a name="define-the-transfer-locations"></a><span data-ttu-id="0183a-133">Definujte umístění převodu</span><span class="sxs-lookup"><span data-stu-id="0183a-133">Define the transfer locations</span></span>
1. <span data-ttu-id="0183a-134">Klepněte na tlačítko Další.</span><span class="sxs-lookup"><span data-stu-id="0183a-134">Click Next.</span></span>
2. <span data-ttu-id="0183a-135">V poli Sklad kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="0183a-135">In the Warehouse field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="0183a-136">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="0183a-136">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="0183a-137">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="0183a-137">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="0183a-138">V poli Umístění kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="0183a-138">In the Location field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="0183a-139">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="0183a-139">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="0183a-140">V poli Dopravce vyberte hodnotu „Přepravce“.</span><span class="sxs-lookup"><span data-stu-id="0183a-140">In the Freighted by field, select 'Shipper'.</span></span>
    * <span data-ttu-id="0183a-141">Možnosti zahrnují: Přepravce – organizace provozující expediční sklad, příjemce – organizace provozující příjem ze skladu, dopravce – dodavatel třetí strany.</span><span class="sxs-lookup"><span data-stu-id="0183a-141">Options include: Shipper - the organization operating the shipping warehouse, Recipient -  the organization operating the receiving warehouse, Carrier - a third party vendor.</span></span> <span data-ttu-id="0183a-142">Pokud pracující organizace je dodavatelem, vyžaduje aktivita převodu smlouvu o subdodavatelství.</span><span class="sxs-lookup"><span data-stu-id="0183a-142">If the operating organization is a vendor, the transfer activity requires a subcontracting agreement.</span></span>  
8. <span data-ttu-id="0183a-143">Klepněte na tlačítko Další.</span><span class="sxs-lookup"><span data-stu-id="0183a-143">Click Next.</span></span>

## <a name="define-the-activity-times"></a><span data-ttu-id="0183a-144">Definujte čas aktivity</span><span class="sxs-lookup"><span data-stu-id="0183a-144">Define the activity times</span></span>
1. <span data-ttu-id="0183a-145">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="0183a-145">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0183a-146">Je požadována definice modulu Runtime.</span><span class="sxs-lookup"><span data-stu-id="0183a-146">The definition of a Runtime is required.</span></span> <span data-ttu-id="0183a-147">Modul Runtime se používá k výpočtu nákladů a doby propustnosti kanbanových úloh.</span><span class="sxs-lookup"><span data-stu-id="0183a-147">The Runtime is used to calculate cost and the throughput times of the kanban jobs.</span></span> <span data-ttu-id="0183a-148">Moduly Runtime nejsou používány k výpočtu vytížení kapacity a spotřeby, což je počítáno podle času cyklu, odvozeného z úlohy verze výrobního toku.</span><span class="sxs-lookup"><span data-stu-id="0183a-148">Runtimes are not used to calculate capacity load and consumption, which is calculated by cycle time, derived from the production flow version task.</span></span>  
2. <span data-ttu-id="0183a-149">Do pole Čas zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="0183a-149">In the Time field, enter a number.</span></span>
3. <span data-ttu-id="0183a-150">Zadejte hodnotu do pole Jednotka.</span><span class="sxs-lookup"><span data-stu-id="0183a-150">In the Unit field, type a value.</span></span>
4. <span data-ttu-id="0183a-151">Vyberte jednotku času.</span><span class="sxs-lookup"><span data-stu-id="0183a-151">Select the Time unit.</span></span>
5. <span data-ttu-id="0183a-152">V poli Podle množství zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="0183a-152">In the Per quantity field, enter a number.</span></span>
6. <span data-ttu-id="0183a-153">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="0183a-153">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0183a-154">Časy čekání jsou volitelné.</span><span class="sxs-lookup"><span data-stu-id="0183a-154">Queue times are optional.</span></span>  
7. <span data-ttu-id="0183a-155">Do pole Čas zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="0183a-155">In the Time field, enter a number.</span></span>
8. <span data-ttu-id="0183a-156">Zadejte hodnotu do pole Jednotka.</span><span class="sxs-lookup"><span data-stu-id="0183a-156">In the Unit field, type a value.</span></span>
9. <span data-ttu-id="0183a-157">Vyberte jednotku času.</span><span class="sxs-lookup"><span data-stu-id="0183a-157">Select the Time unit.</span></span>
10. <span data-ttu-id="0183a-158">V poli Podle množství zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="0183a-158">In the Per quantity field, enter a number.</span></span>
11. <span data-ttu-id="0183a-159">Klepněte na tlačítko Další.</span><span class="sxs-lookup"><span data-stu-id="0183a-159">Click Next.</span></span>
12. <span data-ttu-id="0183a-160">Klepněte na tlačítko Dokončit.</span><span class="sxs-lookup"><span data-stu-id="0183a-160">Click Finish.</span></span>
13. <span data-ttu-id="0183a-161">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="0183a-161">Close the page.</span></span>


