---
title: Přidání uvítací zprávy
description: V tomto tématu je popsán postup při přidání uvítací zprávy na webovou stránku Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5910ab85b1b0b2df992a24ad3cf7a032e7b98ea9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980125"
---
# <a name="add-a-welcome-message"></a><span data-ttu-id="fedc7-103">Přidání uvítací zprávy</span><span class="sxs-lookup"><span data-stu-id="fedc7-103">Add a welcome message</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="fedc7-104">V tomto tématu je popsán postup při přidání uvítací zprávy na webovou stránku Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="fedc7-104">This topic describes how to add a welcome message to your Microsoft Dynamics 365 Commerce website.</span></span>

## <a name="overview"></a><span data-ttu-id="fedc7-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="fedc7-105">Overview</span></span>

<span data-ttu-id="fedc7-106">Uvítací zpráva na webu elektronického obchodu může informovat návštěvníky o probíhajícím prodeji, aktualizacích webu nebo dostupnosti sezónních kolekcí.</span><span class="sxs-lookup"><span data-stu-id="fedc7-106">A welcome message on your e-Commerce website can inform visitors about ongoing sales, site updates, or availability of seasonal collections.</span></span> <span data-ttu-id="fedc7-107">Uvítací zpráva je nastavena pomocí modulu výstrahy.</span><span class="sxs-lookup"><span data-stu-id="fedc7-107">The welcome message is set by using the alert module.</span></span>

<span data-ttu-id="fedc7-108">Modul výstrahy by měl být přidán do pozice **Chybové/informační zprávy** ve fragmentu záhlaví.</span><span class="sxs-lookup"><span data-stu-id="fedc7-108">The alert module should be added to the **Error/Information messages** slot of the header fragment.</span></span> <span data-ttu-id="fedc7-109">Modul výstrahy umožňuje zadat zobrazovaný text, jeho barvu a zarovnání.</span><span class="sxs-lookup"><span data-stu-id="fedc7-109">The alert module lets you specify the text that is shown, the text color, and the alignment.</span></span> <span data-ttu-id="fedc7-110">Umožňuje také určit, zda návštěvníci webu mohou zprávu zamítnout.</span><span class="sxs-lookup"><span data-stu-id="fedc7-110">It also lets you specify whether visitors to the site can dismiss the message.</span></span>

<span data-ttu-id="fedc7-111">Uvítací zpráva, která je přidána do sdíleného fragmentu záhlaví, se zobrazí na všech stránkách, které používají šablonu, v níž je použit sdílený fragment záhlaví.</span><span class="sxs-lookup"><span data-stu-id="fedc7-111">When a welcome message is added to a shared header fragment, it will be shown on every page that uses the template where that shared header fragment is used.</span></span>

<span data-ttu-id="fedc7-112">Chcete-li na svůj web přidat uvítací zprávu, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="fedc7-112">To add a welcome message to your site, follow these steps.</span></span>

1. <span data-ttu-id="fedc7-113">V tvůrci webů Commerce přejděte na svůj web.</span><span class="sxs-lookup"><span data-stu-id="fedc7-113">In Commerce site builder, go to your site.</span></span>
1. <span data-ttu-id="fedc7-114">Vyberte **Fragmenty**.</span><span class="sxs-lookup"><span data-stu-id="fedc7-114">Select **Fragments**.</span></span>
1. <span data-ttu-id="fedc7-115">Vyberte fragment záhlaví, do kterého chcete přidat zprávu.</span><span class="sxs-lookup"><span data-stu-id="fedc7-115">Select the header fragment to add the message to.</span></span>
1. <span data-ttu-id="fedc7-116">Ve stromové struktuře rozbalte **Chybové/informační zprávy**.</span><span class="sxs-lookup"><span data-stu-id="fedc7-116">In the outline tree, expand **Error/Information messages**.</span></span>
1. <span data-ttu-id="fedc7-117">Vyberte modul výstrahy a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="fedc7-117">Select the alert module, and then select **OK**.</span></span> <span data-ttu-id="fedc7-118">Pokud modul výstrahy ještě neexistuje, nejprve vyberte tlačítko se třemi tečkami (**...**) vedle položky **Chybové/informační zprávy** a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="fedc7-118">If an alert module doesn't yet exist, first select the ellipsis button (**...**) next to **Error/Information messages**, and then select **Add module**.</span></span>
1. <span data-ttu-id="fedc7-119">V podokně vlastností vpravo na kartě **Data** vyberte možnost **Přidat zdroj dat** a pak vyberte možnost **Obsah**</span><span class="sxs-lookup"><span data-stu-id="fedc7-119">In the property pane on the right, on the **Data** tab, select **Add Data Source**, and then select **Content**.</span></span>
1. <span data-ttu-id="fedc7-120">Do pole **Vstupní text** zadejte text uvítací zprávy.</span><span class="sxs-lookup"><span data-stu-id="fedc7-120">In the **Input Text** field, enter the text of the welcome message.</span></span>
1. <span data-ttu-id="fedc7-121">Chcete-li vrátit fragment záhlaví se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** jej publikujte.</span><span class="sxs-lookup"><span data-stu-id="fedc7-121">Select **Save**, select **Finish editing** to check in the header fragment, and then select **Publish** to publish it.</span></span> 

<span data-ttu-id="fedc7-122">Uvítací zpráva se nyní zobrazuje v horní části každé stránky webu, která používá vybraný fragment záhlaví.</span><span class="sxs-lookup"><span data-stu-id="fedc7-122">The welcome message will now appear at the top of every site page that uses the selected header fragment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fedc7-123">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="fedc7-123">Additional resources</span></span>

[<span data-ttu-id="fedc7-124">Přidání loga</span><span class="sxs-lookup"><span data-stu-id="fedc7-124">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="fedc7-125">Volba motivu webu</span><span class="sxs-lookup"><span data-stu-id="fedc7-125">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="fedc7-126">Práce se soubory přepisu šablon CSS</span><span class="sxs-lookup"><span data-stu-id="fedc7-126">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="fedc7-127">Přidání ikony oblíbené položky</span><span class="sxs-lookup"><span data-stu-id="fedc7-127">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="fedc7-128">Přidání oznámení o vlastnických právech</span><span class="sxs-lookup"><span data-stu-id="fedc7-128">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="fedc7-129">Přidání jazyků na web</span><span class="sxs-lookup"><span data-stu-id="fedc7-129">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="fedc7-130">Přidání kódu skriptu na webové stránky pro podporu telemetrie</span><span class="sxs-lookup"><span data-stu-id="fedc7-130">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

