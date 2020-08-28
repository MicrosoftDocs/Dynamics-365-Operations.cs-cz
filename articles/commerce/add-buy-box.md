---
title: Modul buy boxu
description: Tohle téma se zabývá moduly buy boxu a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3fe5c1eb5808ef778aeda29442fa884556671296
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686663"
---
# <a name="buy-box-module"></a><span data-ttu-id="39663-103">Modul buy boxu</span><span class="sxs-lookup"><span data-stu-id="39663-103">Buy box module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="39663-104">Tohle téma se zabývá moduly buy boxu a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="39663-104">This topic covers buy box modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="39663-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="39663-105">Overview</span></span>

<span data-ttu-id="39663-106">Termín *buy box* se obvykle vztahuje k oblasti stránky s podrobnostmi o produktu, která se nachází „above the fold“ a která je hostitelem nejdůležitějších informací vyžadovaných k provedení nákupu produktu.</span><span class="sxs-lookup"><span data-stu-id="39663-106">The term *buy box* typically refers to the area of a product details page that is "above the fold," and that hosts all the most important information that is required to make a product purchase.</span></span> <span data-ttu-id="39663-107">(Oblast „above the fold“ je viditelná po prvním načtení stránky, takže uživatelé nemusejí posouvat zobrazení směrem dolů, aby ji viděli.)</span><span class="sxs-lookup"><span data-stu-id="39663-107">(An area that is "above the fold" is visible when the page is first loaded, so that users don't have to scroll down to see it.)</span></span>

<span data-ttu-id="39663-108">Modul buy boxu je speciální kontejner, který slouží k hostování všech modulů, které jsou zobrazeny v oblasti buy boxu na stránce podrobností produktu.</span><span class="sxs-lookup"><span data-stu-id="39663-108">A buy box module is special container that is used to host all the modules that are shown in the buy box area of a product details page.</span></span>

<span data-ttu-id="39663-109">Adresa URL stránky s podrobnostmi o produktu obsahuje ID produktu.</span><span class="sxs-lookup"><span data-stu-id="39663-109">The URL of a product details page includes the product ID.</span></span> <span data-ttu-id="39663-110">Všechny informace, které jsou požadovány pro vygenerování modulu buy boxu, jsou odvozeny z tohoto ID produktu.</span><span class="sxs-lookup"><span data-stu-id="39663-110">All the information that is required to render a buy box module is derived from this product ID.</span></span> <span data-ttu-id="39663-111">Není-li zadáno ID produktu, nebude modul buy boxu na stránce správně vykreslen.</span><span class="sxs-lookup"><span data-stu-id="39663-111">If a product ID isn't provided, the buy box module won't be rendered correctly on a page.</span></span> <span data-ttu-id="39663-112">Modul buy boxu lze proto použít pouze na stránkách, které mají kontext produktu.</span><span class="sxs-lookup"><span data-stu-id="39663-112">Therefore, a buy box module can be used only on pages that have product context.</span></span> <span data-ttu-id="39663-113">Chcete-li použít položku na stránce, která nemá kontext produktu (například domovskou stránku nebo marketingovou stránku), je nutné provést další úpravy.</span><span class="sxs-lookup"><span data-stu-id="39663-113">To use it on a page that doesn't have product context (for example, a home page or a marketing page), you must do additional customizations.</span></span>

<span data-ttu-id="39663-114">Následující obrázek ukazuje příklad modulu buy boxu na stránce s podrobnostmi o produktu.</span><span class="sxs-lookup"><span data-stu-id="39663-114">The following image shows an example of a buy box module on a product details page.</span></span>

![Příklad modulu buy boxu](./media/ecommerce-pdp-buybox.PNG)

## <a name="buy-box-module-properties-and-slots"></a><span data-ttu-id="39663-116">Vlastnosti a pozice modulu buy boxu</span><span class="sxs-lookup"><span data-stu-id="39663-116">Buy box module properties and slots</span></span> 

<span data-ttu-id="39663-117">Na stránce s podrobnostmi o produktu je buy box rozdělen na dvě oblasti: oblast médií v levé části a oblast obsahu vpravo.</span><span class="sxs-lookup"><span data-stu-id="39663-117">On a product details page, a buy box is divided into two regions: a media region on the left and a content region on the right.</span></span> <span data-ttu-id="39663-118">Ve výchozím nastavení je poměr šířky sloupce oblasti médií k šířce sloupce oblast obsahu 2:1.</span><span class="sxs-lookup"><span data-stu-id="39663-118">By default, the ratio of the width of the media region column to the width of the content region column is 2:1.</span></span> <span data-ttu-id="39663-119">Na mobilních zařízeních obě oblasti navrstveny, takže se jedna oblast zobrazí pod druhou oblastí.</span><span class="sxs-lookup"><span data-stu-id="39663-119">On mobile devices, the two regions are stacked so that one region appears below the other region.</span></span> <span data-ttu-id="39663-120">Motivy lze použít k přizpůsobení šířky sloupců a rozměru pro skládání.</span><span class="sxs-lookup"><span data-stu-id="39663-120">Themes can be used to customize the column widths and stacking rank.</span></span>

<span data-ttu-id="39663-121">Modul buy boxu vykreslí název, popis, cenu a hodnocení produktu.</span><span class="sxs-lookup"><span data-stu-id="39663-121">A buy box module renders the title, description, price, and ratings of a product.</span></span> <span data-ttu-id="39663-122">Dále odběratelům vybírá varianty produktu, které mají různé atributy produktu, například velikost, styl a barvu.</span><span class="sxs-lookup"><span data-stu-id="39663-122">It also lets customers select product variants that have different product attributes, such as size, style, and color.</span></span> <span data-ttu-id="39663-123">Je-li vybrána varianta produktu, budou další vlastnosti v buy boxu (například popis a obrázky produktu) aktualizovány tak, aby odrážely informace o variantách.</span><span class="sxs-lookup"><span data-stu-id="39663-123">When a product variant is selected, other properties in the buy box (for example, the product description and images) are updated to reflect the variant information.</span></span> 

<span data-ttu-id="39663-124">Výběr množství je k dispozici, takže zákazníci mohou určit množství položek, které mají být zakoupeny.</span><span class="sxs-lookup"><span data-stu-id="39663-124">A quantity selector is provided, so that customers can specify the quantity of items to purchase.</span></span> <span data-ttu-id="39663-125">Maximální množství, které lze koupit, lze definovat v nastavení pracoviště.</span><span class="sxs-lookup"><span data-stu-id="39663-125">The maximum quantity that can be purchased can be defined in the site settings.</span></span>

<span data-ttu-id="39663-126">Z buy boxu mohou zákazníci také provádět akce, jako je přidání produktu do nákupního košíku, přidání produktu do svého seznamu přání a výběr místa výdeje.</span><span class="sxs-lookup"><span data-stu-id="39663-126">From the buy box, customers can also perform actions such as adding a product to the cart, adding a product to their wishlist, and selecting a pickup location.</span></span> <span data-ttu-id="39663-127">Tyto akce lze provést u produktu nebo varianty produktu.</span><span class="sxs-lookup"><span data-stu-id="39663-127">These actions can be performed on a product or a product variant.</span></span> <span data-ttu-id="39663-128">Chcete-li přidat produkt do seznamu přání, je nutné, aby byl přihlášen zákazník.</span><span class="sxs-lookup"><span data-stu-id="39663-128">To add a product to a wishlist, the customer must be signed in.</span></span>

<span data-ttu-id="39663-129">Pomocí motivů lze odebrat nebo změnit pořadí vlastností produktu a ovládacích prvků akcí pro buy box.</span><span class="sxs-lookup"><span data-stu-id="39663-129">Themes can be used to remove or change the order of buy box product properties and action controls.</span></span> 

## <a name="module-properties"></a><span data-ttu-id="39663-130">Vlastnosti modulu</span><span class="sxs-lookup"><span data-stu-id="39663-130">Module properties</span></span>

- <span data-ttu-id="39663-131">**Značka záhlaví** – Tato vlastnost definuje značku nadpisu produktu.</span><span class="sxs-lookup"><span data-stu-id="39663-131">**Heading tag** – This property defines the heading tag for the product title.</span></span> <span data-ttu-id="39663-132">Je-li buy box v horní části stránky, měla by být tato vlastnost nastavena na **H1**, aby vyhovovala standardům usnadnění.</span><span class="sxs-lookup"><span data-stu-id="39663-132">If the buy box is at the top of the page, this property should be set to **h1** to meet accessibility standards.</span></span> 

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a><span data-ttu-id="39663-133">Moduly, které lze použít v modulu buy boxu</span><span class="sxs-lookup"><span data-stu-id="39663-133">Modules that can be used in a buy box module</span></span>

- <span data-ttu-id="39663-134">**Galerie médií** – Tento modul slouží k předvedení obrázků produktu na stránce s podrobnostmi o produktu.</span><span class="sxs-lookup"><span data-stu-id="39663-134">**Media gallery** – This module is used to showcase images of a product on a product details page.</span></span> <span data-ttu-id="39663-135">Další informace o tomto modulu naleznete v části [Modul galerie médií](media-gallery-module.md).</span><span class="sxs-lookup"><span data-stu-id="39663-135">For more information about this module, see [Media gallery module](media-gallery-module.md).</span></span>
- <span data-ttu-id="39663-136">**Volič obchodů** – Tento modul zobrazuje seznam obchodů, které jsou poblíž a kde je položka k výdeji.</span><span class="sxs-lookup"><span data-stu-id="39663-136">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="39663-137">Umožňuje uživatelům zadat umístění pro hledání obchodů, které jsou v okolí.</span><span class="sxs-lookup"><span data-stu-id="39663-137">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="39663-138">Další informace o tomto modulu naleznete v části [Modul volby obchodu](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="39663-138">For more information about this module, see [Store selector module](store-selector.md).</span></span>

## <a name="buy-box-module-settings"></a><span data-ttu-id="39663-139">Nastavení modulu buy boxu</span><span class="sxs-lookup"><span data-stu-id="39663-139">Buy box module settings</span></span>

<span data-ttu-id="39663-140">Následující nastavení modulu buy boxu lze konfigurovat na **Nastavení webu \> Rozšíření**:</span><span class="sxs-lookup"><span data-stu-id="39663-140">The following buy box module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="39663-141">**Limit množství na řádku košíku** – Tato vlastnost se používá k určení maximálního počtu jednotlivých položek, které lze přidat do nákupního košíku.</span><span class="sxs-lookup"><span data-stu-id="39663-141">**Cart line quantity limit** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="39663-142">Maloobchodní prodejce může například rozhodnout, že v jedné transakci lze prodávat pouze 10 jednotlivých produktů.</span><span class="sxs-lookup"><span data-stu-id="39663-142">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="39663-143">**Zásoby** – Informace, jak použít nastavení zásob, naleznete v části [Použití nastavení zásob](inventory-settings.md).</span><span class="sxs-lookup"><span data-stu-id="39663-143">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="39663-144">**Přidat do nákupního košíku** – Tato vlastnost se používá ke specifikaci chování po přidání položky do košíku.</span><span class="sxs-lookup"><span data-stu-id="39663-144">**Add to cart** - This property is used to specify the behavior after an item is added to the cart.</span></span> <span data-ttu-id="39663-145">Možné hodnoty jsou **Přejít do nákupního košíku**, **Nepřecházet do nákupního košíku** a **Zobrazit oznámení**.</span><span class="sxs-lookup"><span data-stu-id="39663-145">The possible values are **Navigate to cart**, **Do not navigate to cart**, and **Show notifications**.</span></span> <span data-ttu-id="39663-146">Když je tato hodnota nastavena na **Přejít do nákupního košíku**, uživatelé jsou po přidání položky přesměrováni na stránku nákupního košíku.</span><span class="sxs-lookup"><span data-stu-id="39663-146">When the value is set to **Navigate to cart**, users are sent to the cart page after they add an item.</span></span> <span data-ttu-id="39663-147">Když je tato hodnota nastavena na **Nepřecházet do nákupního košíku**, uživatelé nejsou po přidání položky přesměrováni na stránku nákupního košíku.</span><span class="sxs-lookup"><span data-stu-id="39663-147">When the value is set to **Do not navigate to cart**, users aren't sent to the cart page after they add an item.</span></span> <span data-ttu-id="39663-148">Když je hodnota nastavena na **Zobrazit oznámení**, uživatelům se zobrazí potvrzovací oznámení a poté mohou nadále procházet stránku podrobností o produktu.</span><span class="sxs-lookup"><span data-stu-id="39663-148">When the value is set to **Show notifications**, users are shown a confirmation notification and can continue to browse on the product details page.</span></span> 

    <span data-ttu-id="39663-149">Následující obrázek ukazuje příklad potvrzovacího oznámení „přidáno do košíku“ na webu Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="39663-149">The following image shows an example of an "added to cart" confirmation notification on the Fabrikam site.</span></span>

    ![Příklad modulu oznámení](./media/ecommerce-addtocart-notifications.PNG)

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="39663-151">Interakce Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="39663-151">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="39663-152">Modul buy boxu načítá informace o produktu pomocí rozhraní API Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="39663-152">The buy box module retrieves product information by using Commerce Scale Unit application programming interfaces (APIs).</span></span> <span data-ttu-id="39663-153">ID produktu ze stránky s podrobnostmi o produktu slouží k načtení všech informací.</span><span class="sxs-lookup"><span data-stu-id="39663-153">The product ID from the product details page is used to retrieve all information.</span></span>

## <a name="add-a-buy-box-module-to-a-page"></a><span data-ttu-id="39663-154">Přidání modulu buy boxu na stránku</span><span class="sxs-lookup"><span data-stu-id="39663-154">Add a buy box module to a page</span></span>

<span data-ttu-id="39663-155">Chcete-li přidat modul buy boxu na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="39663-155">To add a buy box module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="39663-156">Přejděte na **Fragmenty** a volbou **Nový** vytvořte nový fragment.</span><span class="sxs-lookup"><span data-stu-id="39663-156">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="39663-157">V dialogovém okně **Nový fragment stránky** vyberte modul **Buybox**.</span><span class="sxs-lookup"><span data-stu-id="39663-157">In the **New page fragment** dialog box, select the **Buybox** module.</span></span>
1. <span data-ttu-id="39663-158">V části **Název fragmentu stránky** zadejte název pro **Fragment buy boxu** a poté vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="39663-158">Under **Page fragment name**, enter the name **Buy box fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="39663-159">V pozici **Galeria médií** modulu buy boxu vyberte tři tečky (**...**) a poté vyberte **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="39663-159">In the **Media Gallery** slot of the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="39663-160">V dialogovém okně **Přidat modul** vyberte modul **Galerie médií** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="39663-160">In the **Add Module** dialog box, select the **Media gallery** module, and then select **OK**.</span></span>
1. <span data-ttu-id="39663-161">V pozici **Volba obchodu** modulu buy boxu vyberte tři tečky (**...**) a poté vyberte **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="39663-161">In the **Store selector** slot of the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="39663-162">V dialogovém okně **Přidat modul** vyberte modul **Volba obchodu** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="39663-162">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="39663-163">Chcete-li vrátit fragment se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** jej publikujte.</span><span class="sxs-lookup"><span data-stu-id="39663-163">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="39663-164">Přejděte na **Šablony** a poté volbou **Nová** vytvořte novou šablonu.</span><span class="sxs-lookup"><span data-stu-id="39663-164">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="39663-165">V dialogovém okně **Nová šablona** v části **Název šablony** zadejte **Šablona stránky podrobností o produktu** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="39663-165">In the **New Template** dialog box, under **Template name**, enter **PDP template**, and then select **OK**.</span></span>
1. <span data-ttu-id="39663-166">V pozici **Tělo** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="39663-166">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="39663-167">V dialogovém okně **Přidat modul** vyberte modul **Výchozí stránka** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="39663-167">In the **Add Module** dialog box, select the **Default Page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="39663-168">V pozici **Hlavní** na výchozí stránce vyberte tři tečky (**...**) a vyberte možnost **Přidat fragment stránky**.</span><span class="sxs-lookup"><span data-stu-id="39663-168">In the **Main** slot of the default page, select the ellipsis (**...**), and then select **Add Page Fragment**.</span></span>
1. <span data-ttu-id="39663-169">V dialogovém okně **Vybrat fragment stránky** vyberte **Fragment buy boxu**, který jste vytvořili předtím, a pak vyberte tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="39663-169">In the **Select page fragment** dialog box, select the **Buy box fragment** fragment that you created earlier, and then select **OK**.</span></span>
1. <span data-ttu-id="39663-170">Chcete-li vrátit šablonu se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="39663-170">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="39663-171">Přejděte na **Stránky** a volbou **Nová** vytvořte novou stránku.</span><span class="sxs-lookup"><span data-stu-id="39663-171">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="39663-172">V dialogovém okně **Zvolte šablonu** vyberte šablonu **Šablona stránky podrobností o produktu**.</span><span class="sxs-lookup"><span data-stu-id="39663-172">In the **Choose a template** dialog box, select the **PDP template** template.</span></span> <span data-ttu-id="39663-173">V části **Název stránky** zadejte **Stránka podrobností o produktu** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="39663-173">Under **Page name**, enter **PDP page**, and then select **OK**.</span></span>
1. <span data-ttu-id="39663-174">V pozici **Hlavní** na nové stránce vyberte tři tečky (**...**) a vyberte možnost **Přidat fragment stránky**.</span><span class="sxs-lookup"><span data-stu-id="39663-174">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Page Fragment**.</span></span>
1. <span data-ttu-id="39663-175">V dialogovém okně **Vybrat fragment stránky** vyberte **Fragment buy boxu**, který jste vytvořili předtím, a pak vyberte tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="39663-175">In the **Select page fragment** dialog box, select the **Buy box fragment** fragment that you created earlier, and then select **OK**.</span></span>
1. <span data-ttu-id="39663-176">Uložte stránku a zobrazte náhled.</span><span class="sxs-lookup"><span data-stu-id="39663-176">Save and preview the page.</span></span> <span data-ttu-id="39663-177">Do adresy URL stránky náhledu přidejte parametr řetězce dotazu **?productid=&lt;id produktu&gt;**.</span><span class="sxs-lookup"><span data-stu-id="39663-177">Add the **?productid=&lt;product id&gt;** query string parameter to the URL of the preview page.</span></span> <span data-ttu-id="39663-178">Tímto způsobem se pro načtení a vykreslení stránky náhledu použije kontext produktu.</span><span class="sxs-lookup"><span data-stu-id="39663-178">In that way, the product context is used to load and render the preview page.</span></span>
1. <span data-ttu-id="39663-179">Chcete-li vrátit stránku se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="39663-179">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> <span data-ttu-id="39663-180">Na stránce s podrobnostmi o produktu by se měl zobrazit buy box.</span><span class="sxs-lookup"><span data-stu-id="39663-180">A buy box should appear on the product details page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="39663-181">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="39663-181">Additional resources</span></span>

[<span data-ttu-id="39663-182">Přehled startovací sady</span><span class="sxs-lookup"><span data-stu-id="39663-182">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="39663-183">Modul volby obchodu</span><span class="sxs-lookup"><span data-stu-id="39663-183">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="39663-184">Modul galerie médií</span><span class="sxs-lookup"><span data-stu-id="39663-184">Media gallery module</span></span>](media-gallery-module.md)

[<span data-ttu-id="39663-185">Modul kontejneru</span><span class="sxs-lookup"><span data-stu-id="39663-185">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="39663-186">Modul košíku</span><span class="sxs-lookup"><span data-stu-id="39663-186">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="39663-187">Modul ikony košíku</span><span class="sxs-lookup"><span data-stu-id="39663-187">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="39663-188">Modul pokladny</span><span class="sxs-lookup"><span data-stu-id="39663-188">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="39663-189">Modul potvrzení objednávky</span><span class="sxs-lookup"><span data-stu-id="39663-189">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="39663-190">Modul záhlaví</span><span class="sxs-lookup"><span data-stu-id="39663-190">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="39663-191">Modul zápatí</span><span class="sxs-lookup"><span data-stu-id="39663-191">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="39663-192">Výpočet dostupnosti zásob pro maloobchodní kanály</span><span class="sxs-lookup"><span data-stu-id="39663-192">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
