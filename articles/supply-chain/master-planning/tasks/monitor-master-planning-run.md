---
title: Sledování běhu hlavního plánování
description: Toto téma vysvětluje, jak může plánovač provozu sledovat, zda probíhá hlavní spuštění plánování.
author: josaw1
manager: tfehr
ms.date: 11/04/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 045b82af6f65b22e1c683f8de47a6df282711e6a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423589"
---
# <a name="monitor-a-master-planning-run"></a><span data-ttu-id="694b3-103">Sledování běhu hlavního plánování</span><span class="sxs-lookup"><span data-stu-id="694b3-103">Monitor a master planning run</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="use-a-gantt-chart-to-visualize-master-planning-progress"></a><span data-ttu-id="694b3-104">Použít Ganttův diagram ke znázornění průběhu hlavního plánování</span><span class="sxs-lookup"><span data-stu-id="694b3-104">Use a Gantt chart to visualize master planning progress</span></span>

<span data-ttu-id="694b3-105">Na stránce **Zobrazit průběh hlavního plánování** můžete zobrazit podrobné informace o historickém běhu hlavního plánování jako Ganttův diagram.</span><span class="sxs-lookup"><span data-stu-id="694b3-105">From the **View master planning progress** page, you can view details of historical master planning runs as a Gantt chart.</span></span> <span data-ttu-id="694b3-106">Tato funkce vám může pomoci pochopit čas strávený v různých fázích hlavního plánování.</span><span class="sxs-lookup"><span data-stu-id="694b3-106">This functionality can help you understand the time that is spent on the various phases of master planning.</span></span> <span data-ttu-id="694b3-107">Pro aktuální aktivní úlohu plánování lze pomocí stránky **Zobrazit průběh hlavního plánování** sledovat průběh a zobrazit odhadovanou zbývající dobu.</span><span class="sxs-lookup"><span data-stu-id="694b3-107">For a current active planning job, the **View master planning progress** page can be used to track progress and view the estimated remaining time.</span></span>

### <a name="turn-on-and-use-the-master-plan-progress-visualization-feature"></a><span data-ttu-id="694b3-108">Zapnout a použít funkci vizualizace průběhu hlavního plánu</span><span class="sxs-lookup"><span data-stu-id="694b3-108">Turn on and use the Master plan progress visualization feature</span></span>

<span data-ttu-id="694b3-109">Pokud chcete tuto funkci používat, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="694b3-109">To use this functionality, follow these steps.</span></span>

1. <span data-ttu-id="694b3-110">V pracovním prostoru **Správa funkcí** na kartě **Nová** vyberte v seznamu **Vizualizace pokroku optimalizace plánování**.</span><span class="sxs-lookup"><span data-stu-id="694b3-110">In the **Feature management** workspace, on the **New** tab, select **Master planning progress visualization** in the list.</span></span> <span data-ttu-id="694b3-111">Pokud se tato funkce nezobrazí na kartě **Nová**, podívejte se na karty **Není povoleno** a **Vše**.</span><span class="sxs-lookup"><span data-stu-id="694b3-111">If the feature doesn't appear on the **New** tab, look on the **Not enabled** and **All** tabs.</span></span>
1. <span data-ttu-id="694b3-112">Vyberte **Povolit**.</span><span class="sxs-lookup"><span data-stu-id="694b3-112">Select **Enable now**.</span></span> <span data-ttu-id="694b3-113">Můžete také vybrat možnost **Plán** a vybrat čas, kdy má být funkce zapnuta.</span><span class="sxs-lookup"><span data-stu-id="694b3-113">Alternatively, select **Schedule**, and then select the time when you want the feature to be turned on.</span></span>

<span data-ttu-id="694b3-114">Na stránce **Zobrazit průběh hlavního plánování** lze zobrazit historické úlohy plánování i aktivní úlohy plánování.</span><span class="sxs-lookup"><span data-stu-id="694b3-114">The **View master planning progress** page can display both historical planning jobs and active planning jobs.</span></span> 

<span data-ttu-id="694b3-115">Chcete-li zobrazit historické úlohy plánování, existují dvě možnosti.</span><span class="sxs-lookup"><span data-stu-id="694b3-115">To view historical planning jobs, there are two options.</span></span> 

1. <span data-ttu-id="694b3-116">Přejděte na **Hlavní plánování \> Nastavení \> Plány \> Hlavní plány** a v podokně úloh vyberte **Historie**.</span><span class="sxs-lookup"><span data-stu-id="694b3-116">Go to **Master planning \> Setup \> Plans \> Master plans**, and then, on the Action Pane, select **History**.</span></span> <span data-ttu-id="694b3-117">Při výběru požadované úlohy vyberte možnost **Dotazy** a poté vyberte možnost **Zobrazit průběh**</span><span class="sxs-lookup"><span data-stu-id="694b3-117">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>
1. <span data-ttu-id="694b3-118">Přejděte na **Hlavní plánování \> Pracovní prostory \> Hlavní plánování** a na kartě Hlavní plánování klikněte na **Historie**.</span><span class="sxs-lookup"><span data-stu-id="694b3-118">Go to **Master planning \> Workspaces \> Master planning**, on the Master planning tile click **History**.</span></span> <span data-ttu-id="694b3-119">Při výběru požadované úlohy vyberte možnost **Dotazy** a poté vyberte možnost **Zobrazit průběh**</span><span class="sxs-lookup"><span data-stu-id="694b3-119">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>

<span data-ttu-id="694b3-120">Chcete-li zobrazit aktivní úlohy plánování, existují dvě možnosti.</span><span class="sxs-lookup"><span data-stu-id="694b3-120">To view active planning jobs, there are two options.</span></span> 
1. <span data-ttu-id="694b3-121">Přejděte na **Hlavní plánování \> Pracovní prostory \> Hlavní plánování**, v podokně úloh vyberte **Nedokončený proces plánování**.</span><span class="sxs-lookup"><span data-stu-id="694b3-121">Go to **Master planning \> Workspaces \> Master planning**, on the Action Pane, select **Unfinished planning process**.</span></span> <span data-ttu-id="694b3-122">Při výběru požadované úlohy vyberte možnost **Dotazy** a poté vyberte možnost **Zobrazit průběh**.</span><span class="sxs-lookup"><span data-stu-id="694b3-122">With the desired job selected, select **Inquiries**,  and then select **View progress**.</span></span>
1. <span data-ttu-id="694b3-123">Přejděte na **Hlavní plánování \> Pracovní prostory \> Hlavní plánování** a na kartě Hlavní plánování klikněte na **Zobrazit průběh**.</span><span class="sxs-lookup"><span data-stu-id="694b3-123">Go to **Master planning \> Workspaces \> Master planning**, on the Master planning tile click **View progress**.</span></span> <span data-ttu-id="694b3-124">Při výběru požadované úlohy vyberte možnost **Dotazy** a poté vyberte možnost **Zobrazit průběh**</span><span class="sxs-lookup"><span data-stu-id="694b3-124">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>

<span data-ttu-id="694b3-125">Všimněte si, že aktivní úlohy lze zobrazit pouze při zpracování úlohy plánování.</span><span class="sxs-lookup"><span data-stu-id="694b3-125">Note you can view active jobs only when a planning job is processing.</span></span>

### <a name="analyze-a-master-planning-job"></a><span data-ttu-id="694b3-126">Analýza úlohy hlavního plánování</span><span class="sxs-lookup"><span data-stu-id="694b3-126">Analyze a master planning job</span></span>

<span data-ttu-id="694b3-127">V Ganttově diagramu můžete rozbalit všechny následující procesy plánování a zobrazit tak další podrobnosti o době strávené tímto způsobem:</span><span class="sxs-lookup"><span data-stu-id="694b3-127">In the Gantt chart, you can expand each of the following planning processes to view additional details about the time that is spent:</span></span>

- <span data-ttu-id="694b3-128">Inicializace</span><span class="sxs-lookup"><span data-stu-id="694b3-128">Initializing</span></span>
- <span data-ttu-id="694b3-129">Odstranění a vložení dat</span><span class="sxs-lookup"><span data-stu-id="694b3-129">Deleting and inserting data</span></span>
- <span data-ttu-id="694b3-130">Plánování disponibility</span><span class="sxs-lookup"><span data-stu-id="694b3-130">Coverage planning</span></span>
- <span data-ttu-id="694b3-131">Zpoždění</span><span class="sxs-lookup"><span data-stu-id="694b3-131">Delays</span></span>
- <span data-ttu-id="694b3-132">Zprávy akce</span><span class="sxs-lookup"><span data-stu-id="694b3-132">Action messages</span></span>
- <span data-ttu-id="694b3-133">Vyrovnání záloh</span><span class="sxs-lookup"><span data-stu-id="694b3-133">Finalization</span></span>
- <span data-ttu-id="694b3-134">Automatické potvrzování</span><span class="sxs-lookup"><span data-stu-id="694b3-134">Auto-firming</span></span>

<span data-ttu-id="694b3-135">Ganttův diagram je užitečný nástroj, pokud chcete zobrazit dopad zpráv s akcemi.</span><span class="sxs-lookup"><span data-stu-id="694b3-135">The Gantt chart is a useful tool if you want to view the impact of using action messages.</span></span>

#### <a name="navigation-in-the-gantt-chart"></a><span data-ttu-id="694b3-136">Navigace v Ganttově diagramu</span><span class="sxs-lookup"><span data-stu-id="694b3-136">Navigation in the Gantt chart</span></span>

- <span data-ttu-id="694b3-137">Chcete-li rozbalit vybranou skupinu a zobrazit podrobnosti, vyberte ve stromovém zobrazení znaménko plus (**+**).</span><span class="sxs-lookup"><span data-stu-id="694b3-137">To expand the selected group and show the details, select the plus sign (**+**) in the tree view.</span></span>
- <span data-ttu-id="694b3-138">Chcete-li sbalit vybranou skupinu, vyberte ve stromovém zobrazení znaménko mínus (**-**).</span><span class="sxs-lookup"><span data-stu-id="694b3-138">To collapse the selected group, select the minus sign (**–**) in the tree view.</span></span>
- <span data-ttu-id="694b3-139">K navigaci můžete používat klávesnici.</span><span class="sxs-lookup"><span data-stu-id="694b3-139">You can use your keyboard for navigation.</span></span> <span data-ttu-id="694b3-140">K pohybu mezi řádky používejte **šipku nahoru** a **šipku dolů**.</span><span class="sxs-lookup"><span data-stu-id="694b3-140">Use the **Up arrow** and **Down arrow** keys to move between rows.</span></span> <span data-ttu-id="694b3-141">K rozbalení a sbalení skupin použijte klávesy **šipka vpravo** a **šipka vlevo**.</span><span class="sxs-lookup"><span data-stu-id="694b3-141">Use the **Right arrow** and **Left arrow** keys to expand and collapse groups.</span></span>
- <span data-ttu-id="694b3-142">Chcete-li otevřít nebo zavřít všechny úrovně v Ganttově diagramu, vyberte možnost **rozbalit vše** nebo **Sbalit vše**.</span><span class="sxs-lookup"><span data-stu-id="694b3-142">To open or close all levels in the Gantt chart, select **Expand all** or **Collapse all**.</span></span>
- <span data-ttu-id="694b3-143">Chcete-li zobrazit související čas zpracování, podržte ukazatel myši nad úkolem.</span><span class="sxs-lookup"><span data-stu-id="694b3-143">To view the related processing time, hover over a task.</span></span> <span data-ttu-id="694b3-144">(Úkoly jsou na nejnižší úrovni v Ganttově diagramu.)</span><span class="sxs-lookup"><span data-stu-id="694b3-144">(Tasks are the lowest level in the Gantt chart.)</span></span>

#### <a name="view-an-additional-master-planning-run-to-compare-jobs"></a><span data-ttu-id="694b3-145">Zobrazení dalšího spuštění hlavního plánování pro porovnání úloh</span><span class="sxs-lookup"><span data-stu-id="694b3-145">View an additional master planning run to compare jobs</span></span>

<span data-ttu-id="694b3-146">Výběrem úlohy hlavního plánování v poli **Zobrazit další spuštění hlavního plánování** můžete zobrazit další spuštění hlavního plánování v Ganttově diagramu a porovnat tyto dvě úlohy.</span><span class="sxs-lookup"><span data-stu-id="694b3-146">By selecting a master planning job on field **Show additional master planning run**, you can view an additional master planning run in the Gantt chart and compare the two jobs.</span></span>

#### <a name="bom-level-display"></a><span data-ttu-id="694b3-147">Zobrazení na úrovni kusovníku</span><span class="sxs-lookup"><span data-stu-id="694b3-147">BOM-level display</span></span>

<span data-ttu-id="694b3-148">Úrovně kusovníku se zobrazují různě pro plánování disponibility, zpoždění, akce a potvrzování.</span><span class="sxs-lookup"><span data-stu-id="694b3-148">Bill of materials (BOM) levels are shown differently for coverage planning, delays, actions, and firming.</span></span>

- <span data-ttu-id="694b3-149">**Plánování disponibility** – úrovně kusovníku se zobrazují očekávaným způsobem.</span><span class="sxs-lookup"><span data-stu-id="694b3-149">**Coverage planning** – BOM levels are shown as expected.</span></span> <span data-ttu-id="694b3-150">Ty jsou vypočteny shora dolů.</span><span class="sxs-lookup"><span data-stu-id="694b3-150">They are calculated from the top down.</span></span>

    <span data-ttu-id="694b3-151">**Příklad:** úroveň kusovníku 0, 1, 2</span><span class="sxs-lookup"><span data-stu-id="694b3-151">**Example:** BOM level 0, 1, 2</span></span>

- <span data-ttu-id="694b3-152">**Zpoždění** – úrovně kusovníku se zobrazují jako úrovně kusovníku plánování disponibility násobené hodnotou-1.</span><span class="sxs-lookup"><span data-stu-id="694b3-152">**Delays** – BOM levels are shown as the coverage planning BOM levels multiplied by –1.</span></span> <span data-ttu-id="694b3-153">(Jinými slovy, mají záporné znaménko.)</span><span class="sxs-lookup"><span data-stu-id="694b3-153">(In other words, they have a negative sign.)</span></span>

    <span data-ttu-id="694b3-154">**Příklad:** úroveň kusovníku –2, –1, 0</span><span class="sxs-lookup"><span data-stu-id="694b3-154">**Example:** BOM level –2, –1, 0</span></span>

- <span data-ttu-id="694b3-155">**Zpráva akce** – úrovně kusovníku se zobrazují očekávaným způsobem.</span><span class="sxs-lookup"><span data-stu-id="694b3-155">**Action message** – BOM levels are shown as expected.</span></span> <span data-ttu-id="694b3-156">Ty jsou vypočteny shora dolů.</span><span class="sxs-lookup"><span data-stu-id="694b3-156">They are calculated from the top down.</span></span>

    <span data-ttu-id="694b3-157">**Příklad:** úroveň kusovníku 0, 1, 2</span><span class="sxs-lookup"><span data-stu-id="694b3-157">**Example:** BOM level 0, 1, 2</span></span>

- <span data-ttu-id="694b3-158">**Automatické potvrzení** – úrovně kusovníku jsou zobrazeny jako 999 mínus úroveň kusovníku plánování disponibility.</span><span class="sxs-lookup"><span data-stu-id="694b3-158">**Auto-firming** – BOM levels are shown as 999 minus the coverage planning BOM level.</span></span>

    <span data-ttu-id="694b3-159">**Příklad:** úroveň kusovníku 999, 998, 997</span><span class="sxs-lookup"><span data-stu-id="694b3-159">**Example:** BOM level 999, 998, 997</span></span>

<span data-ttu-id="694b3-160">Chování je shrnuto v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="694b3-160">The following table summarizes the behavior.</span></span>

| <span data-ttu-id="694b3-161">Zobrazená úroveň kusovníku</span><span class="sxs-lookup"><span data-stu-id="694b3-161">BOM level that is shown</span></span> | <span data-ttu-id="694b3-162">Koncové zboží</span><span class="sxs-lookup"><span data-stu-id="694b3-162">End item</span></span> | <span data-ttu-id="694b3-163">Dílčí komponenta</span><span class="sxs-lookup"><span data-stu-id="694b3-163">Subcomponent</span></span> | <span data-ttu-id="694b3-164">Surovina</span><span class="sxs-lookup"><span data-stu-id="694b3-164">Raw material</span></span> |
|---|---|---|---|
| <span data-ttu-id="694b3-165">Plánování disponibility</span><span class="sxs-lookup"><span data-stu-id="694b3-165">Coverage planning</span></span> | <span data-ttu-id="694b3-166">0</span><span class="sxs-lookup"><span data-stu-id="694b3-166">0</span></span> | <span data-ttu-id="694b3-167">1</span><span class="sxs-lookup"><span data-stu-id="694b3-167">1</span></span> | <span data-ttu-id="694b3-168">2</span><span class="sxs-lookup"><span data-stu-id="694b3-168">2</span></span> |
| <span data-ttu-id="694b3-169">Zpoždění</span><span class="sxs-lookup"><span data-stu-id="694b3-169">Delays</span></span> | <span data-ttu-id="694b3-170">0</span><span class="sxs-lookup"><span data-stu-id="694b3-170">0</span></span> | <span data-ttu-id="694b3-171">–1</span><span class="sxs-lookup"><span data-stu-id="694b3-171">–1</span></span> | <span data-ttu-id="694b3-172">–2</span><span class="sxs-lookup"><span data-stu-id="694b3-172">–2</span></span> |
| <span data-ttu-id="694b3-173">Zpráva akce</span><span class="sxs-lookup"><span data-stu-id="694b3-173">Action message</span></span> | <span data-ttu-id="694b3-174">0</span><span class="sxs-lookup"><span data-stu-id="694b3-174">0</span></span> | <span data-ttu-id="694b3-175">1</span><span class="sxs-lookup"><span data-stu-id="694b3-175">1</span></span> | <span data-ttu-id="694b3-176">2</span><span class="sxs-lookup"><span data-stu-id="694b3-176">2</span></span> |
| <span data-ttu-id="694b3-177">Automatické potvrzování</span><span class="sxs-lookup"><span data-stu-id="694b3-177">Auto-firming</span></span> | <span data-ttu-id="694b3-178">999</span><span class="sxs-lookup"><span data-stu-id="694b3-178">999</span></span> | <span data-ttu-id="694b3-179">998</span><span class="sxs-lookup"><span data-stu-id="694b3-179">998</span></span> | <span data-ttu-id="694b3-180">997</span><span class="sxs-lookup"><span data-stu-id="694b3-180">997</span></span> |

#### <a name="visualize-progress"></a><span data-ttu-id="694b3-181">Průběh vizualizace</span><span class="sxs-lookup"><span data-stu-id="694b3-181">Visualize progress</span></span>

<span data-ttu-id="694b3-182">Pokud zobrazíte úlohu hlavního plánování, která je aktuálně spuštěna, zobrazí se průběh v Ganttově diagramu prostřednictvím barev.</span><span class="sxs-lookup"><span data-stu-id="694b3-182">If you view a master planning job that is currently running, progress is shown through colors in the Gantt chart.</span></span> <span data-ttu-id="694b3-183">Pro modrý motiv se aplikují následující barvy:</span><span class="sxs-lookup"><span data-stu-id="694b3-183">The following colors apply to the blue theme.</span></span> <span data-ttu-id="694b3-184">U jiných barevných motivů se barvy liší.</span><span class="sxs-lookup"><span data-stu-id="694b3-184">For other color themes, the colors will differ.</span></span>

- <span data-ttu-id="694b3-185">**Tmavě modrá** – dokončené plánované úkoly.</span><span class="sxs-lookup"><span data-stu-id="694b3-185">**Dark blue** – Completed planning tasks.</span></span>
- <span data-ttu-id="694b3-186">**Oranžová** – úkol, který právě probíhá.</span><span class="sxs-lookup"><span data-stu-id="694b3-186">**Orange** – The task that is currently in progress.</span></span>
- <span data-ttu-id="694b3-187">**Světle modrá** – odhad pro zbývající úkoly.</span><span class="sxs-lookup"><span data-stu-id="694b3-187">**Light blue** – The estimate for remaining tasks.</span></span>

<span data-ttu-id="694b3-188">Barva se zobrazí pouze na nejnižší úrovni v Ganttově diagramu.</span><span class="sxs-lookup"><span data-stu-id="694b3-188">The color is shown only on the lowest level in the Gantt chart.</span></span> <span data-ttu-id="694b3-189">Výběrem možnosti **Rozbalit vše** zobrazte všechny úkoly v rámci úlohy hlavního plánování.</span><span class="sxs-lookup"><span data-stu-id="694b3-189">Select **Expand all** to view all tasks in the master planning job.</span></span> <span data-ttu-id="694b3-190">Odhad zbývajících úkolů je založen na historických úlohách hlavního plánování.</span><span class="sxs-lookup"><span data-stu-id="694b3-190">The estimate of remaining tasks is based on historical master planning jobs.</span></span>

## <a name="run-master-planning-and-track-processing-time"></a><span data-ttu-id="694b3-191">Spustit hlavní plánování a sledovat čas zpracování</span><span class="sxs-lookup"><span data-stu-id="694b3-191">Run master planning and track processing time</span></span>

1. <span data-ttu-id="694b3-192">Na výchozím řídicím panelu vyberte **Hlavní plánování**.</span><span class="sxs-lookup"><span data-stu-id="694b3-192">On the default dashboard, select **Master planning**.</span></span>
1. <span data-ttu-id="694b3-193">V poli **Plán** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="694b3-193">In the **Plan** field, enter or select a value.</span></span>
1. <span data-ttu-id="694b3-194">Vyberte **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="694b3-194">Select **Run**.</span></span>
1. <span data-ttu-id="694b3-195">Nastavte možnost **Sledovat čas zpracování** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="694b3-195">Set the **Track processing time** option to **Yes**.</span></span>
1. <span data-ttu-id="694b3-196">Do pole **Počet vláken** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="694b3-196">In the **Number of threads** field, enter a number.</span></span>
1. <span data-ttu-id="694b3-197">Na pevné záložce **záznamy, které mají být zahrnuty** vyberte možnost **Filtr**.</span><span class="sxs-lookup"><span data-stu-id="694b3-197">On the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="694b3-198">V mřížce vyberte řádek, ve kterém je pole **Pole** nastaveno na **číslo položky**.</span><span class="sxs-lookup"><span data-stu-id="694b3-198">In the grid, select the row where the **Field** field is set to **Item number**.</span></span>
1. <span data-ttu-id="694b3-199">Zadejte hodnotu do pole **Kritéria**.</span><span class="sxs-lookup"><span data-stu-id="694b3-199">In the **Criteria** field, enter a value.</span></span>
1. <span data-ttu-id="694b3-200">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="694b3-200">Select **OK**.</span></span>
