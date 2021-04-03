---
title: Vytvářejte ve správě zaměstnaneckých výhod sestavy v rámci zákona Affordable Care Act
description: Toto téma popisuje, jak vám správa zaměstnaneckých výhod pomáhá sledovat informace, které jsou hlášeny formuláři 1095-B a formuláři 1095-C pro mandát zaměstnavatele podle zákona Affordable Care Act (ACA).
author: andreabichsel
manager: tfehr
ms.date: 12/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 24df18f428e4ca14859bc34048a6bda5e03d1b2f
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464367"
---
# <a name="generate-aca-reports-in-benefits-management"></a><span data-ttu-id="68151-103">Generujte zprávy ACA ve Správě zaměstnaneckých výhod</span><span class="sxs-lookup"><span data-stu-id="68151-103">Generate ACA reports in Benefits management</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="68151-104">Správa zaměstnaneckých výhod pomáhá sledovat informace, které jsou hlášeny formuláři 1095-B a formuláři 1095-C pro mandát zaměstnavatele podle zákona Affordable Care Act (ACA).</span><span class="sxs-lookup"><span data-stu-id="68151-104">Benefits management helps you track information that is reported on Form 1095-B and Form 1095-C for the Affordable Care Act (ACA) employer mandate.</span></span> <span data-ttu-id="68151-105">Stejně jako možnost ACA hlášení v minulosti v pracovním prostoru **zaměstnanecké výhody**, tato funkce se vztahuje pouze na právnické osoby ve Spojených státech.</span><span class="sxs-lookup"><span data-stu-id="68151-105">Like the ACA reporting capability in the old **Benefits** workspace, this functionality applies only to legal entities in the United States.</span></span>

<span data-ttu-id="68151-106">Abyste mohli tuto funkci používat, musíte nejprve zapnout **Pokročilou správu zaměstnaneckých výhod**.</span><span class="sxs-lookup"><span data-stu-id="68151-106">To use this functionality, you must first turn on **Advanced Benefits Management**.</span></span> <span data-ttu-id="68151-107">Další informace, včetně důležitých upozornění na správu zaměstnaneckých výhod, viz [Povolení nebo zákaz správy zaměstnaneckých výhod](hr-admin-manage-features.md#enable-or-disable-benefits-management).</span><span class="sxs-lookup"><span data-stu-id="68151-107">For more information, including important caveats about Benefits management, see [Enable or disable Benefits management](hr-admin-manage-features.md#enable-or-disable-benefits-management).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="68151-108">Sestavení ACA můžete použít pouze buď z pracovního prostoru **správa zaměstnaneckých výhod**, nebo staršího prostoru **zaměstnanecké výhody**, ne z obou.</span><span class="sxs-lookup"><span data-stu-id="68151-108">You can use ACA reporting only from either the **Benefits management** workspace or the old **Benefits** workspace, not from both.</span></span> <span data-ttu-id="68151-109">Například pokud jste přešli na správu zaměstnaneckých výhod, hlášení ACA je k dispozici pouze z prostoru **správa zaměstnaneckých výhod**, ne ze starého pracovního prostoru **zaměstnanecké výhody**.</span><span class="sxs-lookup"><span data-stu-id="68151-109">For example, if you switched to Benefits management, ACA reporting is available only from the **Benefits management** workspace, not from the old **Benefits** workspace.</span></span>
>
> <span data-ttu-id="68151-110">Pokud přepnete na správu zaměstnaneckých výhod uprostřed roku registrace, musíte správně nakonfigurovat data zaměstnanců pro celý rok ve správě výhod.</span><span class="sxs-lookup"><span data-stu-id="68151-110">If you switch to Benefits management in the middle of an enrollment year, you must correctly configure employee data for the whole year in Benefits management.</span></span> <span data-ttu-id="68151-111">Tímto způsobem zajistíte, že budete dostávat přesné informace o sestavách za celý rok.</span><span class="sxs-lookup"><span data-stu-id="68151-111">In this way, you ensure that you will receive accurate reporting information for the whole year.</span></span>

## <a name="getting-started"></a><span data-ttu-id="68151-112">Začínáme</span><span class="sxs-lookup"><span data-stu-id="68151-112">Getting started</span></span>

<span data-ttu-id="68151-113">Chcete-li sledovat informace proformuláře 1095, nejprve vytvořte jednu nebo více skupin Affordable Care.</span><span class="sxs-lookup"><span data-stu-id="68151-113">To track information for 1095 forms, first create one or more Affordable Care coverage groups.</span></span> <span data-ttu-id="68151-114">Tyto skupiny označují následující informace:</span><span class="sxs-lookup"><span data-stu-id="68151-114">These groups indicate the following information:</span></span>

- <span data-ttu-id="68151-115">Nabídka krytí, která byla poskytnuta zaměstnanci</span><span class="sxs-lookup"><span data-stu-id="68151-115">The offer of coverage that was provided to an employee</span></span>
- <span data-ttu-id="68151-116">Podíl zaměstnance na nejnižší měsíční prémii, pokud je cena nad federální hranicí chudoby</span><span class="sxs-lookup"><span data-stu-id="68151-116">The employee's share of the lowest-cost monthly premium, if the cost is above the federal poverty line</span></span>
- <span data-ttu-id="68151-117">Případně program Safe Harbor, který využívá zaměstnavatel</span><span class="sxs-lookup"><span data-stu-id="68151-117">The safe harbor that is used by the employer, if applicable</span></span>

<span data-ttu-id="68151-118">Skupiny pokrytí Affordable Care vám pomohou spravovat tyto informace pro více záznamů zaměstnanců, které mají stejné podmínky.</span><span class="sxs-lookup"><span data-stu-id="68151-118">Affordable Care coverage groups help you manage this information for multiple employee records that have the same conditions.</span></span> <span data-ttu-id="68151-119">Skupiny můžete snadno přiřadit jednomu nebo více zaměstnancům.</span><span class="sxs-lookup"><span data-stu-id="68151-119">You can easily assign groups to one or more employees.</span></span>

### <a name="create-or-edit-an-affordable-care-coverage-group"></a><span data-ttu-id="68151-120">Vytvořte nebo upravte skupinu pokrytí Affordable Care</span><span class="sxs-lookup"><span data-stu-id="68151-120">Create or edit an Affordable Care coverage group</span></span>

1. <span data-ttu-id="68151-121">V pracovním prostoru **správa zaměstnaneckých výhod** vyberte **Skupina pokrytí Affordable Care**.</span><span class="sxs-lookup"><span data-stu-id="68151-121">In the **Benefits management** workspace, select **Affordable Care coverage group**.</span></span>

    ![Výběr skupiny pokrytí Affordable Care](./media/hr-benefits-management-aca-coverage-group.png)

2. <span data-ttu-id="68151-123">Vyberte **Nová** k vytvoření nové skupiny pokrytí Affordable Care nebo **Upravit** ke změně existující skupiny.</span><span class="sxs-lookup"><span data-stu-id="68151-123">Select **New** to create a new Affordable Care coverage group or **Edit** to change an existing group.</span></span>

    ![Vyberte Nová nebo Upravit](./media/hr-benefits-management-aca-new.png)

3. <span data-ttu-id="68151-125">Nastavte následující pole.</span><span class="sxs-lookup"><span data-stu-id="68151-125">Set the following fields.</span></span>

    | <span data-ttu-id="68151-126">Pole</span><span class="sxs-lookup"><span data-stu-id="68151-126">Field</span></span> | <span data-ttu-id="68151-127">popis</span><span class="sxs-lookup"><span data-stu-id="68151-127">Description</span></span> |
    |---|---|
    | <span data-ttu-id="68151-128">Jméno</span><span class="sxs-lookup"><span data-stu-id="68151-128">Name</span></span> | <span data-ttu-id="68151-129">Zadejte název skupiny.</span><span class="sxs-lookup"><span data-stu-id="68151-129">Enter a name for the group.</span></span> |
    | <span data-ttu-id="68151-130">popis</span><span class="sxs-lookup"><span data-stu-id="68151-130">Description</span></span> | <span data-ttu-id="68151-131">Zadejte popis skupiny.</span><span class="sxs-lookup"><span data-stu-id="68151-131">Enter a description of the group.</span></span> |
    | <span data-ttu-id="68151-132">Nabídka pokrytí</span><span class="sxs-lookup"><span data-stu-id="68151-132">Offer of coverage</span></span> | <span data-ttu-id="68151-133">Krytí, které je nabízeno zaměstnancům, jejich manželům nebo partnerům a jejich závislým osobám.</span><span class="sxs-lookup"><span data-stu-id="68151-133">The coverage that is offered to employees, their spouse or partner, and their dependents.</span></span> |
    | <span data-ttu-id="68151-134">Podíl zaměstnance na nákladech</span><span class="sxs-lookup"><span data-stu-id="68151-134">Employee share of cost</span></span> | <span data-ttu-id="68151-135">Množství, za které je zaměstnanec zodpovědný.</span><span class="sxs-lookup"><span data-stu-id="68151-135">The amount that the employee is responsible for.</span></span> |
    | <span data-ttu-id="68151-136">Použitelná sekce 4980H Safe Harbor</span><span class="sxs-lookup"><span data-stu-id="68151-136">Applicable section 4980H safe harbor</span></span> | <span data-ttu-id="68151-137">Kód Safe Harbor 4980H nebo kód transition relief.</span><span class="sxs-lookup"><span data-stu-id="68151-137">The 4980H safe harbor or transition relief code.</span></span> |
    | <span data-ttu-id="68151-138">Měsíc začátku plánu</span><span class="sxs-lookup"><span data-stu-id="68151-138">Plan start month</span></span> | <span data-ttu-id="68151-139">Vyberte kalendářní měsíc, kdy začíná rok vašeho plánu dávek.</span><span class="sxs-lookup"><span data-stu-id="68151-139">Select the calendar month when your benefit plan year begins.</span></span> |
    | <span data-ttu-id="68151-140">Skupina platná od</span><span class="sxs-lookup"><span data-stu-id="68151-140">Group valid from</span></span> | <span data-ttu-id="68151-141">První datum, kdy je tento záznam platný.</span><span class="sxs-lookup"><span data-stu-id="68151-141">The first date when this record is valid.</span></span> |
    | <span data-ttu-id="68151-142">Skupina platná do</span><span class="sxs-lookup"><span data-stu-id="68151-142">Group valid through</span></span> | <span data-ttu-id="68151-143">Poslední datum, kdy je tento záznam platný.</span><span class="sxs-lookup"><span data-stu-id="68151-143">The last date when this record is valid.</span></span> <span data-ttu-id="68151-144">Pokud není datum vypršení platnosti, zadejte **Nikdy**.</span><span class="sxs-lookup"><span data-stu-id="68151-144">If there is no expiration date, enter **Never**.</span></span> |

    ![Vytvoření skupiny disponibility](./media/hr-benefits-management-aca-new-group.png)

4. <span data-ttu-id="68151-146">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="68151-146">Select **Save**.</span></span>

### <a name="assign-multiple-employees-to-an-affordable-care-coverage-group"></a><span data-ttu-id="68151-147">Přiřaďte více zaměstnanců do skupiny pokrytí Affordable Care</span><span class="sxs-lookup"><span data-stu-id="68151-147">Assign multiple employees to an Affordable Care coverage group</span></span>

1. <span data-ttu-id="68151-148">V pracovním prostoru **správa zaměstnaneckých výhod** vyberte **Skupina pokrytí Affordable Care**.</span><span class="sxs-lookup"><span data-stu-id="68151-148">In the **Benefits management** workspace, select **Affordable Care coverage group**.</span></span>
2. <span data-ttu-id="68151-149">Vyberte skupinu, ke které chcete přiřadit zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="68151-149">Select the group to assign employees to.</span></span>
3. <span data-ttu-id="68151-150">Vyberte **Hromadné přiřazení**.</span><span class="sxs-lookup"><span data-stu-id="68151-150">Select **Mass assignment**.</span></span>

    ![Vyberte Hromadné přiřazení.](./media/hr-benefits-management-aca-mass-assignment.png)

4. <span data-ttu-id="68151-152">Vyberte zaměstnance v seznamu a poté vyberte **Přiřadit**.</span><span class="sxs-lookup"><span data-stu-id="68151-152">Select employees in the list, and then select **Assign**.</span></span>

    ![Přiřaďte vybrané zaměstnance ke skupině](./media/hr-benefits-management-aca-assign-coverage-group.png)

## <a name="maintain-multiple-versions-of-coverage-options"></a><span data-ttu-id="68151-154">Správa několika verzí možností pokrytí</span><span class="sxs-lookup"><span data-stu-id="68151-154">Maintain multiple versions of coverage options</span></span>

<span data-ttu-id="68151-155">Můžete spravovat několik verzí skupin pokrytí.</span><span class="sxs-lookup"><span data-stu-id="68151-155">You can maintain multiple versions of any coverage group.</span></span> <span data-ttu-id="68151-156">Když se ve vaší organizaci nebo ve výhodách, které nabízí, něco změní, můžete udržovat aktuální informace o skupině, aniž byste museli vytvářet novou skupinu a přiřazovat k ní zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="68151-156">When something changes in your organization or the benefits that are offered, you can keep the group's information up to date without having to create a new group and reassign employees to it.</span></span>

<span data-ttu-id="68151-157">Poté, co jste vytvořili skupiny pokrytí Affordable Care, můžete jim hromadně přiřadit zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="68151-157">After you've created Affordable Care coverage groups, you can mass-assign employees to them.</span></span> <span data-ttu-id="68151-158">Můžete také jednotlivě přiřadit zaměstnance ke skupinám a určit, zda jsou sledovány a hlášeny informace ACA.</span><span class="sxs-lookup"><span data-stu-id="68151-158">You can also individually assign employees to groups, and indicate whether ACA information is tracked and reported.</span></span>

<span data-ttu-id="68151-159">Pokud pro zaměstnance nemusíte sledovat a hlásit informace ACA, můžete nastavit **Zpráva o pokrytí** možnost **Ne**.</span><span class="sxs-lookup"><span data-stu-id="68151-159">If you don't have to track and report ACA information for an employee, you can set the **Report coverage** option to **No**.</span></span> <span data-ttu-id="68151-160">Můžete mít například zaměstnance na částečný úvazek, kteří nevyžadují hlášení ACA.</span><span class="sxs-lookup"><span data-stu-id="68151-160">For example, you might have part-time employees who don't require ACA reporting.</span></span>

### <a name="override-default-values-for-an-employee"></a><span data-ttu-id="68151-161">Přepsat výchozí hodnoty pro zaměstnance</span><span class="sxs-lookup"><span data-stu-id="68151-161">Override default values for an employee</span></span>

<span data-ttu-id="68151-162">U zaměstnanců, kteří jsou přiřazeni do skupiny pokrytí Affordable Care, můžete změnit následující možnosti pro měsíce, které vyžadují různé hodnoty:</span><span class="sxs-lookup"><span data-stu-id="68151-162">For employees who are assigned to an Affordable Care coverage group, you can change the following options for any months that require different values:</span></span>

- <span data-ttu-id="68151-163">Nabídka pokrytí</span><span class="sxs-lookup"><span data-stu-id="68151-163">Offer of coverage</span></span>
- <span data-ttu-id="68151-164">Podíl zaměstnance na nákladech</span><span class="sxs-lookup"><span data-stu-id="68151-164">Employee share of cost</span></span>
- <span data-ttu-id="68151-165">Použitelná sekce 4980H Safe Harbor</span><span class="sxs-lookup"><span data-stu-id="68151-165">Applicable section 4980H safe harbor</span></span>

> [!NOTE]
> <span data-ttu-id="68151-166">U zpráv ACA 2020 musíte na formuláři 1095-C hlásit pracovní i domácí PSČ.</span><span class="sxs-lookup"><span data-stu-id="68151-166">For 2020 ACA reports, you must report both work and home ZIP Codes on Form 1095-C.</span></span> <span data-ttu-id="68151-167">Hodnoty se vyplňují automaticky na základě aktuálních aktivních míst.</span><span class="sxs-lookup"><span data-stu-id="68151-167">Values are automatically filled in, based on current active locations.</span></span> <span data-ttu-id="68151-168">Pokud bylo kterékoli místo v kterékoli části roku jiné, musíte přepsat hodnotu.</span><span class="sxs-lookup"><span data-stu-id="68151-168">If either location was different during any part of the year, you must override the value.</span></span> <span data-ttu-id="68151-169">Pole **PSČ** (řádek 17) sestavy 1095-C se vyplní pouze pokud kód **Nabídka krytí** obsahuje od **1L** po **1Q** následovně:</span><span class="sxs-lookup"><span data-stu-id="68151-169">The **ZIP Code** field (line 17) of the 1095-C report is filled in only if the **Offer of coverage** code contains **1L** through **1Q**, as follows:</span></span>
>
> - <span data-ttu-id="68151-170">**1L, 1M nebo 1N:** PSČ primární rezidence</span><span class="sxs-lookup"><span data-stu-id="68151-170">**1L, 1M, or 1N:** The primary residence ZIP Code</span></span>
> - <span data-ttu-id="68151-171">**1O, 1P, 1Q:** Primární PSČ práce</span><span class="sxs-lookup"><span data-stu-id="68151-171">**1O, 1P, 1Q:** The primary work ZIP Code</span></span>

<span data-ttu-id="68151-172">Chcete-li zadat výjimky pro jakékoli hodnoty skupiny pokrytí Affordable Care, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="68151-172">To enter exceptions for any values of an Affordable Care coverage group, follow these steps.</span></span>

1. <span data-ttu-id="68151-173">Ve **Správa zaměstnanců** pracovním prostoru vyberte **Odkazy** a poté vyberte **Pracovníci**.</span><span class="sxs-lookup"><span data-stu-id="68151-173">In the **Personnel management** workspace, select **Links**, and then select **Workers**.</span></span>
2. <span data-ttu-id="68151-174">V seznamu vyberte zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="68151-174">Select the employee in the list.</span></span>
3. <span data-ttu-id="68151-175">Na kartě **Zaměstnání** v sekci **Více informací** vyberte **Pokrytí Affordable Care**.</span><span class="sxs-lookup"><span data-stu-id="68151-175">On the **Employment** tab, in the **More information** section, select **Affordable Care coverage**.</span></span>

    ![Změna možností pro jednoho zaměstnance](./media/hr-benefits-management-aca-change-single-employee.png)

4. <span data-ttu-id="68151-177">Vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="68151-177">Select **Edit**.</span></span>
5. <span data-ttu-id="68151-178">U každého měsíce, který vyžaduje změny, zaškrtněte políčko **Přepsat výchozí** a poté podle potřeby změňte ostatní hodnoty.</span><span class="sxs-lookup"><span data-stu-id="68151-178">For each month that requires changes, select the **Override default** check box, and then change the other values as required.</span></span>

    ![Přepsat výchozí hodnoty](./media/hr-benefits-management-aca-override-default.png)

6. <span data-ttu-id="68151-180">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="68151-180">Select **Save**.</span></span>

## <a name="report-health-care-coverage"></a><span data-ttu-id="68151-181">Vykazování pokrytí zdravotní péče</span><span class="sxs-lookup"><span data-stu-id="68151-181">Report health care coverage</span></span>

<span data-ttu-id="68151-182">Musíte sledovat jakékoli pojištění zdravotní péče sponzorované zaměstnavatelem a pojištěné u zaměstnanců na plný i částečný úvazek.</span><span class="sxs-lookup"><span data-stu-id="68151-182">You must track any employer-sponsored, self-insured health care coverage for full-time and part-time employees.</span></span> <span data-ttu-id="68151-183">Zahrňte každého zaměstnance společně s jeho závislými osobami do zprávy 1095-C za měsíce, kdy byli pojištěni.</span><span class="sxs-lookup"><span data-stu-id="68151-183">Include each employee, together with their dependents, on the 1095-C report for the months when they were covered.</span></span>

<span data-ttu-id="68151-184">Chcete-li určit, zda je třeba nahlásit plán výhod, postupujte podle těchto kroků.</span><span class="sxs-lookup"><span data-stu-id="68151-184">To indicate whether a benefit plan must be reported, follow these steps.</span></span>

1. <span data-ttu-id="68151-185">V pracovním prostoru **Správa zaměstnaneckých** výhod vyberte možnost **plány zaměstnaneckých výhod**.</span><span class="sxs-lookup"><span data-stu-id="68151-185">In the **Benefits management** workspace, select **Benefit plans**.</span></span>
2. <span data-ttu-id="68151-186">Vyberte plán výhod, který chcete nahlásit.</span><span class="sxs-lookup"><span data-stu-id="68151-186">Select the benefit plan to report.</span></span>
3. <span data-ttu-id="68151-187">Vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="68151-187">Select **Edit**.</span></span>
4. <span data-ttu-id="68151-188">Nastavte možnost **Hlášeno podle zákona Affordable Care** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="68151-188">Set the **Reported under the Affordable Care Act** option to **Yes**.</span></span>

    ![Vykazování pokrytí zdravotní péče](./media/hr-benefits-management-aca-report-coverage.png)

5. <span data-ttu-id="68151-190">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="68151-190">Select **Save**.</span></span>

<span data-ttu-id="68151-191">Pokud si zaměstnanec zvolí krytí zdravotní péče pro závislou osobu, doba jejího krytí se určí podle data, kdy byla závislá osoba zapsána nebo odstraněna.</span><span class="sxs-lookup"><span data-stu-id="68151-191">If an employee chooses health care coverage for a dependent, the dependent's coverage period is determined by the date when the dependent was enrolled or removed.</span></span> <span data-ttu-id="68151-192">Data pokrytí závislých osob se automaticky počítají na základě období, kdy závislá osoba byla způsobilá a aktivní v plánu během roku registrace.</span><span class="sxs-lookup"><span data-stu-id="68151-192">Coverage dates for dependents are automatically calculated based on the period when the dependent was eligible and active in a plan during the enrollment year.</span></span>

## <a name="generate-1095-b-and-1095-c-forms"></a><span data-ttu-id="68151-193">Generujte formuláře 1095-B a 1095-C</span><span class="sxs-lookup"><span data-stu-id="68151-193">Generate 1095-B and 1095-C forms</span></span>

<span data-ttu-id="68151-194">ACA formuláře 1095-B and 1095-C můžete vygenerovat a poté rozeslat všem zaměstnancům.</span><span class="sxs-lookup"><span data-stu-id="68151-194">You can generate ACA 1095-B and 1095-C forms, and then distribute them to each of your employees.</span></span> <span data-ttu-id="68151-195">Můžete také elektronicky vygenerovat formulář 1095-C a odpovídající přenosové soubory 1094-C a odeslat je do Internal Revenue Service (IRS).</span><span class="sxs-lookup"><span data-stu-id="68151-195">You can also electronically generate Form 1095-C and the corresponding 1094-C transmittal files to send to the Internal Revenue Service (IRS).</span></span>

1. <span data-ttu-id="68151-196">V pracovním prostoru **správa zaměstnaneckých výhod** vyberte **Formulář ACA 1095-B** nebo **Formulář ACA 1095-C**.</span><span class="sxs-lookup"><span data-stu-id="68151-196">In the **Benefits management** workspace, select **ACA 1095-B form** or **ACA 1095-C form**.</span></span>
2. <span data-ttu-id="68151-197">Podle potřeby změňte parametry a poté vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="68151-197">Change the parameters as required, and then select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="68151-198">Při tisku formulářů 1095-C pro více než 500 zaměstnanců obdržíte více než jeden soubor PDF.</span><span class="sxs-lookup"><span data-stu-id="68151-198">If you're printing 1095-C forms for more than 500 employees, you will receive more than one PDF file.</span></span> <span data-ttu-id="68151-199">Doporučujeme zvýšit hodnotu pole **Maximální velikost souboru v megabajtech** na stránce **Parametry správy dokumentů** na **150**.</span><span class="sxs-lookup"><span data-stu-id="68151-199">We recommend that you increase the value of the **Maximum file size in megabytes** field on the **Document management parameters** page to **150**.</span></span> <span data-ttu-id="68151-200">(Chcete-li tuto stránku rychle otevřít, můžete použít vyhledávací pole na navigační liště.)</span><span class="sxs-lookup"><span data-stu-id="68151-200">(To quickly open that page, you can use the search field on the navigation bar.)</span></span>
    >
    > ![Změna maximální velikosti souboru](./media/hr-benefits-management-aca-maximum-file-size.png)

3. <span data-ttu-id="68151-202">Chcete-li zkontrolovat stav svých přehledů a zobrazit je, otevřete vyhledávací pole na navigačním panelu stránky **Úlohy elektronického hlášení**.</span><span class="sxs-lookup"><span data-stu-id="68151-202">To check the status of your reports and view them, use the search field on the navigation bar to open the **Electronic reporting jobs** page.</span></span>

    ![Hledání stránky úloh elektronického výkaznictví](./media/hr-benefits-management-aca-search-electronic-reporting-jobs.png)

4. <span data-ttu-id="68151-204">Vyberte sestavu, kterou chcete zobrazit, a poté vyberte **Zobrazit soubory**.</span><span class="sxs-lookup"><span data-stu-id="68151-204">Select the report to view, and then select **Show files**.</span></span>

    ![Zobrazují se soubory](./media/hr-benefits-management-aca-show-files.png)

5. <span data-ttu-id="68151-206">Zvolte **Otevřít**.</span><span class="sxs-lookup"><span data-stu-id="68151-206">Select **Open**.</span></span>

    ![Otevření souboru](./media/hr-benefits-management-aca-open-file.png)

6. <span data-ttu-id="68151-208">Na oznamovací liště, která se zobrazí v dolní části okna prohlížeče, otevřete soubor zip a poté vyberte sestavu.</span><span class="sxs-lookup"><span data-stu-id="68151-208">From the Notification bar that appears at the bottom of the browser window, open the zip file, and then select the report.</span></span> <span data-ttu-id="68151-209">Můžete zobrazit nebo vytisknout soubor PDF.</span><span class="sxs-lookup"><span data-stu-id="68151-209">You can view or print the PDF file.</span></span>

    ![Ukázkový formulář 1095-C](./media/hr-benefits-management-aca-1095-c-form.png)

## <a name="view-aca-coverage-information"></a><span data-ttu-id="68151-211">Zobrazit informace o pokrytí ACA</span><span class="sxs-lookup"><span data-stu-id="68151-211">View ACA coverage information</span></span>

<span data-ttu-id="68151-212">Stránka **Pokrytí Worker Affordable Care** zobrazuje následující informace:</span><span class="sxs-lookup"><span data-stu-id="68151-212">The **Worker Affordable Care coverage** page shows the following information:</span></span>

- <span data-ttu-id="68151-213">Zaměstnanci, kteří jsou přiřazeni ke každé skupině pokrytí</span><span class="sxs-lookup"><span data-stu-id="68151-213">Employees who are assigned to each coverage group</span></span>
- <span data-ttu-id="68151-214">Zaměstnanci, kteří nemusí být zahrnuti do zprávy</span><span class="sxs-lookup"><span data-stu-id="68151-214">Employees who don't have to be included on a report</span></span>
- <span data-ttu-id="68151-215">Nepřiřazení zaměstnanci</span><span class="sxs-lookup"><span data-stu-id="68151-215">Unassigned employees</span></span>

<span data-ttu-id="68151-216">Chcete-li tuto informaci zobrazit, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="68151-216">To view this information, follow these steps.</span></span>

1. <span data-ttu-id="68151-217">V pracovním prostoru **správa zaměstnaneckých výhod** vyberte **Skupina pokrytí Worker Affordable Care**.</span><span class="sxs-lookup"><span data-stu-id="68151-217">In the **Benefits management** workspace, select **Worker Affordable Care coverage**.</span></span>
2. <span data-ttu-id="68151-218">V poli **Název skupiny** vyberte skupinu.</span><span class="sxs-lookup"><span data-stu-id="68151-218">In the **Group name** field, select a group.</span></span>

    ![Prohlížení pokrytí ACA](./media/hr-benefits-management-aca-view-coverage.png)

<span data-ttu-id="68151-220">U případných přepsaných výchozích hodnot skupiny pokrytí ACA se vedle změněné hodnoty zobrazí hvězdička.</span><span class="sxs-lookup"><span data-stu-id="68151-220">If any default values from the Affordable Care coverage group have been overridden, an asterisk appears next to the value that was changed.</span></span> <span data-ttu-id="68151-221">Pokud jsou hodnoty u všech 12 měsíců stejné a nebyly přepsány, hodnota bude uvedena ve sloupci **Všech 12 měsíců**.</span><span class="sxs-lookup"><span data-stu-id="68151-221">If the values for all 12 months are the same and haven't been overridden, the value appears in the **All 12 months** column.</span></span>

<span data-ttu-id="68151-222">Můžete si prohlédnout zaměstnance, kteří jsou označeni jako nezodpovědní ACA a kteří nebudou vyžadovat formulář 1095-C.</span><span class="sxs-lookup"><span data-stu-id="68151-222">You can view employees who are marked as not ACA-reportable, and who won't require a Form 1095-C.</span></span> <span data-ttu-id="68151-223">V poli **Filtrovat podle** vyberte **Není třeba hlásit ACA**.</span><span class="sxs-lookup"><span data-stu-id="68151-223">In the **Filter by** field, select **Not ACA reportable**.</span></span>

<span data-ttu-id="68151-224">Můžete zobrazit zaměstnance, kteří nejsou přiřazeni ke skupině nebo kterým je přiřazena skupina, jejíž platnost vypršela.</span><span class="sxs-lookup"><span data-stu-id="68151-224">You can view employees who aren't assigned to a group, or who are assigned to an expired group.</span></span> <span data-ttu-id="68151-225">V poli **Filtrovat podle** vyberte **Nepřiřazená nebo vypršela skupina**.</span><span class="sxs-lookup"><span data-stu-id="68151-225">In the **Filter by** field, select **Unassigned or expired group**.</span></span>

### <a name="export-to-excel"></a><span data-ttu-id="68151-226">Export do aplikace Excel</span><span class="sxs-lookup"><span data-stu-id="68151-226">Export to Excel</span></span>

<span data-ttu-id="68151-227">Chcete-li exportovat některý ze seznamů Microsoft Excel, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="68151-227">To export any of the lists to Microsoft Excel, follow these steps.</span></span>

1. <span data-ttu-id="68151-228">Vyberte tlačítko **Otevřít Microsoft Office**.</span><span class="sxs-lookup"><span data-stu-id="68151-228">Select the **Open in Microsoft Office** button.</span></span>
2. <span data-ttu-id="68151-229">Vyberte **Dočasná tabulka lidských zdrojů HCM pro interní použití**.</span><span class="sxs-lookup"><span data-stu-id="68151-229">Select **HCM Human Resources temporary table for internal use**.</span></span>
3. <span data-ttu-id="68151-230">Vyberte **Stáhnout**.</span><span class="sxs-lookup"><span data-stu-id="68151-230">Select **Download**.</span></span>

### <a name="view-aca-reportable-dependents"></a><span data-ttu-id="68151-231">Zobrazit závislé osoby závislé na ACA</span><span class="sxs-lookup"><span data-stu-id="68151-231">View ACA-reportable dependents</span></span>

<span data-ttu-id="68151-232">Pokud musíte hlásit kryté osoby, protože poskytujete pojištěné osoby, můžete zobrazit závislé osoby, na které se vztahují plány dávek, které jsou označeny jako **hlásitelné ACA**.</span><span class="sxs-lookup"><span data-stu-id="68151-232">If you must report covered individuals because you provide self-insured coverage, you can view dependents who are covered under benefit plans that are marked as **ACA reportable**.</span></span> <span data-ttu-id="68151-233">V podokně akcí vyberte **Zobrazit data pokrytí rodinného příslušníka**.</span><span class="sxs-lookup"><span data-stu-id="68151-233">On the Action Pane, select **View Dependent coverage**.</span></span>

![Zobrazení pokrytí rodinného příslušníka](./media/hr-benefits-management-aca-view-dependent-coverage.png)

<span data-ttu-id="68151-235">Zobrazí se informace o pokrytí závislých osob zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="68151-235">Coverage information for the employee's dependents is shown.</span></span>

![Pokrytí závislých prvků](./media/hr-benefits-management-aca-dependents.png)

> [!NOTE]
> <span data-ttu-id="68151-237">Tato stránka zobrazuje pouze plány výhod, které jsou označeny jako **hlásitelné ACA**.</span><span class="sxs-lookup"><span data-stu-id="68151-237">The page shows only benefits plans that are marked as **ACA reportable**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]