---
title: Přidání oznámení o vlastnických právech
description: V tomto tématu je popsán postup při přidání oznámení o autorských právech na web elektronického obchodu.
author: psimolin
manager: AnnBe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 54b48ee74bc9d9f2b77f0584a0bf1739a8dfdbdb
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025475"
---
# <a name="add-a-copyright-notice"></a><span data-ttu-id="ec555-103">Přidání oznámení o vlastnických právech</span><span class="sxs-lookup"><span data-stu-id="ec555-103">Add a copyright notice</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="ec555-104">V tomto tématu je popsán postup při přidání oznámení o autorských právech na web elektronického obchodu.</span><span class="sxs-lookup"><span data-stu-id="ec555-104">This topic describes how to add a copyright notice to your e-Commerce website.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ec555-105">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="ec555-105">Prerequisites</span></span>

<span data-ttu-id="ec555-106">Před přidáním oznámení o autorských právech na web je nutné mít k dispozici následující položky:</span><span class="sxs-lookup"><span data-stu-id="ec555-106">Before you can add a copyright notice to your site, you must have the following items:</span></span>

- <span data-ttu-id="ec555-107">Šablonu obsahující sdílený fragment zápatí.</span><span class="sxs-lookup"><span data-stu-id="ec555-107">A template that includes a shared footer fragment.</span></span>
- <span data-ttu-id="ec555-108">Stránku používající tuto šablonu.</span><span class="sxs-lookup"><span data-stu-id="ec555-108">A page that uses that template.</span></span>

## <a name="add-a-copyright-notice"></a><span data-ttu-id="ec555-109">Přidání oznámení o vlastnických právech</span><span class="sxs-lookup"><span data-stu-id="ec555-109">Add a copyright notice</span></span>

<span data-ttu-id="ec555-110">Chcete-li přidat oznámení o autorských právech do dolní části každé stránky, která používá určitou šablonu, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="ec555-110">To add a copyright notice to the bottom of every page that uses a specific template, follow these steps.</span></span>

1. <span data-ttu-id="ec555-111">Přejděte na **Fragmenty** a pak vyberte **Nový fragment stránky**.</span><span class="sxs-lookup"><span data-stu-id="ec555-111">Go to **Fragments**, and then select **New Page Fragment**.</span></span>
1. <span data-ttu-id="ec555-112">V dialogovém okně vyberte modul **Zápatí** a tento fragment pojmenujte.</span><span class="sxs-lookup"><span data-stu-id="ec555-112">In the dialog box, select the **Footer** module, and name the fragment.</span></span> <span data-ttu-id="ec555-113">Zadejte například **Zápatí–autorská práva**.</span><span class="sxs-lookup"><span data-stu-id="ec555-113">For example, enter **Footer-Copyright**.</span></span>
1. <span data-ttu-id="ec555-114">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="ec555-114">Select **OK**.</span></span>
1. <span data-ttu-id="ec555-115">V navigačním podokně vyberte tlačítko se třemi tečkami (**...**) vedle **Zápatí** a vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="ec555-115">In the navigation pane, select the ellipsis button (**...**) next to **Footer**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="ec555-116">V dialogovém okně vyberte **Kategorie zápati** a pak vyberte možnost **OK**.</span><span class="sxs-lookup"><span data-stu-id="ec555-116">In the dialog box, select **Footer category**, and then select **OK**.</span></span>
1. <span data-ttu-id="ec555-117">V navigačním podokně vyberte tlačítko se třemi tečkami vedle **Kategorie zápatí** a vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="ec555-117">In the navigation pane, select the ellipsis button next to **Footer category**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="ec555-118">V dialogovém okně vyberte **Textový blok** a pak vyberte možnost **OK**.</span><span class="sxs-lookup"><span data-stu-id="ec555-118">In the dialog box, select **Text block**, and then select **OK**.</span></span>
1. <span data-ttu-id="ec555-119">V navigačním podokně vyberte položku **Textový blok**.</span><span class="sxs-lookup"><span data-stu-id="ec555-119">In the navigation pane, select **Text block**.</span></span>
1. <span data-ttu-id="ec555-120">V podokně vlastností vpravo v poli **Odstavec** přidejte zprávu o autorských právech.</span><span class="sxs-lookup"><span data-stu-id="ec555-120">In the properties pane on the right, in the **Paragraph** field, add your copyright message.</span></span> <span data-ttu-id="ec555-121">Zadejte například **(C) Fabrikam 2019**.</span><span class="sxs-lookup"><span data-stu-id="ec555-121">For example, enter **(C) Fabrikam 2019**.</span></span>
1. <span data-ttu-id="ec555-122">Vyberte možnost **Uložit**, pak vyberte možnost **Vrátit se změnami** a pak vyberte možnost **Publikovat**.</span><span class="sxs-lookup"><span data-stu-id="ec555-122">Select **Save**, select **Check In**, and then select **Publish**.</span></span>
1. <span data-ttu-id="ec555-123">Přejděte na **Šablony**, vyberte šablonu a poté vyberte možnost **Rezervovat**.</span><span class="sxs-lookup"><span data-stu-id="ec555-123">Go to **Templates**, select the template, and then select **Check Out**.</span></span>
1. <span data-ttu-id="ec555-124">V části **Osnova stránky** rozbalte možnost **Text** a pak rozbalte možnost **Výchozí stránka**.</span><span class="sxs-lookup"><span data-stu-id="ec555-124">Under **Page Outline**, expand **Body**, and then expand **Default Page**.</span></span>
1. <span data-ttu-id="ec555-125">Vyberte tlačítko se třemi tečkami vedle **Pozice zápatí** a poté vyberte možnost **Přidat fragment**.</span><span class="sxs-lookup"><span data-stu-id="ec555-125">Select the ellipsis button next to **Footer Slot**, and then select **Add Fragment**.</span></span>
1. <span data-ttu-id="ec555-126">Vyberte fragment, který jste vytvořili dříve, a poté vyberte možnost **Vybrat**.</span><span class="sxs-lookup"><span data-stu-id="ec555-126">Select the fragment that you created earlier, and then select **Select**.</span></span>
1. <span data-ttu-id="ec555-127">Vraťte šablonu se změnami a publikujte ji.</span><span class="sxs-lookup"><span data-stu-id="ec555-127">Check in the template, and publish it.</span></span>

<span data-ttu-id="ec555-128">Zápatí, které obsahuje poznámku o autorských právech, se automaticky zobrazí v dolní části všech stránek, které používají vybranou šablonu.</span><span class="sxs-lookup"><span data-stu-id="ec555-128">The footer that contains the copyright notice automatically appears at the bottom of all pages that use the selected template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ec555-129">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="ec555-129">Additional resources</span></span>

[<span data-ttu-id="ec555-130">Přidání loga</span><span class="sxs-lookup"><span data-stu-id="ec555-130">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="ec555-131">Volba motivu webu</span><span class="sxs-lookup"><span data-stu-id="ec555-131">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="ec555-132">Práce se soubory přepisu šablon CSS</span><span class="sxs-lookup"><span data-stu-id="ec555-132">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="ec555-133">Přidání ikony oblíbené položky</span><span class="sxs-lookup"><span data-stu-id="ec555-133">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="ec555-134">Přidání uvítací zprávy</span><span class="sxs-lookup"><span data-stu-id="ec555-134">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="ec555-135">Přidání jazyků na web</span><span class="sxs-lookup"><span data-stu-id="ec555-135">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="ec555-136">Přidání kódu skriptu na webové stránky pro podporu telemetrie</span><span class="sxs-lookup"><span data-stu-id="ec555-136">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

