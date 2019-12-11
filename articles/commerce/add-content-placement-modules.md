---
title: Modul umístění obsahu
description: Tohle téma se zabývá modulem umístění obsahu a modulem položky umístění obsahu a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 1b64e930628c969334ff6e643ba23b77445e6e4c
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785293"
---
# <a name="content-placement-module"></a><span data-ttu-id="08331-103">Modul umístění obsahu</span><span class="sxs-lookup"><span data-stu-id="08331-103">Content placement module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="08331-104">Tohle téma se zabývá modulem umístění obsahu a modulem položky umístění obsahu a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="08331-104">This topic covers content placement and content placement item modules, and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="08331-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="08331-105">Overview</span></span>

<span data-ttu-id="08331-106">Modul umístění obsahu je speciální kontejner, do kterého lze umístit jiné moduly v určitém rozložení.</span><span class="sxs-lookup"><span data-stu-id="08331-106">A content placement module is a special container that other modules can be put inside in a specific layout.</span></span> <span data-ttu-id="08331-107">Moduly umístění obsahu podporují následující typy modulů jako podřízené moduly: položka umístění obsahu, položka přivítání v účtu, položka objednávky účtu, položka seznamu přání účtu a položka profilu účtu.</span><span class="sxs-lookup"><span data-stu-id="08331-107">Content placement modules support the following types of modules as child modules: content placement item, account welcome item, account order item, account wish list item, and account profile item.</span></span>

<span data-ttu-id="08331-108">Moduly umístění obsahu odvozují data z podřízených modulů, které podporují.</span><span class="sxs-lookup"><span data-stu-id="08331-108">Content placement modules derive data from the child modules that they support.</span></span> <span data-ttu-id="08331-109">Proto lze moduly umístění obsahu použít různými způsoby v závislosti na modulech, které jsou do něj přidány.</span><span class="sxs-lookup"><span data-stu-id="08331-109">Therefore, content placement modules can be used in various ways, depending on the modules that are added to it.</span></span>

<span data-ttu-id="08331-110">Moduly položek umístění obsahu používají obrázky i text k přezentaci promoakcí, zásad a funkcí produktu.</span><span class="sxs-lookup"><span data-stu-id="08331-110">Content placement item modules use both images and text to showcase promotions, policies, and product features.</span></span> <span data-ttu-id="08331-111">Například modul položky umístění obsahu lze použít na domovské stránce k zobrazení zásad obchodu nebo informací o dodávce.</span><span class="sxs-lookup"><span data-stu-id="08331-111">For example, a content placement item module can be used on a home page to show store policies or shipping information.</span></span> <span data-ttu-id="08331-112">Moduly položek umístění obsahu jsou řízeny daty ze systému správy obsahu (CMS) a lze je umístit na libovolnou stránku.</span><span class="sxs-lookup"><span data-stu-id="08331-112">Content placement item modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="08331-113">Lze je však použít pouze uvnitř modulu umístění obsahu.</span><span class="sxs-lookup"><span data-stu-id="08331-113">However, they can be used only inside a content placement module.</span></span>

## <a name="examples-of-content-placement-modules-in-e-commerce"></a><span data-ttu-id="08331-114">Příklady modulů umístění obsahu v elektronickém obchodování</span><span class="sxs-lookup"><span data-stu-id="08331-114">Examples of content placement modules in e-Commerce</span></span>

* <span data-ttu-id="08331-115">Moduly umístění obsahu, které obsahují moduly položek umístění obsahu, lze na domovské stránce nebo marketingových stránkách využít k prezentaci funkcí produktu, promoakcí, zásad obchodu, dodacích informací a dalších informací pomocí obrázků i textu.</span><span class="sxs-lookup"><span data-stu-id="08331-115">Content placement modules that contain content placement item modules can be used on a home page or marketing pages to showcase product features, promotions, store policies, shipping information, and other information through both images and text.</span></span>
* <span data-ttu-id="08331-116">Moduly umístění obsahu s informacemi o modulech položek umístění obsahu mohou být použity na stránkách s podrobnostmi o produktu a prezentovat funkce produktu.</span><span class="sxs-lookup"><span data-stu-id="08331-116">Content placement modules that contain content placement item modules can be used on product details pages to showcase product features.</span></span>
* <span data-ttu-id="08331-117">Moduly umístění obsahu, které obsahují modul položky přivítání v účtu nebo modul položky objednávky účtu, lze použít na stránkách správy účtů.</span><span class="sxs-lookup"><span data-stu-id="08331-117">Content placement modules that contain account welcome item or account order item modules can be used on account management pages.</span></span>

## <a name="content-placement-module-properties"></a><span data-ttu-id="08331-118">Vlastnosti modulu umístění obsahu</span><span class="sxs-lookup"><span data-stu-id="08331-118">Content placement module properties</span></span>

| <span data-ttu-id="08331-119">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="08331-119">Property name</span></span> | <span data-ttu-id="08331-120">Hodnota</span><span class="sxs-lookup"><span data-stu-id="08331-120">Value</span></span> | <span data-ttu-id="08331-121">Popis</span><span class="sxs-lookup"><span data-stu-id="08331-121">Description</span></span> |
|---------------|-------|-------------|
| <span data-ttu-id="08331-122">Šířka</span><span class="sxs-lookup"><span data-stu-id="08331-122">Width</span></span>         | <span data-ttu-id="08331-123">**Přizpůsobit kontejneru** nebo **Vyplnit obrazovku**</span><span class="sxs-lookup"><span data-stu-id="08331-123">**Fit container** or **Fill screen**</span></span> | <span data-ttu-id="08331-124">Je-li hodnota nastavena na **Přizpůsobit kontejneru**, budou položky uvnitř modulu umístění obsahu omezeny na jeho šířku.</span><span class="sxs-lookup"><span data-stu-id="08331-124">If the value is set to **Fit container**, the items inside the content placement module are restricted to the width of the content placement module.</span></span> <span data-ttu-id="08331-125">Je-li hodnota nastavena na **Vyplnit obrazovku**, položky nejsou omezeny na šířku modulu umístění obsahu, ale mohou přejít do režimu celé obrazovky.</span><span class="sxs-lookup"><span data-stu-id="08331-125">If the value is set to **Fill screen**, the items aren't restricted to the width of the content placement module but can go into full-screen mode.</span></span> |

## <a name="content-placement-item-module-properties"></a><span data-ttu-id="08331-126">Vlastnosti modulu položky umístění obsahu</span><span class="sxs-lookup"><span data-stu-id="08331-126">Content placement item module properties</span></span>

| <span data-ttu-id="08331-127">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="08331-127">Property name</span></span> | <span data-ttu-id="08331-128">Hodnota</span><span class="sxs-lookup"><span data-stu-id="08331-128">Value</span></span> | <span data-ttu-id="08331-129">Popis</span><span class="sxs-lookup"><span data-stu-id="08331-129">Description</span></span> |
|---------------|-------|-------------|
| <span data-ttu-id="08331-130">Záhlaví</span><span class="sxs-lookup"><span data-stu-id="08331-130">Heading</span></span>       | <span data-ttu-id="08331-131">Text a značky nadpisu (**H1**, **H2**, **H3**, **H4**, **H5** nebo **H6**)</span><span class="sxs-lookup"><span data-stu-id="08331-131">Heading text and heading tags (**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**)</span></span> | <span data-ttu-id="08331-132">Každý modul položky umístění obsahu může mít nadpis.</span><span class="sxs-lookup"><span data-stu-id="08331-132">Every content placement item module can have a heading.</span></span> <span data-ttu-id="08331-133">Vlastnost **Nadpis** podporuje značky nadpisů.</span><span class="sxs-lookup"><span data-stu-id="08331-133">The **Heading** property supports heading tags.</span></span> <span data-ttu-id="08331-134">Standardně je použita značka nadpisu **H2**, ale značku nadpisu lze změnit, aby odpovídala požadavkům na usnadnění.</span><span class="sxs-lookup"><span data-stu-id="08331-134">By default, the **H2** heading tag is used, but the heading tag can be changed to meet accessibility requirements.</span></span> |
| <span data-ttu-id="08331-135">Odstavec</span><span class="sxs-lookup"><span data-stu-id="08331-135">Paragraph</span></span>     | <span data-ttu-id="08331-136">Text odstavce</span><span class="sxs-lookup"><span data-stu-id="08331-136">Paragraph text</span></span> | <span data-ttu-id="08331-137">Moduly položek umístění obsahu podporují text odstavce ve formátu RTF.</span><span class="sxs-lookup"><span data-stu-id="08331-137">Content placement item modules support paragraph text in rich text format.</span></span> <span data-ttu-id="08331-138">Jsou podporovány některé základní funkce pro formát RTF, například tučné a podtržené písmo, kurzíva a hypertextové odkazy.</span><span class="sxs-lookup"><span data-stu-id="08331-138">Some basic rich text capabilities are supported, such as bold, underlined, and italic text, and hyperlinks.</span></span> <span data-ttu-id="08331-139">Některé z těchto funkcí mohou být přepsány motivem stránky, který je použit pro daný modul.</span><span class="sxs-lookup"><span data-stu-id="08331-139">Some of these capabilities can be overridden by the page theme that is applied to the module.</span></span> |
| <span data-ttu-id="08331-140">Obrázek</span><span class="sxs-lookup"><span data-stu-id="08331-140">Image</span></span>         | <span data-ttu-id="08331-141">Soubor obrázku</span><span class="sxs-lookup"><span data-stu-id="08331-141">Image file</span></span> | <span data-ttu-id="08331-142">K textu může být přidružen obrázek.</span><span class="sxs-lookup"><span data-stu-id="08331-142">An image can be associated with the text.</span></span> |
| <span data-ttu-id="08331-143">Připojení</span><span class="sxs-lookup"><span data-stu-id="08331-143">Link</span></span>          | <span data-ttu-id="08331-144">Adresa URL odkazu a text odkazu</span><span class="sxs-lookup"><span data-stu-id="08331-144">Link URL and link text</span></span> | <span data-ttu-id="08331-145">K textu lze přidat odkaz a přesměrovat uživatele na určitou stránku.</span><span class="sxs-lookup"><span data-stu-id="08331-145">A link can be added to the text to redirect users to a specific page.</span></span> |
| <span data-ttu-id="08331-146">Velikost dlaždice</span><span class="sxs-lookup"><span data-stu-id="08331-146">Tile size</span></span>     | <span data-ttu-id="08331-147">Číslo od **1** do **12**</span><span class="sxs-lookup"><span data-stu-id="08331-147">A number from **1** through **12**</span></span> | <span data-ttu-id="08331-148">Tato vlastnost definuje pro každou položku umístění obsahu počet pozic, které by měla položka vyplnit v modulu umístění obsahu.</span><span class="sxs-lookup"><span data-stu-id="08331-148">For each content placement item, this property defines the number of slots that the item should fill in the content placement module.</span></span> <span data-ttu-id="08331-149">Maximální velikost modulu umístění obsahu je 12 pozic.</span><span class="sxs-lookup"><span data-stu-id="08331-149">The maximum size of the content placement module is 12 slots.</span></span> <span data-ttu-id="08331-150">Pokud celková velikost dlaždice pro prvních *n* položek v modulu umístění obsahu překračuje 12 pozic, budou položky zalomeny na další řádek.</span><span class="sxs-lookup"><span data-stu-id="08331-150">If the total tile size for the first *n* items in the content placement module exceeds 12 slots, the items are wrapped to the next row.</span></span> |

## <a name="add-a-content-placement-module-that-contains-a-content-placement-item-module-to-a-page"></a><span data-ttu-id="08331-151">Přidání modulu umístění obsahu obsahujícího modul položky umístění obsahu na stránku</span><span class="sxs-lookup"><span data-stu-id="08331-151">Add a content placement module that contains a content placement item module to a page</span></span>

<span data-ttu-id="08331-152">Chcete-li přidat modul umístění obsahu obsahující modul položky umístění obsahu na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="08331-152">To add a content placement module that contains a content placement item module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="08331-153">Vytvořte šablonu s názvem **Šablona umístění obsahu**.</span><span class="sxs-lookup"><span data-stu-id="08331-153">Create a template that is named **content placement template**.</span></span>
1. <span data-ttu-id="08331-154">V pozici **Hlavní** na výchozí stránce přidejte modul umístění obsahu.</span><span class="sxs-lookup"><span data-stu-id="08331-154">In the **Main** slot of the default page, add a content placement module.</span></span>
1. <span data-ttu-id="08331-155">V modulu umístění obsahu obsahujícího přidejte modul položky umístění obsahu.</span><span class="sxs-lookup"><span data-stu-id="08331-155">In the content placement module, add a content placement item module.</span></span>
1. <span data-ttu-id="08331-156">Vraťte šablonu se změnami a publikujte ji.</span><span class="sxs-lookup"><span data-stu-id="08331-156">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="08331-157">Šablonu umístění obsahu, kterou jste právě vytvořili, použijte pro vytvoření stránky s názvem **Stránka umístění obsahu**.</span><span class="sxs-lookup"><span data-stu-id="08331-157">Use the content placement template that you just created to create a page that is named **Content placement page**.</span></span>
1. <span data-ttu-id="08331-158">V pozici **Hlavní** na nové stránce přidejte modul umístění obsahu.</span><span class="sxs-lookup"><span data-stu-id="08331-158">In the **Main** slot of the new page, add a content placement module.</span></span>
1. <span data-ttu-id="08331-159">V modulu umístění obsahu obsahujícího přidejte modul položky umístění obsahu.</span><span class="sxs-lookup"><span data-stu-id="08331-159">In the content placement module, add a content placement item module.</span></span>
1. <span data-ttu-id="08331-160">V podokně vlastností pro modul položky umístění obsahu vyberte obrázek, přidejte nadpis, přidejte odstavec, přidejte odkaz, nastavte adresu URL odkazu a nastavte velikost dlaždice na **6**.</span><span class="sxs-lookup"><span data-stu-id="08331-160">In the property pane for the content placement item module, select an image, add a heading, add a paragraph, add a link, set the link URL, and set the tile size to **6**.</span></span>
1. <span data-ttu-id="08331-161">Zopakováním kroků 7 a 8 přidejte další položku umístění obsahu, která má stejnou velikost dlaždice.</span><span class="sxs-lookup"><span data-stu-id="08331-161">Repeat steps 7 and 8 to add another content placement item module that has the same tile size.</span></span>
1. <span data-ttu-id="08331-162">Uložte stránku a zobrazte náhled.</span><span class="sxs-lookup"><span data-stu-id="08331-162">Save and preview the page.</span></span> <span data-ttu-id="08331-163">Měly by se zobrazit dvě položky umístění obsahu vedle sebe.</span><span class="sxs-lookup"><span data-stu-id="08331-163">You should see two content placement items that appear side by side.</span></span> <span data-ttu-id="08331-164">Chcete-li dosáhnout požadovaného rozložení, můžete upravit vlastnost **Velikost dlaždice** u každého modulu položky umístění obsahu nebo přidat další moduly.</span><span class="sxs-lookup"><span data-stu-id="08331-164">You can adjust the **Tile size** property of each content placement item module or add more modules to achieve the desired layout.</span></span>
1. <span data-ttu-id="08331-165">Vraťte stránku se změnami a publikujte ji.</span><span class="sxs-lookup"><span data-stu-id="08331-165">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="08331-166">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="08331-166">Additional resources</span></span>

[<span data-ttu-id="08331-167">Přehled startovací sady</span><span class="sxs-lookup"><span data-stu-id="08331-167">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="08331-168">Modul výstrahy</span><span class="sxs-lookup"><span data-stu-id="08331-168">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="08331-169">Karuselový modul</span><span class="sxs-lookup"><span data-stu-id="08331-169">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="08331-170">Modul bloku s formátovaným obsahem</span><span class="sxs-lookup"><span data-stu-id="08331-170">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="08331-171">Propagační modul</span><span class="sxs-lookup"><span data-stu-id="08331-171">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="08331-172">Modul hlavního banneru</span><span class="sxs-lookup"><span data-stu-id="08331-172">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="08331-173">Modul přehrávače videa</span><span class="sxs-lookup"><span data-stu-id="08331-173">Video player module</span></span>](add-video-player.md)
