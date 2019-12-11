---
title: Konfigurace hodnocení a recenzí
description: V tomto tématu je popsán postup při konfiguraci webu elektronického obchodování pro zobrazení hodnocení a recenzí zákazníků v řešení Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0612b32e7751b32ad851f627a53bce2ac491870f
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770474"
---
# <a name="configure-ratings-and-reviews"></a><span data-ttu-id="5235a-103">Konfigurace hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="5235a-103">Configure ratings and reviews</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="5235a-104">V tomto tématu je popsán postup při konfiguraci webu elektronického obchodování pro zobrazení hodnocení a recenzí zákazníků v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5235a-104">This topic describes how to configure your e-Commerce site to show customer ratings and reviews in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5235a-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="5235a-105">Overview</span></span>

<span data-ttu-id="5235a-106">Hodnocení a recenze na webech elektronických obchodů pomáhají zákazníkům lépe se seznámit s produkty před tím, než se je rozhodnou zakoupit, a to zobrazením, co si ostatní zákazníci o těchto produktech myslí.</span><span class="sxs-lookup"><span data-stu-id="5235a-106">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision, by showing them what other customers think about those products.</span></span> <span data-ttu-id="5235a-107">U webů elektronického obchodování jsou hodnocení a recenze také mechanismem pro shromažďování názorů o produktech od zákazníků.</span><span class="sxs-lookup"><span data-stu-id="5235a-107">For e-Commerce websites, ratings and reviews are also a mechanism for collecting customer feedback about products.</span></span> 

<span data-ttu-id="5235a-108">Hodnocení se zobrazují na stránkách seznamů produktů, na stránkách se seznamem kategorií, na stránkách výsledků hledání a na dalších stránkách webu.</span><span class="sxs-lookup"><span data-stu-id="5235a-108">Ratings are shown on product list pages, category list pages, search results pages, and other site pages.</span></span> <span data-ttu-id="5235a-109">Histogramy hodnocení a recenze produktů jsou zobrazeny na stránkách s podrobnostmi o produktu.</span><span class="sxs-lookup"><span data-stu-id="5235a-109">Ratings histograms and product reviews are shown on product details pages (PDPs).</span></span> <span data-ttu-id="5235a-110">Tlačítko **Napsat recenzi** umožňuje zákazníkům předkládat hodnocení a recenze produktu.</span><span class="sxs-lookup"><span data-stu-id="5235a-110">A **Write a review** button lets customers submit ratings and reviews for a product.</span></span>

## <a name="ratings-and-reviews-modules-on-pdps"></a><span data-ttu-id="5235a-111">Moduly hodnocení a recenzí na stránkách s podrobnostmi o produktu</span><span class="sxs-lookup"><span data-stu-id="5235a-111">Ratings and reviews modules on PDPs</span></span> 

<span data-ttu-id="5235a-112">Ve třech modulech se zobrazuje souhrn hodnocení a recenzí na stránce s podrobnostmi o produktu:</span><span class="sxs-lookup"><span data-stu-id="5235a-112">Three modules show the ratings and reviews summary on PDPs:</span></span>

- <span data-ttu-id="5235a-113">Modul pro napsání recenze</span><span class="sxs-lookup"><span data-stu-id="5235a-113">Write review module</span></span>
- <span data-ttu-id="5235a-114">Modul seznamu recenzí produktu</span><span class="sxs-lookup"><span data-stu-id="5235a-114">Product reviews list module</span></span>
- <span data-ttu-id="5235a-115">Modul histogramu hodnocení</span><span class="sxs-lookup"><span data-stu-id="5235a-115">Ratings histogram module</span></span>
 
<span data-ttu-id="5235a-116">Následující obrázek ukazuje, jak vypadají moduly hodnocení a recenzí na stránce s podrobnostmi o produktu.</span><span class="sxs-lookup"><span data-stu-id="5235a-116">The following illustration shows what the ratings and reviews modules look like on a PDP.</span></span>

![Hodnocení a recenzí na stránce s podrobnostmi o produktu](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> <span data-ttu-id="5235a-118">Informace, jak optimalizovat šablony a rozložení stránky s podrobnostmi o produktu tak, aby bylo možné sdílet konfigurace pro moduly hodnocení a recenzí mezi několika stránkami s podrobnostmi o produktu na vašem webu elektronického obchodu, naleznete v tématu [Přehled šablon a rozložení](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5235a-118">For information about how to optimize PDP templates and layouts so that you can share the configurations for ratings and reviews modules among multiple PDPs on your e-Commerce site, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

<span data-ttu-id="5235a-119">Následující obrázek ukazuje, jak dialogové okno **Přidat modul** zobrazuje moduly hodnocení a recenzí v aplikaci řešení Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5235a-119">The following illustration shows how the **Add module** dialog box presents ratings and reviews modules in Dynamics 365 Commerce.</span></span>

![Dialogové okno Přidat modul](media/rnr-eCommerce-pdp-adding-rnr-modules.png)

### <a name="write-review-module"></a><span data-ttu-id="5235a-121">Modul pro napsání recenze</span><span class="sxs-lookup"><span data-stu-id="5235a-121">Write review module</span></span>

<span data-ttu-id="5235a-122">Modul pro napsání recenze obsahuje tlačítko **Napsat recenzi**, které uživateli umožňuje přihlásit se, přiřadit hodnocení a napsat recenzi produktu.</span><span class="sxs-lookup"><span data-stu-id="5235a-122">The write review module includes a **Write a review** button that lets users sign in, assign a rating, and write a review of a product.</span></span> <span data-ttu-id="5235a-123">Tento modul dále umožňuje uživatelům upravit dříve odeslané hodnocení nebo recenzi.</span><span class="sxs-lookup"><span data-stu-id="5235a-123">This module also lets users edit a rating or review that they previously submitted.</span></span> <span data-ttu-id="5235a-124">Tento modul se obvykle zobrazí nad moduly histogramu hodnocení a seznamu recenzí produktu na stránce s podrobnostmi o produktu.</span><span class="sxs-lookup"><span data-stu-id="5235a-124">This module typically appears above the ratings histogram and product reviews list modules on a PDP.</span></span>

<span data-ttu-id="5235a-125">Následující ilustrace znázorňuje dialogové okno **Napsat recenzi**, které se zobrazí, když zákazník vybere možnost **Napsat recenzi**.</span><span class="sxs-lookup"><span data-stu-id="5235a-125">The following illustration shows the **Write a review** dialog box that appears when a customer selects **Write a review**.</span></span> <span data-ttu-id="5235a-126">Zákazník může toto dialogové okno použít k odeslání hodnocení a recenze.</span><span class="sxs-lookup"><span data-stu-id="5235a-126">The customer can use this dialog box to submit a rating and a review.</span></span>

![Dialogové okno Napsat recenzi](media/rnr-eCommerce-write-review-module.png)

<span data-ttu-id="5235a-128">V následující tabulce je uvedena vlastnost modulu pro napsání recenze, kterou je nutné nakonfigurovat v nástroji pro tvorbu obsahu.</span><span class="sxs-lookup"><span data-stu-id="5235a-128">The following table shows the write review module property that needs to be configured in the authoring tool.</span></span>

| <span data-ttu-id="5235a-129">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="5235a-129">Property name</span></span> | <span data-ttu-id="5235a-130">Hodnota</span><span class="sxs-lookup"><span data-stu-id="5235a-130">Value</span></span>        | <span data-ttu-id="5235a-131">Popis vlastnosti</span><span class="sxs-lookup"><span data-stu-id="5235a-131">Property description</span></span>                 |
|---------------|--------------|--------------------------------------|
| <span data-ttu-id="5235a-132">Název</span><span class="sxs-lookup"><span data-stu-id="5235a-132">Name</span></span>          | <span data-ttu-id="5235a-133">Napsat recenzi</span><span class="sxs-lookup"><span data-stu-id="5235a-133">Write review</span></span> | <span data-ttu-id="5235a-134">Název modulu pro napsání recenze.</span><span class="sxs-lookup"><span data-stu-id="5235a-134">The name of the write review module.</span></span> |

### <a name="ratings-histogram-module"></a><span data-ttu-id="5235a-135">Modul histogramu hodnocení</span><span class="sxs-lookup"><span data-stu-id="5235a-135">Ratings histogram module</span></span>

<span data-ttu-id="5235a-136">V modulu histogramu hodnocení se zobrazuje histogram hodnocení.</span><span class="sxs-lookup"><span data-stu-id="5235a-136">The ratings histogram module shows a ratings histogram.</span></span> <span data-ttu-id="5235a-137">Tento modul se obvykle nachází mezi modulem pro napsání recenze a modulem seznamu recenzí produktu na stránce s podrobnostmi o produktu.</span><span class="sxs-lookup"><span data-stu-id="5235a-137">This module typically appears between the write review module and the product reviews list module on a PDP.</span></span>

<span data-ttu-id="5235a-138">Modul histogramu hodnocení nevyžaduje žádnou konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="5235a-138">The ratings histogram module requires no configuration.</span></span> <span data-ttu-id="5235a-139">Stačí pouze přidat modul do šablony stránky s podrobnostmi o produktu.</span><span class="sxs-lookup"><span data-stu-id="5235a-139">You just have to add the module in the PDP template.</span></span> 

<span data-ttu-id="5235a-140">Následující ilustrace ukazuje, jak vypadá šablona stránky s podrobnostmi o produktu v řešení Dynamics 365 Commerce, když jsou moduly hodnocení a recenzí nakonfigurovány pro zobrazení na stránce s podrobnostmi o produktu.</span><span class="sxs-lookup"><span data-stu-id="5235a-140">The following illustrations shows what a PDP template looks like in Dynamics 365 Commerce when ratings and reviews modules are configured for display on PDPs.</span></span>

![Šablona stránky s podrobnostmi o produktu při konfiguraci hodnocení a recenzí na stránkách s podrobnostmi o produktu](media/rnr-eCommerce-pdp-reviews-modules.png)

### <a name="product-reviews-list-module"></a><span data-ttu-id="5235a-142">Modul seznamu recenzí produktu</span><span class="sxs-lookup"><span data-stu-id="5235a-142">Product reviews list module</span></span>

<span data-ttu-id="5235a-143">V modulu seznam recenzí produktu se zobrazuje seznam recenzí produktů spolu s možnostmi řazení, filtrování a stránkování.</span><span class="sxs-lookup"><span data-stu-id="5235a-143">The product reviews list module shows a list of product reviews together with sort, filter, and pagination options.</span></span> <span data-ttu-id="5235a-144">Tento modul se obvykle zobrazuje za modulem histogramu hodnocení na stránce s podrobnostmi o produktu.</span><span class="sxs-lookup"><span data-stu-id="5235a-144">This module typically appears after the ratings histogram module on a PDP.</span></span>

<span data-ttu-id="5235a-145">V následující tabulce jsou uvedeny vlastnosti modulu seznamu recenzí produktu, které je nutné nakonfigurovat v nástroji pro tvorbu obsahu.</span><span class="sxs-lookup"><span data-stu-id="5235a-145">The following table shows the product reviews list module properties that need to be configured in the authoring tool.</span></span>

| <span data-ttu-id="5235a-146">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="5235a-146">Property name</span></span>              | <span data-ttu-id="5235a-147">Hodnota</span><span class="sxs-lookup"><span data-stu-id="5235a-147">Value</span></span> | <span data-ttu-id="5235a-148">Popis vlastnosti</span><span class="sxs-lookup"><span data-stu-id="5235a-148">Property description</span></span> |
|----------------------------|-------| ---------------------|
| <span data-ttu-id="5235a-149">Recenze zobrazené na každé stránce</span><span class="sxs-lookup"><span data-stu-id="5235a-149">Reviews shown on each page</span></span> | <span data-ttu-id="5235a-150">10</span><span class="sxs-lookup"><span data-stu-id="5235a-150">10</span></span>    | <span data-ttu-id="5235a-151">Počet recenzí, které mají být zobrazeny v čase na stránce s podrobnostmi o produktu.</span><span class="sxs-lookup"><span data-stu-id="5235a-151">The number of reviews that should be shown at a time on a PDP.</span></span> <span data-ttu-id="5235a-152">Součástí jsou tlačítka **Další** a **Předchozí**, aby se uživatelé mohli pohybovat na stránkách recenzí.</span><span class="sxs-lookup"><span data-stu-id="5235a-152">**Next** and **Previous** buttons are included, so that users can move through the pages of reviews.</span></span> |

#### <a name="ratings-histogram--summary-view"></a><span data-ttu-id="5235a-153">Histogram hodnocení – souhrnné zobrazení</span><span class="sxs-lookup"><span data-stu-id="5235a-153">Ratings histogram – Summary view</span></span>

<span data-ttu-id="5235a-154">Modul seznamu recenzí produktu obsahuje pozici, do níž lze přidat modul histogramu hodnocení.</span><span class="sxs-lookup"><span data-stu-id="5235a-154">The product reviews list module includes a slot where you can add a ratings histogram module.</span></span> <span data-ttu-id="5235a-155">Následující obrázek znázorňuje, jak lze přidat modul histogramu hodnocení do modulu seznamu recenzí produktu v řešení Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5235a-155">The following illustration shows how you can add a ratings histogram module in the product reviews list module in Dynamics 365 Commerce.</span></span>

![Přidání modulu histogramu hodnocení do modulu seznamu recenzí produktu](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="configure-a-site-to-show-ratings-and-reviews"></a><span data-ttu-id="5235a-157">Konfigurace webu pro zobrazení hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="5235a-157">Configure a site to show ratings and reviews</span></span>

<span data-ttu-id="5235a-158">Hodnoty konfigurace hodnocení a recenzí, jako je například ID klienta, délka textu recenze a délka názvu recenze, jsou konfigurovány na úrovni webu.</span><span class="sxs-lookup"><span data-stu-id="5235a-158">Configuration values for ratings and reviews, such as the tenant ID, review text length, and review title length, are configured at the site level.</span></span> 

<span data-ttu-id="5235a-159">Chcete-li nakonfigurovat web tak, aby zobrazoval hodnocení a recenze, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="5235a-159">To configure a site to show ratings and reviews, follow these steps.</span></span> 

1. <span data-ttu-id="5235a-160">Přejděte do umístění **Domů \> Weby**.</span><span class="sxs-lookup"><span data-stu-id="5235a-160">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="5235a-161">Vyberte název webu.</span><span class="sxs-lookup"><span data-stu-id="5235a-161">Select the name of your site.</span></span> 
1. <span data-ttu-id="5235a-162">Přejděte na **Správa webu \> Rozšiřitelnost**.</span><span class="sxs-lookup"><span data-stu-id="5235a-162">Go to **Site management \> Extensibility**.</span></span> 
1. <span data-ttu-id="5235a-163">Do pole **Maximální délka textu recenze** zadejte maximální počet znaků textu recenze (například **1000**).</span><span class="sxs-lookup"><span data-stu-id="5235a-163">In the **Review Text Max Length** field, enter the maximum number of characters that review text can have (for example, **1000**).</span></span> 
1. <span data-ttu-id="5235a-164">Do pole **Maximální délka názvu recenze** zadejte maximální počet znaků názvu recenze (například **55**).</span><span class="sxs-lookup"><span data-stu-id="5235a-164">In the **Review Title Max Length** field, enter the maximum number of characters that review titles can have (for example, **55**).</span></span> 
1. <span data-ttu-id="5235a-165">Vyberte možnost **Uložit a publikovat**.</span><span class="sxs-lookup"><span data-stu-id="5235a-165">Select **Save and Publish**.</span></span> 

<span data-ttu-id="5235a-166">Následující obrázek znázorňuje, jak vypadá tato konfigurace v řešení Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5235a-166">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Konfigurace webu pro zobrazení hodnocení a recenzí](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a><span data-ttu-id="5235a-168">Propojení hodnocení produktu se sekcí Recenze na stránce s podrobnostmi o produktu</span><span class="sxs-lookup"><span data-stu-id="5235a-168">Link a product rating to the Reviews section of a PDP</span></span>

<span data-ttu-id="5235a-169">Hodnocení produktu je uvedeno pod názvem produktu nahoře na stránce s podrobnostmi o produktu.</span><span class="sxs-lookup"><span data-stu-id="5235a-169">A product rating is shown below the product title at the top of PDP.</span></span> <span data-ttu-id="5235a-170">Hodnocení produktu lze nakonfigurovat tak, aby bylo propojeno se sekcí **Recenze** na stejné stránce s podrobnostmi o produktu.</span><span class="sxs-lookup"><span data-stu-id="5235a-170">The product rating can be configured so that it's linked to the **Reviews** section of the same PDP.</span></span> 

<span data-ttu-id="5235a-171">Chcete-li propojit hodnocení produktu se sekcí **Recenze** na stránce s podrobnostmi o produktu, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="5235a-171">To link a product rating to the **Reviews** section of the PDP, follow these steps.</span></span>

1. <span data-ttu-id="5235a-172">Otevřete šablonu stránky s podrobnostmi o produktu.</span><span class="sxs-lookup"><span data-stu-id="5235a-172">Open the PDP template.</span></span> 
1. <span data-ttu-id="5235a-173">Přejít na **Nastavení modulu kontejneru buy boxu**.</span><span class="sxs-lookup"><span data-stu-id="5235a-173">Go to **Buy box container module settings**.</span></span>
1. <span data-ttu-id="5235a-174">V části **Buy box** vyberte **Hodnocení produktu** a poté zaškrtněte políčko **Propojit kliknutí s úplným modulem recenzí**.</span><span class="sxs-lookup"><span data-stu-id="5235a-174">Under **Buy box**, select **Product ratings**, and then select the **Link the click to full reviews module** check box.</span></span>

<span data-ttu-id="5235a-175">Následující obrázek znázorňuje, jak vypadá tato konfigurace v řešení Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5235a-175">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Propojení hodnocení produktu se sekcí Recenze na stránce s podrobnostmi o produktu](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a><span data-ttu-id="5235a-177">Konfigurace odkazu na stránku ochrany osobních údajů a zásad</span><span class="sxs-lookup"><span data-stu-id="5235a-177">Configure the link for the privacy and policy page</span></span>

<span data-ttu-id="5235a-178">Chcete-li konfigurovat odkaz na stránku ochrany osobních údajů a zásad, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="5235a-178">To configure the link for the privacy and policy page, follow these steps.</span></span>

1. <span data-ttu-id="5235a-179">Přejděte do umístění **Domů \> Weby**.</span><span class="sxs-lookup"><span data-stu-id="5235a-179">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="5235a-180">Vyberte název webu.</span><span class="sxs-lookup"><span data-stu-id="5235a-180">Select the name of your site.</span></span> 
1. <span data-ttu-id="5235a-181">Přejděte na **Správa webu \> Rozšiřitelnost**.</span><span class="sxs-lookup"><span data-stu-id="5235a-181">Go to **Site management \> Extensibility**</span></span>
1. <span data-ttu-id="5235a-182">Na kartě **Trasy** v části **Ochrana osobních údajů a zásady RNR** vyberte možnost **Přidat odkaz**.</span><span class="sxs-lookup"><span data-stu-id="5235a-182">On the **Routes** tab, under **RNR Privacy and Policy**, select **Add a link**.</span></span> <span data-ttu-id="5235a-183">Je-li již zadán odkaz a chcete jej nahradit, vyberte odkaz.</span><span class="sxs-lookup"><span data-stu-id="5235a-183">If a link is already entered, and you want to replace it, select the link.</span></span> 
1. <span data-ttu-id="5235a-184">V dialogovém okně **Přidat odkaz** vyberte odkaz na stránku ochrany osobních údajů a zásad a poté klepněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="5235a-184">In the **Add a link** dialog box, select the link for the privacy and policy page, and then select **OK**.</span></span> 
1. <span data-ttu-id="5235a-185">Vyberte možnost **Uložit a publikovat**.</span><span class="sxs-lookup"><span data-stu-id="5235a-185">Select **Save and Publish**.</span></span> 

<span data-ttu-id="5235a-186">Následující obrázek znázorňuje, jak vypadá tato konfigurace v řešení Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5235a-186">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Konfigurace odkazu na stránku ochrany osobních údajů a zásad](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="additional-resources"></a><span data-ttu-id="5235a-188">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="5235a-188">Additional resources</span></span>

[<span data-ttu-id="5235a-189">Přehled hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="5235a-189">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="5235a-190">Připojení k používání hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="5235a-190">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="5235a-191">Správa hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="5235a-191">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="5235a-192">Synchronizace hodnocení produktů v Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="5235a-192">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
