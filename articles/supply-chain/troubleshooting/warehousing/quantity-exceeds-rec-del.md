---
title: Množství, které se pokoušíte aktualizovat, překračuje přijaté / doručené množství.
description: Když vygenerujete dodací list, odchozí náklad obsahuje vyskladněné množství, které překlačuje množství práce, které bylo vyskladněno a rezervováno pro prodejní objednávku.
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
ms.openlocfilehash: 66d9cd80cc61e00d1d88ab4f59d03054d746cdd9
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249073"
---
# <a name="quantity-that-youre-trying-to-update-exceeds-the-receiveddelivered-quantity"></a><span data-ttu-id="d6be1-103">Množství, které se pokoušíte aktualizovat, překračuje přijaté / doručené množství</span><span class="sxs-lookup"><span data-stu-id="d6be1-103">Quantity that you're trying to update exceeds the received/delivered quantity</span></span>

<span data-ttu-id="d6be1-104">Kód chyby: SYS7676</span><span class="sxs-lookup"><span data-stu-id="d6be1-104">Error code: SYS7676</span></span>

## <a name="symptoms"></a><span data-ttu-id="d6be1-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="d6be1-105">Symptoms</span></span>

<span data-ttu-id="d6be1-106">Když vygenerujete dodací list, odchozí náklad obsahuje vyskladněné množství, které překlačuje množství práce, které bylo vyskladněno a rezervováno pro prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="d6be1-106">When you generate a packing slip, the outbound load contains a quantity that exceeds the work quantity that was picked and reserved for the sales order.</span></span>

<span data-ttu-id="d6be1-107">Když se pokusíte vygenerovat dodací list, systém zobrazí následující chybovou zprávu:</span><span class="sxs-lookup"><span data-stu-id="d6be1-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="d6be1-108">Množství, které se pokoušíte aktualizovat, překračuje přijaté či dodané množství.</span><span class="sxs-lookup"><span data-stu-id="d6be1-108">The quantity that you are trying to update exceeds the quantity received/delivered.</span></span>

<span data-ttu-id="d6be1-109">Proto nemůžete vygenerovat dodací list pro zásilku.</span><span class="sxs-lookup"><span data-stu-id="d6be1-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="d6be1-110">Příčina</span><span class="sxs-lookup"><span data-stu-id="d6be1-110">Cause</span></span>

<span data-ttu-id="d6be1-111">Vybrané množství práce neodpovídá vytvořenému množství práce na řádku dodávky.</span><span class="sxs-lookup"><span data-stu-id="d6be1-111">The picked work quantity doesn't match the created work quantity on the load line.</span></span> <span data-ttu-id="d6be1-112">Například k tomuto problému může dojít, pokud počet řádků nákladu, počet vytvořených prací nebo vybrané množství není přesný.</span><span class="sxs-lookup"><span data-stu-id="d6be1-112">For example, this issue might occur if the load line quantity, work created quantity, or picked quantity isn't accurate.</span></span>

## <a name="resolution"></a><span data-ttu-id="d6be1-113">Řešení</span><span class="sxs-lookup"><span data-stu-id="d6be1-113">Resolution</span></span>

<span data-ttu-id="d6be1-114">Náklad nebo zásilka je aktuálně ve stavu, kdy se generování dodacího listu nezdaří.</span><span class="sxs-lookup"><span data-stu-id="d6be1-114">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="d6be1-115">Chcete-li problém opravit, proveďte jeden nebo více z následujících úkolů:</span><span class="sxs-lookup"><span data-stu-id="d6be1-115">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="d6be1-116">Zkontrolujte řádky nákladu a ujistěte se, že všechny související práce byly dokončeny na konečném místě přepravy a že množství odpovídá.</span><span class="sxs-lookup"><span data-stu-id="d6be1-116">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="d6be1-117">Upravte množství řádku nákladu.</span><span class="sxs-lookup"><span data-stu-id="d6be1-117">Adjust the load line quantity.</span></span>
- <span data-ttu-id="d6be1-118">Stornujte všechny registrace vyskladnění a znovu proveďte vyskladnění.</span><span class="sxs-lookup"><span data-stu-id="d6be1-118">Reverse all pick registrations, and redo picking.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="d6be1-119">Zkontrolujte řádky nákladu a ujistěte se, že všechny související práce byly dokončeny na konečném místě přepravy a že množství odpovídá</span><span class="sxs-lookup"><span data-stu-id="d6be1-119">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="d6be1-120">Pomocí následujících kroků zkontrolujte řádky nákladu a ujistěte se, že všechny související práce byly dokončeny na konečném místě přepravy a že množství odpovídá</span><span class="sxs-lookup"><span data-stu-id="d6be1-120">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="d6be1-121">Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-121">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="d6be1-122">Vyberte dodávku, pro kterou nelze vygenerovat odeslání.</span><span class="sxs-lookup"><span data-stu-id="d6be1-122">Select the load that the shipment can't be generated for.</span></span>
1. <span data-ttu-id="d6be1-123">Na záložce s náhledem **Řádky nákladu** vyberte řádek nákladu.</span><span class="sxs-lookup"><span data-stu-id="d6be1-123">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="d6be1-124">Poznamenejte si hodnotu pole **Množství vytvořených prací**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-124">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="d6be1-125">V podokně akcí na kartě **Náklady** ve skupině **Související informace** vyberte **Práce**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-125">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="d6be1-126">Ověřte, že práce byla dokončena na konečném místě přepravy a že vybrané množství práce odpovídá vytvořenému množství práce na řádku zatížení.</span><span class="sxs-lookup"><span data-stu-id="d6be1-126">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="d6be1-127">Tento postup opakujte pro všechny řádky nákladů, abyste se ujistili, že jsou splněna všechna kritéria.</span><span class="sxs-lookup"><span data-stu-id="d6be1-127">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="adjust-the-load-line-quantity"></a><span data-ttu-id="d6be1-128">Upravte množství řádku nákladu</span><span class="sxs-lookup"><span data-stu-id="d6be1-128">Adjust the load line quantity</span></span>

<span data-ttu-id="d6be1-129">Následujícím postupem upravte množství řádku nákladu.</span><span class="sxs-lookup"><span data-stu-id="d6be1-129">Use the following procedure to adjust the load line quantity.</span></span>

1. <span data-ttu-id="d6be1-130">Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-130">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="d6be1-131">Vyberte náklad, pro který nelze vygenerovat dodací list.</span><span class="sxs-lookup"><span data-stu-id="d6be1-131">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="d6be1-132">V podokně akcí na kartě  **Odeslat a přijmout** ve skupině  **Stornování** vyberte **Storno potvrzení zásilky**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-132">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="d6be1-133">Na kartě  **Řádky nákladu** vyberte řádek nákladu položky, která způsobuje problém.</span><span class="sxs-lookup"><span data-stu-id="d6be1-133">On the **Load lines** tab, select the load line for the item that causes an issue.</span></span>
1. <span data-ttu-id="d6be1-134">Vyberte **Snížit vydané množství** a upravte vydané množství.</span><span class="sxs-lookup"><span data-stu-id="d6be1-134">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="d6be1-135">Nastavte pole **Snížit řádek nákladu** tak, aby odráželo úpravy na řádku nákladu.</span><span class="sxs-lookup"><span data-stu-id="d6be1-135">Set the **Reduce load line** field to reflect adjustments on the load line.</span></span>

### <a name="reverse-all-pick-registrations-and-redo-picking"></a><span data-ttu-id="d6be1-136">Stornujte všechny registrace vyskladnění a znovu proveďte vyskladnění</span><span class="sxs-lookup"><span data-stu-id="d6be1-136">Reverse all pick registrations, and redo picking</span></span>

<span data-ttu-id="d6be1-137">Pokud někdo použil registraci vyzvednutí k uzavření řádku nákladu bez práce, může dojít k rozporu mezi množstvím na řádku nákladu a vyskladněným množstvím.</span><span class="sxs-lookup"><span data-stu-id="d6be1-137">If someone used pick registration to close a load line without work, a discrepancy can occur between the load line quantity and the picked quantity.</span></span> <span data-ttu-id="d6be1-138">V takovém případě musí být ruční registrace vyskladnění obrácena a vyzvednutí musí být poté dokončeno pomocí mobilní aplikace Warehouse Management.</span><span class="sxs-lookup"><span data-stu-id="d6be1-138">In this case, manual pick registration must be reversed, and picking must then be completed by using the Warehouse Management mobile app.</span></span>

<span data-ttu-id="d6be1-139">Chcete-li registraci vyskladnění zrušit, použijte následující postup.</span><span class="sxs-lookup"><span data-stu-id="d6be1-139">Use the following procedure to reverse the pick registration.</span></span>

1. <span data-ttu-id="d6be1-140">Přejděte na **Pohledávky \> Objednávky \> Všechny objednávky**.</span><span class="sxs-lookup"><span data-stu-id="d6be1-140">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="d6be1-141">Vyberte prodejní objednávku, u které nemůžete zaúčtovat dodací list pro náklad.</span><span class="sxs-lookup"><span data-stu-id="d6be1-141">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="d6be1-142">Na kartě  **Řádky prodejní objednávky** vyberte řádek prodejní objednávky, pro kterou byla provedena registrace vyskladnění.</span><span class="sxs-lookup"><span data-stu-id="d6be1-142">On the **Sales order lines** tab, select the sales order line that pick registration was done for.</span></span>
1. <span data-ttu-id="d6be1-143">Vyberte **Aktualizovat řádek \> Vyskladnit** ke zrušení vyskladnění položek.</span><span class="sxs-lookup"><span data-stu-id="d6be1-143">Select **Update line \> Pick** to unpick the items.</span></span>
