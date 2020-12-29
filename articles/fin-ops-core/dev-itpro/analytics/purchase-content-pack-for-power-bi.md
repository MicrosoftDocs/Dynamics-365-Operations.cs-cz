---
title: Analýza obsahu výdajů na nákup v Power BI
description: Toto téma popisuje, co je součástí obsahu analýzy nákupu a výdajů v Power BI. Popisuje, jak získat přístup k sestavám, které jsou obsaženy v obsahu, a uvádí informace o datovém modelu a entitách, které se používají k vytváření obsahu.
author: FrankDahl
manager: AnnBe
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 3f556cf2e506c57e465c2a86485d2cdd4cf8b65e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680607"
---
# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="c5aef-104">Analýza obsahu výdajů na nákup v Power BI</span><span class="sxs-lookup"><span data-stu-id="c5aef-104">Purchase spend analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c5aef-105">Toto téma popisuje, co je součástí obsahu **analýzy nákupu a výdajů** v Microsoft Power BI.</span><span class="sxs-lookup"><span data-stu-id="c5aef-105">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="c5aef-106">Vysvětluje přístup k sestavám Power BI a poskytuje informace o datovém modelu a entitách, které byly použity k sestavení obsahu.</span><span class="sxs-lookup"><span data-stu-id="c5aef-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="c5aef-107">Přehled</span><span class="sxs-lookup"><span data-stu-id="c5aef-107">Overview</span></span>

<span data-ttu-id="c5aef-108">Obsah **Analýza nákupních výdajů** v Power BI byl vytvořen, aby pomohl nákupním manažerům a vedoucím pracovníkům, kteří odpovídají za rozpočty, sledovat nákupní výdaje.</span><span class="sxs-lookup"><span data-stu-id="c5aef-108">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep track of purchase spending.</span></span> <span data-ttu-id="c5aef-109">Manažeři mohou analyzovat nákupní výdaje následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="c5aef-109">Managers can analyze purchase spending in the following ways:</span></span>

- <span data-ttu-id="c5aef-110">Nákup k datu v daném roce (podle skupiny dodavatelů a jednotlivých dodavatelů, kategorie zásobování a jednotlivých produktů a umístění dodavatele)</span><span class="sxs-lookup"><span data-stu-id="c5aef-110">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
- <span data-ttu-id="c5aef-111">Rok přes rok nákupu změna (podle skupiny a zadávání zakázek kategorií dodavatele)</span><span class="sxs-lookup"><span data-stu-id="c5aef-111">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="c5aef-112">Obsah používá nákupní transakční data a poskytuje agregované zobrazení nákupní celopodnikových údajů a rozpis nákupních výdajů podle dodavatelů a produktů.</span><span class="sxs-lookup"><span data-stu-id="c5aef-112">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="c5aef-113">V sestavách jsou zvýrazněny změny nákupních výdajů v průběhu času.</span><span class="sxs-lookup"><span data-stu-id="c5aef-113">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="c5aef-114">Proto lze sestavy používat k upozornění manažerů na pozitivní a negativní trendy výdajů u jednotlivých dodavatelů a výrobků.</span><span class="sxs-lookup"><span data-stu-id="c5aef-114">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="c5aef-115">Grafy dále zobrazují nákupní výdaje pro zásobování různých kategorií a skupin dodavatelů.</span><span class="sxs-lookup"><span data-stu-id="c5aef-115">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="c5aef-116">Proto manažeři pro kategorie a regionální manažeři mohou tyto grafy používat k identifikaci změn v chování při výdajích.</span><span class="sxs-lookup"><span data-stu-id="c5aef-116">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="c5aef-117">Přístup k obsahu Power BI</span><span class="sxs-lookup"><span data-stu-id="c5aef-117">Accessing the Power BI content</span></span>
<span data-ttu-id="c5aef-118">Obsah **Analýza nákupu a výdajů** v Power BI se zobrazí na stránce **Analýza nákupu a výdajů** (**Zásobování a zdroje** \> **Dotazy a sestavy** \> **Analýza výkonu nákupu** \> **Analýza nákupu a výdajů**).</span><span class="sxs-lookup"><span data-stu-id="c5aef-118">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** \> **Inquiries and reports** \> **Purchase performance analysis** \> **Purchase and spend analysis**).</span></span>

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="c5aef-119">Metriky, které jsou součástí obsahu Power BI</span><span class="sxs-lookup"><span data-stu-id="c5aef-119">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="c5aef-120">**Balíček obsahu analýzy investic** Power BI do nákupu obsahuje sestavu, která obsahuje sadu metrik.</span><span class="sxs-lookup"><span data-stu-id="c5aef-120">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="c5aef-121">Tyto metriky jsou zobrazována jako grafy, dlaždice a tabulky.</span><span class="sxs-lookup"><span data-stu-id="c5aef-121">These metrics are visualized as charts, tiles, and tables.</span></span> 

<span data-ttu-id="c5aef-122">Následující sekce poskytují přehled vizualizací.</span><span class="sxs-lookup"><span data-stu-id="c5aef-122">The following sections provide an overview of the visualizations.</span></span>

### <a name="purchase-by-vendor-report-page"></a><span data-ttu-id="c5aef-123">Stránka sestavy nákupu podle dodavatele</span><span class="sxs-lookup"><span data-stu-id="c5aef-123">Purchase by vendor report page</span></span>
<span data-ttu-id="c5aef-124">**Grafy**</span><span class="sxs-lookup"><span data-stu-id="c5aef-124">**Charts**</span></span>
- <span data-ttu-id="c5aef-125">Prvních 10 dodavatelů podle nákupu (skládaný sloupcový graf)</span><span class="sxs-lookup"><span data-stu-id="c5aef-125">Top 10 vendors by purchase (stacked bar chart)</span></span>
- <span data-ttu-id="c5aef-126">Celkový nákup podle skupiny dodavatelů / země / name (výsečový graf)</span><span class="sxs-lookup"><span data-stu-id="c5aef-126">Total purchase by vendor group / country / name (pie chart)</span></span>
- <span data-ttu-id="c5aef-127">Nákup podle skupiny dodavatelů / země / název (sloupcový graf)</span><span class="sxs-lookup"><span data-stu-id="c5aef-127">Purchase by vendor group / country / name (column chart)</span></span>
- <span data-ttu-id="c5aef-128">Průměrný nákup podle skupiny dodavatelů / země / název (sloupcový graf)</span><span class="sxs-lookup"><span data-stu-id="c5aef-128">Average purchase by vendor group / country / name (column chart)</span></span>

<span data-ttu-id="c5aef-129">**Dlaždice**</span><span class="sxs-lookup"><span data-stu-id="c5aef-129">**Tiles**</span></span>
- <span data-ttu-id="c5aef-130">Celkový nákup</span><span class="sxs-lookup"><span data-stu-id="c5aef-130">Total purchase</span></span>
- <span data-ttu-id="c5aef-131">Meziroční růst nákupů</span><span class="sxs-lookup"><span data-stu-id="c5aef-131">YOY purchase growth</span></span>
- <span data-ttu-id="c5aef-132">Celkový počet dodavatelů</span><span class="sxs-lookup"><span data-stu-id="c5aef-132">Total # vendors</span></span>
- <span data-ttu-id="c5aef-133">Celkový počet aktivních dodavatelů</span><span class="sxs-lookup"><span data-stu-id="c5aef-133">Total # of active vendors</span></span>

<span data-ttu-id="c5aef-134">**Příklad**</span><span class="sxs-lookup"><span data-stu-id="c5aef-134">**Example**</span></span>
<img src="media/spend1.png" alt="Purchase by vendor">

### <a name="purchase-by-product-report-page"></a><span data-ttu-id="c5aef-135">Stránka sestavy nákupu podle produktu</span><span class="sxs-lookup"><span data-stu-id="c5aef-135">Purchase by product report page</span></span>

<span data-ttu-id="c5aef-136">**Grafy**</span><span class="sxs-lookup"><span data-stu-id="c5aef-136">**Charts**</span></span>
- <span data-ttu-id="c5aef-137">Nákup podle kategorie zásobování / název produktu (sloupcový graf)</span><span class="sxs-lookup"><span data-stu-id="c5aef-137">Purchase by procurement category / product name (column chart)</span></span>
- <span data-ttu-id="c5aef-138">Celkový nákup podle kategorie zásobování / název produktu (výsečový graf)</span><span class="sxs-lookup"><span data-stu-id="c5aef-138">Total purchase by procurement category / product name (pie chart)</span></span>
- <span data-ttu-id="c5aef-139">Prvních 10 produktů podle nákupu (skládaný sloupcový graf)</span><span class="sxs-lookup"><span data-stu-id="c5aef-139">Top 10 products by purchase (stacked bar chart)</span></span>

<span data-ttu-id="c5aef-140">**Dlaždice**</span><span class="sxs-lookup"><span data-stu-id="c5aef-140">**Tiles**</span></span>
- <span data-ttu-id="c5aef-141">Celkový počet produktů</span><span class="sxs-lookup"><span data-stu-id="c5aef-141">Total # of products</span></span></li>
- <span data-ttu-id="c5aef-142">Celkové procento aktivních produktů z celkového počtu produktů</span><span class="sxs-lookup"><span data-stu-id="c5aef-142">Total active products percentage of total # of products</span></span>
- <span data-ttu-id="c5aef-143">Počet účtování produktů pro 80 % nákupů</span><span class="sxs-lookup"><span data-stu-id="c5aef-143">Number of products accounting for 80% purchase</span></span>

<span data-ttu-id="c5aef-144">**Příklad**</span><span class="sxs-lookup"><span data-stu-id="c5aef-144">**Example**</span></span>


<img src="media/purchaseByProduct.png" alt="Purchase by Product">

### <a name="purchase-by-period-report-page"></a><span data-ttu-id="c5aef-145">Stránka sestavy nákupu podle období</span><span class="sxs-lookup"><span data-stu-id="c5aef-145">Purchase by period report page</span></span>
<span data-ttu-id="c5aef-146">Tato stránka zobrazuje nákupy v tomto a minulém roce a růst podle kategorie zásobování.</span><span class="sxs-lookup"><span data-stu-id="c5aef-146">This page shows purchases this year and last year, and growth by procurement category.</span></span>

<span data-ttu-id="c5aef-147">**Grafy**</span><span class="sxs-lookup"><span data-stu-id="c5aef-147">**Charts**</span></span> 
- <span data-ttu-id="c5aef-148">Nákup za měsíc / den (sloupcový graf)</span><span class="sxs-lookup"><span data-stu-id="c5aef-148">Purchase by month / day (column chart)</span></span>
- <span data-ttu-id="c5aef-149">Kumulativní mezirodčí nákupní odchylka (vodopádový graf)</span><span class="sxs-lookup"><span data-stu-id="c5aef-149">Cumulative purchase YOY variance (waterfall chart)</span></span>
- <span data-ttu-id="c5aef-150">Meziroční růst celkového nákupu (sloupcový graf)</span><span class="sxs-lookup"><span data-stu-id="c5aef-150">Total purchase YOY growth (column chart)</span></span>
- <span data-ttu-id="c5aef-151">Prohlášení o zadávání veřejných zakázek (matice)</span><span class="sxs-lookup"><span data-stu-id="c5aef-151">Procurement statement (matrix)</span></span>

<span data-ttu-id="c5aef-152">**Dlaždice**</span><span class="sxs-lookup"><span data-stu-id="c5aef-152">**Tiles**</span></span>
- <span data-ttu-id="c5aef-153">Meziroční růst nákupů</span><span class="sxs-lookup"><span data-stu-id="c5aef-153">YOY purchase growth</span></span>
- <span data-ttu-id="c5aef-154">Meziroční růst nákupů v %</span><span class="sxs-lookup"><span data-stu-id="c5aef-154">YOY purchase growth %</span></span>

<span data-ttu-id="c5aef-155">**Příklad**</span><span class="sxs-lookup"><span data-stu-id="c5aef-155">**Example**</span></span>
<img src="media/purchaseByPeriod.png" alt="Purchase by Period">

### <a name="purchase-by-vendor-location-report-page"></a><span data-ttu-id="c5aef-156">Stránka sestavy nákupu podle místa dodavatele</span><span class="sxs-lookup"><span data-stu-id="c5aef-156">Purchase by vendor location report page</span></span>

<span data-ttu-id="c5aef-157">**Grafy**</span><span class="sxs-lookup"><span data-stu-id="c5aef-157">**Charts**</span></span>
- <span data-ttu-id="c5aef-158">Nákup podle města</span><span class="sxs-lookup"><span data-stu-id="c5aef-158">Purchase by city</span></span>
- <span data-ttu-id="c5aef-159">Meziroční růst nákupů v %</span><span class="sxs-lookup"><span data-stu-id="c5aef-159">Purchase YOY growth %</span></span>
- <span data-ttu-id="c5aef-160">Nákup podle země</span><span class="sxs-lookup"><span data-stu-id="c5aef-160">Purchase by country</span></span>

<span data-ttu-id="c5aef-161">**Příklad**</span><span class="sxs-lookup"><span data-stu-id="c5aef-161">**Example**</span></span>
<img src="media/purchByVendorLocation.png" alt="Purchase by Vendor Location">

### <a name="purchase-spend-analysis-by-time-report-page"></a><span data-ttu-id="c5aef-162">Stránka sestavy analýzy výdajů při nákupu podle času</span><span class="sxs-lookup"><span data-stu-id="c5aef-162">Purchase spend analysis by time report page</span></span>

<span data-ttu-id="c5aef-163">**Grafy**</span><span class="sxs-lookup"><span data-stu-id="c5aef-163">**Charts**</span></span> 
- <span data-ttu-id="c5aef-164">Aktální rok nákupu podle měsíců / den (spojnicový graf)</span><span class="sxs-lookup"><span data-stu-id="c5aef-164">Purchase current year by month / day (line chart)</span></span>
- <span data-ttu-id="c5aef-165">Nákup za aktuální a předchozí rok (řádkový a sloupcový graf)</span><span class="sxs-lookup"><span data-stu-id="c5aef-165">Purchase current and last year (line and column chart)</span></span>

<span data-ttu-id="c5aef-166">**Příklad**</span><span class="sxs-lookup"><span data-stu-id="c5aef-166">**Example**</span></span>
<img src="media/PurchByTIme.png" alt="Purchase by Time">

### <a name="purchase-spend-analysis-by-vendor-report-page"></a><span data-ttu-id="c5aef-167">Stránka sestavy analýzy výdajů při nákupu podle dodavatele</span><span class="sxs-lookup"><span data-stu-id="c5aef-167">Purchase spend analysis by vendor report page</span></span>

<span data-ttu-id="c5aef-168">**Grafy**</span><span class="sxs-lookup"><span data-stu-id="c5aef-168">**Charts**</span></span> 
- <span data-ttu-id="c5aef-169">TOP 10 % nákupů dodavatele nákupní (trychtýřový graf)</span><span class="sxs-lookup"><span data-stu-id="c5aef-169">Top 10 vendor purchase % of purchase (funnel)</span></span>
- <span data-ttu-id="c5aef-170">Top 10 dodavatelů se zvýšenými investicemi meziročně</span><span class="sxs-lookup"><span data-stu-id="c5aef-170">Top 10 vendors with increased spending YOY</span></span>
- <span data-ttu-id="c5aef-171">Top 10 dodavatelů se sníženými investicemi meziročně</span><span class="sxs-lookup"><span data-stu-id="c5aef-171">Top 10 vendors with decreased spending YOY</span></span>

<span data-ttu-id="c5aef-172">**Příklad** 
</span><span class="sxs-lookup"><span data-stu-id="c5aef-172">**Example** 
</span></span><img src="media/PurchSpendAnalysisByVendor.png" alt="Purchase spend by vendor">


## <a name="data-model-and-entities"></a><span data-ttu-id="c5aef-173">Datový model a entity</span><span class="sxs-lookup"><span data-stu-id="c5aef-173">Data model and entities</span></span>
<span data-ttu-id="c5aef-174">Následující data se používají k naplnění stránek sestavy v obsahu **Analýza nákupu a výdajů** v Power BI.</span><span class="sxs-lookup"><span data-stu-id="c5aef-174">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="c5aef-175">Tato data jsou vyjádřena jako agregační měření, která jsou rozfázována v úložišti entit.</span><span class="sxs-lookup"><span data-stu-id="c5aef-175">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="c5aef-176">Úložiště entit je databáze Microsoft SQL Server, která je optimalizována pro analýzu.</span><span class="sxs-lookup"><span data-stu-id="c5aef-176">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="c5aef-177">Další informace naleznete v tématu [Integrace Power BI s úložištěm entit](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="c5aef-177">For more information, see [Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="c5aef-178">Souhrnná opatření v tomto balíčku obsahu jsou podmnožinou celkových opatření, která byla k dispozici v nákupní datové krychli v Microsoft Dynamics AX 2012 a Microsoft Dynamics AX 2012 R3.</span><span class="sxs-lookup"><span data-stu-id="c5aef-178">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="c5aef-179">Příprava fází agregovaných opatření krychle v úložišti Entity vyžaduje, aby bylo možné je nasadit.</span><span class="sxs-lookup"><span data-stu-id="c5aef-179">To stage the cube's aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="c5aef-180">Další informace získáte v postupu nastavování agregovaných opatření v úložišti entity v příspěvku v blogu [Integrace Power BI s úložištěm entity](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="c5aef-180">For more information, see the procedure for staging aggregate measurements in the Entity store in [Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="c5aef-181">Následující klíčová agregovaná opatření jsou k dispozici přímo z entity řádky faktury a slouží jako základ obsahu.</span><span class="sxs-lookup"><span data-stu-id="c5aef-181">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="c5aef-182">Celek</span><span class="sxs-lookup"><span data-stu-id="c5aef-182">Entity</span></span>        | <span data-ttu-id="c5aef-183">Klíčová opatření agregace</span><span class="sxs-lookup"><span data-stu-id="c5aef-183">Key aggregate measurements</span></span> | <span data-ttu-id="c5aef-184">Zdroj dat</span><span class="sxs-lookup"><span data-stu-id="c5aef-184">Data source</span></span>                                 | <span data-ttu-id="c5aef-185">Pole</span><span class="sxs-lookup"><span data-stu-id="c5aef-185">Field</span></span>              | <span data-ttu-id="c5aef-186">popis</span><span class="sxs-lookup"><span data-stu-id="c5aef-186">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="c5aef-187">Řádky faktury</span><span class="sxs-lookup"><span data-stu-id="c5aef-187">Invoice lines</span></span> | <span data-ttu-id="c5aef-188">Nákup</span><span class="sxs-lookup"><span data-stu-id="c5aef-188">Purchase</span></span>                   | <span data-ttu-id="c5aef-189">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="c5aef-189">VendInvoiceTrans</span></span>                            | <span data-ttu-id="c5aef-190">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="c5aef-190">SUM(LineAmountMST)</span></span> | <span data-ttu-id="c5aef-191">Částka v zúčtovací měně.</span><span class="sxs-lookup"><span data-stu-id="c5aef-191">The amount in the accounting currency.</span></span> |

<span data-ttu-id="c5aef-192">V následující tabulce jsou uvedena klíčová opatření, která jsou vypočtena z entity řádky faktury.</span><span class="sxs-lookup"><span data-stu-id="c5aef-192">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="c5aef-193">Výměra</span><span class="sxs-lookup"><span data-stu-id="c5aef-193">Measure</span></span>               | <span data-ttu-id="c5aef-194">Výpočet</span><span class="sxs-lookup"><span data-stu-id="c5aef-194">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5aef-195">Aktuální rok nákupu</span><span class="sxs-lookup"><span data-stu-id="c5aef-195">Purchase current year</span></span> | <span data-ttu-id="c5aef-196">Aktuální rok nákupu = SUM (Řádky faktury\[Nákup\])</span><span class="sxs-lookup"><span data-stu-id="c5aef-196">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="c5aef-197">Minulý nákupní rok</span><span class="sxs-lookup"><span data-stu-id="c5aef-197">Purchase last year</span></span>    | <span data-ttu-id="c5aef-198">Minulý nákupní rok = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span><span class="sxs-lookup"><span data-stu-id="c5aef-198">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="c5aef-199">Meziroční růst nákupů</span><span class="sxs-lookup"><span data-stu-id="c5aef-199">YOY purchase growth</span></span>   | <span data-ttu-id="c5aef-200">Meziroční růst nákup = \[Aktuální nákupní rok\] – \[Minulý nákupní rok\]</span><span class="sxs-lookup"><span data-stu-id="c5aef-200">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="c5aef-201">Následující klíčové dimenze v obsahu se používají jako filtry k rozdělení agregovaných opatření, aby bylo možné dosažení většího rozlišení a získání hlubších analytických poznatků.</span><span class="sxs-lookup"><span data-stu-id="c5aef-201">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="c5aef-202">Celek</span><span class="sxs-lookup"><span data-stu-id="c5aef-202">Entity</span></span>                 | <span data-ttu-id="c5aef-203">Příklady atributů</span><span class="sxs-lookup"><span data-stu-id="c5aef-203">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="c5aef-204">Dodavatelé</span><span class="sxs-lookup"><span data-stu-id="c5aef-204">Vendors</span></span>                | <span data-ttu-id="c5aef-205">Skupiny dodavatelů, země nebo oblast dodavatele nebo název dodavatele</span><span class="sxs-lookup"><span data-stu-id="c5aef-205">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="c5aef-206">Produkty</span><span class="sxs-lookup"><span data-stu-id="c5aef-206">Products</span></span>               | <span data-ttu-id="c5aef-207">Číslo produktu, název produktu, název skupiny zboží</span><span class="sxs-lookup"><span data-stu-id="c5aef-207">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="c5aef-208">Kategorie zásobování</span><span class="sxs-lookup"><span data-stu-id="c5aef-208">Procurement categories</span></span> | <span data-ttu-id="c5aef-209">Kategorie zásobování, názvy kategorií zásobování</span><span class="sxs-lookup"><span data-stu-id="c5aef-209">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="c5aef-210">Právnické osoby</span><span class="sxs-lookup"><span data-stu-id="c5aef-210">Legal entities</span></span>         | <span data-ttu-id="c5aef-211">Jméno právnické osoby</span><span class="sxs-lookup"><span data-stu-id="c5aef-211">Legal entity name</span></span>                                     |
| <span data-ttu-id="c5aef-212">Data</span><span class="sxs-lookup"><span data-stu-id="c5aef-212">Dates</span></span>                  | <span data-ttu-id="c5aef-213">Data, Posun o rok</span><span class="sxs-lookup"><span data-stu-id="c5aef-213">Dates, Year offset</span></span>                                    |

<span data-ttu-id="c5aef-214">Ve výchozím nastavení obsah zobrazuje data pro aktuální kalendářní rok.</span><span class="sxs-lookup"><span data-stu-id="c5aef-214">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="c5aef-215">Můžete však změnit filtr dat v části filtrů sestavy.</span><span class="sxs-lookup"><span data-stu-id="c5aef-215">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="c5aef-216">Můžete také změnit filtr společnosti.</span><span class="sxs-lookup"><span data-stu-id="c5aef-216">You can also change the company filter.</span></span>
