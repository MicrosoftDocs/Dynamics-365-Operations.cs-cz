---
title: Modul zápatí
description: Toto téma popisuje moduly zápatí a způsob jejich vytváření v řešení Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 05/28/2020
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
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e81617979a945274500c9f4ceaa8078d8dfd79e8
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686711"
---
# <a name="footer-module"></a><span data-ttu-id="0d71c-103">Modul zápatí</span><span class="sxs-lookup"><span data-stu-id="0d71c-103">Footer module</span></span>  

[!include [banner](includes/banner.md)]

<span data-ttu-id="0d71c-104">Toto téma popisuje moduly zápatí a popisuje, jak je vytvořit v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0d71c-104">This topic covers footer modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0d71c-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="0d71c-105">Overview</span></span>

<span data-ttu-id="0d71c-106">Modul zápatí je speciální kontejner, který se používá k hostování modulů, které se zobrazují v zápatí stránky.</span><span class="sxs-lookup"><span data-stu-id="0d71c-106">The footer module is a special container that is used to host the modules that appear in the page footer.</span></span> <span data-ttu-id="0d71c-107">Může se například jednat o odkazy na různé stránky na webu, například **O nás** a **Zásady obchodu**.</span><span class="sxs-lookup"><span data-stu-id="0d71c-107">For example, it can include links to various pages across the site, such as **Contact Us** and **Store Policies** pages.</span></span>

<span data-ttu-id="0d71c-108">Následující obrázek znázorňuje příklad modulu zápatí na stránce webu.</span><span class="sxs-lookup"><span data-stu-id="0d71c-108">The following image shows an example of a footer module on a site page.</span></span>

![Příklad modulu zápatí](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties"></a><span data-ttu-id="0d71c-110">Vlastnosti modulu zápatí</span><span class="sxs-lookup"><span data-stu-id="0d71c-110">Footer module properties</span></span> 

<span data-ttu-id="0d71c-111">Podobně jako většina kontejnerů, modul zápatí podporuje vlastnosti pro nadpis a šířku.</span><span class="sxs-lookup"><span data-stu-id="0d71c-111">Like most containers, a footer module supports properties for the heading and the width.</span></span> <span data-ttu-id="0d71c-112">Podporuje také přidání modulů kategorií s více zápatími.</span><span class="sxs-lookup"><span data-stu-id="0d71c-112">It also supports the addition of multiple footer category modules.</span></span> <span data-ttu-id="0d71c-113">Přidaný modul kategorie zápatí je vykreslen jako sloupec v modulu zápatí.</span><span class="sxs-lookup"><span data-stu-id="0d71c-113">Each footer category module that is added is rendered as a column in the footer module.</span></span>

## <a name="modules-available-in-a-footer-module"></a><span data-ttu-id="0d71c-114">Moduly dostupné v modulu zápatí</span><span class="sxs-lookup"><span data-stu-id="0d71c-114">Modules available in a footer module</span></span>

<span data-ttu-id="0d71c-115">**Položky zápatí** – Modul položek zápatí může obsahovat nadpis, obrázek a odkaz.</span><span class="sxs-lookup"><span data-stu-id="0d71c-115">**Footer items** – A footer items module can contain a heading, an image, and a link.</span></span> <span data-ttu-id="0d71c-116">Nadpis lze použít samostatně nebo v kombinaci s obrázkem a odkazem.</span><span class="sxs-lookup"><span data-stu-id="0d71c-116">The heading can be used either alone or in combination with an image and a link.</span></span> <span data-ttu-id="0d71c-117">Každý odkaz v zápatí lze nakonfigurovat tak, aby obsahoval pouze text (například odkazy „Kontaktujte nás“ a „Ochrana osobních údajů“), nebo aby měl text i obrázek (například odkazy na sociální média).</span><span class="sxs-lookup"><span data-stu-id="0d71c-117">Every link in the footer can be configured so that it has just text (for example, "Contact Us" and "Privacy" links), or so that it has both text and an image (for example, social media links).</span></span>

<span data-ttu-id="0d71c-118">**Zpět na začátek** – Modul Zpět na začátek obsahuje odkaz pro rychlou navigaci na začátek stránky.</span><span class="sxs-lookup"><span data-stu-id="0d71c-118">**Back to top** – A back to top module provides a link for quick navigation to the top of the page.</span></span> <span data-ttu-id="0d71c-119">Cíl je povinný.</span><span class="sxs-lookup"><span data-stu-id="0d71c-119">A destination is required.</span></span> <span data-ttu-id="0d71c-120">Výchozí hodnota cíle je \#, která přesměruje uživatele na začátek stránky.</span><span class="sxs-lookup"><span data-stu-id="0d71c-120">The default destination value is \#, which takes the user to the top of the page.</span></span>

## <a name="create-a-footer-module"></a><span data-ttu-id="0d71c-121">Vytvoření modulu zápatí</span><span class="sxs-lookup"><span data-stu-id="0d71c-121">Create a footer module</span></span>

1. <span data-ttu-id="0d71c-122">Přejděte na **Fragmenty** a volbou **Nový** vytvořte nový fragment.</span><span class="sxs-lookup"><span data-stu-id="0d71c-122">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="0d71c-123">V dialogovém okně **Nový fragment stránky** vyberte modul **Kontejner**, zadejte název fragmentu stránky a poté klepněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="0d71c-123">In the **New page fragment** dialog box, select the **Container** module, enter a name for the page fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="0d71c-124">V pozici **Výchozí kontejner** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="0d71c-124">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0d71c-125">V dialogovém okně **Přidat modul** vyberte modul **Kategorie zápatí** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="0d71c-125">In the **Add Module** dialog box, select the **Footer category** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0d71c-126">V pozici **Kategorie zápatí** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="0d71c-126">In the **Footer category** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="0d71c-127">V dialogovém okně **Přidat modul** vyberte modul **Položka zápatí** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="0d71c-127">In the **Add Module** dialog box, select the **Footer item** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0d71c-128">Vyberte pozici **Položka zápatí** a poté v podokně vlastností napravo dle potřeb nakonfigurujte nadpis, odkaz a text odkazu a obrázek.</span><span class="sxs-lookup"><span data-stu-id="0d71c-128">Select the **Footer item** slot, and then, in the properties pane on the right, configure the heading, link and link text, and image as needed.</span></span>
1. <span data-ttu-id="0d71c-129">Chcete-li přidat další položky zápatí, opakujte kroky 5 až 7.</span><span class="sxs-lookup"><span data-stu-id="0d71c-129">To add more footer items, repeat steps 5 through 7 for each.</span></span>
1. <span data-ttu-id="0d71c-130">Chcete-li přidat do zápatí odkaz „zpět na začátek“, v pozici **Kategorie zápatí** vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="0d71c-130">To add a "back to top" link to your footer, select the ellipsis (**...**) in the **Footer category** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="0d71c-131">V dialogovém okně **Přidat modul** vyberte modul **Zpět na začátek** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="0d71c-131">In the **Add Module** dialog box, select the **Back to top** module, and then select **OK**.</span></span>
1. <span data-ttu-id="0d71c-132">Vyberte pozici **Zpět na začátek** a poté v podokně vlastností napravo dle potřeb nakonfigurujte text a další vlastnosti modulu.</span><span class="sxs-lookup"><span data-stu-id="0d71c-132">Select the **Back to top** slot, and then, in the properties pane on the right, configure the text and other module properties as needed.</span></span>
1. <span data-ttu-id="0d71c-133">Chcete-li vrátit fragment se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="0d71c-133">Select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="0d71c-134">Chcete-li zajistit, aby se záhlaví zobrazilo na každé stránce, postupujte podle následujících kroků pro všechny šablony stránek, které jsou pro daný web vytvořeny.</span><span class="sxs-lookup"><span data-stu-id="0d71c-134">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="0d71c-135">V pozici **Zápatí** modulu **Výchozí stránka** přidejte fragment zápatí, který jste vytvořili.</span><span class="sxs-lookup"><span data-stu-id="0d71c-135">In the **Footer** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="0d71c-136">Chcete-li vrátit šablonu se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="0d71c-136">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="0d71c-137">Přidáním fragmentu stránky do šablon stránek pomůžete zaručit, že zápatí bude vykresleno na každé stránce.</span><span class="sxs-lookup"><span data-stu-id="0d71c-137">By adding the page fragment to page templates, you help guarantee that the footer is rendered on every page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0d71c-138">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="0d71c-138">Additional resources</span></span>

[<span data-ttu-id="0d71c-139">Přehled startovací sady</span><span class="sxs-lookup"><span data-stu-id="0d71c-139">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="0d71c-140">Modul kontejneru</span><span class="sxs-lookup"><span data-stu-id="0d71c-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="0d71c-141">Modul buy boxu</span><span class="sxs-lookup"><span data-stu-id="0d71c-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="0d71c-142">Modul košíku</span><span class="sxs-lookup"><span data-stu-id="0d71c-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="0d71c-143">Modul pokladny</span><span class="sxs-lookup"><span data-stu-id="0d71c-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="0d71c-144">Modul potvrzení objednávky</span><span class="sxs-lookup"><span data-stu-id="0d71c-144">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="0d71c-145">Modul záhlaví</span><span class="sxs-lookup"><span data-stu-id="0d71c-145">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="0d71c-146">Modul zápatí</span><span class="sxs-lookup"><span data-stu-id="0d71c-146">Footer module</span></span>](author-footer-module.md)
