---
title: "Konfigurace správy výdajů"
description: "Tento článek popisuje, co je třeba zvážit a jaká rozhodnutí je třeba učinit během procesu plánování před konfigurací oblasti Správa výdajů v aplikaci Microsoft Dynamics 365 for Finance and Operations."
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e213c4436452ddf1d0e22d791c7ee2cee803edc7
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---

# <a name="configure-expense-management"></a><span data-ttu-id="3f7c9-103">Konfigurace správy výdajů</span><span class="sxs-lookup"><span data-stu-id="3f7c9-103">Configure expense management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3f7c9-104">Toto téma popisuje, co je třeba zvážit a jaká rozhodnutí je třeba učinit během procesu plánování před konfigurací oblasti Správa výdajů v aplikaci Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3f7c9-104">This topic describes the considerations and the decisions that you must make during the planning process before you configure Expense management in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="3f7c9-105">Ve správě výdajů můžete ukládat informace například o metodách platby, cestovních žádankách, sestavách výdajů, zásadách atd.</span><span class="sxs-lookup"><span data-stu-id="3f7c9-105">In Expense management, you can store information about payment methods, travel requisitions, expense reports, policies, and so on.</span></span>

<span data-ttu-id="3f7c9-106">Vzhledem k tomu, že mnohá rozhodnutí, která jste učinili při plánování konfigurace pro správu výdajů, vycházejí z hierarchie a finanční struktury organizace, je třeba využít dokumenty plánování pro tyto oblasti.</span><span class="sxs-lookup"><span data-stu-id="3f7c9-106">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="3f7c9-107">Mezipodnikové výdaje</span><span class="sxs-lookup"><span data-stu-id="3f7c9-107">Intercompany expenses</span></span>

<span data-ttu-id="3f7c9-108">Při povolení mezipodnikových výdajů povolíte právnickým osobám a zaměstnancům, aby vystavovali výdaje jménem jiné právnické osoby a vybírali platby od právnické osoby zaměstnání v rámci vaší organizace.</span><span class="sxs-lookup"><span data-stu-id="3f7c9-108">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of another legal entity, and collect payment from the legal entity of employment within your organization.</span></span> <span data-ttu-id="3f7c9-109">Například zaměstnanec v právnické osobě A dokončí projekt pro právnickou osobu B a projektu vzniknou cestovní výdaje.</span><span class="sxs-lookup"><span data-stu-id="3f7c9-109">For example, an employee in legal entity A completes a project for legal entity B, and the project incurs travel related expenses.</span></span> <span data-ttu-id="3f7c9-110">Pokud jsou povoleny mezipodnikové výdaje, může zaměstnanec poté vyplnit vyúčtování výdajů, které zaúčtují výdaje právnické osobě B, a výdaje musí být zaplaceny právnickou osobou A. Pokud vaše organizace nezahrnuje více právnických osob, nemusíte povolit mezipodnikové výdaje.</span><span class="sxs-lookup"><span data-stu-id="3f7c9-110">If intercompany expenses are enabled, the employee can then file an expense report that will post the expense to legal entity B, and the expense must then be paid by legal entity A. If your organization doesn’t have multiple legal entities, you don’t have to enable intercompany expenses.</span></span>

<span data-ttu-id="3f7c9-111">**Rozhodnutí:** Chcete povolit mezipodnikové výdaje?</span><span class="sxs-lookup"><span data-stu-id="3f7c9-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="3f7c9-112">Správa financí</span><span class="sxs-lookup"><span data-stu-id="3f7c9-112">Financial management</span></span>

<span data-ttu-id="3f7c9-113">Správa výdajů je úzce integrována s finanční správou organizace.</span><span class="sxs-lookup"><span data-stu-id="3f7c9-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="3f7c9-114">Řada konfigurací pro správu výdajů bude založena na rozhodnutích, která jste učinili ohledně financí vaší organizace.</span><span class="sxs-lookup"><span data-stu-id="3f7c9-114">Lots of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="3f7c9-115">Následující oddíly popisují různé oblasti, které vyžadují plánování, a rozhodnutí založená na finančních rozhodnutích organizace a pokynech od týmu vedení.</span><span class="sxs-lookup"><span data-stu-id="3f7c9-115">The following sections describe the various areas that require planning and decisions, based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="3f7c9-116">Diety</span><span class="sxs-lookup"><span data-stu-id="3f7c9-116">Per diems</span></span>

<span data-ttu-id="3f7c9-117">Je nutné definovat diety zaměstnance, které vaše organizace poskytuje.</span><span class="sxs-lookup"><span data-stu-id="3f7c9-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="3f7c9-118">Protože diety jsou obvykle použity k pokrytí výdajů, jako je stravování, ubytování nebo jiné vedlejší náklady, můžete vytvořit pravidla pro náhrady denních diet, které vaše organizace nabízí.</span><span class="sxs-lookup"><span data-stu-id="3f7c9-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="3f7c9-119">Denní diety lze nastavit podle roční doby, cíle cesty nebo podle obojího.</span><span class="sxs-lookup"><span data-stu-id="3f7c9-119">per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="3f7c9-120">Při definování pravidla denní diety můžete zadat, aby bylo procento denní diety strženo, pokud zaměstnanec bude mít zajištěno náhradní stravování nebo jiné služby.</span><span class="sxs-lookup"><span data-stu-id="3f7c9-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="3f7c9-121">Můžete také definovat úrovně sazeb denní diety a nastavit minimální a maximální počet hodin, pro které lze sazby denních diet použít na cestu pracovníka.</span><span class="sxs-lookup"><span data-stu-id="3f7c9-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span>

<span data-ttu-id="3f7c9-122">**Rozhodnutí:**</span><span class="sxs-lookup"><span data-stu-id="3f7c9-122">**Decisions:**</span></span>

- <span data-ttu-id="3f7c9-123">Výchozí pravidla denních diet pro první a poslední den:</span><span class="sxs-lookup"><span data-stu-id="3f7c9-123">Default per diem rules for the first and last days:</span></span>

    - <span data-ttu-id="3f7c9-124">Jaký je minimální počet hodin, které zaměstnanec může za den nárokovat a stále obdržet diety?</span><span class="sxs-lookup"><span data-stu-id="3f7c9-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    - <span data-ttu-id="3f7c9-125">Je částka, která je k dispozici na stravování pro první a poslední den, snížena?</span><span class="sxs-lookup"><span data-stu-id="3f7c9-125">Is there a reduction in the amount that is offered for meals for the first day and last day?</span></span> <span data-ttu-id="3f7c9-126">Pokud dojde ke snížení, jaké je procento snížení?</span><span class="sxs-lookup"><span data-stu-id="3f7c9-126">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="3f7c9-127">Je částka, která je k dispozici na hotel pro první a poslední den, snížena?</span><span class="sxs-lookup"><span data-stu-id="3f7c9-127">Is there a reduction in the amount that is offered for a hotel for the first day and last day?</span></span> <span data-ttu-id="3f7c9-128">Pokud dojde ke snížení, jaké je procento snížení?</span><span class="sxs-lookup"><span data-stu-id="3f7c9-128">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="3f7c9-129">Je částka, která je k dispozici na další výdaje pro první a poslední den, snížena?</span><span class="sxs-lookup"><span data-stu-id="3f7c9-129">Is there a reduction in the amount that is offered for other expenses that are incurred on the first day and last day?</span></span> <span data-ttu-id="3f7c9-130">Pokud dojde ke snížení, jaké je procento snížení?</span><span class="sxs-lookup"><span data-stu-id="3f7c9-130">If there is a reduction, what is the percentage of the reduction?</span></span>

- <span data-ttu-id="3f7c9-131">Výchozí pravidla pro diety:</span><span class="sxs-lookup"><span data-stu-id="3f7c9-131">Default per diem rules:</span></span>

    - <span data-ttu-id="3f7c9-132">Uplatňuje se procento snížení denní diety pro každé jídlo, například pokud je zajištěno jiné jídlo?</span><span class="sxs-lookup"><span data-stu-id="3f7c9-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="3f7c9-133">Pokud dojde ke snížení, jaké je procento snížení pro každé jídlo?</span><span class="sxs-lookup"><span data-stu-id="3f7c9-133">If there is a reduction, what is the reduction percentage for each meal?</span></span>
    - <span data-ttu-id="3f7c9-134">Je srážka za jídlo vypočítána za den, cestu nebo počet jídel za den?</span><span class="sxs-lookup"><span data-stu-id="3f7c9-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    - <span data-ttu-id="3f7c9-135">Mají být částky denních diet zaokrouhleny obvyklým způsobem nebo zaokrouhleny nahoru?</span><span class="sxs-lookup"><span data-stu-id="3f7c9-135">Should per diem amounts be rounded in the regular manner or rounded up?</span></span>
    - <span data-ttu-id="3f7c9-136">Jsou diety vypočítány za období 24 hodin nebo za kalendářní den?</span><span class="sxs-lookup"><span data-stu-id="3f7c9-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>

- <span data-ttu-id="3f7c9-137">Pravidla denních diet založená na místě:</span><span class="sxs-lookup"><span data-stu-id="3f7c9-137">Per diem rules that are based on location:</span></span>

    - <span data-ttu-id="3f7c9-138">Liší se sazby denních diet podle místa?</span><span class="sxs-lookup"><span data-stu-id="3f7c9-138">Do per diem rates vary according to location?</span></span> <span data-ttu-id="3f7c9-139">Jaká místa jsou zahrnuta?</span><span class="sxs-lookup"><span data-stu-id="3f7c9-139">What locations are included?</span></span>
    - <span data-ttu-id="3f7c9-140">Pokud se sazby denních diet liší podle místa, pro každé místo, jaká procentuální částka je k dispozici pro následující typy nákladů:</span><span class="sxs-lookup"><span data-stu-id="3f7c9-140">If per diem rates vary according to location, for each location, what percentage amount is provided for the following types of expenses:</span></span>

        - <span data-ttu-id="3f7c9-141">Jídla</span><span class="sxs-lookup"><span data-stu-id="3f7c9-141">Meals</span></span>
        - <span data-ttu-id="3f7c9-142">Hotel</span><span class="sxs-lookup"><span data-stu-id="3f7c9-142">Hotel</span></span>
        - <span data-ttu-id="3f7c9-143">Jiné výdaje</span><span class="sxs-lookup"><span data-stu-id="3f7c9-143">Other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="3f7c9-144">Deníky a účty správy výdajů</span><span class="sxs-lookup"><span data-stu-id="3f7c9-144">Expense management journals and accounts</span></span>

<span data-ttu-id="3f7c9-145">Správa výdajů vyžaduje použití několika deníků a účtů.</span><span class="sxs-lookup"><span data-stu-id="3f7c9-145">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="3f7c9-146">Je nutné se rozhodnout, například zda se používá stejný účet pro hotovostní zálohy a spory platební karty.</span><span class="sxs-lookup"><span data-stu-id="3f7c9-146">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span>

<span data-ttu-id="3f7c9-147">**Rozhodnutí:**</span><span class="sxs-lookup"><span data-stu-id="3f7c9-147">**Decisions:**</span></span>

- <span data-ttu-id="3f7c9-148">Do kterého deníku hlavní knihy mají být zaúčtována schválená vyúčtování výdajů.</span><span class="sxs-lookup"><span data-stu-id="3f7c9-148">Which ledger journal are approved expense reports posted to?</span></span>
- <span data-ttu-id="3f7c9-149">Jaký účet se používá pro hotovostní zálohy?</span><span class="sxs-lookup"><span data-stu-id="3f7c9-149">Which account is used for cash advances?</span></span>
- <span data-ttu-id="3f7c9-150">Mají být hotovostní zálohy zaúčtovány okamžitě?</span><span class="sxs-lookup"><span data-stu-id="3f7c9-150">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="3f7c9-151">Způsoby platby</span><span class="sxs-lookup"><span data-stu-id="3f7c9-151">Payment methods</span></span>

<span data-ttu-id="3f7c9-152">Pokud povolíte zaměstnancům vydávat výdaje jménem vaší společnosti, je nutné definovat metody platby, které mohou zaměstnanci používat.</span><span class="sxs-lookup"><span data-stu-id="3f7c9-152">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="3f7c9-153">Může například zaměstnancům dovolit používat hotovost nebo firemní platební kartu.</span><span class="sxs-lookup"><span data-stu-id="3f7c9-153">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="3f7c9-154">Můžete také zaměstnancům umožnit používat osobní kreditní karty a potom provést refundaci pro zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="3f7c9-154">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="3f7c9-155">Je třeba provést následující rozhodnutí pro každý způsob platby, který povolíte.</span><span class="sxs-lookup"><span data-stu-id="3f7c9-155">You must make the following decisions for each payment method that you allow.</span></span>

<span data-ttu-id="3f7c9-156">**Rozhodnutí:**</span><span class="sxs-lookup"><span data-stu-id="3f7c9-156">**Decisions:**</span></span>

- <span data-ttu-id="3f7c9-157">Jaké metody platby jsou povoleny?</span><span class="sxs-lookup"><span data-stu-id="3f7c9-157">What payment methods are allowed?</span></span>
- <span data-ttu-id="3f7c9-158">Kdo vlastní výdaje metody platby?</span><span class="sxs-lookup"><span data-stu-id="3f7c9-158">Who owns the payment method expenses?</span></span>
- <span data-ttu-id="3f7c9-159">Existuje typ protiúčtu?</span><span class="sxs-lookup"><span data-stu-id="3f7c9-159">Is there an offset account type?</span></span> <span data-ttu-id="3f7c9-160">Pokud existuje typ protiúčtu, jaký je to účet?</span><span class="sxs-lookup"><span data-stu-id="3f7c9-160">If there is an offset account type, what is it?</span></span>
- <span data-ttu-id="3f7c9-161">Pokud existuje protiúčet, jaký je účet?</span><span class="sxs-lookup"><span data-stu-id="3f7c9-161">If there is an offset account, what is the account?</span></span>
- <span data-ttu-id="3f7c9-162">Pokud je jako způsob platby zvolena kreditní karta, má být způsob platby použit pouze s importovanými transakcemi?</span><span class="sxs-lookup"><span data-stu-id="3f7c9-162">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="3f7c9-163">Kategorie výdajů a sdílené kategorie</span><span class="sxs-lookup"><span data-stu-id="3f7c9-163">Expense categories and shared categories</span></span>

<span data-ttu-id="3f7c9-164">Když zaměstnanci vytvoří sestavu výdajů, musí být každý výdaj, který zaznamenají, přidružen ke kategorii výdajů.</span><span class="sxs-lookup"><span data-stu-id="3f7c9-164">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="3f7c9-165">Kategorie výdajů jsou odvozeny ze sdílených kategorií, které mohou být sdíleny právnickými osobami v rámci dané organizace.</span><span class="sxs-lookup"><span data-stu-id="3f7c9-165">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="3f7c9-166">Tyto kategorie lze také sdílet v modulu Řízení a účetnictví projektů, v závislosti na tom, jak je definována vaše organizace.</span><span class="sxs-lookup"><span data-stu-id="3f7c9-166">These categories can also be shared in Project management and accounting, depending on the way that your organization is defined.</span></span> <span data-ttu-id="3f7c9-167">Na základě definice organizace a pokynů od implementačního týmu určete, zda mají být kategorie použité ve správě výdajů použity pouze ve správě výdajů nebo zda mají být sdíleny mezi správou projektu a účetnictvím a správou výdajů.</span><span class="sxs-lookup"><span data-stu-id="3f7c9-167">Based on the definition of your organization and guidance from the implementation team, determine whether the categories that are used in Expense management will be used only in Expense management, or whether they should be shared between Project management and accounting and Expense management.</span></span> <span data-ttu-id="3f7c9-168">Všimněte si, že tyto kategorie lze sdílet mezi projektem a výdaji nebo projektem a výrobou, ale nikoli mezi výdaji a výrobou.</span><span class="sxs-lookup"><span data-stu-id="3f7c9-168">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="3f7c9-169">Je třeba provést následující rozhodnutí pro každou kategorii výdajů.</span><span class="sxs-lookup"><span data-stu-id="3f7c9-169">You must make the following decisions for each expense category.</span></span>

<span data-ttu-id="3f7c9-170">**Rozhodnutí:**</span><span class="sxs-lookup"><span data-stu-id="3f7c9-170">**Decisions:**</span></span>

- <span data-ttu-id="3f7c9-171">Co je kategorie výdajů?</span><span class="sxs-lookup"><span data-stu-id="3f7c9-171">What is the expense category?</span></span> <span data-ttu-id="3f7c9-172">Příklady obsahují kategorie pro lety, hotel a ujeté kilometry.</span><span class="sxs-lookup"><span data-stu-id="3f7c9-172">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="3f7c9-173">Lze kategorii výdajů použít také v modulu Řízení a účetnictví projektů.</span><span class="sxs-lookup"><span data-stu-id="3f7c9-173">Can the expense category also be used in Project management and accounting?</span></span>
- <span data-ttu-id="3f7c9-174">Co je typ výdajů?</span><span class="sxs-lookup"><span data-stu-id="3f7c9-174">What is the expense type?</span></span>
- <span data-ttu-id="3f7c9-175">Jaká je výchozí metoda platby pro kategorii výdajů?</span><span class="sxs-lookup"><span data-stu-id="3f7c9-175">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="3f7c9-176">Musí být výdaje v kategorii výdajů rozepsány?</span><span class="sxs-lookup"><span data-stu-id="3f7c9-176">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="3f7c9-177">Jaký je hlavní výchozí účet pro kategorii výdajů?</span><span class="sxs-lookup"><span data-stu-id="3f7c9-177">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="3f7c9-178">Jaká je výchozí skupina DPH zboží pro kategorii výdajů?</span><span class="sxs-lookup"><span data-stu-id="3f7c9-178">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="3f7c9-179">Jsou pro tuto kategorii výdajů povolený další způsoby platby?</span><span class="sxs-lookup"><span data-stu-id="3f7c9-179">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="3f7c9-180">Pokud jsou povoleny další platební metody, jaké to jsou metody?</span><span class="sxs-lookup"><span data-stu-id="3f7c9-180">If additional payment methods are allowed, what are they?</span></span>
- <span data-ttu-id="3f7c9-181">Existují dílčí kategorie v této kategorii výdajů?</span><span class="sxs-lookup"><span data-stu-id="3f7c9-181">Are there subcategories in this expense category?</span></span> <span data-ttu-id="3f7c9-182">Pokud existují dílčí kategorie, je nutné provést následující rozhodnutí:</span><span class="sxs-lookup"><span data-stu-id="3f7c9-182">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="3f7c9-183">Jsou některé dílčí kategorie vyloučeny z vratky daně?</span><span class="sxs-lookup"><span data-stu-id="3f7c9-183">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="3f7c9-184">Co je skupina DPH zboží dílčích kategorií?</span><span class="sxs-lookup"><span data-stu-id="3f7c9-184">What is the item sales tax group of the subcategories?</span></span>

<span data-ttu-id="3f7c9-185">Pokud je kategorie výdajů použita také v modulu Řízení a účetnictví projektů, odpovězte na zbývající otázky.</span><span class="sxs-lookup"><span data-stu-id="3f7c9-185">If the expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="3f7c9-186">V opačném případě se přesuňte na následující část.</span><span class="sxs-lookup"><span data-stu-id="3f7c9-186">Otherwise, move on to the next section.</span></span>

- <span data-ttu-id="3f7c9-187">Jaké nákladové účty budou použity pro následující výdaje?</span><span class="sxs-lookup"><span data-stu-id="3f7c9-187">Which cost accounts will be used for the following expenses?</span></span>

    - <span data-ttu-id="3f7c9-188">Náklady</span><span class="sxs-lookup"><span data-stu-id="3f7c9-188">Cost</span></span>
    - <span data-ttu-id="3f7c9-189">Přiřazení mezd</span><span class="sxs-lookup"><span data-stu-id="3f7c9-189">Payroll allocation</span></span>
    - <span data-ttu-id="3f7c9-190">NV – náklady</span><span class="sxs-lookup"><span data-stu-id="3f7c9-190">WIP-cost value</span></span>
    - <span data-ttu-id="3f7c9-191">Náklady – zboží</span><span class="sxs-lookup"><span data-stu-id="3f7c9-191">Cost-item</span></span>
    - <span data-ttu-id="3f7c9-192">Nedokončená výroba – hodnota nákladů – položka</span><span class="sxs-lookup"><span data-stu-id="3f7c9-192">WIP-cost value-item</span></span>
    - <span data-ttu-id="3f7c9-193">Časově rozlišená ztráta</span><span class="sxs-lookup"><span data-stu-id="3f7c9-193">Accrued loss</span></span>
    - <span data-ttu-id="3f7c9-194">NV – časově rozlišená ztráta</span><span class="sxs-lookup"><span data-stu-id="3f7c9-194">WIP-accrued loss</span></span>

- <span data-ttu-id="3f7c9-195">Jaké účty výnosů budou použity pro následující?</span><span class="sxs-lookup"><span data-stu-id="3f7c9-195">Which revenue accounts will be used for the following?</span></span>

    - <span data-ttu-id="3f7c9-196">Fakturované výnosy</span><span class="sxs-lookup"><span data-stu-id="3f7c9-196">Invoiced revenue</span></span>
    - <span data-ttu-id="3f7c9-197">Časově rozlišené výnosy – hodnota prodeje</span><span class="sxs-lookup"><span data-stu-id="3f7c9-197">Accrued revenue-sales value</span></span>
    - <span data-ttu-id="3f7c9-198">NV – hodnota prodeje</span><span class="sxs-lookup"><span data-stu-id="3f7c9-198">WIP-sales value</span></span>
    - <span data-ttu-id="3f7c9-199">Časově rozlišené výnosy – výroba</span><span class="sxs-lookup"><span data-stu-id="3f7c9-199">Accrued revenue-production</span></span>
    - <span data-ttu-id="3f7c9-200">NV – výroba</span><span class="sxs-lookup"><span data-stu-id="3f7c9-200">WIP-production</span></span>
    - <span data-ttu-id="3f7c9-201">Časově rozlišené výnosy – zisk</span><span class="sxs-lookup"><span data-stu-id="3f7c9-201">Accrued revenue-profit</span></span>
    - <span data-ttu-id="3f7c9-202">NV – zisk</span><span class="sxs-lookup"><span data-stu-id="3f7c9-202">WIP-profit</span></span>
    - <span data-ttu-id="3f7c9-203">Časově rozlišené výnosy – předplatné</span><span class="sxs-lookup"><span data-stu-id="3f7c9-203">Accrued revenue-subscription</span></span>
    - <span data-ttu-id="3f7c9-204">NV – předplatné</span><span class="sxs-lookup"><span data-stu-id="3f7c9-204">WIP-subscription</span></span>

### <a name="taxes"></a><span data-ttu-id="3f7c9-205">Daně</span><span class="sxs-lookup"><span data-stu-id="3f7c9-205">Taxes</span></span>

<span data-ttu-id="3f7c9-206">U daní souvisejících s výdaji je třeba určit, co je zahrnuto nebo povoleno v sestavách výdajů.</span><span class="sxs-lookup"><span data-stu-id="3f7c9-206">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span>

<span data-ttu-id="3f7c9-207">**Rozhodnutí:**</span><span class="sxs-lookup"><span data-stu-id="3f7c9-207">**Decisions:**</span></span>

- <span data-ttu-id="3f7c9-208">Je daň z přidané hodnoty zahrnuta v částkách výdajů.</span><span class="sxs-lookup"><span data-stu-id="3f7c9-208">Is sales tax included in the expense amounts?</span></span>
- <span data-ttu-id="3f7c9-209">Má být povolena vratka daně výdajů?</span><span class="sxs-lookup"><span data-stu-id="3f7c9-209">Should tax recovery be enabled on expenses?</span></span>

    > [!NOTE]
    > <span data-ttu-id="3f7c9-210">Pokud jste plánovali hlavní knihu a rozhodli jste použít daň z přidané hodnoty pro USA a daňová pravidla, nemůžete povolit vratku daně výdajů.</span><span class="sxs-lookup"><span data-stu-id="3f7c9-210">When you were planning the general ledger, if you decided to apply U.S. sales tax and use tax rules, you can’t enable tax recovery on expenses.</span></span> <span data-ttu-id="3f7c9-211">(Chcete-li použít daň z přidané hodnoty pro USA a daňová pravidla, nastavte možnost **Použít daňové předpisy pro DPH** na **Ano**.)</span><span class="sxs-lookup"><span data-stu-id="3f7c9-211">(To apply U.S. sales tax and use tax rules, set the **Apply sales tax taxations rules** option to **Yes**.)</span></span>

## <a name="policies"></a><span data-ttu-id="3f7c9-212">Zásady</span><span class="sxs-lookup"><span data-stu-id="3f7c9-212">Policies</span></span>

<span data-ttu-id="3f7c9-213">Vytvořením sestavy výdajů pomůžete své organizaci ušetřit čas a peníze, když zaměstnanci generují výdaje jejím jménem.</span><span class="sxs-lookup"><span data-stu-id="3f7c9-213">By creating expense report policies, you can help your organization save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="3f7c9-214">Zásady zajišťují, že zaměstnanci nepřekročí rozpočet, poskytnou všechny požadované informace a utratí peníze pouze v případě potřeby.</span><span class="sxs-lookup"><span data-stu-id="3f7c9-214">Policies help guarantee that employees stay in budget, provide all required information, and spend money only as they require it.</span></span> <span data-ttu-id="3f7c9-215">Je třeba provést následující rozhodnutí pro každou zásadu sestavy výdajů a každou zásadu schválení sestavy výdajů, kterou vytvoříte.</span><span class="sxs-lookup"><span data-stu-id="3f7c9-215">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span>

<span data-ttu-id="3f7c9-216">**Rozhodnutí:**</span><span class="sxs-lookup"><span data-stu-id="3f7c9-216">**Decisions:**</span></span>

- <span data-ttu-id="3f7c9-217">Jaký je název zásad?</span><span class="sxs-lookup"><span data-stu-id="3f7c9-217">What is the name of the policy?</span></span>
- <span data-ttu-id="3f7c9-218">K čemu slouží zásady výdajů?</span><span class="sxs-lookup"><span data-stu-id="3f7c9-218">What is the expense policy for?</span></span>
- <span data-ttu-id="3f7c9-219">Pokud jste se dříve rozhodli povolit mezipodnikové výdaje, kterých společností ve vaší organizaci se tyto zásady týkají?</span><span class="sxs-lookup"><span data-stu-id="3f7c9-219">If you previously decided to enable intercompany expenses, which companies in your organization will this policy apply to?</span></span>
- <span data-ttu-id="3f7c9-220">Kdy zásady začínají platit?</span><span class="sxs-lookup"><span data-stu-id="3f7c9-220">When does the policy become effective?</span></span>
- <span data-ttu-id="3f7c9-221">Kdy platnost zásad vyprší?</span><span class="sxs-lookup"><span data-stu-id="3f7c9-221">When does the policy expire?</span></span>
- <span data-ttu-id="3f7c9-222">Co je pravidlo zásad?</span><span class="sxs-lookup"><span data-stu-id="3f7c9-222">What is the policy rule?</span></span>
- <span data-ttu-id="3f7c9-223">Jaký je výstup pravidla zásad?</span><span class="sxs-lookup"><span data-stu-id="3f7c9-223">What is the outcome of the policy rule?</span></span>

