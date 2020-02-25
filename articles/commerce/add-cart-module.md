---
title: Modul košíku
description: Tohle téma se zabývá moduly košíku a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: f6dd8fb56f7342eb9c877eda503a92f4a31e5863
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025429"
---
# <a name="cart-module"></a><span data-ttu-id="a2db3-103">Modul košíku</span><span class="sxs-lookup"><span data-stu-id="a2db3-103">Cart module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="a2db3-104">Tohle téma se zabývá moduly košíku a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a2db3-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a2db3-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="a2db3-105">Overview</span></span>

<span data-ttu-id="a2db3-106">Modul košíku se používá k zobrazení položek, které byly přidány do košíku, než odběratel pokračuje v rezervaci.</span><span class="sxs-lookup"><span data-stu-id="a2db3-106">A cart module is used to show the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="a2db3-107">Obsahuje například všechny položky, které byly přidány do nákupního košíku a souhrn objednávky.</span><span class="sxs-lookup"><span data-stu-id="a2db3-107">For example, it includes all the items that have been added to the cart and an order summary.</span></span> <span data-ttu-id="a2db3-108">Dále umožňuje odběrateli použití nebo odebrání propagačních kódů.</span><span class="sxs-lookup"><span data-stu-id="a2db3-108">It also lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="a2db3-109">Modul košíku podporuje přihlášené uživatele i hosty.</span><span class="sxs-lookup"><span data-stu-id="a2db3-109">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="a2db3-110">Také podporuje odkaz **Zpět na nákupy**.</span><span class="sxs-lookup"><span data-stu-id="a2db3-110">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="a2db3-111">Můžete konfigurovat cestu pro tento odkaz v **Nastavení webu \> Rozšíření \> Cesty**.</span><span class="sxs-lookup"><span data-stu-id="a2db3-111">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="a2db3-112">Modul košíku vykresluje data na základě ID košíku.</span><span class="sxs-lookup"><span data-stu-id="a2db3-112">The cart module renders data based on the cart ID.</span></span> <span data-ttu-id="a2db3-113">ID košíku je soubor cookie prohlížeče, který je k dispozici v rámci celého webu.</span><span class="sxs-lookup"><span data-stu-id="a2db3-113">The cart ID is a browser cookie that is available throughout the site.</span></span>

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="a2db3-114">Vlastnosti a pozice modulu košíku</span><span class="sxs-lookup"><span data-stu-id="a2db3-114">Cart module properties and slots</span></span>

<span data-ttu-id="a2db3-115">Modul košíku má vlastnost **Záhlaví**, kterou lze nastavit na hodnoty, jako je **Nákupní taška** a **Položky v košíku**.</span><span class="sxs-lookup"><span data-stu-id="a2db3-115">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="a2db3-116">Moduly, které lze použít v modulu košíku</span><span class="sxs-lookup"><span data-stu-id="a2db3-116">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="a2db3-117">**Textový blok** – Tento modul podporuje vlastní zasílání zpráv v modulu košíku.</span><span class="sxs-lookup"><span data-stu-id="a2db3-117">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="a2db3-118">Zprávy řídí systém správy obsahu (CMS).</span><span class="sxs-lookup"><span data-stu-id="a2db3-118">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="a2db3-119">Lze přidat libovolnou zprávu, například „Při problémech s objednávkou volejte 123 456 789“.</span><span class="sxs-lookup"><span data-stu-id="a2db3-119">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="a2db3-120">**Volič obchodů** – Tento modul zobrazuje seznam obchodů, které jsou poblíž a kde je položka k výdeji.</span><span class="sxs-lookup"><span data-stu-id="a2db3-120">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="a2db3-121">Umožňuje uživatelům zadat umístění pro hledání obchodů, které jsou v okolí.</span><span class="sxs-lookup"><span data-stu-id="a2db3-121">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="a2db3-122">Modul volby obchodu je integrovaný s API geokódování služby Mapy Bing, které slouží k převodu umístění na zeměpisnou šířku a délku.</span><span class="sxs-lookup"><span data-stu-id="a2db3-122">The store selector module is integrated with the Bing Maps Geocoding application programming interface (API) to convert the location to a latitude and longitude.</span></span> <span data-ttu-id="a2db3-123">Klíč rozhraní API mapy služby Bing je povinný a musí být přidán do stránky sdílené parametry pro Retail v aplikaci Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="a2db3-123">A Bing Maps API key is required and must be added to the Retail shared parameters page in Dynamics 365 Retail.</span></span> <span data-ttu-id="a2db3-124">Tento modul podporuje dvě vlastnosti, **Okruh hledání** a **Odkaz na podmínky služby**.</span><span class="sxs-lookup"><span data-stu-id="a2db3-124">This module supports two properties, **Search radius** and **Terms of service link**.</span></span> <span data-ttu-id="a2db3-125">Vlastnost **Okruh hledání** definuje poloměr vyhledávání pro obchody v mílích.</span><span class="sxs-lookup"><span data-stu-id="a2db3-125">The **Search radius** property defines the search radius for stores, in miles.</span></span> <span data-ttu-id="a2db3-126">Není-li zadána žádná hodnota, použije se výchozí poloměr vyhledávání 50 mil.</span><span class="sxs-lookup"><span data-stu-id="a2db3-126">If no value is specified, the default search radius, 50 miles, is used.</span></span> <span data-ttu-id="a2db3-127">Pokud se používají mapy Bing nebo některá externí služba, vlastnost **Odkaz na podmínky služby** se používá k získání odkazu na podmínky služby.</span><span class="sxs-lookup"><span data-stu-id="a2db3-127">If Bings Maps or any external service is used, the **Terms of service link** property can be used to provide a link to the terms of service.</span></span> <span data-ttu-id="a2db3-128">Pro službu Bing Maps je vyžadován odkaz na podmínky služby.</span><span class="sxs-lookup"><span data-stu-id="a2db3-128">A terms of service link is required for the Bing Maps service.</span></span> 

## <a name="cart-module-settings"></a><span data-ttu-id="a2db3-129">Nastavení modulu košíku</span><span class="sxs-lookup"><span data-stu-id="a2db3-129">Cart module settings</span></span>

<span data-ttu-id="a2db3-130">Moduly košíku mají následující nastavení, která lze konfigurovat na **Nastavení webu \> Rozšíření**:</span><span class="sxs-lookup"><span data-stu-id="a2db3-130">Cart modules have the following settings that can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="a2db3-131">**Maximální množství** – tato vlastnost se používá k určení maximálního počtu jednotlivých položek, které lze přidat do nákupního košíku.</span><span class="sxs-lookup"><span data-stu-id="a2db3-131">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="a2db3-132">Maloobchodní prodejce může například rozhodnout, že v jedné transakci lze prodávat pouze 10 jednotlivých produktů.</span><span class="sxs-lookup"><span data-stu-id="a2db3-132">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="a2db3-133">**Kontrola zásob** – Je-li nastavena hodnota **Pravda**, položka se přidá do košíku pouze poté, co se modul buy boxu ověří, že je na skladě.</span><span class="sxs-lookup"><span data-stu-id="a2db3-133">**Inventory check** – When the value is set to **True**, an item is added to the cart only after the buy box module makes sure that it's in stock.</span></span> <span data-ttu-id="a2db3-134">Tato kontrola zásob se provádí pro scénáře, když má být položka expedována, a pro scénáře, kdy má být vyzvednuta v obchodě.</span><span class="sxs-lookup"><span data-stu-id="a2db3-134">This inventory check is done both for scenarios where the item will be shipped and for scenarios where it will be picked up in the store.</span></span> <span data-ttu-id="a2db3-135">Je-li tato hodnota nastavena na hodnotu **Nepravda**, před přidáním položky do nákupního košíku a podání objednávky není provedena kontrola zásob.</span><span class="sxs-lookup"><span data-stu-id="a2db3-135">If the value is set to **False**, no inventory check is done before an item is added to the cart and the order is placed.</span></span>
- <span data-ttu-id="a2db3-136">**Zásboník zásob** – Tato vlastnost se používá k určení čísla zásobníku pro zásoby.</span><span class="sxs-lookup"><span data-stu-id="a2db3-136">**Inventory buffer** – This property is used to specify a buffer number for inventory.</span></span> <span data-ttu-id="a2db3-137">Údržba zásob probíhá v reálném čase a když mnoho zákazníků podá objednávku, může být obtížné zajistit přesný počet zásob.</span><span class="sxs-lookup"><span data-stu-id="a2db3-137">Inventory is maintained in real time, and when many customers place orders, it can be difficult to maintain an accurate inventory count.</span></span> <span data-ttu-id="a2db3-138">Když je provedena kontrola zásob, pokud je množství na skladu nižší než množství zásobníku, produkt je brán, jakože není na skladu.</span><span class="sxs-lookup"><span data-stu-id="a2db3-138">When an inventory check is done, if the inventory is less than the buffer amount, the product is treated as out of stock.</span></span> <span data-ttu-id="a2db3-139">Pokud se tedy prodej rychle točí prostřednictvím několika kanálů a zásoby nejsou plně synchronizovány, existuje menší riziko, že položka, která se nenachází na skladě, je v prodeji.</span><span class="sxs-lookup"><span data-stu-id="a2db3-139">Therefore, when sales occur quickly through several channels, and the inventory count isn't fully synced, there is less risk that an item that is out of stock will be sold.</span></span>
- <span data-ttu-id="a2db3-140">**Zpět k nákupu** – Tato vlastnost se používá k určení trasy pro odkaz **Zpět k nákupu**.</span><span class="sxs-lookup"><span data-stu-id="a2db3-140">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="a2db3-141">Tento postup lze konfigurovat na úrovni pracoviště.</span><span class="sxs-lookup"><span data-stu-id="a2db3-141">This route can be configured at the site level.</span></span> <span data-ttu-id="a2db3-142">Tuto konfiguraci maloobchodní prodejci používají pro nasměrování zákazníků zpět na domovskou stránku nebo jakoukoli jinou stránku na webu.</span><span class="sxs-lookup"><span data-stu-id="a2db3-142">This configuration lets retailers take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="a2db3-143">Interakce Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="a2db3-143">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="a2db3-144">Modul košíku načítá informace o produktu pomocí rozhraní API Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="a2db3-144">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="a2db3-145">ID košíku ze souboru cookie prohlížeče se používá k načtení všech informací o produktu z Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="a2db3-145">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="a2db3-146">Přidání modulu košíku na stránku</span><span class="sxs-lookup"><span data-stu-id="a2db3-146">Add a cart module to a page</span></span>

<span data-ttu-id="a2db3-147">Chcete-li přidat modul košíku na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="a2db3-147">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="a2db3-148">Vytvořte fragment s názvem **Fragment košíku** a do něj přidejte modul košíku.</span><span class="sxs-lookup"><span data-stu-id="a2db3-148">Create a fragment that is named **Cart fragment**, and add a cart module to it.</span></span>
1. <span data-ttu-id="a2db3-149">Přidejte do modulu košíku nadpis.</span><span class="sxs-lookup"><span data-stu-id="a2db3-149">Add a heading to the cart module.</span></span>
1. <span data-ttu-id="a2db3-150">Přidejte modul Selector obchodu do modulu vozík.</span><span class="sxs-lookup"><span data-stu-id="a2db3-150">Add a store selector module to the cart module.</span></span>
1. <span data-ttu-id="a2db3-151">Uložte fragment, dokončete úpravy a publikujte ji.</span><span class="sxs-lookup"><span data-stu-id="a2db3-151">Save the fragment, finish editing it, and publish it.</span></span>
1. <span data-ttu-id="a2db3-152">Vytvořte šablonu s názvem **Šablona košíku** a přidejte fragment košíku, který jste právě vytvořili.</span><span class="sxs-lookup"><span data-stu-id="a2db3-152">Create a template that is named **Cart template**, and add the cart fragment that you just created to it.</span></span>
1. <span data-ttu-id="a2db3-153">Uložte šablonu, dokončete úpravy a publikujte ji.</span><span class="sxs-lookup"><span data-stu-id="a2db3-153">Save the template, finish editing it, and publish it.</span></span>
1. <span data-ttu-id="a2db3-154">Vytvořte stránku, která používá novou šablonu.</span><span class="sxs-lookup"><span data-stu-id="a2db3-154">Create a page that uses the new template.</span></span>
1. <span data-ttu-id="a2db3-155">Uložte stránku a zobrazte náhled.</span><span class="sxs-lookup"><span data-stu-id="a2db3-155">Save and preview the page.</span></span>
1. <span data-ttu-id="a2db3-156">Dokončete úpravy stránky a publikujte ji.</span><span class="sxs-lookup"><span data-stu-id="a2db3-156">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a2db3-157">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="a2db3-157">Additional resources</span></span>

[<span data-ttu-id="a2db3-158">Přehled startovací sady</span><span class="sxs-lookup"><span data-stu-id="a2db3-158">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="a2db3-159">Modul kontejneru</span><span class="sxs-lookup"><span data-stu-id="a2db3-159">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="a2db3-160">Modul buy boxu</span><span class="sxs-lookup"><span data-stu-id="a2db3-160">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="a2db3-161">Modul pokladny</span><span class="sxs-lookup"><span data-stu-id="a2db3-161">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="a2db3-162">Modul potvrzení objednávky</span><span class="sxs-lookup"><span data-stu-id="a2db3-162">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="a2db3-163">Modul záhlaví</span><span class="sxs-lookup"><span data-stu-id="a2db3-163">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="a2db3-164">Modul zápatí</span><span class="sxs-lookup"><span data-stu-id="a2db3-164">Footer module</span></span>](author-footer-module.md)
