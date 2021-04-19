---
title: Vytváření dynamických stránek elektronického obchodu na základě parametrů adresy URL
description: Toto téma popisuje, jak nastavit stránku elektronického obchodování Microsoft Dynamics 365 Commerce, která může poskytovat dynamický obsah na základě parametrů adresy URL.
author: StuHarg
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 8f59b80880e6947e1b45c110df0e78d4bdd57c5d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795804"
---
# <a name="create-dynamic-e-commerce-pages-based-on-url-parameters"></a><span data-ttu-id="b4b82-103">Vytváření dynamických stránek elektronického obchodu na základě parametrů adresy URL</span><span class="sxs-lookup"><span data-stu-id="b4b82-103">Create dynamic e-commerce pages based on URL parameters</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b4b82-104">Toto téma popisuje, jak nastavit stránku elektronického obchodování Microsoft Dynamics 365 Commerce, která může poskytovat dynamický obsah na základě parametrů adresy URL.</span><span class="sxs-lookup"><span data-stu-id="b4b82-104">This topic describes how to set up a Microsoft Dynamics 365 Commerce e-commerce page that can serve dynamic content, based on URL parameters.</span></span>

<span data-ttu-id="b4b82-105">Stránku elektronického obchodování lze nakonfigurovat tak, aby zobrazovala různý obsah na základě segmentu v cestě URL.</span><span class="sxs-lookup"><span data-stu-id="b4b82-105">An e-commerce page can be configured to serve different content, based on a segment in the URL path.</span></span> <span data-ttu-id="b4b82-106">Proto se stránka nazývá dynamická stránka.</span><span class="sxs-lookup"><span data-stu-id="b4b82-106">Therefore, the page is known as a dynamic page.</span></span> <span data-ttu-id="b4b82-107">Segment se používá jako parametr k načtení obsahu stránky.</span><span class="sxs-lookup"><span data-stu-id="b4b82-107">The segment is used as a parameter to retrieve the page content.</span></span> <span data-ttu-id="b4b82-108">Například stránka s názvem **blog\_viewer** je vytvořena a přidružena k adrese URL `https://fabrikam.com/blog`.</span><span class="sxs-lookup"><span data-stu-id="b4b82-108">For example, a page that is named **blog\_viewer** is created and associated with the URL `https://fabrikam.com/blog`.</span></span> <span data-ttu-id="b4b82-109">Tuto stránku lze poté použít k zobrazení jiného obsahu na základě posledního segmentu v cestě URL.</span><span class="sxs-lookup"><span data-stu-id="b4b82-109">This page can then be used to show different content, based on the last segment in the URL path.</span></span> <span data-ttu-id="b4b82-110">Například poslední segment v adrese URL `https://fabrikam.com/blog/article-1` je **article-1**.</span><span class="sxs-lookup"><span data-stu-id="b4b82-110">For example, the last segment in the URL `https://fabrikam.com/blog/article-1` is **article-1**.</span></span>

<span data-ttu-id="b4b82-111">Samostatné vlastní stránky, které přepisují dynamickou stránku, lze také přidružit k segmentům v cestě URL.</span><span class="sxs-lookup"><span data-stu-id="b4b82-111">Separate custom pages that override the dynamic page can also be associated with segments in the URL path.</span></span> <span data-ttu-id="b4b82-112">Například stránka s názvem **blog\_summery** je vytvořena a přidružena k adrese URL `https://fabrikam.com/blog/about-this-blog`.</span><span class="sxs-lookup"><span data-stu-id="b4b82-112">For example, a page that is named **blog\_summary** is created and associated with the URL `https://fabrikam.com/blog/about-this-blog`.</span></span> <span data-ttu-id="b4b82-113">Je-li tato adresa URL požadována, stránka **blog\_summary** stránka, která je přidružena k parametru **/about-this-blog**, je vrácena namísto stránky **blog\_viewer**.</span><span class="sxs-lookup"><span data-stu-id="b4b82-113">When this URL is requested, the **blog\_summary** page that is associated with the **/about-this-blog** parameter is returned instead of the **blog\_viewer** page.</span></span>

> [!NOTE]
> <span data-ttu-id="b4b82-114">Funkce pro hostování, načítání a zobrazování dynamického obsahu stránky je implementována pomocí vlastního modulu.</span><span class="sxs-lookup"><span data-stu-id="b4b82-114">The functionality for hosting, retrieving, and showing dynamic page content is implemented by using a custom module.</span></span> <span data-ttu-id="b4b82-115">Další informace viz [Rozšíření online kanálu](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="b4b82-115">For more information, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

## <a name="set-up-a-dynamic-e-commerce-page"></a><span data-ttu-id="b4b82-116">Nastavení dynamické stránky elektronického obchodování</span><span class="sxs-lookup"><span data-stu-id="b4b82-116">Set up a dynamic e-commerce page</span></span>

<span data-ttu-id="b4b82-117">Chcete-li nastavit dynamickou stránku elektronického obchodování, musíte vytvořit dynamickou stránku, vytvořit základní adresu URL a nakonfigurovat cestu k dynamické stránce.</span><span class="sxs-lookup"><span data-stu-id="b4b82-117">To set up a dynamic e-commerce page, you must create the dynamic page, create the base URL, and configure the route to the dynamic page.</span></span>

### <a name="create-the-page-that-will-serve-dynamic-content"></a><span data-ttu-id="b4b82-118">Vytvoření stránky, která bude zobrazovat dynamický obsah</span><span class="sxs-lookup"><span data-stu-id="b4b82-118">Create the page that will serve dynamic content</span></span>

<span data-ttu-id="b4b82-119">Chcete-li vytvořit stránku, která bude poskytovat dynamický obsah, postupujte podle pokynů v tématu [Prodání nové stránky webu](add-new-page.md).</span><span class="sxs-lookup"><span data-stu-id="b4b82-119">To create a page that will serve dynamic content, follow the steps in [Add a new site page](add-new-page.md).</span></span> <span data-ttu-id="b4b82-120">Stránka, kterou vytvoříte, bude vyžadovat implementaci modulu, který k načtení obsahu z externího zdroje dat použije poslední segment v cestě URL.</span><span class="sxs-lookup"><span data-stu-id="b4b82-120">The page that you create will require implementation of a module that uses the last segment in the URL path to retrieve content from an external data source.</span></span> <span data-ttu-id="b4b82-121">Další informace o vývoji vlastních modulů najdete v tématu [Rozšíření online kanálu](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="b4b82-121">For more information about custom module development, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

### <a name="create-the-base-url-for-the-dynamic-page"></a><span data-ttu-id="b4b82-122">Vytvoření základní adresy URL pro dynamickou stránku</span><span class="sxs-lookup"><span data-stu-id="b4b82-122">Create the base URL for the dynamic page</span></span>

<span data-ttu-id="b4b82-123">Chcete-li vytvořit základní adresu URL pro dynamickou stránku v nástroji pro tvorbu webů Commerce, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="b4b82-123">To create the base URL for the dynamic page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="b4b82-124">Přejděte na **Adresy URL** a vyberte **Nový \> Nová adresa URL**.</span><span class="sxs-lookup"><span data-stu-id="b4b82-124">Go to **URLs**, and select **New \> New URL**.</span></span>
1. <span data-ttu-id="b4b82-125">V dialogovém okně **Vytvořit novou adresu URL** vyberte **Interní stránka**.</span><span class="sxs-lookup"><span data-stu-id="b4b82-125">In the **Create new URL** dialog box, select **Internal page**.</span></span> <span data-ttu-id="b4b82-126">V části **Cesta URL** zadejte cestu, která bude sloužit jako kořen pro dynamickou stránku (v tomto příkladu **/blog**).</span><span class="sxs-lookup"><span data-stu-id="b4b82-126">Under **URL path**, enter the path that will serve as the root for the dynamic page (in this example, **/blog**).</span></span> <span data-ttu-id="b4b82-127">Pak vyberte **Další**.</span><span class="sxs-lookup"><span data-stu-id="b4b82-127">Then select **Next**.</span></span>
1. <span data-ttu-id="b4b82-128">V dialogovém okně **Vybrat stránku** vyberte stránku, kterou jste vytvořili a která má sloužit jako dynamická stránka, a pak vyberte tlačítko **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="b4b82-128">In the **Select a page** dialog box, select the page that you created to serve as the dynamic page, and then select **Save**.</span></span>
1. <span data-ttu-id="b4b82-129">Zvolte **Publikovat**.</span><span class="sxs-lookup"><span data-stu-id="b4b82-129">Select **Publish**.</span></span>

### <a name="configure-the-route-to-the-dynamic-page"></a><span data-ttu-id="b4b82-130">Konfigurace cesty na dynamickou stránku</span><span class="sxs-lookup"><span data-stu-id="b4b82-130">Configure the route to the dynamic page</span></span>

<span data-ttu-id="b4b82-131">Chcete-li nakonfigurovat cestu k dynamické stránce v nástroji pro tvorbu webů Commerce, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="b4b82-131">To configure the route to the dynamic page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="b4b82-132">Přejděte na **Nastavení webu \> Rozšíření**.</span><span class="sxs-lookup"><span data-stu-id="b4b82-132">Go to **Site Settings \> Extensions**.</span></span>
1. <span data-ttu-id="b4b82-133">V části **Parametrizované cesty URL** vyberte **Přidat** a poté zadejte cestu URL, kterou jste zadali při vytváření adresy URL (v tomto příkladu **/blog**).</span><span class="sxs-lookup"><span data-stu-id="b4b82-133">Under **Parameterized URL paths**, select **Add**, and then enter the URL path that you entered when you created the URL (in this example, **/blog**).</span></span>
1. <span data-ttu-id="b4b82-134">Vyberte možnost **Uložit a publikovat**.</span><span class="sxs-lookup"><span data-stu-id="b4b82-134">Select **Save and publish**.</span></span>

<span data-ttu-id="b4b82-135">Po nakonfigurování trasy všechny požadavky na cestu parametrizované adresy URL vrátí stránku, která je přidružena k této adrese URL.</span><span class="sxs-lookup"><span data-stu-id="b4b82-135">After the route is configured, all requests to the parameterized URL path will return the page that is associated with that URL.</span></span> <span data-ttu-id="b4b82-136">Pokud nějaké požadavky obsahují další segment, vrátí se přidružená stránka a obsah stránky se načte pomocí segmentu jako parametru.</span><span class="sxs-lookup"><span data-stu-id="b4b82-136">If any requests contain an additional segment, the associated page will be returned, and the page content will be retrieved by using the segment as a parameter.</span></span> <span data-ttu-id="b4b82-137">Například `https://fabrikam.com/blog/article-1` vrátí stránku **blog\_summary** a její obsah se načte pomocí parametru **/article-1**.</span><span class="sxs-lookup"><span data-stu-id="b4b82-137">For example, `https://fabrikam.com/blog/article-1` will return the **blog\_summary** page, and the page content will be retrieved by using the **/article-1** parameter.</span></span>

## <a name="override-a-parameterized-url-with-a-custom-page"></a><span data-ttu-id="b4b82-138">Přepsání parametrizované adresy URL vlastní stránkou</span><span class="sxs-lookup"><span data-stu-id="b4b82-138">Override a parameterized URL with a custom page</span></span>

<span data-ttu-id="b4b82-139">Chcete-li přepsat parametrizovanou adresu URL vlastní stránkou v nástroji pro tvorbu webů Commerce, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="b4b82-139">To override a parameterized URL with a custom page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="b4b82-140">Přejděte na **Adresy URL** a vyberte **Nový \> Nová adresa URL**.</span><span class="sxs-lookup"><span data-stu-id="b4b82-140">Go to **URLs**, and select **New \> New URL**.</span></span>
1. <span data-ttu-id="b4b82-141">V dialogovém okně **Vytvořit novou adresu URL** vyberte **Interní stránka**.</span><span class="sxs-lookup"><span data-stu-id="b4b82-141">In the **Create new URL** dialog box, select **Internal page**.</span></span> <span data-ttu-id="b4b82-142">V části **Cesta URL** zadejte cestu, která zahrnuje segment, který má být přepsán (v tomto příkladu **/blog/about-this-blog**).</span><span class="sxs-lookup"><span data-stu-id="b4b82-142">Under **URL path**, enter the path that includes the segment to override (in this example, **/blog/about-this-blog**).</span></span> <span data-ttu-id="b4b82-143">Pak vyberte **Další**.</span><span class="sxs-lookup"><span data-stu-id="b4b82-143">Then select **Next**.</span></span>
1. <span data-ttu-id="b4b82-144">V dialogovém okně **Vybrat stránku** vyberte vlastní stránku a poté vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="b4b82-144">In the **Select a page** dialog box, select the custom page, and then select **Save**.</span></span>
1. <span data-ttu-id="b4b82-145">Zvolte **Publikovat**.</span><span class="sxs-lookup"><span data-stu-id="b4b82-145">Select **Publish**.</span></span>
1. <span data-ttu-id="b4b82-146">Pokud vlastní stránka ještě nebyla publikována, přejděte na možnost **Stránky**, vyberte vlastní stránku a poté vyberte **Publikovat**.</span><span class="sxs-lookup"><span data-stu-id="b4b82-146">If the custom page hasn't yet been published, go to **Pages**, select the custom page, and then select **Publish**.</span></span>

<span data-ttu-id="b4b82-147">Po publikování vlastní stránky se zobrazí místo dynamické stránky s parametrizovaným obsahem.</span><span class="sxs-lookup"><span data-stu-id="b4b82-147">After the custom page is published, it will be served instead of the dynamic page that has parameterized content.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b4b82-148">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="b4b82-148">Additional resources</span></span>

[<span data-ttu-id="b4b82-149">Úprava existující webové stránky</span><span class="sxs-lookup"><span data-stu-id="b4b82-149">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="b4b82-150">Přidání nové webové stránky</span><span class="sxs-lookup"><span data-stu-id="b4b82-150">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="b4b82-151">Výběr rozvržení stránky</span><span class="sxs-lookup"><span data-stu-id="b4b82-151">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="b4b82-152">Správa metadat SEO</span><span class="sxs-lookup"><span data-stu-id="b4b82-152">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="b4b82-153">Uložení, náhled a publikování stránky</span><span class="sxs-lookup"><span data-stu-id="b4b82-153">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="b4b82-154">Obohacení stránky produktu</span><span class="sxs-lookup"><span data-stu-id="b4b82-154">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="b4b82-155">Obohacení cílové stránky kategorie</span><span class="sxs-lookup"><span data-stu-id="b4b82-155">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="b4b82-156">Ověření přístupnosti obsahu stránky</span><span class="sxs-lookup"><span data-stu-id="b4b82-156">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="b4b82-157">Rozšiřitelnost online kanálu</span><span class="sxs-lookup"><span data-stu-id="b4b82-157">Online channel extensibility</span></span>](e-commerce-extensibility/overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
