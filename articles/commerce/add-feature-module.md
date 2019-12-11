---
title: Propagační modul
description: Tohle téma se zabývá propagačními moduly a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 76b59681d0bda11446f6db8b2685d1a0656f8f55
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785276"
---
# <a name="feature-module"></a><span data-ttu-id="97c59-103">Propagační modul</span><span class="sxs-lookup"><span data-stu-id="97c59-103">Feature module</span></span> 

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="97c59-104">Tohle téma se zabývá propagačními moduly a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="97c59-104">This topic covers feature modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="97c59-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="97c59-105">Overview</span></span>

<span data-ttu-id="97c59-106">Propagační modul slouží k nabízení produktů a propagačních akcí prostřednictvím kombinace obrázků a textu.</span><span class="sxs-lookup"><span data-stu-id="97c59-106">A feature module is used to market products or promotions through a combination of images and text.</span></span> <span data-ttu-id="97c59-107">Maloobchodní prodejce může například přidat propagační modul na stránku podrobností o produktu, aby zdrůraznil charakteristiky produktu.</span><span class="sxs-lookup"><span data-stu-id="97c59-107">For example, a retailer can add a feature module to a product details page to highlight the features of the product.</span></span>

<span data-ttu-id="97c59-108">Propagační modul je řízen daty ze systému správy obsahu (CMS).</span><span class="sxs-lookup"><span data-stu-id="97c59-108">A feature module is driven by data from the content management system (CMS).</span></span> <span data-ttu-id="97c59-109">Jedná se o samostatný modul, který nezávisí na jiných modulech na stránce.</span><span class="sxs-lookup"><span data-stu-id="97c59-109">It's a stand-alone module that doesn't depend on any other modules on the page.</span></span> <span data-ttu-id="97c59-110">Propagační modul může být umístěn na libovolné stránce webu, kde chce maloprodejce něco nabízet nebo propagovat (například produkty, prodeje nebo funkce).</span><span class="sxs-lookup"><span data-stu-id="97c59-110">A feature module can be put on any site page where a retailer wants to market or promote something (for example products, sales, or features).</span></span>

## <a name="examples-of-feature-modules-in-e-commerce"></a><span data-ttu-id="97c59-111">Příklady propagačních modulů v elektronickém obchodování</span><span class="sxs-lookup"><span data-stu-id="97c59-111">Examples of feature modules in e-Commerce</span></span>

<span data-ttu-id="97c59-112">Propagační modul se může používat na následujících stránkách:</span><span class="sxs-lookup"><span data-stu-id="97c59-112">A feature module can used on the following pages:</span></span>

- <span data-ttu-id="97c59-113">K prezentaci charakteristik produktu na stránce s podrobnostmi o produktu</span><span class="sxs-lookup"><span data-stu-id="97c59-113">A product details page, to showcase product features</span></span>
- <span data-ttu-id="97c59-114">Domovská stránka k propagaci produktů</span><span class="sxs-lookup"><span data-stu-id="97c59-114">The home page, to promote products</span></span>
- <span data-ttu-id="97c59-115">Stránka kategorie, která umožňuje zvýraznit kategorii produktů</span><span class="sxs-lookup"><span data-stu-id="97c59-115">A category page, to highlight a category of products</span></span>

## <a name="feature-module-properties"></a><span data-ttu-id="97c59-116">Vlastnosti propagačního modulu</span><span class="sxs-lookup"><span data-stu-id="97c59-116">Feature module properties</span></span>

| <span data-ttu-id="97c59-117">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="97c59-117">Property name</span></span>     | <span data-ttu-id="97c59-118">Hodnoty</span><span class="sxs-lookup"><span data-stu-id="97c59-118">Values</span></span> | <span data-ttu-id="97c59-119">Popis</span><span class="sxs-lookup"><span data-stu-id="97c59-119">Description</span></span> |
|-------------------|--------|-------------|
| <span data-ttu-id="97c59-120">Obrázek</span><span class="sxs-lookup"><span data-stu-id="97c59-120">Image</span></span>             | <span data-ttu-id="97c59-121">Soubor obrázku</span><span class="sxs-lookup"><span data-stu-id="97c59-121">Image file</span></span> | <span data-ttu-id="97c59-122">Obrázek lze použít pro nabízení produktu nebo promoakce.</span><span class="sxs-lookup"><span data-stu-id="97c59-122">An image can be used to market the product or promotion.</span></span> <span data-ttu-id="97c59-123">Obrázek lze odeslat do galerie obrázků nebo lze použít existující obrázek.</span><span class="sxs-lookup"><span data-stu-id="97c59-123">An image can be uploaded to the image gallery, or an existing image can be used.</span></span> |
| <span data-ttu-id="97c59-124">Záhlaví</span><span class="sxs-lookup"><span data-stu-id="97c59-124">Heading</span></span>           | <span data-ttu-id="97c59-125">Text a značka nadpisu (**H1**, **H2**, **H3**, **H4**, **H5** nebo **H6**)</span><span class="sxs-lookup"><span data-stu-id="97c59-125">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="97c59-126">Každý propagační modul může mít nadpis.</span><span class="sxs-lookup"><span data-stu-id="97c59-126">Every feature module can have a heading.</span></span> <span data-ttu-id="97c59-127">Standardně se pro značku nadpisu používá označení **H2**.</span><span class="sxs-lookup"><span data-stu-id="97c59-127">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="97c59-128">Značku však lze změnit tak, aby vyhovovala požadavkům na usnadnění.</span><span class="sxs-lookup"><span data-stu-id="97c59-128">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="97c59-129">Odstavec</span><span class="sxs-lookup"><span data-stu-id="97c59-129">Paragraph</span></span>         | <span data-ttu-id="97c59-130">Text odstavce</span><span class="sxs-lookup"><span data-stu-id="97c59-130">Paragraph text</span></span> | <span data-ttu-id="97c59-131">Propagační moduly podporují text odstavce ve formátu RTF.</span><span class="sxs-lookup"><span data-stu-id="97c59-131">Feature modules support paragraph text in rich text format.</span></span> <span data-ttu-id="97c59-132">Jsou podporovány některé základní funkce pro formát RTF, například tučné a podtržené písmo, kurzíva a hypertextové odkazy.</span><span class="sxs-lookup"><span data-stu-id="97c59-132">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="97c59-133">Některé z těchto funkcí mohou být přepsány motivem stránky, který je použit pro daný modul.</span><span class="sxs-lookup"><span data-stu-id="97c59-133">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="97c59-134">Připojení</span><span class="sxs-lookup"><span data-stu-id="97c59-134">Link</span></span>              | <span data-ttu-id="97c59-135">Text odkazu, adresa URL odkazu, popisek ARIA (Accessible Rich Internet Applications) a **Otevřít odkaz na nové kartě**</span><span class="sxs-lookup"><span data-stu-id="97c59-135">Link text, link URL, Accessible Rich Internet Applications (ARIA) label, and **Open link in new tab**</span></span> | <span data-ttu-id="97c59-136">Propagační moduly podporují jeden nebo více odkazů pro volání akce.</span><span class="sxs-lookup"><span data-stu-id="97c59-136">Feature modules support one or more "call to action" links.</span></span> <span data-ttu-id="97c59-137">Je-li přidán odkaz, je nutné zadat text odkazu, adresu URL a popisek ARIA.</span><span class="sxs-lookup"><span data-stu-id="97c59-137">If a link is added, link text, a URL, and an ARIA label are required.</span></span> <span data-ttu-id="97c59-138">Popisky ARIA by měly být názorné, aby splňovaly požadavky na usnadnění.</span><span class="sxs-lookup"><span data-stu-id="97c59-138">ARIA labels should be descriptive to meet accessibility requirements.</span></span> <span data-ttu-id="97c59-139">Odkazy lze konfigurovat tak, aby byly otevřeny na nové kartě.</span><span class="sxs-lookup"><span data-stu-id="97c59-139">Links can be configured so that they are opened on a new tab.</span></span> |
| <span data-ttu-id="97c59-140">Umístění obrázku</span><span class="sxs-lookup"><span data-stu-id="97c59-140">Image placement</span></span>   | <span data-ttu-id="97c59-141">**Vpravo**, **vlevo**, **nahoře** nebo **dole**</span><span class="sxs-lookup"><span data-stu-id="97c59-141">**Right**, **Left**, **Top**, or **Bottom**</span></span> | <span data-ttu-id="97c59-142">Tato vlastnost definuje pozici obrázku vzhledem k danému textu.</span><span class="sxs-lookup"><span data-stu-id="97c59-142">This property defines the position of the image relative to the text.</span></span> <span data-ttu-id="97c59-143">Je-li například vybrána volba **Vpravo**, zobrazí se obrázek napravo od textu.</span><span class="sxs-lookup"><span data-stu-id="97c59-143">For example, if **Right** is selected, the image appears to the right of the text.</span></span> |
| <span data-ttu-id="97c59-144">Velikost sloupce pro obrázek</span><span class="sxs-lookup"><span data-stu-id="97c59-144">Image column size</span></span> | <span data-ttu-id="97c59-145">Hodnota od **1** do **12**</span><span class="sxs-lookup"><span data-stu-id="97c59-145">A value from **1** through **12**</span></span> | <span data-ttu-id="97c59-146">Tato vlastnost definuje velikost obrázku vzhledem k danému textu.</span><span class="sxs-lookup"><span data-stu-id="97c59-146">This property defines the size of the image relative to the text.</span></span> <span data-ttu-id="97c59-147">Velikost je vyjádřena jako počet sloupců na stránce.</span><span class="sxs-lookup"><span data-stu-id="97c59-147">Size is expressed as a number of columns on the page.</span></span> <span data-ttu-id="97c59-148">Na stránce je 12 sloupců.</span><span class="sxs-lookup"><span data-stu-id="97c59-148">There are 12 columns on a page.</span></span> <span data-ttu-id="97c59-149">Ve výchozím nastavení má obrázek a text stejnou velikost (šest sloupců).</span><span class="sxs-lookup"><span data-stu-id="97c59-149">By default, the image and text have equal size (six columns each).</span></span> <span data-ttu-id="97c59-150">Velikost však lze upravit podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="97c59-150">However, the size can be adjusted as required.</span></span> |

## <a name="add-a-feature-module-to-a-new-page"></a><span data-ttu-id="97c59-151">Přidání propagačního modulu na novou stránku</span><span class="sxs-lookup"><span data-stu-id="97c59-151">Add a feature module to a new page</span></span> 

<span data-ttu-id="97c59-152">Chcete-li přidat propagační modul na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="97c59-152">To add a feature module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="97c59-153">Přejděte na **Šablony** a vytvořte šablonu stránky s názvem **Propagační šablona**.</span><span class="sxs-lookup"><span data-stu-id="97c59-153">Go to **Templates**, and create a page template that is named **feature template**.</span></span>
1. <span data-ttu-id="97c59-154">V pozici **Hlavní** na výchozí stránce přidejte propagační modul.</span><span class="sxs-lookup"><span data-stu-id="97c59-154">In the **Main** slot of the default page, add a feature module.</span></span>
1. <span data-ttu-id="97c59-155">Vraťte šablonu se změnami a publikujte ji.</span><span class="sxs-lookup"><span data-stu-id="97c59-155">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="97c59-156">Propagační šablonu, kterou jste právě vytvořili, použijte pro vytvoření stránky s názvem **Propagační stránka**.</span><span class="sxs-lookup"><span data-stu-id="97c59-156">Use the feature template that you just created to create a page that is named **feature page**.</span></span>
1. <span data-ttu-id="97c59-157">V pozici **Hlavní** na výchozí stránce vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="97c59-157">In the **Main** slot of the default page, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="97c59-158">V dialogovém okně **Přidat modul** v části **Vyberte moduly** vyberte propagační modul a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="97c59-158">In the **Add Module** dialog box, under **Select Modules**, select a feature module, and then select **OK**.</span></span>
1. <span data-ttu-id="97c59-159">V levém stromu osnovy vyberte propagační modul.</span><span class="sxs-lookup"><span data-stu-id="97c59-159">In the outline tree on the left, select the feature module.</span></span>
1. <span data-ttu-id="97c59-160">V podokně vlastností vpravo vyberte možnost **Přidat obrázek**.</span><span class="sxs-lookup"><span data-stu-id="97c59-160">In the properties pane on the right, select **Add an image**.</span></span> <span data-ttu-id="97c59-161">Poté buď vyberte existující obrázek, nebo odešlete nový obrázek.</span><span class="sxs-lookup"><span data-stu-id="97c59-161">Then either select an existing image or upload a new image.</span></span>
1. <span data-ttu-id="97c59-162">Vyberte **Nadpis**.</span><span class="sxs-lookup"><span data-stu-id="97c59-162">Select **Heading**.</span></span>
1. <span data-ttu-id="97c59-163">V dialogovém okně **Nadpis** přidejte text nadpisu, vyberte úroveň nadpisu a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="97c59-163">In the **Heading** dialog box, add the heading text, select the heading level, and then select **OK**.</span></span>
1. <span data-ttu-id="97c59-164">V části **Formátovanýtext** přidejte text podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="97c59-164">Under **Rich Text**, add text as you require.</span></span>
1. <span data-ttu-id="97c59-165">Vyberte možnost **Přidat odkazakce**.</span><span class="sxs-lookup"><span data-stu-id="97c59-165">Select **Add Action Link**.</span></span>
1. <span data-ttu-id="97c59-166">V dialogovém okně **Odkaz na akci** přidejte text odkazu, adresu URL odkazu a popisek ARIA pro daný odkaz a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="97c59-166">In the **Action Link** dialog box, add link text, a link URL, and an ARIA label for the link, and then select **OK**.</span></span>
1. <span data-ttu-id="97c59-167">Uložte stránku a zobrazte náhled změn.</span><span class="sxs-lookup"><span data-stu-id="97c59-167">Save the page, and preview your changes.</span></span>
1. <span data-ttu-id="97c59-168">Vraťte stránku se změnami a publikujte ji.</span><span class="sxs-lookup"><span data-stu-id="97c59-168">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="97c59-169">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="97c59-169">Additional resources</span></span>

[<span data-ttu-id="97c59-170">Přehled startovací sady</span><span class="sxs-lookup"><span data-stu-id="97c59-170">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="97c59-171">Modul výstrahy</span><span class="sxs-lookup"><span data-stu-id="97c59-171">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="97c59-172">Karuselový modul</span><span class="sxs-lookup"><span data-stu-id="97c59-172">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="97c59-173">Modul bloku s formátovaným obsahem</span><span class="sxs-lookup"><span data-stu-id="97c59-173">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="97c59-174">Modul umístění obsahu</span><span class="sxs-lookup"><span data-stu-id="97c59-174">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="97c59-175">Modul hlavního banneru</span><span class="sxs-lookup"><span data-stu-id="97c59-175">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="97c59-176">Modul přehrávače videa</span><span class="sxs-lookup"><span data-stu-id="97c59-176">Video player module</span></span>](add-video-player.md)
