---
title: Modul košíku
description: Tohle téma se zabývá moduly košíku a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: f21268ed4cffed1d5c789f722796cdf05e965819
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/27/2020
ms.locfileid: "3621029"
---
# <a name="cart-module"></a><span data-ttu-id="7d18e-103">Modul košíku</span><span class="sxs-lookup"><span data-stu-id="7d18e-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7d18e-104">Tohle téma se zabývá moduly košíku a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7d18e-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="7d18e-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="7d18e-105">Overview</span></span>

<span data-ttu-id="7d18e-106">Modul košíku zobrazuje položky, které byly přidány do košíku, než odběratel pokračuje v rezervaci.</span><span class="sxs-lookup"><span data-stu-id="7d18e-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="7d18e-107">Modul také zobrazuje souhrn objednávky a umožňuje odběrateli použití nebo odebrání propagačních kódů.</span><span class="sxs-lookup"><span data-stu-id="7d18e-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="7d18e-108">Modul košíku podporuje přihlášené uživatele i hosty.</span><span class="sxs-lookup"><span data-stu-id="7d18e-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="7d18e-109">Také podporuje odkaz **Zpět na nákupy**.</span><span class="sxs-lookup"><span data-stu-id="7d18e-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="7d18e-110">Můžete konfigurovat cestu pro tento odkaz v **Nastavení webu \> Rozšíření \> Cesty**.</span><span class="sxs-lookup"><span data-stu-id="7d18e-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="7d18e-111">Modul košíku vykresluje data založená na ID košíku, což je soubor cookie prohlížeče dostupný v rámci celého webu.</span><span class="sxs-lookup"><span data-stu-id="7d18e-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span> 

<span data-ttu-id="7d18e-112">Následující obrázek ukazuje příklad stránky nákupního košíku na webu Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="7d18e-112">The following image shows an example of a cart page on the Fabrikam site.</span></span>

![Příklad modulu nákupního košíku](./media/cart2.PNG)

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="7d18e-114">Vlastnosti a pozice modulu košíku</span><span class="sxs-lookup"><span data-stu-id="7d18e-114">Cart module properties and slots</span></span>

<span data-ttu-id="7d18e-115">Modul košíku má vlastnost **Záhlaví**, kterou lze nastavit na hodnoty, jako je **Nákupní taška** a **Položky v košíku**.</span><span class="sxs-lookup"><span data-stu-id="7d18e-115">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="7d18e-116">Moduly, které lze použít v modulu košíku</span><span class="sxs-lookup"><span data-stu-id="7d18e-116">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="7d18e-117">**Textový blok** – Tento modul podporuje vlastní zasílání zpráv v modulu košíku.</span><span class="sxs-lookup"><span data-stu-id="7d18e-117">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="7d18e-118">Zprávy řídí systém správy obsahu (CMS).</span><span class="sxs-lookup"><span data-stu-id="7d18e-118">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="7d18e-119">Lze přidat libovolnou zprávu, například „Při problémech s objednávkou volejte 123 456 789“.</span><span class="sxs-lookup"><span data-stu-id="7d18e-119">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="7d18e-120">**Volič obchodů** – Tento modul zobrazuje seznam obchodů, které jsou poblíž a kde je položka k výdeji.</span><span class="sxs-lookup"><span data-stu-id="7d18e-120">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="7d18e-121">Umožňuje uživatelům zadat umístění pro hledání obchodů, které jsou v okolí.</span><span class="sxs-lookup"><span data-stu-id="7d18e-121">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="7d18e-122">Další informace o tomto modulu naleznete v tématu [Modul volič obchodů](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="7d18e-122">For more information on this module, see [Store selector module](store-selector.md).</span></span>

## <a name="module-properties"></a><span data-ttu-id="7d18e-123">Vlastnosti modulu</span><span class="sxs-lookup"><span data-stu-id="7d18e-123">Module properties</span></span>

<span data-ttu-id="7d18e-124">Následující nastavení modulu nákupního košíku lze konfigurovat na **Nastavení webu \> Rozšíření**:</span><span class="sxs-lookup"><span data-stu-id="7d18e-124">The following cart module settings can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="7d18e-125">**Maximální množství** – tato vlastnost se používá k určení maximálního počtu jednotlivých položek, které lze přidat do nákupního košíku.</span><span class="sxs-lookup"><span data-stu-id="7d18e-125">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="7d18e-126">Maloobchodní prodejce může například rozhodnout, že v jedné transakci lze prodávat pouze 10 jednotlivých produktů.</span><span class="sxs-lookup"><span data-stu-id="7d18e-126">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="7d18e-127">**Zásoby** – Informace, jak použít nastavení zásob, naleznete v části [Použití nastavení zásob](inventory-settings.md).</span><span class="sxs-lookup"><span data-stu-id="7d18e-127">**Inventory** – For information about how to apply inventory settings, see [Apply inventory settings](inventory-settings.md).</span></span>
- <span data-ttu-id="7d18e-128">**Zpět k nákupu** – Tato vlastnost se používá k určení trasy pro odkaz **Zpět k nákupu**.</span><span class="sxs-lookup"><span data-stu-id="7d18e-128">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="7d18e-129">Postup lze konfigurovat na úrovni webu a umožnit maloobchodním prodejcům, aby se odběratel mohl vrátit na domovskou stránku nebo na jakoukoli jinou stránku na webu.</span><span class="sxs-lookup"><span data-stu-id="7d18e-129">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="7d18e-130">Interakce Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="7d18e-130">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="7d18e-131">Modul košíku načítá informace o produktu pomocí rozhraní API Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="7d18e-131">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="7d18e-132">ID košíku ze souboru cookie prohlížeče se používá k načtení všech informací o produktu z Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="7d18e-132">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="7d18e-133">Přidání modulu košíku na stránku</span><span class="sxs-lookup"><span data-stu-id="7d18e-133">Add a cart module to a page</span></span>

<span data-ttu-id="7d18e-134">Chcete-li přidat modul košíku na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="7d18e-134">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="7d18e-135">Přejděte na **Fragmenty stránky** a volbou **Nový** vytvořte nový fragment.</span><span class="sxs-lookup"><span data-stu-id="7d18e-135">Go to **Page Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="7d18e-136">V dialogovém okně **Nový fragment stránky** vyberte modul **Nákupní košík**.</span><span class="sxs-lookup"><span data-stu-id="7d18e-136">In the **New Page Fragment** dialog box, select the **Cart** module.</span></span>
1. <span data-ttu-id="7d18e-137">V části **Název fragmentu stránky** zadejte název pro **Fragment nákupního košíku** a poté vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="7d18e-137">Under **Page Fragment Name**, enter the name **Cart fragment**, and then select **OK**.</span></span>
1. <span data-ttu-id="7d18e-138">Vyberte pozici **Nákupní košík**.</span><span class="sxs-lookup"><span data-stu-id="7d18e-138">Select the **Cart** slot.</span></span>
1. <span data-ttu-id="7d18e-139">V podokně vlastností vpravo vyberte symbol tužky, do pole zadejte text záhlaví a poté zaškrtněte symbol zaškrtnutí.</span><span class="sxs-lookup"><span data-stu-id="7d18e-139">In the properties pane on the right, select the pencil symbol, enter heading text in the field, and then select the check mark symbol.</span></span>
1. <span data-ttu-id="7d18e-140">V pozici **Nákupní košík** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="7d18e-140">In the **Cart** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="7d18e-141">V dialogovém okně **Přidat modul** vyberte modul **Volba obchodu** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="7d18e-141">In the **Add Module** dialog box, select the **Store selector** module, and then select **OK**.</span></span>
1. <span data-ttu-id="7d18e-142">Chcete-li vrátit fragment se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** jej publikujte.</span><span class="sxs-lookup"><span data-stu-id="7d18e-142">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="7d18e-143">Přejděte na **Šablony** a poté volbou **Nová** vytvořte novou šablonu.</span><span class="sxs-lookup"><span data-stu-id="7d18e-143">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="7d18e-144">V dialogovém okně **Nová šablona** v části **Název šablony** zadejte název šablony.</span><span class="sxs-lookup"><span data-stu-id="7d18e-144">In the **New Template** dialog box, under **Template name**, enter a name for the template.</span></span>
1. <span data-ttu-id="7d18e-145">Ve stromové struktuře vyberte pozici **Obsah**, vyberte tři tečky (**...**) a vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="7d18e-145">In the outline tree, select the **Body** slot, select the ellipsis (**...**), and then select **Add Fragment**.</span></span>
1. <span data-ttu-id="7d18e-146">V dialogovém okně **Vybrat fragment stránky** vyberte **Fragment nákupního košíku** a pak vyberte tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="7d18e-146">In the **Select Page Fragment** dialog box, select the **Cart fragment** fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="7d18e-147">Chcete-li vrátit šablonu se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="7d18e-147">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="7d18e-148">Přejděte na **Stránky** a volbou **Nová** vytvořte novou stránku.</span><span class="sxs-lookup"><span data-stu-id="7d18e-148">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="7d18e-149">V dialogovém okně **Zvolte šablonu** vyberte šablonu, kterou jste vytvořili, zadejte název stránky a pak vyberte tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="7d18e-149">In the **Choose a template** dialog box, select the template that you created, enter a page name, and then select **OK**.</span></span>
1. <span data-ttu-id="7d18e-150">Vyberte možnost **Uložit** a poté vyberte možnost **Náhled**, chcete-li zobrazit náhled stránky.</span><span class="sxs-lookup"><span data-stu-id="7d18e-150">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="7d18e-151">Chcete-li vrátit stránku se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="7d18e-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7d18e-152">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="7d18e-152">Additional resources</span></span>

[<span data-ttu-id="7d18e-153">Přehled startovací sady</span><span class="sxs-lookup"><span data-stu-id="7d18e-153">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="7d18e-154">Modul kontejneru</span><span class="sxs-lookup"><span data-stu-id="7d18e-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="7d18e-155">Modul volby obchodu</span><span class="sxs-lookup"><span data-stu-id="7d18e-155">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="7d18e-156">Modul buy boxu</span><span class="sxs-lookup"><span data-stu-id="7d18e-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="7d18e-157">Ikona modulu košíku</span><span class="sxs-lookup"><span data-stu-id="7d18e-157">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="7d18e-158">Modul pokladny</span><span class="sxs-lookup"><span data-stu-id="7d18e-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="7d18e-159">Modul potvrzení objednávky</span><span class="sxs-lookup"><span data-stu-id="7d18e-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="7d18e-160">Modul záhlaví</span><span class="sxs-lookup"><span data-stu-id="7d18e-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="7d18e-161">Modul zápatí</span><span class="sxs-lookup"><span data-stu-id="7d18e-161">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="7d18e-162">Výpočet dostupnosti zásob pro maloobchodní kanály</span><span class="sxs-lookup"><span data-stu-id="7d18e-162">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
