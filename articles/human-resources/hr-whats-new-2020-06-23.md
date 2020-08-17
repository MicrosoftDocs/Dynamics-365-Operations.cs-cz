---
title: Co je nového a co se změnilo v aplikaci Dynamics 365 Human Resources (25. června 2020)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 06/25/2020
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
ms.search.validFrom: 2020-06-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fa02cf10b2b4fe08440d3641472e83dfe58169c9
ms.sourcegitcommit: 81296c49be9953aa01e15527c34d0ef13b4622a9
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/22/2020
ms.locfileid: "3614379"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-23-2020"></a><span data-ttu-id="92a64-103">Co je nového a co se změnilo v aplikaci Dynamics 365 Human Resources (23. června 2020)</span><span class="sxs-lookup"><span data-stu-id="92a64-103">What's new or changed in Dynamics 365 Human Resources (June 23, 2020)</span></span>

<span data-ttu-id="92a64-104">Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="92a64-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="92a64-105">Změny se vztahují na sestavení číslo 8.1.3347.</span><span class="sxs-lookup"><span data-stu-id="92a64-105">Changes apply to build number 8.1.3347.</span></span> <span data-ttu-id="92a64-106">Čísla v závorkách v některých záhlavích se vztahují na čísla podpory v Lifecycle Services (LCS) pro referenci.</span><span class="sxs-lookup"><span data-stu-id="92a64-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="when-an-enrollment-is-expired-for-a-terminated-employee-the-leave-type-balance-and-amount-are-all-cleared-in-the-leave-enrollment-form-444867"></a><span data-ttu-id="92a64-107">Když skončí platnost prováděcí smlouvy zaměstnance po rozvázání pracovního poměru, položky typ dovolené, zůstatek a částka se z formuláře registrace dovolené vymažou (444867)</span><span class="sxs-lookup"><span data-stu-id="92a64-107">When an enrollment is expired for a terminated employee, the leave type, balance, and amount are all cleared in the Leave enrollment form (444867)</span></span>

<span data-ttu-id="92a64-108">Hodnoty v polích **Typ dovolené**, **Zůstatek** a **Množství** se nyní při provedení tohoto výběru zachovají (nebudou vymazány).</span><span class="sxs-lookup"><span data-stu-id="92a64-108">Values in the **Leave type**, **Balance**, and **Amount** are now maintained instead of cleared upon making this selection.</span></span>

## <a name="incorrect-forecasted-balance-when-new-feature-leave-accrual-for-a-single-company-or-a-single-plan-is-enabled-456553"></a><span data-ttu-id="92a64-109">Nesprávný odhadovaný zůstatek, když je aktivována nová funkce (Časové rozlišení pracovního volna pro jednu společnost nebo jeden plán) (456553)</span><span class="sxs-lookup"><span data-stu-id="92a64-109">Incorrect forecasted balance when new feature (Leave accrual for a single company or a single plan) is enabled (456553)</span></span>

<span data-ttu-id="92a64-110">Správný odhadovaný zůstatek se nyní zobrazí, když je aktivováno časové rozlišení pracovního volna pro jednu společnost nebo jeden plán.</span><span class="sxs-lookup"><span data-stu-id="92a64-110">The correct forecasted balance now displays when the leave accrual for a single company or single plan has been enabled.</span></span>

## <a name="entities-with-relations-that-result-in-duplicate-navigation-properties-456486"></a><span data-ttu-id="92a64-111">Subjekty se vztahy, které vedou k duplicitě navigačních vlastností (456486)</span><span class="sxs-lookup"><span data-stu-id="92a64-111">Entities with relations that result in duplicate navigation properties (456486)</span></span>

<span data-ttu-id="92a64-112">Tato vydaná verze opravuje problém s navigačními vlastnostmi (vztahy) více subjektů.</span><span class="sxs-lookup"><span data-stu-id="92a64-112">This release corrects an issue with the navigation properties (relation) of multiple entities.</span></span> <span data-ttu-id="92a64-113">Jsou detekovány duplicitní vztahy.</span><span class="sxs-lookup"><span data-stu-id="92a64-113">Duplicate relations are detected.</span></span> <span data-ttu-id="92a64-114">Všechny tyto scénáře byly opraveny.</span><span class="sxs-lookup"><span data-stu-id="92a64-114">These scenarios have all been corrected.</span></span>
 
## <a name="cross-company-comments-on-performance-review-455536"></a><span data-ttu-id="92a64-115">Mezipodnikové komentáře k přehledu výkonů (455536)</span><span class="sxs-lookup"><span data-stu-id="92a64-115">Cross-company comments on Performance review (455536)</span></span>

<span data-ttu-id="92a64-116">Po této opravě jsou nyní v přehledech výkonů viditelné mezipodnikové komentáře.</span><span class="sxs-lookup"><span data-stu-id="92a64-116">Cross-company comments are now visible on performance reviews with this fix.</span></span> <span data-ttu-id="92a64-117">Tato změna opravuje zobrazení komentářů kontrolora zadaných v různých společnostech v rámci stejné kontroly výkonu.</span><span class="sxs-lookup"><span data-stu-id="92a64-117">This change corrects the view of reviewer comments that were entered in different companies for the same performance review.</span></span>
 
## <a name="inconsistency-in-showing-compensation-management-data-432562"></a><span data-ttu-id="92a64-118">Nekonzistence při zobrazování údajů správy kompenzací (432562)</span><span class="sxs-lookup"><span data-stu-id="92a64-118">Inconsistency in showing compensation management data (432562)</span></span>

<span data-ttu-id="92a64-119">V samoobsluze pro manažery je nyní zachováno konzistentní zobrazení údajů o kompenzacích.</span><span class="sxs-lookup"><span data-stu-id="92a64-119">A consistent view of compensation data is now maintained in Manager self service.</span></span> <span data-ttu-id="92a64-120">V závislosti na tom, jak přejdete k **Podrobnostem o kompenzaci** pracovníka se nyní manažerům zobrazují údaje o kompenzaci konzistentně.</span><span class="sxs-lookup"><span data-stu-id="92a64-120">Depending on how you navigate to a worker's **Compensation details**, compensation data now consistently displays to managers.</span></span>
 
## <a name="fixed-compensation-plans-effective-date-defaults-to-todays-date-411994"></a><span data-ttu-id="92a64-121">Výchozí datum účinnosti plánu fixní kompenzace je dnešní datum (411994)</span><span class="sxs-lookup"><span data-stu-id="92a64-121">Fixed compensation plan's effective date defaults to today's date (411994)</span></span>

<span data-ttu-id="92a64-122">Počáteční datum kompenzace nyní vychází z počátečního data pozice, jež je zaměstnanci přiřazena.</span><span class="sxs-lookup"><span data-stu-id="92a64-122">The compensation start date is now based on the start date of the position being assigned to the employee.</span></span>

## <a name="leave-and-absence-form-enable-half-day-definition-is-disabled-when-form-opens-452607"></a><span data-ttu-id="92a64-123">Formulář pracovního volna a absence: při otevření formuláře je pole Povolit definici poloviny dne deaktivováno (452607)</span><span class="sxs-lookup"><span data-stu-id="92a64-123">Leave and absence form Enable half day definition is disabled when form opens (452607)</span></span>

<span data-ttu-id="92a64-124">Na základě této změny bude pole **Povolit definici poloviny dne** povoleno do doby vzniku nové transakce pracovního volna.</span><span class="sxs-lookup"><span data-stu-id="92a64-124">With this change, the **Enable half day definition** will be enabled until new leave transactions exist.</span></span> 

## <a name="unable-to-publish-to-hcmdiscussionentity-via-excel-totalratingscore-field-error-453899"></a><span data-ttu-id="92a64-125">Nelze publikovat do HcmDiscussionEntity prostřednictvím aplikace Excel; chyba pole TotalRatingScore (453899)</span><span class="sxs-lookup"><span data-stu-id="92a64-125">Unable to publish to HcmDiscussionEntity via Excel; TotalRatingScore field error (453899)</span></span>

<span data-ttu-id="92a64-126">Nyní můžete pole **TotalRatingScore** aktualizovat pomocí položky **HCMDiskuseEntity** v nástroji pro návrh sešitů Excel.</span><span class="sxs-lookup"><span data-stu-id="92a64-126">You can now update the **TotalRatingScore** field using **HCMDiscussionEntity** in the Excel workbook designer.</span></span>

## <a name="in-preview"></a><span data-ttu-id="92a64-127">Náhled</span><span class="sxs-lookup"><span data-stu-id="92a64-127">In preview</span></span>

## <a name="database-logging"></a><span data-ttu-id="92a64-128">Protokolování databáze</span><span class="sxs-lookup"><span data-stu-id="92a64-128">Database logging</span></span>

<span data-ttu-id="92a64-129">Protokolování databáze umožňuje určit, které tabulky a pole mají být monitorovány.</span><span class="sxs-lookup"><span data-stu-id="92a64-129">Database logging allows you to determine which tables and fields to monitor.</span></span> <span data-ttu-id="92a64-130">Umožňuje také určit události, které by měly spustit sledování změn.</span><span class="sxs-lookup"><span data-stu-id="92a64-130">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="92a64-131">Pomocí funkcí protokolování databáze se můžete podívat na tyto změny v průběhu času.</span><span class="sxs-lookup"><span data-stu-id="92a64-131">You use database logging capabilities to see these changes over time.</span></span> <span data-ttu-id="92a64-132">Další informace získáte v rématu [Konfigurace a správa protokolování databáze](hr-admin-database-logging.md).</span><span class="sxs-lookup"><span data-stu-id="92a64-132">For more information, see [Configure and manage database logging](hr-admin-database-logging.md).</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="92a64-133">Povinná pole</span><span class="sxs-lookup"><span data-stu-id="92a64-133">Mandatory fields</span></span> 

<span data-ttu-id="92a64-134">Nyní můžete změnit pole na povinná pomocí personalizačních funkcí systému lidských zdrojů.</span><span class="sxs-lookup"><span data-stu-id="92a64-134">You can now make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="92a64-135">Tato funkce vyžaduje **Uložená zobrazení**.</span><span class="sxs-lookup"><span data-stu-id="92a64-135">This feature requires **Saved views**.</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="92a64-136">Aplikace Human Resources v Teams</span><span class="sxs-lookup"><span data-stu-id="92a64-136">Human Resources application in Teams</span></span>

<span data-ttu-id="92a64-137">Zaměstnanci mohou prohlížet a požadovat pracovní volno v rámci Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="92a64-137">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="92a64-138">Mohou interagovat s robotem a vytvářet žádosti o dovolenou.</span><span class="sxs-lookup"><span data-stu-id="92a64-138">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="92a64-139">Další informace viz [Aplikace Human Resources v Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span><span class="sxs-lookup"><span data-stu-id="92a64-139">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="92a64-140">Entity právy datových rámců (DMF) pro správu zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="92a64-140">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="92a64-141">Zvýhodněné účetní jednotky se uvolňují.</span><span class="sxs-lookup"><span data-stu-id="92a64-141">Benefits management entities are releasing.</span></span> <span data-ttu-id="92a64-142">Entity DMF umožňují import a export dat pro snadnou konfiguraci správy výhod.</span><span class="sxs-lookup"><span data-stu-id="92a64-142">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="92a64-143">K přesunutí dat bude k dispozici šablona správy výhod.</span><span class="sxs-lookup"><span data-stu-id="92a64-143">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="92a64-144">Šablona exportuje a importuje data sekvenčně, aby respektovala datové závislosti.</span><span class="sxs-lookup"><span data-stu-id="92a64-144">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="92a64-145">Nákup a prodej pracovního volna</span><span class="sxs-lookup"><span data-stu-id="92a64-145">Buy and sell leave</span></span> 

<span data-ttu-id="92a64-146">Některé organizace poskytují výhodu, která zaměstnancům umožňuje nakupovat nebo prodávat dovolenou.</span><span class="sxs-lookup"><span data-stu-id="92a64-146">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="92a64-147">Tento proces je často řízen ručně.</span><span class="sxs-lookup"><span data-stu-id="92a64-147">This process is often managed manually.</span></span> <span data-ttu-id="92a64-148">Tato funkce automatizuje správu zásad a požadavků oddělení lidských zdrojů.</span><span class="sxs-lookup"><span data-stu-id="92a64-148">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="92a64-149">Usnadňuje proces správy dovolených a pomáhá eliminovat chyby.</span><span class="sxs-lookup"><span data-stu-id="92a64-149">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="92a64-150">Další informace naleznete zde:</span><span class="sxs-lookup"><span data-stu-id="92a64-150">For more information, see:</span></span>

- [<span data-ttu-id="92a64-151">Správa zásad nákupu a prodeje pracovního volna</span><span class="sxs-lookup"><span data-stu-id="92a64-151">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="92a64-152">Nákup a prodej pracovního volna</span><span class="sxs-lookup"><span data-stu-id="92a64-152">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="92a64-153">Časové rozlišení pracovního volna pro jednu společnost nebo jeden plán</span><span class="sxs-lookup"><span data-stu-id="92a64-153">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="92a64-154">Zákazníci mohou zpracovat časové rozlišení pro jednu společnost nebo jeden plán dovolené a nepřítomnosti.</span><span class="sxs-lookup"><span data-stu-id="92a64-154">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="92a64-155">Tato schopnost objasňuje proces časového rozlišení pro zákazníky s různými roky dovolené nebo zásadami časového rozlišení dovolené.</span><span class="sxs-lookup"><span data-stu-id="92a64-155">This ability provides clarity into the accrual process for customers with different leave years or leave accrual policies.</span></span> <span data-ttu-id="92a64-156">Další informace získáte v části [Časové rozlišení dovolené podle společnosti nebo plánu dovolených](hr-leave-and-absence-accrue.md#accrue-leave-per-company-or-per-leave-plan).</span><span class="sxs-lookup"><span data-stu-id="92a64-156">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md#accrue-leave-per-company-or-per-leave-plan).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="92a64-157">Přidání příloh k požadavkům na volno</span><span class="sxs-lookup"><span data-stu-id="92a64-157">Add attachments to time off requests</span></span>

<span data-ttu-id="92a64-158">Schopnost přidávat přílohy ke schváleným požadavkům na dovolenou je v současném prostředí COVID-19 kritická.</span><span class="sxs-lookup"><span data-stu-id="92a64-158">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="92a64-159">Zaměstnanci nyní mohou tyto přílohy přidávat.</span><span class="sxs-lookup"><span data-stu-id="92a64-159">Employees can now add these attachments.</span></span> <span data-ttu-id="92a64-160">Mají také podrobnější přehled o tom, jak jsou aktualizovány žádosti o dovolenou.</span><span class="sxs-lookup"><span data-stu-id="92a64-160">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="92a64-161">Další informace získáte v části [Přidání přílohy k existující žádosti](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span><span class="sxs-lookup"><span data-stu-id="92a64-161">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="92a64-162">Přidání kódu důvodu k časově rozlišeným pozastavením</span><span class="sxs-lookup"><span data-stu-id="92a64-162">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="92a64-163">K akruálnímu pozastavení byly přidány kódy důvodů.</span><span class="sxs-lookup"><span data-stu-id="92a64-163">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="92a64-164">Pravidla pro převod do dalšího období</span><span class="sxs-lookup"><span data-stu-id="92a64-164">Carry forward rules</span></span> 

<span data-ttu-id="92a64-165">Můžete určit typ převodu pracovního volna do dalšího období pro převod zůstatků, kde byly převedeny úpravy převodu do dalšího období.</span><span class="sxs-lookup"><span data-stu-id="92a64-165">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="92a64-166">Pokud například zaměstnanec přenese deset dní dopředu, můžete pro tyto 10 dny vybrat jiný typ pracovního volna.</span><span class="sxs-lookup"><span data-stu-id="92a64-166">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="92a64-167">Další informace naleznete v tématu [Konfigurace typů pracovního volna a absence](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="92a64-167">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="92a64-168">Časové rozlišení pozastavení dovolené pro zadané typy dovolené</span><span class="sxs-lookup"><span data-stu-id="92a64-168">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="92a64-169">Můžete vytvořit pravidlo pro pozastavení přírůstků dovolené pro zaměstnance s požadavky na dovolenou zadanými pro neplacenou dovolenou.</span><span class="sxs-lookup"><span data-stu-id="92a64-169">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="92a64-170">Neplacená dovolená může být zadána, ale nemusí.</span><span class="sxs-lookup"><span data-stu-id="92a64-170">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="92a64-171">Dovolenou můžete pozastavit na základě jiného typu dovolené.</span><span class="sxs-lookup"><span data-stu-id="92a64-171">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="92a64-172">Entita DMF dostupná pro pozastavení časového rozlišení</span><span class="sxs-lookup"><span data-stu-id="92a64-172">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="92a64-173">Entita DMF je nyní k dispozici pro akruální pozastavení</span><span class="sxs-lookup"><span data-stu-id="92a64-173">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="92a64-174">Již brzy</span><span class="sxs-lookup"><span data-stu-id="92a64-174">Coming soon</span></span>

## <a name="configure-the-name-of-employee-self-service"></a><span data-ttu-id="92a64-175">Konfigurace samoobsluhy pro zaměstnance</span><span class="sxs-lookup"><span data-stu-id="92a64-175">Configure the name of Employee self-service</span></span>

<span data-ttu-id="92a64-176">V **parametrech lidských zdrojů** bude k dispozici nová možnost aktualizace názvu pracovního prostoru Zaměstnanecká samoobsluha na Samoobsluha.</span><span class="sxs-lookup"><span data-stu-id="92a64-176">A new option will be available in **Human Resources parameters** to update the name of the Employee self service workspace to Self service.</span></span>

## <a name="checklist-entities-included-in-common-data-service"></a><span data-ttu-id="92a64-177">Položky kontrolního seznamu zahrnuté do Common Data Service</span><span class="sxs-lookup"><span data-stu-id="92a64-177">Checklist entities included in Common Data Service</span></span>

<span data-ttu-id="92a64-178">Položky kontrolního seznamu pro onboarding, offboarding, převody a obchodní procesy budou v systému Common Data Service k dispozici již brzy.</span><span class="sxs-lookup"><span data-stu-id="92a64-178">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon within Common Data Service.</span></span>

## <a name="see-also"></a><span data-ttu-id="92a64-179">Viz také</span><span class="sxs-lookup"><span data-stu-id="92a64-179">See also</span></span>

[<span data-ttu-id="92a64-180">Co je nového a co se změnilo v Human Resources</span><span class="sxs-lookup"><span data-stu-id="92a64-180">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="92a64-181">Přehled produktu Dynamics 365 Human Resources vydání 2019 vlny 2</span><span class="sxs-lookup"><span data-stu-id="92a64-181">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="92a64-182">Aktualizace procesu</span><span class="sxs-lookup"><span data-stu-id="92a64-182">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="92a64-183">Správa funkcí</span><span class="sxs-lookup"><span data-stu-id="92a64-183">Manage features</span></span>](hr-admin-manage-features.md)