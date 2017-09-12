---
title: "Názvosloví čísel a názvů variant produktu"
description: "Toto téma popisuje, jak nastavit názvosloví pro čísla produktu, které nahradí opravený formát [základní produkt - konfigurace – velikost – barva – styl]. Nové názvosloví má cílený formát, který zahrnuje číslo základního produktu, rozměry aktivního produktu a textové oddělovače podle vašeho výběru. Můžete také vytvořit názvosloví pro názvy produktů. A konečně můžete také vytvořit názvosloví k identifikaci konfigurací, které jsou vytvořeny konfigurátorem produktu založeném na omezeních. Tato názvosloví můžou obsahovat atributy podle vašeho výběru."
author: roxanadiaconu
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 220104
ms.assetid: 3fe69fb7-5c32-423c-98a8-2f53186cda68
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: d1a9ced00d8dc09e59512056392a250a76ba5b97
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---

# <a name="nomenclature-of-product-variant-numbers-and-names"></a><span data-ttu-id="171e3-107">Názvosloví čísel a názvů variant produktu</span><span class="sxs-lookup"><span data-stu-id="171e3-107">Nomenclature of product variant numbers and names</span></span>

<span data-ttu-id="171e3-108">Toto téma popisuje, jak nastavit názvosloví pro čísla produktu, které nahradí opravený formát [základní produkt - konfigurace – velikost – barva – styl].</span><span class="sxs-lookup"><span data-stu-id="171e3-108">This topic describes how you can set up a product number nomenclature to replace the fixed [Product master number - Configuration - Size - Color - Style] format.</span></span> <span data-ttu-id="171e3-109">Nové názvosloví má cílený formát, který zahrnuje číslo základního produktu, rozměry aktivního produktu a textové oddělovače podle vašeho výběru.</span><span class="sxs-lookup"><span data-stu-id="171e3-109">The new nomenclature has a targeted format that includes the product master number, active product dimensions, and text delimiters of your choice.</span></span> <span data-ttu-id="171e3-110">Můžete také vytvořit názvosloví pro názvy produktů.</span><span class="sxs-lookup"><span data-stu-id="171e3-110">You can also create a nomenclature for product names.</span></span> <span data-ttu-id="171e3-111">A konečně můžete také vytvořit názvosloví k identifikaci konfigurací, které jsou vytvořeny konfigurátorem produktu založeném na omezeních.</span><span class="sxs-lookup"><span data-stu-id="171e3-111">Finally, you can build a nomenclature to identify configurations that are created by the constraint-based product configurator.</span></span> <span data-ttu-id="171e3-112">Tato názvosloví můžou obsahovat atributy podle vašeho výběru.</span><span class="sxs-lookup"><span data-stu-id="171e3-112">These nomenclatures can contain attributes of your choice.</span></span>

<span data-ttu-id="171e3-113">Nová názvosloví pro čísla variant produktu a názvy variant produktu umožňují zahrnout segmenty do identifikátorů variant produktu.</span><span class="sxs-lookup"><span data-stu-id="171e3-113">The new nomenclatures for product variant numbers and product variant names let you include segments in the identifiers for product variants.</span></span> <span data-ttu-id="171e3-114">Tyto segmenty mohou obsahovat číslo a název základního produktu, ID a názvy dimenzí produktu, číselné řady, konstanty textu a atributy.</span><span class="sxs-lookup"><span data-stu-id="171e3-114">These segments can include the product master number and name, product dimension IDs and names, number sequences, text constants, and attributes.</span></span> <span data-ttu-id="171e3-115">Tato funkce umožňuje rychle najít konkrétní variantu produktu, když vytváříte nákupní nebo prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="171e3-115">This functionality lets you quickly find a specific product variant when you create a sales order or a purchase order.</span></span> <span data-ttu-id="171e3-116">Názvosloví pro čísla variant produktu i názvy variant produktu se vytváří na stránce **Názvosloví produktu**.</span><span class="sxs-lookup"><span data-stu-id="171e3-116">You create nomenclatures for both product variant numbers and product variant names by using the **Product nomenclature** page.</span></span> <span data-ttu-id="171e3-117">Tuto stránku otevřete tak, že kliknete na **Správa informací o produktu** &gt; **Nastavení**.</span><span class="sxs-lookup"><span data-stu-id="171e3-117">To open this page, click **Product information management** &gt; **Setup**.</span></span>

## <a name="nomenclature-of-predefined-product-variants"></a><span data-ttu-id="171e3-118">Názvosloví předdefinovaných variant produktu</span><span class="sxs-lookup"><span data-stu-id="171e3-118">Nomenclature of predefined product variants</span></span>
<span data-ttu-id="171e3-119">Varianty produktu jsou generovány pro hlavní produkty podle jedné ze tří technologií konfigurace:</span><span class="sxs-lookup"><span data-stu-id="171e3-119">Product variants are generated for product masters according to one of three configuration technologies:</span></span>

-   <span data-ttu-id="171e3-120">Předem definované varianty</span><span class="sxs-lookup"><span data-stu-id="171e3-120">Predefined variants</span></span>
-   <span data-ttu-id="171e3-121">Založené na omezeních</span><span class="sxs-lookup"><span data-stu-id="171e3-121">Constraint-based</span></span>
-   <span data-ttu-id="171e3-122">Založené na dimenzi</span><span class="sxs-lookup"><span data-stu-id="171e3-122">Dimension-based</span></span>

<span data-ttu-id="171e3-123">Každá varianta produktu má číslo a název a názvosloví identifikace variant produktu umožňuje vybrat segmenty, které budou zahrnuty do každého čísla nebo názvu varianty produktu.</span><span class="sxs-lookup"><span data-stu-id="171e3-123">Each product variant has a number and a name, and the product variant identification nomenclatures let you select the segments that will be included in each product variant number or name.</span></span> <span data-ttu-id="171e3-124">Můžete vybrat následující segmenty na stránce **Názvosloví produktu**:</span><span class="sxs-lookup"><span data-stu-id="171e3-124">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="171e3-125">Číslo základního produktu</span><span class="sxs-lookup"><span data-stu-id="171e3-125">Product master number</span></span>
-   <span data-ttu-id="171e3-126">Název základního produktu</span><span class="sxs-lookup"><span data-stu-id="171e3-126">Product master name</span></span>
-   <span data-ttu-id="171e3-127">Hodnota číselné řady</span><span class="sxs-lookup"><span data-stu-id="171e3-127">Number sequence value</span></span>
-   <span data-ttu-id="171e3-128">Textová konstanta</span><span class="sxs-lookup"><span data-stu-id="171e3-128">Text constant</span></span>
-   <span data-ttu-id="171e3-129">Dimenze produktu</span><span class="sxs-lookup"><span data-stu-id="171e3-129">Product dimensions</span></span>
    -   <span data-ttu-id="171e3-130">ID nebo název konfigurace</span><span class="sxs-lookup"><span data-stu-id="171e3-130">Configuration ID or name</span></span>
    -   <span data-ttu-id="171e3-131">ID nebo název barvy</span><span class="sxs-lookup"><span data-stu-id="171e3-131">Color ID or name</span></span>
    -   <span data-ttu-id="171e3-132">ID nebo název velikosti</span><span class="sxs-lookup"><span data-stu-id="171e3-132">Size ID or name</span></span>
    -   <span data-ttu-id="171e3-133">ID nebo název stylu</span><span class="sxs-lookup"><span data-stu-id="171e3-133">Style ID or name</span></span>

<span data-ttu-id="171e3-134">Po definování názvosloví čísel identifikace varianty produktu může být produkt přidružen ke skupině dimenzí produktu.</span><span class="sxs-lookup"><span data-stu-id="171e3-134">After you define a product variant identification number nomenclature, you can associate it with a product dimension group.</span></span> <span data-ttu-id="171e3-135">Všem základním produktům, které odkazují na tuto skupinu dimenzí produktu, pak budou přiřazena čísla variant produktů podle klasifikace.</span><span class="sxs-lookup"><span data-stu-id="171e3-135">All product masters that reference this product dimension group will then be assigned product variant numbers according to the nomenclature.</span></span> <span data-ttu-id="171e3-136">Názvosloví pro názvy variant produktu ale nelze přidružit skupinám dimenzí produktu.</span><span class="sxs-lookup"><span data-stu-id="171e3-136">However, product variant name nomenclatures can't be associated with product dimension groups.</span></span> <span data-ttu-id="171e3-137">Můžete také přiřadit názvosloví pro identifikaci variant produktu přímo základnímu produktu.</span><span class="sxs-lookup"><span data-stu-id="171e3-137">You can also assign a product variant identification nomenclature directly to a product master.</span></span> <span data-ttu-id="171e3-138">V takovém případě budou variantám produktu, které patří k základnímu produktu, přiřazena čísla a názvy variant produktu podle určených názvosloví.</span><span class="sxs-lookup"><span data-stu-id="171e3-138">In this case, the product variants that belong to the product master will be assigned product variant numbers and names according to the nomenclatures.</span></span>

### <a name="example"></a><span data-ttu-id="171e3-139">Příklad</span><span class="sxs-lookup"><span data-stu-id="171e3-139">Example</span></span>

<span data-ttu-id="171e3-140">Tričko (TS1234) se vyrábí ve třech velikostech (S, M, L), čtyřech barvách (červená, zelená, modrá a žlutá) a dvou stylech (Polo, V).</span><span class="sxs-lookup"><span data-stu-id="171e3-140">A T-shirt (TS1234) is produced in three sizes (S, M, L), four colors (Red, Green, Blue, Yellow), and two styles (Polo, V).</span></span> <span data-ttu-id="171e3-141">Proto může existovat 24 variant produktu (= 3 x 4 x 2).</span><span class="sxs-lookup"><span data-stu-id="171e3-141">Therefore, 24 product variants are possible (= 3 × 4 × 2).</span></span> <span data-ttu-id="171e3-142">Vytvoříte názvosloví čísel variant produktů, které obsahuje následující segmenty:</span><span class="sxs-lookup"><span data-stu-id="171e3-142">You create a product variant number nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="171e3-143">Číslo základního produktu</span><span class="sxs-lookup"><span data-stu-id="171e3-143">Product master number</span></span>
2.  <span data-ttu-id="171e3-144">Textová konstanta: "-"</span><span class="sxs-lookup"><span data-stu-id="171e3-144">Text constant: "-"</span></span>
3.  <span data-ttu-id="171e3-145">Barva</span><span class="sxs-lookup"><span data-stu-id="171e3-145">Color</span></span>
4.  <span data-ttu-id="171e3-146">Textová konstanta: "-"</span><span class="sxs-lookup"><span data-stu-id="171e3-146">Text constant: "-"</span></span>
5.  <span data-ttu-id="171e3-147">Velikost</span><span class="sxs-lookup"><span data-stu-id="171e3-147">Size</span></span>
6.  <span data-ttu-id="171e3-148">Textová konstanta: "-"</span><span class="sxs-lookup"><span data-stu-id="171e3-148">Text constant: "-"</span></span>
7.  <span data-ttu-id="171e3-149">Styl</span><span class="sxs-lookup"><span data-stu-id="171e3-149">Style</span></span>

<span data-ttu-id="171e3-150">V tomto případě bude číslo varianty produktu pro červené, malé polo tričko: TS1234-Red-Small-Polo.</span><span class="sxs-lookup"><span data-stu-id="171e3-150">In this case, the product variant number for a red, small, polo T-shirt will be TS1234-Red-Small-Polo.</span></span>

## <a name="nomenclature-of-constraintbased-configurations"></a><span data-ttu-id="171e3-151">Názvosloví konfigurací založených na omezeních</span><span class="sxs-lookup"><span data-stu-id="171e3-151">Nomenclature of constraintbased configurations</span></span>
<span data-ttu-id="171e3-152">Pro konfigurace založené na omezeních můžete vytvořit vyhrazené názvosloví pro dimenzi konfiguračního produktu.</span><span class="sxs-lookup"><span data-stu-id="171e3-152">For constraint-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="171e3-153">Můžete vybrat následující segmenty na stránce **Názvosloví produktu**:</span><span class="sxs-lookup"><span data-stu-id="171e3-153">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="171e3-154">Hodnota číselné řady</span><span class="sxs-lookup"><span data-stu-id="171e3-154">Number sequence value</span></span>
-   <span data-ttu-id="171e3-155">Textová konstanta</span><span class="sxs-lookup"><span data-stu-id="171e3-155">Text constant</span></span>
-   <span data-ttu-id="171e3-156">Hodnota atributu</span><span class="sxs-lookup"><span data-stu-id="171e3-156">Attribute value</span></span>

<span data-ttu-id="171e3-157">Jednotlivé komponenty v modelu konfigurace produktu můžou mít vlastní názvosloví konfigurace.</span><span class="sxs-lookup"><span data-stu-id="171e3-157">Each component in a product configuration model can have its own configuration nomenclature.</span></span> <span data-ttu-id="171e3-158">Lze použít pouze atributy, které patří ke komponentě.</span><span class="sxs-lookup"><span data-stu-id="171e3-158">Only attributes that belong to the component can be used.</span></span> <span data-ttu-id="171e3-159">Nemohou být použity atributy z dílčích komponent nebo požadavky uživatelů.</span><span class="sxs-lookup"><span data-stu-id="171e3-159">Attributes from subcomponents or user requirements can't be used.</span></span>

### <a name="example"></a><span data-ttu-id="171e3-160">Příklad</span><span class="sxs-lookup"><span data-stu-id="171e3-160">Example</span></span>

<span data-ttu-id="171e3-161">Model konfigurace produktu má kořenovou komponentu se dvěma atributy:</span><span class="sxs-lookup"><span data-stu-id="171e3-161">A product configuration model has a root component that has two attributes:</span></span>

-   <span data-ttu-id="171e3-162">Materiál (plast, dřevo, ocel.)</span><span class="sxs-lookup"><span data-stu-id="171e3-162">Material (Plastic, Wood, Steel)</span></span>
-   <span data-ttu-id="171e3-163">Délka (10... 100)</span><span class="sxs-lookup"><span data-stu-id="171e3-163">Length (10...100)</span></span>

<span data-ttu-id="171e3-164">Vytvoříte názvosloví konfigurace, které obsahuje následující segmenty:</span><span class="sxs-lookup"><span data-stu-id="171e3-164">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="171e3-165">Hodnota atributu: materiál</span><span class="sxs-lookup"><span data-stu-id="171e3-165">Attribute value: Material</span></span>
2.  <span data-ttu-id="171e3-166">Textová konstanta: "AAA"</span><span class="sxs-lookup"><span data-stu-id="171e3-166">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="171e3-167">Hodnota atributu: délka</span><span class="sxs-lookup"><span data-stu-id="171e3-167">Attribute value: Length</span></span>

<span data-ttu-id="171e3-168">V takovém případě bude ID konfigurace dřevěného materiálu, který má délku 78, WoodAAA78.</span><span class="sxs-lookup"><span data-stu-id="171e3-168">In this case, the configuration ID for wood material that has a length of 78 will be WoodAAA78.</span></span>

## <a name="nomenclature-of-dimensionbased-configurations"></a><span data-ttu-id="171e3-169">Názvosloví konfigurací založených na dimenzích</span><span class="sxs-lookup"><span data-stu-id="171e3-169">Nomenclature of dimensionbased configurations</span></span>
<span data-ttu-id="171e3-170">Pro konfigurace založené na dimenzích můžete vytvořit vyhrazené názvosloví pro dimenzi konfiguračního produktu.</span><span class="sxs-lookup"><span data-stu-id="171e3-170">For dimension-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="171e3-171">Můžete vybrat následující segmenty na stránce **Názvosloví produktu**:</span><span class="sxs-lookup"><span data-stu-id="171e3-171">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="171e3-172">Hodnota číselné řady</span><span class="sxs-lookup"><span data-stu-id="171e3-172">Number sequence value</span></span>
-   <span data-ttu-id="171e3-173">Textová konstanta</span><span class="sxs-lookup"><span data-stu-id="171e3-173">Text constant</span></span>
-   <span data-ttu-id="171e3-174">Položka konfigurační skupiny</span><span class="sxs-lookup"><span data-stu-id="171e3-174">Configuration group item</span></span>

<span data-ttu-id="171e3-175">Můžete definovat názvosloví konfigurace pro kusovníky (BOM).</span><span class="sxs-lookup"><span data-stu-id="171e3-175">You can define a configuration nomenclature for a bill of materials (BOM).</span></span>

### <a name="example"></a><span data-ttu-id="171e3-176">Příklad</span><span class="sxs-lookup"><span data-stu-id="171e3-176">Example</span></span>

<span data-ttu-id="171e3-177">Kusovník má čtyři řádky kusovníku, které jsou rozděleny do dvou konfiguračních skupin:</span><span class="sxs-lookup"><span data-stu-id="171e3-177">A BOM has four BOM lines that are divided into two configuration groups:</span></span>

-   <span data-ttu-id="171e3-178">Řádek kusovníku: M0007, standardní skříň</span><span class="sxs-lookup"><span data-stu-id="171e3-178">BOM line: M0007, Standard cabinet</span></span>
    -   <span data-ttu-id="171e3-179">Skupina konfigurace: Skříň</span><span class="sxs-lookup"><span data-stu-id="171e3-179">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="171e3-180">Řádek kusovníku: M0008, vysoká koncová skříň</span><span class="sxs-lookup"><span data-stu-id="171e3-180">BOM line: M0008, High end cabinet</span></span>
    -   <span data-ttu-id="171e3-181">Skupina konfigurace: Skříň</span><span class="sxs-lookup"><span data-stu-id="171e3-181">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="171e3-182">Řádek kusovníku: M0021, přední potah mřížky</span><span class="sxs-lookup"><span data-stu-id="171e3-182">BOM line: M0021, Front grill cloth</span></span>
    -   <span data-ttu-id="171e3-183">Skupina konfigurace: Přední mřížka</span><span class="sxs-lookup"><span data-stu-id="171e3-183">Configuration group: Front grill</span></span>
-   <span data-ttu-id="171e3-184">Řádek kusovníku: M0022, přední kovová mřížka</span><span class="sxs-lookup"><span data-stu-id="171e3-184">BOM line: M0022, Front grill metal</span></span>
    -   <span data-ttu-id="171e3-185">Skupina konfigurace: Přední mřížka</span><span class="sxs-lookup"><span data-stu-id="171e3-185">Configuration group: Front grill</span></span>

<span data-ttu-id="171e3-186">Vytvoříte názvosloví konfigurace, které obsahuje následující segmenty:</span><span class="sxs-lookup"><span data-stu-id="171e3-186">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="171e3-187">Skupina konfigurace: Skříň</span><span class="sxs-lookup"><span data-stu-id="171e3-187">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="171e3-188">Textová konstanta: "&"</span><span class="sxs-lookup"><span data-stu-id="171e3-188">Text constant: "&"</span></span>
3.  <span data-ttu-id="171e3-189">Skupina konfigurace: Přední mřížka</span><span class="sxs-lookup"><span data-stu-id="171e3-189">Configuration group: Front grill</span></span>

<span data-ttu-id="171e3-190">V tomto případě bude ID konfigurace standardní skříně s přední látkovou mřížkou M0007&M0021.</span><span class="sxs-lookup"><span data-stu-id="171e3-190">In this case, the configuration ID for a standard cabinet that has a cloth front grill will be M0007&M0021.</span></span>

## <a name="nomenclature-for-a-combination-of-product-variants-and-configurations"></a><span data-ttu-id="171e3-191">Názvosloví kombinace variant a konfigurací produktu</span><span class="sxs-lookup"><span data-stu-id="171e3-191">Nomenclature for a combination of product variants and configurations</span></span>
<span data-ttu-id="171e3-192">Při použití technologie konfigurace založené na omezeních nebo na dimenzích ke konfiguraci variant produktu pro základní produkt mohou čísla variant produktu zahrnovat čísla variant produktu z konfigurační dimenze.</span><span class="sxs-lookup"><span data-stu-id="171e3-192">When you use either the constraint-based configuration technology or the dimension-based configuration technology to configure product variants for a product master, the product variant numbers of the product variants can include the nomenclature from the configuration dimension.</span></span> <span data-ttu-id="171e3-193">Chcete-li nakonfigurovat varianty, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="171e3-193">Follow these steps to configure variants.</span></span>

1.  <span data-ttu-id="171e3-194">Na stránce **Názvosloví produktu** definujte názvosloví čísel variant produktů, které zahrnuje konfigurační dimenzi.</span><span class="sxs-lookup"><span data-stu-id="171e3-194">On the **Product nomenclature** page, define a product variant number nomenclature that includes the configuration dimension.</span></span>
2.  <span data-ttu-id="171e3-195">Toto názvosloví přiřaďte skupině dimenze produktu s dimenzí konfigurace.</span><span class="sxs-lookup"><span data-stu-id="171e3-195">Assign the nomenclature to a product dimension group that has the configuration dimension.</span></span>
3.  <span data-ttu-id="171e3-196">Definujte názvosloví konfigurace pro komponenty nebo kusovníky, které budou použity ke konfiguraci variant produktu.</span><span class="sxs-lookup"><span data-stu-id="171e3-196">Define a configuration nomenclature for the components or BOMs that will be used to configure the product variants.</span></span>

<span data-ttu-id="171e3-197">Můžete také vytvořit názvosloví pro názvy variant produktů.</span><span class="sxs-lookup"><span data-stu-id="171e3-197">You can also create nomenclatures for the product variant names.</span></span> <span data-ttu-id="171e3-198">Názvy variant produktů lze nakonfigurovat tak, aby zahrnovaly ID nebo název konfigurace.</span><span class="sxs-lookup"><span data-stu-id="171e3-198">The product variant names can be configured to include the configuration ID or name.</span></span>

### <a name="example-for-constraint-based-configurations"></a><span data-ttu-id="171e3-199">Příklad konfigurací založených na omezeních</span><span class="sxs-lookup"><span data-stu-id="171e3-199">Example for constraint-based configurations</span></span>

<span data-ttu-id="171e3-200">V tomto příkladu můžete používat číslo varianty produktu, která se skládá z následujících segmentů:</span><span class="sxs-lookup"><span data-stu-id="171e3-200">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="171e3-201">Číslo základního produktu</span><span class="sxs-lookup"><span data-stu-id="171e3-201">Product master number</span></span>
2.  <span data-ttu-id="171e3-202">Textová konstanta "\_"</span><span class="sxs-lookup"><span data-stu-id="171e3-202">Text constant "\_"</span></span>
3.  <span data-ttu-id="171e3-203">Konfigurace</span><span class="sxs-lookup"><span data-stu-id="171e3-203">Configuration</span></span>

<span data-ttu-id="171e3-204">Názvosloví konfigurace sestává z následujících segmentů:</span><span class="sxs-lookup"><span data-stu-id="171e3-204">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="171e3-205">Hodnota atributu: materiál</span><span class="sxs-lookup"><span data-stu-id="171e3-205">Attribute value: Material</span></span>
2.  <span data-ttu-id="171e3-206">Textová konstanta: "AAA"</span><span class="sxs-lookup"><span data-stu-id="171e3-206">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="171e3-207">Hodnota atributu: délka</span><span class="sxs-lookup"><span data-stu-id="171e3-207">Attribute value: Length</span></span>

<span data-ttu-id="171e3-208">Pro segmenty můžete zadat následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="171e3-208">You enter the following values for segments:</span></span>

-   <span data-ttu-id="171e3-209">Číslo základního produktu = **M0099**</span><span class="sxs-lookup"><span data-stu-id="171e3-209">Product master number = **M0099**</span></span>
-   <span data-ttu-id="171e3-210">Materiál = **plast**</span><span class="sxs-lookup"><span data-stu-id="171e3-210">Material = **Plastic**</span></span>
-   <span data-ttu-id="171e3-211">Délka = **12**</span><span class="sxs-lookup"><span data-stu-id="171e3-211">Length = **12**</span></span>

<span data-ttu-id="171e3-212">V tomto případě bude číslo varianty produktu M0099\_PlasticAAA12.</span><span class="sxs-lookup"><span data-stu-id="171e3-212">In this case, the product variant number will be M0099\_PlasticAAA12.</span></span>

### <a name="example-for-dimension-based-configurations"></a><span data-ttu-id="171e3-213">Příklad konfigurací založených na dimenzích</span><span class="sxs-lookup"><span data-stu-id="171e3-213">Example for dimension-based configurations</span></span>

<span data-ttu-id="171e3-214">V tomto příkladu můžete používat číslo varianty produktu, která se skládá z následujících segmentů:</span><span class="sxs-lookup"><span data-stu-id="171e3-214">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="171e3-215">Číslo základního produktu</span><span class="sxs-lookup"><span data-stu-id="171e3-215">Product master number</span></span>
2.  <span data-ttu-id="171e3-216">Textová konstanta: "//"</span><span class="sxs-lookup"><span data-stu-id="171e3-216">Text constant "//"</span></span>
3.  <span data-ttu-id="171e3-217">Konfigurace</span><span class="sxs-lookup"><span data-stu-id="171e3-217">Configuration</span></span>

<span data-ttu-id="171e3-218">Názvosloví konfigurace sestává z následujících segmentů:</span><span class="sxs-lookup"><span data-stu-id="171e3-218">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="171e3-219">Skupina konfigurace: Skříň</span><span class="sxs-lookup"><span data-stu-id="171e3-219">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="171e3-220">Textová konstanta: "&"</span><span class="sxs-lookup"><span data-stu-id="171e3-220">Text constant: "&"</span></span>
3.  <span data-ttu-id="171e3-221">Skupina konfigurace: Přední mřížka</span><span class="sxs-lookup"><span data-stu-id="171e3-221">Configuration group: Front grill</span></span>

<span data-ttu-id="171e3-222">Pro segmenty můžete zadat následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="171e3-222">You enter the following values for segments:</span></span>

-   <span data-ttu-id="171e3-223">Číslo základního produktu = **D0123**</span><span class="sxs-lookup"><span data-stu-id="171e3-223">Product master number = **D0123**</span></span>
-   <span data-ttu-id="171e3-224">Skříň = **M0008**</span><span class="sxs-lookup"><span data-stu-id="171e3-224">Cabinet = **M0008**</span></span>
-   <span data-ttu-id="171e3-225">Přední mřížka = **M0022**</span><span class="sxs-lookup"><span data-stu-id="171e3-225">Front grill = **M0022**</span></span>

<span data-ttu-id="171e3-226">V tomto případě bude číslo varianty produktu D0123//M0008&M0022.</span><span class="sxs-lookup"><span data-stu-id="171e3-226">In this case, the product variant number will be D0123//M0008&M0022.</span></span>

## <a name="numbering-conflicts"></a><span data-ttu-id="171e3-227">Číslování konfliktů</span><span class="sxs-lookup"><span data-stu-id="171e3-227">Numbering conflicts</span></span>
<span data-ttu-id="171e3-228">V některých případech nemusí názvosloví čísel variant produktů, které nastavíte, vytvářet čísla variant jedinečných produktů.</span><span class="sxs-lookup"><span data-stu-id="171e3-228">In some cases, a product variant number nomenclature that you set up might not produce unique product variant numbers.</span></span> <span data-ttu-id="171e3-229">Čísla nebudou jedinečná například, když jedna aktivní dimenze produktu není součástí názvosloví pro základní produkt využívající technologii konfigurace předem definované varianty.</span><span class="sxs-lookup"><span data-stu-id="171e3-229">For example, the product variant numbers won't be unique if one active product dimension isn't included in the nomenclature for a product master that uses the predefined variant configuration technology.</span></span> <span data-ttu-id="171e3-230">Způsob, kterým budete řešit konflikty je různý, podle technologie konfigurace.</span><span class="sxs-lookup"><span data-stu-id="171e3-230">The way that you handle conflicts varies, depending on the configuration technology.</span></span>

### <a name="predefined-variants"></a><span data-ttu-id="171e3-231">Předem definované varianty</span><span class="sxs-lookup"><span data-stu-id="171e3-231">Predefined variants</span></span>

<span data-ttu-id="171e3-232">Pokud se pokusíte automaticky nebo ručně vytvořit varianty produktu, kde jeden nebo více končí stejným číslem varianty produktu, dojde k chybě.</span><span class="sxs-lookup"><span data-stu-id="171e3-232">An error occurs if you try to manually create or automatically generate product variants, and more than one product variant ends up with the same product variant number.</span></span> <span data-ttu-id="171e3-233">Této situaci se lze vyhnout tak, že budete ve skupině dimenzí produktu používat všechny aktivní dimenze produktu.</span><span class="sxs-lookup"><span data-stu-id="171e3-233">To avoid this scenario, you should use all active product dimensions in the product dimension group.</span></span> <span data-ttu-id="171e3-234">Alternativně zahrňte číselnou řadu, což vám pomůže zaručit jedinečnost čísel variat produktu.</span><span class="sxs-lookup"><span data-stu-id="171e3-234">Alternatively, include a number sequence to help guarantee that the product variant numbers are unique.</span></span>

### <a name="constraint-based-configurations"></a><span data-ttu-id="171e3-235">Konfigurace založené na omezeních</span><span class="sxs-lookup"><span data-stu-id="171e3-235">Constraint-based configurations</span></span>

<span data-ttu-id="171e3-236">V závislosti na názvosloví se systém může pokusit přiřadit nejedinečné číslo varianty produktu ke konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="171e3-236">Depending on the nomenclature, the system might try to assign a non-unique product variant number to a configuration.</span></span> <span data-ttu-id="171e3-237">V takovém případě systém používá číselnou řadu pro konfigurační dimenzi jako číslo varianty produktu. V takovém případě bude zobrazena varovná zpráva.</span><span class="sxs-lookup"><span data-stu-id="171e3-237">In this case, the system uses the number sequence for the configuration dimension as the product variant number instead, and you receive a warning.</span></span> <span data-ttu-id="171e3-238">Této situaci se lze vyhnout tak, že do názvosloví zahrnete dostatek produktů, které pomohou zaručit jedinečná čísla variant produktu.</span><span class="sxs-lookup"><span data-stu-id="171e3-238">To avoid this scenario, you should include enough attributes in the nomenclature to help guarantee unique product variant numbers.</span></span> <span data-ttu-id="171e3-239">Měli byste také zajistit, že je pro komponentu zapnutá možnost **Opakované použití**.</span><span class="sxs-lookup"><span data-stu-id="171e3-239">You should also make sure that the **Reuse** option is turned on for the component.</span></span>

### <a name="dimension-based-configurations"></a><span data-ttu-id="171e3-240">Konfigurace založené na dimenzích</span><span class="sxs-lookup"><span data-stu-id="171e3-240">Dimension-based configurations</span></span>

<span data-ttu-id="171e3-241">Během jednoho kroku procesu konfigurace systém navrhne hodnotu konfigurace podle klasifikace.</span><span class="sxs-lookup"><span data-stu-id="171e3-241">During one step of the configuration process, the system suggests a configuration value according to the nomenclature.</span></span> <span data-ttu-id="171e3-242">V tomto kroku můžete ručně změnit hodnotu konfigurace.</span><span class="sxs-lookup"><span data-stu-id="171e3-242">In this step, you can manually change the configuration value.</span></span> <span data-ttu-id="171e3-243">Po uložení konfigurace systém zkontroluje, zda je hodnota konfigurace jedinečná.</span><span class="sxs-lookup"><span data-stu-id="171e3-243">When you save the configuration, the system verifies that the configuration value is unique.</span></span> <span data-ttu-id="171e3-244">Není-li hodnota, kterou jste zadali jedinečná, zobrazí se chybová zpráva.</span><span class="sxs-lookup"><span data-stu-id="171e3-244">If the value that you entered isn't unique, you receive an error message.</span></span> <span data-ttu-id="171e3-245">Chcete-li uložit konfiguraci, musíte zadat jedinečnou hodnotu konfigurace.</span><span class="sxs-lookup"><span data-stu-id="171e3-245">To save the configuration, you must enter a unique configuration value.</span></span>

<a name="see-also"></a><span data-ttu-id="171e3-246">Viz také</span><span class="sxs-lookup"><span data-stu-id="171e3-246">See also</span></span>
--------

[<span data-ttu-id="171e3-247">Vytvoření názvosloví čísel produktů pro předdefinované varianty produktu</span><span class="sxs-lookup"><span data-stu-id="171e3-247">Create a product number nomenclature for predefined product variants</span></span>](/dynamics365/unified-operations/supply-chain/pim/tasks/create-product-number-nomenclature-predefined-variants-2016-11)

[<span data-ttu-id="171e3-248">Vytvoření názvosloví čísel produktů pro nakonfigurované varianty produktu</span><span class="sxs-lookup"><span data-stu-id="171e3-248">Create a product number nomenclature for configured product variants</span></span>](/dynamics365/unified-operations/supply-chain/pim/tasks/create-product-number-nomenclature-product-variants_2016_11)


