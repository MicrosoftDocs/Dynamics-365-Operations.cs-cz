---
title: Přidání kódu skriptu na webové stránky pro podporu telemetrie
description: V tomto tématu je popsán postup přidání kódu skriptu na straně klienta na stránky webu za účelem podpory kolekce telemetrie na straně klienta.
author: bicyclingfool
ms.date: 09/29/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: fb1773ab10b23a586eb6a8286f145181818585b9
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797424"
---
# <a name="add-script-code-to-site-pages-to-support-telemetry"></a><span data-ttu-id="837b5-103">Přidání kódu skriptu na webové stránky pro podporu telemetrie</span><span class="sxs-lookup"><span data-stu-id="837b5-103">Add script code to site pages to support telemetry</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="837b5-104">V tomto tématu je popsán postup přidání kódu skriptu na straně klienta na stránky webu za účelem podpory kolekce telemetrie na straně klienta.</span><span class="sxs-lookup"><span data-stu-id="837b5-104">This topic describes how to add client-side script code to your site pages to support the collection of client-side telemetry.</span></span>

<span data-ttu-id="837b5-105">Služba Web Analytics je základní nástroj, který umožňuje pochopit, jakým způsobem zákazníci komunikují s webem, a učinit rozhodnutí, která pomohou optimalizovat prostředí s maximálním vylazením.</span><span class="sxs-lookup"><span data-stu-id="837b5-105">Web analytics are an essential tool when you want to understand how your customers interact with your site and make decisions that will help optimize the experience for maximum conversion.</span></span> <span data-ttu-id="837b5-106">K dispozici je mnoho balíčků služby Web Analytics, které vám pomohou dosáhnout těchto cílů, jako jsou služby Google Analytics, Clicky, Moz Analytics a KISSMetrics.</span><span class="sxs-lookup"><span data-stu-id="837b5-106">Many web analytics packages are available to help you achieve these goals, such as Google Analytics, Clicky, Moz Analytics, and KISSMetrics.</span></span> <span data-ttu-id="837b5-107">Většina balíčků služby Web Analytics vyžaduje přidání kódu skriptu na straně klienta do prvku **\<head\>** kódu HTML pro všechny stránky vašeho webu.</span><span class="sxs-lookup"><span data-stu-id="837b5-107">Most web analytics packages require that you add client-side script code in the **\<head\>** element of the HTML for all pages of your site.</span></span>

> [!NOTE]
> <span data-ttu-id="837b5-108">Pokyny v tomto tématu se vztahují také na jiné vlastní funkce na straně klienta, které řešení Microsoft Dynamics 365 Commerce nativně nenabízí.</span><span class="sxs-lookup"><span data-stu-id="837b5-108">The instructions in this topic also apply to other custom client-side functionality that Microsoft Dynamics 365 Commerce doesn't natively offer.</span></span>

## <a name="create-a-reusable-fragment-for-your-script-code"></a><span data-ttu-id="837b5-109">Vytvoření opakovaně použitelného fragmentu kódu skriptu</span><span class="sxs-lookup"><span data-stu-id="837b5-109">Create a reusable fragment for your script code</span></span>

<span data-ttu-id="837b5-110">Fragment umožňuje opakované použití vloženého nebo vnějšího kódu skriptu na všech stránkách vašeho webu bez ohledu na použitou šablonu.</span><span class="sxs-lookup"><span data-stu-id="837b5-110">A fragment allows you to reuse inline or external script code across all pages on your site, regardless of the template they use.</span></span>

### <a name="create-a-reusable-fragment-for-your-inline-script-code"></a><span data-ttu-id="837b5-111">Vytvoření opakovaně použitelného fragmentu pro váš kód vloženého skriptu</span><span class="sxs-lookup"><span data-stu-id="837b5-111">Create a reusable fragment for your inline script code</span></span>

<span data-ttu-id="837b5-112">Chcete-li vytvořit opakovaně použitelný fragment pro vložený kód skriptu v rámci konfigurátoru webu, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="837b5-112">To create a reusable fragment for your inline script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="837b5-113">Přejděte na **Fragmenty** a pak vyberte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="837b5-113">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="837b5-114">V dialogovém okně **Nový fragment** vyberte **Vložený skript**.</span><span class="sxs-lookup"><span data-stu-id="837b5-114">In the **New fragment** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="837b5-115">V části **Název fragmentu** zadejte název fragmentu a poté vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="837b5-115">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="837b5-116">V rámci vytvořeného fragmentu vyberte modul **Výchozí vložený skript**.</span><span class="sxs-lookup"><span data-stu-id="837b5-116">Under the fragment that you created, select the **Default inline script** module.</span></span>
1. <span data-ttu-id="837b5-117">V podokně vlastností vpravo v části **vložený skript** zadejte skript na straně klienta.</span><span class="sxs-lookup"><span data-stu-id="837b5-117">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="837b5-118">Poté nakonfigurujte další možnosti podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="837b5-118">Then configure other options as you require.</span></span>
1. <span data-ttu-id="837b5-119">Vyberte **Uložit** a potom vyberte **Dokončit úpravy**.</span><span class="sxs-lookup"><span data-stu-id="837b5-119">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="837b5-120">Zvolte **Publikovat**.</span><span class="sxs-lookup"><span data-stu-id="837b5-120">Select **Publish**.</span></span>

### <a name="create-a-reusable-fragment-for-your-external-script-code"></a><span data-ttu-id="837b5-121">Vytvoření opakovaně použitelného fragmentu pro váš kód externího skriptu</span><span class="sxs-lookup"><span data-stu-id="837b5-121">Create a reusable fragment for your external script code</span></span>

<span data-ttu-id="837b5-122">Chcete-li vytvořit opakovaně použitelný fragment pro externí kód skriptu v rámci konfigurátoru webu, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="837b5-122">To create a reusable fragment for your external script code in site builder, follow these steps.</span></span>

1. <span data-ttu-id="837b5-123">Přejděte na **Fragmenty** a pak vyberte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="837b5-123">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="837b5-124">V dialogovém okně **Nový fragment** vyberte **Externí skript**.</span><span class="sxs-lookup"><span data-stu-id="837b5-124">In the **New fragment** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="837b5-125">V části **Název fragmentu** zadejte název fragmentu a poté vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="837b5-125">Under **Fragment name**, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="837b5-126">V rámci vytvořeného fragmentu vyberte modul **Výchozí externí skript**.</span><span class="sxs-lookup"><span data-stu-id="837b5-126">Under the fragment that you created, select the **Default external script** module.</span></span>
1. <span data-ttu-id="837b5-127">V podokně vlastností vpravo v části **Zdroj skriptu** přidejte externí nebo relativní adresu URL pro externí zdroj skriptu.</span><span class="sxs-lookup"><span data-stu-id="837b5-127">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="837b5-128">Poté nakonfigurujte další možnosti podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="837b5-128">Then configure other options as you require.</span></span>
1. <span data-ttu-id="837b5-129">Vyberte **Uložit** a potom vyberte **Dokončit úpravy**.</span><span class="sxs-lookup"><span data-stu-id="837b5-129">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="837b5-130">Zvolte **Publikovat**.</span><span class="sxs-lookup"><span data-stu-id="837b5-130">Select **Publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="837b5-131">Pokud jsou pro váš web povoleny zásady zabezpečení obsahu (CSP), je nutné, aby v konfigurátoru webů Commerce byly do směrnice CSP **script-src** přidány všechny externí adresy URL.</span><span class="sxs-lookup"><span data-stu-id="837b5-131">If content security policy (CSP) is enabled for your site, ensure that all external URLs are added to the **script-src** CSP directive in Commerce site builder.</span></span> <span data-ttu-id="837b5-132">Další informace viz [Správa zásad zabezpečení obsahu (CSP)](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="837b5-132">For more information, see [Manage Content Security Policy (CSP)](manage-csp.md).</span></span>

## <a name="add-a-fragment-that-includes-script-code-to-a-template"></a><span data-ttu-id="837b5-133">Přidání fragmentu, který zahrnuje kód skriptu, do šablony</span><span class="sxs-lookup"><span data-stu-id="837b5-133">Add a fragment that includes script code to a template</span></span>

<span data-ttu-id="837b5-134">Chcete-li přidat fragment, který obsahuje kód skriptu, do šablony v konfigurátoru webů, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="837b5-134">To add a fragment that includes script code to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="837b5-135">Přejděte na **Šablony** a otevřete šablonu pro stránky, na které chcete přidat kód skriptu.</span><span class="sxs-lookup"><span data-stu-id="837b5-135">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="837b5-136">V levém podokně rozbalte hierarchii šablon, aby se zobrazila pozice **Hlavička HTML**.</span><span class="sxs-lookup"><span data-stu-id="837b5-136">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="837b5-137">V pozici **Hlavička HTML** vyberte tlačítko se třemi tečkami (**...**) a poté vyberte možnost **Přidat fragment**.</span><span class="sxs-lookup"><span data-stu-id="837b5-137">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add fragment**.</span></span>
1. <span data-ttu-id="837b5-138">Vyberte fragment, který jste pro kód skriptu vytvořili.</span><span class="sxs-lookup"><span data-stu-id="837b5-138">Select the fragment that you created for your script code.</span></span>
1. <span data-ttu-id="837b5-139">Vyberte **Uložit** a potom vyberte **Dokončit úpravy**.</span><span class="sxs-lookup"><span data-stu-id="837b5-139">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="837b5-140">Zvolte **Publikovat**.</span><span class="sxs-lookup"><span data-stu-id="837b5-140">Select **Publish**.</span></span>

## <a name="add-an-external-script-or-inline-script-directly-to-a-template"></a><span data-ttu-id="837b5-141">Přidání externího skriptu nebo vloženého skriptu přímo do šablony</span><span class="sxs-lookup"><span data-stu-id="837b5-141">Add an external script or inline script directly to a template</span></span>

<span data-ttu-id="837b5-142">Chcete-li vložit vložený nebo externí skript přímo do sady stránek, která je řízena jedinou šablonou, nemusíte nejprve vytvořit fragment.</span><span class="sxs-lookup"><span data-stu-id="837b5-142">If you want to insert an inline or external script directly into a set of pages that are controlled by a single template, you don't have to create a fragment first.</span></span>

### <a name="add-an-inline-script-directly-to-a-template"></a><span data-ttu-id="837b5-143">Přidání vloženého skriptu přímo do šablony</span><span class="sxs-lookup"><span data-stu-id="837b5-143">Add an inline script directly to a template</span></span>

<span data-ttu-id="837b5-144">Chcete-li přidat vložený skript přímo do šablony v rámci konfigurátoru webu, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="837b5-144">To add an inline script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="837b5-145">Přejděte na **Šablony** a otevřete šablonu pro stránky, na které chcete přidat kód skriptu.</span><span class="sxs-lookup"><span data-stu-id="837b5-145">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="837b5-146">V levém podokně rozbalte hierarchii šablon, aby se zobrazila pozice **Hlavička HTML**.</span><span class="sxs-lookup"><span data-stu-id="837b5-146">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="837b5-147">V pozici **Hlavička HTML** vyberte tlačítko se třemi tečkami (**...**) a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="837b5-147">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="837b5-148">V dialogovém okně **Přidat modul** vyberte **vložený skript**.</span><span class="sxs-lookup"><span data-stu-id="837b5-148">In the **Add Module** dialog box, select **Inline script**.</span></span>
1. <span data-ttu-id="837b5-149">V podokně vlastností vpravo v části **vložený skript** zadejte skript na straně klienta.</span><span class="sxs-lookup"><span data-stu-id="837b5-149">In the property pane on the right, under **Inline script**, enter your client-side script.</span></span> <span data-ttu-id="837b5-150">Poté nakonfigurujte další možnosti podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="837b5-150">Then configure other options as you require.</span></span>
1. <span data-ttu-id="837b5-151">Vyberte **Uložit** a potom vyberte **Dokončit úpravy**.</span><span class="sxs-lookup"><span data-stu-id="837b5-151">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="837b5-152">Zvolte **Publikovat**.</span><span class="sxs-lookup"><span data-stu-id="837b5-152">Select **Publish**.</span></span>

### <a name="add-an-external-script-directly-to-a-template"></a><span data-ttu-id="837b5-153">Přidání externího skriptu přímo do šablony</span><span class="sxs-lookup"><span data-stu-id="837b5-153">Add an external script directly to a template</span></span>

<span data-ttu-id="837b5-154">Chcete-li přidat externí skript přímo do šablony v rámci konfigurátoru webu, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="837b5-154">To add an external script directly to a template in site builder, follow these steps.</span></span>

1. <span data-ttu-id="837b5-155">Přejděte na **Šablony** a otevřete šablonu pro stránky, na které chcete přidat kód skriptu.</span><span class="sxs-lookup"><span data-stu-id="837b5-155">Go to **Templates**, and open the template for the pages that you want to add your script code to.</span></span>
1. <span data-ttu-id="837b5-156">V levém podokně rozbalte hierarchii šablon, aby se zobrazila pozice **Hlavička HTML**.</span><span class="sxs-lookup"><span data-stu-id="837b5-156">In the left pane, expand the template hierarchy to show the **HTML Head** slot.</span></span>
1. <span data-ttu-id="837b5-157">V pozici **Hlavička HTML** vyberte tlačítko se třemi tečkami (**...**) a poté vyberte možnost **Přidat modul**.</span><span class="sxs-lookup"><span data-stu-id="837b5-157">In the **HTML Head** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="837b5-158">V dialogovém okně **Přidat modul** vyberte **Externí skript**.</span><span class="sxs-lookup"><span data-stu-id="837b5-158">In the **Add Module** dialog box, select **External script**.</span></span>
1. <span data-ttu-id="837b5-159">V podokně vlastností vpravo v části **Zdroj skriptu** přidejte externí nebo relativní adresu URL pro externí zdroj skriptu.</span><span class="sxs-lookup"><span data-stu-id="837b5-159">In the property pane on the right, under **Script source**, add an external or relative URL for the external script source.</span></span> <span data-ttu-id="837b5-160">Poté nakonfigurujte další možnosti podle potřeby.</span><span class="sxs-lookup"><span data-stu-id="837b5-160">Then configure other options as you require.</span></span>
1. <span data-ttu-id="837b5-161">Vyberte **Uložit** a potom vyberte **Dokončit úpravy**.</span><span class="sxs-lookup"><span data-stu-id="837b5-161">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="837b5-162">Zvolte **Publikovat**.</span><span class="sxs-lookup"><span data-stu-id="837b5-162">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="837b5-163">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="837b5-163">Additional resources</span></span>

[<span data-ttu-id="837b5-164">Přidání loga</span><span class="sxs-lookup"><span data-stu-id="837b5-164">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="837b5-165">Volba motivu webu</span><span class="sxs-lookup"><span data-stu-id="837b5-165">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="837b5-166">Práce se soubory přepisu šablon CSS</span><span class="sxs-lookup"><span data-stu-id="837b5-166">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="837b5-167">Přidání ikony oblíbené položky</span><span class="sxs-lookup"><span data-stu-id="837b5-167">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="837b5-168">Přidání uvítací zprávy</span><span class="sxs-lookup"><span data-stu-id="837b5-168">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="837b5-169">Přidání oznámení o vlastnických právech</span><span class="sxs-lookup"><span data-stu-id="837b5-169">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="837b5-170">Přidání jazyků na web</span><span class="sxs-lookup"><span data-stu-id="837b5-170">Add languages to your site</span></span>](add-languages-to-site.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
