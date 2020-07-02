---
title: Co je nového nebo změněného v aplikaci Dynamics 365 Human Resources (28. května 2020)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c386025843edef83d229a42d3f2314678fadae20
ms.sourcegitcommit: beddfba095c23b3265f0004f5124c4e9dc6404cc
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411923"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-28-2020"></a><span data-ttu-id="6829b-103">Co je nového nebo změněného v aplikaci Dynamics 365 Human Resources (28. května 2020)</span><span class="sxs-lookup"><span data-stu-id="6829b-103">What's new or changed in Dynamics 365 Human Resources (May 28, 2020)</span></span>

<span data-ttu-id="6829b-104">Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="6829b-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="6829b-105">Změny se vztahují na sestavení číslo 8.1.3287.</span><span class="sxs-lookup"><span data-stu-id="6829b-105">Changes apply to build number 8.1.3287.</span></span> <span data-ttu-id="6829b-106">Čísla v závorkách v některých záhlavích se vztahují na čísla podpory v Lifecycle Services (LCS) pro referenci.</span><span class="sxs-lookup"><span data-stu-id="6829b-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="leaverequest-entity-doesnt-work-when-you-enable-multiple-types-per-leave-plan-447498"></a><span data-ttu-id="6829b-107">Entita LeaveRequest nefunguje, když povolíte více typů plánů volna (447498)</span><span class="sxs-lookup"><span data-stu-id="6829b-107">LeaveRequest entity doesn't work when you enable multiple types per leave plan (447498)</span></span>

<span data-ttu-id="6829b-108">S touto změnou **LeaveEnrollmentV2Entity** je nyní k dispozici k opravě chyby, ke které dochází, když povolíte více typů dovolené.</span><span class="sxs-lookup"><span data-stu-id="6829b-108">With this change, the **LeaveEnrollmentV2Entity** is now available to correct the error that occurs when you enable multiple leave types.</span></span>

## <a name="batch-contention-reduction-feature-preview-446619"></a><span data-ttu-id="6829b-109">Funkce omezení obsahu dávky (náhled) (446619)</span><span class="sxs-lookup"><span data-stu-id="6829b-109">Batch contention reduction feature (preview) (446619)</span></span>

<span data-ttu-id="6829b-110">Pokud tuto funkci povolíte, můžete při výběru úkolů a dokončení úloh očekávat snížení blokování v tabulkách dávkových rámců.</span><span class="sxs-lookup"><span data-stu-id="6829b-110">When you enable this feature, you can expect a reduction in blocking on batch framework tables while selecting tasks and finishing jobs.</span></span>

## <a name="updateconflict-while-saving-worker-prevents-editing-a-record-in-people-427915"></a><span data-ttu-id="6829b-111">UpdateConflict při ukládání pracovníka zabraňuje úpravám záznamu v aplikaci People (427915)</span><span class="sxs-lookup"><span data-stu-id="6829b-111">UpdateConflict while saving worker prevents editing a record in People (427915)</span></span>

<span data-ttu-id="6829b-112">Tato změna opravuje chybu při přidávání nového pracovníka, aktualizaci informací o adrese a změně jazykových preferencí.</span><span class="sxs-lookup"><span data-stu-id="6829b-112">This change corrects an error when adding a new worker, updating address information, and changing language preference.</span></span> <span data-ttu-id="6829b-113">V tomto jedinečném scénáři se zobrazila chyba označující, že záznam nelze aktualizovat.</span><span class="sxs-lookup"><span data-stu-id="6829b-113">In this unique scenario, an error displayed indicating the record couldn't be updated.</span></span> 

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-to-resubmit-425407"></a><span data-ttu-id="6829b-114">Nelze přidat přílohu ke schválené žádosti o pracovní volno a znovu ji odeslat (425407)</span><span class="sxs-lookup"><span data-stu-id="6829b-114">Unable to add an attachment to an approved leave request to resubmit (425407)</span></span>

<span data-ttu-id="6829b-115">Tato změna nyní umožňuje přílohy ke schváleným žádostem o dovolenou.</span><span class="sxs-lookup"><span data-stu-id="6829b-115">This change now allows attachments to approved leave requests.</span></span>

## <a name="user-can-enter-compensation-for-an-employee-in-a-different-legal-entity-form-409529"></a><span data-ttu-id="6829b-116">Uživatel může zadat náhradu za zaměstnance v jiném formuláři právnické osoby (409529)</span><span class="sxs-lookup"><span data-stu-id="6829b-116">User can enter compensation for an employee in a different legal entity form (409529)</span></span>

<span data-ttu-id="6829b-117">Tato změna zakáže možnosti kompenzace, aby se zabránilo neúmyslnému zápisu záznamů o kompenzaci pro nesprávnou právnickou osobu.</span><span class="sxs-lookup"><span data-stu-id="6829b-117">This change disables compensation options to prevent inadvertent entry of compensation records for the wrong legal entity.</span></span>

## <a name="error-when-you-transfer-an-employee-and-the-worker-position-assignment-date-is-before-the-position-duration-429402"></a><span data-ttu-id="6829b-118">Chyba při převodu zaměstnance a datum přiřazení pracovní pozice je před trváním pozice (429402)</span><span class="sxs-lookup"><span data-stu-id="6829b-118">Error when you transfer an employee and the Worker position assignment date is before the position duration (429402)</span></span>

<span data-ttu-id="6829b-119">Chybové zprávy při převodu zaměstnance v tomto scénáři byly aktualizovány, aby lépe popisovaly změny potřebné k odstranění problému.</span><span class="sxs-lookup"><span data-stu-id="6829b-119">Error messages when transferring an employee in this scenario have been updated to better describe the changes needed to correct the problem.</span></span>

## <a name="attachments-capabilities-in-employee-self-service-benefits-enrollment"></a><span data-ttu-id="6829b-120">Funkce příloh v samoobslužném zápisu zaměstnaneckých výhod zaměstnance</span><span class="sxs-lookup"><span data-stu-id="6829b-120">Attachments capabilities in Employee self service benefits enrollment</span></span>
 
<span data-ttu-id="6829b-121">Nyní můžete přidávat přílohy během procesu zápisu výhod pro každý plán, do kterého se zaměstnanec zapisuje.</span><span class="sxs-lookup"><span data-stu-id="6829b-121">Now you can add attachments during the benefits enrollment process for each plan that the employee's enrolling in.</span></span> <span data-ttu-id="6829b-122">Poté si můžete zobrazit přílohy ve formuláři **Registrované zaměstnanecké výhody pracovníka**.</span><span class="sxs-lookup"><span data-stu-id="6829b-122">You can then view the attachments within the **Worker enrolled benefit** form.</span></span>

## <a name="in-preview"></a><span data-ttu-id="6829b-123">Náhled</span><span class="sxs-lookup"><span data-stu-id="6829b-123">In preview</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="6829b-124">Aplikace Human Resources v Teams</span><span class="sxs-lookup"><span data-stu-id="6829b-124">Human Resources application in Teams</span></span>

<span data-ttu-id="6829b-125">Zaměstnanci mohou prohlížet a požadovat pracovní volno v rámci Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="6829b-125">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="6829b-126">Mohou interagovat s robotem a vytvářet žádosti o dovolenou.</span><span class="sxs-lookup"><span data-stu-id="6829b-126">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="6829b-127">Další informace viz [Aplikace Human Resources v Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span><span class="sxs-lookup"><span data-stu-id="6829b-127">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="leave-suspension"></a><span data-ttu-id="6829b-128">Pozastavit pracovní volno</span><span class="sxs-lookup"><span data-stu-id="6829b-128">Leave suspension</span></span>

<span data-ttu-id="6829b-129">Můžete přerušit pracovní volno a absenci v Human Resources pro zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="6829b-129">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="6829b-130">Pozastavením volna se zastaví časové rozlišení volna pro vybrané typy pracovního volna.</span><span class="sxs-lookup"><span data-stu-id="6829b-130">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="6829b-131">Pokud k přerušení dojde po zpracování časového rozlišení, pozastavením volna se vytvoří průběžná Úprava zůstatku zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="6829b-131">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="6829b-132">Další informace naleznete v části [Přerušení pracovního volna](hr-leave-and-absence-suspend-leave.md).</span><span class="sxs-lookup"><span data-stu-id="6829b-132">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a><span data-ttu-id="6829b-133">Aktualizujte uživatelské prostředí, abyste naznačili, že akruální účet je pozastaven (429550)</span><span class="sxs-lookup"><span data-stu-id="6829b-133">Update user experience to indicate that accrual is suspended (429550)</span></span>

<span data-ttu-id="6829b-134">Uživatelská zkušenost nyní naznačuje, že přírůstek byl pro plán pozastaven.</span><span class="sxs-lookup"><span data-stu-id="6829b-134">The user experience now indicates that the accrual has been suspended for a plan.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="6829b-135">Již brzy</span><span class="sxs-lookup"><span data-stu-id="6829b-135">Coming soon</span></span>

## <a name="database-logging-in-preview-in-june"></a><span data-ttu-id="6829b-136">Protokolování databáze (v náhledu v červnu)</span><span class="sxs-lookup"><span data-stu-id="6829b-136">Database logging (in preview in June)</span></span>

<span data-ttu-id="6829b-137">Funkce protokolování databáze umožňuje určit, které tabulky a pole mají být monitorovány.</span><span class="sxs-lookup"><span data-stu-id="6829b-137">The database logging feature allows you to determine which table and fields should be monitored.</span></span> <span data-ttu-id="6829b-138">Umožňuje také určit události, které by měly spustit sledování změn.</span><span class="sxs-lookup"><span data-stu-id="6829b-138">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="6829b-139">K dispozici jsou možnosti dotazů, které tyto změny v průběhu času uvidí.</span><span class="sxs-lookup"><span data-stu-id="6829b-139">Inquiry capabilities are available to see these changes over time.</span></span>

## <a name="buy-and-sell-leave-in-preview-june-1"></a><span data-ttu-id="6829b-140">Koupit a prodat volno (v náhledu 1. června)</span><span class="sxs-lookup"><span data-stu-id="6829b-140">Buy and sell leave (in preview June 1)</span></span>

<span data-ttu-id="6829b-141">Některé organizace poskytují výhodu, která zaměstnancům umožňuje nakupovat nebo prodávat dovolenou.</span><span class="sxs-lookup"><span data-stu-id="6829b-141">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="6829b-142">Tento proces je často řízen ručně.</span><span class="sxs-lookup"><span data-stu-id="6829b-142">This process is often managed manually.</span></span> <span data-ttu-id="6829b-143">Tato funkce poskytuje automatizovanější způsob správy zásad a požadavků oddělení lidských zdrojů a pomáhá eliminovat chyby a zefektivnit proces správy dovolené.</span><span class="sxs-lookup"><span data-stu-id="6829b-143">This feature provides a more automated way to manage policies and requests for the HR department, and it helps eliminate mistakes while streamlining the leave management process.</span></span>

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="6829b-144">Entity právy datových rámců (DMF) pro správu zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="6829b-144">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="6829b-145">Zvýhodněné účetní jednotky se uvolňují.</span><span class="sxs-lookup"><span data-stu-id="6829b-145">Benefits management entities are releasing.</span></span> <span data-ttu-id="6829b-146">Entity DMF umožňují import a export dat pro snadnou konfiguraci správy výhod.</span><span class="sxs-lookup"><span data-stu-id="6829b-146">DMF entities allow importing and exporting data to easily configure benefits management.</span></span> <span data-ttu-id="6829b-147">K přesunutí dat bude k dispozici také šablona správy výhod.</span><span class="sxs-lookup"><span data-stu-id="6829b-147">A Benefits management template will also be available to move data.</span></span> <span data-ttu-id="6829b-148">Šablona exportuje a importuje data sekvenčním způsobem, aby respektovala datové závislosti.</span><span class="sxs-lookup"><span data-stu-id="6829b-148">The template exports and imports the data in a sequential manner to respect data dependencies.</span></span>

## <a name="add-reason-code-to-accrual-suspensions-june-1"></a><span data-ttu-id="6829b-149">Přidejte kód příčiny pro akruální pozastavení (1. červen)</span><span class="sxs-lookup"><span data-stu-id="6829b-149">Add reason code to accrual suspensions (June 1)</span></span>

<span data-ttu-id="6829b-150">K akruálnímu pozastavení byly přidány kódy důvodů.</span><span class="sxs-lookup"><span data-stu-id="6829b-150">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules-june-1"></a><span data-ttu-id="6829b-151">Pravidla pro převod do dalšího období (1. červen)</span><span class="sxs-lookup"><span data-stu-id="6829b-151">Carry forward rules (June 1)</span></span>

<span data-ttu-id="6829b-152">Můžete určit typ převodu pracovního volna do dalšího období pro převod zůstatků, kde byly převedeny úpravy převodu do dalšího období.</span><span class="sxs-lookup"><span data-stu-id="6829b-152">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="6829b-153">Pokud například zaměstnanec přenese deset dní dopředu, můžete pro tyto 10 dny vybrat jiný typ pracovního volna.</span><span class="sxs-lookup"><span data-stu-id="6829b-153">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="6829b-154">Další informace naleznete v tématu [Konfigurace typů pracovního volna a absence](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="6829b-154">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types-june-1"></a><span data-ttu-id="6829b-155">Pozastavení časového limitu pro vybrané typy dovolené (1. červen)</span><span class="sxs-lookup"><span data-stu-id="6829b-155">Suspend leave accrual for specified leave types (June 1)</span></span>

<span data-ttu-id="6829b-156">V této verzi může HR vytvořit pravidlo pro pozastavení přírůstků dovolené pro zaměstnance s požadavky na dovolenou zadanými pro neplacenou dovolenou.</span><span class="sxs-lookup"><span data-stu-id="6829b-156">In this release, HR can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="6829b-157">Neplacená dovolená může být zadána, ale nemusí.</span><span class="sxs-lookup"><span data-stu-id="6829b-157">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="6829b-158">Dovolenou můžete pozastavit na základě jiného typu dovolené.</span><span class="sxs-lookup"><span data-stu-id="6829b-158">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions-june-1"></a><span data-ttu-id="6829b-159">Entita DMF je k dispozici pro akruální pozastavení (1. červen)</span><span class="sxs-lookup"><span data-stu-id="6829b-159">DMF entity available for accrual suspensions (June 1)</span></span>

<span data-ttu-id="6829b-160">Entita DMF je nyní k dispozici pro akruální pozastavení</span><span class="sxs-lookup"><span data-stu-id="6829b-160">A DMF entity is now available for accrual suspensions.</span></span>