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
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c6527ad00e74fa105f3873036eb56557b98b05aa
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817371"
---
# <a name="text-block-module"></a><span data-ttu-id="571df-103">Modul textového bloku</span><span class="sxs-lookup"><span data-stu-id="571df-103">Text block module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="571df-104">Tohle téma se zabývá moduly textového bloku a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="571df-104">This topic covers text block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="571df-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="571df-105">Overview</span></span>

<span data-ttu-id="571df-106">Modul textového bloku je modul, který se používá k přidání textového obsahu.</span><span class="sxs-lookup"><span data-stu-id="571df-106">A text block module is a module that is used to add textual content.</span></span> <span data-ttu-id="571df-107">Tento obsah může být informativní nebo propagační.</span><span class="sxs-lookup"><span data-stu-id="571df-107">This content can be informational or promotional.</span></span>

<span data-ttu-id="571df-108">Moduly textového bloku jsou řízeny daty ze systému správy obsahu (CMS) a lze je umístit na libovolnou stránku.</span><span class="sxs-lookup"><span data-stu-id="571df-108">Text block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="571df-109">Jedná se o samostatné moduly, které nezávisejí na kontextu stránky ani na jiných modulech.</span><span class="sxs-lookup"><span data-stu-id="571df-109">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-text-block-modules-in-e-commerce"></a><span data-ttu-id="571df-110">Příklady modulů textového bloku v elektronickém obchodování</span><span class="sxs-lookup"><span data-stu-id="571df-110">Examples of text block modules in e-Commerce</span></span>

<span data-ttu-id="571df-111">Moduly tetových bloků lze používat následujícími způsoby:</span><span class="sxs-lookup"><span data-stu-id="571df-111">Text block modules can be used in the following ways:</span></span>

* <span data-ttu-id="571df-112">K prezentaci funkcí produktu na stránce s podrobnostmi o produktu.</span><span class="sxs-lookup"><span data-stu-id="571df-112">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="571df-113">Pro informativní potřeby na libovolné stránce.</span><span class="sxs-lookup"><span data-stu-id="571df-113">For informational purposes on any page.</span></span> <span data-ttu-id="571df-114">Mohou například vysvětlit výhody věrnostních programů, popsat zásady dodávek a vrácení, odpovídat na nejčastější dotazy nebo poskytovat obsah „o nás“.</span><span class="sxs-lookup"><span data-stu-id="571df-114">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="571df-115">Chcete-li přidat vlastní zprávy na stránce s podrobnostmi o produktu</span><span class="sxs-lookup"><span data-stu-id="571df-115">To add custom messages on a product details page.</span></span> <span data-ttu-id="571df-116">(například „Bezplatné poštovné u objednávek přes 1 000 Kč“).</span><span class="sxs-lookup"><span data-stu-id="571df-116">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="571df-117">K zobrazení informací o právních omezeních a kontaktech na stránce s podrobnostmi o produktu, stránce košíku, stránkách pokladny a dalších stránkách (například „Dodávky a refundace podléhají zásadám obchodu“).</span><span class="sxs-lookup"><span data-stu-id="571df-117">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

<span data-ttu-id="571df-118">Následující obrázek ukazuje příklad modulu textového bloku použitého na domovské stránce.</span><span class="sxs-lookup"><span data-stu-id="571df-118">The following image shows an example of a text block module that is used on a home page.</span></span>

![Příklad modulu textového bloku](./media/ecommerce-textblock.PNG)

## <a name="text-block-module-properties"></a><span data-ttu-id="571df-120">Vlasstnosti modulu textového bloku</span><span class="sxs-lookup"><span data-stu-id="571df-120">Text block module properties</span></span>

| <span data-ttu-id="571df-121">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="571df-121">Property name</span></span>     | <span data-ttu-id="571df-122">Hodnota</span><span class="sxs-lookup"><span data-stu-id="571df-122">Value</span></span>                                            | <span data-ttu-id="571df-123">popis</span><span class="sxs-lookup"><span data-stu-id="571df-123">Description</span></span> |
|-------------------|--------------------------------------------------|-------------|
| <span data-ttu-id="571df-124">Formátovaný text</span><span class="sxs-lookup"><span data-stu-id="571df-124">Rich text</span></span>         | <span data-ttu-id="571df-125">Formátovaný text</span><span class="sxs-lookup"><span data-stu-id="571df-125">Rich text</span></span>                                        | <span data-ttu-id="571df-126">Text odstavce.</span><span class="sxs-lookup"><span data-stu-id="571df-126">Paragraph text.</span></span> <span data-ttu-id="571df-127">Jsou podporovány některé základní funkce pro formát RTF, například tučné a podtržené písmo a kurzíva.</span><span class="sxs-lookup"><span data-stu-id="571df-127">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |
| <span data-ttu-id="571df-128">Vlastní název třídy</span><span class="sxs-lookup"><span data-stu-id="571df-128">Custom class name</span></span> | <span data-ttu-id="571df-129">Název třídy Cascading Style Sheets (CSS)</span><span class="sxs-lookup"><span data-stu-id="571df-129">A Cascading Style Sheets (CSS) class name</span></span>        | <span data-ttu-id="571df-130">Název vlastní CSS třídy, kterou vývojář poskytuje k formátování tohoto modulu.</span><span class="sxs-lookup"><span data-stu-id="571df-130">The name of a custom CSS class that a developer provides to format this module.</span></span> <span data-ttu-id="571df-131">Název třídy by měl být definován v balíku motivů.</span><span class="sxs-lookup"><span data-stu-id="571df-131">The class name should be defined in the theme pack.</span></span> |
| <span data-ttu-id="571df-132">Velikost písma</span><span class="sxs-lookup"><span data-stu-id="571df-132">Font size</span></span>         | <span data-ttu-id="571df-133">**Malá**, **Střední**, **Velká** nebo **Extra velká**</span><span class="sxs-lookup"><span data-stu-id="571df-133">**Small**, **Medium**, **Large**, or **X-Large**</span></span> | <span data-ttu-id="571df-134">Velikost písma obsahu.</span><span class="sxs-lookup"><span data-stu-id="571df-134">The font size of the content.</span></span> |

## <a name="add-a-text-block-module-to-a-page"></a><span data-ttu-id="571df-135">Přidání modulu textového bloku na stránku</span><span class="sxs-lookup"><span data-stu-id="571df-135">Add a text block module to a page</span></span>

<span data-ttu-id="571df-136">Chcete-li přidat modul textového bloku na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="571df-136">To add a text block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="571df-137">Přejděte na **Šablony** a poté volbou **Nová** vytvořte novou šablonu.</span><span class="sxs-lookup"><span data-stu-id="571df-137">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="571df-138">V dialogovém okně **Nová šablona** v části **Název šablony** zadejte **Šablona obsahu**.</span><span class="sxs-lookup"><span data-stu-id="571df-138">In the **New Template** dialog box, under **Template name**, enter **Content template**.</span></span>
1. <span data-ttu-id="571df-139">V pozici **Tělo** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="571df-139">In the **Body** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="571df-140">V dialogovém okně **Přidat modul** vyberte modul **Výchozí stránka** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="571df-140">In the **Add Module** dialog box, select the **Default page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="571df-141">Chcete-li vrátit šablonu se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="571df-141">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="571df-142">Přejděte na **Stránky** a volbou **Nová** vytvořte novou stránku.</span><span class="sxs-lookup"><span data-stu-id="571df-142">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="571df-143">V dialogovém okně **Zvolte šablonu** vyberte šablonu **Šablona obsahu**.</span><span class="sxs-lookup"><span data-stu-id="571df-143">In the **Choose a template** dialog box, select **Content template**.</span></span> <span data-ttu-id="571df-144">V části **Název stránky** zadejte **Stránka obsahu** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="571df-144">Under **Page name**, enter **Content page**, and then select **OK**.</span></span>
1. <span data-ttu-id="571df-145">V pozici **Hlavní** na nové stránce vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="571df-145">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="571df-146">V dialogovém okně **Přidat modul** vyberte modul **Kontejner** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="571df-146">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="571df-147">V podokně vlastností modulu kontejner nastavte vlastnost **Šířka** na **Vyplnit kontejner**.</span><span class="sxs-lookup"><span data-stu-id="571df-147">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="571df-148">V pozici **Kontejner** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="571df-148">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="571df-149">V dialogovém okně **Přidat modul** vyberte modul **Textový blok** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="571df-149">In the **Add Module** dialog box, select the **Text block** module, and then select **OK**.</span></span> 
1. <span data-ttu-id="571df-150">V podokně vlastností modulu textového bloku přidejte text do pole **RTF**.</span><span class="sxs-lookup"><span data-stu-id="571df-150">In the property pane of the text block module, add text to the **Rich text** field.</span></span>
1. <span data-ttu-id="571df-151">Vyberte možnost **Uložit** a poté vyberte možnost **Náhled**, chcete-li zobrazit náhled stránky.</span><span class="sxs-lookup"><span data-stu-id="571df-151">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="571df-152">Chcete-li vrátit stránku se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="571df-152">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="571df-153">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="571df-153">Additional resources</span></span>

[<span data-ttu-id="571df-154">Přehled knihovny modulů</span><span class="sxs-lookup"><span data-stu-id="571df-154">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="571df-155">Modul propagačního banneru</span><span class="sxs-lookup"><span data-stu-id="571df-155">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="571df-156">Karuselový modul</span><span class="sxs-lookup"><span data-stu-id="571df-156">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="571df-157">Modul bloku obsahu</span><span class="sxs-lookup"><span data-stu-id="571df-157">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="571df-158">Modul videopřehrávače</span><span class="sxs-lookup"><span data-stu-id="571df-158">Video player module</span></span>](add-video-player.md)

