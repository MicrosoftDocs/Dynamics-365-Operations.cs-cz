---
title: Modul navigační nabídky
description: Tohle téma se zabývá moduly navigační nabídky a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
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
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 91239bd1db3f5819b7ad8d45ccfd8ab0d88b1b41
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817867"
---
# <a name="navigation-menu-module"></a><span data-ttu-id="970e2-103">Modul navigační nabídky</span><span class="sxs-lookup"><span data-stu-id="970e2-103">Navigation menu module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="970e2-104">Tohle téma se zabývá moduly navigační nabídky a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="970e2-104">This topic covers navigation menu modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="970e2-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="970e2-105">Overview</span></span>

<span data-ttu-id="970e2-106">Primárním účelem modulů navigační nabídky je umožnit uživatelům webu procházet produkty a stránky webu podle hierarchie navigace sítě definované v centrále Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="970e2-106">The primary purpose of navigation menu modules is to allow site users to browse products and site pages according to the channel navigation hierarchy defined in Dynamics 365 Commerce headquarters.</span></span> <span data-ttu-id="970e2-107">Položky konfigurované v modulu navigační nabídky se zobrazují jako navigace v záhlaví webu.</span><span class="sxs-lookup"><span data-stu-id="970e2-107">Items configured in a navigation menu module appear as site header navigation.</span></span> <span data-ttu-id="970e2-108">Moduly navigační nabídky také podporují statické položky nabídky, které odkazují na jiné stránky na webu elektronického obchodu.</span><span class="sxs-lookup"><span data-stu-id="970e2-108">Navigation menu modules also support static menu items that link to other pages on an e-Commerce site.</span></span>

<span data-ttu-id="970e2-109">Modul navigační nabídky lze přidat do modulu záhlaví stránky.</span><span class="sxs-lookup"><span data-stu-id="970e2-109">The navigation menu module can be added to the header module of a page.</span></span> <span data-ttu-id="970e2-110">V motivu Fabrikam zobrazuje navigační nabídka ve výchozím nastavení dvě úrovně.</span><span class="sxs-lookup"><span data-stu-id="970e2-110">In the Fabrikam theme, the navigation menu shows two levels by default.</span></span> <span data-ttu-id="970e2-111">V motivu Starter zobrazuje navigační nabídka ve výchozím nastavení tři úrovně.</span><span class="sxs-lookup"><span data-stu-id="970e2-111">In the Starter theme, the navigation menu shows three levels by default.</span></span> <span data-ttu-id="970e2-112">Chcete-li změnit počet úrovní, je u motivu vyžadováno rozšíření zobrazení.</span><span class="sxs-lookup"><span data-stu-id="970e2-112">To change to the number of levels, a view extension is required on the theme.</span></span>

<span data-ttu-id="970e2-113">Následující obrázek ukazuje příklad navigační nabídky pro web Fabrikam se dvěma úrovněmi hierarchie kategorií a některými položkami statické nabídky.</span><span class="sxs-lookup"><span data-stu-id="970e2-113">The following illustration shows an example of a navigation menu for the Fabrikam site with two levels of category hierarchy and some static menu items.</span></span>
<span data-ttu-id="970e2-114">![Příklad modulu navigační nabídky](./media/ecommerce-header.png)</span><span class="sxs-lookup"><span data-stu-id="970e2-114">![Example of a navigation meu module](./media/ecommerce-header.png)</span></span>

## <a name="navigation-menu-module-properties"></a><span data-ttu-id="970e2-115">Vlastnosti modulu navigační nabídky</span><span class="sxs-lookup"><span data-stu-id="970e2-115">Navigation menu module properties</span></span>

| <span data-ttu-id="970e2-116">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="970e2-116">Property name</span></span>             | <span data-ttu-id="970e2-117">Hodnota</span><span class="sxs-lookup"><span data-stu-id="970e2-117">Value</span></span>                 | <span data-ttu-id="970e2-118">popis</span><span class="sxs-lookup"><span data-stu-id="970e2-118">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="970e2-119">Zdroj</span><span class="sxs-lookup"><span data-stu-id="970e2-119">Source</span></span>                  | <span data-ttu-id="970e2-120">**Maloobchod**, **Ruční vytváření**, **Maloobchod a ruční vytváření**</span><span class="sxs-lookup"><span data-stu-id="970e2-120">**Retail**, **Manual authoring**, **Retail and manual authoring**</span></span> | <span data-ttu-id="970e2-121">Hodnota **Maloobchod** umožňuje v navigační nabídce zobrazit hierarchii navigace sítě z centrály Commerce.</span><span class="sxs-lookup"><span data-stu-id="970e2-121">The **Retail** value allows the channel navigation hierarchy from Commerce headquarters to be displayed on the navigation menu.</span></span> <span data-ttu-id="970e2-122">Hodnota **Ruční vytváření** umožňuje doporučovat statické položky nabídky.</span><span class="sxs-lookup"><span data-stu-id="970e2-122">The **Manual authoring** value allows static menu items to be curated.</span></span> <span data-ttu-id="970e2-123">Hodnota **Maloobchod a ruční vyváření** umožňuje kombinaci obou.</span><span class="sxs-lookup"><span data-stu-id="970e2-123">The **Retail and manual authoring** value allows a mix of both.</span></span> |
| <span data-ttu-id="970e2-124">Zobrazení obrázků kategorií</span><span class="sxs-lookup"><span data-stu-id="970e2-124">Show category images</span></span> | <span data-ttu-id="970e2-125">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="970e2-125">**True** or **False**</span></span>    | <span data-ttu-id="970e2-126">Je-li povolena, tato vlastnost zobrazuje obrázky kategorií v navigační nabídce, jak je definováno v centrále Commerce pro každou kategorii.</span><span class="sxs-lookup"><span data-stu-id="970e2-126">When enabled, this property displays category images on the navigation menu as defined in Commerce headquarters for each category.</span></span> <span data-ttu-id="970e2-127">Přidáno v Comerce verze 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="970e2-127">Added in Commerce release 10.0.14.</span></span> |
| <span data-ttu-id="970e2-128">Statická položka nabídky</span><span class="sxs-lookup"><span data-stu-id="970e2-128">Static menu item</span></span>| <span data-ttu-id="970e2-129">Pole hodnot</span><span class="sxs-lookup"><span data-stu-id="970e2-129">Array of values</span></span>| <span data-ttu-id="970e2-130">Statické položky nabídky, které přidružují název položky nabídky s odkazem na stránku statického webu.</span><span class="sxs-lookup"><span data-stu-id="970e2-130">Static menu items that associate a menu item name with a link to a static site page.</span></span> <span data-ttu-id="970e2-131">Položky nabídky můžete vytvořit pod dalšími položkami nabídky.</span><span class="sxs-lookup"><span data-stu-id="970e2-131">You can create menu items below other menu items.</span></span> <span data-ttu-id="970e2-132">Ve výchozím nastavení se statické nabídky zobrazují na kořenové úrovni a budou přidány do hierarchie navigace sítě, pokud existuje.</span><span class="sxs-lookup"><span data-stu-id="970e2-132">By default, static menus appear at the root level and will be appended to the channel navigation hierarchy if it exists.</span></span> |

<span data-ttu-id="970e2-133">Následující obrázek ukazuje příklad obrázku kategorie zobrazeného v navigační nabídce pro web Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="970e2-133">The following illustration shows an example of a category image displayed on the navigation menu for the Fabrikam site.</span></span>
<span data-ttu-id="970e2-134">![Příklad modulu navigační nabídky s obrázky kategorií](./media/ecommerce-categoryimages.PNG)</span><span class="sxs-lookup"><span data-stu-id="970e2-134">![Example of a navigation meu module with category images](./media/ecommerce-categoryimages.PNG)</span></span>

## <a name="add-a-navigation-menu-module-to-a-header-module"></a><span data-ttu-id="970e2-135">Přidání modul navigační nabídky do modulu záhlaví</span><span class="sxs-lookup"><span data-stu-id="970e2-135">Add a navigation menu module to a header module</span></span>

<span data-ttu-id="970e2-136">Podrobnosti, jak přidat modul navigační nabídky do modulu záhlaví, viz [Modul záhlaví](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="970e2-136">For details about how to add a navigation menu module to a header module, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="970e2-137">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="970e2-137">Additional resources</span></span>

[<span data-ttu-id="970e2-138">Přehled knihovny modulů</span><span class="sxs-lookup"><span data-stu-id="970e2-138">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="970e2-139">Modul buy boxu</span><span class="sxs-lookup"><span data-stu-id="970e2-139">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="970e2-140">Zásady zacházení se soubory cookie</span><span class="sxs-lookup"><span data-stu-id="970e2-140">Cookie compliance</span></span>](cookie-compliance.md)

[<span data-ttu-id="970e2-141">Modul záhlaví</span><span class="sxs-lookup"><span data-stu-id="970e2-141">Header module</span></span>](author-header-module.md)
