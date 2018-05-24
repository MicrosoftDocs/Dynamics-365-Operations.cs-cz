---
title: "Alternativní dodání"
description: "Zájemci o prodejní objednávky mohou využívat stránku Alternativy doručení k zjišťování alternativních možností plnění objednávky."
author: ChristianRytt
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesLineDeliveryDetails
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 271623
ms.assetid: 527f6084-44fe-41bb-924f-4386e926358a
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: crytt
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 855fdd0e57a7001628b715038785379d5a986789
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---

# <a name="delivery-alternatives"></a><span data-ttu-id="3116a-103">Alternativní dodání</span><span class="sxs-lookup"><span data-stu-id="3116a-103">Delivery alternatives</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3116a-104">Zájemci o prodejní objednávky mohou využívat stránku **Alternativy doručení** k zjišťování alternativních možností plnění objednávky.</span><span class="sxs-lookup"><span data-stu-id="3116a-104">Sales order takers can use the **Delivery alternatives** page to discover alternative order fulfillment options.</span></span>

<span data-ttu-id="3116a-105">Rozložení stránky **Alternativy doručení** poskytuje lepší přehled o všech alternativních možnostech.</span><span class="sxs-lookup"><span data-stu-id="3116a-105">The **Delivery alternatives** page layout gives an overview of all alternative options.</span></span> <span data-ttu-id="3116a-106">Umožňuje také zájemcům o objednávky nahlédnout na stávající společnost z hlediska příležitostí plnění.</span><span class="sxs-lookup"><span data-stu-id="3116a-106">It also lets order takers look beyond the current company for fulfillment opportunities.</span></span> <span data-ttu-id="3116a-107">Mají možnost zobrazit mezipodnikové příležitosti a příležitosti od externích dodavatelů.</span><span class="sxs-lookup"><span data-stu-id="3116a-107">They can now view both intercompany opportunities and opportunities from external vendors.</span></span> <span data-ttu-id="3116a-108">Díky třídění možností podle data dodání mohou zájemci o prodejní objednávky zobrazit inteligentní seznam alternativ doručení.</span><span class="sxs-lookup"><span data-stu-id="3116a-108">By sorting the options by delivery date, sales order takers can view an intelligent list of delivery alternatives.</span></span> <span data-ttu-id="3116a-109">Kromě toho jim parametry pomohou lépe řídit navrhované dodávky.</span><span class="sxs-lookup"><span data-stu-id="3116a-109">In addition, parameters help them better manage the suggested deliveries.</span></span> <span data-ttu-id="3116a-110">Vzhledem k tomu, že doba přepravy může ovlivnit data dodání, mohou zájemci o prodejní objednávku prozkoumat různé možnosti, které dopravci nabízejí.</span><span class="sxs-lookup"><span data-stu-id="3116a-110">Because transport time can affect delivery dates, sales order takers can explore the various transportation choices that carriers offer.</span></span> <span data-ttu-id="3116a-111">Vzhledem k tomu, že pro každý návrh se zobrazí podrobné informace, mohou pořizovatelé objednávky činit informovaná rozhodování přímo ze stránky **Alternativní dodání**.</span><span class="sxs-lookup"><span data-stu-id="3116a-111">Because detailed information is shown for each suggestion, order takers can make informed decisions directly from the **Delivery alternatives** page.</span></span>

## <a name="open-the-delivery-alternatives-page"></a><span data-ttu-id="3116a-112">Otevření stránky alternativní dodání</span><span class="sxs-lookup"><span data-stu-id="3116a-112">Open the Delivery alternatives page</span></span>
<span data-ttu-id="3116a-113">Stránku **Alternativní doručení** můžete otevřít z řádku prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="3116a-113">You can open the **Delivery alternatives** page from the sales order line.</span></span>

1.  <span data-ttu-id="3116a-114">Klikněte na **Produkty a dodávka** &gt; **Alternativní dodání**.</span><span class="sxs-lookup"><span data-stu-id="3116a-114">Click **Products and supply** &gt; **Delivery alternatives**.</span></span>
2.  <span data-ttu-id="3116a-115">Klekněte na **Podrobnosti řádku** &gt; **Doručení** &gt; **Alternativní doručení.**</span><span class="sxs-lookup"><span data-stu-id="3116a-115">Click **Line details** &gt; **Delivery** &gt; **Delivery alternatives.**</span></span>

<span data-ttu-id="3116a-116">Můžete také otevřít stránku **Alternativní doručení** tak, že otevřete pracovní prostor **Zpracování prodejní objednávky a dotaz** a potom kliknete na **Objednávky a oblíbené položky** &gt; **Řádky zpožděné objednávky** &gt; **Alternativy doručení** **Poznámka:** Stránku **Alternativní doručení** můžete otevřít pouze v případě, že jsou splněny následující podmínky:</span><span class="sxs-lookup"><span data-stu-id="3116a-116">You can also open the **Delivery alternatives** page by opening the **Sales order processing and inquiry** workspace, and then clicking **Orders and favorites** &gt; **Delayed order lines** &gt; **Delivery alternatives** **Note:** You can open the **Delivery alternatives** page only if both the following conditions are met:</span></span>

-   <span data-ttu-id="3116a-117">Jsou vyplněny všechny povinné informace o řádku prodeje.</span><span class="sxs-lookup"><span data-stu-id="3116a-117">All mandatory sales line information is filled in.</span></span>
-   <span data-ttu-id="3116a-118">Pole **Řízení data dodání** je nastaveno na jinou hodnotu než **Žádná**.</span><span class="sxs-lookup"><span data-stu-id="3116a-118">The **Delivery date control** field is set to a value other than **None**.</span></span>

## <a name="delivery-date-control-methods"></a><span data-ttu-id="3116a-119">Metody řízení data dodání</span><span class="sxs-lookup"><span data-stu-id="3116a-119">Delivery date control methods</span></span>
<span data-ttu-id="3116a-120">Metoda řízení data dodání určuje, jak systém stanovuje data dodání, jak se vypočítávají alternativy dodání a jaké informace se zobrazují.</span><span class="sxs-lookup"><span data-stu-id="3116a-120">The delivery date control method determines how the system establishes delivery dates, how delivery alternatives are calculated, and what information is shown.</span></span> <span data-ttu-id="3116a-121">Data dodání berou v úvahu kalendáře.</span><span class="sxs-lookup"><span data-stu-id="3116a-121">Note that delivery data control takes calendars into consideration.</span></span> <span data-ttu-id="3116a-122">Proto následující kalendáře mohou ovlivnit navrhované datum příjmu: kalendář skladu, kalendář dopravy, kalendář dodavatele a kalendář odběratele.</span><span class="sxs-lookup"><span data-stu-id="3116a-122">Therefore, the following calendars can affect the suggested receipt date: Warehouse calendar, Transport calendar, Vendor calendar, and Customer calendar.</span></span> <span data-ttu-id="3116a-123">V následující tabulce jsou popsány všechny metody řízení data dodání.</span><span class="sxs-lookup"><span data-stu-id="3116a-123">The following table describes each method for delivery date control.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3116a-124"><strong>Metoda</strong></span><span class="sxs-lookup"><span data-stu-id="3116a-124"><strong>Method</strong></span></span></td>
<td><span data-ttu-id="3116a-125"><strong>Popis</strong></span><span class="sxs-lookup"><span data-stu-id="3116a-125"><strong>Description</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3116a-126"><strong>Žádné</strong></span><span class="sxs-lookup"><span data-stu-id="3116a-126"><strong>None</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="3116a-127">Alternativní doručení pro řádky prodeje nejsou podporovány.</span><span class="sxs-lookup"><span data-stu-id="3116a-127">Delivery alternatives for sales lines aren&#39;t supported.</span></span> <span data-ttu-id="3116a-128">Tato možnost vypne řízení data dodání.</span><span class="sxs-lookup"><span data-stu-id="3116a-128">This option turns off delivery data control.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3116a-129"><strong>Doba realizace prodeje</strong></span><span class="sxs-lookup"><span data-stu-id="3116a-129"><strong>Sales lead time</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="3116a-130">Alternativní dodání se vypočítá podle předdefinované doby realizace prodeje.</span><span class="sxs-lookup"><span data-stu-id="3116a-130">Delivery alternatives are calculated based on the predefined sales lead time.</span></span> <span data-ttu-id="3116a-131">Dopravní dny se vypočítávají podle způsobu dodání.</span><span class="sxs-lookup"><span data-stu-id="3116a-131">The transport days are calculated based on the mode of delivery.</span></span></li>
<li><span data-ttu-id="3116a-132">Alternativní dodání zahrnuje sklady, které obsahuje zásoby na skladě a objednávek nabídky a poptávky.</span><span class="sxs-lookup"><span data-stu-id="3116a-132">Delivery alternatives include warehouses that have on-hand inventory, and supply/demand orders.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3116a-133"><strong>ATP</strong></span><span class="sxs-lookup"><span data-stu-id="3116a-133"><strong>ATP</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="3116a-134">Alternativní doručení se vypočítává na základě logiky Lze slíbit (ATP).</span><span class="sxs-lookup"><span data-stu-id="3116a-134">Delivery alternatives are calculated based on available to promise (ATP) logic.</span></span> <span data-ttu-id="3116a-135">Bere se v úvahu aktuální dostupnost a očekávaná budoucí dostupnost.</span><span class="sxs-lookup"><span data-stu-id="3116a-135">The current availability and expected future availability are considered.</span></span> <span data-ttu-id="3116a-136">Dopravní dny se vypočítávají podle způsobu dodání.</span><span class="sxs-lookup"><span data-stu-id="3116a-136">The transport days are calculated based on the mode of delivery.</span></span></li>
<li><span data-ttu-id="3116a-137">Alternativní dodání zahrnuje sklady, které obsahuje zásoby na skladě a objednávek nabídky a poptávky.</span><span class="sxs-lookup"><span data-stu-id="3116a-137">Delivery alternatives include warehouses that have on-hand inventory, and supply/demand orders.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3116a-138"><strong>ATP + rezerva výdeje</strong></span><span class="sxs-lookup"><span data-stu-id="3116a-138"><strong>ATP + Issue margin</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="3116a-139">Alternativní dodání se počítá jako pro metodu ATP, ale rezerva výdeje je zahrnuta ve výpočtu.</span><span class="sxs-lookup"><span data-stu-id="3116a-139">Delivery alternatives are calculated as for the ATP method, but the issue margin is included in the calculation.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3116a-140"><strong>CTP</strong></span><span class="sxs-lookup"><span data-stu-id="3116a-140"><strong>CTP</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="3116a-141">Alternativní doručení se vypočítává na základě logiky příslib na základě ověření dostupné kapacity (CTP).</span><span class="sxs-lookup"><span data-stu-id="3116a-141">Delivery alternatives are calculated based on the capable to promise (CTP) logic.</span></span> <span data-ttu-id="3116a-142">Rozpad MRP slouží k určení dostupnosti.</span><span class="sxs-lookup"><span data-stu-id="3116a-142">MRP explosion is used to determine availability.</span></span> <span data-ttu-id="3116a-143">Všimněte si, že alespoň CTP vyrovnává data dodání s prodejní dobou realizace.</span><span class="sxs-lookup"><span data-stu-id="3116a-143">Note that, at a minimum, CTP offsets delivery dates to the sales lead time.</span></span> <span data-ttu-id="3116a-144">Dopravní dny se vypočítávají podle způsobu dodání.</span><span class="sxs-lookup"><span data-stu-id="3116a-144">The transport days are calculated based on the mode of delivery.</span></span></li>
<li><span data-ttu-id="3116a-145">Alternativy dodání zahrnují návrhy pro tyto sklady:</span><span class="sxs-lookup"><span data-stu-id="3116a-145">Delivery alternatives include suggestions for the following warehouses:</span></span>
<ul>
<li><span data-ttu-id="3116a-146">Aktuální sklad</span><span class="sxs-lookup"><span data-stu-id="3116a-146">Current warehouse</span></span></li>
<li><span data-ttu-id="3116a-147">Výchozí sklad</span><span class="sxs-lookup"><span data-stu-id="3116a-147">Default warehouse</span></span></li>
<li><span data-ttu-id="3116a-148">Všechny sklady, které mají k dispozici množství na skladě</span><span class="sxs-lookup"><span data-stu-id="3116a-148">All warehouses that have available on-hand inventory</span></span></li>
<li><span data-ttu-id="3116a-149">Všechny sklady, které mají objednávky dodávky</span><span class="sxs-lookup"><span data-stu-id="3116a-149">All warehouses that have supply orders</span></span></li>
<li><span data-ttu-id="3116a-150">Všechny sklady, které mají aktivní verze kusovníku (BOM)</span><span class="sxs-lookup"><span data-stu-id="3116a-150">All warehouses that have active bill of materials (BOM) versions</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="view-information-about-delivery-alternatives"></a><span data-ttu-id="3116a-151">Zobrazení informací o alternativním dodání</span><span class="sxs-lookup"><span data-stu-id="3116a-151">View information about delivery alternatives</span></span>
<span data-ttu-id="3116a-152">Tento oddíl popisuje informace o alternativách dodání, které jsou k dispozici na všech kartách stránky **Alternativní dodání**.</span><span class="sxs-lookup"><span data-stu-id="3116a-152">This section describes the information about delivery alternatives that is available on each tab of the **Delivery alternatives** page.</span></span>

### <a name="products"></a><span data-ttu-id="3116a-153">Produkty</span><span class="sxs-lookup"><span data-stu-id="3116a-153">Products</span></span>

<span data-ttu-id="3116a-154">Na této kartě se zobrazuje souhrn produktu a podrobnosti o stávajícím řádku prodeje.</span><span class="sxs-lookup"><span data-stu-id="3116a-154">This tab shows a summary of the product and details of the current sales line.</span></span>

### <a name="delivery-alternatives"></a><span data-ttu-id="3116a-155">Alternativní dodání</span><span class="sxs-lookup"><span data-stu-id="3116a-155">Delivery alternatives</span></span>

<span data-ttu-id="3116a-156">Tato karta zobrazí seznam alternativních dodání seřazených podle data příjmu.</span><span class="sxs-lookup"><span data-stu-id="3116a-156">This tab shows a list of delivery alternatives that is sorted by receipt data.</span></span> <span data-ttu-id="3116a-157">Nad seznamem můžete vybrat možnosti, na kterých budou založeny návrhy.</span><span class="sxs-lookup"><span data-stu-id="3116a-157">Above the list, you can select which options to base the suggestions on.</span></span> <span data-ttu-id="3116a-158">Můžete také vybrat způsob dodání, který určuje dopravní dny.</span><span class="sxs-lookup"><span data-stu-id="3116a-158">You can also select the mode of delivery, which determines the transport days.</span></span> <span data-ttu-id="3116a-159">Existují tyto možnosti:</span><span class="sxs-lookup"><span data-stu-id="3116a-159">The following options are available:</span></span>

-   <span data-ttu-id="3116a-160">**Zahrnout ostatní varianty produktu** – tato možnost je k dispozici pro produkty, které mají varianty produktu.</span><span class="sxs-lookup"><span data-stu-id="3116a-160">**Include other product variants** - This option is available for products that have product variants.</span></span> <span data-ttu-id="3116a-161">Bude zahrnovat alternativní dodání pro ostatní varianty produktu.</span><span class="sxs-lookup"><span data-stu-id="3116a-161">It will include delivery alternatives for other variants of the product.</span></span> <span data-ttu-id="3116a-162">Tato možnost není k dispozici pro CTP.</span><span class="sxs-lookup"><span data-stu-id="3116a-162">This option isn't available for CTP.</span></span>
-   <span data-ttu-id="3116a-163">**Zahrnout částečné množství** – ve výchozím nastavení jsou zde pouze návrhy, které vyhovují plnému množství na řádku prodeje.</span><span class="sxs-lookup"><span data-stu-id="3116a-163">**Include partial quantity** - By default, only suggestions that fulfill the full quantity of the sales line are included.</span></span> <span data-ttu-id="3116a-164">Výběrem této možnosti zahrnete návrhy, které splňují pouze částečně řádku objednávky.</span><span class="sxs-lookup"><span data-stu-id="3116a-164">Select this option to include suggestions that only partially fulfill the order line.</span></span> <span data-ttu-id="3116a-165">Tato možnost je užitečná, když odběratel požaduje dřívější datum dodání a akceptuje částečné dodávky.</span><span class="sxs-lookup"><span data-stu-id="3116a-165">This option is useful when the customer requests an earlier delivery date and accepts partial delivery.</span></span>
-   <span data-ttu-id="3116a-166">**Zahrnout pozdější data** – ve výchozím nastavení pouze návrhy, které jsou lepší (dřívější) než jsou zobrazená aktuální data na řádku prodeje.</span><span class="sxs-lookup"><span data-stu-id="3116a-166">**Include later dates** - By default, only suggestions that are better (earlier) than the current dates on the sales line are shown.</span></span> <span data-ttu-id="3116a-167">Tuto možnost vyberte, chcete-li zahrnout pozdější data.</span><span class="sxs-lookup"><span data-stu-id="3116a-167">Select this option to include later dates.</span></span> <span data-ttu-id="3116a-168">Tato možnost může být užitečná v situacích, kdy mají prioritu jiné parametry než datum.</span><span class="sxs-lookup"><span data-stu-id="3116a-168">This option can be useful in situations where parameters other than the date have priority.</span></span> <span data-ttu-id="3116a-169">Může být například upřednostňovaný konkrétní dodavatel nebo sklad.</span><span class="sxs-lookup"><span data-stu-id="3116a-169">For example, a specific vendor or warehouse might be preferred.</span></span>
-   <span data-ttu-id="3116a-170">**Způsob dodání** - vyberte preferovaný způsob dodání pro optimalizaci dopravního času a nákladů.</span><span class="sxs-lookup"><span data-stu-id="3116a-170">**Mode of delivery** - Select the preferred mode of delivery to optimize transport time and cost.</span></span> <span data-ttu-id="3116a-171">Ihned uvidíte vliv na alternativní navrhované dodání.</span><span class="sxs-lookup"><span data-stu-id="3116a-171">You will immediately see the effect on the suggested delivery alternatives.</span></span> <span data-ttu-id="3116a-172">Je tedy snadné porovnat alternativy.</span><span class="sxs-lookup"><span data-stu-id="3116a-172">Therefore, it's easy to compare the alternatives.</span></span>
-   <span data-ttu-id="3116a-173">**Zahrnout zásobování** – Když je vybráno zásobování, mezi navrhované alternativy dodání patří možnosti nákupu od externích dodavatelů a jiných společností v organizaci (mezipodniková).</span><span class="sxs-lookup"><span data-stu-id="3116a-173">**Include procurement** - When procurement is selected, the suggested delivery alternatives include options to procure from both external vendors and other companies in the enterprise (intercompany).</span></span> <span data-ttu-id="3116a-174">Volba **Zahrnout zásobování** je podporovaná pro ATP a ATP + řízení data dodání marže.</span><span class="sxs-lookup"><span data-stu-id="3116a-174">The **Include procurement** option is supported for ATP and ATP + Issue margin delivery date control.</span></span> <span data-ttu-id="3116a-175">Jsou zahrnuty možnosti zásobování od výchozího nákupního dodavatele produktu a všech schválených dodavatelů pro produkt.</span><span class="sxs-lookup"><span data-stu-id="3116a-175">Procurement options from the default purchase vendor for the product and all approved vendors for the product are included.</span></span>
-   <span data-ttu-id="3116a-176">Pro externí dodavatele platí, že výpočet vychází z doby realizace nákupu.</span><span class="sxs-lookup"><span data-stu-id="3116a-176">For external vendors, the calculation is based on the purchase lead time.</span></span>
-   <span data-ttu-id="3116a-177">Pro mezipodnikové výpočty se bere v úvahu to, co je k dispozici ze zdrojové společnosti, na základě řízení data dodání ve zdrojové společnosti.</span><span class="sxs-lookup"><span data-stu-id="3116a-177">For intercompany, the calculation considers what is available from the sourcing company, based on delivery date control in the sourcing company.</span></span>
-   <span data-ttu-id="3116a-178">**Typ dodávky** (platí pro zásobování)</span><span class="sxs-lookup"><span data-stu-id="3116a-178">**Delivery type** (Relevant for procurement)</span></span>
    -   <span data-ttu-id="3116a-179">**Sklad** - produkty se odesílají ze zdrojového skladu pro pracoviště nebo skladu na řádku prodeje.</span><span class="sxs-lookup"><span data-stu-id="3116a-179">**Stock** - Products are shipped from the sourcing warehouse to the site/warehouse on the sales line.</span></span> <span data-ttu-id="3116a-180">Následně jsou odeslány z tohoto skladu odběrateli.</span><span class="sxs-lookup"><span data-stu-id="3116a-180">They are then shipped from that warehouse to the customer.</span></span>
    -   <span data-ttu-id="3116a-181">**Přímá dodávka** - produkty se odesílají přímo ze zdrojového skladu odběrateli.</span><span class="sxs-lookup"><span data-stu-id="3116a-181">**Direct delivery** - Products are shipped directly from the sourcing warehouse to the customer.</span></span>

### <a name="availability-information"></a><span data-ttu-id="3116a-182">Informace o dostupnosti</span><span class="sxs-lookup"><span data-stu-id="3116a-182">Availability information</span></span>

<span data-ttu-id="3116a-183">Informace na této kartě souvisí s vybranou alternativní řádkou dodávky.</span><span class="sxs-lookup"><span data-stu-id="3116a-183">Information on this tab is related to the delivery alternative line that is selected.</span></span> <span data-ttu-id="3116a-184">Zobrazují se následující informace v závislosti na řízení data dodání pro řádku prodeje:</span><span class="sxs-lookup"><span data-stu-id="3116a-184">The following information is shown, depending on the delivery date control for the sales line:</span></span>

-   <span data-ttu-id="3116a-185">**Doba realizace prodeje**</span><span class="sxs-lookup"><span data-stu-id="3116a-185">**Sales lead time**</span></span>
    -   <span data-ttu-id="3116a-186">**K dispozici dnes** - zobrazuje aktuální fyzické množství, fyzicky rezervované a dostupné fyzické zásoby.</span><span class="sxs-lookup"><span data-stu-id="3116a-186">**Available today** - Show the current physical on-hand, physical reserved, and available physical inventory.</span></span>
    -   <span data-ttu-id="3116a-187">**Parametry** - zobrazuje skladovou jednotku a dobu realizace prodejů.</span><span class="sxs-lookup"><span data-stu-id="3116a-187">**Parameters** - Show the inventory unit and sales lead time.</span></span>

-   <span data-ttu-id="3116a-188">**ATP a ATP + rezerva výdeje**</span><span class="sxs-lookup"><span data-stu-id="3116a-188">**ATP and ATP + Issue margin**</span></span>
    -   <span data-ttu-id="3116a-189">**K dispozici dnes** - zobrazuje aktuální fyzické množství, fyzicky rezervované a dostupné fyzické zásoby.</span><span class="sxs-lookup"><span data-stu-id="3116a-189">**Available today** - Show the current physical on-hand, physical reserved, and available physical inventory.</span></span>
    -   <span data-ttu-id="3116a-190">**Parametry** - zobrazuje skladovou jednotku a dobu realizace prodejů.</span><span class="sxs-lookup"><span data-stu-id="3116a-190">**Parameters** - Show the inventory unit and sales lead time.</span></span>
    -   <span data-ttu-id="3116a-191">**Budoucí dostupnost** - zobrazuje grafické znázornění aktuální a budoucí dostupnosti vybraného pracoviště a skladu pod možností **alternativní dodání**.</span><span class="sxs-lookup"><span data-stu-id="3116a-191">**Future availability** - Show a graphical representation of current and future availability for the selected site and warehouse under **Delivery alternatives**.</span></span> <span data-ttu-id="3116a-192">Po kliknutí na sloupce grafu se zobrazí podrobnější informace o budoucí dostupnosti produktu.</span><span class="sxs-lookup"><span data-stu-id="3116a-192">You can click the chart columns to see more detailed information about the future availability of the product.</span></span> <span data-ttu-id="3116a-193">Posuvník ukazuje seznam relevantních požadavků a objednávek dodávky v rámci ochranné doby ATP.</span><span class="sxs-lookup"><span data-stu-id="3116a-193">The slider shows a list of relevant demand and supply orders within the ATP time fence.</span></span>

-   <span data-ttu-id="3116a-194">**CTP**</span><span class="sxs-lookup"><span data-stu-id="3116a-194">**CTP**</span></span>
    -   <span data-ttu-id="3116a-195">**K dispozici dnes** - zobrazuje aktuální fyzické množství, fyzicky rezervované a dostupné fyzické zásoby.</span><span class="sxs-lookup"><span data-stu-id="3116a-195">**Available today** - Show the current physical on-hand, physical reserved, and available physical inventory.</span></span>
    -   <span data-ttu-id="3116a-196">**Parametry** - zobrazuje skladovou jednotku a dobu realizace prodejů.</span><span class="sxs-lookup"><span data-stu-id="3116a-196">**Parameters** - Show the inventory unit and sales lead time.</span></span>
    -   <span data-ttu-id="3116a-197">**Rozpad** - zobrazuje alternativní rozpad dodávky vybrané dodávky.</span><span class="sxs-lookup"><span data-stu-id="3116a-197">**Explosion** - Show a supply explosion of the selected delivery alternative.</span></span> <span data-ttu-id="3116a-198">Můžete vybrat **nastavení** pro změnu polí a dimenzí skladů, které se zobrazují v rozbalení.</span><span class="sxs-lookup"><span data-stu-id="3116a-198">You can use **Setup** to change the fields and inventory dimensions that are shown in the explosion.</span></span>

### <a name="impact-of-selected-alternative"></a><span data-ttu-id="3116a-199">Dopad vybrané alternativy</span><span class="sxs-lookup"><span data-stu-id="3116a-199">Impact of selected alternative</span></span>

<span data-ttu-id="3116a-200">Tato karta se podrobněji věnuje dopadu alternativy vybrané dodávky.</span><span class="sxs-lookup"><span data-stu-id="3116a-200">This tab highlights the impact of the selected delivery alternative.</span></span> <span data-ttu-id="3116a-201">Pokud klepnete na tlačítko **OK**, řádek prodeje se aktualizuje zvýrazněnými hodnotami ve VYBRANÝCH sloupcích.</span><span class="sxs-lookup"><span data-stu-id="3116a-201">If you click **OK**, the sales line is updated with the highlighted values in the SELECTED columns.</span></span> <span data-ttu-id="3116a-202">Všimněte si, že pokud je množství v alternativě pro vybranou dodávku menší než množství na řádku prodeje, vytvoření plánu dodávek a řádku objednávky je rozděleno do dvou řádků: jeden řádek pro vybrané množství a jeden řádek pro zbývající množství.</span><span class="sxs-lookup"><span data-stu-id="3116a-202">Note that, if the quantity on the selected delivery alternative is less than quantity on the sales line, a delivery schedule is created, and the order line is split into two lines: one line for the selected quantity and one line for the remaining quantity.</span></span> <span data-ttu-id="3116a-203">Můžete také aktualizovat obchodních řádek tak, aby odpovídal řádkům plánu a ovlivňoval tvorbu cen.</span><span class="sxs-lookup"><span data-stu-id="3116a-203">You can also update the commercial line so that it matches the schedule lines and affects the pricing.</span></span>

<a name="additional-resources"></a><span data-ttu-id="3116a-204">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="3116a-204">Additional resources</span></span>
--------

[<span data-ttu-id="3116a-205">Příslib objednávky</span><span class="sxs-lookup"><span data-stu-id="3116a-205">Order promising</span></span>](delivery-dates-available-promise-calculations.md)





