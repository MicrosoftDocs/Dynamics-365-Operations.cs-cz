---
title: Modul bloku s formátovaným obsahem
description: Tohle téma se zabývá moduly bloků s formátovaným obsahem a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 27dabb425b3c9a3015ffc54ff3c0e50b7ee11749
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785414"
---
# <a name="content-rich-block-module"></a><span data-ttu-id="8b282-103">Modul bloku s formátovaným obsahem</span><span class="sxs-lookup"><span data-stu-id="8b282-103">Content rich block module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="8b282-104">Tohle téma se zabývá moduly bloků s formátovaným obsahem a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8b282-104">This topic covers content rich block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="8b282-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="8b282-105">Overview</span></span>

<span data-ttu-id="8b282-106">Modul bloku s formátovaným obsahem je speciální kontejner, do kterého lze vložit jednu nebo více položek bloku s formátovaným obsahem.</span><span class="sxs-lookup"><span data-stu-id="8b282-106">A content rich block module is a special container that one or more content rich block items can be put inside.</span></span> <span data-ttu-id="8b282-107">Moduly bloků s formátovaným obsahem se používají pro textový obsah na stránce.</span><span class="sxs-lookup"><span data-stu-id="8b282-107">Content rich block modules are used for textual content on a page.</span></span> <span data-ttu-id="8b282-108">Tento obsah může být buď informativní, nebo propagační.</span><span class="sxs-lookup"><span data-stu-id="8b282-108">This content can be either informational or promotional.</span></span>

<span data-ttu-id="8b282-109">Moduly bloků s formátovaným obsahem jsou řízeny daty ze systému správy obsahu (CMS) a lze je umístit na libovolnou stránku.</span><span class="sxs-lookup"><span data-stu-id="8b282-109">Content rich block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="8b282-110">Jedná se o samostatné moduly, které nezávisejí na kontextu stránky ani na jiných modulech.</span><span class="sxs-lookup"><span data-stu-id="8b282-110">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-content-rich-block-modules-in-e-commerce"></a><span data-ttu-id="8b282-111">Příklady modulů bloků s formátovaným obsahem v elektronickém obchodování</span><span class="sxs-lookup"><span data-stu-id="8b282-111">Examples of content rich block modules in e-Commerce</span></span>

<span data-ttu-id="8b282-112">Moduly bloků s formátovaným obsahem lze používat následujícími způsoby:</span><span class="sxs-lookup"><span data-stu-id="8b282-112">Content rich block modules can be used in the following ways:</span></span>

* <span data-ttu-id="8b282-113">K prezentaci funkcí produktu na stránce s podrobnostmi o produktu.</span><span class="sxs-lookup"><span data-stu-id="8b282-113">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="8b282-114">Pro informativní potřeby na libovolné stránce.</span><span class="sxs-lookup"><span data-stu-id="8b282-114">For informational purposes on any page.</span></span> <span data-ttu-id="8b282-115">Mohou například vysvětlit výhody věrnostních programů, popsat zásady dodávek a vrácení, odpovídat na nejčastější dotazy nebo poskytovat obsah „o nás“.</span><span class="sxs-lookup"><span data-stu-id="8b282-115">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="8b282-116">Chcete-li přidat vlastní zprávy na stránce s podrobnostmi o produktu</span><span class="sxs-lookup"><span data-stu-id="8b282-116">To add custom messages on a product details page.</span></span> <span data-ttu-id="8b282-117">(například „Bezplatné poštovné u objednávek přes 1 000 Kč“).</span><span class="sxs-lookup"><span data-stu-id="8b282-117">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="8b282-118">K zobrazení informací o právních omezeních a kontaktech na stránce s podrobnostmi o produktu, stránce košíku, stránkách pokladny a dalších stránkách (například „Dodávky a refundace podléhají zásadám obchodu“).</span><span class="sxs-lookup"><span data-stu-id="8b282-118">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

## <a name="content-rich-block-module-properties"></a><span data-ttu-id="8b282-119">Vlastnosti modulu bloku s formátovaným obsahem</span><span class="sxs-lookup"><span data-stu-id="8b282-119">Content rich block module properties</span></span>

| <span data-ttu-id="8b282-120">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="8b282-120">Property name</span></span>     | <span data-ttu-id="8b282-121">Hodnota</span><span class="sxs-lookup"><span data-stu-id="8b282-121">Value</span></span>                                 | <span data-ttu-id="8b282-122">Vlastnost</span><span class="sxs-lookup"><span data-stu-id="8b282-122">Property</span></span> |
|-------------------|---------------------------------------|----------|
| <span data-ttu-id="8b282-123">Počet sloupců</span><span class="sxs-lookup"><span data-stu-id="8b282-123">Number of columns</span></span> | <span data-ttu-id="8b282-124">Číslo od **1** do **4**</span><span class="sxs-lookup"><span data-stu-id="8b282-124">A number from **1** through **4**</span></span>     | <span data-ttu-id="8b282-125">Počet sloupců v bloku s formátovaným obsahem.</span><span class="sxs-lookup"><span data-stu-id="8b282-125">The number of columns in the content rich block.</span></span> <span data-ttu-id="8b282-126">Může mít až čtyři sloupce.</span><span class="sxs-lookup"><span data-stu-id="8b282-126">There can be up to four columns.</span></span> |
| <span data-ttu-id="8b282-127">Šířka</span><span class="sxs-lookup"><span data-stu-id="8b282-127">Width</span></span>             | <span data-ttu-id="8b282-128">**Vyplnit kontejner** nebo **Vyplnit obrazovku**</span><span class="sxs-lookup"><span data-stu-id="8b282-128">**Fill container** or **Fill screen**</span></span> | <span data-ttu-id="8b282-129">Je-li hodnota nastavena na **Vyplnit kontejner**, budou položky uvnitř kontejneru omezeny na jeho šířku.</span><span class="sxs-lookup"><span data-stu-id="8b282-129">If the value is set to **Fill container**, the items inside the container are restricted to the width of the container.</span></span> <span data-ttu-id="8b282-130">Je-li hodnota nastavena na **Vyplnit obrazovku**, položky nejsou omezeny na šířku kontejneru, ale mohou přejít do režimu celé obrazovky.</span><span class="sxs-lookup"><span data-stu-id="8b282-130">If the value is set to **Fill screen**, the items aren't restricted to the container width but can go into full-screen mode.</span></span> <span data-ttu-id="8b282-131">Chcete-li dosáhnout požadovaného rozvržení, můžete změnit tuto hodnotu.</span><span class="sxs-lookup"><span data-stu-id="8b282-131">You can change the value to achieve the desired layout.</span></span> |

## <a name="content-rich-block-item-module-properties"></a><span data-ttu-id="8b282-132">Vlastnosti modulu položky bloku s formátovaným obsahem</span><span class="sxs-lookup"><span data-stu-id="8b282-132">Content rich block item module properties</span></span>

| <span data-ttu-id="8b282-133">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="8b282-133">Property name</span></span> | <span data-ttu-id="8b282-134">Hodnota</span><span class="sxs-lookup"><span data-stu-id="8b282-134">Value</span></span>          | <span data-ttu-id="8b282-135">Popis</span><span class="sxs-lookup"><span data-stu-id="8b282-135">Description</span></span> |
|---------------|----------------|-------------|
| <span data-ttu-id="8b282-136">Odstavec</span><span class="sxs-lookup"><span data-stu-id="8b282-136">Paragraph</span></span>     | <span data-ttu-id="8b282-137">Text odstavce</span><span class="sxs-lookup"><span data-stu-id="8b282-137">Paragraph text</span></span> | <span data-ttu-id="8b282-138">Text, který provází jednotlivé položky bloku s formátovaným obsahem.</span><span class="sxs-lookup"><span data-stu-id="8b282-138">The text that accompanies each content rich block item.</span></span> <span data-ttu-id="8b282-139">Jsou podporovány některé základní funkce pro formát RTF, například tučné a podtržené písmo a kurzíva.</span><span class="sxs-lookup"><span data-stu-id="8b282-139">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |

## <a name="add-a-content-rich-block-module-to-a-page"></a><span data-ttu-id="8b282-140">Přidání modulu bloku s formátovaným obsahem na stránku</span><span class="sxs-lookup"><span data-stu-id="8b282-140">Add a content rich block module to a page</span></span>

<span data-ttu-id="8b282-141">Chcete-li přidat modul bloku s formátovaným obsahem na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="8b282-141">To add a content rich block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="8b282-142">Vytvořte šablonu stránky s názvem **Šablona obsahu**.</span><span class="sxs-lookup"><span data-stu-id="8b282-142">Create a page template that is named **Content template**.</span></span>
1. <span data-ttu-id="8b282-143">V pozici **Hlavní** na výchozí stránce přidejte modul bloku s formátovaným obsahem.</span><span class="sxs-lookup"><span data-stu-id="8b282-143">In the **Main** slot of the default page, add a content rich block module.</span></span>
1. <span data-ttu-id="8b282-144">Vraťte šablonu se změnami a publikujte ji.</span><span class="sxs-lookup"><span data-stu-id="8b282-144">Check in the template, and publish it.</span></span>
1. <span data-ttu-id="8b282-145">Šablonu obsahu, kterou jste právě vytvořili, použijte pro vytvoření stránky s názvem **Stránka obsahu**.</span><span class="sxs-lookup"><span data-stu-id="8b282-145">Use the content template that you just created to create a page that is named **Content page**.</span></span>
1. <span data-ttu-id="8b282-146">V pozici **Hlavní** na nové stránce přidejte modul bloku s formátovaným obsahem.</span><span class="sxs-lookup"><span data-stu-id="8b282-146">In the **Main** slot of the new page, add a content rich block module.</span></span>
1. <span data-ttu-id="8b282-147">Ve vlastnostech modulu bloku s formátovaným obsahem nastavte počet sloupců na **2**.</span><span class="sxs-lookup"><span data-stu-id="8b282-147">In the properties of the content rich block module, set number of columns to **2**.</span></span>
1. <span data-ttu-id="8b282-148">V modulu bloku s formátovaným obsahem vyberte možnost **Přidat modul** a přidejte položku bloku s formátovaným obsahem (například **Položka1**).</span><span class="sxs-lookup"><span data-stu-id="8b282-148">In the content rich block module, select **Add a module**, and add a content rich block item (for example, **item1**).</span></span>
1. <span data-ttu-id="8b282-149">V nové položce bloku s formátovaným obsahem přidejte text odstavce.</span><span class="sxs-lookup"><span data-stu-id="8b282-149">In the new content rich block item, add paragraph text.</span></span>
1. <span data-ttu-id="8b282-150">V modulu bloku s formátovaným obsahem vyberte možnost **Přidat modul** a přidejte položku bloku s formátovaným obsahem (například **Položka2**).</span><span class="sxs-lookup"><span data-stu-id="8b282-150">In the content rich block module, select **Add a module**, and add a content rich block item (for example, **item2**).</span></span>
1. <span data-ttu-id="8b282-151">V nové položce bloku s formátovaným obsahem přidejte text odstavce.</span><span class="sxs-lookup"><span data-stu-id="8b282-151">In the new content rich block item, add paragraph text.</span></span>
1. <span data-ttu-id="8b282-152">Uložte stránku a zobrazte náhled změn.</span><span class="sxs-lookup"><span data-stu-id="8b282-152">Save the page, and preview the changes.</span></span> <span data-ttu-id="8b282-153">V zobrazení se dvěma sloupci byste měli vidět dva bloky s formátovaným textem.</span><span class="sxs-lookup"><span data-stu-id="8b282-153">You should see two rich text blocks in a two-column view.</span></span>
1. <span data-ttu-id="8b282-154">Vraťte stránku se změnami a publikujte ji.</span><span class="sxs-lookup"><span data-stu-id="8b282-154">Check in the page, and publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="8b282-155">Přidáte-li třetí položku bloku s formátovaným obsahem, bude umístěna pod dvě dříve přidané položky.</span><span class="sxs-lookup"><span data-stu-id="8b282-155">If you add a third content rich block item, it will be stacked below the two items that you previously added.</span></span> <span data-ttu-id="8b282-156">Změnou počtu sloupců a položek v kontejneru můžete dosáhnout různých rozložení textového obsahu.</span><span class="sxs-lookup"><span data-stu-id="8b282-156">By changing the number of columns and items in the container, you can achieve different layouts for textual content.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8b282-157">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="8b282-157">Additional resources</span></span>

[<span data-ttu-id="8b282-158">Přehled startovací sady</span><span class="sxs-lookup"><span data-stu-id="8b282-158">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="8b282-159">Modul výstrahy</span><span class="sxs-lookup"><span data-stu-id="8b282-159">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="8b282-160">Karuselový modul</span><span class="sxs-lookup"><span data-stu-id="8b282-160">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="8b282-161">Modul umístění obsahu</span><span class="sxs-lookup"><span data-stu-id="8b282-161">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="8b282-162">Propagační modul</span><span class="sxs-lookup"><span data-stu-id="8b282-162">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="8b282-163">Modul hlavního banneru</span><span class="sxs-lookup"><span data-stu-id="8b282-163">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="8b282-164">Modul přehrávače videa</span><span class="sxs-lookup"><span data-stu-id="8b282-164">Video player module</span></span>](add-video-player.md)

