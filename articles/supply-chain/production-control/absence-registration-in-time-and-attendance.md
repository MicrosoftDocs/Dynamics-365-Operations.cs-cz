---
title: Registrace absence v modulu Čas a docházka
description: Toto téma vysvětluje, jak pracovat s registracemi absence v modulu Čas a docházka.
author: johanhoffmann
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JMGParameters, JmgAbsenceCalendar
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b765ae63cfb17e26439758f2a0ed64770ef70881
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809271"
---
# <a name="absence-registration-in-time-and-attendance"></a><span data-ttu-id="07fb8-103">Registrace absence v modulu Čas a docházka</span><span class="sxs-lookup"><span data-stu-id="07fb8-103">Absence registration in Time and attendance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="07fb8-104">Toto téma popisuje koncept absence a vysvětluje, jak pracovat s absencí v modulu Čas a docházka.</span><span class="sxs-lookup"><span data-stu-id="07fb8-104">This topic describes the concepts for absence and explains how to handle absence in Time and attendance.</span></span>

## <a name="absence-that-is-based-on-regular-work-hours"></a><span data-ttu-id="07fb8-105">Absence založená na běžné pracovní době</span><span class="sxs-lookup"><span data-stu-id="07fb8-105">Absence that is based on regular work hours</span></span>

<span data-ttu-id="07fb8-106">Pracovníci jsou považováni za nepřítomné za každou hodinu, kterou neodpracovali ve své standardní pracovní době.</span><span class="sxs-lookup"><span data-stu-id="07fb8-106">Workers are considered absent for any hours that they don't work during their regular work hours.</span></span> <span data-ttu-id="07fb8-107">Běžná pracovní doba je definována ve standardním časovém profilu pracovníka.</span><span class="sxs-lookup"><span data-stu-id="07fb8-107">Regular work hours are defined in a worker's standard time profile.</span></span>

<span data-ttu-id="07fb8-108">Například pracovník pracuje v denním profilu, který má stanovený příchod v 7:00 a odchod v 15:00.</span><span class="sxs-lookup"><span data-stu-id="07fb8-108">For example, a worker is working on a day profile that has clock-in at 7:00 AM and clock-out at 3:00 PM.</span></span> <span data-ttu-id="07fb8-109">Pokud pracovník označí čas příchodu v 9:00, je v tento den považován za nepřítomného od 7:00 do 9:00.</span><span class="sxs-lookup"><span data-stu-id="07fb8-109">If the worker clocks in at 9:00 AM, he is considered absent from 7:00 AM to 9:00 AM on that day.</span></span>

<span data-ttu-id="07fb8-110">V takovém případě jsou pracovníci vyzváni, aby zadali důvod své absence.</span><span class="sxs-lookup"><span data-stu-id="07fb8-110">In this case, workers are prompted to enter a reason for their absence.</span></span> <span data-ttu-id="07fb8-111">Důvod mohou určit zvolením kódu absence.</span><span class="sxs-lookup"><span data-stu-id="07fb8-111">They can specify a reason by selecting an absence code.</span></span>

## <a name="absence-codes"></a><span data-ttu-id="07fb8-112">Kódy absencí</span><span class="sxs-lookup"><span data-stu-id="07fb8-112">Absence codes</span></span>

<span data-ttu-id="07fb8-113">Kódy absence definují různé typy absence.</span><span class="sxs-lookup"><span data-stu-id="07fb8-113">Absence codes define the various types of absence.</span></span> <span data-ttu-id="07fb8-114">Kódy absence určuje společnost.</span><span class="sxs-lookup"><span data-stu-id="07fb8-114">Absence codes are defined by the company.</span></span>

<span data-ttu-id="07fb8-115">Na kódy absence lze použít různá pravidla.</span><span class="sxs-lookup"><span data-stu-id="07fb8-115">Various rules can be applied to absence codes.</span></span> <span data-ttu-id="07fb8-116">Například kód absence lze nakonfigurovat tak, aby absenci odečítal ze mzdy nebo naopak neodečítal.</span><span class="sxs-lookup"><span data-stu-id="07fb8-116">For example, an absence code can be configured to deduct or grant pay.</span></span>

<span data-ttu-id="07fb8-117">Společnost například definuje kód absence **Opoždění**, který pracovníci použijí, pokud přijdou pozdě a nemají k tomu dostatečný důvod.</span><span class="sxs-lookup"><span data-stu-id="07fb8-117">For example, a company defines a **Late** absence code that workers use if they come in late and don't have a good reason.</span></span> <span data-ttu-id="07fb8-118">Společnost též definuje kód absence **Interní kurz**, který pracovníci použijí pro čas strávený docházkou na interní kurzy.</span><span class="sxs-lookup"><span data-stu-id="07fb8-118">The company also defines an **Internal course** absence code that workers use for time that they spend attending internal courses.</span></span> <span data-ttu-id="07fb8-119">Tyto kódy absence lze nastavit tak, že **Opoždění** se odečte od mzdy pracovníka, zatímco **Interní kurz** se z jeho mzdy neodečte.</span><span class="sxs-lookup"><span data-stu-id="07fb8-119">These absence codes can be set up so that **Late** deducts from a worker's pay but **Internal course** doesn't deduct from a worker's pay.</span></span>

<span data-ttu-id="07fb8-120">Můžete nastavit automatické kódy absence.</span><span class="sxs-lookup"><span data-stu-id="07fb8-120">You can set up automatic absence codes.</span></span> <span data-ttu-id="07fb8-121">Tyto kódy absence lze použít pro výpočet času pracovníka, když není registrována žádná absence.</span><span class="sxs-lookup"><span data-stu-id="07fb8-121">These absence codes can be used to calculate a worker's time when no absence is registered.</span></span> <span data-ttu-id="07fb8-122">Časový profil pracovníka určuje, zda se používá kód absence pro standardní pracovní dobu nebo pro pružnou pracovní dobu.</span><span class="sxs-lookup"><span data-stu-id="07fb8-122">The worker's time profile determines whether the absence code for standard time or flex time is used.</span></span>

### <a name="set-up-standard-time-and-flex-time"></a><span data-ttu-id="07fb8-123">Nastavení standardní a pružné pracovní doby</span><span class="sxs-lookup"><span data-stu-id="07fb8-123">Set up standard time and flex time</span></span>

- <span data-ttu-id="07fb8-124">Nakonfigurujte parametry pro standardní a pružnou pracovní dobu pomocí možností **Automaticky vložit absenci** a **Automaticky vložit flex--** na stránce **Parametry času a docházky**.</span><span class="sxs-lookup"><span data-stu-id="07fb8-124">Configure the parameters for standard time and flex time by using the **Auto insert absence** and **Auto insert Flex-** options on the **Time and attendance parameters** page.</span></span>

## <a name="absence-groups"></a><span data-ttu-id="07fb8-125">Skupiny absencí</span><span class="sxs-lookup"><span data-stu-id="07fb8-125">Absence groups</span></span>

<span data-ttu-id="07fb8-126">Kódy absencí jsou seskupeny do skupin absencí.</span><span class="sxs-lookup"><span data-stu-id="07fb8-126">Absence codes are grouped into absence groups.</span></span> <span data-ttu-id="07fb8-127">Skupiny absencí použijete pro seskupení kódů absencí, které mají společné vlastnosti.</span><span class="sxs-lookup"><span data-stu-id="07fb8-127">You use absence groups to group absence codes that have common characteristics.</span></span> <span data-ttu-id="07fb8-128">Příklady zahrnují kódy absencí pro zákonnou absenci nebo absencí z důvodu návštěvy lékaře, účasti u soudu jako porotce nebo nemocného dítěte.</span><span class="sxs-lookup"><span data-stu-id="07fb8-128">Examples include absence codes for a legal absence, or absence because of a doctor's appointment, jury duty, or a sick child.</span></span>

## <a name="planned-absence"></a><span data-ttu-id="07fb8-129">Plánovaná absence</span><span class="sxs-lookup"><span data-stu-id="07fb8-129">Planned absence</span></span>

<span data-ttu-id="07fb8-130">Pokud víte, že pracovník bude nepřítomen určitou dobu, například nadcházející dovolená, můžete použít plánovanou absenci.</span><span class="sxs-lookup"><span data-stu-id="07fb8-130">If you know that a worker will be absent for a period, such as an upcoming vacation, you can use planned absence.</span></span> <span data-ttu-id="07fb8-131">Plánovanou absenci nastavíte pomocí konfigurace kódu absence tak, aby počítal s plánovanou absencí.</span><span class="sxs-lookup"><span data-stu-id="07fb8-131">You set up planned absence by configuring the absence code so that it considers the planned absence.</span></span> <span data-ttu-id="07fb8-132">Při nastavování plánované absence nebudete vyzváni k zadání kódu absence v době absence, když jsou počítány registrace pracovní doby uživatele.</span><span class="sxs-lookup"><span data-stu-id="07fb8-132">When you set up a planned absence, you aren't prompted for an absence code during the absence period when user time registrations are calculated.</span></span> <span data-ttu-id="07fb8-133">Plánovanou absenci lze určit pro jednoho zaměstnance, nebo můžete definovat dávkovou úlohu pro hromadnou aktualizaci plánovaných absencí pro pracovníky.</span><span class="sxs-lookup"><span data-stu-id="07fb8-133">Planned absence can be defined for a single worker, or you can define a batch job to bulk update the planned absence for workers.</span></span>

### <a name="set-up-planned-absence"></a><span data-ttu-id="07fb8-134">Nastavení plánované absence</span><span class="sxs-lookup"><span data-stu-id="07fb8-134">Set up planned absence</span></span>

1. <span data-ttu-id="07fb8-135">Vyberte **Lidské zdroje** &gt; **Pracovníci** &gt; **Zaměstnanci** a vyberte zaměstnance.</span><span class="sxs-lookup"><span data-stu-id="07fb8-135">Select **Human resources** &gt; **Workers** &gt; **Employees**, and select an employee.</span></span>
2. <span data-ttu-id="07fb8-136">Vyberte **Pracovní doba** &gt; **Přiřazení pracovní doby** &gt; **Registrace času absence** a nastavte plánovanou absenci.</span><span class="sxs-lookup"><span data-stu-id="07fb8-136">Select **Time** &gt; **Time assignments** &gt; **Time Absence registration**, and set up the planned absence.</span></span>

## <a name="interrupted-planned-absence"></a><span data-ttu-id="07fb8-137">Přerušená plánovaná absence</span><span class="sxs-lookup"><span data-stu-id="07fb8-137">Interrupted planned absence</span></span>

<span data-ttu-id="07fb8-138">Použijete-li možnost **Přerušit** při nastavování plánované absence, plánovaná absence bude přerušena v případě, že se pracovník dostaví do práce v období plánované absence.</span><span class="sxs-lookup"><span data-stu-id="07fb8-138">If you apply the **Interrupt** option when you set up a planned absence, the planned absence will be interrupted if the worker signs in during the planned absence period.</span></span> <span data-ttu-id="07fb8-139">Plánovaná absence bude označena jako **Přerušená** a nebude mít žádný vliv na budoucí výpočty.</span><span class="sxs-lookup"><span data-stu-id="07fb8-139">The planned absence will be marked as **Interrupted** and won't have any effect on future calculations.</span></span>

### <a name="set-up-a-planned-absence-for-interruption"></a><span data-ttu-id="07fb8-140">Nastavení plánované absence pro přerušení</span><span class="sxs-lookup"><span data-stu-id="07fb8-140">Set up a planned absence for interruption</span></span>

1. <span data-ttu-id="07fb8-141">Otevřete stránku **Registrace času absence**, jak je popsáno v postupu pro nastavení plánované absence.</span><span class="sxs-lookup"><span data-stu-id="07fb8-141">Open the **Time Absence registration** page as described in the procedure for setting up planned absence.</span></span>
2. <span data-ttu-id="07fb8-142">Vyberte **Přerušit**.</span><span class="sxs-lookup"><span data-stu-id="07fb8-142">Select **Interrupt**.</span></span>

<span data-ttu-id="07fb8-143">Možnost **Přerušit** se použije při registraci času prostřednictvím dílenského terminálu nebo dílenského zařízení.</span><span class="sxs-lookup"><span data-stu-id="07fb8-143">The **Interrupt** option applies when time is registered through the shop floor terminal or the shop floor device.</span></span> <span data-ttu-id="07fb8-144">Možnost se nepoužije, když jsou zadány registrace na stránkách výpočtu a schválení, nebo na stránce **Elektronická časová karta**.</span><span class="sxs-lookup"><span data-stu-id="07fb8-144">The option doesn't apply if the registrations are entered on the calculation and approval pages, or on the **Electronic timecard** page.</span></span>

## <a name="examples-of-the-use-of-absence-in-a-flex-profile"></a><span data-ttu-id="07fb8-145">Příklady použití absence v profilu pružné pracovní doby</span><span class="sxs-lookup"><span data-stu-id="07fb8-145">Examples of the use of absence in a flex profile</span></span>

<span data-ttu-id="07fb8-146">Následující tři příklady ukazují, jak se vypočítávají absence v profilu s pružnou pracovní dobou.</span><span class="sxs-lookup"><span data-stu-id="07fb8-146">The following three examples show how absence is calculated in a profile that has flex periods.</span></span>

<span data-ttu-id="07fb8-147">Příklady používají následující profil.</span><span class="sxs-lookup"><span data-stu-id="07fb8-147">The examples use the following profile.</span></span>

| <span data-ttu-id="07fb8-148">Označení příchodu</span><span class="sxs-lookup"><span data-stu-id="07fb8-148">Clock-in</span></span> | <span data-ttu-id="07fb8-149">Standardní čas</span><span class="sxs-lookup"><span data-stu-id="07fb8-149">Standard time</span></span>    | <span data-ttu-id="07fb8-150">Přerušení</span><span class="sxs-lookup"><span data-stu-id="07fb8-150">Break</span></span>             | <span data-ttu-id="07fb8-151">Standardní čas</span><span class="sxs-lookup"><span data-stu-id="07fb8-151">Standard time</span></span> | <span data-ttu-id="07fb8-152">Flexibilita-</span><span class="sxs-lookup"><span data-stu-id="07fb8-152">Flex-</span></span>        | <span data-ttu-id="07fb8-153">Označení odchodu</span><span class="sxs-lookup"><span data-stu-id="07fb8-153">Clock-out</span></span> | <span data-ttu-id="07fb8-154">Flexibilita+</span><span class="sxs-lookup"><span data-stu-id="07fb8-154">Flex+</span></span>        |
|----------|------------------|-------------------|---------------|--------------|-----------|--------------|
| <span data-ttu-id="07fb8-155">8:00</span><span class="sxs-lookup"><span data-stu-id="07fb8-155">8 AM</span></span>     | <span data-ttu-id="07fb8-156">9:00 až 11:30</span><span class="sxs-lookup"><span data-stu-id="07fb8-156">9 AM to 11:30 AM</span></span> | <span data-ttu-id="07fb8-157">11:30 až 12:00</span><span class="sxs-lookup"><span data-stu-id="07fb8-157">11:30 AM to 12 PM</span></span> | <span data-ttu-id="07fb8-158">12:00 až 15:00</span><span class="sxs-lookup"><span data-stu-id="07fb8-158">12 PM to 3 PM</span></span> | <span data-ttu-id="07fb8-159">15:00 až 16:00</span><span class="sxs-lookup"><span data-stu-id="07fb8-159">3 PM to 4 PM</span></span> | <span data-ttu-id="07fb8-160">16:00</span><span class="sxs-lookup"><span data-stu-id="07fb8-160">4 PM</span></span>      | <span data-ttu-id="07fb8-161">16:00 až 18:00</span><span class="sxs-lookup"><span data-stu-id="07fb8-161">4 PM to 6 PM</span></span> |

### <a name="example-1-signing-out-during-a-flex--period"></a><span data-ttu-id="07fb8-162">Příklad 1: Odhlášení během pružné pracovní doby (Flex-)</span><span class="sxs-lookup"><span data-stu-id="07fb8-162">Example 1: Signing out during a Flex- period</span></span>

<span data-ttu-id="07fb8-163">Pracovník označí čas příchodu v 8:00 a čas odchodu v 15:30.</span><span class="sxs-lookup"><span data-stu-id="07fb8-163">The worker clocks in at 8:00 AM and clocks out at 3:30 PM.</span></span> <span data-ttu-id="07fb8-164">Protože pracovník v tomto případě označí odchod během pružné pracovní doby (Flex-), nevypočítá se žádná absence a od zůstatku pružné pracovní doby pracovníka se odečte půl hodiny.</span><span class="sxs-lookup"><span data-stu-id="07fb8-164">In this case, because the worker clocks out during a Flex- period, no absence is calculated, and half an hour is deducted from the worker's flex balance.</span></span>

### <a name="example-2-signing-out-in-during-standard-time-period"></a><span data-ttu-id="07fb8-165">Příklad 2: Odhlášení ve standardní pracovní době</span><span class="sxs-lookup"><span data-stu-id="07fb8-165">Example 2: Signing out in during Standard time period</span></span>

<span data-ttu-id="07fb8-166">Pracovník označí čas příchodu v 8:00 a čas odchodu v 14:30.</span><span class="sxs-lookup"><span data-stu-id="07fb8-166">The worker clocks in at 8:00 AM and clocks out at 2:30 PM.</span></span> <span data-ttu-id="07fb8-167">Protože pracovník v tomto případě označí odchod během standardní pracovní doby, absence se vypočítá z času 14:30 až 16:00 a zaregistruje se doba absence 1,5 hodiny.</span><span class="sxs-lookup"><span data-stu-id="07fb8-167">In this case, because the worker clocks out during the Standard time period, absence is calculated from 2:30 PM to 4 PM, and an absence period of 1.5 hours is registered.</span></span> <span data-ttu-id="07fb8-168">Je požadován kód absence pro toto období.</span><span class="sxs-lookup"><span data-stu-id="07fb8-168">An absence code for that period is required.</span></span>

### <a name="example-3-signing-out-during-a-flex-period"></a><span data-ttu-id="07fb8-169">Příklad 3: Odhlášení během pružné pracovní doby (Flex+)</span><span class="sxs-lookup"><span data-stu-id="07fb8-169">Example 3: Signing out during a Flex+ period</span></span>

<span data-ttu-id="07fb8-170">Pracovník označí čas příchodu v 8:00 a čas odchodu v 16:30.</span><span class="sxs-lookup"><span data-stu-id="07fb8-170">The worker clocks in at 8:00 AM and clocks out at 4:30 PM.</span></span> <span data-ttu-id="07fb8-171">Protože pracovník v tomto případě označí odchod během pružné pracovní doby (Flex+), nevypočítá se žádná absence a do zůstatku pružné pracovní doby se přidá půl hodiny.</span><span class="sxs-lookup"><span data-stu-id="07fb8-171">In this case, because the worker clocks out during a Flex+ period, no absence is calculated, and half an hour is added to the worker's flex balance.</span></span>

## <a name="absence-in-the-calculation-and-approval-process"></a><span data-ttu-id="07fb8-172">Absence v procesu výpočtu a schválení</span><span class="sxs-lookup"><span data-stu-id="07fb8-172">Absence in the calculation and approval process</span></span>

<span data-ttu-id="07fb8-173">Registrace pracovní doby pracovníka musí být vypočteny a schváleny předtím, než je lze převést do výplatního systému jako položky mzdy.</span><span class="sxs-lookup"><span data-stu-id="07fb8-173">Worker time registrations must be calculated and approved before they can be transferred to a payroll system as pay items.</span></span>

<span data-ttu-id="07fb8-174">Schvalovatel může změnit registrace pracovní doby pracovníka.</span><span class="sxs-lookup"><span data-stu-id="07fb8-174">An approver can change a worker's time registrations.</span></span> <span data-ttu-id="07fb8-175">Schvalovatel může dokonce změnit jakoukoliv absenci, kterou pracovník zaregistroval.</span><span class="sxs-lookup"><span data-stu-id="07fb8-175">The approver can even change any absence that the worker has registered.</span></span> <span data-ttu-id="07fb8-176">Pokud schvalovatel ručně zadá časové období, které má kód absence, není pro toto období kód absence přepsán výchozím kódem absence z parametrů modulu Čas a docházka.</span><span class="sxs-lookup"><span data-stu-id="07fb8-176">If the approver manually enters a time period that has an absence code, the absence code for that period isn't overridden by the default absence code from the Time and attendance parameters.</span></span>

<span data-ttu-id="07fb8-177">Například pracovník označí příchod v 10:00 a vybere kód absence, který označuje, že má zpoždění.</span><span class="sxs-lookup"><span data-stu-id="07fb8-177">For example, a worker clocks in at 10 AM and selects an absence code that indicates that she is late.</span></span> <span data-ttu-id="07fb8-178">Později pracovník informuje svého nadřízeného o tom, že byl u lékaře od 8:00 do 10:00.</span><span class="sxs-lookup"><span data-stu-id="07fb8-178">Later, the worker informs her supervisor that she had a doctor's appointment from 8 AM to 10 AM.</span></span> <span data-ttu-id="07fb8-179">Návštěva lékaře nesmí způsobit srážku ze mzdy pracovníka.</span><span class="sxs-lookup"><span data-stu-id="07fb8-179">A doctor's appointment should not cause a deduction in the worker's pay.</span></span> <span data-ttu-id="07fb8-180">Proto v tomto případě může nadřízený upravit dvě hodiny absence od 8:00 do 10:00 tak, že ručně zadá kód absence, který označuje pro tyto dvě hodiny nemoc.</span><span class="sxs-lookup"><span data-stu-id="07fb8-180">Therefore, in this case, the supervisor can adjust the two hours of absence from 8 AM to 10 AM by manually entering an absence code that indicates illness for those two hours.</span></span>

### <a name="calculate-and-approve-absence"></a><span data-ttu-id="07fb8-181">Výpočet a schválení absence</span><span class="sxs-lookup"><span data-stu-id="07fb8-181">Calculate and approve absence</span></span>

- <span data-ttu-id="07fb8-182">Vyberte **Čas a docházka** &gt; **Zkontrolovat a schválit** &gt; **Schválit nebo vypočítat**.</span><span class="sxs-lookup"><span data-stu-id="07fb8-182">Select **Time attendance** &gt; **Review and approve** &gt; **Approve or Calculate**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]