---
title: Ověření přístupnosti obsahu stránky
description: Toto téma popisuje, jak ověřit přístupnost obsahu stránky v Microsoft Dynamics 365 Commerce.
author: josaw1
manager: annbe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2019-12-19
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 186044fc7a360f227cecffb39bad0e225245dd4d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5210964"
---
# <a name="verify-page-content-accessibility"></a><span data-ttu-id="1c0c7-103">Ověření přístupnosti obsahu stránky</span><span class="sxs-lookup"><span data-stu-id="1c0c7-103">Verify page content accessibility</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="1c0c7-104">Toto téma popisuje, jak ověřit přístupnost obsahu stránky v Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1c0c7-104">This topic describes how to verify the accessibility of page content in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="1c0c7-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="1c0c7-105">Overview</span></span>

<span data-ttu-id="1c0c7-106">Po dokončení změn stránky byste měli zajistit, aby byl obsah přístupný všem uživatelům na webu.</span><span class="sxs-lookup"><span data-stu-id="1c0c7-106">When you've finished changing a page, you should make sure that the content is accessible to everyone on the web.</span></span> <span data-ttu-id="1c0c7-107">V nástrojích pro vytváření obchodních společností můžete snadno ověřit přístupnost obsahu stránky pomocí integrované služby [Microsoft Accessibility Insights](https://accessibilityinsights.io/).</span><span class="sxs-lookup"><span data-stu-id="1c0c7-107">In the Commerce authoring tools, you can easily verify the accessibility of page content by using the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service.</span></span> <span data-ttu-id="1c0c7-108">Tato služba ověřuje obsah stránky podle nejnovějších pokynů pro usnadnění přístupu [konsorcia W3C (World Wide Web Consortium)](https://www.w3.org/standards/webdesign/accessibility).</span><span class="sxs-lookup"><span data-stu-id="1c0c7-108">This service verifies your page content against the latest [World Wide Web Consortium (W3C) accessibility](https://www.w3.org/standards/webdesign/accessibility) guidelines.</span></span>

<span data-ttu-id="1c0c7-109">Integrace [Microsoft Accessibility Insights](https://accessibilityinsights.io/) musí být zapnuta na úrovni klienta nebo webu před použitím.</span><span class="sxs-lookup"><span data-stu-id="1c0c7-109">The [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration must be turned on at the tenant or site level before you can use it.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-all-the-sites-in-your-tenant"></a><span data-ttu-id="1c0c7-110">Zapněte Microsoft Accessibility Insights pro všechny weby v klientovi.</span><span class="sxs-lookup"><span data-stu-id="1c0c7-110">Turn on Microsoft Accessibility Insights for all the sites in your tenant</span></span>

<span data-ttu-id="1c0c7-111">Chcete-li zapnout integraci [Microsoft Accessibility Insights](https://accessibilityinsights.io/) pro všechny weby Commerce ve vašem klientovi, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="1c0c7-111">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for all the Commerce sites in your tenant, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="1c0c7-112">Chcete-li získat přístup k nastavení klienta, musíte být přihlášen ke Commerce jako správce systému.</span><span class="sxs-lookup"><span data-stu-id="1c0c7-112">To access tenant settings, you must be signed in to Commerce as a system admin.</span></span>

1. <span data-ttu-id="1c0c7-113">Přihlaste se k Commerce jako správce systému.</span><span class="sxs-lookup"><span data-stu-id="1c0c7-113">Sign in to Commerce as a system admin.</span></span>
1. <span data-ttu-id="1c0c7-114">V levém navigačním podokně vyberte **Nastavení klienta** (vedle symbolu ozubeného kola), čímž jej rozbalíte.</span><span class="sxs-lookup"><span data-stu-id="1c0c7-114">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
1. <span data-ttu-id="1c0c7-115">V části **Nastavení klienta** vyberte **Funkce**.</span><span class="sxs-lookup"><span data-stu-id="1c0c7-115">Under **Tenant Settings**, select **Features**.</span></span>
1. <span data-ttu-id="1c0c7-116">Nastavte možnost **Kontrola dostupnosti** na **Zapnuto**.</span><span class="sxs-lookup"><span data-stu-id="1c0c7-116">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-a-single-site"></a><span data-ttu-id="1c0c7-117">Zapnout Microsoft Accessibility Insights pro jeden web</span><span class="sxs-lookup"><span data-stu-id="1c0c7-117">Turn on Microsoft Accessibility Insights for a single site</span></span>

<span data-ttu-id="1c0c7-118">Chcete-li zapnout integraci [Microsoft Accessibility Insights](https://accessibilityinsights.io/) pro jeden web Commerce, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="1c0c7-118">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for a single Commerce site, follow these steps.</span></span>

1. <span data-ttu-id="1c0c7-119">V části **Weby** vyberte **Fabrikam** (nebo název vašeho webu).</span><span class="sxs-lookup"><span data-stu-id="1c0c7-119">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="1c0c7-120">V levém navigačním podokně vyberte **Nastavení webu** a rozbalte je.</span><span class="sxs-lookup"><span data-stu-id="1c0c7-120">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="1c0c7-121">V části **nastavení webu** vyberte **Funkce**.</span><span class="sxs-lookup"><span data-stu-id="1c0c7-121">Under **Site Settings**, select **Features**.</span></span>
1. <span data-ttu-id="1c0c7-122">Nastavte možnost **Kontrola dostupnosti** na **Zapnuto**.</span><span class="sxs-lookup"><span data-stu-id="1c0c7-122">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="verify-the-accessibility-of-the-content-on-the-home-page"></a><span data-ttu-id="1c0c7-123">Ověření dostupnosti obsahu na domovské stránce</span><span class="sxs-lookup"><span data-stu-id="1c0c7-123">Verify the accessibility of the content on the home page</span></span>

<span data-ttu-id="1c0c7-124">Chcete-li použít službu [Microsoft Accessibility Insights](https://accessibilityinsights.io/) k prohledání a ověření obsahu domovské stránky v Commerce, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="1c0c7-124">To use the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service to scan and verify the content of your home page in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="1c0c7-125">V části **Weby** vyberte **Fabrikam** (nebo název vašeho webu).</span><span class="sxs-lookup"><span data-stu-id="1c0c7-125">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="1c0c7-126">V levém navigačním podokně vyberte položku **Stránky**.</span><span class="sxs-lookup"><span data-stu-id="1c0c7-126">In the left navigation pane, select **Pages**.</span></span>
1. <span data-ttu-id="1c0c7-127">Vyhledejte a vyberte domovskou stránku, kterou chcete otevřít v editoru stránek.</span><span class="sxs-lookup"><span data-stu-id="1c0c7-127">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="1c0c7-128">Na příkazovém řádku vyberte možnost **Zkontrolovat dostupnost**.</span><span class="sxs-lookup"><span data-stu-id="1c0c7-128">On the command bar, select **Check accessibility**.</span></span> <span data-ttu-id="1c0c7-129">Zobrazí se stránka **Zkontrolovat dostupnost**.</span><span class="sxs-lookup"><span data-stu-id="1c0c7-129">The **Check Accessibility** page appears.</span></span>
1. <span data-ttu-id="1c0c7-130">Po dokončení skenování si prohlédněte obsah sestavy.</span><span class="sxs-lookup"><span data-stu-id="1c0c7-130">After the scan is completed, review the contents of the report.</span></span>
1. <span data-ttu-id="1c0c7-131">Pokud se některé kontroly nezdařily, vyberte každou nezdařené kontrolní položku a rozbalte ji tak, aby bylo možné zobrazit další podrobnosti.</span><span class="sxs-lookup"><span data-stu-id="1c0c7-131">If any checks failed, select each failed check item to expand it so that you can view more details.</span></span>
1. <span data-ttu-id="1c0c7-132">Chcete-li sestavu po dokončení revize zavřít, posuňte se na konec stránky **Zkontrolovat dostupnost** a vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="1c0c7-132">To close the report after you've finished reviewing it, scroll to the bottom of the **Check Accessibility** page, and select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1c0c7-133">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="1c0c7-133">Additional resources</span></span>

[<span data-ttu-id="1c0c7-134">Úprava existující webové stránky</span><span class="sxs-lookup"><span data-stu-id="1c0c7-134">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="1c0c7-135">Přidání nové webové stránky</span><span class="sxs-lookup"><span data-stu-id="1c0c7-135">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="1c0c7-136">Výběr rozvržení stránky</span><span class="sxs-lookup"><span data-stu-id="1c0c7-136">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="1c0c7-137">Správa metadat SEO</span><span class="sxs-lookup"><span data-stu-id="1c0c7-137">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="1c0c7-138">Uložení, náhled a publikování stránky</span><span class="sxs-lookup"><span data-stu-id="1c0c7-138">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="1c0c7-139">Obohacení stránky produktu</span><span class="sxs-lookup"><span data-stu-id="1c0c7-139">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="1c0c7-140">Obohacení cílové stránky kategorie</span><span class="sxs-lookup"><span data-stu-id="1c0c7-140">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="1c0c7-141">Vytváření dynamických stránek elektronického obchodu na základě parametrů adresy URL</span><span class="sxs-lookup"><span data-stu-id="1c0c7-141">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]