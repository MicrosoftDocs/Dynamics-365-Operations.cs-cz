---
title: Modul navigační nabídky
description: Tohle téma se zabývá moduly navigační nabídky a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/28/2021
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
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: f3461993e2bd59d66be1640331e4ef315a078469
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251204"
---
# <a name="navigation-menu-module"></a><span data-ttu-id="71613-103">Modul navigační nabídky</span><span class="sxs-lookup"><span data-stu-id="71613-103">Navigation menu module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="71613-104">Tohle téma se zabývá moduly navigační nabídky a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="71613-104">This topic covers navigation menu modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="71613-105">Primárním účelem modulů navigační nabídky je umožnit uživatelům webu procházet produkty a stránky webu podle hierarchie navigace sítě definované v centrále Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="71613-105">The primary purpose of navigation menu modules is to allow site users to browse products and site pages according to the channel navigation hierarchy defined in Dynamics 365 Commerce headquarters.</span></span> <span data-ttu-id="71613-106">Položky konfigurované v modulu navigační nabídky se zobrazují jako navigace v záhlaví webu.</span><span class="sxs-lookup"><span data-stu-id="71613-106">Items configured in a navigation menu module appear as site header navigation.</span></span> <span data-ttu-id="71613-107">Moduly navigační nabídky také podporují statické položky nabídky, které odkazují na jiné stránky na webu elektronického obchodu.</span><span class="sxs-lookup"><span data-stu-id="71613-107">Navigation menu modules also support static menu items that link to other pages on an e-Commerce site.</span></span>

<span data-ttu-id="71613-108">Modul navigační nabídky lze přidat do modulu záhlaví stránky.</span><span class="sxs-lookup"><span data-stu-id="71613-108">The navigation menu module can be added to the header module of a page.</span></span> <span data-ttu-id="71613-109">V motivu Fabrikam zobrazuje navigační nabídka ve výchozím nastavení dvě úrovně.</span><span class="sxs-lookup"><span data-stu-id="71613-109">In the Fabrikam theme, the navigation menu shows two levels by default.</span></span> <span data-ttu-id="71613-110">V motivu Starter zobrazuje navigační nabídka ve výchozím nastavení tři úrovně.</span><span class="sxs-lookup"><span data-stu-id="71613-110">In the Starter theme, the navigation menu shows three levels by default.</span></span> <span data-ttu-id="71613-111">Chcete-li změnit počet úrovní, je u motivu vyžadováno rozšíření zobrazení.</span><span class="sxs-lookup"><span data-stu-id="71613-111">To change to the number of levels, a view extension is required on the theme.</span></span>

<span data-ttu-id="71613-112">Následující obrázek ukazuje příklad navigační nabídky pro web Fabrikam se dvěma úrovněmi hierarchie kategorií a některými položkami statické nabídky.</span><span class="sxs-lookup"><span data-stu-id="71613-112">The following illustration shows an example of a navigation menu for the Fabrikam site with two levels of category hierarchy and some static menu items.</span></span>
<span data-ttu-id="71613-113">![Příklad modulu navigační nabídky](./media/ecommerce-header.png)</span><span class="sxs-lookup"><span data-stu-id="71613-113">![Example of a navigation meu module](./media/ecommerce-header.png)</span></span>

## <a name="navigation-menu-module-properties"></a><span data-ttu-id="71613-114">Vlastnosti modulu navigační nabídky</span><span class="sxs-lookup"><span data-stu-id="71613-114">Navigation menu module properties</span></span>

| <span data-ttu-id="71613-115">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="71613-115">Property name</span></span>             | <span data-ttu-id="71613-116">Hodnota</span><span class="sxs-lookup"><span data-stu-id="71613-116">Value</span></span>                 | <span data-ttu-id="71613-117">popis</span><span class="sxs-lookup"><span data-stu-id="71613-117">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="71613-118">Zdroj</span><span class="sxs-lookup"><span data-stu-id="71613-118">Source</span></span>                  | <span data-ttu-id="71613-119">**Maloobchod**, **Ruční vytváření**, **Maloobchod a ruční vytváření**</span><span class="sxs-lookup"><span data-stu-id="71613-119">**Retail**, **Manual authoring**, **Retail and manual authoring**</span></span> | <span data-ttu-id="71613-120">Hodnota **Maloobchod** umožňuje v navigační nabídce zobrazit hierarchii navigace sítě z centrály Commerce.</span><span class="sxs-lookup"><span data-stu-id="71613-120">The **Retail** value allows the channel navigation hierarchy from Commerce headquarters to be displayed on the navigation menu.</span></span> <span data-ttu-id="71613-121">Hodnota **Ruční vytváření** umožňuje doporučovat statické položky nabídky.</span><span class="sxs-lookup"><span data-stu-id="71613-121">The **Manual authoring** value allows static menu items to be curated.</span></span> <span data-ttu-id="71613-122">Hodnota **Maloobchod a ruční vyváření** umožňuje kombinaci obou.</span><span class="sxs-lookup"><span data-stu-id="71613-122">The **Retail and manual authoring** value allows a mix of both.</span></span> |
| <span data-ttu-id="71613-123">Zobrazení obrázků kategorií</span><span class="sxs-lookup"><span data-stu-id="71613-123">Show category images</span></span> | <span data-ttu-id="71613-124">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="71613-124">**True** or **False**</span></span>    | <span data-ttu-id="71613-125">Je-li povolena, tato vlastnost zobrazuje obrázky kategorií v navigační nabídce, jak je definováno v centrále Commerce pro každou kategorii.</span><span class="sxs-lookup"><span data-stu-id="71613-125">When enabled, this property displays category images on the navigation menu as defined in Commerce headquarters for each category.</span></span> <span data-ttu-id="71613-126">Přidáno v Comerce verze 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="71613-126">Added in Commerce release 10.0.14.</span></span> |
| <span data-ttu-id="71613-127">Zobrazit propagační akce</span><span class="sxs-lookup"><span data-stu-id="71613-127">Show promotions</span></span> | <span data-ttu-id="71613-128">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="71613-128">**True** or **False**</span></span> | <span data-ttu-id="71613-129">Když je tato vlastnost povolena, lze propagační akce konfigurovat pomocí obrázků, odkazů a textu.</span><span class="sxs-lookup"><span data-stu-id="71613-129">When this property is enabled, promotions can be configured by using images, links, and text.</span></span> <span data-ttu-id="71613-130">Tato vlastnost byla přidána ve verzi Commerce verze 10.0.17.</span><span class="sxs-lookup"><span data-stu-id="71613-130">This property was added in the Commerce version 10.0.17 release.</span></span> |
| <span data-ttu-id="71613-131">Přidejte propagační akce</span><span class="sxs-lookup"><span data-stu-id="71613-131">Add promotions</span></span> | <span data-ttu-id="71613-132">Text, obrázek nebo odkaz</span><span class="sxs-lookup"><span data-stu-id="71613-132">Text, image, or link</span></span> | <span data-ttu-id="71613-133">Když je povolena vlastnost **Zobrazit propagační akce**, můžete v navigační nabídce přidat text, obrázek nebo odkaz jako propagační obsah.</span><span class="sxs-lookup"><span data-stu-id="71613-133">When the **Show promotions** property is enabled, you can add text, an image, or a link as promotional content on the navigation menu.</span></span> |
| <span data-ttu-id="71613-134">Povolení navigační nabídky s více úrovněmi</span><span class="sxs-lookup"><span data-stu-id="71613-134">Enable multi-level navigation menu</span></span> | <span data-ttu-id="71613-135">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="71613-135">**True** or **False**</span></span> | <span data-ttu-id="71613-136">Když je tato vlastnost povolena, navigační nabídka může zobrazit více úrovní navigační hierarchie.</span><span class="sxs-lookup"><span data-stu-id="71613-136">When this property is enabled, the navigation menu can show multiple levels of the navigation hierarchy.</span></span> <span data-ttu-id="71613-137">Tato funkce je k dispozici v aplikaci Commerce verze 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="71613-137">This feature is available in the Commerce version 10.0.15 release.</span></span> |
| <span data-ttu-id="71613-138">Počet úrovní</span><span class="sxs-lookup"><span data-stu-id="71613-138">Number of levels</span></span> | <span data-ttu-id="71613-139">Celé číslo</span><span class="sxs-lookup"><span data-stu-id="71613-139">integer</span></span> | <span data-ttu-id="71613-140">Tato vlastnost definuje počet úrovní, které se mají zobrazit, pokud je vlastnost **Povolit navigační nabídku s více úrovněmi** je nastavena na **Pravda**.</span><span class="sxs-lookup"><span data-stu-id="71613-140">This property defines the numbers of levels that should be shown if the **Enable multilevel navigation menu** property is set to **True**.</span></span> |
| <span data-ttu-id="71613-141">Statická položka nabídky</span><span class="sxs-lookup"><span data-stu-id="71613-141">Static menu item</span></span>| <span data-ttu-id="71613-142">Pole hodnot</span><span class="sxs-lookup"><span data-stu-id="71613-142">Array of values</span></span>| <span data-ttu-id="71613-143">Statické položky nabídky, které přidružují název položky nabídky s odkazem na stránku statického webu.</span><span class="sxs-lookup"><span data-stu-id="71613-143">Static menu items that associate a menu item name with a link to a static site page.</span></span> <span data-ttu-id="71613-144">Položky nabídky můžete vytvořit pod dalšími položkami nabídky.</span><span class="sxs-lookup"><span data-stu-id="71613-144">You can create menu items below other menu items.</span></span> <span data-ttu-id="71613-145">Ve výchozím nastavení se statické nabídky zobrazují na kořenové úrovni a budou přidány do hierarchie navigace sítě, pokud existuje.</span><span class="sxs-lookup"><span data-stu-id="71613-145">By default, static menus appear at the root level and will be appended to the channel navigation hierarchy if it exists.</span></span> |
| <span data-ttu-id="71613-146">Zobrazení kořenové nabídky</span><span class="sxs-lookup"><span data-stu-id="71613-146">Show root menu</span></span> | <span data-ttu-id="71613-147">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="71613-147">**True** or **False**</span></span> | <span data-ttu-id="71613-148">Když je tato vlastnost povolena, lze navigační nabídku definovat pod vlastním kořenem (například **Koupit**).</span><span class="sxs-lookup"><span data-stu-id="71613-148">When this property is enabled, the navigation menu can be defined under a custom root (for example, **Shop now**).</span></span> <span data-ttu-id="71613-149">Tato funkce je k dispozici ve vydání Dynamics 365 Commerce 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="71613-149">This feature is available in the Dynamics 365 Commerce 10.0.15 release.</span></span> |
| <span data-ttu-id="71613-150">Kořenová nabídka</span><span class="sxs-lookup"><span data-stu-id="71613-150">Root menu</span></span> | <span data-ttu-id="71613-151">řetězec</span><span class="sxs-lookup"><span data-stu-id="71613-151">string</span></span> | <span data-ttu-id="71613-152">Tuto vlastnost lze použít k definování textu pro vlastní kořen, pokud je vlastnost **Zobrazit kořenovou nabídku** nastavena na **Pravda**.</span><span class="sxs-lookup"><span data-stu-id="71613-152">This property can be used to define text for a custom root if the **Show root menu** property is set to **True**.</span></span> |

<span data-ttu-id="71613-153">Následující obrázek ukazuje příklad obrázku kategorie zobrazeného v navigační nabídce pro web Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="71613-153">The following illustration shows an example of a category image displayed on the navigation menu for the Fabrikam site.</span></span>
<span data-ttu-id="71613-154">![Příklad modulu navigační nabídky s obrázky kategorií](./media/ecommerce-categoryimages.PNG)</span><span class="sxs-lookup"><span data-stu-id="71613-154">![Example of a navigation meu module with category images](./media/ecommerce-categoryimages.PNG)</span></span>

## <a name="add-a-navigation-menu-module-to-a-header-module"></a><span data-ttu-id="71613-155">Přidání modul navigační nabídky do modulu záhlaví</span><span class="sxs-lookup"><span data-stu-id="71613-155">Add a navigation menu module to a header module</span></span>

<span data-ttu-id="71613-156">Podrobnosti, jak přidat modul navigační nabídky do modulu záhlaví, viz [Modul záhlaví](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="71613-156">For details about how to add a navigation menu module to a header module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="71613-157">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="71613-157">Additional resources</span></span>

[<span data-ttu-id="71613-158">Přehled knihovny modulů</span><span class="sxs-lookup"><span data-stu-id="71613-158">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="71613-159">Modul popisu cesty</span><span class="sxs-lookup"><span data-stu-id="71613-159">Breadcrumb module</span></span>](add-breadcrumb.md)

[<span data-ttu-id="71613-160">Modul volby lokality</span><span class="sxs-lookup"><span data-stu-id="71613-160">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="71613-161">Modul buy boxu</span><span class="sxs-lookup"><span data-stu-id="71613-161">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="71613-162">Zásady zacházení se soubory cookie</span><span class="sxs-lookup"><span data-stu-id="71613-162">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="71613-163">Modul záhlaví</span><span class="sxs-lookup"><span data-stu-id="71613-163">Header module</span></span>](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]