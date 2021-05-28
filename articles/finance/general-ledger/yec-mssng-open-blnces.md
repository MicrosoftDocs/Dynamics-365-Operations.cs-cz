---
title: Chybějící počáteční zůstatky roční uzávěrky
description: Toto téma vysvětluje, proč mohou při uzavírání roku chybět počáteční zůstatky a jak tyto zůstatky znovu vytvořit, pokud chybí.
author: kweekley
ms.date: 05/12/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 045d0bf11b11c9a353858ce3ca82c698dbceea7c
ms.sourcegitcommit: 817716c2e96f24af0ef1d7d5323afdeccdc602f3
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/13/2021
ms.locfileid: "6028553"
---
# <a name="year-end-close-missing-opening-balances"></a><span data-ttu-id="5a4ba-103">Chybějící počáteční zůstatky roční uzávěrky</span><span class="sxs-lookup"><span data-stu-id="5a4ba-103">Year-end close missing opening balances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5a4ba-104">Toto téma vysvětluje, proč mohou při uzavírání roku chybět počáteční zůstatky a jak tyto zůstatky znovu vytvořit, pokud chybí.</span><span class="sxs-lookup"><span data-stu-id="5a4ba-104">This topic explains why opening balances might be missing when you close a year, and how to rebuild those balances if they are missing.</span></span>

### <a name="symptom"></a><span data-ttu-id="5a4ba-105">Příznak</span><span class="sxs-lookup"><span data-stu-id="5a4ba-105">Symptom</span></span>

<span data-ttu-id="5a4ba-106">Proč po spuštění roční závěrky hlavní knihy nejsou žádné počáteční zůstatky?</span><span class="sxs-lookup"><span data-stu-id="5a4ba-106">Why are there no beginning balances after running the General ledger year-end close?</span></span> 

### <a name="resolution"></a><span data-ttu-id="5a4ba-107">Řešení</span><span class="sxs-lookup"><span data-stu-id="5a4ba-107">Resolution</span></span>

<span data-ttu-id="5a4ba-108">Zde je třeba zkontrolovat, zda jste provedli roční uzávěrku v hlavní knize a poté vygenerovali předvahu, která nezobrazuje počáteční zůstatky pro příští fiskální rok.</span><span class="sxs-lookup"><span data-stu-id="5a4ba-108">Here are things to check if you've closed a year in General ledger, and then generated a trial balance that doesn't display opening balances for the next fiscal year.</span></span>

<span data-ttu-id="5a4ba-109">Pokud je pole **Vrátit zpět předchozí uzávěrku** nastaveno na **Ano**, dojde ke stornování předchozí roční uzávěrky pro stejný fiskální rok.</span><span class="sxs-lookup"><span data-stu-id="5a4ba-109">If the **Undo previous close** field is set to **Yes**, the previous year-end close for the same fiscal year is being reversed.</span></span> <span data-ttu-id="5a4ba-110">Při spuštění procesu stornování roční uzávěrky se odstraní všechny záznamy pro konečné a počáteční zůstatky, jako kdyby roční uzávěrka nikdy neproběhla.</span><span class="sxs-lookup"><span data-stu-id="5a4ba-110">When running a process to reverse the year-end close, all entries for both closing and opening balances will be deleted, as if the year had never been closed.</span></span> <span data-ttu-id="5a4ba-111">Odstraní se i doklady.</span><span class="sxs-lookup"><span data-stu-id="5a4ba-111">The vouchers are also deleted.</span></span> <span data-ttu-id="5a4ba-112">Proces roční uzávěrky se znovu automaticky nespustí.</span><span class="sxs-lookup"><span data-stu-id="5a4ba-112">The year-end close process will not run again automatically.</span></span> <span data-ttu-id="5a4ba-113">Celý proces je třeba spustit znovu, ale tentokrát s aktualizovaným nastavením **Vrátit zpět předchozí uzávěrku** na **Ne**.</span><span class="sxs-lookup"><span data-stu-id="5a4ba-113">You must start the process again, this time updating the **Undo previous close** option to **No**.</span></span>

<span data-ttu-id="5a4ba-114">Tomuto scénáři se věnují časté dotazy na téma roční uzávěrky.</span><span class="sxs-lookup"><span data-stu-id="5a4ba-114">This scenario is covered in the year-end close FAQ topic.</span></span> <span data-ttu-id="5a4ba-115">Další informace viz [Časté dotazy k aktivitám na konci roku](faq-year-end-activities.md).</span><span class="sxs-lookup"><span data-stu-id="5a4ba-115">For more information, see [Year-end activities FAQ](faq-year-end-activities.md).</span></span>

### <a name="symptom"></a><span data-ttu-id="5a4ba-116">Příznak</span><span class="sxs-lookup"><span data-stu-id="5a4ba-116">Symptom</span></span>

<span data-ttu-id="5a4ba-117">Koncem roku byla spuštěna roční uzávěrka s možností **Vrátit zpět předchozí uzávěrku** nastavenou na **Ne**, ale počáteční zůstatky za fiskální rok stále nejsou.</span><span class="sxs-lookup"><span data-stu-id="5a4ba-117">I ran year-end close with the **Undo previous close** option set to **No**, and I still do not have opening balances for my fiscal year.</span></span>

### <a name="resolution"></a><span data-ttu-id="5a4ba-118">Řešení</span><span class="sxs-lookup"><span data-stu-id="5a4ba-118">Resolution</span></span>

<span data-ttu-id="5a4ba-119">Nejprve zkontrolujte stav dávkové úlohy.</span><span class="sxs-lookup"><span data-stu-id="5a4ba-119">First check the status of the batch job.</span></span> <span data-ttu-id="5a4ba-120">Uzavření roku zahrnuje řadu samostatných úloh, ale nejdůležitějším krokem je dávková úloha s popisem úlohy **Krok 5.0.0**.</span><span class="sxs-lookup"><span data-stu-id="5a4ba-120">Closing a year includes a number of separate tasks, but the most critical step is the batch task with the task description **Step 5.0.0**.</span></span> <span data-ttu-id="5a4ba-121">Zaúčtování počátečních transakcí a volitelně uzávěrkových transakcí do hlavní knihy probíhá během tohoto kroku.</span><span class="sxs-lookup"><span data-stu-id="5a4ba-121">Posting the opening transactions, and optionally the closing transactions, to General ledger takes place during this step.</span></span> 

<span data-ttu-id="5a4ba-122">[![Seznam historie dávek](./media/yec-mssng-open-blnces-01.png)](./media/yec-mssng-open-blnces-01.png)</span><span class="sxs-lookup"><span data-stu-id="5a4ba-122">[![Batch history list](./media/yec-mssng-open-blnces-01.png)](./media/yec-mssng-open-blnces-01.png)</span></span>

<span data-ttu-id="5a4ba-123">Pokud tento krok skončil úspěšně, ale na stránce **Dotaz na předvahu** (**Hlavní kniha > Dotazy a sestavy > Předvaha**) nevidíte počáteční zůstatky, zkontrolujte výsledky dávkové úlohy roční uzávěrky a zjistěte, zda byl krok Znovu sestavit zůstatky úspěšně dokončen.</span><span class="sxs-lookup"><span data-stu-id="5a4ba-123">If this step ended successfully but you don’t see opening balances on the **Trial balance inquiry** page (**General ledger > Inquires and reports > Trial balance**), review the results of the year-end close batch job to see if the Rebuild balances step completed successfully.</span></span>

<span data-ttu-id="5a4ba-124">[![Výsledky dávkové úlohy roční uzávěrky](./media/yec-mssng-open-blnces-02.png)](./media/yec-mssng-open-blnces-02.png)</span><span class="sxs-lookup"><span data-stu-id="5a4ba-124">[![Results of year-end close batch job](./media/yec-mssng-open-blnces-02.png)](./media/yec-mssng-open-blnces-02.png)</span></span>

<span data-ttu-id="5a4ba-125">Pokud se tento krok z nějakého důvodu nepovedl, počáteční (a volitelně uzávěrkové) transakce byly pravděpodobně úspěšně zaúčtovány.</span><span class="sxs-lookup"><span data-stu-id="5a4ba-125">If this step has failed for any reason, the opening (and optionally closing) transactions were likely posted successfully.</span></span> <span data-ttu-id="5a4ba-126">Můžete ověřit, že transakce hlavní knihy byly úspěšně zaúčtovány, a to pomocí stránky **Dotaz na transakce dokladu** zadáním čísla a data dokladu poskytnutého v dialogu roční uzávěrky pro rok, který jste uzavřeli (**Hlavní kniha > Dotazy a sestavy > Transakce dokladu**).</span><span class="sxs-lookup"><span data-stu-id="5a4ba-126">You can verify that the General ledger transactions were posted successfully using the **Voucher transactions inquiry** page by specifying the voucher number and date provided on the year-end close dialog for the year that you closed, (**General Ledger > Inquiries and reports > Voucher transactions**).</span></span>

<span data-ttu-id="5a4ba-127">[![Dotaz na transakce dokladu](./media/yec-mssng-open-blnces-03.png)](./media/yec-mssng-open-blnces-03.png)</span><span class="sxs-lookup"><span data-stu-id="5a4ba-127">[![Voucher transactions inquiry](./media/yec-mssng-open-blnces-03.png)](./media/yec-mssng-open-blnces-03.png)</span></span>

<span data-ttu-id="5a4ba-128">Pokud jsou k dispozici počáteční (a volitelně uzávěrkové) doklady, nemusíte roční uzávěrku spouštět znovu.</span><span class="sxs-lookup"><span data-stu-id="5a4ba-128">If the opening (and optionally closing) vouchers are present, you don’t need to run the year-end close again.</span></span> <span data-ttu-id="5a4ba-129">Místo toho v další části vyhledejte informace o tom, jak postupovat dále.</span><span class="sxs-lookup"><span data-stu-id="5a4ba-129">Instead refer to the next section for information about how to move forward.</span></span>

### <a name="symptom"></a><span data-ttu-id="5a4ba-130">Příznak</span><span class="sxs-lookup"><span data-stu-id="5a4ba-130">Symptom</span></span>

<span data-ttu-id="5a4ba-131">Krok „Znovu sestavit zůstatky“ v roční uzávěrce se nepovedl, musím spustit celý proces roční uzávěrky znovu?</span><span class="sxs-lookup"><span data-stu-id="5a4ba-131">The “Rebuild balances” step in the year-end close failed, do I need to re-run the entire year-end close process?</span></span>

### <a name="resolution"></a><span data-ttu-id="5a4ba-132">Řešení</span><span class="sxs-lookup"><span data-stu-id="5a4ba-132">Resolution</span></span>

<span data-ttu-id="5a4ba-133">Krok Znovu sestavit zůstatky aktualizuje zůstatky hlavní knihy, které se používají při generování dotazu na předvahu.</span><span class="sxs-lookup"><span data-stu-id="5a4ba-133">The Rebuild balances step updates the General ledger balances that are used when the Trial balance inquiry is generated.</span></span>  <span data-ttu-id="5a4ba-134">Jde o poslední krok v procesu roční uzávěrky.</span><span class="sxs-lookup"><span data-stu-id="5a4ba-134">It is the final step in the year-end close process.</span></span>  <span data-ttu-id="5a4ba-135">Pokud je tento krok jediným krokem, který se nepovedl, transakce hlavní knihy byly úspěšně zaúčtovány.</span><span class="sxs-lookup"><span data-stu-id="5a4ba-135">If this step is the only step that failed, the General ledger transactions have posted successfully.</span></span>  <span data-ttu-id="5a4ba-136">Roční uzávěrku nemusíte znovu spouštět.</span><span class="sxs-lookup"><span data-stu-id="5a4ba-136">You do not need to run the year-end close again.</span></span> <span data-ttu-id="5a4ba-137">Proces můžete spustit, abyste ručně znovu sestavili zůstatky, a to pomocí stránky **Sady finanční dimenze** (**Hlavní kniha > Účtová osnova > Dimenze > Sady finančních dimenzí**).</span><span class="sxs-lookup"><span data-stu-id="5a4ba-137">You can run the process to rebuild the balances manually using the **Financial dimension sets** page (**General ledger > Chart of accounts > Dimensions > Financial dimension sets**).</span></span>

<span data-ttu-id="5a4ba-138">[![Tlačítko Znovu sestavit zůstatky na stránce Sady finančních dimenzí](./media/yec-mssng-open-blnces-04.png)](./media/yec-mssng-open-blnces-04.png)</span><span class="sxs-lookup"><span data-stu-id="5a4ba-138">[![Rebuild balances button on Financial dimension sets page](./media/yec-mssng-open-blnces-04.png)](./media/yec-mssng-open-blnces-04.png)</span></span>

<span data-ttu-id="5a4ba-139">Pokud zpracování tohoto kroku trvá dlouho, doporučujeme zkontrolovat doporučené postupy pro sady finančních dimenzí, jak je popsáno v části [Osvědčené postupy pro aktualizaci sad finančních dimenzí](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/best-practices-for-updating-financial-dimension-set-dimension-sets).</span><span class="sxs-lookup"><span data-stu-id="5a4ba-139">If this step takes a long time to process, we recommend reviewing the best practices for financial dimension sets as described in [Best practices for updating Financial dimension sets](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/best-practices-for-updating-financial-dimension-set-dimension-sets).</span></span> 

