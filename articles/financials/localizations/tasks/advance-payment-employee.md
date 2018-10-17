--- 
title: "EEU 00047 Záloha pro zaměstnance"
description: "Tato procedura ukazuje, jak lze nastavit a registrovat transakce pro držitele zálohy."
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RCashTable, LedgerJournalSetup, HcmWorkerGroup_RU, EmplPosting_RU, VendParameters, RCashPosting, BankParameters, PaymTerm, HcmWorker, HcmWorkerNewWorker, HcmWorkerAdvHolderTableListPage_RU, HcmWorkerAdvHolderTable_RU, PurchTable, PurchCreateOrder, HcmAdvHolderLookup_RU, InventItemIdLookupPurchase, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog, EmplTrans_RU, EmplBalance_RU
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: e3c07789bfa0839436caf32e428f3abeecb8f2b7
ms.contentlocale: cs-cz
ms.lasthandoff: 09/14/2018

---
# <a name="eeu-00047-advance-payment-to-employee"></a><span data-ttu-id="1d9fb-103">EEU 00047 Záloha pro zaměstnance</span><span class="sxs-lookup"><span data-stu-id="1d9fb-103">EEU-00047 Advance payment to employee</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1d9fb-104">Tato procedura ukazuje, jak lze nastavit a registrovat transakce pro držitele zálohy.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-104">This procedure demonstrates how to set up and register transactions for an advance holder.</span></span> <span data-ttu-id="1d9fb-105">Procedura byla vytvořena za použití ukázkových dat společnosti DEMF s primární adresou právnické osoby v Litvě.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-105">This procedure was created using the demo data company DEMF with a primary address in Lithuania.</span></span> <span data-ttu-id="1d9fb-106">Tento úkol lze použít pouze pro právnické osoby s primární adresu v Polsku, Litvě, Lotyšsku, Estonsku, České republice nebo Maďarsku.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-106">This task only works for legal entities with a primary address in Poland, Lithuania, Latvia, Estonia, Czech Republic, or Hungary.</span></span> <span data-ttu-id="1d9fb-107">Tato procedura je určena pro funkci, která byla přidána do aplikace Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-new-cash-account"></a><span data-ttu-id="1d9fb-108">Vytvoření nového bankovního účtu</span><span class="sxs-lookup"><span data-stu-id="1d9fb-108">Create a new cash account</span></span>
1. <span data-ttu-id="1d9fb-109">Přejděte do nabídky Pokladna a banka > Bankovní účty > Pokladní účty.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-109">Go to Cash and bank management > Bank accounts > Cash accounts.</span></span>
2. <span data-ttu-id="1d9fb-110">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-110">Click New.</span></span>
3. <span data-ttu-id="1d9fb-111">Zadejte hodnotu do pole Hotovost.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-111">In the Cash field, type a value.</span></span>
4. <span data-ttu-id="1d9fb-112">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="1d9fb-113">V poli Skupina číselné řady zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-113">In the Number sequence group field, enter or select a value.</span></span>
6. <span data-ttu-id="1d9fb-114">Rozbalte sekci Ověření.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-114">Expand the Validation section.</span></span>
7. <span data-ttu-id="1d9fb-115">V poli Měna zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-115">In the Currency field, enter or select a value.</span></span>
8. <span data-ttu-id="1d9fb-116">Vyberte možnost Ano v poli Záporná hotovost.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-116">Select Yes in the Negative cash field.</span></span>
9. <span data-ttu-id="1d9fb-117">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-117">Click Save.</span></span>

## <a name="create-a-new-journal"></a><span data-ttu-id="1d9fb-118">Vytvoření nového deníku</span><span class="sxs-lookup"><span data-stu-id="1d9fb-118">Create a new journal</span></span>
1. <span data-ttu-id="1d9fb-119">Přejděte do hlavní knihy > Nastavení deníku > Názvy deníků.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-119">Go to General ledger > Journal setup > Journal names.</span></span>
2. <span data-ttu-id="1d9fb-120">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-120">Click New.</span></span>
3. <span data-ttu-id="1d9fb-121">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-121">In the Name field, type a value.</span></span>
4. <span data-ttu-id="1d9fb-122">V poli Číselná řada dokladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-122">In the Voucher series field, enter or select a value.</span></span>
5. <span data-ttu-id="1d9fb-123">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-123">Click Save.</span></span>
6. <span data-ttu-id="1d9fb-124">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-124">Click New.</span></span>
7. <span data-ttu-id="1d9fb-125">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-125">In the Name field, type a value.</span></span>
8. <span data-ttu-id="1d9fb-126">Vyberte volbu v poli Typ deníku.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-126">In the Journal type field, select an option.</span></span>
9. <span data-ttu-id="1d9fb-127">V poli Číselná řada dokladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-127">In the Voucher series field, enter or select a value.</span></span>
10. <span data-ttu-id="1d9fb-128">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-128">Click Save.</span></span>

## <a name="create-an-advance-holder-group"></a><span data-ttu-id="1d9fb-129">Vytvoření skupiny držitelů záloh</span><span class="sxs-lookup"><span data-stu-id="1d9fb-129">Create an advance holder group</span></span>
1. <span data-ttu-id="1d9fb-130">Přejděte na Závazky > Nastavení > Držitelé zálohy > Skupiny držitelů záloh.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-130">Go to Accounts payable > Setup > Advance holders > Advance holder groups.</span></span>
2. <span data-ttu-id="1d9fb-131">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-131">Click New.</span></span>
3. <span data-ttu-id="1d9fb-132">Zadejte hodnotu do pole Skupina.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-132">In the Group field, type a value.</span></span>
4. <span data-ttu-id="1d9fb-133">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-133">In the Description field, type a value.</span></span>
5. <span data-ttu-id="1d9fb-134">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-134">Click Save.</span></span>

## <a name="create-an-employee-posting-profile"></a><span data-ttu-id="1d9fb-135">Vytvoření účetního profilu zaměstnance</span><span class="sxs-lookup"><span data-stu-id="1d9fb-135">Create an employee posting profile</span></span>
1. <span data-ttu-id="1d9fb-136">Přejděte na Závazky > Nastavení > Držitelé zálohy > Účetní profily zaměstnanců.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-136">Go to Accounts payable > Setup > Advance holders > Employee posting profiles.</span></span>
2. <span data-ttu-id="1d9fb-137">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-137">Click New.</span></span>
3. <span data-ttu-id="1d9fb-138">Zadejte hodnotu do pole Účetní profil.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-138">In the Posting profile field, type a value.</span></span>
4. <span data-ttu-id="1d9fb-139">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-139">In the Description field, type a value.</span></span>
5. <span data-ttu-id="1d9fb-140">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-140">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="1d9fb-141">Vyberte volbu v poli Platné pro.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-141">In the Valid for field, select an option.</span></span>
7. <span data-ttu-id="1d9fb-142">Zadejte požadované hodnoty do pole Součtový účet.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-142">In the Summary account field, specify the desired values.</span></span>
8. <span data-ttu-id="1d9fb-143">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-143">Click Save.</span></span>

## <a name="set-up-advance-holder-parameters"></a><span data-ttu-id="1d9fb-144">Nastavení parametrů držitele zálohy</span><span class="sxs-lookup"><span data-stu-id="1d9fb-144">Set up advance holder parameters</span></span>
1. <span data-ttu-id="1d9fb-145">Přejděte do nabídky Závazky > Nastavení > Parametry závazků.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-145">Go to Accounts payable > Setup > Accounts payable parameters.</span></span>
2. <span data-ttu-id="1d9fb-146">Klepněte na kartu Držitelé zálohy.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-146">Click the Advance holders tab.</span></span>
3. <span data-ttu-id="1d9fb-147">V poli Účetní profil zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-147">In the Posting profile field, enter or select a value.</span></span>
4. <span data-ttu-id="1d9fb-148">V poli Název zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-148">In the Name field, enter or select a value.</span></span>
5. <span data-ttu-id="1d9fb-149">V poli Hotovost zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-149">In the Cash field, enter or select a value.</span></span>
6. <span data-ttu-id="1d9fb-150">V poli Název zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-150">In the Name field, enter or select a value.</span></span>
7. <span data-ttu-id="1d9fb-151">V poli Typ účtu vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-151">In the Account type field, select an option.</span></span>
8. <span data-ttu-id="1d9fb-152">Zadejte požadované hodnoty do pole Hlavní účet.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-152">In the Main account field, specify the desired values.</span></span>
9. <span data-ttu-id="1d9fb-153">Klikněte na kartu Číselné řady.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-153">Click the Number sequences tab.</span></span>
10. <span data-ttu-id="1d9fb-154">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-154">Click Save.</span></span>

## <a name="set-up-a-cash-posting-profile"></a><span data-ttu-id="1d9fb-155">Nastavení účetního profilu pro hotovost</span><span class="sxs-lookup"><span data-stu-id="1d9fb-155">Set up a cash posting profile</span></span>
1. <span data-ttu-id="1d9fb-156">Přejděte do nabídky Pokladna a banka > Nastavení > Účetní profily pro hotovost.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-156">Go to Cash and bank management > Setup > Cash posting profiles.</span></span>
2. <span data-ttu-id="1d9fb-157">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-157">Click New.</span></span>
3. <span data-ttu-id="1d9fb-158">Zadejte hodnotu do pole Účtování hotovosti.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-158">In the Cash posting field, type a value.</span></span>
4. <span data-ttu-id="1d9fb-159">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-159">In the Description field, type a value.</span></span>
5. <span data-ttu-id="1d9fb-160">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-160">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="1d9fb-161">Vyberte volbu v poli Platné pro.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-161">In the Valid for field, select an option.</span></span>
7. <span data-ttu-id="1d9fb-162">Zadejte požadované hodnoty do pole Hlavní účet.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-162">In the Main account field, specify the desired values.</span></span>
8. <span data-ttu-id="1d9fb-163">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-163">Click Save.</span></span>

## <a name="set-up-cash-and-bank-parameters"></a><span data-ttu-id="1d9fb-164">Nastavení parametrů pokladny a banky</span><span class="sxs-lookup"><span data-stu-id="1d9fb-164">Set up cash and bank parameters</span></span>
1. <span data-ttu-id="1d9fb-165">Přejděte do nabídky Pokladna a banka > Nastavení > Parametry pokladny a banky.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-165">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="1d9fb-166">Klikněte na kartu Hotovost.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-166">Click the Cash tab.</span></span>
3. <span data-ttu-id="1d9fb-167">V poli Hotovost zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-167">In the Cash field, enter or select a value.</span></span>
4. <span data-ttu-id="1d9fb-168">V poli Účtování hotovosti nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-168">In the Cash posting field, enter or select a value.</span></span>
5. <span data-ttu-id="1d9fb-169">Klepněte na tlačítko Uložit.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-169">Click Save.</span></span>
6. <span data-ttu-id="1d9fb-170">Klikněte na kartu Číselné řady.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-170">Click the Number sequences tab.</span></span>
7. <span data-ttu-id="1d9fb-171">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-171">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="1d9fb-172">V poli Kód číselné řady zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-172">In the Number sequence code field, enter or select a value.</span></span>
9. <span data-ttu-id="1d9fb-173">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-173">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="1d9fb-174">V poli Kód číselné řady zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-174">In the Number sequence code field, enter or select a value.</span></span>
11. <span data-ttu-id="1d9fb-175">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-175">Click Save.</span></span>

## <a name="set-up-terms-of-payment"></a><span data-ttu-id="1d9fb-176">Nastavit podmínky platby</span><span class="sxs-lookup"><span data-stu-id="1d9fb-176">Set up terms of payment</span></span>
1. <span data-ttu-id="1d9fb-177">Přejděte do nabídky Závazky > Nastavení platby > Podmínky platby.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-177">Go to Accounts payable > Payment setup > Terms of payment.</span></span>
2. <span data-ttu-id="1d9fb-178">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-178">Click Edit.</span></span>
3. <span data-ttu-id="1d9fb-179">Vyberte možnost Ano v poli Od držitele zálohy.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-179">Select Yes in the From advance holder field.</span></span>
4. <span data-ttu-id="1d9fb-180">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-180">Click Save.</span></span>

## <a name="create-a-new-worker"></a><span data-ttu-id="1d9fb-181">Vytvoření nového pracovníka</span><span class="sxs-lookup"><span data-stu-id="1d9fb-181">Create a new worker</span></span>
1. <span data-ttu-id="1d9fb-182">Přejděte k nabídce Lidské zdroje > Pracovníci > Pracovníci.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-182">Go to Human resources > Workers > Workers.</span></span>
2. <span data-ttu-id="1d9fb-183">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-183">Click New.</span></span>
3. <span data-ttu-id="1d9fb-184">Do pole Křestní jméno zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-184">In the First name field, type a value.</span></span>
4. <span data-ttu-id="1d9fb-185">Do pole příjmení zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-185">In the Last name field, type a value.</span></span>
5. <span data-ttu-id="1d9fb-186">Zadejte hodnotu do pole ID pracovníka.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-186">In the Worker ID field, type a value.</span></span>
6. <span data-ttu-id="1d9fb-187">Klikněte na Přijmout nového pracovníka.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-187">Click Hire new worker.</span></span>
7. <span data-ttu-id="1d9fb-188">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-188">Click Save.</span></span>

## <a name="set-up-a-worker-as-an-advance-holder"></a><span data-ttu-id="1d9fb-189">Nastavení pracovníka jako držitele zálohy.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-189">Set up a worker as an advance holder</span></span>
1. <span data-ttu-id="1d9fb-190">Přejděte na Závazky > Držitelé zálohy > Držitelé zálohy.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-190">Go to Accounts payable > Advance holders > Advance holders.</span></span>
2. <span data-ttu-id="1d9fb-191">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-191">Click Edit.</span></span>
3. <span data-ttu-id="1d9fb-192">V poli Skupina zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-192">In the Group field, enter or select a value.</span></span>
4. <span data-ttu-id="1d9fb-193">Vyberte možnost Ano v poli Držitel zálohy.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-193">Select Yes in the Advance holder field.</span></span>
5. <span data-ttu-id="1d9fb-194">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-194">Click Save.</span></span>

## <a name="create-and-post-a-purchase-order-invoice"></a><span data-ttu-id="1d9fb-195">Vytvoření a zaúčtování faktury nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-195">Create and post a purchase order invoice</span></span>
1. <span data-ttu-id="1d9fb-196">Přejděte na Závazky > Nákupní objednávky > Všechny nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-196">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="1d9fb-197">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-197">Click New.</span></span>
3. <span data-ttu-id="1d9fb-198">V poli Účet dodavatele zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-198">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="1d9fb-199">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-199">Click OK.</span></span>
5. <span data-ttu-id="1d9fb-200">V poli Řádky nebo záhlaví vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-200">In the Lines or header field, select an option.</span></span>
6. <span data-ttu-id="1d9fb-201">Rozbalte část Ceny a slevy.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-201">Expand the Price and discount section.</span></span>
7. <span data-ttu-id="1d9fb-202">V poli Platební podmínky zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-202">In the Terms of payment field, enter or select a value.</span></span>
8. <span data-ttu-id="1d9fb-203">V poli Držitel zálohy zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-203">In the Advance holder field, enter or select a value.</span></span>
9. <span data-ttu-id="1d9fb-204">V poli Řádky nebo záhlaví vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-204">In the Lines or header field, select an option.</span></span>
10. <span data-ttu-id="1d9fb-205">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-205">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="1d9fb-206">V poli Číslo zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-206">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="1d9fb-207">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-207">In the Quantity field, enter a number.</span></span>
13. <span data-ttu-id="1d9fb-208">Zadejte číslo do pole Jednotková cena.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-208">In the Unit price field, enter a number.</span></span>
14. <span data-ttu-id="1d9fb-209">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-209">Click Save.</span></span>
15. <span data-ttu-id="1d9fb-210">V podokně akcí klikněte na položku Nákup.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-210">On the Action Pane, click Purchase.</span></span>
16. <span data-ttu-id="1d9fb-211">Klikněte na tlačítko Potvrdit.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-211">Click Confirm.</span></span>
17. <span data-ttu-id="1d9fb-212">V podokně akcí klikněte na položku Faktura.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-212">On the Action Pane, click Invoice.</span></span>
18. <span data-ttu-id="1d9fb-213">Klikněte na položku Faktura.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-213">Click Invoice.</span></span>
19. <span data-ttu-id="1d9fb-214">Kliknutím na Výchozí od: Množství v příjemce produktu otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-214">Click Default from: Product receipt quantity to open the drop dialog.</span></span>
20. <span data-ttu-id="1d9fb-215">Vyberte volbu v poli Výchozí množství pro řádky.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-215">In the Default quantity for lines field, select an option.</span></span>
21. <span data-ttu-id="1d9fb-216">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-216">Click OK.</span></span>
22. <span data-ttu-id="1d9fb-217">Zadejte hodnotu do pole Číslo.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-217">In the Number field, type a value.</span></span>
23. <span data-ttu-id="1d9fb-218">Do pole Popis faktury zadejte nějakou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-218">In the Invoice description field, type a value.</span></span>
24. <span data-ttu-id="1d9fb-219">Zadejte datum do pole Datum faktury.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-219">In the Invoice date field, enter a date.</span></span>
25. <span data-ttu-id="1d9fb-220">Do pole Rejstřík DPH zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-220">In the Date of VAT register field, enter a date.</span></span>
26. <span data-ttu-id="1d9fb-221">Zadejte datum do pole Datum přijetí dokumentu.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-221">In the Receive document date field, enter a date.</span></span>
27. <span data-ttu-id="1d9fb-222">Klikněte na položku Zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-222">Click Post.</span></span>

## <a name="balance-and-close-advance-holders-transactions"></a><span data-ttu-id="1d9fb-223">Zůstatek a uzavření transakce držitelů záloh</span><span class="sxs-lookup"><span data-stu-id="1d9fb-223">Balance and close advance holders transactions</span></span>
1. <span data-ttu-id="1d9fb-224">Přejděte na Závazky > Držitelé zálohy > Držitelé zálohy.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-224">Go to Accounts payable > Advance holders > Advance holders.</span></span>
2. <span data-ttu-id="1d9fb-225">Klikněte na Transakce.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-225">Click Transactions.</span></span>
3. <span data-ttu-id="1d9fb-226">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-226">Close the page.</span></span>
4. <span data-ttu-id="1d9fb-227">Klikněte na Zůstatek.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-227">Click Balance.</span></span>
5. <span data-ttu-id="1d9fb-228">Klikněte na Uzavřít v bance.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-228">Click Close via bank.</span></span>
6. <span data-ttu-id="1d9fb-229">Vyberte možnost Ano v poli Automaticky.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-229">Select Yes in the Automatic field.</span></span>
7. <span data-ttu-id="1d9fb-230">V poli Převáděná částka</span><span class="sxs-lookup"><span data-stu-id="1d9fb-230">In the Amount to be transferred.</span></span> <span data-ttu-id="1d9fb-231">zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-231">field, enter a number.</span></span>
8. <span data-ttu-id="1d9fb-232">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-232">Click OK.</span></span>
9. <span data-ttu-id="1d9fb-233">Klikněte na Uzavřít v hotovosti.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-233">Click Close via cash.</span></span>
10. <span data-ttu-id="1d9fb-234">Vyberte možnost Ano v poli Automaticky.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-234">Select Yes in the Automatic field.</span></span>
11. <span data-ttu-id="1d9fb-235">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-235">Click OK.</span></span>
12. <span data-ttu-id="1d9fb-236">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-236">Close the page.</span></span>
13. <span data-ttu-id="1d9fb-237">Klikněte na Transakce.</span><span class="sxs-lookup"><span data-stu-id="1d9fb-237">Click Transactions.</span></span>


