---
title: Co je nového nebo změněného v aplikaci Dynamics 365 Human Resources (14. května 2020)
description: Tohle téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Human Resources k 14. květnu 2020.
author: andreabichsel
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f8244d512c9e1236fc52cd4a91cdc78cc2b9b984
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893094"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-14-2020"></a><span data-ttu-id="9fd69-103">Co je nového nebo změněného v aplikaci Dynamics 365 Human Resources (14. května 2020)</span><span class="sxs-lookup"><span data-stu-id="9fd69-103">What's new or changed in Dynamics 365 Human Resources (May 14, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="9fd69-104">Toto téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="9fd69-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="9fd69-105">Změny se vztahují na sestavení číslo 8.1.3244.</span><span class="sxs-lookup"><span data-stu-id="9fd69-105">Changes apply to build number 8.1.3244.</span></span> <span data-ttu-id="9fd69-106">Čísla v závorkách v některých záhlavích se vztahují na čísla podpory pro referenci v Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="9fd69-106">The numbers in parentheses in some headings refer to Lifecycle Services (LCS) support numbers for reference.</span></span>

## <a name="platform-changes"></a><span data-ttu-id="9fd69-107">Změny platformy</span><span class="sxs-lookup"><span data-stu-id="9fd69-107">Platform changes</span></span>

<span data-ttu-id="9fd69-108">Změny platformy jsou součástí vydání tohoto týdne.</span><span class="sxs-lookup"><span data-stu-id="9fd69-108">Platform changes are included in this week's release.</span></span> <span data-ttu-id="9fd69-109">Další informace naleznete v části [Aktualizace platformy pro verze 10.0.10 aplikací Finance and Operations (květen 2020)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-34.md).</span><span class="sxs-lookup"><span data-stu-id="9fd69-109">For more information, see [Platform updates for version 10.0.10 of Finance and Operations apps (May 2020)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-update-34.md).</span></span> <span data-ttu-id="9fd69-110">Tato verze obsahuje opravy chyb a změny uložených zobrazení.</span><span class="sxs-lookup"><span data-stu-id="9fd69-110">This release includes bug fixes and changes to saved views.</span></span>
 
## <a name="ensure-dataverse-picklists-are-consistent-with-leave-enums-436343"></a><span data-ttu-id="9fd69-111">Zajistěte, že rozevírací seznamy Dataverse jsou shodné s výčty volna (436343)</span><span class="sxs-lookup"><span data-stu-id="9fd69-111">Ensure Dataverse picklists are consistent with Leave enums (436343)</span></span>

<span data-ttu-id="9fd69-112">Rozevírací seznamy Dataverse jsou nyní shodné s výčty volna.</span><span class="sxs-lookup"><span data-stu-id="9fd69-112">Dataverse picklists are now consistent with Leave enums.</span></span>

## <a name="allow-users-to-configure-leave-request-workflow-based-on-the-request-amount-300044"></a><span data-ttu-id="9fd69-113">Umožněte uživatelům konfigurovat pracovní postup žádosti o volno na základě požadované délky (300044)</span><span class="sxs-lookup"><span data-stu-id="9fd69-113">Allow users to configure leave request workflow based on the request amount (300044)</span></span>

<span data-ttu-id="9fd69-114">Uživatelé mohou nakonfigurovat pracovní postupy žádosti o volno na základě požadovaných délek.</span><span class="sxs-lookup"><span data-stu-id="9fd69-114">Users can configure leave requests workflows based on request amounts.</span></span>
 
## <a name="new-worker-form-exposes-data-through-the-view-menu-when-advanced-security-is-enabled-403185"></a><span data-ttu-id="9fd69-115">Nový formulář pracovníka vystaví data prostřednictvím nabídky Zobrazit, pokud je povoleno rozšířené zabezpečení (403185)</span><span class="sxs-lookup"><span data-stu-id="9fd69-115">New worker form exposes data through the View menu when advanced security is enabled (403185)</span></span>

<span data-ttu-id="9fd69-116">Toto vydání opravuje, jak funguje zobrazení pracovníků napříč právnickými osobami, když je povolen pokročilý přístup a pracovníci v jiných společnostech jsou přístupní.</span><span class="sxs-lookup"><span data-stu-id="9fd69-116">This release corrects how viewing workers across legal entities functions when advanced access is enabled and workers in other companies are accessible.</span></span>

## <a name="allow-running-leave-accruals-for-a-single-plan-or-a-single-company-318844"></a><span data-ttu-id="9fd69-117">Povolení spuštění časového rozlišení volna pro jeden plán nebo pro jednu společnost (318844)</span><span class="sxs-lookup"><span data-stu-id="9fd69-117">Allow running leave accruals for a single plan or a single company (318844)</span></span>

<span data-ttu-id="9fd69-118">S touto změnou můžete spouštět časová rozlišení pro společnost nebo plán.</span><span class="sxs-lookup"><span data-stu-id="9fd69-118">With this change, you can run accruals for a company or a plan.</span></span>
 
## <a name="show-the-positions-full-time-equivalent-fte-in-the-enrolled-workers-form-414658"></a><span data-ttu-id="9fd69-119">Zobrazení ekvivalentu plného úvazku ve formuláři registrovaných pracovníků (414658)</span><span class="sxs-lookup"><span data-stu-id="9fd69-119">Show the position's full-time equivalent (FTE) in the Enrolled workers form (414658)</span></span>

<span data-ttu-id="9fd69-120">Hodnota ekvivalentu plného úvazku z pozice pracovníka určuje míru časového rozlišení pracovníka, když je na typu volna povolena možnost ekvivalentu plného úvazku.</span><span class="sxs-lookup"><span data-stu-id="9fd69-120">The FTE value from a worker's position determines a worker's accrual rate when the FTE option is enabled on the leave type.</span></span> <span data-ttu-id="9fd69-121">Toto pole je nyní zahrnuto ve formuláři **Registrovaní pracovníci** a v dialogovém okně **Hromadná registrace**.</span><span class="sxs-lookup"><span data-stu-id="9fd69-121">This field is now included in **Enrolled workers** form and the **Mass enrollment** dialog.</span></span>

## <a name="add-leave-balance-expiration-batch-job-431266"></a><span data-ttu-id="9fd69-122">Přidat dávkovou úlohu vypršení platnosti zůstatku volna (431266)</span><span class="sxs-lookup"><span data-stu-id="9fd69-122">Add leave balance expiration batch job (431266)</span></span>

<span data-ttu-id="9fd69-123">Nyní je k dispozici nová dávková úloha, která se spouští denně.</span><span class="sxs-lookup"><span data-stu-id="9fd69-123">A new batch job is now available that runs daily.</span></span> <span data-ttu-id="9fd69-124">Snižuje zbývající zůstatek volna, když nastanou data vypršení platnosti.</span><span class="sxs-lookup"><span data-stu-id="9fd69-124">It decreases the remaining leave balance when expiration dates become current.</span></span>

## <a name="exporting-personal-contacts-for-an-employee-using-the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-the-parent-relationship-type-345893"></a><span data-ttu-id="9fd69-125">Export osobních kontaktů zaměstnance pomocí entity kontaktní osoby pracovníka neexportuje osobní kontakty s typem nadřazeného vztahu (345893)</span><span class="sxs-lookup"><span data-stu-id="9fd69-125">Exporting personal contacts for an employee using the Worker personal contact person entity doesn't export personal contacts with the Parent relationship type (345893)</span></span>

<span data-ttu-id="9fd69-126">Datová entita **Kontaktní osoba pracovníka** (**HcmPersonalContactPersonEntity** v DMF a **PersonalContactPerson** v OData) nemohla exportovat osobní kontakty, které mají typ vztahu **Nadřazený**.</span><span class="sxs-lookup"><span data-stu-id="9fd69-126">The **Worker personal contact person** data entity (**HcmPersonalContactPersonEntity** in DMF and **PersonalContactPerson** in OData) couldn't export personal contacts that have a relationship type of **Parent**.</span></span> <span data-ttu-id="9fd69-127">Tento problém je opraven u osobních kontaktů vytvořených po této změně.</span><span class="sxs-lookup"><span data-stu-id="9fd69-127">This issue is fixed for personal contacts that are created after this change.</span></span> <span data-ttu-id="9fd69-128">Existující osobní kontakty typu **Nadřazený** budou opraveny v pozdějším vydání.</span><span class="sxs-lookup"><span data-stu-id="9fd69-128">Existing personal contacts of type **Parent** will be fixed in a later release.</span></span>

## <a name="reason-codes-display-across-different-scenarios-when-theyre-marked-as-leave-and-absence-and-the-streamlined-employee-form-is-enabled-434163"></a><span data-ttu-id="9fd69-129">Kódy důvodů se zobrazují v různých scénářích, když jsou označeny jako Pracovní volno a absence a je aktivován zjednodušený formulář zaměstnance (434163)</span><span class="sxs-lookup"><span data-stu-id="9fd69-129">Reason codes display across different scenarios when they're marked as Leave and absence and the streamlined employee form is enabled (434163)</span></span>

<span data-ttu-id="9fd69-130">Tato změna omezuje kódy důvodů pouze na kódy pracovního volna a absence, pokud povolíte zjednodušené zadávání zaměstnanců.</span><span class="sxs-lookup"><span data-stu-id="9fd69-130">This change restricts the reason codes to only Leave and absence codes when you enable streamlined employee entry.</span></span>

## <a name="the-preview-feature-assign-a-leave-plan-to-employees-in-the-future-displays-error-433555"></a><span data-ttu-id="9fd69-131">Funkce Preview s názvem Přiřadit zaměstnancům plán volna v budoucnu zobrazí chybu (433555)</span><span class="sxs-lookup"><span data-stu-id="9fd69-131">The preview feature Assign a leave plan to employees in the future displays error (433555)</span></span>

<span data-ttu-id="9fd69-132">Tato změna opravuje chybu, pokud má plán pracovního volna přiřazené dva typy pracovního volna a pokusíte se o přiřazení zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="9fd69-132">This change corrects an error when a leave plan has two leave types assigned and you attempt to assign an employee.</span></span>

## <a name="getting-started-banner-appears-for-all-users-441731"></a><span data-ttu-id="9fd69-133">Pro všechny uživatele se zobrazí banner Začínáme (441731)</span><span class="sxs-lookup"><span data-stu-id="9fd69-133">Getting started banner appears for all users (441731)</span></span>

<span data-ttu-id="9fd69-134">Při této změně je banner Začínáme skryt pro uživatele, kteří nejsou správci systému nebo správci dat.</span><span class="sxs-lookup"><span data-stu-id="9fd69-134">With this change, the Getting started banner is hidden for users that aren't System administrators or Data management administrators.</span></span> 

## <a name="the-dataverse-worker-address-entity-works-differently-in-terms-of-date-time-effective-dates-in-human-resources-425071"></a><span data-ttu-id="9fd69-135">Entita adresy pracovníka v Dataverse pracuje odlišně, pokud jde o data účinnosti data v Human Resources (425071)</span><span class="sxs-lookup"><span data-stu-id="9fd69-135">The Dataverse Worker Address entity works differently in terms of date time effective dates in Human Resources (425071)</span></span>

<span data-ttu-id="9fd69-136">Tato změna udržuje informace o adrese v souladu v určitých scénářích na základě údajů adresy.</span><span class="sxs-lookup"><span data-stu-id="9fd69-136">This change keeps address information aligned in certain scenarios, based on the dates of the address.</span></span>

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-425407"></a><span data-ttu-id="9fd69-137">Nelze přidat přílohu ke schválené žádosti o pracovní volno (425407)</span><span class="sxs-lookup"><span data-stu-id="9fd69-137">Unable to add an attachment to an approved leave request (425407)</span></span>

<span data-ttu-id="9fd69-138">Díky vydání tohoto týdne můžete přidávat přílohy ke schváleným žádostem o pracovní volno, aniž byste museli žádost o pracovní volno měnit.</span><span class="sxs-lookup"><span data-stu-id="9fd69-138">With this week's release, you can add attachments to approved leave requests without changing the leave request.</span></span>

## <a name="in-preview"></a><span data-ttu-id="9fd69-139">Náhled</span><span class="sxs-lookup"><span data-stu-id="9fd69-139">In preview</span></span>

## <a name="leave-suspension"></a><span data-ttu-id="9fd69-140">Pozastavit pracovní volno</span><span class="sxs-lookup"><span data-stu-id="9fd69-140">Leave suspension</span></span>

<span data-ttu-id="9fd69-141">Můžete přerušit pracovní volno a absenci v Human Resources pro zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="9fd69-141">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="9fd69-142">Pozastavením volna se zastaví časové rozlišení volna pro vybrané typy pracovního volna.</span><span class="sxs-lookup"><span data-stu-id="9fd69-142">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="9fd69-143">Pokud k přerušení dojde po zpracování časového rozlišení, pozastavením volna se vytvoří průběžná Úprava zůstatku zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="9fd69-143">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="9fd69-144">Další informace naleznete v části [Přerušení pracovního volna](hr-leave-and-absence-suspend-leave.md).</span><span class="sxs-lookup"><span data-stu-id="9fd69-144">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a><span data-ttu-id="9fd69-145">Aktualizujte uživatelské prostředí, abyste naznačili, že akruální účet je pozastaven (429550)</span><span class="sxs-lookup"><span data-stu-id="9fd69-145">Update user experience to indicate that accrual is suspended (429550)</span></span>

<span data-ttu-id="9fd69-146">Uživatelská zkušenost nyní naznačuje, že přírůstek byl pro plán pozastaven.</span><span class="sxs-lookup"><span data-stu-id="9fd69-146">The user experience now indicates that the accrual has been suspended for a plan.</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types-272447"></a><span data-ttu-id="9fd69-147">Pozastavení časového limitu pro vybrané typy dovolené (272447)</span><span class="sxs-lookup"><span data-stu-id="9fd69-147">Suspend leave accrual for specified leave types (272447)</span></span>

<span data-ttu-id="9fd69-148">V této verzi může HR vytvořit pravidlo pro pozastavení přírůstků dovolené pro zaměstnance s požadavky na dovolenou zadanými pro neplacenou dovolenou.</span><span class="sxs-lookup"><span data-stu-id="9fd69-148">In this release, HR can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="9fd69-149">Neplacená dovolená může být zadána, ale nemusí.</span><span class="sxs-lookup"><span data-stu-id="9fd69-149">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="9fd69-150">Dovolenou můžete pozastavit na základě jiného typu dovolené.</span><span class="sxs-lookup"><span data-stu-id="9fd69-150">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions-429549"></a><span data-ttu-id="9fd69-151">Entita DMF je k dispozici pro akruální pozastavení (429549)</span><span class="sxs-lookup"><span data-stu-id="9fd69-151">DMF entity available for accrual suspensions (429549)</span></span>

<span data-ttu-id="9fd69-152">Entita DMF je nyní k dispozici pro akruální pozastavení</span><span class="sxs-lookup"><span data-stu-id="9fd69-152">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="add-reason-code-to-accrual-suspensions-429547"></a><span data-ttu-id="9fd69-153">Přidejte kód příčiny pro akruální pozastavení (429547)</span><span class="sxs-lookup"><span data-stu-id="9fd69-153">Add reason code to accrual suspensions (429547)</span></span>

<span data-ttu-id="9fd69-154">K akruálnímu pozastavení byly přidány kódy důvodů.</span><span class="sxs-lookup"><span data-stu-id="9fd69-154">Reason codes have been added to the accrual suspension.</span></span>

## <a name="begin-transitioning-from-human-resources-parameters-to-leave-and-absence-parameters"></a><span data-ttu-id="9fd69-155">Začněte přechod z parametrů lidských zdrojů na parametry dovolené a nepřítomnosti</span><span class="sxs-lookup"><span data-stu-id="9fd69-155">Begin transitioning from Human Resources parameters to leave and absence parameters</span></span>

<span data-ttu-id="9fd69-156">Tato verze začíná kombinovat parametry lidských zdrojů s parametry dovolené a nepřítomnosti.</span><span class="sxs-lookup"><span data-stu-id="9fd69-156">This release starts to combine Human Resources parameters with Leave and absence parameters.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="9fd69-157">Pravidla pro převod do dalšího období</span><span class="sxs-lookup"><span data-stu-id="9fd69-157">Carry forward rules</span></span>

<span data-ttu-id="9fd69-158">Můžete určit typ převodu pracovního volna do dalšího období pro převod zůstatků, kde byly převedeny úpravy převodu do dalšího období.</span><span class="sxs-lookup"><span data-stu-id="9fd69-158">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="9fd69-159">Pokud například zaměstnanec přenese deset dní dopředu, můžete pro tyto 10 dny vybrat jiný typ pracovního volna.</span><span class="sxs-lookup"><span data-stu-id="9fd69-159">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="9fd69-160">Další informace naleznete v tématu [Konfigurace typů pracovního volna a absence](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="9fd69-160">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="9fd69-161">Viz také</span><span class="sxs-lookup"><span data-stu-id="9fd69-161">See also</span></span>

[<span data-ttu-id="9fd69-162">Co je nového a co se změnilo v Human Resources</span><span class="sxs-lookup"><span data-stu-id="9fd69-162">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="9fd69-163">Přehled produktu Dynamics 365 Human Resources vydání 2019 vlny 2</span><span class="sxs-lookup"><span data-stu-id="9fd69-163">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="9fd69-164">Aktualizace procesu</span><span class="sxs-lookup"><span data-stu-id="9fd69-164">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="9fd69-165">Správa funkcí</span><span class="sxs-lookup"><span data-stu-id="9fd69-165">Manage features</span></span>](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]