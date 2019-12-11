---
title: Modul hlavního banneru
description: Tohle téma se zabývá moduly hlavního banneru a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: c43704992e9759e7207f1b1c9bc958449daa6d1d
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785377"
---
# <a name="hero-module"></a><span data-ttu-id="e05e7-103">Modul hlavního banneru</span><span class="sxs-lookup"><span data-stu-id="e05e7-103">Hero module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="e05e7-104">Tohle téma se zabývá moduly hlavního banneru a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e05e7-104">This topic covers hero modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="e05e7-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="e05e7-105">Overview</span></span>

<span data-ttu-id="e05e7-106">Modul hlavního banneru slouží k nabízení produktů a propagačních akcí prostřednictvím kombinace obrázků a textu.</span><span class="sxs-lookup"><span data-stu-id="e05e7-106">A hero module is used to market products or promotions through a combination of images and text.</span></span> <span data-ttu-id="e05e7-107">Maloobchodní prodejce může například přidat modul hlavního banneru na domovskou stránku webu elektronického obchodu a propagovat tak nový produkt a upoutat pozornost zákazníků.</span><span class="sxs-lookup"><span data-stu-id="e05e7-107">For example, a retailer can add a hero module to the home page of an e-Commerce site to promote a new product and attract the attention of customers.</span></span>

<span data-ttu-id="e05e7-108">Modul hlavního banneru je řízen daty ze systému správy obsahu (CMS).</span><span class="sxs-lookup"><span data-stu-id="e05e7-108">A hero module is driven by data from the content management system (CMS).</span></span> <span data-ttu-id="e05e7-109">Jedná se o samostatný modul, který nezávisí na jiných modulech na stránce.</span><span class="sxs-lookup"><span data-stu-id="e05e7-109">It's a stand-alone module that doesn't depend on any other modules on the page.</span></span> <span data-ttu-id="e05e7-110">Modul hlavního banneru může být umístěn na libovolné stránce webu, kde chce maloprodejce něco nabízet nebo propagovat (například produkty, prodeje nebo funkce).</span><span class="sxs-lookup"><span data-stu-id="e05e7-110">A hero module can be put on any site page where a retailer wants to market or promote something (for example, products, sales, or features).</span></span>

## <a name="examples-of-hero-module-in-e-commerce"></a><span data-ttu-id="e05e7-111">Příklady modulů hlavního banneru v elektronickém obchodu</span><span class="sxs-lookup"><span data-stu-id="e05e7-111">Examples of hero module in e-Commerce</span></span>

- <span data-ttu-id="e05e7-112">Modul hlavního banneru lze použít na domovské stránce webu elektronického obchodu a zvýraznit promoakce a nové produkty.</span><span class="sxs-lookup"><span data-stu-id="e05e7-112">A hero module can be used on the home page of an e-Commerce site to highlight promotions and new products.</span></span>
- <span data-ttu-id="e05e7-113">Chcete-li prezentovat informace o produktu, můžete na stránce s podrobnostmi o produktu použít modul hlavního banneru.</span><span class="sxs-lookup"><span data-stu-id="e05e7-113">A hero module can be used on a product details page to showcase product information.</span></span>
- <span data-ttu-id="e05e7-114">Do karuselového modulu lze vložit více modulů hlavního banneru pro zvýraznění více produktů nebo propagačních akcí.</span><span class="sxs-lookup"><span data-stu-id="e05e7-114">Multiple hero modules can be put inside a carousel module to highlight multiple products or promotions.</span></span>

## <a name="hero-module-properties"></a><span data-ttu-id="e05e7-115">Vlastnosti modulu hlavního banneru</span><span class="sxs-lookup"><span data-stu-id="e05e7-115">Hero module properties</span></span>

| <span data-ttu-id="e05e7-116">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="e05e7-116">Property name</span></span>  | <span data-ttu-id="e05e7-117">Hodnoty</span><span class="sxs-lookup"><span data-stu-id="e05e7-117">Values</span></span> | <span data-ttu-id="e05e7-118">Popis</span><span class="sxs-lookup"><span data-stu-id="e05e7-118">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="e05e7-119">Obrázek</span><span class="sxs-lookup"><span data-stu-id="e05e7-119">Image</span></span>          | <span data-ttu-id="e05e7-120">Soubor obrázku</span><span class="sxs-lookup"><span data-stu-id="e05e7-120">Image file</span></span> | <span data-ttu-id="e05e7-121">Obrázek lze použít pro prezentaci produktu nebo promoakce.</span><span class="sxs-lookup"><span data-stu-id="e05e7-121">An image can be used to showcase a product or a promotion.</span></span> <span data-ttu-id="e05e7-122">Obrázek lze odeslat do galerie obrázků nebo lze použít existující obrázek.</span><span class="sxs-lookup"><span data-stu-id="e05e7-122">An image can be uploaded to the image gallery, or an existing image can be used.</span></span> |
| <span data-ttu-id="e05e7-123">Záhlaví</span><span class="sxs-lookup"><span data-stu-id="e05e7-123">Heading</span></span>        | <span data-ttu-id="e05e7-124">Text a značka nadpisu (**H1**, **H2**, **H3**, **H4**, **H5** nebo **H6**)</span><span class="sxs-lookup"><span data-stu-id="e05e7-124">Heading text and heading tag (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="e05e7-125">Každý modul hlavního banneru může mít nadpis.</span><span class="sxs-lookup"><span data-stu-id="e05e7-125">Every hero module can have a heading.</span></span> <span data-ttu-id="e05e7-126">Standardně se pro značku nadpisu používá označení **H2**.</span><span class="sxs-lookup"><span data-stu-id="e05e7-126">By default, the **H2** heading tag is used for the heading.</span></span> <span data-ttu-id="e05e7-127">Značku však lze změnit tak, aby vyhovovala požadavkům na usnadnění.</span><span class="sxs-lookup"><span data-stu-id="e05e7-127">However, the tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="e05e7-128">Odstavec</span><span class="sxs-lookup"><span data-stu-id="e05e7-128">Paragraph</span></span>      | <span data-ttu-id="e05e7-129">Text odstavce</span><span class="sxs-lookup"><span data-stu-id="e05e7-129">Paragraph text</span></span> | <span data-ttu-id="e05e7-130">Moduly hlavního banneru podporují text odstavce ve formátu RTF.</span><span class="sxs-lookup"><span data-stu-id="e05e7-130">Hero modules support paragraph text in rich text format.</span></span> <span data-ttu-id="e05e7-131">Jsou podporovány některé základní funkce pro formát RTF, například tučné a podtržené písmo, kurzíva a hypertextové odkazy.</span><span class="sxs-lookup"><span data-stu-id="e05e7-131">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="e05e7-132">Některé z těchto funkcí mohou být přepsány motivem stránky, který je použit pro daný modul.</span><span class="sxs-lookup"><span data-stu-id="e05e7-132">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="e05e7-133">Připojení</span><span class="sxs-lookup"><span data-stu-id="e05e7-133">Link</span></span>           | <span data-ttu-id="e05e7-134">Text odkazu, adresa URL odkazu, popisek ARIA (Accessible Rich Internet Applications) a **Otevřít odkaz na nové kartě**</span><span class="sxs-lookup"><span data-stu-id="e05e7-134">Link text, link URL, Accessible Rich Internet Applications (ARIA) label, and **Open link in new tab**</span></span> | <span data-ttu-id="e05e7-135">Moduly hlavního banneru podporují jeden nebo více odkazů pro volání akce.</span><span class="sxs-lookup"><span data-stu-id="e05e7-135">Hero modules support one or more "call to action" links.</span></span> <span data-ttu-id="e05e7-136">Je-li přidán odkaz, je nutné zadat text odkazu, adresu URL a popisek ARIA.</span><span class="sxs-lookup"><span data-stu-id="e05e7-136">If a link is added, link text, a URL, and an ARIA label are required.</span></span> <span data-ttu-id="e05e7-137">Popisky ARIA by měly být názorné, aby splňovaly požadavky na usnadnění.</span><span class="sxs-lookup"><span data-stu-id="e05e7-137">ARIA labels should be descriptive to meet accessibility requirements.</span></span> <span data-ttu-id="e05e7-138">Odkazy lze konfigurovat tak, aby byly otevřeny na nové kartě.</span><span class="sxs-lookup"><span data-stu-id="e05e7-138">Links can be configured so that they are opened on a new tab.</span></span> |
| <span data-ttu-id="e05e7-139">Umístění textu</span><span class="sxs-lookup"><span data-stu-id="e05e7-139">Text placement</span></span> | <span data-ttu-id="e05e7-140">**Vlevo nahoře**, **Vpravo nahoře**, **Uprostřed nahoře**, **Vlevo dole**, **Vpravo dole**, **Uprostřed dole**, **Uprostřed vlevo**, **Uprostřed vpravo** nebo **Uprostřed**</span><span class="sxs-lookup"><span data-stu-id="e05e7-140">**Top Left**, **Top Right**, **Top Center**, **Bottom Left**, **Bottom Right**, **Bottom Center**, **Center Left**, **Center Right**, or **Center Center**</span></span> | <span data-ttu-id="e05e7-141">Tato vlastnost definuje pozici obrázku vzhledem k danému textu.</span><span class="sxs-lookup"><span data-stu-id="e05e7-141">This property defines the position of the image relative to the text.</span></span> <span data-ttu-id="e05e7-142">Je-li například vybrána volba **Vpravo**, zobrazí se obrázek napravo od textu.</span><span class="sxs-lookup"><span data-stu-id="e05e7-142">For example, if **Right** is selected, the image appears to the right of the text.</span></span> |
| <span data-ttu-id="e05e7-143">Motiv textu</span><span class="sxs-lookup"><span data-stu-id="e05e7-143">Text theme</span></span>     | <span data-ttu-id="e05e7-144">**Světlý** nebo **Tmavý**</span><span class="sxs-lookup"><span data-stu-id="e05e7-144">**Light** or **Dark**</span></span> | <span data-ttu-id="e05e7-145">Pro text lze definovat barevné schéma, které je založeno na obrázku pozadí.</span><span class="sxs-lookup"><span data-stu-id="e05e7-145">A color scheme can be defined for the text, based on the background image.</span></span> <span data-ttu-id="e05e7-146">Má-li například obrázek tmavé pozadí, je možné použít světlý motiv, aby byl text lépe viditelný a odpovídal poměrům kontrastu barev pro účely usnadnění.</span><span class="sxs-lookup"><span data-stu-id="e05e7-146">For example, if the image has a dark background, a light theme can be applied to make the text more visible and to meet color contrast ratios for accessibility purposes.</span></span> |
| <span data-ttu-id="e05e7-147">Přechod</span><span class="sxs-lookup"><span data-stu-id="e05e7-147">Gradient</span></span>       | <span data-ttu-id="e05e7-148">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="e05e7-148">**True** or **False**</span></span> | <span data-ttu-id="e05e7-149">Přechod může být použit na obrázek, aby vyhověl poměrům kontrastu barev pro účely usnadnění.</span><span class="sxs-lookup"><span data-stu-id="e05e7-149">A gradient can be applied to the image to meet color contrast ratios for accessibility purposes.</span></span> |

## <a name="add-a-hero-module-to-a-new-page"></a><span data-ttu-id="e05e7-150">Přidání modulu hlavního banneru na novou stránku</span><span class="sxs-lookup"><span data-stu-id="e05e7-150">Add a hero module to a new page</span></span>

<span data-ttu-id="e05e7-151">Chcete-li přidat modul hlavního banneru na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="e05e7-151">To add a hero module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="e05e7-152">Přejděte na **Šablony** a vytvořte šablonu stránky s názvem **Šablona hlavního banneru**.</span><span class="sxs-lookup"><span data-stu-id="e05e7-152">Go to **Templates**, and create a page template that is named **hero template**.</span></span>
1. <span data-ttu-id="e05e7-153">V pozici **Hlavní** na výchozí stránce přidejte modul hlavního banneru.</span><span class="sxs-lookup"><span data-stu-id="e05e7-153">In the **Main** slot of the default page, add a hero module.</span></span>
1. <span data-ttu-id="e05e7-154">Vraťte šablonu se změnami a publikujte ji.</span><span class="sxs-lookup"><span data-stu-id="e05e7-154">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="e05e7-155">Šablonu hlavního banneru, kterou jste právě vytvořili, použijte pro vytvoření stránky s názvem **Stránka hlavního banneru**.</span><span class="sxs-lookup"><span data-stu-id="e05e7-155">Use the hero template that you just created to create a page that is named **hero page**.</span></span>
1. <span data-ttu-id="e05e7-156">V pozici **Hlavní** na výchozí stránce vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="e05e7-156">In the **Main** slot of the default page, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="e05e7-157">V dialogovém okně **Přidat modul** v části **Vyberte moduly** vyberte modul hlavního banneru a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="e05e7-157">In the **Add Module** dialog box, under **Select Modules**, select the hero module, and then select **OK**.</span></span>
1. <span data-ttu-id="e05e7-158">V levém stromu osnovy vyberte modul hlavního banneru.</span><span class="sxs-lookup"><span data-stu-id="e05e7-158">In the outline tree on the left, select the hero module.</span></span>
1. <span data-ttu-id="e05e7-159">V podokně vlastností vpravo vyberte možnost **Přidat obrázek**.</span><span class="sxs-lookup"><span data-stu-id="e05e7-159">In the properties pane on the right, select **Add an image**.</span></span> <span data-ttu-id="e05e7-160">Poté buď vyberte existující obrázek, nebo odešlete nový obrázek.</span><span class="sxs-lookup"><span data-stu-id="e05e7-160">Then either select an existing image or upload a new image.</span></span>
1. <span data-ttu-id="e05e7-161">Vyberte **Nadpis**.</span><span class="sxs-lookup"><span data-stu-id="e05e7-161">Select **Heading**.</span></span>
1. <span data-ttu-id="e05e7-162">V dialogovém okně **Nadpis** přidejte text nadpisu, vyberte úroveň nadpisu a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="e05e7-162">In the **Heading** dialog box, add the heading text, select the heading level, and then select **OK**.</span></span>
1. <span data-ttu-id="e05e7-163">V části **Formátovanýtext** přidejte text podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="e05e7-163">Under **Rich Text**, add text as you require.</span></span>
1. <span data-ttu-id="e05e7-164">Vyberte možnost **Přidat odkazakce**.</span><span class="sxs-lookup"><span data-stu-id="e05e7-164">Select **Add Action Link**.</span></span>
1. <span data-ttu-id="e05e7-165">V dialogovém okně **Odkaz na akci** přidejte text odkazu, adresu URL odkazu a popisek ARIA pro daný odkaz a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="e05e7-165">In the **Action Link** dialog box, add link text, a link URL, and an ARIA label for the link, and then select **OK**.</span></span>
1. <span data-ttu-id="e05e7-166">Uložte stránku a zobrazte náhled změn.</span><span class="sxs-lookup"><span data-stu-id="e05e7-166">Save the page, and preview your changes.</span></span>
1. <span data-ttu-id="e05e7-167">Vraťte stránku se změnami a publikujte ji.</span><span class="sxs-lookup"><span data-stu-id="e05e7-167">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e05e7-168">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="e05e7-168">Additional resources</span></span>

[<span data-ttu-id="e05e7-169">Přehled startovací sady</span><span class="sxs-lookup"><span data-stu-id="e05e7-169">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="e05e7-170">Modul výstrahy</span><span class="sxs-lookup"><span data-stu-id="e05e7-170">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="e05e7-171">Karuselový modul</span><span class="sxs-lookup"><span data-stu-id="e05e7-171">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="e05e7-172">Modul bloku s formátovaným obsahem</span><span class="sxs-lookup"><span data-stu-id="e05e7-172">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="e05e7-173">Modul umístění obsahu</span><span class="sxs-lookup"><span data-stu-id="e05e7-173">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="e05e7-174">Propagační modul</span><span class="sxs-lookup"><span data-stu-id="e05e7-174">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="e05e7-175">Modul přehrávače videa</span><span class="sxs-lookup"><span data-stu-id="e05e7-175">Video player module</span></span>](add-video-player.md)
