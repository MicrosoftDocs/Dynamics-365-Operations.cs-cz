--- 
title: "Proces získání nároku na zaměstnaneckou výhodu"
description: "Tento postup upravuje proces nároku na zaměstnanecké výhody."
author: kherr75
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 7c05c7613ee0d37d6bdfcb42f4e9611629d215bd
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---
# <a name="benefit-eligibility-process"></a><span data-ttu-id="cee62-103">Proces získání nároku na zaměstnaneckou výhodu</span><span class="sxs-lookup"><span data-stu-id="cee62-103">Benefit eligibility process</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cee62-104">Tento postup upravuje proces nároku na zaměstnanecké výhody.</span><span class="sxs-lookup"><span data-stu-id="cee62-104">This procedure hows the benefit eligibility process works.</span></span> <span data-ttu-id="cee62-105">Výsledky se zobrazí po dokončení procesu.</span><span class="sxs-lookup"><span data-stu-id="cee62-105">When the process is complete you can view the results.</span></span> <span data-ttu-id="cee62-106">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="cee62-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="cee62-107">Přejděte k nabídce Lidské zdroje > Výhody > Výhody.</span><span class="sxs-lookup"><span data-stu-id="cee62-107">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="cee62-108">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="cee62-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="cee62-109">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="cee62-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="cee62-110">Klikněte na možnost Upravit.</span><span class="sxs-lookup"><span data-stu-id="cee62-110">Click Edit.</span></span>
5. <span data-ttu-id="cee62-111">V poli Nárok vyberte možnost „Podle pravidel“.</span><span class="sxs-lookup"><span data-stu-id="cee62-111">In the Eligibility field, select 'Rule based'.</span></span>
6. <span data-ttu-id="cee62-112">V poli Typ pravidla vyberte pravidlo zásad zaměstnanecké výhody, které má být použito na zaměstnaneckou výhodu.</span><span class="sxs-lookup"><span data-stu-id="cee62-112">In the Rule type field, select the benefit policy rule you would like applied to the benefit.</span></span>
7. <span data-ttu-id="cee62-113">V podokně akcí klikněte na možnost Zaměstnanecká výhoda.</span><span class="sxs-lookup"><span data-stu-id="cee62-113">On the Action Pane, click Benefit.</span></span>
8. <span data-ttu-id="cee62-114">Kliknutím na možnost Vytvořit událost nároku otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="cee62-114">Click Create eligibility event to open the drop dialog.</span></span>
9. <span data-ttu-id="cee62-115">Zadejte hodnotu do pole Událost.</span><span class="sxs-lookup"><span data-stu-id="cee62-115">In the Event field, type a value.</span></span>
10. <span data-ttu-id="cee62-116">Zadejte hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="cee62-116">In the Description field, type a value.</span></span>
11. <span data-ttu-id="cee62-117">Vyberte v poli typ události možnost „Otevřít přihlášení“.</span><span class="sxs-lookup"><span data-stu-id="cee62-117">In the Event type field, select 'Open enrollment'.</span></span>
12. <span data-ttu-id="cee62-118">Do pole Počáteční datum pokrytí zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="cee62-118">In the Coverage start date field, enter a date and time.</span></span>
13. <span data-ttu-id="cee62-119">Zadejte zadejte datum a čas do pole Počáteční datum doby přihlášení.</span><span class="sxs-lookup"><span data-stu-id="cee62-119">In the Enrollment period start date field, enter a date and time.</span></span>
14. <span data-ttu-id="cee62-120">Zadejte číslo do pole Počet dnů pro přihlášení.</span><span class="sxs-lookup"><span data-stu-id="cee62-120">In the Days to enroll field, enter a number.</span></span>
15. <span data-ttu-id="cee62-121">Klikněte na Vytvořit událost.</span><span class="sxs-lookup"><span data-stu-id="cee62-121">Click Create event.</span></span>
16. <span data-ttu-id="cee62-122">Klepněte na tlačítko Přidat na pevné záložce Zaměstnanci</span><span class="sxs-lookup"><span data-stu-id="cee62-122">Click Add in the Workers FastTab.</span></span>
17. <span data-ttu-id="cee62-123">Vyberte v poli Zobrazit podle typu možnost Zaměstnanci.</span><span class="sxs-lookup"><span data-stu-id="cee62-123">In the Show by type field, select 'Employees'.</span></span>
18. <span data-ttu-id="cee62-124">V poli Zobrazit podle právnické osoby zaškrtněte možnost „Aktuální právnická osoba“.</span><span class="sxs-lookup"><span data-stu-id="cee62-124">In the Show by legal entity field, select 'Current legal entity'.</span></span>
19. <span data-ttu-id="cee62-125">V seznamu označte všechny řádky nebo jejich označení zrušte.</span><span class="sxs-lookup"><span data-stu-id="cee62-125">In the list, mark or unmark all rows.</span></span>
20. <span data-ttu-id="cee62-126">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="cee62-126">Click OK.</span></span>
21. <span data-ttu-id="cee62-127">Klikněte na možnost Zpracovat.</span><span class="sxs-lookup"><span data-stu-id="cee62-127">Click Process.</span></span>
22. <span data-ttu-id="cee62-128">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="cee62-128">Click OK.</span></span>
23. <span data-ttu-id="cee62-129">Aktualizujte stránku.</span><span class="sxs-lookup"><span data-stu-id="cee62-129">Refresh the page.</span></span>
24. <span data-ttu-id="cee62-130">Klikněte na možnost Zobrazit výsledky.</span><span class="sxs-lookup"><span data-stu-id="cee62-130">Click Show results.</span></span>
25. <span data-ttu-id="cee62-131">Otevřete filtr sloupce Stav.</span><span class="sxs-lookup"><span data-stu-id="cee62-131">Open Status column filter.</span></span>
26. <span data-ttu-id="cee62-132">Seřadit od A do Z</span><span class="sxs-lookup"><span data-stu-id="cee62-132">Sort A to Z</span></span>


