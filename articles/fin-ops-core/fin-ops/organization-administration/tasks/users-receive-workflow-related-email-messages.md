---
title: Umožňuje uživatelům dostávat e-mailové zprávy týkající se workflowu
description: Systém můžete konfigurovat na zaslání e-mailových zpráv uživatelům, když nastanou události týkající se workflowu.
author: jasongre
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserManagement, SysUserSetup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f4c9f2f22bc4b5ca5b4351f7956ad2eb6d3b903d
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140414"
---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a><span data-ttu-id="4e06a-103">Umožňuje uživatelům dostávat e-mailové zprávy týkající se workflowu</span><span class="sxs-lookup"><span data-stu-id="4e06a-103">Enable users to receive workflow-related email messages</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4e06a-104">Systém můžete konfigurovat na zaslání e-mailových zpráv uživatelům, když nastanou události týkající se workflowu.</span><span class="sxs-lookup"><span data-stu-id="4e06a-104">You can configure the system to send email messages to users when workflow-related events occur.</span></span> <span data-ttu-id="4e06a-105">Například je možné zaslat e-mailové zprávy uživatelům, když jim jsou přiřazeny dokumenty ke schválení.</span><span class="sxs-lookup"><span data-stu-id="4e06a-105">For example, email messages can be sent to users when documents are assigned to them for approval.</span></span> <span data-ttu-id="4e06a-106">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="4e06a-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="4e06a-107">Přejděte na **Navigační podokno > Moduly > Správa systému > Uživatelé > Uživatelé**.</span><span class="sxs-lookup"><span data-stu-id="4e06a-107">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="4e06a-108">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="4e06a-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="4e06a-109">V **Podokně akcí** klikněte na možnost **Možnosti uživatele**.</span><span class="sxs-lookup"><span data-stu-id="4e06a-109">On the **Action pane**, click **User options**.</span></span>
4. <span data-ttu-id="4e06a-110">Klikněte na kartu **Workflow**. Zkontrolujte, zda je rozbalen oddíl **Oznámení**.</span><span class="sxs-lookup"><span data-stu-id="4e06a-110">Click the **Workflow** tab. Make sure that the **Notifications** section is expanded.</span></span> <span data-ttu-id="4e06a-111">V části **Oznámení** můžete určit, jakým způsobem má uživatel dostávat oznámení o události týkající se workflowu.</span><span class="sxs-lookup"><span data-stu-id="4e06a-111">In the **Notifications** section, you can specify how you want the user to be notified about workflow-related events.</span></span>  
5. <span data-ttu-id="4e06a-112">V poli **Typ oznámení workflowu položky řádku** zvolte možnost.</span><span class="sxs-lookup"><span data-stu-id="4e06a-112">In the **Line-item workflow notification type** field, select an option.</span></span>
    - <span data-ttu-id="4e06a-113">Seskupená – Oznámení pro položky řádku jsou seskupena do jedné e-mailové zprávy.</span><span class="sxs-lookup"><span data-stu-id="4e06a-113">Grouped – Notifications for line items are grouped into a single email message.</span></span>
    - <span data-ttu-id="4e06a-114">Individuální – E-mailová zpráva je odeslána pro každou položku řádku.</span><span class="sxs-lookup"><span data-stu-id="4e06a-114">Individual – An email message is sent for each line item.</span></span>  
    - <span data-ttu-id="4e06a-115">Pokud chcete, aby uživatelé dostávali upozornění v klientovi, zaškrtněte políčko **Odesílat oznámení e-mailem**.</span><span class="sxs-lookup"><span data-stu-id="4e06a-115">If you want the user to receive notifications in the client, select the **Send notifications in email** check box.</span></span>  
6. <span data-ttu-id="4e06a-116">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="4e06a-116">Click **Save**.</span></span>
7. <span data-ttu-id="4e06a-117">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="4e06a-117">Close the page.</span></span>

