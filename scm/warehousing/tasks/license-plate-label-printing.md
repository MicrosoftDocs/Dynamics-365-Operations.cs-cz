--- 
title: "Povolení tisku popisku registrační značky"
description: "Tento postup umožňuje automatický tisk štítku Sériový nákladový kód kontejneru (SSCC) po vydání poslední položky ze skladu v procesu prodejního výdeje."
author: perlynne
manager: AnnBe
ms.date: 11/03/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6d186bf7e4aee8cfa97adbd90b9090085e842f9b
ms.contentlocale: cs-cz
ms.lasthandoff: 08/29/2017

---
# <a name="enable-license-plate-label-printing"></a><span data-ttu-id="b636a-103">Povolení tisku popisku registrační značky</span><span class="sxs-lookup"><span data-stu-id="b636a-103">Enable license plate label printing</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b636a-104">Tento postup umožňuje automatický tisk štítku Sériový nákladový kód kontejneru (SSCC) po vydání poslední položky ze skladu v procesu prodejního výdeje.</span><span class="sxs-lookup"><span data-stu-id="b636a-104">This procedure enables the automatic printing of a Serial shipping container code (SSCC) label after the last item is picked from inventory in a sales picking work process.</span></span> <span data-ttu-id="b636a-105">Tento postup můžete projít v ukázkových datech společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="b636a-105">You can run this procedure in demo data company USMF.</span></span> <span data-ttu-id="b636a-106">Pokud jej používáte s použitím vlastních dat, je třeba mít k nastavenou číselnou řadu pro registračních značky vozidla.</span><span class="sxs-lookup"><span data-stu-id="b636a-106">If you’re run it using your own data, you need to have a number sequence set up for license plates.</span></span> <span data-ttu-id="b636a-107">Je nutné nastavit tiskárnu štítků před zahájením této úlohy.</span><span class="sxs-lookup"><span data-stu-id="b636a-107">You need to set up a label printer before you begin this task.</span></span> <span data-ttu-id="b636a-108">Přejděte do nabídky Správa organizace > Nastavení > Jednotky Síťové tiskárny.</span><span class="sxs-lookup"><span data-stu-id="b636a-108">Go to Organization administration > Setup > Network printers.</span></span> <span data-ttu-id="b636a-109">V podokně Akce klikněte na Možnosti a poté klepněte na tlačítko Stáhnout instalační program agenta směrování dokumentů.</span><span class="sxs-lookup"><span data-stu-id="b636a-109">On the Action pane, click Options, and then click the Download document routing agent installer button.</span></span> <span data-ttu-id="b636a-110">Spusťte instalační program a ujistěte se, že máte nastavenu síťovou tiskárnu na hodnotu Aktivní předtím, než budete pokračovat v postupu.</span><span class="sxs-lookup"><span data-stu-id="b636a-110">Run the installer and make sure that you have a working network printer set to Active before you continue with the procedure.</span></span>


## <a name="set-up-the-gs1-company-prefix"></a><span data-ttu-id="b636a-111">Nastavení předpony společnosti GS1</span><span class="sxs-lookup"><span data-stu-id="b636a-111">Set up the GS1 company prefix</span></span>
1. <span data-ttu-id="b636a-112">Přejděte do nabídky Řízení skladu > Nastavení > Parametry řízení skladu.</span><span class="sxs-lookup"><span data-stu-id="b636a-112">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="b636a-113">Do pole Předpona společnosti GS1 zadejte 7 čísel pro vaše číslo společnosti GS1.</span><span class="sxs-lookup"><span data-stu-id="b636a-113">In the GS1 company prefix field, enter the 7 numbers for your GS1 company number.</span></span>
3. <span data-ttu-id="b636a-114">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b636a-114">Click Save.</span></span>
4. <span data-ttu-id="b636a-115">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b636a-115">Close the page.</span></span>

## <a name="setup-the-sscc-license-plate-number-sequence"></a><span data-ttu-id="b636a-116">Nastavení číselné řady registrační značky vozidla SSCC</span><span class="sxs-lookup"><span data-stu-id="b636a-116">Setup the SSCC license plate number sequence</span></span>
1. <span data-ttu-id="b636a-117">Přejděte na Správa organizace > Číselné řady > Číselné řady.</span><span class="sxs-lookup"><span data-stu-id="b636a-117">Go to Organization administration > Number sequences > Number sequences.</span></span>
2. <span data-ttu-id="b636a-118">Vyberte volbu v poli Oblast.</span><span class="sxs-lookup"><span data-stu-id="b636a-118">In the Area field, select an option.</span></span>
3. <span data-ttu-id="b636a-119">Vyberte volbu v poli Odkaz.</span><span class="sxs-lookup"><span data-stu-id="b636a-119">In the Reference field, select an option.</span></span>
4. <span data-ttu-id="b636a-120">Zadejte hodnotu do pole Společnost.</span><span class="sxs-lookup"><span data-stu-id="b636a-120">In the Company field, type a value.</span></span>
5. <span data-ttu-id="b636a-121">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="b636a-121">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="b636a-122">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="b636a-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="b636a-123">Rozbalte sekci Segmenty.</span><span class="sxs-lookup"><span data-stu-id="b636a-123">Expand the Segments section.</span></span>
8. <span data-ttu-id="b636a-124">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="b636a-124">Click Edit.</span></span>
9. <span data-ttu-id="b636a-125">V tabulce segmentů vyberte první řádek.</span><span class="sxs-lookup"><span data-stu-id="b636a-125">In the Segments table, select the first row</span></span>
10. <span data-ttu-id="b636a-126">Klepněte na tlačítko Odebrat.</span><span class="sxs-lookup"><span data-stu-id="b636a-126">Click Remove.</span></span>
11. <span data-ttu-id="b636a-127">Klepněte na tlačítko Odebrat.</span><span class="sxs-lookup"><span data-stu-id="b636a-127">Click Remove.</span></span>
12. <span data-ttu-id="b636a-128">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b636a-128">Click Save.</span></span>
13. <span data-ttu-id="b636a-129">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b636a-129">Close the page.</span></span>

## <a name="create-the-document-route-layout"></a><span data-ttu-id="b636a-130">Vytvoření rozvržení směrování dokumentu</span><span class="sxs-lookup"><span data-stu-id="b636a-130">Create the document route layout</span></span>
1. <span data-ttu-id="b636a-131">Přejít na Správa skladu > Nastavení > Směrování dokumentu > Rozložení směrování dokumentů.</span><span class="sxs-lookup"><span data-stu-id="b636a-131">Go to Warehouse management > Setup > Document routing > Document routing layouts.</span></span>
    * <span data-ttu-id="b636a-132">Povolte rozvržení SSCC.</span><span class="sxs-lookup"><span data-stu-id="b636a-132">Enable the SSCC layout.</span></span>  
2. <span data-ttu-id="b636a-133">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="b636a-133">Click New.</span></span>
3. <span data-ttu-id="b636a-134">Zadejte hodnotu do pole ID rozvržení.</span><span class="sxs-lookup"><span data-stu-id="b636a-134">In the Layout ID field, type a value.</span></span>
4. <span data-ttu-id="b636a-135">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="b636a-135">In the Description field, type a value.</span></span>
5. <span data-ttu-id="b636a-136">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="b636a-136">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="b636a-137">Klikněte na Vložit na konci textu.</span><span class="sxs-lookup"><span data-stu-id="b636a-137">Click Insert at end of text.</span></span>
7. <span data-ttu-id="b636a-138">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b636a-138">Click Save.</span></span>
8. <span data-ttu-id="b636a-139">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b636a-139">Close the page.</span></span>

## <a name="set-up-the-document-routing"></a><span data-ttu-id="b636a-140">Nastavení směrování dokumentu</span><span class="sxs-lookup"><span data-stu-id="b636a-140">Set up the document routing</span></span>
1. <span data-ttu-id="b636a-141">Přejít na Správa skladu > Nastavení > Směrování dokumentu > Směrování dokumentů.</span><span class="sxs-lookup"><span data-stu-id="b636a-141">Go to Warehouse management > Setup > Document routing > Document routing.</span></span>
2. <span data-ttu-id="b636a-142">V poli Typ pořadí pracovních činností vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="b636a-142">In the Work order type field, select an option.</span></span>
3. <span data-ttu-id="b636a-143">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="b636a-143">Click New.</span></span>
4. <span data-ttu-id="b636a-144">Zadejte hodnotu do pole Sklad.</span><span class="sxs-lookup"><span data-stu-id="b636a-144">In the Warehouse field, type a value.</span></span>
5. <span data-ttu-id="b636a-145">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="b636a-145">In the Name field, type a value.</span></span>
6. <span data-ttu-id="b636a-146">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="b636a-146">Click New.</span></span>
7. <span data-ttu-id="b636a-147">V poli ID rozvržení zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b636a-147">In the Layout ID field, enter or select a value.</span></span>
8. <span data-ttu-id="b636a-148">V poli Název zadejte název tiskárny, kterou chcete použít.</span><span class="sxs-lookup"><span data-stu-id="b636a-148">In the Name field, enter the printer name that you want to use..</span></span>
9. <span data-ttu-id="b636a-149">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b636a-149">Click Save.</span></span>
10. <span data-ttu-id="b636a-150">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b636a-150">Close the page.</span></span>

## <a name="create-mobile-device-menu"></a><span data-ttu-id="b636a-151">Vytvoření nabídky mobilního zařízení</span><span class="sxs-lookup"><span data-stu-id="b636a-151">Create mobile device menu</span></span>
1. <span data-ttu-id="b636a-152">Přejděte do nabídky Řízení skladu > Nastavení > Mobilní zařízení > Položky nabídky mobilního zařízení.</span><span class="sxs-lookup"><span data-stu-id="b636a-152">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="b636a-153">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="b636a-153">Click New.</span></span>
3. <span data-ttu-id="b636a-154">Do pole Položky nabídky mobilního zařízení zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b636a-154">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="b636a-155">Zadejte hodnotu do pole Titul.</span><span class="sxs-lookup"><span data-stu-id="b636a-155">In the Title field, type a value.</span></span>
5. <span data-ttu-id="b636a-156">Vyberte volbu v poli Režim.</span><span class="sxs-lookup"><span data-stu-id="b636a-156">In the Mode field, select an option.</span></span>
6. <span data-ttu-id="b636a-157">Vyberte možnost Ano v poli Použít stávající práci.</span><span class="sxs-lookup"><span data-stu-id="b636a-157">Select Yes in the Use existing work field.</span></span>
7. <span data-ttu-id="b636a-158">Vyberte možnost Ano v poli Generovat registrační značku.</span><span class="sxs-lookup"><span data-stu-id="b636a-158">Select Yes in the Generate license plate field.</span></span>
8. <span data-ttu-id="b636a-159">Rozbalte sekci Pracovní třídy.</span><span class="sxs-lookup"><span data-stu-id="b636a-159">Expand the Work classes section.</span></span>
9. <span data-ttu-id="b636a-160">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="b636a-160">Click New.</span></span>
10. <span data-ttu-id="b636a-161">Zadejte hodnotu do pole ID pracovní třídy.</span><span class="sxs-lookup"><span data-stu-id="b636a-161">In the Work class ID field, type a value.</span></span>
11. <span data-ttu-id="b636a-162">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b636a-162">Click Save.</span></span>
12. <span data-ttu-id="b636a-163">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b636a-163">Close the page.</span></span>
13. <span data-ttu-id="b636a-164">Přejděte do nabídky Řízení skladu > Nastavení > Mobilní zařízení > Nabídka mobilního zařízení.</span><span class="sxs-lookup"><span data-stu-id="b636a-164">Go to Warehouse management > Setup > Mobile device > Mobile device menu.</span></span>
14. <span data-ttu-id="b636a-165">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="b636a-165">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="b636a-166">Ve stromové struktuře vyberte "Ve stromu vybrat dříve vytvořenou položku nabídky".</span><span class="sxs-lookup"><span data-stu-id="b636a-166">In the tree, select 'In the tree, select the menu item that you created before.'.</span></span>
16. <span data-ttu-id="b636a-167">Klikněte na možnost Upravit.</span><span class="sxs-lookup"><span data-stu-id="b636a-167">Click Edit.</span></span>
17. <span data-ttu-id="b636a-168">Klepnutím na šipku přidejte položku nabídky do nabídky.</span><span class="sxs-lookup"><span data-stu-id="b636a-168">Click on the arrow to add the menu item to the menu.</span></span>
18. <span data-ttu-id="b636a-169">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b636a-169">Click Save.</span></span>
19. <span data-ttu-id="b636a-170">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b636a-170">Close the page.</span></span>

## <a name="update-a-work-template"></a><span data-ttu-id="b636a-171">Aktualizace šablony práce</span><span class="sxs-lookup"><span data-stu-id="b636a-171">Update a work template</span></span>
1. <span data-ttu-id="b636a-172">Přejděte do nabídky Řízení skladu > Nastavení > Práce > Pracovní šablony.</span><span class="sxs-lookup"><span data-stu-id="b636a-172">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="b636a-173">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="b636a-173">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="b636a-174">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="b636a-174">Click Edit.</span></span>
4. <span data-ttu-id="b636a-175">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="b636a-175">Click New.</span></span>
5. <span data-ttu-id="b636a-176">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="b636a-176">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="b636a-177">V poli Typ práce vyberte „Tisk“.</span><span class="sxs-lookup"><span data-stu-id="b636a-177">In the Work type field, select 'Print'.</span></span>
7. <span data-ttu-id="b636a-178">V poli ID pracovní třídy zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="b636a-178">In the Work class ID field, enter or select a value.</span></span>
8. <span data-ttu-id="b636a-179">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="b636a-179">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="b636a-180">Klikněte na Přesunout nahoru.</span><span class="sxs-lookup"><span data-stu-id="b636a-180">Click Move up.</span></span>
10. <span data-ttu-id="b636a-181">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="b636a-181">Click Save.</span></span>
11. <span data-ttu-id="b636a-182">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="b636a-182">Close the page.</span></span>


