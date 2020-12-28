---
title: Modul iframe
description: Tohle téma se zabývá modulem iframe a popisuje, jak jej přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
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
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 4afd8f60938c99d1981be1625ef28f91d9e4bb4c
ms.sourcegitcommit: 9c05d48f6e03532aa711e1d89d0b2981e9d37200
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/03/2020
ms.locfileid: "4665389"
---
# <a name="iframe-module"></a><span data-ttu-id="b286c-103">Modul iframe</span><span class="sxs-lookup"><span data-stu-id="b286c-103">Iframe module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b286c-104">Tohle téma se zabývá modulem iframe a popisuje, jak jej přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b286c-104">This topic covers the iframe module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b286c-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="b286c-105">Overview</span></span>

<span data-ttu-id="b286c-106">Modul iframe poskytuje prvek iframe (vložený rámec), který hostuje externí obsah na webu.</span><span class="sxs-lookup"><span data-stu-id="b286c-106">An iframe module provides an iframe (inline frame) that hosts external content on a site.</span></span> <span data-ttu-id="b286c-107">Například může být použit k hostování videa YouTube nebo prohlížeče souborů PDF na jakékoli stránce webu.</span><span class="sxs-lookup"><span data-stu-id="b286c-107">For example, it can be used to host a YouTube video or a PDF file viewer on any site page.</span></span> 

<span data-ttu-id="b286c-108">Modul iframe vyžaduje cílovou adresu URL.</span><span class="sxs-lookup"><span data-stu-id="b286c-108">An iframe module requires a target URL.</span></span> <span data-ttu-id="b286c-109">Poté je hostitelem obsahu cílové stránky uvnitř prvku HTML **iframe**.</span><span class="sxs-lookup"><span data-stu-id="b286c-109">It then hosts the content of the target page inside an HTML **iframe** element.</span></span> <span data-ttu-id="b286c-110">Externí adresy URL musí být na seznamu povolených podle směrnic o zásadách zabezpečení obsahu webu (CSP).</span><span class="sxs-lookup"><span data-stu-id="b286c-110">External URLs must be on the allow list per the site's content security policy (CSP) directives.</span></span> <span data-ttu-id="b286c-111">U obsahu prvku iframe by měly být adresy URL povoleny pomocí směrnice **frame-ancestor**.</span><span class="sxs-lookup"><span data-stu-id="b286c-111">For iframe content, URLs should be allowed by using the **frame-ancestor** directive.</span></span> <span data-ttu-id="b286c-112">Další informace viz [Správa zásad zabezpečení obsahu (CSP)](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="b286c-112">For more information, see [Manage Content Security Policy (CSP)](manage-csp.md).</span></span>

> [!NOTE]
> <span data-ttu-id="b286c-113">Modul iframe je k dispozici v Dynamics 365 Commerce vydání 10.0.13.</span><span class="sxs-lookup"><span data-stu-id="b286c-113">The iframe module is available in the Dynamics 365 Commerce 10.0.13 release.</span></span>

<span data-ttu-id="b286c-114">Následující obrázek ukazuje příklady modulů iframe, které zobrazují externí videa na stránkách webu.</span><span class="sxs-lookup"><span data-stu-id="b286c-114">The following image shows examples of iframe modules that showcase external videos on site pages.</span></span>

![Příklad modulů iframe zobrazujících externí videa](./media/ecommerce-iframe.PNG)

## <a name="iframe-module-properties"></a><span data-ttu-id="b286c-116">Vlastnosti modulu iframe</span><span class="sxs-lookup"><span data-stu-id="b286c-116">Iframe module properties</span></span>

| <span data-ttu-id="b286c-117">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="b286c-117">Property name</span></span>             | <span data-ttu-id="b286c-118">Hodnota</span><span class="sxs-lookup"><span data-stu-id="b286c-118">Value</span></span>                 | <span data-ttu-id="b286c-119">popis</span><span class="sxs-lookup"><span data-stu-id="b286c-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="b286c-120">Nadpis</span><span class="sxs-lookup"><span data-stu-id="b286c-120">Heading</span></span> | <span data-ttu-id="b286c-121">Text</span><span class="sxs-lookup"><span data-stu-id="b286c-121">Text</span></span> | <span data-ttu-id="b286c-122">Nadpis modulu.</span><span class="sxs-lookup"><span data-stu-id="b286c-122">The heading for the module.</span></span> |
| <span data-ttu-id="b286c-123">Cílová adresa URL</span><span class="sxs-lookup"><span data-stu-id="b286c-123">Target URL</span></span> | <span data-ttu-id="b286c-124">Adresa URL</span><span class="sxs-lookup"><span data-stu-id="b286c-124">URL</span></span> | <span data-ttu-id="b286c-125">Adresa URL, která je hostována v modulu.</span><span class="sxs-lookup"><span data-stu-id="b286c-125">The URL that is hosted in the module.</span></span> |
| <span data-ttu-id="b286c-126">Výška</span><span class="sxs-lookup"><span data-stu-id="b286c-126">Height</span></span> | <span data-ttu-id="b286c-127">Počet nebo procento</span><span class="sxs-lookup"><span data-stu-id="b286c-127">Number or percentage</span></span> | <span data-ttu-id="b286c-128">Výška modulu v pixelech nebo v procentech.</span><span class="sxs-lookup"><span data-stu-id="b286c-128">The height of the module, in pixels or as a percentage.</span></span> <span data-ttu-id="b286c-129">Například hodnota **100** bude považována za počet pixelů a hodnota **100%** bude považována za procento.</span><span class="sxs-lookup"><span data-stu-id="b286c-129">For example, the value **100** will be treated as a number of pixels, and the value **100%** will be treated as a percentage.</span></span> |
| <span data-ttu-id="b286c-130">Popisek aria</span><span class="sxs-lookup"><span data-stu-id="b286c-130">Aria label</span></span> | <span data-ttu-id="b286c-131">Text</span><span class="sxs-lookup"><span data-stu-id="b286c-131">Text</span></span> | <span data-ttu-id="b286c-132">Pro účely usnadnění přístupu lze definovat označení přístupných aplikací Rich Internet Applications (ARIA).</span><span class="sxs-lookup"><span data-stu-id="b286c-132">An Accessible Rich Internet Applications (ARIA) label can be defined for accessibility purposes.</span></span> |

## <a name="add-an-iframe-module-to-a-page"></a><span data-ttu-id="b286c-133">Přidání modulu iframe na stránku</span><span class="sxs-lookup"><span data-stu-id="b286c-133">Add an iframe module to a page</span></span>

<span data-ttu-id="b286c-134">Chcete-li na stránku přidat modul iframe a zobrazit externí video, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="b286c-134">To add an iframe module to a page to show an external video, follow these steps.</span></span>

1. <span data-ttu-id="b286c-135">Přejděte na **Šablony** a poté volbou **Nová** vytvořte novou šablonu.</span><span class="sxs-lookup"><span data-stu-id="b286c-135">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="b286c-136">V dialogovém okně **Nová šablona** v části **Název šablony** zadejte **Šablona marketingu** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="b286c-136">In the **New Template** dialog box, under **Template name**, enter **Marketing template**, and then select **OK**.</span></span>
1. <span data-ttu-id="b286c-137">Chcete-li vrátit šablonu se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="b286c-137">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="b286c-138">Přejděte na **Stránky** a volbou **Nová** vytvořte novou stránku.</span><span class="sxs-lookup"><span data-stu-id="b286c-138">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="b286c-139">V dialogovém okně **Zvolte šablonu** vyberte šablonu **Šablona marketingu**.</span><span class="sxs-lookup"><span data-stu-id="b286c-139">In the **Choose a template** dialog box, select the **Marketing template** template.</span></span> <span data-ttu-id="b286c-140">V části **Název stránky** zadejte **Stránka marketingu** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="b286c-140">Under **Page name**, enter **Marketing page**, and then select **OK**.</span></span>
1. <span data-ttu-id="b286c-141">V pozici **Hlavní** na nové stránce vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="b286c-141">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b286c-142">V dialogovém okně **Přidat modul** vyberte modul **Kontejner** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="b286c-142">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b286c-143">V podokně vlastností modulu nastavte hodnotu **Šířka** na **Vyplnit kontejner**.</span><span class="sxs-lookup"><span data-stu-id="b286c-143">In the module's properties pane, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="b286c-144">V pozici **Kontejner** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="b286c-144">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b286c-145">V dialogovém okně **Přidat modul** vyberte modul **iframe** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="b286c-145">In the **Add Module** dialog box, select the **iframe** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b286c-146">V podokně vlastností modulu nastavte hodnotu **Cílová adresa URL** externí adresy URL videa.</span><span class="sxs-lookup"><span data-stu-id="b286c-146">In the module's properties pane, set the **Target URL** value to an external URL for a video.</span></span>
1. <span data-ttu-id="b286c-147">Nastavte další vlastnosti, například **Nadpis** a **Výška**, dle potřeby.</span><span class="sxs-lookup"><span data-stu-id="b286c-147">Set other properties, such as **Heading** and **Height**, as you require.</span></span>
1. <span data-ttu-id="b286c-148">Chcete-li vrátit stránku se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="b286c-148">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="b286c-149">Přejděte na marketingovou stránku svého webu.</span><span class="sxs-lookup"><span data-stu-id="b286c-149">Go to the marketing page on your site.</span></span> <span data-ttu-id="b286c-150">Měli byste vidět, že video je vykresleno v modulu iframe.</span><span class="sxs-lookup"><span data-stu-id="b286c-150">You should see that the video is rendered in the iframe module.</span></span>
 
## <a name="additional-resources"></a><span data-ttu-id="b286c-151">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="b286c-151">Additional resources</span></span>

[<span data-ttu-id="b286c-152">Přehled knihovny modulů</span><span class="sxs-lookup"><span data-stu-id="b286c-152">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="b286c-153">Správa zásad zabezpečení obsahu (CSP)</span><span class="sxs-lookup"><span data-stu-id="b286c-153">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)
