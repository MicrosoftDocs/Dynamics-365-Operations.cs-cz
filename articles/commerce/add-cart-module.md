---
title: Modul košíku
description: Tohle téma se zabývá moduly košíku a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 12/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: abb9909c03577763ff7e6242c9395a58159df6ca
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985972"
---
# <a name="cart-module"></a><span data-ttu-id="636f7-103">Modul košíku</span><span class="sxs-lookup"><span data-stu-id="636f7-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="636f7-104">Tohle téma se zabývá moduly košíku a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="636f7-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="636f7-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="636f7-105">Overview</span></span>

<span data-ttu-id="636f7-106">Modul košíku zobrazuje položky, které byly přidány do košíku, než odběratel pokračuje v rezervaci.</span><span class="sxs-lookup"><span data-stu-id="636f7-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="636f7-107">Modul také zobrazuje souhrn objednávky a umožňuje odběrateli použití nebo odebrání propagačních kódů.</span><span class="sxs-lookup"><span data-stu-id="636f7-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="636f7-108">Modul košíku podporuje přihlášené uživatele i hosty.</span><span class="sxs-lookup"><span data-stu-id="636f7-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="636f7-109">Také podporuje odkaz **Zpět na nákupy**.</span><span class="sxs-lookup"><span data-stu-id="636f7-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="636f7-110">Můžete konfigurovat cestu pro tento odkaz v **Nastavení webu \> Rozšíření \> Cesty**.</span><span class="sxs-lookup"><span data-stu-id="636f7-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="636f7-111">Modul košíku vykresluje data založená na ID košíku, což je soubor cookie prohlížeče dostupný v rámci celého webu.</span><span class="sxs-lookup"><span data-stu-id="636f7-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span> 

<span data-ttu-id="636f7-112">Následující obrázek ukazuje příklad stránky nákupního košíku na webu Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="636f7-112">The following image shows an example of a cart page on the Fabrikam site.</span></span>

![Příklad modulu nákupního košíku na webu Fabrikam](./media/cart2.PNG)

<span data-ttu-id="636f7-114">Následující obrázek ukazuje příklad stránky nákupního košíku na webu Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="636f7-114">The following image shows an example of a cart page on the Fabrikam site.</span></span> <span data-ttu-id="636f7-115">V tomto příkladu je za řádkovou položku účtován manipulační poplatek.</span><span class="sxs-lookup"><span data-stu-id="636f7-115">In this example, there is a handling fee for a line item.</span></span>

![Příklad modulu nákupního košíku s manipulačním poplatkem za řádkovou položku](./media/ecommerce-handling-fee.png)

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="636f7-117">Vlastnosti a pozice modulu košíku</span><span class="sxs-lookup"><span data-stu-id="636f7-117">Cart module properties and slots</span></span>

| <span data-ttu-id="636f7-118">Vlastnost</span><span class="sxs-lookup"><span data-stu-id="636f7-118">Property</span></span> | <span data-ttu-id="636f7-119">Hodnoty</span><span class="sxs-lookup"><span data-stu-id="636f7-119">Values</span></span> | <span data-ttu-id="636f7-120">popis</span><span class="sxs-lookup"><span data-stu-id="636f7-120">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="636f7-121">Záhlaví</span><span class="sxs-lookup"><span data-stu-id="636f7-121">Heading</span></span> | <span data-ttu-id="636f7-122">Text a značka nadpisu (**H1**, **H2**, **H3**, **H4**, **H5** nebo **H6**)</span><span class="sxs-lookup"><span data-stu-id="636f7-122">Heading text and a heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="636f7-123">Nadpis košíku, jako "Nákupní taška" nebo "Položky v nákupním košíku".</span><span class="sxs-lookup"><span data-stu-id="636f7-123">A heading for the cart, such as "Shopping bag" or "Items in your cart."</span></span> |
| <span data-ttu-id="636f7-124">Zobrazit chybu vyprodanosti</span><span class="sxs-lookup"><span data-stu-id="636f7-124">Show out of stock errors</span></span> | <span data-ttu-id="636f7-125">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="636f7-125">**True** or **False**</span></span> | <span data-ttu-id="636f7-126">Pokud je tato vlastnost nastavena na **Pravda**, na stránce košíku se zobrazí chyby související s akciemi.</span><span class="sxs-lookup"><span data-stu-id="636f7-126">If this property is set to **True**, the cart page will show stock-related errors.</span></span> <span data-ttu-id="636f7-127">Doporučujeme nastavit tuto vlastnost na **Pravda** pokud jsou na webu prováděny kontroly zásob.</span><span class="sxs-lookup"><span data-stu-id="636f7-127">We recommend that you set this property to **True** if inventory checks are applied on the site.</span></span> |
| <span data-ttu-id="636f7-128">Zobrazit přepravní poplatky u řádkových položek</span><span class="sxs-lookup"><span data-stu-id="636f7-128">Show shipping charges for line items</span></span> | <span data-ttu-id="636f7-129">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="636f7-129">**True** or **False**</span></span> | <span data-ttu-id="636f7-130">Pokud je tato vlastnost nastavena na **Pravda**, řádkové položky košíku zobrazí přepravné, jsou-li tyto informace k dispozici.</span><span class="sxs-lookup"><span data-stu-id="636f7-130">If this property is set to **True**, cart line items will show the shipping charges, if this information is available.</span></span> <span data-ttu-id="636f7-131">Tato funkce není v motivu Fabrikam podporována, protože uživatelé vyberou dopravu pouze v pokladně.</span><span class="sxs-lookup"><span data-stu-id="636f7-131">This feature isn't supported in the Fabrikam theme, because users select shipping only in the checkout flow.</span></span> <span data-ttu-id="636f7-132">Tuto funkci však lze zapnout v jiných workflowech, pokud je to možné.</span><span class="sxs-lookup"><span data-stu-id="636f7-132">However, this feature can be turned on in other workflows if it's applicable.</span></span> |
| <span data-ttu-id="636f7-133">Zobrazit dostupné propagační akce</span><span class="sxs-lookup"><span data-stu-id="636f7-133">Show available promotions</span></span>| <span data-ttu-id="636f7-134">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="636f7-134">**True** or **False**</span></span> | <span data-ttu-id="636f7-135">Pokud je tato vlastnost nastavena na **Pravda**, košík zobrazuje dostupné propagační akce na základě položek v košíku.</span><span class="sxs-lookup"><span data-stu-id="636f7-135">If this property is set to **True**, the cart shows available promotions, based on items in the cart.</span></span> <span data-ttu-id="636f7-136">Tato funkce je k dispozici ve vydání Dynamics 365 Commerce 10.0.16.</span><span class="sxs-lookup"><span data-stu-id="636f7-136">This capability is available in the Dynamics 365 Commerce 10.0.16 release.</span></span> |

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="636f7-137">Moduly, které lze použít v modulu košíku</span><span class="sxs-lookup"><span data-stu-id="636f7-137">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="636f7-138">**Textový blok** – Tento modul podporuje vlastní zasílání zpráv v modulu košíku.</span><span class="sxs-lookup"><span data-stu-id="636f7-138">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="636f7-139">Zprávy řídí systém správy obsahu (CMS).</span><span class="sxs-lookup"><span data-stu-id="636f7-139">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="636f7-140">Lze přidat libovolnou zprávu, například „Při problémech s objednávkou volejte 123 456 789“.</span><span class="sxs-lookup"><span data-stu-id="636f7-140">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="636f7-141">**Volič obchodů** – Tento modul zobrazuje seznam obchodů, které jsou poblíž a kde je položka k výdeji.</span><span class="sxs-lookup"><span data-stu-id="636f7-141">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="636f7-142">Umožňuje uživatelům zadat umístění pro hledání obchodů, které jsou v okolí.</span><span class="sxs-lookup"><span data-stu-id="636f7-142">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="636f7-143">Další informace o tomto modulu naleznete v tématu [Modul volič obchodů](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="636f7-143">For more information on this module, see [Store selector module](store-selector.md).</span></span>

## <a name="module-properties"></a><span data-ttu-id="636f7-144">Vlastnosti modulu</span><span class="sxs-lookup"><span data-stu-id="636f7-144">Module properties</span></span>

<span data-ttu-id="636f7-145">Následující nastavení modulu nákupního košíku lze konfigurovat na **Nastavení webu \> Rozšíření**:</span><span class="sxs-lookup"><span data-stu-id="636f7-145">The following cart module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="636f7-146">**Maximální množství** – tato vlastnost se používá k určení maximálního počtu jednotlivých položek, které lze přidat do nákupního košíku.</span><span class="sxs-lookup"><span data-stu-id="636f7-146">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="636f7-147">Maloobchodní prodejce může například rozhodnout, že v jedné transakci lze prodávat pouze 10 jednotlivých produktů.</span><span class="sxs-lookup"><span data-stu-id="636f7-147">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="636f7-148">**Zásoby** – Informace, jak použít nastavení zásob, naleznete v části [Použití nastavení zásob](inventory-settings.md).</span><span class="sxs-lookup"><span data-stu-id="636f7-148">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="636f7-149">**Zpět k nákupu** – Tato vlastnost se používá k určení trasy pro odkaz **Zpět k nákupu**.</span><span class="sxs-lookup"><span data-stu-id="636f7-149">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="636f7-150">Postup lze konfigurovat na úrovni webu a umožnit maloobchodním prodejcům, aby se odběratel mohl vrátit na domovskou stránku nebo na jakoukoli jinou stránku na webu.</span><span class="sxs-lookup"><span data-stu-id="636f7-150">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="636f7-151">V Dynamics 365 Commerce vydání 10.0.14 a novější jsou položky v košíku agregovány na základě nastavení, která jsou definována v profilu online funkcí pro online obchod v Commerce.</span><span class="sxs-lookup"><span data-stu-id="636f7-151">In the Dynamics 365 Commerce 10.0.14 release and later, items in the cart are aggregated based on the settings that are defined in the online functionality profile for the online store in Commerce headquarters.</span></span> <span data-ttu-id="636f7-152">Další informace o tom, jak vytvořit profil online funkcí a nastavit vlastnosti, které jsou vyžadovány pro agregaci, najdete v tématu [Vytvořte si online funkční profil](online-functionality-profile.md).</span><span class="sxs-lookup"><span data-stu-id="636f7-152">For more information about how to create an online functionality profile and set the properties that are required for aggregation, see [Create an online functionality profile](online-functionality-profile.md).</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="636f7-153">Interakce Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="636f7-153">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="636f7-154">Modul košíku načítá informace o produktu pomocí rozhraní API Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="636f7-154">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="636f7-155">ID košíku ze souboru cookie prohlížeče se používá k načtení všech informací o produktu z Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="636f7-155">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="636f7-156">Přidání modulu košíku na stránku</span><span class="sxs-lookup"><span data-stu-id="636f7-156">Add a cart module to a page</span></span>

<span data-ttu-id="636f7-157">Chcete-li přidat modul košíku na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="636f7-157">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="636f7-158">Přejděte na **Fragmenty** a volbou **Nový** vytvořte nový fragment.</span><span class="sxs-lookup"><span data-stu-id="636f7-158">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="636f7-159">V dialogovém okně **Nový fragment** vyberte modul **Košík**.</span><span class="sxs-lookup"><span data-stu-id="636f7-159">In the **New fragment** dialog box, select the **Cart** module.</span></span>
1. <span data-ttu-id="636f7-160">V části **Název fragmentu** zadejte název pro **Fragment košíku** a poté vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="636f7-160">Under **Fragment name**, enter the name **Cart fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="636f7-161">Vyberte pozici **Nákupní košík**.</span><span class="sxs-lookup"><span data-stu-id="636f7-161">Select the **Cart** slot.</span></span>
1. <span data-ttu-id="636f7-162">V podokně vlastností vpravo vyberte symbol tužky, do pole zadejte text záhlaví a poté zaškrtněte symbol zaškrtnutí.</span><span class="sxs-lookup"><span data-stu-id="636f7-162">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="636f7-163">V pozici **Nákupní košík** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="636f7-163">In the **Cart** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="636f7-164">V dialogovém okně **Přidat modul** vyberte modul **Volba obchodu** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="636f7-164">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="636f7-165">Chcete-li vrátit fragment se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** jej publikujte.</span><span class="sxs-lookup"><span data-stu-id="636f7-165">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="636f7-166">Přejděte na **Šablony** a poté volbou **Nová** vytvořte novou šablonu.</span><span class="sxs-lookup"><span data-stu-id="636f7-166">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="636f7-167">V dialogovém okně **Nová šablona** v části **Název šablony** zadejte název šablony.</span><span class="sxs-lookup"><span data-stu-id="636f7-167">In the **New Template** dialog box, under **Template name**, enter a name for the template.</span></span>
1. <span data-ttu-id="636f7-168">Ve stromové struktuře vyberte pozici **Obsah**, vyberte tři tečky (**...**) a vyberte možnost **Přidat fragment**.</span><span class="sxs-lookup"><span data-stu-id="636f7-168">In the outline tree, select the **Body** slot, select the ellipsis (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="636f7-169">V dialogovém okně **Vybrat fragment** vyberte **Fragment košíku** a pak vyberte tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="636f7-169">In the **Select fragment** dialog box, select the **Cart fragment** fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="636f7-170">Chcete-li vrátit šablonu se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="636f7-170">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="636f7-171">Přejděte na **Stránky** a volbou **Nová** vytvořte novou stránku.</span><span class="sxs-lookup"><span data-stu-id="636f7-171">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="636f7-172">V dialogovém okně **Zvolte šablonu** vyberte šablonu, kterou jste vytvořili, zadejte název stránky a pak vyberte tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="636f7-172">In the **Choose a template** dialog box, select the template that you created, enter a page name, and then select **OK**.</span></span>
1. <span data-ttu-id="636f7-173">Vyberte možnost **Uložit** a poté vyberte možnost **Náhled**, chcete-li zobrazit náhled stránky.</span><span class="sxs-lookup"><span data-stu-id="636f7-173">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="636f7-174">Chcete-li vrátit stránku se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="636f7-174">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="636f7-175">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="636f7-175">Additional resources</span></span>

[<span data-ttu-id="636f7-176">Modul ikony košíku</span><span class="sxs-lookup"><span data-stu-id="636f7-176">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="636f7-177">Modul pokladny</span><span class="sxs-lookup"><span data-stu-id="636f7-177">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="636f7-178">Platební modul</span><span class="sxs-lookup"><span data-stu-id="636f7-178">Payment module</span></span>](payment-module.md)

[<span data-ttu-id="636f7-179">Modul dodací adresy</span><span class="sxs-lookup"><span data-stu-id="636f7-179">Shipping address module</span></span>](ship-address-module.md)

[<span data-ttu-id="636f7-180">Modul možností doručení</span><span class="sxs-lookup"><span data-stu-id="636f7-180">Delivery options module</span></span>](delivery-options-module.md)

[<span data-ttu-id="636f7-181">Modul s informacemi o vyzvednutí</span><span class="sxs-lookup"><span data-stu-id="636f7-181">Pickup information module</span></span>](pickup-info-module.md)

[<span data-ttu-id="636f7-182">Modul podrobností objednávky</span><span class="sxs-lookup"><span data-stu-id="636f7-182">Order details module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="636f7-183">Modul dárkového poukazu</span><span class="sxs-lookup"><span data-stu-id="636f7-183">Gift card module</span></span>](add-giftcard.md)

[<span data-ttu-id="636f7-184">Výpočet dostupnosti zásob pro maloobchodní kanály</span><span class="sxs-lookup"><span data-stu-id="636f7-184">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)

[<span data-ttu-id="636f7-185">Vytvoření online funkčního profilu</span><span class="sxs-lookup"><span data-stu-id="636f7-185">Create an online functionality profile</span></span>](online-functionality-profile.md)
