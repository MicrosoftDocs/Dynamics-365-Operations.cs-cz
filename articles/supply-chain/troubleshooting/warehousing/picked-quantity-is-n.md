---
title: Vydané množství není během generování dodacího listu dostatečné
description: Když vygenerujete dodací list, odchozí náklad obsahuje vyskladněné množství, které neodpovídá vytvořenému množství práce na řádku nákladu.
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
ms.openlocfilehash: fa6054dc26e4306ec16e37b0e6c320342ed40fe0
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/14/2021
ms.locfileid: "6249072"
---
# <a name="picked-quantity-isnt-sufficient-during-packing-slip-generation"></a><span data-ttu-id="2c4f2-103">Vydané množství není během generování dodacího listu dostatečné</span><span class="sxs-lookup"><span data-stu-id="2c4f2-103">Picked quantity isn't sufficient during packing slip generation</span></span>

<span data-ttu-id="2c4f2-104">Kód chyby: SYS54073</span><span class="sxs-lookup"><span data-stu-id="2c4f2-104">Error code: SYS54073</span></span>

## <a name="symptoms"></a><span data-ttu-id="2c4f2-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="2c4f2-105">Symptoms</span></span>

<span data-ttu-id="2c4f2-106">Když vygenerujete dodací list, odchozí náklad obsahuje vyskladněné množství, které neodpovídá vytvořenému množství práce na řádku nákladu.</span><span class="sxs-lookup"><span data-stu-id="2c4f2-106">When you generate a packing slip, the outbound load contains a picked quantity that doesn't match the created work quantity on the load line.</span></span>

<span data-ttu-id="2c4f2-107">Když se pokusíte vygenerovat dodací list, systém zobrazí následující chybovou zprávu:</span><span class="sxs-lookup"><span data-stu-id="2c4f2-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="2c4f2-108">Hodnota %1 byla vyskladněna, proto nestačí aktualizovat %2, když potom zbývající zůstatek musí být %3.</span><span class="sxs-lookup"><span data-stu-id="2c4f2-108">As %1 have been picked, it is not sufficient to update %2, when, subsequently, the remainder must be %3.</span></span>

<span data-ttu-id="2c4f2-109">Proto nemůžete vygenerovat dodací list pro zásilku.</span><span class="sxs-lookup"><span data-stu-id="2c4f2-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="2c4f2-110">Příčina</span><span class="sxs-lookup"><span data-stu-id="2c4f2-110">Cause</span></span>

<span data-ttu-id="2c4f2-111">Dodací list nelze v aktuálním stavu vygenerovat, protože může existovat jedna z následujících podmínek:</span><span class="sxs-lookup"><span data-stu-id="2c4f2-111">The packing slip can't be generated in its current state because one of the following conditions might exist:</span></span>

- <span data-ttu-id="2c4f2-112">Související práce ještě nebyly vybrány a přesunuty na konečné místo dodání.</span><span class="sxs-lookup"><span data-stu-id="2c4f2-112">The related work hasn't yet been picked and moved to the final shipping location.</span></span>
- <span data-ttu-id="2c4f2-113">Vybrané množství práce neodpovídá vytvořenému množství práce na řádku dodávky.</span><span class="sxs-lookup"><span data-stu-id="2c4f2-113">The picked work quantity doesn't match the created work quantity on the load line.</span></span>
- <span data-ttu-id="2c4f2-114">Množství na řádku dodávky, množství vytvořené práce a vyskladněné množství se neshodují.</span><span class="sxs-lookup"><span data-stu-id="2c4f2-114">The load line quantity, work created quantity, and picked quantity don't match.</span></span>

## <a name="resolution"></a><span data-ttu-id="2c4f2-115">Řešení</span><span class="sxs-lookup"><span data-stu-id="2c4f2-115">Resolution</span></span>

<span data-ttu-id="2c4f2-116">Náklad nebo zásilka je aktuálně ve stavu, kdy se generování dodacího listu nezdaří.</span><span class="sxs-lookup"><span data-stu-id="2c4f2-116">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="2c4f2-117">Chcete-li problém opravit, proveďte jeden nebo více z následujících úkolů:</span><span class="sxs-lookup"><span data-stu-id="2c4f2-117">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="2c4f2-118">Zkontrolujte řádky nákladu a ujistěte se, že všechny související práce byly dokončeny na konečném místě přepravy a že množství odpovídá.</span><span class="sxs-lookup"><span data-stu-id="2c4f2-118">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="2c4f2-119">Upravte množství řádku nákladu.</span><span class="sxs-lookup"><span data-stu-id="2c4f2-119">Adjust the load line quantity.</span></span>
- <span data-ttu-id="2c4f2-120">Stornujte všechny registrace vyskladnění a znovu proveďte vyskladnění.</span><span class="sxs-lookup"><span data-stu-id="2c4f2-120">Reverse all pick registrations, and redo picking.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="2c4f2-121">Zkontrolujte řádky nákladu a ujistěte se, že všechny související práce byly dokončeny na konečném místě přepravy a že množství odpovídá</span><span class="sxs-lookup"><span data-stu-id="2c4f2-121">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="2c4f2-122">Pomocí následujících kroků zkontrolujte řádky nákladu a ujistěte se, že všechny související práce byly dokončeny na konečném místě přepravy a že množství odpovídá</span><span class="sxs-lookup"><span data-stu-id="2c4f2-122">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="2c4f2-123">Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.</span><span class="sxs-lookup"><span data-stu-id="2c4f2-123">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="2c4f2-124">Vyberte náklad, pro který nelze vygenerovat dodací list.</span><span class="sxs-lookup"><span data-stu-id="2c4f2-124">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="2c4f2-125">Na záložce s náhledem **Řádky nákladu** vyberte řádek nákladu.</span><span class="sxs-lookup"><span data-stu-id="2c4f2-125">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="2c4f2-126">Poznamenejte si hodnotu pole **Množství vytvořených prací**.</span><span class="sxs-lookup"><span data-stu-id="2c4f2-126">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="2c4f2-127">V podokně akcí na kartě **Náklady** ve skupině **Související informace** vyberte **Práce**.</span><span class="sxs-lookup"><span data-stu-id="2c4f2-127">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="2c4f2-128">Ověřte, že práce byla dokončena na konečném místě přepravy a že vybrané množství práce odpovídá vytvořenému množství práce na řádku zatížení.</span><span class="sxs-lookup"><span data-stu-id="2c4f2-128">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="2c4f2-129">Tento postup opakujte pro všechny řádky nákladů, abyste se ujistili, že jsou splněna všechna kritéria.</span><span class="sxs-lookup"><span data-stu-id="2c4f2-129">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="adjust-the-load-line-quantity"></a><span data-ttu-id="2c4f2-130">Upravte množství řádku nákladu</span><span class="sxs-lookup"><span data-stu-id="2c4f2-130">Adjust the load line quantity</span></span>

<span data-ttu-id="2c4f2-131">Následujícím postupem upravte množství řádku nákladu.</span><span class="sxs-lookup"><span data-stu-id="2c4f2-131">Use the following procedure to adjust the load line quantity.</span></span>

1. <span data-ttu-id="2c4f2-132">Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.</span><span class="sxs-lookup"><span data-stu-id="2c4f2-132">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="2c4f2-133">Vyberte náklad, pro který nelze vygenerovat dodací list.</span><span class="sxs-lookup"><span data-stu-id="2c4f2-133">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="2c4f2-134">V podokně akcí na kartě  **Odeslat a přijmout** ve skupině  **Stornování** vyberte **Storno potvrzení zásilky**.</span><span class="sxs-lookup"><span data-stu-id="2c4f2-134">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="2c4f2-135">Na kartě  **Řádky nákladu** vyberte řádek nákladu položky, která způsobuje problém.</span><span class="sxs-lookup"><span data-stu-id="2c4f2-135">On the **Load lines** tab, select the load line for the item that causes an issue.</span></span>
1. <span data-ttu-id="2c4f2-136">Vyberte **Snížit vydané množství** a upravte vydané množství.</span><span class="sxs-lookup"><span data-stu-id="2c4f2-136">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="2c4f2-137">Nastavte pole **Snížit řádek nákladu** tak, aby odráželo úpravy na řádku nákladu.</span><span class="sxs-lookup"><span data-stu-id="2c4f2-137">Set the **Reduce load line** field to reflect adjustments on the load line.</span></span>

### <a name="reverse-all-pick-registrations-and-redo-picking"></a><span data-ttu-id="2c4f2-138">Stornujte všechny registrace vyskladnění a znovu proveďte vyskladnění</span><span class="sxs-lookup"><span data-stu-id="2c4f2-138">Reverse all pick registrations, and redo picking</span></span>

<span data-ttu-id="2c4f2-139">K problému může dojít, protože někdo použil registraci vyskladnění k uzavření řádku nákladu bez práce.</span><span class="sxs-lookup"><span data-stu-id="2c4f2-139">The issue might occur because someone used pick registration to close a load line without work.</span></span> <span data-ttu-id="2c4f2-140">V takovém případě musí být ruční registrace vyskladnění obrácena a vyzvednutí musí být poté dokončeno pomocí mobilní aplikace Warehouse Management.</span><span class="sxs-lookup"><span data-stu-id="2c4f2-140">In this case, manual pick registration must be reversed, and picking must then be completed by using the Warehouse Management mobile app.</span></span>

<span data-ttu-id="2c4f2-141">Chcete-li registraci vyskladnění zrušit, použijte následující postup.</span><span class="sxs-lookup"><span data-stu-id="2c4f2-141">Use the following procedure to reverse the pick registration.</span></span>

1. <span data-ttu-id="2c4f2-142">Přejděte na **Pohledávky \> Objednávky \> Všechny objednávky**.</span><span class="sxs-lookup"><span data-stu-id="2c4f2-142">Go to **Accounts receivable \> Orders \> All orders**.</span></span>
1. <span data-ttu-id="2c4f2-143">Vyberte prodejní objednávku, u které nemůžete zaúčtovat dodací list pro náklad.</span><span class="sxs-lookup"><span data-stu-id="2c4f2-143">Select the sales order for which you can't post a packing slip for the load.</span></span>
1. <span data-ttu-id="2c4f2-144">Na kartě  **Řádky prodejní objednávky** vyberte řádek prodejní objednávky, pro kterou byla provedena registrace vyskladnění.</span><span class="sxs-lookup"><span data-stu-id="2c4f2-144">On the **Sales order lines** tab, select the sales order line that pick registration was done for.</span></span>
1. <span data-ttu-id="2c4f2-145">Vyberte **Aktualizovat řádek \> Vyskladnit** ke zrušení vyskladnění položek.</span><span class="sxs-lookup"><span data-stu-id="2c4f2-145">Select **Update line \> Pick** to unpick the items.</span></span>
