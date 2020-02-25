---
title: Přidání uvítací zprávy
description: V tomto tématu je popsán postup při přidání uvítací zprávy na webovou stránku Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 12/12/2019
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
ms.openlocfilehash: ca10b01268b5dcd4c6fe448d90cd0ebd65a2673b
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001247"
---
# <a name="add-a-welcome-message"></a><span data-ttu-id="3a734-103">Přidání uvítací zprávy</span><span class="sxs-lookup"><span data-stu-id="3a734-103">Add a welcome message</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="3a734-104">V tomto tématu je popsán postup při přidání uvítací zprávy na webovou stránku Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3a734-104">This topic describes how to add a welcome message to your Microsoft Dynamics 365 Commerce website.</span></span>

## <a name="overview"></a><span data-ttu-id="3a734-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="3a734-105">Overview</span></span>

<span data-ttu-id="3a734-106">Uvítací zpráva na webu elektronického obchodu může informovat návštěvníky o probíhajícím prodeji, aktualizacích webu nebo dostupnosti sezónních kolekcí.</span><span class="sxs-lookup"><span data-stu-id="3a734-106">A welcome message on your e-Commerce website can inform visitors about ongoing sales, site updates, or availability of seasonal collections.</span></span> <span data-ttu-id="3a734-107">Uvítací zpráva je nastavena pomocí modulu výstrahy.</span><span class="sxs-lookup"><span data-stu-id="3a734-107">The welcome message is set by using the alert module.</span></span>

<span data-ttu-id="3a734-108">Modul výstrahy by měl být přidán do pozice **Chybové/informační zprávy** ve fragmentu záhlaví.</span><span class="sxs-lookup"><span data-stu-id="3a734-108">The alert module should be added to the **Error/Information messages** slot of the header fragment.</span></span> <span data-ttu-id="3a734-109">Modul výstrahy umožňuje zadat zobrazovaný text, jeho barvu a zarovnání.</span><span class="sxs-lookup"><span data-stu-id="3a734-109">The alert module lets you specify the text that is shown, the text color, and the alignment.</span></span> <span data-ttu-id="3a734-110">Umožňuje také určit, zda návštěvníci webu mohou zprávu zamítnout.</span><span class="sxs-lookup"><span data-stu-id="3a734-110">It also lets you specify whether visitors to the site can dismiss the message.</span></span>

<span data-ttu-id="3a734-111">Uvítací zpráva, která je přidána do sdíleného fragmentu záhlaví, se zobrazí na všech stránkách, které používají šablonu, v níž je použit sdílený fragment záhlaví.</span><span class="sxs-lookup"><span data-stu-id="3a734-111">When a welcome message is added to a shared header fragment, it will be shown on every page that uses the template where that shared header fragment is used.</span></span>

<span data-ttu-id="3a734-112">Chcete-li na svůj web přidat uvítací zprávu, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="3a734-112">To add a welcome message to your site, follow these steps.</span></span>

1. <span data-ttu-id="3a734-113">V Dynamics 365 Commerce přejděte na web.</span><span class="sxs-lookup"><span data-stu-id="3a734-113">In Dynamics 365 Commerce, go to your site.</span></span>
1. <span data-ttu-id="3a734-114">Vyberte **Fragmenty**.</span><span class="sxs-lookup"><span data-stu-id="3a734-114">Select **Fragments**.</span></span>
1. <span data-ttu-id="3a734-115">Vyberte fragment záhlaví, do kterého chcete přidat zprávu.</span><span class="sxs-lookup"><span data-stu-id="3a734-115">Select the header fragment to add the message to.</span></span>
1. <span data-ttu-id="3a734-116">Ve stromové struktuře rozbalte **Chybové/informační zprávy**.</span><span class="sxs-lookup"><span data-stu-id="3a734-116">In the outline tree, expand **Error/Information messages**.</span></span>
1. <span data-ttu-id="3a734-117">Vyberte modul výstrahy.</span><span class="sxs-lookup"><span data-stu-id="3a734-117">Select the alert module.</span></span>

    <span data-ttu-id="3a734-118">Pokud modul výstrahy ještě neexistuje, vyberte tlačítko se třemi tečkami (**...**) vedle položky **Chybové/informační zprávy** a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="3a734-118">If an alert module doesn't yet exist, select the ellipsis button (**...**) next to **Error/Information messages**, and then select **Add module**.</span></span> <span data-ttu-id="3a734-119">Vyberte modul výstrahy a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="3a734-119">Select the alert module, and then select **OK**.</span></span>

1. <span data-ttu-id="3a734-120">V podokně vlastností vpravo na kartě **Data** vyberte možnost **Přidat zdroj dat** a pak vyberte možnost **Obsah**</span><span class="sxs-lookup"><span data-stu-id="3a734-120">In the property pane on the right, on the **Data** tab, select **Add Data Source**, and then select **Content**.</span></span>
1. <span data-ttu-id="3a734-121">Do pole **Vstupní text** zadejte text uvítací zprávy.</span><span class="sxs-lookup"><span data-stu-id="3a734-121">In the **Input Text** field, enter the text of the welcome message.</span></span>
1. <span data-ttu-id="3a734-122">Uložte fragment záhlaví, vraťte jej se změnami a publikujte.</span><span class="sxs-lookup"><span data-stu-id="3a734-122">Save the header fragment, check it in, and publish it.</span></span>

<span data-ttu-id="3a734-123">Uvítací zpráva se nyní zobrazuje v horní části každé stránky webu, která používá vybraný fragment záhlaví.</span><span class="sxs-lookup"><span data-stu-id="3a734-123">The welcome message will now appear at the top of every site page that uses the selected header fragment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3a734-124">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="3a734-124">Additional resources</span></span>

[<span data-ttu-id="3a734-125">Přidání loga</span><span class="sxs-lookup"><span data-stu-id="3a734-125">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="3a734-126">Volba motivu webu</span><span class="sxs-lookup"><span data-stu-id="3a734-126">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="3a734-127">Práce se soubory přepisu šablon CSS</span><span class="sxs-lookup"><span data-stu-id="3a734-127">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="3a734-128">Přidání ikony oblíbené položky</span><span class="sxs-lookup"><span data-stu-id="3a734-128">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="3a734-129">Přidání oznámení o vlastnických právech</span><span class="sxs-lookup"><span data-stu-id="3a734-129">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="3a734-130">Přidání jazyků na web</span><span class="sxs-lookup"><span data-stu-id="3a734-130">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="3a734-131">Přidání kódu skriptu na webové stránky pro podporu telemetrie</span><span class="sxs-lookup"><span data-stu-id="3a734-131">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

