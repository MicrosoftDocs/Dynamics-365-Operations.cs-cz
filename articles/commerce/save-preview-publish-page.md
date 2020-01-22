---
title: Uložení, náhled a publikování stránky
description: Toto téma popisuje, jak uložit, zobrazit náhled a publikovat stránku v aplikaci Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 3fff8299ecc6833890b14fa421501236830b2c61
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945667"
---
# <a name="save-preview-and-publish-a-page"></a><span data-ttu-id="e89f6-103">Uložení, náhled a publikování stránky</span><span class="sxs-lookup"><span data-stu-id="e89f6-103">Save, preview, and publish a page</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="e89f6-104">Toto téma popisuje, jak uložit, zobrazit náhled a publikovat stránku v aplikaci Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e89f6-104">This topic describes how to save, preview, and publish a page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="save-a-page"></a><span data-ttu-id="e89f6-105">Uložení stránky</span><span class="sxs-lookup"><span data-stu-id="e89f6-105">Save a page</span></span>

<span data-ttu-id="e89f6-106">Chcete-li stránku uložit, je nutné ji rezervovat pro sebe a otevřít v editoru stránek.</span><span class="sxs-lookup"><span data-stu-id="e89f6-106">To save a page, you must have it checked out to yourself and open in the page editor.</span></span> <span data-ttu-id="e89f6-107">Stránku byste měli uložit ihned po úpravě, aby bylo zaručeno, že jsou uloženy provedené změny.</span><span class="sxs-lookup"><span data-stu-id="e89f6-107">You should save a page immediately after you modify it, to help guarantee that your changes are stored.</span></span>

<span data-ttu-id="e89f6-108">Při uložení stránky se tyto změny zobrazí pouze pro vás.</span><span class="sxs-lookup"><span data-stu-id="e89f6-108">When you save a page, the changes are visible only to you.</span></span> <span data-ttu-id="e89f6-109">Operace uložení je určena především pro uložení změn, zatímco stránka ještě není připravena k vrácení se změnami.</span><span class="sxs-lookup"><span data-stu-id="e89f6-109">The save operation is intended primarily to store changes while the page isn't yet ready to be checked in.</span></span> <span data-ttu-id="e89f6-110">Po dokončení úprav stránky doporučujeme, abyste ji vrátili se změnami, aby byly změny viditelné i pro ostatní.</span><span class="sxs-lookup"><span data-stu-id="e89f6-110">When you've finished modifying the page, we recommend that you check it in, so that the changes become visible to others.</span></span> <span data-ttu-id="e89f6-111">V tomto okamžiku může být stránka také rezervována jinými uživateli, kteří je musí upravit.</span><span class="sxs-lookup"><span data-stu-id="e89f6-111">At that point, the page can also be checked out by other users who must modify it.</span></span>

## <a name="preview-a-page"></a><span data-ttu-id="e89f6-112">Náhled stránky</span><span class="sxs-lookup"><span data-stu-id="e89f6-112">Preview a page</span></span>

<span data-ttu-id="e89f6-113">Vývojový nástroj nabízí dva druhy funkcí náhledu: podokno náhledu WYSIWYG v editoru stránek a v samostatném okně náhledu.</span><span class="sxs-lookup"><span data-stu-id="e89f6-113">The authoring tool offers two kinds of preview features: a "what you see is what you get" (WYSIWYG) preview pane in the page editor and a separate preview window.</span></span>

<span data-ttu-id="e89f6-114">Když používáte editor stránek, zobrazí se v prostředním podokně náhled WYSIWYG.</span><span class="sxs-lookup"><span data-stu-id="e89f6-114">While you're using the page editor, a "what you see is what you get" (WYSIWYG) preview appears in the center pane.</span></span> <span data-ttu-id="e89f6-115">Tento náhled je automaticky aktualizován při každém uložení stránky.</span><span class="sxs-lookup"><span data-stu-id="e89f6-115">This preview is automatically updated whenever you save the page.</span></span> <span data-ttu-id="e89f6-116">Aktualizaci můžete také provést ručně výběrem možnosti **Aktualizovat** na panelu příkazů.</span><span class="sxs-lookup"><span data-stu-id="e89f6-116">You can also manually update it by selecting **Refresh** on the command bar.</span></span> <span data-ttu-id="e89f6-117">Náhled WYSIWYG vykreslí stránku stejně, jako ji uvidí uživatelé webu, ale pomocníky pro vytváření obsahu jsou vykresleni nad ní.</span><span class="sxs-lookup"><span data-stu-id="e89f6-117">The WYSIWYG preview renders the page just as the site's users will see it, but authoring helpers are rendered on top of it.</span></span>

<span data-ttu-id="e89f6-118">Po dokončení úprav stránky můžete zobrazit náhled a zobrazit informace o tom, co se odběratelé uvidí.</span><span class="sxs-lookup"><span data-stu-id="e89f6-118">When you've finished modifying the page, you might want to preview it to see what customers will see.</span></span> <span data-ttu-id="e89f6-119">Chcete-li zobrazit náhled stránky, vyberte v panelu příkazů možnost **Náhled**.</span><span class="sxs-lookup"><span data-stu-id="e89f6-119">To preview a page, select **Preview** on the command bar.</span></span> <span data-ttu-id="e89f6-120">Náhled se zobrazí v samostatném okně prohlížeče.</span><span class="sxs-lookup"><span data-stu-id="e89f6-120">The preview will appear in a separate browser window.</span></span> <span data-ttu-id="e89f6-121">Stránka v okně náhledu je vykreslována tak, jak ji uživatel webu uvidí.</span><span class="sxs-lookup"><span data-stu-id="e89f6-121">The page in the preview window is rendered just as the site's user will see it.</span></span> <span data-ttu-id="e89f6-122">Můžete změnit velikost okna, abyste se ujistili, že odpovídající moduly jsou správně vykresleny ve všech portech zobrazení.</span><span class="sxs-lookup"><span data-stu-id="e89f6-122">You can resize the window to make sure that responsive modules are correctly rendered in all view ports.</span></span>

> [!NOTE]
> <span data-ttu-id="e89f6-123">Pro náhled nepublikovaného obsahu jsou vyžadovány ověření a správná oprávnění.</span><span class="sxs-lookup"><span data-stu-id="e89f6-123">Authentication and correct permissions are required to preview unpublished content.</span></span> <span data-ttu-id="e89f6-124">Pokud tedy sdílíte adresu URL náhledu s někým, musí mít tato osoba správná oprávnění pro přístup k obsahu.</span><span class="sxs-lookup"><span data-stu-id="e89f6-124">Therefore, if you share the URL of the preview with someone, that person must have the correct permissions to access the content.</span></span>

## <a name="publish-a-page"></a><span data-ttu-id="e89f6-125">Publikování stránky</span><span class="sxs-lookup"><span data-stu-id="e89f6-125">Publish a page</span></span>

<span data-ttu-id="e89f6-126">Jakmile je stránka připravena, následujícím krokem bude publikování, aby mohli externí uživatelé zobrazit obsah.</span><span class="sxs-lookup"><span data-stu-id="e89f6-126">When your page is ready, the next step is to publish it, so that external users can view the content.</span></span> <span data-ttu-id="e89f6-127">Před publikováním stránky je nutné ji vrátit se změnami.</span><span class="sxs-lookup"><span data-stu-id="e89f6-127">Before you can publish a page, you must check it in.</span></span>

<span data-ttu-id="e89f6-128">Stránky můžete publikovat a zrušit jejich publikování pomocí inspektoru stránky nebo editoru stránek.</span><span class="sxs-lookup"><span data-stu-id="e89f6-128">You can publish and unpublish pages from either the page inspector or the page editor.</span></span> <span data-ttu-id="e89f6-129">Kontrola stránky zobrazuje seznam stránek a umožňuje hromadné operace.</span><span class="sxs-lookup"><span data-stu-id="e89f6-129">The page inspector shows a list of pages and allows for bulk operations.</span></span> <span data-ttu-id="e89f6-130">Editor stránek lze použít k publikování nebo zrušení publikování pouze jedné stránky, která je v ní otevřena.</span><span class="sxs-lookup"><span data-stu-id="e89f6-130">The page editor can be used to publish or unpublish only the single page that is open in it.</span></span>

<span data-ttu-id="e89f6-131">Chcete-li publikovat jednu nebo více stránek z kontroloru stránek, vyberte je, zkontrolujte, zda jsou vráceny se změnami, a pak vyberte **Publikovat** na panelu příkazů.</span><span class="sxs-lookup"><span data-stu-id="e89f6-131">To publish one or more pages from the page inspector, select the pages, make sure that they are checked in, and then select **Publish** on the command bar.</span></span> <span data-ttu-id="e89f6-132">Stránky se publikují a obdržíte oznámení o operaci ve vývojovém nástroji.</span><span class="sxs-lookup"><span data-stu-id="e89f6-132">The pages are published, and you receive a notification about the operation in the authoring tool.</span></span>

<span data-ttu-id="e89f6-133">Chcete-li publikovat jednu stránku z editoru stránek, je postup podobný.</span><span class="sxs-lookup"><span data-stu-id="e89f6-133">To publish a single page from the page editor, the procedure is similar.</span></span> <span data-ttu-id="e89f6-134">Když je stránka otevřena v editoru stránek, ujistěte se, že byla vrácena se změnami, a poté v panelu příkazů vyberte **Publikovat**.</span><span class="sxs-lookup"><span data-stu-id="e89f6-134">While the page is open in the page editor, make sure that it has been checked in, and then select **Publish** on the command bar.</span></span> <span data-ttu-id="e89f6-135">Stránka se publikuje a obdržíte oznámení o operaci ve vývojovém nástroji.</span><span class="sxs-lookup"><span data-stu-id="e89f6-135">The page is published, and you receive a notification about the operation.</span></span>

<span data-ttu-id="e89f6-136">Při publikování stránky se publikuje pouze obsah stránky.</span><span class="sxs-lookup"><span data-stu-id="e89f6-136">When you publish a page, just the page content is published.</span></span> <span data-ttu-id="e89f6-137">Vy i ostatní uživatelé mohou přejít na stránku a zobrazit ji pouze po přidružení adresy URL.</span><span class="sxs-lookup"><span data-stu-id="e89f6-137">You and other users can go to the page and view it only after a URL is associated with it.</span></span> <span data-ttu-id="e89f6-138">Adresa URL musí být publikována samostatně.</span><span class="sxs-lookup"><span data-stu-id="e89f6-138">The URL must be published separately.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e89f6-139">Před publikováním stránky je nutné, aby všechny obrázky nebo fragmenty, které odkazují na stránku, již byly publikovány.</span><span class="sxs-lookup"><span data-stu-id="e89f6-139">Before you can publish a page, any images or fragments that the page references must already be published.</span></span>

## <a name="save-preview-and-publish-a-home-page"></a><span data-ttu-id="e89f6-140">Uložení, náhled a publikování domovské stránky</span><span class="sxs-lookup"><span data-stu-id="e89f6-140">Save, preview, and publish a home page</span></span>

<span data-ttu-id="e89f6-141">Chcete-li uložit, zobrazit náhled a publikovat domovskou stránku, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="e89f6-141">To save, preview, and publish a home page, follow these steps.</span></span>

1. <span data-ttu-id="e89f6-142">V části **Weby** vyberte **Fabrikam** (nebo název vašeho webu).</span><span class="sxs-lookup"><span data-stu-id="e89f6-142">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="e89f6-143">V navigačním podokně nalevo vyberte položku **Stránky**.</span><span class="sxs-lookup"><span data-stu-id="e89f6-143">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="e89f6-144">Vyhledejte a vyberte domovskou stránku, kterou chcete otevřít v editoru stránek.</span><span class="sxs-lookup"><span data-stu-id="e89f6-144">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="e89f6-145">Vyberte **Rezervovat**.</span><span class="sxs-lookup"><span data-stu-id="e89f6-145">Select **Check Out**.</span></span>
1. <span data-ttu-id="e89f6-146">Změňte stránku podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="e89f6-146">Modify the page as you require.</span></span>
1. <span data-ttu-id="e89f6-147">Vyberte **Uložit** a potom **Vrátit se změnami**.</span><span class="sxs-lookup"><span data-stu-id="e89f6-147">Select **Save**, and then select **Check In**.</span></span>
1. <span data-ttu-id="e89f6-148">Do pole **Poznámky** zadejte poznámku ohledně změn, které jste provedli, a poté vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="e89f6-148">In the **Comments** field, enter a note about the changes that you made, and then select **OK**.</span></span>
1. <span data-ttu-id="e89f6-149">Chcete-li zobrazit náhled stránky, vyberte volbu **Náhled**.</span><span class="sxs-lookup"><span data-stu-id="e89f6-149">Select **Preview** to preview your page.</span></span> <span data-ttu-id="e89f6-150">Až skončíte, zavřete kartu náhledu a vraťte se do nástroje pro vytváření obsahu.</span><span class="sxs-lookup"><span data-stu-id="e89f6-150">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="e89f6-151">Zvolte **Publikovat**.</span><span class="sxs-lookup"><span data-stu-id="e89f6-151">Select **Publish**.</span></span>

## <a name="publish-a-url"></a><span data-ttu-id="e89f6-152">Publikování adresy URL</span><span class="sxs-lookup"><span data-stu-id="e89f6-152">Publish a URL</span></span>

<span data-ttu-id="e89f6-153">Adresu URL publikujete takto.</span><span class="sxs-lookup"><span data-stu-id="e89f6-153">To publish a URL, follow these steps.</span></span>

1. <span data-ttu-id="e89f6-154">V části **Weby** vyberte **Fabrikam** (nebo název vašeho webu).</span><span class="sxs-lookup"><span data-stu-id="e89f6-154">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="e89f6-155">V navigačním podokně nalevo vyberte položku **Adresy URL**.</span><span class="sxs-lookup"><span data-stu-id="e89f6-155">In the navigation pane on the left, select **URLs**.</span></span>
1. <span data-ttu-id="e89f6-156">Vyhledejte a vyberte adresu URL, kterou chcete publikovat.</span><span class="sxs-lookup"><span data-stu-id="e89f6-156">Find and select the URL to publish.</span></span>
1. <span data-ttu-id="e89f6-157">Na příkazovém řádku vyberte možnost **Publikovat**.</span><span class="sxs-lookup"><span data-stu-id="e89f6-157">On the command bar, select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e89f6-158">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="e89f6-158">Additional resources</span></span>

[<span data-ttu-id="e89f6-159">Úprava existující webové stránky</span><span class="sxs-lookup"><span data-stu-id="e89f6-159">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="e89f6-160">Přidání nové webové stránky</span><span class="sxs-lookup"><span data-stu-id="e89f6-160">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="e89f6-161">Výběr rozvržení stránky</span><span class="sxs-lookup"><span data-stu-id="e89f6-161">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="e89f6-162">Správa metadat SEO</span><span class="sxs-lookup"><span data-stu-id="e89f6-162">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="e89f6-163">Obohacení stránky produktu</span><span class="sxs-lookup"><span data-stu-id="e89f6-163">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="e89f6-164">Obohacení cílové stránky kategorie</span><span class="sxs-lookup"><span data-stu-id="e89f6-164">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="e89f6-165">Ověření přístupnosti obsahu stránky</span><span class="sxs-lookup"><span data-stu-id="e89f6-165">Verify page content accessibility</span></span>](verify-accessibility.md)
