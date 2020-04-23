---
title: Vytvoření plánu dodávek
description: Tento postup ukazuje, jak vytvořit plán dodávek pro prodejní objednávku.
author: omulvad
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesDeliverySchedule, SalesEditLines,  SrsReportViewerForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: af983b30530a7f5d0a82f98deeb12180c42d86cd
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215808"
---
# <a name="create-delivery-schedule"></a><span data-ttu-id="50b95-103">Vytvoření plánu dodávek</span><span class="sxs-lookup"><span data-stu-id="50b95-103">Create delivery schedule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="50b95-104">Tento postup ukazuje, jak vytvořit plán dodávek pro prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="50b95-104">This procedure demonstrates how to create a delivery schedule for a sales order.</span></span> <span data-ttu-id="50b95-105">Plán dodávek se používá, pokud množství z objednávky nebo nabídky má být dodáno v podobě vícenásobné expedice.</span><span class="sxs-lookup"><span data-stu-id="50b95-105">A delivery schedule is used when a quantity on an order or a quotation is requested to be delivered in multiple shipments.</span></span> <span data-ttu-id="50b95-106">Tento postup můžete použít s ukázkovými daty společnosti USMF nebo pomocí vlastních dat.</span><span class="sxs-lookup"><span data-stu-id="50b95-106">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="create-delivery-schedule"></a><span data-ttu-id="50b95-107">Vytvoření plánu dodávek</span><span class="sxs-lookup"><span data-stu-id="50b95-107">Create delivery schedule</span></span>
1. <span data-ttu-id="50b95-108">Přejděte na Všechny prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="50b95-108">Go to All sales orders.</span></span>
2. <span data-ttu-id="50b95-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="50b95-109">Click New.</span></span>
3. <span data-ttu-id="50b95-110">V poli Účet odběratele zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="50b95-110">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="50b95-111">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="50b95-111">Click OK.</span></span>
5. <span data-ttu-id="50b95-112">V poli Číslo zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="50b95-112">In the Item number field, enter or select a value.</span></span>
6. <span data-ttu-id="50b95-113">Do pole Množství zadejte číslo, které je větší než 1.</span><span class="sxs-lookup"><span data-stu-id="50b95-113">In the Quantity field, enter a number that is bigger than 1.</span></span>
7. <span data-ttu-id="50b95-114">Klikněte na položku Řádek prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="50b95-114">Click Sales order line.</span></span>
8. <span data-ttu-id="50b95-115">Klikněte na položku Plán dodávek.</span><span class="sxs-lookup"><span data-stu-id="50b95-115">Click Delivery schedule.</span></span>
    * <span data-ttu-id="50b95-116">Stránka Plán dodávek je místo, kde můžete zadat počet dodávek, ve kterých budou dodány celková množství řádku objednávky pro odběratele.</span><span class="sxs-lookup"><span data-stu-id="50b95-116">The Delivery schedule page is the place where you can specify the number of shipments in which the total quantity of the order line will be delivered to the customer.</span></span>    
    * <span data-ttu-id="50b95-117">Ve výchozím stavu systém zkopíruje celkové množství a další podrobnosti o původním prodejním řádku na první řádek plánu dodávek.</span><span class="sxs-lookup"><span data-stu-id="50b95-117">By default, the system copies the total quantity and other delivery details of the original sales line into the first delivery schedule line.</span></span> <span data-ttu-id="50b95-118">V tomto příkladu vytvoříme plán na dvě dodávky s posunem data druhé dodávky o týden od první.</span><span class="sxs-lookup"><span data-stu-id="50b95-118">In this example, we'll create a schedule for two shipments, with the second shipment's date offset by a week from the first one.</span></span>  
9. <span data-ttu-id="50b95-119">Do pole Množství zadejte číslo, které je částí celkového množství.</span><span class="sxs-lookup"><span data-stu-id="50b95-119">In the Quantity field, enter a number that is part of the total quantity.</span></span>
10. <span data-ttu-id="50b95-120">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="50b95-120">Click New.</span></span>
11. <span data-ttu-id="50b95-121">V poli Množství zadejte zbývající množství.</span><span class="sxs-lookup"><span data-stu-id="50b95-121">In the Quantity field, enter the remaining quantity.</span></span>
12. <span data-ttu-id="50b95-122">Do pole Požadované datum expedice zadejte datum, které je jeden týden před datem dodání prvního řádku.</span><span class="sxs-lookup"><span data-stu-id="50b95-122">In the Requested ship date field, enter a date a date that is one week ahead from the date of the first delivery line.</span></span>
    * <span data-ttu-id="50b95-123">Dvě možnosti na pevné záložce Převod nákladů řídí způsob, jakým chcete poplatky distribuovat napříč řádky plánu dodávek po jejich přiřazení na řádek původní objednávky.</span><span class="sxs-lookup"><span data-stu-id="50b95-123">The two options on the Charges conversion FastTab control how you want the charges to be distributed across the delivery schedule lines, once they've been assigned to the original order line.</span></span> <span data-ttu-id="50b95-124">Pokud vyberete Kopírovat hrubé částky, stejná částka nákladů se zkopíruje do každého řádku.</span><span class="sxs-lookup"><span data-stu-id="50b95-124">If you select Copy gross amounts, the same charge amount is copied to each line.</span></span> <span data-ttu-id="50b95-125">Možnost Přidělit řádkům dodávek umožňuje dělit náklady rovnoměrně mezi řádky dodávky.</span><span class="sxs-lookup"><span data-stu-id="50b95-125">The Allocate to delivery lines option divides the charge equally across the delivery lines.</span></span>  
    * <span data-ttu-id="50b95-126">Rozdělit lze jen pevné náklady, zatímco variabilní náklady se stále budou kopírovat do řádků.</span><span class="sxs-lookup"><span data-stu-id="50b95-126">Only fixed charges can be divided, whereas variable charges will still be copied to the lines.</span></span>  
13. <span data-ttu-id="50b95-127">Přesuňte kurzor od druhého řádku dodání, pokud chcete stránku aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="50b95-127">Move the cursor away from the second delivery line to update the page.</span></span>
    * <span data-ttu-id="50b95-128">Je možné sledovat celkové množství, která je přiděleno na řádky plánu dodávek tím, že si prohlédnete pole Součet a Zbývající.</span><span class="sxs-lookup"><span data-stu-id="50b95-128">You can keep track of the total quantity that's allocated to the delivery schedule lines by looking at the Total and Remaining fields.</span></span> <span data-ttu-id="50b95-129">Pokud je zbývající množství nulové, bylo do plánu přiděleno celé množství z původního řádku.</span><span class="sxs-lookup"><span data-stu-id="50b95-129">When the remaining quantity is zero, the full quantity from the original line has been allocated to the schedule.</span></span>   
14. <span data-ttu-id="50b95-130">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="50b95-130">Click OK.</span></span>
    * <span data-ttu-id="50b95-131">Plán dodávek byl nyní zkopírován do řádků objednávky.</span><span class="sxs-lookup"><span data-stu-id="50b95-131">The delivery schedule has now been copied to the order lines.</span></span>   
    * <span data-ttu-id="50b95-132">Původní řádek objednávky označovány jako obchodní řádek byl předveden na řádek objednávky s více dodávkami.</span><span class="sxs-lookup"><span data-stu-id="50b95-132">The original order line, referred to as a Commercial line, has been converted to an Order line with multiple deliveries.</span></span> <span data-ttu-id="50b95-133">Je označen jedinečnou ikonou a chová se jako záhlaví pro řádky dodávky.</span><span class="sxs-lookup"><span data-stu-id="50b95-133">It is marked with a distinct icon and acts as a header for the delivery lines.</span></span>  
    * <span data-ttu-id="50b95-134">Dva nové řádky, označované jako řádky dodávky, tvoří jeden plán dodávek.</span><span class="sxs-lookup"><span data-stu-id="50b95-134">The two new lines, referred to as delivery lines, make up one delivery schedule.</span></span> <span data-ttu-id="50b95-135">Objednávka bude zpracována s ohledem na tyto řádky, nikoli na původní řádek.</span><span class="sxs-lookup"><span data-stu-id="50b95-135">The order will be processed against these lines and not the original line.</span></span> <span data-ttu-id="50b95-136">Pokud jsou vytištěny dokumenty, jako například doklady pro potvrzení, výdejky, dodací listy nebo faktury, budou zobrazeny pouze řádky dodávky.</span><span class="sxs-lookup"><span data-stu-id="50b95-136">If documents such as confirmation slips, picking lists, packing slips, or invoices are printed, only the delivery lines are shown.</span></span>   
    * <span data-ttu-id="50b95-137">Řádky dodávky mohou mít jiná data dodání, množství, způsoby dodání a dimenze uskladnění, jako například pracoviště a sklad.</span><span class="sxs-lookup"><span data-stu-id="50b95-137">The delivery lines can have different delivery dates, quantities, modes of delivery, and storage dimensions, such as site and warehouse.</span></span> <span data-ttu-id="50b95-138">Dimenze produktu však musí vždy souhlasit s údaji na obchodním řádku a nelze je změnit.</span><span class="sxs-lookup"><span data-stu-id="50b95-138">However, the product dimensions must always match the ones on the commercial line and can't be changed.</span></span>  
15. <span data-ttu-id="50b95-139">Do pole Množství zadejte číslo, které je větší než současné.</span><span class="sxs-lookup"><span data-stu-id="50b95-139">In the Quantity field, enter a number that's bigger than the current one.</span></span>
16. <span data-ttu-id="50b95-140">Vyberte obchodní řádek a prohlédněte si jeho vliv na přepočítání množství.</span><span class="sxs-lookup"><span data-stu-id="50b95-140">Select the commercial line to see the effect of the quantity recalculation.</span></span>
17. <span data-ttu-id="50b95-141">V podokně akcí klikněte na položku Vyskladnit a zabalit.</span><span class="sxs-lookup"><span data-stu-id="50b95-141">On the Action Pane, click Pick and pack.</span></span>
18. <span data-ttu-id="50b95-142">Klikněte na Zaúčtovat dodací list.</span><span class="sxs-lookup"><span data-stu-id="50b95-142">Click Post packing slip.</span></span>
19. <span data-ttu-id="50b95-143">Rozbalte sekci Parametry.</span><span class="sxs-lookup"><span data-stu-id="50b95-143">Expand the Parameters section.</span></span>
20. <span data-ttu-id="50b95-144">V poli Množství vyberte možnost Vše.</span><span class="sxs-lookup"><span data-stu-id="50b95-144">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="50b95-145">Mějte na paměti, že dodací list bude vytvořen pro dva řádky plánu dodávek a nikoli pro původní řádek objednávky.</span><span class="sxs-lookup"><span data-stu-id="50b95-145">Note that the packing slip will be created for the two delivery schedule lines and not the original order line.</span></span>  
21. <span data-ttu-id="50b95-146">Vyberte možnost Ano v poli Tisk dodacího listu.</span><span class="sxs-lookup"><span data-stu-id="50b95-146">Select Yes in the Print packing slip field.</span></span>
22. <span data-ttu-id="50b95-147">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="50b95-147">Click OK.</span></span>
23. <span data-ttu-id="50b95-148">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="50b95-148">Click Yes.</span></span>
24. <span data-ttu-id="50b95-149">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="50b95-149">Close the page.</span></span>

