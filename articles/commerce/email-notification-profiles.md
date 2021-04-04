---
title: Nastavení profilu oznámení e-mailem
description: Toto téma popisuje, jak vytvořit profil oznámení e-mailem v aplikaci Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: annbe
ms.date: 03/01/2021
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
ms.openlocfilehash: d82a1abe68ff6e162acb75c6fdc1e207af11c279
ms.sourcegitcommit: 88babb2fffe97e93bbde543633fc492120f2a4fc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/06/2021
ms.locfileid: "5555300"
---
# <a name="set-up-an-email-notification-profile"></a><span data-ttu-id="a6bc0-103">Nastavení profilu oznámení e-mailem</span><span class="sxs-lookup"><span data-stu-id="a6bc0-103">Set up an email notification profile</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a6bc0-104">Toto téma popisuje, jak vytvořit profil oznámení e-mailem v aplikaci Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a6bc0-104">This topic describes how to create an email notification profile in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="a6bc0-105">Při vytváření kanálů můžete nastavit e-mailový oznamovací profil.</span><span class="sxs-lookup"><span data-stu-id="a6bc0-105">When you create channels, you can set up an email notification profile.</span></span> <span data-ttu-id="a6bc0-106">Tímto způsobem mohou být e-maily zasílány zákazníkům ohledně různých transakčních událostí, jako je vytvoření objednávky, stav odeslání objednávky a selhání platby.</span><span class="sxs-lookup"><span data-stu-id="a6bc0-106">In that way, emails can be sent to customers for various transactional events, such as order creation, order shipping status, and payment failure.</span></span>

<span data-ttu-id="a6bc0-107">Další informace o konfiguraci e-mailu naleznete v tématu [Konfigurace a odesílání e-mailu](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="a6bc0-107">For additional email configuration information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="create-an-email-notification-profile"></a><span data-ttu-id="a6bc0-108">Vytvoření profilu oznámení e-mailem</span><span class="sxs-lookup"><span data-stu-id="a6bc0-108">Create an email notification profile</span></span>

<span data-ttu-id="a6bc0-109">Chcete-li vytvořit profil oznámení e-mailem, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="a6bc0-109">To create an email notification profile, follow these steps.</span></span>

1. <span data-ttu-id="a6bc0-110">V navigačním podokně přejděte na **Moduly \> Maloobchodní a velkoobchodní prodej \> Nastavení centrály \> Profil oznámení e-mailem aplikace Commerce**.</span><span class="sxs-lookup"><span data-stu-id="a6bc0-110">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="a6bc0-111">V podokně akcí klikněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="a6bc0-111">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="a6bc0-112">Do pole **Profil oznámení e-mailem** zadejte název pro identifikaci profilu.</span><span class="sxs-lookup"><span data-stu-id="a6bc0-112">In the **Email notification profile** field, enter a name to identify the profile.</span></span>
1. <span data-ttu-id="a6bc0-113">Zadejte příslušný popis do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="a6bc0-113">In the **Description** field, enter a relevant description.</span></span>
1. <span data-ttu-id="a6bc0-114">Nastavení přepínač **Aktivní** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="a6bc0-114">Set the **Active** switch to **Yes**.</span></span>

### <a name="create-an-email-template"></a><span data-ttu-id="a6bc0-115">Vytvoření šablonu e-mailu</span><span class="sxs-lookup"><span data-stu-id="a6bc0-115">Create an email template</span></span>

<span data-ttu-id="a6bc0-116">Než bude možné povolit typ e-mailového oznámení, musíte vytvořit šablonu e-mailu organizace v centrále Commerce.</span><span class="sxs-lookup"><span data-stu-id="a6bc0-116">Before an email notification type can be enabled, you must create an organization email template in Commerce headquarters.</span></span> <span data-ttu-id="a6bc0-117">Tato šablona definuje předmět e-mailu, odesílatele, výchozí jazyk a tělo e-mailu pro každý jazyk, který chcete podporovat.</span><span class="sxs-lookup"><span data-stu-id="a6bc0-117">This template defines the email subject, sender, default language, and email body for each language that you want to support.</span></span>

<span data-ttu-id="a6bc0-118">Šablonu e-mailu vytvoříte takto:</span><span class="sxs-lookup"><span data-stu-id="a6bc0-118">To create an email template, follow these steps.</span></span>

1. <span data-ttu-id="a6bc0-119">V navigačním podokně přejděte na **Moduly \> Maloobchodní a velkoobchodní prodej \> Nastavení centrály \> Parametry \> E-mailové šablony organizace**.</span><span class="sxs-lookup"><span data-stu-id="a6bc0-119">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="a6bc0-120">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="a6bc0-120">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="a6bc0-121">V poli **ID e-mailu** zadejte ID, které pomůže identifikovat tuto šablonu.</span><span class="sxs-lookup"><span data-stu-id="a6bc0-121">In the **Email ID** field, enter an ID to help identify this template.</span></span>
1. <span data-ttu-id="a6bc0-122">Do pole **Jméno odesílatele** zadejte jméno odesílatele.</span><span class="sxs-lookup"><span data-stu-id="a6bc0-122">In the **Sends name** field, enter the senders name.</span></span>
1. <span data-ttu-id="a6bc0-123">Zadejte smysluplný popis do pole **Popis e-mailu**.</span><span class="sxs-lookup"><span data-stu-id="a6bc0-123">In the **Email Description**, enter a meaningful description.</span></span>
1. <span data-ttu-id="a6bc0-124">Do pole **E-mail odesílatele** zadejte e-mailovou adresu odesílatele.</span><span class="sxs-lookup"><span data-stu-id="a6bc0-124">In the **Sender email**, enter the senders email address.</span></span>
1. <span data-ttu-id="a6bc0-125">V části **Všeobecné** vyberte výchozí jazyk šablony e-mailu.</span><span class="sxs-lookup"><span data-stu-id="a6bc0-125">In the **General** section, select a default language for the email template.</span></span> <span data-ttu-id="a6bc0-126">Výchozí jazyk se použije, pokud pro zadaný jazyk neexistuje žádná lokalizovaná šablona.</span><span class="sxs-lookup"><span data-stu-id="a6bc0-126">The default language will be used when no localized template exists for the specified language.</span></span>
1. <span data-ttu-id="a6bc0-127">Rozbalte část **Obsah e-mailové zprávy**, zvolte **Nový** a vytvořte obsah šablony.</span><span class="sxs-lookup"><span data-stu-id="a6bc0-127">Expand the **Email message content** section and select **New** to create the template content.</span></span> <span data-ttu-id="a6bc0-128">Pro každou položku obsahu vyberte jazyk a zadejte předmět e-mailu.</span><span class="sxs-lookup"><span data-stu-id="a6bc0-128">For each content item, select the language and provide the email subject line.</span></span> <span data-ttu-id="a6bc0-129">Pokud e-mail bude mít text, zkontrolujte zda je zaškrtnuto políčko **má tělo**.</span><span class="sxs-lookup"><span data-stu-id="a6bc0-129">If the email will have a body, ensure that the **Has body** box is checked.</span></span>
1. <span data-ttu-id="a6bc0-130">V podokně akcí vyberte **E-mailová zpráva** a zadejte šablonu e-mailového textu.</span><span class="sxs-lookup"><span data-stu-id="a6bc0-130">On the action pane, select **Email message** to provide an email body template.</span></span>

<span data-ttu-id="a6bc0-131">Následující obrázek ukazuje několik příkladů nastavení šablony e-mailu.</span><span class="sxs-lookup"><span data-stu-id="a6bc0-131">The following image shows some example email template settings.</span></span>

![Nastavení šablony e-mailu](media/email-template.png)

### <a name="create-an-email-event"></a><span data-ttu-id="a6bc0-133">Vytvoření e-mailové události</span><span class="sxs-lookup"><span data-stu-id="a6bc0-133">Create an email event</span></span>

<span data-ttu-id="a6bc0-134">E-mailovou událost vytvoříte takto.</span><span class="sxs-lookup"><span data-stu-id="a6bc0-134">To create an email event, follow these steps.</span></span>

1. <span data-ttu-id="a6bc0-135">V navigačním podokně přejděte na **Moduly \> Maloobchodní a velkoobchodní prodej \> Nastavení centrály \> Profil oznámení e-mailem aplikace Commerce**.</span><span class="sxs-lookup"><span data-stu-id="a6bc0-135">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="a6bc0-136">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="a6bc0-136">In the list, find and select the desired record.</span></span> 
1. <span data-ttu-id="a6bc0-137">Z rozevíracího seznamu **ID e-mailu** vyberte e-mailovou šablonu.</span><span class="sxs-lookup"><span data-stu-id="a6bc0-137">Select the email template from the **Email ID** drop-down list.</span></span>
1. <span data-ttu-id="a6bc0-138">Z rozevíracího seznamu vyberte **Typ oznámení e-mailem**.</span><span class="sxs-lookup"><span data-stu-id="a6bc0-138">Select the appropriate **Email notification type** from the drop-down list.</span></span>
1. <span data-ttu-id="a6bc0-139">Zaškrtněte políčko **Aktivní**.</span><span class="sxs-lookup"><span data-stu-id="a6bc0-139">Select the **Active** check box.</span></span>
1. <span data-ttu-id="a6bc0-140">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="a6bc0-140">On the action pane, select **Save**.</span></span>

<span data-ttu-id="a6bc0-141">Následující obrázek ukazuje několik příkladů nastavení oznámení události.</span><span class="sxs-lookup"><span data-stu-id="a6bc0-141">The following image shows some example event notification settings.</span></span>

![Nastavení oznámení události](media/email-notification-profile.png)

### <a name="next-steps"></a><span data-ttu-id="a6bc0-143">Další kroky</span><span class="sxs-lookup"><span data-stu-id="a6bc0-143">Next steps</span></span>

<span data-ttu-id="a6bc0-144">Před odesláním e-mailu je nutné nakonfigurovat službu odchozí pošty a nastavit dávkovou úlohu.</span><span class="sxs-lookup"><span data-stu-id="a6bc0-144">Before you can send mails, you must configure your outgoing mail service and set up a batch job.</span></span> <span data-ttu-id="a6bc0-145">Další informace naleznete v tématu [Konfigurace a odesílání e-mailu](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="a6bc0-145">For more information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="a6bc0-146">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="a6bc0-146">Additional resources</span></span>

[<span data-ttu-id="a6bc0-147">Konfigurace a odeslání e-mailu</span><span class="sxs-lookup"><span data-stu-id="a6bc0-147">Configure and send email</span></span>](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="a6bc0-148">Přehled kanálů</span><span class="sxs-lookup"><span data-stu-id="a6bc0-148">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="a6bc0-149">Předpoklady nastavení kanálu</span><span class="sxs-lookup"><span data-stu-id="a6bc0-149">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="a6bc0-150">Přehled organizací a organizačních hierarchií</span><span class="sxs-lookup"><span data-stu-id="a6bc0-150">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
