---
title: Co je nového nebo změněného v aplikaci Dynamics 365 for Talent (31. ledna 2019)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 1/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-01-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 5c9449e2bdec8c17cc2cf659ed68ac1d713a26ad
ms.sourcegitcommit: 1e32d78868098fd76124bb41363f15c4ec3ea15a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/05/2019
ms.locfileid: "374727"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-january-31-2019"></a><span data-ttu-id="56140-103">Co je nového nebo změněného v aplikaci Dynamics 365 for Talent (31. ledna 2019)</span><span class="sxs-lookup"><span data-stu-id="56140-103">What's new or changed in Dynamics 365 for Talent (January 31, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="56140-104">Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 for Talent.</span><span class="sxs-lookup"><span data-stu-id="56140-104">This topic describes features that are either new or changed in Dynamics 365 for Talent</span></span>

<span data-ttu-id="56140-105">**Sestavení 8.1.2128**</span><span class="sxs-lookup"><span data-stu-id="56140-105">**Build 8.1.2128**</span></span>

## <a name="core-hr-changes"></a><span data-ttu-id="56140-106">Změny Core HR</span><span class="sxs-lookup"><span data-stu-id="56140-106">Core HR Changes</span></span>

### <a name="time-off-taken-on-leave-people-card-doesnt-consider-leave-plan-dates"></a><span data-ttu-id="56140-107">Volno využité na kartě dovolené zaměstnanců nezohledňuje plánovaná data dovolené</span><span class="sxs-lookup"><span data-stu-id="56140-107">Time off taken on leave people card doesn't consider leave plan dates</span></span>
<span data-ttu-id="56140-108">Pro ty, kteří mají plány dovolené nepoužívané v kalendářním roce, karta **Vybráno** nyní zobrazuje dovolenou, která byla využita v roce dovolené definované pro plán.</span><span class="sxs-lookup"><span data-stu-id="56140-108">For those that have leave plans that don’t run on a calendar year, the **Taken** card now displays time off that’s been taken in the plan-defined leave year.</span></span> <span data-ttu-id="56140-109">Pokud je například rok dovolené v organizaci od 1. června do 30. května a zaměstnanec si vyberte 3 dny v prosinci, budou se na kartě **Vybráno** k 15. lednu zobrazovat 3 dny.</span><span class="sxs-lookup"><span data-stu-id="56140-109">For example, if an organization’s leave year is June 1 through May 30 and an employee has taken 3 days off in December, the **Taken** card on January 15, will display 3 days.</span></span> 

### <a name="accrual-amounts-not-matching-tier-date-basis"></a><span data-ttu-id="56140-110">Časové rozlišené částky neodpovídají základu data vrstvy</span><span class="sxs-lookup"><span data-stu-id="56140-110">Accrual amounts not matching tier date basis</span></span>
<span data-ttu-id="56140-111">Byly přidány nové možnosti pro dovolenou a absenci (parametry **lidských zdrojů**) pro povolení zákazníkům určit, ke kterému datu jsou měsíce služby zaměstnance platné.</span><span class="sxs-lookup"><span data-stu-id="56140-111">New options have been added to leave and absence (**Human resources** parameters) to enable customers to determine when employees’ months of service date are effective.</span></span> <span data-ttu-id="56140-112">V některých organizacích je tímto datem konec měsíce, jinde to ale může být začátek příštího měsíce.</span><span class="sxs-lookup"><span data-stu-id="56140-112">For some organizations, the date is the end of the month, but for others it may be the start of the next month.</span></span> <span data-ttu-id="56140-113">Jedna organizace může například udělovat čas volna k 31. prosinci, zatímco jiná k 1. lednu.</span><span class="sxs-lookup"><span data-stu-id="56140-113">For example, one organization may award time off on December 31, while another may award time off on January 1.</span></span> <span data-ttu-id="56140-114">Tato možnost vám umožní zvolit, kdy dojde k udělení.</span><span class="sxs-lookup"><span data-stu-id="56140-114">This option will allow you to choose when the award should occur.</span></span> 

### <a name="worker-hire-actions-are-stuck-in-workflow-complete-state"></a><span data-ttu-id="56140-115">Akce náboru pracovníků jsou zastavené ve stavu Workflow dokončen</span><span class="sxs-lookup"><span data-stu-id="56140-115">Worker hire actions are stuck in "Workflow complete" state</span></span>
<span data-ttu-id="56140-116">Byly provedeny změny k nápravě problémů, kdy malý počet workflow skončil se stavem Workflow dokončen</span><span class="sxs-lookup"><span data-stu-id="56140-116">Changes have been made to correct an issue where a small number of workflows finished with a "Workflow complete" status.</span></span> <span data-ttu-id="56140-117">Nové workflowy by se nyní měly přesunout do stavu Dokončeno, jakmile skončí workflow.</span><span class="sxs-lookup"><span data-stu-id="56140-117">New workflows should now move to a "Completed" state when the workflow finishes.</span></span> <span data-ttu-id="56140-118">Všechny workflowy ve stavu workflow byl dokončen budou přesunuty do chybového stavu umožňujícího aktualizaci nebo odebrání v případě potřeby.</span><span class="sxs-lookup"><span data-stu-id="56140-118">Any workflows in a workflow completed status will be transitioned to an error status to allow for updating or removal if required.</span></span> 
