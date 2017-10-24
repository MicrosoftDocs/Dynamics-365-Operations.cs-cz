---
title: "Nastavení úrokových sazeb pro kód úroku"
description: "Kódy úroků obsahují nastavení, která určují, kdy bude placen úrok a jak se vypočítá na účtech po splatnosti."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 59402
ms.assetid: 3b945333-1eaf-4658-ab5a-1a7791a7eb40
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 59acfaa93b1352f2be6d750dea6bdd740bac0312
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-interest-rates-for-an-interest-code"></a><span data-ttu-id="d2c55-103">Nastavení úrokových sazeb pro kód úroku</span><span class="sxs-lookup"><span data-stu-id="d2c55-103">Set up interest rates for an interest code</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="d2c55-104">Kódy úroků obsahují nastavení, která určují, kdy bude placen úrok a jak se vypočítá na účtech po splatnosti.</span><span class="sxs-lookup"><span data-stu-id="d2c55-104">Interest codes contain settings that determine when interest is charged and how it is calculated on overdue accounts.</span></span>

<span data-ttu-id="d2c55-105">Můžete nastavit jediný kód úroku a použít ho pro více účetních profilů zákazníků, účtovacích kódů nebo určité řady faktur.</span><span class="sxs-lookup"><span data-stu-id="d2c55-105">You can set up a single interest code and apply it to multiple customer posting profiles, billing codes, or to specific invoice lines.</span></span> <span data-ttu-id="d2c55-106">Při změně podrobností kódu úroku, všechny funkce, které používají kód automaticky implementují změny pro nové transakce.</span><span class="sxs-lookup"><span data-stu-id="d2c55-106">When the interest code details are changed, all features that use the code will automatically implement the changes on new transactions.</span></span> <span data-ttu-id="d2c55-107">Pro každý kód úroku můžete nastavit dva typy sazeb:</span><span class="sxs-lookup"><span data-stu-id="d2c55-107">For each interest code, you can set up two types of rates:</span></span>
-   <span data-ttu-id="d2c55-108">Sazby pro úrokové příjmy – představují výnosy, které jsou vytvořené účtováním úroků na fakturách nebo oznámeních úroků.</span><span class="sxs-lookup"><span data-stu-id="d2c55-108">Rates for interest earnings − These represent revenue that is earned by charging interest on invoices or interest notes.</span></span>
-   <span data-ttu-id="d2c55-109">Sazby pro úrokové platby − představují náklady zaplacené za úrok u dobropisů.</span><span class="sxs-lookup"><span data-stu-id="d2c55-109">Rates for interest payments − These represent a cost that is paid for interest on credit notes.</span></span>

<span data-ttu-id="d2c55-110">Oba tyto typy sazeb mohou existovat ve stejnou dobu a ve stejném kódu úroku.</span><span class="sxs-lookup"><span data-stu-id="d2c55-110">Both of these rate types can exist at the same time and in the same interest code.</span></span> <span data-ttu-id="d2c55-111">Úrokové sazby mohou být založeny na třech typech výpočtů:</span><span class="sxs-lookup"><span data-stu-id="d2c55-111">Interest rates can be based on three calculation types:</span></span>
-   <span data-ttu-id="d2c55-112">Úrok podle procent.</span><span class="sxs-lookup"><span data-stu-id="d2c55-112">Interest by percentage.</span></span>
-   <span data-ttu-id="d2c55-113">Úrok podle částky.</span><span class="sxs-lookup"><span data-stu-id="d2c55-113">Interest by amount.</span></span>
-   <span data-ttu-id="d2c55-114">Úrok podle rozsahu, jehož výsledkem je jednotná procentní sazba nebo částka.</span><span class="sxs-lookup"><span data-stu-id="d2c55-114">Interest by range, which results in a single percentage or amount.</span></span>

<span data-ttu-id="d2c55-115">Při použití kódu úroku, který se používá k výpočtu úroku, je pro každou úrokovou sazbu platnou v době, kdy platba překročila datum splatnosti transakce, vytvořeno samostatné oznámení úroků.</span><span class="sxs-lookup"><span data-stu-id="d2c55-115">When an interest code is used to calculate interest, a separate interest note is created for each interest rate that is in effect during the time that the payment has exceeded the transaction due date.</span></span> <span data-ttu-id="d2c55-116">K nastavení úrokových sazeb pro úroky, které můžete získat účtováním úroků, slouží karta **Zisky** na stránce **Kód úroku**.</span><span class="sxs-lookup"><span data-stu-id="d2c55-116">You use the **Earnings** tab on the **Interest code** page to set up interest rates for interest that you earn by charging interest.</span></span> <span data-ttu-id="d2c55-117">Na kartě **Platby** můžete nastavit úrokové sazby pro úroky, které platíte.</span><span class="sxs-lookup"><span data-stu-id="d2c55-117">Use the **Payments** tab to set up interest rates for interest that you pay.</span></span>

## <a name="interest-rates-based-on-a-percentage"></a><span data-ttu-id="d2c55-118">Úrokové sazby podle procent</span><span class="sxs-lookup"><span data-stu-id="d2c55-118">Interest rates based on a percentage</span></span>
<span data-ttu-id="d2c55-119">Můžete nastavit úrokové sazby pro výpočet zadané procentní hodnoty.</span><span class="sxs-lookup"><span data-stu-id="d2c55-119">You can set up interest rates that calculate a specified percentage.</span></span>

-   <span data-ttu-id="d2c55-120">Částka úroku platí pro všechny měny.</span><span class="sxs-lookup"><span data-stu-id="d2c55-120">Interest amount applies to all currencies.</span></span>
-   <span data-ttu-id="d2c55-121">Volitelně lze zadat omezení částky úroku.</span><span class="sxs-lookup"><span data-stu-id="d2c55-121">Optional interest amount limits can be entered.</span></span>
-   <span data-ttu-id="d2c55-122">Na stránce **Nastavení kódů úroků** je v poli **Vypočítat úrok podle** zvolena možnost **Procento**.</span><span class="sxs-lookup"><span data-stu-id="d2c55-122">**Percentage** is selected** **in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="d2c55-123">Pokud chcete například nastavit kód úroku, který stanoví 5% úrok po uplynutí každých dvou měsíců, kdy je faktura po splatnosti, zadejte do pole **Vypočítat úroky jednou za** hodnotu 2 a vyberte možnost **Měsíc**.</span><span class="sxs-lookup"><span data-stu-id="d2c55-123">For example, to set up an interest code that assesses 5 percent interest for every two months that the invoice payment exceeds the transaction due date, you would enter 2 in the **Calculate interest every** field and select **Month**.</span></span>

## <a name="interest-rates-based-on-amounts"></a><span data-ttu-id="d2c55-124">Úrokové sazby podle částek</span><span class="sxs-lookup"><span data-stu-id="d2c55-124">Interest rates based on amounts</span></span>
<span data-ttu-id="d2c55-125">Můžete nastavit úrokové sazby pro výpočet určité částky podle měny.</span><span class="sxs-lookup"><span data-stu-id="d2c55-125">You can set up interest rates that calculate a specified amount per currency.</span></span>
-   <span data-ttu-id="d2c55-126">Částka úroku se zadává pro každou měnu v kódu úroku.</span><span class="sxs-lookup"><span data-stu-id="d2c55-126">An interest amount is specified for each currency in the interest code.</span></span>
-   <span data-ttu-id="d2c55-127">Volitelně lze zadat omezení částky úroku.</span><span class="sxs-lookup"><span data-stu-id="d2c55-127">Optional interest amount limits can be entered.</span></span>
-   <span data-ttu-id="d2c55-128">Na stránce **Nastavení kódů úroků** je v poli **Vypočítat úrok podle** zvolena možnost **Částka **.</span><span class="sxs-lookup"><span data-stu-id="d2c55-128">**Amount **is selected in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="d2c55-129">Pokud chcete například nastavit kód úroku, který stanoví úrok 25,00 po uplynutí každých 20 dnů, kdy je faktura po splatnosti, zadejte do pole **Vypočítat úroky jednou za** hodnotu 20 a vyberte možnost **Den**.</span><span class="sxs-lookup"><span data-stu-id="d2c55-129">For example, to set up an interest code that assesses interest of 25.00 for every 20 days that the invoice payment exceeds the transaction due date, you would enter 20 in the **Calculate interest every** field and select **Day**.</span></span>

## <a name="interest-rates-based-on-ranges"></a><span data-ttu-id="d2c55-130">Úrokové sazby podle rozsahů</span><span class="sxs-lookup"><span data-stu-id="d2c55-130">Interest rates based on ranges</span></span>
<span data-ttu-id="d2c55-131">Můžete nastavit úrokové sazby, které jsou závislé na částce po splatnosti, počtu dní, po které je částka po splatnosti nebo počtu měsíců, po které je částka po splatnosti.</span><span class="sxs-lookup"><span data-stu-id="d2c55-131">You can set up interest rates that vary depending on the overdue amount, the number of days that the amount is late, or the number of months that the amount is late.</span></span>
-   <span data-ttu-id="d2c55-132">Na kartě **Zisky podle měny** můžete určit specifické nastavení úroků pro každou měnu.</span><span class="sxs-lookup"><span data-stu-id="d2c55-132">You can use the **Earnings by Currency** tab to define specific interest settings for each currency.</span></span> <span data-ttu-id="d2c55-133">Na stejném místě se určuje také rozsah.</span><span class="sxs-lookup"><span data-stu-id="d2c55-133">This is also where you will define the range.</span></span>
-   <span data-ttu-id="d2c55-134">K přidání řádků, které představují rozsahy, které chcete nastavit, použijte tlačítko **Rozsahy**.</span><span class="sxs-lookup"><span data-stu-id="d2c55-134">Use the **Ranges** button to add lines that represent the ranges that you want to set up.</span></span> <span data-ttu-id="d2c55-135">Hodnota **Od** představuje začátek rozsahu a číslo **Hodnota úroků** představuje procento nebo částku (podle výběru provedeného v poli **Vypočítat úrok podle** na stránce **Nastavení kódů úroku**).</span><span class="sxs-lookup"><span data-stu-id="d2c55-135">The **From** value represents the beginning of the range and the **Interest value** number represents either a percentage or an amount, depending on the selection in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

## <a name="example-1-interest-by-range--amount"></a><span data-ttu-id="d2c55-136">Příklad 1: Úroky podle rozsahu = částka</span><span class="sxs-lookup"><span data-stu-id="d2c55-136">Example 1: Interest by range = Amount</span></span>
<span data-ttu-id="d2c55-137">Nastavíte kód úroku, který přiřadí úrok jednou za každé tři měsíce, po které platba faktury překročí její splatnost.</span><span class="sxs-lookup"><span data-stu-id="d2c55-137">You set up an interest code that assesses interest one time for every three months that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="d2c55-138">Chcete založit výpočet na hodnotě úroku v procentech podle stupňovitých intervalů částky.</span><span class="sxs-lookup"><span data-stu-id="d2c55-138">You want to base the calculation on a percentage interest value, according to stepped amount intervals.</span></span> <span data-ttu-id="d2c55-139">Hodnota úroku bude 1 % pro fakturační částky do 1 000,00, 2 procenta pro částky od 1 001,00 do 5 000,00 a 3 % pro částky větší než 5 000,00.</span><span class="sxs-lookup"><span data-stu-id="d2c55-139">The interest value will be 1 percent for invoice amounts up to 1,000.00, 2 percent for amounts from 1,001.00 to 5,000.00, and 3 percent for amounts larger than 5,000.00.</span></span> <span data-ttu-id="d2c55-140">Hodnoty polí pro kód úroku nastavíte následovně.</span><span class="sxs-lookup"><span data-stu-id="d2c55-140">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="d2c55-141">**Název pole**</span><span class="sxs-lookup"><span data-stu-id="d2c55-141">**Field name**</span></span>                  | <span data-ttu-id="d2c55-142">**Hodnota pole**</span><span class="sxs-lookup"><span data-stu-id="d2c55-142">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="d2c55-143">**Kód úroku**</span><span class="sxs-lookup"><span data-stu-id="d2c55-143">**Interest code**</span></span>               | <span data-ttu-id="d2c55-144">3M%ByAmt</span><span class="sxs-lookup"><span data-stu-id="d2c55-144">3M%ByAmt</span></span>        |
| <span data-ttu-id="d2c55-145">**Vypočítat úroky jednou za**</span><span class="sxs-lookup"><span data-stu-id="d2c55-145">**Calculate interest every**</span></span>    | <span data-ttu-id="d2c55-146">3/měsíc</span><span class="sxs-lookup"><span data-stu-id="d2c55-146">3/Month</span></span>         |
| <span data-ttu-id="d2c55-147">**Úrok podle rozsahu**</span><span class="sxs-lookup"><span data-stu-id="d2c55-147">**Interest by range**</span></span>           | <span data-ttu-id="d2c55-148">Částka</span><span class="sxs-lookup"><span data-stu-id="d2c55-148">Amount</span></span>          |
| <span data-ttu-id="d2c55-149">**Vypočítat úrok podle**</span><span class="sxs-lookup"><span data-stu-id="d2c55-149">**Calculate interest based on**</span></span> | <span data-ttu-id="d2c55-150">Procento</span><span class="sxs-lookup"><span data-stu-id="d2c55-150">Percentage</span></span>      |

<span data-ttu-id="d2c55-151">Takto nastavíte rozsah informací.</span><span class="sxs-lookup"><span data-stu-id="d2c55-151">You set up the range information as follows.</span></span>

| <span data-ttu-id="d2c55-152">**Od hodnoty**</span><span class="sxs-lookup"><span data-stu-id="d2c55-152">**From value**</span></span> | <span data-ttu-id="d2c55-153">**Hodnota úroků**</span><span class="sxs-lookup"><span data-stu-id="d2c55-153">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="d2c55-154">0</span><span class="sxs-lookup"><span data-stu-id="d2c55-154">0</span></span>              | <span data-ttu-id="d2c55-155">1</span><span class="sxs-lookup"><span data-stu-id="d2c55-155">1</span></span>                  |
| <span data-ttu-id="d2c55-156">1,001</span><span class="sxs-lookup"><span data-stu-id="d2c55-156">1,001</span></span>          | <span data-ttu-id="d2c55-157">2</span><span class="sxs-lookup"><span data-stu-id="d2c55-157">2</span></span>                  |
| <span data-ttu-id="d2c55-158">5,001</span><span class="sxs-lookup"><span data-stu-id="d2c55-158">5,001</span></span>          | <span data-ttu-id="d2c55-159">3</span><span class="sxs-lookup"><span data-stu-id="d2c55-159">3</span></span>                  |

 
## <a name="example-2-interest-by-range--days"></a><span data-ttu-id="d2c55-160">Příklad 2: Úrok podle rozsahu = dny</span><span class="sxs-lookup"><span data-stu-id="d2c55-160">Example 2: Interest by range = Days</span></span>
--------------------------------------------------

<span data-ttu-id="d2c55-161">Nastavíte kód úroku, který přiřadí úrok jednou za každých 15 dnů, po které platba faktury překročí její splatnost.</span><span class="sxs-lookup"><span data-stu-id="d2c55-161">You set up an interest code that assesses interest one time for every 15 days that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="d2c55-162">Chcete založit výpočet na hodnotě částky úroku podle stupňovitých intervalů dnů.</span><span class="sxs-lookup"><span data-stu-id="d2c55-162">You want to base the calculation on an amount interest value, according to stepped day intervals.</span></span> <span data-ttu-id="d2c55-163">Hodnota úroku bude 10,00 za každých 15 dní během prvních 60 dnů, 15,00 za každých 15 dní od 61. do 90. dne a 20,00 za každých 15 dní od 91. dne.</span><span class="sxs-lookup"><span data-stu-id="d2c55-163">The interest value will be 10.00 per 15 days during the first 60 days, 15.00 per 15 days during days 61 to 90, and 20.00 per 15 days from day 91 and after.</span></span> <span data-ttu-id="d2c55-164">Hodnoty polí pro kód úroku nastavíte následovně.</span><span class="sxs-lookup"><span data-stu-id="d2c55-164">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="d2c55-165">**Název pole**</span><span class="sxs-lookup"><span data-stu-id="d2c55-165">**Field name**</span></span>                  | <span data-ttu-id="d2c55-166">**Hodnota pole**</span><span class="sxs-lookup"><span data-stu-id="d2c55-166">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="d2c55-167">**Kód úroku**</span><span class="sxs-lookup"><span data-stu-id="d2c55-167">**Interest code**</span></span>               | <span data-ttu-id="d2c55-168">15DAmtXDay</span><span class="sxs-lookup"><span data-stu-id="d2c55-168">15DAmtXDay</span></span>      |
| <span data-ttu-id="d2c55-169">**Vypočítat úroky jednou za**</span><span class="sxs-lookup"><span data-stu-id="d2c55-169">**Calculate interest every**</span></span>    | <span data-ttu-id="d2c55-170">15/den</span><span class="sxs-lookup"><span data-stu-id="d2c55-170">15/Day</span></span>          |
| <span data-ttu-id="d2c55-171">**Úrok podle rozsahu**</span><span class="sxs-lookup"><span data-stu-id="d2c55-171">**Interest by range**</span></span>           | <span data-ttu-id="d2c55-172">Dny</span><span class="sxs-lookup"><span data-stu-id="d2c55-172">Days</span></span>            |
| <span data-ttu-id="d2c55-173">**Vypočítat úrok podle**</span><span class="sxs-lookup"><span data-stu-id="d2c55-173">**Calculate interest based on**</span></span> | <span data-ttu-id="d2c55-174">Částka</span><span class="sxs-lookup"><span data-stu-id="d2c55-174">Amount</span></span>          |

<span data-ttu-id="d2c55-175">Takto nastavíte rozsah informací.</span><span class="sxs-lookup"><span data-stu-id="d2c55-175">You set up the range information as follows.</span></span>

| <span data-ttu-id="d2c55-176">**Od hodnoty**</span><span class="sxs-lookup"><span data-stu-id="d2c55-176">**From value**</span></span> | <span data-ttu-id="d2c55-177">**Hodnota úroků**</span><span class="sxs-lookup"><span data-stu-id="d2c55-177">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="d2c55-178">0</span><span class="sxs-lookup"><span data-stu-id="d2c55-178">0</span></span>              | <span data-ttu-id="d2c55-179">10</span><span class="sxs-lookup"><span data-stu-id="d2c55-179">10</span></span>                 |
| <span data-ttu-id="d2c55-180">61</span><span class="sxs-lookup"><span data-stu-id="d2c55-180">61</span></span>             | <span data-ttu-id="d2c55-181">15</span><span class="sxs-lookup"><span data-stu-id="d2c55-181">15</span></span>                 |
| <span data-ttu-id="d2c55-182">91</span><span class="sxs-lookup"><span data-stu-id="d2c55-182">91</span></span>             | <span data-ttu-id="d2c55-183">20</span><span class="sxs-lookup"><span data-stu-id="d2c55-183">20</span></span>                 |

 
## <a name="example-3-interest-by-range--months"></a><span data-ttu-id="d2c55-184">Příklad 3: Úrok podle rozsahu = měsíce</span><span class="sxs-lookup"><span data-stu-id="d2c55-184">Example 3: Interest by range = Months</span></span>
----------------------------------------------------

<span data-ttu-id="d2c55-185">Nastavíte kód úroku, který přiřadí úrok jednou za každý měsíc, po které platba faktury překročí její splatnost.</span><span class="sxs-lookup"><span data-stu-id="d2c55-185">You set up an interest code that assesses interest one time for every month that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="d2c55-186">Chcete založit výpočet na hodnotě úroku v procentech podle stupňovitých intervalů měsíců.</span><span class="sxs-lookup"><span data-stu-id="d2c55-186">You want to base the calculation on a percentage interest value, according to stepped month intervals.</span></span> <span data-ttu-id="d2c55-187">Hodnota úroků bude 1,5 % měsíčně za první tři měsíce po splatnosti, 2,0 % měsíčně za druhé tři měsíce a 2,5 % měsíčně za každý měsíc po prvních šesti měsících.</span><span class="sxs-lookup"><span data-stu-id="d2c55-187">The interest value will be 1.5 percent per month for the first three overdue months, 2.0 percent per month for the second three months, and 2.5 percent per month for each month beyond the first six months.</span></span> <span data-ttu-id="d2c55-188">Hodnoty polí pro kód úroku nastavíte následovně.</span><span class="sxs-lookup"><span data-stu-id="d2c55-188">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="d2c55-189">**Název pole**</span><span class="sxs-lookup"><span data-stu-id="d2c55-189">**Field name**</span></span>                  | <span data-ttu-id="d2c55-190">**Hodnota pole**</span><span class="sxs-lookup"><span data-stu-id="d2c55-190">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="d2c55-191">**Kód úroku**</span><span class="sxs-lookup"><span data-stu-id="d2c55-191">**Interest code**</span></span>               | <span data-ttu-id="d2c55-192">1M%ByMth</span><span class="sxs-lookup"><span data-stu-id="d2c55-192">1M%ByMth</span></span>        |
| <span data-ttu-id="d2c55-193">**Vypočítat úroky jednou za**</span><span class="sxs-lookup"><span data-stu-id="d2c55-193">**Calculate interest every**</span></span>    | <span data-ttu-id="d2c55-194">1/měsíc</span><span class="sxs-lookup"><span data-stu-id="d2c55-194">1/Month</span></span>         |
| <span data-ttu-id="d2c55-195">**Úrok podle rozsahu**</span><span class="sxs-lookup"><span data-stu-id="d2c55-195">**Interest by range**</span></span>           | <span data-ttu-id="d2c55-196">Měsíce</span><span class="sxs-lookup"><span data-stu-id="d2c55-196">Months</span></span>          |
| <span data-ttu-id="d2c55-197">**Vypočítat úrok podle**</span><span class="sxs-lookup"><span data-stu-id="d2c55-197">**Calculate interest based on**</span></span> | <span data-ttu-id="d2c55-198">Procento</span><span class="sxs-lookup"><span data-stu-id="d2c55-198">Percentage</span></span>      |

<span data-ttu-id="d2c55-199">Takto nastavíte rozsah informací.</span><span class="sxs-lookup"><span data-stu-id="d2c55-199">You set up the range information as follows.</span></span>

| <span data-ttu-id="d2c55-200">**Od hodnoty**</span><span class="sxs-lookup"><span data-stu-id="d2c55-200">**From value**</span></span> | <span data-ttu-id="d2c55-201">**Hodnota úroků**</span><span class="sxs-lookup"><span data-stu-id="d2c55-201">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="d2c55-202">0</span><span class="sxs-lookup"><span data-stu-id="d2c55-202">0</span></span>              | <span data-ttu-id="d2c55-203">1.5</span><span class="sxs-lookup"><span data-stu-id="d2c55-203">1.5</span></span>                |
| <span data-ttu-id="d2c55-204">4</span><span class="sxs-lookup"><span data-stu-id="d2c55-204">4</span></span>              | <span data-ttu-id="d2c55-205">2</span><span class="sxs-lookup"><span data-stu-id="d2c55-205">2</span></span>                  |
| <span data-ttu-id="d2c55-206">7</span><span class="sxs-lookup"><span data-stu-id="d2c55-206">7</span></span>              | <span data-ttu-id="d2c55-207">2,5</span><span class="sxs-lookup"><span data-stu-id="d2c55-207">2.5</span></span>                |

## <a name="new-versions"></a><span data-ttu-id="d2c55-208">Nové verze</span><span class="sxs-lookup"><span data-stu-id="d2c55-208">New versions</span></span>
<span data-ttu-id="d2c55-209">Kódy úroků mají časovou platnost.</span><span class="sxs-lookup"><span data-stu-id="d2c55-209">Interest codes are date effective.</span></span> <span data-ttu-id="d2c55-210">Pokud chcete upravit úrokové sazby, můžete vytvořit **novou verzi**, která bude účinná k budoucímu datu.</span><span class="sxs-lookup"><span data-stu-id="d2c55-210">If you want to modify the interest rate, you can create a **new version** that is effective as of a future date.</span></span>

<span data-ttu-id="d2c55-211">K zobrazení různých verzí můžete použít volbu nabídky **K datu** a vybrat koncové datum.</span><span class="sxs-lookup"><span data-stu-id="d2c55-211">To view different versions, you can use the **As of Date** menu choice to select the cutoff date.</span></span> <span data-ttu-id="d2c55-212">Také můžete výběrem možnosti **Zobrazit všechny záznamy** zobrazit na stránce všechny kódy úroků.</span><span class="sxs-lookup"><span data-stu-id="d2c55-212">You can also select the **Display all records** to view all interest codes in the page.</span></span>




