---
title: Modul volby lokality
description: Tohle téma se zabývá modulem volby lokality a popisuje, jak jej přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: bd54695f54b501631f916328c05bfd47e538d50d
ms.sourcegitcommit: 765056b5dc1d0a8c27e56ff2cbd310ad3349ff09
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/20/2020
ms.locfileid: "4055823"
---
# <a name="site-selector-module"></a><span data-ttu-id="4fb04-103">Modul volby lokality</span><span class="sxs-lookup"><span data-stu-id="4fb04-103">Site selector module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="4fb04-104">Tohle téma se zabývá modulem volby lokality a popisuje, jak jej přidat na stránky webu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4fb04-104">This topic covers the site selector module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="4fb04-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="4fb04-105">Overview</span></span>

<span data-ttu-id="4fb04-106">Pokud má firma různé weby napříč trhy, regiony a národními prostředími, uživatelé webu potřebují snadný způsob, jak přepínat mezi lokalitami a vybrat si preferovaný nákupní web.</span><span class="sxs-lookup"><span data-stu-id="4fb04-106">When a business has different sites across markets, regions, and locales, site users need an easy way to switch between sites and select their preferred shopping site.</span></span> <span data-ttu-id="4fb04-107">Jako řešení tohoto scénáře umožňuje modul volby lokality uživatelům procházet více webů.</span><span class="sxs-lookup"><span data-stu-id="4fb04-107">To accommodate this scenario, the site selector module lets users browse across multiple sites.</span></span>

<span data-ttu-id="4fb04-108">Modul volby lokality musí být nakonfigurován se seznamem webů (trhy, regiony nebo národní prostředí), které uživatelé webu mohou procházet.</span><span class="sxs-lookup"><span data-stu-id="4fb04-108">The site selector module must be configured with the list of sites (markets, regions, or locales) that site users can browse.</span></span>

> [!NOTE]
> <span data-ttu-id="4fb04-109">Modul volby lokality je k dispozici v Dynamics 365 Commerce verze 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="4fb04-109">The site selector module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="4fb04-110">Následující obrázek ukazuje příklad modulu volby lokality, který se nachází v záhlaví stránky webu.</span><span class="sxs-lookup"><span data-stu-id="4fb04-110">The following illustration shows an example of a site selector module that is featured in the header of a site page.</span></span>

![Příklad modulu volby lokality v záhlaví stránky webu](./media/ecommerce-sitepicker.PNG)

## <a name="site-selector-module-properties"></a><span data-ttu-id="4fb04-112">Vlastnosti modulu volby lokality</span><span class="sxs-lookup"><span data-stu-id="4fb04-112">Site selector module properties</span></span>

| <span data-ttu-id="4fb04-113">Název vlastnosti</span><span class="sxs-lookup"><span data-stu-id="4fb04-113">Property name</span></span> | <span data-ttu-id="4fb04-114">Hodnota</span><span class="sxs-lookup"><span data-stu-id="4fb04-114">Value</span></span>                 | <span data-ttu-id="4fb04-115">popis</span><span class="sxs-lookup"><span data-stu-id="4fb04-115">Description</span></span> |
|---------------|-----------------------|-------------|
| <span data-ttu-id="4fb04-116">Záhlaví</span><span class="sxs-lookup"><span data-stu-id="4fb04-116">Heading</span></span>       | <span data-ttu-id="4fb04-117">Text</span><span class="sxs-lookup"><span data-stu-id="4fb04-117">Text</span></span>                  | <span data-ttu-id="4fb04-118">Nadpis modulu.</span><span class="sxs-lookup"><span data-stu-id="4fb04-118">The heading for the module.</span></span> |
| <span data-ttu-id="4fb04-119">Možnosti webu</span><span class="sxs-lookup"><span data-stu-id="4fb04-119">Site options</span></span>  | <span data-ttu-id="4fb04-120">Název, obrázek, URL</span><span class="sxs-lookup"><span data-stu-id="4fb04-120">Name, Image, URL</span></span>      | <span data-ttu-id="4fb04-121">Tato vlastnost určuje název, odkaz na domovskou stránku webu a volitelný obrázek, který se má zobrazit pro každý web, který je součástí modulu.</span><span class="sxs-lookup"><span data-stu-id="4fb04-121">This property specifies a name, a link to the site's home page, and an optional image to show for each site that is included in the module.</span></span> <span data-ttu-id="4fb04-122">Obrázek může být vlajka nebo nějaké znázornění trhu, regionu nebo národního prostředí.</span><span class="sxs-lookup"><span data-stu-id="4fb04-122">The image can be a flag, or some representation of a market, region, or locale.</span></span> |

## <a name="add-a-site-selector-module-to-a-page"></a><span data-ttu-id="4fb04-123">Přidání modulu volby lokality na stránku</span><span class="sxs-lookup"><span data-stu-id="4fb04-123">Add a site selector module to a page</span></span>

<span data-ttu-id="4fb04-124">Modul volby lokality lze přidat do [modulu záhlaví](author-header-module.md) pod pozicí pro výběr lokality.</span><span class="sxs-lookup"><span data-stu-id="4fb04-124">The site selector module can be added to the [Header module](author-header-module.md) under the site selector slot.</span></span> <span data-ttu-id="4fb04-125">Po přidání můžete definovat možnosti záhlaví a webu modulu.</span><span class="sxs-lookup"><span data-stu-id="4fb04-125">After it's added, you can define the module heading and site options.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4fb04-126">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="4fb04-126">Additional resources</span></span>

[<span data-ttu-id="4fb04-127">Přehled knihovny modulů</span><span class="sxs-lookup"><span data-stu-id="4fb04-127">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="4fb04-128">Modul záhlaví</span><span class="sxs-lookup"><span data-stu-id="4fb04-128">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="4fb04-129">Modul popisu cesty</span><span class="sxs-lookup"><span data-stu-id="4fb04-129">Breadcrumb module</span></span>](add-breadcrumb.md)

[<span data-ttu-id="4fb04-130">Modul navigační nabídky</span><span class="sxs-lookup"><span data-stu-id="4fb04-130">Navigation menu module</span></span>](nav-menu-module.md)
