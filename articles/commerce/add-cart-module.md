---
title: Modul košíku
description: Tohle téma se zabývá moduly košíku a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 04/13/2020
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
ms.openlocfilehash: d91f6ff24f8f2c051ed23565983c2bc6a2c12b55
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261414"
---
# <a name="cart-module"></a><span data-ttu-id="02ab1-103">Modul košíku</span><span class="sxs-lookup"><span data-stu-id="02ab1-103">Cart module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="02ab1-104">Tohle téma se zabývá moduly košíku a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="02ab1-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="02ab1-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="02ab1-105">Overview</span></span>

<span data-ttu-id="02ab1-106">Modul košíku zobrazuje položky, které byly přidány do košíku, než odběratel pokračuje v rezervaci.</span><span class="sxs-lookup"><span data-stu-id="02ab1-106">A cart module shows the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="02ab1-107">Modul také zobrazuje souhrn objednávky a umožňuje odběrateli použití nebo odebrání propagačních kódů.</span><span class="sxs-lookup"><span data-stu-id="02ab1-107">The module also shows an order summary and lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="02ab1-108">Modul košíku podporuje přihlášené uživatele i hosty.</span><span class="sxs-lookup"><span data-stu-id="02ab1-108">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="02ab1-109">Také podporuje odkaz **Zpět na nákupy**.</span><span class="sxs-lookup"><span data-stu-id="02ab1-109">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="02ab1-110">Můžete konfigurovat cestu pro tento odkaz v **Nastavení webu \> Rozšíření \> Cesty**.</span><span class="sxs-lookup"><span data-stu-id="02ab1-110">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="02ab1-111">Modul košíku vykresluje data založená na ID košíku, což je soubor cookie prohlížeče dostupný v rámci celého webu.</span><span class="sxs-lookup"><span data-stu-id="02ab1-111">The cart module renders data based on the cart ID, which is a browser cookie available throughout the site.</span></span>

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="02ab1-112">Vlastnosti a pozice modulu košíku</span><span class="sxs-lookup"><span data-stu-id="02ab1-112">Cart module properties and slots</span></span>

<span data-ttu-id="02ab1-113">Modul košíku má vlastnost **Záhlaví**, kterou lze nastavit na hodnoty, jako je **Nákupní taška** a **Položky v košíku**.</span><span class="sxs-lookup"><span data-stu-id="02ab1-113">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="02ab1-114">Moduly, které lze použít v modulu košíku</span><span class="sxs-lookup"><span data-stu-id="02ab1-114">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="02ab1-115">**Textový blok** – Tento modul podporuje vlastní zasílání zpráv v modulu košíku.</span><span class="sxs-lookup"><span data-stu-id="02ab1-115">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="02ab1-116">Zprávy řídí systém správy obsahu (CMS).</span><span class="sxs-lookup"><span data-stu-id="02ab1-116">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="02ab1-117">Lze přidat libovolnou zprávu, například „Při problémech s objednávkou volejte 123 456 789“.</span><span class="sxs-lookup"><span data-stu-id="02ab1-117">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="02ab1-118">**Volič obchodů** – Tento modul zobrazuje seznam obchodů, které jsou poblíž a kde je položka k výdeji.</span><span class="sxs-lookup"><span data-stu-id="02ab1-118">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="02ab1-119">Umožňuje uživatelům zadat umístění pro hledání obchodů, které jsou v okolí.</span><span class="sxs-lookup"><span data-stu-id="02ab1-119">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="02ab1-120">Další informace o tomto modulu naleznete v tématu [Modul volič obchodů](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="02ab1-120">For more information on this module, see [Store selector module](store-selector.md).</span></span>


## <a name="module-properties"></a><span data-ttu-id="02ab1-121">Vlastnosti modulu</span><span class="sxs-lookup"><span data-stu-id="02ab1-121">Module properties</span></span>

<span data-ttu-id="02ab1-122">Moduly košíku mají následující nastavení, která lze konfigurovat na **Nastavení webu \> Rozšíření**:</span><span class="sxs-lookup"><span data-stu-id="02ab1-122">Cart modules have the following settings that can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="02ab1-123">**Maximální množství** – tato vlastnost se používá k určení maximálního počtu jednotlivých položek, které lze přidat do nákupního košíku.</span><span class="sxs-lookup"><span data-stu-id="02ab1-123">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="02ab1-124">Maloobchodní prodejce může například rozhodnout, že v jedné transakci lze prodávat pouze 10 jednotlivých produktů.</span><span class="sxs-lookup"><span data-stu-id="02ab1-124">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="02ab1-125">**Kontrola zásob** – Je-li nastavena hodnota **Pravda**, položka se přidá do košíku pouze poté, co se modul buy boxu ověří, že je na skladě.</span><span class="sxs-lookup"><span data-stu-id="02ab1-125">**Inventory check** – When the value is set to **True**, an item is added to the cart only after the buy box module makes sure that it's in stock.</span></span> <span data-ttu-id="02ab1-126">Tato kontrola zásob se provádí pro scénáře, když má být položka expedována, a pro scénáře, kdy má být vyzvednuta v obchodě.</span><span class="sxs-lookup"><span data-stu-id="02ab1-126">This inventory check is done for scenarios where the item will be shipped and for scenarios where it will be picked up in the store.</span></span> <span data-ttu-id="02ab1-127">Je-li tato hodnota nastavena na hodnotu **Nepravda**, před přidáním položky do nákupního košíku a podání objednávky není provedena kontrola zásob.</span><span class="sxs-lookup"><span data-stu-id="02ab1-127">If the value is set to **False**, no inventory check is done before an item is added to the cart and the order is placed.</span></span> <span data-ttu-id="02ab1-128">Informace o tom, jak konfigurovat nastavení zásob v administrativě, naleznete v tématu [Výpočet dostupnosti zásob pro maloobchodní kanály](calculated-inventory-retail-channels.md).</span><span class="sxs-lookup"><span data-stu-id="02ab1-128">For information on how to configure inventory settings in back office, see [Calculate inventory availability for retail channels](calculated-inventory-retail-channels.md).</span></span>
- <span data-ttu-id="02ab1-129">**Zásboník zásob** – Tato vlastnost se používá k určení čísla zásobníku pro zásoby.</span><span class="sxs-lookup"><span data-stu-id="02ab1-129">**Inventory buffer** – This property is used to specify a buffer number for inventory.</span></span> <span data-ttu-id="02ab1-130">Údržba zásob probíhá v reálném čase a když mnoho zákazníků podá objednávku, může být obtížné zajistit přesný počet zásob.</span><span class="sxs-lookup"><span data-stu-id="02ab1-130">Inventory is maintained in real time, and when many customers place orders, it can be difficult to maintain an accurate inventory count.</span></span> <span data-ttu-id="02ab1-131">Když je provedena kontrola zásob, pokud je množství na skladu nižší než množství zásobníku, produkt je brán, jakože není na skladu.</span><span class="sxs-lookup"><span data-stu-id="02ab1-131">When an inventory check is done, if the inventory is less than the buffer amount, the product is treated as out of stock.</span></span> <span data-ttu-id="02ab1-132">Pokud se tedy prodej rychle točí prostřednictvím několika kanálů a zásoby nejsou plně synchronizovány, existuje menší riziko, že položka, která se nenachází na skladě, je v prodeji.</span><span class="sxs-lookup"><span data-stu-id="02ab1-132">Therefore, when sales occur quickly through several channels, and the inventory count isn't fully synced, there is less risk that an item that is out of stock will be sold.</span></span>
- <span data-ttu-id="02ab1-133">**Zpět k nákupu** – Tato vlastnost se používá k určení trasy pro odkaz **Zpět k nákupu**.</span><span class="sxs-lookup"><span data-stu-id="02ab1-133">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="02ab1-134">Postup lze konfigurovat na úrovni webu a umožnit maloobchodním prodejcům, aby se odběratel mohl vrátit na domovskou stránku nebo na jakoukoli jinou stránku na webu.</span><span class="sxs-lookup"><span data-stu-id="02ab1-134">The route can be configured at the site level, allowing retailers to take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="02ab1-135">Interakce Commerce Scale Unit</span><span class="sxs-lookup"><span data-stu-id="02ab1-135">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="02ab1-136">Modul košíku načítá informace o produktu pomocí rozhraní API Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="02ab1-136">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="02ab1-137">ID košíku ze souboru cookie prohlížeče se používá k načtení všech informací o produktu z Commerce Scale Unit.</span><span class="sxs-lookup"><span data-stu-id="02ab1-137">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="02ab1-138">Přidání modulu košíku na stránku</span><span class="sxs-lookup"><span data-stu-id="02ab1-138">Add a cart module to a page</span></span>

<span data-ttu-id="02ab1-139">Chcete-li přidat modul košíku na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="02ab1-139">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="02ab1-140">Vytvořte fragment s názvem **Fragment košíku** a modul košíku do nového fragmentu.</span><span class="sxs-lookup"><span data-stu-id="02ab1-140">Create a fragment named **Cart fragment**, and add a cart module to the new fragment.</span></span>
1. <span data-ttu-id="02ab1-141">Přidejte do modulu košíku nadpis.</span><span class="sxs-lookup"><span data-stu-id="02ab1-141">Add a heading to the cart module.</span></span>
1. <span data-ttu-id="02ab1-142">Přidejte modul Selector obchodu do modulu vozík.</span><span class="sxs-lookup"><span data-stu-id="02ab1-142">Add a store selector module to the cart module.</span></span>
1. <span data-ttu-id="02ab1-143">Uložte fragment, dokončete úpravy a publikujte jej.</span><span class="sxs-lookup"><span data-stu-id="02ab1-143">Save the fragment, finish editing, and then publish the fragment.</span></span>
1. <span data-ttu-id="02ab1-144">Vytvořte šablonu s názvem **Šablona košíku** a přidejte fragment košíku, který jste právě vytvořili.</span><span class="sxs-lookup"><span data-stu-id="02ab1-144">Create a template named **Cart template**, and add the cart fragment that you just created.</span></span>
1. <span data-ttu-id="02ab1-145">Uložte šblonu, dokončete úpravy a publikujte ji.</span><span class="sxs-lookup"><span data-stu-id="02ab1-145">Save the template, finish editing, and then publish the template.</span></span>
1. <span data-ttu-id="02ab1-146">Vytvořte stránku, která používá novou šablonu.</span><span class="sxs-lookup"><span data-stu-id="02ab1-146">Create a page that uses the new template.</span></span>
1. <span data-ttu-id="02ab1-147">Uložte stránku a zobrazte náhled.</span><span class="sxs-lookup"><span data-stu-id="02ab1-147">Save and preview the page.</span></span>
1. <span data-ttu-id="02ab1-148">Dokončete úpravu stránky a publikujte ji.</span><span class="sxs-lookup"><span data-stu-id="02ab1-148">Finish editing the page, and then publish the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="02ab1-149">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="02ab1-149">Additional resources</span></span>

[<span data-ttu-id="02ab1-150">Přehled startovací sady</span><span class="sxs-lookup"><span data-stu-id="02ab1-150">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="02ab1-151">Modul kontejneru</span><span class="sxs-lookup"><span data-stu-id="02ab1-151">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="02ab1-152">Modul volby obchodu</span><span class="sxs-lookup"><span data-stu-id="02ab1-152">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="02ab1-153">Modul buy boxu</span><span class="sxs-lookup"><span data-stu-id="02ab1-153">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="02ab1-154">Ikona modulu košíku</span><span class="sxs-lookup"><span data-stu-id="02ab1-154">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="02ab1-155">Modul pokladny</span><span class="sxs-lookup"><span data-stu-id="02ab1-155">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="02ab1-156">Modul potvrzení objednávky</span><span class="sxs-lookup"><span data-stu-id="02ab1-156">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="02ab1-157">Modul záhlaví</span><span class="sxs-lookup"><span data-stu-id="02ab1-157">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="02ab1-158">Modul zápatí</span><span class="sxs-lookup"><span data-stu-id="02ab1-158">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="02ab1-159">Výpočet dostupnosti zásob pro maloobchodní kanály</span><span class="sxs-lookup"><span data-stu-id="02ab1-159">Calculate inventory availability for retail channels</span></span>](calculated-inventory-retail-channels.md)
