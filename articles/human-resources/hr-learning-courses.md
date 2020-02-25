---
title: Nastavení školících kurzů
description: Správci lidských zdrojů a vedoucí pracovníci mohou funkce kurzů používat ke správě informací o školeních nabízených pracovníkům.
author: andreabichsel
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: c3c23ab6fca3f97fbca9edfe83c656e7ca8a2800
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008345"
---
# <a name="set-up-training-courses"></a><span data-ttu-id="c8b54-103">Nastavení školících kurzů</span><span class="sxs-lookup"><span data-stu-id="c8b54-103">Set up training courses</span></span>

<span data-ttu-id="c8b54-104">Správci lidských zdrojů a vedoucí pracovníci mohou funkce kurzů používat ke správě informací o školeních nabízených pracovníkům.</span><span class="sxs-lookup"><span data-stu-id="c8b54-104">Human resources administrators and managers can use the courses features to maintain information about the training that's offered to workers.</span></span>

 <a name="set-up-prerequisites"></a><span data-ttu-id="c8b54-105"> Nastavení předpokladů</span><span class="sxs-lookup"><span data-stu-id="c8b54-105">Set up prerequisites</span></span>
---------------------

<span data-ttu-id="c8b54-106">Před vytvořením kurzů je nutné znát a nastavit následující informace.</span><span class="sxs-lookup"><span data-stu-id="c8b54-106">The following information is required and must be set up before you create courses.</span></span>
-   <span data-ttu-id="c8b54-107">**Typy kurzů**</span><span class="sxs-lookup"><span data-stu-id="c8b54-107">**Course types**</span></span>

<span data-ttu-id="c8b54-108">Tyto informace jsou volitelné informace, které lze určit pro kurzy.</span><span class="sxs-lookup"><span data-stu-id="c8b54-108">The following information is optional information that you can specify for courses.</span></span> <span data-ttu-id="c8b54-109">Pokud víte, že budete zadávat tyto údaje pro kurzy, nastavte je před vytvořením záznamů kurzu.</span><span class="sxs-lookup"><span data-stu-id="c8b54-109">If you know that you will be entering this information for courses, you should set up this information before you create course records.</span></span>
-   <span data-ttu-id="c8b54-110">**Skupiny učeben**</span><span class="sxs-lookup"><span data-stu-id="c8b54-110">**Classroom groups**</span></span>
-   <span data-ttu-id="c8b54-111">**Skupiny kurzů**</span><span class="sxs-lookup"><span data-stu-id="c8b54-111">**Course groups**</span></span>
-   <span data-ttu-id="c8b54-112">**Místo konání kurzu**</span><span class="sxs-lookup"><span data-stu-id="c8b54-112">**Course locations**</span></span>
-   <span data-ttu-id="c8b54-113">**Učebny**</span><span class="sxs-lookup"><span data-stu-id="c8b54-113">**Classrooms**</span></span>
-   <span data-ttu-id="c8b54-114">**Instruktoři**</span><span class="sxs-lookup"><span data-stu-id="c8b54-114">**Instructors**</span></span>

## <a name="course-types"></a><span data-ttu-id="c8b54-115">Typy kurzů</span><span class="sxs-lookup"><span data-stu-id="c8b54-115">Course types</span></span>
<span data-ttu-id="c8b54-116">Typy kurzů slouží k rozdělení kurzů podle struktury nebo obsahu kurzu.</span><span class="sxs-lookup"><span data-stu-id="c8b54-116">You can use course types to categorize courses according to the structure or content of the course.</span></span> <span data-ttu-id="c8b54-117">Na stránce **Typy kurzů** můžete vytvořit typy kurzů.</span><span class="sxs-lookup"><span data-stu-id="c8b54-117">You can create course types on the **Course types** page.</span></span> <span data-ttu-id="c8b54-118">Musíte vybrat typ kurzu, když vytváříte záznam kurzu.</span><span class="sxs-lookup"><span data-stu-id="c8b54-118">You must select a course type when you create a course record.</span></span>

## <a name="course-setup-type"></a><span data-ttu-id="c8b54-119">Typ nastavení kurzu</span><span class="sxs-lookup"><span data-stu-id="c8b54-119">Course setup type</span></span>
<span data-ttu-id="c8b54-120">V následující tabulce jsou uvedeny tři typy nastavení kurzů.</span><span class="sxs-lookup"><span data-stu-id="c8b54-120">The following table lists the three setup types for courses.</span></span> <span data-ttu-id="c8b54-121">Typy nastavení určují strukturu kurzu.</span><span class="sxs-lookup"><span data-stu-id="c8b54-121">Setup types determine the structure of the course.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c8b54-122">Typ nastavení</span><span class="sxs-lookup"><span data-stu-id="c8b54-122">Setup type</span></span></th>
<th><span data-ttu-id="c8b54-123">Popis</span><span class="sxs-lookup"><span data-stu-id="c8b54-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8b54-124"><strong>Standardní</strong></span><span class="sxs-lookup"><span data-stu-id="c8b54-124"><strong>Standard</strong></span></span></td>
<td><span data-ttu-id="c8b54-125">Vyberte tento typ pro kurzy, které nemají denní agendu.</span><span class="sxs-lookup"><span data-stu-id="c8b54-125">Select this type for courses that will not have a daily agenda.</span></span> <span data-ttu-id="c8b54-126">Toto je výchozí typ nastavení, když vytváříte nový kurz.</span><span class="sxs-lookup"><span data-stu-id="c8b54-126">This is the default setup type when you create a new course.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8b54-127"><strong>Agenda</strong></span><span class="sxs-lookup"><span data-stu-id="c8b54-127"><strong>Agenda</strong></span></span></td>
<td><span data-ttu-id="c8b54-128">Tento typ vyberte pro naplánování podrobností pro jednotlivé dny vícedenního kurzu.</span><span class="sxs-lookup"><span data-stu-id="c8b54-128">Select this type to plan the details of each day of a course that takes place over multiple days.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c8b54-129"><strong>Agenda + relace</strong></span><span class="sxs-lookup"><span data-stu-id="c8b54-129"><strong>Agenda + session</strong></span></span></td>
<td><span data-ttu-id="c8b54-130">Vyberte tento typ pro složitější kurzy.</span><span class="sxs-lookup"><span data-stu-id="c8b54-130">Select this type for the more complex courses.</span></span> <span data-ttu-id="c8b54-131">Agendu kurzu lze například rozdělit do běhů a relací.</span><span class="sxs-lookup"><span data-stu-id="c8b54-131">For example, you can divide the agenda for the course into tracks and sessions.</span></span>
<ul>
<li><span data-ttu-id="c8b54-132"><strong>Běhy </strong> – Běhy jsou konkrétní témata kurzu.</span><span class="sxs-lookup"><span data-stu-id="c8b54-132"><strong>Track</strong> – Tracks are specific subject areas for a course.</span></span></li>
<li><span data-ttu-id="c8b54-133"><strong>Relace</strong> – Relace rozdělují běhy a mohou identifikovat specifické procesy nebo postupy, které se vztahují k jednotlivým běhům.</span><span class="sxs-lookup"><span data-stu-id="c8b54-133"><strong>Sessions</strong> – Sessions divide up tracks and help identify specific processes or techniques that are relevant to the track.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="course-tasks"></a><span data-ttu-id="c8b54-134">Úkoly kurzu</span><span class="sxs-lookup"><span data-stu-id="c8b54-134">Course tasks</span></span>
<span data-ttu-id="c8b54-135">U každého kurzu můžete provést následující úlohy.</span><span class="sxs-lookup"><span data-stu-id="c8b54-135">For each course, you can complete the following tasks.</span></span>
- <span data-ttu-id="c8b54-136">Registrovat účastníky</span><span class="sxs-lookup"><span data-stu-id="c8b54-136">Register participants</span></span>
- <span data-ttu-id="c8b54-137">Nastavit uzávěrku registrace</span><span class="sxs-lookup"><span data-stu-id="c8b54-137">Specify a registration deadline</span></span>
- <span data-ttu-id="c8b54-138">Definovat minimální a maximální počet účastníků</span><span class="sxs-lookup"><span data-stu-id="c8b54-138">Define the minimum and maximum number of participants</span></span>
- <span data-ttu-id="c8b54-139">Přiřadit místo konání kurzu a učebnu</span><span class="sxs-lookup"><span data-stu-id="c8b54-139">Assign a course location and classroom</span></span>
- <span data-ttu-id="c8b54-140">Doporučit hotely účastníkům kurzu</span><span class="sxs-lookup"><span data-stu-id="c8b54-140">Recommend hotels to course participants</span></span>
- <span data-ttu-id="c8b54-141">Vytvořit popis kurzu, který je poté možné zveřejnit na portálu Samoobsluha pro zaměstnance</span><span class="sxs-lookup"><span data-stu-id="c8b54-141">Create a course description, which you can then advertise on Employee self service</span></span>

  ><span data-ttu-id="c8b54-142">**Poznámka** Kurz lze odstranit pouze v případě, že do něj není nikdo zaregistrován.</span><span class="sxs-lookup"><span data-stu-id="c8b54-142">**Note** You can delete a course only if no one has registered for it.</span></span> 

## <a name="course-statuses"></a><span data-ttu-id="c8b54-143">Stavy kurzu</span><span class="sxs-lookup"><span data-stu-id="c8b54-143">Course statuses</span></span>
<span data-ttu-id="c8b54-144">V následující tabulce jsou uvedeny možné stavy kurzu a akce, které lze provádět, je-li kurz nachází ve specifickém stavu.</span><span class="sxs-lookup"><span data-stu-id="c8b54-144">The following table lists the possible course statuses and the actions that you can complete when the course has a specific status.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="c8b54-145">Stav</span><span class="sxs-lookup"><span data-stu-id="c8b54-145">Status</span></span></th>
<th><span data-ttu-id="c8b54-146">Akce</span><span class="sxs-lookup"><span data-stu-id="c8b54-146">Actions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c8b54-147"><strong>Vytvořeno</strong></span><span class="sxs-lookup"><span data-stu-id="c8b54-147"><strong>Created</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="c8b54-148">Zadávání a úprava informací o kurzu.</span><span class="sxs-lookup"><span data-stu-id="c8b54-148">Enter and modify course information.</span></span></li>
<li><span data-ttu-id="c8b54-149">Změňte stav kurzu na <strong>Otevřen</strong>, aby se pracovníci mohli do kurzu registrovat.</span><span class="sxs-lookup"><span data-stu-id="c8b54-149">Change the course status to <strong>Open</strong> so that workers can register for the course.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8b54-150"><strong>Otevřít</strong></span><span class="sxs-lookup"><span data-stu-id="c8b54-150"><strong>Open</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="c8b54-151">Zaregistrujte účastníky na kurz.</span><span class="sxs-lookup"><span data-stu-id="c8b54-151">Register participants for the course.</span></span></li>
<li><span data-ttu-id="c8b54-152">Odeberte účastníky z kurzu.</span><span class="sxs-lookup"><span data-stu-id="c8b54-152">Remove participants from the course.</span></span></li>
<li><span data-ttu-id="c8b54-153">Potvrďte účastníky kurzu.</span><span class="sxs-lookup"><span data-stu-id="c8b54-153">Confirm participants for the course.</span></span></li>
<li><span data-ttu-id="c8b54-154">Změňte stav kurzu na <strong>Uzavřeno</strong> nebo <strong>Zrušeno</strong>.</span><span class="sxs-lookup"><span data-stu-id="c8b54-154">Change the course status to <strong>Closed</strong> or <strong>Canceled</strong>.</span></span></li>
<li><span data-ttu-id="c8b54-155">Naplánujte dotazníky pro účastníky, jejichž stav je <strong>Potvrzeno</strong>.</span><span class="sxs-lookup"><span data-stu-id="c8b54-155">Plan questionnaires for participants whose status is <strong>Confirmed</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c8b54-156"><strong>Zavřeno</strong></span><span class="sxs-lookup"><span data-stu-id="c8b54-156"><strong>Closed</strong></span></span></td>
<td><span data-ttu-id="c8b54-157">Kurz můžete znovu otevřít.</span><span class="sxs-lookup"><span data-stu-id="c8b54-157">You can reopen the course.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c8b54-158"><strong>Zrušeno</strong></span><span class="sxs-lookup"><span data-stu-id="c8b54-158"><strong>Canceled</strong></span></span></td>
<td><span data-ttu-id="c8b54-159">Kurz můžete znovu otevřít.</span><span class="sxs-lookup"><span data-stu-id="c8b54-159">You can reopen the course.</span></span></td>
</tr>
</tbody>
</table>

## <a name="course-participants"></a><span data-ttu-id="c8b54-160">Účastníci kurzu</span><span class="sxs-lookup"><span data-stu-id="c8b54-160">Course participants</span></span>
<span data-ttu-id="c8b54-161">Účastníci kurzu jsou pracovníci, kteří se účastní školicího kurzu nebo události.</span><span class="sxs-lookup"><span data-stu-id="c8b54-161">Course participants are workers who participate in a training course or event.</span></span> <span data-ttu-id="c8b54-162">Účastníky můžete registrovat pouze pro otevřené kurzy.</span><span class="sxs-lookup"><span data-stu-id="c8b54-162">You can only register participants for open courses.</span></span> <span data-ttu-id="c8b54-163">Maximální a minimální počty účastníků, které lze do kurzu registrovat, jsou uvedeny na pevné záložce **Obecné** na stránce **Kurzy**.</span><span class="sxs-lookup"><span data-stu-id="c8b54-163">The minimum and maximum number of participants that you can register for a course is defined on the **General** FastTab on the **Courses** page.</span></span>

<a name="workflow"></a><span data-ttu-id="c8b54-164">Workflow</span><span class="sxs-lookup"><span data-stu-id="c8b54-164">Workflow</span></span>
--------

<span data-ttu-id="c8b54-165">Zaměstnancům, kteří se do kurzu zaregistrují na stránce **Samoobsluha pro zaměstnance**, může být registrace nasměrována do workflowu pro schválení.</span><span class="sxs-lookup"><span data-stu-id="c8b54-165">Employees who register for a course through the **Employee self service** page can have their registration routed through workflow for approval.</span></span> <span data-ttu-id="c8b54-166">Workflow lze přiřadit ke kurzu na pevné záložce **Obecné** na stránce **Kurzy**.</span><span class="sxs-lookup"><span data-stu-id="c8b54-166">You can assign a workflow to a course on the **General** FastTab on the **Courses** page.</span></span>





