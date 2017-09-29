--- 
title: " Konfigurace a spuštění úlohy pro výpočet výkazů"
description: "Tento postup vás provede konfigurací a spuštěním opakovaných dávkových úloh pro tvorbu a výpočet výkazů pro vybraný obchod nebo skupinu obchodů."
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
ms.openlocfilehash: 2bae81073fa6561c02d2dac0cd83db6a10ad00c3
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---
# <a name="configure-and-run-a-job-to-calculate-statements"></a><span data-ttu-id="ef907-103"> Konfigurace a spuštění úlohy pro výpočet výkazů</span><span class="sxs-lookup"><span data-stu-id="ef907-103">Configure and run a job to calculate statements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="ef907-104">Tento postup vás provede konfigurací a spuštěním opakovaných dávkových úloh pro tvorbu a výpočet výkazů pro vybraný obchod nebo skupinu obchodů.</span><span class="sxs-lookup"><span data-stu-id="ef907-104">This procedure walks through configuring and running recurrent batch jobs to create and calculate statements for a selected store or group of stores.</span></span> <span data-ttu-id="ef907-105">Tato procedura používá v ukázkových datech společnost USRT.</span><span class="sxs-lookup"><span data-stu-id="ef907-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="ef907-106">Přejděte na Všechny pracovní prostory > Finance maloobchodu.</span><span class="sxs-lookup"><span data-stu-id="ef907-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="ef907-107">Klikněte na Vypočítat výkazy.</span><span class="sxs-lookup"><span data-stu-id="ef907-107">Click Calculate statements.</span></span>
    * <span data-ttu-id="ef907-108">Pokud chcete vytvořit dávkovou úlohu pro skupinu obchodů, vyberte určitý obchod nebo uzel.</span><span class="sxs-lookup"><span data-stu-id="ef907-108">Select either a specific store, or a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="ef907-109">Kliknutím na šipku přidejte výběr.</span><span class="sxs-lookup"><span data-stu-id="ef907-109">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="ef907-110">Klikněte na kartu Spustit na pozadí.</span><span class="sxs-lookup"><span data-stu-id="ef907-110">Click the Run in the background tab.</span></span>
4. <span data-ttu-id="ef907-111">Vyberte možnost „Ano“ v části Dávkové zpracování.</span><span class="sxs-lookup"><span data-stu-id="ef907-111">Under Batch processing, select 'Yes'.</span></span>
5. <span data-ttu-id="ef907-112">Klepněte na tlačítko Opakování.</span><span class="sxs-lookup"><span data-stu-id="ef907-112">Click Recurrence.</span></span>
6. <span data-ttu-id="ef907-113">Zadejte datum do pole Počáteční datum.</span><span class="sxs-lookup"><span data-stu-id="ef907-113">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="ef907-114">Zadejte čas do pole Počáteční čas.</span><span class="sxs-lookup"><span data-stu-id="ef907-114">In the Start time field, enter a time.</span></span>
8. <span data-ttu-id="ef907-115">Vyberte možnost Bez koncového data.</span><span class="sxs-lookup"><span data-stu-id="ef907-115">Select the No end date option.</span></span>
9. <span data-ttu-id="ef907-116">V poli PatternUnit zadejte „Dny“.</span><span class="sxs-lookup"><span data-stu-id="ef907-116">In the PatternUnit field, enter 'Days'.</span></span>
10. <span data-ttu-id="ef907-117">Do pole Za zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="ef907-117">In the Per field, enter a number.</span></span>
11. <span data-ttu-id="ef907-118">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="ef907-118">Click OK.</span></span>
12. <span data-ttu-id="ef907-119">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="ef907-119">Click OK.</span></span>


