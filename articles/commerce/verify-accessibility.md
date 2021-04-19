---
title: Ověření přístupnosti obsahu stránky
description: Toto téma popisuje, jak ověřit přístupnost obsahu stránky v Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2019-12-19
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 885696c13b0e5353e6dbd9dc21cf075d5e301786
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791624"
---
# <a name="verify-page-content-accessibility"></a><span data-ttu-id="228ab-103">Ověření přístupnosti obsahu stránky</span><span class="sxs-lookup"><span data-stu-id="228ab-103">Verify page content accessibility</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="228ab-104">Toto téma popisuje, jak ověřit přístupnost obsahu stránky v Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="228ab-104">This topic describes how to verify the accessibility of page content in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="228ab-105">Po dokončení změn stránky byste měli zajistit, aby byl obsah přístupný všem uživatelům na webu.</span><span class="sxs-lookup"><span data-stu-id="228ab-105">When you've finished changing a page, you should make sure that the content is accessible to everyone on the web.</span></span> <span data-ttu-id="228ab-106">V nástrojích pro vytváření obchodních společností můžete snadno ověřit přístupnost obsahu stránky pomocí integrované služby [Microsoft Accessibility Insights](https://accessibilityinsights.io/).</span><span class="sxs-lookup"><span data-stu-id="228ab-106">In the Commerce authoring tools, you can easily verify the accessibility of page content by using the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service.</span></span> <span data-ttu-id="228ab-107">Tato služba ověřuje obsah stránky podle nejnovějších pokynů pro usnadnění přístupu [konsorcia W3C (World Wide Web Consortium)](https://www.w3.org/standards/webdesign/accessibility).</span><span class="sxs-lookup"><span data-stu-id="228ab-107">This service verifies your page content against the latest [World Wide Web Consortium (W3C) accessibility](https://www.w3.org/standards/webdesign/accessibility) guidelines.</span></span>

<span data-ttu-id="228ab-108">Integrace [Microsoft Accessibility Insights](https://accessibilityinsights.io/) musí být zapnuta na úrovni klienta nebo webu před použitím.</span><span class="sxs-lookup"><span data-stu-id="228ab-108">The [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration must be turned on at the tenant or site level before you can use it.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-all-the-sites-in-your-tenant"></a><span data-ttu-id="228ab-109">Zapněte Microsoft Accessibility Insights pro všechny weby v klientovi.</span><span class="sxs-lookup"><span data-stu-id="228ab-109">Turn on Microsoft Accessibility Insights for all the sites in your tenant</span></span>

<span data-ttu-id="228ab-110">Chcete-li zapnout integraci [Microsoft Accessibility Insights](https://accessibilityinsights.io/) pro všechny weby Commerce ve vašem klientovi, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="228ab-110">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for all the Commerce sites in your tenant, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="228ab-111">Chcete-li získat přístup k nastavení klienta, musíte být přihlášen ke Commerce jako správce systému.</span><span class="sxs-lookup"><span data-stu-id="228ab-111">To access tenant settings, you must be signed in to Commerce as a system admin.</span></span>

1. <span data-ttu-id="228ab-112">Přihlaste se k Commerce jako správce systému.</span><span class="sxs-lookup"><span data-stu-id="228ab-112">Sign in to Commerce as a system admin.</span></span>
1. <span data-ttu-id="228ab-113">V levém navigačním podokně vyberte **Nastavení klienta** (vedle symbolu ozubeného kola), čímž jej rozbalíte.</span><span class="sxs-lookup"><span data-stu-id="228ab-113">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
1. <span data-ttu-id="228ab-114">V části **Nastavení klienta** vyberte **Funkce**.</span><span class="sxs-lookup"><span data-stu-id="228ab-114">Under **Tenant Settings**, select **Features**.</span></span>
1. <span data-ttu-id="228ab-115">Nastavte možnost **Kontrola dostupnosti** na **Zapnuto**.</span><span class="sxs-lookup"><span data-stu-id="228ab-115">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-a-single-site"></a><span data-ttu-id="228ab-116">Zapnout Microsoft Accessibility Insights pro jeden web</span><span class="sxs-lookup"><span data-stu-id="228ab-116">Turn on Microsoft Accessibility Insights for a single site</span></span>

<span data-ttu-id="228ab-117">Chcete-li zapnout integraci [Microsoft Accessibility Insights](https://accessibilityinsights.io/) pro jeden web Commerce, postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="228ab-117">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for a single Commerce site, follow these steps.</span></span>

1. <span data-ttu-id="228ab-118">V části **Weby** vyberte **Fabrikam** (nebo název vašeho webu).</span><span class="sxs-lookup"><span data-stu-id="228ab-118">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="228ab-119">V levém navigačním podokně vyberte **Nastavení webu** a rozbalte je.</span><span class="sxs-lookup"><span data-stu-id="228ab-119">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="228ab-120">V části **nastavení webu** vyberte **Funkce**.</span><span class="sxs-lookup"><span data-stu-id="228ab-120">Under **Site Settings**, select **Features**.</span></span>
1. <span data-ttu-id="228ab-121">Nastavte možnost **Kontrola dostupnosti** na **Zapnuto**.</span><span class="sxs-lookup"><span data-stu-id="228ab-121">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="verify-the-accessibility-of-the-content-on-the-home-page"></a><span data-ttu-id="228ab-122">Ověření dostupnosti obsahu na domovské stránce</span><span class="sxs-lookup"><span data-stu-id="228ab-122">Verify the accessibility of the content on the home page</span></span>

<span data-ttu-id="228ab-123">Chcete-li použít službu [Microsoft Accessibility Insights](https://accessibilityinsights.io/) k prohledání a ověření obsahu domovské stránky v Commerce, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="228ab-123">To use the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service to scan and verify the content of your home page in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="228ab-124">V části **Weby** vyberte **Fabrikam** (nebo název vašeho webu).</span><span class="sxs-lookup"><span data-stu-id="228ab-124">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="228ab-125">V levém navigačním podokně vyberte položku **Stránky**.</span><span class="sxs-lookup"><span data-stu-id="228ab-125">In the left navigation pane, select **Pages**.</span></span>
1. <span data-ttu-id="228ab-126">Vyhledejte a vyberte domovskou stránku, kterou chcete otevřít v editoru stránek.</span><span class="sxs-lookup"><span data-stu-id="228ab-126">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="228ab-127">Na příkazovém řádku vyberte možnost **Zkontrolovat dostupnost**.</span><span class="sxs-lookup"><span data-stu-id="228ab-127">On the command bar, select **Check accessibility**.</span></span> <span data-ttu-id="228ab-128">Zobrazí se stránka **Zkontrolovat dostupnost**.</span><span class="sxs-lookup"><span data-stu-id="228ab-128">The **Check Accessibility** page appears.</span></span>
1. <span data-ttu-id="228ab-129">Po dokončení skenování si prohlédněte obsah sestavy.</span><span class="sxs-lookup"><span data-stu-id="228ab-129">After the scan is completed, review the contents of the report.</span></span>
1. <span data-ttu-id="228ab-130">Pokud se některé kontroly nezdařily, vyberte každou nezdařené kontrolní položku a rozbalte ji tak, aby bylo možné zobrazit další podrobnosti.</span><span class="sxs-lookup"><span data-stu-id="228ab-130">If any checks failed, select each failed check item to expand it so that you can view more details.</span></span>
1. <span data-ttu-id="228ab-131">Chcete-li sestavu po dokončení revize zavřít, posuňte se na konec stránky **Zkontrolovat dostupnost** a vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="228ab-131">To close the report after you've finished reviewing it, scroll to the bottom of the **Check Accessibility** page, and select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="228ab-132">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="228ab-132">Additional resources</span></span>

[<span data-ttu-id="228ab-133">Úprava existující webové stránky</span><span class="sxs-lookup"><span data-stu-id="228ab-133">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="228ab-134">Přidání nové webové stránky</span><span class="sxs-lookup"><span data-stu-id="228ab-134">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="228ab-135">Výběr rozvržení stránky</span><span class="sxs-lookup"><span data-stu-id="228ab-135">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="228ab-136">Správa metadat SEO</span><span class="sxs-lookup"><span data-stu-id="228ab-136">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="228ab-137">Uložení, náhled a publikování stránky</span><span class="sxs-lookup"><span data-stu-id="228ab-137">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="228ab-138">Obohacení stránky produktu</span><span class="sxs-lookup"><span data-stu-id="228ab-138">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="228ab-139">Obohacení cílové stránky kategorie</span><span class="sxs-lookup"><span data-stu-id="228ab-139">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="228ab-140">Vytváření dynamických stránek elektronického obchodu na základě parametrů adresy URL</span><span class="sxs-lookup"><span data-stu-id="228ab-140">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
