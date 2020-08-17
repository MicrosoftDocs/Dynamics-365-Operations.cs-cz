---
title: Co je nového nebo co se změnilo v aplikaci Dynamics 365 Human Resources (23. července 2020)
description: Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Human Resources.
author: Darinkramer
manager: AnnBe
ms.date: 07/23/2020
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
ms.search.validFrom: 2020-07-23
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: dd71ab5c48be1bec5ce2272bbff37ab10a4aed67
ms.sourcegitcommit: 81296c49be9953aa01e15527c34d0ef13b4622a9
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/22/2020
ms.locfileid: "3614403"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-23-2020"></a><span data-ttu-id="be618-103">Co je nového nebo co se změnilo v aplikaci Dynamics 365 Human Resources (23. července 2020)</span><span class="sxs-lookup"><span data-stu-id="be618-103">What's new or changed in Dynamics 365 Human Resources (July 23, 2020)</span></span>

<span data-ttu-id="be618-104">Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="be618-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="be618-105">Změny se vztahují na sestavení číslo 8.1.3416.</span><span class="sxs-lookup"><span data-stu-id="be618-105">Changes apply to build number 8.1.3416.</span></span> <span data-ttu-id="be618-106">Čísla v závorkách v některých záhlavích se vztahují na čísla podpory v Lifecycle Services (LCS) pro referenci.</span><span class="sxs-lookup"><span data-stu-id="be618-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="deleting-financial-dimensions-on-a-position-doesnt-work-as-expected-445476"></a><span data-ttu-id="be618-107">Odstranění finančních dimenzí na pozici nefunguje podle očekávání (445476)</span><span class="sxs-lookup"><span data-stu-id="be618-107">Deleting Financial Dimensions on a Position doesn't work as expected (445476)</span></span>

<span data-ttu-id="be618-108">Odstranění dimenzí z pozice nyní odstraní stejné pozice z Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="be618-108">Removing dimensions from a position now removes those same positions from Common Data Service.</span></span>

## <a name="positions-not-in-hierarchy-show-inactive-positions-397257"></a><span data-ttu-id="be618-109">Pozice, které nejsou v hierarchii, ukazují neaktivní pozice (397257)</span><span class="sxs-lookup"><span data-stu-id="be618-109">Positions not in hierarchy show inactive positions (397257)</span></span>

<span data-ttu-id="be618-110">Pozice, které jsou neaktivní (jejichž platnost vypršela), se již v hierarchii pozic nezobrazují jako **Pozice, které nejsou v hierarchii**.</span><span class="sxs-lookup"><span data-stu-id="be618-110">Positions that are inactive (have an expired duration), no longer display in the position hierarchy as **Positions not in hierarchy**.</span></span> 

## <a name="validation-occurring-between-leaveenrollmententity-and-hcmworkerentity-on-data-management-framework-dmf-import-causes-slow-data-loads-442324"></a><span data-ttu-id="be618-111">Ověření, které nastane mezi importem LeaveEnrollmentEntity a HcmWorkerEntity na importu architektury pro správu dat (DMF), způsobuje pomalé načítání dat (442324)</span><span class="sxs-lookup"><span data-stu-id="be618-111">Validation occurring between LeaveEnrollmentEntity and HcmWorkerEntity on Data Management Framework (DMF) import causes slow data loads (442324)</span></span>

<span data-ttu-id="be618-112">Změny v této verzi zvyšují výkon **LeaveEnrollmentEntity**.</span><span class="sxs-lookup"><span data-stu-id="be618-112">Changes in this release increase the performance of **LeaveEnrollmentEntity**.</span></span>

## <a name="unable-to-personalize-in-organization-administration-447490"></a><span data-ttu-id="be618-113">Nelze provádět přizpůsobení ve správě organizace (447490)</span><span class="sxs-lookup"><span data-stu-id="be618-113">Unable to personalize in Organization administration (447490)</span></span>

<span data-ttu-id="be618-114">Díky této změně si nyní můžete přizpůsobit odkazy ve **Správě organizace**.</span><span class="sxs-lookup"><span data-stu-id="be618-114">With this change, you can now personalize the links in **Organization administration**.</span></span>

## <a name="in-preview"></a><span data-ttu-id="be618-115">Náhled</span><span class="sxs-lookup"><span data-stu-id="be618-115">In preview</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="be618-116">Povinná pole</span><span class="sxs-lookup"><span data-stu-id="be618-116">Mandatory fields</span></span> 

<span data-ttu-id="be618-117">Nyní můžete změnit pole na povinná pomocí personalizačních funkcí systému lidských zdrojů.</span><span class="sxs-lookup"><span data-stu-id="be618-117">You can now make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="be618-118">Tato funkce vyžaduje **Uložená zobrazení**.</span><span class="sxs-lookup"><span data-stu-id="be618-118">This feature requires **Saved views**.</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="be618-119">Aplikace Human Resources v Teams</span><span class="sxs-lookup"><span data-stu-id="be618-119">Human Resources application in Teams</span></span>

<span data-ttu-id="be618-120">Zaměstnanci mohou prohlížet a požadovat pracovní volno v rámci Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="be618-120">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="be618-121">Mohou interagovat s robotem a vytvářet žádosti o dovolenou.</span><span class="sxs-lookup"><span data-stu-id="be618-121">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="be618-122">Další informace viz [Aplikace Human Resources v Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span><span class="sxs-lookup"><span data-stu-id="be618-122">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="be618-123">Entity právy datových rámců (DMF) pro správu zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="be618-123">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="be618-124">Zvýhodněné účetní jednotky se uvolňují.</span><span class="sxs-lookup"><span data-stu-id="be618-124">Benefits management entities are releasing.</span></span> <span data-ttu-id="be618-125">Entity DMF umožňují import a export dat pro snadnou konfiguraci správy výhod.</span><span class="sxs-lookup"><span data-stu-id="be618-125">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="be618-126">K přesunutí dat bude k dispozici šablona správy výhod.</span><span class="sxs-lookup"><span data-stu-id="be618-126">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="be618-127">Šablona exportuje a importuje data sekvenčně, aby respektovala datové závislosti.</span><span class="sxs-lookup"><span data-stu-id="be618-127">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="be618-128">Nákup a prodej pracovního volna</span><span class="sxs-lookup"><span data-stu-id="be618-128">Buy and sell leave</span></span> 

<span data-ttu-id="be618-129">Některé organizace poskytují výhodu, která zaměstnancům umožňuje nakupovat nebo prodávat dovolenou.</span><span class="sxs-lookup"><span data-stu-id="be618-129">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="be618-130">Tento proces je často řízen ručně.</span><span class="sxs-lookup"><span data-stu-id="be618-130">This process is often managed manually.</span></span> <span data-ttu-id="be618-131">Tato funkce automatizuje správu zásad a požadavků oddělení lidských zdrojů.</span><span class="sxs-lookup"><span data-stu-id="be618-131">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="be618-132">Usnadňuje proces správy dovolených a pomáhá eliminovat chyby.</span><span class="sxs-lookup"><span data-stu-id="be618-132">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="be618-133">Další informace naleznete zde:</span><span class="sxs-lookup"><span data-stu-id="be618-133">For more information, see:</span></span>

- [<span data-ttu-id="be618-134">Správa zásad nákupu a prodeje pracovního volna</span><span class="sxs-lookup"><span data-stu-id="be618-134">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="be618-135">Nákup a prodej pracovního volna</span><span class="sxs-lookup"><span data-stu-id="be618-135">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="be618-136">Časové rozlišení pracovního volna pro jednu společnost nebo jeden plán</span><span class="sxs-lookup"><span data-stu-id="be618-136">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="be618-137">Zákazníci mohou zpracovat časové rozlišení pro jednu společnost nebo jeden plán dovolené a nepřítomnosti.</span><span class="sxs-lookup"><span data-stu-id="be618-137">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="be618-138">Tato schopnost objasňuje proces časového rozlišení pro zákazníky s různými roky dovolené nebo zásadami časového rozlišení dovolené.</span><span class="sxs-lookup"><span data-stu-id="be618-138">This ability provides clarity for the accrual process for customers with different leave years or leaves accrual policies.</span></span> <span data-ttu-id="be618-139">Další informace získáte v části [Časové rozlišení dovolené podle společnosti nebo plánu dovolených](hr-leave-and-absence-accrue.md#accrue-leave-per-company-or-per-leave-plan).</span><span class="sxs-lookup"><span data-stu-id="be618-139">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md#accrue-leave-per-company-or-per-leave-plan).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="be618-140">Přidání příloh k požadavkům na volno</span><span class="sxs-lookup"><span data-stu-id="be618-140">Add attachments to time-off requests</span></span>

<span data-ttu-id="be618-141">Schopnost přidávat přílohy ke schváleným požadavkům na dovolenou je v současném prostředí COVID-19 kritická.</span><span class="sxs-lookup"><span data-stu-id="be618-141">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="be618-142">Zaměstnanci nyní mohou tyto přílohy přidávat.</span><span class="sxs-lookup"><span data-stu-id="be618-142">Employees can now add these attachments.</span></span> <span data-ttu-id="be618-143">Mají také podrobnější přehled o tom, jak jsou aktualizovány žádosti o dovolenou.</span><span class="sxs-lookup"><span data-stu-id="be618-143">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="be618-144">Další informace získáte v části [Přidání přílohy k existující žádosti](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span><span class="sxs-lookup"><span data-stu-id="be618-144">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="be618-145">Přidání kódu důvodu k časově rozlišeným pozastavením</span><span class="sxs-lookup"><span data-stu-id="be618-145">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="be618-146">K akruálnímu pozastavení byly přidány kódy důvodů.</span><span class="sxs-lookup"><span data-stu-id="be618-146">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="be618-147">Pravidla pro převod do dalšího období</span><span class="sxs-lookup"><span data-stu-id="be618-147">Carry forward rules</span></span> 

<span data-ttu-id="be618-148">Můžete určit typ převodu pracovního volna do dalšího období pro převod zůstatků, kde byly převedeny úpravy převodu do dalšího období.</span><span class="sxs-lookup"><span data-stu-id="be618-148">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="be618-149">Pokud například zaměstnanec přenese deset dní dopředu, můžete pro tyto 10 dny vybrat jiný typ pracovního volna.</span><span class="sxs-lookup"><span data-stu-id="be618-149">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="be618-150">Další informace naleznete v tématu [Konfigurace typů pracovního volna a absence](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="be618-150">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="be618-151">Časové rozlišení pozastavení dovolené pro zadané typy dovolené</span><span class="sxs-lookup"><span data-stu-id="be618-151">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="be618-152">Můžete vytvořit pravidlo pro pozastavení přírůstků dovolené pro zaměstnance s požadavky na dovolenou zadanými pro neplacenou dovolenou.</span><span class="sxs-lookup"><span data-stu-id="be618-152">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="be618-153">Neplacená dovolená může být zadána, ale nemusí.</span><span class="sxs-lookup"><span data-stu-id="be618-153">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="be618-154">Dovolenou můžete pozastavit na základě jiného typu dovolené.</span><span class="sxs-lookup"><span data-stu-id="be618-154">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="be618-155">Entita DMF dostupná pro pozastavení časového rozlišení</span><span class="sxs-lookup"><span data-stu-id="be618-155">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="be618-156">Entita DMF je nyní k dispozici pro akruální pozastavení</span><span class="sxs-lookup"><span data-stu-id="be618-156">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="be618-157">Již brzy</span><span class="sxs-lookup"><span data-stu-id="be618-157">Coming soon</span></span>

## <a name="checklist-entities-included-in-common-data-service"></a><span data-ttu-id="be618-158">Položky kontrolního seznamu zahrnuté do Common Data Service</span><span class="sxs-lookup"><span data-stu-id="be618-158">Checklist entities included in Common Data Service</span></span>

<span data-ttu-id="be618-159">Položky kontrolního seznamu pro onboarding, offboarding, převody a obchodní procesy budou v systému Common Data Service k dispozici již brzy.</span><span class="sxs-lookup"><span data-stu-id="be618-159">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Common Data Service.</span></span>

## <a name="platform-changes"></a><span data-ttu-id="be618-160">Změny platformy</span><span class="sxs-lookup"><span data-stu-id="be618-160">Platform changes</span></span>

<span data-ttu-id="be618-161">Platform update 10.0.12 (36)</span><span class="sxs-lookup"><span data-stu-id="be618-161">Platform update 10.0.12 (36)</span></span>

## <a name="see-also"></a><span data-ttu-id="be618-162">Viz také</span><span class="sxs-lookup"><span data-stu-id="be618-162">See also</span></span>

[<span data-ttu-id="be618-163">Co je nového a co se změnilo v Human Resources</span><span class="sxs-lookup"><span data-stu-id="be618-163">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="be618-164">Přehled produktu Dynamics 365 Human Resources vydání 2019 vlny 2</span><span class="sxs-lookup"><span data-stu-id="be618-164">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="be618-165">Aktualizace procesu</span><span class="sxs-lookup"><span data-stu-id="be618-165">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="be618-166">Správa funkcí</span><span class="sxs-lookup"><span data-stu-id="be618-166">Manage features</span></span>](hr-admin-manage-features.md)
