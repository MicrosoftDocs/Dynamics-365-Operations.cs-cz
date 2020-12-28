---
title: Moduly hodnocení a recenzí
description: Toto téma popisuje moduly hodnocení a recenzí použité na stránkách s podrobnostmi o produktu v řešení Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 09/15/2020
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
ms.author: gmohanv
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: Release 10.0.6
ms.openlocfilehash: 85fb1272103eed7d6e44635b7c20438471d96b34
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410884"
---
# <a name="ratings-and-reviews-modules"></a><span data-ttu-id="42001-103">Moduly hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="42001-103">Ratings and reviews modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="42001-104">Toto téma popisuje moduly hodnocení a recenzí použité na stránkách s podrobnostmi o produktu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="42001-104">This topic covers ratings and reviews modules used on product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="42001-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="42001-105">Overview</span></span>

<span data-ttu-id="42001-106">Hodnocení a recenze na webech elektronických obchodů pomáhají zákazníkům lépe se seznámit s produkty před tím, než se je rozhodnou zakoupit, a představují také mechanismus ke shromažďování zpětné vazby uživatelů ohledně produktů.</span><span class="sxs-lookup"><span data-stu-id="42001-106">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision, and are also a mechanism for collecting customer feedback about products.</span></span> 

<span data-ttu-id="42001-107">Hodnocení se zobrazují na stránkách seznamů produktů, na stránkách se seznamem kategorií, na stránkách výsledků hledání a na dalších stránkách webu.</span><span class="sxs-lookup"><span data-stu-id="42001-107">Ratings are shown on product list pages, category list pages, search results pages, and other site pages.</span></span> 

<span data-ttu-id="42001-108">Histogramy hodnocení a recenze produktů jsou zobrazeny na stránkách s podrobnostmi o produktu.</span><span class="sxs-lookup"><span data-stu-id="42001-108">Ratings histograms and product reviews are shown on PDPs.</span></span> <span data-ttu-id="42001-109">Tlačítko **Napsat recenzi** umožňuje zákazníkům předkládat hodnocení a recenze produktu.</span><span class="sxs-lookup"><span data-stu-id="42001-109">A **Write a review** button lets customers submit ratings and reviews for a product.</span></span> <span data-ttu-id="42001-110">Tyto funkce jsou řízeny moduly hodnocení a recenzí.</span><span class="sxs-lookup"><span data-stu-id="42001-110">These PDP features are controlled by ratings and review modules.</span></span>

## <a name="ratings-and-reviews-modules-on-pdps"></a><span data-ttu-id="42001-111">Moduly hodnocení a recenzí na stránkách s podrobnostmi o produktu</span><span class="sxs-lookup"><span data-stu-id="42001-111">Ratings and reviews modules on PDPs</span></span> 

<span data-ttu-id="42001-112">Ve třech modulech se zobrazuje souhrn hodnocení a recenzí na stránce s podrobnostmi o produktu:</span><span class="sxs-lookup"><span data-stu-id="42001-112">Three modules show the ratings and reviews summary on PDPs:</span></span>
- <span data-ttu-id="42001-113">Modul pro napsání recenze</span><span class="sxs-lookup"><span data-stu-id="42001-113">Write review module</span></span>
- <span data-ttu-id="42001-114">Modul seznamu recenzí produktu</span><span class="sxs-lookup"><span data-stu-id="42001-114">Product reviews list module</span></span>
- <span data-ttu-id="42001-115">Modul histogramu hodnocení</span><span class="sxs-lookup"><span data-stu-id="42001-115">Ratings histogram module</span></span>
 
<span data-ttu-id="42001-116">Následující obrázek ukazuje, jak vypadají moduly hodnocení a recenzí na stránce s podrobnostmi o produktu.</span><span class="sxs-lookup"><span data-stu-id="42001-116">The following illustration shows what the ratings and reviews modules look like on a PDP.</span></span>

![Hodnocení a recenzí na stránce s podrobnostmi o produktu](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> <span data-ttu-id="42001-118">Informace, jak optimalizovat šablony a rozložení stránky s podrobnostmi o produktu tak, aby bylo možné sdílet konfigurace pro moduly hodnocení a recenzí mezi několika stránkami s podrobnostmi o produktu na vašem webu elektronického obchodu, naleznete v tématu [Přehled šablon a rozložení](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="42001-118">For information about how to optimize PDP templates and layouts so that you can share the configurations for ratings and reviews modules among multiple PDPs on your e-Commerce site, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

<span data-ttu-id="42001-119">Následující obrázek ukazuje, jak dialogové okno **Přidat modul** zobrazuje moduly hodnocení a recenzí v aplikaci řešení Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="42001-119">The following illustration shows how the **Add module** dialog box presents ratings and reviews modules in Dynamics 365 Commerce.</span></span>
<span data-ttu-id="42001-120">![Dialogové okno Přidat modul](media/rnr-eCommerce-pdp-adding-rnr-modules.png)</span><span class="sxs-lookup"><span data-stu-id="42001-120">![Add module dialog box](media/rnr-eCommerce-pdp-adding-rnr-modules.png)</span></span>

### <a name="write-review-module"></a><span data-ttu-id="42001-121">Modul pro napsání recenze</span><span class="sxs-lookup"><span data-stu-id="42001-121">Write review module</span></span>

<span data-ttu-id="42001-122">Modul pro napsání recenze obsahuje tlačítko **Napsat recenzi**, které uživateli umožňuje přihlásit se, přiřadit hodnocení a napsat recenzi produktu.</span><span class="sxs-lookup"><span data-stu-id="42001-122">The write review module includes a **Write a review** button that lets users sign in, assign a rating, and write a review of a product.</span></span> <span data-ttu-id="42001-123">Tento modul dále umožňuje uživatelům upravit dříve odeslané hodnocení nebo recenzi.</span><span class="sxs-lookup"><span data-stu-id="42001-123">This module also lets users edit a rating or review that they previously submitted.</span></span> <span data-ttu-id="42001-124">Tento modul se obvykle zobrazí nad moduly histogramu hodnocení a seznamu recenzí produktu na stránce s podrobnostmi o produktu.</span><span class="sxs-lookup"><span data-stu-id="42001-124">This module typically appears above the ratings histogram and product reviews list modules on a PDP.</span></span>
<span data-ttu-id="42001-125">Následující ilustrace znázorňuje dialogové okno **Napsat recenzi**, které se zobrazí, když zákazník vybere možnost **Napsat recenzi**.</span><span class="sxs-lookup"><span data-stu-id="42001-125">The following illustration shows the **Write a review** dialog box that appears when a customer selects **Write a review**.</span></span> <span data-ttu-id="42001-126">Zákazník může toto dialogové okno použít k odeslání hodnocení a recenze.</span><span class="sxs-lookup"><span data-stu-id="42001-126">The customer can use this dialog box to submit a rating and a review.</span></span>
<span data-ttu-id="42001-127">![Dialogové okno Napsat recenzi](media/rnr-eCommerce-write-review-module.png) V následující tabulce je uvedena vlastnost modulu pro napsání recenze, kterou je nutné nakonfigurovat v nástroji pro tvorbu obsahu.</span><span class="sxs-lookup"><span data-stu-id="42001-127">![Write a review dialog box](media/rnr-eCommerce-write-review-module.png) The following table shows the write review module property that needs to be configured in the authoring tool.</span></span>
| <span data-ttu-id="42001-128">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="42001-128">Property name</span></span> | <span data-ttu-id="42001-129">Hodnota</span><span class="sxs-lookup"><span data-stu-id="42001-129">Value</span></span>        | <span data-ttu-id="42001-130">Popis vlastnosti</span><span class="sxs-lookup"><span data-stu-id="42001-130">Property description</span></span>                 |
|---------------|--------------|--------------------------------------|
| <span data-ttu-id="42001-131">Název</span><span class="sxs-lookup"><span data-stu-id="42001-131">Name</span></span>          | <span data-ttu-id="42001-132">Napsat recenzi</span><span class="sxs-lookup"><span data-stu-id="42001-132">Write review</span></span> | <span data-ttu-id="42001-133">Název modulu pro napsání recenze.</span><span class="sxs-lookup"><span data-stu-id="42001-133">The name of the write review module.</span></span> |

### <a name="ratings-histogram-module"></a><span data-ttu-id="42001-134">Modul histogramu hodnocení</span><span class="sxs-lookup"><span data-stu-id="42001-134">Ratings histogram module</span></span>

<span data-ttu-id="42001-135">V modulu histogramu hodnocení se zobrazuje histogram hodnocení.</span><span class="sxs-lookup"><span data-stu-id="42001-135">The ratings histogram module shows a ratings histogram.</span></span> <span data-ttu-id="42001-136">Tento modul se obvykle nachází mezi modulem pro napsání recenze a modulem seznamu recenzí produktu na stránce s podrobnostmi o produktu.</span><span class="sxs-lookup"><span data-stu-id="42001-136">This module typically appears between the write review module and the product reviews list module on a PDP.</span></span>
<span data-ttu-id="42001-137">Modul histogramu hodnocení nevyžaduje žádnou konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="42001-137">The ratings histogram module requires no configuration.</span></span> <span data-ttu-id="42001-138">Stačí pouze přidat modul do šablony stránky s podrobnostmi o produktu.</span><span class="sxs-lookup"><span data-stu-id="42001-138">You just have to add the module in the PDP template.</span></span> <span data-ttu-id="42001-139">Následující ilustrace ukazuje, jak vypadá šablona stránky s podrobnostmi o produktu v řešení Dynamics 365 Commerce, když jsou moduly hodnocení a recenzí nakonfigurovány pro zobrazení na stránce s podrobnostmi o produktu.</span><span class="sxs-lookup"><span data-stu-id="42001-139">The following illustrations shows what a PDP template looks like in Dynamics 365 Commerce when ratings and reviews modules are configured for display on PDPs.</span></span>
<span data-ttu-id="42001-140">![Šablona stránky s podrobnostmi o produktu při konfiguraci hodnocení a recenzí na stránkách s podrobnostmi o produktu](media/rnr-eCommerce-pdp-reviews-modules.png)</span><span class="sxs-lookup"><span data-stu-id="42001-140">![PDP template when ratings and reviews are configured for display on PDPs](media/rnr-eCommerce-pdp-reviews-modules.png)</span></span>

### <a name="product-reviews-list-module"></a><span data-ttu-id="42001-141">Modul seznamu recenzí produktu</span><span class="sxs-lookup"><span data-stu-id="42001-141">Product reviews list module</span></span>

<span data-ttu-id="42001-142">V modulu seznam recenzí produktu se zobrazuje seznam recenzí produktů spolu s možnostmi řazení, filtrování a stránkování.</span><span class="sxs-lookup"><span data-stu-id="42001-142">The product reviews list module shows a list of product reviews together with sort, filter, and pagination options.</span></span> <span data-ttu-id="42001-143">Tento modul se obvykle zobrazuje za modulem histogramu hodnocení na stránce s podrobnostmi o produktu.</span><span class="sxs-lookup"><span data-stu-id="42001-143">This module typically appears after the ratings histogram module on a PDP.</span></span>
<span data-ttu-id="42001-144">V následující tabulce jsou uvedeny vlastnosti modulu seznamu recenzí produktu, které je nutné nakonfigurovat v nástroji pro tvorbu obsahu.</span><span class="sxs-lookup"><span data-stu-id="42001-144">The following table shows the product reviews list module properties that need to be configured in the authoring tool.</span></span>

| <span data-ttu-id="42001-145">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="42001-145">Property name</span></span>              | <span data-ttu-id="42001-146">Hodnota</span><span class="sxs-lookup"><span data-stu-id="42001-146">Value</span></span> | <span data-ttu-id="42001-147">Popis vlastnosti</span><span class="sxs-lookup"><span data-stu-id="42001-147">Property description</span></span> |
|----------------------------|-------| ---------------------|
| <span data-ttu-id="42001-148">Recenze zobrazené na každé stránce</span><span class="sxs-lookup"><span data-stu-id="42001-148">Reviews shown on each page</span></span> | <span data-ttu-id="42001-149">10</span><span class="sxs-lookup"><span data-stu-id="42001-149">10</span></span>    | <span data-ttu-id="42001-150">Počet recenzí, které mají být zobrazeny v čase na stránce s podrobnostmi o produktu.</span><span class="sxs-lookup"><span data-stu-id="42001-150">The number of reviews that should be shown at a time on a PDP.</span></span> <span data-ttu-id="42001-151">Součástí jsou tlačítka **Další** a **Předchozí**, aby se uživatelé mohli pohybovat na stránkách recenzí.</span><span class="sxs-lookup"><span data-stu-id="42001-151">**Next** and **Previous** buttons are included, so that users can move through the pages of reviews.</span></span> |

#### <a name="ratings-histogram--summary-view"></a><span data-ttu-id="42001-152">Histogram hodnocení – souhrnné zobrazení</span><span class="sxs-lookup"><span data-stu-id="42001-152">Ratings histogram – Summary view</span></span>

<span data-ttu-id="42001-153">Modul seznamu recenzí produktu obsahuje pozici, do níž lze přidat modul histogramu hodnocení.</span><span class="sxs-lookup"><span data-stu-id="42001-153">The product reviews list module includes a slot where you can add a ratings histogram module.</span></span> <span data-ttu-id="42001-154">Následující obrázek znázorňuje, jak lze přidat modul histogramu hodnocení do modulu seznamu recenzí produktu v řešení Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="42001-154">The following illustration shows how you can add a ratings histogram module in the product reviews list module in Dynamics 365 Commerce.</span></span>

![Přidání modulu histogramu hodnocení do modulu seznamu recenzí produktu](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="additional-resources"></a><span data-ttu-id="42001-156">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="42001-156">Additional resources</span></span>

[<span data-ttu-id="42001-157">Přehled knihovny modulů</span><span class="sxs-lookup"><span data-stu-id="42001-157">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="42001-158">Modul kontejneru</span><span class="sxs-lookup"><span data-stu-id="42001-158">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="42001-159">Modul košíku</span><span class="sxs-lookup"><span data-stu-id="42001-159">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="42001-160">Modul pokladny</span><span class="sxs-lookup"><span data-stu-id="42001-160">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="42001-161">Modul potvrzení objednávky</span><span class="sxs-lookup"><span data-stu-id="42001-161">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="42001-162">Modul záhlaví</span><span class="sxs-lookup"><span data-stu-id="42001-162">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="42001-163">Modul zápatí</span><span class="sxs-lookup"><span data-stu-id="42001-163">Footer module</span></span>](author-footer-module.md)
