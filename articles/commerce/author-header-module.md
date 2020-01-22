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
ms.openlocfilehash: cc98419077f6f563ea2265d4e68ba809971cfbd6
ms.sourcegitcommit: ff93b8f6a11993f2cd00be2da7aa77ef0d950ab8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/03/2019
ms.locfileid: "2885471"
---
# <a name="header-module"></a><span data-ttu-id="c91e7-103">Modul záhlaví</span><span class="sxs-lookup"><span data-stu-id="c91e7-103">Header module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="c91e7-104">Toto téma popisuje moduly záhlaví a popisuje, jak je vytvořit v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="c91e7-104">This topic covers header modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="c91e7-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="c91e7-105">Overview</span></span>

<span data-ttu-id="c91e7-106">Modul záhlaví je speciální kontejner, který se používá k hostování všech modulů, které budou zobrazeny v záhlaví stránky.</span><span class="sxs-lookup"><span data-stu-id="c91e7-106">A header module is a special container that is used to host all the modules that will be shown in a page's header.</span></span> <span data-ttu-id="c91e7-107">Může například obsahovat logo webu, odkazy na hierarchii navigace, odkazy na další stránky na webu a vyhledávací panel.</span><span class="sxs-lookup"><span data-stu-id="c91e7-107">For example, it can include your site logo, links to the navigation hierarchy, links to other pages on the site, and the search bar.</span></span>

<span data-ttu-id="c91e7-108">Modul záhlaví je automaticky optimalizován pro zařízení, na kterém je stránka prohlížena (tj. desktopové nebo mobilní zařízení).</span><span class="sxs-lookup"><span data-stu-id="c91e7-108">A header module is automatically optimized for the device that the site is being viewed on (that is, a desktop device or a mobile device).</span></span> <span data-ttu-id="c91e7-109">Například v mobilním zařízení je navigační panel sbalen do tlačítka **Nabídka** (což je někdy nazýváno *hamburgerová nabídka*).</span><span class="sxs-lookup"><span data-stu-id="c91e7-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header"></a><span data-ttu-id="c91e7-110">Vlastnosti záhlaví</span><span class="sxs-lookup"><span data-stu-id="c91e7-110">Properties of a header</span></span>

<span data-ttu-id="c91e7-111">Podobně jako běžné kontejnery podporuje modul záhlaví vlastnosti **nadpis** a **šířka**.</span><span class="sxs-lookup"><span data-stu-id="c91e7-111">Like generic containers, a header module supports the **heading** and **width** properties.</span></span>

<span data-ttu-id="c91e7-112">Modul záhlaví obsahuje více pozic.</span><span class="sxs-lookup"><span data-stu-id="c91e7-112">A header module has multiple slots.</span></span> <span data-ttu-id="c91e7-113">Obsahuje například pozice pro informační zprávu, navigační nabídku, logo, vyhledávací panel, ikonu vozíku, ikonu seznamu přání a informace o účtu.</span><span class="sxs-lookup"><span data-stu-id="c91e7-113">For example, there are slots for an informational message, navigation menu, logo, search bar, cart icon, wish list icon, and account information.</span></span> <span data-ttu-id="c91e7-114">Každá pozice podporuje určitou sadu modulů.</span><span class="sxs-lookup"><span data-stu-id="c91e7-114">Each slot supports a specific set of modules.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="c91e7-115">Moduly, které jsou k dispozici v modulu záhlaví</span><span class="sxs-lookup"><span data-stu-id="c91e7-115">Modules that are available in a header module</span></span>

<span data-ttu-id="c91e7-116">Následující moduly lze použít v modulu záhlaví:</span><span class="sxs-lookup"><span data-stu-id="c91e7-116">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="c91e7-117">**Navigační nabídka** – Navigační nabídka představuje hierarchii navigace kanálu a další statické navigační odkazy.</span><span class="sxs-lookup"><span data-stu-id="c91e7-117">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="c91e7-118">Hierarchii navigace kanálu lze nakonfigurovat v aplikaci Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="c91e7-118">The channel navigation hierarchy can be configured in Dynamics 365 Retail.</span></span> <span data-ttu-id="c91e7-119">Konfigurované položky jsou pak zobrazeny jako navigace v záhlaví.</span><span class="sxs-lookup"><span data-stu-id="c91e7-119">Configured items then appear as header navigation.</span></span> <span data-ttu-id="c91e7-120">Kromě toho lze konfigurovat statické navigační odkazy a poskytnout relativní odkazy na jiné stránky na webu elektronického obchodování.</span><span class="sxs-lookup"><span data-stu-id="c91e7-120">In addition, static navigation links can be configured, and relative links to other pages on the e-Commerce site can be provided.</span></span> <span data-ttu-id="c91e7-121">Samotné záhlaví lze zarovnat doleva, doprava nebo na střed.</span><span class="sxs-lookup"><span data-stu-id="c91e7-121">The header itself can be aligned left, right, or center.</span></span>
- <span data-ttu-id="c91e7-122">**Ikona košíku** – Ikona košíku je speciální ikona, která představuje košík.</span><span class="sxs-lookup"><span data-stu-id="c91e7-122">**Cart icon** – The cart icon is a special icon that represents the cart.</span></span> <span data-ttu-id="c91e7-123">Je zobrazena v záhlaví a udává počet položek v vozíku.</span><span class="sxs-lookup"><span data-stu-id="c91e7-123">It's shown in the header and indicates the number of items in the cart.</span></span> <span data-ttu-id="c91e7-124">Odkaz na stránku košíku by měl doprovázet ikonu košíku, aby mohli být zákazníci při interakci s ikonou přesměrováni na stránku košíku.</span><span class="sxs-lookup"><span data-stu-id="c91e7-124">A link to the cart page should accompany the cart icon, so that customers can be redirected to the cart page when they interact with the icon.</span></span>
- <span data-ttu-id="c91e7-125">**Ikona seznamu přání** – V záhlaví je zobrazena ikona seznamu přání a udává počet přidaných položek do seznamu přání zákazníka.</span><span class="sxs-lookup"><span data-stu-id="c91e7-125">**Wish list icon** – The wish list icon is shown in the header and indicates the number of items that have been added to the customer's wish list.</span></span> <span data-ttu-id="c91e7-126">Odkaz na stránku seznamu přání by měl doprovázet tuto ikonu, aby mohli být zákazníci při interakci s ikonou přesměrováni na stránku seznamu přání.</span><span class="sxs-lookup"><span data-stu-id="c91e7-126">A link to the wish list page should accompany this icon, so that customers can be redirected to the wish list page when they interact with the icon.</span></span>
- <span data-ttu-id="c91e7-127">**Přihlašovací modul** – V záhlaví se zobrazí přihlašovací modul.</span><span class="sxs-lookup"><span data-stu-id="c91e7-127">**Sign-in module** – The sign-in module is shown in the header.</span></span> <span data-ttu-id="c91e7-128">Odběratelé se mohou přihlásit nebo registrovat k účtu.</span><span class="sxs-lookup"><span data-stu-id="c91e7-128">It lets customers either sign in to their account or sign up for an account.</span></span> <span data-ttu-id="c91e7-129">Pokud je zákazník již přihlášen, lze tento modul nakonfigurovat tak, aby zobrazoval odkazy na stránku účtu, stránku historie objednávek nebo jinou stránku.</span><span class="sxs-lookup"><span data-stu-id="c91e7-129">If the customer is already signed in, the module can be configured to show links to the account page, order history page, or another page.</span></span>
- <span data-ttu-id="c91e7-130">**Modul loga** – Tento modul zobrazuje logo, které představuje maloobchodníka a značku.</span><span class="sxs-lookup"><span data-stu-id="c91e7-130">**Logo module** – This module shows the logo that represents the retailer and brand.</span></span> <span data-ttu-id="c91e7-131">Jedná se o obrázek s odkazem.</span><span class="sxs-lookup"><span data-stu-id="c91e7-131">It's an image that has a link.</span></span> <span data-ttu-id="c91e7-132">Odkaz je obvykle konfigurován tak, že přesměruje na domovskou stránku. Zákazníci se tedy mohou rychle vrátit na domovskou stránku z libovolné stránky na webu.</span><span class="sxs-lookup"><span data-stu-id="c91e7-132">The link is typically configured so that it has a redirect to the home page, Therefore, customers can quickly return to the home page from any page on the site.</span></span>
- <span data-ttu-id="c91e7-133">**Výstraha** – V záhlaví se zobrazí výstraha, která slouží k zobrazení vložené zprávy, která se vztahuje na všechny stránky na webu.</span><span class="sxs-lookup"><span data-stu-id="c91e7-133">**Alert** – An alert appears in the header and is used to show an inline message that applies to all pages on the site.</span></span> <span data-ttu-id="c91e7-134">Výstraha může například zobrazovat zprávu, že „Výroční výprodej končí za 2 dny“.</span><span class="sxs-lookup"><span data-stu-id="c91e7-134">For example, an alert might show a message such as "Annual sale ends in 2 days."</span></span>
- <span data-ttu-id="c91e7-135">**Vyhledávací panel** – Vyhledávací panel umožňuje uživatelům zadat hledané termíny, aby mohli vyhledávat produkty.</span><span class="sxs-lookup"><span data-stu-id="c91e7-135">**Search bar** – The search bar lets users enter search terms so that they can search for products.</span></span> <span data-ttu-id="c91e7-136">Modul musí být konfigurován s adresou URL stránky výsledků hledání.</span><span class="sxs-lookup"><span data-stu-id="c91e7-136">The module must be configured with the URL of the search results page.</span></span> <span data-ttu-id="c91e7-137">Parametr řetězce dotazu lze nakonfigurovat (výchozí hodnota je **„q“**).</span><span class="sxs-lookup"><span data-stu-id="c91e7-137">The query string parameter can be configured (the default value is **"q"**).</span></span> <span data-ttu-id="c91e7-138">Vyhledávací panel obsahuje pozici automatických návrhů, kam by měl být přidán modul automatických návrhů.</span><span class="sxs-lookup"><span data-stu-id="c91e7-138">The search bar has an autosuggest slot where the autosuggest module should be added.</span></span>
- <span data-ttu-id="c91e7-139">**Automatické návrhy** – Modul automatických návrhů zobrazuje automaticky navrhované výsledky.</span><span class="sxs-lookup"><span data-stu-id="c91e7-139">**Autosuggest** – The autosuggest module shows automatically suggested results.</span></span> <span data-ttu-id="c91e7-140">Může se jednat o tyto výsledky: klíčová slova, produkty nebo kategorie, ve kterých je hledaný výraz nalezen.</span><span class="sxs-lookup"><span data-stu-id="c91e7-140">These results can be keywords, products, or categories where the search term is found.</span></span>

## <a name="create-a-header-module"></a><span data-ttu-id="c91e7-141">Vytvoření modulu záhlaví</span><span class="sxs-lookup"><span data-stu-id="c91e7-141">Create a header module</span></span>

<span data-ttu-id="c91e7-142">Chcete-li vytvořit modul záhlaví, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="c91e7-142">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="c91e7-143">Vytvořte fragment stránky, který obsahuje modul záhlaví.</span><span class="sxs-lookup"><span data-stu-id="c91e7-143">Create a page fragment that includes a header module.</span></span>
1. <span data-ttu-id="c91e7-144">Přidejte moduly do pozic v modulu záhlaví.</span><span class="sxs-lookup"><span data-stu-id="c91e7-144">Add modules to the slots in the header module.</span></span>
1. <span data-ttu-id="c91e7-145">Aktualizujte nastavení pro každý modul.</span><span class="sxs-lookup"><span data-stu-id="c91e7-145">Update the settings for each module.</span></span>
1. <span data-ttu-id="c91e7-146">Uložte fragment stránky.</span><span class="sxs-lookup"><span data-stu-id="c91e7-146">Save the page fragment.</span></span> 
1. <span data-ttu-id="c91e7-147">Vraťte stránku se změnami a publikujte ji.</span><span class="sxs-lookup"><span data-stu-id="c91e7-147">Check in the page, and publish it.</span></span>

<span data-ttu-id="c91e7-148">Chcete-li zajistit, aby se záhlaví zobrazilo na každé stránce, postupujte podle následujících kroků pro všechny šablony stránek, které jsou pro daný web vytvořeny.</span><span class="sxs-lookup"><span data-stu-id="c91e7-148">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="c91e7-149">Na výchozí stránce přidejte do hlavní pozice záhlaví fragment stránky obsahující modul záhlaví.</span><span class="sxs-lookup"><span data-stu-id="c91e7-149">On the default page, add the page fragment containing the header module to the header in the main slot.</span></span>
1. <span data-ttu-id="c91e7-150">Uložte šablonu.</span><span class="sxs-lookup"><span data-stu-id="c91e7-150">Save the template.</span></span> 
1. <span data-ttu-id="c91e7-151">Vraťte šablonu se změnami a publikujte ji.</span><span class="sxs-lookup"><span data-stu-id="c91e7-151">Check in the template, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c91e7-152">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="c91e7-152">Additional resources</span></span>

[<span data-ttu-id="c91e7-153">Přehled startovací sady</span><span class="sxs-lookup"><span data-stu-id="c91e7-153">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="c91e7-154">Modul kontejneru</span><span class="sxs-lookup"><span data-stu-id="c91e7-154">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="c91e7-155">Modul buy boxu</span><span class="sxs-lookup"><span data-stu-id="c91e7-155">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="c91e7-156">Modul košíku</span><span class="sxs-lookup"><span data-stu-id="c91e7-156">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="c91e7-157">Modul pokladny</span><span class="sxs-lookup"><span data-stu-id="c91e7-157">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="c91e7-158">Modul potvrzení objednávky</span><span class="sxs-lookup"><span data-stu-id="c91e7-158">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="c91e7-159">Modul záhlaví</span><span class="sxs-lookup"><span data-stu-id="c91e7-159">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="c91e7-160">Modul zápatí</span><span class="sxs-lookup"><span data-stu-id="c91e7-160">Footer module</span></span>](author-footer-module.md)
