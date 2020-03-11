---
title: Konfigurace hodnocení a recenzí
description: V tomto tématu je popsán postup při konfiguraci webu elektronického obchodování pro zobrazení hodnocení a recenzí zákazníků v řešení Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 02/17/2020
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
ms.openlocfilehash: edd2082b5d2cafcb955f8e3c7762bcba523ac479
ms.sourcegitcommit: 0dace221e8874021dd212271567666f717d39793
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/19/2020
ms.locfileid: "3071559"
---
# <a name="configure-ratings-and-reviews"></a><span data-ttu-id="d3e22-103">Konfigurace hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="d3e22-103">Configure ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d3e22-104">V tomto tématu je popsán postup při konfiguraci webu elektronického obchodování pro zobrazení hodnocení a recenzí zákazníků v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d3e22-104">This topic describes how to configure your e-Commerce site to show customer ratings and reviews in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d3e22-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="d3e22-105">Overview</span></span>

<span data-ttu-id="d3e22-106">Hodnocení a recenze na webech elektronických obchodů pomáhají zákazníkům lépe se seznámit s produkty před tím, než se je rozhodnou zakoupit, a to zobrazením, co si ostatní zákazníci o těchto produktech myslí.</span><span class="sxs-lookup"><span data-stu-id="d3e22-106">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision by showing them what other customers think about those products.</span></span> <span data-ttu-id="d3e22-107">U webů elektronického obchodování jsou hodnocení a recenze také mechanismem pro shromažďování názorů o produktech od zákazníků.</span><span class="sxs-lookup"><span data-stu-id="d3e22-107">For e-Commerce websites, ratings and reviews are also a mechanism for collecting customer feedback about products.</span></span> 

## <a name="configure-a-site-to-show-ratings-and-reviews"></a><span data-ttu-id="d3e22-108">Konfigurace webu pro zobrazení hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="d3e22-108">Configure a site to show ratings and reviews</span></span>

<span data-ttu-id="d3e22-109">Hodnoty konfigurace hodnocení a recenzí, jako je například ID klienta, délka textu recenze a délka názvu recenze, jsou konfigurovány na úrovni webu.</span><span class="sxs-lookup"><span data-stu-id="d3e22-109">Configuration values for ratings and reviews, such as the tenant ID, review text length, and review title length, are configured at the site level.</span></span> 

<span data-ttu-id="d3e22-110">Chcete-li nakonfigurovat web tak, aby zobrazoval hodnocení a recenze, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="d3e22-110">To configure a site to show ratings and reviews, follow these steps.</span></span> 

1. <span data-ttu-id="d3e22-111">Přejděte do umístění **Domů \> Weby**.</span><span class="sxs-lookup"><span data-stu-id="d3e22-111">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="d3e22-112">Vyberte název webu.</span><span class="sxs-lookup"><span data-stu-id="d3e22-112">Select the name of your site.</span></span> 
1. <span data-ttu-id="d3e22-113">Přejděte na **Nastavení webu \> Rozšíření**.</span><span class="sxs-lookup"><span data-stu-id="d3e22-113">Go to **Site settings \> Extensions**.</span></span> 
1. <span data-ttu-id="d3e22-114">Do pole **Maximální délka textu recenze** zadejte maximální počet znaků textu recenze (například **1000**).</span><span class="sxs-lookup"><span data-stu-id="d3e22-114">In the **Review text max length** field, enter the maximum number of characters that review text can have (for example, **1000**).</span></span> 
1. <span data-ttu-id="d3e22-115">Do pole **Maximální délka názvu recenze** zadejte maximální počet znaků názvu recenze (například **55**).</span><span class="sxs-lookup"><span data-stu-id="d3e22-115">In the **Review title max length** field, enter the maximum number of characters that review titles can have (for example, **55**).</span></span> 
1. <span data-ttu-id="d3e22-116">Vyberte možnost **Uložit a publikovat**.</span><span class="sxs-lookup"><span data-stu-id="d3e22-116">Select **Save and Publish**.</span></span> 

<span data-ttu-id="d3e22-117">Následující obrázek znázorňuje, jak vypadá tato konfigurace v řešení Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d3e22-117">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Konfigurace webu pro zobrazení hodnocení a recenzí](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a><span data-ttu-id="d3e22-119">Propojení hodnocení produktu se sekcí Recenze na stránce s podrobnostmi o produktu</span><span class="sxs-lookup"><span data-stu-id="d3e22-119">Link a product rating to the Reviews section of a PDP</span></span>

<span data-ttu-id="d3e22-120">Hodnocení produktu je uvedeno pod názvem produktu nahoře na stránce s podrobnostmi o produktu.</span><span class="sxs-lookup"><span data-stu-id="d3e22-120">A product rating is shown below the product title at the top of PDP.</span></span> <span data-ttu-id="d3e22-121">Hodnocení produktu lze nakonfigurovat tak, aby bylo propojeno se sekcí **Recenze** na stejné stránce s podrobnostmi o produktu.</span><span class="sxs-lookup"><span data-stu-id="d3e22-121">The product rating can be configured so that it's linked to the **Reviews** section of the same PDP.</span></span> 

<span data-ttu-id="d3e22-122">Chcete-li propojit hodnocení produktu se sekcí **Recenze** na stránce s podrobnostmi o produktu, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="d3e22-122">To link a product rating to the **Reviews** section of the PDP, follow these steps.</span></span>

1. <span data-ttu-id="d3e22-123">Otevřete šablonu stránky s podrobnostmi o produktu.</span><span class="sxs-lookup"><span data-stu-id="d3e22-123">Open the PDP template.</span></span> 
1. <span data-ttu-id="d3e22-124">Přejít na **Nastavení modulu kontejneru buy boxu**.</span><span class="sxs-lookup"><span data-stu-id="d3e22-124">Go to **Buy box container module settings**.</span></span>
1. <span data-ttu-id="d3e22-125">V části **Buy box** vyberte **Hodnocení produktu** a poté zaškrtněte políčko **Propojit kliknutí s úplným modulem recenzí**.</span><span class="sxs-lookup"><span data-stu-id="d3e22-125">Under **Buy box**, select **Product ratings**, and then select the **Link the click to full reviews module** check box.</span></span>

<span data-ttu-id="d3e22-126">Následující obrázek znázorňuje, jak vypadá tato konfigurace v řešení Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d3e22-126">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Propojení hodnocení produktu se sekcí Recenze na stránce s podrobnostmi o produktu](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a><span data-ttu-id="d3e22-128">Konfigurace odkazu na stránku ochrany osobních údajů a zásad</span><span class="sxs-lookup"><span data-stu-id="d3e22-128">Configure the link for the privacy and policy page</span></span>

<span data-ttu-id="d3e22-129">Chcete-li konfigurovat odkaz na stránku ochrany osobních údajů a zásad, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="d3e22-129">To configure the link for the privacy and policy page, follow these steps.</span></span>

1. <span data-ttu-id="d3e22-130">Přejděte do umístění **Domů \> Weby**.</span><span class="sxs-lookup"><span data-stu-id="d3e22-130">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="d3e22-131">Vyberte název webu.</span><span class="sxs-lookup"><span data-stu-id="d3e22-131">Select the name of your site.</span></span> 
1. <span data-ttu-id="d3e22-132">Přejděte na **Nastavení webu \> Rozšíření**.</span><span class="sxs-lookup"><span data-stu-id="d3e22-132">Go to **Site settings \> Extensions**.</span></span>
1. <span data-ttu-id="d3e22-133">Na kartě **Trasy** v části **Ochrana osobních údajů a zásady RNR** vyberte možnost **Přidat odkaz**.</span><span class="sxs-lookup"><span data-stu-id="d3e22-133">On the **Routes** tab, under **RNR Privacy and Policy**, select **Add a link**.</span></span> <span data-ttu-id="d3e22-134">Je-li již zadán odkaz a chcete jej nahradit, vyberte odkaz.</span><span class="sxs-lookup"><span data-stu-id="d3e22-134">If a link is already entered, and you want to replace it, select the link.</span></span> 
1. <span data-ttu-id="d3e22-135">V dialogovém okně **Přidat odkaz** vyberte odkaz na stránku ochrany osobních údajů a zásad a poté klepněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="d3e22-135">In the **Add a link** dialog box, select the link for the privacy and policy page, and then select **OK**.</span></span> 
1. <span data-ttu-id="d3e22-136">Vyberte možnost **Uložit a publikovat**.</span><span class="sxs-lookup"><span data-stu-id="d3e22-136">Select **Save and Publish**.</span></span> 

<span data-ttu-id="d3e22-137">Následující obrázek znázorňuje, jak vypadá tato konfigurace v řešení Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d3e22-137">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Konfigurace odkazu na stránku ochrany osobních údajů a zásad](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="configure-ratings-and-reviews-modules-on-product-details-pages"></a><span data-ttu-id="d3e22-139">Konfigurovat moduly hodnocení a recenzí na stránkách s podrobnostmi o produktu</span><span class="sxs-lookup"><span data-stu-id="d3e22-139">Configure ratings and reviews modules on product details pages</span></span>

<span data-ttu-id="d3e22-140">Informace týkající se konfigurace hodnocení a recenzí na stránkách s podrobnostmi o produktu naleznete v tématu [Moduly hodnocení a recenzí](ratings-reviews-modules.md).</span><span class="sxs-lookup"><span data-stu-id="d3e22-140">For information on configuring ratings and reviews modules on product details pages, see [Ratings and reviews modules](ratings-reviews-modules.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d3e22-141">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="d3e22-141">Additional resources</span></span>

[<span data-ttu-id="d3e22-142">Přehled hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="d3e22-142">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="d3e22-143">Připojení k používání hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="d3e22-143">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="d3e22-144">Správa hodnocení a recenzí</span><span class="sxs-lookup"><span data-stu-id="d3e22-144">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="d3e22-145">Konfigurovat moduly hodnocení a recenzí na stránkách s podrobnostmi o produktu</span><span class="sxs-lookup"><span data-stu-id="d3e22-145">Configure ratings and reviews modules on product details pages</span></span>](ratings-reviews-modules.md)

[<span data-ttu-id="d3e22-146">Synchronizace hodnocení produktů v Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="d3e22-146">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
