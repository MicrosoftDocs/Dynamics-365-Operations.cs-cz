---
title: Konfigurace volitelných funkcí pro prostředí Preview aplikace Dynamics 365 Commerce
description: Toto téma vysvětluje, jak konfigurovat volitelné funkce náhledu Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 12/10/2019
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
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 43b23b9ef881b2ab2f3d005d4ba761848a7fa4ed
ms.sourcegitcommit: 4ed1d8ad8a0206a4172dbb41cc43f7d95073059c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024722"
---
# <a name="configure-optional-features-for-a-dynamics-365-commerce-preview-environment"></a><span data-ttu-id="2aec5-103">Konfigurace volitelných funkcí pro prostředí Preview aplikace Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="2aec5-103">Configure optional features for a Dynamics 365 Commerce preview environment</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="2aec5-104">Toto téma vysvětluje, jak konfigurovat volitelné funkce náhledu Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2aec5-104">This topic explains how to configure optional features for a Microsoft Dynamics 365 Commerce preview environment.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2aec5-105">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="2aec5-105">Prerequisites</span></span>

<span data-ttu-id="2aec5-106">Chcete-li vyhodnotit funkce transakčního e-mailu, musí být splněny následující předpoklady:</span><span class="sxs-lookup"><span data-stu-id="2aec5-106">If you want to evaluate the transactional email features, the following prerequisites must be met:</span></span>

- <span data-ttu-id="2aec5-107">Máte k dispozici e-mailový server (Simple Mail Transfer Protocol \[SMTP\]), který lze použít z předplatného Microsoft Azure, kde jste zřídili prostředí náhledu.</span><span class="sxs-lookup"><span data-stu-id="2aec5-107">You have an available email server (Simple Mail Transfer Protocol \[SMTP\] server) that can be used from the Microsoft Azure subscription where you provisioned the preview environment.</span></span>
- <span data-ttu-id="2aec5-108">Máte k dispozici plně kvalifikovaný název domény (FQDN)/IP adresu, číslo portu SMTP a podrobnosti o ověřování.</span><span class="sxs-lookup"><span data-stu-id="2aec5-108">You have the server's fully qualified domain name (FQDN)/IP address, SMTP port number, and authentication details available.</span></span>

<span data-ttu-id="2aec5-109">Chcete-li vyhodnotit funkce správy digitálních datových zdrojů pomocí přijetí nových bitových kopií omnikanálu, musíte mít k dispozici název klienta systému správy obsahu (CMS).</span><span class="sxs-lookup"><span data-stu-id="2aec5-109">If you want to evaluate Digital Asset Management features by ingesting new omni-channel images, you must have the name of your content management system (CMS) tenant available.</span></span> <span data-ttu-id="2aec5-110">Pokyny k vyhledání tohoto názvu jsou uvedeny dále v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="2aec5-110">Instructions for finding this name are provided later in this topic.</span></span> <span data-ttu-id="2aec5-111">> > > (Ot.: kde jsou instrukce?)</span><span class="sxs-lookup"><span data-stu-id="2aec5-111">>>>(Q: where are the instructions?)</span></span>

## <a name="configure-the-image-back-end"></a><span data-ttu-id="2aec5-112">Konfigurace back-endu bitové kopie</span><span class="sxs-lookup"><span data-stu-id="2aec5-112">Configure the image back end</span></span>

### <a name="find-your-media-base-url"></a><span data-ttu-id="2aec5-113">Hledání základní adresy URL média</span><span class="sxs-lookup"><span data-stu-id="2aec5-113">Find your media base URL</span></span>

> [!NOTE]
> <span data-ttu-id="2aec5-114">Před provedením tohoto postupu je třeba provést kroky uvedené v tématu [nastavení webu v Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span><span class="sxs-lookup"><span data-stu-id="2aec5-114">Before you can complete this procedure, you must complete the steps in [Set up your site in Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span></span>

1. <span data-ttu-id="2aec5-115">Přihlaste se k nástroji pro správu webu Commerce pomocí adresy URL, kterou jste si poznamenali při inicializaci e-Commerce během zřizování (viz [Inicializace e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="2aec5-115">Sign in to the Commerce site management tool by using the URL you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="2aec5-116">Otevřete stránku **Fabrikam**.</span><span class="sxs-lookup"><span data-stu-id="2aec5-116">Open the **Fabrikam** site.</span></span>
1. <span data-ttu-id="2aec5-117">V nabídce vlevo vyberte **Datové zdroje**.</span><span class="sxs-lookup"><span data-stu-id="2aec5-117">On the menu on the left, select **Assets**.</span></span>
1. <span data-ttu-id="2aec5-118">Vyberte libovolný obrázek.</span><span class="sxs-lookup"><span data-stu-id="2aec5-118">Select any single image asset.</span></span>
1. <span data-ttu-id="2aec5-119">V inspektoru vlastnosti vpravo najděte vlastnost **Veřejná adresa URL**.</span><span class="sxs-lookup"><span data-stu-id="2aec5-119">In the property inspector on the right, find the **Public URL** property.</span></span> <span data-ttu-id="2aec5-120">Hodnota je URL.</span><span class="sxs-lookup"><span data-stu-id="2aec5-120">The value is a URL.</span></span> <span data-ttu-id="2aec5-121">Následuje příklad:</span><span class="sxs-lookup"><span data-stu-id="2aec5-121">Here is an example:</span></span>

    <span data-ttu-id="2aec5-122">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span><span class="sxs-lookup"><span data-stu-id="2aec5-122">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span></span>

1. <span data-ttu-id="2aec5-123">Nahraďte poslední identifikátor v adrese URL (**MA1nQC** v předchozím příkladu) s řetězcem **search?fileName=**.</span><span class="sxs-lookup"><span data-stu-id="2aec5-123">Replace the last identifier in the URL (**MA1nQC** in the preceding example) with the string **search?fileName=**.</span></span> <span data-ttu-id="2aec5-124">Takto vypadá adresa URL po provedení této změny:</span><span class="sxs-lookup"><span data-stu-id="2aec5-124">Here is what the example URL looks like after this change is made:</span></span>

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    <span data-ttu-id="2aec5-125">Tato adresa URL je základní adresa URL média.</span><span class="sxs-lookup"><span data-stu-id="2aec5-125">This URL is your media base URL.</span></span> <span data-ttu-id="2aec5-126">Poznamenejte si ji.</span><span class="sxs-lookup"><span data-stu-id="2aec5-126">Make a note of it.</span></span>

### <a name="update-the-media-base-url"></a><span data-ttu-id="2aec5-127">Aktualizace základní adresy URL média</span><span class="sxs-lookup"><span data-stu-id="2aec5-127">Update the media base URL</span></span>

1. <span data-ttu-id="2aec5-128">Přihlaste se do Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="2aec5-128">Sign in to Dynamics 365 Retail.</span></span>
1. <span data-ttu-id="2aec5-129">Pomocí nabídky v levé části přejděte na **Moduly \> Retail \> Nastavení kanálu \> Profily kanálu**.</span><span class="sxs-lookup"><span data-stu-id="2aec5-129">Use the menu on the left to go to **Modules \> Retail \> Channel setup \> Channel profiles**.</span></span>
1. <span data-ttu-id="2aec5-130">Vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="2aec5-130">Select **Edit**.</span></span>
1. <span data-ttu-id="2aec5-131">V části **Vlastnosti profilu** nahraďte hodnotu vlastnosti **Základní adresa URL serveru médií** základní adresou URL médií, kterou jste vytvořili dříve.</span><span class="sxs-lookup"><span data-stu-id="2aec5-131">Under **Profile properties**, replace the value for the **Media Server Base URL** property with the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="2aec5-132">V seznamu vlevo pod **výchozím** kanálem vyberte jiný kanál.</span><span class="sxs-lookup"><span data-stu-id="2aec5-132">In the list on the left, under the **Default** channel, select the other channel.</span></span>
1. <span data-ttu-id="2aec5-133">Ve **Vlastnostech profilu** vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="2aec5-133">Under **Profile properties**, select **Add**.</span></span>
1. <span data-ttu-id="2aec5-134">U vlastnosti, která byla přidána, vyberte **Základní adresa URL serveru médií** jako klíč vlastnosti.</span><span class="sxs-lookup"><span data-stu-id="2aec5-134">For the property that was added, select **Media Server Base URL** as the property key.</span></span> <span data-ttu-id="2aec5-135">Jako hodnotu vlastnosti zadejte adresu URL základních médií, kterou jste vytvořili dříve.</span><span class="sxs-lookup"><span data-stu-id="2aec5-135">As the property value, enter the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="2aec5-136">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="2aec5-136">Select **Save**.</span></span>

## <a name="configure-the-email-server"></a><span data-ttu-id="2aec5-137">Konfigurace e-mailového serveru</span><span class="sxs-lookup"><span data-stu-id="2aec5-137">Configure the email server</span></span>

> [!NOTE]
> <span data-ttu-id="2aec5-138">Server SMTP nebo zadaná e-mailová služba musí být v rámci předplatného Azure, které používáte pro dané prostředí, přístupné.</span><span class="sxs-lookup"><span data-stu-id="2aec5-138">The SMTP server or email service that you enter here must be accessible from the Azure subscription that you're using for the environment.</span></span>

1. <span data-ttu-id="2aec5-139">Přihlaste se do aplikace Retail.</span><span class="sxs-lookup"><span data-stu-id="2aec5-139">Sign in to Retail.</span></span>
1. <span data-ttu-id="2aec5-140">Pomocí nabídky v levé části přejděte na **Moduly \> Správa organizace \> Nastavení \> Email \> Parametry e-mailu**.</span><span class="sxs-lookup"><span data-stu-id="2aec5-140">Use the menu on the left to go to **Modules \> System administration \> Setup \> Email \> Email parameters**.</span></span>
1. <span data-ttu-id="2aec5-141">Na kartě **Nastavení SMTP** do pole **Server odchozí pošty** zadejte FQDN nebo IP adresu serveru SMTP nebo e-mailové služby.</span><span class="sxs-lookup"><span data-stu-id="2aec5-141">On the **SMTP settings** tab, in the **Outgoing mail server** field, enter the FQDN or IP address of your SMTP server or email service.</span></span>
1. <span data-ttu-id="2aec5-142">Do pole **Číslo portu SMTP** zadejte číslo portu.</span><span class="sxs-lookup"><span data-stu-id="2aec5-142">In the **SMTP port number** field, enter the port number.</span></span> <span data-ttu-id="2aec5-143">(Pokud nepoužíváte protokol Secure Sockets Layer \[SSL\], je výchozí číslo portu **25**.)</span><span class="sxs-lookup"><span data-stu-id="2aec5-143">(If you aren't using Secure Sockets Layer \[SSL\], the default port number is **25**.)</span></span>
1. <span data-ttu-id="2aec5-144">Pokud je vyžadováno ověření, zadejte hodnoty do polí **Uživatelské jméno** a **Heslo**.</span><span class="sxs-lookup"><span data-stu-id="2aec5-144">If authentication is required, enter values in the **User name** and **Password** fields.</span></span>
1. <span data-ttu-id="2aec5-145">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="2aec5-145">Select **Save**.</span></span>
1. <span data-ttu-id="2aec5-146">Vyberte **Aktualizovat**.</span><span class="sxs-lookup"><span data-stu-id="2aec5-146">Select **Refresh**.</span></span>
1. <span data-ttu-id="2aec5-147">Na kartě **Testovací e-mail** v poli **Poskytovatel e-mailu** vyberte **SMTP**.</span><span class="sxs-lookup"><span data-stu-id="2aec5-147">On the **Test email** tab, in the **Email provider** field, select **SMTP**.</span></span>
1. <span data-ttu-id="2aec5-148">V poli **Příjemce** zadejte e-mailovou adresu, na kterou má být doručen testovací e-mail.</span><span class="sxs-lookup"><span data-stu-id="2aec5-148">In the **Send to** field, enter the email address that the test email should be delivered to.</span></span>
1. <span data-ttu-id="2aec5-149">Vyberte **Odeslat testovací e-mail**.</span><span class="sxs-lookup"><span data-stu-id="2aec5-149">Select **Send test email**.</span></span>

## <a name="configure-email-templates"></a><span data-ttu-id="2aec5-150">Konfigurace e-mailových šablon</span><span class="sxs-lookup"><span data-stu-id="2aec5-150">Configure email templates</span></span>

<span data-ttu-id="2aec5-151">Pro každou transakční událost, pro kterou chcete odeslat e-maily, musíte aktualizovat e-mailovou šablonu platnou adresou odesílatele.</span><span class="sxs-lookup"><span data-stu-id="2aec5-151">For each transactional event that you want to send emails for, you must update the email template with a valid sender email address.</span></span>

1. <span data-ttu-id="2aec5-152">Přihlaste se do aplikace Retail.</span><span class="sxs-lookup"><span data-stu-id="2aec5-152">Sign in to Retail.</span></span>
1. <span data-ttu-id="2aec5-153">Pomocí nabídky v levé části přejděte na **Moduly \> Správa organizace \> Nastavení \> Šablony e-mailu organizace**.</span><span class="sxs-lookup"><span data-stu-id="2aec5-153">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="2aec5-154">Vyberte možnost **Zobrazit seznam**.</span><span class="sxs-lookup"><span data-stu-id="2aec5-154">Select **Show list**.</span></span>
1. <span data-ttu-id="2aec5-155">Pro každou šablonu v seznamu postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="2aec5-155">For each template in the list, follow these steps:</span></span>

    1. <span data-ttu-id="2aec5-156">Do pole **Adresa odesílatele** zadejte e-mailovou adresu odesílatele.</span><span class="sxs-lookup"><span data-stu-id="2aec5-156">In the **Sender email** field, enter the sender email address.</span></span>
    1. <span data-ttu-id="2aec5-157">Volitelné: Do pole **Jméno odesílatele** zadejte jméno, které má být použito jako jméno odesílatele.</span><span class="sxs-lookup"><span data-stu-id="2aec5-157">Optional: In the **Sender name** field, enter the name that should be used as the sender name.</span></span>

1. <span data-ttu-id="2aec5-158">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="2aec5-158">Select **Save**.</span></span>

## <a name="customize-email-templates"></a><span data-ttu-id="2aec5-159">Přizpůsobení šablon e-mailu</span><span class="sxs-lookup"><span data-stu-id="2aec5-159">Customize email templates</span></span>

<span data-ttu-id="2aec5-160">Šablony e-mailů je vhodné přizpůsobit tak, aby používaly různé obrázky.</span><span class="sxs-lookup"><span data-stu-id="2aec5-160">You might want to customize the email templates so that they use different images.</span></span> <span data-ttu-id="2aec5-161">Nebo můžete chtít aktualizovat odkazy v šablonách tak, aby byly v prostředí náhledu.</span><span class="sxs-lookup"><span data-stu-id="2aec5-161">Or you might want to update the links in the templates so that they go to your preview environment.</span></span> <span data-ttu-id="2aec5-162">Tento postup vysvětluje, jak stáhnout výchozí šablony, přizpůsobit je a aktualizovat šablony v systému.</span><span class="sxs-lookup"><span data-stu-id="2aec5-162">This procedure explains how to download the default templates, customize them, and update the templates in the system.</span></span>

1. <span data-ttu-id="2aec5-163">Ve webovém prohlížeči můžete stáhnout [soubor .zip s náhledem výchozích šablon e-mailu Microsoft Dynamics 365 Commerce](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip), které obsahují následující dokumenty HTML v místním počítači.</span><span class="sxs-lookup"><span data-stu-id="2aec5-163">In a web browser, download the [Microsoft Dynamics 365 Commerce Preview default email templates zip file](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) to your local computer.</span></span> <span data-ttu-id="2aec5-164">Tento soubor obsahuje následující dokumenty HTML:</span><span class="sxs-lookup"><span data-stu-id="2aec5-164">This file contains the following HTML documents:</span></span>

    - <span data-ttu-id="2aec5-165">Šablona potvrzení objednávky</span><span class="sxs-lookup"><span data-stu-id="2aec5-165">Order confirmation template</span></span>
    - <span data-ttu-id="2aec5-166">Šablona dárkového poukazu</span><span class="sxs-lookup"><span data-stu-id="2aec5-166">Issue gift card template</span></span>
    - <span data-ttu-id="2aec5-167">Šablona nové objednávky</span><span class="sxs-lookup"><span data-stu-id="2aec5-167">New order template</span></span>
    - <span data-ttu-id="2aec5-168">Šablona objednávky balení</span><span class="sxs-lookup"><span data-stu-id="2aec5-168">Pack order template</span></span>
    - <span data-ttu-id="2aec5-169">Šablona objednávky výdeje</span><span class="sxs-lookup"><span data-stu-id="2aec5-169">Pick order template</span></span>

1. <span data-ttu-id="2aec5-170">Přizpůsobte šablony pomocí textu nebo editoru HTML.</span><span class="sxs-lookup"><span data-stu-id="2aec5-170">Customize the templates by using a text or HTML editor.</span></span> <span data-ttu-id="2aec5-171">Další informace naleznete v části [podporované tokeny](#supported-tokens-in-the-email-template) dále v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="2aec5-171">See the list of [supported tokens](#supported-tokens-in-the-email-template) later in this topic.</span></span>
1. <span data-ttu-id="2aec5-172">Přihlaste se do aplikace Retail.</span><span class="sxs-lookup"><span data-stu-id="2aec5-172">Sign in to Retail.</span></span>
1. <span data-ttu-id="2aec5-173">Pomocí nabídky v levé části přejděte na **Moduly \> Správa organizace \> Nastavení \> Šablony e-mailu organizace**.</span><span class="sxs-lookup"><span data-stu-id="2aec5-173">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="2aec5-174">Rozbalením seznamu v levé části zobrazíte všechny šablony.</span><span class="sxs-lookup"><span data-stu-id="2aec5-174">Expand the list on the left to see all the templates.</span></span>
1. <span data-ttu-id="2aec5-175">U každé šablony, kterou chcete přizpůsobit, postupujte následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="2aec5-175">For each template that you want to customize, follow these steps:</span></span>

    1. <span data-ttu-id="2aec5-176">Vyberte šablonu v seznamu.</span><span class="sxs-lookup"><span data-stu-id="2aec5-176">Select the template in the list.</span></span>
    1. <span data-ttu-id="2aec5-177">V části **Obsah e-mailové zprávy** vyberte odpovídající jazykovou verzi ze seznamu.</span><span class="sxs-lookup"><span data-stu-id="2aec5-177">Under **Email message content**, select the appropriate language version in the list.</span></span> <span data-ttu-id="2aec5-178">(Výchozí kód jazyka je **en-us**.)</span><span class="sxs-lookup"><span data-stu-id="2aec5-178">(The default language is **en-us**.)</span></span>
    1. <span data-ttu-id="2aec5-179">V části **Obsah e-mailové zprávy** vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="2aec5-179">Under **Email message content**, select **Edit**.</span></span> <span data-ttu-id="2aec5-180">Zobrazí se podokno **Odeslat šablonu e-mailu**.</span><span class="sxs-lookup"><span data-stu-id="2aec5-180">The **Upload email template** pane appears.</span></span>
    1. <span data-ttu-id="2aec5-181">Vyberte **Procházet** a najděte soubor HTML, který má přizpůsobený obsah.</span><span class="sxs-lookup"><span data-stu-id="2aec5-181">Select **Browse**, and find the HTML file that has the customized content.</span></span>
    1. <span data-ttu-id="2aec5-182">Vyberte **Odeslat**.</span><span class="sxs-lookup"><span data-stu-id="2aec5-182">Select **Upload**.</span></span> <span data-ttu-id="2aec5-183">Šablona se nahraje do systému a zobrazí se náhled.</span><span class="sxs-lookup"><span data-stu-id="2aec5-183">The template is uploaded into the system, and a preview is shown.</span></span>
    1. <span data-ttu-id="2aec5-184">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="2aec5-184">Select **OK**.</span></span>
    1. <span data-ttu-id="2aec5-185">Volitelné: Upravte vlastnost **Předmět** šablony.</span><span class="sxs-lookup"><span data-stu-id="2aec5-185">Optional: Customize the **Subject** property of the template.</span></span>
    1. <span data-ttu-id="2aec5-186">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="2aec5-186">Select **Save**.</span></span>

### <a name="supported-tokens-in-the-email-template"></a><span data-ttu-id="2aec5-187">Podporované tokeny v šabloně e-mailu</span><span class="sxs-lookup"><span data-stu-id="2aec5-187">Supported tokens in the email template</span></span>

<span data-ttu-id="2aec5-188">Když je e-mail vykreslován, budou tyto tokeny nahrazeny skutečnými hodnotami, které platí pro zákazníka a jeho objednávku.</span><span class="sxs-lookup"><span data-stu-id="2aec5-188">When the email is rendered, these tokens are replaced with actual values that apply to the customer and the customer's order.</span></span>

#### <a name="sales-order"></a><span data-ttu-id="2aec5-189">Prodejní objednávka</span><span class="sxs-lookup"><span data-stu-id="2aec5-189">Sales order</span></span>

<span data-ttu-id="2aec5-190">Následující tokeny se vztahují na celkovou prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="2aec5-190">The following tokens apply to the overall sales order.</span></span>

| <span data-ttu-id="2aec5-191">Název tokenu</span><span class="sxs-lookup"><span data-stu-id="2aec5-191">Name of the token</span></span> | <span data-ttu-id="2aec5-192">Token </span><span class="sxs-lookup"><span data-stu-id="2aec5-192">Token</span></span> |
|-------------------|-------|
| <span data-ttu-id="2aec5-193">Číslo objednávky</span><span class="sxs-lookup"><span data-stu-id="2aec5-193">Order number</span></span>      | <span data-ttu-id="2aec5-194">%salesid%</span><span class="sxs-lookup"><span data-stu-id="2aec5-194">%salesid%</span></span> |
| <span data-ttu-id="2aec5-195">Jméno zákazníka</span><span class="sxs-lookup"><span data-stu-id="2aec5-195">Customer's name</span></span>   | <span data-ttu-id="2aec5-196">%customername%</span><span class="sxs-lookup"><span data-stu-id="2aec5-196">%customername%</span></span> |
| <span data-ttu-id="2aec5-197">Adresa dodání</span><span class="sxs-lookup"><span data-stu-id="2aec5-197">Delivery address</span></span>  | <span data-ttu-id="2aec5-198">%deliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="2aec5-198">%deliveryaddress%</span></span> |
| <span data-ttu-id="2aec5-199">Fakturační adresa</span><span class="sxs-lookup"><span data-stu-id="2aec5-199">Billing address</span></span>   | <span data-ttu-id="2aec5-200">%customeraddress%</span><span class="sxs-lookup"><span data-stu-id="2aec5-200">%customeraddress%</span></span> |
| <span data-ttu-id="2aec5-201">Datum objednávky</span><span class="sxs-lookup"><span data-stu-id="2aec5-201">Order date</span></span>        | <span data-ttu-id="2aec5-202">%shipdate%</span><span class="sxs-lookup"><span data-stu-id="2aec5-202">%shipdate%</span></span> |
| <span data-ttu-id="2aec5-203">Způsob doručení</span><span class="sxs-lookup"><span data-stu-id="2aec5-203">Delivery mode</span></span>     | <span data-ttu-id="2aec5-204">%modeofdelivery%</span><span class="sxs-lookup"><span data-stu-id="2aec5-204">%modeofdelivery%</span></span> |
| <span data-ttu-id="2aec5-205">Sleva</span><span class="sxs-lookup"><span data-stu-id="2aec5-205">Discount</span></span>          | <span data-ttu-id="2aec5-206">%discount%</span><span class="sxs-lookup"><span data-stu-id="2aec5-206">%discount%</span></span> |
| <span data-ttu-id="2aec5-207">DPH</span><span class="sxs-lookup"><span data-stu-id="2aec5-207">Sales tax</span></span>         | <span data-ttu-id="2aec5-208">%tax%</span><span class="sxs-lookup"><span data-stu-id="2aec5-208">%tax%</span></span> |
| <span data-ttu-id="2aec5-209">Celková hodnota objednávky</span><span class="sxs-lookup"><span data-stu-id="2aec5-209">Order total</span></span>       | <span data-ttu-id="2aec5-210">%total%</span><span class="sxs-lookup"><span data-stu-id="2aec5-210">%total%</span></span> |

#### <a name="sales-line"></a><span data-ttu-id="2aec5-211">Řádek prodeje</span><span class="sxs-lookup"><span data-stu-id="2aec5-211">Sales line</span></span>

<span data-ttu-id="2aec5-212">Následující tokeny jsou nahrazeny hodnotami pro každý produkt v objednávce.</span><span class="sxs-lookup"><span data-stu-id="2aec5-212">The following tokens are replaced with values for each product in the order.</span></span>

> [!NOTE]
> <span data-ttu-id="2aec5-213">Token **Product list - start** vložte na začátek bloku HTML, který se opakuje u každého produktu, a token **Product list - end** na konec bloku.</span><span class="sxs-lookup"><span data-stu-id="2aec5-213">Put the **Product list - start** token at the beginning of the HTML block that is repeated for every product, and put the **Product list - end** token at the end of the block.</span></span>

| <span data-ttu-id="2aec5-214">Název tokenu</span><span class="sxs-lookup"><span data-stu-id="2aec5-214">Name of the token</span></span>      | <span data-ttu-id="2aec5-215">Token </span><span class="sxs-lookup"><span data-stu-id="2aec5-215">Token</span></span> |
|------------------------|-------|
| <span data-ttu-id="2aec5-216">Seznam produktů - začátek</span><span class="sxs-lookup"><span data-stu-id="2aec5-216">Product list - start</span></span>   | <span data-ttu-id="2aec5-217">\<!--%tablebegin.salesline% --\></span><span class="sxs-lookup"><span data-stu-id="2aec5-217">\<!--%tablebegin.salesline% --\></span></span> |
| <span data-ttu-id="2aec5-218">Seznam produktů - konec</span><span class="sxs-lookup"><span data-stu-id="2aec5-218">Product list - end</span></span>     | <span data-ttu-id="2aec5-219">\<!--%tableend.salesline%--\></span><span class="sxs-lookup"><span data-stu-id="2aec5-219">\<!--%tableend.salesline%--\></span></span> |
| <span data-ttu-id="2aec5-220">Název produktu</span><span class="sxs-lookup"><span data-stu-id="2aec5-220">Product name</span></span>           | <span data-ttu-id="2aec5-221">%lineproductname%</span><span class="sxs-lookup"><span data-stu-id="2aec5-221">%lineproductname%</span></span> |
| <span data-ttu-id="2aec5-222">Popis</span><span class="sxs-lookup"><span data-stu-id="2aec5-222">Description</span></span>            | <span data-ttu-id="2aec5-223">%lineproductdescription%</span><span class="sxs-lookup"><span data-stu-id="2aec5-223">%lineproductdescription%</span></span> |
| <span data-ttu-id="2aec5-224">Množství</span><span class="sxs-lookup"><span data-stu-id="2aec5-224">Quantity</span></span>               | <span data-ttu-id="2aec5-225">%linequantity%</span><span class="sxs-lookup"><span data-stu-id="2aec5-225">%linequantity%</span></span> |
| <span data-ttu-id="2aec5-226">Cena řádkové jednotky</span><span class="sxs-lookup"><span data-stu-id="2aec5-226">Line unit price</span></span>        | <span data-ttu-id="2aec5-227">%lineprice% (verify)</span><span class="sxs-lookup"><span data-stu-id="2aec5-227">%lineprice% (verify)</span></span> |
| <span data-ttu-id="2aec5-228">celkem řádkových položek</span><span class="sxs-lookup"><span data-stu-id="2aec5-228">line item total</span></span>        | <span data-ttu-id="2aec5-229">%linenetamount%</span><span class="sxs-lookup"><span data-stu-id="2aec5-229">%linenetamount%</span></span> |
| <span data-ttu-id="2aec5-230">řádková sleva</span><span class="sxs-lookup"><span data-stu-id="2aec5-230">line discount</span></span>          | <span data-ttu-id="2aec5-231">%linediscount%</span><span class="sxs-lookup"><span data-stu-id="2aec5-231">%linediscount%</span></span> |
| <span data-ttu-id="2aec5-232">Datum expedice</span><span class="sxs-lookup"><span data-stu-id="2aec5-232">Ship date</span></span>              | <span data-ttu-id="2aec5-233">%lineshipdate%</span><span class="sxs-lookup"><span data-stu-id="2aec5-233">%lineshipdate%</span></span> |
| <span data-ttu-id="2aec5-234">Způsob zásobování</span><span class="sxs-lookup"><span data-stu-id="2aec5-234">Procurement method</span></span>     | <span data-ttu-id="2aec5-235">%linedeliverymode%</span><span class="sxs-lookup"><span data-stu-id="2aec5-235">%linedeliverymode%</span></span> |
| <span data-ttu-id="2aec5-236">adresa dodání</span><span class="sxs-lookup"><span data-stu-id="2aec5-236">delivery address</span></span>       | <span data-ttu-id="2aec5-237">%linedeliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="2aec5-237">%linedeliveryaddress%</span></span> |
| <span data-ttu-id="2aec5-238">Prodejní jednotka řádku</span><span class="sxs-lookup"><span data-stu-id="2aec5-238">Sales unit of the line</span></span> | <span data-ttu-id="2aec5-239">%lineunit%</span><span class="sxs-lookup"><span data-stu-id="2aec5-239">%lineunit%</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="2aec5-240">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="2aec5-240">Additional resources</span></span>

[<span data-ttu-id="2aec5-241">Přehled prostředí Preview aplikace Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="2aec5-241">Dynamics 365 Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="2aec5-242">Zřízení prostředí Preview aplikace Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="2aec5-242">Provision a Dynamics 365 Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="2aec5-243">Konfigurace prostředí Preview aplikace Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="2aec5-243">Configure a Dynamics 365 Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="2aec5-244">Často kladené dotazy k prostředí Preview aplikace Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="2aec5-244">Dynamics 365 Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="2aec5-245">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="2aec5-245">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="2aec5-246">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="2aec5-246">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="2aec5-247">Portál Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="2aec5-247">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="2aec5-248">Web Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="2aec5-248">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
