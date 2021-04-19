---
title: Naplánování výrobní zakázky
description: Tato procedura popisuje způsob plánování výrobní zakázky.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob, WrkCtrCapResSum, ProdRouteJobSched, ProductionOrderScheduleDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0a52e2ee3bf0c5dadeda375882d16de60b31d658
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831883"
---
# <a name="schedule-a-production-order"></a><span data-ttu-id="23f41-103">Naplánování výrobní zakázky</span><span class="sxs-lookup"><span data-stu-id="23f41-103">Schedule a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="23f41-104">Tato procedura popisuje způsob plánování výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="23f41-104">This procedure shows how to schedule a production order.</span></span> <span data-ttu-id="23f41-105">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="23f41-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="23f41-106">Jedná se o třetí proceduru ze sedmi, která vysvětluje životního cyklus výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="23f41-106">This is the third procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="schedule-a-production-order"></a><span data-ttu-id="23f41-107">Naplánování výrobní zakázky</span><span class="sxs-lookup"><span data-stu-id="23f41-107">Schedule a production order</span></span>
1. <span data-ttu-id="23f41-108">Přejděte na Řízení výroby > Výrobní zakázky > Všechny výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="23f41-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="23f41-109">Vyberte výrobní zakázku, která má stav Odhadováno.</span><span class="sxs-lookup"><span data-stu-id="23f41-109">Select a production order that has the Estimated status.</span></span>  
2. <span data-ttu-id="23f41-110">V podokně akcí klikněte na možnost Plán.</span><span class="sxs-lookup"><span data-stu-id="23f41-110">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="23f41-111">Klikněte na Plánovat úlohy.</span><span class="sxs-lookup"><span data-stu-id="23f41-111">Click Schedule jobs.</span></span>
    * <span data-ttu-id="23f41-112">Parametry pro plánování se nastavují na této stránce.</span><span class="sxs-lookup"><span data-stu-id="23f41-112">The parameters for scheduling are set up on this page.</span></span> <span data-ttu-id="23f41-113">Můžete nastavit parametry pro konkrétní uživatelé nebo u všech uživatelů.</span><span class="sxs-lookup"><span data-stu-id="23f41-113">You can set up the parameters for specific users or all users.</span></span>  
4. <span data-ttu-id="23f41-114">V poli Způsob plánování vyberte „Vpřed ode dneška“.</span><span class="sxs-lookup"><span data-stu-id="23f41-114">In the Scheduling direction field, select 'Forward from today'.</span></span>
5. <span data-ttu-id="23f41-115">Do pole Datum plánování zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="23f41-115">In the Scheduling date field, enter a date.</span></span>
6. <span data-ttu-id="23f41-116">Zaškrtněte políčko Omezená kapacita, nebo jeho zaškrtnutí zrušte.</span><span class="sxs-lookup"><span data-stu-id="23f41-116">Select or clear the Finite capacity check box.</span></span>
7. <span data-ttu-id="23f41-117">Zaškrtněte políčko Omezený materiál, nebo jeho zaškrtnutí zrušte.</span><span class="sxs-lookup"><span data-stu-id="23f41-117">Select or clear the Finite material check box.</span></span>
8. <span data-ttu-id="23f41-118">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="23f41-118">Click OK.</span></span>

## <a name="view-the-scheduling-results"></a><span data-ttu-id="23f41-119">Zobrazte výsledky plánování</span><span class="sxs-lookup"><span data-stu-id="23f41-119">View the scheduling results</span></span>
1. <span data-ttu-id="23f41-120">V podokně akcí klikněte na položku Výrobní zakázka.</span><span class="sxs-lookup"><span data-stu-id="23f41-120">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="23f41-121">Klikněte na Všechny úlohy.</span><span class="sxs-lookup"><span data-stu-id="23f41-121">Click All jobs.</span></span>
    * <span data-ttu-id="23f41-122">Tato stránka zobrazuje naplánované úlohy, které jste právě vygenerovali.</span><span class="sxs-lookup"><span data-stu-id="23f41-122">This page displays the scheduled jobs that you have just generated.</span></span>  
3. <span data-ttu-id="23f41-123">Rozbalte nebo sbalte oddíl Plánování.</span><span class="sxs-lookup"><span data-stu-id="23f41-123">Expand or collapse the Scheduling section.</span></span>
    * <span data-ttu-id="23f41-124">Na pevné záložce Plánování můžete zobrazit plánované datum a čas.</span><span class="sxs-lookup"><span data-stu-id="23f41-124">On the Scheduling FastTab, you can view the scheduled date and time.</span></span>  
4. <span data-ttu-id="23f41-125">Klepněte na možnost Dotazy.</span><span class="sxs-lookup"><span data-stu-id="23f41-125">Click Inquiries.</span></span>
5. <span data-ttu-id="23f41-126">Klikněte na možnost Vytížení kapacity.</span><span class="sxs-lookup"><span data-stu-id="23f41-126">Click Capacity load.</span></span>
    * <span data-ttu-id="23f41-127">Na stránce Vytížení kapacity se zobrazí kapacita rezervovaná pomocí plánování práce, celkový počet hodin, které jsou aktuálně rezervovány u prostředku a počet hodin, které jsou nadále k dispozici pro plánování úlohy u prostředku.</span><span class="sxs-lookup"><span data-stu-id="23f41-127">The Capacity load page displays the capacity that is reserved through job scheduling, the total number of hours that are currently reserved on the resource, and the number of hours that remain available for job scheduling on the resource.</span></span>  
6. <span data-ttu-id="23f41-128">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="23f41-128">Close the page.</span></span>
7. <span data-ttu-id="23f41-129">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="23f41-129">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]