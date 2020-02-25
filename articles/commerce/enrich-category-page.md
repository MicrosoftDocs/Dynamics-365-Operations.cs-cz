---
title: Obohacení cílové stránky kategorie
description: V tomto tématu je popsáno obohacování stránek kategorií v řešení Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 71348efba9fc1374b9e6599eb23f198d3851036e
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003043"
---
# <a name="enrich-a-category-landing-page"></a><span data-ttu-id="74d4a-103">Obohacení cílové stránky kategorie</span><span class="sxs-lookup"><span data-stu-id="74d4a-103">Enrich a category landing page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="74d4a-104">V tomto tématu je popsáno obohacování stránek kategorií v řešení Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="74d4a-104">This topic covers the enrichment of category pages in Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="74d4a-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="74d4a-105">Overview</span></span>

<span data-ttu-id="74d4a-106">Řešení Commerce poskytuje výchozí cílovou stránku kategorie, která se používá při zobrazení dat kategorie.</span><span class="sxs-lookup"><span data-stu-id="74d4a-106">Commerce provides a default category landing page that is used when category data is shown.</span></span> <span data-ttu-id="74d4a-107">Výchozí stránka kategorie obsahuje potřebné prvky, jako zpřesnění, umístění produktu zařazeného do kategorie, možnosti řazení, souhrn voleb a ovládací prvky stránkování.</span><span class="sxs-lookup"><span data-stu-id="74d4a-107">A default category page contains required elements, such as refiners, categorized product placement, sorting options, a choice summary, and pagination controls.</span></span> 

<span data-ttu-id="74d4a-108">Namísto použití výchozí stránky kategorie však můžete použít „obohacenou“ cílovou stránku kategorie s dalším obsahem a specifickými prvky.</span><span class="sxs-lookup"><span data-stu-id="74d4a-108">However, instead of using the default category page, you might want to use an "enriched" category landing page that has more content and more specific elements.</span></span> <span data-ttu-id="74d4a-109">Typické obohacení může zahrnovat přidání marketingového obchodního obsahu na stránku kategorie, které se týká.</span><span class="sxs-lookup"><span data-stu-id="74d4a-109">A typical enrichment might involve adding category-specific marketing content to the category page.</span></span> <span data-ttu-id="74d4a-110">Tento obsah může zahrnovat umístění produktu, který je součástí více kategorií, pro účely křížového prodeje, redakční seznamy, obrázky, videa a další text.</span><span class="sxs-lookup"><span data-stu-id="74d4a-110">This content might include cross-category product placement for cross-sell purposes, editorial lists, images, videos, and other text.</span></span> <span data-ttu-id="74d4a-111">Výchozí stránku kategorie můžete buď upravit, nebo definovat jinou stránku kategorie pro určitou kategorii.</span><span class="sxs-lookup"><span data-stu-id="74d4a-111">You can either modify the default category page or define a different category page for a specific category.</span></span>

![Obohacená cílová stránka kategorie](./media/CategoryLandingPages.png)

<span data-ttu-id="74d4a-113">Stránka **Produkt** v nástroji pro tvorbu obsahu zahrnuje seznam kategorií z daného kanálu, které jsou přiřazeny k danému webu.</span><span class="sxs-lookup"><span data-stu-id="74d4a-113">In the authoring tool, the **Product** page includes a list of categories from the channel that are assigned to the site.</span></span> <span data-ttu-id="74d4a-114">Je- li pro stránku kategorie vybrán stav **Obohaceno**, tato stránka kategorie byla obohacena.</span><span class="sxs-lookup"><span data-stu-id="74d4a-114">If the **Enriched** status is selected for a category page, that category page has been enriched.</span></span> <span data-ttu-id="74d4a-115">V opačném případě se pro kategorii použije výchozí stránka a obsah kategorie.</span><span class="sxs-lookup"><span data-stu-id="74d4a-115">Otherwise, the default category page and content are used for the category.</span></span> <span data-ttu-id="74d4a-116">Chcete-li zobrazit náhled obohacených i neobohacených stránek kategorie, vyberte název kategorie.</span><span class="sxs-lookup"><span data-stu-id="74d4a-116">You can preview both the enriched and non-enriched category pages for a category by selecting the category name.</span></span>

<span data-ttu-id="74d4a-117">Chcete-li obohatit stránku kategorie, postupujte podle následujících pokynů.</span><span class="sxs-lookup"><span data-stu-id="74d4a-117">To enrich a category page, do the following.</span></span>

1. <span data-ttu-id="74d4a-118">Na stránce **Produkty** vyberte název kategorie, jejíž stránku chcete obohatit.</span><span class="sxs-lookup"><span data-stu-id="74d4a-118">On the **Products** page, select the name of the category that you want to enrich the category page for.</span></span> <span data-ttu-id="74d4a-119">V editoru stránek se pro vybranou kategorii otevře výchozí stránka kategorie.</span><span class="sxs-lookup"><span data-stu-id="74d4a-119">The default category page for the selected category is opened in the page editor.</span></span>
2. <span data-ttu-id="74d4a-120">Vyberte **Obohatit stránku kategorie**.</span><span class="sxs-lookup"><span data-stu-id="74d4a-120">Select **Enrich category page**.</span></span>
3. <span data-ttu-id="74d4a-121">Vyberte šablonu pro obohacenou stránku kategorie.</span><span class="sxs-lookup"><span data-stu-id="74d4a-121">Select a template for the enriched category page.</span></span> <span data-ttu-id="74d4a-122">Pokud provádíte pouze drobné změny, můžete vybrat výchozí stránku kategorie.</span><span class="sxs-lookup"><span data-stu-id="74d4a-122">If you're making only minor changes, you can select the default category page.</span></span> <span data-ttu-id="74d4a-123">Případně můžete vybrat některou ze šablon stránek kategorie.</span><span class="sxs-lookup"><span data-stu-id="74d4a-123">Alternatively, you can select a specific category page template.</span></span> <span data-ttu-id="74d4a-124">Když vyberete šablonu, otevře se editor stránek a vybraná šablona se použije k vytvoření nové stránky kategorie pro vybranou kategorii.</span><span class="sxs-lookup"><span data-stu-id="74d4a-124">When you select the template, the page editor is opened, and the selected template is used to create a new category page for the selected category.</span></span> <span data-ttu-id="74d4a-125">Stránka je pro vás rezervována a nyní můžete provést změny.</span><span class="sxs-lookup"><span data-stu-id="74d4a-125">The page is checked out to you, and you can now make your changes.</span></span>

> [!NOTE]
> <span data-ttu-id="74d4a-126">Moduly, které používají data specifikace kategorie, používají data z vybrané kategorie.</span><span class="sxs-lookup"><span data-stu-id="74d4a-126">Modules that use category specification data use the data from your selected category.</span></span>
>
> <span data-ttu-id="74d4a-127">Nastavení šablony, kterou vyberete, určuje změny, které lze provést.</span><span class="sxs-lookup"><span data-stu-id="74d4a-127">The settings of the template that you select determine the changes that you can make.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="74d4a-128">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="74d4a-128">Additional resources</span></span>

[<span data-ttu-id="74d4a-129">Úprava existující webové stránky</span><span class="sxs-lookup"><span data-stu-id="74d4a-129">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="74d4a-130">Přidání nové webové stránky</span><span class="sxs-lookup"><span data-stu-id="74d4a-130">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="74d4a-131">Výběr rozvržení stránky</span><span class="sxs-lookup"><span data-stu-id="74d4a-131">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="74d4a-132">Správa metadat SEO</span><span class="sxs-lookup"><span data-stu-id="74d4a-132">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="74d4a-133">Uložení, náhled a publikování stránky</span><span class="sxs-lookup"><span data-stu-id="74d4a-133">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="74d4a-134">Obohacení stránky produktu</span><span class="sxs-lookup"><span data-stu-id="74d4a-134">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="74d4a-135">Ověření přístupnosti obsahu stránky</span><span class="sxs-lookup"><span data-stu-id="74d4a-135">Verify page content accessibility</span></span>](verify-accessibility.md)
