---
title: Výstražná upozornění klientovi e-mailem
description: Toto téma obsahuje informace o nastavení pravidel, která budou odesílat e-mailová oznámení, pokud dojde k předem definované události.
author: tjvass
manager: AnnBe
ms.date: 02/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: kfend
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2019-1-29
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 314f04eec04a75aed058c9c38066738e8758f653
ms.sourcegitcommit: 440ebe14ad26574ba227d23ee8370f6b6110645b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/01/2019
ms.locfileid: "373744"
---
# <a name="client-alert-notifications-by-email"></a><span data-ttu-id="3bb27-103">Výstražná upozornění klientovi e-mailem</span><span class="sxs-lookup"><span data-stu-id="3bb27-103">Client alert notifications by email</span></span>

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="3bb27-104">V aplikaci Microsoft Dynamics 365 for Finance and Operations můžete definovat vlastní pravidla výstrah, která sledují filtrovaná zobrazení dat a automaticky odesílají oznámení e-mailem, když dojde k předem definované události.</span><span class="sxs-lookup"><span data-stu-id="3bb27-104">In Microsoft Dynamics 365 for Finance and Operations, you can define custom alert rules that monitor filtered views of data and automatically send email notifications when predefined events occur.</span></span> <span data-ttu-id="3bb27-105">Možnost odeslání e-mailového oznámení je k dispozici pro všechny podporované typy výstrah a lze ji rovněž zapnout pro existující pravidla výstrah.</span><span class="sxs-lookup"><span data-stu-id="3bb27-105">The option to send email notifications is available for all supported alert types and can also be turned on for existing alert rules.</span></span>

<span data-ttu-id="3bb27-106">Můžete použít vestavěné ovládací prvky k vytváření pravidel výstrah, která sledují filtrovaná zobrazení dávkových úloh systému.</span><span class="sxs-lookup"><span data-stu-id="3bb27-106">You can use built-in controls to create alert rules that monitor the filtered views of system batch jobs.</span></span> <span data-ttu-id="3bb27-107">Sledováním hodnoty pole **Stav** můžete také nastavit pravidla výstrah, která odesílají e-mail při selhání dávkové úlohy.</span><span class="sxs-lookup"><span data-stu-id="3bb27-107">By monitoring the value of the **Status** field, you can also configure alert rules that send email when a batch job fails.</span></span> <span data-ttu-id="3bb27-108">Po vytvoření těchto pravidel výstrah již nemusíte kontrolovat sestavy ohledně změn obchodní dat.</span><span class="sxs-lookup"><span data-stu-id="3bb27-108">After these alert rules are created, you no longer have to check reports for changes to business data.</span></span> <span data-ttu-id="3bb27-109">Místo toho můžete nechat inteligentní službu detekce změny Finance and Operations, aby prováděla monitoring za vás.</span><span class="sxs-lookup"><span data-stu-id="3bb27-109">Instead, you can let the Finance and Operations intelligent change detection service do the monitoring for you.</span></span>

<span data-ttu-id="3bb27-110">Výstrahy klienta závisí na podsystému e-mailu, který je poskytován prostřednictvím integrace s Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="3bb27-110">Client alerts depend on the email subsystem that is provided through integration with Microsoft Office.</span></span> <span data-ttu-id="3bb27-111">Doporučujeme použít poskytovatele SMTP, aby e-mailová distribuce nemusela spoléhat na lokálního e-mailového klienta.</span><span class="sxs-lookup"><span data-stu-id="3bb27-111">We recommend that you use the Simple Mail Transfer Protocol (SMTP) provider, so that email distribution doesn't have to rely on a local mail client.</span></span>

<span data-ttu-id="3bb27-112">Aby mohli odesílat oznámení e-mailem, musí odběratelé nakonfigurovat integrované e-mailové služby.</span><span class="sxs-lookup"><span data-stu-id="3bb27-112">To send notifications by email, customers must configure integrated email services.</span></span> <span data-ttu-id="3bb27-113">E-mailová oznámení se odesílají příjemcům jménem vlastníků výstrahy.</span><span class="sxs-lookup"><span data-stu-id="3bb27-113">Email notifications are sent to recipients on behalf of alert owners.</span></span>

<span data-ttu-id="3bb27-114">Další informace o způsobu konfigurace e-mailu v aplikaci Finance and Operations naleznete v tématu [Konfigurace a odesílání e-mailu](../organization-administration/configure-email.md).</span><span class="sxs-lookup"><span data-stu-id="3bb27-114">For more information about how to configure email in Finance and Operations, see [Configure and send email](../organization-administration/configure-email.md).</span></span>

<span data-ttu-id="3bb27-115">Následující obrázek znázorňuje dialogové okno **Vytvoření pravidla výstrahy**, které nyní zahrnuje možnost **Odeslat e-mail**.</span><span class="sxs-lookup"><span data-stu-id="3bb27-115">The following image shows the **Create alert rule** dialog box, which now includes a **Send email** option.</span></span>

<span data-ttu-id="3bb27-116">[![Dialogové okno vytvoření pravidla výstrahy, kde je možnost Odeslat e-mail nastavena na Ano](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)</span><span class="sxs-lookup"><span data-stu-id="3bb27-116">[![Create alert rule dialog box, where the Send email option is set to Yes](./media/Create-alert-rule-form.png)](./media/Create-alert-rule-form.png)</span></span>

> [!NOTE]
> <span data-ttu-id="3bb27-117">Když je možnost **Odeslat e-mail** nastavena na **Ano**, výstražná oznámení budou nadále doručována z Centra akcí.</span><span class="sxs-lookup"><span data-stu-id="3bb27-117">When the **Send email** option is set to **Yes**, alert notifications will continue to be delivered from the Action Center.</span></span>

## <a name="alert-notification-email-templates"></a><span data-ttu-id="3bb27-118">Šablony e-mailu s výstražným upozorněním</span><span class="sxs-lookup"><span data-stu-id="3bb27-118">Alert notification email templates</span></span>

<span data-ttu-id="3bb27-119">Služba odešle e-mailová upozornění pomocí předdefinovaných šablon e-mailu, které doručují základní podrobnosti výstražných upozornění.</span><span class="sxs-lookup"><span data-stu-id="3bb27-119">The service sends email notifications by using predefined email templates that deliver the basic details of the alert notification.</span></span> <span data-ttu-id="3bb27-120">Tyto podrobnosti zahrnují přímý odkaz na stránku, kde bylo definováno pravidla výstrahy.</span><span class="sxs-lookup"><span data-stu-id="3bb27-120">These details include a direct link to the page where the alert rule was defined.</span></span>

<span data-ttu-id="3bb27-121">Následující obrázek zobrazuje strukturu výstražných oznámení při přijetí e-mailem.</span><span class="sxs-lookup"><span data-stu-id="3bb27-121">The following image show the structure of the alert notifications when they are received by email.</span></span>

<span data-ttu-id="3bb27-122">[![Výstražná upozornění založená na šabloně pro vytvoření záznamu, změny polí a odstranění šablon](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)</span><span class="sxs-lookup"><span data-stu-id="3bb27-122">[![Template-based alert notifications for record creation, field changes, and template deletion](./media/Alert-email-templates.png)](./media/Alert-email-templates.png)</span></span>