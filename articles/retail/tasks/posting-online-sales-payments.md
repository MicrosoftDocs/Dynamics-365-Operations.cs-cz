--- 
title: "Zaúčtování online prodeje a plateb"
description: "Tato procedura vás provede konfigurací a spuštěním opakující se dávkové úlohy pro vytváření prodejních objednávek a plateb za transakce obchodu online."
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 13839bbe6ca03f3cfc7036fce87477bf7d5af2a7
ms.contentlocale: cs-cz
ms.lasthandoff: 09/14/2018

---
# <a name="posting-of-online-sales-and-payments"></a><span data-ttu-id="d6d60-103">Zaúčtování online prodeje a plateb</span><span class="sxs-lookup"><span data-stu-id="d6d60-103">Posting of online sales and payments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="d6d60-104">Tato procedura vás provede konfigurací a spuštěním opakující se dávkové úlohy pro vytváření prodejních objednávek a plateb za transakce obchodu online.</span><span class="sxs-lookup"><span data-stu-id="d6d60-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="d6d60-105">Tato procedura používá v ukázkových datech společnost USRT.</span><span class="sxs-lookup"><span data-stu-id="d6d60-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="d6d60-106">Přejděte na Všechny pracovní prostory > Finance maloobchodu.</span><span class="sxs-lookup"><span data-stu-id="d6d60-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="d6d60-107">Klikněte na Synchronizovat objednávky.</span><span class="sxs-lookup"><span data-stu-id="d6d60-107">Click Synchronize orders.</span></span>
3. <span data-ttu-id="d6d60-108">Vyberte „Maloobchody podle regionu“ v poli Organizační hierarchie.</span><span class="sxs-lookup"><span data-stu-id="d6d60-108">In the Organization hierarchy field, select 'Retail Stores by Region'.</span></span>
    * <span data-ttu-id="d6d60-109">Pokud chcete vytvořit dávkovou úlohu pro skupinu obchodů, vyberte určitý obchod online nebo vyberte uzel.</span><span class="sxs-lookup"><span data-stu-id="d6d60-109">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="d6d60-110">Kliknutím na šipku přidejte výběr.</span><span class="sxs-lookup"><span data-stu-id="d6d60-110">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="d6d60-111">Klikněte na kartu Spustit na pozadí.</span><span class="sxs-lookup"><span data-stu-id="d6d60-111">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="d6d60-112">Zaškrtněte nebo zrušte zaškrtnutí políčka Dávkové zpracování.</span><span class="sxs-lookup"><span data-stu-id="d6d60-112">Check or uncheck the Batch processing checkbox.</span></span>
6. <span data-ttu-id="d6d60-113">Klepněte na tlačítko Opakování.</span><span class="sxs-lookup"><span data-stu-id="d6d60-113">Click Recurrence.</span></span>
7. <span data-ttu-id="d6d60-114">Vyberte možnost Bez koncového data.</span><span class="sxs-lookup"><span data-stu-id="d6d60-114">Select the No end date option.</span></span>
8. <span data-ttu-id="d6d60-115">Zadejte číslo do pole Počet.</span><span class="sxs-lookup"><span data-stu-id="d6d60-115">In the Count field, enter a number.</span></span>
9. <span data-ttu-id="d6d60-116">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="d6d60-116">Click OK.</span></span>
10. <span data-ttu-id="d6d60-117">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="d6d60-117">Click OK.</span></span>


