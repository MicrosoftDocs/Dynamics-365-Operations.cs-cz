---
title: Modul textového bloku
description: Tohle téma se zabývá moduly textového bloku a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: fc5b2fa35633b1ce7f7ffefacec318e14fa8db3f
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025590"
---
# <a name="text-block-module"></a><span data-ttu-id="cea64-103">Modul textového bloku</span><span class="sxs-lookup"><span data-stu-id="cea64-103">Text block module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="cea64-104">Tohle téma se zabývá moduly textového bloku a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="cea64-104">This topic covers text block modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="cea64-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="cea64-105">Overview</span></span>

<span data-ttu-id="cea64-106">Modul textového bloku je modul, který se používá k přidání textového obsahu.</span><span class="sxs-lookup"><span data-stu-id="cea64-106">A text block module is a module that is used to add textual content.</span></span> <span data-ttu-id="cea64-107">Tento obsah může být informativní nebo propagační.</span><span class="sxs-lookup"><span data-stu-id="cea64-107">This content can be informational or promotional.</span></span>

<span data-ttu-id="cea64-108">Moduly textového bloku jsou řízeny daty ze systému správy obsahu (CMS) a lze je umístit na libovolnou stránku.</span><span class="sxs-lookup"><span data-stu-id="cea64-108">Text block modules are driven by data from the content management system (CMS) and can be put on any page.</span></span> <span data-ttu-id="cea64-109">Jedná se o samostatné moduly, které nezávisejí na kontextu stránky ani na jiných modulech.</span><span class="sxs-lookup"><span data-stu-id="cea64-109">They are stand-alone modules that don't depend on page context or any other modules.</span></span>

## <a name="examples-of-text-block-modules-in-e-commerce"></a><span data-ttu-id="cea64-110">Příklady modulů textového bloku v elektronickém obchodování</span><span class="sxs-lookup"><span data-stu-id="cea64-110">Examples of text block modules in e-Commerce</span></span>

<span data-ttu-id="cea64-111">Moduly tetových bloků lze používat následujícími způsoby:</span><span class="sxs-lookup"><span data-stu-id="cea64-111">Text block modules can be used in the following ways:</span></span>

* <span data-ttu-id="cea64-112">K prezentaci funkcí produktu na stránce s podrobnostmi o produktu.</span><span class="sxs-lookup"><span data-stu-id="cea64-112">To showcase product features on a product details page.</span></span>
* <span data-ttu-id="cea64-113">Pro informativní potřeby na libovolné stránce.</span><span class="sxs-lookup"><span data-stu-id="cea64-113">For informational purposes on any page.</span></span> <span data-ttu-id="cea64-114">Mohou například vysvětlit výhody věrnostních programů, popsat zásady dodávek a vrácení, odpovídat na nejčastější dotazy nebo poskytovat obsah „o nás“.</span><span class="sxs-lookup"><span data-stu-id="cea64-114">For example, they can explain the benefits of loyalty programs, describe shipping and return policies, answer frequently asked questions, or provide "about us" content.</span></span>
* <span data-ttu-id="cea64-115">Chcete-li přidat vlastní zprávy na stránce s podrobnostmi o produktu</span><span class="sxs-lookup"><span data-stu-id="cea64-115">To add custom messages on a product details page.</span></span> <span data-ttu-id="cea64-116">(například „Bezplatné poštovné u objednávek přes 1 000 Kč“).</span><span class="sxs-lookup"><span data-stu-id="cea64-116">(for example, "Free shipping for orders over $50").</span></span>
* <span data-ttu-id="cea64-117">K zobrazení informací o právních omezeních a kontaktech na stránce s podrobnostmi o produktu, stránce košíku, stránkách pokladny a dalších stránkách (například „Dodávky a refundace podléhají zásadám obchodu“).</span><span class="sxs-lookup"><span data-stu-id="cea64-117">For disclaimers and contact details on product details pages, cart pages, checkout pages, and other pages (for example, "Shipping and returns are subject to store policies").</span></span>

## <a name="text-block-module-properties"></a><span data-ttu-id="cea64-118">Vlasstnosti modulu textového bloku</span><span class="sxs-lookup"><span data-stu-id="cea64-118">Text block module properties</span></span>

| <span data-ttu-id="cea64-119">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="cea64-119">Property name</span></span>     | <span data-ttu-id="cea64-120">Value</span><span class="sxs-lookup"><span data-stu-id="cea64-120">Value</span></span>                                            | <span data-ttu-id="cea64-121">Popis</span><span class="sxs-lookup"><span data-stu-id="cea64-121">Description</span></span> |
|-------------------|--------------------------------------------------|-------------|
| <span data-ttu-id="cea64-122">Formátovaný text</span><span class="sxs-lookup"><span data-stu-id="cea64-122">Rich text</span></span>         | <span data-ttu-id="cea64-123">Formátovaný text</span><span class="sxs-lookup"><span data-stu-id="cea64-123">Rich text</span></span>                                        | <span data-ttu-id="cea64-124">Text odstavce.</span><span class="sxs-lookup"><span data-stu-id="cea64-124">Paragraph text.</span></span> <span data-ttu-id="cea64-125">Jsou podporovány některé základní funkce pro formát RTF, například tučné a podtržené písmo a kurzíva.</span><span class="sxs-lookup"><span data-stu-id="cea64-125">Some basic rich text capabilities are supported, such as bold, underlined, and italic text.</span></span> |
| <span data-ttu-id="cea64-126">Vlastní název třídy</span><span class="sxs-lookup"><span data-stu-id="cea64-126">Custom class name</span></span> | <span data-ttu-id="cea64-127">Název třídy Cascading Style Sheets (CSS)</span><span class="sxs-lookup"><span data-stu-id="cea64-127">A Cascading Style Sheets (CSS) class name</span></span>        | <span data-ttu-id="cea64-128">Název vlastní CSS třídy, kterou vývojář poskytuje k formátování tohoto modulu.</span><span class="sxs-lookup"><span data-stu-id="cea64-128">The name of a custom CSS class that a developer provides to format this module.</span></span> <span data-ttu-id="cea64-129">Název třídy by měl být definován v balíku motivů.</span><span class="sxs-lookup"><span data-stu-id="cea64-129">The class name should be defined in the theme pack.</span></span> |
| <span data-ttu-id="cea64-130">Velikost písma</span><span class="sxs-lookup"><span data-stu-id="cea64-130">Font size</span></span>         | <span data-ttu-id="cea64-131">**Malá**, **Střední**, **Velká** nebo **Extra velká**</span><span class="sxs-lookup"><span data-stu-id="cea64-131">**Small**, **Medium**, **Large**, or **X-Large**</span></span> | <span data-ttu-id="cea64-132">Velikost písma obsahu.</span><span class="sxs-lookup"><span data-stu-id="cea64-132">The font size of the content.</span></span> |

## <a name="add-a-text-block-module-to-a-page"></a><span data-ttu-id="cea64-133">Přidání modulu textového bloku na stránku</span><span class="sxs-lookup"><span data-stu-id="cea64-133">Add a text block module to a page</span></span>

<span data-ttu-id="cea64-134">Chcete-li přidat modul textového bloku na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="cea64-134">To add a text block module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="cea64-135">Vytvořte šablonu stránky s názvem **Šablona obsahu**.</span><span class="sxs-lookup"><span data-stu-id="cea64-135">Create a page template that is named **Content template**.</span></span> 
1. <span data-ttu-id="cea64-136">Do úseku **Tělo** přidejte modul **Výchozí stránka**.</span><span class="sxs-lookup"><span data-stu-id="cea64-136">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="cea64-137">Dokončete úpravy šablony a publikujte ji.</span><span class="sxs-lookup"><span data-stu-id="cea64-137">Finish editing the template, and publish it.</span></span>
1. <span data-ttu-id="cea64-138">Šablonu obsahu, kterou jste právě vytvořili, použijte pro vytvoření stránky s názvem **Stránka obsahu**.</span><span class="sxs-lookup"><span data-stu-id="cea64-138">Use the content template that you just created to create a page that is named **Content page**.</span></span>
1. <span data-ttu-id="cea64-139">V úseku **Hlavní** nové stránky přidejte modul kontejneru.</span><span class="sxs-lookup"><span data-stu-id="cea64-139">In the **Main** slot of the new page, add a container module.</span></span>
1. <span data-ttu-id="cea64-140">V podokně vlastností modulu kontejner nastavte vlastnost **Šířka** na **Vyplnit kontejner**.</span><span class="sxs-lookup"><span data-stu-id="cea64-140">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="cea64-141">Přidejte modul textového bloku do modulu kontejneru.</span><span class="sxs-lookup"><span data-stu-id="cea64-141">Add a text block module to the container module.</span></span> 
1. <span data-ttu-id="cea64-142">V podokně vlastností modulu textového bloku přidejte text do pole **RTF**.</span><span class="sxs-lookup"><span data-stu-id="cea64-142">In the property pane of the text block module, add text to the **Rich text** field.</span></span>
1. <span data-ttu-id="cea64-143">Dokončete úpravy stránky a publikujte ji.</span><span class="sxs-lookup"><span data-stu-id="cea64-143">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cea64-144">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="cea64-144">Additional resources</span></span>

[<span data-ttu-id="cea64-145">Přehled startovací sady</span><span class="sxs-lookup"><span data-stu-id="cea64-145">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="cea64-146">Modul propagačního banneru</span><span class="sxs-lookup"><span data-stu-id="cea64-146">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="cea64-147">Karuselový modul</span><span class="sxs-lookup"><span data-stu-id="cea64-147">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="cea64-148">Modul bloku obsahu</span><span class="sxs-lookup"><span data-stu-id="cea64-148">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="cea64-149">Modul videopřehrávače</span><span class="sxs-lookup"><span data-stu-id="cea64-149">Video player module</span></span>](add-video-player.md)

