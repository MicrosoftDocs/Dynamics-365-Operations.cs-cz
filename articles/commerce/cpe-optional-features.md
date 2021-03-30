---
title: Konfigurace volitelných funkcí pro prostředí vyhodnocení aplikace Dynamics 365 Commerce
description: Toto téma vysvětluje, jak konfigurovat volitelné funkce prostředí vyhodnocení Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: def99a34404357e28501de5ccf11c6130d53f34f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213811"
---
# <a name="configure-optional-features-for-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="e4584-103">Konfigurace volitelných funkcí pro prostředí vyhodnocení aplikace Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="e4584-103">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e4584-104">Toto téma vysvětluje, jak konfigurovat volitelné funkce prostředí vyhodnocení Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="e4584-104">This topic explains how to configure optional features for a Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e4584-105">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="e4584-105">Prerequisites</span></span>

<span data-ttu-id="e4584-106">Chcete-li vyhodnotit funkce transakčního e-mailu, musí být splněny následující předpoklady:</span><span class="sxs-lookup"><span data-stu-id="e4584-106">If you want to evaluate the transactional email features, the following prerequisites must be met:</span></span>

- <span data-ttu-id="e4584-107">Máte k dispozici e-mailový server (Simple Mail Transfer Protocol \[SMTP\]), který lze použít z předplatného Microsoft Azure, kde jste zřídili prostředí vyhodnocení.</span><span class="sxs-lookup"><span data-stu-id="e4584-107">You have an available email server (Simple Mail Transfer Protocol \[SMTP\] server) that can be used from the Microsoft Azure subscription where you provisioned the evaluation environment.</span></span>
- <span data-ttu-id="e4584-108">Máte k dispozici plně kvalifikovaný název domény (FQDN)/IP adresu, číslo portu SMTP a podrobnosti o ověřování.</span><span class="sxs-lookup"><span data-stu-id="e4584-108">You have the server's fully qualified domain name (FQDN)/IP address, SMTP port number, and authentication details available.</span></span>

## <a name="configure-the-image-back-end"></a><span data-ttu-id="e4584-109">Konfigurace back-endu bitové kopie</span><span class="sxs-lookup"><span data-stu-id="e4584-109">Configure the image back end</span></span>

### <a name="find-your-media-base-url"></a><span data-ttu-id="e4584-110">Hledání základní adresy URL média</span><span class="sxs-lookup"><span data-stu-id="e4584-110">Find your media base URL</span></span>

> [!NOTE]
> <span data-ttu-id="e4584-111">Před provedením tohoto postupu je třeba provést kroky uvedené v tématu [nastavení webu v Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span><span class="sxs-lookup"><span data-stu-id="e4584-111">Before you can complete this procedure, you must complete the steps in [Set up your site in Commerce](cpe-post-provisioning.md#set-up-your-site-in-commerce).</span></span>

1. <span data-ttu-id="e4584-112">Přihlaste se k nástroji pro tvorbu webu Commerce pomocí adresy URL, kterou jste si poznamenali při inicializaci e-Commerce během zřizování (viz [Inicializace e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="e4584-112">Sign in to the Commerce site builder by using the URL you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="e4584-113">Otevřete stránku **Fabrikam**.</span><span class="sxs-lookup"><span data-stu-id="e4584-113">Open the **Fabrikam** site.</span></span>
1. <span data-ttu-id="e4584-114">V nabídce vlevo vyberte **Mediální knihovna**.</span><span class="sxs-lookup"><span data-stu-id="e4584-114">On the menu on the left, select **Media Library**.</span></span>
1. <span data-ttu-id="e4584-115">Vyberte libovolný obrázek.</span><span class="sxs-lookup"><span data-stu-id="e4584-115">Select any single image asset.</span></span>
1. <span data-ttu-id="e4584-116">V inspektoru vlastnosti vpravo najděte vlastnost **Veřejná adresa URL**.</span><span class="sxs-lookup"><span data-stu-id="e4584-116">In the property inspector on the right, find the **Public URL** property.</span></span> <span data-ttu-id="e4584-117">Hodnota je URL.</span><span class="sxs-lookup"><span data-stu-id="e4584-117">The value is a URL.</span></span> <span data-ttu-id="e4584-118">Následuje příklad:</span><span class="sxs-lookup"><span data-stu-id="e4584-118">Here is an example:</span></span>

    <span data-ttu-id="e4584-119">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span><span class="sxs-lookup"><span data-stu-id="e4584-119">`https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/MA1nQC`.</span></span>

1. <span data-ttu-id="e4584-120">Nahraďte poslední identifikátor v adrese URL (**MA1nQC** v předchozím příkladu) s řetězcem **search?fileName=**.</span><span class="sxs-lookup"><span data-stu-id="e4584-120">Replace the last identifier in the URL (**MA1nQC** in the preceding example) with the string **search?fileName=**.</span></span> <span data-ttu-id="e4584-121">Takto vypadá adresa URL po provedení této změny:</span><span class="sxs-lookup"><span data-stu-id="e4584-121">Here is what the example URL looks like after this change is made:</span></span>

    `https://images-us-sb.cms.commerce.dynamics.com/cms/api/fabrikam/imageFileData/search?fileName=`

    <span data-ttu-id="e4584-122">Tato adresa URL je základní adresa URL média.</span><span class="sxs-lookup"><span data-stu-id="e4584-122">This URL is your media base URL.</span></span> <span data-ttu-id="e4584-123">Poznamenejte si ji.</span><span class="sxs-lookup"><span data-stu-id="e4584-123">Make a note of it.</span></span>

### <a name="update-the-media-base-url"></a><span data-ttu-id="e4584-124">Aktualizace základní adresy URL média</span><span class="sxs-lookup"><span data-stu-id="e4584-124">Update the media base URL</span></span>

1. <span data-ttu-id="e4584-125">Přihlaste se do centrály Commerce.</span><span class="sxs-lookup"><span data-stu-id="e4584-125">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="e4584-126">Pomocí nabídky v levé části přejděte na **Moduly \> Retail and commerce \> Nastavení kanálu \> Profily kanálu**.</span><span class="sxs-lookup"><span data-stu-id="e4584-126">Use the menu on the left to go to **Modules \> Retail and commerce \> Channel setup \> Channel profiles**.</span></span>
1. <span data-ttu-id="e4584-127">Vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="e4584-127">Select **Edit**.</span></span>
1. <span data-ttu-id="e4584-128">V části **Vlastnosti profilu** nahraďte hodnotu vlastnosti **Základní adresa URL serveru médií** základní adresou URL médií, kterou jste vytvořili dříve.</span><span class="sxs-lookup"><span data-stu-id="e4584-128">Under **Profile properties**, replace the value for the **Media Server Base URL** property with the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="e4584-129">Vyberte kanál, který je nazvaný **scXXXXXXXXX**.</span><span class="sxs-lookup"><span data-stu-id="e4584-129">Select the channel that is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="e4584-130">Ve **Vlastnostech profilu** vyberte **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="e4584-130">Under **Profile properties**, select **Add**.</span></span>
1. <span data-ttu-id="e4584-131">U vlastnosti, která byla přidána, vyberte **Základní adresa URL serveru médií** jako klíč vlastnosti.</span><span class="sxs-lookup"><span data-stu-id="e4584-131">For the property that was added, select **Media Server Base URL** as the property key.</span></span> <span data-ttu-id="e4584-132">Jako hodnotu vlastnosti zadejte adresu URL základních médií, kterou jste vytvořili dříve.</span><span class="sxs-lookup"><span data-stu-id="e4584-132">As the property value, enter the media base URL that you created earlier.</span></span>
1. <span data-ttu-id="e4584-133">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="e4584-133">Select **Save**.</span></span>

## <a name="configure-and-test-the-email-server"></a><span data-ttu-id="e4584-134">Konfigurace a test e-mailového serveru</span><span class="sxs-lookup"><span data-stu-id="e4584-134">Configure and test the email server</span></span>

> [!NOTE]
> <span data-ttu-id="e4584-135">Server SMTP nebo zadaná e-mailová služba musí být v rámci předplatného Azure, které používáte pro dané prostředí, přístupné.</span><span class="sxs-lookup"><span data-stu-id="e4584-135">The SMTP server or email service that you enter here must be accessible from the Azure subscription that you're using for the environment.</span></span>

1. <span data-ttu-id="e4584-136">Přihlaste se do centrály Commerce.</span><span class="sxs-lookup"><span data-stu-id="e4584-136">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="e4584-137">Pomocí nabídky v levé části přejděte na **Moduly \> Retail \> Nastavení centrály \> Parametry \> Parametry e-mailu**.</span><span class="sxs-lookup"><span data-stu-id="e4584-137">Use the menu on the left to go to **Modules \> Retail and Commerce \> Headquarters setup \> Parameters \> Email parameters**.</span></span>
1. <span data-ttu-id="e4584-138">Na kartě **Nastavení SMTP** do pole **Server odchozí pošty** zadejte FQDN nebo IP adresu serveru SMTP nebo e-mailové služby.</span><span class="sxs-lookup"><span data-stu-id="e4584-138">On the **SMTP settings** tab, in the **Outgoing mail server** field, enter the FQDN or IP address of your SMTP server or email service.</span></span>
1. <span data-ttu-id="e4584-139">Do pole **Číslo portu SMTP** zadejte číslo portu.</span><span class="sxs-lookup"><span data-stu-id="e4584-139">In the **SMTP port number** field, enter the port number.</span></span> <span data-ttu-id="e4584-140">(Pokud nepoužíváte protokol Secure Sockets Layer \[SSL\], je výchozí číslo portu **25**.)</span><span class="sxs-lookup"><span data-stu-id="e4584-140">(If you aren't using Secure Sockets Layer \[SSL\], the default port number is **25**.)</span></span>
1. <span data-ttu-id="e4584-141">Pokud je vyžadováno ověření, zadejte hodnoty do polí **Uživatelské jméno** a **Heslo**.</span><span class="sxs-lookup"><span data-stu-id="e4584-141">If authentication is required, enter values in the **User name** and **Password** fields.</span></span>
1. <span data-ttu-id="e4584-142">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="e4584-142">Select **Save**.</span></span>
1. <span data-ttu-id="e4584-143">Vyberte **Aktualizovat**.</span><span class="sxs-lookup"><span data-stu-id="e4584-143">Select **Refresh**.</span></span>
1. <span data-ttu-id="e4584-144">Na kartě **Testovací e-mail** v poli **Poskytovatel e-mailu** vyberte **SMTP**.</span><span class="sxs-lookup"><span data-stu-id="e4584-144">On the **Test email** tab, in the **Email provider** field, select **SMTP**.</span></span>
1. <span data-ttu-id="e4584-145">V poli **Příjemce** zadejte e-mailovou adresu, na kterou má být doručen testovací e-mail.</span><span class="sxs-lookup"><span data-stu-id="e4584-145">In the **Send to** field, enter the email address that the test email should be delivered to.</span></span>
1. <span data-ttu-id="e4584-146">Vyberte **Odeslat testovací e-mail**.</span><span class="sxs-lookup"><span data-stu-id="e4584-146">Select **Send test email**.</span></span>

## <a name="configure-email-templates"></a><span data-ttu-id="e4584-147">Konfigurace e-mailových šablon</span><span class="sxs-lookup"><span data-stu-id="e4584-147">Configure email templates</span></span>

<span data-ttu-id="e4584-148">Pro každou transakční událost, pro kterou chcete odeslat e-maily, musíte aktualizovat e-mailovou šablonu platnou adresou odesílatele.</span><span class="sxs-lookup"><span data-stu-id="e4584-148">For each transactional event that you want to send emails for, you must update the email template with a valid sender email address.</span></span>

1. <span data-ttu-id="e4584-149">Přihlaste se do centrály Commerce.</span><span class="sxs-lookup"><span data-stu-id="e4584-149">Sign in to Commerce headquarters.</span></span>
1. <span data-ttu-id="e4584-150">Pomocí nabídky v levé části přejděte na **Moduly \> Retail \> Nastavení centrály \> Parametry \> Šablony e-mailu organizace**.</span><span class="sxs-lookup"><span data-stu-id="e4584-150">Use the menu on the left to go to **Modules \> Retail and Commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="e4584-151">Vyberte možnost **Zobrazit seznam**.</span><span class="sxs-lookup"><span data-stu-id="e4584-151">Select **Show list**.</span></span>
1. <span data-ttu-id="e4584-152">Pro každou šablonu v seznamu postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="e4584-152">For each template in the list, follow these steps:</span></span>

    1. <span data-ttu-id="e4584-153">Do pole **Adresa odesílatele** zadejte e-mailovou adresu odesílatele.</span><span class="sxs-lookup"><span data-stu-id="e4584-153">In the **Sender email** field, enter the sender email address.</span></span>
    1. <span data-ttu-id="e4584-154">Volitelné: Do pole **Jméno odesílatele** zadejte jméno, které má být použito jako jméno odesílatele.</span><span class="sxs-lookup"><span data-stu-id="e4584-154">Optional: In the **Sender name** field, enter the name that should be used as the sender name.</span></span>

1. <span data-ttu-id="e4584-155">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="e4584-155">Select **Save**.</span></span>

## <a name="customize-email-templates"></a><span data-ttu-id="e4584-156">Přizpůsobení šablon e-mailu</span><span class="sxs-lookup"><span data-stu-id="e4584-156">Customize email templates</span></span>

<span data-ttu-id="e4584-157">Šablony e-mailů je vhodné přizpůsobit tak, aby používaly různé obrázky.</span><span class="sxs-lookup"><span data-stu-id="e4584-157">You might want to customize the email templates so that they use different images.</span></span> <span data-ttu-id="e4584-158">Nebo můžete chtít aktualizovat odkazy v šablonách tak, aby byly v prostředí vyhodnocení.</span><span class="sxs-lookup"><span data-stu-id="e4584-158">Or you might want to update the links in the templates so that they go to your evaluation environment.</span></span> <span data-ttu-id="e4584-159">Tento postup vysvětluje, jak stáhnout výchozí šablony, přizpůsobit je a aktualizovat šablony v systému.</span><span class="sxs-lookup"><span data-stu-id="e4584-159">This procedure explains how to download the default templates, customize them, and update the templates in the system.</span></span>

1. <span data-ttu-id="e4584-160">Ve webovém prohlížeči můžete stáhnout [soubor zip vyhodnocení výchozích šablon e-mailu Microsoft Dynamics 365 Commerce](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) do místního počítače.</span><span class="sxs-lookup"><span data-stu-id="e4584-160">In a web browser, download the [Microsoft Dynamics 365 Commerce Evaluation default email templates zip file](https://download.microsoft.com/download/d/7/b/d7b6c4d4-fe09-4922-9551-46bbb29d202d/Commerce.Preview.Default.Email.Templates.zip) to your local computer.</span></span> <span data-ttu-id="e4584-161">Tento soubor obsahuje následující dokumenty HTML:</span><span class="sxs-lookup"><span data-stu-id="e4584-161">This file contains the following HTML documents:</span></span>

    - <span data-ttu-id="e4584-162">Šablona potvrzení objednávky</span><span class="sxs-lookup"><span data-stu-id="e4584-162">Order confirmation template</span></span>
    - <span data-ttu-id="e4584-163">Šablona dárkového poukazu</span><span class="sxs-lookup"><span data-stu-id="e4584-163">Issue gift card template</span></span>
    - <span data-ttu-id="e4584-164">Šablona nové objednávky</span><span class="sxs-lookup"><span data-stu-id="e4584-164">New order template</span></span>
    - <span data-ttu-id="e4584-165">Šablona objednávky balení</span><span class="sxs-lookup"><span data-stu-id="e4584-165">Pack order template</span></span>
    - <span data-ttu-id="e4584-166">Šablona objednávky výdeje</span><span class="sxs-lookup"><span data-stu-id="e4584-166">Pick order template</span></span>

1. <span data-ttu-id="e4584-167">Přizpůsobte šablony pomocí textu nebo editoru HTML.</span><span class="sxs-lookup"><span data-stu-id="e4584-167">Customize the templates by using a text or HTML editor.</span></span> <span data-ttu-id="e4584-168">Další informace naleznete v části [podporované tokeny](#supported-tokens-in-the-email-template) dále v tomto tématu.</span><span class="sxs-lookup"><span data-stu-id="e4584-168">See the list of [supported tokens](#supported-tokens-in-the-email-template) later in this topic.</span></span>
1. <span data-ttu-id="e4584-169">Přihlášení do Commerce.</span><span class="sxs-lookup"><span data-stu-id="e4584-169">Sign in to Commerce.</span></span>
1. <span data-ttu-id="e4584-170">Pomocí nabídky v levé části přejděte na **Moduly \> Správa organizace \> Nastavení \> Šablony e-mailu organizace**.</span><span class="sxs-lookup"><span data-stu-id="e4584-170">Use the menu on the left to go to **Modules \> Organization administration \> Setup \> Organization email templates**.</span></span>
1. <span data-ttu-id="e4584-171">Rozbalením seznamu v levé části zobrazíte všechny šablony.</span><span class="sxs-lookup"><span data-stu-id="e4584-171">Expand the list on the left to see all the templates.</span></span>
1. <span data-ttu-id="e4584-172">U každé šablony, kterou chcete přizpůsobit, postupujte následujícím způsobem:</span><span class="sxs-lookup"><span data-stu-id="e4584-172">For each template that you want to customize, follow these steps:</span></span>

    1. <span data-ttu-id="e4584-173">Vyberte šablonu v seznamu.</span><span class="sxs-lookup"><span data-stu-id="e4584-173">Select the template in the list.</span></span>
    1. <span data-ttu-id="e4584-174">V části **Obsah e-mailové zprávy** vyberte odpovídající jazykovou verzi ze seznamu.</span><span class="sxs-lookup"><span data-stu-id="e4584-174">Under **Email message content**, select the appropriate language version in the list.</span></span> <span data-ttu-id="e4584-175">(Výchozí kód jazyka je **en-us**.)</span><span class="sxs-lookup"><span data-stu-id="e4584-175">(The default language is **en-us**.)</span></span>
    1. <span data-ttu-id="e4584-176">V části **Obsah e-mailové zprávy** vyberte **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="e4584-176">Under **Email message content**, select **Edit**.</span></span> <span data-ttu-id="e4584-177">Zobrazí se podokno **Odeslat šablonu e-mailu**.</span><span class="sxs-lookup"><span data-stu-id="e4584-177">The **Upload email template** pane appears.</span></span>
    1. <span data-ttu-id="e4584-178">Vyberte **Procházet** a najděte soubor HTML, který má přizpůsobený obsah.</span><span class="sxs-lookup"><span data-stu-id="e4584-178">Select **Browse**, and find the HTML file that has the customized content.</span></span>
    1. <span data-ttu-id="e4584-179">Vyberte **Odeslat**.</span><span class="sxs-lookup"><span data-stu-id="e4584-179">Select **Upload**.</span></span> <span data-ttu-id="e4584-180">Šablona se nahraje do systému a zobrazí se náhled.</span><span class="sxs-lookup"><span data-stu-id="e4584-180">The template is uploaded into the system, and a preview is shown.</span></span>
    1. <span data-ttu-id="e4584-181">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="e4584-181">Select **OK**.</span></span>
    1. <span data-ttu-id="e4584-182">Volitelné: Upravte vlastnost **Předmět** šablony.</span><span class="sxs-lookup"><span data-stu-id="e4584-182">Optional: Customize the **Subject** property of the template.</span></span>
    1. <span data-ttu-id="e4584-183">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="e4584-183">Select **Save**.</span></span>

### <a name="supported-tokens-in-the-email-template"></a><span data-ttu-id="e4584-184">Podporované tokeny v šabloně e-mailu</span><span class="sxs-lookup"><span data-stu-id="e4584-184">Supported tokens in the email template</span></span>

<span data-ttu-id="e4584-185">Když je e-mail vykreslován, budou tyto tokeny nahrazeny skutečnými hodnotami, které platí pro zákazníka a jeho objednávku.</span><span class="sxs-lookup"><span data-stu-id="e4584-185">When the email is rendered, these tokens are replaced with actual values that apply to the customer and the customer's order.</span></span>

#### <a name="sales-order"></a><span data-ttu-id="e4584-186">Prodejní objednávka</span><span class="sxs-lookup"><span data-stu-id="e4584-186">Sales order</span></span>

<span data-ttu-id="e4584-187">Následující tokeny se vztahují na celkovou prodejní objednávku.</span><span class="sxs-lookup"><span data-stu-id="e4584-187">The following tokens apply to the overall sales order.</span></span>

| <span data-ttu-id="e4584-188">Název tokenu</span><span class="sxs-lookup"><span data-stu-id="e4584-188">Name of the token</span></span> | <span data-ttu-id="e4584-189">Token</span><span class="sxs-lookup"><span data-stu-id="e4584-189">Token</span></span> |
|-------------------|-------|
| <span data-ttu-id="e4584-190">Číslo objednávky</span><span class="sxs-lookup"><span data-stu-id="e4584-190">Order number</span></span>      | <span data-ttu-id="e4584-191">%salesid%</span><span class="sxs-lookup"><span data-stu-id="e4584-191">%salesid%</span></span> |
| <span data-ttu-id="e4584-192">Jméno zákazníka</span><span class="sxs-lookup"><span data-stu-id="e4584-192">Customer's name</span></span>   | <span data-ttu-id="e4584-193">%customername%</span><span class="sxs-lookup"><span data-stu-id="e4584-193">%customername%</span></span> |
| <span data-ttu-id="e4584-194">Adresa dodání</span><span class="sxs-lookup"><span data-stu-id="e4584-194">Delivery address</span></span>  | <span data-ttu-id="e4584-195">%deliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="e4584-195">%deliveryaddress%</span></span> |
| <span data-ttu-id="e4584-196">Fakturační adresa</span><span class="sxs-lookup"><span data-stu-id="e4584-196">Billing address</span></span>   | <span data-ttu-id="e4584-197">%customeraddress%</span><span class="sxs-lookup"><span data-stu-id="e4584-197">%customeraddress%</span></span> |
| <span data-ttu-id="e4584-198">Datum objednávky</span><span class="sxs-lookup"><span data-stu-id="e4584-198">Order date</span></span>        | <span data-ttu-id="e4584-199">%shipdate%</span><span class="sxs-lookup"><span data-stu-id="e4584-199">%shipdate%</span></span> |
| <span data-ttu-id="e4584-200">Způsob doručení</span><span class="sxs-lookup"><span data-stu-id="e4584-200">Delivery mode</span></span>     | <span data-ttu-id="e4584-201">%modeofdelivery%</span><span class="sxs-lookup"><span data-stu-id="e4584-201">%modeofdelivery%</span></span> |
| <span data-ttu-id="e4584-202">Sleva</span><span class="sxs-lookup"><span data-stu-id="e4584-202">Discount</span></span>          | <span data-ttu-id="e4584-203">%discount%</span><span class="sxs-lookup"><span data-stu-id="e4584-203">%discount%</span></span> |
| <span data-ttu-id="e4584-204">DPH</span><span class="sxs-lookup"><span data-stu-id="e4584-204">Sales tax</span></span>         | <span data-ttu-id="e4584-205">%tax%</span><span class="sxs-lookup"><span data-stu-id="e4584-205">%tax%</span></span> |
| <span data-ttu-id="e4584-206">Celková hodnota objednávky</span><span class="sxs-lookup"><span data-stu-id="e4584-206">Order total</span></span>       | <span data-ttu-id="e4584-207">%total%</span><span class="sxs-lookup"><span data-stu-id="e4584-207">%total%</span></span> |

#### <a name="sales-line"></a><span data-ttu-id="e4584-208">Řádek prodeje</span><span class="sxs-lookup"><span data-stu-id="e4584-208">Sales line</span></span>

<span data-ttu-id="e4584-209">Následující tokeny jsou nahrazeny hodnotami pro každý produkt v objednávce.</span><span class="sxs-lookup"><span data-stu-id="e4584-209">The following tokens are replaced with values for each product in the order.</span></span>

> [!NOTE]
> <span data-ttu-id="e4584-210">Token **Product list - start** vložte na začátek bloku HTML, který se opakuje u každého produktu, a token **Product list - end** na konec bloku.</span><span class="sxs-lookup"><span data-stu-id="e4584-210">Put the **Product list - start** token at the beginning of the HTML block that is repeated for every product, and put the **Product list - end** token at the end of the block.</span></span>

| <span data-ttu-id="e4584-211">Název tokenu</span><span class="sxs-lookup"><span data-stu-id="e4584-211">Name of the token</span></span>      | <span data-ttu-id="e4584-212">Token</span><span class="sxs-lookup"><span data-stu-id="e4584-212">Token</span></span> |
|------------------------|-------|
| <span data-ttu-id="e4584-213">Seznam produktů - začátek</span><span class="sxs-lookup"><span data-stu-id="e4584-213">Product list - start</span></span>   | \<!--%tablebegin.salesline% --\> |
| <span data-ttu-id="e4584-214">Seznam produktů - konec</span><span class="sxs-lookup"><span data-stu-id="e4584-214">Product list - end</span></span>     | \<!--%tableend.salesline%--\> |
| <span data-ttu-id="e4584-215">Název produktu</span><span class="sxs-lookup"><span data-stu-id="e4584-215">Product name</span></span>           | <span data-ttu-id="e4584-216">%lineproductname%</span><span class="sxs-lookup"><span data-stu-id="e4584-216">%lineproductname%</span></span> |
| <span data-ttu-id="e4584-217">popis</span><span class="sxs-lookup"><span data-stu-id="e4584-217">Description</span></span>            | <span data-ttu-id="e4584-218">%lineproductdescription%</span><span class="sxs-lookup"><span data-stu-id="e4584-218">%lineproductdescription%</span></span> |
| <span data-ttu-id="e4584-219">Množství</span><span class="sxs-lookup"><span data-stu-id="e4584-219">Quantity</span></span>               | <span data-ttu-id="e4584-220">%linequantity%</span><span class="sxs-lookup"><span data-stu-id="e4584-220">%linequantity%</span></span> |
| <span data-ttu-id="e4584-221">Cena řádkové jednotky</span><span class="sxs-lookup"><span data-stu-id="e4584-221">Line unit price</span></span>        | <span data-ttu-id="e4584-222">%lineprice% (ověřit)</span><span class="sxs-lookup"><span data-stu-id="e4584-222">%lineprice% (verify)</span></span> |
| <span data-ttu-id="e4584-223">celkem řádkových položek</span><span class="sxs-lookup"><span data-stu-id="e4584-223">line item total</span></span>        | <span data-ttu-id="e4584-224">%linenetamount%</span><span class="sxs-lookup"><span data-stu-id="e4584-224">%linenetamount%</span></span> |
| <span data-ttu-id="e4584-225">řádková sleva</span><span class="sxs-lookup"><span data-stu-id="e4584-225">line discount</span></span>          | <span data-ttu-id="e4584-226">%linediscount%</span><span class="sxs-lookup"><span data-stu-id="e4584-226">%linediscount%</span></span> |
| <span data-ttu-id="e4584-227">Datum expedice</span><span class="sxs-lookup"><span data-stu-id="e4584-227">Ship date</span></span>              | <span data-ttu-id="e4584-228">%lineshipdate%</span><span class="sxs-lookup"><span data-stu-id="e4584-228">%lineshipdate%</span></span> |
| <span data-ttu-id="e4584-229">Způsob zásobování</span><span class="sxs-lookup"><span data-stu-id="e4584-229">Procurement method</span></span>     | <span data-ttu-id="e4584-230">%linedeliverymode%</span><span class="sxs-lookup"><span data-stu-id="e4584-230">%linedeliverymode%</span></span> |
| <span data-ttu-id="e4584-231">adresa dodání</span><span class="sxs-lookup"><span data-stu-id="e4584-231">delivery address</span></span>       | <span data-ttu-id="e4584-232">%linedeliveryaddress%</span><span class="sxs-lookup"><span data-stu-id="e4584-232">%linedeliveryaddress%</span></span> |
| <span data-ttu-id="e4584-233">Prodejní jednotka řádku</span><span class="sxs-lookup"><span data-stu-id="e4584-233">Sales unit of the line</span></span> | <span data-ttu-id="e4584-234">%lineunit%</span><span class="sxs-lookup"><span data-stu-id="e4584-234">%lineunit%</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="e4584-235">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="e4584-235">Additional resources</span></span>

[<span data-ttu-id="e4584-236">Přehled prostředí vyhodnocení Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="e4584-236">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="e4584-237">Zřízení prostředí vyhodnocení Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="e4584-237">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="e4584-238">Konfigurace prostředí vyhodnocení Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="e4584-238">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="e4584-239">Konfigurovat BOPIS v prostředí vyhodnocení Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="e4584-239">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="e4584-240">Časté otázky týkající se prostředí vyhodnocení Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="e4584-240">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="e4584-241">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="e4584-241">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="e4584-242">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="e4584-242">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="e4584-243">Portál Microsoft Azure</span><span class="sxs-lookup"><span data-stu-id="e4584-243">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="e4584-244">Web Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="e4584-244">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]