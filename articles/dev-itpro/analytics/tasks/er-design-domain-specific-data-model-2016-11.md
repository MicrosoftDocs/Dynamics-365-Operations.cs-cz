--- 
title: "Návrh datového modelu pro určitou doménu pro elektronické výkaznictví (ER)"
description: "Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může vytvořit novou konfiguraci pro elektronické výkaznictví, která obsahuje model dat pro elektronické platební doklady."
author: NickSelin
manager: AnnBe
ms.date: 12/21/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: dff076c83c225b1a3379200537c8bfb23957ee23
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---
# <a name="design-a-domain-specific-data-model-for-electronic-reporting-er"></a><span data-ttu-id="c3b90-103">Návrh datového modelu pro určitou doménu pro elektronické výkaznictví (ER)</span><span class="sxs-lookup"><span data-stu-id="c3b90-103">Design a domain-specific data model for electronic reporting (ER)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c3b90-104">Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může vytvořit novou konfiguraci pro elektronické výkaznictví, která obsahuje model dat pro elektronické platební doklady.</span><span class="sxs-lookup"><span data-stu-id="c3b90-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="c3b90-105">Tento datový model se použije později jako zdroj dat při vytvoření formátu pro platební doklady.</span><span class="sxs-lookup"><span data-stu-id="c3b90-105">This data model will later be used as a data source when you create the format of the payment documents.</span></span>



<span data-ttu-id="c3b90-106">V tomto příkladu vytvoříte konfiguraci pro vzorovou společnost Litware, Inc. Tyto kroky lze provést v kterékoli společnosti, protože konfigurace ER se sdílí mezi společnostmi.</span><span class="sxs-lookup"><span data-stu-id="c3b90-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="c3b90-107">K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v postupu "Vytvoření poskytovatele konfigurace a jeho označení jako aktivního".</span><span class="sxs-lookup"><span data-stu-id="c3b90-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>

1. <span data-ttu-id="c3b90-108">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="c3b90-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="c3b90-109">Vyberte poskytovatele konfigurace pro vzorovou společnost Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="c3b90-109">Select the configuration provider for sample company, ‘Litware, Inc.’</span></span> <span data-ttu-id="c3b90-110">Pokud tohoto zprostředkovatele konfigurace nevidíte, musíte nejprve dokončit jednotlivé kroky v postupu "Vytvoření poskytovatele konfigurace a jeho označení jako aktivního".</span><span class="sxs-lookup"><span data-stu-id="c3b90-110">If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
2. <span data-ttu-id="c3b90-111">Klikněte na Konfigurace výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="c3b90-111">Click Reporting configurations.</span></span>
    * <span data-ttu-id="c3b90-112">Vytvoříte konfiguraci, která obsahuje model dat pro elektronické platební doklady.</span><span class="sxs-lookup"><span data-stu-id="c3b90-112">You will create a configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="c3b90-113">Tento datový model se použije později jako zdroj dat při vytvoření formátu pro platební doklady.</span><span class="sxs-lookup"><span data-stu-id="c3b90-113">This data model will be used later as a data source when you create the format for the payment documents.</span></span>  

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="c3b90-114">Vytvoření nové konfigurace datového modelu</span><span class="sxs-lookup"><span data-stu-id="c3b90-114">Create a new data model configuration</span></span>
1. <span data-ttu-id="c3b90-115">Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="c3b90-115">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="c3b90-116">V poli Název zadejte Platby (zjednodušený model).</span><span class="sxs-lookup"><span data-stu-id="c3b90-116">In the Name field, type 'Payments (simplified model)'.</span></span>
    * <span data-ttu-id="c3b90-117">Platby (zjednodušený model)</span><span class="sxs-lookup"><span data-stu-id="c3b90-117">Payments (simplified model)</span></span>  
3. <span data-ttu-id="c3b90-118">V poli Popis zadejte „Konfigurace modelu platby“.</span><span class="sxs-lookup"><span data-stu-id="c3b90-118">In the Description field, type 'Payment model configuration'.</span></span>
    * <span data-ttu-id="c3b90-119">Konfigurace modelu platby</span><span class="sxs-lookup"><span data-stu-id="c3b90-119">Payment model configuration</span></span>  
    * <span data-ttu-id="c3b90-120">Aktivní poskytovatel konfigurace se zadá automaticky v tomto poli.</span><span class="sxs-lookup"><span data-stu-id="c3b90-120">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="c3b90-121">Tento zprostředkovatel bude moci udržovat tuto konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="c3b90-121">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="c3b90-122">Jiní poskytovatelé mohou použít tuto konfiguraci, ale nebudou moci ji spravovat.</span><span class="sxs-lookup"><span data-stu-id="c3b90-122">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
4. <span data-ttu-id="c3b90-123">Klepnutím na tlačítko Dokončit konfiguraci dokončíte vytvoření konfigurace</span><span class="sxs-lookup"><span data-stu-id="c3b90-123">Click ‘Create configuration’ button to complete the configuration creation task</span></span>

## <a name="create-a-data-model"></a><span data-ttu-id="c3b90-124">Vytvoření datového modelu</span><span class="sxs-lookup"><span data-stu-id="c3b90-124">Create a data model</span></span>
    * <span data-ttu-id="c3b90-125">Vytváříte nový datový model pro vybranou konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="c3b90-125">You're creating a new data model for the selected configuration.</span></span> <span data-ttu-id="c3b90-126">Tato verze konfigurace bude mít stav Koncept.</span><span class="sxs-lookup"><span data-stu-id="c3b90-126">This configuration version will have a status of Draft.</span></span>  
1. <span data-ttu-id="c3b90-127">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="c3b90-127">Click Designer.</span></span>

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a><span data-ttu-id="c3b90-128">Definování struktury strany účastnící se v platebním procesu</span><span class="sxs-lookup"><span data-stu-id="c3b90-128">Define the structure of a party participating in a payment process</span></span>
1. <span data-ttu-id="c3b90-129">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="c3b90-129">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="c3b90-130">Do pole Název zadejte 'Strana'.</span><span class="sxs-lookup"><span data-stu-id="c3b90-130">In the Name field, type 'Party'.</span></span>
    * <span data-ttu-id="c3b90-131">Strana</span><span class="sxs-lookup"><span data-stu-id="c3b90-131">Party</span></span>  
3. <span data-ttu-id="c3b90-132">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="c3b90-132">Click Add.</span></span>
4. <span data-ttu-id="c3b90-133">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="c3b90-133">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="c3b90-134">Do pole Název zadejte název.</span><span class="sxs-lookup"><span data-stu-id="c3b90-134">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="c3b90-135">Jméno</span><span class="sxs-lookup"><span data-stu-id="c3b90-135">Name</span></span>  
6. <span data-ttu-id="c3b90-136">V poli Typ položky vyberte Řetězec.</span><span class="sxs-lookup"><span data-stu-id="c3b90-136">In the Item type field, select 'String'.</span></span>
7. <span data-ttu-id="c3b90-137">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="c3b90-137">Click Add.</span></span>
8. <span data-ttu-id="c3b90-138">Do pole Najít zadejte 'Strana'.</span><span class="sxs-lookup"><span data-stu-id="c3b90-138">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="c3b90-139">Strana</span><span class="sxs-lookup"><span data-stu-id="c3b90-139">Party</span></span>  
9. <span data-ttu-id="c3b90-140">Klikněte na Vyhledat předchozí.</span><span class="sxs-lookup"><span data-stu-id="c3b90-140">Click Find previous.</span></span>

## <a name="define-the-bank-structure-for-this-model"></a><span data-ttu-id="c3b90-141">Definování struktury banky pro tento model</span><span class="sxs-lookup"><span data-stu-id="c3b90-141">Define the bank structure for this model</span></span>
1. <span data-ttu-id="c3b90-142">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="c3b90-142">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="c3b90-143">Do pole Název zadejte hodnotu Agent.</span><span class="sxs-lookup"><span data-stu-id="c3b90-143">In the Name field, type 'Agent'.</span></span>
    * <span data-ttu-id="c3b90-144">Zástupce</span><span class="sxs-lookup"><span data-stu-id="c3b90-144">Agent</span></span>  
3. <span data-ttu-id="c3b90-145">V poli Typ položky vyberte Záznam.</span><span class="sxs-lookup"><span data-stu-id="c3b90-145">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="c3b90-146">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="c3b90-146">Click Add.</span></span>
5. <span data-ttu-id="c3b90-147">V poli Popis zadejte 'Finanční instituce (například banka) obsluhující účet pro stranu (dlužník/věřitel).'.</span><span class="sxs-lookup"><span data-stu-id="c3b90-147">In the Description field, enter 'Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).'.</span></span>
    * <span data-ttu-id="c3b90-148">Finanční instituce (například banka) obsluhující účet pro stranu (dlužníka/věřitele).</span><span class="sxs-lookup"><span data-stu-id="c3b90-148">Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).</span></span>  
6. <span data-ttu-id="c3b90-149">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="c3b90-149">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="c3b90-150">Do pole Název zadejte název.</span><span class="sxs-lookup"><span data-stu-id="c3b90-150">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="c3b90-151">Jméno</span><span class="sxs-lookup"><span data-stu-id="c3b90-151">Name</span></span>  
8. <span data-ttu-id="c3b90-152">V poli Typ položky vyberte Řetězec.</span><span class="sxs-lookup"><span data-stu-id="c3b90-152">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="c3b90-153">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="c3b90-153">Click Add.</span></span>
10. <span data-ttu-id="c3b90-154">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="c3b90-154">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="c3b90-155">Do pole Název zadejte SWIFT.</span><span class="sxs-lookup"><span data-stu-id="c3b90-155">In the Name field, type 'SWIFT'.</span></span>
    * <span data-ttu-id="c3b90-156">SWIFT</span><span class="sxs-lookup"><span data-stu-id="c3b90-156">SWIFT</span></span>  
12. <span data-ttu-id="c3b90-157">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="c3b90-157">Click Add.</span></span>
13. <span data-ttu-id="c3b90-158">Do pole Popis zadejte Identifikační kód banky.</span><span class="sxs-lookup"><span data-stu-id="c3b90-158">In the Description field, enter 'Bank identification code'.</span></span>
    * <span data-ttu-id="c3b90-159">Identifikační kód banky</span><span class="sxs-lookup"><span data-stu-id="c3b90-159">Bank identification code</span></span>  
14. <span data-ttu-id="c3b90-160">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="c3b90-160">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="c3b90-161">Do pole Název zadejte „RoutingNumber“.</span><span class="sxs-lookup"><span data-stu-id="c3b90-161">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="c3b90-162">Směrový kód</span><span class="sxs-lookup"><span data-stu-id="c3b90-162">RoutingNumber</span></span>  
16. <span data-ttu-id="c3b90-163">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="c3b90-163">Click Add.</span></span>
17. <span data-ttu-id="c3b90-164">Do pole Popis zadejte 'Směrový kód'.</span><span class="sxs-lookup"><span data-stu-id="c3b90-164">In the Description field, enter 'Routing number'.</span></span>
    * <span data-ttu-id="c3b90-165">Směrový kód banky</span><span class="sxs-lookup"><span data-stu-id="c3b90-165">Routing number</span></span>  
18. <span data-ttu-id="c3b90-166">Klikněte na Vyhledat předchozí.</span><span class="sxs-lookup"><span data-stu-id="c3b90-166">Click Find previous.</span></span>

## <a name="define-the-bank-account-structure-for-this-model"></a><span data-ttu-id="c3b90-167">Definování struktury bankovního účtu pro tento model</span><span class="sxs-lookup"><span data-stu-id="c3b90-167">Define the bank account structure for this model</span></span>
1. <span data-ttu-id="c3b90-168">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="c3b90-168">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="c3b90-169">Do pole Název zadejte Účet.</span><span class="sxs-lookup"><span data-stu-id="c3b90-169">In the Name field, type 'Account'.</span></span>
    * <span data-ttu-id="c3b90-170">Účet</span><span class="sxs-lookup"><span data-stu-id="c3b90-170">Account</span></span>  
3. <span data-ttu-id="c3b90-171">V poli Typ položky vyberte Záznam.</span><span class="sxs-lookup"><span data-stu-id="c3b90-171">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="c3b90-172">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="c3b90-172">Click Add.</span></span>
5. <span data-ttu-id="c3b90-173">Do pole Popis zadejte 'Identifikace účtu strany ve finanční instituci (například bance).'.</span><span class="sxs-lookup"><span data-stu-id="c3b90-173">In the Description field, enter 'Identification of an account of a party in a financial institution (for instance, a bank).'.</span></span>
    * <span data-ttu-id="c3b90-174">Identifikace účtu strany ve finanční instituci (například bance).</span><span class="sxs-lookup"><span data-stu-id="c3b90-174">Identification of an account of a party in a financial institution (for instance, a bank).</span></span>  
6. <span data-ttu-id="c3b90-175">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="c3b90-175">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="c3b90-176">Do pole Název zadejte Měna.</span><span class="sxs-lookup"><span data-stu-id="c3b90-176">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="c3b90-177">Měna</span><span class="sxs-lookup"><span data-stu-id="c3b90-177">Currency</span></span>  
8. <span data-ttu-id="c3b90-178">V poli Typ položky vyberte Řetězec.</span><span class="sxs-lookup"><span data-stu-id="c3b90-178">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="c3b90-179">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="c3b90-179">Click Add.</span></span>
10. <span data-ttu-id="c3b90-180">Do pole Popis zadejte Kód měny.</span><span class="sxs-lookup"><span data-stu-id="c3b90-180">In the Description field, enter 'Currency code'.</span></span>
    * <span data-ttu-id="c3b90-181">Kód měny</span><span class="sxs-lookup"><span data-stu-id="c3b90-181">Currency code</span></span>  
11. <span data-ttu-id="c3b90-182">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="c3b90-182">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="c3b90-183">Do pole Název zadejte Číslo.</span><span class="sxs-lookup"><span data-stu-id="c3b90-183">In the Name field, type 'Number'.</span></span>
    * <span data-ttu-id="c3b90-184">Počet</span><span class="sxs-lookup"><span data-stu-id="c3b90-184">Number</span></span>  
13. <span data-ttu-id="c3b90-185">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="c3b90-185">Click Add.</span></span>
14. <span data-ttu-id="c3b90-186">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="c3b90-186">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="c3b90-187">Do pole Název zadejte IBAN.</span><span class="sxs-lookup"><span data-stu-id="c3b90-187">In the Name field, type 'IBAN'.</span></span>
    * <span data-ttu-id="c3b90-188">KÓD IBAN</span><span class="sxs-lookup"><span data-stu-id="c3b90-188">IBAN</span></span>  
16. <span data-ttu-id="c3b90-189">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="c3b90-189">Click Add.</span></span>
17. <span data-ttu-id="c3b90-190">Do pole Popis zadejte 'Číslo IBAN (International Bank Account Number)'.</span><span class="sxs-lookup"><span data-stu-id="c3b90-190">In the Description field, enter 'International bank account number'.</span></span>
    * <span data-ttu-id="c3b90-191">Číslo IBAN (International Bank Account Number)</span><span class="sxs-lookup"><span data-stu-id="c3b90-191">International bank account number</span></span>  

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a><span data-ttu-id="c3b90-192">Definování struktury platební zprávy pro platby typu převod kreditu</span><span class="sxs-lookup"><span data-stu-id="c3b90-192">Define the payment message structure for credit transfer payment type</span></span>
1. <span data-ttu-id="c3b90-193">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="c3b90-193">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="c3b90-194">Do pole Nový uzel zadejte Kořen modelu.</span><span class="sxs-lookup"><span data-stu-id="c3b90-194">In the New node as a field, enter 'Model root'.</span></span>
3. <span data-ttu-id="c3b90-195">Zadejte hodnotu CustomerCreditTransferInitiation do pole Název.</span><span class="sxs-lookup"><span data-stu-id="c3b90-195">In the Name field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="c3b90-196">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="c3b90-196">CustomerCreditTransferInitiation</span></span>  
4. <span data-ttu-id="c3b90-197">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="c3b90-197">Click Add.</span></span>
5. <span data-ttu-id="c3b90-198">Do pole Najít zadejte hodnotu 'CustomerCreditTransferInitiation'.</span><span class="sxs-lookup"><span data-stu-id="c3b90-198">In the Find field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="c3b90-199">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="c3b90-199">CustomerCreditTransferInitiation</span></span>  
6. <span data-ttu-id="c3b90-200">Klikněte na Vyhledat předchozí.</span><span class="sxs-lookup"><span data-stu-id="c3b90-200">Click Find previous.</span></span>
7. <span data-ttu-id="c3b90-201">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="c3b90-201">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="c3b90-202">Do pole Název zadejte „MessageIdentification“.</span><span class="sxs-lookup"><span data-stu-id="c3b90-202">In the Name field, type 'MessageIdentification'.</span></span>
    * <span data-ttu-id="c3b90-203">MessageIdentification</span><span class="sxs-lookup"><span data-stu-id="c3b90-203">MessageIdentification</span></span>  
9. <span data-ttu-id="c3b90-204">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="c3b90-204">Click Add.</span></span>
10. <span data-ttu-id="c3b90-205">V poli Popis zadejte Odkaz Point to Point tak, jak byl přiřazen přikazující straně a odeslán další straně k identifikaci zprávy.</span><span class="sxs-lookup"><span data-stu-id="c3b90-205">In the Description field, enter 'The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.'.</span></span>
    * <span data-ttu-id="c3b90-206">Odkaz Point to Point tak, jak byl přiřazen přikazující straně a odeslán další straně k identifikaci zprávy.</span><span class="sxs-lookup"><span data-stu-id="c3b90-206">The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.</span></span>  
11. <span data-ttu-id="c3b90-207">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="c3b90-207">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="c3b90-208">Do pole Název zadejte „ProcessingDateTime“.</span><span class="sxs-lookup"><span data-stu-id="c3b90-208">In the Name field, type 'ProcessingDateTime'.</span></span>
    * <span data-ttu-id="c3b90-209">ProcessingDateTime</span><span class="sxs-lookup"><span data-stu-id="c3b90-209">ProcessingDateTime</span></span>  
13. <span data-ttu-id="c3b90-210">V poli Typ položky vyberte Datum a čas.</span><span class="sxs-lookup"><span data-stu-id="c3b90-210">In the Item type field, select 'DateTime'.</span></span>
14. <span data-ttu-id="c3b90-211">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="c3b90-211">Click Add.</span></span>
15. <span data-ttu-id="c3b90-212">Do pole Popis zadejte 'Datum a čas, kdy byla platební zpráva vytvořena.'.</span><span class="sxs-lookup"><span data-stu-id="c3b90-212">In the Description field, enter 'Date and time at which the payment message was created.'.</span></span>
    * <span data-ttu-id="c3b90-213">Datum a čas, kdy byla platební zpráva vytvořena.</span><span class="sxs-lookup"><span data-stu-id="c3b90-213">Date and time at which the payment message was created.</span></span>  
16. <span data-ttu-id="c3b90-214">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="c3b90-214">Click New to open the drop dialog.</span></span>
    * <span data-ttu-id="c3b90-215">Definování struktury platební transakce pro tento model.</span><span class="sxs-lookup"><span data-stu-id="c3b90-215">Define the payment transaction structure for this model.</span></span>  
17. <span data-ttu-id="c3b90-216">Do pole Název zadejte Platby.</span><span class="sxs-lookup"><span data-stu-id="c3b90-216">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="c3b90-217">Platby</span><span class="sxs-lookup"><span data-stu-id="c3b90-217">Payments</span></span>  
18. <span data-ttu-id="c3b90-218">V poli Typ položky vyberte Seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="c3b90-218">In the Item type field, select 'Record list'.</span></span>
19. <span data-ttu-id="c3b90-219">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="c3b90-219">Click Add.</span></span>
20. <span data-ttu-id="c3b90-220">Do pole Popis zadejte Řádky platby pro aktuální zprávu.</span><span class="sxs-lookup"><span data-stu-id="c3b90-220">In the Description field, enter 'Payment lines of the current message'.</span></span>
    * <span data-ttu-id="c3b90-221">Řádky platby pro aktuální zprávu</span><span class="sxs-lookup"><span data-stu-id="c3b90-221">Payment lines of the current message</span></span>  
21. <span data-ttu-id="c3b90-222">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="c3b90-222">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="c3b90-223">Do pole Název zadejte Věřitel.</span><span class="sxs-lookup"><span data-stu-id="c3b90-223">In the Name field, type 'Creditor'.</span></span>
    * <span data-ttu-id="c3b90-224">Věřitel</span><span class="sxs-lookup"><span data-stu-id="c3b90-224">Creditor</span></span>  
23. <span data-ttu-id="c3b90-225">V poli Typ položky vyberte Záznam.</span><span class="sxs-lookup"><span data-stu-id="c3b90-225">In the Item type field, select 'Record'.</span></span>
24. <span data-ttu-id="c3b90-226">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="c3b90-226">Click Add.</span></span>
25. <span data-ttu-id="c3b90-227">V poli Popis zadejte Strana, pro kterou je peněžní částka splatná.</span><span class="sxs-lookup"><span data-stu-id="c3b90-227">In the Description field, enter 'Party to which an amount of money is due.'.</span></span>
    * <span data-ttu-id="c3b90-228">Strana, pro kterou je peněžní částka splatná.</span><span class="sxs-lookup"><span data-stu-id="c3b90-228">Party to which an amount of money is due.</span></span>  
26. <span data-ttu-id="c3b90-229">Klikněte na možnost Přepnout odkaz položky.</span><span class="sxs-lookup"><span data-stu-id="c3b90-229">Click Switch item reference.</span></span>
27. <span data-ttu-id="c3b90-230">Do pole Najít zadejte 'Strana'.</span><span class="sxs-lookup"><span data-stu-id="c3b90-230">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="c3b90-231">Strana</span><span class="sxs-lookup"><span data-stu-id="c3b90-231">Party</span></span>  
28. <span data-ttu-id="c3b90-232">Klikněte na Najít další.</span><span class="sxs-lookup"><span data-stu-id="c3b90-232">Click Find next.</span></span>
29. <span data-ttu-id="c3b90-233">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c3b90-233">Click OK.</span></span>
30. <span data-ttu-id="c3b90-234">Do pole Najít zadejte 'Platby'.</span><span class="sxs-lookup"><span data-stu-id="c3b90-234">In the Find field, type 'Payments'.</span></span>
    * <span data-ttu-id="c3b90-235">Platby</span><span class="sxs-lookup"><span data-stu-id="c3b90-235">Payments</span></span>  
31. <span data-ttu-id="c3b90-236">Klikněte na Najít další.</span><span class="sxs-lookup"><span data-stu-id="c3b90-236">Click Find next.</span></span>
32. <span data-ttu-id="c3b90-237">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="c3b90-237">Click New to open the drop dialog.</span></span>
33. <span data-ttu-id="c3b90-238">Do pole Název zadejte Dlužník.</span><span class="sxs-lookup"><span data-stu-id="c3b90-238">In the Name field, type 'Debtor'.</span></span>
    * <span data-ttu-id="c3b90-239">Dlužník</span><span class="sxs-lookup"><span data-stu-id="c3b90-239">Debtor</span></span>  
34. <span data-ttu-id="c3b90-240">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="c3b90-240">Click Add.</span></span>
35. <span data-ttu-id="c3b90-241">V poli Popis zadejte Strana vlastnící finanční částku pro (konečného) věřitele.</span><span class="sxs-lookup"><span data-stu-id="c3b90-241">In the Description field, enter 'Party that owes an amount of money to the (ultimate) creditor.'.</span></span>
    * <span data-ttu-id="c3b90-242">Strana vlastnící finanční částku pro (konečného) věřitele.</span><span class="sxs-lookup"><span data-stu-id="c3b90-242">Party that owes an amount of money to the (ultimate) creditor.</span></span>  
36. <span data-ttu-id="c3b90-243">Klikněte na možnost Přepnout odkaz položky.</span><span class="sxs-lookup"><span data-stu-id="c3b90-243">Click Switch item reference.</span></span>
37. <span data-ttu-id="c3b90-244">Do pole Najít zadejte 'Strana'.</span><span class="sxs-lookup"><span data-stu-id="c3b90-244">In the Find field, type 'Party'.</span></span>
    * <span data-ttu-id="c3b90-245">Strana</span><span class="sxs-lookup"><span data-stu-id="c3b90-245">Party</span></span>  
38. <span data-ttu-id="c3b90-246">Klikněte na Najít další.</span><span class="sxs-lookup"><span data-stu-id="c3b90-246">Click Find next.</span></span>
39. <span data-ttu-id="c3b90-247">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="c3b90-247">Click OK.</span></span>
40. <span data-ttu-id="c3b90-248">Klikněte na Najít další.</span><span class="sxs-lookup"><span data-stu-id="c3b90-248">Click Find next.</span></span>
41. <span data-ttu-id="c3b90-249">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="c3b90-249">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="c3b90-250">Do pole Název zadejte Popis.</span><span class="sxs-lookup"><span data-stu-id="c3b90-250">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="c3b90-251">popis</span><span class="sxs-lookup"><span data-stu-id="c3b90-251">Description</span></span>  
43. <span data-ttu-id="c3b90-252">V poli Typ položky vyberte Řetězec.</span><span class="sxs-lookup"><span data-stu-id="c3b90-252">In the Item type field, select 'String'.</span></span>
44. <span data-ttu-id="c3b90-253">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="c3b90-253">Click Add.</span></span>
45. <span data-ttu-id="c3b90-254">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="c3b90-254">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="c3b90-255">Do pole Název zadejte Měna.</span><span class="sxs-lookup"><span data-stu-id="c3b90-255">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="c3b90-256">Měna</span><span class="sxs-lookup"><span data-stu-id="c3b90-256">Currency</span></span>  
47. <span data-ttu-id="c3b90-257">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="c3b90-257">Click Add.</span></span>
48. <span data-ttu-id="c3b90-258">Do pole Popis zadejte Kód měny.</span><span class="sxs-lookup"><span data-stu-id="c3b90-258">In the Description field, enter 'Currency code'.</span></span>
    * <span data-ttu-id="c3b90-259">Kód měny</span><span class="sxs-lookup"><span data-stu-id="c3b90-259">Currency code</span></span>  
49. <span data-ttu-id="c3b90-260">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="c3b90-260">Click New to open the drop dialog.</span></span>
50. <span data-ttu-id="c3b90-261">Do pole Název zadejte Datum transakce.</span><span class="sxs-lookup"><span data-stu-id="c3b90-261">In the Name field, type 'TransactionDate'.</span></span>
    * <span data-ttu-id="c3b90-262">Datum transakce</span><span class="sxs-lookup"><span data-stu-id="c3b90-262">TransactionDate</span></span>  
51. <span data-ttu-id="c3b90-263">V poli Typ položky vyberte Datum.</span><span class="sxs-lookup"><span data-stu-id="c3b90-263">In the Item type field, select 'Date'.</span></span>
52. <span data-ttu-id="c3b90-264">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="c3b90-264">Click Add.</span></span>
53. <span data-ttu-id="c3b90-265">Do pole Popis zadejte 'Datum transakce'.</span><span class="sxs-lookup"><span data-stu-id="c3b90-265">In the Description field, enter 'Transaction date'.</span></span>
    * <span data-ttu-id="c3b90-266">Datum transakce</span><span class="sxs-lookup"><span data-stu-id="c3b90-266">Transaction date</span></span>  
54. <span data-ttu-id="c3b90-267">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="c3b90-267">Click New to open the drop dialog.</span></span>
55. <span data-ttu-id="c3b90-268">Do pole Název zadejte Požadovaná částka.</span><span class="sxs-lookup"><span data-stu-id="c3b90-268">In the Name field, type 'InstructedAmount'.</span></span>
    * <span data-ttu-id="c3b90-269">Požadovaná částka</span><span class="sxs-lookup"><span data-stu-id="c3b90-269">InstructedAmount</span></span>  
56. <span data-ttu-id="c3b90-270">V poli Typ položky vyberte Reálný.</span><span class="sxs-lookup"><span data-stu-id="c3b90-270">In the Item type field, select 'Real'.</span></span>
57. <span data-ttu-id="c3b90-271">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="c3b90-271">Click Add.</span></span>
58. <span data-ttu-id="c3b90-272">V poli Popis uveďte Peněžní částka, která má být přesunuta mezi dlužníkem a věřitelem před odečtením poplatků.</span><span class="sxs-lookup"><span data-stu-id="c3b90-272">In the Description field, enter 'The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="c3b90-273">Částka by měla být vyjádřená v měně podle objednávky strany příkazce.</span><span class="sxs-lookup"><span data-stu-id="c3b90-273">The amount should be expressed in the currency as ordered by the initiating party.'.</span></span>
    * <span data-ttu-id="c3b90-274">Peněžní částka, která má být přesunuta mezi dlužníkem a věřitelem před odečtením poplatků.</span><span class="sxs-lookup"><span data-stu-id="c3b90-274">The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="c3b90-275">Částka by měla být vyjádřená v měně podle objednávky strany příkazce.</span><span class="sxs-lookup"><span data-stu-id="c3b90-275">The amount should be expressed in the currency as ordered by the initiating party.</span></span>  
59. <span data-ttu-id="c3b90-276">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="c3b90-276">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="c3b90-277">Zadejte text „End2EndID“ do pole Název.</span><span class="sxs-lookup"><span data-stu-id="c3b90-277">In the Name field, type 'End2EndID'.</span></span>
    * <span data-ttu-id="c3b90-278">End2EndID</span><span class="sxs-lookup"><span data-stu-id="c3b90-278">End2EndID</span></span>  
61. <span data-ttu-id="c3b90-279">V poli Typ položky vyberte Řetězec.</span><span class="sxs-lookup"><span data-stu-id="c3b90-279">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="c3b90-280">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="c3b90-280">Click Add.</span></span>
63. <span data-ttu-id="c3b90-281">Do pole Popis zadejte hodnotu 'Jedinečná identifikace přiřazena stranou příkazce'.</span><span class="sxs-lookup"><span data-stu-id="c3b90-281">In the Description field, enter 'The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="c3b90-282">Tato identifikace se přenáší beze změny v průběhu celého řetězce od začátku do konce.</span><span class="sxs-lookup"><span data-stu-id="c3b90-282">This identification is passed on, unchanged, throughout the entire end-to-end chain.'.</span></span>
    * <span data-ttu-id="c3b90-283">Jedinečná identifikace přiřazena stranou příkazce.</span><span class="sxs-lookup"><span data-stu-id="c3b90-283">The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="c3b90-284">Tato identifikace se přenáší beze změny v průběhu celého řetězce od začátku do konce.</span><span class="sxs-lookup"><span data-stu-id="c3b90-284">This identification is passed on, unchanged, throughout the entire end-to-end chain.</span></span>  
64. <span data-ttu-id="c3b90-285">Zadejte PaymentModel do pole Název.</span><span class="sxs-lookup"><span data-stu-id="c3b90-285">In the Name field, type 'PaymentModel'.</span></span>
    * <span data-ttu-id="c3b90-286">Název PaymentModel vychází z předdefinovaných rozhraní formulářů plateb.</span><span class="sxs-lookup"><span data-stu-id="c3b90-286">The PaymentModel name aligns with predefined interfaces of payment forms.</span></span>  
65. <span data-ttu-id="c3b90-287">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="c3b90-287">Click Save.</span></span>
66. <span data-ttu-id="c3b90-288">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="c3b90-288">Close the page.</span></span>


