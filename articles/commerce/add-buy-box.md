---
title: Modul buy boxu
description: Tohle téma se zabývá moduly buy boxu a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 11/11/2019
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e86b1881e6829ccc33f36ada453af20c1815a2fa
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811134"
---
# <a name="buy-box-module"></a><span data-ttu-id="8ed46-103">Modul buy boxu</span><span class="sxs-lookup"><span data-stu-id="8ed46-103">Buy box module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="8ed46-104">Tohle téma se zabývá moduly buy boxu a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8ed46-104">This topic covers buy box modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="8ed46-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="8ed46-105">Overview</span></span>

<span data-ttu-id="8ed46-106">Termín *buy box* se obvykle vztahuje k oblasti stránky s podrobnostmi o produktu, která se nachází „above the fold“ a která je hostitelem nejdůležitějších informací vyžadovaných k provedení nákupu produktu.</span><span class="sxs-lookup"><span data-stu-id="8ed46-106">The term *buy box* typically refers to the area of a product details page that is "above the fold," and that hosts all the most important information that is required to make a product purchase.</span></span> <span data-ttu-id="8ed46-107">(Oblast „above the fold“ je viditelná po prvním načtení stránky, takže uživatelé nemusejí posouvat zobrazení směrem dolů, aby ji viděli.)</span><span class="sxs-lookup"><span data-stu-id="8ed46-107">(An area that is "above the fold" is visible when the page is first loaded, so that users don't have to scroll down to see it.)</span></span>

<span data-ttu-id="8ed46-108">Modul buy boxu je speciální kontejner, který slouží k hostování všech modulů, které jsou zobrazeny v oblasti buy boxu na stránce podrobností produktu.</span><span class="sxs-lookup"><span data-stu-id="8ed46-108">A buy box module is special container that is used to host all the modules that are shown in the buy box area of a product details page.</span></span>

<span data-ttu-id="8ed46-109">Adresa URL stránky s podrobnostmi o produktu obsahuje ID produktu.</span><span class="sxs-lookup"><span data-stu-id="8ed46-109">The URL of a product details page includes the product ID.</span></span> <span data-ttu-id="8ed46-110">Všechny informace, které jsou požadovány pro vygenerování modulu buy boxu, jsou odvozeny z tohoto ID produktu.</span><span class="sxs-lookup"><span data-stu-id="8ed46-110">All the information that is required to render a buy box module is derived from this product ID.</span></span> <span data-ttu-id="8ed46-111">Není-li zadáno ID produktu, nebude modul buy boxu na stránce správně vykreslen.</span><span class="sxs-lookup"><span data-stu-id="8ed46-111">If a product ID isn't provided, the buy box module won't be rendered correctly on a page.</span></span> <span data-ttu-id="8ed46-112">Proto nelze použít modul buy boxu na žádné stránce, která nemá kontext produktu (například domovská stránka nebo marketingová stránka).</span><span class="sxs-lookup"><span data-stu-id="8ed46-112">Therefore, a buy box module can't be used on any page that doesn't have product context (for example, a home page or a marketing page).</span></span>

## <a name="buy-box-module-properties-and-slots"></a><span data-ttu-id="8ed46-113">Vlastnosti a pozice modulu buy boxu</span><span class="sxs-lookup"><span data-stu-id="8ed46-113">Buy box module properties and slots</span></span> 

<span data-ttu-id="8ed46-114">Coby kontejner řídí modul buy boxu některé základní vlastnosti, jako je například šířka.</span><span class="sxs-lookup"><span data-stu-id="8ed46-114">As a container, a buy box module controls some basic properties, such as the width.</span></span> <span data-ttu-id="8ed46-115">Nastavení šířky určuje, zda se moduly uvnitř kontejneru musí vejít do tohoto kontejneru nebo zda mohou vyplnit obrazovku.</span><span class="sxs-lookup"><span data-stu-id="8ed46-115">The width setting determines whether the modules inside the container must fit within that container, or whether they can fill the screen.</span></span>

<span data-ttu-id="8ed46-116">Na stránce s podrobnostmi o produktu je buy box rozdělen na dvě oblasti: oblast médií v levé části a oblast obsahu vpravo.</span><span class="sxs-lookup"><span data-stu-id="8ed46-116">On a product details page, a buy box is divided into two regions: a media region on the left and a content region on the right.</span></span> <span data-ttu-id="8ed46-117">Tyto dvě oblasti jsou reprezentovány pozicemi v modulu buy boxu.</span><span class="sxs-lookup"><span data-stu-id="8ed46-117">These two regions are represented by slots in the buy box module.</span></span> <span data-ttu-id="8ed46-118">Každá pozice je předem nakonfigurována tak, aby přijímala pouze určité moduly, které jsou v pozici podporovány.</span><span class="sxs-lookup"><span data-stu-id="8ed46-118">Each slot is preconfigured to accept only specific modules that are supported by the slot.</span></span> <span data-ttu-id="8ed46-119">Například pozice **Média** podporuje pouze modul galerie médií.</span><span class="sxs-lookup"><span data-stu-id="8ed46-119">For example, a **Media** slot supports only the media gallery module.</span></span>

<span data-ttu-id="8ed46-120">Standardně je poměr šířek sloupců pro oblast médií a oblast obsahu 2:1.</span><span class="sxs-lookup"><span data-stu-id="8ed46-120">By default, the ratio of column widths for the media region and the content region is 2:1.</span></span> <span data-ttu-id="8ed46-121">Šířku sloupců však může být přepsána motivem.</span><span class="sxs-lookup"><span data-stu-id="8ed46-121">However, the column widths can be overridden by the theme.</span></span> <span data-ttu-id="8ed46-122">Kromě toho jsou na mobilních zařízeních obě oblasti navrstveny, takže se jedna oblast zobrazí pod druhou oblastí.</span><span class="sxs-lookup"><span data-stu-id="8ed46-122">In addition, on mobile devices, the two regions are stacked, so that one region appears below the other region.</span></span>

## <a name="modules-that-can-be-used-in-a-buy-box-module"></a><span data-ttu-id="8ed46-123">Moduly, které lze použít v modulu buy boxu</span><span class="sxs-lookup"><span data-stu-id="8ed46-123">Modules that can be used in a buy box module</span></span>

- <span data-ttu-id="8ed46-124">**Galerie médií** – Tento modul slouží k předvedení obrázků produktu na stránce s podrobnostmi o produktu.</span><span class="sxs-lookup"><span data-stu-id="8ed46-124">**Media gallery** – This module is used to showcase images of a product on a product details page.</span></span> <span data-ttu-id="8ed46-125">Může podporovat jeden nebo mnoho obrázků.</span><span class="sxs-lookup"><span data-stu-id="8ed46-125">It can support one to many images.</span></span> <span data-ttu-id="8ed46-126">Podporuje také obrázky miniatur.</span><span class="sxs-lookup"><span data-stu-id="8ed46-126">It also supports thumbnail images.</span></span> <span data-ttu-id="8ed46-127">Obrázky miniatur lze uspořádat vodorovně (jako řádek pod obrázkem) nebo svisle (jako sloupec vedle obrázku).</span><span class="sxs-lookup"><span data-stu-id="8ed46-127">The thumbnail images can be arranged either horizontally (as a row below the image) or vertically (as a column next to the image).</span></span> <span data-ttu-id="8ed46-128">Modul galerie médií lze přidat do pozice **Média** v modulu buy boxu.</span><span class="sxs-lookup"><span data-stu-id="8ed46-128">The media gallery module can be added to the **Media** slot in the buy box module.</span></span> <span data-ttu-id="8ed46-129">V současné době podporuje pouze obrázky a videa.</span><span class="sxs-lookup"><span data-stu-id="8ed46-129">It currently supports only images and videos.</span></span>
- <span data-ttu-id="8ed46-130">**Název produktu** – Tento modul zobrazuje název produktu na stránce podrobností produktu.</span><span class="sxs-lookup"><span data-stu-id="8ed46-130">**Product title** – This module shows the title of the product on a product details page.</span></span> <span data-ttu-id="8ed46-131">Standardně je použita značka nadpisu **H1**, ale značku nadpisu lze podle potřeby změnit.</span><span class="sxs-lookup"><span data-stu-id="8ed46-131">By default, the **H1** heading tag is used, but the heading tag can be changed as required.</span></span>
- <span data-ttu-id="8ed46-132">**Hodnocení produktu** – Tento modul zobrazuje hodnocení pomocí hvězdiček na základě zákaznického hodnocení produktu.</span><span class="sxs-lookup"><span data-stu-id="8ed46-132">**Product rating** – This module shows star ratings, based on customer ratings for a product.</span></span> <span data-ttu-id="8ed46-133">Modul buy boxu načte hodnocení produktu pro jednotlivé produkty ze služby hodnocení.</span><span class="sxs-lookup"><span data-stu-id="8ed46-133">The buy box module retrieves the product ratings for each product from the ratings service.</span></span>
- <span data-ttu-id="8ed46-134">**Cena produktu** – Tento modul zobrazuje cenu produktu.</span><span class="sxs-lookup"><span data-stu-id="8ed46-134">**Product price** – This module shows the price of the product.</span></span> <span data-ttu-id="8ed46-135">Cena zahrnuje přeškrtnuté ceny a slevy.</span><span class="sxs-lookup"><span data-stu-id="8ed46-135">The price includes strikethrough prices and discounts.</span></span>
- <span data-ttu-id="8ed46-136">**Popis produktu** – Tento modul zobrazuje popis produktu.</span><span class="sxs-lookup"><span data-stu-id="8ed46-136">**Product description** – This module shows the description of the product.</span></span>
- <span data-ttu-id="8ed46-137">**Konfigurace produktu** – Tento modul zobrazuje velikost, styl a rozměry produktu.</span><span class="sxs-lookup"><span data-stu-id="8ed46-137">**Product configure** – This module shows the size, style, and dimensions of the product.</span></span> <span data-ttu-id="8ed46-138">Selektory rozměrů lze skládat svisle nebo je možné je zobrazit vedle sebe.</span><span class="sxs-lookup"><span data-stu-id="8ed46-138">The dimension selectors can be stacked vertically, or they can appear side by side.</span></span> <span data-ttu-id="8ed46-139">Je-li vybrána varianta produktu, budou další vlastnosti v buy boxu (například popis a obrázky produktu) aktualizovány tak, aby odrážely informace o variantách.</span><span class="sxs-lookup"><span data-stu-id="8ed46-139">When a product variant is selected, other properties in the buy box (for example, the product description and images) are updated to reflect the variant information.</span></span>
- <span data-ttu-id="8ed46-140">**Množství produktu** – Tento modul se používá ke konfiguraci množství produktu.</span><span class="sxs-lookup"><span data-stu-id="8ed46-140">**Product quantity** – This module is used to configure the quantity of the product.</span></span> <span data-ttu-id="8ed46-141">Nastavení omezuje množství produktu nebo varianty, které lze přidat do nákupního košíku.</span><span class="sxs-lookup"><span data-stu-id="8ed46-141">A setting limits the quantity of a product or variant that can be added to the cart.</span></span>
- <span data-ttu-id="8ed46-142">**Přidat do nákupního košíku** – Tento modul slouží k provedení akce „Přidat do košíku“.</span><span class="sxs-lookup"><span data-stu-id="8ed46-142">**Add to cart** – This module is used to perform the "add to the cart" action.</span></span> <span data-ttu-id="8ed46-143">Do nákupního košíku lze přidat pouze produkt nebo variantu.</span><span class="sxs-lookup"><span data-stu-id="8ed46-143">Only a product or a variant can be added to the cart.</span></span> <span data-ttu-id="8ed46-144">Jinými slovy, hlavní produkt nelze přidat do košíku.</span><span class="sxs-lookup"><span data-stu-id="8ed46-144">In other words, a master product can't be added to the cart.</span></span> <span data-ttu-id="8ed46-145">Modul obsahuje vlastnost **Přejít do nákupního košíku**, kterou může nastavit autor webu.</span><span class="sxs-lookup"><span data-stu-id="8ed46-145">The module has a **Navigate to cart** property that the site author can set.</span></span> <span data-ttu-id="8ed46-146">Je-li tato vlastnost nastavena na hodnotu **Pravda**, uživatel je přesměrován na stránku nákupního košíku vždy, když je aktivována akce „Přidat do košíku“.</span><span class="sxs-lookup"><span data-stu-id="8ed46-146">When this property is set to **True**, the user is taken to the cart page every time that an "add to the cart" action is triggered.</span></span> <span data-ttu-id="8ed46-147">Je-li nastavena na hodnotu **Nepravda**, může zákazník pokračovat v procházení stránky s podrobnostmi o produktu po přidání položek do nákupního košíku.</span><span class="sxs-lookup"><span data-stu-id="8ed46-147">When it's set to **False**, the customer can continue to browse on the product details page after items are added to the cart.</span></span>
- <span data-ttu-id="8ed46-148">**Přidat do seznamu přání** – Tento modul slouží k přidání položky do seznamu přání odběratele.</span><span class="sxs-lookup"><span data-stu-id="8ed46-148">**Add to wish list** – This module is used to add an item to the customer's wish list.</span></span> <span data-ttu-id="8ed46-149">Do seznamu přání lze přidat pouze produkt nebo variantu.</span><span class="sxs-lookup"><span data-stu-id="8ed46-149">Only a product or a variant can be added to a wish list.</span></span> <span data-ttu-id="8ed46-150">Dále je nutné, aby byl zákazník přihlášen k danému webu.</span><span class="sxs-lookup"><span data-stu-id="8ed46-150">Additionally, the customer must be signed in to the site.</span></span> <span data-ttu-id="8ed46-151">Modul zahrnuje logiku zpracování chyb, aby bylo zajištěno, že obě tyto podmínky budou splněny.</span><span class="sxs-lookup"><span data-stu-id="8ed46-151">The module includes error handling logic to make sure that both these conditions are met.</span></span>
- <span data-ttu-id="8ed46-152">**Hledat v obchodě** – Tento modul aktivuje tok „koupit online, vyzvednout v obchodě“.</span><span class="sxs-lookup"><span data-stu-id="8ed46-152">**Find in store** – This module triggers the "buy online, pick up in store" flow.</span></span>
- <span data-ttu-id="8ed46-153">**Vyzvednout v obchodě** – Tento modul zobrazuje seznam obchodů, které jsou poblíž a kde je položka k výdeji.</span><span class="sxs-lookup"><span data-stu-id="8ed46-153">**Pick up in store** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="8ed46-154">Standardně tento modul zobrazuje obchody, které jsou v okruhu 80 km umístění zákazníka.</span><span class="sxs-lookup"><span data-stu-id="8ed46-154">By default, this module shows stores that are within a 50-mile radius of the customer's location.</span></span> <span data-ttu-id="8ed46-155">Okruh hledání však můžete upravit v modulu.</span><span class="sxs-lookup"><span data-stu-id="8ed46-155">However, the search radius can be customized in the module.</span></span> <span data-ttu-id="8ed46-156">U každého obchodu se provádí kontrola zásob, je-li zapnuta funkce kontroly zásob a je zobrazena odpovídající zpráva na skladě nebo není na skladě.</span><span class="sxs-lookup"><span data-stu-id="8ed46-156">For each store, an inventory check is done, if the inventory check functionality is turned on, and an appropriate in-stock or out-of-stock message is shown.</span></span>
- <span data-ttu-id="8ed46-157">**Hledání obchodů v mapách Bing** – Tento modul lze použít uvnitř modulu vyzvednutí v obchodě.</span><span class="sxs-lookup"><span data-stu-id="8ed46-157">**Store search by Bing Maps** – This module can be used inside the pick up in store module.</span></span> <span data-ttu-id="8ed46-158">Umožňuje zákazníkům vyhledávat obchody zadáním umístění.</span><span class="sxs-lookup"><span data-stu-id="8ed46-158">It lets customers search for stores by entering a location.</span></span> <span data-ttu-id="8ed46-159">Programovací rozhraní (API) pro aplikaci geokódování služby Mapy Bing, které slouží k převodu zadaného umístění na zeměpisnou šířku a délku.</span><span class="sxs-lookup"><span data-stu-id="8ed46-159">The Bing Maps geocoding application programming interface (API) is used to convert the specified location to a latitude and a longitude.</span></span> <span data-ttu-id="8ed46-160">Je-li použit tento modul, zobrazí se pouze obchody, které jsou poblíž aktuálního umístění zákazníka, a zákazník nebude moci vyhledat jiné umístění.</span><span class="sxs-lookup"><span data-stu-id="8ed46-160">If this module is used, only stores that are near the customer's current location are shown, and the customer can't search for a different location.</span></span>
- <span data-ttu-id="8ed46-161">**Blok s formátovaným obsahem** – Tento modul může zobrazit zprávu, kterou autor webu nebo prodejce chce umístit do buy boxu, například „Při problémech s objednávkou volejte 123 456 789“ nebo „Poštovné zdarma při objednávce nad 1000 Kč“.</span><span class="sxs-lookup"><span data-stu-id="8ed46-161">**Content rich block** – This module can show a message that the site author or retailer wants to promote in the buy box, such as "For issues with order, contact 1-800-FABRIKAM" or "Free shipping on orders over $100."</span></span> <span data-ttu-id="8ed46-162">Zprávy řídí systém správy obsahu (CMS).</span><span class="sxs-lookup"><span data-stu-id="8ed46-162">The messages are driven by the content management system (CMS).</span></span>

## <a name="buy-box-module-settings"></a><span data-ttu-id="8ed46-163">Nastavení modulu buy boxu</span><span class="sxs-lookup"><span data-stu-id="8ed46-163">Buy box module settings</span></span>

<span data-ttu-id="8ed46-164">Moduly buy boxu mají tři nastavení, která lze konfigurovat:</span><span class="sxs-lookup"><span data-stu-id="8ed46-164">Buy box modules have three settings that can be configured:</span></span>

- <span data-ttu-id="8ed46-165">**Maximální množství** – Maximální počet jednotlivých položek, které lze přidat do nákupního košíku.</span><span class="sxs-lookup"><span data-stu-id="8ed46-165">**Maximum quantity** – The maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="8ed46-166">Maloobchodní prodejce může například rozhodnout, že v jedné transakci lze prodávat pouze 10 jednotlivých produktů.</span><span class="sxs-lookup"><span data-stu-id="8ed46-166">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="8ed46-167">**Kontrola zásob** – Je-li nastavena hodnota **Pravda**, položka se přidá do košíku pouze poté, co se modul buy boxu ověří, že je na skladě.</span><span class="sxs-lookup"><span data-stu-id="8ed46-167">**Inventory check** – When the value is set to **True**, an item is added to the cart only after the buy box module makes sure that it's in stock.</span></span> <span data-ttu-id="8ed46-168">Tato kontrola zásob se provádí pro scénáře, když má být položka expedována, a pro scénáře, kdy má být vyzvednuta v obchodě.</span><span class="sxs-lookup"><span data-stu-id="8ed46-168">This inventory check is done both for scenarios where the item will be shipped and for scenarios where it will be picked up in the store.</span></span> <span data-ttu-id="8ed46-169">Je-li tato hodnota nastavena na hodnotu **Nepravda**, před přidáním položky do nákupního košíku a podání objednávky není provedena kontrola zásob.</span><span class="sxs-lookup"><span data-stu-id="8ed46-169">If the value is set to **False**, no inventory check is done before an item is added to the cart and the order is placed.</span></span>
- <span data-ttu-id="8ed46-170">**Zásboník zásob** – Údržba zásob probíhá v reálném čase a když mnoho zákazníků podá objednávku, může být obtížné zajistit přesný počet zásob.</span><span class="sxs-lookup"><span data-stu-id="8ed46-170">**Inventory buffer** – Inventory is maintained in real time, and when many customers place orders, it can be difficult to maintain an accurate inventory count.</span></span> <span data-ttu-id="8ed46-171">Proto lze pro zásoby definovat zásobník.</span><span class="sxs-lookup"><span data-stu-id="8ed46-171">Therefore, a buffer can be defined for inventory.</span></span> <span data-ttu-id="8ed46-172">Když je provedena kontrola zásob, pokud je množství na skladu nižší než množství zásobníku, produkt je brán, jakože není na skladu.</span><span class="sxs-lookup"><span data-stu-id="8ed46-172">When an inventory check is done, if the inventory is less than the buffer amount, the product is treated as out of stock.</span></span> <span data-ttu-id="8ed46-173">Pokud se tedy prodej rychle točí prostřednictvím několika kanálů, takže zásoby nejsou plně synchronizovány, existuje menší riziko, že položka, která se nenachází na skladě, je v prodeji.</span><span class="sxs-lookup"><span data-stu-id="8ed46-173">Therefore, when sales occur quickly through several channels, so that the inventory count isn't fully synced, there is less risk that an item that is out of stock will be sold.</span></span>

## <a name="retail-server-interaction"></a><span data-ttu-id="8ed46-174">Interakce se serverem maloobchodu</span><span class="sxs-lookup"><span data-stu-id="8ed46-174">Retail server interaction</span></span>

<span data-ttu-id="8ed46-175">Modul buy boxu načítá informace o produktu pomocí rozhraní API serveru maloobchodu.</span><span class="sxs-lookup"><span data-stu-id="8ed46-175">The buy box module retrieves product information using Retail Server APIs.</span></span> <span data-ttu-id="8ed46-176">ID produktu ze stránky s podrobnostmi o produktu slouží k načtení všech informací.</span><span class="sxs-lookup"><span data-stu-id="8ed46-176">The product ID from the product details page is used to retrieve all information.</span></span>

## <a name="add-a-buy-box-module-to-a-page"></a><span data-ttu-id="8ed46-177">Přidání modulu buy boxu na stránku</span><span class="sxs-lookup"><span data-stu-id="8ed46-177">Add a buy box module to a page</span></span>

<span data-ttu-id="8ed46-178">Chcete-li přidat modul buy boxu na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="8ed46-178">To add a buy box module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="8ed46-179">Vytvořte fragment s názvem **Fragment buy boxu** a do něj přidejte modul buy boxu.</span><span class="sxs-lookup"><span data-stu-id="8ed46-179">Create a fragment that is named **buy box fragment**, and add a buy box module to it.</span></span>
1. <span data-ttu-id="8ed46-180">Do pozice **Média** modulu buy boxu přidejte modul galerie médií.</span><span class="sxs-lookup"><span data-stu-id="8ed46-180">In the **Media** slot of the buy box module, add a media gallery module.</span></span>
1. <span data-ttu-id="8ed46-181">Do pozice **Obsah** modulu buy boxu přidejte následující moduly: název produktu, hodnocení produktu, cena produktu, popis produktu, konfigurace produktu, přidat do košíku, přidat do seznamu přání a hledat v obchodě.</span><span class="sxs-lookup"><span data-stu-id="8ed46-181">In the **Content** slot of the buy box module, add the following modules: product title, product rating, product price, product description, product configure, add to cart, add to wish list, and find in store.</span></span> <span data-ttu-id="8ed46-182">Rozložení modulů v pozici **Obsah** můžete dle libosti změnit.</span><span class="sxs-lookup"><span data-stu-id="8ed46-182">You can rearrange the modules in the **Content** slot to achieve the desired layout.</span></span>
1. <span data-ttu-id="8ed46-183">Vyberte modul pro vyhledání v obchodě.</span><span class="sxs-lookup"><span data-stu-id="8ed46-183">Select the find in store module.</span></span> <span data-ttu-id="8ed46-184">V pozici uvnitř tohoto modulu přidejte modul pro vyzvednutí v obchodě.</span><span class="sxs-lookup"><span data-stu-id="8ed46-184">In the slot inside this module, add a pick up in store module.</span></span>
1. <span data-ttu-id="8ed46-185">V pozici uvnitř modulu vyzvednutí v obchodě přidejte modul hledání obchodů v mapách Bing.</span><span class="sxs-lookup"><span data-stu-id="8ed46-185">In the slot inside the pick up in store module, add a store search by Bing Maps module.</span></span>
1. <span data-ttu-id="8ed46-186">Vraťte stránku se změnami a publikujte ji.</span><span class="sxs-lookup"><span data-stu-id="8ed46-186">Check in the page, and publish it.</span></span>
1. <span data-ttu-id="8ed46-187">Vytvořte šablonu pro stránku s podrobnostmi o produktu a pojmenujte ji **Šablona POP**.</span><span class="sxs-lookup"><span data-stu-id="8ed46-187">Create a template for a product details page, and name it **PDP template**.</span></span>
1. <span data-ttu-id="8ed46-188">Přidejte výchozí stránku.</span><span class="sxs-lookup"><span data-stu-id="8ed46-188">Add a default page.</span></span>
1. <span data-ttu-id="8ed46-189">V pozici **Hlavní** na výchozí stránce přidejte fragment buy boxu.</span><span class="sxs-lookup"><span data-stu-id="8ed46-189">In the **Main** slot of the default page, add a buy box fragment.</span></span>
1. <span data-ttu-id="8ed46-190">Uložte šablonu, vraťte ji se změnami a publikujte.</span><span class="sxs-lookup"><span data-stu-id="8ed46-190">Save the template, check it in, and publish it.</span></span>
1. <span data-ttu-id="8ed46-191">Šablonu, kterou jste právě vytvořili, použijte pro vytvoření stránky s názvem **Stránka POP**.</span><span class="sxs-lookup"><span data-stu-id="8ed46-191">Use the template that you just created to create a page that is named **PDP page**.</span></span>
1. <span data-ttu-id="8ed46-192">V pozici **Hlavní** nové stránky přidejte fragment buy boxu.</span><span class="sxs-lookup"><span data-stu-id="8ed46-192">In the **Main** slot of the new page, add a buy box fragment.</span></span>
1. <span data-ttu-id="8ed46-193">Uložte stránku a zobrazte náhled.</span><span class="sxs-lookup"><span data-stu-id="8ed46-193">Save and preview the page.</span></span> <span data-ttu-id="8ed46-194">Do adresy URL stránky náhledu přidejte parametr řetězce dotazu **?productid=&lt;id produktu&gt;**.</span><span class="sxs-lookup"><span data-stu-id="8ed46-194">Add the **?productid=&lt;product id&gt;** query string parameter to the URL of the preview page.</span></span> <span data-ttu-id="8ed46-195">Tímto způsobem se pro načtení a vykreslení stránky náhledu použije kontext produktu.</span><span class="sxs-lookup"><span data-stu-id="8ed46-195">In that way, the product context is used to load and render the preview page.</span></span>
1. <span data-ttu-id="8ed46-196">Vraťte stránku se změnami a publikujte ji.</span><span class="sxs-lookup"><span data-stu-id="8ed46-196">Check in the page, and publish it.</span></span> <span data-ttu-id="8ed46-197">Na stránce s podrobnostmi o produktu by se měl zobrazit buy box.</span><span class="sxs-lookup"><span data-stu-id="8ed46-197">A buy box should appear on the product details page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8ed46-198">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="8ed46-198">Additional resources</span></span>

[<span data-ttu-id="8ed46-199">Přehled startovací sady</span><span class="sxs-lookup"><span data-stu-id="8ed46-199">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="8ed46-200">Modul kontejneru</span><span class="sxs-lookup"><span data-stu-id="8ed46-200">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="8ed46-201">Modul košíku</span><span class="sxs-lookup"><span data-stu-id="8ed46-201">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="8ed46-202">Modul pokladny</span><span class="sxs-lookup"><span data-stu-id="8ed46-202">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="8ed46-203">Modul potvrzení objednávky</span><span class="sxs-lookup"><span data-stu-id="8ed46-203">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="8ed46-204">Modul záhlaví</span><span class="sxs-lookup"><span data-stu-id="8ed46-204">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="8ed46-205">Modul zápatí</span><span class="sxs-lookup"><span data-stu-id="8ed46-205">Footer module</span></span>](author-footer-module.md)