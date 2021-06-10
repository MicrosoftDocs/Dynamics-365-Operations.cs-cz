---
title: Nakonfigurujte dovednosti
description: Můžete sledovat dovednosti svého pracovníka v Dynamics 365 Human Resources. Můžete také určit dovednosti, které jsou požadovány pro určitou práci.
author: andreabichsel
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmSkill, HcmSkillGapProfile, HcmSkillMapping, HcmSkillType, HcmEmployeeDevelopmentWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 3361
ms.assetid: c2ce94c0-933d-4edb-822c-7f0e7b49e4ee
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 816822d1f3d365b4c5571c13e9f596e1c5d5e59c
ms.sourcegitcommit: 48528233e0f02dbd47e96e030254ef65f2bb899e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/20/2021
ms.locfileid: "6076552"
---
# <a name="configure-skills"></a><span data-ttu-id="403dd-104">Nakonfigurujte dovednosti</span><span class="sxs-lookup"><span data-stu-id="403dd-104">Configure skills</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="403dd-105">Můžete sledovat dovednosti svého pracovníka v Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="403dd-105">You can track your worker's skills in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="403dd-106">Můžete také určit dovednosti, které jsou požadovány pro určitou práci.</span><span class="sxs-lookup"><span data-stu-id="403dd-106">You can also specify the skills that are required for a specific job.</span></span>

<span data-ttu-id="403dd-107">Zde jsou příklady dovedností, které lze sledovat:</span><span class="sxs-lookup"><span data-stu-id="403dd-107">Examples of skills you can track include:</span></span>

- <span data-ttu-id="403dd-108">Dozorčí - schopnost dohlížet na práci ostatních.</span><span class="sxs-lookup"><span data-stu-id="403dd-108">Supervisory – Ability to supervise the work of others.</span></span>
- <span data-ttu-id="403dd-109">Vůdčí - schopnost vést zaměstnance a obchodní domény.</span><span class="sxs-lookup"><span data-stu-id="403dd-109">Leadership – Ability to lead employees and business domains.</span></span>
- <span data-ttu-id="403dd-110">Plánování - schopnost dívat se dopředu, formulovat vize a schopnost tyto vize definovat.</span><span class="sxs-lookup"><span data-stu-id="403dd-110">Planning – Ability to look ahead, to form vision statements, and to see them through.</span></span>
- <span data-ttu-id="403dd-111">HTML – schopnost psát v kódu HTML.</span><span class="sxs-lookup"><span data-stu-id="403dd-111">HTML – Ability to write HTML code.</span></span>

<span data-ttu-id="403dd-112">Pokud jste ještě nenastavili typy dovedností a modely hodnocení, budete je muset před vytvořením dovedností přidat.</span><span class="sxs-lookup"><span data-stu-id="403dd-112">If you haven't already set up skill types and rating models, you'll need to add some before creating skills.</span></span>

<span data-ttu-id="403dd-113">Dovednosti pro pracovníka mohou zadat následující lidé:</span><span class="sxs-lookup"><span data-stu-id="403dd-113">The following people can enter skills for a worker:</span></span>

- <span data-ttu-id="403dd-114">Pracovníci mohou sami zadat dovednosti do samoobsluhy zaměstnanců.</span><span class="sxs-lookup"><span data-stu-id="403dd-114">Workers can enter skills for themselves in Employee self-service.</span></span> <span data-ttu-id="403dd-115">Tyto dovednosti vyžadují souhlas manažera.</span><span class="sxs-lookup"><span data-stu-id="403dd-115">These skills require manager approval.</span></span>
- <span data-ttu-id="403dd-116">Manažeři mohou zadat dovednosti pro své pracovníky.</span><span class="sxs-lookup"><span data-stu-id="403dd-116">Managers can enter skills for their workers.</span></span> <span data-ttu-id="403dd-117">Můžete vytvořit pracovní postup, který tyto dovednosti automaticky schválí.</span><span class="sxs-lookup"><span data-stu-id="403dd-117">You can create a workflow that auto-approves these skills.</span></span>

## <a name="create-a-skill-type"></a><span data-ttu-id="403dd-118">Vytvoření typu dovednosti</span><span class="sxs-lookup"><span data-stu-id="403dd-118">Create a skill type</span></span>

<span data-ttu-id="403dd-119">Typy dovedností jsou kategorie, do kterých jednotlivé dovednosti spadají, například administrativa nebo prodej.</span><span class="sxs-lookup"><span data-stu-id="403dd-119">Skill types are categories that individual skills fall under, such as Administration or Sales.</span></span>

1. <span data-ttu-id="403dd-120">V pracovním prostoru **Rozvoj zaměstnanců** vyberte **Odkazy**.</span><span class="sxs-lookup"><span data-stu-id="403dd-120">In the **Employee development** workspace, select **Links**.</span></span>

2. <span data-ttu-id="403dd-121">V **Nastavení kompetence** vyberte **Typy dovedností**.</span><span class="sxs-lookup"><span data-stu-id="403dd-121">Under **Competency setup**, select **Skill types**.</span></span>

3. <span data-ttu-id="403dd-122">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="403dd-122">Select **New**.</span></span>

4. <span data-ttu-id="403dd-123">Vyplňte následující pole:</span><span class="sxs-lookup"><span data-stu-id="403dd-123">Complete the following fields:</span></span>

   - <span data-ttu-id="403dd-124">**Typ dovednosti**: Zadejte název typu dovednosti.</span><span class="sxs-lookup"><span data-stu-id="403dd-124">**Skill type**: Enter a name for the skill type.</span></span>
   - <span data-ttu-id="403dd-125">**Popis**: Zadejte popis typu dovednosti.</span><span class="sxs-lookup"><span data-stu-id="403dd-125">**Description**: Enter a description for the skill type.</span></span>

5. <span data-ttu-id="403dd-126">Zvolte možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="403dd-126">Select **Save**.</span></span>

## <a name="create-a-rating-model"></a><span data-ttu-id="403dd-127">Vytvoření nového modelu hodnocení</span><span class="sxs-lookup"><span data-stu-id="403dd-127">Create a rating model</span></span>

<span data-ttu-id="403dd-128">Modely hodnocení pomáhají ve vyhodnocení skutečné úrovně dovedností osoby, úrovně, které mají dosáhnout, nebo úrovně dovednosti, která je požadována pro úlohu.</span><span class="sxs-lookup"><span data-stu-id="403dd-128">Rating models help evaluate a person's actual level of skill, the level they should work to achieve, or the level of skill required for a job.</span></span> <span data-ttu-id="403dd-129">Každé úrovni v modelu hodnocení je přiřazen koeficient.</span><span class="sxs-lookup"><span data-stu-id="403dd-129">Each level in a rating model is assigned a factor.</span></span>

1. <span data-ttu-id="403dd-130">V pracovním prostoru **Rozvoj zaměstnanců** vyberte **Odkazy**.</span><span class="sxs-lookup"><span data-stu-id="403dd-130">In the **Employee development** workspace, select **Links**.</span></span>

2. <span data-ttu-id="403dd-131">V **Nastavení kompetence** vyberte **Modely hodnocení**.</span><span class="sxs-lookup"><span data-stu-id="403dd-131">Under **Competency setup**, select **Rating models**.</span></span>

3. <span data-ttu-id="403dd-132">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="403dd-132">Select **New**.</span></span>

4. <span data-ttu-id="403dd-133">Vyplňte následující pole:</span><span class="sxs-lookup"><span data-stu-id="403dd-133">Complete the following fields:</span></span>

   - <span data-ttu-id="403dd-134">**Hodnocení**: Zadejte název modelu hodnocení, například **Dovednosti**.</span><span class="sxs-lookup"><span data-stu-id="403dd-134">**Rating**: Enter a name for the rating model, such as **Skills**.</span></span>
   - <span data-ttu-id="403dd-135">**Popis**: Zadejte popis modelu hodnocení, například **Hodnocení dovedností**.</span><span class="sxs-lookup"><span data-stu-id="403dd-135">**Description**: Enter a description for the rating model, such as **Skill ratings**.</span></span>

5. <span data-ttu-id="403dd-136">V sekci **Úrovně** vyberte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="403dd-136">In the **Levels** section, select **New**.</span></span> <span data-ttu-id="403dd-137">Pro každou úroveň, kterou chcete přidat, vyplňte následující pole:</span><span class="sxs-lookup"><span data-stu-id="403dd-137">For each level you want to add, complete the following fields:</span></span>

   - <span data-ttu-id="403dd-138">**Ǔroveň**: Zadejte název úrovně.</span><span class="sxs-lookup"><span data-stu-id="403dd-138">**Level**: Enter a name for the level.</span></span>
   - <span data-ttu-id="403dd-139">**Popis**: Zadejte popis úrovně.</span><span class="sxs-lookup"><span data-stu-id="403dd-139">**Description**: Enter a description for the level.</span></span>
   - <span data-ttu-id="403dd-140">**Faktor**: Zadejte hodnotu faktoru od 0-9.</span><span class="sxs-lookup"><span data-stu-id="403dd-140">**Factor**: Enter a factor value from 0-9.</span></span> <span data-ttu-id="403dd-141">Faktor pomáhá normalizovat výsledky dovedností, které používají různé modely hodnocení.</span><span class="sxs-lookup"><span data-stu-id="403dd-141">Factors help normalize the scores of skills that use different rating models.</span></span> <span data-ttu-id="403dd-142">Každá úroveň musí mít jedinečný faktor.</span><span class="sxs-lookup"><span data-stu-id="403dd-142">Each level must have a unique factor.</span></span> <span data-ttu-id="403dd-143">Úrovně s vyšší hodnotou koeficientu nesou v modelu hodnocení větší váhu.</span><span class="sxs-lookup"><span data-stu-id="403dd-143">Levels with higher factor values carry more weight in a rating model.</span></span>

   <span data-ttu-id="403dd-144">Podle potřeby pokračujte v přidávání úrovní.</span><span class="sxs-lookup"><span data-stu-id="403dd-144">Continue adding levels as necessary.</span></span> <span data-ttu-id="403dd-145">Můžete zadat až 10 úrovní pro každý model hodnocení.</span><span class="sxs-lookup"><span data-stu-id="403dd-145">You can enter up to 10 levels for each rating model.</span></span>

6. <span data-ttu-id="403dd-146">Zvolte možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="403dd-146">Select **Save**.</span></span>

## <a name="create-a-skill"></a><span data-ttu-id="403dd-147">Vytvoření dovednosti</span><span class="sxs-lookup"><span data-stu-id="403dd-147">Create a skill</span></span>

<span data-ttu-id="403dd-148">Před přiřazením dovednosti nebo vytvořením vyhledávání s mapováním dovedností nebo vytvořením profilu dovedností je nutné zadat informace o dovednostech na stránce **Dovednosti**.</span><span class="sxs-lookup"><span data-stu-id="403dd-148">Before you can assign a skill, or create a skill-mapping search or skill profile, you must enter information about the skills on the **Skills** page.</span></span> <span data-ttu-id="403dd-149">Pro každou dovednost můžete vybrat typ dovednosti a model hodnocení.</span><span class="sxs-lookup"><span data-stu-id="403dd-149">For each skill, you can select a skill type and a rating model.</span></span>

1. <span data-ttu-id="403dd-150">V pracovním prostoru **Rozvoj zaměstnanců** vyberte **Odkazy**.</span><span class="sxs-lookup"><span data-stu-id="403dd-150">In the **Employee development** workspace, select **Links**.</span></span>

2. <span data-ttu-id="403dd-151">V **Nastavení kompetence** vyberte **Dovednosti**.</span><span class="sxs-lookup"><span data-stu-id="403dd-151">Under **Competency setup**, select **Skills**.</span></span>

3. <span data-ttu-id="403dd-152">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="403dd-152">Select **New**.</span></span>

4. <span data-ttu-id="403dd-153">Vyplňte následující pole:</span><span class="sxs-lookup"><span data-stu-id="403dd-153">Complete the following fields:</span></span>

   - <span data-ttu-id="403dd-154">**Dovednost**: Zadejte název typu dovednosti.</span><span class="sxs-lookup"><span data-stu-id="403dd-154">**Skill**: Enter a name for the skill.</span></span>
   - <span data-ttu-id="403dd-155">**Popis**: Zadejte popis dovednosti.</span><span class="sxs-lookup"><span data-stu-id="403dd-155">**Description**: Enter a description for the skill.</span></span>
   - <span data-ttu-id="403dd-156">**Hodnocení**: Vyberte model hodnocení, který chcete pro tuto dovednost použít.</span><span class="sxs-lookup"><span data-stu-id="403dd-156">**Rating**: Select the rating model you want to use for this skill.</span></span>
   - <span data-ttu-id="403dd-157">**Typ dovednosti**: Vyberte ze seznamu typů dovedností.</span><span class="sxs-lookup"><span data-stu-id="403dd-157">**Skill type**: Select from the list of skill types.</span></span>

5. <span data-ttu-id="403dd-158">Zvolte možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="403dd-158">Select **Save**.</span></span>

## <a name="see-also"></a><span data-ttu-id="403dd-159">Viz také</span><span class="sxs-lookup"><span data-stu-id="403dd-159">See also</span></span>

[<span data-ttu-id="403dd-160">Zadejte dovednosti</span><span class="sxs-lookup"><span data-stu-id="403dd-160">Enter skills</span></span>](hr-develop-enter-skills.md)<br>
[<span data-ttu-id="403dd-161">Mapové dovednosti</span><span class="sxs-lookup"><span data-stu-id="403dd-161">Map skills</span></span>](hr-develop-map-skills.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]