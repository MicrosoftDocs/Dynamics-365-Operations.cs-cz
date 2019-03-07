---
title: Ruční odpis
description: Tento článek poskytuje přehled o metodě ručního odpisu.
author: ShylaThompson
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
ms.custom: 13811
ms.assetid: b0e837c9-515a-4aed-9060-5ec94f37edeb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 14e385e60e10146a0855a467af57a0a31fcc53bd
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "330993"
---
# <a name="manual-depreciation"></a><span data-ttu-id="b4509-103">Ruční odpis</span><span class="sxs-lookup"><span data-stu-id="b4509-103">Manual depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b4509-104">Tento článek poskytuje přehled o metodě ručního odpisu.</span><span class="sxs-lookup"><span data-stu-id="b4509-104">This article gives an overview of the manual depreciation method.</span></span>

<span data-ttu-id="b4509-105">Když nastavujete odpisový plán dlouhodobého majetku a v poli **Metoda** na stránce **Odpisové plány** vyberete položku **Ručně**, jsou odpisy dlouhodobého majetku přiřazené k odpisovému plánu stanoveny podle procentuální hodnoty zadané pro každý interval v kalendářním roce.</span><span class="sxs-lookup"><span data-stu-id="b4509-105">When you set up a fixed asset depreciation profile and select **Manual** in the **Method** field on the **Depreciation profiles** page, the depreciation of fixed assets that are assigned to the depreciation profile is determined by the percentage that you enter for each interval in the calendar year.</span></span> <span data-ttu-id="b4509-106">Nastavené procentuální hodnoty pro intervaly jsou zaúčtovány podle hodnoty, kterou jste vybrali v poli **Frekvence období** na pevné záložce **Obecné** na stránce **Odpisové plány**.</span><span class="sxs-lookup"><span data-stu-id="b4509-106">The intervals that you set up percentages for are posted according to the value that you select in the **Period frequency** field on the **General** FastTab of the **Depreciation profiles** page.</span></span> <span data-ttu-id="b4509-107">Vybrat můžete tyto hodnoty:</span><span class="sxs-lookup"><span data-stu-id="b4509-107">Here are the values that you can select:</span></span>

-   <span data-ttu-id="b4509-108">Ročně</span><span class="sxs-lookup"><span data-stu-id="b4509-108">Yearly</span></span>
-   <span data-ttu-id="b4509-109">Měsíčně</span><span class="sxs-lookup"><span data-stu-id="b4509-109">Monthly</span></span>
-   <span data-ttu-id="b4509-110">Kvartálně</span><span class="sxs-lookup"><span data-stu-id="b4509-110">Quarterly</span></span>
-   <span data-ttu-id="b4509-111">Pololetně</span><span class="sxs-lookup"><span data-stu-id="b4509-111">Half-Yearly</span></span>
-   <span data-ttu-id="b4509-112">Denně</span><span class="sxs-lookup"><span data-stu-id="b4509-112">Daily</span></span>

<span data-ttu-id="b4509-113">Po výběru frekvence období klikněte na možnost **Ruční plány** a nastavte procentuální hodnoty pro jednotlivé intervaly účtování.</span><span class="sxs-lookup"><span data-stu-id="b4509-113">After you select the period frequency, click **Manual schedules**, and set up percentages for each posting interval.</span></span> <span data-ttu-id="b4509-114">Ručně zadávané plány a intervaly účtování společně definují částku odpisu (viz příklady níže v tomto článku).</span><span class="sxs-lookup"><span data-stu-id="b4509-114">Together, the manual schedules and the posting intervals define the depreciation amount, as shown in the examples later in this article.</span></span> <span data-ttu-id="b4509-115">Ruční odpisy se vždy počítají jako procentuální hodnota pořizovací ceny.</span><span class="sxs-lookup"><span data-stu-id="b4509-115">Manual depreciation is always calculated as a percentage of the acquisition price.</span></span> <span data-ttu-id="b4509-116">U ručních odpisů nemusí procentuální hodnoty, které zadáváte do intervalů odpisu, dávat dohromady 100 procent.</span><span class="sxs-lookup"><span data-stu-id="b4509-116">For manual depreciation, the percentages that you enter in the intervals of the depreciation don't have to add up to 100 percent.</span></span> <span data-ttu-id="b4509-117">Ruční odpisy jsou flexibilní odpisovou metodu, která se často používá k určení mimořádného odpisového plánu na stránce **Knihy**, jako je například nepravidelný odpis pro zvláštní účely (například daň).</span><span class="sxs-lookup"><span data-stu-id="b4509-117">Manual depreciation is a flexible depreciation method that is often used to define an extraordinary depreciation profile on the **Books** page, such as a non-periodic depreciation for special purposes (for example, tax).</span></span>

## <a name="examples"></a><span data-ttu-id="b4509-118">Příklad</span><span class="sxs-lookup"><span data-stu-id="b4509-118">Examples</span></span>
<span data-ttu-id="b4509-119">Pořizovací cena: 11 000,00 Předpokládaná konečná zůstatková hodnota: 1 000,00 V následující tabulce jsou uvedeny intervaly a procentuální hodnoty, které se nastavují na stránce **Plán odpisových plánů dlouhodobého majetku**.</span><span class="sxs-lookup"><span data-stu-id="b4509-119">Acquisition price: 11,000.00 Expected scrap value: 1,000.00 The following table shows the intervals and percentages that you set up on the **Fixed asset depreciation profile schedules** page.</span></span>

| <span data-ttu-id="b4509-120">Číslo intervalu</span><span class="sxs-lookup"><span data-stu-id="b4509-120">Interval number</span></span> | <span data-ttu-id="b4509-121">Procento</span><span class="sxs-lookup"><span data-stu-id="b4509-121">Percentage</span></span> |
|-----------------|------------|
| <span data-ttu-id="b4509-122">1</span><span class="sxs-lookup"><span data-stu-id="b4509-122">1</span></span>               | <span data-ttu-id="b4509-123">10,00</span><span class="sxs-lookup"><span data-stu-id="b4509-123">10.00</span></span>      |
| <span data-ttu-id="b4509-124">2</span><span class="sxs-lookup"><span data-stu-id="b4509-124">2</span></span>               | <span data-ttu-id="b4509-125">50,00</span><span class="sxs-lookup"><span data-stu-id="b4509-125">50.00</span></span>      |
| <span data-ttu-id="b4509-126">3</span><span class="sxs-lookup"><span data-stu-id="b4509-126">3</span></span>               | <span data-ttu-id="b4509-127">8,00</span><span class="sxs-lookup"><span data-stu-id="b4509-127">8.00</span></span>       |

<span data-ttu-id="b4509-128">V následující tabulce je znázorněn způsob výpočtu odpisu pro jednotlivé intervaly.</span><span class="sxs-lookup"><span data-stu-id="b4509-128">The following table shows how the depreciation for each interval is calculated.</span></span>

|  <span data-ttu-id="b4509-129">Číslo intervalu</span><span class="sxs-lookup"><span data-stu-id="b4509-129">Interval number</span></span> | <span data-ttu-id="b4509-130">Výpočet částky ročního odpisu</span><span class="sxs-lookup"><span data-stu-id="b4509-130">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="b4509-131">Zůstatková účetní hodnota na konci intervalu</span><span class="sxs-lookup"><span data-stu-id="b4509-131">Net book value at the end of the interval</span></span> |
|------------------|-----------------------------------------------|-------------------------------------------|
| <span data-ttu-id="b4509-132">1</span><span class="sxs-lookup"><span data-stu-id="b4509-132">1</span></span>                | <span data-ttu-id="b4509-133">(11 000 – 1 000) × 10 % = 1 000</span><span class="sxs-lookup"><span data-stu-id="b4509-133">(11,000 – 1,000) × 10% = 1,000</span></span>                | <span data-ttu-id="b4509-134">10,000 (11 000 – 1 000)</span><span class="sxs-lookup"><span data-stu-id="b4509-134">10,000 (11,000 – 1,000)</span></span>                   |
| <span data-ttu-id="b4509-135">2</span><span class="sxs-lookup"><span data-stu-id="b4509-135">2</span></span>                | <span data-ttu-id="b4509-136">(11 000 – 1 000) × 50 % = 5 000</span><span class="sxs-lookup"><span data-stu-id="b4509-136">(11,000 – 1,000) × 50% = 5,000</span></span>                | <span data-ttu-id="b4509-137">5 000 (10 000 – 5 000)</span><span class="sxs-lookup"><span data-stu-id="b4509-137">5,000 (10,000 – 5,000)</span></span>                    |
| <span data-ttu-id="b4509-138">3</span><span class="sxs-lookup"><span data-stu-id="b4509-138">3</span></span>                | <span data-ttu-id="b4509-139">(11 000 – 1 000) × 8 % = 800</span><span class="sxs-lookup"><span data-stu-id="b4509-139">(11,000 – 1,000) × 8% = 800</span></span>                   | <span data-ttu-id="b4509-140">4 200 (5 000 – 800)</span><span class="sxs-lookup"><span data-stu-id="b4509-140">4,200 (5,000 – 800)</span></span>                       |

<span data-ttu-id="b4509-141">Pokud v poli **Frekvence období** vyberete hodnotu **Měsíčně**, je nutné zadat 12 ručně naplánovaných intervalů.</span><span class="sxs-lookup"><span data-stu-id="b4509-141">If you select **Monthly** in the **Period frequency** field, you set up 12 manual schedule intervals.</span></span> <span data-ttu-id="b4509-142">V následující tabulce jsou uvedeny částky odpisů za první dva intervaly.</span><span class="sxs-lookup"><span data-stu-id="b4509-142">The following table shows the depreciation amounts for the first two intervals.</span></span>

| <span data-ttu-id="b4509-143">Interval</span><span class="sxs-lookup"><span data-stu-id="b4509-143">Interval</span></span> | <span data-ttu-id="b4509-144">Odpisovaná částka</span><span class="sxs-lookup"><span data-stu-id="b4509-144">Depreciation amount</span></span>            |
|----------|--------------------------------|
| <span data-ttu-id="b4509-145">Leden</span><span class="sxs-lookup"><span data-stu-id="b4509-145">January</span></span>  | <span data-ttu-id="b4509-146">(11 000 – 1 000) × 10 % = 1 000</span><span class="sxs-lookup"><span data-stu-id="b4509-146">(11,000 – 1,000) × 10% = 1,000</span></span> |
| <span data-ttu-id="b4509-147">Únor</span><span class="sxs-lookup"><span data-stu-id="b4509-147">February</span></span> | <span data-ttu-id="b4509-148">(11 000 – 1 000) × 50 % = 5 000</span><span class="sxs-lookup"><span data-stu-id="b4509-148">(11,000 – 1,000) × 50% = 5,000</span></span> |

<span data-ttu-id="b4509-149">Pokud vyberete hodnotu <strong>Pololetně</strong> v poli *<strong><em>Frekvence období</em>*,</strong> nastavujete dva ruční intervaly plánu.</span><span class="sxs-lookup"><span data-stu-id="b4509-149">If you select <strong>Half-Yearly</strong> in the *<strong><em>Period frequency</em>* field</strong>, you set up two manual schedule intervals.</span></span> <span data-ttu-id="b4509-150">V následující tabulce jsou uvedeny částky odpisů za tyto dva intervaly.</span><span class="sxs-lookup"><span data-stu-id="b4509-150">The following table shows the depreciation amounts for those two intervals.</span></span>

| <span data-ttu-id="b4509-151">Interval</span><span class="sxs-lookup"><span data-stu-id="b4509-151">Interval</span></span>    | <span data-ttu-id="b4509-152">Odpisovaná částka</span><span class="sxs-lookup"><span data-stu-id="b4509-152">Depreciation amount</span></span>            |
|-------------|--------------------------------|
| <span data-ttu-id="b4509-153">30. června</span><span class="sxs-lookup"><span data-stu-id="b4509-153">June 30</span></span>     | <span data-ttu-id="b4509-154">(11 000 – 1 000) × 10 % = 1 000</span><span class="sxs-lookup"><span data-stu-id="b4509-154">(11,000 – 1,000) × 10% = 1,000</span></span> |
| <span data-ttu-id="b4509-155">31. prosince</span><span class="sxs-lookup"><span data-stu-id="b4509-155">December 31</span></span> | <span data-ttu-id="b4509-156">(11 000 – 1 000) × 50 % = 5 000</span><span class="sxs-lookup"><span data-stu-id="b4509-156">(11,000 – 1,000) × 50% = 5,000</span></span> |

<span data-ttu-id="b4509-157">Celkové procento pro všechny intervaly nemusí být 100.</span><span class="sxs-lookup"><span data-stu-id="b4509-157">The total of percentages for all intervals doesn't have to be 100.</span></span> <span data-ttu-id="b4509-158">Pokud však hodnota v poli **Kumulativní procento** na stránce **Plán odpisových plánů dlouhodobého majetku** není **100**, obdržíte zprávu.</span><span class="sxs-lookup"><span data-stu-id="b4509-158">However, you receive a message if the value in the **Cumulative percentage** field on the **Fixed asset depreciation profile schedules** page isn't **100**.</span></span>



