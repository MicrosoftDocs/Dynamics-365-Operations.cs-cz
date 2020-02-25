---
title: Modul bloku obsahu
description: Tohle téma se zabývá moduly bloků s obsahem a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: f91de93ce5ed4813f9f2adbe7678229189b5af2f
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025751"
---
# <a name="content-block-module"></a><span data-ttu-id="35ad4-103">Modul bloku obsahu</span><span class="sxs-lookup"><span data-stu-id="35ad4-103">Content block module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="35ad4-104">Tohle téma se zabývá moduly bloků s obsahem a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="35ad4-104">This topic covers content block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="35ad4-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="35ad4-105">Overview</span></span>

<span data-ttu-id="35ad4-106">Modul bloku obsahu slouží k nabízení produktů a propagačních akcí prostřednictvím kombinace obrázků a textu.</span><span class="sxs-lookup"><span data-stu-id="35ad4-106">A content block module is used to market products or promotions through a combination of images and text.</span></span> <span data-ttu-id="35ad4-107">Maloobchodní prodejce může například přidat modul bloku obsahu na domovskou stránku webu elektronického obchodu a propagovat tak nový produkt a upoutat pozornost zákazníků.</span><span class="sxs-lookup"><span data-stu-id="35ad4-107">For example, a retailer can add a content block module to the home page of an e-Commerce site to promote a new product and attract the attention of customers.</span></span>

<span data-ttu-id="35ad4-108">Modul bloku obsahu je řízen daty ze systému správy obsahu (CMS).</span><span class="sxs-lookup"><span data-stu-id="35ad4-108">A content block module is driven by data from the content management system (CMS).</span></span> <span data-ttu-id="35ad4-109">Jedná se o samostatný modul, který nezávisí na jiných modulech na stránce.</span><span class="sxs-lookup"><span data-stu-id="35ad4-109">It's a stand-alone module that doesn't depend on any other modules on the page.</span></span> <span data-ttu-id="35ad4-110">Modul bloku obsahu může být umístěn na libovolné stránce webu, kde chce maloprodejce něco nabízet nebo propagovat (například produkty, prodeje nebo funkce).</span><span class="sxs-lookup"><span data-stu-id="35ad4-110">A content block module can be put on any site page where a retailer wants to market or promote something (for example, products, sales, or features).</span></span>

## <a name="examples-of-content-block-module-in-e-commerce"></a><span data-ttu-id="35ad4-111">Příklady modulů bloků obsahu v elektronickém obchodování</span><span class="sxs-lookup"><span data-stu-id="35ad4-111">Examples of content block module in e-Commerce</span></span>

- <span data-ttu-id="35ad4-112">Modul bloku obsahu lze použít na domovské stránce webu elektronického obchodu a zvýraznit promoakce a nové produkty.</span><span class="sxs-lookup"><span data-stu-id="35ad4-112">A content block module can be used on the home page of an e-Commerce site to highlight promotions and new products.</span></span>
- <span data-ttu-id="35ad4-113">Chcete-li prezentovat informace o produktu, můžete na stránce s podrobnostmi o produktu použít modul bloku obsahu.</span><span class="sxs-lookup"><span data-stu-id="35ad4-113">A content block module can be used on a product details page to showcase product information.</span></span>
- <span data-ttu-id="35ad4-114">Do karuselového modulu lze vložit více modulů bloku obsahu pro zvýraznění více produktů nebo propagačních akcí.</span><span class="sxs-lookup"><span data-stu-id="35ad4-114">Multiple content block modules can be put inside a carousel module to highlight multiple products or promotions.</span></span>

## <a name="content-block-modules-and-themes"></a><span data-ttu-id="35ad4-115">Moduly bloku obsahu a motivy</span><span class="sxs-lookup"><span data-stu-id="35ad4-115">Content block modules and themes</span></span>

<span data-ttu-id="35ad4-116">Moduly bloku obsahu mohou podporovat různá rozložení a styly založené na motivu.</span><span class="sxs-lookup"><span data-stu-id="35ad4-116">Content block modules can support various layouts and styles based on a theme.</span></span> <span data-ttu-id="35ad4-117">Motiv Fabrikam například podporuje tři varianty rozvržení modulu bloku obsahu: hero, funkce a dlaždice.</span><span class="sxs-lookup"><span data-stu-id="35ad4-117">For example, the Fabrikam theme supports three layout variations of a content block module: hero, feature, and tile.</span></span> <span data-ttu-id="35ad4-118">V rozvržení hero se zobrazuje obrázek na pozadí s překrytím textu.</span><span class="sxs-lookup"><span data-stu-id="35ad4-118">The hero layout shows an image on the background with text overlay.</span></span> <span data-ttu-id="35ad4-119">Rozvržení funkce zobrazuje obrázek a text vedle sebe.</span><span class="sxs-lookup"><span data-stu-id="35ad4-119">The feature layout shows an image and text side by side.</span></span> <span data-ttu-id="35ad4-120">Rozložení dlaždic umožňuje více bloků obsahu ve formátu dlaždic.</span><span class="sxs-lookup"><span data-stu-id="35ad4-120">The tile layout allows multiple content blocks in a tile format.</span></span>

<span data-ttu-id="35ad4-121">Kromě toho může motiv vystavovat různé vlastnosti pro každé rozvržení.</span><span class="sxs-lookup"><span data-stu-id="35ad4-121">In addition, the theme can expose different properties for each layout.</span></span> <span data-ttu-id="35ad4-122">Vývojář motivů může vytvořit další rozložení s více styly pomocí modulu bloku obsahu.</span><span class="sxs-lookup"><span data-stu-id="35ad4-122">A theme developer can build more layouts with more styles using the content block module.</span></span>

<span data-ttu-id="35ad4-123">Na následujícím obrázku je znázorněn příklad modulu blok obsahu s rozvržením Hero.</span><span class="sxs-lookup"><span data-stu-id="35ad4-123">The following image shows an example of a content block module with a hero layout.</span></span>

![Příklad hlavního modulu](./media/Hero.PNG)

<span data-ttu-id="35ad4-125">Na následujícím obrázku je znázorněn příklad modulu blok obsahu s rozvržením funkce.</span><span class="sxs-lookup"><span data-stu-id="35ad4-125">The following image shows an example of a content block module with a feature layout.</span></span>

![Příklady propagačních modulů](./media/Feature.PNG)

## <a name="content-block-module-properties"></a><span data-ttu-id="35ad4-127">Vlastnosti modulu bloku obsahu</span><span class="sxs-lookup"><span data-stu-id="35ad4-127">Content block module properties</span></span>

| <span data-ttu-id="35ad4-128">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="35ad4-128">Property name</span></span>  | <span data-ttu-id="35ad4-129">Hodnoty</span><span class="sxs-lookup"><span data-stu-id="35ad4-129">Values</span></span> | <span data-ttu-id="35ad4-130">Popis</span><span class="sxs-lookup"><span data-stu-id="35ad4-130">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="35ad4-131">Obrázek</span><span class="sxs-lookup"><span data-stu-id="35ad4-131">Image</span></span>          | <span data-ttu-id="35ad4-132">Soubor obrázku</span><span class="sxs-lookup"><span data-stu-id="35ad4-132">Image file</span></span> | <span data-ttu-id="35ad4-133">Obrázek lze použít pro prezentaci produktu nebo promoakce.</span><span class="sxs-lookup"><span data-stu-id="35ad4-133">An image can be used to showcase a product or a promotion.</span></span> <span data-ttu-id="35ad4-134">Obrázek lze odeslat do galerie obrázků nebo lze použít existující obrázek.</span><span class="sxs-lookup"><span data-stu-id="35ad4-134">An image can be uploaded to the image gallery, or an existing image can be used.</span></span> |
| <span data-ttu-id="35ad4-135">Záhlaví</span><span class="sxs-lookup"><span data-stu-id="35ad4-135">Heading</span></span>        | <span data-ttu-id="35ad4-136">Text a značka nadpisu (**H1**, **H2**, **H3**, **H4**, **H5** nebo **H6**)</span><span class="sxs-lookup"><span data-stu-id="35ad4-136">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="35ad4-137">Každý modul hlavního banneru může mít nadpis.</span><span class="sxs-lookup"><span data-stu-id="35ad4-137">Every hero module can have a heading.</span></span> <span data-ttu-id="35ad4-138">Standardně se pro značku nadpisu používá označení **H2**.</span><span class="sxs-lookup"><span data-stu-id="35ad4-138">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="35ad4-139">Značku však lze změnit tak, aby vyhovovala požadavkům na usnadnění.</span><span class="sxs-lookup"><span data-stu-id="35ad4-139">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="35ad4-140">Odstavec</span><span class="sxs-lookup"><span data-stu-id="35ad4-140">Paragraph</span></span>      | <span data-ttu-id="35ad4-141">Text odstavce</span><span class="sxs-lookup"><span data-stu-id="35ad4-141">Paragraph text</span></span> | <span data-ttu-id="35ad4-142">Moduly hlavního banneru podporují text odstavce ve formátu RTF.</span><span class="sxs-lookup"><span data-stu-id="35ad4-142">Hero modules support paragraph text in rich text format.</span></span> <span data-ttu-id="35ad4-143">Jsou podporovány některé základní funkce pro formát RTF, například tučné a podtržené písmo, kurzíva a hypertextové odkazy.</span><span class="sxs-lookup"><span data-stu-id="35ad4-143">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="35ad4-144">Některé z těchto funkcí mohou být přepsány motivem stránky, který je použit pro daný modul.</span><span class="sxs-lookup"><span data-stu-id="35ad4-144">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="35ad4-145">Připojení</span><span class="sxs-lookup"><span data-stu-id="35ad4-145">Link</span></span>           | <span data-ttu-id="35ad4-146">Text odkazu, adresa URL odkazu, popisek ARIA (Accessible Rich Internet Applications) a **Otevřít odkaz na nové kartě**</span><span class="sxs-lookup"><span data-stu-id="35ad4-146">Link text, link URL, Accessible Rich Internet Applications (ARIA) label, and **Open link in new tab**</span></span> | <span data-ttu-id="35ad4-147">Moduly hlavního banneru podporují jeden nebo více odkazů pro volání akce.</span><span class="sxs-lookup"><span data-stu-id="35ad4-147">Hero modules support one or more "call to action" links.</span></span> <span data-ttu-id="35ad4-148">Je-li přidán odkaz, je nutné zadat text odkazu, adresu URL a popisek ARIA.</span><span class="sxs-lookup"><span data-stu-id="35ad4-148">If a link is added, link text, a URL, and an ARIA label are required.</span></span> <span data-ttu-id="35ad4-149">Popisky ARIA by měly být názorné, aby splňovaly požadavky na usnadnění.</span><span class="sxs-lookup"><span data-stu-id="35ad4-149">ARIA labels should be descriptive to meet accessibility requirements.</span></span> <span data-ttu-id="35ad4-150">Odkazy lze konfigurovat tak, aby byly otevřeny na nové kartě.</span><span class="sxs-lookup"><span data-stu-id="35ad4-150">Links can be configured so that they are opened on a new tab.</span></span> |

## <a name="content-block-module-properties-exposed-by-the-fabrikam-theme"></a><span data-ttu-id="35ad4-151">Vlastnosti modulu bloku obsahu vystavené motivem Fabrikam</span><span class="sxs-lookup"><span data-stu-id="35ad4-151">Content block module properties exposed by the Fabrikam theme</span></span> 

| <span data-ttu-id="35ad4-152">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="35ad4-152">Property name</span></span>  | <span data-ttu-id="35ad4-153">Hodnoty</span><span class="sxs-lookup"><span data-stu-id="35ad4-153">Values</span></span> | <span data-ttu-id="35ad4-154">Popis</span><span class="sxs-lookup"><span data-stu-id="35ad4-154">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="35ad4-155">Umístění textu</span><span class="sxs-lookup"><span data-stu-id="35ad4-155">Text placement</span></span> | <span data-ttu-id="35ad4-156">**Vlevo**, **Vpravo**, **Střed**</span><span class="sxs-lookup"><span data-stu-id="35ad4-156">**Left**, **Right**, **Center**</span></span> | <span data-ttu-id="35ad4-157">Tato vlastnost definuje pozici textu na obrázku.</span><span class="sxs-lookup"><span data-stu-id="35ad4-157">This property defines the position of the text on the image.</span></span> <span data-ttu-id="35ad4-158">Vztahuje se pouze na rozvržení Hero.</span><span class="sxs-lookup"><span data-stu-id="35ad4-158">It only applies to the hero layout.</span></span> |
| <span data-ttu-id="35ad4-159">Motiv textu</span><span class="sxs-lookup"><span data-stu-id="35ad4-159">Text theme</span></span>     | <span data-ttu-id="35ad4-160">**Světlý** nebo **Tmavý**</span><span class="sxs-lookup"><span data-stu-id="35ad4-160">**Light** or **Dark**</span></span> | <span data-ttu-id="35ad4-161">Pro text lze definovat barevné schéma, které je založeno na obrázku pozadí.</span><span class="sxs-lookup"><span data-stu-id="35ad4-161">A color scheme can be defined for the text, based on the background image.</span></span> <span data-ttu-id="35ad4-162">Má-li například obrázek tmavé pozadí, je možné použít světlý motiv, aby byl text lépe viditelný a odpovídal poměrům kontrastu barev pro účely usnadnění.</span><span class="sxs-lookup"><span data-stu-id="35ad4-162">For example, if the image has a dark background, a light theme can be applied to make the text more visible and to meet color contrast ratios for accessibility purposes.</span></span> <span data-ttu-id="35ad4-163">Vztahuje se pouze na rozvržení Hero.</span><span class="sxs-lookup"><span data-stu-id="35ad4-163">It only applies to the hero layout.</span></span>|
| <span data-ttu-id="35ad4-164">Umístění obrázku</span><span class="sxs-lookup"><span data-stu-id="35ad4-164">Image placement</span></span>       | <span data-ttu-id="35ad4-165">**Vlevo**, **vpravo**</span><span class="sxs-lookup"><span data-stu-id="35ad4-165">**Left**,  **Right**</span></span> | <span data-ttu-id="35ad4-166">Tato vlastnost určuje, zda má být obrázek vlevo nebo vpravo od textu.</span><span class="sxs-lookup"><span data-stu-id="35ad4-166">This property specifies if the image should be to the left or right of the text.</span></span> <span data-ttu-id="35ad4-167">Vztahuje se pouze na rozvržení funkce.</span><span class="sxs-lookup"><span data-stu-id="35ad4-167">It only applies to the feature layout.</span></span>  |

## <a name="add-a-content-block-module-to-a-new-page"></a><span data-ttu-id="35ad4-168">Přidání modulu bloku obsahu na novou stránku</span><span class="sxs-lookup"><span data-stu-id="35ad4-168">Add a content block module to a new page</span></span>

<span data-ttu-id="35ad4-169">Chcete-li přidat modul hlavního banneru na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="35ad4-169">To add a hero module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="35ad4-170">Přejděte na **Šablony** a vytvořte šablonu stránky s názvem **šablona bloku obsahu**.</span><span class="sxs-lookup"><span data-stu-id="35ad4-170">Go to **Templates**, and create a page template that is named **content block template**.</span></span>
1. <span data-ttu-id="35ad4-171">V pozici **Hlavní** na výchozí stránce přidejte modul hlavního banneru.</span><span class="sxs-lookup"><span data-stu-id="35ad4-171">In the **Main** slot of the default page, add a hero module.</span></span>
1. <span data-ttu-id="35ad4-172">Vraťte šablonu se změnami a publikujte ji.</span><span class="sxs-lookup"><span data-stu-id="35ad4-172">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="35ad4-173">Šablonu hero, kterou jste právě vytvořili, použijte pro vytvoření stránky s názvem **Stránka bloku obsahu**.</span><span class="sxs-lookup"><span data-stu-id="35ad4-173">Use the hero template that you just created to create a page that is named **content block page**.</span></span>
1. <span data-ttu-id="35ad4-174">V pozici **Hlavní** na výchozí stránce vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="35ad4-174">In the **Main** slot of the default page, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="35ad4-175">V dialogovém okně **Přidat modul** v části **Vyberte moduly** vyberte modul hlavního banneru a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="35ad4-175">In the **Add Module** dialog box, under **Select Modules**, select the hero module, and then select **OK**.</span></span>
1. <span data-ttu-id="35ad4-176">V levém stromu osnovy vyberte modul bloku obsahu.</span><span class="sxs-lookup"><span data-stu-id="35ad4-176">In the outline tree on the left, select the content block module.</span></span>
1. <span data-ttu-id="35ad4-177">V podokně vlastností vpravo vyberte možnost **Přidat obrázek**.</span><span class="sxs-lookup"><span data-stu-id="35ad4-177">In the properties pane on the right, select **Add an image**.</span></span> <span data-ttu-id="35ad4-178">Poté buď vyberte existující obrázek, nebo odešlete nový obrázek.</span><span class="sxs-lookup"><span data-stu-id="35ad4-178">Then either select an existing image or upload a new image.</span></span>
1. <span data-ttu-id="35ad4-179">Vyberte **Nadpis**.</span><span class="sxs-lookup"><span data-stu-id="35ad4-179">Select **Heading**.</span></span>
1. <span data-ttu-id="35ad4-180">V dialogovém okně **Nadpis** přidejte text nadpisu, vyberte úroveň nadpisu a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="35ad4-180">In the **Heading** dialog box, add the heading text, select the heading level, and then select **OK**.</span></span>
1. <span data-ttu-id="35ad4-181">V části **Formátovanýtext** přidejte text podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="35ad4-181">Under **Rich Text**, add text as you require.</span></span>
1. <span data-ttu-id="35ad4-182">Vyberte **Přidat odkaz**.</span><span class="sxs-lookup"><span data-stu-id="35ad4-182">Select **Add Link**.</span></span>
1. <span data-ttu-id="35ad4-183">V dialogovém okně **Odkaz** přidejte text odkazu, adresu URL odkazu a popisek ARIA pro daný odkaz a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="35ad4-183">In the **Link** dialog box, add link text, a link URL, and an ARIA label for the link, and then select **OK**.</span></span>
1. <span data-ttu-id="35ad4-184">Vyberte rozvržení **Hero**.</span><span class="sxs-lookup"><span data-stu-id="35ad4-184">Select the **Hero** layout.</span></span>
1. <span data-ttu-id="35ad4-185">Uložte stránku a zobrazte náhled změn.</span><span class="sxs-lookup"><span data-stu-id="35ad4-185">Save the page, and preview your changes.</span></span>
1. <span data-ttu-id="35ad4-186">Vraťte stránku se změnami a publikujte ji.</span><span class="sxs-lookup"><span data-stu-id="35ad4-186">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="35ad4-187">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="35ad4-187">Additional resources</span></span>

[<span data-ttu-id="35ad4-188">Přehled startovací sady</span><span class="sxs-lookup"><span data-stu-id="35ad4-188">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="35ad4-189">Modul propagačního banneru</span><span class="sxs-lookup"><span data-stu-id="35ad4-189">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="35ad4-190">Karuselový modul</span><span class="sxs-lookup"><span data-stu-id="35ad4-190">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="35ad4-191">Modul textového bloku</span><span class="sxs-lookup"><span data-stu-id="35ad4-191">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="35ad4-192">Modul videopřehrávače</span><span class="sxs-lookup"><span data-stu-id="35ad4-192">Video player module</span></span>](add-video-player.md)
