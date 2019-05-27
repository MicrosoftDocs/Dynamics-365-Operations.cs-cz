---
title: Degresivní odpis 200 procent
description: Tento článek poskytuje přehled o metodě odpisu „degresivní odpis 200 procent“.
author: saraschi2
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13951
ms.assetid: 69b4e010-7683-4dc2-8a06-6d572f37e903
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ec51f9e12e31e81c56fab9e82d0fc18d45beb5e6
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569306"
---
# <a name="200-percent-reducing-balance-depreciation"></a><span data-ttu-id="e52fd-103">Degresivní odpis 200 procent</span><span class="sxs-lookup"><span data-stu-id="e52fd-103">200 percent reducing balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e52fd-104">Tento článek poskytuje přehled o metodě odpisu „degresivní odpis 200 procent“.</span><span class="sxs-lookup"><span data-stu-id="e52fd-104">This article gives an overview of the 200 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="e52fd-105">Pokud nastavujete odpisový profil dlouhodobého majetku a zaškrtnete volbu **Degresivní 200 %** v poli **Metoda** na stránce **Odpisové profily**, dlouhodobý majetek, který je přiřazen k tomuto odpisovému profilu, bude odpisován o stejný procentní podíl v každém období odpisu.</span><span class="sxs-lookup"><span data-stu-id="e52fd-105">When you set up a fixed asset depreciation profile and select **200% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> <span data-ttu-id="e52fd-106">Procentuální hodnota se vypočte na základě životnosti majetku.</span><span class="sxs-lookup"><span data-stu-id="e52fd-106">The percentage is calculated based on the service life of the asset.</span></span> <span data-ttu-id="e52fd-107">Když má například majetek životnost pět let, procentuální hodnota se vypočte jako 40 procent (200 % ÷ 5).</span><span class="sxs-lookup"><span data-stu-id="e52fd-107">For example, if an asset has a service life of five years, the percentage is calculated as 40 percent (200% ÷ 5).</span></span> 

<span data-ttu-id="e52fd-108">Tato metoda je také známá jako klesající dvojitý zůstatek.</span><span class="sxs-lookup"><span data-stu-id="e52fd-108">This method is also known as double declining balance.</span></span>

<span data-ttu-id="e52fd-109">Pokud chcete nastavit 200% degresivní odpisování, je nutné také vybrat možnosti v polích **Odpisový rok** a **Frekvence období** na stránce **Odpisové profily**.</span><span class="sxs-lookup"><span data-stu-id="e52fd-109">To set up 200% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="e52fd-110">Možnosti dostupné v poli **Frekvence období** se liší v závislosti na hodnotě vybrané v poli **Odpisový rok**.</span><span class="sxs-lookup"><span data-stu-id="e52fd-110">The options that are available in the **Period frequency** field vary, depending on the value that you select in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="e52fd-111">Výběr odpisového roku</span><span class="sxs-lookup"><span data-stu-id="e52fd-111">Select a depreciation year</span></span>
<span data-ttu-id="e52fd-112">V poli **Odpisový rok** na stránce **Odpisové plány** můžete vybrat buď **Kalendářní** nebo **Fiskální**.</span><span class="sxs-lookup"><span data-stu-id="e52fd-112">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="e52fd-113">Výchozí hodnota je **Kalendářní**.</span><span class="sxs-lookup"><span data-stu-id="e52fd-113">The default value is **Calendar**.</span></span> 

<span data-ttu-id="e52fd-114">Vaše volba určí, jaké možnosti budou dostupné v poli **Frekvence období**.</span><span class="sxs-lookup"><span data-stu-id="e52fd-114">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="e52fd-115">Toto pole definuje časové rozdělení zaúčtování odpisů a částky v kalendářním roce.</span><span class="sxs-lookup"><span data-stu-id="e52fd-115">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="e52fd-116">Kalendář</span><span class="sxs-lookup"><span data-stu-id="e52fd-116">Calendar</span></span>

<span data-ttu-id="e52fd-117">V poli **Odpisový rok** můžete ponechat výchozí hodnotu **Kalendářní**.</span><span class="sxs-lookup"><span data-stu-id="e52fd-117">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="e52fd-118">Možnost **Kalendářní** aktualizuje odpisovou základnu 1. ledna každého roku.</span><span class="sxs-lookup"><span data-stu-id="e52fd-118">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="e52fd-119">Odpis obvykle zůstatková účetní hodnota mínus likvidační hodnota.</span><span class="sxs-lookup"><span data-stu-id="e52fd-119">Typically, the depreciation is the net book value minus the scrap value.</span></span> <span data-ttu-id="e52fd-120">V níže uvedených příkladech této kapitoly je odpisová základna čitatelem v prvním výrazu ve výpočtech ve sloupci Kalkulace.</span><span class="sxs-lookup"><span data-stu-id="e52fd-120">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="e52fd-121">Vyberete-li jako odpisový rok možnost **Kalendář**, v poli **Frekvence období** jsou k dispozici následující možnosti:</span><span class="sxs-lookup"><span data-stu-id="e52fd-121">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="e52fd-122">Možnost **Ročně** provede zaúčtování 31. prosince.</span><span class="sxs-lookup"><span data-stu-id="e52fd-122">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="e52fd-123">**Měsíčně** provádí zaúčtování měsíčně na konci každého kalendářního měsíce.</span><span class="sxs-lookup"><span data-stu-id="e52fd-123">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="e52fd-124">**Čtvrtletně** provádí zaúčtování čtvrtletní částky na konci každého kalendářního čtvrtletí (31. března, 30. června, 30. září a 31. prosince).</span><span class="sxs-lookup"><span data-stu-id="e52fd-124">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="e52fd-125">**Pololetně** provádí zaúčtování pololetní částky na konci poloviny kalendářního roku (30. června a 31. prosince).</span><span class="sxs-lookup"><span data-stu-id="e52fd-125">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="e52fd-126">Položka **Denně** zaúčtuje částku odpisu pro metodu denních odpisů s použitím jedné transakce pro každý den.</span><span class="sxs-lookup"><span data-stu-id="e52fd-126">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="e52fd-127">Fiskální</span><span class="sxs-lookup"><span data-stu-id="e52fd-127">Fiscal</span></span>

<span data-ttu-id="e52fd-128">Vyberete-li možnost **Fiskální** v poli **Odpisový rok**, degresivní odpis 200 % je vypočten na základě fiskálního roku pro fiskální kalendář, který je určen pro knihu, nebo pro fiskální kalendář, který je vybrán na stránce **Hlavní kniha**.</span><span class="sxs-lookup"><span data-stu-id="e52fd-128">If you select **Fiscal** in the **Depreciation** year field, 200% reducing balance depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="e52fd-129">Fiskální kalendáře se nastavují na stránce **Fiskální kalendáře**.</span><span class="sxs-lookup"><span data-stu-id="e52fd-129">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="e52fd-130">Například pro fiskální rok od 1. července do 30. června začíná výpočet odpisů datem 1. července.</span><span class="sxs-lookup"><span data-stu-id="e52fd-130">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="e52fd-131">Fiskální rok může být delší nebo kratší než 12 měsíců.</span><span class="sxs-lookup"><span data-stu-id="e52fd-131">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="e52fd-132">Odpisy se upravují pro jednotlivá období.</span><span class="sxs-lookup"><span data-stu-id="e52fd-132">The depreciation is adjusted for each period.</span></span> <span data-ttu-id="e52fd-133">Délka dalšího fiskálního roku záleží na nastavení období na stránce **Fiskální kalendáře**.</span><span class="sxs-lookup"><span data-stu-id="e52fd-133">The length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="e52fd-134">Vyberete-li jako odpisový rok možnost **Fiskální**, v poli **Frekvence období** jsou k dispozici následující možnosti:</span><span class="sxs-lookup"><span data-stu-id="e52fd-134">When **Fiscal** is selected as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="e52fd-135">Možnost **Ročně** zaúčtuje celkovou částku odpisu vypočteného pro fiskální rok jako jednu částku poslední den fiskálního roku.</span><span class="sxs-lookup"><span data-stu-id="e52fd-135">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year as one amount, on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="e52fd-136">**Fiskální období** zaúčtuje celkovou částku odpisu vypočteného pro fiskální rok.</span><span class="sxs-lookup"><span data-stu-id="e52fd-136">**Fiscal period** posts the total amount of the depreciation that is calculated for the fiscal year.</span></span> <span data-ttu-id="e52fd-137">Tato částka se rozloží do fiskálních období, která jsou definována na stránce **Fiskální kalendáře**.</span><span class="sxs-lookup"><span data-stu-id="e52fd-137">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-200-reducing-balance-depreciation"></a><span data-ttu-id="e52fd-138">Příklad 200% degresivního odpisování</span><span class="sxs-lookup"><span data-stu-id="e52fd-138">Example of 200% reducing balance depreciation</span></span>

|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="e52fd-139">Pořizovací náklady</span><span class="sxs-lookup"><span data-stu-id="e52fd-139">Acquisition cost</span></span>               | <span data-ttu-id="e52fd-140">11 000</span><span class="sxs-lookup"><span data-stu-id="e52fd-140">11,000</span></span> |
| <span data-ttu-id="e52fd-141">Zůstatková hodnota</span><span class="sxs-lookup"><span data-stu-id="e52fd-141">Salvage value</span></span>                  | <span data-ttu-id="e52fd-142">1 000</span><span class="sxs-lookup"><span data-stu-id="e52fd-142">1, 000</span></span> |
| <span data-ttu-id="e52fd-143">Odpisová základna</span><span class="sxs-lookup"><span data-stu-id="e52fd-143">Depreciation base</span></span>              | <span data-ttu-id="e52fd-144">10 000</span><span class="sxs-lookup"><span data-stu-id="e52fd-144">10,000</span></span> |
| <span data-ttu-id="e52fd-145">Roky životnosti</span><span class="sxs-lookup"><span data-stu-id="e52fd-145">Service life years</span></span>             | <span data-ttu-id="e52fd-146">5</span><span class="sxs-lookup"><span data-stu-id="e52fd-146">5</span></span>      |
| <span data-ttu-id="e52fd-147">Roční procentuální hodnota odpisu</span><span class="sxs-lookup"><span data-stu-id="e52fd-147">Yearly depreciation percentage</span></span> | <span data-ttu-id="e52fd-148">40 %</span><span class="sxs-lookup"><span data-stu-id="e52fd-148">40%</span></span>    |

<span data-ttu-id="e52fd-149">Metoda degresivního odepisování 200 % vydělí 200 procent počtem roků životnosti.</span><span class="sxs-lookup"><span data-stu-id="e52fd-149">The 200% reducing balance method divides 200 percent by the service life years.</span></span> <span data-ttu-id="e52fd-150">Procentuální hodnota se vynásobí čistou účetní hodnotou majetku, aby byla určena částka odpisu pro rok.</span><span class="sxs-lookup"><span data-stu-id="e52fd-150">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="e52fd-151">Období</span><span class="sxs-lookup"><span data-stu-id="e52fd-151">Period</span></span> | <span data-ttu-id="e52fd-152">Výpočet částky ročního odpisu</span><span class="sxs-lookup"><span data-stu-id="e52fd-152">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="e52fd-153">Účetní hodnota</span><span class="sxs-lookup"><span data-stu-id="e52fd-153">Book value</span></span>             | <span data-ttu-id="e52fd-154">Čistá účetní hodnota na konci roku</span><span class="sxs-lookup"><span data-stu-id="e52fd-154">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| <span data-ttu-id="e52fd-155">Rok 1</span><span class="sxs-lookup"><span data-stu-id="e52fd-155">Year 1</span></span> | <span data-ttu-id="e52fd-156">(11 000 – 1 000) × 40% = 4 000</span><span class="sxs-lookup"><span data-stu-id="e52fd-156">(11,000 – 1,000) × 40% = 4,000</span></span>                | <span data-ttu-id="e52fd-157">11 000 – 4 000 = 7 000</span><span class="sxs-lookup"><span data-stu-id="e52fd-157">11,000 – 4,000 = 7,000</span></span> | <span data-ttu-id="e52fd-158">11 000 – 1 000 – 4 000 = 6 000</span><span class="sxs-lookup"><span data-stu-id="e52fd-158">11,000 – 1,000 – 4,000 = 6,000</span></span>        |
| <span data-ttu-id="e52fd-159">Rok 2</span><span class="sxs-lookup"><span data-stu-id="e52fd-159">Year 2</span></span> | <span data-ttu-id="e52fd-160">6 000 × 40% = 2 400</span><span class="sxs-lookup"><span data-stu-id="e52fd-160">6,000 × 40% = 2,400</span></span>                           | <span data-ttu-id="e52fd-161">7 000 – 2 400 = 4 600</span><span class="sxs-lookup"><span data-stu-id="e52fd-161">7,000 – 2,400 = 4,600</span></span>  | <span data-ttu-id="e52fd-162">6 000 – 2 400 = 3 600</span><span class="sxs-lookup"><span data-stu-id="e52fd-162">6,000 – 2,400 = 3,600</span></span>                 |
| <span data-ttu-id="e52fd-163">Rok 3</span><span class="sxs-lookup"><span data-stu-id="e52fd-163">Year 3</span></span> | <span data-ttu-id="e52fd-164">3 600 × 40% = 1 440</span><span class="sxs-lookup"><span data-stu-id="e52fd-164">3,600 × 40% = 1,440</span></span>                           | <span data-ttu-id="e52fd-165">4 600 – 1 440 = 3 160</span><span class="sxs-lookup"><span data-stu-id="e52fd-165">4,600 – 1,440 = 3,160</span></span>  | <span data-ttu-id="e52fd-166">3 600 – 1 440 = 2 160</span><span class="sxs-lookup"><span data-stu-id="e52fd-166">3,600 – 1,440 = 2,160</span></span>                 |

> [!NOTE] 
> <span data-ttu-id="e52fd-167">Když částka vypočtená s použitím metody 200% degresivního odpisování klesne pod hodnotu menší než má částka, která by byla vypočtena s použitím lineární metody, obvykle dojde k převodu na lineární metodu pro zbytek životnosti.</span><span class="sxs-lookup"><span data-stu-id="e52fd-167">Typically, when the amount that is calculated by using the 200% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>



