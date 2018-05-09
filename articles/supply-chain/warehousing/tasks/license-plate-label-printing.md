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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 0c0515d61f651b9244525fc20c242f3d31eb3a20
ms.contentlocale: cs-cz
ms.lasthandoff: 05/08/2018

---
# <a name="enable-license-plate-label-printing"></a><span data-ttu-id="92670-103">Povolení tisku popisku registrační značky</span><span class="sxs-lookup"><span data-stu-id="92670-103">Enable license plate label printing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="92670-104">Tento postup umožňuje automatický tisk štítku Sériový nákladový kód kontejneru (SSCC) po vydání poslední položky ze skladu v procesu prodejního výdeje.</span><span class="sxs-lookup"><span data-stu-id="92670-104">This procedure enables the automatic printing of a Serial shipping container code (SSCC) label after the last item is picked from inventory in a sales picking work process.</span></span> <span data-ttu-id="92670-105">Tento postup můžete projít v ukázkových datech společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="92670-105">You can run this procedure in demo data company USMF.</span></span> <span data-ttu-id="92670-106">Pokud jej používáte s použitím vlastních dat, je třeba mít k nastavenou číselnou řadu pro registračních značky vozidla.</span><span class="sxs-lookup"><span data-stu-id="92670-106">If you’re run it using your own data, you need to have a number sequence set up for license plates.</span></span> <span data-ttu-id="92670-107">Je nutné nastavit tiskárnu štítků před zahájením této úlohy.</span><span class="sxs-lookup"><span data-stu-id="92670-107">You need to set up a label printer before you begin this task.</span></span> <span data-ttu-id="92670-108">Přejděte do nabídky Správa organizace > Nastavení > Jednotky Síťové tiskárny.</span><span class="sxs-lookup"><span data-stu-id="92670-108">Go to Organization administration > Setup > Network printers.</span></span> <span data-ttu-id="92670-109">V podokně Akce klikněte na Možnosti a poté klepněte na tlačítko Stáhnout instalační program agenta směrování dokumentů.</span><span class="sxs-lookup"><span data-stu-id="92670-109">On the Action pane, click Options, and then click the Download document routing agent installer button.</span></span> <span data-ttu-id="92670-110">Spusťte instalační program a ujistěte se, že máte nastavenu síťovou tiskárnu na hodnotu Aktivní předtím, než budete pokračovat v postupu.</span><span class="sxs-lookup"><span data-stu-id="92670-110">Run the installer and make sure that you have a working network printer set to Active before you continue with the procedure.</span></span>


## <a name="set-up-the-gs1-company-prefix"></a><span data-ttu-id="92670-111">Nastavení předpony společnosti GS1</span><span class="sxs-lookup"><span data-stu-id="92670-111">Set up the GS1 company prefix</span></span>
1. <span data-ttu-id="92670-112">Přejděte do nabídky Řízení skladu > Nastavení > Parametry řízení skladu.</span><span class="sxs-lookup"><span data-stu-id="92670-112">Go to Warehouse management > Setup > Warehouse management parameters.</span></span>
2. <span data-ttu-id="92670-113">Do pole Předpona společnosti GS1 zadejte 7 čísel pro vaše číslo společnosti GS1.</span><span class="sxs-lookup"><span data-stu-id="92670-113">In the GS1 company prefix field, enter the 7 numbers for your GS1 company number.</span></span>
3. <span data-ttu-id="92670-114">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="92670-114">Click Save.</span></span>
4. <span data-ttu-id="92670-115">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="92670-115">Close the page.</span></span>

## <a name="setup-the-sscc-license-plate-number-sequence"></a><span data-ttu-id="92670-116">Nastavení číselné řady registrační značky vozidla SSCC</span><span class="sxs-lookup"><span data-stu-id="92670-116">Setup the SSCC license plate number sequence</span></span>
1. <span data-ttu-id="92670-117">Přejděte na Správa organizace > Číselné řady > Číselné řady.</span><span class="sxs-lookup"><span data-stu-id="92670-117">Go to Organization administration > Number sequences > Number sequences.</span></span>
2. <span data-ttu-id="92670-118">Vyberte volbu v poli Oblast.</span><span class="sxs-lookup"><span data-stu-id="92670-118">In the Area field, select an option.</span></span>
3. <span data-ttu-id="92670-119">Vyberte volbu v poli Odkaz.</span><span class="sxs-lookup"><span data-stu-id="92670-119">In the Reference field, select an option.</span></span>
4. <span data-ttu-id="92670-120">Zadejte hodnotu do pole Společnost.</span><span class="sxs-lookup"><span data-stu-id="92670-120">In the Company field, type a value.</span></span>
5. <span data-ttu-id="92670-121">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="92670-121">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="92670-122">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="92670-122">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="92670-123">Rozbalte sekci Segmenty.</span><span class="sxs-lookup"><span data-stu-id="92670-123">Expand the Segments section.</span></span>
8. <span data-ttu-id="92670-124">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="92670-124">Click Edit.</span></span>
9. <span data-ttu-id="92670-125">V tabulce segmentů vyberte první řádek.</span><span class="sxs-lookup"><span data-stu-id="92670-125">In the Segments table, select the first row</span></span>
10. <span data-ttu-id="92670-126">Klepněte na tlačítko Odebrat.</span><span class="sxs-lookup"><span data-stu-id="92670-126">Click Remove.</span></span>
11. <span data-ttu-id="92670-127">Klepněte na tlačítko Odebrat.</span><span class="sxs-lookup"><span data-stu-id="92670-127">Click Remove.</span></span>
12. <span data-ttu-id="92670-128">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="92670-128">Click Save.</span></span>
13. <span data-ttu-id="92670-129">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="92670-129">Close the page.</span></span>

## <a name="create-the-document-route-layout"></a><span data-ttu-id="92670-130">Vytvoření rozvržení směrování dokumentu</span><span class="sxs-lookup"><span data-stu-id="92670-130">Create the document route layout</span></span>
1. <span data-ttu-id="92670-131">Přejít na Správa skladu > Nastavení > Směrování dokumentu > Rozložení směrování dokumentů.</span><span class="sxs-lookup"><span data-stu-id="92670-131">Go to Warehouse management > Setup > Document routing > Document routing layouts.</span></span>
    * <span data-ttu-id="92670-132">Povolte rozvržení SSCC.</span><span class="sxs-lookup"><span data-stu-id="92670-132">Enable the SSCC layout.</span></span>  
2. <span data-ttu-id="92670-133">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="92670-133">Click New.</span></span>
3. <span data-ttu-id="92670-134">Zadejte hodnotu do pole ID rozvržení.</span><span class="sxs-lookup"><span data-stu-id="92670-134">In the Layout ID field, type a value.</span></span>
4. <span data-ttu-id="92670-135">Zadejte nějakou hodnotu do pole Popis.</span><span class="sxs-lookup"><span data-stu-id="92670-135">In the Description field, type a value.</span></span>
5. <span data-ttu-id="92670-136">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="92670-136">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="92670-137">Klikněte na Vložit na konci textu.</span><span class="sxs-lookup"><span data-stu-id="92670-137">Click Insert at end of text.</span></span>
7. <span data-ttu-id="92670-138">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="92670-138">Click Save.</span></span>
8. <span data-ttu-id="92670-139">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="92670-139">Close the page.</span></span>

## <a name="set-up-the-document-routing"></a><span data-ttu-id="92670-140">Nastavení směrování dokumentu</span><span class="sxs-lookup"><span data-stu-id="92670-140">Set up the document routing</span></span>
1. <span data-ttu-id="92670-141">Přejít na Správa skladu > Nastavení > Směrování dokumentu > Směrování dokumentů.</span><span class="sxs-lookup"><span data-stu-id="92670-141">Go to Warehouse management > Setup > Document routing > Document routing.</span></span>
2. <span data-ttu-id="92670-142">V poli Typ pořadí pracovních činností vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="92670-142">In the Work order type field, select an option.</span></span>
3. <span data-ttu-id="92670-143">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="92670-143">Click New.</span></span>
4. <span data-ttu-id="92670-144">Zadejte hodnotu do pole Sklad.</span><span class="sxs-lookup"><span data-stu-id="92670-144">In the Warehouse field, type a value.</span></span>
5. <span data-ttu-id="92670-145">Zadejte hodnotu do pole Název.</span><span class="sxs-lookup"><span data-stu-id="92670-145">In the Name field, type a value.</span></span>
6. <span data-ttu-id="92670-146">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="92670-146">Click New.</span></span>
7. <span data-ttu-id="92670-147">V poli ID rozvržení zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="92670-147">In the Layout ID field, enter or select a value.</span></span>
8. <span data-ttu-id="92670-148">V poli Název zadejte název tiskárny, kterou chcete použít.</span><span class="sxs-lookup"><span data-stu-id="92670-148">In the Name field, enter the printer name that you want to use..</span></span>
9. <span data-ttu-id="92670-149">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="92670-149">Click Save.</span></span>
10. <span data-ttu-id="92670-150">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="92670-150">Close the page.</span></span>

## <a name="create-mobile-device-menu"></a><span data-ttu-id="92670-151">Vytvoření nabídky mobilního zařízení</span><span class="sxs-lookup"><span data-stu-id="92670-151">Create mobile device menu</span></span>
1. <span data-ttu-id="92670-152">Přejděte do nabídky Řízení skladu > Nastavení > Mobilní zařízení > Položky nabídky mobilního zařízení.</span><span class="sxs-lookup"><span data-stu-id="92670-152">Go to Warehouse management > Setup > Mobile device > Mobile device menu items.</span></span>
2. <span data-ttu-id="92670-153">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="92670-153">Click New.</span></span>
3. <span data-ttu-id="92670-154">Do pole Položky nabídky mobilního zařízení zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="92670-154">In the Menu item name field, type a value.</span></span>
4. <span data-ttu-id="92670-155">Zadejte hodnotu do pole Titul.</span><span class="sxs-lookup"><span data-stu-id="92670-155">In the Title field, type a value.</span></span>
5. <span data-ttu-id="92670-156">Vyberte volbu v poli Režim.</span><span class="sxs-lookup"><span data-stu-id="92670-156">In the Mode field, select an option.</span></span>
6. <span data-ttu-id="92670-157">Vyberte možnost Ano v poli Použít stávající práci.</span><span class="sxs-lookup"><span data-stu-id="92670-157">Select Yes in the Use existing work field.</span></span>
7. <span data-ttu-id="92670-158">Vyberte možnost Ano v poli Generovat registrační značku.</span><span class="sxs-lookup"><span data-stu-id="92670-158">Select Yes in the Generate license plate field.</span></span>
8. <span data-ttu-id="92670-159">Rozbalte sekci Pracovní třídy.</span><span class="sxs-lookup"><span data-stu-id="92670-159">Expand the Work classes section.</span></span>
9. <span data-ttu-id="92670-160">Klikněte na položku Nová.</span><span class="sxs-lookup"><span data-stu-id="92670-160">Click New.</span></span>
10. <span data-ttu-id="92670-161">Zadejte hodnotu do pole ID pracovní třídy.</span><span class="sxs-lookup"><span data-stu-id="92670-161">In the Work class ID field, type a value.</span></span>
11. <span data-ttu-id="92670-162">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="92670-162">Click Save.</span></span>
12. <span data-ttu-id="92670-163">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="92670-163">Close the page.</span></span>
13. <span data-ttu-id="92670-164">Přejděte do nabídky Řízení skladu > Nastavení > Mobilní zařízení > Nabídka mobilního zařízení.</span><span class="sxs-lookup"><span data-stu-id="92670-164">Go to Warehouse management > Setup > Mobile device > Mobile device menu.</span></span>
14. <span data-ttu-id="92670-165">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="92670-165">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="92670-166">Ve stromové struktuře vyberte "Ve stromu vybrat dříve vytvořenou položku nabídky".</span><span class="sxs-lookup"><span data-stu-id="92670-166">In the tree, select 'In the tree, select the menu item that you created before.'.</span></span>
16. <span data-ttu-id="92670-167">Klikněte na možnost Upravit.</span><span class="sxs-lookup"><span data-stu-id="92670-167">Click Edit.</span></span>
17. <span data-ttu-id="92670-168">Klepnutím na šipku přidejte položku nabídky do nabídky.</span><span class="sxs-lookup"><span data-stu-id="92670-168">Click on the arrow to add the menu item to the menu.</span></span>
18. <span data-ttu-id="92670-169">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="92670-169">Click Save.</span></span>
19. <span data-ttu-id="92670-170">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="92670-170">Close the page.</span></span>

## <a name="update-a-work-template"></a><span data-ttu-id="92670-171">Aktualizace šablony práce</span><span class="sxs-lookup"><span data-stu-id="92670-171">Update a work template</span></span>
1. <span data-ttu-id="92670-172">Přejděte do nabídky Řízení skladu > Nastavení > Práce > Pracovní šablony.</span><span class="sxs-lookup"><span data-stu-id="92670-172">Go to Warehouse management > Setup > Work > Work templates.</span></span>
2. <span data-ttu-id="92670-173">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="92670-173">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="92670-174">Klikněte na položku Upravit.</span><span class="sxs-lookup"><span data-stu-id="92670-174">Click Edit.</span></span>
4. <span data-ttu-id="92670-175">Klepněte na možnost Nový.</span><span class="sxs-lookup"><span data-stu-id="92670-175">Click New.</span></span>
5. <span data-ttu-id="92670-176">Označte v seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="92670-176">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="92670-177">V poli Typ práce vyberte „Tisk“.</span><span class="sxs-lookup"><span data-stu-id="92670-177">In the Work type field, select 'Print'.</span></span>
7. <span data-ttu-id="92670-178">V poli ID pracovní třídy zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="92670-178">In the Work class ID field, enter or select a value.</span></span>
8. <span data-ttu-id="92670-179">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="92670-179">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="92670-180">Klikněte na Přesunout nahoru.</span><span class="sxs-lookup"><span data-stu-id="92670-180">Click Move up.</span></span>
10. <span data-ttu-id="92670-181">Klikněte na položku Uložit.</span><span class="sxs-lookup"><span data-stu-id="92670-181">Click Save.</span></span>
11. <span data-ttu-id="92670-182">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="92670-182">Close the page.</span></span>


