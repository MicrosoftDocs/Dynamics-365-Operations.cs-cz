---
title: Časté dotazy k workflow
description: Toto téma poskytuje odpovědi na časté otázky týkající se systému workflow v Microsoft Dynamics 365 for Finance and Operations.
author: ChrisGarty
manager: AnnBe
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: adcc9bbc422a3fddfd51d248daf95c0da6d4c9bb
ms.sourcegitcommit: 8cf77e9171d6cad8ae6c8bfad9e4f9a46fef6d23
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/19/2019
ms.locfileid: "1688993"
---
# <a name="workflow-faq"></a><span data-ttu-id="fb2ed-103">Workflow – Často kladené otázky</span><span class="sxs-lookup"><span data-stu-id="fb2ed-103">Workflow FAQ</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fb2ed-104">Toto téma poskytuje odpovědi na časté otázky týkající se systému workflow v Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="fb2ed-104">This topic answers frequently asked questions about the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a><span data-ttu-id="fb2ed-105">Proč je při odmítnutí pracovní položky doručeno více oznámení?</span><span class="sxs-lookup"><span data-stu-id="fb2ed-105">Why are multiple notifications received when a work item is rejected?</span></span>
<span data-ttu-id="fb2ed-106">Když je pracovní položka odmítnuta, tato pracovní položka je dokončena jako odmítnutá.</span><span class="sxs-lookup"><span data-stu-id="fb2ed-106">When a work item is rejected, that work item is completed as rejected.</span></span> <span data-ttu-id="fb2ed-107">Jiná pracovní položka je vytvořena a přiřazena původci.</span><span class="sxs-lookup"><span data-stu-id="fb2ed-107">Another work item is created and assigned to the originator.</span></span> <span data-ttu-id="fb2ed-108">To znamená, že existuje oznámení původci o odmítnuté pracovní položce, a samostatné oznámení uživateli přiřazenému k nové pracovní položce s požadovanou změnou.</span><span class="sxs-lookup"><span data-stu-id="fb2ed-108">This means that there is a notification to the originator for the rejected work item, and a separate notification to the user assigned to the new "change requested" work item.</span></span> 

<span data-ttu-id="fb2ed-109">Každé oznámení je pro jinou pracovní položku, ale podobnost může způsobit zmatek.</span><span class="sxs-lookup"><span data-stu-id="fb2ed-109">Each notification is for a different work item, but the similarity can cause confusion.</span></span> <span data-ttu-id="fb2ed-110">Hledáme způsoby, jak tuto skutečnost v budoucnu vylepšit.</span><span class="sxs-lookup"><span data-stu-id="fb2ed-110">We are looking at ways to improve this in a future release.</span></span>

## <a name="why-are-my-workflow-exports-failing"></a><span data-ttu-id="fb2ed-111">Proč se nedaří exporty mých workflow?</span><span class="sxs-lookup"><span data-stu-id="fb2ed-111">Why are my workflow exports failing?</span></span>
<span data-ttu-id="fb2ed-112">V současné době existuje omezení funkce exportu workflow, která nedovoluje, aby názvy workflow byly delší než 48 znaků.</span><span class="sxs-lookup"><span data-stu-id="fb2ed-112">There is currently a limitation in the workflow export feature that prevents workflow names from exceeding 48 characters.</span></span> <span data-ttu-id="fb2ed-113">Použití názvu, který je delší než 48 znaků, může vést k tomu, že dojde k chybě „Serveru se nepodařilo ověřit požadavek“, anebo se nepodaří exportovat soubor s typem souboru.</span><span class="sxs-lookup"><span data-stu-id="fb2ed-113">Using a name that is longer than 48 characters can result in a "Server failed to authenticate the request" error and/or prevent a file to be exported  without a file type.</span></span> <span data-ttu-id="fb2ed-114">Následující příspěvek blogu poskytuje více podrobností o [odstraňování potíží s exportem workflow](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).</span><span class="sxs-lookup"><span data-stu-id="fb2ed-114">The following blog post provides more details [Workflow Export Troubleshooting](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).</span></span>

## <a name="can-the-submitter-of-a-workflow-also-approve-the-workflow"></a><span data-ttu-id="fb2ed-115">Může odesílatel workflow také schválit workflow?</span><span class="sxs-lookup"><span data-stu-id="fb2ed-115">Can the submitter of a workflow also approve the workflow?</span></span>
<span data-ttu-id="fb2ed-116">Ano, odesílatel workflow může také schválit workflow, pokud je to tímto způsobem nakonfigurováno.</span><span class="sxs-lookup"><span data-stu-id="fb2ed-116">Yes, a submitter of a workflow can also approve the workflow if it is configured that way.</span></span> <span data-ttu-id="fb2ed-117">Chcete-li předejít tomuto chování, nastavte **Parametry workflow > Obecné > Schvalovatel > Nepovolit schválení odesílatelem** na hodnotu **Ano**.</span><span class="sxs-lookup"><span data-stu-id="fb2ed-117">To prevent this behavior, set **Workflow parameters > General > Approver > Disallow approval by submitter** to **Yes**.</span></span>

## <a name="can-i-add-alerts-to-workflows-to-provide-notifications-to-users"></a><span data-ttu-id="fb2ed-118">Mohu přidat výstrahy do workflow a poskytnout tak uživatelům upozornění?</span><span class="sxs-lookup"><span data-stu-id="fb2ed-118">Can I add alerts to workflows to provide notifications to users?</span></span>
<span data-ttu-id="fb2ed-119">Zde je několik klíčových oblastí, které je třeba vzít do úvahy při přidávání výstrah do workflow za účelem poskytování oznámení:</span><span class="sxs-lookup"><span data-stu-id="fb2ed-119">Here are a few key areas to note about adding alerts to workflows to provide notifications:</span></span>
- <span data-ttu-id="fb2ed-120">Výstrahy a mechanismy oznamování workflow</span><span class="sxs-lookup"><span data-stu-id="fb2ed-120">Alerts versus workflow notification mechanisms</span></span>
    - <span data-ttu-id="fb2ed-121">Výstrahy lze nastavit pro změny záznamů.</span><span class="sxs-lookup"><span data-stu-id="fb2ed-121">Alerts can be set up for record changes.</span></span> <span data-ttu-id="fb2ed-122">Workflow mění záznamy, takže je možné nastavit výstrahu související se změnou záznamu způsobenou workflow.</span><span class="sxs-lookup"><span data-stu-id="fb2ed-122">Workflows change records, so it's possible to set up an alert related to a record change caused by a workflow.</span></span> <span data-ttu-id="fb2ed-123">Protože však workflow mají jiné předdefinované možnosti oznámení, není použití výstrah ideální.</span><span class="sxs-lookup"><span data-stu-id="fb2ed-123">However, because workflows have different built-in notification options, using alerts isn’t ideal.</span></span>
- <span data-ttu-id="fb2ed-124">Standardní oznámení z workflow</span><span class="sxs-lookup"><span data-stu-id="fb2ed-124">Standard notifications from workflows</span></span> 
    - <span data-ttu-id="fb2ed-125">Workflow obsahují e-mailová oznámení.</span><span class="sxs-lookup"><span data-stu-id="fb2ed-125">Workflows have built in email notifications.</span></span> <span data-ttu-id="fb2ed-126">Zákazník může nakonfigurovat oznámení tak, aby se uživatelům odesílaly e-maily.</span><span class="sxs-lookup"><span data-stu-id="fb2ed-126">A customer can configure the notifications so that the users are sent emails.</span></span> <span data-ttu-id="fb2ed-127">Tato oznámení nemají za následek zprávy centra akcí pro uživatele.</span><span class="sxs-lookup"><span data-stu-id="fb2ed-127">Those notifications don’t result in Action Center messages for users.</span></span>
    - <span data-ttu-id="fb2ed-128">V budoucí aktualizaci bude přidána zpráva centra akcí, takže uživateli bude přiřazena pracovní položka workflow.</span><span class="sxs-lookup"><span data-stu-id="fb2ed-128">In a future update we will be adding an Action Center message so a user is assigned a workflow work item.</span></span> 
- <span data-ttu-id="fb2ed-129">Přidání oznámení do workflow</span><span class="sxs-lookup"><span data-stu-id="fb2ed-129">Adding notifications to workflows</span></span>
    - <span data-ttu-id="fb2ed-130">Zprávy centra akcí lze vytvářet pro konkrétní uživatele, například zprávu vytvořenou z workflow v jazyce X + +.</span><span class="sxs-lookup"><span data-stu-id="fb2ed-130">Action Center messages can be created for specific users, such as a message created from a workflow in X++.</span></span>
    - <span data-ttu-id="fb2ed-131">[Workflow mají obchodní události](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow), které může odběratel použít ke spuštění aplikace Flow s oznámeními, která hledají.</span><span class="sxs-lookup"><span data-stu-id="fb2ed-131">[Workflows have Business Events](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) that the customer could use to trigger Flows have the notifications that they are looking for.</span></span>   

<span data-ttu-id="fb2ed-132">V souhrnu, pokud uživatel neobdrží správné oznámení z centra akcí, když jsou mu přiřazeny pracovní položky workflow, využijte [obchodní události workflow](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) s aplikací Microsoft Flow s cílem poskytovat další nebo odlišná oznámení.</span><span class="sxs-lookup"><span data-stu-id="fb2ed-132">In summary, if a user does not get the proper notification from the Action Center when they are assigned a workflow work item, then leverage [Workflow Business Events](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/business-events/business-events-workflow) with Microsoft Flow to provide additional or different notifications.</span></span>
