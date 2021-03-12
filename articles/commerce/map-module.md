---
title: Modul mapy
description: Toto téma popisuje moduly mapy a popisuje, jak je konfigurovat v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: e93358a9c76e8eb7bfb4ade4f772dece2aa5f7d3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982483"
---
# <a name="map-module"></a><span data-ttu-id="b3188-103">Modul mapy</span><span class="sxs-lookup"><span data-stu-id="b3188-103">Map module</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="b3188-104">Toto téma popisuje moduly mapy a popisuje, jak je konfigurovat v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b3188-104">This topic covers map modules and describes how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b3188-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="b3188-105">Overview</span></span>

<span data-ttu-id="b3188-106">Modul mapy zobrazuje umístění obchodů na interaktivní mapě, která je vykreslena pomocí [webového ovládacího prvku Bing Maps V8](https://docs.microsoft.com/bingmaps/v8-web-control/).</span><span class="sxs-lookup"><span data-stu-id="b3188-106">A map module shows the locations of stores on an interactive map that is rendered by using the [Bing Maps V8 Web Control](https://docs.microsoft.com/bingmaps/v8-web-control/).</span></span> <span data-ttu-id="b3188-107">Klíč rozhraní API mapy služby Bing je povinný a musí být přidán do stránky se sdílenými parametry pro centrálu Commerce.</span><span class="sxs-lookup"><span data-stu-id="b3188-107">A Bing Maps API key is required and must be added to the shared parameters page in Commerce headquarters.</span></span> <span data-ttu-id="b3188-108">Moduly mapy poskytují různá zobrazení, jako jsou silniční, anténní a pouliční, které si uživatelé mohou vybrat pro zobrazení polohy na mapě.</span><span class="sxs-lookup"><span data-stu-id="b3188-108">Map modules provide different views, such as Road, Aerial, and Streetside, that users can select to view map locations.</span></span> <span data-ttu-id="b3188-109">Umožňují také interakce, jako je přibližování a používání polohy uživatele.</span><span class="sxs-lookup"><span data-stu-id="b3188-109">They also allow for interactions such as zooming and using the user's location.</span></span>

<span data-ttu-id="b3188-110">Modul mapy pracuje ve spojení s modulem pro výběr obchodů a určuje geografická umístění obchodů, které musí být vykresleny na mapě.</span><span class="sxs-lookup"><span data-stu-id="b3188-110">A map module works in conjunction with the store selector module to determine the geographic locations of stores that must be rendered on a map.</span></span> <span data-ttu-id="b3188-111">Selektor úložiště a moduly mapy spolupracují, když uživatel vybere úložiště v jednom z těchto modulů na stránce webu.</span><span class="sxs-lookup"><span data-stu-id="b3188-111">Store selector and map modules interact when a user selects a store in one of those modules on a site page.</span></span> <span data-ttu-id="b3188-112">Moduly mapy lze rozšířit i na další scénáře, mimo interakci s moduly výběru obchodů.</span><span class="sxs-lookup"><span data-stu-id="b3188-112">Map modules can be extended for other scenarios, beyond interaction with store selector modules.</span></span> <span data-ttu-id="b3188-113">Vyžaduje se však přizpůsobení modulu.</span><span class="sxs-lookup"><span data-stu-id="b3188-113">However, module customization is required.</span></span>

> [!NOTE]
> <span data-ttu-id="b3188-114">Mapový modul je k dispozici v Dynamics 365 Commerce vydání 10.0.13.</span><span class="sxs-lookup"><span data-stu-id="b3188-114">The map module is available in the Dynamics 365 Commerce 10.0.13 release.</span></span>

<span data-ttu-id="b3188-115">Následující obrázek ukazuje příklad modulu mapy bloku použitého na stránce umístění obchodu.</span><span class="sxs-lookup"><span data-stu-id="b3188-115">The following image shows an example of a map module that is used on a store locations page.</span></span>

![Příklad modulu volby obchodu](./media/ecommerce-Storelocator.PNG)

## <a name="module-properties"></a><span data-ttu-id="b3188-117">Vlastnosti modulu</span><span class="sxs-lookup"><span data-stu-id="b3188-117">Module properties</span></span>

| <span data-ttu-id="b3188-118">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="b3188-118">Property name</span></span>             | <span data-ttu-id="b3188-119">Hodnota</span><span class="sxs-lookup"><span data-stu-id="b3188-119">Value</span></span>                 | <span data-ttu-id="b3188-120">popis</span><span class="sxs-lookup"><span data-stu-id="b3188-120">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="b3188-121">Nadpis</span><span class="sxs-lookup"><span data-stu-id="b3188-121">Heading</span></span> | <span data-ttu-id="b3188-122">Text</span><span class="sxs-lookup"><span data-stu-id="b3188-122">Text</span></span> | <span data-ttu-id="b3188-123">Nadpis modulu.</span><span class="sxs-lookup"><span data-stu-id="b3188-123">The heading for the module.</span></span> |
| <span data-ttu-id="b3188-124">Možnosti připínáčku: Výchozí ikona</span><span class="sxs-lookup"><span data-stu-id="b3188-124">Pushpin options: Default icon</span></span> | <span data-ttu-id="b3188-125">Obrázek</span><span class="sxs-lookup"><span data-stu-id="b3188-125">Image</span></span> | <span data-ttu-id="b3188-126">Obrázek symbolu připínáčku, který se má použít pro obchody zobrazené na mapě.</span><span class="sxs-lookup"><span data-stu-id="b3188-126">The pushpin symbol image to use for stores that are shown on a map.</span></span> |
| <span data-ttu-id="b3188-127">Možnosti připínáčku: aktivní ikona</span><span class="sxs-lookup"><span data-stu-id="b3188-127">Pushpin options: Active icon</span></span> | <span data-ttu-id="b3188-128">Obrázek</span><span class="sxs-lookup"><span data-stu-id="b3188-128">Image</span></span> | <span data-ttu-id="b3188-129">Obrázek symbolu připínáčku, který se má použít pro obchod vybraný na mapě.</span><span class="sxs-lookup"><span data-stu-id="b3188-129">The pushpin symbol image to use for a store that is selected on a map.</span></span> |
| <span data-ttu-id="b3188-130">Možnosti připínáčku: Barva výchozí ikony</span><span class="sxs-lookup"><span data-stu-id="b3188-130">Pushpin options: Default icon color</span></span> | <span data-ttu-id="b3188-131">Řetězec znaků</span><span class="sxs-lookup"><span data-stu-id="b3188-131">Character string</span></span> | <span data-ttu-id="b3188-132">Text nebo hexadecimální hodnota barvy symbolů připínáčku na mapě.</span><span class="sxs-lookup"><span data-stu-id="b3188-132">The text or hexadecimal value for the color of pushpin symbols on a map.</span></span> |
| <span data-ttu-id="b3188-133">Možnosti připínáčku: barva aktivní ikony</span><span class="sxs-lookup"><span data-stu-id="b3188-133">Pushpin options: Active icon color</span></span> | <span data-ttu-id="b3188-134">Řetězec znaků</span><span class="sxs-lookup"><span data-stu-id="b3188-134">Character string</span></span> | <span data-ttu-id="b3188-135">Textová nebo hexadecimální hodnota barvy vybraných symbolů připínáčku na mapě.</span><span class="sxs-lookup"><span data-stu-id="b3188-135">The text or hexadecimal value for the color of selected pushpin symbols on a map.</span></span> |
| <span data-ttu-id="b3188-136">Zobrazit index</span><span class="sxs-lookup"><span data-stu-id="b3188-136">Show index</span></span> | <span data-ttu-id="b3188-137">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="b3188-137">**True** or **False**</span></span> | <span data-ttu-id="b3188-138">Pokud je tato vlastnost nastavena na **pravda**, každý symbol připínáčku, který označuje obchod, zobrazí index.</span><span class="sxs-lookup"><span data-stu-id="b3188-138">If this property is set to **True**, every pushpin symbol that indicates a store will show an index.</span></span> <span data-ttu-id="b3188-139">Tento index bude odpovídat indexu v zobrazení seznamu, které zobrazuje modul pro výběr úložiště.</span><span class="sxs-lookup"><span data-stu-id="b3188-139">This index will match the index in the list view that the store selector module shows.</span></span> |

## <a name="add-allowed-mapping-urls-to-a-sites-content-security-policy-directives"></a><span data-ttu-id="b3188-140">Přidejte povolené mapovací adresy URL do směrnic zásad zabezpečení obsahu webu</span><span class="sxs-lookup"><span data-stu-id="b3188-140">Add allowed mapping URLs to a site's content security policy directives</span></span>

<span data-ttu-id="b3188-141">Aby modul map pracoval s mapami Bing, musíte zajistit, aby byly povoleny následující adresy URL maování podle zásad zabezpečení obsahu vašeho webu (CSP).</span><span class="sxs-lookup"><span data-stu-id="b3188-141">For the maps module to interact with Bing Maps, you must ensure that the following mapping URLs are allowed per your site's content security policy (CSP).</span></span> <span data-ttu-id="b3188-142">Toto nastavení se provádí v nástroji Commerce site Builder přidáním povolených adres URL do různých směrnic CSP webu (například **img-src**).</span><span class="sxs-lookup"><span data-stu-id="b3188-142">This setup is done in Commerce site builder, by adding allowed URLs to various site CSP directives (for example, **img-src**).</span></span> <span data-ttu-id="b3188-143">Další informace viz [Zásady zabezpečení obsahu](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="b3188-143">For more information, see [Content security policy](manage-csp.md).</span></span> 

- <span data-ttu-id="b3188-144">Do směrnice **connect-src** přidejte **&#42;.bing.com**.</span><span class="sxs-lookup"><span data-stu-id="b3188-144">To the **connect-src** directive, add **&#42;.bing.com**.</span></span>
- <span data-ttu-id="b3188-145">Do směrnice **img-src** přidejte **&#42;.virtualearth.net**.</span><span class="sxs-lookup"><span data-stu-id="b3188-145">To the **img-src** directive, add **&#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="b3188-146">Do směrnice **script-src** přidejte **&#42;.bing.com, &#42;.virtualearth.net**.</span><span class="sxs-lookup"><span data-stu-id="b3188-146">To the **script-src** directive, add **&#42;.bing.com, &#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="b3188-147">Do směrnice **script-src** přidejte **&#42;.bing.com**.</span><span class="sxs-lookup"><span data-stu-id="b3188-147">To the **script style-src** directive, add **&#42;.bing.com**.</span></span>

## <a name="add-a-map-module-to-a-page"></a><span data-ttu-id="b3188-148">Přidání modulu mapy na stránku</span><span class="sxs-lookup"><span data-stu-id="b3188-148">Add a map module to a page</span></span>

<span data-ttu-id="b3188-149">Podrobné informace o konfiguraci modulu mapy na stránce viz [Uložení modulu selektoru](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="b3188-149">For detailed information about how to configure a map module on a page, see [Store selector module](store-selector.md).</span></span> 
 
## <a name="additional-resources"></a><span data-ttu-id="b3188-150">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="b3188-150">Additional resources</span></span>

[<span data-ttu-id="b3188-151">Přehled knihovny modulů</span><span class="sxs-lookup"><span data-stu-id="b3188-151">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="b3188-152">Modul buy boxu</span><span class="sxs-lookup"><span data-stu-id="b3188-152">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="b3188-153">Modul košíku</span><span class="sxs-lookup"><span data-stu-id="b3188-153">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="b3188-154">Modul volby obchodu</span><span class="sxs-lookup"><span data-stu-id="b3188-154">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="b3188-155">Správa map Bing pro vaši organizaci</span><span class="sxs-lookup"><span data-stu-id="b3188-155">Manage Bing Maps for your organization</span></span>](./dev-itpro/manage-bing-maps.md)

[<span data-ttu-id="b3188-156">Webový ovládací prvek Bing Maps V8</span><span class="sxs-lookup"><span data-stu-id="b3188-156">Bing Maps V8 Web Control</span></span>](https://docs.microsoft.com/bingmaps/v8-web-control/)
