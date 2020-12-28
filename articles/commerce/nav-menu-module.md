---
title: Modul navigační nabídky
description: Tohle téma se zabývá moduly navigační nabídky a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/01/2020
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
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: b0e8168ca9ec9ca68011650a73cc09983deca645
ms.sourcegitcommit: eee3523be26369aecdb36c0143a6ee3dab4b7966
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/20/2020
ms.locfileid: "4410919"
---
# <a name="navigation-menu-module"></a><span data-ttu-id="3d2a9-103">Modul navigační nabídky</span><span class="sxs-lookup"><span data-stu-id="3d2a9-103">Navigation menu module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3d2a9-104">Tohle téma se zabývá moduly navigační nabídky a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3d2a9-104">This topic covers navigation menu modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="3d2a9-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="3d2a9-105">Overview</span></span>

<span data-ttu-id="3d2a9-106">Primárním účelem modulů navigační nabídky je umožnit uživatelům webu procházet produkty a stránky webu podle hierarchie navigace sítě definované v centrále Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3d2a9-106">The primary purpose of navigation menu modules is to allow site users to browse products and site pages according to the channel navigation hierarchy defined in Dynamics 365 Commerce headquarters.</span></span> <span data-ttu-id="3d2a9-107">Položky konfigurované v modulu navigační nabídky se zobrazují jako navigace v záhlaví webu.</span><span class="sxs-lookup"><span data-stu-id="3d2a9-107">Items configured in a navigation menu module appear as site header navigation.</span></span> <span data-ttu-id="3d2a9-108">Moduly navigační nabídky také podporují statické položky nabídky, které odkazují na jiné stránky na webu elektronického obchodu.</span><span class="sxs-lookup"><span data-stu-id="3d2a9-108">Navigation menu modules also support static menu items that link to other pages on an e-Commerce site.</span></span>

<span data-ttu-id="3d2a9-109">Modul navigační nabídky lze přidat do modulu záhlaví stránky.</span><span class="sxs-lookup"><span data-stu-id="3d2a9-109">The navigation menu module can be added to the header module of a page.</span></span> <span data-ttu-id="3d2a9-110">V motivu Fabrikam zobrazuje navigační nabídka ve výchozím nastavení dvě úrovně.</span><span class="sxs-lookup"><span data-stu-id="3d2a9-110">In the Fabrikam theme, the navigation menu shows two levels by default.</span></span> <span data-ttu-id="3d2a9-111">V motivu Starter zobrazuje navigační nabídka ve výchozím nastavení tři úrovně.</span><span class="sxs-lookup"><span data-stu-id="3d2a9-111">In the Starter theme, the navigation menu shows three levels by default.</span></span> <span data-ttu-id="3d2a9-112">Chcete-li změnit počet úrovní, je u motivu vyžadováno rozšíření zobrazení.</span><span class="sxs-lookup"><span data-stu-id="3d2a9-112">To change to the number of levels, a view extension is required on the theme.</span></span>

<span data-ttu-id="3d2a9-113">Následující obrázek ukazuje příklad navigační nabídky pro web Fabrikam se dvěma úrovněmi hierarchie kategorií a některými položkami statické nabídky.</span><span class="sxs-lookup"><span data-stu-id="3d2a9-113">The following illustration shows an example of a navigation menu for the Fabrikam site with two levels of category hierarchy and some static menu items.</span></span>
<span data-ttu-id="3d2a9-114">![Příklad modulu navigační nabídky](./media/ecommerce-header.png)</span><span class="sxs-lookup"><span data-stu-id="3d2a9-114">![Example of a navigation meu module](./media/ecommerce-header.png)</span></span>

## <a name="navigation-menu-module-properties"></a><span data-ttu-id="3d2a9-115">Vlastnosti modulu navigační nabídky</span><span class="sxs-lookup"><span data-stu-id="3d2a9-115">Navigation menu module properties</span></span>

| <span data-ttu-id="3d2a9-116">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="3d2a9-116">Property name</span></span>             | <span data-ttu-id="3d2a9-117">Hodnota</span><span class="sxs-lookup"><span data-stu-id="3d2a9-117">Value</span></span>                 | <span data-ttu-id="3d2a9-118">popis</span><span class="sxs-lookup"><span data-stu-id="3d2a9-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="3d2a9-119">Zdroj</span><span class="sxs-lookup"><span data-stu-id="3d2a9-119">Source</span></span>                  | <span data-ttu-id="3d2a9-120">**Maloobchod**, **Ruční vytváření**, **Maloobchod a ruční vytváření**</span><span class="sxs-lookup"><span data-stu-id="3d2a9-120">**Retail**, **Manual authoring**, **Retail and manual authoring**</span></span> | <span data-ttu-id="3d2a9-121">Hodnota **Maloobchod** umožňuje v navigační nabídce zobrazit hierarchii navigace sítě z centrály Commerce.</span><span class="sxs-lookup"><span data-stu-id="3d2a9-121">The **Retail** value allows the channel navigation hierarchy from Commerce headquarters to be displayed on the navigation menu.</span></span> <span data-ttu-id="3d2a9-122">Hodnota **Ruční vytváření** umožňuje doporučovat statické položky nabídky.</span><span class="sxs-lookup"><span data-stu-id="3d2a9-122">The **Manual authoring** value allows static menu items to be curated.</span></span> <span data-ttu-id="3d2a9-123">Hodnota **Maloobchod a ruční vyváření** umožňuje kombinaci obou.</span><span class="sxs-lookup"><span data-stu-id="3d2a9-123">The **Retail and manual authoring** value allows a mix of both.</span></span> |
| <span data-ttu-id="3d2a9-124">Zobrazení obrázků kategorií</span><span class="sxs-lookup"><span data-stu-id="3d2a9-124">Show category images</span></span> | <span data-ttu-id="3d2a9-125">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="3d2a9-125">**True** or **False**</span></span>    | <span data-ttu-id="3d2a9-126">Je-li povolena, tato vlastnost zobrazuje obrázky kategorií v navigační nabídce, jak je definováno v centrále Commerce pro každou kategorii.</span><span class="sxs-lookup"><span data-stu-id="3d2a9-126">When enabled, this property displays category images on the navigation menu as defined in Commerce headquarters for each category.</span></span> <span data-ttu-id="3d2a9-127">Přidáno v Comerce verze 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="3d2a9-127">Added in Commerce release 10.0.14.</span></span> |
| <span data-ttu-id="3d2a9-128">Povolení navigační nabídky s více úrovněmi</span><span class="sxs-lookup"><span data-stu-id="3d2a9-128">Enable multi-level navigation menu</span></span> | <span data-ttu-id="3d2a9-129">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="3d2a9-129">**True** or **False**</span></span> | <span data-ttu-id="3d2a9-130">Když je tato vlastnost povolena, navigační nabídka může zobrazit více úrovní navigační hierarchie.</span><span class="sxs-lookup"><span data-stu-id="3d2a9-130">When this property is enabled, the navigation menu can show multiple levels of the navigation hierarchy.</span></span> <span data-ttu-id="3d2a9-131">Tato funkce je k dispozici ve vydání Dynamics 365 Commerce 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="3d2a9-131">This feature is available in the Dynamics 365 Commerce 10.0.15 release.</span></span> |
| <span data-ttu-id="3d2a9-132">Počet úrovní</span><span class="sxs-lookup"><span data-stu-id="3d2a9-132">Number of levels</span></span> | <span data-ttu-id="3d2a9-133">Celé číslo</span><span class="sxs-lookup"><span data-stu-id="3d2a9-133">integer</span></span> | <span data-ttu-id="3d2a9-134">Tato vlastnost definuje počet úrovní, které se mají zobrazit, pokud je vlastnost **Povolit navigační nabídku s více úrovněmi** je nastavena na **Pravda**.</span><span class="sxs-lookup"><span data-stu-id="3d2a9-134">This property defines the numbers of levels that should be shown if the **Enable multilevel navigation menu** property is set to **True**.</span></span> |
| <span data-ttu-id="3d2a9-135">Statická položka nabídky</span><span class="sxs-lookup"><span data-stu-id="3d2a9-135">Static menu item</span></span>| <span data-ttu-id="3d2a9-136">Pole hodnot</span><span class="sxs-lookup"><span data-stu-id="3d2a9-136">Array of values</span></span>| <span data-ttu-id="3d2a9-137">Statické položky nabídky, které přidružují název položky nabídky s odkazem na stránku statického webu.</span><span class="sxs-lookup"><span data-stu-id="3d2a9-137">Static menu items that associate a menu item name with a link to a static site page.</span></span> <span data-ttu-id="3d2a9-138">Položky nabídky můžete vytvořit pod dalšími položkami nabídky.</span><span class="sxs-lookup"><span data-stu-id="3d2a9-138">You can create menu items below other menu items.</span></span> <span data-ttu-id="3d2a9-139">Ve výchozím nastavení se statické nabídky zobrazují na kořenové úrovni a budou přidány do hierarchie navigace sítě, pokud existuje.</span><span class="sxs-lookup"><span data-stu-id="3d2a9-139">By default, static menus appear at the root level and will be appended to the channel navigation hierarchy if it exists.</span></span> |
| <span data-ttu-id="3d2a9-140">Zobrazení kořenové nabídky</span><span class="sxs-lookup"><span data-stu-id="3d2a9-140">Show root menu</span></span> | <span data-ttu-id="3d2a9-141">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="3d2a9-141">**True** or **False**</span></span> | <span data-ttu-id="3d2a9-142">Když je tato vlastnost povolena, lze navigační nabídku definovat pod vlastním kořenem (například **Koupit**).</span><span class="sxs-lookup"><span data-stu-id="3d2a9-142">When this property is enabled, the navigation menu can be defined under a custom root (for example, **Shop now**).</span></span> <span data-ttu-id="3d2a9-143">Tato funkce je k dispozici ve vydání Dynamics 365 Commerce 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="3d2a9-143">This feature is available in the Dynamics 365 Commerce 10.0.15 release.</span></span> |
| <span data-ttu-id="3d2a9-144">Kořenová nabídka</span><span class="sxs-lookup"><span data-stu-id="3d2a9-144">Root menu</span></span> | <span data-ttu-id="3d2a9-145">řetězec</span><span class="sxs-lookup"><span data-stu-id="3d2a9-145">string</span></span> | <span data-ttu-id="3d2a9-146">Tuto vlastnost lze použít k definování textu pro vlastní kořen, pokud je vlastnost **Zobrazit kořenovou nabídku** nastavena na **Pravda**.</span><span class="sxs-lookup"><span data-stu-id="3d2a9-146">This property can be used to define text for a custom root if the **Show root menu** property is set to **True**.</span></span> |

<span data-ttu-id="3d2a9-147">Následující obrázek ukazuje příklad obrázku kategorie zobrazeného v navigační nabídce pro web Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="3d2a9-147">The following illustration shows an example of a category image displayed on the navigation menu for the Fabrikam site.</span></span>
<span data-ttu-id="3d2a9-148">![Příklad modulu navigační nabídky s obrázky kategorií](./media/ecommerce-categoryimages.PNG)</span><span class="sxs-lookup"><span data-stu-id="3d2a9-148">![Example of a navigation meu module with category images](./media/ecommerce-categoryimages.PNG)</span></span>

## <a name="add-a-navigation-menu-module-to-a-header-module"></a><span data-ttu-id="3d2a9-149">Přidání modul navigační nabídky do modulu záhlaví</span><span class="sxs-lookup"><span data-stu-id="3d2a9-149">Add a navigation menu module to a header module</span></span>

<span data-ttu-id="3d2a9-150">Podrobnosti, jak přidat modul navigační nabídky do modulu záhlaví, viz [Modul záhlaví](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="3d2a9-150">For details about how to add a navigation menu module to a header module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3d2a9-151">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="3d2a9-151">Additional resources</span></span>

[<span data-ttu-id="3d2a9-152">Přehled knihovny modulů</span><span class="sxs-lookup"><span data-stu-id="3d2a9-152">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="3d2a9-153">Modul popisu cesty</span><span class="sxs-lookup"><span data-stu-id="3d2a9-153">Breadcrumb module</span></span>](add-breadcrumb.md)

[<span data-ttu-id="3d2a9-154">Modul volby lokality</span><span class="sxs-lookup"><span data-stu-id="3d2a9-154">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="3d2a9-155">Modul buy boxu</span><span class="sxs-lookup"><span data-stu-id="3d2a9-155">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="3d2a9-156">Zásady zacházení se soubory cookie</span><span class="sxs-lookup"><span data-stu-id="3d2a9-156">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="3d2a9-157">Modul záhlaví</span><span class="sxs-lookup"><span data-stu-id="3d2a9-157">Header module</span></span>](author-header-module.md)
