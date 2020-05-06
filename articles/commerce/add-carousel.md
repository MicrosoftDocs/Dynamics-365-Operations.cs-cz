---
title: Karuselový modul
description: Tohle téma se zabývá karuselovými moduly a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 04/14/2020
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
ms.openlocfilehash: f399e4c5618b65b781fdd3ec835e841614579313
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269721"
---
# <a name="carousel-module"></a><span data-ttu-id="67aff-103">Karuselový modul</span><span class="sxs-lookup"><span data-stu-id="67aff-103">Carousel module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="67aff-104">Tohle téma se zabývá karuselovými moduly a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="67aff-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="67aff-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="67aff-105">Overview</span></span>

<span data-ttu-id="67aff-106">Karuselový modul slouží k umístění propagačních položek do rotujícího banneru karuselu (včetně formátovaných obrázků), který mohou zákazníci procházet.</span><span class="sxs-lookup"><span data-stu-id="67aff-106">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="67aff-107">Maloobchodní prodejce může například pomocí karuselového modulu na domovské stránce prezentovat nové produkty nebo propagační akce.</span><span class="sxs-lookup"><span data-stu-id="67aff-107">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="67aff-108">Do karuselového modulu můžete přidat modul bloku obsahu.</span><span class="sxs-lookup"><span data-stu-id="67aff-108">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="67aff-109">Vlastnosti karuselového modulu pak definují způsob, jakým jsou tyto moduly vykreslovány.</span><span class="sxs-lookup"><span data-stu-id="67aff-109">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="67aff-110">Příklady karuselových modulů v elektronickém obchodu</span><span class="sxs-lookup"><span data-stu-id="67aff-110">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="67aff-111">Na domovské stránce lze použít karusel s více propagačními moduly.</span><span class="sxs-lookup"><span data-stu-id="67aff-111">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="67aff-112">Na stránce s podrobnostmi o produktu lze použít karusel s více propagačními moduly.</span><span class="sxs-lookup"><span data-stu-id="67aff-112">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="67aff-113">Karusel lze použít na libovolné marketingové stránce k propagaci promoakcí a produktů.</span><span class="sxs-lookup"><span data-stu-id="67aff-113">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

## <a name="carousel-module-properties"></a><span data-ttu-id="67aff-114">Vlastnosti karuselového modulu</span><span class="sxs-lookup"><span data-stu-id="67aff-114">Carousel module properties</span></span>

| <span data-ttu-id="67aff-115">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="67aff-115">Property name</span></span>             | <span data-ttu-id="67aff-116">Hodnota</span><span class="sxs-lookup"><span data-stu-id="67aff-116">Value</span></span>                 | <span data-ttu-id="67aff-117">Popis</span><span class="sxs-lookup"><span data-stu-id="67aff-117">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="67aff-118">Přehrát automaticky</span><span class="sxs-lookup"><span data-stu-id="67aff-118">Autoplay</span></span>                  | <span data-ttu-id="67aff-119">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="67aff-119">**True** or **False**</span></span> | <span data-ttu-id="67aff-120">Je- li nastavena hodnota **Pravda**, dojde k automatickému přechodu mezi položkami v karuselu.</span><span class="sxs-lookup"><span data-stu-id="67aff-120">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="67aff-121">Pokud je hodnota nastavena na **Nepravda**, nedochází k žádnému přechodu, pokud zákazník nepoužije klávesnici nebo myš k přechodu z jedné položky na další položku.</span><span class="sxs-lookup"><span data-stu-id="67aff-121">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="67aff-122">Interval přechodu snímků</span><span class="sxs-lookup"><span data-stu-id="67aff-122">Slide transition interval</span></span> | <span data-ttu-id="67aff-123">Hodnota v sekundách</span><span class="sxs-lookup"><span data-stu-id="67aff-123">A value in seconds</span></span>    | <span data-ttu-id="67aff-124">Interval pro přechody mezi položkami.</span><span class="sxs-lookup"><span data-stu-id="67aff-124">The interval for transitions between items.</span></span> |
| <span data-ttu-id="67aff-125">Typ přechodu</span><span class="sxs-lookup"><span data-stu-id="67aff-125">Transition type</span></span>           | <span data-ttu-id="67aff-126">**Posunutí** nebo **Slábnutí**</span><span class="sxs-lookup"><span data-stu-id="67aff-126">**Slide** or **Fade**</span></span> | <span data-ttu-id="67aff-127">Přechodový efekt mezi položkami.</span><span class="sxs-lookup"><span data-stu-id="67aff-127">The transition effect between items.</span></span> |
| <span data-ttu-id="67aff-128">Skrýt karuselové překlopení</span><span class="sxs-lookup"><span data-stu-id="67aff-128">Hide carousel flipper</span></span>     | <span data-ttu-id="67aff-129">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="67aff-129">**True** or **False**</span></span> | <span data-ttu-id="67aff-130">Je-li nastavena na **true**, bude páka karuselu a indikátor pořadí skrytý.</span><span class="sxs-lookup"><span data-stu-id="67aff-130">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="67aff-131">Povolit zrušení karuselu</span><span class="sxs-lookup"><span data-stu-id="67aff-131">Allow carousel dismiss</span></span>    | <span data-ttu-id="67aff-132">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="67aff-132">**True** or **False**</span></span> | <span data-ttu-id="67aff-133">Je-li tato hodnota nastavena na hodnotu **pravda**, uživatelé mohou karusel zrušit.</span><span class="sxs-lookup"><span data-stu-id="67aff-133">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="67aff-134">Přidání karuselového modulu na stránku</span><span class="sxs-lookup"><span data-stu-id="67aff-134">Add a carousel module to a page</span></span>

<span data-ttu-id="67aff-135">Chcete-li přidat karuselový modul na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="67aff-135">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="67aff-136">Zvolte **Nová** pro vytvoření šablony stránky.</span><span class="sxs-lookup"><span data-stu-id="67aff-136">Select **New** to create a page template.</span></span>
1. <span data-ttu-id="67aff-137">V dialogovém okně **Nová šablona** v části **Název šablony** zadejte **Šablona karuselu** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="67aff-137">In the **New Template** dialog box, under **Template Name**, enter **Carousel template**, and then select **OK**.</span></span>
1. <span data-ttu-id="67aff-138">Do úseku **Tělo** přidejte modul **Výchozí stránka**.</span><span class="sxs-lookup"><span data-stu-id="67aff-138">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="67aff-139">Chcete-li vrátit šablonu se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="67aff-139">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>  
1. <span data-ttu-id="67aff-140">Šablonu karuselu, kterou jste právě vytvořili, použijte pro vytvoření stránky s názvem **Stránka karuselu**.</span><span class="sxs-lookup"><span data-stu-id="67aff-140">Use the carousel template that you just created to create a page that is named **Carousel page**.</span></span>
1. <span data-ttu-id="67aff-141">V úseku **Hlavní** nové stránky přidejte modul kontejneru.</span><span class="sxs-lookup"><span data-stu-id="67aff-141">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="67aff-142">V podokně napravo nastavte hodnotu **šířka** na **Vyplnit obrazovku**.</span><span class="sxs-lookup"><span data-stu-id="67aff-142">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="67aff-143">V části **Osnova stránky** stránky přidejte do modulu kontejneru modul karuselu.</span><span class="sxs-lookup"><span data-stu-id="67aff-143">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="67aff-144">Přidejte modul bloku obsahu do karuselového modulu.</span><span class="sxs-lookup"><span data-stu-id="67aff-144">Add a content block module to the carousel module.</span></span> <span data-ttu-id="67aff-145">Vlastnosti modulu bloku obsahu lze nastavit v **Záhlaví**, **Odkaz**, **Rozložení** a dalších vlastností.</span><span class="sxs-lookup"><span data-stu-id="67aff-145">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="67aff-146">Přidání a konfigurace jiného modulu bloku obsahu.</span><span class="sxs-lookup"><span data-stu-id="67aff-146">Add and configure another content block module.</span></span>
1. <span data-ttu-id="67aff-147">Nastavte další vlastnosti modulu karuselu podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="67aff-147">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="67aff-148">Vyberte možnost **Uložit** a poté vyberte možnost **Náhled**, chcete-li zobrazit náhled stránky.</span><span class="sxs-lookup"><span data-stu-id="67aff-148">Select **Save**, and then select **Preview** to preview the page.</span></span> <span data-ttu-id="67aff-149">Stránka by měla zobrazit karusel, který má dva moduly uvnitř (modul hlavního banneru a propagační modul).</span><span class="sxs-lookup"><span data-stu-id="67aff-149">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="67aff-150">Chcete-li dosáhnout požadovaného účinku, můžete změnit další vlastnosti pro karuselový a propagační modul nebo modul hlavního banneru.</span><span class="sxs-lookup"><span data-stu-id="67aff-150">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="67aff-151">Chcete-li vrátit stránku se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="67aff-151">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="67aff-152">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="67aff-152">Additional resources</span></span>

[<span data-ttu-id="67aff-153">Přehled startovací sady</span><span class="sxs-lookup"><span data-stu-id="67aff-153">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="67aff-154">Modul propagačního banneru</span><span class="sxs-lookup"><span data-stu-id="67aff-154">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="67aff-155">Modul textového bloku</span><span class="sxs-lookup"><span data-stu-id="67aff-155">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="67aff-156">Modul bloku obsahu</span><span class="sxs-lookup"><span data-stu-id="67aff-156">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="67aff-157">Modul videopřehrávače</span><span class="sxs-lookup"><span data-stu-id="67aff-157">Video player module</span></span>](add-video-player.md)
