---
title: Finanční sestavy předvah
description: Tento článek popisuje výchozí sestavy pro předvahy. Popisuje také stavební bloky, které jsou přidruženy k těmto sestavám, a způsob změn sestav tak, aby odpovídaly vašim obchodním požadavkům.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5fd4512b02070415b6228c91b66635815dbacaa2
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175323"
---
# <a name="trial-balance-financial-reports"></a><span data-ttu-id="323f9-104">Finanční sestavy předvah</span><span class="sxs-lookup"><span data-stu-id="323f9-104">Trial balance financial reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="323f9-105">Tento článek popisuje výchozí sestavy pro předvahy.</span><span class="sxs-lookup"><span data-stu-id="323f9-105">This article describes the default reports for trial balances.</span></span> <span data-ttu-id="323f9-106">Popisuje také stavební bloky, které jsou přidruženy k těmto sestavám, a způsob změn sestav tak, aby odpovídaly vašim obchodním požadavkům.</span><span class="sxs-lookup"><span data-stu-id="323f9-106">It also describes the building blocks that are associated with these reports and how you can modify the reports to fit your business requirements.</span></span> 

<a name="default-trial-balance-reports"></a><span data-ttu-id="323f9-107">Výchozí finanční sestavy předvah</span><span class="sxs-lookup"><span data-stu-id="323f9-107">Default trial balance reports</span></span>
-----------------------------

<span data-ttu-id="323f9-108">Ve finančním vykazování existují tři sestavy předvah.</span><span class="sxs-lookup"><span data-stu-id="323f9-108">Three trial balance reports are available in Financial reporting.</span></span>

| <span data-ttu-id="323f9-109">Výchozí sestava</span><span class="sxs-lookup"><span data-stu-id="323f9-109">Default report</span></span>                                 | <span data-ttu-id="323f9-110">Jak funguje</span><span class="sxs-lookup"><span data-stu-id="323f9-110">What it does</span></span>                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="323f9-111">Podrobná předvaha – výchozí</span><span class="sxs-lookup"><span data-stu-id="323f9-111">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="323f9-112">Obsahuje informace o zůstatku na všech účtech, včetně zůstatků má dáti a dal a jejich čisté hodnoty, spolu s datem transakce, dokladu a popisem deníku.</span><span class="sxs-lookup"><span data-stu-id="323f9-112">Provides balance information for all accounts, and includes debit and credit balances, and the net of these, together with the transaction date, voucher, and journal description.</span></span>                  |
| <span data-ttu-id="323f9-113">Souhrnná předvaha – výchozí</span><span class="sxs-lookup"><span data-stu-id="323f9-113">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="323f9-114">Obsahuje informace o zůstatku pro všechny účty a zahrnuje počáteční a závěrkové zůstatky a zůstatky za má dáti a dal spolu s jejich čistým rozdílem.</span><span class="sxs-lookup"><span data-stu-id="323f9-114">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference.</span></span>                                        |
| <span data-ttu-id="323f9-115">Souhrnná roční předvaha – výchozí</span><span class="sxs-lookup"><span data-stu-id="323f9-115">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="323f9-116">Obsahuje informace o zůstatku pro všechny účty a zahrnuje počáteční a závěrkové zůstatky a zůstatky za má dáti a dal spolu s jejich čistým rozdílem pro aktuální a minulý rok.</span><span class="sxs-lookup"><span data-stu-id="323f9-116">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference for the current year and the past year.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="323f9-117">Stavební bloky</span><span class="sxs-lookup"><span data-stu-id="323f9-117">Building blocks</span></span>
<span data-ttu-id="323f9-118">Finanční sestavy předvahy používají následující stavební bloky.</span><span class="sxs-lookup"><span data-stu-id="323f9-118">The trial balance financial reports use the following building blocks.</span></span>

| <span data-ttu-id="323f9-119">Výchozí sestava</span><span class="sxs-lookup"><span data-stu-id="323f9-119">Default report</span></span>                                 | <span data-ttu-id="323f9-120">Definice řádku</span><span class="sxs-lookup"><span data-stu-id="323f9-120">Row definition</span></span>          | <span data-ttu-id="323f9-121">Definice sloupce</span><span class="sxs-lookup"><span data-stu-id="323f9-121">Column definition</span></span>                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| <span data-ttu-id="323f9-122">Podrobná předvaha – výchozí</span><span class="sxs-lookup"><span data-stu-id="323f9-122">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="323f9-123">Předvaha – výchozí</span><span class="sxs-lookup"><span data-stu-id="323f9-123">Trial Balance - Default</span></span> | <span data-ttu-id="323f9-124">Podrobná předvaha – výchozí</span><span class="sxs-lookup"><span data-stu-id="323f9-124">Detailed Trial Balance - Default</span></span>               |
| <span data-ttu-id="323f9-125">Souhrnná předvaha – výchozí</span><span class="sxs-lookup"><span data-stu-id="323f9-125">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="323f9-126">Předvaha – výchozí</span><span class="sxs-lookup"><span data-stu-id="323f9-126">Trial Balance - Default</span></span> | <span data-ttu-id="323f9-127">Souhrnná předvaha – výchozí</span><span class="sxs-lookup"><span data-stu-id="323f9-127">Summary Trial Balance - Default</span></span>                |
| <span data-ttu-id="323f9-128">Souhrnná roční předvaha – výchozí</span><span class="sxs-lookup"><span data-stu-id="323f9-128">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="323f9-129">Předvaha – výchozí</span><span class="sxs-lookup"><span data-stu-id="323f9-129">Trial Balance - Default</span></span> | <span data-ttu-id="323f9-130">Souhrnná roční předvaha – výchozí</span><span class="sxs-lookup"><span data-stu-id="323f9-130">Summary Trial Balance Year Over Year - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="323f9-131">Definice řádku</span><span class="sxs-lookup"><span data-stu-id="323f9-131">Row definition</span></span>

<span data-ttu-id="323f9-132">Definice řádku, předvaha – výchozí nastavení, obsahuje jediný řádek, který se shromažďuje ve všech hlavních účtech.</span><span class="sxs-lookup"><span data-stu-id="323f9-132">The row definition, Trial Balance – Default, contains a single row that pulls in all main accounts.</span></span> <span data-ttu-id="323f9-133">Z toho vyplývá, že každý může generovat sestavu bez nutnosti provádět změny.</span><span class="sxs-lookup"><span data-stu-id="323f9-133">Therefore, anyone can generate the report without having to make any modifications.</span></span> <span data-ttu-id="323f9-134">Při zobrazení sestavy přejděte do jednoho řádku a podívejte se na podrobnosti o jednotlivých účtech.</span><span class="sxs-lookup"><span data-stu-id="323f9-134">When you view the report, you drill into the single row to see details about each account.</span></span> <span data-ttu-id="323f9-135">Definici řádku můžete upravit tak, aby obsahovala více podrobností.</span><span class="sxs-lookup"><span data-stu-id="323f9-135">You can modify the row definition so that it includes more detail.</span></span> <span data-ttu-id="323f9-136">Chcete-li změnit řádek definice Předvaha – výchozí, aby obsahoval řádky všech účtů, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="323f9-136">To modify the Trial Balance – Default row definition so that it includes rows for all accounts, follow these steps.</span></span>

1.  <span data-ttu-id="323f9-137">Klikněte na tlačítko **Upravit** a poté klikněte na tlačítko **Vložit řádky z dimenzí**.</span><span class="sxs-lookup"><span data-stu-id="323f9-137">Click **Edit**, and then click **Insert Rows from Dimensions**.</span></span> <span data-ttu-id="323f9-138">Příkaz **Vložit řádky z dimenzí** umožňuje vybrat dimenze, které mají být v definici řádku.</span><span class="sxs-lookup"><span data-stu-id="323f9-138">The **Insert Rows from Dimensions** command lets you choose the dimensions that you want to have in your row definition.</span></span> <span data-ttu-id="323f9-139">Pro tuto definici řádku použijete **hlavní účet**.</span><span class="sxs-lookup"><span data-stu-id="323f9-139">For this row definition, you're going to use **Main Account**.</span></span>
2.  <span data-ttu-id="323f9-140">Ujistěte se, že **hlavní účet** obsahuje všechny ampersandy (&), a klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="323f9-140">Make sure that **Main Account** contains all ampersands (&), and then click **OK**.</span></span>

<span data-ttu-id="323f9-141">Definice řádku nyní obsahuje všechny hlavní účty pro výchozí právnickou osobu.</span><span class="sxs-lookup"><span data-stu-id="323f9-141">The row definition now contains all the main accounts for your default legal entity.</span></span>

### <a name="column-definition"></a><span data-ttu-id="323f9-142">Definice sloupce</span><span class="sxs-lookup"><span data-stu-id="323f9-142">Column definition</span></span>

<span data-ttu-id="323f9-143">Každá sestavu předvahy používá jinou definici sloupců.</span><span class="sxs-lookup"><span data-stu-id="323f9-143">Each trial balance report uses a different column definition.</span></span> <span data-ttu-id="323f9-144">Tyto definice sloupců obsahují různé typy sloupců, které poskytují různé úrovně podrobností a finanční údaje.</span><span class="sxs-lookup"><span data-stu-id="323f9-144">These column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="323f9-145">**Podrobná předvaha – výchozí typy sloupce:**</span><span class="sxs-lookup"><span data-stu-id="323f9-145">**Detailed Trial Balance – Default column types:**</span></span>
    -   <span data-ttu-id="323f9-146">**DESC** – popis z definice řádku</span><span class="sxs-lookup"><span data-stu-id="323f9-146">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="323f9-147">**ACCT** – kódy účtů</span><span class="sxs-lookup"><span data-stu-id="323f9-147">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="323f9-148">**ATTR (3)** – atributy:</span><span class="sxs-lookup"><span data-stu-id="323f9-148">**ATTR (3)** – Attributes:</span></span>
        -   <span data-ttu-id="323f9-149">Datum transakce</span><span class="sxs-lookup"><span data-stu-id="323f9-149">Transaction Date</span></span>
        -   <span data-ttu-id="323f9-150">Doklad</span><span class="sxs-lookup"><span data-stu-id="323f9-150">Voucher</span></span>
        -   <span data-ttu-id="323f9-151">Popis deníku</span><span class="sxs-lookup"><span data-stu-id="323f9-151">Journal Description</span></span>
    -   <span data-ttu-id="323f9-152">**FD** – finanční data, která obsahují pouze položky má dáti</span><span class="sxs-lookup"><span data-stu-id="323f9-152">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="323f9-153">**FD** – finanční data, která obsahují pouze položky dal</span><span class="sxs-lookup"><span data-stu-id="323f9-153">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="323f9-154">**CALC** – čistý rozdíl</span><span class="sxs-lookup"><span data-stu-id="323f9-154">**CALC** – The net difference</span></span>
-   <span data-ttu-id="323f9-155">**Podrobná předvaha – výchozí typy sloupců:**</span><span class="sxs-lookup"><span data-stu-id="323f9-155">**Summary Trial Balance – Default columns types:**</span></span>
    -   <span data-ttu-id="323f9-156">**ACCT** – kódy účtů</span><span class="sxs-lookup"><span data-stu-id="323f9-156">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="323f9-157">**DESC** – popis z definice řádku</span><span class="sxs-lookup"><span data-stu-id="323f9-157">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="323f9-158">**ATTR** – atribut:</span><span class="sxs-lookup"><span data-stu-id="323f9-158">**ATTR** – An attribute:</span></span>
        -   <span data-ttu-id="323f9-159">Doklad</span><span class="sxs-lookup"><span data-stu-id="323f9-159">Voucher</span></span>
    -   <span data-ttu-id="323f9-160">**FD** – počáteční zůstatek finančních dat</span><span class="sxs-lookup"><span data-stu-id="323f9-160">**FD** – The beginning balance financial data</span></span>
    -   <span data-ttu-id="323f9-161">**FD** – finanční data, která obsahují pouze položky má dáti</span><span class="sxs-lookup"><span data-stu-id="323f9-161">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="323f9-162">**FD** – finanční data, která obsahují pouze položky dal</span><span class="sxs-lookup"><span data-stu-id="323f9-162">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="323f9-163">**CALC** – čistý rozdíl</span><span class="sxs-lookup"><span data-stu-id="323f9-163">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="323f9-164">**CALC** – konečný zůstatek</span><span class="sxs-lookup"><span data-stu-id="323f9-164">**CALC** – The closing balance</span></span>
-   <span data-ttu-id="323f9-165">**Souhrnná roční předvaha – výchozí**</span><span class="sxs-lookup"><span data-stu-id="323f9-165">**Summary Trial Balance Year Over Year – Default:**</span></span>
    -   <span data-ttu-id="323f9-166">**ACCT** – kódy účtů</span><span class="sxs-lookup"><span data-stu-id="323f9-166">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="323f9-167">**DESC** – popis z definice řádku</span><span class="sxs-lookup"><span data-stu-id="323f9-167">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="323f9-168">**ATTR** – atribut</span><span class="sxs-lookup"><span data-stu-id="323f9-168">**ATTR** – An attribute</span></span>
        -   <span data-ttu-id="323f9-169">Doklad</span><span class="sxs-lookup"><span data-stu-id="323f9-169">Voucher</span></span>
    -   <span data-ttu-id="323f9-170">**FD** – Finanční zůstatek od začátku roku pro aktuální rok</span><span class="sxs-lookup"><span data-stu-id="323f9-170">**FD** – The beginning balance financial data for the current year</span></span>
    -   <span data-ttu-id="323f9-171">**FD** – finanční data, která obsahují pouze položky má dáti pro aktuální rok</span><span class="sxs-lookup"><span data-stu-id="323f9-171">**FD** – Financial data that contains only debits for the current year</span></span>
    -   <span data-ttu-id="323f9-172">**FD** – finanční data, která obsahují pouze položky dal pro aktuální rok</span><span class="sxs-lookup"><span data-stu-id="323f9-172">**FD** – Financial data that contains only credits for the current year</span></span>
    -   <span data-ttu-id="323f9-173">**CALC** – čistý rozdíl</span><span class="sxs-lookup"><span data-stu-id="323f9-173">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="323f9-174">**CALC** – konečný zůstatek</span><span class="sxs-lookup"><span data-stu-id="323f9-174">**CALC** – The closing balance</span></span>
    -   <span data-ttu-id="323f9-175">**FD** – finanční data, která obsahují pouze položky má dáti pro předchozí rok</span><span class="sxs-lookup"><span data-stu-id="323f9-175">**FD** – Financial data that contains only debits for the last year</span></span>
    -   <span data-ttu-id="323f9-176">**FD** – finanční data, která obsahují pouze položky dal pro předchozí rok</span><span class="sxs-lookup"><span data-stu-id="323f9-176">**FD** – Financial data that contains only credits for the last year</span></span>



<a name="additional-resources"></a><span data-ttu-id="323f9-177">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="323f9-177">Additional resources</span></span>
--------

[<span data-ttu-id="323f9-178">Finanční výkaznictví</span><span class="sxs-lookup"><span data-stu-id="323f9-178">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="323f9-179">Zobrazení finančních sestav</span><span class="sxs-lookup"><span data-stu-id="323f9-179">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="323f9-180">Blog o finančním výkaznictví v Dynamics</span><span class="sxs-lookup"><span data-stu-id="323f9-180">Dynamics Financial Reporting Blog</span></span>](https://blogs.msdn.com/b/dynamics_financial_reporting/)



