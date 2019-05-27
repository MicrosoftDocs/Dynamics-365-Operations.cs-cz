---
title: Konfigurace a spuštění úlohy pro zaúčtování výkazů
description: Tento postup vás provede konfigurací a spuštěním opakované dávkové úlohy pro zaúčtování výkazů pro vybraný obchod nebo skupinu obchodů.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 676216d90c50c0d3fa1a839cab7a734e624708ba
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550109"
---
# <a name="configure-and-run-job-to-post-statements"></a><span data-ttu-id="c24cb-103">Konfigurace a spuštění úlohy pro zaúčtování výkazů</span><span class="sxs-lookup"><span data-stu-id="c24cb-103">Configure and run job to post statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="c24cb-104">Tento postup vás provede konfigurací a spuštěním opakované dávkové úlohy pro zaúčtování výkazů pro vybraný obchod nebo skupinu obchodů.</span><span class="sxs-lookup"><span data-stu-id="c24cb-104">This procedure walks through configuring and running a recurrent batch job to post statements for a selected store or group of stores.</span></span> <span data-ttu-id="c24cb-105">Tato procedura používá v ukázkových datech společnost USRT.</span><span class="sxs-lookup"><span data-stu-id="c24cb-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="c24cb-106">Přejděte na Všechny pracovní prostory > ..</span><span class="sxs-lookup"><span data-stu-id="c24cb-106">Go to All workspaces > ..</span></span> <span data-ttu-id="c24cb-107">> Finance maloobchodu.</span><span class="sxs-lookup"><span data-stu-id="c24cb-107">> Retail store financials.</span></span>
2. <span data-ttu-id="c24cb-108">Klikněte na Zaúčtovat výkazy.</span><span class="sxs-lookup"><span data-stu-id="c24cb-108">Click Post statements.</span></span>
    * <span data-ttu-id="c24cb-109">Vyberte organizační hierarchii a poté ve stromu uzlů organizace vyberte jednotlivý obchod nebo do uzel.</span><span class="sxs-lookup"><span data-stu-id="c24cb-109">Select an organizational hierarchy and then in the organization nodes tree, select either an individual store or a node.</span></span> <span data-ttu-id="c24cb-110">Pokud chcete vytvořit dávkovou úlohu pro skupinu obchodů, vyberte uzel.</span><span class="sxs-lookup"><span data-stu-id="c24cb-110">Select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="c24cb-111">Kliknutím na šipku přidejte výběr.</span><span class="sxs-lookup"><span data-stu-id="c24cb-111">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="c24cb-112">Klikněte na kartu Spustit na pozadí.</span><span class="sxs-lookup"><span data-stu-id="c24cb-112">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="c24cb-113">Zaškrtněte nebo zrušte zaškrtnutí políčka Dávkové zpracování.</span><span class="sxs-lookup"><span data-stu-id="c24cb-113">Check or uncheck the Batch processing checkbox.</span></span>
5. <span data-ttu-id="c24cb-114">Klepněte na tlačítko Opakování.</span><span class="sxs-lookup"><span data-stu-id="c24cb-114">Click Recurrence.</span></span>
6. <span data-ttu-id="c24cb-115">Zadejte datum do pole Počáteční datum.</span><span class="sxs-lookup"><span data-stu-id="c24cb-115">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="c24cb-116">Zadejte čas do pole Počáteční čas.</span><span class="sxs-lookup"><span data-stu-id="c24cb-116">In the Start time field, enter a time.</span></span>
    * <span data-ttu-id="c24cb-117">Vyberte, zda chcete ukončit opakování po určitém počtu opakování, v konkrétním datu, nebo nikdy.</span><span class="sxs-lookup"><span data-stu-id="c24cb-117">Choose whether you want to end the recurrence after a specific number of runs, at a specific date, or never.</span></span> <span data-ttu-id="c24cb-118">Poté pomocí výběru různých možností definujte, jak často chcete úlohu provádět.</span><span class="sxs-lookup"><span data-stu-id="c24cb-118">Then choose the various options to define how frequently you want the job to run.</span></span>  
8. <span data-ttu-id="c24cb-119">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c24cb-119">Click OK.</span></span>
9. <span data-ttu-id="c24cb-120">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c24cb-120">Click OK.</span></span>

