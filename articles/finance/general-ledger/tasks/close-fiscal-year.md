---
title: Uzavření fiskálního roku
description: Tato procedura vás provede procesem roční uzávěrky, která zůstatky převádí do nového fiskálního roku.
author: aprilolson
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters, LedgerFiscalCloseGroup, LedgerFiscalCloseAddLedger, SysLookupMultiSelectGrid, LedgerFiscalCloseRunGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 593ab5b45cc0c2e1a8b876aa89de014fd9df1a13
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3137939"
---
# <a name="close-the-fiscal-year"></a><span data-ttu-id="0a4ea-103">Uzavření fiskálního roku</span><span class="sxs-lookup"><span data-stu-id="0a4ea-103">Close the fiscal year</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0a4ea-104">Tato procedura vás provede procesem roční uzávěrky, která zůstatky převádí do nového fiskálního roku.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-104">This procedure steps through the year end close process that transfers balances to a new fiscal year.</span></span>


## <a name="validate-year-end-close-parameters"></a><span data-ttu-id="0a4ea-105">Ověření parametrů roční uzávěrky</span><span class="sxs-lookup"><span data-stu-id="0a4ea-105">Validate year-end close parameters</span></span>
1. <span data-ttu-id="0a4ea-106">Přejděte na **Navigační podokno > Moduly > Hlavní kniha > Nastavení hlavní knihy > Parametry hlavní knihy**.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-106">Go to **Navigation pane > Modules > General ledger > Ledger setup > General ledger parameters**.</span></span>
2. <span data-ttu-id="0a4ea-107">Rozbalte oddíl **Uzávěrka fiskálního roku**.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-107">Expand the **Fiscal year close** section.</span></span>
3. <span data-ttu-id="0a4ea-108">Vyberte Ano nebo ne pro možnost **Odstranit transakce roční uzávěrky během převodu**.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-108">Select 'Yes' or 'No' for the **Delete close-of-year transactions during transfer** option.</span></span>
    
    <span data-ttu-id="0a4ea-109">Pokud již byl uzavřen fiskální rok a znovu spuštěna roční uzávěrka, je toto nastavení důležité.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-109">If the fiscal year has already been closed and the year-end close is being run again, this setting is important.</span></span> <span data-ttu-id="0a4ea-110">Pokud je nastavená na hodnotu Ano, bude odstraněn doklad pro předchozího roční uzávěrku a bude vytvořen nový doklad pro všechny počáteční zůstatky účtů.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-110">If set to Yes, the voucher for the previous year-end close will be deleted, and a new voucher will be created for all accounts beginning balances.</span></span> <span data-ttu-id="0a4ea-111">Pokud je nastavena na hodnotu Ne, předchozí doklad zůstane a nový doklad bude vytvořen pouze pro opravné položky, které byly zaúčtovány po poslední roční uzávěrce.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-111">If set to No, the previous voucher will remain and a new voucher will only be created for adjusting entries that were posted after the last year-end close.</span></span>

4. <span data-ttu-id="0a4ea-112">Vyberte Ano nebo Ne jako odpověď na dotaz, zda **vytvořit transakce uzávěrky během převodu**.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-112">Select 'Yes' or 'No' for the **Create closing transactions during transfer** option.</span></span>

    <span data-ttu-id="0a4ea-113">Pokud je nastavena na hodnotu Ano, budou vytvořeny dvě transakce.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-113">If set to Yes, two transactions are created.</span></span> <span data-ttu-id="0a4ea-114">Jeden doklad byl vytvořen v uzavíraném fiskálním roce, aby byly vynulovány zůstatky účtů hlavní knihy zisků a ztrát a druhý je vytvořen v dalším fiskálním roce pro počáteční zůstatky.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-114">One voucher is created in the fiscal year being closed to bring the balances of the P&L ledger accounts down to zero and a second voucher is created in the next fiscal year for the beginning balances.</span></span> <span data-ttu-id="0a4ea-115">Pokud je nastavena hodnota Ne, jediný doklad je vytvořen pro počáteční zůstatky dalšího fiskálního roku.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-115">If set to No, a single voucher is created in the next fiscal year for the beginning balances.</span></span>  

5. <span data-ttu-id="0a4ea-116">Vyberte Ano nebo Ne jako odpověď na dotaz, zda **nastavit stav fiskálního roku na trvale uzavřený**.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-116">Select 'Yes' or 'No' for the **Set fiscal year status to permanently closed** option.</span></span>

    <span data-ttu-id="0a4ea-117">Pokud je nastaveno na hodnotu Ano, stav fiskálního roku bude nastaven na Trvale uzavřeno.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-117">If set to Yes, the fiscal year status will be set to Permanently closed.</span></span>  <span data-ttu-id="0a4ea-118">Vzhledem k tomu, že trvale uzavřený rok nelze znovu otevřít, je nejvhodnější nastavit tuto možnost na hodnotu Ne.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-118">Because a permanently closed year cannot be reopened, it would be a best practice to set this option to No.</span></span>  

6. <span data-ttu-id="0a4ea-119">Vyberte Ano nebo ne pro zda **číslo dokladu musí být vyplněno během konce roku zavřete**.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-119">Select 'Yes' or 'No' for the **Voucher number must be filled in during the year end close** option.</span></span>

    <span data-ttu-id="0a4ea-120">Pokud bude nastavena na hodnotu Ano, číslo dokladu musí být zadáno ručně během procesu roční uzávěrky.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-120">If set to Yes, a voucher number must be manually entered during the year end close process.</span></span> <span data-ttu-id="0a4ea-121">Číselná řada není použita k vygenerování tohoto čísla dokladu.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-121">A number sequence is not used to generate this voucher number.</span></span> <span data-ttu-id="0a4ea-122">Je doporučeno nastavit ji na hodnotu Ano.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-122">It's a best practice to set this to Yes.</span></span>  

7. <span data-ttu-id="0a4ea-123">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-123">Close the page.</span></span>
8. <span data-ttu-id="0a4ea-124">Přejděte na **Hlavní kniha > Uzávěrka období > Roční uzávěrka**.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-124">Go to **General ledger > Period close > Year end close**.</span></span>
9. <span data-ttu-id="0a4ea-125">Kliknutím na tlačítko **Nový** vytvořte šablonu roční uzávěrky.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-125">Click **New** to create a year-end close template.</span></span>

    <span data-ttu-id="0a4ea-126">Šablonu lze vytvořit skupinu právnických osob, pro které se má spustit roční uzávěrka.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-126">A template can be created for a group of legal entities for which to run the year-end close.</span></span> <span data-ttu-id="0a4ea-127">Tuto šablonu můžete znovu používat každý rok.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-127">This template can be reused year after year.</span></span>  

10. <span data-ttu-id="0a4ea-128">Do pole **Název skupiny** zadejte název šablony roční uzávěrky.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-128">In the **Group name** field, enter a year-end close template name..</span></span>
11. <span data-ttu-id="0a4ea-129">V poli **Fiskální kalendář** vyberte fiskální rok, pro který bude šablona vytvořena.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-129">In the **Fiscal calendar** field, select the fiscal year for which the template will be created.</span></span>

    <span data-ttu-id="0a4ea-130">Pouze právnické osoby, které používají stejný fiskální rok, mohou být seskupeny do šablony roční uzávěrky.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-130">Only legal entities which use the same fiscal year can be grouped together in the year-end close template.</span></span> <span data-ttu-id="0a4ea-131">Důvodem je, že roční uzávěrka se provádí výběrem fiskálního roku, nikoli data.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-131">This is because the year end close is done by selecting a fiscal year, not a date.</span></span>  

12. <span data-ttu-id="0a4ea-132">V **podokně akcí** klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-132">On the **Action pane**, click **Save**.</span></span>
13. <span data-ttu-id="0a4ea-133">V části **právnické osoby** klikněte na tlačítko **přidat** a vyberte právnické osoby pro tuto šablonu.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-133">In the **Legal entities** section, click **Add** to select the legal entities for this template.</span></span>
    
    <span data-ttu-id="0a4ea-134">Právnické osoby lze přidat výběrem právnické osoby nebo výběrem organizační hierarchie.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-134">Legal entities can be added by either selecting the legal entities or by selecting an organizational hierarchy.</span></span>  <span data-ttu-id="0a4ea-135">Budou přidány pouze právnické osoby s organizační hierarchií se stejným vybraným fiskálním kalendářem.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-135">Only legal entities with the organizational hierarchy with the same fiscal calendar selected will be added.</span></span>  

14. <span data-ttu-id="0a4ea-136">Vyberte právnické osoby nebo organizační hierarchii.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-136">Select either the legal entities or the organizational hierarchy.</span></span>
15. <span data-ttu-id="0a4ea-137">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-137">Click **OK**.</span></span>
16. <span data-ttu-id="0a4ea-138">Vyberte Ano nebo ne v **dimenzi Rozvaha převodu**.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-138">Select 'Yes' or 'No' in the **Transfer balance sheet dimension**.</span></span>

    <span data-ttu-id="0a4ea-139">Je nejvhodnější nastavit tuto možnost na hodnotu Ano pro rozvahové účty.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-139">It's best practice to set this option to Yes for Balance sheet accounts.</span></span> <span data-ttu-id="0a4ea-140">To bude udržovat finanční dimenze v zaúčtovaných transakcích při vytváření počátečních zůstatků rozvahových účtů.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-140">This will maintain the financial dimensions on posted transactions when creating the beginning balances for the balance sheet accounts.</span></span> <span data-ttu-id="0a4ea-141">Pro účty zisků a ztrát můžete vybrat možnost zachování finančních dimenzí (Zavřít všechny), když jsou zůstatky přesunuty do Zachovaných zisků, nebo můžete vybrat nahrazení finančních dimenzí hodnotou jiné dimenze (Zavřít jednu).</span><span class="sxs-lookup"><span data-stu-id="0a4ea-141">For profit and loss accounts, you can select to maintain the financial dimensions (Close all) when the balances are moved to Retained earnings or you can select to have the financial dimensions replaced with a different dimension value (Close single).</span></span> <span data-ttu-id="0a4ea-142">Pokud zvolíte Zavřít jednu, můžete definovat konkrétní hodnotu dimenze pro každou dimenzi nebo toto pole nechat prázdné.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-142">If you choose Close single, you can define a specific dimension value for each dimension or even choose to leave it blank.</span></span>  

17. <span data-ttu-id="0a4ea-143">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-143">Click **Save**.</span></span>
18. <span data-ttu-id="0a4ea-144">Spusťte roční uzávěrku výběrem příkazu **Spustit fiskální uzávěrku** v **podokně akcí**.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-144">Start the year-end close by choosing **Run fiscal close** on the **Action Pane**.</span></span> <span data-ttu-id="0a4ea-145">Pro vybranou šablonu se spustí roční uzávěrka.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-145">The year-end close will be run for the selected template.</span></span>  
19. <span data-ttu-id="0a4ea-146">Vyberte všechny právnické osoby nebo jejich podmnožinu ze šablony, pro kterou chcete roční uzávěrku spustit.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-146">Select all or a subset of legal entities from the template for which to run the year-end close.</span></span>

    <span data-ttu-id="0a4ea-147">Při prvním spuštění konci roku zavřít, chcete-li získat počáteční zůstatek, které většina organizací mohou zvolit spuštění Uzávěrka pro všechny právnické osoby v rámci šablony.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-147">When first running the year-end close, to get beginning balance,s most organizations may choose to run the year-end close for all legal entities within the template.</span></span> <span data-ttu-id="0a4ea-148">Pokud jsou potom provedeny úpravy položky, můžete spustit roční uzávěrku pouze pro právnické osoby, které mají úpravy.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-148">If adjusting entries are made after that, you may choose to run the year-end close for only the legal entities that have adjustments.</span></span>  

20. <span data-ttu-id="0a4ea-149">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-149">Click **OK**.</span></span>
21. <span data-ttu-id="0a4ea-150">Vyberte fiskální rok, pro který chcete spustit roční uzávěrku.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-150">Select the fiscal year for which to run the year-end close.</span></span>
22. <span data-ttu-id="0a4ea-151">Zadejte hodnotu do pole **Typ dokladu**.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-151">In the **Voucher field**, type a value.</span></span> <span data-ttu-id="0a4ea-152">Platí pravidlo doporučeného postupu zahrnout do čísla dokladu fiskální rok k usnadnění vyhledání dokladu roční uzávěrky, který je vytvořen.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-152">It's best practice to include the fiscal year in the voucher number, to make it easier to find the year-end close voucher that is created.</span></span>  
23. <span data-ttu-id="0a4ea-153">Roční uzávěrka se nastaví na výchozí dávková spouštění.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-153">The year-end close defaults to run in batch.</span></span> <span data-ttu-id="0a4ea-154">Pro dlouhodobé procesy platí pravidlo doporučeného postupu spouštět je v dávkovém režimu.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-154">It's best practice for long-running processes to run in batch mode.</span></span> <span data-ttu-id="0a4ea-155">To je obvykle jeden z těchto procesů, což je důvod pro použití v dávkovém režimu ve výchozím nastavení.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-155">This is typically one of those processes, which is why the default is to use batch mode.</span></span>  
24. <span data-ttu-id="0a4ea-156">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="0a4ea-156">Click **OK**.</span></span>

