---
title: Vytvoření a otevření požadavku na pozici
description: Náborové projekty umožňují spravovat proces náboru.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRMRecruitingTable, HcmWorkerLookUp, HcmJobLookup, HRMRecruitingMedia, HRMRecruitingJobAd
audience: Application User
ms.reviewer: anbichse
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d23f180c1afcfa6d24c0b44f69fba9b40c114e1b
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564644"
---
# <a name="develop-and-open-job-requisition"></a><span data-ttu-id="0a183-103">Vytvoření a otevření požadavku na pozici</span><span class="sxs-lookup"><span data-stu-id="0a183-103">Develop and open job requisition</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0a183-104">Náborové projekty umožňují spravovat proces náboru.</span><span class="sxs-lookup"><span data-stu-id="0a183-104">Recruitment projects help manage the recruiting process.</span></span> <span data-ttu-id="0a183-105">K jednotlivým náborovým projektům lze nastavit informace, jako například práci, na kterou probíhá nábor, název náborového pracovníka, stav projektu a oddělení, ve kterém se úloha bude nacházet.</span><span class="sxs-lookup"><span data-stu-id="0a183-105">For each recruitment project, you can set up information, such as the job that recruiting is for, the name of the recruiter, the status of the project and the department that the job will be located in.</span></span> <span data-ttu-id="0a183-106">Po vytvoření náborového projektu můžete napsat inzerát na pozici projektu, publikovat inzerát na samoobslužných stránkách zaměstnanců, přiřadit přihlášky k zaměstnání pro projekt a sledovat aktivity pro daný projekt.</span><span class="sxs-lookup"><span data-stu-id="0a183-106">After creating a recruitment project, you can write a job advertisement for the project, publish the ad on Employee self-service pages, associate applications for employment with the project, and track activities for that project.</span></span> <span data-ttu-id="0a183-107">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="0a183-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="0a183-108">Pokud chcete zahájit postup, přejděte na Lidské zdroje > Nábor > Náborové projekty >Náborové projekty</span><span class="sxs-lookup"><span data-stu-id="0a183-108">To begin the procedure, go to Human resources > Recruitment > Recruitment projects > Recruitment projects</span></span>

1. <span data-ttu-id="0a183-109">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="0a183-109">Click New.</span></span>
2. <span data-ttu-id="0a183-110">Zadejte hodnotu do pole Náborový projekt.</span><span class="sxs-lookup"><span data-stu-id="0a183-110">In the Recruitment project field, type a value.</span></span>
3. <span data-ttu-id="0a183-111">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="0a183-111">In the Description field, type a value.</span></span>
4. <span data-ttu-id="0a183-112">V poli Náborový pracovník kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="0a183-112">In the Recruiter field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="0a183-113">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="0a183-113">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="0a183-114">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="0a183-114">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="0a183-115">Klepněte na tlačítko Vybrat.</span><span class="sxs-lookup"><span data-stu-id="0a183-115">Click Select.</span></span>
8. <span data-ttu-id="0a183-116">V poli Oddělení kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="0a183-116">In the Department field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="0a183-117">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="0a183-117">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="0a183-118">V poli Úloha kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="0a183-118">In the Job field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="0a183-119">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="0a183-119">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="0a183-120">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="0a183-120">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="0a183-121">Do pole Počet volných míst zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="0a183-121">In the Number of openings field, enter a number.</span></span>
14. <span data-ttu-id="0a183-122">V poli Náborový manažer kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="0a183-122">In the Hiring manager field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="0a183-123">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="0a183-123">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="0a183-124">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="0a183-124">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="0a183-125">Klepněte na tlačítko Vybrat.</span><span class="sxs-lookup"><span data-stu-id="0a183-125">Click Select.</span></span>
18. <span data-ttu-id="0a183-126">Zadejte datum do pole Konečný termín přihlášky.</span><span class="sxs-lookup"><span data-stu-id="0a183-126">In the Application deadline field, enter a date.</span></span>
19. <span data-ttu-id="0a183-127">Klepněte na Média.</span><span class="sxs-lookup"><span data-stu-id="0a183-127">Click Media.</span></span>
    * <span data-ttu-id="0a183-128">Náborové projekty zahrnují možnost zadat sdělovací prostředky, které chcete použít pro inzerování otevřených pozic.</span><span class="sxs-lookup"><span data-stu-id="0a183-128">Recruitment projects include the option to specify media outlets to use to advertise open positions.</span></span>  
20. <span data-ttu-id="0a183-129">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="0a183-129">Click New.</span></span>
21. <span data-ttu-id="0a183-130">V poli Média kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="0a183-130">In the Media field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="0a183-131">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="0a183-131">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="0a183-132">Zadejte datum do pole Počáteční datum.</span><span class="sxs-lookup"><span data-stu-id="0a183-132">In the Start date field, enter a date.</span></span>
24. <span data-ttu-id="0a183-133">Zadejte datum do pole Koncové datum.</span><span class="sxs-lookup"><span data-stu-id="0a183-133">In the End date field, enter a date.</span></span>
25. <span data-ttu-id="0a183-134">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="0a183-134">Click Save.</span></span>
26. <span data-ttu-id="0a183-135">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="0a183-135">Close the page.</span></span>
27. <span data-ttu-id="0a183-136">Klikněte na Pracovní inzeráty.</span><span class="sxs-lookup"><span data-stu-id="0a183-136">Click Job ads.</span></span>
28. <span data-ttu-id="0a183-137">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="0a183-137">Click Save.</span></span>
29. <span data-ttu-id="0a183-138">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="0a183-138">Close the page.</span></span>
30. <span data-ttu-id="0a183-139">Označte nebo odznačte pole Zobrazit v samoobsluze pro zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="0a183-139">Check or uncheck the Display on employee self service checkbox.</span></span>
    * <span data-ttu-id="0a183-140">Označte pole Zobrazit v samoobsluze pro zaměstnance pro zviditelnění projektu náboru pro zaměstnance na samoobslužných stránkách zaměstnanců.</span><span class="sxs-lookup"><span data-stu-id="0a183-140">Select the Display on employee self service check box to make the recruitment project visible to employees on their Employee self-service pages.</span></span>  
31. <span data-ttu-id="0a183-141">Klikněte na Stav náborového projektu.</span><span class="sxs-lookup"><span data-stu-id="0a183-141">Click Recruitment project status.</span></span>
32. <span data-ttu-id="0a183-142">Klikněte na položku Spustit.</span><span class="sxs-lookup"><span data-stu-id="0a183-142">Click Start.</span></span>
    * <span data-ttu-id="0a183-143">Stav Zahájeno znamená, že je projekt připraven přijímat žádosti.</span><span class="sxs-lookup"><span data-stu-id="0a183-143">The Started status means that the project is ready to receive applications.</span></span>  
33. <span data-ttu-id="0a183-144">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="0a183-144">Click OK.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]