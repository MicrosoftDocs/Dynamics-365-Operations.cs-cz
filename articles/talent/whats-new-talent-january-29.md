---
title: Co je nového nebo změněného v aplikaci Dynamics 365 Talent (31. ledna 2019)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Talent.
author: andreabichsel
manager: AnnBe
ms.date: 01/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-01-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 8e8c11e460a4678efea81f8d3d1eec96b673d329
ms.sourcegitcommit: 53174ed4e7cc4e1ba07cdfc39207e7296ef87c1f
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/07/2020
ms.locfileid: "4690045"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-january-31-2019"></a><span data-ttu-id="29a84-103">Co je nového nebo změněného v aplikaci Dynamics 365 Talent (31. ledna 2019)</span><span class="sxs-lookup"><span data-stu-id="29a84-103">What's new or changed in Dynamics 365 Talent (January 31, 2019)</span></span>

<span data-ttu-id="29a84-104">Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="29a84-104">This topic describes features that are either new or changed in Dynamics 365 Talent.</span></span>

<span data-ttu-id="29a84-105">**Sestavení 8.1.2128**</span><span class="sxs-lookup"><span data-stu-id="29a84-105">**Build 8.1.2128**</span></span>

## <a name="core-hr-changes"></a><span data-ttu-id="29a84-106">Změny Core HR</span><span class="sxs-lookup"><span data-stu-id="29a84-106">Core HR Changes</span></span>

### <a name="time-off-taken-on-leave-people-card-doesnt-consider-leave-plan-dates"></a><span data-ttu-id="29a84-107">Volno využité na kartě dovolené zaměstnanců nezohledňuje plánovaná data dovolené</span><span class="sxs-lookup"><span data-stu-id="29a84-107">Time off taken on leave people card doesn't consider leave plan dates</span></span>
<span data-ttu-id="29a84-108">Pro plány pracovního volna nepoužívané v kalendářním roce, karta **Vybráno** nyní zobrazuje pracovní volno, které bylo využito v roce pracovního volna definovaného pro plán.</span><span class="sxs-lookup"><span data-stu-id="29a84-108">For leave plans that don’t run on a calendar year, the **Taken** card now displays time off that’s been taken in the plan-defined leave year.</span></span> <span data-ttu-id="29a84-109">Pokud je například rok pracovního volna v organizaci od 1. června do 30. května a zaměstnanec si vyberte 3 dny v prosinci, budou se na kartě **Vybráno** k 15. lednu zobrazovat 3 dny.</span><span class="sxs-lookup"><span data-stu-id="29a84-109">For example, if an organization’s leave year is June 1 through May 30 and an employee has taken three days off in December, the **Taken** card on January 15, will display 3 days.</span></span> 

### <a name="accrual-amounts-not-matching-tier-date-basis"></a><span data-ttu-id="29a84-110">Časové rozlišené částky neodpovídají základu data vrstvy</span><span class="sxs-lookup"><span data-stu-id="29a84-110">Accrual amounts not matching tier date basis</span></span>
<span data-ttu-id="29a84-111">Byly přidány nové možnosti pro dovolenou a absenci (parametry **lidských zdrojů**) pro povolení zákazníkům určit, ke kterému datu jsou měsíce služby zaměstnance platné.</span><span class="sxs-lookup"><span data-stu-id="29a84-111">New options have been added to leave and absence (**Human resources** parameters) to enable customers to determine when employees’ months of service date are effective.</span></span> <span data-ttu-id="29a84-112">V některých organizacích je tímto datem konec měsíce, jinde to ale může být začátek příštího měsíce.</span><span class="sxs-lookup"><span data-stu-id="29a84-112">For some organizations, the date is the end of the month, but for others it may be the start of the next month.</span></span> <span data-ttu-id="29a84-113">Jedna organizace může například udělovat čas volna k 31. prosinci, zatímco jiná k 1. lednu.</span><span class="sxs-lookup"><span data-stu-id="29a84-113">For example, one organization may award time off on December 31, while another may award time off on January 1.</span></span> <span data-ttu-id="29a84-114">Tato možnost vám umožní zvolit, kdy dojde k udělení.</span><span class="sxs-lookup"><span data-stu-id="29a84-114">This option will allow you to choose when the award should occur.</span></span> 

### <a name="worker-hire-actions-are-stuck-in-workflow-complete-state"></a><span data-ttu-id="29a84-115">Akce náboru pracovníků jsou zastavené ve stavu Workflow dokončen</span><span class="sxs-lookup"><span data-stu-id="29a84-115">Worker hire actions are stuck in "Workflow complete" state</span></span>
<span data-ttu-id="29a84-116">Byly provedeny změny k nápravě problémů, kdy malý počet workflow skončil se stavem Workflow dokončen</span><span class="sxs-lookup"><span data-stu-id="29a84-116">Changes have been made to correct an issue where a small number of workflows finished with a "Workflow complete" status.</span></span> <span data-ttu-id="29a84-117">Nové workflowy by se nyní měly přesunout do stavu Dokončeno, jakmile skončí workflow.</span><span class="sxs-lookup"><span data-stu-id="29a84-117">New workflows should now move to a "Completed" state when the workflow finishes.</span></span> <span data-ttu-id="29a84-118">Všechny workflowy ve stavu workflow byl dokončen budou přesunuty do chybového stavu umožňujícího aktualizaci nebo odebrání v případě potřeby.</span><span class="sxs-lookup"><span data-stu-id="29a84-118">Any workflows in a workflow completed status will be transitioned to an error status to allow for updating or removal if required.</span></span> 
