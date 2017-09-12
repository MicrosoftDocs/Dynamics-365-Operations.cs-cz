---
title: "Nastavení školících kurzů"
description: "Správci lidských zdrojů a vedoucí pracovníci mohou funkce kurzů používat ke správě informací o školeních nabízených pracovníkům."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 0ab79e85872c19e30f24e182ea483687ecc0bc09
ms.contentlocale: cs-cz
ms.lasthandoff: 06/29/2017


---

# <a name="set-up-training-courses"></a><span data-ttu-id="523fa-103">Nastavení školících kurzů</span><span class="sxs-lookup"><span data-stu-id="523fa-103">Set up training courses</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="523fa-104">Správci lidských zdrojů a vedoucí pracovníci mohou funkce kurzů používat ke správě informací o školeních nabízených pracovníkům.</span><span class="sxs-lookup"><span data-stu-id="523fa-104">Human resources administrators and managers can use the courses features to maintain information about the training that's offered to workers.</span></span>

 <a name="set-up-prerequisites"></a><span data-ttu-id="523fa-105"> Nastavení předpokladů</span><span class="sxs-lookup"><span data-stu-id="523fa-105">Set up prerequisites</span></span>
---------------------

<span data-ttu-id="523fa-106">Před vytvořením kurzů je nutné znát a nastavit následující informace.</span><span class="sxs-lookup"><span data-stu-id="523fa-106">The following information is required and must be set up before you create courses.</span></span>
-   <span data-ttu-id="523fa-107">**Typy kurzů**</span><span class="sxs-lookup"><span data-stu-id="523fa-107">**Course types**</span></span>

<span data-ttu-id="523fa-108">Tyto informace jsou volitelné informace, které lze určit pro kurzy.</span><span class="sxs-lookup"><span data-stu-id="523fa-108">The following information is optional information that you can specify for courses.</span></span> <span data-ttu-id="523fa-109">Pokud víte, že budete zadávat tyto údaje pro kurzy, nastavte je před vytvořením záznamů kurzu.</span><span class="sxs-lookup"><span data-stu-id="523fa-109">If you know that you will be entering this information for courses, you should set up this information before you create course records.</span></span>
-   <span data-ttu-id="523fa-110">**Skupiny učeben**</span><span class="sxs-lookup"><span data-stu-id="523fa-110">**Classroom groups**</span></span>
-   <span data-ttu-id="523fa-111">**Skupiny kurzů**</span><span class="sxs-lookup"><span data-stu-id="523fa-111">**Course groups**</span></span>
-   <span data-ttu-id="523fa-112">**Místo konání kurzu**</span><span class="sxs-lookup"><span data-stu-id="523fa-112">**Course locations**</span></span>
-   <span data-ttu-id="523fa-113">**Učebny**</span><span class="sxs-lookup"><span data-stu-id="523fa-113">**Classrooms**</span></span>
-   <span data-ttu-id="523fa-114">**Instruktoři**</span><span class="sxs-lookup"><span data-stu-id="523fa-114">**Instructors**</span></span>

## <a name="course-types"></a><span data-ttu-id="523fa-115">Typy kurzů</span><span class="sxs-lookup"><span data-stu-id="523fa-115">Course types</span></span>
<span data-ttu-id="523fa-116">Typy kurzů slouží k rozdělení kurzů podle struktury nebo obsahu kurzu.</span><span class="sxs-lookup"><span data-stu-id="523fa-116">You can use course types to categorize courses according to the structure or content of the course.</span></span> <span data-ttu-id="523fa-117">Na stránce **Typy kurzů** můžete vytvořit typy kurzů.</span><span class="sxs-lookup"><span data-stu-id="523fa-117">You can create course types on the **Course types** page.</span></span> <span data-ttu-id="523fa-118">Musíte vybrat typ kurzu, když vytváříte záznam kurzu.</span><span class="sxs-lookup"><span data-stu-id="523fa-118">You must select a course type when you create a course record.</span></span>

## <a name="course-setup-type"></a><span data-ttu-id="523fa-119">Typ nastavení kurzu</span><span class="sxs-lookup"><span data-stu-id="523fa-119">Course setup type</span></span>
<span data-ttu-id="523fa-120">V následující tabulce jsou uvedeny tři typy nastavení kurzů.</span><span class="sxs-lookup"><span data-stu-id="523fa-120">The following table lists the three setup types for courses.</span></span> <span data-ttu-id="523fa-121">Typy nastavení určují strukturu kurzu.</span><span class="sxs-lookup"><span data-stu-id="523fa-121">Setup types determine the structure of the course.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="523fa-122">Typ nastavení</span><span class="sxs-lookup"><span data-stu-id="523fa-122">Setup type</span></span></th>
<th><span data-ttu-id="523fa-123">Popis</span><span class="sxs-lookup"><span data-stu-id="523fa-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="523fa-124"><strong>Standardní</strong></span><span class="sxs-lookup"><span data-stu-id="523fa-124"><strong>Standard</strong></span></span></td>
<td><span data-ttu-id="523fa-125">Vyberte tento typ pro kurzy, které nemají denní agendu.</span><span class="sxs-lookup"><span data-stu-id="523fa-125">Select this type for courses that will not have a daily agenda.</span></span> <span data-ttu-id="523fa-126">Toto je výchozí typ nastavení, když vytváříte nový kurz.</span><span class="sxs-lookup"><span data-stu-id="523fa-126">This is the default setup type when you create a new course.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="523fa-127"><strong>Agenda</strong></span><span class="sxs-lookup"><span data-stu-id="523fa-127"><strong>Agenda</strong></span></span></td>
<td><span data-ttu-id="523fa-128">Tento typ vyberte pro naplánování podrobností pro jednotlivé dny vícedenního kurzu.</span><span class="sxs-lookup"><span data-stu-id="523fa-128">Select this type to plan the details of each day of a course that takes place over multiple days.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="523fa-129"><strong>Agenda + relace</strong></span><span class="sxs-lookup"><span data-stu-id="523fa-129"><strong>Agenda + session</strong></span></span></td>
<td><span data-ttu-id="523fa-130">Vyberte tento typ pro složitější kurzy.</span><span class="sxs-lookup"><span data-stu-id="523fa-130">Select this type for the more complex courses.</span></span> <span data-ttu-id="523fa-131">Agendu kurzu lze například rozdělit do běhů a relací.</span><span class="sxs-lookup"><span data-stu-id="523fa-131">For example, you can divide the agenda for the course into tracks and sessions.</span></span>
<ul>
<li><span data-ttu-id="523fa-132"><strong>Běhy </strong> – Běhy jsou konkrétní témata kurzu.</span><span class="sxs-lookup"><span data-stu-id="523fa-132"><strong>Track</strong> – Tracks are specific subject areas for a course.</span></span></li>
<li><span data-ttu-id="523fa-133"><strong>Relace</strong> – Relace rozdělují běhy a mohou identifikovat specifické procesy nebo postupy, které se vztahují k jednotlivým běhům.</span><span class="sxs-lookup"><span data-stu-id="523fa-133"><strong>Sessions</strong> – Sessions divide up tracks and help identify specific processes or techniques that are relevant to the track.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="course-tasks"></a><span data-ttu-id="523fa-134">Úkoly kurzu</span><span class="sxs-lookup"><span data-stu-id="523fa-134">Course tasks</span></span>
<span data-ttu-id="523fa-135">U každého kurzu můžete provést následující úlohy.</span><span class="sxs-lookup"><span data-stu-id="523fa-135">For each course, you can complete the following tasks.</span></span>
-   <span data-ttu-id="523fa-136">Registrovat účastníky</span><span class="sxs-lookup"><span data-stu-id="523fa-136">Register participants</span></span>
-   <span data-ttu-id="523fa-137">Nastavit uzávěrku registrace</span><span class="sxs-lookup"><span data-stu-id="523fa-137">Specify a registration deadline</span></span>
-   <span data-ttu-id="523fa-138">Definovat minimální a maximální počet účastníků</span><span class="sxs-lookup"><span data-stu-id="523fa-138">Define the minimum and maximum number of participants</span></span>
-   <span data-ttu-id="523fa-139">Přiřadit místo konání kurzu a učebnu</span><span class="sxs-lookup"><span data-stu-id="523fa-139">Assign a course location and classroom</span></span>
-   <span data-ttu-id="523fa-140">Doporučit hotely účastníkům kurzu</span><span class="sxs-lookup"><span data-stu-id="523fa-140">Recommend hotels to course participants</span></span>
-   <span data-ttu-id="523fa-141">Vytvořit popis kurzu, který je poté možné zveřejnit na portálu Samoobsluha pro zaměstnance</span><span class="sxs-lookup"><span data-stu-id="523fa-141">Create a course description, which you can then advertise on Employee self service</span></span>

  ><span data-ttu-id="523fa-142">**Poznámka** Kurz lze odstranit pouze v případě, že do něj není nikdo zaregistrován.</span><span class="sxs-lookup"><span data-stu-id="523fa-142">**Note** You can delete a course only if no one has registered for it.</span></span> 
    
## <a name="course-statuses"></a><span data-ttu-id="523fa-143">Stavy kurzu</span><span class="sxs-lookup"><span data-stu-id="523fa-143">Course statuses</span></span>
<span data-ttu-id="523fa-144">V následující tabulce jsou uvedeny možné stavy kurzu a akce, které lze provádět, je-li kurz nachází ve specifickém stavu.</span><span class="sxs-lookup"><span data-stu-id="523fa-144">The following table lists the possible course statuses and the actions that you can complete when the course has a specific status.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="523fa-145">Stav</span><span class="sxs-lookup"><span data-stu-id="523fa-145">Status</span></span></th>
<th><span data-ttu-id="523fa-146">Akce</span><span class="sxs-lookup"><span data-stu-id="523fa-146">Actions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="523fa-147"><strong>Vytvořeno</strong></span><span class="sxs-lookup"><span data-stu-id="523fa-147"><strong>Created</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="523fa-148">Zadávání a úprava informací o kurzu.</span><span class="sxs-lookup"><span data-stu-id="523fa-148">Enter and modify course information.</span></span></li>
<li><span data-ttu-id="523fa-149">Změňte stav kurzu na <strong>Otevřen</strong>, aby se pracovníci mohli do kurzu registrovat.</span><span class="sxs-lookup"><span data-stu-id="523fa-149">Change the course status to <strong>Open</strong> so that workers can register for the course.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="523fa-150"><strong>Otevřít</strong></span><span class="sxs-lookup"><span data-stu-id="523fa-150"><strong>Open</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="523fa-151">Zaregistrujte účastníky na kurz.</span><span class="sxs-lookup"><span data-stu-id="523fa-151">Register participants for the course.</span></span></li>
<li><span data-ttu-id="523fa-152">Odeberte účastníky z kurzu.</span><span class="sxs-lookup"><span data-stu-id="523fa-152">Remove participants from the course.</span></span></li>
<li><span data-ttu-id="523fa-153">Potvrďte účastníky kurzu.</span><span class="sxs-lookup"><span data-stu-id="523fa-153">Confirm participants for the course.</span></span></li>
<li><span data-ttu-id="523fa-154">Změňte stav kurzu na <strong>Uzavřeno</strong> nebo <strong>Zrušeno</strong>.</span><span class="sxs-lookup"><span data-stu-id="523fa-154">Change the course status to <strong>Closed</strong> or <strong>Canceled</strong>.</span></span></li>
<li><span data-ttu-id="523fa-155">Naplánujte dotazníky pro účastníky, jejichž stav je <strong>Potvrzeno</strong>.</span><span class="sxs-lookup"><span data-stu-id="523fa-155">Plan questionnaires for participants whose status is <strong>Confirmed</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="523fa-156"><strong>Zavřeno</strong></span><span class="sxs-lookup"><span data-stu-id="523fa-156"><strong>Closed</strong></span></span></td>
<td><span data-ttu-id="523fa-157">Kurz můžete znovu otevřít.</span><span class="sxs-lookup"><span data-stu-id="523fa-157">You can reopen the course.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="523fa-158"><strong>Zrušeno</strong></span><span class="sxs-lookup"><span data-stu-id="523fa-158"><strong>Canceled</strong></span></span></td>
<td><span data-ttu-id="523fa-159">Kurz můžete znovu otevřít.</span><span class="sxs-lookup"><span data-stu-id="523fa-159">You can reopen the course.</span></span></td>
</tr>
</tbody>
</table>

## <a name="course-participants"></a><span data-ttu-id="523fa-160">Účastníci kurzu</span><span class="sxs-lookup"><span data-stu-id="523fa-160">Course participants</span></span>
<span data-ttu-id="523fa-161">Účastníky kurzu jsou pracovníci, uchazeči nebo kontaktní osoby, kteří se účastní školicího kurzu nebo události.</span><span class="sxs-lookup"><span data-stu-id="523fa-161">Course participants are workers, applicants, or contact persons who participate in a training course or event.</span></span> <span data-ttu-id="523fa-162">Účastníky můžete registrovat pouze pro otevřené kurzy.</span><span class="sxs-lookup"><span data-stu-id="523fa-162">You can only register participants for open courses.</span></span> <span data-ttu-id="523fa-163">Maximální a minimální počty účastníků, které lze do kurzu registrovat, jsou uvedeny na pevné záložce **Obecné** na stránce **Kurzy**.</span><span class="sxs-lookup"><span data-stu-id="523fa-163">The minimum and maximum number of participants that you can register for a course is defined on the **General** FastTab on the **Courses** page.</span></span>

<a name="workflow"></a><span data-ttu-id="523fa-164">Workflow</span><span class="sxs-lookup"><span data-stu-id="523fa-164">Workflow</span></span>
--------

<span data-ttu-id="523fa-165">Zaměstnancům, kteří se do kurzu zaregistrují na stránce **Samoobsluha pro zaměstnance**, může být registrace nasměrována do workflowu pro schválení.</span><span class="sxs-lookup"><span data-stu-id="523fa-165">Employees who register for a course through the **Employee self service** page can have their registration routed through workflow for approval.</span></span>  <span data-ttu-id="523fa-166">Workflow lze přiřadit ke kurzu na pevné záložce **Obecné** na stránce **Kurzy**.</span><span class="sxs-lookup"><span data-stu-id="523fa-166">A workflow can be assigned to a course on the **General** FastTab on the **Courses** page.</span></span>






