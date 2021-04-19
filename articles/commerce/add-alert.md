---
title: Modul propagačního banneru
description: Tohle téma se zabývá moduly propagačního banneru a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: be3cc9729b58fce9ebc9885d8cb20b63114362a0
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796239"
---
# <a name="promo-banner-module"></a><span data-ttu-id="adad5-103">Modul propagačního banneru</span><span class="sxs-lookup"><span data-stu-id="adad5-103">Promo banner module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="adad5-104">Tohle téma se zabývá moduly propagačního banneru a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="adad5-104">This topic covers promo banner modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="adad5-105">Moduly propagačního banneru slouží k zobrazení vložených informačních zpráv na stránce.</span><span class="sxs-lookup"><span data-stu-id="adad5-105">Promo banner modules are used to show inline informational messages on a page.</span></span> <span data-ttu-id="adad5-106">Lze je použít k zobrazení promoakcí v rámci celého webu, které se zobrazí na všech stránkách webu elektronického obchodu.</span><span class="sxs-lookup"><span data-stu-id="adad5-106">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="adad5-107">Moduly propagačního banneru podporují textové zprávy a odkazy.</span><span class="sxs-lookup"><span data-stu-id="adad5-107">Promo banner modules support a text message and a link.</span></span> <span data-ttu-id="adad5-108">Je-li do modulu propagačního banneru přidáno více zpráv, stane se bannerem rotujících karuselů, které umožňují zákazníkům cyklicky procházet všechny zprávy.</span><span class="sxs-lookup"><span data-stu-id="adad5-108">If multiple messages are added to a promo banner module, it becomes a rotating carousel banner that lets customers cycle through all the messages.</span></span> 

<span data-ttu-id="adad5-109">Moduly propagačního banneru jsou řízeny daty ze systému správy obsahu (CMS) a lze je umístit na libovolnou stránku.</span><span class="sxs-lookup"><span data-stu-id="adad5-109">Promo banner modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a><span data-ttu-id="adad5-110">Příklady použití propagačního banneru v e-Commerce</span><span class="sxs-lookup"><span data-stu-id="adad5-110">Usage examples of promo banners in e-Commerce</span></span>

<span data-ttu-id="adad5-111">Reklamní bannery mohou být použity v záhlaví pracoviště pro zobrazení promoakcí a zpráv na úrovni celého pracoviště, jak je uvedeno v následujících příkladech.</span><span class="sxs-lookup"><span data-stu-id="adad5-111">Promo banners can be used in the site header to show site-wide promotions or messages, as in the following examples.</span></span>

<span data-ttu-id="adad5-112">„Výroční výprodej končí za 10 dnů“</span><span class="sxs-lookup"><span data-stu-id="adad5-112">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="adad5-113">„Ušetřete v předškolním výprodeji.</span><span class="sxs-lookup"><span data-stu-id="adad5-113">"Save big with back to school sale.</span></span> <span data-ttu-id="adad5-114">Pusťte se do nakupování.“</span><span class="sxs-lookup"><span data-stu-id="adad5-114">Shop Now."</span></span>

<span data-ttu-id="adad5-115">„Využijte výproDEJ k Díkuvzdání!“</span><span class="sxs-lookup"><span data-stu-id="adad5-115">"Shop for Thanksgiving SALE!"</span></span> 

<span data-ttu-id="adad5-116">Na následujícím obrázku je znázorněn příklad propagačního banneru.</span><span class="sxs-lookup"><span data-stu-id="adad5-116">The following image shows an example of a promo banner.</span></span>

![Příklad modulu propagačního banneru](./media/ecommerce-Promobanner.PNG)

## <a name="promo-banner-module-properties"></a><span data-ttu-id="adad5-118">Vlastnosti modulu propagačního banneru</span><span class="sxs-lookup"><span data-stu-id="adad5-118">Promo banner module properties</span></span>

| <span data-ttu-id="adad5-119">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="adad5-119">Property name</span></span>             | <span data-ttu-id="adad5-120">Hodnota</span><span class="sxs-lookup"><span data-stu-id="adad5-120">Value</span></span>                              | <span data-ttu-id="adad5-121">popis</span><span class="sxs-lookup"><span data-stu-id="adad5-121">Description</span></span> |
|---------------------------|------------------------------------|-------------|
| <span data-ttu-id="adad5-122">Bannerové zprávy</span><span class="sxs-lookup"><span data-stu-id="adad5-122">Banner messages</span></span>           | <span data-ttu-id="adad5-123">Text a odkazy</span><span class="sxs-lookup"><span data-stu-id="adad5-123">Text and links</span></span>                     | <span data-ttu-id="adad5-124">Pole textu a odkazů.</span><span class="sxs-lookup"><span data-stu-id="adad5-124">An array of text and links.</span></span> |
| <span data-ttu-id="adad5-125">Přehrát automaticky</span><span class="sxs-lookup"><span data-stu-id="adad5-125">Autoplay</span></span>                  | <span data-ttu-id="adad5-126">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="adad5-126">**True** or **False**</span></span>              | <span data-ttu-id="adad5-127">Hodnota, která určuje, zda jsou zprávy automaticky cyklicky procházeny, pokud je konfigurováno více zpráv.</span><span class="sxs-lookup"><span data-stu-id="adad5-127">A value that indicates whether messages are automatically cycled through, if multiple messages are configured.</span></span> |
| <span data-ttu-id="adad5-128">Interval přechodu snímků</span><span class="sxs-lookup"><span data-stu-id="adad5-128">Slide transition interval</span></span> | <span data-ttu-id="adad5-129">Počet milisekund (MS)</span><span class="sxs-lookup"><span data-stu-id="adad5-129">A number of milliseconds (ms)</span></span>      | <span data-ttu-id="adad5-130">Interval, který se používá pro procházení zpráv.</span><span class="sxs-lookup"><span data-stu-id="adad5-130">The interval that is used to cycle through messages.</span></span> |
| <span data-ttu-id="adad5-131">Povolit zavření</span><span class="sxs-lookup"><span data-stu-id="adad5-131">Allow dismiss</span></span>             | <span data-ttu-id="adad5-132">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="adad5-132">**True** or **False**</span></span>              | <span data-ttu-id="adad5-133">Je-li tato hodnota nastavena na hodnotu **pravda**, zákazníci mohou výstrahu zavřít.</span><span class="sxs-lookup"><span data-stu-id="adad5-133">If the value is set to **True**, customers can dismiss the alert.</span></span> |
| <span data-ttu-id="adad5-134">Zobrazit páku karuselu</span><span class="sxs-lookup"><span data-stu-id="adad5-134">Show carousel flipper</span></span>     | <span data-ttu-id="adad5-135">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="adad5-135">**True** or **False**</span></span>              | <span data-ttu-id="adad5-136">Hodnota, která určuje, zda se mají zobrazit páky karuselu, aby zákazníci mohli ručně cyklovat více položek banneru.</span><span class="sxs-lookup"><span data-stu-id="adad5-136">A value that indicates whether the carousel flippers should be shown, so that customers can manually cycle through multiple banner items.</span></span> |
| <span data-ttu-id="adad5-137">Zarovnání textu</span><span class="sxs-lookup"><span data-stu-id="adad5-137">Text alignment</span></span>            | <span data-ttu-id="adad5-138">**Vpravo**, **vlevo** nebo **uprostřed**</span><span class="sxs-lookup"><span data-stu-id="adad5-138">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="adad5-139">Zarovnání textu v modulu propagačního banneru.</span><span class="sxs-lookup"><span data-stu-id="adad5-139">The text alignment in the promo banner module.</span></span> |
| <span data-ttu-id="adad5-140">Připojení</span><span class="sxs-lookup"><span data-stu-id="adad5-140">Link</span></span>                      | <span data-ttu-id="adad5-141">Adresa URL</span><span class="sxs-lookup"><span data-stu-id="adad5-141">A URL</span></span>                              | <span data-ttu-id="adad5-142">Adresa URL pro volitelný odkaz.</span><span class="sxs-lookup"><span data-stu-id="adad5-142">The URL for an optional link.</span></span> |

## <a name="add-a-promo-banner-module-to-a-page"></a><span data-ttu-id="adad5-143">Přidání modulu propagačního banneru na novou stránku</span><span class="sxs-lookup"><span data-stu-id="adad5-143">Add a promo banner module to a page</span></span> 

<span data-ttu-id="adad5-144">Chcete-li přidat modul propagačního banneru na stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="adad5-144">To add a promo banner module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="adad5-145">Přejděte na **Šablony** a poté volbou **Nová** vytvořte novou šablonu.</span><span class="sxs-lookup"><span data-stu-id="adad5-145">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="adad5-146">V dialogovém okně **Nová šablona** v části **Název šablony** zadejte **Šablona propagačního banneru** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="adad5-146">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="adad5-147">V části **Osnova stránky** přidejte modul **Výchozí stránka** do pozice **Hlavní část**.</span><span class="sxs-lookup"><span data-stu-id="adad5-147">Under **Page Outline**, add a **Default page** module to the **Body** slot.</span></span> 
1. <span data-ttu-id="adad5-148">Chcete-li vrátit šablonu se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="adad5-148">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 
1. <span data-ttu-id="adad5-149">Šablonu, kterou jste právě vytvořili, použijte pro vytvoření stránky s názvem **Stránka propagačního banneru**.</span><span class="sxs-lookup"><span data-stu-id="adad5-149">Use the template that you just created to create a page that is named **Promo banner page**.</span></span> 
1. <span data-ttu-id="adad5-150">V úseku **Hlavní** nové stránky přidejte modul kontejneru.</span><span class="sxs-lookup"><span data-stu-id="adad5-150">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="adad5-151">V podokně napravo nastavte hodnotu **šířka** na **Vyplnit kontejner**.</span><span class="sxs-lookup"><span data-stu-id="adad5-151">In the pane on the right, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="adad5-152">V části **Osnova stránky** stránky přidejte do modulu kontejneru modul propgačního banneru.</span><span class="sxs-lookup"><span data-stu-id="adad5-152">Under **Page Outline**, add a promo banner module to the container module.</span></span>
1. <span data-ttu-id="adad5-153">V nastavení pro modul propgačního banneru přidejte jednu nebo více zpráv banneru.</span><span class="sxs-lookup"><span data-stu-id="adad5-153">In the settings for the banner module, add one or more banner messages.</span></span> <span data-ttu-id="adad5-154">Každá zpráva může obsahovat text spolu s odkazem.</span><span class="sxs-lookup"><span data-stu-id="adad5-154">Each message can have text together with a link.</span></span> <span data-ttu-id="adad5-155">Chcete-li dále upravit modul propgačního banneru, můžete upravit ostatní vlastnosti.</span><span class="sxs-lookup"><span data-stu-id="adad5-155">You can edit the other properties to customize the module further.</span></span>
1. <span data-ttu-id="adad5-156">Vyberte možnost **Uložit** a poté vyberte možnost **Náhled**, chcete-li zobrazit náhled stránky.</span><span class="sxs-lookup"><span data-stu-id="adad5-156">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="adad5-157">V horní části stránky by se měla zobrazit výstraha zobrazující text, který jste přidali.</span><span class="sxs-lookup"><span data-stu-id="adad5-157">At the top of the page, you should see an alert that shows the text that you added.</span></span>
1. <span data-ttu-id="adad5-158">Chcete-li vrátit stránku se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="adad5-158">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="adad5-159">Propagační banner se obvykle používá v patici záhlaví stránky nebo v pozici dílčího hlavního záhlaví.</span><span class="sxs-lookup"><span data-stu-id="adad5-159">A promo banner is typically used in the page header slot or a subheader slot.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="adad5-160">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="adad5-160">Additional resources</span></span>

[<span data-ttu-id="adad5-161">Přehled knihovny modulů</span><span class="sxs-lookup"><span data-stu-id="adad5-161">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="adad5-162">Karuselový modul</span><span class="sxs-lookup"><span data-stu-id="adad5-162">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="adad5-163">Modul textového bloku</span><span class="sxs-lookup"><span data-stu-id="adad5-163">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="adad5-164">Modul bloku obsahu</span><span class="sxs-lookup"><span data-stu-id="adad5-164">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="adad5-165">Modul videopřehrávače</span><span class="sxs-lookup"><span data-stu-id="adad5-165">Video player module</span></span>](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]