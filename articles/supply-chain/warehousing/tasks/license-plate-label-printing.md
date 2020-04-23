---
title: Povolení tisku popisku registrační značky
description: Tohle téma popisuje automatický tisk štítku Sériový nákladový kód kontejneru (SSCC) po vydání poslední položky ze skladu v procesu prodejního výdeje.
author: perlynne
manager: tfehr
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysCorpNetPrinterList, WHSParameters, NumberSequenceTableListPage, NumberSequenceDetails, WHSDocumentRoutingLayout, WHSDocumentRouting, WHSRFMenuItem, WHSRFMenu, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 484a1465dd41429fe201de18aac55f118a483cab
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/02/2020
ms.locfileid: "3217004"
---
# <a name="enable-license-plate-label-printing"></a><span data-ttu-id="be787-103">Povolení tisku popisku registrační značky</span><span class="sxs-lookup"><span data-stu-id="be787-103">Enable license plate label printing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="be787-104">Tohle téma popisuje automatický tisk štítku Sériový nákladový kód kontejneru (SSCC) po vydání poslední položky ze skladu v procesu prodejního výdeje.</span><span class="sxs-lookup"><span data-stu-id="be787-104">This topic shows how to enable the automatic printing of a Serial shipping container code (SSCC) label after the last item is picked from inventory in a sales picking work process.</span></span> <span data-ttu-id="be787-105">Tento postup můžete projít v ukázkových datech společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="be787-105">You can run this procedure in demo data company USMF.</span></span> <span data-ttu-id="be787-106">Pokud jej používáte s použitím vlastních dat, je třeba mít k nastavenou číselnou řadu pro registračních značky vozidla.</span><span class="sxs-lookup"><span data-stu-id="be787-106">If you're run it using your own data, you need to have a number sequence set up for license plates.</span></span> <span data-ttu-id="be787-107">Je nutné nastavit tiskárnu štítků před zahájením této úlohy.</span><span class="sxs-lookup"><span data-stu-id="be787-107">You need to set up a label printer before you begin this task.</span></span> <span data-ttu-id="be787-108">Přejděte do nabídky Správa organizace > Nastavení > Jednotky Síťové tiskárny.</span><span class="sxs-lookup"><span data-stu-id="be787-108">Go to Organization administration > Setup > Network printers.</span></span> <span data-ttu-id="be787-109">V podokně Akce klikněte na Možnosti a poté klepněte na tlačítko Stáhnout instalační program agenta směrování dokumentů.</span><span class="sxs-lookup"><span data-stu-id="be787-109">On the Action pane, click Options, and then click the Download document routing agent installer button.</span></span> <span data-ttu-id="be787-110">Spusťte instalační program a ujistěte se, že máte nastavenu síťovou tiskárnu na hodnotu Aktivní předtím, než budete pokračovat v postupu.</span><span class="sxs-lookup"><span data-stu-id="be787-110">Run the installer and make sure that you have a working network printer set to Active before you continue with the procedure.</span></span>


## <a name="set-up-the-gs1-company-prefix"></a><span data-ttu-id="be787-111">Nastavení předpony společnosti GS1</span><span class="sxs-lookup"><span data-stu-id="be787-111">Set up the GS1 company prefix</span></span>
1. <span data-ttu-id="be787-112">Přejděte na **Navigační podokno > Moduly > Řízení skladu > Nastavení > Parametry řízení skladu**.</span><span class="sxs-lookup"><span data-stu-id="be787-112">Go to **Navigation pane > Modules > Warehouse management > Setup > Warehouse management parameters**.</span></span>
2. <span data-ttu-id="be787-113">Do pole **Předpona společnosti GS1** zadejte 7 čísel pro vaše číslo společnosti GS1.</span><span class="sxs-lookup"><span data-stu-id="be787-113">In the **GS1 company prefix** field, enter the 7 numbers for your GS1 company number.</span></span>
3. <span data-ttu-id="be787-114">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="be787-114">Select **Save**.</span></span>
4. <span data-ttu-id="be787-115">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="be787-115">Close the page.</span></span>

## <a name="setup-the-sscc-license-plate-number-sequence"></a><span data-ttu-id="be787-116">Nastavení číselné řady registrační značky vozidla SSCC</span><span class="sxs-lookup"><span data-stu-id="be787-116">Setup the SSCC license plate number sequence</span></span>
1. <span data-ttu-id="be787-117">Přejděte na **Navigační podokno > Moduly > Správa organizace > Číselné řady > Číselné řady**.</span><span class="sxs-lookup"><span data-stu-id="be787-117">Go to **Navigation pane > Modules > Organization administration > Number sequences > Number sequences**.</span></span>
2. <span data-ttu-id="be787-118">Vyberte volbu v poli **Oblast**.</span><span class="sxs-lookup"><span data-stu-id="be787-118">In the **Area** field, select an option.</span></span>
3. <span data-ttu-id="be787-119">Vyberte volbu v poli **Odkaz**.</span><span class="sxs-lookup"><span data-stu-id="be787-119">In the **Reference** field, select an option.</span></span>
4. <span data-ttu-id="be787-120">Zadejte hodnotu do pole **Společnost**.</span><span class="sxs-lookup"><span data-stu-id="be787-120">In the **Company** field, type a value.</span></span>
5. <span data-ttu-id="be787-121">Rozbalte sekci **Segmenty**.</span><span class="sxs-lookup"><span data-stu-id="be787-121">Expand the **Segments** section.</span></span>
6. <span data-ttu-id="be787-122">Vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="be787-122">Select **Edit**.</span></span>
7. <span data-ttu-id="be787-123">V tabulce **Segmenty** vyberte první řádek.</span><span class="sxs-lookup"><span data-stu-id="be787-123">In the **Segments** table, select the first row</span></span>
8. <span data-ttu-id="be787-124">Vyberte možnost **Odebrat**.</span><span class="sxs-lookup"><span data-stu-id="be787-124">Select **Remove**.</span></span>
9. <span data-ttu-id="be787-125">Vyberte možnost **Odebrat**.</span><span class="sxs-lookup"><span data-stu-id="be787-125">Select **Remove**.</span></span>
10. <span data-ttu-id="be787-126">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="be787-126">Select **Save**.</span></span>
11. <span data-ttu-id="be787-127">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="be787-127">Close the page.</span></span>

## <a name="create-the-document-route-layout"></a><span data-ttu-id="be787-128">Vytvoření rozvržení směrování dokumentu</span><span class="sxs-lookup"><span data-stu-id="be787-128">Create the document route layout</span></span>
1. <span data-ttu-id="be787-129">Přejděte do **navigačního podokna > Moduly > Správa skladu > Nastavení > Směrování dokumentu > Rozložení směrování dokumentů**.</span><span class="sxs-lookup"><span data-stu-id="be787-129">Go to **Navigation pane > Modules > Warehouse management > Setup > Document routing > Document routing layouts**.</span></span> <span data-ttu-id="be787-130">Povolte rozvržení SSCC.</span><span class="sxs-lookup"><span data-stu-id="be787-130">Enable the SSCC layout.</span></span>  
2. <span data-ttu-id="be787-131">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="be787-131">Select **New**.</span></span>
3. <span data-ttu-id="be787-132">Zadejte hodnotu do pole **ID rozvržení**.</span><span class="sxs-lookup"><span data-stu-id="be787-132">In the **Layout ID** field, type a value.</span></span>
4. <span data-ttu-id="be787-133">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="be787-133">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="be787-134">Vyberte **Vložit na konci textu**.</span><span class="sxs-lookup"><span data-stu-id="be787-134">Select **Insert at end of text**.</span></span>
6. <span data-ttu-id="be787-135">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="be787-135">Select **Save**.</span></span>
7. <span data-ttu-id="be787-136">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="be787-136">Close the page.</span></span>

## <a name="set-up-the-document-routing"></a><span data-ttu-id="be787-137">Nastavení směrování dokumentu</span><span class="sxs-lookup"><span data-stu-id="be787-137">Set up the document routing</span></span>
1. <span data-ttu-id="be787-138">Přejděte do **navigačního podokna > Moduly > Správa skladu > Nastavení > Směrování dokumentu > Směrování dokumentů**.</span><span class="sxs-lookup"><span data-stu-id="be787-138">Go to **Navigation pane > Modules > Warehouse management > Setup > Document routing > Document routing**.</span></span>
2. <span data-ttu-id="be787-139">V poli **Typ pracovního příkazu** vyberte možnost.</span><span class="sxs-lookup"><span data-stu-id="be787-139">In the **Work order type** field, select an option.</span></span>
3. <span data-ttu-id="be787-140">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="be787-140">Select **New**.</span></span>
4. <span data-ttu-id="be787-141">Zadejte hodnotu do pole **Sklad**.</span><span class="sxs-lookup"><span data-stu-id="be787-141">In the **Warehouse** field, type a value.</span></span>
5. <span data-ttu-id="be787-142">Zadejte hodnotu do pole **Název**.</span><span class="sxs-lookup"><span data-stu-id="be787-142">In the **Name** field, type a value.</span></span>
6. <span data-ttu-id="be787-143">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="be787-143">Select **New**.</span></span>
7. <span data-ttu-id="be787-144">V poli **ID rozvržení** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="be787-144">In the **Layout ID** field, enter or select a value.</span></span>
8. <span data-ttu-id="be787-145">V poli **Název** zadejte název tiskárny, kterou chcete použít.</span><span class="sxs-lookup"><span data-stu-id="be787-145">In the **Name** field, enter the printer name that you want to use.</span></span>
9. <span data-ttu-id="be787-146">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="be787-146">Select **Save**.</span></span>
10. <span data-ttu-id="be787-147">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="be787-147">Close the page.</span></span>

## <a name="create-mobile-device-menu"></a><span data-ttu-id="be787-148">Vytvoření nabídky mobilního zařízení</span><span class="sxs-lookup"><span data-stu-id="be787-148">Create mobile device menu</span></span>
1. <span data-ttu-id="be787-149">V navigačním podokně přejděte do nabídky **Moduly > Řízení skladu > Nastavení > Mobilní zařízení > Položky nabídky mobilního zařízení**.</span><span class="sxs-lookup"><span data-stu-id="be787-149">Go to **Navigation pane > Modules > Warehouse management > Setup > Mobile device > Mobile device menu items**.</span></span>
2. <span data-ttu-id="be787-150">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="be787-150">Select **New**.</span></span>
3. <span data-ttu-id="be787-151">Do pole **Název položky nabídky** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="be787-151">In the **Menu item name** field, type a value.</span></span>
4. <span data-ttu-id="be787-152">Zadejte hodnotu do pole **Nadpis**.</span><span class="sxs-lookup"><span data-stu-id="be787-152">In the **Title** field, type a value.</span></span>
5. <span data-ttu-id="be787-153">V poli **Režim** vyberte režim.</span><span class="sxs-lookup"><span data-stu-id="be787-153">In the **Mode** field, select an option.</span></span>
6. <span data-ttu-id="be787-154">V poli **Použít stávající práci** vyberte možnost **Ano**.</span><span class="sxs-lookup"><span data-stu-id="be787-154">Select **Yes** in the **Use existing work** field.</span></span>
7. <span data-ttu-id="be787-155">V poli **Generovat registrační značku** vyberte možnost **Ano**.</span><span class="sxs-lookup"><span data-stu-id="be787-155">Select **Yes** in the **Generate license plate** field.</span></span>
8. <span data-ttu-id="be787-156">Rozbalte sekci **Pracovní třídy**.</span><span class="sxs-lookup"><span data-stu-id="be787-156">Expand the **Work classes** section.</span></span>
9. <span data-ttu-id="be787-157">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="be787-157">Select **New**.</span></span>
10. <span data-ttu-id="be787-158">Do pole **ID pracovní třídy** zadejte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="be787-158">In the **Work class ID** field, type a value.</span></span>
11. <span data-ttu-id="be787-159">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="be787-159">Select **Save**.</span></span>
12. <span data-ttu-id="be787-160">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="be787-160">Close the page.</span></span>
13. <span data-ttu-id="be787-161">V navigačním podokně přejděte do nabídky **Moduly > Řízení skladu > Nastavení > Mobilní zařízení > Nabídka mobilního zařízení**.</span><span class="sxs-lookup"><span data-stu-id="be787-161">Go to **navigation pane > Modules > Warehouse management > Setup > Mobile device > Mobile device menu**.</span></span>
14. <span data-ttu-id="be787-162">Ve stromové struktuře vyberte dříve vytvořenou položku nabídky.</span><span class="sxs-lookup"><span data-stu-id="be787-162">In the tree, select the menu item that you created before.</span></span>
15. <span data-ttu-id="be787-163">Vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="be787-163">Select **Edit**.</span></span>
16. <span data-ttu-id="be787-164">Výběrem šipky přidáte do nabídky danou položku.</span><span class="sxs-lookup"><span data-stu-id="be787-164">Select the arrow to add the menu item to the menu.</span></span>
17. <span data-ttu-id="be787-165">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="be787-165">Select **Save**.</span></span>
18. <span data-ttu-id="be787-166">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="be787-166">Close the page.</span></span>

## <a name="update-a-work-template"></a><span data-ttu-id="be787-167">Aktualizace šablony práce</span><span class="sxs-lookup"><span data-stu-id="be787-167">Update a work template</span></span>
1. <span data-ttu-id="be787-168">V navigačním podokně přejděte na **Moduly > Řízení skladu > Nastavení > Práce > Pracovní šablony**.</span><span class="sxs-lookup"><span data-stu-id="be787-168">Go to **Navigation pane > Modules > Warehouse management > Setup > Work > Work templates**.</span></span>
2. <span data-ttu-id="be787-169">Vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="be787-169">Select **Edit**.</span></span>
3. <span data-ttu-id="be787-170">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="be787-170">Select **New**.</span></span>
4. <span data-ttu-id="be787-171">V poli **Typ práce** vyberte **Tisk**.</span><span class="sxs-lookup"><span data-stu-id="be787-171">In the **Work type** field, select **Print**.</span></span>
5. <span data-ttu-id="be787-172">V poli **ID pracovní třídy** zadejte nebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="be787-172">In the **Work class ID** field, enter or select a value.</span></span>
6. <span data-ttu-id="be787-173">Vyberte **Přesunout nahoru**.</span><span class="sxs-lookup"><span data-stu-id="be787-173">Select **Move up**.</span></span>
7. <span data-ttu-id="be787-174">Zvolte **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="be787-174">Select **Save**.</span></span>
8. <span data-ttu-id="be787-175">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="be787-175">Close the page.</span></span>

