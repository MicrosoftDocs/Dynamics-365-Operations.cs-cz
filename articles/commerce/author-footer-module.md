---
title: Modul zápatí
description: Toto téma popisuje moduly zápatí a způsob jejich vytváření v řešení Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 42a71ea9498461febca80952acc3158517918332
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/16/2020
ms.locfileid: "3816954"
---
# <a name="footer-module"></a><span data-ttu-id="aadca-103">Modul zápatí</span><span class="sxs-lookup"><span data-stu-id="aadca-103">Footer module</span></span>  

[!include [banner](includes/banner.md)]

<span data-ttu-id="aadca-104">Toto téma popisuje moduly zápatí a popisuje, jak je vytvořit v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="aadca-104">This topic covers footer modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="aadca-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="aadca-105">Overview</span></span>

<span data-ttu-id="aadca-106">Modul zápatí je speciální kontejner, který se používá k hostování modulů, které se zobrazují v zápatí stránky.</span><span class="sxs-lookup"><span data-stu-id="aadca-106">The footer module is a special container that is used to host the modules that appear in the page footer.</span></span> <span data-ttu-id="aadca-107">Může se například jednat o odkazy na různé stránky na webu, například **O nás** a **Zásady obchodu**.</span><span class="sxs-lookup"><span data-stu-id="aadca-107">For example, it can include links to various pages across the site, such as **Contact Us** and **Store Policies** pages.</span></span>

<span data-ttu-id="aadca-108">Následující obrázek znázorňuje příklad modulu zápatí na stránce webu.</span><span class="sxs-lookup"><span data-stu-id="aadca-108">The following image shows an example of a footer module on a site page.</span></span>

![Příklad modulu zápatí](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties"></a><span data-ttu-id="aadca-110">Vlastnosti modulu zápatí</span><span class="sxs-lookup"><span data-stu-id="aadca-110">Footer module properties</span></span> 

<span data-ttu-id="aadca-111">Podobně jako většina kontejnerů, modul zápatí podporuje vlastnosti pro nadpis a šířku.</span><span class="sxs-lookup"><span data-stu-id="aadca-111">Like most containers, a footer module supports properties for the heading and the width.</span></span> <span data-ttu-id="aadca-112">Podporuje také přidání modulů kategorií s více zápatími.</span><span class="sxs-lookup"><span data-stu-id="aadca-112">It also supports the addition of multiple footer category modules.</span></span> <span data-ttu-id="aadca-113">Přidaný modul kategorie zápatí je vykreslen jako sloupec v modulu zápatí.</span><span class="sxs-lookup"><span data-stu-id="aadca-113">Each footer category module that is added is rendered as a column in the footer module.</span></span>

## <a name="modules-available-in-a-footer-module"></a><span data-ttu-id="aadca-114">Moduly dostupné v modulu zápatí</span><span class="sxs-lookup"><span data-stu-id="aadca-114">Modules available in a footer module</span></span>

<span data-ttu-id="aadca-115">**Položky zápatí** – Modul položek zápatí může obsahovat nadpis, obrázek a odkaz.</span><span class="sxs-lookup"><span data-stu-id="aadca-115">**Footer items** – A footer items module can contain a heading, an image, and a link.</span></span> <span data-ttu-id="aadca-116">Nadpis lze použít samostatně nebo v kombinaci s obrázkem a odkazem.</span><span class="sxs-lookup"><span data-stu-id="aadca-116">The heading can be used either alone or in combination with an image and a link.</span></span> <span data-ttu-id="aadca-117">Každý odkaz v zápatí lze nakonfigurovat tak, aby obsahoval pouze text (například odkazy „Kontaktujte nás“ a „Ochrana osobních údajů“), nebo aby měl text i obrázek (například odkazy na sociální média).</span><span class="sxs-lookup"><span data-stu-id="aadca-117">Every link in the footer can be configured so that it has just text (for example, "Contact Us" and "Privacy" links), or so that it has both text and an image (for example, social media links).</span></span>

<span data-ttu-id="aadca-118">**Zpět na začátek** – Modul Zpět na začátek obsahuje odkaz pro rychlou navigaci na začátek stránky.</span><span class="sxs-lookup"><span data-stu-id="aadca-118">**Back to top** – A back to top module provides a link for quick navigation to the top of the page.</span></span> <span data-ttu-id="aadca-119">Cíl je povinný.</span><span class="sxs-lookup"><span data-stu-id="aadca-119">A destination is required.</span></span> <span data-ttu-id="aadca-120">Výchozí hodnota cíle je \#, která přesměruje uživatele na začátek stránky.</span><span class="sxs-lookup"><span data-stu-id="aadca-120">The default destination value is \#, which takes the user to the top of the page.</span></span>

## <a name="create-a-footer-module"></a><span data-ttu-id="aadca-121">Vytvoření modulu zápatí</span><span class="sxs-lookup"><span data-stu-id="aadca-121">Create a footer module</span></span>

1. <span data-ttu-id="aadca-122">Přejděte na **Fragmenty** a volbou **Nový** vytvořte nový fragment.</span><span class="sxs-lookup"><span data-stu-id="aadca-122">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="aadca-123">V dialogovém okně **Nový fragment** vyberte modul **Kontejner**, zadejte název fragmentu a poté klepněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="aadca-123">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="aadca-124">V pozici **Výchozí kontejner** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="aadca-124">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="aadca-125">V dialogovém okně **Přidat modul** vyberte modul **Kategorie zápatí** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="aadca-125">In the **Add Module** dialog box, select the **Footer category** module, and then select **OK**.</span></span>
1. <span data-ttu-id="aadca-126">V pozici **Kategorie zápatí** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="aadca-126">In the **Footer category** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="aadca-127">V dialogovém okně **Přidat modul** vyberte modul **Položka zápatí** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="aadca-127">In the **Add Module** dialog box, select the **Footer item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="aadca-128">Vyberte pozici **Položka zápatí** a poté v podokně vlastností napravo dle potřeb nakonfigurujte nadpis, odkaz a text odkazu a obrázek.</span><span class="sxs-lookup"><span data-stu-id="aadca-128">Select the **Footer item** slot, and then, in the properties pane on the right, configure the heading, link and link text, and image as needed.</span></span>
1. <span data-ttu-id="aadca-129">Chcete-li přidat další položky zápatí, opakujte kroky 5 až 7.</span><span class="sxs-lookup"><span data-stu-id="aadca-129">To add more footer items, repeat steps 5 through 7 for each.</span></span>
1. <span data-ttu-id="aadca-130">Chcete-li přidat do zápatí odkaz „zpět na začátek“, v pozici **Kategorie zápatí** vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="aadca-130">To add a "back to top" link to your footer, select the ellipsis (**...**) in the **Footer category** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="aadca-131">V dialogovém okně **Přidat modul** vyberte modul **Zpět na začátek** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="aadca-131">In the **Add Module** dialog box, select the **Back to top** module, and then select **OK**.</span></span>
1. <span data-ttu-id="aadca-132">Vyberte pozici **Zpět na začátek** a poté v podokně vlastností napravo dle potřeb nakonfigurujte text a další vlastnosti modulu.</span><span class="sxs-lookup"><span data-stu-id="aadca-132">Select the **Back to top** slot, and then, in the properties pane on the right, configure the text and other module properties as needed.</span></span>
1. <span data-ttu-id="aadca-133">Chcete-li vrátit fragment se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="aadca-133">Select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="aadca-134">Chcete-li zajistit, aby se záhlaví zobrazilo na každé stránce, postupujte podle následujících kroků pro všechny šablony stránek, které jsou pro daný web vytvořeny.</span><span class="sxs-lookup"><span data-stu-id="aadca-134">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="aadca-135">V pozici **Zápatí** modulu **Výchozí stránka** přidejte fragment zápatí, který jste vytvořili.</span><span class="sxs-lookup"><span data-stu-id="aadca-135">In the **Footer** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="aadca-136">Chcete-li vrátit šablonu se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="aadca-136">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="aadca-137">Přidáním fragmentu do šablon stránek pomůžete zaručit, že zápatí bude vykresleno na každé stránce.</span><span class="sxs-lookup"><span data-stu-id="aadca-137">By adding the fragment to page templates, you help guarantee that the footer is rendered on every page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="aadca-138">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="aadca-138">Additional resources</span></span>

[<span data-ttu-id="aadca-139">Přehled knihovny modulů</span><span class="sxs-lookup"><span data-stu-id="aadca-139">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="aadca-140">Modul kontejneru</span><span class="sxs-lookup"><span data-stu-id="aadca-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="aadca-141">Modul buy boxu</span><span class="sxs-lookup"><span data-stu-id="aadca-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="aadca-142">Modul košíku</span><span class="sxs-lookup"><span data-stu-id="aadca-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="aadca-143">Modul pokladny</span><span class="sxs-lookup"><span data-stu-id="aadca-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="aadca-144">Modul potvrzení objednávky</span><span class="sxs-lookup"><span data-stu-id="aadca-144">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="aadca-145">Modul záhlaví</span><span class="sxs-lookup"><span data-stu-id="aadca-145">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="aadca-146">Modul zápatí</span><span class="sxs-lookup"><span data-stu-id="aadca-146">Footer module</span></span>](author-footer-module.md)
