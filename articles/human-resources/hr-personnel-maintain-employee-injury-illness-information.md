---
title: Udržování informací o zraněních a onemocněních zaměstnanců
description: Doporučuje se nejprve postupovat podle příručky „Určení zranění a onemocnění“ protože některé se zde uplatňují některé údaje.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMInjuryIncident, HcmWorkerLookUp, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 367834e7e02d2061732f46d8e697044e7c49b884
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417597"
---
# <a name="maintain-employee-injury-and-illness-information"></a><span data-ttu-id="bbf1d-103">Udržování informací o zraněních a onemocněních zaměstnanců</span><span class="sxs-lookup"><span data-stu-id="bbf1d-103">Maintain employee injury and illness information</span></span>



<span data-ttu-id="bbf1d-104">Doporučuje se nejprve postupovat podle příručky „Určení zranění a onemocnění“ protože některé se zde uplatňují některé údaje.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-104">It is recommended to complete the 'Setup injury and illness' task guide first, as some of the setup information is used here.</span></span> 



<span data-ttu-id="bbf1d-105">Tento záznam úlohy popisuje základní postup pro vytvoření případu zranění nebo onemocnění.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-105">This task recording covers the basic steps to creating an injury or illness case.</span></span> <span data-ttu-id="bbf1d-106">Kromě sledování podrobností o zranění nebo onemocnění, je také sledovaný stav případu.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-106">Besides tracking the details of the injury or illness, there is a case status that is tracked as well.</span></span>  <span data-ttu-id="bbf1d-107">Výchozí nastavení případu se stavem „Otevřeno“.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-107">The case defaults with an 'open' status.</span></span>  <span data-ttu-id="bbf1d-108">Stav lze spravovat z položky nabídky „Stav případu“ v pruhu aplikace v horní části stránky.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-108">The statuses can be managed from the 'Case status' menu item at the top of the page.</span></span>

1. <span data-ttu-id="bbf1d-109">Přejděte na Lidské zdroje > Pracovníci > Zranění a onemocnění > Incidenty zranění nebo onemocnění.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-109">Go to Human resources > Workers > Injury and illness > Injury or illness incidents.</span></span>
2. <span data-ttu-id="bbf1d-110">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-110">Click New.</span></span>
3. <span data-ttu-id="bbf1d-111">Zadejte hodnotu do pole Popis případu.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-111">In the Case description field, type a value.</span></span>
    * <span data-ttu-id="bbf1d-112">Příklad: Zranění zápěstí</span><span class="sxs-lookup"><span data-stu-id="bbf1d-112">Example:  Wrist injury</span></span>  
4. <span data-ttu-id="bbf1d-113">V poli Pracovník zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-113">In the Worker field, enter or select a value.</span></span>
    * <span data-ttu-id="bbf1d-114">Příklad: Ahmed Barnett</span><span class="sxs-lookup"><span data-stu-id="bbf1d-114">Example: Ahmed Barnett</span></span>  
5. <span data-ttu-id="bbf1d-115">Zadejte datum a čas do pole Datum a čas incidentu.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-115">In the Date and time of incident field, enter a date and time.</span></span>
    * <span data-ttu-id="bbf1d-116">Příklad: 20. 1. 2016 10:00:00</span><span class="sxs-lookup"><span data-stu-id="bbf1d-116">Example:  1/20/2016 10:00 AM</span></span>  
6. <span data-ttu-id="bbf1d-117">V poli Typ zranění nebo onemocnění zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-117">In the Injury or illness type field, enter or select a value.</span></span>
    * <span data-ttu-id="bbf1d-118">Příklad: Zlomenina</span><span class="sxs-lookup"><span data-stu-id="bbf1d-118">Example:  Fracture</span></span>  
7. <span data-ttu-id="bbf1d-119">V poli Část těla zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-119">In the Body part field, enter or select a value.</span></span>
    * <span data-ttu-id="bbf1d-120">Příklad: Zápěstí</span><span class="sxs-lookup"><span data-stu-id="bbf1d-120">Example:  Wrist</span></span>  
8. <span data-ttu-id="bbf1d-121">V poli Typ výsledku zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-121">In the Outcome type field, enter or select a value.</span></span>
    * <span data-ttu-id="bbf1d-122">Příklad: Léčba</span><span class="sxs-lookup"><span data-stu-id="bbf1d-122">Example:  Therapy</span></span>  
9. <span data-ttu-id="bbf1d-123">Zadejte datum a čas do pole Datum a čas nahlášení.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-123">In the Date and time reported field, enter a date and time.</span></span>
    * <span data-ttu-id="bbf1d-124">Datum a čas ohlášené v poli musí být pozdější než datum a čas incidentu.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-124">The date and time reported must be later than the date and time of incident.</span></span>  
10. <span data-ttu-id="bbf1d-125">Zadejte nebo vyberte požadovanou hodnotu u osoby, která vykázala případ.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-125">In the Person who reported case field, enter or select a value.</span></span>
    * <span data-ttu-id="bbf1d-126">To může být zaměstnanec nebo na jiný důkaz k incidentu.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-126">This could be the employee or another witness to the incident.</span></span>  <span data-ttu-id="bbf1d-127">Příklad: Ahmed Barnett</span><span class="sxs-lookup"><span data-stu-id="bbf1d-127">Example: Ahmed Barnett</span></span>  
11. <span data-ttu-id="bbf1d-128">Rozbalte sekci Incident.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-128">Expand the Incident section.</span></span>
12. <span data-ttu-id="bbf1d-129">Zadejte hodnotu do pole Kde k incidentu došlo.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-129">In the Where incident occurred field, type a value.</span></span>
    * <span data-ttu-id="bbf1d-130">Příklad: Sklad</span><span class="sxs-lookup"><span data-stu-id="bbf1d-130">Example:  Warehouse</span></span>  
13. <span data-ttu-id="bbf1d-131">Vyberte možnost Ano v poli V pracovních prostorách.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-131">Select Yes in the On work premises field.</span></span>
    * <span data-ttu-id="bbf1d-132">Pokud incident vznikl v pracovních prostorách, vyberte ano.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-132">If the incident occurred on work premises, select yes.</span></span>  
14. <span data-ttu-id="bbf1d-133">Zadejte datum a čas do pole Datum a čas zahájení práce.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-133">In the Date and time began work field, enter a date and time.</span></span>
    * <span data-ttu-id="bbf1d-134">Zadejte datum a čas, kdy ovlivněný jednotlivec začal pracovat před výskytem incidentu.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-134">Enter the date and time that affected individual started working, prior to the incident occurring.</span></span>  
15. <span data-ttu-id="bbf1d-135">Zadejte hodnotu do pole Práce nebo úkol zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-135">In the Employee job or task field, type a value.</span></span>
    * <span data-ttu-id="bbf1d-136">Zadejte úlohu nebo úkol, který pracovník vykonával při vzniku incidentu.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-136">Enter the job or task the worker was performing when the incident occurred.</span></span>  <span data-ttu-id="bbf1d-137">Příklad: Nakládání krabic</span><span class="sxs-lookup"><span data-stu-id="bbf1d-137">Example:  Loading boxes</span></span>  
16. <span data-ttu-id="bbf1d-138">Zadejte hodnotu do pole Příčina incidentu.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-138">In the Cause of incident field, type a value.</span></span>
    * <span data-ttu-id="bbf1d-139">Zadejte příčinu nebo incident.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-139">Enter the cause of the incident.</span></span>  <span data-ttu-id="bbf1d-140">Příklad: Uklouznutí na vlhké podlaze</span><span class="sxs-lookup"><span data-stu-id="bbf1d-140">Example:  Slipped on wet floor</span></span>  
17. <span data-ttu-id="bbf1d-141">Zadejte nebo vyberte hodnotu do pole Úroveň závažnosti.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-141">In the Severity level field, enter or select a value.</span></span>
18. <span data-ttu-id="bbf1d-142">Zadejte hodnotu do pole Provést akci.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-142">In the Action to be taken field, type a value.</span></span>
    * <span data-ttu-id="bbf1d-143">Příklad: Rychlé rozlití při úklidu</span><span class="sxs-lookup"><span data-stu-id="bbf1d-143">Example:  Clean up spills promptly</span></span>  
19. <span data-ttu-id="bbf1d-144">Zadejte číslo do pole Očekávané dny v pracovní neschopnosti.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-144">In the Expected days away from work field, enter a number.</span></span>
    * <span data-ttu-id="bbf1d-145">Zadejte počet dní, po které se očekává, že daná osoba bude v pracovní neschopnosti.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-145">Enter the number of days that the individual is expected to be away from work.</span></span>  <span data-ttu-id="bbf1d-146">Jakmile se osoba vrátí do práce, aktualizujte pole „Počet dnů pracovní neschopnosti“ skutečným počtem dnů nepřítomnosti.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-146">Once the individual returns to work, update the 'Days away from work' field with the actual number of days away.</span></span>  
20. <span data-ttu-id="bbf1d-147">Rozbalte část Náklady na zranění nebo onemocnění.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-147">Expand the Injury or illness costs section.</span></span>
21. <span data-ttu-id="bbf1d-148">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-148">Click Add.</span></span>
22. <span data-ttu-id="bbf1d-149">Do pole Datum zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-149">In the Date field, enter a date.</span></span>
23. <span data-ttu-id="bbf1d-150">V poli Typ nákladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-150">In the Cost type field, enter or select a value.</span></span>
    * <span data-ttu-id="bbf1d-151">Příklad:  Léčení   Můžete také zadat částku a připojit podklady, jako jsou například faktury nebo lékařské potvrzení o nákladech.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-151">Example:  Therapy    You can also enter in an amount, and attach any supporting documentation such as invoices or doctor's notes to the cost.</span></span>  
24. <span data-ttu-id="bbf1d-152">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-152">Click Add.</span></span>
25. <span data-ttu-id="bbf1d-153">Do pole Datum zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-153">In the Date field, enter a date.</span></span>
26. <span data-ttu-id="bbf1d-154">V poli Typ nákladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-154">In the Cost type field, enter or select a value.</span></span>
    * <span data-ttu-id="bbf1d-155">Příklad: Lékař</span><span class="sxs-lookup"><span data-stu-id="bbf1d-155">Example: Doctor</span></span>  
27. <span data-ttu-id="bbf1d-156">Rozbalte část Ošetření zranění nebo onemocnění.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-156">Expand the Injury or illness treatments section.</span></span>
28. <span data-ttu-id="bbf1d-157">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-157">Click Add.</span></span>
29. <span data-ttu-id="bbf1d-158">Do pole Datum ošetření zadejte datum a čas.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-158">In the Treatment date field, enter a date and time.</span></span>
30. <span data-ttu-id="bbf1d-159">V poli Typ ošetření zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-159">In the Treatment type field, enter or select a value.</span></span>
    * <span data-ttu-id="bbf1d-160">Příklad: Dlaha</span><span class="sxs-lookup"><span data-stu-id="bbf1d-160">Example:  Splint</span></span>  
31. <span data-ttu-id="bbf1d-161">Volitelně nastavte v části Návštěva pohotovosti v nemocnici hodnotu Ano.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-161">Optionally, set the emergency room hospital visit section to Yes.</span></span>
32. <span data-ttu-id="bbf1d-162">Zadejte hodnotu do pole Poznámky k ošetření.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-162">In the Treatment comments field, type a value.</span></span>
    * <span data-ttu-id="bbf1d-163">Příklad: Dlaha po dobu 2 týdnů</span><span class="sxs-lookup"><span data-stu-id="bbf1d-163">Example:  Splint for 2 weeks</span></span>  
33. <span data-ttu-id="bbf1d-164">Do pole Jméno lékaře zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-164">In the Physician name field, type a value.</span></span>
    * <span data-ttu-id="bbf1d-165">Příklad: Dr. Anderson</span><span class="sxs-lookup"><span data-stu-id="bbf1d-165">Example:  Dr. Anderson</span></span>  
34. <span data-ttu-id="bbf1d-166">Zadejte hodnotu do pole Léčebné zařízení a umístění.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-166">In the Treatment facility and location field, type a value.</span></span>
    * <span data-ttu-id="bbf1d-167">Příklad: Pohotovost Elm St. </span><span class="sxs-lookup"><span data-stu-id="bbf1d-167">Example:  Elm St. Emergency</span></span>  
35. <span data-ttu-id="bbf1d-168">Zadejte hodnotu do pole Podrobnosti o ošetření.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-168">In the Treatment details field, type a value.</span></span>
    * <span data-ttu-id="bbf1d-169">Příklad: Rentgenem potvrzená zlomenina, aplikována dlaha</span><span class="sxs-lookup"><span data-stu-id="bbf1d-169">Example:  Xray confirms fracture, wear splint</span></span>  
36. <span data-ttu-id="bbf1d-170">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-170">Click Save.</span></span>
    * <span data-ttu-id="bbf1d-171">Stav případu lze kdykoli aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-171">The case status can be updated at any time.</span></span>  <span data-ttu-id="bbf1d-172">Nastavte případ na stav Probíhá, pokud probíhá zpracování zranění nebo onemocnění.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-172">Set the case to in process, if the processing of the injury or illness is in process.</span></span>  <span data-ttu-id="bbf1d-173">Jakmile uzavřete incident, můžete pouze přidat nebo odebrat náklady, léčbu nebo evidenci související s incidentem.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-173">Once you close the incident you can only add or remove costs, treatments or filings related to the incident.</span></span>  <span data-ttu-id="bbf1d-174">Chcete-li upravit informace, případ znovu otevřete.</span><span class="sxs-lookup"><span data-stu-id="bbf1d-174">To modify other information, reopen the case.</span></span>  

