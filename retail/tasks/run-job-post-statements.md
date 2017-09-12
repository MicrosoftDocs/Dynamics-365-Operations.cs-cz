--- 
title: " Konfigurace a spuštění úlohy pro zaúčtování výkazů"
description: "Tento postup vás provede konfigurací a spuštěním opakované dávkové úlohy pro zaúčtování výkazů pro vybraný obchod nebo skupinu obchodů."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 0e2dae54cc9ccfc0a85046c5478e539585c3744d
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---
# <a name="configure-and-run-a-job-to-post-statements"></a><span data-ttu-id="6f46b-103"> Konfigurace a spuštění úlohy pro zaúčtování výkazů</span><span class="sxs-lookup"><span data-stu-id="6f46b-103">Configure and run a job to post statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="6f46b-104">Tento postup vás provede konfigurací a spuštěním opakované dávkové úlohy pro zaúčtování výkazů pro vybraný obchod nebo skupinu obchodů.</span><span class="sxs-lookup"><span data-stu-id="6f46b-104">This procedure walks through configuring and running a recurrent batch job to post statements for a selected store or group of stores.</span></span> <span data-ttu-id="6f46b-105">Tato procedura používá v ukázkových datech společnost USRT.</span><span class="sxs-lookup"><span data-stu-id="6f46b-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="6f46b-106">Přejděte na Všechny pracovní prostory > ..</span><span class="sxs-lookup"><span data-stu-id="6f46b-106">Go to All workspaces > ..</span></span> <span data-ttu-id="6f46b-107">> Finance maloobchodu.</span><span class="sxs-lookup"><span data-stu-id="6f46b-107">> Retail store financials.</span></span>
2. <span data-ttu-id="6f46b-108">Klikněte na Zaúčtovat výkazy.</span><span class="sxs-lookup"><span data-stu-id="6f46b-108">Click Post statements.</span></span>
    * <span data-ttu-id="6f46b-109">Vyberte organizační hierarchii a poté ve stromu uzlů organizace vyberte jednotlivý obchod nebo do uzel.</span><span class="sxs-lookup"><span data-stu-id="6f46b-109">Select an organizational hierarchy and then in the organization nodes tree, select either an individual store or a node.</span></span> <span data-ttu-id="6f46b-110">Pokud chcete vytvořit dávkovou úlohu pro skupinu obchodů, vyberte uzel.</span><span class="sxs-lookup"><span data-stu-id="6f46b-110">Select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="6f46b-111">Kliknutím na šipku přidejte výběr.</span><span class="sxs-lookup"><span data-stu-id="6f46b-111">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="6f46b-112">Klikněte na kartu Spustit na pozadí.</span><span class="sxs-lookup"><span data-stu-id="6f46b-112">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="6f46b-113">Zaškrtněte nebo zrušte zaškrtnutí políčka Dávkové zpracování.</span><span class="sxs-lookup"><span data-stu-id="6f46b-113">Check or uncheck the Batch processing checkbox.</span></span>
5. <span data-ttu-id="6f46b-114">Klepněte na tlačítko Opakování.</span><span class="sxs-lookup"><span data-stu-id="6f46b-114">Click Recurrence.</span></span>
6. <span data-ttu-id="6f46b-115">Zadejte datum do pole Počáteční datum.</span><span class="sxs-lookup"><span data-stu-id="6f46b-115">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="6f46b-116">Zadejte čas do pole Počáteční čas.</span><span class="sxs-lookup"><span data-stu-id="6f46b-116">In the Start time field, enter a time.</span></span>
    * <span data-ttu-id="6f46b-117">Vyberte, zda chcete ukončit opakování po určitém počtu opakování, v konkrétním datu, nebo nikdy.</span><span class="sxs-lookup"><span data-stu-id="6f46b-117">Choose whether you want to end the recurrence after a specific number of runs, at a specific date, or never.</span></span> <span data-ttu-id="6f46b-118">Poté pomocí výběru různých možností definujte, jak často chcete úlohu provádět.</span><span class="sxs-lookup"><span data-stu-id="6f46b-118">Then choose the various options to define how frequently you want the job to run.</span></span>  
8. <span data-ttu-id="6f46b-119">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="6f46b-119">Click OK.</span></span>
9. <span data-ttu-id="6f46b-120">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="6f46b-120">Click OK.</span></span>


