---
title: Poradce při potížích s výdejem a balením
description: Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při výdeji a balení v Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 01e33b63e09a035f5243bd57faf53b522737c987
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5223235"
---
# <a name="troubleshoot-picking-and-packing"></a><span data-ttu-id="727e1-103">Poradce při potížích s výdejem a balením</span><span class="sxs-lookup"><span data-stu-id="727e1-103">Troubleshoot picking and packing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="727e1-104">Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při výdeji a balení v Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="727e1-104">This topic describes how to fix common issues that you might encounter while you pick and pack in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-dimension-location-cant-be-left-blank-if-dimension-serial-number-is-set"></a><span data-ttu-id="727e1-105">Zobrazí se následující chybová zpráva: „Umístění dimenze nemůže zůstat prázdné, pokud je nastaveno sériové číslo dimenze.“</span><span class="sxs-lookup"><span data-stu-id="727e1-105">I receive the following error message: "Dimension location can't be left blank if dimension serial number is set."</span></span>

### <a name="issue-description"></a><span data-ttu-id="727e1-106">Popis problému</span><span class="sxs-lookup"><span data-stu-id="727e1-106">Issue description</span></span>

<span data-ttu-id="727e1-107">Tato chybová zpráva se zobrazí, pokud vytvoříte převodní příkaz pro sériovou položku pomocí skladu, který je povolen pro pokročilou správu skladu (WMS), a po dokončení práce se pokusíte potvrdit zásilku.</span><span class="sxs-lookup"><span data-stu-id="727e1-107">You receive this error message if you create a transfer order for a serial item by using a warehouse that is enabled for advanced warehouse management (WMS), and then, after the work is completed, you try to confirm the shipment.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="727e1-108">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="727e1-108">Issue resolution</span></span>

<span data-ttu-id="727e1-109">Pole **Výchozí skladové místo příjmu** je prázdné pro tranzitní sklad ze skladu.</span><span class="sxs-lookup"><span data-stu-id="727e1-109">The **Default receipt location** field is blank for a transit warehouse of the "from" warehouse.</span></span> <span data-ttu-id="727e1-110">Chcete-li tento problém vyřešit, zadejte výchozí skladové místo příjmu v tranzitním skladu.</span><span class="sxs-lookup"><span data-stu-id="727e1-110">To fix this issue, specify a default receipt location in the transit warehouse.</span></span> <span data-ttu-id="727e1-111">Ujistěte se, že toto umístění je řízeno registrační značkou.</span><span class="sxs-lookup"><span data-stu-id="727e1-111">Make sure that this location is license plate–controlled.</span></span>

## <a name="i-receive-the-following-error-message-invalid-license-plate"></a><span data-ttu-id="727e1-112">Zobrazuje se následující chybová zpráva: „Neplatná registrační značka.“</span><span class="sxs-lookup"><span data-stu-id="727e1-112">I receive the following error message: "Invalid license plate."</span></span>

### <a name="issue-description"></a><span data-ttu-id="727e1-113">Popis problému</span><span class="sxs-lookup"><span data-stu-id="727e1-113">Issue description</span></span>

<span data-ttu-id="727e1-114">Tato chybová zpráva se zobrazí v aplikaci skladu při skenování ID registrační značky.</span><span class="sxs-lookup"><span data-stu-id="727e1-114">You receive this error message in the warehouse app when you scan a license plate ID.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="727e1-115">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="727e1-115">Issue resolution</span></span>

<span data-ttu-id="727e1-116">Ujistěte se, že v tabulce registračních značek existuje ID registrační značky a že položky a množství na registrační značce jsou k dispozici (jinými slovy nejsou blokovány).</span><span class="sxs-lookup"><span data-stu-id="727e1-116">Make sure that the license plate ID exists in the license plates table, and that the items and quantities on the license plate are available (in other words, they aren't blocked).</span></span>

## <a name="i-receive-the-following-error-message-field-load-weight-1-can-only-contain-positive-numbers-update-has-been-canceled"></a><span data-ttu-id="727e1-117">Zobrazuje se následující chybová zpráva: „Pole 'Hmotnost nákladu'(=-%1) může obsahovat pouze kladná čísla.</span><span class="sxs-lookup"><span data-stu-id="727e1-117">I receive the following error message: "Field 'Load weight'(=-%1) can only contain positive numbers.</span></span> <span data-ttu-id="727e1-118">Aktualizace byla zrušena."</span><span class="sxs-lookup"><span data-stu-id="727e1-118">Update has been canceled."</span></span>

### <a name="issue-description"></a><span data-ttu-id="727e1-119">Popis problému</span><span class="sxs-lookup"><span data-stu-id="727e1-119">Issue description</span></span>

<span data-ttu-id="727e1-120">Tato chybová zpráva se zobrazí, pokud existuje otevřená práce při zpracování práce z umístění balení do přechodných skladových míst nebo z přechodných skladových míst do umístění překladiště.</span><span class="sxs-lookup"><span data-stu-id="727e1-120">You receive this error message if there is open work when you process work from packing locations to staging locations, or from staging locations to dock locations.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="727e1-121">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="727e1-121">Issue resolution</span></span>

<span data-ttu-id="727e1-122">Abyste tento problém vyřešili, přejděte na **Správa systému \> Pravidelné úkoly \> Databáze \> Kontrola konzistence** a spusťte proces pro **Kontrola konzistence hmotnosti nákladu skladu**.</span><span class="sxs-lookup"><span data-stu-id="727e1-122">To fix this issue, go to **System administration \> Periodic tasks \> Database \> Consistency check**, and run the process for **Warehouse load weight consistency check**.</span></span>

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a><span data-ttu-id="727e1-123">Zobrazuje se následující chybová zpráva: „Množství není platné pro jednotku %1.“</span><span class="sxs-lookup"><span data-stu-id="727e1-123">I receive the following error message: "The quantity is not valid for unit %1."</span></span>

### <a name="issue-description"></a><span data-ttu-id="727e1-124">Popis problému</span><span class="sxs-lookup"><span data-stu-id="727e1-124">Issue description</span></span>

<span data-ttu-id="727e1-125">Tato chybová zpráva se zobrazí, když se pokusíte provést a *rozdělený výdej* ve více dávkách.</span><span class="sxs-lookup"><span data-stu-id="727e1-125">You receive this error message when you try to perform a *split pick* across multiple batches.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="727e1-126">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="727e1-126">Issue resolution</span></span>

<span data-ttu-id="727e1-127">Pracovník skladu musí používat proces *Krátkodobé vyskladnění* v aplikaci skladu.</span><span class="sxs-lookup"><span data-stu-id="727e1-127">The warehouse worker must use the *Short picking* process in the warehouse app.</span></span> <span data-ttu-id="727e1-128">Pokud se snažíte o výdej více dávek ze stejného místa, můžete také použít možnost **Úplný** v aplikaci skladu.</span><span class="sxs-lookup"><span data-stu-id="727e1-128">If you're trying to pick multiple batches from the same location, you can also use the **Full** option in the warehouse app.</span></span>

## <a name="i-cant-move-inventory-to-a-location-that-is-license-platecontrolled"></a><span data-ttu-id="727e1-129">Nemohu přesunout inventář na místo, kde se kontrolují registrační značky.</span><span class="sxs-lookup"><span data-stu-id="727e1-129">I can't move inventory to a location that is license plate–controlled.</span></span>

### <a name="issue-description"></a><span data-ttu-id="727e1-130">Popis problému</span><span class="sxs-lookup"><span data-stu-id="727e1-130">Issue description</span></span>

<span data-ttu-id="727e1-131">Vydaná množství v nákladu nelze snížit.</span><span class="sxs-lookup"><span data-stu-id="727e1-131">You can't reduce picked quantities on a load.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="727e1-132">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="727e1-132">Issue resolution</span></span>

<span data-ttu-id="727e1-133">V předchozích verzích vyskladněné množství v nákladu nelze snížit.</span><span class="sxs-lookup"><span data-stu-id="727e1-133">In earlier versions, you can't reduce picked quantities on a load.</span></span> <span data-ttu-id="727e1-134">Nyní však můžete zrušit výdej v umístění, kde se kontroluje registrační značka.</span><span class="sxs-lookup"><span data-stu-id="727e1-134">However, you can now unpick to a license plate–controlled location.</span></span> <span data-ttu-id="727e1-135">Musíte zadat hodnotu **Umístění** i hodnotu **Registrační značka** pro řádek nákladu na stránce **Snižte vydané množství**.</span><span class="sxs-lookup"><span data-stu-id="727e1-135">You must specify both a **Location** value and a **License plate** value for the load line on the **Reduce picked quantity** page.</span></span>

## <a name="can-i-print-a-delivery-note-or-packing-content-by-warehouse"></a><span data-ttu-id="727e1-136">Mohu vytisknout poznámku k dodání nebo balicí obsah podle skladu?</span><span class="sxs-lookup"><span data-stu-id="727e1-136">Can I print a delivery note or packing content by warehouse?</span></span>

### <a name="issue-description"></a><span data-ttu-id="727e1-137">Popis problému</span><span class="sxs-lookup"><span data-stu-id="727e1-137">Issue description</span></span>

<span data-ttu-id="727e1-138">Chcete vytisknout poznámku k dodání nebo balicí obsah podle skladu nebo místa na stránce **Aktualizace řádku šablony pracovního auditu**.</span><span class="sxs-lookup"><span data-stu-id="727e1-138">You want to print a delivery note or packing content by warehouse or site on the **Work audit template line update** page.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="727e1-139">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="727e1-139">Issue resolution</span></span>

<span data-ttu-id="727e1-140">Když tisknete dokument pomocí nastavení správy tisku, omezte rozsah (místo / sklad) prostřednictvím správy tisku místo výběru **Upravit nastavení tisku** na stránce **Aktualizace řádku šablony pracovního auditu**.</span><span class="sxs-lookup"><span data-stu-id="727e1-140">When you print a document by using Print management settings, limit the scope (site/warehouse) through Print management instead of by selecting **Edit print settings** on the **Work audit template line update** page.</span></span>

## <a name="i-cant-cancel-a-packing-slip-after-its-posted-from-a-sales-order"></a><span data-ttu-id="727e1-141">Po zaúčtování z prodejní objednávky nemůžu zrušit dodací list.</span><span class="sxs-lookup"><span data-stu-id="727e1-141">I can't cancel a packing slip after it's posted from a sales order.</span></span>

### <a name="issue-description"></a><span data-ttu-id="727e1-142">Popis problému</span><span class="sxs-lookup"><span data-stu-id="727e1-142">Issue description</span></span>

<span data-ttu-id="727e1-143">Když jsou pro WMS povoleny procesy výdeje a expedice, nemůžete zrušit dodací list poté, co je zaúčtován z prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="727e1-143">When picking and shipping processes are enabled for WMS, you can't cancel a packing slip after it's posted from a sales order.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="727e1-144">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="727e1-144">Issue resolution</span></span>

<span data-ttu-id="727e1-145">Chcete-li opravit zaúčtované dodací listy pro položky, které jsou povoleny pro WMS, musíte zaúčtování provést z nákladu, nikoli přímo z objednávky.</span><span class="sxs-lookup"><span data-stu-id="727e1-145">To correct posted packing slips for items that are enabled for WMS, the posting must occur from the load, not from the order.</span></span> <span data-ttu-id="727e1-146">Společnost Microsoft vyhodnotila tento problém a zjistila, že jde o omezení funkcí.</span><span class="sxs-lookup"><span data-stu-id="727e1-146">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="727e1-147">Obecně platí, že u prodejní objednávky, která byla vybrána a odeslána prostřednictvím procesů správy skladu, může být dodací list aktualizován z nákladu nebo dodávky a samotného dokladu prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="727e1-147">In general, a sales order that has been picked and shipped through warehouse management processes can be packing slip–updated from the load or shipment and the sales order document itself.</span></span> <span data-ttu-id="727e1-148">Pokud však u prodejní objednávky aktualizujete dodací list z dokladu prodejní objednávky, nelze přesto z nákladu nebo prodejní objednávky provést změnu dodacího listu.</span><span class="sxs-lookup"><span data-stu-id="727e1-148">However, if you packing slip–update the sales order from the sales order document, packing slip reversal still can't be done from the load or sales order.</span></span> <span data-ttu-id="727e1-149">Proto doporučujeme použít zaúčtování dodacího listu z nákladu.</span><span class="sxs-lookup"><span data-stu-id="727e1-149">Therefore, we recommend that you use the packing slip posting from the load.</span></span> <span data-ttu-id="727e1-150">V takovém případě bude povolen reverz, který musí být proveden z nákladu.</span><span class="sxs-lookup"><span data-stu-id="727e1-150">In this case, the reversal that must be done from the load will be enabled.</span></span>

## <a name="i-receive-the-following-error-message-not-enough-work-can-be-found-for-cluster"></a><span data-ttu-id="727e1-151">Zobrazí se mi následující chybová zpráva: "Pro seskupení nelze najít dostatek práce."</span><span class="sxs-lookup"><span data-stu-id="727e1-151">I receive the following error message: "Not enough work can be found for cluster."</span></span>

### <a name="issue-description"></a><span data-ttu-id="727e1-152">Popis problému</span><span class="sxs-lookup"><span data-stu-id="727e1-152">Issue description</span></span>

<span data-ttu-id="727e1-153">Když používáte proces *Systémově řízený výdej seskupení*, pokud nakonfigurujete profil seskupení, kde lze vybrat například 10 pozic, proces funguje podle plánu, když je dostatek práce k výdeji do 10 pozic.</span><span class="sxs-lookup"><span data-stu-id="727e1-153">When you use the *System directed cluster picking* process, if you configure a cluster profile where, for example, 10 positions can be picked, the process works as planned when there is enough work to pick to 10 positions.</span></span> <span data-ttu-id="727e1-154">Pokud však můžete vybrat pouze osm pozic, zobrazí se tato chybová zpráva, protože pro jedno seskupení není dostatek práce.</span><span class="sxs-lookup"><span data-stu-id="727e1-154">However, if there are only eight positions to pick, you receive this error message, because there isn't enough work for one cluster.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="727e1-155">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="727e1-155">Issue resolution</span></span>

<span data-ttu-id="727e1-156">Chcete-li tento problém vyřešit, upravte profil seskupení a nastavte možnost **Aktivovat pozice** na *Ne*.</span><span class="sxs-lookup"><span data-stu-id="727e1-156">To fix this issue, edit the cluster profile, and set the **Activate positions** option to *No*.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]