---
title: Přehled stránek s podrobnostmi o produktu
description: Toto téma poskytuje přehled stránek podrobností o produktu (PDP) v řešení Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: c53e74204fad2960dfba972a38c511df7d6672d8
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410888"
---
# <a name="product-details-pages-overview"></a><span data-ttu-id="41281-103">Přehled stránek s podrobnostmi o produktu</span><span class="sxs-lookup"><span data-stu-id="41281-103">Product details pages overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="41281-104">Toto téma poskytuje přehled stránek podrobností o produktu (PDP) v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="41281-104">This topic provides an overview of product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="41281-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="41281-105">Overview</span></span>

<span data-ttu-id="41281-106">Systém PDP poskytuje podrobné informace o produktu a umožňuje zákazníkům vybrat možnosti produktu, například velikost, styl a barvu.</span><span class="sxs-lookup"><span data-stu-id="41281-106">A PDP provides detailed information about a product, and lets customers select product options such as a size, style, and color.</span></span> <span data-ttu-id="41281-107">PDP by měl předprezentovat všechny informace o produktu, které odběratel potřebuje k provedení rozhodnutí o nákupu.</span><span class="sxs-lookup"><span data-stu-id="41281-107">A PDP should showcase all the product information that a customer requires to make a purchase decision.</span></span>

<span data-ttu-id="41281-108">Následující obrázek znázorňuje příklad PDP</span><span class="sxs-lookup"><span data-stu-id="41281-108">The following illustration shows an example of a PDP.</span></span>

![Příklad stránky podrobností o produktu](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a><span data-ttu-id="41281-110">Moduly záhlaví a zápatí</span><span class="sxs-lookup"><span data-stu-id="41281-110">Header and footer modules</span></span>

<span data-ttu-id="41281-111">Horní okraj PDP obsahuje záhlaví, ve kterém jsou zobrazeny všechny kategorie produktů a další stránky, které chtějí odběratelé vyhledávat.</span><span class="sxs-lookup"><span data-stu-id="41281-111">The top of a PDP has a header that shows all the product categories and other pages that the retailer wants customers to browse.</span></span> <span data-ttu-id="41281-112">Dolní okraj stránky má zápatí, které obsahuje rychlé odkazy na různá témata, která mohou být zajímavá.</span><span class="sxs-lookup"><span data-stu-id="41281-112">The bottom of the page has a footer that contains quick links to various topics that might interest customers.</span></span>

## <a name="buy-box-module"></a><span data-ttu-id="41281-113">Modul buy boxu</span><span class="sxs-lookup"><span data-stu-id="41281-113">Buy box module</span></span>

<span data-ttu-id="41281-114">Nejdůležitějším modulem systému PDP je modul buy boxu, který se zobrazí jako první položka v hlavní části stránky.</span><span class="sxs-lookup"><span data-stu-id="41281-114">The most important module on a PDP is the buy box module, which appears as the first item in the main section of the page.</span></span> <span data-ttu-id="41281-115">Modul buy boxu zobrazuje důležité informace o produktu, jako je například název produktu, popis produktu, cena produktu, obrázky produktů a hodnocení produktu.</span><span class="sxs-lookup"><span data-stu-id="41281-115">A buy box module shows important product information, such as the product name, the product description, the product price, product images, and product ratings.</span></span>

<span data-ttu-id="41281-116">Modul buy boxu umožňuje odběrateli vybrat možnosti produktu (například velikost, styl a barvu) a přidat produkt do košíku.</span><span class="sxs-lookup"><span data-stu-id="41281-116">The buy box module lets the customer select product options (for example, a size, style, and color) and add the product to the cart.</span></span> <span data-ttu-id="41281-117">Rovněž umožňuje odběrateli nakoupit produkt online a vyzvednout jej v obchodě.</span><span class="sxs-lookup"><span data-stu-id="41281-117">It also lets the customer buy the product online and pick it up in a store.</span></span> <span data-ttu-id="41281-118">Nákup online a výdej v modulu obchod používá integraci s rozhraními API služby Bing Maps k hledání blízkých obchodů nebo obchodů v jiném umístění, které určuje zákazník.</span><span class="sxs-lookup"><span data-stu-id="41281-118">The buy online and pick up in store module uses integration with Bing Maps application programming interfaces (APIs) to find nearby stores or stores in another location that the customer specifies.</span></span>

<span data-ttu-id="41281-119">Modul buy boxu vyžaduje ID produktu.</span><span class="sxs-lookup"><span data-stu-id="41281-119">A buy box module requires a product ID.</span></span> <span data-ttu-id="41281-120">Toto ID je odvozeno od kontextu stránky.</span><span class="sxs-lookup"><span data-stu-id="41281-120">This ID is derived from the page context.</span></span> <span data-ttu-id="41281-121">Je-li do stránky přidán modul buy boxu, na kterém kontext stránky neobsahuje ID produktu, nebudou informace správně vygenerovány.</span><span class="sxs-lookup"><span data-stu-id="41281-121">If a buy box module is added to a page where the page context doesn't include a product ID, it won't render the information correctly.</span></span>

## <a name="product-specifications-module"></a><span data-ttu-id="41281-122">Modul specifikací produktu</span><span class="sxs-lookup"><span data-stu-id="41281-122">Product specifications module</span></span>

<span data-ttu-id="41281-123">Modul specifikací produktu lze použít k předvedení dalších podrobností o produktu.</span><span class="sxs-lookup"><span data-stu-id="41281-123">The product specifications module can be used to showcase additional details about the product.</span></span> <span data-ttu-id="41281-124">Tyto podrobnosti jsou čerpány z atributů produktu v aplikaci Commerce.</span><span class="sxs-lookup"><span data-stu-id="41281-124">These details are taken from product attributes in Commerce.</span></span> <span data-ttu-id="41281-125">V modulu specifikace produktu jsou zobrazeny všechny atributy, pro které je vlastnost **viditelné** nastavena na hodnotu **true**.</span><span class="sxs-lookup"><span data-stu-id="41281-125">The product specifications module shows every attribute where the **visible** property is set to **true**.</span></span> <span data-ttu-id="41281-126">K načtení atributů produktu je vyžadováno ID produktu.</span><span class="sxs-lookup"><span data-stu-id="41281-126">It requires a product ID to retrieve the product attributes.</span></span>

## <a name="recommendations-module"></a><span data-ttu-id="41281-127">Modul doporučení</span><span class="sxs-lookup"><span data-stu-id="41281-127">Recommendations module</span></span>

<span data-ttu-id="41281-128">Nejdůležitějším modulem systému PDP je modul doporučení.</span><span class="sxs-lookup"><span data-stu-id="41281-128">The recommendations module is an important module on a PDP.</span></span> <span data-ttu-id="41281-129">Zatímco odběratelé procházejí produkty, měly by jim být prezentovány další možnosti produktu, aby mohli najít správný produkt a nakupovat.</span><span class="sxs-lookup"><span data-stu-id="41281-129">While customers browse for products, more product options should be presented to them, so that they can find the correct product and make a purchase.</span></span> <span data-ttu-id="41281-130">Doporučení zákazníkům umožňují snadno objevit související obsah a pokračovat v nákupu.</span><span class="sxs-lookup"><span data-stu-id="41281-130">Recommendations help customers easily discover related content and continue to shop.</span></span>

<span data-ttu-id="41281-131">K dispozici jsou různé typy seznamů doporučení:</span><span class="sxs-lookup"><span data-stu-id="41281-131">Different types of recommendation lists are available:</span></span>

- <span data-ttu-id="41281-132">Seznam **Lidem se také líbí** je založen na strojovém učení.</span><span class="sxs-lookup"><span data-stu-id="41281-132">The **People also like** list is based on machine learning.</span></span> <span data-ttu-id="41281-133">K poskytování doporučení používá historii transakcí ostatních zákazníků.</span><span class="sxs-lookup"><span data-stu-id="41281-133">It uses the transaction history of other customers to provide recommendations.</span></span> <span data-ttu-id="41281-134">Tento seznam je vygenerován službou doporučení a připomíná seznam "Zákazníci, kteří toto nakoupili, koupili také...".</span><span class="sxs-lookup"><span data-stu-id="41281-134">This list is generated by the recommendations service and resembles "Customers who bought this also bought..." lists.</span></span> <span data-ttu-id="41281-135">K vygenerování tohoto seznamu je nutné ID produktu.</span><span class="sxs-lookup"><span data-stu-id="41281-135">A product ID is required to generate this list.</span></span>
- <span data-ttu-id="41281-136">Seznam **Související** lze nakonfigurovat pro produkt v Commerce.</span><span class="sxs-lookup"><span data-stu-id="41281-136">A **Related** list can be configured for a product in Commerce.</span></span> <span data-ttu-id="41281-137">U souvisejícího seznamu lze nakonfigurovat například pro hnědou koženou kabelku další kabelky, které jsou kožené nebo navržené pro cestování.</span><span class="sxs-lookup"><span data-stu-id="41281-137">For example, for a brown leather travel handbag, more handbags that are leather-based or designed for travel purposes can be configured for the related list.</span></span> <span data-ttu-id="41281-138">Jiné typy souvisejících seznamů, například **Doplňky** a **Podobně**, lze také konfigurovat v Commerce.</span><span class="sxs-lookup"><span data-stu-id="41281-138">Other types of related lists, such as **Accessories** and **More like this**, can also be configured in Commerce.</span></span> <span data-ttu-id="41281-139">K vygenerování tohoto seznamu je nutné ID produktu.</span><span class="sxs-lookup"><span data-stu-id="41281-139">A product ID is required to generate this list.</span></span> <span data-ttu-id="41281-140">Proto, pokud je přidán na domovskou stránku, kde kontext stránky neobsahuje ID produktu, bude seznam prázdný.</span><span class="sxs-lookup"><span data-stu-id="41281-140">Therefore, if it's added to a home page, where the page context doesn't include a product ID, the list will be empty.</span></span>
- <span data-ttu-id="41281-141">lgoritmem generované seznamy doporučení, jako je například **Trendující**, **Nejlepe prodávané** a **Nové**, lze použít na PDP.</span><span class="sxs-lookup"><span data-stu-id="41281-141">Algorithmically generated recommendation lists, such as **Trending**, **Best Selling**, and **New**, can be used on PDPs.</span></span> <span data-ttu-id="41281-142">Ačkoli tyto seznamy nemusí přímo souviset s produktem v systémech PDP, jsou jiným způsobem, jak zákazníkům pomoci najít produkty, které je mohou zajímat.</span><span class="sxs-lookup"><span data-stu-id="41281-142">Although these lists might not be directly related to the product on the PDP, they are another way to help customers find products that might interest them.</span></span> <span data-ttu-id="41281-143">Tyto typy seznamů nevyžadují ID produktu.</span><span class="sxs-lookup"><span data-stu-id="41281-143">These types of lists don't require a product ID.</span></span> <span data-ttu-id="41281-144">Jedná se o obecné seznamy, které jsou generovány na základě vzorků nákupu v celém webu.</span><span class="sxs-lookup"><span data-stu-id="41281-144">They are generic lists that are generated based on shopping patterns across the site.</span></span>
- <span data-ttu-id="41281-145">Redakční seznamy jsou ručně spravované seznamy.</span><span class="sxs-lookup"><span data-stu-id="41281-145">Editorial lists are manually curated lists.</span></span> <span data-ttu-id="41281-146">Maloobchodní prodejce se může například rozhodnout ručně spravovat seznamy výrobků, které chce prezentovat.</span><span class="sxs-lookup"><span data-stu-id="41281-146">For example, a retailer might decide to manually curate lists of products that it wants to showcase.</span></span>

## <a name="ratings-and-reviews-modules"></a><span data-ttu-id="41281-147">Moduly hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="41281-147">Ratings and reviews modules</span></span>

<span data-ttu-id="41281-148">K zobrazení a přidání recenzí lze použít tři moduly:</span><span class="sxs-lookup"><span data-stu-id="41281-148">Three modules can be used to show and add reviews:</span></span>

- <span data-ttu-id="41281-149">**Modul hodnocení a recenzí** - tento modul zobrazuje hodnocení a recenze poskytované jinými odběrateli.</span><span class="sxs-lookup"><span data-stu-id="41281-149">**Reviews** – This module lists ratings and reviews that have been provided by other customers.</span></span> <span data-ttu-id="41281-150">Zákazníci mohou tyto recenze třídit a filtrovat.</span><span class="sxs-lookup"><span data-stu-id="41281-150">Customers can sort and filter the reviews.</span></span> <span data-ttu-id="41281-151">Tento modul také zákazníkům umožňuje zákazníkům označovat recenze jako To se mi líbí nebo Už se mi to nelíbí a hlásit problémy.</span><span class="sxs-lookup"><span data-stu-id="41281-151">This module also lets customers like or dislike reviews, and report issues.</span></span>
- <span data-ttu-id="41281-152">**Napsat recenzi** – tento modul umožní zákazníkům psát vlastní recenze produktu.</span><span class="sxs-lookup"><span data-stu-id="41281-152">**Write review** – This module lets customers write their own reviews of a product.</span></span>
- <span data-ttu-id="41281-153">**Histogram hodnocení** – Tento modul obsahuje histogram, který zobrazuje trend hodnocení produktu.</span><span class="sxs-lookup"><span data-stu-id="41281-153">**Ratings histogram** – This module includes a histogram that shows the ratings trend for a product.</span></span>

<span data-ttu-id="41281-154">Další podrobnosti získáte v tématu [Přehled hodnocení a recenzí](ratings-reviews-overview.md).</span><span class="sxs-lookup"><span data-stu-id="41281-154">For more details, see [Ratings and reviews overview](ratings-reviews-overview.md).</span></span>

## <a name="marketing-modules"></a><span data-ttu-id="41281-155">Moduly marketing</span><span class="sxs-lookup"><span data-stu-id="41281-155">Marketing modules</span></span>

<span data-ttu-id="41281-156">Pokud je marketingový obsah jedinečný pro určitý produkt, lze do PDP přidat libovolný marketingový modul.</span><span class="sxs-lookup"><span data-stu-id="41281-156">If marketing content is unique to a specific product, any marketing module can be added to the PDP.</span></span> <span data-ttu-id="41281-157">Marketingové moduly můžete přidat do PDP pomocí "obohacení" stránky.</span><span class="sxs-lookup"><span data-stu-id="41281-157">You can add marketing modules to a PDP by "enriching" the page.</span></span> <span data-ttu-id="41281-158">Další informace naleznete v tématu [Obohacení stránky produktu](enrich-product-page.md).</span><span class="sxs-lookup"><span data-stu-id="41281-158">For more details, see [Enrich a product page](enrich-product-page.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="41281-159">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="41281-159">Additional resources</span></span>

[<span data-ttu-id="41281-160">Přehled domovské stránky</span><span class="sxs-lookup"><span data-stu-id="41281-160">Home page overview</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="41281-161">Přehled stránek košíku a pokladny</span><span class="sxs-lookup"><span data-stu-id="41281-161">Cart and checkout pages overview</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="41281-162">Přehled stránek správy účtů</span><span class="sxs-lookup"><span data-stu-id="41281-162">Account management pages overview</span></span>](quick-tour-account-management.md)

[<span data-ttu-id="41281-163">Obohacení stránky podrobností produktu</span><span class="sxs-lookup"><span data-stu-id="41281-163">Enrich a product details page</span></span>](enrich-product-page.md)
