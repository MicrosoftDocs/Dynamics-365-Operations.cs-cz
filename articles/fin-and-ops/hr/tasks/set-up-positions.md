---
title: Nastavit pozice
description: Pozice jsou důležitým prvkem nižší úrovně hierarchie organizace.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, HcmWorkforceWorkspace, HcmWorkerActivityChart, HcmAllWorkersListPart, HcmPosition, HcmPositionNewPosition, HcmJobLookup, HcmPositionReportsToDialog, HcmPositionLookup, FinancialDimensionDefaultTemplatesLookup, DimensionLookup
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4fd355fb6c3d2742e046a616585ca349c623341d
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/19/2019
ms.locfileid: "856823"
---
# <a name="set-up-positions"></a><span data-ttu-id="6439f-103">Nastavit pozice</span><span class="sxs-lookup"><span data-stu-id="6439f-103">Set up positions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6439f-104">Pozice jsou důležitým prvkem nižší úrovně hierarchie organizace.</span><span class="sxs-lookup"><span data-stu-id="6439f-104">Positions are an important element of the lower level of an organization hierarchy.</span></span> <span data-ttu-id="6439f-105">Pozice je individuální instance práce.</span><span class="sxs-lookup"><span data-stu-id="6439f-105">A position is an individual instance of a job.</span></span> <span data-ttu-id="6439f-106">Například pozice „Manažer prodeje (východ)“ je jednou z pozic, která je přidružena k úloze „Manažer prodeje“.</span><span class="sxs-lookup"><span data-stu-id="6439f-106">For example, the position, “Sales manager (East),” is one of the positions that is associated with the job, “Sales manager.”</span></span> <span data-ttu-id="6439f-107">Pozice se nachází v oddělení a může mít pouze jednoho pracovníka, který je k ní přidružen.</span><span class="sxs-lookup"><span data-stu-id="6439f-107">A position exists in a department and may have only one worker associated with it.</span></span> <span data-ttu-id="6439f-108">V rámci tohoto úkolu vás provedeme kroky potřebnými pro vytvoření pozice.</span><span class="sxs-lookup"><span data-stu-id="6439f-108">In this task we will walk through the steps required to create a position.</span></span> <span data-ttu-id="6439f-109">Tato úloha je určena pro odborníka na lidské zdroje.</span><span class="sxs-lookup"><span data-stu-id="6439f-109">This procedure is intended for Human Resources Specialists.</span></span>

1. <span data-ttu-id="6439f-110">Klikněte na Správa zaměstnanců.</span><span class="sxs-lookup"><span data-stu-id="6439f-110">Click Workforce management.</span></span>
2. <span data-ttu-id="6439f-111">Klikněte na Otevřít pozice.</span><span class="sxs-lookup"><span data-stu-id="6439f-111">Click Open positions.</span></span>
3. <span data-ttu-id="6439f-112">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="6439f-112">Click New to open the drop dialog.</span></span>
4. <span data-ttu-id="6439f-113">V poli Úloha zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="6439f-113">In the Job field, enter or select a value.</span></span>
    * <span data-ttu-id="6439f-114">Popis úlohy, název a zaměstnanecký faktor Ekvivalent plného úvazku se automaticky zkopírují z vybrané úlohy na pozici.</span><span class="sxs-lookup"><span data-stu-id="6439f-114">The Job description, title, and full-time equivalent employment factor are automatically copied from the selected job into the position.</span></span>  
5. <span data-ttu-id="6439f-115">Vyřešit změny úlohy.</span><span class="sxs-lookup"><span data-stu-id="6439f-115">ResolveChanges the Job.</span></span>
6. <span data-ttu-id="6439f-116">Klikněte na Vytvořit pozici.</span><span class="sxs-lookup"><span data-stu-id="6439f-116">Click Create position.</span></span>
7. <span data-ttu-id="6439f-117">V poli Oddělení zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="6439f-117">In the Department field, enter or select a value.</span></span>
8. <span data-ttu-id="6439f-118">V poli Typ pozice zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="6439f-118">In the Position type field, enter or select a value.</span></span>
9. <span data-ttu-id="6439f-119">V poli Oblast kompenzace zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="6439f-119">In the Compensation region field, enter or select a value.</span></span>
    * <span data-ttu-id="6439f-120">Pole Oblast kompenzace určuje pravidla způsobilosti kompenzace a rozpočty fixního zvýšení platné pro zaměstnance na této pozici.</span><span class="sxs-lookup"><span data-stu-id="6439f-120">The Compensation region field determines the compensation eligibility rules and fixed increase budgets that apply to an employee in that position.</span></span>  
10. <span data-ttu-id="6439f-121">Do pole K dispozici pro přiřazení zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="6439f-121">In the Available for assignment field, enter a date and time.</span></span>
11. <span data-ttu-id="6439f-122">Rozbalte oddíl Doba trvání pozice.</span><span class="sxs-lookup"><span data-stu-id="6439f-122">Expand the Position duration section.</span></span>
    * <span data-ttu-id="6439f-123">Ve výchozím nastavení se zadává trvání pozice na základě dříve zadaného data aktivace a vyřazení</span><span class="sxs-lookup"><span data-stu-id="6439f-123">Position duration is entered by default based on activation and retirement dates entered earlier</span></span>  
12. <span data-ttu-id="6439f-124">Rozbalte pole Sestavy pro umístění oddílu.</span><span class="sxs-lookup"><span data-stu-id="6439f-124">Expand the Reports to position section.</span></span>
    * <span data-ttu-id="6439f-125">Po přiřazení pracovníka k pozici, která je podřízena jiné pozici, můžete vytvořit vztah přímého vykazování mezi zaměstnanci, kteří jsou přiřazeni do dvou pozic.</span><span class="sxs-lookup"><span data-stu-id="6439f-125">When you assign a worker to a position that reports to another position, you create a direct reporting relationship between the workers who are assigned to the two positions.</span></span>  
13. <span data-ttu-id="6439f-126">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="6439f-126">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="6439f-127">V poli Nadřízená pozice zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="6439f-127">In the Reports to field, enter or select a value.</span></span>
15. <span data-ttu-id="6439f-128">Klepněte na volbu Nový.</span><span class="sxs-lookup"><span data-stu-id="6439f-128">Click Create.</span></span>
16. <span data-ttu-id="6439f-129">Rozbalte oddíl Přiřazení pracovníka.</span><span class="sxs-lookup"><span data-stu-id="6439f-129">Expand the Worker assignment section.</span></span>
17. <span data-ttu-id="6439f-130">Rozbalte nebo sbalte oddíl Vztahy.</span><span class="sxs-lookup"><span data-stu-id="6439f-130">Expand the Relationships section.</span></span>
    * <span data-ttu-id="6439f-131">Pokud vaše společnost používá hierarchii matice nebo jinou vlastní hierarchii, můžete nastavit typy hierarchií pozic a přidat vztahy podřízenosti k pozicím pro každý nastavený typ hierarchie.</span><span class="sxs-lookup"><span data-stu-id="6439f-131">If your organization uses a matrix hierarchy or another custom hierarchy, you can set up position hierarchy types and then add reporting relationships to positions for each hierarchy type that you set up.</span></span>  
18. <span data-ttu-id="6439f-132">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="6439f-132">Click Add.</span></span>
19. <span data-ttu-id="6439f-133">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="6439f-133">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="6439f-134">V poli Název hierarchie zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="6439f-134">In the Hierarchy name field, enter or select a value.</span></span>
21. <span data-ttu-id="6439f-135">V poli Nadřízená pozice zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="6439f-135">In the Reports to position field, enter or select a value.</span></span>
22. <span data-ttu-id="6439f-136">Rozbalte sekci Mzdy.</span><span class="sxs-lookup"><span data-stu-id="6439f-136">Expand the Payroll section.</span></span>
23. <span data-ttu-id="6439f-137">V poli Platební cyklus zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="6439f-137">In the Pay cycle field, enter or select a value.</span></span>
24. <span data-ttu-id="6439f-138">V poli Zaplatil(a) zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="6439f-138">In the Paid by field, enter or select a value.</span></span>
25. <span data-ttu-id="6439f-139">Do pole Roční normální hodiny zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="6439f-139">In the Annual regular hours field, enter a number.</span></span>
    * <span data-ttu-id="6439f-140">Toto je počet pravidelně placených hodin, které jsou od pracovníka na této pozici každý rok očekávány.</span><span class="sxs-lookup"><span data-stu-id="6439f-140">This is the number of regularly paid hours that the worker in this position is expected to work each year.</span></span>  
26. <span data-ttu-id="6439f-141">Rozbalte část Odbor.</span><span class="sxs-lookup"><span data-stu-id="6439f-141">Expand the Labor union section.</span></span>
27. <span data-ttu-id="6439f-142">Sbalte část Odbor.</span><span class="sxs-lookup"><span data-stu-id="6439f-142">Collapse the Labor union section.</span></span>
28. <span data-ttu-id="6439f-143">Rozbalte část Finanční dimenze.</span><span class="sxs-lookup"><span data-stu-id="6439f-143">Expand the Financial dimensions section.</span></span>
29. <span data-ttu-id="6439f-144">V poli Šablona distribuce zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="6439f-144">In the Distribution template field, enter or select a value.</span></span>
30. <span data-ttu-id="6439f-145">V poli Oddělení zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="6439f-145">In the Department field, enter or select a value.</span></span>
31. <span data-ttu-id="6439f-146">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="6439f-146">Click Save.</span></span>

