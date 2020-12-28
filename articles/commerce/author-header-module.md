---
title: Modul záhlaví
description: Toto téma popisuje moduly záhlaví a popisuje, jak vytvořit moduly záhlaví v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 52069af5ca2211473d4a096ad850b5be1290bba1
ms.sourcegitcommit: eee3523be26369aecdb36c0143a6ee3dab4b7966
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/20/2020
ms.locfileid: "4410918"
---
# <a name="header-module"></a><span data-ttu-id="84239-103">Modul záhlaví</span><span class="sxs-lookup"><span data-stu-id="84239-103">Header module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="84239-104">Toto téma popisuje moduly záhlaví a popisuje, jak vytvořit moduly záhlaví v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="84239-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="84239-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="84239-105">Overview</span></span>

<span data-ttu-id="84239-106">V Dynamics 365 Commerce je záhlaví stránky nakonfigurováno jako fragment stránky, který obsahuje moduly záhlaví, propagačního banneru a souhlasu se soubory cookie.</span><span class="sxs-lookup"><span data-stu-id="84239-106">In Dynamics 365 Commerce, a page header is configured as a page fragment that includes the header, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="84239-107">Modul záhlaví obsahuje logo webu, odkazy na navigační hierarchii, odkazy na další stránky na webu, modul ikony košíku, symbol požadovaných položek, přihlašovací možnosti a vyhledávací panel.</span><span class="sxs-lookup"><span data-stu-id="84239-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart icon module, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="84239-108">Modul záhlaví je automaticky optimalizován pro zařízení, na kterém je stránka prohlížena (jinými slovy desktopové nebo mobilní zařízení).</span><span class="sxs-lookup"><span data-stu-id="84239-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="84239-109">Například v mobilním zařízení je navigační panel sbalen do tlačítka **Nabídka** (což je někdy nazýváno *hamburgerová nabídka*).</span><span class="sxs-lookup"><span data-stu-id="84239-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

<span data-ttu-id="84239-110">Následující obrázek znázorňuje příklad modulu záhlaví na domovské stránce.</span><span class="sxs-lookup"><span data-stu-id="84239-110">The following image shows an example of a header module on a home page.</span></span>

![Příklad modulu záhlaví](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a><span data-ttu-id="84239-112">Vlastnosti modulu záhlaví</span><span class="sxs-lookup"><span data-stu-id="84239-112">Properties of a header module</span></span>

<span data-ttu-id="84239-113">Modul záhlaví podporuje vlastnosti **Obrázek loga**, **Odkaz na logo** a **Odkazy na můj účet**.</span><span class="sxs-lookup"><span data-stu-id="84239-113">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="84239-114">Vlastnosti **Obrázek loga** a **Odkaz na logo** se používají k definování loga na stránce.</span><span class="sxs-lookup"><span data-stu-id="84239-114">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="84239-115">Další informace naleznete v tématu [Přidat logo](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="84239-115">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="84239-116">Vlastnost **Odkazy na můj účet** lze použít k definování stránek účtů, pro které chce vlastník webu zobrazit v záhlaví rychlé odkazy.</span><span class="sxs-lookup"><span data-stu-id="84239-116">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-within-a-header-module"></a><span data-ttu-id="84239-117">Moduly, které jsou k dispozici v rámci modulu záhlaví</span><span class="sxs-lookup"><span data-stu-id="84239-117">Modules that are available within a header module</span></span>

<span data-ttu-id="84239-118">Následující moduly lze použít v modulu záhlaví:</span><span class="sxs-lookup"><span data-stu-id="84239-118">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="84239-119">**Navigační nabídka** – Navigační nabídka představuje hierarchii navigace kanálu a další statické navigační odkazy.</span><span class="sxs-lookup"><span data-stu-id="84239-119">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="84239-120">Další informace naleznete v tématu [Modul navigační nabídky](nav-menu-module.md).</span><span class="sxs-lookup"><span data-stu-id="84239-120">For more information, see [Navigation menu module](nav-menu-module.md).</span></span>

- <span data-ttu-id="84239-121">**Vyhledávání** – Vyhledávací modul umožňuje uživatelům zadat hledané termíny, aby mohli vyhledávat produkty.</span><span class="sxs-lookup"><span data-stu-id="84239-121">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="84239-122">Adresa URL výchozí stránky pro vyhledávání a parametry vyhledávacího dotazu musí být zadány v **Nastavení webu \> Rozšíření**.</span><span class="sxs-lookup"><span data-stu-id="84239-122">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="84239-123">Modul vyhledávání obsahuje vlastnosti, které umožňují potlačit tlačítko hledání nebo popis podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="84239-123">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="84239-124">Modul vyhledávání také podporuje možnosti automatického navrhování, například výsledky hledání produktů, klíčových slov a kategorií.</span><span class="sxs-lookup"><span data-stu-id="84239-124">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

- <span data-ttu-id="84239-125">**Ikona košíku** – ikona košíku představuje ikonu nákupního košíku, která zobrazuje počet položek v košíku v kterémkoli daném okamžiku.</span><span class="sxs-lookup"><span data-stu-id="84239-125">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="84239-126">Další informace naleznete v tématu [Modul s ikonou košíku](cart-icon-module.md).</span><span class="sxs-lookup"><span data-stu-id="84239-126">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

- <span data-ttu-id="84239-127">**Selektor webu** - Modul pro výběr webů umožňuje uživatelům procházet různé předdefinované weby na základě trhu, regionů a národních prostředí.</span><span class="sxs-lookup"><span data-stu-id="84239-127">**Site selector** - The site selector module lets users browse across different predefined sites, based on market, regions, and locales.</span></span> <span data-ttu-id="84239-128">Další informace naleznete v tématu [Modul pro výběr webu](site-selector.md).</span><span class="sxs-lookup"><span data-stu-id="84239-128">For more information, see [Site selector module](site-selector.md).</span></span>

- <span data-ttu-id="84239-129">**Výběr obchodu** - Modul pro výběr obchodu lze zahrnout do slotu pro výběr obchodu v modulu záhlaví.</span><span class="sxs-lookup"><span data-stu-id="84239-129">**Store selector** - The store selector module can be included in a header module's store selector slot.</span></span> <span data-ttu-id="84239-130">Umožňuje uživatelům procházet a vyhledávat obchody v okolí.</span><span class="sxs-lookup"><span data-stu-id="84239-130">It lets users browse and find nearby stores.</span></span> <span data-ttu-id="84239-131">Uživatelé mohou také určit preferovaný obchod.</span><span class="sxs-lookup"><span data-stu-id="84239-131">Users can also specify a preferred store.</span></span> <span data-ttu-id="84239-132">Tento obchod se poté zobrazí v záhlaví.</span><span class="sxs-lookup"><span data-stu-id="84239-132">That store will then be shown in the header.</span></span> <span data-ttu-id="84239-133">Když je modul pro výběr obchodu zahrnut v modulu záhlaví, jeho vlastnost **Režim** musí být nastavena na **Najít obchody**.</span><span class="sxs-lookup"><span data-stu-id="84239-133">When the store selector module is included in the header module, its **Mode** property must be set to **Find stores**.</span></span> <span data-ttu-id="84239-134">Další informace naleznete v tématu [Modul pro výběr obchodu](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="84239-134">For more information, see [Store selector module](store-selector.md).</span></span>

> [!NOTE]
> - <span data-ttu-id="84239-135">Podpora pro použití modulu ikony košíku v modulech záhlaví je k dispozici v Dynamics 365 Commerce vydání 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="84239-135">Support for using the cart icon module in header modules is available in the Dynamics 365 Commerce 10.0.11 release.</span></span>
> - <span data-ttu-id="84239-136">Podpora pro použití modulu výběru webu v modulech záhlaví je k dispozici v Dynamics 365 Commerce vydání 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="84239-136">Support for using the site selector module in header modules is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>
> - <span data-ttu-id="84239-137">Podpora pro použití modulu výběru obchodu v modulech záhlaví je k dispozici v Dynamics 365 Commerce vydání 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="84239-137">Support for using the store selector module in header modules is available in the Dynamics 365 Commerce 10.0.15 release.</span></span>

## <a name="create-a-header-fragment-for-a-page"></a><span data-ttu-id="84239-138">Vytvoření fragmentu záhlaví stránky</span><span class="sxs-lookup"><span data-stu-id="84239-138">Create a header fragment for a page</span></span>

<span data-ttu-id="84239-139">Chcete-li vytvořit fragment záhlaví, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="84239-139">To create a header fragment, follow these steps.</span></span>

1. <span data-ttu-id="84239-140">Přejděte na **Fragmenty** a volbou **Nový** vytvořte nový fragment.</span><span class="sxs-lookup"><span data-stu-id="84239-140">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="84239-141">V dialogovém okně **Nový fragment** vyberte modul **Kontejner**, zadejte název fragmentu a poté klepněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="84239-141">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="84239-142">Vyberte pozici **Výchozí kontejner** a poté v podokně vlastností napravo nastavte vlastnost **Šířka** na **Vyplnit obrazovku**.</span><span class="sxs-lookup"><span data-stu-id="84239-142">Select the **Default container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill Screen**.</span></span>
1. <span data-ttu-id="84239-143">V pozici **Výchozí kontejner** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="84239-143">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="84239-144">V dialogovém okně **Přidat modul** vyberte moduly **Souhlas se soubory cookie**, **Záhlaví** a **Propagační banner** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="84239-144">In the **Add Module** dialog box, select the **Cookie consent**, **Header**, and **Promo banner** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="84239-145">V podokně vlastností modulu **Propagační banner** vyberte **Přidat zprávu** a potom vyberte **Zpráva**.</span><span class="sxs-lookup"><span data-stu-id="84239-145">In the properties pane of the **Promo banner** module, select **Add Message**, and then select **Message**.</span></span>
1. <span data-ttu-id="84239-146">V dialogovém okně **Zpráva** přidejte text a odkazy na propagační obsah a poté vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="84239-146">In the **Message** dialog box, add text and links for the promotional content, and then select **OK**.</span></span>
1. <span data-ttu-id="84239-147">V podokně vlastností modulu **Souhlas se soubory cookie** přidejte a nakonfigurujte text a odkaz na stránku ochrany osobních údajů webu.</span><span class="sxs-lookup"><span data-stu-id="84239-147">In the properties pane of the **Cookie consent** module, add and configure text and a link to the site privacy page.</span></span>
1. <span data-ttu-id="84239-148">V pozici **Navigační nabídka** modulu záhlaví vyberte tři tečky (**...**) a poté vyberte **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="84239-148">In the **Navigation menu** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="84239-149">V dialogovém okně **Přidat modul** vyberte modul **Navigační nabídka** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="84239-149">In the **Add Module** dialog box, select the **Navigation menu** module, and then select **OK**.</span></span>
1. <span data-ttu-id="84239-150">V podokně vlastností modulu navigační nabídky v části **Zdroj pro navigační nabídku** vyberte **Server maloobchodu**.</span><span class="sxs-lookup"><span data-stu-id="84239-150">In the property pane for the navigation menu module, under **Source for navigation menu**, select **Retail Server**.</span></span>
1. <span data-ttu-id="84239-151">V podokně vlastností modulu navigační nabídky v části **Statické položky nabídky** vyberte **Přidat položku nabídky** a potom vyberte **Položka nabídky**.</span><span class="sxs-lookup"><span data-stu-id="84239-151">In the property pane for the navigation menu module, under **Static menu items**, select **Add Menu item**, and then select **Menu item**.</span></span> 
1. <span data-ttu-id="84239-152">V dialogovém okně **Položka nabídky** v části **Text položky nabídky** zadejte „Kontakt“.</span><span class="sxs-lookup"><span data-stu-id="84239-152">In the **Menu item** dialog box, under **Menu Item Text** enter "Contact."</span></span>
1. <span data-ttu-id="84239-153">V dialogovém okně **Položka nabídky** v části **Cíl odkazu na položku nabídky** vyberte **Přidat odkaz**.</span><span class="sxs-lookup"><span data-stu-id="84239-153">In the **Menu item** dialog box, under **Menu Item Link target** select **Add a link**.</span></span>
1. <span data-ttu-id="84239-154">V dialogovém okně **Přidat odkaz** vyberte adresu URL pro stránku „Kontakt“ na webu a vyberte tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="84239-154">In the **Add a link** dialog box, select the URL for the site's "Contact" page, and then select **OK**.</span></span>  
1. <span data-ttu-id="84239-155">V dialogovém okně **Položka nabídky** vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="84239-155">In the **Menu item** dialog box, select **OK**.</span></span>
1. <span data-ttu-id="84239-156">V pozici **Vyhledávání** modulu záhlaví vyberte tři tečky (**...**) a poté vyberte **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="84239-156">In the **Search** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="84239-157">V dialogovém okně **Přidat modul** vyberte modul **Vyhledávání** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="84239-157">In the **Add Module** dialog box, select the **Search** module, and then select **OK**.</span></span>
1. <span data-ttu-id="84239-158">V podokně vlastností modulu vyhledávání dle potřeby nakonfigurujte vlastnosti.</span><span class="sxs-lookup"><span data-stu-id="84239-158">In the property pane for the search module, configure the properties as needed.</span></span>
1. <span data-ttu-id="84239-159">V pozici **Ikona nákupního košíku** modulu záhlaví vyberte tři tečky (**...**) a poté vyberte **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="84239-159">In the **Cart icon** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="84239-160">V dialogovém okně **Přidat modul** vyberte modul **Ikona nákupního košíku** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="84239-160">In the **Add Module** dialog box, select the **Cart icon** module, and then select **OK**.</span></span>
1. <span data-ttu-id="84239-161">V podokně vlastností modulu ikony nákupního košíku dle potřeby nakonfigurujte vlastnosti.</span><span class="sxs-lookup"><span data-stu-id="84239-161">In the property pane for the cart icon module, configure the properties as needed.</span></span> <span data-ttu-id="84239-162">Pokud chcete, aby ikona nákupního košíku zobrazovala souhrn nákupního košíku (označovaný také jako mini košík), když na ni uživatelé umístí kurzor myši, vyberte **Zobrazit mini košík**.</span><span class="sxs-lookup"><span data-stu-id="84239-162">If you want the cart icon to display a cart summary (also known as a mini cart) when users hover over it, select **Show mini cart**.</span></span>
1. <span data-ttu-id="84239-163">Chcete-li vrátit fragment se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** jej publikujte.</span><span class="sxs-lookup"><span data-stu-id="84239-163">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="84239-164">Chcete-li zajistit, aby se záhlaví zobrazilo na každé stránce, postupujte podle následujících kroků pro všechny šablony stránek, které jsou pro daný web vytvořeny.</span><span class="sxs-lookup"><span data-stu-id="84239-164">To help ensure that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="84239-165">V pozici **Záhlaví** modulu **Výchozí stránka** přidejte fragment zápatí, který jste vytvořili.</span><span class="sxs-lookup"><span data-stu-id="84239-165">In the **Header** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="84239-166">Chcete-li vrátit šablonu se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="84239-166">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="84239-167">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="84239-167">Additional resources</span></span>

[<span data-ttu-id="84239-168">Přehled knihovny modulů</span><span class="sxs-lookup"><span data-stu-id="84239-168">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="84239-169">Modul kontejneru</span><span class="sxs-lookup"><span data-stu-id="84239-169">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="84239-170">Modul ikony košíku</span><span class="sxs-lookup"><span data-stu-id="84239-170">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="84239-171">Modul propagačního banneru</span><span class="sxs-lookup"><span data-stu-id="84239-171">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="84239-172">Modul navigační nabídky</span><span class="sxs-lookup"><span data-stu-id="84239-172">Navigation Menu module</span></span>](nav-menu-module.md) 

[<span data-ttu-id="84239-173">Souhlas se soubory cookie</span><span class="sxs-lookup"><span data-stu-id="84239-173">Cookie consent</span></span>](cookie-consent-module.md)

[<span data-ttu-id="84239-174">Modul zápatí</span><span class="sxs-lookup"><span data-stu-id="84239-174">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="84239-175">Modul volby webu</span><span class="sxs-lookup"><span data-stu-id="84239-175">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="84239-176">Modul volby obchodu</span><span class="sxs-lookup"><span data-stu-id="84239-176">Store selector module</span></span>](store-selector.md)
