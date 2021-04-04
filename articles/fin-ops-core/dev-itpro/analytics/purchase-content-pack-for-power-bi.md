---
title: Analýza obsahu výdajů na nákup v Power BI
description: Toto téma popisuje, co je součástí obsahu analýzy nákupu a výdajů v Power BI.
author: FrankDahl
manager: AnnBe
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a4149b13754b544558dbb5666fbec7df97e5c5d8
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559542"
---
# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="5cb42-103">Analýza obsahu výdajů na nákup v Power BI</span><span class="sxs-lookup"><span data-stu-id="5cb42-103">Purchase spend analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5cb42-104">Toto téma popisuje, co je součástí obsahu **analýzy nákupu a výdajů** v Microsoft Power BI.</span><span class="sxs-lookup"><span data-stu-id="5cb42-104">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="5cb42-105">Vysvětluje přístup k sestavám Power BI a poskytuje informace o datovém modelu a entitách, které byly použity k sestavení obsahu.</span><span class="sxs-lookup"><span data-stu-id="5cb42-105">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="5cb42-106">Přehled</span><span class="sxs-lookup"><span data-stu-id="5cb42-106">Overview</span></span>

<span data-ttu-id="5cb42-107">Obsah **Analýza nákupních výdajů** v Power BI byl vytvořen, aby pomohl nákupním manažerům a vedoucím pracovníkům, kteří odpovídají za rozpočty, sledovat nákupní výdaje.</span><span class="sxs-lookup"><span data-stu-id="5cb42-107">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep track of purchase spending.</span></span> <span data-ttu-id="5cb42-108">Manažeři mohou analyzovat nákupní výdaje následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="5cb42-108">Managers can analyze purchase spending in the following ways:</span></span>

- <span data-ttu-id="5cb42-109">Nákup k datu v daném roce (podle skupiny dodavatelů a jednotlivých dodavatelů, kategorie zásobování a jednotlivých produktů a umístění dodavatele)</span><span class="sxs-lookup"><span data-stu-id="5cb42-109">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
- <span data-ttu-id="5cb42-110">Rok přes rok nákupu změna (podle skupiny a zadávání zakázek kategorií dodavatele)</span><span class="sxs-lookup"><span data-stu-id="5cb42-110">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="5cb42-111">Obsah používá nákupní transakční data a poskytuje agregované zobrazení nákupní celopodnikových údajů a rozpis nákupních výdajů podle dodavatelů a produktů.</span><span class="sxs-lookup"><span data-stu-id="5cb42-111">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="5cb42-112">V sestavách jsou zvýrazněny změny nákupních výdajů v průběhu času.</span><span class="sxs-lookup"><span data-stu-id="5cb42-112">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="5cb42-113">Proto lze sestavy používat k upozornění manažerů na pozitivní a negativní trendy výdajů u jednotlivých dodavatelů a výrobků.</span><span class="sxs-lookup"><span data-stu-id="5cb42-113">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="5cb42-114">Grafy dále zobrazují nákupní výdaje pro zásobování různých kategorií a skupin dodavatelů.</span><span class="sxs-lookup"><span data-stu-id="5cb42-114">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="5cb42-115">Proto manažeři pro kategorie a regionální manažeři mohou tyto grafy používat k identifikaci změn v chování při výdajích.</span><span class="sxs-lookup"><span data-stu-id="5cb42-115">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="5cb42-116">Přístup k obsahu Power BI</span><span class="sxs-lookup"><span data-stu-id="5cb42-116">Accessing the Power BI content</span></span>
<span data-ttu-id="5cb42-117">Obsah **Analýza nákupu a výdajů** v Power BI se zobrazí na stránce **Analýza nákupu a výdajů** (**Zásobování a zdroje** \> **Dotazy a sestavy** \> **Analýza výkonu nákupu** \> **Analýza nákupu a výdajů**).</span><span class="sxs-lookup"><span data-stu-id="5cb42-117">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** \> **Inquiries and reports** \> **Purchase performance analysis** \> **Purchase and spend analysis**).</span></span>

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="5cb42-118">Metriky, které jsou součástí obsahu Power BI</span><span class="sxs-lookup"><span data-stu-id="5cb42-118">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="5cb42-119">**Balíček obsahu analýzy investic** Power BI do nákupu obsahuje sestavu, která obsahuje sadu metrik.</span><span class="sxs-lookup"><span data-stu-id="5cb42-119">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="5cb42-120">Tyto metriky jsou zobrazována jako grafy, dlaždice a tabulky.</span><span class="sxs-lookup"><span data-stu-id="5cb42-120">These metrics are visualized as charts, tiles, and tables.</span></span> 

<span data-ttu-id="5cb42-121">Následující sekce poskytují přehled vizualizací.</span><span class="sxs-lookup"><span data-stu-id="5cb42-121">The following sections provide an overview of the visualizations.</span></span>

### <a name="purchase-by-vendor-report-page"></a><span data-ttu-id="5cb42-122">Stránka sestavy nákupu podle dodavatele</span><span class="sxs-lookup"><span data-stu-id="5cb42-122">Purchase by vendor report page</span></span>
<span data-ttu-id="5cb42-123">**Grafy**</span><span class="sxs-lookup"><span data-stu-id="5cb42-123">**Charts**</span></span>
- <span data-ttu-id="5cb42-124">Prvních 10 dodavatelů podle nákupu (skládaný sloupcový graf)</span><span class="sxs-lookup"><span data-stu-id="5cb42-124">Top 10 vendors by purchase (stacked bar chart)</span></span>
- <span data-ttu-id="5cb42-125">Celkový nákup podle skupiny dodavatelů / země / name (výsečový graf)</span><span class="sxs-lookup"><span data-stu-id="5cb42-125">Total purchase by vendor group / country / name (pie chart)</span></span>
- <span data-ttu-id="5cb42-126">Nákup podle skupiny dodavatelů / země / název (sloupcový graf)</span><span class="sxs-lookup"><span data-stu-id="5cb42-126">Purchase by vendor group / country / name (column chart)</span></span>
- <span data-ttu-id="5cb42-127">Průměrný nákup podle skupiny dodavatelů / země / název (sloupcový graf)</span><span class="sxs-lookup"><span data-stu-id="5cb42-127">Average purchase by vendor group / country / name (column chart)</span></span>

<span data-ttu-id="5cb42-128">**Dlaždice**</span><span class="sxs-lookup"><span data-stu-id="5cb42-128">**Tiles**</span></span>
- <span data-ttu-id="5cb42-129">Celkový nákup</span><span class="sxs-lookup"><span data-stu-id="5cb42-129">Total purchase</span></span>
- <span data-ttu-id="5cb42-130">Meziroční růst nákupů</span><span class="sxs-lookup"><span data-stu-id="5cb42-130">YOY purchase growth</span></span>
- <span data-ttu-id="5cb42-131">Celkový počet dodavatelů</span><span class="sxs-lookup"><span data-stu-id="5cb42-131">Total # vendors</span></span>
- <span data-ttu-id="5cb42-132">Celkový počet aktivních dodavatelů</span><span class="sxs-lookup"><span data-stu-id="5cb42-132">Total # of active vendors</span></span>

<span data-ttu-id="5cb42-133">**Příklad**</span><span class="sxs-lookup"><span data-stu-id="5cb42-133">**Example**</span></span>
<img src="media/spend1.png" alt="Purchase by vendor">

### <a name="purchase-by-product-report-page"></a><span data-ttu-id="5cb42-134">Stránka sestavy nákupu podle produktu</span><span class="sxs-lookup"><span data-stu-id="5cb42-134">Purchase by product report page</span></span>

<span data-ttu-id="5cb42-135">**Grafy**</span><span class="sxs-lookup"><span data-stu-id="5cb42-135">**Charts**</span></span>
- <span data-ttu-id="5cb42-136">Nákup podle kategorie zásobování / název produktu (sloupcový graf)</span><span class="sxs-lookup"><span data-stu-id="5cb42-136">Purchase by procurement category / product name (column chart)</span></span>
- <span data-ttu-id="5cb42-137">Celkový nákup podle kategorie zásobování / název produktu (výsečový graf)</span><span class="sxs-lookup"><span data-stu-id="5cb42-137">Total purchase by procurement category / product name (pie chart)</span></span>
- <span data-ttu-id="5cb42-138">Prvních 10 produktů podle nákupu (skládaný sloupcový graf)</span><span class="sxs-lookup"><span data-stu-id="5cb42-138">Top 10 products by purchase (stacked bar chart)</span></span>

<span data-ttu-id="5cb42-139">**Dlaždice**</span><span class="sxs-lookup"><span data-stu-id="5cb42-139">**Tiles**</span></span>
- <span data-ttu-id="5cb42-140">Celkový počet produktů</span><span class="sxs-lookup"><span data-stu-id="5cb42-140">Total # of products</span></span></li>
- <span data-ttu-id="5cb42-141">Celkové procento aktivních produktů z celkového počtu produktů</span><span class="sxs-lookup"><span data-stu-id="5cb42-141">Total active products percentage of total # of products</span></span>
- <span data-ttu-id="5cb42-142">Počet účtování produktů pro 80 % nákupů</span><span class="sxs-lookup"><span data-stu-id="5cb42-142">Number of products accounting for 80% purchase</span></span>

<span data-ttu-id="5cb42-143">**Příklad**</span><span class="sxs-lookup"><span data-stu-id="5cb42-143">**Example**</span></span>


<img src="media/purchaseByProduct.png" alt="Purchase by Product">

### <a name="purchase-by-period-report-page"></a><span data-ttu-id="5cb42-144">Stránka sestavy nákupu podle období</span><span class="sxs-lookup"><span data-stu-id="5cb42-144">Purchase by period report page</span></span>
<span data-ttu-id="5cb42-145">Tato stránka zobrazuje nákupy v tomto a minulém roce a růst podle kategorie zásobování.</span><span class="sxs-lookup"><span data-stu-id="5cb42-145">This page shows purchases this year and last year, and growth by procurement category.</span></span>

<span data-ttu-id="5cb42-146">**Grafy**</span><span class="sxs-lookup"><span data-stu-id="5cb42-146">**Charts**</span></span> 
- <span data-ttu-id="5cb42-147">Nákup za měsíc / den (sloupcový graf)</span><span class="sxs-lookup"><span data-stu-id="5cb42-147">Purchase by month / day (column chart)</span></span>
- <span data-ttu-id="5cb42-148">Kumulativní mezirodčí nákupní odchylka (vodopádový graf)</span><span class="sxs-lookup"><span data-stu-id="5cb42-148">Cumulative purchase YOY variance (waterfall chart)</span></span>
- <span data-ttu-id="5cb42-149">Meziroční růst celkového nákupu (sloupcový graf)</span><span class="sxs-lookup"><span data-stu-id="5cb42-149">Total purchase YOY growth (column chart)</span></span>
- <span data-ttu-id="5cb42-150">Prohlášení o zadávání veřejných zakázek (matice)</span><span class="sxs-lookup"><span data-stu-id="5cb42-150">Procurement statement (matrix)</span></span>

<span data-ttu-id="5cb42-151">**Dlaždice**</span><span class="sxs-lookup"><span data-stu-id="5cb42-151">**Tiles**</span></span>
- <span data-ttu-id="5cb42-152">Meziroční růst nákupů</span><span class="sxs-lookup"><span data-stu-id="5cb42-152">YOY purchase growth</span></span>
- <span data-ttu-id="5cb42-153">Meziroční růst nákupů v %</span><span class="sxs-lookup"><span data-stu-id="5cb42-153">YOY purchase growth %</span></span>

<span data-ttu-id="5cb42-154">**Příklad**</span><span class="sxs-lookup"><span data-stu-id="5cb42-154">**Example**</span></span>
<img src="media/purchaseByPeriod.png" alt="Purchase by Period">

### <a name="purchase-by-vendor-location-report-page"></a><span data-ttu-id="5cb42-155">Stránka sestavy nákupu podle místa dodavatele</span><span class="sxs-lookup"><span data-stu-id="5cb42-155">Purchase by vendor location report page</span></span>

<span data-ttu-id="5cb42-156">**Grafy**</span><span class="sxs-lookup"><span data-stu-id="5cb42-156">**Charts**</span></span>
- <span data-ttu-id="5cb42-157">Nákup podle města</span><span class="sxs-lookup"><span data-stu-id="5cb42-157">Purchase by city</span></span>
- <span data-ttu-id="5cb42-158">Meziroční růst nákupů v %</span><span class="sxs-lookup"><span data-stu-id="5cb42-158">Purchase YOY growth %</span></span>
- <span data-ttu-id="5cb42-159">Nákup podle země</span><span class="sxs-lookup"><span data-stu-id="5cb42-159">Purchase by country</span></span>

<span data-ttu-id="5cb42-160">**Příklad**</span><span class="sxs-lookup"><span data-stu-id="5cb42-160">**Example**</span></span>
<img src="media/purchByVendorLocation.png" alt="Purchase by Vendor Location">

### <a name="purchase-spend-analysis-by-time-report-page"></a><span data-ttu-id="5cb42-161">Stránka sestavy analýzy výdajů při nákupu podle času</span><span class="sxs-lookup"><span data-stu-id="5cb42-161">Purchase spend analysis by time report page</span></span>

<span data-ttu-id="5cb42-162">**Grafy**</span><span class="sxs-lookup"><span data-stu-id="5cb42-162">**Charts**</span></span> 
- <span data-ttu-id="5cb42-163">Aktální rok nákupu podle měsíců / den (spojnicový graf)</span><span class="sxs-lookup"><span data-stu-id="5cb42-163">Purchase current year by month / day (line chart)</span></span>
- <span data-ttu-id="5cb42-164">Nákup za aktuální a předchozí rok (řádkový a sloupcový graf)</span><span class="sxs-lookup"><span data-stu-id="5cb42-164">Purchase current and last year (line and column chart)</span></span>

<span data-ttu-id="5cb42-165">**Příklad**</span><span class="sxs-lookup"><span data-stu-id="5cb42-165">**Example**</span></span>
<img src="media/PurchByTIme.png" alt="Purchase by Time">

### <a name="purchase-spend-analysis-by-vendor-report-page"></a><span data-ttu-id="5cb42-166">Stránka sestavy analýzy výdajů při nákupu podle dodavatele</span><span class="sxs-lookup"><span data-stu-id="5cb42-166">Purchase spend analysis by vendor report page</span></span>

<span data-ttu-id="5cb42-167">**Grafy**</span><span class="sxs-lookup"><span data-stu-id="5cb42-167">**Charts**</span></span> 
- <span data-ttu-id="5cb42-168">TOP 10 % nákupů dodavatele nákupní (trychtýřový graf)</span><span class="sxs-lookup"><span data-stu-id="5cb42-168">Top 10 vendor purchase % of purchase (funnel)</span></span>
- <span data-ttu-id="5cb42-169">Top 10 dodavatelů se zvýšenými investicemi meziročně</span><span class="sxs-lookup"><span data-stu-id="5cb42-169">Top 10 vendors with increased spending YOY</span></span>
- <span data-ttu-id="5cb42-170">Top 10 dodavatelů se sníženými investicemi meziročně</span><span class="sxs-lookup"><span data-stu-id="5cb42-170">Top 10 vendors with decreased spending YOY</span></span>

<span data-ttu-id="5cb42-171">**Příklad** 
</span><span class="sxs-lookup"><span data-stu-id="5cb42-171">**Example** 
</span></span><img src="media/PurchSpendAnalysisByVendor.png" alt="Purchase spend by vendor">


## <a name="data-model-and-entities"></a><span data-ttu-id="5cb42-172">Datový model a entity</span><span class="sxs-lookup"><span data-stu-id="5cb42-172">Data model and entities</span></span>
<span data-ttu-id="5cb42-173">Následující data se používají k naplnění stránek sestavy v obsahu **Analýza nákupu a výdajů** v Power BI.</span><span class="sxs-lookup"><span data-stu-id="5cb42-173">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="5cb42-174">Tato data jsou vyjádřena jako agregační měření, která jsou rozfázována v úložišti entit.</span><span class="sxs-lookup"><span data-stu-id="5cb42-174">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="5cb42-175">Úložiště entit je databáze Microsoft SQL Server, která je optimalizována pro analýzu.</span><span class="sxs-lookup"><span data-stu-id="5cb42-175">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="5cb42-176">Další informace naleznete v tématu [Integrace Power BI s úložištěm entit](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="5cb42-176">For more information, see [Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="5cb42-177">Souhrnná opatření v tomto balíčku obsahu jsou podmnožinou celkových opatření, která byla k dispozici v nákupní datové krychli v Microsoft Dynamics AX 2012 a Microsoft Dynamics AX 2012 R3.</span><span class="sxs-lookup"><span data-stu-id="5cb42-177">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="5cb42-178">Příprava fází agregovaných opatření krychle v úložišti Entity vyžaduje, aby bylo možné je nasadit.</span><span class="sxs-lookup"><span data-stu-id="5cb42-178">To stage the cube's aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="5cb42-179">Další informace získáte v postupu nastavování agregovaných opatření v úložišti entity v příspěvku v blogu [Integrace Power BI s úložištěm entity](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="5cb42-179">For more information, see the procedure for staging aggregate measurements in the Entity store in [Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="5cb42-180">Následující klíčová agregovaná opatření jsou k dispozici přímo z entity řádky faktury a slouží jako základ obsahu.</span><span class="sxs-lookup"><span data-stu-id="5cb42-180">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="5cb42-181">Celek</span><span class="sxs-lookup"><span data-stu-id="5cb42-181">Entity</span></span>        | <span data-ttu-id="5cb42-182">Klíčová opatření agregace</span><span class="sxs-lookup"><span data-stu-id="5cb42-182">Key aggregate measurements</span></span> | <span data-ttu-id="5cb42-183">Zdroj dat</span><span class="sxs-lookup"><span data-stu-id="5cb42-183">Data source</span></span>                                 | <span data-ttu-id="5cb42-184">Pole</span><span class="sxs-lookup"><span data-stu-id="5cb42-184">Field</span></span>              | <span data-ttu-id="5cb42-185">popis</span><span class="sxs-lookup"><span data-stu-id="5cb42-185">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="5cb42-186">Řádky faktury</span><span class="sxs-lookup"><span data-stu-id="5cb42-186">Invoice lines</span></span> | <span data-ttu-id="5cb42-187">Nákup</span><span class="sxs-lookup"><span data-stu-id="5cb42-187">Purchase</span></span>                   | <span data-ttu-id="5cb42-188">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="5cb42-188">VendInvoiceTrans</span></span>                            | <span data-ttu-id="5cb42-189">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="5cb42-189">SUM(LineAmountMST)</span></span> | <span data-ttu-id="5cb42-190">Částka v zúčtovací měně.</span><span class="sxs-lookup"><span data-stu-id="5cb42-190">The amount in the accounting currency.</span></span> |

<span data-ttu-id="5cb42-191">V následující tabulce jsou uvedena klíčová opatření, která jsou vypočtena z entity řádky faktury.</span><span class="sxs-lookup"><span data-stu-id="5cb42-191">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="5cb42-192">Výměra</span><span class="sxs-lookup"><span data-stu-id="5cb42-192">Measure</span></span>               | <span data-ttu-id="5cb42-193">Výpočet</span><span class="sxs-lookup"><span data-stu-id="5cb42-193">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cb42-194">Aktuální rok nákupu</span><span class="sxs-lookup"><span data-stu-id="5cb42-194">Purchase current year</span></span> | <span data-ttu-id="5cb42-195">Aktuální rok nákupu = SUM (Řádky faktury\[Nákup\])</span><span class="sxs-lookup"><span data-stu-id="5cb42-195">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="5cb42-196">Minulý nákupní rok</span><span class="sxs-lookup"><span data-stu-id="5cb42-196">Purchase last year</span></span>    | <span data-ttu-id="5cb42-197">Minulý nákupní rok = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span><span class="sxs-lookup"><span data-stu-id="5cb42-197">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="5cb42-198">Meziroční růst nákupů</span><span class="sxs-lookup"><span data-stu-id="5cb42-198">YOY purchase growth</span></span>   | <span data-ttu-id="5cb42-199">Meziroční růst nákup = \[Aktuální nákupní rok\] – \[Minulý nákupní rok\]</span><span class="sxs-lookup"><span data-stu-id="5cb42-199">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="5cb42-200">Následující klíčové dimenze v obsahu se používají jako filtry k rozdělení agregovaných opatření, aby bylo možné dosažení většího rozlišení a získání hlubších analytických poznatků.</span><span class="sxs-lookup"><span data-stu-id="5cb42-200">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="5cb42-201">Celek</span><span class="sxs-lookup"><span data-stu-id="5cb42-201">Entity</span></span>                 | <span data-ttu-id="5cb42-202">Příklady atributů</span><span class="sxs-lookup"><span data-stu-id="5cb42-202">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="5cb42-203">Dodavatelé</span><span class="sxs-lookup"><span data-stu-id="5cb42-203">Vendors</span></span>                | <span data-ttu-id="5cb42-204">Skupiny dodavatelů, země nebo oblast dodavatele nebo název dodavatele</span><span class="sxs-lookup"><span data-stu-id="5cb42-204">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="5cb42-205">Produkty</span><span class="sxs-lookup"><span data-stu-id="5cb42-205">Products</span></span>               | <span data-ttu-id="5cb42-206">Číslo produktu, název produktu, název skupiny zboží</span><span class="sxs-lookup"><span data-stu-id="5cb42-206">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="5cb42-207">Kategorie zásobování</span><span class="sxs-lookup"><span data-stu-id="5cb42-207">Procurement categories</span></span> | <span data-ttu-id="5cb42-208">Kategorie zásobování, názvy kategorií zásobování</span><span class="sxs-lookup"><span data-stu-id="5cb42-208">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="5cb42-209">Právnické osoby</span><span class="sxs-lookup"><span data-stu-id="5cb42-209">Legal entities</span></span>         | <span data-ttu-id="5cb42-210">Jméno právnické osoby</span><span class="sxs-lookup"><span data-stu-id="5cb42-210">Legal entity name</span></span>                                     |
| <span data-ttu-id="5cb42-211">Data</span><span class="sxs-lookup"><span data-stu-id="5cb42-211">Dates</span></span>                  | <span data-ttu-id="5cb42-212">Data, Posun o rok</span><span class="sxs-lookup"><span data-stu-id="5cb42-212">Dates, Year offset</span></span>                                    |

<span data-ttu-id="5cb42-213">Ve výchozím nastavení obsah zobrazuje data pro aktuální kalendářní rok.</span><span class="sxs-lookup"><span data-stu-id="5cb42-213">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="5cb42-214">Můžete však změnit filtr dat v části filtrů sestavy.</span><span class="sxs-lookup"><span data-stu-id="5cb42-214">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="5cb42-215">Můžete také změnit filtr společnosti.</span><span class="sxs-lookup"><span data-stu-id="5cb42-215">You can also change the company filter.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]