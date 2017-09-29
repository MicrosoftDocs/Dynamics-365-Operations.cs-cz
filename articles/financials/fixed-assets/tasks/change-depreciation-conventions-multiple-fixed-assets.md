--- 
title: "Změna způsobu odpisu pro více položek dlouhodobého majetku"
description: "Tato úloha aktualizuje způsob odpisu pro uvedenou skupinu dlouhodobého majetku."
author: saraschi2
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 0f711d2e18a13ab972e548d3304652dee3f2e406
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---
# <a name="change-depreciation-conventions-for-multiple-fixed-assets"></a><span data-ttu-id="41b53-103">Změna způsobu odpisu pro více položek dlouhodobého majetku</span><span class="sxs-lookup"><span data-stu-id="41b53-103">Change depreciation conventions for multiple fixed assets</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="41b53-104">Tato úloha aktualizuje způsob odpisu pro uvedenou skupinu dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="41b53-104">This task updates the depreciation convention for a specified fixed asset group.</span></span> <span data-ttu-id="41b53-105">Tento průvodce úlohou používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="41b53-105">This task guide uses the USMF demo company.</span></span>

1. <span data-ttu-id="41b53-106">Přejděte na Dlouhodobý majetek > Pravidelné úlohy > Hromadná aktualizace</span><span class="sxs-lookup"><span data-stu-id="41b53-106">Go to Fixed assets > Periodic tasks > Mass update</span></span>
2. <span data-ttu-id="41b53-107">V poli Kniha odpisů kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="41b53-107">In the Depreciation book field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="41b53-108">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="41b53-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="41b53-109">V poli Uvedeno do užívání - začátek zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="41b53-109">In the Placed in service start field, enter a date.</span></span>
5. <span data-ttu-id="41b53-110">V poli Uvedeno do užívání - konec zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="41b53-110">In the Placed in service end field, enter a date.</span></span>
    * <span data-ttu-id="41b53-111">Pouze majetek, který tvoří součást vybrané knihy odpisů a byl uveden do služby mezi těmito daty, se aktualizuje.</span><span class="sxs-lookup"><span data-stu-id="41b53-111">Only assets that are a part of the select depreciation book and that have been placed in service between these dates will be updated.</span></span>  
6. <span data-ttu-id="41b53-112">Vyberte volbu v poli Aktuální způsob odpisu.</span><span class="sxs-lookup"><span data-stu-id="41b53-112">In the Current depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="41b53-113">Bude aktualizován pouze majetek, který má aktuální způsob odpisu.</span><span class="sxs-lookup"><span data-stu-id="41b53-113">Only assets that have the current depreciation convention will be updated.</span></span>  
7. <span data-ttu-id="41b53-114">Vyberte volbu v poli Nový způsob odpisu.</span><span class="sxs-lookup"><span data-stu-id="41b53-114">In the New depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="41b53-115">Ověřte, zda že se sestava vytiskne v požadovaném cíli.</span><span class="sxs-lookup"><span data-stu-id="41b53-115">Verify the report will print to the desired destination.</span></span>  
8. <span data-ttu-id="41b53-116">Rozbalte oddíl Záznamy k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="41b53-116">Expand the Records to include section.</span></span>
9. <span data-ttu-id="41b53-117">Klepněte na tlačítko Filtr.</span><span class="sxs-lookup"><span data-stu-id="41b53-117">Click Filter.</span></span>
10. <span data-ttu-id="41b53-118">V seznamu vyberte Skupina dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="41b53-118">In the list, select the Fixed asset group.</span></span>
11. <span data-ttu-id="41b53-119">V poli Kritéria kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="41b53-119">In the Criteria field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="41b53-120">Vyberte požadovanou skupinu dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="41b53-120">Select the desired Fixed asset group.</span></span>
13. <span data-ttu-id="41b53-121">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="41b53-121">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="41b53-122">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="41b53-122">Click OK.</span></span>
15. <span data-ttu-id="41b53-123">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="41b53-123">Click OK.</span></span>
    *  <span data-ttu-id="41b53-124">Výsledky procesu jsou zobrazeny v sestavě Hromadná aktualizace.</span><span class="sxs-lookup"><span data-stu-id="41b53-124">Results of the process are shown on the Mass update report.</span></span>     


