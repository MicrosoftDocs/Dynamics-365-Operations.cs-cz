---
title: Modul výsledků hledání
description: Tohle téma se zabývá moduly výsledků hledání a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3761be29955458099d01f2271057884fc1fd6f28
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/01/2021
ms.locfileid: "5097171"
---
# <a name="search-results-module"></a><span data-ttu-id="380b6-103">Modul výsledků hledání</span><span class="sxs-lookup"><span data-stu-id="380b6-103">Search results module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="380b6-104">Tohle téma se zabývá moduly výsledků hledání a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="380b6-104">This topic covers search results modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="380b6-105">Modul výsledků vyhledávání vrátí výsledky vyhledávání produktů a seznam příslušných zpřesnění pro produkty.</span><span class="sxs-lookup"><span data-stu-id="380b6-105">The search results module returns product search results and a list of applicable refiners for the products.</span></span> <span data-ttu-id="380b6-106">Moduly výsledků hledání na webech Dynamics 365 Commerce lze použít k vykreslení stránek pro následující scénáře:</span><span class="sxs-lookup"><span data-stu-id="380b6-106">Search results modules on Dynamics 365 Commerce sites can be used to render pages for the following scenarios:</span></span>

- <span data-ttu-id="380b6-107">Výsledky vyhledávání, které jsou spuštěny vyhledáváním uživatelů</span><span class="sxs-lookup"><span data-stu-id="380b6-107">Search results that are initiated by a user search</span></span>
- <span data-ttu-id="380b6-108">Výsledky vyhledávání, které zobrazují konkrétní sadu produktů, například „Nakupujte podobný vzhled“</span><span class="sxs-lookup"><span data-stu-id="380b6-108">Search results that show a specific set of products, such as "Shop similar looks"</span></span>
- <span data-ttu-id="380b6-109">Seznamy produktů, které patří do kategorie</span><span class="sxs-lookup"><span data-stu-id="380b6-109">Lists of products that belong to a category</span></span>

<span data-ttu-id="380b6-110">Další informace o kategoriích a stránkách s výsledky vyhledávání najdete v části [Výchozí cílová stránka kategorie a přehled stránky s výsledky vyhledávání](category-search-page-overview.md).</span><span class="sxs-lookup"><span data-stu-id="380b6-110">For more information about category and search results pages, see [Default category landing page and search results page overview](category-search-page-overview.md).</span></span>

<span data-ttu-id="380b6-111">Následující obrázek ukazuje příklad stránky výsledků hledání pro kategorii na webu Fabrikam.</span><span class="sxs-lookup"><span data-stu-id="380b6-111">The following illustration shows an example of a search results page for a category on the Fabrikam site.</span></span>

![Příklad stránky výsledků vyhledávání na webu Fabrikam](./media/SimpleCategoryLandingDressCategory.png)

## <a name="search-results-module-properties"></a><span data-ttu-id="380b6-113">Vlastnosti modulu výsledků hledání</span><span class="sxs-lookup"><span data-stu-id="380b6-113">Search results module properties</span></span>

<span data-ttu-id="380b6-114">V následující tabulce jsou uvedeny vlastnosti modulů výsledků hledání spolu s jejich hodnotami a popisy.</span><span class="sxs-lookup"><span data-stu-id="380b6-114">The following table lists the properties of search result modules, together with their values and descriptions.</span></span>

| <span data-ttu-id="380b6-115">Vlastnost</span><span class="sxs-lookup"><span data-stu-id="380b6-115">Property</span></span> | <span data-ttu-id="380b6-116">Hodnoty</span><span class="sxs-lookup"><span data-stu-id="380b6-116">Values</span></span> | <span data-ttu-id="380b6-117">popis</span><span class="sxs-lookup"><span data-stu-id="380b6-117">Description</span></span> |
|----------|--------|-------------|
| <span data-ttu-id="380b6-118">Počet položek na stránku</span><span class="sxs-lookup"><span data-stu-id="380b6-118">Items per page</span></span> | <span data-ttu-id="380b6-119">Celé číslo</span><span class="sxs-lookup"><span data-stu-id="380b6-119">Integer</span></span> | <span data-ttu-id="380b6-120">Počet položek, které by měly být zobrazeny na každé stránce.</span><span class="sxs-lookup"><span data-stu-id="380b6-120">The number of items that should be shown on each page.</span></span> |
| <span data-ttu-id="380b6-121">Povolit zpět na PDP</span><span class="sxs-lookup"><span data-stu-id="380b6-121">Allow back on PDP</span></span> | <span data-ttu-id="380b6-122">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="380b6-122">**True** or **False**</span></span> | <span data-ttu-id="380b6-123">Pokud je tato vlastnost nastavena na **True**, když uživatel vybere produkt na stránce s výsledky vyhledávání, navigace s popisem cesty na stránce s podrobnostmi o produktu (PDP), která je otevřena, zobrazí odkaz „Zpět na výsledky“.</span><span class="sxs-lookup"><span data-stu-id="380b6-123">If this property is set to **True**, when a user selects a product on the search results page, the breadcrumb navigation on the product details page (PDP) that is opened will show a "Back to results" link.</span></span> |
| <span data-ttu-id="380b6-124">Rozbalit zpřesnění</span><span class="sxs-lookup"><span data-stu-id="380b6-124">Expand Refiners</span></span> | <span data-ttu-id="380b6-125">**Všechno**, **1**, **2**, **3** nebo **4**</span><span class="sxs-lookup"><span data-stu-id="380b6-125">**All**, **1**, **2**, **3**, or **4**</span></span> | <span data-ttu-id="380b6-126">Počet nejlepších upřesnění, které by se měly při načtení stránky rozšířit.</span><span class="sxs-lookup"><span data-stu-id="380b6-126">The number of top refiners that should be expanded when a page is loaded.</span></span> <span data-ttu-id="380b6-127">Například, pokud je tato vlastnost nastavena na **3**, budou rozbaleny první tři upřesnění na stránce.</span><span class="sxs-lookup"><span data-stu-id="380b6-127">For example, if this property is set to **3**, the first three refiners on the page will be expanded.</span></span> |
| <span data-ttu-id="380b6-128">Skrýt zobrazení hierarchie kategorií</span><span class="sxs-lookup"><span data-stu-id="380b6-128">Hide category hierarchy display</span></span> | <span data-ttu-id="380b6-129">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="380b6-129">**True** or **False**</span></span> | <span data-ttu-id="380b6-130">Pokud je tato vlastnost nastavena na **True**, zobrazení hierarchie kategorií na stránce bude skryto.</span><span class="sxs-lookup"><span data-stu-id="380b6-130">If this property is set to **True**, the category hierarchy display on the page will be hidden.</span></span> <span data-ttu-id="380b6-131">Tato vlastnost by měla být nastavena na **True**, pokud používáte [modul popisu cesty](add-breadcrumb.md) pro zobrazení hierarchie kategorií.</span><span class="sxs-lookup"><span data-stu-id="380b6-131">This property should be set to **True** if you're using the [breadcrumb module](add-breadcrumb.md) to show the category hierarchy.</span></span>|
| <span data-ttu-id="380b6-132">Zahrnout do výsledků vyhledávání atributy produktu</span><span class="sxs-lookup"><span data-stu-id="380b6-132">Include product attributes in search results</span></span> | <span data-ttu-id="380b6-133">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="380b6-133">**True** or **False**</span></span> | <span data-ttu-id="380b6-134">Pokud je tato vlastnost nastavena na **True**, budou vráceny atributy produktů ve výsledcích hledání.</span><span class="sxs-lookup"><span data-stu-id="380b6-134">If this property is set to **True**, attributes will be returned for the products in the search results.</span></span> <span data-ttu-id="380b6-135">Ačkoli tyto atributy lze zobrazit na webu Commerce, je nutné rozšíření.</span><span class="sxs-lookup"><span data-stu-id="380b6-135">Although these attributes can be shown on a Commerce site, an extension is required.</span></span>|
| <span data-ttu-id="380b6-136">Zobrazit ceny na pobočkách</span><span class="sxs-lookup"><span data-stu-id="380b6-136">Show affiliation prices</span></span> | <span data-ttu-id="380b6-137">**Pravda** nebo **nepravda**</span><span class="sxs-lookup"><span data-stu-id="380b6-137">**True** or **False**</span></span> | <span data-ttu-id="380b6-138">Pokud je tato vlastnost nastavena na **True**, ceny umístění pro produkty se zobrazí ve výsledcích vyhledávání, když přihlášený uživatel prochází stránku.</span><span class="sxs-lookup"><span data-stu-id="380b6-138">If this property is set to **True**, affiliation prices for products will be shown in the search results when a signed-in user browses the page.</span></span> |

> [!IMPORTANT]
> <span data-ttu-id="380b6-139">V Dynamics 365 Commerce verze 10.0.16 a novější lze konfiguraci **Zobrazit ceny umístění** použít k zobrazení cen umístění na stránce.</span><span class="sxs-lookup"><span data-stu-id="380b6-139">In the Dynamics 365 Commerce 10.0.16 release and later, the **Show affiliation prices** configuration can be used to show affiliation prices on the page.</span></span>

## <a name="supported-modules"></a><span data-ttu-id="380b6-140">Podporované moduly</span><span class="sxs-lookup"><span data-stu-id="380b6-140">Supported modules</span></span>

<span data-ttu-id="380b6-141">Modul výsledků vyhledávání podporuje [modul rychlého zobrazení](quick-view-module.md), který umožňuje uživatelům prohlížet informace o produktu a přidávat položky do košíku ze stránky výsledků vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="380b6-141">The search results module supports the [quick view module](quick-view-module.md), which lets users view product information and add items to the cart from the search results page.</span></span>

## <a name="add-a-search-results-module-to-a-category-page"></a><span data-ttu-id="380b6-142">Přidat modul výsledků vyhledávání na stránku kategorie</span><span class="sxs-lookup"><span data-stu-id="380b6-142">Add a search results module to a category page</span></span>

<span data-ttu-id="380b6-143">Chcete-li přidat modul výsledků vyhledávání na stránku kategorie, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="380b6-143">To add a search results module to a category page, follow these steps.</span></span>

1. <span data-ttu-id="380b6-144">Přejděte na **Šablony** a poté volbou **Nová** vytvořte novou šablonu.</span><span class="sxs-lookup"><span data-stu-id="380b6-144">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="380b6-145">V dialogovém okně **Nová šablona** zadejte název **Výsledků vyhledávání** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="380b6-145">In the **New template** dialog box, enter the name **Search results**, and then select **OK**.</span></span>
1. <span data-ttu-id="380b6-146">V pozici **Tělo** vyberte tři tečky (...) a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="380b6-146">In the **Body** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="380b6-147">V dialogovém okně **Přidat modul** vyberte modul **Výchozí stránka** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="380b6-147">In the **Add Module** dialog box, select the **Default Page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="380b6-148">V pozici **Hlavní** modulu **Výchozí stránka** vyberte tlačítko se třemi tečkami (...) a vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="380b6-148">In the **Main** slot of the **Default Page** module, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="380b6-149">V dialogovém okně **Přidat modul** vyberte modul **Kontejner** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="380b6-149">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="380b6-150">V pozici **Kontejner** vyberte tři tečky (...) a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="380b6-150">In the **Container** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="380b6-151">V dialogovém okně **Přidat modul** vyberte modul **Popis cesty** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="380b6-151">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="380b6-152">V podokně vlastností **Popis cesty** zadejte hodnotu **1** pro **Min. počet výskytů**.</span><span class="sxs-lookup"><span data-stu-id="380b6-152">In the **Breadcrumb** properties pane, enter the value **1** for **Min Occurs**.</span></span>
1. <span data-ttu-id="380b6-153">V pozici **Kontejner** vyberte tři tečky (...) a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="380b6-153">In the **Container** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="380b6-154">V dialogovém okně **Přidat modul** vyberte modul **Výsledky vyhledávání** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="380b6-154">In the **Add Module** dialog box, select the **Search results** module, and then select **OK**.</span></span>
1. <span data-ttu-id="380b6-155">V podokně vlastností **Výsledky vyhledávání** zadejte hodnotu **1** pro **Min. počet výskytů** a poté nastavte další požadované vlastnosti modulu výsledků hledání.</span><span class="sxs-lookup"><span data-stu-id="380b6-155">In the **Search results** properties pane, enter the value **1** for **Min Occurs**, and then set any other required properties for the search results module.</span></span> <span data-ttu-id="380b6-156">Nastavením těchto vlastností v šabloně zajistíte, že veškerá přizpůsobení konkrétní stránce kategorie budou tato nastavení automaticky zahrnovat.</span><span class="sxs-lookup"><span data-stu-id="380b6-156">By setting these properties in the template, you ensure that any customizations to a specific category page will automatically include these settings.</span></span>
1. <span data-ttu-id="380b6-157">Chcete-li publikovat šablonu, vyberte možnost **Dokončit úpravy** a volbou **Publikovat**.</span><span class="sxs-lookup"><span data-stu-id="380b6-157">Select **Finish editing**, and then select **Publish** to publish the template.</span></span>
1. <span data-ttu-id="380b6-158">Přejděte na **Stránky** a volbou **Nová** vytvořte novou stránku.</span><span class="sxs-lookup"><span data-stu-id="380b6-158">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="380b6-159">V dialogovém okně **Zvolte šablonu** vyberte šablonu **Výsledky vyhledávání**, kterou jste vytvořili, zadejte **Stránku kategorie** pro **Název stranky** a pak vyberte tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="380b6-159">In the **Choose a template** dialog box, select the **Search results** template that you created, enter **Category page** for **Page name**, and then select **OK**.</span></span> <span data-ttu-id="380b6-160">Protože jsou všechny hodnoty nastaveny v šabloně, je stránka připravena k publikování.</span><span class="sxs-lookup"><span data-stu-id="380b6-160">Because all the values are set in the template, the page is ready to be published.</span></span>
1. <span data-ttu-id="380b6-161">Chcete-li vrátit stránku se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="380b6-161">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="380b6-162">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="380b6-162">Additional resources</span></span>

[<span data-ttu-id="380b6-163">Přehled výchozí cílové stránky kategorie a stránky výsledků hledání</span><span class="sxs-lookup"><span data-stu-id="380b6-163">Default category landing page and search results page overview</span></span>](category-search-page-overview.md)

[<span data-ttu-id="380b6-164">Přehled knihovny modulů</span><span class="sxs-lookup"><span data-stu-id="380b6-164">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="380b6-165">Modul rychlého zobrazení</span><span class="sxs-lookup"><span data-stu-id="380b6-165">Quick view module</span></span>](quick-view-module.md)
