---
title: Vytvoření URL adresy stránky
description: V tomto tématu jsou popsány základní koncepce a postupy pro vytvoření adresy URL stránky na webu.
author: bicyclingfool
manager: annbe
ms.date: 10/01/2019
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
ms.openlocfilehash: 588cbedb077fab0663d3d62fc4a8b8ed915635b3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410740"
---
# <a name="create-a-page-url"></a><span data-ttu-id="1192a-103">Vytvoření URL adresy stránky</span><span class="sxs-lookup"><span data-stu-id="1192a-103">Create a page URL</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="1192a-104">V tomto tématu jsou popsány základní koncepce a postupy pro vytvoření adresy URL stránky na webu.</span><span class="sxs-lookup"><span data-stu-id="1192a-104">This topic covers the basic concepts and procedures for creating a page URL on your site.</span></span>

## <a name="overview"></a><span data-ttu-id="1192a-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="1192a-105">Overview</span></span>

<span data-ttu-id="1192a-106">Úplná nebo absolutní adresa URL, která odkazuje na stránku na webu, se skládá z různých částí.</span><span class="sxs-lookup"><span data-stu-id="1192a-106">The full, or absolute, URL that points to a page on your site consists of distinct parts.</span></span> <span data-ttu-id="1192a-107">Například adresa URL `https://www.contoso.com/en-us/contactus` má následující části:</span><span class="sxs-lookup"><span data-stu-id="1192a-107">For example, the URL `https://www.contoso.com/en-us/contactus` has the following parts:</span></span>

- <span data-ttu-id="1192a-108">`https://www.contoso.com` – Protokol HTTP a doména pracoviště.</span><span class="sxs-lookup"><span data-stu-id="1192a-108">`https://www.contoso.com` – The HTTP protocol and the site's domain.</span></span>
- <span data-ttu-id="1192a-109">`/en-us` – Cesta k jazyku webu.</span><span class="sxs-lookup"><span data-stu-id="1192a-109">`/en-us` – The site's language path.</span></span>
- <span data-ttu-id="1192a-110">`/contactus` – Relativní adresa URL stránky **Kontaktujte nás**.</span><span class="sxs-lookup"><span data-stu-id="1192a-110">`/contactus` – The relative URL for the **Contact Us** page.</span></span> <span data-ttu-id="1192a-111">Relativní adresa URL se také nazývá *slug* adresy URL.</span><span class="sxs-lookup"><span data-stu-id="1192a-111">A relative URL is also known as a URL *slug*.</span></span>

<span data-ttu-id="1192a-112">Doménu webu a volitelnou cestu k jazyku webu vytvoříte při zřízení webu.</span><span class="sxs-lookup"><span data-stu-id="1192a-112">You establish your site's domain and optional language path when you set up the site.</span></span> <span data-ttu-id="1192a-113">Na stránce online obchodů v nastaveních webu můžete přidat další domény a cesty k jazyku webu.</span><span class="sxs-lookup"><span data-stu-id="1192a-113">You can add more domains and language paths to your site through the online stores page in the site's settings.</span></span>

<span data-ttu-id="1192a-114">Slug adresy URL stránky existuje jako samostatná entita ve vývojovém prostředí webu.</span><span class="sxs-lookup"><span data-stu-id="1192a-114">The URL slug for a page exists as a standalone entity in the site authoring environment.</span></span> <span data-ttu-id="1192a-115">Adresa URL stránky se skládá ze dvou částí: názvu, který představuje slug adresy URL, a ukazatel na stránku buď na vašem webu, nebo na externím webu.</span><span class="sxs-lookup"><span data-stu-id="1192a-115">A page URL consists of two parts: a name that represents the URL slug, and a pointer to a page on either your site or an external site.</span></span> <span data-ttu-id="1192a-116">Adresu URL stránky lze také nakonfigurovat tak, aby přesměrovala na jinou stránku buď na vašem webu, nebo na externím webu.</span><span class="sxs-lookup"><span data-stu-id="1192a-116">A page URL can also be configured to act as a redirect to another page on either your site or an external site.</span></span>

## <a name="create-a-page-url"></a><span data-ttu-id="1192a-117">Vytvoření URL adresy stránky</span><span class="sxs-lookup"><span data-stu-id="1192a-117">Create a page URL</span></span>

<span data-ttu-id="1192a-118">Existují dva způsoby vytvoření adresy URL stránky:</span><span class="sxs-lookup"><span data-stu-id="1192a-118">There are two ways to create page URLs:</span></span>

- <span data-ttu-id="1192a-119">Automaticky, při vytvoření stránky</span><span class="sxs-lookup"><span data-stu-id="1192a-119">Automatically, when you create a page</span></span>
- <span data-ttu-id="1192a-120">Ručně, ze stránky **Adresy URL**</span><span class="sxs-lookup"><span data-stu-id="1192a-120">Manually, from the **URLs** page</span></span>

### <a name="create-a-page-url-when-you-create-a-page"></a><span data-ttu-id="1192a-121">Vytvoření adresy URL stránky při vytvoření stránky</span><span class="sxs-lookup"><span data-stu-id="1192a-121">Create a page URL when you create a page</span></span>

<span data-ttu-id="1192a-122">Pokud při vytváření nové stránky zadáte název do pole **Adresa URL**, bude na stránce **Adresy URL** automaticky vytvořena adresa URL stránky odkazující na tuto stránku.</span><span class="sxs-lookup"><span data-stu-id="1192a-122">If you provide a name in the **URL** field when you create a new page, a page URL that points to that page is automatically created on the **URLs** page.</span></span> <span data-ttu-id="1192a-123">Po publikování adresy URL a stránky, na kterou odkazuje, mohou uživatelé webu (vaši zákazníci) získat přístup ke stránce, která je přidružena k dané adrese URL.</span><span class="sxs-lookup"><span data-stu-id="1192a-123">After you publish the URL and the page that it points to, site users (your customers) can access the page that is associated with the URL.</span></span>

> [!NOTE]
> <span data-ttu-id="1192a-124">Pokud publikujete adresu URL, aniž byste publikovali stránku, na kterou odkazuje, zobrazí se uživatelům webu Chyba 404 při pokusu o přístup na stránku.</span><span class="sxs-lookup"><span data-stu-id="1192a-124">If you publish a URL without publishing the page that it points to, site users receive a 404 error when they try to access the page.</span></span> <span data-ttu-id="1192a-125">Pokud publikujete stránku bez publikování adresy URL, která na ni odkazuje, nelze k této stránce přistupovat pomocí adresy URL.</span><span class="sxs-lookup"><span data-stu-id="1192a-125">If you publish a page without publishing the URL that points to it, the page can't be accessed by using a URL.</span></span>

### <a name="manually-create-a-page-url"></a><span data-ttu-id="1192a-126">Ruční vytvoření adresy URL stránky</span><span class="sxs-lookup"><span data-stu-id="1192a-126">Manually create a page URL</span></span>

<span data-ttu-id="1192a-127">Když vytváříte novou stránku, nemusíte zadat její adresu URL.</span><span class="sxs-lookup"><span data-stu-id="1192a-127">When you create new pages, you aren't required to specify a page URL.</span></span> <span data-ttu-id="1192a-128">Pokud ponecháte pole adresy URL prázdné, bude stránka vytvořena v nepropojeném stavu.</span><span class="sxs-lookup"><span data-stu-id="1192a-128">If you leave the URL field blank, the page is created in an unlinked state.</span></span> <span data-ttu-id="1192a-129">V takovém případě nebudou mít zákazníci přístup na stránku, i když bude publikována.</span><span class="sxs-lookup"><span data-stu-id="1192a-129">In this case, customers won't be able to access the page, even if it's published.</span></span> <span data-ttu-id="1192a-130">Aby byla stránka přístupná, je nutné ručně vytvořit adresu URL a propojit ji se stránkou.</span><span class="sxs-lookup"><span data-stu-id="1192a-130">To make the page accessible, you must manually create the URL and link it to the page.</span></span>

<span data-ttu-id="1192a-131">Chcete-li vytvořit adresu URL stránky ručně, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="1192a-131">To manually create the page URL for a page, follow these steps.</span></span>

1. <span data-ttu-id="1192a-132">Na stránce **Adresy URL** zvolte **Nová**.</span><span class="sxs-lookup"><span data-stu-id="1192a-132">On the **URLs** page, select **New**.</span></span>
1. <span data-ttu-id="1192a-133">Vyberte stránku webu, které má být přiřazena adresa URL.</span><span class="sxs-lookup"><span data-stu-id="1192a-133">Select the site page to associate with the URL.</span></span>
1. <span data-ttu-id="1192a-134">Zadejte slug adresy URL a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="1192a-134">Enter the URL slug, and then select **OK**.</span></span>

<span data-ttu-id="1192a-135">V tomto okamžiku se adresa URL nachází ve stavu konceptu.</span><span class="sxs-lookup"><span data-stu-id="1192a-135">At this point, the URL is in a draft state.</span></span> <span data-ttu-id="1192a-136">Musí být publikována před tím, než mohou uživatelé webu přistupovat k příslušné stránce.</span><span class="sxs-lookup"><span data-stu-id="1192a-136">It must be published before site users can access the associated page.</span></span>

## <a name="update-a-page-url"></a><span data-ttu-id="1192a-137">Aktualizace adresy URL stránky</span><span class="sxs-lookup"><span data-stu-id="1192a-137">Update a page URL</span></span>

<span data-ttu-id="1192a-138">Chcete-li aktualizovat cílovou stránku adresy URL, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="1192a-138">To update the target page of a page URL, follow these steps.</span></span>

1. <span data-ttu-id="1192a-139">Na stránce **Adresy URL** vyberte adresu URL, kterou chcete aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="1192a-139">On the **URLs** page, select the URL to update.</span></span>
1. <span data-ttu-id="1192a-140">V podokně vlastností vpravo vyberte tlačítko se třemi tečkami (**...**) vedle pole cílové stránky.</span><span class="sxs-lookup"><span data-stu-id="1192a-140">In the property pane on the right, select the ellipsis button (**...**) next to the target page field.</span></span>
1. <span data-ttu-id="1192a-141">V dialogovém okně vyberte jinou stránku a pak vyberte možnost **OK**.</span><span class="sxs-lookup"><span data-stu-id="1192a-141">In the dialog box, select a different page, and then select **OK**.</span></span>
1. <span data-ttu-id="1192a-142">Uložte a publikujte adresu URL.</span><span class="sxs-lookup"><span data-stu-id="1192a-142">Save and publish the URL.</span></span>

## <a name="redirect-a-page-url"></a><span data-ttu-id="1192a-143">Přesměrování adresy URL stránky</span><span class="sxs-lookup"><span data-stu-id="1192a-143">Redirect a page URL</span></span>

<span data-ttu-id="1192a-144">V některých případech můžete požadovat, aby vaši zákazníci při požadavku na konkrétní adresu URL zobrazili jinou stránku.</span><span class="sxs-lookup"><span data-stu-id="1192a-144">Sometimes, you might want your customers to view a different page when they request a specific URL.</span></span> <span data-ttu-id="1192a-145">V těchto případech je často nejlepší a nejjednodušší změnit stránku, na kterou adresa URL stránky odkazuje.</span><span class="sxs-lookup"><span data-stu-id="1192a-145">In these cases, the best and easiest approach is often to change the page that the page URL points to.</span></span> <span data-ttu-id="1192a-146">Je však možné, že máte legitimní důvody k přesměrování požadavků na adresu URL na jinou adresu URL pomocí přesměrování HTTP 301 nebo 3023.</span><span class="sxs-lookup"><span data-stu-id="1192a-146">However, you might have legitimate reasons for using HTTP 301 or 3023 redirects to redirect requests for a URL to a different URL.</span></span>

<span data-ttu-id="1192a-147">Chcete-li přesměrovat adresu URL na jinou adresu URL, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="1192a-147">To redirect a URL to a different URL, follow these steps.</span></span>

1. <span data-ttu-id="1192a-148">Na stránce **Adresy URL** vyberte adresu URL, kterou chcete aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="1192a-148">On the **URLs** page, select the URL to update.</span></span>
1. <span data-ttu-id="1192a-149">V podokně vlastností vpravo vyberte vlastnost **Přesměrovat**.</span><span class="sxs-lookup"><span data-stu-id="1192a-149">In the property pane on the right, select **Redirect**.</span></span>
1. <span data-ttu-id="1192a-150">Vyberte cíl přesměrování:</span><span class="sxs-lookup"><span data-stu-id="1192a-150">Select a destination for the redirect:</span></span>

    - <span data-ttu-id="1192a-151">Chcete-li odkázat na jinou stránku na webu, **vyberte volbu** Interní adresa URL, vyberte tlačítkose třemi tečkami (**...**) a vyberte adresu URL, na kterou chcete přesměrovat.</span><span class="sxs-lookup"><span data-stu-id="1192a-151">To point to another page on your site, select **Internal URL**, select the ellipsis button (**...**), and then select the URL to redirect to.</span></span>
    - <span data-ttu-id="1192a-152">Chcete-li odkázat na stránku na externím webu, vyberte volbu **Externí adresa URL** a poté zadejte úplnou adresu URL pro tuto stránku.</span><span class="sxs-lookup"><span data-stu-id="1192a-152">To point to a page on an external site, select **External URL**, and then enter the full URL for that page.</span></span> <span data-ttu-id="1192a-153">Nezapomeňte zadat i protokol.</span><span class="sxs-lookup"><span data-stu-id="1192a-153">Be sure to include the protocol.</span></span> <span data-ttu-id="1192a-154">Zadejte například `https://domain.com/new/page`.</span><span class="sxs-lookup"><span data-stu-id="1192a-154">For example, enter `https://domain.com/new/page`.</span></span> <span data-ttu-id="1192a-155">Pokud již adresa URL přesměrovává na interní adresu URL, je nutné před zadáním externí adresy URL vybrat možnost **Vymazat výběr**.</span><span class="sxs-lookup"><span data-stu-id="1192a-155">If the URL already redirects to an internal URL, you must select **Clear selection** before you can enter an external URL.</span></span>

1. <span data-ttu-id="1192a-156">Vyberte typ přesměrování:</span><span class="sxs-lookup"><span data-stu-id="1192a-156">Select a redirect type:</span></span>

    - <span data-ttu-id="1192a-157">**Trvalé přesměrování (301)** – Tuto možnost vyberte, pokud víte, že se váš obsah trvale přesouvá a neobnoví se na předchozí adresu URL.</span><span class="sxs-lookup"><span data-stu-id="1192a-157">**Permanent redirect (301)** – Select this option when you know that your content is moving permanently and won't revert to its previous URL.</span></span> <span data-ttu-id="1192a-158">Vyhledávací weby přiřadí hodnotu SEO (Search Engine Optimization) adresy URL pro přesměrování adrese URL, na kterou je přesměrovávána a aktualizuje jejich záznam, aby se zobrazila nová adresa URL.</span><span class="sxs-lookup"><span data-stu-id="1192a-158">Search engines will assign the search engine optimization (SEO) value of the redirecting URL to the URL that is being redirected to and update their record to show the new URL.</span></span> 
    - <span data-ttu-id="1192a-159">**Dočasné přesměrování (302)** – Tuto možnost vyberte, chcete-li přesměrovat provoz bez aktualizace vyhledávacích webů.</span><span class="sxs-lookup"><span data-stu-id="1192a-159">**Temporary redirect (302)** – Select this option to redirect traffic without updating search engines.</span></span> <span data-ttu-id="1192a-160">Tento přístup se obvykle používá v případě, že se obsah brzy vrátí na předchozí adresu URL.</span><span class="sxs-lookup"><span data-stu-id="1192a-160">This approach is typically used if the content will soon revert to its previous URL.</span></span>

1. <span data-ttu-id="1192a-161">Až budete připraveni provést přesměrování, uložte a publikujte adresu URL.</span><span class="sxs-lookup"><span data-stu-id="1192a-161">When you're ready to implement the redirect, save and publish the URL.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1192a-162">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="1192a-162">Additional resources</span></span>

[<span data-ttu-id="1192a-163">Přizpůsobení navigace na webu</span><span class="sxs-lookup"><span data-stu-id="1192a-163">Customize site navigation</span></span>](customize-site-navigation.md)

[<span data-ttu-id="1192a-164">Přidání nové webové stránky</span><span class="sxs-lookup"><span data-stu-id="1192a-164">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="1192a-165">Konfigurace názvu domény</span><span class="sxs-lookup"><span data-stu-id="1192a-165">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="1192a-166">Přidání jazyků na web</span><span class="sxs-lookup"><span data-stu-id="1192a-166">Add languages to your site</span></span>](add-languages-to-site.md)
