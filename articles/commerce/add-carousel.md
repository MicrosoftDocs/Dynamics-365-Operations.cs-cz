---
title: Karuselový modul
description: Tohle téma se zabývá karuselovými moduly a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: c2c5adc8ab2e0330f7b07e5153fd8332ab0203e5
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785230"
---
# <a name="carousel-module"></a><span data-ttu-id="9954e-103">Karuselový modul</span><span class="sxs-lookup"><span data-stu-id="9954e-103">Carousel module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="9954e-104">Tohle téma se zabývá karuselovými moduly a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="9954e-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="9954e-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="9954e-105">Overview</span></span>

<span data-ttu-id="9954e-106">Karuselový modul slouží k umístění propagačních položek do karuselu, který mohou zákazníci procházet.</span><span class="sxs-lookup"><span data-stu-id="9954e-106">A carousel module is used to put multiple promotional items in a carousel that customers can browse.</span></span> <span data-ttu-id="9954e-107">Je to speciální modul kontejneru, který hostuje jiné moduly.</span><span class="sxs-lookup"><span data-stu-id="9954e-107">It's a special container module that hosts other modules.</span></span> <span data-ttu-id="9954e-108">Maloobchodní prodejce může například pomocí karuselového modulu na domovské stránce prezentovat nové produkty nebo propagační akce.</span><span class="sxs-lookup"><span data-stu-id="9954e-108">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="9954e-109">Do karuselového modulu můžete přidat modul hlavního banneru nebo propagační modul.</span><span class="sxs-lookup"><span data-stu-id="9954e-109">You can add hero and feature modules inside a carousel module.</span></span> <span data-ttu-id="9954e-110">Vlastnosti karuselového modulu pak definují způsob, jakým jsou tyto moduly vykreslovány.</span><span class="sxs-lookup"><span data-stu-id="9954e-110">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="9954e-111">Příklady karuselových modulů v elektronickém obchodu</span><span class="sxs-lookup"><span data-stu-id="9954e-111">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="9954e-112">Na domovské stránce lze použít karusel s více propagačními moduly.</span><span class="sxs-lookup"><span data-stu-id="9954e-112">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="9954e-113">Na stránce s podrobnostmi o produktu lze použít karusel s více propagačními moduly.</span><span class="sxs-lookup"><span data-stu-id="9954e-113">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="9954e-114">Karusel lze použít na libovolné marketingové stránce k propagaci promoakcí a produktů.</span><span class="sxs-lookup"><span data-stu-id="9954e-114">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

## <a name="carousel-module-properties"></a><span data-ttu-id="9954e-115">Vlastnosti karuselového modulu</span><span class="sxs-lookup"><span data-stu-id="9954e-115">Carousel module properties</span></span>

| <span data-ttu-id="9954e-116">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="9954e-116">Property name</span></span>             | <span data-ttu-id="9954e-117">Hodnota</span><span class="sxs-lookup"><span data-stu-id="9954e-117">Value</span></span>                                | <span data-ttu-id="9954e-118">Popis</span><span class="sxs-lookup"><span data-stu-id="9954e-118">Description</span></span> |
|---------------------------|--------------------------------------|-------------|
| <span data-ttu-id="9954e-119">Přehrát automaticky</span><span class="sxs-lookup"><span data-stu-id="9954e-119">Autoplay</span></span>                  | <span data-ttu-id="9954e-120">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="9954e-120">**True** or **False**</span></span>                | <span data-ttu-id="9954e-121">Je- li nastavena hodnota **Pravda**, dojde k automatickému přechodu mezi položkami v karuselu.</span><span class="sxs-lookup"><span data-stu-id="9954e-121">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="9954e-122">Pokud je hodnota nastavena na **Nepravda**, nedochází k žádnému přechodu, pokud zákazník nepoužije klávesnici nebo myš k přechodu z jedné položky na další položku.</span><span class="sxs-lookup"><span data-stu-id="9954e-122">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="9954e-123">Interval přechodu snímků</span><span class="sxs-lookup"><span data-stu-id="9954e-123">Slide transition interval</span></span> | <span data-ttu-id="9954e-124">Hodnota v sekundách</span><span class="sxs-lookup"><span data-stu-id="9954e-124">A value in seconds</span></span>                   | <span data-ttu-id="9954e-125">Interval pro přechody mezi položkami.</span><span class="sxs-lookup"><span data-stu-id="9954e-125">The interval for transitions between items.</span></span> |
| <span data-ttu-id="9954e-126">Animace přechodu</span><span class="sxs-lookup"><span data-stu-id="9954e-126">Transition animation</span></span>      | <span data-ttu-id="9954e-127">**Posunutí** nebo **Slábnutí**</span><span class="sxs-lookup"><span data-stu-id="9954e-127">**Slide** or **Fade**</span></span>                | <span data-ttu-id="9954e-128">Efekt při přechodu.</span><span class="sxs-lookup"><span data-stu-id="9954e-128">The transition effect.</span></span> |
| <span data-ttu-id="9954e-129">Šířka</span><span class="sxs-lookup"><span data-stu-id="9954e-129">Width</span></span>                     | <span data-ttu-id="9954e-130">**Přizpůsobit kontejneru** nebo **Vyplnit obrazovku**</span><span class="sxs-lookup"><span data-stu-id="9954e-130">**Fit container** or **Fill screen**</span></span> | <span data-ttu-id="9954e-131">Je-li hodnota nastavena na **Přizpůsobit kontejneru**, budou položky uvnitř karuselu omezeny na šířku karuselu.</span><span class="sxs-lookup"><span data-stu-id="9954e-131">If the value is set to **Fit container**, the items inside the carousel are restricted to the width of the carousel.</span></span> <span data-ttu-id="9954e-132">Je-li hodnota nastavena na **Vyplnit obrazovku**, položky nejsou omezeny na šířku karuselu, ale mohou přejít do režimu celé obrazovky.</span><span class="sxs-lookup"><span data-stu-id="9954e-132">If the value is set to **Fill screen**, the items aren't restricted to the carousel width but can go into full-screen mode.</span></span> <span data-ttu-id="9954e-133">Chcete-li dosáhnout požadovaného rozvržení, můžete změnit tuto hodnotu.</span><span class="sxs-lookup"><span data-stu-id="9954e-133">You can change the value to achieve the desired layout.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="9954e-134">Přidání karuselového modulu na stránku</span><span class="sxs-lookup"><span data-stu-id="9954e-134">Add a carousel module to a page</span></span>

<span data-ttu-id="9954e-135">Chcete-li přidat karuselový modul na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="9954e-135">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="9954e-136">Vytvořte šablonu stránky s názvem **Šablona karuselu**.</span><span class="sxs-lookup"><span data-stu-id="9954e-136">Create a page template that is named **carousel template**.</span></span>
1. <span data-ttu-id="9954e-137">V pozici **Hlavní** na výchozí stránce přidejte karuselový modul.</span><span class="sxs-lookup"><span data-stu-id="9954e-137">In the **Main** slot of the default page, add a carousel module.</span></span>
1. <span data-ttu-id="9954e-138">Přidejte modul hlavního banneru do karuselového modulu.</span><span class="sxs-lookup"><span data-stu-id="9954e-138">Add a hero module to the carousel module.</span></span>
1. <span data-ttu-id="9954e-139">Přidejte propagační modul do karuselového modulu.</span><span class="sxs-lookup"><span data-stu-id="9954e-139">Add a feature module to the carousel module.</span></span>
1. <span data-ttu-id="9954e-140">Vraťte šablonu se změnami a publikujte ji.</span><span class="sxs-lookup"><span data-stu-id="9954e-140">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="9954e-141">Šablonu karuselu, kterou jste právě vytvořili, použijte pro vytvoření stránky s názvem **Stránka karuselu**.</span><span class="sxs-lookup"><span data-stu-id="9954e-141">Use the carousel template that you just created to create a page that is named **carousel page**.</span></span>
1. <span data-ttu-id="9954e-142">V úseku **Hlavní** nové stránky přidejte karuselový modul.</span><span class="sxs-lookup"><span data-stu-id="9954e-142">In the **Main** slot of the new page, add a carousel module.</span></span>
1. <span data-ttu-id="9954e-143">Nastavte vlastnost **Šířka** karuselového modulu na **Vyplnit obrazovku**.</span><span class="sxs-lookup"><span data-stu-id="9954e-143">Set the **Width** property of the carousel module to **Fill screen**.</span></span> 
1. <span data-ttu-id="9954e-144">Nastavte vlastnost **Animace přechodu** na **Posunutí**.</span><span class="sxs-lookup"><span data-stu-id="9954e-144">Set the **Transition animation** property to **Slide**.</span></span>
1. <span data-ttu-id="9954e-145">Přidejte modul hlavního banneru do karuselového modulu.</span><span class="sxs-lookup"><span data-stu-id="9954e-145">Add a hero module to the carousel module.</span></span>
1. <span data-ttu-id="9954e-146">V modulu hlavního banneru přidejte obrázek a nadpis a pak vyberte možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="9954e-146">In the hero module, add an image and a heading, and then select **Save**.</span></span>
1. <span data-ttu-id="9954e-147">Přidejte propagační modul do karuselového modulu.</span><span class="sxs-lookup"><span data-stu-id="9954e-147">Add a feature module to the carousel module.</span></span>
1. <span data-ttu-id="9954e-148">V propagačním modulu přidejte obrázek, nadpis a odstavec textu.</span><span class="sxs-lookup"><span data-stu-id="9954e-148">In the feature module, add an image, a heading, and a paragraph of text.</span></span>
1. <span data-ttu-id="9954e-149">Uložte stránku a zobrazte náhled.</span><span class="sxs-lookup"><span data-stu-id="9954e-149">Save and preview the page.</span></span> <span data-ttu-id="9954e-150">Stránka by měla zobrazit karusel, který má dva moduly uvnitř (modul hlavního banneru a propagační modul).</span><span class="sxs-lookup"><span data-stu-id="9954e-150">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="9954e-151">Chcete-li dosáhnout požadovaného účinku, můžete změnit další vlastnosti pro karuselový a propagační modul nebo modul hlavního banneru.</span><span class="sxs-lookup"><span data-stu-id="9954e-151">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="9954e-152">Vraťte stránku se změnami a publikujte ji.</span><span class="sxs-lookup"><span data-stu-id="9954e-152">Check in the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9954e-153">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="9954e-153">Additional resources</span></span>

[<span data-ttu-id="9954e-154">Přehled startovací sady</span><span class="sxs-lookup"><span data-stu-id="9954e-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="9954e-155">Modul výstrahy</span><span class="sxs-lookup"><span data-stu-id="9954e-155">Alert module</span></span>](add-alert.md)

[<span data-ttu-id="9954e-156">Modul bloku s formátovaným obsahem</span><span class="sxs-lookup"><span data-stu-id="9954e-156">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="9954e-157">Modul umístění obsahu</span><span class="sxs-lookup"><span data-stu-id="9954e-157">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="9954e-158">Propagační modul</span><span class="sxs-lookup"><span data-stu-id="9954e-158">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="9954e-159">Modul hlavního banneru</span><span class="sxs-lookup"><span data-stu-id="9954e-159">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="9954e-160">Modul přehrávače videa</span><span class="sxs-lookup"><span data-stu-id="9954e-160">Video player module</span></span>](add-video-player.md)
