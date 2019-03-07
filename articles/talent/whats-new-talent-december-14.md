---
title: Co je nového nebo upraveného v aplikaci Dynamics 365 for Talent Core HR (14. prosince 2018)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 12/14/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-12-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 7d2866923efd7f115ad5290f35ed4fcac5e47573
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "303504"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-december-14-2018"></a><span data-ttu-id="b5807-103">Co je nového nebo upraveného v aplikaci Dynamics 365 for Talent Core HR (14. prosince 2018)</span><span class="sxs-lookup"><span data-stu-id="b5807-103">What's new or changed in Dynamics 365 for Talent Core HR (December 14, 2018)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b5807-104">**Sestavení 8.1.2085**</span><span class="sxs-lookup"><span data-stu-id="b5807-104">**Build 8.1.2085**</span></span>

<span data-ttu-id="b5807-105">Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Core HR.</span><span class="sxs-lookup"><span data-stu-id="b5807-105">This topic describes features that are either new or changed in Core HR.</span></span>

## <a name="changes"></a><span data-ttu-id="b5807-106">Změny</span><span class="sxs-lookup"><span data-stu-id="b5807-106">Changes</span></span>

### <a name="us---aca-affordable-care-act-support-for-tax-year-2018-1095-b-and-1095-c-forms"></a><span data-ttu-id="b5807-107">US - ACA (Provedení dostupné péče) podpora daňového roku 2018 1095-B a formulářů 1095-C</span><span class="sxs-lookup"><span data-stu-id="b5807-107">US - ACA (Affordable Care Act) support for tax year 2018 1095-B and 1095-C forms</span></span>

<span data-ttu-id="b5807-108">Každý rok musí příslušní velcí zaměstnavatelů poskytovat každému zaměstnanci na plný úvazek formulář 1095-C.</span><span class="sxs-lookup"><span data-stu-id="b5807-108">Each year, Applicable Large Employers (ALEs) must provide each full-time employees with a 1095-C.</span></span> <span data-ttu-id="b5807-109">Dále, pokud zaměstnavatel poskytuje vlastní pojistné krytí, musí zaměstnanci (na plný či částečný úvazek), který je krytý jedním ze zdravotních plánů zaměstnance, poskytnout formulář 1095-C (pokud se jedná o příslušného velkého zaměstnavatele) a formulář 1095-B (pokud se jedná o malé zaměstnavatele).</span><span class="sxs-lookup"><span data-stu-id="b5807-109">In addition, if the employer provides self-insured coverage they must provide the 1095-C (if they are an ALE) and a 1095-B (if they are a small employer) to any employee, full-time or part-time, covered under one of their offered health plans.</span></span> <span data-ttu-id="b5807-110">Tato funkce poskytuje vytisknutelné formuláře 1095-C i 1095-B.</span><span class="sxs-lookup"><span data-stu-id="b5807-110">This feature provides printable forms for both the 1095-C and 1095-B.</span></span>

### <a name="during-import-submittedbypersonid-field-on-hcmperfjournalentity-is-ignored"></a><span data-ttu-id="b5807-111">Při importu pole SubmittedByPersonId na HcmPerfJournalEntity je ignorováno</span><span class="sxs-lookup"><span data-stu-id="b5807-111">During import SubmittedByPersonId field on HcmPerfJournalEntity is ignored</span></span>

<span data-ttu-id="b5807-112">Při importu/exportu výkonu záznamů v deníku je pole **odeslal** ignorováno.</span><span class="sxs-lookup"><span data-stu-id="b5807-112">When importing/exporting performance journal entries, the **Submitted by** field is ignored.</span></span> <span data-ttu-id="b5807-113">Touto změnou hodnota **import a export** představuje hodnotu, která v tabulce během exportu při importu systému bude aktualizována o hodnotu zadanou v importovaném souboru.</span><span class="sxs-lookup"><span data-stu-id="b5807-113">With this change, the value **imported/exported** will reflect the value in the table during the export, when importing the system will be updated with the value supplied in the import file.</span></span>

### <a name="analytics-tab-on-leave-and-absence-workspace-displays-openconnectionerror-error-for-non-system-admin-roles"></a><span data-ttu-id="b5807-114">Analytika v pracovním prostoru 'Volna a absence' zobrazuje chybu "OpenConnectionError" pro role správce, které nejsou systémové</span><span class="sxs-lookup"><span data-stu-id="b5807-114">Analytics tab on 'Leave and absence' workspace displays "OpenConnectionError" error for non-system Admin roles</span></span>

<span data-ttu-id="b5807-115">S touto aktualizací nebudou při otevírání záložky **Analýza** v pracovním prostoru **Dovolená a absence** zobrazeny žádné chyby.</span><span class="sxs-lookup"><span data-stu-id="b5807-115">With this update, no errors will be issued when opening the **Analytics** tab on the **Leave and Absence** workspace.</span></span>

### <a name="employee-self-service-position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a><span data-ttu-id="b5807-116">Samoobsluha pro zaměstnance, rozbalení hierarchie pozic ze selhání dlaždic za účelem získání nadřazeného uzlu</span><span class="sxs-lookup"><span data-stu-id="b5807-116">Employee self-service, Position Hierarchy drill-down from tile fails to get parent node</span></span>

<span data-ttu-id="b5807-117">Byla provedena změna opravy chyby "Získání nadřazeného uzlu se nezdařilo", když došlo k úpravě hierarchie pozice, aby s zobrazila ve stávajícím praocvním prostoru a pozice je vybrána v hierarchii.</span><span class="sxs-lookup"><span data-stu-id="b5807-117">A change has been made to correct the error "Getting the parent node failed" when the position hierarchy has been personalized to appear on an existing workspace and a position is selected in the hierarchy.</span></span>  

### <a name="must-be-system-admin-to-see-the-payroll-tab-in-the-position-page"></a><span data-ttu-id="b5807-118">Musí být správce systému,a by na stránce Pozice bylo možné zobrazit záložku Mzda</span><span class="sxs-lookup"><span data-stu-id="b5807-118">Must be System Admin to see the Payroll tab in the Position page</span></span>

<span data-ttu-id="b5807-119">Byla provedena změna, která má zahrnout správné bezpečnostní prvky do stávajícího právnění: "Udržovat podrobnosti mezd a pozice pracovníka".</span><span class="sxs-lookup"><span data-stu-id="b5807-119">A change has been made to include the correct security elements in the existing privilege: "Maintain payroll worker and position detail".</span></span> <span data-ttu-id="b5807-120">Touto změnou standardně Správce mezd bude mít přístup k polím mezd na stránce pozice.</span><span class="sxs-lookup"><span data-stu-id="b5807-120">With this change, by default, the Payroll Administrator will have access to the Payroll fields on the Position page.</span></span>

### <a name="error-when-submitting-performance-review-to-manager-and-the-reviewsperfperiod-placeholder-is-used-in-the-submission-instructions"></a><span data-ttu-id="b5807-121">Došlo k chybě při odeslání kontroly výkonu vedoucímu pracovníkovi a v pokynech odeslání je použit zástupný znak %Reviews.PerfPeriod%</span><span class="sxs-lookup"><span data-stu-id="b5807-121">Error when submitting performance review to manager and the %Reviews.PerfPeriod% placeholder is used in the Submission instructions</span></span>

<span data-ttu-id="b5807-122">Byla provedena změny, která opravuje chybu "Odkaz s hodnotou null" při použití zástupného textu %Reviews.PerfPeriod% v pokynech odeslání.</span><span class="sxs-lookup"><span data-stu-id="b5807-122">A change has been made that corrects the "Null Reference" error when using the %Reviews.PerfPeriod% placeholder in the Submission instructions.</span></span>

### <a name="workforce-power-bi-report-shows-error-when-worker-seniority-date-is-a-leap-day"></a><span data-ttu-id="b5807-123">Výkaz pracovní síly Power BI zobrazuje chybu, když je datum mzdového služebního věku v přestupný den</span><span class="sxs-lookup"><span data-stu-id="b5807-123">Workforce Power BI report shows error when worker seniority date is a leap day</span></span>

<span data-ttu-id="b5807-124">Touto změnou jsou nyní v Power BI podporovány přestupné dny.</span><span class="sxs-lookup"><span data-stu-id="b5807-124">With this change, leap days are now supported in Power BI.</span></span>

### <a name="integration-between-core-hr-and-attract"></a><span data-ttu-id="b5807-125">Integrace mezi aplikacemi Core HR a Attract</span><span class="sxs-lookup"><span data-stu-id="b5807-125">Integration between Core HR and Attract</span></span>

<span data-ttu-id="b5807-126">Byla provedena změna, která má aktualizovat integraci mezi aplikacemi Core HR a Attract související s nabíranými uchazeči.</span><span class="sxs-lookup"><span data-stu-id="b5807-126">A change has been made to update the integration between Core HR and Attract related to candidates to hire.</span></span> <span data-ttu-id="b5807-127">Aby nabíraná uchazeči byli vidět v pracovním prostoru **Správa zaměstnanců**, jsou pro entity aplikací (CDS 2.0) použity následující CDS:</span><span class="sxs-lookup"><span data-stu-id="b5807-127">For candidates to hire to be visible in the **Personnel Management** workspace, the following CDS for Apps (CDS 2.0) entities are used:</span></span>

<span data-ttu-id="b5807-128">Žádost o práci</span><span class="sxs-lookup"><span data-stu-id="b5807-128">Job Application</span></span>
- <span data-ttu-id="b5807-129">Stav důvodů je třeba nastavit na přijetí nabídky</span><span class="sxs-lookup"><span data-stu-id="b5807-129">Status Reason needs to be set to Offer Accepted</span></span>
-   <span data-ttu-id="b5807-130">Poskytuje kandidát a pracovní místo</span><span class="sxs-lookup"><span data-stu-id="b5807-130">Provides Candidate and Job Opening</span></span>

<span data-ttu-id="b5807-131">Kandidát</span><span class="sxs-lookup"><span data-stu-id="b5807-131">Candidate</span></span>
-   <span data-ttu-id="b5807-132">Poskytuje informace o kandidátovi</span><span class="sxs-lookup"><span data-stu-id="b5807-132">Provides Candidate information</span></span>

<span data-ttu-id="b5807-133">Volné pracovní místo</span><span class="sxs-lookup"><span data-stu-id="b5807-133">Job Opening</span></span>
-   <span data-ttu-id="b5807-134">Poskytuje ID volné pozice a účastníky volné pracovní pozice</span><span class="sxs-lookup"><span data-stu-id="b5807-134">Provides Job Opening ID and Job Opening Participants</span></span>

<span data-ttu-id="b5807-135">Účastníci volné pracovní pozice</span><span class="sxs-lookup"><span data-stu-id="b5807-135">Job Opening Participants</span></span>
-   <span data-ttu-id="b5807-136">Uvádí náborového manažera</span><span class="sxs-lookup"><span data-stu-id="b5807-136">Provides Hiring Manager</span></span>

<span data-ttu-id="b5807-137">Když je kandidát přidán do Správy zaměstnanců, může být zamítnut pomocí nové možnosti dostupné na kartě kandidáta.</span><span class="sxs-lookup"><span data-stu-id="b5807-137">When a candidate is added to Personnel Management, the candidate can now also be dismissed using a new option available on the candidate card.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="b5807-138">Již brzy</span><span class="sxs-lookup"><span data-stu-id="b5807-138">Coming soon</span></span>

### <a name="leave-and-absence-future-leave-and-forecasting-leave-balances"></a><span data-ttu-id="b5807-139">Dovolená a absence: budoucí volno a prognózy volna</span><span class="sxs-lookup"><span data-stu-id="b5807-139">Leave and absence: Future leave and forecasting leave balances</span></span>

<span data-ttu-id="b5807-140">Se změnami, které zaměstnancům umožňují předpovídat dobu volna a požaddat žádosti u boudcí volno, aniž by došlo k ovlivnění stávajících rozložení volna, se mění také způsob zobrazení rozložení volna.</span><span class="sxs-lookup"><span data-stu-id="b5807-140">With the changes being made to allow for employees to forecast time off and request future time off requests without impacting their current time off balances, the way the time off balances are displayed is also changing.</span></span> 

<span data-ttu-id="b5807-141">Dostupný zůstatek, který je aktuálně zobrazen, je množství volna dostupného pro žádosti, včetně nárůstů během dne a všech schválených žádostí o volno do konce období.</span><span class="sxs-lookup"><span data-stu-id="b5807-141">The available balance currently displayed is the amount of time off available for requests including accruals through today and all approved leave requests to the end of time.</span></span> 

<span data-ttu-id="b5807-142">Jakmile bude možné předpovídat, zobrazený zůstatek se změní na aktuální zůstatek volna, včetně nárůstu během dne a žádostí během dne.</span><span class="sxs-lookup"><span data-stu-id="b5807-142">When the ability to forecast is released, the balance displayed changes to  be the current balance of time off including accruals through today and requests through today.</span></span> <span data-ttu-id="b5807-143">Zaměstnanci a řídící pracovníci uvidí tyto aktualizované rozložení volna na kartě **Pracovní volno** karty a v okně **Rozložení volna**.</span><span class="sxs-lookup"><span data-stu-id="b5807-143">Employees and managers will see these updated balances in employee and manager self-service on the **Time off** card and in the **Time off balances** window.</span></span> <span data-ttu-id="b5807-144">Manažeři HR uvidí tyto aktualizované zůstatky v pracovní prostoru **Lidé** a v okně **Přiřazené plány volna** zaměstance.</span><span class="sxs-lookup"><span data-stu-id="b5807-144">HR managers will see these updated balances in the **People** workspace and in the employee’s **Assigned leave plans** window.</span></span>

## <a name="known-issue"></a><span data-ttu-id="b5807-145">Známý problém</span><span class="sxs-lookup"><span data-stu-id="b5807-145">Known issue</span></span>

### <a name="mapping-errors-in-the-integration-with-finance-and-operations"></a><span data-ttu-id="b5807-146">Chyby mapování integrace s aplikací Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b5807-146">Mapping errors in the integration with Finance and Operations</span></span>

<span data-ttu-id="b5807-147">Byly zjištěny následující chyby v aktuální šabloně pro integraci aplikace Talent s aplikací Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b5807-147">The following issues have been identified in the current template for integrating Talent with Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="b5807-148">Nová šablona bude publikována brzy a bude použita pro všechny nové integrace projektů, které jsou vytvořeny.</span><span class="sxs-lookup"><span data-stu-id="b5807-148">A new template will be published soon and will be applied to all new integration projects that are created.</span></span> <span data-ttu-id="b5807-149">Pro existující integrace projektů lze mapování úkolu aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="b5807-149">For existing integration projects, the task mappings can be updated.</span></span> <span data-ttu-id="b5807-150">Aktualizované mapování naleznete v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="b5807-150">Refer to the following table for updated mappings.</span></span> 

>[!NOTE]
> <span data-ttu-id="b5807-151">Úkol Pracovní pozice do  přiřazení práce nadřazené pozice neintegruje data.</span><span class="sxs-lookup"><span data-stu-id="b5807-151">The Job Positions to Positions Parent Job Assignment task does not integrate data.</span></span> <span data-ttu-id="b5807-152">Toto je problém, který je právě zkoumán.</span><span class="sxs-lookup"><span data-stu-id="b5807-152">This is an issue that is currently being researched.</span></span> <span data-ttu-id="b5807-153">Aktuální mapování nelze nijak obejít.</span><span class="sxs-lookup"><span data-stu-id="b5807-153">There is no workaround in the current mapping.</span></span> 

<span data-ttu-id="b5807-154">Úkol oddělení do provozní jednotky vyžaduje aktualizaci následujících mapování.</span><span class="sxs-lookup"><span data-stu-id="b5807-154">The Departments to Operating unit task needs the following mappings updated.</span></span>

| <span data-ttu-id="b5807-155">Stávající pole zdroje</span><span class="sxs-lookup"><span data-stu-id="b5807-155">Existing source field</span></span>          | <span data-ttu-id="b5807-156">Pole nového zdroje</span><span class="sxs-lookup"><span data-stu-id="b5807-156">New source field</span></span> |
| -------------------------------|------------------|
| <span data-ttu-id="b5807-157">cdm_description (popis)</span><span class="sxs-lookup"><span data-stu-id="b5807-157">cdm_description (Description)</span></span>  | <span data-ttu-id="b5807-158">cdm_name (název)</span><span class="sxs-lookup"><span data-stu-id="b5807-158">cdm_name (Name)</span></span>  |

<span data-ttu-id="b5807-159">Také je třeba přidat další mapování.</span><span class="sxs-lookup"><span data-stu-id="b5807-159">An additional mapping also needs to be added.</span></span> <span data-ttu-id="b5807-160">Vyberte poslední pole **Žádná** pro přidání následujícího mapování.</span><span class="sxs-lookup"><span data-stu-id="b5807-160">Select the last **None** field to add the following mapping.</span></span>

| <span data-ttu-id="b5807-161">Zdrojové pole</span><span class="sxs-lookup"><span data-stu-id="b5807-161">Source field</span></span>                   | <span data-ttu-id="b5807-162">Cílové pole</span><span class="sxs-lookup"><span data-stu-id="b5807-162">Destination field</span></span>    |
| -------------------------------|----------------------|
| <span data-ttu-id="b5807-163">cdm_description (popis)</span><span class="sxs-lookup"><span data-stu-id="b5807-163">cdm_description (Description)</span></span>  | <span data-ttu-id="b5807-164">NAMEALIAS (NAMEALIAS)</span><span class="sxs-lookup"><span data-stu-id="b5807-164">NAMEALIAS (NAMEALIAS)</span></span>|

<span data-ttu-id="b5807-165">Aktualizované mapování by mělo vypadat jako následující obrázek.</span><span class="sxs-lookup"><span data-stu-id="b5807-165">The updated mappings should look like the following image.</span></span>

![Úkol oddělení do operačních jednotek](./media/DepartmentMapping.png)


<span data-ttu-id="b5807-167">Úkol úloh do podrobnosti úlohy vyžaduje aktualizaci následujících mapování.</span><span class="sxs-lookup"><span data-stu-id="b5807-167">The Jobs to Job Detail task needs the following mappings updated.</span></span>

| <span data-ttu-id="b5807-168">Stávající pole zdroje</span><span class="sxs-lookup"><span data-stu-id="b5807-168">Existing source field</span></span>          | <span data-ttu-id="b5807-169">Pole nového zdroje</span><span class="sxs-lookup"><span data-stu-id="b5807-169">New source field</span></span>                   |
| -------------------------------|------------------------------------|
| <span data-ttu-id="b5807-170">cdm_name (název)</span><span class="sxs-lookup"><span data-stu-id="b5807-170">cdm_name (Name)</span></span>                | <span data-ttu-id="b5807-171">cdm_description (popis)</span><span class="sxs-lookup"><span data-stu-id="b5807-171">cdm_description (Description)</span></span>      |
| <span data-ttu-id="b5807-172">cdm_name (popis)</span><span class="sxs-lookup"><span data-stu-id="b5807-172">cdm_name (Description)</span></span>         | <span data-ttu-id="b5807-173">cdm_description (popis práce)</span><span class="sxs-lookup"><span data-stu-id="b5807-173">cdm_jobdescription(Job Description)</span></span>|


<span data-ttu-id="b5807-174">Aktualizované mapování by mělo vypadat jako obrázek níže.</span><span class="sxs-lookup"><span data-stu-id="b5807-174">The updated mappings should look like the image below.</span></span>

![Úkol úloh do podrobnosti úlohy](./media/JobMapping.png)

<span data-ttu-id="b5807-176">Úkol pracovníci do práce vyžaduje aktualizaci následujících mapování.</span><span class="sxs-lookup"><span data-stu-id="b5807-176">The Workers to Work task needs the following mappings updated.</span></span>

| <span data-ttu-id="b5807-177">Stávající pole zdroje</span><span class="sxs-lookup"><span data-stu-id="b5807-177">Existing source field</span></span>                 | <span data-ttu-id="b5807-178">Pole nového zdroje</span><span class="sxs-lookup"><span data-stu-id="b5807-178">New source field</span></span>                               |
| --------------------------------------|------------------------------------------------|
| <span data-ttu-id="b5807-179">cdm_emailaddress1 (e-mailová adresa 1)</span><span class="sxs-lookup"><span data-stu-id="b5807-179">cdm_emailaddress1 (Email Address 1)</span></span>   | <span data-ttu-id="b5807-180">cdm_primaryemailaddress (primární e-mailová adresa</span><span class="sxs-lookup"><span data-stu-id="b5807-180">cdm_primaryemailaddress (Primary Email Address</span></span> |
| <span data-ttu-id="b5807-181">cdm_telephone1 (telefon 1)</span><span class="sxs-lookup"><span data-stu-id="b5807-181">cdm_telephone1 (Telephone 1)</span></span>          | <span data-ttu-id="b5807-182">cdm_primarytelephone (primární telefon)</span><span class="sxs-lookup"><span data-stu-id="b5807-182">cdm_primarytelephone (Primary Telephone)</span></span>       |

<span data-ttu-id="b5807-183">Transformace pole pohlaví je rovněž třeba aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="b5807-183">The Gender field transform also needs to be updated.</span></span> <span data-ttu-id="b5807-184">Vyberte typ mapy **fn** (funkce) pro pohlaví a aktualizujte následující mapování hodnot.</span><span class="sxs-lookup"><span data-stu-id="b5807-184">Select the **fn** (function) map type for Gender and update the following value mappings.</span></span>

| <span data-ttu-id="b5807-185">Hodnota CDS</span><span class="sxs-lookup"><span data-stu-id="b5807-185">CDS value</span></span>                   | <span data-ttu-id="b5807-186">Hodnota aplikace Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b5807-186">Finance and Operations value</span></span>                     |
| ----------------------------|--------------------------------------------------|
| <span data-ttu-id="b5807-187">75440000</span><span class="sxs-lookup"><span data-stu-id="b5807-187">75440000</span></span>                    | <span data-ttu-id="b5807-188">Muž</span><span class="sxs-lookup"><span data-stu-id="b5807-188">Male</span></span>                                             |
| <span data-ttu-id="b5807-189">75440001</span><span class="sxs-lookup"><span data-stu-id="b5807-189">75440001</span></span>                    | <span data-ttu-id="b5807-190">Žena</span><span class="sxs-lookup"><span data-stu-id="b5807-190">Female</span></span>                                           |
| <span data-ttu-id="b5807-191">75440002</span><span class="sxs-lookup"><span data-stu-id="b5807-191">75440002</span></span>                    | <span data-ttu-id="b5807-192">Neomezeno</span><span class="sxs-lookup"><span data-stu-id="b5807-192">None</span></span>                                             | 
| <span data-ttu-id="b5807-193">75440003</span><span class="sxs-lookup"><span data-stu-id="b5807-193">75440003</span></span>                    | <span data-ttu-id="b5807-194">Nespecifické</span><span class="sxs-lookup"><span data-stu-id="b5807-194">NonSpecific</span></span>                                      |

<span data-ttu-id="b5807-195">Aktualizované mapování by mělo vypadat jako následující obrázky.</span><span class="sxs-lookup"><span data-stu-id="b5807-195">The updated mappings should look like the following images.</span></span>

![Úkol pracovníci pracovníkovi](./media/WorkerMapping.png)

![Transformace pole pohlaví](./media/WorkerTransform.png)
