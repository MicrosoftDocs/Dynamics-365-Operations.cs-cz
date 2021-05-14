---
title: Přiřazení kvality
description: Toto téma popisuje, jak můžete použít přidružení kvality v Microsoft Dynamics 365 Supply Chain Management k automatickému generování objednávek kvality, které souvisejí s vašimi procesy prodeje, nákupu a výroby.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestAssociationTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2020-06-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0f46f09dc9b67cfb04d0320a071c2c739266af58
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956576"
---
# <a name="quality-associations"></a><span data-ttu-id="d4cca-103">Přiřazení kvality</span><span class="sxs-lookup"><span data-stu-id="d4cca-103">Quality associations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d4cca-104">Toto téma popisuje, jak můžete použít přidružení kvality v Microsoft Dynamics 365 Supply Chain Management k automatickému generování objednávek kvality, které souvisejí s vašimi procesy prodeje, nákupu a výroby.</span><span class="sxs-lookup"><span data-stu-id="d4cca-104">This topic describes how you can use quality associations in Microsoft Dynamics 365 Supply Chain Management to automatically generate quality orders that are related to your sales, purchase, and production processes.</span></span>

<span data-ttu-id="d4cca-105">Přidružení kvality určuje pro vygenerovanou objednávku kvality tyto informace:</span><span class="sxs-lookup"><span data-stu-id="d4cca-105">A quality association defines all the following information for a quality order that is generated:</span></span>

- <span data-ttu-id="d4cca-106">Událost transakce</span><span class="sxs-lookup"><span data-stu-id="d4cca-106">The transaction event</span></span>
- <span data-ttu-id="d4cca-107">Sada testů, které je nutné u položky vykonat</span><span class="sxs-lookup"><span data-stu-id="d4cca-107">The set of tests that must be performed on the items</span></span>
- <span data-ttu-id="d4cca-108">Přijatelná úroveň kvality (AQL)</span><span class="sxs-lookup"><span data-stu-id="d4cca-108">The acceptable quality level (AQL)</span></span>
- <span data-ttu-id="d4cca-109">Plán vzorkování</span><span class="sxs-lookup"><span data-stu-id="d4cca-109">The sampling plan</span></span>

<span data-ttu-id="d4cca-110">Přiřazení kvality je nutné definovat pro každou variantu obchodního procesu, který vyžaduje automatické generování objednávky kvality.</span><span class="sxs-lookup"><span data-stu-id="d4cca-110">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="d4cca-111">Objednávky kvality lze generovat například v obchodních procesech pro nákupní objednávky, karanténní příkazy, prodejní objednávky a výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="d4cca-111">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="d4cca-112">Práce s přidruženími kvality</span><span class="sxs-lookup"><span data-stu-id="d4cca-112">Working with quality associations</span></span>

<span data-ttu-id="d4cca-113">Obchodní proces, který používá přidružení kvality, může být přiřazen k různým zdrojovým dokumentům, jako například k nákupním objednávkám, prodejním objednávkám nebo výrobním zakázkám.</span><span class="sxs-lookup"><span data-stu-id="d4cca-113">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="d4cca-114">Každý záznam o přidružení kvality určuje sadu testů, přijatelnou úroveň kvality a plán vzorkování, které platí pro vygenerované objednávky kvality.</span><span class="sxs-lookup"><span data-stu-id="d4cca-114">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="d4cca-115">Je nutné definovat záznam o přidružení kvality pro každou variantu v obchodním procesu.</span><span class="sxs-lookup"><span data-stu-id="d4cca-115">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="d4cca-116">Můžete například nastavit přidružení kvality, které vygeneruje objednávku kvality při aktualizaci příjemky produktu nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="d4cca-116">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="d4cca-117">V závislosti na nastavení plánu provádění může být samotný spouštěcí proces blokován, pokud existuje otevřená objednávka kvality.</span><span class="sxs-lookup"><span data-stu-id="d4cca-117">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order.</span></span> <span data-ttu-id="d4cca-118">Můžete také blokovat následné procesy, jako je fakturace nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="d4cca-118">Alternatively, subsequent processes, such as purchase order invoicing, can be blocked.</span></span>

> [!NOTE]
> <span data-ttu-id="d4cca-119">Pokud existují otevřené objednávky kvality, skladová množství jsou automaticky blokována před vydáním.</span><span class="sxs-lookup"><span data-stu-id="d4cca-119">While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="d4cca-120">V závislosti na nastavení pole **Úplné blokování** na stránce **Vzorkování položky** se množství rovná buď množství na objednávce kvality, nebo množství na řádku zdrojového dokumentu.</span><span class="sxs-lookup"><span data-stu-id="d4cca-120">Depending on the setting of the **Full blocking** field on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span> <span data-ttu-id="d4cca-121">Další informace viz [Vzorkování položek řízení jakosti](quality-item-sampling.md).</span><span class="sxs-lookup"><span data-stu-id="d4cca-121">For more information, see [Quality management item sampling](quality-item-sampling.md).</span></span>

<span data-ttu-id="d4cca-122">Pro určitý obchodní proces určuje záznam o přidružení kvality událost a podmínky, pro které je objednávka kvality generována.</span><span class="sxs-lookup"><span data-stu-id="d4cca-122">For a given business process, the quality association record identifies the event and conditions that a quality order is generated for.</span></span> <span data-ttu-id="d4cca-123">Podmínky mohou být specifické buď pro pracoviště, nebo pro právnickou osobu.</span><span class="sxs-lookup"><span data-stu-id="d4cca-123">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="d4cca-124">Objednávku kvality, která zahrnuje destrukční testy, je možné generovat, jen když pro tuto událost existují zásoby.</span><span class="sxs-lookup"><span data-stu-id="d4cca-124">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="d4cca-125">Chcete-li pracovat s přidruženími kvality, přejděte na **Řízení zásob \> Založit \> Kontrola kvality \> Přidružení kvality**.</span><span class="sxs-lookup"><span data-stu-id="d4cca-125">To work with quality associations, go to **Inventory management \> Setup \> Quality control \> Quality associations**.</span></span> <span data-ttu-id="d4cca-126">Následující příklady ukazují způsob definování záznamu o přidružení kvality pro varianty každého obchodního procesu.</span><span class="sxs-lookup"><span data-stu-id="d4cca-126">The following examples show how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="d4cca-127">Pro každý příklad jsou v následující tabulce shrnuty události a podmínky, kterou jsou definovány v záznamu o přidružení kvality.</span><span class="sxs-lookup"><span data-stu-id="d4cca-127">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d4cca-128">Typ odkazu</span><span class="sxs-lookup"><span data-stu-id="d4cca-128">Reference type</span></span></th>
<th><span data-ttu-id="d4cca-129">Typ události</span><span class="sxs-lookup"><span data-stu-id="d4cca-129">Event type</span></span></th>
<th><span data-ttu-id="d4cca-130">Spuštění</span><span class="sxs-lookup"><span data-stu-id="d4cca-130">Execution</span></span></th>
<th><span data-ttu-id="d4cca-131">Blokování události</span><span class="sxs-lookup"><span data-stu-id="d4cca-131">Event blocking</span></span></th>
<th><span data-ttu-id="d4cca-132">Odkaz na dokument</span><span class="sxs-lookup"><span data-stu-id="d4cca-132">Document reference</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d4cca-133">Zásoby</span><span class="sxs-lookup"><span data-stu-id="d4cca-133">Inventory</span></span></td>
<td><span data-ttu-id="d4cca-134">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="d4cca-134">Not applicable</span></span></td>
<td><span data-ttu-id="d4cca-135">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="d4cca-135">Not applicable</span></span></td>
<td><span data-ttu-id="d4cca-136">Žádné</span><span class="sxs-lookup"><span data-stu-id="d4cca-136">None</span></span></td>
<td><span data-ttu-id="d4cca-137">Vše</span><span class="sxs-lookup"><span data-stu-id="d4cca-137">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="d4cca-138">Prodeje</span><span class="sxs-lookup"><span data-stu-id="d4cca-138">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="d4cca-139">Proces vyskladnění je naplánován.</span><span class="sxs-lookup"><span data-stu-id="d4cca-139">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="d4cca-140">Před</span><span class="sxs-lookup"><span data-stu-id="d4cca-140">Before</span></span></td>
<td><span data-ttu-id="d4cca-141">Žádné</span><span class="sxs-lookup"><span data-stu-id="d4cca-141">None</span></span></td>
<td rowspan="22"><span data-ttu-id="d4cca-142">Specifické ID, Skupina nebo Vše</span><span class="sxs-lookup"><span data-stu-id="d4cca-142">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4cca-143">Proces vyskladnění</span><span class="sxs-lookup"><span data-stu-id="d4cca-143">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4cca-144">Dodací list</span><span class="sxs-lookup"><span data-stu-id="d4cca-144">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4cca-145">Faktura</span><span class="sxs-lookup"><span data-stu-id="d4cca-145">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d4cca-146">Dodací list</span><span class="sxs-lookup"><span data-stu-id="d4cca-146">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="d4cca-147">Před</span><span class="sxs-lookup"><span data-stu-id="d4cca-147">Before</span></span></td>
<td><span data-ttu-id="d4cca-148">Žádné</span><span class="sxs-lookup"><span data-stu-id="d4cca-148">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4cca-149">Dodací list</span><span class="sxs-lookup"><span data-stu-id="d4cca-149">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4cca-150">Faktura</span><span class="sxs-lookup"><span data-stu-id="d4cca-150">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="d4cca-151">Nákup</span><span class="sxs-lookup"><span data-stu-id="d4cca-151">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="d4cca-152">Příjemka</span><span class="sxs-lookup"><span data-stu-id="d4cca-152">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="d4cca-153">Před</span><span class="sxs-lookup"><span data-stu-id="d4cca-153">Before</span></span></td>
<td><span data-ttu-id="d4cca-154">Žádné</span><span class="sxs-lookup"><span data-stu-id="d4cca-154">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4cca-155">Příjemka</span><span class="sxs-lookup"><span data-stu-id="d4cca-155">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4cca-156">Příjemka produktu</span><span class="sxs-lookup"><span data-stu-id="d4cca-156">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4cca-157">Faktura</span><span class="sxs-lookup"><span data-stu-id="d4cca-157">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d4cca-158">Po</span><span class="sxs-lookup"><span data-stu-id="d4cca-158">After</span></span></td>
<td><span data-ttu-id="d4cca-159">Žádné</span><span class="sxs-lookup"><span data-stu-id="d4cca-159">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4cca-160">Příjemka produktu</span><span class="sxs-lookup"><span data-stu-id="d4cca-160">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4cca-161">Faktura</span><span class="sxs-lookup"><span data-stu-id="d4cca-161">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d4cca-162">Registrace</span><span class="sxs-lookup"><span data-stu-id="d4cca-162">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="d4cca-163">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="d4cca-163">Not applicable</span></span></td>
<td><span data-ttu-id="d4cca-164">Žádné</span><span class="sxs-lookup"><span data-stu-id="d4cca-164">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4cca-165">Příjemka produktu</span><span class="sxs-lookup"><span data-stu-id="d4cca-165">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4cca-166">Faktura</span><span class="sxs-lookup"><span data-stu-id="d4cca-166">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="d4cca-167">Příjemka produktu</span><span class="sxs-lookup"><span data-stu-id="d4cca-167">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="d4cca-168">Před</span><span class="sxs-lookup"><span data-stu-id="d4cca-168">Before</span></span></td>
<td><span data-ttu-id="d4cca-169">Žádné</span><span class="sxs-lookup"><span data-stu-id="d4cca-169">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4cca-170">Příjemka produktu</span><span class="sxs-lookup"><span data-stu-id="d4cca-170">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4cca-171">Faktura</span><span class="sxs-lookup"><span data-stu-id="d4cca-171">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d4cca-172">Po</span><span class="sxs-lookup"><span data-stu-id="d4cca-172">After</span></span></td>
<td><span data-ttu-id="d4cca-173">Žádné</span><span class="sxs-lookup"><span data-stu-id="d4cca-173">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4cca-174">Faktura</span><span class="sxs-lookup"><span data-stu-id="d4cca-174">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="d4cca-175">Výroba</span><span class="sxs-lookup"><span data-stu-id="d4cca-175">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="d4cca-176">Registrace</span><span class="sxs-lookup"><span data-stu-id="d4cca-176">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="d4cca-177">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="d4cca-177">Not applicable</span></span></td>
<td><span data-ttu-id="d4cca-178">Žádné</span><span class="sxs-lookup"><span data-stu-id="d4cca-178">None</span></span></td>
<td rowspan="12"><span data-ttu-id="d4cca-179">Vše</span><span class="sxs-lookup"><span data-stu-id="d4cca-179">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4cca-180">Ohlásit jako dokončené</span><span class="sxs-lookup"><span data-stu-id="d4cca-180">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4cca-181">Konec</span><span class="sxs-lookup"><span data-stu-id="d4cca-181">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="d4cca-182">Ohlásit jako dokončené</span><span class="sxs-lookup"><span data-stu-id="d4cca-182">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="d4cca-183">Před</span><span class="sxs-lookup"><span data-stu-id="d4cca-183">Before</span></span></td>
<td><span data-ttu-id="d4cca-184">Žádné</span><span class="sxs-lookup"><span data-stu-id="d4cca-184">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4cca-185">Ohlásit jako dokončené</span><span class="sxs-lookup"><span data-stu-id="d4cca-185">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4cca-186">Konec</span><span class="sxs-lookup"><span data-stu-id="d4cca-186">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d4cca-187">Po</span><span class="sxs-lookup"><span data-stu-id="d4cca-187">After</span></span></td>
<td><span data-ttu-id="d4cca-188">Žádné</span><span class="sxs-lookup"><span data-stu-id="d4cca-188">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4cca-189">Konec</span><span class="sxs-lookup"><span data-stu-id="d4cca-189">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="d4cca-190">Karanténa</span><span class="sxs-lookup"><span data-stu-id="d4cca-190">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="d4cca-191">Ohlásit jako dokončené</span><span class="sxs-lookup"><span data-stu-id="d4cca-191">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="d4cca-192">Před</span><span class="sxs-lookup"><span data-stu-id="d4cca-192">Before</span></span></td>
<td><span data-ttu-id="d4cca-193">Ohlásit jako dokončené</span><span class="sxs-lookup"><span data-stu-id="d4cca-193">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4cca-194">Konec</span><span class="sxs-lookup"><span data-stu-id="d4cca-194">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4cca-195">Po</span><span class="sxs-lookup"><span data-stu-id="d4cca-195">After</span></span></td>
<td><span data-ttu-id="d4cca-196">Konec</span><span class="sxs-lookup"><span data-stu-id="d4cca-196">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4cca-197">Konec</span><span class="sxs-lookup"><span data-stu-id="d4cca-197">End</span></span></td>
<td><span data-ttu-id="d4cca-198">Před</span><span class="sxs-lookup"><span data-stu-id="d4cca-198">Before</span></span></td>
<td><span data-ttu-id="d4cca-199">Konec</span><span class="sxs-lookup"><span data-stu-id="d4cca-199">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d4cca-200">Operace postupu</span><span class="sxs-lookup"><span data-stu-id="d4cca-200">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="d4cca-201">Oznámit jako dokončené</span><span class="sxs-lookup"><span data-stu-id="d4cca-201">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="d4cca-202">Před</span><span class="sxs-lookup"><span data-stu-id="d4cca-202">Before</span></span></td>
<td><span data-ttu-id="d4cca-203">Není</span><span class="sxs-lookup"><span data-stu-id="d4cca-203">None</span></span></td>
<td rowspan="3"><span data-ttu-id="d4cca-204">Specifické ID, Skupina nebo Vše a Podle prostředku, Skupina nebo Vše</span><span class="sxs-lookup"><span data-stu-id="d4cca-204">Specific ID, Group, or All, and specific Resource, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4cca-205">Oznámit jako dokončené</span><span class="sxs-lookup"><span data-stu-id="d4cca-205">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4cca-206">Po</span><span class="sxs-lookup"><span data-stu-id="d4cca-206">After</span></span></td>
<td><span data-ttu-id="d4cca-207">Není</span><span class="sxs-lookup"><span data-stu-id="d4cca-207">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d4cca-208">Výroba vedlejších produktů</span><span class="sxs-lookup"><span data-stu-id="d4cca-208">Co-product production</span></span></td>
<td><span data-ttu-id="d4cca-209">Registrace</span><span class="sxs-lookup"><span data-stu-id="d4cca-209">Registration</span></span></td>
<td><span data-ttu-id="d4cca-210">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="d4cca-210">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d4cca-211">Není</span><span class="sxs-lookup"><span data-stu-id="d4cca-211">None</span></span></td>
<td rowspan="3"><span data-ttu-id="d4cca-212">Vše</span><span class="sxs-lookup"><span data-stu-id="d4cca-212">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d4cca-213">Oznámit jako dokončené</span><span class="sxs-lookup"><span data-stu-id="d4cca-213">Report as finished</span></span></td>
<td><span data-ttu-id="d4cca-214">Před</span><span class="sxs-lookup"><span data-stu-id="d4cca-214">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4cca-215">Po</span><span class="sxs-lookup"><span data-stu-id="d4cca-215">After</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="d4cca-216">Funkce *Správa kvality pro procesy skladu* přidává možnosti zpracování objednávky kvality pro výrobu s polem **Typ události** nastaveným jako *Oznámit jako dokončené* a polem **Spuštění** nastaveným jako *Po dokončení*, a pro nákupy s polem **Typem události** nastaveným jako *Registrace*.</span><span class="sxs-lookup"><span data-stu-id="d4cca-216">The *Quality management for warehouse processes* feature adds capabilities for quality order processing for production where the **Event type** field is set to *Report as finished* and the **Execution** field is set to *After*, and for purchases where the **Event type** field is set to *Registration*.</span></span> <span data-ttu-id="d4cca-217">Další informace viz [Správa kvality pro procesy skladu](quality-management-for-warehouses-processes.md).</span><span class="sxs-lookup"><span data-stu-id="d4cca-217">For more information, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

<span data-ttu-id="d4cca-218">V následující tabulce jsou uvedeny další informace o způsobu, jak lze generovat objednávky kvality pro určité typy procesů.</span><span class="sxs-lookup"><span data-stu-id="d4cca-218">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>

<div class="tableSection">
<table>
<thead>
<tr>
<th><span data-ttu-id="d4cca-219">Typ procesu</span><span class="sxs-lookup"><span data-stu-id="d4cca-219">Type of process</span></span></th>
<th><span data-ttu-id="d4cca-220">Kdy lze objednávku kvality generovat automaticky</span><span class="sxs-lookup"><span data-stu-id="d4cca-220">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="d4cca-221">Kdy lze objednávku kvality generovat v případě, že je vyžadován destrukční test</span><span class="sxs-lookup"><span data-stu-id="d4cca-221">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="d4cca-222">Informace o podmínkách</span><span class="sxs-lookup"><span data-stu-id="d4cca-222">Condition information</span></span></th>
<th><span data-ttu-id="d4cca-223">Informace o ručním generování</span><span class="sxs-lookup"><span data-stu-id="d4cca-223">Manual generation information</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d4cca-224">Nákupní objednávka</span><span class="sxs-lookup"><span data-stu-id="d4cca-224">Purchase order</span></span></td>
<td><span data-ttu-id="d4cca-225">Před tím nebo po tom, co je příjemka produktu pro přijatý materiál zaúčtována</span><span class="sxs-lookup"><span data-stu-id="d4cca-225">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="d4cca-226">Po tom, co je příjemka produktu pro přijatý materiál zaúčtována, protože materiál musí být k dispozici pro destrukční testy</span><span class="sxs-lookup"><span data-stu-id="d4cca-226">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="d4cca-227">Požadavek pro objednávku kvality se může týkat určitého pracoviště, položky, dodavatele nebo kombinace těchto podmínek.</span><span class="sxs-lookup"><span data-stu-id="d4cca-227">The requirement for a quality order can reflect a specific site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="d4cca-228">Ručně vygenerovaná objednávka kvality, která odkazuje na nákupní objednávku, může použít informace ze záznamu o přidružení kvality, jako je plán testování vzorku.</span><span class="sxs-lookup"><span data-stu-id="d4cca-228">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4cca-229">Karanténní příkaz</span><span class="sxs-lookup"><span data-stu-id="d4cca-229">Quarantine order</span></span></td>
<td><span data-ttu-id="d4cca-230">Před tím nebo po tom, co je karanténní příkaz vykázán jako dokončený nebo ukončený</span><span class="sxs-lookup"><span data-stu-id="d4cca-230">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="d4cca-231">Objednávky kvality, které vyžadují provedení destrukčních testů, nelze generovat.</span><span class="sxs-lookup"><span data-stu-id="d4cca-231">Quality orders that require destructive tests can't be generated.</span></span> <span data-ttu-id="d4cca-232">Předpokládá se, že funkce karanténního příkazu zpracovává likvidaci materiálu, který je zničen.</span><span class="sxs-lookup"><span data-stu-id="d4cca-232">It's assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="d4cca-233">Požadavek pro objednávku kvality se může týkat určitého pracoviště, položky, dodavatele nebo kombinace těchto podmínek.</span><span class="sxs-lookup"><span data-stu-id="d4cca-233">The requirement for a quality order can reflect a specific site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="d4cca-234">Ručně vygenerovaná objednávka kvality, která odkazuje na karanténní příkaz, může použít informace ze záznamu o přidružení kvality, jako je plán testování vzorku.</span><span class="sxs-lookup"><span data-stu-id="d4cca-234">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4cca-235">Prodejní objednávka</span><span class="sxs-lookup"><span data-stu-id="d4cca-235">Sales order</span></span></td>
<td><span data-ttu-id="d4cca-236">Před naplánovaným procesem vyskladnění nebo aktualizací dodacího listu pro položky, které byly právě dodány</span><span class="sxs-lookup"><span data-stu-id="d4cca-236">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="d4cca-237">Při jakémkoli kroku</span><span class="sxs-lookup"><span data-stu-id="d4cca-237">At any step</span></span></td>
<td><span data-ttu-id="d4cca-238">Požadavek pro objednávku kvality se může týkat určitého pracoviště, položky, odběratele nebo kombinace těchto podmínek.</span><span class="sxs-lookup"><span data-stu-id="d4cca-238">The requirement for a quality order can reflect a specific site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="d4cca-239">Ručně vygenerovaná objednávka kvality, která odkazuje na prodejní objednávku, může použít informace ze záznamu o přidružení kvality, jako je plán testování vzorku.</span><span class="sxs-lookup"><span data-stu-id="d4cca-239">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4cca-240">Výrobní zakázka</span><span class="sxs-lookup"><span data-stu-id="d4cca-240">Production order</span></span></td>
<td><span data-ttu-id="d4cca-241">Před tím nebo po tom, co je vykázáno dokončené množství pro výrobní zakázku</span><span class="sxs-lookup"><span data-stu-id="d4cca-241">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="d4cca-242">Po tom, co je vykázáno dokončené množství pro výrobní zakázku</span><span class="sxs-lookup"><span data-stu-id="d4cca-242">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="d4cca-243">Požadavek pro objednávku kvality se může týkat určitého pracoviště, položky, nebo kombinace těchto podmínek.</span><span class="sxs-lookup"><span data-stu-id="d4cca-243">The requirement for a quality order can reflect a specific site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="d4cca-244">Ručně vygenerovaná objednávka kvality, která odkazuje na výrobní zakázku, může použít informace ze záznamu o přidružení kvality, jako je plán testování vzorku.</span><span class="sxs-lookup"><span data-stu-id="d4cca-244">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4cca-245">Výrobní zakázka s operací postupu</span><span class="sxs-lookup"><span data-stu-id="d4cca-245">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="d4cca-246">Před tím nebo po tom, co je dokončeno ohlášení pro operaci</span><span class="sxs-lookup"><span data-stu-id="d4cca-246">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="d4cca-247">Po tom, co je pro poslední operaci dokončeno ohlášení výrobní zakázky</span><span class="sxs-lookup"><span data-stu-id="d4cca-247">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="d4cca-248">Požadavek pro objednávku kvality se může týkat určitého pracoviště, položky, provozního prostředku nebo kombinace těchto podmínek.</span><span class="sxs-lookup"><span data-stu-id="d4cca-248">The requirement for a quality order can reflect a specific site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="d4cca-249">Ručně vygenerovaná objednávka kvality, která odkazuje na operaci postupu, může použít informace ze záznamu o přidružení kvality, jako je plán testování vzorku.</span><span class="sxs-lookup"><span data-stu-id="d4cca-249">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d4cca-250">Zásoby</span><span class="sxs-lookup"><span data-stu-id="d4cca-250">Inventory</span></span></td>
<td><span data-ttu-id="d4cca-251">Objednávku kvality nelze automaticky generovat pro transakci v deníku zásob ani pro transakce převodních příkazů.</span><span class="sxs-lookup"><span data-stu-id="d4cca-251">A quality order can't be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="d4cca-252">Objednávku kvality je možné vytvořit ručně pro množství položky na skladě.</span><span class="sxs-lookup"><span data-stu-id="d4cca-252">A quality order must be manually created for an item's inventory quantity.</span></span> <span data-ttu-id="d4cca-253">Jsou vyžadovány fyzické zásoby na skladě.</span><span class="sxs-lookup"><span data-stu-id="d4cca-253">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>
</div>

## <a name="examples-of-automatic-generation-of-quality-orders"></a><span data-ttu-id="d4cca-254">Příklady automatického generování objednávek kvality</span><span class="sxs-lookup"><span data-stu-id="d4cca-254">Examples of automatic generation of quality orders</span></span>

### <a name="purchasing"></a><span data-ttu-id="d4cca-255">Nákup</span><span class="sxs-lookup"><span data-stu-id="d4cca-255">Purchasing</span></span>

<span data-ttu-id="d4cca-256">Pokud v nákupu nastavíte pole **Typ události** na hodnotu *Příjemka produktu* a pole **Spuštění** na *Po* na stránce **Přidružení kvality**, získáte následující výsledky:</span><span class="sxs-lookup"><span data-stu-id="d4cca-256">In purchasing, if you set the **Event type** field to *Product receipt* and the **Execution** field to *After* on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="d4cca-257">Pokud je možnost **Podle aktualizovaného množství** nastavená na *Ano*, objednávka kvality se vygeneruje pro každý příjem na základě nákupní objednávky podle přijatého množství a nastavení ve vzorku položky.</span><span class="sxs-lookup"><span data-stu-id="d4cca-257">If the **Per updated quantity** option is set to *Yes*, a quality order is generated for every receipt against the purchase order, based on the received quantity and settings in the item sampling.</span></span> <span data-ttu-id="d4cca-258">Při každém příjmu množství na základě nákupní objednávky jsou nové objednávky kvality generovány na základě nově přijatého množství.</span><span class="sxs-lookup"><span data-stu-id="d4cca-258">Every time that a quantity is received against the purchase order, new quality orders are generated based on the newly received quantity.</span></span>
- <span data-ttu-id="d4cca-259">Pokud je možnost **Podle aktualizovaného množství** nastavená na *Ne*, objednávka kvality se vygeneruje pro první příjem na základě nákupní objednávky podle přijatého množství a nastavení ve vzorku položky.</span><span class="sxs-lookup"><span data-stu-id="d4cca-259">If the **Per updated quantity** option is set to *No*, a quality order is generated for the first receipt against the purchase order, based on the received quantity.</span></span> <span data-ttu-id="d4cca-260">Dále se vytvoří jedna nebo více objednávek kvality na základě zbývajícího množství v závislosti na sledovacích dimenzích.</span><span class="sxs-lookup"><span data-stu-id="d4cca-260">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions.</span></span> <span data-ttu-id="d4cca-261">Objednávky kvality nejsou vygenerovány pro následné příjmy s nákupní objednávkou.</span><span class="sxs-lookup"><span data-stu-id="d4cca-261">Quality orders aren't generated for subsequent receipts against the purchase order.</span></span>

### <a name="production"></a><span data-ttu-id="d4cca-262">Výrobní</span><span class="sxs-lookup"><span data-stu-id="d4cca-262">Production</span></span>

<span data-ttu-id="d4cca-263">Pokud ve výrobě nastavíte pole **Typ události** na hodnotu *Vykázat jako dokončené* a pole **Spuštění** na *Po* na stránce **Přidružení kvality**, získáte následující výsledky:</span><span class="sxs-lookup"><span data-stu-id="d4cca-263">In production, if you set the **Event type** field to *Report as finished* and the **Execution** field to *After* on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="d4cca-264">Pokud je možnost **Podle aktualizovaného množství** nastavená na *Ano*, objednávka kvality se vygeneruje podle každého dokončeného množství a nastavení ve vzorku položky.</span><span class="sxs-lookup"><span data-stu-id="d4cca-264">If the **Per updated quantity** option is set to *Yes*, a quality order is generated based on every finished quantity and settings in the item sampling.</span></span> <span data-ttu-id="d4cca-265">Při každém vykázání množství jako dokončeného na základě výrobní zakázky jsou nové objednávky kvality generovány na základě nově dokončeného množství.</span><span class="sxs-lookup"><span data-stu-id="d4cca-265">Every time that a quantity is reported as finished against the production order, new quality orders are generated based on the newly finished quantity.</span></span> <span data-ttu-id="d4cca-266">Tato logika generování je konzistentní s nákupem.</span><span class="sxs-lookup"><span data-stu-id="d4cca-266">This generation logic is consistent with purchasing.</span></span>
- <span data-ttu-id="d4cca-267">Pokud je možnost **Podle aktualizovaného množství** nastavená na *Ne*, objednávka kvality se vygeneruje při přvní vykázání množství jako dokončeného na základě dokončeného množství.</span><span class="sxs-lookup"><span data-stu-id="d4cca-267">If the **Per updated quantity** option is set to *No*, a quality order is generated the first time that a quantity is reported as finished, based on the finished quantity.</span></span> <span data-ttu-id="d4cca-268">Dále se vytvoří jedna nebo více objednávek kvality na základě zbývajícího množství v závislosti na sledovacích dimenzích vzorku položky.</span><span class="sxs-lookup"><span data-stu-id="d4cca-268">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions of the item sampling.</span></span> <span data-ttu-id="d4cca-269">Objednávky kvality nejsou vygenerovány pro následná dokončená množství.</span><span class="sxs-lookup"><span data-stu-id="d4cca-269">Quality orders aren't generated for subsequent finished quantities.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="d4cca-270">Specifikace kvality</span><span class="sxs-lookup"><span data-stu-id="d4cca-270">Quality specification</span></span></th>
<th><span data-ttu-id="d4cca-271">Na aktualizované množství</span><span class="sxs-lookup"><span data-stu-id="d4cca-271">Per updated quantity</span></span></th>
<th><span data-ttu-id="d4cca-272">Na sledovací dimenzi</span><span class="sxs-lookup"><span data-stu-id="d4cca-272">Per tracking dimension</span></span></th>
<th><span data-ttu-id="d4cca-273">Výsledek</span><span class="sxs-lookup"><span data-stu-id="d4cca-273">Result</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d4cca-274">Počet procent: 10 %</span><span class="sxs-lookup"><span data-stu-id="d4cca-274">Percentage: 10%</span></span></td>
<td><span data-ttu-id="d4cca-275">Ano</span><span class="sxs-lookup"><span data-stu-id="d4cca-275">Yes</span></span></td>
<td>
<p><span data-ttu-id="d4cca-276">Číslo dávky: Ne</span><span class="sxs-lookup"><span data-stu-id="d4cca-276">Batch number: No</span></span></p>
<p><span data-ttu-id="d4cca-277">Sériové číslo: Ne</span><span class="sxs-lookup"><span data-stu-id="d4cca-277">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="d4cca-278">Množství na objednávce: 100</span><span class="sxs-lookup"><span data-stu-id="d4cca-278">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="d4cca-279">Vykázat jako dokončené pro 30</span><span class="sxs-lookup"><span data-stu-id="d4cca-279">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="d4cca-280">Objednávka kvality 1 na 3 (10 % z 30)</span><span class="sxs-lookup"><span data-stu-id="d4cca-280">Quality order 1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="d4cca-281">Vykázat jako dokončené pro 70</span><span class="sxs-lookup"><span data-stu-id="d4cca-281">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="d4cca-282">Objednávka kvality 2 na 7 (10 % ze zbývajícího množství objednávky, které se v tomto případě rovná 70)</span><span class="sxs-lookup"><span data-stu-id="d4cca-282">Quality order 2 for 7 (10% of the remaining order quantity, which is 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="d4cca-283">Fixní množství: 1</span><span class="sxs-lookup"><span data-stu-id="d4cca-283">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="d4cca-284">Žádný</span><span class="sxs-lookup"><span data-stu-id="d4cca-284">No</span></span></td>
<td>
<p><span data-ttu-id="d4cca-285">Číslo dávky: Ne</span><span class="sxs-lookup"><span data-stu-id="d4cca-285">Batch number: No</span></span></p>
<p><span data-ttu-id="d4cca-286">Sériové číslo: Ne</span><span class="sxs-lookup"><span data-stu-id="d4cca-286">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="d4cca-287">Množství na objednávce: 100</span><span class="sxs-lookup"><span data-stu-id="d4cca-287">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="d4cca-288">Vykázat jako dokončené pro 30</span><span class="sxs-lookup"><span data-stu-id="d4cca-288">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="d4cca-289">Objednávka kvality 1 pro 1 (pro první vykázané množství jako dokončené, které má pevnou hodnotu 1)</span><span class="sxs-lookup"><span data-stu-id="d4cca-289">Quality order 1 for 1 (for the first reported-as-finished quantity, which has a fixed value of 1)</span></span></li>
<li><span data-ttu-id="d4cca-290">Objednávka kvality 2 pro 1 (pro zbývající množství, které má stabilně pevnou hodnotu 1)</span><span class="sxs-lookup"><span data-stu-id="d4cca-290">Quality order 2 for 1 (for the remaining quantity, which still has a fixed value of 1)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="d4cca-291">Vykázat jako dokončené pro 10</span><span class="sxs-lookup"><span data-stu-id="d4cca-291">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="d4cca-292">Nejsou vytvořeny žádné objednávky kvality.</span><span class="sxs-lookup"><span data-stu-id="d4cca-292">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="d4cca-293">Vykázat jako dokončené pro 60</span><span class="sxs-lookup"><span data-stu-id="d4cca-293">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="d4cca-294">Nejsou vytvořeny žádné objednávky kvality.</span><span class="sxs-lookup"><span data-stu-id="d4cca-294">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="d4cca-295">Fixní množství: 1</span><span class="sxs-lookup"><span data-stu-id="d4cca-295">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="d4cca-296">Ano</span><span class="sxs-lookup"><span data-stu-id="d4cca-296">Yes</span></span></td>
<td>
<p><span data-ttu-id="d4cca-297">Číslo dávky: Ano</span><span class="sxs-lookup"><span data-stu-id="d4cca-297">Batch number: Yes</span></span></p>
<p><span data-ttu-id="d4cca-298">Sériové číslo: Ano</span><span class="sxs-lookup"><span data-stu-id="d4cca-298">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="d4cca-299">Množství na objednávce: 10</span><span class="sxs-lookup"><span data-stu-id="d4cca-299">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="d4cca-300">Zpráva o dokončení pro 3: 1 pro číslo šarže b1, sériové číslo s1; 1 pro číslo šarže b2, sériové číslo s2; a 1 pro číslo šarže b3, sériové číslo s3</span><span class="sxs-lookup"><span data-stu-id="d4cca-300">Report as finished for 3: 1 for batch number b1, serial number s1; 1 for batch number b2, serial number s2; and 1 for batch number b3, serial number s3</span></span>
<ul>
<li><span data-ttu-id="d4cca-301">Pořadí kvality 1 pro 1 z dávky b1, sériové číslo s1</span><span class="sxs-lookup"><span data-stu-id="d4cca-301">Quality order 1 for 1 of batch number b1, serial number s1</span></span></li>
<li><span data-ttu-id="d4cca-302">Pořadí kvality 2 pro 1 z dávky b2, sériové číslo s2</span><span class="sxs-lookup"><span data-stu-id="d4cca-302">Quality order 2 for 1 of batch number b2, serial number s2</span></span></li>
<li><span data-ttu-id="d4cca-303">Pořadí kvality 3 pro 1 z dávky b3, sériové číslo s3</span><span class="sxs-lookup"><span data-stu-id="d4cca-303">Quality order 3 for 1 of batch number b3, serial number s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="d4cca-304">Zpráva o dokončení pro 2: 1 pro číslo šarže b4, sériové číslo s4; a 1 pro číslo šarže b5, sériové číslo s5</span><span class="sxs-lookup"><span data-stu-id="d4cca-304">Report as finished for 2: 1 for batch number b4, serial number s4; and 1 for batch number b5, serial number s5</span></span>
<ul>
<li><span data-ttu-id="d4cca-305">Pořadí kvality 4 pro 1 z dávky b4, sériové číslo s4</span><span class="sxs-lookup"><span data-stu-id="d4cca-305">Quality order 4 for 1 of batch number b4, serial number s4</span></span></li>
<li><span data-ttu-id="d4cca-306">Pořadí kvality 5 pro 1 z dávky b5, sériové číslo s5</span><span class="sxs-lookup"><span data-stu-id="d4cca-306">Quality order 5 for 1 of batch number b5, serial number s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="d4cca-307"><strong>Poznámka:</strong> Dávku lze znovu použít.</span><span class="sxs-lookup"><span data-stu-id="d4cca-307"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="d4cca-308">Fixní množství: 2</span><span class="sxs-lookup"><span data-stu-id="d4cca-308">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="d4cca-309">Žádný</span><span class="sxs-lookup"><span data-stu-id="d4cca-309">No</span></span></td>
<td>
<p><span data-ttu-id="d4cca-310">Číslo dávky: Ano</span><span class="sxs-lookup"><span data-stu-id="d4cca-310">Batch number: Yes</span></span></p>
<p><span data-ttu-id="d4cca-311">Sériové číslo: Ano</span><span class="sxs-lookup"><span data-stu-id="d4cca-311">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="d4cca-312">Množství na objednávce: 10</span><span class="sxs-lookup"><span data-stu-id="d4cca-312">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="d4cca-313">Zpráva o dokončení pro 3: 1 pro číslo šarže b1, sériové číslo s1; 1 pro číslo šarže b2, sériové číslo s2; a 1 pro číslo šarže b3, sériové číslo s3; a 1 pro číslo šarže b4, sériové číslo s4</span><span class="sxs-lookup"><span data-stu-id="d4cca-313">Report as finished for 4: 1 for batch number b1, serial number s1; 1 for batch number b2, serial number s2; 1 for batch number b3, serial number s3; and 1 for batch number b4, serial number s4</span></span>
<ul>
<li><span data-ttu-id="d4cca-314">Pořadí kvality 1 pro 1 z dávky b1, sériové číslo s1</span><span class="sxs-lookup"><span data-stu-id="d4cca-314">Quality order 1 for 1 of batch number b1, serial number s1</span></span></li>
<li><span data-ttu-id="d4cca-315">Pořadí kvality 2 pro 1 z dávky b2, sériové číslo s2</span><span class="sxs-lookup"><span data-stu-id="d4cca-315">Quality order 2 for 1 of batch number b2, serial number s2</span></span></li>
<li><span data-ttu-id="d4cca-316">Pořadí kvality 3 pro 1 z dávky b3, sériové číslo s3</span><span class="sxs-lookup"><span data-stu-id="d4cca-316">Quality order 3 for 1 of batch number b3, serial number s3</span></span></li>
<li><span data-ttu-id="d4cca-317">Pořadí kvality 4 pro 1 z dávky b4, sériové číslo s4</span><span class="sxs-lookup"><span data-stu-id="d4cca-317">Quality order 4 for 1 of batch number b4, serial number s4</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="d4cca-318">Objednávka kvality 5 pro 2, bez reference na dávku a sériové číslo</span><span class="sxs-lookup"><span data-stu-id="d4cca-318">Quality order 5 for 2, without a reference to a batch number and a serial number</span></span></li>
</ul>
</li>
<li><span data-ttu-id="d4cca-319">Zpráva o dokončení pro 6: 1 pro číslo šarže b5, sériové číslo s5; 1 pro číslo šarže b6, sériové číslo s6; 1 pro číslo šarže b7, sériové číslo s7; 1 pro číslo šarže b8, sériové číslo s8; 1 pro číslo šarže b9, sériové číslo s9; a 1 pro číslo šarže b10, sériové číslo s10</span><span class="sxs-lookup"><span data-stu-id="d4cca-319">Report as finished for 6: 1 for batch number b5, serial number s5; 1 for batch number b6, serial number s6; 1 for batch number b7, serial number s7; 1 for batch number b8, serial number s8; 1 for batch number b9, serial number s9; and 1 for batch number b10, serial number s10</span></span>
<ul>
<li><span data-ttu-id="d4cca-320">Nejsou vytvořeny žádné objednávky kvality.</span><span class="sxs-lookup"><span data-stu-id="d4cca-320">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="d4cca-321">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="d4cca-321">Additional resources</span></span>

- [<span data-ttu-id="d4cca-322">Procesy správy kvality</span><span class="sxs-lookup"><span data-stu-id="d4cca-322">Quality management processes</span></span>](quality-management-processes.md)
- [<span data-ttu-id="d4cca-323">Povolit správu kvality a neshod</span><span class="sxs-lookup"><span data-stu-id="d4cca-323">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="d4cca-324">Správa kvality pro procesy skladu</span><span class="sxs-lookup"><span data-stu-id="d4cca-324">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
