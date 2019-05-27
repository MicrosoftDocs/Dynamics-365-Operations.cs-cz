---
title: Časté dotazy k workflow
description: Toto téma poskytuje odpovědi na časté otázky týkající se systému workflow v Microsoft Dynamics 365 for Finance and Operations.
author: ChrisGarty
manager: AnnBe
ms.date: 05/07/2019
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
ms.openlocfilehash: f6240b1b5136937aa47f455547fed6f0c7c08e2c
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2019
ms.locfileid: "1509284"
---
# <a name="workflow-system"></a><span data-ttu-id="df406-103">Systémový workflowu</span><span class="sxs-lookup"><span data-stu-id="df406-103">Workflow system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="df406-104">Toto téma poskytuje odpovědi na časté otázky týkající se systému workflow v Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="df406-104">This topic answers frequently asked questions about the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="notifications"></a><span data-ttu-id="df406-105">Oznámení</span><span class="sxs-lookup"><span data-stu-id="df406-105">Notifications</span></span>

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a><span data-ttu-id="df406-106">Proč je při odmítnutí pracovní položky doručeno více oznámení?</span><span class="sxs-lookup"><span data-stu-id="df406-106">Why are multiple notifications received when a work item is rejected?</span></span>
<span data-ttu-id="df406-107">Když je pracovní položka odmítnuta, tato pracovní položka je dokončena jako odmítnutá.</span><span class="sxs-lookup"><span data-stu-id="df406-107">When a work item is rejected, that work item is completed as rejected.</span></span> <span data-ttu-id="df406-108">Jiná pracovní položka je vytvořena a přiřazena původci.</span><span class="sxs-lookup"><span data-stu-id="df406-108">Another work item is created and assigned to the originator.</span></span> <span data-ttu-id="df406-109">To znamená, že existuje oznámení původci o odmítnuté pracovní položce, a samostatné oznámení uživateli přiřazenému k nové pracovní položce s požadovanou změnou.</span><span class="sxs-lookup"><span data-stu-id="df406-109">This means that there is a notification to the originator for the rejected work item, and a separate notification to the user assigned to the new "change requested" work item.</span></span> 

<span data-ttu-id="df406-110">Každé oznámení je pro jinou pracovní položku, ale podobnost může způsobit zmatek.</span><span class="sxs-lookup"><span data-stu-id="df406-110">Each notification is for a different work item, but the similarity can cause confusion.</span></span> <span data-ttu-id="df406-111">Hledáme způsoby, jak tuto skutečnost v budoucnu vylepšit.</span><span class="sxs-lookup"><span data-stu-id="df406-111">We are looking at ways to improve this in a future release.</span></span>

### <a name="why-are-my-workflow-exports-failing"></a><span data-ttu-id="df406-112">Proč se nedaří exporty mých workflow?</span><span class="sxs-lookup"><span data-stu-id="df406-112">Why are my workflow exports failing?</span></span>
<span data-ttu-id="df406-113">V současné době existuje omezení funkce exportu workflow, která nedovoluje, aby názvy workflow byly delší než 48 znaků.</span><span class="sxs-lookup"><span data-stu-id="df406-113">There is currently a limitation in the workflow export feature that prevents workflow names from exceeding 48 characters.</span></span> <span data-ttu-id="df406-114">Použití názvu, který je delší než 48 znaků, může vést k tomu, že dojde k chybě „Serveru se nepodařilo ověřit požadavek“, anebo se nepodaří exportovat soubor s typem souboru.</span><span class="sxs-lookup"><span data-stu-id="df406-114">Using a name that is longer than 48 characters can result in a "Server failed to authenticate the request" error and/or prevent a file to be exported  without a file type.</span></span> <span data-ttu-id="df406-115">Následující příspěvek blogu poskytuje více podrobností o [odstraňování potíží s exportem workflow](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).</span><span class="sxs-lookup"><span data-stu-id="df406-115">The following blog post provides more details [Workflow Export Troubleshooting](https://community.dynamics.com/ax/b/elandaxdynamicsaxupgradesanddevelopment/archive/2019/04/10/workflow-export-troubleshooting).</span></span>
