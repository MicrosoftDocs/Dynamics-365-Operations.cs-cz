---
title: Platby DPH a pravidla zaokrouhlení
description: Tento článek vysvětluje princip nastavení pravidla zaokrouhlování v rámci finančních DPH, a zaokrouhlení zůstatku DPH během úlohy Vyrovnat a zaúčtovat DPH.
author: ShylaThompson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f03336c834e74cd12d039c7b9692874843811746
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "367839"
---
# <a name="sales-tax-payments-and-rounding-rules"></a><span data-ttu-id="254ce-103">Platby DPH a pravidla zaokrouhlení</span><span class="sxs-lookup"><span data-stu-id="254ce-103">Sales tax payments and rounding rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="254ce-104">Tento článek vysvětluje princip nastavení pravidla zaokrouhlování v rámci finančních DPH, a zaokrouhlení zůstatku DPH během úlohy Vyrovnat a zaúčtovat DPH.</span><span class="sxs-lookup"><span data-stu-id="254ce-104">This article explains how the rounding rule setup on the Sales tax authorities works and rounding the sales tax balance during the Settle and post sales tax job.</span></span>

<span data-ttu-id="254ce-105">DPH musí být vykázána a zaplacena v pravidelných intervalech finančnímu úřadu.</span><span class="sxs-lookup"><span data-stu-id="254ce-105">Periodically, sales tax needs to be reported and paid to tax authorities.</span></span> <span data-ttu-id="254ce-106">Toto lze provést spuštěním procesu vyúčtování a následného poprodejního daňového procesu na stránce Daň z prodeje.</span><span class="sxs-lookup"><span data-stu-id="254ce-106">This can be done by running the settle and post sales tax process in the Sales tax page.</span></span> <span data-ttu-id="254ce-107">Daň z prodeje za určité období bude vypořádána proti účtům daně z prodeje a zůstatek daně z prodeje bude účtován na účet vypořádání daně z prodeje.</span><span class="sxs-lookup"><span data-stu-id="254ce-107">Sales tax for a period will be settled against the sales tax accounts and the sales tax balance will be posted to the Sales tax settlement account.</span></span> <span data-ttu-id="254ce-108">Zůstatek DPH, který se zaúčtuje na účet pro vyrovnání DPH, je možné zaokrouhlit podle požadavků finančního úřadu nastavením pravidla zaokrouhlování na stránce DPH.</span><span class="sxs-lookup"><span data-stu-id="254ce-108">The sales tax balance, which is posted on the Sales tax settlement account, can be rounded as required by tax authorities by setting up a rounding rule on the Sales tax page.</span></span> 

<span data-ttu-id="254ce-109">Rozdíl v zaokrouhlení se zaúčtuje na účet pro zaokrouhlení DPH, který je vybrán v poli Účty pro automatické transakce v hlavní knize.</span><span class="sxs-lookup"><span data-stu-id="254ce-109">The rounding difference is posted to the Sales tax rounding account that is selected in the Accounts for automatic transactions field in the General ledger.</span></span>

<span data-ttu-id="254ce-110">Níže naleznete příklady popisující princip pravidla zaokrouhlování pro finanční úřad.</span><span class="sxs-lookup"><span data-stu-id="254ce-110">The below example illustrates how the rounding rule on Sales tax authority works.</span></span>

### <a name="example"></a><span data-ttu-id="254ce-111">Příklad:</span><span class="sxs-lookup"><span data-stu-id="254ce-111">Example:</span></span>

<span data-ttu-id="254ce-112">Celková částka DPH pro období se zobrazí jako kreditní zůstatek -98 765,43.</span><span class="sxs-lookup"><span data-stu-id="254ce-112">The total sales tax for a period shows a credit balance of -98,765.43.</span></span> <span data-ttu-id="254ce-113">Právnická osoba shromáždila vyšší částku DPH než kolik zaplatila.</span><span class="sxs-lookup"><span data-stu-id="254ce-113">The legal entity collected more sales taxes than it paid.</span></span> <span data-ttu-id="254ce-114">Proto právnická osoba dluží peníze daňovému úřadu.</span><span class="sxs-lookup"><span data-stu-id="254ce-114">Therefore, the legal entity owes money to the tax authority.</span></span> 

<span data-ttu-id="254ce-115">Právnická osoba chce použít metodu zaokrouhlení, která zaokrouhluje zůstatek na nejbližší násobek 1,00.</span><span class="sxs-lookup"><span data-stu-id="254ce-115">The legal entity wants to use a rounding method that rounds the balance to the nearest 1.00.</span></span> <span data-ttu-id="254ce-116">Uživatel odpovědný za účtování DPH musí provést následující akce.</span><span class="sxs-lookup"><span data-stu-id="254ce-116">The user who is responsible for sales tax accounting performs the following steps.</span></span>

1.  <span data-ttu-id="254ce-117">Klikněte na Daň &gt; Nepřímé daně &gt; DPH &gt; Finanční úřady</span><span class="sxs-lookup"><span data-stu-id="254ce-117">Click Tax &gt; Indirect taxes &gt; Sales tax &gt; Sales tax authorities</span></span>
2.  <span data-ttu-id="254ce-118">Na pevné kartě Obecné vybere v poli Způsob zaokrouhlování možnost Normální.</span><span class="sxs-lookup"><span data-stu-id="254ce-118">On the General FastTab, select Normal in the Rounding form field.</span></span>
3.  <span data-ttu-id="254ce-119">V poli Zaokrouhlení zadejte číslo 1,00.</span><span class="sxs-lookup"><span data-stu-id="254ce-119">In the Round-off field, enter 1.00.</span></span>
4.  <span data-ttu-id="254ce-120">V době, kdy je nutné zaplatit DPH daňovému úřadu, otevře stránku Vyrovnat a zaúčtovat DPH.</span><span class="sxs-lookup"><span data-stu-id="254ce-120">When it is time to pay the sales taxes to the tax authority, open the Settle and post sales tax page.</span></span> <span data-ttu-id="254ce-121">(Klikněte na Daň &gt; Přiznání &gt; DPH &gt; Vyrovnat a zaúčtovat DPH.)</span><span class="sxs-lookup"><span data-stu-id="254ce-121">(Click Tax &gt; Declarations &gt; Sales tax &gt; Settle and post sales tax.)</span></span>
5.  <span data-ttu-id="254ce-122">V účtu pro vyrovnání DPH je částka daňové povinnosti 98 765,43 zaokrouhlena na 98 765.</span><span class="sxs-lookup"><span data-stu-id="254ce-122">On the sales tax settlement account, the tax liability amount of 98,765.43 is rounded to 98,765.</span></span>

<span data-ttu-id="254ce-123">Následující tabulka ukazuje, jak je zaokrouhlena částka 98 765,43 pomocí každé z metod zaokrouhlení, která je k dispozici v poli Způsob zaokrouhlování na stránce Finanční úřady.</span><span class="sxs-lookup"><span data-stu-id="254ce-123">The following table shows how an amount of 98,765.43 is rounded by using each rounding method that is available in the Rounding form field in the Sales tax authorities page.</span></span>

| <span data-ttu-id="254ce-124">Možnost zaokrouhlování</span><span class="sxs-lookup"><span data-stu-id="254ce-124">Rounding form option</span></span>                | <span data-ttu-id="254ce-125">Zaokrouhlená hodnota = 0,01</span><span class="sxs-lookup"><span data-stu-id="254ce-125">Round-off value = 0.01</span></span> | <span data-ttu-id="254ce-126">Zaokrouhlená hodnota = 0,10</span><span class="sxs-lookup"><span data-stu-id="254ce-126">Round-off value = 0.10</span></span> | <span data-ttu-id="254ce-127">Zaokrouhlená hodnota = 1,00</span><span class="sxs-lookup"><span data-stu-id="254ce-127">Round-off value = 1.00</span></span> | <span data-ttu-id="254ce-128">Zaokrouhlená hodnota = 100,00</span><span class="sxs-lookup"><span data-stu-id="254ce-128">Round-off value = 100.00</span></span> |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|
| <span data-ttu-id="254ce-129">Normální</span><span class="sxs-lookup"><span data-stu-id="254ce-129">Normal</span></span>                              | <span data-ttu-id="254ce-130">98 765,43</span><span class="sxs-lookup"><span data-stu-id="254ce-130">98,765.43</span></span>              | <span data-ttu-id="254ce-131">98 765,40</span><span class="sxs-lookup"><span data-stu-id="254ce-131">98,765.40</span></span>              | <span data-ttu-id="254ce-132">98 765,00</span><span class="sxs-lookup"><span data-stu-id="254ce-132">98,765.00</span></span>              | <span data-ttu-id="254ce-133">98 800,00</span><span class="sxs-lookup"><span data-stu-id="254ce-133">98,800.00</span></span>                |
| <span data-ttu-id="254ce-134">Dolů</span><span class="sxs-lookup"><span data-stu-id="254ce-134">Downward</span></span>                            | <span data-ttu-id="254ce-135">98 765,43</span><span class="sxs-lookup"><span data-stu-id="254ce-135">98,765.43</span></span>              | <span data-ttu-id="254ce-136">98 765,40</span><span class="sxs-lookup"><span data-stu-id="254ce-136">98,765.40</span></span>              | <span data-ttu-id="254ce-137">98 765,00</span><span class="sxs-lookup"><span data-stu-id="254ce-137">98,765.00</span></span>              | <span data-ttu-id="254ce-138">98 700,00</span><span class="sxs-lookup"><span data-stu-id="254ce-138">98,700.00</span></span>                |
| <span data-ttu-id="254ce-139">Zaokrouhlení nahoru</span><span class="sxs-lookup"><span data-stu-id="254ce-139">Rounding-up</span></span>                         | <span data-ttu-id="254ce-140">98 765,43</span><span class="sxs-lookup"><span data-stu-id="254ce-140">98,765.43</span></span>              | <span data-ttu-id="254ce-141">98 765,50</span><span class="sxs-lookup"><span data-stu-id="254ce-141">98,765.50</span></span>              | <span data-ttu-id="254ce-142">98 766,00</span><span class="sxs-lookup"><span data-stu-id="254ce-142">98,766.00</span></span>              | <span data-ttu-id="254ce-143">98 800,00</span><span class="sxs-lookup"><span data-stu-id="254ce-143">98,800.00</span></span>                |
| <span data-ttu-id="254ce-144">Vlastní výhoda pro kreditní zůstatek</span><span class="sxs-lookup"><span data-stu-id="254ce-144">Own advantage, for a credit balance</span></span> | <span data-ttu-id="254ce-145">98 765,43</span><span class="sxs-lookup"><span data-stu-id="254ce-145">98,765.43</span></span>              | <span data-ttu-id="254ce-146">98 765,40</span><span class="sxs-lookup"><span data-stu-id="254ce-146">98,765.40</span></span>              | <span data-ttu-id="254ce-147">98 765,00</span><span class="sxs-lookup"><span data-stu-id="254ce-147">98,765.00</span></span>              | <span data-ttu-id="254ce-148">98 700,00</span><span class="sxs-lookup"><span data-stu-id="254ce-148">98,700.00</span></span>                |
| <span data-ttu-id="254ce-149">Vlastní výhoda pro debetní zůstatek</span><span class="sxs-lookup"><span data-stu-id="254ce-149">Own advantage, for a debit balance</span></span>  | <span data-ttu-id="254ce-150">98,765.43</span><span class="sxs-lookup"><span data-stu-id="254ce-150">98,765.43</span></span>              | <span data-ttu-id="254ce-151">98,765.50</span><span class="sxs-lookup"><span data-stu-id="254ce-151">98,765.50</span></span>              | <span data-ttu-id="254ce-152">98,766.00</span><span class="sxs-lookup"><span data-stu-id="254ce-152">98,766.00</span></span>              | <span data-ttu-id="254ce-153">98,800.00</span><span class="sxs-lookup"><span data-stu-id="254ce-153">98,800.00</span></span>                |

> [!NOTE]                                                                                  
> <span data-ttu-id="254ce-154">Vyberete-li možnost Vlastní výhoda, zaokrouhlení je vždy ve prospěch právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="254ce-154">If you select Own advantage, the rounding is always to the advantage of the legal entity.</span></span> 

<span data-ttu-id="254ce-155">Další informace naleznete v následujících tématech:</span><span class="sxs-lookup"><span data-stu-id="254ce-155">For more information, see the following topics:</span></span>
- [<span data-ttu-id="254ce-156">Přehled DPH</span><span class="sxs-lookup"><span data-stu-id="254ce-156">Sales tax overview</span></span>](indirect-taxes-overview.md)
- [<span data-ttu-id="254ce-157">Vytvoření platby DPH</span><span class="sxs-lookup"><span data-stu-id="254ce-157">Create a sales tax payment</span></span>](tasks/create-sales-tax-payment.md)
- [<span data-ttu-id="254ce-158">Vytváření obchodních transakcí v dokladech</span><span class="sxs-lookup"><span data-stu-id="254ce-158">Create sales transactions on documents</span></span>](tasks/create-sales-tax-transactions-documents.md)
- [<span data-ttu-id="254ce-159">Zobrazení zaúčtovaných transakcí DPH</span><span class="sxs-lookup"><span data-stu-id="254ce-159">View posted sales tax transactions</span></span>](tasks/view-posted-sales-tax-transactions.md)


