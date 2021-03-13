---
title: Úprava existující webové stránky
description: Toto téma popisuje, jak upravit existující stránku webu v aplikaci Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 47a7d17b97631ba469a9b68f5f6cf492ebccde6f
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/01/2021
ms.locfileid: "5097299"
---
# <a name="modify-an-existing-site-page"></a><span data-ttu-id="2dd10-103">Úprava existující webové stránky</span><span class="sxs-lookup"><span data-stu-id="2dd10-103">Modify an existing site page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="2dd10-104">Toto téma popisuje, jak upravit existující stránku webu v aplikaci Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2dd10-104">This topic describes how to modify an existing site page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2dd10-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="2dd10-105">Overview</span></span>

<span data-ttu-id="2dd10-106">Pokud je nutné upravit stránku, otevřete ji nejprve v editoru stránek.</span><span class="sxs-lookup"><span data-stu-id="2dd10-106">When you must modify a page, the first step is to open it in the page editor.</span></span> <span data-ttu-id="2dd10-107">Přejděte na web, který obsahuje vaši stránku, a pak v seznamu stránek najděte požadovanou stránku.</span><span class="sxs-lookup"><span data-stu-id="2dd10-107">Go to the site that contains your page, and then, in the list of pages, find the page that you want.</span></span> <span data-ttu-id="2dd10-108">Nemůžete-li stránku najít, můžete použít funkci bohatého vyhledávání nástroje pro vytváření.</span><span class="sxs-lookup"><span data-stu-id="2dd10-108">If you can't find the page, you can use the authoring tool's rich search functionality.</span></span> <span data-ttu-id="2dd10-109">Zadejte přesný název stránky nebo zadejte několik prvních písmen a potom hvězdičku (\*).</span><span class="sxs-lookup"><span data-stu-id="2dd10-109">Either type the exact page name, or type the first few letters of it and then an asterisk (\*).</span></span> <span data-ttu-id="2dd10-110">Zobrazí se filtrovaný seznam stránek.</span><span class="sxs-lookup"><span data-stu-id="2dd10-110">A filtered list of pages appears.</span></span> <span data-ttu-id="2dd10-111">Pomocí tohoto seznamu můžete vyhledat požadovanou stránku.</span><span class="sxs-lookup"><span data-stu-id="2dd10-111">You can use this list to find the page that you want.</span></span> <span data-ttu-id="2dd10-112">Po nalezení správné stránky vyberte název stránky a otevřete tak stránku v editoru stránek.</span><span class="sxs-lookup"><span data-stu-id="2dd10-112">After you find the correct page, select the page name to open the page in the page editor.</span></span>

> [!TIP]
> <span data-ttu-id="2dd10-113">Je-li stránka viditelná v inspektoru stránky, můžete vybrat možnost **Upravit** a před otevřením stránky v editoru stránek ji zkontrolovat.</span><span class="sxs-lookup"><span data-stu-id="2dd10-113">If your page is visible in the page inspector, you can select **Edit** and check the page out before you open it in the page editor.</span></span> <span data-ttu-id="2dd10-114">Tímto způsobem lze zkontrolovat více stránek najednou.</span><span class="sxs-lookup"><span data-stu-id="2dd10-114">In this way, you can check out multiple pages at the same time.</span></span>

<span data-ttu-id="2dd10-115">Po otevření stránky v editoru stránek se ujistěte, že je rezervována vám.</span><span class="sxs-lookup"><span data-stu-id="2dd10-115">After the page is open in the page editor, you must make sure that it's checked out to you.</span></span> <span data-ttu-id="2dd10-116">Panel příkazů v redakčním nástroji je dynamický, kontextový a stavový.</span><span class="sxs-lookup"><span data-stu-id="2dd10-116">The command bar in the authoring tool is dynamic, context-sensitive, and state-sensitive.</span></span> <span data-ttu-id="2dd10-117">Z toho vyplývá, že se zobrazí pouze akce, které lze aktuálně provádět na stránce.</span><span class="sxs-lookup"><span data-stu-id="2dd10-117">Therefore, it shows only the actions that you can currently perform on the page.</span></span> <span data-ttu-id="2dd10-118">Není-li například stránka pro vás zarezervována, v panelu příkazů se nezobrazí tlačítka **Uložit** a **Dokončit úpravy**.</span><span class="sxs-lookup"><span data-stu-id="2dd10-118">For example, if the page isn't checked out to you, the **Save** and **Finish editing** buttons don't appear on the command bar.</span></span> <span data-ttu-id="2dd10-119">Stav stránky se také zobrazuje na pravé straně okna.</span><span class="sxs-lookup"><span data-stu-id="2dd10-119">The state of the page is also shown on the right side of the window.</span></span>

<span data-ttu-id="2dd10-120">Pokud stránka dosud není rezervována, vyberte **Upravit** na panelu příkazů.</span><span class="sxs-lookup"><span data-stu-id="2dd10-120">If the page isn't already checked out to you, select **Edit** on the command bar.</span></span> <span data-ttu-id="2dd10-121">Panel příkazů se změní, aby odrážel nový stav stránky.</span><span class="sxs-lookup"><span data-stu-id="2dd10-121">The command bar changes to reflect the new state of the page.</span></span> <span data-ttu-id="2dd10-122">Obdržíte také oznámení o tom, že pro vás byla stránka rezervována.</span><span class="sxs-lookup"><span data-stu-id="2dd10-122">You also receive a notification that states that the page was checked out to you.</span></span>

<span data-ttu-id="2dd10-123">Chcete-li provést vlastní změny, proveďte následující kroky.</span><span class="sxs-lookup"><span data-stu-id="2dd10-123">The next step is to make your actual changes.</span></span> <span data-ttu-id="2dd10-124">Často použijete stromovou strukturu osnovy stránky vlevo k vyhledání a výběru modulu, který chcete změnit, a poté proveďte změny v podokně vlastnosti vpravo.</span><span class="sxs-lookup"><span data-stu-id="2dd10-124">Often, you will use the page outline tree on the left to find and select the module that you want to change, and then make changes in the properties pane on the right.</span></span> 

<span data-ttu-id="2dd10-125">Vaše změna však může někdy zahrnovat přidání nebo odebrání modelů nebo fragmentů.</span><span class="sxs-lookup"><span data-stu-id="2dd10-125">However, your change might sometimes involve adding or removing models or fragments.</span></span> <span data-ttu-id="2dd10-126">Chcete-li přidat fragment nebo modul, vyhledejte úsek, do něhož chcete přidat modul nebo fragment, pomocí stromu osnovy stránek, a pak vyberte tlačítko se třemi tečkami (**...**) pro tento úsek.</span><span class="sxs-lookup"><span data-stu-id="2dd10-126">To add a fragment or module, use the page outline tree to find the slot that you want to add the module or fragment to, and then select the ellipsis button (**...**) for that slot.</span></span> <span data-ttu-id="2dd10-127">Zobrazí se nabídka obsahující příkazy pro přidání modulu nebo fragmentu.</span><span class="sxs-lookup"><span data-stu-id="2dd10-127">A menu appears that includes commands for adding a module or fragment.</span></span> <span data-ttu-id="2dd10-128">Chcete-li odebrat modul nebo fragment, vyhledejte jej a vyberte ve stromu osnovy stránek, vyberte tlačítko se třemi tečkami a pak vyberte příkaz pro odstranění modulu nebo fragmentu.</span><span class="sxs-lookup"><span data-stu-id="2dd10-128">To remove a module or fragment, find and select it in the page outline tree, select the ellipsis button, and then select the command to delete the module or fragment.</span></span>

> [!TIP]
> <span data-ttu-id="2dd10-129">Můžete také zobrazit a upravit vlastnosti libovolného modulu, který je viditelný v náhledu vizuálního tvůrce stránek, výběrem volby přímo.</span><span class="sxs-lookup"><span data-stu-id="2dd10-129">You can also view and edit the properties for any module that is visible in the visual page builder preview by selecting it directly.</span></span>

<span data-ttu-id="2dd10-130">Po provedení změn a zobrazení náhledu jejich účinku byste měli stránku uložit zaškrtnutím políčka **Dokončit úpravy** na panelu příkazů.</span><span class="sxs-lookup"><span data-stu-id="2dd10-130">After you've finished making your changes and previewing their effect, you should check in the page by selecting **Finish editing** on the command bar.</span></span> 

<span data-ttu-id="2dd10-131">Chcete-li změny publikovat ihned, vyberte možnost **Publikovat** na panelu příkazů.</span><span class="sxs-lookup"><span data-stu-id="2dd10-131">To publish your changes immediately, select **Publish** on the command bar.</span></span> <span data-ttu-id="2dd10-132">Bude publikována poslední vrácená verze stránky, kterou jste upravili, a zpřístupní se tak externím uživatelům, kteří web zobrazí.</span><span class="sxs-lookup"><span data-stu-id="2dd10-132">The latest checked-in version of the page that you modified is published and becomes available to external users who view your site.</span></span> 

## <a name="example-change-the-video-on-the-home-page"></a><span data-ttu-id="2dd10-133">Příklad: Změna videa na domovské stránce</span><span class="sxs-lookup"><span data-stu-id="2dd10-133">Example: Change the video on the home page</span></span>

<span data-ttu-id="2dd10-134">Následující příklad ukazuje, jak upravit domovskou stránku změnou videa, které se zobrazí v modulu přehrávač videa.</span><span class="sxs-lookup"><span data-stu-id="2dd10-134">The following example shows how to modify the home page by changing the video that appears in the video player module.</span></span>

1. <span data-ttu-id="2dd10-135">V části **Weby** vyberte **Fabrikam** (nebo název vašeho webu).</span><span class="sxs-lookup"><span data-stu-id="2dd10-135">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="2dd10-136">V navigačním podokně nalevo vyberte položku **Stránky**.</span><span class="sxs-lookup"><span data-stu-id="2dd10-136">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="2dd10-137">Vyhledejte a vyberte domovskou stránku, kterou chcete otevřít v editoru stránek.</span><span class="sxs-lookup"><span data-stu-id="2dd10-137">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="2dd10-138">Na příkazovém řádku vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="2dd10-138">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="2dd10-139">V osnově stránky vyberte úsek **Hlavní**.</span><span class="sxs-lookup"><span data-stu-id="2dd10-139">In the page outline, select the **Main** slot.</span></span>
1. <span data-ttu-id="2dd10-140">V úseku **Hlavní** rozbalte všechny moduly plovoucího obsahu.</span><span class="sxs-lookup"><span data-stu-id="2dd10-140">Under the **Main** slot, expand all the fluid container modules.</span></span>
1. <span data-ttu-id="2dd10-141">Vyhledejte a vyberte modul přehrávače videa.</span><span class="sxs-lookup"><span data-stu-id="2dd10-141">Find and select the video player module.</span></span>
1. <span data-ttu-id="2dd10-142">V podokně vlastnosti vpravo vyberte vlastnost **video**.</span><span class="sxs-lookup"><span data-stu-id="2dd10-142">In the properties pane on the right, select the **video** property.</span></span> <span data-ttu-id="2dd10-143">Zobrazí se okno pro výběr zdroje.</span><span class="sxs-lookup"><span data-stu-id="2dd10-143">The asset picker appears.</span></span>
1. <span data-ttu-id="2dd10-144">V okně peo výběr zdroje vyberte dostupný zdroj videa nebo vyberte možnost **Odeslat nový zdroj** a odešlete nový zdroj videa.</span><span class="sxs-lookup"><span data-stu-id="2dd10-144">In the asset picker, select an available video asset, or select **Upload new asset** to upload a new video asset.</span></span>
1. <span data-ttu-id="2dd10-145">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="2dd10-145">Select **OK**.</span></span>
1. <span data-ttu-id="2dd10-146">Vyberte **Uložit** a potom vyberte **Dokončit úpravy**.</span><span class="sxs-lookup"><span data-stu-id="2dd10-146">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="2dd10-147">Do pole **Poznámky** zadejte **Změněné video** a pak vyberte **OK.**</span><span class="sxs-lookup"><span data-stu-id="2dd10-147">In the **Comments** field, enter **Changed the video**, and then select **OK**.</span></span>
1. <span data-ttu-id="2dd10-148">Chcete-li zobrazit náhled aktualizované stránky, vyberte volbu **Náhled**.</span><span class="sxs-lookup"><span data-stu-id="2dd10-148">Select **Preview** to preview the updated page.</span></span> <span data-ttu-id="2dd10-149">Až skončíte, zavřete kartu náhledu a vraťte se do nástroje pro vytváření obsahu.</span><span class="sxs-lookup"><span data-stu-id="2dd10-149">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="2dd10-150">Zvolte **Publikovat**.</span><span class="sxs-lookup"><span data-stu-id="2dd10-150">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2dd10-151">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="2dd10-151">Additional resources</span></span>

[<span data-ttu-id="2dd10-152">Přidání nové webové stránky</span><span class="sxs-lookup"><span data-stu-id="2dd10-152">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="2dd10-153">Výběr rozvržení stránky</span><span class="sxs-lookup"><span data-stu-id="2dd10-153">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="2dd10-154">Správa metadat SEO</span><span class="sxs-lookup"><span data-stu-id="2dd10-154">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="2dd10-155">Uložení, náhled a publikování stránky</span><span class="sxs-lookup"><span data-stu-id="2dd10-155">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="2dd10-156">Obohacení stránky produktu</span><span class="sxs-lookup"><span data-stu-id="2dd10-156">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="2dd10-157">Obohacení cílové stránky kategorie</span><span class="sxs-lookup"><span data-stu-id="2dd10-157">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="2dd10-158">Ověření přístupnosti obsahu stránky</span><span class="sxs-lookup"><span data-stu-id="2dd10-158">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="2dd10-159">Vytváření dynamických stránek elektronického obchodu na základě parametrů adresy URL</span><span class="sxs-lookup"><span data-stu-id="2dd10-159">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)
