---
title: Nastavení profilu oznámení e-mailem
description: Toto téma popisuje, jak vytvořit profil oznámení e-mailem v aplikaci Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
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
ms.openlocfilehash: 9e5d90eaf1815bbe54b0bea40d92a0a993a23b75
ms.sourcegitcommit: 141e0239b6310ab4a6a775bc0997120c31634f79
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/10/2020
ms.locfileid: "3113798"
---
# <a name="set-up-an-email-notification-profile"></a><span data-ttu-id="6e0fd-103">Nastavení profilu oznámení e-mailem</span><span class="sxs-lookup"><span data-stu-id="6e0fd-103">Set up an email notification profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="6e0fd-104">Toto téma popisuje, jak vytvořit profil oznámení e-mailem v aplikaci Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6e0fd-104">This topic describes how to create an email notification profile in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="6e0fd-105">Přehled</span><span class="sxs-lookup"><span data-stu-id="6e0fd-105">Overview</span></span>

<span data-ttu-id="6e0fd-106">Před vytvořením kanálů budete mít možnost nastavit profil, který zajistí, že e-mailová oznámení mohou být odeslána pro různé události, jako je například vytvoření objednávky, stav expedice objednávky a chyba platby.</span><span class="sxs-lookup"><span data-stu-id="6e0fd-106">Before creating channels, you'll want to set up a profile to ensure that email notifications can be sent out for various events, such as order creation, order shipping status, and payment failure.</span></span>

<span data-ttu-id="6e0fd-107">Další informace o konfiguraci e-mailu naleznete v tématu [Konfigurace a odesílání e-mailu](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="6e0fd-107">For additional email configuration information, see [Configure and send email](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json).</span></span>

## <a name="create-an-email-notification-profile"></a><span data-ttu-id="6e0fd-108">Vytvoření profilu oznámení e-mailem</span><span class="sxs-lookup"><span data-stu-id="6e0fd-108">Create an email notification profile</span></span>

<span data-ttu-id="6e0fd-109">Chcete-li vytvořit profil oznámení e-mailem, postupujte následujícím způsobem.</span><span class="sxs-lookup"><span data-stu-id="6e0fd-109">To create an email notification profile, follow these steps.</span></span>

1. <span data-ttu-id="6e0fd-110">V navigačním podokně přejděte na **Moduly \> Maloobchodní a velkoobchodní prodej \> Nastavení centrály \> Profil oznámení e-mailem aplikace Commerce**.</span><span class="sxs-lookup"><span data-stu-id="6e0fd-110">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="6e0fd-111">V podokně akcí klikněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="6e0fd-111">On the action pane, click **New**.</span></span>
1. <span data-ttu-id="6e0fd-112">Do pole **Profil oznámení e-mailem** zadejte název pro identifikaci profilu.</span><span class="sxs-lookup"><span data-stu-id="6e0fd-112">In the **Email notification profile** field, enter a name to identify the profile.</span></span>
1. <span data-ttu-id="6e0fd-113">Zadejte příslušný popis do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="6e0fd-113">In the **Description** field, enter a relevant description.</span></span>
1. <span data-ttu-id="6e0fd-114">Nastavení přepínač **Aktivní** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="6e0fd-114">Set the **Active** switch to **Yes**.</span></span>

### <a name="create-an-email-template"></a><span data-ttu-id="6e0fd-115">Vytvoření šablonu e-mailu</span><span class="sxs-lookup"><span data-stu-id="6e0fd-115">Create an email template</span></span>

<span data-ttu-id="6e0fd-116">Před vytvořením oznámení e-mailem je nutné vytvořit šablonu e-mailu organizace, která obsahuje e-mailové informace odesílatele a šablonu e-mailu.</span><span class="sxs-lookup"><span data-stu-id="6e0fd-116">Before an email notification can be created, you must create an organization email template which contains the senders email information and the email template.</span></span>

<span data-ttu-id="6e0fd-117">Šablonu e-mailu vytvoříte takto:</span><span class="sxs-lookup"><span data-stu-id="6e0fd-117">To create an email template, follow these steps.</span></span>

1. <span data-ttu-id="6e0fd-118">V navigačním podokně přejděte na **Moduly \> Maloobchodní a velkoobchodní prodej \> Nastavení centrály \> Parametry \> E-mailové šablony organizace**.</span><span class="sxs-lookup"><span data-stu-id="6e0fd-118">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Parameters \> Organization email templates**.</span></span>
1. <span data-ttu-id="6e0fd-119">V podokně akcí zvolte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="6e0fd-119">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="6e0fd-120">V poli **ID e-mailu** zadejte ID, které pomůže identifikovat tuto šablonu.</span><span class="sxs-lookup"><span data-stu-id="6e0fd-120">In the **Email ID** field, enter an ID to help identify this template.</span></span>
1. <span data-ttu-id="6e0fd-121">Do pole **Jméno odesílatele** zadejte jméno odesílatele.</span><span class="sxs-lookup"><span data-stu-id="6e0fd-121">In the **Sends name** field, enter the senders name.</span></span>
1. <span data-ttu-id="6e0fd-122">Zadejte smysluplný popis do pole **Popis e-mailu**.</span><span class="sxs-lookup"><span data-stu-id="6e0fd-122">In the **Email Description**, enter a meaningful description.</span></span>
1. <span data-ttu-id="6e0fd-123">Do pole **E-mail odesílatele** zadejte e-mailovou adresu odesílatele.</span><span class="sxs-lookup"><span data-stu-id="6e0fd-123">In the **Sender email**, enter the senders email address.</span></span>
1. <span data-ttu-id="6e0fd-124">V části **Obecné** vyplňte veškeré potřebné volitelné informace (jako je například priorita e-mailu).</span><span class="sxs-lookup"><span data-stu-id="6e0fd-124">In the **General** section, fill out any optional information needed (such as the email priority).</span></span>
1. <span data-ttu-id="6e0fd-125">Rozbalte část **Obsah e-mailové zprávy**, zvolte **Nový** a vytvořte obsah šablony.</span><span class="sxs-lookup"><span data-stu-id="6e0fd-125">Expand the **Email message content** section and select **New** to create the template content.</span></span> <span data-ttu-id="6e0fd-126">Pro každou položku obsahu vyberte jazyk a zadejte předmět e-mailu.</span><span class="sxs-lookup"><span data-stu-id="6e0fd-126">For each content item, select the language and provide the email subject line.</span></span> <span data-ttu-id="6e0fd-127">Pokud e-mail bude mít text, zkontrolujte zda je zaškrtnuto políčko **má tělo**.</span><span class="sxs-lookup"><span data-stu-id="6e0fd-127">If the email will have a body, ensure that the **Has body** box is checked.</span></span>
1. <span data-ttu-id="6e0fd-128">V podokně akcí vyberte **E-mailová zpráva** a zadejte šablonu e-mailového textu.</span><span class="sxs-lookup"><span data-stu-id="6e0fd-128">On the action pane, select **Email message** to provide an email body template.</span></span>

<span data-ttu-id="6e0fd-129">Následující obrázek ukazuje několik příkladů nastavení šablony e-mailu.</span><span class="sxs-lookup"><span data-stu-id="6e0fd-129">The following image shows some example email template settings.</span></span>

![Nastavení šablony e-mailu](media/email-template.png)

### <a name="create-an-email-event"></a><span data-ttu-id="6e0fd-131">Vytvoření e-mailové události</span><span class="sxs-lookup"><span data-stu-id="6e0fd-131">Create an email event</span></span>

<span data-ttu-id="6e0fd-132">E-mailovou událost vytvoříte takto.</span><span class="sxs-lookup"><span data-stu-id="6e0fd-132">To create an email event, follow these steps.</span></span>

1. <span data-ttu-id="6e0fd-133">V navigačním podokně přejděte na **Moduly \> Maloobchodní a velkoobchodní prodej \> Nastavení centrály \> Profil oznámení e-mailem aplikace Commerce**.</span><span class="sxs-lookup"><span data-stu-id="6e0fd-133">In the navigation pane, go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce email notification profile**.</span></span>
1. <span data-ttu-id="6e0fd-134">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="6e0fd-134">In the list, find and select the desired record.</span></span> 
1. <span data-ttu-id="6e0fd-135">Z rozevíracího seznamu **ID e-mailu** vyberte e-mailovou šablonu.</span><span class="sxs-lookup"><span data-stu-id="6e0fd-135">Select the email template from the **Email ID** drop-down list.</span></span>
1. <span data-ttu-id="6e0fd-136">Z rozevíracího seznamu vyberte **Typ oznámení e-mailem**.</span><span class="sxs-lookup"><span data-stu-id="6e0fd-136">Select the appropriate **Email notification type** from the drop-down list.</span></span>
1. <span data-ttu-id="6e0fd-137">Zaškrtněte políčko **Aktivní**.</span><span class="sxs-lookup"><span data-stu-id="6e0fd-137">Select the **Active** check box.</span></span>
1. <span data-ttu-id="6e0fd-138">V podokně akcí vyberte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="6e0fd-138">On the action pane, select **Save**.</span></span>

<span data-ttu-id="6e0fd-139">Následující obrázek ukazuje několik příkladů nastavení oznámení události.</span><span class="sxs-lookup"><span data-stu-id="6e0fd-139">The following image shows some example event notification settings.</span></span>

![Nastavení oznámení události](media/email-notification-profile.png)

## <a name="additional-resources"></a><span data-ttu-id="6e0fd-141">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="6e0fd-141">Additional resources</span></span>

[<span data-ttu-id="6e0fd-142">Konfigurace a odeslání e-mailu</span><span class="sxs-lookup"><span data-stu-id="6e0fd-142">Configure and send email</span></span>](../fin-ops-core/fin-ops/organization-administration/configure-email.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="6e0fd-143">Přehled kanálů</span><span class="sxs-lookup"><span data-stu-id="6e0fd-143">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="6e0fd-144">Předpoklady nastavení kanálu</span><span class="sxs-lookup"><span data-stu-id="6e0fd-144">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="6e0fd-145">Přehled organizací a organizačních hierarchií</span><span class="sxs-lookup"><span data-stu-id="6e0fd-145">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)
