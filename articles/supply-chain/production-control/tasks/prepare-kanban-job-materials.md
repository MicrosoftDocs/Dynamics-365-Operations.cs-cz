---
title: Příprava kanbanové úlohy procesu, když pro pracovní buňku jsou k dispozici materiály
description: Tento úkol se zaměřuje na přípravu zpracování kanbanové úlohy, pokud jsou všechny materiály k dispozici pro pracovní buňku.
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 714196ba92fe3f57c80809930ed54705a4e75078
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "341941"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-available-for-the-work-cell"></a><span data-ttu-id="bd1dc-103">Příprava kanbanové úlohy procesu, když pro pracovní buňku jsou k dispozici materiály</span><span class="sxs-lookup"><span data-stu-id="bd1dc-103">Prepare a process kanban job when materials are available for the work cell</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bd1dc-104">Tento úkol se zaměřuje na přípravu zpracování kanbanové úlohy, pokud jsou všechny materiály k dispozici pro pracovní buňku.</span><span class="sxs-lookup"><span data-stu-id="bd1dc-104">This task focuses on preparing a process kanban job when all materials are available for the work cell.</span></span> <span data-ttu-id="bd1dc-105">Tento úkol byl vytvořen pomocí ukázkových dat společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="bd1dc-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="bd1dc-106">Tento úkol je určen pro operátora stroje.</span><span class="sxs-lookup"><span data-stu-id="bd1dc-106">This task is intended for the machine operator.</span></span>

1. <span data-ttu-id="bd1dc-107">Přejděte na kanbanovou desku pro úlohy procesu.</span><span class="sxs-lookup"><span data-stu-id="bd1dc-107">Go to Kanban board for process jobs.</span></span>
2. <span data-ttu-id="bd1dc-108">V poli Pracovní buňka kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="bd1dc-108">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="bd1dc-109">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="bd1dc-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="bd1dc-110">Vyberte pracovní buňku 1250 a klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="bd1dc-110">Select work cell 1250 and click OK.</span></span>  
4. <span data-ttu-id="bd1dc-111">Vyberte ze seznamu řádek 4.</span><span class="sxs-lookup"><span data-stu-id="bd1dc-111">In the list, select row 4.</span></span>
    * <span data-ttu-id="bd1dc-112">V prázdné ukázkové společnosti je Kanban 000329 na řádku 4 první úlohou, které ještě není dokončena.</span><span class="sxs-lookup"><span data-stu-id="bd1dc-112">In the clean demo company, Kanban 000329 in row 4 is the first job that is not completed yet.</span></span>  
5. <span data-ttu-id="bd1dc-113">Přepněte rozšíření oddílu Výdejka.</span><span class="sxs-lookup"><span data-stu-id="bd1dc-113">Toggle the expansion of the Picking list section.</span></span>
    * <span data-ttu-id="bd1dc-114">Ověřte, zda stav dodávky je k dispozici pro všechny položky ve výdejce.</span><span class="sxs-lookup"><span data-stu-id="bd1dc-114">Verify that the supply status is available for all items in the picking list.</span></span>  
    * <span data-ttu-id="bd1dc-115">Pokud je vybráno více úloh, výdejky zobrazí součet všech položek, které jsou potřebné pro vybrané úlohy.</span><span class="sxs-lookup"><span data-stu-id="bd1dc-115">If multiple jobs are selected, the picking list will show the sum of all items needed for the selected jobs.</span></span>  
6. <span data-ttu-id="bd1dc-116">Klepněte na Připravit.</span><span class="sxs-lookup"><span data-stu-id="bd1dc-116">Click Prepare.</span></span>
    * <span data-ttu-id="bd1dc-117">Proces přípravy je dokončen.</span><span class="sxs-lookup"><span data-stu-id="bd1dc-117">The preparation process is now completed.</span></span> <span data-ttu-id="bd1dc-118">Označení pole pro všechny řádky výdejky označuje, že je vybrán stav dodání.</span><span class="sxs-lookup"><span data-stu-id="bd1dc-118">The selected check box for all rows in the picking list indicates that the supply status is picked.</span></span>  

