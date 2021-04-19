---
title: Správa metadat SEO
description: Toto téma popisuje způsob správy metadat optimalizace vyhledávačů (SEO) v aplikaci Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1e03ef346df92a94b0a403f241d0f7d1f64fd210
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794204"
---
# <a name="manage-seo-metadata"></a><span data-ttu-id="1b5d0-103">Správa metadat SEO</span><span class="sxs-lookup"><span data-stu-id="1b5d0-103">Manage SEO metadata</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1b5d0-104">Toto téma popisuje způsob správy metadat optimalizace vyhledávačů (SEO) v aplikaci Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1b5d0-104">This topic describes how to manage search engine optimization (SEO) metadata in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="1b5d0-105">Metadata SEO pro web lze spravovat pomocí map webů a metadat stránky.</span><span class="sxs-lookup"><span data-stu-id="1b5d0-105">SEO metadata for a site can be managed by using site maps and page metadata.</span></span>
    
## <a name="site-maps"></a><span data-ttu-id="1b5d0-106">Mapy webu</span><span class="sxs-lookup"><span data-stu-id="1b5d0-106">Site maps</span></span>

<span data-ttu-id="1b5d0-107">Mapa webu je strojově čitelný seznam stránek na vašem webu ve formátu XML.</span><span class="sxs-lookup"><span data-stu-id="1b5d0-107">A site map is a machine-readable list, in XML format, of the pages on your website.</span></span> <span data-ttu-id="1b5d0-108">Je určena k použití vyhledávacími weby, aby mohly poskytovat lepší výsledky hledání z vašeho webu.</span><span class="sxs-lookup"><span data-stu-id="1b5d0-108">It's intended to be consumed by search engines, so that they can provide better search results from your site.</span></span> <span data-ttu-id="1b5d0-109">Mapy stránek mohou být ručně pokryty vyhledávacími stroji nebo publikovány v souboru robots. txt.</span><span class="sxs-lookup"><span data-stu-id="1b5d0-109">Site maps can be manually ingested by search engines or published in a robots.txt file.</span></span>

<span data-ttu-id="1b5d0-110">Dynamics 365 Commerce podporuje automatické generování map webu.</span><span class="sxs-lookup"><span data-stu-id="1b5d0-110">Dynamics 365 Commerce supports automatic generation of site maps.</span></span> <span data-ttu-id="1b5d0-111">Mapy stránek jsou při publikování a publikování stránek automaticky aktualizovány.</span><span class="sxs-lookup"><span data-stu-id="1b5d0-111">Site maps are automatically updated when pages are published and unpublished.</span></span>

### <a name="turn-on-site-map-generation"></a><span data-ttu-id="1b5d0-112">Zapnout generování mapy stránek</span><span class="sxs-lookup"><span data-stu-id="1b5d0-112">Turn on site map generation</span></span>

1. <span data-ttu-id="1b5d0-113">Přihlaste se k nástroji pro vytváření obsahu.</span><span class="sxs-lookup"><span data-stu-id="1b5d0-113">Sign in to the authoring tool.</span></span>
1. <span data-ttu-id="1b5d0-114">V části **Weby** vyberte **Fabrikam** (nebo název vašeho webu).</span><span class="sxs-lookup"><span data-stu-id="1b5d0-114">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="1b5d0-115">V navigačním podokně nalevo vyberte položku **Správa webu**.</span><span class="sxs-lookup"><span data-stu-id="1b5d0-115">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="1b5d0-116">Ujistěte se, že je zapnutá možnost **Mapy webů povoleno**.</span><span class="sxs-lookup"><span data-stu-id="1b5d0-116">Make sure that the **Site maps enabled** option is turned on.</span></span>

## <a name="page-metadata"></a><span data-ttu-id="1b5d0-117">Metadata stránky</span><span class="sxs-lookup"><span data-stu-id="1b5d0-117">Page metadata</span></span>

<span data-ttu-id="1b5d0-118">Dynamics 365 Commerce umožňuje spravovat metadata SEO pro jednotlivé stránky.</span><span class="sxs-lookup"><span data-stu-id="1b5d0-118">Dynamics 365 Commerce lets you manage SEO metadata for individual pages.</span></span> <span data-ttu-id="1b5d0-119">Tyto informace můžete zobrazit a upravit v oddílu **Vlastnosti SEO** kontejneru stránky.</span><span class="sxs-lookup"><span data-stu-id="1b5d0-119">You can view and modify this information in the **SEO Properties** section of a page container.</span></span> <span data-ttu-id="1b5d0-120">Jsou podporovány následující vlastnosti metadat SEO:</span><span class="sxs-lookup"><span data-stu-id="1b5d0-120">The following SEO metadata properties are supported:</span></span>

- <span data-ttu-id="1b5d0-121">Titul</span><span class="sxs-lookup"><span data-stu-id="1b5d0-121">Title</span></span>
- <span data-ttu-id="1b5d0-122">Popis</span><span class="sxs-lookup"><span data-stu-id="1b5d0-122">Description</span></span>
- <span data-ttu-id="1b5d0-123">Klíčová slova SEO</span><span class="sxs-lookup"><span data-stu-id="1b5d0-123">SEO keywords</span></span>
- <span data-ttu-id="1b5d0-124">Štítky standardu ARIA</span><span class="sxs-lookup"><span data-stu-id="1b5d0-124">Aria labels</span></span>
- <span data-ttu-id="1b5d0-125">noindex</span><span class="sxs-lookup"><span data-stu-id="1b5d0-125">noindex</span></span>
- <span data-ttu-id="1b5d0-126">nofollow</span><span class="sxs-lookup"><span data-stu-id="1b5d0-126">nofollow</span></span>
- <span data-ttu-id="1b5d0-127">noarchive</span><span class="sxs-lookup"><span data-stu-id="1b5d0-127">noarchive</span></span>
- <span data-ttu-id="1b5d0-128">nocache</span><span class="sxs-lookup"><span data-stu-id="1b5d0-128">nocache</span></span>
- <span data-ttu-id="1b5d0-129">noOpenDirectoryProject</span><span class="sxs-lookup"><span data-stu-id="1b5d0-129">noOpenDirectoryProject</span></span>
- <span data-ttu-id="1b5d0-130">nosnippet</span><span class="sxs-lookup"><span data-stu-id="1b5d0-130">nosnippet</span></span>
- <span data-ttu-id="1b5d0-131">noImageIndex</span><span class="sxs-lookup"><span data-stu-id="1b5d0-131">noImageIndex</span></span>
- <span data-ttu-id="1b5d0-132">unavailableAfter</span><span class="sxs-lookup"><span data-stu-id="1b5d0-132">unavailableAfter</span></span>

### <a name="modify-page-metadata"></a><span data-ttu-id="1b5d0-133">Upravit metadata stránky</span><span class="sxs-lookup"><span data-stu-id="1b5d0-133">Modify page metadata</span></span>

<span data-ttu-id="1b5d0-134">Chcete-li upravit metadata stránky, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="1b5d0-134">To modify page metadata, follow these steps.</span></span>

1. <span data-ttu-id="1b5d0-135">V části **Weby** vyberte **Fabrikam** (nebo název vašeho webu).</span><span class="sxs-lookup"><span data-stu-id="1b5d0-135">Under **Sites**, select the **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="1b5d0-136">V navigačním podokně nalevo vyberte položku **Stránky**.</span><span class="sxs-lookup"><span data-stu-id="1b5d0-136">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="1b5d0-137">Vyberte domovskou stránku, kterou chcete otevřít v editoru stránek.</span><span class="sxs-lookup"><span data-stu-id="1b5d0-137">Select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="1b5d0-138">Na příkazovém řádku vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="1b5d0-138">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="1b5d0-139">V podokně vlastnosti vpravo rozbalte možnost **Výchozí metatagy**.</span><span class="sxs-lookup"><span data-stu-id="1b5d0-139">In the properties pane on the right, expand **Default metatags**.</span></span>
1. <span data-ttu-id="1b5d0-140">Chcete-li přidat nový metatag, vyberte možnost **Přidat** a poté zadejte požadovanou značku do pole.</span><span class="sxs-lookup"><span data-stu-id="1b5d0-140">To add a new metatag, select **Add**, and then enter the tag in the field.</span></span> <span data-ttu-id="1b5d0-141">Chcete-li odebrat existující metatag, vyberte symbol odpadkového koše napravo od něj.</span><span class="sxs-lookup"><span data-stu-id="1b5d0-141">To remove an existing metatag, select the trash can symbol to the right of it.</span></span>
1. <span data-ttu-id="1b5d0-142">Vyberte **Uložit** a potom vyberte **Dokončit úpravy**.</span><span class="sxs-lookup"><span data-stu-id="1b5d0-142">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="1b5d0-143">Do pole **Poznámky** zadejte **Aktualizované MetaTagy** a pak vyberte **OK.**</span><span class="sxs-lookup"><span data-stu-id="1b5d0-143">In the **Comments** field, enter **Updated metatags**, and then select **OK**.</span></span>
1. <span data-ttu-id="1b5d0-144">Chcete-li zobrazit náhled stránky, vyberte volbu **Náhled**.</span><span class="sxs-lookup"><span data-stu-id="1b5d0-144">Select **Preview** to preview your page.</span></span> <span data-ttu-id="1b5d0-145">Až skončíte, zavřete kartu náhledu a vraťte se do nástroje pro vytváření obsahu.</span><span class="sxs-lookup"><span data-stu-id="1b5d0-145">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="1b5d0-146">Zvolte **Publikovat**.</span><span class="sxs-lookup"><span data-stu-id="1b5d0-146">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1b5d0-147">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="1b5d0-147">Additional resources</span></span>

[<span data-ttu-id="1b5d0-148">Úprava existující webové stránky</span><span class="sxs-lookup"><span data-stu-id="1b5d0-148">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="1b5d0-149">Přidání nové webové stránky</span><span class="sxs-lookup"><span data-stu-id="1b5d0-149">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="1b5d0-150">Výběr rozvržení stránky</span><span class="sxs-lookup"><span data-stu-id="1b5d0-150">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="1b5d0-151">Uložení, náhled a publikování stránky</span><span class="sxs-lookup"><span data-stu-id="1b5d0-151">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="1b5d0-152">Obohacení stránky produktu</span><span class="sxs-lookup"><span data-stu-id="1b5d0-152">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="1b5d0-153">Obohacení cílové stránky kategorie</span><span class="sxs-lookup"><span data-stu-id="1b5d0-153">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="1b5d0-154">Ověření přístupnosti obsahu stránky</span><span class="sxs-lookup"><span data-stu-id="1b5d0-154">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="1b5d0-155">Vytváření dynamických stránek elektronického obchodu na základě parametrů adresy URL</span><span class="sxs-lookup"><span data-stu-id="1b5d0-155">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
