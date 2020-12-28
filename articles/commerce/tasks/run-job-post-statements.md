---
title: Konfigurace a spuštění úlohy pro zaúčtování výkazů
description: Tento postup vás provede konfigurací a spuštěním opakované dávkové úlohy pro zaúčtování výkazů pro vybraný obchod nebo skupinu obchodů.
author: josaw1
manager: AnnBe
ms.date: 07/29/2019
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
ms.openlocfilehash: f89203850b302b769b22920fa5c42d2b0b877684
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4410815"
---
# <a name="configure-and-run-job-to-post-statements"></a><span data-ttu-id="83079-103">Konfigurace a spuštění úlohy pro zaúčtování výkazů</span><span class="sxs-lookup"><span data-stu-id="83079-103">Configure and run job to post statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="83079-104">Tento postup vás provede konfigurací a spuštěním opakované dávkové úlohy pro zaúčtování výkazů pro vybraný obchod nebo skupinu obchodů.</span><span class="sxs-lookup"><span data-stu-id="83079-104">This procedure walks through configuring and running a recurrent batch job to post statements for a selected store or group of stores.</span></span> <span data-ttu-id="83079-105">Tato procedura používá v ukázkových datech společnost USRT.</span><span class="sxs-lookup"><span data-stu-id="83079-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="83079-106">Přejděte na Všechny pracovní prostory > ..</span><span class="sxs-lookup"><span data-stu-id="83079-106">Go to All workspaces > ..</span></span> <span data-ttu-id="83079-107">> Finance obchodu.</span><span class="sxs-lookup"><span data-stu-id="83079-107">> Store financials.</span></span>
2. <span data-ttu-id="83079-108">Klikněte na Zaúčtovat příkazy v dávkách.</span><span class="sxs-lookup"><span data-stu-id="83079-108">Click Post statements in batch.</span></span>
    * <span data-ttu-id="83079-109">Vyberte organizační hierarchii a poté ve stromu uzlů organizace vyberte jednotlivý obchod nebo do uzel.</span><span class="sxs-lookup"><span data-stu-id="83079-109">Select an organizational hierarchy and then in the organization nodes tree, select either an individual store or a node.</span></span> <span data-ttu-id="83079-110">Pokud chcete vytvořit dávkovou úlohu pro skupinu obchodů, vyberte uzel.</span><span class="sxs-lookup"><span data-stu-id="83079-110">Select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="83079-111">Kliknutím na šipku přidejte výběr.</span><span class="sxs-lookup"><span data-stu-id="83079-111">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="83079-112">Klikněte na kartu Spustit na pozadí. ![Spustit na pozadí](../dev-itpro/media/runbackground.png "Spustit na pozadí")</span><span class="sxs-lookup"><span data-stu-id="83079-112">Click the Run in the background tab. ![Run in the background](../dev-itpro/media/runbackground.png "Run in the background")</span></span> 
4. <span data-ttu-id="83079-113">Zaškrtněte nebo zrušte zaškrtnutí políčka Dávkové zpracování.</span><span class="sxs-lookup"><span data-stu-id="83079-113">Check or uncheck the Batch processing checkbox.</span></span>
<span data-ttu-id="83079-114">![Dávkové zpracování](../dev-itpro/media/batchprocessing.png "Dávkové zpracování a opakování")</span><span class="sxs-lookup"><span data-stu-id="83079-114">![Batch Processing](../dev-itpro/media/batchprocessing.png "Batch Processing & Recurrance")</span></span> 
5. <span data-ttu-id="83079-115">Klepněte na tlačítko Opakování.</span><span class="sxs-lookup"><span data-stu-id="83079-115">Click Recurrence.</span></span>
6. <span data-ttu-id="83079-116">Zadejte datum do pole Počáteční datum.</span><span class="sxs-lookup"><span data-stu-id="83079-116">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="83079-117">Zadejte čas do pole Počáteční čas.</span><span class="sxs-lookup"><span data-stu-id="83079-117">In the Start time field, enter a time.</span></span>
    * <span data-ttu-id="83079-118">Vyberte, zda chcete ukončit opakování po určitém počtu opakování, v konkrétním datu, nebo nikdy.</span><span class="sxs-lookup"><span data-stu-id="83079-118">Choose whether you want to end the recurrence after a specific number of runs, at a specific date, or never.</span></span> <span data-ttu-id="83079-119">Poté pomocí výběru různých možností definujte, jak často chcete úlohu provádět.</span><span class="sxs-lookup"><span data-stu-id="83079-119">Then choose the various options to define how frequently you want the job to run.</span></span>  
8. <span data-ttu-id="83079-120">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="83079-120">Click OK.</span></span>
9. <span data-ttu-id="83079-121">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="83079-121">Click OK.</span></span>

