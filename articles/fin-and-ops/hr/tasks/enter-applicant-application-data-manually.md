---
title: Ruční zadávání dat o přihlášce a uchazeči
description: Tento postup popisuje, jak ručně spravovat informace o uchazečích a jejich přihláškách.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmApplicant, LogisticsContactInfoGrid, HRMApplication,  DirPartyTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ea61e3c1d76ade6e0d694b4b521e4be76fc8799d
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2019
ms.locfileid: "1507707"
---
# <a name="enter-applicant-and-application-data-manually"></a><span data-ttu-id="04a13-103">Ruční zadávání dat o přihlášce a uchazeči</span><span class="sxs-lookup"><span data-stu-id="04a13-103">Enter applicant and application data manually</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="04a13-104">Tento postup popisuje, jak ručně spravovat informace o uchazečích a jejich přihláškách.</span><span class="sxs-lookup"><span data-stu-id="04a13-104">This procedure shows how to manually maintain information about applicants and their application.</span></span>   <span data-ttu-id="04a13-105">Můžete zadat a spravovat osobní údaje, data a časy pohovoru, odkazy, kompetence a požadavky na ubytování pro uchazeče.</span><span class="sxs-lookup"><span data-stu-id="04a13-105">You can enter and maintain personal information, interview dates and times, references, competencies, and accommodation requests for applicants.</span></span> <span data-ttu-id="04a13-106">Také můžete aktualizovat stav uchazečových žádostí o zaměstnání a vytváření dopisů nebo e-mailových zpráv ke komunikaci s uchazeči.</span><span class="sxs-lookup"><span data-stu-id="04a13-106">You can also update the status of applicants’ applications for employment and create letters or email messages to communicate with applicants.</span></span> <span data-ttu-id="04a13-107">Při vytvoření záznamu žadatele se vytvoří osobní záznam tohoto uchazeče v globálním adresáři.</span><span class="sxs-lookup"><span data-stu-id="04a13-107">When you create an applicant record, a person record for that applicant is created in the global address book.</span></span>       <span data-ttu-id="04a13-108">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="04a13-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-new-applicant-record"></a><span data-ttu-id="04a13-109">Vytvoření záznamu nového uchazeče</span><span class="sxs-lookup"><span data-stu-id="04a13-109">Create a new applicant record</span></span>
1. <span data-ttu-id="04a13-110">Přejděte na Lidské zdroje > Nábor > Uchazeči > Uchazeči.</span><span class="sxs-lookup"><span data-stu-id="04a13-110">Go to Human resources > Recruitment > Applicants > Applicants.</span></span>
2. <span data-ttu-id="04a13-111">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="04a13-111">Click New.</span></span>
3. <span data-ttu-id="04a13-112">Do pole Křestní jméno zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="04a13-112">In the First name field, type a value.</span></span>
4. <span data-ttu-id="04a13-113">Do pole příjmení zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="04a13-113">In the Last name field, type a value.</span></span>
    * <span data-ttu-id="04a13-114">Pokud jsou k dispozici, můžete zadat další informace o žadateli.</span><span class="sxs-lookup"><span data-stu-id="04a13-114">You can enter additional applicant information if it's available.</span></span> <span data-ttu-id="04a13-115">Informace mohou například zahrnovat nejvyšší vzdělání uchazeče, aktuální pracovní funkci nebo předchozího zaměstnavatele.</span><span class="sxs-lookup"><span data-stu-id="04a13-115">For example, information can include the applicant's highest degree, current job title, or previous employer.</span></span>  
5. <span data-ttu-id="04a13-116">Přepněte rozšíření oddílu Kontaktní údaje.</span><span class="sxs-lookup"><span data-stu-id="04a13-116">Toggle the expansion of the Contact information section.</span></span>
6. <span data-ttu-id="04a13-117">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="04a13-117">Click Add.</span></span>
7. <span data-ttu-id="04a13-118">Do pole Popis zadejte E-mail pro komunikaci.</span><span class="sxs-lookup"><span data-stu-id="04a13-118">In the Description field, type 'Communications email'.</span></span>
8. <span data-ttu-id="04a13-119">Vyberte volbu v poli Typ.</span><span class="sxs-lookup"><span data-stu-id="04a13-119">In the Type field, select an option.</span></span>
9. <span data-ttu-id="04a13-120">Zadejte hodnotu do pole Kontaktní číslo/adresa.</span><span class="sxs-lookup"><span data-stu-id="04a13-120">In the Contact number/address field, type a value.</span></span>
    * <span data-ttu-id="04a13-121">Tento e-mailová adresa bude použita pro generování e-mailové komunikace s uchazečem.</span><span class="sxs-lookup"><span data-stu-id="04a13-121">This email address will be used to generate email communication with the applicant.</span></span>  
10. <span data-ttu-id="04a13-122">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="04a13-122">Click Add.</span></span>
11. <span data-ttu-id="04a13-123">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="04a13-123">In the Description field, type a value.</span></span>
12. <span data-ttu-id="04a13-124">Zadejte hodnotu do pole Kontaktní číslo/adresa.</span><span class="sxs-lookup"><span data-stu-id="04a13-124">In the Contact number/address field, type a value.</span></span>
    * <span data-ttu-id="04a13-125">Osobní informace uchazeče.</span><span class="sxs-lookup"><span data-stu-id="04a13-125">Applicant personal information.</span></span>  
    * <span data-ttu-id="04a13-126">V případě potřeby můžete zadat další osobní informace pro žadatele.</span><span class="sxs-lookup"><span data-stu-id="04a13-126">You can enter additional personal information for the applicant, if needed.</span></span> <span data-ttu-id="04a13-127">Ty mohou například zahrnovat datum narození, údaje o etnickém původu, pohlaví nebo rodinný stav.</span><span class="sxs-lookup"><span data-stu-id="04a13-127">For example, this can include birth date, ethnic origin, gender, or marital status.</span></span>  
13. <span data-ttu-id="04a13-128">V podokně akcí klikněte na možnost Kompetence.</span><span class="sxs-lookup"><span data-stu-id="04a13-128">On the Action Pane, click Competencies.</span></span>
    * <span data-ttu-id="04a13-129">Můžete zadat profil kompetencí uchazeče, včetně jejich dovedností, profesionálních zkušeností, vzdělání, testů a certifikátů.</span><span class="sxs-lookup"><span data-stu-id="04a13-129">You can enter the applicant's competency profile, including their skills, professional experiences, education, tests, or certificates.</span></span>  
    * <span data-ttu-id="04a13-130">Tyto informace slouží k mapování dovedností uchazeče k dovednostem spojeným s úlohami, které jsou definovány v datech společnosti.</span><span class="sxs-lookup"><span data-stu-id="04a13-130">This information can be used to map the applicant's skills to the skills associated with the jobs defined in your company's data.</span></span>   

## <a name="create-an-application-for-the-applicant"></a><span data-ttu-id="04a13-131">Vytvoření přihlášky pro uchazeče</span><span class="sxs-lookup"><span data-stu-id="04a13-131">Create an application for the applicant</span></span>
1. <span data-ttu-id="04a13-132">Klikněte na Přihlášky.</span><span class="sxs-lookup"><span data-stu-id="04a13-132">Click Applications.</span></span>
2. <span data-ttu-id="04a13-133">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="04a13-133">Click New.</span></span>
3. <span data-ttu-id="04a13-134">V poli Náborový projekt kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="04a13-134">In the Recruitment project field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="04a13-135">Výběrem náborového projektu bude uchazeč přidružen ke konkrétní otevřené pozici zahrnuté v daném náborovém projektu.</span><span class="sxs-lookup"><span data-stu-id="04a13-135">By selecting a recruitment project, the applicant will be associated with a specific opening included in that recruitment project.</span></span>  
4. <span data-ttu-id="04a13-136">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="04a13-136">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="04a13-137">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="04a13-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="04a13-138">Ve výchozím nastavení je pozice a oddělení založeno na vybraném náborovém projektu.</span><span class="sxs-lookup"><span data-stu-id="04a13-138">By default, the job and department are based on the selected recruitment project.</span></span>  
6. <span data-ttu-id="04a13-139">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="04a13-139">Click Save.</span></span>
    * <span data-ttu-id="04a13-140">Po uložení přihlášky bude k ní možné připojit dokumenty, včetně zkušeností, odměn a průvodního dopisu uchazeče.</span><span class="sxs-lookup"><span data-stu-id="04a13-140">After saving the application, you can attach documents to it, including the applicant's experience, awards, and cover letter.</span></span>  

