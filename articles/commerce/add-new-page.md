---
title: Přidání nové webové stránky
description: Toto téma popisuje, jak přidat novou stránku webu v řešení Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 04/14/2020
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
ms.openlocfilehash: b0f1e290526c25aa6e6300c65e24044a325bee53
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410729"
---
# <a name="add-a-new-site-page"></a><span data-ttu-id="939e4-103">Přidání nové webové stránky</span><span class="sxs-lookup"><span data-stu-id="939e4-103">Add a new site page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="939e4-104">Toto téma popisuje, jak přidat novou stránku webu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="939e4-104">This topic describes how to add a new site page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="939e4-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="939e4-105">Overview</span></span>

<span data-ttu-id="939e4-106">Po vytvoření šablon a fragmentů pro váš web je dalším krokem vytváření stránek, které je používají.</span><span class="sxs-lookup"><span data-stu-id="939e4-106">After you've created templates and fragments for your site, the next step is to start to create pages that use them.</span></span> <span data-ttu-id="939e4-107">Než začnete, musíte vybrat šablonu nebo rozložení, název stránky a adresu URL stránky.</span><span class="sxs-lookup"><span data-stu-id="939e4-107">To get started, you must select a template or layout, a page name, and a page URL.</span></span>

## <a name="template-or-layout"></a><span data-ttu-id="939e4-108">Šablona nebo rozložení</span><span class="sxs-lookup"><span data-stu-id="939e4-108">Template or layout</span></span>

<span data-ttu-id="939e4-109">Pro novou stránku můžete použít buď šablonu, nebo rozvržení.</span><span class="sxs-lookup"><span data-stu-id="939e4-109">You can use either a template or a layout for your new page.</span></span> <span data-ttu-id="939e4-110">Další informace získáte v části [Přehled šablon a rozložení](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="939e4-110">For more information, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

## <a name="page-name"></a><span data-ttu-id="939e4-111">Název stránky</span><span class="sxs-lookup"><span data-stu-id="939e4-111">Page name</span></span>

<span data-ttu-id="939e4-112">Název stránky musí být jedinečný pro vaši stránku.</span><span class="sxs-lookup"><span data-stu-id="939e4-112">The page name must be unique to your page.</span></span> <span data-ttu-id="939e4-113">Měl by být názorný, aby jej bylo možné snadno najít a ostatní uživatelé věděli, pro k čemu je daná stránka určena.</span><span class="sxs-lookup"><span data-stu-id="939e4-113">It should be descriptive, so that you can easily find it and other people know what the page is intended for.</span></span> <span data-ttu-id="939e4-114">Název stránky vyberte pečlivě, protože jej nelze později změnit.</span><span class="sxs-lookup"><span data-stu-id="939e4-114">Choose the page name carefully, because it can't be changed later.</span></span>

## <a name="page-url"></a><span data-ttu-id="939e4-115">Adresa URL stránky</span><span class="sxs-lookup"><span data-stu-id="939e4-115">Page URL</span></span>

<span data-ttu-id="939e4-116">Máte možnost zadat adresu URL nové stránky.</span><span class="sxs-lookup"><span data-stu-id="939e4-116">You can have the option to enter a URL for your new page.</span></span> <span data-ttu-id="939e4-117">Při vytváření stránky můžete zadat řetězec, který bude použit k vytvoření úplné adresy URL.</span><span class="sxs-lookup"><span data-stu-id="939e4-117">When you create a page, you can enter a string that will be used to form a complete URL.</span></span> <span data-ttu-id="939e4-118">Tento řetězec je označován jako relativní adresa URL nebo jako slug adresy URL.</span><span class="sxs-lookup"><span data-stu-id="939e4-118">This string is known as a relative URL or a URL slug.</span></span> <span data-ttu-id="939e4-119">Na základě slugu adresy URL je poté vytvořena úplná adresa URL a je jí přiřazena nová stránka.</span><span class="sxs-lookup"><span data-stu-id="939e4-119">A complete URL is then generated based on the URL slug, and the new page is assigned to it.</span></span> <span data-ttu-id="939e4-120">Tento slug adresy URL lze změnit později před publikováním stránky.</span><span class="sxs-lookup"><span data-stu-id="939e4-120">You can change the URL slug later, before you publish the page.</span></span> <span data-ttu-id="939e4-121">Další informace naleznete v tématu [Vytvoření adresy URL stránky](create-page-URL.md).</span><span class="sxs-lookup"><span data-stu-id="939e4-121">For more information, see [Create a page URL](create-page-URL.md).</span></span>

> [!NOTE]
> <span data-ttu-id="939e4-122">Dynamics 365 Commerce odděluje adresy URL a obsah.</span><span class="sxs-lookup"><span data-stu-id="939e4-122">Dynamics 365 Commerce decouples URLs and content.</span></span> <span data-ttu-id="939e4-123">Jinými slovy, lze vytvořit stránku, která není přidružena k adrese URL, a lze vytvořit adresu URL, která není přidružena ke stránce.</span><span class="sxs-lookup"><span data-stu-id="939e4-123">In other words, a page can be created that isn't associated with an URL, and a URL can be created that isn't associated with a page.</span></span> <span data-ttu-id="939e4-124">Proto lze pro adresu URL lze prohodit obsah bez prostorů a přesměrování lze snázeji spravovat.</span><span class="sxs-lookup"><span data-stu-id="939e4-124">Therefore, content swapping can be done for a URL and doesn't require downtime, and redirects are easier to manage.</span></span>

## <a name="add-a-new-page"></a><span data-ttu-id="939e4-125">Přidání nové stránky</span><span class="sxs-lookup"><span data-stu-id="939e4-125">Add a new page</span></span>

<span data-ttu-id="939e4-126">Chcete-li na svůj web přidat novou stránku webu, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="939e4-126">To add a new site page to your site, follow these steps.</span></span>

1. <span data-ttu-id="939e4-127">V části **Weby** vyberte **Fabrikam** (nebo název vašeho webu).</span><span class="sxs-lookup"><span data-stu-id="939e4-127">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="939e4-128">Zvolte **Nová stránka**.</span><span class="sxs-lookup"><span data-stu-id="939e4-128">Select **New Page**.</span></span>
1. <span data-ttu-id="939e4-129">V dialogovém okně **Nová stránka** vyberte šablonu a pak vyberte možnost **OK**.</span><span class="sxs-lookup"><span data-stu-id="939e4-129">In the **New Page** dialog box, select a template, and then select **OK**.</span></span>
1. <span data-ttu-id="939e4-130">Do pole **Název stránky** zadejte název stránky (například **Moje nová stránka**).</span><span class="sxs-lookup"><span data-stu-id="939e4-130">In the **Page Name** field, enter a page name (for example, **My New Page**).</span></span>
1. <span data-ttu-id="939e4-131">Do pole **Adresa URL** zadejte řetězec (slug adresy URL), čímž vytvoříte adresu URL (například **mojenovastranka**).</span><span class="sxs-lookup"><span data-stu-id="939e4-131">In the **URL** field, enter a string (URL slug) to complete the URL (for example, **mynewpage**).</span></span>
1. <span data-ttu-id="939e4-132">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="939e4-132">Select **OK**.</span></span> <span data-ttu-id="939e4-133">Zobrazí se editor stránek.</span><span class="sxs-lookup"><span data-stu-id="939e4-133">The page editor appears.</span></span> <span data-ttu-id="939e4-134">Všimněte si, že záhlaví a zápatí jsou automaticky přidány na stránku na základě vybrané šablony.</span><span class="sxs-lookup"><span data-stu-id="939e4-134">Notice that a header and a footer are automatically added to the page, based on the template that you selected.</span></span>
1. <span data-ttu-id="939e4-135">V osnově stránky vyberte pozici **Hlavní**, vyberte tlačítko se třemi tečkami (**...**) a vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="939e4-135">In the page outline, select the **Main** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="939e4-136">Vyberte **Kontejner** a potom **OK**.</span><span class="sxs-lookup"><span data-stu-id="939e4-136">Select **Container**, and then select **OK**</span></span>
1. <span data-ttu-id="939e4-137">Vyberte **Tekutý kontejner**, vyberte tlačítko se třemi tečkami a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="939e4-137">Select **Fluid Container**, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="939e4-138">Vyberte **Blok s formátovaným obsahem** a pak klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="939e4-138">Select **Content Rich block**, and then select **OK**.</span></span>
1. <span data-ttu-id="939e4-139">Vyberte **Blok s formátovaným obsahem**, vyberte tlačítko se třemi tečkami a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="939e4-139">Select **Content Rich Block**, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="939e4-140">Vyberte **Položka bloku s formátovaným obsahem** a pak klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="939e4-140">Select **Content rich block item**, and then select **OK**.</span></span>
1. <span data-ttu-id="939e4-141">V podokně vlastností vpravo vyberte možnost **Odstavec** a pak v poli zadejte **Můj testovací text**.</span><span class="sxs-lookup"><span data-stu-id="939e4-141">In the properties pane on the right, select **Paragraph**, and then, in the field, enter **My test text**.</span></span>
1. <span data-ttu-id="939e4-142">Vyberte **Uložit** a potom vyberte **Dokončit úpravy**.</span><span class="sxs-lookup"><span data-stu-id="939e4-142">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="939e4-143">Do pole **Poznámky** zadejte **Přidaná nová stránka** a pak vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="939e4-143">In the **Comments** field, enter **Added new page**, and then select **OK**.</span></span>
1. <span data-ttu-id="939e4-144">Chcete-li zobrazit náhled stránky, vyberte volbu **Náhled**.</span><span class="sxs-lookup"><span data-stu-id="939e4-144">Select **Preview** to preview your page.</span></span> <span data-ttu-id="939e4-145">Až skončíte, zavřete kartu náhledu a vraťte se do nástroje pro vytváření obsahu.</span><span class="sxs-lookup"><span data-stu-id="939e4-145">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="939e4-146">Zvolte **Publikovat**.</span><span class="sxs-lookup"><span data-stu-id="939e4-146">Select **Publish**.</span></span>
1. <span data-ttu-id="939e4-147">V cestě navigace (popis cesty) vyberte **Fabrikam** (nebo název vašeho webu).</span><span class="sxs-lookup"><span data-stu-id="939e4-147">In the navigation path (breadcrumbs), select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="939e4-148">V navigačním podokně nalevo vyberte položku **Adresy URL**.</span><span class="sxs-lookup"><span data-stu-id="939e4-148">In the navigation pane on the left, select **URLs**.</span></span>
1. <span data-ttu-id="939e4-149">V seznamu vyhledejte a vyberte svou adresu URL (**mojenovastranka)**.</span><span class="sxs-lookup"><span data-stu-id="939e4-149">Find and select your URL (**mynewpage**) in the list.</span></span>
1. <span data-ttu-id="939e4-150">Zvolte **Publikovat**.</span><span class="sxs-lookup"><span data-stu-id="939e4-150">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="939e4-151">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="939e4-151">Additional resources</span></span>

[<span data-ttu-id="939e4-152">Úprava existující webové stránky</span><span class="sxs-lookup"><span data-stu-id="939e4-152">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="939e4-153">Výběr rozvržení stránky</span><span class="sxs-lookup"><span data-stu-id="939e4-153">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="939e4-154">Správa metadat SEO</span><span class="sxs-lookup"><span data-stu-id="939e4-154">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="939e4-155">Uložení, náhled a publikování stránky</span><span class="sxs-lookup"><span data-stu-id="939e4-155">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="939e4-156">Obohacení stránky produktu</span><span class="sxs-lookup"><span data-stu-id="939e4-156">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="939e4-157">Obohacení cílové stránky kategorie</span><span class="sxs-lookup"><span data-stu-id="939e4-157">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="939e4-158">Ověření přístupnosti obsahu stránky</span><span class="sxs-lookup"><span data-stu-id="939e4-158">Verify page content accessibility</span></span>](verify-accessibility.md)
