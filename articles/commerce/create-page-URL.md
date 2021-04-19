---
title: Vytvoření URL adresy stránky
description: V tomto tématu jsou popsány základní koncepce a postupy pro vytvoření adresy URL stránky na webu.
author: bicyclingfool
ms.date: 10/01/2019
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
ms.openlocfilehash: 98743d8948669f32d3c74e1915c7ed53db81141c
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795684"
---
# <a name="create-a-page-url"></a><span data-ttu-id="4f23b-103">Vytvoření URL adresy stránky</span><span class="sxs-lookup"><span data-stu-id="4f23b-103">Create a page URL</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4f23b-104">V tomto tématu jsou popsány základní koncepce a postupy pro vytvoření adresy URL stránky na webu.</span><span class="sxs-lookup"><span data-stu-id="4f23b-104">This topic covers the basic concepts and procedures for creating a page URL on your site.</span></span>

<span data-ttu-id="4f23b-105">Úplná nebo absolutní adresa URL, která odkazuje na stránku na webu, se skládá z různých částí.</span><span class="sxs-lookup"><span data-stu-id="4f23b-105">The full, or absolute, URL that points to a page on your site consists of distinct parts.</span></span> <span data-ttu-id="4f23b-106">Například adresa URL `https://www.contoso.com/en-us/contactus` má následující části:</span><span class="sxs-lookup"><span data-stu-id="4f23b-106">For example, the URL `https://www.contoso.com/en-us/contactus` has the following parts:</span></span>

- <span data-ttu-id="4f23b-107">`https://www.contoso.com` – Protokol HTTP a doména pracoviště.</span><span class="sxs-lookup"><span data-stu-id="4f23b-107">`https://www.contoso.com` – The HTTP protocol and the site's domain.</span></span>
- <span data-ttu-id="4f23b-108">`/en-us` – Cesta k jazyku webu.</span><span class="sxs-lookup"><span data-stu-id="4f23b-108">`/en-us` – The site's language path.</span></span>
- <span data-ttu-id="4f23b-109">`/contactus` – Relativní adresa URL stránky **Kontaktujte nás**.</span><span class="sxs-lookup"><span data-stu-id="4f23b-109">`/contactus` – The relative URL for the **Contact Us** page.</span></span> <span data-ttu-id="4f23b-110">Relativní adresa URL se také nazývá *slug* adresy URL.</span><span class="sxs-lookup"><span data-stu-id="4f23b-110">A relative URL is also known as a URL *slug*.</span></span>

<span data-ttu-id="4f23b-111">Doménu webu a volitelnou cestu k jazyku webu vytvoříte při zřízení webu.</span><span class="sxs-lookup"><span data-stu-id="4f23b-111">You establish your site's domain and optional language path when you set up the site.</span></span> <span data-ttu-id="4f23b-112">Na stránce online obchodů v nastaveních webu můžete přidat další domény a cesty k jazyku webu.</span><span class="sxs-lookup"><span data-stu-id="4f23b-112">You can add more domains and language paths to your site through the online stores page in the site's settings.</span></span>

<span data-ttu-id="4f23b-113">Slug adresy URL stránky existuje jako samostatná entita ve vývojovém prostředí webu.</span><span class="sxs-lookup"><span data-stu-id="4f23b-113">The URL slug for a page exists as a standalone entity in the site authoring environment.</span></span> <span data-ttu-id="4f23b-114">Adresa URL stránky se skládá ze dvou částí: názvu, který představuje slug adresy URL, a ukazatel na stránku buď na vašem webu, nebo na externím webu.</span><span class="sxs-lookup"><span data-stu-id="4f23b-114">A page URL consists of two parts: a name that represents the URL slug, and a pointer to a page on either your site or an external site.</span></span> <span data-ttu-id="4f23b-115">Adresu URL stránky lze také nakonfigurovat tak, aby přesměrovala na jinou stránku buď na vašem webu, nebo na externím webu.</span><span class="sxs-lookup"><span data-stu-id="4f23b-115">A page URL can also be configured to act as a redirect to another page on either your site or an external site.</span></span>

## <a name="create-a-page-url"></a><span data-ttu-id="4f23b-116">Vytvoření URL adresy stránky</span><span class="sxs-lookup"><span data-stu-id="4f23b-116">Create a page URL</span></span>

<span data-ttu-id="4f23b-117">Existují dva způsoby vytvoření adresy URL stránky:</span><span class="sxs-lookup"><span data-stu-id="4f23b-117">There are two ways to create page URLs:</span></span>

- <span data-ttu-id="4f23b-118">Automaticky, při vytvoření stránky</span><span class="sxs-lookup"><span data-stu-id="4f23b-118">Automatically, when you create a page</span></span>
- <span data-ttu-id="4f23b-119">Ručně, ze stránky **Adresy URL**</span><span class="sxs-lookup"><span data-stu-id="4f23b-119">Manually, from the **URLs** page</span></span>

### <a name="create-a-page-url-when-you-create-a-page"></a><span data-ttu-id="4f23b-120">Vytvoření adresy URL stránky při vytvoření stránky</span><span class="sxs-lookup"><span data-stu-id="4f23b-120">Create a page URL when you create a page</span></span>

<span data-ttu-id="4f23b-121">Pokud při vytváření nové stránky zadáte název do pole **Adresa URL**, bude na stránce **Adresy URL** automaticky vytvořena adresa URL stránky odkazující na tuto stránku.</span><span class="sxs-lookup"><span data-stu-id="4f23b-121">If you provide a name in the **URL** field when you create a new page, a page URL that points to that page is automatically created on the **URLs** page.</span></span> <span data-ttu-id="4f23b-122">Po publikování adresy URL a stránky, na kterou odkazuje, mohou uživatelé webu (vaši zákazníci) získat přístup ke stránce, která je přidružena k dané adrese URL.</span><span class="sxs-lookup"><span data-stu-id="4f23b-122">After you publish the URL and the page that it points to, site users (your customers) can access the page that is associated with the URL.</span></span>

> [!NOTE]
> <span data-ttu-id="4f23b-123">Pokud publikujete adresu URL, aniž byste publikovali stránku, na kterou odkazuje, zobrazí se uživatelům webu Chyba 404 při pokusu o přístup na stránku.</span><span class="sxs-lookup"><span data-stu-id="4f23b-123">If you publish a URL without publishing the page that it points to, site users receive a 404 error when they try to access the page.</span></span> <span data-ttu-id="4f23b-124">Pokud publikujete stránku bez publikování adresy URL, která na ni odkazuje, nelze k této stránce přistupovat pomocí adresy URL.</span><span class="sxs-lookup"><span data-stu-id="4f23b-124">If you publish a page without publishing the URL that points to it, the page can't be accessed by using a URL.</span></span>

### <a name="manually-create-a-page-url"></a><span data-ttu-id="4f23b-125">Ruční vytvoření adresy URL stránky</span><span class="sxs-lookup"><span data-stu-id="4f23b-125">Manually create a page URL</span></span>

<span data-ttu-id="4f23b-126">Když vytváříte novou stránku, nemusíte zadat její adresu URL.</span><span class="sxs-lookup"><span data-stu-id="4f23b-126">When you create new pages, you aren't required to specify a page URL.</span></span> <span data-ttu-id="4f23b-127">Pokud ponecháte pole adresy URL prázdné, bude stránka vytvořena v nepropojeném stavu.</span><span class="sxs-lookup"><span data-stu-id="4f23b-127">If you leave the URL field blank, the page is created in an unlinked state.</span></span> <span data-ttu-id="4f23b-128">V takovém případě nebudou mít zákazníci přístup na stránku, i když bude publikována.</span><span class="sxs-lookup"><span data-stu-id="4f23b-128">In this case, customers won't be able to access the page, even if it's published.</span></span> <span data-ttu-id="4f23b-129">Aby byla stránka přístupná, je nutné ručně vytvořit adresu URL a propojit ji se stránkou.</span><span class="sxs-lookup"><span data-stu-id="4f23b-129">To make the page accessible, you must manually create the URL and link it to the page.</span></span>

<span data-ttu-id="4f23b-130">Chcete-li vytvořit adresu URL stránky ručně, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="4f23b-130">To manually create the page URL for a page, follow these steps.</span></span>

1. <span data-ttu-id="4f23b-131">Na stránce **Adresy URL** zvolte **Nová**.</span><span class="sxs-lookup"><span data-stu-id="4f23b-131">On the **URLs** page, select **New**.</span></span>
1. <span data-ttu-id="4f23b-132">Vyberte stránku webu, které má být přiřazena adresa URL.</span><span class="sxs-lookup"><span data-stu-id="4f23b-132">Select the site page to associate with the URL.</span></span>
1. <span data-ttu-id="4f23b-133">Zadejte slug adresy URL a poté klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="4f23b-133">Enter the URL slug, and then select **OK**.</span></span>

<span data-ttu-id="4f23b-134">V tomto okamžiku se adresa URL nachází ve stavu konceptu.</span><span class="sxs-lookup"><span data-stu-id="4f23b-134">At this point, the URL is in a draft state.</span></span> <span data-ttu-id="4f23b-135">Musí být publikována před tím, než mohou uživatelé webu přistupovat k příslušné stránce.</span><span class="sxs-lookup"><span data-stu-id="4f23b-135">It must be published before site users can access the associated page.</span></span>

## <a name="update-a-page-url"></a><span data-ttu-id="4f23b-136">Aktualizace adresy URL stránky</span><span class="sxs-lookup"><span data-stu-id="4f23b-136">Update a page URL</span></span>

<span data-ttu-id="4f23b-137">Chcete-li aktualizovat cílovou stránku adresy URL, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="4f23b-137">To update the target page of a page URL, follow these steps.</span></span>

1. <span data-ttu-id="4f23b-138">Na stránce **Adresy URL** vyberte adresu URL, kterou chcete aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="4f23b-138">On the **URLs** page, select the URL to update.</span></span>
1. <span data-ttu-id="4f23b-139">V podokně vlastností vpravo vyberte tlačítko se třemi tečkami (**...**) vedle pole cílové stránky.</span><span class="sxs-lookup"><span data-stu-id="4f23b-139">In the property pane on the right, select the ellipsis button (**...**) next to the target page field.</span></span>
1. <span data-ttu-id="4f23b-140">V dialogovém okně vyberte jinou stránku a pak vyberte možnost **OK**.</span><span class="sxs-lookup"><span data-stu-id="4f23b-140">In the dialog box, select a different page, and then select **OK**.</span></span>
1. <span data-ttu-id="4f23b-141">Uložte a publikujte adresu URL.</span><span class="sxs-lookup"><span data-stu-id="4f23b-141">Save and publish the URL.</span></span>

## <a name="redirect-a-page-url"></a><span data-ttu-id="4f23b-142">Přesměrování adresy URL stránky</span><span class="sxs-lookup"><span data-stu-id="4f23b-142">Redirect a page URL</span></span>

<span data-ttu-id="4f23b-143">V některých případech můžete požadovat, aby vaši zákazníci při požadavku na konkrétní adresu URL zobrazili jinou stránku.</span><span class="sxs-lookup"><span data-stu-id="4f23b-143">Sometimes, you might want your customers to view a different page when they request a specific URL.</span></span> <span data-ttu-id="4f23b-144">V těchto případech je často nejlepší a nejjednodušší změnit stránku, na kterou adresa URL stránky odkazuje.</span><span class="sxs-lookup"><span data-stu-id="4f23b-144">In these cases, the best and easiest approach is often to change the page that the page URL points to.</span></span> <span data-ttu-id="4f23b-145">Je však možné, že máte legitimní důvody k přesměrování požadavků na adresu URL na jinou adresu URL pomocí přesměrování HTTP 301 nebo 3023.</span><span class="sxs-lookup"><span data-stu-id="4f23b-145">However, you might have legitimate reasons for using HTTP 301 or 3023 redirects to redirect requests for a URL to a different URL.</span></span>

<span data-ttu-id="4f23b-146">Chcete-li přesměrovat adresu URL na jinou adresu URL, postupujte podle následujících kroků.</span><span class="sxs-lookup"><span data-stu-id="4f23b-146">To redirect a URL to a different URL, follow these steps.</span></span>

1. <span data-ttu-id="4f23b-147">Na stránce **Adresy URL** vyberte adresu URL, kterou chcete aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="4f23b-147">On the **URLs** page, select the URL to update.</span></span>
1. <span data-ttu-id="4f23b-148">V podokně vlastností vpravo vyberte vlastnost **Přesměrovat**.</span><span class="sxs-lookup"><span data-stu-id="4f23b-148">In the property pane on the right, select **Redirect**.</span></span>
1. <span data-ttu-id="4f23b-149">Vyberte cíl přesměrování:</span><span class="sxs-lookup"><span data-stu-id="4f23b-149">Select a destination for the redirect:</span></span>

    - <span data-ttu-id="4f23b-150">Chcete-li odkázat na jinou stránku na webu, **vyberte volbu** Interní adresa URL, vyberte tlačítkose třemi tečkami (**...**) a vyberte adresu URL, na kterou chcete přesměrovat.</span><span class="sxs-lookup"><span data-stu-id="4f23b-150">To point to another page on your site, select **Internal URL**, select the ellipsis button (**...**), and then select the URL to redirect to.</span></span>
    - <span data-ttu-id="4f23b-151">Chcete-li odkázat na stránku na externím webu, vyberte volbu **Externí adresa URL** a poté zadejte úplnou adresu URL pro tuto stránku.</span><span class="sxs-lookup"><span data-stu-id="4f23b-151">To point to a page on an external site, select **External URL**, and then enter the full URL for that page.</span></span> <span data-ttu-id="4f23b-152">Nezapomeňte zadat i protokol.</span><span class="sxs-lookup"><span data-stu-id="4f23b-152">Be sure to include the protocol.</span></span> <span data-ttu-id="4f23b-153">Zadejte například `https://domain.com/new/page`.</span><span class="sxs-lookup"><span data-stu-id="4f23b-153">For example, enter `https://domain.com/new/page`.</span></span> <span data-ttu-id="4f23b-154">Pokud již adresa URL přesměrovává na interní adresu URL, je nutné před zadáním externí adresy URL vybrat možnost **Vymazat výběr**.</span><span class="sxs-lookup"><span data-stu-id="4f23b-154">If the URL already redirects to an internal URL, you must select **Clear selection** before you can enter an external URL.</span></span>

1. <span data-ttu-id="4f23b-155">Vyberte typ přesměrování:</span><span class="sxs-lookup"><span data-stu-id="4f23b-155">Select a redirect type:</span></span>

    - <span data-ttu-id="4f23b-156">**Trvalé přesměrování (301)** – Tuto možnost vyberte, pokud víte, že se váš obsah trvale přesouvá a neobnoví se na předchozí adresu URL.</span><span class="sxs-lookup"><span data-stu-id="4f23b-156">**Permanent redirect (301)** – Select this option when you know that your content is moving permanently and won't revert to its previous URL.</span></span> <span data-ttu-id="4f23b-157">Vyhledávací weby přiřadí hodnotu SEO (Search Engine Optimization) adresy URL pro přesměrování adrese URL, na kterou je přesměrovávána a aktualizuje jejich záznam, aby se zobrazila nová adresa URL.</span><span class="sxs-lookup"><span data-stu-id="4f23b-157">Search engines will assign the search engine optimization (SEO) value of the redirecting URL to the URL that is being redirected to and update their record to show the new URL.</span></span> 
    - <span data-ttu-id="4f23b-158">**Dočasné přesměrování (302)** – Tuto možnost vyberte, chcete-li přesměrovat provoz bez aktualizace vyhledávacích webů.</span><span class="sxs-lookup"><span data-stu-id="4f23b-158">**Temporary redirect (302)** – Select this option to redirect traffic without updating search engines.</span></span> <span data-ttu-id="4f23b-159">Tento přístup se obvykle používá v případě, že se obsah brzy vrátí na předchozí adresu URL.</span><span class="sxs-lookup"><span data-stu-id="4f23b-159">This approach is typically used if the content will soon revert to its previous URL.</span></span>

1. <span data-ttu-id="4f23b-160">Až budete připraveni provést přesměrování, uložte a publikujte adresu URL.</span><span class="sxs-lookup"><span data-stu-id="4f23b-160">When you're ready to implement the redirect, save and publish the URL.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4f23b-161">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="4f23b-161">Additional resources</span></span>

[<span data-ttu-id="4f23b-162">Přizpůsobení navigace na webu</span><span class="sxs-lookup"><span data-stu-id="4f23b-162">Customize site navigation</span></span>](customize-site-navigation.md)

[<span data-ttu-id="4f23b-163">Přidání nové webové stránky</span><span class="sxs-lookup"><span data-stu-id="4f23b-163">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="4f23b-164">Konfigurace názvu domény</span><span class="sxs-lookup"><span data-stu-id="4f23b-164">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="4f23b-165">Přidání jazyků na web</span><span class="sxs-lookup"><span data-stu-id="4f23b-165">Add languages to your site</span></span>](add-languages-to-site.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
