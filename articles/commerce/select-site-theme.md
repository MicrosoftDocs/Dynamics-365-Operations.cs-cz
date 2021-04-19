---
title: Volba motivu webu
description: Toto téma popisuje, jak nastavit nebo změnit motiv webu v aplikaci Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1e11e2ffafa29dfe4ad7a4a8e4d14e9d7c74c31f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794060"
---
# <a name="select-a-site-theme"></a><span data-ttu-id="4923c-103">Volba motivu webu</span><span class="sxs-lookup"><span data-stu-id="4923c-103">Select a site theme</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4923c-104">Toto téma popisuje, jak nastavit nebo změnit motiv webu v aplikaci Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4923c-104">This topic describes how to set or change your site's theme in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="4923c-105">Rozvržení a styl webu (například písma, velikosti a barvy) jsou definovány motivem, který vyberete a použijete na webu.</span><span class="sxs-lookup"><span data-stu-id="4923c-105">A site's layout and style (for example, fonts, sizes, and colors) are defined by the theme that you select and apply to the site.</span></span> <span data-ttu-id="4923c-106">Motiv je vytvořen a nasazen vývojářem ve vaší společnosti.</span><span class="sxs-lookup"><span data-stu-id="4923c-106">A theme is created and deployed by a developer at your company.</span></span> <span data-ttu-id="4923c-107">Přehled motivů naleznete v tématu [Přehled motivů](e-commerce-extensibility/theming.md).</span><span class="sxs-lookup"><span data-stu-id="4923c-107">For an overview of themes, see [Theming overview](e-commerce-extensibility/theming.md).</span></span> <span data-ttu-id="4923c-108">Další informace o tom, jak vytvářet a nasazovat motivy, naleznete v tématu [Vytvoření nového motivu](e-commerce-extensibility/create-theme.md).</span><span class="sxs-lookup"><span data-stu-id="4923c-108">For more information about how to create and deploy themes, see [Create a new theme](e-commerce-extensibility/create-theme.md).</span></span>

<span data-ttu-id="4923c-109">Ve výchozím nastavení je při prvním vytvoření webu použit motiv s názvem **Fabrikam**.</span><span class="sxs-lookup"><span data-stu-id="4923c-109">By default, when you first create a site, it uses a theme that is named **Fabrikam**.</span></span> <span data-ttu-id="4923c-110">Tento výchozí motiv je poskytován jako součást knihovny modulů Commerce.</span><span class="sxs-lookup"><span data-stu-id="4923c-110">This default theme is provided as part of the Commerce module library.</span></span> <span data-ttu-id="4923c-111">Po nasazení dalších motivů webu můžete nakonfigurovat web tak, aby používal jeden z nich.</span><span class="sxs-lookup"><span data-stu-id="4923c-111">After you've deployed additional themes for your site, you can configure the site so that it uses one of them instead.</span></span>

## <a name="select-the-site-theme"></a><span data-ttu-id="4923c-112">Volba motivu webu</span><span class="sxs-lookup"><span data-stu-id="4923c-112">Select the site theme</span></span>

<span data-ttu-id="4923c-113">Chcete-li vybrat motiv, který je pro web použit, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="4923c-113">To select the theme that is applied to your site, follow these steps.</span></span>

1. <span data-ttu-id="4923c-114">Ve vývojovém prostředí webu přejděte na web.</span><span class="sxs-lookup"><span data-stu-id="4923c-114">In the site authoring environment, go to your site.</span></span>
1. <span data-ttu-id="4923c-115">Přejděte na **Správa webu** \> **Rozšiřitelnost**.</span><span class="sxs-lookup"><span data-stu-id="4923c-115">Go to **Site Management** \> **Extensibility**.</span></span>
1. <span data-ttu-id="4923c-116">V části **Motiv** vyberte v rozevírací nabídce motiv.</span><span class="sxs-lookup"><span data-stu-id="4923c-116">Under **Theme**, select a theme on the drop-down menu.</span></span>
1. <span data-ttu-id="4923c-117">Chcete-li vybraný motiv použít na váš web, vyberte možnost **Uložit a publikovat**.</span><span class="sxs-lookup"><span data-stu-id="4923c-117">To apply the selected theme to your site, select **Save and publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="4923c-118">Vybraný motiv se publikuje na vašem webu, jakmile vyberete **Uložit a publikovat** na stránce **Rozšiřitelnost**.</span><span class="sxs-lookup"><span data-stu-id="4923c-118">The theme that you select is published to your site as soon as you select **Save and publish** on the **Extensibility** page.</span></span> <span data-ttu-id="4923c-119">Chcete-li si prohlédnout motiv na vašem webu před jeho použitím, můžete použít vývojové prostředí nebo prostředí sandbox.</span><span class="sxs-lookup"><span data-stu-id="4923c-119">To preview a theme on your site before you apply it, you can use your development or sandbox environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4923c-120">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="4923c-120">Additional resources</span></span>

[<span data-ttu-id="4923c-121">Přidání loga</span><span class="sxs-lookup"><span data-stu-id="4923c-121">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="4923c-122">Práce se soubory přepisu šablon CSS</span><span class="sxs-lookup"><span data-stu-id="4923c-122">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="4923c-123">Přidání ikony oblíbené položky</span><span class="sxs-lookup"><span data-stu-id="4923c-123">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="4923c-124">Přidání uvítací zprávy</span><span class="sxs-lookup"><span data-stu-id="4923c-124">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="4923c-125">Přidání oznámení o vlastnických právech</span><span class="sxs-lookup"><span data-stu-id="4923c-125">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="4923c-126">Přidání jazyků na web</span><span class="sxs-lookup"><span data-stu-id="4923c-126">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="4923c-127">Přidání kódu skriptu na webové stránky pro podporu telemetrie</span><span class="sxs-lookup"><span data-stu-id="4923c-127">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="4923c-128">Přehled motivů</span><span class="sxs-lookup"><span data-stu-id="4923c-128">Theming overview</span></span>](e-commerce-extensibility/theming.md)

[<span data-ttu-id="4923c-129">Vytvoření nového tématu</span><span class="sxs-lookup"><span data-stu-id="4923c-129">Create a new theme</span></span>](e-commerce-extensibility/create-theme.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
