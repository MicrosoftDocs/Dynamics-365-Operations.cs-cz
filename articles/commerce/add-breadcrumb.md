---
title: Modul popisu cesty
description: Tohle téma se zabývá moduly popisu cesty a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
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
ms.openlocfilehash: ec9f5c72b03d9fd76055369e24491db5c7633cdf
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517153"
---
# <a name="breadcrumb-module"></a><span data-ttu-id="3f03b-103">Modul popisu cesty</span><span class="sxs-lookup"><span data-stu-id="3f03b-103">Breadcrumb module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3f03b-104">Tohle téma se zabývá moduly popisu cesty a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3f03b-104">This topic covers breadcrumb modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="3f03b-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="3f03b-105">Overview</span></span>

<span data-ttu-id="3f03b-106">Moduly popisu cesty se používají k zajištění sekundární navigace na stránkách webu.</span><span class="sxs-lookup"><span data-stu-id="3f03b-106">Breadcrumb modules are used to provide secondary navigation on site pages.</span></span> <span data-ttu-id="3f03b-107">Obvykle se zobrazují v horní části stránky pod záhlavím.</span><span class="sxs-lookup"><span data-stu-id="3f03b-107">They are typically shown at the top of a page, below the header.</span></span> <span data-ttu-id="3f03b-108">Přestože lze moduly popisu cesty přidat na jakoukoli stránku, nejčastěji se používají na stránkách podrobností o produktu, aby zobrazovaly hierarchii kategorií produktů a poskytovaly rychlý způsob, jak se pohybovat po webu.</span><span class="sxs-lookup"><span data-stu-id="3f03b-108">Although breadcrumb modules can be added to any page, they are most often used on product details pages (PDPs), to show the product category hierarchy and provide a quick way to move around a site.</span></span> <span data-ttu-id="3f03b-109">Modul popisu cesty lze také použít k zobrazení odkazu „Zpět na výsledky“, když uživatelé otevřou stránku podrobností o produktu ze stránky vyhledávání nebo seznamu.</span><span class="sxs-lookup"><span data-stu-id="3f03b-109">A breadcrumb module can also be used to show a "Back to results" link when users open a PDP from a search or list page.</span></span> <span data-ttu-id="3f03b-110">Tímto způsobem se uživatelé mohou rychle vrátit na svou stránku filtrovaného seznamu a pokračovat v nakupování.</span><span class="sxs-lookup"><span data-stu-id="3f03b-110">In this way, users can quickly return to their filtered list page to continue shopping.</span></span>

<span data-ttu-id="3f03b-111">Na stránkách, které mají kontext kategorie produktu, jako jsou stránky podrobností o produktu a stránky kategorií, ukazují moduly popisu cesty hierarchii kategorií.</span><span class="sxs-lookup"><span data-stu-id="3f03b-111">On pages that have product category context, such as PDPs and category pages, breadcrumb modules show the category hierarchy.</span></span> <span data-ttu-id="3f03b-112">Na stránkách, které nemají kontext kategorie, zobrazí moduly popisu cesty standardně **&lt;Kořen webu&gt; / &lt;Aktuální stránka&gt;**.</span><span class="sxs-lookup"><span data-stu-id="3f03b-112">On pages that don't have category context, breadcrumb modules show **&lt;Site root&gt; / &lt;Current page&gt;** by default.</span></span> <span data-ttu-id="3f03b-113">Moduly popisu cesty lze také ručně konfigurovat na jiných typech webových stránek, aby zobrazovaly odkazy na konkrétní stránky na webu.</span><span class="sxs-lookup"><span data-stu-id="3f03b-113">Breadcrumb modules can also be manually configured on other types of site pages to show links to specific pages on the site.</span></span>

> [!NOTE]
> <span data-ttu-id="3f03b-114">Modul popisu cesty je k dispozici v Dynamics 365 Commerce vydání 10.0.12.</span><span class="sxs-lookup"><span data-stu-id="3f03b-114">The breadcrumb module is available in the Dynamics 365 Commerce 10.0.12 release.</span></span>

<span data-ttu-id="3f03b-115">Následující obrázek znázorňuje příklad modulu popisu cesty, který zobrazuje hierarchii kategorií na stránce podrobností o produktu.</span><span class="sxs-lookup"><span data-stu-id="3f03b-115">The following image shows an example of a breadcrumb module that shows the category hierarchy on a PDP.</span></span>

![Příklad modulu popisu cesty](./media/ecommerce-breadcrumb.PNG)

## <a name="breadcrumb-module-settings"></a><span data-ttu-id="3f03b-117">Nastavení modulu popisu cesty</span><span class="sxs-lookup"><span data-stu-id="3f03b-117">Breadcrumb module settings</span></span>

<span data-ttu-id="3f03b-118">Modul popisu cesty řídí nastavení **Typ zobrazení popisu cesty na stránce podrobností o produktu**, které je definováno v **Nastavení webu \> Rozšíření** v tvůrci webů.</span><span class="sxs-lookup"><span data-stu-id="3f03b-118">The breadcrumb module relies on the **Breadcrumb display type on PDP** setting, which is defined at **Site Settings \> Extensions** in site builder.</span></span> <span data-ttu-id="3f03b-119">Toto nastavení má tři mezi možné hodnoty:</span><span class="sxs-lookup"><span data-stu-id="3f03b-119">This setting has three possible values:</span></span>

- <span data-ttu-id="3f03b-120">**Zobrazit hierarchii kategorií** – Je-li tato hodnota vybrána, modul popisu cesty zobrazí hierarchii celé kategorie produktu, který je zobrazen na stránce s podrobnostmi o produktu.</span><span class="sxs-lookup"><span data-stu-id="3f03b-120">**Show category hierarchy** – When this value is selected, the breadcrumb module will show the full category hierarchy of the product that is viewed on the PDP.</span></span>
- <span data-ttu-id="3f03b-121">**Zobrazit odkaz Zpět na výsledky** – Když je tato hodnota vybrána, modul popisu cesty zobrazí na stránce podrobností o produktu odkaz „Zpět na výsledky“, pokud uživatel otevřel stránku podrobností o produktu z modulu, který podporuje odkaz „Zpět na výsledky“.</span><span class="sxs-lookup"><span data-stu-id="3f03b-121">**Show back to results** – When this value is selected, the breadcrumb module will show a "Back to results" link on a PDP if the user opened the PDP from a module that allows for a "Back to results" link.</span></span> <span data-ttu-id="3f03b-122">Tato funkce je k dispozici, když uživatelé přecházejí ze stránek kategorií, vyhledávání, seznamu a seznamů doporučení.</span><span class="sxs-lookup"><span data-stu-id="3f03b-122">This functionality is available when users navigate from category, search, list, and recommendation lists pages.</span></span> <span data-ttu-id="3f03b-123">Pro podporu této funkce mají moduly kolekce produktů a výsledků vyhledávání vlastnost, která je pojmenována **Povolit odkaz Zpět na výsledky na stránce podrobností o produktu**.</span><span class="sxs-lookup"><span data-stu-id="3f03b-123">To support this functionality, product collection and search results modules have a property that is named **Allow back to results on PDP**.</span></span> <span data-ttu-id="3f03b-124">Tato vlastnost vám poskytuje flexibilitu při definování, které moduly by měly podporovat funkci odkazu „Zpět na výsledky“ na stránce podrobností o produktu.</span><span class="sxs-lookup"><span data-stu-id="3f03b-124">This property gives you the flexibility to define which modules should support the "Back to results" link functionality on the PDP.</span></span> <span data-ttu-id="3f03b-125">Například když je vybrána možnost **Zobrazit odkaz Zpět na výsledky** pro nastavení **Typ zobrazení popisu cesty na stránce podrobností o produktu** a možnost **Povolit odkaz Zpět na výsledky na stránce podrobností o produktu** pro modul výsledků vyhledávání na stránce vyhledávání, odkaz „Zpět na výsledky“ se zobrazí, když uživatelé přejdou ze stránky vyhledávání na stránku podrobností o produktu.</span><span class="sxs-lookup"><span data-stu-id="3f03b-125">For example, when **Show back to results** is selected for the **Breadcrumb display type on PDP** setting of the breadcrumb module, and **Allow back to results on PDP** is selected for the search page search results module, a "Back to results" link will be shown when users navigate from the search page to a PDP.</span></span>
- <span data-ttu-id="3f03b-126">**Zobrazit hierarchii kategorií a odkaz Zpět na výsledky** – Tato hodnota je kombinací předchozích dvou.</span><span class="sxs-lookup"><span data-stu-id="3f03b-126">**Show category hierarchy and back to results** – This value is a combination of the previous two.</span></span> <span data-ttu-id="3f03b-127">Když je tato hodnota vybrána, modul popisu cesty zobrazí na stránce podrobností o produktu jak hierarchii celé kategorie, tak i odkaz „Zpět na výsledky“ (pokud je nakonfigurován).</span><span class="sxs-lookup"><span data-stu-id="3f03b-127">When this value is selected, the breadcrumb module will show both the full category hierarchy and a "Back to results" link (if it's configured) on a PDP.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3f03b-128">Tato nastavení jsou k dispozici ve vydání Dynamics 365 Commerce 10.0.12.</span><span class="sxs-lookup"><span data-stu-id="3f03b-128">These settings are available in the Dynamics 365 Commerce 10.0.12 release.</span></span> <span data-ttu-id="3f03b-129">Pokud provádíte aktualizaci ze starší verze Dynamics 365 Commerce, musíte ručně aktualizovat soubor appsettings.json.</span><span class="sxs-lookup"><span data-stu-id="3f03b-129">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="3f03b-130">Pokyny k aktualizaci souboru appsettings.json najdete v části [Aktualizace SDK a knihoven modulů](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="3f03b-130">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="breadcrumb-module-properties"></a><span data-ttu-id="3f03b-131">Vlastnosti modulu popisu cesty</span><span class="sxs-lookup"><span data-stu-id="3f03b-131">Breadcrumb module properties</span></span>

| <span data-ttu-id="3f03b-132">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="3f03b-132">Property name</span></span> | <span data-ttu-id="3f03b-133">Hodnoty</span><span class="sxs-lookup"><span data-stu-id="3f03b-133">Values</span></span> | <span data-ttu-id="3f03b-134">popis</span><span class="sxs-lookup"><span data-stu-id="3f03b-134">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="3f03b-135">Kořen</span><span class="sxs-lookup"><span data-stu-id="3f03b-135">Root</span></span> | <span data-ttu-id="3f03b-136">Text nebo odkaz</span><span class="sxs-lookup"><span data-stu-id="3f03b-136">Text or link</span></span>| <span data-ttu-id="3f03b-137">Tato volitelná vlastnost určuje text odkazu a cíl odkazu pro kořen webu popisu cesty.</span><span class="sxs-lookup"><span data-stu-id="3f03b-137">This optional property specifies link text and a link target for the breadcrumb site root.</span></span> <span data-ttu-id="3f03b-138">Pokud tato vlastnost není nakonfigurována, nebude definován žádný kořen.</span><span class="sxs-lookup"><span data-stu-id="3f03b-138">If this property isn't configured, no root will be defined.</span></span> |
| <span data-ttu-id="3f03b-139">Odkaz popisu cesty</span><span class="sxs-lookup"><span data-stu-id="3f03b-139">Breadcrumb link</span></span> | <span data-ttu-id="3f03b-140">Propojení</span><span class="sxs-lookup"><span data-stu-id="3f03b-140">Link</span></span> | <span data-ttu-id="3f03b-141">Tato volitelná vlastnost definuje odkazy na ručně konfigurovaný popis cesty, pokud jsou tyto odkazy vyžadovány.</span><span class="sxs-lookup"><span data-stu-id="3f03b-141">This optional property specifies links for a manually configured breadcrumb, if these links are required.</span></span> <span data-ttu-id="3f03b-142">Odkazy se zobrazí v pořadí, v jakém jsou uvedeny.</span><span class="sxs-lookup"><span data-stu-id="3f03b-142">Links appear in the order that they are listed in.</span></span> |

## <a name="add-a-breadcrumb-module-to-a-new-page"></a><span data-ttu-id="3f03b-143">Přidání modulu popisu cesty na novou stránku</span><span class="sxs-lookup"><span data-stu-id="3f03b-143">Add a breadcrumb module to a new page</span></span>

<span data-ttu-id="3f03b-144">Chcete-li přidat modul popisu cesty na stránku podrobností o produktu a nastavit požadované vlastnosti, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="3f03b-144">To add a breadcrumb module to a PDP and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="3f03b-145">Přejděte na **Nastavení webu \> Rozšíření** a pak pro nastavení **Typ zobrazení popisu cesty** na stránce podrobností o produktu vyberte **Zobrazit hierarchii kategorií**.</span><span class="sxs-lookup"><span data-stu-id="3f03b-145">Go to **Site Settings \> Extensions**, and then, for the **Breadcrumb display type on PDP** setting, select **Show category hierarchy**.</span></span>
1. <span data-ttu-id="3f03b-146">Přejděte na **Šablony** a vyberte šablonu stránky podrobností o produktu.</span><span class="sxs-lookup"><span data-stu-id="3f03b-146">Go to **Templates**, and select the PDP template.</span></span>
1. <span data-ttu-id="3f03b-147">V pozici **Kontejner**, který obsahuje modul buy box, vyberte tři tečky (**...**) a poté vyberte **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="3f03b-147">In the **Container** slot that contains the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="3f03b-148">V dialogovém okně **Přidat modul** vyberte modul **Popis cesty** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="3f03b-148">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="3f03b-149">Chcete-li vrátit šablonu se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="3f03b-149">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="3f03b-150">Přejděte na **Stránky** a otevřete stránku podrobností o produktu, která používá šablonu stránky podrobností o produktu.</span><span class="sxs-lookup"><span data-stu-id="3f03b-150">Go to **Pages**, and open a PDP that uses the PDP template.</span></span> <span data-ttu-id="3f03b-151">Pokud stránka podrobností o produktu ještě neexistuje, vytvořte ji.</span><span class="sxs-lookup"><span data-stu-id="3f03b-151">If a PDP doesn't yet exist, create one.</span></span>
1. <span data-ttu-id="3f03b-152">V pozici **Kontejner**, který obsahuje modul buy box, vyberte tři tečky (**...**) a poté vyberte **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="3f03b-152">In the **Container** slot that contains the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="3f03b-153">V dialogovém okně **Přidat modul** vyberte modul **Popis cesty** a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="3f03b-153">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="3f03b-154">V podokně vlastností pozice **Popis cesty** v sekci **Kořen** vyberte **Text odkazu**.</span><span class="sxs-lookup"><span data-stu-id="3f03b-154">In the properties pane of the **Breadcrumb** slot, under **Root**, select **Link text**.</span></span>
1. <span data-ttu-id="3f03b-155">V dialogovém okně **Text odkazu** zadejte **Domů** a poté v sekci **Cíl odkazu** vyberte **Přidat odkaz**.</span><span class="sxs-lookup"><span data-stu-id="3f03b-155">In the **Link text** dialog box, enter **Home**, and then, under **Link target**, select **Add a link**.</span></span>
1. <span data-ttu-id="3f03b-156">V dialogovém okně **Přidat odkaz** vyberte odkaz pro kořen popisu cesty a poté klepněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="3f03b-156">In the **Add a link** dialog box, select a link for the breadcrumb root, and then select **OK**.</span></span>
1. <span data-ttu-id="3f03b-157">Vyberte možnost **Uložit** a poté vyberte možnost **Náhled**, chcete-li zobrazit náhled stránky.</span><span class="sxs-lookup"><span data-stu-id="3f03b-157">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="3f03b-158">Chcete-li vrátit šablonu se změnami, vyberte možnost **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="3f03b-158">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3f03b-159">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="3f03b-159">Additional resources</span></span>

[<span data-ttu-id="3f03b-160">Přehled knihovny modulů</span><span class="sxs-lookup"><span data-stu-id="3f03b-160">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="3f03b-161">Modul navigační nabídky</span><span class="sxs-lookup"><span data-stu-id="3f03b-161">Navigation menu module</span></span>](nav-menu-module.md)

[<span data-ttu-id="3f03b-162">Modul volby webu</span><span class="sxs-lookup"><span data-stu-id="3f03b-162">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="3f03b-163">Přehled výchozí cílové stránky kategorie a stránky výsledků hledání</span><span class="sxs-lookup"><span data-stu-id="3f03b-163">Overview of default category landing page and search results page</span></span>](category-search-page-overview.md)

[<span data-ttu-id="3f03b-164">Moduly kolekce produktů</span><span class="sxs-lookup"><span data-stu-id="3f03b-164">Product collection modules</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="3f03b-165">Modul buy boxu</span><span class="sxs-lookup"><span data-stu-id="3f03b-165">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="3f03b-166">SDK a aktualizace knihovny modulů</span><span class="sxs-lookup"><span data-stu-id="3f03b-166">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)
