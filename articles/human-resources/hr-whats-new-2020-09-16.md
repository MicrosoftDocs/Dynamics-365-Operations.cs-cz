---
title: Co je nového nebo upraveného v aplikaci Dynamics 365 Human Resources (16. září 2020)
description: Tohle téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Human Resources k 16. září 2020.
author: jcart1106
manager: tfehr
ms.date: 09/16/2020
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
ms.author: jcart
ms.search.validFrom: 2020-09-16
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 14a4c08b0d223bc7fd8044354f5976388af9176b
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467450"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-16-2020"></a><span data-ttu-id="f26c0-103">Co je nového nebo upraveného v aplikaci Dynamics 365 Human Resources (16. září 2020)</span><span class="sxs-lookup"><span data-stu-id="f26c0-103">What's new or changed in Dynamics 365 Human Resources (September 16, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="f26c0-104">Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="f26c0-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="f26c0-105">Změny se vztahují na sestavení číslo 8.1.3557.</span><span class="sxs-lookup"><span data-stu-id="f26c0-105">Changes apply to build number 8.1.3557.</span></span> <span data-ttu-id="f26c0-106">Čísla v závorkách vedle některých funkcí se vztahují na čísla podpory pro referenci v Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="f26c0-106">The numbers in parentheses next to some features refer to Lifecycle Services (LCS) support numbers for reference.</span></span>

## <a name="included-in-this-release"></a><span data-ttu-id="f26c0-107">Zahrnuté do této verze</span><span class="sxs-lookup"><span data-stu-id="f26c0-107">Included in this release</span></span>

-  [<span data-ttu-id="f26c0-108">Uložená zobrazení - obecná dostupnost</span><span class="sxs-lookup"><span data-stu-id="f26c0-108">Saved views - general availability</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability)<br><span data-ttu-id="f26c0-109">- Další informace naleznete v tématu [Uložená zobrazení](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/saved-views).</span><span class="sxs-lookup"><span data-stu-id="f26c0-109">- For more information, see [Saved views](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/saved-views).</span></span> 

- <span data-ttu-id="f26c0-110">Formulář **Akce polohy** má aktualizovanou mřížku dimenzí a nové dialogové okno (469495).</span><span class="sxs-lookup"><span data-stu-id="f26c0-110">The **Position actions** form has an updated dimensions grid and new dialogue (469495).</span></span>

- <span data-ttu-id="f26c0-111">Pokud nastavíte **Omezte přístup k informacím o pracovníkovi** na ano v možnosti **Rozšířený přístup** v **Sdílené parametry lidských zdrojů**, formuláře zaměstnaneckých výhod nyní zobrazují pouze příslušné pracovníky (393384).</span><span class="sxs-lookup"><span data-stu-id="f26c0-111">If you set **Restrict access to worker information** to yes in **Advanced access** in **Human Resources Shared parameters**, benefits forms now show only the appropriate workers (393384).</span></span>

- <span data-ttu-id="f26c0-112">Nové možnosti generování kalendáře v entitě **WorkCalendar** (477055):</span><span class="sxs-lookup"><span data-stu-id="f26c0-112">New calendar generation options in the **WorkCalendar** entity (477055):</span></span><br><span data-ttu-id="f26c0-113">- Výchozí čas ukončení</span><span class="sxs-lookup"><span data-stu-id="f26c0-113">- Default ending time</span></span><br><span data-ttu-id="f26c0-114">- Výchozí čas zahájení</span><span class="sxs-lookup"><span data-stu-id="f26c0-114">-    Default starting time</span></span><br><span data-ttu-id="f26c0-115">- Je pátek pracovní den</span><span class="sxs-lookup"><span data-stu-id="f26c0-115">-  Is Friday working day</span></span><br><span data-ttu-id="f26c0-116">- Je pondělí pracovní den</span><span class="sxs-lookup"><span data-stu-id="f26c0-116">-  Is Monday working day</span></span><br><span data-ttu-id="f26c0-117">- Je sobota pracovní den</span><span class="sxs-lookup"><span data-stu-id="f26c0-117">-  Is Saturday working day</span></span><br><span data-ttu-id="f26c0-118">- Je neděle pracovní den</span><span class="sxs-lookup"><span data-stu-id="f26c0-118">- Is Sunday working day</span></span><br><span data-ttu-id="f26c0-119">- Je čtvrtek pracovní den</span><span class="sxs-lookup"><span data-stu-id="f26c0-119">- Is Thursday working day</span></span><br><span data-ttu-id="f26c0-120">- Je úterý pracovní den</span><span class="sxs-lookup"><span data-stu-id="f26c0-120">- Is Tuesday working day</span></span><br><span data-ttu-id="f26c0-121">- Je středa pracovní den</span><span class="sxs-lookup"><span data-stu-id="f26c0-121">- Is Wednesday working day</span></span><br><span data-ttu-id="f26c0-122">- ID svátku pracovního kalendáře</span><span class="sxs-lookup"><span data-stu-id="f26c0-122">- Work calendar holiday ID</span></span>

- <span data-ttu-id="f26c0-123">Entita **LeaveBankTransactionV1** nyní obsahuje kód příčiny (477823).</span><span class="sxs-lookup"><span data-stu-id="f26c0-123">The **LeaveBankTransactionV1** entity now includes the reason code (477823).</span></span>

- <span data-ttu-id="f26c0-124">Nyní můžete ukládat záznamy úkolů (492923).</span><span class="sxs-lookup"><span data-stu-id="f26c0-124">You can now save task recordings (492923).</span></span>

- <span data-ttu-id="f26c0-125">Data jsou nyní úspěšně publikována z **HCMWorkerContactEntity** (427620).</span><span class="sxs-lookup"><span data-stu-id="f26c0-125">Data is now published successfully from **HCMWorkerContactEntity** (427620).</span></span>

- <span data-ttu-id="f26c0-126">Pevná záložka **Kompenzace** se nyní zobrazí pro typ pracovníka dodavatele ve formuláři **Akce pracovníků** (482494).</span><span class="sxs-lookup"><span data-stu-id="f26c0-126">The **Compensation** fast tab now displays for the contractor worker type in the **Worker actions** form (482494).</span></span>

- <span data-ttu-id="f26c0-127">Pole **Úroveň** a **Plán** jsou nyní povinná, pokud nastavíte **Pevná kompenzace**.</span><span class="sxs-lookup"><span data-stu-id="f26c0-127">The **Level** and **Plan** fields are now mandatory if you set **Fixed compensation**.</span></span> <span data-ttu-id="f26c0-128">Pokud necháte tato pole nevyplněná (482497), zobrazí se chybová zpráva.</span><span class="sxs-lookup"><span data-stu-id="f26c0-128">An error message displays if you leave these fields blank (482497).</span></span>

- <span data-ttu-id="f26c0-129">Pole **Typ plánu** v položce **Zaměstnanecké výhody** je nyní rozevírací seznam (488768).</span><span class="sxs-lookup"><span data-stu-id="f26c0-129">The **Plan type** field in **Benefits** is now a dropdown list (488768).</span></span>

- <span data-ttu-id="f26c0-130">Správci systému nyní dostanou oznámení, pokud je vlastní pole odstraněno z Human Resources (481408).</span><span class="sxs-lookup"><span data-stu-id="f26c0-130">System administrators now receive a notification if a custom field is deleted from Human Resources (481408).</span></span>

- <span data-ttu-id="f26c0-131">Během procesu ukončení zaměstnance se Human Resources chová podle očekávání a po zdání uzamčení nezmění vybranou společnost (479877).</span><span class="sxs-lookup"><span data-stu-id="f26c0-131">During the terminate employee process, Human Resources behaves as expected and doesn't change the selected company after appearing to lock (479877).</span></span> 

- <span data-ttu-id="f26c0-132">Manažeři již nemohou přidat sloupec s číslem prostřednictvím personalizace (485317).</span><span class="sxs-lookup"><span data-stu-id="f26c0-132">Managers can no longer add a number column through personalization (485317).</span></span>

- <span data-ttu-id="f26c0-133">Manažeři již nemohou odstranit filtr datového rozsahu z vypršení platnosti identifikačních čísel (485321).</span><span class="sxs-lookup"><span data-stu-id="f26c0-133">Managers can no longer remove the data range filter from identification numbers expiring (485321).</span></span>

- <span data-ttu-id="f26c0-134">Když je pole **Nadřízená pozice** je prázdné, podrobnosti o pozici se stále zobrazují, když umístíte ukazatel myši na pozici (433328).</span><span class="sxs-lookup"><span data-stu-id="f26c0-134">When the **Reports to** field is empty, position details still display when hovering over the position (433328).</span></span>

- <span data-ttu-id="f26c0-135">Zaměstnanci si nyní mohou zobrazit informace o plánu výhod v samoobslužné službě pro zaměstnance (481676).</span><span class="sxs-lookup"><span data-stu-id="f26c0-135">Employees can now view benefit plan information in Employee self service (481676).</span></span>

- <span data-ttu-id="f26c0-136">Zaměstnanci nyní mohou zobrazit všechny registrované kurzy (429048).</span><span class="sxs-lookup"><span data-stu-id="f26c0-136">Employees can now see all registered courses (429048).</span></span>

- <span data-ttu-id="f26c0-137">Nyní můžete omezit možnosti zobrazení pro stránku **Profesionální certifikáty**.</span><span class="sxs-lookup"><span data-stu-id="f26c0-137">You can now restrict viewing options for the **Professional certificates** page.</span></span> <span data-ttu-id="f26c0-138">Možnosti zobrazení můžete omezit na aktuální právnickou osobu, podle stavu pracovníka a podle typu pracovníka (451501).</span><span class="sxs-lookup"><span data-stu-id="f26c0-138">You can restrict viewing options to the current legal entity, by worker status, and by worker type (451501).</span></span> 


## <a name="in-preview"></a><span data-ttu-id="f26c0-139">Náhled</span><span class="sxs-lookup"><span data-stu-id="f26c0-139">In Preview</span></span>

### <a name="human-resources-app-in-teams"></a><span data-ttu-id="f26c0-140">Aplikace Human Resources v Teams</span><span class="sxs-lookup"><span data-stu-id="f26c0-140">Human Resources app in Teams</span></span>

<span data-ttu-id="f26c0-141">Zaměstnanci mohou prohlížet a požadovat pracovní volno v rámci Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="f26c0-141">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="f26c0-142">Mohou interagovat s robotem a vytvářet žádosti o dovolenou.</span><span class="sxs-lookup"><span data-stu-id="f26c0-142">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="f26c0-143">Další informace naleznete zde:</span><span class="sxs-lookup"><span data-stu-id="f26c0-143">For more information, see:</span></span>

- <span data-ttu-id="f26c0-144">[Dovolená a nepřítomnost zaměstnanců v Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) v plánu 1. vlny vydání v Dynamics 365 2020</span><span class="sxs-lookup"><span data-stu-id="f26c0-144">[Employee leave and absence experience in Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 1 plan</span></span>
- <span data-ttu-id="f26c0-145">[Aplikace Human Resources v Teams](https://go.microsoft.com/fwlink/?linkid=2127841) v dokumentaci k Human Resources</span><span class="sxs-lookup"><span data-stu-id="f26c0-145">[Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841) in Human Resources documentation</span></span>

### <a name="human-resources-app-in-teams-preview-features"></a><span data-ttu-id="f26c0-146">Funkce preview aplikace Human Resources v Teams</span><span class="sxs-lookup"><span data-stu-id="f26c0-146">Human Resources app in Teams preview features</span></span>
 
-  <span data-ttu-id="f26c0-147">**Oznámení**: Odesílatelé a schvalovatelé žádostí o volno budou upozorněni v aplikaci Human Resources v Teams.</span><span class="sxs-lookup"><span data-stu-id="f26c0-147">**Notifications**: Submitters and approvers of time-off requests will be notified in the Human Resources app in Teams.</span></span> <span data-ttu-id="f26c0-148">Schvalovatelé mohou schválit nebo zamítnout žádosti o volno.</span><span class="sxs-lookup"><span data-stu-id="f26c0-148">Approvers can approve or deny time-off requests.</span></span> <span data-ttu-id="f26c0-149">Odesílatelé budou upozorněni, pokud byl požadavek schválen nebo zamítnut.</span><span class="sxs-lookup"><span data-stu-id="f26c0-149">Submitters will be notified if the request was approved or denied.</span></span> <span data-ttu-id="f26c0-150">Další informace naleznete zde:</span><span class="sxs-lookup"><span data-stu-id="f26c0-150">For more information, see:</span></span>
   - <span data-ttu-id="f26c0-151">[Dovolená a nepřítomnost zaměstnanců v Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) v plánu 2. vlny vydání v Dynamics 365 2020</span><span class="sxs-lookup"><span data-stu-id="f26c0-151">[Employee leave and absence experience in Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 2 plan</span></span>
   - <span data-ttu-id="f26c0-152">[Povolení oznámení pro aplikaci Human Resources v Teams](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#enable-notifications-for-the-human-resources-app-in-teams) v dokumentaci k Human Resources</span><span class="sxs-lookup"><span data-stu-id="f26c0-152">[Enable notifications for the Human Resources app in Teams](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#enable-notifications-for-the-human-resources-app-in-teams) in Human Resources documentation</span></span>
   - <span data-ttu-id="f26c0-153">[Zapnutí nebo vypnutí oznámení aplikace Teams pro jednotlivé uživatele](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#turn-teams-notifications-on-or-off-for-individual-users) v dokumentaci k Human Resources</span><span class="sxs-lookup"><span data-stu-id="f26c0-153">[Turn Teams notifications on or off for individual users](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#turn-teams-notifications-on-or-off-for-individual-users) in Human Resources documentation</span></span>
   - <span data-ttu-id="f26c0-154">[Oznámení aplikace Teams](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#teams-notifications) v dokumentaci k Human Resources</span><span class="sxs-lookup"><span data-stu-id="f26c0-154">[Teams notifications](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#teams-notifications) in Human Resources documentation</span></span>
   - <span data-ttu-id="f26c0-155">[Zobrazení kalendáře pracovního volna vašeho týmu](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar) v dokumentaci k Human Resources</span><span class="sxs-lookup"><span data-stu-id="f26c0-155">[View your team's leave calendar](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar) in Human Resources documentation</span></span>
 
- <span data-ttu-id="f26c0-156">**Kalendář volna manažera**: Manažeři mohou vidět schválené a nevyřízené volno pro jejich přímé podřízené v zobrazení kalendáře.</span><span class="sxs-lookup"><span data-stu-id="f26c0-156">**Manager time-off calendar**: Managers can see approved and pending time off for their direct reports in a calendar view.</span></span> <span data-ttu-id="f26c0-157">Tohle zobrazení umožňuje snadné pochopení, kdy jsou členové jejich týmu mimo práci.</span><span class="sxs-lookup"><span data-stu-id="f26c0-157">This view provides an easy understanding of when their team members are away from work.</span></span> <span data-ttu-id="f26c0-158">Další informace naleznete zde:</span><span class="sxs-lookup"><span data-stu-id="f26c0-158">For more information, see:</span></span>
   - <span data-ttu-id="f26c0-159">[Dovolená a nepřítomnost zaměstnanců v Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) v plánu 2. vlny vydání v Dynamics 365 2020</span><span class="sxs-lookup"><span data-stu-id="f26c0-159">[Employee leave and absence experience in Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) in the Dynamics 365 2020 release wave 2 plan</span></span>
   - <span data-ttu-id="f26c0-160">[Zobrazení kalendáře pracovního volna vašeho týmu](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar) v dokumentaci k Human Resources</span><span class="sxs-lookup"><span data-stu-id="f26c0-160">[View your team's leave calendar](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar) in Human Resources documentation</span></span>

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a><span data-ttu-id="f26c0-161">Možnost konfigurace pro umístění seznamu Pracovní položky přiřazené mně (477004)</span><span class="sxs-lookup"><span data-stu-id="f26c0-161">Configuration option to position Work items assigned to me list (477004)</span></span>

<span data-ttu-id="f26c0-162">Nyní je k dispozici nová možnost umístění seznamu **Pracovní položky přiřazené mně** v pravém sloupci řídicího panelu.</span><span class="sxs-lookup"><span data-stu-id="f26c0-162">A new option is now available to position the **Work items assigned to me** list in the right-hand column of the dashboard.</span></span> <span data-ttu-id="f26c0-163">S touto změnou se všechny pracovní položky a seznamy úkolů zobrazí ve stejné oblasti.</span><span class="sxs-lookup"><span data-stu-id="f26c0-163">With this change, all work items and to do lists display in the same area.</span></span> <span data-ttu-id="f26c0-164">Povolte tuto funkci zapnutím funkce **Preview – Vylepšené prostředí pracovního postupu** ve správě funkcí.</span><span class="sxs-lookup"><span data-stu-id="f26c0-164">Enable this functionality by turning on **Preview - Workflow experience enhancements** in Feature management.</span></span> <span data-ttu-id="f26c0-165">Další informace o zapnutí funkcí Preview naleznete v tématu [Správa funkcí](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="f26c0-165">For more information about turning on preview features, see [Manage features](hr-admin-manage-features.md).</span></span>

<span data-ttu-id="f26c0-166">Tato funkce také podporuje možnosti pracovního postupu, které se zobrazují ve formulářích akcí personálu.</span><span class="sxs-lookup"><span data-stu-id="f26c0-166">This feature also promotes the workflow options that appear in the personnel actions forms.</span></span> <span data-ttu-id="f26c0-167">Možnosti pracovního postupu se také zobrazují nad pevnou záložkou akce pro rychlý přístup.</span><span class="sxs-lookup"><span data-stu-id="f26c0-167">Workflow options also appear above the action fast tab for quick access.</span></span> <span data-ttu-id="f26c0-168">Další informace naleznete zde:</span><span class="sxs-lookup"><span data-stu-id="f26c0-168">For more information, see:</span></span> 

- <span data-ttu-id="f26c0-169">[Vylepšení prostředí pracovního postupu pro správu organizace a personálu](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) v plánu Dynamics 365 2020 2. vlna vydání</span><span class="sxs-lookup"><span data-stu-id="f26c0-169">[Organization and personnel management workflow experience enhancements](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) in the Dynamics 365 2020 release wave 2 plan</span></span>

![Pracovní položky přiřazené mně](./media/hr-workflow-work-items-assigned-to-me.png)

![Rychlý přístup k položkám pracovního postupu](./media/hr-workflow-quick-access.png)

### <a name="leave-and-absence-calendar"></a><span data-ttu-id="f26c0-172">Kalendář pracovního volna a absence</span><span class="sxs-lookup"><span data-stu-id="f26c0-172">Leave and absence calendar</span></span>

<span data-ttu-id="f26c0-173">Toto vydání obsahuje další možnosti kalendáře pro kalendáře dovolené a nepřítomnosti.</span><span class="sxs-lookup"><span data-stu-id="f26c0-173">This release includes additional calendar options for leave and absence calendars.</span></span> <span data-ttu-id="f26c0-174">Další informace naleznete v tématu [Zobrazení kalendáře týmu a společnosti](https://docs.microsoft.com/dynamics365/human-resources/hr-employee-self-service-calendar).</span><span class="sxs-lookup"><span data-stu-id="f26c0-174">For more information, see [View team and company calendars](https://docs.microsoft.com/dynamics365/human-resources/hr-employee-self-service-calendar).</span></span>

## <a name="coming-soon"></a><span data-ttu-id="f26c0-175">Již brzy</span><span class="sxs-lookup"><span data-stu-id="f26c0-175">Coming Soon</span></span>

### <a name="checklist-entities-included-in-dataverse"></a><span data-ttu-id="f26c0-176">Položky kontrolního seznamu zahrnuté do Dataverse</span><span class="sxs-lookup"><span data-stu-id="f26c0-176">Checklist entities included in Dataverse</span></span>

<span data-ttu-id="f26c0-177">Položky kontrolního seznamu pro onboarding, offboarding, převody a obchodní procesy budou v systému Dataverse k dispozici již brzy.</span><span class="sxs-lookup"><span data-stu-id="f26c0-177">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Dataverse.</span></span>

### <a name="benefits-management-reason-codes"></a><span data-ttu-id="f26c0-178">Kódy důvodů správy zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="f26c0-178">Benefits management reason codes</span></span>

<span data-ttu-id="f26c0-179">Kódy důvodů správy zaměstnaneckých výhod budou brzy kombinovány se stávajícími kódy důvodů v aplikaci Human Resources.</span><span class="sxs-lookup"><span data-stu-id="f26c0-179">Benefits management reason codes will soon be combined with existing reason codes in Human Resources.</span></span> <span data-ttu-id="f26c0-180">Pokud jste ve správě zaměstnaneckých výhod vytvořili kódy důvodů, které mají více než 15 znaků, musíte ve správě zaměstnaneckých výhod změnit název kódu důvodu. Formulář **Kódy důvodů** může mít 15 znaků nebo méně.</span><span class="sxs-lookup"><span data-stu-id="f26c0-180">If you created reason codes in Benefits management that are over 15 characters, you must change the name of the reason code in the Benefits management **Reason codes** form to be 15 characters or less.</span></span> <span data-ttu-id="f26c0-181">Po aktualizaci názvu se kód důvodu zobrazí pod existujícím formulářem kódu důvodu ve správě personálu.</span><span class="sxs-lookup"><span data-stu-id="f26c0-181">After you update the name, the reason code will appear under the existing reason code form in Personnel management.</span></span> <span data-ttu-id="f26c0-182">Tato změna bude k dispozici v budoucnu a nebude mít vliv na stávající funkčnost.</span><span class="sxs-lookup"><span data-stu-id="f26c0-182">This change will be available in the future and won't affect existing functionality.</span></span>

## <a name="see-also"></a><span data-ttu-id="f26c0-183">Viz také</span><span class="sxs-lookup"><span data-stu-id="f26c0-183">See also</span></span>

[<span data-ttu-id="f26c0-184">Co je nového a co se změnilo v Human Resources</span><span class="sxs-lookup"><span data-stu-id="f26c0-184">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="f26c0-185">Přehled produktu Dynamics 365 Human Resources vydání 2019 vlny 2</span><span class="sxs-lookup"><span data-stu-id="f26c0-185">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="f26c0-186">Aktualizace procesu</span><span class="sxs-lookup"><span data-stu-id="f26c0-186">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="f26c0-187">Správa funkcí</span><span class="sxs-lookup"><span data-stu-id="f26c0-187">Manage features</span></span>](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]