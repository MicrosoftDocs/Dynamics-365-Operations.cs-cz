---
title: "Přehled správy kvality"
description: "Toto téma popisuje, jak lze použít správu kvality v aplikaci Microsoft Dynamics 365 for Finance and Operations ke zlepšení kvality produktů v rámci dodavatelsko-odběratelského řetězce."
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 1630d13437d7e930fdf32ed5fdc61fc62bc33817
ms.contentlocale: cs-cz
ms.lasthandoff: 08/07/2018

---

# <a name="quality-management-overview"></a><span data-ttu-id="d0a80-103">Přehled správy kvality</span><span class="sxs-lookup"><span data-stu-id="d0a80-103">Quality management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d0a80-104">Toto téma popisuje, jak lze použít správu kvality v aplikaci Microsoft Dynamics 365 for Finance and Operations ke zlepšení kvality produktů v rámci dodavatelsko-odběratelského řetězce.</span><span class="sxs-lookup"><span data-stu-id="d0a80-104">This topic describes how you can use quality management in Microsoft Dynamics 365 for Finance and Operations to help improve product quality within your supply chain.</span></span>

<span data-ttu-id="d0a80-105">Správa kvality pomáhá se správou doby oběhu objednávky při zpracování nevyhovujících produktů bez ohledu na místo jejich původu.</span><span class="sxs-lookup"><span data-stu-id="d0a80-105">Quality management can help you manage turnaround times when you handle nonconforming products, regardless of their point of origin.</span></span> <span data-ttu-id="d0a80-106">Vzhledem k tomu, že typy diagnostiky jsou propojeny s hlášením oprav, aplikace Microsoft Dynamics 365 for Finance and Operations může naplánovat úlohy k nápravě problémů a zabránění jejich opakování.</span><span class="sxs-lookup"><span data-stu-id="d0a80-106">Because diagnostic types are linked to correction reporting, Microsoft Dynamics 365 for Finance and Operations can schedule tasks to correct problems and prevent them from recurring.</span></span>

<span data-ttu-id="d0a80-107">Kromě funkcí pro správu neshod obsahuje moduly správy kvality také funkce pro sledování problémů podle jejich typu (včetně interních potíží) a pro určování krátkodobých a dlouhodobých řešení.</span><span class="sxs-lookup"><span data-stu-id="d0a80-107">In addition to functionality for managing nonconformance, quality management includes functionality for tracking issues by problem type (even internal problems), and for identifying solutions as short-term or long-term.</span></span> <span data-ttu-id="d0a80-108">Statistické údaje o klíčových ukazatelů výkonnosti (KPI) nabízí náhled na historii předchozích potíží s neshodami a řešení, která byla použita k jejich nápravě.</span><span class="sxs-lookup"><span data-stu-id="d0a80-108">Statistics about key performance indicators (KPIs) provide insight into the history of previous nonconformance issues and the solutions that were used to correct them.</span></span> <span data-ttu-id="d0a80-109">Historická data můžete použít ke kontrole účinnosti předchozích opatření pro zajištění kvality a k rozhodnutí o tom, zda tato opatření použít i v budoucnu.</span><span class="sxs-lookup"><span data-stu-id="d0a80-109">You can use historical data to review the effectiveness of previous quality measures and determine appropriate measures to use in the future.</span></span>

<span data-ttu-id="d0a80-110">Při nastavování přidružení kvality může aplikace Finance and Operations vygenerovat objednávky kvality pro různé obchodní procesy, události a podmínky.</span><span class="sxs-lookup"><span data-stu-id="d0a80-110">When you set up a quality association, Finance and Operations can generate quality orders for various business processes, events, and conditions.</span></span> <span data-ttu-id="d0a80-111">Přiřazení kvality může zahrnovat určitou položku, určitou skupinu položek nebo všechny položky.</span><span class="sxs-lookup"><span data-stu-id="d0a80-111">The quality association can cover a specific item, a specific group of items, or all items.</span></span>

## <a name="examples-of-the-use-of-quality-management"></a><span data-ttu-id="d0a80-112">Příklady použití správy kvality</span><span class="sxs-lookup"><span data-stu-id="d0a80-112">Examples of the use of quality management</span></span>
<span data-ttu-id="d0a80-113">Správa kvality je flexibilní a lze ji implementovat různými způsoby, aby byly splněny požadavky konkrétních úrovní operací dodavatelsko-odběratelského řetězce.</span><span class="sxs-lookup"><span data-stu-id="d0a80-113">Quality management is flexible and can be implemented in various ways to meet the requirements of specific levels of supply chain operations.</span></span> <span data-ttu-id="d0a80-114">V následujících příkladech jsou znázorněna možná použití těchto funkcí:</span><span class="sxs-lookup"><span data-stu-id="d0a80-114">The following examples illustrate possible uses of these features:</span></span>

-   <span data-ttu-id="d0a80-115">Automatické spuštění procesu řízení kvality na základě předem definovaných kritérií (při registraci nákupní objednávky od konkrétního dodavatele ve skladu).</span><span class="sxs-lookup"><span data-stu-id="d0a80-115">Automatically start a quality control process, based on predefined criteria (upon warehouse registration of a purchase order from a specific vendor).</span></span>
-   <span data-ttu-id="d0a80-116">Blokování zásob při inventuře zabraňuje použití neschválených zásob (úplné blokování množství nákupní objednávky).</span><span class="sxs-lookup"><span data-stu-id="d0a80-116">Block inventory during inspection to prevent non-approved inventory from being used (full blocking of purchase order quantities).</span></span>
-   <span data-ttu-id="d0a80-117">Použití vzorkování jako součásti přidružení k definici množství aktuálních fyzických zásob, které je nutné zkontrolovat.</span><span class="sxs-lookup"><span data-stu-id="d0a80-117">Use item sampling as part of a quality association to define the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="d0a80-118">Vzorkování může být založeno na pevném množství nebo na procentuální hodnotě.</span><span class="sxs-lookup"><span data-stu-id="d0a80-118">Sampling can be based on fixed quantities or a percentage.</span></span>
-   <span data-ttu-id="d0a80-119">Vytvořte objednávky kvality pro částečné příjmy.</span><span class="sxs-lookup"><span data-stu-id="d0a80-119">Create quality orders for partial receipts.</span></span> <span data-ttu-id="d0a80-120">Abyste mohli vytvořit objednávku kvality, která je založena na množství fyzicky přijatém s objednávkou, je nutné zaškrtnout políčko **Na aktualizované množství** ve formuláři **Vzorkování položky**.</span><span class="sxs-lookup"><span data-stu-id="d0a80-120">To create a quality order that is based on the quantity that is physically received with an order, you must select the **Per updated quantity** check box on the **Item sampling** form.</span></span>
-   <span data-ttu-id="d0a80-121">Vytvoření typů testu, které zahrnují minimální, maximální a cílové hodnoty testu, a vykonání testu kvality vůči množství s předdefinovanými ověřovacími výsledky.</span><span class="sxs-lookup"><span data-stu-id="d0a80-121">Create test types that include minimum, maximum, and target test values, and perform qualitative-versus-quantitative testing that has predefined validation results.</span></span>
-   <span data-ttu-id="d0a80-122">Určení přijatelné úrovně kvality (AQL) pro řízení odchylek měření kvality.</span><span class="sxs-lookup"><span data-stu-id="d0a80-122">Specify an acceptable quality level (AQL) to control quality measure tolerances.</span></span>
-   <span data-ttu-id="d0a80-123">Určení zdrojů vyžadovaných operací kontroly, jako je například prostor testu nebo testovací přístroje.</span><span class="sxs-lookup"><span data-stu-id="d0a80-123">Specify the resources that an inspection operation requires, such as a test area and test instruments.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="d0a80-124">Práce s přidruženími kvality</span><span class="sxs-lookup"><span data-stu-id="d0a80-124">Working with quality associations</span></span>
<span data-ttu-id="d0a80-125">Obchodní proces, který používá přidružení kvality, může být přiřazen k různým zdrojovým dokumentům, jako například k nákupním objednávkám, prodejním objednávkám nebo výrobním zakázkám.</span><span class="sxs-lookup"><span data-stu-id="d0a80-125">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="d0a80-126">Každý záznam o přidružení kvality určuje sadu testů, přijatelnou úroveň kvality a plán vzorkování, které platí pro vygenerované objednávky kvality.</span><span class="sxs-lookup"><span data-stu-id="d0a80-126">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="d0a80-127">Je nutné definovat záznam o přidružení kvality pro každou variantu v obchodním procesu.</span><span class="sxs-lookup"><span data-stu-id="d0a80-127">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="d0a80-128">Můžete například nastavit přidružení kvality, které vygeneruje objednávku kvality při aktualizaci příjemky produktu nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="d0a80-128">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="d0a80-129">V závislosti na nastavení plánu provedení může být samotný spouštěcí proces blokován, dokud existuje otevřená objednávka kvality, nebo mohou být blokovány další procesy, jako například fakturování nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="d0a80-129">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order, or the next processes, such as purchase order invoicing, can be blocked.</span></span>

<span data-ttu-id="d0a80-130">**Poznámka:** Pokud existují otevřené objednávky kvality, skladová množství jsou automaticky blokována před vydáním.</span><span class="sxs-lookup"><span data-stu-id="d0a80-130">**Note:** While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="d0a80-131">V závislosti na nastavení **Úplné blokování** na stránce **Vzorkování položky** se množství rovná buď množství na objednávce kvality, nebo množství na řádku zdrojového dokumentu.</span><span class="sxs-lookup"><span data-stu-id="d0a80-131">Depending on the **Full blocking** setting on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span>

<span data-ttu-id="d0a80-132">Pro určitý obchodní proces určuje záznam o přidružení kvality událost a podmínky, pro které je objednávka kvality generována.</span><span class="sxs-lookup"><span data-stu-id="d0a80-132">For a given business process, the quality association record identifies the event and the conditions that a quality order is generated for.</span></span> <span data-ttu-id="d0a80-133">Podmínky mohou být specifické buď pro pracoviště, nebo pro právnickou osobu.</span><span class="sxs-lookup"><span data-stu-id="d0a80-133">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="d0a80-134">Objednávku kvality, která zahrnuje destrukční testy, je možné generovat, jen když pro tuto událost existují zásoby.</span><span class="sxs-lookup"><span data-stu-id="d0a80-134">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="d0a80-135">Následující příklady ilustrují způsob definování záznamu o přidružení kvality pro varianty každého obchodního procesu.</span><span class="sxs-lookup"><span data-stu-id="d0a80-135">The following examples illustrate how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="d0a80-136">Pro každý příklad jsou v následující tabulce shrnuty události a podmínky, kterou jsou definovány v záznamu o přidružení kvality.</span><span class="sxs-lookup"><span data-stu-id="d0a80-136">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="d0a80-137">Typ odkazu</span><span class="sxs-lookup"><span data-stu-id="d0a80-137">Reference type</span></span></th>
<th><span data-ttu-id="d0a80-138">Typ události</span><span class="sxs-lookup"><span data-stu-id="d0a80-138">Event type</span></span></th>
<th><span data-ttu-id="d0a80-139">Spuštění</span><span class="sxs-lookup"><span data-stu-id="d0a80-139">Execution</span></span></th>
<th><span data-ttu-id="d0a80-140">Blokování události</span><span class="sxs-lookup"><span data-stu-id="d0a80-140">Event blocking</span></span></th>
<th><span data-ttu-id="d0a80-141">Odkaz na dokument</span><span class="sxs-lookup"><span data-stu-id="d0a80-141">Document reference</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="d0a80-142">Zásoby</span><span class="sxs-lookup"><span data-stu-id="d0a80-142">Inventory</span></span></td>
<td><span data-ttu-id="d0a80-143">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="d0a80-143">Not applicable</span></span></td>
<td><span data-ttu-id="d0a80-144">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="d0a80-144">Not applicable</span></span></td>
<td><span data-ttu-id="d0a80-145">Žádné</span><span class="sxs-lookup"><span data-stu-id="d0a80-145">None</span></span></td>
<td><span data-ttu-id="d0a80-146">Vše</span><span class="sxs-lookup"><span data-stu-id="d0a80-146">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="d0a80-147">Prodeje</span><span class="sxs-lookup"><span data-stu-id="d0a80-147">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="d0a80-148">Proces vyskladnění je naplánován.</span><span class="sxs-lookup"><span data-stu-id="d0a80-148">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="d0a80-149">Před</span><span class="sxs-lookup"><span data-stu-id="d0a80-149">Before</span></span></td>
<td><span data-ttu-id="d0a80-150">Žádné</span><span class="sxs-lookup"><span data-stu-id="d0a80-150">None</span></span></td>
<td rowspan="22"><span data-ttu-id="d0a80-151">Specifické ID, Skupina nebo Vše</span><span class="sxs-lookup"><span data-stu-id="d0a80-151">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d0a80-152">Proces vyskladnění</span><span class="sxs-lookup"><span data-stu-id="d0a80-152">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d0a80-153">Dodací list</span><span class="sxs-lookup"><span data-stu-id="d0a80-153">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d0a80-154">Faktura</span><span class="sxs-lookup"><span data-stu-id="d0a80-154">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d0a80-155">Dodací list</span><span class="sxs-lookup"><span data-stu-id="d0a80-155">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="d0a80-156">Před</span><span class="sxs-lookup"><span data-stu-id="d0a80-156">Before</span></span></td>
<td><span data-ttu-id="d0a80-157">Žádné</span><span class="sxs-lookup"><span data-stu-id="d0a80-157">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d0a80-158">Dodací list</span><span class="sxs-lookup"><span data-stu-id="d0a80-158">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d0a80-159">Faktura</span><span class="sxs-lookup"><span data-stu-id="d0a80-159">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="d0a80-160">Nákup</span><span class="sxs-lookup"><span data-stu-id="d0a80-160">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="d0a80-161">Příjemka</span><span class="sxs-lookup"><span data-stu-id="d0a80-161">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="d0a80-162">Před</span><span class="sxs-lookup"><span data-stu-id="d0a80-162">Before</span></span></td>
<td><span data-ttu-id="d0a80-163">Žádné</span><span class="sxs-lookup"><span data-stu-id="d0a80-163">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d0a80-164">Příjemka</span><span class="sxs-lookup"><span data-stu-id="d0a80-164">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d0a80-165">Příjemka produktu</span><span class="sxs-lookup"><span data-stu-id="d0a80-165">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d0a80-166">Faktura</span><span class="sxs-lookup"><span data-stu-id="d0a80-166">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d0a80-167">Po</span><span class="sxs-lookup"><span data-stu-id="d0a80-167">After</span></span></td>
<td><span data-ttu-id="d0a80-168">Žádné</span><span class="sxs-lookup"><span data-stu-id="d0a80-168">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d0a80-169">Příjemka produktu</span><span class="sxs-lookup"><span data-stu-id="d0a80-169">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d0a80-170">Faktura</span><span class="sxs-lookup"><span data-stu-id="d0a80-170">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d0a80-171">Registrace</span><span class="sxs-lookup"><span data-stu-id="d0a80-171">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="d0a80-172">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="d0a80-172">Not applicable</span></span></td>
<td><span data-ttu-id="d0a80-173">Žádné</span><span class="sxs-lookup"><span data-stu-id="d0a80-173">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d0a80-174">Příjemka produktu</span><span class="sxs-lookup"><span data-stu-id="d0a80-174">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d0a80-175">Faktura</span><span class="sxs-lookup"><span data-stu-id="d0a80-175">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="d0a80-176">Příjemka produktu</span><span class="sxs-lookup"><span data-stu-id="d0a80-176">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="d0a80-177">Před</span><span class="sxs-lookup"><span data-stu-id="d0a80-177">Before</span></span></td>
<td><span data-ttu-id="d0a80-178">Žádné</span><span class="sxs-lookup"><span data-stu-id="d0a80-178">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d0a80-179">Příjemka produktu</span><span class="sxs-lookup"><span data-stu-id="d0a80-179">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d0a80-180">Faktura</span><span class="sxs-lookup"><span data-stu-id="d0a80-180">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d0a80-181">Po</span><span class="sxs-lookup"><span data-stu-id="d0a80-181">After</span></span></td>
<td><span data-ttu-id="d0a80-182">Žádné</span><span class="sxs-lookup"><span data-stu-id="d0a80-182">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d0a80-183">Faktura</span><span class="sxs-lookup"><span data-stu-id="d0a80-183">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="d0a80-184">Výroba</span><span class="sxs-lookup"><span data-stu-id="d0a80-184">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="d0a80-185">Registrace</span><span class="sxs-lookup"><span data-stu-id="d0a80-185">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="d0a80-186">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="d0a80-186">Not applicable</span></span></td>
<td><span data-ttu-id="d0a80-187">Žádné</span><span class="sxs-lookup"><span data-stu-id="d0a80-187">None</span></span></td>
<td rowspan="12"><span data-ttu-id="d0a80-188">Vše</span><span class="sxs-lookup"><span data-stu-id="d0a80-188">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d0a80-189">Ohlásit jako dokončené</span><span class="sxs-lookup"><span data-stu-id="d0a80-189">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d0a80-190">Konec</span><span class="sxs-lookup"><span data-stu-id="d0a80-190">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="d0a80-191">Ohlásit jako dokončené</span><span class="sxs-lookup"><span data-stu-id="d0a80-191">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="d0a80-192">Před</span><span class="sxs-lookup"><span data-stu-id="d0a80-192">Before</span></span></td>
<td><span data-ttu-id="d0a80-193">Žádné</span><span class="sxs-lookup"><span data-stu-id="d0a80-193">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d0a80-194">Ohlásit jako dokončené</span><span class="sxs-lookup"><span data-stu-id="d0a80-194">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d0a80-195">Konec</span><span class="sxs-lookup"><span data-stu-id="d0a80-195">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d0a80-196">Po</span><span class="sxs-lookup"><span data-stu-id="d0a80-196">After</span></span></td>
<td><span data-ttu-id="d0a80-197">Žádné</span><span class="sxs-lookup"><span data-stu-id="d0a80-197">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d0a80-198">Konec</span><span class="sxs-lookup"><span data-stu-id="d0a80-198">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="d0a80-199">Karanténa</span><span class="sxs-lookup"><span data-stu-id="d0a80-199">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="d0a80-200">Ohlásit jako dokončené</span><span class="sxs-lookup"><span data-stu-id="d0a80-200">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="d0a80-201">Před</span><span class="sxs-lookup"><span data-stu-id="d0a80-201">Before</span></span></td>
<td><span data-ttu-id="d0a80-202">Ohlásit jako dokončené</span><span class="sxs-lookup"><span data-stu-id="d0a80-202">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d0a80-203">Konec</span><span class="sxs-lookup"><span data-stu-id="d0a80-203">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d0a80-204">Po</span><span class="sxs-lookup"><span data-stu-id="d0a80-204">After</span></span></td>
<td><span data-ttu-id="d0a80-205">Konec</span><span class="sxs-lookup"><span data-stu-id="d0a80-205">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d0a80-206">Konec</span><span class="sxs-lookup"><span data-stu-id="d0a80-206">End</span></span></td>
<td><span data-ttu-id="d0a80-207">Před</span><span class="sxs-lookup"><span data-stu-id="d0a80-207">Before</span></span></td>
<td><span data-ttu-id="d0a80-208">Konec</span><span class="sxs-lookup"><span data-stu-id="d0a80-208">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d0a80-209">Operace postupu</span><span class="sxs-lookup"><span data-stu-id="d0a80-209">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="d0a80-210">Ohlásit jako dokončené</span><span class="sxs-lookup"><span data-stu-id="d0a80-210">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="d0a80-211">Před</span><span class="sxs-lookup"><span data-stu-id="d0a80-211">Before</span></span></td>
<td><span data-ttu-id="d0a80-212">Žádné</span><span class="sxs-lookup"><span data-stu-id="d0a80-212">None</span></span></td>
<td rowspan="3"><span data-ttu-id="d0a80-213">Specifické ID, Skupina nebo Vše a Podle prostředku, Skupina nebo Vše</span><span class="sxs-lookup"><span data-stu-id="d0a80-213">Specific ID, Group, or All, and Resource specific, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d0a80-214">Ohlásit jako dokončené</span><span class="sxs-lookup"><span data-stu-id="d0a80-214">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d0a80-215">Po</span><span class="sxs-lookup"><span data-stu-id="d0a80-215">After</span></span></td>
<td><span data-ttu-id="d0a80-216">Žádné</span><span class="sxs-lookup"><span data-stu-id="d0a80-216">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d0a80-217">Výroba vedlejších produktů</span><span class="sxs-lookup"><span data-stu-id="d0a80-217">Co-product production</span></span></td>
<td><span data-ttu-id="d0a80-218">Registrace</span><span class="sxs-lookup"><span data-stu-id="d0a80-218">Registration</span></span></td>
<td><span data-ttu-id="d0a80-219">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="d0a80-219">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d0a80-220">Žádné</span><span class="sxs-lookup"><span data-stu-id="d0a80-220">None</span></span></td>
<td rowspan="3"><span data-ttu-id="d0a80-221">Vše</span><span class="sxs-lookup"><span data-stu-id="d0a80-221">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d0a80-222">Ohlásit jako dokončené</span><span class="sxs-lookup"><span data-stu-id="d0a80-222">Report as finished</span></span></td>
<td><span data-ttu-id="d0a80-223">Před</span><span class="sxs-lookup"><span data-stu-id="d0a80-223">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d0a80-224">Po</span><span class="sxs-lookup"><span data-stu-id="d0a80-224">After</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d0a80-225">V následující tabulce jsou uvedeny další informace o způsobu, jak lze generovat objednávky kvality pro určité typy procesů.</span><span class="sxs-lookup"><span data-stu-id="d0a80-225">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>
<div class="tableSection">

<table>
<tbody>
<tr>
<th><span data-ttu-id="d0a80-226">Typ procesu</span><span class="sxs-lookup"><span data-stu-id="d0a80-226">Type of process</span></span></th>
<th><span data-ttu-id="d0a80-227">Kdy lze objednávku kvality generovat automaticky</span><span class="sxs-lookup"><span data-stu-id="d0a80-227">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="d0a80-228">Kdy lze objednávku kvality generovat v případě, že je vyžadován destrukční test</span><span class="sxs-lookup"><span data-stu-id="d0a80-228">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="d0a80-229">Informace o podmínkách</span><span class="sxs-lookup"><span data-stu-id="d0a80-229">Condition information</span></span></th>
<th><span data-ttu-id="d0a80-230">Informace o ručním generování</span><span class="sxs-lookup"><span data-stu-id="d0a80-230">Manual generation information</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="d0a80-231">Nákupní objednávka</span><span class="sxs-lookup"><span data-stu-id="d0a80-231">Purchase order</span></span></td>
<td><span data-ttu-id="d0a80-232">Před tím nebo po tom, co je příjemka produktu pro přijatý materiál zaúčtována</span><span class="sxs-lookup"><span data-stu-id="d0a80-232">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="d0a80-233">Po tom, co je příjemka produktu pro přijatý materiál zaúčtována, protože materiál musí být k dispozici pro destrukční testy</span><span class="sxs-lookup"><span data-stu-id="d0a80-233">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="d0a80-234">Požadavek pro objednávku kvality se může týkat určitého pracoviště, položky, dodavatele nebo kombinace těchto podmínek.</span><span class="sxs-lookup"><span data-stu-id="d0a80-234">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="d0a80-235">Ručně vygenerovaná objednávka kvality, která odkazuje na nákupní objednávku, může použít informace ze záznamu o přidružení kvality, jako je plán testování vzorku.</span><span class="sxs-lookup"><span data-stu-id="d0a80-235">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d0a80-236">Karanténní příkaz</span><span class="sxs-lookup"><span data-stu-id="d0a80-236">Quarantine order</span></span></td>
<td><span data-ttu-id="d0a80-237">Před tím nebo po tom, co je karanténní příkaz vykázán jako dokončený nebo ukončený</span><span class="sxs-lookup"><span data-stu-id="d0a80-237">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="d0a80-238">Objednávky kvality, které vyžadují provedení destrukčních testů, nelze generovat.</span><span class="sxs-lookup"><span data-stu-id="d0a80-238">Quality orders that require destructive tests can&#39;t be generated.</span></span> <span data-ttu-id="d0a80-239">Předpokládá se, že funkce karanténního příkazu zpracovává likvidaci materiálu, který je zničen.</span><span class="sxs-lookup"><span data-stu-id="d0a80-239">It&#39;s assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="d0a80-240">Požadavek pro objednávku kvality se může týkat určitého pracoviště, položky, dodavatele nebo kombinace těchto podmínek.</span><span class="sxs-lookup"><span data-stu-id="d0a80-240">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="d0a80-241">Ručně vygenerovaná objednávka kvality, která odkazuje na karanténní příkaz, může použít informace ze záznamu o přidružení kvality, jako je plán testování vzorku.</span><span class="sxs-lookup"><span data-stu-id="d0a80-241">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d0a80-242">Prodejní objednávka</span><span class="sxs-lookup"><span data-stu-id="d0a80-242">Sales order</span></span></td>
<td><span data-ttu-id="d0a80-243">Před naplánovaným procesem vyskladnění nebo aktualizací dodacího listu pro položky, které byly právě dodány</span><span class="sxs-lookup"><span data-stu-id="d0a80-243">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="d0a80-244">Při jakémkoli kroku</span><span class="sxs-lookup"><span data-stu-id="d0a80-244">At any step</span></span></td>
<td><span data-ttu-id="d0a80-245">Požadavek pro objednávku kvality se může týkat určitého pracoviště, položky, odběratele nebo kombinace těchto podmínek.</span><span class="sxs-lookup"><span data-stu-id="d0a80-245">The requirement for a quality order can reflect a particular site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="d0a80-246">Ručně vygenerovaná objednávka kvality, která odkazuje na prodejní objednávku, může použít informace ze záznamu o přidružení kvality, jako je plán testování vzorku.</span><span class="sxs-lookup"><span data-stu-id="d0a80-246">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d0a80-247">Výrobní zakázka</span><span class="sxs-lookup"><span data-stu-id="d0a80-247">Production order</span></span></td>
<td><span data-ttu-id="d0a80-248">Před tím nebo po tom, co je vykázáno dokončené množství pro výrobní zakázku</span><span class="sxs-lookup"><span data-stu-id="d0a80-248">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="d0a80-249">Po tom, co je vykázáno dokončené množství pro výrobní zakázku</span><span class="sxs-lookup"><span data-stu-id="d0a80-249">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="d0a80-250">Požadavek pro objednávku kvality se může týkat určitého pracoviště, položky nebo kombinace těchto podmínek.</span><span class="sxs-lookup"><span data-stu-id="d0a80-250">The requirement for a quality order can reflect a particular site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="d0a80-251">Ručně vygenerovaná objednávka kvality, která odkazuje na výrobní zakázku, může použít informace ze záznamu o přidružení kvality, jako je plán testování vzorku.</span><span class="sxs-lookup"><span data-stu-id="d0a80-251">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d0a80-252">Výrobní zakázka s operací postupu</span><span class="sxs-lookup"><span data-stu-id="d0a80-252">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="d0a80-253">Před tím nebo po tom, co je dokončeno ohlášení pro operaci</span><span class="sxs-lookup"><span data-stu-id="d0a80-253">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="d0a80-254">Po tom, co je pro poslední operaci dokončeno ohlášení výrobní zakázky</span><span class="sxs-lookup"><span data-stu-id="d0a80-254">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="d0a80-255">Požadavek pro objednávku kvality se může týkat určitého pracoviště, položky, provozního prostředku nebo kombinace těchto podmínek.</span><span class="sxs-lookup"><span data-stu-id="d0a80-255">The requirement for a quality order can reflect a particular, site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="d0a80-256">Ručně vygenerovaná objednávka kvality, která odkazuje na operaci postupu, může použít informace ze záznamu o přidružení kvality, jako je plán testování vzorku.</span><span class="sxs-lookup"><span data-stu-id="d0a80-256">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d0a80-257">Zásoby</span><span class="sxs-lookup"><span data-stu-id="d0a80-257">Inventory</span></span></td>
<td><span data-ttu-id="d0a80-258">Objednávku kvality nelze automaticky generovat pro transakci v deníku zásob ani pro transakce převodních příkazů.</span><span class="sxs-lookup"><span data-stu-id="d0a80-258">A quality order cannot be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="d0a80-259">Objednávku kvality je možné vytvořit ručně pro množství položky na skladě.</span><span class="sxs-lookup"><span data-stu-id="d0a80-259">A quality order must be created manually for an item&#39;s inventory quantity.</span></span> <span data-ttu-id="d0a80-260">Jsou vyžadovány fyzické zásoby na skladě.</span><span class="sxs-lookup"><span data-stu-id="d0a80-260">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>

## <a name="quality-management-pages"></a><span data-ttu-id="d0a80-261">Stránky modulu Správa kvality</span><span class="sxs-lookup"><span data-stu-id="d0a80-261">Quality management pages</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d0a80-262">Strana</span><span class="sxs-lookup"><span data-stu-id="d0a80-262">Page</span></span></th>
<th><span data-ttu-id="d0a80-263">Popis</span><span class="sxs-lookup"><span data-stu-id="d0a80-263">Description</span></span></th>
<th><span data-ttu-id="d0a80-264">Příklad</span><span class="sxs-lookup"><span data-stu-id="d0a80-264">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d0a80-265">Přiřazení kvality</span><span class="sxs-lookup"><span data-stu-id="d0a80-265">Quality associations</span></span></td>
<td><span data-ttu-id="d0a80-266">Přečtěte si předchozí část tohoto článku.</span><span class="sxs-lookup"><span data-stu-id="d0a80-266">See the previous sections of this article.</span></span></td>
<td><span data-ttu-id="d0a80-267">Přidružení kvality určuje pro vygenerovanou objednávku kvality tyto informace:</span><span class="sxs-lookup"><span data-stu-id="d0a80-267">A quality association defines all the following information for a quality order that is generated:</span></span>
<ul>
<li><span data-ttu-id="d0a80-268">Událost transakce</span><span class="sxs-lookup"><span data-stu-id="d0a80-268">The transaction event</span></span></li>
<li><span data-ttu-id="d0a80-269">Sada testů, které je nutné u položky vykonat</span><span class="sxs-lookup"><span data-stu-id="d0a80-269">The set of tests that must be performed on the items</span></span></li>
<li><span data-ttu-id="d0a80-270">Přijatelná úroveň kvality</span><span class="sxs-lookup"><span data-stu-id="d0a80-270">The AQL</span></span></li>
<li><span data-ttu-id="d0a80-271">Plán vzorkování</span><span class="sxs-lookup"><span data-stu-id="d0a80-271">The sampling plan</span></span></li>
</ul>
<span data-ttu-id="d0a80-272">Přiřazení kvality je nutné definovat pro každou variantu obchodního procesu, který vyžaduje automatické generování objednávky kvality.</span><span class="sxs-lookup"><span data-stu-id="d0a80-272">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="d0a80-273">Objednávky kvality lze generovat například v obchodních procesech pro nákupní objednávky, karanténní příkazy, prodejní objednávky a výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="d0a80-273">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d0a80-274">Testy</span><span class="sxs-lookup"><span data-stu-id="d0a80-274">Tests</span></span></td>
<td><span data-ttu-id="d0a80-275">Tuto stránku použijte k definování a prohlížení individuálních testů, které zjišťují, zda vaše produkty splňují specifikace kvality.</span><span class="sxs-lookup"><span data-stu-id="d0a80-275">Use this page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="d0a80-276">Ke skupině testů můžete přiřadit jeden nebo více individuálních testů.</span><span class="sxs-lookup"><span data-stu-id="d0a80-276">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="d0a80-277">V tomto případě zadáte také informace specifické pro daný test, jako jsou například přijatelné hodnoty měření.</span><span class="sxs-lookup"><span data-stu-id="d0a80-277">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="d0a80-278">Hodnoty měření se používají k testování množství a testovací proměnné slouží pro testy kvality.</span><span class="sxs-lookup"><span data-stu-id="d0a80-278">Measurement values are used for quantitative tests, and test variables are used for qualitative tests.</span></span>
<ul>
<li><span data-ttu-id="d0a80-279">Kvantitativní test má typ testu <strong>Celé číslo</strong> nebo <strong>Zlomek</strong> a také má určenou měrnou jednotku.</span><span class="sxs-lookup"><span data-stu-id="d0a80-279">A quantitative test has a test type of <strong>Integer</strong> or <strong>Fraction</strong>, and also has a designated unit of measure.</span></span> <span data-ttu-id="d0a80-280">Specifikace kvality a výsledky testu jsou vyjádřeny jako čísla.</span><span class="sxs-lookup"><span data-stu-id="d0a80-280">Quality specifications and test results are expressed as numbers.</span></span></li>
<li><span data-ttu-id="d0a80-281">V případě testu kvality se jedná o test typu <strong>Parametr</strong>.</span><span class="sxs-lookup"><span data-stu-id="d0a80-281">A qualitative test has a test type of <strong>Option</strong>.</span></span> <span data-ttu-id="d0a80-282">Testy kvality vyžadují další informace o měřených testovacích proměnných a o výčtu jejich hodnot.</span><span class="sxs-lookup"><span data-stu-id="d0a80-282">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="d0a80-283">Specifikace kvality a výsledky testu jsou vyjádřeny v závislosti na výstupu.</span><span class="sxs-lookup"><span data-stu-id="d0a80-283">Quality specifications and test results are expressed according to an outcome.</span></span></li>
</ul></td>
<td><span data-ttu-id="d0a80-284">Výrobní společnost provádí dva testy na zakoupeném materiálu: kvantitativní test ohledně kvality materiálu a test kvality ohledně poškození balení.</span><span class="sxs-lookup"><span data-stu-id="d0a80-284">A manufacturing company performs two tests on purchased material: a quantitative test about material quality and a qualitative test about packaging damage.</span></span> <span data-ttu-id="d0a80-285">Tato společnost definuje další informace ohledně kvalitativního testu s cílem identifikovat testovací proměnnou (poškozené balení) a její výstupní hodnoty.</span><span class="sxs-lookup"><span data-stu-id="d0a80-285">The company defines additional information about the qualitative test to identify the test variable (damaged packaging) and its outcomes.</span></span> <span data-ttu-id="d0a80-286">Společnost používá stránku <strong>Testovací skupiny</strong> k přiřazení dvou testů do skupiny testů a k určení informací o daném testu.</span><span class="sxs-lookup"><span data-stu-id="d0a80-286">The company uses the <strong>Test groups</strong> page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="d0a80-287">Testovací skupina je přiřazena k objednávce kvality, takže daná společnost může vytvořit sestavu pro dané dva testy.</span><span class="sxs-lookup"><span data-stu-id="d0a80-287">The test group is assigned to a quality order, so that the company can report test results for the two tests.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d0a80-288">Testovací skupiny</span><span class="sxs-lookup"><span data-stu-id="d0a80-288">Test groups</span></span></td>
<td><span data-ttu-id="d0a80-289">Tato stránka slouží k nastavení, úpravě a zobrazení testovacích skupin a jednotlivých testů přiřazených testovací skupině.</span><span class="sxs-lookup"><span data-stu-id="d0a80-289">Use this page to set up, edit, and view test groups and the individual tests that are assigned to a test group.</span></span> <span data-ttu-id="d0a80-290">V horním podokně jsou zobrazeny testovací skupiny a v dolním podokně jsou zobrazeny testy, které jsou přiřazené vybrané testovací skupině.</span><span class="sxs-lookup"><span data-stu-id="d0a80-290">The upper pane displays test groups, and the lower pane displays the tests that are assigned to a selected test group.</span></span> <span data-ttu-id="d0a80-291">Každé testovací skupině můžete přiřadit několik zásad, jako například plán vzorkování, přijatelnou úroveň kvality a požadavek na destrukční testy.</span><span class="sxs-lookup"><span data-stu-id="d0a80-291">You assign several policies to a test group, such as a sampling plan, an AQL, and the requirement for destructive testing.</span></span> <span data-ttu-id="d0a80-292">Při přiřazení jednotlivého testu do skupiny testů definujete další informace, jako jsou například pořadí, dokumenty nebo data platnosti.</span><span class="sxs-lookup"><span data-stu-id="d0a80-292">When you assign an individual test to a test group, you define additional information, such as the sequence, documents, and validity dates.</span></span> <span data-ttu-id="d0a80-293">Pro kvantitativní test definujete také informace o přijatelných hodnotách měření.</span><span class="sxs-lookup"><span data-stu-id="d0a80-293">For a quantitative test, the information that you define also includes the acceptable measurement values.</span></span> <span data-ttu-id="d0a80-294">Informace o testu kvality obsahují také testovací proměnné a výchozí výstup.</span><span class="sxs-lookup"><span data-stu-id="d0a80-294">For a qualitative test, the information includes the test variable and default outcome.</span></span> <span data-ttu-id="d0a80-295">Skupina testů přiřazená objednávce kvality určuje výchozí sadu testů, které je nutné na určených položkách vykonat.</span><span class="sxs-lookup"><span data-stu-id="d0a80-295">The test group that is assigned to a quality order defines the default set of tests that must be performed on the specified item.</span></span> <span data-ttu-id="d0a80-296">Testy však můžete přidat, odstranit nebo změnit na objednávce kvality.</span><span class="sxs-lookup"><span data-stu-id="d0a80-296">However, you can add, delete, or change tests on the quality order.</span></span> <span data-ttu-id="d0a80-297">Výsledky testu jsou uvedeny pro všechny testy v objednávce kvality.</span><span class="sxs-lookup"><span data-stu-id="d0a80-297">Test results are reported for each test on a quality order.</span></span></td>
<td><span data-ttu-id="d0a80-298">Výrobní společnost má definované testovací skupiny pro každou variantu pokynů týkajících se kvality.</span><span class="sxs-lookup"><span data-stu-id="d0a80-298">A manufacturing company defines a test group for each variation of its quality guidelines.</span></span> <span data-ttu-id="d0a80-299">Různé testovací skupiny odrážejí rozdíly v plánech vzorkování, v sadách testů, které je nutné provádět dohromady, v přijatelné úrovni kvality i v dalších činitelích.</span><span class="sxs-lookup"><span data-stu-id="d0a80-299">The various test groups reflect differences in the sampling plans, the sets of tests that must be performed together, the AQL, and other factors.</span></span> <span data-ttu-id="d0a80-300">Pro kvantitativní testy existují také rozdíly v přijatelných hodnotách měření.</span><span class="sxs-lookup"><span data-stu-id="d0a80-300">For quantitative tests, there are also differences in the acceptable measurement values.</span></span> <span data-ttu-id="d0a80-301">K uplatnění pokynů týkajících se kvality přiřadí společnost na stránce <strong>Přidružení kvality</strong> každé testovací skupině pravidlo automatického generování objednávek kvality a také přiřadí skupiny testů k objednávce kvality, který byla vytvořena ručně.</span><span class="sxs-lookup"><span data-stu-id="d0a80-301">To enforce its quality guidelines, the company assigns a test group to each rule for automatically generating quality orders on the <strong>Quality associations</strong> page, and also assigns a test group to quality orders that are manually created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d0a80-302">Skupiny kvality položek</span><span class="sxs-lookup"><span data-stu-id="d0a80-302">Item quality groups</span></span></td>
<td><span data-ttu-id="d0a80-303">Tato stránka slouží k nastavení, úpravě a zobrazení položek zařazených do skupin kvality, které jsou přiřazeny položce.</span><span class="sxs-lookup"><span data-stu-id="d0a80-303">Use this page to set up, edit, and view the items that are assigned to a quality group or the quality groups that are assigned to an item.</span></span> <span data-ttu-id="d0a80-304">Skupina kvality představuje společné požadavky na testování položek.</span><span class="sxs-lookup"><span data-stu-id="d0a80-304">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="d0a80-305">Po určení požadavků na testování na stránce <strong>Testovací skupiny</strong> můžete definovat pravidla pro automatické generování objednávek kvality.</span><span class="sxs-lookup"><span data-stu-id="d0a80-305">After you define the test requirements on the <strong>Test groups</strong> page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="d0a80-306">Proces můžete zjednodušit tak, že nebudete definovat pravidla pro jednotlivé položky.</span><span class="sxs-lookup"><span data-stu-id="d0a80-306">To simplify the process, you don&#39;t define rules for individual items.</span></span> <span data-ttu-id="d0a80-307">Namísto toho na stránce <strong>Přidružení kvality</strong> určíte pravidla pro skupinu kvality.</span><span class="sxs-lookup"><span data-stu-id="d0a80-307">Instead, you define rules for a quality group, by using the <strong>Quality associations</strong> page.</span></span> <span data-ttu-id="d0a80-308">Pro vybranou skupinu kvality můžete také použít stránku <strong>Skupiny kvality položek</strong> a přiřadit k této skupině příslušné položky.</span><span class="sxs-lookup"><span data-stu-id="d0a80-308">You can also use the <strong>Item quality groups</strong> page for a selected quality group to assign relevant items to that group.</span></span> <span data-ttu-id="d0a80-309">Pro vybranou položku můžete také použít stránku <strong>Skupiny kvality položek</strong> a přiřadit příslušnou skupiny kvality příslušné položce.</span><span class="sxs-lookup"><span data-stu-id="d0a80-309">You can also use the <strong>Item quality groups</strong> page for a selected item to assign relevant quality groups to that item.</span></span></td>
<td><span data-ttu-id="d0a80-310">Výrobní společnost nakupuje různé suroviny, které při vstupní kontrole podléhají stejným požadavkům na testování.</span><span class="sxs-lookup"><span data-stu-id="d0a80-310">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="d0a80-311">Společnost definuje skupinu kvality a přiřadí čísla položek, které jsou přidruženy k surovinám, do této skupiny.</span><span class="sxs-lookup"><span data-stu-id="d0a80-311">The company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="d0a80-312">Později společnosti zakoupí nový typ suroviny, který má stejné požadavky na testování.</span><span class="sxs-lookup"><span data-stu-id="d0a80-312">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="d0a80-313">Namísto vytvoření nových požadavků na testování pro nový materiál společnost přidá číslo položky pro nový materiál do stávající skupiny kvality.</span><span class="sxs-lookup"><span data-stu-id="d0a80-313">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span> <span data-ttu-id="d0a80-314">Stejná výrobní společnost vyrábí také položky, na které jsou kladeny stejné požadavky na testování, a expeduje položky, které před odesláním podléhají stejné kontrole.</span><span class="sxs-lookup"><span data-stu-id="d0a80-314">The same manufacturing company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="d0a80-315">Společnost definuje další dvě skupiny kvality a do každé skupiny zařadí příslušné položky.</span><span class="sxs-lookup"><span data-stu-id="d0a80-315">The company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d0a80-316">Testovací proměnné</span><span class="sxs-lookup"><span data-stu-id="d0a80-316">Test variables</span></span></td>
<td><span data-ttu-id="d0a80-317">Tato stránka slouží k určení a zobrazení proměnných spojených s testem kvality.</span><span class="sxs-lookup"><span data-stu-id="d0a80-317">Use this page to define and view the variables that are associated with a qualitative test.</span></span> <span data-ttu-id="d0a80-318">Pro každou proměnnou určete výčet výstupních hodnot, které reprezentují možné volby.</span><span class="sxs-lookup"><span data-stu-id="d0a80-318">For each variable, you define enumerated outcomes that represent the possible options.</span></span> <span data-ttu-id="d0a80-319">Na stránce <strong>Testy</strong> určete testy.</span><span class="sxs-lookup"><span data-stu-id="d0a80-319">You define tests on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="d0a80-320">U testů kvality je nutné nastavit typ testu na hodnotu <strong>Možnost</strong>.</span><span class="sxs-lookup"><span data-stu-id="d0a80-320">For qualitative tests, you must set the test type to <strong>Option</strong>.</span></span> <span data-ttu-id="d0a80-321">Na stránce <strong>Testovací skupiny</strong> přiřaďte testovací proměnnou k jednotlivému testu.</span><span class="sxs-lookup"><span data-stu-id="d0a80-321">Use the <strong>Test groups</strong> page to assign a test variable to an individual test.</span></span></td>
<td><span data-ttu-id="d0a80-322">Společnost vyrábějící cukrovinky používá kontrolní test pro dokončené výrobky.</span><span class="sxs-lookup"><span data-stu-id="d0a80-322">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="d0a80-323">Kontrolní test má několik proměnných.</span><span class="sxs-lookup"><span data-stu-id="d0a80-323">This inspection test has several variables.</span></span> <span data-ttu-id="d0a80-324">Jedna proměnná odpovídá chuti, přičemž možné výstupní hodnoty pro tuto proměnnou jsou „dobrá“ a „špatná“.</span><span class="sxs-lookup"><span data-stu-id="d0a80-324">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="d0a80-325">Druhá proměnná odpovídá barvě, přičemž možní výstupní hodnoty jsou „příliš tmavá“, „příliš světlá“ a „správná“.</span><span class="sxs-lookup"><span data-stu-id="d0a80-325">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d0a80-326">Výsledky testovacích proměnných</span><span class="sxs-lookup"><span data-stu-id="d0a80-326">Test variable outcomes</span></span></td>
<td><span data-ttu-id="d0a80-327">Na této stránce lze nastavit, upravit nebo zobrazit možné výsledky testů pro testovací proměnnou, která je přidružena k testu kvality.</span><span class="sxs-lookup"><span data-stu-id="d0a80-327">Use this page to set up, edit, and to view the possible test results for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="d0a80-328">Každé výstupní hodnotě přiřadíte stav <strong>úspěch</strong> nebo <strong>neúspěch</strong>.</span><span class="sxs-lookup"><span data-stu-id="d0a80-328">For each outcome, you assign a <strong>pass</strong> or <strong>fail</strong> status.</span></span> <span data-ttu-id="d0a80-329">Pro každý test kvality definovaný na stránce <strong>Testy</strong> je nutné definovat proměnnou a její výstupní hodnoty.</span><span class="sxs-lookup"><span data-stu-id="d0a80-329">You must define a variable and its outcomes for each qualitative test that is defined on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="d0a80-330">(U kvalitativních testů je typ testu nastaven na <strong>Volba</strong> na stránce <strong>Testy</strong>.) Pomocí stránky <strong>Skupiny testů</strong> přiřaďte proměnnou testu a výchozí výstup k samostatnému kvalitativnímu testu.</span><span class="sxs-lookup"><span data-stu-id="d0a80-330">(For qualitative tests, the test type is set to <strong>Option</strong> on the <strong>Tests</strong> page.) Use the <strong>Test groups</strong> page to assign a test variable and the default outcome to an individual qualitative test.</span></span></td>
<td><span data-ttu-id="d0a80-331">Společnost vyrábějící cukrovinky používá kontrolní test pro dokončené výrobky.</span><span class="sxs-lookup"><span data-stu-id="d0a80-331">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="d0a80-332">Kontrolní test má několik proměnných.</span><span class="sxs-lookup"><span data-stu-id="d0a80-332">This inspection test has of several variables.</span></span> <span data-ttu-id="d0a80-333">Jedna proměnná odpovídá chuti, přičemž možné výstupní hodnoty pro tuto proměnnou jsou „dobrá“ a „špatná“.</span><span class="sxs-lookup"><span data-stu-id="d0a80-333">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="d0a80-334">Druhá proměnná odpovídá barvě, přičemž možní výstupní hodnoty jsou „příliš tmavá“, „příliš světlá“ a „správná“.</span><span class="sxs-lookup"><span data-stu-id="d0a80-334">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span> <span data-ttu-id="d0a80-335">Ke každé výstupní hodnotě je přiřazen stav <strong>úspěch</strong> nebo <strong>neúspěch</strong>.</span><span class="sxs-lookup"><span data-stu-id="d0a80-335">A status of <strong>pass</strong> or <strong>fail</strong> is assigned to each outcome.</span></span> <span data-ttu-id="d0a80-336">Během kontrolního testu pro každou proměnnou kontrolor ohlásí výsledky testu výběrem některé z výstupních hodnot.</span><span class="sxs-lookup"><span data-stu-id="d0a80-336">During the inspection test for each variable, the inspector reports the test result by selecting one of the outcomes.</span></span></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="d0a80-337">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="d0a80-337">Additional resources</span></span>
--------

[<span data-ttu-id="d0a80-338">Procesy správy kvality</span><span class="sxs-lookup"><span data-stu-id="d0a80-338">Quality management processes</span></span>](quality-management-processes.md)

[<span data-ttu-id="d0a80-339">Povolení správy neshod</span><span class="sxs-lookup"><span data-stu-id="d0a80-339">Enabling nonconformance management</span></span>](enable-nonconformance-management.md)

