---
title: Prohlídka stránek podrobností o produktu
description: Toto téma poskytuje přehled stránek podrobností o produktu (PDP) v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 3b02d50adbfcda27d590bcb87fd9669d67d4a01c
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697858"
---
# <a name="overview-of-product-details-pages"></a><span data-ttu-id="2e333-103">Prohlídka stránek podrobností o produktu</span><span class="sxs-lookup"><span data-stu-id="2e333-103">Overview of product details pages</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="2e333-104">Toto téma poskytuje přehled stránek podrobností o produktu (PDP) v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2e333-104">This topic provides an overview of product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2e333-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="2e333-105">Overview</span></span>

<span data-ttu-id="2e333-106">Systém PDP poskytuje podrobné informace o produktu a umožňuje zákazníkům vybrat možnosti produktu, například velikost, styl a barvu.</span><span class="sxs-lookup"><span data-stu-id="2e333-106">A PDP provides detailed information about a product, and lets customers select product options such as a size, style, and color.</span></span> <span data-ttu-id="2e333-107">PDP by měl předprezentovat všechny informace o produktu, které odběratel potřebuje k provedení rozhodnutí o nákupu.</span><span class="sxs-lookup"><span data-stu-id="2e333-107">A PDP should showcase all the product information that a customer requires to make a purchase decision.</span></span>

<span data-ttu-id="2e333-108">Následující obrázek znázorňuje příklad PDP</span><span class="sxs-lookup"><span data-stu-id="2e333-108">The following illustration shows an example of a PDP.</span></span>

![Příklad stránky podrobností o produktu](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a><span data-ttu-id="2e333-110">Moduly záhlaví a zápatí</span><span class="sxs-lookup"><span data-stu-id="2e333-110">Header and footer modules</span></span>

<span data-ttu-id="2e333-111">Horní okraj PDP obsahuje záhlaví, ve kterém jsou zobrazeny všechny kategorie produktů a další stránky, které chtějí odběratelé vyhledávat.</span><span class="sxs-lookup"><span data-stu-id="2e333-111">The top of a PDP has a header that shows all the product categories and other pages that the retailer wants customers to browse.</span></span> <span data-ttu-id="2e333-112">Dolní okraj stránky má zápatí, které obsahuje rychlé odkazy na různá témata, která mohou být zajímavá.</span><span class="sxs-lookup"><span data-stu-id="2e333-112">The bottom of the page has a footer that contains quick links to various topics that might interest customers.</span></span>

## <a name="buy-box-module"></a><span data-ttu-id="2e333-113">Modul buy boxu</span><span class="sxs-lookup"><span data-stu-id="2e333-113">Buy box module</span></span>

<span data-ttu-id="2e333-114">Nejdůležitějším modulem systému PDP je modul buy boxu.</span><span class="sxs-lookup"><span data-stu-id="2e333-114">The most important module on a PDP is the buy box module.</span></span> <span data-ttu-id="2e333-115">Proto se jedná o první položku v hlavní části stránky.</span><span class="sxs-lookup"><span data-stu-id="2e333-115">Therefore, it's the first item in the main section of the page.</span></span> <span data-ttu-id="2e333-116">Modul buy boxu se nachází v modulu kontejnerů a je hostitelem několika modulů, které obsahují nejdůležitější informace o produktu.</span><span class="sxs-lookup"><span data-stu-id="2e333-116">A buy box module is a container module and hosts several modules that contain the most important information about the product.</span></span> <span data-ttu-id="2e333-117">Tyto informace zahrnují název produktu, obrázky produktu, popis, cenu a hodnocení produktu.</span><span class="sxs-lookup"><span data-stu-id="2e333-117">This information includes the product name, product images, the description, the price, and product ratings.</span></span>

<span data-ttu-id="2e333-118">Modul buy boxu umožňuje odběrateli vybrat možnosti produktu (například velikost, styl a barvu) a přidat produkt do košíku.</span><span class="sxs-lookup"><span data-stu-id="2e333-118">The buy box module lets the customer select product options (for example, a size, style, and color) and add the product to the cart.</span></span> <span data-ttu-id="2e333-119">Rovněž umožňuje odběrateli nakoupit produkt online a vyzvednout jej v obchodě.</span><span class="sxs-lookup"><span data-stu-id="2e333-119">It also lets the customer buy the product online and pick it up in a store.</span></span> <span data-ttu-id="2e333-120">Nákup online a výdej v modulu obchod používá integraci s rozhraními API služby Bing Maps k hledání blízkých obchodů nebo obchodů v jiném umístění, které určuje zákazník.</span><span class="sxs-lookup"><span data-stu-id="2e333-120">The buy online and pick up in store module uses integration with Bing Maps application programming interfaces (APIs) to find nearby stores or stores in another location that the customer specifies.</span></span>

<span data-ttu-id="2e333-121">Modul buy boxu vyžaduje ID produktu.</span><span class="sxs-lookup"><span data-stu-id="2e333-121">A buy box module requires a product ID.</span></span> <span data-ttu-id="2e333-122">Toto ID je odvozeno od kontextu stránky.</span><span class="sxs-lookup"><span data-stu-id="2e333-122">This ID is derived from the page context.</span></span> <span data-ttu-id="2e333-123">Je-li do stránky přidán modul buy boxu, na kterém kontext stránky neobsahuje ID produktu, nebudou informace správně vygenerovány.</span><span class="sxs-lookup"><span data-stu-id="2e333-123">If a buy box module is added to a page where the page context doesn't include a product ID, it won't render the information correctly.</span></span>

## <a name="product-specifications-module"></a><span data-ttu-id="2e333-124">Modul specifikací produktu</span><span class="sxs-lookup"><span data-stu-id="2e333-124">Product specifications module</span></span>

<span data-ttu-id="2e333-125">Modul specifikací produktu lze použít k předvedení dalších podrobností o produktu.</span><span class="sxs-lookup"><span data-stu-id="2e333-125">The product specifications module can be used to showcase additional details about the product.</span></span> <span data-ttu-id="2e333-126">Tyto podrobnosti jsou čerpány z atributů produktu v aplikaci Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="2e333-126">These details are taken from product attributes in Dynamics 365 Retail.</span></span> <span data-ttu-id="2e333-127">V modulu specifikace produktu jsou zobrazeny všechny atributy, pro které je vlastnost **viditelné** nastavena na hodnotu **true**.</span><span class="sxs-lookup"><span data-stu-id="2e333-127">The product specifications module shows every attribute where the **visible** property is set to **true**.</span></span> <span data-ttu-id="2e333-128">K načtení atributů produktu je vyžadováno ID produktu.</span><span class="sxs-lookup"><span data-stu-id="2e333-128">It requires a product ID to retrieve the product attributes.</span></span>

## <a name="recommendations-module"></a><span data-ttu-id="2e333-129">Modul doporučení</span><span class="sxs-lookup"><span data-stu-id="2e333-129">Recommendations module</span></span>

<span data-ttu-id="2e333-130">Nejdůležitějším modulem systému PDP je modul doporučení.</span><span class="sxs-lookup"><span data-stu-id="2e333-130">The recommendations module is an important module on a PDP.</span></span> <span data-ttu-id="2e333-131">Zatímco odběratelé procházejí produkty, měly by jim být prezentovány další možnosti produktu, aby mohli najít správný produkt a nakupovat.</span><span class="sxs-lookup"><span data-stu-id="2e333-131">While customers browse for products, more product options should be presented to them, so that they can find the correct product and make a purchase.</span></span> <span data-ttu-id="2e333-132">Doporučení zákazníkům umožňují snadno objevit související obsah a pokračovat v nákupu.</span><span class="sxs-lookup"><span data-stu-id="2e333-132">Recommendations help customers easily discover related content and continue to shop.</span></span>

<span data-ttu-id="2e333-133">K dispozici jsou různé typy seznamů doporučení:</span><span class="sxs-lookup"><span data-stu-id="2e333-133">Different types of recommendation lists are available:</span></span>

- <span data-ttu-id="2e333-134">Seznam **Lidem se také líbí** je založen na strojovém učení.</span><span class="sxs-lookup"><span data-stu-id="2e333-134">The **People also like** list is based on machine learning.</span></span> <span data-ttu-id="2e333-135">K poskytování doporučení používá historii transakcí ostatních zákazníků.</span><span class="sxs-lookup"><span data-stu-id="2e333-135">It uses the transaction history of other customers to provide recommendations.</span></span> <span data-ttu-id="2e333-136">Tento seznam je vygenerován službou doporučení a připomíná seznam "Zákazníci, kteří toto nakoupili, koupili také...".</span><span class="sxs-lookup"><span data-stu-id="2e333-136">This list is generated by the recommendations service and resembles "Customers who bought this also bought..." lists.</span></span> <span data-ttu-id="2e333-137">K vygenerování tohoto seznamu je nutné ID produktu.</span><span class="sxs-lookup"><span data-stu-id="2e333-137">A product ID is required to generate this list.</span></span>
- <span data-ttu-id="2e333-138">Seznam **Související** lze nakonfigurovat pro produkt v Retail.</span><span class="sxs-lookup"><span data-stu-id="2e333-138">A **Related** list can be configured for a product in Retail.</span></span> <span data-ttu-id="2e333-139">U souvisejícího seznamu lze nakonfigurovat například pro hnědou koženou kabelku další kabelky, které jsou kožené nebo navržené pro cestování.</span><span class="sxs-lookup"><span data-stu-id="2e333-139">For example, for a brown leather travel handbag, more handbags that are leather-based or designed for travel purposes can be configured for the related list.</span></span> <span data-ttu-id="2e333-140">Jiné typy souvisejících seznamů, například **Doplňky** a **Podobně**, lze také konfigurovat v Retail.</span><span class="sxs-lookup"><span data-stu-id="2e333-140">Other types of related lists, such as **Accessories** and **More like this**, can also be configured in Retail.</span></span> <span data-ttu-id="2e333-141">K vygenerování tohoto seznamu je nutné ID produktu.</span><span class="sxs-lookup"><span data-stu-id="2e333-141">A product ID is required to generate this list.</span></span> <span data-ttu-id="2e333-142">Proto, pokud je přidán na domovskou stránku, kde kontext stránky neobsahuje ID produktu, bude seznam prázdný.</span><span class="sxs-lookup"><span data-stu-id="2e333-142">Therefore, if it's added to a home page, where the page context doesn't include a product ID, the list will be empty.</span></span>
- <span data-ttu-id="2e333-143">lgoritmem generované seznamy doporučení, jako je například **Trendující**, **Nejlepe prodávané** a **Nové**, lze použít na PDP.</span><span class="sxs-lookup"><span data-stu-id="2e333-143">Algorithmically generated recommendation lists, such as **Trending**, **Best Selling**, and **New**, can be used on PDPs.</span></span> <span data-ttu-id="2e333-144">Ačkoli tyto seznamy nemusí přímo souviset s produktem v systémech PDP, jsou jiným způsobem, jak zákazníkům pomoci najít produkty, které je mohou zajímat.</span><span class="sxs-lookup"><span data-stu-id="2e333-144">Although these lists might not be directly related to the product on the PDP, they are another way to help customers find products that might interest them.</span></span> <span data-ttu-id="2e333-145">Tyto typy seznamů nevyžadují ID produktu.</span><span class="sxs-lookup"><span data-stu-id="2e333-145">These types of lists don't require a product ID.</span></span> <span data-ttu-id="2e333-146">Jedná se o obecné seznamy, které jsou generovány na základě vzorků nákupu v celém webu.</span><span class="sxs-lookup"><span data-stu-id="2e333-146">They are generic lists that are generated based on shopping patterns across the site.</span></span>
- <span data-ttu-id="2e333-147">Redakční seznamy jsou ručně spravované seznamy.</span><span class="sxs-lookup"><span data-stu-id="2e333-147">Editorial lists are manually curated lists.</span></span> <span data-ttu-id="2e333-148">Maloobchodní prodejce se může například rozhodnout ručně spravovat seznamy výrobků, které chce prezentovat.</span><span class="sxs-lookup"><span data-stu-id="2e333-148">For example, a retailer might decide to manually curate lists of products that it wants to showcase.</span></span>

## <a name="ratings-and-reviews-module"></a><span data-ttu-id="2e333-149">Modul hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="2e333-149">Ratings and reviews module</span></span>

<span data-ttu-id="2e333-150">Modul hodnocení a recenzí zobrazuje hodnocení a recenze poskytované jinými odběrateli.</span><span class="sxs-lookup"><span data-stu-id="2e333-150">The ratings and reviews module shows ratings and reviews that have been provided by other customers.</span></span> <span data-ttu-id="2e333-151">Umožňuje také zákazníkovi napsat vlastní recenzi produktu.</span><span class="sxs-lookup"><span data-stu-id="2e333-151">It also lets a customer write his or her own review of the product.</span></span> <span data-ttu-id="2e333-152">Dále obsahuje histogram, který zobrazuje trend hodnocení produktu.</span><span class="sxs-lookup"><span data-stu-id="2e333-152">Additionally, it includes a histogram that shows the ratings trend for the product.</span></span> <span data-ttu-id="2e333-153">Další podrobnosti získáte v tématu [Přehled hodnocení a recenzí](ratings-reviews-overview.md).</span><span class="sxs-lookup"><span data-stu-id="2e333-153">For more details, see [Ratings and reviews overview](ratings-reviews-overview.md).</span></span>

## <a name="marketing-modules"></a><span data-ttu-id="2e333-154">Moduly marketing</span><span class="sxs-lookup"><span data-stu-id="2e333-154">Marketing modules</span></span>

<span data-ttu-id="2e333-155">Pokud je marketingový obsah jedinečný pro určitý produkt, lze do PDP přidat libovolný marketingový modul.</span><span class="sxs-lookup"><span data-stu-id="2e333-155">If marketing content is unique to a specific product, any marketing module can be added to the PDP.</span></span> <span data-ttu-id="2e333-156">Marketingové moduly můžete přidat do PDP pomocí "obohacení" stránky.</span><span class="sxs-lookup"><span data-stu-id="2e333-156">You can add marketing modules to a PDP by "enriching" the page.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="2e333-157">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="2e333-157">Additional resources</span></span>

[<span data-ttu-id="2e333-158">Přehled domovské stránky</span><span class="sxs-lookup"><span data-stu-id="2e333-158">Overview of the home page</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="2e333-159">Přehled výchozí kategorie cílové stránky a stránka výsledků hledání</span><span class="sxs-lookup"><span data-stu-id="2e333-159">Overview of default category landing page and search results page</span></span>](category-search-page-overview.md)

[<span data-ttu-id="2e333-160">Přehled stránek košíku a pokladny</span><span class="sxs-lookup"><span data-stu-id="2e333-160">Overview of cart and checkout pages</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="2e333-161">Přehled stránek správy účtů</span><span class="sxs-lookup"><span data-stu-id="2e333-161">Overview of account management pages</span></span>](quick-tour-account-management.md)
