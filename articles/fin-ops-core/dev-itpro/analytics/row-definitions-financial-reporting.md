---
title: Definice řádku v návrháři finanční sestavy
description: Definice řádku je součástí sestavy nebo stavebního bloku, který určuje obsah jednotlivých řádků ve finanční sestavě. Definici řádku lze kombinovat s definicemi sloupců, definicemi stromu výkaznictví a definicemi sestav a vytvořit tak skupinu stavebních bloků, které může používat více společností.
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 68873
ms.assetid: 2fd7b5da-700f-48cb-9003-90c0d82f818f
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 8cc7de1473ed6ec9b93bd880b47b0c25ec5a7262
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185191"
---
# <a name="row-definitions-in-financial-report-designer"></a><span data-ttu-id="d5ac1-104">Definice řádku v návrháři finanční sestavy</span><span class="sxs-lookup"><span data-stu-id="d5ac1-104">Row definitions in financial report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d5ac1-105">Definice řádku je součástí sestavy nebo stavebního bloku, který určuje obsah jednotlivých řádků ve finanční sestavě.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-105">A row definition is a report component, or building block, that specifies the contents of each row on a financial report.</span></span> <span data-ttu-id="d5ac1-106">Definici řádku lze kombinovat s definicemi sloupců, definicemi stromu výkaznictví a definicemi sestav a vytvořit tak skupinu stavebních bloků, které může používat více společností.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-106">A row definition can be combined with column definitions, reporting tree definitions, and report definitions to create a building block group that can be used by multiple companies.</span></span>

## <a name="create-a-row-definition"></a><span data-ttu-id="d5ac1-107">Vytvoření definice řádků</span><span class="sxs-lookup"><span data-stu-id="d5ac1-107">Create a row definition</span></span>

1. <span data-ttu-id="d5ac1-108">V Návrháři sestav v navigačním podokně klikněte na tlačítko **Definice řádku**.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-108">In Report Designer, in the navigation pane, click **Row Definitions**.</span></span>
2. <span data-ttu-id="d5ac1-109">V nabídce **Soubor** klikněte na tlačítko **Nový** a klikněte na možnost **Definice řádku**.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-109">On the **File** menu, click **New**, and then click **Row Definition**.</span></span> <span data-ttu-id="d5ac1-110">Další informace o obsahu každé buňky naleznete v tématu [Úprava buněk definice řádku](modify-row-definition-cells-financial-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="d5ac1-110">For more information about the content of each cell, see [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>

## <a name="open-a-row-definition"></a><span data-ttu-id="d5ac1-111">Otevření definice řádku</span><span class="sxs-lookup"><span data-stu-id="d5ac1-111">Open a row definition</span></span>
1. <span data-ttu-id="d5ac1-112">V Návrháři sestav v navigačním podokně klikněte na tlačítko **Definice řádku**.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-112">In Report Designer, in the navigation pane, click **Row Definitions**.</span></span>
2. <span data-ttu-id="d5ac1-113">Definici řádku otevřete kliknutím dvakrát na její název.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-113">Double-click the name of the row definition to open.</span></span>
3. <span data-ttu-id="d5ac1-114">Chcete-li zobrazit stavební bloky, které jsou přidruženy k definici řádku, klikněte pravým tlačítkem myši na definici řádku a poté vyberte možnost **Přidružení**.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-114">To view any building blocks that are associated with the row definition, right-click the row definition, and then select **Associations**.</span></span>

## <a name="contents-of-a-row-definition"></a><span data-ttu-id="d5ac1-115"> Obsah definice řádku</span><span class="sxs-lookup"><span data-stu-id="d5ac1-115">Contents of a row definition</span></span>
<span data-ttu-id="d5ac1-116">Definice řádku může obsahovat až 20 000 řádků finančních dimenzí a obsahovat následující informace:</span><span class="sxs-lookup"><span data-stu-id="d5ac1-116">A row definition can contain up to 20,000 financial dimension rows and can include the following information:</span></span>

- <span data-ttu-id="d5ac1-117">popisný text, který přidává do sestavy přehlednost vytvořením záhlaví, řádků a mezer pro oddíly, například **Hotovost** nebo **Celkové výnosy**</span><span class="sxs-lookup"><span data-stu-id="d5ac1-117">Descriptive text that adds meaning to the report by creating section headings, lines, and spaces, such as **Cash** or **Total Revenue**</span></span>
- <span data-ttu-id="d5ac1-118">Odkazy na finanční data, která mohou zahrnovat hodnoty dimenze v aplikaci Microsoft Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="d5ac1-118">Links to financial data, which can include dimension values in the Microsoft Dynamics 365 Finance</span></span>

    > [!NOTE]
    > <span data-ttu-id="d5ac1-119">Definici řádků můžete nastavit tak, aby se data ze systému finančních dimenzí načítala při každém generování sestavy.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-119">You can set up a row definition to pull data from the financial dimensions system every time that the report is generated.</span></span>

- <span data-ttu-id="d5ac1-120">Součty a vzorce řádků, které jsou založeny na propojených finančních datech</span><span class="sxs-lookup"><span data-stu-id="d5ac1-120">Row totals and formulas that are based on the linked financial data</span></span>

<span data-ttu-id="d5ac1-121">Obvykle každý řádek v definici řádku obsahuje jeden z následujících typů informací:</span><span class="sxs-lookup"><span data-stu-id="d5ac1-121">Usually, each row in a row definition contains one of the following types of information:</span></span>

- <span data-ttu-id="d5ac1-122">Odkazy na systém finančních dimenzí</span><span class="sxs-lookup"><span data-stu-id="d5ac1-122">References to the financial dimensions system</span></span>
- <span data-ttu-id="d5ac1-123">Součty nebo výpočty založené na údajích</span><span class="sxs-lookup"><span data-stu-id="d5ac1-123">Totals or calculations that are based on the data</span></span>
- <span data-ttu-id="d5ac1-124">Formátování</span><span class="sxs-lookup"><span data-stu-id="d5ac1-124">Formatting</span></span>

<span data-ttu-id="d5ac1-125">Existují dvě metody pro zadávání informací do definice řádku:</span><span class="sxs-lookup"><span data-stu-id="d5ac1-125">There are two methods for entering information in a row definition:</span></span>

- <span data-ttu-id="d5ac1-126">Ručně zadejte informace řádku do nové definice řádku.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-126">Manually enter row information in a new row definition.</span></span> <span data-ttu-id="d5ac1-127">Další informace naleznete v tématu [Úprava buněk definice řádku](modify-row-definition-cells-financial-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="d5ac1-127">For more information, see [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>
- <span data-ttu-id="d5ac1-128">Použijte návrháře sestav k získání informací řádku přímo z finančních dimenzí.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-128">Use report designer to pull row information directly from the financial dimensions.</span></span> <span data-ttu-id="d5ac1-129">Další informace naleznete v části „Související vzorce/řádky/jednotky“ v části [Úprava buněk definice řádku](modify-row-definition-cells-financial-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="d5ac1-129">For more information, see the "Related formulas/rows/units" section in [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>

## <a name="add-dimensions-in-a-row-definition"></a><span data-ttu-id="d5ac1-130"> Přidání dimenzí do definice řádku</span><span class="sxs-lookup"><span data-stu-id="d5ac1-130">Add dimensions in a row definition</span></span>
<span data-ttu-id="d5ac1-131">Dimenze je protnutím dat a hodnot.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-131">A dimension is an intersection of data and values.</span></span> <span data-ttu-id="d5ac1-132">Můžete seskupit data a hodnoty v návrháři sestav.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-132">You can group data and values in report designer.</span></span> <span data-ttu-id="d5ac1-133">Potom můžete klasifikovat a analyzovat transakce podrobněji.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-133">You can then classify and analyze transactions in more detail.</span></span> <span data-ttu-id="d5ac1-134">Můžete použít dialogové okno **Vložit řádky z dimenzí** k přidání více řádků současně do definice řádku.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-134">You can use the **Insert Rows from Dimensions** dialog box to add multiple rows to a row definition at the same time.</span></span> <span data-ttu-id="d5ac1-135">Dialogové okno zobrazí pro každou dimenzi jeden sloupec.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-135">The dialog box displays one column for each dimension.</span></span> <span data-ttu-id="d5ac1-136">Následující tabulka popisuje informace, které můžete zadat do každé z dimenzí.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-136">The following table describes the information that you can specify for each dimension.</span></span>

| <span data-ttu-id="d5ac1-137">Možnost</span><span class="sxs-lookup"><span data-stu-id="d5ac1-137">Option</span></span>                | <span data-ttu-id="d5ac1-138">Popis</span><span class="sxs-lookup"><span data-stu-id="d5ac1-138">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="d5ac1-139">Dimenze</span><span class="sxs-lookup"><span data-stu-id="d5ac1-139">Dimension</span></span>             | <span data-ttu-id="d5ac1-140">Vzor, který identifikuje dimenzi pro přidání definice řádku.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-140">The pattern that identifies the dimension to add to the row definition.</span></span> <span data-ttu-id="d5ac1-141">Tento vzor obsahuje jeden znak ampersand (&) nebo znak křížku (\#) pro každou pozici v dimenzích.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-141">This pattern contains one ampersand (&) or number sign (\#) for each position in the dimensions.</span></span> <span data-ttu-id="d5ac1-142">Obecně byste měli používat všechny ampersandy pro dimenzi hlavního účtu a všechny křížky pro jiné dimenze.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-142">Generally, use all ampersands for the Main Account dimension and all number signs for other dimensions.</span></span> |
| <span data-ttu-id="d5ac1-143">Začátek rozsahu dimenzí</span><span class="sxs-lookup"><span data-stu-id="d5ac1-143">Dimension Range Start</span></span> | <span data-ttu-id="d5ac1-144">První hodnota pro tuto dimenzi, která se má přidat do definice řádku</span><span class="sxs-lookup"><span data-stu-id="d5ac1-144">The first value for this dimension to add to the row definition.</span></span> |
| <span data-ttu-id="d5ac1-145">Konec rozsahu dimenzí</span><span class="sxs-lookup"><span data-stu-id="d5ac1-145">Dimension Range End</span></span>   | <span data-ttu-id="d5ac1-146">Poslední hodnota pro tuto dimenzi k přidání do definice řádku.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-146">The last value for this dimension to add to the row definition.</span></span> |

<span data-ttu-id="d5ac1-147">Chcete-li přidat dimenze do definice řádku, proveďte následující kroky.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-147">To add dimensions to a row definition, follow these steps.</span></span>

1. <span data-ttu-id="d5ac1-148">V Návrháři sestav klikněte na tlačítko **Definice řádku** a potom otevřete definici řádku ke změně.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-148">In Report Designer, click **Row Definitions**, and then open the row definition to modify.</span></span>
2. <span data-ttu-id="d5ac1-149">V nabídce **Upravit** klikněte na tlačítko **Vložit řádky z dimenzí**.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-149">On the **Edit** menu, click **Insert Rows from Dimensions**.</span></span>
3. <span data-ttu-id="d5ac1-150">V dialogovém okně **Vložit řádky z dimenzí** vyberte v řádku **Dimenze** buňku dimenze, která má být převedena do definice řádku, a klikněte na tlačítko **Všechny &&&**.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-150">In the **Insert Rows from Dimensions** dialog box, in the **Dimensions** row, select the cell for the dimension to transfer to the row definition, and then click **All &&&**.</span></span>
4. <span data-ttu-id="d5ac1-151">Chcete-li omezit definici řádku na určitý rozsah hodnot dimenzí, zadejte počáteční hodnotu dimenze do buňky **Počátek rozsahu dimenzí** a poté zadejte konečnou hodnotu dimenze do buňky **Konec rozsahu dimenzí**.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-151">To limit the row definition to a specific range of dimension values, enter the starting dimension value in the **Dimension Range Start** cell, and then enter the ending dimension value in the **Dimension Range End** cell.</span></span> <span data-ttu-id="d5ac1-152">Chcete-li zahrnout všechny hodnoty pro zvolenou dimenzi, ponechte tyto buňky prázdné.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-152">To include all values for the selected dimension, leave these cells empty.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d5ac1-153">V závislosti na tom, jak databáze systému ERP kompletuje data, nemusejí zástupné znaky (\* nebo ?) v rozsazích dimenzí vrátit všechny požadované hodnoty.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-153">Wildcard characters (\* or ?) in dimension ranges might not return all the results that you want, depending on how the ERP database collates data.</span></span>

5. <span data-ttu-id="d5ac1-154">V poli **Kód počátečního řádku** určete kód řádku pro první hodnotu dimenze, která má být přidána do definice řádku.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-154">In the **Starting row code** field, specify the row code for the first dimension value to add to the row definition.</span></span>
6. <span data-ttu-id="d5ac1-155">V poli **Zvýšit každý řádek o** určete mezeru mezi po sobě jdoucími kódy řádků.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-155">In the **Increment each row by** field, specify the gap between consecutive row codes.</span></span> <span data-ttu-id="d5ac1-156">Například pokud je kód prvního řádku 100 a přírůstek je 30, první nové řádky budou mít kódy 100, 130, 160, 190 a 220.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-156">For example, if the first row code is 100, and the increment value is 30, the first new rows have the codes 100, 130, 160, 190, and 220.</span></span> <span data-ttu-id="d5ac1-157">Použijte hodnotu přírůstku, která zajistí dostatek prostoru pro vkládání nových řádků formátu a vzorců.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-157">Use an increment value that provides enough space to insert new format and formula rows.</span></span>
7. <span data-ttu-id="d5ac1-158">Klepněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-158">Click **OK**.</span></span> <span data-ttu-id="d5ac1-159">Pro každý řádek vybrané hodnoty dimenze je přidán jeden řádek do definice řádku.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-159">For each of the selected dimension values, one line is added to the row definition.</span></span>

## <a name="adjust-rounding-in-a-row-definition"></a><span data-ttu-id="d5ac1-160"> Úprava zaokrouhlování v definici řádku</span><span class="sxs-lookup"><span data-stu-id="d5ac1-160">Adjust rounding in a row definition</span></span>
<span data-ttu-id="d5ac1-161">Pokud máte rozvahu, ve které jsou částky zaokrouhleny, součty mohou překračovat zůstatek.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-161">If you have a balance sheet where the amounts are rounded, the totals might not balance.</span></span> <span data-ttu-id="d5ac1-162">Tomuto problému může dojít, pokud například použijete možnost zaokrouhlení v sestavě rozvahy a definice sestavy také určuje zaokrouhlení.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-162">This issue can occur if, for example, you use the rounding option on a balance sheet report and the report definition also specifies rounding.</span></span> <span data-ttu-id="d5ac1-163">Můžete použít možnost **Vyrovnání rozdílů po zaokrouhlení** v definici řádku a vyrovnat tak částky v rozvaze.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-163">You can use the **Rounding adjustment** option in the row definition to balance the amounts in the balance sheets.</span></span> <span data-ttu-id="d5ac1-164">Zaokrouhlení se vypíná nebo upravuje na kartě **Nastavení** v rámci definice sestavy.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-164">You can turn rounding off or modify it on the **Settings** tab of the report definition.</span></span> <span data-ttu-id="d5ac1-165">Způsob zaokrouhlování částek je uveden v následující tabulce.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-165">The following table shows how amounts are rounded.</span></span> <span data-ttu-id="d5ac1-166">V této tabulce se součty řádků 100 a 200 liší, když je zaokrouhlování zapnuto.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-166">In this table, the totals of rows 100 and 200 differ when rounding is turned on.</span></span>

| <span data-ttu-id="d5ac1-167">Kód řádku</span><span class="sxs-lookup"><span data-stu-id="d5ac1-167">Row code</span></span> | <span data-ttu-id="d5ac1-168">Částky bez zaokrouhlení</span><span class="sxs-lookup"><span data-stu-id="d5ac1-168">Amounts without rounding</span></span> | <span data-ttu-id="d5ac1-169">Částka se zaokrouhlením na celé tisíce</span><span class="sxs-lookup"><span data-stu-id="d5ac1-169">Amount with rounding to whole thousands</span></span> |
|----------|--------------------------|-----------------------------------------|
| <span data-ttu-id="d5ac1-170">100</span><span class="sxs-lookup"><span data-stu-id="d5ac1-170">100</span></span>      | <span data-ttu-id="d5ac1-171">3 600</span><span class="sxs-lookup"><span data-stu-id="d5ac1-171">3,600</span></span>                    | <span data-ttu-id="d5ac1-172">4</span><span class="sxs-lookup"><span data-stu-id="d5ac1-172">4</span></span>                                       |
| <span data-ttu-id="d5ac1-173">200</span><span class="sxs-lookup"><span data-stu-id="d5ac1-173">200</span></span>      | <span data-ttu-id="d5ac1-174">3 700</span><span class="sxs-lookup"><span data-stu-id="d5ac1-174">3,700</span></span>                    | <span data-ttu-id="d5ac1-175">4</span><span class="sxs-lookup"><span data-stu-id="d5ac1-175">4</span></span>                                       |
| <span data-ttu-id="d5ac1-176">Celkem</span><span class="sxs-lookup"><span data-stu-id="d5ac1-176">Total</span></span>    | <span data-ttu-id="d5ac1-177">7 300</span><span class="sxs-lookup"><span data-stu-id="d5ac1-177">7,300</span></span>                    | <span data-ttu-id="d5ac1-178">8</span><span class="sxs-lookup"><span data-stu-id="d5ac1-178">8</span></span>                                       |

<span data-ttu-id="d5ac1-179">Chcete-li upravit zaokrouhlování v rozvaze, proveďte následující kroky.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-179">To adjust rounding in a balance sheet, follow these steps.</span></span>

1. <span data-ttu-id="d5ac1-180">V Návrháři sestav klikněte na tlačítko **Definice řádku** a potom otevřete definici řádku ke změně.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-180">In Report Designer, click **Row Definitions**, and then open the row definition to modify.</span></span>
2. <span data-ttu-id="d5ac1-181">V nabídce **Úpravy** klikněte na příkaz **Vyrovnání rozdílů po zaokrouhlení**.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-181">On the **Edit** menu, click **Rounding Adjustment**.</span></span>
3. <span data-ttu-id="d5ac1-182">V dialogovém okně **Vyrovnání rozdílů po zaokrouhlení** zadejte následující hodnoty:</span><span class="sxs-lookup"><span data-stu-id="d5ac1-182">In the **Rounding Adjustments** dialog box, enter the following values:</span></span>

    - <span data-ttu-id="d5ac1-183">**Řádek vyrovnání rozdílů po zaokrouhlení** – kód řádku, který bude upraven kvůli vyrovnání rozvahy.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-183">**Rounding adjustment row** – The row code for the row that should be adjusted to balance the balance sheet.</span></span>
    - <span data-ttu-id="d5ac1-184">**Řádek součtu majetku** – kód řádku v rozvaze, který obsahuje součet majetku.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-184">**Total assets row** – The row code for the row in the balance sheet that contains the total assets.</span></span>
    - <span data-ttu-id="d5ac1-185">**Řádek součtu závazků a jmění** – kód řádku v rozvaze, který obsahuje součet závazků a jmění.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-185">**Total liabilities and equity row** – The row code for the row in the balance sheet that contains the total liabilities and equity.</span></span>
    - <span data-ttu-id="d5ac1-186">**Limit částky úpravy** – limit pro automatické úpravy vyjádřený jako kladné celé číslo.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-186">**Adjustment amount limit** – A positive whole number that specifies the limit on automatic adjustments.</span></span> <span data-ttu-id="d5ac1-187">Tato částka je porovnána s absolutní hodnotou skutečného zaokrouhlovacího rozdílu.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-187">This amount is compared with the absolute value of the actual rounding difference.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d5ac1-188">Tyto kódy řádků musí být propojeny na vaše finanční data.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-188">These row codes must be linked to your financial data.</span></span> <span data-ttu-id="d5ac1-189">Jinými slovy, řádek musí mít hodnotu dimenze ve své buňce **Odkaz na finanční dimenze**.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-189">In other words, the row must have a dimension value in its **Link to Financial Dimensions** cell.</span></span> <span data-ttu-id="d5ac1-190">**Neodkazujte** na řádek popisu (**DESC**), výpočtu (**CALC**) nebo součtu (**TOT**).</span><span class="sxs-lookup"><span data-stu-id="d5ac1-190">Do **not** reference a description (**DESC**), calculated (**CALC**), or totaled (**TOT**) row.</span></span>

<span data-ttu-id="d5ac1-191">Částky ve vaší rozvaze budou vyrovnávány rovnoměrně při zapnutém zaokrouhlování.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-191">The amounts in your balance sheet will now balance evenly when rounding is turned on.</span></span>

> [!NOTE]
> <span data-ttu-id="d5ac1-192">Limit vyrovnání rozdílů po zaokrouhlení je založen na možnosti **Přesnost zaokrouhlování** zadané pro definici sestavy.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-192">The adjustment limit is applied based on the **Rounding precision** option that is specified for the report definition.</span></span> <span data-ttu-id="d5ac1-193">Pokud například vyberete zaokrouhlení sestavy na tisíce a zadáte hodnotu **2** do pole **Limit částky úpravy**, zobrazí se upozornění, když se hodnota identifikovaná v poli **Řádek vyrovnání rozdílů po zaokrouhlení** zvýší nebo sníží o více než 2 000 Kč.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-193">For example, if you round your report to thousands and enter **2** in the **Adjustment amount limit** field, you receive a warning message when the value in the **Rounding adjustment row** field increases or decreases by more than 2,000.</span></span>

## <a name="format-row-and-column-text"></a><span data-ttu-id="d5ac1-194">Formátování textu řádků a sloupců</span><span class="sxs-lookup"><span data-stu-id="d5ac1-194">Format row and column text</span></span>
<span data-ttu-id="d5ac1-195">Změnou písma a formátováním textu můžete přizpůsobit vzhled sestav.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-195">You can customize the appearance of your reports by changing fonts and formatting text.</span></span> <span data-ttu-id="d5ac1-196">Následující části vysvětlují formátování vzhledu řádků a sloupců v sestavách.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-196">The following sections explain how to format the appearance of rows and columns on reports.</span></span>

### <a name="manage-font-styles"></a><span data-ttu-id="d5ac1-197">Správa stylů písem</span><span class="sxs-lookup"><span data-stu-id="d5ac1-197">Manage font styles</span></span>

<span data-ttu-id="d5ac1-198">Můžete vytvořit a upravit styly písem pro sestavy.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-198">You can create and modify font styles for your report.</span></span> <span data-ttu-id="d5ac1-199">Můžete také použít tyto styly pro dokument nebo konkrétní řádek či sloupec v sestavě.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-199">You can then apply those styles to the document, or to a specific row or column on a report.</span></span>

<table>
<tbody>
<tr>
<td><span data-ttu-id="d5ac1-200"><strong>Vytvoření stylu písma</strong></span><span class="sxs-lookup"><span data-stu-id="d5ac1-200"><strong>Create a font style</strong></span></span></td>
<td>
<ol>
<li><span data-ttu-id="d5ac1-201">V Návrháři sestav v nabídce <strong>Formát </strong>klikněte na tlačítko <strong>Styly a formátování</strong>.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-201">In Report Designer, on the <strong>Format</strong> menu, click <strong>Styles and Formatting</strong>.</span></span></li>
<li><span data-ttu-id="d5ac1-202">V dialogovém okně <strong>Styly a formátování</strong> klikněte na položku <strong>Nový</strong> a pak zadejte jedinečný název pro nový styl.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-202">In the <strong>Styles and Formatting</strong> dialog box, click <strong>New</strong>, and then enter a unique name for the new style.</span></span></li>
<li><span data-ttu-id="d5ac1-203">Vyberte požadované možnosti písma a pak klikněte na tlačítko <strong>OK</strong>.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-203">Make your font selections, and then click <strong>OK</strong>.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="d5ac1-204"><strong>Úprava stylu písma</strong></span><span class="sxs-lookup"><span data-stu-id="d5ac1-204"><strong>Modify a font style</strong></span></span></td>
<td>
<ol>
<li><span data-ttu-id="d5ac1-205">V Návrháři sestav v nabídce <strong>Formát </strong>klikněte na tlačítko <strong>Styly a formátování</strong>.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-205">In Report Designer, on the <strong>Format</strong> menu, click <strong>Styles and Formatting</strong>.</span></span></li>
<li><span data-ttu-id="d5ac1-206">V dialogovém okně <strong>Styly a formátování</strong> vyberte styl písma, který chcete upravit, a klikněte na položku <strong>Upravit</strong>.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-206">In the <strong>Styles and Formatting</strong> dialog box, select a style to modify, and then click <strong>Modify</strong>.</span></span></li>
<li><span data-ttu-id="d5ac1-207">Vyberte požadované možnosti písma a pak klikněte na tlačítko <strong>OK</strong>.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-207">Make your font selections, and then click <strong>OK</strong>.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="d5ac1-208"><strong>Použití stylu písma</strong></span><span class="sxs-lookup"><span data-stu-id="d5ac1-208"><strong>Apply a font style</strong></span></span></td>
<td>
<ol>
<li><span data-ttu-id="d5ac1-209">V návrháři sestav v definici či definici sloupce nebo v záhlavích a zápatích vyberte jednu nebo více buněk.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-209">In Report Designer, in a definition or column definition, or in headers and footers, select one or more cells.</span></span></li>
<li><span data-ttu-id="d5ac1-210">V seznamu <strong>Styl</strong> na panelu nástrojů vyberte styl písma.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-210">In the <strong>Style</strong> list on the toolbar, select a font style.</span></span></li>
</ol>
</td>
</tr>
</tbody>
</table>

### <a name="format-row-text"></a><span data-ttu-id="d5ac1-211">Formátování textu řádků</span><span class="sxs-lookup"><span data-stu-id="d5ac1-211">Format row text</span></span>

<span data-ttu-id="d5ac1-212">Formátování určené v definici řádku přepíše formátování určené v definici sloupce a definici sestavy.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-212">The formatting that is specified in the row definition overrides any formatting that is specified in the column definition and the report definition.</span></span> <span data-ttu-id="d5ac1-213">Pomocí ovládacích prvků na panelu nástrojů formátování můžete upravit formát textu.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-213">You can modify the text format by using the controls on the formatting toolbar.</span></span> <span data-ttu-id="d5ac1-214">Tyto ovládací prvky jsou standardní ovládací prvky systému Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-214">These controls are standard Microsoft Windows controls.</span></span>

1. <span data-ttu-id="d5ac1-215">V Návrháři sestav otevřete definici řádků, kterou chcete změnit.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-215">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="d5ac1-216">Vyberte buňky k formátování.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-216">Select the cells to format.</span></span> <span data-ttu-id="d5ac1-217">Chcete-li vybrat více buněk, podržte klávesu Ctrl a vyberte buňky.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-217">To select multiple cells, hold down the Ctrl key while you select the cell.</span></span>
3. <span data-ttu-id="d5ac1-218">Na panelu nástrojů klikněte na tlačítko formátu, který chcete použít.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-218">Click the toolbar button of the format to apply.</span></span> <span data-ttu-id="d5ac1-219">Chcete-li například odsadit řádek, vyberte ho a klikněte na tlačítko **Zvětšit odsazení** ![Zvětšit odsazení](media/indent.gif "Zvětšit odsazení") na panelu nástrojů.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-219">For example, to indent a row, select the row, and then click **Increase Indent** ![Increase Indent](media/indent.gif "Increase Indent") on the toolbar.</span></span>

### <a name="adjust-columns-while-you-design-reports"></a><span data-ttu-id="d5ac1-220">Úprava sloupců během návrhu sestav</span><span class="sxs-lookup"><span data-stu-id="d5ac1-220">Adjust columns while you design reports</span></span>

<span data-ttu-id="d5ac1-221">K usnadnění zobrazování sloupců, se kterými pracujete v definici řádku, můžete upravit šířku sloupce a skrýt (minimalizovat) nebo zobrazit sloupce v podokně náhledu.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-221">To make it easier to view the columns that you're working on in the row definition, you can adjust the width of a column, and can also hide (minimize) or show columns in the view pane.</span></span> <span data-ttu-id="d5ac1-222">Provedené úpravy mají vliv pouze na vzhled zobrazení ve sloupcích.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-222">The modifications that you make affect only the on-screen appearance of the columns.</span></span> <span data-ttu-id="d5ac1-223">Nemají vliv na formátování sloupců v sestavách.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-223">They don't affect the column formatting on reports.</span></span>

### <a name="change-the-width-of-a-column-in-the-view-pane"></a><span data-ttu-id="d5ac1-224">Změna šířky sloupce v podokně náhledu</span><span class="sxs-lookup"><span data-stu-id="d5ac1-224">Change the width of a column in the view pane</span></span>

1. <span data-ttu-id="d5ac1-225">V Návrháři sestav otevřete definici řádku k úpravě.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-225">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="d5ac1-226">V nabídce **Formát** klikněte na příkaz **Šířka sloupce**.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-226">On the **Format** menu, select **Column Width**.</span></span>
3. <span data-ttu-id="d5ac1-227">V dialogovém okně **Šířka sloupce** zadejte hodnotu a klikněte na tlačítko **OK**.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-227">In the **Column Width** dialog box, enter a value, and then click **OK**.</span></span> <span data-ttu-id="d5ac1-228">Případně můžete také přetáhnout pravý okraj buňky záhlaví sloupce a změnit tak šířku sloupce.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-228">Alternatively, you can drag the right boundary of a column heading cell to change the width of the column.</span></span>

### <a name="hide-columns-in-the-view-pane"></a><span data-ttu-id="d5ac1-229">Skrytí sloupců v podokně náhledu</span><span class="sxs-lookup"><span data-stu-id="d5ac1-229">Hide columns in the view pane</span></span>

1. <span data-ttu-id="d5ac1-230">V Návrháři sestav otevřete definici řádku k úpravě.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-230">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="d5ac1-231">Vyberte sloupec nebo sloupce, které chcete minimalizovat.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-231">Select the column or columns to minimize.</span></span>
3. <span data-ttu-id="d5ac1-232">Klikněte pravým tlačítkem myši a poté klikněte na položku **Skrýt**.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-232">Right-click, and then click **Hide**.</span></span>

### <a name="show-all-hidden-columns-in-the-view-pane"></a><span data-ttu-id="d5ac1-233">Zobrazení všech skrytých sloupců v podokně náhledu</span><span class="sxs-lookup"><span data-stu-id="d5ac1-233">Show all hidden columns in the view pane</span></span>

1. <span data-ttu-id="d5ac1-234">V Návrháři sestav otevřete definici řádku k úpravě.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-234">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="d5ac1-235">Klikněte pravým tlačítkem myši na minimalizovaný sloupec, který chcete zobrazit, a klikněte na tlačítko **Zobrazit**.</span><span class="sxs-lookup"><span data-stu-id="d5ac1-235">Right-click the minimized column to display, and then click **Unhide**.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="d5ac1-236">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="d5ac1-236">Additional resources</span></span>

[<span data-ttu-id="d5ac1-237">Finanční výkaznictví</span><span class="sxs-lookup"><span data-stu-id="d5ac1-237">Financial reporting</span></span>](financial-reporting-intro.md)
