---
title: Modul iframe
description: Tohle téma se zabývá modulem iframe a popisuje, jak jej přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 7b397b91d1b8a45347ef2d05f42fb7c610ab3912
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797063"
---
# <a name="iframe-module"></a><span data-ttu-id="b9907-103">Modul iFrame</span><span class="sxs-lookup"><span data-stu-id="b9907-103">Iframe module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b9907-104">Tohle téma se zabývá modulem iframe a popisuje, jak jej přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b9907-104">This topic covers the iframe module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="b9907-105">Modul iframe poskytuje prvek iframe (vložený rámec), který hostuje externí obsah na webu.</span><span class="sxs-lookup"><span data-stu-id="b9907-105">An iframe module provides an iframe (inline frame) that hosts external content on a site.</span></span> <span data-ttu-id="b9907-106">Například může být použit k hostování videa YouTube nebo prohlížeče souborů PDF na jakékoli stránce webu.</span><span class="sxs-lookup"><span data-stu-id="b9907-106">For example, it can be used to host a YouTube video or a PDF file viewer on any site page.</span></span> 

<span data-ttu-id="b9907-107">Modul iframe vyžaduje cílovou adresu URL.</span><span class="sxs-lookup"><span data-stu-id="b9907-107">An iframe module requires a target URL.</span></span> <span data-ttu-id="b9907-108">Poté je hostitelem obsahu cílové stránky uvnitř prvku HTML **iframe**.</span><span class="sxs-lookup"><span data-stu-id="b9907-108">It then hosts the content of the target page inside an HTML **iframe** element.</span></span> <span data-ttu-id="b9907-109">Externí adresy URL musí být na seznamu povolených podle směrnic o zásadách zabezpečení obsahu webu (CSP).</span><span class="sxs-lookup"><span data-stu-id="b9907-109">External URLs must be on the allow list per the site's content security policy (CSP) directives.</span></span> <span data-ttu-id="b9907-110">U obsahu prvku iframe by měly být adresy URL povoleny pomocí směrnice **frame-ancestor**.</span><span class="sxs-lookup"><span data-stu-id="b9907-110">For iframe content, URLs should be allowed by using the **frame-ancestor** directive.</span></span> <span data-ttu-id="b9907-111">Další informace viz [Správa zásad zabezpečení obsahu (CSP)](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="b9907-111">For more information, see [Manage Content Security Policy (CSP)](manage-csp.md).</span></span>

> [!NOTE]
> <span data-ttu-id="b9907-112">Modul iframe je k dispozici v Dynamics 365 Commerce vydání 10.0.13.</span><span class="sxs-lookup"><span data-stu-id="b9907-112">The iframe module is available in the Dynamics 365 Commerce 10.0.13 release.</span></span>

<span data-ttu-id="b9907-113">Následující obrázek ukazuje příklady modulů iframe, které zobrazují externí videa na stránkách webu.</span><span class="sxs-lookup"><span data-stu-id="b9907-113">The following image shows examples of iframe modules that showcase external videos on site pages.</span></span>

![Příklad modulů iframe zobrazujících externí videa](./media/ecommerce-iframe.PNG)

## <a name="iframe-module-properties"></a><span data-ttu-id="b9907-115">Vlastnosti modulu iframe</span><span class="sxs-lookup"><span data-stu-id="b9907-115">Iframe module properties</span></span>

| <span data-ttu-id="b9907-116">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="b9907-116">Property name</span></span>             | <span data-ttu-id="b9907-117">Hodnota</span><span class="sxs-lookup"><span data-stu-id="b9907-117">Value</span></span>                 | <span data-ttu-id="b9907-118">popis</span><span class="sxs-lookup"><span data-stu-id="b9907-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="b9907-119">Nadpis</span><span class="sxs-lookup"><span data-stu-id="b9907-119">Heading</span></span> | <span data-ttu-id="b9907-120">Text</span><span class="sxs-lookup"><span data-stu-id="b9907-120">Text</span></span> | <span data-ttu-id="b9907-121">Nadpis modulu.</span><span class="sxs-lookup"><span data-stu-id="b9907-121">The heading for the module.</span></span> |
| <span data-ttu-id="b9907-122">Cílová adresa URL</span><span class="sxs-lookup"><span data-stu-id="b9907-122">Target URL</span></span> | <span data-ttu-id="b9907-123">Adresa URL</span><span class="sxs-lookup"><span data-stu-id="b9907-123">URL</span></span> | <span data-ttu-id="b9907-124">Adresa URL, která je hostována v modulu.</span><span class="sxs-lookup"><span data-stu-id="b9907-124">The URL that is hosted in the module.</span></span> |
| <span data-ttu-id="b9907-125">Výška</span><span class="sxs-lookup"><span data-stu-id="b9907-125">Height</span></span> | <span data-ttu-id="b9907-126">Počet nebo procento</span><span class="sxs-lookup"><span data-stu-id="b9907-126">Number or percentage</span></span> | <span data-ttu-id="b9907-127">Výška modulu v pixelech nebo v procentech.</span><span class="sxs-lookup"><span data-stu-id="b9907-127">The height of the module, in pixels or as a percentage.</span></span> <span data-ttu-id="b9907-128">Například hodnota **100** bude považována za počet pixelů a hodnota **100%** bude považována za procento.</span><span class="sxs-lookup"><span data-stu-id="b9907-128">For example, the value **100** will be treated as a number of pixels, and the value **100%** will be treated as a percentage.</span></span> |
| <span data-ttu-id="b9907-129">Popisek aria</span><span class="sxs-lookup"><span data-stu-id="b9907-129">Aria label</span></span> | <span data-ttu-id="b9907-130">Text</span><span class="sxs-lookup"><span data-stu-id="b9907-130">Text</span></span> | <span data-ttu-id="b9907-131">Pro účely usnadnění přístupu lze definovat označení přístupných aplikací Rich Internet Applications (ARIA).</span><span class="sxs-lookup"><span data-stu-id="b9907-131">An Accessible Rich Internet Applications (ARIA) label can be defined for accessibility purposes.</span></span> |

## <a name="add-an-iframe-module-to-a-page"></a><span data-ttu-id="b9907-132">Přidání modulu iframe na stránku</span><span class="sxs-lookup"><span data-stu-id="b9907-132">Add an iframe module to a page</span></span>

<span data-ttu-id="b9907-133">Chcete-li na stránku přidat modul iframe a zobrazit externí video, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="b9907-133">To add an iframe module to a page to show an external video, follow these steps.</span></span>

1. <span data-ttu-id="b9907-134">Přejděte na **Šablony** a poté volbou **Nová** vytvořte novou šablonu.</span><span class="sxs-lookup"><span data-stu-id="b9907-134">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="b9907-135">V dialogovém okně **Nová šablona** v části **Název šablony** zadejte **Šablona marketingu** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="b9907-135">In the **New Template** dialog box, under **Template name**, enter **Marketing template**, and then select **OK**.</span></span>
1. <span data-ttu-id="b9907-136">Chcete-li vrátit šablonu se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="b9907-136">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="b9907-137">Přejděte na **Stránky** a volbou **Nová** vytvořte novou stránku.</span><span class="sxs-lookup"><span data-stu-id="b9907-137">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="b9907-138">V dialogovém okně **Zvolte šablonu** vyberte šablonu **Šablona marketingu**.</span><span class="sxs-lookup"><span data-stu-id="b9907-138">In the **Choose a template** dialog box, select the **Marketing template** template.</span></span> <span data-ttu-id="b9907-139">V části **Název stránky** zadejte **Stránka marketingu** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="b9907-139">Under **Page name**, enter **Marketing page**, and then select **OK**.</span></span>
1. <span data-ttu-id="b9907-140">V pozici **Hlavní** na nové stránce vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="b9907-140">In the **Main** slot of the new page, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b9907-141">V dialogovém okně **Přidat modul** vyberte modul **Kontejner** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="b9907-141">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b9907-142">V podokně vlastností modulu nastavte hodnotu **Šířka** na **Vyplnit kontejner**.</span><span class="sxs-lookup"><span data-stu-id="b9907-142">In the module's properties pane, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="b9907-143">V pozici **Kontejner** vyberte tři tečky (**...**) a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="b9907-143">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b9907-144">V dialogovém okně **Přidat modul** vyberte modul **iframe** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="b9907-144">In the **Add Module** dialog box, select the **iframe** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b9907-145">V podokně vlastností modulu nastavte hodnotu **Cílová adresa URL** externí adresy URL videa.</span><span class="sxs-lookup"><span data-stu-id="b9907-145">In the module's properties pane, set the **Target URL** value to an external URL for a video.</span></span>
1. <span data-ttu-id="b9907-146">Nastavte další vlastnosti, například **Nadpis** a **Výška**, dle potřeby.</span><span class="sxs-lookup"><span data-stu-id="b9907-146">Set other properties, such as **Heading** and **Height**, as you require.</span></span>
1. <span data-ttu-id="b9907-147">Chcete-li vrátit stránku se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="b9907-147">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="b9907-148">Přejděte na marketingovou stránku svého webu.</span><span class="sxs-lookup"><span data-stu-id="b9907-148">Go to the marketing page on your site.</span></span> <span data-ttu-id="b9907-149">Měli byste vidět, že video je vykresleno v modulu iframe.</span><span class="sxs-lookup"><span data-stu-id="b9907-149">You should see that the video is rendered in the iframe module.</span></span>
 
## <a name="additional-resources"></a><span data-ttu-id="b9907-150">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="b9907-150">Additional resources</span></span>

[<span data-ttu-id="b9907-151">Přehled knihovny modulů</span><span class="sxs-lookup"><span data-stu-id="b9907-151">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="b9907-152">Správa zásad zabezpečení obsahu (CSP)</span><span class="sxs-lookup"><span data-stu-id="b9907-152">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]