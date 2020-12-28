---
title: Vývoj struktury kompenzace
description: Tento článek vás provede procesem vytváření plánu fixní kompenzace a přihlašování zaměstnanců do plánu pomocí pravidel způsobilosti.
author: andreabichsel
manager: AnnBe
ms.date: 02/10/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: DefaultDashboard, HcmCompensationWorkspace, HcmCompFixedPlansPart, HRMCompFixedPlanTable, HRMCompCreateGridDialog, HRCCompGridView, HRMCompEligibility,  HRCCompGrid
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 124d0f7f83feebabf622f00732c25bfa0f6eccdd
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417660"
---
# <a name="develop-a-compensation-structure"></a><span data-ttu-id="ae690-103">Vývoj struktury kompenzace</span><span class="sxs-lookup"><span data-stu-id="ae690-103">Develop a compensation structure</span></span>

<span data-ttu-id="ae690-104">Tento článek vás provede procesem vytváření plánu fixní kompenzace a přihlašování zaměstnanců do plánu pomocí pravidel způsobilosti.</span><span class="sxs-lookup"><span data-stu-id="ae690-104">This article walks you through creating a fixed compensation plan and enrolling employees in the plan through eligibility rules.</span></span> <span data-ttu-id="ae690-105">Tento článek používá ukázková data USMF a je určen pro manažery kompenzace a výhod.</span><span class="sxs-lookup"><span data-stu-id="ae690-105">This article uses the USMF demo data and applies to Compensation and Benefits Managers.</span></span>

## <a name="create-a-fixed-compensation-plan"></a><span data-ttu-id="ae690-106">Vytvoření plánu fixní kompenzace</span><span class="sxs-lookup"><span data-stu-id="ae690-106">Create a fixed compensation plan</span></span>

1. <span data-ttu-id="ae690-107">Vyberte **Správa kompenzací**.</span><span class="sxs-lookup"><span data-stu-id="ae690-107">Select **Compensation management**.</span></span>

2. <span data-ttu-id="ae690-108">Vyberte **Plány fixní kompenzace**.</span><span class="sxs-lookup"><span data-stu-id="ae690-108">Select **Fixed compensation plans**.</span></span>

3. <span data-ttu-id="ae690-109">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="ae690-109">Select **New**.</span></span>

4. <span data-ttu-id="ae690-110">Zadejte hodnotu do pole **Plán**.</span><span class="sxs-lookup"><span data-stu-id="ae690-110">In the **Plan** field, enter a value.</span></span>

5. <span data-ttu-id="ae690-111">V poli **Popis** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ae690-111">In the **Description** field, enter a value.</span></span>

6. <span data-ttu-id="ae690-112">Zadejte datum do pole **Datum platnosti**.</span><span class="sxs-lookup"><span data-stu-id="ae690-112">In the **Effective date** field, enter a date.</span></span>

7. <span data-ttu-id="ae690-113">V poli **Typ** určete, zda je plánem fixní kompenzace **Pásmo**, **Stupeň** nebo **Krok**.</span><span class="sxs-lookup"><span data-stu-id="ae690-113">In the **Type** field, select whether the fixed compensation plan is a **Band**, **Grade**, or **Step** plan.</span></span>

8. <span data-ttu-id="ae690-114">Pole **Doporučení povoleno** se chová jako výchozí hodnota pro všechny akce přidané do tohoto plánu v události zpracování.</span><span class="sxs-lookup"><span data-stu-id="ae690-114">The **Recommendation allowed** checkbox acts as a default value for any actions added to this plan in a Process event.</span></span> <span data-ttu-id="ae690-115">Povolením doporučení lze při zpracování kompenzace přepsat vypočítanou částku směrnice.</span><span class="sxs-lookup"><span data-stu-id="ae690-115">Allowing recommendations enables you to override the calculated guideline amount when processing compensation.</span></span>

9. <span data-ttu-id="ae690-116">Pole **Tolerance mimo rozsah** umožňuje určit, jakým způsobem chcete zpracovat částky kompenzace, které se nacházejí mimo určený rozsah struktury kompenzace na dané úrovni.</span><span class="sxs-lookup"><span data-stu-id="ae690-116">The **Out of range tolerance** field allows you to specify how you want to handle compensation amounts that fall outside of the specified compensation structure range for the given level.</span></span> <span data-ttu-id="ae690-117">Nastavení pole **Tolerance mimo rozsah** na **Žádný** umožňuje použít jakoukoli částku kompenzace.</span><span class="sxs-lookup"><span data-stu-id="ae690-117">Setting the **Out of range tolerance** field to **None** allows you to use any compensation amount.</span></span> <span data-ttu-id="ae690-118">**Předběžná tolerance** upozorní uživatele, pokud je kompenzace menší než minimální nebo větší než maximální výše referenčního bodu této úrovně.</span><span class="sxs-lookup"><span data-stu-id="ae690-118">**Soft tolerance** warns users if the compensation amount is less than the minimum or greater than the maximum reference point amounts for that level.</span></span> <span data-ttu-id="ae690-119">Uživatelé mohou výstrahu ignorovat a pokračovat.</span><span class="sxs-lookup"><span data-stu-id="ae690-119">Users can ignore the warning and continue.</span></span> <span data-ttu-id="ae690-120">**Pevná tolerance** vytvoří chybu, pokud je kompenzace zaměstnance nastavena mimo minimální a maximální referenční body pro úroveň, a automaticky upraví kompenzaci zaměstnance tak, aby spadala do rozsahu.</span><span class="sxs-lookup"><span data-stu-id="ae690-120">**Hard tolerance** generates an error if an employee's compensation is outside the minimum and maximum reference points for the level and will automatically adjust the employee's compensation to fall within the range.</span></span>

10. <span data-ttu-id="ae690-121">Pole **Pravidlo zařazení** vypočítává kompenzaci zaměstnance během procesní události.</span><span class="sxs-lookup"><span data-stu-id="ae690-121">The **Hire rule** field calculates an employee's compensation during a process event.</span></span> <span data-ttu-id="ae690-122">**Pravidlo zařazení** s hodnotou **Procento** vypočítá zvýšení, které je poměrné délce času, kdy byl pracovník zaměstnán během daného cyklu.</span><span class="sxs-lookup"><span data-stu-id="ae690-122">A **Hire rule** of **Percent** calculates an increase that's prorated for the length of the time the worker has been employed in the cycle.</span></span>

11. <span data-ttu-id="ae690-123">Zadejte hodnotu do pole **Měna**.</span><span class="sxs-lookup"><span data-stu-id="ae690-123">In the **Currency** field, type a value.</span></span>

12. <span data-ttu-id="ae690-124">V poli **Převod mzdové sazby** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ae690-124">In the **Pay rate conversion** field, enter or select a value.</span></span>

13. <span data-ttu-id="ae690-125">Rozbalte oddíl **Matice využití rozsahu**.</span><span class="sxs-lookup"><span data-stu-id="ae690-125">Expand the **Range utilization matrix** section.</span></span> <span data-ttu-id="ae690-126">Volitelně můžete přidat záznamy využití a dostat tak zaměstnance rychleji do jejich středového bodu a zpomalit jejich dosažení maxima rozsahu.</span><span class="sxs-lookup"><span data-stu-id="ae690-126">Optionally, add range utilization records to get employees to their midpoint faster and slow them from reaching the maximum of their range.</span></span>

14. <span data-ttu-id="ae690-127">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="ae690-127">Select **Save**.</span></span> <span data-ttu-id="ae690-128">Tím se aktivuje tlačítko **Nastavit kompenzaci** a budete pokračovat ve definování struktury kompenzací pro daný plán.</span><span class="sxs-lookup"><span data-stu-id="ae690-128">This enables the **Set up compensation** button and continue defining your compensation structure for the plan.</span></span>

15. <span data-ttu-id="ae690-129">Vyberte **Nastavení kompenzace**.</span><span class="sxs-lookup"><span data-stu-id="ae690-129">Select **Set up compensation**.</span></span> <span data-ttu-id="ae690-130">Můžete vytvořit strukturu kompenzace pomocí jedné z následujících třech metod:</span><span class="sxs-lookup"><span data-stu-id="ae690-130">You can create a compensation structure by using one of these three methods:</span></span>

    - <span data-ttu-id="ae690-131">Vytvořte zcela novou strukturu výběrem sady referenčních bodů a přidáním úrovní pro vytvoření vlastní struktury.</span><span class="sxs-lookup"><span data-stu-id="ae690-131">Create a completely new structure by selecting a set of reference points and adding the levels to create your own structure.</span></span>
    - <span data-ttu-id="ae690-132">Zkopírujte strukturu kompenzací z existujícího plánu jako výchozí bod a upravte jej na nový plán.</span><span class="sxs-lookup"><span data-stu-id="ae690-132">Copy a compensation structure from an existing plan as a starting point and modify it for the new plan.</span></span>
    - <span data-ttu-id="ae690-133">Vyberte existující mřížku kompenzace.</span><span class="sxs-lookup"><span data-stu-id="ae690-133">Select an existing compensation grid.</span></span> <span data-ttu-id="ae690-134">Je-li kompenzační mřížka již používaná jiným plánem, změny provedené v mřížce budou také zahrnuty do jiného plánu.</span><span class="sxs-lookup"><span data-stu-id="ae690-134">If another plan already uses the compensation grid, the other plan also reflects any changes you make to the grid.</span></span>

16. <span data-ttu-id="ae690-135">Vyberte **Vytvořit novou ze stávající matice kompenzace**.</span><span class="sxs-lookup"><span data-stu-id="ae690-135">Select **Create new from existing compensation matrix**.</span></span>

17. <span data-ttu-id="ae690-136">V poli **Kopírovat z mřížky** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ae690-136">In the **Copy from grid** field, enter or select a value.</span></span> <span data-ttu-id="ae690-137">Volitelně můžete změnit název nové mřížky kompenzací, která bude vytvořena jako kopie vybrané mřížky.</span><span class="sxs-lookup"><span data-stu-id="ae690-137">Optionally, you can change the name of the new compensation grid that you create by copying the selected grid.</span></span>

18. <span data-ttu-id="ae690-138">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="ae690-138">Select **OK**.</span></span>

19. <span data-ttu-id="ae690-139">Vyberte **Hromadnou změnu**.</span><span class="sxs-lookup"><span data-stu-id="ae690-139">Select **Mass change**.</span></span> <span data-ttu-id="ae690-140">**Hromadná změna** vám umožní spravovat částky matice kompenzace použitím procenta nebo jednotného nárůstu pro jednu nebo více úrovní a/nebo referenčních bodů.</span><span class="sxs-lookup"><span data-stu-id="ae690-140">**Mass change** allows you to maintain the compensation matrix amounts by applying a percent or flat amount increase to one or more levels or reference points.</span></span>

20. <span data-ttu-id="ae690-141">Zadejte číslo do pole **Částka úpravy**.</span><span class="sxs-lookup"><span data-stu-id="ae690-141">In the **Adjustment amount** field, enter a number.</span></span>

21. <span data-ttu-id="ae690-142">V seznamu označte všechny řádky nebo jejich označení zrušte.</span><span class="sxs-lookup"><span data-stu-id="ae690-142">In the list, mark or unmark all rows.</span></span>

22. <span data-ttu-id="ae690-143">Klikněte na **Použít na mřížku**.</span><span class="sxs-lookup"><span data-stu-id="ae690-143">Click **Apply to grid**.</span></span>

23. <span data-ttu-id="ae690-144">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ae690-144">Close the page.</span></span> <span data-ttu-id="ae690-145">Jakmile struktura kompenzace bude vytvořena nebo vybrána, lze vybrat, který referenční bod by měl být použit jako kontrolní bod pro plán fixní kompenzace.</span><span class="sxs-lookup"><span data-stu-id="ae690-145">After you create the compensation structure, you can select which of the reference points to use as the control point for the fixed compensation plan.</span></span> <span data-ttu-id="ae690-146">Kontrolní bod se používá k výpočtu srovnávacího poměru zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="ae690-146">The control point is used to calculate an employee's Compa Ratio.</span></span>

24. <span data-ttu-id="ae690-147">V poli **Kontrolní bod** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ae690-147">In the **Control point** field, enter or select a value.</span></span>

25. <span data-ttu-id="ae690-148">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ae690-148">Close the page.</span></span>

## <a name="create-an-eligibility-rule-for-the-fixed-compensation-plan"></a><span data-ttu-id="ae690-149">Vytvoření pravidla kompenzace pro plán fixní kompenzace</span><span class="sxs-lookup"><span data-stu-id="ae690-149">Create an eligibility rule for the fixed compensation plan</span></span>

<span data-ttu-id="ae690-150">Nový plán fixní kompenzace nelze přiřadit zaměstnanci, dokud nebudou definována pravidla způsobilosti pro plán.</span><span class="sxs-lookup"><span data-stu-id="ae690-150">You can't assign a fixed compensation plan to an employee until you define eligibility rules for the plan.</span></span>  

1. <span data-ttu-id="ae690-151">Vyberte **Pravidla nároků**.</span><span class="sxs-lookup"><span data-stu-id="ae690-151">Select **Eligibility rules**.</span></span>

2. <span data-ttu-id="ae690-152">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="ae690-152">Select **New**.</span></span>

3. <span data-ttu-id="ae690-153">V poli **Nárok** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ae690-153">In the **Eligibility** field, enter a value.</span></span>

4. <span data-ttu-id="ae690-154">V poli **Popis** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ae690-154">In the **Description** field, enter a value.</span></span>

5. <span data-ttu-id="ae690-155">Zadejte datum do pole **Datum platnosti**.</span><span class="sxs-lookup"><span data-stu-id="ae690-155">In the **Effective date** field, enter a date.</span></span> <span data-ttu-id="ae690-156">Pravidla způsobilosti se používají pro plány fixní i variabilní kompenzace.</span><span class="sxs-lookup"><span data-stu-id="ae690-156">Both fixed and variable compensation plans use eligibility rules.</span></span> <span data-ttu-id="ae690-157">V poli **Typ** vyberte typ plánování.</span><span class="sxs-lookup"><span data-stu-id="ae690-157">In the **Type** field, select the type of plan.</span></span>

6. <span data-ttu-id="ae690-158">V poli **Plán** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ae690-158">In the **Plan** field, enter or select a value.</span></span> <span data-ttu-id="ae690-159">Vyberte kritéria, která zaměstnanec musí splňovat, aby splňoval požadavky pro plán kompenzace.</span><span class="sxs-lookup"><span data-stu-id="ae690-159">Select the criteria an employee must meet in order to be eligible for the compensation plan.</span></span> <span data-ttu-id="ae690-160">Kritéria mohou zahrnovat:</span><span class="sxs-lookup"><span data-stu-id="ae690-160">Criteria can include:</span></span>

    - <span data-ttu-id="ae690-161">**Oddělení**</span><span class="sxs-lookup"><span data-stu-id="ae690-161">**Department**</span></span>
    - <span data-ttu-id="ae690-162">**Odbor**</span><span class="sxs-lookup"><span data-stu-id="ae690-162">**Labor union**</span></span>
    - <span data-ttu-id="ae690-163">**Umístění** (**Umístění kompenzace**)</span><span class="sxs-lookup"><span data-stu-id="ae690-163">**Location** (**Compensation region**)</span></span>
    - <span data-ttu-id="ae690-164">**Práce**</span><span class="sxs-lookup"><span data-stu-id="ae690-164">**Job**</span></span>
    - <span data-ttu-id="ae690-165">**Funkce**</span><span class="sxs-lookup"><span data-stu-id="ae690-165">**Function**</span></span>
    - <span data-ttu-id="ae690-166">**Typ úlohy**</span><span class="sxs-lookup"><span data-stu-id="ae690-166">**Job type**</span></span>
    - <span data-ttu-id="ae690-167">**Úroveň kompenzace**</span><span class="sxs-lookup"><span data-stu-id="ae690-167">**Compensation level**</span></span>
    
    <span data-ttu-id="ae690-168">Zaměstnanec musí splňovat všechna uvedená kritéria, aby splňoval požadavky pro plán kompenzace.</span><span class="sxs-lookup"><span data-stu-id="ae690-168">The employee must meet all specified criteria to be eligible for the compensation plan.</span></span> <span data-ttu-id="ae690-169">Pokud neuvedete žádná kritéria, všichni zaměstnanci splňují požadavky pro plán kompenzace.</span><span class="sxs-lookup"><span data-stu-id="ae690-169">If you don't specify any criteria, all employees are eligible for the compensation plan.</span></span> <span data-ttu-id="ae690-170">Pokud zaměstnanec nesplňuje kritéria určená v pravidlu způsobilosti, nebo nebylo zadáno pravidlo způsobilosti pro plán kompenzace, plán kompenzace se nezobrazí ve vyhledávání při vytváření záznamu fixní kompenzace pro určitého zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="ae690-170">If an employee doesn't meet the criteria specified in the eligibility rule, or an eligibility rule has not been specified for a compensation plan, the compensation plan won't appear in the lookup when you create a fixed compensation record for an employee.</span></span>

7. <span data-ttu-id="ae690-171">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ae690-171">Close the page.</span></span>

8. <span data-ttu-id="ae690-172">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ae690-172">Close the page.</span></span>

