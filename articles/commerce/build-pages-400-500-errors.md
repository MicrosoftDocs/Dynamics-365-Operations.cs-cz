---
title: Vytvoření stránek s vlastní odpovědí pro chyby kódu stavu 4xx/5xx
description: Toto téma popisuje, jak vytvořit stránky s vlastní odpovědí pro chyby kódu stavu 4xx a 5xx pomocí nástrojů pro tvorbu obsahu v řešení Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 060f5e5616624279711f61f582e6a898c7eb7785
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269537"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a><span data-ttu-id="55034-103">Vytvoření stránek s vlastní odpovědí pro chyby kódu stavu 4xx/5xx</span><span class="sxs-lookup"><span data-stu-id="55034-103">Build custom response pages for 4xx/5xx status code errors</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="55034-104">Toto téma popisuje, jak vytvořit stránky s vlastní odpovědí pro chyby kódu stavu 4xx a 5xx pomocí nástrojů pro tvorbu obsahu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="55034-104">This topic describes how to build custom response pages for 4xx and 5xx status code errors by using the authoring tools in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="55034-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="55034-105">Overview</span></span>

<span data-ttu-id="55034-106">Není-li požadavek úspěšný, server vydá odpovědi na chyby kódu stavu HTTP.</span><span class="sxs-lookup"><span data-stu-id="55034-106">If a request isn't successful, the server issues HTTP status code error responses.</span></span> <span data-ttu-id="55034-107">Kód stavu 404 je zachycen a vrácen v případě, že stránka nebyla nalezena a kód stavu 500 je zachycen a vrácen, pokud dojde k chybě serveru.</span><span class="sxs-lookup"><span data-stu-id="55034-107">The 404 status code is captured and returned if a page isn't found, and the 500 status code is captured and returned if a server error occurs.</span></span> <span data-ttu-id="55034-108">V Dynamics 365 Commerce mohou uživatelé aplikace vytvářet stránky s vlastními odpovědmi na chyby kódu stavu, které jsou zobrazeny uživatelům.</span><span class="sxs-lookup"><span data-stu-id="55034-108">In Dynamics 365 Commerce, application users can build custom status code error response pages that are shown to users for these status code error responses.</span></span>

## <a name="build-a-status-code-error-response-page"></a><span data-ttu-id="55034-109">Sestavení stránky s odpovědí na chybu kódu stavu</span><span class="sxs-lookup"><span data-stu-id="55034-109">Build a status code error response page</span></span>

<span data-ttu-id="55034-110">Chcete-li sestavit stránku s odpovědí na chybu kódu stavu, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="55034-110">To start to build a status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="55034-111">V upřednostňovaném webovém prohlížeči se přihlaste k řešení Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="55034-111">In your preferred web browser, sign in to Dynamics 365 Commerce.</span></span> 
1. <span data-ttu-id="55034-112">Vyberte web, pro který chcete vytvořit stránku s odpovědí na chybu kódu stavu 4xx/5xx.</span><span class="sxs-lookup"><span data-stu-id="55034-112">Select the site that you want to build a 4xx/5xx status code error response page for.</span></span>

### <a name="build-the-template"></a><span data-ttu-id="55034-113">Sestavení šablony</span><span class="sxs-lookup"><span data-stu-id="55034-113">Build the template</span></span>

<span data-ttu-id="55034-114">Chcete-li sestavit šablonu pro chybu kódu stavu, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="55034-114">To build the template for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="55034-115">Přejděte na **Šablony**.</span><span class="sxs-lookup"><span data-stu-id="55034-115">Go to **Templates**.</span></span>
1. <span data-ttu-id="55034-116">Zvolte **Nová** pro vytvoření šablony stránky.</span><span class="sxs-lookup"><span data-stu-id="55034-116">Select **New** to create a page template.</span></span>
1. <span data-ttu-id="55034-117">V dialogovém okně **Nová šablona** v části **Název šablony** zadejte název nové šablony a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="55034-117">In the **New Template** dialog box, under **Template Name**, enter a name for the new template, and then select **OK**.</span></span>
1. <span data-ttu-id="55034-118">Sestavte šablonu na základě struktury, kterou má mít stránka s odpovědí na chybu kódu stavu.</span><span class="sxs-lookup"><span data-stu-id="55034-118">Build the template, based on the structure that you want the status code error response page to have.</span></span>
1. <span data-ttu-id="55034-119">Chcete-li vrátit šablonu se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="55034-119">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 

### <a name="build-the-status-code-error-response-page"></a><span data-ttu-id="55034-120">Sestavení stránky s odpovědí na chybu kódu stavu</span><span class="sxs-lookup"><span data-stu-id="55034-120">Build the status code error response page</span></span>

<span data-ttu-id="55034-121">Chcete-li sestavit stránku s odpovědí na chybu kódu stavu, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="55034-121">To build the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="55034-122">Přejít na **Stránky**.</span><span class="sxs-lookup"><span data-stu-id="55034-122">Go to **Pages**.</span></span>
1. <span data-ttu-id="55034-123">Volbou **Nová** vytvořte stránku.</span><span class="sxs-lookup"><span data-stu-id="55034-123">Select **New** to create a page.</span></span>
1. <span data-ttu-id="55034-124">V dialogovém okně **Zvolte šablonu** vyberte šablonu a pak v části **Název stránky** zadejte název pro stránku s reakcí na kód chybového stavu.</span><span class="sxs-lookup"><span data-stu-id="55034-124">In the **Choose a template** dialog box, select a template, and then, under **Page name**, enter a name for the status code error response page.</span></span> <span data-ttu-id="55034-125">Ponechejte pole **Adresa URL stránky** prázdné.</span><span class="sxs-lookup"><span data-stu-id="55034-125">Leave the **Page URL** field blank.</span></span>
1. <span data-ttu-id="55034-126">Sestavte stránku.</span><span class="sxs-lookup"><span data-stu-id="55034-126">Build the page.</span></span>
1. <span data-ttu-id="55034-127">Chcete-li vrátit stránku se změnami, vyberte možnost **Uložit**, pak **Dokončit úpravy** a volbou **Publikovat** ji publikujte.</span><span class="sxs-lookup"><span data-stu-id="55034-127">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="55034-128">Můžete vytvořit samostatné stránky s odpovědí na chyby kódu stavu 4xx a 5xx.</span><span class="sxs-lookup"><span data-stu-id="55034-128">You can create separate status code error response pages for 4xx and 5xx status code errors.</span></span> <span data-ttu-id="55034-129">Případně můžete pro obě kategorie chyb použít stejnou stránku s obecnou odpovědí na chybu kódu stavu.</span><span class="sxs-lookup"><span data-stu-id="55034-129">Alternatively, you can use the same general status code error response page for both error categories.</span></span>

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a><span data-ttu-id="55034-130">Nastavení přesměrování na stránku s odpovědí na chybu kódu stavu</span><span class="sxs-lookup"><span data-stu-id="55034-130">Set up a redirect for the status code error response page</span></span>

<span data-ttu-id="55034-131">Chcete-li nastavit přesměrování pro chybu kódu stavu, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="55034-131">To set up a redirect for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="55034-132">Přejděte na **Adresy URL \> Nová \> Nový alias** a vyberte stránku s odpovědí na chybu kódu stavu, kterou jste vytvořili dříve.</span><span class="sxs-lookup"><span data-stu-id="55034-132">Go to **URLs \> New \> New Alias**, and select the status code error response page that you built earlier.</span></span>
1. <span data-ttu-id="55034-133">V poli **Alias** zadejte buď **výchozí-4xx** nebo **výchozí-5xx** v závislosti na stránce s odpovědí na chybu kódu stavu, pro kterou nastavujete přesměrování.</span><span class="sxs-lookup"><span data-stu-id="55034-133">In the **Alias** field, enter either **default-4xx** or **default-5xx**, depending on the status code error response page that you're setting up a redirect for.</span></span> <span data-ttu-id="55034-134">Tyto aliasy musí být publikovány.</span><span class="sxs-lookup"><span data-stu-id="55034-134">These aliases must be published.</span></span> <span data-ttu-id="55034-135">V opačném případě nebude přesměrování fungovat.</span><span class="sxs-lookup"><span data-stu-id="55034-135">Otherwise, the redirect won't work.</span></span>
1. <span data-ttu-id="55034-136">Zvolte **OK** pro potvrzení propojení.</span><span class="sxs-lookup"><span data-stu-id="55034-136">Select **OK** to commit the linking.</span></span>

> [!NOTE]
> <span data-ttu-id="55034-137">Pokud pro obě kategorie chyb používáte jedinou stránku s odpovědí na chybu kódu stavu, opakujte tento postup a propojte alias jiné kategorie chyb na stejné stránce.</span><span class="sxs-lookup"><span data-stu-id="55034-137">If you're using a single status code error response page for both error categories, repeat this procedure to link an alias for the other error category to the same page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="55034-138">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="55034-138">Additional resources</span></span>

[<span data-ttu-id="55034-139">Práce se šablonami</span><span class="sxs-lookup"><span data-stu-id="55034-139">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="55034-140">Přidání nové webové stránky</span><span class="sxs-lookup"><span data-stu-id="55034-140">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="55034-141">Vytvoření URL adresy stránky</span><span class="sxs-lookup"><span data-stu-id="55034-141">Create a page URL</span></span>](create-page-url.md)
