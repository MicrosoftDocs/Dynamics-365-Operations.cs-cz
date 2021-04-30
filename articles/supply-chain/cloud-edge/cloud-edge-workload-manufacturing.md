---
title: Pracovní zátěže spuštění výroby pro cloudové a hraniční jednotky škálování
description: Toto téma popisuje, jak pracovní zátěže spuštění výroby fungují s cloudovými a hraničními jednotkami škálování.
author: cabeln
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: cabeln
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: a6d6979093c67d2d89b88678712f4c0205c63194
ms.sourcegitcommit: 639175a39da38edd13e21eeb5a1a5ca62fa44d99
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/15/2021
ms.locfileid: "5899088"
---
# <a name="manufacturing-execution-workloads-for-cloud-and-edge-scale-units"></a><span data-ttu-id="b3c9f-103">Pracovní zátěž spouštění výroby pro jednotky škálování cloudu a hraniční sítě</span><span class="sxs-lookup"><span data-stu-id="b3c9f-103">Manufacturing execution workloads for cloud and edge scale units</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> <span data-ttu-id="b3c9f-104">Úloha provádění výroby je v tomto okamžiku k dispozici v preview.</span><span class="sxs-lookup"><span data-stu-id="b3c9f-104">The manufacturing execution workload is available in preview at this point in time.</span></span>
> <span data-ttu-id="b3c9f-105">Některé obchodní funkce nejsou ve veřejném náhledu plně podporovány, když se používají jednotky škálování pracovní zátěže.</span><span class="sxs-lookup"><span data-stu-id="b3c9f-105">Some business functionality isn't fully supported in the public preview when workload scale units are used.</span></span>

<span data-ttu-id="b3c9f-106">Při provádění výroby poskytují jednotky škálování následující funkce:</span><span class="sxs-lookup"><span data-stu-id="b3c9f-106">In manufacturing execution, scale units deliver the following capabilities:</span></span>

- <span data-ttu-id="b3c9f-107">Obsluha strojů a vedoucí výroby mají přístup k operačnímu výrobnímu plánu.</span><span class="sxs-lookup"><span data-stu-id="b3c9f-107">Machine operators and shop floor supervisors can access the operational production plan.</span></span>
- <span data-ttu-id="b3c9f-108">Operátoři strojů mohou udržovat aktuální plán spuštěním samostatných a procesních výrobních úloh.</span><span class="sxs-lookup"><span data-stu-id="b3c9f-108">Machine operators can keep the plan up to date by running discrete and process manufacturing jobs.</span></span>
- <span data-ttu-id="b3c9f-109">Vedoucí dílny může upravit operační plán.</span><span class="sxs-lookup"><span data-stu-id="b3c9f-109">The shop floor supervisor can adjust the operational plan.</span></span>
- <span data-ttu-id="b3c9f-110">Pracovníci mají přístup k času a docházce pro označení příchodu a odchodu v hraničním pásmu, aby zajistili správný výpočet platu pracovníka.</span><span class="sxs-lookup"><span data-stu-id="b3c9f-110">Workers can access time and attendance for clock-in and clock-out on the edge, to ensure correct worker pay calculation.</span></span>

<span data-ttu-id="b3c9f-111">Toto téma popisuje, jak pracovní zátěže spuštění výroby fungují s cloudovými a hraničními jednotkami škálování.</span><span class="sxs-lookup"><span data-stu-id="b3c9f-111">This topic describes how manufacturing execution workloads work with cloud and edge scale units.</span></span>

## <a name="the-manufacturing-lifecycle"></a><span data-ttu-id="b3c9f-112">Životní cyklus výroby</span><span class="sxs-lookup"><span data-stu-id="b3c9f-112">The manufacturing lifecycle</span></span>

<span data-ttu-id="b3c9f-113">Jak ukazuje následující obrázek, životní cyklus výroby je rozdělen do tří fází: *Plánování*, *Provedení* a *Dokončení*.</span><span class="sxs-lookup"><span data-stu-id="b3c9f-113">As the following illustration shows, the manufacturing lifecycle is divided into three phases: *Plan*, *Execute*, and *Finalize*.</span></span>

<span data-ttu-id="b3c9f-114">[![Fáze provedení výroby při použití jediného prostředí](media/mes-phases.png "Fáze provedení výroby při použití jediného prostředí")](media/mes-phases-large.png)</span><span class="sxs-lookup"><span data-stu-id="b3c9f-114">[![Manufacturing execution phases when a single environment is used](media/mes-phases.png "Manufacturing execution phases when a single environment is used")](media/mes-phases-large.png)</span></span>

<span data-ttu-id="b3c9f-115">Fáze _Plánování_ zahrnuje definici produktu, plánování, vytváření a plánování objednávek a vydání.</span><span class="sxs-lookup"><span data-stu-id="b3c9f-115">The _Plan_ phase includes product definition, planning, order creation and scheduling, and release.</span></span> <span data-ttu-id="b3c9f-116">Krok uvolnění označuje přechod z fáze _Plánování_ do fáze _Provedení_.</span><span class="sxs-lookup"><span data-stu-id="b3c9f-116">The release step indicates the transition from the _Plan_ phase to the _Execute_ phase.</span></span> <span data-ttu-id="b3c9f-117">Po uvolnění výrobní zakázky budou úlohy výrobní zakázky viditelné na produkční ploše a připraveny k provedení.</span><span class="sxs-lookup"><span data-stu-id="b3c9f-117">When a production order is released, the production order jobs will be visible on the production floor and ready for execution.</span></span>

<span data-ttu-id="b3c9f-118">Když je úloha produkce označena jako dokončená, přesune se z fáze _Provedení_ do fáze _Dokončení_.</span><span class="sxs-lookup"><span data-stu-id="b3c9f-118">When a production job is marked as completed, it moves from the _Execute_ phase to the _Finalize_ phase.</span></span> <span data-ttu-id="b3c9f-119">Ve fázi _Dokončení_ projdou registrace z fáze *Provedení* schvalovacím pracovním procesem, kde jsou vypočítány, schváleny a přeneseny.</span><span class="sxs-lookup"><span data-stu-id="b3c9f-119">In the _Finalize_ phase, the registrations from the *Execute* phase go through an approval workflow, where they are calculated, approved, and transferred.</span></span> <span data-ttu-id="b3c9f-120">V tomto okamžiku je výrobní zakázka dokončena.</span><span class="sxs-lookup"><span data-stu-id="b3c9f-120">At that point, the production order is completed.</span></span> <span data-ttu-id="b3c9f-121">Tím je generován základ pro plat pracovníka.</span><span class="sxs-lookup"><span data-stu-id="b3c9f-121">Therefore, the basis for the workers' pay is generated.</span></span>

## <a name="splitting-the-execute-phase-into-a-separate-workload"></a><span data-ttu-id="b3c9f-122">Rozdělení fáze Provedení na samostatnou úlohu</span><span class="sxs-lookup"><span data-stu-id="b3c9f-122">Splitting the Execute phase into a separate workload</span></span>

<span data-ttu-id="b3c9f-123">Jak ukazuje následující obrázek, při použití jednotek měřítka je fáze _Provedení_ rozdělena jako samostatná úloha.</span><span class="sxs-lookup"><span data-stu-id="b3c9f-123">As the following illustration shows, when scale units are used, the _Execute_ phase is split out as a separate workload.</span></span>

<span data-ttu-id="b3c9f-124">[![Fáze provedení výroby při použití jednotek škálování](media/mes-phases-workloads.png "Fáze provedení výroby při použití jednotek škálování")](media/mes-phases-workloads-large.png)</span><span class="sxs-lookup"><span data-stu-id="b3c9f-124">[![Manufacturing execution phases when scale units are used](media/mes-phases-workloads.png "Manufacturing execution phases when scale units are used")](media/mes-phases-workloads-large.png)</span></span>

<span data-ttu-id="b3c9f-125">Model nyní přechází z instalace s jednou instancí na model, který je založen na jednotkách centra a škálování.</span><span class="sxs-lookup"><span data-stu-id="b3c9f-125">The model now goes from a single-instance installation to a model that is based on the hub and scale units.</span></span> <span data-ttu-id="b3c9f-126">Fáze _Plánování_ a _Dokončení_ běží jako operace back-office v centru a pracovní zátěž provedení výroby probíhá na jednotkách škálování.</span><span class="sxs-lookup"><span data-stu-id="b3c9f-126">The _Plan_ and _Finalize_ phases run as back-office operations on the hub, and the manufacturing execution workload runs on the scale units.</span></span> <span data-ttu-id="b3c9f-127">Data se přenášejí asynchronně mezi centrem a jednotkami měřítka.</span><span class="sxs-lookup"><span data-stu-id="b3c9f-127">Data is transferred asynchronously between the hub and scale units.</span></span>

<span data-ttu-id="b3c9f-128">Když je v centru uvolněna výrobní zakázka, všechna data potřebná ke zpracování produkčních úloh se přenesou do jednotky škálování.</span><span class="sxs-lookup"><span data-stu-id="b3c9f-128">When a production order is released on the hub, all data that is required to process production jobs is transferred to the scale unit.</span></span> <span data-ttu-id="b3c9f-129">Tato data zahrnují výrobní zakázky, výrobní trasy, kusovníky a produkty.</span><span class="sxs-lookup"><span data-stu-id="b3c9f-129">This data includes production orders, production routes, bills of materials, and products.</span></span> <span data-ttu-id="b3c9f-130">Data, která nesouvisí s výrobní zakázkou (například nepřímé aktivity, kódy nepřítomnosti a parametry výroby), se také přenesou z centra do jednotky škálování.</span><span class="sxs-lookup"><span data-stu-id="b3c9f-130">Data that isn't related to a production order (such as indirect activities, absence codes, and production parameters) is also transferred from the hub to the scale unit.</span></span> <span data-ttu-id="b3c9f-131">Data, která pocházejí z centra a která se přenášejí do jednotky škálování, lze zpravidla vytvářet nebo aktualizovat pouze v centru.</span><span class="sxs-lookup"><span data-stu-id="b3c9f-131">As a rule, data that originates from the hub and that is transferred to the scale unit can be created or updated only on the hub.</span></span> <span data-ttu-id="b3c9f-132">Například na stupnici nelze vytvořit nový kód absence nebo nepřímou aktivitu&mdash;lze je použít pouze pro registraci.</span><span class="sxs-lookup"><span data-stu-id="b3c9f-132">For example, a new absence code or indirect activity can't be created on the scale unit&mdash;they can be used only for registration.</span></span> <span data-ttu-id="b3c9f-133">Registrace provedené na jednotce škálování během provádění se poté přenesou do centra, kde se zpracovávají schválení času a docházky, inventář a finanční aktualizace.</span><span class="sxs-lookup"><span data-stu-id="b3c9f-133">The registrations that are made on the scale unit during execution are then transferred to the hub, where time and attendance approval, inventory, and financial updates are processed.</span></span>

## <a name="manufacturing-execution-tasks-that-can-be-run-on-workloads"></a><span data-ttu-id="b3c9f-134">Výroba prováděcích úloh, které lze spouštět na úlohách</span><span class="sxs-lookup"><span data-stu-id="b3c9f-134">Manufacturing execution tasks that can be run on workloads</span></span>

<span data-ttu-id="b3c9f-135">Následující úlohy provádění výroby lze aktuálně spouštět na úlohách, když se používají jednotky škálování:</span><span class="sxs-lookup"><span data-stu-id="b3c9f-135">The following manufacturing execution tasks can currently be run on workloads when scale units are used:</span></span>

- <span data-ttu-id="b3c9f-136">Píchnutí příchodu, přihlášení, odpíchnutí příchodu a nepřítomnost</span><span class="sxs-lookup"><span data-stu-id="b3c9f-136">Clock-in, log-in, clock-out, and absence</span></span>
- <span data-ttu-id="b3c9f-137">Zahájit práci</span><span class="sxs-lookup"><span data-stu-id="b3c9f-137">Start job</span></span>
- <span data-ttu-id="b3c9f-138">Seskupení úloh</span><span class="sxs-lookup"><span data-stu-id="b3c9f-138">Bundle jobs</span></span>
- <span data-ttu-id="b3c9f-139">Průběh sestavy</span><span class="sxs-lookup"><span data-stu-id="b3c9f-139">Report progress</span></span>
- <span data-ttu-id="b3c9f-140">Vykázat odpad</span><span class="sxs-lookup"><span data-stu-id="b3c9f-140">Report scrap</span></span>
- <span data-ttu-id="b3c9f-141">Nepřímá aktivita</span><span class="sxs-lookup"><span data-stu-id="b3c9f-141">Indirect activity</span></span>
- <span data-ttu-id="b3c9f-142">Přerušení</span><span class="sxs-lookup"><span data-stu-id="b3c9f-142">Break</span></span>

## <a name="working-with-manufacturing-execution-workloads-on-the-hub"></a><span data-ttu-id="b3c9f-143">Práce s výrobními úlohami spuštění v centru</span><span class="sxs-lookup"><span data-stu-id="b3c9f-143">Working with manufacturing execution workloads on the hub</span></span>

<span data-ttu-id="b3c9f-144">Obvykle se procesy, které jsou vyžadovány ke spouštění pracovních úloh spuštění výroby, spouštějí automaticky, aby se podle potřeby synchronizovalo centrum a všechny jednotky škálování.</span><span class="sxs-lookup"><span data-stu-id="b3c9f-144">Usually, the processes that are required to run manufacturing execution workloads run automatically to keep the hub and all the scale units in sync, as needed.</span></span> <span data-ttu-id="b3c9f-145">Pokud však máte potíže, můžete ručně spustit zpracování nezpracovaných registrací, které jsou přijímány z úloh, nebo zkontrolovat protokol zpracování registrace.</span><span class="sxs-lookup"><span data-stu-id="b3c9f-145">However, if you're having trouble, you can manually trigger the processing of raw registrations that are received from workloads and/or check the registration processing log.</span></span>

### <a name="manually-process-raw-registrations"></a><span data-ttu-id="b3c9f-146">Ruční zpracování nezpracovaných registrací</span><span class="sxs-lookup"><span data-stu-id="b3c9f-146">Manually process raw registrations</span></span>

<span data-ttu-id="b3c9f-147">Dávková úloha v Supply Chain Management se spouští automaticky a zpracovává všechny registrace, které byly přijaty z úloh.</span><span class="sxs-lookup"><span data-stu-id="b3c9f-147">A batch job in Supply Chain Management runs automatically to process all the registrations that have been received from the workloads.</span></span> <span data-ttu-id="b3c9f-148">Tato úloha vytvoří požadované produkční deníky a položky deníku při zpracování registrace dokončené úlohy na úloze.</span><span class="sxs-lookup"><span data-stu-id="b3c9f-148">This job creates the required production journals and logbook entries when a registration is processed for a completed job on the workload.</span></span>

<span data-ttu-id="b3c9f-149">I když se úloha obvykle spouští automaticky, můžete ji kdykoli spustit ručně po přihlášení do centra a přejít na **Kontrola výroby \> Pravidelné úkoly \> Správa zátěže backoffice \> Zpracovat nezpracované registrace**.</span><span class="sxs-lookup"><span data-stu-id="b3c9f-149">Although the job usually runs automatically, you can run it manually at any time by signing in to the hub and going to **Production control \> Periodic tasks \> Backoffice workload management \> Process raw registrations**.</span></span>

### <a name="check-the-raw-registration-processing-log"></a><span data-ttu-id="b3c9f-150">Kontrola nezpracovaného protokolu zpracování registrace</span><span class="sxs-lookup"><span data-stu-id="b3c9f-150">Check the raw registration processing log</span></span>

<span data-ttu-id="b3c9f-151">Chcete-li zkontrolovat protokol zpracování registrace, přihlaste se do centra a přejděte na **Kontrola výroby \> Pravidelné úkoly \> Správa zátěže backoffice \> Nezpracovaný protokol zpracování registrace**.</span><span class="sxs-lookup"><span data-stu-id="b3c9f-151">To review the registration processing log, sign in to the hub, and go to **Production control \> Periodic tasks \> Backoffice workload management \> Raw registration processing log**.</span></span> <span data-ttu-id="b3c9f-152">Stránka **Protokol zpracování nezpracované registrace** zobrazuje seznam zpracovaných nezpracovaných registrací a stav každé registrace.</span><span class="sxs-lookup"><span data-stu-id="b3c9f-152">The **Raw registration processing log** page shows a list of processed raw registrations and the status of each registration.</span></span>

<span data-ttu-id="b3c9f-153">![Kontrola stránky protokolu nezpracované registrace](media/mes-processing-log.png "Kontrola stránky protokolu nezpracované registrace")</span><span class="sxs-lookup"><span data-stu-id="b3c9f-153">![Raw registration processing log page](media/mes-processing-log.png "Raw registration processing log page")</span></span>

<span data-ttu-id="b3c9f-154">Na jakékoli registraci v seznamu můžete pracovat tak, že ji vyberete a poté vyberete jedno z následujících tlačítek v podokně akcí:</span><span class="sxs-lookup"><span data-stu-id="b3c9f-154">You can work on any registration in the list by selecting it and then selecting one of the following buttons on the Action Pane:</span></span>

- <span data-ttu-id="b3c9f-155">**Proces** - Ruční zpracování vybrané registrace.</span><span class="sxs-lookup"><span data-stu-id="b3c9f-155">**Process** – Manually process the selected registration.</span></span> <span data-ttu-id="b3c9f-156">Tato akce může být užitečná, pokud úloha _Zpracovat nezpracované registrace_ neproběhla nebo selhala.</span><span class="sxs-lookup"><span data-stu-id="b3c9f-156">This action can be useful if the _Process raw registrations_ job hasn't run, or if it failed.</span></span>
- <span data-ttu-id="b3c9f-157">**Zrušit** - Zruší vybranou registraci.</span><span class="sxs-lookup"><span data-stu-id="b3c9f-157">**Cancel** – Cancel the selected registration.</span></span>

## <a name="working-with-manufacturing-execution-workloads-on-a-scale-unit"></a><span data-ttu-id="b3c9f-158">Práce s výrobními úlohami spuštění na jednotce škálování</span><span class="sxs-lookup"><span data-stu-id="b3c9f-158">Working with manufacturing execution workloads on a scale unit</span></span>

<span data-ttu-id="b3c9f-159">Obvykle se procesy, které jsou vyžadovány ke spouštění pracovních úloh spuštění výroby, spouštějí automaticky, aby se podle potřeby synchronizovalo centrum a všechny jednotky škálování.</span><span class="sxs-lookup"><span data-stu-id="b3c9f-159">Usually, the processes that are required to run manufacturing execution workloads run automatically to keep the hub and all the scale units in sync, as needed.</span></span> <span data-ttu-id="b3c9f-160">Pokud však máte potíže, můžete zkontrolovat historii objednávek, které byly zpracovány v jednotce škálování, nebo ručně spustit úlohu _Výrobní centrum procesoru zpráv jednotky škálování_.</span><span class="sxs-lookup"><span data-stu-id="b3c9f-160">However, if you're having trouble, you can check the history of orders that have been processed on a scale unit or manually run the _Manufacturing hub to scale unit message processor_ job.</span></span>

### <a name="view-the-history-of-manufacturing-jobs-that-have-been-processed-on-a-scale-unit"></a><span data-ttu-id="b3c9f-161">Zobrazte historii výrobních úloh, které byly zpracovány na jednotce škálování</span><span class="sxs-lookup"><span data-stu-id="b3c9f-161">View the history of manufacturing jobs that have been processed on a scale unit</span></span>

<span data-ttu-id="b3c9f-162">Chcete-li zkontrolovat historii výrobních úloh, které byly zpracovány na jednotce škálování, přihlaste se do stroje jednotky škálování a přejděte na **Kontrola výroby \> Pravidelné úkoly \> Správa úloh backoffice \> Historie zpracování výrobních úloh**.</span><span class="sxs-lookup"><span data-stu-id="b3c9f-162">To review the history of manufacturing jobs that have been processed on a scale unit, sign in to the scale unit machine, and go to **Production control \> Periodic tasks \> Backoffice workload management \> Manufacturing jobs processing history**.</span></span> <span data-ttu-id="b3c9f-163">Stránka **Historie zpracování výrobních úloh** zobrazuje historii zpracování výrobních zakázek na jednotce škálování.</span><span class="sxs-lookup"><span data-stu-id="b3c9f-163">The **Manufacturing jobs processing history** page shows the processing history of the production orders on the scale unit.</span></span> <span data-ttu-id="b3c9f-164">Na každé výrobní zakázce v seznamu můžete pracovat tak, že ji vyberete a poté vyberete jedno z následujících tlačítek v podokně akcí:</span><span class="sxs-lookup"><span data-stu-id="b3c9f-164">You can work on any production order in the list by selecting it and then selecting one of the following buttons on the Action Pane:</span></span>

- <span data-ttu-id="b3c9f-165">**Proces** - Ruční zpracování vybrané výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="b3c9f-165">**Process** – Manually process the selected production order.</span></span>
- <span data-ttu-id="b3c9f-166">**Zrušit** - Zrušte vybranou výrobní zakázku.</span><span class="sxs-lookup"><span data-stu-id="b3c9f-166">**Cancel** – Cancel the selected production order.</span></span>

### <a name="manufacturing-hub-to-scale-unit-message-processor-job"></a><span data-ttu-id="b3c9f-167">Výrobní centrum pro úlohu procesoru zprávy jednotky škálování</span><span class="sxs-lookup"><span data-stu-id="b3c9f-167">Manufacturing hub to scale unit message processor job</span></span>

<span data-ttu-id="b3c9f-168">Úloha _Výrobní centrum pro procesor zpráv jednotky škálování_ zpracovává data z centra do jednotky škálování.</span><span class="sxs-lookup"><span data-stu-id="b3c9f-168">The _Manufacturing hub to scale unit message processor_ job processes data from the hub to the scale unit.</span></span> <span data-ttu-id="b3c9f-169">Tato úloha se automaticky spustí, když je nasazena úloha provedení.</span><span class="sxs-lookup"><span data-stu-id="b3c9f-169">This job is automatically started when the manufacturing execution workload is deployed.</span></span> <span data-ttu-id="b3c9f-170">Můžete jej však kdykoli spustit ručně tak, že přejdete na **Kontrola výroby \> Pravidelné úkoly \> Správa úlohy backoffice \> Výrobní centrum pro škálování procesorů zpráv jednotky**.</span><span class="sxs-lookup"><span data-stu-id="b3c9f-170">However, you can run it manually at any time by going to **Production control \> Periodic tasks \> Backoffice workload management \> Manufacturing hub to scale unit message processor**.</span></span>

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
