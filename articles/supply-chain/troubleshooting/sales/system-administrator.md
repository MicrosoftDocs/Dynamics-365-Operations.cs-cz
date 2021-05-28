---
title: Správci systému nemohou vymazat pozastavení objednávky, protože nejsou autorizovaní
description: Správci systému nemohou vymazat pozastavení objednávky, protože nejsou autorizovaní.
author: SmithaNataraj
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: acabd6409d9b2860535335bc648bcc34304e0cb0
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026354"
---
# <a name="system-administrators-cant-clear-order-holds-because-they-arent-authorized"></a><span data-ttu-id="d4593-103">Správci systému nemohou vymazat pozastavení objednávky, protože nejsou autorizovaní</span><span class="sxs-lookup"><span data-stu-id="d4593-103">System administrators can't clear order holds because they aren't authorized</span></span>

<span data-ttu-id="d4593-104">Číslo článku znalostní báze: 4614642</span><span class="sxs-lookup"><span data-stu-id="d4593-104">KB number: 4614642</span></span>

## <a name="symptoms"></a><span data-ttu-id="d4593-105">Příznaky</span><span class="sxs-lookup"><span data-stu-id="d4593-105">Symptoms</span></span>

<span data-ttu-id="d4593-106">Správci systému nemohou vymazat pozastavení prodejní objednávky, pokud nemají konkrétní roli, která je přiřazena v kódu blokování objednávky.</span><span class="sxs-lookup"><span data-stu-id="d4593-106">System administrators can't clear sales order holds unless they have the specific role that is assigned in the order hold code.</span></span>

## <a name="resolution"></a><span data-ttu-id="d4593-107">Rozlišení</span><span class="sxs-lookup"><span data-stu-id="d4593-107">Resolution</span></span>

<span data-ttu-id="d4593-108">Přístup k některým operacím, jako je zúčtování blokování prodejní objednávky, je řízen nastavením obchodních zásad.</span><span class="sxs-lookup"><span data-stu-id="d4593-108">Access to some operations, such as clearing sales order holds, is driven by the setup of a business policy.</span></span> <span data-ttu-id="d4593-109">Správci systému obvykle nemají povoleno provádět operace tohoto typu.</span><span class="sxs-lookup"><span data-stu-id="d4593-109">System administrators aren't typically allowed to perform operations of this type.</span></span> 

<span data-ttu-id="d4593-110">Častěji se přístup k provedení konkrétního úkolu řídí obchodními zásadami a k provádění tohoto úkolu jsou povoleny pouze konkrétní osoby v organizaci.</span><span class="sxs-lookup"><span data-stu-id="d4593-110">More often, access to perform a specific task is governed by business policies, and only specific persons in an organization are approved to perform that task.</span></span> <span data-ttu-id="d4593-111">Mezi příklady patří schválení, která jsou výsledkem schválení pracovního postupu, a konkrétní úkoly, které jsou výsledkem konfigurace pracovního postupu.</span><span class="sxs-lookup"><span data-stu-id="d4593-111">Examples include approvals that are the result of workflow approvals and specific tasks that are the result of a workflow configuration.</span></span>

<span data-ttu-id="d4593-112">Ačkoli s přidržením objednávky není spojen žádný pracovní postup, princip je podobný.</span><span class="sxs-lookup"><span data-stu-id="d4593-112">Although no workflow is associated with order holds, the principle is similar.</span></span> <span data-ttu-id="d4593-113">Relevantní role označuje konkrétní skupinu lidí v organizaci, kteří mají právo vymazat blokování objednávky.</span><span class="sxs-lookup"><span data-stu-id="d4593-113">A relevant role designates the specific group of people in an organization who have the right to clear order holds.</span></span> <span data-ttu-id="d4593-114">Toto právo by nemělo být nutně uděleno všem správcům, protože tento přístup porušuje definované obchodní zásady.</span><span class="sxs-lookup"><span data-stu-id="d4593-114">This right should not necessarily be granted to all administrators, because that approach violates the defined business policy.</span></span>
