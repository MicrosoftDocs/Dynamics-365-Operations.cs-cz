---
title: Modul propagačního banneru
description: Tohle téma se zabývá moduly propagačního banneru a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: da5e220e4578d1064eb7b627b441d3f585b3c095
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025613"
---
# <a name="promo-banner-module"></a><span data-ttu-id="775dc-103">Modul propagačního banneru</span><span class="sxs-lookup"><span data-stu-id="775dc-103">Promo banner module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="775dc-104">Tohle téma se zabývá moduly propagačního banneru a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="775dc-104">This topic covers promo banner modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="775dc-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="775dc-105">Overview</span></span>

<span data-ttu-id="775dc-106">Moduly propagačního banneru slouží k zobrazení vložených informačních zpráv na stránce.</span><span class="sxs-lookup"><span data-stu-id="775dc-106">Promo banner modules are used to show inline informational messages on a page.</span></span> <span data-ttu-id="775dc-107">Lze je použít k zobrazení promoakcí v rámci celého webu, které se zobrazí na všech stránkách webu elektronického obchodu.</span><span class="sxs-lookup"><span data-stu-id="775dc-107">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="775dc-108">Moduly propagačního banneru podporují textové zprávy a odkazy.</span><span class="sxs-lookup"><span data-stu-id="775dc-108">Promo banner modules support a text message and a link.</span></span> <span data-ttu-id="775dc-109">Je-li do modulu propagačního banneru přidáno více zpráv, stane se bannerem rotujících karuselů, které umožňují zákazníkům cyklicky procházet všechny zprávy.</span><span class="sxs-lookup"><span data-stu-id="775dc-109">If multiple messages are added to a promo banner module, it becomes a rotating carousel banner that lets customers cycle through all the messages.</span></span> 

<span data-ttu-id="775dc-110">Moduly propagačního banneru jsou řízeny daty ze systému správy obsahu (CMS) a lze je umístit na libovolnou stránku.</span><span class="sxs-lookup"><span data-stu-id="775dc-110">Promo banner modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="usage-examples-of-promo-banners-in-e-commerce"></a><span data-ttu-id="775dc-111">Příklady použití propagačního banneru v e-Commerce</span><span class="sxs-lookup"><span data-stu-id="775dc-111">Usage examples of promo banners in e-Commerce</span></span>

<span data-ttu-id="775dc-112">Reklamní bannery mohou být použity v záhlaví pracoviště pro zobrazení promoakcí a zpráv na úrovni celého pracoviště, jak je uvedeno v následujících příkladech.</span><span class="sxs-lookup"><span data-stu-id="775dc-112">Promo banners can be used in the site header to show site-wide promotions or messages, as in the following examples.</span></span>

<span data-ttu-id="775dc-113">„Výroční výprodej končí za 10 dnů“</span><span class="sxs-lookup"><span data-stu-id="775dc-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="775dc-114">„Ušetřete v předškolním výprodeji.</span><span class="sxs-lookup"><span data-stu-id="775dc-114">"Save big with back to school sale.</span></span> <span data-ttu-id="775dc-115">Pusťte se do nakupování.“</span><span class="sxs-lookup"><span data-stu-id="775dc-115">Shop Now."</span></span>

## <a name="promo-banner-module-properties"></a><span data-ttu-id="775dc-116">Vlastnosti modulu propagačního banneru</span><span class="sxs-lookup"><span data-stu-id="775dc-116">Promo banner module properties</span></span>

| <span data-ttu-id="775dc-117">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="775dc-117">Property name</span></span>             | <span data-ttu-id="775dc-118">Value</span><span class="sxs-lookup"><span data-stu-id="775dc-118">Value</span></span>                              | <span data-ttu-id="775dc-119">Popis</span><span class="sxs-lookup"><span data-stu-id="775dc-119">Description</span></span> |
|---------------------------|------------------------------------|-------------|
| <span data-ttu-id="775dc-120">Bannerové zprávy</span><span class="sxs-lookup"><span data-stu-id="775dc-120">Banner messages</span></span>           | <span data-ttu-id="775dc-121">Text a odkazy</span><span class="sxs-lookup"><span data-stu-id="775dc-121">Text and links</span></span>                     | <span data-ttu-id="775dc-122">Pole textu a odkazů.</span><span class="sxs-lookup"><span data-stu-id="775dc-122">An array of text and links.</span></span> |
| <span data-ttu-id="775dc-123">Přehrát automaticky</span><span class="sxs-lookup"><span data-stu-id="775dc-123">Autoplay</span></span>                  | <span data-ttu-id="775dc-124">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="775dc-124">**True** or **False**</span></span>              | <span data-ttu-id="775dc-125">Hodnota, která určuje, zda jsou zprávy automaticky cyklicky procházeny, pokud je konfigurováno více zpráv.</span><span class="sxs-lookup"><span data-stu-id="775dc-125">A value that indicates whether messages are automatically cycled through, if multiple messages are configured.</span></span> |
| <span data-ttu-id="775dc-126">Interval přechodu snímků</span><span class="sxs-lookup"><span data-stu-id="775dc-126">Slide transition interval</span></span> | <span data-ttu-id="775dc-127">Počet milisekund (MS)</span><span class="sxs-lookup"><span data-stu-id="775dc-127">A number of milliseconds (ms)</span></span>      | <span data-ttu-id="775dc-128">Interval, který se používá pro procházení zpráv.</span><span class="sxs-lookup"><span data-stu-id="775dc-128">The interval that is used to cycle through messages.</span></span> |
| <span data-ttu-id="775dc-129">Povolit zavření</span><span class="sxs-lookup"><span data-stu-id="775dc-129">Allow dismiss</span></span>             | <span data-ttu-id="775dc-130">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="775dc-130">**True** or **False**</span></span>              | <span data-ttu-id="775dc-131">Je-li tato hodnota nastavena na hodnotu **pravda**, zákazníci mohou výstrahu zavřít.</span><span class="sxs-lookup"><span data-stu-id="775dc-131">If the value is set to **True**, customers can dismiss the alert.</span></span> |
| <span data-ttu-id="775dc-132">Zobrazit páku karuselu</span><span class="sxs-lookup"><span data-stu-id="775dc-132">Show carousel flipper</span></span>     | <span data-ttu-id="775dc-133">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="775dc-133">**True** or **False**</span></span>              | <span data-ttu-id="775dc-134">Hodnota, která určuje, zda se mají zobrazit páky karuselu, aby zákazníci mohli ručně cyklovat více položek banneru.</span><span class="sxs-lookup"><span data-stu-id="775dc-134">A value that indicates whether the carousel flippers should be shown, so that customers can manually cycle through multiple banner items.</span></span> |
| <span data-ttu-id="775dc-135">Zarovnání textu</span><span class="sxs-lookup"><span data-stu-id="775dc-135">Text alignment</span></span>            | <span data-ttu-id="775dc-136">**Vpravo**, **vlevo** nebo **uprostřed**</span><span class="sxs-lookup"><span data-stu-id="775dc-136">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="775dc-137">Zarovnání textu v modulu propagačního banneru.</span><span class="sxs-lookup"><span data-stu-id="775dc-137">The text alignment in the promo banner module.</span></span> |
| <span data-ttu-id="775dc-138">Připojení</span><span class="sxs-lookup"><span data-stu-id="775dc-138">Link</span></span>                      | <span data-ttu-id="775dc-139">Adresa URL</span><span class="sxs-lookup"><span data-stu-id="775dc-139">A URL</span></span>                              | <span data-ttu-id="775dc-140">Adresa URL pro volitelný odkaz.</span><span class="sxs-lookup"><span data-stu-id="775dc-140">The URL for an optional link.</span></span> |

## <a name="add-a-promo-banner-module-to-a-page"></a><span data-ttu-id="775dc-141">Přidání modulu propagačního banneru na novou stránku</span><span class="sxs-lookup"><span data-stu-id="775dc-141">Add a promo banner module to a page</span></span> 

<span data-ttu-id="775dc-142">Chcete-li přidat modul propagačního banneru na stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="775dc-142">To add a promo banner module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="775dc-143">Vytvořte šablonu stránky s názvem **Šablona propagačního banneru**.</span><span class="sxs-lookup"><span data-stu-id="775dc-143">Create a page template that is named **Promo banner template**.</span></span>
1. <span data-ttu-id="775dc-144">V části **Osnova stránky** přidejte modul **Výchozí stránka** do slotu **Hlavní část**.</span><span class="sxs-lookup"><span data-stu-id="775dc-144">Under **Page Outline**, add a **Default page** module to the **Body** slot.</span></span> 
1. <span data-ttu-id="775dc-145">Vraťte šablonu se změnami a publikujte ji.</span><span class="sxs-lookup"><span data-stu-id="775dc-145">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="775dc-146">Šablonu, kterou jste právě vytvořili, použijte pro vytvoření stránky s názvem **Stránka propagačního banneru**.</span><span class="sxs-lookup"><span data-stu-id="775dc-146">Use the template that you just created to create a page that is named **Promo banner page**.</span></span> 
1. <span data-ttu-id="775dc-147">V úseku **Hlavní** nové stránky přidejte modul kontejneru.</span><span class="sxs-lookup"><span data-stu-id="775dc-147">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="775dc-148">V podokně napravo nastavte hodnotu **šířka** na **Vyplnit kontejner**.</span><span class="sxs-lookup"><span data-stu-id="775dc-148">In the pane on the right, set the **Width** value to **Fill Container**.</span></span>
1. <span data-ttu-id="775dc-149">V části **Osnova stránky** stránky přidejte do modulu kontejneru modul propgačního banneru.</span><span class="sxs-lookup"><span data-stu-id="775dc-149">Under **Page Outline**, add a promo banner module to the container module.</span></span>
1. <span data-ttu-id="775dc-150">V nastavení pro modul propgačního banneru přidejte jednu nebo více zpráv banneru.</span><span class="sxs-lookup"><span data-stu-id="775dc-150">In the settings for the banner module, add one or more banner messages.</span></span> <span data-ttu-id="775dc-151">Každá zpráva může obsahovat text spolu s odkazem.</span><span class="sxs-lookup"><span data-stu-id="775dc-151">Each message can have text together with a link.</span></span> <span data-ttu-id="775dc-152">Chcete-li dále upravit modul propgačního banneru, můžete upravit ostatní vlastnosti.</span><span class="sxs-lookup"><span data-stu-id="775dc-152">You can edit the other properties to customize the module further.</span></span>
1. <span data-ttu-id="775dc-153">Uložte stránku a zobrazte náhled.</span><span class="sxs-lookup"><span data-stu-id="775dc-153">Save and preview the page.</span></span> <span data-ttu-id="775dc-154">V horní části stránky by se měla zobrazit výstraha zobrazující text, který jste přidali.</span><span class="sxs-lookup"><span data-stu-id="775dc-154">At the top of the page, you should see an alert that shows the text that you added.</span></span>
1. <span data-ttu-id="775dc-155">Dokončete úpravy stránky a publikujte ji.</span><span class="sxs-lookup"><span data-stu-id="775dc-155">Finish editing the page, and publish it.</span></span> 

> [!NOTE]
> <span data-ttu-id="775dc-156">Propagační banner se obvykle používá v patici záhlaví stránky nebo v pozici dílčího hlavního záhlaví.</span><span class="sxs-lookup"><span data-stu-id="775dc-156">A promo banner is typically used in the page header slot or a subheader slot.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="775dc-157">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="775dc-157">Additional resources</span></span>

[<span data-ttu-id="775dc-158">Přehled startovací sady</span><span class="sxs-lookup"><span data-stu-id="775dc-158">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="775dc-159">Karuselový modul</span><span class="sxs-lookup"><span data-stu-id="775dc-159">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="775dc-160">Modul textového bloku</span><span class="sxs-lookup"><span data-stu-id="775dc-160">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="775dc-161">Modul bloku obsahu</span><span class="sxs-lookup"><span data-stu-id="775dc-161">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="775dc-162">Modul videopřehrávače</span><span class="sxs-lookup"><span data-stu-id="775dc-162">Video player module</span></span>](add-video-player.md)
