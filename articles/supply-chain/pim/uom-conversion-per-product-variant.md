---
title: Převod měrné jednotky pro variantu produktu
description: Toto téma popisuje nastavení způsobu převodu měrné jednotky u variant produktu.
author: johanhoffmann
manager: AnnBe
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: UnitOfMeasureConversion
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: c8181f0bda9b781a6c2b0feb0aba1beb51bfea65
ms.sourcegitcommit: af36eb17b36092a3101bbfc96486b25036676558
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/06/2020
ms.locfileid: "2935092"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a><span data-ttu-id="b62ce-103">Převod měrné jednotky pro variantu produktu</span><span class="sxs-lookup"><span data-stu-id="b62ce-103">Unit of measure conversion per product variant</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b62ce-104">Toto téma popisuje nastavení způsobu převodu měrné jednotky u variant produktu.</span><span class="sxs-lookup"><span data-stu-id="b62ce-104">This topic explains how unit of measure conversions can be set up on product variants.</span></span> <span data-ttu-id="b62ce-105">Zahrnuje také příklad nastavení.</span><span class="sxs-lookup"><span data-stu-id="b62ce-105">It includes an example of the setup.</span></span>

<span data-ttu-id="b62ce-106">Tato funkce umožňuje společnostem definovat jiný převod jednotek mezi variantami stejného produktu.</span><span class="sxs-lookup"><span data-stu-id="b62ce-106">This feature makes it possible for companies to define different unit conversion between the variants of the same product.</span></span> <span data-ttu-id="b62ce-107">Následující příklad je použit v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="b62ce-107">The following example is used in this topic.</span></span> <span data-ttu-id="b62ce-108">Společnost prodává trička ve velikostech S, M, L a XL.</span><span class="sxs-lookup"><span data-stu-id="b62ce-108">A company sells T-shirts in sizes Small, Medium, Large, and Extra-Large.</span></span> <span data-ttu-id="b62ce-109">Tričko je definováno jako produkt a jsou definovány různé velikosti variant produktu.</span><span class="sxs-lookup"><span data-stu-id="b62ce-109">The T-shirt is defined as a product, and the different sizes are defined as variants of the product.</span></span> <span data-ttu-id="b62ce-110">Trička jsou zabalena v krabicích. Do krabice se vejde pět triček. V případě velikosti XL se však trička vlezou jen čtyři.</span><span class="sxs-lookup"><span data-stu-id="b62ce-110">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-Large size where there is only space for four T-shirts.</span></span> <span data-ttu-id="b62ce-111">Společnost chce sledovat různé varianty triček po **kusech**, nicméně trička prodává po **krabicích**.</span><span class="sxs-lookup"><span data-stu-id="b62ce-111">The company wants to track the different variants of the T-shirts in the unit **Pieces** but is selling the T-shirts in the unit **Boxes**.</span></span> <span data-ttu-id="b62ce-112">Převod mezi jednotkou zásob a prodejní jednotkou je 1 krabice = 5 kusů s výjimkou varianty XL, kde 1 krabice = 4 kusy.</span><span class="sxs-lookup"><span data-stu-id="b62ce-112">The conversion between the inventory unit and the sales unit is 1 Box = 5 Pieces, except for the variant Extra-Large, where the conversion is 1 Box = 4 Pieces.</span></span>

### <a name="set-up-a-product-for-unit-conversion-per-variant"></a><span data-ttu-id="b62ce-113">Nastavení produktu pro převod jednotek pro variantu</span><span class="sxs-lookup"><span data-stu-id="b62ce-113">Set up a product for unit conversion per variant</span></span>

<span data-ttu-id="b62ce-114">Varianty produktu lze vytvořit pouze pro produkty **podtyp produktu**: **základní produkt**.</span><span class="sxs-lookup"><span data-stu-id="b62ce-114">Product variants can only be created for products of **Product subtype**: **Product master**.</span></span> <span data-ttu-id="b62ce-115">Další informace naleznete v tématu [Vytvoření základního produktu](tasks/create-product-master.md).</span><span class="sxs-lookup"><span data-stu-id="b62ce-115">For more information, see [Create a product master](tasks/create-product-master.md).</span></span>

<span data-ttu-id="b62ce-116">Tato funkce není povolena pro produkty, které jsou nastaveny pro procesy skutečné hmotnosti.</span><span class="sxs-lookup"><span data-stu-id="b62ce-116">The feature is not enabled for products that are set up for Catch Weight processes.</span></span> 

<span data-ttu-id="b62ce-117">Po vytvoření základního produktu s variantami produktu lze nastavit převody jednotek pro varianty.</span><span class="sxs-lookup"><span data-stu-id="b62ce-117">When the product master with released products variants is created, unit conversions per variants can be set up.</span></span> <span data-ttu-id="b62ce-118">Položku nabídky pro otevření stránky s převody naleznete v kontextu produktu nebo variantě produktu na následujících stránkách.</span><span class="sxs-lookup"><span data-stu-id="b62ce-118">You can find the menu item for opening the unit conversion page in context of a product or a product variant on the following pages.</span></span>

-   <span data-ttu-id="b62ce-119">Strnka **Podrobnosti o produktu**</span><span class="sxs-lookup"><span data-stu-id="b62ce-119">**Product details** page</span></span>
-   <span data-ttu-id="b62ce-120">Strána **Zveřejněné informace o produktu**</span><span class="sxs-lookup"><span data-stu-id="b62ce-120">**Released products details** page</span></span>
-   <span data-ttu-id="b62ce-121">Stránka **zveřejněné varianty produktu**</span><span class="sxs-lookup"><span data-stu-id="b62ce-121">**Released product variants** page</span></span>

<span data-ttu-id="b62ce-122">Otevřete-li stránku **Převod jednotek** v kontextu základního produktu nebo zveřejněné varianty produktu, můžete vybrat, jestli chcete nastavit převod jednotky pro produkt nebo variantu produktu.</span><span class="sxs-lookup"><span data-stu-id="b62ce-122">When you open the **Unit conversion** page in context of a product master or released product variant, you can select if you want to set up the unit conversion for the product or for a product variant.</span></span> <span data-ttu-id="b62ce-123">To lze provést výběrem buď **varianty produktu**, nebo **produktu** v poli **Tvorba převodu pro**.</span><span class="sxs-lookup"><span data-stu-id="b62ce-123">You do that by selecting either **Product variant** or **Product** in the **Create conversion for** field.</span></span>

### <a name="product-variant"></a><span data-ttu-id="b62ce-124">Varianta produktu</span><span class="sxs-lookup"><span data-stu-id="b62ce-124">Product variant</span></span>

<span data-ttu-id="b62ce-125">Vyberete-li **Varianta produktu**, můžete si vybrat, pro kterou variantu si přejete nastavit převod jednotek v poli **varianta produktu**.</span><span class="sxs-lookup"><span data-stu-id="b62ce-125">If you select **Product variant,** then you can select for which variant you want to set up the unit conversion in the **Product variant** field.</span></span>

### <a name="product"></a><span data-ttu-id="b62ce-126">Produkt</span><span class="sxs-lookup"><span data-stu-id="b62ce-126">Product</span></span>

<span data-ttu-id="b62ce-127">Vyberete-li **Produkt**, potom můžete nastavit převod jednotky pro základní produkt.</span><span class="sxs-lookup"><span data-stu-id="b62ce-127">If you select **Product**, then you can set up a unit conversion for the product master.</span></span> <span data-ttu-id="b62ce-128">Tento převod jednotek bude použit pro všechny varianty produktu bez definovaného převodu jednotek.</span><span class="sxs-lookup"><span data-stu-id="b62ce-128">This unit conversion will apply for all product variants with no defined unit conversion.</span></span>

### <a name="example"></a><span data-ttu-id="b62ce-129">Příklad</span><span class="sxs-lookup"><span data-stu-id="b62ce-129">Example</span></span>

<span data-ttu-id="b62ce-130">Základní produkt, **tričko**, má čtyři varianty: S, M, L a XL.</span><span class="sxs-lookup"><span data-stu-id="b62ce-130">A product master, **T-Shirt**, has four released products variants Small, Medium, Large, and X-Large.</span></span> <span data-ttu-id="b62ce-131">Trička jsou zabalena v krabicích. Do krabice se vejde pět triček. V případě velikosti XL se však trička vlezou jen čtyři.</span><span class="sxs-lookup"><span data-stu-id="b62ce-131">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-large size where there is only space for four T-shirts.</span></span>

<span data-ttu-id="b62ce-132">Nejprve otevřete stránku **Převod jednotek** ze stránky podrobnosti o zveřejnění produktu pro **tričko.**</span><span class="sxs-lookup"><span data-stu-id="b62ce-132">First, open the **Unit conversion** page from the Release product details page for **T-shirt.**</span></span>

<span data-ttu-id="b62ce-133">Na stránce **Převod jednotek** nastavte převod jednotky pro variantu produktu XL.</span><span class="sxs-lookup"><span data-stu-id="b62ce-133">On the **Unit conversion** page, set up the unit conversion for the release product variant X-Large.</span></span>

| <span data-ttu-id="b62ce-134">**Pole**</span><span class="sxs-lookup"><span data-stu-id="b62ce-134">**Field**</span></span>             | <span data-ttu-id="b62ce-135">**Nastavení**</span><span class="sxs-lookup"><span data-stu-id="b62ce-135">**Setting**</span></span>             |
|-----------------------|-------------------------|
| <span data-ttu-id="b62ce-136">Vytvoření převodu pro</span><span class="sxs-lookup"><span data-stu-id="b62ce-136">Create conversion for</span></span> | <span data-ttu-id="b62ce-137">Varianta produktu</span><span class="sxs-lookup"><span data-stu-id="b62ce-137">Product variant</span></span>         |
| <span data-ttu-id="b62ce-138">Varianta produktu</span><span class="sxs-lookup"><span data-stu-id="b62ce-138">Product variant</span></span>       | <span data-ttu-id="b62ce-139">Tričko : : XL : :</span><span class="sxs-lookup"><span data-stu-id="b62ce-139">T-Shirt : : X-Large : :</span></span> |
| <span data-ttu-id="b62ce-140">Z jednotky</span><span class="sxs-lookup"><span data-stu-id="b62ce-140">From unit</span></span>             | <span data-ttu-id="b62ce-141">Krabice</span><span class="sxs-lookup"><span data-stu-id="b62ce-141">Boxes</span></span>                   |
| <span data-ttu-id="b62ce-142">Koeficient</span><span class="sxs-lookup"><span data-stu-id="b62ce-142">Factor</span></span>                | <span data-ttu-id="b62ce-143">4</span><span class="sxs-lookup"><span data-stu-id="b62ce-143">4</span></span>                       |
| <span data-ttu-id="b62ce-144">Do jednotky</span><span class="sxs-lookup"><span data-stu-id="b62ce-144">To Unit</span></span>               | <span data-ttu-id="b62ce-145">Kusy</span><span class="sxs-lookup"><span data-stu-id="b62ce-145">Pieces</span></span>                  |

<span data-ttu-id="b62ce-146">Varianty zveřejněného produktu S, M a L mají stejný převod jednotek mezi jednotkou krabice a kusů, což znamená, že můžete definovat převod jednotky pro tyto varianty produktu pro základní produkt.</span><span class="sxs-lookup"><span data-stu-id="b62ce-146">The Released product variants Small, Medium, and Large have the same unit conversion between the unit Box and Pieces, which means that you can define the unit conversion for these product variants on the product master.</span></span>

| <span data-ttu-id="b62ce-147">**Pole**</span><span class="sxs-lookup"><span data-stu-id="b62ce-147">**Field**</span></span>             | <span data-ttu-id="b62ce-148">**Nastavení**</span><span class="sxs-lookup"><span data-stu-id="b62ce-148">**Setting**</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="b62ce-149">Vytvoření převodu pro</span><span class="sxs-lookup"><span data-stu-id="b62ce-149">Create conversion for</span></span> | <span data-ttu-id="b62ce-150">Produkt</span><span class="sxs-lookup"><span data-stu-id="b62ce-150">Product</span></span>     |
| <span data-ttu-id="b62ce-151">Produkt</span><span class="sxs-lookup"><span data-stu-id="b62ce-151">Product</span></span>               | <span data-ttu-id="b62ce-152">Tričko</span><span class="sxs-lookup"><span data-stu-id="b62ce-152">T-Shirt</span></span>     |
| <span data-ttu-id="b62ce-153">Z jednotky</span><span class="sxs-lookup"><span data-stu-id="b62ce-153">From unit</span></span>             | <span data-ttu-id="b62ce-154">Krabice</span><span class="sxs-lookup"><span data-stu-id="b62ce-154">Boxes</span></span>       |
| <span data-ttu-id="b62ce-155">Koeficient</span><span class="sxs-lookup"><span data-stu-id="b62ce-155">Factor</span></span>                | <span data-ttu-id="b62ce-156">5</span><span class="sxs-lookup"><span data-stu-id="b62ce-156">5</span></span>           |
| <span data-ttu-id="b62ce-157">Do jednotky</span><span class="sxs-lookup"><span data-stu-id="b62ce-157">To Unit</span></span>               | <span data-ttu-id="b62ce-158">Kusy</span><span class="sxs-lookup"><span data-stu-id="b62ce-158">Pieces</span></span>      |

### <a name="using-excel-to-update-the-unit-conversions"></a><span data-ttu-id="b62ce-159">Použití aplikace Excel pro aktualizaci převodů jednotek</span><span class="sxs-lookup"><span data-stu-id="b62ce-159">Using Excel to update the unit conversions</span></span>

<span data-ttu-id="b62ce-160">Pokud má produkt mnoho variant s různými převody jednotek, je vhodné exportovat převody jednotek ze stránky **Převod jednotek** do tabulky aplikace Excel, aktualizovat převody a publikovat je zpět v aplikaci Supply Chain Mangement.</span><span class="sxs-lookup"><span data-stu-id="b62ce-160">If a product has many product variants with different unit conversions, it's a good idea to export the unit conversions from the **Unit conversion** page to an Excel spreadsheet, update the conversions, and then publish them back to Supply Chain Mangement.</span></span>

<span data-ttu-id="b62ce-161">Možnost exportovat do aplikace Excel a publikovat úpravy zpět do aplikace Supply Chain Mangement je povolena z nabídky **Otevřít v aplikaci Microsoft office** v podokně Akce na stránce **Převod jednotek**.</span><span class="sxs-lookup"><span data-stu-id="b62ce-161">The option to export to Excel and publish the edits back to Supply Chain Mangement is enabled from the **Open in Microsoft office** menu item on the Action Pane on the **Unit conversion** page.</span></span>
