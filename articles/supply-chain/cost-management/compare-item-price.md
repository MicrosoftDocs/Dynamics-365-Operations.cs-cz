---
title: Porovnat sestavu úložiště cen položek
description: Naučte se generovat sestavu porovnávacího úložiště cen položek a poté procházet a exportovat výsledek.
author: AndersGirke
manager: AnnBe
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostAdminWorkspace, CostAnalysisWorkspace, InventItemPriceCompareStorage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2020-03-01
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 80e376db3616af27d94ee55480cd2f56441db93b
ms.sourcegitcommit: 0dace221e8874021dd212271567666f717d39793
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/19/2020
ms.locfileid: "3072108"
---
# <a name="compare-item-prices-storage-report"></a><span data-ttu-id="df7ae-103">Porovnat sestavu úložiště cen položek</span><span class="sxs-lookup"><span data-stu-id="df7ae-103">Compare item prices storage report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="df7ae-104">V tomto tématu je vysvětleno, jak spustit sestavu **Porovnání úložiště cen položek** a zpřístupnit výstup digitálně, a to buď jako interaktivní stránku v Dynamics 365 Supply Chain Management nebo jako exportovaný dokument v některém z několika formátů.</span><span class="sxs-lookup"><span data-stu-id="df7ae-104">This topic explains how to run a **Compare item prices storage** report and make the output available digitally, either as an interactive page in Dynamics 365 Supply Chain Management, or as an exported document in any of several formats.</span></span>

<span data-ttu-id="df7ae-105">Pokud zobrazíte sestavu ve svém prohlížeči, sloupce a agregované zůstatky jsou v závislosti na konfigurovaném rozvržení dynamicky upravovány.</span><span class="sxs-lookup"><span data-stu-id="df7ae-105">When you view the report in your browser, columns and aggregate balances are dynamically adjusted, depending on your configured layout.</span></span> <span data-ttu-id="df7ae-106">Výsledky můžete řadit, filtrovat, přecházet k podrobnostem atd.</span><span class="sxs-lookup"><span data-stu-id="df7ae-106">You can sort the results, filter them, drill down into the data, and more.</span></span>

<span data-ttu-id="df7ae-107">Výsledky sestavy jsou uloženy v datové entitě **Porovnat ceny položek**, což umožňuje filtrovat a exportovat výsledky do formátu, jako je například CSV nebo Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="df7ae-107">Report results are stored in the **Compare item prices** data entity, which lets you filter and export the results to a format such as CSV or Microsoft Excel.</span></span>

<span data-ttu-id="df7ae-108">Sestava **Porovnání úložiště cen položek** je užitečná v případech, kdy výstup obsahuje mnoho řádků.</span><span class="sxs-lookup"><span data-stu-id="df7ae-108">The **Compare item prices storage** report is helpful in cases where the output contains many lines.</span></span> <span data-ttu-id="df7ae-109">Výstup bude obsahovat například mnoho řádků v případě, že máte více než 40 000 položek, které mají v nákladové verzi pozastavenou cenu položky.</span><span class="sxs-lookup"><span data-stu-id="df7ae-109">For example, the output will contain many lines if you have more than 40,000 items holding a pending item price in the costing version.</span></span>

## <a name="enable-compare-item-prices-storage"></a><span data-ttu-id="df7ae-110">Povolit porovnání úložiště cen položek</span><span class="sxs-lookup"><span data-stu-id="df7ae-110">Enable compare item prices storage</span></span>

<span data-ttu-id="df7ae-111">Než můžete použít tuto funkci, musíte ji povolit ve svém systému.</span><span class="sxs-lookup"><span data-stu-id="df7ae-111">Before you can use this feature, you must enable it on your system.</span></span> <span data-ttu-id="df7ae-112">Správci mohou pomocí nastavení [správa funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a povolit je v případě potřeby.</span><span class="sxs-lookup"><span data-stu-id="df7ae-112">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the feature status and enable it if needed.</span></span> <span data-ttu-id="df7ae-113">Tato funkce je uvedena jako:</span><span class="sxs-lookup"><span data-stu-id="df7ae-113">Here, the feature is listed as:</span></span>

- <span data-ttu-id="df7ae-114">**Modul** - Správa nákladů</span><span class="sxs-lookup"><span data-stu-id="df7ae-114">**Module** - Cost management</span></span>
- <span data-ttu-id="df7ae-115">**Název funkce** – Porovnání úložiště cen položky</span><span class="sxs-lookup"><span data-stu-id="df7ae-115">**Feature name** - Compare item price storage</span></span>

## <a name="generate-a-compare-item-prices-storage-report"></a><span data-ttu-id="df7ae-116">Generovat sestavu s porovnáním cen položek</span><span class="sxs-lookup"><span data-stu-id="df7ae-116">Generate a Compare item prices storage report</span></span>

<span data-ttu-id="df7ae-117">Chcete-li vytvořit a uložit sestavu **Porovnat sestavu úložiště cen položek**, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="df7ae-117">Follow these steps to generate and store a **Compare item prices storage** report:</span></span>

1. <span data-ttu-id="df7ae-118">Přejděte na **Řízení nákladů > Dotazy a sestavy > Předem stanovené sestavy nákladů > Porovnání úložiště cen položek**.</span><span class="sxs-lookup"><span data-stu-id="df7ae-118">Go to **Cost management > Inquiries and reports > Predetermined cost reports > Compare item prices storage**.</span></span>

1. <span data-ttu-id="df7ae-119">Výběrem **Nový** otevřete podokno **Porovnat ceny položek**.</span><span class="sxs-lookup"><span data-stu-id="df7ae-119">Select **New** to open the **Compare item prices** pane.</span></span> <span data-ttu-id="df7ae-120">Chcete-li definovat ceny, které mají být porovnány v sestavě, nastavte následující volby:</span><span class="sxs-lookup"><span data-stu-id="df7ae-120">Set the following options to define which prices to compare in your report:</span></span>

    - <span data-ttu-id="df7ae-121">Na pevné záložce **Parametry** zadejte jedinečný **Název** sestavy a použijte pole v sekcích **Nevyřízené ceny pro porovnání** a **Ceny použité pro porovnání** a definujte, které ceny a kalendářní data chcete porovnat.</span><span class="sxs-lookup"><span data-stu-id="df7ae-121">On the **Parameters** FastTab, give the report a unique **Name** and use the fields in the **Pending prices to compare** and **Prices used for comparison** sections to define which prices and dates to compare.</span></span>
    - <span data-ttu-id="df7ae-122">Na pevné záložce **Záznamy, které mají být zahrnuty** nastavte filtry a omezení, která definují, která data mají být do sestavy zahrnuta.</span><span class="sxs-lookup"><span data-stu-id="df7ae-122">On the **Records to include** FastTab, set up filters and constraints to define which data to include in the report.</span></span>
    - <span data-ttu-id="df7ae-123">Na pevné záložce **Spustit na pozadí** nastavte, jak, kdy a jak často chcete sestavu generovat.</span><span class="sxs-lookup"><span data-stu-id="df7ae-123">On the **Run in the background** FastTab, set up how, when, and the frequency at which you want to generate the report.</span></span>
    > [!NOTE]
    > <span data-ttu-id="df7ae-124">Tato sestava se vždy spustí jako součást dávkové úlohy.</span><span class="sxs-lookup"><span data-stu-id="df7ae-124">This report is always executed as part of a batch job.</span></span>

1. <span data-ttu-id="df7ae-125">Vyberte **OK**, pokud chcete použít své nastavení a zavřete podokno.</span><span class="sxs-lookup"><span data-stu-id="df7ae-125">Select **OK** to apply your settings and close the pane.</span></span>

1. <span data-ttu-id="df7ae-126">Po dokončení dávkové úlohy bude tato úloha uvedena na stránce **Porovnat úložiště cen položek**.</span><span class="sxs-lookup"><span data-stu-id="df7ae-126">After the batch job is completed, it will be listed on the **Compare item prices storage** page.</span></span> <span data-ttu-id="df7ae-127">Možná budete muset stránku obnovit pro zobrazení sestavy.</span><span class="sxs-lookup"><span data-stu-id="df7ae-127">You may need to refresh the page to see the report.</span></span>

## <a name="explore-the-compare-item-prices-storage-report"></a><span data-ttu-id="df7ae-128">Prozkoumejte sestavu Porovnat úložiště cen položek</span><span class="sxs-lookup"><span data-stu-id="df7ae-128">Explore the Compare item prices storage report</span></span>

<span data-ttu-id="df7ae-129">Po vygenerování sestavy ji můžete kdykoli zobrazit a prozkoumat následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="df7ae-129">After you've generated a report, you can view and explore it at any time as follows:</span></span>

1. <span data-ttu-id="df7ae-130">Přejděte na **Řízení nákladů > Dotazy a sestavy > Předem stanovené sestavy nákladů > Porovnání úložiště cen položek**.</span><span class="sxs-lookup"><span data-stu-id="df7ae-130">Go to **Cost management > Inquiries and reports > Predetermined cost reports > Compare item prices storage**.</span></span>

1. <span data-ttu-id="df7ae-131">Vyberte sestavu ze seznamu.</span><span class="sxs-lookup"><span data-stu-id="df7ae-131">Select a report from the list.</span></span>

1. <span data-ttu-id="df7ae-132">Proveďte některou z následujících akcí:</span><span class="sxs-lookup"><span data-stu-id="df7ae-132">Do one of the following:</span></span>

    - <span data-ttu-id="df7ae-133">Vyberte **Přehled**, chcete-li získat přehled výsledků sestavy.</span><span class="sxs-lookup"><span data-stu-id="df7ae-133">Select **Overview** to get an overview of your report results.</span></span>
    - <span data-ttu-id="df7ae-134">Vyberte **Zobrazit podrobnosti**, chcete-li získat podrobnější zobrazení sestavy</span><span class="sxs-lookup"><span data-stu-id="df7ae-134">Select **View details** to get a more detailed view of your report</span></span>

1. <span data-ttu-id="df7ae-135">Po otevření vybraného zobrazení můžete provést následující:</span><span class="sxs-lookup"><span data-stu-id="df7ae-135">After the selected view opens, you can do the following:</span></span>

    - <span data-ttu-id="df7ae-136">Vyberte téměř libovolné záhlaví sloupce, chcete-li tabulku seřadit nebo filtrovat podle hodnot v tomto sloupci, stejně jako u většiny standardních formulářů v Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="df7ae-136">Select almost any column heading to sort or filter the table by values in that column, just as with most standard forms in Supply Chain Management.</span></span> <span data-ttu-id="df7ae-137">Poznámka: není možné třídit nebo filtrovat sloupec **Čistá změna ceny v %**, protože se jedná o počítané pole.</span><span class="sxs-lookup"><span data-stu-id="df7ae-137">Note, you can't sort or filter the **Net change price %** column because it's a calculated field.</span></span>
    - <span data-ttu-id="df7ae-138">Výběrem možnosti **Zobrazení dimenze** otevřete podokno, ve kterém můžete vybrat sloupec dimenze, který má být zahrnut ve formuláři.</span><span class="sxs-lookup"><span data-stu-id="df7ae-138">Select **Dimension display** to open a pane where you can choose which dimension column to include on the form.</span></span> <span data-ttu-id="df7ae-139">Nastavte **Uložit nastavení** na **Ano**, pokud chcete nastavení uložit, aby byla při příštím otevření sestavy zachována.</span><span class="sxs-lookup"><span data-stu-id="df7ae-139">Set **Save setup** to **Yes** if you'd like to save these settings so they will be preserved the next time you open the report.</span></span> <span data-ttu-id="df7ae-140">Vyberte **OK**, pokud chcete použít své nastavení a zavřete.</span><span class="sxs-lookup"><span data-stu-id="df7ae-140">Select **OK** to apply your settings and close.</span></span>
    - <span data-ttu-id="df7ae-141">Vyberte libovolný řádek ve formuláři a pak výběrem možnosti **Zobrazit podrobnosti** zobrazte další informace o vybrané položce.</span><span class="sxs-lookup"><span data-stu-id="df7ae-141">Select any row in the form and then select **View details** to see more information about the selected item.</span></span> <span data-ttu-id="df7ae-142">Z tohoto místa budete moci přejít k datům.</span><span class="sxs-lookup"><span data-stu-id="df7ae-142">You'll be able to drill down into the data from here.</span></span>
    - <span data-ttu-id="df7ae-143">Vyberte libovolný řádek ve formuláři a pak výběrem možnosti **Zobrazit srovnávací graf** zobrazte interaktivní grafické znázornění výsledků, které se vztahují k vybrané položce.</span><span class="sxs-lookup"><span data-stu-id="df7ae-143">Select any row in the form and then select **View comparison chart** to see an interactive graphical representation of your results as they relate to your selected item.</span></span> <span data-ttu-id="df7ae-144">Tyto výsledky můžete prozkoumat výběrem různých grafických prvků v tabulce a legendě grafu.</span><span class="sxs-lookup"><span data-stu-id="df7ae-144">You can explore these results by selecting various graphical elements in the chart and chart legend.</span></span>
    - <span data-ttu-id="df7ae-145">Vyberte libovolný řádek ve formuláři a pak výběrem možnosti **Zobrazit podrobnosti výpočtu** zobrazte další informace o výpočtech vztahujících se k vybrané položce.</span><span class="sxs-lookup"><span data-stu-id="df7ae-145">Select any row in the form and then select **View calculation details** to see more information about calculations related to the selected item.</span></span> <span data-ttu-id="df7ae-146">Z tohoto místa budete moci přejít k datům.</span><span class="sxs-lookup"><span data-stu-id="df7ae-146">You'll be able to drill down into the data from here.</span></span>

## <a name="export-the-compare-item-prices-storage-report"></a><span data-ttu-id="df7ae-147">Exportujte sestavu Porovnat úložiště cen položek</span><span class="sxs-lookup"><span data-stu-id="df7ae-147">Export the Compare item prices storage report</span></span>

<span data-ttu-id="df7ae-148">Každá generovaná sestava je uložena v datové entitě **Porovnat ceny položek**.</span><span class="sxs-lookup"><span data-stu-id="df7ae-148">Each report that you generate is stored in the **Compare item prices** data entity.</span></span> <span data-ttu-id="df7ae-149">Pomocí standardních funkcí Supply Chain Management můžete exportovat data z této entity do libovolného podporovaného formátu dat, včetně formátu CSV nebo Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="df7ae-149">You can use the standard data management features of Supply Chain Management to export data from this entity to any supported data format, including CSV or Microsoft Excel.</span></span>

<span data-ttu-id="df7ae-150">Následuje příklad exportu sestavy **Porovnání úložiště cen položek**:</span><span class="sxs-lookup"><span data-stu-id="df7ae-150">The following is an example of how to export a **Compare item prices storage** report:</span></span>

1. <span data-ttu-id="df7ae-151">Přejděte do nabídky **Správa systému > Pracovní prostory > Správa dat**.</span><span class="sxs-lookup"><span data-stu-id="df7ae-151">Go to **System administration > Workspaces > Data management**.</span></span>

1. <span data-ttu-id="df7ae-152">Vyberte tlačítko **Export** v části **Správa dat**.</span><span class="sxs-lookup"><span data-stu-id="df7ae-152">Select the **Export** button in the **Data management** section.</span></span>

1. <span data-ttu-id="df7ae-153">Otevře se stránka **Export**, kterou použijete k nastavení úlohy exportu.</span><span class="sxs-lookup"><span data-stu-id="df7ae-153">The **Export** page opens, which you'll use to set up your export job.</span></span> <span data-ttu-id="df7ae-154">Začněte tím, že své úloze zadáte **Název skupiny**.</span><span class="sxs-lookup"><span data-stu-id="df7ae-154">Start by giving your job a **Group name**.</span></span>

1. <span data-ttu-id="df7ae-155">V části **Vybrané entity** vyberte možnost **Přidat entitu** a otevřete dialogové okno, ve kterém můžete nastavit následující možnosti:</span><span class="sxs-lookup"><span data-stu-id="df7ae-155">In the **Selected entities** section, select **Add entity** to open a dialog box where you can set the following options:</span></span>

    - <span data-ttu-id="df7ae-156">**Název entity** – vyberte **Porovnat ceny položek**.</span><span class="sxs-lookup"><span data-stu-id="df7ae-156">**Entity name** - Select **Compare item prices**.</span></span>
    - <span data-ttu-id="df7ae-157">**Formát cílových dat** – vyberte formát, do kterého chcete exportovat.</span><span class="sxs-lookup"><span data-stu-id="df7ae-157">**Target data format** - Choose the format that you want to export to.</span></span>

1. <span data-ttu-id="df7ae-158">Vyberte **Přidat**, chcete-li přidat nový řádek a vyberte **Zavřít** pro zavření dialogového okna.</span><span class="sxs-lookup"><span data-stu-id="df7ae-158">Select **Add** to add the new row and then select **Close** to close the dialog box.</span></span>

1. <span data-ttu-id="df7ae-159">Obvykle exportujete vždy jednu sestavu.</span><span class="sxs-lookup"><span data-stu-id="df7ae-159">Usually you'll export one report at a time.</span></span> <span data-ttu-id="df7ae-160">Provedete to tak, že nastavíte **Filtr** pro řádek, který jste právě přidali do podokna **Dotaz**.</span><span class="sxs-lookup"><span data-stu-id="df7ae-160">To do this, set up a **Filter** for the row you just added to the **Inquiry** pane.</span></span> <span data-ttu-id="df7ae-161">To vám umožní definovat sestavy z entity **Porovnat ceny položek**, kterou chcete zahrnout do exportu.</span><span class="sxs-lookup"><span data-stu-id="df7ae-161">This will let you define which reports from the **Compare item prices** entity that you want to include in your export.</span></span> <span data-ttu-id="df7ae-162">Chcete-li exportovat jednu sestavu, nastavte následující možnosti filtrování:</span><span class="sxs-lookup"><span data-stu-id="df7ae-162">Set the following filter options to export a single report:</span></span>

    - <span data-ttu-id="df7ae-163">Na kartě **Rozsah** vyberte možnost **Přidat** a přidejte nový řádek.</span><span class="sxs-lookup"><span data-stu-id="df7ae-163">On the **Range** tab, select **Add** to add a new row.</span></span>
    - <span data-ttu-id="df7ae-164">Nastavte **Tabulku** pro **Porovnání cen položek**.</span><span class="sxs-lookup"><span data-stu-id="df7ae-164">Set **Table** to **Compare item prices**.</span></span>
    - <span data-ttu-id="df7ae-165">Nastavte **Odvozenou tabulku** pro **Porovnání cen položek**.</span><span class="sxs-lookup"><span data-stu-id="df7ae-165">Set **Derived table** to **Compare item prices**.</span></span>
    - <span data-ttu-id="df7ae-166">Nastavte **Pole** na pole, podle kterého chcete filtrovat.</span><span class="sxs-lookup"><span data-stu-id="df7ae-166">Set **Field** to the field that you want to filter by.</span></span> <span data-ttu-id="df7ae-167">Obvykle použijete **Název provedení** nebo **Čas provedení**.</span><span class="sxs-lookup"><span data-stu-id="df7ae-167">Usually you'll use **Execution name** or **Execution time**.</span></span>
    - <span data-ttu-id="df7ae-168">Nastavte **Kritéria** na hodnotu z vybraného pole, které chcete vyhledat (buď název sestavy, nebo čas vygenerování sestavy).</span><span class="sxs-lookup"><span data-stu-id="df7ae-168">Set **Criteria** to the value from your selected field that you want to look for (either the name of the report or the time the report was generated).</span></span>
    - <span data-ttu-id="df7ae-169">V případě potřeby přidejte do tabulky **Rozsah** další řádky, dokud neurčíte jedinečnou sestavu, kterou hledáte.</span><span class="sxs-lookup"><span data-stu-id="df7ae-169">If necessary, add more rows to the **Range** table until you have uniquely identified the report that you're looking for.</span></span>

1. <span data-ttu-id="df7ae-170">Vyberte **OK**, pokud chcete uložit své nastavení a zavřít.</span><span class="sxs-lookup"><span data-stu-id="df7ae-170">Select **OK** to save your settings and close.</span></span>

1. <span data-ttu-id="df7ae-171">Nastavení exportu uložíte výběrem možnosti **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="df7ae-171">Select **Save** to save your export setup.</span></span>

1. <span data-ttu-id="df7ae-172">Otevřete kartu **Možnosti exportu** a výběrem volby **Exportovat nyní** vygenerujte exportovaný soubor.</span><span class="sxs-lookup"><span data-stu-id="df7ae-172">Open the **Export options** tab and select **Export now** to generate the export file.</span></span>

1. <span data-ttu-id="df7ae-173">Otevře se stránka **Souhrn spuštění**, v níž se zobrazí stav úlohy exportu a seznam exportovaných entit.</span><span class="sxs-lookup"><span data-stu-id="df7ae-173">The **Execution summary** page opens, where you can see the status of your export job and a list of entities that were exported.</span></span> <span data-ttu-id="df7ae-174">Vyberte entitu **Porovnat ceny zboží**, která je uvedena v oblasti **Stav zpracování entity** a poté vyberte **Stáhnout soubor** pro stažení dat exportovaných z této entity.</span><span class="sxs-lookup"><span data-stu-id="df7ae-174">Select the **Compare item prices** entity listed in the **Entity processing status** area and then select **Download file** to download the data exported from that entity.</span></span>

<span data-ttu-id="df7ae-175">Další informace o tom, jak používat správu dat k exportu dat, naleznete v tématu [Přehled úloh importu a exportu dat](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span><span class="sxs-lookup"><span data-stu-id="df7ae-175">For more information about how to use data management to export data, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md).</span></span>
