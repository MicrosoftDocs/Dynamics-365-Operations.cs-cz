---
title: Ohlášení jako dokončené ze zařízení úkolového lístku
description: Toto téma popisuje, jak nakonfigurovat systém tak, aby uživatelé zařízení úkolového lístku mohli vykazovat hotové produkty z výrobní zakázky do zásob.
author: johanhoffmann
manager: tfehr
ms.date: 05/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistrationSetupTouch
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: f5d34893ddc8adc3785ec50dbd72438cf8f68c5d
ms.sourcegitcommit: 52ba8d3e6af72df5dab6c04b9684a61454d353ad
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/26/2020
ms.locfileid: "3403255"
---
# <a name="report-as-finished-from-the-job-card-device"></a><span data-ttu-id="a6bb5-103">Ohlášení jako dokončené ze zařízení úkolového lístku</span><span class="sxs-lookup"><span data-stu-id="a6bb5-103">Report as finished from the job card device</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a6bb5-104">Pracovníci používají stránku **Zpráva o pokroku** v zařízení úkolového lístku k vykazování množství, která byla dokončena pro výrobní úlohu.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-104">Workers use the **Report progress** page on the job card device to report quantities that have been completed for a production job.</span></span>

## <a name="control-whether-quantities-that-are-reported-as-finished-are-added-to-inventory"></a><span data-ttu-id="a6bb5-105">Kontrola, zda jsou do zásob přidána množství, která jsou hlášena jako hotová</span><span class="sxs-lookup"><span data-stu-id="a6bb5-105">Control whether quantities that are reported as finished are added to inventory</span></span>

<span data-ttu-id="a6bb5-106">Chcete-li určit, zda a jak se mají do zásob přidávat množství, která jsou hlášena jako hotová při poslední operaci, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-106">To control whether and how the quantities that are reported as finished on the last operation should be added to inventory, follow these steps.</span></span>

1. <span data-ttu-id="a6bb5-107">Klikněte na **Řízení výroby \> Nastavení \> Provádění výroby \> Výchozí hodnoty výrobní zakázky**.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-107">Go to **Product control \> Setup \> Manufacturing execution \> Production order defaults**.</span></span>
1. <span data-ttu-id="a6bb5-108">Na kartě **Vykázat jako hotové** nastavte pole **Aktualizovat hlášení o dokončených online** na některou z následujících hodnot:</span><span class="sxs-lookup"><span data-stu-id="a6bb5-108">On the **Report as finished** tab, set the **Update finished report on-line** field to one of the following values:</span></span>

    - <span data-ttu-id="a6bb5-109">**Ne** - Při vykazování množství při poslední operaci nebude do zásob přidáno žádné množství.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-109">**No** – No quantity will be added to inventory when quantities are reported on the last operation.</span></span> <span data-ttu-id="a6bb5-110">Stav výrobního příkazu se ale nezmění nikdy.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-110">The status of the production order will never change.</span></span>
    - <span data-ttu-id="a6bb5-111">**Stav + množství** - Stav výrobního příkazu se změní na *Hlášeno jako dokončené* a množství v zásobách bude hlášeno jako dokončené.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-111">**Status + Quantity** – The status of the production order will change to *Reported as finished*, and the quantity will be reported as finished to inventory.</span></span>
    - <span data-ttu-id="a6bb5-112">**Množství** - Množství bude hlášeno jako hotové ve skladu, ale stav výrobního příkazu se nikdy nezmění.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-112">**Quantity** – The quantity will be reported as finished to inventory, but the status of the production order will never change.</span></span>
    - <span data-ttu-id="a6bb5-113">**Stav** Změní se pouze stav výrobního příkazu.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-113">**Status** – Only the status of the production order will change.</span></span> <span data-ttu-id="a6bb5-114">Při vykazování množství při poslední operaci nebude do zásob přidáno žádné množství.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-114">No quantities will be added to inventory when quantities are reported on the last operation.</span></span>

> [!NOTE]
> <span data-ttu-id="a6bb5-115">Množství není sledováno v zásobách, pokud operace, které jsou hlášeny jako dokončené, nejsou definovány jako poslední operace.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-115">Quantities aren't tracked in inventory if the operations that they are reported as finished on aren't defined as the last operation.</span></span> <span data-ttu-id="a6bb5-116">Tato množství však lze použít k zobrazení pokroku.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-116">However, those quantities can be used to view progress.</span></span> <span data-ttu-id="a6bb5-117">Mohou být také zahrnuta do pravidel, která určují, zda pracovníci mohou zahájit další operaci před dosažením definovaného prahu vykazovaných množství při předchozí operaci.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-117">They can also be included in rules that control whether workers can start the next operation before a defined threshold of reported quantities on the previous operation is reached.</span></span> <span data-ttu-id="a6bb5-118">Tato pravidla můžete definovat na kartě **Ověření množství** stránky **Výchozí hodnoty výrobního příkazu**.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-118">You can define these rules on the **Quantity validation** tab of the **Production order defaults** page.</span></span>

<span data-ttu-id="a6bb5-119">Více informací o tom, jak pracovat se stránkou **Výchozí hodnoty výrobního příkazu** uvádí téma [Parametry výroby v realizaci výroby](production-parameters-manufacturing-execution.md).</span><span class="sxs-lookup"><span data-stu-id="a6bb5-119">For more information about how to work with the **Production order defaults** page, see [Production parameters in Manufacturing execution](production-parameters-manufacturing-execution.md).</span></span>

## <a name="report-batch-controlled-items-as-finished"></a><span data-ttu-id="a6bb5-120">Hlášení dávek kontrolovaných položek jako dokončených</span><span class="sxs-lookup"><span data-stu-id="a6bb5-120">Report batch-controlled items as finished</span></span>

<span data-ttu-id="a6bb5-121">Zařízení úkolového lístku podporuje tři scénáře pro vykazování položek dávek.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-121">The job card device supports three scenarios for reporting on batch items.</span></span> <span data-ttu-id="a6bb5-122">Tyto scénáře platí jak pro položky, které jsou povoleny pro pokročilé skladové procesy, tak pro položky, které nejsou povoleny pro pokročilé skladové procesy.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-122">These scenarios apply both to items that are enabled for advanced warehouse processes and to items that aren't enabled for advanced warehouse processes.</span></span>

- <span data-ttu-id="a6bb5-123">**Ručně přiřazená čísla dávek:** Pracovníci zadají vlastní číslo dávky.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-123">**Manually assigned batch numbers:** Workers enter a custom batch number.</span></span> <span data-ttu-id="a6bb5-124">Toto číslo dávky může pocházet z externího zdroje, který systém nezná.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-124">This batch number might come from an external source that isn't known to the system.</span></span>
- <span data-ttu-id="a6bb5-125">**Předdefinovaná čísla dávek:** Pracovníci vyberou číslo dávky ze seznamu čísel dávek, které systém automaticky vygeneruje před uvolněním výrobního příkazu do zařízení úkolového lístku.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-125">**Predefined batch numbers:** Workers select a batch number in a list of batch numbers that the system automatically generates before the production order is released to the job card device.</span></span>
- <span data-ttu-id="a6bb5-126">**Opravená čísla dávek:** Pracovníci nezadají ani nevyberou číslo dávky.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-126">**Fixed batch numbers:** Workers don't enter or select a batch number.</span></span> <span data-ttu-id="a6bb5-127">Místo toho systém automaticky přiřadí číslo dávky pracovnímu příkazu před vydáním.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-127">Instead, the system automatically assigns a batch number to the production order before it's released.</span></span>

<span data-ttu-id="a6bb5-128">Pokud chcete jednotlivé scénáře povolit, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-128">To enable each scenario, follow these steps.</span></span>

1. <span data-ttu-id="a6bb5-129">Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-129">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="a6bb5-130">Vyberte produkt ke konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-130">Select the product to configure.</span></span>
1. <span data-ttu-id="a6bb5-131">Na pevné záložce **Správa zásob** v poli **Skupina čísel dávek** vyberte skupinu čísla sledování, která je nastavená na podporu vašeho scénáře.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-131">On the **Manage inventory** FastTab, in the **Batch number group** field, select the tracking number group that is set up to support your scenario.</span></span>

> [!NOTE]
> <span data-ttu-id="a6bb5-132">Pokud není ve výchozím nastavení číslu kontrolovanému podle dávek přiřazená žádná skupina čísel dávek, poskytne zařízení úkolového lístku ruční zadání čísla dávky během vykazování jako dokončené.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-132">By default, if no batch number group is assigned to a batch-controlled product, the job card device provides manual entry for the batch number during reporting as finished.</span></span>

<span data-ttu-id="a6bb5-133">Následující podkapitoly popisují, jak nastavit skupiny sledovacích čísel na podporu každého ze tří scénářů pro vykazování položek dávek.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-133">The following subsections describe how to set up tracking number groups to support each of the three scenarios for reporting on batch items.</span></span>

### <a name="enable-batch-number-reporting-on-the-job-card-device"></a><span data-ttu-id="a6bb5-134">Povolení vykazování čísel dávek v zařízení úkolového lístku</span><span class="sxs-lookup"><span data-stu-id="a6bb5-134">Enable batch number reporting on the job card device</span></span>

<span data-ttu-id="a6bb5-135">Chcete-li povolit, aby vaše zařízení úkolového lístku přijímala číslo dávky během hlášení jako dokončené, musíte použít [správu funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) k zapnutí následujících funkcí (v tomto pořadí):</span><span class="sxs-lookup"><span data-stu-id="a6bb5-135">To enable your job card devices to accept a batch number during reporting as finished, you must use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the following features (in this order):</span></span>

1. <span data-ttu-id="a6bb5-136">Vylepšené uživatelské prostředí pro dialogové okno průběhu sestavy v zařízení úkolového lístku</span><span class="sxs-lookup"><span data-stu-id="a6bb5-136">Improved user experience for the Report progress dialog in the Job Card Device</span></span>
1. <span data-ttu-id="a6bb5-137">Umožňuje zadávat čísla dávky a sériová čísla při vykazování za dokončené v zařízení úkolového lístku (Preview)</span><span class="sxs-lookup"><span data-stu-id="a6bb5-137">Enable to enter batch and serial numbers while reporting as finished from the Job Card Device (Preview)</span></span>

### <a name="set-up-a-tracking-number-group-that-lets-workers-manually-assign-a-batch-number"></a><span data-ttu-id="a6bb5-138">Nastavení skupiny čísel sledování, která pracovníkům umožňuje ruční přiřazení čísla dávky</span><span class="sxs-lookup"><span data-stu-id="a6bb5-138">Set up a tracking number group that lets workers manually assign a batch number</span></span>

<span data-ttu-id="a6bb5-139">Při nastavení skupiny čísel tak, aby vyžadovalo od pracovníků ruční přiřazení čísel dávek, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-139">To allow for manually assigned batch numbers, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="a6bb5-140">Přejděte na **Správa zásob \> Nastavení \> Dimenze \> Skupiny čísel sledování**.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-140">Go to **Inventory management \> Setup \> Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="a6bb5-141">Vytvořte nebo vyberte skupinu sledovacích čísel, kterou chcete nastavit.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-141">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="a6bb5-142">Na pevné záložce **Obecné** nastavte možnost **Ruční** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-142">On the **General** FastTab, set the **Manual** option to **Yes**.</span></span>

    <span data-ttu-id="a6bb5-143">![Stránka skupin sledovacích čísel](media/tracking-number-group-manual.png "Stránka skupin sledovacích čísel")</span><span class="sxs-lookup"><span data-stu-id="a6bb5-143">![Tracking number groups page](media/tracking-number-group-manual.png "Tracking number groups page")</span></span>

1. <span data-ttu-id="a6bb5-144">Nastavte další hodnoty podle potřeby a poté vyberte tuto skupinu sledovacích čísel jako skupinu čísel dávek vydaných produktů, pro které chcete tento scénář použít.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-144">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="a6bb5-145">Při použití tohoto scénáře pole **Číslo dávky**, které poskytuje stránka **Nahlásit pokrok** na kartě zařízení úkolového lístku, poskytuje textové pole, do něhož mohou pracovníci zadat libovolnou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-145">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides is a text box where workers can enter any value.</span></span>

<span data-ttu-id="a6bb5-146">![Stránka hlášení pokroku s polem pro ruční čísla dávky](media/job-card-device-batch-manual.png "Stránka hlášení pokroku s polem pro ruční čísla dávky")</span><span class="sxs-lookup"><span data-stu-id="a6bb5-146">![Report progress page with a field for manual batch numbers](media/job-card-device-batch-manual.png "Report progress page with a field for manual batch numbers")</span></span>

### <a name="set-up-a-tracking-number-group-that-provides-a-list-of-predefined-batch-numbers"></a><span data-ttu-id="a6bb5-147">Nastavte skupinu sledovacích čísel, která poskytuje seznam předdefinovaných čísel dávky</span><span class="sxs-lookup"><span data-stu-id="a6bb5-147">Set up a tracking number group that provides a list of predefined batch numbers</span></span>

<span data-ttu-id="a6bb5-148">Pokud chcete poskytnout seznam předdefinovaných čísel dávky, nastavte skupinu sledovacích čísel následovně.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-148">To provide a list of predefined batch numbers, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="a6bb5-149">Přejděte na **Správa zásob \> Nastavení > Dimenze \> Skupiny čísel sledování**.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-149">Go to **Inventory management \> Setup > Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="a6bb5-150">Vytvořte nebo vyberte skupinu sledovacích čísel, kterou chcete nastavit.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-150">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="a6bb5-151">Na pevné záložce **Obecné** nastavte možnost **Pouze pro transakce zásob** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-151">On the **General** FastTab, set the **Only for inventory transactions** option to **Yes**.</span></span>
1. <span data-ttu-id="a6bb5-152">Pomocí pole **Na množství** rozdělte čísla dávky na množství na základě zadané hodnoty.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-152">Use the **Per qty.** field to split batch numbers per quantity, based on the value that you enter.</span></span> <span data-ttu-id="a6bb5-153">Například máte výrobní zakázku na deset kusů a v poli **Na množství** je nastavena hodnota *2*.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-153">For example, you have a production order for ten pieces, and the **Per qty.** field is set to *2*.</span></span> <span data-ttu-id="a6bb5-154">V takovém případě bude výrobní zakázce při vytvoření přiřazeno pět čísel dávky.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-154">In this case, five batch numbers will be assigned to the production order when it's created.</span></span>

    <span data-ttu-id="a6bb5-155">![Stránka skupin sledovacích čísel](media/tracking-number-group-predefined.png "Stránka skupin sledovacích čísel")</span><span class="sxs-lookup"><span data-stu-id="a6bb5-155">![Tracking number groups page](media/tracking-number-group-predefined.png "The Tracking number groups page")</span></span>

1. <span data-ttu-id="a6bb5-156">Nastavte další hodnoty podle potřeby a poté vyberte tuto skupinu sledovacích čísel jako skupinu čísel dávek vydaných produktů, pro které chcete tento scénář použít.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-156">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="a6bb5-157">Při použití tohoto scénáře pole **Číslo dávky**, které poskytuje stránka **Nahlásit pokrok** na zařízení úkolového lístku, představuje rozevírací seznam, kde pracovníci musí vybrat předdefinovanou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-157">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides is a drop-down list where workers must select a predefined value.</span></span>

<span data-ttu-id="a6bb5-158">![Stránka hlášení pokroku se seznamem předdefinovaných čísel dávky](media/job-card-device-batch-predefined.png "Stránka hlášení pokroku se seznamem předdefinovaných čísel dávky")</span><span class="sxs-lookup"><span data-stu-id="a6bb5-158">![Report progress page with a list of predefined batch numbers](media/job-card-device-batch-predefined.png "Report progress page with a list of predefined batch numbers")</span></span>

### <a name="set-up-a-tracking-number-group-that-automatically-assigns-batch-numbers"></a><span data-ttu-id="a6bb5-159">Nastavení skupiny čísel sledování, která automaticky přiřazuje čísla dávky</span><span class="sxs-lookup"><span data-stu-id="a6bb5-159">Set up a tracking number group that automatically assigns batch numbers</span></span>

<span data-ttu-id="a6bb5-160">Pokud mají být čísla dávky přidělována automaticky beze vstupu pracovníka, nastavte skupinu čísel sledování podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-160">If batch numbers should be assigned automatically, without worker input, follow these steps to set up a tracking number group.</span></span>

1. <span data-ttu-id="a6bb5-161">Přejděte na **Správa zásob \> Nastavení \> Dimenze \> Skupiny čísel sledování**.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-161">Go to **Inventory management \> Setup \> Dimensions \> Tracking number groups**.</span></span>
1. <span data-ttu-id="a6bb5-162">Vytvořte nebo vyberte skupinu sledovacích čísel, kterou chcete nastavit.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-162">Create or select the tracking number group to set up.</span></span>
1. <span data-ttu-id="a6bb5-163">Na pevné záložce **Obecné** nastavte možnost **Pouze pro transakce zásob** na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-163">On the **General** FastTab, set the **Only for inventory transactions** option to **No**.</span></span>
1. <span data-ttu-id="a6bb5-164">Nastavte možnost **Ruční** na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-164">Set the **Manual** option to **No**.</span></span>

    <span data-ttu-id="a6bb5-165">![Stránka skupin sledovacích čísel](media/tracking-number-group-fixed.png "Stránka skupin sledovacích čísel")</span><span class="sxs-lookup"><span data-stu-id="a6bb5-165">![Tracking number groups page](media/tracking-number-group-fixed.png "Tracking number groups page")</span></span>

1. <span data-ttu-id="a6bb5-166">Nastavte další hodnoty podle potřeby a poté vyberte tuto skupinu sledovacích čísel jako skupinu čísel dávek vydaných produktů, pro které chcete tento scénář použít.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-166">Set other values as you require, and then select this tracking number group as the batch number group for released products that you want to use this scenario for.</span></span>

<span data-ttu-id="a6bb5-167">Při použití tohoto scénáře pole **Číslo dávky**, které poskytuje stránka **Nahlásit pokrok** na kartě zařízení úkolového lístku, zobrazuje hodnotu, kterou však pracovníci nemohou upravovat.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-167">When you use this scenario, the **Batch number** field that the **Report progress** page on the job card device provides shows a value, but workers can't edit it.</span></span>

<span data-ttu-id="a6bb5-168">![Stránka hlášení pokroku s polem pro pevná čísla dávky](media/job-card-device-batch-fixed.png "Stránka hlášení pokroku s polem pro pevná čísla dávky")</span><span class="sxs-lookup"><span data-stu-id="a6bb5-168">![Report progress page with a fixed batch number](media/job-card-device-batch-fixed.png "Report progress page with a fixed batch number")</span></span>

## <a name="report-as-finished-to-a-license-plate"></a><span data-ttu-id="a6bb5-169">Nahlášení jako dokončené do registrační značky</span><span class="sxs-lookup"><span data-stu-id="a6bb5-169">Report as finished to a license plate</span></span>

<span data-ttu-id="a6bb5-170">Pokročilé skladové procesy mohou pomocí rozměru registrační značky sledovat zásoby ve skladovacích místech, která byla pro tento účel nastavena.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-170">Advanced warehouse processes can use the license plate dimension to track inventory on warehouse locations that have been set up for this purpose.</span></span> <span data-ttu-id="a6bb5-171">V tomto případě je registrační značka vyžadována, když pracovník nahlásí množství jako dokončená.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-171">In this case, the license plate number is required when a worker reports quantities as finished.</span></span>

### <a name="enable-license-plate-reporting-and-label-printing"></a><span data-ttu-id="a6bb5-172">Povolení vykazování registrační značky a tisku štítku</span><span class="sxs-lookup"><span data-stu-id="a6bb5-172">Enable license plate reporting and label printing</span></span>

<span data-ttu-id="a6bb5-173">Chcete-li používat funkce popsané v této části, musíte použít [správu funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) pro zapnutí následujících funkcí (v tomto pořadí):</span><span class="sxs-lookup"><span data-stu-id="a6bb5-173">To use the features that are described in this section, you must use [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn on the following features (in this order):</span></span>

1. <span data-ttu-id="a6bb5-174">Registrační značka pro vykazování jako dokončené přidána do zařízení úkolového lístku</span><span class="sxs-lookup"><span data-stu-id="a6bb5-174">License plate for reporting as finished added to the Job Card Device</span></span>
1. <span data-ttu-id="a6bb5-175">Povolit automatické generování čísla registrační značky při vykazování jako dokončeno v zařízení úkolového lístku</span><span class="sxs-lookup"><span data-stu-id="a6bb5-175">Enable automatic generation of license plate number when reporting as finished in the job card device</span></span>
1. <span data-ttu-id="a6bb5-176">Vytisknout štítek ze zařízení úkolového lístku</span><span class="sxs-lookup"><span data-stu-id="a6bb5-176">Print label from Job Card Device</span></span>

### <a name="set-up-reporting-as-finished-to-a-license-plate"></a><span data-ttu-id="a6bb5-177">Nastavení hlášení jako dokončené do registrační značky</span><span class="sxs-lookup"><span data-stu-id="a6bb5-177">Set up reporting as finished to a license plate</span></span>

<span data-ttu-id="a6bb5-178">Chcete-li určit, zda by pracovníci měli znovu použít existující registrační značku nebo vygenerovat novou registrační značku, když ohlásí množství jako dokončené, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-178">To control whether workers should reuse an existing license plate or generate a new license plate when they report quantities as finished, follow these steps.</span></span>

1. <span data-ttu-id="a6bb5-179">Přejděte do nabídky **Řízení výroby \> Nastavení \> Provádění výroby \> Konfigurovat úkolový lístek pro zařízení**.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-179">Go to **Production control \> Setup \> Manufacturing execution \> Configure job card for devices**.</span></span>
2. <span data-ttu-id="a6bb5-180">U každého zařízení nastavte následující možnosti:</span><span class="sxs-lookup"><span data-stu-id="a6bb5-180">Set the following options for each device:</span></span>

    - <span data-ttu-id="a6bb5-181">**Generovat registrační značku** – Nastavením této možnosti na **Ano** vygenerujete novou registrační značku pro každé nahlášení jako dokončené.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-181">**Generate license plate** – Set this option to **Yes** to generate a new license plate for each report as finished.</span></span> <span data-ttu-id="a6bb5-182">Nastavte ji na **Ne**, pokud by se pro každé hlášení měla použít stávající registrační značka.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-182">Set it to **No** if an existing license plate should be used for each report as finished.</span></span>
    - <span data-ttu-id="a6bb5-183">**Tisk štítku** – Nastavte tuto možnost na **Ano**, pokud pracovník musí vytisknout registrační značku pro každé hlášení jako dokončené.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-183">**Print label** – Set this option to **Yes** if the worker must print a license plate label for each report as finished.</span></span> <span data-ttu-id="a6bb5-184">Nastavte ji na **Ne**, pokud není vyžadován žádný popisek.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-184">Set it to **No** if no label is required.</span></span> 

<span data-ttu-id="a6bb5-185">![Stránka Konfigurovat úkolový lístek pro zařízení](media/config-job-card-raf.png "Stránka Konfigurovat úkolový lístek pro zařízení")</span><span class="sxs-lookup"><span data-stu-id="a6bb5-185">![Configure job card for devices page](media/config-job-card-raf.png "Configure job card for devices page")</span></span>

> [!NOTE]
> <span data-ttu-id="a6bb5-186">Pokud chcete konfigurovat štítek, přejděte na **Správa skladu \> Nastavení \> Směrování dokumentu \> Směrování dokumentu**.</span><span class="sxs-lookup"><span data-stu-id="a6bb5-186">To configure the label, go to **Warehouse management \> Setup \> Document routing \> Document routing**.</span></span> <span data-ttu-id="a6bb5-187">Další informace získáte v části [Povolení tisku štítků registračních značek](../warehousing/tasks/license-plate-label-printing.md).</span><span class="sxs-lookup"><span data-stu-id="a6bb5-187">For more information, see [Enable license plate label printing](../warehousing/tasks/license-plate-label-printing.md).</span></span>
