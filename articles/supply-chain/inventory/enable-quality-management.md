---
title: Přehled správy kvality
description: Toto téma popisuje, jak lze použít správu kvality v aplikaci Dynamics 365 Supply Chain Management za účelem zlepšení kvality produktu v rámci dodavatelsko-odběratelského řetězce.
author: perlynne
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e1d7828e6bb9a3684c1d76e2cfac96174a8dfbf4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4423885"
---
# <a name="quality-management-overview"></a><span data-ttu-id="1b9e6-103">Přehled správy kvality</span><span class="sxs-lookup"><span data-stu-id="1b9e6-103">Quality management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1b9e6-104">Toto téma popisuje, jak lze použít správu kvality v aplikaci Dynamics 365 Supply Chain Management za účelem zlepšení kvality produktu v rámci dodavatelsko-odběratelského řetězce.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-104">This topic describes how you can use quality management in Dynamics 365 Supply Chain Management to help improve product quality within your supply chain.</span></span>

<span data-ttu-id="1b9e6-105">Správa kvality pomáhá se správou doby oběhu objednávky při zpracování nevyhovujících produktů bez ohledu na místo jejich původu.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-105">Quality management can help you manage turnaround times when you handle nonconforming products, regardless of their point of origin.</span></span> <span data-ttu-id="1b9e6-106">Vzhledem k tomu, že typy diagnostiky jsou propojeny s vykazováním oprav, aplikace Supply Chain Management může naplánovat úlohy pro nápravu problémů a zabránění jejich opakování.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-106">Because diagnostic types are linked to correction reporting, Supply Chain Management can schedule tasks to correct problems and prevent them from recurring.</span></span>

<span data-ttu-id="1b9e6-107">Kromě funkcí pro správu neshod obsahuje moduly správy kvality také funkce pro sledování problémů podle jejich typu (včetně interních potíží) a pro určování krátkodobých a dlouhodobých řešení.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-107">In addition to functionality for managing nonconformance, quality management includes functionality for tracking issues by problem type (even internal problems), and for identifying solutions as short-term or long-term.</span></span> <span data-ttu-id="1b9e6-108">Statistické údaje o klíčových ukazatelů výkonnosti (KPI) nabízí náhled na historii předchozích potíží s neshodami a řešení, která byla použita k jejich nápravě.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-108">Statistics about key performance indicators (KPIs) provide insight into the history of previous nonconformance issues and the solutions that were used to correct them.</span></span> <span data-ttu-id="1b9e6-109">Historická data můžete použít ke kontrole účinnosti předchozích opatření pro zajištění kvality a k rozhodnutí o tom, zda tato opatření použít i v budoucnu.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-109">You can use historical data to review the effectiveness of previous quality measures and determine appropriate measures to use in the future.</span></span>

<span data-ttu-id="1b9e6-110">Při nastavování přidružení kvality může aplikace Supply Chain Management vygenerovat objednávky kvality pro různé obchodní procesy, události a podmínky.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-110">When you set up a quality association, Supply Chain Management can generate quality orders for various business processes, events, and conditions.</span></span> <span data-ttu-id="1b9e6-111">Přiřazení kvality může zahrnovat určitou položku, určitou skupinu položek nebo všechny položky.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-111">The quality association can cover a specific item, a specific group of items, or all items.</span></span>

## <a name="examples-of-the-use-of-quality-management"></a><span data-ttu-id="1b9e6-112">Příklady použití správy kvality</span><span class="sxs-lookup"><span data-stu-id="1b9e6-112">Examples of the use of quality management</span></span>
<span data-ttu-id="1b9e6-113">Správa kvality je flexibilní a lze ji implementovat různými způsoby, aby byly splněny požadavky konkrétních úrovní operací dodavatelsko-odběratelského řetězce.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-113">Quality management is flexible and can be implemented in various ways to meet the requirements of specific levels of supply chain operations.</span></span> <span data-ttu-id="1b9e6-114">V následujících příkladech jsou znázorněna možná použití těchto funkcí:</span><span class="sxs-lookup"><span data-stu-id="1b9e6-114">The following examples illustrate possible uses of these features:</span></span>

-   <span data-ttu-id="1b9e6-115">Automatické spuštění procesu řízení kvality na základě předem definovaných kritérií (při registraci nákupní objednávky od konkrétního dodavatele ve skladu).</span><span class="sxs-lookup"><span data-stu-id="1b9e6-115">Automatically start a quality control process, based on predefined criteria (upon warehouse registration of a purchase order from a specific vendor).</span></span>
-   <span data-ttu-id="1b9e6-116">Blokování zásob při inventuře zabraňuje použití neschválených zásob (úplné blokování množství nákupní objednávky).</span><span class="sxs-lookup"><span data-stu-id="1b9e6-116">Block inventory during inspection to prevent non-approved inventory from being used (full blocking of purchase order quantities).</span></span>
-   <span data-ttu-id="1b9e6-117">Použití vzorkování jako součásti přidružení k definici množství aktuálních fyzických zásob, které je nutné zkontrolovat.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-117">Use item sampling as part of a quality association to define the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="1b9e6-118">Vzorkování může být založeno na pevném množství, procentuální hodnotě nebo celé licenční značky.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-118">Sampling can be based on fixed quantities, a percentage, or full license plate.</span></span>

> [!NOTE]
> <span data-ttu-id="1b9e6-119">Funkce _Správa kvality pro procesy skladu_ rozšiřuje možnosti správy kvality.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-119">The _Quality management for warehouse processes_ feature extends the capabilities of quality management.</span></span> <span data-ttu-id="1b9e6-120">Používáte-li tuto funkci, přejděte do tématu [Správa kvality pro procesy skladu](quality-management-for-warehouses-processes.md), kde najdete příklady, jak povolit správu kvality.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-120">If you are using this feature, then see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md) for examples of how quality management works when it's enabled.</span></span>

-   <span data-ttu-id="1b9e6-121">Vytvořte objednávky kvality pro částečné příjmy.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-121">Create quality orders for partial receipts.</span></span> <span data-ttu-id="1b9e6-122">Abyste mohli vytvořit objednávku kvality, která je založena na množství fyzicky přijatém s objednávkou, je nutné zaškrtnout políčko **Na aktualizované množství** ve formuláři **Vzorkování položky**.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-122">To create a quality order that is based on the quantity that is physically received with an order, you must select the **Per updated quantity** check box on the **Item sampling** form.</span></span>
-   <span data-ttu-id="1b9e6-123">Vytvoření typů testu, které zahrnují minimální, maximální a cílové hodnoty testu, a vykonání testu kvality vůči množství s předdefinovanými ověřovacími výsledky.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-123">Create test types that include minimum, maximum, and target test values, and perform qualitative-versus-quantitative testing that has predefined validation results.</span></span>
-   <span data-ttu-id="1b9e6-124">Určení přijatelné úrovně kvality (AQL) pro řízení odchylek měření kvality.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-124">Specify an acceptable quality level (AQL) to control quality measure tolerances.</span></span>
-   <span data-ttu-id="1b9e6-125">Určení zdrojů vyžadovaných operací kontroly, jako je například prostor testu nebo testovací přístroje.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-125">Specify the resources that an inspection operation requires, such as a test area and test instruments.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="1b9e6-126">Práce s přidruženími kvality</span><span class="sxs-lookup"><span data-stu-id="1b9e6-126">Working with quality associations</span></span>
<span data-ttu-id="1b9e6-127">Obchodní proces, který používá přidružení kvality, může být přiřazen k různým zdrojovým dokumentům, jako například k nákupním objednávkám, prodejním objednávkám nebo výrobním zakázkám.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-127">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="1b9e6-128">Každý záznam o přidružení kvality určuje sadu testů, přijatelnou úroveň kvality a plán vzorkování, které platí pro vygenerované objednávky kvality.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-128">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="1b9e6-129">Je nutné definovat záznam o přidružení kvality pro každou variantu v obchodním procesu.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-129">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="1b9e6-130">Můžete například nastavit přidružení kvality, které vygeneruje objednávku kvality při aktualizaci příjemky produktu nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-130">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="1b9e6-131">V závislosti na nastavení plánu provedení může být samotný spouštěcí proces blokován, dokud existuje otevřená objednávka kvality, nebo mohou být blokovány další procesy, jako například fakturování nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-131">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order, or the next processes, such as purchase order invoicing, can be blocked.</span></span>

<span data-ttu-id="1b9e6-132">**Poznámka:** Pokud existují otevřené objednávky kvality, skladová množství jsou automaticky blokována před vydáním.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-132">**Note:** While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="1b9e6-133">V závislosti na nastavení **Úplné blokování** na stránce **Vzorkování položky** se množství rovná buď množství na objednávce kvality, nebo množství na řádku zdrojového dokumentu.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-133">Depending on the **Full blocking** setting on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span>

<span data-ttu-id="1b9e6-134">Pro určitý obchodní proces určuje záznam o přidružení kvality událost a podmínky, pro které je objednávka kvality generována.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-134">For a given business process, the quality association record identifies the event and the conditions that a quality order is generated for.</span></span> <span data-ttu-id="1b9e6-135">Podmínky mohou být specifické buď pro pracoviště, nebo pro právnickou osobu.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-135">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="1b9e6-136">Objednávku kvality, která zahrnuje destrukční testy, je možné generovat, jen když pro tuto událost existují zásoby.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-136">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="1b9e6-137">Následující příklady ilustrují způsob definování záznamu o přidružení kvality pro varianty každého obchodního procesu.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-137">The following examples illustrate how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="1b9e6-138">Pro každý příklad jsou v následující tabulce shrnuty události a podmínky, kterou jsou definovány v záznamu o přidružení kvality.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-138">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="1b9e6-139">Typ odkazu</span><span class="sxs-lookup"><span data-stu-id="1b9e6-139">Reference type</span></span></th>
<th><span data-ttu-id="1b9e6-140">Typ události</span><span class="sxs-lookup"><span data-stu-id="1b9e6-140">Event type</span></span></th>
<th><span data-ttu-id="1b9e6-141">Spuštění</span><span class="sxs-lookup"><span data-stu-id="1b9e6-141">Execution</span></span></th>
<th><span data-ttu-id="1b9e6-142">Blokování události</span><span class="sxs-lookup"><span data-stu-id="1b9e6-142">Event blocking</span></span></th>
<th><span data-ttu-id="1b9e6-143">Odkaz na dokument</span><span class="sxs-lookup"><span data-stu-id="1b9e6-143">Document reference</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="1b9e6-144">Zásoby</span><span class="sxs-lookup"><span data-stu-id="1b9e6-144">Inventory</span></span></td>
<td><span data-ttu-id="1b9e6-145">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="1b9e6-145">Not applicable</span></span></td>
<td><span data-ttu-id="1b9e6-146">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="1b9e6-146">Not applicable</span></span></td>
<td><span data-ttu-id="1b9e6-147">Žádné</span><span class="sxs-lookup"><span data-stu-id="1b9e6-147">None</span></span></td>
<td><span data-ttu-id="1b9e6-148">Vše</span><span class="sxs-lookup"><span data-stu-id="1b9e6-148">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="1b9e6-149">Prodeje</span><span class="sxs-lookup"><span data-stu-id="1b9e6-149">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="1b9e6-150">Proces vyskladnění je naplánován.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-150">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="1b9e6-151">Před</span><span class="sxs-lookup"><span data-stu-id="1b9e6-151">Before</span></span></td>
<td><span data-ttu-id="1b9e6-152">Žádné</span><span class="sxs-lookup"><span data-stu-id="1b9e6-152">None</span></span></td>
<td rowspan="22"><span data-ttu-id="1b9e6-153">Specifické ID, Skupina nebo Vše</span><span class="sxs-lookup"><span data-stu-id="1b9e6-153">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1b9e6-154">Proces vyskladnění</span><span class="sxs-lookup"><span data-stu-id="1b9e6-154">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1b9e6-155">Dodací list</span><span class="sxs-lookup"><span data-stu-id="1b9e6-155">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1b9e6-156">Faktura</span><span class="sxs-lookup"><span data-stu-id="1b9e6-156">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="1b9e6-157">Dodací list</span><span class="sxs-lookup"><span data-stu-id="1b9e6-157">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="1b9e6-158">Před</span><span class="sxs-lookup"><span data-stu-id="1b9e6-158">Before</span></span></td>
<td><span data-ttu-id="1b9e6-159">Žádné</span><span class="sxs-lookup"><span data-stu-id="1b9e6-159">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1b9e6-160">Dodací list</span><span class="sxs-lookup"><span data-stu-id="1b9e6-160">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1b9e6-161">Faktura</span><span class="sxs-lookup"><span data-stu-id="1b9e6-161">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="1b9e6-162">Nákup</span><span class="sxs-lookup"><span data-stu-id="1b9e6-162">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="1b9e6-163">Příjemka</span><span class="sxs-lookup"><span data-stu-id="1b9e6-163">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="1b9e6-164">Před</span><span class="sxs-lookup"><span data-stu-id="1b9e6-164">Before</span></span></td>
<td><span data-ttu-id="1b9e6-165">Žádné</span><span class="sxs-lookup"><span data-stu-id="1b9e6-165">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1b9e6-166">Příjemka</span><span class="sxs-lookup"><span data-stu-id="1b9e6-166">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1b9e6-167">Příjemka produktu</span><span class="sxs-lookup"><span data-stu-id="1b9e6-167">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1b9e6-168">Faktura</span><span class="sxs-lookup"><span data-stu-id="1b9e6-168">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="1b9e6-169">Po</span><span class="sxs-lookup"><span data-stu-id="1b9e6-169">After</span></span></td>
<td><span data-ttu-id="1b9e6-170">Žádné</span><span class="sxs-lookup"><span data-stu-id="1b9e6-170">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1b9e6-171">Příjemka produktu</span><span class="sxs-lookup"><span data-stu-id="1b9e6-171">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1b9e6-172">Faktura</span><span class="sxs-lookup"><span data-stu-id="1b9e6-172">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="1b9e6-173">Registrace</span><span class="sxs-lookup"><span data-stu-id="1b9e6-173">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="1b9e6-174">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="1b9e6-174">Not applicable</span></span></td>
<td><span data-ttu-id="1b9e6-175">Žádné</span><span class="sxs-lookup"><span data-stu-id="1b9e6-175">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1b9e6-176">Příjemka produktu</span><span class="sxs-lookup"><span data-stu-id="1b9e6-176">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1b9e6-177">Faktura</span><span class="sxs-lookup"><span data-stu-id="1b9e6-177">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="1b9e6-178">Příjemka produktu</span><span class="sxs-lookup"><span data-stu-id="1b9e6-178">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="1b9e6-179">Před</span><span class="sxs-lookup"><span data-stu-id="1b9e6-179">Before</span></span></td>
<td><span data-ttu-id="1b9e6-180">Žádné</span><span class="sxs-lookup"><span data-stu-id="1b9e6-180">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1b9e6-181">Příjemka produktu</span><span class="sxs-lookup"><span data-stu-id="1b9e6-181">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1b9e6-182">Faktura</span><span class="sxs-lookup"><span data-stu-id="1b9e6-182">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="1b9e6-183">Po</span><span class="sxs-lookup"><span data-stu-id="1b9e6-183">After</span></span></td>
<td><span data-ttu-id="1b9e6-184">Žádné</span><span class="sxs-lookup"><span data-stu-id="1b9e6-184">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1b9e6-185">Faktura</span><span class="sxs-lookup"><span data-stu-id="1b9e6-185">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="1b9e6-186">Výroba</span><span class="sxs-lookup"><span data-stu-id="1b9e6-186">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="1b9e6-187">Registrace</span><span class="sxs-lookup"><span data-stu-id="1b9e6-187">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="1b9e6-188">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="1b9e6-188">Not applicable</span></span></td>
<td><span data-ttu-id="1b9e6-189">Žádné</span><span class="sxs-lookup"><span data-stu-id="1b9e6-189">None</span></span></td>
<td rowspan="12"><span data-ttu-id="1b9e6-190">Vše</span><span class="sxs-lookup"><span data-stu-id="1b9e6-190">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1b9e6-191">Ohlásit jako dokončené</span><span class="sxs-lookup"><span data-stu-id="1b9e6-191">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1b9e6-192">Konec</span><span class="sxs-lookup"><span data-stu-id="1b9e6-192">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="1b9e6-193">Ohlásit jako dokončené</span><span class="sxs-lookup"><span data-stu-id="1b9e6-193">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="1b9e6-194">Před</span><span class="sxs-lookup"><span data-stu-id="1b9e6-194">Before</span></span></td>
<td><span data-ttu-id="1b9e6-195">Žádné</span><span class="sxs-lookup"><span data-stu-id="1b9e6-195">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1b9e6-196">Ohlásit jako dokončené</span><span class="sxs-lookup"><span data-stu-id="1b9e6-196">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1b9e6-197">Konec</span><span class="sxs-lookup"><span data-stu-id="1b9e6-197">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="1b9e6-198">Po</span><span class="sxs-lookup"><span data-stu-id="1b9e6-198">After</span></span></td>
<td><span data-ttu-id="1b9e6-199">Žádné</span><span class="sxs-lookup"><span data-stu-id="1b9e6-199">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1b9e6-200">Konec</span><span class="sxs-lookup"><span data-stu-id="1b9e6-200">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="1b9e6-201">Karanténa</span><span class="sxs-lookup"><span data-stu-id="1b9e6-201">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="1b9e6-202">Ohlásit jako dokončené</span><span class="sxs-lookup"><span data-stu-id="1b9e6-202">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="1b9e6-203">Před</span><span class="sxs-lookup"><span data-stu-id="1b9e6-203">Before</span></span></td>
<td><span data-ttu-id="1b9e6-204">Ohlásit jako dokončené</span><span class="sxs-lookup"><span data-stu-id="1b9e6-204">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1b9e6-205">Konec</span><span class="sxs-lookup"><span data-stu-id="1b9e6-205">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1b9e6-206">Po</span><span class="sxs-lookup"><span data-stu-id="1b9e6-206">After</span></span></td>
<td><span data-ttu-id="1b9e6-207">Konec</span><span class="sxs-lookup"><span data-stu-id="1b9e6-207">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1b9e6-208">Konec</span><span class="sxs-lookup"><span data-stu-id="1b9e6-208">End</span></span></td>
<td><span data-ttu-id="1b9e6-209">Před</span><span class="sxs-lookup"><span data-stu-id="1b9e6-209">Before</span></span></td>
<td><span data-ttu-id="1b9e6-210">Konec</span><span class="sxs-lookup"><span data-stu-id="1b9e6-210">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="1b9e6-211">Operace postupu</span><span class="sxs-lookup"><span data-stu-id="1b9e6-211">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="1b9e6-212">Ohlásit jako dokončené</span><span class="sxs-lookup"><span data-stu-id="1b9e6-212">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="1b9e6-213">Před</span><span class="sxs-lookup"><span data-stu-id="1b9e6-213">Before</span></span></td>
<td><span data-ttu-id="1b9e6-214">Žádné</span><span class="sxs-lookup"><span data-stu-id="1b9e6-214">None</span></span></td>
<td rowspan="3"><span data-ttu-id="1b9e6-215">Specifické ID, Skupina nebo Vše a Podle prostředku, Skupina nebo Vše</span><span class="sxs-lookup"><span data-stu-id="1b9e6-215">Specific ID, Group, or All, and Resource specific, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1b9e6-216">Ohlásit jako dokončené</span><span class="sxs-lookup"><span data-stu-id="1b9e6-216">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1b9e6-217">Po</span><span class="sxs-lookup"><span data-stu-id="1b9e6-217">After</span></span></td>
<td><span data-ttu-id="1b9e6-218">Žádné</span><span class="sxs-lookup"><span data-stu-id="1b9e6-218">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="1b9e6-219">Výroba vedlejších produktů</span><span class="sxs-lookup"><span data-stu-id="1b9e6-219">Co-product production</span></span></td>
<td><span data-ttu-id="1b9e6-220">Registrace</span><span class="sxs-lookup"><span data-stu-id="1b9e6-220">Registration</span></span></td>
<td><span data-ttu-id="1b9e6-221">Nelze použít</span><span class="sxs-lookup"><span data-stu-id="1b9e6-221">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="1b9e6-222">Žádné</span><span class="sxs-lookup"><span data-stu-id="1b9e6-222">None</span></span></td>
<td rowspan="3"><span data-ttu-id="1b9e6-223">Vše</span><span class="sxs-lookup"><span data-stu-id="1b9e6-223">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="1b9e6-224">Ohlásit jako dokončené</span><span class="sxs-lookup"><span data-stu-id="1b9e6-224">Report as finished</span></span></td>
<td><span data-ttu-id="1b9e6-225">Před</span><span class="sxs-lookup"><span data-stu-id="1b9e6-225">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1b9e6-226">Po</span><span class="sxs-lookup"><span data-stu-id="1b9e6-226">After</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1b9e6-227">V následující tabulce jsou uvedeny další informace o způsobu, jak lze generovat objednávky kvality pro určité typy procesů.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-227">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>
<div class="tableSection">

<table>
<tbody>
<tr>
<th><span data-ttu-id="1b9e6-228">Typ procesu</span><span class="sxs-lookup"><span data-stu-id="1b9e6-228">Type of process</span></span></th>
<th><span data-ttu-id="1b9e6-229">Kdy lze objednávku kvality generovat automaticky</span><span class="sxs-lookup"><span data-stu-id="1b9e6-229">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="1b9e6-230">Kdy lze objednávku kvality generovat v případě, že je vyžadován destrukční test</span><span class="sxs-lookup"><span data-stu-id="1b9e6-230">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="1b9e6-231">Informace o podmínkách</span><span class="sxs-lookup"><span data-stu-id="1b9e6-231">Condition information</span></span></th>
<th><span data-ttu-id="1b9e6-232">Informace o ručním generování</span><span class="sxs-lookup"><span data-stu-id="1b9e6-232">Manual generation information</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="1b9e6-233">Nákupní objednávka</span><span class="sxs-lookup"><span data-stu-id="1b9e6-233">Purchase order</span></span></td>
<td><span data-ttu-id="1b9e6-234">Před tím nebo po tom, co je příjemka produktu pro přijatý materiál zaúčtována</span><span class="sxs-lookup"><span data-stu-id="1b9e6-234">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="1b9e6-235">Po tom, co je příjemka produktu pro přijatý materiál zaúčtována, protože materiál musí být k dispozici pro destrukční testy</span><span class="sxs-lookup"><span data-stu-id="1b9e6-235">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="1b9e6-236">Požadavek pro objednávku kvality se může týkat určitého pracoviště, položky, dodavatele nebo kombinace těchto podmínek.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-236">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="1b9e6-237">Ručně vygenerovaná objednávka kvality, která odkazuje na nákupní objednávku, může použít informace ze záznamu o přidružení kvality, jako je plán testování vzorku.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-237">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1b9e6-238">Karanténní příkaz</span><span class="sxs-lookup"><span data-stu-id="1b9e6-238">Quarantine order</span></span></td>
<td><span data-ttu-id="1b9e6-239">Před tím nebo po tom, co je karanténní příkaz vykázán jako dokončený nebo ukončený</span><span class="sxs-lookup"><span data-stu-id="1b9e6-239">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="1b9e6-240">Objednávky kvality, které vyžadují provedení destrukčních testů, nelze generovat.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-240">Quality orders that require destructive tests can&#39;t be generated.</span></span> <span data-ttu-id="1b9e6-241">Předpokládá se, že funkce karanténního příkazu zpracovává likvidaci materiálu, který je zničen.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-241">It&#39;s assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="1b9e6-242">Požadavek pro objednávku kvality se může týkat určitého pracoviště, položky, dodavatele nebo kombinace těchto podmínek.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-242">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="1b9e6-243">Ručně vygenerovaná objednávka kvality, která odkazuje na karanténní příkaz, může použít informace ze záznamu o přidružení kvality, jako je plán testování vzorku.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-243">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1b9e6-244">Prodejní objednávka</span><span class="sxs-lookup"><span data-stu-id="1b9e6-244">Sales order</span></span></td>
<td><span data-ttu-id="1b9e6-245">Před naplánovaným procesem vyskladnění nebo aktualizací dodacího listu pro položky, které byly právě dodány</span><span class="sxs-lookup"><span data-stu-id="1b9e6-245">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="1b9e6-246">Při jakémkoli kroku</span><span class="sxs-lookup"><span data-stu-id="1b9e6-246">At any step</span></span></td>
<td><span data-ttu-id="1b9e6-247">Požadavek pro objednávku kvality se může týkat určitého pracoviště, položky, odběratele nebo kombinace těchto podmínek.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-247">The requirement for a quality order can reflect a particular site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="1b9e6-248">Ručně vygenerovaná objednávka kvality, která odkazuje na prodejní objednávku, může použít informace ze záznamu o přidružení kvality, jako je plán testování vzorku.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-248">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1b9e6-249">Výrobní zakázka</span><span class="sxs-lookup"><span data-stu-id="1b9e6-249">Production order</span></span></td>
<td><span data-ttu-id="1b9e6-250">Před tím nebo po tom, co je vykázáno dokončené množství pro výrobní zakázku</span><span class="sxs-lookup"><span data-stu-id="1b9e6-250">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="1b9e6-251">Po tom, co je vykázáno dokončené množství pro výrobní zakázku</span><span class="sxs-lookup"><span data-stu-id="1b9e6-251">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="1b9e6-252">Požadavek pro objednávku kvality se může týkat určitého pracoviště, položky nebo kombinace těchto podmínek.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-252">The requirement for a quality order can reflect a particular site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="1b9e6-253">Ručně vygenerovaná objednávka kvality, která odkazuje na výrobní zakázku, může použít informace ze záznamu o přidružení kvality, jako je plán testování vzorku.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-253">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1b9e6-254">Výrobní zakázka s operací postupu</span><span class="sxs-lookup"><span data-stu-id="1b9e6-254">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="1b9e6-255">Před tím nebo po tom, co je dokončeno ohlášení pro operaci</span><span class="sxs-lookup"><span data-stu-id="1b9e6-255">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="1b9e6-256">Po tom, co je pro poslední operaci dokončeno ohlášení výrobní zakázky</span><span class="sxs-lookup"><span data-stu-id="1b9e6-256">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="1b9e6-257">Požadavek pro objednávku kvality se může týkat určitého pracoviště, položky, provozního prostředku nebo kombinace těchto podmínek.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-257">The requirement for a quality order can reflect a particular, site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="1b9e6-258">Ručně vygenerovaná objednávka kvality, která odkazuje na operaci postupu, může použít informace ze záznamu o přidružení kvality, jako je plán testování vzorku.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-258">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1b9e6-259">Zásoby</span><span class="sxs-lookup"><span data-stu-id="1b9e6-259">Inventory</span></span></td>
<td><span data-ttu-id="1b9e6-260">Objednávku kvality nelze automaticky generovat pro transakci v deníku zásob ani pro transakce převodních příkazů.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-260">A quality order cannot be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="1b9e6-261">Objednávku kvality je možné vytvořit ručně pro množství položky na skladě.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-261">A quality order must be created manually for an item&#39;s inventory quantity.</span></span> <span data-ttu-id="1b9e6-262">Jsou vyžadovány fyzické zásoby na skladě.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-262">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>

## <a name="quality-order-auto-generation-examples"></a><span data-ttu-id="1b9e6-263">Příklady automatického generování objednávek kvality</span><span class="sxs-lookup"><span data-stu-id="1b9e6-263">Quality order auto-generation examples</span></span>

### <a name="purchasing"></a><span data-ttu-id="1b9e6-264">Nákup</span><span class="sxs-lookup"><span data-stu-id="1b9e6-264">Purchasing</span></span>

<span data-ttu-id="1b9e6-265">Pokud v nákupu nastavíte pole **Typ události** na hodnotu **Příjemka produktu** a pole **Spuštění** na **Po** na stránce **Přidružení kvality**, získáte následující výsledky:</span><span class="sxs-lookup"><span data-stu-id="1b9e6-265">In purchasing, if you set the **Event type** field to **Product receipt** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span> 

- <span data-ttu-id="1b9e6-266">Pokud je možnost **Podle aktualizovaného množství** nastavená na **Ano**, objednávka kvality se vygeneruje pro každý příjem na základě nákupní objednávky podle přijatého množství a nastavení ve vzorku položky.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-266">If the **Per updated quantity** option is set to **Yes**, a quality order is generated for every receipt against the purchase order, based on the received quantity and settings in the item sampling.</span></span> <span data-ttu-id="1b9e6-267">Při každém příjmu množství na základě nákupní objednávky jsou nové objednávky kvality generovány na základě nově přijatého množství.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-267">Every time that a quantity is received against the purchase order, new quality orders are generated based on the newly received quantity.</span></span>
- <span data-ttu-id="1b9e6-268">Pokud je možnost **Podle aktualizovaného množství** nastavená na **Ne**, objednávka kvality se vygeneruje pro první příjem na základě nákupní objednávky podle přijatého množství a nastavení ve vzorku položky.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-268">If the **Per updated quantity** option is set to **No**, a quality order is generated for the first receipt against the purchase order, based on the received quantity.</span></span> <span data-ttu-id="1b9e6-269">Dále se vytvoří jedna nebo více objednávek kvality na základě zbývajícího množství v závislosti na sledovacích dimenzích.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-269">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions.</span></span> <span data-ttu-id="1b9e6-270">Objednávky kvality nejsou vygenerovány pro následné příjmy s nákupní objednávkou.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-270">Quality orders aren't generated for subsequent receipts against the purchase order.</span></span>

### <a name="production"></a><span data-ttu-id="1b9e6-271">Výrobní</span><span class="sxs-lookup"><span data-stu-id="1b9e6-271">Production</span></span>

<span data-ttu-id="1b9e6-272">Pokud ve výrobě nastavíte pole **Typ události** na hodnotu **Vykázat jako dokončené** a pole **Spuštění** na **Po** na stránce **Přidružení kvality**, získáte následující výsledky:</span><span class="sxs-lookup"><span data-stu-id="1b9e6-272">In production, if you set the **Event type** field to **Report as finished** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="1b9e6-273">Pokud je možnost **Podle aktualizovaného množství** nastavená na **Ano**, objednávka kvality se vygeneruje podle každého dokončeného množství a nastavení ve vzorku položky.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-273">If the **Per updated quantity** option is set to **Yes**, a quality order is generated based on every finished quantity and settings in the item sampling.</span></span> <span data-ttu-id="1b9e6-274">Při každém vykázání množství jako dokončeného na základě výrobní zakázky jsou nové objednávky kvality generovány na základě nově dokončeného množství.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-274">Every time that a quantity is reported as finished against the production order, new quality orders are generated based on newly finished quantity.</span></span> <span data-ttu-id="1b9e6-275">Tato logika generování je konzistentní s nákupem.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-275">This generation logic is consistent with purchasing.</span></span>
- <span data-ttu-id="1b9e6-276">Pokud je možnost **Podle aktualizovaného množství** nastavená na **Ne**, objednávka kvality se vygeneruje při přvní vykázání množství jako dokončeného na základě dokončeného množství.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-276">If the **Per updated quantity** option is set to **No**, a quality order is generated the first time that a quantity is reported as finished, based on the finished quantity.</span></span> <span data-ttu-id="1b9e6-277">Dále se vytvoří jedna nebo více objednávek kvality na základě zbývajícího množství v závislosti na sledovacích dimenzích vzorku položky.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-277">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions of the item sampling.</span></span> <span data-ttu-id="1b9e6-278">Objednávky kvality nejsou vygenerovány pro následná dokončená množství.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-278">Quality orders aren't generated for subsequent finished quantities.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="1b9e6-279">Specifikace kvality</span><span class="sxs-lookup"><span data-stu-id="1b9e6-279">Quality specification</span></span></th>
<th><span data-ttu-id="1b9e6-280">Na aktualizované množství</span><span class="sxs-lookup"><span data-stu-id="1b9e6-280">Per updated quantity</span></span></th>
<th><span data-ttu-id="1b9e6-281">Na sledovací dimenzi</span><span class="sxs-lookup"><span data-stu-id="1b9e6-281">Per tracking dimension</span></span></th>
<th><span data-ttu-id="1b9e6-282">Výsledek</span><span class="sxs-lookup"><span data-stu-id="1b9e6-282">Result</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="1b9e6-283">Počet procent: 10 %</span><span class="sxs-lookup"><span data-stu-id="1b9e6-283">Percentage: 10%</span></span></td>
<td><span data-ttu-id="1b9e6-284">Ano</span><span class="sxs-lookup"><span data-stu-id="1b9e6-284">Yes</span></span></td>
<td>
<p><span data-ttu-id="1b9e6-285">Číslo dávky: Ne</span><span class="sxs-lookup"><span data-stu-id="1b9e6-285">Batch number: No</span></span></p>
<p><span data-ttu-id="1b9e6-286">Sériové číslo: Ne</span><span class="sxs-lookup"><span data-stu-id="1b9e6-286">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="1b9e6-287">Množství na objednávce: 100</span><span class="sxs-lookup"><span data-stu-id="1b9e6-287">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="1b9e6-288">Vykázat jako dokončené pro 30</span><span class="sxs-lookup"><span data-stu-id="1b9e6-288">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="1b9e6-289">Objednávka kvality č. 1 na 3 (10 % z 30)</span><span class="sxs-lookup"><span data-stu-id="1b9e6-289">Quality order #1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="1b9e6-290">Vykázat jako dokončené pro 70</span><span class="sxs-lookup"><span data-stu-id="1b9e6-290">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="1b9e6-291">Objednávka kvality č.2 na 7 (10 % ze zbývajícího množství objednávky, které se v tomto případě rovná 70)</span><span class="sxs-lookup"><span data-stu-id="1b9e6-291">Quality order #2 for 7 (10% of the remaining order quantity, which equals 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="1b9e6-292">Fixní množství: 1</span><span class="sxs-lookup"><span data-stu-id="1b9e6-292">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="1b9e6-293">Ne</span><span class="sxs-lookup"><span data-stu-id="1b9e6-293">No</span></span></td>
<td>
<p><span data-ttu-id="1b9e6-294">Číslo dávky: Ne</span><span class="sxs-lookup"><span data-stu-id="1b9e6-294">Batch number: No</span></span></p>
<p><span data-ttu-id="1b9e6-295">Sériové číslo: Ne</span><span class="sxs-lookup"><span data-stu-id="1b9e6-295">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="1b9e6-296">Množství na objednávce: 100</span><span class="sxs-lookup"><span data-stu-id="1b9e6-296">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="1b9e6-297">Vykázat jako dokončené pro 30</span><span class="sxs-lookup"><span data-stu-id="1b9e6-297">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="1b9e6-298">Objednávka kvality č. 1 pro 1 (pro první vykázané množství jako dokončené, které má pevnou hodnotu 1)</span><span class="sxs-lookup"><span data-stu-id="1b9e6-298">Quality order #1 for 1 (for the first reported-as-finished quantity, which has a fixed value of 1)</span></span></li>
<li><span data-ttu-id="1b9e6-299">Objednávka kvality č. 2 pro 1 (pro zbývající množství, které má stabilně pevnou hodnotu 1)</span><span class="sxs-lookup"><span data-stu-id="1b9e6-299">Quality order #2 for 1 (for the remaining quantity, which still has a fixed value of 1)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="1b9e6-300">Vykázat jako dokončené pro 10</span><span class="sxs-lookup"><span data-stu-id="1b9e6-300">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="1b9e6-301">Nejsou vytvořeny žádné objednávky kvality.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-301">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="1b9e6-302">Vykázat jako dokončené pro 60</span><span class="sxs-lookup"><span data-stu-id="1b9e6-302">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="1b9e6-303">Nejsou vytvořeny žádné objednávky kvality.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-303">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="1b9e6-304">Fixní množství: 1</span><span class="sxs-lookup"><span data-stu-id="1b9e6-304">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="1b9e6-305">Ano</span><span class="sxs-lookup"><span data-stu-id="1b9e6-305">Yes</span></span></td>
<td>
<p><span data-ttu-id="1b9e6-306">Číslo dávky: Ano</span><span class="sxs-lookup"><span data-stu-id="1b9e6-306">Batch number: Yes</span></span></p>
<p><span data-ttu-id="1b9e6-307">Sériové číslo: Ano</span><span class="sxs-lookup"><span data-stu-id="1b9e6-307">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="1b9e6-308">Množství na objednávce: 10</span><span class="sxs-lookup"><span data-stu-id="1b9e6-308">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="1b9e6-309">Vykázat jako dokončené pro 3: 1 pro #b1, #s1; 1 pro #b2, #s2 a 1 pro #b3, #s3</span><span class="sxs-lookup"><span data-stu-id="1b9e6-309">Report as finished for 3: 1 for #b1, #s1; 1 for #b2, #s2; and 1 for #b3, #s3</span></span>
<ul>
<li><span data-ttu-id="1b9e6-310">Pořadí kvality č 1 pro 1 z dávky #b1, sériové #s1</span><span class="sxs-lookup"><span data-stu-id="1b9e6-310">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="1b9e6-311">Pořadí kvality č 2 pro 1 z dávky #b2, sériové #s2</span><span class="sxs-lookup"><span data-stu-id="1b9e6-311">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="1b9e6-312">Pořadí kvality č 3 pro 1 z dávky #b3, sériové #s3</span><span class="sxs-lookup"><span data-stu-id="1b9e6-312">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="1b9e6-313">Vykázat jako dokončené pro 2:1 pro #b4, #s4 a 1 pro #b5, #s5</span><span class="sxs-lookup"><span data-stu-id="1b9e6-313">Report as finished for 2: 1 for #b4, #s4; and 1 for #b5, #s5</span></span>
<ul>
<li><span data-ttu-id="1b9e6-314">Pořadí kvality č 4 pro 1 z dávky #b4, sériové #s4</span><span class="sxs-lookup"><span data-stu-id="1b9e6-314">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
<li><span data-ttu-id="1b9e6-315">Pořadí kvality č 5 pro 1 z dávky #b5, sériové #s5</span><span class="sxs-lookup"><span data-stu-id="1b9e6-315">Quality order #5 for 1 of batch #b5, serial #s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="1b9e6-316"><strong>Poznámka:</strong> Dávku lze znovu použít.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-316"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="1b9e6-317">Fixní množství: 2</span><span class="sxs-lookup"><span data-stu-id="1b9e6-317">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="1b9e6-318">Ne</span><span class="sxs-lookup"><span data-stu-id="1b9e6-318">No</span></span></td>
<td>
<p><span data-ttu-id="1b9e6-319">Číslo dávky: Ano</span><span class="sxs-lookup"><span data-stu-id="1b9e6-319">Batch number: Yes</span></span></p>
<p><span data-ttu-id="1b9e6-320">Sériové číslo: Ano</span><span class="sxs-lookup"><span data-stu-id="1b9e6-320">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="1b9e6-321">Množství na objednávce: 10</span><span class="sxs-lookup"><span data-stu-id="1b9e6-321">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="1b9e6-322">Vykázat jako dokončené 4: 1 pro #b1, #s1; 1 pro #b2, #s2; 1 pro #b3, #s3 a 1 pro #b4, #s4</span><span class="sxs-lookup"><span data-stu-id="1b9e6-322">Report as finished for 4: 1 for #b1, #s1; 1 for #b2, #s2; 1 for #b3, #s3; and 1 for #b4, #s4</span></span>
<ul>
<li><span data-ttu-id="1b9e6-323">Pořadí kvality č 1 pro 1 z dávky #b1, sériové #s1</span><span class="sxs-lookup"><span data-stu-id="1b9e6-323">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="1b9e6-324">Pořadí kvality č 2 pro 1 z dávky #b2, sériové #s2</span><span class="sxs-lookup"><span data-stu-id="1b9e6-324">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="1b9e6-325">Pořadí kvality č 3 pro 1 z dávky #b3, sériové #s3</span><span class="sxs-lookup"><span data-stu-id="1b9e6-325">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
<li><span data-ttu-id="1b9e6-326">Pořadí kvality č 4 pro 1 z dávky #b4, sériové #s4</span><span class="sxs-lookup"><span data-stu-id="1b9e6-326">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="1b9e6-327">Objednávka kvality #5 pro 2, bez reference na dávku a sériové číslo</span><span class="sxs-lookup"><span data-stu-id="1b9e6-327">Quality order #5 for 2, without a reference to a batch and a serial number</span></span></li>
</ul>
</li>
<li><span data-ttu-id="1b9e6-328">Vykázat jako dokončené pro 6: 1 pro #b5, #s5; 1 pro #b6, #s6; 1 pro #b7, #s7; 1 pro #b8, #s8; 1 pro #b9, #s9 a 1 pro #b10, #s10</span><span class="sxs-lookup"><span data-stu-id="1b9e6-328">Report as finished for 6: 1 for #b5, #s5; 1 for #b6, #s6; 1 for #b7, #s7; 1 for #b8, #s8; 1 for #b9, #s9; and 1 for #b10, #s10</span></span>
<ul>
<li><span data-ttu-id="1b9e6-329">Nejsou vytvořeny žádné objednávky kvality.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-329">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="1b9e6-330">Funkce *Správa kvality pro procesy skladu* přidává možnosti zpracování objednávky kvality pro výrobu s atributem **Typ události** nastaveným jako *Oznámit jako dokončené* a atributem **Spuštění** nastaveným jako *Po dokončení*, a pro nákupy s atributem **Typem události** nastaveným jako *Registrace*.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-330">The *Quality management for warehouse processes* feature adds capabilities for quality order processing for production with **Event type** set to *Report as finished* and **Execution** set to *After*, and for purchases with **Event type** set to *Registration*.</span></span> <span data-ttu-id="1b9e6-331">Další informace vizi [Správa kvality pro procesy skladu](quality-management-for-warehouses-processes.md).</span><span class="sxs-lookup"><span data-stu-id="1b9e6-331">For details, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

## <a name="quality-management-pages"></a><span data-ttu-id="1b9e6-332">Stránky modulu Správa kvality</span><span class="sxs-lookup"><span data-stu-id="1b9e6-332">Quality management pages</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1b9e6-333">Strana</span><span class="sxs-lookup"><span data-stu-id="1b9e6-333">Page</span></span></th>
<th><span data-ttu-id="1b9e6-334">popis</span><span class="sxs-lookup"><span data-stu-id="1b9e6-334">Description</span></span></th>
<th><span data-ttu-id="1b9e6-335">Příklad</span><span class="sxs-lookup"><span data-stu-id="1b9e6-335">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1b9e6-336">Přiřazení kvality</span><span class="sxs-lookup"><span data-stu-id="1b9e6-336">Quality associations</span></span></td>
<td><span data-ttu-id="1b9e6-337">Přečtěte si předchozí část tohoto článku.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-337">See the previous sections of this article.</span></span></td>
<td><span data-ttu-id="1b9e6-338">Přidružení kvality určuje pro vygenerovanou objednávku kvality tyto informace:</span><span class="sxs-lookup"><span data-stu-id="1b9e6-338">A quality association defines all the following information for a quality order that is generated:</span></span>
<ul>
<li><span data-ttu-id="1b9e6-339">Událost transakce</span><span class="sxs-lookup"><span data-stu-id="1b9e6-339">The transaction event</span></span></li>
<li><span data-ttu-id="1b9e6-340">Sada testů, které je nutné u položky vykonat</span><span class="sxs-lookup"><span data-stu-id="1b9e6-340">The set of tests that must be performed on the items</span></span></li>
<li><span data-ttu-id="1b9e6-341">Přijatelná úroveň kvality</span><span class="sxs-lookup"><span data-stu-id="1b9e6-341">The AQL</span></span></li>
<li><span data-ttu-id="1b9e6-342">Plán vzorkování</span><span class="sxs-lookup"><span data-stu-id="1b9e6-342">The sampling plan</span></span></li>
</ul>
<span data-ttu-id="1b9e6-343">Přiřazení kvality je nutné definovat pro každou variantu obchodního procesu, který vyžaduje automatické generování objednávky kvality.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-343">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="1b9e6-344">Objednávky kvality lze generovat například v obchodních procesech pro nákupní objednávky, karanténní příkazy, prodejní objednávky a výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-344">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b9e6-345">Testy</span><span class="sxs-lookup"><span data-stu-id="1b9e6-345">Tests</span></span></td>
<td><span data-ttu-id="1b9e6-346">Tuto stránku použijte k definování a prohlížení individuálních testů, které zjišťují, zda vaše produkty splňují specifikace kvality.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-346">Use this page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="1b9e6-347">Ke skupině testů můžete přiřadit jeden nebo více individuálních testů.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-347">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="1b9e6-348">V tomto případě zadáte také informace specifické pro daný test, jako jsou například přijatelné hodnoty měření.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-348">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="1b9e6-349">Hodnoty měření se používají k testování množství a testovací proměnné slouží pro testy kvality.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-349">Measurement values are used for quantitative tests, and test variables are used for qualitative tests.</span></span>
<ul>
<li><span data-ttu-id="1b9e6-350">Kvantitativní test má typ testu <strong>Celé číslo</strong> nebo <strong>Zlomek</strong> a také má určenou měrnou jednotku.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-350">A quantitative test has a test type of <strong>Integer</strong> or <strong>Fraction</strong>, and also has a designated unit of measure.</span></span> <span data-ttu-id="1b9e6-351">Specifikace kvality a výsledky testu jsou vyjádřeny jako čísla.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-351">Quality specifications and test results are expressed as numbers.</span></span></li>
<li><span data-ttu-id="1b9e6-352">V případě testu kvality se jedná o test typu <strong>Parametr</strong>.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-352">A qualitative test has a test type of <strong>Option</strong>.</span></span> <span data-ttu-id="1b9e6-353">Testy kvality vyžadují další informace o měřených testovacích proměnných a o výčtu jejich hodnot.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-353">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="1b9e6-354">Specifikace kvality a výsledky testu jsou vyjádřeny v závislosti na výstupu.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-354">Quality specifications and test results are expressed according to an outcome.</span></span></li>
</ul></td>
<td><span data-ttu-id="1b9e6-355">Výrobní společnost provádí dva testy na zakoupeném materiálu: kvantitativní test ohledně kvality materiálu a test kvality ohledně poškození balení.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-355">A manufacturing company performs two tests on purchased material: a quantitative test about material quality and a qualitative test about packaging damage.</span></span> <span data-ttu-id="1b9e6-356">Tato společnost definuje další informace ohledně kvalitativního testu s cílem identifikovat testovací proměnnou (poškozené balení) a její výstupní hodnoty.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-356">The company defines additional information about the qualitative test to identify the test variable (damaged packaging) and its outcomes.</span></span> <span data-ttu-id="1b9e6-357">Společnost používá stránku <strong>Testovací skupiny</strong> k přiřazení dvou testů do skupiny testů a k určení informací o daném testu.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-357">The company uses the <strong>Test groups</strong> page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="1b9e6-358">Testovací skupina je přiřazena k objednávce kvality, takže daná společnost může vytvořit sestavu pro dané dva testy.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-358">The test group is assigned to a quality order, so that the company can report test results for the two tests.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b9e6-359">Testovací skupiny</span><span class="sxs-lookup"><span data-stu-id="1b9e6-359">Test groups</span></span></td>
<td><span data-ttu-id="1b9e6-360">Tato stránka slouží k nastavení, úpravě a zobrazení testovacích skupin a jednotlivých testů přiřazených testovací skupině.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-360">Use this page to set up, edit, and view test groups and the individual tests that are assigned to a test group.</span></span> <span data-ttu-id="1b9e6-361">V horním podokně jsou zobrazeny testovací skupiny a v dolním podokně jsou zobrazeny testy, které jsou přiřazené vybrané testovací skupině.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-361">The upper pane displays test groups, and the lower pane displays the tests that are assigned to a selected test group.</span></span> <span data-ttu-id="1b9e6-362">Každé testovací skupině můžete přiřadit několik zásad, jako například plán vzorkování, přijatelnou úroveň kvality a požadavek na destrukční testy.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-362">You assign several policies to a test group, such as a sampling plan, an AQL, and the requirement for destructive testing.</span></span> <span data-ttu-id="1b9e6-363">Při přiřazení jednotlivého testu do skupiny testů definujete další informace, jako jsou například pořadí, dokumenty nebo data platnosti.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-363">When you assign an individual test to a test group, you define additional information, such as the sequence, documents, and validity dates.</span></span> <span data-ttu-id="1b9e6-364">Pro kvantitativní test definujete také informace o přijatelných hodnotách měření.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-364">For a quantitative test, the information that you define also includes the acceptable measurement values.</span></span> <span data-ttu-id="1b9e6-365">Informace o testu kvality obsahují také testovací proměnné a výchozí výstup.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-365">For a qualitative test, the information includes the test variable and default outcome.</span></span> <span data-ttu-id="1b9e6-366">Skupina testů přiřazená objednávce kvality určuje výchozí sadu testů, které je nutné na určených položkách vykonat.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-366">The test group that is assigned to a quality order defines the default set of tests that must be performed on the specified item.</span></span> <span data-ttu-id="1b9e6-367">Testy však můžete přidat, odstranit nebo změnit na objednávce kvality.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-367">However, you can add, delete, or change tests on the quality order.</span></span> <span data-ttu-id="1b9e6-368">Výsledky testu jsou uvedeny pro všechny testy v objednávce kvality.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-368">Test results are reported for each test on a quality order.</span></span></td>
<td><span data-ttu-id="1b9e6-369">Výrobní společnost má definované testovací skupiny pro každou variantu pokynů týkajících se kvality.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-369">A manufacturing company defines a test group for each variation of its quality guidelines.</span></span> <span data-ttu-id="1b9e6-370">Různé testovací skupiny odrážejí rozdíly v plánech vzorkování, v sadách testů, které je nutné provádět dohromady, v přijatelné úrovni kvality i v dalších činitelích.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-370">The various test groups reflect differences in the sampling plans, the sets of tests that must be performed together, the AQL, and other factors.</span></span> <span data-ttu-id="1b9e6-371">Pro kvantitativní testy existují také rozdíly v přijatelných hodnotách měření.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-371">For quantitative tests, there are also differences in the acceptable measurement values.</span></span> <span data-ttu-id="1b9e6-372">K uplatnění pokynů týkajících se kvality přiřadí společnost na stránce <strong>Přidružení kvality</strong> každé testovací skupině pravidlo automatického generování objednávek kvality a také přiřadí skupiny testů k objednávce kvality, který byla vytvořena ručně.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-372">To enforce its quality guidelines, the company assigns a test group to each rule for automatically generating quality orders on the <strong>Quality associations</strong> page, and also assigns a test group to quality orders that are manually created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b9e6-373">Skupiny kvality položek</span><span class="sxs-lookup"><span data-stu-id="1b9e6-373">Item quality groups</span></span></td>
<td><span data-ttu-id="1b9e6-374">Tato stránka slouží k nastavení, úpravě a zobrazení položek zařazených do skupin kvality, které jsou přiřazeny položce.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-374">Use this page to set up, edit, and view the items that are assigned to a quality group or the quality groups that are assigned to an item.</span></span> <span data-ttu-id="1b9e6-375">Skupina kvality představuje společné požadavky na testování položek.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-375">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="1b9e6-376">Po určení požadavků na testování na stránce <strong>Testovací skupiny</strong> můžete definovat pravidla pro automatické generování objednávek kvality.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-376">After you define the test requirements on the <strong>Test groups</strong> page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="1b9e6-377">Proces můžete zjednodušit tak, že nebudete definovat pravidla pro jednotlivé položky.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-377">To simplify the process, you don&#39;t define rules for individual items.</span></span> <span data-ttu-id="1b9e6-378">Namísto toho na stránce <strong>Přidružení kvality</strong> určíte pravidla pro skupinu kvality.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-378">Instead, you define rules for a quality group, by using the <strong>Quality associations</strong> page.</span></span> <span data-ttu-id="1b9e6-379">Pro vybranou skupinu kvality můžete také použít stránku <strong>Skupiny kvality položek</strong> a přiřadit k této skupině příslušné položky.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-379">You can also use the <strong>Item quality groups</strong> page for a selected quality group to assign relevant items to that group.</span></span> <span data-ttu-id="1b9e6-380">Pro vybranou položku můžete také použít stránku <strong>Skupiny kvality položek</strong> a přiřadit příslušnou skupiny kvality příslušné položce.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-380">You can also use the <strong>Item quality groups</strong> page for a selected item to assign relevant quality groups to that item.</span></span></td>
<td><span data-ttu-id="1b9e6-381">Výrobní společnost nakupuje různé suroviny, které při vstupní kontrole podléhají stejným požadavkům na testování.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-381">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="1b9e6-382">Společnost definuje skupinu kvality a přiřadí čísla položek, které jsou přidruženy k surovinám, do této skupiny.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-382">The company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="1b9e6-383">Později společnosti zakoupí nový typ suroviny, který má stejné požadavky na testování.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-383">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="1b9e6-384">Namísto vytvoření nových požadavků na testování pro nový materiál společnost přidá číslo položky pro nový materiál do stávající skupiny kvality.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-384">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span> <span data-ttu-id="1b9e6-385">Stejná výrobní společnost vyrábí také položky, na které jsou kladeny stejné požadavky na testování, a expeduje položky, které před odesláním podléhají stejné kontrole.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-385">The same manufacturing company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="1b9e6-386">Společnost definuje další dvě skupiny kvality a do každé skupiny zařadí příslušné položky.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-386">The company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b9e6-387">Testovací proměnné</span><span class="sxs-lookup"><span data-stu-id="1b9e6-387">Test variables</span></span></td>
<td><span data-ttu-id="1b9e6-388">Tato stránka slouží k určení a zobrazení proměnných spojených s testem kvality.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-388">Use this page to define and view the variables that are associated with a qualitative test.</span></span> <span data-ttu-id="1b9e6-389">Pro každou proměnnou určete výčet výstupních hodnot, které reprezentují možné volby.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-389">For each variable, you define enumerated outcomes that represent the possible options.</span></span> <span data-ttu-id="1b9e6-390">Na stránce <strong>Testy</strong> určete testy.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-390">You define tests on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="1b9e6-391">U testů kvality je nutné nastavit typ testu na hodnotu <strong>Možnost</strong>.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-391">For qualitative tests, you must set the test type to <strong>Option</strong>.</span></span> <span data-ttu-id="1b9e6-392">Na stránce <strong>Testovací skupiny</strong> přiřaďte testovací proměnnou k jednotlivému testu.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-392">Use the <strong>Test groups</strong> page to assign a test variable to an individual test.</span></span></td>
<td><span data-ttu-id="1b9e6-393">Společnost vyrábějící cukrovinky používá kontrolní test pro dokončené výrobky.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-393">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="1b9e6-394">Kontrolní test má několik proměnných.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-394">This inspection test has several variables.</span></span> <span data-ttu-id="1b9e6-395">Jedna proměnná odpovídá chuti, přičemž možné výstupní hodnoty pro tuto proměnnou jsou „dobrá“ a „špatná“.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-395">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="1b9e6-396">Druhá proměnná odpovídá barvě, přičemž možní výstupní hodnoty jsou „příliš tmavá“, „příliš světlá“ a „správná“.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-396">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b9e6-397">Výsledky testovacích proměnných</span><span class="sxs-lookup"><span data-stu-id="1b9e6-397">Test variable outcomes</span></span></td>
<td><span data-ttu-id="1b9e6-398">Na této stránce lze nastavit, upravit nebo zobrazit možné výsledky testů pro testovací proměnnou, která je přidružena k testu kvality.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-398">Use this page to set up, edit, and to view the possible test results for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="1b9e6-399">Každé výstupní hodnotě přiřadíte stav <strong>úspěch</strong> nebo <strong>neúspěch</strong>.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-399">For each outcome, you assign a <strong>pass</strong> or <strong>fail</strong> status.</span></span> <span data-ttu-id="1b9e6-400">Pro každý test kvality definovaný na stránce <strong>Testy</strong> je nutné definovat proměnnou a její výstupní hodnoty.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-400">You must define a variable and its outcomes for each qualitative test that is defined on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="1b9e6-401">(U kvalitativních testů je typ testu nastaven na <strong>Volba</strong> na stránce <strong>Testy</strong>.) Pomocí stránky <strong>Skupiny testů</strong> přiřaďte proměnnou testu a výchozí výstup k samostatnému kvalitativnímu testu.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-401">(For qualitative tests, the test type is set to <strong>Option</strong> on the <strong>Tests</strong> page.) Use the <strong>Test groups</strong> page to assign a test variable and the default outcome to an individual qualitative test.</span></span></td>
<td><span data-ttu-id="1b9e6-402">Společnost vyrábějící cukrovinky používá kontrolní test pro dokončené výrobky.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-402">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="1b9e6-403">Kontrolní test má několik proměnných.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-403">This inspection test has of several variables.</span></span> <span data-ttu-id="1b9e6-404">Jedna proměnná odpovídá chuti, přičemž možné výstupní hodnoty pro tuto proměnnou jsou „dobrá“ a „špatná“.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-404">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="1b9e6-405">Druhá proměnná odpovídá barvě, přičemž možní výstupní hodnoty jsou „příliš tmavá“, „příliš světlá“ a „správná“.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-405">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span> <span data-ttu-id="1b9e6-406">Ke každé výstupní hodnotě je přiřazen stav <strong>úspěch</strong> nebo <strong>neúspěch</strong>.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-406">A status of <strong>pass</strong> or <strong>fail</strong> is assigned to each outcome.</span></span> <span data-ttu-id="1b9e6-407">Během kontrolního testu pro každou proměnnou kontrolor ohlásí výsledky testu výběrem některé z výstupních hodnot.</span><span class="sxs-lookup"><span data-stu-id="1b9e6-407">During the inspection test for each variable, the inspector reports the test result by selecting one of the outcomes.</span></span></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="1b9e6-408">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="1b9e6-408">Additional resources</span></span>
--------

[<span data-ttu-id="1b9e6-409">Procesy správy kvality</span><span class="sxs-lookup"><span data-stu-id="1b9e6-409">Quality management processes</span></span>](quality-management-processes.md)

[<span data-ttu-id="1b9e6-410">Řízení neshody</span><span class="sxs-lookup"><span data-stu-id="1b9e6-410">Nonconformance management</span></span>](enable-nonconformance-management.md)

[<span data-ttu-id="1b9e6-411">Správa kvality pro procesy skladu</span><span class="sxs-lookup"><span data-stu-id="1b9e6-411">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)
