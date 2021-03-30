---
title: Degresivní odpis
description: Tento článek poskytuje přehled o metodě degresivního odpisování.
author: ShylaThompson
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 3281
ms.assetid: 1b86763d-d47c-4a6a-a9a6-d97a736750da
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 69228aec217826780ceb91771028a6a5a180d037
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220978"
---
# <a name="reduce-balance-depreciation"></a><span data-ttu-id="91437-103">Degresivní odpis</span><span class="sxs-lookup"><span data-stu-id="91437-103">Reduce balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="91437-104">Tento článek poskytuje přehled o metodě degresivního odpisování.</span><span class="sxs-lookup"><span data-stu-id="91437-104">This article gives an overview of the Reducing balance method of depreciation.</span></span>

<span data-ttu-id="91437-105">Pokud nastavujete odpisový plán dlouhodobého majetku a zaškrtnete volbu Zrychleně v poli Metoda na stránce Odpisové profily, odpisy dlouhodobého majetku, který je přiřazen k tomuto odpisovému plánu, prováděny o stejný procentní podíl v každém období odpisu.</span><span class="sxs-lookup"><span data-stu-id="91437-105">When you set up a fixed asset depreciation profile and select Reducing balance in the Method field in the Depreciation profiles page, the assets that have this depreciation profile assigned to them are depreciated by the same percentage in each depreciation period.</span></span>

<span data-ttu-id="91437-106">Chcete-li nastavit degresivní odpisování, musíte také provést výběr v polích na pevné záložce Obecné na stránce Odpisové profily.</span><span class="sxs-lookup"><span data-stu-id="91437-106">To set up reducing balance depreciation, you must also make selections in fields on the General FastTab of the Depreciation profiles page.</span></span> <span data-ttu-id="91437-107">Nejprve vyberte příslušný rok v poli Odpisový rok.</span><span class="sxs-lookup"><span data-stu-id="91437-107">First, select a year in the Depreciation year field.</span></span> <span data-ttu-id="91437-108">V závislosti na vašem výběru se v poli Frekvence období zobrazí různé možnosti, jak je vysvětleno v následujících sekcích.</span><span class="sxs-lookup"><span data-stu-id="91437-108">Depending on the selection, different options appear in the Period frequency field, as explained in the following sections.</span></span> 

<span data-ttu-id="91437-109">Dále je pro odpisový plán nutné zadat hodnotu do pole Procento.</span><span class="sxs-lookup"><span data-stu-id="91437-109">You must also enter a value in the Percentage field for the depreciation profile.</span></span> <span data-ttu-id="91437-110">Vyberte-li možnost Úplné odpisy, použije se zbývající základ odpisů v posledním odpisovém období a může jít o velkou částku.</span><span class="sxs-lookup"><span data-stu-id="91437-110">If you select the Full depreciation option, the remaining depreciation basis is taken in the last depreciation period and could be a large amount.</span></span> <span data-ttu-id="91437-111">Některé země/oblasti nepoužívají přepínač na metodu lineárního odpisu.</span><span class="sxs-lookup"><span data-stu-id="91437-111">Some countries/regions do not use a switchover to a straight line method.</span></span> <span data-ttu-id="91437-112">K přepínání dojde, pokud je částka alternativní metody odpisování vyšší než částka původního plánu odpisu anebo se s ní shoduje a odebraná částka odpisu je částkou alternativní metody.</span><span class="sxs-lookup"><span data-stu-id="91437-112">Switchover occurs when the alternative depreciation method amount is greater than or equal to the primary depreciation profile amount, and the depreciation amount taken is the alternative method amount.</span></span> 

<span data-ttu-id="91437-113">Vzhledem k tomu, že majetek nebude nikdy možné zcela odepsat na základě procentuálního výpočtu, pro úplný odpis majetku je třeba vybrat možnost Úplné odpisy.</span><span class="sxs-lookup"><span data-stu-id="91437-113">Because an asset will never be fully depreciated based on a percentage calculation, you must select the Full depreciation option to fully depreciate an asset.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="91437-114">Výběr odpisového roku</span><span class="sxs-lookup"><span data-stu-id="91437-114">Select a depreciation year</span></span>
<span data-ttu-id="91437-115">V poli Odpisový rok na stránce Odpisové plány můžete vybrat buď Kalendářní, nebo Fiskální.</span><span class="sxs-lookup"><span data-stu-id="91437-115">You can select either Calendar or Fiscal in the Depreciation year field in the Depreciation profiles page.</span></span> <span data-ttu-id="91437-116">Tato volba určí, jaké možnosti budou dostupné v poli Frekvence období.</span><span class="sxs-lookup"><span data-stu-id="91437-116">The selection defines the options that are available in the Period frequency field.</span></span> <span data-ttu-id="91437-117">Výchozí volbou je Kalendářní.</span><span class="sxs-lookup"><span data-stu-id="91437-117">The default option is Calendar.</span></span>

### <a name="calendar"></a><span data-ttu-id="91437-118">Kalendář</span><span class="sxs-lookup"><span data-stu-id="91437-118">Calendar</span></span>

<span data-ttu-id="91437-119">Možnost Kalendářní aktualizuje odpisový základ (což je obvykle čistá účetní hodnota minus konečná zůstatková hodnota) 1. ledna každého roku.</span><span class="sxs-lookup"><span data-stu-id="91437-119">The Calendar option updates the depreciation base, which is typically the net book value minus the scrap value, on January 1 of each year.</span></span> <span data-ttu-id="91437-120">V příkladu degresivního odpisu později v tomto tématu je odpisová základna čitatelem v prvním výrazu ve výpočtech ve sloupci kalkulací.</span><span class="sxs-lookup"><span data-stu-id="91437-120">In the reducing balance depreciation example later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="91437-121">Jestliže vyberete možnost Kalendářní, v poli Frekvence období jsou k dispozici následující možnosti, které definují časové rozdělení zaúčtování odpisů a částky během kalendářního roku:</span><span class="sxs-lookup"><span data-stu-id="91437-121">If you select Calendar, the following options are available in the Period frequency field, which defines the depreciation accrual posting dates and amounts throughout the calendar year:</span></span>

-   <span data-ttu-id="91437-122">Ročně provádí zaúčtování 31. prosince.</span><span class="sxs-lookup"><span data-stu-id="91437-122">Yearly posts on December 31.</span></span>
-   <span data-ttu-id="91437-123">Měsíčně provádí zaúčtování měsíčně na konci každého kalendářního měsíce.</span><span class="sxs-lookup"><span data-stu-id="91437-123">Monthly posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="91437-124">Čtvrtletně provádí zaúčtování čtvrtletní částky na konci každého kalendářního čtvrtletí (31. března, 30. června, 30. září a 31. prosince).</span><span class="sxs-lookup"><span data-stu-id="91437-124">Quarterly posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="91437-125">Pololetně provádí zaúčtování pololetní částky na konci každého pololetí kalendářního roku (30. června a 31. prosince).</span><span class="sxs-lookup"><span data-stu-id="91437-125">Half-Yearly posts a half-yearly amount at the end of each calendar half-year (June 30 and December 31).</span></span>
-   <span data-ttu-id="91437-126">Denně zaúčtuje částku odpisu pro metodu denních odpisů s použitím jedné transakce pro každý den.</span><span class="sxs-lookup"><span data-stu-id="91437-126">Daily posts the depreciation amount for the daily depreciation method using one transaction for each day.</span></span>

<span data-ttu-id="91437-127">Když například zvolíte Ročně, roční odpisy se zaúčtují pouze jednou – 31. prosince každého roku.</span><span class="sxs-lookup"><span data-stu-id="91437-127">For example, if you select Yearly, the yearly depreciation is posted only one time, on December 31 of each year.</span></span> <span data-ttu-id="91437-128">Pokud vyberete Měsíčně, měsíční odpis se zaúčtuje každý měsíc jako 1/12 ročního odpisu.</span><span class="sxs-lookup"><span data-stu-id="91437-128">If you select Monthly, the monthly depreciation is posted each month as 1/12 of the yearly depreciation amount.</span></span>

### <a name="fiscal"></a><span data-ttu-id="91437-129">Fiskální</span><span class="sxs-lookup"><span data-stu-id="91437-129">Fiscal</span></span>

<span data-ttu-id="91437-130">Zaškrtnete-li v poli Odpisový rok volbu Fiskální, použije se metoda lineárního odpisu.</span><span class="sxs-lookup"><span data-stu-id="91437-130">If you select Fiscal in the Depreciation year field, the straight line depreciation method is used.</span></span> <span data-ttu-id="91437-131">Vypočítává se na základě fiskálního roku, který je nastaven na stránce Fiskální kalendáře, pro fiskální kalendář vybraný na stránce Hlavní kniha.</span><span class="sxs-lookup"><span data-stu-id="91437-131">It is calculated based on the fiscal year, which is set up in the Fiscal calendars page for the fiscal calendar that is selected in the Ledger page.</span></span> <span data-ttu-id="91437-132">Například pro fiskální rok od 1. července do 30. června začíná výpočet odpisů datem 1. července.</span><span class="sxs-lookup"><span data-stu-id="91437-132">For example, for fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="91437-133">Fiskální rok může být delší nebo kratší než 12 měsíců.</span><span class="sxs-lookup"><span data-stu-id="91437-133">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="91437-134">Odpisy se upravují pro jednotlivá fiskální období.</span><span class="sxs-lookup"><span data-stu-id="91437-134">The depreciation is adjusted for each fiscal period.</span></span> <span data-ttu-id="91437-135">Délka dalšího fiskálního roku vychází z fiskálních období nastavených při vytváření nového fiskálního roku na stránce Fiskální kalendáře.</span><span class="sxs-lookup"><span data-stu-id="91437-135">The length of the next fiscal year is based on the fiscal periods that you set up when you create a new fiscal year in the Fiscal calendars page.</span></span>


<span data-ttu-id="91437-136">Vyberete-li Fiskální, v poli Frekvence období jsou k dispozici následující možnosti:</span><span class="sxs-lookup"><span data-stu-id="91437-136">If you select Fiscal, the following options are available in the Period frequency field:</span></span>

-   <span data-ttu-id="91437-137">Ročně zaúčtuje celkovou částku odpisu vypočteného pro fiskální rok jako jednu částku poslední den fiskálního roku.</span><span class="sxs-lookup"><span data-stu-id="91437-137">Yearly posts the total amount of the depreciation calculated for the fiscal year as one amount on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="91437-138">Fiskální období zaúčtuje celkovou částku odpisu vypočteného pro fiskální rok, která se rozloží do fiskálních období definovaných pro fiskální kalendář vybraný na stránce Hlavní kniha nebo pro fiskální kalendář vybraný pro knihu pro dlouhodobý majetek.</span><span class="sxs-lookup"><span data-stu-id="91437-138">Fiscal period posts the total amount of the depreciation calculated for the fiscal year, which is accrued into the fiscal periods that are defined for the fiscal calendar that is selected in the Ledger page, or for the fiscal calendar that is selected for the book for a fixed asset.</span></span>

## <a name="example-of-reducing-balance-depreciation"></a><span data-ttu-id="91437-139">Příklad degresivního odpisování</span><span class="sxs-lookup"><span data-stu-id="91437-139">Example of reducing balance depreciation</span></span>

<span data-ttu-id="91437-140">Předpokládejme, že pořizovací cena dlouhodobého majetku činí 11 000, konečná zůstatková hodnota je 1000 a procentuální koeficient odpisu je 30.</span><span class="sxs-lookup"><span data-stu-id="91437-140">Suppose that the fixed asset acquisition price is 11,000, the scrap value is 1,000, and the depreciation percentage factor is 30.</span></span> 

<span data-ttu-id="91437-141">Pomocí metody Degresivní odpisování je 30 % odpisové základny (čistá účetní hodnota mínus konečná zůstatková hodnota) vypočítáno na konci předchozího odpisového období.</span><span class="sxs-lookup"><span data-stu-id="91437-141">Using the Reducing balance method, 30 percent of the depreciation base (net book value minus scrap value) is calculated at the end of the previous depreciation period.</span></span> <span data-ttu-id="91437-142">Odpisy za první tři roky jsou uvedeny v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="91437-142">Depreciation for the first three years is shown in the following table.</span></span>

| <span data-ttu-id="91437-143">Období</span><span class="sxs-lookup"><span data-stu-id="91437-143">Period</span></span> | <span data-ttu-id="91437-144">Výpočet částky ročního odpisu</span><span class="sxs-lookup"><span data-stu-id="91437-144">Calculation of yearly depreciation amount</span></span> | <span data-ttu-id="91437-145">Čistá účetní hodnota na konci roku</span><span class="sxs-lookup"><span data-stu-id="91437-145">Net book value at the end of the year</span></span> |
|--------|-------------------------------------------|---------------------------------------|
| <span data-ttu-id="91437-146">Rok 1</span><span class="sxs-lookup"><span data-stu-id="91437-146">Year 1</span></span> | <span data-ttu-id="91437-147">(11,000 - 1,000) \* 30% = 3,000</span><span class="sxs-lookup"><span data-stu-id="91437-147">(11,000 - 1,000) \* 30% = 3,000</span></span>           | <span data-ttu-id="91437-148">(11 000 – 1 000) – 3 000 = 7 000</span><span class="sxs-lookup"><span data-stu-id="91437-148">(11,000 - 1,000) - 3,000 = 7,000</span></span>      |
| <span data-ttu-id="91437-149">Rok 2</span><span class="sxs-lookup"><span data-stu-id="91437-149">Year 2</span></span> | <span data-ttu-id="91437-150">(7,000 - 1,000) \* 30% = 1,800</span><span class="sxs-lookup"><span data-stu-id="91437-150">(7,000 - 1,000) \* 30% = 1,800</span></span>            | <span data-ttu-id="91437-151">(7 000 – 1 800) = 5 200</span><span class="sxs-lookup"><span data-stu-id="91437-151">(7,000 -1,800) = 5,200</span></span>                |
| <span data-ttu-id="91437-152">Rok 3</span><span class="sxs-lookup"><span data-stu-id="91437-152">Year 3</span></span> | <span data-ttu-id="91437-153">(5,200 - 1,000) \* 30% = 1,260</span><span class="sxs-lookup"><span data-stu-id="91437-153">(5,200 - 1,000) \* 30% = 1,260</span></span>            | <span data-ttu-id="91437-154">(5 200 – 1 260) = 3 940</span><span class="sxs-lookup"><span data-stu-id="91437-154">(5,200 - 1,260) = 3,940</span></span>               |


-







[!INCLUDE[footer-include](../../includes/footer-banner.md)]