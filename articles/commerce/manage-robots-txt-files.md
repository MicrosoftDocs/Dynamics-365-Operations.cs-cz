---
title: Správa souborů robots.txt
description: Toto téma popisuje správu souborů robots.txt v aplikaci Microsoft Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: brishoo
ms.search.validFrom: 2019-12-18
ms.dyn365.ops.version: ''
ms.openlocfilehash: d0ce49f2968030ca4656a01c7646819c01635e12
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003480"
---
# <a name="manage-robotstxt-files"></a><span data-ttu-id="71c56-103">Správa souborů robots.txt</span><span class="sxs-lookup"><span data-stu-id="71c56-103">Manage robots.txt files</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="71c56-104">Toto téma popisuje správu souborů robots.txt v aplikaci Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="71c56-104">This topic describes how to manage robots.txt files in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="71c56-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="71c56-105">Overview</span></span>

<span data-ttu-id="71c56-106">Protokol pro zakázání přístupu robotům, neboli robots.txt, je standardem, který weby používají ke komunikaci s webovými roboty.</span><span class="sxs-lookup"><span data-stu-id="71c56-106">The robots exclusion standard, or robots.txt, is a standard that websites use to communicate with web robots.</span></span> <span data-ttu-id="71c56-107">Protokol dává pokyny webovým robotům o všech oblastech webu, které by neměly být navštíveny.</span><span class="sxs-lookup"><span data-stu-id="71c56-107">It instructs web robots about any areas of a website that should not be visited.</span></span> <span data-ttu-id="71c56-108">Roboti často používají vyhledávací stroje k indexování webů.</span><span class="sxs-lookup"><span data-stu-id="71c56-108">Robots are often used by search engines to index websites.</span></span>

<span data-ttu-id="71c56-109">Chcete-li ze serveru vyloučit roboty, vytvoříte na serveru soubor.</span><span class="sxs-lookup"><span data-stu-id="71c56-109">To exclude robots from a server, you create a file on the server.</span></span> <span data-ttu-id="71c56-110">V tomto souboru určíte zásady přístupu pro roboty.</span><span class="sxs-lookup"><span data-stu-id="71c56-110">In this file, you specify an access policy for robots.</span></span> <span data-ttu-id="71c56-111">Soubor musí být přístupný prostřednictvím protokolu HTTP na místní adrese URL **/robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="71c56-111">The file must be accessible via HTTP at the local URL **/robots.txt**.</span></span> <span data-ttu-id="71c56-112">Soubor robots.txt pomáhá vyhledávacím webům indexovat obsah vašeho webu.</span><span class="sxs-lookup"><span data-stu-id="71c56-112">The robots.txt file helps search engines index the content on your site.</span></span>

<span data-ttu-id="71c56-113">Dynamics 365 Commerce umožňuje odeslat do vaší domény soubor robots.txt.</span><span class="sxs-lookup"><span data-stu-id="71c56-113">Dynamics 365 Commerce lets you upload a robots.txt file for your domain.</span></span> <span data-ttu-id="71c56-114">Pro každou doménu v prostředí Commerce můžete odeslat jeden soubor robots.txt a přidružit jej k této doméně.</span><span class="sxs-lookup"><span data-stu-id="71c56-114">For each domain in your Commerce environment, you can upload one robots.txt file and associate it with that domain.</span></span>

<span data-ttu-id="71c56-115">Další informace o souboru robots.txt naleznete v části [Stránky webových robotů](https://www.robotstxt.org/).</span><span class="sxs-lookup"><span data-stu-id="71c56-115">For more information about the robots.txt file, visit [The Web Robots Pages](https://www.robotstxt.org/).</span></span>

## <a name="upload-a-robotstxt-file"></a><span data-ttu-id="71c56-116">Odeslání souboru robots.txt</span><span class="sxs-lookup"><span data-stu-id="71c56-116">Upload a robots.txt file</span></span>

<span data-ttu-id="71c56-117">Po vytvoření a úpravě souboru robots.txt podle [protokolu pro zakázání přístupu robotům](https://www.robotstxt.org/orig.html) zkontrolujte, zda je soubor přístupný v počítači, ve kterém budete používat vývojářské nástroje Commerce.</span><span class="sxs-lookup"><span data-stu-id="71c56-117">After you've created and edited your robots.txt file according to the [robots exclusion standard](https://www.robotstxt.org/orig.html), make sure that the file is accessible on the computer where you will use the Commerce authoring tools.</span></span> <span data-ttu-id="71c56-118">Soubor musí mít název **robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="71c56-118">The file must be named **robots.txt**.</span></span> <span data-ttu-id="71c56-119">Pro dosažení optimálních výsledků musí být ve formátu uvedeném v protokolu.</span><span class="sxs-lookup"><span data-stu-id="71c56-119">For best results, it must be in the format that is noted in the standard.</span></span> <span data-ttu-id="71c56-120">Každý zákazník Commerce je zodpovědný za ověřování a údržbu obsahu souboru robots.txt.</span><span class="sxs-lookup"><span data-stu-id="71c56-120">Each Commerce customer is responsible for validating and maintaining the contents of its robots.txt file.</span></span> <span data-ttu-id="71c56-121">Chcete-li odeslat soubor robots.txt, musíte být přihlášen ke Commerce jako správce systému.</span><span class="sxs-lookup"><span data-stu-id="71c56-121">To upload a robots.txt file, you must be signed in to Commerce as a system admin.</span></span>

<span data-ttu-id="71c56-122">Postup odeslání souboru robots.txt v Commerce je následovný.</span><span class="sxs-lookup"><span data-stu-id="71c56-122">To upload a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="71c56-123">Přihlaste se k Commerce jako správce systému.</span><span class="sxs-lookup"><span data-stu-id="71c56-123">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="71c56-124">V levém navigačním podokně vyberte **Nastavení klienta** (vedle symbolu ozubeného kola), čímž jej rozbalíte.</span><span class="sxs-lookup"><span data-stu-id="71c56-124">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="71c56-125">V části **Nastavení klienta** vyberte **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="71c56-125">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="71c56-126">V hlavní části okna se zobrazí seznam všech domén přidružených k danému prostředí.</span><span class="sxs-lookup"><span data-stu-id="71c56-126">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="71c56-127">Volbou **Spravovat** odešlete soubor robots.txt do domény ve vašem prostředí.</span><span class="sxs-lookup"><span data-stu-id="71c56-127">Select **Manage** to upload a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="71c56-128">V nabídce vpravo klikněte na tlačítko **Odeslat** (šipka směřující nahoru) vedle domény, která je přidružena k souboru robots.txt.</span><span class="sxs-lookup"><span data-stu-id="71c56-128">On the menu on the right, select the **Upload** button (the upward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="71c56-129">Zobrazí se dialogové okno prohlížeče souborů.</span><span class="sxs-lookup"><span data-stu-id="71c56-129">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="71c56-130">V dialogovém okně vyhledejte a vyberte soubor robots.txt, který chcete odeslat pro přidruženou doménu, a pak volbou **Otevřít** dokončete odeslání souboru.</span><span class="sxs-lookup"><span data-stu-id="71c56-130">In the dialog box, browse to and select the robots.txt file that you want to upload for the associated domain, and then select **Open** to complete the upload.</span></span>

> [!NOTE] 
> <span data-ttu-id="71c56-131">Během odesílání Commerce ověří, že soubor je textový soubor, ale neověří obsah souboru.</span><span class="sxs-lookup"><span data-stu-id="71c56-131">During upload, Commerce verifies that the file is a text file, but it doesn't validate the file's contents.</span></span>

## <a name="download-a-robotstxt-file"></a><span data-ttu-id="71c56-132">Stažení souboru robots.txt</span><span class="sxs-lookup"><span data-stu-id="71c56-132">Download a robots.txt file</span></span>

<span data-ttu-id="71c56-133">Postup stažení souboru robots.txt v Commerce je následovný.</span><span class="sxs-lookup"><span data-stu-id="71c56-133">To download a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="71c56-134">Přihlaste se k Commerce jako správce systému.</span><span class="sxs-lookup"><span data-stu-id="71c56-134">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="71c56-135">V levém navigačním podokně vyberte **Nastavení klienta** (vedle symbolu ozubeného kola), čímž jej rozbalíte.</span><span class="sxs-lookup"><span data-stu-id="71c56-135">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="71c56-136">V části **Nastavení klienta** vyberte **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="71c56-136">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="71c56-137">V hlavní části okna se zobrazí seznam všech domén přidružených k danému prostředí.</span><span class="sxs-lookup"><span data-stu-id="71c56-137">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="71c56-138">Volbou **Spravovat** stáhnete soubor robots.txt do domény ve vašem prostředí.</span><span class="sxs-lookup"><span data-stu-id="71c56-138">Select **Manage** to download a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="71c56-139">V nabídce vpravo klikněte na tlačítko **Stáhnout** (šipka směřující dolů) vedle domény, která je přidružena k souboru robots.txt.</span><span class="sxs-lookup"><span data-stu-id="71c56-139">On the menu on the right, select the **Download** button (the downward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="71c56-140">Zobrazí se dialogové okno prohlížeče souborů.</span><span class="sxs-lookup"><span data-stu-id="71c56-140">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="71c56-141">V dialogovém okně přejděte k požadovanému umístění na místním disku, potvrďte nebo zadejte název souboru a potom volbou **Uložit** dokončete stahování.</span><span class="sxs-lookup"><span data-stu-id="71c56-141">In the dialog box, go to the desired location on your local drive, confirm or enter a file name, and then select **Save** to complete the download.</span></span>

> [!NOTE]
> <span data-ttu-id="71c56-142">Tento postup lze použít ke stažení pouze souborů robots.txt, které byly dříve odeslány pomocí vývojářských nástrojů Commerce.</span><span class="sxs-lookup"><span data-stu-id="71c56-142">This procedure can be used to download only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="delete-a-robotstxt-file"></a><span data-ttu-id="71c56-143">Odstranění souboru robots.txt</span><span class="sxs-lookup"><span data-stu-id="71c56-143">Delete a robots.txt file</span></span>

<span data-ttu-id="71c56-144">Postup odstranění souboru robots.txt v Commerce je následovný.</span><span class="sxs-lookup"><span data-stu-id="71c56-144">To delete a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="71c56-145">Přihlaste se k Commerce jako správce systému.</span><span class="sxs-lookup"><span data-stu-id="71c56-145">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="71c56-146">V levém navigačním podokně vyberte **Nastavení klienta** (vedle symbolu ozubeného kola), čímž jej rozbalíte.</span><span class="sxs-lookup"><span data-stu-id="71c56-146">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="71c56-147">V části **Nastavení klienta** vyberte **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="71c56-147">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="71c56-148">V hlavní části okna se zobrazí seznam všech domén přidružených k danému prostředí.</span><span class="sxs-lookup"><span data-stu-id="71c56-148">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="71c56-149">Volbou **Spravovat** odstraníte soubor robots.txt do domény ve vašem prostředí.</span><span class="sxs-lookup"><span data-stu-id="71c56-149">Select **Manage** to delete a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="71c56-150">V nabídce vpravo klikněte na tlačítko **Odstranit** (symbol odpadkového koše) vedle domény, která je přidružena k souboru robots.txt.</span><span class="sxs-lookup"><span data-stu-id="71c56-150">On the menu on the right, select the **Delete** button (the trash can symbol) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="71c56-151">Zobrazí se okno prohlížeče souborů.</span><span class="sxs-lookup"><span data-stu-id="71c56-151">A file browser window appears.</span></span>
6. <span data-ttu-id="71c56-152">V okně prohlížeče souborů vyhledejte a vyberte soubor robots.txt, který chcete odstranit pro danou doménu, a vyberte volbu **Otevřít**.</span><span class="sxs-lookup"><span data-stu-id="71c56-152">In the file browser window, browse to and select the robots.txt file that you want to delete for the domain, and then select **Open**.</span></span> <span data-ttu-id="71c56-153">Zobrazí se okno se zprávou upozornění.</span><span class="sxs-lookup"><span data-stu-id="71c56-153">A warning message box appears.</span></span>
7. <span data-ttu-id="71c56-154">V okně se zprávou vyberte možnost **Odstranit** a potvrďte odstranění souboru robots.txt.</span><span class="sxs-lookup"><span data-stu-id="71c56-154">In the message box, select **Delete** to confirm deletion of the robots.txt file.</span></span>

> [!NOTE] 
> <span data-ttu-id="71c56-155">Tento postup lze použít k odstranění pouze souborů robots.txt, které byly dříve odeslány pomocí vývojářských nástrojů Commerce.</span><span class="sxs-lookup"><span data-stu-id="71c56-155">This procedure can be used to delete only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="71c56-156">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="71c56-156">Additional resources</span></span>

[<span data-ttu-id="71c56-157">Konfigurace názvu domény</span><span class="sxs-lookup"><span data-stu-id="71c56-157">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="71c56-158">Nasazení nového webu elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="71c56-158">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="71c56-159">Vytvoření webu elektronického obchodu</span><span class="sxs-lookup"><span data-stu-id="71c56-159">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="71c56-160">Přiřazení online webu ke kanálu</span><span class="sxs-lookup"><span data-stu-id="71c56-160">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="71c56-161">Nastavení vlastních stránek pro přihlášení uživatelů</span><span class="sxs-lookup"><span data-stu-id="71c56-161">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="71c56-162">Přidání podpory pro síť CDN</span><span class="sxs-lookup"><span data-stu-id="71c56-162">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="71c56-163">Povolení zjišťování obchodu na základě polohy</span><span class="sxs-lookup"><span data-stu-id="71c56-163">Enable location-based store detection</span></span>](enable-store-detection.md)
