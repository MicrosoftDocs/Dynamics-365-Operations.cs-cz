---
title: Množství překračuje procento nadměrné dodávky během generování dodacího listu
description: Když vygenerujete dodací list, odchozí náklad obsahuje množství, které přesahuje procento nadměrného doručení.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSSalesPackingSlipPost,WHSLoadPlanningListPage_WHSSalesPackingSlipPost,WHSLoadPlanningWorkbench_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1106322cc3772c1b671b7fa82fb74039c028ba35
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249070"
---
# <a name="quantity-exceeds-over-delivery-percentage-during-packing-slip-generation"></a><span data-ttu-id="2f482-103">Množství překračuje procento nadměrné dodávky během generování dodacího listu</span><span class="sxs-lookup"><span data-stu-id="2f482-103">Quantity exceeds over-delivery percentage during packing slip generation</span></span>

<span data-ttu-id="2f482-104">Kód chyby: SYS24920</span><span class="sxs-lookup"><span data-stu-id="2f482-104">Error code: SYS24920</span></span>

## <a name="symptoms"></a><span data-ttu-id="2f482-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="2f482-105">Symptoms</span></span>

<span data-ttu-id="2f482-106">Když vygenerujete dodací list, odchozí náklad obsahuje množství, které přesahuje procento nadměrného doručení.</span><span class="sxs-lookup"><span data-stu-id="2f482-106">When you generate a packing slip, the outbound load contains a quantity that exceeds the over-delivery percentage.</span></span>

<span data-ttu-id="2f482-107">Když se pokusíte vygenerovat dodací list, systém zobrazí následující chybovou zprávu:</span><span class="sxs-lookup"><span data-stu-id="2f482-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="2f482-108">Navýšení dodávky řádku je %1 procent, ale povolené navýšení je pouze %2 procent.</span><span class="sxs-lookup"><span data-stu-id="2f482-108">Overdelivery of line is %1 percent, but the allowed overdelivery is only %2 percent.</span></span>

<span data-ttu-id="2f482-109">Proto nemůžete vygenerovat dodací list pro zásilku.</span><span class="sxs-lookup"><span data-stu-id="2f482-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="2f482-110">Příčina</span><span class="sxs-lookup"><span data-stu-id="2f482-110">Cause</span></span>

<span data-ttu-id="2f482-111">Vybrané množství pro náklad nebo zásilku je větší než objednané množství a není v rozmezí procenta nadměrného doručení.</span><span class="sxs-lookup"><span data-stu-id="2f482-111">The picked quantity for the load or shipment is more than the ordered quantity and isn't within the range of the over-delivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="2f482-112">Řešení</span><span class="sxs-lookup"><span data-stu-id="2f482-112">Resolution</span></span>

<span data-ttu-id="2f482-113">Náklad nebo zásilka je aktuálně ve stavu, kdy se generování dodacího listu nezdaří.</span><span class="sxs-lookup"><span data-stu-id="2f482-113">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="2f482-114">Chcete-li problém opravit, proveďte jeden nebo více z následujících úkolů:</span><span class="sxs-lookup"><span data-stu-id="2f482-114">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="2f482-115">Upravte množství řádku nákladu.</span><span class="sxs-lookup"><span data-stu-id="2f482-115">Adjust the load line quantity.</span></span>
- <span data-ttu-id="2f482-116">Upravte procento navýšení dodávky.</span><span class="sxs-lookup"><span data-stu-id="2f482-116">Adjust the over-delivery percentage.</span></span>
- <span data-ttu-id="2f482-117">Proveďte storno a úpravy.</span><span class="sxs-lookup"><span data-stu-id="2f482-117">Reverse and make adjustments.</span></span>

### <a name="adjust-the-load-line-quantity"></a><span data-ttu-id="2f482-118">Upravte množství řádku nákladu</span><span class="sxs-lookup"><span data-stu-id="2f482-118">Adjust the load line quantity</span></span>

<span data-ttu-id="2f482-119">Následujícím postupem upravte množství řádku nákladu.</span><span class="sxs-lookup"><span data-stu-id="2f482-119">Use the following procedure to adjust the load line quantity.</span></span>

1. <span data-ttu-id="2f482-120">Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.</span><span class="sxs-lookup"><span data-stu-id="2f482-120">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="2f482-121">Vyberte náklad, pro který nelze vygenerovat dodací list.</span><span class="sxs-lookup"><span data-stu-id="2f482-121">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="2f482-122">V podokně akcí na kartě  **Odeslat a přijmout** ve skupině  **Stornování** vyberte **Storno potvrzení zásilky**.</span><span class="sxs-lookup"><span data-stu-id="2f482-122">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="2f482-123">Na kartě  **Řádky nákladu** vyberte řádek nákladu, který přesahuje procento navýšení dodávky.</span><span class="sxs-lookup"><span data-stu-id="2f482-123">On the **Load lines** tab, select the load line for the item that exceeds the over-delivery percentage.</span></span>
1. <span data-ttu-id="2f482-124">Vyberte **Snížit vydané množství** a upravte vydané množství.</span><span class="sxs-lookup"><span data-stu-id="2f482-124">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="2f482-125">Na kartě  **Detaily řádku** vyberte možnost **Objednat**.</span><span class="sxs-lookup"><span data-stu-id="2f482-125">On the  **Line details** tab, select **Order**.</span></span>
1. <span data-ttu-id="2f482-126">Nastavte pole **Množství** na vyskladněné množství (tj. na hodnotu pole **Množství vytvořené prací**), aby mohlo dojít k vygenerování dodacího listu.</span><span class="sxs-lookup"><span data-stu-id="2f482-126">Set the **Quantity** field to the picked quantity (that is, the value of the **Work created quantity** field), so that packing slip generation can proceed.</span></span>

### <a name="adjust-the-over-delivery-percentage"></a><span data-ttu-id="2f482-127">Upravte procento navýšení dodávky</span><span class="sxs-lookup"><span data-stu-id="2f482-127">Adjust the over-delivery percentage</span></span>

<span data-ttu-id="2f482-128">Následujícím postupem upravte procento navýšení dodávky.</span><span class="sxs-lookup"><span data-stu-id="2f482-128">Use the following procedure to adjust the over-delivery percentage.</span></span>

1. <span data-ttu-id="2f482-129">Přejděte na **Pohledávky \> Objednávky \> Všechny objednávky**.</span><span class="sxs-lookup"><span data-stu-id="2f482-129">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="2f482-130">Vyberte prodejní objednávku, u které nemůžete zaúčtovat dodací list pro náklad.</span><span class="sxs-lookup"><span data-stu-id="2f482-130">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="2f482-131">Na kartě  **Řádky prodejní objednávky** vyberte řádek prodejní objednávky, který přesahuje procento navýšení dodávky.</span><span class="sxs-lookup"><span data-stu-id="2f482-131">On the **Sales order lines** tab, select the sales order line for the item that exceeds the over-delivery percentage.</span></span>
1. <span data-ttu-id="2f482-132">Na kartě  **Detaily řádku** vyberte možnost **Doručení**.</span><span class="sxs-lookup"><span data-stu-id="2f482-132">On the  **Line details** tab, select **Delivery**.</span></span>
1. <span data-ttu-id="2f482-133">Nastavte pole **Navýšení dodávky** na větší procento, které odpovídá množství, které bylo vyskladněno oproti množství naložení, aby mohlo pokračovat generování dodacího listu.</span><span class="sxs-lookup"><span data-stu-id="2f482-133">Set the **Overdelivery** field to a larger percentage that accommodates the quantity that was picked against the load quantity, so that packing slip generation can proceed.</span></span>

### <a name="reverse-and-make-adjustments"></a><span data-ttu-id="2f482-134">Proveďte storno a úpravy</span><span class="sxs-lookup"><span data-stu-id="2f482-134">Reverse and make adjustments</span></span>

<span data-ttu-id="2f482-135">Stornujte vše, co bylo zaúčtováno pro náklad (například dodací list, potvrzení zásilky a práce), proveďte úpravy prodejní objednávky, znovu vydejte objednávku do skladu a dokončete postup odeslání.</span><span class="sxs-lookup"><span data-stu-id="2f482-135">Reverse everything that has been posted for the load (for example, the packing slip, shipment confirmation, and work), make sales order adjustments, re-release the order to the warehouse, and complete the shipment procedure.</span></span>

<span data-ttu-id="2f482-136">Následujícím postupem zrušíte dodací list.</span><span class="sxs-lookup"><span data-stu-id="2f482-136">Use the following procedure to cancel a packing slip.</span></span>

1. <span data-ttu-id="2f482-137">Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.</span><span class="sxs-lookup"><span data-stu-id="2f482-137">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="2f482-138">V podokně akcí na kartě  **Odeslat a přijmout** ve skupině  **Stornování** vyberte **Storno dodacích listů**.</span><span class="sxs-lookup"><span data-stu-id="2f482-138">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Cancel packing slips**.</span></span>

<span data-ttu-id="2f482-139">Následujícím postupem stornujete potvrzení zásilky.</span><span class="sxs-lookup"><span data-stu-id="2f482-139">Use the following procedure to reverse a shipment confirmation.</span></span>

1. <span data-ttu-id="2f482-140">Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.</span><span class="sxs-lookup"><span data-stu-id="2f482-140">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="2f482-141">V podokně akcí na kartě  **Odeslat a přijmout** ve skupině  **Stornování** vyberte **Storno potvrzení zásilky**.</span><span class="sxs-lookup"><span data-stu-id="2f482-141">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>

<span data-ttu-id="2f482-142">Storno práce můžete provést následujícím postupem.</span><span class="sxs-lookup"><span data-stu-id="2f482-142">Use the following procedure to reverse work.</span></span>

1. <span data-ttu-id="2f482-143">Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.</span><span class="sxs-lookup"><span data-stu-id="2f482-143">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="2f482-144">V podokně Akce na kartě  **Náklady** ve skupině  **Práce** vyberte  **Stornovat práci**.</span><span class="sxs-lookup"><span data-stu-id="2f482-144">On the Action Pane, on the **Loads** tab, in the **Work** group, select **Reverse work**.</span></span>
