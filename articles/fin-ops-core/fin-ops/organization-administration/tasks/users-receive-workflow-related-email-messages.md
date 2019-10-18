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
ms.openlocfilehash: 5e08f95ef6d263ee0f8c0a94b258c8a2795786bc
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189837"
---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a><span data-ttu-id="eff46-103">Umožňuje uživatelům dostávat e-mailové zprávy týkající se workflowu</span><span class="sxs-lookup"><span data-stu-id="eff46-103">Enable users to receive workflow-related email messages</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="eff46-104">Systém můžete konfigurovat na zaslání e-mailových zpráv uživatelům, když nastanou události týkající se workflowu.</span><span class="sxs-lookup"><span data-stu-id="eff46-104">You can configure the system to send email messages to users when workflow-related events occur.</span></span> <span data-ttu-id="eff46-105">Například je možné zaslat e-mailové zprávy uživatelům, když jim jsou přiřazeny dokumenty ke schválení.</span><span class="sxs-lookup"><span data-stu-id="eff46-105">For example, email messages can be sent to users when documents are assigned to them for approval.</span></span> <span data-ttu-id="eff46-106">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="eff46-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="eff46-107">Přejděte na **Navigační podokno > Moduly > Správa systému > Uživatelé > Uživatelé**.</span><span class="sxs-lookup"><span data-stu-id="eff46-107">Go to **Navigation pane > Modules > System administration > Users > Users**.</span></span>
2. <span data-ttu-id="eff46-108">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="eff46-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="eff46-109">V **Podokně akcí** klikněte na možnost **Možnosti uživatele**.</span><span class="sxs-lookup"><span data-stu-id="eff46-109">On the **Action pane**, click **User options**.</span></span>
4. <span data-ttu-id="eff46-110">Klikněte na kartu **Workflow**. Zkontrolujte, zda je rozbalen oddíl **Oznámení**.</span><span class="sxs-lookup"><span data-stu-id="eff46-110">Click the **Workflow** tab. Make sure that the **Notifications** section is expanded.</span></span> <span data-ttu-id="eff46-111">V části **Oznámení** můžete určit, jakým způsobem má uživatel dostávat oznámení o události týkající se workflowu.</span><span class="sxs-lookup"><span data-stu-id="eff46-111">In the **Notifications** section, you can specify how you want the user to be notified about workflow-related events.</span></span>  
5. <span data-ttu-id="eff46-112">V poli **Typ oznámení workflowu položky řádku** zvolte možnost.</span><span class="sxs-lookup"><span data-stu-id="eff46-112">In the **Line-item workflow notification type** field, select an option.</span></span>
    - <span data-ttu-id="eff46-113">Seskupená – Oznámení pro položky řádku jsou seskupena do jedné e-mailové zprávy.</span><span class="sxs-lookup"><span data-stu-id="eff46-113">Grouped – Notifications for line items are grouped into a single email message.</span></span>
    - <span data-ttu-id="eff46-114">Individuální – E-mailová zpráva je odeslána pro každou položku řádku.</span><span class="sxs-lookup"><span data-stu-id="eff46-114">Individual – An email message is sent for each line item.</span></span>  
    - <span data-ttu-id="eff46-115">Pokud chcete, aby uživatelé dostávali upozornění v klientovi, zaškrtněte políčko **Odesílat oznámení e-mailem**.</span><span class="sxs-lookup"><span data-stu-id="eff46-115">If you want the user to receive notifications in the client, select the **Send notifications in email** check box.</span></span>  
6. <span data-ttu-id="eff46-116">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="eff46-116">Click **Save**.</span></span>
7. <span data-ttu-id="eff46-117">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="eff46-117">Close the page.</span></span>

