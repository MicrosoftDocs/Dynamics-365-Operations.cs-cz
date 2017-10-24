---
title: "Lineární odpis s vyrovnáním na konci životnosti"
description: "Tento článek poskytuje přehled o metodě odpisování Lineární s vyrovnáním na konci životnosti."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13851
ms.assetid: 0fa2f71a-596c-414c-a6e6-8f7405a0bf81
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 4ad82f3177e4abb7b9cb575b910aabc69901f475
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="straight-line-life-remaining-depreciation"></a><span data-ttu-id="3c0e3-103">Lineární odpis s vyrovnáním na konci životnosti</span><span class="sxs-lookup"><span data-stu-id="3c0e3-103">Straight line life remaining depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="3c0e3-104">Tento článek poskytuje přehled o metodě odpisování Lineární s vyrovnáním na konci životnosti.</span><span class="sxs-lookup"><span data-stu-id="3c0e3-104">This article gives an overview of the Straight line life remaining method of depreciation.</span></span>

<span data-ttu-id="3c0e3-105">Když nastavíte odpisový plán dlouhodobého majetku a zaškrtnete políčko **Lineární s vyrovnáním na konci životnosti** v poli **Metoda** na stránce **Profily odpisů**, budou odpisy dlouhodobého majetku přiřazeného k tomuto plánu založeny na zbývající době životnosti tohoto majetku.</span><span class="sxs-lookup"><span data-stu-id="3c0e3-105">When you set up a fixed asset depreciation profile and select **Straight line life remaining** in the **Method** field on the **Depreciation profiles** page, the depreciation of fixed assets that are assigned to the depreciation profile is based on the remaining service life of the asset.</span></span> <span data-ttu-id="3c0e3-106">Obvykle bude tato částka ve všech obdobích odpisu stejná.</span><span class="sxs-lookup"><span data-stu-id="3c0e3-106">The depreciation amount is generally the same in each depreciation period.</span></span> <span data-ttu-id="3c0e3-107">Pokud chcete nastavit odpisování podle zbývající lineární životnosti, je nutné také vybrat možnosti v polích **Odpisový rok** a **Frekvence období** na stránce **Odpisové profily**.</span><span class="sxs-lookup"><span data-stu-id="3c0e3-107">To set up straight line life remaining depreciation, you also must select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="3c0e3-108">Možnosti dostupné v poli **Frekvence období** se liší v závislosti na hodnotě vybrané v poli **Odpisový rok**.</span><span class="sxs-lookup"><span data-stu-id="3c0e3-108">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="3c0e3-109">Výběr odpisového roku</span><span class="sxs-lookup"><span data-stu-id="3c0e3-109">Select a depreciation year</span></span>
<span data-ttu-id="3c0e3-110">V poli **Odpisový rok** na stránce **Odpisové plány** můžete vybrat buď **Kalendářní** nebo **Fiskální**.</span><span class="sxs-lookup"><span data-stu-id="3c0e3-110">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="3c0e3-111">Výchozí hodnota je **Kalendářní**.</span><span class="sxs-lookup"><span data-stu-id="3c0e3-111">The default value is **Calendar**.</span></span> <span data-ttu-id="3c0e3-112">Vaše volba určí, jaké možnosti budou dostupné v poli **Frekvence období**.</span><span class="sxs-lookup"><span data-stu-id="3c0e3-112">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="3c0e3-113">Toto pole definuje časové rozdělení zaúčtování odpisů a částky v kalendářním roce.</span><span class="sxs-lookup"><span data-stu-id="3c0e3-113">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="3c0e3-114">Kalendář</span><span class="sxs-lookup"><span data-stu-id="3c0e3-114">Calendar</span></span>

<span data-ttu-id="3c0e3-115">Pokud v poli **Rok odpisu** vyberete ***Kalendářní***, bude předpokládán rok od 1. ledna do 31. prosince, a to i v případě, že jste definovali fiskální kalendář odlišně.</span><span class="sxs-lookup"><span data-stu-id="3c0e3-115">If you select **Calendar** in the ***Depreciation year*** field, a year of January 1 through December 31 is assumed, even if you've defined the fiscal calendar differently.</span></span> <span data-ttu-id="3c0e3-116">Možnost **Kalendářní** aktualizuje odpisovou základnu 1. ledna každého roku.</span><span class="sxs-lookup"><span data-stu-id="3c0e3-116">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="3c0e3-117">Odpisová základna je obvykle zůstatková účetní hodnota mínus likvidační hodnota.</span><span class="sxs-lookup"><span data-stu-id="3c0e3-117">Typically, the depreciation base is the net book value minus the salvage value.</span></span> <span data-ttu-id="3c0e3-118">V níže uvedených příkladech této kapitoly je odpisová základna čitatelem v prvním výrazu ve výpočtech ve sloupci Kalkulace.</span><span class="sxs-lookup"><span data-stu-id="3c0e3-118">In the example later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> <span data-ttu-id="3c0e3-119">Vyberete-li jako odpisový rok možnost **Kalendář**, v poli **Frekvence období** jsou k dispozici následující možnosti:</span><span class="sxs-lookup"><span data-stu-id="3c0e3-119">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="3c0e3-120">Možnost **Ročně** provede zaúčtování 31. prosince.</span><span class="sxs-lookup"><span data-stu-id="3c0e3-120">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="3c0e3-121">**Měsíčně** provádí zaúčtování měsíčně na konci každého kalendářního měsíce.</span><span class="sxs-lookup"><span data-stu-id="3c0e3-121">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="3c0e3-122">**Čtvrtletně** provádí zaúčtování čtvrtletní částky na konci každého kalendářního čtvrtletí (31. března, 30. června, 30. září a 31. prosince).</span><span class="sxs-lookup"><span data-stu-id="3c0e3-122">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="3c0e3-123">**Pololetně** provádí zaúčtování pololetní částky na konci každého pololetí kalendářního roku (30. června a 31. prosince).</span><span class="sxs-lookup"><span data-stu-id="3c0e3-123">**Half-Yearly** posts a half-yearly amount at the end of each calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="3c0e3-124">Položka **Denně** zaúčtuje částku odpisu pro metodu denních odpisů s použitím jedné transakce pro každý den.</span><span class="sxs-lookup"><span data-stu-id="3c0e3-124">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

<span data-ttu-id="3c0e3-125">Když například zvolíte **Ročně**, roční odpisy se zaúčtují pouze jednou – 31. prosince každého roku.</span><span class="sxs-lookup"><span data-stu-id="3c0e3-125">For example, if you select **Yearly**, the yearly depreciation is posted only one time, on December 31 of each year.</span></span> <span data-ttu-id="3c0e3-126">Pokud vyberete **Měsíčně**, měsíční odpis se zaúčtuje každý měsíc jako 1/12 ročního odpisu.</span><span class="sxs-lookup"><span data-stu-id="3c0e3-126">If you select **Monthly**, the monthly depreciation is posted each month, as one-twelfth of the yearly depreciation amount.</span></span>

### <a name="fiscal"></a><span data-ttu-id="3c0e3-127">Fiskální</span><span class="sxs-lookup"><span data-stu-id="3c0e3-127">Fiscal</span></span>

<span data-ttu-id="3c0e3-128">Pokud vyberete možnost **Fiskální** v poli **Odpisový rok**, bude použita metoda zbývajícího lineárního odpisu.</span><span class="sxs-lookup"><span data-stu-id="3c0e3-128">If you select **Fiscal** in the **Depreciation year** field, straight line life remaining depreciation is used.</span></span> <span data-ttu-id="3c0e3-129">Odpis je založen na zbývajících fiskální rocích.</span><span class="sxs-lookup"><span data-stu-id="3c0e3-129">Depreciation is calculated based on the fiscal years remaining.</span></span> <span data-ttu-id="3c0e3-130">Například pro fiskální rok od 1. července 2015 do 30. června 2016 začíná výpočet odpisů datem 1. července.</span><span class="sxs-lookup"><span data-stu-id="3c0e3-130">For example, for the fiscal year July 1, 2015, through June 30, 2016, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="3c0e3-131">Fiskální rok může být delší nebo kratší než 12 měsíců.</span><span class="sxs-lookup"><span data-stu-id="3c0e3-131">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="3c0e3-132">Odpisy se upravují pro jednotlivá fiskální období.</span><span class="sxs-lookup"><span data-stu-id="3c0e3-132">The depreciation is adjusted for each fiscal period.</span></span> <span data-ttu-id="3c0e3-133">Délka dalšího fiskálního roku záleží na nastavení fiskálního období na stránce **Fiskální kalendáře**.</span><span class="sxs-lookup"><span data-stu-id="3c0e3-133">The length of the next fiscal year is determined by the fiscal periods that are set up on the **Fiscal calendars** page.</span></span> <span data-ttu-id="3c0e3-134">Vyberete-li jako odpisový rok možnost **Fiskální**, v poli **Frekvence období** jsou k dispozici následující možnosti:</span><span class="sxs-lookup"><span data-stu-id="3c0e3-134">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="3c0e3-135">Možnost **Ročně** zaúčtuje celkovou částku odpisu vypočteného pro fiskální rok jako jednu částku poslední den fiskálního roku.</span><span class="sxs-lookup"><span data-stu-id="3c0e3-135">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year as one amount, on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="3c0e3-136">**Fiskální období**vypočte celkovou částku odpisu pro fiskální rok.</span><span class="sxs-lookup"><span data-stu-id="3c0e3-136">**Fiscal period** calculates the total amount of the depreciation for the fiscal year.</span></span> <span data-ttu-id="3c0e3-137">Tato částka se rozloží do fiskálních období, která jsou definována na stránce **Fiskální kalendáře** nebo pro fiskální kalendář uvedený pro knihu.</span><span class="sxs-lookup"><span data-stu-id="3c0e3-137">This amount is then accrued into the fiscal periods that are defined on the **Fiscal calendars** page for the fiscal calendar that is specified for the book.</span></span>

## <a name="example-of-straight-line-depreciation-of-an-unchanged-fixed-asset"></a><span data-ttu-id="3c0e3-138">Příklady lineárního odpisu nezměněného dlouhodobého majetku</span><span class="sxs-lookup"><span data-stu-id="3c0e3-138">Example of straight line depreciation of an unchanged fixed asset</span></span>
<span data-ttu-id="3c0e3-139">Dlouhodobý majetek má následující charakteristiky.</span><span class="sxs-lookup"><span data-stu-id="3c0e3-139">A fixed asset has the following characteristics.</span></span>

|                     |        |
|---------------------|--------|
| <span data-ttu-id="3c0e3-140">Pořizovací náklady</span><span class="sxs-lookup"><span data-stu-id="3c0e3-140">Acquisition cost</span></span>    | <span data-ttu-id="3c0e3-141">11 000</span><span class="sxs-lookup"><span data-stu-id="3c0e3-141">11,000</span></span> |
| <span data-ttu-id="3c0e3-142">Zůstatková hodnota</span><span class="sxs-lookup"><span data-stu-id="3c0e3-142">Salvage value</span></span>       | <span data-ttu-id="3c0e3-143">1 000</span><span class="sxs-lookup"><span data-stu-id="3c0e3-143">1,000</span></span>  |
| <span data-ttu-id="3c0e3-144">Odpisová základna</span><span class="sxs-lookup"><span data-stu-id="3c0e3-144">Depreciation base</span></span>   | <span data-ttu-id="3c0e3-145">10 000</span><span class="sxs-lookup"><span data-stu-id="3c0e3-145">10,000</span></span> |
| <span data-ttu-id="3c0e3-146">Roky životnosti</span><span class="sxs-lookup"><span data-stu-id="3c0e3-146">Service life years</span></span>  | <span data-ttu-id="3c0e3-147">5</span><span class="sxs-lookup"><span data-stu-id="3c0e3-147">5</span></span>      |
| <span data-ttu-id="3c0e3-148">Roční odpisy</span><span class="sxs-lookup"><span data-stu-id="3c0e3-148">Yearly depreciation</span></span> | <span data-ttu-id="3c0e3-149">2 000</span><span class="sxs-lookup"><span data-stu-id="3c0e3-149">2,000</span></span>  |

<span data-ttu-id="3c0e3-150">Částka odpisu je stejná pro každý rok: (pořizovací náklady - zůstatková hodnota) ÷ roky životnosti</span><span class="sxs-lookup"><span data-stu-id="3c0e3-150">The depreciation amount is the same every year: (Acquisition cost – Salvage value) ÷ Service life years</span></span>

| <span data-ttu-id="3c0e3-151">Období</span><span class="sxs-lookup"><span data-stu-id="3c0e3-151">Period</span></span> | <span data-ttu-id="3c0e3-152">Výpočet částky ročního odpisu</span><span class="sxs-lookup"><span data-stu-id="3c0e3-152">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="3c0e3-153">Čistá účetní hodnota na konci roku</span><span class="sxs-lookup"><span data-stu-id="3c0e3-153">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|---------------------------------------|
| <span data-ttu-id="3c0e3-154">Rok 1</span><span class="sxs-lookup"><span data-stu-id="3c0e3-154">Year 1</span></span> | <span data-ttu-id="3c0e3-155">(11 000 – 1 000) ÷ 5 = 2 000</span><span class="sxs-lookup"><span data-stu-id="3c0e3-155">(11,000 – 1,000) ÷ 5 = 2,000</span></span>                  | <span data-ttu-id="3c0e3-156">9 000</span><span class="sxs-lookup"><span data-stu-id="3c0e3-156">9,000</span></span>                                 |
| <span data-ttu-id="3c0e3-157">Rok 2</span><span class="sxs-lookup"><span data-stu-id="3c0e3-157">Year 2</span></span> | <span data-ttu-id="3c0e3-158">(9 000 – 1 000) ÷ 4 = 2 000</span><span class="sxs-lookup"><span data-stu-id="3c0e3-158">(9,000 – 1,000) ÷ 4 = 2,000</span></span>                   | <span data-ttu-id="3c0e3-159">7 000</span><span class="sxs-lookup"><span data-stu-id="3c0e3-159">7,000</span></span>                                 |
| <span data-ttu-id="3c0e3-160">Rok 3</span><span class="sxs-lookup"><span data-stu-id="3c0e3-160">Year 3</span></span> | <span data-ttu-id="3c0e3-161">(7 000 – 1 000) ÷ 3 = 2 000</span><span class="sxs-lookup"><span data-stu-id="3c0e3-161">(7,000 – 1,000) ÷ 3 = 2,000</span></span>                   | <span data-ttu-id="3c0e3-162">5 000</span><span class="sxs-lookup"><span data-stu-id="3c0e3-162">5,000</span></span>                                 |
| <span data-ttu-id="3c0e3-163">Rok 4</span><span class="sxs-lookup"><span data-stu-id="3c0e3-163">Year 4</span></span> | <span data-ttu-id="3c0e3-164">(5 000 – 1 000) ÷ 2 = 2 000</span><span class="sxs-lookup"><span data-stu-id="3c0e3-164">(5,000 – 1,000) ÷ 2 = 2,000</span></span>                   | <span data-ttu-id="3c0e3-165">3 000</span><span class="sxs-lookup"><span data-stu-id="3c0e3-165">3,000</span></span>                                 |
| <span data-ttu-id="3c0e3-166">Rok 5</span><span class="sxs-lookup"><span data-stu-id="3c0e3-166">Year 5</span></span> | <span data-ttu-id="3c0e3-167">(3 000 – 1 000) ÷ 1 = 2 000</span><span class="sxs-lookup"><span data-stu-id="3c0e3-167">(3,000 – 1,000) ÷ 1 = 2,000</span></span>                   | <span data-ttu-id="3c0e3-168">1 000</span><span class="sxs-lookup"><span data-stu-id="3c0e3-168">1,000</span></span>                                 |






