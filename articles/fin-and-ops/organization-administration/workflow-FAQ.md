---
title: Časté dotazy k workflow
description: Toto téma poskytuje odpovědi na časté otázky týkající se systému workflow v Microsoft Dynamics 365 for Finance and Operations.
author: ChrisGarty
manager: AnnBe
ms.date: 02/28/2019
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
ms.openlocfilehash: f058a450eb18e688efbc5306a42b4efef6aa91e7
ms.sourcegitcommit: 9a723737565ac78c884e40f7129d0f5aad747524
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/01/2019
ms.locfileid: "773199"
---
# <a name="workflow-system"></a><span data-ttu-id="99349-103">Systémový workflowu</span><span class="sxs-lookup"><span data-stu-id="99349-103">Workflow system</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="99349-104">Toto téma poskytuje odpovědi na časté otázky týkající se systému workflow v Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="99349-104">This topic answers frequently asked questions about the workflow system in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="notifications"></a><span data-ttu-id="99349-105">Oznámení</span><span class="sxs-lookup"><span data-stu-id="99349-105">Notifications</span></span>

### <a name="why-are-multiple-notifications-received-when-a-work-item-is-rejected"></a><span data-ttu-id="99349-106">Proč je při odmítnutí pracovní položky doručeno více oznámení?</span><span class="sxs-lookup"><span data-stu-id="99349-106">Why are multiple notifications received when a work item is rejected?</span></span>
<span data-ttu-id="99349-107">Když je pracovní položka odmítnuta, tato pracovní položka je dokončena jako odmítnutá.</span><span class="sxs-lookup"><span data-stu-id="99349-107">When a work item is rejected, that work item is completed as rejected.</span></span> <span data-ttu-id="99349-108">Jiná pracovní položka je vytvořena a přiřazena původci.</span><span class="sxs-lookup"><span data-stu-id="99349-108">Another work item is created and assigned to the originator.</span></span> <span data-ttu-id="99349-109">To znamená, že existuje oznámení původci o odmítnuté pracovní položce, a samostatné oznámení uživateli přiřazenému k nové pracovní položce s požadovanou změnou.</span><span class="sxs-lookup"><span data-stu-id="99349-109">This means that there is a notification to the originator for the rejected work item, and a separate notification to the user assigned to the new "change requested" work item.</span></span> 

<span data-ttu-id="99349-110">Každé oznámení je pro jinou pracovní položku, ale podobnost může způsobit zmatek.</span><span class="sxs-lookup"><span data-stu-id="99349-110">Each notification is for a different work item, but the similarity can cause confusion.</span></span> <span data-ttu-id="99349-111">Hledáme způsoby, jak tuto skutečnost v budoucnu vylepšit.</span><span class="sxs-lookup"><span data-stu-id="99349-111">We are looking at ways to improve this in a future release.</span></span>
