---
title: Přidání loga
description: Toto téma popisuje, jak přidat logo na web v řešení Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f15680deb0eab763ba68f2897139c915d1f8a6a3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410731"
---
# <a name="add-a-logo"></a><span data-ttu-id="0317a-103">Přidání loga</span><span class="sxs-lookup"><span data-stu-id="0317a-103">Add a logo</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0317a-104">Toto téma popisuje, jak přidat logo na web v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0317a-104">This topic describes how to add a logo to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0317a-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="0317a-105">Overview</span></span>

<span data-ttu-id="0317a-106">Když vytváříte web, jedna z prvních věcí, kterou pravděpodobně uděláte, je přidání loga vaší společnosti nebo značky do záhlaví webu.</span><span class="sxs-lookup"><span data-stu-id="0317a-106">When you build your site, one of the first things that you will probably do is add your company or brand logo to the site's header.</span></span> <span data-ttu-id="0317a-107">Online knihovna modulů Dynamics 365 Commerce poskytuje modul, který tuto úlohu usnadňuje.</span><span class="sxs-lookup"><span data-stu-id="0317a-107">The Dynamics 365 Commerce online module library provides a module that makes this task easy.</span></span>

<span data-ttu-id="0317a-108">Logo můžete přidat přímo do šablony, rozložení nebo stránky.</span><span class="sxs-lookup"><span data-stu-id="0317a-108">You can add a logo directly to a template, layout, or page.</span></span> <span data-ttu-id="0317a-109">Tímto způsobem můžete snadno změnit logo, které se zobrazí na určitých stránkách nebo skupinách stránek.</span><span class="sxs-lookup"><span data-stu-id="0317a-109">In this way, you can easily change the logo that appears on specific pages or groups of pages.</span></span> <span data-ttu-id="0317a-110">Toto téma však popisuje nejčastější scénář, ve kterém přidáte logo do fragmentu záhlaví, který lze znovu použít na všech stránkách webu.</span><span class="sxs-lookup"><span data-stu-id="0317a-110">However, this topic covers the most frequent scenario, where you add your logo to a header fragment that can be reused across all the pages of your site.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="0317a-111">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="0317a-111">Prerequisites</span></span>

<span data-ttu-id="0317a-112">Před přidáním loga na všechny stránky webu je nutné tyto úkoly dokončit.</span><span class="sxs-lookup"><span data-stu-id="0317a-112">Before you can add a logo to all the pages of your site, you must complete these tasks.</span></span>

1. <span data-ttu-id="0317a-113">Odešlete logo do knihovny médií.</span><span class="sxs-lookup"><span data-stu-id="0317a-113">Upload your logo to the Media Library.</span></span>
1. <span data-ttu-id="0317a-114">Vytvořte fragment záhlaví.</span><span class="sxs-lookup"><span data-stu-id="0317a-114">Create a header fragment.</span></span> <span data-ttu-id="0317a-115">Další informace o vytváření a používání fragmentů naleznete v tématu [Práce s fragmenty](work-with-fragments.md).</span><span class="sxs-lookup"><span data-stu-id="0317a-115">For more information about how to create and use fragments, see [Work with fragments](work-with-fragments.md).</span></span>
1. <span data-ttu-id="0317a-116">Zahrňte do šablony fragment záhlaví, který stránky vašeho webu používají pro své možnosti rozložení a modulu.</span><span class="sxs-lookup"><span data-stu-id="0317a-116">Include the header fragment in the template that the pages of your site use for their layout and module options.</span></span> <span data-ttu-id="0317a-117">Další informace o šablonách získáte v části [Práce s šablonami](work-with-templates.md).</span><span class="sxs-lookup"><span data-stu-id="0317a-117">For more information about templates, see [Work with templates](work-with-templates.md).</span></span>

## <a name="add-a-logo-to-a-header-fragment"></a><span data-ttu-id="0317a-118">Přidání loga do fragmentu záhlaví</span><span class="sxs-lookup"><span data-stu-id="0317a-118">Add a logo to a header fragment</span></span>

<span data-ttu-id="0317a-119">Chcete-li přidat logo do fragmentu záhlaví webu, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="0317a-119">To add a logo to the header fragment for your site, follow these steps.</span></span>

1. <span data-ttu-id="0317a-120">V navigačním podokně nalevo vyberte položku **Fragmenty**.</span><span class="sxs-lookup"><span data-stu-id="0317a-120">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="0317a-121">Vyberte záhlaví, které jste vytvořili dříve, a poté vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="0317a-121">Select the header fragment that you created, and then select **Edit**.</span></span>
1. <span data-ttu-id="0317a-122">Rozbalte modul záhlaví.</span><span class="sxs-lookup"><span data-stu-id="0317a-122">Expand the header module.</span></span>
1. <span data-ttu-id="0317a-123">V podokně vlastností modulu záhlaví zadejte obrázek a odkaz na logo.</span><span class="sxs-lookup"><span data-stu-id="0317a-123">In the property pane for the header module, provide an image and link for the logo.</span></span> 
1. <span data-ttu-id="0317a-124">Uložte fragment záhlaví, dokončete úpravy a publikujte jej.</span><span class="sxs-lookup"><span data-stu-id="0317a-124">Save the header fragment, finish editing it, and publish it.</span></span>

<span data-ttu-id="0317a-125">Po publikování aktualizovaného fragmentu záhlaví budou všechny stránky webu, které používají šablonu obsahující fragment záhlaví, zobrazovat vaše logo.</span><span class="sxs-lookup"><span data-stu-id="0317a-125">After you publish the updated header fragment, all site pages that use the template that contains the header fragment will show your logo.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0317a-126">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="0317a-126">Additional resources</span></span>

[<span data-ttu-id="0317a-127">Volba motivu webu</span><span class="sxs-lookup"><span data-stu-id="0317a-127">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="0317a-128">Práce se soubory přepisu šablon CSS</span><span class="sxs-lookup"><span data-stu-id="0317a-128">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="0317a-129">Přidání ikony oblíbené položky</span><span class="sxs-lookup"><span data-stu-id="0317a-129">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="0317a-130">Přidání uvítací zprávy</span><span class="sxs-lookup"><span data-stu-id="0317a-130">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="0317a-131">Přidání oznámení o vlastnických právech</span><span class="sxs-lookup"><span data-stu-id="0317a-131">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="0317a-132">Přidání jazyků na web</span><span class="sxs-lookup"><span data-stu-id="0317a-132">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="0317a-133">Přidání kódu skriptu na webové stránky pro podporu telemetrie</span><span class="sxs-lookup"><span data-stu-id="0317a-133">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

