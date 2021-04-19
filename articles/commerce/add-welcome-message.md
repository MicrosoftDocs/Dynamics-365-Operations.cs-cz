---
title: Přidání uvítací zprávy
description: V tomto tématu je popsán postup při přidání uvítací zprávy na webovou stránku Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3e61f43eca7d1343d020e1c01b5b1140f07b63c6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797376"
---
# <a name="add-a-welcome-message"></a><span data-ttu-id="3530f-103">Přidání uvítací zprávy</span><span class="sxs-lookup"><span data-stu-id="3530f-103">Add a welcome message</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3530f-104">V tomto tématu je popsán postup při přidání uvítací zprávy na webovou stránku Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3530f-104">This topic describes how to add a welcome message to your Microsoft Dynamics 365 Commerce website.</span></span>

<span data-ttu-id="3530f-105">Uvítací zpráva na webu elektronického obchodu může informovat návštěvníky o probíhajícím prodeji, aktualizacích webu nebo dostupnosti sezónních kolekcí.</span><span class="sxs-lookup"><span data-stu-id="3530f-105">A welcome message on your e-Commerce website can inform visitors about ongoing sales, site updates, or availability of seasonal collections.</span></span> <span data-ttu-id="3530f-106">Uvítací zpráva je nastavena pomocí modulu výstrahy.</span><span class="sxs-lookup"><span data-stu-id="3530f-106">The welcome message is set by using the alert module.</span></span>

<span data-ttu-id="3530f-107">Modul výstrahy by měl být přidán do pozice **Chybové/informační zprávy** ve fragmentu záhlaví.</span><span class="sxs-lookup"><span data-stu-id="3530f-107">The alert module should be added to the **Error/Information messages** slot of the header fragment.</span></span> <span data-ttu-id="3530f-108">Modul výstrahy umožňuje zadat zobrazovaný text, jeho barvu a zarovnání.</span><span class="sxs-lookup"><span data-stu-id="3530f-108">The alert module lets you specify the text that is shown, the text color, and the alignment.</span></span> <span data-ttu-id="3530f-109">Umožňuje také určit, zda návštěvníci webu mohou zprávu zamítnout.</span><span class="sxs-lookup"><span data-stu-id="3530f-109">It also lets you specify whether visitors to the site can dismiss the message.</span></span>

<span data-ttu-id="3530f-110">Uvítací zpráva, která je přidána do sdíleného fragmentu záhlaví, se zobrazí na všech stránkách, které používají šablonu, v níž je použit sdílený fragment záhlaví.</span><span class="sxs-lookup"><span data-stu-id="3530f-110">When a welcome message is added to a shared header fragment, it will be shown on every page that uses the template where that shared header fragment is used.</span></span>

<span data-ttu-id="3530f-111">Chcete-li na svůj web přidat uvítací zprávu, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="3530f-111">To add a welcome message to your site, follow these steps.</span></span>

1. <span data-ttu-id="3530f-112">V tvůrci webů Commerce přejděte na svůj web.</span><span class="sxs-lookup"><span data-stu-id="3530f-112">In Commerce site builder, go to your site.</span></span>
1. <span data-ttu-id="3530f-113">Vyberte **Fragmenty**.</span><span class="sxs-lookup"><span data-stu-id="3530f-113">Select **Fragments**.</span></span>
1. <span data-ttu-id="3530f-114">Vyberte fragment záhlaví, do kterého chcete přidat zprávu.</span><span class="sxs-lookup"><span data-stu-id="3530f-114">Select the header fragment to add the message to.</span></span>
1. <span data-ttu-id="3530f-115">Ve stromové struktuře rozbalte **Chybové/informační zprávy**.</span><span class="sxs-lookup"><span data-stu-id="3530f-115">In the outline tree, expand **Error/Information messages**.</span></span>
1. <span data-ttu-id="3530f-116">Vyberte modul výstrahy a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="3530f-116">Select the alert module, and then select **OK**.</span></span> <span data-ttu-id="3530f-117">Pokud modul výstrahy ještě neexistuje, nejprve vyberte tlačítko se třemi tečkami (**...**) vedle položky **Chybové/informační zprávy** a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="3530f-117">If an alert module doesn't yet exist, first select the ellipsis button (**...**) next to **Error/Information messages**, and then select **Add module**.</span></span>
1. <span data-ttu-id="3530f-118">V podokně vlastností vpravo na kartě **Data** vyberte možnost **Přidat zdroj dat** a pak vyberte možnost **Obsah**</span><span class="sxs-lookup"><span data-stu-id="3530f-118">In the property pane on the right, on the **Data** tab, select **Add Data Source**, and then select **Content**.</span></span>
1. <span data-ttu-id="3530f-119">Do pole **Vstupní text** zadejte text uvítací zprávy.</span><span class="sxs-lookup"><span data-stu-id="3530f-119">In the **Input Text** field, enter the text of the welcome message.</span></span>
1. <span data-ttu-id="3530f-120">Chcete-li vrátit fragment záhlaví se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** jej publikujte.</span><span class="sxs-lookup"><span data-stu-id="3530f-120">Select **Save**, select **Finish editing** to check in the header fragment, and then select **Publish** to publish it.</span></span> 

<span data-ttu-id="3530f-121">Uvítací zpráva se nyní zobrazuje v horní části každé stránky webu, která používá vybraný fragment záhlaví.</span><span class="sxs-lookup"><span data-stu-id="3530f-121">The welcome message will now appear at the top of every site page that uses the selected header fragment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3530f-122">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="3530f-122">Additional resources</span></span>

[<span data-ttu-id="3530f-123">Přidání loga</span><span class="sxs-lookup"><span data-stu-id="3530f-123">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="3530f-124">Volba motivu webu</span><span class="sxs-lookup"><span data-stu-id="3530f-124">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="3530f-125">Práce se soubory přepisu šablon CSS</span><span class="sxs-lookup"><span data-stu-id="3530f-125">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="3530f-126">Přidání ikony oblíbené položky</span><span class="sxs-lookup"><span data-stu-id="3530f-126">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="3530f-127">Přidání oznámení o vlastnických právech</span><span class="sxs-lookup"><span data-stu-id="3530f-127">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="3530f-128">Přidání jazyků na web</span><span class="sxs-lookup"><span data-stu-id="3530f-128">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="3530f-129">Přidání kódu skriptu na webové stránky pro podporu telemetrie</span><span class="sxs-lookup"><span data-stu-id="3530f-129">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
