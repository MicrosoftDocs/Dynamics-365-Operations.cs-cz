---
title: Přehled výchozí cílové stránky kategorie a stránky s výsledky hledání
description: Tohle téma obsahuje přehled výchozí cílové stránky kategorie a stránky výsledků hledání v řešení Dynamics 365 Commerce.
author: ashishmsft
manager: annbe
ms.date: 06/30/2020
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
ms.openlocfilehash: e85449c10fa4a768a144ce423a77bd1fc2c94352
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410749"
---
# <a name="default-category-landing-page-and-search-results-page-overview"></a><span data-ttu-id="75eba-103">Přehled výchozí cílové stránky kategorie a stránky s výsledky hledání</span><span class="sxs-lookup"><span data-stu-id="75eba-103">Default category landing page and search results page overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="75eba-104">Tohle téma obsahuje přehled výchozí cílové stránky kategorie a stránky výsledků hledání v elektronickém obchodu Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="75eba-104">This topic provides an overview of the default category landing page and search results page in Microsoft Dynamics 365 Commerce e-Commerce.</span></span>

## <a name="default-category-landing-page"></a><span data-ttu-id="75eba-105">Výchozí cílová stránka kategorie</span><span class="sxs-lookup"><span data-stu-id="75eba-105">Default category landing page</span></span>

<span data-ttu-id="75eba-106">Výchozí cílová stránka kategorie je stránka, na kterou jsou uživatelé webu obvykle přesměrování při výběru kategorie v navigační hierarchii.</span><span class="sxs-lookup"><span data-stu-id="75eba-106">The default category landing page is the page that website users typically are taken to when they select a category in the navigation hierarchy.</span></span> <span data-ttu-id="75eba-107">Stránka kategorie umožňuje procházení a také třídění a zpřesnění produktů zařazených do kategorií.</span><span class="sxs-lookup"><span data-stu-id="75eba-107">The category page lets you browse, and you can also sort and refine the categorized products.</span></span>

![Výchozí cílová stránka kategorie](./media/SimpleCategoryLandingDressCategory.png)

<span data-ttu-id="75eba-109">V horní části stránky se nachází záhlaví, ve kterém jsou zobrazeny všechny kategorie produktů, jak je vytvořitl manažer prodeje.</span><span class="sxs-lookup"><span data-stu-id="75eba-109">At the top of the page is a header that shows all the product categories and other pages that the merchandising manager has categorized.</span></span> <span data-ttu-id="75eba-110">Konfigurace je součástí konfigurace hierarchie navigace kanálu.</span><span class="sxs-lookup"><span data-stu-id="75eba-110">Configuration is done as part of the configuration of the channel navigation hierarchy.</span></span> <span data-ttu-id="75eba-111">V dolní částí stránky se nachází zápatí, které obsahuje rychlé odkazy na různá témata, která by mohla zajímat nakupujícího.</span><span class="sxs-lookup"><span data-stu-id="75eba-111">At the bottom of the page is a footer that includes quick links to various topics that a shopper might be interested in.</span></span>

<span data-ttu-id="75eba-112">Pro kategorii jsou nezbytné následující součásti:</span><span class="sxs-lookup"><span data-stu-id="75eba-112">The following components are essential for a category:</span></span>

- <span data-ttu-id="75eba-113">**Dlaždice umístění produktu** zobrazuje produkty, které manažer prodeje definoval v kategorii jako součást konfigurace hierarchie navigace.</span><span class="sxs-lookup"><span data-stu-id="75eba-113">**Product placement tiles** show the products that the merchandising manager has defined in a category as part of the configuration of the navigation hierarchy.</span></span>
- <span data-ttu-id="75eba-114">**Souhr zpřesnění a voleb** jsou filtry, které poskytují počty a které lze je použít k upřesnění položek.</span><span class="sxs-lookup"><span data-stu-id="75eba-114">**Refiners and choice summary** are filters that provide counts and that can be used to refine items.</span></span> <span data-ttu-id="75eba-115">Manažer prodeje je konfiguruje jako součást konfigurace metadat souvisejících s kategoriemi kanálů a atributy produktu.</span><span class="sxs-lookup"><span data-stu-id="75eba-115">The merchandising manager configures them as part of the configuration of the metadata related to channel categories and product attributes.</span></span>
- <span data-ttu-id="75eba-116">**Možnosti řazení** slouží návštěvníkům webu k třídění produktů.</span><span class="sxs-lookup"><span data-stu-id="75eba-116">**Sorting options** are used by website visitors to sort the products.</span></span> <span data-ttu-id="75eba-117">Ve výchozím nastavení jsou k dispozici následující možnosti řazení:</span><span class="sxs-lookup"><span data-stu-id="75eba-117">By default, the following sorting options are available:</span></span>

    - <span data-ttu-id="75eba-118">Cena – od nejnižší po nejvyšší</span><span class="sxs-lookup"><span data-stu-id="75eba-118">Price – low to high</span></span>
    - <span data-ttu-id="75eba-119">Cena – od nejvyšší po nejnižší</span><span class="sxs-lookup"><span data-stu-id="75eba-119">Price – high to low</span></span>
    - <span data-ttu-id="75eba-120">Název produktu – \[A–Z\]</span><span class="sxs-lookup"><span data-stu-id="75eba-120">Product name – \[A-Z\]</span></span>
    - <span data-ttu-id="75eba-121">Název produktu – \[Z–A\]</span><span class="sxs-lookup"><span data-stu-id="75eba-121">Product name – \[Z-A\]</span></span>
    - <span data-ttu-id="75eba-122">Hodnocení – od nejnižšího po nejvyšší</span><span class="sxs-lookup"><span data-stu-id="75eba-122">Ratings – low to high</span></span>
    - <span data-ttu-id="75eba-123">Hodnocení – od nejvyššího po nejnižší</span><span class="sxs-lookup"><span data-stu-id="75eba-123">Ratings – high to low</span></span>

- <span data-ttu-id="75eba-124">**Stránkování** umožňuje návštěvníkům webu přesun z jedné stránky výsledků kategorizovaného produktu na jinou stránku.</span><span class="sxs-lookup"><span data-stu-id="75eba-124">**Pagination** lets website visitors move from one page of categorized product results to another page.</span></span>
- <span data-ttu-id="75eba-125">**Celkový počet** udává celkový počet produktů, které jsou definovány v kategorii.</span><span class="sxs-lookup"><span data-stu-id="75eba-125">**Total count** provides the total number of products that are defined in a category.</span></span>

## <a name="enrich-a-category-landing-page"></a><span data-ttu-id="75eba-126">Obohacení cílové stránky kategorie</span><span class="sxs-lookup"><span data-stu-id="75eba-126">Enrich a category landing page</span></span>

<span data-ttu-id="75eba-127">Chcete-li, aby cílová stránka kategorie měla lépe přizpůsobené prostředí pro určitou kategorii, můžete „obohatit“ kategorii na dané cílové stránce kategorie.</span><span class="sxs-lookup"><span data-stu-id="75eba-127">If you want a category landing page to have a more tailored experience for a specific category, you can "enrich" the category landing page for that category.</span></span> <span data-ttu-id="75eba-128">Můžete například přidat marketingové video a nějaký příběh kategorie, abyste získali pozornost nakupujícího.</span><span class="sxs-lookup"><span data-stu-id="75eba-128">For example, you can add a marketing video and some category storytelling to get the shopper's attention.</span></span> <span data-ttu-id="75eba-129">Další informace naleznete v tématu [Obohacení cílové stránky kategorie](enrich-category-page.md).</span><span class="sxs-lookup"><span data-stu-id="75eba-129">For more information, see [Enrich a category landing page](enrich-category-page.md).</span></span>

![Obohacená cílová stránka kategorie](./media/CategoryLandingPages.png)

## <a name="auto-suggest-and-search-results-pages"></a><span data-ttu-id="75eba-131">Automatické návrhy a stránky výsledků hledání</span><span class="sxs-lookup"><span data-stu-id="75eba-131">Auto-suggest and search results pages</span></span>

<span data-ttu-id="75eba-132">Uživatelé webu mohou web prozkoumat buď přechodem na kategorii z hierarchie navigace, nebo zadáním hledaného termínu do vyhledávacího pole.</span><span class="sxs-lookup"><span data-stu-id="75eba-132">Website users can explore a site either by going to a category from the navigation hierarchy or by entering a search term in the search field.</span></span>

<span data-ttu-id="75eba-133">Jakmile uživatelé začnou psát do vyhledávacího pole, projeví se moderní funkce automatických návrhů, které navrhují hledané termíny.</span><span class="sxs-lookup"><span data-stu-id="75eba-133">As soon as users start to type in the search field, they experience the immersive auto-suggest functionality that suggests search terms.</span></span>

<span data-ttu-id="75eba-134">Zde jsou některé typy návrhů, které mohou být zobrazeny:</span><span class="sxs-lookup"><span data-stu-id="75eba-134">Here are some of the types of suggestions that might be shown:</span></span>

- <span data-ttu-id="75eba-135">**Klíčová slova** se používají k vyhledávání položek napříč všemi produkty, které jsou roztříděny v kanálu.</span><span class="sxs-lookup"><span data-stu-id="75eba-135">**Keywords** are used to find items across all products that are assorted to the channel.</span></span>
- <span data-ttu-id="75eba-136">**Produkty** poskytují přímé odkazy na stránku s podrobnostmi o produktu.</span><span class="sxs-lookup"><span data-stu-id="75eba-136">**Products** provide direct links to the product details page.</span></span>
- <span data-ttu-id="75eba-137">**Návrhy vyhledávání ve vymezených kategoriích** uvádí různé kategorie a umožňují uživatelům hledat klíčové slovo v určité kategorii.</span><span class="sxs-lookup"><span data-stu-id="75eba-137">**Scoped category search suggestions** list various categories and let users search for the keyword in a specific category.</span></span>

![Moderní automatické návrhy](./media/ImmersiveAutoSuggestUX.png)

<span data-ttu-id="75eba-139">Když uživatel vybere jeden z návrhů vyhledávání klíčového slova nebo ve vymezené kategorii, nebo když neexistují žádné návrhy pro hledaný termín, které zadají, budou přesměrováni na stránku s výsledky hledání.</span><span class="sxs-lookup"><span data-stu-id="75eba-139">When users select one of the keyword or scoped category search suggestions, or when there are no suggestions for the search term that they enter, they are redirected to a search results page.</span></span> <span data-ttu-id="75eba-140">Uživatelé pak mohou procházet, třídit a upřesnit seznam výsledků hledání a vyhledat požadovanou položku.</span><span class="sxs-lookup"><span data-stu-id="75eba-140">The users can then browse, sort, and refine the list of search results to find the desired item.</span></span>

![Cílová stránka vyhledávání](./media/SearchLanding.png)

<span data-ttu-id="75eba-142">Pro stránku výsledků hledání jsou nezbytné následující součásti:</span><span class="sxs-lookup"><span data-stu-id="75eba-142">The following components are essential for a search results page:</span></span>

- <span data-ttu-id="75eba-143">**Dlaždice umístění produktu** zobrazí produkty pro hledání uživatele.</span><span class="sxs-lookup"><span data-stu-id="75eba-143">**Product placement tiles** show the products for the user's search.</span></span> <span data-ttu-id="75eba-144">Ve výchozím nastavení jsou tyto dlaždice řazeny podle skóre relevantnosti cloudového vyhledávání uživatele.</span><span class="sxs-lookup"><span data-stu-id="75eba-144">By default, these tiles are sorted by the cloud-powered search relevancy score for the user search.</span></span>
- <span data-ttu-id="75eba-145">**Souhr zpřesnění a voleb** jsou filtry, které poskytují počty a které lze je použít k upřesnění položek.</span><span class="sxs-lookup"><span data-stu-id="75eba-145">**Refiners and choice summary** are filters that provide counts and that can be used to refine items.</span></span> <span data-ttu-id="75eba-146">Manažer prodeje je konfiguruje jako součást konfigurace metadat „kategorie kanálu a atributy produktu“.</span><span class="sxs-lookup"><span data-stu-id="75eba-146">The merchandising manager configures them as part of the configuration of the "channel categories and product attributes" metadata.</span></span>
- <span data-ttu-id="75eba-147">**Možnosti řazení** slouží návštěvníkům webu k třídění produktů.</span><span class="sxs-lookup"><span data-stu-id="75eba-147">**Sorting options** are used by website visitors to sort the products.</span></span> <span data-ttu-id="75eba-148">Ve výchozím nastavení jsou k dispozici následující možnosti řazení:</span><span class="sxs-lookup"><span data-stu-id="75eba-148">By default, the following sorting options are available:</span></span>

    - <span data-ttu-id="75eba-149">Cena – od nejnižší po nejvyšší</span><span class="sxs-lookup"><span data-stu-id="75eba-149">Price – low to high</span></span>
    - <span data-ttu-id="75eba-150">Cena – od nejvyšší po nejnižší</span><span class="sxs-lookup"><span data-stu-id="75eba-150">Price – high to low</span></span>
    - <span data-ttu-id="75eba-151">Název produktu – \[A–Z\]</span><span class="sxs-lookup"><span data-stu-id="75eba-151">Product name – \[A-Z\]</span></span>
    - <span data-ttu-id="75eba-152">Název produktu – \[Z–A\]</span><span class="sxs-lookup"><span data-stu-id="75eba-152">Product name – \[Z-A\]</span></span>
    - <span data-ttu-id="75eba-153">Hodnocení – od nejnižšího po nejvyšší</span><span class="sxs-lookup"><span data-stu-id="75eba-153">Ratings – low to high</span></span>
    - <span data-ttu-id="75eba-154">Hodnocení – od nejvyššího po nejnižší</span><span class="sxs-lookup"><span data-stu-id="75eba-154">Ratings – high to low</span></span>
    - <span data-ttu-id="75eba-155">Výchozí</span><span class="sxs-lookup"><span data-stu-id="75eba-155">Default</span></span>

- <span data-ttu-id="75eba-156">**Stránkování** umožňuje návštěvníkům webu přesun z jedné stránky výsledků kategorizovaného produktu na jinou stránku.</span><span class="sxs-lookup"><span data-stu-id="75eba-156">**Pagination** lets website visitors move from one page of categorized product results to another page.</span></span>
- <span data-ttu-id="75eba-157">**Celkový počet** udává celkový počet produktů, které jsou definovány v kategorii a odpovídají kritériím hledání.</span><span class="sxs-lookup"><span data-stu-id="75eba-157">**Total count** provides the total number of products that are defined in a category and that match the search criteria.</span></span>

>[!NOTE]
><span data-ttu-id="75eba-158">Tyto vyhledávací funkce využívající cloud jsou k dispozici od verze 10.0.8.</span><span class="sxs-lookup"><span data-stu-id="75eba-158">These cloud-powered search capabilities are available starting in version 10.0.8.</span></span> <span data-ttu-id="75eba-159">Ujistěte se, že v části **Parametry velkoobchodu> Konfigurační parametry** je u položky ProductSearch.UseAzureSearch nastavena hodnota „true“.</span><span class="sxs-lookup"><span data-stu-id="75eba-159">Ensure that under **Commerce Parameters > Configuration Parameters** there is an entry for "ProductSearch.UseAzureSearch set to 'true'".</span></span> 
<span data-ttu-id="75eba-160">![Konfigurační parametry pro cloudové vyhledávání](./media/CloudPoweredSearchConfigurationParameters.png)</span><span class="sxs-lookup"><span data-stu-id="75eba-160">![Configuration parameters for cloud-powered search](./media/CloudPoweredSearchConfigurationParameters.png)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="75eba-161">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="75eba-161">Additional resources</span></span>

[<span data-ttu-id="75eba-162">Přehled hledání využívajícího cloud</span><span class="sxs-lookup"><span data-stu-id="75eba-162">Cloud-powered search overview</span></span>](cloud-powered-search-overview.md)

[<span data-ttu-id="75eba-163">Přehled domovské stránky</span><span class="sxs-lookup"><span data-stu-id="75eba-163">Home page overview</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="75eba-164">Přehled stránek s podrobnostmi o produktu</span><span class="sxs-lookup"><span data-stu-id="75eba-164">Product details pages overview</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="75eba-165">Přehled stránek košíku a pokladny</span><span class="sxs-lookup"><span data-stu-id="75eba-165">Cart and checkout pages overview</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="75eba-166">Přehled stránek správy účtů</span><span class="sxs-lookup"><span data-stu-id="75eba-166">Account management pages overview</span></span>](quick-tour-account-management.md)

