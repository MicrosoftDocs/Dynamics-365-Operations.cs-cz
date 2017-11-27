---
title: "Zásady práce ve skladu"
description: "Zásady práce ve skladu řídí, zda je skladová práce vytvářena skladovými procesy ve výrobě na základě typu pracovního příkazu, skladového místa a produktu."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSWorkPolicy
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 196561
ms.assetid: cbf48ec6-1836-48d5-ad66-a9b534af1786
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 83e8dc76350e0d40a392e9a04ddca5b4b45d0da0
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="warehouse-work-policies"></a><span data-ttu-id="427a3-103">Zásady práce ve skladu</span><span class="sxs-lookup"><span data-stu-id="427a3-103">Warehouse work policies</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="427a3-104">Zásady práce ve skladu v aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition řídí, zda je skladová práce vytvářena skladovými procesy ve výrobě na základě typu pracovního příkazu, skladového místa a produktu.</span><span class="sxs-lookup"><span data-stu-id="427a3-104">Warehouse work policies in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition control whether warehouse work is created by warehouse processes in manufacturing, based on work order type, inventory location, and product.</span></span>

<span data-ttu-id="427a3-105">Tato pracovní zásada řídí, zda je vytvořena práce skladu pro procesy skladu při výrobě.</span><span class="sxs-lookup"><span data-stu-id="427a3-105">This work policy controls whether warehouse work is created for warehouse processes in manufacturing.</span></span> <span data-ttu-id="427a3-106">Zásadu práce můžete nastavit použitím kombinace **typů pracovního příkazu**, **skladového místa** a **produktu**.</span><span class="sxs-lookup"><span data-stu-id="427a3-106">You can set up the work policy by using a combination of **work order types**, an **inventory location**, and a **product**.</span></span> <span data-ttu-id="427a3-107">Například produkt L0101 je vykazován jako dokončený na umístění výstupu 001.</span><span class="sxs-lookup"><span data-stu-id="427a3-107">For example, product L0101 is reported as finished to output location 001.</span></span> <span data-ttu-id="427a3-108">Hotového výrobek je později spotřebován v jiné výrobní zakázce v umístění výstupu 001.</span><span class="sxs-lookup"><span data-stu-id="427a3-108">The finished good is later consumed in another production order at output location 001.</span></span> <span data-ttu-id="427a3-109">V tomto případě můžete nastavením pracovní zásady zabránit vytvoření práce pro zaskladnění hotových výrobků, když nahlásíte produkt L0101 jako dokončený v umístění výstupu 001.</span><span class="sxs-lookup"><span data-stu-id="427a3-109">In this case, you can set up a work policy to prevent the work for finished goods put-away from being created when you report product L0101 as finished to output location 001.</span></span> <span data-ttu-id="427a3-110">Zásady práce označují individuální entitu, kterou lze popsat pomocí následujících informací:</span><span class="sxs-lookup"><span data-stu-id="427a3-110">The work policy is an individual entity that can be described through the following information:</span></span>

-   <span data-ttu-id="427a3-111">**Název pracovní zásady**(jedinečný identifikátor pracovní zásady)</span><span class="sxs-lookup"><span data-stu-id="427a3-111">**Work policy name** (the unique identifier of the work policy)</span></span>
-   <span data-ttu-id="427a3-112">**Typy pracovních činností** a **způsob vytvoření práce**</span><span class="sxs-lookup"><span data-stu-id="427a3-112">**Work order types** and **Work creation method**</span></span>
-   <span data-ttu-id="427a3-113">**Skladová místa**</span><span class="sxs-lookup"><span data-stu-id="427a3-113">**Inventory locations**</span></span>
-   <span data-ttu-id="427a3-114">**Výrobky**</span><span class="sxs-lookup"><span data-stu-id="427a3-114">**Products**</span></span>

## <a name="work-order-types"></a><span data-ttu-id="427a3-115">Typy pořadí pracovních činností</span><span class="sxs-lookup"><span data-stu-id="427a3-115">Work order types</span></span>
<span data-ttu-id="427a3-116">Můžete vybrat některý z následujících typů pracovních příkazů:</span><span class="sxs-lookup"><span data-stu-id="427a3-116">You can select the following work order types:</span></span>

-   <span data-ttu-id="427a3-117">Výdej dokončeného zboží</span><span class="sxs-lookup"><span data-stu-id="427a3-117">Finished goods put away</span></span>
-   <span data-ttu-id="427a3-118">Vyskladnění vedlejšího produktu</span><span class="sxs-lookup"><span data-stu-id="427a3-118">Co-product and by-product put away</span></span>
-   <span data-ttu-id="427a3-119">Výdej suroviny</span><span class="sxs-lookup"><span data-stu-id="427a3-119">Raw material picking</span></span>

<span data-ttu-id="427a3-120">Pole **Metoda vytváření práce** má hodnotu **Nikdy**.</span><span class="sxs-lookup"><span data-stu-id="427a3-120">The **Work creation method** field has the value **Never**.</span></span> <span data-ttu-id="427a3-121">Tato hodnota značí, že pracovní zásada zabrání vytvoření práce ve skladu pro vybraný typ výrobního příkazu.</span><span class="sxs-lookup"><span data-stu-id="427a3-121">This value indicates that the work policy will prevent warehouse work from being created for the selected work order type.</span></span>

## <a name="inventory-locations"></a><span data-ttu-id="427a3-122">Skladová místa</span><span class="sxs-lookup"><span data-stu-id="427a3-122">Inventory locations</span></span>
<span data-ttu-id="427a3-123">Můžete vybrat místo, na které se pracovní zásada vztahuje.</span><span class="sxs-lookup"><span data-stu-id="427a3-123">You can select a location that the work policy applies to.</span></span> <span data-ttu-id="427a3-124">Pokud žádné umístění není přidruženo k zásadě práce, zásada práce se nevztahuje na všechny procesy.</span><span class="sxs-lookup"><span data-stu-id="427a3-124">If no location is associated with a work policy, the work policy doesn’t apply to any processes.</span></span> <span data-ttu-id="427a3-125">Na stránce **Umístění** můžete vybrat nebo zrušit výběr zásady práci na určité místo.</span><span class="sxs-lookup"><span data-stu-id="427a3-125">On the **Locations** page, you can also select or cancel the selection of the work policy for a specific location.</span></span>

## <a name="products"></a><span data-ttu-id="427a3-126">Produkty</span><span class="sxs-lookup"><span data-stu-id="427a3-126">Products</span></span>
<span data-ttu-id="427a3-127">Můžete vybrat produkt, na který se pracovní zásada vztahuje.</span><span class="sxs-lookup"><span data-stu-id="427a3-127">You can select a product that the work policy applies to.</span></span> <span data-ttu-id="427a3-128">Zásadu práce lze použít pro všechny produkty nebo vybrané produkty.</span><span class="sxs-lookup"><span data-stu-id="427a3-128">You can apply the work policy to either all products or selected products.</span></span>

## <a name="example"></a><span data-ttu-id="427a3-129">Příklad</span><span class="sxs-lookup"><span data-stu-id="427a3-129">Example</span></span>
<span data-ttu-id="427a3-130">V následujícím příkladu jsou dvě výrobní zakázky, PRD-001 a PRD-00*2*.</span><span class="sxs-lookup"><span data-stu-id="427a3-130">In the following example, there are two production orders, PRD-001 and PRD-00*2*.</span></span> <span data-ttu-id="427a3-131">Výrobní zakázka PRD-001 má operaci s názvem **Sestavení**, kde produkt SC1 je hlášen jako dokončený v místě O1.</span><span class="sxs-lookup"><span data-stu-id="427a3-131">Production order PRD-001 has an operation that is named **Assembly**, where product SC1 is being reported as finished to location O1.</span></span> <span data-ttu-id="427a3-132">Výrobní zakázka PRD-002 má operaci, která se nazývá **Lakování** a spotřebovává produkt SC1 z umístění O1.</span><span class="sxs-lookup"><span data-stu-id="427a3-132">Production order PRD-002 has an operation that is named **Painting** and consumes product SC1 from location O1.</span></span> <span data-ttu-id="427a3-133">Výrobní zakázka PRD-002 také spotřebovává suroviny RM1 z umístění O1.</span><span class="sxs-lookup"><span data-stu-id="427a3-133">Production order PRD-002 also consumes raw material RM1 from location O1.</span></span> <span data-ttu-id="427a3-134">RM1 je uložen ve skladu BULK-001 a bude vyskladněno v umístění O1 během práce ve skladu pro výdej surovin.</span><span class="sxs-lookup"><span data-stu-id="427a3-134">RM1 is stored in warehouse location BULK-001 and will be picked to location O1 by warehouse work for raw material picking.</span></span> <span data-ttu-id="427a3-135">Pro uvolnění výroby PRD-002 je generována práce vyskladnění.</span><span class="sxs-lookup"><span data-stu-id="427a3-135">The picking work is generated when production PRD-002 is released.</span></span> 

<span data-ttu-id="427a3-136">[![Zásady práce ve skladu](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span><span class="sxs-lookup"><span data-stu-id="427a3-136">[![Warehouse work policies](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span></span> 

<span data-ttu-id="427a3-137">Při plánování konfigurace zásad práce ve skladu pro tento scénář je třeba zvážit následujících informace:</span><span class="sxs-lookup"><span data-stu-id="427a3-137">When you plan to configure a warehouse work policy for this scenario, you should consider the following information:</span></span>

-   <span data-ttu-id="427a3-138">Práce ve skladu pro výdej dokončeného zboží není vyžadována, když vykážete produkt SC1 jako dokončený z výrobní zakázky PRD-001 do umístění O1.</span><span class="sxs-lookup"><span data-stu-id="427a3-138">Warehouse work for finished goods put-away isn’t required when you report product SC1 as finished from production order PRD-001 to location O1.</span></span> <span data-ttu-id="427a3-139">Důvodem je, že operace **Lakování** pro výrobní zakázku PRD-002 spotřebovává SC1 na stejném místě.</span><span class="sxs-lookup"><span data-stu-id="427a3-139">This is because the **Painting** operation for production order PRD-002 consumes SC1 at the same location.</span></span>
-   <span data-ttu-id="427a3-140">Práce ve skladu pro vyzvednutí surovin je požadována pro účely přesunutí surovin RM1 z umístění ve skladu BULK-001 do umístění O1.</span><span class="sxs-lookup"><span data-stu-id="427a3-140">Warehouse work for raw material picking is required in order to move raw material RM1 from warehouse location BULK-001 to location O1.</span></span>

<span data-ttu-id="427a3-141">Toto je příklad zásad práce, které můžete nastavit na základě těchto důvodů.</span><span class="sxs-lookup"><span data-stu-id="427a3-141">Here is an example of the work policy that you can set up, based on these considerations.</span></span>

|                                         |                                                       |
|-----------------------------------------|-------------------------------------------------------|
|<span data-ttu-id="427a3-142">**Název pracovní zásady**</span><span class="sxs-lookup"><span data-stu-id="427a3-142">**Work policy name**</span></span><br>                 |<span data-ttu-id="427a3-143">**Typy pořadí pracovních činností**</span><span class="sxs-lookup"><span data-stu-id="427a3-143">**Work order types**</span></span><br>                               |
| <span data-ttu-id="427a3-144">Bez zaskladnění 01     \`</span><span class="sxs-lookup"><span data-stu-id="427a3-144">No put away 01     \`</span></span>                    |<span data-ttu-id="427a3-145">- Zaskladnění dokončeného výrobku</span><span class="sxs-lookup"><span data-stu-id="427a3-145">- Finished good put away</span></span><br>                           |
|                                         |<span data-ttu-id="427a3-146">**Umístění**</span><span class="sxs-lookup"><span data-stu-id="427a3-146">**Locations**</span></span><br>                                      |
|                                         |<span data-ttu-id="427a3-147">- O1</span><span class="sxs-lookup"><span data-stu-id="427a3-147">- O1</span></span>   |                                               |
|                                         |<span data-ttu-id="427a3-148">**Produkty**</span><span class="sxs-lookup"><span data-stu-id="427a3-148">**Products**</span></span> <br>                                      |
|                                         |<span data-ttu-id="427a3-149">- SC1</span><span class="sxs-lookup"><span data-stu-id="427a3-149">- SC1</span></span>                                                  |

<span data-ttu-id="427a3-150">Následující procedury obsahují podrobné pokyny ke způsobu nastavení zásad pracovního skladu pro tento scénář.</span><span class="sxs-lookup"><span data-stu-id="427a3-150">The following procedures provide step-by-step instructions about how to set up the warehouse work policy for this scenario.</span></span> <span data-ttu-id="427a3-151">Je popsána také ukázka nastavení, která uvádí, jak vykázat výrobní zakázku jako dokončenou v místě, které nemá licenční kód.</span><span class="sxs-lookup"><span data-stu-id="427a3-151">A sample setup showing how to report a production order as finished to a location that isn’t license plate–controlled is also described.</span></span>

## <a name="set-up-a-warehouse-work-policy"></a><span data-ttu-id="427a3-152">Nastavení zásady práce ve skladu</span><span class="sxs-lookup"><span data-stu-id="427a3-152">Set up a warehouse work policy</span></span>
<span data-ttu-id="427a3-153">Skladové procesy ne vždy zahrnují skladovou práci.</span><span class="sxs-lookup"><span data-stu-id="427a3-153">Warehouse processes don’t always include warehouse work.</span></span> <span data-ttu-id="427a3-154">Definováním zásad práce můžete zabránit vytváření práce pro výdej surovin, ale také vyskladnění dokončených výrobků pro sérii produktů v konkrétních umístěních.</span><span class="sxs-lookup"><span data-stu-id="427a3-154">By defining a work policy, you can prevent the creation of work for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span> <span data-ttu-id="427a3-155">K vytvoření této procedury jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="427a3-155">The USMF demo data company was used to create this procedure.</span></span> 

<span data-ttu-id="427a3-156">KROKY (21)</span><span class="sxs-lookup"><span data-stu-id="427a3-156">STEPS (21)</span></span>

|     |                                                                            |
|-----|----------------------------------------------------------------------------|
| <span data-ttu-id="427a3-157">1.</span><span class="sxs-lookup"><span data-stu-id="427a3-157">1.</span></span>  | <span data-ttu-id="427a3-158">Přejděte do nabídky Řízení skladu &gt; Nastavení &gt; Práce &gt; Pracovní zásady.</span><span class="sxs-lookup"><span data-stu-id="427a3-158">Go to Warehouse management &gt; Setup &gt; Work &gt; Work policies.</span></span>        |
| <span data-ttu-id="427a3-159">2.</span><span class="sxs-lookup"><span data-stu-id="427a3-159">2.</span></span>  | <span data-ttu-id="427a3-160">Klikněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="427a3-160">Click New.</span></span>                                                                 |
| <span data-ttu-id="427a3-161">3.</span><span class="sxs-lookup"><span data-stu-id="427a3-161">3.</span></span>  | <span data-ttu-id="427a3-162">Do pole Název pracovní zásady zadejte „Žádné vyskladnění“.</span><span class="sxs-lookup"><span data-stu-id="427a3-162">In the Work policy name field, type 'No put-away work'.</span></span>                    |
| <span data-ttu-id="427a3-163">4.</span><span class="sxs-lookup"><span data-stu-id="427a3-163">4.</span></span>  | <span data-ttu-id="427a3-164">Klepněte na tlačítko Uložit.</span><span class="sxs-lookup"><span data-stu-id="427a3-164">Click Save.</span></span>                                                                |
| <span data-ttu-id="427a3-165">5.</span><span class="sxs-lookup"><span data-stu-id="427a3-165">5.</span></span>  | <span data-ttu-id="427a3-166">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="427a3-166">Click Add.</span></span>                                                                 |
| <span data-ttu-id="427a3-167">6.</span><span class="sxs-lookup"><span data-stu-id="427a3-167">6.</span></span>  | <span data-ttu-id="427a3-168">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="427a3-168">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="427a3-169">7.</span><span class="sxs-lookup"><span data-stu-id="427a3-169">7.</span></span>  | <span data-ttu-id="427a3-170">V poli Typ pořadí pracovních činností vyberte možnost Výdej dokončeného zboží.</span><span class="sxs-lookup"><span data-stu-id="427a3-170">In the Work order type field, select 'Finished goods put away'.</span></span>            |
| <span data-ttu-id="427a3-171">8.</span><span class="sxs-lookup"><span data-stu-id="427a3-171">8.</span></span>  | <span data-ttu-id="427a3-172">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="427a3-172">Click Add.</span></span>                                                                 |
| <span data-ttu-id="427a3-173">9.</span><span class="sxs-lookup"><span data-stu-id="427a3-173">9.</span></span>  | <span data-ttu-id="427a3-174">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="427a3-174">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="427a3-175">10.</span><span class="sxs-lookup"><span data-stu-id="427a3-175">10.</span></span> | <span data-ttu-id="427a3-176">V poli Typ pořadí pracovních činností vyberte Vyskladnění vedlejšího produktu.</span><span class="sxs-lookup"><span data-stu-id="427a3-176">In the Work order type field, select 'Co-product and by-product put away'.</span></span> |
| <span data-ttu-id="427a3-177">11.</span><span class="sxs-lookup"><span data-stu-id="427a3-177">11.</span></span> | <span data-ttu-id="427a3-178">Rozbalte oblast Skladová místa.</span><span class="sxs-lookup"><span data-stu-id="427a3-178">Expand the Inventory locations section.</span></span>                                    |
| <span data-ttu-id="427a3-179">12.</span><span class="sxs-lookup"><span data-stu-id="427a3-179">12.</span></span> | <span data-ttu-id="427a3-180">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="427a3-180">Click Add.</span></span>                                                                 |
| <span data-ttu-id="427a3-181">13.</span><span class="sxs-lookup"><span data-stu-id="427a3-181">13.</span></span> | <span data-ttu-id="427a3-182">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="427a3-182">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="427a3-183">14.</span><span class="sxs-lookup"><span data-stu-id="427a3-183">14.</span></span> | <span data-ttu-id="427a3-184">V seznamu Sklad zadejte „51“.</span><span class="sxs-lookup"><span data-stu-id="427a3-184">In the Warehouse list, enter '51'.</span></span>                                         |
| <span data-ttu-id="427a3-185">15.</span><span class="sxs-lookup"><span data-stu-id="427a3-185">15.</span></span> | <span data-ttu-id="427a3-186">V poli Umístění zadejte nebo vyberte hodnotu 001.</span><span class="sxs-lookup"><span data-stu-id="427a3-186">In the Location field, enter or select '001'.</span></span>                              |
| <span data-ttu-id="427a3-187">16.</span><span class="sxs-lookup"><span data-stu-id="427a3-187">16.</span></span> | <span data-ttu-id="427a3-188">Rozbalte část Produkty.</span><span class="sxs-lookup"><span data-stu-id="427a3-188">Expand the Products section.</span></span>                                               |
| <span data-ttu-id="427a3-189">17.</span><span class="sxs-lookup"><span data-stu-id="427a3-189">17.</span></span> | <span data-ttu-id="427a3-190">Vyberte možnost Vybráno v poli Výběr produktu.</span><span class="sxs-lookup"><span data-stu-id="427a3-190">In the Product selection field, select 'Selected'.</span></span>                         |
| <span data-ttu-id="427a3-191">18.</span><span class="sxs-lookup"><span data-stu-id="427a3-191">18.</span></span> | <span data-ttu-id="427a3-192">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="427a3-192">Click Add.</span></span>                                                                 |
| <span data-ttu-id="427a3-193">19.</span><span class="sxs-lookup"><span data-stu-id="427a3-193">19.</span></span> | <span data-ttu-id="427a3-194">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="427a3-194">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="427a3-195">20.</span><span class="sxs-lookup"><span data-stu-id="427a3-195">20.</span></span> | <span data-ttu-id="427a3-196">V poli Číslo zboží zadejte nebo vyberte hodnotu L0101.</span><span class="sxs-lookup"><span data-stu-id="427a3-196">In the Item number field, enter or select 'L0101'.</span></span>                         |
| <span data-ttu-id="427a3-197">21.</span><span class="sxs-lookup"><span data-stu-id="427a3-197">21.</span></span> | <span data-ttu-id="427a3-198">Klepněte na tlačítko Uložit.</span><span class="sxs-lookup"><span data-stu-id="427a3-198">Click Save.</span></span>                                                                |

## <a name="report-a-production-order-as-finished-to-a-location-that-isnt-license-platecontrolled"></a><span data-ttu-id="427a3-199">Vykázání výrobní zakázky jako dokončené v místě, které není řízeno registrační značkou</span><span class="sxs-lookup"><span data-stu-id="427a3-199">Report a production order as finished to a location that isn’t license plate–controlled</span></span>
<span data-ttu-id="427a3-200">Tato procedura obsahuje ukázku dokončeného hlášení do skladového místa, které není řízeno registrační značkou.</span><span class="sxs-lookup"><span data-stu-id="427a3-200">This procedure shows an example of reporting as finished to a location that isn't license plate–controlled.</span></span> <span data-ttu-id="427a3-201">Předpokladem pro tento úkol je příslušné pracovní pravidlo.</span><span class="sxs-lookup"><span data-stu-id="427a3-201">An applicable work policy is the prerequisite for this task.</span></span> <span data-ttu-id="427a3-202">Předchozí procedura popisovala nastavení pracovních zásad.</span><span class="sxs-lookup"><span data-stu-id="427a3-202">The previous procedure shows the setup of the work policy.</span></span> 

<span data-ttu-id="427a3-203">KROKY (25)</span><span class="sxs-lookup"><span data-stu-id="427a3-203">STEPS (25)</span></span>

<table>
<tbody>
<tr>
<td colspan="3"><span data-ttu-id="427a3-204"><strong>Dílčí úkol: Nastavení výstupního umístění.</strong></span><span class="sxs-lookup"><span data-stu-id="427a3-204"><strong>Sub-task: Set up an output location.</strong></span></span></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td><span data-ttu-id="427a3-205">Přejděte na nabídce Správa organizace &gt; Zdroje &gt; Skupiny prostředků.</span><span class="sxs-lookup"><span data-stu-id="427a3-205">Go to Organization administration &gt; Resources &gt; Resource groups.</span></span></td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td><span data-ttu-id="427a3-206">V seznamu vyberte skupinu prostředků '5102'.</span><span class="sxs-lookup"><span data-stu-id="427a3-206">In the list, select resource group '5102'.</span></span></td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td><span data-ttu-id="427a3-207">Klikněte na možnost Upravit.</span><span class="sxs-lookup"><span data-stu-id="427a3-207">Click Edit.</span></span></td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td><span data-ttu-id="427a3-208">V poli Výstupní sklad vyberte 51.</span><span class="sxs-lookup"><span data-stu-id="427a3-208">In the Output warehouse field, enter '51'.</span></span></td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td><span data-ttu-id="427a3-209">V poli Výstupní umístění vyberte 001.</span><span class="sxs-lookup"><span data-stu-id="427a3-209">In the Output location field, enter '001'.</span></span></td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td><span data-ttu-id="427a3-210">Umístění 001 není umístění řízené registrační značkou.</span><span class="sxs-lookup"><span data-stu-id="427a3-210">Location 001 isn't a license plate–controlled location.</span></span> <span data-ttu-id="427a3-211">Umístění výstupu bez registrační značky můžete nastavit pouze v případě, že pro umístění existuje příslušné pracovní pravidlo.</span><span class="sxs-lookup"><span data-stu-id="427a3-211">You can set up a non–license plate output location only if an applicable work policy exists for the location.</span></span></td>
</tr>
<tr>
<td colspan="3"><span data-ttu-id="427a3-212"><strong>Dílčí úkol: Vytvoření výrobní zakázky a její ohlášení jako dokončené.</strong></span><span class="sxs-lookup"><span data-stu-id="427a3-212"><strong>Sub-task: Create a production order and report it as finished.</strong></span></span></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td><span data-ttu-id="427a3-213">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="427a3-213">Close the page.</span></span></td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td><span data-ttu-id="427a3-214">Přejděte na Řízení výroby &gt; Výrobní zakázky &gt; Všechny výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="427a3-214">Go to Production control &gt; Production orders &gt; All production orders.</span></span></td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td><span data-ttu-id="427a3-215">Klikněte na možnost Nová výrobní zakázka.</span><span class="sxs-lookup"><span data-stu-id="427a3-215">Click New production order.</span></span></td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td><span data-ttu-id="427a3-216">V poli Číslo zboží zadejte 'L0101'.</span><span class="sxs-lookup"><span data-stu-id="427a3-216">In the Item number field, enter 'L0101'.</span></span></td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td><span data-ttu-id="427a3-217">Klepněte na volbu Nový.</span><span class="sxs-lookup"><span data-stu-id="427a3-217">Click Create.</span></span></td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td><span data-ttu-id="427a3-218">V podokně akcí klikněte na možnost Výrobní zakázka.</span><span class="sxs-lookup"><span data-stu-id="427a3-218">On the Action Pane, click Production order.</span></span></td>
</tr>
<tr>
<td></td>
<td>7.</td>
<td><span data-ttu-id="427a3-219">Klepněte na Odhad.</span><span class="sxs-lookup"><span data-stu-id="427a3-219">Click Estimate.</span></span></td>
</tr>
<tr>
<td></td>
<td>8.</td>
<td><span data-ttu-id="427a3-220">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="427a3-220">Click OK.</span></span></td>
</tr>
<tr>
<td></td>
<td>9.</td>
<td><span data-ttu-id="427a3-221">Klepněte na tlačítko Start.</span><span class="sxs-lookup"><span data-stu-id="427a3-221">Click Start.</span></span></td>
</tr>
<tr>
<td></td>
<td>10.</td>
<td><span data-ttu-id="427a3-222">Klepněte na kartuObecné.</span><span class="sxs-lookup"><span data-stu-id="427a3-222">Click the General tab.</span></span></td>
</tr>
<tr>
<td></td>
<td>11.</td>
<td><span data-ttu-id="427a3-223">V poli Automatická spotřeba kusovníku vyberte hodnotu „Nikdy“.</span><span class="sxs-lookup"><span data-stu-id="427a3-223">In the Automatic BOM consumption field, select 'Never'.</span></span></td>
</tr>
<tr>
<td></td>
<td>12.</td>
<td><span data-ttu-id="427a3-224">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="427a3-224">Click OK.</span></span></td>
</tr>
<tr>
<td></td>
<td>13.</td>
<td><span data-ttu-id="427a3-225">Klepněte na možnost Vykázat jako dokončené.</span><span class="sxs-lookup"><span data-stu-id="427a3-225">Click Report as finished.</span></span></td>
</tr>
<tr>
<td></td>
<td>14.</td>
<td><span data-ttu-id="427a3-226">Klepněte na kartuObecné.</span><span class="sxs-lookup"><span data-stu-id="427a3-226">Click the General tab.</span></span></td>
</tr>
<tr>
<td></td>
<td>15.</td>
<td><span data-ttu-id="427a3-227">Vyberte možnost Ano v poli Akceptovat chybu.</span><span class="sxs-lookup"><span data-stu-id="427a3-227">Select Yes in the Accept error field.</span></span></td>
</tr>
<tr>
<td></td>
<td>16.</td>
<td><span data-ttu-id="427a3-228">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="427a3-228">Click OK.</span></span></td>
</tr>
<tr>
<td></td>
<td>17.</td>
<td><span data-ttu-id="427a3-229">V podokně akcí klikněte na možnost Sklad.</span><span class="sxs-lookup"><span data-stu-id="427a3-229">On the Action Pane, click Warehouse.</span></span></td>
</tr>
<tr>
<td></td>
<td>18.</td>
<td><span data-ttu-id="427a3-230">Klepněte na tlačítko Podrobnosti práce.</span><span class="sxs-lookup"><span data-stu-id="427a3-230">Click Work details.</span></span></td>
</tr>
<tr>
<td></td>
<td>19.</td>
<td><span data-ttu-id="427a3-231">Pokud byla výrobní zakázka ohlášena jako dokončená, žádná práce nebyla pro vyskladnění vytvořena.</span><span class="sxs-lookup"><span data-stu-id="427a3-231">When the production order was reported as finished, no work was generated for put-away.</span></span> <span data-ttu-id="427a3-232">K tomu dochází, protože jsou definovány zásady práce, které brání generování práce, když je produkt L0101 ohlášen za dokončený v umístění 001.</span><span class="sxs-lookup"><span data-stu-id="427a3-232">This occurs because a work policy is defined that prevents work from being generated when product L0101 is reported as finished to location 001.</span></span></td>
</tr>
</tbody>
</table>




