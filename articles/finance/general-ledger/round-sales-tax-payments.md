---
title: Platby DPH a pravidla zaokrouhlení
description: Tento článek vysvětluje princip nastavení pravidla zaokrouhlování v rámci finančních DPH, a zaokrouhlení zůstatku DPH během úlohy Vyrovnat a zaúčtovat DPH.
author: ShylaThompson
manager: AnnBe
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: roschlom
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e8d7e402614b35a77a0283d31377a073b0a6b357
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990182"
---
# <a name="sales-tax-payments-and-rounding-rules"></a><span data-ttu-id="80897-103">Platby DPH a pravidla zaokrouhlení</span><span class="sxs-lookup"><span data-stu-id="80897-103">Sales tax payments and rounding rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="80897-104">Tento článek vysvětluje princip nastavení pravidla zaokrouhlování v rámci finančních DPH, a zaokrouhlení zůstatku DPH během úlohy Vyrovnat a zaúčtovat DPH.</span><span class="sxs-lookup"><span data-stu-id="80897-104">This article explains how the rounding rule setup on the Sales tax authorities works and rounding the sales tax balance during the Settle and post sales tax job.</span></span>

<span data-ttu-id="80897-105">DPH musí být vykázána a zaplacena v pravidelných intervalech finančnímu úřadu.</span><span class="sxs-lookup"><span data-stu-id="80897-105">Periodically, sales tax needs to be reported and paid to tax authorities.</span></span> <span data-ttu-id="80897-106">Toto lze provést spuštěním procesu vyúčtování a následného poprodejního daňového procesu na stránce Daň z prodeje.</span><span class="sxs-lookup"><span data-stu-id="80897-106">This can be done by running the settle and post sales tax process in the Sales tax page.</span></span> <span data-ttu-id="80897-107">Daň z prodeje za určité období bude vypořádána proti účtům daně z prodeje a zůstatek daně z prodeje bude účtován na účet vypořádání daně z prodeje.</span><span class="sxs-lookup"><span data-stu-id="80897-107">Sales tax for a period will be settled against the sales tax accounts and the sales tax balance will be posted to the Sales tax settlement account.</span></span> <span data-ttu-id="80897-108">Zůstatek DPH, který se zaúčtuje na účet pro vyrovnání DPH, je možné zaokrouhlit podle požadavků finančního úřadu nastavením pravidla zaokrouhlování na stránce DPH.</span><span class="sxs-lookup"><span data-stu-id="80897-108">The sales tax balance, which is posted on the Sales tax settlement account, can be rounded as required by tax authorities by setting up a rounding rule on the Sales tax page.</span></span> 

<span data-ttu-id="80897-109">Rozdíl v zaokrouhlení se zaúčtuje na účet pro zaokrouhlení DPH, který je vybrán v poli Účty pro automatické transakce v hlavní knize.</span><span class="sxs-lookup"><span data-stu-id="80897-109">The rounding difference is posted to the Sales tax rounding account that is selected in the Accounts for automatic transactions field in the General ledger.</span></span>

<span data-ttu-id="80897-110">Níže naleznete příklady popisující princip pravidla zaokrouhlování pro finanční úřad.</span><span class="sxs-lookup"><span data-stu-id="80897-110">The below example illustrates how the rounding rule on Sales tax authority works.</span></span>

## <a name="examples"></a><span data-ttu-id="80897-111">Příklad</span><span class="sxs-lookup"><span data-stu-id="80897-111">Examples</span></span>

<span data-ttu-id="80897-112">Celková částka DPH pro období se zobrazí jako kreditní zůstatek -98 765,43.</span><span class="sxs-lookup"><span data-stu-id="80897-112">The total sales tax for a period shows a credit balance of -98,765.43.</span></span> <span data-ttu-id="80897-113">Právnická osoba shromáždila vyšší částku DPH než kolik zaplatila.</span><span class="sxs-lookup"><span data-stu-id="80897-113">The legal entity collected more sales taxes than it paid.</span></span> <span data-ttu-id="80897-114">Proto právnická osoba dluží peníze daňovému úřadu.</span><span class="sxs-lookup"><span data-stu-id="80897-114">Therefore, the legal entity owes money to the tax authority.</span></span> 

<span data-ttu-id="80897-115">Právnická osoba chce použít metodu zaokrouhlení, která zaokrouhluje zůstatek na nejbližší násobek 1,00.</span><span class="sxs-lookup"><span data-stu-id="80897-115">The legal entity wants to use a rounding method that rounds the balance to the nearest 1.00.</span></span> <span data-ttu-id="80897-116">Uživatel odpovědný za účtování DPH musí provést následující akce.</span><span class="sxs-lookup"><span data-stu-id="80897-116">The user who is responsible for sales tax accounting performs the following steps.</span></span>

1. <span data-ttu-id="80897-117">Klikne na **Daň** > **Nepřímé daně** > **DPH** > **Finanční úřady**.</span><span class="sxs-lookup"><span data-stu-id="80897-117">Click **Tax** > **Indirect taxes** > **Sales tax** > **Sales tax authorities**.</span></span>
2. <span data-ttu-id="80897-118">Na pevné kartě **Obecné** vybere v poli **Způsob zaokrouhlování** možnost **Normální**.</span><span class="sxs-lookup"><span data-stu-id="80897-118">On the **General** FastTab, in the **Rounding form** field, select **Normal**.</span></span>
3. <span data-ttu-id="80897-119">V poli **Zaokrouhlení** zadejte číslo 1,00.</span><span class="sxs-lookup"><span data-stu-id="80897-119">In the **Round-off** field, enter 1.00.</span></span>
4. <span data-ttu-id="80897-120">V době, kdy je nutné zaplatit DPH daňovému úřadu, přejděte na **Daň** > **Deklarace** > **DPH** > **Vyrovnat a zaúčtovat DPH**.</span><span class="sxs-lookup"><span data-stu-id="80897-120">When it is time to pay the sales taxes to the tax authority, go to **Tax** > **Declarations** > **Sales tax** > **Settle and post sale tax**.</span></span> <span data-ttu-id="80897-121">V účtu pro vyrovnání DPH můžete vidět, že částka daňové povinnosti **98 765,43** je zaokrouhlena na zaokrouhlena na **98 765**.</span><span class="sxs-lookup"><span data-stu-id="80897-121">On the sales tax settlement account, you can see that the tax liability amount of **98,765.43** is rounded to **98,765**.</span></span>

<span data-ttu-id="80897-122">Následující tabulka ukazuje, jak je zaokrouhlena částka 98 765,43 pomocí každé z metod zaokrouhlení, která je k dispozici v poli **Způsob zaokrouhlování** na stránce **Finanční úřady**.</span><span class="sxs-lookup"><span data-stu-id="80897-122">The following table shows how an amount of 98,765.43 is rounded by using each rounding method that is available in the **Rounding form** field in the **Sales tax authorities** page.</span></span>

> [!NOTE]                                                                                  
> <span data-ttu-id="80897-123">Je-li hodnota zaokrouhlení nastavena na 0,00, pak:</span><span class="sxs-lookup"><span data-stu-id="80897-123">If the round-off value is set as 0.00, then:</span></span>
>
> - <span data-ttu-id="80897-124">Pro normální zaokrouhlování je chování zaokrouhlení stejné jako při **zaokrouhlení = 0,01**.</span><span class="sxs-lookup"><span data-stu-id="80897-124">For normal rounding, the rounding behavior is the same as for **Round-off = 0.01**.</span></span>
> - <span data-ttu-id="80897-125">U možností **Způsob zaokrouhlování**, **dolů**, **Zaokrouhlení nahoru** a **Vlastní výhoda** je chování stejné jako při **Zaokrouhlení = 1.00**.</span><span class="sxs-lookup"><span data-stu-id="80897-125">For the **Rounding form options**, **Downward**, **Rounding-up**, and **Own advantage**, the behavior is the same as for **Round-off = 1.00**.</span></span>

| <span data-ttu-id="80897-126">Možnost zaokrouhlování</span><span class="sxs-lookup"><span data-stu-id="80897-126">Rounding form option</span></span>                | <span data-ttu-id="80897-127">Zaokrouhlená hodnota = 0,01</span><span class="sxs-lookup"><span data-stu-id="80897-127">Round-off value = 0.01</span></span> | <span data-ttu-id="80897-128">Zaokrouhlená hodnota = 0,10</span><span class="sxs-lookup"><span data-stu-id="80897-128">Round-off value = 0.10</span></span> | <span data-ttu-id="80897-129">Zaokrouhlená hodnota = 1,00</span><span class="sxs-lookup"><span data-stu-id="80897-129">Round-off value = 1.00</span></span> | <span data-ttu-id="80897-130">Zaokrouhlená hodnota = 100,00</span><span class="sxs-lookup"><span data-stu-id="80897-130">Round-off value = 100.00</span></span> | <span data-ttu-id="80897-131">Zaokrouhlená hodnota = 0,00</span><span class="sxs-lookup"><span data-stu-id="80897-131">Round-off value = 0.00</span></span>   |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|--------------------------|
| <span data-ttu-id="80897-132">Normální</span><span class="sxs-lookup"><span data-stu-id="80897-132">Normal</span></span>                              | <span data-ttu-id="80897-133">98,765.43</span><span class="sxs-lookup"><span data-stu-id="80897-133">98,765.43</span></span>              | <span data-ttu-id="80897-134">98,765.40</span><span class="sxs-lookup"><span data-stu-id="80897-134">98,765.40</span></span>              | <span data-ttu-id="80897-135">98,765.00</span><span class="sxs-lookup"><span data-stu-id="80897-135">98,765.00</span></span>              | <span data-ttu-id="80897-136">98,800.00</span><span class="sxs-lookup"><span data-stu-id="80897-136">98,800.00</span></span>                | <span data-ttu-id="80897-137">98,765.43</span><span class="sxs-lookup"><span data-stu-id="80897-137">98,765.43</span></span>                |
| <span data-ttu-id="80897-138">Dolů</span><span class="sxs-lookup"><span data-stu-id="80897-138">Downward</span></span>                            | <span data-ttu-id="80897-139">98,765.43</span><span class="sxs-lookup"><span data-stu-id="80897-139">98,765.43</span></span>              | <span data-ttu-id="80897-140">98,765.40</span><span class="sxs-lookup"><span data-stu-id="80897-140">98,765.40</span></span>              | <span data-ttu-id="80897-141">98,765.00</span><span class="sxs-lookup"><span data-stu-id="80897-141">98,765.00</span></span>              | <span data-ttu-id="80897-142">98,700.00</span><span class="sxs-lookup"><span data-stu-id="80897-142">98,700.00</span></span>                | <span data-ttu-id="80897-143">98,765.00</span><span class="sxs-lookup"><span data-stu-id="80897-143">98,765.00</span></span>                |
| <span data-ttu-id="80897-144">Zaokrouhlení nahoru</span><span class="sxs-lookup"><span data-stu-id="80897-144">Rounding-up</span></span>                         | <span data-ttu-id="80897-145">98,765.43</span><span class="sxs-lookup"><span data-stu-id="80897-145">98,765.43</span></span>              | <span data-ttu-id="80897-146">98,765.50</span><span class="sxs-lookup"><span data-stu-id="80897-146">98,765.50</span></span>              | <span data-ttu-id="80897-147">98,766.00</span><span class="sxs-lookup"><span data-stu-id="80897-147">98,766.00</span></span>              | <span data-ttu-id="80897-148">98,800.00</span><span class="sxs-lookup"><span data-stu-id="80897-148">98,800.00</span></span>                | <span data-ttu-id="80897-149">98,766.00</span><span class="sxs-lookup"><span data-stu-id="80897-149">98,766.00</span></span>                |
| <span data-ttu-id="80897-150">Vlastní výhoda pro kreditní zůstatek</span><span class="sxs-lookup"><span data-stu-id="80897-150">Own advantage, for a credit balance</span></span> | <span data-ttu-id="80897-151">98,765.43</span><span class="sxs-lookup"><span data-stu-id="80897-151">98,765.43</span></span>              | <span data-ttu-id="80897-152">98,765.40</span><span class="sxs-lookup"><span data-stu-id="80897-152">98,765.40</span></span>              | <span data-ttu-id="80897-153">98,765.00</span><span class="sxs-lookup"><span data-stu-id="80897-153">98,765.00</span></span>              | <span data-ttu-id="80897-154">98,700.00</span><span class="sxs-lookup"><span data-stu-id="80897-154">98,700.00</span></span>                | <span data-ttu-id="80897-155">98,765.00</span><span class="sxs-lookup"><span data-stu-id="80897-155">98,765.00</span></span>                |
| <span data-ttu-id="80897-156">Vlastní výhoda pro debetní zůstatek</span><span class="sxs-lookup"><span data-stu-id="80897-156">Own advantage, for a debit balance</span></span>  | <span data-ttu-id="80897-157">98,765.43</span><span class="sxs-lookup"><span data-stu-id="80897-157">98,765.43</span></span>              | <span data-ttu-id="80897-158">98,765.50</span><span class="sxs-lookup"><span data-stu-id="80897-158">98,765.50</span></span>              | <span data-ttu-id="80897-159">98,766.00</span><span class="sxs-lookup"><span data-stu-id="80897-159">98,766.00</span></span>              | <span data-ttu-id="80897-160">98,800.00</span><span class="sxs-lookup"><span data-stu-id="80897-160">98,800.00</span></span>                | <span data-ttu-id="80897-161">98,766.00</span><span class="sxs-lookup"><span data-stu-id="80897-161">98,766.00</span></span>                |

### <a name="normal-round-and-round-precision-is-001"></a><span data-ttu-id="80897-162">Normální zaokrouhlení a přesnost zaokrouhlení je 0,01</span><span class="sxs-lookup"><span data-stu-id="80897-162">Normal round, and round precision is 0.01</span></span>

<table>
  <tr>
    <td><span data-ttu-id="80897-163">Zaokrouhlení</span><span class="sxs-lookup"><span data-stu-id="80897-163">Rounding</span></span>
    </td>
    <td><span data-ttu-id="80897-164">Proces výpočtu</span><span class="sxs-lookup"><span data-stu-id="80897-164">Calculation process</span></span>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="80897-165">round(1,015, 0,01) = 1,02</span><span class="sxs-lookup"><span data-stu-id="80897-165">round(1.015, 0.01) = 1.02</span></span>
    </td>
    <td>
      <ol>
        <li><span data-ttu-id="80897-166">round(1,015 / 0,01, 0) = round(101,5, 0) = 102</span><span class="sxs-lookup"><span data-stu-id="80897-166">round(1.015 / 0.01, 0) = round(101.5, 0) = 102</span></span>
        </li>
        <li><span data-ttu-id="80897-167">102 \* 0,01 = 1,02</span><span class="sxs-lookup"><span data-stu-id="80897-167">102 \* 0.01 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="80897-168">round(1,014, 0,01) = 1,01</span><span class="sxs-lookup"><span data-stu-id="80897-168">round(1.014, 0.01) = 1.01</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="80897-169">round(1,014 / 0,01, 0) = round(101,4, 0) = 101</span><span class="sxs-lookup"><span data-stu-id="80897-169">round(1.014 / 0.01, 0) = round(101.4, 0) = 101</span></span>
        </li>
        <li><span data-ttu-id="80897-170">101 \* 0,01 = 1,01</span><span class="sxs-lookup"><span data-stu-id="80897-170">101 \* 0.01 = 1.01</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="80897-171">round(1,011, 0,02) = 1,02</span><span class="sxs-lookup"><span data-stu-id="80897-171">round(1.011, 0.02) = 1.02</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="80897-172">round(1,011 / 0,02, 0) = round(50,55, 0) = 51</span><span class="sxs-lookup"><span data-stu-id="80897-172">round(1.011 / 0.02, 0) = round(50.55, 0) = 51</span></span>
        </li>
        <li><span data-ttu-id="80897-173">51 \* 0,02 = 1,02</span><span class="sxs-lookup"><span data-stu-id="80897-173">51 \* 0.02 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="80897-174">round(1,009, 0,02) = 1,00</span><span class="sxs-lookup"><span data-stu-id="80897-174">round(1.009, 0.02) = 1.00</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="80897-175">round(1,009 / 0,02, 0) = round(50,45, 0) = 50</span><span class="sxs-lookup"><span data-stu-id="80897-175">round(1.009 / 0.02, 0) = round(50.45, 0) = 50</span></span>
        </li>
        <li><span data-ttu-id="80897-176">50 \* 0,02 = 1,00</span><span class="sxs-lookup"><span data-stu-id="80897-176">50 \* 0.02 = 1.00</span></span>
        </li>
      </ol>
    </td>
  </tr>
</table>

> [!NOTE]                                                                                  
> <span data-ttu-id="80897-177">Vyberete-li možnost Vlastní výhoda, zaokrouhlení je vždy ve prospěch právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="80897-177">If you select Own advantage, the rounding is always to the advantage of the legal entity.</span></span> 

<span data-ttu-id="80897-178">Další informace naleznete v následujících tématech:</span><span class="sxs-lookup"><span data-stu-id="80897-178">For more information, see the following topics:</span></span>
- [<span data-ttu-id="80897-179">Přehled DPH</span><span class="sxs-lookup"><span data-stu-id="80897-179">Sales tax overview</span></span>](indirect-taxes-overview.md)
- [<span data-ttu-id="80897-180">Vytvoření platby DPH</span><span class="sxs-lookup"><span data-stu-id="80897-180">Create a sales tax payment</span></span>](tasks/create-sales-tax-payment.md)
- [<span data-ttu-id="80897-181">Vytváření transakcí DPH v dokladech</span><span class="sxs-lookup"><span data-stu-id="80897-181">Create sales tax transactions on documents</span></span>](tasks/create-sales-tax-transactions-documents.md)
- [<span data-ttu-id="80897-182">Zobrazení zaúčtovaných transakcí DPH</span><span class="sxs-lookup"><span data-stu-id="80897-182">View posted sales tax transactions</span></span>](tasks/view-posted-sales-tax-transactions.md)
- [<span data-ttu-id="80897-183">Funkce round</span><span class="sxs-lookup"><span data-stu-id="80897-183">round Function</span></span>](https://msdn.microsoft.com/library/aa850656.aspx)


