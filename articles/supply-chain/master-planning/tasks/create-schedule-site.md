---
title: Vytvoření plánu pro pracoviště
description: Tento postup popisuje způsob plánování výrobních zakázek, které nebyly dosud pro pracoviště zahájeny.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f9e188c5059b3957f3c0291bc4b8c525aac4d399
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5214267"
---
# <a name="create-a-schedule-for-a-site"></a><span data-ttu-id="e497a-103">Vytvoření plánu pro pracoviště</span><span class="sxs-lookup"><span data-stu-id="e497a-103">Create a schedule for a site</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e497a-104">Tento postup popisuje způsob plánování výrobních zakázek, které nebyly dosud pro pracoviště zahájeny.</span><span class="sxs-lookup"><span data-stu-id="e497a-104">This procedure shows how to schedule production orders that are not yet started for a site.</span></span>  <span data-ttu-id="e497a-105">K dokončení tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="e497a-105">The demo data company USMF is used to complete this procedure.</span></span>


## <a name="identify-production-orders-that-are-not-started"></a><span data-ttu-id="e497a-106">určení výrobních zakázek, které nebyly zahájeny</span><span class="sxs-lookup"><span data-stu-id="e497a-106">Identify production orders that are not started</span></span>
1. <span data-ttu-id="e497a-107">Přejděte na Řízení výroby > Výrobní zakázky > Všechny výrobní zakázky.</span><span class="sxs-lookup"><span data-stu-id="e497a-107">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="e497a-108">Použijte rychlý filtr pro hledání záznamů.</span><span class="sxs-lookup"><span data-stu-id="e497a-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="e497a-109">Můžete například filtrovat v poli Pracoviště pomocí hodnoty „1“.</span><span class="sxs-lookup"><span data-stu-id="e497a-109">For example, filter on the Site field with a value of '1'.</span></span>
    * <span data-ttu-id="e497a-110">1 představuje pracoviště v rámci USMF.</span><span class="sxs-lookup"><span data-stu-id="e497a-110">1 represents a site in USMF.</span></span> <span data-ttu-id="e497a-111">Pokud nepoužíváte USMF, vyberte pracoviště z vlastní společnosti.</span><span class="sxs-lookup"><span data-stu-id="e497a-111">If you are not using USMF, select a site from your own company.</span></span>  
3. <span data-ttu-id="e497a-112">Otevřete filtr sloupce Stav.</span><span class="sxs-lookup"><span data-stu-id="e497a-112">Open the Status column filter.</span></span>
4. <span data-ttu-id="e497a-113">Použijte filtr v poli Stav, s hodnotou Plánováno a za použití operátoru filtru „je přesně“.</span><span class="sxs-lookup"><span data-stu-id="e497a-113">Apply a filter on the "Status" field, with a value of "Scheduled", using the "is exactly" filter operator.</span></span>

## <a name="create-a-schedule"></a><span data-ttu-id="e497a-114">Vytvoření plánu</span><span class="sxs-lookup"><span data-stu-id="e497a-114">Create a schedule</span></span>
1. <span data-ttu-id="e497a-115">V seznamu označte všechny řádky nebo jejich označení zrušte.</span><span class="sxs-lookup"><span data-stu-id="e497a-115">In the list, mark or unmark all rows.</span></span>
2. <span data-ttu-id="e497a-116">V podokně akcí klikněte na možnost Plán.</span><span class="sxs-lookup"><span data-stu-id="e497a-116">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="e497a-117">Klikněte na Plánovat úlohy.</span><span class="sxs-lookup"><span data-stu-id="e497a-117">Click Schedule jobs.</span></span>
4. <span data-ttu-id="e497a-118">V poli Způsob plánování vyberte „Zpět od data dodání“.</span><span class="sxs-lookup"><span data-stu-id="e497a-118">In the Scheduling direction field, select 'Backward from delivery date'.</span></span>
5. <span data-ttu-id="e497a-119">Vyberte Ne v poli Omezená kapacita.</span><span class="sxs-lookup"><span data-stu-id="e497a-119">Select No in the Finite capacity field.</span></span>
6. <span data-ttu-id="e497a-120">Vyberte Ne v poli Omezený materiál.</span><span class="sxs-lookup"><span data-stu-id="e497a-120">Select No in the Finite material field.</span></span>
7. <span data-ttu-id="e497a-121">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="e497a-121">Click OK.</span></span>
    * <span data-ttu-id="e497a-122">Tato operace může chvíli trvat.</span><span class="sxs-lookup"><span data-stu-id="e497a-122">This may take a while.</span></span>  

## <a name="view-the-result-of-scheduled-production-orders"></a><span data-ttu-id="e497a-123">Zobrazení výsledků naplánovaných výrobních zakázek</span><span class="sxs-lookup"><span data-stu-id="e497a-123">View the result of scheduled production orders</span></span>
1. <span data-ttu-id="e497a-124">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="e497a-124">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="e497a-125">Můžete označit libovolné řádky.</span><span class="sxs-lookup"><span data-stu-id="e497a-125">You can mark any row.</span></span>  
2. <span data-ttu-id="e497a-126">V podokně akcí klikněte na položku Výrobní zakázka.</span><span class="sxs-lookup"><span data-stu-id="e497a-126">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="e497a-127">Klikněte na Všechny úlohy.</span><span class="sxs-lookup"><span data-stu-id="e497a-127">Click All jobs.</span></span>
    * <span data-ttu-id="e497a-128">Na této stránce můžete vidět seznam úloh.</span><span class="sxs-lookup"><span data-stu-id="e497a-128">On this page, you can see the list of jobs.</span></span> <span data-ttu-id="e497a-129">Na kartě Plánování můžete zobrazit počáteční datum a koncové datum úlohy.</span><span class="sxs-lookup"><span data-stu-id="e497a-129">On the Scheduling tab, you can see the Start date and End date for a job.</span></span>  
4. <span data-ttu-id="e497a-130">Klepněte na Kusovníky.</span><span class="sxs-lookup"><span data-stu-id="e497a-130">Click Materials.</span></span>
    * <span data-ttu-id="e497a-131">Na této stránce se zobrazí odhad spotřeby materiálu pro operace ve výrobní zakázce, a aktuální dostupné zásoby.</span><span class="sxs-lookup"><span data-stu-id="e497a-131">On this page, you can see the estimated material consumption for the operations on the production order and the current available inventory.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]