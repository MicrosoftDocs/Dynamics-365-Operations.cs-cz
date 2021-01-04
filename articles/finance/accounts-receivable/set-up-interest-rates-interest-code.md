---
title: Nastavení úrokových sazeb pro kód úroku
description: Kódy úroků obsahují nastavení, která určují, kdy bude placen úrok a jak se vypočítá na účtech po splatnosti.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Interest
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 59402
ms.assetid: 3b945333-1eaf-4658-ab5a-1a7791a7eb40
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a3ca43503ecbe8e814958576e46ced10bfe9ad49
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441056"
---
# <a name="set-up-interest-rates-for-an-interest-code"></a><span data-ttu-id="05ef9-103">Nastavení úrokových sazeb pro kód úroku</span><span class="sxs-lookup"><span data-stu-id="05ef9-103">Set up interest rates for an interest code</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="05ef9-104">Kódy úroků obsahují nastavení, která určují, kdy bude placen úrok a jak se vypočítá na účtech po splatnosti.</span><span class="sxs-lookup"><span data-stu-id="05ef9-104">Interest codes contain settings that determine when interest is charged and how it is calculated on overdue accounts.</span></span>

<span data-ttu-id="05ef9-105">Můžete nastavit jediný kód úroku a použít ho pro více účetních profilů zákazníků, účtovacích kódů nebo určité řady faktur.</span><span class="sxs-lookup"><span data-stu-id="05ef9-105">You can set up a single interest code and apply it to multiple customer posting profiles, billing codes, or to specific invoice lines.</span></span> <span data-ttu-id="05ef9-106">Při změně podrobností kódu úroku, všechny funkce, které používají kód automaticky implementují změny pro nové transakce.</span><span class="sxs-lookup"><span data-stu-id="05ef9-106">When the interest code details are changed, all features that use the code will automatically implement the changes on new transactions.</span></span> <span data-ttu-id="05ef9-107">Pro každý kód úroku můžete nastavit dva typy sazeb:</span><span class="sxs-lookup"><span data-stu-id="05ef9-107">For each interest code, you can set up two types of rates:</span></span>
-   <span data-ttu-id="05ef9-108">Sazby pro úrokové příjmy – představují výnosy, které jsou vytvořené účtováním úroků na fakturách nebo oznámeních úroků.</span><span class="sxs-lookup"><span data-stu-id="05ef9-108">Rates for interest earnings − These represent revenue that is earned by charging interest on invoices or interest notes.</span></span>
-   <span data-ttu-id="05ef9-109">Sazby pro úrokové platby − představují náklady zaplacené za úrok u dobropisů.</span><span class="sxs-lookup"><span data-stu-id="05ef9-109">Rates for interest payments − These represent a cost that is paid for interest on credit notes.</span></span>

<span data-ttu-id="05ef9-110">Oba tyto typy sazeb mohou existovat ve stejnou dobu a ve stejném kódu úroku.</span><span class="sxs-lookup"><span data-stu-id="05ef9-110">Both of these rate types can exist at the same time and in the same interest code.</span></span> <span data-ttu-id="05ef9-111">Úrokové sazby mohou být založeny na třech typech výpočtů:</span><span class="sxs-lookup"><span data-stu-id="05ef9-111">Interest rates can be based on three calculation types:</span></span>
-   <span data-ttu-id="05ef9-112">Úrok podle procent.</span><span class="sxs-lookup"><span data-stu-id="05ef9-112">Interest by percentage.</span></span>
-   <span data-ttu-id="05ef9-113">Úrok podle částky.</span><span class="sxs-lookup"><span data-stu-id="05ef9-113">Interest by amount.</span></span>
-   <span data-ttu-id="05ef9-114">Úrok podle rozsahu, jehož výsledkem je jednotná procentní sazba nebo částka.</span><span class="sxs-lookup"><span data-stu-id="05ef9-114">Interest by range, which results in a single percentage or amount.</span></span>

<span data-ttu-id="05ef9-115">Při použití kódu úroku, který se používá k výpočtu úroku, je pro každou úrokovou sazbu platnou v době, kdy platba překročila datum splatnosti transakce, vytvořeno samostatné oznámení úroků.</span><span class="sxs-lookup"><span data-stu-id="05ef9-115">When an interest code is used to calculate interest, a separate interest note is created for each interest rate that is in effect during the time that the payment has exceeded the transaction due date.</span></span> <span data-ttu-id="05ef9-116">K nastavení úrokových sazeb pro úroky, které můžete získat účtováním úroků, slouží karta **Zisky** na stránce **Kód úroku**.</span><span class="sxs-lookup"><span data-stu-id="05ef9-116">You use the **Earnings** tab on the **Interest code** page to set up interest rates for interest that you earn by charging interest.</span></span> <span data-ttu-id="05ef9-117">Na kartě **Platby** můžete nastavit úrokové sazby pro úroky, které platíte.</span><span class="sxs-lookup"><span data-stu-id="05ef9-117">Use the **Payments** tab to set up interest rates for interest that you pay.</span></span>

## <a name="interest-rates-based-on-a-percentage"></a><span data-ttu-id="05ef9-118">Úrokové sazby podle procent</span><span class="sxs-lookup"><span data-stu-id="05ef9-118">Interest rates based on a percentage</span></span>
<span data-ttu-id="05ef9-119">Můžete nastavit úrokové sazby pro výpočet zadané procentní hodnoty.</span><span class="sxs-lookup"><span data-stu-id="05ef9-119">You can set up interest rates that calculate a specified percentage.</span></span>

- <span data-ttu-id="05ef9-120">Částka úroku platí pro všechny měny.</span><span class="sxs-lookup"><span data-stu-id="05ef9-120">Interest amount applies to all currencies.</span></span>
- <span data-ttu-id="05ef9-121">Volitelně lze zadat omezení částky úroku.</span><span class="sxs-lookup"><span data-stu-id="05ef9-121">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="05ef9-122">Na stránce <strong>Nastavení kódů úroků**</strong> je v poli <strong>**Vypočítat úrok podle</strong> zvolena možnost <strong>Procento</strong>.</span><span class="sxs-lookup"><span data-stu-id="05ef9-122"><strong>Percentage</strong> is selected\*\* <strong>in the \*\*Calculate interest based on</strong> field on the <strong>Set up Interest codes</strong> page.</span></span>

<span data-ttu-id="05ef9-123">Pokud chcete například nastavit kód úroku, který stanoví 5% úrok po uplynutí každých dvou měsíců, kdy je faktura po splatnosti, zadejte do pole **Vypočítat úroky jednou za** hodnotu 2 a vyberte možnost **Měsíc**.</span><span class="sxs-lookup"><span data-stu-id="05ef9-123">For example, to set up an interest code that assesses 5 percent interest for every two months that the invoice payment exceeds the transaction due date, you would enter 2 in the **Calculate interest every** field and select **Month**.</span></span>

## <a name="interest-rates-based-on-amounts"></a><span data-ttu-id="05ef9-124">Úrokové sazby podle částek</span><span class="sxs-lookup"><span data-stu-id="05ef9-124">Interest rates based on amounts</span></span>
<span data-ttu-id="05ef9-125">Můžete nastavit úrokové sazby pro výpočet určité částky podle měny.</span><span class="sxs-lookup"><span data-stu-id="05ef9-125">You can set up interest rates that calculate a specified amount per currency.</span></span>
- <span data-ttu-id="05ef9-126">Částka úroku se zadává pro každou měnu v kódu úroku.</span><span class="sxs-lookup"><span data-stu-id="05ef9-126">An interest amount is specified for each currency in the interest code.</span></span>
- <span data-ttu-id="05ef9-127">Volitelně lze zadat omezení částky úroku.</span><span class="sxs-lookup"><span data-stu-id="05ef9-127">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="05ef9-128">Na stránce **Nastavení kódů úroků** je v poli **Vypočítat úrok podle** zvolena možnost **Částka**.</span><span class="sxs-lookup"><span data-stu-id="05ef9-128">**Amount** is selected in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="05ef9-129">Pokud chcete například nastavit kód úroku, který stanoví úrok 25,00 po uplynutí každých 20 dnů, kdy je faktura po splatnosti, zadejte do pole **Vypočítat úroky jednou za** hodnotu 20 a vyberte možnost **Den**.</span><span class="sxs-lookup"><span data-stu-id="05ef9-129">For example, to set up an interest code that assesses interest of 25.00 for every 20 days that the invoice payment exceeds the transaction due date, you would enter 20 in the **Calculate interest every** field and select **Day**.</span></span>

## <a name="interest-rates-based-on-ranges"></a><span data-ttu-id="05ef9-130">Úrokové sazby podle rozsahů</span><span class="sxs-lookup"><span data-stu-id="05ef9-130">Interest rates based on ranges</span></span>
<span data-ttu-id="05ef9-131">Můžete nastavit úrokové sazby, které jsou závislé na částce po splatnosti, počtu dní, po které je částka po splatnosti nebo počtu měsíců, po které je částka po splatnosti.</span><span class="sxs-lookup"><span data-stu-id="05ef9-131">You can set up interest rates that vary depending on the overdue amount, the number of days that the amount is late, or the number of months that the amount is late.</span></span>
-   <span data-ttu-id="05ef9-132">Na kartě **Zisky podle měny** můžete určit specifické nastavení úroků pro každou měnu.</span><span class="sxs-lookup"><span data-stu-id="05ef9-132">You can use the **Earnings by Currency** tab to define specific interest settings for each currency.</span></span> <span data-ttu-id="05ef9-133">Na stejném místě se určuje také rozsah.</span><span class="sxs-lookup"><span data-stu-id="05ef9-133">This is also where you will define the range.</span></span>
-   <span data-ttu-id="05ef9-134">K přidání řádků, které představují rozsahy, které chcete nastavit, použijte tlačítko **Rozsahy**.</span><span class="sxs-lookup"><span data-stu-id="05ef9-134">Use the **Ranges** button to add lines that represent the ranges that you want to set up.</span></span> <span data-ttu-id="05ef9-135">Hodnota **Od** představuje začátek rozsahu a číslo **Hodnota úroků** představuje procento nebo částku (podle výběru provedeného v poli **Vypočítat úrok podle** na stránce **Nastavení kódů úroku**).</span><span class="sxs-lookup"><span data-stu-id="05ef9-135">The **From** value represents the beginning of the range and the **Interest value** number represents either a percentage or an amount, depending on the selection in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

## <a name="example-1-interest-by-range--amount"></a><span data-ttu-id="05ef9-136">Příklad 1: Úroky podle rozsahu = částka</span><span class="sxs-lookup"><span data-stu-id="05ef9-136">Example 1: Interest by range = Amount</span></span>
<span data-ttu-id="05ef9-137">Nastavíte kód úroku, který přiřadí úrok jednou za každé tři měsíce, po které platba faktury překročí její splatnost.</span><span class="sxs-lookup"><span data-stu-id="05ef9-137">You set up an interest code that assesses interest one time for every three months that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="05ef9-138">Chcete založit výpočet na hodnotě úroku v procentech podle stupňovitých intervalů částky.</span><span class="sxs-lookup"><span data-stu-id="05ef9-138">You want to base the calculation on a percentage interest value, according to stepped amount intervals.</span></span> <span data-ttu-id="05ef9-139">Hodnota úroku bude 1 % pro fakturační částky do 1 000,00, 2 procenta pro částky od 1 001,00 do 5 000,00 a 3 % pro částky větší než 5 000,00.</span><span class="sxs-lookup"><span data-stu-id="05ef9-139">The interest value will be 1 percent for invoice amounts up to 1,000.00, 2 percent for amounts from 1,001.00 to 5,000.00, and 3 percent for amounts larger than 5,000.00.</span></span> <span data-ttu-id="05ef9-140">Hodnoty polí pro kód úroku nastavíte následovně.</span><span class="sxs-lookup"><span data-stu-id="05ef9-140">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="05ef9-141">**Název pole**</span><span class="sxs-lookup"><span data-stu-id="05ef9-141">**Field name**</span></span>                  | <span data-ttu-id="05ef9-142">**Hodnota pole**</span><span class="sxs-lookup"><span data-stu-id="05ef9-142">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="05ef9-143">**Kód úroku**</span><span class="sxs-lookup"><span data-stu-id="05ef9-143">**Interest code**</span></span>               | <span data-ttu-id="05ef9-144">3M%ByAmt</span><span class="sxs-lookup"><span data-stu-id="05ef9-144">3M%ByAmt</span></span>        |
| <span data-ttu-id="05ef9-145">**Vypočítat úroky jednou za**</span><span class="sxs-lookup"><span data-stu-id="05ef9-145">**Calculate interest every**</span></span>    | <span data-ttu-id="05ef9-146">3/měsíc</span><span class="sxs-lookup"><span data-stu-id="05ef9-146">3/Month</span></span>         |
| <span data-ttu-id="05ef9-147">**Úrok podle rozsahu**</span><span class="sxs-lookup"><span data-stu-id="05ef9-147">**Interest by range**</span></span>           | <span data-ttu-id="05ef9-148">Částka</span><span class="sxs-lookup"><span data-stu-id="05ef9-148">Amount</span></span>          |
| <span data-ttu-id="05ef9-149">**Vypočítat úrok podle**</span><span class="sxs-lookup"><span data-stu-id="05ef9-149">**Calculate interest based on**</span></span> | <span data-ttu-id="05ef9-150">Procento</span><span class="sxs-lookup"><span data-stu-id="05ef9-150">Percentage</span></span>      |

<span data-ttu-id="05ef9-151">Takto nastavíte rozsah informací.</span><span class="sxs-lookup"><span data-stu-id="05ef9-151">You set up the range information as follows.</span></span>

| <span data-ttu-id="05ef9-152">**Od hodnoty**</span><span class="sxs-lookup"><span data-stu-id="05ef9-152">**From value**</span></span> | <span data-ttu-id="05ef9-153">**Hodnota úroků**</span><span class="sxs-lookup"><span data-stu-id="05ef9-153">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="05ef9-154">0</span><span class="sxs-lookup"><span data-stu-id="05ef9-154">0</span></span>              | <span data-ttu-id="05ef9-155">1</span><span class="sxs-lookup"><span data-stu-id="05ef9-155">1</span></span>                  |
| <span data-ttu-id="05ef9-156">1,001</span><span class="sxs-lookup"><span data-stu-id="05ef9-156">1,001</span></span>          | <span data-ttu-id="05ef9-157">2</span><span class="sxs-lookup"><span data-stu-id="05ef9-157">2</span></span>                  |
| <span data-ttu-id="05ef9-158">5,001</span><span class="sxs-lookup"><span data-stu-id="05ef9-158">5,001</span></span>          | <span data-ttu-id="05ef9-159">3</span><span class="sxs-lookup"><span data-stu-id="05ef9-159">3</span></span>                  |


## <a name="example-2-interest-by-range--days"></a><span data-ttu-id="05ef9-160">Příklad 2: Úrok podle rozsahu = dny</span><span class="sxs-lookup"><span data-stu-id="05ef9-160">Example 2: Interest by range = Days</span></span>
--------------------------------------------------

<span data-ttu-id="05ef9-161">Nastavíte kód úroku, který přiřadí úrok jednou za každých 15 dnů, po které platba faktury překročí její splatnost.</span><span class="sxs-lookup"><span data-stu-id="05ef9-161">You set up an interest code that assesses interest one time for every 15 days that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="05ef9-162">Chcete založit výpočet na hodnotě částky úroku podle stupňovitých intervalů dnů.</span><span class="sxs-lookup"><span data-stu-id="05ef9-162">You want to base the calculation on an amount interest value, according to stepped day intervals.</span></span> <span data-ttu-id="05ef9-163">Hodnota úroku bude 10,00 za každých 15 dní během prvních 60 dnů, 15,00 za každých 15 dní od 61. do 90. dne a 20,00 za každých 15 dní od 91. dne.</span><span class="sxs-lookup"><span data-stu-id="05ef9-163">The interest value will be 10.00 per 15 days during the first 60 days, 15.00 per 15 days during days 61 to 90, and 20.00 per 15 days from day 91 and after.</span></span> <span data-ttu-id="05ef9-164">Hodnoty polí pro kód úroku nastavíte následovně.</span><span class="sxs-lookup"><span data-stu-id="05ef9-164">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="05ef9-165">**Název pole**</span><span class="sxs-lookup"><span data-stu-id="05ef9-165">**Field name**</span></span>                  | <span data-ttu-id="05ef9-166">**Hodnota pole**</span><span class="sxs-lookup"><span data-stu-id="05ef9-166">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="05ef9-167">**Kód úroku**</span><span class="sxs-lookup"><span data-stu-id="05ef9-167">**Interest code**</span></span>               | <span data-ttu-id="05ef9-168">15DAmtXDay</span><span class="sxs-lookup"><span data-stu-id="05ef9-168">15DAmtXDay</span></span>      |
| <span data-ttu-id="05ef9-169">**Vypočítat úroky jednou za**</span><span class="sxs-lookup"><span data-stu-id="05ef9-169">**Calculate interest every**</span></span>    | <span data-ttu-id="05ef9-170">15/den</span><span class="sxs-lookup"><span data-stu-id="05ef9-170">15/Day</span></span>          |
| <span data-ttu-id="05ef9-171">**Úrok podle rozsahu**</span><span class="sxs-lookup"><span data-stu-id="05ef9-171">**Interest by range**</span></span>           | <span data-ttu-id="05ef9-172">Dny</span><span class="sxs-lookup"><span data-stu-id="05ef9-172">Days</span></span>            |
| <span data-ttu-id="05ef9-173">**Vypočítat úrok podle**</span><span class="sxs-lookup"><span data-stu-id="05ef9-173">**Calculate interest based on**</span></span> | <span data-ttu-id="05ef9-174">Částka</span><span class="sxs-lookup"><span data-stu-id="05ef9-174">Amount</span></span>          |

<span data-ttu-id="05ef9-175">Takto nastavíte rozsah informací.</span><span class="sxs-lookup"><span data-stu-id="05ef9-175">You set up the range information as follows.</span></span>

| <span data-ttu-id="05ef9-176">**Od hodnoty**</span><span class="sxs-lookup"><span data-stu-id="05ef9-176">**From value**</span></span> | <span data-ttu-id="05ef9-177">**Hodnota úroků**</span><span class="sxs-lookup"><span data-stu-id="05ef9-177">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="05ef9-178">0</span><span class="sxs-lookup"><span data-stu-id="05ef9-178">0</span></span>              | <span data-ttu-id="05ef9-179">10</span><span class="sxs-lookup"><span data-stu-id="05ef9-179">10</span></span>                 |
| <span data-ttu-id="05ef9-180">61</span><span class="sxs-lookup"><span data-stu-id="05ef9-180">61</span></span>             | <span data-ttu-id="05ef9-181">15</span><span class="sxs-lookup"><span data-stu-id="05ef9-181">15</span></span>                 |
| <span data-ttu-id="05ef9-182">91</span><span class="sxs-lookup"><span data-stu-id="05ef9-182">91</span></span>             | <span data-ttu-id="05ef9-183">20</span><span class="sxs-lookup"><span data-stu-id="05ef9-183">20</span></span>                 |


## <a name="example-3-interest-by-range--months"></a><span data-ttu-id="05ef9-184">Příklad 3: Úrok podle rozsahu = měsíce</span><span class="sxs-lookup"><span data-stu-id="05ef9-184">Example 3: Interest by range = Months</span></span>
----------------------------------------------------

<span data-ttu-id="05ef9-185">Nastavíte kód úroku, který přiřadí úrok jednou za každý měsíc, po které platba faktury překročí její splatnost.</span><span class="sxs-lookup"><span data-stu-id="05ef9-185">You set up an interest code that assesses interest one time for every month that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="05ef9-186">Chcete založit výpočet na hodnotě úroku v procentech podle stupňovitých intervalů měsíců.</span><span class="sxs-lookup"><span data-stu-id="05ef9-186">You want to base the calculation on a percentage interest value, according to stepped month intervals.</span></span> <span data-ttu-id="05ef9-187">Hodnota úroků bude 1,5 % měsíčně za první tři měsíce po splatnosti, 2,0 % měsíčně za druhé tři měsíce a 2,5 % měsíčně za každý měsíc po prvních šesti měsících.</span><span class="sxs-lookup"><span data-stu-id="05ef9-187">The interest value will be 1.5 percent per month for the first three overdue months, 2.0 percent per month for the second three months, and 2.5 percent per month for each month beyond the first six months.</span></span> <span data-ttu-id="05ef9-188">Hodnoty polí pro kód úroku nastavíte následovně.</span><span class="sxs-lookup"><span data-stu-id="05ef9-188">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="05ef9-189">**Název pole**</span><span class="sxs-lookup"><span data-stu-id="05ef9-189">**Field name**</span></span>                  | <span data-ttu-id="05ef9-190">**Hodnota pole**</span><span class="sxs-lookup"><span data-stu-id="05ef9-190">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="05ef9-191">**Kód úroku**</span><span class="sxs-lookup"><span data-stu-id="05ef9-191">**Interest code**</span></span>               | <span data-ttu-id="05ef9-192">1M%ByMth</span><span class="sxs-lookup"><span data-stu-id="05ef9-192">1M%ByMth</span></span>        |
| <span data-ttu-id="05ef9-193">**Vypočítat úroky jednou za**</span><span class="sxs-lookup"><span data-stu-id="05ef9-193">**Calculate interest every**</span></span>    | <span data-ttu-id="05ef9-194">1/měsíc</span><span class="sxs-lookup"><span data-stu-id="05ef9-194">1/Month</span></span>         |
| <span data-ttu-id="05ef9-195">**Úrok podle rozsahu**</span><span class="sxs-lookup"><span data-stu-id="05ef9-195">**Interest by range**</span></span>           | <span data-ttu-id="05ef9-196">Měsíce</span><span class="sxs-lookup"><span data-stu-id="05ef9-196">Months</span></span>          |
| <span data-ttu-id="05ef9-197">**Vypočítat úrok podle**</span><span class="sxs-lookup"><span data-stu-id="05ef9-197">**Calculate interest based on**</span></span> | <span data-ttu-id="05ef9-198">Procento</span><span class="sxs-lookup"><span data-stu-id="05ef9-198">Percentage</span></span>      |

<span data-ttu-id="05ef9-199">Takto nastavíte rozsah informací.</span><span class="sxs-lookup"><span data-stu-id="05ef9-199">You set up the range information as follows.</span></span>

| <span data-ttu-id="05ef9-200">**Od hodnoty**</span><span class="sxs-lookup"><span data-stu-id="05ef9-200">**From value**</span></span> | <span data-ttu-id="05ef9-201">**Hodnota úroků**</span><span class="sxs-lookup"><span data-stu-id="05ef9-201">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="05ef9-202">0</span><span class="sxs-lookup"><span data-stu-id="05ef9-202">0</span></span>              | <span data-ttu-id="05ef9-203">1.5</span><span class="sxs-lookup"><span data-stu-id="05ef9-203">1.5</span></span>                |
| <span data-ttu-id="05ef9-204">4</span><span class="sxs-lookup"><span data-stu-id="05ef9-204">4</span></span>              | <span data-ttu-id="05ef9-205">2</span><span class="sxs-lookup"><span data-stu-id="05ef9-205">2</span></span>                  |
| <span data-ttu-id="05ef9-206">7</span><span class="sxs-lookup"><span data-stu-id="05ef9-206">7</span></span>              | <span data-ttu-id="05ef9-207">2,5</span><span class="sxs-lookup"><span data-stu-id="05ef9-207">2.5</span></span>                |

## <a name="new-versions"></a><span data-ttu-id="05ef9-208">Nové verze</span><span class="sxs-lookup"><span data-stu-id="05ef9-208">New versions</span></span>
<span data-ttu-id="05ef9-209">Kódy úroků mají časovou platnost.</span><span class="sxs-lookup"><span data-stu-id="05ef9-209">Interest codes are date effective.</span></span> <span data-ttu-id="05ef9-210">Pokud chcete upravit úrokové sazby, můžete vytvořit **novou verzi**, která bude účinná k budoucímu datu.</span><span class="sxs-lookup"><span data-stu-id="05ef9-210">If you want to modify the interest rate, you can create a **new version** that is effective as of a future date.</span></span>

<span data-ttu-id="05ef9-211">K zobrazení různých verzí můžete použít volbu nabídky **K datu** a vybrat koncové datum.</span><span class="sxs-lookup"><span data-stu-id="05ef9-211">To view different versions, you can use the **As of Date** menu choice to select the cutoff date.</span></span> <span data-ttu-id="05ef9-212">Také můžete výběrem možnosti **Zobrazit všechny záznamy** zobrazit na stránce všechny kódy úroků.</span><span class="sxs-lookup"><span data-stu-id="05ef9-212">You can also select the **Display all records** to view all interest codes in the page.</span></span>



