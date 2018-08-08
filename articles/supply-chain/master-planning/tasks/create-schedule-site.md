--- 
title: "Vytvoření plánu pro pracoviště"
description: "Tento postup popisuje způsob plánování výrobních zakázek, které nebyly dosud pro pracoviště zahájeny."
author: ShylaThompson
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 0afc49f8da3aa20d4002517834b7ddc41a7fc827
ms.contentlocale: cs-cz
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-schedule-for-a-site"></a><span data-ttu-id="6010d-103">Vytvoření plánu pro pracoviště</span><span class="sxs-lookup"><span data-stu-id="6010d-103">Create a schedule for a site</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6010d-104">Tento postup popisuje způsob plánování výrobních zakázek, které nebyly dosud pro pracoviště zahájeny.</span><span class="sxs-lookup"><span data-stu-id="6010d-104">This procedure shows how to schedule production orders that are not yet started for a site.</span></span>  <span data-ttu-id="6010d-105">K dokončení tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="6010d-105">The demo data company USMF is used to complete this procedure.</span></span>


## <a name="identify-production-orders-that-are-not-started"></a><span data-ttu-id="6010d-106">určení výrobních zakázek, které nebyly zahájeny</span><span class="sxs-lookup"><span data-stu-id="6010d-106">Identify production orders that are not started</span></span>
1. <span data-ttu-id="6010d-107">Přejděte na Řízení výroby > Výrobní zakázky > Všechny výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="6010d-107">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="6010d-108">Použijte rychlý filtr pro hledání záznamů.</span><span class="sxs-lookup"><span data-stu-id="6010d-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="6010d-109">Můžete například filtrovat v poli Pracoviště pomocí hodnoty „1“.</span><span class="sxs-lookup"><span data-stu-id="6010d-109">For example, filter on the Site field with a value of '1'.</span></span>
    * <span data-ttu-id="6010d-110">1 představuje pracoviště v rámci USMF.</span><span class="sxs-lookup"><span data-stu-id="6010d-110">1 represents a site in USMF.</span></span> <span data-ttu-id="6010d-111">Pokud nepoužíváte USMF, vyberte pracoviště z vlastní společnosti.</span><span class="sxs-lookup"><span data-stu-id="6010d-111">If you are not using USMF, select a site from your own company.</span></span>  
3. <span data-ttu-id="6010d-112">Otevřete filtr sloupce Stav.</span><span class="sxs-lookup"><span data-stu-id="6010d-112">Open the Status column filter.</span></span>
4. <span data-ttu-id="6010d-113">Použijte filtr v poli Stav, s hodnotou Plánováno a za použití operátoru filtru „je přesně“.</span><span class="sxs-lookup"><span data-stu-id="6010d-113">Apply a filter on the "Status" field, with a value of "Scheduled", using the "is exactly" filter operator.</span></span>

## <a name="create-a-schedule"></a><span data-ttu-id="6010d-114">Vytvoření plánu</span><span class="sxs-lookup"><span data-stu-id="6010d-114">Create a schedule</span></span>
1. <span data-ttu-id="6010d-115">V seznamu označte všechny řádky nebo jejich označení zrušte.</span><span class="sxs-lookup"><span data-stu-id="6010d-115">In the list, mark or unmark all rows.</span></span>
2. <span data-ttu-id="6010d-116">V podokně akcí klikněte na možnost Plán.</span><span class="sxs-lookup"><span data-stu-id="6010d-116">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="6010d-117">Klikněte na Plánovat úlohy.</span><span class="sxs-lookup"><span data-stu-id="6010d-117">Click Schedule jobs.</span></span>
4. <span data-ttu-id="6010d-118">V poli Způsob plánování vyberte „Zpět od data dodání“.</span><span class="sxs-lookup"><span data-stu-id="6010d-118">In the Scheduling direction field, select 'Backward from delivery date'.</span></span>
5. <span data-ttu-id="6010d-119">Vyberte Ne v poli Omezená kapacita.</span><span class="sxs-lookup"><span data-stu-id="6010d-119">Select No in the Finite capacity field.</span></span>
6. <span data-ttu-id="6010d-120">Vyberte Ne v poli Omezený materiál.</span><span class="sxs-lookup"><span data-stu-id="6010d-120">Select No in the Finite material field.</span></span>
7. <span data-ttu-id="6010d-121">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="6010d-121">Click OK.</span></span>
    * <span data-ttu-id="6010d-122">Tato operace může chvíli trvat.</span><span class="sxs-lookup"><span data-stu-id="6010d-122">This may take a while.</span></span>  

## <a name="view-the-result-of-scheduled-production-orders"></a><span data-ttu-id="6010d-123">Zobrazení výsledků naplánovaných výrobních zakázek</span><span class="sxs-lookup"><span data-stu-id="6010d-123">View the result of scheduled production orders</span></span>
1. <span data-ttu-id="6010d-124">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="6010d-124">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="6010d-125">Můžete označit libovolné řádky.</span><span class="sxs-lookup"><span data-stu-id="6010d-125">You can mark any row.</span></span>  
2. <span data-ttu-id="6010d-126">V podokně akcí klikněte na položku Výrobní zakázka.</span><span class="sxs-lookup"><span data-stu-id="6010d-126">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="6010d-127">Klikněte na Všechny úlohy.</span><span class="sxs-lookup"><span data-stu-id="6010d-127">Click All jobs.</span></span>
    * <span data-ttu-id="6010d-128">Na této stránce můžete vidět seznam úloh.</span><span class="sxs-lookup"><span data-stu-id="6010d-128">On this page, you can see the list of jobs.</span></span> <span data-ttu-id="6010d-129">Na kartě Plánování můžete zobrazit počáteční datum a koncové datum úlohy.</span><span class="sxs-lookup"><span data-stu-id="6010d-129">On the Scheduling tab, you can see the Start date and End date for a job.</span></span>  
4. <span data-ttu-id="6010d-130">Klepněte na Kusovníky.</span><span class="sxs-lookup"><span data-stu-id="6010d-130">Click Materials.</span></span>
    * <span data-ttu-id="6010d-131">Na této stránce se zobrazí odhad spotřeby materiálu pro operace ve výrobní zakázce, a aktuální dostupné zásoby.</span><span class="sxs-lookup"><span data-stu-id="6010d-131">On this page, you can see the estimated material consumption for the operations on the production order and the current available inventory.</span></span>  


