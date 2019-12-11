---
title: Modul záhlaví
description: Toto téma popisuje moduly záhlaví a popisuje, jak je vytvořit v řešení Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: d393701dacb88ab03a4b56724d93c794da6bb5c8
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697268"
---
# <a name="header-module"></a><span data-ttu-id="6f5b7-103">Modul záhlaví</span><span class="sxs-lookup"><span data-stu-id="6f5b7-103">Header module</span></span>

<span data-ttu-id="6f5b7-104">[!include [banner]includes/preview-banner.md)] [!include [banner](includes/banner.md)]</span><span class="sxs-lookup"><span data-stu-id="6f5b7-104">[!include [banner]includes/preview-banner.md)] [!include [banner](includes/banner.md)]</span></span>

<span data-ttu-id="6f5b7-105">Toto téma popisuje moduly záhlaví a popisuje, jak je vytvořit v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-105">This topic covers header modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6f5b7-106">Přehled</span><span class="sxs-lookup"><span data-stu-id="6f5b7-106">Overview</span></span>

<span data-ttu-id="6f5b7-107">Modul záhlaví je speciální kontejner, který se používá k hostování všech modulů, které budou zobrazeny v záhlaví stránky.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-107">A header module is a special container that is used to host all the modules that will be shown in a page's header.</span></span> <span data-ttu-id="6f5b7-108">Může například obsahovat logo webu, odkazy na hierarchii navigace, odkazy na další stránky na webu a vyhledávací panel.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-108">For example, it can include your site logo, links to the navigation hierarchy, links to other pages on the site, and the search bar.</span></span>

<span data-ttu-id="6f5b7-109">Modul záhlaví je automaticky optimalizován pro zařízení, na kterém je stránka prohlížena (tj. desktopové nebo mobilní zařízení).</span><span class="sxs-lookup"><span data-stu-id="6f5b7-109">A header module is automatically optimized for the device that the site is being viewed on (that is, a desktop device or a mobile device).</span></span> <span data-ttu-id="6f5b7-110">Například v mobilním zařízení je navigační panel sbalen do tlačítka **Nabídka** (což je někdy nazýváno *hamburgerová nabídka*).</span><span class="sxs-lookup"><span data-stu-id="6f5b7-110">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header"></a><span data-ttu-id="6f5b7-111">Vlastnosti záhlaví</span><span class="sxs-lookup"><span data-stu-id="6f5b7-111">Properties of a header</span></span>

<span data-ttu-id="6f5b7-112">Podobně jako běžné kontejnery podporuje modul záhlaví vlastnosti **nadpis** a **šířka**.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-112">Like generic containers, a header module supports the **heading** and **width** properties.</span></span>

<span data-ttu-id="6f5b7-113">Modul záhlaví obsahuje více pozic.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-113">A header module has multiple slots.</span></span> <span data-ttu-id="6f5b7-114">Obsahuje například pozice pro informační zprávu, navigační nabídku, logo, vyhledávací panel, ikonu vozíku, ikonu seznamu přání a informace o účtu.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-114">For example, there are slots for an informational message, navigation menu, logo, search bar, cart icon, wish list icon, and account information.</span></span> <span data-ttu-id="6f5b7-115">Každá pozice podporuje určitou sadu modulů.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-115">Each slot supports a specific set of modules.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="6f5b7-116">Moduly, které jsou k dispozici v modulu záhlaví</span><span class="sxs-lookup"><span data-stu-id="6f5b7-116">Modules that are available in a header module</span></span>

<span data-ttu-id="6f5b7-117">Následující moduly lze použít v modulu záhlaví:</span><span class="sxs-lookup"><span data-stu-id="6f5b7-117">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="6f5b7-118">**Navigační nabídka** – Navigační nabídka představuje hierarchii navigace kanálu a další statické navigační odkazy.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-118">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="6f5b7-119">Hierarchii navigace kanálu lze nakonfigurovat v aplikaci Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-119">The channel navigation hierarchy can be configured in Dynamics 365 Retail.</span></span> <span data-ttu-id="6f5b7-120">Konfigurované položky jsou pak zobrazeny jako navigace v záhlaví.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-120">Configured items then appear as header navigation.</span></span> <span data-ttu-id="6f5b7-121">Kromě toho lze konfigurovat statické navigační odkazy a poskytnout relativní odkazy na jiné stránky na webu elektronického obchodování.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-121">In addition, static navigation links can be configured, and relative links to other pages on the e-Commerce site can be provided.</span></span> <span data-ttu-id="6f5b7-122">Samotné záhlaví lze zarovnat doleva, doprava nebo na střed.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-122">The header itself can be aligned left, right, or center.</span></span>
- <span data-ttu-id="6f5b7-123">**Ikona košíku** – Ikona košíku je speciální ikona, která představuje košík.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-123">**Cart icon** – The cart icon is a special icon that represents the cart.</span></span> <span data-ttu-id="6f5b7-124">Je zobrazena v záhlaví a udává počet položek v vozíku.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-124">It's shown in the header and indicates the number of items in the cart.</span></span> <span data-ttu-id="6f5b7-125">Odkaz na stránku košíku by měl doprovázet ikonu košíku, aby mohli být zákazníci při interakci s ikonou přesměrováni na stránku košíku.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-125">A link to the cart page should accompany the cart icon, so that customers can be redirected to the cart page when they interact with the icon.</span></span>
- <span data-ttu-id="6f5b7-126">**Ikona seznamu přání** – V záhlaví je zobrazena ikona seznamu přání a udává počet přidaných položek do seznamu přání zákazníka.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-126">**Wish list icon** – The wish list icon is shown in the header and indicates the number of items that have been added to the customer's wish list.</span></span> <span data-ttu-id="6f5b7-127">Odkaz na stránku seznamu přání by měl doprovázet tuto ikonu, aby mohli být zákazníci při interakci s ikonou přesměrováni na stránku seznamu přání.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-127">A link to the wish list page should accompany this icon, so that customers can be redirected to the wish list page when they interact with the icon.</span></span>
- <span data-ttu-id="6f5b7-128">**Přihlašovací modul** – V záhlaví se zobrazí přihlašovací modul.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-128">**Sign-in module** – The sign-in module is shown in the header.</span></span> <span data-ttu-id="6f5b7-129">Odběratelé se mohou přihlásit nebo registrovat k účtu.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-129">It lets customers either sign in to their account or sign up for an account.</span></span> <span data-ttu-id="6f5b7-130">Pokud je zákazník již přihlášen, lze tento modul nakonfigurovat tak, aby zobrazoval odkazy na stránku účtu, stránku historie objednávek nebo jinou stránku.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-130">If the customer is already signed in, the module can be configured to show links to the account page, order history page, or another page.</span></span>
- <span data-ttu-id="6f5b7-131">**Modul loga** – Tento modul zobrazuje logo, které představuje maloobchodníka a značku.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-131">**Logo module** – This module shows the logo that represents the retailer and brand.</span></span> <span data-ttu-id="6f5b7-132">Jedná se o obrázek s odkazem.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-132">It's an image that has a link.</span></span> <span data-ttu-id="6f5b7-133">Odkaz je obvykle konfigurován tak, že přesměruje na domovskou stránku. Zákazníci se tedy mohou rychle vrátit na domovskou stránku z libovolné stránky na webu.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-133">The link is typically configured so that it has a redirect to the home page, Therefore, customers can quickly return to the home page from any page on the site.</span></span>
- <span data-ttu-id="6f5b7-134">**Výstraha** – V záhlaví se zobrazí výstraha, která slouží k zobrazení vložené zprávy, která se vztahuje na všechny stránky na webu.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-134">**Alert** – An alert appears in the header and is used to show an inline message that applies to all pages on the site.</span></span> <span data-ttu-id="6f5b7-135">Výstraha může například zobrazovat zprávu, že „Výroční výprodej končí za 2 dny“.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-135">For example, an alert might show a message such as "Annual sale ends in 2 days."</span></span>
- <span data-ttu-id="6f5b7-136">**Vyhledávací panel** – Vyhledávací panel umožňuje uživatelům zadat hledané termíny, aby mohli vyhledávat produkty.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-136">**Search bar** – The search bar lets users enter search terms so that they can search for products.</span></span> <span data-ttu-id="6f5b7-137">Modul musí být konfigurován s adresou URL stránky výsledků hledání.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-137">The module must be configured with the URL of the search results page.</span></span> <span data-ttu-id="6f5b7-138">Parametr řetězce dotazu lze nakonfigurovat (výchozí hodnota je **„q“**).</span><span class="sxs-lookup"><span data-stu-id="6f5b7-138">The query string parameter can be configured (the default value is **"q"**).</span></span> <span data-ttu-id="6f5b7-139">Vyhledávací panel obsahuje pozici automatických návrhů, kam by měl být přidán modul automatických návrhů.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-139">The search bar has an autosuggest slot where the autosuggest module should be added.</span></span>
- <span data-ttu-id="6f5b7-140">**Automatické návrhy** – Modul automatických návrhů zobrazuje automaticky navrhované výsledky.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-140">**Autosuggest** – The autosuggest module shows automatically suggested results.</span></span> <span data-ttu-id="6f5b7-141">Může se jednat o tyto výsledky: klíčová slova, produkty nebo kategorie, ve kterých je hledaný výraz nalezen.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-141">These results can be keywords, products, or categories where the search term is found.</span></span>

## <a name="create-a-header-module"></a><span data-ttu-id="6f5b7-142">Vytvoření modulu záhlaví</span><span class="sxs-lookup"><span data-stu-id="6f5b7-142">Create a header module</span></span>

<span data-ttu-id="6f5b7-143">Chcete-li vytvořit modul záhlaví, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-143">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="6f5b7-144">Vytvořte fragment stránky, který obsahuje modul záhlaví.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-144">Create a page fragment that includes a header module.</span></span>
1. <span data-ttu-id="6f5b7-145">Přidejte moduly do pozic v modulu záhlaví.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-145">Add modules to the slots in the header module.</span></span>
1. <span data-ttu-id="6f5b7-146">Aktualizujte nastavení pro každý modul.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-146">Update the settings for each module.</span></span>
1. <span data-ttu-id="6f5b7-147">Uložte fragment stránky.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-147">Save the page fragment.</span></span> 
1. <span data-ttu-id="6f5b7-148">Vraťte stránku se změnami a publikujte ji.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-148">Check in the page, and publish it.</span></span>

<span data-ttu-id="6f5b7-149">Chcete-li zajistit, aby se záhlaví zobrazilo na každé stránce, postupujte podle následujících kroků pro všechny šablony stránek, které jsou pro daný web vytvořeny.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-149">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="6f5b7-150">Na výchozí stránce přidejte do hlavní pozice záhlaví fragment stránky obsahující modul záhlaví.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-150">On the default page, add the page fragment containing the header module to the header in the main slot.</span></span>
1. <span data-ttu-id="6f5b7-151">Uložte šablonu.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-151">Save the template.</span></span> 
1. <span data-ttu-id="6f5b7-152">Vraťte šablonu se změnami a publikujte ji.</span><span class="sxs-lookup"><span data-stu-id="6f5b7-152">Check in the template, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6f5b7-153">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="6f5b7-153">Additional resources</span></span>

[<span data-ttu-id="6f5b7-154">Přehled startovací sady</span><span class="sxs-lookup"><span data-stu-id="6f5b7-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="6f5b7-155">Modul kontejneru</span><span class="sxs-lookup"><span data-stu-id="6f5b7-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="6f5b7-156">Modul buy boxu</span><span class="sxs-lookup"><span data-stu-id="6f5b7-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="6f5b7-157">Modul košíku</span><span class="sxs-lookup"><span data-stu-id="6f5b7-157">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="6f5b7-158">Modul pokladny</span><span class="sxs-lookup"><span data-stu-id="6f5b7-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="6f5b7-159">Modul potvrzení objednávky</span><span class="sxs-lookup"><span data-stu-id="6f5b7-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="6f5b7-160">Modul záhlaví</span><span class="sxs-lookup"><span data-stu-id="6f5b7-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="6f5b7-161">Modul zápatí</span><span class="sxs-lookup"><span data-stu-id="6f5b7-161">Footer module</span></span>](author-footer-module.md)
