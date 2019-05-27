---
title: Elektronické vykazování – návrh datového modelu pro určitou doménu
description: Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může vytvořit novou konfiguraci pro elektronické výkaznictví, která obsahuje model dat pro elektronické platební doklady.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERDataContainerDescriptorReferenceSwitchDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0debb7276c4f3e41c2e85ce6bc63b8df5bc159f8
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551511"
---
# <a name="er-design-domain-specific-data-model"></a><span data-ttu-id="33f98-103">Elektronické vykazování – návrh datového modelu pro určitou doménu</span><span class="sxs-lookup"><span data-stu-id="33f98-103">ER Design domain specific data model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="33f98-104">Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může vytvořit novou konfiguraci pro elektronické výkaznictví, která obsahuje model dat pro elektronické platební doklady.</span><span class="sxs-lookup"><span data-stu-id="33f98-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="33f98-105">Tento datový model se použije později jako zdroj dat při vytvoření formátu pro platební doklady.</span><span class="sxs-lookup"><span data-stu-id="33f98-105">This data model will later be used as a data source when you create the format of the payment documents.</span></span>



<span data-ttu-id="33f98-106">V tomto příkladu vytvoříte konfiguraci pro vzorovou společnost Litware, Inc. Tyto kroky lze provést v kterékoli společnosti, protože konfigurace ER se sdílí mezi společnostmi.</span><span class="sxs-lookup"><span data-stu-id="33f98-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="33f98-107">K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v postupu "Vytvoření poskytovatele konfigurace a jeho označení jako aktivního".</span><span class="sxs-lookup"><span data-stu-id="33f98-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

1. <span data-ttu-id="33f98-108">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="33f98-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="33f98-109">Vyberte poskytovatele konfigurace pro vzorovou společnost Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="33f98-109">Select the configuration provider for sample company, ‘Litware, Inc.’</span></span> <span data-ttu-id="33f98-110">Pokud tohoto zprostředkovatele konfigurace nevidíte, musíte nejprve dokončit jednotlivé kroky v postupu "Vytvoření poskytovatele konfigurace a jeho označení jako aktivního".</span><span class="sxs-lookup"><span data-stu-id="33f98-110">If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
2. <span data-ttu-id="33f98-111">Klikněte na Konfigurace výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="33f98-111">Click Reporting configurations.</span></span>
    * <span data-ttu-id="33f98-112">Vytvoříte konfiguraci, která obsahuje model dat pro elektronické platební doklady.</span><span class="sxs-lookup"><span data-stu-id="33f98-112">You will create a configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="33f98-113">Tento datový model se použije později jako zdroj dat při vytvoření formátu pro platební doklady.</span><span class="sxs-lookup"><span data-stu-id="33f98-113">This data model will be used later as a data source when you create the format for the payment documents.</span></span>  

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="33f98-114">Vytvoření nové konfigurace datového modelu</span><span class="sxs-lookup"><span data-stu-id="33f98-114">Create a new data model configuration</span></span>
1. <span data-ttu-id="33f98-115">Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="33f98-115">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="33f98-116">V poli Název zadejte Platby (zjednodušený model).</span><span class="sxs-lookup"><span data-stu-id="33f98-116">In the Name field, type 'Payments (simplified model)'.</span></span>
    * <span data-ttu-id="33f98-117">Platby (zjednodušený model)</span><span class="sxs-lookup"><span data-stu-id="33f98-117">Payments (simplified model)</span></span>  
3. <span data-ttu-id="33f98-118">V poli Popis zadejte „Konfigurace modelu platby“.</span><span class="sxs-lookup"><span data-stu-id="33f98-118">In the Description field, type 'Payment model configuration'.</span></span>
    * <span data-ttu-id="33f98-119">Konfigurace modelu platby</span><span class="sxs-lookup"><span data-stu-id="33f98-119">Payment model configuration</span></span>  
    * <span data-ttu-id="33f98-120">Aktivní poskytovatel konfigurace se zadá automaticky v tomto poli.</span><span class="sxs-lookup"><span data-stu-id="33f98-120">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="33f98-121">Tento zprostředkovatel bude moci udržovat tuto konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="33f98-121">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="33f98-122">Jiní poskytovatelé mohou použít tuto konfiguraci, ale nebudou moci ji spravovat.</span><span class="sxs-lookup"><span data-stu-id="33f98-122">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
4. <span data-ttu-id="33f98-123">Klepnutím na tlačítko Dokončit konfiguraci dokončíte vytvoření konfigurace</span><span class="sxs-lookup"><span data-stu-id="33f98-123">Click ‘Create configuration’ button to complete the configuration creation task</span></span>

## <a name="create-a-data-model"></a><span data-ttu-id="33f98-124">Vytvoření datového modelu</span><span class="sxs-lookup"><span data-stu-id="33f98-124">Create a data model</span></span>
    * <span data-ttu-id="33f98-125">Vytváříte nový datový model pro vybranou konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="33f98-125">You're creating a new data model for the selected configuration.</span></span> <span data-ttu-id="33f98-126">Tato verze konfigurace bude mít stav Koncept.</span><span class="sxs-lookup"><span data-stu-id="33f98-126">This configuration version will have a status of Draft.</span></span>  
1. <span data-ttu-id="33f98-127">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="33f98-127">Click Designer.</span></span>

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a><span data-ttu-id="33f98-128">Definování struktury strany účastnící se v platebním procesu</span><span class="sxs-lookup"><span data-stu-id="33f98-128">Define the structure of a party participating in a payment process</span></span>
1. <span data-ttu-id="33f98-129">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="33f98-129">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="33f98-130">Do pole Název zadejte 'Strana'.</span><span class="sxs-lookup"><span data-stu-id="33f98-130">In the Name field, type 'Party'.</span></span>
    * <span data-ttu-id="33f98-131">Strana</span><span class="sxs-lookup"><span data-stu-id="33f98-131">Party</span></span>  
3. <span data-ttu-id="33f98-132">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="33f98-132">Click Add.</span></span>
4. <span data-ttu-id="33f98-133">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="33f98-133">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="33f98-134">Do pole Název zadejte název.</span><span class="sxs-lookup"><span data-stu-id="33f98-134">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="33f98-135">Jméno</span><span class="sxs-lookup"><span data-stu-id="33f98-135">Name</span></span>  
6. <span data-ttu-id="33f98-136">V poli Typ položky vyberte Řetězec.</span><span class="sxs-lookup"><span data-stu-id="33f98-136">In the Item type field, select 'String'.</span></span>
7. <span data-ttu-id="33f98-137">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="33f98-137">Click Add.</span></span>
8. <span data-ttu-id="33f98-138">Do pole Najít zadejte 'Strana'.</span><span class="sxs-lookup"><span data-stu-id="33f98-138">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="33f98-139">Strana</span><span class="sxs-lookup"><span data-stu-id="33f98-139">Party</span></span>  
9. <span data-ttu-id="33f98-140">Klikněte na Vyhledat předchozí.</span><span class="sxs-lookup"><span data-stu-id="33f98-140">Click Find previous.</span></span>

## <a name="define-the-bank-structure-for-this-model"></a><span data-ttu-id="33f98-141">Definování struktury banky pro tento model</span><span class="sxs-lookup"><span data-stu-id="33f98-141">Define the bank structure for this model</span></span>
1. <span data-ttu-id="33f98-142">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="33f98-142">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="33f98-143">Do pole Název zadejte hodnotu Agent.</span><span class="sxs-lookup"><span data-stu-id="33f98-143">In the Name field, type 'Agent'.</span></span>
    * <span data-ttu-id="33f98-144">Zástupce</span><span class="sxs-lookup"><span data-stu-id="33f98-144">Agent</span></span>  
3. <span data-ttu-id="33f98-145">V poli Typ položky vyberte Záznam.</span><span class="sxs-lookup"><span data-stu-id="33f98-145">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="33f98-146">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="33f98-146">Click Add.</span></span>
5. <span data-ttu-id="33f98-147">V poli Popis zadejte 'Finanční instituce (například banka) obsluhující účet pro stranu (dlužník/věřitel).'.</span><span class="sxs-lookup"><span data-stu-id="33f98-147">In the Description field, enter 'Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).'.</span></span>
    * <span data-ttu-id="33f98-148">Finanční instituce (například banka) obsluhující účet pro stranu (dlužníka/věřitele).</span><span class="sxs-lookup"><span data-stu-id="33f98-148">Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).</span></span>  
6. <span data-ttu-id="33f98-149">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="33f98-149">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="33f98-150">Do pole Název zadejte název.</span><span class="sxs-lookup"><span data-stu-id="33f98-150">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="33f98-151">Jméno</span><span class="sxs-lookup"><span data-stu-id="33f98-151">Name</span></span>  
8. <span data-ttu-id="33f98-152">V poli Typ položky vyberte Řetězec.</span><span class="sxs-lookup"><span data-stu-id="33f98-152">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="33f98-153">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="33f98-153">Click Add.</span></span>
10. <span data-ttu-id="33f98-154">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="33f98-154">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="33f98-155">Do pole Název zadejte SWIFT.</span><span class="sxs-lookup"><span data-stu-id="33f98-155">In the Name field, type 'SWIFT'.</span></span>
    * <span data-ttu-id="33f98-156">SWIFT</span><span class="sxs-lookup"><span data-stu-id="33f98-156">SWIFT</span></span>  
12. <span data-ttu-id="33f98-157">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="33f98-157">Click Add.</span></span>
13. <span data-ttu-id="33f98-158">Do pole Popis zadejte Identifikační kód banky.</span><span class="sxs-lookup"><span data-stu-id="33f98-158">In the Description field, enter 'Bank identification code'.</span></span>
    * <span data-ttu-id="33f98-159">Identifikační kód banky</span><span class="sxs-lookup"><span data-stu-id="33f98-159">Bank identification code</span></span>  
14. <span data-ttu-id="33f98-160">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="33f98-160">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="33f98-161">Do pole Název zadejte „RoutingNumber“.</span><span class="sxs-lookup"><span data-stu-id="33f98-161">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="33f98-162">Směrový kód</span><span class="sxs-lookup"><span data-stu-id="33f98-162">RoutingNumber</span></span>  
16. <span data-ttu-id="33f98-163">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="33f98-163">Click Add.</span></span>
17. <span data-ttu-id="33f98-164">Do pole Popis zadejte 'Směrový kód'.</span><span class="sxs-lookup"><span data-stu-id="33f98-164">In the Description field, enter 'Routing number'.</span></span>
    * <span data-ttu-id="33f98-165">Směrový kód banky</span><span class="sxs-lookup"><span data-stu-id="33f98-165">Routing number</span></span>  
18. <span data-ttu-id="33f98-166">Klikněte na Vyhledat předchozí.</span><span class="sxs-lookup"><span data-stu-id="33f98-166">Click Find previous.</span></span>

## <a name="define-the-bank-account-structure-for-this-model"></a><span data-ttu-id="33f98-167">Definování struktury bankovního účtu pro tento model</span><span class="sxs-lookup"><span data-stu-id="33f98-167">Define the bank account structure for this model</span></span>
1. <span data-ttu-id="33f98-168">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="33f98-168">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="33f98-169">Do pole Název zadejte Účet.</span><span class="sxs-lookup"><span data-stu-id="33f98-169">In the Name field, type 'Account'.</span></span>
    * <span data-ttu-id="33f98-170">Účet</span><span class="sxs-lookup"><span data-stu-id="33f98-170">Account</span></span>  
3. <span data-ttu-id="33f98-171">V poli Typ položky vyberte Záznam.</span><span class="sxs-lookup"><span data-stu-id="33f98-171">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="33f98-172">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="33f98-172">Click Add.</span></span>
5. <span data-ttu-id="33f98-173">Do pole Popis zadejte 'Identifikace účtu strany ve finanční instituci (například bance).'.</span><span class="sxs-lookup"><span data-stu-id="33f98-173">In the Description field, enter 'Identification of an account of a party in a financial institution (for instance, a bank).'.</span></span>
    * <span data-ttu-id="33f98-174">Identifikace účtu strany ve finanční instituci (například bance).</span><span class="sxs-lookup"><span data-stu-id="33f98-174">Identification of an account of a party in a financial institution (for instance, a bank).</span></span>  
6. <span data-ttu-id="33f98-175">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="33f98-175">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="33f98-176">Do pole Název zadejte Měna.</span><span class="sxs-lookup"><span data-stu-id="33f98-176">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="33f98-177">Měna</span><span class="sxs-lookup"><span data-stu-id="33f98-177">Currency</span></span>  
8. <span data-ttu-id="33f98-178">V poli Typ položky vyberte Řetězec.</span><span class="sxs-lookup"><span data-stu-id="33f98-178">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="33f98-179">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="33f98-179">Click Add.</span></span>
10. <span data-ttu-id="33f98-180">Do pole Popis zadejte Kód měny.</span><span class="sxs-lookup"><span data-stu-id="33f98-180">In the Description field, enter 'Currency code'.</span></span>
    * <span data-ttu-id="33f98-181">Kód měny</span><span class="sxs-lookup"><span data-stu-id="33f98-181">Currency code</span></span>  
11. <span data-ttu-id="33f98-182">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="33f98-182">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="33f98-183">Do pole Název zadejte Číslo.</span><span class="sxs-lookup"><span data-stu-id="33f98-183">In the Name field, type 'Number'.</span></span>
    * <span data-ttu-id="33f98-184">Počet</span><span class="sxs-lookup"><span data-stu-id="33f98-184">Number</span></span>  
13. <span data-ttu-id="33f98-185">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="33f98-185">Click Add.</span></span>
14. <span data-ttu-id="33f98-186">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="33f98-186">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="33f98-187">Do pole Název zadejte IBAN.</span><span class="sxs-lookup"><span data-stu-id="33f98-187">In the Name field, type 'IBAN'.</span></span>
    * <span data-ttu-id="33f98-188">KÓD IBAN</span><span class="sxs-lookup"><span data-stu-id="33f98-188">IBAN</span></span>  
16. <span data-ttu-id="33f98-189">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="33f98-189">Click Add.</span></span>
17. <span data-ttu-id="33f98-190">Do pole Popis zadejte 'Číslo IBAN (International Bank Account Number)'.</span><span class="sxs-lookup"><span data-stu-id="33f98-190">In the Description field, enter 'International bank account number'.</span></span>
    * <span data-ttu-id="33f98-191">Číslo IBAN (International Bank Account Number)</span><span class="sxs-lookup"><span data-stu-id="33f98-191">International bank account number</span></span>  

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a><span data-ttu-id="33f98-192">Definování struktury platební zprávy pro platby typu převod kreditu</span><span class="sxs-lookup"><span data-stu-id="33f98-192">Define the payment message structure for credit transfer payment type</span></span>
1. <span data-ttu-id="33f98-193">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="33f98-193">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="33f98-194">Do pole Nový uzel zadejte Kořen modelu.</span><span class="sxs-lookup"><span data-stu-id="33f98-194">In the New node as a field, enter 'Model root'.</span></span>
3. <span data-ttu-id="33f98-195">Zadejte hodnotu CustomerCreditTransferInitiation do pole Název.</span><span class="sxs-lookup"><span data-stu-id="33f98-195">In the Name field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="33f98-196">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="33f98-196">CustomerCreditTransferInitiation</span></span>  
4. <span data-ttu-id="33f98-197">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="33f98-197">Click Add.</span></span>
5. <span data-ttu-id="33f98-198">Do pole Najít zadejte hodnotu 'CustomerCreditTransferInitiation'.</span><span class="sxs-lookup"><span data-stu-id="33f98-198">In the Find field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="33f98-199">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="33f98-199">CustomerCreditTransferInitiation</span></span>  
6. <span data-ttu-id="33f98-200">Klikněte na Vyhledat předchozí.</span><span class="sxs-lookup"><span data-stu-id="33f98-200">Click Find previous.</span></span>
7. <span data-ttu-id="33f98-201">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="33f98-201">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="33f98-202">Do pole Název zadejte „MessageIdentification“.</span><span class="sxs-lookup"><span data-stu-id="33f98-202">In the Name field, type 'MessageIdentification'.</span></span>
    * <span data-ttu-id="33f98-203">MessageIdentification</span><span class="sxs-lookup"><span data-stu-id="33f98-203">MessageIdentification</span></span>  
9. <span data-ttu-id="33f98-204">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="33f98-204">Click Add.</span></span>
10. <span data-ttu-id="33f98-205">V poli Popis zadejte Odkaz Point to Point tak, jak byl přiřazen přikazující straně a odeslán další straně k identifikaci zprávy.</span><span class="sxs-lookup"><span data-stu-id="33f98-205">In the Description field, enter 'The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.'.</span></span>
    * <span data-ttu-id="33f98-206">Odkaz Point to Point tak, jak byl přiřazen přikazující straně a odeslán další straně k identifikaci zprávy.</span><span class="sxs-lookup"><span data-stu-id="33f98-206">The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.</span></span>  
11. <span data-ttu-id="33f98-207">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="33f98-207">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="33f98-208">Do pole Název zadejte „ProcessingDateTime“.</span><span class="sxs-lookup"><span data-stu-id="33f98-208">In the Name field, type 'ProcessingDateTime'.</span></span>
    * <span data-ttu-id="33f98-209">ProcessingDateTime</span><span class="sxs-lookup"><span data-stu-id="33f98-209">ProcessingDateTime</span></span>  
13. <span data-ttu-id="33f98-210">V poli Typ položky vyberte Datum a čas.</span><span class="sxs-lookup"><span data-stu-id="33f98-210">In the Item type field, select 'DateTime'.</span></span>
14. <span data-ttu-id="33f98-211">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="33f98-211">Click Add.</span></span>
15. <span data-ttu-id="33f98-212">Do pole Popis zadejte 'Datum a čas, kdy byla platební zpráva vytvořena.'.</span><span class="sxs-lookup"><span data-stu-id="33f98-212">In the Description field, enter 'Date and time at which the payment message was created.'.</span></span>
    * <span data-ttu-id="33f98-213">Datum a čas, kdy byla platební zpráva vytvořena.</span><span class="sxs-lookup"><span data-stu-id="33f98-213">Date and time at which the payment message was created.</span></span>  
16. <span data-ttu-id="33f98-214">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="33f98-214">Click New to open the drop dialog.</span></span>
    * <span data-ttu-id="33f98-215">Definování struktury platební transakce pro tento model.</span><span class="sxs-lookup"><span data-stu-id="33f98-215">Define the payment transaction structure for this model.</span></span>  
17. <span data-ttu-id="33f98-216">Do pole Název zadejte Platby.</span><span class="sxs-lookup"><span data-stu-id="33f98-216">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="33f98-217">Platby</span><span class="sxs-lookup"><span data-stu-id="33f98-217">Payments</span></span>  
18. <span data-ttu-id="33f98-218">V poli Typ položky vyberte Seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="33f98-218">In the Item type field, select 'Record list'.</span></span>
19. <span data-ttu-id="33f98-219">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="33f98-219">Click Add.</span></span>
20. <span data-ttu-id="33f98-220">Do pole Popis zadejte Řádky platby pro aktuální zprávu.</span><span class="sxs-lookup"><span data-stu-id="33f98-220">In the Description field, enter 'Payment lines of the current message'.</span></span>
    * <span data-ttu-id="33f98-221">Řádky platby pro aktuální zprávu</span><span class="sxs-lookup"><span data-stu-id="33f98-221">Payment lines of the current message</span></span>  
21. <span data-ttu-id="33f98-222">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="33f98-222">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="33f98-223">Do pole Název zadejte Věřitel.</span><span class="sxs-lookup"><span data-stu-id="33f98-223">In the Name field, type 'Creditor'.</span></span>
    * <span data-ttu-id="33f98-224">Věřitel</span><span class="sxs-lookup"><span data-stu-id="33f98-224">Creditor</span></span>  
23. <span data-ttu-id="33f98-225">V poli Typ položky vyberte Záznam.</span><span class="sxs-lookup"><span data-stu-id="33f98-225">In the Item type field, select 'Record'.</span></span>
24. <span data-ttu-id="33f98-226">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="33f98-226">Click Add.</span></span>
25. <span data-ttu-id="33f98-227">V poli Popis zadejte Strana, pro kterou je peněžní částka splatná.</span><span class="sxs-lookup"><span data-stu-id="33f98-227">In the Description field, enter 'Party to which an amount of money is due.'.</span></span>
    * <span data-ttu-id="33f98-228">Strana, pro kterou je peněžní částka splatná.</span><span class="sxs-lookup"><span data-stu-id="33f98-228">Party to which an amount of money is due.</span></span>  
26. <span data-ttu-id="33f98-229">Klikněte na možnost Přepnout odkaz položky.</span><span class="sxs-lookup"><span data-stu-id="33f98-229">Click Switch item reference.</span></span>
27. <span data-ttu-id="33f98-230">Do pole Najít zadejte 'Strana'.</span><span class="sxs-lookup"><span data-stu-id="33f98-230">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="33f98-231">Strana</span><span class="sxs-lookup"><span data-stu-id="33f98-231">Party</span></span>  
28. <span data-ttu-id="33f98-232">Klikněte na Najít další.</span><span class="sxs-lookup"><span data-stu-id="33f98-232">Click Find next.</span></span>
29. <span data-ttu-id="33f98-233">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="33f98-233">Click OK.</span></span>
30. <span data-ttu-id="33f98-234">Do pole Najít zadejte 'Platby'.</span><span class="sxs-lookup"><span data-stu-id="33f98-234">In the Find field, type 'Payments'.</span></span>
    * <span data-ttu-id="33f98-235">Platby</span><span class="sxs-lookup"><span data-stu-id="33f98-235">Payments</span></span>  
31. <span data-ttu-id="33f98-236">Klikněte na Najít další.</span><span class="sxs-lookup"><span data-stu-id="33f98-236">Click Find next.</span></span>
32. <span data-ttu-id="33f98-237">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="33f98-237">Click New to open the drop dialog.</span></span>
33. <span data-ttu-id="33f98-238">Do pole Název zadejte Dlužník.</span><span class="sxs-lookup"><span data-stu-id="33f98-238">In the Name field, type 'Debtor'.</span></span>
    * <span data-ttu-id="33f98-239">Dlužník</span><span class="sxs-lookup"><span data-stu-id="33f98-239">Debtor</span></span>  
34. <span data-ttu-id="33f98-240">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="33f98-240">Click Add.</span></span>
35. <span data-ttu-id="33f98-241">V poli Popis zadejte Strana vlastnící finanční částku pro (konečného) věřitele.</span><span class="sxs-lookup"><span data-stu-id="33f98-241">In the Description field, enter 'Party that owes an amount of money to the (ultimate) creditor.'.</span></span>
    * <span data-ttu-id="33f98-242">Strana vlastnící finanční částku pro (konečného) věřitele.</span><span class="sxs-lookup"><span data-stu-id="33f98-242">Party that owes an amount of money to the (ultimate) creditor.</span></span>  
36. <span data-ttu-id="33f98-243">Klikněte na možnost Přepnout odkaz položky.</span><span class="sxs-lookup"><span data-stu-id="33f98-243">Click Switch item reference.</span></span>
37. <span data-ttu-id="33f98-244">Do pole Najít zadejte 'Strana'.</span><span class="sxs-lookup"><span data-stu-id="33f98-244">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="33f98-245">Strana</span><span class="sxs-lookup"><span data-stu-id="33f98-245">Party</span></span>  
38. <span data-ttu-id="33f98-246">Klikněte na Najít další.</span><span class="sxs-lookup"><span data-stu-id="33f98-246">Click Find next.</span></span>
39. <span data-ttu-id="33f98-247">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="33f98-247">Click OK.</span></span>
40. <span data-ttu-id="33f98-248">Klikněte na Najít další.</span><span class="sxs-lookup"><span data-stu-id="33f98-248">Click Find next.</span></span>
41. <span data-ttu-id="33f98-249">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="33f98-249">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="33f98-250">Do pole Název zadejte Popis.</span><span class="sxs-lookup"><span data-stu-id="33f98-250">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="33f98-251">popis</span><span class="sxs-lookup"><span data-stu-id="33f98-251">Description</span></span>  
43. <span data-ttu-id="33f98-252">V poli Typ položky vyberte Řetězec.</span><span class="sxs-lookup"><span data-stu-id="33f98-252">In the Item type field, select 'String'.</span></span>
44. <span data-ttu-id="33f98-253">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="33f98-253">Click Add.</span></span>
45. <span data-ttu-id="33f98-254">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="33f98-254">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="33f98-255">Do pole Název zadejte Měna.</span><span class="sxs-lookup"><span data-stu-id="33f98-255">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="33f98-256">Měna</span><span class="sxs-lookup"><span data-stu-id="33f98-256">Currency</span></span>  
47. <span data-ttu-id="33f98-257">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="33f98-257">Click Add.</span></span>
48. <span data-ttu-id="33f98-258">Do pole Popis zadejte Kód měny.</span><span class="sxs-lookup"><span data-stu-id="33f98-258">In the Description field, enter 'Currency code'.</span></span>
    * <span data-ttu-id="33f98-259">Kód měny</span><span class="sxs-lookup"><span data-stu-id="33f98-259">Currency code</span></span>  
49. <span data-ttu-id="33f98-260">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="33f98-260">Click New to open the drop dialog.</span></span>
50. <span data-ttu-id="33f98-261">Do pole Název zadejte Datum transakce.</span><span class="sxs-lookup"><span data-stu-id="33f98-261">In the Name field, type 'TransactionDate'.</span></span>
    * <span data-ttu-id="33f98-262">Datum transakce</span><span class="sxs-lookup"><span data-stu-id="33f98-262">TransactionDate</span></span>  
51. <span data-ttu-id="33f98-263">V poli Typ položky vyberte Datum.</span><span class="sxs-lookup"><span data-stu-id="33f98-263">In the Item type field, select 'Date'.</span></span>
52. <span data-ttu-id="33f98-264">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="33f98-264">Click Add.</span></span>
53. <span data-ttu-id="33f98-265">Do pole Popis zadejte 'Datum transakce'.</span><span class="sxs-lookup"><span data-stu-id="33f98-265">In the Description field, enter 'Transaction date'.</span></span>
    * <span data-ttu-id="33f98-266">Datum transakce</span><span class="sxs-lookup"><span data-stu-id="33f98-266">Transaction date</span></span>  
54. <span data-ttu-id="33f98-267">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="33f98-267">Click New to open the drop dialog.</span></span>
55. <span data-ttu-id="33f98-268">Do pole Název zadejte Požadovaná částka.</span><span class="sxs-lookup"><span data-stu-id="33f98-268">In the Name field, type 'InstructedAmount'.</span></span>
    * <span data-ttu-id="33f98-269">Požadovaná částka</span><span class="sxs-lookup"><span data-stu-id="33f98-269">InstructedAmount</span></span>  
56. <span data-ttu-id="33f98-270">V poli Typ položky vyberte Reálný.</span><span class="sxs-lookup"><span data-stu-id="33f98-270">In the Item type field, select 'Real'.</span></span>
57. <span data-ttu-id="33f98-271">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="33f98-271">Click Add.</span></span>
58. <span data-ttu-id="33f98-272">V poli Popis uveďte Peněžní částka, která má být přesunuta mezi dlužníkem a věřitelem před odečtením poplatků.</span><span class="sxs-lookup"><span data-stu-id="33f98-272">In the Description field, enter 'The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="33f98-273">Částka by měla být vyjádřená v měně podle objednávky strany příkazce.</span><span class="sxs-lookup"><span data-stu-id="33f98-273">The amount should be expressed in the currency as ordered by the initiating party.'.</span></span>
    * <span data-ttu-id="33f98-274">Peněžní částka, která má být přesunuta mezi dlužníkem a věřitelem před odečtením poplatků.</span><span class="sxs-lookup"><span data-stu-id="33f98-274">The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="33f98-275">Částka by měla být vyjádřená v měně podle objednávky strany příkazce.</span><span class="sxs-lookup"><span data-stu-id="33f98-275">The amount should be expressed in the currency as ordered by the initiating party.</span></span>  
59. <span data-ttu-id="33f98-276">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="33f98-276">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="33f98-277">Zadejte text „End2EndID“ do pole Název.</span><span class="sxs-lookup"><span data-stu-id="33f98-277">In the Name field, type 'End2EndID'.</span></span>
    * <span data-ttu-id="33f98-278">End2EndID</span><span class="sxs-lookup"><span data-stu-id="33f98-278">End2EndID</span></span>  
61. <span data-ttu-id="33f98-279">V poli Typ položky vyberte Řetězec.</span><span class="sxs-lookup"><span data-stu-id="33f98-279">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="33f98-280">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="33f98-280">Click Add.</span></span>
63. <span data-ttu-id="33f98-281">Do pole Popis zadejte hodnotu 'Jedinečná identifikace přiřazena stranou příkazce'.</span><span class="sxs-lookup"><span data-stu-id="33f98-281">In the Description field, enter 'The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="33f98-282">Tato identifikace se přenáší beze změny v průběhu celého řetězce od začátku do konce.</span><span class="sxs-lookup"><span data-stu-id="33f98-282">This identification is passed on, unchanged, throughout the entire end-to-end chain.'.</span></span>
    * <span data-ttu-id="33f98-283">Jedinečná identifikace přiřazena stranou příkazce.</span><span class="sxs-lookup"><span data-stu-id="33f98-283">The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="33f98-284">Tato identifikace se přenáší beze změny v průběhu celého řetězce od začátku do konce.</span><span class="sxs-lookup"><span data-stu-id="33f98-284">This identification is passed on, unchanged, throughout the entire end-to-end chain.</span></span>  
64. <span data-ttu-id="33f98-285">Zadejte PaymentModel do pole Název.</span><span class="sxs-lookup"><span data-stu-id="33f98-285">In the Name field, type 'PaymentModel'.</span></span>
    * <span data-ttu-id="33f98-286">Název PaymentModel vychází z předdefinovaných rozhraní formulářů plateb.</span><span class="sxs-lookup"><span data-stu-id="33f98-286">The PaymentModel name aligns with predefined interfaces of payment forms.</span></span>  
65. <span data-ttu-id="33f98-287">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="33f98-287">Click Save.</span></span>
66. <span data-ttu-id="33f98-288">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="33f98-288">Close the page.</span></span>

