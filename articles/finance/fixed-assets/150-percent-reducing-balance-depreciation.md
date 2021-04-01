---
title: Degresivní odpis 150 procent
description: Tento článek poskytuje přehled o metodě odpisu „degresivní odpis 150 procent“.
author: saraschi2
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 13891
ms.assetid: 36d1112d-921c-4fff-abe0-0ff2429848d3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4edc868b76d466c41be8036b962730db90eeb68a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249430"
---
# <a name="150-percent-reducing-balance-depreciation"></a><span data-ttu-id="f91bd-103">Degresivní odpis 150 procent</span><span class="sxs-lookup"><span data-stu-id="f91bd-103">150 percent reducing balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f91bd-104">Tento článek poskytuje přehled o metodě odpisu „degresivní odpis 150 procent“.</span><span class="sxs-lookup"><span data-stu-id="f91bd-104">This article gives an overview of the 150 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="f91bd-105">Pokud nastavujete odpisový profil dlouhodobého majetku a zaškrtnete volbu **Degresivní 150 %** v poli **Metoda** na stránce **Odpisové profily**, dlouhodobý majetek, který je přiřazen k tomuto odpisovému profilu, bude odpisován o stejný procentní podíl v každém období odpisu.</span><span class="sxs-lookup"><span data-stu-id="f91bd-105">When you set up a fixed asset depreciation profile and select **150% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> <span data-ttu-id="f91bd-106">Tato procentuální hodnota se vypočte na základě životnosti majetku.</span><span class="sxs-lookup"><span data-stu-id="f91bd-106">This percentage is calculated based on the service life of the asset.</span></span> <span data-ttu-id="f91bd-107">Když má například majetek životnost pět let, procentuální hodnota se vypočte jako 30 procent (150 % ÷ 5).</span><span class="sxs-lookup"><span data-stu-id="f91bd-107">For example, if an asset has a service life of five years, the percentage is calculated as 30 percent (150% ÷ 5).</span></span> 

<span data-ttu-id="f91bd-108">Pokud chcete nastavit 150% degresivní odpisování, je nutné také vybrat možnosti v polích **Odpisový rok** a **Frekvence období** na stránce **Odpisové profily**.</span><span class="sxs-lookup"><span data-stu-id="f91bd-108">To set up 150% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="f91bd-109">Možnosti dostupné v poli **Frekvence období** se liší v závislosti na hodnotě vybrané v poli **Odpisový rok**.</span><span class="sxs-lookup"><span data-stu-id="f91bd-109">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="selection-of-depreciation-year"></a><span data-ttu-id="f91bd-110">Výběr roku pro odpisy</span><span class="sxs-lookup"><span data-stu-id="f91bd-110">Selection of depreciation year</span></span>
<span data-ttu-id="f91bd-111">V poli **Odpisový rok** na stránce **Odpisové plány** můžete vybrat buď **Kalendářní** nebo **Fiskální**.</span><span class="sxs-lookup"><span data-stu-id="f91bd-111">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> 

<span data-ttu-id="f91bd-112">Výchozí hodnota je **Kalendářní**.</span><span class="sxs-lookup"><span data-stu-id="f91bd-112">The default value is **Calendar**.</span></span> <span data-ttu-id="f91bd-113">Vaše volba určí, jaké možnosti budou dostupné v poli **Frekvence období**.</span><span class="sxs-lookup"><span data-stu-id="f91bd-113">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="f91bd-114">Toto pole definuje časové rozdělení zaúčtování odpisů a částky v kalendářním roce.</span><span class="sxs-lookup"><span data-stu-id="f91bd-114">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="f91bd-115">Kalendář</span><span class="sxs-lookup"><span data-stu-id="f91bd-115">Calendar</span></span>

<span data-ttu-id="f91bd-116">V poli **Odpisový rok** můžete ponechat výchozí hodnotu **Kalendářní**.</span><span class="sxs-lookup"><span data-stu-id="f91bd-116">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="f91bd-117">Možnost **Kalendářní** aktualizuje odpisovou základnu 1. ledna každého roku.</span><span class="sxs-lookup"><span data-stu-id="f91bd-117">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="f91bd-118">Odpisová základna je obvykle zůstatková účetní hodnota mínus likvidační hodnota.</span><span class="sxs-lookup"><span data-stu-id="f91bd-118">Typically, the depreciation base is the net book value minus the scrap value.</span></span> <span data-ttu-id="f91bd-119">V níže uvedených příkladech této kapitoly je odpisová základna čitatelem v prvním výrazu ve výpočtech ve sloupci Kalkulace.</span><span class="sxs-lookup"><span data-stu-id="f91bd-119">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="f91bd-120">Vyberete-li jako odpisový rok možnost **Kalendář**, v poli **Frekvence období** jsou k dispozici následující možnosti:</span><span class="sxs-lookup"><span data-stu-id="f91bd-120">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="f91bd-121">Možnost **Ročně** provede zaúčtování 31. prosince.</span><span class="sxs-lookup"><span data-stu-id="f91bd-121">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="f91bd-122">**Měsíčně** provádí zaúčtování měsíčně na konci každého kalendářního měsíce.</span><span class="sxs-lookup"><span data-stu-id="f91bd-122">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="f91bd-123">**Čtvrtletně** provádí zaúčtování čtvrtletní částky na konci každého kalendářního čtvrtletí (31. března, 30. června, 30. září a 31. prosince).</span><span class="sxs-lookup"><span data-stu-id="f91bd-123">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="f91bd-124">**Pololetně** provádí zaúčtování pololetní částky na konci poloviny kalendářního roku (30. června a 31. prosince).</span><span class="sxs-lookup"><span data-stu-id="f91bd-124">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="f91bd-125">Položka **Denně** zaúčtuje částku odpisu pro metodu denních odpisů s použitím jedné transakce pro každý den.</span><span class="sxs-lookup"><span data-stu-id="f91bd-125">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="f91bd-126">Fiskální</span><span class="sxs-lookup"><span data-stu-id="f91bd-126">Fiscal</span></span>

<span data-ttu-id="f91bd-127">Vyberete-li možnost **Fiskální** v poli **Odpisový rok**, degresivní odpis 150 % je vypočten na základě fiskálního roku pro fiskální kalendář, který je určen pro knihu, nebo pro fiskální kalendář, který je vybrán na stránce **Hlavní kniha**.</span><span class="sxs-lookup"><span data-stu-id="f91bd-127">If you select **Fiscal** in the **Depreciation year** field, 150% reducing balance depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="f91bd-128">Fiskální kalendáře se nastavují na stránce **Fiskální kalendáře**.</span><span class="sxs-lookup"><span data-stu-id="f91bd-128">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="f91bd-129">Například pro fiskální rok od 1. července do 30. června začíná výpočet odpisů datem 1. července.</span><span class="sxs-lookup"><span data-stu-id="f91bd-129">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="f91bd-130">Fiskální rok může být delší nebo kratší než 12 měsíců.</span><span class="sxs-lookup"><span data-stu-id="f91bd-130">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="f91bd-131">Odpisy se upravují pro jednotlivá období.</span><span class="sxs-lookup"><span data-stu-id="f91bd-131">The depreciation is adjusted for each period.</span></span> <span data-ttu-id="f91bd-132">Délka dalšího fiskálního roku záleží na nastavení období na stránce **Fiskální kalendáře**.</span><span class="sxs-lookup"><span data-stu-id="f91bd-132">The length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="f91bd-133">Vyberete-li jako odpisový rok možnost **Fiskální**, v poli **Frekvence období** jsou k dispozici následující možnosti:</span><span class="sxs-lookup"><span data-stu-id="f91bd-133">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="f91bd-134">**Ročně** - Zaúčtuje celkovou částku odpisu vypočteného pro fiskální rok poslední den fiskálního roku.</span><span class="sxs-lookup"><span data-stu-id="f91bd-134">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="f91bd-135">**Fiskální období** zaúčtuje celkovou částku odpisu vypočteného pro fiskální rok.</span><span class="sxs-lookup"><span data-stu-id="f91bd-135">**Fiscal period** posts the total amount of the depreciation that is calculated for the fiscal year.</span></span> <span data-ttu-id="f91bd-136">Tato částka se rozloží do fiskálních období, která jsou definována na stránce **Fiskální kalendáře**.</span><span class="sxs-lookup"><span data-stu-id="f91bd-136">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-150-reducing-balance-depreciation"></a><span data-ttu-id="f91bd-137">Příklad 150% degresivního odpisování</span><span class="sxs-lookup"><span data-stu-id="f91bd-137">Example of 150% reducing balance depreciation</span></span>

|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="f91bd-138">Pořizovací náklady</span><span class="sxs-lookup"><span data-stu-id="f91bd-138">Acquisition cost</span></span>               | <span data-ttu-id="f91bd-139">11 000</span><span class="sxs-lookup"><span data-stu-id="f91bd-139">11,000</span></span> |
| <span data-ttu-id="f91bd-140">Zůstatková hodnota</span><span class="sxs-lookup"><span data-stu-id="f91bd-140">Salvage value</span></span>                  | <span data-ttu-id="f91bd-141">1 000</span><span class="sxs-lookup"><span data-stu-id="f91bd-141">1,000</span></span>  |
| <span data-ttu-id="f91bd-142">Odpisová základna</span><span class="sxs-lookup"><span data-stu-id="f91bd-142">Depreciation base</span></span>              | <span data-ttu-id="f91bd-143">10 000</span><span class="sxs-lookup"><span data-stu-id="f91bd-143">10,000</span></span> |
| <span data-ttu-id="f91bd-144">Roky životnosti</span><span class="sxs-lookup"><span data-stu-id="f91bd-144">Service life years</span></span>             | <span data-ttu-id="f91bd-145">5</span><span class="sxs-lookup"><span data-stu-id="f91bd-145">5</span></span>      |
| <span data-ttu-id="f91bd-146">Roční procentuální hodnota odpisu</span><span class="sxs-lookup"><span data-stu-id="f91bd-146">Yearly depreciation percentage</span></span> | <span data-ttu-id="f91bd-147">30 %</span><span class="sxs-lookup"><span data-stu-id="f91bd-147">30%</span></span>    |

<span data-ttu-id="f91bd-148">Metoda degresivního odepisování 150 % vydělí 150 procent počtem roků životnosti.</span><span class="sxs-lookup"><span data-stu-id="f91bd-148">The 150% reducing balance method divides 150 percent by the service life years.</span></span> <span data-ttu-id="f91bd-149">Procentuální hodnota se vynásobí čistou účetní hodnotou majetku, aby byla určena částka odpisu pro rok.</span><span class="sxs-lookup"><span data-stu-id="f91bd-149">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="f91bd-150">Období</span><span class="sxs-lookup"><span data-stu-id="f91bd-150">Period</span></span> | <span data-ttu-id="f91bd-151">Výpočet částky ročního odpisu</span><span class="sxs-lookup"><span data-stu-id="f91bd-151">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="f91bd-152">Účetní hodnota</span><span class="sxs-lookup"><span data-stu-id="f91bd-152">Book value</span></span>             | <span data-ttu-id="f91bd-153">Čistá účetní hodnota na konci roku</span><span class="sxs-lookup"><span data-stu-id="f91bd-153">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| <span data-ttu-id="f91bd-154">Rok 1</span><span class="sxs-lookup"><span data-stu-id="f91bd-154">Year 1</span></span> | <span data-ttu-id="f91bd-155">(11 000 – 1 000) × 30 % = 3 000</span><span class="sxs-lookup"><span data-stu-id="f91bd-155">(11,000 – 1,000) × 30% = 3,000</span></span>                | <span data-ttu-id="f91bd-156">11 000 – 3 000 = 8 000</span><span class="sxs-lookup"><span data-stu-id="f91bd-156">11,000 – 3,000 = 8,000</span></span> | <span data-ttu-id="f91bd-157">11 000 – 1 000 – 3 000 = 7 000</span><span class="sxs-lookup"><span data-stu-id="f91bd-157">11,000 – 1,000 – 3,000 = 7,000</span></span>        |
| <span data-ttu-id="f91bd-158">Rok 2</span><span class="sxs-lookup"><span data-stu-id="f91bd-158">Year 2</span></span> | <span data-ttu-id="f91bd-159">7 000 × 30 % = 2 100</span><span class="sxs-lookup"><span data-stu-id="f91bd-159">7,000 × 30% = 2,100</span></span>                           | <span data-ttu-id="f91bd-160">8 000 – 2 100 = 5 900</span><span class="sxs-lookup"><span data-stu-id="f91bd-160">8,000 – 2,100 = 5,900</span></span>  | <span data-ttu-id="f91bd-161">7 000 – 2 100 = 4 900</span><span class="sxs-lookup"><span data-stu-id="f91bd-161">7,000 – 2,100 = 4,900</span></span>                 |
| <span data-ttu-id="f91bd-162">Rok 3</span><span class="sxs-lookup"><span data-stu-id="f91bd-162">Year 3</span></span> | <span data-ttu-id="f91bd-163">4 900 × 30 % = 1 470</span><span class="sxs-lookup"><span data-stu-id="f91bd-163">4,900 × 30% = 1,470</span></span>                           | <span data-ttu-id="f91bd-164">5 900 – 1 470 = 4 430</span><span class="sxs-lookup"><span data-stu-id="f91bd-164">5,900 – 1,470 = 4,430</span></span>  | <span data-ttu-id="f91bd-165">4 900 – 1 470 = 3 430</span><span class="sxs-lookup"><span data-stu-id="f91bd-165">4,900 – 1,470 = 3,430</span></span>                 |

> [!NOTE]
> <span data-ttu-id="f91bd-166">Když částka vypočtená s použitím metody 150% degresivního odpisování klesne pod hodnotu menší než má částka, která by byla vypočtena s použitím lineární metody, obvykle dojde k převodu na lineární metodu pro zbytek životnosti.</span><span class="sxs-lookup"><span data-stu-id="f91bd-166">Typically, when the amount that is calculated by using the 150% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]