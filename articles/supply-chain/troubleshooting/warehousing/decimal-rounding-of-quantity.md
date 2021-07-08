---
title: Desetinné zaokrouhlování množství fyzické aktualizace je nesprávné
description: Když vygenerujete dodací list, odchozí náklad obsahuje množství, které neodpovídá přesnosti na počet desetinných míst, který je definován v jednotce.
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
ms.openlocfilehash: 1e63440834f516879aa8ad711bd789e62b0ee993
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/14/2021
ms.locfileid: "6248771"
---
# <a name="decimal-rounding-of-the-physical-updating-quantity-is-incorrect"></a><span data-ttu-id="c5c4a-103">Desetinné zaokrouhlování množství fyzické aktualizace je nesprávné</span><span class="sxs-lookup"><span data-stu-id="c5c4a-103">Decimal rounding of the physical updating quantity is incorrect</span></span>

<span data-ttu-id="c5c4a-104">Kód chyby: SYS19589</span><span class="sxs-lookup"><span data-stu-id="c5c4a-104">Error code: SYS19589</span></span>

## <a name="symptoms"></a><span data-ttu-id="c5c4a-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="c5c4a-105">Symptoms</span></span>

<span data-ttu-id="c5c4a-106">Když vygenerujete dodací list, odchozí náklad obsahuje množství, které neodpovídá přesnosti na počet desetinných míst, který je definován v jednotce.</span><span class="sxs-lookup"><span data-stu-id="c5c4a-106">When you generate a packing slip, the outbound load contains a quantity that doesn't match the decimal precision that is defined in the unit.</span></span>

<span data-ttu-id="c5c4a-107">Když se pokusíte vygenerovat dodací list, systém zobrazí následující chybovou zprávu:</span><span class="sxs-lookup"><span data-stu-id="c5c4a-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="c5c4a-108">Desetinné zaokrouhlení fyzicky aktualizovaného množství v jednotce %1 je nesprávné.</span><span class="sxs-lookup"><span data-stu-id="c5c4a-108">Decimal rounding of the physical updating quantity in the unit %1 is incorrect.</span></span>

<span data-ttu-id="c5c4a-109">Proto nemůžete vygenerovat dodací list pro zásilku.</span><span class="sxs-lookup"><span data-stu-id="c5c4a-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="c5c4a-110">Příčina</span><span class="sxs-lookup"><span data-stu-id="c5c4a-110">Cause</span></span>

<span data-ttu-id="c5c4a-111">Systém vyhodnotí, zda desetinné zaokrouhlení přepravního množství odpovídá přesnosti na desetinná místa, která je definována pro přepravní jednotku.</span><span class="sxs-lookup"><span data-stu-id="c5c4a-111">The system evaluates whether the decimal rounding of the shipping quantity corresponds to the decimal precision that is defined for the shipping unit.</span></span> <span data-ttu-id="c5c4a-112">Když systém zaokrouhlí množství zásilky na zadaný počet desetinných míst, pokud zjistí, že zaokrouhlené množství zásilky neodpovídá skutečnému množství zásilky, nelze vygenerovat dodací list.</span><span class="sxs-lookup"><span data-stu-id="c5c4a-112">When the system rounds the shipping quantity to the specified number of decimal places, if it finds that the rounded shipping quantity doesn't match the actual shipping quantity, you can't generate the packing slip.</span></span> <span data-ttu-id="c5c4a-113">Například k tomuto problému může dojít, pokud je prodejní množství 1,75 kilogramu (kg), ale desetinná přesnost je nastavena na *1*.</span><span class="sxs-lookup"><span data-stu-id="c5c4a-113">For example, this issue might occur if the sales quantity is 1.75 kilograms (kg), but the decimal precision is set to *1*.</span></span>

## <a name="resolution"></a><span data-ttu-id="c5c4a-114">Řešení</span><span class="sxs-lookup"><span data-stu-id="c5c4a-114">Resolution</span></span>

<span data-ttu-id="c5c4a-115">Náklad nebo zásilka je aktuálně ve stavu, kdy se generování dodacího listu nezdaří.</span><span class="sxs-lookup"><span data-stu-id="c5c4a-115">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="c5c4a-116">Chcete-li problém opravit, proveďte jeden nebo více z následujících úkolů:</span><span class="sxs-lookup"><span data-stu-id="c5c4a-116">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="c5c4a-117">Zkontrolujte řádky nákladu a proveďte úpravy, abyste zajistili, že množství lze čistě převést bez desetinných čísel a jakýchkoli dalších problémů se zaokrouhlováním.</span><span class="sxs-lookup"><span data-stu-id="c5c4a-117">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without decimal numbers and any other rounding issues.</span></span>
- <span data-ttu-id="c5c4a-118">Zkontrolujte řádky nákladu a proveďte úpravy, abyste se ujistili, že jednotka a množství jsou zarovnány s desetinnou přesností jednotky.</span><span class="sxs-lookup"><span data-stu-id="c5c4a-118">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-decimal-numbers-and-any-other-rounding-issues"></a><span data-ttu-id="c5c4a-119">Zkontrolujte řádky nákladu a proveďte úpravy, abyste zajistili, že množství lze čistě převést bez desetinných čísel a jakýchkoli dalších problémů se zaokrouhlováním</span><span class="sxs-lookup"><span data-stu-id="c5c4a-119">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without decimal numbers and any other rounding issues</span></span>

<span data-ttu-id="c5c4a-120">Pomocí následujícího postupu zkontrolujte řádky nákladu a proveďte úpravy, abyste zajistili, že množství lze čistě převést bez desetinných čísel a jakýchkoli dalších problémů se zaokrouhlováním.</span><span class="sxs-lookup"><span data-stu-id="c5c4a-120">Use the following procedure to review your load lines and make adjustments to ensure that the quantity can be cleanly converted without decimal numbers and any other rounding issues.</span></span>

1. <span data-ttu-id="c5c4a-121">Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.</span><span class="sxs-lookup"><span data-stu-id="c5c4a-121">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="c5c4a-122">Vyberte náklad, pro který nelze vygenerovat dodací list.</span><span class="sxs-lookup"><span data-stu-id="c5c4a-122">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="c5c4a-123">V podokně akcí na kartě  **Odeslat a přijmout** ve skupině  **Stornování** vyberte **Storno potvrzení zásilky**.</span><span class="sxs-lookup"><span data-stu-id="c5c4a-123">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="c5c4a-124">Na kartě  **Řádky nákladu** vyberte řádek nákladu položky, která způsobuje problém.</span><span class="sxs-lookup"><span data-stu-id="c5c4a-124">On the **Load lines** tab, select the load line for the item that causes an issue.</span></span>
1. <span data-ttu-id="c5c4a-125">Vyberte **Snížit vydané množství** a upravte vydané množství.</span><span class="sxs-lookup"><span data-stu-id="c5c4a-125">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="c5c4a-126">Na kartě  **Detaily řádku** vyberte možnost **Objednat**.</span><span class="sxs-lookup"><span data-stu-id="c5c4a-126">On the  **Line details** tab, select **Order**.</span></span>
1. <span data-ttu-id="c5c4a-127">Nastavte pole **Množství** na vyskladněné množství (tj. na hodnotu pole **Množství vytvořené prací**), aby mohlo dojít k vygenerování dodacího listu.</span><span class="sxs-lookup"><span data-stu-id="c5c4a-127">Set the **Quantity** field to the picked quantity (that is, the value of the **Work created quantity** field), so that packing slip generation can proceed.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-unit-and-quantity-are-aligned-with-the-decimal-precision-of-the-unit"></a><span data-ttu-id="c5c4a-128">Zkontrolujte řádky nákladu a proveďte úpravy, abyste se ujistili, že jednotka a množství jsou zarovnány s desetinnou přesností jednotky</span><span class="sxs-lookup"><span data-stu-id="c5c4a-128">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit</span></span>

<span data-ttu-id="c5c4a-129">Následujícím způsobem zkontrolujte řádky nákladu a proveďte úpravy, abyste se ujistili, že jednotka a množství jsou zarovnány s desetinnou přesností jednotky</span><span class="sxs-lookup"><span data-stu-id="c5c4a-129">Use the following procedure to review your load lines and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>

1. <span data-ttu-id="c5c4a-130">Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.</span><span class="sxs-lookup"><span data-stu-id="c5c4a-130">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="c5c4a-131">Vyberte náklad, pro který nelze vygenerovat dodací list.</span><span class="sxs-lookup"><span data-stu-id="c5c4a-131">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="c5c4a-132">Na záložce s náhledem **Řádky nákladu** vyberte řádek nákladu položky, která způsobuje problém.</span><span class="sxs-lookup"><span data-stu-id="c5c4a-132">On the **Load lines** FastTab, select the load line for the item that causes an issue.</span></span> <span data-ttu-id="c5c4a-133">Poznamenejte si hodnotu pole **Množství** a **Jednotka**.</span><span class="sxs-lookup"><span data-stu-id="c5c4a-133">Make a note of the value of the **Quantity** and **Unit** fields.</span></span>
1. <span data-ttu-id="c5c4a-134">Přejděte do nabídky **Správa organizace \> Jednotky \> Jednotky**.</span><span class="sxs-lookup"><span data-stu-id="c5c4a-134">Go to **Organization administration \> Units \> Units**.</span></span>
1. <span data-ttu-id="c5c4a-135">Vyberte jednotku, pro kterou nelze vygenerovat dodací list.</span><span class="sxs-lookup"><span data-stu-id="c5c4a-135">Select the unit that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="c5c4a-136">Upravte hodnotu pole **Desetinná přesnost** podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="c5c4a-136">Adjust the value of the **Decimal precision** field as required.</span></span>
