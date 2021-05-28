---
title: Modul mapy
description: Toto téma popisuje moduly mapy a popisuje, jak je konfigurovat v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 659211f3a74c38389f991cd2385366d175b0c7c0
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020252"
---
# <a name="map-module"></a><span data-ttu-id="4aee1-103">Modul mapy</span><span class="sxs-lookup"><span data-stu-id="4aee1-103">Map module</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="4aee1-104">Toto téma popisuje moduly mapy a popisuje, jak je konfigurovat v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4aee1-104">This topic covers map modules and describes how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="4aee1-105">Modul mapy zobrazuje umístění obchodů na interaktivní mapě, která je vykreslena pomocí [webového ovládacího prvku Bing Maps V8](/bingmaps/v8-web-control/).</span><span class="sxs-lookup"><span data-stu-id="4aee1-105">A map module shows the locations of stores on an interactive map that is rendered by using the [Bing Maps V8 Web Control](/bingmaps/v8-web-control/).</span></span> <span data-ttu-id="4aee1-106">Klíč rozhraní API mapy služby Bing je povinný a musí být přidán do stránky se sdílenými parametry pro centrálu Commerce.</span><span class="sxs-lookup"><span data-stu-id="4aee1-106">A Bing Maps API key is required and must be added to the shared parameters page in Commerce headquarters.</span></span> <span data-ttu-id="4aee1-107">Moduly mapy poskytují různá zobrazení, jako jsou silniční, anténní a pouliční, které si uživatelé mohou vybrat pro zobrazení polohy na mapě.</span><span class="sxs-lookup"><span data-stu-id="4aee1-107">Map modules provide different views, such as Road, Aerial, and Streetside, that users can select to view map locations.</span></span> <span data-ttu-id="4aee1-108">Umožňují také interakce, jako je přibližování a používání polohy uživatele.</span><span class="sxs-lookup"><span data-stu-id="4aee1-108">They also allow for interactions such as zooming and using the user's location.</span></span>

<span data-ttu-id="4aee1-109">Modul mapy pracuje ve spojení s modulem pro výběr obchodů a určuje geografická umístění obchodů, které musí být vykresleny na mapě.</span><span class="sxs-lookup"><span data-stu-id="4aee1-109">A map module works in conjunction with the store selector module to determine the geographic locations of stores that must be rendered on a map.</span></span> <span data-ttu-id="4aee1-110">Selektor úložiště a moduly mapy spolupracují, když uživatel vybere úložiště v jednom z těchto modulů na stránce webu.</span><span class="sxs-lookup"><span data-stu-id="4aee1-110">Store selector and map modules interact when a user selects a store in one of those modules on a site page.</span></span> <span data-ttu-id="4aee1-111">Moduly mapy lze rozšířit i na další scénáře, mimo interakci s moduly výběru obchodů.</span><span class="sxs-lookup"><span data-stu-id="4aee1-111">Map modules can be extended for other scenarios, beyond interaction with store selector modules.</span></span> <span data-ttu-id="4aee1-112">Vyžaduje se však přizpůsobení modulu.</span><span class="sxs-lookup"><span data-stu-id="4aee1-112">However, module customization is required.</span></span>

> [!NOTE]
> <span data-ttu-id="4aee1-113">Mapový modul je k dispozici v Dynamics 365 Commerce vydání 10.0.13.</span><span class="sxs-lookup"><span data-stu-id="4aee1-113">The map module is available in the Dynamics 365 Commerce 10.0.13 release.</span></span>

<span data-ttu-id="4aee1-114">Následující obrázek ukazuje příklad modulu mapy bloku použitého na stránce umístění obchodu.</span><span class="sxs-lookup"><span data-stu-id="4aee1-114">The following image shows an example of a map module that is used on a store locations page.</span></span>

![Příklad modulu volby obchodu](./media/ecommerce-Storelocator.PNG)

## <a name="module-properties"></a><span data-ttu-id="4aee1-116">Vlastnosti modulu</span><span class="sxs-lookup"><span data-stu-id="4aee1-116">Module properties</span></span>

| <span data-ttu-id="4aee1-117">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="4aee1-117">Property name</span></span>             | <span data-ttu-id="4aee1-118">Hodnota</span><span class="sxs-lookup"><span data-stu-id="4aee1-118">Value</span></span>                 | <span data-ttu-id="4aee1-119">popis</span><span class="sxs-lookup"><span data-stu-id="4aee1-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="4aee1-120">Nadpis</span><span class="sxs-lookup"><span data-stu-id="4aee1-120">Heading</span></span> | <span data-ttu-id="4aee1-121">Text</span><span class="sxs-lookup"><span data-stu-id="4aee1-121">Text</span></span> | <span data-ttu-id="4aee1-122">Nadpis modulu.</span><span class="sxs-lookup"><span data-stu-id="4aee1-122">The heading for the module.</span></span> |
| <span data-ttu-id="4aee1-123">Možnosti připínáčku: Výchozí ikona</span><span class="sxs-lookup"><span data-stu-id="4aee1-123">Pushpin options: Default icon</span></span> | <span data-ttu-id="4aee1-124">Obrázek</span><span class="sxs-lookup"><span data-stu-id="4aee1-124">Image</span></span> | <span data-ttu-id="4aee1-125">Obrázek symbolu připínáčku, který se má použít pro obchody zobrazené na mapě.</span><span class="sxs-lookup"><span data-stu-id="4aee1-125">The pushpin symbol image to use for stores that are shown on a map.</span></span> |
| <span data-ttu-id="4aee1-126">Možnosti připínáčku: aktivní ikona</span><span class="sxs-lookup"><span data-stu-id="4aee1-126">Pushpin options: Active icon</span></span> | <span data-ttu-id="4aee1-127">Obrázek</span><span class="sxs-lookup"><span data-stu-id="4aee1-127">Image</span></span> | <span data-ttu-id="4aee1-128">Obrázek symbolu připínáčku, který se má použít pro obchod vybraný na mapě.</span><span class="sxs-lookup"><span data-stu-id="4aee1-128">The pushpin symbol image to use for a store that is selected on a map.</span></span> |
| <span data-ttu-id="4aee1-129">Možnosti připínáčku: Barva výchozí ikony</span><span class="sxs-lookup"><span data-stu-id="4aee1-129">Pushpin options: Default icon color</span></span> | <span data-ttu-id="4aee1-130">Řetězec znaků</span><span class="sxs-lookup"><span data-stu-id="4aee1-130">Character string</span></span> | <span data-ttu-id="4aee1-131">Text nebo hexadecimální hodnota barvy symbolů připínáčku na mapě.</span><span class="sxs-lookup"><span data-stu-id="4aee1-131">The text or hexadecimal value for the color of pushpin symbols on a map.</span></span> |
| <span data-ttu-id="4aee1-132">Možnosti připínáčku: barva aktivní ikony</span><span class="sxs-lookup"><span data-stu-id="4aee1-132">Pushpin options: Active icon color</span></span> | <span data-ttu-id="4aee1-133">Řetězec znaků</span><span class="sxs-lookup"><span data-stu-id="4aee1-133">Character string</span></span> | <span data-ttu-id="4aee1-134">Textová nebo hexadecimální hodnota barvy vybraných symbolů připínáčku na mapě.</span><span class="sxs-lookup"><span data-stu-id="4aee1-134">The text or hexadecimal value for the color of selected pushpin symbols on a map.</span></span> |
| <span data-ttu-id="4aee1-135">Zobrazit index</span><span class="sxs-lookup"><span data-stu-id="4aee1-135">Show index</span></span> | <span data-ttu-id="4aee1-136">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="4aee1-136">**True** or **False**</span></span> | <span data-ttu-id="4aee1-137">Pokud je tato vlastnost nastavena na **pravda**, každý symbol připínáčku, který označuje obchod, zobrazí index.</span><span class="sxs-lookup"><span data-stu-id="4aee1-137">If this property is set to **True**, every pushpin symbol that indicates a store will show an index.</span></span> <span data-ttu-id="4aee1-138">Tento index bude odpovídat indexu v zobrazení seznamu, které zobrazuje modul pro výběr úložiště.</span><span class="sxs-lookup"><span data-stu-id="4aee1-138">This index will match the index in the list view that the store selector module shows.</span></span> |

## <a name="add-allowed-mapping-urls-to-a-sites-content-security-policy-directives"></a><span data-ttu-id="4aee1-139">Přidejte povolené mapovací adresy URL do směrnic zásad zabezpečení obsahu webu</span><span class="sxs-lookup"><span data-stu-id="4aee1-139">Add allowed mapping URLs to a site's content security policy directives</span></span>

<span data-ttu-id="4aee1-140">Aby modul map pracoval s mapami Bing, musíte zajistit, aby byly povoleny následující adresy URL maování podle zásad zabezpečení obsahu vašeho webu (CSP).</span><span class="sxs-lookup"><span data-stu-id="4aee1-140">For the maps module to interact with Bing Maps, you must ensure that the following mapping URLs are allowed per your site's content security policy (CSP).</span></span> <span data-ttu-id="4aee1-141">Toto nastavení se provádí v nástroji Commerce site Builder přidáním povolených adres URL do různých směrnic CSP webu (například **img-src**).</span><span class="sxs-lookup"><span data-stu-id="4aee1-141">This setup is done in Commerce site builder, by adding allowed URLs to various site CSP directives (for example, **img-src**).</span></span> <span data-ttu-id="4aee1-142">Další informace viz [Zásady zabezpečení obsahu](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="4aee1-142">For more information, see [Content security policy](manage-csp.md).</span></span> 

- <span data-ttu-id="4aee1-143">Do směrnice **connect-src** přidejte **&#42;.bing.com**.</span><span class="sxs-lookup"><span data-stu-id="4aee1-143">To the **connect-src** directive, add **&#42;.bing.com**.</span></span>
- <span data-ttu-id="4aee1-144">Do směrnice **img-src** přidejte **&#42;.virtualearth.net**.</span><span class="sxs-lookup"><span data-stu-id="4aee1-144">To the **img-src** directive, add **&#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="4aee1-145">Do směrnice **script-src** přidejte **&#42;.bing.com, &#42;.virtualearth.net**.</span><span class="sxs-lookup"><span data-stu-id="4aee1-145">To the **script-src** directive, add **&#42;.bing.com, &#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="4aee1-146">Do směrnice **script-src** přidejte **&#42;.bing.com**.</span><span class="sxs-lookup"><span data-stu-id="4aee1-146">To the **script style-src** directive, add **&#42;.bing.com**.</span></span>

## <a name="add-a-map-module-to-a-page"></a><span data-ttu-id="4aee1-147">Přidání modulu mapy na stránku</span><span class="sxs-lookup"><span data-stu-id="4aee1-147">Add a map module to a page</span></span>

<span data-ttu-id="4aee1-148">Podrobné informace o konfiguraci modulu mapy na stránce viz [Uložení modulu selektoru](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="4aee1-148">For detailed information about how to configure a map module on a page, see [Store selector module](store-selector.md).</span></span> 
 
## <a name="additional-resources"></a><span data-ttu-id="4aee1-149">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="4aee1-149">Additional resources</span></span>

[<span data-ttu-id="4aee1-150">Přehled knihovny modulů</span><span class="sxs-lookup"><span data-stu-id="4aee1-150">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="4aee1-151">Modul buy boxu</span><span class="sxs-lookup"><span data-stu-id="4aee1-151">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="4aee1-152">Modul košíku</span><span class="sxs-lookup"><span data-stu-id="4aee1-152">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="4aee1-153">Modul volby obchodu</span><span class="sxs-lookup"><span data-stu-id="4aee1-153">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="4aee1-154">Správa map Bing pro vaši organizaci</span><span class="sxs-lookup"><span data-stu-id="4aee1-154">Manage Bing Maps for your organization</span></span>](./dev-itpro/manage-bing-maps.md)

[<span data-ttu-id="4aee1-155">Webový ovládací prvek Bing Maps V8</span><span class="sxs-lookup"><span data-stu-id="4aee1-155">Bing Maps V8 Web Control</span></span>](/bingmaps/v8-web-control/)


[!INCLUDE[footer-include](../includes/footer-banner.md)]