---
title: Odeslání a obsluha statických souborů
description: Tohle téma popisuje, jak odeslat statický soubor do konfigurátoru webů Microsoft Dynamics 365 Commerce a jak vytvořit vlastní adresu URL a název souboru, který lze použít k vyžádání tohoto souboru.
author: StuHarg
manager: annbe
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 1d709d99737ad05af1fb19d9f3ef7b87a8db80d3
ms.sourcegitcommit: da17648c296b22d517eadb2f71c7803672e5648d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/19/2021
ms.locfileid: "5031813"
---
# <a name="upload-and-serve-static-files"></a><span data-ttu-id="ddb5b-103">Odeslání a obsluha statických souborů</span><span class="sxs-lookup"><span data-stu-id="ddb5b-103">Upload and serve static files</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ddb5b-104">Tohle téma popisuje, jak odeslat statický soubor do konfigurátoru webů Microsoft Dynamics 365 Commerce a jak vytvořit vlastní adresu URL a název souboru, který lze použít k vyžádání tohoto souboru.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-104">This topic describes how to upload a static file into Microsoft Dynamics 365 Commerce site builder, and how to create a custom URL and file name that can be used to request that file.</span></span>

<span data-ttu-id="ddb5b-105">Některé konektory jiných výrobců vyžadují, aby byl soubor hostován a obsluhován z webu elektronického obchodování.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-105">Some third-party connectors require that a file be hosted and served from the e-commerce site.</span></span> <span data-ttu-id="ddb5b-106">Tyto konektory očekávají, že soubor bude vrácen požadavky na konkrétní cestu URL zpětného volání a název souboru.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-106">These connectors expect that the file will be returned by requests to a specific callback URL path and file name.</span></span> <span data-ttu-id="ddb5b-107">Toto téma proto vysvětluje, jak nahrát a zobrazit statický soubor, který má na webu uživatelem definovanou adresu URL a název souboru na webu elektronického obchodování Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-107">Therefore, this topic explains how to upload and serve a static file that has a user-definable URL and file name on a Dynamics 365 Commerce e-commerce site.</span></span>

## <a name="create-a-site-url-that-returns-a-static-file"></a><span data-ttu-id="ddb5b-108">Vytvoření adresy URL webu, která vrací statický soubor</span><span class="sxs-lookup"><span data-stu-id="ddb5b-108">Create a site URL that returns a static file</span></span>

<span data-ttu-id="ddb5b-109">Chcete-li vytvořit adresu URL webu, která vrací statický soubor v konfigurátoru webů Commerce, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-109">To create a site URL that returns a static file in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="ddb5b-110">Přejděte do knihovny médií webu a nahrajte soubor, který by měl být obsloužen žádostmi na adresu URL, kterou definujete.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-110">Go to your site's Media library, and upload the file that should be served by requests to the URL that you will define.</span></span> <span data-ttu-id="ddb5b-111">Pokud jste již soubor nahráli, můžete tento krok přeskočit.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-111">If you've already uploaded the file, you can skip this step.</span></span>
1. <span data-ttu-id="ddb5b-112">Jděte na **Adresy URL** pro váš web.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-112">Go to **URLs** for your site.</span></span>
1. <span data-ttu-id="ddb5b-113">Zvolte **Nový \> Nová adresa URL**.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-113">Select **New \> New URL**.</span></span>
1. <span data-ttu-id="ddb5b-114">V dialogovém okně **Nová adresa URL** vyberte **Prostředek knihovny médií**.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-114">In the **New URL** dialog box, select **Media library asset**.</span></span>
1. <span data-ttu-id="ddb5b-115">Do pole **Cesta URL** zadejte cestu URL.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-115">In the **URL path** field, enter the URL path.</span></span> <span data-ttu-id="ddb5b-116">Do cesty zahrňte název souboru.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-116">Include the file name in the path.</span></span>
1. <span data-ttu-id="ddb5b-117">Zvolte **Další**.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-117">Select **Next**.</span></span> <span data-ttu-id="ddb5b-118">Otevře se knihovna médií a zobrazí se všechny prostředky médií typu **dokument**, které byly nahrány.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-118">The Media library is opened and shows all media assets of the **document** type that have been uploaded.</span></span>
1. <span data-ttu-id="ddb5b-119">Vyberte soubor, který má být obsloužen požadavky na adresu URL, kterou jste definovali v kroku 5.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-119">Select the file that should be served for requests to the URL that you defined in step 5.</span></span>
1. <span data-ttu-id="ddb5b-120">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-120">Select **Save**.</span></span>

<span data-ttu-id="ddb5b-121">V tomto okamžiku se vytvořená adresa URL nachází ve stavu konceptu.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-121">At this point, the URL that you created is in a draft state.</span></span> <span data-ttu-id="ddb5b-122">Soubor, na který adresa URL odkazuje, nebude vrácen, dokud adresu URL nepublikujete.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-122">The file that the URL points to won't be returned until you publish the URL.</span></span> <span data-ttu-id="ddb5b-123">Před publikováním adresy URL můžete ověřit, zda vrací správná data.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-123">Before you publish the URL, you can validate that it returns the correct data.</span></span>

## <a name="validate-and-publish-a-url"></a><span data-ttu-id="ddb5b-124">Ověření a publikování adresy URL</span><span class="sxs-lookup"><span data-stu-id="ddb5b-124">Validate and publish a URL</span></span>

<span data-ttu-id="ddb5b-125">Chcete-li ověřit adresu URL před jejím publikování, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-125">To validate an URL before you publish it, follow these steps.</span></span>

1. <span data-ttu-id="ddb5b-126">Jděte na **Adresy URL** pro váš web a vyberte adresu URL, jejíž náhled chcete zobrazit.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-126">Go to **URLs** for your site, and select the URL to preview.</span></span>
2. <span data-ttu-id="ddb5b-127">V podokně vlastností vpravo pod tlačítkem **Upravit** vyberte správný odkaz na adresu URL.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-127">In the properties pane on the right, below the **Edit** button, select the correct URL link.</span></span> <span data-ttu-id="ddb5b-128">Otevře se nové okno prohlížeče a měla by se zobrazit chyba 404.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-128">A new browser window is opened, and you should receive a 404 error.</span></span>
3. <span data-ttu-id="ddb5b-129">Připojte řetězec dotazu **?preview=inprogress** k adrese URL (například `https://yoursite.com/callback.html?preview=inprogress`) a znovu načtěte stránku.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-129">Append the **?preview=inprogress** query string to the URL (for example, `https://yoursite.com/callback.html?preview=inprogress`), and reload the page.</span></span> <span data-ttu-id="ddb5b-130">Soubor, který jste nahráli do knihovny médií, by měl být vrácen v odpovědi.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-130">The file that you uploaded to the Media library should be returned in the response.</span></span>

<span data-ttu-id="ddb5b-131">Po ověření adresy URL ji můžete publikovat.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-131">After you've validated the URL, you can publish it.</span></span>

1. <span data-ttu-id="ddb5b-132">Jděte na **Adresy URL** pro váš web a vyberte adresu URL.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-132">Go to **URLs** for your site, and select the URL.</span></span>
2. <span data-ttu-id="ddb5b-133">Na příkazovém řádku vyberte možnost **Publikovat**.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-133">Select **Publish** on the command bar.</span></span>

## <a name="update-the-file-that-a-url-points-to"></a><span data-ttu-id="ddb5b-134">Aktualizace souboru, na který odkazuje adresa URL</span><span class="sxs-lookup"><span data-stu-id="ddb5b-134">Update the file that a URL points to</span></span>

<span data-ttu-id="ddb5b-135">Po publikování adresy URL ji můžete aktualizovat tak, aby odkazovala na jiný soubor.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-135">After a URL is published, you can update it so that it points to a different file.</span></span> <span data-ttu-id="ddb5b-136">Alternativně můžete adresu URL aktualizovat tak, aby odkazovala na jiný typ prostředku, jak je popsáno v následující části.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-136">Alternatively, you can update the URL so that it points to a different the type of resource, as described in the next section.</span></span> <span data-ttu-id="ddb5b-137">Můžete například nasměrovat adresu URL na interní stránku nebo přesměrování.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-137">For example, you can point the URL to an internal page or a redirect.</span></span>

<span data-ttu-id="ddb5b-138">Chcete-li aktualizovat soubor, na který odkazuje adresa URL, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-138">To update the file that a URL points to, follow these steps.</span></span>

1. <span data-ttu-id="ddb5b-139">Jděte na **Adresy URL** pro váš web a vyberte adresu URL, kterou chcete aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-139">Go to **URLs** for your site, and select the URL to update.</span></span>
1. <span data-ttu-id="ddb5b-140">V podokně vlastností vpravo vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-140">In the properties pane on the right, select **Edit**.</span></span>
1. <span data-ttu-id="ddb5b-141">V části **Přiřazení adresy URL** vyberte pole **Krok 2** a poté vyberte nový dokument z knihovny médií.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-141">Under **URL assignment**, select the **Step 2** box, and then select a new document from the Media library.</span></span>
1. <span data-ttu-id="ddb5b-142">Zvolte **Použít**.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-142">Select **Apply**.</span></span>

## <a name="update-the-asset-type-that-a-url-points-to"></a><span data-ttu-id="ddb5b-143">Aktualizace typu prostředku, na který odkazuje adresa URL</span><span class="sxs-lookup"><span data-stu-id="ddb5b-143">Update the asset type that a URL points to</span></span>

<span data-ttu-id="ddb5b-144">Můžete také aktualizovat adresu URL tak, aby odkazovala na jiný typ prostředku, například na interní stránku nebo přesměrování.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-144">You can also update a URL so that it points to a different type of asset (resource), such as an internal page or a redirect.</span></span>

<span data-ttu-id="ddb5b-145">Chcete-li aktualizovat typ prostředku, na který odkazuje adresa URL, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-145">To update the asset type that a URL points to, follow these steps.</span></span>

1. <span data-ttu-id="ddb5b-146">Jděte na **Adresy URL** pro váš web a vyberte adresu URL, kterou chcete aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-146">Go to **URLs** for your site, and select the URL to update.</span></span>
1. <span data-ttu-id="ddb5b-147">V podokně vlastností vpravo vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-147">In the properties pane on the right, select **Edit**.</span></span>
1. <span data-ttu-id="ddb5b-148">V části **Přiřazení adresy URL** v poli **Krok 1**, vyberte jiný typ prostředku.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-148">Under **URL assignment**, under **Step 1**, select a different asset type.</span></span>
1. <span data-ttu-id="ddb5b-149">Vyberte pole **Krok 2** a poté vyberte nový prostředek.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-149">Select the **Step 2** box, and then select the new asset.</span></span>
1. <span data-ttu-id="ddb5b-150">Zvolte **Použít**.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-150">Select **Apply**.</span></span>

## <a name="change-the-url-path"></a><span data-ttu-id="ddb5b-151">Změna cesty URL</span><span class="sxs-lookup"><span data-stu-id="ddb5b-151">Change the URL path</span></span>

<span data-ttu-id="ddb5b-152">Po vytvoření adresy URL nelze změnit její cestu.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-152">After a URL is created, its path can't be changed.</span></span> <span data-ttu-id="ddb5b-153">Pokud musíte změnit cestu URL, která obsluhuje soubor nebo jiný typ prostředku, musíte vytvořit novou adresu URL, namapovat ji na existující soubor nebo jiný prostředek a poté zrušit publikování a odstranit starou adresu URL.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-153">If you must change the URL path that serves a file or any other type of resource, you have to create a new URL, map it to the existing file or other resource, and then unpublish and delete the old URL.</span></span>

<span data-ttu-id="ddb5b-154">K úpravě cesty URL postupujte následovně.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-154">To change the URL path, follow these steps.</span></span>

1. <span data-ttu-id="ddb5b-155">Chcete-li vytvořit novou adresu URL a namapovat ji na existující soubor nebo jiný prostředek, postupujte podle pokynů v části [Vytvoření adresy URL webu, která vrací statický soubor](#create-a-site-url-that-returns-a-static-file) dříve v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-155">To create a new URL and map it to the existing file or another resource, follow the instructions in the [Create a site URL that returns a static file](#create-a-site-url-that-returns-a-static-file) section earlier in this topic.</span></span>
1. <span data-ttu-id="ddb5b-156">Vyberte novou adresu URL a vyberte **Publikovat** na panelu příkazů.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-156">Select the new URL, and select **Publish** on the command bar.</span></span> <span data-ttu-id="ddb5b-157">Nová adresa URL je publikována.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-157">The new URL is published.</span></span>
1. <span data-ttu-id="ddb5b-158">Chcete-li zrušit publikování staré adresy URL, vyberte ji a poté vyberte **Zrušit publikování** na panelu příkazů.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-158">To unpublish the old URL, select it, and then select **Unpublish** on the command bar.</span></span> <span data-ttu-id="ddb5b-159">Jestli chcete, můžete nyní odstranit starou adresu URL.</span><span class="sxs-lookup"><span data-stu-id="ddb5b-159">You can now delete the old URL if you want.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ddb5b-160">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="ddb5b-160">Additional resources</span></span>

[<span data-ttu-id="ddb5b-161">Přehled správy digitálních aktiv</span><span class="sxs-lookup"><span data-stu-id="ddb5b-161">Digital asset management overview</span></span>](dam-overview.md)

[<span data-ttu-id="ddb5b-162">Odeslání obrázků</span><span class="sxs-lookup"><span data-stu-id="ddb5b-162">Upload images</span></span>](dam-upload-images.md)

[<span data-ttu-id="ddb5b-163">Odeslat videa</span><span class="sxs-lookup"><span data-stu-id="ddb5b-163">Upload videos</span></span>](dam-upload-video.md)

[<span data-ttu-id="ddb5b-164">Odeslání souborů jiných než obrázky a videa</span><span class="sxs-lookup"><span data-stu-id="ddb5b-164">Upload files other than images and videos</span></span>](dam-upload-files.md)

[<span data-ttu-id="ddb5b-165">Oříznutí obrázků</span><span class="sxs-lookup"><span data-stu-id="ddb5b-165">Crop images</span></span>](dam-crop-images.md)

[<span data-ttu-id="ddb5b-166">Přizpůsobení ohniska obrázku</span><span class="sxs-lookup"><span data-stu-id="ddb5b-166">Customize image focal points</span></span>](dam-custom-focal-point.md)
