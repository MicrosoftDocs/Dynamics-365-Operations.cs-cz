---
title: Modul košíku
description: Tohle téma se zabývá moduly košíku a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d9a15f85838849796d6ce4674712636251c75bf3
ms.sourcegitcommit: 97ceb24f191161ca601e0889a539df665834ac3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/16/2020
ms.locfileid: "3818268"
---
# <a name="cart-module"></a><span data-ttu-id="3309c-103">Modul košíku</span><span class="sxs-lookup"><span data-stu-id="3309c-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3309c-104">Tohle téma se zabývá moduly košíku a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3309c-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="3309c-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="3309c-105">Overview</span></span>

<span data-ttu-id="3309c-106">Modul košíku zobrazuje položky, které byly přidány do košíku, než odběratel pokračuje v rezervaci.</span><span class="sxs-lookup"><span data-stu-id="3309c-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="3309c-107">Modul také zobrazuje souhrn objednávky a umožňuje odběrateli použití nebo odebrání propagačních kódů.</span><span class="sxs-lookup"><span data-stu-id="3309c-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="3309c-108">Modul košíku podporuje přihlášené uživatele i hosty.</span><span class="sxs-lookup"><span data-stu-id="3309c-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="3309c-109">Také podporuje odkaz **Zpět na nákupy**.</span><span class="sxs-lookup"><span data-stu-id="3309c-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="3309c-110">Můžete konfigurovat cestu pro tento odkaz v **Nastavení webu \> Rozšíření \> Cesty**.</span><span class="sxs-lookup"><span data-stu-id="3309c-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="3309c-111">Modul košíku vykresluje data založená na ID košíku, což je soubor cookie prohlížeče dostupný v rámci celého webu.</span><span class="sxs-lookup"><span data-stu-id="3309c-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span> 

<span data-ttu-id="3309c-112">Následující obrázek ukazuje příklad stránky nákupního košíku na webu Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="3309c-112">The following image shows an example of a cart page on the Fabrikam site.</span></span>

![Příklad modulu nákupního košíku na webu Fabrikam](./media/cart2.PNG)

<span data-ttu-id="3309c-114">Následující obrázek ukazuje příklad stránky nákupního košíku na webu Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="3309c-114">The following image shows an example of a cart page on the Fabrikam site.</span></span> <span data-ttu-id="3309c-115">V tomto příkladu je za řádkovou položku účtován manipulační poplatek.</span><span class="sxs-lookup"><span data-stu-id="3309c-115">In this example, there is a handling fee for a line item.</span></span>

![Příklad modulu nákupního košíku s manipulačním poplatkem za řádkovou položku](./media/ecommerce-handling-fee.png)

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="3309c-117">Vlastnosti a pozice modulu košíku</span><span class="sxs-lookup"><span data-stu-id="3309c-117">Cart module properties and slots</span></span>

| <span data-ttu-id="3309c-118">Vlastnost</span><span class="sxs-lookup"><span data-stu-id="3309c-118">Property</span></span> | <span data-ttu-id="3309c-119">Hodnoty</span><span class="sxs-lookup"><span data-stu-id="3309c-119">Values</span></span> | <span data-ttu-id="3309c-120">popis</span><span class="sxs-lookup"><span data-stu-id="3309c-120">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="3309c-121">Záhlaví</span><span class="sxs-lookup"><span data-stu-id="3309c-121">Heading</span></span> | <span data-ttu-id="3309c-122">Text a značka nadpisu (**H1**, **H2**, **H3**, **H4**, **H5** nebo **H6**)</span><span class="sxs-lookup"><span data-stu-id="3309c-122">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="3309c-123">Nadpis košíku, jako "Nákupní taška" nebo "Položky v nákupním košíku".</span><span class="sxs-lookup"><span data-stu-id="3309c-123">A heading for the cart, such as "Shopping bag" or "Items in your cart."</span></span> |
| <span data-ttu-id="3309c-124">Zobrazit chybu vyprodanosti</span><span class="sxs-lookup"><span data-stu-id="3309c-124">Show out of stock errors</span></span> | <span data-ttu-id="3309c-125">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="3309c-125">**True** or **False**</span></span> | <span data-ttu-id="3309c-126">Pokud je tato vlastnost nastavena na **Pravda**, na stránce košíku se zobrazí chyby související s akciemi.</span><span class="sxs-lookup"><span data-stu-id="3309c-126">If this property is set to **True**, the cart page will show stock-related errors.</span></span> <span data-ttu-id="3309c-127">Doporučujeme nastavit tuto vlastnost na **Pravda** pokud jsou na webu prováděny kontroly zásob.</span><span class="sxs-lookup"><span data-stu-id="3309c-127">We recommend that you set this property to **True** if inventory checks are applied on the site.</span></span> |
| <span data-ttu-id="3309c-128">Zobrazit přepravní poplatky u řádkových položek</span><span class="sxs-lookup"><span data-stu-id="3309c-128">Show shipping charges for line items</span></span> | <span data-ttu-id="3309c-129">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="3309c-129">**True** or **False**</span></span> | <span data-ttu-id="3309c-130">Pokud je tato vlastnost nastavena na **Pravda**, řádkové položky košíku zobrazí přepravné, jsou-li tyto informace k dispozici.</span><span class="sxs-lookup"><span data-stu-id="3309c-130">If this property is set to **True**, cart line items will show the shipping charges, if this information is available.</span></span> <span data-ttu-id="3309c-131">Tato funkce není v motivu Fabrikam podporována, protože uživatelé vyberou dopravu pouze v pokladně.</span><span class="sxs-lookup"><span data-stu-id="3309c-131">This feature isn't supported in the Fabrikam theme, because users select shipping only in the checkout flow.</span></span> <span data-ttu-id="3309c-132">Tuto funkci však lze zapnout v jiných workflowech, pokud je to možné.</span><span class="sxs-lookup"><span data-stu-id="3309c-132">However, this feature can be turned on in other workflows if it's applicable.</span></span> |

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="3309c-133">Moduly, které lze použít v modulu košíku</span><span class="sxs-lookup"><span data-stu-id="3309c-133">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="3309c-134">**Textový blok** – Tento modul podporuje vlastní zasílání zpráv v modulu košíku.</span><span class="sxs-lookup"><span data-stu-id="3309c-134">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="3309c-135">Zprávy řídí systém správy obsahu (CMS).</span><span class="sxs-lookup"><span data-stu-id="3309c-135">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="3309c-136">Lze přidat libovolnou zprávu, například „Při problémech s objednávkou volejte 123 456 789“.</span><span class="sxs-lookup"><span data-stu-id="3309c-136">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="3309c-137">**Volič obchodů** – Tento modul zobrazuje seznam obchodů, které jsou poblíž a kde je položka k výdeji.</span><span class="sxs-lookup"><span data-stu-id="3309c-137">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="3309c-138">Umožňuje uživatelům zadat umístění pro hledání obchodů, které jsou v okolí.</span><span class="sxs-lookup"><span data-stu-id="3309c-138">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="3309c-139">Další informace o tomto modulu naleznete v tématu [Modul volič obchodů](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="3309c-139">For more information on this module, see [Store selector module](store-selector.md).</span></span>

## <a name="module-properties"></a><span data-ttu-id="3309c-140">Vlastnosti modulu</span><span class="sxs-lookup"><span data-stu-id="3309c-140">Module properties</span></span>

<span data-ttu-id="3309c-141">Následující nastavení modulu nákupního košíku lze konfigurovat na **Nastavení webu \> Rozšíření**:</span><span class="sxs-lookup"><span data-stu-id="3309c-141">The following cart module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="3309c-142">**Maximální množství** – tato vlastnost se používá k určení maximálního počtu jednotlivých položek, které lze přidat do nákupního košíku.</span><span class="sxs-lookup"><span data-stu-id="3309c-142">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="3309c-143">Maloobchodní prodejce může například rozhodnout, že v jedné transakci lze prodávat pouze 10 jednotlivých produktů.</span><span class="sxs-lookup"><span data-stu-id="3309c-143">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="3309c-144">**Zásoby** – Informace, jak použít nastavení zásob, naleznete v části [Použití nastavení zásob](inventory-settings.md).</span><span class="sxs-lookup"><span data-stu-id="3309c-144">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="3309c-145">**Zpět k nákupu** – Tato vlastnost se používá k určení trasy pro odkaz **Zpět k nákupu**.</span><span class="sxs-lookup"><span data-stu-id="3309c-145">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="3309c-146">Postup lze konfigurovat na úrovni webu a umožnit maloobchodním prodejcům, aby se odběratel mohl vrátit na domovskou stránku nebo na jakoukoli jinou stránku na webu.</span><span class="sxs-lookup"><span data-stu-id="3309c-146">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="3309c-147">Interakce Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="3309c-147">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="3309c-148">Modul košíku načítá informace o produktu pomocí rozhraní API Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="3309c-148">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="3309c-149">ID košíku ze souboru cookie prohlížeče se používá k načtení všech informací o produktu z Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="3309c-149">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="3309c-150">Přidání modulu košíku na stránku</span><span class="sxs-lookup"><span data-stu-id="3309c-150">Add a cart module to a page</span></span>

<span data-ttu-id="3309c-151">Chcete-li přidat modul košíku na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="3309c-151">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="3309c-152">Přejděte na **Fragmenty** a volbou **Nový** vytvořte nový fragment.</span><span class="sxs-lookup"><span data-stu-id="3309c-152">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="3309c-153">V dialogovém okně **Nový fragment** vyberte modul **Košík**.</span><span class="sxs-lookup"><span data-stu-id="3309c-153">In the **New fragment** dialog box, select the **Cart** module.</span></span>
1. <span data-ttu-id="3309c-154">V části **Název fragmentu** zadejte název pro **Fragment košíku** a poté vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="3309c-154">Under **Fragment name**, enter the name **Cart fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="3309c-155">Vyberte pozici **Nákupní košík**.</span><span class="sxs-lookup"><span data-stu-id="3309c-155">Select the **Cart** slot.</span></span>
1. <span data-ttu-id="3309c-156">V podokně vlastností vpravo vyberte symbol tužky, do pole zadejte text záhlaví a poté zaškrtněte symbol zaškrtnutí.</span><span class="sxs-lookup"><span data-stu-id="3309c-156">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="3309c-157">V pozici **Nákupní košík** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="3309c-157">In the **Cart** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="3309c-158">V dialogovém okně **Přidat modul** vyberte modul **Volba obchodu** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="3309c-158">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="3309c-159">Chcete-li vrátit fragment se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** jej publikujte.</span><span class="sxs-lookup"><span data-stu-id="3309c-159">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="3309c-160">Přejděte na **Šablony** a poté volbou **Nová** vytvořte novou šablonu.</span><span class="sxs-lookup"><span data-stu-id="3309c-160">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="3309c-161">V dialogovém okně **Nová šablona** v části **Název šablony** zadejte název šablony.</span><span class="sxs-lookup"><span data-stu-id="3309c-161">In the **New Template** dialog box, under **Template name**, enter a name for the template.</span></span>
1. <span data-ttu-id="3309c-162">Ve stromové struktuře vyberte pozici **Obsah**, vyberte tři tečky (**...**) a vyberte možnost **Přidat fragment**.</span><span class="sxs-lookup"><span data-stu-id="3309c-162">In the outline tree, select the **Body** slot, select the ellipsis (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="3309c-163">V dialogovém okně **Vybrat fragment** vyberte **Fragment košíku** a pak vyberte tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="3309c-163">In the **Select fragment** dialog box, select the **Cart fragment** fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="3309c-164">Chcete-li vrátit šablonu se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="3309c-164">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="3309c-165">Přejděte na **Stránky** a volbou **Nová** vytvořte novou stránku.</span><span class="sxs-lookup"><span data-stu-id="3309c-165">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="3309c-166">V dialogovém okně **Zvolte šablonu** vyberte šablonu, kterou jste vytvořili, zadejte název stránky a pak vyberte tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="3309c-166">In the **Choose a template** dialog box, select the template that you created, enter a page name, and then select **OK**.</span></span>
1. <span data-ttu-id="3309c-167">Vyberte možnost **Uložit** a poté vyberte možnost **Náhled**, chcete-li zobrazit náhled stránky.</span><span class="sxs-lookup"><span data-stu-id="3309c-167">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="3309c-168">Chcete-li vrátit stránku se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="3309c-168">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3309c-169">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="3309c-169">Additional resources</span></span>

[<span data-ttu-id="3309c-170">Modul ikony košíku</span><span class="sxs-lookup"><span data-stu-id="3309c-170">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="3309c-171">Modul pokladny</span><span class="sxs-lookup"><span data-stu-id="3309c-171">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="3309c-172">Modul platby</span><span class="sxs-lookup"><span data-stu-id="3309c-172">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="3309c-173">Modul dodací adresy</span><span class="sxs-lookup"><span data-stu-id="3309c-173">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="3309c-174">Modul možností doručení</span><span class="sxs-lookup"><span data-stu-id="3309c-174">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="3309c-175">Modul podrobností objednávky</span><span class="sxs-lookup"><span data-stu-id="3309c-175">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="3309c-176">Modul dárkového poukazu</span><span class="sxs-lookup"><span data-stu-id="3309c-176">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="3309c-177">Výpočet dostupnosti zásob pro maloobchodní kanály</span><span class="sxs-lookup"><span data-stu-id="3309c-177">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
