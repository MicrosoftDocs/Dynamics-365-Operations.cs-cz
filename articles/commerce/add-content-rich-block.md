---
title: Modul textového bloku
description: Tohle téma se zabývá moduly textového bloku a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3926f23e4e762a49ef94ef0c8f3291e7e9a4a6a2
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206384"
---
# <a name="text-block-module"></a><span data-ttu-id="72c1b-103">Modul textového bloku</span><span class="sxs-lookup"><span data-stu-id="72c1b-103">Text block module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="72c1b-104">Tohle téma se zabývá moduly textového bloku a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="72c1b-104">This topic covers text block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="72c1b-105">Modul textového bloku je modul, který se používá k přidání textového obsahu.</span><span class="sxs-lookup"><span data-stu-id="72c1b-105">A text block module is a module that is used to add textual content.</span></span> <span data-ttu-id="72c1b-106">Tento obsah může být informativní nebo propagační.</span><span class="sxs-lookup"><span data-stu-id="72c1b-106">This content can be informational or promotional.</span></span>

<span data-ttu-id="72c1b-107">Moduly textového bloku jsou řízeny daty ze systému správy obsahu (CMS) a lze je umístit na libovolnou stránku.</span><span class="sxs-lookup"><span data-stu-id="72c1b-107">Text block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="72c1b-108">Jedná se o samostatné moduly, které nezávisejí na kontextu stránky ani na jiných modulech.</span><span class="sxs-lookup"><span data-stu-id="72c1b-108">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-text-block-modules-in-e-commerce"></a><span data-ttu-id="72c1b-109">Příklady modulů textového bloku v elektronickém obchodování</span><span class="sxs-lookup"><span data-stu-id="72c1b-109">Examples of text block modules in e-Commerce</span></span>

<span data-ttu-id="72c1b-110">Moduly tetových bloků lze používat následujícími způsoby:</span><span class="sxs-lookup"><span data-stu-id="72c1b-110">Text block modules can be used in the following ways:</span></span>

* <span data-ttu-id="72c1b-111">K prezentaci funkcí produktu na stránce s podrobnostmi o produktu.</span><span class="sxs-lookup"><span data-stu-id="72c1b-111">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="72c1b-112">Pro informativní potřeby na libovolné stránce.</span><span class="sxs-lookup"><span data-stu-id="72c1b-112">For informational purposes on any page.</span></span> <span data-ttu-id="72c1b-113">Mohou například vysvětlit výhody věrnostních programů, popsat zásady dodávek a vrácení, odpovídat na nejčastější dotazy nebo poskytovat obsah „o nás“.</span><span class="sxs-lookup"><span data-stu-id="72c1b-113">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="72c1b-114">Chcete-li přidat vlastní zprávy na stránce s podrobnostmi o produktu</span><span class="sxs-lookup"><span data-stu-id="72c1b-114">To add custom messages on a product details page.</span></span> <span data-ttu-id="72c1b-115">(například „Bezplatné poštovné u objednávek přes 1 000 Kč“).</span><span class="sxs-lookup"><span data-stu-id="72c1b-115">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="72c1b-116">K zobrazení informací o právních omezeních a kontaktech na stránce s podrobnostmi o produktu, stránce košíku, stránkách pokladny a dalších stránkách (například „Dodávky a refundace podléhají zásadám obchodu“).</span><span class="sxs-lookup"><span data-stu-id="72c1b-116">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

<span data-ttu-id="72c1b-117">Následující obrázek ukazuje příklad modulu textového bloku použitého na domovské stránce.</span><span class="sxs-lookup"><span data-stu-id="72c1b-117">The following image shows an example of a text block module that is used on a home page.</span></span>

![Příklad modulu textového bloku](./media/ecommerce-textblock.PNG)

## <a name="text-block-module-properties"></a><span data-ttu-id="72c1b-119">Vlasstnosti modulu textového bloku</span><span class="sxs-lookup"><span data-stu-id="72c1b-119">Text block module properties</span></span>

| <span data-ttu-id="72c1b-120">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="72c1b-120">Property name</span></span>     | <span data-ttu-id="72c1b-121">Hodnota</span><span class="sxs-lookup"><span data-stu-id="72c1b-121">Value</span></span>                                            | <span data-ttu-id="72c1b-122">popis</span><span class="sxs-lookup"><span data-stu-id="72c1b-122">Description</span></span> |
|-------------------|--------------------------------------------------|-------------|
| <span data-ttu-id="72c1b-123">Formátovaný text</span><span class="sxs-lookup"><span data-stu-id="72c1b-123">Rich text</span></span>         | <span data-ttu-id="72c1b-124">Formátovaný text</span><span class="sxs-lookup"><span data-stu-id="72c1b-124">Rich text</span></span>                                        | <span data-ttu-id="72c1b-125">Text odstavce.</span><span class="sxs-lookup"><span data-stu-id="72c1b-125">Paragraph text.</span></span> <span data-ttu-id="72c1b-126">Jsou podporovány některé základní funkce pro formát RTF, například tučné a podtržené písmo a kurzíva.</span><span class="sxs-lookup"><span data-stu-id="72c1b-126">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |
| <span data-ttu-id="72c1b-127">Vlastní název třídy</span><span class="sxs-lookup"><span data-stu-id="72c1b-127">Custom class name</span></span> | <span data-ttu-id="72c1b-128">Název třídy Cascading Style Sheets (CSS)</span><span class="sxs-lookup"><span data-stu-id="72c1b-128">A Cascading Style Sheets (CSS) class name</span></span>        | <span data-ttu-id="72c1b-129">Název vlastní CSS třídy, kterou vývojář poskytuje k formátování tohoto modulu.</span><span class="sxs-lookup"><span data-stu-id="72c1b-129">The name of a custom CSS class that a developer provides to format this module.</span></span> <span data-ttu-id="72c1b-130">Název třídy by měl být definován v balíku motivů.</span><span class="sxs-lookup"><span data-stu-id="72c1b-130">The class name should be defined in the theme pack.</span></span> |
| <span data-ttu-id="72c1b-131">Velikost písma</span><span class="sxs-lookup"><span data-stu-id="72c1b-131">Font size</span></span>         | <span data-ttu-id="72c1b-132">**Malá**, **Střední**, **Velká** nebo **Extra velká**</span><span class="sxs-lookup"><span data-stu-id="72c1b-132">**Small**, **Medium**, **Large**, or **X-Large**</span></span> | <span data-ttu-id="72c1b-133">Velikost písma obsahu.</span><span class="sxs-lookup"><span data-stu-id="72c1b-133">The font size of the content.</span></span> |

## <a name="add-a-text-block-module-to-a-page"></a><span data-ttu-id="72c1b-134">Přidání modulu textového bloku na stránku</span><span class="sxs-lookup"><span data-stu-id="72c1b-134">Add a text block module to a page</span></span>

<span data-ttu-id="72c1b-135">Chcete-li přidat modul textového bloku na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="72c1b-135">To add a text block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="72c1b-136">Přejděte na **Šablony** a poté volbou **Nová** vytvořte novou šablonu.</span><span class="sxs-lookup"><span data-stu-id="72c1b-136">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="72c1b-137">V dialogovém okně **Nová šablona** v části **Název šablony** zadejte **Šablona obsahu**.</span><span class="sxs-lookup"><span data-stu-id="72c1b-137">In the **New Template** dialog box, under **Template name**, enter **Content template**.</span></span>
1. <span data-ttu-id="72c1b-138">V pozici **Tělo** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="72c1b-138">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="72c1b-139">V dialogovém okně **Přidat modul** vyberte modul **Výchozí stránka** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="72c1b-139">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="72c1b-140">Chcete-li vrátit šablonu se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="72c1b-140">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="72c1b-141">Přejděte na **Stránky** a volbou **Nová** vytvořte novou stránku.</span><span class="sxs-lookup"><span data-stu-id="72c1b-141">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="72c1b-142">V dialogovém okně **Zvolte šablonu** vyberte šablonu **Šablona obsahu**.</span><span class="sxs-lookup"><span data-stu-id="72c1b-142">In the **Choose a template** dialog box, select **Content template**.</span></span> <span data-ttu-id="72c1b-143">V části **Název stránky** zadejte **Stránka obsahu** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="72c1b-143">Under **Page name**, enter **Content page**, and then select **OK**.</span></span>
1. <span data-ttu-id="72c1b-144">V pozici **Hlavní** na nové stránce vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="72c1b-144">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="72c1b-145">V dialogovém okně **Přidat modul** vyberte modul **Kontejner** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="72c1b-145">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="72c1b-146">V podokně vlastností modulu kontejner nastavte vlastnost **Šířka** na **Vyplnit kontejner**.</span><span class="sxs-lookup"><span data-stu-id="72c1b-146">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="72c1b-147">V pozici **Kontejner** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="72c1b-147">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="72c1b-148">V dialogovém okně **Přidat modul** vyberte modul **Textový blok** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="72c1b-148">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span> 
1. <span data-ttu-id="72c1b-149">V podokně vlastností modulu textového bloku přidejte text do pole **RTF**.</span><span class="sxs-lookup"><span data-stu-id="72c1b-149">In the property pane of the text block module, add text to the **Rich text** field.</span></span>
1. <span data-ttu-id="72c1b-150">Vyberte možnost **Uložit** a poté vyberte možnost **Náhled**, chcete-li zobrazit náhled stránky.</span><span class="sxs-lookup"><span data-stu-id="72c1b-150">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="72c1b-151">Chcete-li vrátit stránku se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="72c1b-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="72c1b-152">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="72c1b-152">Additional resources</span></span>

[<span data-ttu-id="72c1b-153">Přehled knihovny modulů</span><span class="sxs-lookup"><span data-stu-id="72c1b-153">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="72c1b-154">Modul propagačního banneru</span><span class="sxs-lookup"><span data-stu-id="72c1b-154">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="72c1b-155">Karuselový modul</span><span class="sxs-lookup"><span data-stu-id="72c1b-155">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="72c1b-156">Modul bloku obsahu</span><span class="sxs-lookup"><span data-stu-id="72c1b-156">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="72c1b-157">Modul videopřehrávače</span><span class="sxs-lookup"><span data-stu-id="72c1b-157">Video player module</span></span>](add-video-player.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]