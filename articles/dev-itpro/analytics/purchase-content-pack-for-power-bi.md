---
title: "Analýza obsahu Power BI výdajů na nákup"
description: "Toto téma popisuje, co je součástí obsahu analýzy nákupu a výdajů v Power BI. Popisuje, jak získat přístup k sestavám, které jsou obsaženy v obsahu, a uvádí informace o datovém modelu a entitách, které se používají k vytváření obsahu."
author: FrankDahl
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 6485f36802fc4e327e223f47d65c4bdca11c1609
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="purchase-spend-analysis-power-bi-content"></a><span data-ttu-id="50dd3-104">Analýza obsahu Power BI výdajů na nákup</span><span class="sxs-lookup"><span data-stu-id="50dd3-104">Purchase spend analysis Power BI content</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="50dd3-105">Toto téma popisuje, co je součástí obsahu analýzy **nákupu a výdajů** v Power BI.</span><span class="sxs-lookup"><span data-stu-id="50dd3-105">This topic describes what is included in the **Purchase spend analysis** Microsoft Power BI content.</span></span> <span data-ttu-id="50dd3-106">Vysvětluje přístup k sestavám Power BI a poskytuje informace o datovém modelu a entitách, které jsou použity k sestavení obsahu.</span><span class="sxs-lookup"><span data-stu-id="50dd3-106">It explains how to access the Power BI reports, and provides information about the data model and entities that are used to build the content.</span></span>

## <a name="overview"></a><span data-ttu-id="50dd3-107">Přehled</span><span class="sxs-lookup"><span data-stu-id="50dd3-107">Overview</span></span>

<span data-ttu-id="50dd3-108">Obsah Power BI **Analýza nákupních výdajů** byl vytvořen na pomoc nákupním manažerům a vedoucím pracovníkům, kteří odpovídají za rozpočty, prohlížet nákupní výdaje.</span><span class="sxs-lookup"><span data-stu-id="50dd3-108">The **Purchase spend analysis** Power BI content was designed to help purchasing managers and managers who are responsible for budgets keep an eye on purchase spending.</span></span> <span data-ttu-id="50dd3-109">Manažeři mohou analyzovat nákupní výdaje následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="50dd3-109">Managers can analyze purchase spending in the following ways:</span></span>

-   <span data-ttu-id="50dd3-110">Nákup k datu v daném roce (podle skupiny dodavatelů a jednotlivých dodavatelů, kategorie zásobování a jednotlivých produktů a umístění dodavatele)</span><span class="sxs-lookup"><span data-stu-id="50dd3-110">Year-to-date purchase (by vendor group and individual vendors, procurement category and individual products, and vendor location)</span></span>
-   <span data-ttu-id="50dd3-111">Rok přes rok nákupu změna (podle skupiny a zadávání zakázek kategorií dodavatele)</span><span class="sxs-lookup"><span data-stu-id="50dd3-111">Year-over-year purchase change (by vendor group and procurement category)</span></span>

<span data-ttu-id="50dd3-112">Obsah používá nákupní transakční data a poskytuje agregované zobrazení nákupní celopodnikových údajů a rozpis nákupních výdajů podle dodavatelů a produktů.</span><span class="sxs-lookup"><span data-stu-id="50dd3-112">The content uses purchase transactional data, and provides both an aggregate view of the company-wide purchase figures and a breakdown of purchase spending by vendor and product.</span></span> <span data-ttu-id="50dd3-113">V sestavách jsou zvýrazněny změny nákupních výdajů v průběhu času.</span><span class="sxs-lookup"><span data-stu-id="50dd3-113">Reports highlight changes in purchase spending over time.</span></span> <span data-ttu-id="50dd3-114">Proto lze sestavy používat k upozornění manažerů na pozitivní a negativní trendy výdajů u jednotlivých dodavatelů a výrobků.</span><span class="sxs-lookup"><span data-stu-id="50dd3-114">Therefore, the reports can be used to alert managers about positive and negative spending trends for individual vendors and products.</span></span> <span data-ttu-id="50dd3-115">Grafy dále zobrazují nákupní výdaje pro zásobování různých kategorií a skupin dodavatelů.</span><span class="sxs-lookup"><span data-stu-id="50dd3-115">Additionally, charts show purchase spending for different procurement categories and vendor groups.</span></span> <span data-ttu-id="50dd3-116">Proto manažeři pro kategorie a regionální manažeři mohou tyto grafy používat k identifikaci změn v chování při výdajích.</span><span class="sxs-lookup"><span data-stu-id="50dd3-116">Therefore, category and regional managers can use the charts to help identify changes in spending behavior.</span></span>

## <a name="accessing-the-power-bi-content"></a><span data-ttu-id="50dd3-117">Přístup k obsahu Power BI</span><span class="sxs-lookup"><span data-stu-id="50dd3-117">Accessing the Power BI content</span></span>
<span data-ttu-id="50dd3-118">Pokud používáte aktualizaci Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (červenec 2017), obsah Power BI **Analýza nákupu a výdajů** se zobrazí na stránce **Analýza nákupu a výdajů** (**Nákup a zdroje** > **Dotazy a sestavy** > **Analýza výkonu nákupu** > **Analýza nákupu a investic**).</span><span class="sxs-lookup"><span data-stu-id="50dd3-118">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017), the **Purchase spend analysis** Power BI content is shown on the **Purchase and spend analysis** page (**Procurement and sourcing** > **Inquiries and reports** > **Purchase performance analysis** > **Purchase and spend analysis**).</span></span> 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a><span data-ttu-id="50dd3-119">Metriky, které jsou součástí obsahu Power BI</span><span class="sxs-lookup"><span data-stu-id="50dd3-119">Metrics that are included in the Power BI content</span></span>
<span data-ttu-id="50dd3-120">Obsahu Power BI **Analýza nákupu a výdajů** obsahuje sestavu, která obsahuje sadu metrik.</span><span class="sxs-lookup"><span data-stu-id="50dd3-120">The **Purchase spend analysis** Power BI content includes a report that consists of a set of metrics.</span></span> <span data-ttu-id="50dd3-121">Tyto metriky jsou zobrazována jako grafy, dlaždice a tabulky.</span><span class="sxs-lookup"><span data-stu-id="50dd3-121">These metrics are visualized as charts, tiles, and tables.</span></span> <span data-ttu-id="50dd3-122">Následující tabulka poskytuje přehled vizualizací.</span><span class="sxs-lookup"><span data-stu-id="50dd3-122">The following table provides an overview of the visualizations.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="50dd3-123">Stránka sestavy</span><span class="sxs-lookup"><span data-stu-id="50dd3-123">Report page</span></span></th>
<th><span data-ttu-id="50dd3-124">Grafy</span><span class="sxs-lookup"><span data-stu-id="50dd3-124">Charts</span></span></th>
<th><span data-ttu-id="50dd3-125">Dlaždice</span><span class="sxs-lookup"><span data-stu-id="50dd3-125">Tiles</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="50dd3-126">Nákup podle dodavatele</span><span class="sxs-lookup"><span data-stu-id="50dd3-126">Purchase by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="50dd3-127">Prvních 10 dodavatelů podle nákupu (skládaný sloupcový graf)</span><span class="sxs-lookup"><span data-stu-id="50dd3-127">Top 10 vendors by purchase (stacked bar chart)</span></span></li>
<li><span data-ttu-id="50dd3-128">Celkový nákup podle skupiny dodavatelů / země / name (výsečový graf)</span><span class="sxs-lookup"><span data-stu-id="50dd3-128">Total purchase by vendor group / country / name (pie chart)</span></span></li>
<li><span data-ttu-id="50dd3-129">Nákup podle skupiny dodavatelů / země / název (sloupcový graf)</span><span class="sxs-lookup"><span data-stu-id="50dd3-129">Purchase by vendor group / country / name (column chart)</span></span></li>
<li><span data-ttu-id="50dd3-130">Průměrný nákup podle skupiny dodavatelů / země / název (sloupcový graf)</span><span class="sxs-lookup"><span data-stu-id="50dd3-130">Average purchase by vendor group / country / name (column chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="50dd3-131">Celkový nákup</span><span class="sxs-lookup"><span data-stu-id="50dd3-131">Total purchase</span></span></li>
<li><span data-ttu-id="50dd3-132">Meziroční růst nákupů</span><span class="sxs-lookup"><span data-stu-id="50dd3-132">YOY purchase growth</span></span></li>
<li><span data-ttu-id="50dd3-133">Celkový počet dodavatelů</span><span class="sxs-lookup"><span data-stu-id="50dd3-133">Total # vendors</span></span></li>
<li><span data-ttu-id="50dd3-134">Celkový počet aktivních dodavatelů</span><span class="sxs-lookup"><span data-stu-id="50dd3-134">Total # of active vendors</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="50dd3-135">Nákup podle produktu</span><span class="sxs-lookup"><span data-stu-id="50dd3-135">Purchase by product</span></span></td>
<td><ul>
<li><span data-ttu-id="50dd3-136">Nákup podle kategorie zásobování / název produktu (sloupcový graf)</span><span class="sxs-lookup"><span data-stu-id="50dd3-136">Purchase by procurement category / product name (column chart)</span></span></li>
<li><span data-ttu-id="50dd3-137">Celkový nákup podle kategorie zásobování / název produktu (výsečový graf)</span><span class="sxs-lookup"><span data-stu-id="50dd3-137">Total purchase by procurement category / product name (pie chart)</span></span></li>
<li><span data-ttu-id="50dd3-138">Prvních 10 produktů podle nákupu (skládaný sloupcový graf)</span><span class="sxs-lookup"><span data-stu-id="50dd3-138">Top 10 products by purchase (stacked bar chart)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="50dd3-139">Celkový počet produktů</span><span class="sxs-lookup"><span data-stu-id="50dd3-139">Total # of products</span></span></li>
<li><span data-ttu-id="50dd3-140">Celkové procento aktivních produktů z celkového počtu produktů</span><span class="sxs-lookup"><span data-stu-id="50dd3-140">Total active products percentage of total # of products</span></span></li>
<li><span data-ttu-id="50dd3-141">Počet účtování produktů pro 80 % nákupů</span><span class="sxs-lookup"><span data-stu-id="50dd3-141">Number of products accounting for 80% purchase</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="50dd3-142">Nákup podle období*</span><span class="sxs-lookup"><span data-stu-id="50dd3-142">Purchase by period*</span></span></td>
<td><ul>
<li><span data-ttu-id="50dd3-143">Nákup za měsíc / den (sloupcový graf)</span><span class="sxs-lookup"><span data-stu-id="50dd3-143">Purchase by month / day (column chart)</span></span></li>
<li><span data-ttu-id="50dd3-144">Kumulativní mezirodčí nákupní odchylka (vodopádový graf)</span><span class="sxs-lookup"><span data-stu-id="50dd3-144">Cumulative purchase YOY variance (waterfall chart)</span></span></li>
<li><span data-ttu-id="50dd3-145">Meziroční růst celkového nákupu (sloupcový graf)</span><span class="sxs-lookup"><span data-stu-id="50dd3-145">Total purchase YOY growth (column chart)</span></span></li>
<li><span data-ttu-id="50dd3-146">Prohlášení o zadávání veřejných zakázek (matice)</span><span class="sxs-lookup"><span data-stu-id="50dd3-146">Procurement statement (matrix)</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="50dd3-147">Meziroční růst nákupů</span><span class="sxs-lookup"><span data-stu-id="50dd3-147">YOY purchase growth</span></span></li>
<li><span data-ttu-id="50dd3-148">Meziroční růst nákupů v %</span><span class="sxs-lookup"><span data-stu-id="50dd3-148">YOY purchase growth %</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="50dd3-149">Nákup podle místa dodavatele</span><span class="sxs-lookup"><span data-stu-id="50dd3-149">Purchase by vendor location</span></span></td>
<td><ul>
<li><span data-ttu-id="50dd3-150">Nákup podle města</span><span class="sxs-lookup"><span data-stu-id="50dd3-150">Purchase by city</span></span></li>
<li><span data-ttu-id="50dd3-151">Meziroční růst nákupů v %</span><span class="sxs-lookup"><span data-stu-id="50dd3-151">Purchase YOY growth %</span></span></li>
<li><span data-ttu-id="50dd3-152">Nákup podle země</span><span class="sxs-lookup"><span data-stu-id="50dd3-152">Purchase by country</span></span></li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="50dd3-153">Analýza výdajů při nákupu podle času</span><span class="sxs-lookup"><span data-stu-id="50dd3-153">Purchase spend analysis by time</span></span></td>
<td><ul>
<li><span data-ttu-id="50dd3-154">Aktální rok nákupu podle měsíců / den (spojnicový graf)</span><span class="sxs-lookup"><span data-stu-id="50dd3-154">Purchase current year by month / day (line chart)</span></span></li>
<li><span data-ttu-id="50dd3-155">Nákup za aktuální a předchozí rok (řádkový a sloupcový graf)</span><span class="sxs-lookup"><span data-stu-id="50dd3-155">Purchase current and last year (line and column chart)</span></span></li>
</ul></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="50dd3-156">Analýza výdajů při nákupu podle dodavatele</span><span class="sxs-lookup"><span data-stu-id="50dd3-156">Purchase spend analysis by vendor</span></span></td>
<td><ul>
<li><span data-ttu-id="50dd3-157">TOP 10 % nákupů dodavatele nákupní (trychtýřový graf)</span><span class="sxs-lookup"><span data-stu-id="50dd3-157">Top 10 vendor purchase % of purchase (funnel)</span></span></li>
<li><span data-ttu-id="50dd3-158">Top 10 dodavatelů se zvýšenými investicemi meziročně</span><span class="sxs-lookup"><span data-stu-id="50dd3-158">Top 10 vendors with increased spending YOY</span></span></li>
<li><span data-ttu-id="50dd3-159">Top 10 dodavatelů se sníženými investicemi meziročně</span><span class="sxs-lookup"><span data-stu-id="50dd3-159">Top 10 vendors with decreased spending YOY</span></span></li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

<span data-ttu-id="50dd3-160">\* Nákup v tomto a minulém roce a růst podle kategorie zásobování</span><span class="sxs-lookup"><span data-stu-id="50dd3-160">\* Purchase this year and last year, and growth by procurement category</span></span>

## <a name="extending-the-power-bi-content"></a><span data-ttu-id="50dd3-161">Rozšíření obsahu v Power BI</span><span class="sxs-lookup"><span data-stu-id="50dd3-161">Extending the Power BI content</span></span>
<span data-ttu-id="50dd3-162">Pomocí balíčků obsahu, které jsou k dispozici ve službě Microsoft Dynamics Lifecycle Services (LCS) můžete poskytovat skvělou analýzu osobám, které nejsou přihlášeny k aplikaci Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="50dd3-162">By using the content packs that are available in Microsoft Dynamics Lifecycle Services (LCS), you can provide great analytics to people who don't sign in to Microsoft Dynamics 365.</span></span> <span data-ttu-id="50dd3-163">Tyto balíčky obsahu můžete upravit tak, aby zahrnovaly jiné sestavy nebo vizuály, a potom publikovat balíčky obsahu na svého klienta Power BI.com pro analýzu.</span><span class="sxs-lookup"><span data-stu-id="50dd3-163">You can modify these content packs so that they include other reports or visuals, and then publish the content packs to your Power BI.com tenant for analysis.</span></span> 

<span data-ttu-id="50dd3-164">Obsah Power BI **Analýza nákupu a výdajů** naleznete v knihovně sdíleného majetku ve službě LCS.</span><span class="sxs-lookup"><span data-stu-id="50dd3-164">You can find the **Purchase spend analysis** Power BI content in the Shared assets library in LCS.</span></span> <span data-ttu-id="50dd3-165">Další informace o stažení obsahu a jeho implementaci ve vaší organizaci naleznete v tématu [Obsah Power BI v LCS od společnosti Microsoft a vašich partnerů](power-bi-content-microsoft-partners.md).</span><span class="sxs-lookup"><span data-stu-id="50dd3-165">For more information about how to download the content and implement it in your organization, see [Power BI content in LCS from Microsoft and your partners](power-bi-content-microsoft-partners.md).</span></span> <span data-ttu-id="50dd3-166">Pokud se chcete podívat na ukázku, jak implementovat obsah Power BI, najdete informace v tématu [Obsah Power BI od společnosti Microsoft a partnerů ve službě Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) pro Office Mix.</span><span class="sxs-lookup"><span data-stu-id="50dd3-166">To watch a demo that shows how to implement the Power BI content, see the [Power BI content from Microsoft and your partners in Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) Office Mix.</span></span>

<span data-ttu-id="50dd3-167">Nezapomeňte si stáhnout obsah **Analýza nákupu a výdajů**, který se vztahuje k vámi používané verzi aplikace Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="50dd3-167">Be sure to download the **Purchase spend analysis** content that applies to the version of Dynamics 365 that you're using.</span></span>

> [!NOTE]
> <span data-ttu-id="50dd3-168">Pokud používáte verzi Microsoft Dynamics 365 for Operations 1611, je předpokladem pro tento obsah Power BI článek znalostní báze KB 4011327.</span><span class="sxs-lookup"><span data-stu-id="50dd3-168">If you're using Microsoft Dynamics 365 for Operations version 1611, KB 4011327 is a prerequisite for this Power BI content.</span></span> <span data-ttu-id="50dd3-169">Po přihlášení ke službě LCS můžete přejít k článku znalostní báze zde: https://fix.lcs.dynamics.com/issue/results/?q=kb4011327.</span><span class="sxs-lookup"><span data-stu-id="50dd3-169">After you sign in to LCS, you can access the KB at https://fix.lcs.dynamics.com/issue/results/?q=kb4011327.</span></span>

## <a name="data-model-and-entities"></a><span data-ttu-id="50dd3-170">Datový model a entity</span><span class="sxs-lookup"><span data-stu-id="50dd3-170">Data model and entities</span></span>
<span data-ttu-id="50dd3-171">Následující data se používají k naplnění stránek sestavy v obsahu **Analýza nákupu a výdajů** v Power BI.</span><span class="sxs-lookup"><span data-stu-id="50dd3-171">The following data is used to fill the report pages in the **Purchase spend analysis** Power BI content.</span></span> <span data-ttu-id="50dd3-172">Tato data jsou vyjádřena jako agregační měření, která jsou rozfázována v úložišti entit.</span><span class="sxs-lookup"><span data-stu-id="50dd3-172">This data is represented as aggregate measurements that are staged in the Entity store.</span></span> <span data-ttu-id="50dd3-173">Úložiště entit je databáze Microsoft SQL Server, která je optimalizována pro analýzu.</span><span class="sxs-lookup"><span data-stu-id="50dd3-173">The Entity store is a Microsoft SQL Server database that is optimized for analytics.</span></span> <span data-ttu-id="50dd3-174">Další informace naleznete v tématu [Přehled integrace Power BI úložištěm entit](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="50dd3-174">For more information, see [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span>

<span data-ttu-id="50dd3-175">Souhrnná opatření v tomto obsahu jsou podmnožinou celkových opatření, která byla k dispozici v nákupní datové krychli v aplikaci Microsoft Dynamics AX 2012 a AX 2012 R3.</span><span class="sxs-lookup"><span data-stu-id="50dd3-175">The aggregate measurements in this content are the subset of aggregate measurements that were available in the Purchase Cube in Microsoft Dynamics AX 2012 and Microsoft Dynamics AX 2012 R3.</span></span> <span data-ttu-id="50dd3-176">Příprava fází agregovaných opatření v úložišti Entity vyžaduje, aby bylo možné je nasadit.</span><span class="sxs-lookup"><span data-stu-id="50dd3-176">To stage the cube’s aggregate measurements in the Entity store, you must make them deployable.</span></span> <span data-ttu-id="50dd3-177">Další informace získáte v postupu nastavování agregovaných opatření v úložišti entity v příspěvku v blogu [Přehled integrace Power BI s úložištěm entit](power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="50dd3-177">For more information, see the procedure for staging aggregate measurements in the Entity store in [Overview of Power BI integration with Entity store](power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="50dd3-178">Následující klíčová agregovaná opatření jsou k dispozici přímo z entity řádky faktury a slouží jako základ obsahu.</span><span class="sxs-lookup"><span data-stu-id="50dd3-178">The following key aggregate measurements are available directly from the Invoice lines entity and are used as the basis of the content.</span></span>

| <span data-ttu-id="50dd3-179">Celek</span><span class="sxs-lookup"><span data-stu-id="50dd3-179">Entity</span></span>        | <span data-ttu-id="50dd3-180">Klíčová opatření agregace</span><span class="sxs-lookup"><span data-stu-id="50dd3-180">Key aggregate measurements</span></span> | <span data-ttu-id="50dd3-181">Zdroj dat</span><span class="sxs-lookup"><span data-stu-id="50dd3-181">Data source</span></span>                                 | <span data-ttu-id="50dd3-182">Pole</span><span class="sxs-lookup"><span data-stu-id="50dd3-182">Field</span></span>              | <span data-ttu-id="50dd3-183">popis</span><span class="sxs-lookup"><span data-stu-id="50dd3-183">Description</span></span>                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| <span data-ttu-id="50dd3-184">Řádky faktury</span><span class="sxs-lookup"><span data-stu-id="50dd3-184">Invoice lines</span></span> | <span data-ttu-id="50dd3-185">Nákup</span><span class="sxs-lookup"><span data-stu-id="50dd3-185">Purchase</span></span>                   | <span data-ttu-id="50dd3-186">VendInvoiceTrans</span><span class="sxs-lookup"><span data-stu-id="50dd3-186">VendInvoiceTrans</span></span>                            | <span data-ttu-id="50dd3-187">SUM(LineAmountMST)</span><span class="sxs-lookup"><span data-stu-id="50dd3-187">SUM(LineAmountMST)</span></span> | <span data-ttu-id="50dd3-188">Částka v zúčtovací měně.</span><span class="sxs-lookup"><span data-stu-id="50dd3-188">The amount in the accounting currency.</span></span> |

<span data-ttu-id="50dd3-189">V následující tabulce jsou uvedena klíčová opatření, která jsou vypočtena z entity řádky faktury.</span><span class="sxs-lookup"><span data-stu-id="50dd3-189">The following table shows the key measurements in the content that are calculated from the Invoice lines entity.</span></span>

| <span data-ttu-id="50dd3-190">Výměra</span><span class="sxs-lookup"><span data-stu-id="50dd3-190">Measure</span></span>               | <span data-ttu-id="50dd3-191">Výpočet</span><span class="sxs-lookup"><span data-stu-id="50dd3-191">Calculation</span></span>                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50dd3-192">Aktuální rok nákupu</span><span class="sxs-lookup"><span data-stu-id="50dd3-192">Purchase current year</span></span> | <span data-ttu-id="50dd3-193">Aktuální rok nákupu = SUM (Řádky faktury\[Nákup\])</span><span class="sxs-lookup"><span data-stu-id="50dd3-193">Purchase current year = SUM('Invoice lines'\[Purchase\])</span></span>                                            |
| <span data-ttu-id="50dd3-194">Minulý nákupní rok</span><span class="sxs-lookup"><span data-stu-id="50dd3-194">Purchase last year</span></span>    | <span data-ttu-id="50dd3-195">Minulý nákupní rok = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span><span class="sxs-lookup"><span data-stu-id="50dd3-195">Purchase last year = CALCULATE(SUM('Invoice lines'\[Purchase\]), SAMEPERIODLASTYEAR(Dates\[Date\]))</span></span> |
| <span data-ttu-id="50dd3-196">Meziroční růst nákupů</span><span class="sxs-lookup"><span data-stu-id="50dd3-196">YOY purchase growth</span></span>   | <span data-ttu-id="50dd3-197">Meziroční růst nákup = \[Aktuální nákupní rok\] – \[Minulý nákupní rok\]</span><span class="sxs-lookup"><span data-stu-id="50dd3-197">YOY purchase growth = \[Purchase current year\] – \[Purchase last year\]</span></span>                            |

<span data-ttu-id="50dd3-198">Následující klíčové dimenze v obsahu se používají jako filtry k rozdělení agregovaných opatření, aby bylo možné dosažení většího rozlišení a získání hlubších analytických poznatků.</span><span class="sxs-lookup"><span data-stu-id="50dd3-198">The following key dimensions in the content are used as filters to slice the aggregate measurements, so that you can achieve more granularity and gain deeper analytical insights.</span></span>

| <span data-ttu-id="50dd3-199">Celek</span><span class="sxs-lookup"><span data-stu-id="50dd3-199">Entity</span></span>                 | <span data-ttu-id="50dd3-200">Příklady atributů</span><span class="sxs-lookup"><span data-stu-id="50dd3-200">Examples of attributes</span></span>                                |
|------------------------|-------------------------------------------------------|
| <span data-ttu-id="50dd3-201">Dodavatelé</span><span class="sxs-lookup"><span data-stu-id="50dd3-201">Vendors</span></span>                | <span data-ttu-id="50dd3-202">Skupiny dodavatelů, země nebo oblast dodavatele nebo název dodavatele</span><span class="sxs-lookup"><span data-stu-id="50dd3-202">Vendor groups, Vendor country or regions, Vendor name</span></span> |
| <span data-ttu-id="50dd3-203">Produkty</span><span class="sxs-lookup"><span data-stu-id="50dd3-203">Products</span></span>               | <span data-ttu-id="50dd3-204">Číslo produktu, název produktu, název skupiny zboží</span><span class="sxs-lookup"><span data-stu-id="50dd3-204">Product number, Product name, Item groups name</span></span>        |
| <span data-ttu-id="50dd3-205">Kategorie zásobování</span><span class="sxs-lookup"><span data-stu-id="50dd3-205">Procurement categories</span></span> | <span data-ttu-id="50dd3-206">Kategorie zásobování, názvy kategorií zásobování</span><span class="sxs-lookup"><span data-stu-id="50dd3-206">Procurement category, Procurement category names</span></span>      |
| <span data-ttu-id="50dd3-207">Právnické osoby</span><span class="sxs-lookup"><span data-stu-id="50dd3-207">Legal entities</span></span>         | <span data-ttu-id="50dd3-208">Jméno právnické osoby</span><span class="sxs-lookup"><span data-stu-id="50dd3-208">Legal entity name</span></span>                                     |
| <span data-ttu-id="50dd3-209">Data</span><span class="sxs-lookup"><span data-stu-id="50dd3-209">Dates</span></span>                  | <span data-ttu-id="50dd3-210">Data, Posun o rok</span><span class="sxs-lookup"><span data-stu-id="50dd3-210">Dates, Year offset</span></span>                                    |

<span data-ttu-id="50dd3-211">Ve výchozím nastavení obsah zobrazuje data pro aktuální kalendářní rok.</span><span class="sxs-lookup"><span data-stu-id="50dd3-211">By default, the content shows data for the current calendar year.</span></span> <span data-ttu-id="50dd3-212">Můžete však změnit filtr dat v části filtrů sestavy.</span><span class="sxs-lookup"><span data-stu-id="50dd3-212">However, you can change the date filter in the report filters section.</span></span> <span data-ttu-id="50dd3-213">Můžete také změnit filtr společnosti.</span><span class="sxs-lookup"><span data-stu-id="50dd3-213">You can also change the company filter.</span></span>

