---
title: "Projektové smlouvy"
description: "Tento článek popisuje projektové smlouvy (obsahuje i příklady), které můžete vytvořit pro různé typy projektů a zdroje financování, dále způsoby, jak lze spravovat smlouvy a fakturovat odběratele projektu v aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: d13362acf70edc03a47662c4c3eff680cc04bd8f
ms.contentlocale: cs-cz
ms.lasthandoff: 07/18/2017

---

# <a name="project-contracts"></a><span data-ttu-id="4d1b6-103">Projektové smlouvy</span><span class="sxs-lookup"><span data-stu-id="4d1b6-103">Project contracts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="4d1b6-104">Tento článek popisuje projektové smlouvy (obsahuje i příklady), které můžete vytvořit pro různé typy projektů a zdroje financování, dále způsoby, jak lze spravovat smlouvy a fakturovat odběratele projektu v aplikaci Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-104">This article describes and provides examples of the project contracts that you can create for various types of projects and funding sources, and how you can manage contracts and invoice project customers in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span>

<span data-ttu-id="4d1b6-105">Typ projektu, který vytvoříte pro smlouvu projektu, určuje metodu použitou při fakturaci odběratelům projektu.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-105">The type of project that you create for a project contract determines the method that is used to invoice project customers.</span></span> <span data-ttu-id="4d1b6-106">Můžete změnit projektovou smlouvu a související projekt, ale nelze změnit typ projektu.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-106">You can change a project contract and the related project, but you can't change the project type.</span></span> 

<span data-ttu-id="4d1b6-107">Pomocí projektové smlouvy můžete fakturovat jeden nebo několik projektů současně.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-107">By using a project contract, you can invoice one or more projects at the same time.</span></span> <span data-ttu-id="4d1b6-108">Smlouva projektu rovněž pomáhá zajistit, aby byl pro každý dílčí projekt v projektové struktuře použit stejný fakturační postup.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-108">The project contract also helps guarantee a consistent invoicing procedure for every subproject in a project structure.</span></span> 

<span data-ttu-id="4d1b6-109">Každý projekt, který bude fakturován, musí být přidružen k projektové smlouvě.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-109">Every project that will be invoiced must be associated with a project contract.</span></span> <span data-ttu-id="4d1b6-110">Nastavení projektové smlouvy platí pro všechny projekty a dílčí projekty, které jsou přidruženy k dané projektové smlouvě.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-110">The settings for a project contract apply to all projects and subprojects that are associated with that project contract.</span></span> 

<span data-ttu-id="4d1b6-111">Projektová smlouva může určit jeden nebo více zdrojů financování.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-111">A project contract can specify one or more sources of funding.</span></span> <span data-ttu-id="4d1b6-112">Díky tomu je možné rozdělit účtování mezi více investorů, nastavit limity financování, aby zdrojům financování nebyla účtována větší než určená částka, a nakonfigurovat pravidla financování pro účtování výdajů.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-112">Therefore, you can split the billing among multiple funders, set up funding limits so that funding sources are not billed more than a specified amount, and configure funding rules for charging expenditures.</span></span>

## <a name="funding-for-project-contracts"></a><span data-ttu-id="4d1b6-113">Financování pro smlouvy projektu</span><span class="sxs-lookup"><span data-stu-id="4d1b6-113">Funding for project contracts</span></span>
<span data-ttu-id="4d1b6-114">Některé projektové smlouvy uvádí, že více stran sdílí odpovědnost za financování nákladů na projekt.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-114">Some project contracts specify that multiple parties share the responsibility for funding the project costs.</span></span> <span data-ttu-id="4d1b6-115">Několik příkladů:</span><span class="sxs-lookup"><span data-stu-id="4d1b6-115">Here are some examples:</span></span>

-   <span data-ttu-id="4d1b6-116">Velký odběratel, která má několik divizí, požaduje, aby bylo financování projektu rozděleno dle divizí.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-116">A large customer that has multiple divisions requests that funding of a project be split by division.</span></span>
-   <span data-ttu-id="4d1b6-117">Vaše společnost sdílí náklady na velký projekt s externí organizací.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-117">Your company shares the costs of a large project with an external organization.</span></span>
-   <span data-ttu-id="4d1b6-118">Projekt cesty je financován společně dvěma obcemi.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-118">A  road project is co-funded by two municipalities.</span></span>
-   <span data-ttu-id="4d1b6-119">Projekt mostu je financován státním grantem a soukromou společností.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-119">A bridge project is funded by a government grant and a private corporation.</span></span>

<span data-ttu-id="4d1b6-120">V aplikaci Finance and Operations můžete rozdělit účtování pro jednu transakci nebo celý projekt mezi více odběratelů, grantů nebo organizací.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-120">In Finance and Operations, you can split the billing for a single transaction or an entire project among multiple customers, grants, or organizations.</span></span> 

<span data-ttu-id="4d1b6-121">V projektech s více investory se všechny strany, které přispívají k financování projektu s rozšířeným financováním, nazývají zdroje financování.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-121">In projects that have multiple funders, all parties that contribute to the funding of an advanced funding project are called funding sources.</span></span> <span data-ttu-id="4d1b6-122">Po definování odběratele, organizace nebo grantu jako zdroje financování může být přiřazen k jedné nebo více pravidlům financování.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-122">After a customer, organization, or grant is defined as a funding source, it can be assigned to one or more funding rules.</span></span> <span data-ttu-id="4d1b6-123">Pravidla financování obsahují kritéria, která určují, jak jsou náklady přidělovány různým zdrojům financování pro projekt.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-123">Funding rules contain the criteria that determines how charges are allocated to the various funding sources for a project.</span></span> 

<span data-ttu-id="4d1b6-124">Vzhledem k tomu, že položky na skladě, jako jsou ty, které se zobrazí v nákupním žádankách a nákupních objednávkách, nelze rozdělit, nelze rozdělit částky nákladů mezi více zdrojů financování v době distribuce.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-124">Because stocked items, such as those that appear on purchase requisitions and purchase orders, can't be split, the cost amount can't be split among multiple funding sources at the time of distribution.</span></span> <span data-ttu-id="4d1b6-125">Hodnota zdroje financování tedy zůstane 0 (nula), dokud nebude zaúčtován skladový výdej.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-125">Therefore, the funding source value remains 0 (zero) until the inventory issue is posted.</span></span> <span data-ttu-id="4d1b6-126">Při zaúčtování skladového výdeje bude částka nákladů rozdělena podle pravidel rozúčtování pro projekt.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-126">When the inventory issue is posted, the cost amount is distributed according to the account distribution rules for the project.</span></span>

<span data-ttu-id="4d1b6-127">Zde jsou některé kroky, které vám usnadňují rozdělení účtování mezi více zdrojů financování:</span><span class="sxs-lookup"><span data-stu-id="4d1b6-127">Here are some steps that you can take to make it easier to split the billing among multiple funding sources:</span></span>

-   <span data-ttu-id="4d1b6-128">Určete, že všechny transakce, které jsou zadány pro projekt, používají stejnou prodejní měnu jako projektová smlouva.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-128">Specify that all transactions that are entered for a project use the same sales currency as the project contract.</span></span>
-   <span data-ttu-id="4d1b6-129">Nastavte limity financování tak, aby zdroj financování nebyl fakturován více, než je zadaná částka projektu.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-129">Set up funding limits, so that a funding source isn't invoiced more than a specified amount toward a project.</span></span>
-   <span data-ttu-id="4d1b6-130">Konfigurujte pravidla financování a limity financování pro každého pracovníka, položku, kategorii, skupiny kategorií a typ transakce (nebo pro všechny typy transakcí).</span><span class="sxs-lookup"><span data-stu-id="4d1b6-130">Configure funding rules and funding limits for each worker, item, category, category group, and transaction type (or for all transaction types).</span></span>
-   <span data-ttu-id="4d1b6-131">Vyberte volitelná počáteční a koncová data vymezující období, kdy každé pravidlo financování platí.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-131">Select optional start and end dates to define the period when each funding rule is valid.</span></span>
-   <span data-ttu-id="4d1b6-132">Zadejte procentuální hodnotu, za kterou je zodpovědný každý zdroj financování.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-132">Specify the percentage that each funding source is responsible for.</span></span>
-   <span data-ttu-id="4d1b6-133">Určete, jaký zdroj financování je odpovědný za zaokrouhlení rozdílů, které jsou způsobeny výpočty přidělení financování.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-133">Specify which funding source is responsible for rounding differences that are caused by funding allocation calculations.</span></span>
-   <span data-ttu-id="4d1b6-134">Nastavte pravidla, která určují, jak jsou náklady projektu fakturovány externím odběratelům a účtovány interním organizacím.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-134">Set up rules that determine how project costs are invoiced to external customers and charged to internal organizations.</span></span>
-   <span data-ttu-id="4d1b6-135">Zaznamenejte transakce na účet blokovaného financování, dokud nejsou získány další finanční prostředky nebo se nerozhodnete nést náklady interně.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-135">Record transactions in an on-hold funding account until additional funding can be obtained, or until you decide to bear the costs internally.</span></span>

<span data-ttu-id="4d1b6-136">Chcete-li určit daňovou skupinu a přidružit ji k transakci, projekt vyhledává přidělování daňové skupiny.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-136">To determine which tax group to associate with a transaction, the project is searched for a tax group assignment.</span></span> <span data-ttu-id="4d1b6-137">Pokud nebylo provedeno přiřazení žádné daňové skupiny na úrovni projektu, bude vyhledána projektová smlouva.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-137">If no tax group assignment has been made at the project level, the project contract is searched.</span></span>

### <a name="example-multiple-funding-sources-simple"></a><span data-ttu-id="4d1b6-138">Příklad: Více zdrojů financování (jednoduché)</span><span class="sxs-lookup"><span data-stu-id="4d1b6-138">Example: Multiple funding sources (simple)</span></span>

<span data-ttu-id="4d1b6-139">Následující tabulka obsahuje situace pro správu přidělení financování mezi více zdrojů financování.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-139">The following table provides scenarios for managing funding allocation among multiple funding sources.</span></span> <span data-ttu-id="4d1b6-140">Tyto situace jsou založeny na následujících předpokladech:</span><span class="sxs-lookup"><span data-stu-id="4d1b6-140">These scenarios are based on the following assumptions:</span></span>

-   <span data-ttu-id="4d1b6-141">Nastavení priority se promítnou do přiřazení prostředků před použitím jiných kritérií pravidla financování.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-141">Priority settings are factored into the allocation of funds before other funding rule criteria are applied.</span></span>
-   <span data-ttu-id="4d1b6-142">Nebyl zadán žádný rozsah dat k určení období d v případě, že pravidlo financování platí.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-142">No date range has been specified to define the period d when the funding rule is valid.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4d1b6-143"><strong>Scénář</strong></span><span class="sxs-lookup"><span data-stu-id="4d1b6-143"><strong>Scenario</strong></span></span></td>
<td><span data-ttu-id="4d1b6-144"><strong>Zdroj financování </strong></span><span class="sxs-lookup"><span data-stu-id="4d1b6-144"><strong>Funding source</strong></span></span></td>
<td><span data-ttu-id="4d1b6-145"><strong>Přidělená procenta </strong></span><span class="sxs-lookup"><span data-stu-id="4d1b6-145"><strong>Allocation percentage</strong></span></span></td>
<td><span data-ttu-id="4d1b6-146"><strong>Priorita přidělení </strong></span><span class="sxs-lookup"><span data-stu-id="4d1b6-146"><strong>Allocation priority</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d1b6-147">Chcete přidělit náklady jednomu zdroji financování do vyčerpání finančních prostředků, přidělte náklady druhému zdroji financování, dokud nebudou vyčerpány jeho finanční prostředky, a nakonec přidělte zbývající náklady třetímu zdroji financování.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-147">You want to allocate costs to one funding source until its funds are exhausted, allocate costs to a second funding source until its funds are exhausted, and finally allocate the remaining costs to a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="4d1b6-148">Zdroj　financování　1</span><span class="sxs-lookup"><span data-stu-id="4d1b6-148">Funding　source　1</span></span></li>
<li><span data-ttu-id="4d1b6-149">Zdroj　financování　2</span><span class="sxs-lookup"><span data-stu-id="4d1b6-149">Funding　source　2</span></span></li>
<li><span data-ttu-id="4d1b6-150">Zdroj　financování　3</span><span class="sxs-lookup"><span data-stu-id="4d1b6-150">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="4d1b6-151">100 %</span><span class="sxs-lookup"><span data-stu-id="4d1b6-151">100%</span></span></li>
<li><span data-ttu-id="4d1b6-152">100 %</span><span class="sxs-lookup"><span data-stu-id="4d1b6-152">100%</span></span></li>
<li><span data-ttu-id="4d1b6-153">100 %</span><span class="sxs-lookup"><span data-stu-id="4d1b6-153">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="4d1b6-154">1</span><span class="sxs-lookup"><span data-stu-id="4d1b6-154">1</span></span></li>
<li><span data-ttu-id="4d1b6-155">2</span><span class="sxs-lookup"><span data-stu-id="4d1b6-155">2</span></span></li>
<li><span data-ttu-id="4d1b6-156">3</span><span class="sxs-lookup"><span data-stu-id="4d1b6-156">3</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d1b6-157">Chcete přidělit 75 procent nákladů jednomu zdroji financování a 25 % druhému zdroji financování.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-157">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="4d1b6-158">Pokud je některý z těchto zdrojů financování vyčerpán, chcete zbývající náklady uhradit ze třetího zdroje financování.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-158">When either of those funding sources is exhausted, you want to pay the remaining costs from a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="4d1b6-159">Zdroj　financování　1</span><span class="sxs-lookup"><span data-stu-id="4d1b6-159">Funding　source　1</span></span></li>
<li><span data-ttu-id="4d1b6-160">Zdroj　financování　2</span><span class="sxs-lookup"><span data-stu-id="4d1b6-160">Funding　source　2</span></span></li>
<li><span data-ttu-id="4d1b6-161">Zdroj　financování　3</span><span class="sxs-lookup"><span data-stu-id="4d1b6-161">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="4d1b6-162">75 %</span><span class="sxs-lookup"><span data-stu-id="4d1b6-162">75%</span></span></li>
<li><span data-ttu-id="4d1b6-163">25 %</span><span class="sxs-lookup"><span data-stu-id="4d1b6-163">25%</span></span></li>
<li><span data-ttu-id="4d1b6-164">100 %</span><span class="sxs-lookup"><span data-stu-id="4d1b6-164">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="4d1b6-165">1</span><span class="sxs-lookup"><span data-stu-id="4d1b6-165">1</span></span></li>
<li><span data-ttu-id="4d1b6-166">1</span><span class="sxs-lookup"><span data-stu-id="4d1b6-166">1</span></span></li>
<li><span data-ttu-id="4d1b6-167">2</span><span class="sxs-lookup"><span data-stu-id="4d1b6-167">2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d1b6-168">Chcete přidělit 75 procent nákladů jednomu zdroji financování a 25 % druhému zdroji financování.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-168">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="4d1b6-169">Pokud je některý z těchto zdrojů financování vyčerpán, chcete rozdělit zbývající náklady mezi třetí zdroj financování a čtvrtý zdroj financování.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-169">When either of those funding sources is exhausted, you want to split the remaining costs between a third funding source and a fourth funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="4d1b6-170">Zdroj　financování　1</span><span class="sxs-lookup"><span data-stu-id="4d1b6-170">Funding　source　1</span></span></li>
<li><span data-ttu-id="4d1b6-171">Zdroj　financování　2</span><span class="sxs-lookup"><span data-stu-id="4d1b6-171">Funding　source　2</span></span></li>
<li><span data-ttu-id="4d1b6-172">Zdroj　financování　3</span><span class="sxs-lookup"><span data-stu-id="4d1b6-172">Funding　source　3</span></span></li>
<li><span data-ttu-id="4d1b6-173">Zdroj　financování　4</span><span class="sxs-lookup"><span data-stu-id="4d1b6-173">Funding　source　4</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="4d1b6-174">75 %</span><span class="sxs-lookup"><span data-stu-id="4d1b6-174">75%</span></span></li>
<li><span data-ttu-id="4d1b6-175">25 %</span><span class="sxs-lookup"><span data-stu-id="4d1b6-175">25%</span></span></li>
<li><span data-ttu-id="4d1b6-176">50 %</span><span class="sxs-lookup"><span data-stu-id="4d1b6-176">50%</span></span></li>
<li><span data-ttu-id="4d1b6-177">50 %</span><span class="sxs-lookup"><span data-stu-id="4d1b6-177">50%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="4d1b6-178">1</span><span class="sxs-lookup"><span data-stu-id="4d1b6-178">1</span></span></li>
<li><span data-ttu-id="4d1b6-179">1</span><span class="sxs-lookup"><span data-stu-id="4d1b6-179">1</span></span></li>
<li><span data-ttu-id="4d1b6-180">2</span><span class="sxs-lookup"><span data-stu-id="4d1b6-180">2</span></span></li>
<li><span data-ttu-id="4d1b6-181">2</span><span class="sxs-lookup"><span data-stu-id="4d1b6-181">2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d1b6-182">Chcete přidělit prvních 25 procent nákladů jednomu zdroji financování a zbytek druhému zdroji financování.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-182">You want to allocate the first 25 percent of costs to one funding source and the rest to a second funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="4d1b6-183">Zdroj　financování　1</span><span class="sxs-lookup"><span data-stu-id="4d1b6-183">Funding　source　1</span></span></li>
<li><span data-ttu-id="4d1b6-184">Zdroj　financování　2</span><span class="sxs-lookup"><span data-stu-id="4d1b6-184">Funding　source　2</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="4d1b6-185">25 %</span><span class="sxs-lookup"><span data-stu-id="4d1b6-185">25%</span></span></li>
<li><span data-ttu-id="4d1b6-186">100 %</span><span class="sxs-lookup"><span data-stu-id="4d1b6-186">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="4d1b6-187">1</span><span class="sxs-lookup"><span data-stu-id="4d1b6-187">1</span></span></li>
<li><span data-ttu-id="4d1b6-188">2</span><span class="sxs-lookup"><span data-stu-id="4d1b6-188">2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a><span data-ttu-id="4d1b6-189">Příklad: Více zdrojů financování (složité)</span><span class="sxs-lookup"><span data-stu-id="4d1b6-189">Example: Multiple funding sources (complex)</span></span>

<span data-ttu-id="4d1b6-190">K dispozici jsou tři zdroje financování, které chcete použít v následujícím pořadí:</span><span class="sxs-lookup"><span data-stu-id="4d1b6-190">You have three funding sources that you want to use in the following order:</span></span>

1.  <span data-ttu-id="4d1b6-191">Použijte zdroj financování 2 a zdroj financování 3 rovnoměrně, dokud nebude zdroj financování 2 vyčerpán.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-191">Use funding source 2 and funding source 3 equally until funding source 2 is exhausted.</span></span>
2.  <span data-ttu-id="4d1b6-192">Pokračujte v používání zdroje financování 3, dokud jej nevyčerpáte.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-192">Continue to use funding source 3 until it is exhausted.</span></span>
3.  <span data-ttu-id="4d1b6-193">Použijte zdroj financování 1, až bude zdroj financování 3 vyčerpán.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-193">Use funding source 1 after funding source 3 is exhausted.</span></span>

<span data-ttu-id="4d1b6-194">Chcete-li tento cíl splnit, postupujte následovně:</span><span class="sxs-lookup"><span data-stu-id="4d1b6-194">To accomplish this goal, you must do the following:</span></span>

-   <span data-ttu-id="4d1b6-195">Nastavte limity financování pro zdroj financování 2 a zdroj financování 3, odpovídající jejím částkám.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-195">Set up funding limits for funding source 2 and funding source 3, for their respective amounts.</span></span>
-   <span data-ttu-id="4d1b6-196">Vytvořte následující pravidla financování:</span><span class="sxs-lookup"><span data-stu-id="4d1b6-196">Create the following funding rules:</span></span>
    -   <span data-ttu-id="4d1b6-197">Pravidlo 1 (Priorita 1): Přidělte 50 procent transakcí financování zdroji financování 2 a 50 procent zdroji financování 3.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-197">Rule 1 (Priority 1): Allocate 50 percent of transactions to funding source 2 and 50 percent to funding source 3.</span></span>
    -   <span data-ttu-id="4d1b6-198">Pravidlo 2 (Priorita 2): Přidělte 100 procent transakcí zdroji financování 3.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-198">Rule 2 (Priority 2): Allocate 100 percent of transactions to funding source 3.</span></span>
    -   <span data-ttu-id="4d1b6-199">Pravidlo 3 (Priorita 3): Přidělte 100 procent transakcí zdroji financování 1.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-199">Rule 3 (Priority 3): Allocate 100 percent of transactions to funding source 1.</span></span>

<span data-ttu-id="4d1b6-200">Toto nastavení funguje, protože transakce jsou kontrolovány dle pravidel a limitů, aby bylo možné určit, zda některé z nich platí pro transakci.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-200">This setup works because transactions are checked against rules and limits to determine whether any of them apply to the transaction.</span></span> <span data-ttu-id="4d1b6-201">Pokud pro transakci neplatí žádné konkrétní pravidlo nebo limit, platí pravidlo Všechny transakce.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-201">If no specific rules or limits apply to the transaction, the All transactions rule applies.</span></span> <span data-ttu-id="4d1b6-202">Pravidlo Všechny transakce platí pro všechny transakce.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-202">The All transactions rule matches all transactions.</span></span> 

<span data-ttu-id="4d1b6-203">Je-li nalezeno pravidlo, které odpovídá transakci, je nejdříve použito procento přidělené danému pravidlu, ale až po kontrole shod oproti všem limitům, které byly nastaveny.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-203">If a rule is found that matches a transaction, the percentage that has been allocated in that rule is applied first, but only after the matches are checked against any limits that have been set up.</span></span> <span data-ttu-id="4d1b6-204">Pokud byl splněn limit a byly vyčerpány prostředky zdroje financování, pravidlo financování přidružené k limitu financování bude ignorováno a program zkontroluje následující pravidlo, které lze použít.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-204">If a limit has been met, and a funding source’s funds are exhausted, the funding rule that is associated with the funding limit is disregarded, and the program checks for the next rule that applies.</span></span> 

<span data-ttu-id="4d1b6-205">V některých případech lze dle pravidla rozdělit pouze část transakce.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-205">In some cases, only part of a transaction can be allocated under a rule.</span></span> <span data-ttu-id="4d1b6-206">K tomu může dojít, protože bylo dosaženo limitu při přidělení transakce.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-206">This might happen because a limit is reached when the transaction is allocated.</span></span> <span data-ttu-id="4d1b6-207">V tomto případě lze pouze určitou částku přidělit podle tohoto pravidla, jako například 50 procent, každému zdroji financování.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-207">In this case, only a certain amount is allocated according to that rule, such as 50 percent to each funding source.</span></span> <span data-ttu-id="4d1b6-208">To je případ pravidla 1, které je popsáno dříve v tomto oddílu.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-208">This is the case in rule 1, which is described earlier in this section.</span></span> <span data-ttu-id="4d1b6-209">Zbytek bude přidělen podle dalšího pravidla v pořadí.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-209">The remainder is allocated according to the next rule in the sequence.</span></span> 

<span data-ttu-id="4d1b6-210">Následující tabulka zkoumá tuto situaci podrobněji.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-210">The following table examines this scenario in more detail.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4d1b6-211"><strong>Výběr </strong></span><span class="sxs-lookup"><span data-stu-id="4d1b6-211"><strong>Focus</strong></span></span></td>
<td><span data-ttu-id="4d1b6-212"><strong>Podrobnosti </strong></span><span class="sxs-lookup"><span data-stu-id="4d1b6-212"><strong>Details</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d1b6-213">Pravidla financování</span><span class="sxs-lookup"><span data-stu-id="4d1b6-213">Funding rules</span></span></td>
<td><ul>
<li><span data-ttu-id="4d1b6-214">Pravidlo 1 (Priorita 1): Všechny transakce.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-214">Rule 1 (Priority 1): All transactions.</span></span> <span data-ttu-id="4d1b6-215">Přidělte zdroj financování 2 ve výši 50 % a zdroj financování 3 ve výši 50 %.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-215">Allocate funding source 2 at 50% and funding source 3 at 50%.</span></span></li>
<li><span data-ttu-id="4d1b6-216">Pravidlo 2 (Priorita 2): Všechny transakce.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-216">Rule 2 (Priority 2): All transactions.</span></span> <span data-ttu-id="4d1b6-217">Přidělte zdroj financování 3 ve výši 100 %.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-217">Allocate funding source 3 at 100%.</span></span></li>
<li><span data-ttu-id="4d1b6-218">Pravidlo 3 (Priorita 2): Všechny transakce.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-218">Rule 3 (Priority 2): All transactions.</span></span> <span data-ttu-id="4d1b6-219">Přidělte zdroj financování 1 ve výši 100 %.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-219">Allocate funding source 1 at 100%.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d1b6-220">Limity financování</span><span class="sxs-lookup"><span data-stu-id="4d1b6-220">Funding limits</span></span></td>
<td><ul>
<li><span data-ttu-id="4d1b6-221">Limit zdroje financování 1 = 10 000,00</span><span class="sxs-lookup"><span data-stu-id="4d1b6-221">Funding source 1 limit = 10,000.00</span></span></li>
<li><span data-ttu-id="4d1b6-222">Limit zdroje financování 2 = 500,00</span><span class="sxs-lookup"><span data-stu-id="4d1b6-222">Funding source 2 limit = 500.00</span></span></li>
<li><span data-ttu-id="4d1b6-223">Limit zdroje financování 3 = 750,00</span><span class="sxs-lookup"><span data-stu-id="4d1b6-223">Funding source 3 limit = 750.00</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d1b6-224">Transakce 1</span><span class="sxs-lookup"><span data-stu-id="4d1b6-224">Transaction 1</span></span></td>
<td><span data-ttu-id="4d1b6-225"><strong>Částka transakce:</strong> 100,00<strong>Financovaní:</strong> Transakce bude zaplacena pouze podle pravidla 1, protože transakce je plně zaplacena po použití pravidla 1.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-225"><strong>Transaction amount:</strong> 100.00<strong>Funding:</strong> The transaction is paid according to rule 1 only, because the transaction is fully paid after rule 1 is applied.</span></span> <span data-ttu-id="4d1b6-226">Transakce je financována rovnoměrně mezi zdrojem financování 2 a zdrojem financování 3.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-226">The transaction is funded equally between funding source 2 and funding source 3.</span></span>
<ul>
<li><span data-ttu-id="4d1b6-227">Zdroj financování 2: 50,00</span><span class="sxs-lookup"><span data-stu-id="4d1b6-227">Funding source 2: 50.00</span></span></li>
<li><span data-ttu-id="4d1b6-228">Zdroj financování 3: 50,00</span><span class="sxs-lookup"><span data-stu-id="4d1b6-228">Funding source 3: 50.00</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d1b6-229">Transakce 2</span><span class="sxs-lookup"><span data-stu-id="4d1b6-229">Transaction 2</span></span></td>
<td><span data-ttu-id="4d1b6-230"><strong>Částka transakce:</strong> 5 000,00<strong>Financování:</strong> Transakce se vyplácí podle všech tří pravidel.<strong>Pravidlo 1</strong>
</span><span class="sxs-lookup"><span data-stu-id="4d1b6-230"><strong>Transaction amount:</strong> 5,000.00<strong>Funding:</strong> The transaction is paid according to all three rules.<strong>Rule 1</strong>
</span></span><ul>
<li><span data-ttu-id="4d1b6-231">Zdroj financování 2: 450,00</span><span class="sxs-lookup"><span data-stu-id="4d1b6-231">Funding source 2: 450.00</span></span></li>
<li><span data-ttu-id="4d1b6-232">Zdroj financování 3: 450,00</span><span class="sxs-lookup"><span data-stu-id="4d1b6-232">Funding source 3: 450.00</span></span></li>
</ul><span data-ttu-id="4d1b6-233">
<strong>Pravidlo 2</strong>
</span><span class="sxs-lookup"><span data-stu-id="4d1b6-233">
<strong>Rule 2</strong>
</span></span><ul>
<li><span data-ttu-id="4d1b6-234">Zdroj financování 3: 250,00 (= 750,00 – 50,00 – 450,00)</span><span class="sxs-lookup"><span data-stu-id="4d1b6-234">Funding source 3: 250.00 (= 750.00 – 50.00 – 450.00)</span></span></li>
</ul><span data-ttu-id="4d1b6-235">
<strong>Pravidlo 3</strong>
</span><span class="sxs-lookup"><span data-stu-id="4d1b6-235">
<strong>Rule 3</strong>
</span></span><ul>
<li><span data-ttu-id="4d1b6-236">Zdroj financování 1: 3 850,00 (= 5 000,00 – 450,00 – 450,00 – 250,00)</span><span class="sxs-lookup"><span data-stu-id="4d1b6-236">Funding source 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d1b6-237">Celkové prostředky rozdělené pro každý zdroj financování</span><span class="sxs-lookup"><span data-stu-id="4d1b6-237">Total funds that are distributed for each funding source</span></span></td>
<td><ul>
<li><span data-ttu-id="4d1b6-238">Zdroj financování 1: 3 850,00</span><span class="sxs-lookup"><span data-stu-id="4d1b6-238">Funding source 1: 3,850.00</span></span></li>
<li><span data-ttu-id="4d1b6-239">Zdroj financování 2: 500,00</span><span class="sxs-lookup"><span data-stu-id="4d1b6-239">Funding source 2: 500.00</span></span></li>
<li><span data-ttu-id="4d1b6-240">Zdroj financování 3: 750,00</span><span class="sxs-lookup"><span data-stu-id="4d1b6-240">Funding source 3: 750.00</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a><span data-ttu-id="4d1b6-241">Pravidla účtování</span><span class="sxs-lookup"><span data-stu-id="4d1b6-241">Billing rules</span></span>
<span data-ttu-id="4d1b6-242">Když sjednáváte projektovou smlouvu s odběratelem, definujete, kdy a jak můžete fakturovat odběrateli za práci na projektu.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-242">When you negotiate a project contract with a customer, you define how and when you can invoice the customer for work on a project.</span></span> <span data-ttu-id="4d1b6-243">Jakmile nastavíte projektovou smlouvu a projekt, můžete nastavit pravidla účtování pro projekt.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-243">After you set up the project contract and the project, you can set up billing rules for the project.</span></span> <span data-ttu-id="4d1b6-244">Pravidla účtování jsou založena na podmínkách projektu stanovených v projektové smlouvě.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-244">Billing rules are based on the project terms that are specified in the project contract.</span></span> <span data-ttu-id="4d1b6-245">Pravidla účtování, která můžete vytvořit, závisí na podmínkách v projektové smlouvě a typu projektu, jako je Čas a materiál nebo Pevná cena, který přidružíte k pravidlům účtování.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-245">The billing rules that you can create depend on the terms of the project contract and the project type, such as Time and material or Fixed-price, that you associate with the billing rule.</span></span> <span data-ttu-id="4d1b6-246">Můžete vytvořit více než jedno pravidlo pro projektovou smlouvu.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-246">You can create more than one billing rule for a project contract.</span></span> <span data-ttu-id="4d1b6-247">Lze také přiřadit pravidlo účtování více projektům, které jsou přidružené ke stejné projektové smlouvě a mají podobná platební podmínky.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-247">You can also assign a billing rule to multiple projects that are associated with the same project contract and have similar billing terms.</span></span> 

<span data-ttu-id="4d1b6-248">Můžete vytvářet následující typy pravidel účtování:</span><span class="sxs-lookup"><span data-stu-id="4d1b6-248">You can set up the following types of billing rules:</span></span>

-   <span data-ttu-id="4d1b6-249">**Jednotka dodání** – Fakturujte odběratele po dokončení jednotky dodání.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-249">**Unit of delivery** – Invoice a customer when you complete a unit of delivery.</span></span> <span data-ttu-id="4d1b6-250">Jednotky dodání definujete ve smlouvě.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-250">You define the units of delivery in the contract.</span></span>
-   <span data-ttu-id="4d1b6-251">**Průběh** – Fakturujte odběratele po dokončení určitého procenta projektu.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-251">**Progress** – Invoice a customer when you complete a specified percentage of the project.</span></span> <span data-ttu-id="4d1b6-252">Pravidla účtování můžete nastavit pro automatické vypočítání procenta dokončené práce nebo můžete ručně vypočítat procento dokončené práce a částku k fakturaci odběrateli.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-252">You can set up a billing rule to automatically calculate the percentage of work completed, or you can manually calculate the percentage of work completed and the amount to invoice the customer.</span></span>
-   <span data-ttu-id="4d1b6-253">**Milník** – Fakturujte odběratele v plné výši milníku projektu při dosažení milníku.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-253">**Milestone** – Invoice a customer for the full amount of a project milestone when the milestone is reached.</span></span>
-   <span data-ttu-id="4d1b6-254">**Poplatek** – Fakturujte odběratele za služby plus správní poplatek, což je obvykle procento nákladů služby.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-254">**Fee** – Invoice a customer for your services plus a management fee, which is typically a percentage of the cost of services.</span></span>
-   <span data-ttu-id="4d1b6-255">**Čas a materiál** – Fakturujte odběratele za hodnotu času a materiálů použitých v projektu.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-255">**Time and material** – Invoice a customer for the value of time and materials that are used on a project.</span></span>

<span data-ttu-id="4d1b6-256">Pro všechny typy pravidel účtování můžete zadat procento zadržení, o které se mají snížit faktury odběratele, než projekt dosáhne dohodnuté fáze.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-256">For all types of billing rules, you can specify a retention percentage that is deducted from customer invoices until a project reaches an agreed-upon stage.</span></span> <span data-ttu-id="4d1b6-257">Procento zadržení platby je určeno ve smlouvě projektu.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-257">The payment retention percentage is specified in the project contract.</span></span> <span data-ttu-id="4d1b6-258">Částka je vypočítávána na základě a odečtena od celkové hodnoty řádků na faktuře odběratele.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-258">The amount is calculated based on, and subtracted from, the total value of the lines in a customer invoice.</span></span> 

<span data-ttu-id="4d1b6-259">Pro pravidla účtování **Čas a materiál** a **Průběh** je možné přiřadit fakturovatelné kategorie.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-259">For **Time and material** and **Progress** billing rules, you can assign chargeable categories.</span></span> <span data-ttu-id="4d1b6-260">Fakturovatelné kategorie označují transakce, které mají být zahrnuty do faktur odběratelů.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-260">Chargeable categories indicate the transactions that should be included in customer invoices.</span></span> 

<span data-ttu-id="4d1b6-261">Až budete připraveni fakturovat odběrateli, částka k fakturaci pro projekt je vypočtena na základě pravidel účtování a je vygenerován návrh projektové faktury.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-261">When you are ready to invoice the customer, the amount to invoice for the project is calculated based on the billing rules, and a project invoice proposal is generated.</span></span> 

<span data-ttu-id="4d1b6-262">Následující části obsahují příklady, které ukazují, jak nastavit a spravovat pravidla účtování pro projekt.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-262">The following sections provide examples that show how to set up and manage billing rules for a project.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a><span data-ttu-id="4d1b6-263">Příklad: Vytvoření pravidla účtování na základě počtu dodaných jednotek</span><span class="sxs-lookup"><span data-stu-id="4d1b6-263">Example: Create a billing rule that is based on the number of units delivered</span></span>

<span data-ttu-id="4d1b6-264">Vaše organizace uzavře smlouvu na poskytnutí celkem pěti školení zaměstnancům odběratele za cenu 10 000 za relaci školení.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-264">Your organization enters into an agreement to provide a total of five training sessions to a customer’s employees at a cost of 10,000 per training session.</span></span> <span data-ttu-id="4d1b6-265">Fakturujete odběratele po každé vzdělávací relaci.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-265">You invoice the customer after each training session.</span></span> 

<span data-ttu-id="4d1b6-266">Když nastavujete pravidla účtování pro smlouvu, použijte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="4d1b6-266">When you set up the billing rules for the contract, you use the following values:</span></span>

-   <span data-ttu-id="4d1b6-267">Jednotka dodání je jedna relace školení.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-267">The unit of delivery is one training session.</span></span>
-   <span data-ttu-id="4d1b6-268">Jednotková cena je 10 000 za relaci školení.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-268">The unit price is 10,000 per training session.</span></span>
-   <span data-ttu-id="4d1b6-269">Celkový počet jednotek je pět školení.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-269">The total number of units is five training sessions.</span></span>

<span data-ttu-id="4d1b6-270">Po dokončení jedné relace školení můžete vytvořit fakturu na 10 000 za první dodanou jednotku a odeslat fakturu odběrateli.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-270">When you have completed one training session, you can create an invoice for 10,000, for the first unit that was delivered, and send the invoice to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a><span data-ttu-id="4d1b6-271">Příklad: Vytvoření pravidla účtování na základě udaného procenta dokončení projektu (ruční výpočet)</span><span class="sxs-lookup"><span data-stu-id="4d1b6-271">Example: Create a billing rule that is based on a specified percentage of project completion (manual calculation)</span></span>

<span data-ttu-id="4d1b6-272">Vaše organizace, softwarová konzultační firma, uzavře smlouvu s odběratelem na vývoj části produktu, který odběratel vyvíjí.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-272">Your organization, a software consulting firm, enters into an agreement with a customer to develop part of a product that the customer is developing.</span></span> <span data-ttu-id="4d1b6-273">Vaše organizace se zaváže k doručování kódu softwaru během období šesti měsíců.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-273">Your organization agrees to deliver the software code over a period of six months.</span></span> <span data-ttu-id="4d1b6-274">Odběratel souhlasí uhradit vaší organizaci celkem 100 000 za práci.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-274">The customer agrees to pay your organization a total of 100,000 for the work.</span></span> <span data-ttu-id="4d1b6-275">Vytvoříte pravidlo účtování pro fakturaci odběratele na základě procenta dokončené práce na projektu, jak je uvedeno ve smlouvě.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-275">You create a billing rule to invoice the customer based on the percentage of work that is completed on the project, as specified in the contract.</span></span>

-   <span data-ttu-id="4d1b6-276">Na konci prvního měsíce se sejdete s odběratelem, abyste určili procento dokončené práce.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-276">At the end of the first month, you meet with the customer to determine the percentage of work completed.</span></span> <span data-ttu-id="4d1b6-277">Po kontrole projektu vy a odběratel usoudíte, že je projekt dokončen z 15 procent.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-277">After you and the customer review the project, you decide that the project is 15 percent completed.</span></span>
-   <span data-ttu-id="4d1b6-278">Vytvořte fakturu na 15 000 (15 procent ze 100 000) a odešlete ji odběrateli.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-278">You create an invoice for 15,000 (15 percent of 100,000) and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a><span data-ttu-id="4d1b6-279">Příklad: Vytvoření pravidla účtování na základě udaného procenta dokončení projektu (automatický výpočet)</span><span class="sxs-lookup"><span data-stu-id="4d1b6-279">Example: Create a billing rule that is based on a specified percentage of project completion (automatic calculation)</span></span>

<span data-ttu-id="4d1b6-280">Vaše organizace, která se zabývá vývojem softwaru, souhlasí s vývojem balíčku pro mzdové účetnictví pro odběratele za cenu 30 000.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-280">Your organization, a software development firm, agrees to develop a payroll accounting package for a customer for 30,000.</span></span> <span data-ttu-id="4d1b6-281">Odběratel souhlasí uhradit vaší organizaci na základě procenta dokončené práce.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-281">The customer agrees to pay your organization based on the percentage of work completed.</span></span> <span data-ttu-id="4d1b6-282">Náklady na projekt odhadujete na 20 000.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-282">You estimate that the project costs are 20,000.</span></span> <span data-ttu-id="4d1b6-283">Projektová smlouva určuje kategorie práce, které máte použít v procesu účtování.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-283">The project contract specifies the categories of work that you use in the billing process.</span></span> <span data-ttu-id="4d1b6-284">Můžete nastavit pravidla účtování, která automaticky vypočítají částky faktur pro procentuální část práce dokončenou v každé kategorii.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-284">You set up billing rules that automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="4d1b6-285">Nastavte rozpočet pro každou kategorii:</span><span class="sxs-lookup"><span data-stu-id="4d1b6-285">You set up a budget for each category:</span></span>

-   <span data-ttu-id="4d1b6-286">**Vývoj** – náklady 15 000 a výnos 20 000</span><span class="sxs-lookup"><span data-stu-id="4d1b6-286">**Development** – Cost of 15,000 and revenue of 20,000</span></span>
-   <span data-ttu-id="4d1b6-287">**Instalace** – náklady 5 000 a výnos 10 000</span><span class="sxs-lookup"><span data-stu-id="4d1b6-287">**Installation** – Cost of 5,000 and revenue of 10,000</span></span>

<span data-ttu-id="4d1b6-288">Při prvním vytváření faktury odběratele je částka faktury automaticky vypočítána z následujících informací:</span><span class="sxs-lookup"><span data-stu-id="4d1b6-288">When you create a customer invoice for the first time, the invoice amount is automatically calculated based on the following information:</span></span>

-   <span data-ttu-id="4d1b6-289">Za měsíc odešle pracovník na projektu časový rozvrh pro projekt.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-289">After a month, the worker on the project submits a timesheet for the project.</span></span> <span data-ttu-id="4d1b6-290">Náklady na hodiny pracovníka jsou 5 000 za vývoj a 1 000 za instalaci.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-290">The cost of the worker’s hours is 5,000 for development and 1,000 for installation.</span></span> <span data-ttu-id="4d1b6-291">Vývojové práce jsou z 33 procent dokončeny (5 000 skutečné náklady / 15 000 rozpočtové náklady) a instalační práce jsou dokončeny ze 20 procent (1 000 skutečné náklady / 5 000 rozpočtové náklady).</span><span class="sxs-lookup"><span data-stu-id="4d1b6-291">The development work is 33 percent completed (5,000 actual cost/15,000 budget cost), and the installation work is 20 percent completed (1,000 actual cost/5,000 budget cost).</span></span>
-   <span data-ttu-id="4d1b6-292">Částka faktury 8 667 je automaticky vypočtena (33 procent ze 20 000 + 20 procent z 10 000).</span><span class="sxs-lookup"><span data-stu-id="4d1b6-292">The invoice amount of 8,667 is automatically calculated (33 percent of 20,000 + 20 percent of 10,000).</span></span>
-   <span data-ttu-id="4d1b6-293">Vytvořte fakturu na 8 667 a odešlete ji odběrateli.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-293">You create an invoice for 8,667 and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a><span data-ttu-id="4d1b6-294">Příklad: Vytvoření pravidla účtování na základě dohodnutých milníků</span><span class="sxs-lookup"><span data-stu-id="4d1b6-294">Example: Create a billing rule that is based on agreed-upon milestones</span></span>

<span data-ttu-id="4d1b6-295">Vaše organizace, poradenská firma v oblasti managementu, souhlasí s provedením průzkumu trhu pro spotřebitelský produkt, které odběratel plánuje prodávat.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-295">Your organization, a management consulting firm, agrees to conduct market research for a consumer product that the customer plans to sell.</span></span> <span data-ttu-id="4d1b6-296">Zákazník souhlasí s využitím vašich služeb po dobu tří měsíců, počínaje březnem a souhlasí, že vaší organizaci zaplatí 50 000.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-296">The customer agrees to use your services for a period of three months, starting in March, and agrees to pay your organization 50,000.</span></span> <span data-ttu-id="4d1b6-297">Projekt obsahuje tři milníky:</span><span class="sxs-lookup"><span data-stu-id="4d1b6-297">The project has three milestones:</span></span>

-   <span data-ttu-id="4d1b6-298">Milník 1: Shromáždění spotřebitelských dat – 31. března</span><span class="sxs-lookup"><span data-stu-id="4d1b6-298">Milestone 1: Collect consumer data – March 31</span></span>
-   <span data-ttu-id="4d1b6-299">Milník 2: Analýza spotřebitelských dat – 30. dubna</span><span class="sxs-lookup"><span data-stu-id="4d1b6-299">Milestone 2: Analyze consumer data – April 30</span></span>
-   <span data-ttu-id="4d1b6-300">Milník 3: Předložení zprávy o životaschopnosti produktu – 31. května</span><span class="sxs-lookup"><span data-stu-id="4d1b6-300">Milestone 3: Present a product viability proposal – May 31</span></span>

<span data-ttu-id="4d1b6-301">Odběratel souhlasí s platbou 10 000 vaší organizaci za první milník, 20 000 za druhý milník a 20 000 za třetí milník.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-301">The customer agrees to pay your organization 10,000 for the first milestone, 20,000 for the second milestone, and 20,000 for the third milestone.</span></span> 

<span data-ttu-id="4d1b6-302">Při nastavování projektové smlouvy souhlasíte s fakturací odběratele na základě dokončeného milníku.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-302">When you set up the project contract, you agree to bill the customer based on the milestone that has been completed.</span></span> <span data-ttu-id="4d1b6-303">Pravidlo účtování zahrnuje následující kroky:</span><span class="sxs-lookup"><span data-stu-id="4d1b6-303">The billing rule setup includes the following steps:</span></span>

-   <span data-ttu-id="4d1b6-304">Definujte milníky projektu.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-304">Define the project milestones.</span></span>
-   <span data-ttu-id="4d1b6-305">Definujte částku k fakturaci odběratele při dokončení jednotlivých milníků.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-305">Define the amount to invoice the customer when each milestone is completed.</span></span>

<span data-ttu-id="4d1b6-306">Po dokončení první milníku 31. března označte milník jako dokončený a pak vytvořte fakturu na částku 10 000 a odešlete ji odběrateli.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-306">When the first milestone is completed on March 31, you mark the milestone as completed, and then create an invoice for 10,000 and send it to the customer.</span></span> <span data-ttu-id="4d1b6-307">Nelze vytvořit fakturu pro milník, dokud není označen jako dokončený.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-307">You can’t create an invoice for a milestone until you have marked the milestone as completed.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a><span data-ttu-id="4d1b6-308">Příklad: Vytvoření pravidla účtování na základě služeb a správního poplatku</span><span class="sxs-lookup"><span data-stu-id="4d1b6-308">Example: Create a billing rule that is based on services plus a management fee</span></span>

<span data-ttu-id="4d1b6-309">Vaše organizace, která se zabývá poradenstvím v oblasti managementu, souhlasí s provedením průzkumu trhu za účelem vyhodnocení životnosti produktu, který odběratel (maloobchodní společnost), vyvíjí.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-309">Your organization, a management consulting firm, agrees to conduct market research to evaluate the viability of a product that the customer, a retail company, is developing.</span></span> <span data-ttu-id="4d1b6-310">V podmínkách smlouvy je uvedeno, že poskytnete služby tří nejlepších poradců v oblasti managementu, kteří provedou výzkum za náklady na bázi času a materiálu.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-310">The terms of the agreement specify that you will provide the services of your top three management consultants, who will conduct the research on a time-and-materials basis.</span></span> <span data-ttu-id="4d1b6-311">Odběratel se zavazuje platit 100 za hodinu a správní poplatek ve výši 10 procent za konzultační hodiny, které jsou účtovány v projektu.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-311">The customer agrees to pay 100 per hour, plus a 10 percent management fee for the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="4d1b6-312">Při nastavování projektové smlouvy vytvořte pravidlo účtování pro přidání správního poplatku 10 procent za konzultační hodiny účtované v projektu.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-312">When you set up the project contract, create a billing rule to add a 10 percent management fee to the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="4d1b6-313">Při vytváření faktury pro odběratele je odběrateli fakturován správní poplatek 10 procent a náklady na konzultační hodiny.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-313">When you create an invoice for the customer, the customer is billed a 10 percent management fee plus the cost of the consulting hours.</span></span> <span data-ttu-id="4d1b6-314">Například pokud tři konzultanti pracovali celkem 200 hodin na projektu, bude vytvořena faktura na částku 22 000 na základě následující kalkulace:</span><span class="sxs-lookup"><span data-stu-id="4d1b6-314">For example, if the three consultants worked a total of 200 hours on the project, an invoice for 22,000 is created based on the following calculation:</span></span>

-   <span data-ttu-id="4d1b6-315">200 hodin za 100 za hodinu = 20 000</span><span class="sxs-lookup"><span data-stu-id="4d1b6-315">200 hours at 100 per hour = 20,000</span></span>
-   <span data-ttu-id="4d1b6-316">10procentní správní poplatek = 2000</span><span class="sxs-lookup"><span data-stu-id="4d1b6-316">10 percent management fee = 2,000</span></span>
-   <span data-ttu-id="4d1b6-317">Celková fakturovaná částka = 22 000</span><span class="sxs-lookup"><span data-stu-id="4d1b6-317">Total invoice amount = 22,000</span></span>

<span data-ttu-id="4d1b6-318">Pokud poplatky zdaňuje odběratel a vy vyberete skupinu DPH v projektové smlouvě, skupina DPH je automaticky zadána do pravidel účtování pro poplatky.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-318">If fees are taxable to a customer, and you select a sales tax group in the project contract, the sales tax group is automatically entered in a billing rule for fees.</span></span>

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a><span data-ttu-id="4d1b6-319">Příklad: Vytvoření pravidla fakturace pro hodnotu času a materiálu</span><span class="sxs-lookup"><span data-stu-id="4d1b6-319">Example: Create a billing rule for the value of time and materials</span></span>

<span data-ttu-id="4d1b6-320">Vaše organizace, která nabízí poradenství v oblasti softwaru, se zavazuje poskytnout odběrateli pět technických poradců pro práci na projektu vývoje softwaru po dobu následujících šesti měsíců.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-320">Your organization, a software consulting firm, agrees to provide five technical consultants to work on a software development project for a customer for the next six months.</span></span> <span data-ttu-id="4d1b6-321">Odběratel souhlasí s platbou 150 za každou konzultační hodinu a náklady na kancelářské potřeby.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-321">The customer agrees to pay 150 for each consulting hour, plus the cost of office supplies.</span></span> <span data-ttu-id="4d1b6-322">Vaše organizace odešle fakturu odběrateli na konci každého měsíce.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-322">Your organization sends an invoice to the customer at the end of each month.</span></span> 

<span data-ttu-id="4d1b6-323">Při nastavování projektové smlouvy souhlasíte s fakturací odběratele každý měsíc za čas a materiál v projektu.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-323">When you set up the project contract, you agree to bill the customer each month for time and materials on the project.</span></span> <span data-ttu-id="4d1b6-324">Vytvoříte pravidlo účtování, které obsahuje následující informace:</span><span class="sxs-lookup"><span data-stu-id="4d1b6-324">You create a billing rule that includes the following information:</span></span>

-   <span data-ttu-id="4d1b6-325">Časové období smlouvy je šest měsíců.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-325">The contract period is six months.</span></span>
-   <span data-ttu-id="4d1b6-326">Konzultační čas se počítá ze sazby 150 za hodinu.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-326">Consulting time is calculated at a rate of 150 per hour.</span></span>
-   <span data-ttu-id="4d1b6-327">Kancelářské potřeby jsou fakturovány za náklady a celkové náklady na projekt nesmí přesáhnout 10 000.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-327">Office supplies are invoiced at cost, and the total cost for the project must not exceed 10,000.</span></span>
-   <span data-ttu-id="4d1b6-328">Faktura odběratele se vytváří na konci každého kalendářního měsíce během projektu.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-328">You create a customer invoice at the end of each calendar month during the project.</span></span>

<span data-ttu-id="4d1b6-329">Během prvního měsíce je zaznamenáno celkem 800 hodin konzultanty na projektu.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-329">During the first month, a total of 800 hours are recorded by the consultants on the project.</span></span> <span data-ttu-id="4d1b6-330">Náklady na kancelářské potřeby zaúčtované v projektu jsou 2 000.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-330">The cost of office supplies that are charged to the project is 2,000.</span></span> <span data-ttu-id="4d1b6-331">Proto na konci měsíce vytvoříte fakturu na 122 000, která se vypočítá jako 800 hodin za 150 za hodinu a 2 000 za kancelářské potřeby.</span><span class="sxs-lookup"><span data-stu-id="4d1b6-331">Therefore, at the end of the month, you create an invoice for 122,000, which is calculated as 800 hours at 150 per hour, plus 2,000 for office supplies.</span></span>




