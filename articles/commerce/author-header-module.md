---
title: Modul záhlaví
description: Toto téma popisuje moduly záhlaví a popisuje, jak vytvořit moduly záhlaví v řešení Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 04/13/2020
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
ms.openlocfilehash: cec138ebefbd2beb2f1cf6302ce58d8bbc5c4bbd
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261437"
---
# <a name="header-module"></a><span data-ttu-id="2d574-103">Modul záhlaví</span><span class="sxs-lookup"><span data-stu-id="2d574-103">Header module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="2d574-104">Toto téma popisuje moduly záhlaví a popisuje, jak vytvořit moduly záhlaví v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2d574-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2d574-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="2d574-105">Overview</span></span>

<span data-ttu-id="2d574-106">V aplikaci Dynamics 365 Commerce se záhlaví stránky skládá z několika modulů, jako je například záhlaví, navigační nabídka, hledání, reklamní banner a moduly souhlasu se soubory cookie.</span><span class="sxs-lookup"><span data-stu-id="2d574-106">In Dynamics 365 Commerce, a page header comprises multiple modules, such as the header, navigation menu, search, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="2d574-107">Modul záhlaví obsahuje logo webu, odkazy na navigační hierarchii, odkazy na další stránky na webu, symbol košíku, symbol požadovaných položek, přihlašovací možnosti a vyhledávací panel.</span><span class="sxs-lookup"><span data-stu-id="2d574-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart symbol, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="2d574-108">Modul záhlaví je automaticky optimalizován pro zařízení, na kterém je stránka prohlížena (jinými slovy desktopové nebo mobilní zařízení).</span><span class="sxs-lookup"><span data-stu-id="2d574-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="2d574-109">Například v mobilním zařízení je navigační panel sbalen do tlačítka **Nabídka** (což je někdy nazýváno *hamburgerová nabídka*).</span><span class="sxs-lookup"><span data-stu-id="2d574-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header-module"></a><span data-ttu-id="2d574-110">Vlastnosti modulu záhlaví</span><span class="sxs-lookup"><span data-stu-id="2d574-110">Properties of a header module</span></span>

<span data-ttu-id="2d574-111">Modul záhlaví podporuje vlastnosti **Obrázek loga**, **Odkaz na logo** a **Odkazy na můj účet**.</span><span class="sxs-lookup"><span data-stu-id="2d574-111">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="2d574-112">Vlastnosti **Obrázek loga** a **Odkaz na logo** se používají k definování loga na stránce.</span><span class="sxs-lookup"><span data-stu-id="2d574-112">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="2d574-113">Další informace naleznete v tématu [Přidat logo](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="2d574-113">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="2d574-114">Vlastnost **Odkazy na můj účet** lze použít k definování stránek účtů, pro které chce vlastník webu zobrazit v záhlaví rychlé odkazy.</span><span class="sxs-lookup"><span data-stu-id="2d574-114">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="2d574-115">Moduly, které jsou k dispozici v modulu záhlaví</span><span class="sxs-lookup"><span data-stu-id="2d574-115">Modules that are available in a header module</span></span>

<span data-ttu-id="2d574-116">Následující moduly lze použít v modulu záhlaví:</span><span class="sxs-lookup"><span data-stu-id="2d574-116">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="2d574-117">**Navigační nabídka** – Navigační nabídka představuje hierarchii navigace kanálu a další statické navigační odkazy.</span><span class="sxs-lookup"><span data-stu-id="2d574-117">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="2d574-118">Hierarchii navigace kanálu lze nakonfigurovat v aplikaci Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2d574-118">The channel navigation hierarchy can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="2d574-119">Navigační nabídka obsahuje vlastnost **Zdroj navigace**, která se používá k určení položek navigační nabídky serveru Retail a statických položek nabídky jako zdroje.</span><span class="sxs-lookup"><span data-stu-id="2d574-119">The navigation menu has a **Navigation Source** property that is used to specify Retail Server navigation menu items and static menu items as a source.</span></span> <span data-ttu-id="2d574-120">Jsou-li statické položky nabídky určeny jako zdroj, lze poskytnout relativní odkazy na jiné stránky na webu.</span><span class="sxs-lookup"><span data-stu-id="2d574-120">If static menu items are specified as a source, relative links to other pages on the site can be provided.</span></span> <span data-ttu-id="2d574-121">Konfigurované položky jsou pak zobrazeny jako navigace v záhlaví.</span><span class="sxs-lookup"><span data-stu-id="2d574-121">Configured items then appear as header navigation.</span></span> 
- <span data-ttu-id="2d574-122">**Vyhledávání** – Vyhledávací modul umožňuje uživatelům zadat hledané termíny, aby mohli vyhledávat produkty.</span><span class="sxs-lookup"><span data-stu-id="2d574-122">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="2d574-123">Adresa URL výchozí stránky pro vyhledávání a parametry vyhledávacího dotazu musí být zadány v **Nastavení webu \> Rozšíření**.</span><span class="sxs-lookup"><span data-stu-id="2d574-123">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="2d574-124">Modul vyhledávání obsahuje vlastnosti, které umožňují potlačit tlačítko hledání nebo popis podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="2d574-124">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="2d574-125">Modul vyhledávání také podporuje možnosti automatického navrhování, například výsledky hledání produktů, klíčových slov a kategorií.</span><span class="sxs-lookup"><span data-stu-id="2d574-125">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>
- <span data-ttu-id="2d574-126">**Ikona košíku** – ikona košíku představuje ikonu nákupního košíku, která zobrazuje počet položek v košíku v kterémkoli daném okamžiku.</span><span class="sxs-lookup"><span data-stu-id="2d574-126">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="2d574-127">Další informace naleznete v tématu [Modul s ikonou košíku](cart-icon-module.md).</span><span class="sxs-lookup"><span data-stu-id="2d574-127">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

## <a name="create-a-header-module-for-a-page"></a><span data-ttu-id="2d574-128">Vytvoření modulu záhlaví stránky</span><span class="sxs-lookup"><span data-stu-id="2d574-128">Create a header module for a page</span></span>

<span data-ttu-id="2d574-129">Chcete-li vytvořit modul záhlaví, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="2d574-129">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="2d574-130">Vytvořte fragment s názvem **Fragment záhlaví** a do něj přidejte modul kontejneru.</span><span class="sxs-lookup"><span data-stu-id="2d574-130">Create a fragment that is named **Header fragment**, and add a container module to it.</span></span>
1. <span data-ttu-id="2d574-131">V podokně vlastností modulu kontejner nastavte vlastnost **Šířka** na **Vyplnit kontejner**.</span><span class="sxs-lookup"><span data-stu-id="2d574-131">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="2d574-132">Přidejte moduly propagačních bannnerů a souhlas se soubory cookie do modulu kontejneru.</span><span class="sxs-lookup"><span data-stu-id="2d574-132">Add a promo banner and cookie consent modules to the container module.</span></span>
1. <span data-ttu-id="2d574-133">Do fragmentu přidejte další modul kontejneru a nastavte vlastnost **Šířka** na **Vyplnit kontejner**.</span><span class="sxs-lookup"><span data-stu-id="2d574-133">Add another container module to the fragment, and set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="2d574-134">Přidejte modul záhlaví do druhého modulu kontejneru.</span><span class="sxs-lookup"><span data-stu-id="2d574-134">Add a header module to the second container module.</span></span>
1. <span data-ttu-id="2d574-135">Do pozice **Navigační nabídky** modulu záhlaví přidejte modul navigační nabídka.</span><span class="sxs-lookup"><span data-stu-id="2d574-135">In the **Navigation menu** slot of the header module, add a navigation menu module.</span></span> 
1. <span data-ttu-id="2d574-136">V podokně vlastností modulu navigační nabídka konfigurujte vlastnosti modulu navigační nabídka.</span><span class="sxs-lookup"><span data-stu-id="2d574-136">In the property pane for the navigation menu module, configure the properties of the navigation menu module.</span></span>
1. <span data-ttu-id="2d574-137">Do pozice **Vyhledávání** modulu záhlaví přidejte modul vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="2d574-137">In the **Search** slot of the header module, add a search module.</span></span> 
1. <span data-ttu-id="2d574-138">V podokně vlastností modulu vyhledávání konfigurujte vlastnosti modulu vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="2d574-138">In the property pane for the search module, configure the properties of the search module.</span></span> 
1. <span data-ttu-id="2d574-139">Ve slotu **Ikona nákupního košíku** modulu záhlaví přidejte modul ikony vozíku.</span><span class="sxs-lookup"><span data-stu-id="2d574-139">In the **Cart icon** slot of the header module, add a cart icon module.</span></span> 
1. <span data-ttu-id="2d574-140">V podokně vlastností modulu ikony košíku konfigurujte vlastnosti modulu ikony košíku.</span><span class="sxs-lookup"><span data-stu-id="2d574-140">In the property pane for the cart icon module, configure the properties of the cart icon module.</span></span> <span data-ttu-id="2d574-141">Chcete-li, aby ikona košíku při přechodu myší zobrazila košík, vyberte **True** pro možnost **Zobrazit mini košík**.</span><span class="sxs-lookup"><span data-stu-id="2d574-141">If you want the cart icon to display a mini cart when hovered over, select **True** for **Show mini cart**.</span></span>
1. <span data-ttu-id="2d574-142">Uložte fragment stránky, dokončete úpravy a publikujte ji.</span><span class="sxs-lookup"><span data-stu-id="2d574-142">Save the page fragment, finish editing, and publish it.</span></span> 


<span data-ttu-id="2d574-143">Chcete-li zajistit, aby se záhlaví zobrazilo na každé stránce, postupujte podle následujících kroků pro všechny šablony stránek, které jsou pro daný web vytvořeny.</span><span class="sxs-lookup"><span data-stu-id="2d574-143">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="2d574-144">Do pozice **Hlavní** na výchozí stránce přidejte do záhlaví fragment záhlaví stránky obsahující modul záhlaví.</span><span class="sxs-lookup"><span data-stu-id="2d574-144">In the **Main** slot of the default page, add the header page fragment that contains the header module to the header.</span></span>
1. <span data-ttu-id="2d574-145">Uložte šablonu, dokončete úpravy a publikujte ji.</span><span class="sxs-lookup"><span data-stu-id="2d574-145">Save the template, finish editing, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2d574-146">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="2d574-146">Additional resources</span></span>

[<span data-ttu-id="2d574-147">Přehled startovací sady</span><span class="sxs-lookup"><span data-stu-id="2d574-147">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="2d574-148">Modul kontejneru</span><span class="sxs-lookup"><span data-stu-id="2d574-148">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="2d574-149">Modul buy boxu</span><span class="sxs-lookup"><span data-stu-id="2d574-149">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="2d574-150">Modul košíku</span><span class="sxs-lookup"><span data-stu-id="2d574-150">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="2d574-151">Ikona modulu košíku</span><span class="sxs-lookup"><span data-stu-id="2d574-151">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="2d574-152">Modul pokladny</span><span class="sxs-lookup"><span data-stu-id="2d574-152">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="2d574-153">Modul potvrzení objednávky</span><span class="sxs-lookup"><span data-stu-id="2d574-153">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="2d574-154">Modul záhlaví</span><span class="sxs-lookup"><span data-stu-id="2d574-154">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="2d574-155">Modul zápatí</span><span class="sxs-lookup"><span data-stu-id="2d574-155">Footer module</span></span>](author-footer-module.md)
