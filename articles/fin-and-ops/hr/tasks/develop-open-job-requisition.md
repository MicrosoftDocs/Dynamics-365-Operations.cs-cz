---
title: Vytvoření a otevření požadavku na pozici
description: Náborové projekty umožňují spravovat proces náboru.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMRecruitingTable, HcmWorkerLookUp, HcmJobLookup, HRMRecruitingMedia, HRMRecruitingJobAd
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 556f99d34521cce70efb64c5fbababd815e8429d
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2019
ms.locfileid: "1507699"
---
# <a name="develop-and-open-job-requisition"></a><span data-ttu-id="e6fe4-103">Vytvoření a otevření požadavku na pozici</span><span class="sxs-lookup"><span data-stu-id="e6fe4-103">Develop and open job requisition</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e6fe4-104">Náborové projekty umožňují spravovat proces náboru.</span><span class="sxs-lookup"><span data-stu-id="e6fe4-104">Recruitment projects help manage the recruiting process.</span></span> <span data-ttu-id="e6fe4-105">K jednotlivým náborovým projektům lze nastavit informace, jako například práci, na kterou probíhá nábor, název náborového pracovníka, stav projektu a oddělení, ve kterém se úloha bude nacházet.</span><span class="sxs-lookup"><span data-stu-id="e6fe4-105">For each recruitment project, you can set up information, such as the job that recruiting is for, the name of the recruiter, the status of the project and the department that the job will be located in.</span></span> <span data-ttu-id="e6fe4-106">Po vytvoření náborového projektu můžete napsat inzerát na pozici projektu, publikovat inzerát na samoobslužných stránkách zaměstnanců, přiřadit přihlášky k zaměstnání pro projekt a sledovat aktivity pro daný projekt.</span><span class="sxs-lookup"><span data-stu-id="e6fe4-106">After creating a recruitment project, you can write a job advertisement for the project, publish the ad on Employee self-service pages, associate applications for employment with the project, and track activities for that project.</span></span> <span data-ttu-id="e6fe4-107">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="e6fe4-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="e6fe4-108">Pokud chcete zahájit postup, přejděte na Lidské zdroje > Nábor > Náborové projekty >Náborové projekty</span><span class="sxs-lookup"><span data-stu-id="e6fe4-108">To begin the procedure, go to Human resources > Recruitment > Recruitment projects > Recruitment projects</span></span>

1. <span data-ttu-id="e6fe4-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="e6fe4-109">Click New.</span></span>
2. <span data-ttu-id="e6fe4-110">Zadejte hodnotu do pole Náborový projekt.</span><span class="sxs-lookup"><span data-stu-id="e6fe4-110">In the Recruitment project field, type a value.</span></span>
3. <span data-ttu-id="e6fe4-111">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="e6fe4-111">In the Description field, type a value.</span></span>
4. <span data-ttu-id="e6fe4-112">V poli Náborový pracovník kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="e6fe4-112">In the Recruiter field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="e6fe4-113">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="e6fe4-113">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="e6fe4-114">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="e6fe4-114">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="e6fe4-115">Klepněte na tlačítko Vybrat.</span><span class="sxs-lookup"><span data-stu-id="e6fe4-115">Click Select.</span></span>
8. <span data-ttu-id="e6fe4-116">V poli Oddělení kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="e6fe4-116">In the Department field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="e6fe4-117">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="e6fe4-117">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="e6fe4-118">V poli Úloha kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="e6fe4-118">In the Job field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="e6fe4-119">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="e6fe4-119">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="e6fe4-120">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="e6fe4-120">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="e6fe4-121">Do pole Počet volných míst zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="e6fe4-121">In the Number of openings field, enter a number.</span></span>
14. <span data-ttu-id="e6fe4-122">V poli Náborový manažer kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="e6fe4-122">In the Hiring manager field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="e6fe4-123">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="e6fe4-123">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="e6fe4-124">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="e6fe4-124">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="e6fe4-125">Klepněte na tlačítko Vybrat.</span><span class="sxs-lookup"><span data-stu-id="e6fe4-125">Click Select.</span></span>
18. <span data-ttu-id="e6fe4-126">Zadejte datum do pole Konečný termín přihlášky.</span><span class="sxs-lookup"><span data-stu-id="e6fe4-126">In the Application deadline field, enter a date.</span></span>
19. <span data-ttu-id="e6fe4-127">Klepněte na Média.</span><span class="sxs-lookup"><span data-stu-id="e6fe4-127">Click Media.</span></span>
    * <span data-ttu-id="e6fe4-128">Náborové projekty zahrnují možnost zadat sdělovací prostředky, které chcete použít pro inzerování otevřených pozic.</span><span class="sxs-lookup"><span data-stu-id="e6fe4-128">Recruitment projects include the option to specify media outlets to use to advertise open positions.</span></span>  
20. <span data-ttu-id="e6fe4-129">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="e6fe4-129">Click New.</span></span>
21. <span data-ttu-id="e6fe4-130">V poli Média kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="e6fe4-130">In the Media field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="e6fe4-131">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="e6fe4-131">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="e6fe4-132">Zadejte datum do pole Počáteční datum.</span><span class="sxs-lookup"><span data-stu-id="e6fe4-132">In the Start date field, enter a date.</span></span>
24. <span data-ttu-id="e6fe4-133">Zadejte datum do pole Koncové datum.</span><span class="sxs-lookup"><span data-stu-id="e6fe4-133">In the End date field, enter a date.</span></span>
25. <span data-ttu-id="e6fe4-134">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="e6fe4-134">Click Save.</span></span>
26. <span data-ttu-id="e6fe4-135">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="e6fe4-135">Close the page.</span></span>
27. <span data-ttu-id="e6fe4-136">Klikněte na Pracovní inzeráty.</span><span class="sxs-lookup"><span data-stu-id="e6fe4-136">Click Job ads.</span></span>
28. <span data-ttu-id="e6fe4-137">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="e6fe4-137">Click Save.</span></span>
29. <span data-ttu-id="e6fe4-138">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="e6fe4-138">Close the page.</span></span>
30. <span data-ttu-id="e6fe4-139">Označte nebo odznačte pole Zobrazit v samoobsluze pro zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="e6fe4-139">Check or uncheck the Display on employee self service checkbox.</span></span>
    * <span data-ttu-id="e6fe4-140">Označte pole Zobrazit v samoobsluze pro zaměstnance pro zviditelnění projektu náboru pro zaměstnance na samoobslužných stránkách zaměstnanců.</span><span class="sxs-lookup"><span data-stu-id="e6fe4-140">Select the Display on employee self service check box to make the recruitment project visible to employees on their Employee self-service pages.</span></span>  
31. <span data-ttu-id="e6fe4-141">Klikněte na Stav náborového projektu.</span><span class="sxs-lookup"><span data-stu-id="e6fe4-141">Click Recruitment project status.</span></span>
32. <span data-ttu-id="e6fe4-142">Klikněte na položku Spustit.</span><span class="sxs-lookup"><span data-stu-id="e6fe4-142">Click Start.</span></span>
    * <span data-ttu-id="e6fe4-143">Stav Zahájeno znamená, že je projekt připraven přijímat žádosti.</span><span class="sxs-lookup"><span data-stu-id="e6fe4-143">The Started status means that the project is ready to receive applications.</span></span>  
33. <span data-ttu-id="e6fe4-144">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="e6fe4-144">Click OK.</span></span>

