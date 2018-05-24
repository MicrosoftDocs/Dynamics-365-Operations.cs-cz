---
title: "Degresivní odpis 175 %"
description: "Toto téma poskytuje přehled metody degresivního odpisu 175 %."
author: saraschi2
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13911
ms.assetid: cc5d001f-bcfe-4602-9ec1-9e265e9fd188
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 8f78eb06930eab26d300fba6fd28333a5ce39cf8
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---

# <a name="175-percent-reducing-balance-depreciation"></a><span data-ttu-id="d2a8a-103">Degresivní odpis 175 %</span><span class="sxs-lookup"><span data-stu-id="d2a8a-103">175 percent reducing balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d2a8a-104">Toto téma poskytuje přehled metody degresivního odpisu 175 %.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-104">This topic gives an overview of the 175 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="d2a8a-105">Pokud nastavujete odpisový profil dlouhodobého majetku a zaškrtnete volbu **Degresivní 175 %** v poli **Metoda** na stránce **Odpisové profily**, dlouhodobý majetek, který je přiřazen k tomuto odpisovému profilu, bude odpisován o stejný procentní podíl v každém období odpisu.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-105">When you set up a fixed asset depreciation profile and select **175% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> 

<span data-ttu-id="d2a8a-106">Pokud chcete nastavit 175% degresivní odpisování, je nutné také vybrat možnosti v polích **Odpisový rok** a **Frekvence období** na stránce **Odpisové profily**.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-106">To set up 175% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="d2a8a-107">Možnosti dostupné v poli **Frekvence období** se liší v závislosti na hodnotě vybrané v poli **Odpisový rok**.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-107">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="d2a8a-108">Výběr odpisového roku</span><span class="sxs-lookup"><span data-stu-id="d2a8a-108">Select a depreciation year</span></span>
<span data-ttu-id="d2a8a-109">V poli **Odpisový rok** na stránce **Odpisové plány** můžete vybrat buď **Kalendářní** nebo **Fiskální**.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-109">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="d2a8a-110">Výchozí hodnota je **Kalendářní**.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-110">The default value is **Calendar**.</span></span> 

<span data-ttu-id="d2a8a-111">Vaše volba určí, jaké možnosti budou dostupné v poli **Frekvence období**.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-111">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="d2a8a-112">Toto pole definuje časové rozdělení zaúčtování odpisů a částky v kalendářním roce.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-112">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="d2a8a-113">Kalendář</span><span class="sxs-lookup"><span data-stu-id="d2a8a-113">Calendar</span></span>

<span data-ttu-id="d2a8a-114">V poli **Odpisový rok** můžete ponechat výchozí hodnotu **Kalendářní**.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-114">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="d2a8a-115">Možnost **Kalendářní** aktualizuje odpisovou základnu 1. ledna každého roku.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-115">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="d2a8a-116">Odpisová základna je obvykle zůstatková účetní hodnota mínus likvidační hodnota.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-116">Typically, the depreciation base is the net book value minus the scrap value.</span></span> <span data-ttu-id="d2a8a-117">V níže uvedených příkladech této kapitoly je odpisová základna čitatelem v prvním výrazu ve výpočtech ve sloupci Kalkulace.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-117">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="d2a8a-118">Vyberete-li jako odpisový rok možnost **Kalendář**, v poli **Frekvence období** jsou k dispozici následující možnosti:</span><span class="sxs-lookup"><span data-stu-id="d2a8a-118">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="d2a8a-119">Možnost **Ročně** provede zaúčtování 31. prosince.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-119">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="d2a8a-120">**Měsíčně** provádí zaúčtování měsíčně na konci každého kalendářního měsíce.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-120">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="d2a8a-121">**Čtvrtletně** provádí zaúčtování čtvrtletní částky na konci každého kalendářního čtvrtletí (31. března, 30. června, 30. září a 31. prosince).</span><span class="sxs-lookup"><span data-stu-id="d2a8a-121">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="d2a8a-122">**Pololetně** provádí zaúčtování pololetní částky na konci poloviny kalendářního roku (30. června a 31. prosince).</span><span class="sxs-lookup"><span data-stu-id="d2a8a-122">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="d2a8a-123">Položka **Denně** zaúčtuje částku odpisu pro metodu denních odpisů s použitím jedné transakce pro každý den.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-123">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="d2a8a-124">Fiskální</span><span class="sxs-lookup"><span data-stu-id="d2a8a-124">Fiscal</span></span>

<span data-ttu-id="d2a8a-125">Vyberete-li možnost **Fiskální** v poli **Odpisový rok**, degresivní odpis 175 % je vypočten na základě fiskálního roku pro fiskální kalendář, který je určen pro knihu, nebo pro fiskální kalendář, který je vybrán na stránce **Hlavní kniha**.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-125">If you select **Fiscal** in the **Depreciation year** field, 175% reducing balance depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="d2a8a-126">Fiskální kalendáře se nastavují na stránce **Fiskální kalendáře**.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-126">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> <span data-ttu-id="d2a8a-127">Více informací získáte v tématu [Fiskální kalendáře, fiskální roky a období](../budgeting/fiscal-calendars-fiscal-years-periods.md).</span><span class="sxs-lookup"><span data-stu-id="d2a8a-127">For more information, see [Fiscal calendars, fiscal years, and periods](../budgeting/fiscal-calendars-fiscal-years-periods.md).</span></span>

<span data-ttu-id="d2a8a-128">Například pro fiskální rok od 1. července do 30. června začíná výpočet odpisů datem 1. července.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-128">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="d2a8a-129">Fiskální rok může být delší nebo kratší než 12 měsíců.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-129">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="d2a8a-130">Odpisování je automaticky upravováno pro jednotlivá období a délka dalšího fiskálního roku je určována dle nastavení období na stránce **Fiskální kalendáře**.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-130">The depreciation is automatically adjusted for each period, and the length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="d2a8a-131">Vyberete-li jako odpisový rok možnost **Fiskální**, v poli **Frekvence období** jsou k dispozici následující možnosti:</span><span class="sxs-lookup"><span data-stu-id="d2a8a-131">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="d2a8a-132">**Ročně** - Zaúčtuje celkovou částku odpisu vypočteného pro fiskální rok poslední den fiskálního roku.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-132">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="d2a8a-133">**Fiskální období** vypočte celkovou částku odpisu pro fiskální rok.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-133">**Fiscal period** calculates the total amount of the depreciation for the fiscal year.</span></span> <span data-ttu-id="d2a8a-134">Tato částka se rozloží do fiskálních období, která jsou definována na stránce **Fiskální kalendáře**.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-134">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-175-reducing-balance-depreciation"></a><span data-ttu-id="d2a8a-135">Příklad 175% degresivního odpisování</span><span class="sxs-lookup"><span data-stu-id="d2a8a-135">Example of 175% reducing balance depreciation</span></span>

|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="d2a8a-136">Pořizovací náklady</span><span class="sxs-lookup"><span data-stu-id="d2a8a-136">Acquisition cost</span></span>               | <span data-ttu-id="d2a8a-137">11 000</span><span class="sxs-lookup"><span data-stu-id="d2a8a-137">11,000</span></span> |
| <span data-ttu-id="d2a8a-138">Zůstatková hodnota</span><span class="sxs-lookup"><span data-stu-id="d2a8a-138">Salvage value</span></span>                  | <span data-ttu-id="d2a8a-139">1 000</span><span class="sxs-lookup"><span data-stu-id="d2a8a-139">1,000</span></span>  |
| <span data-ttu-id="d2a8a-140">Odpisová základna</span><span class="sxs-lookup"><span data-stu-id="d2a8a-140">Depreciation base</span></span>              | <span data-ttu-id="d2a8a-141">10 000</span><span class="sxs-lookup"><span data-stu-id="d2a8a-141">10,000</span></span> |
| <span data-ttu-id="d2a8a-142">Roky životnosti</span><span class="sxs-lookup"><span data-stu-id="d2a8a-142">Service life years</span></span>             | <span data-ttu-id="d2a8a-143">5</span><span class="sxs-lookup"><span data-stu-id="d2a8a-143">5</span></span>      |
| <span data-ttu-id="d2a8a-144">Roční procentuální hodnota odpisu</span><span class="sxs-lookup"><span data-stu-id="d2a8a-144">Yearly depreciation percentage</span></span> | <span data-ttu-id="d2a8a-145">35 %</span><span class="sxs-lookup"><span data-stu-id="d2a8a-145">35%</span></span>    |

<span data-ttu-id="d2a8a-146">Metoda degresivního odepisování 175 % vydělí 175 procent počtem roků životnosti.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-146">The 175% reducing balance depreciation method divides 175 percent by the service life years.</span></span> <span data-ttu-id="d2a8a-147">Procentuální hodnota se vynásobí čistou účetní hodnotou majetku, aby byla určena částka odpisu pro rok.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-147">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="d2a8a-148">Období</span><span class="sxs-lookup"><span data-stu-id="d2a8a-148">Period</span></span> | <span data-ttu-id="d2a8a-149">Výpočet částky ročního odpisu</span><span class="sxs-lookup"><span data-stu-id="d2a8a-149">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="d2a8a-150">Účetní hodnota</span><span class="sxs-lookup"><span data-stu-id="d2a8a-150">Book value</span></span>                  | <span data-ttu-id="d2a8a-151">Čistá účetní hodnota na konci roku</span><span class="sxs-lookup"><span data-stu-id="d2a8a-151">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|-----------------------------|---------------------------------------|
| <span data-ttu-id="d2a8a-152">Rok 1</span><span class="sxs-lookup"><span data-stu-id="d2a8a-152">Year 1</span></span> | <span data-ttu-id="d2a8a-153">(11 000 – 1 000) × 35 % = 3 500</span><span class="sxs-lookup"><span data-stu-id="d2a8a-153">(11,000 – 1,000) × 35% = 3,500</span></span>                | <span data-ttu-id="d2a8a-154">11 000 – 3 500 = 7 500</span><span class="sxs-lookup"><span data-stu-id="d2a8a-154">11,000 – 3,500 = 7,500</span></span>      | <span data-ttu-id="d2a8a-155">11 000 – 1 000 – 3 500 = 6 500</span><span class="sxs-lookup"><span data-stu-id="d2a8a-155">11,000 – 1,000 – 3,500 = 6,500</span></span>        |
| <span data-ttu-id="d2a8a-156">Rok 2</span><span class="sxs-lookup"><span data-stu-id="d2a8a-156">Year 2</span></span> | <span data-ttu-id="d2a8a-157">6 500 × 35 % = 2 275</span><span class="sxs-lookup"><span data-stu-id="d2a8a-157">6,500 × 35% = 2,275</span></span>                           | <span data-ttu-id="d2a8a-158">7 500 – 2 275 = 5 225</span><span class="sxs-lookup"><span data-stu-id="d2a8a-158">7,500 – 2,275 = 5,225</span></span>       | <span data-ttu-id="d2a8a-159">6 500 – 2 275 = 4 225</span><span class="sxs-lookup"><span data-stu-id="d2a8a-159">6,500 – 2,275 = 4,225</span></span>                 |
| <span data-ttu-id="d2a8a-160">Rok 3</span><span class="sxs-lookup"><span data-stu-id="d2a8a-160">Year 3</span></span> | <span data-ttu-id="d2a8a-161">4 225 × 35 % = 1 478,75</span><span class="sxs-lookup"><span data-stu-id="d2a8a-161">4,225 × 35% = 1,478.75</span></span>                        | <span data-ttu-id="d2a8a-162">5 225 – 1 478,75 = 3 746,25</span><span class="sxs-lookup"><span data-stu-id="d2a8a-162">5,225 – 1,478.75 = 3,746.25</span></span> | <span data-ttu-id="d2a8a-163">4 225 – 1 478,75 = 2 746,25</span><span class="sxs-lookup"><span data-stu-id="d2a8a-163">4,225 – 1,478.75 = 2,746.25</span></span>           |

> [!NOTE] 
> <span data-ttu-id="d2a8a-164">Když částka vypočtená s použitím metody 175% degresivního odpisování klesne pod hodnotu menší než má částka, která by byla vypočtena s použitím lineární metody, obvykle dojde k převodu na lineární metodu pro zbytek životnosti.</span><span class="sxs-lookup"><span data-stu-id="d2a8a-164">Typically, when the amount that is calculated by using the 175% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>




