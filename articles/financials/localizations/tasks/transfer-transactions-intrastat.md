--- 
title: "Převod transakcí do systému Intrastat"
description: "Tento postup vás provede nastavením parametrů systému Intrastat a převodem transakcí do systému Intrastat."
author: Anasyash
manager: AnnBe
ms.date: 06/09/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: anasyash
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: a968bf4ec263f3b7c2b4e5b215fe782d4b54dd8e
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---
# <a name="transfer-transactions-to-the-intrastat"></a><span data-ttu-id="63965-103">Převod transakcí do systému Intrastat</span><span class="sxs-lookup"><span data-stu-id="63965-103">Transfer transactions to the Intrastat</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="63965-104">Tento postup vás provede nastavením parametrů systému Intrastat a převodem transakcí do systému Intrastat.</span><span class="sxs-lookup"><span data-stu-id="63965-104">This procedure walks you through how to set up Intrastat parameters and transfer transactions to Intrastat.</span></span> <span data-ttu-id="63965-105">Tato procedura byla vytvořena pomocí ukázkových dat společnosti DEMF.</span><span class="sxs-lookup"><span data-stu-id="63965-105">This procedure was created using the demo data company DEMF.</span></span>


## <a name="create-new-and-update-existing-commodity-code"></a><span data-ttu-id="63965-106">Vytvoření nového a aktualizace existujícího kódu komodity</span><span class="sxs-lookup"><span data-stu-id="63965-106">Create new and update existing commodity code</span></span>
1. <span data-ttu-id="63965-107">Přejděte do nabídky Řízení informací o produktech > Nastavení > Kategorie a atributy > Hierarchie kategorií.</span><span class="sxs-lookup"><span data-stu-id="63965-107">Go to Product information management > Setup > Categories and attributes > Category hierarchies.</span></span>
2. <span data-ttu-id="63965-108">V seznamu vyhledejte nebo vyberte záznam, "Kódy komodit systému Intrastat".</span><span class="sxs-lookup"><span data-stu-id="63965-108">In the list, find or select the record "Intrastat commodity codes."</span></span>
3. <span data-ttu-id="63965-109">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="63965-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="63965-110">Ve stromovém zobrazení vyberte „záznam“.</span><span class="sxs-lookup"><span data-stu-id="63965-110">In the tree, select 'a record'.</span></span>
    * <span data-ttu-id="63965-111">Vyberte například „Intrastat\Reproduktor“.</span><span class="sxs-lookup"><span data-stu-id="63965-111">For example, select 'Intrastat\Speaker'.</span></span>  
5. <span data-ttu-id="63965-112">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="63965-112">Click Edit.</span></span>
6. <span data-ttu-id="63965-113">Rozbalte oddíl Zahraniční obchod.</span><span class="sxs-lookup"><span data-stu-id="63965-113">Expand the Foreign trade section.</span></span>
7. <span data-ttu-id="63965-114">V poli Dodatečné jednotky zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="63965-114">In the Additional units field, enter or select a value.</span></span>
    * <span data-ttu-id="63965-115">Vyberte například „ks“.</span><span class="sxs-lookup"><span data-stu-id="63965-115">For example, choose 'pcs'.</span></span>  
8. <span data-ttu-id="63965-116">V poli Hmotnost nelze použít vyberte možnost Ano.</span><span class="sxs-lookup"><span data-stu-id="63965-116">Select Yes in the Weight not applicable field.</span></span>
9. <span data-ttu-id="63965-117">Ve stromovém zobrazení vyberte Intrastat.</span><span class="sxs-lookup"><span data-stu-id="63965-117">In the tree, select 'Intrastat'.</span></span>
10. <span data-ttu-id="63965-118">Klikněte na možnost Nový uzel kategorie.</span><span class="sxs-lookup"><span data-stu-id="63965-118">Click New category node.</span></span>
11. <span data-ttu-id="63965-119">Do pole Název zadejte název komodity.</span><span class="sxs-lookup"><span data-stu-id="63965-119">In the Name field, enter the name of commodity.</span></span>
    * <span data-ttu-id="63965-120">Například zadejte „Jiné zboží“.</span><span class="sxs-lookup"><span data-stu-id="63965-120">For example, type 'Other commodity'.</span></span>  
12. <span data-ttu-id="63965-121">V poli Kód zadejte kód komodity.</span><span class="sxs-lookup"><span data-stu-id="63965-121">In the Code field, enter the commodity code.</span></span>
    * <span data-ttu-id="63965-122">Zadejte například 995 00 00.</span><span class="sxs-lookup"><span data-stu-id="63965-122">For example, type '995 00 00'.</span></span>  
13. <span data-ttu-id="63965-123">Do pole Popisný název zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="63965-123">In the Friendly name field, type a value.</span></span>
    * <span data-ttu-id="63965-124">Zadejte například Jiné.</span><span class="sxs-lookup"><span data-stu-id="63965-124">For example, type 'Other'.</span></span>  
14. <span data-ttu-id="63965-125">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="63965-125">Click Save.</span></span>
15. <span data-ttu-id="63965-126">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="63965-126">Close the page.</span></span>

## <a name="assign-commodity-code-to-product-hierarchy-and-released-product"></a><span data-ttu-id="63965-127">Přiřazení kódu komodity k hierarchii produktů a uvolněným produktům</span><span class="sxs-lookup"><span data-stu-id="63965-127">Assign commodity code to product hierarchy and released product</span></span>
1. <span data-ttu-id="63965-128">Použijte rychlý filtr pro hledání záznamů.</span><span class="sxs-lookup"><span data-stu-id="63965-128">Use the Quick Filter to find records.</span></span> <span data-ttu-id="63965-129">Můžete například filtrovat v poli Jméno pomocí hodnoty „prodeje“.</span><span class="sxs-lookup"><span data-stu-id="63965-129">For example, filter on the Name field with a value of 'sales'.</span></span>
2. <span data-ttu-id="63965-130">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="63965-130">In the list, click the link in the selected row.</span></span>
3. <span data-ttu-id="63965-131">Ve stromovém zobrazení rozbalte uzel kategorie.</span><span class="sxs-lookup"><span data-stu-id="63965-131">In the tree, expand 'a category node'.</span></span>
    * <span data-ttu-id="63965-132">Například rozbalte "Prodejní hierarchie\Domácí audio".</span><span class="sxs-lookup"><span data-stu-id="63965-132">For example, expand 'Sales hierarchy\Home audio'.</span></span>  
4. <span data-ttu-id="63965-133">Ve stromovém zobrazení vyberte kategorii, ke které chcete přiřadit kód komodity.</span><span class="sxs-lookup"><span data-stu-id="63965-133">In the tree, select 'the category to assign to the commodity code'.</span></span>
    * <span data-ttu-id="63965-134">Například vyberte "Prodejní hierarchie\Domácí audio\Reproduktory".</span><span class="sxs-lookup"><span data-stu-id="63965-134">For example, select 'Sales hierarchy\Home audio\Speakers.</span></span>  
5. <span data-ttu-id="63965-135">Rozbalte oddíl Kódy komodit.</span><span class="sxs-lookup"><span data-stu-id="63965-135">Expand the Commodity codes section.</span></span>
6. <span data-ttu-id="63965-136">Klepněte na možnost Přidat.</span><span class="sxs-lookup"><span data-stu-id="63965-136">Click Add.</span></span>
7. <span data-ttu-id="63965-137">V poli Vybrat hierarchii vyberte Intrastat.</span><span class="sxs-lookup"><span data-stu-id="63965-137">In the Select hierarchy field, select 'Intrastat'.</span></span>
8. <span data-ttu-id="63965-138">Vyhledejte ze seznamu kód komodity a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="63965-138">In the list, find and select the commodity code</span></span>
    * <span data-ttu-id="63965-139">Vyberte například „Reproduktor 920 20 34“.</span><span class="sxs-lookup"><span data-stu-id="63965-139">For example, select '920 20 34 Speaker'.</span></span>  
9. <span data-ttu-id="63965-140">Klepněte na SelectCodes.</span><span class="sxs-lookup"><span data-stu-id="63965-140">Click SelectCodes.</span></span>
10. <span data-ttu-id="63965-141">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="63965-141">Click OK.</span></span>
11. <span data-ttu-id="63965-142">Přejděte na možnosti Řízení informací o produktech > Produkty > Uvolněné produkty.</span><span class="sxs-lookup"><span data-stu-id="63965-142">Go to Product information management > Products > Released products.</span></span>
12. <span data-ttu-id="63965-143">V seznamu vyberte uvolněný produkt, který přiřadíte ke kódu komodity.</span><span class="sxs-lookup"><span data-stu-id="63965-143">In the list, choose the released product that you will assign to the commodity code.</span></span>
    * <span data-ttu-id="63965-144">Vyberte například „D0001“.</span><span class="sxs-lookup"><span data-stu-id="63965-144">For example, choose 'D0001'.</span></span>  
13. <span data-ttu-id="63965-145">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="63965-145">Click Edit.</span></span>
14. <span data-ttu-id="63965-146">Rozbalte oddíl Zahraniční obchod.</span><span class="sxs-lookup"><span data-stu-id="63965-146">Expand the Foreign trade section.</span></span>
15. <span data-ttu-id="63965-147">V poli Komodita zadejte kód komodity.</span><span class="sxs-lookup"><span data-stu-id="63965-147">In the Commodity field, enter the commodity code</span></span>
    * <span data-ttu-id="63965-148">Vyberte například hodnotu „Reproduktor 920 20 34“.</span><span class="sxs-lookup"><span data-stu-id="63965-148">For example, select value '920 20 34 Speaker'.</span></span>    
16. <span data-ttu-id="63965-149">V poli Procento nákladů zadejte požadované číslo.</span><span class="sxs-lookup"><span data-stu-id="63965-149">In the Charges percentage field, enter a number.</span></span>
    * <span data-ttu-id="63965-150">Například zadejte 3.</span><span class="sxs-lookup"><span data-stu-id="63965-150">For example, enter '3'.</span></span>  
17. <span data-ttu-id="63965-151">V poli Země/oblast zadejte nebo vyberte zemi nebo oblast původu</span><span class="sxs-lookup"><span data-stu-id="63965-151">In the Country/region field, enter or select a country or region of origin</span></span>
    * <span data-ttu-id="63965-152">Vyberte například AUT.</span><span class="sxs-lookup"><span data-stu-id="63965-152">For example, select 'AUT'.</span></span>  
18. <span data-ttu-id="63965-153">Rozbalte oblast Spravovat sklad.</span><span class="sxs-lookup"><span data-stu-id="63965-153">Expand the Manage inventory section.</span></span>
19. <span data-ttu-id="63965-154">V poli Čistá hmotnost zadejte hmotnost v kg.</span><span class="sxs-lookup"><span data-stu-id="63965-154">In the Net weight field, enter a weight in kg.</span></span>
    * <span data-ttu-id="63965-155">Například zadejte 2.5.</span><span class="sxs-lookup"><span data-stu-id="63965-155">For example, enter '2.5'.</span></span>  
20. <span data-ttu-id="63965-156">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="63965-156">Click Save.</span></span>

## <a name="set-up-intrastat-transaction-codes-and-foreign-trade-parameters"></a><span data-ttu-id="63965-157">Nastavení kódy transakcí systému Intrastat a parametrů zahraničního obchodu</span><span class="sxs-lookup"><span data-stu-id="63965-157">Set up Intrastat transaction codes and foreign trade parameters</span></span>
1. <span data-ttu-id="63965-158">Přejděte na Daň > Nastavení > Zahraniční obchod > Kódy transakcí</span><span class="sxs-lookup"><span data-stu-id="63965-158">Go to Tax > Setup > Foreign trade > Transaction codes</span></span>
2. <span data-ttu-id="63965-159">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="63965-159">Click New.</span></span>
3. <span data-ttu-id="63965-160">V poli Kód transakce zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="63965-160">In the Transaction code field, type a value.</span></span>
    * <span data-ttu-id="63965-161">Jako kód transakce použitý pro vrácení zadejte například hodnotu 21.</span><span class="sxs-lookup"><span data-stu-id="63965-161">For example, enter '21' for the transaction code used as return.</span></span>  
4. <span data-ttu-id="63965-162">Zadejte název kódu transakce do pole Název.</span><span class="sxs-lookup"><span data-stu-id="63965-162">In the Name field, type the name of transaction code.</span></span>
    * <span data-ttu-id="63965-163">Například zadejte Vrácení.</span><span class="sxs-lookup"><span data-stu-id="63965-163">For example, enter 'Return'.</span></span>  
5. <span data-ttu-id="63965-164">Vyberte volbu v poli Statistická částka.</span><span class="sxs-lookup"><span data-stu-id="63965-164">In the Statistical amount field, select an option.</span></span>
    * <span data-ttu-id="63965-165">Vyberte například možnost „Prázdné“, která značí, že Statistická hodnota uváděná pro transakce s kódem transakce „21“ bude vždy nula.</span><span class="sxs-lookup"><span data-stu-id="63965-165">For example, select 'Empty' which indicates that the Statistical value to be reported for transactions with Transaction code of "21" will always be zero.</span></span>  
6. <span data-ttu-id="63965-166">Přejděte na Daň > Nastavení > Zahraniční obchod > Parametry zahraničního obchodu.</span><span class="sxs-lookup"><span data-stu-id="63965-166">Go to Tax > Setup > Foreign trade > Foreign trade parameters</span></span>
7. <span data-ttu-id="63965-167">V poli Kód transakce zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="63965-167">In the Transaction code field, enter or select a value.</span></span>
    * <span data-ttu-id="63965-168">Vyberte například 11.</span><span class="sxs-lookup"><span data-stu-id="63965-168">For example, select '11'.</span></span>  
8. <span data-ttu-id="63965-169">V poli Dobropis zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="63965-169">In the Credit note field, enter or select a value.</span></span>
    * <span data-ttu-id="63965-170">Tato hodnota určuje fyzické vrácení.</span><span class="sxs-lookup"><span data-stu-id="63965-170">This value also identifies the physical return.</span></span> <span data-ttu-id="63965-171">Dobropis pro fyzické vrácení bude převeden do deníku Intrastat v opačném směru.</span><span class="sxs-lookup"><span data-stu-id="63965-171">The credit note for the physical return will be transferred in the Intrastat journal with opposite direction.</span></span> <span data-ttu-id="63965-172">Například vrácení pro „doručení“ je převedeno na expedici.</span><span class="sxs-lookup"><span data-stu-id="63965-172">For example, the return of arrival is transferred as dispatch.</span></span>   <span data-ttu-id="63965-173">V opačném případě je dobropis považován za opravu a je převeden ve stejném směru s opačným znaménkem.</span><span class="sxs-lookup"><span data-stu-id="63965-173">Otherwise, the credit note is considered a correction and is transferred with the same direction and opposite sign.</span></span> <span data-ttu-id="63965-174">Například korekce doručení je převedena jako přijetí se zápornou částkou, kde je aktivní příznak nastaven na "Oprava".</span><span class="sxs-lookup"><span data-stu-id="63965-174">For example, the correction of arrival is transferred as an arrival with negative amount and the active flag is set to "Correction".</span></span>  
9. <span data-ttu-id="63965-175">Rozbalte sekci Převod.</span><span class="sxs-lookup"><span data-stu-id="63965-175">Expand the Transfer section.</span></span>
10. <span data-ttu-id="63965-176">Vyberte možnost Ano v poli Položky s kódem zboží.</span><span class="sxs-lookup"><span data-stu-id="63965-176">Select Yes in the Items with commodity code field.</span></span>
    * <span data-ttu-id="63965-177">Vyberte tuto možnost, pokud chcete převést pouze transakce s přiřazeným kódem zboží.</span><span class="sxs-lookup"><span data-stu-id="63965-177">Select this option to transfer only the transactions with a commodity code assigned.</span></span> <span data-ttu-id="63965-178">Transakce bez kódu komodity nebudou převedeny do systému Intrastat.</span><span class="sxs-lookup"><span data-stu-id="63965-178">Transactions without a commodity code won't be transferred to Intrastat.</span></span>  
11. <span data-ttu-id="63965-179">V poli „Převést při splnění kritéria pro“ vyberte požadovanou možnost.</span><span class="sxs-lookup"><span data-stu-id="63965-179">In the Transfer when meeting criterion for field, select an option.</span></span>
    * <span data-ttu-id="63965-180">Vyberte například "Jedno z vybraných".</span><span class="sxs-lookup"><span data-stu-id="63965-180">For example, select 'One of the selected'.</span></span>  
12. <span data-ttu-id="63965-181">Rozbalte oddíl Hierarchie kódů komodit.</span><span class="sxs-lookup"><span data-stu-id="63965-181">Expand the Commodity code hierarchy section.</span></span>
13. <span data-ttu-id="63965-182">Klepněte na kartu vlastností Země/oblasti.</span><span class="sxs-lookup"><span data-stu-id="63965-182">Click the Country/region properties tab.</span></span>
14. <span data-ttu-id="63965-183">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="63965-183">Click New.</span></span>
15. <span data-ttu-id="63965-184">V poli Země/oblast zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="63965-184">In the Country/region field, enter or select a value.</span></span>
    * <span data-ttu-id="63965-185">Například vyberte hodnotu „FRA“.</span><span class="sxs-lookup"><span data-stu-id="63965-185">For example, select the value 'FRA'.</span></span>  
16. <span data-ttu-id="63965-186">V poli Kód Intrastat zadejte kód ISO pro danou zemi.</span><span class="sxs-lookup"><span data-stu-id="63965-186">In the Intrastat code field, enter the ISO code for the country.</span></span>
    * <span data-ttu-id="63965-187">Zadejte například FR.</span><span class="sxs-lookup"><span data-stu-id="63965-187">For example, type 'FR'.</span></span>  
17. <span data-ttu-id="63965-188">Do zadávacího pole Země/oblast vyberte položku „EU“.</span><span class="sxs-lookup"><span data-stu-id="63965-188">In the Country/region type field, select 'EU'.</span></span>
18. <span data-ttu-id="63965-189">Klikněte na kartu Číselné řady.</span><span class="sxs-lookup"><span data-stu-id="63965-189">Click the Number sequences tab.</span></span>

## <a name="set-up-modes-of-delivery-and-rules-for-including-charges-in-intrastat"></a><span data-ttu-id="63965-190">Nastavení způsobů dodání a pravidel pro zahrnutí nákladů v systému Intrastat</span><span class="sxs-lookup"><span data-stu-id="63965-190">Set up Modes of delivery and rules for including charges in Intrastat</span></span>
1. <span data-ttu-id="63965-191">Přejděte na Prodej a marketing > Nastavení > Distribuce > Způsoby dodání</span><span class="sxs-lookup"><span data-stu-id="63965-191">Go to Sales and marketing > Setup > Distribution > Modes of delivery</span></span>
2. <span data-ttu-id="63965-192">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="63965-192">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="63965-193">Vyberte například 20 Air.</span><span class="sxs-lookup"><span data-stu-id="63965-193">For example, select '20 Air'.</span></span>  
3. <span data-ttu-id="63965-194">Rozbalte oddíl Zahraniční obchod.</span><span class="sxs-lookup"><span data-stu-id="63965-194">Expand the Foreign trade section.</span></span>
4. <span data-ttu-id="63965-195">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="63965-195">Click Edit.</span></span>
5. <span data-ttu-id="63965-196">V poli Přeprava zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="63965-196">In the Transport field, enter or select a value.</span></span>
    * <span data-ttu-id="63965-197">Vyberte například 02.</span><span class="sxs-lookup"><span data-stu-id="63965-197">For example, select '02'.</span></span>  
6. <span data-ttu-id="63965-198">Přejděte na Pohledávky > Nastavení poplatků > Kód nákladů.</span><span class="sxs-lookup"><span data-stu-id="63965-198">Go to Accounts receivable > Charges setup > Charges code.</span></span>
7. <span data-ttu-id="63965-199">Použijte rychlý filtr pro hledání záznamů.</span><span class="sxs-lookup"><span data-stu-id="63965-199">Use the Quick Filter to find records.</span></span> <span data-ttu-id="63965-200">Můžete například filtrovat v poli Kód nákladů pomocí hodnoty „dopravné“.</span><span class="sxs-lookup"><span data-stu-id="63965-200">For example, filter on the Charges code field with a value of 'freight'.</span></span>
8. <span data-ttu-id="63965-201">Rozbalte oddíl Zahraniční obchod.</span><span class="sxs-lookup"><span data-stu-id="63965-201">Expand the Foreign trade section.</span></span>
9. <span data-ttu-id="63965-202">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="63965-202">Click Edit.</span></span>
10. <span data-ttu-id="63965-203">Vyberte možnost Ano v poli Hodnota faktury Intrastat.</span><span class="sxs-lookup"><span data-stu-id="63965-203">Select Yes in the Intrastat invoice value field.</span></span>
    * <span data-ttu-id="63965-204">Částka bude přenesena do pole s náklady faktury a bude shrnuta s ohledem na převedenou částkou v poli Částka faktury.</span><span class="sxs-lookup"><span data-stu-id="63965-204">The amount will be transferred to the  Invoice charges field and will be summarized with the amount transferred in the Invoice amount field.</span></span>    <span data-ttu-id="63965-205">Vyberte možnost Ano v poli Statistická hodnota Intrastat, pokud je třeba soubor změn přenést do pole Statistické náklady a shrnout pomocí pole Statistická částka.</span><span class="sxs-lookup"><span data-stu-id="63965-205">Select Yes in the Intrastat statistical value field if the amount of changes need to be transferred to the field Statistical charges and summarized with Statistical amount.</span></span>  

## <a name="sell-products-for-eu-customers"></a><span data-ttu-id="63965-206">Prodej produktů odběratelům EU</span><span class="sxs-lookup"><span data-stu-id="63965-206">Sell products for EU customers</span></span>
1. <span data-ttu-id="63965-207">Přejděte na Pohledávky > Objednávky > Všechny prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="63965-207">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="63965-208">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="63965-208">Click New.</span></span>
3. <span data-ttu-id="63965-209">V poli Účet odběratele vyberte zákazníka EU.</span><span class="sxs-lookup"><span data-stu-id="63965-209">In the Customer account field, select an EU customer</span></span>
    * <span data-ttu-id="63965-210">Vyberte například "DE-012 Litware Retail".</span><span class="sxs-lookup"><span data-stu-id="63965-210">For example, select "DE-012 Litware Retail".</span></span>  
4. <span data-ttu-id="63965-211">Rozbalte sekci Dodání.</span><span class="sxs-lookup"><span data-stu-id="63965-211">Expand the Delivery section.</span></span>
5. <span data-ttu-id="63965-212">V poli Způsob dodání vyberte nebo zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="63965-212">In the Mode of delivery field, enter or select a value.</span></span>
    * <span data-ttu-id="63965-213">Vyberte například 20 Air.</span><span class="sxs-lookup"><span data-stu-id="63965-213">For example, select '20 Air'.</span></span>  
6. <span data-ttu-id="63965-214">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="63965-214">Click OK.</span></span>
7. <span data-ttu-id="63965-215">Umístěte kurzor na první řádek z řádků prodejní objednávky.</span><span class="sxs-lookup"><span data-stu-id="63965-215">Place the cursor on the first row of sales order lines.</span></span>
8. <span data-ttu-id="63965-216">V poli Číslo zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="63965-216">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="63965-217">Vyberte například D001.</span><span class="sxs-lookup"><span data-stu-id="63965-217">For example, select 'D001'.</span></span>  
9. <span data-ttu-id="63965-218">Rozbalte sekci Podrobnosti řádku.</span><span class="sxs-lookup"><span data-stu-id="63965-218">Expand the Line details section.</span></span>
10. <span data-ttu-id="63965-219">Klepněte na kartu zahraničního obchodu.</span><span class="sxs-lookup"><span data-stu-id="63965-219">Click the Foreign trade tab.</span></span>
    * <span data-ttu-id="63965-220">Přeprava je vyplněna automaticky z vybraného způsobu dodání.</span><span class="sxs-lookup"><span data-stu-id="63965-220">The transport is filled automatically from the chosen Mode of delivery.</span></span>  
11. <span data-ttu-id="63965-221">V poli Přístav zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="63965-221">In the Port field, enter or select a value.</span></span>
12. <span data-ttu-id="63965-222">Klepněte na tlačítko Finanční údaje.</span><span class="sxs-lookup"><span data-stu-id="63965-222">Click Financials.</span></span>
    * <span data-ttu-id="63965-223">Podle nastavení se tato částka zahrne v poli Hodnota faktury Intrastat.</span><span class="sxs-lookup"><span data-stu-id="63965-223">As per the settings, this amount will be included in Intrastat invoice value.</span></span>  
13. <span data-ttu-id="63965-224">Klikněte na položku Spravovat náklady.</span><span class="sxs-lookup"><span data-stu-id="63965-224">Click Maintain charges.</span></span>
14. <span data-ttu-id="63965-225">V poli Kód nákladů zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="63965-225">In the Charges code field, enter or select a value.</span></span>
    * <span data-ttu-id="63965-226">V tomto příkladu vyberte Dopravné.</span><span class="sxs-lookup"><span data-stu-id="63965-226">For example, select 'FREIGHT'.</span></span>  
15. <span data-ttu-id="63965-227">Zaškrtněte políčko Zachovat.</span><span class="sxs-lookup"><span data-stu-id="63965-227">Select the Keep check box.</span></span>
16. <span data-ttu-id="63965-228">Zadejte číslo do pole Hodnota nákladů.</span><span class="sxs-lookup"><span data-stu-id="63965-228">In the Charges value field, enter a number.</span></span>
    * <span data-ttu-id="63965-229">Například zadejte 10.</span><span class="sxs-lookup"><span data-stu-id="63965-229">For example, enter '10'.</span></span>  
17. <span data-ttu-id="63965-230">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="63965-230">Click Save.</span></span>
18. <span data-ttu-id="63965-231">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="63965-231">Close the page.</span></span>
19. <span data-ttu-id="63965-232">V podokně akcí klikněte na položku Faktura.</span><span class="sxs-lookup"><span data-stu-id="63965-232">On the Action Pane, click Invoice.</span></span>
20. <span data-ttu-id="63965-233">Klikněte na položku Faktura.</span><span class="sxs-lookup"><span data-stu-id="63965-233">Click Invoice.</span></span>
21. <span data-ttu-id="63965-234">Rozbalte sekci Parametry.</span><span class="sxs-lookup"><span data-stu-id="63965-234">Expand the Parameters section.</span></span>
22. <span data-ttu-id="63965-235">V poli Množství vyberte možnost Vše.</span><span class="sxs-lookup"><span data-stu-id="63965-235">In the Quantity field, select 'All'.</span></span>
23. <span data-ttu-id="63965-236">Rozbalte sekci Nastavení.</span><span class="sxs-lookup"><span data-stu-id="63965-236">Expand the Setup section.</span></span>
24. <span data-ttu-id="63965-237">Do pole Datum faktury zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="63965-237">In the Invoice date field, enter a date.</span></span>
    * <span data-ttu-id="63965-238">Například zadejte 2015-01-31.</span><span class="sxs-lookup"><span data-stu-id="63965-238">For example, enter '2015-01-31'.</span></span>  
25. <span data-ttu-id="63965-239">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="63965-239">Click OK.</span></span>
26. <span data-ttu-id="63965-240">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="63965-240">Click OK.</span></span>
27. <span data-ttu-id="63965-241">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="63965-241">Close the page.</span></span>
28. <span data-ttu-id="63965-242">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="63965-242">Click New.</span></span>
29. <span data-ttu-id="63965-243">V poli Účet odběratele vyberte zákazníka EU.</span><span class="sxs-lookup"><span data-stu-id="63965-243">In the Customer account field, select an EU customer.</span></span>
    * <span data-ttu-id="63965-244">Vyberte například DE-013 Trey Wholesales</span><span class="sxs-lookup"><span data-stu-id="63965-244">For example, select 'DE-013 Trey Wholesales'</span></span>  
30. <span data-ttu-id="63965-245">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="63965-245">Click OK.</span></span>
31. <span data-ttu-id="63965-246">V poli Číslo zboží zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="63965-246">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="63965-247">Vyberte například D0001.</span><span class="sxs-lookup"><span data-stu-id="63965-247">For example, select 'D0001'.</span></span>  
32. <span data-ttu-id="63965-248">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="63965-248">Click Save.</span></span>
33. <span data-ttu-id="63965-249">Klikněte na položku Faktura.</span><span class="sxs-lookup"><span data-stu-id="63965-249">Click Invoice.</span></span>
34. <span data-ttu-id="63965-250">Do pole Datum faktury zadejte datum.</span><span class="sxs-lookup"><span data-stu-id="63965-250">In the Invoice date field, enter a date.</span></span>
    * <span data-ttu-id="63965-251">Například zadejte datum 2015-01-31.</span><span class="sxs-lookup"><span data-stu-id="63965-251">For example, enter the date '2015-01-31'.</span></span>  
35. <span data-ttu-id="63965-252">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="63965-252">Click OK.</span></span>
36. <span data-ttu-id="63965-253">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="63965-253">Click OK.</span></span>

## <a name="transfer-transactions-to-the-intrastat"></a><span data-ttu-id="63965-254">Převod transakcí do systému Intrastat</span><span class="sxs-lookup"><span data-stu-id="63965-254">Transfer transactions to the Intrastat</span></span>
1. <span data-ttu-id="63965-255">Přejděte na Daň > Deklarace > Zahraniční obchod > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="63965-255">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
2. <span data-ttu-id="63965-256">Klepněte na položku Převod.</span><span class="sxs-lookup"><span data-stu-id="63965-256">Click Transfer.</span></span>
3. <span data-ttu-id="63965-257">Vyberte možnost Ano v poli Faktura odběratele.</span><span class="sxs-lookup"><span data-stu-id="63965-257">Select Yes in the Customer invoice field.</span></span>
4. <span data-ttu-id="63965-258">Klepněte na tlačítko Filtr.</span><span class="sxs-lookup"><span data-stu-id="63965-258">Click Filter.</span></span>
5. <span data-ttu-id="63965-259">Označte na seznamu řádek s datem.</span><span class="sxs-lookup"><span data-stu-id="63965-259">In the list, mark the row with Date</span></span>
6. <span data-ttu-id="63965-260">Zadejte hodnotu do pole Kritéria.</span><span class="sxs-lookup"><span data-stu-id="63965-260">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="63965-261">Například zadejte filtr pro období Leden 2015 (přesná hodnota závisí na formátu data): 1/1/2015..1/31/2015</span><span class="sxs-lookup"><span data-stu-id="63965-261">For example, enter the filter for the period January 2015 (the exact value depends on your date format): 1/1/2015..1/31/2015</span></span>  
7. <span data-ttu-id="63965-262">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="63965-262">Click OK.</span></span>
8. <span data-ttu-id="63965-263">Klikněte na tlačítko OK.</span><span class="sxs-lookup"><span data-stu-id="63965-263">Click OK.</span></span>
9. <span data-ttu-id="63965-264">Vyhledejte na seznamu převedený záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="63965-264">In the list, find and selected the transferred record.</span></span>
10. <span data-ttu-id="63965-265">Klikněte na záložku Obecné.</span><span class="sxs-lookup"><span data-stu-id="63965-265">Click the General tab.</span></span>
    * <span data-ttu-id="63965-266">Zkontrolujte převedená data včetně Cílová země/oblast expedice, země původu, hmotnosti, množství, množství v dalších jednotkách, zboží, kódu transakce, výše faktury a statistických částek.</span><span class="sxs-lookup"><span data-stu-id="63965-266">Review transferred data, including country\region of destination/dispatch, country of origin, weight, quantity, quantity in additional units, commodity, transaction code, invoice amounts and statistical amounts.</span></span>   <span data-ttu-id="63965-267">Tato data lze v případě potřeby změnit.</span><span class="sxs-lookup"><span data-stu-id="63965-267">You can modify data if necessary.</span></span>  


