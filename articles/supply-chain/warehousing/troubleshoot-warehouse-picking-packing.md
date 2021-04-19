---
title: Poradce při potížích s výdejem a balením
description: Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při výdeji a balení v Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 1a54fa9dc21fb1691d74905a1215f4dfea31f136
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828123"
---
# <a name="troubleshoot-picking-and-packing"></a><span data-ttu-id="3cca3-103">Poradce při potížích s výdejem a balením</span><span class="sxs-lookup"><span data-stu-id="3cca3-103">Troubleshoot picking and packing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3cca3-104">Toto téma popisuje, jak vyřešit běžné problémy, s nimiž se můžete setkat při výdeji a balení v Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="3cca3-104">This topic describes how to fix common issues that you might encounter while you pick and pack in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-dimension-location-cant-be-left-blank-if-dimension-serial-number-is-set"></a><span data-ttu-id="3cca3-105">Zobrazí se následující chybová zpráva: „Umístění dimenze nemůže zůstat prázdné, pokud je nastaveno sériové číslo dimenze.“</span><span class="sxs-lookup"><span data-stu-id="3cca3-105">I receive the following error message: "Dimension location can't be left blank if dimension serial number is set."</span></span>

### <a name="issue-description"></a><span data-ttu-id="3cca3-106">Popis problému</span><span class="sxs-lookup"><span data-stu-id="3cca3-106">Issue description</span></span>

<span data-ttu-id="3cca3-107">Tato chybová zpráva se zobrazí, pokud vytvoříte převodní příkaz pro sériovou položku pomocí skladu, který je povolen pro pokročilou správu skladu (WMS), a po dokončení práce se pokusíte potvrdit zásilku.</span><span class="sxs-lookup"><span data-stu-id="3cca3-107">You receive this error message if you create a transfer order for a serial item by using a warehouse that is enabled for advanced warehouse management (WMS), and then, after the work is completed, you try to confirm the shipment.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="3cca3-108">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="3cca3-108">Issue resolution</span></span>

<span data-ttu-id="3cca3-109">Pole **Výchozí skladové místo příjmu** je prázdné pro tranzitní sklad ze skladu.</span><span class="sxs-lookup"><span data-stu-id="3cca3-109">The **Default receipt location** field is blank for a transit warehouse of the "from" warehouse.</span></span> <span data-ttu-id="3cca3-110">Chcete-li tento problém vyřešit, zadejte výchozí skladové místo příjmu v tranzitním skladu.</span><span class="sxs-lookup"><span data-stu-id="3cca3-110">To fix this issue, specify a default receipt location in the transit warehouse.</span></span> <span data-ttu-id="3cca3-111">Ujistěte se, že toto umístění je řízeno registrační značkou.</span><span class="sxs-lookup"><span data-stu-id="3cca3-111">Make sure that this location is license plate–controlled.</span></span>

## <a name="i-receive-the-following-error-message-invalid-license-plate"></a><span data-ttu-id="3cca3-112">Zobrazuje se následující chybová zpráva: „Neplatná registrační značka.“</span><span class="sxs-lookup"><span data-stu-id="3cca3-112">I receive the following error message: "Invalid license plate."</span></span>

### <a name="issue-description"></a><span data-ttu-id="3cca3-113">Popis problému</span><span class="sxs-lookup"><span data-stu-id="3cca3-113">Issue description</span></span>

<span data-ttu-id="3cca3-114">Tato chybová zpráva se zobrazí v mobilní aplikaci Řízení skladu při skenování ID registrační značky.</span><span class="sxs-lookup"><span data-stu-id="3cca3-114">You receive this error message in the Warehouse Management mobile app when you scan a license plate ID.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="3cca3-115">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="3cca3-115">Issue resolution</span></span>

<span data-ttu-id="3cca3-116">Ujistěte se, že v tabulce registračních značek existuje ID registrační značky a že položky a množství na registrační značce jsou k dispozici (jinými slovy nejsou blokovány).</span><span class="sxs-lookup"><span data-stu-id="3cca3-116">Make sure that the license plate ID exists in the license plates table, and that the items and quantities on the license plate are available (in other words, they aren't blocked).</span></span>

## <a name="i-receive-the-following-error-message-field-load-weight-1-can-only-contain-positive-numbers-update-has-been-canceled"></a><span data-ttu-id="3cca3-117">Zobrazuje se následující chybová zpráva: „Pole 'Hmotnost nákladu'(=-%1) může obsahovat pouze kladná čísla.</span><span class="sxs-lookup"><span data-stu-id="3cca3-117">I receive the following error message: "Field 'Load weight'(=-%1) can only contain positive numbers.</span></span> <span data-ttu-id="3cca3-118">Aktualizace byla zrušena."</span><span class="sxs-lookup"><span data-stu-id="3cca3-118">Update has been canceled."</span></span>

### <a name="issue-description"></a><span data-ttu-id="3cca3-119">Popis problému</span><span class="sxs-lookup"><span data-stu-id="3cca3-119">Issue description</span></span>

<span data-ttu-id="3cca3-120">Tato chybová zpráva se zobrazí, pokud existuje otevřená práce při zpracování práce z umístění balení do přechodných skladových míst nebo z přechodných skladových míst do umístění překladiště.</span><span class="sxs-lookup"><span data-stu-id="3cca3-120">You receive this error message if there is open work when you process work from packing locations to staging locations, or from staging locations to dock locations.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="3cca3-121">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="3cca3-121">Issue resolution</span></span>

<span data-ttu-id="3cca3-122">Abyste tento problém vyřešili, přejděte na **Správa systému \> Pravidelné úkoly \> Databáze \> Kontrola konzistence** a spusťte proces pro **Kontrola konzistence hmotnosti nákladu skladu**.</span><span class="sxs-lookup"><span data-stu-id="3cca3-122">To fix this issue, go to **System administration \> Periodic tasks \> Database \> Consistency check**, and run the process for **Warehouse load weight consistency check**.</span></span>

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a><span data-ttu-id="3cca3-123">Zobrazuje se následující chybová zpráva: „Množství není platné pro jednotku %1.“</span><span class="sxs-lookup"><span data-stu-id="3cca3-123">I receive the following error message: "The quantity is not valid for unit %1."</span></span>

### <a name="issue-description"></a><span data-ttu-id="3cca3-124">Popis problému</span><span class="sxs-lookup"><span data-stu-id="3cca3-124">Issue description</span></span>

<span data-ttu-id="3cca3-125">Tato chybová zpráva se zobrazí, když se pokusíte provést a *rozdělený výdej* ve více dávkách.</span><span class="sxs-lookup"><span data-stu-id="3cca3-125">You receive this error message when you try to perform a *split pick* across multiple batches.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="3cca3-126">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="3cca3-126">Issue resolution</span></span>

<span data-ttu-id="3cca3-127">Pracovník skladu musí používat proces *Krátkodobé vyskladnění* v mobilní aplikaci Řízení skladu.</span><span class="sxs-lookup"><span data-stu-id="3cca3-127">The warehouse worker must use the *Short picking* process in the Warehouse Management mobile app.</span></span> <span data-ttu-id="3cca3-128">Pokud se snažíte o výdej více dávek ze stejného místa, můžete také použít možnost **Úplný** v aplikaci.</span><span class="sxs-lookup"><span data-stu-id="3cca3-128">If you're trying to pick multiple batches from the same location, you can also use the **Full** option in the app.</span></span>

## <a name="i-cant-move-inventory-to-a-location-that-is-license-platecontrolled"></a><span data-ttu-id="3cca3-129">Nemohu přesunout inventář na místo, kde se kontrolují registrační značky.</span><span class="sxs-lookup"><span data-stu-id="3cca3-129">I can't move inventory to a location that is license plate–controlled.</span></span>

### <a name="issue-description"></a><span data-ttu-id="3cca3-130">Popis problému</span><span class="sxs-lookup"><span data-stu-id="3cca3-130">Issue description</span></span>

<span data-ttu-id="3cca3-131">Vydaná množství v nákladu nelze snížit.</span><span class="sxs-lookup"><span data-stu-id="3cca3-131">You can't reduce picked quantities on a load.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="3cca3-132">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="3cca3-132">Issue resolution</span></span>

<span data-ttu-id="3cca3-133">V předchozích verzích vyskladněné množství v nákladu nelze snížit.</span><span class="sxs-lookup"><span data-stu-id="3cca3-133">In earlier versions, you can't reduce picked quantities on a load.</span></span> <span data-ttu-id="3cca3-134">Nyní však můžete zrušit výdej v umístění, kde se kontroluje registrační značka.</span><span class="sxs-lookup"><span data-stu-id="3cca3-134">However, you can now unpick to a license plate–controlled location.</span></span> <span data-ttu-id="3cca3-135">Musíte zadat hodnotu **Umístění** i hodnotu **Registrační značka** pro řádek nákladu na stránce **Snižte vydané množství**.</span><span class="sxs-lookup"><span data-stu-id="3cca3-135">You must specify both a **Location** value and a **License plate** value for the load line on the **Reduce picked quantity** page.</span></span>

## <a name="can-i-print-a-delivery-note-or-packing-content-by-warehouse"></a><span data-ttu-id="3cca3-136">Mohu vytisknout poznámku k dodání nebo balicí obsah podle skladu?</span><span class="sxs-lookup"><span data-stu-id="3cca3-136">Can I print a delivery note or packing content by warehouse?</span></span>

### <a name="issue-description"></a><span data-ttu-id="3cca3-137">Popis problému</span><span class="sxs-lookup"><span data-stu-id="3cca3-137">Issue description</span></span>

<span data-ttu-id="3cca3-138">Chcete vytisknout poznámku k dodání nebo balicí obsah podle skladu nebo místa na stránce **Aktualizace řádku šablony pracovního auditu**.</span><span class="sxs-lookup"><span data-stu-id="3cca3-138">You want to print a delivery note or packing content by warehouse or site on the **Work audit template line update** page.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="3cca3-139">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="3cca3-139">Issue resolution</span></span>

<span data-ttu-id="3cca3-140">Když tisknete dokument pomocí nastavení správy tisku, omezte rozsah (místo / sklad) prostřednictvím správy tisku místo výběru **Upravit nastavení tisku** na stránce **Aktualizace řádku šablony pracovního auditu**.</span><span class="sxs-lookup"><span data-stu-id="3cca3-140">When you print a document by using Print management settings, limit the scope (site/warehouse) through Print management instead of by selecting **Edit print settings** on the **Work audit template line update** page.</span></span>

## <a name="i-cant-cancel-a-packing-slip-after-its-posted-from-a-sales-order"></a><span data-ttu-id="3cca3-141">Po zaúčtování z prodejní objednávky nemůžu zrušit dodací list.</span><span class="sxs-lookup"><span data-stu-id="3cca3-141">I can't cancel a packing slip after it's posted from a sales order.</span></span>

### <a name="issue-description"></a><span data-ttu-id="3cca3-142">Popis problému</span><span class="sxs-lookup"><span data-stu-id="3cca3-142">Issue description</span></span>

<span data-ttu-id="3cca3-143">Když jsou pro WMS povoleny procesy výdeje a expedice, nemůžete zrušit dodací list poté, co je zaúčtován z prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="3cca3-143">When picking and shipping processes are enabled for WMS, you can't cancel a packing slip after it's posted from a sales order.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="3cca3-144">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="3cca3-144">Issue resolution</span></span>

<span data-ttu-id="3cca3-145">Chcete-li opravit zaúčtované dodací listy pro položky, které jsou povoleny pro WMS, musíte zaúčtování provést z nákladu, nikoli přímo z objednávky.</span><span class="sxs-lookup"><span data-stu-id="3cca3-145">To correct posted packing slips for items that are enabled for WMS, the posting must occur from the load, not from the order.</span></span> <span data-ttu-id="3cca3-146">Společnost Microsoft vyhodnotila tento problém a zjistila, že jde o omezení funkcí.</span><span class="sxs-lookup"><span data-stu-id="3cca3-146">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="3cca3-147">Obecně platí, že u prodejní objednávky, která byla vybrána a odeslána prostřednictvím procesů správy skladu, může být dodací list aktualizován z nákladu nebo dodávky a samotného dokladu prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="3cca3-147">In general, a sales order that has been picked and shipped through warehouse management processes can be packing slip–updated from the load or shipment and the sales order document itself.</span></span> <span data-ttu-id="3cca3-148">Pokud však u prodejní objednávky aktualizujete dodací list z dokladu prodejní objednávky, nelze přesto z nákladu nebo prodejní objednávky provést změnu dodacího listu.</span><span class="sxs-lookup"><span data-stu-id="3cca3-148">However, if you packing slip–update the sales order from the sales order document, packing slip reversal still can't be done from the load or sales order.</span></span> <span data-ttu-id="3cca3-149">Proto doporučujeme použít zaúčtování dodacího listu z nákladu.</span><span class="sxs-lookup"><span data-stu-id="3cca3-149">Therefore, we recommend that you use the packing slip posting from the load.</span></span> <span data-ttu-id="3cca3-150">V takovém případě bude povolen reverz, který musí být proveden z nákladu.</span><span class="sxs-lookup"><span data-stu-id="3cca3-150">In this case, the reversal that must be done from the load will be enabled.</span></span>

## <a name="i-receive-the-following-error-message-not-enough-work-can-be-found-for-cluster"></a><span data-ttu-id="3cca3-151">Zobrazí se mi následující chybová zpráva: "Pro seskupení nelze najít dostatek práce."</span><span class="sxs-lookup"><span data-stu-id="3cca3-151">I receive the following error message: "Not enough work can be found for cluster."</span></span>

### <a name="issue-description"></a><span data-ttu-id="3cca3-152">Popis problému</span><span class="sxs-lookup"><span data-stu-id="3cca3-152">Issue description</span></span>

<span data-ttu-id="3cca3-153">Když používáte proces *Systémově řízený výdej seskupení*, pokud nakonfigurujete profil seskupení, kde lze vybrat například 10 pozic, proces funguje podle plánu, když je dostatek práce k výdeji do 10 pozic.</span><span class="sxs-lookup"><span data-stu-id="3cca3-153">When you use the *System directed cluster picking* process, if you configure a cluster profile where, for example, 10 positions can be picked, the process works as planned when there is enough work to pick to 10 positions.</span></span> <span data-ttu-id="3cca3-154">Pokud však můžete vybrat pouze osm pozic, zobrazí se tato chybová zpráva, protože pro jedno seskupení není dostatek práce.</span><span class="sxs-lookup"><span data-stu-id="3cca3-154">However, if there are only eight positions to pick, you receive this error message, because there isn't enough work for one cluster.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="3cca3-155">Řešení problému</span><span class="sxs-lookup"><span data-stu-id="3cca3-155">Issue resolution</span></span>

<span data-ttu-id="3cca3-156">Chcete-li tento problém vyřešit, upravte profil seskupení a nastavte možnost **Aktivovat pozice** na *Ne*.</span><span class="sxs-lookup"><span data-stu-id="3cca3-156">To fix this issue, edit the cluster profile, and set the **Activate positions** option to *No*.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]