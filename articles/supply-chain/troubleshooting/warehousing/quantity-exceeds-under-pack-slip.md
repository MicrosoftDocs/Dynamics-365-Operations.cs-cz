---
title: Množství překračuje procento nedostatečné dodávky během generování dodacího listu
description: Když vygenerujete dodací list, odchozí náklad obsahuje množství, které přesahuje procento nedostatečné dodávky.
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
ms.openlocfilehash: ecdd377d12faf40f64736e93671dcf42ff132403
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249068"
---
# <a name="quantity-exceeds-under-delivery-percentage-during-packing-slip-generation"></a><span data-ttu-id="555de-103">Množství překračuje procento nedostatečné dodávky během generování dodacího listu</span><span class="sxs-lookup"><span data-stu-id="555de-103">Quantity exceeds under-delivery percentage during packing slip generation</span></span>

<span data-ttu-id="555de-104">Kód chyby: SYS24921</span><span class="sxs-lookup"><span data-stu-id="555de-104">Error code: SYS24921</span></span>

## <a name="symptoms"></a><span data-ttu-id="555de-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="555de-105">Symptoms</span></span>

<span data-ttu-id="555de-106">Když vygenerujete dodací list, odchozí náklad obsahuje množství, které přesahuje procento nedostatečné dodávky.</span><span class="sxs-lookup"><span data-stu-id="555de-106">When you generate a packing slip, the outbound load contains a quantity that exceeds the under-delivery percentage.</span></span>

<span data-ttu-id="555de-107">Když se pokusíte vygenerovat dodací list, systém zobrazí následující chybovou zprávu:</span><span class="sxs-lookup"><span data-stu-id="555de-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="555de-108">Snížení dodávky řádku je %1 procent, ale povolené snížení je pouze %2 procent.</span><span class="sxs-lookup"><span data-stu-id="555de-108">Underdelivery of line is %1 percent, but the allowed underdelivery is only %2 percent.</span></span>

<span data-ttu-id="555de-109">Proto nemůžete vygenerovat dodací list pro zásilku.</span><span class="sxs-lookup"><span data-stu-id="555de-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="555de-110">Příčina</span><span class="sxs-lookup"><span data-stu-id="555de-110">Cause</span></span>

<span data-ttu-id="555de-111">Vybrané množství pro náklad nebo zásilku je menší než objednané množství a není v rozmezí procenta nedostatečné dodávky.</span><span class="sxs-lookup"><span data-stu-id="555de-111">The picked quantity for the load or shipment is less than the ordered quantity and isn't within the range of the under-delivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="555de-112">Řešení</span><span class="sxs-lookup"><span data-stu-id="555de-112">Resolution</span></span>

<span data-ttu-id="555de-113">Náklad nebo zásilka je aktuálně ve stavu, kdy se generování dodacího listu nezdaří.</span><span class="sxs-lookup"><span data-stu-id="555de-113">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="555de-114">Chcete-li problém opravit, proveďte jeden nebo více z následujících úkolů:</span><span class="sxs-lookup"><span data-stu-id="555de-114">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="555de-115">Upravte procento nedostatečné dodávky.</span><span class="sxs-lookup"><span data-stu-id="555de-115">Adjust the under-delivery percentage.</span></span>
- <span data-ttu-id="555de-116">Proveďte storno a úpravy.</span><span class="sxs-lookup"><span data-stu-id="555de-116">Reverse and make adjustments.</span></span>

### <a name="adjust-the-under-delivery-percentage"></a><span data-ttu-id="555de-117">Upravte procento nedostatečné dodávky</span><span class="sxs-lookup"><span data-stu-id="555de-117">Adjust the under-delivery percentage</span></span>

<span data-ttu-id="555de-118">Následujícím postupem upravte procento nedostatečné dodávky.</span><span class="sxs-lookup"><span data-stu-id="555de-118">Use the following procedure to adjust the under-delivery percentage.</span></span>

1. <span data-ttu-id="555de-119">Přejděte na **Pohledávky \> Objednávky \> Všechny objednávky**.</span><span class="sxs-lookup"><span data-stu-id="555de-119">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="555de-120">Vyberte prodejní objednávku, u které nemůžete zaúčtovat dodací list pro náklad.</span><span class="sxs-lookup"><span data-stu-id="555de-120">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="555de-121">Na kartě  **Řádky prodejní objednávky** vyberte řádek prodejní objednávky, který přesahuje procento nedostatečné dodávky.</span><span class="sxs-lookup"><span data-stu-id="555de-121">On the **Sales order lines** tab, select the sales order line for the item that exceeds the under-delivery percentage.</span></span>
1. <span data-ttu-id="555de-122">Na kartě  **Detaily řádku** vyberte možnost **Doručení**.</span><span class="sxs-lookup"><span data-stu-id="555de-122">On the  **Line details** tab, select **Delivery**.</span></span>
1. <span data-ttu-id="555de-123">Nastavte pole **Nedostatečná dodávka** na větší procento, které odpovídá množství, které bylo vyskladněno oproti množství naložení, aby mohlo pokračovat generování dodacího listu.</span><span class="sxs-lookup"><span data-stu-id="555de-123">Set the **Underdelivery** field to a larger percentage that accommodates the quantity that was picked against the load quantity, so that packing slip generation can proceed.</span></span>

### <a name="reverse-and-make-adjustments"></a><span data-ttu-id="555de-124">Proveďte storno a úpravy</span><span class="sxs-lookup"><span data-stu-id="555de-124">Reverse and make adjustments</span></span>

<span data-ttu-id="555de-125">Stornujte vše, co bylo zaúčtováno pro náklad (například dodací list, potvrzení zásilky a práce), proveďte úpravy prodejní objednávky, znovu vydejte objednávku do skladu a dokončete postup odeslání.</span><span class="sxs-lookup"><span data-stu-id="555de-125">Reverse everything that has been posted for the load (for example, the packing slip, shipment confirmation, and work), make sales order adjustments, re-release the order to the warehouse, and complete the shipment procedure.</span></span>

<span data-ttu-id="555de-126">Následujícím postupem zrušíte dodací list.</span><span class="sxs-lookup"><span data-stu-id="555de-126">Use the following procedure to cancel a packing slip.</span></span>

1. <span data-ttu-id="555de-127">Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.</span><span class="sxs-lookup"><span data-stu-id="555de-127">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="555de-128">V podokně akcí na kartě  **Odeslat a přijmout** ve skupině  **Stornování** vyberte **Storno dodacích listů**.</span><span class="sxs-lookup"><span data-stu-id="555de-128">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Cancel packing slips**.</span></span>

<span data-ttu-id="555de-129">Následujícím postupem stornujete potvrzení zásilky.</span><span class="sxs-lookup"><span data-stu-id="555de-129">Use the following procedure to reverse a shipment confirmation.</span></span>

1. <span data-ttu-id="555de-130">Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.</span><span class="sxs-lookup"><span data-stu-id="555de-130">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="555de-131">V podokně akcí na kartě  **Odeslat a přijmout** ve skupině  **Stornování** vyberte **Storno potvrzení zásilky**.</span><span class="sxs-lookup"><span data-stu-id="555de-131">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>

<span data-ttu-id="555de-132">Storno práce můžete provést následujícím postupem.</span><span class="sxs-lookup"><span data-stu-id="555de-132">Use the following procedure to reverse work.</span></span>

1. <span data-ttu-id="555de-133">Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.</span><span class="sxs-lookup"><span data-stu-id="555de-133">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="555de-134">V podokně Akce na kartě  **Náklady** ve skupině  **Práce** vyberte  **Stornovat práci**.</span><span class="sxs-lookup"><span data-stu-id="555de-134">On the Action Pane, on the **Loads** tab, in the **Work** group, select **Reverse work**.</span></span>
