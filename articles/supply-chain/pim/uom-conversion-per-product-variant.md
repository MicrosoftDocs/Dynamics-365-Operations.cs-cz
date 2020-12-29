---
title: Převod měrné jednotky pro variantu produktu
description: Toto téma popisuje nastavení způsobu převodu měrné jednotky pro varianty produktu. Zahrnuje také příklad nastavení.
author: johanhoffmann
manager: tfehr
ms.date: 05/11/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: UnitOfMeasureConversion
ROBOTS: noindex, nofollow
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-04-01
ms.dyn365.ops.version: 10
ms.openlocfilehash: 71d35d47a703f0931ba3b4ab5df21c7199c7ea5b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424101"
---
# <a name="unit-of-measure-conversion-per-product-variant"></a><span data-ttu-id="bac4c-104">Převod měrné jednotky pro variantu produktu</span><span class="sxs-lookup"><span data-stu-id="bac4c-104">Unit of measure conversion per product variant</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bac4c-105">Toto téma popisuje nastavení způsobu převodu měrné jednotky pro různé varianty produktu.</span><span class="sxs-lookup"><span data-stu-id="bac4c-105">This topic explains how to set up unit of measure conversions for various product variants.</span></span>

<span data-ttu-id="bac4c-106">Místo vytváření více jednotlivých produktů, které je třeba udržovat, můžete pomocí variant produktu vytvořit variace jednoho produktu.</span><span class="sxs-lookup"><span data-stu-id="bac4c-106">Instead of creating multiple individual products that must be maintained, you can use product variants to create variations of a single product.</span></span> <span data-ttu-id="bac4c-107">Variantou produktu může být Například tričko dané velikosti a barvy.</span><span class="sxs-lookup"><span data-stu-id="bac4c-107">For example, a product variant might be a T-shirt of a given size and color.</span></span>

<span data-ttu-id="bac4c-108">Dříve bylo možné provádět jednotkové převody pouze na základním produktu.</span><span class="sxs-lookup"><span data-stu-id="bac4c-108">Previously, unit conversions could be set up only on the product master.</span></span> <span data-ttu-id="bac4c-109">Proto měly všechny varianty produktu stejná pravidla pro převod jednotek.</span><span class="sxs-lookup"><span data-stu-id="bac4c-109">Therefore, all product variants had the same unit conversion rules.</span></span> <span data-ttu-id="bac4c-110">Nicméně, když je funkce *Převody měrných jednotek pro varianty produktů* zapnutá, pokud se vaše trička prodávají v krabicích a počet triček, které lze zabalit do krabice, závisí na velikosti trička, můžete nyní nastavit jednotkové převody mezi různými velikostmi triček a krabic, do kterých se trička zabalí.</span><span class="sxs-lookup"><span data-stu-id="bac4c-110">However, when the *Unit of measure conversions for product variants* feature is turned on, if your T-shirts are sold in boxes, and the number of T-shirts that can be packed in a box depends on the size of the T-shirts, you can now set up unit conversions between the different shirt sizes and the boxes that are used for packaging.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="bac4c-111">Zapnutí funkce ve vašem systému</span><span class="sxs-lookup"><span data-stu-id="bac4c-111">Turn on the feature in your system</span></span>

<span data-ttu-id="bac4c-112">Pokud tuto funkci ve vašem systému ještě nevidíte, přejděte na [Správu funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) a zapněte funkci *Převody měrných jednotek pro varianty produktů*.</span><span class="sxs-lookup"><span data-stu-id="bac4c-112">If you don't already see this feature in your system, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Unit of measure conversions for product variants* feature.</span></span>

## <a name="set-up-a-product-for-unit-conversion-per-variant"></a><span data-ttu-id="bac4c-113">Nastavení produktu pro převod jednotek pro variantu</span><span class="sxs-lookup"><span data-stu-id="bac4c-113">Set up a product for unit conversion per variant</span></span>

<span data-ttu-id="bac4c-114">Varianty produktu lze vytvořit pouze pro produkty, které jsou základními produkty.</span><span class="sxs-lookup"><span data-stu-id="bac4c-114">Product variants can be created only for products that are product masters.</span></span> <span data-ttu-id="bac4c-115">Další informace naleznete v tématu [Vytvoření základního produktu](tasks/create-product-master.md).</span><span class="sxs-lookup"><span data-stu-id="bac4c-115">For more information, see [Create a product master](tasks/create-product-master.md).</span></span> <span data-ttu-id="bac4c-116">funkce *Převody měrných jednotek pro varianty produktů* není k dispozici pro produkty, které jsou nastaveny pro procesy se skutečnou hmotnosti.</span><span class="sxs-lookup"><span data-stu-id="bac4c-116">The *Unit of measure conversions for product variants* feature isn't available for products that are set up for catch-weight processes.</span></span>

<span data-ttu-id="bac4c-117">Chcete-li nakonfigurovat předlohu produktu tak, aby podporovala převod jednotky pro každou variantu, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="bac4c-117">To configure a product master to support unit conversion per variant, follow these steps.</span></span>

1. <span data-ttu-id="bac4c-118">Přejděte do nabídky **Řízení informací o produktech \> Produkty \> Základní produkty**.</span><span class="sxs-lookup"><span data-stu-id="bac4c-118">Go to **Product information management \> Products \> Product masters**.</span></span>
1. <span data-ttu-id="bac4c-119">Vytvořte nebo otevřete hlavní produkt a přejděte na jeho stránku **Detaily produktu**.</span><span class="sxs-lookup"><span data-stu-id="bac4c-119">Create or open a product master to go to its **Product details** page.</span></span>
1. <span data-ttu-id="bac4c-120">Nastavte možnost **Povolit převody měrných jednotek** na *Ano*.</span><span class="sxs-lookup"><span data-stu-id="bac4c-120">Set the **Enable unit of measure conversions** option to *Yes*.</span></span>
1. <span data-ttu-id="bac4c-121">V podokně akcí na kartě **Produkt** ve skupině **Nastavení** zvolte **Převody jednotek**.</span><span class="sxs-lookup"><span data-stu-id="bac4c-121">On the Action Pane, on the **Product** tab, in the **Set up** group, select **Unit conversions**.</span></span>
1. <span data-ttu-id="bac4c-122">Otevře se stránka **Převody jednotek**.</span><span class="sxs-lookup"><span data-stu-id="bac4c-122">The **Unit conversions** page opens.</span></span> <span data-ttu-id="bac4c-123">Vyberte jeden z následujících karet:</span><span class="sxs-lookup"><span data-stu-id="bac4c-123">Select one of the following tabs:</span></span>

    - <span data-ttu-id="bac4c-124">**Převody uvnitř třídy** - Tuto kartu vyberte, chcete-li převádět jednotky, které patří do stejné třídy jednotek.</span><span class="sxs-lookup"><span data-stu-id="bac4c-124">**Intra-class conversions** – Select this tab to convert between units that belong to the same unit class.</span></span>
    - <span data-ttu-id="bac4c-125">**Převody vně třídy** - Tuto kartu vyberte, chcete-li převádět jednotky, které nepatří do stejné třídy jednotek.</span><span class="sxs-lookup"><span data-stu-id="bac4c-125">**Inter-class conversions** – Select this tab to convert between units that belong to different unit classes.</span></span>

1. <span data-ttu-id="bac4c-126">K přidání nového převodu jednotek klikněte na tlačítko **Nový**.</span><span class="sxs-lookup"><span data-stu-id="bac4c-126">Select **New** to add a new unit conversion.</span></span>
1. <span data-ttu-id="bac4c-127">Nastavte pole **Vytvořit převod pro** na jednu z následujících hodnot:</span><span class="sxs-lookup"><span data-stu-id="bac4c-127">Set the **Create conversion for** field to one of the following values:</span></span>

    - <span data-ttu-id="bac4c-128">**Produkt** - Vyberete-li tuto hodnotu, můžete nastavit převod jednotky pro základní produkt.</span><span class="sxs-lookup"><span data-stu-id="bac4c-128">**Product** – If you select this value, you can set up a unit conversion for the product master.</span></span> <span data-ttu-id="bac4c-129">Tento převod jednotek bude použit jako záložní pro všechny varianty produktů, pro které není definovaný žádný převod jednotek.</span><span class="sxs-lookup"><span data-stu-id="bac4c-129">That unit conversion will be used as a fallback for all product variants that no unit conversion is defined for.</span></span>
    - <span data-ttu-id="bac4c-130">**Varianta produkt** - Vyberete-li tuto hodnotu, můžete nastavit převod jednotky pro určitou variantu produktu.</span><span class="sxs-lookup"><span data-stu-id="bac4c-130">**Product variant** – If you select this value, you can set up a unit conversion for a specific product variant.</span></span> <span data-ttu-id="bac4c-131">Použijte pole **Varianta produktu** k výběru varianty.</span><span class="sxs-lookup"><span data-stu-id="bac4c-131">Use the **Product variant** field to select the variant.</span></span>

    ![![Přidání nového převodu jednotek](media/uom-new-conversion.png "Přidání nového převodu jednotek")](media/uom-new-conversion.png "Adding a new unit conversion")

1. <span data-ttu-id="bac4c-133">K nastavení převodu jednotek použijte další pole, která jsou k dispozici.</span><span class="sxs-lookup"><span data-stu-id="bac4c-133">Use the other fields that are provided to set up your unit conversion.</span></span>
1. <span data-ttu-id="bac4c-134">Vyberte **OK** k uložení nového převodu jednotek.</span><span class="sxs-lookup"><span data-stu-id="bac4c-134">Select **OK** to save the new unit conversion.</span></span>

> [!TIP]
> <span data-ttu-id="bac4c-135">Otevřete stránku **Převody jednotek** pro produkt nebo variantu produktu z kterékoli z následujících stránek:</span><span class="sxs-lookup"><span data-stu-id="bac4c-135">You can open the **Unit conversions** page for a product or a product variant from any of the following pages:</span></span>
> 
> - <span data-ttu-id="bac4c-136">Podrobnosti produktu</span><span class="sxs-lookup"><span data-stu-id="bac4c-136">Product details</span></span>
> - <span data-ttu-id="bac4c-137">Podrobnosti o uvolněných produktech</span><span class="sxs-lookup"><span data-stu-id="bac4c-137">Released products details</span></span>
> - <span data-ttu-id="bac4c-138">Uvolněné varianty produktu</span><span class="sxs-lookup"><span data-stu-id="bac4c-138">Released product variants</span></span>

## <a name="example-scenario"></a><span data-ttu-id="bac4c-139">Příklad</span><span class="sxs-lookup"><span data-stu-id="bac4c-139">Example scenario</span></span>

<span data-ttu-id="bac4c-140">V tomto scénáři společnost prodává trička ve velikostech S, M, L a XL.</span><span class="sxs-lookup"><span data-stu-id="bac4c-140">In this scenario, a company sells T-shirts in sizes small, medium, large, and extra-large.</span></span> <span data-ttu-id="bac4c-141">Tričko je definováno jako produkt a jsou definovány různé velikosti variant produktu.</span><span class="sxs-lookup"><span data-stu-id="bac4c-141">The T-shirt is defined as a product, and the different sizes are defined as variants of that product.</span></span> <span data-ttu-id="bac4c-142">Košile jsou baleny v krabicích.</span><span class="sxs-lookup"><span data-stu-id="bac4c-142">The shirts are packed in boxes.</span></span> <span data-ttu-id="bac4c-143">Pro S, M a L velikosti může být v každé krabici pět košil.</span><span class="sxs-lookup"><span data-stu-id="bac4c-143">For sizes small, medium, and large, there can be five shirts in each box.</span></span> <span data-ttu-id="bac4c-144">Avšak pro velikost XL je v každé krabici místo pouze pro čtyři košile.</span><span class="sxs-lookup"><span data-stu-id="bac4c-144">However, for size extra-large, there is space for only four shirts in each box.</span></span>

<span data-ttu-id="bac4c-145">Společnost chce sledovat různé varianty triček podle *kusů*, ale prodávat je po *krabicích*.</span><span class="sxs-lookup"><span data-stu-id="bac4c-145">The company wants to track the different variants in the *Pieces* unit, but it's selling them in the *Boxes* unit.</span></span> <span data-ttu-id="bac4c-146">U S, M a L velikostí je převod mezi jednotkou zásob a prodejní jednotkou 1 krabice = 5 kusů.</span><span class="sxs-lookup"><span data-stu-id="bac4c-146">For sizes small, medium, and large, the conversion between the inventory unit and the sales unit is 1 Box = 5 Pieces.</span></span> <span data-ttu-id="bac4c-147">U XL velikosti je převod 1 krabice = 4 kusy.</span><span class="sxs-lookup"><span data-stu-id="bac4c-147">For size extra-large, the conversion is 1 Box = 4 Pieces.</span></span>

1. <span data-ttu-id="bac4c-148">Ze stránky **Podrobnosti o zveřejnění produktu** pro **tričko** otevřete stránku **Převod jednotek**.</span><span class="sxs-lookup"><span data-stu-id="bac4c-148">From the **Released product details** page for the **T-Shirt** product, open the **Unit conversions** page.</span></span>
1. <span data-ttu-id="bac4c-149">Na stránce **Převod jednotek** nastavte převod jednotek pro variantu produktu **XL** takto.</span><span class="sxs-lookup"><span data-stu-id="bac4c-149">On the **Unit conversions** page, set up the following unit conversion for the **X-Large** released product variant.</span></span>

    | <span data-ttu-id="bac4c-150">Pole</span><span class="sxs-lookup"><span data-stu-id="bac4c-150">Field</span></span>                 | <span data-ttu-id="bac4c-151">Nastavení</span><span class="sxs-lookup"><span data-stu-id="bac4c-151">Setting</span></span>                 |
    |-----------------------|-------------------------|
    | <span data-ttu-id="bac4c-152">Vytvoření převodu pro</span><span class="sxs-lookup"><span data-stu-id="bac4c-152">Create conversion for</span></span> | <span data-ttu-id="bac4c-153">Varianta produktu</span><span class="sxs-lookup"><span data-stu-id="bac4c-153">Product variant</span></span>         |
    | <span data-ttu-id="bac4c-154">Varianta produktu</span><span class="sxs-lookup"><span data-stu-id="bac4c-154">Product variant</span></span>       | <span data-ttu-id="bac4c-155">Tričko : : XL : :</span><span class="sxs-lookup"><span data-stu-id="bac4c-155">T-Shirt : : X-Large : :</span></span> |
    | <span data-ttu-id="bac4c-156">Z jednotky</span><span class="sxs-lookup"><span data-stu-id="bac4c-156">From unit</span></span>             | <span data-ttu-id="bac4c-157">Krabice</span><span class="sxs-lookup"><span data-stu-id="bac4c-157">Boxes</span></span>                   |
    | <span data-ttu-id="bac4c-158">Koeficient</span><span class="sxs-lookup"><span data-stu-id="bac4c-158">Factor</span></span>                | <span data-ttu-id="bac4c-159">4</span><span class="sxs-lookup"><span data-stu-id="bac4c-159">4</span></span>                       |
    | <span data-ttu-id="bac4c-160">Do jednotky</span><span class="sxs-lookup"><span data-stu-id="bac4c-160">To Unit</span></span>               | <span data-ttu-id="bac4c-161">Kusy</span><span class="sxs-lookup"><span data-stu-id="bac4c-161">Pieces</span></span>                  |

1. <span data-ttu-id="bac4c-162">Protože varianty zveřejněného produktu **S**, **M** a **L** mají stejný převod jednotek mezi jednotkou *krabice* a *kusů*, znamená to, že můžete definovat převod jednotky pro tyto varianty produktu pro základní produkt.</span><span class="sxs-lookup"><span data-stu-id="bac4c-162">Because the **Small**, **Medium**, and **Large** product variants all have the same unit conversion between the *Box* and *Pieces* units, you can define the following unit conversion for them on the product master.</span></span>

    | <span data-ttu-id="bac4c-163">Pole</span><span class="sxs-lookup"><span data-stu-id="bac4c-163">Field</span></span>                 | <span data-ttu-id="bac4c-164">Nastavení</span><span class="sxs-lookup"><span data-stu-id="bac4c-164">Setting</span></span> |
    |-----------------------|---------|
    | <span data-ttu-id="bac4c-165">Vytvoření převodu pro</span><span class="sxs-lookup"><span data-stu-id="bac4c-165">Create conversion for</span></span> | <span data-ttu-id="bac4c-166">Produkt</span><span class="sxs-lookup"><span data-stu-id="bac4c-166">Product</span></span> |
    | <span data-ttu-id="bac4c-167">Produkt</span><span class="sxs-lookup"><span data-stu-id="bac4c-167">Product</span></span>               | <span data-ttu-id="bac4c-168">Tričko</span><span class="sxs-lookup"><span data-stu-id="bac4c-168">T-Shirt</span></span> |
    | <span data-ttu-id="bac4c-169">Z jednotky</span><span class="sxs-lookup"><span data-stu-id="bac4c-169">From unit</span></span>             | <span data-ttu-id="bac4c-170">Krabice</span><span class="sxs-lookup"><span data-stu-id="bac4c-170">Boxes</span></span>   |
    | <span data-ttu-id="bac4c-171">Koeficient</span><span class="sxs-lookup"><span data-stu-id="bac4c-171">Factor</span></span>                | <span data-ttu-id="bac4c-172">5</span><span class="sxs-lookup"><span data-stu-id="bac4c-172">5</span></span>       |
    | <span data-ttu-id="bac4c-173">Do jednotky</span><span class="sxs-lookup"><span data-stu-id="bac4c-173">To Unit</span></span>               | <span data-ttu-id="bac4c-174">Kusy</span><span class="sxs-lookup"><span data-stu-id="bac4c-174">Pieces</span></span>  |

## <a name="using-excel-to-update-the-unit-conversions"></a><span data-ttu-id="bac4c-175">Použití aplikace Excel pro aktualizaci převodů jednotek</span><span class="sxs-lookup"><span data-stu-id="bac4c-175">Using Excel to update the unit conversions</span></span>

<span data-ttu-id="bac4c-176">Pokud má produkt mnoho variant produktu, které mají různé jednotkové převody, je vhodné exportovat jednotkové převody do sešitu Microsoft Excel, aktualizovat je a poté je publikovat zpět do Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="bac4c-176">If a product has many product variants that have different unit conversions, it's a good idea to export the unit conversions to a Microsoft Excel workbook, update them, and then publish them back to Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="bac4c-177">Chcete-li exportovat jednotkové převody do Excelu, na stránce **Převody jednotek** v podokně akcí vyberte **Otevřít v Microsoft Office**.</span><span class="sxs-lookup"><span data-stu-id="bac4c-177">To export unit conversions to Excel, on the **Unit conversions** page, on the Action Pane, select **Open in Microsoft Office**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bac4c-178">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="bac4c-178">Additional resources</span></span>

[<span data-ttu-id="bac4c-179">Správa měrných jednotek</span><span class="sxs-lookup"><span data-stu-id="bac4c-179">Manage unit of measure</span></span>](tasks/manage-unit-measure.md)
