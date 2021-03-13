---
title: Co je nového nebo co se změnilo v aplikaci Dynamics 365 Human Resources (08. července 2020)
description: Tohle téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Human Resources k 8. červenci 2020.
author: andreabichsel
manager: tfehr
ms.date: 07/08/2020
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
ms.author: jaredha
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 14dfd925009cb2a9d40044e27f28521ff4d331b7
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/06/2021
ms.locfileid: "5130390"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-8-2020"></a><span data-ttu-id="2b400-103">Co je nového nebo co se změnilo v aplikaci Dynamics 365 Human Resources (8. července 2020)</span><span class="sxs-lookup"><span data-stu-id="2b400-103">What's new or changed in Dynamics 365 Human Resources (July 8, 2020)</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="2b400-104">Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="2b400-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="2b400-105">Změny se vztahují na sestavení číslo 8.1.3382.</span><span class="sxs-lookup"><span data-stu-id="2b400-105">Changes apply to build number 8.1.3382.</span></span> <span data-ttu-id="2b400-106">Čísla v závorkách v některých záhlavích se vztahují na čísla podpory v Lifecycle Services (LCS) pro referenci.</span><span class="sxs-lookup"><span data-stu-id="2b400-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="database-logging"></a><span data-ttu-id="2b400-107">Protokolování databáze</span><span class="sxs-lookup"><span data-stu-id="2b400-107">Database logging</span></span>

<span data-ttu-id="2b400-108">Protokolování databáze umožňuje určit, které tabulky a pole mají být monitorovány.</span><span class="sxs-lookup"><span data-stu-id="2b400-108">Database logging allows you to determine which tables and fields to monitor.</span></span> <span data-ttu-id="2b400-109">Umožňuje také určit události, které by měly spustit sledování změn.</span><span class="sxs-lookup"><span data-stu-id="2b400-109">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="2b400-110">Pomocí funkcí protokolování databáze se můžete podívat na tyto změny v průběhu času.</span><span class="sxs-lookup"><span data-stu-id="2b400-110">You use database logging capabilities to see these changes over time.</span></span> <span data-ttu-id="2b400-111">Další informace získáte v rématu [Konfigurace a správa protokolování databáze](hr-admin-database-logging.md).</span><span class="sxs-lookup"><span data-stu-id="2b400-111">For more information, see [Configure and manage database logging](hr-admin-database-logging.md).</span></span>

## <a name="configure-the-name-of-employee-self-service"></a><span data-ttu-id="2b400-112">Konfigurace samoobsluhy pro zaměstnance</span><span class="sxs-lookup"><span data-stu-id="2b400-112">Configure the name of Employee self service</span></span>

<span data-ttu-id="2b400-113">V **Parametry lidských zdrojů** můžete nyní změnit název pracovního prostoru **Zaměstnanecká samoobsluha** na **Samoobsluha**.</span><span class="sxs-lookup"><span data-stu-id="2b400-113">In **Human Resources parameters**, you can now change the name of the **Employee self service** workspace to **Self service**.</span></span> <span data-ttu-id="2b400-114">Další informace naleznete v tématu [Změna názvu pracovního prostoru samoobsluhy pro zaměstnance](hr-employee-self-service-workspace-name.md)</span><span class="sxs-lookup"><span data-stu-id="2b400-114">For more information, see [Change Employee self service workspace name](hr-employee-self-service-workspace-name.md)</span></span>

## <a name="benefits-management-open-enrollment-access-outside-of-period"></a><span data-ttu-id="2b400-115">Oevřený přístup k zápisu správy zaměstnaneckých výhod mimo období</span><span class="sxs-lookup"><span data-stu-id="2b400-115">Benefits management open enrollment access outside of period</span></span>

<span data-ttu-id="2b400-116">Toto vydání opravuje chybu, kdy zaměstnanci měli přístup k výhodám otevřeného zápisu mimo období zápisu nebo bez životní události.</span><span class="sxs-lookup"><span data-stu-id="2b400-116">This release fixes a bug where employees could access benefits open enrollment outside of the enrollment period or without a life event.</span></span> <span data-ttu-id="2b400-117">V důsledku toho, pokud potřebujete ukázat otevřený zápis do samoobslužné služby zaměstnance, musíte upravit data otevřeného zápisu na dnešek (nebo dříve), abyste je zpřístupnili.</span><span class="sxs-lookup"><span data-stu-id="2b400-117">As a result, if you need to demo open enrollment in Employee self service, you must adjust the open enrollment dates to today (or earlier) to make it accessible.</span></span> <span data-ttu-id="2b400-118">Toto nastavení můžete změnit pod **Správa výhod > Období pravidel a možností**.</span><span class="sxs-lookup"><span data-stu-id="2b400-118">You can change this setting under **Benefits management > Rules and options periods**.</span></span>

## <a name="email-employee-enrollment-confirmation"></a><span data-ttu-id="2b400-119">E-mail s potvrzením o registraci zaměstnance</span><span class="sxs-lookup"><span data-stu-id="2b400-119">Email employee enrollment confirmation</span></span>

<span data-ttu-id="2b400-120">Po dokončení výběru výhod nyní můžete zaměstnancům zasílat e-maily.</span><span class="sxs-lookup"><span data-stu-id="2b400-120">You can now send emails to employees after they complete their benefits selection.</span></span> <span data-ttu-id="2b400-121">Můžete buď odeslat výchozí zprávu, nebo použít šablonu e-mailu organizace.</span><span class="sxs-lookup"><span data-stu-id="2b400-121">You can either send a default message or use an organization email template.</span></span> <span data-ttu-id="2b400-122">Tato nastavení jsou pod **Parametry lidských zdrojů > Správa zaměstnaneckých výhod**.</span><span class="sxs-lookup"><span data-stu-id="2b400-122">These settings are under **Human resource parameters > Benefits management**.</span></span>

## <a name="canceled-leave-still-appears-in-upcoming-time-off-on-people-workspace-441358"></a><span data-ttu-id="2b400-123">Zrušená dovolená se stále zobrazuje v nadcházejícím pracovním volnu v pracovním prostoru Lidé (441358)</span><span class="sxs-lookup"><span data-stu-id="2b400-123">Canceled leave still appears in upcoming time off on People workspace (441358)</span></span>

<span data-ttu-id="2b400-124">Zrušená dovolená se již nezobrazuje jako nadcházející volno na kartách volna v pracovním prostoru **Lidé**.</span><span class="sxs-lookup"><span data-stu-id="2b400-124">Canceled leave no longer displays as upcoming time off on the leave cards in the **People** workspace.</span></span>

## <a name="unable-to-use-the-department-entity-property-in-the-positionv2-entity-456486"></a><span data-ttu-id="2b400-125">Nelze použít vlastnost entity oddělení v entitě PositionV2 (456486)</span><span class="sxs-lookup"><span data-stu-id="2b400-125">Unable to use the department entity property in the PositionV2 entity (456486)</span></span>

<span data-ttu-id="2b400-126">Nyní můžete přidat oddělení bez vytvoření duplicitního vztahu.</span><span class="sxs-lookup"><span data-stu-id="2b400-126">You can now add a department without creating a duplicate relation.</span></span>

## <a name="payrollworkerenrolledbenefitdetailentity-should-only-use-calculated-field-for-retirement-plans-459779"></a><span data-ttu-id="2b400-127">PayrollWorkerEnrolledBenefitDetailEntity by měl používat vypočítané pole pouze pro penzijní plány (459779)</span><span class="sxs-lookup"><span data-stu-id="2b400-127">PayrollWorkerEnrolledBenefitDetailEntity should only use calculated field for retirement plans (459779)</span></span>

<span data-ttu-id="2b400-128">Při exportu entity **PayrollWorkerEnrolledBenefitDetailEntity** určuje export, zda by měl použít vypočtené pole na základě tabulky sazeb nebo použít pole **ContributionAmountCur** ze záložní tabulky.</span><span class="sxs-lookup"><span data-stu-id="2b400-128">When exporting the **PayrollWorkerEnrolledBenefitDetailEntity** entity, the export determines whether it should use a calculated field based on a rate table or use the **ContributionAmountCur** field on the backing table.</span></span> <span data-ttu-id="2b400-129">Logika použitá datovou entitou používá tabulku sazeb v situacích, kdy aplikace normálně ne.</span><span class="sxs-lookup"><span data-stu-id="2b400-129">The logic used by the data entity uses the rate table in situations where the application normally doesn't.</span></span> <span data-ttu-id="2b400-130">Tato logika způsobí, že export entity vrátí nulovou hodnotu pro tento sloupec, protože neexistuje žádná tabulka sazeb výpočtu a produkt neumožňuje zákazníkovi specifikovat jednu.</span><span class="sxs-lookup"><span data-stu-id="2b400-130">This logic causes the entity exports to return a zero value for this column, because there's no calculation rate table and the product doesn't allow the customer to specify one.</span></span>
 
## <a name="confusing-translations-in-czech-language-in-personnel-management-and-employee-self-service-400276"></a><span data-ttu-id="2b400-131">Zmatení překladů v českém jazyce ve Správě zaměstnanců a Samoobsluze zaměstnanců (400276)</span><span class="sxs-lookup"><span data-stu-id="2b400-131">Confusing translations in Czech language in Personnel management and Employee self service (400276)</span></span>

<span data-ttu-id="2b400-132">Toto vydání opravuje překlady pro **Adresář společnosti**, **Další zaregistrovaný kurz**, **Úloha** a **Pozice**.</span><span class="sxs-lookup"><span data-stu-id="2b400-132">This release corrects the translations for **Company directory**, **Next registered course**, **Job**, and **Position**.</span></span>
 
## <a name="the-workcalendaremployment-table-doesnt-have-the-created-and-modified-system-fields-enabled-460171"></a><span data-ttu-id="2b400-133">Tabulka WorkCalendarEmployment nemá vytvořená a upravená systémová pole povolena (460171)</span><span class="sxs-lookup"><span data-stu-id="2b400-133">The WorkCalendarEmployment table doesn't have the created and modified system fields enabled (460171)</span></span>

<span data-ttu-id="2b400-134">Vytvořená a upravená systémová pole jsou nyní povolena v tabulce **WorkCalendarEmployment** v Human Resources.</span><span class="sxs-lookup"><span data-stu-id="2b400-134">Created and modified system fields are now enabled on the **WorkCalendarEmployment** table in Human Resources.</span></span>
 
## <a name="null-reference-exception-for-hire-and-add-details-for-future-employee-455475"></a><span data-ttu-id="2b400-135">Nulová referenční výjimka pro Přijetí a přidejte podrobnosti pro budoucího zaměstnance (455475)</span><span class="sxs-lookup"><span data-stu-id="2b400-135">Null reference exception for Hire and add details for future employee (455475)</span></span>

<span data-ttu-id="2b400-136">Toto vydání opravuje chybu (nulová reference) v zjednodušeném záznamu zaměstnance, když přijmete zaměstnance pomocí možnosti **Příjem a přidání podrobností**.</span><span class="sxs-lookup"><span data-stu-id="2b400-136">This release corrects an error (null reference) in streamlined employee entry when you hire an employee using the option to **Hire and add details**.</span></span>

## <a name="changes-made-in-the-dataverse-worker-entity-dont-reflect-in-human-resources-455652"></a><span data-ttu-id="2b400-137">Změny provedené v entitě Dataverse Pracovník se neodráží v Human Resources (455652)</span><span class="sxs-lookup"><span data-stu-id="2b400-137">Changes made in the Dataverse Worker entity don't reflect in Human Resources (455652)</span></span>

<span data-ttu-id="2b400-138">Změny provedené v následujících polích v entitě **Pracovník** v Dataverse se nyní objeví v Human Resources:</span><span class="sxs-lookup"><span data-stu-id="2b400-138">Changes made to the following fields in the **Worker** entity in Dataverse will now show up in Human Resources:</span></span>

- <span data-ttu-id="2b400-139">**Práce z domu**</span><span class="sxs-lookup"><span data-stu-id="2b400-139">**Works from home**</span></span>
- <span data-ttu-id="2b400-140">**Datum služebního věku**</span><span class="sxs-lookup"><span data-stu-id="2b400-140">**Seniority date**</span></span>
- <span data-ttu-id="2b400-141">**Datum výročí**</span><span class="sxs-lookup"><span data-stu-id="2b400-141">**Anniversary date**</span></span>
- <span data-ttu-id="2b400-142">**Datum původního přijetí**</span><span class="sxs-lookup"><span data-stu-id="2b400-142">**Original hire date**</span></span>

## <a name="correct-compensation-level-doesnt-default-based-on-the-job-assigned-to-the-position-394136"></a><span data-ttu-id="2b400-143">Správná úroveň kompenzace není výchozí na základě úlohy přiřazené k dané pozici (394136)</span><span class="sxs-lookup"><span data-stu-id="2b400-143">Correct compensation level doesn't default based on the job assigned to the position (394136)</span></span>

<span data-ttu-id="2b400-144">S touto změnou je výchozí úroveň správné úrovně kompenzace na základě záznamů **Datum platnosti** pro **Detaily pozice** a **Počáteční datum** z **Přiřazení kompenzačního plánu**.</span><span class="sxs-lookup"><span data-stu-id="2b400-144">With this change, the correct compensation level defaults based on the **Date effective** records for the **Position details** and the **Start date** of the **Compensation plan assignment**.</span></span>

## <a name="in-preview"></a><span data-ttu-id="2b400-145">Náhled</span><span class="sxs-lookup"><span data-stu-id="2b400-145">In preview</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="2b400-146">Povinná pole</span><span class="sxs-lookup"><span data-stu-id="2b400-146">Mandatory fields</span></span> 

<span data-ttu-id="2b400-147">Nyní můžete změnit pole na povinná pomocí personalizačních funkcí systému lidských zdrojů.</span><span class="sxs-lookup"><span data-stu-id="2b400-147">You can now make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="2b400-148">Tato funkce vyžaduje **Uložená zobrazení**.</span><span class="sxs-lookup"><span data-stu-id="2b400-148">This feature requires **Saved views**.</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="2b400-149">Aplikace Human Resources v Teams</span><span class="sxs-lookup"><span data-stu-id="2b400-149">Human Resources application in Teams</span></span>

<span data-ttu-id="2b400-150">Zaměstnanci mohou prohlížet a požadovat pracovní volno v rámci Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="2b400-150">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="2b400-151">Mohou interagovat s robotem a vytvářet žádosti o dovolenou.</span><span class="sxs-lookup"><span data-stu-id="2b400-151">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="2b400-152">Další informace viz [Aplikace Human Resources v Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span><span class="sxs-lookup"><span data-stu-id="2b400-152">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="2b400-153">Entity právy datových rámců (DMF) pro správu zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="2b400-153">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="2b400-154">Zvýhodněné účetní jednotky se uvolňují.</span><span class="sxs-lookup"><span data-stu-id="2b400-154">Benefits management entities are releasing.</span></span> <span data-ttu-id="2b400-155">Entity DMF umožňují import a export dat pro snadnou konfiguraci správy výhod.</span><span class="sxs-lookup"><span data-stu-id="2b400-155">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="2b400-156">K přesunutí dat bude k dispozici šablona správy výhod.</span><span class="sxs-lookup"><span data-stu-id="2b400-156">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="2b400-157">Šablona exportuje a importuje data sekvenčně, aby respektovala datové závislosti.</span><span class="sxs-lookup"><span data-stu-id="2b400-157">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="2b400-158">Nákup a prodej pracovního volna</span><span class="sxs-lookup"><span data-stu-id="2b400-158">Buy and sell leave</span></span> 

<span data-ttu-id="2b400-159">Některé organizace poskytují výhodu, která zaměstnancům umožňuje nakupovat nebo prodávat dovolenou.</span><span class="sxs-lookup"><span data-stu-id="2b400-159">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="2b400-160">Tento proces je často řízen ručně.</span><span class="sxs-lookup"><span data-stu-id="2b400-160">This process is often managed manually.</span></span> <span data-ttu-id="2b400-161">Tato funkce automatizuje správu zásad a požadavků oddělení lidských zdrojů.</span><span class="sxs-lookup"><span data-stu-id="2b400-161">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="2b400-162">Usnadňuje proces správy dovolených a pomáhá eliminovat chyby.</span><span class="sxs-lookup"><span data-stu-id="2b400-162">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="2b400-163">Další informace naleznete zde:</span><span class="sxs-lookup"><span data-stu-id="2b400-163">For more information, see:</span></span>

- [<span data-ttu-id="2b400-164">Správa zásad nákupu a prodeje pracovního volna</span><span class="sxs-lookup"><span data-stu-id="2b400-164">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="2b400-165">Nákup a prodej pracovního volna</span><span class="sxs-lookup"><span data-stu-id="2b400-165">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="2b400-166">Časové rozlišení pracovního volna pro jednu společnost nebo jeden plán</span><span class="sxs-lookup"><span data-stu-id="2b400-166">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="2b400-167">Zákazníci mohou zpracovat časové rozlišení pro jednu společnost nebo jeden plán dovolené a nepřítomnosti.</span><span class="sxs-lookup"><span data-stu-id="2b400-167">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="2b400-168">Tato schopnost objasňuje proces časového rozlišení pro zákazníky s různými roky dovolené nebo zásadami časového rozlišení dovolené.</span><span class="sxs-lookup"><span data-stu-id="2b400-168">This ability provides clarity for the accrual process for customers with different leave years or leave accrual policies.</span></span> <span data-ttu-id="2b400-169">Další informace získáte v části [Časové rozlišení dovolené podle společnosti nebo plánu dovolených](hr-leave-and-absence-accrue.md).</span><span class="sxs-lookup"><span data-stu-id="2b400-169">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="2b400-170">Přidání příloh k požadavkům na volno</span><span class="sxs-lookup"><span data-stu-id="2b400-170">Add attachments to time-off requests</span></span>

<span data-ttu-id="2b400-171">Schopnost přidávat přílohy ke schváleným požadavkům na dovolenou je v současném prostředí COVID-19 kritická.</span><span class="sxs-lookup"><span data-stu-id="2b400-171">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="2b400-172">Zaměstnanci nyní mohou tyto přílohy přidávat.</span><span class="sxs-lookup"><span data-stu-id="2b400-172">Employees can now add these attachments.</span></span> <span data-ttu-id="2b400-173">Mají také podrobnější přehled o tom, jak jsou aktualizovány žádosti o dovolenou.</span><span class="sxs-lookup"><span data-stu-id="2b400-173">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="2b400-174">Další informace získáte v části [Přidání přílohy k existující žádosti](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span><span class="sxs-lookup"><span data-stu-id="2b400-174">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="2b400-175">Přidání kódu důvodu k časově rozlišeným pozastavením</span><span class="sxs-lookup"><span data-stu-id="2b400-175">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="2b400-176">K akruálnímu pozastavení byly přidány kódy důvodů.</span><span class="sxs-lookup"><span data-stu-id="2b400-176">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="2b400-177">Pravidla pro převod do dalšího období</span><span class="sxs-lookup"><span data-stu-id="2b400-177">Carry forward rules</span></span> 

<span data-ttu-id="2b400-178">Můžete určit typ převodu pracovního volna do dalšího období pro převod zůstatků, kde byly převedeny úpravy převodu do dalšího období.</span><span class="sxs-lookup"><span data-stu-id="2b400-178">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="2b400-179">Pokud například zaměstnanec přenese deset dní dopředu, můžete pro tyto 10 dny vybrat jiný typ pracovního volna.</span><span class="sxs-lookup"><span data-stu-id="2b400-179">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="2b400-180">Další informace naleznete v tématu [Konfigurace typů pracovního volna a absence](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="2b400-180">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="2b400-181">Časové rozlišení pozastavení dovolené pro zadané typy dovolené</span><span class="sxs-lookup"><span data-stu-id="2b400-181">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="2b400-182">Můžete vytvořit pravidlo pro pozastavení přírůstků dovolené pro zaměstnance s požadavky na dovolenou zadanými pro neplacenou dovolenou.</span><span class="sxs-lookup"><span data-stu-id="2b400-182">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="2b400-183">Neplacená dovolená může být zadána, ale nemusí.</span><span class="sxs-lookup"><span data-stu-id="2b400-183">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="2b400-184">Dovolenou můžete pozastavit na základě jiného typu dovolené.</span><span class="sxs-lookup"><span data-stu-id="2b400-184">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="2b400-185">Entita DMF dostupná pro pozastavení časového rozlišení</span><span class="sxs-lookup"><span data-stu-id="2b400-185">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="2b400-186">Entita DMF je nyní k dispozici pro akruální pozastavení</span><span class="sxs-lookup"><span data-stu-id="2b400-186">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="2b400-187">Již brzy</span><span class="sxs-lookup"><span data-stu-id="2b400-187">Coming soon</span></span>

## <a name="checklist-entities-included-in-dataverse"></a><span data-ttu-id="2b400-188">Položky kontrolního seznamu zahrnuté do Dataverse</span><span class="sxs-lookup"><span data-stu-id="2b400-188">Checklist entities included in Dataverse</span></span>

<span data-ttu-id="2b400-189">Položky kontrolního seznamu pro onboarding, offboarding, převody a obchodní procesy budou v systému Dataverse k dispozici již brzy.</span><span class="sxs-lookup"><span data-stu-id="2b400-189">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Dataverse.</span></span>

## <a name="see-also"></a><span data-ttu-id="2b400-190">Viz také</span><span class="sxs-lookup"><span data-stu-id="2b400-190">See also</span></span>

[<span data-ttu-id="2b400-191">Co je nového a co se změnilo v Human Resources</span><span class="sxs-lookup"><span data-stu-id="2b400-191">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="2b400-192">Přehled produktu Dynamics 365 Human Resources vydání 2019 vlny 2</span><span class="sxs-lookup"><span data-stu-id="2b400-192">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="2b400-193">Aktualizace procesu</span><span class="sxs-lookup"><span data-stu-id="2b400-193">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="2b400-194">Správa funkcí</span><span class="sxs-lookup"><span data-stu-id="2b400-194">Manage features</span></span>](hr-admin-manage-features.md)
