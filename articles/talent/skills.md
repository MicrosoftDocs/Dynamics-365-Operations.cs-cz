---
title: "Sladění dovedností zaměstnanců s potřebami společnosti"
description: "Můžete sledovat dovednosti, které zaměstnanci, uchazeči nebo kontaktní osoby mají (nebo které by měli mít) k účinnému plnění svých rolí. Můžete také určit dovednosti, které jsou požadovány pro určitou práci."
author: kherr75
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 3a5b9f98b371dbad9b6b0538e0d9975dc5ed701c
ms.contentlocale: cs-cz
ms.lasthandoff: 04/13/2018

---

# <a name="align-workforce-skills-with-business-needs"></a><span data-ttu-id="e044c-104">Sladění dovedností zaměstnanců s potřebami společnosti</span><span class="sxs-lookup"><span data-stu-id="e044c-104">Align workforce skills with business needs</span></span>

[!INCLUDE [banner](includes/banner.md)]

<span data-ttu-id="e044c-105">Můžete sledovat dovednosti, které zaměstnanci, uchazeči nebo kontaktní osoby mají (nebo které by měli mít) k účinnému plnění svých rolí.</span><span class="sxs-lookup"><span data-stu-id="e044c-105">You can track the skills that workers, applicants, or contact persons have, or should have, to fulfill their roles effectively.</span></span> <span data-ttu-id="e044c-106">Můžete také určit dovednosti, které jsou požadovány pro určitou práci.</span><span class="sxs-lookup"><span data-stu-id="e044c-106">You can also specify the skills that are required for a specific job.</span></span>

<span data-ttu-id="e044c-107">Zde jsou příklady dovedností, které lze sledovat:</span><span class="sxs-lookup"><span data-stu-id="e044c-107">Examples of skills you can track include the following:</span></span>
-   <span data-ttu-id="e044c-108">Dozorčí - schopnost dohlížet na práci ostatních.</span><span class="sxs-lookup"><span data-stu-id="e044c-108">Supervisory – Ability to supervise the work of others.</span></span>
-   <span data-ttu-id="e044c-109">Vůdčí - schopnost vést zaměstnance a obchodní domény.</span><span class="sxs-lookup"><span data-stu-id="e044c-109">Leadership – Ability to lead employees and business domains.</span></span>
-   <span data-ttu-id="e044c-110">Plánování - schopnost dívat se dopředu, formulovat vize a schopnost tyto vize definovat.</span><span class="sxs-lookup"><span data-stu-id="e044c-110">Planning – Ability to look ahead, to form visions, and to see them through.</span></span>
-   <span data-ttu-id="e044c-111">HTML – schopnost psát v kódu HTML.</span><span class="sxs-lookup"><span data-stu-id="e044c-111">HTML – Ability to write HTML code.</span></span>

<span data-ttu-id="e044c-112">Před přiřazením dovednosti k osobě nebo pracovní pozici, vytvořením vyhledávání s mapováním dovedností nebo vytvořením profilu dovedností je nutné zadat informace o dovednostech na stránce **Dovednosti**.</span><span class="sxs-lookup"><span data-stu-id="e044c-112">Before you can assign a skill to a person or a job, create a skill-mapping search, or create a skill profile, you must enter information about the skills on the **Skills** page.</span></span> <span data-ttu-id="e044c-113">Pro každou dovednost můžete vybrat typ dovednosti a model hodnocení.</span><span class="sxs-lookup"><span data-stu-id="e044c-113">For each skill, you can select a skill type and a rating model.</span></span>

## <a name="rating-models"></a><span data-ttu-id="e044c-114">Modely hodnocení</span><span class="sxs-lookup"><span data-stu-id="e044c-114">Rating models</span></span>
<span data-ttu-id="e044c-115">Modely hodnocení pomáhají ve vyhodnocení skutečné úrovně dovedností osoby, úrovně, které mají dosáhnout, nebo úrovně dovednosti, která je požadována pro úlohu.</span><span class="sxs-lookup"><span data-stu-id="e044c-115">Rating models help evaluate a person's actual level of skill, the level they should work to achieve, or the level of skill that is required for a job.</span></span> <span data-ttu-id="e044c-116">Můžete zadat až 10 úrovní pro model hodnocení.</span><span class="sxs-lookup"><span data-stu-id="e044c-116">You can enter up to 10 levels for a rating model.</span></span>  <span data-ttu-id="e044c-117">Každé úrovni v modelu hodnocení je přiřazen koeficient.</span><span class="sxs-lookup"><span data-stu-id="e044c-117">Each level in a rating model is assigned a factor.</span></span>  <span data-ttu-id="e044c-118">Hodnota koeficientu se použije k normalizaci výsledků dovedností, které používají různé modely hodnocení.</span><span class="sxs-lookup"><span data-stu-id="e044c-118">The factor value will be used to normalize the scores of skills that use different rating models.</span></span>  <span data-ttu-id="e044c-119">Koeficient musí být číslo mezi 0 a 9 a každá úroveň musí mít jedinečný koeficient.</span><span class="sxs-lookup"><span data-stu-id="e044c-119">The factor must be a number between 0-9 and each level must have a unique factor.</span></span>  <span data-ttu-id="e044c-120">Úrovně s vyšší hodnotou koeficientu nesou v modelu hodnocení větší váhu.</span><span class="sxs-lookup"><span data-stu-id="e044c-120">Levels with higher factor values carry more weight in a rating model.</span></span>

## <a name="specify-job-skills"></a><span data-ttu-id="e044c-121">Určení dovedností pro úlohu</span><span class="sxs-lookup"><span data-stu-id="e044c-121">Specify job skills</span></span>
<span data-ttu-id="e044c-122">Při zadání informací o pracovní pozici můžete zadat dovednosti, které má daná osoba mít k provedení práce v rámci pracovní pozice.</span><span class="sxs-lookup"><span data-stu-id="e044c-122">When you enter information about a job, you can specify the skills that a person should have to perform the work required for the job.</span></span>  <span data-ttu-id="e044c-123">Dále je možné určit požadovanou úroveň pro každou dovednost a také úroveň důležitosti dané dovednosti.</span><span class="sxs-lookup"><span data-stu-id="e044c-123">In addition you can specify the desired level for each skill as well the level of importance of the skill.</span></span> <span data-ttu-id="e044c-124">Různé pracovní pozice mohou vyžadovat různé úrovně důležitosti pro stejné dovednosti.</span><span class="sxs-lookup"><span data-stu-id="e044c-124">Different jobs can require different levels of importance for the same skill.</span></span>

## <a name="enter-skills-for-workers-applicants-or-contacts"></a><span data-ttu-id="e044c-125">Zadejte dovedností zaměstnanců, uchazečů nebo kontaktů</span><span class="sxs-lookup"><span data-stu-id="e044c-125">Enter skills for workers, applicants, or contacts</span></span>
<span data-ttu-id="e044c-126">Můžete zadat cílové dovednosti, nebo skutečné dovedností zaměstnanců, uchazečů nebo kontaktů.</span><span class="sxs-lookup"><span data-stu-id="e044c-126">You can enter target skills or actual skills for workers, applicants, or contacts.</span></span> <span data-ttu-id="e044c-127">Cílové dovednosti jsou dovednosti, kterých se osoba chystá dosáhnout.</span><span class="sxs-lookup"><span data-stu-id="e044c-127">A target skill is a skill that a person plans to achieve.</span></span> <span data-ttu-id="e044c-128">Skutečná dovednost je dovednost, kterou pracovník aktuálně disponuje.</span><span class="sxs-lookup"><span data-stu-id="e044c-128">An actual skill is a skill that a person currently has.</span></span>

## <a name="skill-mapping-and-skill-mapping-profiles"></a><span data-ttu-id="e044c-129"> Mapování dovedností a profily mapování dovedností</span><span class="sxs-lookup"><span data-stu-id="e044c-129">Skill mapping and Skill mapping profiles</span></span>
<span data-ttu-id="e044c-130">Lze vytvořit hledání v rámci mapování dovedností k vyhledání pracovníka, uchazeče nebo kontaktní osoby, která je kvalifikována k provádění určitého úkolu.</span><span class="sxs-lookup"><span data-stu-id="e044c-130">You can create a skill-mapping search to find a worker, applicant, or contact person who is qualified to perform a specific type of task.</span></span> <span data-ttu-id="e044c-131">Při hledání v rámci mapování dovedností se prohledávají dovednosti, certifikáty vzdělání, pozice důvěry a zkušenosti s projektem a jsou vráceny výsledky, které odpovídají zadaným kritériím.</span><span class="sxs-lookup"><span data-stu-id="e044c-131">Skill-mapping searches look across skills, education, certificates, positions of trust and project experience and return results that match the criteria entered.</span></span>  <span data-ttu-id="e044c-132">Například může být užitečné vědět, kteří pracovníci ve vaší organizaci získali CPA.</span><span class="sxs-lookup"><span data-stu-id="e044c-132">For example, it might be useful to know which workers in your organization earned their CPA.</span></span>

<span data-ttu-id="e044c-133">Profily mapování dovedností umožňují vyhledání aktuálního zaměstnance nebo kandidáta s kvalifikací, která přímo odpovídá obchodním potřebám.</span><span class="sxs-lookup"><span data-stu-id="e044c-133">Skill-mapping profiles allow you to find current employees or candidates with qualifications that directly correspond to business needs.</span></span>  <span data-ttu-id="e044c-134">Můžete například vytvořit profil mapování dovedností pro otevřenou pozici ve vaší organizaci.</span><span class="sxs-lookup"><span data-stu-id="e044c-134">For example, you could create a skill-mapping profile for an open position in your organization.</span></span> <span data-ttu-id="e044c-135">Vytvořením profilu pro určitou pozici a zkopírováním dovedností, vzdělání a certifikátů z této pracovní pozice do profilu lze rychle vyhledat pracovníky, uchazeče a kontaktní osoby, které odpovídají jednomu nebo více kritériím zadaným v profilu, a zobrazit seznam uchazečů, jejichž dovednosti nejlépe odpovídají požadovaným dovednostem pro pracovní pozici.</span><span class="sxs-lookup"><span data-stu-id="e044c-135">By creating a profile for a particular job and copying the skills, education and certificates from that job to the profile, you can quickly search workers, applicants and contact persons who match one or more of the criteria entered on the profile and view a list of the candidates whose skills most closely match the skills required for the job.</span></span>

> <span data-ttu-id="e044c-136">**Poznámka** V seznamu s výsledky mapování dovednosti mohou být zobrazeni nebo zahrnuti v profilu dovedností pouze zaměstnanci, uchazeči a kontaktní osoby, které jsou vybrány k zahrnutí do hledání v rámci mapování dovedností.</span><span class="sxs-lookup"><span data-stu-id="e044c-136">**Note** Only workers, applicants, and contact persons who are selected to be included in skill mapping searches can be displayed in a skill-mapping results list, or included in a skill profile.</span></span> <span data-ttu-id="e044c-137">Chcete-li zahrnout pracovníka, uchazeče nebo kontaktní osobu do vyhledávání v rámci mapování dovedností, nastavte možnost **Zahrnout do mapování dovedností** na hodnotu Ano na následujících stránkách:</span><span class="sxs-lookup"><span data-stu-id="e044c-137">To include a worker, applicant, or contact person in skill mapping searches, set the **Include in skill mapping** selection to Yes in the following pages:</span></span>
> 
> + <span data-ttu-id="e044c-138">Pracovní podproces</span><span class="sxs-lookup"><span data-stu-id="e044c-138">Worker</span></span>
> + <span data-ttu-id="e044c-139">Zaměstnanec</span><span class="sxs-lookup"><span data-stu-id="e044c-139">Employee</span></span>
> + <span data-ttu-id="e044c-140">Uchazeč</span><span class="sxs-lookup"><span data-stu-id="e044c-140">Applicant</span></span>
> + <span data-ttu-id="e044c-141">Kontakty</span><span class="sxs-lookup"><span data-stu-id="e044c-141">Contacts</span></span>

## <a name="skill-gap-analysis-and-skill-profile-analysis"></a><span data-ttu-id="e044c-142">Analýza mezer v dovednostech a analýza profilu dovedností</span><span class="sxs-lookup"><span data-stu-id="e044c-142">Skill gap analysis and skill profile analysis</span></span>
<span data-ttu-id="e044c-143">Můžete vytvořit analýzu profilu dovedností, a zobrazit tak seznam kompetencí pro pracovníka, uchazeče nebo kontaktní osobu k určitému datu.</span><span class="sxs-lookup"><span data-stu-id="e044c-143">You can create a skill profile analysis to view a list of the competencies of a worker, applicant, or contact person as of a specific date.</span></span> <span data-ttu-id="e044c-144">Můžete vytvořit analýzu dovednostních mezer k porovnání dovedností dané osoby s dovednostmi požadovanými pro určitou úlohu.</span><span class="sxs-lookup"><span data-stu-id="e044c-144">You can create a skill gap analysis to compare a person’s skills and the skills that are required for a specific job.</span></span>  



<a name="see-also"></a><span data-ttu-id="e044c-145">Viz také</span><span class="sxs-lookup"><span data-stu-id="e044c-145">See also</span></span>
--------

[<span data-ttu-id="e044c-146">Lidské zdroje</span><span class="sxs-lookup"><span data-stu-id="e044c-146">Human resources</span></span>](index.md)




