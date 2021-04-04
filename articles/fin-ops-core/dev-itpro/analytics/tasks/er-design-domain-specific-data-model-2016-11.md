---
title: Elektronické vykazování – návrh datového modelu pro určitou doménu
description: Toto téma popisuje, jak vytvořit novou konfiguraci elektronického výkaznictví (ER), která obsahuje datový model pro dokumenty elektronických plateb.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERDataContainerDescriptorReferenceSwitchDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 284fad8b6646c35217789cc9936cbe9fe75a03d0
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567801"
---
# <a name="er-design-domain-specific-data-model"></a><span data-ttu-id="9a3c2-103">Elektronické vykazování – návrh datového modelu pro určitou doménu</span><span class="sxs-lookup"><span data-stu-id="9a3c2-103">ER Design domain specific data model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9a3c2-104">Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může vytvořit novou konfiguraci pro elektronické výkaznictví, která obsahuje model dat pro elektronické platební doklady.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="9a3c2-105">Tento datový model se použije později jako zdroj dat při vytvoření formátu pro platební doklady.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-105">This data model will later be used as a data source when you create the format of the payment documents.</span></span>

<span data-ttu-id="9a3c2-106">V tomto příkladu vytvoříte konfiguraci pro vzorovou společnost Litware, Inc. Tyto kroky lze provést v kterékoli společnosti, protože konfigurace ER se sdílí mezi společnostmi.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in any company as ER configurations are shared among companies.</span></span> <span data-ttu-id="9a3c2-107">K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v proceduře "Vytvoření poskytovatele konfigurace a jeho označení jako aktivního".</span><span class="sxs-lookup"><span data-stu-id="9a3c2-107">To complete these steps, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>

1. <span data-ttu-id="9a3c2-108">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>

    <span data-ttu-id="9a3c2-109">Vyberte poskytovatele konfigurace pro vzorovou společnost 'Litware, Inc'.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-109">Select the configuration provider for sample company, 'Litware, Inc.'</span></span> <span data-ttu-id="9a3c2-110">Pokud tohoto zprostředkovatele konfigurace nevidíte, musíte nejprve dokončit jednotlivé kroky v postupu „Vytvoření poskytovatele konfigurace a jeho označení jako aktivního“.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-110">If you don't see this configuration provider, you must first complete the steps in the "Create a configuration provider and mark it as active" procedure.</span></span>  
    
2. <span data-ttu-id="9a3c2-111">Klikněte na Konfigurace výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-111">Click Reporting configurations.</span></span>

    <span data-ttu-id="9a3c2-112">Vytvoříte konfiguraci, která obsahuje model dat pro elektronické platební doklady.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-112">You will create a configuration that contains a data model for electronic payment documents.</span></span> <span data-ttu-id="9a3c2-113">Tento datový model se použije později jako zdroj dat při vytvoření formátu pro platební doklady.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-113">This data model will be used later as a data source when you create the format for the payment documents.</span></span>  

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="9a3c2-114">Vytvoření nové konfigurace datového modelu</span><span class="sxs-lookup"><span data-stu-id="9a3c2-114">Create a new data model configuration</span></span>
1. <span data-ttu-id="9a3c2-115">Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-115">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="9a3c2-116">V poli Název zadejte Platby (zjednodušený model).</span><span class="sxs-lookup"><span data-stu-id="9a3c2-116">In the Name field, type 'Payments (simplified model)'.</span></span>
3. <span data-ttu-id="9a3c2-117">V poli Popis zadejte „Konfigurace modelu platby“.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-117">In the Description field, type 'Payment model configuration'.</span></span>

    <span data-ttu-id="9a3c2-118">Aktivní poskytovatel konfigurace se zadá automaticky v tomto poli.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-118">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="9a3c2-119">Tento zprostředkovatel bude moci udržovat tuto konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-119">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="9a3c2-120">Jiní poskytovatelé mohou použít tuto konfiguraci, ale nebudou moci ji spravovat.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-120">Other providers can use this configuration, but will not be able to maintain it.</span></span>  

4. <span data-ttu-id="9a3c2-121">Klepnutím na tlačítko 'Dokončit konfiguraci' dokončíte vytvoření konfigurace</span><span class="sxs-lookup"><span data-stu-id="9a3c2-121">Click 'Create configuration' button to complete the configuration creation task</span></span>

## <a name="create-a-data-model"></a><span data-ttu-id="9a3c2-122">Vytvoření datového modelu</span><span class="sxs-lookup"><span data-stu-id="9a3c2-122">Create a data model</span></span>
<span data-ttu-id="9a3c2-123">Vytváříte nový datový model pro vybranou konfiguraci.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-123">You're creating a new data model for the selected configuration.</span></span> <span data-ttu-id="9a3c2-124">Tato verze konfigurace bude mít stav Koncept.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-124">This configuration version will have a status of Draft.</span></span>  
1. <span data-ttu-id="9a3c2-125">Klikněte na možnost Návrhář.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-125">Click Designer.</span></span>

## <a name="define-the-structure-of-a-party-participating-in-a-payment-process"></a><span data-ttu-id="9a3c2-126">Definování struktury strany účastnící se v platebním procesu</span><span class="sxs-lookup"><span data-stu-id="9a3c2-126">Define the structure of a party participating in a payment process</span></span>
1. <span data-ttu-id="9a3c2-127">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-127">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="9a3c2-128">Do pole Název zadejte 'Strana'.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-128">In the Name field, type 'Party'.</span></span>
3. <span data-ttu-id="9a3c2-129">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-129">Click Add.</span></span>
4. <span data-ttu-id="9a3c2-130">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-130">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="9a3c2-131">Do pole Název zadejte název.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-131">In the Name field, type 'Name'.</span></span>
6. <span data-ttu-id="9a3c2-132">V poli Typ položky vyberte Řetězec.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-132">In the Item type field, select 'String'.</span></span>
7. <span data-ttu-id="9a3c2-133">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-133">Click Add.</span></span>
8. <span data-ttu-id="9a3c2-134">Do pole Najít zadejte 'Strana'.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-134">In the Find field, type 'Party'.</span></span>
9. <span data-ttu-id="9a3c2-135">Klikněte na Vyhledat předchozí.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-135">Click Find previous.</span></span>

## <a name="define-the-bank-structure-for-this-model"></a><span data-ttu-id="9a3c2-136">Definování struktury banky pro tento model</span><span class="sxs-lookup"><span data-stu-id="9a3c2-136">Define the bank structure for this model</span></span>
1. <span data-ttu-id="9a3c2-137">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-137">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="9a3c2-138">Do pole Název zadejte hodnotu Agent.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-138">In the Name field, type 'Agent'.</span></span>
3. <span data-ttu-id="9a3c2-139">V poli Typ položky vyberte Záznam.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-139">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="9a3c2-140">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-140">Click Add.</span></span>
5. <span data-ttu-id="9a3c2-141">V poli Popis zadejte 'Finanční instituce (například banka) obsluhující účet pro stranu (dlužník/věřitel).'.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-141">In the Description field, enter 'Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).'.</span></span>

    <span data-ttu-id="9a3c2-142">Finanční instituce (například banka) obsluhující účet pro stranu (dlužníka/věřitele).</span><span class="sxs-lookup"><span data-stu-id="9a3c2-142">Financial institution (for instance, a bank) servicing an account for the party (debtor/creditor).</span></span>  

6. <span data-ttu-id="9a3c2-143">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-143">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="9a3c2-144">Do pole Název zadejte název.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-144">In the Name field, type 'Name'.</span></span> 
8. <span data-ttu-id="9a3c2-145">V poli Typ položky vyberte Řetězec.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-145">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="9a3c2-146">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-146">Click Add.</span></span>
10. <span data-ttu-id="9a3c2-147">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-147">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="9a3c2-148">Do pole Název zadejte SWIFT.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-148">In the Name field, type 'SWIFT'.</span></span>
12. <span data-ttu-id="9a3c2-149">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-149">Click Add.</span></span>
13. <span data-ttu-id="9a3c2-150">Do pole Popis zadejte Identifikační kód banky.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-150">In the Description field, enter 'Bank identification code'.</span></span> 
14. <span data-ttu-id="9a3c2-151">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-151">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="9a3c2-152">Do pole Název zadejte „RoutingNumber“.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-152">In the Name field, type 'RoutingNumber'.</span></span>
16. <span data-ttu-id="9a3c2-153">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-153">Click Add.</span></span>
17. <span data-ttu-id="9a3c2-154">Do pole Popis zadejte 'Směrový kód'.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-154">In the Description field, enter 'Routing number'.</span></span>
18. <span data-ttu-id="9a3c2-155">Klikněte na Vyhledat předchozí.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-155">Click Find previous.</span></span>

## <a name="define-the-bank-account-structure-for-this-model"></a><span data-ttu-id="9a3c2-156">Definování struktury bankovního účtu pro tento model</span><span class="sxs-lookup"><span data-stu-id="9a3c2-156">Define the bank account structure for this model</span></span>
1. <span data-ttu-id="9a3c2-157">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-157">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="9a3c2-158">Do pole Název zadejte Účet.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-158">In the Name field, type 'Account'.</span></span> 
3. <span data-ttu-id="9a3c2-159">V poli Typ položky vyberte Záznam.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-159">In the Item type field, select 'Record'.</span></span>
4. <span data-ttu-id="9a3c2-160">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-160">Click Add.</span></span>
5. <span data-ttu-id="9a3c2-161">Do pole Popis zadejte 'Identifikace účtu strany ve finanční instituci (například bance).'.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-161">In the Description field, enter 'Identification of an account of a party in a financial institution (for instance, a bank).'.</span></span>

    <span data-ttu-id="9a3c2-162">Identifikace účtu strany ve finanční instituci (například bance).</span><span class="sxs-lookup"><span data-stu-id="9a3c2-162">Identification of an account of a party in a financial institution (for instance, a bank).</span></span>  

6. <span data-ttu-id="9a3c2-163">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-163">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="9a3c2-164">Do pole Název zadejte Měna.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-164">In the Name field, type 'Currency'.</span></span> 
8. <span data-ttu-id="9a3c2-165">V poli Typ položky vyberte Řetězec.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-165">In the Item type field, select 'String'.</span></span>
9. <span data-ttu-id="9a3c2-166">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-166">Click Add.</span></span>
10. <span data-ttu-id="9a3c2-167">Do pole Popis zadejte Kód měny.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-167">In the Description field, enter 'Currency code'.</span></span>
11. <span data-ttu-id="9a3c2-168">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-168">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="9a3c2-169">Do pole Název zadejte Číslo.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-169">In the Name field, type 'Number'.</span></span> 
13. <span data-ttu-id="9a3c2-170">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-170">Click Add.</span></span>
14. <span data-ttu-id="9a3c2-171">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-171">Click New to open the drop dialog.</span></span>
15. <span data-ttu-id="9a3c2-172">Do pole Název zadejte IBAN.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-172">In the Name field, type 'IBAN'.</span></span> 
16. <span data-ttu-id="9a3c2-173">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-173">Click Add.</span></span>
17. <span data-ttu-id="9a3c2-174">Do pole Popis zadejte 'Číslo IBAN (International Bank Account Number)'.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-174">In the Description field, enter 'International bank account number'.</span></span>

## <a name="define-the-payment-message-structure-for-credit-transfer-payment-type"></a><span data-ttu-id="9a3c2-175">Definování struktury platební zprávy pro platby typu převod kreditu</span><span class="sxs-lookup"><span data-stu-id="9a3c2-175">Define the payment message structure for credit transfer payment type</span></span>
1. <span data-ttu-id="9a3c2-176">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-176">Click New to open the drop dialog.</span></span>
2. <span data-ttu-id="9a3c2-177">Do pole Nový uzel zadejte Kořen modelu.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-177">In the New node as a field, enter 'Model root'.</span></span>
3. <span data-ttu-id="9a3c2-178">Zadejte hodnotu CustomerCreditTransferInitiation do pole Název.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-178">In the Name field, type 'CustomerCreditTransferInitiation'.</span></span>
4. <span data-ttu-id="9a3c2-179">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-179">Click Add.</span></span>
5. <span data-ttu-id="9a3c2-180">Do pole Najít zadejte hodnotu 'CustomerCreditTransferInitiation'.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-180">In the Find field, type 'CustomerCreditTransferInitiation'.</span></span> 
6. <span data-ttu-id="9a3c2-181">Klikněte na Vyhledat předchozí.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-181">Click Find previous.</span></span>
7. <span data-ttu-id="9a3c2-182">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-182">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="9a3c2-183">Do pole Název zadejte „MessageIdentification“.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-183">In the Name field, type 'MessageIdentification'.</span></span> 
9. <span data-ttu-id="9a3c2-184">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-184">Click Add.</span></span>
10. <span data-ttu-id="9a3c2-185">V poli Popis zadejte Odkaz Point to Point tak, jak byl přiřazen přikazující straně a odeslán další straně k identifikaci zprávy.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-185">In the Description field, enter 'The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.'.</span></span>

    <span data-ttu-id="9a3c2-186">Odkaz Point to Point tak, jak byl přiřazen přikazující straně a odeslán další straně k identifikaci zprávy.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-186">The point-to-point reference assigned by the instructing party (and sent to the next party) to identify a message.</span></span>  

11. <span data-ttu-id="9a3c2-187">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-187">Click New to open the drop dialog.</span></span>
12. <span data-ttu-id="9a3c2-188">Do pole Název zadejte „ProcessingDateTime“.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-188">In the Name field, type 'ProcessingDateTime'.</span></span>
13. <span data-ttu-id="9a3c2-189">V poli Typ položky vyberte Datum a čas.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-189">In the Item type field, select 'DateTime'.</span></span>
14. <span data-ttu-id="9a3c2-190">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-190">Click Add.</span></span>
15. <span data-ttu-id="9a3c2-191">Do pole Popis zadejte 'Datum a čas, kdy byla platební zpráva vytvořena.'.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-191">In the Description field, enter 'Date and time at which the payment message was created.'.</span></span> 
16. <span data-ttu-id="9a3c2-192">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-192">Click New to open the drop dialog.</span></span>

    <span data-ttu-id="9a3c2-193">Definování struktury platební transakce pro tento model.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-193">Define the payment transaction structure for this model.</span></span>  

17. <span data-ttu-id="9a3c2-194">Do pole Název zadejte Platby.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-194">In the Name field, type 'Payments'.</span></span>
18. <span data-ttu-id="9a3c2-195">V poli Typ položky vyberte Seznam záznamů.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-195">In the Item type field, select 'Record list'.</span></span>
19. <span data-ttu-id="9a3c2-196">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-196">Click Add.</span></span>
20. <span data-ttu-id="9a3c2-197">Do pole Popis zadejte Řádky platby pro aktuální zprávu.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-197">In the Description field, enter 'Payment lines of the current message'.</span></span>
21. <span data-ttu-id="9a3c2-198">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-198">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="9a3c2-199">Do pole Název zadejte Věřitel.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-199">In the Name field, type 'Creditor'.</span></span> 
23. <span data-ttu-id="9a3c2-200">V poli Typ položky vyberte Záznam.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-200">In the Item type field, select 'Record'.</span></span>
24. <span data-ttu-id="9a3c2-201">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-201">Click Add.</span></span>
25. <span data-ttu-id="9a3c2-202">V poli Popis zadejte Strana, pro kterou je peněžní částka splatná.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-202">In the Description field, enter 'Party to which an amount of money is due.'.</span></span> 
26. <span data-ttu-id="9a3c2-203">Klikněte na možnost Přepnout odkaz položky.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-203">Click Switch item reference.</span></span>
27. <span data-ttu-id="9a3c2-204">Do pole Najít zadejte 'Strana'.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-204">In the Find field, type 'Party'.</span></span>
28. <span data-ttu-id="9a3c2-205">Klikněte na Najít další.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-205">Click Find next.</span></span>
29. <span data-ttu-id="9a3c2-206">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-206">Click OK.</span></span>
30. <span data-ttu-id="9a3c2-207">Do pole Najít zadejte 'Platby'.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-207">In the Find field, type 'Payments'.</span></span>
31. <span data-ttu-id="9a3c2-208">Klikněte na Najít další.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-208">Click Find next.</span></span>
32. <span data-ttu-id="9a3c2-209">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-209">Click New to open the drop dialog.</span></span>
33. <span data-ttu-id="9a3c2-210">Do pole Název zadejte Dlužník.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-210">In the Name field, type 'Debtor'.</span></span> 
34. <span data-ttu-id="9a3c2-211">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-211">Click Add.</span></span>
35. <span data-ttu-id="9a3c2-212">V poli Popis zadejte Strana vlastnící finanční částku pro (konečného) věřitele.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-212">In the Description field, enter 'Party that owes an amount of money to the (ultimate) creditor.'.</span></span>
36. <span data-ttu-id="9a3c2-213">Klikněte na možnost Přepnout odkaz položky.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-213">Click Switch item reference.</span></span>
37. <span data-ttu-id="9a3c2-214">Do pole Najít zadejte 'Strana'.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-214">In the Find field, type 'Party'.</span></span>
38. <span data-ttu-id="9a3c2-215">Klikněte na Najít další.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-215">Click Find next.</span></span>
39. <span data-ttu-id="9a3c2-216">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-216">Click OK.</span></span>
40. <span data-ttu-id="9a3c2-217">Klikněte na Najít další.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-217">Click Find next.</span></span>
41. <span data-ttu-id="9a3c2-218">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-218">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="9a3c2-219">Do pole Název zadejte Popis.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-219">In the Name field, type 'Description'.</span></span>
43. <span data-ttu-id="9a3c2-220">V poli Typ položky vyberte Řetězec.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-220">In the Item type field, select 'String'.</span></span>
44. <span data-ttu-id="9a3c2-221">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-221">Click Add.</span></span>
45. <span data-ttu-id="9a3c2-222">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-222">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="9a3c2-223">Do pole Název zadejte Měna.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-223">In the Name field, type 'Currency'.</span></span>
47. <span data-ttu-id="9a3c2-224">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-224">Click Add.</span></span>
48. <span data-ttu-id="9a3c2-225">Do pole Popis zadejte Kód měny.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-225">In the Description field, enter 'Currency code'.</span></span>
49. <span data-ttu-id="9a3c2-226">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-226">Click New to open the drop dialog.</span></span>
50. <span data-ttu-id="9a3c2-227">Do pole Název zadejte Datum transakce.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-227">In the Name field, type 'TransactionDate'.</span></span> 
51. <span data-ttu-id="9a3c2-228">V poli Typ položky vyberte Datum.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-228">In the Item type field, select 'Date'.</span></span>
52. <span data-ttu-id="9a3c2-229">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-229">Click Add.</span></span>
53. <span data-ttu-id="9a3c2-230">Do pole Popis zadejte 'Datum transakce'.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-230">In the Description field, enter 'Transaction date'.</span></span> 
54. <span data-ttu-id="9a3c2-231">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-231">Click New to open the drop dialog.</span></span>
55. <span data-ttu-id="9a3c2-232">Do pole Název zadejte Požadovaná částka.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-232">In the Name field, type 'InstructedAmount'.</span></span>  
56. <span data-ttu-id="9a3c2-233">V poli Typ položky vyberte Reálný.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-233">In the Item type field, select 'Real'.</span></span>
57. <span data-ttu-id="9a3c2-234">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-234">Click Add.</span></span>
58. <span data-ttu-id="9a3c2-235">V poli Popis uveďte Peněžní částka, která má být přesunuta mezi dlužníkem a věřitelem před odečtením poplatků.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-235">In the Description field, enter 'The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="9a3c2-236">Částka by měla být vyjádřená v měně podle objednávky strany příkazce.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-236">The amount should be expressed in the currency as ordered by the initiating party.'.</span></span>

    <span data-ttu-id="9a3c2-237">Peněžní částka, která má být přesunuta mezi dlužníkem a věřitelem před odečtením poplatků.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-237">The amount of money to be moved between the debtor and creditor, before deduction of charges.</span></span> <span data-ttu-id="9a3c2-238">Částka by měla být vyjádřená v měně podle objednávky strany příkazce.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-238">The amount should be expressed in the currency as ordered by the initiating party.</span></span>  

59. <span data-ttu-id="9a3c2-239">Kliknutím na možnost Nový otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-239">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="9a3c2-240">Zadejte text „End2EndID“ do pole Název.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-240">In the Name field, type 'End2EndID'.</span></span> 
61. <span data-ttu-id="9a3c2-241">V poli Typ položky vyberte Řetězec.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-241">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="9a3c2-242">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-242">Click Add.</span></span>
63. <span data-ttu-id="9a3c2-243">Do pole Popis zadejte hodnotu 'Jedinečná identifikace přiřazena stranou příkazce'.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-243">In the Description field, enter 'The unique identification assigned by the initiating party.</span></span> <span data-ttu-id="9a3c2-244">Tato identifikace se přenáší beze změny v průběhu celého řetězce od začátku do konce.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-244">This identification is passed on, unchanged, throughout the entire end-to-end chain.'.</span></span> 
64. <span data-ttu-id="9a3c2-245">Zadejte PaymentModel do pole Název.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-245">In the Name field, type 'PaymentModel'.</span></span>

    <span data-ttu-id="9a3c2-246">Název PaymentModel vychází z předdefinovaných rozhraní formulářů plateb.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-246">The PaymentModel name aligns with predefined interfaces of payment forms.</span></span>  

65. <span data-ttu-id="9a3c2-247">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-247">Click Save.</span></span>
66. <span data-ttu-id="9a3c2-248">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="9a3c2-248">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]