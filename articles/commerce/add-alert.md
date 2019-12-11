---
title: Modul výstrahy
description: Tohle téma se zabývá moduly výstrahy a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 82138dd7f0934f732215f67a3726638eb87075d4
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785345"
---
# <a name="alert-module"></a><span data-ttu-id="ea0dd-103">Modul výstrahy</span><span class="sxs-lookup"><span data-stu-id="ea0dd-103">Alert module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="ea0dd-104">Tohle téma se zabývá moduly výstrahy a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ea0dd-104">This topic covers alert modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ea0dd-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="ea0dd-105">Overview</span></span>

<span data-ttu-id="ea0dd-106">Modul výstrahy slouží k zobrazení vložených informačních zpráv na stránce.</span><span class="sxs-lookup"><span data-stu-id="ea0dd-106">An alert module is used to show inline informational messages on a page.</span></span> <span data-ttu-id="ea0dd-107">Moduly výstrah podporují textové zprávy a odkazy.</span><span class="sxs-lookup"><span data-stu-id="ea0dd-107">Alert modules support a text message and a link.</span></span> <span data-ttu-id="ea0dd-108">Lze je použít k zobrazení promoakcí v rámci celého webu, které se zobrazí na všech stránkách webu elektronického obchodu.</span><span class="sxs-lookup"><span data-stu-id="ea0dd-108">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="ea0dd-109">Moduly výstrah jsou řízeny daty ze systému správy obsahu (CMS) a lze je umístit na libovolnou stránku.</span><span class="sxs-lookup"><span data-stu-id="ea0dd-109">Alert modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="examples-of-alert-modules-in-e-commerce"></a><span data-ttu-id="ea0dd-110">Příklady modulů výstrah v elektronickém obchodu</span><span class="sxs-lookup"><span data-stu-id="ea0dd-110">Examples of alert modules in e-Commerce</span></span>

<span data-ttu-id="ea0dd-111">Moduly výstrah lze použít v záhlaví webu, kde označují promoakce nebo zprávy na úrovni celého webu.</span><span class="sxs-lookup"><span data-stu-id="ea0dd-111">Alert modules can be used in the site header to indicate site-wide promotions or messages.</span></span> <span data-ttu-id="ea0dd-112">Několik příkladů:</span><span class="sxs-lookup"><span data-stu-id="ea0dd-112">Here are some examples:</span></span>

<span data-ttu-id="ea0dd-113">„Výroční výprodej končí za 10 dnů“</span><span class="sxs-lookup"><span data-stu-id="ea0dd-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="ea0dd-114">„Ušetřete v předškolním výprodeji.</span><span class="sxs-lookup"><span data-stu-id="ea0dd-114">"Save big with back to school sale.</span></span> <span data-ttu-id="ea0dd-115">Pusťte se do nakupování.“</span><span class="sxs-lookup"><span data-stu-id="ea0dd-115">Shop Now."</span></span>

## <a name="alert-module-properties"></a><span data-ttu-id="ea0dd-116">Vlastnosti modulu výstrahy</span><span class="sxs-lookup"><span data-stu-id="ea0dd-116">Alert module properties</span></span>

| <span data-ttu-id="ea0dd-117">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="ea0dd-117">Property name</span></span>  | <span data-ttu-id="ea0dd-118">Hodnota</span><span class="sxs-lookup"><span data-stu-id="ea0dd-118">Value</span></span>                              | <span data-ttu-id="ea0dd-119">Popis</span><span class="sxs-lookup"><span data-stu-id="ea0dd-119">Description</span></span> |
|----------------|------------------------------------|-------------|
| <span data-ttu-id="ea0dd-120">Text</span><span class="sxs-lookup"><span data-stu-id="ea0dd-120">Text</span></span>           | <span data-ttu-id="ea0dd-121">Text</span><span class="sxs-lookup"><span data-stu-id="ea0dd-121">Text</span></span>                               | <span data-ttu-id="ea0dd-122">Textová zpráva, která se zobrazí v modulu výstrahy.</span><span class="sxs-lookup"><span data-stu-id="ea0dd-122">The text message that appears in the alert module.</span></span> |
| <span data-ttu-id="ea0dd-123">Zarovnání textu</span><span class="sxs-lookup"><span data-stu-id="ea0dd-123">Text alignment</span></span> | <span data-ttu-id="ea0dd-124">**Vpravo**, **vlevo** nebo **uprostřed**</span><span class="sxs-lookup"><span data-stu-id="ea0dd-124">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="ea0dd-125">Hodnota definující zarovnání textu v modulu výstrahy.</span><span class="sxs-lookup"><span data-stu-id="ea0dd-125">A value that defines how text is aligned in the alert module.</span></span> |
| <span data-ttu-id="ea0dd-126">Zamítnout výstrahu</span><span class="sxs-lookup"><span data-stu-id="ea0dd-126">Dismiss alert</span></span>  | <span data-ttu-id="ea0dd-127">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="ea0dd-127">**True** or **False**</span></span>              | <span data-ttu-id="ea0dd-128">Je-li tato hodnota nastavena na hodnotu **pravda**, zákazník může výstrahu zavřít.</span><span class="sxs-lookup"><span data-stu-id="ea0dd-128">If the value is set to **True**, the customer can dismiss the alert.</span></span> |
| <span data-ttu-id="ea0dd-129">Připojení</span><span class="sxs-lookup"><span data-stu-id="ea0dd-129">Link</span></span>           | <span data-ttu-id="ea0dd-130">Adresa URL</span><span class="sxs-lookup"><span data-stu-id="ea0dd-130">URL</span></span>                                | <span data-ttu-id="ea0dd-131">Adresa URL pro volitelný odkaz.</span><span class="sxs-lookup"><span data-stu-id="ea0dd-131">The URL for an optional link.</span></span> |

## <a name="add-an-alert-module-to-a-page"></a><span data-ttu-id="ea0dd-132">Přidání modulu výstrahy na stránku</span><span class="sxs-lookup"><span data-stu-id="ea0dd-132">Add an alert module to a page</span></span> 

<span data-ttu-id="ea0dd-133">Chcete-li přidat modul výstrahy na stránku a nastavit požadované vlastnosti, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="ea0dd-133">To add an alert module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="ea0dd-134">Vytvořte šablonu stránky s názvem **Šablona výstrahy**.</span><span class="sxs-lookup"><span data-stu-id="ea0dd-134">Create a page template that is named **alert template**.</span></span>
1. <span data-ttu-id="ea0dd-135">V pozici **Hlavní** na výchozí stránce přidejte modul výstrahy.</span><span class="sxs-lookup"><span data-stu-id="ea0dd-135">In the **Main** slot of the default page, add an alert module.</span></span>
1. <span data-ttu-id="ea0dd-136">Vraťte šablonu se změnami a publikujte ji.</span><span class="sxs-lookup"><span data-stu-id="ea0dd-136">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="ea0dd-137">Šablonu výstrahy, kterou jste právě vytvořili, použijte pro vytvoření stránky s názvem **Stránka výstrahy**.</span><span class="sxs-lookup"><span data-stu-id="ea0dd-137">Use the alert template that you just created to create a page that is named **alert page**.</span></span> 
1. <span data-ttu-id="ea0dd-138">V pozici **Hlavní** nové stránky přidejte modul výstrahy.</span><span class="sxs-lookup"><span data-stu-id="ea0dd-138">In the **Main** slot of the new page, add an alert module.</span></span>
1. <span data-ttu-id="ea0dd-139">V nastavení modulu výstrahy zadejte text výstrahy.</span><span class="sxs-lookup"><span data-stu-id="ea0dd-139">In the settings for the alert module, enter the alert text.</span></span> <span data-ttu-id="ea0dd-140">Chcete-li dále upravit modul výstrahy, můžete upravit ostatní vlastnosti.</span><span class="sxs-lookup"><span data-stu-id="ea0dd-140">You can edit the other properties if you want to customize the alert module further.</span></span>
1. <span data-ttu-id="ea0dd-141">Uložte stránku a zobrazte náhled.</span><span class="sxs-lookup"><span data-stu-id="ea0dd-141">Save and preview the page.</span></span> <span data-ttu-id="ea0dd-142">V horní části stránky by se měla zobrazit výstraha obsahující text, který jste přidali.</span><span class="sxs-lookup"><span data-stu-id="ea0dd-142">At the top of the page, you should see an alert that has the text that you added.</span></span>
1. <span data-ttu-id="ea0dd-143">Vraťte stránku se změnami a publikujte ji.</span><span class="sxs-lookup"><span data-stu-id="ea0dd-143">Check in the page, and publish it.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="ea0dd-144">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="ea0dd-144">Additional resources</span></span>

[<span data-ttu-id="ea0dd-145">Přehled startovací sady</span><span class="sxs-lookup"><span data-stu-id="ea0dd-145">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="ea0dd-146">Karuselový modul</span><span class="sxs-lookup"><span data-stu-id="ea0dd-146">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="ea0dd-147">Modul bloku s formátovaným obsahem</span><span class="sxs-lookup"><span data-stu-id="ea0dd-147">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="ea0dd-148">Modul umístění obsahu</span><span class="sxs-lookup"><span data-stu-id="ea0dd-148">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="ea0dd-149">Propagační modul</span><span class="sxs-lookup"><span data-stu-id="ea0dd-149">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="ea0dd-150">Modul hlavního banneru </span><span class="sxs-lookup"><span data-stu-id="ea0dd-150">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="ea0dd-151">Modul přehrávače videa</span><span class="sxs-lookup"><span data-stu-id="ea0dd-151">Video player module</span></span>](add-video-player.md)
