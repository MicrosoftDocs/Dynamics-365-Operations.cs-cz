---
title: Správa metadat SEO
description: Toto téma popisuje způsob správy metadat optimalizace vyhledávačů (SEO) v aplikaci Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 1e7da7bf5c473746413e92babfa943f546b7724d
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003457"
---
# <a name="manage-seo-metadata"></a><span data-ttu-id="31b15-103">Správa metadat SEO</span><span class="sxs-lookup"><span data-stu-id="31b15-103">Manage SEO metadata</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="31b15-104">Toto téma popisuje způsob správy metadat optimalizace vyhledávačů (SEO) v aplikaci Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="31b15-104">This topic describes how to manage search engine optimization (SEO) metadata in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="31b15-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="31b15-105">Overview</span></span>

<span data-ttu-id="31b15-106">Metadata SEO pro web lze spravovat pomocí map webů a metadat stránky.</span><span class="sxs-lookup"><span data-stu-id="31b15-106">SEO metadata for a site can be managed by using site maps and page metadata.</span></span>
    
## <a name="site-maps"></a><span data-ttu-id="31b15-107">Mapy webu</span><span class="sxs-lookup"><span data-stu-id="31b15-107">Site maps</span></span>

<span data-ttu-id="31b15-108">Mapa webu je strojově čitelný seznam stránek na vašem webu ve formátu XML.</span><span class="sxs-lookup"><span data-stu-id="31b15-108">A site map is a machine-readable list, in XML format, of the pages on your website.</span></span> <span data-ttu-id="31b15-109">Je určena k použití vyhledávacími weby, aby mohly poskytovat lepší výsledky hledání z vašeho webu.</span><span class="sxs-lookup"><span data-stu-id="31b15-109">It's intended to be consumed by search engines, so that they can provide better search results from your site.</span></span> <span data-ttu-id="31b15-110">Mapy stránek mohou být ručně pokryty vyhledávacími stroji nebo publikovány v souboru robots. txt.</span><span class="sxs-lookup"><span data-stu-id="31b15-110">Site maps can be manually ingested by search engines or published in a robots.txt file.</span></span>

<span data-ttu-id="31b15-111">Dynamics 365 Commerce podporuje automatické generování map webu.</span><span class="sxs-lookup"><span data-stu-id="31b15-111">Dynamics 365 Commerce supports automatic generation of site maps.</span></span> <span data-ttu-id="31b15-112">Mapy stránek jsou při publikování a publikování stránek automaticky aktualizovány.</span><span class="sxs-lookup"><span data-stu-id="31b15-112">Site maps are automatically updated when pages are published and unpublished.</span></span>

### <a name="turn-on-site-map-generation"></a><span data-ttu-id="31b15-113">Zapnout generování mapy stránek</span><span class="sxs-lookup"><span data-stu-id="31b15-113">Turn on site map generation</span></span>

1. <span data-ttu-id="31b15-114">Přihlaste se k nástroji pro vytváření obsahu.</span><span class="sxs-lookup"><span data-stu-id="31b15-114">Sign in to the authoring tool.</span></span>
1. <span data-ttu-id="31b15-115">V části **Weby** vyberte **Fabrikam** (nebo název vašeho webu).</span><span class="sxs-lookup"><span data-stu-id="31b15-115">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="31b15-116">V navigačním podokně nalevo vyberte položku **Správa webu**.</span><span class="sxs-lookup"><span data-stu-id="31b15-116">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="31b15-117">Ujistěte se, že je zapnutá možnost **Mapy webů povoleno**.</span><span class="sxs-lookup"><span data-stu-id="31b15-117">Make sure that the **Site maps enabled** option is turned on.</span></span>

## <a name="page-metadata"></a><span data-ttu-id="31b15-118">Metadata stránky</span><span class="sxs-lookup"><span data-stu-id="31b15-118">Page metadata</span></span>

<span data-ttu-id="31b15-119">Dynamics 365 Commerce umožňuje spravovat metadata SEO pro jednotlivé stránky.</span><span class="sxs-lookup"><span data-stu-id="31b15-119">Dynamics 365 Commerce lets you manage SEO metadata for individual pages.</span></span> <span data-ttu-id="31b15-120">Tyto informace můžete zobrazit a upravit v oddílu **Vlastnosti SEO** kontejneru stránky.</span><span class="sxs-lookup"><span data-stu-id="31b15-120">You can view and modify this information in the **SEO Properties** section of a page container.</span></span> <span data-ttu-id="31b15-121">Jsou podporovány následující vlastnosti metadat SEO:</span><span class="sxs-lookup"><span data-stu-id="31b15-121">The following SEO metadata properties are supported:</span></span>

- <span data-ttu-id="31b15-122">Titul</span><span class="sxs-lookup"><span data-stu-id="31b15-122">Title</span></span>
- <span data-ttu-id="31b15-123">Popis</span><span class="sxs-lookup"><span data-stu-id="31b15-123">Description</span></span>
- <span data-ttu-id="31b15-124">Klíčová slova SEO</span><span class="sxs-lookup"><span data-stu-id="31b15-124">SEO keywords</span></span>
- <span data-ttu-id="31b15-125">Štítky standardu ARIA</span><span class="sxs-lookup"><span data-stu-id="31b15-125">Aria labels</span></span>
- <span data-ttu-id="31b15-126">noindex</span><span class="sxs-lookup"><span data-stu-id="31b15-126">noindex</span></span>
- <span data-ttu-id="31b15-127">nofollow</span><span class="sxs-lookup"><span data-stu-id="31b15-127">nofollow</span></span>
- <span data-ttu-id="31b15-128">noarchive</span><span class="sxs-lookup"><span data-stu-id="31b15-128">noarchive</span></span>
- <span data-ttu-id="31b15-129">nocache</span><span class="sxs-lookup"><span data-stu-id="31b15-129">nocache</span></span>
- <span data-ttu-id="31b15-130">noOpenDirectoryProject</span><span class="sxs-lookup"><span data-stu-id="31b15-130">noOpenDirectoryProject</span></span>
- <span data-ttu-id="31b15-131">nosnippet</span><span class="sxs-lookup"><span data-stu-id="31b15-131">nosnippet</span></span>
- <span data-ttu-id="31b15-132">noImageIndex</span><span class="sxs-lookup"><span data-stu-id="31b15-132">noImageIndex</span></span>
- <span data-ttu-id="31b15-133">unavailableAfter</span><span class="sxs-lookup"><span data-stu-id="31b15-133">unavailableAfter</span></span>

### <a name="modify-page-metadata"></a><span data-ttu-id="31b15-134">Upravit metadata stránky</span><span class="sxs-lookup"><span data-stu-id="31b15-134">Modify page metadata</span></span>

<span data-ttu-id="31b15-135">Chcete-li upravit metadata stránky, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="31b15-135">To modify page metadata, follow these steps.</span></span>

1. <span data-ttu-id="31b15-136">V části **Weby** vyberte **Fabrikam** (nebo název vašeho webu).</span><span class="sxs-lookup"><span data-stu-id="31b15-136">Under **Sites**, select the **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="31b15-137">V navigačním podokně nalevo vyberte položku **Stránky**.</span><span class="sxs-lookup"><span data-stu-id="31b15-137">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="31b15-138">Vyberte domovskou stránku, kterou chcete otevřít v editoru stránek.</span><span class="sxs-lookup"><span data-stu-id="31b15-138">Select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="31b15-139">V podokně akcí vyberte možnost **Odhlášení**.</span><span class="sxs-lookup"><span data-stu-id="31b15-139">On the Action Pane, select **Check Out**.</span></span>
1. <span data-ttu-id="31b15-140">V podokně vlastnosti vpravo rozbalte možnost **Výchozí metatagy**.</span><span class="sxs-lookup"><span data-stu-id="31b15-140">In the properties pane on the right, expand **Default metatags**.</span></span>
1. <span data-ttu-id="31b15-141">Chcete-li přidat nový metatag, vyberte možnost **Přidat** a poté zadejte požadovanou značku do pole.</span><span class="sxs-lookup"><span data-stu-id="31b15-141">To add a new metatag, select **Add**, and then enter the tag in the field.</span></span>

    <span data-ttu-id="31b15-142">Chcete-li odebrat existující metatag, vyberte symbol odpadkového koše napravo od něj.</span><span class="sxs-lookup"><span data-stu-id="31b15-142">To remove an existing metatag, select the trash can symbol to the right of it.</span></span>

1. <span data-ttu-id="31b15-143">Vyberte **Uložit** a potom **Vrátit se změnami**.</span><span class="sxs-lookup"><span data-stu-id="31b15-143">Select **Save**, and then select **Check In**.</span></span>
1. <span data-ttu-id="31b15-144">Do pole **Poznámky** zadejte **Aktualizované MetaTagy** a pak vyberte **OK.**</span><span class="sxs-lookup"><span data-stu-id="31b15-144">In the **Comments** field, enter **Updated metatags**, and then select **OK**.</span></span>
1. <span data-ttu-id="31b15-145">Chcete-li zobrazit náhled stránky, vyberte volbu **Náhled**.</span><span class="sxs-lookup"><span data-stu-id="31b15-145">Select **Preview** to preview your page.</span></span> <span data-ttu-id="31b15-146">Až skončíte, zavřete kartu náhledu a vraťte se do nástroje pro vytváření obsahu.</span><span class="sxs-lookup"><span data-stu-id="31b15-146">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="31b15-147">Zvolte **Publikovat**.</span><span class="sxs-lookup"><span data-stu-id="31b15-147">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="31b15-148">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="31b15-148">Additional resources</span></span>

[<span data-ttu-id="31b15-149">Úprava existující webové stránky</span><span class="sxs-lookup"><span data-stu-id="31b15-149">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="31b15-150">Přidání nové webové stránky</span><span class="sxs-lookup"><span data-stu-id="31b15-150">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="31b15-151">Výběr rozvržení stránky</span><span class="sxs-lookup"><span data-stu-id="31b15-151">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="31b15-152">Uložení, náhled a publikování stránky</span><span class="sxs-lookup"><span data-stu-id="31b15-152">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="31b15-153">Obohacení stránky produktu</span><span class="sxs-lookup"><span data-stu-id="31b15-153">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="31b15-154">Obohacení cílové stránky kategorie</span><span class="sxs-lookup"><span data-stu-id="31b15-154">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="31b15-155">Ověření přístupnosti obsahu stránky</span><span class="sxs-lookup"><span data-stu-id="31b15-155">Verify page content accessibility</span></span>](verify-accessibility.md)
