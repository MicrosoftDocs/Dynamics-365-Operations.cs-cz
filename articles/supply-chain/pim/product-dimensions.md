---
title: Dimenze produktu
description: "Existují čtyři dimenze produktu – barva, konfigurace, velikost a styl. Kombinujte dimenze produktu ve skupinách dimenzí a přiřazujte skupiny dimenzí k základním produktům. Kombinace dimenzí produktu určuje způsob definování variant produktu."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDimension, EcoResProductDimensionGroup, EcoResProductMasterDimension, RetailEcoResColor, RetailEcoResSize, RetailEcoResStyle
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 68f4bfcf62b5e7c65cbe361b510c2769b0e9bebb
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="product-dimensions"></a><span data-ttu-id="67b91-105">Dimenze produktu</span><span class="sxs-lookup"><span data-stu-id="67b91-105">Product dimensions</span></span>

[!include[banner](../includes/banner.md)]

[!include[Retail name](../includes/retail-name.md)]


<span data-ttu-id="67b91-106">Existují čtyři dimenze produktu – barva, konfigurace, velikost a styl.</span><span class="sxs-lookup"><span data-stu-id="67b91-106">There are four product dimensions -  Color, Configuration, Size and Style.</span></span> <span data-ttu-id="67b91-107">Kombinujte dimenze produktu ve skupinách dimenzí a přiřazujte skupiny dimenzí k základním produktům.</span><span class="sxs-lookup"><span data-stu-id="67b91-107">You combine product dimensions in dimension groups and assign dimension groups to product masters.</span></span> <span data-ttu-id="67b91-108">Kombinace dimenzí produktu určuje způsob definování variant produktu.</span><span class="sxs-lookup"><span data-stu-id="67b91-108">The combinations of product dimensions determine how product variants are defined.</span></span>

<span data-ttu-id="67b91-109">Dimenze produktu jsou vlastnosti, které slouží k identifikaci varianty produktu.</span><span class="sxs-lookup"><span data-stu-id="67b91-109">Product dimensions are characteristics that serve to identify a product variant.</span></span> <span data-ttu-id="67b91-110">Kombinace dimenzí produktu slouží k definování variant produktu.</span><span class="sxs-lookup"><span data-stu-id="67b91-110">You can use combinations of product dimensions to define product variants.</span></span> <span data-ttu-id="67b91-111">Chcete-li vytvořit variantu produktu, je nutné definovat alespoň jednu dimenzi produktu pro základní produkt.</span><span class="sxs-lookup"><span data-stu-id="67b91-111">You must define at least one product dimension for a product master in order to create a product variant.</span></span>
<span data-ttu-id="67b91-112">Varianty produktu</span><span class="sxs-lookup"><span data-stu-id="67b91-112">Product variants</span></span>
----------------

<span data-ttu-id="67b91-113">Varianty produktu jsou označovány také jako položky.</span><span class="sxs-lookup"><span data-stu-id="67b91-113">Product variants are also referred to as items.</span></span> <span data-ttu-id="67b91-114">Položka je hmotný produkt, který není stejný jako služba.</span><span class="sxs-lookup"><span data-stu-id="67b91-114">An item is a tangible product, which is not the same as a service.</span></span> <span data-ttu-id="67b91-115">Je také možné definovat základní produkt s typem Servis.</span><span class="sxs-lookup"><span data-stu-id="67b91-115">It is also possible to define a product master with the Service type.</span></span> <span data-ttu-id="67b91-116">Pomocí typu Služba můžete specifikovat varianty produktu, které obsahují služby.</span><span class="sxs-lookup"><span data-stu-id="67b91-116">By using the Service type, you can specify product variants that include services.</span></span> <span data-ttu-id="67b91-117">Můžete například určit základní produkt pro konzultační práci a varianty produktu pro práci, kterou zajišťují vyšší konzultanti a nižší konzultanti.</span><span class="sxs-lookup"><span data-stu-id="67b91-117">For example, you can specify a product master for Consultancy work and product variants for work that is performed by senior consultants and junior consultants.</span></span>

## <a name="product-dimensions"></a><span data-ttu-id="67b91-118">Dimenze produktu</span><span class="sxs-lookup"><span data-stu-id="67b91-118">Product dimensions</span></span>
<span data-ttu-id="67b91-119">K dispozici jsou následující dimenze produktu: konfigurace, barva, velikost a styl.</span><span class="sxs-lookup"><span data-stu-id="67b91-119">The following product dimensions are available: Configuration, Color, Size, and Style.</span></span> <span data-ttu-id="67b91-120">Varianty produktu lze generovat na základě hodnot dimenzí produktu.</span><span class="sxs-lookup"><span data-stu-id="67b91-120">A product variant can be generated based on the product dimension values.</span></span>

<span data-ttu-id="67b91-121">Hodnoty dimenze produktu, jako například Velikost, Barva a Styl, lze vytvořit na stránce **Velikost**, **Barva** a **Styl**, které jsou přístupné z následujících umístění: **Řízení informací o produktech** &gt; **Nastavení** &gt; **Dimenze a varianty skupiny** &gt; **Velikosti, barvy nebo styly**.</span><span class="sxs-lookup"><span data-stu-id="67b91-121">Product dimensions values such as Size, Color and Style can be created on the **Size**, **Color** and **Style** pages, which can be accessed from the following locations: **Product information management** &gt; **Setup** &gt; **Dimension and variant Groups** &gt; **Sizes/Colors/Styles**.</span></span> <span data-ttu-id="67b91-122">Hodnoty dimenze produktu pro konfigurační dimenze jsou obvykle tvořeny pomocí konfigurátoru produktu nebo konfigurátoru založeného na dimenzích.</span><span class="sxs-lookup"><span data-stu-id="67b91-122">Product dimension values for the Configuration dimension are typically created using either the Product configurator or the Dimension-based configurator.</span></span> <span data-ttu-id="67b91-123">Dimenze produktu se také vytvářejí a udržují na stránce **Dimenze produktu**, která je přístupná z následujících umístění:</span><span class="sxs-lookup"><span data-stu-id="67b91-123">Product dimensions can also be created and maintained on the **Product dimensions** page, which can be accessed from the following locations:</span></span>
-   <span data-ttu-id="67b91-124">Klikněte na **Řízení informací o produktech** &gt; **Produkty** &gt; **Základní produkty**.</span><span class="sxs-lookup"><span data-stu-id="67b91-124">Click **Product information management** &gt; **Products** &gt; **Product masters**.</span></span> <span data-ttu-id="67b91-125">V **podokně akcí** klikněte na možnost **Dimenze produktu**.</span><span class="sxs-lookup"><span data-stu-id="67b91-125">On the **Action Pane**, click **Product dimensions**.</span></span>
-   <span data-ttu-id="67b91-126">Klikněte na **Řízení informací o produktech** &gt; **Produkty** &gt; **Všechny produkty a základní produkty**.</span><span class="sxs-lookup"><span data-stu-id="67b91-126">Click **Product information management** &gt; **Products** &gt; **All products and product masters**.</span></span> <span data-ttu-id="67b91-127">Vyberte základní produkt.</span><span class="sxs-lookup"><span data-stu-id="67b91-127">Select a product master.</span></span> <span data-ttu-id="67b91-128">V **podokně akcí** klikněte na možnost **Dimenze produktu**.</span><span class="sxs-lookup"><span data-stu-id="67b91-128">On the **Action Pane**, click **Product dimensions**.</span></span>
-   <span data-ttu-id="67b91-129">Klikněte na možnosti **Řízení informací o produktech** &gt; **Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="67b91-129">Click **Product information management** &gt; **Released products**.</span></span> <span data-ttu-id="67b91-130">Vyberte základní produkt.</span><span class="sxs-lookup"><span data-stu-id="67b91-130">Select a product master.</span></span> <span data-ttu-id="67b91-131">V **podokně akcí** klikněte na **Produkt**.</span><span class="sxs-lookup"><span data-stu-id="67b91-131">On the **Action Pane**, click **Product**.</span></span> <span data-ttu-id="67b91-132">Ve skupině **Základní produkt** klikněte na **Dimenze produktu**.</span><span class="sxs-lookup"><span data-stu-id="67b91-132">In the **Product master** group, click **Product dimensions**.</span></span>

<span data-ttu-id="67b91-133">Počet variant, které je možné vytvořit pro položku, je omezen počet možných kombinací dimenzí produktu.</span><span class="sxs-lookup"><span data-stu-id="67b91-133">The number of variants that you can create for an item is limited by the number of possible product dimension combinations.</span></span>
| <span data-ttu-id="67b91-134">**Tip**</span><span class="sxs-lookup"><span data-stu-id="67b91-134">**Tip**</span></span>                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67b91-135">Používáte-li na produkt, například na řádku objednávky, vyberete dimenze produktu pro identifikování varianty produktu, se kterou chcete pracovat.</span><span class="sxs-lookup"><span data-stu-id="67b91-135">When you use a product on, for example, an order line, you select the product dimensions to identify the product variant that you want to work with.</span></span> |

## <a name="example"></a><span data-ttu-id="67b91-136">Příklad</span><span class="sxs-lookup"><span data-stu-id="67b91-136">Example</span></span>
<span data-ttu-id="67b91-137">Společnost prodává džíny.</span><span class="sxs-lookup"><span data-stu-id="67b91-137">A company sells denim jeans.</span></span> <span data-ttu-id="67b91-138">Tato položka, džíny, používá pro dimenzi produktu barvy a velikosti.</span><span class="sxs-lookup"><span data-stu-id="67b91-138">The item, Jeans, uses the Color and Size product dimensions.</span></span> <span data-ttu-id="67b91-139">Džíny se prodávají ve třech různých barvách a šesti různých velikostech.</span><span class="sxs-lookup"><span data-stu-id="67b91-139">The jeans are sold in three different colors and six different sizes.</span></span> <span data-ttu-id="67b91-140">Barvy: Modrá, černá, hnědá Velikosti: XS, S, M, L, XL, XXL Ne všechny velikosti jsou k dispozici ve všech třech barvách.</span><span class="sxs-lookup"><span data-stu-id="67b91-140">Colors: Blue, Black, Brown Sizes: XS, S, M, L, XL, XXL Not all sizes are available in all the three colors.</span></span> <span data-ttu-id="67b91-141">Pokud by byly všechny kombinace dostupné, výsledkem by bylo 18 různých druhů džín.</span><span class="sxs-lookup"><span data-stu-id="67b91-141">If all combinations were available, it would create 18 different types of jeans.</span></span> <span data-ttu-id="67b91-142">V tomto příkladu se vyrábí pouze těchto devět kombinací variant produktu.</span><span class="sxs-lookup"><span data-stu-id="67b91-142">In this example, only the following nine product variant combinations are produced.</span></span>

| <span data-ttu-id="67b91-143">Barva</span><span class="sxs-lookup"><span data-stu-id="67b91-143">Color</span></span> | <span data-ttu-id="67b91-144">Velikost</span><span class="sxs-lookup"><span data-stu-id="67b91-144">Size</span></span> |
|-------|------|
| <span data-ttu-id="67b91-145">Modrá</span><span class="sxs-lookup"><span data-stu-id="67b91-145">Blue</span></span>  | <span data-ttu-id="67b91-146">XS</span><span class="sxs-lookup"><span data-stu-id="67b91-146">XS</span></span>   |
| <span data-ttu-id="67b91-147">Modrá</span><span class="sxs-lookup"><span data-stu-id="67b91-147">Blue</span></span>  | <span data-ttu-id="67b91-148">S</span><span class="sxs-lookup"><span data-stu-id="67b91-148">S</span></span>    |
| <span data-ttu-id="67b91-149">Modrá</span><span class="sxs-lookup"><span data-stu-id="67b91-149">Blue</span></span>  | <span data-ttu-id="67b91-150">S</span><span class="sxs-lookup"><span data-stu-id="67b91-150">M</span></span>    |
| <span data-ttu-id="67b91-151">Černá</span><span class="sxs-lookup"><span data-stu-id="67b91-151">Black</span></span> | <span data-ttu-id="67b91-152">S</span><span class="sxs-lookup"><span data-stu-id="67b91-152">M</span></span>    |
| <span data-ttu-id="67b91-153">Černá</span><span class="sxs-lookup"><span data-stu-id="67b91-153">Black</span></span> | <span data-ttu-id="67b91-154">V</span><span class="sxs-lookup"><span data-stu-id="67b91-154">L</span></span>    |
| <span data-ttu-id="67b91-155">Černá</span><span class="sxs-lookup"><span data-stu-id="67b91-155">Black</span></span> | <span data-ttu-id="67b91-156">XL</span><span class="sxs-lookup"><span data-stu-id="67b91-156">XL</span></span>   |
| <span data-ttu-id="67b91-157">Hnědá</span><span class="sxs-lookup"><span data-stu-id="67b91-157">Brown</span></span> | <span data-ttu-id="67b91-158">V</span><span class="sxs-lookup"><span data-stu-id="67b91-158">L</span></span>    |
| <span data-ttu-id="67b91-159">Hnědá</span><span class="sxs-lookup"><span data-stu-id="67b91-159">Brown</span></span> | <span data-ttu-id="67b91-160">XL</span><span class="sxs-lookup"><span data-stu-id="67b91-160">XL</span></span>   |
| <span data-ttu-id="67b91-161">Hnědá</span><span class="sxs-lookup"><span data-stu-id="67b91-161">Brown</span></span> | <span data-ttu-id="67b91-162">XXL</span><span class="sxs-lookup"><span data-stu-id="67b91-162">XXL</span></span>  |






