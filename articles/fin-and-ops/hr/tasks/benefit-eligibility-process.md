--- 
title: "Proces získání nároku na zaměstnaneckou výhodu"
description: "Tento postup ukazuje, jak funguje proces nároku na zaměstnanecké výhody."
author: kherr75
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 965826f5fddc2f53f33157434929eb265979376e
ms.openlocfilehash: 859bf2ef369173ce4b6bc380820ea157ae86e13a
ms.contentlocale: cs-cz
ms.lasthandoff: 09/17/2018

---
# <a name="benefit-eligibility-process"></a><span data-ttu-id="704ab-103">Proces získání nároku na zaměstnaneckou výhodu</span><span class="sxs-lookup"><span data-stu-id="704ab-103">Benefit eligibility process</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="704ab-104">Tento postup ukazuje, jak funguje proces nároku na zaměstnanecké výhody.</span><span class="sxs-lookup"><span data-stu-id="704ab-104">This procedure shows how the benefit eligibility process works.</span></span> <span data-ttu-id="704ab-105">Výsledky se zobrazí po dokončení procesu.</span><span class="sxs-lookup"><span data-stu-id="704ab-105">When the process is complete you can view the results.</span></span> <span data-ttu-id="704ab-106">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="704ab-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="704ab-107">Přejděte k nabídce Lidské zdroje > Výhody > Výhody.</span><span class="sxs-lookup"><span data-stu-id="704ab-107">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="704ab-108">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="704ab-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="704ab-109">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="704ab-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="704ab-110">Klikněte na možnost Upravit.</span><span class="sxs-lookup"><span data-stu-id="704ab-110">Click Edit.</span></span>
5. <span data-ttu-id="704ab-111">V poli Nárok vyberte možnost „Podle pravidel“.</span><span class="sxs-lookup"><span data-stu-id="704ab-111">In the Eligibility field, select 'Rule based'.</span></span>
6. <span data-ttu-id="704ab-112">V poli Typ pravidla vyberte pravidlo zásad zaměstnanecké výhody, které má být použito na zaměstnaneckou výhodu.</span><span class="sxs-lookup"><span data-stu-id="704ab-112">In the Rule type field, select the benefit policy rule you would like applied to the benefit.</span></span>
7. <span data-ttu-id="704ab-113">V podokně akcí klikněte na možnost Zaměstnanecká výhoda.</span><span class="sxs-lookup"><span data-stu-id="704ab-113">On the Action Pane, click Benefit.</span></span>
8. <span data-ttu-id="704ab-114">Kliknutím na možnost Vytvořit událost nároku otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="704ab-114">Click Create eligibility event to open the drop dialog.</span></span>
9. <span data-ttu-id="704ab-115">Zadejte hodnotu do pole Událost.</span><span class="sxs-lookup"><span data-stu-id="704ab-115">In the Event field, type a value.</span></span>
10. <span data-ttu-id="704ab-116">Zadejte hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="704ab-116">In the Description field, type a value.</span></span>
11. <span data-ttu-id="704ab-117">Vyberte v poli typ události možnost „Otevřít přihlášení“.</span><span class="sxs-lookup"><span data-stu-id="704ab-117">In the Event type field, select 'Open enrollment'.</span></span>
12. <span data-ttu-id="704ab-118">Do pole Počáteční datum pokrytí zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="704ab-118">In the Coverage start date field, enter a date and time.</span></span>
13. <span data-ttu-id="704ab-119">Zadejte zadejte datum a čas do pole Počáteční datum doby přihlášení.</span><span class="sxs-lookup"><span data-stu-id="704ab-119">In the Enrollment period start date field, enter a date and time.</span></span>
14. <span data-ttu-id="704ab-120">Zadejte číslo do pole Počet dnů pro přihlášení.</span><span class="sxs-lookup"><span data-stu-id="704ab-120">In the Days to enroll field, enter a number.</span></span>
15. <span data-ttu-id="704ab-121">Klikněte na Vytvořit událost.</span><span class="sxs-lookup"><span data-stu-id="704ab-121">Click Create event.</span></span>
16. <span data-ttu-id="704ab-122">Klepněte na tlačítko Přidat na pevné záložce Zaměstnanci</span><span class="sxs-lookup"><span data-stu-id="704ab-122">Click Add in the Workers FastTab.</span></span>
17. <span data-ttu-id="704ab-123">Vyberte v poli Zobrazit podle typu možnost Zaměstnanci.</span><span class="sxs-lookup"><span data-stu-id="704ab-123">In the Show by type field, select 'Employees'.</span></span>
18. <span data-ttu-id="704ab-124">V poli Zobrazit podle právnické osoby zaškrtněte možnost „Aktuální právnická osoba“.</span><span class="sxs-lookup"><span data-stu-id="704ab-124">In the Show by legal entity field, select 'Current legal entity'.</span></span>
19. <span data-ttu-id="704ab-125">V seznamu označte všechny řádky nebo jejich označení zrušte.</span><span class="sxs-lookup"><span data-stu-id="704ab-125">In the list, mark or unmark all rows.</span></span>
20. <span data-ttu-id="704ab-126">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="704ab-126">Click OK.</span></span>
21. <span data-ttu-id="704ab-127">Klikněte na možnost Zpracovat.</span><span class="sxs-lookup"><span data-stu-id="704ab-127">Click Process.</span></span>
22. <span data-ttu-id="704ab-128">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="704ab-128">Click OK.</span></span>
23. <span data-ttu-id="704ab-129">Aktualizujte stránku.</span><span class="sxs-lookup"><span data-stu-id="704ab-129">Refresh the page.</span></span>
24. <span data-ttu-id="704ab-130">Klikněte na možnost Zobrazit výsledky.</span><span class="sxs-lookup"><span data-stu-id="704ab-130">Click Show results.</span></span>
25. <span data-ttu-id="704ab-131">Otevřete filtr sloupce Stav.</span><span class="sxs-lookup"><span data-stu-id="704ab-131">Open Status column filter.</span></span>
26. <span data-ttu-id="704ab-132">Seřadit od A do Z</span><span class="sxs-lookup"><span data-stu-id="704ab-132">Sort A to Z</span></span>


