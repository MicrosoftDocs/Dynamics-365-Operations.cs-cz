---
title: Degresivní odpis 175 %
description: Toto téma poskytuje přehled metody degresivního odpisu 175 %.
author: saraschi2
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 13911
ms.assetid: cc5d001f-bcfe-4602-9ec1-9e265e9fd188
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f0747c34a4b28340227209adadf367f672deb1ab
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827139"
---
# <a name="175-percent-reducing-balance-depreciation"></a><span data-ttu-id="c755b-103">Degresivní odpis 175 %</span><span class="sxs-lookup"><span data-stu-id="c755b-103">175 percent reducing balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c755b-104">Toto téma poskytuje přehled metody degresivního odpisu 175 %.</span><span class="sxs-lookup"><span data-stu-id="c755b-104">This topic gives an overview of the 175 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="c755b-105">Pokud nastavujete odpisový profil dlouhodobého majetku a zaškrtnete volbu **Degresivní 175 %** v poli **Metoda** na stránce **Odpisové profily**, dlouhodobý majetek, který je přiřazen k tomuto odpisovému profilu, bude odpisován o stejný procentní podíl v každém období odpisu.</span><span class="sxs-lookup"><span data-stu-id="c755b-105">When you set up a fixed asset depreciation profile and select **175% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> 

<span data-ttu-id="c755b-106">Pokud chcete nastavit 175% degresivní odpisování, je nutné také vybrat možnosti v polích **Odpisový rok** a **Frekvence období** na stránce **Odpisové profily**.</span><span class="sxs-lookup"><span data-stu-id="c755b-106">To set up 175% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="c755b-107">Možnosti dostupné v poli **Frekvence období** se liší v závislosti na hodnotě vybrané v poli **Odpisový rok**.</span><span class="sxs-lookup"><span data-stu-id="c755b-107">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="c755b-108">Výběr odpisového roku</span><span class="sxs-lookup"><span data-stu-id="c755b-108">Select a depreciation year</span></span>
<span data-ttu-id="c755b-109">V poli **Odpisový rok** na stránce **Odpisové plány** můžete vybrat buď **Kalendářní** nebo **Fiskální**.</span><span class="sxs-lookup"><span data-stu-id="c755b-109">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="c755b-110">Výchozí hodnota je **Kalendářní**.</span><span class="sxs-lookup"><span data-stu-id="c755b-110">The default value is **Calendar**.</span></span> 

<span data-ttu-id="c755b-111">Vaše volba určí, jaké možnosti budou dostupné v poli **Frekvence období**.</span><span class="sxs-lookup"><span data-stu-id="c755b-111">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="c755b-112">Toto pole definuje časové rozdělení zaúčtování odpisů a částky v kalendářním roce.</span><span class="sxs-lookup"><span data-stu-id="c755b-112">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="c755b-113">Kalendář</span><span class="sxs-lookup"><span data-stu-id="c755b-113">Calendar</span></span>

<span data-ttu-id="c755b-114">V poli **Odpisový rok** můžete ponechat výchozí hodnotu **Kalendářní**.</span><span class="sxs-lookup"><span data-stu-id="c755b-114">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="c755b-115">Možnost **Kalendářní** aktualizuje odpisovou základnu 1. ledna každého roku.</span><span class="sxs-lookup"><span data-stu-id="c755b-115">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="c755b-116">Odpisová základna je obvykle zůstatková účetní hodnota mínus likvidační hodnota.</span><span class="sxs-lookup"><span data-stu-id="c755b-116">Typically, the depreciation base is the net book value minus the scrap value.</span></span> <span data-ttu-id="c755b-117">V níže uvedených příkladech této kapitoly je odpisová základna čitatelem v prvním výrazu ve výpočtech ve sloupci Kalkulace.</span><span class="sxs-lookup"><span data-stu-id="c755b-117">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="c755b-118">Vyberete-li jako odpisový rok možnost **Kalendář**, v poli **Frekvence období** jsou k dispozici následující možnosti:</span><span class="sxs-lookup"><span data-stu-id="c755b-118">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="c755b-119">Možnost **Ročně** provede zaúčtování 31. prosince.</span><span class="sxs-lookup"><span data-stu-id="c755b-119">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="c755b-120">**Měsíčně** provádí zaúčtování měsíčně na konci každého kalendářního měsíce.</span><span class="sxs-lookup"><span data-stu-id="c755b-120">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="c755b-121">**Čtvrtletně** provádí zaúčtování čtvrtletní částky na konci každého kalendářního čtvrtletí (31. března, 30. června, 30. září a 31. prosince).</span><span class="sxs-lookup"><span data-stu-id="c755b-121">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="c755b-122">**Pololetně** provádí zaúčtování pololetní částky na konci poloviny kalendářního roku (30. června a 31. prosince).</span><span class="sxs-lookup"><span data-stu-id="c755b-122">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="c755b-123">Položka **Denně** zaúčtuje částku odpisu pro metodu denních odpisů s použitím jedné transakce pro každý den.</span><span class="sxs-lookup"><span data-stu-id="c755b-123">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="c755b-124">Fiskální</span><span class="sxs-lookup"><span data-stu-id="c755b-124">Fiscal</span></span>

<span data-ttu-id="c755b-125">Vyberete-li možnost **Fiskální** v poli **Odpisový rok**, degresivní odpis 175 % je vypočten na základě fiskálního roku pro fiskální kalendář, který je určen pro knihu, nebo pro fiskální kalendář, který je vybrán na stránce **Hlavní kniha**.</span><span class="sxs-lookup"><span data-stu-id="c755b-125">If you select **Fiscal** in the **Depreciation year** field, 175% reducing balance depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="c755b-126">Fiskální kalendáře se nastavují na stránce **Fiskální kalendáře**.</span><span class="sxs-lookup"><span data-stu-id="c755b-126">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> <span data-ttu-id="c755b-127">Více informací získáte v tématu [Fiskální kalendáře, fiskální roky a období](../budgeting/fiscal-calendars-fiscal-years-periods.md).</span><span class="sxs-lookup"><span data-stu-id="c755b-127">For more information, see [Fiscal calendars, fiscal years, and periods](../budgeting/fiscal-calendars-fiscal-years-periods.md).</span></span>

<span data-ttu-id="c755b-128">Například pro fiskální rok od 1. července do 30. června začíná výpočet odpisů datem 1. července.</span><span class="sxs-lookup"><span data-stu-id="c755b-128">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="c755b-129">Fiskální rok může být delší nebo kratší než 12 měsíců.</span><span class="sxs-lookup"><span data-stu-id="c755b-129">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="c755b-130">Odpisování je automaticky upravováno pro jednotlivá období a délka dalšího fiskálního roku je určována dle nastavení období na stránce **Fiskální kalendáře**.</span><span class="sxs-lookup"><span data-stu-id="c755b-130">The depreciation is automatically adjusted for each period, and the length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="c755b-131">Vyberete-li jako odpisový rok možnost **Fiskální**, v poli **Frekvence období** jsou k dispozici následující možnosti:</span><span class="sxs-lookup"><span data-stu-id="c755b-131">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="c755b-132">**Ročně** - Zaúčtuje celkovou částku odpisu vypočteného pro fiskální rok poslední den fiskálního roku.</span><span class="sxs-lookup"><span data-stu-id="c755b-132">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="c755b-133">**Fiskální období** vypočte celkovou částku odpisu pro fiskální rok.</span><span class="sxs-lookup"><span data-stu-id="c755b-133">**Fiscal period** calculates the total amount of the depreciation for the fiscal year.</span></span> <span data-ttu-id="c755b-134">Tato částka se rozloží do fiskálních období, která jsou definována na stránce **Fiskální kalendáře**.</span><span class="sxs-lookup"><span data-stu-id="c755b-134">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-175-reducing-balance-depreciation"></a><span data-ttu-id="c755b-135">Příklad 175% degresivního odpisování</span><span class="sxs-lookup"><span data-stu-id="c755b-135">Example of 175% reducing balance depreciation</span></span>

| <span data-ttu-id="c755b-136">Pole</span><span class="sxs-lookup"><span data-stu-id="c755b-136">Field</span></span>                          | <span data-ttu-id="c755b-137">Hodnota</span><span class="sxs-lookup"><span data-stu-id="c755b-137">Value</span></span>  |
|--------------------------------|--------|
| <span data-ttu-id="c755b-138">Pořizovací náklady</span><span class="sxs-lookup"><span data-stu-id="c755b-138">Acquisition cost</span></span>               | <span data-ttu-id="c755b-139">11,000</span><span class="sxs-lookup"><span data-stu-id="c755b-139">11,000</span></span> |
| <span data-ttu-id="c755b-140">Zůstatková hodnota</span><span class="sxs-lookup"><span data-stu-id="c755b-140">Salvage value</span></span>                  | <span data-ttu-id="c755b-141">1 000</span><span class="sxs-lookup"><span data-stu-id="c755b-141">1,000</span></span>  |
| <span data-ttu-id="c755b-142">Odpisová základna</span><span class="sxs-lookup"><span data-stu-id="c755b-142">Depreciation base</span></span>              | <span data-ttu-id="c755b-143">10 000</span><span class="sxs-lookup"><span data-stu-id="c755b-143">10,000</span></span> |
| <span data-ttu-id="c755b-144">Roky životnosti</span><span class="sxs-lookup"><span data-stu-id="c755b-144">Service life years</span></span>             | <span data-ttu-id="c755b-145">5</span><span class="sxs-lookup"><span data-stu-id="c755b-145">5</span></span>      |
| <span data-ttu-id="c755b-146">Roční procentuální hodnota odpisu</span><span class="sxs-lookup"><span data-stu-id="c755b-146">Yearly depreciation percentage</span></span> | <span data-ttu-id="c755b-147">35 %</span><span class="sxs-lookup"><span data-stu-id="c755b-147">35%</span></span>    |

<span data-ttu-id="c755b-148">Metoda degresivního odepisování 175 % vydělí 175 procent počtem roků životnosti.</span><span class="sxs-lookup"><span data-stu-id="c755b-148">The 175% reducing balance depreciation method divides 175 percent by the service life years.</span></span> <span data-ttu-id="c755b-149">Procentuální hodnota se vynásobí čistou účetní hodnotou majetku, aby byla určena částka odpisu pro rok.</span><span class="sxs-lookup"><span data-stu-id="c755b-149">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="c755b-150">Období</span><span class="sxs-lookup"><span data-stu-id="c755b-150">Period</span></span> | <span data-ttu-id="c755b-151">Výpočet částky ročního odpisu</span><span class="sxs-lookup"><span data-stu-id="c755b-151">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="c755b-152">Účetní hodnota</span><span class="sxs-lookup"><span data-stu-id="c755b-152">Book value</span></span>                  | <span data-ttu-id="c755b-153">Čistá účetní hodnota na konci roku</span><span class="sxs-lookup"><span data-stu-id="c755b-153">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|-----------------------------|---------------------------------------|
| <span data-ttu-id="c755b-154">Rok 1</span><span class="sxs-lookup"><span data-stu-id="c755b-154">Year 1</span></span> | <span data-ttu-id="c755b-155">(11 000 – 1000) × 35 % = 3500</span><span class="sxs-lookup"><span data-stu-id="c755b-155">(11,000 – 1,000) × 35% = 3,500</span></span>                | <span data-ttu-id="c755b-156">11 000 – 3500 = 7500</span><span class="sxs-lookup"><span data-stu-id="c755b-156">11,000 – 3,500 = 7,500</span></span>      | <span data-ttu-id="c755b-157">11 000 – 1000 – 3500 = 6500</span><span class="sxs-lookup"><span data-stu-id="c755b-157">11,000 – 1,000 – 3,500 = 6,500</span></span>        |
| <span data-ttu-id="c755b-158">Rok 2</span><span class="sxs-lookup"><span data-stu-id="c755b-158">Year 2</span></span> | <span data-ttu-id="c755b-159">6500 × 35 % = 2275</span><span class="sxs-lookup"><span data-stu-id="c755b-159">6,500 × 35% = 2,275</span></span>                           | <span data-ttu-id="c755b-160">7500 – 2275 = 5225</span><span class="sxs-lookup"><span data-stu-id="c755b-160">7,500 – 2,275 = 5,225</span></span>       | <span data-ttu-id="c755b-161">6500 – 2275 = 4225</span><span class="sxs-lookup"><span data-stu-id="c755b-161">6,500 – 2,275 = 4,225</span></span>                 |
| <span data-ttu-id="c755b-162">Rok 3</span><span class="sxs-lookup"><span data-stu-id="c755b-162">Year 3</span></span> | <span data-ttu-id="c755b-163">4225 × 35 % = 1478,75</span><span class="sxs-lookup"><span data-stu-id="c755b-163">4,225 × 35% = 1,478.75</span></span>                        | <span data-ttu-id="c755b-164">5225 – 1478,75 = 3746,25</span><span class="sxs-lookup"><span data-stu-id="c755b-164">5,225 – 1,478.75 = 3,746.25</span></span> | <span data-ttu-id="c755b-165">4225 – 1478,75 = 2746,25</span><span class="sxs-lookup"><span data-stu-id="c755b-165">4,225 – 1,478.75 = 2,746.25</span></span>           |

> [!NOTE] 
> <span data-ttu-id="c755b-166">Když částka vypočtená s použitím metody 175% degresivního odpisování klesne pod hodnotu menší než má částka, která by byla vypočtena s použitím lineární metody, obvykle dojde k převodu na lineární metodu pro zbytek životnosti.</span><span class="sxs-lookup"><span data-stu-id="c755b-166">Typically, when the amount that is calculated by using the 175% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]