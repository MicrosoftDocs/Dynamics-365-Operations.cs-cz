---
title: Analýza obsahu výdajů na nákup v Power BI
description: Toto téma popisuje, co je součástí obsahu analýzy nákupu a výdajů v Power BI. Popisuje, jak získat přístup k sestavám, které jsou obsaženy v obsahu, a uvádí informace o datovém modelu a entitách, které se používají k vytváření obsahu.
author: FrankDahl
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 069c4dc21959ab603ba6ca3da0ac68ef20325265
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "313835"
---
# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="c2b13-104">Analýza obsahu výdajů na nákup v Power BI</span><span class="sxs-lookup"><span data-stu-id="c2b13-104">Purchase spend analysis Power BI content</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c2b13-105">Toto téma popisuje, co je součástí obsahu **analýzy nákupu a výdajů** v Microsoft Power BI.</span><span class="sxs-lookup"><span data-stu-id="c2b13-105">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="c2b13-106">Vysvětluje přístup k sestavám Power BI a poskytuje informace o datovém modelu a entitách, které byly použity k sestavení obsahu.</span><span class="sxs-lookup"><span data-stu-id="c2b13-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="c2b13-107">Přehled</span><span class="sxs-lookup"><span data-stu-id="c2b13-107">Overview</span></span>

<span data-ttu-id="c2b13-108">Obsah **Analýza nákupních výdajů** v Power BI byl vytvořen na pomoc nákupním manažerům a vedoucím pracovníkům, kteří odpovídají za rozpočty, prohlížet nákupní výdaje.</span><span class="sxs-lookup"><span data-stu-id="c2b13-108">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep an eye on purchase spending.</span></span> <span data-ttu-id="c2b13-109">Manažeři mohou analyzovat nákupní výdaje následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="c2b13-109">Managers can analyze purchase spending in the following ways:</span></span>

- <span data-ttu-id="c2b13-110">Nákup k datu v daném roce (podle skupiny dodavatelů a jednotlivých dodavatelů, kategorie zásobování a jednotlivých produktů a umístění dodavatele)</span><span class="sxs-lookup"><span data-stu-id="c2b13-110">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
- <span data-ttu-id="c2b13-111">Rok přes rok nákupu změna (podle skupiny a zadávání zakázek kategorií dodavatele)</span><span class="sxs-lookup"><span data-stu-id="c2b13-111">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="c2b13-112">Obsah používá nákupní transakční data a poskytuje agregované zobrazení nákupní celopodnikových údajů a rozpis nákupních výdajů podle dodavatelů a produktů.</span><span class="sxs-lookup"><span data-stu-id="c2b13-112">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="c2b13-113">V sestavách jsou zvýrazněny změny nákupních výdajů v průběhu času.</span><span class="sxs-lookup"><span data-stu-id="c2b13-113">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="c2b13-114">Proto lze sestavy používat k upozornění manažerů na pozitivní a negativní trendy výdajů u jednotlivých dodavatelů a výrobků.</span><span class="sxs-lookup"><span data-stu-id="c2b13-114">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="c2b13-115">Grafy dále zobrazují nákupní výdaje pro zásobování různých kategorií a skupin dodavatelů.</span><span class="sxs-lookup"><span data-stu-id="c2b13-115">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="c2b13-116">Proto manažeři pro kategorie a regionální manažeři mohou tyto grafy používat k identifikaci změn v chování při výdajích.</span><span class="sxs-lookup"><span data-stu-id="c2b13-116">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="c2b13-117">Přístup k obsahu Power BI</span><span class="sxs-lookup"><span data-stu-id="c2b13-117">Accessing the Power BI content</span></span>
<span data-ttu-id="c2b13-118">Obsah **Analýza nákupu a výdajů** v Power BI se zobrazí na stránce **Analýza nákupu a výdajů** (**Zásobování a zdroje** \> **Dotazy a sestavy** \> **Analýza výkonu nákupu** \> **Analýza nákupu a výdajů**).</span><span class="sxs-lookup"><span data-stu-id="c2b13-118">The **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** \> **Inquiries and reports** \> **Purchase performance analysis** \> **Purchase and spend analysis**).</span></span>

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="c2b13-119">Metriky, které jsou součástí obsahu Power BI</span><span class="sxs-lookup"><span data-stu-id="c2b13-119">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="c2b13-120">**Balíček obsahu analýzy investic** Power BI do nákupu obsahuje sestavu, která obsahuje sadu metrik.</span><span class="sxs-lookup"><span data-stu-id="c2b13-120">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="c2b13-121">Tyto metriky jsou zobrazována jako grafy, dlaždice a tabulky.</span><span class="sxs-lookup"><span data-stu-id="c2b13-121">These metrics are visualized as charts, tiles, and tables.</span></span> <span data-ttu-id="c2b13-122">Následující tabulka poskytuje přehled vizualizací.</span><span class="sxs-lookup"><span data-stu-id="c2b13-122">The following table provides an overview of the visualizations.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="c2b13-123">Stránka sestavy</span><span class="sxs-lookup"><span data-stu-id="c2b13-123">Report page</span></span></th>
<th><span data-ttu-id="c2b13-124">Grafy</span><span class="sxs-lookup"><span data-stu-id="c2b13-124">Charts</span></span></th>
<th><span data-ttu-id="c2b13-125">Dlaždice</span><span class="sxs-lookup"><span data-stu-id="c2b13-125">Tiles</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="c2b13-126">Nákup podle dodavatele</span><span class="sxs-lookup"><span data-stu-id="c2b13-126">Purchase by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="c2b13-127">Prvních 10 dodavatelů podle nákupu (skládaný sloupcový graf)</span><span class="sxs-lookup"><span data-stu-id="c2b13-127">Top 10 vendors by purchase (stacked bar chart)</span></span></li>
<li><span data-ttu-id="c2b13-128">Celkový nákup podle skupiny dodavatelů / země / name (výsečový graf)</span><span class="sxs-lookup"><span data-stu-id="c2b13-128">Total purchase by vendor group / country / name (pie chart)</span></span></li>
<li><span data-ttu-id="c2b13-129">Nákup podle skupiny dodavatelů / země / název (sloupcový graf)</span><span class="sxs-lookup"><span data-stu-id="c2b13-129">Purchase by vendor group / country / name (column chart)</span></span></li>
<li><span data-ttu-id="c2b13-130">Průměrný nákup podle skupiny dodavatelů / země / název (sloupcový graf)</span><span class="sxs-lookup"><span data-stu-id="c2b13-130">Average purchase by vendor group / country / name (column chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="c2b13-131">Celkový nákup</span><span class="sxs-lookup"><span data-stu-id="c2b13-131">Total purchase</span></span></li>
<li><span data-ttu-id="c2b13-132">Meziroční růst nákupů</span><span class="sxs-lookup"><span data-stu-id="c2b13-132">YOY purchase growth</span></span></li>
<li><span data-ttu-id="c2b13-133">Celkový počet dodavatelů</span><span class="sxs-lookup"><span data-stu-id="c2b13-133">Total # vendors</span></span></li>
<li><span data-ttu-id="c2b13-134">Celkový počet aktivních dodavatelů</span><span class="sxs-lookup"><span data-stu-id="c2b13-134">Total # of active vendors</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="c2b13-135">Nákup podle produktu</span><span class="sxs-lookup"><span data-stu-id="c2b13-135">Purchase by product</span></span></td>
<td><ul>
<li><span data-ttu-id="c2b13-136">Nákup podle kategorie zásobování / název produktu (sloupcový graf)</span><span class="sxs-lookup"><span data-stu-id="c2b13-136">Purchase by procurement category / product name (column chart)</span></span></li>
<li><span data-ttu-id="c2b13-137">Celkový nákup podle kategorie zásobování / název produktu (výsečový graf)</span><span class="sxs-lookup"><span data-stu-id="c2b13-137">Total purchase by procurement category / product name (pie chart)</span></span></li>
<li><span data-ttu-id="c2b13-138">Prvních 10 produktů podle nákupu (skládaný sloupcový graf)</span><span class="sxs-lookup"><span data-stu-id="c2b13-138">Top 10 products by purchase (stacked bar chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="c2b13-139">Celkový počet produktů</span><span class="sxs-lookup"><span data-stu-id="c2b13-139">Total # of products</span></span></li>
<li><span data-ttu-id="c2b13-140">Celkové procento aktivních produktů z celkového počtu produktů</span><span class="sxs-lookup"><span data-stu-id="c2b13-140">Total active products percentage of total # of products</span></span></li>
<li><span data-ttu-id="c2b13-141">Počet účtování produktů pro 80 % nákupů</span><span class="sxs-lookup"><span data-stu-id="c2b13-141">Number of products accounting for 80% purchase</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="c2b13-142">Nákup podle období\*</span><span class="sxs-lookup"><span data-stu-id="c2b13-142">Purchase by period\*</span></span></td>
<td><ul>
<li><span data-ttu-id="c2b13-143">Nákup za měsíc / den (sloupcový graf)</span><span class="sxs-lookup"><span data-stu-id="c2b13-143">Purchase by month / day (column chart)</span></span></li>
<li><span data-ttu-id="c2b13-144">Kumulativní mezirodčí nákupní odchylka (vodopádový graf)</span><span class="sxs-lookup"><span data-stu-id="c2b13-144">Cumulative purchase YOY variance (waterfall chart)</span></span></li>
<li><span data-ttu-id="c2b13-145">Meziroční růst celkového nákupu (sloupcový graf)</span><span class="sxs-lookup"><span data-stu-id="c2b13-145">Total purchase YOY growth (column chart)</span></span></li>
<li><span data-ttu-id="c2b13-146">Prohlášení o zadávání veřejných zakázek (matice)</span><span class="sxs-lookup"><span data-stu-id="c2b13-146">Procurement statement (matrix)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="c2b13-147">Meziroční růst nákupů</span><span class="sxs-lookup"><span data-stu-id="c2b13-147">YOY purchase growth</span></span></li>
<li><span data-ttu-id="c2b13-148">Meziroční růst nákupů v %</span><span class="sxs-lookup"><span data-stu-id="c2b13-148">YOY purchase growth %</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="c2b13-149">Nákup podle místa dodavatele</span><span class="sxs-lookup"><span data-stu-id="c2b13-149">Purchase by vendor location</span></span></td>
<td><ul>
<li><span data-ttu-id="c2b13-150">Nákup podle města</span><span class="sxs-lookup"><span data-stu-id="c2b13-150">Purchase by city</span></span></li>
<li><span data-ttu-id="c2b13-151">Meziroční růst nákupů v %</span><span class="sxs-lookup"><span data-stu-id="c2b13-151">Purchase YOY growth %</span></span></li>
<li><span data-ttu-id="c2b13-152">Nákup podle země</span><span class="sxs-lookup"><span data-stu-id="c2b13-152">Purchase by country</span></span></li>
</ul></td>
<td></td>
</tr>
<tr>
<td><span data-ttu-id="c2b13-153">Analýza výdajů při nákupu podle času</span><span class="sxs-lookup"><span data-stu-id="c2b13-153">Purchase spend analysis by time</span></span></td>
<td><ul>
<li><span data-ttu-id="c2b13-154">Aktální rok nákupu podle měsíců / den (spojnicový graf)</span><span class="sxs-lookup"><span data-stu-id="c2b13-154">Purchase current year by month / day (line chart)</span></span></li>
<li><span data-ttu-id="c2b13-155">Nákup za aktuální a předchozí rok (řádkový a sloupcový graf)</span><span class="sxs-lookup"><span data-stu-id="c2b13-155">Purchase current and last year (line and column chart)</span></span></li>
</ul></td>
<td></td>
</tr>
<tr>
<td><span data-ttu-id="c2b13-156">Analýza výdajů při nákupu podle dodavatele</span><span class="sxs-lookup"><span data-stu-id="c2b13-156">Purchase spend analysis by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="c2b13-157">TOP 10 % nákupů dodavatele nákupní (trychtýřový graf)</span><span class="sxs-lookup"><span data-stu-id="c2b13-157">Top 10 vendor purchase % of purchase (funnel)</span></span></li>
<li><span data-ttu-id="c2b13-158">Top 10 dodavatelů se zvýšenými investicemi meziročně</span><span class="sxs-lookup"><span data-stu-id="c2b13-158">Top 10 vendors with increased spending YOY</span></span></li>
<li><span data-ttu-id="c2b13-159">Top 10 dodavatelů se sníženými investicemi meziročně</span><span class="sxs-lookup"><span data-stu-id="c2b13-159">Top 10 vendors with decreased spending YOY</span></span></li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

<span data-ttu-id="c2b13-160">\* Nákup v tomto a minulém roce a růst podle kategorie zásobování</span><span class="sxs-lookup"><span data-stu-id="c2b13-160">\* Purchase this year and last year, and growth by procurement category</span></span>

## <a name="data-model-and-entities"></a><span data-ttu-id="c2b13-161">Datový model a entity</span><span class="sxs-lookup"><span data-stu-id="c2b13-161">Data model and entities</span></span>
<span data-ttu-id="c2b13-162">Následující data se používají k naplnění stránek sestavy v obsahu **Analýza nákupu a výdajů** v Power BI.</span><span class="sxs-lookup"><span data-stu-id="c2b13-162">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="c2b13-163">Tato data jsou vyjádřena jako agregační měření, která jsou rozfázována v úložišti entit.</span><span class="sxs-lookup"><span data-stu-id="c2b13-163">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="c2b13-164">Úložiště entit je databáze Microsoft SQL Server, která je optimalizována pro analýzu.</span><span class="sxs-lookup"><span data-stu-id="c2b13-164">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="c2b13-165">Další informace naleznete v tématu [Přehled integrace Power BI s úložištěm entit](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="c2b13-165">For more information, see [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="c2b13-166">Souhrnná opatření v tomto balíčku obsahu jsou podmnožinou celkových opatření, která byla k dispozici v nákupní datové krychli v Microsoft Dynamics AX 2012 a Microsoft Dynamics AX 2012 R3.</span><span class="sxs-lookup"><span data-stu-id="c2b13-166">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="c2b13-167">Příprava fází agregovaných opatření krychle v úložišti Entity vyžaduje, aby bylo možné je nasadit.</span><span class="sxs-lookup"><span data-stu-id="c2b13-167">To stage the cube's aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="c2b13-168">Další informace získáte v postupu nastavování agregovaných opatření v úložišti entity v příspěvku v blogu [Přehled integrace Power BI s úložištěm entit](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="c2b13-168">For more information, see the procedure for staging aggregate measurements in the Entity store in [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="c2b13-169">Následující klíčová agregovaná opatření jsou k dispozici přímo z entity řádky faktury a slouží jako základ obsahu.</span><span class="sxs-lookup"><span data-stu-id="c2b13-169">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="c2b13-170">Celek</span><span class="sxs-lookup"><span data-stu-id="c2b13-170">Entity</span></span>        | <span data-ttu-id="c2b13-171">Klíčová opatření agregace</span><span class="sxs-lookup"><span data-stu-id="c2b13-171">Key aggregate measurements</span></span> | <span data-ttu-id="c2b13-172">Zdroj dat</span><span class="sxs-lookup"><span data-stu-id="c2b13-172">Data source</span></span>                                 | <span data-ttu-id="c2b13-173">Pole</span><span class="sxs-lookup"><span data-stu-id="c2b13-173">Field</span></span>              | <span data-ttu-id="c2b13-174">popis</span><span class="sxs-lookup"><span data-stu-id="c2b13-174">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="c2b13-175">Řádky faktury</span><span class="sxs-lookup"><span data-stu-id="c2b13-175">Invoice lines</span></span> | <span data-ttu-id="c2b13-176">Nákup</span><span class="sxs-lookup"><span data-stu-id="c2b13-176">Purchase</span></span>                   | <span data-ttu-id="c2b13-177">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="c2b13-177">VendInvoiceTrans</span></span>                            | <span data-ttu-id="c2b13-178">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="c2b13-178">SUM(LineAmountMST)</span></span> | <span data-ttu-id="c2b13-179">Částka v zúčtovací měně.</span><span class="sxs-lookup"><span data-stu-id="c2b13-179">The amount in the accounting currency.</span></span> |

<span data-ttu-id="c2b13-180">V následující tabulce jsou uvedena klíčová opatření, která jsou vypočtena z entity řádky faktury.</span><span class="sxs-lookup"><span data-stu-id="c2b13-180">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="c2b13-181">Výměra</span><span class="sxs-lookup"><span data-stu-id="c2b13-181">Measure</span></span>               | <span data-ttu-id="c2b13-182">Výpočet</span><span class="sxs-lookup"><span data-stu-id="c2b13-182">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2b13-183">Aktuální rok nákupu</span><span class="sxs-lookup"><span data-stu-id="c2b13-183">Purchase current year</span></span> | <span data-ttu-id="c2b13-184">Aktuální rok nákupu = SUM (Řádky faktury\[Nákup\])</span><span class="sxs-lookup"><span data-stu-id="c2b13-184">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="c2b13-185">Minulý nákupní rok</span><span class="sxs-lookup"><span data-stu-id="c2b13-185">Purchase last year</span></span>    | <span data-ttu-id="c2b13-186">Minulý nákupní rok = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span><span class="sxs-lookup"><span data-stu-id="c2b13-186">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="c2b13-187">Meziroční růst nákupů</span><span class="sxs-lookup"><span data-stu-id="c2b13-187">YOY purchase growth</span></span>   | <span data-ttu-id="c2b13-188">Meziroční růst nákup = \[Aktuální nákupní rok\] – \[Minulý nákupní rok\]</span><span class="sxs-lookup"><span data-stu-id="c2b13-188">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="c2b13-189">Následující klíčové dimenze v obsahu se používají jako filtry k rozdělení agregovaných opatření, aby bylo možné dosažení většího rozlišení a získání hlubších analytických poznatků.</span><span class="sxs-lookup"><span data-stu-id="c2b13-189">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="c2b13-190">Celek</span><span class="sxs-lookup"><span data-stu-id="c2b13-190">Entity</span></span>                 | <span data-ttu-id="c2b13-191">Příklady atributů</span><span class="sxs-lookup"><span data-stu-id="c2b13-191">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="c2b13-192">Dodavatelé</span><span class="sxs-lookup"><span data-stu-id="c2b13-192">Vendors</span></span>                | <span data-ttu-id="c2b13-193">Skupiny dodavatelů, země nebo oblast dodavatele nebo název dodavatele</span><span class="sxs-lookup"><span data-stu-id="c2b13-193">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="c2b13-194">Produkty</span><span class="sxs-lookup"><span data-stu-id="c2b13-194">Products</span></span>               | <span data-ttu-id="c2b13-195">Číslo produktu, název produktu, název skupiny zboží</span><span class="sxs-lookup"><span data-stu-id="c2b13-195">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="c2b13-196">Kategorie zásobování</span><span class="sxs-lookup"><span data-stu-id="c2b13-196">Procurement categories</span></span> | <span data-ttu-id="c2b13-197">Kategorie zásobování, názvy kategorií zásobování</span><span class="sxs-lookup"><span data-stu-id="c2b13-197">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="c2b13-198">Právnické osoby</span><span class="sxs-lookup"><span data-stu-id="c2b13-198">Legal entities</span></span>         | <span data-ttu-id="c2b13-199">Jméno právnické osoby</span><span class="sxs-lookup"><span data-stu-id="c2b13-199">Legal entity name</span></span>                                     |
| <span data-ttu-id="c2b13-200">Data</span><span class="sxs-lookup"><span data-stu-id="c2b13-200">Dates</span></span>                  | <span data-ttu-id="c2b13-201">Data, Posun o rok</span><span class="sxs-lookup"><span data-stu-id="c2b13-201">Dates, Year offset</span></span>                                    |

<span data-ttu-id="c2b13-202">Ve výchozím nastavení obsah zobrazuje data pro aktuální kalendářní rok.</span><span class="sxs-lookup"><span data-stu-id="c2b13-202">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="c2b13-203">Můžete však změnit filtr dat v části filtrů sestavy.</span><span class="sxs-lookup"><span data-stu-id="c2b13-203">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="c2b13-204">Můžete také změnit filtr společnosti.</span><span class="sxs-lookup"><span data-stu-id="c2b13-204">You can also change the company filter.</span></span>
