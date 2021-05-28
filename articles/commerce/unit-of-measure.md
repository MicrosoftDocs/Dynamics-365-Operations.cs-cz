---
title: Použití nastavení měrné jednotky
description: Toto téma se týká nastavení měrných jednotek a popisuje, jak je použít v softwaru Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 04/23/2021
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: d1fba966434b80c9b64c1f4d9b6b87993d59c0bf
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6022367"
---
# <a name="apply-unit-of-measure-settings"></a><span data-ttu-id="0dcd0-103">Použití nastavení měrné jednotky</span><span class="sxs-lookup"><span data-stu-id="0dcd0-103">Apply unit of measure settings</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="0dcd0-104">Toto téma se týká nastavení měrných jednotek a popisuje, jak je použít v softwaru Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0dcd0-104">This topic covers unit of measure settings and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="0dcd0-105">Produkt lze prodávat v různých jednotkách, například „jednotlivě“, „pár“ a „tucet“.</span><span class="sxs-lookup"><span data-stu-id="0dcd0-105">A product can be sold in different units, such as "each," "pair," and "dozen."</span></span> <span data-ttu-id="0dcd0-106">V Commerce Headquarters lze pro produkt definovat měrnou jednotku prodeje a zobrazit ji na webu elektronického obchodu.</span><span class="sxs-lookup"><span data-stu-id="0dcd0-106">In Commerce headquarters, the sell-by unit of measure can be defined for a product and shown on an e-commerce site.</span></span> <span data-ttu-id="0dcd0-107">Například pokud maloobchodník prodává produkt jednotlivě i v desítkách, lze zobrazit dostupné měrné jednotky společně s dalšími informacemi o produktu.</span><span class="sxs-lookup"><span data-stu-id="0dcd0-107">For example, if a retailer sells a product both individually and in dozens, the available units of measure can be shown together with other product information.</span></span>

<span data-ttu-id="0dcd0-108">V příkladu na následujícím obrázku byla v Commerce Headquarters nakonfigurována měrná jednotka prodeje ve výši **ea** (jednotlivě).</span><span class="sxs-lookup"><span data-stu-id="0dcd0-108">In the example in the following illustration, a sell-by unit of measure of **ea** (each) has been configured for a product in Commerce headquarters.</span></span>

![Příklad produktu, který je nakonfigurován s měrnou jednotkou v Commerce Headquarters](./media/Productunit-headquarters.PNG)

> [!NOTE]
> <span data-ttu-id="0dcd0-110">Podpora pro použití a zobrazování měrných jednotek je k dispozici od verze Commerce 10.0.19.</span><span class="sxs-lookup"><span data-stu-id="0dcd0-110">Support for applying and showing the unit of measure is available as of the Commerce version 10.0.19 release.</span></span>

## <a name="unit-of-measure-settings"></a><span data-ttu-id="0dcd0-111">Nastavení měrných jednotek</span><span class="sxs-lookup"><span data-stu-id="0dcd0-111">Unit of measure settings</span></span>

<span data-ttu-id="0dcd0-112">Nastavení zobrazení měrné jednotky je definováno v konfigurátoru webů Commerce v nabídce **Nastavení webu \> Rozšíření \> Zobrazit měrnou jednotku pro produkty**.</span><span class="sxs-lookup"><span data-stu-id="0dcd0-112">Unit of measure display settings are defined in Commerce site builder, at **Site settings \> Extensions \> Display unit of measure for products**.</span></span> <span data-ttu-id="0dcd0-113">Existují tři podporovaná nastavení:</span><span class="sxs-lookup"><span data-stu-id="0dcd0-113">There are three supported settings:</span></span>

- <span data-ttu-id="0dcd0-114">**Nezobrazovat** – je-li toto nastavení vybráno, web elektronického obchodu nebude zobrazovat měrnou jednotku produktu.</span><span class="sxs-lookup"><span data-stu-id="0dcd0-114">**Do not display** – When this setting is selected, the e-commerce site won't show the unit of measure for the product.</span></span> <span data-ttu-id="0dcd0-115">Toto chování je výchozím chováním.</span><span class="sxs-lookup"><span data-stu-id="0dcd0-115">This behavior is the default behavior.</span></span>
- <span data-ttu-id="0dcd0-116">**Zobrazit při nákupu produktu** – když je toto nastavení vybráno, měrná jednotka se zobrazí na stránkách s podrobnostmi o produktu, košíku, pokladně, historii objednávek a stránkách podrobností objednávek.</span><span class="sxs-lookup"><span data-stu-id="0dcd0-116">**Display in the product buying experience** – When this setting is selected, the unit of measure is shown on product details, cart, checkout, order history, and order details pages.</span></span>
- <span data-ttu-id="0dcd0-117">**Zobrazit v procházení a nakupování produktu** – pokud je toto nastavení vybráno, měrná jednotka se zobrazí na stránkách nákupu produktu a také během procházení produktu.</span><span class="sxs-lookup"><span data-stu-id="0dcd0-117">**Display in the product browsing and buying experience** – When this setting is selected, the unit of measure is shown on the product buying experience pages and also during the product browsing experience.</span></span> <span data-ttu-id="0dcd0-118">V rámci tohoto chování se měrné jednotky zobrazují ve výsledcích vyhledávání a v modulech kolekce produktů.</span><span class="sxs-lookup"><span data-stu-id="0dcd0-118">As part of this behavior, units of measure are shown in search results and product collection modules.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0dcd0-119">Nastavení zobrazení měrných jednotek je k dispozici od verze Commerce 10.0.19.</span><span class="sxs-lookup"><span data-stu-id="0dcd0-119">Unit of measure display settings are available as of the Commerce version 10.0.19 release.</span></span> <span data-ttu-id="0dcd0-120">Pokud provádíte aktualizaci ze starší verze Commerce, musíte ručně aktualizovat soubor appsettings.json.</span><span class="sxs-lookup"><span data-stu-id="0dcd0-120">If you're updating from an older version of Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="0dcd0-121">Další pokyny viz [SDK a aktualizace knihovny modulů](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="0dcd0-121">For instructions, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="modules-that-use-unit-of-measure-settings"></a><span data-ttu-id="0dcd0-122">Moduly, které používají nastavení měrné jednotky</span><span class="sxs-lookup"><span data-stu-id="0dcd0-122">Modules that use unit of measure settings</span></span>

<span data-ttu-id="0dcd0-123">Moduly, které používají nastavení měrné jednotky, zahrnují moduly buy boxu, seznamu přání, košíku, ikony košíku, kontejneru výsledků hledání, kolekce produktů, pokladny a podrobností objednávky.</span><span class="sxs-lookup"><span data-stu-id="0dcd0-123">Modules that use the unit of measure settings include the buy box, wishlist, cart, cart icon, search results container, product collection, checkout, and order details modules.</span></span>

<span data-ttu-id="0dcd0-124">Na příkladu na následujícím obrázku zobrazuje stránka s podrobnostmi o produktu (PDP) měrné jednotky (**ea**) pro produkt.</span><span class="sxs-lookup"><span data-stu-id="0dcd0-124">In the example in the following illustration, a product details page (PDP) shows the unit of measure (**ea**) for a product.</span></span>

![Příklad PDP, která zobrazuje měrnou jednotku](./media/Productunit-PDP.png)

<span data-ttu-id="0dcd0-126">Na příkladu na následujícím obrázku zobrazuje modul kolekce produktu měrné jednotky (**ea**) pro produkt.</span><span class="sxs-lookup"><span data-stu-id="0dcd0-126">In the example in the following illustration, a product collection module shows the unit of measure (**ea**) for a product.</span></span>

![Příklad modulu kolekce produktu, který zobrazuje měrnou jednotku](./media/Productunit-productcollection.png)

## <a name="additional-resources"></a><span data-ttu-id="0dcd0-128">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="0dcd0-128">Additional resources</span></span>

[<span data-ttu-id="0dcd0-129">Přehled knihovny modulů</span><span class="sxs-lookup"><span data-stu-id="0dcd0-129">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="0dcd0-130">Modul košíku</span><span class="sxs-lookup"><span data-stu-id="0dcd0-130">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="0dcd0-131">Modul buy boxu</span><span class="sxs-lookup"><span data-stu-id="0dcd0-131">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="0dcd0-132">Moduly a stránky správy obchodního vztahu</span><span class="sxs-lookup"><span data-stu-id="0dcd0-132">Account management pages and modules</span></span>](account-management.md)

[<span data-ttu-id="0dcd0-133">SDK a aktualizace knihovny modulů</span><span class="sxs-lookup"><span data-stu-id="0dcd0-133">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
