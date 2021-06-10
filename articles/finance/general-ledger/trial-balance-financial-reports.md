---
title: Finanční sestavy předvah
description: Tento článek popisuje výchozí sestavy pro předvahy. Popisuje také stavební bloky, které jsou přidruženy k těmto sestavám, a způsob změn sestav tak, aby odpovídaly vašim obchodním požadavkům.
author: jinniew
ms.date: 05/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 26ec03422315a280f7e779f992cf694eb5f845ea
ms.sourcegitcommit: 365092f735310990e82516110141d42aaf04e654
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/27/2021
ms.locfileid: "6103651"
---
# <a name="trial-balance-financial-reports"></a><span data-ttu-id="a0cb0-104">Finanční sestavy předvah</span><span class="sxs-lookup"><span data-stu-id="a0cb0-104">Trial balance financial reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a0cb0-105">Tento článek popisuje výchozí sestavy pro předvahy.</span><span class="sxs-lookup"><span data-stu-id="a0cb0-105">This article describes the default reports for trial balances.</span></span> <span data-ttu-id="a0cb0-106">Popisuje také stavební bloky, které jsou přidruženy k těmto sestavám, a způsob změn sestav tak, aby odpovídaly vašim obchodním požadavkům.</span><span class="sxs-lookup"><span data-stu-id="a0cb0-106">It also describes the building blocks that are associated with these reports and how you can modify the reports to fit your business requirements.</span></span> 

## <a name="default-trial-balance-reports"></a><span data-ttu-id="a0cb0-107">Výchozí finanční sestavy předvah</span><span class="sxs-lookup"><span data-stu-id="a0cb0-107">Default trial balance reports</span></span>

<span data-ttu-id="a0cb0-108">Ve finančním vykazování existují tři sestavy předvah.</span><span class="sxs-lookup"><span data-stu-id="a0cb0-108">Three trial balance reports are available in Financial reporting.</span></span>

| <span data-ttu-id="a0cb0-109">Výchozí sestava</span><span class="sxs-lookup"><span data-stu-id="a0cb0-109">Default report</span></span>                                 | <span data-ttu-id="a0cb0-110">Jak funguje</span><span class="sxs-lookup"><span data-stu-id="a0cb0-110">What it does</span></span>                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0cb0-111">Podrobná předvaha – výchozí</span><span class="sxs-lookup"><span data-stu-id="a0cb0-111">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="a0cb0-112">Obsahuje informace o zůstatku na všech účtech, včetně zůstatků má dáti a dal a jejich čisté hodnoty, spolu s datem transakce, dokladu a popisem deníku.</span><span class="sxs-lookup"><span data-stu-id="a0cb0-112">Provides balance information for all accounts, and includes debit and credit balances, and the net of these, together with the transaction date, voucher, and journal description.</span></span>                  |
| <span data-ttu-id="a0cb0-113">Souhrnná předvaha – výchozí</span><span class="sxs-lookup"><span data-stu-id="a0cb0-113">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="a0cb0-114">Obsahuje informace o zůstatku pro všechny účty a zahrnuje počáteční a závěrkové zůstatky a zůstatky za má dáti a dal spolu s jejich čistým rozdílem.</span><span class="sxs-lookup"><span data-stu-id="a0cb0-114">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference.</span></span>                                        |
| <span data-ttu-id="a0cb0-115">Souhrnná roční předvaha – výchozí</span><span class="sxs-lookup"><span data-stu-id="a0cb0-115">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="a0cb0-116">Obsahuje informace o zůstatku pro všechny účty a zahrnuje počáteční a závěrkové zůstatky a zůstatky za má dáti a dal spolu s jejich čistým rozdílem pro aktuální a minulý rok.</span><span class="sxs-lookup"><span data-stu-id="a0cb0-116">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference for the current year and the past year.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="a0cb0-117">Stavební bloky</span><span class="sxs-lookup"><span data-stu-id="a0cb0-117">Building blocks</span></span>
<span data-ttu-id="a0cb0-118">Finanční sestavy předvahy používají následující stavební bloky.</span><span class="sxs-lookup"><span data-stu-id="a0cb0-118">The trial balance financial reports use the following building blocks.</span></span>

| <span data-ttu-id="a0cb0-119">Výchozí sestava</span><span class="sxs-lookup"><span data-stu-id="a0cb0-119">Default report</span></span>                                 | <span data-ttu-id="a0cb0-120">Definice řádku</span><span class="sxs-lookup"><span data-stu-id="a0cb0-120">Row definition</span></span>          | <span data-ttu-id="a0cb0-121">Definice sloupce</span><span class="sxs-lookup"><span data-stu-id="a0cb0-121">Column definition</span></span>                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| <span data-ttu-id="a0cb0-122">Podrobná předvaha – výchozí</span><span class="sxs-lookup"><span data-stu-id="a0cb0-122">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="a0cb0-123">Předvaha – výchozí</span><span class="sxs-lookup"><span data-stu-id="a0cb0-123">Trial Balance - Default</span></span> | <span data-ttu-id="a0cb0-124">Podrobná předvaha – výchozí</span><span class="sxs-lookup"><span data-stu-id="a0cb0-124">Detailed Trial Balance - Default</span></span>               |
| <span data-ttu-id="a0cb0-125">Souhrnná předvaha – výchozí</span><span class="sxs-lookup"><span data-stu-id="a0cb0-125">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="a0cb0-126">Předvaha – výchozí</span><span class="sxs-lookup"><span data-stu-id="a0cb0-126">Trial Balance - Default</span></span> | <span data-ttu-id="a0cb0-127">Souhrnná předvaha – výchozí</span><span class="sxs-lookup"><span data-stu-id="a0cb0-127">Summary Trial Balance - Default</span></span>                |
| <span data-ttu-id="a0cb0-128">Souhrnná roční předvaha – výchozí</span><span class="sxs-lookup"><span data-stu-id="a0cb0-128">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="a0cb0-129">Předvaha – výchozí</span><span class="sxs-lookup"><span data-stu-id="a0cb0-129">Trial Balance - Default</span></span> | <span data-ttu-id="a0cb0-130">Souhrnná roční předvaha – výchozí</span><span class="sxs-lookup"><span data-stu-id="a0cb0-130">Summary Trial Balance Year Over Year - Default</span></span> |

> [!NOTE] 
> <span data-ttu-id="a0cb0-131">Při spuštění sestavy **Zkušební zůstatek** ve Financial Reporting nezapomeňte zaškrtnout políčka pro **Zobrazit řádky bez částek** a **Zobrazit sestavy bez aktivních řádků** na kartě **Nastavení**.</span><span class="sxs-lookup"><span data-stu-id="a0cb0-131">When running the **Trial Balance** report in Financial reporting, be sure to select the check boxes for **Display rows with no amounts** and **Display reports with no active rows** on the **Settings** tab.</span></span>

### <a name="row-definition"></a><span data-ttu-id="a0cb0-132">Definice řádku</span><span class="sxs-lookup"><span data-stu-id="a0cb0-132">Row definition</span></span>

<span data-ttu-id="a0cb0-133">Definice řádku, předvaha – výchozí nastavení, obsahuje jediný řádek, který se shromažďuje ve všech hlavních účtech.</span><span class="sxs-lookup"><span data-stu-id="a0cb0-133">The row definition, Trial Balance – Default, contains a single row that pulls in all main accounts.</span></span> <span data-ttu-id="a0cb0-134">Z toho vyplývá, že každý může generovat sestavu bez nutnosti provádět změny.</span><span class="sxs-lookup"><span data-stu-id="a0cb0-134">Therefore, anyone can generate the report without having to make any modifications.</span></span> <span data-ttu-id="a0cb0-135">Při zobrazení sestavy přejděte do jednoho řádku a podívejte se na podrobnosti o jednotlivých účtech.</span><span class="sxs-lookup"><span data-stu-id="a0cb0-135">When you view the report, you drill into the single row to see details about each account.</span></span> <span data-ttu-id="a0cb0-136">Definici řádku můžete upravit tak, aby obsahovala více podrobností.</span><span class="sxs-lookup"><span data-stu-id="a0cb0-136">You can modify the row definition so that it includes more detail.</span></span> <span data-ttu-id="a0cb0-137">Chcete-li změnit řádek definice Předvaha – výchozí, aby obsahoval řádky všech účtů, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="a0cb0-137">To modify the Trial Balance – Default row definition so that it includes rows for all accounts, follow these steps.</span></span>

1.  <span data-ttu-id="a0cb0-138">Klikněte na tlačítko **Upravit** a poté klikněte na tlačítko **Vložit řádky z dimenzí**.</span><span class="sxs-lookup"><span data-stu-id="a0cb0-138">Click **Edit**, and then click **Insert Rows from Dimensions**.</span></span> <span data-ttu-id="a0cb0-139">Příkaz **Vložit řádky z dimenzí** umožňuje vybrat dimenze, které mají být v definici řádku.</span><span class="sxs-lookup"><span data-stu-id="a0cb0-139">The **Insert Rows from Dimensions** command lets you choose the dimensions that you want to have in your row definition.</span></span> <span data-ttu-id="a0cb0-140">Pro tuto definici řádku použijete **hlavní účet**.</span><span class="sxs-lookup"><span data-stu-id="a0cb0-140">For this row definition, you're going to use **Main Account**.</span></span>
2.  <span data-ttu-id="a0cb0-141">Ujistěte se, že **hlavní účet** obsahuje všechny ampersandy (&), a klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="a0cb0-141">Make sure that **Main Account** contains all ampersands (&), and then click **OK**.</span></span>

<span data-ttu-id="a0cb0-142">Definice řádku nyní obsahuje všechny hlavní účty pro výchozí právnickou osobu.</span><span class="sxs-lookup"><span data-stu-id="a0cb0-142">The row definition now contains all the main accounts for your default legal entity.</span></span>

### <a name="column-definition"></a><span data-ttu-id="a0cb0-143">Definice sloupce</span><span class="sxs-lookup"><span data-stu-id="a0cb0-143">Column definition</span></span>

<span data-ttu-id="a0cb0-144">Každá sestavu předvahy používá jinou definici sloupců.</span><span class="sxs-lookup"><span data-stu-id="a0cb0-144">Each trial balance report uses a different column definition.</span></span> <span data-ttu-id="a0cb0-145">Tyto definice sloupců obsahují různé typy sloupců, které poskytují různé úrovně podrobností a finanční údaje.</span><span class="sxs-lookup"><span data-stu-id="a0cb0-145">These column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="a0cb0-146">**Podrobná předvaha – výchozí typy sloupce:**</span><span class="sxs-lookup"><span data-stu-id="a0cb0-146">**Detailed Trial Balance – Default column types:**</span></span>
    -   <span data-ttu-id="a0cb0-147">**DESC** – popis z definice řádku</span><span class="sxs-lookup"><span data-stu-id="a0cb0-147">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="a0cb0-148">**ACCT** – kódy účtů</span><span class="sxs-lookup"><span data-stu-id="a0cb0-148">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="a0cb0-149">**ATTR (3)** – atributy:</span><span class="sxs-lookup"><span data-stu-id="a0cb0-149">**ATTR (3)** – Attributes:</span></span>
        -   <span data-ttu-id="a0cb0-150">Datum transakce</span><span class="sxs-lookup"><span data-stu-id="a0cb0-150">Transaction Date</span></span>
        -   <span data-ttu-id="a0cb0-151">Doklad</span><span class="sxs-lookup"><span data-stu-id="a0cb0-151">Voucher</span></span>
        -   <span data-ttu-id="a0cb0-152">Popis deníku</span><span class="sxs-lookup"><span data-stu-id="a0cb0-152">Journal Description</span></span>
    -   <span data-ttu-id="a0cb0-153">**FD** – finanční data, která obsahují pouze položky má dáti</span><span class="sxs-lookup"><span data-stu-id="a0cb0-153">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="a0cb0-154">**FD** – finanční data, která obsahují pouze položky dal</span><span class="sxs-lookup"><span data-stu-id="a0cb0-154">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="a0cb0-155">**CALC** – čistý rozdíl</span><span class="sxs-lookup"><span data-stu-id="a0cb0-155">**CALC** – The net difference</span></span>
-   <span data-ttu-id="a0cb0-156">**Podrobná předvaha – výchozí typy sloupců:**</span><span class="sxs-lookup"><span data-stu-id="a0cb0-156">**Summary Trial Balance – Default columns types:**</span></span>
    -   <span data-ttu-id="a0cb0-157">**ACCT** – kódy účtů</span><span class="sxs-lookup"><span data-stu-id="a0cb0-157">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="a0cb0-158">**DESC** – popis z definice řádku</span><span class="sxs-lookup"><span data-stu-id="a0cb0-158">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="a0cb0-159">**ATTR** – atribut:</span><span class="sxs-lookup"><span data-stu-id="a0cb0-159">**ATTR** – An attribute:</span></span>
        -   <span data-ttu-id="a0cb0-160">Doklad</span><span class="sxs-lookup"><span data-stu-id="a0cb0-160">Voucher</span></span>
    -   <span data-ttu-id="a0cb0-161">**FD** – počáteční zůstatek finančních dat</span><span class="sxs-lookup"><span data-stu-id="a0cb0-161">**FD** – The beginning balance financial data</span></span>
    -   <span data-ttu-id="a0cb0-162">**FD** – finanční data, která obsahují pouze položky má dáti</span><span class="sxs-lookup"><span data-stu-id="a0cb0-162">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="a0cb0-163">**FD** – finanční data, která obsahují pouze položky dal</span><span class="sxs-lookup"><span data-stu-id="a0cb0-163">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="a0cb0-164">**CALC** – čistý rozdíl</span><span class="sxs-lookup"><span data-stu-id="a0cb0-164">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="a0cb0-165">**CALC** – konečný zůstatek</span><span class="sxs-lookup"><span data-stu-id="a0cb0-165">**CALC** – The closing balance</span></span>
-   <span data-ttu-id="a0cb0-166">**Souhrnná roční předvaha – výchozí**</span><span class="sxs-lookup"><span data-stu-id="a0cb0-166">**Summary Trial Balance Year Over Year – Default:**</span></span>
    -   <span data-ttu-id="a0cb0-167">**ACCT** – kódy účtů</span><span class="sxs-lookup"><span data-stu-id="a0cb0-167">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="a0cb0-168">**DESC** – popis z definice řádku</span><span class="sxs-lookup"><span data-stu-id="a0cb0-168">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="a0cb0-169">**ATTR** – atribut</span><span class="sxs-lookup"><span data-stu-id="a0cb0-169">**ATTR** – An attribute</span></span>
        -   <span data-ttu-id="a0cb0-170">Doklad</span><span class="sxs-lookup"><span data-stu-id="a0cb0-170">Voucher</span></span>
    -   <span data-ttu-id="a0cb0-171">**FD** – Finanční zůstatek od začátku roku pro aktuální rok</span><span class="sxs-lookup"><span data-stu-id="a0cb0-171">**FD** – The beginning balance financial data for the current year</span></span>
    -   <span data-ttu-id="a0cb0-172">**FD** – finanční data, která obsahují pouze položky má dáti pro aktuální rok</span><span class="sxs-lookup"><span data-stu-id="a0cb0-172">**FD** – Financial data that contains only debits for the current year</span></span>
    -   <span data-ttu-id="a0cb0-173">**FD** – finanční data, která obsahují pouze položky dal pro aktuální rok</span><span class="sxs-lookup"><span data-stu-id="a0cb0-173">**FD** – Financial data that contains only credits for the current year</span></span>
    -   <span data-ttu-id="a0cb0-174">**CALC** – čistý rozdíl</span><span class="sxs-lookup"><span data-stu-id="a0cb0-174">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="a0cb0-175">**CALC** – konečný zůstatek</span><span class="sxs-lookup"><span data-stu-id="a0cb0-175">**CALC** – The closing balance</span></span>
    -   <span data-ttu-id="a0cb0-176">**FD** – finanční data, která obsahují pouze položky má dáti pro předchozí rok</span><span class="sxs-lookup"><span data-stu-id="a0cb0-176">**FD** – Financial data that contains only debits for the last year</span></span>
    -   <span data-ttu-id="a0cb0-177">**FD** – finanční data, která obsahují pouze položky dal pro předchozí rok</span><span class="sxs-lookup"><span data-stu-id="a0cb0-177">**FD** – Financial data that contains only credits for the last year</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a0cb0-178">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="a0cb0-178">Additional resources</span></span>

[<span data-ttu-id="a0cb0-179">Přehled finančního výkaznictví</span><span class="sxs-lookup"><span data-stu-id="a0cb0-179">Financial reporting overview</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="a0cb0-180">Zobrazení finančních sestav</span><span class="sxs-lookup"><span data-stu-id="a0cb0-180">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="a0cb0-181">Blog o finančním výkaznictví v Dynamics</span><span class="sxs-lookup"><span data-stu-id="a0cb0-181">Dynamics Financial Reporting Blog</span></span>](https://blogs.msdn.com/b/dynamics_financial_reporting/)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
