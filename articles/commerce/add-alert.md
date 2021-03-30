---
title: Modul propagačního banneru
description: Tohle téma se zabývá moduly propagačního banneru a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
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
ms.openlocfilehash: 0b9325ef31fc61d451584930b09c2039156c0c05
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206576"
---
# <a name="promo-banner-module"></a><span data-ttu-id="82b89-103">Modul propagačního banneru</span><span class="sxs-lookup"><span data-stu-id="82b89-103">Promo banner module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="82b89-104">Tohle téma se zabývá moduly propagačního banneru a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="82b89-104">This topic covers promo banner modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="82b89-105">Moduly propagačního banneru slouží k zobrazení vložených informačních zpráv na stránce.</span><span class="sxs-lookup"><span data-stu-id="82b89-105">Promo banner modules are used to show inline informational messages on a page.</span></span> <span data-ttu-id="82b89-106">Lze je použít k zobrazení promoakcí v rámci celého webu, které se zobrazí na všech stránkách webu elektronického obchodu.</span><span class="sxs-lookup"><span data-stu-id="82b89-106">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="82b89-107">Moduly propagačního banneru podporují textové zprávy a odkazy.</span><span class="sxs-lookup"><span data-stu-id="82b89-107">Promo banner modules support a text message and a link.</span></span> <span data-ttu-id="82b89-108">Je-li do modulu propagačního banneru přidáno více zpráv, stane se bannerem rotujících karuselů, které umožňují zákazníkům cyklicky procházet všechny zprávy.</span><span class="sxs-lookup"><span data-stu-id="82b89-108">If multiple messages are added to a promo banner module, it becomes a rotating carousel banner that lets customers cycle through all the messages.</span></span> 

<span data-ttu-id="82b89-109">Moduly propagačního banneru jsou řízeny daty ze systému správy obsahu (CMS) a lze je umístit na libovolnou stránku.</span><span class="sxs-lookup"><span data-stu-id="82b89-109">Promo banner modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a><span data-ttu-id="82b89-110">Příklady použití propagačního banneru v e-Commerce</span><span class="sxs-lookup"><span data-stu-id="82b89-110">Usage examples of promo banners in e-Commerce</span></span>

<span data-ttu-id="82b89-111">Reklamní bannery mohou být použity v záhlaví pracoviště pro zobrazení promoakcí a zpráv na úrovni celého pracoviště, jak je uvedeno v následujících příkladech.</span><span class="sxs-lookup"><span data-stu-id="82b89-111">Promo banners can be used in the site header to show site-wide promotions or messages, as in the following examples.</span></span>

<span data-ttu-id="82b89-112">„Výroční výprodej končí za 10 dnů“</span><span class="sxs-lookup"><span data-stu-id="82b89-112">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="82b89-113">„Ušetřete v předškolním výprodeji.</span><span class="sxs-lookup"><span data-stu-id="82b89-113">"Save big with back to school sale.</span></span> <span data-ttu-id="82b89-114">Pusťte se do nakupování.“</span><span class="sxs-lookup"><span data-stu-id="82b89-114">Shop Now."</span></span>

<span data-ttu-id="82b89-115">„Využijte výproDEJ k Díkuvzdání!“</span><span class="sxs-lookup"><span data-stu-id="82b89-115">"Shop for Thanksgiving SALE!"</span></span> 

<span data-ttu-id="82b89-116">Na následujícím obrázku je znázorněn příklad propagačního banneru.</span><span class="sxs-lookup"><span data-stu-id="82b89-116">The following image shows an example of a promo banner.</span></span>

![Příklad modulu propagačního banneru](./media/ecommerce-Promobanner.PNG)

## <a name="promo-banner-module-properties"></a><span data-ttu-id="82b89-118">Vlastnosti modulu propagačního banneru</span><span class="sxs-lookup"><span data-stu-id="82b89-118">Promo banner module properties</span></span>

| <span data-ttu-id="82b89-119">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="82b89-119">Property name</span></span>             | <span data-ttu-id="82b89-120">Hodnota</span><span class="sxs-lookup"><span data-stu-id="82b89-120">Value</span></span>                              | <span data-ttu-id="82b89-121">popis</span><span class="sxs-lookup"><span data-stu-id="82b89-121">Description</span></span> |
|---------------------------|------------------------------------|-------------|
| <span data-ttu-id="82b89-122">Bannerové zprávy</span><span class="sxs-lookup"><span data-stu-id="82b89-122">Banner messages</span></span>           | <span data-ttu-id="82b89-123">Text a odkazy</span><span class="sxs-lookup"><span data-stu-id="82b89-123">Text and links</span></span>                     | <span data-ttu-id="82b89-124">Pole textu a odkazů.</span><span class="sxs-lookup"><span data-stu-id="82b89-124">An array of text and links.</span></span> |
| <span data-ttu-id="82b89-125">Přehrát automaticky</span><span class="sxs-lookup"><span data-stu-id="82b89-125">Autoplay</span></span>                  | <span data-ttu-id="82b89-126">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="82b89-126">**True** or **False**</span></span>              | <span data-ttu-id="82b89-127">Hodnota, která určuje, zda jsou zprávy automaticky cyklicky procházeny, pokud je konfigurováno více zpráv.</span><span class="sxs-lookup"><span data-stu-id="82b89-127">A value that indicates whether messages are automatically cycled through, if multiple messages are configured.</span></span> |
| <span data-ttu-id="82b89-128">Interval přechodu snímků</span><span class="sxs-lookup"><span data-stu-id="82b89-128">Slide transition interval</span></span> | <span data-ttu-id="82b89-129">Počet milisekund (MS)</span><span class="sxs-lookup"><span data-stu-id="82b89-129">A number of milliseconds (ms)</span></span>      | <span data-ttu-id="82b89-130">Interval, který se používá pro procházení zpráv.</span><span class="sxs-lookup"><span data-stu-id="82b89-130">The interval that is used to cycle through messages.</span></span> |
| <span data-ttu-id="82b89-131">Povolit zavření</span><span class="sxs-lookup"><span data-stu-id="82b89-131">Allow dismiss</span></span>             | <span data-ttu-id="82b89-132">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="82b89-132">**True** or **False**</span></span>              | <span data-ttu-id="82b89-133">Je-li tato hodnota nastavena na hodnotu **pravda**, zákazníci mohou výstrahu zavřít.</span><span class="sxs-lookup"><span data-stu-id="82b89-133">If the value is set to **True**, customers can dismiss the alert.</span></span> |
| <span data-ttu-id="82b89-134">Zobrazit páku karuselu</span><span class="sxs-lookup"><span data-stu-id="82b89-134">Show carousel flipper</span></span>     | <span data-ttu-id="82b89-135">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="82b89-135">**True** or **False**</span></span>              | <span data-ttu-id="82b89-136">Hodnota, která určuje, zda se mají zobrazit páky karuselu, aby zákazníci mohli ručně cyklovat více položek banneru.</span><span class="sxs-lookup"><span data-stu-id="82b89-136">A value that indicates whether the carousel flippers should be shown, so that customers can manually cycle through multiple banner items.</span></span> |
| <span data-ttu-id="82b89-137">Zarovnání textu</span><span class="sxs-lookup"><span data-stu-id="82b89-137">Text alignment</span></span>            | <span data-ttu-id="82b89-138">**Vpravo**, **vlevo** nebo **uprostřed**</span><span class="sxs-lookup"><span data-stu-id="82b89-138">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="82b89-139">Zarovnání textu v modulu propagačního banneru.</span><span class="sxs-lookup"><span data-stu-id="82b89-139">The text alignment in the promo banner module.</span></span> |
| <span data-ttu-id="82b89-140">Připojení</span><span class="sxs-lookup"><span data-stu-id="82b89-140">Link</span></span>                      | <span data-ttu-id="82b89-141">Adresa URL</span><span class="sxs-lookup"><span data-stu-id="82b89-141">A URL</span></span>                              | <span data-ttu-id="82b89-142">Adresa URL pro volitelný odkaz.</span><span class="sxs-lookup"><span data-stu-id="82b89-142">The URL for an optional link.</span></span> |

## <a name="add-a-promo-banner-module-to-a-page"></a><span data-ttu-id="82b89-143">Přidání modulu propagačního banneru na novou stránku</span><span class="sxs-lookup"><span data-stu-id="82b89-143">Add a promo banner module to a page</span></span> 

<span data-ttu-id="82b89-144">Chcete-li přidat modul propagačního banneru na stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="82b89-144">To add a promo banner module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="82b89-145">Přejděte na **Šablony** a poté volbou **Nová** vytvořte novou šablonu.</span><span class="sxs-lookup"><span data-stu-id="82b89-145">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="82b89-146">V dialogovém okně **Nová šablona** v části **Název šablony** zadejte **Šablona propagačního banneru** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="82b89-146">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="82b89-147">V části **Osnova stránky** přidejte modul **Výchozí stránka** do pozice **Hlavní část**.</span><span class="sxs-lookup"><span data-stu-id="82b89-147">Under **Page Outline**, add a **Default page** module to the **Body** slot.</span></span> 
1. <span data-ttu-id="82b89-148">Chcete-li vrátit šablonu se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="82b89-148">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 
1. <span data-ttu-id="82b89-149">Šablonu, kterou jste právě vytvořili, použijte pro vytvoření stránky s názvem **Stránka propagačního banneru**.</span><span class="sxs-lookup"><span data-stu-id="82b89-149">Use the template that you just created to create a page that is named **Promo banner page**.</span></span> 
1. <span data-ttu-id="82b89-150">V úseku **Hlavní** nové stránky přidejte modul kontejneru.</span><span class="sxs-lookup"><span data-stu-id="82b89-150">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="82b89-151">V podokně napravo nastavte hodnotu **šířka** na **Vyplnit kontejner**.</span><span class="sxs-lookup"><span data-stu-id="82b89-151">In the pane on the right, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="82b89-152">V části **Osnova stránky** stránky přidejte do modulu kontejneru modul propgačního banneru.</span><span class="sxs-lookup"><span data-stu-id="82b89-152">Under **Page Outline**, add a promo banner module to the container module.</span></span>
1. <span data-ttu-id="82b89-153">V nastavení pro modul propgačního banneru přidejte jednu nebo více zpráv banneru.</span><span class="sxs-lookup"><span data-stu-id="82b89-153">In the settings for the banner module, add one or more banner messages.</span></span> <span data-ttu-id="82b89-154">Každá zpráva může obsahovat text spolu s odkazem.</span><span class="sxs-lookup"><span data-stu-id="82b89-154">Each message can have text together with a link.</span></span> <span data-ttu-id="82b89-155">Chcete-li dále upravit modul propgačního banneru, můžete upravit ostatní vlastnosti.</span><span class="sxs-lookup"><span data-stu-id="82b89-155">You can edit the other properties to customize the module further.</span></span>
1. <span data-ttu-id="82b89-156">Vyberte možnost **Uložit** a poté vyberte možnost **Náhled**, chcete-li zobrazit náhled stránky.</span><span class="sxs-lookup"><span data-stu-id="82b89-156">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="82b89-157">V horní části stránky by se měla zobrazit výstraha zobrazující text, který jste přidali.</span><span class="sxs-lookup"><span data-stu-id="82b89-157">At the top of the page, you should see an alert that shows the text that you added.</span></span>
1. <span data-ttu-id="82b89-158">Chcete-li vrátit stránku se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="82b89-158">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="82b89-159">Propagační banner se obvykle používá v patici záhlaví stránky nebo v pozici dílčího hlavního záhlaví.</span><span class="sxs-lookup"><span data-stu-id="82b89-159">A promo banner is typically used in the page header slot or a subheader slot.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="82b89-160">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="82b89-160">Additional resources</span></span>

[<span data-ttu-id="82b89-161">Přehled knihovny modulů</span><span class="sxs-lookup"><span data-stu-id="82b89-161">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="82b89-162">Karuselový modul</span><span class="sxs-lookup"><span data-stu-id="82b89-162">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="82b89-163">Modul textového bloku</span><span class="sxs-lookup"><span data-stu-id="82b89-163">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="82b89-164">Modul bloku obsahu</span><span class="sxs-lookup"><span data-stu-id="82b89-164">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="82b89-165">Modul videopřehrávače</span><span class="sxs-lookup"><span data-stu-id="82b89-165">Video player module</span></span>](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]