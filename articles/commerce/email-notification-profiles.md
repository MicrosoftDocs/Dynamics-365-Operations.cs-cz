---
title: Nastavení profilu oznámení e-mailem
description: Toto téma popisuje, jak vytvořit profil oznámení e-mailem v aplikaci Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: c0ab56c15a37313d0a88b1174d5bcf51d391dcec
ms.sourcegitcommit: 17ffdcbf4b1801bd6ee9c9ddc18622d5d04b8a98
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2020
ms.locfileid: "3180188"
---
# <a name="set-up-an-email-notification-profile"></a><span data-ttu-id="6a8a8-103">Nastavení profilu oznámení e-mailem</span><span class="sxs-lookup"><span data-stu-id="6a8a8-103">Set up an email notification profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="6a8a8-104">Toto téma popisuje, jak vytvořit profil oznámení e-mailem v aplikaci Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6a8a8-104">This topic describes how to create an email notification profile in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6a8a8-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="6a8a8-105">Overview</span></span>

<span data-ttu-id="6a8a8-106">Před vytvořením kanálů budete mít možnost nastavit profil, který zajistí, že e-mailová oznámení mohou být odeslána pro různé události, jako je například vytvoření objednávky, stav expedice objednávky a chyba platby.</span><span class="sxs-lookup"><span data-stu-id="6a8a8-106">Before creating channels, you'll want to set up a profile to ensure that email notifications can be sent out for various events, such as order creation, order shipping status, and payment failure.</span></span>

<span data-ttu-id="6a8a8-107">Další informace o konfiguraci e-mailu naleznete v tématu [Konfigurace a odesílání e-mailu](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="6a8a8-107">For additional email configuration information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="create-an-email-notification-profile"></a><span data-ttu-id="6a8a8-108">Vytvoření profilu oznámení e-mailem</span><span class="sxs-lookup"><span data-stu-id="6a8a8-108">Create an email notification profile</span></span>

<span data-ttu-id="6a8a8-109">Chcete-li vytvořit profil oznámení e-mailem, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="6a8a8-109">To create an email notification profile, follow these steps.</span></span>

1. <span data-ttu-id="6a8a8-110">V navigačním podokně přejděte na **Moduly \> Maloobchodní a velkoobchodní prodej \> Nastavení centrály \> Profil oznámení e-mailem aplikace Commerce**.</span><span class="sxs-lookup"><span data-stu-id="6a8a8-110">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="6a8a8-111">V podokně akcí klikněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="6a8a8-111">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="6a8a8-112">Do pole **Profil oznámení e-mailem** zadejte název pro identifikaci profilu.</span><span class="sxs-lookup"><span data-stu-id="6a8a8-112">In the **Email notification profile** field, enter a name to identify the profile.</span></span>
1. <span data-ttu-id="6a8a8-113">Zadejte příslušný popis do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="6a8a8-113">In the **Description** field, enter a relevant description.</span></span>
1. <span data-ttu-id="6a8a8-114">Nastavení přepínač **Aktivní** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="6a8a8-114">Set the **Active** switch to **Yes**.</span></span>

### <a name="create-an-email-template"></a><span data-ttu-id="6a8a8-115">Vytvoření šablonu e-mailu</span><span class="sxs-lookup"><span data-stu-id="6a8a8-115">Create an email template</span></span>

<span data-ttu-id="6a8a8-116">Před vytvořením oznámení e-mailem je nutné vytvořit šablonu e-mailu organizace, která obsahuje e-mailové informace odesílatele a šablonu e-mailu.</span><span class="sxs-lookup"><span data-stu-id="6a8a8-116">Before an email notification can be created, you must create an organization email template which contains the senders email information and the email template.</span></span>

<span data-ttu-id="6a8a8-117">Šablonu e-mailu vytvoříte takto:</span><span class="sxs-lookup"><span data-stu-id="6a8a8-117">To create an email template, follow these steps.</span></span>

1. <span data-ttu-id="6a8a8-118">V navigačním podokně přejděte na **Moduly \> Maloobchodní a velkoobchodní prodej \> Nastavení centrály \> Parametry \> E-mailové šablony organizace**.</span><span class="sxs-lookup"><span data-stu-id="6a8a8-118">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="6a8a8-119">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="6a8a8-119">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="6a8a8-120">V poli **ID e-mailu** zadejte ID, které pomůže identifikovat tuto šablonu.</span><span class="sxs-lookup"><span data-stu-id="6a8a8-120">In the **Email ID** field, enter an ID to help identify this template.</span></span>
1. <span data-ttu-id="6a8a8-121">Do pole **Jméno odesílatele** zadejte jméno odesílatele.</span><span class="sxs-lookup"><span data-stu-id="6a8a8-121">In the **Sends name** field, enter the senders name.</span></span>
1. <span data-ttu-id="6a8a8-122">Zadejte smysluplný popis do pole **Popis e-mailu**.</span><span class="sxs-lookup"><span data-stu-id="6a8a8-122">In the **Email Description**, enter a meaningful description.</span></span>
1. <span data-ttu-id="6a8a8-123">Do pole **E-mail odesílatele** zadejte e-mailovou adresu odesílatele.</span><span class="sxs-lookup"><span data-stu-id="6a8a8-123">In the **Sender email**, enter the senders email address.</span></span>
1. <span data-ttu-id="6a8a8-124">V části **Obecné** vyplňte veškeré potřebné volitelné informace (jako je například priorita e-mailu).</span><span class="sxs-lookup"><span data-stu-id="6a8a8-124">In the **General** section, fill out any optional information needed (such as the email priority).</span></span>
1. <span data-ttu-id="6a8a8-125">Rozbalte část **Obsah e-mailové zprávy**, zvolte **Nový** a vytvořte obsah šablony.</span><span class="sxs-lookup"><span data-stu-id="6a8a8-125">Expand the **Email message content** section and select **New** to create the template content.</span></span> <span data-ttu-id="6a8a8-126">Pro každou položku obsahu vyberte jazyk a zadejte předmět e-mailu.</span><span class="sxs-lookup"><span data-stu-id="6a8a8-126">For each content item, select the language and provide the email subject line.</span></span> <span data-ttu-id="6a8a8-127">Pokud e-mail bude mít text, zkontrolujte zda je zaškrtnuto políčko **má tělo**.</span><span class="sxs-lookup"><span data-stu-id="6a8a8-127">If the email will have a body, ensure that the **Has body** box is checked.</span></span>
1. <span data-ttu-id="6a8a8-128">V podokně akcí vyberte **E-mailová zpráva** a zadejte šablonu e-mailového textu.</span><span class="sxs-lookup"><span data-stu-id="6a8a8-128">On the action pane, select **Email message** to provide an email body template.</span></span>

<span data-ttu-id="6a8a8-129">Následující obrázek ukazuje několik příkladů nastavení šablony e-mailu.</span><span class="sxs-lookup"><span data-stu-id="6a8a8-129">The following image shows some example email template settings.</span></span>

![Nastavení šablony e-mailu](media/email-template.png)

### <a name="create-an-email-event"></a><span data-ttu-id="6a8a8-131">Vytvoření e-mailové události</span><span class="sxs-lookup"><span data-stu-id="6a8a8-131">Create an email event</span></span>

<span data-ttu-id="6a8a8-132">E-mailovou událost vytvoříte takto.</span><span class="sxs-lookup"><span data-stu-id="6a8a8-132">To create an email event, follow these steps.</span></span>

1. <span data-ttu-id="6a8a8-133">V navigačním podokně přejděte na **Moduly \> Maloobchodní a velkoobchodní prodej \> Nastavení centrály \> Profil oznámení e-mailem aplikace Commerce**.</span><span class="sxs-lookup"><span data-stu-id="6a8a8-133">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="6a8a8-134">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="6a8a8-134">In the list, find and select the desired record.</span></span> 
1. <span data-ttu-id="6a8a8-135">Z rozevíracího seznamu **ID e-mailu** vyberte e-mailovou šablonu.</span><span class="sxs-lookup"><span data-stu-id="6a8a8-135">Select the email template from the **Email ID** drop-down list.</span></span>
1. <span data-ttu-id="6a8a8-136">Z rozevíracího seznamu vyberte **Typ oznámení e-mailem**.</span><span class="sxs-lookup"><span data-stu-id="6a8a8-136">Select the appropriate **Email notification type** from the drop-down list.</span></span>
1. <span data-ttu-id="6a8a8-137">Zaškrtněte políčko **Aktivní**.</span><span class="sxs-lookup"><span data-stu-id="6a8a8-137">Select the **Active** check box.</span></span>
1. <span data-ttu-id="6a8a8-138">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="6a8a8-138">On the action pane, select **Save**.</span></span>

<span data-ttu-id="6a8a8-139">Následující obrázek ukazuje několik příkladů nastavení oznámení události.</span><span class="sxs-lookup"><span data-stu-id="6a8a8-139">The following image shows some example event notification settings.</span></span>

![Nastavení oznámení události](media/email-notification-profile.png)

### <a name="next-steps"></a><span data-ttu-id="6a8a8-141">Další kroky</span><span class="sxs-lookup"><span data-stu-id="6a8a8-141">Next steps</span></span>

<span data-ttu-id="6a8a8-142">Před odesláním e-mailu je nutné nakonfigurovat službu odchozí pošty a nastavit dávkovou úlohu.</span><span class="sxs-lookup"><span data-stu-id="6a8a8-142">Before you can send mails, you must configure your outgoing mail service and set up a batch job.</span></span> <span data-ttu-id="6a8a8-143">Další informace naleznete v tématu [Konfigurace a odesílání e-mailu](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="6a8a8-143">For more information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="6a8a8-144">Další prostředky</span><span class="sxs-lookup"><span data-stu-id="6a8a8-144">Additional resources</span></span>

[<span data-ttu-id="6a8a8-145">Konfigurace a odeslání e-mailu</span><span class="sxs-lookup"><span data-stu-id="6a8a8-145">Configure and send email</span></span>](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="6a8a8-146">Přehled kanálů</span><span class="sxs-lookup"><span data-stu-id="6a8a8-146">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="6a8a8-147">Předpoklady nastavení kanálu</span><span class="sxs-lookup"><span data-stu-id="6a8a8-147">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="6a8a8-148">Přehled organizací a organizačních hierarchií</span><span class="sxs-lookup"><span data-stu-id="6a8a8-148">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
