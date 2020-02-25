---
title: Karuselový modul
description: Tohle téma se zabývá karuselovými moduly a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: f279d7db0a92df9e64b1d3f6ca01c65ca1478d79
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025774"
---
# <a name="carousel-module"></a><span data-ttu-id="992c6-103">Karuselový modul</span><span class="sxs-lookup"><span data-stu-id="992c6-103">Carousel module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="992c6-104">Tohle téma se zabývá karuselovými moduly a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="992c6-104">This topic covers carousel modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="992c6-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="992c6-105">Overview</span></span>

<span data-ttu-id="992c6-106">Karuselový modul slouží k umístění propagačních položek do rotujícího banneru karuselu (včetně formátovaných obrázků), který mohou zákazníci procházet.</span><span class="sxs-lookup"><span data-stu-id="992c6-106">A carousel module is used to put multiple promotional items (including rich images) in a rotating carousel banner that customers can browse.</span></span> <span data-ttu-id="992c6-107">Maloobchodní prodejce může například pomocí karuselového modulu na domovské stránce prezentovat nové produkty nebo propagační akce.</span><span class="sxs-lookup"><span data-stu-id="992c6-107">For example, a retailer can use a carousel module on a home page to showcase multiple new products or promotions.</span></span>

<span data-ttu-id="992c6-108">Do karuselového modulu můžete přidat modul bloku obsahu.</span><span class="sxs-lookup"><span data-stu-id="992c6-108">You can add content block modules inside a carousel module.</span></span> <span data-ttu-id="992c6-109">Vlastnosti karuselového modulu pak definují způsob, jakým jsou tyto moduly vykreslovány.</span><span class="sxs-lookup"><span data-stu-id="992c6-109">The properties of the carousel module then define how those modules are rendered.</span></span>

## <a name="examples-of-carousel-modules-in-e-commerce"></a><span data-ttu-id="992c6-110">Příklady karuselových modulů v elektronickém obchodu</span><span class="sxs-lookup"><span data-stu-id="992c6-110">Examples of carousel modules in e-Commerce</span></span>

- <span data-ttu-id="992c6-111">Na domovské stránce lze použít karusel s více propagačními moduly.</span><span class="sxs-lookup"><span data-stu-id="992c6-111">A carousel that has multiple promotional modules inside it can be used on a home page.</span></span>
- <span data-ttu-id="992c6-112">Na stránce s podrobnostmi o produktu lze použít karusel s více propagačními moduly.</span><span class="sxs-lookup"><span data-stu-id="992c6-112">A carousel that has multiple promotional modules inside it can be used on a product details page.</span></span>
- <span data-ttu-id="992c6-113">Karusel lze použít na libovolné marketingové stránce k propagaci promoakcí a produktů.</span><span class="sxs-lookup"><span data-stu-id="992c6-113">A carousel can be used on any marketing page to promote multiple promotions or products.</span></span>

## <a name="carousel-module-properties"></a><span data-ttu-id="992c6-114">Vlastnosti karuselového modulu</span><span class="sxs-lookup"><span data-stu-id="992c6-114">Carousel module properties</span></span>

| <span data-ttu-id="992c6-115">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="992c6-115">Property name</span></span>             | <span data-ttu-id="992c6-116">Hodnota</span><span class="sxs-lookup"><span data-stu-id="992c6-116">Value</span></span>                 | <span data-ttu-id="992c6-117">Popis</span><span class="sxs-lookup"><span data-stu-id="992c6-117">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="992c6-118">Přehrát automaticky</span><span class="sxs-lookup"><span data-stu-id="992c6-118">Autoplay</span></span>                  | <span data-ttu-id="992c6-119">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="992c6-119">**True** or **False**</span></span> | <span data-ttu-id="992c6-120">Je- li nastavena hodnota **Pravda**, dojde k automatickému přechodu mezi položkami v karuselu.</span><span class="sxs-lookup"><span data-stu-id="992c6-120">If the value is set to **True**, the transition between items inside the carousel occurs automatically.</span></span> <span data-ttu-id="992c6-121">Pokud je hodnota nastavena na **Nepravda**, nedochází k žádnému přechodu, pokud zákazník nepoužije klávesnici nebo myš k přechodu z jedné položky na další položku.</span><span class="sxs-lookup"><span data-stu-id="992c6-121">If the value is set to **False**, no transition occurs unless the customer uses the keyboard or mouse to move from one item to the next item.</span></span> |
| <span data-ttu-id="992c6-122">Interval přechodu snímků</span><span class="sxs-lookup"><span data-stu-id="992c6-122">Slide transition interval</span></span> | <span data-ttu-id="992c6-123">Hodnota v sekundách</span><span class="sxs-lookup"><span data-stu-id="992c6-123">A value in seconds</span></span>    | <span data-ttu-id="992c6-124">Interval pro přechody mezi položkami.</span><span class="sxs-lookup"><span data-stu-id="992c6-124">The interval for transitions between items.</span></span> |
| <span data-ttu-id="992c6-125">Typ přechodu</span><span class="sxs-lookup"><span data-stu-id="992c6-125">Transition type</span></span>           | <span data-ttu-id="992c6-126">**Posunutí** nebo **Slábnutí**</span><span class="sxs-lookup"><span data-stu-id="992c6-126">**Slide** or **Fade**</span></span> | <span data-ttu-id="992c6-127">Přechodový efekt mezi položkami.</span><span class="sxs-lookup"><span data-stu-id="992c6-127">The transition effect between items.</span></span> |
| <span data-ttu-id="992c6-128">Skrýt karuselové překlopení</span><span class="sxs-lookup"><span data-stu-id="992c6-128">Hide carousel flipper</span></span>     | <span data-ttu-id="992c6-129">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="992c6-129">**True** or **False**</span></span> | <span data-ttu-id="992c6-130">Je-li nastavena na **true**, bude páka karuselu a indikátor pořadí skrytý.</span><span class="sxs-lookup"><span data-stu-id="992c6-130">If the value is set to **True**, the carousel flipper and sequence indicator are hidden.</span></span> |
| <span data-ttu-id="992c6-131">Povolit zrušení karuselu</span><span class="sxs-lookup"><span data-stu-id="992c6-131">Allow carousel dismiss</span></span>    | <span data-ttu-id="992c6-132">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="992c6-132">**True** or **False**</span></span> | <span data-ttu-id="992c6-133">Je-li tato hodnota nastavena na hodnotu **pravda**, uživatelé mohou karusel zrušit.</span><span class="sxs-lookup"><span data-stu-id="992c6-133">If the value is set to **True**, users can dismiss the carousel.</span></span> |

## <a name="add-a-carousel-module-to-a-page"></a><span data-ttu-id="992c6-134">Přidání karuselového modulu na stránku</span><span class="sxs-lookup"><span data-stu-id="992c6-134">Add a carousel module to a page</span></span>

<span data-ttu-id="992c6-135">Chcete-li přidat karuselový modul na novou stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="992c6-135">To add a carousel module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="992c6-136">Vytvořte šablonu stránky s názvem **Šablona karuselu**.</span><span class="sxs-lookup"><span data-stu-id="992c6-136">Create a page template that is named **carousel template**.</span></span>
1. <span data-ttu-id="992c6-137">Do úseku **Tělo** přidejte modul **Výchozí stránka**.</span><span class="sxs-lookup"><span data-stu-id="992c6-137">In the **Body** slot, add a **Default page** module.</span></span>
1. <span data-ttu-id="992c6-138">Vraťte šablonu se změnami a publikujte ji.</span><span class="sxs-lookup"><span data-stu-id="992c6-138">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="992c6-139">Šablonu karuselu, kterou jste právě vytvořili, použijte pro vytvoření stránky s názvem **Stránka karuselu**.</span><span class="sxs-lookup"><span data-stu-id="992c6-139">Use the carousel template that you just created to create a page that is named **carousel page**.</span></span>
1. <span data-ttu-id="992c6-140">V úseku **Hlavní** nové stránky přidejte modul kontejneru.</span><span class="sxs-lookup"><span data-stu-id="992c6-140">In the **Main** slot of the new page, add a container module.</span></span> 
1. <span data-ttu-id="992c6-141">V podokně napravo nastavte hodnotu **šířka** na **Vyplnit obrazovku**.</span><span class="sxs-lookup"><span data-stu-id="992c6-141">In the pane on the right, set the **Width** value to **Fill Screen**.</span></span>
1. <span data-ttu-id="992c6-142">V části **Osnova stránky** stránky přidejte do modulu kontejneru modul karuselu.</span><span class="sxs-lookup"><span data-stu-id="992c6-142">Under **Page Outline**, add a carousel module to the container module.</span></span>
1. <span data-ttu-id="992c6-143">Přidejte modul bloku obsahu do karuselového modulu.</span><span class="sxs-lookup"><span data-stu-id="992c6-143">Add a content block module to the carousel module.</span></span> <span data-ttu-id="992c6-144">Vlastnosti modulu bloku obsahu lze nastavit v **Záhlaví**, **Odkaz**, **Rozložení** a dalších vlastností.</span><span class="sxs-lookup"><span data-stu-id="992c6-144">Set the properties of the content block module by providing **Heading**, **Link**, **Layout**, and other properties.</span></span>
1. <span data-ttu-id="992c6-145">Přidání a konfigurace jiného modulu bloku obsahu.</span><span class="sxs-lookup"><span data-stu-id="992c6-145">Add and configure another content block module.</span></span>
1. <span data-ttu-id="992c6-146">Nastavte další vlastnosti modulu karuselu podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="992c6-146">Set additional properties for the carousel module as you require.</span></span>
1. <span data-ttu-id="992c6-147">Uložte stránku a zobrazte náhled.</span><span class="sxs-lookup"><span data-stu-id="992c6-147">Save and preview the page.</span></span> <span data-ttu-id="992c6-148">Stránka by měla zobrazit karusel, který má dva moduly uvnitř (modul hlavního banneru a propagační modul).</span><span class="sxs-lookup"><span data-stu-id="992c6-148">The page should show a carousel that has two modules inside it (a hero module and a feature module).</span></span> <span data-ttu-id="992c6-149">Chcete-li dosáhnout požadovaného účinku, můžete změnit další vlastnosti pro karuselový a propagační modul nebo modul hlavního banneru.</span><span class="sxs-lookup"><span data-stu-id="992c6-149">You can change additional properties for the carousel, hero, and feature modules to achieve the desired effect.</span></span>
1. <span data-ttu-id="992c6-150">Dokončete úpravy stránky a publikujte ji.</span><span class="sxs-lookup"><span data-stu-id="992c6-150">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="992c6-151">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="992c6-151">Additional resources</span></span>

[<span data-ttu-id="992c6-152">Přehled startovací sady</span><span class="sxs-lookup"><span data-stu-id="992c6-152">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="992c6-153">Modul propagačního banneru</span><span class="sxs-lookup"><span data-stu-id="992c6-153">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="992c6-154">Modul textového bloku</span><span class="sxs-lookup"><span data-stu-id="992c6-154">Text block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="992c6-155">Modul bloku obsahu</span><span class="sxs-lookup"><span data-stu-id="992c6-155">Content block module</span></span>](add-hero-module.md)

[<span data-ttu-id="992c6-156">Modul videopřehrávače</span><span class="sxs-lookup"><span data-stu-id="992c6-156">Video player module</span></span>](add-video-player.md)
