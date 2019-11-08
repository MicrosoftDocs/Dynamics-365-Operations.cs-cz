---
title: Elektronické výkaznictví – Používání finančních dimenzí jako zdroje dat (část 2 - mapování modelu)
description: Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) použití finančních dimenzí jako zdroje dat pro sestavy elektronického výkaznictví.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 788564bfd7c3df146266976d8eef6621ff37ca2a
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550618"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-2---model-mapping"></a><span data-ttu-id="f5b4a-103">Elektronické výkaznictví – Používání finančních dimenzí jako zdroje dat (část 2 - mapování modelu)</span><span class="sxs-lookup"><span data-stu-id="f5b4a-103">ER Use financial dimensions as a data source (Part 2 - Model mapping)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f5b4a-104">Následující postup popisuje, jak uživatel s rolí správce systému nebo vývojář elektronického výkaznictví může nakonfigurovat datový model Elektronické výkaznictví (ER) použití finančních dimenzí jako zdroje dat pro sestavy elektronického výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="f5b4a-105">Tyto kroky lze provést v rámci libovolné společnosti.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="f5b4a-106">K dokončení těchto kroků je nutné nejprve provést kroky v proceduře "Elektronické výkaznictví – Použití finančních dimenzí jako zdroje dat (část 1: návrh datového modelu").</span><span class="sxs-lookup"><span data-stu-id="f5b4a-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 1: Design data model” procedure.</span></span>


## <a name="add-required-data-sources-to-model-mapping"></a><span data-ttu-id="f5b4a-107">Přidání požadovaných zdrojů dat k mapování modelu</span><span class="sxs-lookup"><span data-stu-id="f5b4a-107">Add required data sources to model mapping</span></span>
1. <span data-ttu-id="f5b4a-108">Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="f5b4a-109">Ve stromovém zobrazení vyberte Vzorový model finančních dimenzí.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="f5b4a-110">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-110">Click Designer.</span></span>
4. <span data-ttu-id="f5b4a-111">Klikněte na možnost Mapovat model na datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-111">Click Map model to datasource.</span></span>
5. <span data-ttu-id="f5b4a-112">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-112">Click New.</span></span>
6. <span data-ttu-id="f5b4a-113">V poli Definice vyberte Položka.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-113">In the Definition field, select Entry.</span></span>
7. <span data-ttu-id="f5b4a-114">Do pole Název zadejte Mapování dat dimenzí.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-114">In the Name field, type 'Dimensions data mapping'.</span></span>
8. <span data-ttu-id="f5b4a-115">Do pole Popis zadejte Mapování dat dimenzí.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-115">In the Description field, type 'Dimensions data mapping'.</span></span>
9. <span data-ttu-id="f5b4a-116">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-116">Click Save.</span></span>
10. <span data-ttu-id="f5b4a-117">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-117">Click Designer.</span></span>
11. <span data-ttu-id="f5b4a-118">Ve stromovém zobrazení vyberte možnost 'Dynamics 365 for Operations\Tabulka'.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-118">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
12. <span data-ttu-id="f5b4a-119">Klikněte na možnost Přidat kořen.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-119">Click Add root.</span></span>
13. <span data-ttu-id="f5b4a-120">Do pole Název zadejte text „Společnost“.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-120">In the Name field, type 'Company'.</span></span>
14. <span data-ttu-id="f5b4a-121">Do pole Tabulka zadejte hodnotu „CompanyInfo“.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-121">In the Table field, type 'CompanyInfo'.</span></span>
15. <span data-ttu-id="f5b4a-122">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-122">Click OK.</span></span>
16. <span data-ttu-id="f5b4a-123">Ve stromovém zobrazení vyberte Funkce\Podrobnosti o finančních dimenzích.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-123">In the tree, select 'Functions\Financial dimensions details'.</span></span>
17. <span data-ttu-id="f5b4a-124">Klikněte na možnost Přidat kořen.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-124">Click Add root.</span></span>
    * <span data-ttu-id="f5b4a-125">Tento zdroj dat určuje, jak bude definován obor finančních dimenzí pro jakoukoli sestavu, která bude používat tento model jako zdroj dat.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-125">This data source specifies how the scope of financial dimensions will be defined for any report that will use this model as a data source.</span></span>  
18. <span data-ttu-id="f5b4a-126">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-126">In the Name field, type a value.</span></span>
19. <span data-ttu-id="f5b4a-127">Vyberte možnost Ano v poli Zeptat se na dimenze.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-127">Select Yes in the Ask for dimensions field.</span></span>
    * <span data-ttu-id="f5b4a-128">Vyberte možnost Ano, chcete-li povolit uživateli výběr dimenzí v operačním času ve formuláři Uživatelské dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-128">Select Yes to allow the user to select dimensions at run-time on the User dialog form.</span></span> <span data-ttu-id="f5b4a-129">Pokud je nastavena na hodnotu Ne, všechny finanční dimenze aktuální instance budou použity ve výchozím nastavení.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-129">If set to No, all financial dimensions of the current instance will be used by default.</span></span>  
20. <span data-ttu-id="f5b4a-130">V poli Finanční dimenze vyberte "Právnická osoba".</span><span class="sxs-lookup"><span data-stu-id="f5b4a-130">In the Financial dimensions selection field, select 'Legal entity'.</span></span>
    * <span data-ttu-id="f5b4a-131">Vyberte Vše, chcete-li povolit uživateli výběr požadovaných dimenzí pro aktuální instanci ve vyhledávacím poli.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-131">Select All to allow the user to select desire dimensions for the current  instance in the Lookup field.</span></span>  <span data-ttu-id="f5b4a-132">Vyberte Právnická osoba, chcete-li povolit uživateli výběr dimenzí pro společnost ve vyhledávacím poli.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-132">Select Legal entity to allow the user to select dimensions for the company in the Lookup field.</span></span>  <span data-ttu-id="f5b4a-133">Vyberte dimenzi, abyste uživateli povolili výběr dimenzí pomocí jedné sady dimenzí.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-133">Select Dimension to allow the user to select dimensions using a single dimension set.</span></span>  
21. <span data-ttu-id="f5b4a-134">Vyberte možnost Ano v poli Zeptat se na hlavní účet.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-134">Select Yes in the Ask for main account field.</span></span>
    * <span data-ttu-id="f5b4a-135">Nastavte v poli Zeptat se na hlavní účet hodnotu Ano, chcete-li umožnit uživatelům vybrat hlavní účet jako součást seznamu dimenzí.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-135">Set ‘Ask for main account’ to Yes to allow users to select the main account as part of the list of dimensions.</span></span>   <span data-ttu-id="f5b4a-136">Je-li nastavena na hodnotu Ne, hlavní účet nebude zahrnut do seznamu dimenzí a je povolena možnost "Je hlavní účet povinný".</span><span class="sxs-lookup"><span data-stu-id="f5b4a-136">If set to No, the main account will not be included to the list of dimensions and the ‘Is main account mandatory’ option is enabled.</span></span> <span data-ttu-id="f5b4a-137">Pokud je možnost Je hlavní účet povinný nastavena na hodnotu Ano, zahrňte hlavní účet do seznamu dimenzí nezávisle na výběru uživatele.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-137">If “Is main account mandatory’ is set to Yes, include the main account in the list of dimensions regardless of the user’s selection.</span></span>  
22. <span data-ttu-id="f5b4a-138">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-138">Click OK.</span></span>
23. <span data-ttu-id="f5b4a-139">Ve stromovém zobrazení vyberte možnost 'Dynamics 365 for Operations\Záznamy v tabulce'.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-139">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
24. <span data-ttu-id="f5b4a-140">Klikněte na možnost Přidat kořen.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-140">Click Add root.</span></span>
25. <span data-ttu-id="f5b4a-141">Do pole Název zadejte 'LedgerJournal'.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-141">In the Name field, type 'LedgerJournal'.</span></span>
26. <span data-ttu-id="f5b4a-142">Vyberte možnost Ano v poli Zeptat se na dotaz.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-142">Select Yes in the Ask for query field.</span></span>
27. <span data-ttu-id="f5b4a-143">Do pole Tabulka zadejte hodnotu 'LedgerJournalTable'.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-143">In the Table field, type 'LedgerJournalTable'.</span></span>
28. <span data-ttu-id="f5b4a-144">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-144">Click OK.</span></span>

## <a name="map-data-model-elements-to-added-data-sources"></a><span data-ttu-id="f5b4a-145">Namapování prvků datového modelu na přidané zdroje dat</span><span class="sxs-lookup"><span data-stu-id="f5b4a-145">Map data model elements to added data sources</span></span>
1. <span data-ttu-id="f5b4a-146">Ve stromovém zobrazení rozbalte 'Deník'.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-146">In the tree, expand 'Journal'.</span></span>
2. <span data-ttu-id="f5b4a-147">Ve stromovém zobrazení rozbalte 'Deník\Transakce'.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-147">In the tree, expand 'Journal\Transaction'.</span></span>
3. <span data-ttu-id="f5b4a-148">Ve stromovém zobrazení rozbalte 'Deník\Transakce\Data dimenzí'.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-148">In the tree, expand 'Journal\Transaction\Dimensions data'.</span></span>
4. <span data-ttu-id="f5b4a-149">Ve stromovém zobrazení rozbalte 'Nastavení dimenzí'.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-149">In the tree, expand 'Dimensions setting'.</span></span>
5. <span data-ttu-id="f5b4a-150">Ve stromovém zobrazení rozbalte 'LedgerJournal'.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-150">In the tree, expand 'LedgerJournal'.</span></span>
6. <span data-ttu-id="f5b4a-151">Ve stromovém zobrazení rozbalteLedgerJournal\<Relation.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-151">In the tree, expand 'LedgerJournal\<Relations'.</span></span>
7. <span data-ttu-id="f5b4a-152">Ve stromovém zobrazení rozbalte LedgerJournal\<Vztahy\LedgerJournalTrans.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-152">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
8. <span data-ttu-id="f5b4a-153">Ve stromovém zobrazení vyberte LedgerJourna\\<Relations\LedgerJournalTrans\Voucher.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-153">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Voucher'.</span></span>
9. <span data-ttu-id="f5b4a-154">Ve stromovém zobrazení vyberte možnost 'Deník\Transakce\Doklad'.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-154">In the tree, select 'Journal\Transaction\Voucher'.</span></span>
10. <span data-ttu-id="f5b4a-155">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-155">Click Bind.</span></span>
11. <span data-ttu-id="f5b4a-156">Ve stromovém zobrazení vyberte 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension).</span><span class="sxs-lookup"><span data-stu-id="f5b4a-156">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
    * <span data-ttu-id="f5b4a-157">Všimněte si, že pro jakýkoli odkaz na finanční dimenze, na které je nastaven, jako je například LedgerDimension, je k dispozici odpovídající položka zdroje dat (LedgerDimension.Dimension).</span><span class="sxs-lookup"><span data-stu-id="f5b4a-157">Note that for any reference to financial dimensions that is set to, for instance, LedgerDimension, a corresponding data source item is available (LedgerDimension.Dimension).</span></span> <span data-ttu-id="f5b4a-158">Tato položka zdroje dat nabízí finanční dimenze této sady dimenzí jako seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-158">This data source item offers the financial dimensions of that dimensions set as the record’s list.</span></span>  
12. <span data-ttu-id="f5b4a-159">Ve stromovém zobrazení rozbalte LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension).</span><span class="sxs-lookup"><span data-stu-id="f5b4a-159">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
13. <span data-ttu-id="f5b4a-160">Ve stromovém zobrazení rozbalte LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-160">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
14. <span data-ttu-id="f5b4a-161">Ve stromovém zobrazení rozbalte LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-161">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value'.</span></span>
15. <span data-ttu-id="f5b4a-162">Ve stromovém zobrazení rozbalte LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-162">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition'.</span></span>
16. <span data-ttu-id="f5b4a-163">Ve stromovém zobrazení vyberte LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-163">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name'.</span></span>
17. <span data-ttu-id="f5b4a-164">Ve stromové struktuře vyberte 'Deník\Transakce\Data dimenzí\Název'.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-164">In the tree, select 'Journal\Transaction\Dimensions data\Name'.</span></span>
18. <span data-ttu-id="f5b4a-165">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-165">Click Bind.</span></span>
19. <span data-ttu-id="f5b4a-166">Ve stromovém zobrazení vyberte LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-166">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description'.</span></span>
20. <span data-ttu-id="f5b4a-167">Ve stromové struktuře vyberte 'Deník\Transakce\Data dimenzí\Popis'.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-167">In the tree, select 'Journal\Transaction\Dimensions data\Description'.</span></span>
21. <span data-ttu-id="f5b4a-168">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-168">Click Bind.</span></span>
22. <span data-ttu-id="f5b4a-169">Ve stromovém zobrazení vyberte LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-169">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code'.</span></span>
23. <span data-ttu-id="f5b4a-170">Ve stromové struktuře vyberte 'Deník\Transakce\Data dimenzí\Kód'.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-170">In the tree, select 'Journal\Transaction\Dimensions data\Code'.</span></span>
24. <span data-ttu-id="f5b4a-171">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-171">Click Bind.</span></span>
25. <span data-ttu-id="f5b4a-172">Ve stromovém zobrazení vyberte LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-172">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
26. <span data-ttu-id="f5b4a-173">Ve stromové struktuře vyberte 'Deník\Transakce\Data dimenzí'.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-173">In the tree, select 'Journal\Transaction\Dimensions data'.</span></span>
27. <span data-ttu-id="f5b4a-174">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-174">Click Bind.</span></span>
28. <span data-ttu-id="f5b4a-175">Ve stromovém zobrazení vyberte LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit).</span><span class="sxs-lookup"><span data-stu-id="f5b4a-175">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)'.</span></span>
29. <span data-ttu-id="f5b4a-176">Ve stromovém zobrazení vyberte možnost 'Deník\Transakce\Má dáti'.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-176">In the tree, select 'Journal\Transaction\Debit'.</span></span>
30. <span data-ttu-id="f5b4a-177">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-177">Click Bind.</span></span>
31. <span data-ttu-id="f5b4a-178">Ve stromovém zobrazení vyberte LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate).</span><span class="sxs-lookup"><span data-stu-id="f5b4a-178">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)'.</span></span>
32. <span data-ttu-id="f5b4a-179">Ve stromovém zobrazení vyberte možnost 'Deník\Transakce\Datum'.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-179">In the tree, select 'Journal\Transaction\Date'.</span></span>
33. <span data-ttu-id="f5b4a-180">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-180">Click Bind.</span></span>
34. <span data-ttu-id="f5b4a-181">Ve stromovém zobrazení vyberte LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode).</span><span class="sxs-lookup"><span data-stu-id="f5b4a-181">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)'.</span></span>
35. <span data-ttu-id="f5b4a-182">Ve stromovém zobrazení vyberte možnost 'Deník\Transakce\Měna'.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-182">In the tree, select 'Journal\Transaction\Currency'.</span></span>
36. <span data-ttu-id="f5b4a-183">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-183">Click Bind.</span></span>
37. <span data-ttu-id="f5b4a-184">Ve stromovém zobrazení vyberte LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit).</span><span class="sxs-lookup"><span data-stu-id="f5b4a-184">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)'.</span></span>
38. <span data-ttu-id="f5b4a-185">Ve stromovém zobrazení vyberte možnost 'Deník\Transakce\Dal'.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-185">In the tree, select 'Journal\Transaction\Credit'.</span></span>
39. <span data-ttu-id="f5b4a-186">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-186">Click Bind.</span></span>
40. <span data-ttu-id="f5b4a-187">Ve stromovém zobrazení vyberte LedgerJournal\<Relations\LedgerJournalTrans.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-187">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
41. <span data-ttu-id="f5b4a-188">Ve stromovém zobrazení vyberte možnost 'Deník\Transakce'.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-188">In the tree, select 'Journal\Transaction'.</span></span>
42. <span data-ttu-id="f5b4a-189">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-189">Click Bind.</span></span>
43. <span data-ttu-id="f5b4a-190">Ve stromovém zobrazení vyberte 'LedgerJournal\Číslo dávky deníku(JournalNum)'.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-190">In the tree, select 'LedgerJournal\Journal batch number(JournalNum)'.</span></span>
44. <span data-ttu-id="f5b4a-191">Ve stromovém zobrazení vyberte možnost 'Deník\Dávka'.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-191">In the tree, select 'Journal\Batch'.</span></span>
45. <span data-ttu-id="f5b4a-192">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-192">Click Bind.</span></span>
46. <span data-ttu-id="f5b4a-193">Ve stromovém zobrazení vyberte 'LedgerJournal'.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-193">In the tree, select 'LedgerJournal'.</span></span>
47. <span data-ttu-id="f5b4a-194">Ve stromovém zobrazení vyberte 'Deník'.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-194">In the tree, select 'Journal'.</span></span>
48. <span data-ttu-id="f5b4a-195">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-195">Click Bind.</span></span>
49. <span data-ttu-id="f5b4a-196">Ve stromovém zobrazení rozbalte 'Dimenze'.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-196">In the tree, expand 'Dimensions'.</span></span>
50. <span data-ttu-id="f5b4a-197">Ve stromovém zobrazení rozbalte 'Dimenze\Hlavní účet a dimenze'.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-197">In the tree, expand 'Dimensions\Main account and dimensions'.</span></span>
51. <span data-ttu-id="f5b4a-198">Ve stromovém zobrazení rozbalte 'Dimenze\Hlavní účet a dimenze\Definice'.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-198">In the tree, expand 'Dimensions\Main account and dimensions\Definition'.</span></span>
52. <span data-ttu-id="f5b4a-199">Ve stromové struktuře vyberte 'Dimenze\Hlavní účet a dimenze\Defince\Název'.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-199">In the tree, select 'Dimensions\Main account and dimensions\Definition\Name'.</span></span>
53. <span data-ttu-id="f5b4a-200">Ve stromovém zobrazení vyberte 'Nastavení dimenzí\Kód'.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-200">In the tree, select 'Dimensions setting\Code'.</span></span>
54. <span data-ttu-id="f5b4a-201">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-201">Click Bind.</span></span>
55. <span data-ttu-id="f5b4a-202">Ve stromové struktuře vyberte 'Dimenze\Hlavní účet a dimenze\Definice\Název sloupce sestavy'.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-202">In the tree, select 'Dimensions\Main account and dimensions\Definition\Report column name'.</span></span>
56. <span data-ttu-id="f5b4a-203">Ve stromovém zobrazení vyberte 'Nastavení dimenzí\Název'.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-203">In the tree, select 'Dimensions setting\Name'.</span></span>
57. <span data-ttu-id="f5b4a-204">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-204">Click Bind.</span></span>
58. <span data-ttu-id="f5b4a-205">Ve stromovém zobrazení vyberte 'Dimenze\Hlavní účet a dimenze'.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-205">In the tree, select 'Dimensions\Main account and dimensions'.</span></span>
59. <span data-ttu-id="f5b4a-206">Ve stromovém zobrazení vyberte 'Nastavení dimenzí'.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-206">In the tree, select 'Dimensions setting'.</span></span>
60. <span data-ttu-id="f5b4a-207">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-207">Click Bind.</span></span>
61. <span data-ttu-id="f5b4a-208">Ve stromovém zobrazení vyberte 'Společnost'.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-208">In the tree, select 'Company'.</span></span>
62. <span data-ttu-id="f5b4a-209">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-209">Click Edit.</span></span>
63. <span data-ttu-id="f5b4a-210">V poli expressionAsStringText zadejte 'Company.'find()'.'name()''.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-210">In the expressionAsStringText field, enter 'Company.'find()'.'name()''.</span></span>
    * <span data-ttu-id="f5b4a-211">Company.'find()'.'name()'</span><span class="sxs-lookup"><span data-stu-id="f5b4a-211">Company.'find()'.'name()'</span></span>  
64. <span data-ttu-id="f5b4a-212">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-212">Click Save.</span></span>
65. <span data-ttu-id="f5b4a-213">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-213">Close the page.</span></span>
66. <span data-ttu-id="f5b4a-214">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-214">Click Save.</span></span>
67. <span data-ttu-id="f5b4a-215">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-215">Close the page.</span></span>

## <a name="complete-this-draft-models-version"></a><span data-ttu-id="f5b4a-216">Dokončení tohoto konceptu verze modelu</span><span class="sxs-lookup"><span data-stu-id="f5b4a-216">Complete this draft model’s version</span></span>
1. <span data-ttu-id="f5b4a-217">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-217">Close the page.</span></span>
2. <span data-ttu-id="f5b4a-218">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-218">Close the page.</span></span>
3. <span data-ttu-id="f5b4a-219">Klikněte na položku Změnit stav.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-219">Click Change status.</span></span>
4. <span data-ttu-id="f5b4a-220">Klikněte na tlačítko Dokončit.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-220">Click Complete.</span></span>
5. <span data-ttu-id="f5b4a-221">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="f5b4a-221">Click OK.</span></span>

