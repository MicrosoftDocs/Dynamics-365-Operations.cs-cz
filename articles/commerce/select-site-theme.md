---
title: Volba motivu webu
description: Toto téma popisuje, jak nastavit nebo změnit motiv webu v aplikaci Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: annbe
ms.date: 10/31/2019
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
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 8ee56f1b135c71194f5e7c4b2a8f47a82294ea81
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/01/2019
ms.locfileid: "2698112"
---
# <a name="select-a-site-theme"></a><span data-ttu-id="f8420-103">Volba motivu webu</span><span class="sxs-lookup"><span data-stu-id="f8420-103">Select a site theme</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="f8420-104">Toto téma popisuje, jak nastavit nebo změnit motiv webu v aplikaci Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="f8420-104">This topic describes how to set or change your site's theme in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f8420-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="f8420-105">Overview</span></span>

<span data-ttu-id="f8420-106">Rozvržení a styl webu (například písma, velikosti a barvy) jsou definovány motivem, který vyberete a použijete na webu.</span><span class="sxs-lookup"><span data-stu-id="f8420-106">A site's layout and style (for example, fonts, sizes, and colors) are defined by the theme that you select and apply to the site.</span></span> <span data-ttu-id="f8420-107">Motiv je vytvořen a nasazen vývojářem ve vaší společnosti.</span><span class="sxs-lookup"><span data-stu-id="f8420-107">A theme is created and deployed by a developer at your company.</span></span> <span data-ttu-id="f8420-108">Přehled motivů naleznete v tématu [Přehled motivů](http://).</span><span class="sxs-lookup"><span data-stu-id="f8420-108">For an overview of themes, see [Theming overview](http://).</span></span> <span data-ttu-id="f8420-109">Další informace o tom, jak vytvářet a nasazovat motivy, naleznete v tématu [Vytvoření nového motivu](http://).</span><span class="sxs-lookup"><span data-stu-id="f8420-109">For more information about how to create and deploy themes, see [Create a new theme](http://).</span></span>

<span data-ttu-id="f8420-110">Ve výchozím nastavení je při prvním vytvoření webu použit motiv s názvem **Fabrikam**.</span><span class="sxs-lookup"><span data-stu-id="f8420-110">By default, when you first create a site, it uses a theme that is named **Fabrikam**.</span></span> <span data-ttu-id="f8420-111">Tento výchozí motiv je poskytován jako součást startovní sady.</span><span class="sxs-lookup"><span data-stu-id="f8420-111">This default theme is provided as part of the starter kit.</span></span> <span data-ttu-id="f8420-112">Po nasazení dalších motivů webu můžete nakonfigurovat web tak, aby používal jeden z nich.</span><span class="sxs-lookup"><span data-stu-id="f8420-112">After you've deployed additional themes for your site, you can configure the site so that it uses one of them instead.</span></span>

## <a name="select-the-site-theme"></a><span data-ttu-id="f8420-113">Volba motivu webu</span><span class="sxs-lookup"><span data-stu-id="f8420-113">Select the site theme</span></span>

<span data-ttu-id="f8420-114">Chcete-li vybrat motiv, který je pro web použit, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="f8420-114">To select the theme that is applied to your site, follow these steps.</span></span>

1. <span data-ttu-id="f8420-115">Ve vývojovém prostředí webu přejděte na web.</span><span class="sxs-lookup"><span data-stu-id="f8420-115">In the site authoring environment, go to your site.</span></span>
1. <span data-ttu-id="f8420-116">Přejděte na **Správa webu** \> **Rozšiřitelnost**.</span><span class="sxs-lookup"><span data-stu-id="f8420-116">Go to **Site Management** \> **Extensibility**.</span></span>
1. <span data-ttu-id="f8420-117">V části **Motiv** vyberte v rozevírací nabídce motiv.</span><span class="sxs-lookup"><span data-stu-id="f8420-117">Under **Theme**, select a theme on the drop-down menu.</span></span>
1. <span data-ttu-id="f8420-118">Chcete-li vybraný motiv použít na váš web, vyberte možnost **Uložit a publikovat**.</span><span class="sxs-lookup"><span data-stu-id="f8420-118">To apply the selected theme to your site, select **Save and publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="f8420-119">Vybraný motiv se publikuje na vašem webu, jakmile vyberete **Uložit a publikovat** na stránce **Rozšiřitelnost**.</span><span class="sxs-lookup"><span data-stu-id="f8420-119">The theme that you select is published to your site as soon as you select **Save and publish** on the **Extensibility** page.</span></span> <span data-ttu-id="f8420-120">Chcete-li si prohlédnout motiv na vašem webu před jeho použitím, můžete použít vývojové prostředí nebo prostředí sandbox.</span><span class="sxs-lookup"><span data-stu-id="f8420-120">To preview a theme on your site before you apply it, you can use your development or sandbox environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f8420-121">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="f8420-121">Additional resources</span></span>

[<span data-ttu-id="f8420-122">Přidání loga</span><span class="sxs-lookup"><span data-stu-id="f8420-122">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="f8420-123">Přidání ikony oblíbené položky</span><span class="sxs-lookup"><span data-stu-id="f8420-123">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="f8420-124">Přidání uvítací zprávy</span><span class="sxs-lookup"><span data-stu-id="f8420-124">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="f8420-125">Přidání oznámení o vlastnických právech</span><span class="sxs-lookup"><span data-stu-id="f8420-125">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="f8420-126">Přidání jazyků na web</span><span class="sxs-lookup"><span data-stu-id="f8420-126">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="f8420-127">Přidání kódu skriptu na webové stránky pro podporu telemetrie</span><span class="sxs-lookup"><span data-stu-id="f8420-127">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)
