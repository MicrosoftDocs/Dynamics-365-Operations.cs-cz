---
title: Úprava existující webové stránky
description: Toto téma popisuje, jak upravit existující stránku webu v aplikaci Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ddbef381e9ded18ed1c9226057cac482d4c6e24d
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698365"
---
# <a name="modify-an-existing-site-page"></a><span data-ttu-id="af1f9-103">Úprava existující webové stránky</span><span class="sxs-lookup"><span data-stu-id="af1f9-103">Modify an existing site page</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="af1f9-104">Toto téma popisuje, jak upravit existující stránku webu v aplikaci Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="af1f9-104">This topic describes how to modify an existing site page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="af1f9-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="af1f9-105">Overview</span></span>

<span data-ttu-id="af1f9-106">Pokud je nutné upravit stránku, otevřete ji nejprve v editoru stránek.</span><span class="sxs-lookup"><span data-stu-id="af1f9-106">When you must modify a page, the first step is to open it in the page editor.</span></span> <span data-ttu-id="af1f9-107">Přejděte na web, který obsahuje vaši stránku, a pak v seznamu stránek najděte požadovanou stránku.</span><span class="sxs-lookup"><span data-stu-id="af1f9-107">Go to the site that contains your page, and then, in the list of pages, find the page that you want.</span></span> <span data-ttu-id="af1f9-108">Nemůžete-li stránku najít, můžete použít funkci bohatého vyhledávání nástroje pro vytváření.</span><span class="sxs-lookup"><span data-stu-id="af1f9-108">If you can't find the page, you can use the authoring tool's rich search functionality.</span></span> <span data-ttu-id="af1f9-109">Zadejte přesný název stránky nebo zadejte několik prvních písmen a potom hvězdičku (\*).</span><span class="sxs-lookup"><span data-stu-id="af1f9-109">Either type the exact page name, or type the first few letters of it and then an asterisk (\*).</span></span> <span data-ttu-id="af1f9-110">Zobrazí se filtrovaný seznam stránek.</span><span class="sxs-lookup"><span data-stu-id="af1f9-110">A filtered list of pages appears.</span></span> <span data-ttu-id="af1f9-111">Pomocí tohoto seznamu můžete vyhledat požadovanou stránku.</span><span class="sxs-lookup"><span data-stu-id="af1f9-111">You can use this list to find the page that you want.</span></span> <span data-ttu-id="af1f9-112">Po nalezení správné stránky vyberte název stránky a otevřete tak stránku v editoru stránek.</span><span class="sxs-lookup"><span data-stu-id="af1f9-112">After you find the correct page, select the page name to open the page in the page editor.</span></span>

> [!TIP]
> <span data-ttu-id="af1f9-113">Je-li stránka viditelná v inspektoru stránky, můžete ji vybrat a před otevřením v editoru stránek ji zkontrolovat.</span><span class="sxs-lookup"><span data-stu-id="af1f9-113">If your page is visible in the page inspector, you can select it and check it out before you open it in the page editor.</span></span> <span data-ttu-id="af1f9-114">Tímto způsobem lze zkontrolovat více stránek najednou.</span><span class="sxs-lookup"><span data-stu-id="af1f9-114">In this way, you can check out multiple pages at the same time.</span></span>

<span data-ttu-id="af1f9-115">Po otevření stránky v editoru stránek se ujistěte, že je rezervována vám.</span><span class="sxs-lookup"><span data-stu-id="af1f9-115">After the page is open in the page editor, you must make sure that it's checked out to you.</span></span> <span data-ttu-id="af1f9-116">Panel příkazů v redakčním nástroji je dynamický, kontextový a stavový.</span><span class="sxs-lookup"><span data-stu-id="af1f9-116">The command bar in the authoring tool is dynamic, context-sensitive, and state-sensitive.</span></span> <span data-ttu-id="af1f9-117">Z toho vyplývá, že se zobrazí pouze akce, které lze aktuálně provádět na stránce.</span><span class="sxs-lookup"><span data-stu-id="af1f9-117">Therefore, it shows only the actions that you can curently perform on the page.</span></span> <span data-ttu-id="af1f9-118">Není-li například stránka pro vás zarezervována, v panelu příkazů se nezobrazí tlačítka **Uložit** a **Vrátit se změnami**.</span><span class="sxs-lookup"><span data-stu-id="af1f9-118">For example, if the page isn't checked out to you, the **Save** and **Check in** buttons don't appear on the command bar.</span></span> <span data-ttu-id="af1f9-119">Stav stránky se také zobrazuje na pravé straně okna.</span><span class="sxs-lookup"><span data-stu-id="af1f9-119">The state of the page is also shown on the right side of the window.</span></span>

<span data-ttu-id="af1f9-120">Pokud stránka dosud není rezervována, vyberte **Rezervace** na panelu příkazů.</span><span class="sxs-lookup"><span data-stu-id="af1f9-120">If the page isn't already checked out to you, select **Check out** on the command bar.</span></span> <span data-ttu-id="af1f9-121">Panel příkazů se změní, aby odrážel nový stav stránky.</span><span class="sxs-lookup"><span data-stu-id="af1f9-121">The command bar changes to reflect the new state of the page.</span></span> <span data-ttu-id="af1f9-122">Obdržíte také oznámení o tom, že pro vás byla stránka rezervována.</span><span class="sxs-lookup"><span data-stu-id="af1f9-122">You also receive a notification that states that the page was checked out to you.</span></span>

<span data-ttu-id="af1f9-123">Chcete-li provést vlastní změny, proveďte následující kroky.</span><span class="sxs-lookup"><span data-stu-id="af1f9-123">The next step is to make your actual changes.</span></span> <span data-ttu-id="af1f9-124">Často použijete stromovou strukturu osnovy stránky vlevo k vyhledání a výběru modulu, který chcete změnit, a poté proveďte změny v podokně vlastnosti vpravo.</span><span class="sxs-lookup"><span data-stu-id="af1f9-124">Often, you will use the page outline tree on the left to find and select the module that you want to change, and then make changes in the properties pane on the right.</span></span> 

<span data-ttu-id="af1f9-125">Vaše změna však může někdy zahrnovat přidání nebo odebrání modelů nebo fragmentů.</span><span class="sxs-lookup"><span data-stu-id="af1f9-125">However, your change might sometimes involve adding or removing models or fragments.</span></span> <span data-ttu-id="af1f9-126">Chcete-li přidat fragment nebo modul, vyhledejte úsek, do něhož chcete přidat modul nebo fragment, pomocí stromu osnovy stránek, a pak vyberte tlačítko se třemi tečkami (**...**) pro tento úsek.</span><span class="sxs-lookup"><span data-stu-id="af1f9-126">To add a fragment or module, use the page outline tree to find the slot that you want to add the module or fragment to, and then select the ellipsis button (**...**) for that slot.</span></span> <span data-ttu-id="af1f9-127">Zobrazí se nabídka obsahující příkazy pro přidání modulu nebo fragmentu.</span><span class="sxs-lookup"><span data-stu-id="af1f9-127">A menu appears that includes commands for adding a module or fragment.</span></span> <span data-ttu-id="af1f9-128">Chcete-li odebrat modul nebo fragment, vyhledejte jej a vyberte ve stromu osnovy stránek, vyberte tlačítko se třemi tečkami a pak vyberte příkaz pro odstranění modulu nebo fragmentu.</span><span class="sxs-lookup"><span data-stu-id="af1f9-128">To remove a module or fragment, find and select it in the page outline tree, select the ellipsis button, and then select the command to delete the module or fragment.</span></span>

> [!TIP]
> <span data-ttu-id="af1f9-129">Můžete také zobrazit a upravit vlastnosti libovolného modulu, který je viditelný v náhledu "WYSIWYG", výběrem volby přímo.</span><span class="sxs-lookup"><span data-stu-id="af1f9-129">You can also view and edit the properties for any module that is visible in the "what you see is what you get" (WYSIWYG) preview by selecting it directly.</span></span>

<span data-ttu-id="af1f9-130">Po provedení změn a zobrazení náhledu jejich účinku byste měli stránku uložit zaškrtnutím políčka **Vrátit se změnami** na panelu příkazů.</span><span class="sxs-lookup"><span data-stu-id="af1f9-130">After you've finished making your changes and previewing their effect, you should check in the page by selecting **Check in** on the command bar.</span></span> 

<span data-ttu-id="af1f9-131">Chcete-li změny publikovat ihned, vyberte možnost **Publikovat** na panelu příkazů.</span><span class="sxs-lookup"><span data-stu-id="af1f9-131">To publish your changes immediately, select **Publish** on the command bar.</span></span> <span data-ttu-id="af1f9-132">Bude publikována poslední vrácená verze stránky, kterou jste upravili, a zpřístupní se tak externím uživatelům, kteří web zobrazí.</span><span class="sxs-lookup"><span data-stu-id="af1f9-132">The latest checked-in version of the page that you modified is published and becomes available to external users who view your site.</span></span> 

## <a name="example-change-the-video-on-the-home-page"></a><span data-ttu-id="af1f9-133">Příklad: Změna videa na domovské stránce</span><span class="sxs-lookup"><span data-stu-id="af1f9-133">Example: Change the video on the home page</span></span>

<span data-ttu-id="af1f9-134">Následující příklad ukazuje, jak upravit domovskou stránku změnou videa, které se zobrazí v modulu přehrávač videa.</span><span class="sxs-lookup"><span data-stu-id="af1f9-134">The following example shows how to modify the home page by changing the video that appears in the video player module.</span></span>

1. <span data-ttu-id="af1f9-135">V části **Weby** vyberte **Fabrikam** (nebo název vašeho webu).</span><span class="sxs-lookup"><span data-stu-id="af1f9-135">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="af1f9-136">V navigačním podokně nalevo vyberte položku **Stránky**.</span><span class="sxs-lookup"><span data-stu-id="af1f9-136">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="af1f9-137">Vyhledejte a vyberte domovskou stránku, kterou chcete otevřít v editoru stránek.</span><span class="sxs-lookup"><span data-stu-id="af1f9-137">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="af1f9-138">Na příkazovém řádku vyberte možnost **Rezervovat**.</span><span class="sxs-lookup"><span data-stu-id="af1f9-138">On the command bar, select **Check Out**.</span></span>
1. <span data-ttu-id="af1f9-139">V osnově stránky vyberte úsek **Hlavní**.</span><span class="sxs-lookup"><span data-stu-id="af1f9-139">In the page outline, select the **Main** slot.</span></span>
1. <span data-ttu-id="af1f9-140">V úseku **Hlavní** rozbalte všechny moduly plovoucího obsahu.</span><span class="sxs-lookup"><span data-stu-id="af1f9-140">Under the **Main** slot, expand all the fluid container modules.</span></span>
1. <span data-ttu-id="af1f9-141">Vyhledejte a vyberte modul přehrávače videa.</span><span class="sxs-lookup"><span data-stu-id="af1f9-141">Find and select the video player module.</span></span>
1. <span data-ttu-id="af1f9-142">V podokně vlastnosti vpravo vyberte vlastnost **video**.</span><span class="sxs-lookup"><span data-stu-id="af1f9-142">In the properties pane on the right, select the **video** property.</span></span> <span data-ttu-id="af1f9-143">Zobrazí se okno pro výběr zdroje.</span><span class="sxs-lookup"><span data-stu-id="af1f9-143">The asset picker appears.</span></span>
1. <span data-ttu-id="af1f9-144">V okně peo výběr zdroje vyberte dostupný zdroj videa nebo vyberte možnost **Odeslat nový zdroj** a odešlete nový zdroj videa.</span><span class="sxs-lookup"><span data-stu-id="af1f9-144">In the asset picker, select an available video asset, or select **Upload new asset** to upload a new video asset.</span></span>
1. <span data-ttu-id="af1f9-145">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="af1f9-145">Select **OK**.</span></span>
1. <span data-ttu-id="af1f9-146">Vyberte **Uložit** a potom **Vrátit se změnami**.</span><span class="sxs-lookup"><span data-stu-id="af1f9-146">Select **Save**, and then select **Check In**.</span></span>
1. <span data-ttu-id="af1f9-147">Do pole **Poznámky** zadejte **Změněné video** a pak vyberte **OK.**</span><span class="sxs-lookup"><span data-stu-id="af1f9-147">In the **Comments** field, enter **Changed the video**, and then select **OK**.</span></span>
1. <span data-ttu-id="af1f9-148">Chcete-li zobrazit náhled aktualizované stránky, vyberte volbu **Náhled**.</span><span class="sxs-lookup"><span data-stu-id="af1f9-148">Select **Preview** to preview the updated page.</span></span> <span data-ttu-id="af1f9-149">Až skončíte, zavřete kartu náhledu a vraťte se do nástroje pro vytváření obsahu.</span><span class="sxs-lookup"><span data-stu-id="af1f9-149">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="af1f9-150">Zvolte **Publikovat**.</span><span class="sxs-lookup"><span data-stu-id="af1f9-150">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="af1f9-151">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="af1f9-151">Additional resources</span></span>

[<span data-ttu-id="af1f9-152">Přidání nové webové stránky</span><span class="sxs-lookup"><span data-stu-id="af1f9-152">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="af1f9-153">Výběr rozvržení stránky</span><span class="sxs-lookup"><span data-stu-id="af1f9-153">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="af1f9-154">Správa metadat SEO</span><span class="sxs-lookup"><span data-stu-id="af1f9-154">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="af1f9-155">Uložení, náhled a publikování stránky</span><span class="sxs-lookup"><span data-stu-id="af1f9-155">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="af1f9-156">Obohacení stránky produktu</span><span class="sxs-lookup"><span data-stu-id="af1f9-156">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="af1f9-157">Obohacení cílové stránky kategorie</span><span class="sxs-lookup"><span data-stu-id="af1f9-157">Enrich a category landing page</span></span>](enrich-category-page.md)
