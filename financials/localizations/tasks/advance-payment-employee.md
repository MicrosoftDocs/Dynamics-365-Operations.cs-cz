--- 
title: "Záloha pro zaměstnance (východní Evropa)"
description: "Tato procedura ukazuje, jak lze nastavit a registrovat transakce pro držitele zálohy."
author: v-oloski
manager: AnnBe
ms.date: 10/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 4cc3ba589204f87b844ab4302e03105d2aa1de8d
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---
# <a name="advance-payment-to-an-employee-eastern-europe"></a><span data-ttu-id="408ac-103">Záloha pro zaměstnance (východní Evropa)</span><span class="sxs-lookup"><span data-stu-id="408ac-103">Advance payment to an employee (Eastern Europe)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="408ac-104">Tato procedura ukazuje, jak lze nastavit a registrovat transakce pro držitele zálohy.</span><span class="sxs-lookup"><span data-stu-id="408ac-104">This procedure demonstrates how to set up and register transactions for an advance holder.</span></span> <span data-ttu-id="408ac-105">Procedura byla vytvořena za použití ukázkových dat společnosti DEMF s primární adresou právnické osoby v Litvě.</span><span class="sxs-lookup"><span data-stu-id="408ac-105">This procedure was created using the demo data company DEMF with a primary address in Lithuania.</span></span> <span data-ttu-id="408ac-106">Tento úkol lze použít pouze pro právnické osoby s primární adresu v Polsku, Litvě, Lotyšsku, Estonsku, České republice nebo Maďarsku.</span><span class="sxs-lookup"><span data-stu-id="408ac-106">This task only works for legal entities with a primary address in Poland, Lithuania, Latvia, Estonia, Czech Republic, or Hungary.</span></span> <span data-ttu-id="408ac-107">Tato procedura je určena pro funkci, která byla přidána do aplikace Dynamics 365 for Operations verze 1611.</span><span class="sxs-lookup"><span data-stu-id="408ac-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-new-cash-account"></a><span data-ttu-id="408ac-108">Vytvoření nového bankovního účtu</span><span class="sxs-lookup"><span data-stu-id="408ac-108">Create a new cash account</span></span>
1. <span data-ttu-id="408ac-109">Přejděte do nabídky Pokladna a banka > Bankovní účty > Pokladní účty.</span><span class="sxs-lookup"><span data-stu-id="408ac-109">Go to Cash and bank management > Bank accounts > Cash accounts.</span></span>
2. <span data-ttu-id="408ac-110">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="408ac-110">Click New.</span></span>
3. <span data-ttu-id="408ac-111">Zadejte hodnotu do pole Hotovost.</span><span class="sxs-lookup"><span data-stu-id="408ac-111">In the Cash field, type a value.</span></span>
4. <span data-ttu-id="408ac-112">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="408ac-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="408ac-113">V poli Skupina číselné řady zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="408ac-113">In the Number sequence group field, enter or select a value.</span></span>
6. <span data-ttu-id="408ac-114">Rozbalte sekci Ověření.</span><span class="sxs-lookup"><span data-stu-id="408ac-114">Expand the Validation section.</span></span>
7. <span data-ttu-id="408ac-115">V poli Měna zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="408ac-115">In the Currency field, enter or select a value.</span></span>
8. <span data-ttu-id="408ac-116">Vyberte možnost Ano v poli Záporná hotovost.</span><span class="sxs-lookup"><span data-stu-id="408ac-116">Select Yes in the Negative cash field.</span></span>
9. <span data-ttu-id="408ac-117">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="408ac-117">Click Save.</span></span>

## <a name="create-a-new-journal"></a><span data-ttu-id="408ac-118">Vytvoření nového deníku</span><span class="sxs-lookup"><span data-stu-id="408ac-118">Create a new journal</span></span>
1. <span data-ttu-id="408ac-119">Přejděte do hlavní knihy > Nastavení deníku > Názvy deníků.</span><span class="sxs-lookup"><span data-stu-id="408ac-119">Go to General ledger > Journal setup > Journal names.</span></span>
2. <span data-ttu-id="408ac-120">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="408ac-120">Click New.</span></span>
3. <span data-ttu-id="408ac-121">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="408ac-121">In the Name field, type a value.</span></span>
4. <span data-ttu-id="408ac-122">V poli Číselná řada dokladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="408ac-122">In the Voucher series field, enter or select a value.</span></span>
5. <span data-ttu-id="408ac-123">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="408ac-123">Click Save.</span></span>
6. <span data-ttu-id="408ac-124">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="408ac-124">Click New.</span></span>
7. <span data-ttu-id="408ac-125">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="408ac-125">In the Name field, type a value.</span></span>
8. <span data-ttu-id="408ac-126">Vyberte volbu v poli Typ deníku.</span><span class="sxs-lookup"><span data-stu-id="408ac-126">In the Journal type field, select an option.</span></span>
9. <span data-ttu-id="408ac-127">V poli Číselná řada dokladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="408ac-127">In the Voucher series field, enter or select a value.</span></span>
10. <span data-ttu-id="408ac-128">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="408ac-128">Click Save.</span></span>

## <a name="create-an-advance-holder-group"></a><span data-ttu-id="408ac-129">Vytvoření skupiny držitelů záloh</span><span class="sxs-lookup"><span data-stu-id="408ac-129">Create an advance holder group</span></span>
1. <span data-ttu-id="408ac-130">Přejděte na Závazky > Nastavení > Držitelé zálohy > Skupiny držitelů záloh.</span><span class="sxs-lookup"><span data-stu-id="408ac-130">Go to Accounts payable > Setup > Advance holders > Advance holder groups.</span></span>
2. <span data-ttu-id="408ac-131">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="408ac-131">Click New.</span></span>
3. <span data-ttu-id="408ac-132">Zadejte hodnotu do pole Skupina.</span><span class="sxs-lookup"><span data-stu-id="408ac-132">In the Group field, type a value.</span></span>
4. <span data-ttu-id="408ac-133">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="408ac-133">In the Description field, type a value.</span></span>
5. <span data-ttu-id="408ac-134">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="408ac-134">Click Save.</span></span>

## <a name="create-an-employee-posting-profile"></a><span data-ttu-id="408ac-135">Vytvoření účetního profilu zaměstnance</span><span class="sxs-lookup"><span data-stu-id="408ac-135">Create an employee posting profile</span></span>
1. <span data-ttu-id="408ac-136">Přejděte na Závazky > Nastavení > Držitelé zálohy > Účetní profily zaměstnanců.</span><span class="sxs-lookup"><span data-stu-id="408ac-136">Go to Accounts payable > Setup > Advance holders > Employee posting profiles.</span></span>
2. <span data-ttu-id="408ac-137">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="408ac-137">Click New.</span></span>
3. <span data-ttu-id="408ac-138">Zadejte hodnotu do pole Účetní profil.</span><span class="sxs-lookup"><span data-stu-id="408ac-138">In the Posting profile field, type a value.</span></span>
4. <span data-ttu-id="408ac-139">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="408ac-139">In the Description field, type a value.</span></span>
5. <span data-ttu-id="408ac-140">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="408ac-140">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="408ac-141">Vyberte volbu v poli Platné pro.</span><span class="sxs-lookup"><span data-stu-id="408ac-141">In the Valid for field, select an option.</span></span>
7. <span data-ttu-id="408ac-142">Zadejte požadované hodnoty do pole Součtový účet.</span><span class="sxs-lookup"><span data-stu-id="408ac-142">In the Summary account field, specify the desired values.</span></span>
8. <span data-ttu-id="408ac-143">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="408ac-143">Click Save.</span></span>

## <a name="set-up-advance-holder-parameters"></a><span data-ttu-id="408ac-144">Nastavení parametrů držitele zálohy</span><span class="sxs-lookup"><span data-stu-id="408ac-144">Set up advance holder parameters</span></span>
1. <span data-ttu-id="408ac-145">Přejděte do nabídky Závazky > Nastavení > Parametry závazků.</span><span class="sxs-lookup"><span data-stu-id="408ac-145">Go to Accounts payable > Setup > Accounts payable parameters.</span></span>
2. <span data-ttu-id="408ac-146">Klepněte na kartu Držitelé zálohy.</span><span class="sxs-lookup"><span data-stu-id="408ac-146">Click the Advance holders tab.</span></span>
3. <span data-ttu-id="408ac-147">V poli Účetní profil zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="408ac-147">In the Posting profile field, enter or select a value.</span></span>
4. <span data-ttu-id="408ac-148">V poli Název zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="408ac-148">In the Name field, enter or select a value.</span></span>
5. <span data-ttu-id="408ac-149">V poli Hotovost zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="408ac-149">In the Cash field, enter or select a value.</span></span>
6. <span data-ttu-id="408ac-150">V poli Název zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="408ac-150">In the Name field, enter or select a value.</span></span>
7. <span data-ttu-id="408ac-151">V poli Typ účtu vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="408ac-151">In the Account type field, select an option.</span></span>
8. <span data-ttu-id="408ac-152">Zadejte požadované hodnoty do pole Hlavní účet.</span><span class="sxs-lookup"><span data-stu-id="408ac-152">In the Main account field, specify the desired values.</span></span>
9. <span data-ttu-id="408ac-153">Klikněte na kartu Číselné řady.</span><span class="sxs-lookup"><span data-stu-id="408ac-153">Click the Number sequences tab.</span></span>
10. <span data-ttu-id="408ac-154">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="408ac-154">Click Save.</span></span>

## <a name="set-up-a-cash-posting-profile"></a><span data-ttu-id="408ac-155">Nastavení účetního profilu pro hotovost</span><span class="sxs-lookup"><span data-stu-id="408ac-155">Set up a cash posting profile</span></span>
1. <span data-ttu-id="408ac-156">Přejděte do nabídky Pokladna a banka > Nastavení > Účetní profily pro hotovost.</span><span class="sxs-lookup"><span data-stu-id="408ac-156">Go to Cash and bank management > Setup > Cash posting profiles.</span></span>
2. <span data-ttu-id="408ac-157">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="408ac-157">Click New.</span></span>
3. <span data-ttu-id="408ac-158">Zadejte hodnotu do pole Účtování hotovosti.</span><span class="sxs-lookup"><span data-stu-id="408ac-158">In the Cash posting field, type a value.</span></span>
4. <span data-ttu-id="408ac-159">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="408ac-159">In the Description field, type a value.</span></span>
5. <span data-ttu-id="408ac-160">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="408ac-160">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="408ac-161">Vyberte volbu v poli Platné pro.</span><span class="sxs-lookup"><span data-stu-id="408ac-161">In the Valid for field, select an option.</span></span>
7. <span data-ttu-id="408ac-162">Zadejte požadované hodnoty do pole Hlavní účet.</span><span class="sxs-lookup"><span data-stu-id="408ac-162">In the Main account field, specify the desired values.</span></span>
8. <span data-ttu-id="408ac-163">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="408ac-163">Click Save.</span></span>

## <a name="set-up-cash-and-bank-parameters"></a><span data-ttu-id="408ac-164">Nastavení parametrů pokladny a banky</span><span class="sxs-lookup"><span data-stu-id="408ac-164">Set up cash and bank parameters</span></span>
1. <span data-ttu-id="408ac-165">Přejděte do nabídky Pokladna a banka > Nastavení > Parametry pokladny a banky.</span><span class="sxs-lookup"><span data-stu-id="408ac-165">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="408ac-166">Klikněte na kartu Hotovost.</span><span class="sxs-lookup"><span data-stu-id="408ac-166">Click the Cash tab.</span></span>
3. <span data-ttu-id="408ac-167">V poli Hotovost zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="408ac-167">In the Cash field, enter or select a value.</span></span>
4. <span data-ttu-id="408ac-168">V poli Účtování hotovosti nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="408ac-168">In the Cash posting field, enter or select a value.</span></span>
5. <span data-ttu-id="408ac-169">Klepněte na tlačítko Uložit.</span><span class="sxs-lookup"><span data-stu-id="408ac-169">Click Save.</span></span>
6. <span data-ttu-id="408ac-170">Klikněte na kartu Číselné řady.</span><span class="sxs-lookup"><span data-stu-id="408ac-170">Click the Number sequences tab.</span></span>
7. <span data-ttu-id="408ac-171">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="408ac-171">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="408ac-172">V poli Kód číselné řady zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="408ac-172">In the Number sequence code field, enter or select a value.</span></span>
9. <span data-ttu-id="408ac-173">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="408ac-173">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="408ac-174">V poli Kód číselné řady zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="408ac-174">In the Number sequence code field, enter or select a value.</span></span>
11. <span data-ttu-id="408ac-175">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="408ac-175">Click Save.</span></span>

## <a name="set-up-terms-of-payment"></a><span data-ttu-id="408ac-176">Nastavit podmínky platby</span><span class="sxs-lookup"><span data-stu-id="408ac-176">Set up terms of payment</span></span>
1. <span data-ttu-id="408ac-177">Přejděte do nabídky Závazky > Nastavení platby > Podmínky platby.</span><span class="sxs-lookup"><span data-stu-id="408ac-177">Go to Accounts payable > Payment setup > Terms of payment.</span></span>
2. <span data-ttu-id="408ac-178">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="408ac-178">Click Edit.</span></span>
3. <span data-ttu-id="408ac-179">Vyberte možnost Ano v poli Od držitele zálohy.</span><span class="sxs-lookup"><span data-stu-id="408ac-179">Select Yes in the From advance holder field.</span></span>
4. <span data-ttu-id="408ac-180">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="408ac-180">Click Save.</span></span>

## <a name="create-a-new-worker"></a><span data-ttu-id="408ac-181">Vytvoření nového pracovníka</span><span class="sxs-lookup"><span data-stu-id="408ac-181">Create a new worker</span></span>
1. <span data-ttu-id="408ac-182">Přejděte k nabídce Lidské zdroje > Pracovníci > Pracovníci.</span><span class="sxs-lookup"><span data-stu-id="408ac-182">Go to Human resources > Workers > Workers.</span></span>
2. <span data-ttu-id="408ac-183">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="408ac-183">Click New.</span></span>
3. <span data-ttu-id="408ac-184">Do pole Křestní jméno zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="408ac-184">In the First name field, type a value.</span></span>
4. <span data-ttu-id="408ac-185">Do pole příjmení zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="408ac-185">In the Last name field, type a value.</span></span>
5. <span data-ttu-id="408ac-186">Zadejte hodnotu do pole ID pracovníka.</span><span class="sxs-lookup"><span data-stu-id="408ac-186">In the Worker ID field, type a value.</span></span>
6. <span data-ttu-id="408ac-187">Klikněte na Přijmout nového pracovníka.</span><span class="sxs-lookup"><span data-stu-id="408ac-187">Click Hire new worker.</span></span>
7. <span data-ttu-id="408ac-188">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="408ac-188">Click Save.</span></span>

## <a name="set-up-a-worker-as-an-advance-holder"></a><span data-ttu-id="408ac-189">Nastavení pracovníka jako držitele zálohy.</span><span class="sxs-lookup"><span data-stu-id="408ac-189">Set up a worker as an advance holder</span></span>
1. <span data-ttu-id="408ac-190">Přejděte na Závazky > Držitelé zálohy > Držitelé zálohy.</span><span class="sxs-lookup"><span data-stu-id="408ac-190">Go to Accounts payable > Advance holders > Advance holders.</span></span>
2. <span data-ttu-id="408ac-191">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="408ac-191">Click Edit.</span></span>
3. <span data-ttu-id="408ac-192">V poli Skupina zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="408ac-192">In the Group field, enter or select a value.</span></span>
4. <span data-ttu-id="408ac-193">Vyberte možnost Ano v poli Držitel zálohy.</span><span class="sxs-lookup"><span data-stu-id="408ac-193">Select Yes in the Advance holder field.</span></span>
5. <span data-ttu-id="408ac-194">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="408ac-194">Click Save.</span></span>

## <a name="create-and-post-a-purchase-order-invoice"></a><span data-ttu-id="408ac-195">Vytvoření a zaúčtování faktury nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="408ac-195">Create and post a purchase order invoice</span></span>
1. <span data-ttu-id="408ac-196">Přejděte na Závazky > Nákupní objednávky > Všechny nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="408ac-196">Go to Accounts payable > Purchase orders > All purchase orders.</span></span>
2. <span data-ttu-id="408ac-197">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="408ac-197">Click New.</span></span>
3. <span data-ttu-id="408ac-198">V poli Účet dodavatele zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="408ac-198">In the Vendor account field, enter or select a value.</span></span>
4. <span data-ttu-id="408ac-199">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="408ac-199">Click OK.</span></span>
5. <span data-ttu-id="408ac-200">V poli Řádky nebo záhlaví vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="408ac-200">In the Lines or header field, select an option.</span></span>
6. <span data-ttu-id="408ac-201">Rozbalte část Ceny a slevy.</span><span class="sxs-lookup"><span data-stu-id="408ac-201">Expand the Price and discount section.</span></span>
7. <span data-ttu-id="408ac-202">V poli Platební podmínky zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="408ac-202">In the Terms of payment field, enter or select a value.</span></span>
8. <span data-ttu-id="408ac-203">V poli Držitel zálohy zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="408ac-203">In the Advance holder field, enter or select a value.</span></span>
9. <span data-ttu-id="408ac-204">V poli Řádky nebo záhlaví vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="408ac-204">In the Lines or header field, select an option.</span></span>
10. <span data-ttu-id="408ac-205">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="408ac-205">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="408ac-206">V poli Číslo zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="408ac-206">In the Item number field, enter or select a value.</span></span>
12. <span data-ttu-id="408ac-207">Zadejte číslo do pole Množství.</span><span class="sxs-lookup"><span data-stu-id="408ac-207">In the Quantity field, enter a number.</span></span>
13. <span data-ttu-id="408ac-208">Zadejte číslo do pole Jednotková cena.</span><span class="sxs-lookup"><span data-stu-id="408ac-208">In the Unit price field, enter a number.</span></span>
14. <span data-ttu-id="408ac-209">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="408ac-209">Click Save.</span></span>
15. <span data-ttu-id="408ac-210">V podokně akcí klikněte na položku Nákup.</span><span class="sxs-lookup"><span data-stu-id="408ac-210">On the Action Pane, click Purchase.</span></span>
16. <span data-ttu-id="408ac-211">Klikněte na tlačítko Potvrdit.</span><span class="sxs-lookup"><span data-stu-id="408ac-211">Click Confirm.</span></span>
17. <span data-ttu-id="408ac-212">V podokně akcí klikněte na položku Faktura.</span><span class="sxs-lookup"><span data-stu-id="408ac-212">On the Action Pane, click Invoice.</span></span>
18. <span data-ttu-id="408ac-213">Klikněte na položku Faktura.</span><span class="sxs-lookup"><span data-stu-id="408ac-213">Click Invoice.</span></span>
19. <span data-ttu-id="408ac-214">Kliknutím na Výchozí od: Množství v příjemce produktu otevřete dialogové okno.</span><span class="sxs-lookup"><span data-stu-id="408ac-214">Click Default from: Product receipt quantity to open the drop dialog.</span></span>
20. <span data-ttu-id="408ac-215">Vyberte volbu v poli Výchozí množství pro řádky.</span><span class="sxs-lookup"><span data-stu-id="408ac-215">In the Default quantity for lines field, select an option.</span></span>
21. <span data-ttu-id="408ac-216">Klepněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="408ac-216">Click OK.</span></span>
22. <span data-ttu-id="408ac-217">Zadejte hodnotu do pole Číslo.</span><span class="sxs-lookup"><span data-stu-id="408ac-217">In the Number field, type a value.</span></span>
23. <span data-ttu-id="408ac-218">Do pole Popis faktury zadejte nějakou hodnotu.</span><span class="sxs-lookup"><span data-stu-id="408ac-218">In the Invoice description field, type a value.</span></span>
24. <span data-ttu-id="408ac-219">Zadejte datum do pole Datum faktury.</span><span class="sxs-lookup"><span data-stu-id="408ac-219">In the Invoice date field, enter a date.</span></span>
25. <span data-ttu-id="408ac-220">Do pole Rejstřík DPH zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="408ac-220">In the Date of VAT register field, enter a date.</span></span>
26. <span data-ttu-id="408ac-221">Zadejte datum do pole Datum přijetí dokumentu.</span><span class="sxs-lookup"><span data-stu-id="408ac-221">In the Receive document date field, enter a date.</span></span>
27. <span data-ttu-id="408ac-222">Klikněte na položku Zaúčtovat.</span><span class="sxs-lookup"><span data-stu-id="408ac-222">Click Post.</span></span>

## <a name="balance-and-close-advance-holders-transactions"></a><span data-ttu-id="408ac-223">Zůstatek a uzavření transakce držitelů záloh</span><span class="sxs-lookup"><span data-stu-id="408ac-223">Balance and close advance holders transactions</span></span>
1. <span data-ttu-id="408ac-224">Přejděte na Závazky > Držitelé zálohy > Držitelé zálohy.</span><span class="sxs-lookup"><span data-stu-id="408ac-224">Go to Accounts payable > Advance holders > Advance holders.</span></span>
2. <span data-ttu-id="408ac-225">Klikněte na Transakce.</span><span class="sxs-lookup"><span data-stu-id="408ac-225">Click Transactions.</span></span>
3. <span data-ttu-id="408ac-226">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="408ac-226">Close the page.</span></span>
4. <span data-ttu-id="408ac-227">Klikněte na Zůstatek.</span><span class="sxs-lookup"><span data-stu-id="408ac-227">Click Balance.</span></span>
5. <span data-ttu-id="408ac-228">Klikněte na Uzavřít v bance.</span><span class="sxs-lookup"><span data-stu-id="408ac-228">Click Close via bank.</span></span>
6. <span data-ttu-id="408ac-229">Vyberte možnost Ano v poli Automaticky.</span><span class="sxs-lookup"><span data-stu-id="408ac-229">Select Yes in the Automatic field.</span></span>
7. <span data-ttu-id="408ac-230">V poli Převáděná částka</span><span class="sxs-lookup"><span data-stu-id="408ac-230">In the Amount to be transferred.</span></span> <span data-ttu-id="408ac-231">zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="408ac-231">field, enter a number.</span></span>
8. <span data-ttu-id="408ac-232">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="408ac-232">Click OK.</span></span>
9. <span data-ttu-id="408ac-233">Klikněte na Uzavřít v hotovosti.</span><span class="sxs-lookup"><span data-stu-id="408ac-233">Click Close via cash.</span></span>
10. <span data-ttu-id="408ac-234">Vyberte možnost Ano v poli Automaticky.</span><span class="sxs-lookup"><span data-stu-id="408ac-234">Select Yes in the Automatic field.</span></span>
11. <span data-ttu-id="408ac-235">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="408ac-235">Click OK.</span></span>
12. <span data-ttu-id="408ac-236">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="408ac-236">Close the page.</span></span>
13. <span data-ttu-id="408ac-237">Klikněte na Transakce.</span><span class="sxs-lookup"><span data-stu-id="408ac-237">Click Transactions.</span></span>


