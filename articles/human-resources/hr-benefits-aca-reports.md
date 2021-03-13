---
title: Generování sestav v rámci zákona Affordable Care Act
description: Reporting zákona Affordable Care (ACA) generuje formuláře 1095-B a 1095-C podle části zákona Affordable Care **Mandát zaměstnavatele**.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
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
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 56ff879603a31956db877b45aec11b15371b69f5
ms.sourcegitcommit: 5c1b5ef40ce7359b3f1955535a250718d863badb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/09/2021
ms.locfileid: "5142149"
---
# <a name="generate-aca-reports"></a><span data-ttu-id="4051f-103">Generování ACA sestav</span><span class="sxs-lookup"><span data-stu-id="4051f-103">Generate ACA reports</span></span>

<span data-ttu-id="4051f-104">Reporting zákona Affordable Care (ACA) generuje formuláře 1095-B a 1095-C podle části zákona Affordable Care **Mandát zaměstnavatele**.</span><span class="sxs-lookup"><span data-stu-id="4051f-104">Affordable Care Act (ACA) reporting generates forms 1095-B and 1095-C in support of the **Employer Mandate** portion of the Affordable Care Act.</span></span>

> [!NOTE]
> <span data-ttu-id="4051f-105">Hlášení ACA je povoleno pouze pro právnické osoby ve Spojených státech.</span><span class="sxs-lookup"><span data-stu-id="4051f-105">ACA reporting is only enabled for legal entities in the United States.</span></span>

## <a name="getting-started"></a><span data-ttu-id="4051f-106">Začínáme</span><span class="sxs-lookup"><span data-stu-id="4051f-106">Getting started</span></span>

<span data-ttu-id="4051f-107">Chcete-li sledovat informace proformuláře 1095-B a 1095-C musíte nejprve vytvořit jednu nebo více skupin Affordable Care.</span><span class="sxs-lookup"><span data-stu-id="4051f-107">To track information for forms 1095-B and 1095-C, you must first create one or more Affordable care coverage groups.</span></span> <span data-ttu-id="4051f-108">Skupiny pokrytí Affordable Care označují:</span><span class="sxs-lookup"><span data-stu-id="4051f-108">Affordable Care coverage groups indicate:</span></span>

- <span data-ttu-id="4051f-109">Nabídku pokrytí pro zaměstnance</span><span class="sxs-lookup"><span data-stu-id="4051f-109">The offer of coverage for an employee</span></span>
- <span data-ttu-id="4051f-110">Podíl zaměstnance na nejnižší měsíční prémii, pokud je cena nad federální hranicí chudoby</span><span class="sxs-lookup"><span data-stu-id="4051f-110">The employee’s share of the lowest cost monthly premium, if the cost is above the federal poverty line</span></span>
- <span data-ttu-id="4051f-111">Program Safe Harbor, který využívá zaměstnavatel, je-li k dispozici</span><span class="sxs-lookup"><span data-stu-id="4051f-111">Safe Harbor used by the employer, if applicable</span></span>

<span data-ttu-id="4051f-112">Skupiny pokrytí ACA, budete moci informace v těchto polích spravovat hromadně a nebudete muset upravovat každý záznam zaměstnance se stejnými podmínkami.</span><span class="sxs-lookup"><span data-stu-id="4051f-112">Affordable Care coverage groups allow you to manage the information for these fields without changing every employee record where the conditions are the same.</span></span> <span data-ttu-id="4051f-113">Skupiny pokrytí ACA lze snadno přiřadit k jednomu nebo několika zaměstnancům pomocí funkce **Hromadné přiřazení** na stránce.</span><span class="sxs-lookup"><span data-stu-id="4051f-113">You can easily assign Affordable Care coverage groups to one or more employees by using the **Mass assign** option on the page.</span></span>

## <a name="maintaining-multiple-versions-of-a-coverage-group"></a><span data-ttu-id="4051f-114">Správa několika verzí skupiny pokrytí</span><span class="sxs-lookup"><span data-stu-id="4051f-114">Maintaining multiple versions of a coverage group</span></span>

<span data-ttu-id="4051f-115">Můžete spravovat několik verzí skupin pokrytí.</span><span class="sxs-lookup"><span data-stu-id="4051f-115">You can maintain multiple versions of any coverage group.</span></span> <span data-ttu-id="4051f-116">Tato funkce vám umožňuje provádět změny, aniž byste museli vytvářet novou skupinu a znovu do ní přiřazovat zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="4051f-116">This functionality allows you to make changes without having to create a new group and reassign employees to it.</span></span> 

<span data-ttu-id="4051f-117">Poté, co vytvoříte skupiny pokrytí ACA, můžete hromadně přiřadit skupiny zaměstnancům s volbou **Hromadné přiřazení** volba.</span><span class="sxs-lookup"><span data-stu-id="4051f-117">After you’ve created ACA coverage groups, you can mass assign the groups to employees with the **Mass assignment** option.</span></span> <span data-ttu-id="4051f-118">Můžete také jednotlivě označit, zda chcete sledovat a hlásit informace ACA, a přiřadit zaměstnance do skupiny pokrytí Affordable Care.</span><span class="sxs-lookup"><span data-stu-id="4051f-118">You can also individually indicate whether to track and report ACA information, and assign an employee to an Affordable Care coverage group.</span></span>

<span data-ttu-id="4051f-119">Nemusíte sledovat některé informace o pokrytí ACA, například u zaměstnanců na částečný úvazek.</span><span class="sxs-lookup"><span data-stu-id="4051f-119">You don't need to track some ACA coverage information, such as for part-time employees.</span></span> <span data-ttu-id="4051f-120">V tomto případě nastavte **Zpráva o pokrytí** pole na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="4051f-120">In this case, set the **Report coverage** field to **No**.</span></span> <span data-ttu-id="4051f-121">I když musíte každému zaměstnanci přiřadit sledovatelné informace ACA do skupiny pokrytí Affordable Care, můžete změnit následující možnosti pro měsíce s různými hodnotami:</span><span class="sxs-lookup"><span data-stu-id="4051f-121">Although you must assign each employee with trackable ACA information to an Affordable Care coverage group, you can still change the following options for months with different values:</span></span>

- <span data-ttu-id="4051f-122">**Nabídka pokrytí**</span><span class="sxs-lookup"><span data-stu-id="4051f-122">**Offer of coverage**</span></span>
- <span data-ttu-id="4051f-123">**Podíl zaměstnance na nákladech**</span><span class="sxs-lookup"><span data-stu-id="4051f-123">**Employee share of cost**</span></span>
- <span data-ttu-id="4051f-124">**Institut "Safe Harbor"**</span><span class="sxs-lookup"><span data-stu-id="4051f-124">**Safe Harbor**</span></span>

<span data-ttu-id="4051f-125">Chcete-li zadat výjimky z hodnot skupiny pokrytí ACA, vyberte **Pokrytí Affordable Care** na stránce **Podrobnosti pracovníka** (v části **Další informace** na kartě **Zaměstnání**).</span><span class="sxs-lookup"><span data-stu-id="4051f-125">To enter exceptions for Affordable Care coverage group values, select the **Affordable Care Coverage** link on the **Worker detail** page under the **Additional information** section on the **Employment tab**.</span></span>

## <a name="reporting-health-care-coverage"></a><span data-ttu-id="4051f-126">Vykazování pokrytí zdravotní péče</span><span class="sxs-lookup"><span data-stu-id="4051f-126">Reporting health care coverage</span></span>

<span data-ttu-id="4051f-127">Pokud zaměstnavatel nabízí sponzorované pokrytí s vlastním připojištěním a zaměstnanco tuto nabídku využívá (bez ohledu na to, zda pracuje na plný nebo částečný úvazek), je ve formuláři 1095-C nutné hlásit i další informace vedle údajů o tom, jaké (pokud nějaké) pokrytí zdravotního pojištění bylo nabídnuto zaměstnanci na plný úvazek.</span><span class="sxs-lookup"><span data-stu-id="4051f-127">In addition to tracking health insurance coverage offered to full-time employees, if the employer offers employer-sponsored self-insured health coverage for which the employee is enrolled (regardless of whether their employment status is full-time or part-time), additional information needs to be reported on the 1095-C.</span></span> <span data-ttu-id="4051f-128">Ve výkazu musí být uvedeni všichni zaměstnanci (včetně závislých osob) krytí v rámci plánů zaměstnaneckých výhod sponzorovaných zaměstnavatelem, a to ve všech měsících, kdy pokrytí platilo.</span><span class="sxs-lookup"><span data-stu-id="4051f-128">Each employee (including dependents) covered by the employer-sponsored benefit plans needs to be included on the report for the months they were covered.</span></span> 

<span data-ttu-id="4051f-129">Zaškrtnutím políčka **Lze vykázat podle zákona ACA** můžete určit, zda je třeba daný plán zaměstnaneckých výhod vykazovat.</span><span class="sxs-lookup"><span data-stu-id="4051f-129">You can indicate whether or not each benefit plan must be reported by selecting the **ACA reportable** check box.</span></span>

<span data-ttu-id="4051f-130">Pokud si zaměstnanci navíc zvolili i krytí závislých osob, je možné uvést data, kdy pokrytí začalo platit, na stránce **Udržovat výhody**.</span><span class="sxs-lookup"><span data-stu-id="4051f-130">In addition, if employees have chosen to have any of their dependents covered under a benefit, you can indicate the dates the dependent was covered for each employee on the **Maintain benefits** page.</span></span> <span data-ttu-id="4051f-131">Chcete-li uvést, že se výhoda vztahuje na závislou osobu, vyberte tlačítko **Upravit** na panelu akcí na kartě **Rodinní příslušníci**.</span><span class="sxs-lookup"><span data-stu-id="4051f-131">To indicate that the dependent is covered under the benefit, select the **Edit** button in the action pane of the **Dependents** fast tab.</span></span>

<span data-ttu-id="4051f-132">Na stránce **Správce dat pokrytí rodinného příslušníka** můžete určit data pokrytí závislých osob v rámci zaměstnanecké výhody.</span><span class="sxs-lookup"><span data-stu-id="4051f-132">On the **Dependent coverage date manager** page, you can indicate the dates the dependent was covered by the benefit.</span></span> <span data-ttu-id="4051f-133">Zadáním data na této stránce automaticky zaškrtnete políčko **Pokryto** na stránce **Udržovat výhody**.</span><span class="sxs-lookup"><span data-stu-id="4051f-133">Entering dates on this page will automatically select the **Covered** checkbox on the **Maintain benefits** page.</span></span>

## <a name="generate-1095-b-and-1095-c-forms"></a><span data-ttu-id="4051f-134">Generujte formuláře 1095-B a 1095-C</span><span class="sxs-lookup"><span data-stu-id="4051f-134">Generate 1095-B and 1095-C forms</span></span>

<span data-ttu-id="4051f-135">Formuláře 1095-B and 1095-C můžete vygenerovat i v aplikaci a rozeslat je všem zaměstnancům.</span><span class="sxs-lookup"><span data-stu-id="4051f-135">You can also generate 1095-B and 1095-C forms from within the product, and distribute them to each of your employees.</span></span> <span data-ttu-id="4051f-136">Systém může také elektronicky generovat formuláře 1095-C a přenosové soubory IRS 1094-C.</span><span class="sxs-lookup"><span data-stu-id="4051f-136">The system can also electronically generate 1095-C forms and the 1094-C IRS transmittal files.</span></span>  

<span data-ttu-id="4051f-137">Při generování formuláře 1095 C zadejte příslušný daňový rok a označte, zda mají být nahrazena čísla sociálního pojištění.</span><span class="sxs-lookup"><span data-stu-id="4051f-137">When generating the 1095-C form, enter the appropriate tax year and indicate if social security numbers should be masked.</span></span> <span data-ttu-id="4051f-138">Při tisku formulářů 1095-C pro více než 500 zaměstnanců obdržíte více než jeden soubor PDF.</span><span class="sxs-lookup"><span data-stu-id="4051f-138">If you're printing 1095-C forms for more than 500 employees, you'll receive more than one PDF file.</span></span> <span data-ttu-id="4051f-139">Doporučuje se zvýšit **maximální velikost souboru** v okně **parametry správy dokumentů** na 150 MB.</span><span class="sxs-lookup"><span data-stu-id="4051f-139">It’s recommended that you increase the **Maximum file size** in the **Document management parameters** window to 150 MB.</span></span>

## <a name="viewing-information"></a><span data-ttu-id="4051f-140">Zobrazení informací</span><span class="sxs-lookup"><span data-stu-id="4051f-140">Viewing information</span></span>

<span data-ttu-id="4051f-141">Pomocí stránky **Pokrytí dostupné péče pro pracovníka** můžete zjistit, kteří zaměstnanci byli přiděleni k jednotlivým skupinám pokrytí, kteří zařazeni být nemusí a kteří přiřazeni nejsou.</span><span class="sxs-lookup"><span data-stu-id="4051f-141">You can use the **Worker Affordable Care coverage** page to see which employees have been assigned to each coverage group, which employees don’t need to be included on a report, and which employees are unassigned.</span></span>

<span data-ttu-id="4051f-142">U případných přepsaných výchozích hodnot skupiny pokrytí ACA se vedle změněné hodnoty zobrazí hvězdička.</span><span class="sxs-lookup"><span data-stu-id="4051f-142">If any of the default values from the Affordable Care coverage group have been overridden, an asterisk will appear next to the value that was changed.</span></span> <span data-ttu-id="4051f-143">Pokud jsou hodnoty u všech 12 měsíců stejné a nebyly přepsány, hodnota bude uvedena ve sloupci **Všech 12 měsíců**.</span><span class="sxs-lookup"><span data-stu-id="4051f-143">If the values for all 12 months are the same and haven’t been overridden, the value will print in the **All 12 months** column.</span></span>

<span data-ttu-id="4051f-144">Můžete také použít okno s dotazem, abyste pochopili, kteří zaměstnanci byli označeni jako zaměstnanci, kteří nejsou ACA vykazovatelní.</span><span class="sxs-lookup"><span data-stu-id="4051f-144">You can also use the inquiry window to understand which employees have been flagged as not ACA reportable.</span></span> <span data-ttu-id="4051f-145">Nemusíte sledovat, zda jim bylo nabídnuto pokrytí, a nebudete jim muset na konci roku vydat 1095-C.</span><span class="sxs-lookup"><span data-stu-id="4051f-145">You don’t need to track whether coverage was offered to them and won't need to issue a 1095-C to them at the end of the year.</span></span> <span data-ttu-id="4051f-146">Vyberte **Nevykazovatelní v rámci ACA** v poli **Filtrovat podle** pro vygenerování seznamu všech zaměstnanců, kteří neobdrží 1095-C.</span><span class="sxs-lookup"><span data-stu-id="4051f-146">Select **Not ACA reportable** in the **Filter by** field to generate a list of all employees who won't receive a 1095-C.</span></span>

<span data-ttu-id="4051f-147">Kromě toho můžete také zobrazit všechny zaměstnance, kteří nejsou přiřazeni (pole **Vykazovat pokrytí ACA** je prázdné) nebo kteří byli přiřazeni do skupiny pokrytí ACA, jejíž platnost pro rok zadaný v poli **Rok** vypršela.</span><span class="sxs-lookup"><span data-stu-id="4051f-147">In addition, you can view any employees who are unassigned (the **ACA Report coverage** field is empty) or who have been assigned to an Affordable Care coverage group that is expired for the year selected in the **Year** field.</span></span>

<span data-ttu-id="4051f-148">Seznamy zaměstnanců vygenerovaných podle zadaných filtrů je možné exportovat do aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="4051f-148">You can export lists of employees that were generated using any of the filtering options to Excel.</span></span>

<span data-ttu-id="4051f-149">Pokud potřebujete hlásit kryté osoby, protože poskytujete pojištěné osoby, můžete zobrazit závislé osoby, na které se vztahují plány dávek, které jsou označeny jako **hlásitelné ACA**.</span><span class="sxs-lookup"><span data-stu-id="4051f-149">If you need to report covered individuals because you provide self-insured coverage, you can view any dependents covered under benefit plans marked as **ACA reportable**.</span></span> <span data-ttu-id="4051f-150">V podokně akcí vyberte **Zobrazit data pokrytí rodinného příslušníka**.</span><span class="sxs-lookup"><span data-stu-id="4051f-150">Select **View Dependent coverage** on the action pane.</span></span>

> [!NOTE]
> <span data-ttu-id="4051f-151">Pouze plány dávek označené jako **hlásitelné ACA** zobrazit v okně dotazu.</span><span class="sxs-lookup"><span data-stu-id="4051f-151">Only benefit plans marked as **ACA reportable** display in the inquiry window.</span></span>
