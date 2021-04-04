---
title: Správa souborů robots.txt
description: Toto téma popisuje správu souborů robots.txt v aplikaci Microsoft Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2019-12-18
ms.dyn365.ops.version: ''
ms.openlocfilehash: afd7982179dc9845c9adc24e8c7c9951a04460a3
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477701"
---
# <a name="manage-robotstxt-files"></a><span data-ttu-id="2494d-103">Správa souborů robots.txt</span><span class="sxs-lookup"><span data-stu-id="2494d-103">Manage robots.txt files</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2494d-104">Toto téma popisuje správu souborů robots.txt v aplikaci Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2494d-104">This topic describes how to manage robots.txt files in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="2494d-105">Protokol pro zakázání přístupu robotům, neboli robots.txt, je standardem, který weby používají ke komunikaci s webovými roboty.</span><span class="sxs-lookup"><span data-stu-id="2494d-105">The robots exclusion standard, or robots.txt, is a standard that websites use to communicate with web robots.</span></span> <span data-ttu-id="2494d-106">Protokol dává pokyny webovým robotům o všech oblastech webu, které by neměly být navštíveny.</span><span class="sxs-lookup"><span data-stu-id="2494d-106">It instructs web robots about any areas of a website that should not be visited.</span></span> <span data-ttu-id="2494d-107">Roboti často používají vyhledávací stroje k indexování webů.</span><span class="sxs-lookup"><span data-stu-id="2494d-107">Robots are often used by search engines to index websites.</span></span>

<span data-ttu-id="2494d-108">Chcete-li ze serveru vyloučit roboty, vytvoříte na serveru soubor.</span><span class="sxs-lookup"><span data-stu-id="2494d-108">To exclude robots from a server, you create a file on the server.</span></span> <span data-ttu-id="2494d-109">V tomto souboru určíte zásady přístupu pro roboty.</span><span class="sxs-lookup"><span data-stu-id="2494d-109">In this file, you specify an access policy for robots.</span></span> <span data-ttu-id="2494d-110">Soubor musí být přístupný prostřednictvím protokolu HTTP na místní adrese URL **/robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="2494d-110">The file must be accessible via HTTP at the local URL **/robots.txt**.</span></span> <span data-ttu-id="2494d-111">Soubor robots.txt pomáhá vyhledávacím webům indexovat obsah vašeho webu.</span><span class="sxs-lookup"><span data-stu-id="2494d-111">The robots.txt file helps search engines index the content on your site.</span></span>

<span data-ttu-id="2494d-112">Dynamics 365 Commerce umožňuje odeslat do vaší domény soubor robots.txt.</span><span class="sxs-lookup"><span data-stu-id="2494d-112">Dynamics 365 Commerce lets you upload a robots.txt file for your domain.</span></span> <span data-ttu-id="2494d-113">Pro každou doménu v prostředí Commerce můžete odeslat jeden soubor robots.txt a přidružit jej k této doméně.</span><span class="sxs-lookup"><span data-stu-id="2494d-113">For each domain in your Commerce environment, you can upload one robots.txt file and associate it with that domain.</span></span>

<span data-ttu-id="2494d-114">Další informace o souboru robots.txt naleznete v části [Stránky webových robotů](https://www.robotstxt.org/).</span><span class="sxs-lookup"><span data-stu-id="2494d-114">For more information about the robots.txt file, visit [The Web Robots Pages](https://www.robotstxt.org/).</span></span>

## <a name="upload-a-robotstxt-file"></a><span data-ttu-id="2494d-115">Odeslání souboru robots.txt</span><span class="sxs-lookup"><span data-stu-id="2494d-115">Upload a robots.txt file</span></span>

<span data-ttu-id="2494d-116">Po vytvoření a úpravě souboru robots.txt podle [protokolu pro zakázání přístupu robotům](https://www.robotstxt.org/orig.html) zkontrolujte, zda je soubor přístupný v počítači, ve kterém budete používat vývojářské nástroje Commerce.</span><span class="sxs-lookup"><span data-stu-id="2494d-116">After you've created and edited your robots.txt file according to the [robots exclusion standard](https://www.robotstxt.org/orig.html), make sure that the file is accessible on the computer where you will use the Commerce authoring tools.</span></span> <span data-ttu-id="2494d-117">Soubor musí mít název **robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="2494d-117">The file must be named **robots.txt**.</span></span> <span data-ttu-id="2494d-118">Pro dosažení optimálních výsledků musí být ve formátu uvedeném v protokolu.</span><span class="sxs-lookup"><span data-stu-id="2494d-118">For best results, it must be in the format that is noted in the standard.</span></span> <span data-ttu-id="2494d-119">Každý zákazník Commerce je zodpovědný za ověřování a údržbu obsahu souboru robots.txt.</span><span class="sxs-lookup"><span data-stu-id="2494d-119">Each Commerce customer is responsible for validating and maintaining the contents of its robots.txt file.</span></span> <span data-ttu-id="2494d-120">Chcete-li odeslat soubor robots.txt, musíte být přihlášen ke Commerce jako správce systému.</span><span class="sxs-lookup"><span data-stu-id="2494d-120">To upload a robots.txt file, you must be signed in to Commerce as a system admin.</span></span>

<span data-ttu-id="2494d-121">Postup odeslání souboru robots.txt v Commerce je následovný.</span><span class="sxs-lookup"><span data-stu-id="2494d-121">To upload a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="2494d-122">Přihlaste se k Commerce jako správce systému.</span><span class="sxs-lookup"><span data-stu-id="2494d-122">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="2494d-123">V levém navigačním podokně vyberte **Nastavení klienta** (vedle symbolu ozubeného kola), čímž jej rozbalíte.</span><span class="sxs-lookup"><span data-stu-id="2494d-123">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="2494d-124">V části **Nastavení klienta** vyberte **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="2494d-124">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="2494d-125">V hlavní části okna se zobrazí seznam všech domén přidružených k danému prostředí.</span><span class="sxs-lookup"><span data-stu-id="2494d-125">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="2494d-126">Volbou **Spravovat** odešlete soubor robots.txt do domény ve vašem prostředí.</span><span class="sxs-lookup"><span data-stu-id="2494d-126">Select **Manage** to upload a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="2494d-127">V nabídce vpravo klikněte na tlačítko **Odeslat** (šipka směřující nahoru) vedle domény, která je přidružena k souboru robots.txt.</span><span class="sxs-lookup"><span data-stu-id="2494d-127">On the menu on the right, select the **Upload** button (the upward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="2494d-128">Zobrazí se dialogové okno prohlížeče souborů.</span><span class="sxs-lookup"><span data-stu-id="2494d-128">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="2494d-129">V dialogovém okně vyhledejte a vyberte soubor robots.txt, který chcete odeslat pro přidruženou doménu, a pak volbou **Otevřít** dokončete odeslání souboru.</span><span class="sxs-lookup"><span data-stu-id="2494d-129">In the dialog box, browse to and select the robots.txt file that you want to upload for the associated domain, and then select **Open** to complete the upload.</span></span>

> [!NOTE] 
> <span data-ttu-id="2494d-130">Během odesílání Commerce ověří, že soubor je textový soubor, ale neověří obsah souboru.</span><span class="sxs-lookup"><span data-stu-id="2494d-130">During upload, Commerce verifies that the file is a text file, but it doesn't validate the file's contents.</span></span>

## <a name="download-a-robotstxt-file"></a><span data-ttu-id="2494d-131">Stažení souboru robots.txt</span><span class="sxs-lookup"><span data-stu-id="2494d-131">Download a robots.txt file</span></span>

<span data-ttu-id="2494d-132">Postup stažení souboru robots.txt v Commerce je následovný.</span><span class="sxs-lookup"><span data-stu-id="2494d-132">To download a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="2494d-133">Přihlaste se k Commerce jako správce systému.</span><span class="sxs-lookup"><span data-stu-id="2494d-133">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="2494d-134">V levém navigačním podokně vyberte **Nastavení klienta** (vedle symbolu ozubeného kola), čímž jej rozbalíte.</span><span class="sxs-lookup"><span data-stu-id="2494d-134">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="2494d-135">V části **Nastavení klienta** vyberte **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="2494d-135">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="2494d-136">V hlavní části okna se zobrazí seznam všech domén přidružených k danému prostředí.</span><span class="sxs-lookup"><span data-stu-id="2494d-136">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="2494d-137">Volbou **Spravovat** stáhnete soubor robots.txt do domény ve vašem prostředí.</span><span class="sxs-lookup"><span data-stu-id="2494d-137">Select **Manage** to download a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="2494d-138">V nabídce vpravo klikněte na tlačítko **Stáhnout** (šipka směřující dolů) vedle domény, která je přidružena k souboru robots.txt.</span><span class="sxs-lookup"><span data-stu-id="2494d-138">On the menu on the right, select the **Download** button (the downward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="2494d-139">Zobrazí se dialogové okno prohlížeče souborů.</span><span class="sxs-lookup"><span data-stu-id="2494d-139">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="2494d-140">V dialogovém okně přejděte k požadovanému umístění na místním disku, potvrďte nebo zadejte název souboru a potom volbou **Uložit** dokončete stahování.</span><span class="sxs-lookup"><span data-stu-id="2494d-140">In the dialog box, go to the desired location on your local drive, confirm or enter a file name, and then select **Save** to complete the download.</span></span>

> [!NOTE]
> <span data-ttu-id="2494d-141">Tento postup lze použít ke stažení pouze souborů robots.txt, které byly dříve odeslány pomocí vývojářských nástrojů Commerce.</span><span class="sxs-lookup"><span data-stu-id="2494d-141">This procedure can be used to download only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="delete-a-robotstxt-file"></a><span data-ttu-id="2494d-142">Odstranění souboru robots.txt</span><span class="sxs-lookup"><span data-stu-id="2494d-142">Delete a robots.txt file</span></span>

<span data-ttu-id="2494d-143">Postup odstranění souboru robots.txt v Commerce je následovný.</span><span class="sxs-lookup"><span data-stu-id="2494d-143">To delete a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="2494d-144">Přihlaste se k Commerce jako správce systému.</span><span class="sxs-lookup"><span data-stu-id="2494d-144">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="2494d-145">V levém navigačním podokně vyberte **Nastavení klienta** (vedle symbolu ozubeného kola), čímž jej rozbalíte.</span><span class="sxs-lookup"><span data-stu-id="2494d-145">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="2494d-146">V části **Nastavení klienta** vyberte **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="2494d-146">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="2494d-147">V hlavní části okna se zobrazí seznam všech domén přidružených k danému prostředí.</span><span class="sxs-lookup"><span data-stu-id="2494d-147">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="2494d-148">Volbou **Spravovat** odstraníte soubor robots.txt do domény ve vašem prostředí.</span><span class="sxs-lookup"><span data-stu-id="2494d-148">Select **Manage** to delete a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="2494d-149">V nabídce vpravo klikněte na tlačítko **Odstranit** (symbol odpadkového koše) vedle domény, která je přidružena k souboru robots.txt.</span><span class="sxs-lookup"><span data-stu-id="2494d-149">On the menu on the right, select the **Delete** button (the trash can symbol) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="2494d-150">Zobrazí se okno prohlížeče souborů.</span><span class="sxs-lookup"><span data-stu-id="2494d-150">A file browser window appears.</span></span>
6. <span data-ttu-id="2494d-151">V okně prohlížeče souborů vyhledejte a vyberte soubor robots.txt, který chcete odstranit pro danou doménu, a vyberte volbu **Otevřít**.</span><span class="sxs-lookup"><span data-stu-id="2494d-151">In the file browser window, browse to and select the robots.txt file that you want to delete for the domain, and then select **Open**.</span></span> <span data-ttu-id="2494d-152">Zobrazí se okno se zprávou upozornění.</span><span class="sxs-lookup"><span data-stu-id="2494d-152">A warning message box appears.</span></span>
7. <span data-ttu-id="2494d-153">V okně se zprávou vyberte možnost **Odstranit** a potvrďte odstranění souboru robots.txt.</span><span class="sxs-lookup"><span data-stu-id="2494d-153">In the message box, select **Delete** to confirm deletion of the robots.txt file.</span></span>

> [!NOTE] 
> <span data-ttu-id="2494d-154">Tento postup lze použít k odstranění pouze souborů robots.txt, které byly dříve odeslány pomocí vývojářských nástrojů Commerce.</span><span class="sxs-lookup"><span data-stu-id="2494d-154">This procedure can be used to delete only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2494d-155">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="2494d-155">Additional resources</span></span>

[<span data-ttu-id="2494d-156">Konfigurace názvu domény</span><span class="sxs-lookup"><span data-stu-id="2494d-156">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="2494d-157">Nasazení nového klienta elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="2494d-157">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="2494d-158">Vytvoření webu elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="2494d-158">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="2494d-159">Přidružení webu Dynamics 365 Commerce k online kanálu</span><span class="sxs-lookup"><span data-stu-id="2494d-159">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="2494d-160">Hromadné odeslání přesměrování URL adresy</span><span class="sxs-lookup"><span data-stu-id="2494d-160">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="2494d-161">Nastavení klienta B2C v Commerce</span><span class="sxs-lookup"><span data-stu-id="2494d-161">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="2494d-162">Nastavení vlastních stránek pro přihlášení uživatelů</span><span class="sxs-lookup"><span data-stu-id="2494d-162">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="2494d-163">Konfigurace několika klientů B2C v prostředí Commerce</span><span class="sxs-lookup"><span data-stu-id="2494d-163">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="2494d-164">Přidání podpory pro síť CDN</span><span class="sxs-lookup"><span data-stu-id="2494d-164">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="2494d-165">Povolení zjišťování obchodu na základě polohy</span><span class="sxs-lookup"><span data-stu-id="2494d-165">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
