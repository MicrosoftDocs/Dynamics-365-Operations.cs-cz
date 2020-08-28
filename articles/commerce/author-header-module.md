---
title: Modul záhlaví
description: Toto téma popisuje moduly záhlaví a popisuje, jak vytvořit moduly záhlaví v řešení Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: e7dde3ba1ad375b309ae66cc6d31ccad85615e45
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686615"
---
# <a name="header-module"></a><span data-ttu-id="d6bd0-103">Modul záhlaví</span><span class="sxs-lookup"><span data-stu-id="d6bd0-103">Header module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d6bd0-104">Toto téma popisuje moduly záhlaví a popisuje, jak vytvořit moduly záhlaví v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d6bd0-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d6bd0-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="d6bd0-105">Overview</span></span>

<span data-ttu-id="d6bd0-106">V aplikaci Dynamics 365 Commerce se záhlaví stránky skládá z několika modulů, jako je například záhlaví, navigační nabídka, hledání, reklamní banner a moduly souhlasu se soubory cookie.</span><span class="sxs-lookup"><span data-stu-id="d6bd0-106">In Dynamics 365 Commerce, a page header comprises multiple modules, such as the header, navigation menu, search, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="d6bd0-107">Modul záhlaví obsahuje logo webu, odkazy na navigační hierarchii, odkazy na další stránky na webu, symbol košíku, symbol požadovaných položek, přihlašovací možnosti a vyhledávací panel.</span><span class="sxs-lookup"><span data-stu-id="d6bd0-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart symbol, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="d6bd0-108">Modul záhlaví je automaticky optimalizován pro zařízení, na kterém je stránka prohlížena (jinými slovy desktopové nebo mobilní zařízení).</span><span class="sxs-lookup"><span data-stu-id="d6bd0-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="d6bd0-109">Například v mobilním zařízení je navigační panel sbalen do tlačítka **Nabídka** (což je někdy nazýváno *hamburgerová nabídka*).</span><span class="sxs-lookup"><span data-stu-id="d6bd0-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

<span data-ttu-id="d6bd0-110">Následující obrázek znázorňuje příklad modulu záhlaví na domovské stránce.</span><span class="sxs-lookup"><span data-stu-id="d6bd0-110">The following image shows an example of a header module on a home page.</span></span>

![Příklad modulu záhlaví](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a><span data-ttu-id="d6bd0-112">Vlastnosti modulu záhlaví</span><span class="sxs-lookup"><span data-stu-id="d6bd0-112">Properties of a header module</span></span>

<span data-ttu-id="d6bd0-113">Modul záhlaví podporuje vlastnosti **Obrázek loga**, **Odkaz na logo** a **Odkazy na můj účet**.</span><span class="sxs-lookup"><span data-stu-id="d6bd0-113">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="d6bd0-114">Vlastnosti **Obrázek loga** a **Odkaz na logo** se používají k definování loga na stránce.</span><span class="sxs-lookup"><span data-stu-id="d6bd0-114">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="d6bd0-115">Další informace naleznete v tématu [Přidat logo](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="d6bd0-115">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="d6bd0-116">Vlastnost **Odkazy na můj účet** lze použít k definování stránek účtů, pro které chce vlastník webu zobrazit v záhlaví rychlé odkazy.</span><span class="sxs-lookup"><span data-stu-id="d6bd0-116">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="d6bd0-117">Moduly, které jsou k dispozici v modulu záhlaví</span><span class="sxs-lookup"><span data-stu-id="d6bd0-117">Modules that are available in a header module</span></span>

<span data-ttu-id="d6bd0-118">Následující moduly lze použít v modulu záhlaví:</span><span class="sxs-lookup"><span data-stu-id="d6bd0-118">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="d6bd0-119">**Navigační nabídka** – Navigační nabídka představuje hierarchii navigace kanálu a další statické navigační odkazy.</span><span class="sxs-lookup"><span data-stu-id="d6bd0-119">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="d6bd0-120">Hierarchii navigace kanálu lze nakonfigurovat v aplikaci Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d6bd0-120">The channel navigation hierarchy can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="d6bd0-121">Navigační nabídka obsahuje vlastnost **Zdroj navigace**, která se používá k určení položek navigační nabídky serveru Retail a statických položek nabídky jako zdroje.</span><span class="sxs-lookup"><span data-stu-id="d6bd0-121">The navigation menu has a **Navigation Source** property that is used to specify Retail Server navigation menu items and static menu items as a source.</span></span> <span data-ttu-id="d6bd0-122">Jsou-li statické položky nabídky určeny jako zdroj, lze poskytnout relativní odkazy na jiné stránky na webu.</span><span class="sxs-lookup"><span data-stu-id="d6bd0-122">If static menu items are specified as a source, relative links to other pages on the site can be provided.</span></span> <span data-ttu-id="d6bd0-123">Konfigurované položky jsou pak zobrazeny jako navigace v záhlaví.</span><span class="sxs-lookup"><span data-stu-id="d6bd0-123">Configured items then appear as header navigation.</span></span> 

- <span data-ttu-id="d6bd0-124">**Vyhledávání** – Vyhledávací modul umožňuje uživatelům zadat hledané termíny, aby mohli vyhledávat produkty.</span><span class="sxs-lookup"><span data-stu-id="d6bd0-124">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="d6bd0-125">Adresa URL výchozí stránky pro vyhledávání a parametry vyhledávacího dotazu musí být zadány v **Nastavení webu \> Rozšíření**.</span><span class="sxs-lookup"><span data-stu-id="d6bd0-125">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="d6bd0-126">Modul vyhledávání obsahuje vlastnosti, které umožňují potlačit tlačítko hledání nebo popis podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="d6bd0-126">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="d6bd0-127">Modul vyhledávání také podporuje možnosti automatického navrhování, například výsledky hledání produktů, klíčových slov a kategorií.</span><span class="sxs-lookup"><span data-stu-id="d6bd0-127">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

- <span data-ttu-id="d6bd0-128">**Ikona košíku** – ikona košíku představuje ikonu nákupního košíku, která zobrazuje počet položek v košíku v kterémkoli daném okamžiku.</span><span class="sxs-lookup"><span data-stu-id="d6bd0-128">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="d6bd0-129">Další informace naleznete v tématu [Modul s ikonou košíku](cart-icon-module.md).</span><span class="sxs-lookup"><span data-stu-id="d6bd0-129">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

## <a name="create-a-header-module-for-a-page"></a><span data-ttu-id="d6bd0-130">Vytvoření modulu záhlaví stránky</span><span class="sxs-lookup"><span data-stu-id="d6bd0-130">Create a header module for a page</span></span>

<span data-ttu-id="d6bd0-131">Chcete-li vytvořit modul záhlaví, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="d6bd0-131">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="d6bd0-132">Přejděte na **Fragmenty** a volbou **Nový** vytvořte nový fragment.</span><span class="sxs-lookup"><span data-stu-id="d6bd0-132">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="d6bd0-133">V dialogovém okně **Nový fragment stránky** vyberte modul **Kontejner**, zadejte název fragmentu stránky a poté klepněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="d6bd0-133">In the **New page fragment** dialog box, select the **Container** module, enter a name for the page fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="d6bd0-134">Vyberte pozici **Výchozí kontejner** a poté v podokně vlastností napravo nastavte vlastnost **Šířka** na **Vyplnit kontejner**.</span><span class="sxs-lookup"><span data-stu-id="d6bd0-134">Select the **Default container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="d6bd0-135">V pozici **Výchozí kontejner** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="d6bd0-135">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d6bd0-136">V dialogovém okně **Přidat modul** vyberte moduly **Propagační banner** a **Souhlas se soubory cookie** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="d6bd0-136">In the **Add Module** dialog box, select the **Promo banner** and **Cookie consent** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="d6bd0-137">V pozici **Výchozí kontejner** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="d6bd0-137">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d6bd0-138">V dialogovém okně **Přidat modul** vyberte modul **Kontejner** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="d6bd0-138">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d6bd0-139">Vyberte pozici **Kontejner** a poté v podokně vlastností napravo nastavte vlastnost **Šířka** na **Vyplnit kontejner**.</span><span class="sxs-lookup"><span data-stu-id="d6bd0-139">Select the **Container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="d6bd0-140">V pozici **Kontejner** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="d6bd0-140">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d6bd0-141">V dialogovém okně **Přidat modul** vyberte modul **Záhlaví** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="d6bd0-141">In the **Add Module** dialog box, select the **Header** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d6bd0-142">V pozici **Navigační nabídka** modulu záhlaví vyberte tři tečky (**...**) a poté vyberte **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="d6bd0-142">In the **Navigation menu** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d6bd0-143">V dialogovém okně **Přidat modul** vyberte modul **Navigační nabídka** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="d6bd0-143">In the **Add Module** dialog box, select the **Navigation menu** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d6bd0-144">V podokně vlastností modulu navigační nabídky dle potřeby nakonfigurujte vlastnosti.</span><span class="sxs-lookup"><span data-stu-id="d6bd0-144">In the property pane for the navigation menu module, configure the properties as needed.</span></span>
1. <span data-ttu-id="d6bd0-145">V pozici **Vyhledávání** modulu záhlaví vyberte tři tečky (**...**) a poté vyberte **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="d6bd0-145">In the **Search** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d6bd0-146">V dialogovém okně **Přidat modul** vyberte modul **Vyhledávání** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="d6bd0-146">In the **Add Module** dialog box, select the **Search** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d6bd0-147">V podokně vlastností modulu vyhledávání dle potřeby nakonfigurujte vlastnosti.</span><span class="sxs-lookup"><span data-stu-id="d6bd0-147">In the property pane for the search module, configure the properties as needed.</span></span>
1. <span data-ttu-id="d6bd0-148">V pozici **Ikona nákupního košíku** modulu záhlaví vyberte tři tečky (**...**) a poté vyberte **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="d6bd0-148">In the **Cart icon** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d6bd0-149">V dialogovém okně **Přidat modul** vyberte modul **Ikona nákupního košíku** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="d6bd0-149">In the **Add Module** dialog box, select the **Cart icon** module, and then select **OK**.</span></span>
1. <span data-ttu-id="d6bd0-150">V podokně vlastností modulu ikony nákupního košíku dle potřeby nakonfigurujte vlastnosti.</span><span class="sxs-lookup"><span data-stu-id="d6bd0-150">In the property pane for the cart icon module, configure the properties as needed.</span></span> <span data-ttu-id="d6bd0-151">Pokud chcete, aby ikona nákupního košíku zobrazovala souhrn nákupního košíku (označovaný také jako mini košík), když na ni uživatelé umístí kurzor myši, vyberte **Zobrazit mini košík**.</span><span class="sxs-lookup"><span data-stu-id="d6bd0-151">If you want the cart icon to display a cart summary (also known as a mini cart) when users hover over it, select **Show mini cart**.</span></span>
1. <span data-ttu-id="d6bd0-152">Chcete-li vrátit fragment se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** jej publikujte.</span><span class="sxs-lookup"><span data-stu-id="d6bd0-152">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="d6bd0-153">Chcete-li zajistit, aby se záhlaví zobrazilo na každé stránce, postupujte podle následujících kroků pro všechny šablony stránek, které jsou pro daný web vytvořeny.</span><span class="sxs-lookup"><span data-stu-id="d6bd0-153">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="d6bd0-154">V pozici **Záhlaví** modulu **Výchozí stránka** přidejte fragment zápatí, který jste vytvořili.</span><span class="sxs-lookup"><span data-stu-id="d6bd0-154">In the **Header** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="d6bd0-155">Chcete-li vrátit šablonu se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="d6bd0-155">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d6bd0-156">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="d6bd0-156">Additional resources</span></span>

[<span data-ttu-id="d6bd0-157">Přehled startovací sady</span><span class="sxs-lookup"><span data-stu-id="d6bd0-157">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="d6bd0-158">Modul kontejneru</span><span class="sxs-lookup"><span data-stu-id="d6bd0-158">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="d6bd0-159">Modul buy boxu</span><span class="sxs-lookup"><span data-stu-id="d6bd0-159">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="d6bd0-160">Modul košíku</span><span class="sxs-lookup"><span data-stu-id="d6bd0-160">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="d6bd0-161">Ikona modulu košíku</span><span class="sxs-lookup"><span data-stu-id="d6bd0-161">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="d6bd0-162">Modul pokladny</span><span class="sxs-lookup"><span data-stu-id="d6bd0-162">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="d6bd0-163">Modul potvrzení objednávky</span><span class="sxs-lookup"><span data-stu-id="d6bd0-163">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="d6bd0-164">Modul záhlaví</span><span class="sxs-lookup"><span data-stu-id="d6bd0-164">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="d6bd0-165">Modul zápatí</span><span class="sxs-lookup"><span data-stu-id="d6bd0-165">Footer module</span></span>](author-footer-module.md)
