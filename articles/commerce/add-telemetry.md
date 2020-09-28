---
title: Přidání kódu skriptu na webové stránky pro podporu telemetrie
description: V tomto tématu je popsán postup přidání kódu skriptu na straně klienta na stránky webu za účelem podpory kolekce telemetrie na straně klienta.
author: bicyclingfool
manager: annbe
ms.date: 08/31/2020
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
ms.openlocfilehash: a88f4f920154aafaa15a48af67365152e21111f7
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761242"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="d9a43-103">Přidání kódu skriptu na webové stránky pro podporu telemetrie</span><span class="sxs-lookup"><span data-stu-id="d9a43-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d9a43-104">V tomto tématu je popsán postup přidání kódu skriptu na straně klienta na stránky webu za účelem podpory kolekce telemetrie na straně klienta.</span><span class="sxs-lookup"><span data-stu-id="d9a43-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

## <a name="overview"></a><span data-ttu-id="d9a43-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="d9a43-105">Overview</span></span>

<span data-ttu-id="d9a43-106">Služba Web Analytics je základní nástroj, který umožňuje pochopit, jakým způsobem zákazníci komunikují s webem, a učinit rozhodnutí, která pomohou optimalizovat prostředí s maximálním vylazením.</span><span class="sxs-lookup"><span data-stu-id="d9a43-106">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="d9a43-107">K dispozici je mnoho balíčků služby Web Analytics, které vám pomohou dosáhnout těchto cílů, jako jsou služby Google Analytics, Clicky, Moz Analytics a KISSMetrics.</span><span class="sxs-lookup"><span data-stu-id="d9a43-107">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="d9a43-108">Většina balíčků služby Web Analytics vyžaduje přidání kódu skriptu na straně klienta do prvku **\<head\>** kódu HTML pro všechny stránky vašeho webu.</span><span class="sxs-lookup"><span data-stu-id="d9a43-108">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="d9a43-109">Pokyny v tomto tématu se vztahují také na jiné vlastní funkce na straně klienta, které řešení Microsoft Dynamics 365 Commerce nativně nenabízí.</span><span class="sxs-lookup"><span data-stu-id="d9a43-109">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-fragment-for-your-script-code"></a><span data-ttu-id="d9a43-110">Vytvoření opakovaně použitelného fragmentu kódu skriptu</span><span class="sxs-lookup"><span data-stu-id="d9a43-110">Create a reusable fragment for your script code</span></span>

<span data-ttu-id="d9a43-111">Fragment umožňuje opakované použití vloženého nebo vnějšího kódu skriptu na všech stránkách vašeho webu bez ohledu na použitou šablonu.</span><span class="sxs-lookup"><span data-stu-id="d9a43-111">A fragment allows you to reuse inline or external script code across all pages on your site, regardless of the template they use.</span></span>

### <a name="create-a-reusable-fragment-for-your-inline-script-code"></a><span data-ttu-id="d9a43-112">Vytvoření opakovaně použitelného fragmentu pro váš kód vloženého skriptu</span><span class="sxs-lookup"><span data-stu-id="d9a43-112">Create a reusable fragment for your inline script code</span></span>

<span data-ttu-id="d9a43-113">Chcete-li vytvořit opakovaně použitelný fragment pro vložený kód skriptu v rámci konfigurátoru webu, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="d9a43-113">To create a reusable fragment for your inline script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="d9a43-114">Přejděte na **Fragmenty** a pak vyberte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="d9a43-114">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="d9a43-115">V dialogovém okně **Nový fragment** vyberte **Vložený skript**.</span><span class="sxs-lookup"><span data-stu-id="d9a43-115">In the **New fragment** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="d9a43-116">V části **Název fragmentu** zadejte název fragmentu a poté vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d9a43-116">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="d9a43-117">V rámci vytvořeného fragmentu vyberte modul **Výchozí vložený skript**.</span><span class="sxs-lookup"><span data-stu-id="d9a43-117">Under the fragment that you created, select the **Default inline script** module.</span></span>
1. <span data-ttu-id="d9a43-118">V podokně vlastností vpravo v části **vložený skript**zadejte skript na straně klienta.</span><span class="sxs-lookup"><span data-stu-id="d9a43-118">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="d9a43-119">Poté nakonfigurujte další možnosti podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="d9a43-119">Then configure other options as you require.</span></span>
1. <span data-ttu-id="d9a43-120">Vyberte **Uložit** a potom vyberte **Dokončit úpravy**.</span><span class="sxs-lookup"><span data-stu-id="d9a43-120">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="d9a43-121">Zvolte **Publikovat**.</span><span class="sxs-lookup"><span data-stu-id="d9a43-121">Select **Publish**.</span></span>

### <a name="create-a-reusable-fragment-for-your-external-script-code"></a><span data-ttu-id="d9a43-122">Vytvoření opakovaně použitelného fragmentu pro váš kód externího skriptu</span><span class="sxs-lookup"><span data-stu-id="d9a43-122">Create a reusable fragment for your external script code</span></span>

<span data-ttu-id="d9a43-123">Chcete-li vytvořit opakovaně použitelný fragment pro externí kód skriptu v rámci konfigurátoru webu, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="d9a43-123">To create a reusable fragment for your external script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="d9a43-124">Přejděte na **Fragmenty** a pak vyberte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="d9a43-124">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="d9a43-125">V dialogovém okně **Nový fragment** vyberte **Externí skript**.</span><span class="sxs-lookup"><span data-stu-id="d9a43-125">In the **New fragment** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="d9a43-126">V části **Název fragmentu** zadejte název fragmentu a poté vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="d9a43-126">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="d9a43-127">V rámci vytvořeného fragmentu vyberte modul **Výchozí externí skript**.</span><span class="sxs-lookup"><span data-stu-id="d9a43-127">Under the fragment that you created, select the **Default external script** module.</span></span>
1. <span data-ttu-id="d9a43-128">V podokně vlastností vpravo v části **Zdroj skriptu** přidejte externí nebo relativní adresu URL pro externí zdroj skriptu.</span><span class="sxs-lookup"><span data-stu-id="d9a43-128">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="d9a43-129">Poté nakonfigurujte další možnosti podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="d9a43-129">Then configure other options as you require.</span></span>
1. <span data-ttu-id="d9a43-130">Vyberte **Uložit** a potom vyberte **Dokončit úpravy**.</span><span class="sxs-lookup"><span data-stu-id="d9a43-130">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="d9a43-131">Zvolte **Publikovat**.</span><span class="sxs-lookup"><span data-stu-id="d9a43-131">Select **Publish**.</span></span>

## <a name="add-a-fragment-that-includes-script-code-to-a-template"></a><span data-ttu-id="d9a43-132">Přidání fragmentu, který zahrnuje kód skriptu, do šablony</span><span class="sxs-lookup"><span data-stu-id="d9a43-132">Add a fragment that includes script code to a template</span></span>

<span data-ttu-id="d9a43-133">Chcete-li přidat fragment, který obsahuje kód skriptu, do šablony v konfigurátoru webů, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="d9a43-133">To add a fragment that includes script code to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="d9a43-134">Přejděte na **Šablony** a otevřete šablonu pro stránky, na které chcete přidat kód skriptu.</span><span class="sxs-lookup"><span data-stu-id="d9a43-134">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="d9a43-135">V levém podokně rozbalte hierarchii šablon, aby se zobrazila pozice **Hlavička HTML**.</span><span class="sxs-lookup"><span data-stu-id="d9a43-135">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="d9a43-136">V pozici **Hlavička HTML** vyberte tlačítko se třemi tečkami (**...**) a poté vyberte možnost **Přidat fragment**.</span><span class="sxs-lookup"><span data-stu-id="d9a43-136">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="d9a43-137">Vyberte fragment, který jste pro kód skriptu vytvořili.</span><span class="sxs-lookup"><span data-stu-id="d9a43-137">Select the fragment that you created for your script code.</span></span>
1. <span data-ttu-id="d9a43-138">Vyberte **Uložit** a potom vyberte **Dokončit úpravy**.</span><span class="sxs-lookup"><span data-stu-id="d9a43-138">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="d9a43-139">Zvolte **Publikovat**.</span><span class="sxs-lookup"><span data-stu-id="d9a43-139">Select **Publish**.</span></span>

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a><span data-ttu-id="d9a43-140">Přidání externího skriptu nebo vloženého skriptu přímo do šablony</span><span class="sxs-lookup"><span data-stu-id="d9a43-140">Add an external script or inline script directly to a template</span></span>

<span data-ttu-id="d9a43-141">Chcete-li vložit vložený nebo externí skript přímo do sady stránek, která je řízena jedinou šablonou, nemusíte nejprve vytvořit fragment.</span><span class="sxs-lookup"><span data-stu-id="d9a43-141">If you want to insert an inline or external script directly into a set of pages that are controlled by a single template, you don't have to create a fragment first.</span></span>

### <a name="add-an-inline-script-directly-to-a-template"></a><span data-ttu-id="d9a43-142">Přidání vloženého skriptu přímo do šablony</span><span class="sxs-lookup"><span data-stu-id="d9a43-142">Add an inline script directly to a template</span></span>

<span data-ttu-id="d9a43-143">Chcete-li přidat vložený skript přímo do šablony v rámci konfigurátoru webu, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="d9a43-143">To add an inline script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="d9a43-144">Přejděte na **Šablony** a otevřete šablonu pro stránky, na které chcete přidat kód skriptu.</span><span class="sxs-lookup"><span data-stu-id="d9a43-144">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="d9a43-145">V levém podokně rozbalte hierarchii šablon, aby se zobrazila pozice **Hlavička HTML**.</span><span class="sxs-lookup"><span data-stu-id="d9a43-145">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="d9a43-146">V pozici **Hlavička HTML** vyberte tlačítko se třemi tečkami (**...**) a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="d9a43-146">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d9a43-147">V dialogovém okně **Přidat modul** vyberte **vložený skript**.</span><span class="sxs-lookup"><span data-stu-id="d9a43-147">In the **Add Module** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="d9a43-148">V podokně vlastností vpravo v části **vložený skript**zadejte skript na straně klienta.</span><span class="sxs-lookup"><span data-stu-id="d9a43-148">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="d9a43-149">Poté nakonfigurujte další možnosti podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="d9a43-149">Then configure other options as you require.</span></span>
1. <span data-ttu-id="d9a43-150">Vyberte **Uložit** a potom vyberte **Dokončit úpravy**.</span><span class="sxs-lookup"><span data-stu-id="d9a43-150">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="d9a43-151">Zvolte **Publikovat**.</span><span class="sxs-lookup"><span data-stu-id="d9a43-151">Select **Publish**.</span></span>

### <a name="add-an-external-script-directly-to-a-template"></a><span data-ttu-id="d9a43-152">Přidání externího skriptu přímo do šablony</span><span class="sxs-lookup"><span data-stu-id="d9a43-152">Add an external script directly to a template</span></span>

<span data-ttu-id="d9a43-153">Chcete-li přidat externí skript přímo do šablony v rámci konfigurátoru webu, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="d9a43-153">To add an external script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="d9a43-154">Přejděte na **Šablony** a otevřete šablonu pro stránky, na které chcete přidat kód skriptu.</span><span class="sxs-lookup"><span data-stu-id="d9a43-154">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="d9a43-155">V levém podokně rozbalte hierarchii šablon, aby se zobrazila pozice **Hlavička HTML**.</span><span class="sxs-lookup"><span data-stu-id="d9a43-155">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="d9a43-156">V pozici **Hlavička HTML** vyberte tlačítko se třemi tečkami (**...**) a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="d9a43-156">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="d9a43-157">V dialogovém okně **Přidat modul** vyberte **Externí skript**.</span><span class="sxs-lookup"><span data-stu-id="d9a43-157">In the **Add Module** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="d9a43-158">V podokně vlastností vpravo v části **Zdroj skriptu** přidejte externí nebo relativní adresu URL pro externí zdroj skriptu.</span><span class="sxs-lookup"><span data-stu-id="d9a43-158">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="d9a43-159">Poté nakonfigurujte další možnosti podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="d9a43-159">Then configure other options as you require.</span></span>
1. <span data-ttu-id="d9a43-160">Vyberte **Uložit** a potom vyberte **Dokončit úpravy**.</span><span class="sxs-lookup"><span data-stu-id="d9a43-160">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="d9a43-161">Zvolte **Publikovat**.</span><span class="sxs-lookup"><span data-stu-id="d9a43-161">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d9a43-162">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="d9a43-162">Additional resources</span></span>

[<span data-ttu-id="d9a43-163">Přidání loga</span><span class="sxs-lookup"><span data-stu-id="d9a43-163">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="d9a43-164">Volba motivu webu</span><span class="sxs-lookup"><span data-stu-id="d9a43-164">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="d9a43-165">Práce se soubory přepisu šablon CSS</span><span class="sxs-lookup"><span data-stu-id="d9a43-165">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="d9a43-166">Přidání ikony oblíbené položky</span><span class="sxs-lookup"><span data-stu-id="d9a43-166">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="d9a43-167">Přidání uvítací zprávy</span><span class="sxs-lookup"><span data-stu-id="d9a43-167">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="d9a43-168">Přidání oznámení o vlastnických právech</span><span class="sxs-lookup"><span data-stu-id="d9a43-168">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="d9a43-169">Přidání jazyků na web</span><span class="sxs-lookup"><span data-stu-id="d9a43-169">Add languages to your site</span></span>](add-languages-to-site.md)
