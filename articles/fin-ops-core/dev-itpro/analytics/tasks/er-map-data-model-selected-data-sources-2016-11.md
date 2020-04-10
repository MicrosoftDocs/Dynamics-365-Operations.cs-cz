---
title: Elektronické vykazování – namapování datového modelu na vybrané zdroje dat
description: Následující postup popisuje, jak uživatel s rolí správce systému nebo návrháře elektronického výkaznictví může mapovat datový model elektronického výkaznictví (ER) na vybrané zdroje dat Microsoft Dynamics 365 Finance.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cf19d69c498da32594e17e16fb83ed25e6747982
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142978"
---
# <a name="er-map-data-model-to-selected-data-sources"></a><span data-ttu-id="22a85-103">Elektronické vykazování – namapování datového modelu na vybrané zdroje dat</span><span class="sxs-lookup"><span data-stu-id="22a85-103">ER Map data model to selected data sources</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="22a85-104">Následující postup popisuje, jak uživatel s rolí správce systému nebo návrháře elektronického výkaznictví může mapovat datový model elektronického výkaznictví (ER) na vybrané zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="22a85-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can map an Electronic reporting (ER) data model to selected data sources.</span></span> <span data-ttu-id="22a85-105">Toto mapování modelu bude později použito jako zdroj dat v konfiguraci formátu, která se použije ke správě dokumentů elektronické platby.</span><span class="sxs-lookup"><span data-stu-id="22a85-105">This model mapping will later be used as a data source in a format configuration that will be used to manage electronic payment documents.</span></span> <span data-ttu-id="22a85-106">V tomto příkladu namapujete datový model pro vzorovou společnost Litware, Inc. na zdroje dat.</span><span class="sxs-lookup"><span data-stu-id="22a85-106">In this example, you map a data model for sample company, Litware, Inc. to data sources.</span></span> <span data-ttu-id="22a85-107">Aby bylo možné tyto kroky provést, musíte nejprve dokončit kroky postupu „Volba zdroje dat pro mapování modelu“.</span><span class="sxs-lookup"><span data-stu-id="22a85-107">To complete these steps, you must first complete the steps in the "Select data sources for model mapping" procedure.</span></span>


## <a name="open-er-configurations-tree"></a><span data-ttu-id="22a85-108">Otevření stromu konfigurací elektronického vykazování</span><span class="sxs-lookup"><span data-stu-id="22a85-108">Open ER configurations tree</span></span>
1. <span data-ttu-id="22a85-109">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="22a85-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="22a85-110">Klikněte na Konfigurace.</span><span class="sxs-lookup"><span data-stu-id="22a85-110">Click Configurations.</span></span>

## <a name="select-created-model-mapping"></a><span data-ttu-id="22a85-111">Volba vytvořeného mapování modelu</span><span class="sxs-lookup"><span data-stu-id="22a85-111">Select created model mapping</span></span>
1. <span data-ttu-id="22a85-112">Ve stromovém zobrazení vyberte možnost „Platby (zjednodušený model)“.</span><span class="sxs-lookup"><span data-stu-id="22a85-112">In the tree, select 'Payments (simplified model)'.</span></span>
    * <span data-ttu-id="22a85-113">Ujistěte se, že byla předem vytvořena konfigurace modelu „Platby (zjednodušený model)“.</span><span class="sxs-lookup"><span data-stu-id="22a85-113">Make sure that the model configuration "Payments (simplified model)" has been created in advance.</span></span> <span data-ttu-id="22a85-114">V opačném případě nyní přestaňte a vraťte se po dokončení průvodce záznamem úloh ‘Vytvoření nové konfigurace s datovým modelem zvolené domény‘.</span><span class="sxs-lookup"><span data-stu-id="22a85-114">Otherwise, stop now and return after completion of the task guide 'Create a new configuration with data model of the selected domain'.</span></span>  
2. <span data-ttu-id="22a85-115">Klikněte na Návrhář modelů.</span><span class="sxs-lookup"><span data-stu-id="22a85-115">Click Model designer.</span></span>
3. <span data-ttu-id="22a85-116">Klikněte na možnost Mapovat model na datový zdroj.</span><span class="sxs-lookup"><span data-stu-id="22a85-116">Click Map model to datasource.</span></span>
4. <span data-ttu-id="22a85-117">Vyberte záznam „Mapování Dal“.</span><span class="sxs-lookup"><span data-stu-id="22a85-117">Select the 'CT mapping' record.</span></span>
    * <span data-ttu-id="22a85-118">Mapování Dal</span><span class="sxs-lookup"><span data-stu-id="22a85-118">CT mapping</span></span>  

## <a name="bind-created-data-sources-to-data-model-elements"></a><span data-ttu-id="22a85-119">Vytvoření vazby vytvořených zdrojů dat s prvky datového modelu</span><span class="sxs-lookup"><span data-stu-id="22a85-119">Bind created data sources to data model elements</span></span>
1. <span data-ttu-id="22a85-120">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="22a85-120">Click Designer.</span></span>
2. <span data-ttu-id="22a85-121">Ve stromovém zobrazení vyberte možnost „Datum a čas zpracování(ProcessingDateTime)“.</span><span class="sxs-lookup"><span data-stu-id="22a85-121">In the tree, select 'Processing date & time(ProcessingDateTime)'.</span></span>
3. <span data-ttu-id="22a85-122">Ve stromovém zobrazení vyberte možnost „Datum zpracování(ProcessingDateTime)“.</span><span class="sxs-lookup"><span data-stu-id="22a85-122">In the tree, select 'Processing date(ProcessingDateTime)'.</span></span>
4. <span data-ttu-id="22a85-123">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="22a85-123">Click Bind.</span></span>
5. <span data-ttu-id="22a85-124">Ve stromovém zobrazení vyberte „Identifikace zprávy o platbě(MessageIdentification)“.</span><span class="sxs-lookup"><span data-stu-id="22a85-124">In the tree, select 'Payment message identification(MessageIdentification)'.</span></span>
6. <span data-ttu-id="22a85-125">Ve stromovém zobrazení rozbalte možnost Transakce.</span><span class="sxs-lookup"><span data-stu-id="22a85-125">In the tree, expand 'Transactions'.</span></span>
7. <span data-ttu-id="22a85-126">Ve stromovém zobrazení vyberte „Transakce\Číslo dávky deníku(JournalNum)“.</span><span class="sxs-lookup"><span data-stu-id="22a85-126">In the tree, select 'Transactions\Journal batch number(JournalNum)'.</span></span>
8. <span data-ttu-id="22a85-127">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="22a85-127">Click Bind.</span></span>
9. <span data-ttu-id="22a85-128">Ve stromu vyberte „Platby“.</span><span class="sxs-lookup"><span data-stu-id="22a85-128">In the tree, select 'Payments'.</span></span>
10. <span data-ttu-id="22a85-129">Ve stromovém zobrazení vyberte možnost „Transakce“.</span><span class="sxs-lookup"><span data-stu-id="22a85-129">In the tree, select 'Transactions'.</span></span>
11. <span data-ttu-id="22a85-130">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="22a85-130">Click Bind.</span></span>
12. <span data-ttu-id="22a85-131">Ve stromovém zobrazení rozbalte „Platby= Transakce“.</span><span class="sxs-lookup"><span data-stu-id="22a85-131">In the tree, expand 'Payments= Transactions'.</span></span>
13. <span data-ttu-id="22a85-132">Ve stromovém zobrazení rozbalte „Platby= Transakce\Věřitel“.</span><span class="sxs-lookup"><span data-stu-id="22a85-132">In the tree, expand 'Payments= Transactions\Creditor'.</span></span>
14. <span data-ttu-id="22a85-133">Ve stromovém zobrazení rozbalte „Platby= Transakce\Věřitel\Účet“.</span><span class="sxs-lookup"><span data-stu-id="22a85-133">In the tree, expand 'Payments= Transactions\Creditor\Account'.</span></span>
15. <span data-ttu-id="22a85-134">Ve stromovém zobrazení vyberte „Platby= Transakce\Věřitel\Účet\Kód měny(Měna)“.</span><span class="sxs-lookup"><span data-stu-id="22a85-134">In the tree, select 'Payments= Transactions\Creditor\Account\Currency code(Currency)'.</span></span>
16. <span data-ttu-id="22a85-135">Ve stromovém zobrazení rozbalte „Transakce\vendBankAccountInTransactionCompany()“.</span><span class="sxs-lookup"><span data-stu-id="22a85-135">In the tree, expand 'Transactions\vendBankAccountInTransactionCompany()'.</span></span>
17. <span data-ttu-id="22a85-136">Ve stromovém zobrazení vyberte „Transakce\vendBankAccountInTransactionCompany()\Currency(CurrencyCode)“.</span><span class="sxs-lookup"><span data-stu-id="22a85-136">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Currency(CurrencyCode)'.</span></span>
18. <span data-ttu-id="22a85-137">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="22a85-137">Click Bind.</span></span>
19. <span data-ttu-id="22a85-138">Ve stromovém zobrazení vyberte „Platby= Transakce\Věřitel\Účet\Kód IBAN (IBAN)“.</span><span class="sxs-lookup"><span data-stu-id="22a85-138">In the tree, select 'Payments= Transactions\Creditor\Account\IBAN code(IBAN)'.</span></span>
20. <span data-ttu-id="22a85-139">Ve stromovém zobrazení vyberte „Transakce\vendBankAccountInTransactionCompany()\IBAN(BankIBAN)“.</span><span class="sxs-lookup"><span data-stu-id="22a85-139">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\IBAN(BankIBAN)'.</span></span>
21. <span data-ttu-id="22a85-140">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="22a85-140">Click Bind.</span></span>
22. <span data-ttu-id="22a85-141">Ve stromovém zobrazení vyberte „Platby= Transakce\Věřitel\Účet\Číslo“.</span><span class="sxs-lookup"><span data-stu-id="22a85-141">In the tree, select 'Payments= Transactions\Creditor\Account\Number'.</span></span>
23. <span data-ttu-id="22a85-142">Ve stromovém zobrazení vyberte „Transakce\vendBankAccountInTransactionCompany()\Číslo bankovního účtu(AccountNum)“.</span><span class="sxs-lookup"><span data-stu-id="22a85-142">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Bank account number(AccountNum)'.</span></span>
24. <span data-ttu-id="22a85-143">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="22a85-143">Click Bind.</span></span>
25. <span data-ttu-id="22a85-144">Ve stromovém zobrazení rozbalte „Platby= Transakce\Věřitel\Zástupce“.</span><span class="sxs-lookup"><span data-stu-id="22a85-144">In the tree, expand 'Payments= Transactions\Creditor\Agent'.</span></span>
26. <span data-ttu-id="22a85-145">Ve stromovém zobrazení vyberte „Platby= Transakce\Věřitel\Zástupce\Jméno“.</span><span class="sxs-lookup"><span data-stu-id="22a85-145">In the tree, select 'Payments= Transactions\Creditor\Agent\Name'.</span></span>
27. <span data-ttu-id="22a85-146">Ve stromovém zobrazení vyberte „Transakce\vendBankAccountInTransactionCompany()\Název“.</span><span class="sxs-lookup"><span data-stu-id="22a85-146">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Name'.</span></span>
28. <span data-ttu-id="22a85-147">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="22a85-147">Click Bind.</span></span>
29. <span data-ttu-id="22a85-148">Ve stromovém zobrazení vyberte „Platby= Transakce\Věřitel\Zástupce\Směrový kód(RoutingNumber)“.</span><span class="sxs-lookup"><span data-stu-id="22a85-148">In the tree, select 'Payments= Transactions\Creditor\Agent\Routing number(RoutingNumber)'.</span></span>
30. <span data-ttu-id="22a85-149">Ve stromovém zobrazení vyberte „Transakce\vendBankAccountInTransactionCompany()\Směrový kód(RegistrationNum)“.</span><span class="sxs-lookup"><span data-stu-id="22a85-149">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Routing number(RegistrationNum)'.</span></span>
31. <span data-ttu-id="22a85-150">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="22a85-150">Click Bind.</span></span>
32. <span data-ttu-id="22a85-151">Ve stromovém zobrazení vyberte „Platby= Transakce\Věřitel\Zástupce\Kód SWIFT(SWIFT)“.</span><span class="sxs-lookup"><span data-stu-id="22a85-151">In the tree, select 'Payments= Transactions\Creditor\Agent\SWIFT code(SWIFT)'.</span></span>
33. <span data-ttu-id="22a85-152">Ve stromovém zobrazení vyberte „Transakce\vendBankAccountInTransactionCompany()\Kód SWIFT(SWIFTNo)“.</span><span class="sxs-lookup"><span data-stu-id="22a85-152">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\SWIFT code(SWIFTNo)'.</span></span>
34. <span data-ttu-id="22a85-153">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="22a85-153">Click Bind.</span></span>
35. <span data-ttu-id="22a85-154">Ve stromovém zobrazení vyberte „Platby= Transakce\Věřitel\Název“.</span><span class="sxs-lookup"><span data-stu-id="22a85-154">In the tree, select 'Payments= Transactions\Creditor\Name'.</span></span>
36. <span data-ttu-id="22a85-155">Ve stromovém zobrazení rozbalte „Transakce\findVendTable()“.</span><span class="sxs-lookup"><span data-stu-id="22a85-155">In the tree, expand 'Transactions\findVendTable()'.</span></span>
37. <span data-ttu-id="22a85-156">Ve stromovém zobrazení vyberte „Transakce\findVendTable()\name()'.</span><span class="sxs-lookup"><span data-stu-id="22a85-156">In the tree, select 'Transactions\findVendTable()\name()'.</span></span>
38. <span data-ttu-id="22a85-157">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="22a85-157">Click Bind.</span></span>
39. <span data-ttu-id="22a85-158">Ve stromovém zobrazení vyberte „Platby= Transakce\Kód měny(Měna)“.</span><span class="sxs-lookup"><span data-stu-id="22a85-158">In the tree, select 'Payments= Transactions\Currency code(Currency)'.</span></span>
40. <span data-ttu-id="22a85-159">Ve stromovém zobrazení rozbalte Transactions\>Relations.</span><span class="sxs-lookup"><span data-stu-id="22a85-159">In the tree, expand 'Transactions\>Relations'.</span></span>
41. <span data-ttu-id="22a85-160">Ve stromovém zobrazení rozbalte Transactions\>Relations\Currency table(Currency).</span><span class="sxs-lookup"><span data-stu-id="22a85-160">In the tree, expand 'Transactions\>Relations\Currency table(Currency)'.</span></span>
42. <span data-ttu-id="22a85-161">Ve stromovém zobrazení vyberte Transactions\>Relations\Currency table(Currency)\Currency code(CurrencyCodeISO).</span><span class="sxs-lookup"><span data-stu-id="22a85-161">In the tree, select 'Transactions\>Relations\Currency table(Currency)\Currency code(CurrencyCodeISO)'.</span></span>
43. <span data-ttu-id="22a85-162">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="22a85-162">Click Bind.</span></span>
44. <span data-ttu-id="22a85-163">Ve stromovém zobrazení rozbalte „Platby= Transakce\Dlužník“.</span><span class="sxs-lookup"><span data-stu-id="22a85-163">In the tree, expand 'Payments= Transactions\Debtor'.</span></span>
45. <span data-ttu-id="22a85-164">Ve stromovém zobrazení rozbalte „Platby= Transakce\Dlužník\Účet“.</span><span class="sxs-lookup"><span data-stu-id="22a85-164">In the tree, expand 'Payments= Transactions\Debtor\Account'.</span></span>
46. <span data-ttu-id="22a85-165">Ve stromovém zobrazení vyberte „Platby= Transakce\Dlužník\Účet\Kód měny(Měna)“.</span><span class="sxs-lookup"><span data-stu-id="22a85-165">In the tree, select 'Payments= Transactions\Debtor\Account\Currency code(Currency)'.</span></span>
47. <span data-ttu-id="22a85-166">Ve stromovém zobrazení vyberte „Bankovní účet(BankAccount)“.</span><span class="sxs-lookup"><span data-stu-id="22a85-166">In the tree, select 'Bank Account(BankAccount)'.</span></span>
48. <span data-ttu-id="22a85-167">Ve stromovém zobrazení rozbalte „Bankovní účet(BankAccount)“.</span><span class="sxs-lookup"><span data-stu-id="22a85-167">In the tree, expand 'Bank Account(BankAccount)'.</span></span>
49. <span data-ttu-id="22a85-168">Ve stromovém zobrazení vyberte „Bankovní účet(BankAccount)\Měna(CurrencyCode)“.</span><span class="sxs-lookup"><span data-stu-id="22a85-168">In the tree, select 'Bank Account(BankAccount)\Currency(CurrencyCode)'.</span></span>
50. <span data-ttu-id="22a85-169">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="22a85-169">Click Bind.</span></span>
51. <span data-ttu-id="22a85-170">Ve stromovém zobrazení vyberte „Bankovní účet(BankAccount)\IBAN“.</span><span class="sxs-lookup"><span data-stu-id="22a85-170">In the tree, select 'Bank Account(BankAccount)\IBAN'.</span></span>
52. <span data-ttu-id="22a85-171">Ve stromovém zobrazení vyberte „Platby= Transakce\Dlužník\Účet\Kód IBAN(IBAN)“.</span><span class="sxs-lookup"><span data-stu-id="22a85-171">In the tree, select 'Payments= Transactions\Debtor\Account\IBAN code(IBAN)'.</span></span>
53. <span data-ttu-id="22a85-172">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="22a85-172">Click Bind.</span></span>
54. <span data-ttu-id="22a85-173">Ve stromovém zobrazení vyberte „Platby= Transakce\Dlužník\Účet\Číslo“.</span><span class="sxs-lookup"><span data-stu-id="22a85-173">In the tree, select 'Payments= Transactions\Debtor\Account\Number'.</span></span>
55. <span data-ttu-id="22a85-174">Ve stromovém zobrazení vyberte „Bankovní účet(BankAccount)\Číslo bankovního účtu(AccountNum)“.</span><span class="sxs-lookup"><span data-stu-id="22a85-174">In the tree, select 'Bank Account(BankAccount)\Bank account number(AccountNum)'.</span></span>
56. <span data-ttu-id="22a85-175">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="22a85-175">Click Bind.</span></span>
57. <span data-ttu-id="22a85-176">Ve stromovém zobrazení rozbalte „Platby= Transakce\Dlužník\Zástupce“.</span><span class="sxs-lookup"><span data-stu-id="22a85-176">In the tree, expand 'Payments= Transactions\Debtor\Agent'.</span></span>
58. <span data-ttu-id="22a85-177">Ve stromovém zobrazení vyberte „Platby= Transakce\Dlužník\Zástupce\Jméno“.</span><span class="sxs-lookup"><span data-stu-id="22a85-177">In the tree, select 'Payments= Transactions\Debtor\Agent\Name'.</span></span>
59. <span data-ttu-id="22a85-178">Ve stromovém zobrazení vyberte „Bankovní účet(BankAccount)\Název“.</span><span class="sxs-lookup"><span data-stu-id="22a85-178">In the tree, select 'Bank Account(BankAccount)\Name'.</span></span>
60. <span data-ttu-id="22a85-179">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="22a85-179">Click Bind.</span></span>
61. <span data-ttu-id="22a85-180">Ve stromovém zobrazení vyberte „Platby= Transakce\Dlužník\Zástupce\Směrový kód(RoutingNumber)“.</span><span class="sxs-lookup"><span data-stu-id="22a85-180">In the tree, select 'Payments= Transactions\Debtor\Agent\Routing number(RoutingNumber)'.</span></span>
62. <span data-ttu-id="22a85-181">Ve stromovém zobrazení vyberte „Bankovní účet(BankAccount)\Směrový kód(RegistrationNum)“.</span><span class="sxs-lookup"><span data-stu-id="22a85-181">In the tree, select 'Bank Account(BankAccount)\Routing number(RegistrationNum)'.</span></span>
63. <span data-ttu-id="22a85-182">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="22a85-182">Click Bind.</span></span>
64. <span data-ttu-id="22a85-183">Ve stromovém zobrazení vyberte „Platby= Transakce\Dlužník\Zástupce\Kód SWIFT(SWIFT)“.</span><span class="sxs-lookup"><span data-stu-id="22a85-183">In the tree, select 'Payments= Transactions\Debtor\Agent\SWIFT code(SWIFT)'.</span></span>
65. <span data-ttu-id="22a85-184">Ve stromovém zobrazení vyberte „Bankovní účet(BankAccount)\Kód SWIFT(SWIFTNo)“.</span><span class="sxs-lookup"><span data-stu-id="22a85-184">In the tree, select 'Bank Account(BankAccount)\SWIFT code(SWIFTNo)'.</span></span>
66. <span data-ttu-id="22a85-185">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="22a85-185">Click Bind.</span></span>
67. <span data-ttu-id="22a85-186">Ve stromovém zobrazení vyberte „Platby= Transakce\Dlužník\Název“.</span><span class="sxs-lookup"><span data-stu-id="22a85-186">In the tree, select 'Payments= Transactions\Debtor\Name'.</span></span>
68. <span data-ttu-id="22a85-187">Ve stromovém zobrazení vyberte „Informace o společnosti(Společnost)“.</span><span class="sxs-lookup"><span data-stu-id="22a85-187">In the tree, select 'Company information(Company)'.</span></span>
69. <span data-ttu-id="22a85-188">Ve stromovém zobrazení rozbalte „Informace o společnosti(Společnost)“.</span><span class="sxs-lookup"><span data-stu-id="22a85-188">In the tree, expand 'Company information(Company)'.</span></span>
70. <span data-ttu-id="22a85-189">Ve stromovém zobrazení vyberte „Informace o společnosti(Společnost)\Název“.</span><span class="sxs-lookup"><span data-stu-id="22a85-189">In the tree, select 'Company information(Company)\Name'.</span></span>
71. <span data-ttu-id="22a85-190">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="22a85-190">Click Bind.</span></span>
72. <span data-ttu-id="22a85-191">Ve stromovém zobrazení vyberte „Platby= Transakce\Popis“.</span><span class="sxs-lookup"><span data-stu-id="22a85-191">In the tree, select 'Payments= Transactions\Description'.</span></span>
73. <span data-ttu-id="22a85-192">Ve stromovém zobrazení vyberte „Transakce\Popis(Txt)“.</span><span class="sxs-lookup"><span data-stu-id="22a85-192">In the tree, select 'Transactions\Description(Txt)'.</span></span>
74. <span data-ttu-id="22a85-193">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="22a85-193">Click Bind.</span></span>
75. <span data-ttu-id="22a85-194">Ve stromovém zobrazení vyberte „Platby= Transakce\Koncový identifikační kód(End2EndID)“.</span><span class="sxs-lookup"><span data-stu-id="22a85-194">In the tree, select 'Payments= Transactions\End to end identification code(End2EndID)'.</span></span>
76. <span data-ttu-id="22a85-195">Ve stromovém zobrazení vyberte možnost 'Transactions\$EndToEndID.</span><span class="sxs-lookup"><span data-stu-id="22a85-195">In the tree, select 'Transactions\$EndToEndID'.</span></span>
77. <span data-ttu-id="22a85-196">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="22a85-196">Click Bind.</span></span>
78. <span data-ttu-id="22a85-197">Ve stromovém zobrazení vyberte „Platby= Transakce\Požadovaná částka(InstructedAmount)“.</span><span class="sxs-lookup"><span data-stu-id="22a85-197">In the tree, select 'Payments= Transactions\Instructed amount(InstructedAmount)'.</span></span>
79. <span data-ttu-id="22a85-198">Ve stromovém zobrazení vyberte možnost Transactions\$Amount.</span><span class="sxs-lookup"><span data-stu-id="22a85-198">In the tree, select 'Transactions\$Amount'.</span></span>
80. <span data-ttu-id="22a85-199">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="22a85-199">Click Bind.</span></span>
81. <span data-ttu-id="22a85-200">Ve stromovém zobrazení vyberte „Platby= Transakce\Datum transakce(TransactionDate)“.</span><span class="sxs-lookup"><span data-stu-id="22a85-200">In the tree, select 'Payments= Transactions\Transaction date(TransactionDate)'.</span></span>
82. <span data-ttu-id="22a85-201">Ve stromovém zobrazení vyberte „Transakce\Datum(TransDate)“.</span><span class="sxs-lookup"><span data-stu-id="22a85-201">In the tree, select 'Transactions\Date(TransDate)'.</span></span>
83. <span data-ttu-id="22a85-202">Klikněte na možnost Vazba.</span><span class="sxs-lookup"><span data-stu-id="22a85-202">Click Bind.</span></span>

## <a name="validate-created-mapping"></a><span data-ttu-id="22a85-203">Ověření vytvořeného mapování</span><span class="sxs-lookup"><span data-stu-id="22a85-203">Validate created mapping</span></span>
1. <span data-ttu-id="22a85-204">Klikněte na tlačítko Ověřit.</span><span class="sxs-lookup"><span data-stu-id="22a85-204">Click Validate.</span></span>
    * <span data-ttu-id="22a85-205">Ověřte nové mapování, abyste se ujistili, že všechny vazby jsou v pořádku.</span><span class="sxs-lookup"><span data-stu-id="22a85-205">Validate the new mapping to ensure that all bindings are okay.</span></span>  
2. <span data-ttu-id="22a85-206">Kliknutím na šipku rozbalte nebo sbalte oddíl Seznam chyb.</span><span class="sxs-lookup"><span data-stu-id="22a85-206">Click the arrow to expand or collapse the Error List section.</span></span>
3. <span data-ttu-id="22a85-207">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="22a85-207">Click Save.</span></span>
4. <span data-ttu-id="22a85-208">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="22a85-208">Close the page.</span></span>
5. <span data-ttu-id="22a85-209">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="22a85-209">Close the page.</span></span>
6. <span data-ttu-id="22a85-210">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="22a85-210">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-model-configuration"></a><span data-ttu-id="22a85-211">Změna stavu aktuální verze konfigurace modelu</span><span class="sxs-lookup"><span data-stu-id="22a85-211">Change the status of the current version of model configuration</span></span>
1. <span data-ttu-id="22a85-212">Klikněte na položku Změnit stav.</span><span class="sxs-lookup"><span data-stu-id="22a85-212">Click Change status.</span></span>
    * <span data-ttu-id="22a85-213">Změňte stav navržené konfigurace modelu z Návrh na Dokočeno, aby byla konfigurace dostupná pro návrh formátu platby.</span><span class="sxs-lookup"><span data-stu-id="22a85-213">Change the status of designed model configuration – from Draft to Completed to make it available for payment format design.</span></span>  
2. <span data-ttu-id="22a85-214">Klikněte na tlačítko Dokončit.</span><span class="sxs-lookup"><span data-stu-id="22a85-214">Click Complete.</span></span>
    * <span data-ttu-id="22a85-215">Zvolte Dokončeno.</span><span class="sxs-lookup"><span data-stu-id="22a85-215">Select Complete.</span></span>  
3. <span data-ttu-id="22a85-216">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="22a85-216">In the Description field, type a value.</span></span>
    * <span data-ttu-id="22a85-217">Například 'verze 1'.</span><span class="sxs-lookup"><span data-stu-id="22a85-217">For example, 'version 1'.</span></span>  
4. <span data-ttu-id="22a85-218">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="22a85-218">Click OK.</span></span>
5. <span data-ttu-id="22a85-219">Vyberte dokončenou verzi aktuální konfigurace.</span><span class="sxs-lookup"><span data-stu-id="22a85-219">Select the completed version of the current configuration.</span></span>
    * <span data-ttu-id="22a85-220">Všimněte si, že je vytvořená konfigurace uložena jako dokončená verze 1.</span><span class="sxs-lookup"><span data-stu-id="22a85-220">Note that the created configuration is saved as completed version 1.</span></span>  

