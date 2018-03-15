---
title: "Distribuce a vyplnění dotazníku"
description: "Toto téma vysvětluje, jak distribuovat dotazníky, které navrhnete, aby byly k dispozici osobě nebo skupině osob, které je mají vyplnit."
author: kherr75
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: KMConnectionType, KMKnowledgeCollectorPlanningTabel, SysEmailParameters
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 17424
ms.assetid: fd8d867a-2446-400a-b91f-ad4085427470
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 3954ec2a06c7a2ec964b656e088f8c677094c963
ms.contentlocale: cs-cz
ms.lasthandoff: 02/07/2018

---

# <a name="distribute-and-complete-a-questionnaire"></a><span data-ttu-id="e93ee-103">Distribuce a vyplnění dotazníku</span><span class="sxs-lookup"><span data-stu-id="e93ee-103">Distribute and complete a questionnaire</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="e93ee-104">Toto téma vysvětluje, jak distribuovat dotazníky, které navrhnete, aby byly k dispozici osobě nebo skupině osob, které je mají vyplnit.</span><span class="sxs-lookup"><span data-stu-id="e93ee-104">This topic explains how distribute the questionnaires that you design, so that they are available to the person or group of people who will complete them.</span></span> 

<span data-ttu-id="e93ee-105">Existuje několik způsobů distribuce dotazníků:</span><span class="sxs-lookup"><span data-stu-id="e93ee-105">There are multiple ways to distribute a questionnaire:</span></span>

-   <span data-ttu-id="e93ee-106">Nastavte dotazník jako aktivní.</span><span class="sxs-lookup"><span data-stu-id="e93ee-106">Mark the questionnaire as active.</span></span> <span data-ttu-id="e93ee-107">Dotazník bude poté dostupný všem zaměstnancům, potom není skupina dotazníku nastavena na omezení přístupu k ní.</span><span class="sxs-lookup"><span data-stu-id="e93ee-107">The questionnaire is then available to all employees, unless a questionnaire group is set up to restrict access to it.</span></span>
-   <span data-ttu-id="e93ee-108">Přiřaďte práva ke skupině dotazníku.</span><span class="sxs-lookup"><span data-stu-id="e93ee-108">Assign rights to a questionnaire group.</span></span> <span data-ttu-id="e93ee-109">Dotazník bude poté dostupný všem členům vybrané skupiny.</span><span class="sxs-lookup"><span data-stu-id="e93ee-109">The questionnaire is then available to all members of the selected group.</span></span>
-   <span data-ttu-id="e93ee-110">Vytvořte plánované relace odpovědí.</span><span class="sxs-lookup"><span data-stu-id="e93ee-110">Create planned answer sessions.</span></span> <span data-ttu-id="e93ee-111">Dotazník bude poté dostupný pouze vybrané osobě.</span><span class="sxs-lookup"><span data-stu-id="e93ee-111">The questionnaire is then available only to a particular person.</span></span>
-   <span data-ttu-id="e93ee-112">Vytvořte plán.</span><span class="sxs-lookup"><span data-stu-id="e93ee-112">Create a schedule.</span></span> <span data-ttu-id="e93ee-113">Dotazník bude poté k dispozici více osobám.</span><span class="sxs-lookup"><span data-stu-id="e93ee-113">The questionnaire can then be available to multiple people.</span></span>

## <a name="marking-a-questionnaire-as-active"></a><span data-ttu-id="e93ee-114">Nastavení dotazníku jako aktivního</span><span class="sxs-lookup"><span data-stu-id="e93ee-114">Marking a questionnaire as active</span></span>
<span data-ttu-id="e93ee-115">Nastavením pole **Aktivní** na možnost **Ano** na stránce **Dotazníky** bude dotazník dostupný pro všechny zaměstnance k vyplnění.</span><span class="sxs-lookup"><span data-stu-id="e93ee-115">By setting the **Active** field to **Yes** on the **Questionnaires** page, you make the questionnaire available for all employees to complete.</span></span> <span data-ttu-id="e93ee-116">Respondenti mohou vyplnit dotazník více než jednou.</span><span class="sxs-lookup"><span data-stu-id="e93ee-116">Respondents can complete the questionnaire multiple times.</span></span> <span data-ttu-id="e93ee-117">Tato funkce je užitečná, pokud chcete získávat průběžnou zpětnou vazbu v průběhu roku.</span><span class="sxs-lookup"><span data-stu-id="e93ee-117">This functionality is useful if you want to gather continual feedback throughout the year.</span></span> <span data-ttu-id="e93ee-118">Například lze vytvořit dotazník, který zaměstnanci používají k poskytnutí zpětné vazby na obědy v kantýně.</span><span class="sxs-lookup"><span data-stu-id="e93ee-118">For example, you can make a questionnaire that employees use to give feedback about the lunch service in the cafeteria.</span></span>

## <a name="questionnaire-groups"></a><span data-ttu-id="e93ee-119">Skupiny dotazníků</span><span class="sxs-lookup"><span data-stu-id="e93ee-119">Questionnaire groups</span></span>
<span data-ttu-id="e93ee-120">Můžete nastavit skupiny dotazníků a poté zahrnout respondenty, kterým má být dotazník distribuován.</span><span class="sxs-lookup"><span data-stu-id="e93ee-120">You can set up questionnaire groups and then include the respondents that a questionnaire should be distributed to.</span></span> 

<span data-ttu-id="e93ee-121">Můžete vytvářet skupiny dotazníků z následujících stránek:</span><span class="sxs-lookup"><span data-stu-id="e93ee-121">You can create questionnaire groups from the following pages:</span></span>

-   <span data-ttu-id="e93ee-122">**Skupiny dotazníků**– Pouze jednotlivci ve skupině dotazníků mohou vyplnit vybraný dotazník.</span><span class="sxs-lookup"><span data-stu-id="e93ee-122">**Questionnaire groups** – Only individuals in a questionnaire group can complete a selected questionnaire.</span></span> <span data-ttu-id="e93ee-123">Například vaše cílová skupina jsou dodavatelé, takže můžete vytvořit skupinu dotazníků specifickou pro tyto respondenty.</span><span class="sxs-lookup"><span data-stu-id="e93ee-123">For example, your intended audience is contractors, so you create a questionnaire group that is specific to those respondents.</span></span>
-   <span data-ttu-id="e93ee-124">**Členové skupiny dotazníků** – Do skupiny dotazníků lze přidat osoby.</span><span class="sxs-lookup"><span data-stu-id="e93ee-124">**Questionnaire group members** – You can add people to the questionnaire groups.</span></span>

<span data-ttu-id="e93ee-125">Chcete-li přiřadit skupinu dotazníků k dotazníku, na stránce **Dotazníky** klikněte na možnost **Uživatelská práva**.</span><span class="sxs-lookup"><span data-stu-id="e93ee-125">To assign a questionnaire group to a questionnaire, on the **Questionnaires** page, click **User rights**.</span></span> <span data-ttu-id="e93ee-126">Po uložení dotazníku jako aktivního mohou členové skupiny dotazníků vyplnit dotazník.</span><span class="sxs-lookup"><span data-stu-id="e93ee-126">After the questionnaire is saved as active, the members of the questionnaire group can complete the questionnaire.</span></span> <span data-ttu-id="e93ee-127">Tato funkce je užitečná, pokud chcete otestovat dotazník ve vybrané skupině osob, než jej předáte větší skupině, nebo pokud chcete zaměřit dotazník na velmi specifickou cílovou skupinu.</span><span class="sxs-lookup"><span data-stu-id="e93ee-127">This functionality is helpful if you want to test a questionnaire on a select group of people before you roll it out to a larger group, or if you want to target a questionnaire to a very specific audience.</span></span>

## <a name="planned-answer-sessions-in-a-questionnaire"></a><span data-ttu-id="e93ee-128">Plánované relace odpovědí v dotazníku</span><span class="sxs-lookup"><span data-stu-id="e93ee-128">Planned answer sessions in a questionnaire</span></span>
<span data-ttu-id="e93ee-129">Plánované relace odpovědí jsou dotazníky, pro které jste navrhli a vybrali respondenty.</span><span class="sxs-lookup"><span data-stu-id="e93ee-129">Planned answer sessions are questionnaires that you've designed and selected the respondents for.</span></span> 

> <span data-ttu-id="e93ee-130">**Poznámka:** Než nastavíte plánované relace odpovědí, je nutné navrhnout dotazník.</span><span class="sxs-lookup"><span data-stu-id="e93ee-130">**Note** Before you can set up planned answer sessions, you must design a questionnaire.</span></span> 

<span data-ttu-id="e93ee-131">Na stránce **Plánovaná relace odpovědí** můžete vytvořit plánovanou relaci odpovědí pro jednotlivé zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="e93ee-131">On the **Planned answer session** page, you can create a planned answer session for an individual employee.</span></span> <span data-ttu-id="e93ee-132">V seznamu na stránce jsou zobrazeny všechny plánované dotazníky.</span><span class="sxs-lookup"><span data-stu-id="e93ee-132">The list on the page displays all planned questionnaires.</span></span> 

<span data-ttu-id="e93ee-133">Plánované relace odpovědí se rovněž použijí na stránce **Plány dotazníků**, kde je možné naplánovat dotazníky pro více osob:</span><span class="sxs-lookup"><span data-stu-id="e93ee-133">Planned answer sessions are also used on the **Questionnaire schedules** page, where you can plan questionnaires for multiple people:</span></span>

-   <span data-ttu-id="e93ee-134">Zaměstnanci</span><span class="sxs-lookup"><span data-stu-id="e93ee-134">Employees</span></span>
-   <span data-ttu-id="e93ee-135">Účastníci kurzu</span><span class="sxs-lookup"><span data-stu-id="e93ee-135">Course participants</span></span>
-   <span data-ttu-id="e93ee-136">Organizační jednotky</span><span class="sxs-lookup"><span data-stu-id="e93ee-136">Organizational units</span></span>

<span data-ttu-id="e93ee-137">Každá osoba může odpovídat na dotazník pouze jednou.</span><span class="sxs-lookup"><span data-stu-id="e93ee-137">Each person can answer the questionnaire only one time.</span></span>

## <a name="scheduling-a-questionnaire"></a><span data-ttu-id="e93ee-138">Plánování dotazníku</span><span class="sxs-lookup"><span data-stu-id="e93ee-138">Scheduling a questionnaire</span></span>
<span data-ttu-id="e93ee-139">Volitelně můžete naplánovat dotazník pro více respondentů.</span><span class="sxs-lookup"><span data-stu-id="e93ee-139">You can optionally schedule a questionnaire for multiple respondents.</span></span>

### <a name="planning-types"></a><span data-ttu-id="e93ee-140">Typy plánování</span><span class="sxs-lookup"><span data-stu-id="e93ee-140">Planning types</span></span>

<span data-ttu-id="e93ee-141">Typy plánů jsou požadovány, pokud chcete plánovat plánované relace odpovědí pro více respondentů.</span><span class="sxs-lookup"><span data-stu-id="e93ee-141">Planning types are required if you want to schedule planned answer sessions for multiple respondents.</span></span> <span data-ttu-id="e93ee-142">Typy plánů slouží ke klasifikaci plánů dotazníků.</span><span class="sxs-lookup"><span data-stu-id="e93ee-142">Planning types are used to classify questionnaire schedules.</span></span> <span data-ttu-id="e93ee-143">Můžete například naplánovat dotazníky pro následující účely:</span><span class="sxs-lookup"><span data-stu-id="e93ee-143">For example, you can schedule questionnaires for the following purposes:</span></span>

-   <span data-ttu-id="e93ee-144">Hodnocení</span><span class="sxs-lookup"><span data-stu-id="e93ee-144">Evaluation</span></span>
-   <span data-ttu-id="e93ee-145">Průzkum</span><span class="sxs-lookup"><span data-stu-id="e93ee-145">Survey</span></span>
-   <span data-ttu-id="e93ee-146">Testování</span><span class="sxs-lookup"><span data-stu-id="e93ee-146">Testing</span></span>

<span data-ttu-id="e93ee-147">Typy plánování dotazníku pro plán dotazníku je možné určit na stránce **Plány dotazníků**.</span><span class="sxs-lookup"><span data-stu-id="e93ee-147">You can specify planning types for a questionnaire schedule on the **Questionnaire schedules** page.</span></span>

### <a name="reference-types-for-questionnaire"></a><span data-ttu-id="e93ee-148">Typy odkazů pro dotazník</span><span class="sxs-lookup"><span data-stu-id="e93ee-148">Reference types for questionnaire</span></span>

<span data-ttu-id="e93ee-149">Typy odkazů slouží k zadání kritérií pro respondenty, které můžete vybrat při plánování dotazníku.</span><span class="sxs-lookup"><span data-stu-id="e93ee-149">You can use reference types to enter criteria for the respondents that you might select when you schedule a questionnaire.</span></span> 

<span data-ttu-id="e93ee-150">Stránku **Typy odkazů** lze použít k nastavení typů odkazů pro dotazník.</span><span class="sxs-lookup"><span data-stu-id="e93ee-150">Use the **Reference types** page to set up reference types for a questionnaire.</span></span> <span data-ttu-id="e93ee-151">Každý typ odkazu odpovídá tabulce v aplikaci Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e93ee-151">Each reference type corresponds to a table in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="e93ee-152">Když vytváříte plány dotazníků, můžete zadat jednotlivé záznamy do tabulky nebo vybrané záznamy, ke kterým bude dotazník přiřazen.</span><span class="sxs-lookup"><span data-stu-id="e93ee-152">When you create questionnaire schedules, you can specify individual records in the table or a range of records that the questionnaire will be associated with.</span></span> 

<span data-ttu-id="e93ee-153">Například pokud vyberete tabulku Kurzy, můžete se rozhodnout, kterých konkrétních kurzů se bude dotazník týkat.</span><span class="sxs-lookup"><span data-stu-id="e93ee-153">For example, if you select the Courses table, you can decide which specific course the questionnaire will be for.</span></span> <span data-ttu-id="e93ee-154">Při nastavování odkaz pro tabulku kurzů budou k dispozici některá pole a tlačítka na stránce **Kurzy**.</span><span class="sxs-lookup"><span data-stu-id="e93ee-154">When you set up a reference for the Courses table, some fields and buttons on the **Courses** page become available.</span></span>

### <a name="questionnaire-schedules"></a><span data-ttu-id="e93ee-155">Plány dotazníků</span><span class="sxs-lookup"><span data-stu-id="e93ee-155">Questionnaire schedules</span></span>

<span data-ttu-id="e93ee-156">Plány dotazníků slouží ke generování několika plánovaných relací odpovědí pro skupinu uživatelů, podle typu odkazu.</span><span class="sxs-lookup"><span data-stu-id="e93ee-156">You can use questionnaire schedules to generate multiple planned answer sessions for a group of users, based on a reference type.</span></span> <span data-ttu-id="e93ee-157">Vytvořte plán na stránce **Plány dotazníků**.</span><span class="sxs-lookup"><span data-stu-id="e93ee-157">Create a schedule on the **Questionnaire schedules** page.</span></span> <span data-ttu-id="e93ee-158">Vyberte typ plánování pro kategorizaci plánu a také vyberte typ odkazu, který má být použit pro dotaz na systém pro konkrétní uživatele.</span><span class="sxs-lookup"><span data-stu-id="e93ee-158">Select the planning type to categorize the schedule, and also select the reference type that should be used to query the system for specific users.</span></span> <span data-ttu-id="e93ee-159">Například při nastavení typu odkazu na tabulku kurzů můžete vybrat konkrétní kurz v poli **Odkaz**.</span><span class="sxs-lookup"><span data-stu-id="e93ee-159">For example, if you set the reference type to the Courses table, you can select a specific course in the **Reference** field.</span></span> 

<span data-ttu-id="e93ee-160">Kliknutím na tlačítko **Podrobnosti nastavení** vyberte dotazník a další kritéria.</span><span class="sxs-lookup"><span data-stu-id="e93ee-160">Click **Setup details** to select the questionnaire and other criteria.</span></span> <span data-ttu-id="e93ee-161">Například pokud dotazník slouží k hodnocení instruktora, zadejte jako kritérium jméno instruktora.</span><span class="sxs-lookup"><span data-stu-id="e93ee-161">For example, specify the instructor's name as a criterion if the questionnaire is an evaluation of the instructor.</span></span> <span data-ttu-id="e93ee-162">Po zadání podrobností nastavení systém vygeneruje plánované relace odpovědí pro uživatele, kteří jsou zahrnuty do dotazu.</span><span class="sxs-lookup"><span data-stu-id="e93ee-162">After you've finished entering the setup details, the system generates planned answer sessions for the users that are included in the query.</span></span> 

<span data-ttu-id="e93ee-163">Kliknutím na tlačítko **Plánované relace odpovědí** zobrazíte relace odpovědí pro plán.</span><span class="sxs-lookup"><span data-stu-id="e93ee-163">Click **Planned answer sessions** to view the answer sessions for the schedule.</span></span> <span data-ttu-id="e93ee-164">Můžete pak ručně vytvořit další plánované relace odpovědí nebo odstranit plánované relace odpovědí, které zodpovězeny nebyly.</span><span class="sxs-lookup"><span data-stu-id="e93ee-164">You can then manually create additional planned answer sessions or delete planned answer sessions that haven't been answered.</span></span> 

<span data-ttu-id="e93ee-165">Klikněte na tlačítko **Funkce** &gt; **Spustit**, chcete-li dotazník zpřístupnit pro uživatele v souvisejících plánovaných relacích odpovědí.</span><span class="sxs-lookup"><span data-stu-id="e93ee-165">Click **Functions** &gt; **Start** to make the questionnaire available to the users in related planned answer sessions.</span></span> <span data-ttu-id="e93ee-166">Kliknutím na tlačítko **Odpovědi** zobrazíte dokončené odpovědi v dotazníku.</span><span class="sxs-lookup"><span data-stu-id="e93ee-166">Click **Answers** to view the completed responses to the questionnaire.</span></span> <span data-ttu-id="e93ee-167">Volitelně můžete zkopírovat nastavení plánu dotazníku, plánované relace odpovědí a odpovědi na nový plán dotazníku.</span><span class="sxs-lookup"><span data-stu-id="e93ee-167">You can optionally copy the questionnaire schedule settings, planned answer sessions, and answers to a new questionnaire schedule.</span></span>

## <a name="notifying-respondents-about-questionnaires-that-are-available-to-them"></a><span data-ttu-id="e93ee-168">Oznámení dostupnosti dotazníků pro respondenty</span><span class="sxs-lookup"><span data-stu-id="e93ee-168">Notifying respondents about questionnaires that are available to them</span></span>
<span data-ttu-id="e93ee-169">Při distribuci dotazníku musíte respondenty informovat, že je dotazník k dispozici.</span><span class="sxs-lookup"><span data-stu-id="e93ee-169">When you distribute a questionnaire, you must notify respondents that questionnaires are available to them.</span></span> 

### <a name="notifying-respondents-about-a-planned-answer-session"></a><span data-ttu-id="e93ee-170">Informování respondentů o plánované relaci odpovědí</span><span class="sxs-lookup"><span data-stu-id="e93ee-170">Notifying respondents about a planned answer session</span></span>

<span data-ttu-id="e93ee-171">Pokud používáte plánovou relaci odpovědí, je nutné to dané osobě oznámit přímo, například telefonicky nebo e-mailem.</span><span class="sxs-lookup"><span data-stu-id="e93ee-171">If you use a planned answer session, you must notify the person directly, such as by telephone or email.</span></span>

### <a name="notifying-respondents-about-a-scheduling"></a><span data-ttu-id="e93ee-172">Oznámení plánování respondentům</span><span class="sxs-lookup"><span data-stu-id="e93ee-172">Notifying respondents about a scheduling</span></span>

<span data-ttu-id="e93ee-173">Na stránce **Plány dotazníků** lze připravit a odeslat e-mail všem respondentům přiřazeným k dotazníku.</span><span class="sxs-lookup"><span data-stu-id="e93ee-173">Use the **Questionnaire schedules** page to prepare and send email to all respondents who are assigned to the questionnaire.</span></span> <span data-ttu-id="e93ee-174">Zadejte text e-mailu na kartě **E-mail pro samoobsluhu pro zaměstnance** kartu. Po spuštění plánu klikněte na **Funkce** &gt; **Odeslat e-mail** pro vygenerování a odeslání e-mailu respondentům.</span><span class="sxs-lookup"><span data-stu-id="e93ee-174">Enter the email text on the **E-mail for employee self service** tab. After the schedule has been started, click **Functions** &gt; **Send e-mail** to generate and send the email to the respondents.</span></span> <span data-ttu-id="e93ee-175">Respondenti se pak mohou přihlásit na webové stránce a vyplnit dotazník.</span><span class="sxs-lookup"><span data-stu-id="e93ee-175">Respondents can then sign in to the website and complete the questionnaire.</span></span> 

> <span data-ttu-id="e93ee-176">**Poznámka:** Před použitím funkce e-mailu musí správce IT zadat nastavení e-mailu na stránce **Parametry e-mailu**.</span><span class="sxs-lookup"><span data-stu-id="e93ee-176">**Note** Before you can use the email functionality, your IT administrator must enter the email settings on the **E-mail parameters** page.</span></span>

## <a name="ending-a-scheduled-questionnaire"></a><span data-ttu-id="e93ee-177">Ukončení plánovaného dotazníku</span><span class="sxs-lookup"><span data-stu-id="e93ee-177">Ending a scheduled questionnaire</span></span>
<span data-ttu-id="e93ee-178">Plánovaný dotazník lze ukončit, jakmile všichni respondenti vyplní jim přiřazené relace odpovědí.</span><span class="sxs-lookup"><span data-stu-id="e93ee-178">You can end a scheduled questionnaire after all respondents have completed their assigned answer sessions.</span></span> <span data-ttu-id="e93ee-179">Po ukončení plánovaného dotazníku není možné zkopírovat jeho nastavení do nového plánu.</span><span class="sxs-lookup"><span data-stu-id="e93ee-179">After a scheduled questionnaire is ended, you can't copy its settings to a new schedule.</span></span> 

> <span data-ttu-id="e93ee-180">**Poznámka:** Pokud některý z respondentů nevyplnil dotazník a přesto chcete ukončit plánování, odstraňte nejprve příslušné respondenty ze seznamu na stránce **Plánovaná relace odpovědí**.</span><span class="sxs-lookup"><span data-stu-id="e93ee-180">**Note** If one or more respondents haven't completed the questionnaire, but you still want to end the scheduling, you must first delete those respondents from the list on the **Planned answer session** page.</span></span> <span data-ttu-id="e93ee-181">Poté můžete ukončit plánování.</span><span class="sxs-lookup"><span data-stu-id="e93ee-181">You can then end the schedule.</span></span>

## <a name="completing-questionnaires"></a><span data-ttu-id="e93ee-182">Vyplňování dotazníků</span><span class="sxs-lookup"><span data-stu-id="e93ee-182">Completing questionnaires</span></span>
<span data-ttu-id="e93ee-183">Po návrhu a distribuci dotazníku mohou vybraní respondenti dotazník vyplnit.</span><span class="sxs-lookup"><span data-stu-id="e93ee-183">After you've designed and distributed a questionnaire, the questionnaire can be completed by selected respondents.</span></span> <span data-ttu-id="e93ee-184">Dotazníky, které máte k dispozici, můžete vyplnit ze dvou míst:</span><span class="sxs-lookup"><span data-stu-id="e93ee-184">You can complete the questionnaires that are available to you from two locations:</span></span>

-   <span data-ttu-id="e93ee-185">V navigačním podokně klikněte na možnost **Dotazníky** &gt; **Distribuovat** &gt; **Vyplnit dotazník**.</span><span class="sxs-lookup"><span data-stu-id="e93ee-185">In the navigation pane, click **Questionnaires** &gt; **Distribute** &gt; **Complete a questionnaire**.</span></span>
-   <span data-ttu-id="e93ee-186">V samoobsluze pro zaměstnance klikněte na tlačítko **Dotazníky k vyplnění**.</span><span class="sxs-lookup"><span data-stu-id="e93ee-186">In Employee self-service, click **Questionnaires to complete**.</span></span>

<span data-ttu-id="e93ee-187">Dotazníky lze zpřístupnit pro určité uživatele, skupiny uživatelů nebo všechny uživatele na síti.</span><span class="sxs-lookup"><span data-stu-id="e93ee-187">Questionnaires can made be available to specific users or groups of users, or to all users in a network.</span></span>

<a name="see-also"></a><span data-ttu-id="e93ee-188">Viz také</span><span class="sxs-lookup"><span data-stu-id="e93ee-188">See also</span></span>
--------

[<span data-ttu-id="e93ee-189">Vytváření dotazníků</span><span class="sxs-lookup"><span data-stu-id="e93ee-189">Designing questionnaires</span></span>](design-questionnaires.md)

[<span data-ttu-id="e93ee-190">Používání dotazníků</span><span class="sxs-lookup"><span data-stu-id="e93ee-190">Using questionnaires</span></span>](questionnaires.md)

[<span data-ttu-id="e93ee-191">Zobrazení a zhodnocení výsledků dotazníků</span><span class="sxs-lookup"><span data-stu-id="e93ee-191">Viewing and evaluating the results of questionnaires</span></span>](evaluate-questionnaire-results.md)



