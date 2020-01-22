---
title: Přidání loga
description: Toto téma popisuje, jak přidat logo na web v řešení Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 12/12/2019
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
ms.openlocfilehash: 23bac9aae6beb59912bbc9e1f2c6958c007550b0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914610"
---
# <a name="add-a-logo"></a><span data-ttu-id="bfe10-103">Přidání loga</span><span class="sxs-lookup"><span data-stu-id="bfe10-103">Add a logo</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="bfe10-104">Toto téma popisuje, jak přidat logo na web v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="bfe10-104">This topic describes how to add a logo to your site in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="bfe10-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="bfe10-105">Overview</span></span>

<span data-ttu-id="bfe10-106">Když vytváříte web, jedna z prvních věcí, kterou pravděpodobně uděláte, je přidání loga vaší společnosti nebo značky do záhlaví webu.</span><span class="sxs-lookup"><span data-stu-id="bfe10-106">When you build your site, one of the first things that you will probably do is add your company or brand logo to the site's header.</span></span> <span data-ttu-id="bfe10-107">Online startovací sada řešení Dynamics 365 Commerce poskytuje modul, který tuto úlohu usnadňuje.</span><span class="sxs-lookup"><span data-stu-id="bfe10-107">The Dynamics 365 Commerce online starter kit provides a module that makes this task easy.</span></span>

<span data-ttu-id="bfe10-108">Logo můžete přidat přímo do šablony, rozložení nebo stránky.</span><span class="sxs-lookup"><span data-stu-id="bfe10-108">You can add a logo directly to a template, layout, or page.</span></span> <span data-ttu-id="bfe10-109">Tímto způsobem můžete snadno změnit logo, které se zobrazí na určitých stránkách nebo skupinách stránek.</span><span class="sxs-lookup"><span data-stu-id="bfe10-109">In this way, you can easily change the logo that appears on specific pages or groups of pages.</span></span> <span data-ttu-id="bfe10-110">Toto téma však popisuje nejčastější scénář, ve kterém přidáte logo do fragmentu záhlaví, který lze znovu použít na všech stránkách webu.</span><span class="sxs-lookup"><span data-stu-id="bfe10-110">However, this topic covers the most frequent scenario, where you add your logo to a header fragment that can be reused across all the pages of your site.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="bfe10-111">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="bfe10-111">Prerequisites</span></span>

<span data-ttu-id="bfe10-112">Před přidáním loga na všechny stránky webu je nutné tyto úkoly dokončit.</span><span class="sxs-lookup"><span data-stu-id="bfe10-112">Before you can add a logo to all the pages of your site, you must complete these tasks.</span></span>

1. <span data-ttu-id="bfe10-113">Uložte logo do správce digitálních datových zdrojů, ke kterému máte přístup ze stránky **Datové zdroje**.</span><span class="sxs-lookup"><span data-stu-id="bfe10-113">Upload your logo to the digital assets manager, which you can access from the **Assets** page.</span></span>
1. <span data-ttu-id="bfe10-114">Vytvořte fragment záhlaví.</span><span class="sxs-lookup"><span data-stu-id="bfe10-114">Create a header fragment.</span></span> <span data-ttu-id="bfe10-115">Další informace o vytváření a používání fragmentů naleznete v tématu [Práce s fragmenty](work-with-fragments.md).</span><span class="sxs-lookup"><span data-stu-id="bfe10-115">For more information about how to create and use fragments, see [Work with fragments](work-with-fragments.md).</span></span>
1. <span data-ttu-id="bfe10-116">Zahrňte do šablony fragment záhlaví, který stránky vašeho webu používají pro své možnosti rozložení a modulu.</span><span class="sxs-lookup"><span data-stu-id="bfe10-116">Include the header fragment in the template that the pages of your site use for their layout and module options.</span></span> <span data-ttu-id="bfe10-117">Další informace o šablonách získáte v části [Práce s šablonami](work-with-templates.md).</span><span class="sxs-lookup"><span data-stu-id="bfe10-117">For more information about templates, see [Work with templates](work-with-templates.md).</span></span>

## <a name="add-a-logo-to-a-header-fragment"></a><span data-ttu-id="bfe10-118">Přidání loga do fragmentu záhlaví</span><span class="sxs-lookup"><span data-stu-id="bfe10-118">Add a logo to a header fragment</span></span>

<span data-ttu-id="bfe10-119">Chcete-li přidat logo do fragmentu záhlaví webu, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="bfe10-119">To add a logo to the header fragment for your site, follow these steps.</span></span>

1. <span data-ttu-id="bfe10-120">V navigačním podokně vlevo vyberte **Fragmenty**a pak vyberte fragment záhlaví, který jste vytvořili.</span><span class="sxs-lookup"><span data-stu-id="bfe10-120">In the navigation pane on the left, select **Fragments**, and then select the header fragment that you created.</span></span>
2. <span data-ttu-id="bfe10-121">Vyberte **Rezervovat**.</span><span class="sxs-lookup"><span data-stu-id="bfe10-121">Select **Check out**.</span></span>
3. <span data-ttu-id="bfe10-122">Rozbalte pozici **Záhlaví** a pozici **Logo**.</span><span class="sxs-lookup"><span data-stu-id="bfe10-122">Expand the **Header** slot and the **Logo** slot.</span></span>
4. <span data-ttu-id="bfe10-123">Vyberte tlačítko se třemi tečkami (**...**) vedle pozice **Logo** a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="bfe10-123">Select the ellipsis button (**...**) for the **Logo** slot, and then select **Add module**.</span></span>
5. <span data-ttu-id="bfe10-124">Vyberte modul logo.</span><span class="sxs-lookup"><span data-stu-id="bfe10-124">Select the logo module.</span></span>
6. <span data-ttu-id="bfe10-125">V podokně vlastností napravo nakonfigurujte modul logo, aby se zobrazilo vaše logo.</span><span class="sxs-lookup"><span data-stu-id="bfe10-125">In the properties pane on the right, configure the logo module so that it shows your logo.</span></span>
7. <span data-ttu-id="bfe10-126">Uložte fragment záhlaví, vraťte jej se změnami a publikujte.</span><span class="sxs-lookup"><span data-stu-id="bfe10-126">Save the header fragment, check it in, and publish it.</span></span>

<span data-ttu-id="bfe10-127">Po publikování aktualizovaného fragmentu záhlaví budou všechny stránky webu, které používají šablonu obsahující fragment záhlaví, zobrazovat vaše logo.</span><span class="sxs-lookup"><span data-stu-id="bfe10-127">After you publish the updated header fragment, all site pages that use the template that contains the header fragment will show your logo.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bfe10-128">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="bfe10-128">Additional resources</span></span>

[<span data-ttu-id="bfe10-129">Volba motivu webu</span><span class="sxs-lookup"><span data-stu-id="bfe10-129">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="bfe10-130">Práce se soubory přepisu šablon CSS</span><span class="sxs-lookup"><span data-stu-id="bfe10-130">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="bfe10-131">Přidání ikony oblíbené položky</span><span class="sxs-lookup"><span data-stu-id="bfe10-131">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="bfe10-132">Přidání uvítací zprávy</span><span class="sxs-lookup"><span data-stu-id="bfe10-132">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="bfe10-133">Přidání oznámení o vlastnických právech</span><span class="sxs-lookup"><span data-stu-id="bfe10-133">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="bfe10-134">Přidání jazyků na web</span><span class="sxs-lookup"><span data-stu-id="bfe10-134">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="bfe10-135">Přidání kódu skriptu na webové stránky pro podporu telemetrie</span><span class="sxs-lookup"><span data-stu-id="bfe10-135">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

