---
title: Přidání uvítací zprávy
description: V tomto tématu je popsán postup při přidání uvítací zprávy na webovou stránku Microsoft Dynamics 365 Commerce.
author: psimolin
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
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 25a4e91646916b03c8a138fc713577f429ab633c
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697352"
---
# <a name="add-a-welcome-message"></a><span data-ttu-id="1f785-103">Přidání uvítací zprávy</span><span class="sxs-lookup"><span data-stu-id="1f785-103">Add a welcome message</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="1f785-104">V tomto tématu je popsán postup při přidání uvítací zprávy na webovou stránku Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1f785-104">This topic describes how to add a welcome message to your Microsoft Dynamics 365 Commerce website.</span></span>

## <a name="overview"></a><span data-ttu-id="1f785-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="1f785-105">Overview</span></span>

<span data-ttu-id="1f785-106">Uvítací zpráva na webu elektronického obchodu může informovat návštěvníky o probíhajícím prodeji, aktualizacích webu nebo dostupnosti sezónních kolekcí.</span><span class="sxs-lookup"><span data-stu-id="1f785-106">A welcome message on your e-Commerce website can inform visitors about ongoing sales, site updates, or availability of seasonal collections.</span></span> <span data-ttu-id="1f785-107">Uvítací zpráva je nastavena pomocí modulu výstrahy.</span><span class="sxs-lookup"><span data-stu-id="1f785-107">The welcome message is set by using the alert module.</span></span>

<span data-ttu-id="1f785-108">Modul výstrahy by měl být přidán do pozice **Chybové/informační zprávy** ve fragmentu záhlaví.</span><span class="sxs-lookup"><span data-stu-id="1f785-108">The alert module should be added to the **Error/Information messages** slot of the header fragment.</span></span> <span data-ttu-id="1f785-109">Modul výstrahy umožňuje zadat zobrazovaný text, jeho barvu a zarovnání.</span><span class="sxs-lookup"><span data-stu-id="1f785-109">The alert module lets you specify the text that is shown, the text color, and the alignment.</span></span> <span data-ttu-id="1f785-110">Umožňuje také určit, zda návštěvníci webu mohou zprávu zamítnout.</span><span class="sxs-lookup"><span data-stu-id="1f785-110">It also lets you specify whether visitors to the site can dismiss the message.</span></span>

<span data-ttu-id="1f785-111">Uvítací zpráva, která je přidána do sdíleného fragmentu záhlaví, se zobrazí na všech stránkách, které používají šablonu, v níž je použit sdílený fragment záhlaví.</span><span class="sxs-lookup"><span data-stu-id="1f785-111">When a welcome message is added to a shared header fragment, it will be shown on every page that uses the template where that shared header fragment is used.</span></span>

<span data-ttu-id="1f785-112">Chcete-li na svůj web přidat uvítací zprávu, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="1f785-112">To add a welcome message to your site, follow these steps.</span></span>

1. <span data-ttu-id="1f785-113">V Dynamics 365 Commerce přejděte na web.</span><span class="sxs-lookup"><span data-stu-id="1f785-113">In Dynamics 365 Commerce, go to your site.</span></span>
1. <span data-ttu-id="1f785-114">Vyberte **Fragmenty**.</span><span class="sxs-lookup"><span data-stu-id="1f785-114">Select **Fragments**.</span></span>
1. <span data-ttu-id="1f785-115">Vyberte fragment záhlaví, do kterého chcete přidat zprávu.</span><span class="sxs-lookup"><span data-stu-id="1f785-115">Select the header fragment to add the message to.</span></span>
1. <span data-ttu-id="1f785-116">Ve stromové struktuře rozbalte **Chybové/informační zprávy**.</span><span class="sxs-lookup"><span data-stu-id="1f785-116">In the outline tree, expand **Error/Information messages**.</span></span>
1. <span data-ttu-id="1f785-117">Vyberte modul výstrahy.</span><span class="sxs-lookup"><span data-stu-id="1f785-117">Select the alert module.</span></span>

    <span data-ttu-id="1f785-118">Pokud modul výstrahy ještě neexistuje, vyberte tlačítko se třemi tečkami (**...**) vedle položky **Chybové/informační zprávy** a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="1f785-118">If an alert module doesn't yet exist, select the ellipsis button (**...**) next to **Error/Information messages**, and then select **Add module**.</span></span> <span data-ttu-id="1f785-119">Vyberte modul výstrahy a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="1f785-119">Select the alert module, and then select **OK**.</span></span>

1. <span data-ttu-id="1f785-120">V podokně vlastností vpravo na kartě **Data** vyberte možnost **Přidat zdroj dat** a pak vyberte možnost **Obsah**</span><span class="sxs-lookup"><span data-stu-id="1f785-120">In the property pane on the right, on the **Data** tab, select **Add Data Source**, and then select **Content**.</span></span>
1. <span data-ttu-id="1f785-121">Do pole **Vstupní text** zadejte text uvítací zprávy.</span><span class="sxs-lookup"><span data-stu-id="1f785-121">In the **Input Text** field, enter the text of the welcome message.</span></span>
1. <span data-ttu-id="1f785-122">Uložte fragment záhlaví, vraťte jej se změnami a publikujte.</span><span class="sxs-lookup"><span data-stu-id="1f785-122">Save the header fragment, check it in, and publish it.</span></span>

<span data-ttu-id="1f785-123">Uvítací zpráva se nyní zobrazuje v horní části každé stránky webu, která používá vybraný fragment záhlaví.</span><span class="sxs-lookup"><span data-stu-id="1f785-123">The welcome message will now appear at the top of every site page that uses the selected header fragment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1f785-124">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="1f785-124">Additional resources</span></span>

[<span data-ttu-id="1f785-125">Přidání loga</span><span class="sxs-lookup"><span data-stu-id="1f785-125">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="1f785-126">Volba motivu webu</span><span class="sxs-lookup"><span data-stu-id="1f785-126">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="1f785-127">Přidání ikony oblíbené položky</span><span class="sxs-lookup"><span data-stu-id="1f785-127">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="1f785-128">Přidání oznámení o vlastnických právech</span><span class="sxs-lookup"><span data-stu-id="1f785-128">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="1f785-129">Přidání jazyků na web</span><span class="sxs-lookup"><span data-stu-id="1f785-129">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="1f785-130">Přidání kódu skriptu na webové stránky pro podporu telemetrie</span><span class="sxs-lookup"><span data-stu-id="1f785-130">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

