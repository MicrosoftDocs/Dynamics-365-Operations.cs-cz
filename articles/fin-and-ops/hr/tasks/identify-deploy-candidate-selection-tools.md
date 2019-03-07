---
title: Identifikování a nasazení nástrojů pro výběr kandidáta
description: Najít kvalifikovaný fond uchazečů pro vyplnění volných pracovních míst může být obtížné, zejména v případě, že pozice vyžaduje jedinečnou sadu dovedností.
author: kherr75
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmSkillMapping, HcmJobLookup, HcmSkillMappingLine, HcmPersonCertificate, CCHTMLPrintPreview
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: df7956cfdc3c470b5e652b62e659060120cdd770
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "332718"
---
# <a name="identify-and-deploy-candidate-selection-tools"></a><span data-ttu-id="926e5-103">Identifikování a nasazení nástrojů pro výběr kandidáta</span><span class="sxs-lookup"><span data-stu-id="926e5-103">Identify and deploy candidate selection tools</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="926e5-104">Najít kvalifikovaný fond uchazečů pro vyplnění volných pracovních míst může být obtížné, zejména v případě, že pozice vyžaduje jedinečnou sadu dovedností.</span><span class="sxs-lookup"><span data-stu-id="926e5-104">Finding a qualified pool of candidates to fill vacancies can be difficult, especially when a position requires a unique set of skills.</span></span>  <span data-ttu-id="926e5-105">Avšak uchazeči s dovednostmi, které potřebujete, mohou již být zaměstnáni ve vaší organizaci.</span><span class="sxs-lookup"><span data-stu-id="926e5-105">However, candidates with the skills you need might already be employed in your organization.</span></span> <span data-ttu-id="926e5-106">Můžete u stávajících zaměstnanců nebo nových uchazečů vyhledávat konkrétní sady dovedností.</span><span class="sxs-lookup"><span data-stu-id="926e5-106">You can search for a specific skill set among existing employees, or new applicants.</span></span> <span data-ttu-id="926e5-107">To umožňuje náborovým pracovníkům rychle shromažďovat a sledovat uchazeče, kteří se uchází o volnou pozici nyní nebo v minulosti, nebo najít potenciální uchazeče ze stávajícího fondu zaměstnanců.</span><span class="sxs-lookup"><span data-stu-id="926e5-107">This allows a recruiter to quickly gather and screen applicants who have applied for open position now or in the past, or to find potential candidates from their existing pool of employees.</span></span> <span data-ttu-id="926e5-108">Tento záznam úloh vám usnadní zjistit, jak funkce mapování dovedností může pomoci najít pravou osobu pro volnou pozici.</span><span class="sxs-lookup"><span data-stu-id="926e5-108">Use this task recording to learn how the skill mapping functionality can help you find the right person for an open position.</span></span> <span data-ttu-id="926e5-109">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="926e5-109">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="926e5-110">Přejděte na Lidské zdroje > Kompetence > Analýza dovedností > Profily mapování dovedností.</span><span class="sxs-lookup"><span data-stu-id="926e5-110">Go to Human resources > Competencies > Skill analysis > Skill mapping profiles.</span></span>
2. <span data-ttu-id="926e5-111">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="926e5-111">Click New.</span></span>
3. <span data-ttu-id="926e5-112">V poli Mapování dovedností zadejte název vašeho mapování dovedností.</span><span class="sxs-lookup"><span data-stu-id="926e5-112">In the Skill mapping field, enter a name for your skill mapping.</span></span>  <span data-ttu-id="926e5-113">Příklad: Účetní.</span><span class="sxs-lookup"><span data-stu-id="926e5-113">Example: Accountant.</span></span>
4. <span data-ttu-id="926e5-114">Do pole Popis zadejte popis mapování dovedností.</span><span class="sxs-lookup"><span data-stu-id="926e5-114">In the Description field, enter a description of the skill mapping..</span></span>
5. <span data-ttu-id="926e5-115">Do pole Datum zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="926e5-115">In the Date field, enter a date.</span></span>
6. <span data-ttu-id="926e5-116">Klikněte na Načíst profil.</span><span class="sxs-lookup"><span data-stu-id="926e5-116">Click Retrieve profile.</span></span>
    * <span data-ttu-id="926e5-117">Pomocí možnosti Načíst profil vložte data Certifikát, vzdělání a dovednosti vybrané osoby, práce nebo kurzu jako základ pro vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="926e5-117">Use Retrieve profile to pull in the Certificate, Skill, and Education data from a selected Person, Job or Course as the basis for your search.</span></span>   <span data-ttu-id="926e5-118">Potom můžete přidávat a odebírat kritéria, uvést, jsou-li kritéria volitelné a určit pořadí důležitosti kritérií.</span><span class="sxs-lookup"><span data-stu-id="926e5-118">You can then add or remove criteria, state if the criteria is optional and rank the importance of the criteria.</span></span>  
7. <span data-ttu-id="926e5-119">Klikněte na možnost Úloha.</span><span class="sxs-lookup"><span data-stu-id="926e5-119">Click Job.</span></span>
8. <span data-ttu-id="926e5-120">V poli Úloha zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="926e5-120">In the Job field, enter or select a value.</span></span>
9. <span data-ttu-id="926e5-121">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="926e5-121">Click OK.</span></span>
10. <span data-ttu-id="926e5-122">Rozbalte pevnou záložku rozsahu a zadejte veškeré doplňkové informace, jako jsou například oddělení.</span><span class="sxs-lookup"><span data-stu-id="926e5-122">Expand the range fast tab, and add any additional information, such as department.</span></span>
11. <span data-ttu-id="926e5-123">Rozbalte pevnou záložku certifikátů pro zobrazení nebo úpravu certifikátů.</span><span class="sxs-lookup"><span data-stu-id="926e5-123">Expand the certificates fast tab to view or edit the certificates.</span></span>
12. <span data-ttu-id="926e5-124">Rozbalte pevnou záložku dovedností pro zobrazení nebo úpravu dovedností.</span><span class="sxs-lookup"><span data-stu-id="926e5-124">Expand the Skills fast tab to view or edit the skills.</span></span>
13. <span data-ttu-id="926e5-125">Rozbalte pevnou záložku Vzdělání pro zobrazení nebo úpravu vzdělání.</span><span class="sxs-lookup"><span data-stu-id="926e5-125">Expand the Education fast tab to view or edit the education criteria.</span></span>
14. <span data-ttu-id="926e5-126">Klikněte na tlačítko Spustit.</span><span class="sxs-lookup"><span data-stu-id="926e5-126">Click Execute.</span></span>
15. <span data-ttu-id="926e5-127">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="926e5-127">Click OK.</span></span>
16. <span data-ttu-id="926e5-128">Klikněte na možnost Výsledky.</span><span class="sxs-lookup"><span data-stu-id="926e5-128">Click Result.</span></span>
17. <span data-ttu-id="926e5-129">Klikněte na možnost Výsledky.</span><span class="sxs-lookup"><span data-stu-id="926e5-129">Click Result.</span></span>
18. <span data-ttu-id="926e5-130">Klepněte na možnost Obnovit.</span><span class="sxs-lookup"><span data-stu-id="926e5-130">Click Resume.</span></span>
19. <span data-ttu-id="926e5-131">Klikněte na Certifikáty.</span><span class="sxs-lookup"><span data-stu-id="926e5-131">Click Certificates.</span></span>
    * <span data-ttu-id="926e5-132">Je možné přejít dále na každou uvedenou osobu a zobrazit podrobnosti o jejich vzdělání, dovednostech, profesionálních zkušenostech atd.</span><span class="sxs-lookup"><span data-stu-id="926e5-132">You can drill further into each person listed and see details regarding their education, skills, professional experience etc.</span></span>  
20. <span data-ttu-id="926e5-133">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="926e5-133">Close the page.</span></span>
21. <span data-ttu-id="926e5-134">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="926e5-134">Close the page.</span></span>
22. <span data-ttu-id="926e5-135">Vyberte znovu výsledek.</span><span class="sxs-lookup"><span data-stu-id="926e5-135">Select result again.</span></span>
23. <span data-ttu-id="926e5-136">Klikněte na možnost Sestava.</span><span class="sxs-lookup"><span data-stu-id="926e5-136">Click Report.</span></span>
    * <span data-ttu-id="926e5-137">Sestava zobrazí seznam doporučených spárování v horní části sestavy.</span><span class="sxs-lookup"><span data-stu-id="926e5-137">The report will list the best matches at the top of the report.</span></span>  <span data-ttu-id="926e5-138">Můžete vidět, že je zde uveden element „mezera“.</span><span class="sxs-lookup"><span data-stu-id="926e5-138">You can see that there is a gap element listed.</span></span>  <span data-ttu-id="926e5-139">To je rozdíl mezi úrovní, která byla uvedena v mapování dovedností a úrovní dovednosti, která je přiřazena dané osobě.</span><span class="sxs-lookup"><span data-stu-id="926e5-139">This is the difference between the level that was listed on the skill mapping, and the level of the skill that is assigned to the person.</span></span>  
24. <span data-ttu-id="926e5-140">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="926e5-140">Close the page.</span></span>
25. <span data-ttu-id="926e5-141">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="926e5-141">Click Save.</span></span>

