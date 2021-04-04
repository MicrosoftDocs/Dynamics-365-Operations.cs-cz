---
title: Názvosloví čísel a názvů variant produktu
description: Toto téma popisuje, jak nastavit názvosloví pro čísla produktu, které nahradí opravený formát [základní produkt - konfigurace – velikost – barva – styl].
author: roxanadiaconu
manager: tfehr
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResNomenclature, EcoResProductDimensionGroup, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: 220104
ms.assetid: 3fe69fb7-5c32-423c-98a8-2f53186cda68
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: f4d6ece092f2e592351b4081de9b5d17ed3b9a43
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5260616"
---
# <a name="nomenclature-of-product-variant-numbers-and-names"></a><span data-ttu-id="6a2cd-103">Názvosloví čísel a názvů variant produktu</span><span class="sxs-lookup"><span data-stu-id="6a2cd-103">Nomenclature of product variant numbers and names</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6a2cd-104">Toto téma popisuje, jak nastavit názvosloví pro čísla produktu, které nahradí opravený formát [základní produkt - konfigurace – velikost – barva – styl].</span><span class="sxs-lookup"><span data-stu-id="6a2cd-104">This topic describes how you can set up a product number nomenclature to replace the fixed [Product master number - Configuration - Size - Color - Style] format.</span></span> <span data-ttu-id="6a2cd-105">Nové názvosloví má cílený formát, který zahrnuje číslo základního produktu, rozměry aktivního produktu a textové oddělovače podle vašeho výběru.</span><span class="sxs-lookup"><span data-stu-id="6a2cd-105">The new nomenclature has a targeted format that includes the product master number, active product dimensions, and text delimiters of your choice.</span></span> <span data-ttu-id="6a2cd-106">Můžete také vytvořit názvosloví pro názvy produktů.</span><span class="sxs-lookup"><span data-stu-id="6a2cd-106">You can also create a nomenclature for product names.</span></span> <span data-ttu-id="6a2cd-107">A konečně můžete také vytvořit názvosloví k identifikaci konfigurací, které jsou vytvořeny konfigurátorem produktu založeném na omezeních.</span><span class="sxs-lookup"><span data-stu-id="6a2cd-107">Finally, you can build a nomenclature to identify configurations that are created by the constraint-based product configurator.</span></span> <span data-ttu-id="6a2cd-108">Tato názvosloví můžou obsahovat atributy podle vašeho výběru.</span><span class="sxs-lookup"><span data-stu-id="6a2cd-108">These nomenclatures can contain attributes of your choice.</span></span>

<span data-ttu-id="6a2cd-109">Nová názvosloví pro čísla variant produktu a názvy variant produktu umožňují zahrnout segmenty do identifikátorů variant produktu.</span><span class="sxs-lookup"><span data-stu-id="6a2cd-109">The new nomenclatures for product variant numbers and product variant names let you include segments in the identifiers for product variants.</span></span> <span data-ttu-id="6a2cd-110">Tyto segmenty mohou obsahovat číslo a název základního produktu, ID a názvy dimenzí produktu, číselné řady, konstanty textu a atributy.</span><span class="sxs-lookup"><span data-stu-id="6a2cd-110">These segments can include the product master number and name, product dimension IDs and names, number sequences, text constants, and attributes.</span></span> <span data-ttu-id="6a2cd-111">Tato funkce umožňuje rychle najít konkrétní variantu produktu, když vytváříte nákupní nebo prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="6a2cd-111">This functionality lets you quickly find a specific product variant when you create a sales order or a purchase order.</span></span> <span data-ttu-id="6a2cd-112">Názvosloví pro čísla variant produktu i názvy variant produktu se vytváří na stránce **Názvosloví produktu**.</span><span class="sxs-lookup"><span data-stu-id="6a2cd-112">You create nomenclatures for both product variant numbers and product variant names by using the **Product nomenclature** page.</span></span> <span data-ttu-id="6a2cd-113">Tuto stránku otevřete tak, že kliknete na **Správa informací o produktu** &gt; **Nastavení**.</span><span class="sxs-lookup"><span data-stu-id="6a2cd-113">To open this page, click **Product information management** &gt; **Setup**.</span></span>

## <a name="nomenclature-of-predefined-product-variants"></a><span data-ttu-id="6a2cd-114">Názvosloví předdefinovaných variant produktu</span><span class="sxs-lookup"><span data-stu-id="6a2cd-114">Nomenclature of predefined product variants</span></span>
<span data-ttu-id="6a2cd-115">Varianty produktu jsou generovány pro hlavní produkty podle jedné ze tří technologií konfigurace:</span><span class="sxs-lookup"><span data-stu-id="6a2cd-115">Product variants are generated for product masters according to one of three configuration technologies:</span></span>

-   <span data-ttu-id="6a2cd-116">Předem definované varianty</span><span class="sxs-lookup"><span data-stu-id="6a2cd-116">Predefined variants</span></span>
-   <span data-ttu-id="6a2cd-117">Založené na omezeních</span><span class="sxs-lookup"><span data-stu-id="6a2cd-117">Constraint-based</span></span>
-   <span data-ttu-id="6a2cd-118">Založené na dimenzi</span><span class="sxs-lookup"><span data-stu-id="6a2cd-118">Dimension-based</span></span>

<span data-ttu-id="6a2cd-119">Každá varianta produktu má číslo a název a názvosloví identifikace variant produktu umožňuje vybrat segmenty, které budou zahrnuty do každého čísla nebo názvu varianty produktu.</span><span class="sxs-lookup"><span data-stu-id="6a2cd-119">Each product variant has a number and a name, and the product variant identification nomenclatures let you select the segments that will be included in each product variant number or name.</span></span> <span data-ttu-id="6a2cd-120">Můžete vybrat následující segmenty na stránce **Názvosloví produktu**:</span><span class="sxs-lookup"><span data-stu-id="6a2cd-120">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="6a2cd-121">Číslo základního produktu</span><span class="sxs-lookup"><span data-stu-id="6a2cd-121">Product master number</span></span>
-   <span data-ttu-id="6a2cd-122">Název základního produktu</span><span class="sxs-lookup"><span data-stu-id="6a2cd-122">Product master name</span></span>
-   <span data-ttu-id="6a2cd-123">Hodnota číselné řady</span><span class="sxs-lookup"><span data-stu-id="6a2cd-123">Number sequence value</span></span>
-   <span data-ttu-id="6a2cd-124">Textová konstanta</span><span class="sxs-lookup"><span data-stu-id="6a2cd-124">Text constant</span></span>
-   <span data-ttu-id="6a2cd-125">Dimenze produktu</span><span class="sxs-lookup"><span data-stu-id="6a2cd-125">Product dimensions</span></span>
    -   <span data-ttu-id="6a2cd-126">ID nebo název konfigurace</span><span class="sxs-lookup"><span data-stu-id="6a2cd-126">Configuration ID or name</span></span>
    -   <span data-ttu-id="6a2cd-127">ID nebo název barvy</span><span class="sxs-lookup"><span data-stu-id="6a2cd-127">Color ID or name</span></span>
    -   <span data-ttu-id="6a2cd-128">ID nebo název velikosti</span><span class="sxs-lookup"><span data-stu-id="6a2cd-128">Size ID or name</span></span>
    -   <span data-ttu-id="6a2cd-129">ID nebo název stylu</span><span class="sxs-lookup"><span data-stu-id="6a2cd-129">Style ID or name</span></span>

<span data-ttu-id="6a2cd-130">Po definování názvosloví čísel identifikace varianty produktu může být produkt přidružen ke skupině dimenzí produktu.</span><span class="sxs-lookup"><span data-stu-id="6a2cd-130">After you define a product variant identification number nomenclature, you can associate it with a product dimension group.</span></span> <span data-ttu-id="6a2cd-131">Všem základním produktům, které odkazují na tuto skupinu dimenzí produktu, pak budou přiřazena čísla variant produktů podle klasifikace.</span><span class="sxs-lookup"><span data-stu-id="6a2cd-131">All product masters that reference this product dimension group will then be assigned product variant numbers according to the nomenclature.</span></span> <span data-ttu-id="6a2cd-132">Názvosloví pro názvy variant produktu ale nelze přidružit skupinám dimenzí produktu.</span><span class="sxs-lookup"><span data-stu-id="6a2cd-132">However, product variant name nomenclatures can't be associated with product dimension groups.</span></span> <span data-ttu-id="6a2cd-133">Můžete také přiřadit názvosloví pro identifikaci variant produktu přímo základnímu produktu.</span><span class="sxs-lookup"><span data-stu-id="6a2cd-133">You can also assign a product variant identification nomenclature directly to a product master.</span></span> <span data-ttu-id="6a2cd-134">V takovém případě budou variantám produktu, které patří k základnímu produktu, přiřazena čísla a názvy variant produktu podle určených názvosloví.</span><span class="sxs-lookup"><span data-stu-id="6a2cd-134">In this case, the product variants that belong to the product master will be assigned product variant numbers and names according to the nomenclatures.</span></span>

### <a name="example"></a><span data-ttu-id="6a2cd-135">Příklad</span><span class="sxs-lookup"><span data-stu-id="6a2cd-135">Example</span></span>

<span data-ttu-id="6a2cd-136">Tričko (TS1234) se vyrábí ve třech velikostech (S, M, L), čtyřech barvách (červená, zelená, modrá a žlutá) a dvou stylech (Polo, V).</span><span class="sxs-lookup"><span data-stu-id="6a2cd-136">A T-shirt (TS1234) is produced in three sizes (S, M, L), four colors (Red, Green, Blue, Yellow), and two styles (Polo, V).</span></span> <span data-ttu-id="6a2cd-137">Proto může existovat 24 variant produktu (= 3 x 4 x 2).</span><span class="sxs-lookup"><span data-stu-id="6a2cd-137">Therefore, 24 product variants are possible (= 3 × 4 × 2).</span></span> <span data-ttu-id="6a2cd-138">Vytvoříte názvosloví čísel variant produktů, které obsahuje následující segmenty:</span><span class="sxs-lookup"><span data-stu-id="6a2cd-138">You create a product variant number nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="6a2cd-139">Číslo základního produktu</span><span class="sxs-lookup"><span data-stu-id="6a2cd-139">Product master number</span></span>
2.  <span data-ttu-id="6a2cd-140">Textová konstanta: "-"</span><span class="sxs-lookup"><span data-stu-id="6a2cd-140">Text constant: "-"</span></span>
3.  <span data-ttu-id="6a2cd-141">Barva</span><span class="sxs-lookup"><span data-stu-id="6a2cd-141">Color</span></span>
4.  <span data-ttu-id="6a2cd-142">Textová konstanta: "-"</span><span class="sxs-lookup"><span data-stu-id="6a2cd-142">Text constant: "-"</span></span>
5.  <span data-ttu-id="6a2cd-143">Velikost</span><span class="sxs-lookup"><span data-stu-id="6a2cd-143">Size</span></span>
6.  <span data-ttu-id="6a2cd-144">Textová konstanta: "-"</span><span class="sxs-lookup"><span data-stu-id="6a2cd-144">Text constant: "-"</span></span>
7.  <span data-ttu-id="6a2cd-145">Styl</span><span class="sxs-lookup"><span data-stu-id="6a2cd-145">Style</span></span>

<span data-ttu-id="6a2cd-146">V tomto případě bude číslo varianty produktu pro červené, malé polo tričko: TS1234-Red-Small-Polo.</span><span class="sxs-lookup"><span data-stu-id="6a2cd-146">In this case, the product variant number for a red, small, polo T-shirt will be TS1234-Red-Small-Polo.</span></span>

## <a name="nomenclature-of-constraint-based-configurations"></a><span data-ttu-id="6a2cd-147">Názvosloví konfigurací založených na dimenzích</span><span class="sxs-lookup"><span data-stu-id="6a2cd-147">Nomenclature of constraint-based configurations</span></span>
<span data-ttu-id="6a2cd-148">Pro konfigurace založené na omezeních můžete vytvořit vyhrazené názvosloví pro dimenzi konfiguračního produktu.</span><span class="sxs-lookup"><span data-stu-id="6a2cd-148">For constraint-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="6a2cd-149">Můžete vybrat následující segmenty na stránce **Názvosloví produktu**:</span><span class="sxs-lookup"><span data-stu-id="6a2cd-149">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="6a2cd-150">Hodnota číselné řady</span><span class="sxs-lookup"><span data-stu-id="6a2cd-150">Number sequence value</span></span>
-   <span data-ttu-id="6a2cd-151">Textová konstanta</span><span class="sxs-lookup"><span data-stu-id="6a2cd-151">Text constant</span></span>
-   <span data-ttu-id="6a2cd-152">Hodnota atributu</span><span class="sxs-lookup"><span data-stu-id="6a2cd-152">Attribute value</span></span>

<span data-ttu-id="6a2cd-153">Jednotlivé komponenty v modelu konfigurace produktu můžou mít vlastní názvosloví konfigurace.</span><span class="sxs-lookup"><span data-stu-id="6a2cd-153">Each component in a product configuration model can have its own configuration nomenclature.</span></span> <span data-ttu-id="6a2cd-154">Lze použít pouze atributy, které patří ke komponentě.</span><span class="sxs-lookup"><span data-stu-id="6a2cd-154">Only attributes that belong to the component can be used.</span></span> <span data-ttu-id="6a2cd-155">Nemohou být použity atributy z dílčích komponent nebo požadavky uživatelů.</span><span class="sxs-lookup"><span data-stu-id="6a2cd-155">Attributes from subcomponents or user requirements can't be used.</span></span>

### <a name="example"></a><span data-ttu-id="6a2cd-156">Příklad</span><span class="sxs-lookup"><span data-stu-id="6a2cd-156">Example</span></span>

<span data-ttu-id="6a2cd-157">Model konfigurace produktu má kořenovou komponentu se dvěma atributy:</span><span class="sxs-lookup"><span data-stu-id="6a2cd-157">A product configuration model has a root component that has two attributes:</span></span>

-   <span data-ttu-id="6a2cd-158">Materiál (plast, dřevo, ocel.)</span><span class="sxs-lookup"><span data-stu-id="6a2cd-158">Material (Plastic, Wood, Steel)</span></span>
-   <span data-ttu-id="6a2cd-159">Délka (10... 100)</span><span class="sxs-lookup"><span data-stu-id="6a2cd-159">Length (10...100)</span></span>

<span data-ttu-id="6a2cd-160">Vytvoříte názvosloví konfigurace, které obsahuje následující segmenty:</span><span class="sxs-lookup"><span data-stu-id="6a2cd-160">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="6a2cd-161">Hodnota atributu: materiál</span><span class="sxs-lookup"><span data-stu-id="6a2cd-161">Attribute value: Material</span></span>
2.  <span data-ttu-id="6a2cd-162">Textová konstanta: "AAA"</span><span class="sxs-lookup"><span data-stu-id="6a2cd-162">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="6a2cd-163">Hodnota atributu: délka</span><span class="sxs-lookup"><span data-stu-id="6a2cd-163">Attribute value: Length</span></span>

<span data-ttu-id="6a2cd-164">V takovém případě bude ID konfigurace dřevěného materiálu, který má délku 78, WoodAAA78.</span><span class="sxs-lookup"><span data-stu-id="6a2cd-164">In this case, the configuration ID for wood material that has a length of 78 will be WoodAAA78.</span></span>

## <a name="nomenclature-of-dimension-based-configurations"></a><span data-ttu-id="6a2cd-165">Názvosloví konfigurací založených na dimenzích</span><span class="sxs-lookup"><span data-stu-id="6a2cd-165">Nomenclature of dimension-based configurations</span></span>
<span data-ttu-id="6a2cd-166">Pro konfigurace založené na dimenzích můžete vytvořit vyhrazené názvosloví pro dimenzi konfiguračního produktu.</span><span class="sxs-lookup"><span data-stu-id="6a2cd-166">For dimension-based configurations, you can create a dedicated nomenclature for the configuration product dimension.</span></span> <span data-ttu-id="6a2cd-167">Můžete vybrat následující segmenty na stránce **Názvosloví produktu**:</span><span class="sxs-lookup"><span data-stu-id="6a2cd-167">You can select the following segments on the **Product nomenclature** page:</span></span>

-   <span data-ttu-id="6a2cd-168">Hodnota číselné řady</span><span class="sxs-lookup"><span data-stu-id="6a2cd-168">Number sequence value</span></span>
-   <span data-ttu-id="6a2cd-169">Textová konstanta</span><span class="sxs-lookup"><span data-stu-id="6a2cd-169">Text constant</span></span>
-   <span data-ttu-id="6a2cd-170">Položka konfigurační skupiny</span><span class="sxs-lookup"><span data-stu-id="6a2cd-170">Configuration group item</span></span>

<span data-ttu-id="6a2cd-171">Můžete definovat názvosloví konfigurace pro kusovníky (BOM).</span><span class="sxs-lookup"><span data-stu-id="6a2cd-171">You can define a configuration nomenclature for a bill of materials (BOM).</span></span>

### <a name="example"></a><span data-ttu-id="6a2cd-172">Příklad</span><span class="sxs-lookup"><span data-stu-id="6a2cd-172">Example</span></span>

<span data-ttu-id="6a2cd-173">Kusovník má čtyři řádky kusovníku, které jsou rozděleny do dvou konfiguračních skupin:</span><span class="sxs-lookup"><span data-stu-id="6a2cd-173">A BOM has four BOM lines that are divided into two configuration groups:</span></span>

-   <span data-ttu-id="6a2cd-174">Řádek kusovníku: M0007, standardní skříň</span><span class="sxs-lookup"><span data-stu-id="6a2cd-174">BOM line: M0007, Standard cabinet</span></span>
    -   <span data-ttu-id="6a2cd-175">Skupina konfigurace: Skříň</span><span class="sxs-lookup"><span data-stu-id="6a2cd-175">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="6a2cd-176">Řádek kusovníku: M0008, vysoká koncová skříň</span><span class="sxs-lookup"><span data-stu-id="6a2cd-176">BOM line: M0008, High end cabinet</span></span>
    -   <span data-ttu-id="6a2cd-177">Skupina konfigurace: Skříň</span><span class="sxs-lookup"><span data-stu-id="6a2cd-177">Configuration group: Cabinet</span></span>
-   <span data-ttu-id="6a2cd-178">Řádek kusovníku: M0021, přední potah mřížky</span><span class="sxs-lookup"><span data-stu-id="6a2cd-178">BOM line: M0021, Front grill cloth</span></span>
    -   <span data-ttu-id="6a2cd-179">Skupina konfigurace: Přední mřížka</span><span class="sxs-lookup"><span data-stu-id="6a2cd-179">Configuration group: Front grill</span></span>
-   <span data-ttu-id="6a2cd-180">Řádek kusovníku: M0022, přední kovová mřížka</span><span class="sxs-lookup"><span data-stu-id="6a2cd-180">BOM line: M0022, Front grill metal</span></span>
    -   <span data-ttu-id="6a2cd-181">Skupina konfigurace: Přední mřížka</span><span class="sxs-lookup"><span data-stu-id="6a2cd-181">Configuration group: Front grill</span></span>

<span data-ttu-id="6a2cd-182">Vytvoříte názvosloví konfigurace, které obsahuje následující segmenty:</span><span class="sxs-lookup"><span data-stu-id="6a2cd-182">You create a configuration nomenclature that has the following segments:</span></span>

1.  <span data-ttu-id="6a2cd-183">Skupina konfigurace: Skříň</span><span class="sxs-lookup"><span data-stu-id="6a2cd-183">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="6a2cd-184">Textová konstanta: "&"</span><span class="sxs-lookup"><span data-stu-id="6a2cd-184">Text constant: "&"</span></span>
3.  <span data-ttu-id="6a2cd-185">Skupina konfigurace: Přední mřížka</span><span class="sxs-lookup"><span data-stu-id="6a2cd-185">Configuration group: Front grill</span></span>

<span data-ttu-id="6a2cd-186">V tomto případě bude ID konfigurace standardní skříně s přední látkovou mřížkou M0007&M0021.</span><span class="sxs-lookup"><span data-stu-id="6a2cd-186">In this case, the configuration ID for a standard cabinet that has a cloth front grill will be M0007&M0021.</span></span>

## <a name="nomenclature-for-a-combination-of-product-variants-and-configurations"></a><span data-ttu-id="6a2cd-187">Názvosloví kombinace variant a konfigurací produktu</span><span class="sxs-lookup"><span data-stu-id="6a2cd-187">Nomenclature for a combination of product variants and configurations</span></span>
<span data-ttu-id="6a2cd-188">Při použití technologie konfigurace založené na omezeních nebo na dimenzích ke konfiguraci variant produktu pro základní produkt mohou čísla variant produktu zahrnovat čísla variant produktu z konfigurační dimenze.</span><span class="sxs-lookup"><span data-stu-id="6a2cd-188">When you use either the constraint-based configuration technology or the dimension-based configuration technology to configure product variants for a product master, the product variant numbers of the product variants can include the nomenclature from the configuration dimension.</span></span> <span data-ttu-id="6a2cd-189">Chcete-li nakonfigurovat varianty, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="6a2cd-189">Follow these steps to configure variants.</span></span>

1.  <span data-ttu-id="6a2cd-190">Na stránce **Názvosloví produktu** definujte názvosloví čísel variant produktů, které zahrnuje konfigurační dimenzi.</span><span class="sxs-lookup"><span data-stu-id="6a2cd-190">On the **Product nomenclature** page, define a product variant number nomenclature that includes the configuration dimension.</span></span>
2.  <span data-ttu-id="6a2cd-191">Toto názvosloví přiřaďte skupině dimenze produktu s dimenzí konfigurace.</span><span class="sxs-lookup"><span data-stu-id="6a2cd-191">Assign the nomenclature to a product dimension group that has the configuration dimension.</span></span>
3.  <span data-ttu-id="6a2cd-192">Definujte názvosloví konfigurace pro komponenty nebo kusovníky, které budou použity ke konfiguraci variant produktu.</span><span class="sxs-lookup"><span data-stu-id="6a2cd-192">Define a configuration nomenclature for the components or BOMs that will be used to configure the product variants.</span></span>

<span data-ttu-id="6a2cd-193">Můžete také vytvořit názvosloví pro názvy variant produktů.</span><span class="sxs-lookup"><span data-stu-id="6a2cd-193">You can also create nomenclatures for the product variant names.</span></span> <span data-ttu-id="6a2cd-194">Názvy variant produktů lze nakonfigurovat tak, aby zahrnovaly ID nebo název konfigurace.</span><span class="sxs-lookup"><span data-stu-id="6a2cd-194">The product variant names can be configured to include the configuration ID or name.</span></span>

### <a name="example-for-constraint-based-configurations"></a><span data-ttu-id="6a2cd-195">Příklad konfigurací založených na omezeních</span><span class="sxs-lookup"><span data-stu-id="6a2cd-195">Example for constraint-based configurations</span></span>

<span data-ttu-id="6a2cd-196">V tomto příkladu můžete používat číslo varianty produktu, která se skládá z následujících segmentů:</span><span class="sxs-lookup"><span data-stu-id="6a2cd-196">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="6a2cd-197">Číslo základního produktu</span><span class="sxs-lookup"><span data-stu-id="6a2cd-197">Product master number</span></span>
2.  <span data-ttu-id="6a2cd-198">Textová konstanta "\_"</span><span class="sxs-lookup"><span data-stu-id="6a2cd-198">Text constant "\_"</span></span>
3.  <span data-ttu-id="6a2cd-199">Konfigurace</span><span class="sxs-lookup"><span data-stu-id="6a2cd-199">Configuration</span></span>

<span data-ttu-id="6a2cd-200">Názvosloví konfigurace sestává z následujících segmentů:</span><span class="sxs-lookup"><span data-stu-id="6a2cd-200">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="6a2cd-201">Hodnota atributu: materiál</span><span class="sxs-lookup"><span data-stu-id="6a2cd-201">Attribute value: Material</span></span>
2.  <span data-ttu-id="6a2cd-202">Textová konstanta: "AAA"</span><span class="sxs-lookup"><span data-stu-id="6a2cd-202">Text constant: "AAA"</span></span>
3.  <span data-ttu-id="6a2cd-203">Hodnota atributu: délka</span><span class="sxs-lookup"><span data-stu-id="6a2cd-203">Attribute value: Length</span></span>

<span data-ttu-id="6a2cd-204">Pro segmenty můžete zadat následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="6a2cd-204">You enter the following values for segments:</span></span>

-   <span data-ttu-id="6a2cd-205">Číslo základního produktu = **M0099**</span><span class="sxs-lookup"><span data-stu-id="6a2cd-205">Product master number = **M0099**</span></span>
-   <span data-ttu-id="6a2cd-206">Materiál = **plast**</span><span class="sxs-lookup"><span data-stu-id="6a2cd-206">Material = **Plastic**</span></span>
-   <span data-ttu-id="6a2cd-207">Délka = **12**</span><span class="sxs-lookup"><span data-stu-id="6a2cd-207">Length = **12**</span></span>

<span data-ttu-id="6a2cd-208">V tomto případě bude číslo varianty produktu M0099\_PlasticAAA12.</span><span class="sxs-lookup"><span data-stu-id="6a2cd-208">In this case, the product variant number will be M0099\_PlasticAAA12.</span></span>

### <a name="example-for-dimension-based-configurations"></a><span data-ttu-id="6a2cd-209">Příklad konfigurací založených na dimenzích</span><span class="sxs-lookup"><span data-stu-id="6a2cd-209">Example for dimension-based configurations</span></span>

<span data-ttu-id="6a2cd-210">V tomto příkladu můžete používat číslo varianty produktu, která se skládá z následujících segmentů:</span><span class="sxs-lookup"><span data-stu-id="6a2cd-210">For this example, you use a product variant number nomenclature that consists of the following segments:</span></span>

1.  <span data-ttu-id="6a2cd-211">Číslo základního produktu</span><span class="sxs-lookup"><span data-stu-id="6a2cd-211">Product master number</span></span>
2.  <span data-ttu-id="6a2cd-212">Textová konstanta: "//"</span><span class="sxs-lookup"><span data-stu-id="6a2cd-212">Text constant "//"</span></span>
3.  <span data-ttu-id="6a2cd-213">Konfigurace</span><span class="sxs-lookup"><span data-stu-id="6a2cd-213">Configuration</span></span>

<span data-ttu-id="6a2cd-214">Názvosloví konfigurace sestává z následujících segmentů:</span><span class="sxs-lookup"><span data-stu-id="6a2cd-214">The configuration nomenclature consists of the following segments:</span></span>

1.  <span data-ttu-id="6a2cd-215">Skupina konfigurace: Skříň</span><span class="sxs-lookup"><span data-stu-id="6a2cd-215">Configuration group: Cabinet</span></span>
2.  <span data-ttu-id="6a2cd-216">Textová konstanta: "&"</span><span class="sxs-lookup"><span data-stu-id="6a2cd-216">Text constant: "&"</span></span>
3.  <span data-ttu-id="6a2cd-217">Skupina konfigurace: Přední mřížka</span><span class="sxs-lookup"><span data-stu-id="6a2cd-217">Configuration group: Front grill</span></span>

<span data-ttu-id="6a2cd-218">Pro segmenty můžete zadat následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="6a2cd-218">You enter the following values for segments:</span></span>

-   <span data-ttu-id="6a2cd-219">Číslo základního produktu = **D0123**</span><span class="sxs-lookup"><span data-stu-id="6a2cd-219">Product master number = **D0123**</span></span>
-   <span data-ttu-id="6a2cd-220">Skříň = **M0008**</span><span class="sxs-lookup"><span data-stu-id="6a2cd-220">Cabinet = **M0008**</span></span>
-   <span data-ttu-id="6a2cd-221">Přední mřížka = **M0022**</span><span class="sxs-lookup"><span data-stu-id="6a2cd-221">Front grill = **M0022**</span></span>

<span data-ttu-id="6a2cd-222">V tomto případě bude číslo varianty produktu D0123//M0008&M0022.</span><span class="sxs-lookup"><span data-stu-id="6a2cd-222">In this case, the product variant number will be D0123//M0008&M0022.</span></span>

## <a name="numbering-conflicts"></a><span data-ttu-id="6a2cd-223">Číslování konfliktů</span><span class="sxs-lookup"><span data-stu-id="6a2cd-223">Numbering conflicts</span></span>
<span data-ttu-id="6a2cd-224">V některých případech nemusí názvosloví čísel variant produktů, které nastavíte, vytvářet čísla variant jedinečných produktů.</span><span class="sxs-lookup"><span data-stu-id="6a2cd-224">In some cases, a product variant number nomenclature that you set up might not produce unique product variant numbers.</span></span> <span data-ttu-id="6a2cd-225">Čísla nebudou jedinečná například, když jedna aktivní dimenze produktu není součástí názvosloví pro základní produkt využívající technologii konfigurace předem definované varianty.</span><span class="sxs-lookup"><span data-stu-id="6a2cd-225">For example, the product variant numbers won't be unique if one active product dimension isn't included in the nomenclature for a product master that uses the predefined variant configuration technology.</span></span> <span data-ttu-id="6a2cd-226">Způsob, kterým budete řešit konflikty je různý, podle technologie konfigurace.</span><span class="sxs-lookup"><span data-stu-id="6a2cd-226">The way that you handle conflicts varies, depending on the configuration technology.</span></span>

### <a name="predefined-variants"></a><span data-ttu-id="6a2cd-227">Předem definované varianty</span><span class="sxs-lookup"><span data-stu-id="6a2cd-227">Predefined variants</span></span>

<span data-ttu-id="6a2cd-228">Pokud se pokusíte automaticky nebo ručně vytvořit varianty produktu, kde jeden nebo více končí stejným číslem varianty produktu, dojde k chybě.</span><span class="sxs-lookup"><span data-stu-id="6a2cd-228">An error occurs if you try to manually create or automatically generate product variants, and more than one product variant ends up with the same product variant number.</span></span> <span data-ttu-id="6a2cd-229">Této situaci se lze vyhnout tak, že budete ve skupině dimenzí produktu používat všechny aktivní dimenze produktu.</span><span class="sxs-lookup"><span data-stu-id="6a2cd-229">To avoid this scenario, you should use all active product dimensions in the product dimension group.</span></span> <span data-ttu-id="6a2cd-230">Alternativně zahrňte číselnou řadu, což vám pomůže zaručit jedinečnost čísel variat produktu.</span><span class="sxs-lookup"><span data-stu-id="6a2cd-230">Alternatively, include a number sequence to help guarantee that the product variant numbers are unique.</span></span>

### <a name="constraint-based-configurations"></a><span data-ttu-id="6a2cd-231">Konfigurace založené na omezeních</span><span class="sxs-lookup"><span data-stu-id="6a2cd-231">Constraint-based configurations</span></span>

<span data-ttu-id="6a2cd-232">V závislosti na názvosloví se systém může pokusit přiřadit nejedinečné číslo varianty produktu ke konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="6a2cd-232">Depending on the nomenclature, the system might try to assign a non-unique product variant number to a configuration.</span></span> <span data-ttu-id="6a2cd-233">V takovém případě systém používá číselnou řadu pro konfigurační dimenzi jako číslo varianty produktu. V takovém případě bude zobrazena varovná zpráva.</span><span class="sxs-lookup"><span data-stu-id="6a2cd-233">In this case, the system uses the number sequence for the configuration dimension as the product variant number instead, and you receive a warning.</span></span> <span data-ttu-id="6a2cd-234">Této situaci se lze vyhnout tak, že do názvosloví zahrnete dostatek produktů, které pomohou zaručit jedinečná čísla variant produktu.</span><span class="sxs-lookup"><span data-stu-id="6a2cd-234">To avoid this scenario, you should include enough attributes in the nomenclature to help guarantee unique product variant numbers.</span></span> <span data-ttu-id="6a2cd-235">Měli byste také zajistit, že je pro komponentu zapnutá možnost **Opakované použití**.</span><span class="sxs-lookup"><span data-stu-id="6a2cd-235">You should also make sure that the **Reuse** option is turned on for the component.</span></span>

### <a name="dimension-based-configurations"></a><span data-ttu-id="6a2cd-236">Konfigurace založené na dimenzích</span><span class="sxs-lookup"><span data-stu-id="6a2cd-236">Dimension-based configurations</span></span>

<span data-ttu-id="6a2cd-237">Během jednoho kroku procesu konfigurace systém navrhne hodnotu konfigurace podle klasifikace.</span><span class="sxs-lookup"><span data-stu-id="6a2cd-237">During one step of the configuration process, the system suggests a configuration value according to the nomenclature.</span></span> <span data-ttu-id="6a2cd-238">V tomto kroku můžete ručně změnit hodnotu konfigurace.</span><span class="sxs-lookup"><span data-stu-id="6a2cd-238">In this step, you can manually change the configuration value.</span></span> <span data-ttu-id="6a2cd-239">Po uložení konfigurace systém zkontroluje, zda je hodnota konfigurace jedinečná.</span><span class="sxs-lookup"><span data-stu-id="6a2cd-239">When you save the configuration, the system verifies that the configuration value is unique.</span></span> <span data-ttu-id="6a2cd-240">Není-li hodnota, kterou jste zadali jedinečná, zobrazí se chybová zpráva.</span><span class="sxs-lookup"><span data-stu-id="6a2cd-240">If the value that you entered isn't unique, you receive an error message.</span></span> <span data-ttu-id="6a2cd-241">Chcete-li uložit konfiguraci, musíte zadat jedinečnou hodnotu konfigurace.</span><span class="sxs-lookup"><span data-stu-id="6a2cd-241">To save the configuration, you must enter a unique configuration value.</span></span>

<a name="additional-resources"></a><span data-ttu-id="6a2cd-242">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="6a2cd-242">Additional resources</span></span>
--------

[<span data-ttu-id="6a2cd-243">Vytvoření názvosloví čísel produktů pro předdefinované varianty produktu</span><span class="sxs-lookup"><span data-stu-id="6a2cd-243">Create a product number nomenclature for predefined product variants</span></span>](tasks/create-product-number-nomenclature-predefined-variants-2016-11.md)

[<span data-ttu-id="6a2cd-244">Vytvoření názvosloví čísel produktů pro nakonfigurované varianty produktu</span><span class="sxs-lookup"><span data-stu-id="6a2cd-244">Create a product number nomenclature for configured product variants</span></span>](tasks/create-product-number-nomenclature-product-variants_2016_11.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]