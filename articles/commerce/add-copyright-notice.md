---
title: Přidání oznámení o vlastnických právech
description: V tomto tématu je popsán postup při přidání oznámení o autorských právech na web elektronického obchodu.
author: psimolin
manager: AnnBe
ms.date: 12/12/2019
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
ms.openlocfilehash: 58c2949057ef777f706d12cee2dd3341d1a3b7e6
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914557"
---
# <a name="add-a-copyright-notice"></a><span data-ttu-id="ef062-103">Přidání oznámení o vlastnických právech</span><span class="sxs-lookup"><span data-stu-id="ef062-103">Add a copyright notice</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="ef062-104">V tomto tématu je popsán postup při přidání oznámení o autorských právech na web elektronického obchodu.</span><span class="sxs-lookup"><span data-stu-id="ef062-104">This topic describes how to add a copyright notice to your e-Commerce website.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ef062-105">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="ef062-105">Prerequisites</span></span>

<span data-ttu-id="ef062-106">Před přidáním oznámení o autorských právech na web je nutné mít k dispozici následující položky:</span><span class="sxs-lookup"><span data-stu-id="ef062-106">Before you can add a copyright notice to your site, you must have the following items:</span></span>

- <span data-ttu-id="ef062-107">Šablonu obsahující sdílený fragment zápatí.</span><span class="sxs-lookup"><span data-stu-id="ef062-107">A template that includes a shared footer fragment.</span></span>
- <span data-ttu-id="ef062-108">Stránku používající tuto šablonu.</span><span class="sxs-lookup"><span data-stu-id="ef062-108">A page that uses that template.</span></span>

## <a name="add-a-copyright-notice"></a><span data-ttu-id="ef062-109">Přidání oznámení o vlastnických právech</span><span class="sxs-lookup"><span data-stu-id="ef062-109">Add a copyright notice</span></span>

<span data-ttu-id="ef062-110">Chcete-li přidat oznámení o autorských právech do dolní části každé stránky, která používá určitou šablonu, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="ef062-110">To add a copyright notice to the bottom of every page that uses a specific template, follow these steps.</span></span>

1. <span data-ttu-id="ef062-111">Přejděte na **Fragmenty** a pak vyberte **Nový fragment stránky**.</span><span class="sxs-lookup"><span data-stu-id="ef062-111">Go to **Fragments**, and then select **New Page Fragment**.</span></span>
1. <span data-ttu-id="ef062-112">V dialogovém okně vyberte modul **Zápatí** a tento fragment pojmenujte.</span><span class="sxs-lookup"><span data-stu-id="ef062-112">In the dialog box, select the **Footer** module, and name the fragment.</span></span> <span data-ttu-id="ef062-113">Zadejte například **Zápatí–autorská práva**.</span><span class="sxs-lookup"><span data-stu-id="ef062-113">For example, enter **Footer-Copyright**.</span></span>
1. <span data-ttu-id="ef062-114">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="ef062-114">Select **OK**.</span></span>
1. <span data-ttu-id="ef062-115">V navigačním podokně vyberte tlačítko se třemi tečkami (**...**) vedle **Zápatí** a vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="ef062-115">In the navigation pane, select the ellipsis button (**...**) next to **Footer**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="ef062-116">V dialogovém okně vyberte **Kategorie zápati** a pak vyberte možnost **OK**.</span><span class="sxs-lookup"><span data-stu-id="ef062-116">In the dialog box, select **Footer category**, and then select **OK**.</span></span>
1. <span data-ttu-id="ef062-117">V navigačním podokně vyberte tlačítko se třemi tečkami vedle **Kategorie zápatí** a vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="ef062-117">In the navigation pane, select the ellipsis button next to **Footer category**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="ef062-118">V dialogovém okně vyberte **Položka bloku s formátovaným obsahem** a pak vyberte možnost **OK**.</span><span class="sxs-lookup"><span data-stu-id="ef062-118">In the dialog box, select **Content rich block item**, and then select **OK**.</span></span>
1. <span data-ttu-id="ef062-119">V navigačním podokně vyberte možnost **Položka bloku s formátovaným obsahem**</span><span class="sxs-lookup"><span data-stu-id="ef062-119">In the navigation pane, select **Content rich block item**.</span></span>
1. <span data-ttu-id="ef062-120">V podokně vlastností vpravo v poli **Odstavec** přidejte zprávu o autorských právech.</span><span class="sxs-lookup"><span data-stu-id="ef062-120">In the properties pane on the right, in the **Paragraph** field, add your copyright message.</span></span> <span data-ttu-id="ef062-121">Zadejte například **(C) Fabrikam 2019**.</span><span class="sxs-lookup"><span data-stu-id="ef062-121">For example, enter **(C) Fabrikam 2019**.</span></span>
1. <span data-ttu-id="ef062-122">Vyberte možnost **Uložit**, pak vyberte možnost **Vrátit se změnami** a pak vyberte možnost **Publikovat**.</span><span class="sxs-lookup"><span data-stu-id="ef062-122">Select **Save**, select **Check In**, and then select **Publish**.</span></span>
1. <span data-ttu-id="ef062-123">Přejděte na **Šablony**, vyberte šablonu a poté vyberte možnost **Rezervovat**.</span><span class="sxs-lookup"><span data-stu-id="ef062-123">Go to **Templates**, select the template, and then select **Check Out**.</span></span>
1. <span data-ttu-id="ef062-124">V části **Osnova stránky** rozbalte možnost **Text** a pak rozbalte možnost **Výchozí stránka**.</span><span class="sxs-lookup"><span data-stu-id="ef062-124">Under **Page Outline**, expand **Body**, and then expand **Default Page**.</span></span>
1. <span data-ttu-id="ef062-125">Vyberte tlačítko se třemi tečkami vedle **Pozice zápatí** a poté vyberte možnost **Přidat fragment**.</span><span class="sxs-lookup"><span data-stu-id="ef062-125">Select the ellipsis button next to **Footer Slot**, and then select **Add Fragment**.</span></span>
1. <span data-ttu-id="ef062-126">Vyberte fragment, který jste vytvořili dříve, a poté vyberte možnost **Vybrat**.</span><span class="sxs-lookup"><span data-stu-id="ef062-126">Select the fragment that you created earlier, and then select **Select**.</span></span>
1. <span data-ttu-id="ef062-127">Vraťte šablonu se změnami a publikujte ji.</span><span class="sxs-lookup"><span data-stu-id="ef062-127">Check in the template, and publish it.</span></span>

<span data-ttu-id="ef062-128">Zápatí, které obsahuje poznámku o autorských právech, se automaticky zobrazí v dolní části všech stránek, které používají vybranou šablonu.</span><span class="sxs-lookup"><span data-stu-id="ef062-128">The footer that contains the copyright notice automatically appears at the bottom of all pages that use the selected template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ef062-129">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="ef062-129">Additional resources</span></span>

[<span data-ttu-id="ef062-130">Přidání loga</span><span class="sxs-lookup"><span data-stu-id="ef062-130">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="ef062-131">Volba motivu webu</span><span class="sxs-lookup"><span data-stu-id="ef062-131">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="ef062-132">Práce se soubory přepisu šablon CSS</span><span class="sxs-lookup"><span data-stu-id="ef062-132">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="ef062-133">Přidání ikony oblíbené položky</span><span class="sxs-lookup"><span data-stu-id="ef062-133">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="ef062-134">Přidání uvítací zprávy</span><span class="sxs-lookup"><span data-stu-id="ef062-134">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="ef062-135">Přidání jazyků na web</span><span class="sxs-lookup"><span data-stu-id="ef062-135">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="ef062-136">Přidání kódu skriptu na webové stránky pro podporu telemetrie</span><span class="sxs-lookup"><span data-stu-id="ef062-136">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

