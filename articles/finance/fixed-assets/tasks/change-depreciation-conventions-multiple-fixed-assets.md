---
title: Změna způsobu odpisu pro více položek dlouhodobého majetku
description: Tato úloha aktualizuje způsob odpisu pro uvedenou skupinu dlouhodobého majetku.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysQueryForm, SrsReportViewerForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 39930134782b40de05a92a6ad51c4f628f304a78
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441013"
---
# <a name="change-depreciation-conventions-for-multiple-fixed-assets"></a><span data-ttu-id="9acc7-103">Změna způsobu odpisu pro více položek dlouhodobého majetku</span><span class="sxs-lookup"><span data-stu-id="9acc7-103">Change depreciation conventions for multiple fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9acc7-104">Tato úloha aktualizuje způsob odpisu pro uvedenou skupinu dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="9acc7-104">This task updates the depreciation convention for a specified fixed asset group.</span></span> <span data-ttu-id="9acc7-105">Tento průvodce úlohou používá ukázkovou společnost USMF.</span><span class="sxs-lookup"><span data-stu-id="9acc7-105">This task guide uses the USMF demo company.</span></span>

1. <span data-ttu-id="9acc7-106">Přejděte na Dlouhodobý majetek > Pravidelné úlohy > Hromadná aktualizace</span><span class="sxs-lookup"><span data-stu-id="9acc7-106">Go to Fixed assets > Periodic tasks > Mass update</span></span>
2. <span data-ttu-id="9acc7-107">V poli Kniha odpisů kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="9acc7-107">In the Depreciation book field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="9acc7-108">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="9acc7-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="9acc7-109">V poli Uvedeno do užívání - začátek zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="9acc7-109">In the Placed in service start field, enter a date.</span></span>
5. <span data-ttu-id="9acc7-110">V poli Uvedeno do užívání - konec zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="9acc7-110">In the Placed in service end field, enter a date.</span></span>
    * <span data-ttu-id="9acc7-111">Pouze majetek, který tvoří součást vybrané knihy odpisů a byl uveden do služby mezi těmito daty, se aktualizuje.</span><span class="sxs-lookup"><span data-stu-id="9acc7-111">Only assets that are a part of the select depreciation book and that have been placed in service between these dates will be updated.</span></span>  
6. <span data-ttu-id="9acc7-112">Vyberte volbu v poli Aktuální způsob odpisu.</span><span class="sxs-lookup"><span data-stu-id="9acc7-112">In the Current depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="9acc7-113">Bude aktualizován pouze majetek, který má aktuální způsob odpisu.</span><span class="sxs-lookup"><span data-stu-id="9acc7-113">Only assets that have the current depreciation convention will be updated.</span></span>  
7. <span data-ttu-id="9acc7-114">Vyberte volbu v poli Nový způsob odpisu.</span><span class="sxs-lookup"><span data-stu-id="9acc7-114">In the New depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="9acc7-115">Ověřte, zda že se sestava vytiskne v požadovaném cíli.</span><span class="sxs-lookup"><span data-stu-id="9acc7-115">Verify the report will print to the desired destination.</span></span>  
8. <span data-ttu-id="9acc7-116">Rozbalte oddíl Záznamy k zahrnutí.</span><span class="sxs-lookup"><span data-stu-id="9acc7-116">Expand the Records to include section.</span></span>
9. <span data-ttu-id="9acc7-117">Klepněte na tlačítko Filtr.</span><span class="sxs-lookup"><span data-stu-id="9acc7-117">Click Filter.</span></span>
10. <span data-ttu-id="9acc7-118">V seznamu vyberte Skupina dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="9acc7-118">In the list, select the Fixed asset group.</span></span>
11. <span data-ttu-id="9acc7-119">V poli Kritéria kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="9acc7-119">In the Criteria field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="9acc7-120">Vyberte požadovanou skupinu dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="9acc7-120">Select the desired Fixed asset group.</span></span>
13. <span data-ttu-id="9acc7-121">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="9acc7-121">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="9acc7-122">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="9acc7-122">Click OK.</span></span>
15. <span data-ttu-id="9acc7-123">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="9acc7-123">Click OK.</span></span>
    *  <span data-ttu-id="9acc7-124">Výsledky procesu jsou zobrazeny v sestavě Hromadná aktualizace.</span><span class="sxs-lookup"><span data-stu-id="9acc7-124">Results of the process are shown on the Mass update report.</span></span>     

