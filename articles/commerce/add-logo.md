---
title: Přidání loga
description: Toto téma popisuje, jak přidat logo na web v řešení Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: d9e1cba6bd07e0c3d9ed7d741d87e10837d8021c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797592"
---
# <a name="add-a-logo"></a><span data-ttu-id="5bf28-103">Přidání loga</span><span class="sxs-lookup"><span data-stu-id="5bf28-103">Add a logo</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5bf28-104">Toto téma popisuje, jak přidat logo na web v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="5bf28-104">This topic describes how to add a logo to your site in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="5bf28-105">Když vytváříte web, jedna z prvních věcí, kterou pravděpodobně uděláte, je přidání loga vaší společnosti nebo značky do záhlaví webu.</span><span class="sxs-lookup"><span data-stu-id="5bf28-105">When you build your site, one of the first things that you will probably do is add your company or brand logo to the site's header.</span></span> <span data-ttu-id="5bf28-106">Online knihovna modulů Dynamics 365 Commerce poskytuje modul, který tuto úlohu usnadňuje.</span><span class="sxs-lookup"><span data-stu-id="5bf28-106">The Dynamics 365 Commerce online module library provides a module that makes this task easy.</span></span>

<span data-ttu-id="5bf28-107">Logo můžete přidat přímo do šablony, rozložení nebo stránky.</span><span class="sxs-lookup"><span data-stu-id="5bf28-107">You can add a logo directly to a template, layout, or page.</span></span> <span data-ttu-id="5bf28-108">Tímto způsobem můžete snadno změnit logo, které se zobrazí na určitých stránkách nebo skupinách stránek.</span><span class="sxs-lookup"><span data-stu-id="5bf28-108">In this way, you can easily change the logo that appears on specific pages or groups of pages.</span></span> <span data-ttu-id="5bf28-109">Toto téma však popisuje nejčastější scénář, ve kterém přidáte logo do fragmentu záhlaví, který lze znovu použít na všech stránkách webu.</span><span class="sxs-lookup"><span data-stu-id="5bf28-109">However, this topic covers the most frequent scenario, where you add your logo to a header fragment that can be reused across all the pages of your site.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5bf28-110">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="5bf28-110">Prerequisites</span></span>

<span data-ttu-id="5bf28-111">Před přidáním loga na všechny stránky webu je nutné tyto úkoly dokončit.</span><span class="sxs-lookup"><span data-stu-id="5bf28-111">Before you can add a logo to all the pages of your site, you must complete these tasks.</span></span>

1. <span data-ttu-id="5bf28-112">Odešlete logo do knihovny médií.</span><span class="sxs-lookup"><span data-stu-id="5bf28-112">Upload your logo to the Media Library.</span></span>
1. <span data-ttu-id="5bf28-113">Vytvořte fragment záhlaví.</span><span class="sxs-lookup"><span data-stu-id="5bf28-113">Create a header fragment.</span></span> <span data-ttu-id="5bf28-114">Další informace o vytváření a používání fragmentů naleznete v tématu [Práce s fragmenty](work-with-fragments.md).</span><span class="sxs-lookup"><span data-stu-id="5bf28-114">For more information about how to create and use fragments, see [Work with fragments](work-with-fragments.md).</span></span>
1. <span data-ttu-id="5bf28-115">Zahrňte do šablony fragment záhlaví, který stránky vašeho webu používají pro své možnosti rozložení a modulu.</span><span class="sxs-lookup"><span data-stu-id="5bf28-115">Include the header fragment in the template that the pages of your site use for their layout and module options.</span></span> <span data-ttu-id="5bf28-116">Další informace o šablonách získáte v části [Práce s šablonami](work-with-templates.md).</span><span class="sxs-lookup"><span data-stu-id="5bf28-116">For more information about templates, see [Work with templates](work-with-templates.md).</span></span>

## <a name="add-a-logo-to-a-header-fragment"></a><span data-ttu-id="5bf28-117">Přidání loga do fragmentu záhlaví</span><span class="sxs-lookup"><span data-stu-id="5bf28-117">Add a logo to a header fragment</span></span>

<span data-ttu-id="5bf28-118">Chcete-li přidat logo do fragmentu záhlaví webu, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="5bf28-118">To add a logo to the header fragment for your site, follow these steps.</span></span>

1. <span data-ttu-id="5bf28-119">V navigačním podokně nalevo vyberte položku **Fragmenty**.</span><span class="sxs-lookup"><span data-stu-id="5bf28-119">In the navigation pane on the left, select **Fragments**.</span></span>
1. <span data-ttu-id="5bf28-120">Vyberte záhlaví, které jste vytvořili dříve, a poté vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="5bf28-120">Select the header fragment that you created, and then select **Edit**.</span></span>
1. <span data-ttu-id="5bf28-121">Rozbalte modul záhlaví.</span><span class="sxs-lookup"><span data-stu-id="5bf28-121">Expand the header module.</span></span>
1. <span data-ttu-id="5bf28-122">V podokně vlastností modulu záhlaví zadejte obrázek a odkaz na logo.</span><span class="sxs-lookup"><span data-stu-id="5bf28-122">In the property pane for the header module, provide an image and link for the logo.</span></span> 
1. <span data-ttu-id="5bf28-123">Uložte fragment záhlaví, dokončete úpravy a publikujte jej.</span><span class="sxs-lookup"><span data-stu-id="5bf28-123">Save the header fragment, finish editing it, and publish it.</span></span>

<span data-ttu-id="5bf28-124">Po publikování aktualizovaného fragmentu záhlaví budou všechny stránky webu, které používají šablonu obsahující fragment záhlaví, zobrazovat vaše logo.</span><span class="sxs-lookup"><span data-stu-id="5bf28-124">After you publish the updated header fragment, all site pages that use the template that contains the header fragment will show your logo.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5bf28-125">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="5bf28-125">Additional resources</span></span>

[<span data-ttu-id="5bf28-126">Volba motivu webu</span><span class="sxs-lookup"><span data-stu-id="5bf28-126">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="5bf28-127">Práce se soubory přepisu šablon CSS</span><span class="sxs-lookup"><span data-stu-id="5bf28-127">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="5bf28-128">Přidání ikony oblíbené položky</span><span class="sxs-lookup"><span data-stu-id="5bf28-128">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="5bf28-129">Přidání uvítací zprávy</span><span class="sxs-lookup"><span data-stu-id="5bf28-129">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="5bf28-130">Přidání oznámení o vlastnických právech</span><span class="sxs-lookup"><span data-stu-id="5bf28-130">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="5bf28-131">Přidání jazyků na web</span><span class="sxs-lookup"><span data-stu-id="5bf28-131">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="5bf28-132">Přidání kódu skriptu na webové stránky pro podporu telemetrie</span><span class="sxs-lookup"><span data-stu-id="5bf28-132">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
