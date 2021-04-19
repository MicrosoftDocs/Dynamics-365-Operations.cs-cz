---
title: Modul záhlaví
description: Toto téma popisuje moduly záhlaví a popisuje, jak vytvořit moduly záhlaví v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6b14178431b281daa827749781dd16481f8bfb74
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799897"
---
# <a name="header-module"></a><span data-ttu-id="2d53b-103">Modul záhlaví</span><span class="sxs-lookup"><span data-stu-id="2d53b-103">Header module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2d53b-104">Toto téma popisuje moduly záhlaví a popisuje, jak vytvořit moduly záhlaví v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2d53b-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="2d53b-105">V Dynamics 365 Commerce je záhlaví stránky nakonfigurováno jako fragment stránky, který obsahuje moduly záhlaví, propagačního banneru a souhlasu se soubory cookie.</span><span class="sxs-lookup"><span data-stu-id="2d53b-105">In Dynamics 365 Commerce, a page header is configured as a page fragment that includes the header, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="2d53b-106">Modul záhlaví obsahuje logo webu, odkazy na navigační hierarchii, odkazy na další stránky na webu, modul ikony košíku, symbol požadovaných položek, přihlašovací možnosti a vyhledávací panel.</span><span class="sxs-lookup"><span data-stu-id="2d53b-106">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart icon module, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="2d53b-107">Modul záhlaví je automaticky optimalizován pro zařízení, na kterém je stránka prohlížena (jinými slovy desktopové nebo mobilní zařízení).</span><span class="sxs-lookup"><span data-stu-id="2d53b-107">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="2d53b-108">Například v mobilním zařízení je navigační panel sbalen do tlačítka **Nabídka** (což je někdy nazýváno *hamburgerová nabídka*).</span><span class="sxs-lookup"><span data-stu-id="2d53b-108">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

<span data-ttu-id="2d53b-109">Následující obrázek znázorňuje příklad modulu záhlaví na domovské stránce.</span><span class="sxs-lookup"><span data-stu-id="2d53b-109">The following image shows an example of a header module on a home page.</span></span>

![Příklad modulu záhlaví](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a><span data-ttu-id="2d53b-111">Vlastnosti modulu záhlaví</span><span class="sxs-lookup"><span data-stu-id="2d53b-111">Properties of a header module</span></span>

<span data-ttu-id="2d53b-112">Modul záhlaví podporuje vlastnosti **Obrázek loga**, **Odkaz na logo** a **Odkazy na můj účet**.</span><span class="sxs-lookup"><span data-stu-id="2d53b-112">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="2d53b-113">Vlastnosti **Obrázek loga** a **Odkaz na logo** se používají k definování loga na stránce.</span><span class="sxs-lookup"><span data-stu-id="2d53b-113">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="2d53b-114">Další informace naleznete v tématu [Přidat logo](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="2d53b-114">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="2d53b-115">Vlastnost **Odkazy na můj účet** lze použít k definování stránek účtů, pro které chce vlastník webu zobrazit v záhlaví rychlé odkazy.</span><span class="sxs-lookup"><span data-stu-id="2d53b-115">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-within-a-header-module"></a><span data-ttu-id="2d53b-116">Moduly, které jsou k dispozici v rámci modulu záhlaví</span><span class="sxs-lookup"><span data-stu-id="2d53b-116">Modules that are available within a header module</span></span>

<span data-ttu-id="2d53b-117">Následující moduly lze použít v modulu záhlaví:</span><span class="sxs-lookup"><span data-stu-id="2d53b-117">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="2d53b-118">**Navigační nabídka** – Navigační nabídka představuje hierarchii navigace kanálu a další statické navigační odkazy.</span><span class="sxs-lookup"><span data-stu-id="2d53b-118">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="2d53b-119">Další informace naleznete v tématu [Modul navigační nabídky](nav-menu-module.md).</span><span class="sxs-lookup"><span data-stu-id="2d53b-119">For more information, see [Navigation menu module](nav-menu-module.md).</span></span>

- <span data-ttu-id="2d53b-120">**Vyhledávání** – Vyhledávací modul umožňuje uživatelům zadat hledané termíny, aby mohli vyhledávat produkty.</span><span class="sxs-lookup"><span data-stu-id="2d53b-120">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="2d53b-121">Adresa URL výchozí stránky pro vyhledávání a parametry vyhledávacího dotazu musí být zadány v **Nastavení webu \> Rozšíření**.</span><span class="sxs-lookup"><span data-stu-id="2d53b-121">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="2d53b-122">Modul vyhledávání obsahuje vlastnosti, které umožňují potlačit tlačítko hledání nebo popis podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="2d53b-122">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="2d53b-123">Modul vyhledávání také podporuje možnosti automatického navrhování, například výsledky hledání produktů, klíčových slov a kategorií.</span><span class="sxs-lookup"><span data-stu-id="2d53b-123">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

- <span data-ttu-id="2d53b-124">**Ikona košíku** – ikona košíku představuje ikonu nákupního košíku, která zobrazuje počet položek v košíku v kterémkoli daném okamžiku.</span><span class="sxs-lookup"><span data-stu-id="2d53b-124">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="2d53b-125">Další informace naleznete v tématu [Modul s ikonou košíku](cart-icon-module.md).</span><span class="sxs-lookup"><span data-stu-id="2d53b-125">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

- <span data-ttu-id="2d53b-126">**Selektor webu** - Modul pro výběr webů umožňuje uživatelům procházet různé předdefinované weby na základě trhu, regionů a národních prostředí.</span><span class="sxs-lookup"><span data-stu-id="2d53b-126">**Site selector** - The site selector module lets users browse across different predefined sites, based on market, regions, and locales.</span></span> <span data-ttu-id="2d53b-127">Další informace naleznete v tématu [Modul pro výběr webu](site-selector.md).</span><span class="sxs-lookup"><span data-stu-id="2d53b-127">For more information, see [Site selector module](site-selector.md).</span></span>

- <span data-ttu-id="2d53b-128">**Výběr obchodu** - Modul pro výběr obchodu lze zahrnout do slotu pro výběr obchodu v modulu záhlaví.</span><span class="sxs-lookup"><span data-stu-id="2d53b-128">**Store selector** - The store selector module can be included in a header module's store selector slot.</span></span> <span data-ttu-id="2d53b-129">Umožňuje uživatelům procházet a vyhledávat obchody v okolí.</span><span class="sxs-lookup"><span data-stu-id="2d53b-129">It lets users browse and find nearby stores.</span></span> <span data-ttu-id="2d53b-130">Uživatelé mohou také určit preferovaný obchod.</span><span class="sxs-lookup"><span data-stu-id="2d53b-130">Users can also specify a preferred store.</span></span> <span data-ttu-id="2d53b-131">Tento obchod se poté zobrazí v záhlaví.</span><span class="sxs-lookup"><span data-stu-id="2d53b-131">That store will then be shown in the header.</span></span> <span data-ttu-id="2d53b-132">Když je modul pro výběr obchodu zahrnut v modulu záhlaví, jeho vlastnost **Režim** musí být nastavena na **Najít obchody**.</span><span class="sxs-lookup"><span data-stu-id="2d53b-132">When the store selector module is included in the header module, its **Mode** property must be set to **Find stores**.</span></span> <span data-ttu-id="2d53b-133">Další informace naleznete v tématu [Modul pro výběr obchodu](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="2d53b-133">For more information, see [Store selector module](store-selector.md).</span></span>

> [!NOTE]
> - <span data-ttu-id="2d53b-134">Podpora pro použití modulu ikony košíku v modulech záhlaví je k dispozici v Dynamics 365 Commerce vydání 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="2d53b-134">Support for using the cart icon module in header modules is available in the Dynamics 365 Commerce 10.0.11 release.</span></span>
> - <span data-ttu-id="2d53b-135">Podpora pro použití modulu výběru webu v modulech záhlaví je k dispozici v Dynamics 365 Commerce vydání 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="2d53b-135">Support for using the site selector module in header modules is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>
> - <span data-ttu-id="2d53b-136">Podpora pro použití modulu výběru obchodu v modulech záhlaví je k dispozici v Dynamics 365 Commerce vydání 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="2d53b-136">Support for using the store selector module in header modules is available in the Dynamics 365 Commerce 10.0.15 release.</span></span>

## <a name="create-a-header-fragment-for-a-page"></a><span data-ttu-id="2d53b-137">Vytvoření fragmentu záhlaví stránky</span><span class="sxs-lookup"><span data-stu-id="2d53b-137">Create a header fragment for a page</span></span>

<span data-ttu-id="2d53b-138">Chcete-li vytvořit fragment záhlaví, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="2d53b-138">To create a header fragment, follow these steps.</span></span>

1. <span data-ttu-id="2d53b-139">Přejděte na **Fragmenty** a volbou **Nový** vytvořte nový fragment.</span><span class="sxs-lookup"><span data-stu-id="2d53b-139">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="2d53b-140">V dialogovém okně **Nový fragment** vyberte modul **Kontejner**, zadejte název fragmentu a poté klepněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="2d53b-140">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="2d53b-141">Vyberte pozici **Výchozí kontejner** a poté v podokně vlastností napravo nastavte vlastnost **Šířka** na **Vyplnit obrazovku**.</span><span class="sxs-lookup"><span data-stu-id="2d53b-141">Select the **Default container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill Screen**.</span></span>
1. <span data-ttu-id="2d53b-142">V pozici **Výchozí kontejner** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="2d53b-142">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2d53b-143">V dialogovém okně **Přidat modul** vyberte moduly **Souhlas se soubory cookie**, **Záhlaví** a **Propagační banner** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="2d53b-143">In the **Add Module** dialog box, select the **Cookie consent**, **Header**, and **Promo banner** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="2d53b-144">V podokně vlastností modulu **Propagační banner** vyberte **Přidat zprávu** a potom vyberte **Zpráva**.</span><span class="sxs-lookup"><span data-stu-id="2d53b-144">In the properties pane of the **Promo banner** module, select **Add Message**, and then select **Message**.</span></span>
1. <span data-ttu-id="2d53b-145">V dialogovém okně **Zpráva** přidejte text a odkazy na propagační obsah a poté vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="2d53b-145">In the **Message** dialog box, add text and links for the promotional content, and then select **OK**.</span></span>
1. <span data-ttu-id="2d53b-146">V podokně vlastností modulu **Souhlas se soubory cookie** přidejte a nakonfigurujte text a odkaz na stránku ochrany osobních údajů webu.</span><span class="sxs-lookup"><span data-stu-id="2d53b-146">In the properties pane of the **Cookie consent** module, add and configure text and a link to the site privacy page.</span></span>
1. <span data-ttu-id="2d53b-147">V pozici **Navigační nabídka** modulu záhlaví vyberte tři tečky (**...**) a poté vyberte **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="2d53b-147">In the **Navigation menu** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2d53b-148">V dialogovém okně **Přidat modul** vyberte modul **Navigační nabídka** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="2d53b-148">In the **Add Module** dialog box, select the **Navigation menu** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2d53b-149">V podokně vlastností modulu navigační nabídky v části **Zdroj pro navigační nabídku** vyberte **Server maloobchodu**.</span><span class="sxs-lookup"><span data-stu-id="2d53b-149">In the property pane for the navigation menu module, under **Source for navigation menu**, select **Retail Server**.</span></span>
1. <span data-ttu-id="2d53b-150">V podokně vlastností modulu navigační nabídky v části **Statické položky nabídky** vyberte **Přidat položku nabídky** a potom vyberte **Položka nabídky**.</span><span class="sxs-lookup"><span data-stu-id="2d53b-150">In the property pane for the navigation menu module, under **Static menu items**, select **Add Menu item**, and then select **Menu item**.</span></span> 
1. <span data-ttu-id="2d53b-151">V dialogovém okně **Položka nabídky** v části **Text položky nabídky** zadejte „Kontakt“.</span><span class="sxs-lookup"><span data-stu-id="2d53b-151">In the **Menu item** dialog box, under **Menu Item Text** enter "Contact."</span></span>
1. <span data-ttu-id="2d53b-152">V dialogovém okně **Položka nabídky** v části **Cíl odkazu na položku nabídky** vyberte **Přidat odkaz**.</span><span class="sxs-lookup"><span data-stu-id="2d53b-152">In the **Menu item** dialog box, under **Menu Item Link target** select **Add a link**.</span></span>
1. <span data-ttu-id="2d53b-153">V dialogovém okně **Přidat odkaz** vyberte adresu URL pro stránku „Kontakt“ na webu a vyberte tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="2d53b-153">In the **Add a link** dialog box, select the URL for the site's "Contact" page, and then select **OK**.</span></span>  
1. <span data-ttu-id="2d53b-154">V dialogovém okně **Položka nabídky** vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="2d53b-154">In the **Menu item** dialog box, select **OK**.</span></span>
1. <span data-ttu-id="2d53b-155">V pozici **Vyhledávání** modulu záhlaví vyberte tři tečky (**...**) a poté vyberte **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="2d53b-155">In the **Search** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2d53b-156">V dialogovém okně **Přidat modul** vyberte modul **Vyhledávání** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="2d53b-156">In the **Add Module** dialog box, select the **Search** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2d53b-157">V podokně vlastností modulu vyhledávání dle potřeby nakonfigurujte vlastnosti.</span><span class="sxs-lookup"><span data-stu-id="2d53b-157">In the property pane for the search module, configure the properties as needed.</span></span>
1. <span data-ttu-id="2d53b-158">V pozici **Ikona nákupního košíku** modulu záhlaví vyberte tři tečky (**...**) a poté vyberte **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="2d53b-158">In the **Cart icon** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="2d53b-159">V dialogovém okně **Přidat modul** vyberte modul **Ikona nákupního košíku** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="2d53b-159">In the **Add Module** dialog box, select the **Cart icon** module, and then select **OK**.</span></span>
1. <span data-ttu-id="2d53b-160">V podokně vlastností modulu ikony nákupního košíku dle potřeby nakonfigurujte vlastnosti.</span><span class="sxs-lookup"><span data-stu-id="2d53b-160">In the property pane for the cart icon module, configure the properties as needed.</span></span> <span data-ttu-id="2d53b-161">Pokud chcete, aby ikona nákupního košíku zobrazovala souhrn nákupního košíku (označovaný také jako mini košík), když na ni uživatelé umístí kurzor myši, vyberte **Zobrazit mini košík**.</span><span class="sxs-lookup"><span data-stu-id="2d53b-161">If you want the cart icon to display a cart summary (also known as a mini cart) when users hover over it, select **Show mini cart**.</span></span>
1. <span data-ttu-id="2d53b-162">Chcete-li vrátit fragment se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** jej publikujte.</span><span class="sxs-lookup"><span data-stu-id="2d53b-162">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="2d53b-163">Chcete-li zajistit, aby se záhlaví zobrazilo na každé stránce, postupujte podle následujících kroků pro všechny šablony stránek, které jsou pro daný web vytvořeny.</span><span class="sxs-lookup"><span data-stu-id="2d53b-163">To help ensure that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="2d53b-164">V pozici **Záhlaví** modulu **Výchozí stránka** přidejte fragment zápatí, který jste vytvořili.</span><span class="sxs-lookup"><span data-stu-id="2d53b-164">In the **Header** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="2d53b-165">Chcete-li vrátit šablonu se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="2d53b-165">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2d53b-166">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="2d53b-166">Additional resources</span></span>

[<span data-ttu-id="2d53b-167">Přehled knihovny modulů</span><span class="sxs-lookup"><span data-stu-id="2d53b-167">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="2d53b-168">Modul kontejneru</span><span class="sxs-lookup"><span data-stu-id="2d53b-168">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="2d53b-169">Modul ikony košíku</span><span class="sxs-lookup"><span data-stu-id="2d53b-169">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="2d53b-170">Modul propagačního banneru</span><span class="sxs-lookup"><span data-stu-id="2d53b-170">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="2d53b-171">Modul navigační nabídky</span><span class="sxs-lookup"><span data-stu-id="2d53b-171">Navigation Menu module</span></span>](nav-menu-module.md) 

[<span data-ttu-id="2d53b-172">Souhlas se soubory cookie</span><span class="sxs-lookup"><span data-stu-id="2d53b-172">Cookie consent</span></span>](cookie-consent-module.md)

[<span data-ttu-id="2d53b-173">Modul zápatí</span><span class="sxs-lookup"><span data-stu-id="2d53b-173">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="2d53b-174">Modul volby webu</span><span class="sxs-lookup"><span data-stu-id="2d53b-174">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="2d53b-175">Modul volby obchodu</span><span class="sxs-lookup"><span data-stu-id="2d53b-175">Store selector module</span></span>](store-selector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]