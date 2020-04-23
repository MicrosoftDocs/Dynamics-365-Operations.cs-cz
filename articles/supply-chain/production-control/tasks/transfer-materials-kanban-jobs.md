---
title: Převedení materiálu s kanbanovými úlohami
description: Tento postup se zaměřuje na provádění kanbanové úlohy pro výběr umožňující převod materiálu.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 96cb77b7b37fe6519a812735d9a41749da078cf2
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210357"
---
# <a name="transfer-materials-with-kanban-jobs"></a><span data-ttu-id="0aec7-103">Převedení materiálu s kanbanovými úlohami</span><span class="sxs-lookup"><span data-stu-id="0aec7-103">Transfer materials with kanban jobs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0aec7-104">Tento postup se zaměřuje na provádění kanbanové úlohy pro výběr umožňující převod materiálu.</span><span class="sxs-lookup"><span data-stu-id="0aec7-104">This procedure focuses on executing a withdrawal kanban job to transfer materials.</span></span> <span data-ttu-id="0aec7-105">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="0aec7-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="0aec7-106">Tento postup je určen pro pracovníka skladu.</span><span class="sxs-lookup"><span data-stu-id="0aec7-106">This procedure is intended for the warehouse worker.</span></span>


## <a name="display-transfer-jobs"></a><span data-ttu-id="0aec7-107">Zobrazení úloh převodu</span><span class="sxs-lookup"><span data-stu-id="0aec7-107">Display transfer jobs</span></span>
1. <span data-ttu-id="0aec7-108">Přejděte na Řízení výroby > Kanban > Kanbanová deska pro úlohy převodu.</span><span class="sxs-lookup"><span data-stu-id="0aec7-108">Go to Production control > Kanban > Kanban board for transfer jobs.</span></span>
2. <span data-ttu-id="0aec7-109">Rozbalte nebo sbalte oddíl Filtry.</span><span class="sxs-lookup"><span data-stu-id="0aec7-109">Expand or collapse the Filters section.</span></span>
    * <span data-ttu-id="0aec7-110">V části Filtry můžete určit, jaké úlohy chcete zobrazit filtrováním výrobního toku, názvu aktivity, původu (ze skladu a umístění) a cíle (do skladu a umístění).</span><span class="sxs-lookup"><span data-stu-id="0aec7-110">In the Filters section, you can specify what jobs you want to see by filtering on Production flow, Activity name, From warehouse and location, and To warehouse and location.</span></span>  
3. <span data-ttu-id="0aec7-111">Zadejte hodnotu 11 do pole Ze skladu.</span><span class="sxs-lookup"><span data-stu-id="0aec7-111">In the From warehouse field, type '11'.</span></span>
4. <span data-ttu-id="0aec7-112">Zadejte hodnotu 12 do pole Do umístění.</span><span class="sxs-lookup"><span data-stu-id="0aec7-112">In the To location field, type '12'.</span></span>

## <a name="start-a-transfer-job"></a><span data-ttu-id="0aec7-113">Zahájit úlohu převodu</span><span class="sxs-lookup"><span data-stu-id="0aec7-113">Start a transfer job</span></span>
1. <span data-ttu-id="0aec7-114">Odznačte případně vybraný řádek na seznamu.</span><span class="sxs-lookup"><span data-stu-id="0aec7-114">In the list, deselect the selected row - if any.</span></span>
2. <span data-ttu-id="0aec7-115">Vyberte ze seznamu řádek 4.</span><span class="sxs-lookup"><span data-stu-id="0aec7-115">In the list, select row 4.</span></span>
    * <span data-ttu-id="0aec7-116">Vyberte první úlohu se stavem Neplánováno.</span><span class="sxs-lookup"><span data-stu-id="0aec7-116">Select the first job with status Not planned.</span></span> <span data-ttu-id="0aec7-117">Ujistěte se, že se jedná o jedinou vybranou úlohu.</span><span class="sxs-lookup"><span data-stu-id="0aec7-117">Make sure this is the only job selected.</span></span>  
3. <span data-ttu-id="0aec7-118">Klikněte na položku Spustit.</span><span class="sxs-lookup"><span data-stu-id="0aec7-118">Click Start.</span></span>
    * <span data-ttu-id="0aec7-119">Všimněte si, že ikona označuje, zda je úloha spuštěna.</span><span class="sxs-lookup"><span data-stu-id="0aec7-119">Notice that an icon indicates that the job is started.</span></span>  

## <a name="select-a-second-transfer-job-and-change-quantity"></a><span data-ttu-id="0aec7-120">Výběr druhé úlohy převodu a změna množství</span><span class="sxs-lookup"><span data-stu-id="0aec7-120">Select a second transfer job and change quantity</span></span>
1. <span data-ttu-id="0aec7-121">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="0aec7-121">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0aec7-122">Můžete mít vybraných více úloh, ale nyní vyberte řádek 5.</span><span class="sxs-lookup"><span data-stu-id="0aec7-122">You can have multiple jobs selected, but for now select row 5.</span></span>  
2. <span data-ttu-id="0aec7-123">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="0aec7-123">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="0aec7-124">Ujistěte se, že je vybrána pouze úloha v předchozím kroku.</span><span class="sxs-lookup"><span data-stu-id="0aec7-124">Make sure the job in the previous step is the only one selected.</span></span> <span data-ttu-id="0aec7-125">Zrušte všechny ostatní úlohy.</span><span class="sxs-lookup"><span data-stu-id="0aec7-125">Deselect all other jobs.</span></span>  
3. <span data-ttu-id="0aec7-126">Poznamenejte si hodnotu v poli Množství úlohy pro pozdější potřebu.</span><span class="sxs-lookup"><span data-stu-id="0aec7-126">Note the value in the Job quantity field to reference later</span></span>
4. <span data-ttu-id="0aec7-127">Nastavte Množství úlohy na „30“.</span><span class="sxs-lookup"><span data-stu-id="0aec7-127">Set Job quantity to '30'.</span></span>
    * <span data-ttu-id="0aec7-128">Všimněte si upozornění.</span><span class="sxs-lookup"><span data-stu-id="0aec7-128">Notice the warning!</span></span> <span data-ttu-id="0aec7-129">Nemáte oprávnění převést 30.</span><span class="sxs-lookup"><span data-stu-id="0aec7-129">You are not allowed to transfer 30.</span></span> <span data-ttu-id="0aec7-130">Podle nastavení kanbanového pravidla lze převést pouze původní množství.</span><span class="sxs-lookup"><span data-stu-id="0aec7-130">According to the setup of the kanban rule, you can only transfer the original quantity.</span></span>  
5. <span data-ttu-id="0aec7-131">Použijte hodnotu pole Množství úlohy, kterou jste si dříve zapsali.</span><span class="sxs-lookup"><span data-stu-id="0aec7-131">Use the value noted previously in the Job quantity field</span></span>
    * <span data-ttu-id="0aec7-132">Nastavte Množství úlohy na předchozí hodnotu.</span><span class="sxs-lookup"><span data-stu-id="0aec7-132">Set the Job quantity to the previous value.</span></span>  

## <a name="start-the-second-transfer-job"></a><span data-ttu-id="0aec7-133">Spuštění druhé úlohy převodu</span><span class="sxs-lookup"><span data-stu-id="0aec7-133">Start the second transfer job</span></span>
1. <span data-ttu-id="0aec7-134">Klikněte na položku Spustit.</span><span class="sxs-lookup"><span data-stu-id="0aec7-134">Click Start.</span></span>
    * <span data-ttu-id="0aec7-135">Tato akce spustí převod úlohy z řádku 5.</span><span class="sxs-lookup"><span data-stu-id="0aec7-135">This will start the transfer of the job in row 5.</span></span>  

## <a name="complete-both-transfer-jobs"></a><span data-ttu-id="0aec7-136">Dokončení obou úloh převodu</span><span class="sxs-lookup"><span data-stu-id="0aec7-136">Complete both transfer jobs</span></span>
1. <span data-ttu-id="0aec7-137">Vyberte ze seznamu řádek 4.</span><span class="sxs-lookup"><span data-stu-id="0aec7-137">In the list, select row 4.</span></span>
    * <span data-ttu-id="0aec7-138">Nyní jsou vybrány dvě úlohy převodu – na řádku 4 a 5.</span><span class="sxs-lookup"><span data-stu-id="0aec7-138">Now two transfer jobs are selected on row 4 and row 5.</span></span>  
2. <span data-ttu-id="0aec7-139">Klikněte na tlačítko Dokončit.</span><span class="sxs-lookup"><span data-stu-id="0aec7-139">Click Complete.</span></span>
    * <span data-ttu-id="0aec7-140">Tímto dokončíte převod obou úloh.</span><span class="sxs-lookup"><span data-stu-id="0aec7-140">This will complete the transfer of both jobs.</span></span>  

