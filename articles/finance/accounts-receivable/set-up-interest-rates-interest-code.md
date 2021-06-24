---
title: Nastavení úrokových sazeb pro kód úroku
description: Kódy úroků obsahují nastavení, která určují, kdy bude placen úrok a jak se vypočítá na účtech po splatnosti.
author: ShivamPandey-msft
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Interest
audience: Application User
ms.reviewer: roschlom
ms.custom: 59402
ms.assetid: 3b945333-1eaf-4658-ab5a-1a7791a7eb40
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fc986ea752d1482f618401058f7a0b18f13efd5f
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/04/2021
ms.locfileid: "6188703"
---
# <a name="set-up-interest-rates-for-an-interest-code"></a><span data-ttu-id="8d1fa-103">Nastavení úrokových sazeb pro kód úroku</span><span class="sxs-lookup"><span data-stu-id="8d1fa-103">Set up interest rates for an interest code</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8d1fa-104">Kódy úroků obsahují nastavení, která určují, kdy bude placen úrok a jak se vypočítá na účtech po splatnosti.</span><span class="sxs-lookup"><span data-stu-id="8d1fa-104">Interest codes contain settings that determine when interest is charged and how it is calculated on overdue accounts.</span></span>

<span data-ttu-id="8d1fa-105">Můžete nastavit jediný kód úroku a použít ho pro více účetních profilů zákazníků, účtovacích kódů nebo určité řady faktur.</span><span class="sxs-lookup"><span data-stu-id="8d1fa-105">You can set up a single interest code and apply it to multiple customer posting profiles, billing codes, or to specific invoice lines.</span></span> <span data-ttu-id="8d1fa-106">Při změně podrobností kódu úroku, všechny funkce, které používají kód automaticky implementují změny pro nové transakce.</span><span class="sxs-lookup"><span data-stu-id="8d1fa-106">When the interest code details are changed, all features that use the code will automatically implement the changes on new transactions.</span></span> <span data-ttu-id="8d1fa-107">Pro každý kód úroku můžete nastavit dva typy sazeb:</span><span class="sxs-lookup"><span data-stu-id="8d1fa-107">For each interest code, you can set up two types of rates:</span></span>
-   <span data-ttu-id="8d1fa-108">Sazby pro úrokové příjmy – představují výnosy, které jsou vytvořené účtováním úroků na fakturách nebo oznámeních úroků.</span><span class="sxs-lookup"><span data-stu-id="8d1fa-108">Rates for interest earnings − These represent revenue that is earned by charging interest on invoices or interest notes.</span></span>
-   <span data-ttu-id="8d1fa-109">Sazby pro úrokové platby − představují náklady zaplacené za úrok u dobropisů.</span><span class="sxs-lookup"><span data-stu-id="8d1fa-109">Rates for interest payments − These represent a cost that is paid for interest on credit notes.</span></span>

<span data-ttu-id="8d1fa-110">Oba tyto typy sazeb mohou existovat ve stejnou dobu a ve stejném kódu úroku.</span><span class="sxs-lookup"><span data-stu-id="8d1fa-110">Both of these rate types can exist at the same time and in the same interest code.</span></span> <span data-ttu-id="8d1fa-111">Úrokové sazby mohou být založeny na třech typech výpočtů:</span><span class="sxs-lookup"><span data-stu-id="8d1fa-111">Interest rates can be based on three calculation types:</span></span>
-   <span data-ttu-id="8d1fa-112">Úrok podle procent.</span><span class="sxs-lookup"><span data-stu-id="8d1fa-112">Interest by percentage.</span></span>
-   <span data-ttu-id="8d1fa-113">Úrok podle částky.</span><span class="sxs-lookup"><span data-stu-id="8d1fa-113">Interest by amount.</span></span>
-   <span data-ttu-id="8d1fa-114">Úrok podle rozsahu, jehož výsledkem je jednotná procentní sazba nebo částka.</span><span class="sxs-lookup"><span data-stu-id="8d1fa-114">Interest by range, which results in a single percentage or amount.</span></span>

<span data-ttu-id="8d1fa-115">Při použití kódu úroku, který se používá k výpočtu úroku, je pro každou úrokovou sazbu platnou v době, kdy platba překročila datum splatnosti transakce, vytvořeno samostatné oznámení úroků.</span><span class="sxs-lookup"><span data-stu-id="8d1fa-115">When an interest code is used to calculate interest, a separate interest note is created for each interest rate that is in effect during the time that the payment has exceeded the transaction due date.</span></span> <span data-ttu-id="8d1fa-116">K nastavení úrokových sazeb pro úroky, které můžete získat účtováním úroků, slouží karta **Zisky** na stránce **Kód úroku**.</span><span class="sxs-lookup"><span data-stu-id="8d1fa-116">You use the **Earnings** tab on the **Interest code** page to set up interest rates for interest that you earn by charging interest.</span></span> <span data-ttu-id="8d1fa-117">Na kartě **Platby** můžete nastavit úrokové sazby pro úroky, které platíte.</span><span class="sxs-lookup"><span data-stu-id="8d1fa-117">Use the **Payments** tab to set up interest rates for interest that you pay.</span></span>

## <a name="interest-rates-based-on-a-percentage"></a><span data-ttu-id="8d1fa-118">Úrokové sazby podle procent</span><span class="sxs-lookup"><span data-stu-id="8d1fa-118">Interest rates based on a percentage</span></span>
<span data-ttu-id="8d1fa-119">Můžete nastavit úrokové sazby pro výpočet zadané procentní hodnoty.</span><span class="sxs-lookup"><span data-stu-id="8d1fa-119">You can set up interest rates that calculate a specified percentage.</span></span>

- <span data-ttu-id="8d1fa-120">Částka úroku platí pro všechny měny.</span><span class="sxs-lookup"><span data-stu-id="8d1fa-120">Interest amount applies to all currencies.</span></span>
- <span data-ttu-id="8d1fa-121">Volitelně lze zadat omezení částky úroku.</span><span class="sxs-lookup"><span data-stu-id="8d1fa-121">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="8d1fa-122">Na stránce **Nastavení kódů úroků** je v poli **Vypočítat úrok podle** zvolena možnost **Procento**.</span><span class="sxs-lookup"><span data-stu-id="8d1fa-122">**Percentage** is selected in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="8d1fa-123">Pokud chcete například nastavit kód úroku, který stanoví 5% úrok po uplynutí každých dvou měsíců, kdy je faktura po splatnosti, zadejte do pole **Vypočítat úroky jednou za** hodnotu 2 a vyberte možnost **Měsíc**.</span><span class="sxs-lookup"><span data-stu-id="8d1fa-123">For example, to set up an interest code that assesses 5 percent interest for every two months that the invoice payment exceeds the transaction due date, you would enter 2 in the **Calculate interest every** field and select **Month**.</span></span>

> [!NOTE] 
> <span data-ttu-id="8d1fa-124">Nový algoritmus pro výpočet oznámení úroků je přidán pomocí správy funkcí.</span><span class="sxs-lookup"><span data-stu-id="8d1fa-124">The new algorithm for interest note calculation is added using Feature management.</span></span> <span data-ttu-id="8d1fa-125">Chcete-li použít tento algoritmus, povolte vlastnost **(GBL) Umožnit vypočítat úrok za den jako roční procento vydělené 365**.</span><span class="sxs-lookup"><span data-stu-id="8d1fa-125">To use this algorithm, enable the **(GBL) Allow to calculate interest per day as yearly percent divided by 365** feature.</span></span> <span data-ttu-id="8d1fa-126">Další informace o povolování funkcí naleznete v tématu [Přehled správy funkcí](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8d1fa-126">For information about how to enable the feature, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
> 
> <span data-ttu-id="8d1fa-127">Vzorec pro výpočet výše částky úroku je:</span><span class="sxs-lookup"><span data-stu-id="8d1fa-127">The formula for the calculation for the interest note amount is:</span></span> 
>  
> <span data-ttu-id="8d1fa-128">Výše oznámení o úroku = dlužná částka × roční úrok % / 365 × počet dní zpodění</span><span class="sxs-lookup"><span data-stu-id="8d1fa-128">Interest note amount = Amount owed \* Yearly interest % / 365 \* Number of days late</span></span>
>  
> <span data-ttu-id="8d1fa-129">Tato funkce je k dispozici ve verzi 10.0.18 a novější.</span><span class="sxs-lookup"><span data-stu-id="8d1fa-129">This feature is available in version 10.0.18 or later.</span></span>    
 
## <a name="interest-rates-based-on-amounts"></a><span data-ttu-id="8d1fa-130">Úrokové sazby podle částek</span><span class="sxs-lookup"><span data-stu-id="8d1fa-130">Interest rates based on amounts</span></span>
<span data-ttu-id="8d1fa-131">Můžete nastavit úrokové sazby pro výpočet určité částky podle měny.</span><span class="sxs-lookup"><span data-stu-id="8d1fa-131">You can set up interest rates that calculate a specified amount per currency.</span></span>
- <span data-ttu-id="8d1fa-132">Částka úroku se zadává pro každou měnu v kódu úroku.</span><span class="sxs-lookup"><span data-stu-id="8d1fa-132">An interest amount is specified for each currency in the interest code.</span></span>
- <span data-ttu-id="8d1fa-133">Volitelně lze zadat omezení částky úroku.</span><span class="sxs-lookup"><span data-stu-id="8d1fa-133">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="8d1fa-134">Na stránce **Nastavení kódů úroků** je v poli **Vypočítat úrok podle** zvolena možnost **Částka**.</span><span class="sxs-lookup"><span data-stu-id="8d1fa-134">**Amount** is selected in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="8d1fa-135">Pokud chcete například nastavit kód úroku, který stanoví úrok 25,00 po uplynutí každých 20 dnů, kdy je faktura po splatnosti, zadejte do pole **Vypočítat úroky jednou za** hodnotu 20 a vyberte možnost **Den**.</span><span class="sxs-lookup"><span data-stu-id="8d1fa-135">For example, to set up an interest code that assesses interest of 25.00 for every 20 days that the invoice payment exceeds the transaction due date, you would enter 20 in the **Calculate interest every** field and select **Day**.</span></span>

## <a name="interest-rates-based-on-ranges"></a><span data-ttu-id="8d1fa-136">Úrokové sazby podle rozsahů</span><span class="sxs-lookup"><span data-stu-id="8d1fa-136">Interest rates based on ranges</span></span>
<span data-ttu-id="8d1fa-137">Můžete nastavit úrokové sazby, které jsou závislé na částce po splatnosti, počtu dní, po které je částka po splatnosti nebo počtu měsíců, po které je částka po splatnosti.</span><span class="sxs-lookup"><span data-stu-id="8d1fa-137">You can set up interest rates that vary depending on the overdue amount, the number of days that the amount is late, or the number of months that the amount is late.</span></span>
-   <span data-ttu-id="8d1fa-138">Na kartě **Zisky podle měny** můžete určit specifické nastavení úroků pro každou měnu.</span><span class="sxs-lookup"><span data-stu-id="8d1fa-138">You can use the **Earnings by Currency** tab to define specific interest settings for each currency.</span></span> <span data-ttu-id="8d1fa-139">Na stejném místě se určuje také rozsah.</span><span class="sxs-lookup"><span data-stu-id="8d1fa-139">This is also where you will define the range.</span></span>
-   <span data-ttu-id="8d1fa-140">K přidání řádků, které představují rozsahy, které chcete nastavit, použijte tlačítko **Rozsahy**.</span><span class="sxs-lookup"><span data-stu-id="8d1fa-140">Use the **Ranges** button to add lines that represent the ranges that you want to set up.</span></span> <span data-ttu-id="8d1fa-141">Hodnota **Od** představuje začátek rozsahu a číslo **Hodnota úroků** představuje procento nebo částku (podle výběru provedeného v poli **Vypočítat úrok podle** na stránce **Nastavení kódů úroku**).</span><span class="sxs-lookup"><span data-stu-id="8d1fa-141">The **From** value represents the beginning of the range and the **Interest value** number represents either a percentage or an amount, depending on the selection in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

## <a name="example-1-interest-by-range--amount"></a><span data-ttu-id="8d1fa-142">Příklad 1: Úroky podle rozsahu = částka</span><span class="sxs-lookup"><span data-stu-id="8d1fa-142">Example 1: Interest by range = Amount</span></span>
<span data-ttu-id="8d1fa-143">Nastavíte kód úroku, který přiřadí úrok jednou za každé tři měsíce, po které platba faktury překročí její splatnost.</span><span class="sxs-lookup"><span data-stu-id="8d1fa-143">You set up an interest code that assesses interest one time for every three months that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="8d1fa-144">Chcete založit výpočet na hodnotě úroku v procentech podle stupňovitých intervalů částky.</span><span class="sxs-lookup"><span data-stu-id="8d1fa-144">You want to base the calculation on a percentage interest value, according to stepped amount intervals.</span></span> <span data-ttu-id="8d1fa-145">Hodnota úroku bude 1 % pro fakturační částky do 1 000,00, 2 procenta pro částky od 1 001,00 do 5 000,00 a 3 % pro částky větší než 5 000,00.</span><span class="sxs-lookup"><span data-stu-id="8d1fa-145">The interest value will be 1 percent for invoice amounts up to 1,000.00, 2 percent for amounts from 1,001.00 to 5,000.00, and 3 percent for amounts larger than 5,000.00.</span></span> <span data-ttu-id="8d1fa-146">Hodnoty polí pro kód úroku nastavíte následovně.</span><span class="sxs-lookup"><span data-stu-id="8d1fa-146">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="8d1fa-147">**Název pole**</span><span class="sxs-lookup"><span data-stu-id="8d1fa-147">**Field name**</span></span>                  | <span data-ttu-id="8d1fa-148">**Hodnota pole**</span><span class="sxs-lookup"><span data-stu-id="8d1fa-148">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="8d1fa-149">**Kód úroku**</span><span class="sxs-lookup"><span data-stu-id="8d1fa-149">**Interest code**</span></span>               | <span data-ttu-id="8d1fa-150">3M%ByAmt</span><span class="sxs-lookup"><span data-stu-id="8d1fa-150">3M%ByAmt</span></span>        |
| <span data-ttu-id="8d1fa-151">**Vypočítat úroky jednou za**</span><span class="sxs-lookup"><span data-stu-id="8d1fa-151">**Calculate interest every**</span></span>    | <span data-ttu-id="8d1fa-152">3/měsíc</span><span class="sxs-lookup"><span data-stu-id="8d1fa-152">3/Month</span></span>         |
| <span data-ttu-id="8d1fa-153">**Úrok podle rozsahu**</span><span class="sxs-lookup"><span data-stu-id="8d1fa-153">**Interest by range**</span></span>           | <span data-ttu-id="8d1fa-154">Částka</span><span class="sxs-lookup"><span data-stu-id="8d1fa-154">Amount</span></span>          |
| <span data-ttu-id="8d1fa-155">**Vypočítat úrok podle**</span><span class="sxs-lookup"><span data-stu-id="8d1fa-155">**Calculate interest based on**</span></span> | <span data-ttu-id="8d1fa-156">Procento</span><span class="sxs-lookup"><span data-stu-id="8d1fa-156">Percentage</span></span>      |

<span data-ttu-id="8d1fa-157">Takto nastavíte rozsah informací.</span><span class="sxs-lookup"><span data-stu-id="8d1fa-157">You set up the range information as follows.</span></span>

| <span data-ttu-id="8d1fa-158">**Od hodnoty**</span><span class="sxs-lookup"><span data-stu-id="8d1fa-158">**From value**</span></span> | <span data-ttu-id="8d1fa-159">**Hodnota úroků**</span><span class="sxs-lookup"><span data-stu-id="8d1fa-159">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="8d1fa-160">0</span><span class="sxs-lookup"><span data-stu-id="8d1fa-160">0</span></span>              | <span data-ttu-id="8d1fa-161">1</span><span class="sxs-lookup"><span data-stu-id="8d1fa-161">1</span></span>                  |
| <span data-ttu-id="8d1fa-162">1,001</span><span class="sxs-lookup"><span data-stu-id="8d1fa-162">1,001</span></span>          | <span data-ttu-id="8d1fa-163">2</span><span class="sxs-lookup"><span data-stu-id="8d1fa-163">2</span></span>                  |
| <span data-ttu-id="8d1fa-164">5,001</span><span class="sxs-lookup"><span data-stu-id="8d1fa-164">5,001</span></span>          | <span data-ttu-id="8d1fa-165">3</span><span class="sxs-lookup"><span data-stu-id="8d1fa-165">3</span></span>                  |


## <a name="example-2-interest-by-range--days"></a><span data-ttu-id="8d1fa-166">Příklad 2: Úrok podle rozsahu = dny</span><span class="sxs-lookup"><span data-stu-id="8d1fa-166">Example 2: Interest by range = Days</span></span>

<span data-ttu-id="8d1fa-167">Nastavíte kód úroku, který přiřadí úrok jednou za každých 15 dnů, po které platba faktury překročí její splatnost.</span><span class="sxs-lookup"><span data-stu-id="8d1fa-167">You set up an interest code that assesses interest one time for every 15 days that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="8d1fa-168">Chcete založit výpočet na hodnotě částky úroku podle stupňovitých intervalů dnů.</span><span class="sxs-lookup"><span data-stu-id="8d1fa-168">You want to base the calculation on an amount interest value, according to stepped day intervals.</span></span> <span data-ttu-id="8d1fa-169">Hodnota úroku bude 10,00 za každých 15 dní během prvních 60 dnů, 15,00 za každých 15 dní od 61. do 90. dne a 20,00 za každých 15 dní od 91. dne.</span><span class="sxs-lookup"><span data-stu-id="8d1fa-169">The interest value will be 10.00 per 15 days during the first 60 days, 15.00 per 15 days during days 61 to 90, and 20.00 per 15 days from day 91 and after.</span></span> <span data-ttu-id="8d1fa-170">Hodnoty polí pro kód úroku nastavíte následovně.</span><span class="sxs-lookup"><span data-stu-id="8d1fa-170">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="8d1fa-171">**Název pole**</span><span class="sxs-lookup"><span data-stu-id="8d1fa-171">**Field name**</span></span>                  | <span data-ttu-id="8d1fa-172">**Hodnota pole**</span><span class="sxs-lookup"><span data-stu-id="8d1fa-172">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="8d1fa-173">**Kód úroku**</span><span class="sxs-lookup"><span data-stu-id="8d1fa-173">**Interest code**</span></span>               | <span data-ttu-id="8d1fa-174">15DAmtXDay</span><span class="sxs-lookup"><span data-stu-id="8d1fa-174">15DAmtXDay</span></span>      |
| <span data-ttu-id="8d1fa-175">**Vypočítat úroky jednou za**</span><span class="sxs-lookup"><span data-stu-id="8d1fa-175">**Calculate interest every**</span></span>    | <span data-ttu-id="8d1fa-176">15/den</span><span class="sxs-lookup"><span data-stu-id="8d1fa-176">15/Day</span></span>          |
| <span data-ttu-id="8d1fa-177">**Úrok podle rozsahu**</span><span class="sxs-lookup"><span data-stu-id="8d1fa-177">**Interest by range**</span></span>           | <span data-ttu-id="8d1fa-178">Dny</span><span class="sxs-lookup"><span data-stu-id="8d1fa-178">Days</span></span>            |
| <span data-ttu-id="8d1fa-179">**Vypočítat úrok podle**</span><span class="sxs-lookup"><span data-stu-id="8d1fa-179">**Calculate interest based on**</span></span> | <span data-ttu-id="8d1fa-180">Částka</span><span class="sxs-lookup"><span data-stu-id="8d1fa-180">Amount</span></span>          |

<span data-ttu-id="8d1fa-181">Takto nastavíte rozsah informací.</span><span class="sxs-lookup"><span data-stu-id="8d1fa-181">You set up the range information as follows.</span></span>

| <span data-ttu-id="8d1fa-182">**Od hodnoty**</span><span class="sxs-lookup"><span data-stu-id="8d1fa-182">**From value**</span></span> | <span data-ttu-id="8d1fa-183">**Hodnota úroků**</span><span class="sxs-lookup"><span data-stu-id="8d1fa-183">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="8d1fa-184">0</span><span class="sxs-lookup"><span data-stu-id="8d1fa-184">0</span></span>              | <span data-ttu-id="8d1fa-185">10</span><span class="sxs-lookup"><span data-stu-id="8d1fa-185">10</span></span>                 |
| <span data-ttu-id="8d1fa-186">61</span><span class="sxs-lookup"><span data-stu-id="8d1fa-186">61</span></span>             | <span data-ttu-id="8d1fa-187">15</span><span class="sxs-lookup"><span data-stu-id="8d1fa-187">15</span></span>                 |
| <span data-ttu-id="8d1fa-188">91</span><span class="sxs-lookup"><span data-stu-id="8d1fa-188">91</span></span>             | <span data-ttu-id="8d1fa-189">20</span><span class="sxs-lookup"><span data-stu-id="8d1fa-189">20</span></span>                 |


## <a name="example-3-interest-by-range--months"></a><span data-ttu-id="8d1fa-190">Příklad 3: Úrok podle rozsahu = měsíce</span><span class="sxs-lookup"><span data-stu-id="8d1fa-190">Example 3: Interest by range = Months</span></span>

<span data-ttu-id="8d1fa-191">Nastavíte kód úroku, který přiřadí úrok jednou za každý měsíc, po které platba faktury překročí její splatnost.</span><span class="sxs-lookup"><span data-stu-id="8d1fa-191">You set up an interest code that assesses interest one time for every month that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="8d1fa-192">Chcete založit výpočet na hodnotě úroku v procentech podle stupňovitých intervalů měsíců.</span><span class="sxs-lookup"><span data-stu-id="8d1fa-192">You want to base the calculation on a percentage interest value, according to stepped month intervals.</span></span> <span data-ttu-id="8d1fa-193">Hodnota úroků bude 1,5 % měsíčně za první tři měsíce po splatnosti, 2,0 % měsíčně za druhé tři měsíce a 2,5 % měsíčně za každý měsíc po prvních šesti měsících.</span><span class="sxs-lookup"><span data-stu-id="8d1fa-193">The interest value will be 1.5 percent per month for the first three overdue months, 2.0 percent per month for the second three months, and 2.5 percent per month for each month beyond the first six months.</span></span> <span data-ttu-id="8d1fa-194">Hodnoty polí pro kód úroku nastavíte následovně.</span><span class="sxs-lookup"><span data-stu-id="8d1fa-194">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="8d1fa-195">**Název pole**</span><span class="sxs-lookup"><span data-stu-id="8d1fa-195">**Field name**</span></span>                  | <span data-ttu-id="8d1fa-196">**Hodnota pole**</span><span class="sxs-lookup"><span data-stu-id="8d1fa-196">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="8d1fa-197">**Kód úroku**</span><span class="sxs-lookup"><span data-stu-id="8d1fa-197">**Interest code**</span></span>               | <span data-ttu-id="8d1fa-198">1M%ByMth</span><span class="sxs-lookup"><span data-stu-id="8d1fa-198">1M%ByMth</span></span>        |
| <span data-ttu-id="8d1fa-199">**Vypočítat úroky jednou za**</span><span class="sxs-lookup"><span data-stu-id="8d1fa-199">**Calculate interest every**</span></span>    | <span data-ttu-id="8d1fa-200">1/měsíc</span><span class="sxs-lookup"><span data-stu-id="8d1fa-200">1/Month</span></span>         |
| <span data-ttu-id="8d1fa-201">**Úrok podle rozsahu**</span><span class="sxs-lookup"><span data-stu-id="8d1fa-201">**Interest by range**</span></span>           | <span data-ttu-id="8d1fa-202">Měsíce</span><span class="sxs-lookup"><span data-stu-id="8d1fa-202">Months</span></span>          |
| <span data-ttu-id="8d1fa-203">**Vypočítat úrok podle**</span><span class="sxs-lookup"><span data-stu-id="8d1fa-203">**Calculate interest based on**</span></span> | <span data-ttu-id="8d1fa-204">Procento</span><span class="sxs-lookup"><span data-stu-id="8d1fa-204">Percentage</span></span>      |

<span data-ttu-id="8d1fa-205">Takto nastavíte rozsah informací.</span><span class="sxs-lookup"><span data-stu-id="8d1fa-205">You set up the range information as follows.</span></span>

| <span data-ttu-id="8d1fa-206">**Od hodnoty**</span><span class="sxs-lookup"><span data-stu-id="8d1fa-206">**From value**</span></span> | <span data-ttu-id="8d1fa-207">**Hodnota úroků**</span><span class="sxs-lookup"><span data-stu-id="8d1fa-207">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="8d1fa-208">0</span><span class="sxs-lookup"><span data-stu-id="8d1fa-208">0</span></span>              | <span data-ttu-id="8d1fa-209">1.5</span><span class="sxs-lookup"><span data-stu-id="8d1fa-209">1.5</span></span>                |
| <span data-ttu-id="8d1fa-210">4</span><span class="sxs-lookup"><span data-stu-id="8d1fa-210">4</span></span>              | <span data-ttu-id="8d1fa-211">2</span><span class="sxs-lookup"><span data-stu-id="8d1fa-211">2</span></span>                  |
| <span data-ttu-id="8d1fa-212">7</span><span class="sxs-lookup"><span data-stu-id="8d1fa-212">7</span></span>              | <span data-ttu-id="8d1fa-213">2,5</span><span class="sxs-lookup"><span data-stu-id="8d1fa-213">2.5</span></span>                |

## <a name="new-versions"></a><span data-ttu-id="8d1fa-214">Nové verze</span><span class="sxs-lookup"><span data-stu-id="8d1fa-214">New versions</span></span>
<span data-ttu-id="8d1fa-215">Kódy úroků mají časovou platnost.</span><span class="sxs-lookup"><span data-stu-id="8d1fa-215">Interest codes are date effective.</span></span> <span data-ttu-id="8d1fa-216">Pokud chcete upravit úrokové sazby, můžete vytvořit **novou verzi**, která bude účinná k budoucímu datu.</span><span class="sxs-lookup"><span data-stu-id="8d1fa-216">If you want to modify the interest rate, you can create a **new version** that is effective as of a future date.</span></span>

<span data-ttu-id="8d1fa-217">K zobrazení různých verzí můžete použít volbu nabídky **K datu** a vybrat koncové datum.</span><span class="sxs-lookup"><span data-stu-id="8d1fa-217">To view different versions, you can use the **As of Date** menu choice to select the cutoff date.</span></span> <span data-ttu-id="8d1fa-218">Také můžete výběrem možnosti **Zobrazit všechny záznamy** zobrazit na stránce všechny kódy úroků.</span><span class="sxs-lookup"><span data-stu-id="8d1fa-218">You can also select the **Display all records** to view all interest codes in the page.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
