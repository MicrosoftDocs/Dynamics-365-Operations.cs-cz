---
title: Naplánování vytvoření práce během vlny
description: Toto téma popisuje, jak nastavit a používat metodu zpracování ve vlnách Zpracovat vytvoření práce.
author: perlynne
manager: mirzaab
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ed8f43c7db139b7b16ac6901d5db56ba2f021690
ms.sourcegitcommit: b7a7a14f8650913f6797ae1c4a82ad8adfe415fd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/28/2021
ms.locfileid: "5078240"
---
# <a name="schedule-work-creation-during-wave"></a><span data-ttu-id="37b7b-103">Naplánování vytvoření práce během vlny</span><span class="sxs-lookup"><span data-stu-id="37b7b-103">Schedule work creation during wave</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="37b7b-104">Použijte funkci *Naplánovat vytvoření práce* jako součást vašeho procesu vln, která pomáhá zvýšit propustnost zpracování ve vlnách tím, že systém vytvoří práci pomocí paralelního zpracování.</span><span class="sxs-lookup"><span data-stu-id="37b7b-104">Use the *Schedule work creation* feature as part of your waving process to help increase wave processing throughput by having the system create work using parallel processing.</span></span>

<span data-ttu-id="37b7b-105">Když je funkce povolena, automaticky se vytvoří plánovaná práce, kterou systém nakonec zpracuje a vytvoří skutečnou práci.</span><span class="sxs-lookup"><span data-stu-id="37b7b-105">When the functionality is enabled, planned work will automatically get created, which the system will eventually process to create actual work.</span></span> <span data-ttu-id="37b7b-106">Pokud počet linek zatížení ve vlnách dosáhne předem stanovené prahové hodnoty, systém vytvoří skutečnou práci rychleji použitím paralelního, asynchronního zpracování.</span><span class="sxs-lookup"><span data-stu-id="37b7b-106">If the number of wave load lines reaches a predetermined threshold, the system will create actual work more quickly by applying parallel, asynchronous processing.</span></span>

## <a name="enable-the-schedule-work-creation-feature"></a><span data-ttu-id="37b7b-107">Povolení funkce Naplánovat vytvoření práce</span><span class="sxs-lookup"><span data-stu-id="37b7b-107">Enable the Schedule work creation feature</span></span>

### <a name="enable-the-feature-in-feature-management"></a><span data-ttu-id="37b7b-108">Povolení funkce ve správě funkcí</span><span class="sxs-lookup"><span data-stu-id="37b7b-108">Enable the feature in feature management</span></span>

<span data-ttu-id="37b7b-109">Než můžete použít funkci *Naplánovat vytvoření práce*, musíte ji v systému zapnout.</span><span class="sxs-lookup"><span data-stu-id="37b7b-109">Before you can use the *Schedule work creation* feature, it must be turned on in your system.</span></span> <span data-ttu-id="37b7b-110">Správci mohou pomocí pracovního prostoru [Správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji, pokud je třeba.</span><span class="sxs-lookup"><span data-stu-id="37b7b-110">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="37b7b-111">Funkce je zde uvedena následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="37b7b-111">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="37b7b-112">**Modul:** *Řízení skladu*</span><span class="sxs-lookup"><span data-stu-id="37b7b-112">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="37b7b-113">**Název funkce:** *Vytvoření plánu práce*</span><span class="sxs-lookup"><span data-stu-id="37b7b-113">**Feature name:** *Schedule work creation*</span></span>

> [!NOTE]
> <span data-ttu-id="37b7b-114">Funkce *Blokování v celé organizaci* musí být povolena, než budete moci povolit *Naplánování vytvoření práce*.</span><span class="sxs-lookup"><span data-stu-id="37b7b-114">The *Organization-wide work blocking* feature must be enabled before you can enable *Schedule work creation*.</span></span>

### <a name="manually-enable-batch-processing-of-waves"></a><span data-ttu-id="37b7b-115">Ručně povolte dávkové zpracování ve vlnách</span><span class="sxs-lookup"><span data-stu-id="37b7b-115">Manually enable batch processing of waves</span></span>

<span data-ttu-id="37b7b-116">Chcete-li využít výhod paralelní asynchronní metody k vytvoření skladové práce, musí být váš vlnový proces spuštěn dávkově.</span><span class="sxs-lookup"><span data-stu-id="37b7b-116">To take advantage of a parallel asynchronous method to create warehouse work, your wave process must be running in batch.</span></span> <span data-ttu-id="37b7b-117">Nastavení:</span><span class="sxs-lookup"><span data-stu-id="37b7b-117">To set this up:</span></span>

1. <span data-ttu-id="37b7b-118">Přejděte do nabídky  **Řízení skladu \> Nastavení \> Parametry řízení skladu**.</span><span class="sxs-lookup"><span data-stu-id="37b7b-118">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>

1. <span data-ttu-id="37b7b-119">Na kartě **Obecné** nastavte **Zpracovat vlny v dávce** na *ano*.</span><span class="sxs-lookup"><span data-stu-id="37b7b-119">On the **General** tab, set **Process waves in batch** to *Yes*.</span></span> <span data-ttu-id="37b7b-120">Volitelně můžete také vybrat vyhrazenou **skupinu dávek pro zpracování ve vlnách**, abyste zabránili tomu, aby vaše dávkové zpracování fronty běželo souběžně s jinými procesy.</span><span class="sxs-lookup"><span data-stu-id="37b7b-120">Optionally, you can also select a dedicated **Wave processing batch group** to prevent your batch queue processing from running at the same time as other processes.</span></span>

1. <span data-ttu-id="37b7b-121">Nastavte **Doba čekání na zámek (ms)**, což platí, když systém zpracovává několik vln současně.</span><span class="sxs-lookup"><span data-stu-id="37b7b-121">Set the **Wait for lock (ms) time**, which applies when the system is processing several waves at the same time.</span></span> <span data-ttu-id="37b7b-122">U většiny větších procesů mávání doporučujeme hodnotu *60000*.</span><span class="sxs-lookup"><span data-stu-id="37b7b-122">For most larger waving processes, we recommend a value of *60000*.</span></span>

### <a name="manually-enable-the-new-wave-step-method-for-existing-wave-templates"></a><span data-ttu-id="37b7b-123">Ručně povolte novou metodu kroku vlny pro existující šablony vln</span><span class="sxs-lookup"><span data-stu-id="37b7b-123">Manually enable the new wave step method for existing wave templates</span></span>

<span data-ttu-id="37b7b-124">Začněte tím, že vytvoříte novou metodu kroku vlny a povolíte ji pro paralelní asynchronní zpracování úloh.</span><span class="sxs-lookup"><span data-stu-id="37b7b-124">Start by creating the new wave step method and enabling it for parallel asynchronous task processing.</span></span>

1. <span data-ttu-id="37b7b-125">Přejděte na  **Řízení skladu \> Nastavení \> Vlny \> Metody zpracování ve vlnách**.</span><span class="sxs-lookup"><span data-stu-id="37b7b-125">Go to **Warehouse management \> Setup \> Waves \> Wave process methods**.</span></span>

1. <span data-ttu-id="37b7b-126">Vyberte  **Znovu generovat metodu** a všimněte si, že krok *WHSScheduleWorkCreationWaveStepMethod* byl přidán do seznamu metod zpracování ve vlnách, které můžete použít ve svých šablonách přepravních vln.</span><span class="sxs-lookup"><span data-stu-id="37b7b-126">Select  **Regenerate method** and note that *WHSScheduleWorkCreationWaveStepMethod* has been added to the list of wave process methods you can use in your shipping wave templates.</span></span>

1. <span data-ttu-id="37b7b-127">Vyberte záznam pomocí **názvu metody** *WHSScheduleWorkCreationWaveStepMethod* a vyberte **Konfigurace úlohy**.</span><span class="sxs-lookup"><span data-stu-id="37b7b-127">Select the record with the **Method name** *WHSScheduleWorkCreationWaveStepMethod* and select **Task configuration**.</span></span>

1. <span data-ttu-id="37b7b-128">Pokud chcete do mřížky přidat nový řádek, vyberte **Nový** v podokně úloh a použijte následující nastavení:</span><span class="sxs-lookup"><span data-stu-id="37b7b-128">To add a new row to the grid, select **New** on the Action Pane and use the following settings:</span></span>

    - <span data-ttu-id="37b7b-129">**Sklad** - Vyberte sklad, který budete používat k naplánování zpracování práce plánu.</span><span class="sxs-lookup"><span data-stu-id="37b7b-129">**Warehouse** - Select the warehouse you will use to schedule work creation processing.</span></span>

    - <span data-ttu-id="37b7b-130">**Maximální počet dávkových úloh** - Určete maximální počet dávkových úloh.</span><span class="sxs-lookup"><span data-stu-id="37b7b-130">**Maximum number of batch tasks** - Specify a maximum number of batch tasks.</span></span> <span data-ttu-id="37b7b-131">Ve většině případů by tato hodnota měla být v rozsahu od 8 do 16, doporučujeme vám však experimentovat s optimálním nastavením na základě vašich scénářů.</span><span class="sxs-lookup"><span data-stu-id="37b7b-131">In most cases, this value should be in the range from 8-16, however we recommend that you experiment with the optimal setting based on your scenarios.</span></span>

    - <span data-ttu-id="37b7b-132">**Skupina dávek pro zpracování ve vlnách** - Vyberte vyhrazenou skupinu dávek pro zpracování ve vlnách pro optimalizaci zpracování dávkové fronty.</span><span class="sxs-lookup"><span data-stu-id="37b7b-132">**Wave processing batch group** - Select a dedicated wave processing batch group to optimize your batch queue processing.</span></span>

<span data-ttu-id="37b7b-133">Nyní jste připraveni aktualizovat stávající šablonu vln (nebo vytvořit novou), abyste mohli použít metodu zpracování ve vlnách *Naplánovat vytvoření práce*.</span><span class="sxs-lookup"><span data-stu-id="37b7b-133">Now you are ready to update an existing wave template (or create a new one) to use the *Schedule work creation* wave processing method.</span></span>

1. <span data-ttu-id="37b7b-134">Přejděte na  **Řízení skladu \> Nastavení \> Vlny \> Šablony vlny**.</span><span class="sxs-lookup"><span data-stu-id="37b7b-134">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>

1. <span data-ttu-id="37b7b-135">V podokně úlohy vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="37b7b-135">Select **Edit** on the Action Pane.</span></span>

1. <span data-ttu-id="37b7b-136">V podokně seznamu vyberte šablonu vln, kterou chcete aktualizovat (pokud testujete pomocí ukázkových dat, můžete použít *Výchozí nastavení 24*).</span><span class="sxs-lookup"><span data-stu-id="37b7b-136">In the list pane, select the wave template you would like to update (if you are testing using demo data, then you could use *24 Shipping default*).</span></span>

1. <span data-ttu-id="37b7b-137">Rozbalte kartu s náhledem **Metody** a vyberte řádek s mřížkou **Název** *naplánovat vytvoření práce* v mřížce **Zbývající metody**.</span><span class="sxs-lookup"><span data-stu-id="37b7b-137">Expand the **Methods** FastTab and select the row with the **Name** *Schedule work creation* in the **Remaining methods** grid.</span></span>

1. <span data-ttu-id="37b7b-138">Vyberte šipku směřující ke sloupci **Vybrané metody** pro přesun vybraného řádku do tohoto sloupce.</span><span class="sxs-lookup"><span data-stu-id="37b7b-138">Select the arrow pointing to the **Selected methods** column to move the selected row to that column.</span></span> <span data-ttu-id="37b7b-139">(Můžete mít pouze jednu vybranou metodu v jednom okamžiku, která používá *WHSScheduleWorkCreationWaveStepMethod* nebo *createWork*, takže existující řádek s **názvem metody** *createWork* se automaticky přesune do mřížky **Zbývající metody**.)</span><span class="sxs-lookup"><span data-stu-id="37b7b-139">(You can only have one selected method at a time that uses either *WHSScheduleWorkCreationWaveStepMethod* or *createWork*, so the existing row with **Method name** *createWork* is automatically moved to the **Remaining methods** grid.)</span></span>

## <a name="set-wave-task-processing-threshold-data"></a><span data-ttu-id="37b7b-140">Nastavení prahových dat zpracování vlnové úlohy</span><span class="sxs-lookup"><span data-stu-id="37b7b-140">Set wave task processing threshold data</span></span>

<span data-ttu-id="37b7b-141">Systém vytvoří výchozí prahová data zpracování vlnových úloh při prvním spuštění vlnového procesu pomocí jakéhokoli zpracování založeného na úlohách.</span><span class="sxs-lookup"><span data-stu-id="37b7b-141">The system will create default wave task processing threshold data the first time a wave process runs using any task-based processing.</span></span> <span data-ttu-id="37b7b-142">Data se používají k řízení, kdy zpracování ve vlnách bude probíhat asynchronně a bude založeno na úkolech, což mu umožní paralelně zpracovávat a vytvářet práci.</span><span class="sxs-lookup"><span data-stu-id="37b7b-142">The data is used to control when wave processing will run asynchronously and be task-based, which enables it to process and create work in parallel.</span></span>

<span data-ttu-id="37b7b-143">Výchozí data budou zpočátku používat prahovou hodnotu 15 pro minimální počet řádků zatížení (MINIMUMWAVELOADLINES).</span><span class="sxs-lookup"><span data-stu-id="37b7b-143">The default data will initially use a threshold value of 15 for the minimum number of load lines (MINIMUMWAVELOADLINES).</span></span> <span data-ttu-id="37b7b-144">To znamená, že když systém zpracovává vlnu s více než 15 řádky zatížení, použije asynchronní zpracování úloh.</span><span class="sxs-lookup"><span data-stu-id="37b7b-144">This means that when the system processes a wave with more than 15 loads lines, it will use asynchronous task processing.</span></span> <span data-ttu-id="37b7b-145">Tyto údaje můžete ručně vložit / aktualizovat v tabulce **WHSWaveTaskProcessingThresholdParameters** ve vašem zkušebním prostředí, ale pokud toto nastavení potřebujete změnit v provozním prostředí, musíte zažádat o aktualizaci podporu Microsoftu.</span><span class="sxs-lookup"><span data-stu-id="37b7b-145">You can manually insert/update this data in the **WHSWaveTaskProcessingThresholdParameters** table in your test environments, but if you need to change this setting in a production environment, you must contact Microsoft Support to request the update.</span></span>

## <a name="work-with-the-feature"></a><span data-ttu-id="37b7b-146">Práce s funkcí</span><span class="sxs-lookup"><span data-stu-id="37b7b-146">Work with the feature</span></span>

<span data-ttu-id="37b7b-147">Když je povolena funkce *Naplánovat vytvoření práce*, zpracování ve vlnách vytvoří plánovanou práci, která bude nakonec použita v novém procesu vytváření práce.</span><span class="sxs-lookup"><span data-stu-id="37b7b-147">When the *Schedule work creation* functionality is enabled, wave processing will create planned work, which will eventually be used by the new work creation process.</span></span> <span data-ttu-id="37b7b-148">Během vytváření práce bude práce blokována pomocí funkce *Blokování práce v celé organizaci*.</span><span class="sxs-lookup"><span data-stu-id="37b7b-148">During work creation, the work will be blocked using the *Organization-wide work blocking* feature.</span></span>

<span data-ttu-id="37b7b-149">Následující vývojový diagram ukazuje, jak se během zpracování ve vlnách vytváří plánovaná práce.</span><span class="sxs-lookup"><span data-stu-id="37b7b-149">The following flowchart shows how planned work is created during wave processing.</span></span>

![Naplánovat vytvoření práce](media/schedule-work-creation-process.png)

### <a name="planned-work"></a><span data-ttu-id="37b7b-151">Plánovaná práce</span><span class="sxs-lookup"><span data-stu-id="37b7b-151">Planned work</span></span>

<span data-ttu-id="37b7b-152">Stránka **Podrobnosti o plánované práci** (**Řízení skladu \> Práce \> Podrobnosti plánované práce**) zobrazuje informace o plánované práci, která je původně vytvořena během zpracování ve vlnách.</span><span class="sxs-lookup"><span data-stu-id="37b7b-152">The **Planned work details** page (**Warehouse management \> Work \> Planned work details**) shows information about the planned work, which is initially created during wave processing.</span></span> <span data-ttu-id="37b7b-153">K dispozici jsou následující hodnoty **stavu procesu**:</span><span class="sxs-lookup"><span data-stu-id="37b7b-153">The following **Process status** values are available:</span></span>

- <span data-ttu-id="37b7b-154">**Ve frontě** - Plánovaná práce čeká na použití k vytvoření práce.</span><span class="sxs-lookup"><span data-stu-id="37b7b-154">**Queued** - The planned work is waiting to be used to create work.</span></span>
- <span data-ttu-id="37b7b-155">**Dokončeno** - Plánovaná práce byla použita k vytvoření práce.</span><span class="sxs-lookup"><span data-stu-id="37b7b-155">**Completed** - The planned work has been used to create work.</span></span>
- <span data-ttu-id="37b7b-156">**Selhání** - Zpracování ve vlnách selhalo.</span><span class="sxs-lookup"><span data-stu-id="37b7b-156">**Failed** – The wave processing has failed.</span></span> <span data-ttu-id="37b7b-157">Všimněte si, že plánovaná práce může být ve stavu **Selhání** s nebo bez související skutečné práce.</span><span class="sxs-lookup"><span data-stu-id="37b7b-157">Note that the planned work can be in a **Failed** state with or without related actual work.</span></span> <span data-ttu-id="37b7b-158">Když selže proces vytváření skutečné práce, zůstane skutečná práce ve stavu *Zrušeno*.</span><span class="sxs-lookup"><span data-stu-id="37b7b-158">When the actual work creation process fails, the actual work remains in status *Cancelled*.</span></span>

### <a name="batch-job-for-the-work-creation-process"></a><span data-ttu-id="37b7b-159">Dávková úloha pro proces vytváření práce</span><span class="sxs-lookup"><span data-stu-id="37b7b-159">Batch job for the work creation process</span></span>

<span data-ttu-id="37b7b-160">Chcete-li zobrazit dávkové úlohy pro zpracování ve vlnách, vyberte **Dávkové úlohy** v podokně akcí na straně **Všechny vlny**.</span><span class="sxs-lookup"><span data-stu-id="37b7b-160">To view the batch jobs for processing waves, select **Batch jobs** on the Action Pane on the **All waves** page.</span></span>

<span data-ttu-id="37b7b-161">Odtud můžete zobrazit všechny podrobnosti dávkové úlohy pro každé ID dávkové úlohy.</span><span class="sxs-lookup"><span data-stu-id="37b7b-161">From here, you can view all the batch task details for each of the batch job IDs.</span></span>
