---
title: Konfigurace volitelných funkcí pro prostředí vyhodnocení aplikace Dynamics 365 Commerce
description: Toto téma vysvětluje, jak konfigurovat volitelné funkce prostředí vyhodnocení Microsoft Dynamics 365 Commerce.
author: psimolin
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0a93429e836d818458f11f6f6821fda237edc291
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/22/2021
ms.locfileid: "5936973"
---
# <a name="configure-optional-features-for-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="b80ee-103">Konfigurace volitelných funkcí pro prostředí vyhodnocení aplikace Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="b80ee-103">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b80ee-104">Toto téma vysvětluje, jak konfigurovat volitelné funkce prostředí vyhodnocení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b80ee-104">This topic explains how to configure optional features for a Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b80ee-105">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="b80ee-105">Prerequisites</span></span>

<span data-ttu-id="b80ee-106">Chcete-li vyhodnotit funkce transakčního e-mailu, musí být splněny následující předpoklady:</span><span class="sxs-lookup"><span data-stu-id="b80ee-106">If you want to evaluate the transactional email features, the following prerequisites must be met:</span></span>

- <span data-ttu-id="b80ee-107">Máte k dispozici e-mailový server (Simple Mail Transfer Protocol \[SMTP\]), který lze použít z předplatného Microsoft Azure, kde jste zřídili prostředí vyhodnocení.</span><span class="sxs-lookup"><span data-stu-id="b80ee-107">You have an available email server (Simple Mail Transfer Protocol \[SMTP\] server) that can be used from the Microsoft Azure subscription where you provisioned the evaluation environment.</span></span>
- <span data-ttu-id="b80ee-108">Máte k dispozici plně kvalifikovaný název domény (FQDN)/IP adresu, číslo portu SMTP a podrobnosti o ověřování.</span><span class="sxs-lookup"><span data-stu-id="b80ee-108">You have the server's fully qualified domain name (FQDN)/IP address, SMTP port number, and authentication details available.</span></span>

## <a name="configure-the-image-back-end"></a><span data-ttu-id="b80ee-109">Konfigurace back-endu bitové kopie</span><span class="sxs-lookup"><span data-stu-id="b80ee-109">Configure the image back end</span></span>

### <a name="find-your-media-base-url"></a><span data-ttu-id="b80ee-110">Hledání základní adresy URL média</span><span class="sxs-lookup"><span data-stu-id="b80ee-110">Find your media base URL</span></span>

> [!NOTE]
> <span data-ttu-id="b80ee-111">Před provedením tohoto postupu je třeba provést kroky uvedené v tématu [nastavení webu v Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span><span class="sxs-lookup"><span data-stu-id="b80ee-111">Before you can complete this procedure, you must complete the steps in [Set up your site in Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span></span>

1. <span data-ttu-id="b80ee-112">Přihlaste se k nástroji pro tvorbu webu Commerce pomocí adresy URL, kterou jste si poznamenali při inicializaci e-Commerce během zřizování (viz [Inicializace e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="b80ee-112">Sign in to the Commerce site builder by using the URL you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="b80ee-113">Otevřete stránku **Fabrikam**.</span><span class="sxs-lookup"><span data-stu-id="b80ee-113">Open the **Fabrikam** site.</span></span>
1. <span data-ttu-id="b80ee-114">V nabídce vlevo vyberte **Mediální knihovna**.</span><span class="sxs-lookup"><span data-stu-id="b80ee-114">On the menu on the left, select **Media Library**.</span></span>
1. <span data-ttu-id="b80ee-115">Vyberte libovolný obrázek.</span><span class="sxs-lookup"><span data-stu-id="b80ee-115">Select any single image asset.</span></span>
1. <span data-ttu-id="b80ee-116">V inspektoru vlastnosti vpravo najděte vlastnost **Veřejná adresa URL**.</span><span class="sxs-lookup"><span data-stu-id="b80ee-116">In the property inspector on the right, find the **Public URL** property.</span></span> <span data-ttu-id="b80ee-117">Hodnota je URL.</span><span class="sxs-lookup"><span data-stu-id="b80ee-117">The value is a URL.</span></span> <span data-ttu-id="b80ee-118">Následuje příklad:</span><span class="sxs-lookup"><span data-stu-id="b80ee-118">Here is an example:</span></span>

    <span data-ttu-id="b80ee-119">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span><span class="sxs-lookup"><span data-stu-id="b80ee-119">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span></span>

1. <span data-ttu-id="b80ee-120">Nahraďte poslední identifikátor v adrese URL (**MA1nQC** v předchozím příkladu) s řetězcem **search?fileName=**.</span><span class="sxs-lookup"><span data-stu-id="b80ee-120">Replace the last identifier in the URL (**MA1nQC** in the preceding example) with the string **search?fileName=**.</span></span> <span data-ttu-id="b80ee-121">Takto vypadá adresa URL po provedení této změny:</span><span class="sxs-lookup"><span data-stu-id="b80ee-121">Here is what the example URL looks like after this change is made:</span></span>

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    <span data-ttu-id="b80ee-122">Tato adresa URL je základní adresa URL média.</span><span class="sxs-lookup"><span data-stu-id="b80ee-122">This URL is your media base URL.</span></span> <span data-ttu-id="b80ee-123">Poznamenejte si ji.</span><span class="sxs-lookup"><span data-stu-id="b80ee-123">Make a note of it.</span></span>

### <a name="update-the-media-base-url"></a><span data-ttu-id="b80ee-124">Aktualizace základní adresy URL média</span><span class="sxs-lookup"><span data-stu-id="b80ee-124">Update the media base URL</span></span>

1. <span data-ttu-id="b80ee-125">Přihlaste se do centrály Commerce.</span><span class="sxs-lookup"><span data-stu-id="b80ee-125">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="b80ee-126">Pomocí nabídky v levé části přejděte na **Moduly \> Retail and commerce \> Nastavení kanálu \> Profily kanálu**.</span><span class="sxs-lookup"><span data-stu-id="b80ee-126">Use the menu on the left to go to **Modules \> Retail and commerce \> Channel setup \> Channel profiles**.</span></span>
1. <span data-ttu-id="b80ee-127">Vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="b80ee-127">Select **Edit**.</span></span>
1. <span data-ttu-id="b80ee-128">V části **Vlastnosti profilu** nahraďte hodnotu vlastnosti **Základní adresa URL serveru médií** základní adresou URL médií, kterou jste vytvořili dříve.</span><span class="sxs-lookup"><span data-stu-id="b80ee-128">Under **Profile properties**, replace the value for the **Media Server Base URL** property with the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="b80ee-129">Vyberte kanál, který je nazvaný **scXXXXXXXXX**.</span><span class="sxs-lookup"><span data-stu-id="b80ee-129">Select the channel that is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="b80ee-130">Ve **Vlastnostech profilu** vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="b80ee-130">Under **Profile properties**, select **Add**.</span></span>
1. <span data-ttu-id="b80ee-131">U vlastnosti, která byla přidána, vyberte **Základní adresa URL serveru médií** jako klíč vlastnosti.</span><span class="sxs-lookup"><span data-stu-id="b80ee-131">For the property that was added, select **Media Server Base URL** as the property key.</span></span> <span data-ttu-id="b80ee-132">Jako hodnotu vlastnosti zadejte adresu URL základních médií, kterou jste vytvořili dříve.</span><span class="sxs-lookup"><span data-stu-id="b80ee-132">As the property value, enter the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="b80ee-133">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="b80ee-133">Select **Save**.</span></span>

## <a name="configure-and-test-the-email-server"></a><span data-ttu-id="b80ee-134">Konfigurace a test e-mailového serveru</span><span class="sxs-lookup"><span data-stu-id="b80ee-134">Configure and test the email server</span></span>

> [!NOTE]
> <span data-ttu-id="b80ee-135">Server SMTP nebo zadaná e-mailová služba musí být v rámci předplatného Azure, které používáte pro dané prostředí, přístupné.</span><span class="sxs-lookup"><span data-stu-id="b80ee-135">The SMTP server or email service that you enter here must be accessible from the Azure subscription that you're using for the environment.</span></span>

1. <span data-ttu-id="b80ee-136">Přihlaste se do centrály Commerce.</span><span class="sxs-lookup"><span data-stu-id="b80ee-136">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="b80ee-137">Pomocí nabídky v levé části přejděte na **Moduly \> Retail \> Nastavení centrály \> Parametry \> Parametry e-mailu**.</span><span class="sxs-lookup"><span data-stu-id="b80ee-137">Use the menu on the left to go to **Modules \> Retail and Commerce \> Headquarters setup \> Parameters \> Email parameters**.</span></span>
1. <span data-ttu-id="b80ee-138">Na kartě **Nastavení SMTP** do pole **Server odchozí pošty** zadejte FQDN nebo IP adresu serveru SMTP nebo e-mailové služby.</span><span class="sxs-lookup"><span data-stu-id="b80ee-138">On the **SMTP settings** tab, in the **Outgoing mail server** field, enter the FQDN or IP address of your SMTP server or email service.</span></span>
1. <span data-ttu-id="b80ee-139">Do pole **Číslo portu SMTP** zadejte číslo portu.</span><span class="sxs-lookup"><span data-stu-id="b80ee-139">In the **SMTP port number** field, enter the port number.</span></span> <span data-ttu-id="b80ee-140">(Pokud nepoužíváte protokol Secure Sockets Layer \[SSL\], je výchozí číslo portu **25**.)</span><span class="sxs-lookup"><span data-stu-id="b80ee-140">(If you aren't using Secure Sockets Layer \[SSL\], the default port number is **25**.)</span></span>
1. <span data-ttu-id="b80ee-141">Pokud je vyžadováno ověření, zadejte hodnoty do polí **Uživatelské jméno** a **Heslo**.</span><span class="sxs-lookup"><span data-stu-id="b80ee-141">If authentication is required, enter values in the **User name** and **Password** fields.</span></span>
1. <span data-ttu-id="b80ee-142">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="b80ee-142">Select **Save**.</span></span>
1. <span data-ttu-id="b80ee-143">Vyberte **Aktualizovat**.</span><span class="sxs-lookup"><span data-stu-id="b80ee-143">Select **Refresh**.</span></span>
1. <span data-ttu-id="b80ee-144">Na kartě **Testovací e-mail** v poli **Poskytovatel e-mailu** vyberte **SMTP**.</span><span class="sxs-lookup"><span data-stu-id="b80ee-144">On the **Test email** tab, in the **Email provider** field, select **SMTP**.</span></span>
1. <span data-ttu-id="b80ee-145">V poli **Příjemce** zadejte e-mailovou adresu, na kterou má být doručen testovací e-mail.</span><span class="sxs-lookup"><span data-stu-id="b80ee-145">In the **Send to** field, enter the email address that the test email should be delivered to.</span></span>
1. <span data-ttu-id="b80ee-146">Vyberte **Odeslat testovací e-mail**.</span><span class="sxs-lookup"><span data-stu-id="b80ee-146">Select **Send test email**.</span></span>

## <a name="configure-email-templates"></a><span data-ttu-id="b80ee-147">Konfigurace e-mailových šablon</span><span class="sxs-lookup"><span data-stu-id="b80ee-147">Configure email templates</span></span>

<span data-ttu-id="b80ee-148">Pro každou transakční událost, pro kterou chcete odeslat e-maily, musíte aktualizovat e-mailovou šablonu platnou adresou odesílatele.</span><span class="sxs-lookup"><span data-stu-id="b80ee-148">For each transactional event that you want to send emails for, you must update the email template with a valid sender email address.</span></span>

1. <span data-ttu-id="b80ee-149">Přihlaste se do centrály Commerce.</span><span class="sxs-lookup"><span data-stu-id="b80ee-149">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="b80ee-150">Pomocí nabídky v levé části přejděte na **Moduly \> Retail \> Nastavení centrály \> Parametry \> Šablony e-mailu organizace**.</span><span class="sxs-lookup"><span data-stu-id="b80ee-150">Use the menu on the left to go to **Modules \> Retail and Commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="b80ee-151">Vyberte možnost **Zobrazit seznam**.</span><span class="sxs-lookup"><span data-stu-id="b80ee-151">Select **Show list**.</span></span>
1. <span data-ttu-id="b80ee-152">Pro každou šablonu v seznamu postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="b80ee-152">For each template in the list, follow these steps:</span></span>

    1. <span data-ttu-id="b80ee-153">Do pole **Adresa odesílatele** zadejte e-mailovou adresu odesílatele.</span><span class="sxs-lookup"><span data-stu-id="b80ee-153">In the **Sender email** field, enter the sender email address.</span></span>
    1. <span data-ttu-id="b80ee-154">Volitelné: Do pole **Jméno odesílatele** zadejte jméno, které má být použito jako jméno odesílatele.</span><span class="sxs-lookup"><span data-stu-id="b80ee-154">Optional: In the **Sender name** field, enter the name that should be used as the sender name.</span></span>

1. <span data-ttu-id="b80ee-155">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="b80ee-155">Select **Save**.</span></span>

## <a name="customize-email-templates"></a><span data-ttu-id="b80ee-156">Přizpůsobení šablon e-mailu</span><span class="sxs-lookup"><span data-stu-id="b80ee-156">Customize email templates</span></span>

<span data-ttu-id="b80ee-157">Šablony e-mailů je vhodné přizpůsobit tak, aby používaly různé obrázky.</span><span class="sxs-lookup"><span data-stu-id="b80ee-157">You might want to customize the email templates so that they use different images.</span></span> <span data-ttu-id="b80ee-158">Nebo můžete chtít aktualizovat odkazy v šablonách tak, aby byly v prostředí vyhodnocení.</span><span class="sxs-lookup"><span data-stu-id="b80ee-158">Or you might want to update the links in the templates so that they go to your evaluation environment.</span></span> <span data-ttu-id="b80ee-159">Tento postup vysvětluje, jak stáhnout výchozí šablony, přizpůsobit je a aktualizovat šablony v systému.</span><span class="sxs-lookup"><span data-stu-id="b80ee-159">This procedure explains how to download the default templates, customize them, and update the templates in the system.</span></span>

1. <span data-ttu-id="b80ee-160">Ve webovém prohlížeči můžete stáhnout [soubor zip vyhodnocení výchozích šablon e-mailu Microsoft Dynamics 365 Commerce](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) do místního počítače.</span><span class="sxs-lookup"><span data-stu-id="b80ee-160">In a web browser, download the [Microsoft Dynamics 365 Commerce Evaluation default email templates zip file](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) to your local computer.</span></span> <span data-ttu-id="b80ee-161">Tento soubor obsahuje následující dokumenty HTML:</span><span class="sxs-lookup"><span data-stu-id="b80ee-161">This file contains the following HTML documents:</span></span>

    - <span data-ttu-id="b80ee-162">Šablona potvrzení objednávky</span><span class="sxs-lookup"><span data-stu-id="b80ee-162">Order confirmation template</span></span>
    - <span data-ttu-id="b80ee-163">Šablona dárkového poukazu</span><span class="sxs-lookup"><span data-stu-id="b80ee-163">Issue gift card template</span></span>
    - <span data-ttu-id="b80ee-164">Šablona nové objednávky</span><span class="sxs-lookup"><span data-stu-id="b80ee-164">New order template</span></span>
    - <span data-ttu-id="b80ee-165">Šablona objednávky balení</span><span class="sxs-lookup"><span data-stu-id="b80ee-165">Pack order template</span></span>
    - <span data-ttu-id="b80ee-166">Šablona objednávky výdeje</span><span class="sxs-lookup"><span data-stu-id="b80ee-166">Pick order template</span></span>

1. <span data-ttu-id="b80ee-167">Přizpůsobte šablony pomocí textu nebo editoru HTML.</span><span class="sxs-lookup"><span data-stu-id="b80ee-167">Customize the templates by using a text or HTML editor.</span></span> <span data-ttu-id="b80ee-168">Další informace naleznete v části [podporované tokeny](#supported-tokens-in-the-email-template) dále v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="b80ee-168">See the list of [supported tokens](#supported-tokens-in-the-email-template) later in this topic.</span></span>
1. <span data-ttu-id="b80ee-169">Přihlášení do Commerce.</span><span class="sxs-lookup"><span data-stu-id="b80ee-169">Sign in to Commerce.</span></span>
1. <span data-ttu-id="b80ee-170">Pomocí nabídky v levé části přejděte na **Moduly \> Správa organizace \> Nastavení \> Šablony e-mailu organizace**.</span><span class="sxs-lookup"><span data-stu-id="b80ee-170">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="b80ee-171">Rozbalením seznamu v levé části zobrazíte všechny šablony.</span><span class="sxs-lookup"><span data-stu-id="b80ee-171">Expand the list on the left to see all the templates.</span></span>
1. <span data-ttu-id="b80ee-172">U každé šablony, kterou chcete přizpůsobit, postupujte následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="b80ee-172">For each template that you want to customize, follow these steps:</span></span>

    1. <span data-ttu-id="b80ee-173">Vyberte šablonu v seznamu.</span><span class="sxs-lookup"><span data-stu-id="b80ee-173">Select the template in the list.</span></span>
    1. <span data-ttu-id="b80ee-174">V části **Obsah e-mailové zprávy** vyberte odpovídající jazykovou verzi ze seznamu.</span><span class="sxs-lookup"><span data-stu-id="b80ee-174">Under **Email message content**, select the appropriate language version in the list.</span></span> <span data-ttu-id="b80ee-175">(Výchozí kód jazyka je **en-us**.)</span><span class="sxs-lookup"><span data-stu-id="b80ee-175">(The default language is **en-us**.)</span></span>
    1. <span data-ttu-id="b80ee-176">V části **Obsah e-mailové zprávy** vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="b80ee-176">Under **Email message content**, select **Edit**.</span></span> <span data-ttu-id="b80ee-177">Zobrazí se podokno **Odeslat šablonu e-mailu**.</span><span class="sxs-lookup"><span data-stu-id="b80ee-177">The **Upload email template** pane appears.</span></span>
    1. <span data-ttu-id="b80ee-178">Vyberte **Procházet** a najděte soubor HTML, který má přizpůsobený obsah.</span><span class="sxs-lookup"><span data-stu-id="b80ee-178">Select **Browse**, and find the HTML file that has the customized content.</span></span>
    1. <span data-ttu-id="b80ee-179">Vyberte **Odeslat**.</span><span class="sxs-lookup"><span data-stu-id="b80ee-179">Select **Upload**.</span></span> <span data-ttu-id="b80ee-180">Šablona se nahraje do systému a zobrazí se náhled.</span><span class="sxs-lookup"><span data-stu-id="b80ee-180">The template is uploaded into the system, and a preview is shown.</span></span>
    1. <span data-ttu-id="b80ee-181">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="b80ee-181">Select **OK**.</span></span>
    1. <span data-ttu-id="b80ee-182">Volitelné: Upravte vlastnost **Předmět** šablony.</span><span class="sxs-lookup"><span data-stu-id="b80ee-182">Optional: Customize the **Subject** property of the template.</span></span>
    1. <span data-ttu-id="b80ee-183">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="b80ee-183">Select **Save**.</span></span>

### <a name="supported-tokens-in-the-email-template"></a><span data-ttu-id="b80ee-184">Podporované tokeny v šabloně e-mailu</span><span class="sxs-lookup"><span data-stu-id="b80ee-184">Supported tokens in the email template</span></span>

<span data-ttu-id="b80ee-185">Když je e-mail vykreslován, budou tyto tokeny nahrazeny skutečnými hodnotami, které platí pro zákazníka a jeho objednávku.</span><span class="sxs-lookup"><span data-stu-id="b80ee-185">When the email is rendered, these tokens are replaced with actual values that apply to the customer and the customer's order.</span></span>

#### <a name="sales-order"></a><span data-ttu-id="b80ee-186">Prodejní objednávka</span><span class="sxs-lookup"><span data-stu-id="b80ee-186">Sales order</span></span>

<span data-ttu-id="b80ee-187">Následující tokeny se vztahují na celkovou prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="b80ee-187">The following tokens apply to the overall sales order.</span></span>

| <span data-ttu-id="b80ee-188">Název tokenu</span><span class="sxs-lookup"><span data-stu-id="b80ee-188">Name of the token</span></span> | <span data-ttu-id="b80ee-189">Token</span><span class="sxs-lookup"><span data-stu-id="b80ee-189">Token</span></span> |
|-------------------|-------|
| <span data-ttu-id="b80ee-190">Číslo objednávky</span><span class="sxs-lookup"><span data-stu-id="b80ee-190">Order number</span></span>      | <span data-ttu-id="b80ee-191">%salesid%</span><span class="sxs-lookup"><span data-stu-id="b80ee-191">%salesid%</span></span> |
| <span data-ttu-id="b80ee-192">Jméno zákazníka</span><span class="sxs-lookup"><span data-stu-id="b80ee-192">Customer's name</span></span>   | <span data-ttu-id="b80ee-193">%customername%</span><span class="sxs-lookup"><span data-stu-id="b80ee-193">%customername%</span></span> |
| <span data-ttu-id="b80ee-194">Adresa dodání</span><span class="sxs-lookup"><span data-stu-id="b80ee-194">Delivery address</span></span>  | <span data-ttu-id="b80ee-195">%deliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="b80ee-195">%deliveryaddress%</span></span> |
| <span data-ttu-id="b80ee-196">Fakturační adresa</span><span class="sxs-lookup"><span data-stu-id="b80ee-196">Billing address</span></span>   | <span data-ttu-id="b80ee-197">%customeraddress%</span><span class="sxs-lookup"><span data-stu-id="b80ee-197">%customeraddress%</span></span> |
| <span data-ttu-id="b80ee-198">Datum objednávky</span><span class="sxs-lookup"><span data-stu-id="b80ee-198">Order date</span></span>        | <span data-ttu-id="b80ee-199">%shipdate%</span><span class="sxs-lookup"><span data-stu-id="b80ee-199">%shipdate%</span></span> |
| <span data-ttu-id="b80ee-200">Způsob doručení</span><span class="sxs-lookup"><span data-stu-id="b80ee-200">Delivery mode</span></span>     | <span data-ttu-id="b80ee-201">%modeofdelivery%</span><span class="sxs-lookup"><span data-stu-id="b80ee-201">%modeofdelivery%</span></span> |
| <span data-ttu-id="b80ee-202">Sleva</span><span class="sxs-lookup"><span data-stu-id="b80ee-202">Discount</span></span>          | <span data-ttu-id="b80ee-203">%discount%</span><span class="sxs-lookup"><span data-stu-id="b80ee-203">%discount%</span></span> |
| <span data-ttu-id="b80ee-204">DPH</span><span class="sxs-lookup"><span data-stu-id="b80ee-204">Sales tax</span></span>         | <span data-ttu-id="b80ee-205">%tax%</span><span class="sxs-lookup"><span data-stu-id="b80ee-205">%tax%</span></span> |
| <span data-ttu-id="b80ee-206">Celková hodnota objednávky</span><span class="sxs-lookup"><span data-stu-id="b80ee-206">Order total</span></span>       | <span data-ttu-id="b80ee-207">%total%</span><span class="sxs-lookup"><span data-stu-id="b80ee-207">%total%</span></span> |

#### <a name="sales-line"></a><span data-ttu-id="b80ee-208">Řádek prodeje</span><span class="sxs-lookup"><span data-stu-id="b80ee-208">Sales line</span></span>

<span data-ttu-id="b80ee-209">Následující tokeny jsou nahrazeny hodnotami pro každý produkt v objednávce.</span><span class="sxs-lookup"><span data-stu-id="b80ee-209">The following tokens are replaced with values for each product in the order.</span></span>

> [!NOTE]
> <span data-ttu-id="b80ee-210">Token **Product list - start** vložte na začátek bloku HTML, který se opakuje u každého produktu, a token **Product list - end** na konec bloku.</span><span class="sxs-lookup"><span data-stu-id="b80ee-210">Put the **Product list - start** token at the beginning of the HTML block that is repeated for every product, and put the **Product list - end** token at the end of the block.</span></span>

| <span data-ttu-id="b80ee-211">Název tokenu</span><span class="sxs-lookup"><span data-stu-id="b80ee-211">Name of the token</span></span>      | <span data-ttu-id="b80ee-212">Token</span><span class="sxs-lookup"><span data-stu-id="b80ee-212">Token</span></span> |
|------------------------|-------|
| <span data-ttu-id="b80ee-213">Seznam produktů - začátek</span><span class="sxs-lookup"><span data-stu-id="b80ee-213">Product list - start</span></span>   | \<!--%tablebegin.salesline% --\> |
| <span data-ttu-id="b80ee-214">Seznam produktů - konec</span><span class="sxs-lookup"><span data-stu-id="b80ee-214">Product list - end</span></span>     | \<!--%tableend.salesline%--\> |
| <span data-ttu-id="b80ee-215">Název produktu</span><span class="sxs-lookup"><span data-stu-id="b80ee-215">Product name</span></span>           | <span data-ttu-id="b80ee-216">%lineproductname%</span><span class="sxs-lookup"><span data-stu-id="b80ee-216">%lineproductname%</span></span> |
| <span data-ttu-id="b80ee-217">popis</span><span class="sxs-lookup"><span data-stu-id="b80ee-217">Description</span></span>            | <span data-ttu-id="b80ee-218">%lineproductdescription%</span><span class="sxs-lookup"><span data-stu-id="b80ee-218">%lineproductdescription%</span></span> |
| <span data-ttu-id="b80ee-219">Množství</span><span class="sxs-lookup"><span data-stu-id="b80ee-219">Quantity</span></span>               | <span data-ttu-id="b80ee-220">%linequantity%</span><span class="sxs-lookup"><span data-stu-id="b80ee-220">%linequantity%</span></span> |
| <span data-ttu-id="b80ee-221">Cena řádkové jednotky</span><span class="sxs-lookup"><span data-stu-id="b80ee-221">Line unit price</span></span>        | <span data-ttu-id="b80ee-222">%lineprice% (ověřit)</span><span class="sxs-lookup"><span data-stu-id="b80ee-222">%lineprice% (verify)</span></span> |
| <span data-ttu-id="b80ee-223">celkem řádkových položek</span><span class="sxs-lookup"><span data-stu-id="b80ee-223">line item total</span></span>        | <span data-ttu-id="b80ee-224">%linenetamount%</span><span class="sxs-lookup"><span data-stu-id="b80ee-224">%linenetamount%</span></span> |
| <span data-ttu-id="b80ee-225">řádková sleva</span><span class="sxs-lookup"><span data-stu-id="b80ee-225">line discount</span></span>          | <span data-ttu-id="b80ee-226">%linediscount%</span><span class="sxs-lookup"><span data-stu-id="b80ee-226">%linediscount%</span></span> |
| <span data-ttu-id="b80ee-227">Datum expedice</span><span class="sxs-lookup"><span data-stu-id="b80ee-227">Ship date</span></span>              | <span data-ttu-id="b80ee-228">%lineshipdate%</span><span class="sxs-lookup"><span data-stu-id="b80ee-228">%lineshipdate%</span></span> |
| <span data-ttu-id="b80ee-229">Způsob zásobování</span><span class="sxs-lookup"><span data-stu-id="b80ee-229">Procurement method</span></span>     | <span data-ttu-id="b80ee-230">%linedeliverymode%</span><span class="sxs-lookup"><span data-stu-id="b80ee-230">%linedeliverymode%</span></span> |
| <span data-ttu-id="b80ee-231">adresa dodání</span><span class="sxs-lookup"><span data-stu-id="b80ee-231">delivery address</span></span>       | <span data-ttu-id="b80ee-232">%linedeliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="b80ee-232">%linedeliveryaddress%</span></span> |
| <span data-ttu-id="b80ee-233">Prodejní jednotka řádku</span><span class="sxs-lookup"><span data-stu-id="b80ee-233">Sales unit of the line</span></span> | <span data-ttu-id="b80ee-234">%lineunit%</span><span class="sxs-lookup"><span data-stu-id="b80ee-234">%lineunit%</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="b80ee-235">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="b80ee-235">Additional resources</span></span>

[<span data-ttu-id="b80ee-236">Přehled prostředí vyhodnocení Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="b80ee-236">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="b80ee-237">Zřízení prostředí vyhodnocení Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="b80ee-237">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="b80ee-238">Konfigurace prostředí vyhodnocení Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="b80ee-238">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="b80ee-239">Konfigurovat BOPIS v prostředí vyhodnocení Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="b80ee-239">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="b80ee-240">Časté otázky týkající se prostředí vyhodnocení Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="b80ee-240">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="b80ee-241">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="b80ee-241">Microsoft Lifecycle Services (LCS)</span></span>](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="b80ee-242">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="b80ee-242">Retail Cloud Scale Unit (RCSU)</span></span>](/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="b80ee-243">Portál Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="b80ee-243">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="b80ee-244">Web Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="b80ee-244">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]