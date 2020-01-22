---
title: Přidání kódu skriptu na webové stránky pro podporu telemetrie
description: V tomto tématu je popsán postup přidání kódu skriptu na straně klienta na stránky webu za účelem podpory kolekce telemetrie na straně klienta.
author: bicyclingfool
manager: annbe
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
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 79d0e11946f3c6f4704d3a726d33de0378eb53bd
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914532"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="4983c-103">Přidání kódu skriptu na webové stránky pro podporu telemetrie</span><span class="sxs-lookup"><span data-stu-id="4983c-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="4983c-104">V tomto tématu je popsán postup přidání kódu skriptu na straně klienta na stránky webu za účelem podpory kolekce telemetrie na straně klienta.</span><span class="sxs-lookup"><span data-stu-id="4983c-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="4983c-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="4983c-105">Overview</span></span>

<span data-ttu-id="4983c-106">Služba Web Analytics je základní nástroj, který umožňuje pochopit, jakým způsobem zákazníci komunikují s webem, a učinit rozhodnutí, která pomohou optimalizovat prostředí s maximálním vylazením.</span><span class="sxs-lookup"><span data-stu-id="4983c-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="4983c-107">K dispozici je mnoho balíčků služby Web Analytics, které vám pomohou dosáhnout těchto cílů, jako jsou služby Google Analytics, Clicky, Moz Analytics a KISSMetrics.</span><span class="sxs-lookup"><span data-stu-id="4983c-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="4983c-108">Většina balíčků služby Web Analytics vyžaduje přidání kódu skriptu na straně klienta do prvku **\<head\>** kódu HTML pro všechny stránky vašeho webu.</span><span class="sxs-lookup"><span data-stu-id="4983c-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="4983c-109">Pokyny v tomto tématu se vztahují také na jiné vlastní funkce na straně klienta, které řešení Microsoft Dynamics 365 Commerce nativně nenabízí.</span><span class="sxs-lookup"><span data-stu-id="4983c-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-fragment-for-your-script-code"></a><span data-ttu-id="4983c-110">Vytvoření opakovaně použitelného fragmentu kódu skriptu</span><span class="sxs-lookup"><span data-stu-id="4983c-110">Create a reusable fragment for your script code</span></span>

<span data-ttu-id="4983c-111">Po vytvoření fragmentu kódu skriptu jej lze opakovaně použít na všech stránkách vašeho webu.</span><span class="sxs-lookup"><span data-stu-id="4983c-111">After you create a fragment for your script code, it can be reused across all pages on your site.</span></span>

1. <span data-ttu-id="4983c-112">Přejde na **Fragmenty \> Nový fragment stránky**.</span><span class="sxs-lookup"><span data-stu-id="4983c-112">Go to **Fragments \> New page fragment**.</span></span>
2. <span data-ttu-id="4983c-113">Vyberte možnost **Externískript**, zadejte název fragmentu a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="4983c-113">Select **External Script**, enter a name for the fragment, and then select **OK**.</span></span>
3. <span data-ttu-id="4983c-114">V hierarchii fragmentů vyberte pro fragment, který jste právě vytvořili, podřízený modul **Injektor skriptu**.</span><span class="sxs-lookup"><span data-stu-id="4983c-114">In the fragment hierarchy, select the **script injector** module child of the fragment that you just created.</span></span>
4. <span data-ttu-id="4983c-115">V podokně vlastností vpravo přidejte skript na straně klienta a nastavte další možnosti konfigurace podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="4983c-115">In the property pane on the right, add your client-side script, and set other configuration options as you require.</span></span>

## <a name="add-the-fragment-to-templates"></a><span data-ttu-id="4983c-116">Přidání fragmentu do šablon</span><span class="sxs-lookup"><span data-stu-id="4983c-116">Add the fragment to templates</span></span>

1. <span data-ttu-id="4983c-117">Přejděte na **Šablony** a otevřete šablonu pro stránky, na které chcete přidat kód skriptu.</span><span class="sxs-lookup"><span data-stu-id="4983c-117">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
2. <span data-ttu-id="4983c-118">V levém podokně rozbalte hierarchii šablon, aby se zobrazila pozice **Hlavička HTML**.</span><span class="sxs-lookup"><span data-stu-id="4983c-118">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
3. <span data-ttu-id="4983c-119">Vyberte tlačítko se třemi tečkami (**...**) vedle pozice **Hlavička HTML** a poté vyberte možnost **Přidat fragment**.</span><span class="sxs-lookup"><span data-stu-id="4983c-119">Select the ellipsis button (**...**) for the **HTML Head** slot, and then select **Add fragment**.</span></span>
4. <span data-ttu-id="4983c-120">Vyberte fragment, který jste pro kód skriptu vytvořili.</span><span class="sxs-lookup"><span data-stu-id="4983c-120">Select the fragment that you created for your script code.</span></span>
5. <span data-ttu-id="4983c-121">Uložte šablonu a vraťte ji se změnami.</span><span class="sxs-lookup"><span data-stu-id="4983c-121">Save the template, and check it in.</span></span>

> [!NOTE]
> <span data-ttu-id="4983c-122">Po dokončení je nutné publikovat fragment a hlavní šablonu.</span><span class="sxs-lookup"><span data-stu-id="4983c-122">After you've finished, you must publish the fragment and the master template.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="4983c-123">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="4983c-123">Additional resources</span></span>

[<span data-ttu-id="4983c-124">Přidání loga</span><span class="sxs-lookup"><span data-stu-id="4983c-124">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="4983c-125">Volba motivu webu</span><span class="sxs-lookup"><span data-stu-id="4983c-125">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="4983c-126">Práce se soubory přepisu šablon CSS</span><span class="sxs-lookup"><span data-stu-id="4983c-126">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="4983c-127">Přidání ikony oblíbené položky</span><span class="sxs-lookup"><span data-stu-id="4983c-127">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="4983c-128">Přidání uvítací zprávy</span><span class="sxs-lookup"><span data-stu-id="4983c-128">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="4983c-129">Přidání oznámení o vlastnických právech</span><span class="sxs-lookup"><span data-stu-id="4983c-129">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="4983c-130">Přidání jazyků na web</span><span class="sxs-lookup"><span data-stu-id="4983c-130">Add languages to your site</span></span>](add-languages-to-site.md)

