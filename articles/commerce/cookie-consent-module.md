---
title: Modul souhlasu se soubory cookie
description: Tohle téma se zabývá moduly souhlasu se soubory cookie a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 504232285267fb3663093a84a371e0040233ce23
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993518"
---
# <a name="cookie-consent-module"></a><span data-ttu-id="42dd2-103">Modul souhlasu se soubory cookie</span><span class="sxs-lookup"><span data-stu-id="42dd2-103">Cookie consent module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="42dd2-104">Tohle téma se zabývá moduly souhlasu se soubory cookie a popisuje, jak je přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="42dd2-104">This topic covers cookie consent modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="42dd2-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="42dd2-105">Overview</span></span>

<span data-ttu-id="42dd2-106">Modul souhlasu se soubory cookie vyzve uživatele webu, aby výslovně poskytli souhlas s povolením souborů cookie pro veškeré funkce nebo moduly, které sledují soubory cookie prohlížeče.</span><span class="sxs-lookup"><span data-stu-id="42dd2-106">The cookie consent module prompts site users to explicitly provide consent to allow cookies for any feature or module that tracks browser cookies.</span></span> <span data-ttu-id="42dd2-107">Souhlas je vyžadován při prvním procházení webu uživatelem v nové relaci prohlížeče.</span><span class="sxs-lookup"><span data-stu-id="42dd2-107">The consent is required the first time a site user browses a site in a new browser session.</span></span> <span data-ttu-id="42dd2-108">Po obdržení souhlasu je soubor cookie sledován a uživatel webu již není žádán o souhlas.</span><span class="sxs-lookup"><span data-stu-id="42dd2-108">When consent is received, it is tracked and the site user will not be prompted for consent again.</span></span> <span data-ttu-id="42dd2-109">Další informace viz [Zásady zacházení se soubory cookie](cookie-compliance.md).</span><span class="sxs-lookup"><span data-stu-id="42dd2-109">For more information, see [Cookie compliance](cookie-compliance.md).</span></span>

<span data-ttu-id="42dd2-110">Pokud není obdržen souhlas uživatele se soubory cookie na webu, nebudou se na stránce vykreslovat žádné funkce nebo moduly, které vyžadují souhlas se soubory cookie.</span><span class="sxs-lookup"><span data-stu-id="42dd2-110">If site user cookie consent is not received, any features or modules that require cookie consent will not be rendered on the page.</span></span> <span data-ttu-id="42dd2-111">Například modul pokladny, modul sdílení na sociálních sítích a preferovaná funkce obchodu vyžadují souhlas se soubory cookie a nebudou zobrazeny, pokud nebude přijat souhlas uživatele webu.</span><span class="sxs-lookup"><span data-stu-id="42dd2-111">For example, the checkout module, social share module, and preferred store feature all require cookie consent and will not be rendered if site user consent is not received.</span></span> 

<span data-ttu-id="42dd2-112">Modul souhlasu se soubory cookie lze nakonfigurovat ve fragmentu záhlaví stránky, takže jej lze vynutit při načtení stránky.</span><span class="sxs-lookup"><span data-stu-id="42dd2-112">A cookie consent module can be configured on a page's header fragment so that it can be enforced when the page loads.</span></span> <span data-ttu-id="42dd2-113">Modul souhlasu se soubory cookie by měl obsahovat jasnou zprávu informující uživatele webu o používání souborů cookie na webu a měl by poskytovat odkaz na stránku ochrany osobních údajů webu.</span><span class="sxs-lookup"><span data-stu-id="42dd2-113">The cookie consent module should have a clear message informing the site user about cookie usage on the site and should provide a link to the site's privacy page.</span></span>

<span data-ttu-id="42dd2-114">Následující obrázek znázorňuje příklad zprávy o souhlasu se soubory cookie s odkazem na stránku zásad ochrany osobních údajů webu zobrazeným v záhlaví stránky webu.</span><span class="sxs-lookup"><span data-stu-id="42dd2-114">The following illustration highlights an example of a cookie consent message with a link to the site's privacy policy page displayed on the header of a site page.</span></span>
<span data-ttu-id="42dd2-115">![Příklad modulu souhlasu se soubory cookie](./media/ecommerce-cookieconsent.png)</span><span class="sxs-lookup"><span data-stu-id="42dd2-115">![Example of a cookie consent module](./media/ecommerce-cookieconsent.png)</span></span>

## <a name="cookie-consent-module-properties"></a><span data-ttu-id="42dd2-116">Vlastnosti modulu souhlasu se soubory cookie</span><span class="sxs-lookup"><span data-stu-id="42dd2-116">Cookie consent module properties</span></span>

| <span data-ttu-id="42dd2-117">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="42dd2-117">Property name</span></span>             | <span data-ttu-id="42dd2-118">Hodnota</span><span class="sxs-lookup"><span data-stu-id="42dd2-118">Value</span></span>                 | <span data-ttu-id="42dd2-119">popis</span><span class="sxs-lookup"><span data-stu-id="42dd2-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="42dd2-120">Formátovaný text</span><span class="sxs-lookup"><span data-stu-id="42dd2-120">Rich Text</span></span>                  | <span data-ttu-id="42dd2-121">Formátovaný text</span><span class="sxs-lookup"><span data-stu-id="42dd2-121">Rich Text</span></span> | <span data-ttu-id="42dd2-122">Zde lze zadat oznámení ve formátu RTF zobrazené uživatelům webu, že web používá soubory cookie prohlížeče a že uživatelé by měli přijmout použití souborů cookie, aby byl web plně funkční.</span><span class="sxs-lookup"><span data-stu-id="42dd2-122">Specifies a Rich Text notification to site users that the site uses browser cookies and that users should accept the use of cookies for the site to be fully functional.</span></span> |
| <span data-ttu-id="42dd2-123">Odkazy</span><span class="sxs-lookup"><span data-stu-id="42dd2-123">Links</span></span> | <span data-ttu-id="42dd2-124">Adresa URL</span><span class="sxs-lookup"><span data-stu-id="42dd2-124">URL</span></span> | <span data-ttu-id="42dd2-125">Na stránku ochrany osobních údajů webu, která popisuje typy souborů cookie, které jsou na webu sledovány, lze přidat jeden nebo více odkazů.</span><span class="sxs-lookup"><span data-stu-id="42dd2-125">One or more links can be added to a site's privacy page that describes the types of cookies that are tracked on the site.</span></span> |

## <a name="add-a-cookie-consent-module-to-site-pages"></a><span data-ttu-id="42dd2-126">Přidání modul souhlasu se soubory cookie na stránky webu</span><span class="sxs-lookup"><span data-stu-id="42dd2-126">Add a cookie consent module to site pages</span></span>

<span data-ttu-id="42dd2-127">Aby bylo možné efektivně přidat modul souhlasu se soubory cookie na více stránek webu, lze jej přidat do sdíleného fragmentu záhlaví stránky.</span><span class="sxs-lookup"><span data-stu-id="42dd2-127">To efficiently add a cookie consent module to multiple site pages, it can be added to a shared page header fragment.</span></span> <span data-ttu-id="42dd2-128">Po přidání fragmentu záhlaví na všechny stránky webu se oznámení o souhlasu se soubory cookie automaticky vykreslí při první návštěvě libovolné stránky webu.</span><span class="sxs-lookup"><span data-stu-id="42dd2-128">After the header fragment is added to all site pages, a cookie consent notification will automatically be rendered the first time a site user navigates to any site page.</span></span>

<span data-ttu-id="42dd2-129">Další informace o fragmentech záhlaví a modulech viz [Modul záhlaví](author-header-module.md).</span><span class="sxs-lookup"><span data-stu-id="42dd2-129">For more information about header fragments and modules, see [Header module](author-header-module.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="42dd2-130">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="42dd2-130">Additional resources</span></span>

[<span data-ttu-id="42dd2-131">Přehled knihovny modulů</span><span class="sxs-lookup"><span data-stu-id="42dd2-131">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="42dd2-132">Modul záhlaví</span><span class="sxs-lookup"><span data-stu-id="42dd2-132">Header module</span></span>](author-header-module.md) 

[<span data-ttu-id="42dd2-133">Zásady zacházení se soubory cookie</span><span class="sxs-lookup"><span data-stu-id="42dd2-133">Cookie compliance</span></span>](cookie-compliance.md)
