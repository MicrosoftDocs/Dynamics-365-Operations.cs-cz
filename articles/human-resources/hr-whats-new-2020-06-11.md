---
title: Co je nového a co se změnilo v aplikaci Dynamics 365 Human Resources (11. června 2020)
description: Tohle téma popisuje funkce, které jsou nové nebo se změnily v aplikaci Microsoft Dynamics 365 Human Resources k 11. červnu 2020.
author: andreabichsel
manager: tfehr
ms.date: 06/16/2020
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
ms.search.validFrom: 2020-06-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6ff359f65afc03a1b5691fddc078f73682e99e44
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127794"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-11-2020"></a><span data-ttu-id="35e5d-103">Co je nového a co se změnilo v aplikaci Dynamics 365 Human Resources (11. června 2020)</span><span class="sxs-lookup"><span data-stu-id="35e5d-103">What's new or changed in Dynamics 365 Human Resources (June 11, 2020)</span></span>

<span data-ttu-id="35e5d-104">Tento článek popisuje funkce, které jsou nové nebo se změnily v aplikaci Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="35e5d-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="35e5d-105">Změny se vztahují na sestavení číslo 8.1.3316.</span><span class="sxs-lookup"><span data-stu-id="35e5d-105">Changes apply to build number 8.1.3316.</span></span> <span data-ttu-id="35e5d-106">Čísla v závorkách v některých záhlavích se vztahují na čísla podpory v Lifecycle Services (LCS) pro referenci.</span><span class="sxs-lookup"><span data-stu-id="35e5d-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="streamlined-employee-form-sometimes-causes-child-form-close-x-buttons-to-stop-working-442369"></a><span data-ttu-id="35e5d-107">Zjednodušený formulář zaměstnance někdy způsobuje, že tlačítka pro zavření podřízeného formuláře (X) přestanou fungovat (442369)</span><span class="sxs-lookup"><span data-stu-id="35e5d-107">Streamlined employee form sometimes causes child form close (X) buttons to stop working (442369)</span></span>

<span data-ttu-id="35e5d-108">Po povolení formuláře **Pracovník** tlačítko Zavřít (**X**) příležitostně nefungovalo v podřízených formulářích.</span><span class="sxs-lookup"><span data-stu-id="35e5d-108">When the new **Worker** form was enabled, the close (**X**) button occasionally didn't work on child forms.</span></span> <span data-ttu-id="35e5d-109">K tomuto problému docházelo přerušovaně.</span><span class="sxs-lookup"><span data-stu-id="35e5d-109">This problem was intermittent.</span></span> <span data-ttu-id="35e5d-110">Po odchodu a návratu k němu bylo možné formulář zavřít.</span><span class="sxs-lookup"><span data-stu-id="35e5d-110">You could close the form after leaving and coming back to it.</span></span> <span data-ttu-id="35e5d-111">Můžete například vybrat položku nabídky vlevo a přejít zpět na formulář **Pracovník** a následně ho zavřít.</span><span class="sxs-lookup"><span data-stu-id="35e5d-111">For example, you could select a menu item on the left, and navigate back to the **Worker** form, and then close it.</span></span> <span data-ttu-id="35e5d-112">Tento problém je opraven ve vydání na tento týden.</span><span class="sxs-lookup"><span data-stu-id="35e5d-112">This week's release fixes this problem.</span></span> 

## <a name="the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-a-parent-relationship-type"></a><span data-ttu-id="35e5d-113">Entita osobního kontaktu pracovníka neexportuje osobní kontakty s typem nadřazeného vztahu</span><span class="sxs-lookup"><span data-stu-id="35e5d-113">The Worker personal contact person entity doesn't export personal contacts with a parent relationship type</span></span>

<span data-ttu-id="35e5d-114">V tomto vydání entita **Soukromá kontaktní osoba pracovníka** exportuje všechny typy vztahů.</span><span class="sxs-lookup"><span data-stu-id="35e5d-114">With this release, the **Worker personal contact person** entity exports all relationship types.</span></span>

## <a name="the-hcmpositionworkerassignmentv2entity-should-be-part-of-the-ceridian-payroll-integration-package-by-default-448506"></a><span data-ttu-id="35e5d-115">Entita HcmPositionWorkerAssignmentV2Entity by měla být ve výchozím nastavení součástí integračního balíčku pro mzdové systémy Ceridian (448506)</span><span class="sxs-lookup"><span data-stu-id="35e5d-115">The HcmPositionWorkerAssignmentV2Entity should be part of the Ceridian payroll integration package by default (448506)</span></span>

<span data-ttu-id="35e5d-116">S touto změnou je entita **HcmPositionWorkerAssignmentV2Entity** součástí balíčku integrace mezd v systému Ceridian.</span><span class="sxs-lookup"><span data-stu-id="35e5d-116">With this change, the **HcmPositionWorkerAssignmentV2Entity** is included in the Ceridian payroll integration package.</span></span>

## <a name="in-preview"></a><span data-ttu-id="35e5d-117">Náhled</span><span class="sxs-lookup"><span data-stu-id="35e5d-117">In preview</span></span>

## <a name="database-logging"></a><span data-ttu-id="35e5d-118">Protokolování databáze</span><span class="sxs-lookup"><span data-stu-id="35e5d-118">Database logging</span></span>

<span data-ttu-id="35e5d-119">Funkce protokolování databáze umožňuje určit, které tabulky a pole mají být monitorovány.</span><span class="sxs-lookup"><span data-stu-id="35e5d-119">The database logging feature allows you to determine which tables and fields to monitor.</span></span> <span data-ttu-id="35e5d-120">Umožňuje také určit události, které by měly spustit sledování změn.</span><span class="sxs-lookup"><span data-stu-id="35e5d-120">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="35e5d-121">Pomocí funkcí protokolování databáze se můžete podívat na tyto změny v průběhu času.</span><span class="sxs-lookup"><span data-stu-id="35e5d-121">You use database logging capabilities to see these changes over time.</span></span> <span data-ttu-id="35e5d-122">Další informace získáte v rématu [Konfigurace a správa protokolování databáze](hr-admin-database-logging.md).</span><span class="sxs-lookup"><span data-stu-id="35e5d-122">For more information, see [Configure and manage database logging](hr-admin-database-logging.md).</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="35e5d-123">Aplikace Human Resources v Teams</span><span class="sxs-lookup"><span data-stu-id="35e5d-123">Human Resources application in Teams</span></span>

<span data-ttu-id="35e5d-124">Zaměstnanci mohou prohlížet a požadovat pracovní volno v rámci Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="35e5d-124">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="35e5d-125">Mohou interagovat s robotem a vytvářet žádosti o dovolenou.</span><span class="sxs-lookup"><span data-stu-id="35e5d-125">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="35e5d-126">Další informace viz [Aplikace Human Resources v Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span><span class="sxs-lookup"><span data-stu-id="35e5d-126">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="35e5d-127">Entity právy datových rámců (DMF) pro správu zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="35e5d-127">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="35e5d-128">Zvýhodněné účetní jednotky se uvolňují.</span><span class="sxs-lookup"><span data-stu-id="35e5d-128">Benefits management entities are releasing.</span></span> <span data-ttu-id="35e5d-129">Entity DMF umožňují import a export dat pro snadnou konfiguraci správy výhod.</span><span class="sxs-lookup"><span data-stu-id="35e5d-129">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="35e5d-130">K přesunutí dat bude k dispozici šablona správy výhod.</span><span class="sxs-lookup"><span data-stu-id="35e5d-130">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="35e5d-131">Šablona exportuje a importuje data sekvenčně, aby respektovala datové závislosti.</span><span class="sxs-lookup"><span data-stu-id="35e5d-131">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="35e5d-132">Nákup a prodej pracovního volna</span><span class="sxs-lookup"><span data-stu-id="35e5d-132">Buy and sell leave</span></span> 

<span data-ttu-id="35e5d-133">Některé organizace poskytují výhodu, která zaměstnancům umožňuje nakupovat nebo prodávat dovolenou.</span><span class="sxs-lookup"><span data-stu-id="35e5d-133">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="35e5d-134">Tento proces je často řízen ručně.</span><span class="sxs-lookup"><span data-stu-id="35e5d-134">This process is often managed manually.</span></span> <span data-ttu-id="35e5d-135">Tato funkce automatizuje správu zásad a požadavků oddělení lidských zdrojů.</span><span class="sxs-lookup"><span data-stu-id="35e5d-135">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="35e5d-136">Usnadňuje proces správy dovolených a pomáhá eliminovat chyby.</span><span class="sxs-lookup"><span data-stu-id="35e5d-136">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="35e5d-137">Další informace naleznete zde:</span><span class="sxs-lookup"><span data-stu-id="35e5d-137">For more information, see:</span></span>

- [<span data-ttu-id="35e5d-138">Správa zásad nákupu a prodeje pracovního volna</span><span class="sxs-lookup"><span data-stu-id="35e5d-138">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="35e5d-139">Nákup a prodej pracovního volna</span><span class="sxs-lookup"><span data-stu-id="35e5d-139">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="35e5d-140">Časové rozlišení pracovního volna pro jednu společnost nebo jeden plán</span><span class="sxs-lookup"><span data-stu-id="35e5d-140">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="35e5d-141">Zákazníci mohou zpracovat časové rozlišení pro jednu společnost nebo jeden plán dovolené a nepřítomnosti.</span><span class="sxs-lookup"><span data-stu-id="35e5d-141">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="35e5d-142">Tato schopnost objasňuje proces časového rozlišení pro zákazníky s různými roky dovolené nebo zásadami časového rozlišení dovolené.</span><span class="sxs-lookup"><span data-stu-id="35e5d-142">This ability provides clarity into the accrual process for customers with different leave years or leave accrual policies.</span></span> <span data-ttu-id="35e5d-143">Další informace získáte v části [Časové rozlišení dovolené podle společnosti nebo plánu dovolených](hr-leave-and-absence-accrue.md).</span><span class="sxs-lookup"><span data-stu-id="35e5d-143">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="35e5d-144">Přidání příloh k požadavkům na volno</span><span class="sxs-lookup"><span data-stu-id="35e5d-144">Add attachments to time off requests</span></span>

<span data-ttu-id="35e5d-145">Schopnost přidávat přílohy ke schváleným požadavkům na dovolenou je v současném prostředí COVID-19 kritická.</span><span class="sxs-lookup"><span data-stu-id="35e5d-145">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="35e5d-146">Zaměstnanci nyní mohou tyto přílohy přidávat.</span><span class="sxs-lookup"><span data-stu-id="35e5d-146">Employees can now add these attachments.</span></span> <span data-ttu-id="35e5d-147">Mají také podrobnější přehled o tom, jak jsou aktualizovány žádosti o dovolenou.</span><span class="sxs-lookup"><span data-stu-id="35e5d-147">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="35e5d-148">Další informace získáte v části [Přidání přílohy k existující žádosti](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span><span class="sxs-lookup"><span data-stu-id="35e5d-148">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="35e5d-149">Přidání kódu důvodu k časově rozlišeným pozastavením</span><span class="sxs-lookup"><span data-stu-id="35e5d-149">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="35e5d-150">K akruálnímu pozastavení byly přidány kódy důvodů.</span><span class="sxs-lookup"><span data-stu-id="35e5d-150">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="35e5d-151">Pravidla pro převod do dalšího období</span><span class="sxs-lookup"><span data-stu-id="35e5d-151">Carry forward rules</span></span> 

<span data-ttu-id="35e5d-152">Můžete určit typ převodu pracovního volna do dalšího období pro převod zůstatků, kde byly převedeny úpravy převodu do dalšího období.</span><span class="sxs-lookup"><span data-stu-id="35e5d-152">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="35e5d-153">Pokud například zaměstnanec přenese deset dní dopředu, můžete pro tyto 10 dny vybrat jiný typ pracovního volna.</span><span class="sxs-lookup"><span data-stu-id="35e5d-153">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="35e5d-154">Další informace naleznete v tématu [Konfigurace typů pracovního volna a absence](hr-leave-and-absence-types.md).</span><span class="sxs-lookup"><span data-stu-id="35e5d-154">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="35e5d-155">Časové rozlišení pozastavení dovolené pro zadané typy dovolené</span><span class="sxs-lookup"><span data-stu-id="35e5d-155">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="35e5d-156">Můžete vytvořit pravidlo pro pozastavení přírůstků dovolené pro zaměstnance s požadavky na dovolenou zadanými pro neplacenou dovolenou.</span><span class="sxs-lookup"><span data-stu-id="35e5d-156">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="35e5d-157">Neplacená dovolená může být zadána, ale nemusí.</span><span class="sxs-lookup"><span data-stu-id="35e5d-157">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="35e5d-158">Dovolenou můžete pozastavit na základě jiného typu dovolené.</span><span class="sxs-lookup"><span data-stu-id="35e5d-158">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="35e5d-159">Entita DMF dostupná pro pozastavení časového rozlišení</span><span class="sxs-lookup"><span data-stu-id="35e5d-159">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="35e5d-160">Entita DMF je nyní k dispozici pro akruální pozastavení</span><span class="sxs-lookup"><span data-stu-id="35e5d-160">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="35e5d-161">Již brzy</span><span class="sxs-lookup"><span data-stu-id="35e5d-161">Coming soon</span></span>

## <a name="new-platform-capabilities"></a><span data-ttu-id="35e5d-162">Nové možnosti platformy</span><span class="sxs-lookup"><span data-stu-id="35e5d-162">New platform capabilities</span></span> 

<span data-ttu-id="35e5d-163">Pomocí personalizace budete moci nastavovat pole jako povinná.</span><span class="sxs-lookup"><span data-stu-id="35e5d-163">You'll be able to make fields mandatory by using personalization.</span></span> <span data-ttu-id="35e5d-164">Tato funkce vyžaduje, abyste povolili **uložená zobrazení**.</span><span class="sxs-lookup"><span data-stu-id="35e5d-164">This feature will require you to enable **Saved views**.</span></span>

## <a name="configure-the-name-of-employee-self-service"></a><span data-ttu-id="35e5d-165">Konfigurace samoobsluhy pro zaměstnance</span><span class="sxs-lookup"><span data-stu-id="35e5d-165">Configure the name of Employee self-service</span></span>

<span data-ttu-id="35e5d-166">V parametrech Lidské zdroje bude k dispozici nová možnost aktualizace názvu pracovního prostoru Zaměstnanecká samoobsluha na Samoobsluha.</span><span class="sxs-lookup"><span data-stu-id="35e5d-166">A new option will be available in Human Resources parameters to update the name of the Employee self service workspace to Self service.</span></span> 

## <a name="see-also"></a><span data-ttu-id="35e5d-167">Viz také</span><span class="sxs-lookup"><span data-stu-id="35e5d-167">See also</span></span>

[<span data-ttu-id="35e5d-168">Co je nového a co se změnilo v Human Resources</span><span class="sxs-lookup"><span data-stu-id="35e5d-168">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="35e5d-169">Přehled produktu Dynamics 365 Human Resources vydání 2019 vlny 2</span><span class="sxs-lookup"><span data-stu-id="35e5d-169">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="35e5d-170">Aktualizace procesu</span><span class="sxs-lookup"><span data-stu-id="35e5d-170">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="35e5d-171">Správa funkcí</span><span class="sxs-lookup"><span data-stu-id="35e5d-171">Manage features</span></span>](hr-admin-manage-features.md)