---
title: Vytvoření stránek s vlastní odpovědí pro chyby kódu stavu 4xx/5xx
description: Toto téma popisuje, jak vytvořit stránky s vlastní odpovědí pro chyby kódu stavu 4xx a 5xx pomocí nástrojů pro tvorbu obsahu v řešení Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
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
ms.openlocfilehash: bcceeb1bc68c6432442c863ca06b7ba81d0abed8
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697099"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a><span data-ttu-id="3018a-103">Vytvoření stránek s vlastní odpovědí pro chyby kódu stavu 4xx/5xx</span><span class="sxs-lookup"><span data-stu-id="3018a-103">Build custom response pages for 4xx/5xx status code errors</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="3018a-104">Toto téma popisuje, jak vytvořit stránky s vlastní odpovědí pro chyby kódu stavu 4xx a 5xx pomocí nástrojů pro tvorbu obsahu v řešení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3018a-104">This topic describes how to build custom response pages for 4xx and 5xx status code errors by using the authoring tools in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="3018a-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="3018a-105">Overview</span></span>

<span data-ttu-id="3018a-106">Není-li požadavek úspěšný, server vydá odpovědi na chyby kódu stavu HTTP.</span><span class="sxs-lookup"><span data-stu-id="3018a-106">If a request isn't successful, the server issues HTTP status code error responses.</span></span> <span data-ttu-id="3018a-107">Kód stavu 404 je zachycen a vrácen v případě, že stránka nebyla nalezena a kód stavu 500 je zachycen a vrácen, pokud dojde k chybě serveru.</span><span class="sxs-lookup"><span data-stu-id="3018a-107">The 404 status code is captured and returned if a page isn't found, and the 500 status code is captured and returned if a server error occurs.</span></span> <span data-ttu-id="3018a-108">V Dynamics 365 Commerce mohou uživatelé aplikace vytvářet stránky s vlastními odpovědmi na chyby kódu stavu, které jsou zobrazeny uživatelům.</span><span class="sxs-lookup"><span data-stu-id="3018a-108">In Dynamics 365 Commerce, application users can build custom status code error response pages that are shown to users for these status code error responses.</span></span>

## <a name="build-a-status-code-error-response-page"></a><span data-ttu-id="3018a-109">Sestavení stránky s odpovědí na chybu kódu stavu</span><span class="sxs-lookup"><span data-stu-id="3018a-109">Build a status code error response page</span></span>

<span data-ttu-id="3018a-110">Chcete-li sestavit stránku s odpovědí na chybu kódu stavu, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="3018a-110">To start to build a status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="3018a-111">V upřednostňovaném webovém prohlížeči se přihlaste k řešení Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3018a-111">In your preferred web browser, sign in to Dynamics 365 Commerce.</span></span> 
1. <span data-ttu-id="3018a-112">Vyberte web, pro který chcete vytvořit stránku s odpovědí na chybu kódu stavu 4xx/5xx.</span><span class="sxs-lookup"><span data-stu-id="3018a-112">Select the site that you want to build a 4xx/5xx status code error response page for.</span></span>

### <a name="build-the-template"></a><span data-ttu-id="3018a-113">Sestavení šablony</span><span class="sxs-lookup"><span data-stu-id="3018a-113">Build the template</span></span>

<span data-ttu-id="3018a-114">Chcete-li sestavit šablonu pro chybu kódu stavu, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="3018a-114">To build the template for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="3018a-115">Přejít na **Šablony \> Nová šablona**.</span><span class="sxs-lookup"><span data-stu-id="3018a-115">Go to **Templates \> New template**.</span></span>
1. <span data-ttu-id="3018a-116">Pojmenujte novou šablonu.</span><span class="sxs-lookup"><span data-stu-id="3018a-116">Name the new template.</span></span>
1. <span data-ttu-id="3018a-117">Sestavte šablonu na základě struktury, kterou má mít stránka s odpovědí na chybu kódu stavu.</span><span class="sxs-lookup"><span data-stu-id="3018a-117">Build the template, based on the structure that you want the status code error response page to have.</span></span>
1. <span data-ttu-id="3018a-118">Vraťte šablonu se změnami a publikujte ji.</span><span class="sxs-lookup"><span data-stu-id="3018a-118">Check the template in, and publish it.</span></span>

### <a name="build-the-status-code-error-response-page"></a><span data-ttu-id="3018a-119">Sestavení stránky s odpovědí na chybu kódu stavu</span><span class="sxs-lookup"><span data-stu-id="3018a-119">Build the status code error response page</span></span>

<span data-ttu-id="3018a-120">Chcete-li sestavit stránku s odpovědí na chybu kódu stavu, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="3018a-120">To build the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="3018a-121">Přejděte na **Stránky \> Nová stránka**.</span><span class="sxs-lookup"><span data-stu-id="3018a-121">Go to **Pages \> New Page**.</span></span>
1. <span data-ttu-id="3018a-122">Pojmenujte stránku s odpovědí na chybu kódu stavu, ale **nenastavujte** pole **Adresa URL**.</span><span class="sxs-lookup"><span data-stu-id="3018a-122">Name the status code error response page, but do **not** set the **URL** field.</span></span>
1. <span data-ttu-id="3018a-123">Sestavte stránku.</span><span class="sxs-lookup"><span data-stu-id="3018a-123">Build the page.</span></span>
1. <span data-ttu-id="3018a-124">Vraťte stránku se změnami a publikujte ji.</span><span class="sxs-lookup"><span data-stu-id="3018a-124">Check the page in, and publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="3018a-125">Můžete vytvořit samostatné stránky s odpovědí na chyby kódu stavu 4xx a 5xx.</span><span class="sxs-lookup"><span data-stu-id="3018a-125">You can create separate status code error response pages for 4xx and 5xx status code errors.</span></span> <span data-ttu-id="3018a-126">Případně můžete pro obě kategorie chyb použít stejnou stránku s obecnou odpovědí na chybu kódu stavu.</span><span class="sxs-lookup"><span data-stu-id="3018a-126">Alternatively, you can use the same general status code error response page for both error categories.</span></span>

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a><span data-ttu-id="3018a-127">Nastavení přesměrování na stránku s odpovědí na chybu kódu stavu</span><span class="sxs-lookup"><span data-stu-id="3018a-127">Set up a redirect for the status code error response page</span></span>

<span data-ttu-id="3018a-128">Chcete-li nastavit přesměrování pro chybu kódu stavu, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="3018a-128">To set up a redirect for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="3018a-129">Přejděte na **Adresy URL \> Nová \> Nový alias** a vyberte stránku s odpovědí na chybu kódu stavu, kterou jste vytvořili dříve.</span><span class="sxs-lookup"><span data-stu-id="3018a-129">Go to **URLs \> New \> New Alias**, and select the status code error response page that you built earlier.</span></span>
1. <span data-ttu-id="3018a-130">V poli **Alias** zadejte buď **výchozí-4xx** nebo **výchozí-5xx** v závislosti na stránce s odpovědí na chybu kódu stavu, pro kterou nastavujete přesměrování.</span><span class="sxs-lookup"><span data-stu-id="3018a-130">In the **Alias** field, enter either **default-4xx** or **default-5xx**, depending on the status code error response page that you're setting up a redirect for.</span></span> <span data-ttu-id="3018a-131">Tyto aliasy musí být publikovány.</span><span class="sxs-lookup"><span data-stu-id="3018a-131">These aliases must be published.</span></span> <span data-ttu-id="3018a-132">V opačném případě nebude přesměrování fungovat.</span><span class="sxs-lookup"><span data-stu-id="3018a-132">Otherwise, the redirect won't work.</span></span>
1. <span data-ttu-id="3018a-133">Zvolte **OK** pro potvrzení propojení.</span><span class="sxs-lookup"><span data-stu-id="3018a-133">Select **OK** to commit the linking.</span></span>

> [!NOTE]
> <span data-ttu-id="3018a-134">Pokud pro obě kategorie chyb používáte jedinou stránku s odpovědí na chybu kódu stavu, opakujte tento postup a propojte alias jiné kategorie chyb na stejné stránce.</span><span class="sxs-lookup"><span data-stu-id="3018a-134">If you're using a single status code error response page for both error categories, repeat this procedure to link an alias for the other error category to the same page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3018a-135">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="3018a-135">Additional resources</span></span>

[<span data-ttu-id="3018a-136">Práce se šablonami</span><span class="sxs-lookup"><span data-stu-id="3018a-136">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="3018a-137">Přidání nové webové stránky</span><span class="sxs-lookup"><span data-stu-id="3018a-137">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="3018a-138">Vytvoření URL adresy stránky</span><span class="sxs-lookup"><span data-stu-id="3018a-138">Create a page URL</span></span>](create-page-url.md)
