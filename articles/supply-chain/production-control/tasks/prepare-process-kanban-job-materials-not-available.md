---
title: Příprava kanbanové úlohy procesu, když pro pracovní buňku nejsou k dispozici materiály
description: Tento postup se zaměřuje na přípravu zpracování kanbanové úlohy, když nejsou k dispozici některé materiály pro pracovní buňku, a je tak nutné vybrat materiály ze skladu.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d57df6188aacc2f8a56a7ba91c4ab50a90901a7e
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206892"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-not-available-for-the-work-cell"></a><span data-ttu-id="d5aca-103">Příprava kanbanové úlohy procesu, když pro pracovní buňku nejsou k dispozici materiály</span><span class="sxs-lookup"><span data-stu-id="d5aca-103">Prepare a process kanban job when materials are not available for the work cell</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d5aca-104">Tento postup se zaměřuje na přípravu zpracování kanbanové úlohy, když nejsou k dispozici některé materiály pro pracovní buňku, a je tak nutné vybrat materiály ze skladu.</span><span class="sxs-lookup"><span data-stu-id="d5aca-104">This procedure focuses on preparing a process kanban job when some materials are not available for the work cell, therefore it's necessary to pick materials from the warehouse.</span></span> <span data-ttu-id="d5aca-105">Postup "Příprava procesní kanbanové úlohy, pokud jsou materiály k dispozici" je předpokladem pro vytvoření tohoto postupu.</span><span class="sxs-lookup"><span data-stu-id="d5aca-105">The procedure "Prepare a process kanban job when materials are available" is a prerequisite for creating this procedure.</span></span> <span data-ttu-id="d5aca-106">Tento postup je určen pro operátora stroje.</span><span class="sxs-lookup"><span data-stu-id="d5aca-106">This procedure is intended for the machine operator.</span></span> <span data-ttu-id="d5aca-107">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="d5aca-107">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="d5aca-108">Přejděte na Řízení výroby > Kanban > Kanbanová deska pro úlohy zpracování.</span><span class="sxs-lookup"><span data-stu-id="d5aca-108">Go to Production control > Kanban > Kanban board for process jobs.</span></span>
2. <span data-ttu-id="d5aca-109">V poli Pracovní buňka kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="d5aca-109">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="d5aca-110">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="d5aca-110">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="d5aca-111">Vyberte pracovní buňku 1250.</span><span class="sxs-lookup"><span data-stu-id="d5aca-111">Select work cell 1250.</span></span>  
4. <span data-ttu-id="d5aca-112">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="d5aca-112">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d5aca-113">Vyberte Kanban 000356.</span><span class="sxs-lookup"><span data-stu-id="d5aca-113">Select Kanban 000356.</span></span>  
5. <span data-ttu-id="d5aca-114">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="d5aca-114">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d5aca-115">V seznamu zrušte výběr řádku 4.</span><span class="sxs-lookup"><span data-stu-id="d5aca-115">In the list, deselect row 4.</span></span> <span data-ttu-id="d5aca-116">nebo vyberte řádek 4, pokud jste nedokončili úkolu "Příprava procesní kanbanové úlohy, jakmile jsou materiály k dispozici."</span><span class="sxs-lookup"><span data-stu-id="d5aca-116">or Select row 4 if you haven't completed the task "Prepare a process kanban job when materials are available."</span></span>  
6. <span data-ttu-id="d5aca-117">Přepněte rozšíření oddílu Výdejka.</span><span class="sxs-lookup"><span data-stu-id="d5aca-117">Toggle the expansion of the Picking list section.</span></span>
    * <span data-ttu-id="d5aca-118">Ikona Žádný záznam ve stavu dodávky udává, že 48 z každé položky P0002 chybí pro pracovní buňku.</span><span class="sxs-lookup"><span data-stu-id="d5aca-118">The No entry icon in the supply status indicates that 48 ea of item P0002 are missing for the work cell.</span></span>  

## <a name="transfer-materials-to-work-cell"></a><span data-ttu-id="d5aca-119">Převod materiálů do pracovní buňky</span><span class="sxs-lookup"><span data-stu-id="d5aca-119">Transfer materials to work cell</span></span>
1. <span data-ttu-id="d5aca-120">Přepněte rozšíření oddílu Úlohy převodů.</span><span class="sxs-lookup"><span data-stu-id="d5aca-120">Toggle the expansion of the Transfer jobs section.</span></span>
2. <span data-ttu-id="d5aca-121">Použijte rychlý filtr k filtrování v poli Číslo položky na základě hodnoty P0002.</span><span class="sxs-lookup"><span data-stu-id="d5aca-121">Use the Quick Filter to filter on the Item number field with a value of 'P0002'.</span></span>
3. <span data-ttu-id="d5aca-122">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="d5aca-122">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="d5aca-123">Klikněte na položku Spustit.</span><span class="sxs-lookup"><span data-stu-id="d5aca-123">Click Start.</span></span>
    * <span data-ttu-id="d5aca-124">Probíhá přenos.</span><span class="sxs-lookup"><span data-stu-id="d5aca-124">Transfer is in progress.</span></span>  
5. <span data-ttu-id="d5aca-125">Klikněte na tlačítko Dokončit.</span><span class="sxs-lookup"><span data-stu-id="d5aca-125">Click Complete.</span></span>
    * <span data-ttu-id="d5aca-126">Položka P0002 je nyní k dispozici na výdejce pro kanbanovou úlohu.</span><span class="sxs-lookup"><span data-stu-id="d5aca-126">Item P0002 is now available in the picking list for the kanban job.</span></span> <span data-ttu-id="d5aca-127">To znamená, že můžeme připravit kanban se všemi potřebnými materiály.</span><span class="sxs-lookup"><span data-stu-id="d5aca-127">This means that we can prepare the kanban with all the needed materials.</span></span>  
6. <span data-ttu-id="d5aca-128">Klepněte na Připravit.</span><span class="sxs-lookup"><span data-stu-id="d5aca-128">Click Prepare.</span></span>
    * <span data-ttu-id="d5aca-129">Všimněte si, že ikona ve stavu úlohy označuje, že úloha je nyní připravena.</span><span class="sxs-lookup"><span data-stu-id="d5aca-129">Notice that an icon in the Job status indicates that the job is now ready.</span></span>  

