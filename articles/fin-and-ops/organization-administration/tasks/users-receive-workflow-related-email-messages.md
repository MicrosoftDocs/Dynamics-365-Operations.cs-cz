---
title: Umožňuje uživatelům dostávat e-mailové zprávy týkající se workflowu
description: Systém můžete konfigurovat na zaslání e-mailových zpráv uživatelům, když nastanou události týkající se workflowu.
author: jasongre
manager: AnnBe
ms.date: 08/29/2018
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
ms.openlocfilehash: 6800d02878123388611d35760123d0215e9d539f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "344586"
---
# <a name="enable-users-to-receive-workflow-related-email-messages"></a><span data-ttu-id="cb33f-103">Umožňuje uživatelům dostávat e-mailové zprávy týkající se workflowu</span><span class="sxs-lookup"><span data-stu-id="cb33f-103">Enable users to receive workflow-related email messages</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cb33f-104">Systém můžete konfigurovat na zaslání e-mailových zpráv uživatelům, když nastanou události týkající se workflowu.</span><span class="sxs-lookup"><span data-stu-id="cb33f-104">You can configure the system to send email messages to users when workflow-related events occur.</span></span> <span data-ttu-id="cb33f-105">Například je možné zaslat e-mailové zprávy uživatelům, když jim jsou přiřazeny dokumenty ke schválení.</span><span class="sxs-lookup"><span data-stu-id="cb33f-105">For example, email messages can be sent to users when documents are assigned to them for approval.</span></span> <span data-ttu-id="cb33f-106">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="cb33f-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="cb33f-107">Přejděte do nabídky Správa systému > Uživatelé > Uživatelé.</span><span class="sxs-lookup"><span data-stu-id="cb33f-107">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="cb33f-108">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="cb33f-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="cb33f-109">Klikněte na Možnosti uživatelů.</span><span class="sxs-lookup"><span data-stu-id="cb33f-109">Click User options.</span></span>
4. <span data-ttu-id="cb33f-110">Klikněte na kartu Workflow.</span><span class="sxs-lookup"><span data-stu-id="cb33f-110">Click the Workflow tab.</span></span>
    * <span data-ttu-id="cb33f-111">Ujistěte se, že je rozbalená část Oznámení.</span><span class="sxs-lookup"><span data-stu-id="cb33f-111">Make sure that the Notifications section is expanded.</span></span>     <span data-ttu-id="cb33f-112">V části Oznámení můžete určit, jakým způsobem má uživatel dostávat oznámení o události týkající se workflowu.</span><span class="sxs-lookup"><span data-stu-id="cb33f-112">In the Notifications section, you can specify how you want the user to be notified about workflow-related events.</span></span>  
5. <span data-ttu-id="cb33f-113">V poli Typ oznámení workflowu položky řádku zvolte možnost.</span><span class="sxs-lookup"><span data-stu-id="cb33f-113">In the Line-item workflow notification type field, select an option.</span></span>
    * <span data-ttu-id="cb33f-114">Seskupená – Oznámení pro položky řádku jsou seskupena do jedné e-mailové zprávy.</span><span class="sxs-lookup"><span data-stu-id="cb33f-114">Grouped – Notifications for line items are grouped into a single email message.</span></span>    <span data-ttu-id="cb33f-115">Individuální – E-mailová zpráva je odeslána pro každou položku řádku.</span><span class="sxs-lookup"><span data-stu-id="cb33f-115">Individual – An email message is sent for each line item.</span></span>  
    * <span data-ttu-id="cb33f-116">Pokud chcete, aby uživatelé dostávali upozornění v klientovi, zaškrtněte políčko Odesílat oznámení e-mailem.</span><span class="sxs-lookup"><span data-stu-id="cb33f-116">If you want the user to receive notifications in the client, select the Send notifications in email check box.</span></span>  
6. <span data-ttu-id="cb33f-117">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="cb33f-117">Click Save.</span></span>
7. <span data-ttu-id="cb33f-118">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="cb33f-118">Close the page.</span></span>

