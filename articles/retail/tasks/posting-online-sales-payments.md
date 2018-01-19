--- 
title: " Zaúčtování online prodeje a plateb"
description: "Tato procedura vás provede konfigurací a spuštěním opakující se dávkové úlohy pro vytváření prodejních objednávek a plateb za transakce obchodu online."
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 3799515c538826ac2a0b37a26e83f375591f9813
ms.contentlocale: cs-cz
ms.lasthandoff: 01/19/2018

---
# <a name="post-online-sales-and-payments"></a><span data-ttu-id="6df3e-103"> Zaúčtování online prodeje a plateb</span><span class="sxs-lookup"><span data-stu-id="6df3e-103">Post online sales and payments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="6df3e-104">Tato procedura vás provede konfigurací a spuštěním opakující se dávkové úlohy pro vytváření prodejních objednávek a plateb za transakce obchodu online.</span><span class="sxs-lookup"><span data-stu-id="6df3e-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="6df3e-105">Tato procedura používá v ukázkových datech společnost USRT.</span><span class="sxs-lookup"><span data-stu-id="6df3e-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="6df3e-106">Přejděte na Všechny pracovní prostory > Finance maloobchodu.</span><span class="sxs-lookup"><span data-stu-id="6df3e-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="6df3e-107">Klikněte na Synchronizovat objednávky.</span><span class="sxs-lookup"><span data-stu-id="6df3e-107">Click Synchronize orders.</span></span>
3. <span data-ttu-id="6df3e-108">Vyberte „Maloobchody podle regionu“ v poli Organizační hierarchie.</span><span class="sxs-lookup"><span data-stu-id="6df3e-108">In the Organization hierarchy field, select 'Retail Stores by Region'.</span></span>
    * <span data-ttu-id="6df3e-109">Pokud chcete vytvořit dávkovou úlohu pro skupinu obchodů, vyberte určitý obchod online nebo vyberte uzel.</span><span class="sxs-lookup"><span data-stu-id="6df3e-109">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="6df3e-110">Kliknutím na šipku přidejte výběr.</span><span class="sxs-lookup"><span data-stu-id="6df3e-110">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="6df3e-111">Klikněte na kartu Spustit na pozadí.</span><span class="sxs-lookup"><span data-stu-id="6df3e-111">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="6df3e-112">Zaškrtněte nebo zrušte zaškrtnutí políčka Dávkové zpracování.</span><span class="sxs-lookup"><span data-stu-id="6df3e-112">Check or uncheck the Batch processing checkbox.</span></span>
6. <span data-ttu-id="6df3e-113">Klepněte na tlačítko Opakování.</span><span class="sxs-lookup"><span data-stu-id="6df3e-113">Click Recurrence.</span></span>
7. <span data-ttu-id="6df3e-114">Vyberte možnost Bez koncového data.</span><span class="sxs-lookup"><span data-stu-id="6df3e-114">Select the No end date option.</span></span>
8. <span data-ttu-id="6df3e-115">Zadejte číslo do pole Počet.</span><span class="sxs-lookup"><span data-stu-id="6df3e-115">In the Count field, enter a number.</span></span>
9. <span data-ttu-id="6df3e-116">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="6df3e-116">Click OK.</span></span>
10. <span data-ttu-id="6df3e-117">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="6df3e-117">Click OK.</span></span>


