--- 
title: "Nastavení účetních profilů dlouhodobého majetku"
description: "Tento průvodce úkolem nastaví účetní profily pro dlouhodobý majetek."
author: saraschi2
manager: AnnBe
ms.date: 02/24/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: b9766d96d16429d0ce0864695a3157f54cad4054
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-fixed-asset-posting-profiles"></a><span data-ttu-id="fbec7-103">Nastavení účetních profilů dlouhodobého majetku</span><span class="sxs-lookup"><span data-stu-id="fbec7-103">Set up fixed asset posting profiles</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fbec7-104">Tento průvodce úkolem nastaví účetní profily pro dlouhodobý majetek.</span><span class="sxs-lookup"><span data-stu-id="fbec7-104">This task guide will set up Fixed asset posting profiles.</span></span>  <span data-ttu-id="fbec7-105">Využívá účetní role a ukázková data pro právnické osoby USMF.</span><span class="sxs-lookup"><span data-stu-id="fbec7-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>  <span data-ttu-id="fbec7-106">Příklady uvedené v průvodci úkolem jsou určeny pro základní účetní profil, i když účetní profily je nutné vytvořit pro vaši konkrétní účtovou osnovu a požadavky na finanční výkazy.</span><span class="sxs-lookup"><span data-stu-id="fbec7-106">Examples given in the task guide are for a basic posting profile, though posting profiles must be created for your specific chart of accounts and financial reporting requirements.</span></span>

1. <span data-ttu-id="fbec7-107">Přejděte na Dlouhodobý majetek > Nastavení > Účetní profily dlouhodobého majetku.</span><span class="sxs-lookup"><span data-stu-id="fbec7-107">Go to Fixed assets > Setup > Fixed asset posting profiles.</span></span>
2. <span data-ttu-id="fbec7-108">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="fbec7-108">Click New.</span></span>
3. <span data-ttu-id="fbec7-109">Zadejte hodnotu do pole Účetní profil.</span><span class="sxs-lookup"><span data-stu-id="fbec7-109">In the Posting profile field, type a value.</span></span>
4. <span data-ttu-id="fbec7-110">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="fbec7-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="fbec7-111">Musíte vytvořit zaúčtovací profil pro každý typ transakce dlouhodobého majetku, který chcete použít při práci s dlouhodobým majetkem.</span><span class="sxs-lookup"><span data-stu-id="fbec7-111">You will need to create a posting profile for each fixed asset transaction type you will be using when working with fixed assets.</span></span>  <span data-ttu-id="fbec7-112">Tento průvodce úkolem se spustí s typem Transakce pořízení.</span><span class="sxs-lookup"><span data-stu-id="fbec7-112">This task guide will start with the Acquisition transaction type.</span></span>  
5. <span data-ttu-id="fbec7-113">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="fbec7-113">Click Add.</span></span>
6. <span data-ttu-id="fbec7-114">V poli Kniha zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="fbec7-114">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="fbec7-115">Pole Seskupení umožňuje definovat účetní profil pro tabulku (jeden účet pro každý dlouhodobý majetek) nebo skupinu (jeden účet pro každou skupinu dlouhodobého majetku).</span><span class="sxs-lookup"><span data-stu-id="fbec7-115">The Groupings field allows you to define the posting profile down to the Table (one account set up for each fixed asset) or Group (one account set up for each fixed asset group).</span></span>  <span data-ttu-id="fbec7-116">Pro tohoto průvodce záznamem úloh ponecháme nastavenou hodnotu Vše a použijeme tak veškerý dlouhodobý majetek se zadanou knihou.</span><span class="sxs-lookup"><span data-stu-id="fbec7-116">For this task guide I will leave the value set to “All” to apply to all fixed assets with the specified Book.</span></span>  
7. <span data-ttu-id="fbec7-117">Zadejte požadované hodnoty do pole Hlavní účet.</span><span class="sxs-lookup"><span data-stu-id="fbec7-117">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="fbec7-118">Pro Pořízení zadejte protiúčet, nebo ponechejte pole prázdné a nechte je vyplnit pro určitou transakci.</span><span class="sxs-lookup"><span data-stu-id="fbec7-118">For Acquisitions, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>    
8. <span data-ttu-id="fbec7-119">V poli Typ transakce vyberte typ „Oprava pořizovací ceny“.</span><span class="sxs-lookup"><span data-stu-id="fbec7-119">In the Transaction type field, select 'Acquisition adjustment'.</span></span>
    * <span data-ttu-id="fbec7-120">Pro úpravu transakcí opravy pořizovací ceny použijeme stejné účty, které byly použity pro transakce pořízení.</span><span class="sxs-lookup"><span data-stu-id="fbec7-120">For Acquisition adjustment transactions, we will use the same accounts as used for Acquisition transactions.</span></span>  
9. <span data-ttu-id="fbec7-121">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="fbec7-121">Click Add.</span></span>
10. <span data-ttu-id="fbec7-122">V poli Kniha zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="fbec7-122">In the Book field, enter or select a value.</span></span>
11. <span data-ttu-id="fbec7-123">Zadejte požadované hodnoty do pole Hlavní účet.</span><span class="sxs-lookup"><span data-stu-id="fbec7-123">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="fbec7-124">Pro Opravy pořizovací ceny zadejte protiúčet, nebo ponechejte pole prázdné a nechte je vyplnit pro určitou transakci.</span><span class="sxs-lookup"><span data-stu-id="fbec7-124">For Acquisition adjustments, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>    
12. <span data-ttu-id="fbec7-125">V poli Typ transakce vyberte typ „Odpisy“.</span><span class="sxs-lookup"><span data-stu-id="fbec7-125">In the Transaction type field, select 'Depreciation'.</span></span>
13. <span data-ttu-id="fbec7-126">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="fbec7-126">Click Add.</span></span>
14. <span data-ttu-id="fbec7-127">V poli Kniha zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="fbec7-127">In the Book field, enter or select a value.</span></span>
15. <span data-ttu-id="fbec7-128">Zadejte požadované hodnoty do pole Hlavní účet.</span><span class="sxs-lookup"><span data-stu-id="fbec7-128">In the Main account field, specify the desired values.</span></span>
16. <span data-ttu-id="fbec7-129">Zadejte požadované hodnoty do pole Protiúčet.</span><span class="sxs-lookup"><span data-stu-id="fbec7-129">In the Offset account field, specify the desired values.</span></span>
17. <span data-ttu-id="fbec7-130">V poli Typ transakce vyberte typ „Oprava odpisu“.</span><span class="sxs-lookup"><span data-stu-id="fbec7-130">In the Transaction type field, select 'Depreciation adjustment'.</span></span>
    * <span data-ttu-id="fbec7-131">Pro úpravu transakcí odpisů použijeme stejné účty, které byly použity pro transakce odpisů.</span><span class="sxs-lookup"><span data-stu-id="fbec7-131">For Depreciation adjustment transactions, we will use the same accounts as used for Depreciation transactions.</span></span>  
18. <span data-ttu-id="fbec7-132">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="fbec7-132">Click Add.</span></span>
19. <span data-ttu-id="fbec7-133">V poli Kniha zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="fbec7-133">In the Book field, enter or select a value.</span></span>
20. <span data-ttu-id="fbec7-134">Zadejte požadované hodnoty do pole Hlavní účet.</span><span class="sxs-lookup"><span data-stu-id="fbec7-134">In the Main account field, specify the desired values.</span></span>
21. <span data-ttu-id="fbec7-135">Zadejte požadované hodnoty do pole Protiúčet.</span><span class="sxs-lookup"><span data-stu-id="fbec7-135">In the Offset account field, specify the desired values.</span></span>
22. <span data-ttu-id="fbec7-136">V poli Typ transakce vyberte typ „Vyřazení – odprodej“.</span><span class="sxs-lookup"><span data-stu-id="fbec7-136">In the Transaction type field, select 'Disposal - sale'.</span></span>
23. <span data-ttu-id="fbec7-137">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="fbec7-137">Click Add.</span></span>
24. <span data-ttu-id="fbec7-138">V poli Kniha zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="fbec7-138">In the Book field, enter or select a value.</span></span>
25. <span data-ttu-id="fbec7-139">Zadejte požadované hodnoty do pole Hlavní účet.</span><span class="sxs-lookup"><span data-stu-id="fbec7-139">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="fbec7-140">Pro Vyřazení zadejte protiúčet, nebo ponechejte pole prázdné a nechte je vyplnit pro určitou transakci.</span><span class="sxs-lookup"><span data-stu-id="fbec7-140">For Disposals, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>  
26. <span data-ttu-id="fbec7-141">V poli Typ transakce vyberte typ „Vyřazení – likvidace“.</span><span class="sxs-lookup"><span data-stu-id="fbec7-141">In the Transaction type field, select 'Disposal - scrap'.</span></span>
    * <span data-ttu-id="fbec7-142">Použijeme stejné účty pro Vyřazení – odprodej a Vyřazení – likvidace.</span><span class="sxs-lookup"><span data-stu-id="fbec7-142">We will use the same accounts for Disposal sale and Disposal scrap.</span></span>  
27. <span data-ttu-id="fbec7-143">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="fbec7-143">Click Add.</span></span>
28. <span data-ttu-id="fbec7-144">V poli Kniha zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="fbec7-144">In the Book field, enter or select a value.</span></span>
29. <span data-ttu-id="fbec7-145">Zadejte požadované hodnoty do pole Hlavní účet.</span><span class="sxs-lookup"><span data-stu-id="fbec7-145">In the Main account field, specify the desired values.</span></span>
    * <span data-ttu-id="fbec7-146">Pro Vyřazení zadejte protiúčet, nebo ponechejte pole prázdné a nechte je vyplnit pro určitou transakci.</span><span class="sxs-lookup"><span data-stu-id="fbec7-146">For Disposals, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>  
30. <span data-ttu-id="fbec7-147">Rozbalte sekci Vyřazení.</span><span class="sxs-lookup"><span data-stu-id="fbec7-147">Expand the Disposal section.</span></span>
    * <span data-ttu-id="fbec7-148">Nastavte účetní profily pro vyřazení prodeje i odpadu.</span><span class="sxs-lookup"><span data-stu-id="fbec7-148">You must set up disposal posting profiles for both sale and scrap.</span></span>  <span data-ttu-id="fbec7-149">Začneme s transakcemi zaměřenými na odprodej po vyřazení.</span><span class="sxs-lookup"><span data-stu-id="fbec7-149">We will start with disposal sale transactions.</span></span>  
31. <span data-ttu-id="fbec7-150">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="fbec7-150">Click Add.</span></span>
32. <span data-ttu-id="fbec7-151">V poli Kniha zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="fbec7-151">In the Book field, enter or select a value.</span></span>
33. <span data-ttu-id="fbec7-152">V poli Zaúčtovat hodnotu vyberte Pořizovací hodnota.</span><span class="sxs-lookup"><span data-stu-id="fbec7-152">In the Post value field, select 'Acquisition value'.</span></span>
    * <span data-ttu-id="fbec7-153">Pořizovací hodnota se zaměřuje na pořízení a opravu pořizovací ceny pro všechny roky.</span><span class="sxs-lookup"><span data-stu-id="fbec7-153">Acquisition value will address Acquisition and Acquisition adjustment values for all years.</span></span>  <span data-ttu-id="fbec7-154">Můžete také definovat účty pro tyto typy transakcí samostatně.</span><span class="sxs-lookup"><span data-stu-id="fbec7-154">You can also define accounts for these transaction types separately.</span></span>  
    * <span data-ttu-id="fbec7-155">Můžete nastavit proces vyřazení tak, aby používal různé účty v závislosti na tom, zda je výsledkem odpisu zisk nebo ztráta.</span><span class="sxs-lookup"><span data-stu-id="fbec7-155">You can set the disposal process to use different accounts depending upon if the disposal results in a gain or loss.</span></span>  <span data-ttu-id="fbec7-156">Nastavíme hodnotu prodeje na Vše a použijeme tak stejné účty pro všechny typy vyřazení.</span><span class="sxs-lookup"><span data-stu-id="fbec7-156">I will set the Sales value type to “All” to use the same accounts for all types of disposals.</span></span>  
34. <span data-ttu-id="fbec7-157">Zadejte požadované hodnoty do pole Hlavní účet.</span><span class="sxs-lookup"><span data-stu-id="fbec7-157">In the Main account field, specify the desired values.</span></span>
35. <span data-ttu-id="fbec7-158">Zadejte požadované hodnoty do pole Protiúčet.</span><span class="sxs-lookup"><span data-stu-id="fbec7-158">In the Offset account field, specify the desired values.</span></span>
36. <span data-ttu-id="fbec7-159">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="fbec7-159">Click Add.</span></span>
37. <span data-ttu-id="fbec7-160">V poli Kniha zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="fbec7-160">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="fbec7-161">V poli Zaúčtovat hodnotu vyberte hodnotu Odpis (předchozí roky).</span><span class="sxs-lookup"><span data-stu-id="fbec7-161">In the Post value field, select 'Depreciation (prior years)'.</span></span>  
38. <span data-ttu-id="fbec7-162">Zadejte požadované hodnoty do pole Hlavní účet.</span><span class="sxs-lookup"><span data-stu-id="fbec7-162">In the Main account field, specify the desired values.</span></span>
39. <span data-ttu-id="fbec7-163">Zadejte požadované hodnoty do pole Protiúčet.</span><span class="sxs-lookup"><span data-stu-id="fbec7-163">In the Offset account field, specify the desired values.</span></span>
40. <span data-ttu-id="fbec7-164">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="fbec7-164">Click Add.</span></span>
41. <span data-ttu-id="fbec7-165">V poli Kniha zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="fbec7-165">In the Book field, enter or select a value.</span></span>
42. <span data-ttu-id="fbec7-166">V poli Zaúčtovat hodnotu vyberte hodnotu Odpis (tento rok).</span><span class="sxs-lookup"><span data-stu-id="fbec7-166">In the Post value field, select 'Depreciation (this year)'.</span></span>
43. <span data-ttu-id="fbec7-167">Zadejte požadované hodnoty do pole Hlavní účet.</span><span class="sxs-lookup"><span data-stu-id="fbec7-167">In the Main account field, specify the desired values.</span></span>
44. <span data-ttu-id="fbec7-168">Zadejte požadované hodnoty do pole Protiúčet.</span><span class="sxs-lookup"><span data-stu-id="fbec7-168">In the Offset account field, specify the desired values.</span></span>
45. <span data-ttu-id="fbec7-169">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="fbec7-169">Click Add.</span></span>
46. <span data-ttu-id="fbec7-170">V poli Kniha zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="fbec7-170">In the Book field, enter or select a value.</span></span>
47. <span data-ttu-id="fbec7-171">V poli Zaúčtovat hodnotu vyberte hodnotu Opravy odpisů (předchozí roky).</span><span class="sxs-lookup"><span data-stu-id="fbec7-171">In the Post value field, select 'Depreciation adjustments (prior years)'.</span></span>
48. <span data-ttu-id="fbec7-172">Zadejte požadované hodnoty do pole Hlavní účet.</span><span class="sxs-lookup"><span data-stu-id="fbec7-172">In the Main account field, specify the desired values.</span></span>
49. <span data-ttu-id="fbec7-173">Zadejte požadované hodnoty do pole Protiúčet.</span><span class="sxs-lookup"><span data-stu-id="fbec7-173">In the Offset account field, specify the desired values.</span></span>
50. <span data-ttu-id="fbec7-174">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="fbec7-174">Click Add.</span></span>
51. <span data-ttu-id="fbec7-175">V poli Kniha zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="fbec7-175">In the Book field, enter or select a value.</span></span>
52. <span data-ttu-id="fbec7-176">V poli Zaúčtovat hodnotu vyberte hodnotu Opravy odpisů (tento rok).</span><span class="sxs-lookup"><span data-stu-id="fbec7-176">In the Post value field, select 'Depreciation adjustments (this year)'.</span></span>
53. <span data-ttu-id="fbec7-177">Zadejte požadované hodnoty do pole Hlavní účet.</span><span class="sxs-lookup"><span data-stu-id="fbec7-177">In the Main account field, specify the desired values.</span></span>
54. <span data-ttu-id="fbec7-178">Zadejte požadované hodnoty do pole Protiúčet.</span><span class="sxs-lookup"><span data-stu-id="fbec7-178">In the Offset account field, specify the desired values.</span></span>
55. <span data-ttu-id="fbec7-179">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="fbec7-179">Click Add.</span></span>
56. <span data-ttu-id="fbec7-180">V poli Kniha zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="fbec7-180">In the Book field, enter or select a value.</span></span>
57. <span data-ttu-id="fbec7-181">V poli Zaúčtovat hodnotu vyberte Zůstatková účetní hodnota.</span><span class="sxs-lookup"><span data-stu-id="fbec7-181">In the Post value field, select 'Net book value'.</span></span>
58. <span data-ttu-id="fbec7-182">Zadejte požadované hodnoty do pole Hlavní účet.</span><span class="sxs-lookup"><span data-stu-id="fbec7-182">In the Main account field, specify the desired values.</span></span>
59. <span data-ttu-id="fbec7-183">Zadejte požadované hodnoty do pole Protiúčet.</span><span class="sxs-lookup"><span data-stu-id="fbec7-183">In the Offset account field, specify the desired values.</span></span>
60. <span data-ttu-id="fbec7-184">V poli Odprodej nebo likvidace vyberte „Likvidace“</span><span class="sxs-lookup"><span data-stu-id="fbec7-184">In the Sale or scrap field, select 'Scrap'.</span></span>
61. <span data-ttu-id="fbec7-185">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="fbec7-185">Click Add.</span></span>
62. <span data-ttu-id="fbec7-186">V poli Kniha zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="fbec7-186">In the Book field, enter or select a value.</span></span>
63. <span data-ttu-id="fbec7-187">V poli Zaúčtovat hodnotu vyberte Pořizovací hodnota.</span><span class="sxs-lookup"><span data-stu-id="fbec7-187">In the Post value field, select 'Acquisition value'.</span></span>
64. <span data-ttu-id="fbec7-188">Zadejte požadované hodnoty do pole Hlavní účet.</span><span class="sxs-lookup"><span data-stu-id="fbec7-188">In the Main account field, specify the desired values.</span></span>
65. <span data-ttu-id="fbec7-189">Zadejte požadované hodnoty do pole Protiúčet.</span><span class="sxs-lookup"><span data-stu-id="fbec7-189">In the Offset account field, specify the desired values.</span></span>
66. <span data-ttu-id="fbec7-190">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="fbec7-190">Click Add.</span></span>
67. <span data-ttu-id="fbec7-191">V poli Kniha zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="fbec7-191">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="fbec7-192">V poli Zaúčtovat hodnotu vyberte hodnotu Odpis (předchozí roky).</span><span class="sxs-lookup"><span data-stu-id="fbec7-192">In Post value field, select 'Depreciation (prior years)'.</span></span>  
68. <span data-ttu-id="fbec7-193">Zadejte požadované hodnoty do pole Hlavní účet.</span><span class="sxs-lookup"><span data-stu-id="fbec7-193">In the Main account field, specify the desired values.</span></span>
69. <span data-ttu-id="fbec7-194">Zadejte požadované hodnoty do pole Protiúčet.</span><span class="sxs-lookup"><span data-stu-id="fbec7-194">In the Offset account field, specify the desired values.</span></span>
70. <span data-ttu-id="fbec7-195">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="fbec7-195">Click Add.</span></span>
71. <span data-ttu-id="fbec7-196">V poli Kniha zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="fbec7-196">In the Book field, enter or select a value.</span></span>
72. <span data-ttu-id="fbec7-197">V poli Zaúčtovat hodnotu vyberte hodnotu Odpis (tento rok).</span><span class="sxs-lookup"><span data-stu-id="fbec7-197">In the Post value field, select 'Depreciation (this year)'.</span></span>
73. <span data-ttu-id="fbec7-198">Zadejte požadované hodnoty do pole Hlavní účet.</span><span class="sxs-lookup"><span data-stu-id="fbec7-198">In the Main account field, specify the desired values.</span></span>
74. <span data-ttu-id="fbec7-199">Zadejte požadované hodnoty do pole Protiúčet.</span><span class="sxs-lookup"><span data-stu-id="fbec7-199">In the Offset account field, specify the desired values.</span></span>
75. <span data-ttu-id="fbec7-200">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="fbec7-200">Click Add.</span></span>
76. <span data-ttu-id="fbec7-201">V poli Kniha zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="fbec7-201">In the Book field, enter or select a value.</span></span>
77. <span data-ttu-id="fbec7-202">V poli Zaúčtovat hodnotu vyberte hodnotu Opravy odpisů (předchozí roky).</span><span class="sxs-lookup"><span data-stu-id="fbec7-202">In the Post value field, select 'Depreciation adjustments (prior years)'.</span></span>
78. <span data-ttu-id="fbec7-203">Zadejte požadované hodnoty do pole Hlavní účet.</span><span class="sxs-lookup"><span data-stu-id="fbec7-203">In the Main account field, specify the desired values.</span></span>
79. <span data-ttu-id="fbec7-204">Zadejte požadované hodnoty do pole Protiúčet.</span><span class="sxs-lookup"><span data-stu-id="fbec7-204">In the Offset account field, specify the desired values.</span></span>
80. <span data-ttu-id="fbec7-205">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="fbec7-205">Click Add.</span></span>
81. <span data-ttu-id="fbec7-206">V poli Kniha zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="fbec7-206">In the Book field, enter or select a value.</span></span>
82. <span data-ttu-id="fbec7-207">V poli Zaúčtovat hodnotu vyberte hodnotu Opravy odpisů (tento rok).</span><span class="sxs-lookup"><span data-stu-id="fbec7-207">In the Post value field, select 'Depreciation adjustments (this year)'.</span></span>
83. <span data-ttu-id="fbec7-208">Zadejte požadované hodnoty do pole Hlavní účet.</span><span class="sxs-lookup"><span data-stu-id="fbec7-208">In the Main account field, specify the desired values.</span></span>
84. <span data-ttu-id="fbec7-209">Zadejte požadované hodnoty do pole Protiúčet.</span><span class="sxs-lookup"><span data-stu-id="fbec7-209">In the Offset account field, specify the desired values.</span></span>
85. <span data-ttu-id="fbec7-210">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="fbec7-210">Click Add.</span></span>
86. <span data-ttu-id="fbec7-211">V poli Kniha zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="fbec7-211">In the Book field, enter or select a value.</span></span>
87. <span data-ttu-id="fbec7-212">V poli Zaúčtovat hodnotu vyberte Zůstatková účetní hodnota.</span><span class="sxs-lookup"><span data-stu-id="fbec7-212">In the Post value field, select 'Net book value'.</span></span>
88. <span data-ttu-id="fbec7-213">Zadejte požadované hodnoty do pole Hlavní účet.</span><span class="sxs-lookup"><span data-stu-id="fbec7-213">In the Main account field, specify the desired values.</span></span>
89. <span data-ttu-id="fbec7-214">Zadejte požadované hodnoty do pole Protiúčet.</span><span class="sxs-lookup"><span data-stu-id="fbec7-214">In the Offset account field, specify the desired values.</span></span>


