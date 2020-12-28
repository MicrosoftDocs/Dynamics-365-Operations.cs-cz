---
title: Zvažování optimalizace webového vyhledávače pro váš web
description: Toto téma obsahuje informace o optimalizaci webového vyhledávače (SEO) pro váš web od rozvoje do výroby.
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
ms.openlocfilehash: 6ffc772addb330abe7205007662a3f3e08a3e47f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410866"
---
# <a name="search-engine-optimization-seo-considerations-for-your-site"></a><span data-ttu-id="41a37-103">Zvažování optimalizace webového vyhledávače pro váš web</span><span class="sxs-lookup"><span data-stu-id="41a37-103">Search engine optimization (SEO) considerations for your site</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="41a37-104">Toto téma obsahuje informace o optimalizaci webového vyhledávače (SEO) pro váš web od rozvoje do výroby.</span><span class="sxs-lookup"><span data-stu-id="41a37-104">This topic covers earch engine optimization (SEO) considerations for your site from development to production.</span></span>

## <a name="a-site-that-is-under-development"></a><span data-ttu-id="41a37-105">Web, který je ve vývoji</span><span class="sxs-lookup"><span data-stu-id="41a37-105">A site that is under development</span></span>

<span data-ttu-id="41a37-106">Zatímco probíhá vývoj webu, všechny stránky webu by měly mít metaznačky **NOINDEX** a **NOFOLLOW** aby vyhledávače nemusely stránky indexovat a ukládat verze vývoje vašeho webu do mezipaměti.</span><span class="sxs-lookup"><span data-stu-id="41a37-106">While a site is under development, all site pages should have the **NOINDEX** and **NOFOLLOW** meta tags, so that search engines don't index the pages and store development versions of your site in their cache.</span></span> <span data-ttu-id="41a37-107">Chcete-li provést tuto konfiguraci, je nutné přidat výchozí modul metaznačky do šablony stránky webu.</span><span class="sxs-lookup"><span data-stu-id="41a37-107">To do this configuration, you must add the default meta tags module to the site page template.</span></span> <span data-ttu-id="41a37-108">Výchozí vlastnosti metaznaček budou poté k dispozici v oddílu vlastnosti SEO v editoru stránek.</span><span class="sxs-lookup"><span data-stu-id="41a37-108">The default meta tags properties will then be available in the SEO properties section in the page editor.</span></span> <span data-ttu-id="41a37-109">Tyto vlastnosti lze použít ke správě metaznaček.</span><span class="sxs-lookup"><span data-stu-id="41a37-109">You can use these properties to manage the meta tags.</span></span>

## <a name="soft-launch-of-a-site"></a><span data-ttu-id="41a37-110">Předběžné spuštění webu</span><span class="sxs-lookup"><span data-stu-id="41a37-110">Soft launch of a site</span></span>

<span data-ttu-id="41a37-111">Během "předběžných spuštění" je webová stránka k dispozici pro omezenou cílovou skupinu nebo trh před tím, než dojde k úplnému spuštění.</span><span class="sxs-lookup"><span data-stu-id="41a37-111">During a "soft launch," a website is made available to a limited audience or market before the full launch occurs.</span></span> <span data-ttu-id="41a37-112">Pokud provedete předběžné spuštění vašeho webu, měli byste zvážit, zda nechcete mít metaznačku **NOINDEX** na místě.</span><span class="sxs-lookup"><span data-stu-id="41a37-112">If you do a soft launch of your website, you should consider leaving the **NOINDEX** meta tags in place.</span></span> <span data-ttu-id="41a37-113">Tímto způsobem vám pomůže zaručit, že měkká spuštění zůstanou omezena na posluchače, kterých chcete dosáhnout.</span><span class="sxs-lookup"><span data-stu-id="41a37-113">In this way, you help guarantee that the soft launch remains restricted to the limited audience that you want to reach.</span></span>

## <a name="a-site-that-is-in-production"></a><span data-ttu-id="41a37-114">Web, který je ve výrobě</span><span class="sxs-lookup"><span data-stu-id="41a37-114">A site that is in production</span></span>

<span data-ttu-id="41a37-115">Pokud je web ve výrobě, ujistěte se, že jsou všechny stránky webu správně označeny.</span><span class="sxs-lookup"><span data-stu-id="41a37-115">When a site is in production, you should make sure that all site pages are correctly tagged.</span></span> <span data-ttu-id="41a37-116">Microsoft Dynamics 365 Commerce používá informace zadané pro stránku k vykreslení všech informací SEO na dané stránce.</span><span class="sxs-lookup"><span data-stu-id="41a37-116">Microsoft Dynamics 365 Commerce uses the information that is entered for a page to render all the SEO information on that page.</span></span> <span data-ttu-id="41a37-117">Následující moduly poskytují tuto funkci: souhrn stránek kategorií, souhrn stránek seznamů a souhrn stránky produktu.</span><span class="sxs-lookup"><span data-stu-id="41a37-117">The following modules provide this functionality: category page summary, list page summary, and product page summary.</span></span>

<span data-ttu-id="41a37-118">Chcete-li optimalizovat indexování vyhledávače, vykreslovací systém používá obě informace z vlastností SEO, které jsou konfigurovány v Dynamics 365 Commerce a v informacích specifických pro modul.</span><span class="sxs-lookup"><span data-stu-id="41a37-118">To optimize search engine indexing, the rendering framework uses both information from the SEO properties that are configured in Dynamics 365 Commerce and module-specific information.</span></span> <span data-ttu-id="41a37-119">U webu, které je ve výrobě, se ujistěte, že soubor robots.txt umožňuje indexovat celý web a obsahuje odkazy na váš publikovaný dokument mapy webu.</span><span class="sxs-lookup"><span data-stu-id="41a37-119">For a site that is in production, you should make sure that the robots.txt file allows for indexing of your whole site, and that it contains links to your published site map document.</span></span> <span data-ttu-id="41a37-120">Měli byste zapnout funkci generování mapy webu na **Nastavení webu \> Mapy webů povoleny**.</span><span class="sxs-lookup"><span data-stu-id="41a37-120">You should turn on the site map generation functionality at **Site Settings \> Site maps enabled**.</span></span>

### <a name="page-seo-settings-for-internal-preview-limited-audiences-and-all-audiences"></a><span data-ttu-id="41a37-121">Nastavení SEO stránky pro interní náhled, omezené cílové skupiny a všechny cílové skupiny</span><span class="sxs-lookup"><span data-stu-id="41a37-121">Page SEO settings for internal preview, limited audiences, and all audiences</span></span>

<span data-ttu-id="41a37-122">Vzhledem k tomu, že aplikace Dynamics 365 Commerce podporuje ověřené náhledy (WYSIWYG) ve vizuálním tvůrci stránek, autoři můžou připravovat obsah stránky, aniž by se museli obávat, že tyto informace budou návštěvníkům webu viditelné.</span><span class="sxs-lookup"><span data-stu-id="41a37-122">Because Dynamics 365 Commerce supports "what you see is what you get" (WYSIWYG) authenticated previews in visual page builder, authors can prepare their page content without having to worry that the information will become visible to site visitors.</span></span> <span data-ttu-id="41a37-123">Pokud musí být stránka publikována, ale je nutné omezit její expozici, měla by mít metaznačku **NOINDEX**, aby nebyla indexována vyhledávacími moduly.</span><span class="sxs-lookup"><span data-stu-id="41a37-123">If a page must be published, but its exposure must be limited, it should have the **NOINDEX** meta tag, so that it won't be indexed by search engines.</span></span> <span data-ttu-id="41a37-124">Poté, co je stránka připravena pro všechny cílové skupiny, by měla být k dispozici všechna základní metadata SEO, aby se maximalizovala efektivita indexování vyhledávacího modulu.</span><span class="sxs-lookup"><span data-stu-id="41a37-124">Then, when the page is ready for all audiences, all the basic SEO metadata should be present, to maximize the efficiency of search engine indexing.</span></span> <span data-ttu-id="41a37-125">Kromě toho by měla být odebrána metaznačka **NOLIMIT**.</span><span class="sxs-lookup"><span data-stu-id="41a37-125">Additionally, the **NOLIMIT** meta tag should be removed.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="41a37-126">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="41a37-126">Additional resources</span></span>

[<span data-ttu-id="41a37-127">Správa uživatelů a rolí elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="41a37-127">Manage e-Commerce users and roles</span></span>](manage-ecommerce-users-roles.md)

[<span data-ttu-id="41a37-128">Přidání kódu skriptu na webové stránky pro podporu telemetrie</span><span class="sxs-lookup"><span data-stu-id="41a37-128">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="41a37-129">Správa zásad zabezpečení obsahu (CSP)</span><span class="sxs-lookup"><span data-stu-id="41a37-129">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)
