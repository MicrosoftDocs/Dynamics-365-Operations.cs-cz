---
title: Zbývající fyzické množství v jednotce nesmí být nula
description: Když vygenerujete dodací list, data, která se do něj dodávají, mají nenulové množství zásob, ale nulové množství prodeje.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningListPage_WHSSalesPackingSlipPost, WHSLoadTable_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: bfd381160bcfd1e6e5489e16cc22178b8a5142ee
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/14/2021
ms.locfileid: "6248770"
---
# <a name="physical-remaining-quantity-in-the-unit-must-not-be-zero"></a><span data-ttu-id="39221-103">Zbývající fyzické množství v jednotce nesmí být nula</span><span class="sxs-lookup"><span data-stu-id="39221-103">Physical remaining quantity in the unit must not be zero</span></span>

<span data-ttu-id="39221-104">Kód chyby: SYS19591</span><span class="sxs-lookup"><span data-stu-id="39221-104">Error code: SYS19591</span></span>

## <a name="symptoms"></a><span data-ttu-id="39221-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="39221-105">Symptoms</span></span>

<span data-ttu-id="39221-106">Když vygenerujete dodací list, data, která se do něj dodávají, mají nenulové množství zásob, ale nulové množství prodeje.</span><span class="sxs-lookup"><span data-stu-id="39221-106">When you generate a packing slip, the data that is supplied to it has a non-zero inventory quantity but a zero sales quantity.</span></span>

<span data-ttu-id="39221-107">Když se pokusíte vygenerovat dodací list, systém zobrazí následující chybovou zprávu:</span><span class="sxs-lookup"><span data-stu-id="39221-107">When you try to generate the packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="39221-108">Fyzický zůstatek v jednotce %1 nesmí být roven nule.</span><span class="sxs-lookup"><span data-stu-id="39221-108">Physical remaining quantity in the unit %1 must be other than zero.</span></span>

<span data-ttu-id="39221-109">Proto nemůžete vygenerovat dodací list pro zásilku.</span><span class="sxs-lookup"><span data-stu-id="39221-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="39221-110">Příčina</span><span class="sxs-lookup"><span data-stu-id="39221-110">Cause</span></span>

<span data-ttu-id="39221-111">Systém vyhodnotí zbývající fyzické množství v skladové jednotce a zbývající fyzické množství v přepravní jednotce.</span><span class="sxs-lookup"><span data-stu-id="39221-111">The system evaluates the physical remaining quantity in the inventory unit and the physical remaining quantity in the shipping unit.</span></span> <span data-ttu-id="39221-112">Pokud systém zjistí, že zbývající fyzické množství v přepravní jednotce je 0 (nula), ale fyzické zbývající množství v jednotce zásob není 0, nemůžete vygenerovat dodací list.</span><span class="sxs-lookup"><span data-stu-id="39221-112">If the system finds that the physical remaining quantity in the shipping unit is 0 (zero), but the physical remaining quantity in the inventory unit isn't 0, you can't generate the packing slip.</span></span> <span data-ttu-id="39221-113">Například k tomuto problému může dojít, pokud se prodejní jednotka a jednotka zásob u položky liší a převod mezi jednotkami není přesný.</span><span class="sxs-lookup"><span data-stu-id="39221-113">For example, this issue might occur if the sales unit and inventory unit for the item differ, and the conversion between units isn't accurate.</span></span>

## <a name="resolution"></a><span data-ttu-id="39221-114">Řešení</span><span class="sxs-lookup"><span data-stu-id="39221-114">Resolution</span></span>

<span data-ttu-id="39221-115">Náklad nebo zásilka je aktuálně ve stavu, kdy se generování dodacího listu nezdaří.</span><span class="sxs-lookup"><span data-stu-id="39221-115">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="39221-116">Chcete-li problém opravit, proveďte jeden nebo více z následujících úkolů:</span><span class="sxs-lookup"><span data-stu-id="39221-116">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="39221-117">Zkontrolujte řádky nákladu a ujistěte se, že všechny související práce byly dokončeny na konečném místě přepravy a že množství odpovídá.</span><span class="sxs-lookup"><span data-stu-id="39221-117">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="39221-118">Zkontrolujte řádky nákladu a proveďte úpravy, abyste zajistili, že množství lze čistě převést bez problémů se zaokrouhlováním.</span><span class="sxs-lookup"><span data-stu-id="39221-118">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without rounding issues.</span></span>
- <span data-ttu-id="39221-119">Zkontrolujte řádky nákladu a proveďte úpravy, abyste se ujistili, že jednotka a množství jsou zarovnány s desetinnou přesností jednotky.</span><span class="sxs-lookup"><span data-stu-id="39221-119">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>
- <span data-ttu-id="39221-120">Ujistěte se, že měrná jednotka zásob je menší než měrná jednotka prodeje.</span><span class="sxs-lookup"><span data-stu-id="39221-120">Make sure that the inventory unit of measure is smaller than the sales unit of measure.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="39221-121">Zkontrolujte řádky nákladu a ujistěte se, že všechny související práce byly dokončeny na konečném místě přepravy a že množství odpovídá</span><span class="sxs-lookup"><span data-stu-id="39221-121">Review your load lines, and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="39221-122">Pomocí následujících kroků zkontrolujte řádky nákladu a ujistěte se, že všechny související práce byly dokončeny na konečném místě přepravy a že množství odpovídá</span><span class="sxs-lookup"><span data-stu-id="39221-122">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="39221-123">Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.</span><span class="sxs-lookup"><span data-stu-id="39221-123">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="39221-124">Vyberte dodávku, pro kterou nelze potvrdit odeslání.</span><span class="sxs-lookup"><span data-stu-id="39221-124">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="39221-125">Na záložce s náhledem **Řádky nákladu** vyberte řádek nákladu.</span><span class="sxs-lookup"><span data-stu-id="39221-125">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="39221-126">Poznamenejte si hodnotu pole **Množství vytvořených prací**.</span><span class="sxs-lookup"><span data-stu-id="39221-126">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="39221-127">V podokně akcí na kartě **Náklady** ve skupině **Související informace** vyberte **Práce**.</span><span class="sxs-lookup"><span data-stu-id="39221-127">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="39221-128">Ověřte, že práce byla dokončena na konečném místě přepravy a že vybrané množství práce odpovídá vytvořenému množství práce na řádku zatížení.</span><span class="sxs-lookup"><span data-stu-id="39221-128">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="39221-129">Tento postup opakujte pro všechny řádky nákladů, abyste se ujistili, že jsou splněna všechna kritéria.</span><span class="sxs-lookup"><span data-stu-id="39221-129">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-rounding-issues"></a><span data-ttu-id="39221-130">Zkontrolujte řádky nákladu a proveďte úpravy, abyste zajistili, že množství lze čistě převést bez problémů se zaokrouhlováním</span><span class="sxs-lookup"><span data-stu-id="39221-130">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without rounding issues</span></span>

<span data-ttu-id="39221-131">Pomocí následujícího postupu zkontrolujte řádky nákladu a proveďte úpravy, abyste zajistili, že množství lze čistě převést bez problémů se zaokrouhlováním.</span><span class="sxs-lookup"><span data-stu-id="39221-131">Use the following procedure to review your load lines and make adjustments to ensure that the quantity can be cleanly converted without rounding issues.</span></span>

1. <span data-ttu-id="39221-132">Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.</span><span class="sxs-lookup"><span data-stu-id="39221-132">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="39221-133">Vyberte náklad, pro který nelze vygenerovat dodací list.</span><span class="sxs-lookup"><span data-stu-id="39221-133">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="39221-134">V podokně akcí na kartě  **Odeslat a přijmout** ve skupině  **Stornování** vyberte **Storno potvrzení zásilky**.</span><span class="sxs-lookup"><span data-stu-id="39221-134">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="39221-135">Na kartě  **Řádky nákladu** vyberte řádek nákladu, který přesahuje navýšení dodávky.</span><span class="sxs-lookup"><span data-stu-id="39221-135">On the **Load lines** tab, select the load line for the item that exceeds the over-delivery.</span></span>
1. <span data-ttu-id="39221-136">Vyberte **Snížit vydané množství** a upravte vydané množství.</span><span class="sxs-lookup"><span data-stu-id="39221-136">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="39221-137">Na kartě  **Detaily řádku** vyberte možnost **Objednat**.</span><span class="sxs-lookup"><span data-stu-id="39221-137">On the  **Line details** tab, select **Order**.</span></span>
1. <span data-ttu-id="39221-138">Nastavte pole **Množství** na vyskladněné množství (tj. na hodnotu pole **Množství vytvořené prací**), aby mohlo dojít k vygenerování dodacího listu.</span><span class="sxs-lookup"><span data-stu-id="39221-138">Set the **Quantity** field to the picked quantity (that is, the value of the **Work created quantity** field), so that packing slip generation can proceed.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-unit-and-quantity-are-aligned-with-the-decimal-precision-of-the-unit"></a><span data-ttu-id="39221-139">Zkontrolujte řádky nákladu a proveďte úpravy, abyste se ujistili, že jednotka a množství jsou zarovnány s desetinnou přesností jednotky</span><span class="sxs-lookup"><span data-stu-id="39221-139">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit</span></span>

<span data-ttu-id="39221-140">Následujícím způsobem zkontrolujte řádky nákladu a proveďte úpravy, abyste se ujistili, že jednotka a množství jsou zarovnány s desetinnou přesností jednotky</span><span class="sxs-lookup"><span data-stu-id="39221-140">Use the following procedure to review your load lines and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>

1. <span data-ttu-id="39221-141">Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.</span><span class="sxs-lookup"><span data-stu-id="39221-141">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="39221-142">Vyberte náklad, pro který nelze vygenerovat dodací list.</span><span class="sxs-lookup"><span data-stu-id="39221-142">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="39221-143">Na záložce s náhledem **Řádky nákladu** vyberte řádek nákladu položky, která způsobuje problém.</span><span class="sxs-lookup"><span data-stu-id="39221-143">On the **Load lines** FastTab, select the load line for the item that causes an issue.</span></span> <span data-ttu-id="39221-144">Poznamenejte si hodnotu pole **Množství** a **Jednotka**.</span><span class="sxs-lookup"><span data-stu-id="39221-144">Make a note of the value of the **Quantity** and **Unit** fields.</span></span>
1. <span data-ttu-id="39221-145">Přejděte do nabídky **Správa organizace \> Jednotky \> Jednotky**.</span><span class="sxs-lookup"><span data-stu-id="39221-145">Go to **Organization administration \> Units \> Units**.</span></span>
1. <span data-ttu-id="39221-146">Vyberte jednotku, pro kterou nelze vygenerovat dodací list.</span><span class="sxs-lookup"><span data-stu-id="39221-146">Select the unit that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="39221-147">Upravte hodnotu pole **Desetinná přesnost** podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="39221-147">Adjust the value of the **Decimal precision** field as required.</span></span>

### <a name="make-sure-that-the-inventory-unit-of-measure-is-smaller-than-the-sales-unit-of-measure"></a><span data-ttu-id="39221-148">Ujistěte se, že měrná jednotka zásob je menší než měrná jednotka prodeje</span><span class="sxs-lookup"><span data-stu-id="39221-148">Make sure that the inventory unit of measure is smaller than the sales unit of measure</span></span>

<span data-ttu-id="39221-149">Ujistěte se, že měrná jednotka zásob je menší než měrná jednotka prodeje.</span><span class="sxs-lookup"><span data-stu-id="39221-149">Make sure that the inventory unit of measure is smaller than the sales unit of measure.</span></span> <span data-ttu-id="39221-150">Zvažte rekonfiguraci měrné jednotky pro položku podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="39221-150">Consider reconfiguring the unit of measure for the item as required.</span></span>
