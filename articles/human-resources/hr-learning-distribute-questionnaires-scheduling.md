---
title: Distribuce dotazníků s použitím plánování
description: Plánování dotazníků umožňuje plánovat a rozdělovat dotazníky mezi více respondentů.
author: andreabichsel
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KMKnowledgeCollectorPlanningTable, KMKnowledgeCollectorPlanningMulti, SysQueryForm, HcmPersonLookup, KMKnowledgeCollectorPlanning, HcmLearningWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 952048ce0a2ac94be70d7bde0dc52610f19151ed
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056293"
---
# <a name="distribute-questionnaires-using-scheduling"></a><span data-ttu-id="d271e-103">Distribuce dotazníků s použitím plánování</span><span class="sxs-lookup"><span data-stu-id="d271e-103">Distribute questionnaires using scheduling</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="d271e-104">Plánování dotazníků umožňuje plánovat a rozdělovat dotazníky mezi více respondentů.</span><span class="sxs-lookup"><span data-stu-id="d271e-104">Questionnaire scheduling allows you to plan and distribute questionnaires to multiple respondents.</span></span> <span data-ttu-id="d271e-105">K vytvoření tohoto postupu jsou použita ukázková data společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="d271e-105">The demo data company used to create this procedure is USMF.</span></span>

## <a name="create-a-questionnaire-schedule"></a><span data-ttu-id="d271e-106">Vytvořte plán dotazníku</span><span class="sxs-lookup"><span data-stu-id="d271e-106">Create a questionnaire schedule</span></span>

1. <span data-ttu-id="d271e-107">Přejděte na Dotazník > Distribuovat > Plány dotazníků.</span><span class="sxs-lookup"><span data-stu-id="d271e-107">Go to Questionnaire > Distribute > Questionnaire schedules.</span></span>

2. <span data-ttu-id="d271e-108">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="d271e-108">Click New.</span></span>

3. <span data-ttu-id="d271e-109">Zadejte hodnotu do pole Plánování.</span><span class="sxs-lookup"><span data-stu-id="d271e-109">In the Scheduling field, type a value.</span></span>

4. <span data-ttu-id="d271e-110">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="d271e-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="d271e-111">Nastavte plán pro anonymní v případě, že odpověď by měla být zaznamenána bez jmen přiřazených k odpovědi.</span><span class="sxs-lookup"><span data-stu-id="d271e-111">Set the schedule to Anonymous if the responses should be recorded without names associated to the response.</span></span>  
    * <span data-ttu-id="d271e-112">Povolení anonymních výsledků musí být v parametrech HR nejprve nastaveno.</span><span class="sxs-lookup"><span data-stu-id="d271e-112">Allowing anonymous results must be set up in the HR parameters first.</span></span>  

5. <span data-ttu-id="d271e-113">V poli Typ vyberte typ plánování.</span><span class="sxs-lookup"><span data-stu-id="d271e-113">In the Type field, select the planning type.</span></span>  <span data-ttu-id="d271e-114">V tomto příkladu použijeme typ Spokojenost.</span><span class="sxs-lookup"><span data-stu-id="d271e-114">In this example we will use the Satisfaction type.</span></span>

6. <span data-ttu-id="d271e-115">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="d271e-115">In the list, find and select the desired record.</span></span>

7. <span data-ttu-id="d271e-116">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="d271e-116">In the list, click the link in the selected row.</span></span>

8. <span data-ttu-id="d271e-117">Do pole Datum zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="d271e-117">In the Date field, enter a date.</span></span>

9. <span data-ttu-id="d271e-118">Rozbalte oddíl E-mail pro samoobsluhu pro zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="d271e-118">Expand the Email for employee self service section.</span></span>

10. <span data-ttu-id="d271e-119">Zadejte hodnotu do pole Předmět.</span><span class="sxs-lookup"><span data-stu-id="d271e-119">In the Subject field, type a value.</span></span>

    * <span data-ttu-id="d271e-120">Příklad: Dotazník k dispozici</span><span class="sxs-lookup"><span data-stu-id="d271e-120">Example: Questionnaire available</span></span>  

11. <span data-ttu-id="d271e-121">Do pole Text zadejte text e-mailové zprávy.</span><span class="sxs-lookup"><span data-stu-id="d271e-121">In the Text field, type the body of your email message.</span></span> <span data-ttu-id="d271e-122">Všimněte si, že proměnná slouží k nahrazení hodnot v systému.</span><span class="sxs-lookup"><span data-stu-id="d271e-122">Note, the variable can be used to substitue values in the system.</span></span>

    * <span data-ttu-id="d271e-123">Příklad: Vážený/á %P%, přihlaste se prosím do Samoobsluhy pro zaměstnance a vyplňte dotazník zdraví pracovníků.</span><span class="sxs-lookup"><span data-stu-id="d271e-123">Example: Dear %P%, Please log in to Employee Self Service to complete the Workforce Health questionnaire.</span></span>  <span data-ttu-id="d271e-124">Contoso</span><span class="sxs-lookup"><span data-stu-id="d271e-124">Contoso</span></span>  

12. <span data-ttu-id="d271e-125">Klikněte na tlačítko Uložit.</span><span class="sxs-lookup"><span data-stu-id="d271e-125">Click Save.</span></span>

## <a name="use-the-setup-details-to-select-the-questionnaires-to-be-answered-as-well-as-any-queries-to-use-to-select-respondents"></a><span data-ttu-id="d271e-126">Použijte Podrobnosti nastavení pro výběr dotazníků, které chcete zodpovědět společně s dotazy, které chcete použít u vybraných respondentů.</span><span class="sxs-lookup"><span data-stu-id="d271e-126">Use the Setup details to select the questionnaire(s) to be answered as well as any queries to use to select respondents.</span></span>

1. <span data-ttu-id="d271e-127">Klikněte na Podrobnosti nastavení.</span><span class="sxs-lookup"><span data-stu-id="d271e-127">Click Setup details.</span></span>

2. <span data-ttu-id="d271e-128">V seznamu vyberte dotaz, který chcete použít k vyhledání systému pro respondenty dotazníku.</span><span class="sxs-lookup"><span data-stu-id="d271e-128">In the list, select a query to use to search the system for respondents for the questionnaire.</span></span>

    * <span data-ttu-id="d271e-129">Příklad: Pracovníci</span><span class="sxs-lookup"><span data-stu-id="d271e-129">Example: Workers</span></span>  

3. <span data-ttu-id="d271e-130">Klepněte na tlačítko Zobrazit nebo upravit dotaz a vyberte tak určité uživatele nebo upravte dotaz a vyhledejte tak osoby odpovídající konkrétním kritériím.</span><span class="sxs-lookup"><span data-stu-id="d271e-130">Click View or modify query to select specific people or adjust the query to find people who match specific criteria.</span></span>

    * <span data-ttu-id="d271e-131">Respondenti musí být také uživateli v systému.</span><span class="sxs-lookup"><span data-stu-id="d271e-131">Note that all respondents must also be users in the system.</span></span>  

4. <span data-ttu-id="d271e-132">V seznamu označte řádek Osoba.</span><span class="sxs-lookup"><span data-stu-id="d271e-132">In the list, mark the row for Person</span></span>

5. <span data-ttu-id="d271e-133">V poli Kritéria zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d271e-133">In the Criteria field, enter or select a value.</span></span>

    * <span data-ttu-id="d271e-134">Vyberte Julia Funderburk</span><span class="sxs-lookup"><span data-stu-id="d271e-134">Select Julia Funderburk</span></span>  

6. <span data-ttu-id="d271e-135">V seznamu vyberte Julia Funderburk</span><span class="sxs-lookup"><span data-stu-id="d271e-135">In the list, select Julia Funderburk</span></span>

7. <span data-ttu-id="d271e-136">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="d271e-136">Click OK.</span></span>

8. <span data-ttu-id="d271e-137">Klepněte na kartu Dotazníky.</span><span class="sxs-lookup"><span data-stu-id="d271e-137">Click the Questionnaires tab.</span></span>

9. <span data-ttu-id="d271e-138">Ve stromovém zobrazení rozbalte uzel pro typ dotazníku Průzkum spokojenosti.</span><span class="sxs-lookup"><span data-stu-id="d271e-138">In the tree, expand 'the node for the questionnaire type Satisfaction Survey'.</span></span>

10. <span data-ttu-id="d271e-139">Ve stromové struktuře označte "Posouzení zdravotního stavu pracovníků".</span><span class="sxs-lookup"><span data-stu-id="d271e-139">In the tree, check 'Workforce Health Assessment'.</span></span>

11. <span data-ttu-id="d271e-140">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="d271e-140">Click OK.</span></span>

12. <span data-ttu-id="d271e-141">Klikněte na Plánovaná relace odpovědí.</span><span class="sxs-lookup"><span data-stu-id="d271e-141">Click Planned answer session.</span></span>

    * <span data-ttu-id="d271e-142">Plánované relace odpovědí byly vytvořeny pro jednotlivé vybrané/dotazované uživatele.</span><span class="sxs-lookup"><span data-stu-id="d271e-142">Note that Planned answer sessions have been created for each selected/queried user.</span></span>  

13. <span data-ttu-id="d271e-143">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="d271e-143">Close the page.</span></span>

## <a name="start-the-questionnaire-schedule-in-order-to-make-the-questionnaire-available-for-respondents-to-complete"></a><span data-ttu-id="d271e-144">Zahajte plánování dotazníku, pokud chcete zpřístupnit respondentům dotazník k vyplnění.</span><span class="sxs-lookup"><span data-stu-id="d271e-144">Start the questionnaire schedule in order to make the questionnaire available for respondents to complete.</span></span>

1. <span data-ttu-id="d271e-145">Klepněte na možnost Funkce.</span><span class="sxs-lookup"><span data-stu-id="d271e-145">Click Functions.</span></span>

2. <span data-ttu-id="d271e-146">Klikněte na položku Spustit.</span><span class="sxs-lookup"><span data-stu-id="d271e-146">Click Start.</span></span>

3. <span data-ttu-id="d271e-147">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="d271e-147">Click OK.</span></span>

## <a name="send-the-email-to-inform-respondents-of-the-available-questionnaire"></a><span data-ttu-id="d271e-148">Odešlete e-mail informující respondenty o dostupném dotazníku.</span><span class="sxs-lookup"><span data-stu-id="d271e-148">Send the email to inform respondents of the available questionnaire.</span></span>

1. <span data-ttu-id="d271e-149">Klepněte na možnost Funkce.</span><span class="sxs-lookup"><span data-stu-id="d271e-149">Click Functions.</span></span>

2. <span data-ttu-id="d271e-150">Klikněte na Odeslat e-mail.</span><span class="sxs-lookup"><span data-stu-id="d271e-150">Click Send email.</span></span>

3. <span data-ttu-id="d271e-151">Klikněte na možnost Zrušit.</span><span class="sxs-lookup"><span data-stu-id="d271e-151">Click Cancel.</span></span>

## <a name="use-planned-answer-sessions-to-monitor-who-needs-to-complete-the-questionnaire"></a><span data-ttu-id="d271e-152">Použijte Plánované relace odpovědí ke sledování toho, kdo má dotazník vyplnit.</span><span class="sxs-lookup"><span data-stu-id="d271e-152">Use Planned answer sessions to monitor who needs to complete the questionnaire.</span></span>

1. <span data-ttu-id="d271e-153">Klikněte na Plánovaná relace odpovědí.</span><span class="sxs-lookup"><span data-stu-id="d271e-153">Click Planned answer session.</span></span>

    * <span data-ttu-id="d271e-154">Jakmile budete připraveni ukončit plánovanou relaci, odstraňte veškeré zbývající plánované relace odpovědí.</span><span class="sxs-lookup"><span data-stu-id="d271e-154">Delete any remaining planned answer session when you're ready to end the scheduled session.</span></span>  

2. <span data-ttu-id="d271e-155">Klepněte na tlačítko Odstranit.</span><span class="sxs-lookup"><span data-stu-id="d271e-155">Click Delete.</span></span>

3. <span data-ttu-id="d271e-156">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="d271e-156">Click Yes.</span></span>

4. <span data-ttu-id="d271e-157">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="d271e-157">Close the page.</span></span>

## <a name="end-the-schedule-when-all-respondents-have-completed-the-questionnaire-andor-all-remaining-planned-answer-sessions-have-been-deleted"></a><span data-ttu-id="d271e-158">Poté, co dotazník vyplní všichni respondenti nebo jsou odstraněny všechny zbývající plánované relace odpovědí, plán ukončete.</span><span class="sxs-lookup"><span data-stu-id="d271e-158">End the schedule when all respondents have completed the questionnaire and/or all remaining Planned answer sessions have been deleted.</span></span>

1. <span data-ttu-id="d271e-159">Klepněte na možnost Funkce.</span><span class="sxs-lookup"><span data-stu-id="d271e-159">Click Functions.</span></span>
2. <span data-ttu-id="d271e-160">Klepněte na tlačítko Konec.</span><span class="sxs-lookup"><span data-stu-id="d271e-160">Click End.</span></span>
3. <span data-ttu-id="d271e-161">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="d271e-161">Click OK.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]