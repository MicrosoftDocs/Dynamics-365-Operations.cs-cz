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
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: d9debd16b18300d090bde1862a16920d8e9185eb
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817247"
---
# <a name="promo-banner-module"></a><span data-ttu-id="ec83a-103">Modul propagačního banneru</span><span class="sxs-lookup"><span data-stu-id="ec83a-103">Promo banner module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ec83a-104">Tohle téma se zabývá moduly propagačního banneru a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ec83a-104">This topic covers promo banner modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ec83a-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="ec83a-105">Overview</span></span>

<span data-ttu-id="ec83a-106">Moduly propagačního banneru slouží k zobrazení vložených informačních zpráv na stránce.</span><span class="sxs-lookup"><span data-stu-id="ec83a-106">Promo banner modules are used to show inline informational messages on a page.</span></span> <span data-ttu-id="ec83a-107">Lze je použít k zobrazení promoakcí v rámci celého webu, které se zobrazí na všech stránkách webu elektronického obchodu.</span><span class="sxs-lookup"><span data-stu-id="ec83a-107">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="ec83a-108">Moduly propagačního banneru podporují textové zprávy a odkazy.</span><span class="sxs-lookup"><span data-stu-id="ec83a-108">Promo banner modules support a text message and a link.</span></span> <span data-ttu-id="ec83a-109">Je-li do modulu propagačního banneru přidáno více zpráv, stane se bannerem rotujících karuselů, které umožňují zákazníkům cyklicky procházet všechny zprávy.</span><span class="sxs-lookup"><span data-stu-id="ec83a-109">If multiple messages are added to a promo banner module, it becomes a rotating carousel banner that lets customers cycle through all the messages.</span></span> 

<span data-ttu-id="ec83a-110">Moduly propagačního banneru jsou řízeny daty ze systému správy obsahu (CMS) a lze je umístit na libovolnou stránku.</span><span class="sxs-lookup"><span data-stu-id="ec83a-110">Promo banner modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a><span data-ttu-id="ec83a-111">Příklady použití propagačního banneru v e-Commerce</span><span class="sxs-lookup"><span data-stu-id="ec83a-111">Usage examples of promo banners in e-Commerce</span></span>

<span data-ttu-id="ec83a-112">Reklamní bannery mohou být použity v záhlaví pracoviště pro zobrazení promoakcí a zpráv na úrovni celého pracoviště, jak je uvedeno v následujících příkladech.</span><span class="sxs-lookup"><span data-stu-id="ec83a-112">Promo banners can be used in the site header to show site-wide promotions or messages, as in the following examples.</span></span>

<span data-ttu-id="ec83a-113">„Výroční výprodej končí za 10 dnů“</span><span class="sxs-lookup"><span data-stu-id="ec83a-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="ec83a-114">„Ušetřete v předškolním výprodeji.</span><span class="sxs-lookup"><span data-stu-id="ec83a-114">"Save big with back to school sale.</span></span> <span data-ttu-id="ec83a-115">Pusťte se do nakupování.“</span><span class="sxs-lookup"><span data-stu-id="ec83a-115">Shop Now."</span></span>

<span data-ttu-id="ec83a-116">„Využijte výproDEJ k Díkuvzdání!“</span><span class="sxs-lookup"><span data-stu-id="ec83a-116">"Shop for Thanksgiving SALE!"</span></span> 

<span data-ttu-id="ec83a-117">Na následujícím obrázku je znázorněn příklad propagačního banneru.</span><span class="sxs-lookup"><span data-stu-id="ec83a-117">The following image shows an example of a promo banner.</span></span>

![Příklad modulu propagačního banneru](./media/ecommerce-Promobanner.PNG)

## <a name="promo-banner-module-properties"></a><span data-ttu-id="ec83a-119">Vlastnosti modulu propagačního banneru</span><span class="sxs-lookup"><span data-stu-id="ec83a-119">Promo banner module properties</span></span>

| <span data-ttu-id="ec83a-120">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="ec83a-120">Property name</span></span>             | <span data-ttu-id="ec83a-121">Hodnota</span><span class="sxs-lookup"><span data-stu-id="ec83a-121">Value</span></span>                              | <span data-ttu-id="ec83a-122">popis</span><span class="sxs-lookup"><span data-stu-id="ec83a-122">Description</span></span> |
|---------------------------|------------------------------------|-------------|
| <span data-ttu-id="ec83a-123">Bannerové zprávy</span><span class="sxs-lookup"><span data-stu-id="ec83a-123">Banner messages</span></span>           | <span data-ttu-id="ec83a-124">Text a odkazy</span><span class="sxs-lookup"><span data-stu-id="ec83a-124">Text and links</span></span>                     | <span data-ttu-id="ec83a-125">Pole textu a odkazů.</span><span class="sxs-lookup"><span data-stu-id="ec83a-125">An array of text and links.</span></span> |
| <span data-ttu-id="ec83a-126">Přehrát automaticky</span><span class="sxs-lookup"><span data-stu-id="ec83a-126">Autoplay</span></span>                  | <span data-ttu-id="ec83a-127">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="ec83a-127">**True** or **False**</span></span>              | <span data-ttu-id="ec83a-128">Hodnota, která určuje, zda jsou zprávy automaticky cyklicky procházeny, pokud je konfigurováno více zpráv.</span><span class="sxs-lookup"><span data-stu-id="ec83a-128">A value that indicates whether messages are automatically cycled through, if multiple messages are configured.</span></span> |
| <span data-ttu-id="ec83a-129">Interval přechodu snímků</span><span class="sxs-lookup"><span data-stu-id="ec83a-129">Slide transition interval</span></span> | <span data-ttu-id="ec83a-130">Počet milisekund (MS)</span><span class="sxs-lookup"><span data-stu-id="ec83a-130">A number of milliseconds (ms)</span></span>      | <span data-ttu-id="ec83a-131">Interval, který se používá pro procházení zpráv.</span><span class="sxs-lookup"><span data-stu-id="ec83a-131">The interval that is used to cycle through messages.</span></span> |
| <span data-ttu-id="ec83a-132">Povolit zavření</span><span class="sxs-lookup"><span data-stu-id="ec83a-132">Allow dismiss</span></span>             | <span data-ttu-id="ec83a-133">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="ec83a-133">**True** or **False**</span></span>              | <span data-ttu-id="ec83a-134">Je-li tato hodnota nastavena na hodnotu **pravda**, zákazníci mohou výstrahu zavřít.</span><span class="sxs-lookup"><span data-stu-id="ec83a-134">If the value is set to **True**, customers can dismiss the alert.</span></span> |
| <span data-ttu-id="ec83a-135">Zobrazit páku karuselu</span><span class="sxs-lookup"><span data-stu-id="ec83a-135">Show carousel flipper</span></span>     | <span data-ttu-id="ec83a-136">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="ec83a-136">**True** or **False**</span></span>              | <span data-ttu-id="ec83a-137">Hodnota, která určuje, zda se mají zobrazit páky karuselu, aby zákazníci mohli ručně cyklovat více položek banneru.</span><span class="sxs-lookup"><span data-stu-id="ec83a-137">A value that indicates whether the carousel flippers should be shown, so that customers can manually cycle through multiple banner items.</span></span> |
| <span data-ttu-id="ec83a-138">Zarovnání textu</span><span class="sxs-lookup"><span data-stu-id="ec83a-138">Text alignment</span></span>            | <span data-ttu-id="ec83a-139">**Vpravo**, **vlevo** nebo **uprostřed**</span><span class="sxs-lookup"><span data-stu-id="ec83a-139">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="ec83a-140">Zarovnání textu v modulu propagačního banneru.</span><span class="sxs-lookup"><span data-stu-id="ec83a-140">The text alignment in the promo banner module.</span></span> |
| <span data-ttu-id="ec83a-141">Připojení</span><span class="sxs-lookup"><span data-stu-id="ec83a-141">Link</span></span>                      | <span data-ttu-id="ec83a-142">Adresa URL</span><span class="sxs-lookup"><span data-stu-id="ec83a-142">A URL</span></span>                              | <span data-ttu-id="ec83a-143">Adresa URL pro volitelný odkaz.</span><span class="sxs-lookup"><span data-stu-id="ec83a-143">The URL for an optional link.</span></span> |

## <a name="add-a-promo-banner-module-to-a-page"></a><span data-ttu-id="ec83a-144">Přidání modulu propagačního banneru na novou stránku</span><span class="sxs-lookup"><span data-stu-id="ec83a-144">Add a promo banner module to a page</span></span> 

<span data-ttu-id="ec83a-145">Chcete-li přidat modul propagačního banneru na stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="ec83a-145">To add a promo banner module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="ec83a-146">Přejděte na **Šablony** a poté volbou **Nová** vytvořte novou šablonu.</span><span class="sxs-lookup"><span data-stu-id="ec83a-146">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="ec83a-147">V dialogovém okně **Nová šablona** v části **Název šablony** zadejte **Šablona propagačního banneru** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="ec83a-147">In the **New Template** dialog box, under **Template Name**, enter **Promo banner template**, and then select **OK**.</span></span>
1. <span data-ttu-id="ec83a-148">V části **Osnova stránky** přidejte modul **Výchozí stránka** do pozice **Hlavní část**.</span><span class="sxs-lookup"><span data-stu-id="ec83a-148">Under **Page Outline**, add a **Default page** module to the **Body** slot.</span></span> 
1. <span data-ttu-id="ec83a-149">Chcete-li vrátit šablonu se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="ec83a-149">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 
1. <span data-ttu-id="ec83a-150">Šablonu, kterou jste právě vytvořili, použijte pro vytvoření stránky s názvem **Stránka propagačního banneru**.</span><span class="sxs-lookup"><span data-stu-id="ec83a-150">Use the template that you just created to create a page that is named **Promo banner page**.</span></span> 
1. <span data-ttu-id="ec83a-151">V úseku **Hlavní** nové stránky přidejte modul kontejneru.</span><span class="sxs-lookup"><span data-stu-id="ec83a-151">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="ec83a-152">V podokně napravo nastavte hodnotu **šířka** na **Vyplnit kontejner**.</span><span class="sxs-lookup"><span data-stu-id="ec83a-152">In the pane on the right, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="ec83a-153">V části **Osnova stránky** stránky přidejte do modulu kontejneru modul propgačního banneru.</span><span class="sxs-lookup"><span data-stu-id="ec83a-153">Under **Page Outline**, add a promo banner module to the container module.</span></span>
1. <span data-ttu-id="ec83a-154">V nastavení pro modul propgačního banneru přidejte jednu nebo více zpráv banneru.</span><span class="sxs-lookup"><span data-stu-id="ec83a-154">In the settings for the banner module, add one or more banner messages.</span></span> <span data-ttu-id="ec83a-155">Každá zpráva může obsahovat text spolu s odkazem.</span><span class="sxs-lookup"><span data-stu-id="ec83a-155">Each message can have text together with a link.</span></span> <span data-ttu-id="ec83a-156">Chcete-li dále upravit modul propgačního banneru, můžete upravit ostatní vlastnosti.</span><span class="sxs-lookup"><span data-stu-id="ec83a-156">You can edit the other properties to customize the module further.</span></span>
1. <span data-ttu-id="ec83a-157">Vyberte možnost **Uložit** a poté vyberte možnost **Náhled**, chcete-li zobrazit náhled stránky.</span><span class="sxs-lookup"><span data-stu-id="ec83a-157">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="ec83a-158">V horní části stránky by se měla zobrazit výstraha zobrazující text, který jste přidali.</span><span class="sxs-lookup"><span data-stu-id="ec83a-158">At the top of the page, you should see an alert that shows the text that you added.</span></span>
1. <span data-ttu-id="ec83a-159">Chcete-li vrátit stránku se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="ec83a-159">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="ec83a-160">Propagační banner se obvykle používá v patici záhlaví stránky nebo v pozici dílčího hlavního záhlaví.</span><span class="sxs-lookup"><span data-stu-id="ec83a-160">A promo banner is typically used in the page header slot or a subheader slot.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="ec83a-161">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="ec83a-161">Additional resources</span></span>

[<span data-ttu-id="ec83a-162">Přehled knihovny modulů</span><span class="sxs-lookup"><span data-stu-id="ec83a-162">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="ec83a-163">Karuselový modul</span><span class="sxs-lookup"><span data-stu-id="ec83a-163">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="ec83a-164">Modul textového bloku</span><span class="sxs-lookup"><span data-stu-id="ec83a-164">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="ec83a-165">Modul bloku obsahu</span><span class="sxs-lookup"><span data-stu-id="ec83a-165">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="ec83a-166">Modul videopřehrávače</span><span class="sxs-lookup"><span data-stu-id="ec83a-166">Video player module</span></span>](add-video-player.md)
