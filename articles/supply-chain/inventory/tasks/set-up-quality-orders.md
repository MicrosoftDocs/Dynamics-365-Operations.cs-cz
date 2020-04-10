---
title: Nastavení objednávek kvality
description: Tento postup popisuje povolení procesu řízení kvality, kde musí být příchozí zásoby okamžitě po registraci po doručení prohlédnuty.
author: perlynne
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, InventTestReportSetup, InventTestTable, DefaultDashboard, InventTestVariable, InventTestVariableOutcome, InventItemSampling, InventTestQualityGroup, InventTestItemQualityGroupAdd, SysQueryForm, InventTestItemQualityGroup, InventTestGroup, InventTestAssociationTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9760aeb823730581aa1f02db1574e6f5eccd1f75
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145633"
---
# <a name="set-up-quality-orders"></a><span data-ttu-id="11f5a-103">Nastavení objednávek kvality</span><span class="sxs-lookup"><span data-stu-id="11f5a-103">Set up quality orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="11f5a-104">Tento postup popisuje povolení procesu řízení kvality, kde musí být příchozí zásoby okamžitě po registraci po doručení prohlédnuty.</span><span class="sxs-lookup"><span data-stu-id="11f5a-104">This procedure shows you how to enable a quality management process where incoming inventory must be inspected immediately after arrival registration.</span></span> <span data-ttu-id="11f5a-105">Postup obvykle provádí správce kvality.</span><span class="sxs-lookup"><span data-stu-id="11f5a-105">The procedure will typically be carried out by a quality manager.</span></span> <span data-ttu-id="11f5a-106">Proces zahrnuje vytvoření skupiny kvality, definování položek, které budou testovány, a sestavení skupiny testů, které mají být provedeny u položek ve skupině kvality.</span><span class="sxs-lookup"><span data-stu-id="11f5a-106">The process includes the creation of a quality group, to define the items that are going to be sampled, and a test group to group the tests that are to be performed on items in the quality group.</span></span> <span data-ttu-id="11f5a-107">Tohoto průvodce můžete spustit s ukázkovými daty společnosti USMF.</span><span class="sxs-lookup"><span data-stu-id="11f5a-107">You can run this guide in the USMF demo data company.</span></span>


## <a name="enable-quality-management"></a><span data-ttu-id="11f5a-108">Povolení správy kvality</span><span class="sxs-lookup"><span data-stu-id="11f5a-108">Enable quality management</span></span>
1. <span data-ttu-id="11f5a-109">Přejděte na **Navigační podokno > Moduly > Řízení zásob > Nastavení > Parametry řízení zásob a skladu**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-109">Go to **Navigation pane > Modules > Inventory management > Setup > Inventory and warehouse management parameters**.</span></span>
2. <span data-ttu-id="11f5a-110">Klikněte na kartu **Správa kvality**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-110">Click the **Quality management** tab.</span></span>
3. <span data-ttu-id="11f5a-111">Volbu **Použít správu kvality** nastavte na hodnotu ‚Ano‘.</span><span class="sxs-lookup"><span data-stu-id="11f5a-111">Set the **Use quality management option** to 'Yes'.</span></span>
4. <span data-ttu-id="11f5a-112">Klikněte na **Nastavení sestavy**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-112">Click **Report setup**.</span></span> <span data-ttu-id="11f5a-113">V USMF je nastavení sestavy pro správu kvality již definováno.</span><span class="sxs-lookup"><span data-stu-id="11f5a-113">In USMF, the report setup for quality management is already defined.</span></span> <span data-ttu-id="11f5a-114">Pokud k tomu nedošlo, přidejte zde nové řádky pro různé typy sestav a vyberte typ dokumentu, který má být použit pro každou sestavu.</span><span class="sxs-lookup"><span data-stu-id="11f5a-114">If this wasn't done, you'd add new lines here for the different report types, and select the type of document to be used for each report.</span></span>  
5. <span data-ttu-id="11f5a-115">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="11f5a-115">Close the page.</span></span>
6. <span data-ttu-id="11f5a-116">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="11f5a-116">Close the page.</span></span>

## <a name="create-a-test"></a><span data-ttu-id="11f5a-117">Vytvoření testu</span><span class="sxs-lookup"><span data-stu-id="11f5a-117">Create a test</span></span>
1. <span data-ttu-id="11f5a-118">Přejděte na **Řízení zásob > Nastavení > Řízení kvality > Testy**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-118">Go to **Inventory management > Setup > Quality control > Tests**.</span></span>
2. <span data-ttu-id="11f5a-119">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-119">Click **New**.</span></span>
3. <span data-ttu-id="11f5a-120">Zadejte hodnotu do pole **Test**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-120">In the **Test** field, type a value.</span></span>
4. <span data-ttu-id="11f5a-121">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-121">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="11f5a-122">Vyberte ‚Možnost‘ v poli **Typ**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-122">In the **Type** field, select 'Option'.</span></span> <span data-ttu-id="11f5a-123">V tomto příkladu vyberete Možnost, což nám umožní přiřazení výsledků testu na základě předem definovaných hodnot.</span><span class="sxs-lookup"><span data-stu-id="11f5a-123">In this example, we'll select "Option" which will make it possible to assign the test results based on pre-defined values.</span></span>  
6. <span data-ttu-id="11f5a-124">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-124">Click **Save**.</span></span>
7. <span data-ttu-id="11f5a-125">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="11f5a-125">Close the page.</span></span>

## <a name="create-test-variables-to-define-the-way-test-results-are-recorded"></a><span data-ttu-id="11f5a-126">Vytvoření proměnných testu pro určení způsobu zaznamenávání výsledků testů</span><span class="sxs-lookup"><span data-stu-id="11f5a-126">Create Test variables to define the way test results are recorded</span></span>
1. <span data-ttu-id="11f5a-127">Přejděte na **Řízení zásob > Nastavení > Řízení kvality > Testovací proměnné**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-127">Go to **Inventory management > Setup > Quality control > Test variables**.</span></span>
2. <span data-ttu-id="11f5a-128">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-128">Click **New**.</span></span>
3. <span data-ttu-id="11f5a-129">Zadejte hodnotu do pole **Proměnná**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-129">In the **Variable** field, type a value.</span></span>
4. <span data-ttu-id="11f5a-130">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-130">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="11f5a-131">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-131">Click **Save**.</span></span>
6. <span data-ttu-id="11f5a-132">Klikněte na tlačítko **Výsledky**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-132">Click **Outcomes**.</span></span>
7. <span data-ttu-id="11f5a-133">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-133">Click **New**.</span></span>
8. <span data-ttu-id="11f5a-134">Zadejte hodnotu do pole **Výsledek**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-134">In the **Outcome** field, type a value.</span></span>
9. <span data-ttu-id="11f5a-135">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-135">In the **Description** field, type a value.</span></span>
10. <span data-ttu-id="11f5a-136">Vyberte volbu ‚Úspěch‘ v poli **Stav výsledku**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-136">In the **Outcome status** field, select 'Pass'.</span></span>
11. <span data-ttu-id="11f5a-137">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-137">Click **Save**.</span></span>
12. <span data-ttu-id="11f5a-138">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-138">Click **New**.</span></span>
13. <span data-ttu-id="11f5a-139">Zadejte hodnotu do pole **Výsledek**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-139">In the **Outcome** field, type a value.</span></span>
14. <span data-ttu-id="11f5a-140">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-140">In the **Description** field, type a value.</span></span>
15. <span data-ttu-id="11f5a-141">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-141">Click **Save**.</span></span>
16. <span data-ttu-id="11f5a-142">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="11f5a-142">Close the page.</span></span>
17. <span data-ttu-id="11f5a-143">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="11f5a-143">Close the page.</span></span>

## <a name="set-up-item-sampling"></a><span data-ttu-id="11f5a-144">Nastavení vzorkování zboží</span><span class="sxs-lookup"><span data-stu-id="11f5a-144">Set up item sampling</span></span>
1. <span data-ttu-id="11f5a-145">Přejděte na **Řízení zásob > Nastavení > Řízení kvality > Vzorkování položky**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-145">Go to **Inventory management > Setup > Quality control > Item sampling**.</span></span>
2. <span data-ttu-id="11f5a-146">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-146">Click **New**.</span></span>
3. <span data-ttu-id="11f5a-147">Zadejte hodnotu do pole **Vzorkování položky**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-147">In the **Item sampling** field, type a value.</span></span>
4. <span data-ttu-id="11f5a-148">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-148">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="11f5a-149">Zadejte číslo do pole **Hodnota**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-149">In the **Value** field, enter a number.</span></span> <span data-ttu-id="11f5a-150">Tato hodnota se vztahuje k Určení množství, které je vybráno v přilehlém poli.</span><span class="sxs-lookup"><span data-stu-id="11f5a-150">This value relates to the Quantity specification that's selected in the adjacent field.</span></span>  
6. <span data-ttu-id="11f5a-151">Rozbalte nebo sbalte oddíl **Zpracování**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-151">Expand or collapse the **Process** section.</span></span>
7. <span data-ttu-id="11f5a-152">Zaškrtněte políčko **Úplné blokování** nebo jeho zaškrtnutí zrušte.</span><span class="sxs-lookup"><span data-stu-id="11f5a-152">Select or clear the **Full blocking** check box.</span></span> <span data-ttu-id="11f5a-153">Pokud vyberete tuto možnost a test se nezdařil, je blokováno celé množství řádku šarže nebo zakázky.</span><span class="sxs-lookup"><span data-stu-id="11f5a-153">If you select this option, the whole lot or order line quantity is blocked if a test is failed.</span></span> <span data-ttu-id="11f5a-154">Pokud pole nevyberete, pouze položky v rámci objednávky kvality jsou blokovány.</span><span class="sxs-lookup"><span data-stu-id="11f5a-154">If you don't select it, only the items in the quality order are blocked.</span></span>  
8. <span data-ttu-id="11f5a-155">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-155">Click **Save**.</span></span>
9. <span data-ttu-id="11f5a-156">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="11f5a-156">Close the page.</span></span>

## <a name="create-a-quality-group"></a><span data-ttu-id="11f5a-157">Vytvoření skupiny kvality</span><span class="sxs-lookup"><span data-stu-id="11f5a-157">Create a quality group</span></span>
1. <span data-ttu-id="11f5a-158">Přejděte na **Řízení zásob > Nastavení > Řízení kvality > Skupiny kvality**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-158">Go to **Inventory management > Setup > Quality control > Quality groups**.</span></span>
2. <span data-ttu-id="11f5a-159">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-159">Click **New**.</span></span>
3. <span data-ttu-id="11f5a-160">Zadejte hodnotu do pole **Skupiny kvality**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-160">In the **Quality group** field, type a value.</span></span> <span data-ttu-id="11f5a-161">Popisný název usnadňuje identifikaci toho, které druhy položek skupina obsahuje (kritéria vzorkování).</span><span class="sxs-lookup"><span data-stu-id="11f5a-161">Use a descriptive name to help you identify which kind of items the group will contain (your sampling criteria).</span></span>  
4. <span data-ttu-id="11f5a-162">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-162">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="11f5a-163">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-163">Click **Save**.</span></span>
6. <span data-ttu-id="11f5a-164">Klikněte na možnost **Přidat položky**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-164">Click **Add items**.</span></span>
7. <span data-ttu-id="11f5a-165">Vyberte řádek **Číslo položky**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-165">Select the **Item number** row.</span></span> <span data-ttu-id="11f5a-166">V tomto příkladu filtrování bude spuštěno podle čísla položky.</span><span class="sxs-lookup"><span data-stu-id="11f5a-166">In this example the filtering will be run based on  the item number.</span></span>  
8. <span data-ttu-id="11f5a-167">Zadejte hodnotu do pole **Kritéria**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-167">In the **Criteria** field, type a value.</span></span> <span data-ttu-id="11f5a-168">Pokud například zadáte T\*, dojde k filtrování čísel položek pouze na ty, které začínají na písmeno T.</span><span class="sxs-lookup"><span data-stu-id="11f5a-168">For example, type T\* to filter on the item numbers that start with T.</span></span>  
9. <span data-ttu-id="11f5a-169">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-169">Click **OK**.</span></span>
10. <span data-ttu-id="11f5a-170">Klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-170">Click **OK**.</span></span>
11. <span data-ttu-id="11f5a-171">Klikněte na **Skupiny kvality zboží**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-171">Click **Item quality groups**.</span></span>
12. <span data-ttu-id="11f5a-172">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="11f5a-172">Close the page.</span></span>
13. <span data-ttu-id="11f5a-173">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="11f5a-173">Close the page.</span></span>

## <a name="create-a-test-group"></a><span data-ttu-id="11f5a-174">Vytvoření testovací skupiny</span><span class="sxs-lookup"><span data-stu-id="11f5a-174">Create a test group</span></span>
1. <span data-ttu-id="11f5a-175">Přejděte na **Řízení zásob > Nastavení > Řízení kvality > Testovací skupiny**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-175">Go to **Inventory management > Setup > Quality control > Test groups**.</span></span>
2. <span data-ttu-id="11f5a-176">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-176">Click **New**.</span></span>
3. <span data-ttu-id="11f5a-177">Zadejte hodnotu do pole **Testovací skupiny**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-177">In the **Test group** field, type a value.</span></span> <span data-ttu-id="11f5a-178">Udělte **Testovací skupině** název, který vám pomůže zapamatovat, jaké testy budou spuštěny, a se kterou skupinou kvality by měla být přidružena.</span><span class="sxs-lookup"><span data-stu-id="11f5a-178">Give the **Test group** a name that will help you remember what kind of tests are being run, and which quality group it should be associated with.</span></span> <span data-ttu-id="11f5a-179">Například pokud ji budete používat se skupinou kvality, která vybírá položky začínající na „T“, mohli byste ji nazvat „Testy položek T“.</span><span class="sxs-lookup"><span data-stu-id="11f5a-179">For example, it it's to be used with a quality group that selects items starting with "T", you could call it "T-item tests".</span></span>  
4. <span data-ttu-id="11f5a-180">Zadejte hodnotu do pole **Popis**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-180">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="11f5a-181">V poli **Vzorkování položky** vyberte řádek vzorkování položky, který jste vytvořili dříve.</span><span class="sxs-lookup"><span data-stu-id="11f5a-181">In the **Item sampling** field, select the item sampling line that you created before.</span></span>
6. <span data-ttu-id="11f5a-182">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="11f5a-182">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="11f5a-183">Klikněte na tlačítko **Přidat**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-183">Click **Add**.</span></span>
8. <span data-ttu-id="11f5a-184">V poli **Pořadové číslo** zadejte číslo.</span><span class="sxs-lookup"><span data-stu-id="11f5a-184">In the **Sequence number** field, enter a number.</span></span>
9. <span data-ttu-id="11f5a-185">V poli **Test** vyberte test vytvořený dříve.</span><span class="sxs-lookup"><span data-stu-id="11f5a-185">In the **Test** field, select the test that you created earlier.</span></span>
10. <span data-ttu-id="11f5a-186">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="11f5a-186">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="11f5a-187">Klepněte na kartu **Test**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-187">Click the **Test** tab.</span></span>
12. <span data-ttu-id="11f5a-188">V poli **Proměnná** vyberte proměnnou testu vytvořenou dříve</span><span class="sxs-lookup"><span data-stu-id="11f5a-188">In the **Variable** field, select the test variable that you created before</span></span>
13. <span data-ttu-id="11f5a-189">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="11f5a-189">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="11f5a-190">V poli **Výchozí výsledek** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="11f5a-190">In the **Default outcome** field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="11f5a-191">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="11f5a-191">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="11f5a-192">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-192">Click **Save**.</span></span>
17. <span data-ttu-id="11f5a-193">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="11f5a-193">Close the page.</span></span>

## <a name="define-when-quality-orders-will-be-created"></a><span data-ttu-id="11f5a-194">Určení toho, kdy budou vytvořeny objednávky kvality</span><span class="sxs-lookup"><span data-stu-id="11f5a-194">Define when quality orders will be created</span></span>
1. <span data-ttu-id="11f5a-195">Přejděte na **Řízení zásob > Nastavení > Řízení kvality > Přiřazení kvality**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-195">Go to **Inventory management > Setup > Quality control > Quality associations**.</span></span>
2. <span data-ttu-id="11f5a-196">Klepněte na možnost **Nový**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-196">Click **New**.</span></span>
3. <span data-ttu-id="11f5a-197">Vyberte volbu v poli **Typ odkazu**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-197">In the **Reference type** field, select an option.</span></span>
4. <span data-ttu-id="11f5a-198">V poli **Kód položky** vyberte Skupina.</span><span class="sxs-lookup"><span data-stu-id="11f5a-198">In the **Item code** field, select 'Group'.</span></span> <span data-ttu-id="11f5a-199">V tomto příkladu nyní vybereme „Skupina“ a použijeme dříve vytvořenou skupinu kvality.</span><span class="sxs-lookup"><span data-stu-id="11f5a-199">In this example, we'll select "Group" and use the quality group we created before.</span></span> <span data-ttu-id="11f5a-200">Můžete zde také nastavte možnost "Tabulka" a určit tak položky ručně, nebo vybrat "Vše" a přidat všechny položky do objednávky kvality.</span><span class="sxs-lookup"><span data-stu-id="11f5a-200">You could also set this to "Table" to specify the items manually, or select "All" to add all items to the quality order.</span></span>  
5. <span data-ttu-id="11f5a-201">V poli **Položka** vyberte skupinu kvality, kterou jste vytvořili dříve.</span><span class="sxs-lookup"><span data-stu-id="11f5a-201">In the **Item** field, select the quality group that you created before.</span></span> <span data-ttu-id="11f5a-202">Možnosti dostupné v poli Položka závisí na nastavení v poli Kód položky.</span><span class="sxs-lookup"><span data-stu-id="11f5a-202">The options available in the Item field depend on what you set in the Item code field.</span></span>  
6. <span data-ttu-id="11f5a-203">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="11f5a-203">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="11f5a-204">Rozbalte nebo sbalte oddíl Zpracování.</span><span class="sxs-lookup"><span data-stu-id="11f5a-204">Expand or collapse the Process section.</span></span>
8. <span data-ttu-id="11f5a-205">Vyberte možnost v poli **Typ události**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-205">In the **Event type** field, select an option.</span></span> <span data-ttu-id="11f5a-206">Toto je událost, která spustí test.</span><span class="sxs-lookup"><span data-stu-id="11f5a-206">This is the event that triggers the test.</span></span> <span data-ttu-id="11f5a-207">Možnosti zde dostupné závisí na procesu, který jste vybrali v poli Typu odkazu.</span><span class="sxs-lookup"><span data-stu-id="11f5a-207">The options available here depend on which process you selected in the Reference type field.</span></span>  
9. <span data-ttu-id="11f5a-208">Vyberte volbu v poli **Spuštění**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-208">In the **Execution** field, select an option.</span></span>
10. <span data-ttu-id="11f5a-209">Rozbalte nebo sbalte oddíl **Proces objednávky kvality**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-209">Expand or collapse the **Quality order process** section.</span></span>
11. <span data-ttu-id="11f5a-210">V poli **Blokování události** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.</span><span class="sxs-lookup"><span data-stu-id="11f5a-210">In the **Event blocking** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="11f5a-211">Toto pole zobrazí seznam procesů, které je možné blokovat, pokud je objednávka kvality stále otevřená.</span><span class="sxs-lookup"><span data-stu-id="11f5a-211">This field shows the list of processes that it's possible to block if the quality order is still open.</span></span> <span data-ttu-id="11f5a-212">Možnosti závisí na vybrané možnosti v poli Typ události.</span><span class="sxs-lookup"><span data-stu-id="11f5a-212">The options depend on what you selected in the Event type field.</span></span>  
12. <span data-ttu-id="11f5a-213">Klikněte na odkaz na vybraném řádku v seznamu.</span><span class="sxs-lookup"><span data-stu-id="11f5a-213">In the list, click the link in the selected row.</span></span> <span data-ttu-id="11f5a-214">To závisí na předchozích vybraných hodnotách.</span><span class="sxs-lookup"><span data-stu-id="11f5a-214">This will be depending on the previous selected values.</span></span> <span data-ttu-id="11f5a-215">Určete, zda následující procesy musí být blokovány, zatímco jsou otevřené objednávky kvality připojeny k řádku zdrojového dokumentu.</span><span class="sxs-lookup"><span data-stu-id="11f5a-215">Select if the following processes must be blocked while having open quality orders linked to a source document line.</span></span>  
13. <span data-ttu-id="11f5a-216">Rozbalte nebo sbalte oddíl **Specifikace**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-216">Expand or collapse the **Specifications** section.</span></span>
14. <span data-ttu-id="11f5a-217">V poli **Testovací skupina** vyberte skupinu testu vytvořenou dříve.</span><span class="sxs-lookup"><span data-stu-id="11f5a-217">In the **Test group** field, select the test group that you created before.</span></span>
15. <span data-ttu-id="11f5a-218">Vyhledejte na seznamu požadovaný záznam a vyberte ho.</span><span class="sxs-lookup"><span data-stu-id="11f5a-218">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="11f5a-219">Klikněte na možnost **Uložit**.</span><span class="sxs-lookup"><span data-stu-id="11f5a-219">Click **Save**.</span></span>
17. <span data-ttu-id="11f5a-220">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="11f5a-220">Close the page.</span></span>

