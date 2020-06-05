---
title: Modul volby obchodu
description: Tohle téma se zabývá modulem výběru obchodu a popisuje, jak jej přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 03/19/2020
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
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 460d05ca29d5b8da70a971a649d9edd786f7260d
ms.sourcegitcommit: 15c5ec742d648c5f3506d031a2ab6150dcbae348
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2020
ms.locfileid: "3378201"
---
# <a name="store-selector-module"></a><span data-ttu-id="91ca1-103">Modul volby obchodu</span><span class="sxs-lookup"><span data-stu-id="91ca1-103">Store selector module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="91ca1-104">Tohle téma se zabývá modulem výběru obchodu a popisuje, jak jej přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="91ca1-104">This topic covers the store selector module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="91ca1-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="91ca1-105">Overview</span></span>

<span data-ttu-id="91ca1-106">Modul výběru obchodu je používán ve scénáři zákazníka „Nákup online, vyzvednutí v obchodě“ (BOPIS).</span><span class="sxs-lookup"><span data-stu-id="91ca1-106">A store selector module is used for the "buy online, pick up in store"" (BOPIS) customer scenario.</span></span> <span data-ttu-id="91ca1-107">Zobrazuje seznam obchodů, ve kterých je produkt k dispozici pro výdej, a také otevírací hodiny a zásoby produktů pro každý obchod.</span><span class="sxs-lookup"><span data-stu-id="91ca1-107">It displays a list of stores where a product is available for pickup, as well as store hours and product inventory for each store.</span></span>

<span data-ttu-id="91ca1-108">Modul výběru obchodu vyžaduje pro vyhledání obchodů kontext produktu a umístění.</span><span class="sxs-lookup"><span data-stu-id="91ca1-108">The store selector module requires the context of a product and a search location to find stores.</span></span> <span data-ttu-id="91ca1-109">V případě, že není k dispozici umístění, použije se umístění prohlížeče zákazníka za předpokladu, že zákazník udělí souhlas.</span><span class="sxs-lookup"><span data-stu-id="91ca1-109">In the absence of a search location, it defaults to the customer's browser location, provided that the customer gives consent.</span></span> <span data-ttu-id="91ca1-110">Modul obsahuje vstupní pole, které umožňuje zákazníkovi zadat umístění (PSČ nebo město a stát) k vyhledání obchodů, které jsou v dosahu.</span><span class="sxs-lookup"><span data-stu-id="91ca1-110">The module has an input box which allows the customer to enter a location (zipcode, or city and state) to find stores that are nearby.</span></span>

<span data-ttu-id="91ca1-111">Modul volby obchodu je integrovaný s API geokódování služby Mapy Bing, které slouží k převodu umístění na zeměpisnou šířku a délku.</span><span class="sxs-lookup"><span data-stu-id="91ca1-111">The store selector module is integrated with the Bing Maps Geocoding application programming interface (API) to convert the location to a latitude and longitude.</span></span> <span data-ttu-id="91ca1-112">Klíč rozhraní API mapy služby Bing je povinný a musí být přidán do stránky sdílené parametry pro Commerce v aplikaci Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="91ca1-112">A Bing Maps API key is required and must be added to the Commerce shared parameters page in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="91ca1-113">Modul volby obchodu lze přidat do modulu buy boxu na stránce Podrobnosti o produktu a zobrazit obchody, ve kterých je produkt k dispozici pro výdej.</span><span class="sxs-lookup"><span data-stu-id="91ca1-113">The store selector module can be added to a buy box module on the product details page (PDP) to display stores where a product is available for pickup.</span></span> <span data-ttu-id="91ca1-114">Lze jej také přidat do modulu košíku.</span><span class="sxs-lookup"><span data-stu-id="91ca1-114">It can also be added to a cart module.</span></span> <span data-ttu-id="91ca1-115">Při přidání do modulu košíku zobrazí modul volby obchodu možnosti vyzvednutí pro každou položku řádku nákupního košíku.</span><span class="sxs-lookup"><span data-stu-id="91ca1-115">When added to a cart module, the store selector module displays pickup options for each cart line item.</span></span> <span data-ttu-id="91ca1-116">Kromě toho s použitím vlastního kódu lze tento modul přidat na jiné stránky nebo do jiných modulů prostřednictvím rozšíření a přizpůsobení.</span><span class="sxs-lookup"><span data-stu-id="91ca1-116">In addition, with custom coding this module can be added to other pages or modules via extensions and customizations.</span></span>

<span data-ttu-id="91ca1-117">Aby scénář BOPIS fungoval, měly by být produkty konfigurovány se způsobem dodání „vyzvednutí zákazníkem“.</span><span class="sxs-lookup"><span data-stu-id="91ca1-117">For the BOPIS scenario to work, products should be configured with the "customer pickup" delivery mode.</span></span> <span data-ttu-id="91ca1-118">V opačném případě se modul na příslušných stránkách nezobrazí.</span><span class="sxs-lookup"><span data-stu-id="91ca1-118">Otherwise, the module will not be shown on the respective pages.</span></span> <span data-ttu-id="91ca1-119">Podrobné informace o konfiguraci způsobu dodání naleznete v tématu [Nastavení způsobů dodání](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span><span class="sxs-lookup"><span data-stu-id="91ca1-119">For details on how to configure the delivery mode, see [Set up modes of delivery](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

<span data-ttu-id="91ca1-120">Následující obrázek znázorňuje příklad modulu volby obchodu použitého na stránce s podrobnostmi o produktu.</span><span class="sxs-lookup"><span data-stu-id="91ca1-120">The following image shows an example of a store selector module used on a PDP.</span></span>

![Příklad modulu volby obchodu](./media/BOPIS.PNG)

## <a name="store-selector-module-usage-in-e-commerce"></a><span data-ttu-id="91ca1-122">Použití modulu volby obchodu v e-Commerce</span><span class="sxs-lookup"><span data-stu-id="91ca1-122">Store selector module usage in e-Commerce</span></span>

- <span data-ttu-id="91ca1-123">Modul volby obchodu lze použít na stránce Podrobnosti o produktu a vyhledat obchody v okolí, ve kterých je produkt k dispozici pro výdej.</span><span class="sxs-lookup"><span data-stu-id="91ca1-123">A store selector module can be used on a product details page (PDP) to find nearby stores where a product is available for pickup.</span></span>
- <span data-ttu-id="91ca1-124">Modul volby obchodu lze použít na stránce košíku a vyhledat obchody v okolí, ve kterých je produkt v košíku k dispozici pro výdej.</span><span class="sxs-lookup"><span data-stu-id="91ca1-124">A store selector module can be used on a cart page to find nearby stores where a product in the cart is available for pickup.</span></span>

## <a name="store-selector-module-properties"></a><span data-ttu-id="91ca1-125">Vlastnosti modulu volby obchodu</span><span class="sxs-lookup"><span data-stu-id="91ca1-125">Store selector module properties</span></span>

| <span data-ttu-id="91ca1-126">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="91ca1-126">Property name</span></span>             | <span data-ttu-id="91ca1-127">Hodnota</span><span class="sxs-lookup"><span data-stu-id="91ca1-127">Value</span></span>                 | <span data-ttu-id="91ca1-128">popis</span><span class="sxs-lookup"><span data-stu-id="91ca1-128">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="91ca1-129">Poloměr pro hledání</span><span class="sxs-lookup"><span data-stu-id="91ca1-129">Search radius</span></span> | <span data-ttu-id="91ca1-130">Počet</span><span class="sxs-lookup"><span data-stu-id="91ca1-130">Number</span></span> | <span data-ttu-id="91ca1-131">Definuje poloměr při vyhledávání obchodů v mílích.</span><span class="sxs-lookup"><span data-stu-id="91ca1-131">Defines the search radius for stores, in miles.</span></span> <span data-ttu-id="91ca1-132">Není-li zadána žádná hodnota, použije se výchozí poloměr 50 mil.</span><span class="sxs-lookup"><span data-stu-id="91ca1-132">If no value is specified, the default search radius of 50 miles is used.</span></span>|
|<span data-ttu-id="91ca1-133">Podmínky služby</span><span class="sxs-lookup"><span data-stu-id="91ca1-133">Terms of Service</span></span> | <span data-ttu-id="91ca1-134">Adresa URL</span><span class="sxs-lookup"><span data-stu-id="91ca1-134">URL</span></span>    |  <span data-ttu-id="91ca1-135">Adresa URL podmínek služby, která je vyžadována službou Bing Maps.</span><span class="sxs-lookup"><span data-stu-id="91ca1-135">The terms of service URL that is required for the Bing Maps service.</span></span> |

## <a name="add-a-store-selector-module-to-a-page"></a><span data-ttu-id="91ca1-136">Přidání modulu volby obchodu na stránku</span><span class="sxs-lookup"><span data-stu-id="91ca1-136">Add a store selector module to a page</span></span>

<span data-ttu-id="91ca1-137">Modul volby obchodu vyžaduje kontext produktu, a proto jej lze použít pouze v modulech buy boxu a košíku.</span><span class="sxs-lookup"><span data-stu-id="91ca1-137">A store selector module needs the context of a product, so it can only be used within buy box and cart modules.</span></span> <span data-ttu-id="91ca1-138">Moduly volby obchodu nefungují mimo tyto moduly.</span><span class="sxs-lookup"><span data-stu-id="91ca1-138">Store selector modules do not function outside these modules.</span></span>

- <span data-ttu-id="91ca1-139">Informace o přidání modulu volby obchodu do modulu buy boxu naleznete v tématu [Modul buy boxu](add-buy-box.md).</span><span class="sxs-lookup"><span data-stu-id="91ca1-139">For information on how to add a store selector module to a buy box module, see [Buy box module](add-buy-box.md).</span></span> 
- <span data-ttu-id="91ca1-140">Informace o přidání modulu volby obchodu do modulu košíku naleznete v tématu [Modul košíku](add-cart-module.md).</span><span class="sxs-lookup"><span data-stu-id="91ca1-140">For information on how to add a store selector module to a cart module, see [Cart module](add-cart-module.md)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="91ca1-141">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="91ca1-141">Additional resources</span></span>

[<span data-ttu-id="91ca1-142">Přehled startovací sady</span><span class="sxs-lookup"><span data-stu-id="91ca1-142">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="91ca1-143">Modul buy boxu</span><span class="sxs-lookup"><span data-stu-id="91ca1-143">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="91ca1-144">Modul košíku</span><span class="sxs-lookup"><span data-stu-id="91ca1-144">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="91ca1-145">Rychlá prohlídka stránky podrobností o produktu</span><span class="sxs-lookup"><span data-stu-id="91ca1-145">Quick tour of PDP</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="91ca1-146">Rychlá prohlídka košíku a pokladny</span><span class="sxs-lookup"><span data-stu-id="91ca1-146">Quick tour of Cart and checkout</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="91ca1-147">Nastavit způsoby dodání</span><span class="sxs-lookup"><span data-stu-id="91ca1-147">Set up modes of delivery</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)

[<span data-ttu-id="91ca1-148">Správa map Bing pro vaši organizaci</span><span class="sxs-lookup"><span data-stu-id="91ca1-148">Manage Bing Maps for your organization</span></span>](dev-itpro/manage-bing-maps.md)
