---
title: Karuselový modul
description: Tohle téma se zabývá karuselovými moduly a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 5333ecd7a1fe4f60684fa5f5bb3ac9f98efde6d7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5206504"
---
# <a name="carousel-module"></a><span data-ttu-id="2c5ea-103">Karuselový modul</span><span class="sxs-lookup"><span data-stu-id="2c5ea-103">Carousel module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2c5ea-104">Tohle téma se zabývá karuselovými moduly a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2c5ea-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="2c5ea-105">Karuselový modul slouží k umístění propagačních položek do rotujícího banneru karuselu (včetně formátovaných obrázků), který mohou zákazníci procházet.</span><span class="sxs-lookup"><span data-stu-id="2c5ea-105">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="2c5ea-106">Maloobchodní prodejce může například pomocí karuselového modulu na domovské stránce prezentovat nové produkty nebo propagační akce.</span><span class="sxs-lookup"><span data-stu-id="2c5ea-106">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="2c5ea-107">Do karuselového modulu můžete přidat modul bloku obsahu.</span><span class="sxs-lookup"><span data-stu-id="2c5ea-107">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="2c5ea-108">Vlastnosti karuselového modulu pak definují způsob, jakým jsou tyto moduly vykreslovány.</span><span class="sxs-lookup"><span data-stu-id="2c5ea-108">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="2c5ea-109">Příklady karuselových modulů v elektronickém obchodu</span><span class="sxs-lookup"><span data-stu-id="2c5ea-109">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="2c5ea-110">Na domovské stránce lze použít karusel s více propagačními moduly.</span><span class="sxs-lookup"><span data-stu-id="2c5ea-110">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="2c5ea-111">Na stránce s podrobnostmi o produktu lze použít karusel s více propagačními moduly.</span><span class="sxs-lookup"><span data-stu-id="2c5ea-111">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="2c5ea-112">Karusel lze použít na libovolné marketingové stránce k propagaci promoakcí a produktů.</span><span class="sxs-lookup"><span data-stu-id="2c5ea-112">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

<span data-ttu-id="2c5ea-113">Následující obrázek ukazuje příklad karuselového modulu použitého na domovské stránce.</span><span class="sxs-lookup"><span data-stu-id="2c5ea-113">The following image shows an example of a carousel module that is used on a home page.</span></span> <span data-ttu-id="2c5ea-114">Tento karuselový model obsahuje několik položek bloku obsahu.</span><span class="sxs-lookup"><span data-stu-id="2c5ea-114">This carousel module contains multiple content block items.</span></span>

![Příklad karuselového modulu](./media/Hero.PNG)

## <a name="carousel-module-properties"></a><span data-ttu-id="2c5ea-116">Vlastnosti karuselového modulu</span><span class="sxs-lookup"><span data-stu-id="2c5ea-116">Carousel module properties</span></span>

| <span data-ttu-id="2c5ea-117">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="2c5ea-117">Property name</span></span>             | <span data-ttu-id="2c5ea-118">Hodnota</span><span class="sxs-lookup"><span data-stu-id="2c5ea-118">Value</span></span>                 | <span data-ttu-id="2c5ea-119">popis</span><span class="sxs-lookup"><span data-stu-id="2c5ea-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="2c5ea-120">Přehrát automaticky</span><span class="sxs-lookup"><span data-stu-id="2c5ea-120">Autoplay</span></span>                  | <span data-ttu-id="2c5ea-121">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="2c5ea-121">**True** or **False**</span></span> | <span data-ttu-id="2c5ea-122">Je- li nastavena hodnota **Pravda**, dojde k automatickému přechodu mezi položkami v karuselu.</span><span class="sxs-lookup"><span data-stu-id="2c5ea-122">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="2c5ea-123">Pokud je hodnota nastavena na **Nepravda**, nedochází k žádnému přechodu, pokud zákazník nepoužije klávesnici nebo myš k přechodu z jedné položky na další položku.</span><span class="sxs-lookup"><span data-stu-id="2c5ea-123">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="2c5ea-124">Interval přechodu snímků</span><span class="sxs-lookup"><span data-stu-id="2c5ea-124">Slide transition interval</span></span> | <span data-ttu-id="2c5ea-125">Hodnota v sekundách</span><span class="sxs-lookup"><span data-stu-id="2c5ea-125">A value in seconds</span></span>    | <span data-ttu-id="2c5ea-126">Interval pro přechody mezi položkami.</span><span class="sxs-lookup"><span data-stu-id="2c5ea-126">The interval for transitions between items.</span></span> |
| <span data-ttu-id="2c5ea-127">Typ přechodu</span><span class="sxs-lookup"><span data-stu-id="2c5ea-127">Transition type</span></span>           | <span data-ttu-id="2c5ea-128">**Posunutí** nebo **Slábnutí**</span><span class="sxs-lookup"><span data-stu-id="2c5ea-128">**Slide** or **Fade**</span></span> | <span data-ttu-id="2c5ea-129">Přechodový efekt mezi položkami.</span><span class="sxs-lookup"><span data-stu-id="2c5ea-129">The transition effect between items.</span></span> |
| <span data-ttu-id="2c5ea-130">Skrýt karuselové překlopení</span><span class="sxs-lookup"><span data-stu-id="2c5ea-130">Hide carousel flipper</span></span>     | <span data-ttu-id="2c5ea-131">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="2c5ea-131">**True** or **False**</span></span> | <span data-ttu-id="2c5ea-132">Je-li nastavena na **true**, bude páka karuselu a indikátor pořadí skrytý.</span><span class="sxs-lookup"><span data-stu-id="2c5ea-132">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="2c5ea-133">Povolit zrušení karuselu</span><span class="sxs-lookup"><span data-stu-id="2c5ea-133">Allow carousel dismiss</span></span>    | <span data-ttu-id="2c5ea-134">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="2c5ea-134">**True** or **False**</span></span> | <span data-ttu-id="2c5ea-135">Je-li tato hodnota nastavena na hodnotu **pravda**, uživatelé mohou karusel zrušit.</span><span class="sxs-lookup"><span data-stu-id="2c5ea-135">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="2c5ea-136">Přidání karuselového modulu na stránku</span><span class="sxs-lookup"><span data-stu-id="2c5ea-136">Add a carousel module to a page</span></span>

<span data-ttu-id="2c5ea-137">Chcete-li přidat karuselový modul na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="2c5ea-137">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="2c5ea-138">Přejděte na **Šablony** a poté volbou **Nová** vytvořte novou šablonu.</span><span class="sxs-lookup"><span data-stu-id="2c5ea-138">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="2c5ea-139">V dialogovém okně **Nová šablona** v části **Název šablony** zadejte **Šablona karuselu** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="2c5ea-139">In the **New Template** dialog box, under **Template Name**, enter **Carousel template**, and then select **OK**.</span></span>
1. <span data-ttu-id="2c5ea-140">Do úseku **Tělo** přidejte modul **Výchozí stránka**.</span><span class="sxs-lookup"><span data-stu-id="2c5ea-140">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="2c5ea-141">Chcete-li vrátit šablonu se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="2c5ea-141">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>  
1. <span data-ttu-id="2c5ea-142">Šablonu karuselu, kterou jste právě vytvořili, použijte pro vytvoření stránky s názvem **Stránka karuselu**.</span><span class="sxs-lookup"><span data-stu-id="2c5ea-142">Use the carousel template that you just created to create a page that is named **Carousel page**.</span></span>
1. <span data-ttu-id="2c5ea-143">V úseku **Hlavní** nové stránky přidejte modul kontejneru.</span><span class="sxs-lookup"><span data-stu-id="2c5ea-143">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="2c5ea-144">V podokně napravo nastavte hodnotu **šířka** na **Vyplnit obrazovku**.</span><span class="sxs-lookup"><span data-stu-id="2c5ea-144">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="2c5ea-145">V části **Osnova stránky** stránky přidejte do modulu kontejneru modul karuselu.</span><span class="sxs-lookup"><span data-stu-id="2c5ea-145">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="2c5ea-146">Přidejte modul bloku obsahu do karuselového modulu.</span><span class="sxs-lookup"><span data-stu-id="2c5ea-146">Add a content block module to the carousel module.</span></span> <span data-ttu-id="2c5ea-147">Vlastnosti modulu bloku obsahu lze nastavit v **Záhlaví**, **Odkaz**, **Rozložení** a dalších vlastností.</span><span class="sxs-lookup"><span data-stu-id="2c5ea-147">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="2c5ea-148">Přidání a konfigurace jiného modulu bloku obsahu.</span><span class="sxs-lookup"><span data-stu-id="2c5ea-148">Add and configure another content block module.</span></span>
1. <span data-ttu-id="2c5ea-149">Nastavte další vlastnosti modulu karuselu podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="2c5ea-149">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="2c5ea-150">Vyberte možnost **Uložit** a poté vyberte možnost **Náhled**, chcete-li zobrazit náhled stránky.</span><span class="sxs-lookup"><span data-stu-id="2c5ea-150">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="2c5ea-151">Stránka by měla zobrazit karusel, který má dva moduly uvnitř (modul hlavního banneru a propagační modul).</span><span class="sxs-lookup"><span data-stu-id="2c5ea-151">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="2c5ea-152">Chcete-li dosáhnout požadovaného účinku, můžete změnit další vlastnosti pro karuselový a propagační modul nebo modul hlavního banneru.</span><span class="sxs-lookup"><span data-stu-id="2c5ea-152">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="2c5ea-153">Chcete-li vrátit stránku se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="2c5ea-153">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2c5ea-154">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="2c5ea-154">Additional resources</span></span>

[<span data-ttu-id="2c5ea-155">Přehled knihovny modulů</span><span class="sxs-lookup"><span data-stu-id="2c5ea-155">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="2c5ea-156">Modul propagačního banneru</span><span class="sxs-lookup"><span data-stu-id="2c5ea-156">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="2c5ea-157">Modul textového bloku</span><span class="sxs-lookup"><span data-stu-id="2c5ea-157">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="2c5ea-158">Modul bloku obsahu</span><span class="sxs-lookup"><span data-stu-id="2c5ea-158">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="2c5ea-159">Modul videopřehrávače</span><span class="sxs-lookup"><span data-stu-id="2c5ea-159">Video player module</span></span>](add-video-player.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]