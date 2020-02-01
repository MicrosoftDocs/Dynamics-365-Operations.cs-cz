---
title: Práce se šablonami
description: Toto téma popisuje, jak pracovat s šablonami v aplikaci Microsoft Dynamics 365 Commerce.
author: phinneyridge
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f7f7e2d3dddc35a43adff8d186cf755eba854313
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697720"
---
# <a name="work-with-templates"></a><span data-ttu-id="cccd9-103">Práce se šablonami</span><span class="sxs-lookup"><span data-stu-id="cccd9-103">Work with templates</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="cccd9-104">Toto téma popisuje, jak pracovat s šablonami v aplikaci Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="cccd9-104">This topic describes how to work with templates in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="cccd9-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="cccd9-105">Overview</span></span>

<span data-ttu-id="cccd9-106">Jak bylo uvedeno v [Přehledu šablon a rozvržení](templates-layouts-overview.md), šablony definují sadu možností, které jsou k dispozici pro navazující autory.</span><span class="sxs-lookup"><span data-stu-id="cccd9-106">As was discussed in [Templates and layouts overview](templates-layouts-overview.md), templates define the set of options that is available to downstream authors.</span></span> <span data-ttu-id="cccd9-107">Šablony jsou užitečné pro tým pro vytváření webů v podniku z několika důvodů a dobře strukturované šablony vám mohou pomoci se všemi následujícími cíli:</span><span class="sxs-lookup"><span data-stu-id="cccd9-107">Templates are useful to an enterprise's web authoring team for several reasons, and well-structured templates can help with all the following goals:</span></span>

- <span data-ttu-id="cccd9-108">Zjednodušte prostředí pro každodenní role editora obsahu.</span><span class="sxs-lookup"><span data-stu-id="cccd9-108">Simplify the authoring experience for day-to-day content editor roles.</span></span>

    - <span data-ttu-id="cccd9-109">Možnosti modulu filtrování tak, aby byly v určité části stránky zobrazeny pouze relevantní moduly.</span><span class="sxs-lookup"><span data-stu-id="cccd9-109">Filter module options so that only relevant modules are shown for a specific page section.</span></span> <span data-ttu-id="cccd9-110">(Část marketingové šablony lze například nakonfigurovat tak, aby odfiltroval nepodstatné moduly, které by v tomto kontextu neměly být nikdy použity, a které budou pouze zkomplikovat úlohy vytváření obsahu, pokud jsou zobrazeny.)</span><span class="sxs-lookup"><span data-stu-id="cccd9-110">(For example, a marketing section of a template can be configured to filter out irrelevant modules that should never be used in that context, and that will just complicate content authoring tasks if they are shown.)</span></span>
    - <span data-ttu-id="cccd9-111">Nakonfigurujte výchozí nastavení modulu, aby se zlepšila efektivita vytváření.</span><span class="sxs-lookup"><span data-stu-id="cccd9-111">Configure default module setting to help improve authoring efficiency.</span></span>
    - <span data-ttu-id="cccd9-112">Definujte výchozí fragmenty stránek, které pomáhají zlepšit efektivitu vytváření.</span><span class="sxs-lookup"><span data-stu-id="cccd9-112">Define default page fragments to help improve authoring efficiency.</span></span> <span data-ttu-id="cccd9-113">(Například fragmenty záhlaví a zápatí v šabloně se automaticky zobrazí na každé navazující stránce.)</span><span class="sxs-lookup"><span data-stu-id="cccd9-113">(For example, header and footer fragments in a template will automatically appear on every downstream page.)</span></span>

- <span data-ttu-id="cccd9-114">Zachovejte podnikové weby ve schváleném vzhledu definováním sady uspořádání modulů a možností konfigurace.</span><span class="sxs-lookup"><span data-stu-id="cccd9-114">Keep enterprise sites on-brand by defining an approved set of module arrangement and configuration options.</span></span>

    > [!TIP] 
    > <span data-ttu-id="cccd9-115">Úspěšné weby e-Commerce poskytují zákazníkům známé, opakovatelné firemní vzory návrhu (UX).</span><span class="sxs-lookup"><span data-stu-id="cccd9-115">Successful e-Commerce sites provide customers with familiar, repeatable, and on-brand user experience (UX) design patterns.</span></span> <span data-ttu-id="cccd9-116">Pomocí šablon můžete ovládat konzistenci v celém webu.</span><span class="sxs-lookup"><span data-stu-id="cccd9-116">By using templates, you help control consistency across your site.</span></span>

- <span data-ttu-id="cccd9-117">Zvyšte skóre optimalizace vyhledávače (SEO) tak, že zaručíte opakované a programově definované definice stránek a metadata.</span><span class="sxs-lookup"><span data-stu-id="cccd9-117">Improve search engine optimization (SEO) scores by ensuring repeatable and programmatically defined page definitions and metadata.</span></span>

> [!NOTE]
> <span data-ttu-id="cccd9-118">Ačkoli jsou šablony navrženy za účelem kontroly konzistence v rámci webu, mohou teoreticky být nakonfigurovány tak, aby nevynucují žádnou konzistenci.</span><span class="sxs-lookup"><span data-stu-id="cccd9-118">Although templates are designed to control consistency across a site, they can theoretically be configured so that they don't enforce any consistency.</span></span> <span data-ttu-id="cccd9-119">Značka a správci webu mohou definovat libovolnou úroveň proměnlivosti stránek na webu.</span><span class="sxs-lookup"><span data-stu-id="cccd9-119">Brand and site administrators can define any level of variability for the pages on their site.</span></span> <span data-ttu-id="cccd9-120">Šablona může například být ponechána zcela otevřená, takže autoři obsahu mohou vytvářet libovolné návrhy stránek, které zvolí.</span><span class="sxs-lookup"><span data-stu-id="cccd9-120">For example, a template can be left entirely open, so that content authors can create any page design that they choose.</span></span> <span data-ttu-id="cccd9-121">V tomto případě se nepoužije žádná z výhod uvedených v předchozím seznamu.</span><span class="sxs-lookup"><span data-stu-id="cccd9-121">In this case, none of the benefits in the preceding list are applicable.</span></span>

## <a name="modify-a-template"></a><span data-ttu-id="cccd9-122">Úprava šablony</span><span class="sxs-lookup"><span data-stu-id="cccd9-122">Modify a template</span></span>

<span data-ttu-id="cccd9-123">Šablony jsou upravovány pomocí editoru šablon.</span><span class="sxs-lookup"><span data-stu-id="cccd9-123">Templates are modified by using the template editor.</span></span>

<span data-ttu-id="cccd9-124">Chcete-li otevřít editor šablon, postupujte jedním z následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="cccd9-124">To open the template editor, follow one of these steps:</span></span>

- <span data-ttu-id="cccd9-125">V navigačním podokně webu vyberte možnost **Šablony** a poté vyberte šablonu, kterou chcete upravit.</span><span class="sxs-lookup"><span data-stu-id="cccd9-125">In the navigation pane of your site, select **Templates**, and then select the template to modify.</span></span>
- <span data-ttu-id="cccd9-126">V editoru stránek pro existující stránku vyberte horní uzel ve stromu osnovy vlevo.</span><span class="sxs-lookup"><span data-stu-id="cccd9-126">In the page editor for an existing page, select the top node in the outline tree on the left.</span></span> <span data-ttu-id="cccd9-127">Potom v podokně vlastností vpravo vyberte vlastnost **Upravit šablonu**.</span><span class="sxs-lookup"><span data-stu-id="cccd9-127">Then, in the property pane on the right, select **Edit Template**.</span></span>

<span data-ttu-id="cccd9-128">V zobrazení stromové struktury osnovy na levé straně jsou zobrazeny možnosti modulu a struktury, které jsou k dispozici pro podřízené rozložení a stránky.</span><span class="sxs-lookup"><span data-stu-id="cccd9-128">The outline tree view on the left shows the module options and structures that are available to child layouts and pages.</span></span> <span data-ttu-id="cccd9-129">Vyberete-li modul ve stromu osnovy, můžete zobrazit vlastnosti šablony pro vybraný modul v podokně vlastností vpravo.</span><span class="sxs-lookup"><span data-stu-id="cccd9-129">When you select a module in the outline tree, you can view the template properties for the selected module in the property pane on the right.</span></span> <span data-ttu-id="cccd9-130">Některé z těchto vlastností jsou jedinečné pro úpravy šablony.</span><span class="sxs-lookup"><span data-stu-id="cccd9-130">Some of these properties are unique to template editing.</span></span> <span data-ttu-id="cccd9-131">Následující tabulka obsahuje popis vlastností.</span><span class="sxs-lookup"><span data-stu-id="cccd9-131">The following table describes these properties.</span></span>

| <span data-ttu-id="cccd9-132">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="cccd9-132">Property name</span></span> | <span data-ttu-id="cccd9-133">Popis</span><span class="sxs-lookup"><span data-stu-id="cccd9-133">Description</span></span> |
|---|---|
| <span data-ttu-id="cccd9-134">Min. počet výskytů</span><span class="sxs-lookup"><span data-stu-id="cccd9-134">Min Occurs</span></span> | <span data-ttu-id="cccd9-135">Tato vlastnost definuje minimální počet výskytů pro vybraný modul.</span><span class="sxs-lookup"><span data-stu-id="cccd9-135">This property defines the minimum number of occurrences for the selected module.</span></span> <span data-ttu-id="cccd9-136">Je-li například hodnota nastavena na **1**, modul je povinný pro navazující autory, zatímco pokud je hodnota nastavena na **0** (nula). modul je nepovinný.</span><span class="sxs-lookup"><span data-stu-id="cccd9-136">For example, if the value is set to **1**, the module is required for downstream authors, whereas if the value is set to **0** (zero), the module is optional.</span></span> |
| <span data-ttu-id="cccd9-137">Max. počet výskytů</span><span class="sxs-lookup"><span data-stu-id="cccd9-137">Max Occurs</span></span> | <span data-ttu-id="cccd9-138">Tato vlastnost definuje maximální počet výskytů pro vybraný modul.</span><span class="sxs-lookup"><span data-stu-id="cccd9-138">This property defines the maximum number of occurrences for the selected module.</span></span> <span data-ttu-id="cccd9-139">Je-li například hodnota nastavena na **1**, lze modul přidat pouze jednou.</span><span class="sxs-lookup"><span data-stu-id="cccd9-139">For example, if the value is set to **1**, the module can be added only one time.</span></span> |
| <span data-ttu-id="cccd9-140">Min. moduly (kontejnery)</span><span class="sxs-lookup"><span data-stu-id="cccd9-140">Min Modules (Containers)</span></span> | <span data-ttu-id="cccd9-141">V modulech, které obsahují jiné moduly (tj. *moduly kontejnerů*), definuje tato vlastnost minimální počet všech modulů, které by měly být přidány jako podřízené.</span><span class="sxs-lookup"><span data-stu-id="cccd9-141">For modules that contain other modules (that is, for *containers modules*), this property defines the minimum number of total modules that should be added as children.</span></span> <span data-ttu-id="cccd9-142">Například pro modul karusel může být hodnota nastavena na číslo, které je větší než 1.</span><span class="sxs-lookup"><span data-stu-id="cccd9-142">For example, for a carousel module, the value might be set to a number that is more than 1.</span></span> |
| <span data-ttu-id="cccd9-143">Max. moduly (kontejnery)</span><span class="sxs-lookup"><span data-stu-id="cccd9-143">Max Modules (Containers)</span></span> | <span data-ttu-id="cccd9-144">U modulů kontejnerů tato vlastnost definuje maximální počet modulů celkem, které by měly být přidány jako podřízené.</span><span class="sxs-lookup"><span data-stu-id="cccd9-144">For container modules, this property defines the maximum number of total modules that should be added as children.</span></span> <span data-ttu-id="cccd9-145">Například pro modul karusel může být hodnota nastavena na číslo, které je menší než 10.</span><span class="sxs-lookup"><span data-stu-id="cccd9-145">For example, for a carousel module, the value might be set to a number that is less than 10.</span></span> |
| <span data-ttu-id="cccd9-146">Uzamčeno</span><span class="sxs-lookup"><span data-stu-id="cccd9-146">Locked</span></span> | <span data-ttu-id="cccd9-147">**Zamčený** ovládací prvek logické hodnoty se zobrazí vedle všech vlastností základního modulu.</span><span class="sxs-lookup"><span data-stu-id="cccd9-147">A **Locked** Boolean control appears next to all core module properties.</span></span> <span data-ttu-id="cccd9-148">To umožňuje autorovi šablony zamknout nastavení modulu v šabloně.</span><span class="sxs-lookup"><span data-stu-id="cccd9-148">It lets the template author lock a module setting in the template.</span></span> <span data-ttu-id="cccd9-149">Zamknuté nastavení modulu nelze přepsat žádnými podřízenými rozloženími nebo stránkami.</span><span class="sxs-lookup"><span data-stu-id="cccd9-149">A module setting that is locked can't be overridden by any child layouts or pages.</span></span> <span data-ttu-id="cccd9-150">Stane se centrálně upravitelnou hodnotou vlastnosti pro všechna rozložení a stránky, které šablonu používají.</span><span class="sxs-lookup"><span data-stu-id="cccd9-150">It becomes a centrally editable property value for all layouts and pages that use the template.</span></span> |

## <a name="create-a-new-template"></a><span data-ttu-id="cccd9-151">Vytvořte novou šablonu</span><span class="sxs-lookup"><span data-stu-id="cccd9-151">Create a new template</span></span>

<span data-ttu-id="cccd9-152">Při vytváření nové šblony postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="cccd9-152">To create a new template, follow these steps.</span></span>

1. <span data-ttu-id="cccd9-153">V navigačním podokně webu vyberte možnost **Šablony**, chcete-li otevřít zobrazení inspektoru šablon.</span><span class="sxs-lookup"><span data-stu-id="cccd9-153">In the navigation pane of your site, select **Templates** to open the template inspector view.</span></span>
1. <span data-ttu-id="cccd9-154">vyberte **Nová šabllona**.</span><span class="sxs-lookup"><span data-stu-id="cccd9-154">Select **New Template**.</span></span>
1. <span data-ttu-id="cccd9-155">V dialogovém okně pro vytvoření šablony zadejte název a popis šablony.</span><span class="sxs-lookup"><span data-stu-id="cccd9-155">In the template creation dialog box, enter a name and description for the template.</span></span> <span data-ttu-id="cccd9-156">Zadané hodnoty se zobrazí autorům při vytváření nových stránek.</span><span class="sxs-lookup"><span data-stu-id="cccd9-156">The values that you enter will be shown to authors when they create new pages.</span></span> <span data-ttu-id="cccd9-157">Zadejte proto metadata, která budou užitečná pro autory stránek.</span><span class="sxs-lookup"><span data-stu-id="cccd9-157">Therefore, enter metadata that will be useful to page authors.</span></span> <span data-ttu-id="cccd9-158">Například zadejte jako popis **Použijte tuto šablonu k vytvoření obecných marketingových stránek**.</span><span class="sxs-lookup"><span data-stu-id="cccd9-158">For example, enter **Use this template to create general marketing pages** as the description.</span></span> <span data-ttu-id="cccd9-159">Tato metadata lze upravit později.</span><span class="sxs-lookup"><span data-stu-id="cccd9-159">This metadata can be edited later.</span></span>
1. <span data-ttu-id="cccd9-160">Chcete-li vytvořit novou šablonu a otevřít editor šablon, klepněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="cccd9-160">Select **OK** to create the new template and open the template editor.</span></span> <span data-ttu-id="cccd9-161">Editor šablon zobrazuje strom osnovy vlevo a podokno vlastností vpravo.</span><span class="sxs-lookup"><span data-stu-id="cccd9-161">The template editor shows an outline tree on the left and a property pane on the right.</span></span>
1. <span data-ttu-id="cccd9-162">Ve stromové struktuře osnovy rozbalte uzly a vyberte slot **Záhlaví HTML**.</span><span class="sxs-lookup"><span data-stu-id="cccd9-162">In the outline tree, expand the nodes, and select the **HTML Head** slot.</span></span>
1. <span data-ttu-id="cccd9-163">Pokud v této patici ještě nejsou žádné moduly, vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul.**</span><span class="sxs-lookup"><span data-stu-id="cccd9-163">If there aren't yet any modules in this slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="cccd9-164">V dialogovém okně **Přidat modul** vyberte **Výchozí souhrn stránky** a pak vyberte možnost **OK**.</span><span class="sxs-lookup"><span data-stu-id="cccd9-164">In the **Add Module** dialog box, select **Default page summary**, and then select **OK**.</span></span>
1. <span data-ttu-id="cccd9-165">Ve stromu osnovy vyberte nový modul a poté v podokně vlastností zadejte všechna výchozí nastavení, která mají být automaticky konfigurována pro všechny podřízené stránky šablony.</span><span class="sxs-lookup"><span data-stu-id="cccd9-165">In the outline tree, select the new module, and then, in the property pane, enter any default settings that should be automatically configured for all child pages of the template.</span></span> <span data-ttu-id="cccd9-166">Pokud nechcete žádné výchozí nastavení, ponechte hodnoty prázdné.</span><span class="sxs-lookup"><span data-stu-id="cccd9-166">If you don't want any default settings, leave the values blank.</span></span>
1. <span data-ttu-id="cccd9-167">Ve stromové struktuře vyberte slot **Obsah**, vyberte tlačítko se třemi tečkami a vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="cccd9-167">In the outline tree, select the **Body** slot, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="cccd9-168">Vyberte modul kontejneru stránky (může existovat pouze jedna možnost) a pak klepněte na tlačítko **OK.**</span><span class="sxs-lookup"><span data-stu-id="cccd9-168">Select a page container module (there might be only one option), and then select **OK**.</span></span>

<span data-ttu-id="cccd9-169">V modulu kontejnerů nové stránky se zobrazí nová sada slotů (**Záhlaví**, **hlavní** atd.).</span><span class="sxs-lookup"><span data-stu-id="cccd9-169">Under the new page container module, you will see a new set of slots (**Header**, **Main**, and so on).</span></span> <span data-ttu-id="cccd9-170">Zde můžete přidat a nakonfigurovat možnosti modulu, které budou k dispozici autorům při vytváření stránek z této šablony.</span><span class="sxs-lookup"><span data-stu-id="cccd9-170">Here, you can add and configure the module options that will be available to authors when they create pages from this template.</span></span> <span data-ttu-id="cccd9-171">Pokud ve výchozím nastavení nepřidáte žádné moduly do slotu, budou pro tento slot podporovány všechny dostupné typy modulů.</span><span class="sxs-lookup"><span data-stu-id="cccd9-171">By default, if you don't add any modules to a slot, all available modules types are supported for that slot.</span></span>

<span data-ttu-id="cccd9-172">Šablona je nyní technicky platná a lze ji uložit, vrátit se změnami a použít k vytvoření nových stránek.</span><span class="sxs-lookup"><span data-stu-id="cccd9-172">The template is now technically valid, and it can be saved, checked in, and used to create new pages.</span></span> <span data-ttu-id="cccd9-173">Následující tři oddíly však popisují některá další výchozí nastavení, která je vhodné nakonfigurovat jako první.</span><span class="sxs-lookup"><span data-stu-id="cccd9-173">However, the next three sections describe some other default settings that you might want to configure first.</span></span>

## <a name="add-a-header-and-a-footer"></a><span data-ttu-id="cccd9-174">Vložení záhlaví a zápatí</span><span class="sxs-lookup"><span data-stu-id="cccd9-174">Add a header and a footer</span></span>

<span data-ttu-id="cccd9-175">Pokud již na webu existuje fragment záhlaví, přidejte pomocí následujícího postupu záhlaví a zápatí do šablony.</span><span class="sxs-lookup"><span data-stu-id="cccd9-175">If your site already has a header fragment, follow these steps to add a header and a footer to a template.</span></span>

1. <span data-ttu-id="cccd9-176">Ve stromu osnovy rozbalte oblast **Obsah** a její podřízený modul stránky.</span><span class="sxs-lookup"><span data-stu-id="cccd9-176">In the outline tree, expand the **Body** slot and its child page module.</span></span>
1. <span data-ttu-id="cccd9-177">Vyberte slot **Záhlaví**.</span><span class="sxs-lookup"><span data-stu-id="cccd9-177">Select the **Header** slot.</span></span>
1. <span data-ttu-id="cccd9-178">Vyberte tlačítko se třemi tečkami (...) pro slot **Záhlaví** a poté vyberte možnost **Přidat fragment**.</span><span class="sxs-lookup"><span data-stu-id="cccd9-178">Select the ellipsis button for the **Header** slot, and then select **Add Fragment**.</span></span>
1. <span data-ttu-id="cccd9-179">Vyhledejte a vyberte fragment záhlaví vašeho webu a poté klepněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="cccd9-179">Search for and select your site's header fragment, and then select **OK**.</span></span>

<span data-ttu-id="cccd9-180">Všechny stránky, které používají tuto šablonu, budou automaticky dědit tento fragment záhlaví.</span><span class="sxs-lookup"><span data-stu-id="cccd9-180">All pages that use the template will now automatically inherit this header fragment.</span></span>

<span data-ttu-id="cccd9-181">Pokud váš web dosud neobsahuje fragment záhlaví, vyhledejte informace o [Vytvoření fragmentu](work-with-fragments.md#create-a-fragment) a potom dokončete předchozí postup.</span><span class="sxs-lookup"><span data-stu-id="cccd9-181">If your site doesn't yet have a header fragment, see [Create a fragment](work-with-fragments.md#create-a-fragment) for information about how to create it, and then complete the previous procedure.</span></span>

## <a name="change-the-template-theme"></a><span data-ttu-id="cccd9-182">Změna motivu šablony</span><span class="sxs-lookup"><span data-stu-id="cccd9-182">Change the template theme</span></span>

<span data-ttu-id="cccd9-183">Chcete-li nastavit výchozí motiv pro všechny stránky používající šablonu, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="cccd9-183">To set the default theme for all pages that use a template, follow these steps.</span></span>

1. <span data-ttu-id="cccd9-184">Ve stromu osnovy stránky nalevo rozbalte slot **Hlavní část**.</span><span class="sxs-lookup"><span data-stu-id="cccd9-184">In the outline tree on the left, expand the **Body** slot.</span></span>
1. <span data-ttu-id="cccd9-185">Ve slotu **Hlavní obsah** vyberte modul kontejneru stránky (například **Výchozí stránka**).</span><span class="sxs-lookup"><span data-stu-id="cccd9-185">In the **Body** slot, select the page container module (for example, **Default Page**).</span></span>
1. <span data-ttu-id="cccd9-186">V podokně vlastností vpravo v poli **Motiv** vyberte motiv.</span><span class="sxs-lookup"><span data-stu-id="cccd9-186">In the property pane on the right, in the **Theme** field, select a theme.</span></span>

<span data-ttu-id="cccd9-187">Ve výchozím nastavení budou nyní všechny nové stránky používat vybraný motiv.</span><span class="sxs-lookup"><span data-stu-id="cccd9-187">By default, all new pages will now use the selected theme.</span></span> <span data-ttu-id="cccd9-188">Chcete-li zabránit, aby stránky přepsaly toto nastavení na úrovni rozvržení nebo stránky, nastavte logický ovládací prvek **Zamčeno** na hodnotu **True**.</span><span class="sxs-lookup"><span data-stu-id="cccd9-188">To prevent pages from overriding this setting at the layout or page level, set the **Locked** Boolean control to **True**.</span></span>

## <a name="add-a-script-to-a-template"></a><span data-ttu-id="cccd9-189">Přidání skriptu do šablony</span><span class="sxs-lookup"><span data-stu-id="cccd9-189">Add a script to a template</span></span>

<span data-ttu-id="cccd9-190">Do šablony můžete přidat prvky **&lt;skriptu&gt;** HTML, které obsahují JavaScript.</span><span class="sxs-lookup"><span data-stu-id="cccd9-190">You can add HTML **&lt;script&gt;** elements that contain JavaScript to your template.</span></span> <span data-ttu-id="cccd9-191">Tímto způsobem můžete poskytnout výchozí chování skriptu k záhlaví HTML, začátku hlavního obsahu a konce základního obsahu na vašich sránkách.</span><span class="sxs-lookup"><span data-stu-id="cccd9-191">In this way, you can provide default script behaviors to the HTML head, body begin, and body end sections of your pages.</span></span>

<span data-ttu-id="cccd9-192">Chcete-li přidat skript do šablony, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="cccd9-192">To add a script to a template, follow these steps.</span></span>

1. <span data-ttu-id="cccd9-193">Ve stromu osnovy vlevo vyberte slot, do něhož chcete přidat prvek **&lt;skriptu&gt;** (například záhlaví HTML, začátek hlavního obsahu či konec hlavního obsahu).</span><span class="sxs-lookup"><span data-stu-id="cccd9-193">In the outline tree on the left, select the slot where you want to add the **&lt;script&gt;** element (for example, the HTML head, body begin, or body end).</span></span>
1. <span data-ttu-id="cccd9-194">Vyberte tlačítko se třemi tečkami pro slot a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="cccd9-194">Select the ellipsis button for the slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="cccd9-195">V dialogovém okně **Přidat modul** vyberte skriptovací modul (například **Externí skript** nebo **Vložený skript**).</span><span class="sxs-lookup"><span data-stu-id="cccd9-195">In the **Add Module** dialog box, select a script module (for example, **External Script** or **Inline Script**).</span></span>
1. <span data-ttu-id="cccd9-196">V podokně vlastností vpravo v příslušném ovládacím prvku vlastnosti skriptu (například **vložený skript** nebo **značky skriptu**) zadejte požadovaný skript.</span><span class="sxs-lookup"><span data-stu-id="cccd9-196">In the property pane on the right, in the appropriate script property control (for example, **Inline Script** or **Script tags**), enter your script.</span></span>
1. <span data-ttu-id="cccd9-197">V podokně vlastností zadejte další volitelná nastavení, která chcete konfigurovat.</span><span class="sxs-lookup"><span data-stu-id="cccd9-197">In the property pane, enter any other optional settings that you want to configure.</span></span>

> [!TIP]
> <span data-ttu-id="cccd9-198">Chcete-li znovu použít kterýkoli z skriptovacích modulů pro jiné šablony, můžete je převést na fragmenty.</span><span class="sxs-lookup"><span data-stu-id="cccd9-198">If you want to reuse any of your script modules for other templates, you can convert them to fragments.</span></span> <span data-ttu-id="cccd9-199">Tímto způsobem můžete zvýšit efektivitu procesu tvorby a centralizovat proces aktualizace.</span><span class="sxs-lookup"><span data-stu-id="cccd9-199">In this way, you help make the authoring process more efficient, and you centralize the update process.</span></span> <span data-ttu-id="cccd9-200">Informace o tom, jak převést skriptovací modul na fragment, naleznete v tématu [Uložení existující konfigurace modulu jako fragment](work-with-fragments.md#save-an-existing-module-configuration-as-a-fragment).</span><span class="sxs-lookup"><span data-stu-id="cccd9-200">For information about how to convert a script module to a fragment, see [Save an existing module configuration as a fragment](work-with-fragments.md#save-an-existing-module-configuration-as-a-fragment).</span></span>

## <a name="save-check-in-preview-and-publish-a-template"></a><span data-ttu-id="cccd9-201">Uložení, navrácení se změnami, náhled a publikování šablony</span><span class="sxs-lookup"><span data-stu-id="cccd9-201">Save, check in, preview, and publish a template</span></span>

<span data-ttu-id="cccd9-202">Chcete-li uložit a vrátit se změnami šablonu, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="cccd9-202">To save and check in a template, follow these steps.</span></span>

1. <span data-ttu-id="cccd9-203">V horní části editoru šablon vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="cccd9-203">Select **Save** at the top of the template editor.</span></span> <span data-ttu-id="cccd9-204">Uložené změny nemají vliv na navazující stránky, dokud nejsou vráceny se změnami.</span><span class="sxs-lookup"><span data-stu-id="cccd9-204">Saved changes don't affect downstream pages until they are checked in.</span></span>
1. <span data-ttu-id="cccd9-205">Vyberte **Vrátit se změnami**.</span><span class="sxs-lookup"><span data-stu-id="cccd9-205">Select **Check In**.</span></span> <span data-ttu-id="cccd9-206">Vaše změny jsou nyní zjistitelné pro navazující workflowy.</span><span class="sxs-lookup"><span data-stu-id="cccd9-206">Your changes are now discoverable for downstream workflows.</span></span>

<span data-ttu-id="cccd9-207">Chcete-li zobrazit náhled změn, buď otevřete existující stránku, která používá šablonu, nebo vytvořte novou stránku z šablony.</span><span class="sxs-lookup"><span data-stu-id="cccd9-207">To preview your changes, either open an existing page that uses the template or create a new page from the template.</span></span>

<span data-ttu-id="cccd9-208">Po zobrazení náhledu změn vašich šablon můžete publikovat šablonu na aktivním webu podle jednoho z následujících kroků:</span><span class="sxs-lookup"><span data-stu-id="cccd9-208">After you've previewed the changes to your template, follow one of these steps to publish the template to your live site:</span></span>

* <span data-ttu-id="cccd9-209">Přejděte na **Šablony**, vyberte šablonu a poté vyberte možnost **Publikovat**.</span><span class="sxs-lookup"><span data-stu-id="cccd9-209">Go to **Templates**, select the template, and then select **Publish**.</span></span>
* <span data-ttu-id="cccd9-210">V editoru šablon vyberte možnost **Publikovat.**</span><span class="sxs-lookup"><span data-stu-id="cccd9-210">In the template editor, select **Publish**.</span></span>
* <span data-ttu-id="cccd9-211">Publikujte stránku, která odkazuje na nepublikovanou šablonu.</span><span class="sxs-lookup"><span data-stu-id="cccd9-211">Publish a page that references the unpublished template.</span></span> <span data-ttu-id="cccd9-212">Šablona je automaticky publikována.</span><span class="sxs-lookup"><span data-stu-id="cccd9-212">The template is automatically published.</span></span>

> [!WARNING]
> <span data-ttu-id="cccd9-213">Pokud je publikována šablona nebo jakákoli jiná položka systému správy obsahu (CMS), je zjistitelná na internetu.</span><span class="sxs-lookup"><span data-stu-id="cccd9-213">When a template, or any other content management system (CMS) item, is published, it's discoverable on the internet.</span></span> <span data-ttu-id="cccd9-214">Nepublikujte dokumenty nebo materiály, dokud je nebudete moci zveřejnit.</span><span class="sxs-lookup"><span data-stu-id="cccd9-214">Don't publish documents or assets until you're ready to make them public.</span></span> <span data-ttu-id="cccd9-215">Verze dokumentů, které byly uloženy a vráceny se změnami, ale dosud nebyly publikovány, jsou zjistitelné pouze pro ověřené uživatele systému.</span><span class="sxs-lookup"><span data-stu-id="cccd9-215">Document versions that have been saved and checked in, but that haven't been published, are discoverable only to authenticated system users.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cccd9-216">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="cccd9-216">Additional resources</span></span>

[<span data-ttu-id="cccd9-217">Přehled šablon a rozvržení</span><span class="sxs-lookup"><span data-stu-id="cccd9-217">Templates and layouts overview</span></span>](templates-layouts-overview.md)

[<span data-ttu-id="cccd9-218">Práce s přednastavenými rozloženími</span><span class="sxs-lookup"><span data-stu-id="cccd9-218">Work with preset layouts</span></span>](work-with-layouts.md)