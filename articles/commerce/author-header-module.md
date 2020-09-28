---
title: Modul záhlaví
description: Toto téma popisuje moduly záhlaví a popisuje, jak vytvořit moduly záhlaví v řešení Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 08/31/2020
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
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: eb440a8fb67888c9411ad5998fead4d00982b436
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761217"
---
# <a name="header-module"></a><span data-ttu-id="db3a0-103">Modul záhlaví</span><span class="sxs-lookup"><span data-stu-id="db3a0-103">Header module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="db3a0-104">Toto téma popisuje moduly záhlaví a popisuje, jak vytvořit moduly záhlaví v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="db3a0-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="db3a0-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="db3a0-105">Overview</span></span>

<span data-ttu-id="db3a0-106">V Dynamics 365 Commerce je záhlaví stránky nakonfigurováno jako fragment stránky, který obsahuje moduly záhlaví, propagačního banneru a souhlasu se soubory cookie.</span><span class="sxs-lookup"><span data-stu-id="db3a0-106">In Dynamics 365 Commerce, a page header is configured as a page fragment that includes the header, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="db3a0-107">Modul záhlaví obsahuje logo webu, odkazy na navigační hierarchii, odkazy na další stránky na webu, modul ikony košíku, symbol požadovaných položek, přihlašovací možnosti a vyhledávací panel.</span><span class="sxs-lookup"><span data-stu-id="db3a0-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart icon module, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="db3a0-108">Modul záhlaví je automaticky optimalizován pro zařízení, na kterém je stránka prohlížena (jinými slovy desktopové nebo mobilní zařízení).</span><span class="sxs-lookup"><span data-stu-id="db3a0-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="db3a0-109">Například v mobilním zařízení je navigační panel sbalen do tlačítka **Nabídka** (což je někdy nazýváno *hamburgerová nabídka*).</span><span class="sxs-lookup"><span data-stu-id="db3a0-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

<span data-ttu-id="db3a0-110">Následující obrázek znázorňuje příklad modulu záhlaví na domovské stránce.</span><span class="sxs-lookup"><span data-stu-id="db3a0-110">The following image shows an example of a header module on a home page.</span></span>

![Příklad modulu záhlaví](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a><span data-ttu-id="db3a0-112">Vlastnosti modulu záhlaví</span><span class="sxs-lookup"><span data-stu-id="db3a0-112">Properties of a header module</span></span>

<span data-ttu-id="db3a0-113">Modul záhlaví podporuje vlastnosti **Obrázek loga**, **Odkaz na logo** a **Odkazy na můj účet**.</span><span class="sxs-lookup"><span data-stu-id="db3a0-113">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="db3a0-114">Vlastnosti **Obrázek loga** a **Odkaz na logo** se používají k definování loga na stránce.</span><span class="sxs-lookup"><span data-stu-id="db3a0-114">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="db3a0-115">Další informace naleznete v tématu [Přidat logo](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="db3a0-115">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="db3a0-116">Vlastnost **Odkazy na můj účet** lze použít k definování stránek účtů, pro které chce vlastník webu zobrazit v záhlaví rychlé odkazy.</span><span class="sxs-lookup"><span data-stu-id="db3a0-116">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-within-a-header-module"></a><span data-ttu-id="db3a0-117">Moduly, které jsou k dispozici v rámci modulu záhlaví</span><span class="sxs-lookup"><span data-stu-id="db3a0-117">Modules that are available within a header module</span></span>

<span data-ttu-id="db3a0-118">Následující moduly lze použít v modulu záhlaví:</span><span class="sxs-lookup"><span data-stu-id="db3a0-118">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="db3a0-119">**Navigační nabídka** – Navigační nabídka představuje hierarchii navigace kanálu a další statické navigační odkazy.</span><span class="sxs-lookup"><span data-stu-id="db3a0-119">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="db3a0-120">Další informace naleznete v tématu [Modul navigační nabídky](nav-menu-module.md).</span><span class="sxs-lookup"><span data-stu-id="db3a0-120">For more information, see [Navigation menu module](nav-menu-module.md).</span></span>

- <span data-ttu-id="db3a0-121">**Vyhledávání** – Vyhledávací modul umožňuje uživatelům zadat hledané termíny, aby mohli vyhledávat produkty.</span><span class="sxs-lookup"><span data-stu-id="db3a0-121">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="db3a0-122">Adresa URL výchozí stránky pro vyhledávání a parametry vyhledávacího dotazu musí být zadány v **Nastavení webu \> Rozšíření**.</span><span class="sxs-lookup"><span data-stu-id="db3a0-122">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="db3a0-123">Modul vyhledávání obsahuje vlastnosti, které umožňují potlačit tlačítko hledání nebo popis podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="db3a0-123">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="db3a0-124">Modul vyhledávání také podporuje možnosti automatického navrhování, například výsledky hledání produktů, klíčových slov a kategorií.</span><span class="sxs-lookup"><span data-stu-id="db3a0-124">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

- <span data-ttu-id="db3a0-125">**Ikona košíku** – ikona košíku představuje ikonu nákupního košíku, která zobrazuje počet položek v košíku v kterémkoli daném okamžiku.</span><span class="sxs-lookup"><span data-stu-id="db3a0-125">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="db3a0-126">Další informace naleznete v tématu [Modul s ikonou košíku](cart-icon-module.md).</span><span class="sxs-lookup"><span data-stu-id="db3a0-126">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

## <a name="create-a-header-fragment-for-a-page"></a><span data-ttu-id="db3a0-127">Vytvoření fragmentu záhlaví stránky</span><span class="sxs-lookup"><span data-stu-id="db3a0-127">Create a header fragment for a page</span></span>

<span data-ttu-id="db3a0-128">Chcete-li vytvořit fragment záhlaví, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="db3a0-128">To create a header fragment, follow these steps.</span></span>

1. <span data-ttu-id="db3a0-129">Přejděte na **Fragmenty** a volbou **Nový** vytvořte nový fragment.</span><span class="sxs-lookup"><span data-stu-id="db3a0-129">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="db3a0-130">V dialogovém okně **Nový fragment** vyberte modul **Kontejner**, zadejte název fragmentu a poté klepněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="db3a0-130">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="db3a0-131">Vyberte pozici **Výchozí kontejner** a poté v podokně vlastností napravo nastavte vlastnost **Šířka** na **Vyplnit obrazovku**.</span><span class="sxs-lookup"><span data-stu-id="db3a0-131">Select the **Default container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill Screen**.</span></span>
1. <span data-ttu-id="db3a0-132">V pozici **Výchozí kontejner** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="db3a0-132">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="db3a0-133">V dialogovém okně **Přidat modul** vyberte moduly **Souhlas se soubory cookie**, **Záhlaví** a **Propagační banner** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="db3a0-133">In the **Add Module** dialog box, select the **Cookie consent**, **Header**, and **Promo banner** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="db3a0-134">V podokně vlastností modulu **Propagační banner** vyberte **Přidat zprávu** a potom vyberte **Zpráva**.</span><span class="sxs-lookup"><span data-stu-id="db3a0-134">In the properties pane of the **Promo banner** module, select **Add Message**, and then select **Message**.</span></span>
1. <span data-ttu-id="db3a0-135">V dialogovém okně **Zpráva** přidejte text a odkazy na propagační obsah a poté vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="db3a0-135">In the **Message** dialog box, add text and links for the promotional content, and then select **OK**.</span></span>
1. <span data-ttu-id="db3a0-136">V podokně vlastností modulu **Souhlas se soubory cookie** přidejte a nakonfigurujte text a odkaz na stránku ochrany osobních údajů webu.</span><span class="sxs-lookup"><span data-stu-id="db3a0-136">In the properties pane of the **Cookie consent** module, add and configure text and a link to the site privacy page.</span></span>
1. <span data-ttu-id="db3a0-137">V pozici **Navigační nabídka** modulu záhlaví vyberte tři tečky (**...**) a poté vyberte **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="db3a0-137">In the **Navigation menu** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="db3a0-138">V dialogovém okně **Přidat modul** vyberte modul **Navigační nabídka** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="db3a0-138">In the **Add Module** dialog box, select the **Navigation menu** module, and then select **OK**.</span></span>
1. <span data-ttu-id="db3a0-139">V podokně vlastností modulu navigační nabídky v části **Zdroj pro navigační nabídku** vyberte **Server maloobchodu**.</span><span class="sxs-lookup"><span data-stu-id="db3a0-139">In the property pane for the navigation menu module, under **Source for navigation menu**, select **Retail Server**.</span></span>
1. <span data-ttu-id="db3a0-140">V podokně vlastností modulu navigační nabídky v části **Statické položky nabídky** vyberte **Přidat položku nabídky** a potom vyberte **Položka nabídky**.</span><span class="sxs-lookup"><span data-stu-id="db3a0-140">In the property pane for the navigation menu module, under **Static menu items**, select **Add Menu item**, and then select **Menu item**.</span></span> 
1. <span data-ttu-id="db3a0-141">V dialogovém okně **Položka nabídky** v části **Text položky nabídky** zadejte „Kontakt“.</span><span class="sxs-lookup"><span data-stu-id="db3a0-141">In the **Menu item** dialog box, under **Menu Item Text** enter "Contact."</span></span>
1. <span data-ttu-id="db3a0-142">V dialogovém okně **Položka nabídky** v části **Cíl odkazu na položku nabídky** vyberte **Přidat odkaz**.</span><span class="sxs-lookup"><span data-stu-id="db3a0-142">In the **Menu item** dialog box, under **Menu Item Link target** select **Add a link**.</span></span>
1. <span data-ttu-id="db3a0-143">V dialogovém okně **Přidat odkaz** vyberte adresu URL pro stránku „Kontakt“ na webu a vyberte tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="db3a0-143">In the **Add a link** dialog box, select the URL for the site's "Contact" page, and then select **OK**.</span></span>  
1. <span data-ttu-id="db3a0-144">V dialogovém okně **Položka nabídky** vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="db3a0-144">In the **Menu item** dialog box, select **OK**.</span></span>
1. <span data-ttu-id="db3a0-145">V pozici **Vyhledávání** modulu záhlaví vyberte tři tečky (**...**) a poté vyberte **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="db3a0-145">In the **Search** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="db3a0-146">V dialogovém okně **Přidat modul** vyberte modul **Vyhledávání** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="db3a0-146">In the **Add Module** dialog box, select the **Search** module, and then select **OK**.</span></span>
1. <span data-ttu-id="db3a0-147">V podokně vlastností modulu vyhledávání dle potřeby nakonfigurujte vlastnosti.</span><span class="sxs-lookup"><span data-stu-id="db3a0-147">In the property pane for the search module, configure the properties as needed.</span></span>
1. <span data-ttu-id="db3a0-148">V pozici **Ikona nákupního košíku** modulu záhlaví vyberte tři tečky (**...**) a poté vyberte **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="db3a0-148">In the **Cart icon** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="db3a0-149">V dialogovém okně **Přidat modul** vyberte modul **Ikona nákupního košíku** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="db3a0-149">In the **Add Module** dialog box, select the **Cart icon** module, and then select **OK**.</span></span>
1. <span data-ttu-id="db3a0-150">V podokně vlastností modulu ikony nákupního košíku dle potřeby nakonfigurujte vlastnosti.</span><span class="sxs-lookup"><span data-stu-id="db3a0-150">In the property pane for the cart icon module, configure the properties as needed.</span></span> <span data-ttu-id="db3a0-151">Pokud chcete, aby ikona nákupního košíku zobrazovala souhrn nákupního košíku (označovaný také jako mini košík), když na ni uživatelé umístí kurzor myši, vyberte **Zobrazit mini košík**.</span><span class="sxs-lookup"><span data-stu-id="db3a0-151">If you want the cart icon to display a cart summary (also known as a mini cart) when users hover over it, select **Show mini cart**.</span></span>
1. <span data-ttu-id="db3a0-152">Chcete-li vrátit fragment se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** jej publikujte.</span><span class="sxs-lookup"><span data-stu-id="db3a0-152">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="db3a0-153">Chcete-li zajistit, aby se záhlaví zobrazilo na každé stránce, postupujte podle následujících kroků pro všechny šablony stránek, které jsou pro daný web vytvořeny.</span><span class="sxs-lookup"><span data-stu-id="db3a0-153">To help ensure that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="db3a0-154">V pozici **Záhlaví** modulu **Výchozí stránka** přidejte fragment zápatí, který jste vytvořili.</span><span class="sxs-lookup"><span data-stu-id="db3a0-154">In the **Header** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="db3a0-155">Chcete-li vrátit šablonu se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="db3a0-155">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="db3a0-156">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="db3a0-156">Additional resources</span></span>

[<span data-ttu-id="db3a0-157">Přehled startovací sady</span><span class="sxs-lookup"><span data-stu-id="db3a0-157">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="db3a0-158">Modul kontejneru</span><span class="sxs-lookup"><span data-stu-id="db3a0-158">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="db3a0-159">Modul ikony košíku</span><span class="sxs-lookup"><span data-stu-id="db3a0-159">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="db3a0-160">Modul propagačního banneru</span><span class="sxs-lookup"><span data-stu-id="db3a0-160">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="db3a0-161">Modul navigační nabídky</span><span class="sxs-lookup"><span data-stu-id="db3a0-161">Navigation Menu module</span></span>](nav-menu-module.md) 

[<span data-ttu-id="db3a0-162">Souhlas se soubory cookie</span><span class="sxs-lookup"><span data-stu-id="db3a0-162">Cookie consent</span></span>](cookie-consent-module.md)

[<span data-ttu-id="db3a0-163">Modul zápatí</span><span class="sxs-lookup"><span data-stu-id="db3a0-163">Footer module</span></span>](author-footer-module.md)
