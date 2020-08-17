---
title: Karuselový modul
description: Tohle téma se zabývá karuselovými moduly a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: 10ff0cd566a1a8d89ccadce9571dafc5a592520b
ms.sourcegitcommit: 4a981ee4be6d7e6c0e55541535d386bce2565cba
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/27/2020
ms.locfileid: "3620979"
---
# <a name="carousel-module"></a><span data-ttu-id="009d7-103">Karuselový modul</span><span class="sxs-lookup"><span data-stu-id="009d7-103">Carousel module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="009d7-104">Tohle téma se zabývá karuselovými moduly a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="009d7-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="009d7-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="009d7-105">Overview</span></span>

<span data-ttu-id="009d7-106">Karuselový modul slouží k umístění propagačních položek do rotujícího banneru karuselu (včetně formátovaných obrázků), který mohou zákazníci procházet.</span><span class="sxs-lookup"><span data-stu-id="009d7-106">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="009d7-107">Maloobchodní prodejce může například pomocí karuselového modulu na domovské stránce prezentovat nové produkty nebo propagační akce.</span><span class="sxs-lookup"><span data-stu-id="009d7-107">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="009d7-108">Do karuselového modulu můžete přidat modul bloku obsahu.</span><span class="sxs-lookup"><span data-stu-id="009d7-108">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="009d7-109">Vlastnosti karuselového modulu pak definují způsob, jakým jsou tyto moduly vykreslovány.</span><span class="sxs-lookup"><span data-stu-id="009d7-109">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="009d7-110">Příklady karuselových modulů v elektronickém obchodu</span><span class="sxs-lookup"><span data-stu-id="009d7-110">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="009d7-111">Na domovské stránce lze použít karusel s více propagačními moduly.</span><span class="sxs-lookup"><span data-stu-id="009d7-111">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="009d7-112">Na stránce s podrobnostmi o produktu lze použít karusel s více propagačními moduly.</span><span class="sxs-lookup"><span data-stu-id="009d7-112">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="009d7-113">Karusel lze použít na libovolné marketingové stránce k propagaci promoakcí a produktů.</span><span class="sxs-lookup"><span data-stu-id="009d7-113">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

<span data-ttu-id="009d7-114">Následující obrázek ukazuje příklad karuselového modulu použitého na domovské stránce.</span><span class="sxs-lookup"><span data-stu-id="009d7-114">The following image shows an example of a carousel module that is used on a home page.</span></span> <span data-ttu-id="009d7-115">Tento karuselový model obsahuje několik položek bloku obsahu.</span><span class="sxs-lookup"><span data-stu-id="009d7-115">This carousel module contains multiple content block items.</span></span>

![Příklad karuselového modulu](./media/Hero.PNG)

## <a name="carousel-module-properties"></a><span data-ttu-id="009d7-117">Vlastnosti karuselového modulu</span><span class="sxs-lookup"><span data-stu-id="009d7-117">Carousel module properties</span></span>

| <span data-ttu-id="009d7-118">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="009d7-118">Property name</span></span>             | <span data-ttu-id="009d7-119">Hodnota</span><span class="sxs-lookup"><span data-stu-id="009d7-119">Value</span></span>                 | <span data-ttu-id="009d7-120">popis</span><span class="sxs-lookup"><span data-stu-id="009d7-120">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="009d7-121">Přehrát automaticky</span><span class="sxs-lookup"><span data-stu-id="009d7-121">Autoplay</span></span>                  | <span data-ttu-id="009d7-122">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="009d7-122">**True** or **False**</span></span> | <span data-ttu-id="009d7-123">Je- li nastavena hodnota **Pravda**, dojde k automatickému přechodu mezi položkami v karuselu.</span><span class="sxs-lookup"><span data-stu-id="009d7-123">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="009d7-124">Pokud je hodnota nastavena na **Nepravda**, nedochází k žádnému přechodu, pokud zákazník nepoužije klávesnici nebo myš k přechodu z jedné položky na další položku.</span><span class="sxs-lookup"><span data-stu-id="009d7-124">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="009d7-125">Interval přechodu snímků</span><span class="sxs-lookup"><span data-stu-id="009d7-125">Slide transition interval</span></span> | <span data-ttu-id="009d7-126">Hodnota v sekundách</span><span class="sxs-lookup"><span data-stu-id="009d7-126">A value in seconds</span></span>    | <span data-ttu-id="009d7-127">Interval pro přechody mezi položkami.</span><span class="sxs-lookup"><span data-stu-id="009d7-127">The interval for transitions between items.</span></span> |
| <span data-ttu-id="009d7-128">Typ přechodu</span><span class="sxs-lookup"><span data-stu-id="009d7-128">Transition type</span></span>           | <span data-ttu-id="009d7-129">**Posunutí** nebo **Slábnutí**</span><span class="sxs-lookup"><span data-stu-id="009d7-129">**Slide** or **Fade**</span></span> | <span data-ttu-id="009d7-130">Přechodový efekt mezi položkami.</span><span class="sxs-lookup"><span data-stu-id="009d7-130">The transition effect between items.</span></span> |
| <span data-ttu-id="009d7-131">Skrýt karuselové překlopení</span><span class="sxs-lookup"><span data-stu-id="009d7-131">Hide carousel flipper</span></span>     | <span data-ttu-id="009d7-132">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="009d7-132">**True** or **False**</span></span> | <span data-ttu-id="009d7-133">Je-li nastavena na **true**, bude páka karuselu a indikátor pořadí skrytý.</span><span class="sxs-lookup"><span data-stu-id="009d7-133">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="009d7-134">Povolit zrušení karuselu</span><span class="sxs-lookup"><span data-stu-id="009d7-134">Allow carousel dismiss</span></span>    | <span data-ttu-id="009d7-135">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="009d7-135">**True** or **False**</span></span> | <span data-ttu-id="009d7-136">Je-li tato hodnota nastavena na hodnotu **pravda**, uživatelé mohou karusel zrušit.</span><span class="sxs-lookup"><span data-stu-id="009d7-136">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="009d7-137">Přidání karuselového modulu na stránku</span><span class="sxs-lookup"><span data-stu-id="009d7-137">Add a carousel module to a page</span></span>

<span data-ttu-id="009d7-138">Chcete-li přidat karuselový modul na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="009d7-138">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="009d7-139">Přejděte na **Šablony** a poté volbou **Nová** vytvořte novou šablonu.</span><span class="sxs-lookup"><span data-stu-id="009d7-139">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="009d7-140">V dialogovém okně **Nová šablona** v části **Název šablony** zadejte **Šablona karuselu** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="009d7-140">In the **New Template** dialog box, under **Template Name**, enter **Carousel template**, and then select **OK**.</span></span>
1. <span data-ttu-id="009d7-141">Do úseku **Tělo** přidejte modul **Výchozí stránka**.</span><span class="sxs-lookup"><span data-stu-id="009d7-141">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="009d7-142">Chcete-li vrátit šablonu se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="009d7-142">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>  
1. <span data-ttu-id="009d7-143">Šablonu karuselu, kterou jste právě vytvořili, použijte pro vytvoření stránky s názvem **Stránka karuselu**.</span><span class="sxs-lookup"><span data-stu-id="009d7-143">Use the carousel template that you just created to create a page that is named **Carousel page**.</span></span>
1. <span data-ttu-id="009d7-144">V úseku **Hlavní** nové stránky přidejte modul kontejneru.</span><span class="sxs-lookup"><span data-stu-id="009d7-144">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="009d7-145">V podokně napravo nastavte hodnotu **šířka** na **Vyplnit obrazovku**.</span><span class="sxs-lookup"><span data-stu-id="009d7-145">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="009d7-146">V části **Osnova stránky** stránky přidejte do modulu kontejneru modul karuselu.</span><span class="sxs-lookup"><span data-stu-id="009d7-146">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="009d7-147">Přidejte modul bloku obsahu do karuselového modulu.</span><span class="sxs-lookup"><span data-stu-id="009d7-147">Add a content block module to the carousel module.</span></span> <span data-ttu-id="009d7-148">Vlastnosti modulu bloku obsahu lze nastavit v **Záhlaví**, **Odkaz**, **Rozložení** a dalších vlastností.</span><span class="sxs-lookup"><span data-stu-id="009d7-148">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="009d7-149">Přidání a konfigurace jiného modulu bloku obsahu.</span><span class="sxs-lookup"><span data-stu-id="009d7-149">Add and configure another content block module.</span></span>
1. <span data-ttu-id="009d7-150">Nastavte další vlastnosti modulu karuselu podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="009d7-150">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="009d7-151">Vyberte možnost **Uložit** a poté vyberte možnost **Náhled**, chcete-li zobrazit náhled stránky.</span><span class="sxs-lookup"><span data-stu-id="009d7-151">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="009d7-152">Stránka by měla zobrazit karusel, který má dva moduly uvnitř (modul hlavního banneru a propagační modul).</span><span class="sxs-lookup"><span data-stu-id="009d7-152">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="009d7-153">Chcete-li dosáhnout požadovaného účinku, můžete změnit další vlastnosti pro karuselový a propagační modul nebo modul hlavního banneru.</span><span class="sxs-lookup"><span data-stu-id="009d7-153">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="009d7-154">Chcete-li vrátit stránku se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="009d7-154">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="009d7-155">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="009d7-155">Additional resources</span></span>

[<span data-ttu-id="009d7-156">Přehled startovací sady</span><span class="sxs-lookup"><span data-stu-id="009d7-156">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="009d7-157">Modul propagačního banneru</span><span class="sxs-lookup"><span data-stu-id="009d7-157">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="009d7-158">Modul textového bloku</span><span class="sxs-lookup"><span data-stu-id="009d7-158">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="009d7-159">Modul bloku obsahu</span><span class="sxs-lookup"><span data-stu-id="009d7-159">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="009d7-160">Modul videopřehrávače</span><span class="sxs-lookup"><span data-stu-id="009d7-160">Video player module</span></span>](add-video-player.md)
