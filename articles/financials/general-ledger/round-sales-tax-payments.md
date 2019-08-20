---
title: Platby DPH a pravidla zaokrouhlení
description: Tento článek vysvětluje princip nastavení pravidla zaokrouhlování v rámci finančních DPH, a zaokrouhlení zůstatku DPH během úlohy Vyrovnat a zaúčtovat DPH.
author: ShylaThompson
manager: AnnBe
ms.date: 05/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: yijialuan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 168c2fb9edfc994617ef6764a5b9f5949d599882
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834991"
---
# <a name="sales-tax-payments-and-rounding-rules"></a><span data-ttu-id="e3d16-103">Platby DPH a pravidla zaokrouhlení</span><span class="sxs-lookup"><span data-stu-id="e3d16-103">Sales tax payments and rounding rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e3d16-104">Tento článek vysvětluje princip nastavení pravidla zaokrouhlování v rámci finančních DPH, a zaokrouhlení zůstatku DPH během úlohy Vyrovnat a zaúčtovat DPH.</span><span class="sxs-lookup"><span data-stu-id="e3d16-104">This article explains how the rounding rule setup on the Sales tax authorities works and rounding the sales tax balance during the Settle and post sales tax job.</span></span>

<span data-ttu-id="e3d16-105">DPH musí být vykázána a zaplacena v pravidelných intervalech finančnímu úřadu.</span><span class="sxs-lookup"><span data-stu-id="e3d16-105">Periodically, sales tax needs to be reported and paid to tax authorities.</span></span> <span data-ttu-id="e3d16-106">Toto lze provést spuštěním procesu vyúčtování a následného poprodejního daňového procesu na stránce Daň z prodeje.</span><span class="sxs-lookup"><span data-stu-id="e3d16-106">This can be done by running the settle and post sales tax process in the Sales tax page.</span></span> <span data-ttu-id="e3d16-107">Daň z prodeje za určité období bude vypořádána proti účtům daně z prodeje a zůstatek daně z prodeje bude účtován na účet vypořádání daně z prodeje.</span><span class="sxs-lookup"><span data-stu-id="e3d16-107">Sales tax for a period will be settled against the sales tax accounts and the sales tax balance will be posted to the Sales tax settlement account.</span></span> <span data-ttu-id="e3d16-108">Zůstatek DPH, který se zaúčtuje na účet pro vyrovnání DPH, je možné zaokrouhlit podle požadavků finančního úřadu nastavením pravidla zaokrouhlování na stránce DPH.</span><span class="sxs-lookup"><span data-stu-id="e3d16-108">The sales tax balance, which is posted on the Sales tax settlement account, can be rounded as required by tax authorities by setting up a rounding rule on the Sales tax page.</span></span> 

<span data-ttu-id="e3d16-109">Rozdíl v zaokrouhlení se zaúčtuje na účet pro zaokrouhlení DPH, který je vybrán v poli Účty pro automatické transakce v hlavní knize.</span><span class="sxs-lookup"><span data-stu-id="e3d16-109">The rounding difference is posted to the Sales tax rounding account that is selected in the Accounts for automatic transactions field in the General ledger.</span></span>

<span data-ttu-id="e3d16-110">Níže naleznete příklady popisující princip pravidla zaokrouhlování pro finanční úřad.</span><span class="sxs-lookup"><span data-stu-id="e3d16-110">The below example illustrates how the rounding rule on Sales tax authority works.</span></span>

## <a name="examples"></a><span data-ttu-id="e3d16-111">Příklad</span><span class="sxs-lookup"><span data-stu-id="e3d16-111">Examples</span></span>

<span data-ttu-id="e3d16-112">Celková částka DPH pro období se zobrazí jako kreditní zůstatek -98 765,43.</span><span class="sxs-lookup"><span data-stu-id="e3d16-112">The total sales tax for a period shows a credit balance of -98,765.43.</span></span> <span data-ttu-id="e3d16-113">Právnická osoba shromáždila vyšší částku DPH než kolik zaplatila.</span><span class="sxs-lookup"><span data-stu-id="e3d16-113">The legal entity collected more sales taxes than it paid.</span></span> <span data-ttu-id="e3d16-114">Proto právnická osoba dluží peníze daňovému úřadu.</span><span class="sxs-lookup"><span data-stu-id="e3d16-114">Therefore, the legal entity owes money to the tax authority.</span></span> 

<span data-ttu-id="e3d16-115">Právnická osoba chce použít metodu zaokrouhlení, která zaokrouhluje zůstatek na nejbližší násobek 1,00.</span><span class="sxs-lookup"><span data-stu-id="e3d16-115">The legal entity wants to use a rounding method that rounds the balance to the nearest 1.00.</span></span> <span data-ttu-id="e3d16-116">Uživatel odpovědný za účtování DPH musí provést následující akce.</span><span class="sxs-lookup"><span data-stu-id="e3d16-116">The user who is responsible for sales tax accounting performs the following steps.</span></span>

1.  <span data-ttu-id="e3d16-117">Klikněte na Daň &gt; Nepřímé daně &gt; DPH &gt; Finanční úřady</span><span class="sxs-lookup"><span data-stu-id="e3d16-117">Click Tax &gt; Indirect taxes &gt; Sales tax &gt; Sales tax authorities</span></span>
2.  <span data-ttu-id="e3d16-118">Na pevné kartě Obecné vybere v poli Způsob zaokrouhlování možnost Normální.</span><span class="sxs-lookup"><span data-stu-id="e3d16-118">On the General FastTab, select Normal in the Rounding form field.</span></span>
3.  <span data-ttu-id="e3d16-119">V poli Zaokrouhlení zadejte číslo 1,00.</span><span class="sxs-lookup"><span data-stu-id="e3d16-119">In the Round-off field, enter 1.00.</span></span>
4.  <span data-ttu-id="e3d16-120">V době, kdy je nutné zaplatit DPH daňovému úřadu, otevře stránku Vyrovnat a zaúčtovat DPH.</span><span class="sxs-lookup"><span data-stu-id="e3d16-120">When it is time to pay the sales taxes to the tax authority, open the Settle and post sales tax page.</span></span> <span data-ttu-id="e3d16-121">(Klikněte na Daň &gt; Přiznání &gt; DPH &gt; Vyrovnat a zaúčtovat DPH.)</span><span class="sxs-lookup"><span data-stu-id="e3d16-121">(Click Tax &gt; Declarations &gt; Sales tax &gt; Settle and post sales tax.)</span></span>
5.  <span data-ttu-id="e3d16-122">V účtu pro vyrovnání DPH je částka daňové povinnosti 98 765,43 zaokrouhlena na 98 765.</span><span class="sxs-lookup"><span data-stu-id="e3d16-122">On the sales tax settlement account, the tax liability amount of 98,765.43 is rounded to 98,765.</span></span>

<span data-ttu-id="e3d16-123">Následující tabulka ukazuje, jak je zaokrouhlena částka 98 765,43 pomocí každé z metod zaokrouhlení, která je k dispozici v poli Způsob zaokrouhlování na stránce Finanční úřady.</span><span class="sxs-lookup"><span data-stu-id="e3d16-123">The following table shows how an amount of 98,765.43 is rounded by using each rounding method that is available in the Rounding form field in the Sales tax authorities page.</span></span>

| <span data-ttu-id="e3d16-124">Možnost zaokrouhlování</span><span class="sxs-lookup"><span data-stu-id="e3d16-124">Rounding form option</span></span>                | <span data-ttu-id="e3d16-125">Zaokrouhlená hodnota = 0,01</span><span class="sxs-lookup"><span data-stu-id="e3d16-125">Round-off value = 0.01</span></span> | <span data-ttu-id="e3d16-126">Zaokrouhlená hodnota = 0,10</span><span class="sxs-lookup"><span data-stu-id="e3d16-126">Round-off value = 0.10</span></span> | <span data-ttu-id="e3d16-127">Zaokrouhlená hodnota = 1,00</span><span class="sxs-lookup"><span data-stu-id="e3d16-127">Round-off value = 1.00</span></span> | <span data-ttu-id="e3d16-128">Zaokrouhlená hodnota = 100,00</span><span class="sxs-lookup"><span data-stu-id="e3d16-128">Round-off value = 100.00</span></span> |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|
| <span data-ttu-id="e3d16-129">Normální</span><span class="sxs-lookup"><span data-stu-id="e3d16-129">Normal</span></span>                              | <span data-ttu-id="e3d16-130">98 765,43</span><span class="sxs-lookup"><span data-stu-id="e3d16-130">98,765.43</span></span>              | <span data-ttu-id="e3d16-131">98 765,40</span><span class="sxs-lookup"><span data-stu-id="e3d16-131">98,765.40</span></span>              | <span data-ttu-id="e3d16-132">98 765,00</span><span class="sxs-lookup"><span data-stu-id="e3d16-132">98,765.00</span></span>              | <span data-ttu-id="e3d16-133">98 800,00</span><span class="sxs-lookup"><span data-stu-id="e3d16-133">98,800.00</span></span>                |
| <span data-ttu-id="e3d16-134">Dolů</span><span class="sxs-lookup"><span data-stu-id="e3d16-134">Downward</span></span>                            | <span data-ttu-id="e3d16-135">98 765,43</span><span class="sxs-lookup"><span data-stu-id="e3d16-135">98,765.43</span></span>              | <span data-ttu-id="e3d16-136">98 765,40</span><span class="sxs-lookup"><span data-stu-id="e3d16-136">98,765.40</span></span>              | <span data-ttu-id="e3d16-137">98 765,00</span><span class="sxs-lookup"><span data-stu-id="e3d16-137">98,765.00</span></span>              | <span data-ttu-id="e3d16-138">98 700,00</span><span class="sxs-lookup"><span data-stu-id="e3d16-138">98,700.00</span></span>                |
| <span data-ttu-id="e3d16-139">Zaokrouhlení nahoru</span><span class="sxs-lookup"><span data-stu-id="e3d16-139">Rounding-up</span></span>                         | <span data-ttu-id="e3d16-140">98 765,43</span><span class="sxs-lookup"><span data-stu-id="e3d16-140">98,765.43</span></span>              | <span data-ttu-id="e3d16-141">98 765,50</span><span class="sxs-lookup"><span data-stu-id="e3d16-141">98,765.50</span></span>              | <span data-ttu-id="e3d16-142">98 766,00</span><span class="sxs-lookup"><span data-stu-id="e3d16-142">98,766.00</span></span>              | <span data-ttu-id="e3d16-143">98 800,00</span><span class="sxs-lookup"><span data-stu-id="e3d16-143">98,800.00</span></span>                |
| <span data-ttu-id="e3d16-144">Vlastní výhoda pro kreditní zůstatek</span><span class="sxs-lookup"><span data-stu-id="e3d16-144">Own advantage, for a credit balance</span></span> | <span data-ttu-id="e3d16-145">98 765,43</span><span class="sxs-lookup"><span data-stu-id="e3d16-145">98,765.43</span></span>              | <span data-ttu-id="e3d16-146">98 765,40</span><span class="sxs-lookup"><span data-stu-id="e3d16-146">98,765.40</span></span>              | <span data-ttu-id="e3d16-147">98 765,00</span><span class="sxs-lookup"><span data-stu-id="e3d16-147">98,765.00</span></span>              | <span data-ttu-id="e3d16-148">98 700,00</span><span class="sxs-lookup"><span data-stu-id="e3d16-148">98,700.00</span></span>                |
| <span data-ttu-id="e3d16-149">Vlastní výhoda pro debetní zůstatek</span><span class="sxs-lookup"><span data-stu-id="e3d16-149">Own advantage, for a debit balance</span></span>  | <span data-ttu-id="e3d16-150">98,765.43</span><span class="sxs-lookup"><span data-stu-id="e3d16-150">98,765.43</span></span>              | <span data-ttu-id="e3d16-151">98,765.50</span><span class="sxs-lookup"><span data-stu-id="e3d16-151">98,765.50</span></span>              | <span data-ttu-id="e3d16-152">98,766.00</span><span class="sxs-lookup"><span data-stu-id="e3d16-152">98,766.00</span></span>              | <span data-ttu-id="e3d16-153">98,800.00</span><span class="sxs-lookup"><span data-stu-id="e3d16-153">98,800.00</span></span>                |


### <a name="no-rounding-at-all-since-the-round-off-is-000"></a><span data-ttu-id="e3d16-154">Žádné zaokrouhlování, protože zaokrouhlení je 0,00</span><span class="sxs-lookup"><span data-stu-id="e3d16-154">No rounding at all, since the round-off is 0.00</span></span>

<span data-ttu-id="e3d16-155">round(1,0151, 0.00) = 1,0151 round(1,0149, 0.00) = 1,0149</span><span class="sxs-lookup"><span data-stu-id="e3d16-155">round(1.0151, 0.00) = 1.0151 round(1.0149, 0.00) = 1.0149</span></span>

### <a name="normal-round-and-round-precision-is-001"></a><span data-ttu-id="e3d16-156">Normální zaokrouhlení a přesnost zaokrouhlení je 0,01</span><span class="sxs-lookup"><span data-stu-id="e3d16-156">Normal round, and round precision is 0.01</span></span>

<table>
  <tr>
    <td><span data-ttu-id="e3d16-157">Zaokrouhlení</span><span class="sxs-lookup"><span data-stu-id="e3d16-157">Rounding</span></span>
    </td>
    <td><span data-ttu-id="e3d16-158">Proces výpočtu</span><span class="sxs-lookup"><span data-stu-id="e3d16-158">Calculation process</span></span>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="e3d16-159">round(1,015, 0,01) = 1,02</span><span class="sxs-lookup"><span data-stu-id="e3d16-159">round(1.015, 0.01) = 1.02</span></span>
    </td>
    <td>
      <ol>
        <li><span data-ttu-id="e3d16-160">round(1,015 / 0,01, 0) = round(101,5, 0) = 102</span><span class="sxs-lookup"><span data-stu-id="e3d16-160">round(1.015 / 0.01, 0) = round(101.5, 0) = 102</span></span>
        </li>
        <li><span data-ttu-id="e3d16-161">102 \* 0,01 = 1,02</span><span class="sxs-lookup"><span data-stu-id="e3d16-161">102 \* 0.01 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="e3d16-162">round(1,014, 0,01) = 1,01</span><span class="sxs-lookup"><span data-stu-id="e3d16-162">round(1.014, 0.01) = 1.01</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="e3d16-163">round(1,014 / 0,01, 0) = round(101,4, 0) = 101</span><span class="sxs-lookup"><span data-stu-id="e3d16-163">round(1.014 / 0.01, 0) = round(101.4, 0) = 101</span></span>
        </li>
        <li><span data-ttu-id="e3d16-164">101 \* 0,01 = 1,01</span><span class="sxs-lookup"><span data-stu-id="e3d16-164">101 \* 0.01 = 1.01</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="e3d16-165">round(1,011, 0,02) = 1,02</span><span class="sxs-lookup"><span data-stu-id="e3d16-165">round(1.011, 0.02) = 1.02</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="e3d16-166">round(1,011 / 0,02, 0) = round(50,55, 0) = 51</span><span class="sxs-lookup"><span data-stu-id="e3d16-166">round(1.011 / 0.02, 0) = round(50.55, 0) = 51</span></span>
        </li>
        <li><span data-ttu-id="e3d16-167">51 \* 0,02 = 1,02</span><span class="sxs-lookup"><span data-stu-id="e3d16-167">51 \* 0.02 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="e3d16-168">round(1,009, 0,02) = 1,00</span><span class="sxs-lookup"><span data-stu-id="e3d16-168">round(1.009, 0.02) = 1.00</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="e3d16-169">round(1,009 / 0,02, 0) = round(50,45, 0) = 50</span><span class="sxs-lookup"><span data-stu-id="e3d16-169">round(1.009 / 0.02, 0) = round(50.45, 0) = 50</span></span>
        </li>
        <li><span data-ttu-id="e3d16-170">50 \* 0,02 = 1,00</span><span class="sxs-lookup"><span data-stu-id="e3d16-170">50 \* 0.02 = 1.00</span></span>
        </li>
      </ol>
    </td>
  </tr>
</table>

> [!NOTE]                                                                                  
> <span data-ttu-id="e3d16-171">Vyberete-li možnost Vlastní výhoda, zaokrouhlení je vždy ve prospěch právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="e3d16-171">If you select Own advantage, the rounding is always to the advantage of the legal entity.</span></span> 

<span data-ttu-id="e3d16-172">Další informace naleznete v následujících tématech:</span><span class="sxs-lookup"><span data-stu-id="e3d16-172">For more information, see the following topics:</span></span>
- [<span data-ttu-id="e3d16-173">Přehled DPH</span><span class="sxs-lookup"><span data-stu-id="e3d16-173">Sales tax overview</span></span>](indirect-taxes-overview.md)
- [<span data-ttu-id="e3d16-174">Vytvoření platby DPH</span><span class="sxs-lookup"><span data-stu-id="e3d16-174">Create a sales tax payment</span></span>](tasks/create-sales-tax-payment.md)
- [<span data-ttu-id="e3d16-175">Vytváření obchodních transakcí v dokladech</span><span class="sxs-lookup"><span data-stu-id="e3d16-175">Create sales transactions on documents</span></span>](tasks/create-sales-tax-transactions-documents.md)
- [<span data-ttu-id="e3d16-176">Zobrazení zaúčtovaných transakcí DPH</span><span class="sxs-lookup"><span data-stu-id="e3d16-176">View posted sales tax transactions</span></span>](tasks/view-posted-sales-tax-transactions.md)
- [<span data-ttu-id="e3d16-177">Funkce round</span><span class="sxs-lookup"><span data-stu-id="e3d16-177">round Function</span></span>](https://msdn.microsoft.com/library/aa850656.aspx)


