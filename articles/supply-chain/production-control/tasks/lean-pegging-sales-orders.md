---
title: Doložení z prodejních objednávek štíhlé výroby
description: Tento postup se zaměřuje na ověřování stromu doložení z řádku prodeje, kde položka je vyráběna s kanbany.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ff57169ea58a90d1113bb7ef0a581f900e62a9b2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828555"
---
# <a name="lean-pegging-from-sales-orders"></a><span data-ttu-id="ff4b0-103">Doložení z prodejních objednávek štíhlé výroby</span><span class="sxs-lookup"><span data-stu-id="ff4b0-103">Lean pegging from sales orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ff4b0-104">Tento postup se zaměřuje na ověřování stromu doložení z řádku prodeje, kde položka je vyráběna s kanbany.</span><span class="sxs-lookup"><span data-stu-id="ff4b0-104">This procedure focuses on validating the pegging tree from a sales line where the item is produced with kanbans.</span></span> <span data-ttu-id="ff4b0-105">Po ověření stromu doložení jsou plánovány všechny kanbanové úlohy.</span><span class="sxs-lookup"><span data-stu-id="ff4b0-105">After validating the pegging tree, all the kanban jobs are planned.</span></span> <span data-ttu-id="ff4b0-106">To je užitečné pro objednávky scénáře, kde pořadí příjemce musí zajistit, aby bylo možné výrobu spustit přímo.</span><span class="sxs-lookup"><span data-stu-id="ff4b0-106">This is useful for order scenarios where the order taker needs to ensure that production can start right away.</span></span> <span data-ttu-id="ff4b0-107">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="ff4b0-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="ff4b0-108">Tento postup je určen pro rozšířenou objednávku příjemce pracující ve štíhlé společnosti.</span><span class="sxs-lookup"><span data-stu-id="ff4b0-108">This procedure is intended for the advanced order taker working in a lean company.</span></span>


## <a name="create-a-sales-order-for-a-kanban-controlled-item"></a><span data-ttu-id="ff4b0-109">Vytvořte prodejní objednávky pro položku řízenou kanbanem</span><span class="sxs-lookup"><span data-stu-id="ff4b0-109">Create a sales order for a kanban controlled item</span></span>
1. <span data-ttu-id="ff4b0-110">Přejděte na Všechny prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="ff4b0-110">Go to All sales orders.</span></span>
2. <span data-ttu-id="ff4b0-111">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="ff4b0-111">Click New.</span></span>
3. <span data-ttu-id="ff4b0-112">V poli Účet odběratele zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ff4b0-112">In the Customer account field, enter or select a value.</span></span>
    * <span data-ttu-id="ff4b0-113">Použití US-001.</span><span class="sxs-lookup"><span data-stu-id="ff4b0-113">Use US-001.</span></span>  
4. <span data-ttu-id="ff4b0-114">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="ff4b0-114">Click OK.</span></span>
5. <span data-ttu-id="ff4b0-115">Do pole Číslo položky zadejte L0001.</span><span class="sxs-lookup"><span data-stu-id="ff4b0-115">In the Item number field, type 'L0001'.</span></span>
6. <span data-ttu-id="ff4b0-116">Nastavte množství na hodnotu 30.</span><span class="sxs-lookup"><span data-stu-id="ff4b0-116">Set Quantity to '30'.</span></span>
    * <span data-ttu-id="ff4b0-117">Je důležité, aby množství bylo vyšší než 24 za účelem aktivace pravidla kanbanové události.</span><span class="sxs-lookup"><span data-stu-id="ff4b0-117">It is important that the quantity is higher than 24 in order to trigger the event kanban rule.</span></span>  

## <a name="open-a-pegging-tree"></a><span data-ttu-id="ff4b0-118">Otevřete strom doložení</span><span class="sxs-lookup"><span data-stu-id="ff4b0-118">Open a pegging tree</span></span> 
1. <span data-ttu-id="ff4b0-119">Klikněte na Produkt a dodávka.</span><span class="sxs-lookup"><span data-stu-id="ff4b0-119">Click Product and supply.</span></span>
2. <span data-ttu-id="ff4b0-120">Klepněte na Zobrazit strom doložení.</span><span class="sxs-lookup"><span data-stu-id="ff4b0-120">Click View pegging tree.</span></span>
    * <span data-ttu-id="ff4b0-121">Všimněte si, že strom doložení zobrazuje všechny úrovně doložení pro řádek prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="ff4b0-121">Notice that the pegging tree shows all levels of the pegging needed for the sales order line.</span></span> <span data-ttu-id="ff4b0-122">V tomto případě existují dvě úrovně kanbanů a všechny potřebné součásti.</span><span class="sxs-lookup"><span data-stu-id="ff4b0-122">In this case, there are two levels of kanbans and all the required components.</span></span>  

## <a name="plan-the-pegging-tree"></a><span data-ttu-id="ff4b0-123">Naplánovat strom doložení</span><span class="sxs-lookup"><span data-stu-id="ff4b0-123">Plan the pegging tree</span></span>
1. <span data-ttu-id="ff4b0-124">Ve stromovém zobrazení vyberte „Řádek prodeje 000832\Kanban 000558“.</span><span class="sxs-lookup"><span data-stu-id="ff4b0-124">In the tree, select 'Sales line 000832\Kanban 000558'.</span></span>
2. <span data-ttu-id="ff4b0-125">Rozbalte část Kanbanové úlohy.</span><span class="sxs-lookup"><span data-stu-id="ff4b0-125">Expand the Kanban jobs section.</span></span>
    * <span data-ttu-id="ff4b0-126">Všimněte si, že stav úlohy pro kanbanovou úlohu je Nenaplánováno.</span><span class="sxs-lookup"><span data-stu-id="ff4b0-126">Notice that the job status for the kanban job is Not planned.</span></span>  
3. <span data-ttu-id="ff4b0-127">Klikněte na Naplánovat celý strom doložení.</span><span class="sxs-lookup"><span data-stu-id="ff4b0-127">Click Plan entire pegging tree.</span></span>
    * <span data-ttu-id="ff4b0-128">Tímto naplánujete všechny kanbanové úlohy ve stromu doložení, změníte stav úlohy z Není plánováno na Plánováno.</span><span class="sxs-lookup"><span data-stu-id="ff4b0-128">This will plan all kanban jobs in the pegging tree, changing the Job status from Not planned to Planned.</span></span>  
4. <span data-ttu-id="ff4b0-129">Aktualizujte stránku.</span><span class="sxs-lookup"><span data-stu-id="ff4b0-129">Refresh the page.</span></span>
    * <span data-ttu-id="ff4b0-130">Všimněte si, že stav kanbanové úlohy se změní z Nenaplánováno na Naplánováno.</span><span class="sxs-lookup"><span data-stu-id="ff4b0-130">Notice that the kanban Job status changed from Not planned to Planned.</span></span>  
5. <span data-ttu-id="ff4b0-131">Ve stromovém zobrazení vyberte „Řádek prodeje 000832\Kanban 000558\Výdej pro L0001\Kanban 000559“.</span><span class="sxs-lookup"><span data-stu-id="ff4b0-131">In the tree, select 'Sales line 000832\Kanban 000558\Issue for L0001\Kanban 000559'.</span></span>
    * <span data-ttu-id="ff4b0-132">Úloha pro druhý kanban je také plánována, protože celý strom doložení je plánován.</span><span class="sxs-lookup"><span data-stu-id="ff4b0-132">The job for the second kanban is also planned, because the entire pegging tree is planned.</span></span> <span data-ttu-id="ff4b0-133">Všimněte si, že stav kanbanové úlohy bude změněn z Nenaplánováno na Naplánováno.</span><span class="sxs-lookup"><span data-stu-id="ff4b0-133">Notice that the kanban job status is changed from Not planned to Planned.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]