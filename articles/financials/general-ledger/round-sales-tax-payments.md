---
title: "Platby DPH a pravidla zaokrouhlení"
description: "Tento článek vysvětluje princip nastavení pravidla zaokrouhlování v rámci finančních DPH, a zaokrouhlení zůstatku DPH během úlohy Vyrovnat a zaúčtovat DPH."
author: twheeloc
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 13470282efc6b9135e86355cf8071b841aad3071
ms.contentlocale: cs-cz
ms.lasthandoff: 11/03/2017

---

# <a name="sales-tax-payments-and-rounding-rules"></a><span data-ttu-id="19313-103">Platby DPH a pravidla zaokrouhlení</span><span class="sxs-lookup"><span data-stu-id="19313-103">Sales tax payments and rounding rules</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="19313-104">Tento článek vysvětluje princip nastavení pravidla zaokrouhlování v rámci finančních DPH, a zaokrouhlení zůstatku DPH během úlohy Vyrovnat a zaúčtovat DPH.</span><span class="sxs-lookup"><span data-stu-id="19313-104">This article explains how the rounding rule setup on the Sales tax authorities works and rounding the sales tax balance during the Settle and post sales tax job.</span></span>

<span data-ttu-id="19313-105">DPH musí být vykázána a zaplacena v pravidelných intervalech finančnímu úřadu.</span><span class="sxs-lookup"><span data-stu-id="19313-105">Periodically, sales tax needs to be reported and paid to tax authorities.</span></span> <span data-ttu-id="19313-106">Toto lze provést spuštěním procesu vyúčtování a následného poprodejního daňového procesu na stránce Daň z prodeje.</span><span class="sxs-lookup"><span data-stu-id="19313-106">This can be done by running the settle and post sales tax process in the Sales tax page.</span></span> <span data-ttu-id="19313-107">Daň z prodeje za určité období bude vypořádána proti účtům daně z prodeje a zůstatek daně z prodeje bude účtován na účet vypořádání daně z prodeje.</span><span class="sxs-lookup"><span data-stu-id="19313-107">Sales tax for a period will be settled against the sales tax accounts and the sales tax balance will be posted to the Sales tax settlement account.</span></span> <span data-ttu-id="19313-108">Zůstatek DPH, který se zaúčtuje na účet pro vyrovnání DPH, je možné zaokrouhlit podle požadavků finančního úřadu nastavením pravidla zaokrouhlování na stránce DPH.</span><span class="sxs-lookup"><span data-stu-id="19313-108">The sales tax balance, which is posted on the Sales tax settlement account, can be rounded as required by tax authorities by setting up a rounding rule on the Sales tax page.</span></span> 

<span data-ttu-id="19313-109">Rozdíl v zaokrouhlení se zaúčtuje na účet pro zaokrouhlení DPH, který je vybrán v poli Účty pro automatické transakce v hlavní knize.</span><span class="sxs-lookup"><span data-stu-id="19313-109">The rounding difference is posted to the Sales tax rounding account that is selected in the Accounts for automatic transactions field in the General ledger.</span></span>

<span data-ttu-id="19313-110">Níže naleznete příklady popisující princip pravidla zaokrouhlování pro finanční úřad.</span><span class="sxs-lookup"><span data-stu-id="19313-110">The below example illustrates how the rounding rule on Sales tax authority works.</span></span>

### <a name="example"></a><span data-ttu-id="19313-111">Příklad:</span><span class="sxs-lookup"><span data-stu-id="19313-111">Example:</span></span>

<span data-ttu-id="19313-112">Celková částka DPH pro období se zobrazí jako kreditní zůstatek -98 765,43.</span><span class="sxs-lookup"><span data-stu-id="19313-112">The total sales tax for a period shows a credit balance of -98,765.43.</span></span> <span data-ttu-id="19313-113">Právnická osoba shromáždila vyšší částku DPH než kolik zaplatila.</span><span class="sxs-lookup"><span data-stu-id="19313-113">The legal entity collected more sales taxes than it paid.</span></span> <span data-ttu-id="19313-114">Proto právnická osoba dluží peníze daňovému úřadu.</span><span class="sxs-lookup"><span data-stu-id="19313-114">Therefore, the legal entity owes money to the tax authority.</span></span> 

<span data-ttu-id="19313-115">Právnická osoba chce použít metodu zaokrouhlení, která zaokrouhluje zůstatek na nejbližší násobek 1,00.</span><span class="sxs-lookup"><span data-stu-id="19313-115">The legal entity wants to use a rounding method that rounds the balance to the nearest 1.00.</span></span> <span data-ttu-id="19313-116">Uživatel odpovědný za účtování DPH musí provést následující akce.</span><span class="sxs-lookup"><span data-stu-id="19313-116">The user who is responsible for sales tax accounting performs the following steps.</span></span>

1.  <span data-ttu-id="19313-117">Klikněte na Daň &gt; Nepřímé daně &gt; DPH &gt; Finanční úřady</span><span class="sxs-lookup"><span data-stu-id="19313-117">Click Tax &gt; Indirect taxes &gt; Sales tax &gt; Sales tax authorities</span></span>
2.  <span data-ttu-id="19313-118">Na pevné kartě Obecné vybere v poli Způsob zaokrouhlování možnost Normální.</span><span class="sxs-lookup"><span data-stu-id="19313-118">On the General FastTab, select Normal in the Rounding form field.</span></span>
3.  <span data-ttu-id="19313-119">V poli Zaokrouhlení zadejte číslo 1,00.</span><span class="sxs-lookup"><span data-stu-id="19313-119">In the Round-off field, enter 1.00.</span></span>
4.  <span data-ttu-id="19313-120">V době, kdy je nutné zaplatit DPH daňovému úřadu, otevře stránku Vyrovnat a zaúčtovat DPH.</span><span class="sxs-lookup"><span data-stu-id="19313-120">When it is time to pay the sales taxes to the tax authority, open the Settle and post sales tax page.</span></span> <span data-ttu-id="19313-121">(Klikněte na Daň &gt; Přiznání &gt; DPH &gt; Vyrovnat a zaúčtovat DPH.)</span><span class="sxs-lookup"><span data-stu-id="19313-121">(Click Tax &gt; Declarations &gt; Sales tax &gt; Settle and post sales tax.)</span></span>
5.  <span data-ttu-id="19313-122">V účtu pro vyrovnání DPH je částka daňové povinnosti 98 765,43 zaokrouhlena na 98 765.</span><span class="sxs-lookup"><span data-stu-id="19313-122">On the sales tax settlement account, the tax liability amount of 98,765.43 is rounded to 98,765.</span></span>

<span data-ttu-id="19313-123">Následující tabulka ukazuje, jak je zaokrouhlena částka 98 765,43 pomocí každé z metod zaokrouhlení, která je k dispozici v poli Způsob zaokrouhlování na stránce Finanční úřady.</span><span class="sxs-lookup"><span data-stu-id="19313-123">The following table shows how an amount of 98,765.43 is rounded by using each rounding method that is available in the Rounding form field in the Sales tax authorities page.</span></span>

| <span data-ttu-id="19313-124">Možnost zaokrouhlování</span><span class="sxs-lookup"><span data-stu-id="19313-124">Rounding form option</span></span>                | <span data-ttu-id="19313-125">Zaokrouhlená hodnota = 0,01</span><span class="sxs-lookup"><span data-stu-id="19313-125">Round-off value = 0.01</span></span> | <span data-ttu-id="19313-126">Zaokrouhlená hodnota = 0,10</span><span class="sxs-lookup"><span data-stu-id="19313-126">Round-off value = 0.10</span></span> | <span data-ttu-id="19313-127">Zaokrouhlená hodnota = 1,00</span><span class="sxs-lookup"><span data-stu-id="19313-127">Round-off value = 1.00</span></span> | <span data-ttu-id="19313-128">Zaokrouhlená hodnota = 100,00</span><span class="sxs-lookup"><span data-stu-id="19313-128">Round-off value = 100.00</span></span> |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|
| <span data-ttu-id="19313-129">Normální</span><span class="sxs-lookup"><span data-stu-id="19313-129">Normal</span></span>                              | <span data-ttu-id="19313-130">98 765,43</span><span class="sxs-lookup"><span data-stu-id="19313-130">98,765.43</span></span>              | <span data-ttu-id="19313-131">98 765,40</span><span class="sxs-lookup"><span data-stu-id="19313-131">98,765.40</span></span>              | <span data-ttu-id="19313-132">98 765,00</span><span class="sxs-lookup"><span data-stu-id="19313-132">98,765.00</span></span>              | <span data-ttu-id="19313-133">98 800,00</span><span class="sxs-lookup"><span data-stu-id="19313-133">98,800.00</span></span>                |
| <span data-ttu-id="19313-134">Dolů</span><span class="sxs-lookup"><span data-stu-id="19313-134">Downward</span></span>                            | <span data-ttu-id="19313-135">98 765,43</span><span class="sxs-lookup"><span data-stu-id="19313-135">98,765.43</span></span>              | <span data-ttu-id="19313-136">98 765,40</span><span class="sxs-lookup"><span data-stu-id="19313-136">98,765.40</span></span>              | <span data-ttu-id="19313-137">98 765,00</span><span class="sxs-lookup"><span data-stu-id="19313-137">98,765.00</span></span>              | <span data-ttu-id="19313-138">98 700,00</span><span class="sxs-lookup"><span data-stu-id="19313-138">98,700.00</span></span>                |
| <span data-ttu-id="19313-139">Zaokrouhlení nahoru</span><span class="sxs-lookup"><span data-stu-id="19313-139">Rounding-up</span></span>                         | <span data-ttu-id="19313-140">98 765,43</span><span class="sxs-lookup"><span data-stu-id="19313-140">98,765.43</span></span>              | <span data-ttu-id="19313-141">98 765,50</span><span class="sxs-lookup"><span data-stu-id="19313-141">98,765.50</span></span>              | <span data-ttu-id="19313-142">98 766,00</span><span class="sxs-lookup"><span data-stu-id="19313-142">98,766.00</span></span>              | <span data-ttu-id="19313-143">98 800,00</span><span class="sxs-lookup"><span data-stu-id="19313-143">98,800.00</span></span>                |
| <span data-ttu-id="19313-144">Vlastní výhoda pro kreditní zůstatek</span><span class="sxs-lookup"><span data-stu-id="19313-144">Own advantage, for a credit balance</span></span> | <span data-ttu-id="19313-145">98 765,43</span><span class="sxs-lookup"><span data-stu-id="19313-145">98,765.43</span></span>              | <span data-ttu-id="19313-146">98 765,40</span><span class="sxs-lookup"><span data-stu-id="19313-146">98,765.40</span></span>              | <span data-ttu-id="19313-147">98 765,00</span><span class="sxs-lookup"><span data-stu-id="19313-147">98,765.00</span></span>              | <span data-ttu-id="19313-148">98 700,00</span><span class="sxs-lookup"><span data-stu-id="19313-148">98,700.00</span></span>                |
| <span data-ttu-id="19313-149">Vlastní výhoda pro debetní zůstatek</span><span class="sxs-lookup"><span data-stu-id="19313-149">Own advantage, for a debit balance</span></span>  | <span data-ttu-id="19313-150">98,765.43</span><span class="sxs-lookup"><span data-stu-id="19313-150">98,765.43</span></span>              | <span data-ttu-id="19313-151">98,765.50</span><span class="sxs-lookup"><span data-stu-id="19313-151">98,765.50</span></span>              | <span data-ttu-id="19313-152">98,766.00</span><span class="sxs-lookup"><span data-stu-id="19313-152">98,766.00</span></span>              | <span data-ttu-id="19313-153">98,800.00</span><span class="sxs-lookup"><span data-stu-id="19313-153">98,800.00</span></span>                |

> [!NOTE]                                                                                  
> <span data-ttu-id="19313-154">Vyberete-li možnost Vlastní výhoda, zaokrouhlení je vždy ve prospěch právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="19313-154">If you select Own advantage, the rounding is always to the advantage of the legal entity.</span></span> 

<span data-ttu-id="19313-155">Další informace naleznete v následujících tématech:</span><span class="sxs-lookup"><span data-stu-id="19313-155">For more information, see the following topics:</span></span>
- [<span data-ttu-id="19313-156">Přehled DPH</span><span class="sxs-lookup"><span data-stu-id="19313-156">Sales tax overview</span></span>](indirect-taxes-overview.md)
- [<span data-ttu-id="19313-157">Vytvoření platby DPH</span><span class="sxs-lookup"><span data-stu-id="19313-157">Create a sales tax payment</span></span>](tasks/create-sales-tax-payment.md)
- [<span data-ttu-id="19313-158">Vytváření obchodních transakcí v dokladech</span><span class="sxs-lookup"><span data-stu-id="19313-158">Create sales transactions on documents</span></span>](tasks/create-sales-tax-transactions-documents.md)
- [<span data-ttu-id="19313-159">Zobrazení zaúčtovaných transakcí DPH</span><span class="sxs-lookup"><span data-stu-id="19313-159">View posted sales tax transactions</span></span>](tasks/view-posted-sales-tax-transactions.md)



