---
title: Zásilku nemůžete potvrdit, protože položky nebyly vybrány
description: Zásilku nemůžete potvrdit, protože položky nebyly vybrány
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f3ebd47ffc85d4ca257b404579d60d679f7929b6
ms.sourcegitcommit: f9b145ef4a81cec81f420871b4130b05db4f4500
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301298"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a><span data-ttu-id="c09b4-103">Zásilku nemůžete potvrdit, protože položky nebyly vybrány</span><span class="sxs-lookup"><span data-stu-id="c09b4-103">You can't confirm a shipment because items haven't been picked</span></span>

<span data-ttu-id="c09b4-104">Kód chyby: LoadNotPickedAndMovedToFinalShippingLocation</span><span class="sxs-lookup"><span data-stu-id="c09b4-104">Error code: LoadNotPickedAndMovedToFinalShippingLocation</span></span>

## <a name="symptoms"></a><span data-ttu-id="c09b4-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="c09b4-105">Symptoms</span></span>

<span data-ttu-id="c09b4-106">Když se pokusíte potvrdit dodávku, systém zobrazí následující chybovou zprávu:</span><span class="sxs-lookup"><span data-stu-id="c09b4-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="c09b4-107">Některé položky, které jsou nezbytné pro vytížení %1, dosud nebyly vyzvednuty a přesunuty na konečné skladové místo.</span><span class="sxs-lookup"><span data-stu-id="c09b4-107">Some of the items that are needed for load %1 have not yet been picked and moved to the final shipping location.</span></span>

<span data-ttu-id="c09b4-108">Proto nemůžete potvrdit dodání pro zásilku.</span><span class="sxs-lookup"><span data-stu-id="c09b4-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="c09b4-109">Příčina</span><span class="sxs-lookup"><span data-stu-id="c09b4-109">Cause</span></span>

<span data-ttu-id="c09b4-110">Dodávku nebo zásilku nelze v aktuálním stavu potvrdit, protože může existovat jedna z následujících podmínek:</span><span class="sxs-lookup"><span data-stu-id="c09b4-110">The load or shipment can't be confirmed in its current state because one of the following conditions might exist:</span></span>

- <span data-ttu-id="c09b4-111">Související práce ještě nebyly vybrány a přesunuty na konečné místo dodání.</span><span class="sxs-lookup"><span data-stu-id="c09b4-111">The related work hasn't yet been picked and moved to the final shipping location.</span></span>
- <span data-ttu-id="c09b4-112">Vybrané množství práce neodpovídá vytvořenému množství práce na řádku dodávky.</span><span class="sxs-lookup"><span data-stu-id="c09b4-112">The picked work quantity doesn't match the created work quantity on the load line.</span></span>
- <span data-ttu-id="c09b4-113">Direktiva umístění byla nakonfigurována s umístěním balení jako konečné místo odeslání při použití kontejnerizace šablony vlny.</span><span class="sxs-lookup"><span data-stu-id="c09b4-113">The location directive has been configured with packing location as the final shipping location while using Wave template containerization.</span></span>

## <a name="resolution"></a><span data-ttu-id="c09b4-114">Řešení</span><span class="sxs-lookup"><span data-stu-id="c09b4-114">Resolution</span></span>

<span data-ttu-id="c09b4-115">Náklad nebo zásilka je aktuálně ve stavu, kdy se potvrzení zásilky nezdaří.</span><span class="sxs-lookup"><span data-stu-id="c09b4-115">The load or shipment is currently in a state where shipment confirmation fails.</span></span> <span data-ttu-id="c09b4-116">Chcete-li problém opravit, proveďte jeden nebo více z následujících úkolů:</span><span class="sxs-lookup"><span data-stu-id="c09b4-116">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="c09b4-117">Zkontrolujte řádky nákladu a ujistěte se, že všechny související práce byly dokončeny na konečném místě přepravy a že množství odpovídá</span><span class="sxs-lookup"><span data-stu-id="c09b4-117">Review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="c09b4-118">Zrušte ID práce, která byla vytvořena s umístěním balení jako konečné místo odeslání, překonfigurujte direktivu umístění a znovu uvolněte náklad.</span><span class="sxs-lookup"><span data-stu-id="c09b4-118">Cancel the work IDs that have been created with the packing location as the final shipping location, reconfigure the location directive, and rerelease the load.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="c09b4-119">Zkontrolujte řádky nákladu a ujistěte se, že všechny související práce byly dokončeny na konečném místě přepravy a že množství odpovídá</span><span class="sxs-lookup"><span data-stu-id="c09b4-119">Review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="c09b4-120">Pomocí následujících kroků zkontrolujte řádky nákladu a ujistěte se, že všechny související práce byly dokončeny na konečném místě přepravy a že množství odpovídá</span><span class="sxs-lookup"><span data-stu-id="c09b4-120">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="c09b4-121">Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.</span><span class="sxs-lookup"><span data-stu-id="c09b4-121">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="c09b4-122">Vyberte dodávku, pro kterou nelze potvrdit odeslání.</span><span class="sxs-lookup"><span data-stu-id="c09b4-122">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="c09b4-123">Na záložce s náhledem **Řádky nákladu** vyberte řádek nákladu.</span><span class="sxs-lookup"><span data-stu-id="c09b4-123">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="c09b4-124">Poznamenejte si hodnotu pole **Množství vytvořených prací**.</span><span class="sxs-lookup"><span data-stu-id="c09b4-124">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="c09b4-125">V podokně akcí na kartě **Náklady** ve skupině **Související informace** vyberte **Práce**.</span><span class="sxs-lookup"><span data-stu-id="c09b4-125">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="c09b4-126">Ověřte, že práce byla dokončena na konečném místě přepravy a že vybrané množství práce odpovídá vytvořenému množství práce na řádku zatížení.</span><span class="sxs-lookup"><span data-stu-id="c09b4-126">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="c09b4-127">Tento postup opakujte pro všechny řádky nákladů, abyste se ujistili, že jsou splněna všechna kritéria.</span><span class="sxs-lookup"><span data-stu-id="c09b4-127">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="cancel-the-work-ids-that-have-been-created-with-the-packing-location-as-the-final-shipping-location-reconfigure-the-location-directive-and-rerelease-the-load"></a><span data-ttu-id="c09b4-128">Zrušte ID práce, která byla vytvořena s umístěním balení jako konečné místo odeslání, překonfigurujte direktivu umístění a znovu uvolněte náklad</span><span class="sxs-lookup"><span data-stu-id="c09b4-128">Cancel the work IDs that have been created with the packing location as the final shipping location, reconfigure the location directive, and rerelease the load</span></span>

<span data-ttu-id="c09b4-129">Pomocí následujícího postupu zrušíte ID práce, která mají místo balení jako konečné umístění s automatizovanou kontejnerizací.</span><span class="sxs-lookup"><span data-stu-id="c09b4-129">Use the following procedure to cancel the work IDs that have the packing location as the final put location with automated containerization in place.</span></span>

1. <span data-ttu-id="c09b4-130">Přejděte k nabídce **Řízení skladu \> Periodické úkoly \> Vyčistit \> Zrušit práci**.</span><span class="sxs-lookup"><span data-stu-id="c09b4-130">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="c09b4-131">Otevře se dialogové okno **Zrušit práci**.</span><span class="sxs-lookup"><span data-stu-id="c09b4-131">The **Cancel work** dialog opens.</span></span> <span data-ttu-id="c09b4-132">Do pole **ID práce** zadejte ID práce, kterou chcete zrušit.</span><span class="sxs-lookup"><span data-stu-id="c09b4-132">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span> <span data-ttu-id="c09b4-133">Vybrané ID práce musí mít hodnotu **Pracovní stav** nastavenou na *Otevřeno*, *Probíhá*, *Zrušeno*, *Kombinovaéý* nebo *Uzavřeno*.</span><span class="sxs-lookup"><span data-stu-id="c09b4-133">The selected work ID must have a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="c09b4-134">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="c09b4-134">Select **OK**.</span></span>
1. <span data-ttu-id="c09b4-135">Vyberte možnost **Ano** k potvrzení, že chcete práci zrušit.</span><span class="sxs-lookup"><span data-stu-id="c09b4-135">Select **Yes** to confirm that you want to cancel the work.</span></span>
1. <span data-ttu-id="c09b4-136">Podle potřeby opakujte tento postup pro další ID práce.</span><span class="sxs-lookup"><span data-stu-id="c09b4-136">Repeat this procedure for the other work IDs as needed.</span></span>

<span data-ttu-id="c09b4-137">Další informace viz [Zrušení práce skladu pro zpracování výjimek](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="c09b4-137">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>

<span data-ttu-id="c09b4-138">Pomocí následujícího postupu překonfigurujte direktivu umístění, takže při nastavení automatické kontejnerizace pro šablonu vlny nepoužije umístění balení jako konečné místo odeslání.</span><span class="sxs-lookup"><span data-stu-id="c09b4-138">Use the following procedure to reconfigure the location directive so it won't use the packing location as the final shipping location when automated containerization is set up for the wave template.</span></span>

1. <span data-ttu-id="c09b4-139">Přejděte na **Řízení skladu \> Nastavení \> Směrnice skladového místa**.</span><span class="sxs-lookup"><span data-stu-id="c09b4-139">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="c09b4-140">V poli **Typ pracovního příkazu** vyberte možnost *Prodejní objednávky*.</span><span class="sxs-lookup"><span data-stu-id="c09b4-140">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="c09b4-141">Vyberte direktivu umístění, kterou používáte pro automatizovanou kontejnerizaci.</span><span class="sxs-lookup"><span data-stu-id="c09b4-141">Select the location directive you are using for automated containerization.</span></span>
1. <span data-ttu-id="c09b4-142">Na panelu nástrojů záložky s náhledem **Akce směrnic skladového místa** vyberte možnost **Upravit dotaz**.</span><span class="sxs-lookup"><span data-stu-id="c09b4-142">On the **Location Directive Actions** FastTab toolbar, select **Edit query**.</span></span>
1. <span data-ttu-id="c09b4-143">V dialogovém okně editoru dotazů na kartě **Oblast** najděte řádek, kde je **Pole** nastaveno na *Profil umístění* a ověřte, že pole **Kritéria** pro tento řádek není nastaveno na profil polohy, který má **Typ umístění** nastaveno na *Balení*.</span><span class="sxs-lookup"><span data-stu-id="c09b4-143">In the query editor dialog, on the **Range** tab, find the row where **Field** is set to *Location profile*, and verify that the **Criteria** field for that row is not set to a location profile that has a **Location type** of *Packing*.</span></span> <span data-ttu-id="c09b4-144">Upravte pole **Kritéria** pro opravu konečného skladového místa.</span><span class="sxs-lookup"><span data-stu-id="c09b4-144">Adjust the **Criteria** field to correct the final put location.</span></span>

<span data-ttu-id="c09b4-145">Pomocí následujícího postupu znovu uvolněte náklad a vytvořte pracovní ID se správným konečným místem odeslání.</span><span class="sxs-lookup"><span data-stu-id="c09b4-145">Use the following procedure to rerelease the load and create work IDs with the correct final shipping location.</span></span>

1. <span data-ttu-id="c09b4-146">Přejděte do **Řízení skladu \> Náklady \> Pracovní plocha plánování nákladu**.</span><span class="sxs-lookup"><span data-stu-id="c09b4-146">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="c09b4-147">V sekci **Náklady** vyhledejte náklad, který je třeba uvolnit.</span><span class="sxs-lookup"><span data-stu-id="c09b4-147">In the **Loads** section, find the load that needs to be released.</span></span>
1. <span data-ttu-id="c09b4-148">Na panelu nástrojů v sekci **Náklady** vyberte **Uvolnění \> Uvolnění do skladu** pro uvolnění vybraného nákladu do skladu.</span><span class="sxs-lookup"><span data-stu-id="c09b4-148">On the **Loads** section toolbar, select **Release \> Release to warehouse** to release the selected load to the warehouse.</span></span>
1. <span data-ttu-id="c09b4-149">Podle potřeby opakujte tento postup pro další náklady.</span><span class="sxs-lookup"><span data-stu-id="c09b4-149">Repeat this procedure for the other loads as needed.</span></span>
