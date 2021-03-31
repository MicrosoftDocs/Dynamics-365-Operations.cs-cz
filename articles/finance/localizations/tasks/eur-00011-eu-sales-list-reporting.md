---
title: EUR-00011 Nastavení sestav souhrnného hlášení EU
description: Tato úloha vás provede přehledem o předpokladech pro vytváření souhrnného hlášení (EU).
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionRepositoryTable, ERSolutionImport, SysQueryForm, SysQueryFieldLookUp,  TaxTable, TaxGroup, TaxItemGroup, TaxCountryRegionParameters, TaxVATNumTable, IntrastatParameters, CustTable, DirPartyQuickCreateForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a0ce458697fd61aabddcbf844dd0b2afbe3aa1c0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5228004"
---
# <a name="eur-00011-set-up-eu-sales-list-reporting"></a><span data-ttu-id="6ba56-103">EUR-00011 Nastavení sestav souhrnného hlášení EU</span><span class="sxs-lookup"><span data-stu-id="6ba56-103">EUR-00011 Set up EU sales list reporting</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6ba56-104">Tato úloha vás provede přehledem o předpokladech pro vytváření souhrnného hlášení (EU).</span><span class="sxs-lookup"><span data-stu-id="6ba56-104">This task walks you through an overview of the prerequisites required for EU sales list reporting.</span></span> <span data-ttu-id="6ba56-105">Další informace o výkazu se seznamem prodeje v EU včetně případných požadovaných předpokladů naleznete v nápovědě.</span><span class="sxs-lookup"><span data-stu-id="6ba56-105">For more information about EU Sales list reporting, including required prerequisites, refer to Help.</span></span>

<span data-ttu-id="6ba56-106">Úkol se vztahuje na všechny evropské země/oblasti.</span><span class="sxs-lookup"><span data-stu-id="6ba56-106">This task applies to all European countries/regions.</span></span> <span data-ttu-id="6ba56-107">Průvodce byl vytvořen použitím ukázkových dat společnosti DEMF a následně Německa jako příklad pro domácí zemi nebo oblast.</span><span class="sxs-lookup"><span data-stu-id="6ba56-107">The guide was created using the demo data company DEMF and consequently Germany as an exemplar domestic country/region.</span></span> <span data-ttu-id="6ba56-108">Průvodce také využívá Portugalsko jako příklad země nebo oblasti EU.</span><span class="sxs-lookup"><span data-stu-id="6ba56-108">The guide also uses Portugal as an exemplar EU country/region.</span></span>

<span data-ttu-id="6ba56-109">Tyto úkoly jsou určeny pro správce systému.</span><span class="sxs-lookup"><span data-stu-id="6ba56-109">These tasks are intended for system administrators.</span></span>


## <a name="import-electronic-reporting-configurations-for-eu-sales-list-reporting"></a><span data-ttu-id="6ba56-110">Import elektronického vykazování konfigurace pro vytváření souhrnného hlášení EU</span><span class="sxs-lookup"><span data-stu-id="6ba56-110">Import electronic reporting configurations for EU sales list reporting</span></span>
1. <span data-ttu-id="6ba56-111">Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="6ba56-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="6ba56-112">Klikněte na možnost Nastavit jako aktivní.</span><span class="sxs-lookup"><span data-stu-id="6ba56-112">Click Set active.</span></span>
3. <span data-ttu-id="6ba56-113">Klikněte na možnost Úložiště.</span><span class="sxs-lookup"><span data-stu-id="6ba56-113">Click Repositories.</span></span>
4. <span data-ttu-id="6ba56-114">Klikněte na možnost Otevřít.</span><span class="sxs-lookup"><span data-stu-id="6ba56-114">Click Open.</span></span>
5. <span data-ttu-id="6ba56-115">V podokně akcí klikněte na Možnosti.</span><span class="sxs-lookup"><span data-stu-id="6ba56-115">On the Action Pane, click Options.</span></span>
6. <span data-ttu-id="6ba56-116">Klepněte na možnost Rozšířený filtr či řazení.</span><span class="sxs-lookup"><span data-stu-id="6ba56-116">Click Advanced Filter/Sort.</span></span>
7. <span data-ttu-id="6ba56-117">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="6ba56-117">Click Add.</span></span>
8. <span data-ttu-id="6ba56-118">V poli Pole vyberte „Název konfigurace“.</span><span class="sxs-lookup"><span data-stu-id="6ba56-118">In the Field field, select 'Configuration name'.</span></span>
9. <span data-ttu-id="6ba56-119">Do pole kritéria zadejte hodnotu „Souhrnné hlášení EU (DE)“.</span><span class="sxs-lookup"><span data-stu-id="6ba56-119">In the Criteria field, type 'EU Sales list (DE)'.</span></span>
10. <span data-ttu-id="6ba56-120">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="6ba56-120">Click OK.</span></span>
11. <span data-ttu-id="6ba56-121">Klepněte na tlačítko Importovat.</span><span class="sxs-lookup"><span data-stu-id="6ba56-121">Click Import.</span></span>
12. <span data-ttu-id="6ba56-122">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="6ba56-122">Click Yes.</span></span>
13. <span data-ttu-id="6ba56-123">V podokně akcí klikněte na Možnosti.</span><span class="sxs-lookup"><span data-stu-id="6ba56-123">On the Action Pane, click Options.</span></span>
14. <span data-ttu-id="6ba56-124">Klepněte na možnost Rozšířený filtr či řazení.</span><span class="sxs-lookup"><span data-stu-id="6ba56-124">Click Advanced Filter/Sort.</span></span>
15. <span data-ttu-id="6ba56-125">Klepněte na možnost Resetovat.</span><span class="sxs-lookup"><span data-stu-id="6ba56-125">Click Reset.</span></span>
16. <span data-ttu-id="6ba56-126">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="6ba56-126">Click Add.</span></span>
17. <span data-ttu-id="6ba56-127">V poli Pole vyberte „Název konfigurace“.</span><span class="sxs-lookup"><span data-stu-id="6ba56-127">In the Field field, select 'Configuration name'.</span></span>
18. <span data-ttu-id="6ba56-128">Do pole kritéria zadejte hodnotu „Souhrnné hlášení EU podle řádků“.</span><span class="sxs-lookup"><span data-stu-id="6ba56-128">In the Criteria field, type 'EU Sales list by rows report'.</span></span>
19. <span data-ttu-id="6ba56-129">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="6ba56-129">Click OK.</span></span>
20. <span data-ttu-id="6ba56-130">Klepněte na tlačítko Importovat.</span><span class="sxs-lookup"><span data-stu-id="6ba56-130">Click Import.</span></span>
21. <span data-ttu-id="6ba56-131">Klepněte na tlačítko Ano.</span><span class="sxs-lookup"><span data-stu-id="6ba56-131">Click Yes.</span></span>

## <a name="set-up-sales-tax-codes-for-eu-sales-list-reporting"></a><span data-ttu-id="6ba56-132">Nastavte kódy DPH pro vytváření souhrnného hlášení EU</span><span class="sxs-lookup"><span data-stu-id="6ba56-132">Set up sales tax codes for EU sales list reporting</span></span>
1. <span data-ttu-id="6ba56-133">Přejděte na Daň > Nepřímé daně > DPH > Kódy DPH.</span><span class="sxs-lookup"><span data-stu-id="6ba56-133">Go to Tax > Indirect taxes > Sales tax > Sales tax codes.</span></span>
2. <span data-ttu-id="6ba56-134">Použijte rychlý filtr k filtrování v poli Kód prodejní daně s hodnotou „DPH19“.</span><span class="sxs-lookup"><span data-stu-id="6ba56-134">Use the Quick Filter to filter on the Sales tax code field with a value of 'VAT19'.</span></span>
3. <span data-ttu-id="6ba56-135">Rozbalte část nastavení sestavy.</span><span class="sxs-lookup"><span data-stu-id="6ba56-135">Expand the Report setup section.</span></span>
    * <span data-ttu-id="6ba56-136">Ověřte, zda je vyloučený výběr nastaven na hodnotu Ne.</span><span class="sxs-lookup"><span data-stu-id="6ba56-136">Verify that the Excluded selection is set to No.</span></span>  
    * <span data-ttu-id="6ba56-137">Pro změnu tohoto nastavení může být nutné odemknout průvodce úkolem.</span><span class="sxs-lookup"><span data-stu-id="6ba56-137">You may need to unlock the task guide to change this setting.</span></span>  

## <a name="set-up-sales-tax-groups-for-eu-sales-list-reporting"></a><span data-ttu-id="6ba56-138">Nastavte skupiny DPH pro vytváření souhrnného hlášení EU</span><span class="sxs-lookup"><span data-stu-id="6ba56-138">Set up sales tax groups for EU sales list reporting</span></span>
1. <span data-ttu-id="6ba56-139">Přejděte na Daň > Nepřímé daně > DPH > Skupiny DPH.</span><span class="sxs-lookup"><span data-stu-id="6ba56-139">Go to Tax > Indirect taxes > Sales tax > Sales tax groups.</span></span>
2. <span data-ttu-id="6ba56-140">Použijte rychlý filtr k filtrování v poli Skupina prodejní daně s hodnotou „AR-DOM“.</span><span class="sxs-lookup"><span data-stu-id="6ba56-140">Use the Quick Filter to filter on the Sales tax group field with a value of 'AR-DOM'.</span></span>
3. <span data-ttu-id="6ba56-141">Klikněte na možnost Upravit.</span><span class="sxs-lookup"><span data-stu-id="6ba56-141">Click Edit.</span></span>
4. <span data-ttu-id="6ba56-142">Rozbalte sekci Nastavení.</span><span class="sxs-lookup"><span data-stu-id="6ba56-142">Expand the Setup section.</span></span>
5. <span data-ttu-id="6ba56-143">V seznamu vyberte první řádek.</span><span class="sxs-lookup"><span data-stu-id="6ba56-143">In the list, select the first row.</span></span>
6. <span data-ttu-id="6ba56-144">Zaškrtněte políčko Osvobozené od daně.</span><span class="sxs-lookup"><span data-stu-id="6ba56-144">Select the Exempt check box.</span></span>
7. <span data-ttu-id="6ba56-145">V seznamu vyberte druhý řádek.</span><span class="sxs-lookup"><span data-stu-id="6ba56-145">In the list, select the second row.</span></span>
8. <span data-ttu-id="6ba56-146">Zaškrtněte políčko Osvobozené od daně.</span><span class="sxs-lookup"><span data-stu-id="6ba56-146">Select the Exempt check box.</span></span>
9. <span data-ttu-id="6ba56-147">V seznamu vyberte třetí řádek.</span><span class="sxs-lookup"><span data-stu-id="6ba56-147">In the list, select the third row.</span></span>
10. <span data-ttu-id="6ba56-148">Zaškrtněte políčko Osvobozené od daně.</span><span class="sxs-lookup"><span data-stu-id="6ba56-148">Select the Exempt check box.</span></span>

## <a name="set-up-item-sales-tax-groups-for-eu-sales-list-reporting"></a><span data-ttu-id="6ba56-149">Nastavte položku skupin DPH pro vytváření souhrnného hlášení EU</span><span class="sxs-lookup"><span data-stu-id="6ba56-149">Set up item sales tax groups for EU sales list reporting</span></span>
1. <span data-ttu-id="6ba56-150">Přejděte na Daň > Nepřímé daně > DPH > Skupiny prodejní daně položky.</span><span class="sxs-lookup"><span data-stu-id="6ba56-150">Go to Tax > Indirect taxes > Sales tax > Item sales tax groups.</span></span>
2. <span data-ttu-id="6ba56-151">Použijte rychlý filtr k filtrování v poli Položka prodejní daně s hodnotou „FULL“.</span><span class="sxs-lookup"><span data-stu-id="6ba56-151">Use the Quick Filter to filter on the Item sales tax group field with a value of 'FULL '.</span></span>
    * <span data-ttu-id="6ba56-152">Ověřte, zda je výběr Typ vykazování nastaven na hodnotu „Položka“.</span><span class="sxs-lookup"><span data-stu-id="6ba56-152">Verify that the Reporting type selection is set to 'Item'.</span></span>  
    * <span data-ttu-id="6ba56-153">Pro změnu hodnoty v tomto poli může být nutné odemknout průvodce úkolem.</span><span class="sxs-lookup"><span data-stu-id="6ba56-153">You may need to unlock the task guide to change the value in this field.</span></span>  
3. <span data-ttu-id="6ba56-154">Použijte rychlý filtr k filtrování v poli Položka prodejní daně s hodnotou „RED“.</span><span class="sxs-lookup"><span data-stu-id="6ba56-154">Use the Quick Filter to filter on the Item sales tax group field with a value of 'RED '.</span></span>
    * <span data-ttu-id="6ba56-155">Ověřte, zda je výběr Typ vykazování nastaven na hodnotu „Servis“.</span><span class="sxs-lookup"><span data-stu-id="6ba56-155">Verify that the Reporting type selection is set to 'Service'.</span></span>  
    * <span data-ttu-id="6ba56-156">Pro změnu hodnoty v tomto poli může být nutné odemknout průvodce úkolem.</span><span class="sxs-lookup"><span data-stu-id="6ba56-156">You may need to unlock the task guide to change the value in this field.</span></span>  

## <a name="set-up-countryregion-parameters-for-eu-sales-list-reporting"></a><span data-ttu-id="6ba56-157">Nastavte parametry země/oblasti pro vytváření souhrnného hlášení EU</span><span class="sxs-lookup"><span data-stu-id="6ba56-157">Set up country/region parameters for EU sales list reporting</span></span>
1. <span data-ttu-id="6ba56-158">Přejděte na Daň > Nastavení > DPH > Parametry země/oblasti.</span><span class="sxs-lookup"><span data-stu-id="6ba56-158">Go to Tax > Setup > Sales tax > Country/region parameters.</span></span>
2. <span data-ttu-id="6ba56-159">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="6ba56-159">Click New.</span></span>
3. <span data-ttu-id="6ba56-160">V poli Země/oblast zadejte „PRT“.</span><span class="sxs-lookup"><span data-stu-id="6ba56-160">In the Country/region field, type 'PRT'.</span></span>
4. <span data-ttu-id="6ba56-161">V poli Prodejní daň zadejte „PT“.</span><span class="sxs-lookup"><span data-stu-id="6ba56-161">In the Sales tax field, type 'PT'.</span></span>

## <a name="create-tax-exempt-numbers"></a><span data-ttu-id="6ba56-162">Vytvořit čísla osvobození od daně</span><span class="sxs-lookup"><span data-stu-id="6ba56-162">Create tax exempt numbers</span></span>
1. <span data-ttu-id="6ba56-163">Přejděte na Daň > Nastavení > DPH > DIČ.</span><span class="sxs-lookup"><span data-stu-id="6ba56-163">Go to Tax > Setup > Sales tax > Tax exempt numbers.</span></span>
2. <span data-ttu-id="6ba56-164">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="6ba56-164">Click New.</span></span>
3. <span data-ttu-id="6ba56-165">V poli Země/oblast zadejte „PRT“.</span><span class="sxs-lookup"><span data-stu-id="6ba56-165">In the Country/region field, type 'PRT'.</span></span>
4. <span data-ttu-id="6ba56-166">Do pole DIČ zadejte „PT12345“.</span><span class="sxs-lookup"><span data-stu-id="6ba56-166">In the Tax exempt number field, type 'PT12345'.</span></span>

## <a name="set-up-eu-sales-list-reporting-parameters"></a><span data-ttu-id="6ba56-167">Nastavit parametry sestav souhrnného hlášení EU</span><span class="sxs-lookup"><span data-stu-id="6ba56-167">Set up EU sales list reporting parameters</span></span>
1. <span data-ttu-id="6ba56-168">Přejděte na Daň > Nastavení > Zahraniční obchod > Parametry zahraničního obchodu.</span><span class="sxs-lookup"><span data-stu-id="6ba56-168">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
2. <span data-ttu-id="6ba56-169">Klepněte na kartu souhrnného hlášení EU.</span><span class="sxs-lookup"><span data-stu-id="6ba56-169">Click the EU sales list tab.</span></span>
3. <span data-ttu-id="6ba56-170">Vyberte možnost Ano v poli převodu nákupů.</span><span class="sxs-lookup"><span data-stu-id="6ba56-170">Select Yes in the Transfer purchases field.</span></span>
4. <span data-ttu-id="6ba56-171">Rozbalte položku Pravidla zaokrouhlování.</span><span class="sxs-lookup"><span data-stu-id="6ba56-171">Expand the Rounding rules section.</span></span>
5. <span data-ttu-id="6ba56-172">Nastavit Pravidlo zaokrouhlování na „0,1“.</span><span class="sxs-lookup"><span data-stu-id="6ba56-172">Set Rounding rule to '0.1'.</span></span>
6. <span data-ttu-id="6ba56-173">Vyberte možnost Ano v poli Použít minimální hodnotu.</span><span class="sxs-lookup"><span data-stu-id="6ba56-173">Select Yes in the Use minimum value field.</span></span>
7. <span data-ttu-id="6ba56-174">Do pole Počet desetinných míst zadejte „2“.</span><span class="sxs-lookup"><span data-stu-id="6ba56-174">In the Number of decimals field, enter '2'.</span></span>
8. <span data-ttu-id="6ba56-175">Rozbalte část Elektronické výkaznictví.</span><span class="sxs-lookup"><span data-stu-id="6ba56-175">Expand the Electronic reporting section.</span></span>
9. <span data-ttu-id="6ba56-176">V poli Mapování formátu souboru vyberte „Souhrnné hlášení EU (DE)“.</span><span class="sxs-lookup"><span data-stu-id="6ba56-176">In the File format mapping field, select 'EU Sales list (DE)'.</span></span>
10. <span data-ttu-id="6ba56-177">V poli Mapování formátu sestavy vyberte „Souhrnné hlášení EU podle řádků“.</span><span class="sxs-lookup"><span data-stu-id="6ba56-177">In the Report format mapping field, select 'EU Sales list by rows report'.</span></span>
11. <span data-ttu-id="6ba56-178">Klepněte na kartu vlastností Země/oblasti.</span><span class="sxs-lookup"><span data-stu-id="6ba56-178">Click the Country/region properties tab.</span></span>
    * <span data-ttu-id="6ba56-179">Zkontrolujte, že pole typu Země/oblast je nastaveno na hodnotu „Domácí“ pro zemi nebo oblast Německo.</span><span class="sxs-lookup"><span data-stu-id="6ba56-179">Verify that the Country/region type field is set to 'Domestic' for Country/region DEU.</span></span>  
    * <span data-ttu-id="6ba56-180">Pro změnu hodnoty v tomto poli může být nutné odemknout průvodce úkolem.</span><span class="sxs-lookup"><span data-stu-id="6ba56-180">You may need to unlock the task guide to change the value in this field.</span></span>  
12. <span data-ttu-id="6ba56-181">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="6ba56-181">Click New.</span></span>
13. <span data-ttu-id="6ba56-182">V poli Země/oblast zadejte „PRT“.</span><span class="sxs-lookup"><span data-stu-id="6ba56-182">In the Country/region field, type 'PRT'.</span></span>
14. <span data-ttu-id="6ba56-183">V poli Kód Intrastat zadejte „PT“.</span><span class="sxs-lookup"><span data-stu-id="6ba56-183">In the Intrastat code field, type 'PT'.</span></span>
15. <span data-ttu-id="6ba56-184">Do zadávacího pole Země/oblast vyberte položku „EU“.</span><span class="sxs-lookup"><span data-stu-id="6ba56-184">In the Country/region type field, select 'EU'.</span></span>
16. <span data-ttu-id="6ba56-185">Klikněte na kartu Číselné řady.</span><span class="sxs-lookup"><span data-stu-id="6ba56-185">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="6ba56-186">Ověřte, zda je zadán kód číselné řady pro odkaz „Souhrnného hlášení EU“.</span><span class="sxs-lookup"><span data-stu-id="6ba56-186">Verify that a Number sequence code is specified for the Reference 'EU sales list'.</span></span>  

## <a name="create-a-customer-for-eu-sales-list-reporting-demo-purposes"></a><span data-ttu-id="6ba56-187">Vytvořit odběratele pro účely ukázky souhrnného hlášení EU</span><span class="sxs-lookup"><span data-stu-id="6ba56-187">Create a customer for EU sales list reporting demo purposes</span></span>
1. <span data-ttu-id="6ba56-188">Přejděte na Pohledávky > Zákazníci > Všichni odběratelé.</span><span class="sxs-lookup"><span data-stu-id="6ba56-188">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="6ba56-189">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="6ba56-189">Click New.</span></span>
3. <span data-ttu-id="6ba56-190">V poli Účet odběratele zadejte „PRT-001“.</span><span class="sxs-lookup"><span data-stu-id="6ba56-190">In the Customer account field, type 'PRT-001'.</span></span>
4. <span data-ttu-id="6ba56-191">Do pole Název zadejte „Zákazník z Portugalska“.</span><span class="sxs-lookup"><span data-stu-id="6ba56-191">In the Name field, type 'A customer from Portugal'.</span></span>
5. <span data-ttu-id="6ba56-192">V poli Skupina odběratelů vyberte „10“.</span><span class="sxs-lookup"><span data-stu-id="6ba56-192">In the Customer group field, select '10'.</span></span>
6. <span data-ttu-id="6ba56-193">V poli Skupina DPH vyberte položku „AR-DOM“.</span><span class="sxs-lookup"><span data-stu-id="6ba56-193">In the Sales tax group field, select 'AR-DOM'.</span></span>
7. <span data-ttu-id="6ba56-194">Do pole DIČ vyberte „PT12345“.</span><span class="sxs-lookup"><span data-stu-id="6ba56-194">In the Tax exempt number field, select 'PT12345'.</span></span>
8. <span data-ttu-id="6ba56-195">V poli Země/oblast zadejte „PRT“.</span><span class="sxs-lookup"><span data-stu-id="6ba56-195">In the Country/region field, type 'PRT'.</span></span>
9. <span data-ttu-id="6ba56-196">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="6ba56-196">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]