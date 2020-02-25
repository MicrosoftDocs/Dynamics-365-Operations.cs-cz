---
title: Modul zápatí
description: Toto téma popisuje moduly zápatí a způsob jejich vytváření v řešení Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: f8e0290b5af9d0c1fc9ad0279b0d7f81c9feb2fc
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001126"
---
# <a name="footer-module"></a><span data-ttu-id="b5427-103">Modul zápatí</span><span class="sxs-lookup"><span data-stu-id="b5427-103">Footer module</span></span>  


[!include [banner](includes/banner.md)]

<span data-ttu-id="b5427-104">Toto téma popisuje moduly zápatí a popisuje, jak je vytvořit v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b5427-104">This topic covers footer modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b5427-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="b5427-105">Overview</span></span>

<span data-ttu-id="b5427-106">Modul zápatí je speciální kontejner, který se používá k hostování modulů, které se zobrazují v zápatí stránky.</span><span class="sxs-lookup"><span data-stu-id="b5427-106">The footer module is a special container that is used to host the modules that appear in the page footer.</span></span> <span data-ttu-id="b5427-107">Může se například jednat o odkazy na různé stránky na webu, například **O nás** a **Zásady obchodu**.</span><span class="sxs-lookup"><span data-stu-id="b5427-107">For example, it can include links to various pages across the site, such as **Contact Us** and **Store Policies** pages.</span></span>

## <a name="footer-module-properties"></a><span data-ttu-id="b5427-108">Vlastnosti modulu zápatí</span><span class="sxs-lookup"><span data-stu-id="b5427-108">Footer module properties</span></span> 

<span data-ttu-id="b5427-109">Podobně jako většina kontejnerů, modul zápatí podporuje vlastnosti pro nadpis a šířku.</span><span class="sxs-lookup"><span data-stu-id="b5427-109">Like most containers, a footer module support properties for the heading and the width.</span></span> <span data-ttu-id="b5427-110">Podporuje také přidání modulů kategorií s více zápatími.</span><span class="sxs-lookup"><span data-stu-id="b5427-110">It also supports the addition of multiple footer category modules.</span></span> <span data-ttu-id="b5427-111">Přidaný modul kategorie zápatí je vykreslen jako sloupec v modulu zápatí.</span><span class="sxs-lookup"><span data-stu-id="b5427-111">Each footer category module that is added is rendered as a column in the footer module.</span></span>

## <a name="modules-available-in-a-footer-module"></a><span data-ttu-id="b5427-112">Moduly dostupné v modulu zápatí</span><span class="sxs-lookup"><span data-stu-id="b5427-112">Modules available in a footer module</span></span>

<span data-ttu-id="b5427-113">**Položky zápatí** – Modul položek zápatí může obsahovat nadpis, obrázek a odkaz.</span><span class="sxs-lookup"><span data-stu-id="b5427-113">**Footer items** – A footer items module can contain a heading, an image, and a link.</span></span> <span data-ttu-id="b5427-114">Nadpis lze použít samostatně nebo v kombinaci s obrázkem a odkazem.</span><span class="sxs-lookup"><span data-stu-id="b5427-114">The heading can be used either alone or in combination with an image and a link.</span></span> <span data-ttu-id="b5427-115">Každý odkaz v zápatí lze nakonfigurovat tak, aby obsahoval pouze text (například odkazy „Kontaktujte nás“ a „Ochrana osobních údajů“), nebo aby měl text i obrázek (například odkazy na sociální média).</span><span class="sxs-lookup"><span data-stu-id="b5427-115">Every link in the footer can be configured so that it has just text (for example, "Contact Us" and "Privacy" links), or so that it has both text and an image (for example, social media links).</span></span>

<span data-ttu-id="b5427-116">**Zpět na začátek** – Modul Zpět na začátek obsahuje odkaz pro rychlou navigaci na začátek stránky.</span><span class="sxs-lookup"><span data-stu-id="b5427-116">**Back to top** – A back to top module provides a link for quick navigation to the top of the page.</span></span> <span data-ttu-id="b5427-117">Cíl je povinný.</span><span class="sxs-lookup"><span data-stu-id="b5427-117">A destination is required.</span></span> <span data-ttu-id="b5427-118">Výchozí hodnota cíle je #, která přesměruje uživatele na začátek stránky.</span><span class="sxs-lookup"><span data-stu-id="b5427-118">The default destination value is #, which takes the user to the top of the page.</span></span>

## <a name="author-a-footer-module"></a><span data-ttu-id="b5427-119">Vytvoření modulu zápatí</span><span class="sxs-lookup"><span data-stu-id="b5427-119">Author a footer module</span></span>

1. <span data-ttu-id="b5427-120">V navigačním podokně vyberte **Fragmenty** a pak vyberte možnost **Nový fragment stránky**.</span><span class="sxs-lookup"><span data-stu-id="b5427-120">In the navigation pane, select **Fragments**, and then select **New Page Fragment**.</span></span>
1. <span data-ttu-id="b5427-121">V dialogovém okně **Nový fragment stránky** vyberte modul zápatí, zadejte název fragmentu stránky a poté klepněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="b5427-121">In the **New Page Fragment** dialog box, select the footer module, enter a name for the page fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="b5427-122">Ve stromové struktuře vlevo vyberte pro modul zápatí tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="b5427-122">In the outline tree on the left, select the ellipsis button (**...**) for the footer module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="b5427-123">V dialogovém okně **Přidat modul** vyberte modul kategorie zápatí a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="b5427-123">In the **Add Module** dialog box, select the footer category module, and then select **OK**.</span></span>
1. <span data-ttu-id="b5427-124">Ve stromové struktuře vyberte pro modul kategorie zápatí tlačítko se třemi tečkami a vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="b5427-124">In the outline tree, select the ellipsis button for the footer category module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="b5427-125">V dialogovém okně **Přidat modul** vyberte modul položky zápatí a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="b5427-125">In the **Add Module** dialog box, select the footer item module, and then select **OK**.</span></span>
1. <span data-ttu-id="b5427-126">Ve stromové strukřutě vyberte modul položky zápatí.</span><span class="sxs-lookup"><span data-stu-id="b5427-126">In the outline tree, select the footer item module.</span></span> <span data-ttu-id="b5427-127">Poté v podokně vlastností napravo nakonfigurujte nadpis, odkaz a text odkazu a požadovaný obrázek.</span><span class="sxs-lookup"><span data-stu-id="b5427-127">Then, in the properties pane on the right, configure the heading, link and link text, and image as you require.</span></span>
1. <span data-ttu-id="b5427-128">Chcete-li přidat další položky zápatí, opakujte kroky 5 až 7.</span><span class="sxs-lookup"><span data-stu-id="b5427-128">To add more footer items, repeat steps 5 through 7.</span></span>
1. <span data-ttu-id="b5427-129">Chcete-li přidat do zápatí odkaz „zpět na začátek“, ve stromové struktuře vyberte pro modul kategorie zápatí tlačítko se třemi tečkami a vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="b5427-129">To add a "back to top" link to your footer, select the ellipsis button for the footer category module, and then select **Add Module**.</span></span>
1. <span data-ttu-id="b5427-130">V dialogovém okně **Přidat modul** vyberte modul Zpět na začátek a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="b5427-130">In the **Add Module** dialog box, select the back to top module, and then select **OK**.</span></span>
1. <span data-ttu-id="b5427-131">Ve stromové struktuře vyberte modul Zpět na začátek.</span><span class="sxs-lookup"><span data-stu-id="b5427-131">In the outline tree, select the back to top module.</span></span> <span data-ttu-id="b5427-132">Poté v podokně vlastností napravo nakonfigurujte modul Zpět na zaátek podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="b5427-132">Then, in the properties pane on the right, configure the back to top module as you require.</span></span>
1. <span data-ttu-id="b5427-133">Uložte fragment stránky, vraťte jej se změnami a publikujte.</span><span class="sxs-lookup"><span data-stu-id="b5427-133">Save the page fragment, check it in, and publish it.</span></span>

<span data-ttu-id="b5427-134">U každé šablony stránky, která byla pro web vytvořena, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="b5427-134">On every page template that has been created for the site, follow these steps.</span></span>

1. <span data-ttu-id="b5427-135">V pozici **Hlavní** na výchozí stránce přidejte do modulu zápatí fragment zápatí, který jste vytvořili.</span><span class="sxs-lookup"><span data-stu-id="b5427-135">In the **Main** slot of the default page, in the footer module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="b5427-136">Uložte šablonu, vraťte ji se změnami a publikujte.</span><span class="sxs-lookup"><span data-stu-id="b5427-136">Save the template, check it in, and publish it.</span></span>

<span data-ttu-id="b5427-137">Přidáním fragmentu stránky do šablon stránek pomůžete zaručit, že zápatí bude vykresleno na každé stránce.</span><span class="sxs-lookup"><span data-stu-id="b5427-137">By adding the page fragment to page templates, you help guarantee that the footer is rendered on every page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b5427-138">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="b5427-138">Additional resources</span></span>

[<span data-ttu-id="b5427-139">Přehled startovací sady</span><span class="sxs-lookup"><span data-stu-id="b5427-139">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="b5427-140">Modul kontejneru</span><span class="sxs-lookup"><span data-stu-id="b5427-140">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="b5427-141">Modul buy boxu</span><span class="sxs-lookup"><span data-stu-id="b5427-141">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="b5427-142">Modul košíku</span><span class="sxs-lookup"><span data-stu-id="b5427-142">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="b5427-143">Modul pokladny</span><span class="sxs-lookup"><span data-stu-id="b5427-143">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="b5427-144">Modul potvrzení objednávky</span><span class="sxs-lookup"><span data-stu-id="b5427-144">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="b5427-145">Modul záhlaví</span><span class="sxs-lookup"><span data-stu-id="b5427-145">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="b5427-146">Modul zápatí</span><span class="sxs-lookup"><span data-stu-id="b5427-146">Footer module</span></span>](author-footer-module.md)
