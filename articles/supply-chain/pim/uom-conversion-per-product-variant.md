---
title: Převod měrné jednotky pro variantu produktu
description: Toto téma popisuje nastavení způsobu převodu měrné jednotky u variant produktu.
author: johanhoffmann
manager: AnnBe
ms.date: 12/18/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: 36fc98c44625cce03945d76973de67021d53353e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844362"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a><span data-ttu-id="a875a-103">Převod měrné jednotky pro variantu produktu</span><span class="sxs-lookup"><span data-stu-id="a875a-103">Unit of measure conversion per product variant</span></span>

[!include [banner](../includes/banner.md)]

[!include [pivate-preview](../includes/pivate-preview-banner.md)]

<span data-ttu-id="a875a-104">Toto téma popisuje nastavení způsobu převodu měrné jednotky u variant produktu.</span><span class="sxs-lookup"><span data-stu-id="a875a-104">This topic explains how unit of measure conversions can be set up on product variants.</span></span> <span data-ttu-id="a875a-105">Zahrnuje také příklad nastavení.</span><span class="sxs-lookup"><span data-stu-id="a875a-105">It includes an example of the setup.</span></span>

<span data-ttu-id="a875a-106">Tato funkce umožňuje společnostem definovat jiný převod jednotek mezi variantami stejného produktu.</span><span class="sxs-lookup"><span data-stu-id="a875a-106">This feature makes it possible for companies to define different unit conversion between the variants of the same product.</span></span> <span data-ttu-id="a875a-107">Následující příklad je použit v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="a875a-107">The following example is used in this topic.</span></span> <span data-ttu-id="a875a-108">Společnost prodává trička ve velikostech S, M, L a XL.</span><span class="sxs-lookup"><span data-stu-id="a875a-108">A company sells T-shirts in sizes Small, Medium, Large, and Extra-Large.</span></span> <span data-ttu-id="a875a-109">Tričko je definováno jako produkt a jsou definovány různé velikosti variant produktu.</span><span class="sxs-lookup"><span data-stu-id="a875a-109">The T-shirt is defined as a product, and the different sizes are defined as variants of the product.</span></span> <span data-ttu-id="a875a-110">Trička jsou zabalena v krabicích. Do krabice se vejde pět triček. V případě velikosti XL se však trička vlezou jen čtyři.</span><span class="sxs-lookup"><span data-stu-id="a875a-110">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-Large size where there is only space for four T-shirts.</span></span> <span data-ttu-id="a875a-111">Společnost chce sledovat různé varianty triček po **kusech**, nicméně trička prodává po **krabicích**.</span><span class="sxs-lookup"><span data-stu-id="a875a-111">The company wants to track the different variants of the T-shirts in the unit **Pieces** but is selling the T-shirts in the unit **Boxes**.</span></span> <span data-ttu-id="a875a-112">Převod mezi jednotkou zásob a prodejní jednotkou je 1 krabice = 5 kusů s výjimkou varianty XL, kde 1 krabice = 4 kusy.</span><span class="sxs-lookup"><span data-stu-id="a875a-112">The conversion between the inventory unit and the sales unit is 1 Box = 5 Pieces, except for the variant Extra-Large, where the conversion is 1 Box = 4 Pieces.</span></span>

## <a name="setup"></a><span data-ttu-id="a875a-113">Nastavení</span><span class="sxs-lookup"><span data-stu-id="a875a-113">Setup</span></span>

<span data-ttu-id="a875a-114">Můžete konfigurovat parametry pro funkci pro produkty, které jsou povoleny pro **všechny procesy** nebo pouze pro produkt povolen proý **procesy skladu** pomocí funkce **Povolit konverzace měrné jednotky** na stránce **parametry informací o produktu**.</span><span class="sxs-lookup"><span data-stu-id="a875a-114">You can configure the parameters for using the feature for products enabled for **All processes** or only for product enabled for the **Warehouse processes** by using the **Enable unit of measure conversations** option on the **Product information parameters** page.</span></span>

### <a name="set-up-a-product-for-unit-conversion-per-variant"></a><span data-ttu-id="a875a-115">Nastavení produktu pro převod jednotek pro variantu</span><span class="sxs-lookup"><span data-stu-id="a875a-115">Set up a product for unit conversion per variant</span></span>

<span data-ttu-id="a875a-116">Varianty produktu lze vytvořit pouze pro produkty **podtyp produktu**: **základní produkt**.</span><span class="sxs-lookup"><span data-stu-id="a875a-116">Product variants can only be created for products of **Product subtype**: **Product master**.</span></span> <span data-ttu-id="a875a-117">Další informace naleznete v tématu [Vytvoření základního produktu](tasks/create-product-master.md).</span><span class="sxs-lookup"><span data-stu-id="a875a-117">For more information, see [Create a product master](tasks/create-product-master.md).</span></span>

<span data-ttu-id="a875a-118">Tato funkce není povolena pro produkty, které jsou nastaveny pro procesy skutečné hmotnosti.</span><span class="sxs-lookup"><span data-stu-id="a875a-118">The feature is not enabled for products that are set up for Catch Weight processes.</span></span> 

<span data-ttu-id="a875a-119">Při vytváření základního produktu povolte převod měrné jednotky pomocí funkce **Povolit převody měrné jednotky** na stránce**Podrobnosti o produktu**.</span><span class="sxs-lookup"><span data-stu-id="a875a-119">During the creation of a product master enable unit of measure conversion by using the **Enable unit of measure conversions** option on the **Product details** page.</span></span>

<span data-ttu-id="a875a-120">Po vytvoření základního produktu s variantami produktu lze nastavit převody jednotek pro varianty.</span><span class="sxs-lookup"><span data-stu-id="a875a-120">When the product master with released products variants is created, unit conversions per variants can be set up.</span></span> <span data-ttu-id="a875a-121">Položku nabídky pro otevření stránky s převody naleznete v kontextu produktu nebo variantě produktu na následujících stránkách.</span><span class="sxs-lookup"><span data-stu-id="a875a-121">You can find the menu item for opening the unit conversion page in context of a product or a product variant on the following pages.</span></span>

-   <span data-ttu-id="a875a-122">Strnka **Podrobnosti o produktu**</span><span class="sxs-lookup"><span data-stu-id="a875a-122">**Product details** page</span></span>
-   <span data-ttu-id="a875a-123">Strána **Zveřejněné informace o produktu**</span><span class="sxs-lookup"><span data-stu-id="a875a-123">**Released products details** page</span></span>
-   <span data-ttu-id="a875a-124">Stránka **zveřejněné varianty produktu**</span><span class="sxs-lookup"><span data-stu-id="a875a-124">**Released product variants** page</span></span>

<span data-ttu-id="a875a-125">Otevřete-li stránku **Převod jednotek** v kontextu základního produktu nebo zveřejněné varianty produktu, můžete vybrat, jestli chcete nastavit převod jednotky pro produkt nebo variantu produktu.</span><span class="sxs-lookup"><span data-stu-id="a875a-125">When you open the **Unit conversion** page in context of a product master or released product variant, you can select if you want to set up the unit conversion for the product or for a product variant.</span></span> <span data-ttu-id="a875a-126">To lze provést výběrem buď **varianty produktu**, nebo **produktu** v poli **Tvorba převodu pro**.</span><span class="sxs-lookup"><span data-stu-id="a875a-126">You do that by selecting either **Product variant** or **Product** in the **Create conversion for** field.</span></span>

### <a name="product-variant"></a><span data-ttu-id="a875a-127">Varianta produktu</span><span class="sxs-lookup"><span data-stu-id="a875a-127">Product variant</span></span>

<span data-ttu-id="a875a-128">Vyberete-li **Varianta produktu**, můžete si vybrat, pro kterou variantu si přejete nastavit převod jednotek v poli **varianta produktu**.</span><span class="sxs-lookup"><span data-stu-id="a875a-128">If you select **Product variant,** then you can select for which variant you want to set up the unit conversion in the **Product variant** field.</span></span>

### <a name="product"></a><span data-ttu-id="a875a-129">Produkt</span><span class="sxs-lookup"><span data-stu-id="a875a-129">Product</span></span>

<span data-ttu-id="a875a-130">Vyberete-li **Produkt**, potom můžete nastavit převod jednotky pro základní produkt.</span><span class="sxs-lookup"><span data-stu-id="a875a-130">If you select **Product**, then you can set up a unit conversion for the product master.</span></span> <span data-ttu-id="a875a-131">Tento převod jednotek bude použit pro všechny varianty produktu bez definovaného převodu jednotek.</span><span class="sxs-lookup"><span data-stu-id="a875a-131">This unit conversion will apply for all product variants with no defined unit conversion.</span></span>

### <a name="example"></a><span data-ttu-id="a875a-132">Příklad</span><span class="sxs-lookup"><span data-stu-id="a875a-132">Example</span></span>

<span data-ttu-id="a875a-133">Základní produkt, **tričko**, má čtyři varianty: S, M, L a XL.</span><span class="sxs-lookup"><span data-stu-id="a875a-133">A product master, **T-Shirt**, has four released products variants Small, Medium, Large, and X-Large.</span></span> <span data-ttu-id="a875a-134">Trička jsou zabalena v krabicích. Do krabice se vejde pět triček. V případě velikosti XL se však trička vlezou jen čtyři.</span><span class="sxs-lookup"><span data-stu-id="a875a-134">The T-shirts are packed in boxes and there can be five T-shirts in a box, except for the Extra-large size where there is only space for four T-shirts.</span></span>

<span data-ttu-id="a875a-135">Nejprve otevřete stránku **Převod jednotek** ze stránky podrobnosti o zveřejnění produktu pro **tričko.**</span><span class="sxs-lookup"><span data-stu-id="a875a-135">First, open the **Unit conversion** page from the Release product details page for **T-shirt.**</span></span>

<span data-ttu-id="a875a-136">Na stránce **Převod jednotek** nastavte převod jednotky pro variantu produktu XL.</span><span class="sxs-lookup"><span data-stu-id="a875a-136">On the **Unit conversion** page, set up the unit conversion for the release product variant X-Large.</span></span>

| <span data-ttu-id="a875a-137">**Pole**</span><span class="sxs-lookup"><span data-stu-id="a875a-137">**Field**</span></span>             | <span data-ttu-id="a875a-138">**Nastavení**</span><span class="sxs-lookup"><span data-stu-id="a875a-138">**Setting**</span></span>             |
|-----------------------|-------------------------|
| <span data-ttu-id="a875a-139">Vytvoření převodu pro</span><span class="sxs-lookup"><span data-stu-id="a875a-139">Create conversion for</span></span> | <span data-ttu-id="a875a-140">Varianta produktu</span><span class="sxs-lookup"><span data-stu-id="a875a-140">Product variant</span></span>         |
| <span data-ttu-id="a875a-141">Varianta produktu</span><span class="sxs-lookup"><span data-stu-id="a875a-141">Product variant</span></span>       | <span data-ttu-id="a875a-142">Tričko : : XL : :</span><span class="sxs-lookup"><span data-stu-id="a875a-142">T-Shirt : : X-Large : :</span></span> |
| <span data-ttu-id="a875a-143">Z jednotky</span><span class="sxs-lookup"><span data-stu-id="a875a-143">From unit</span></span>             | <span data-ttu-id="a875a-144">Krabice</span><span class="sxs-lookup"><span data-stu-id="a875a-144">Boxes</span></span>                   |
| <span data-ttu-id="a875a-145">Koeficient</span><span class="sxs-lookup"><span data-stu-id="a875a-145">Factor</span></span>                | <span data-ttu-id="a875a-146">4</span><span class="sxs-lookup"><span data-stu-id="a875a-146">4</span></span>                       |
| <span data-ttu-id="a875a-147">Do jednotky</span><span class="sxs-lookup"><span data-stu-id="a875a-147">To Unit</span></span>               | <span data-ttu-id="a875a-148">Kusy</span><span class="sxs-lookup"><span data-stu-id="a875a-148">Pieces</span></span>                  |

<span data-ttu-id="a875a-149">Varianty zveřejněného produktu S, M a L mají stejný převod jednotek mezi jednotkou krabice a kusů, což znamená, že můžete definovat převod jednotky pro tyto varianty produktu pro základní produkt.</span><span class="sxs-lookup"><span data-stu-id="a875a-149">The Released product variants Small, Medium, and Large have the same unit conversion between the unit Box and Pieces, which means that you can define the unit conversion for these product variants on the product master.</span></span>

| <span data-ttu-id="a875a-150">**Pole**</span><span class="sxs-lookup"><span data-stu-id="a875a-150">**Field**</span></span>             | <span data-ttu-id="a875a-151">**Nastavení**</span><span class="sxs-lookup"><span data-stu-id="a875a-151">**Setting**</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="a875a-152">Vytvoření převodu pro</span><span class="sxs-lookup"><span data-stu-id="a875a-152">Create conversion for</span></span> | <span data-ttu-id="a875a-153">Produkt</span><span class="sxs-lookup"><span data-stu-id="a875a-153">Product</span></span>     |
| <span data-ttu-id="a875a-154">Produkt</span><span class="sxs-lookup"><span data-stu-id="a875a-154">Product</span></span>               | <span data-ttu-id="a875a-155">Tričko</span><span class="sxs-lookup"><span data-stu-id="a875a-155">T-Shirt</span></span>     |
| <span data-ttu-id="a875a-156">Z jednotky</span><span class="sxs-lookup"><span data-stu-id="a875a-156">From unit</span></span>             | <span data-ttu-id="a875a-157">Krabice</span><span class="sxs-lookup"><span data-stu-id="a875a-157">Boxes</span></span>       |
| <span data-ttu-id="a875a-158">Koeficient</span><span class="sxs-lookup"><span data-stu-id="a875a-158">Factor</span></span>                | <span data-ttu-id="a875a-159">5</span><span class="sxs-lookup"><span data-stu-id="a875a-159">5</span></span>           |
| <span data-ttu-id="a875a-160">Do jednotky</span><span class="sxs-lookup"><span data-stu-id="a875a-160">To Unit</span></span>               | <span data-ttu-id="a875a-161">Kusy</span><span class="sxs-lookup"><span data-stu-id="a875a-161">Pieces</span></span>      |

### <a name="using-excel-to-update-the-unit-conversions"></a><span data-ttu-id="a875a-162">Použití aplikace Excel pro aktualizaci převodů jednotek</span><span class="sxs-lookup"><span data-stu-id="a875a-162">Using Excel to update the unit conversions</span></span>

<span data-ttu-id="a875a-163">Pokud má produkt mnoho variant s různými převody jednotek, je vhodné exportovat převody jednotek ze stránky **Převod jednotek** do tabulky aplikace Excel, aktualizovat převody a publikovat je zpět v aplikaci Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a875a-163">If a product has many product variants with different unit conversions, it's a good idea to export the unit conversions from the **Unit conversion** page to an Excel spreadsheet, update the conversions, and then publish them back to Finance and Operations.</span></span>

<span data-ttu-id="a875a-164">Možnost exportovat do aplikace Excel a publikovat úpravy zpět do aplikace Finance and Operations je povolena z nabídky **Otevřít v aplikaci Microsoft office** v podokně Akce na stránce **Převod jednotek**.</span><span class="sxs-lookup"><span data-stu-id="a875a-164">The option to export to Excel and publish the edits back to Finance and Operations is enabled from the **Open in Microsoft office** menu item on the Action Pane on the **Unit conversion** page.</span></span>
