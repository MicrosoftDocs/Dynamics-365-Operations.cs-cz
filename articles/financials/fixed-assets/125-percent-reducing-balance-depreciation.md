---
title: Degresivní odpis 125 procent
description: Tento článek poskytuje přehled o metodě odpisu „degresivní odpis 125 procent“.
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
ms.custom: 13871
ms.assetid: 3abc263e-59d6-4f1a-986d-1be388948bd3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f7af5413376a98c3b2b7ded46c757c9156a3fadf
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555689"
---
# <a name="125-percent-reducing-balance-depreciation"></a><span data-ttu-id="5d67e-103">Degresivní odpis 125 procent</span><span class="sxs-lookup"><span data-stu-id="5d67e-103">125 percent reducing balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5d67e-104">Tento článek poskytuje přehled o metodě odpisu „degresivní odpis 125 procent“.</span><span class="sxs-lookup"><span data-stu-id="5d67e-104">This article gives an overview of the 125 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="5d67e-105">Pokud nastavujete odpisový profil dlouhodobého majetku a zaškrtnete volbu **Degresivní 125 %** v poli **Metoda** na stránce **Odpisové profily**, dlouhodobý majetek, který je přiřazen k tomuto odpisovému profilu, bude odpisován o stejný procentní podíl v každém období odpisu.</span><span class="sxs-lookup"><span data-stu-id="5d67e-105">When you set up a fixed asset depreciation profile and select **125% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned to the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> <span data-ttu-id="5d67e-106">Tato procentuální hodnota se vypočte na základě životnosti majetku.</span><span class="sxs-lookup"><span data-stu-id="5d67e-106">This percentage is calculated based on the service life of the asset.</span></span> <span data-ttu-id="5d67e-107">Když má například majetek životnost pět let, procentuální hodnota se vypočte jako 25 procent (125 % ÷ 5).</span><span class="sxs-lookup"><span data-stu-id="5d67e-107">For example, if an asset has a service life of five years, the percentage is calculated as 25 percent (125% ÷ 5).</span></span>

<span data-ttu-id="5d67e-108">Pokud chcete nastavit 125% degresivní odpisování, je nutné také vybrat možnosti v polích **Odpisový rok** a **Frekvence období** na stránce **Odpisové profily**.</span><span class="sxs-lookup"><span data-stu-id="5d67e-108">To set up 125% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="5d67e-109">Možnosti dostupné v poli **Frekvence období** se liší v závislosti na hodnotě vybrané v poli **Odpisový rok**.</span><span class="sxs-lookup"><span data-stu-id="5d67e-109">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="5d67e-110">Výběr odpisového roku</span><span class="sxs-lookup"><span data-stu-id="5d67e-110">Select a depreciation year</span></span>
<span data-ttu-id="5d67e-111">V poli **Odpisový rok** na stránce **Odpisové plány** můžete vybrat buď **Kalendářní** nebo **Fiskální**.</span><span class="sxs-lookup"><span data-stu-id="5d67e-111">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="5d67e-112">Výchozí hodnota je **Kalendářní**.</span><span class="sxs-lookup"><span data-stu-id="5d67e-112">The default value is **Calendar**.</span></span> 

<span data-ttu-id="5d67e-113">Vaše volba určí, jaké možnosti budou dostupné v poli **Frekvence období**.</span><span class="sxs-lookup"><span data-stu-id="5d67e-113">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="5d67e-114">Toto pole definuje časové rozdělení zaúčtování odpisů a částky v kalendářním roce.</span><span class="sxs-lookup"><span data-stu-id="5d67e-114">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="5d67e-115">Kalendář</span><span class="sxs-lookup"><span data-stu-id="5d67e-115">Calendar</span></span>

<span data-ttu-id="5d67e-116">V poli **Odpisový rok** můžete ponechat výchozí hodnotu **Kalendářní**.</span><span class="sxs-lookup"><span data-stu-id="5d67e-116">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="5d67e-117">Možnost **Kalendářní** aktualizuje odpisovou základnu 1. ledna každého roku.</span><span class="sxs-lookup"><span data-stu-id="5d67e-117">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="5d67e-118">Odpisová základna je obvykle zůstatková účetní hodnota mínus likvidační hodnota.</span><span class="sxs-lookup"><span data-stu-id="5d67e-118">Typically, the depreciation base is the net book value minus the scrap value.</span></span> <span data-ttu-id="5d67e-119">V níže uvedených příkladech této kapitoly je odpisová základna čitatelem v prvním výrazu ve výpočtech ve sloupci Kalkulace.</span><span class="sxs-lookup"><span data-stu-id="5d67e-119">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="5d67e-120">Vyberete-li jako odpisový rok možnost **Kalendář**, v poli **Frekvence období** jsou k dispozici následující možnosti:</span><span class="sxs-lookup"><span data-stu-id="5d67e-120">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="5d67e-121">Možnost **Ročně** provede zaúčtování 31. prosince.</span><span class="sxs-lookup"><span data-stu-id="5d67e-121">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="5d67e-122">**Měsíčně** provádí zaúčtování měsíčně na konci každého kalendářního měsíce.</span><span class="sxs-lookup"><span data-stu-id="5d67e-122">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="5d67e-123">**Čtvrtletně** provádí zaúčtování čtvrtletní částky na konci každého kalendářního čtvrtletí (31. března, 30. června, 30. září a 31. prosince).</span><span class="sxs-lookup"><span data-stu-id="5d67e-123">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="5d67e-124">**Pololetně** provádí zaúčtování pololetní částky na konci poloviny kalendářního roku (30. června a 31. prosince).</span><span class="sxs-lookup"><span data-stu-id="5d67e-124">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="5d67e-125">Položka **Denně** zaúčtuje částku odpisu pro metodu denních odpisů s použitím jedné transakce pro každý den.</span><span class="sxs-lookup"><span data-stu-id="5d67e-125">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="5d67e-126">Fiskální</span><span class="sxs-lookup"><span data-stu-id="5d67e-126">Fiscal</span></span>

<span data-ttu-id="5d67e-127">Vyberete-li možnost **Fiskální** v poli **Odpisový rok**, degresivní odpis 125 % je vypočten na základě fiskálního roku pro fiskální kalendář, který je určen pro knihu, nebo pro fiskální kalendář, který je vybrán na stránce **Hlavní kniha**.</span><span class="sxs-lookup"><span data-stu-id="5d67e-127">If you select **Fiscal** in the **Depreciation year** field, 125% reducing depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="5d67e-128">Fiskální kalendáře se nastavují na stránce **Fiskální kalendáře**.</span><span class="sxs-lookup"><span data-stu-id="5d67e-128">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="5d67e-129">Například pro fiskální rok od 1. července do 30. června začíná výpočet odpisů datem 1. července.</span><span class="sxs-lookup"><span data-stu-id="5d67e-129">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="5d67e-130">Fiskální rok může být delší nebo kratší než 12 měsíců.</span><span class="sxs-lookup"><span data-stu-id="5d67e-130">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="5d67e-131">Odpisování je automaticky upravováno pro jednotlivá období a délka dalšího fiskálního roku je určována dle nastavení období na stránce **Fiskální kalendáře**.</span><span class="sxs-lookup"><span data-stu-id="5d67e-131">The depreciation is automatically adjusted for each period, and the length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="5d67e-132">Vyberete-li jako odpisový rok možnost **Fiskální**, v poli **Frekvence období** jsou k dispozici následující možnosti:</span><span class="sxs-lookup"><span data-stu-id="5d67e-132">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="5d67e-133">Možnost **Ročně** zaúčtuje celkovou částku odpisu vypočteného pro fiskální rok jako jednu částku poslední den fiskálního roku.</span><span class="sxs-lookup"><span data-stu-id="5d67e-133">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year as one amount, on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="5d67e-134">**Fiskální období** zaúčtuje celkovou částku odpisu vypočteného pro fiskální rok.</span><span class="sxs-lookup"><span data-stu-id="5d67e-134">**Fiscal period** posts the total amount of the depreciation that is calculated for the fiscal year.</span></span> <span data-ttu-id="5d67e-135">Tato částka se rozloží do fiskálních období, která jsou definována na stránce **Fiskální kalendáře**.</span><span class="sxs-lookup"><span data-stu-id="5d67e-135">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-125-reducing-balance-depreciation"></a><span data-ttu-id="5d67e-136">Příklad 125% degresivního odpisování</span><span class="sxs-lookup"><span data-stu-id="5d67e-136">Example of 125% reducing balance depreciation</span></span>

|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="5d67e-137">Pořizovací náklady</span><span class="sxs-lookup"><span data-stu-id="5d67e-137">Acquisition cost</span></span>               | <span data-ttu-id="5d67e-138">11 000</span><span class="sxs-lookup"><span data-stu-id="5d67e-138">11,000</span></span> |
| <span data-ttu-id="5d67e-139">Zůstatková hodnota</span><span class="sxs-lookup"><span data-stu-id="5d67e-139">Salvage value</span></span>                  | <span data-ttu-id="5d67e-140">1 000</span><span class="sxs-lookup"><span data-stu-id="5d67e-140">1,000</span></span>  |
| <span data-ttu-id="5d67e-141">Odpisová základna</span><span class="sxs-lookup"><span data-stu-id="5d67e-141">Depreciation base</span></span>              | <span data-ttu-id="5d67e-142">10 000</span><span class="sxs-lookup"><span data-stu-id="5d67e-142">10,000</span></span> |
| <span data-ttu-id="5d67e-143">Roky životnosti</span><span class="sxs-lookup"><span data-stu-id="5d67e-143">Service life years</span></span>             | <span data-ttu-id="5d67e-144">5</span><span class="sxs-lookup"><span data-stu-id="5d67e-144">5</span></span>      |
| <span data-ttu-id="5d67e-145">Roční procentuální hodnota odpisu</span><span class="sxs-lookup"><span data-stu-id="5d67e-145">Yearly depreciation percentage</span></span> | <span data-ttu-id="5d67e-146">25 %</span><span class="sxs-lookup"><span data-stu-id="5d67e-146">25%</span></span>    |

<span data-ttu-id="5d67e-147">Metoda degresivního odepisování 125 % vydělí 125 procent počtem roků životnosti.</span><span class="sxs-lookup"><span data-stu-id="5d67e-147">The 125% reducing balance method divides 125 percent by the service life years.</span></span> <span data-ttu-id="5d67e-148">Procentuální hodnota se vynásobí čistou účetní hodnotou majetku, aby byla určena částka odpisu pro rok.</span><span class="sxs-lookup"><span data-stu-id="5d67e-148">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="5d67e-149">Období</span><span class="sxs-lookup"><span data-stu-id="5d67e-149">Period</span></span> | <span data-ttu-id="5d67e-150">Výpočet částky ročního odpisu</span><span class="sxs-lookup"><span data-stu-id="5d67e-150">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="5d67e-151">Účetní hodnota</span><span class="sxs-lookup"><span data-stu-id="5d67e-151">Book value</span></span>                    | <span data-ttu-id="5d67e-152">Čistá účetní hodnota na konci roku</span><span class="sxs-lookup"><span data-stu-id="5d67e-152">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|-------------------------------|---------------------------------------|
| <span data-ttu-id="5d67e-153">Rok 1</span><span class="sxs-lookup"><span data-stu-id="5d67e-153">Year 1</span></span> | <span data-ttu-id="5d67e-154">(11 000 – 1 000) × 25 % = 2 500</span><span class="sxs-lookup"><span data-stu-id="5d67e-154">(11,000 – 1,000) × 25% = 2,500</span></span>                | <span data-ttu-id="5d67e-155">(11 000 – 2 500) = 8 500</span><span class="sxs-lookup"><span data-stu-id="5d67e-155">(11,000 – 2,500) = 8,500</span></span>      | <span data-ttu-id="5d67e-156">(11 000 – 1 000 – 2 500) = 7 500</span><span class="sxs-lookup"><span data-stu-id="5d67e-156">(11,000 – 1,000 – 2,500) = 7,500</span></span>      |
| <span data-ttu-id="5d67e-157">Rok 2</span><span class="sxs-lookup"><span data-stu-id="5d67e-157">Year 2</span></span> | <span data-ttu-id="5d67e-158">7 500 × 25 % = 1 875</span><span class="sxs-lookup"><span data-stu-id="5d67e-158">7,500 × 25% = 1,875</span></span>                           | <span data-ttu-id="5d67e-159">(8 500 – 1 875) = 6 625</span><span class="sxs-lookup"><span data-stu-id="5d67e-159">(8,500 – 1,875) = 6,625</span></span>       | <span data-ttu-id="5d67e-160">(7 500 – 1 875) = 5 625</span><span class="sxs-lookup"><span data-stu-id="5d67e-160">(7,500 – 1,875) = 5,625</span></span>               |
| <span data-ttu-id="5d67e-161">Rok 3</span><span class="sxs-lookup"><span data-stu-id="5d67e-161">Year 3</span></span> | <span data-ttu-id="5d67e-162">5 625 × 25 % = 1 406,25</span><span class="sxs-lookup"><span data-stu-id="5d67e-162">5,625 × 25% = 1,406.25</span></span>                        | <span data-ttu-id="5d67e-163">(6 625 – 1 406,25) = 5 218,75</span><span class="sxs-lookup"><span data-stu-id="5d67e-163">(6,625 – 1,406.25) = 5,218.75</span></span> | <span data-ttu-id="5d67e-164">(5 625 – 1 406,25) = 4 218,75</span><span class="sxs-lookup"><span data-stu-id="5d67e-164">(5,625 – 1,406.25) = 4,218.75</span></span>         |

> [!NOTE] 
> <span data-ttu-id="5d67e-165">Když částka vypočtená s použitím metody 125% degresivního odpisování klesne pod hodnotu menší než má částka, která by byla vypočtena s použitím lineární metody, obvykle dojde k převodu na lineární metodu pro zbytek životnosti.</span><span class="sxs-lookup"><span data-stu-id="5d67e-165">Typically, when the amount that is calculated by using the 125% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>



