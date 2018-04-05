---
title: "Šablony plánování rozpočtu pro Excel"
description: "Toto téma popisuje, jak vytvořit šablony aplikace Microsoft Excel, které lze použít pro plány rozpočtu."
author: ryansandness
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetPlanSetLayout
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 261794
ms.assetid: 1d8e99c1-b70d-41ba-991e-ab50b16797e0
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 156688b705337331e083ebc19fded57b028acb67
ms.contentlocale: cs-cz
ms.lasthandoff: 03/26/2018

---

# <a name="budget-planning-templates-for-excel"></a><span data-ttu-id="db440-103">Šablony plánování rozpočtu pro Excel</span><span class="sxs-lookup"><span data-stu-id="db440-103">Budget planning templates for Excel</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="db440-104">Toto téma popisuje, jak vytvořit šablony aplikace Microsoft Excel, které lze použít pro plány rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="db440-104">This topic describes how to create Microsoft Excel templates that can be used with budget plans.</span></span>

<span data-ttu-id="db440-105">Toto téma ukazuje, jak vytvořit šablony aplikace Excel, které budou použity s plány rozpočtu pomocí standardní sady ukázkových dat a přihlášení uživatele admin.</span><span class="sxs-lookup"><span data-stu-id="db440-105">This topic shows how to create Excel templates that will be used with budget plans using the standard demo data set and the Admin user login.</span></span> <span data-ttu-id="db440-106">Další informace o plánování rozpočtu naleznete v tématu [Přehled plánování rozpočtu.](budget-planning-overview-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="db440-106">For more information about budget planning, see [Budget planning overview.](budget-planning-overview-configuration.md)</span></span> <span data-ttu-id="db440-107">Můžete také postupovat podle kurzu [Plánování rozpočtu 101](budget-plan.md) a naučit se konfiguraci základního modulu a zásady a použití.</span><span class="sxs-lookup"><span data-stu-id="db440-107">You can also follow the [Budget planning 101](budget-plan.md) tutorial to learn basic module configuration and usage principles.</span></span>

## <a name="generate-a-worksheet-using-budget-plan-document-layout"></a><span data-ttu-id="db440-108">Vygenerování listu pomocí rozvržení dokumentu plánu rozpočtu</span><span class="sxs-lookup"><span data-stu-id="db440-108">Generate a worksheet using budget plan document layout</span></span>

<span data-ttu-id="db440-109">Dokumenty plánu rozpočtu lze zobrazit a upravit pomocí jednoho nebo více rozvržení.</span><span class="sxs-lookup"><span data-stu-id="db440-109">Budget plan documents can be viewed and edited using one or more layouts.</span></span> <span data-ttu-id="db440-110">Každé rozvržení může mít přidruženou šablonu dokumentu rozpočtu plánu pro zobrazení a úpravy dat plánu rozpočtu v listu aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="db440-110">Each layout can have an associated budget plan document template to view and edit the budget plan data in an Excel worksheet.</span></span> <span data-ttu-id="db440-111">V tomto tématu budou generovány šablonu dokumentu plánu rozpočtu pomocí stávající konfigurace rozvržení.</span><span class="sxs-lookup"><span data-stu-id="db440-111">In this topic, a budget plan document template will be generated using an existing layout configuration.</span></span> 

1. <span data-ttu-id="db440-112">Otevřete **Seznam plánů rozpočtu** (**Rozpočtování** &gt; **Plány rozpočtu**).</span><span class="sxs-lookup"><span data-stu-id="db440-112">Open the **Budget plans list** (**Budgeting** &gt; **Budget plans**).</span></span> 
2. <span data-ttu-id="db440-113">Kliknutím na možnost **Nový** vytvořte nový dokument plánu rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="db440-113">Click **New** to create a new budget plan document.</span></span> 

  <span data-ttu-id="db440-114">[![Seznam plánů rozpočtu](./media/bpt11-1024x552.png)](./media/bpt11.png)</span><span class="sxs-lookup"><span data-stu-id="db440-114">[![Budget plans list](./media/bpt11-1024x552.png)](./media/bpt11.png)</span></span> 

3. <span data-ttu-id="db440-115">Použijte možnost řádku **Přidat** k přidání řádků.</span><span class="sxs-lookup"><span data-stu-id="db440-115">Use the **Add** line option to add lines.</span></span> <span data-ttu-id="db440-116">Klikněte na možnost **Rozvržení**, abyste zobrazili konfiguraci rozvržení dokumentu plánu rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="db440-116">Click **Layouts** to view the budget plan document layout configuration.</span></span> 

  <span data-ttu-id="db440-117">[![Přidání plánů rozpočtu](./media/bpt2-1024x274.png)](./media/bpt2.png)</span><span class="sxs-lookup"><span data-stu-id="db440-117">[![Budget plans add](./media/bpt2-1024x274.png)](./media/bpt2.png)</span></span> 

<span data-ttu-id="db440-118">Můžete zkontrolovat konfiguraci rozvržení a podle potřeby ji upravit.</span><span class="sxs-lookup"><span data-stu-id="db440-118">You can review the layout configuration and adjust it as needed.</span></span> 
1. <span data-ttu-id="db440-119">Přejděte na možnosti **Šablona**&gt;**Generovat** k vytvoření souboru aplikace Excel pro toto rozvržení.</span><span class="sxs-lookup"><span data-stu-id="db440-119">Go to **Template** &gt; **Generate** to create an Excel file for this layout.</span></span> 
2. <span data-ttu-id="db440-120">Po vytvoření šablony přejděte na položky **Šablona**&gt;**Zobrazit** a otevřete a zkontrolujte šablonu dokumentu plánu rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="db440-120">After the template is generated, go to **Template** &gt; **View** to open and review the budget plan document template.</span></span> <span data-ttu-id="db440-121">Soubor aplikace Excel můžete uložit na místní disk.</span><span class="sxs-lookup"><span data-stu-id="db440-121">You can save the Excel file to your local drive.</span></span> 

<span data-ttu-id="db440-122">[![Uložit jako](./media/bpt3-1024x545.png)](./media/bpt3.png)</span><span class="sxs-lookup"><span data-stu-id="db440-122">[![Save as](./media/bpt3-1024x545.png)](./media/bpt3.png)</span></span>

> [!NOTE] 
> <span data-ttu-id="db440-123">Poté, co přidružíte k rozvržení dokumentu plánu rozpočtu šablonu aplikace Excel, nemůžete už rozvržení upravovat.</span><span class="sxs-lookup"><span data-stu-id="db440-123">The Budget plan document layout cannot be edited after an Excel template is associated with it.</span></span> <span data-ttu-id="db440-124">Chcete-li změnit rozvržení, odstraňte přidružený soubor šablony aplikace Excel a vygenerujte ho znovu.</span><span class="sxs-lookup"><span data-stu-id="db440-124">To modify the layout, delete the associated Excel template file and regenerate it.</span></span> <span data-ttu-id="db440-125">Tato možnost je vyžadována pro zachování polí v rozvržení a synchronizaci listů.</span><span class="sxs-lookup"><span data-stu-id="db440-125">This is required to keep the fields in the layout and the worksheet synchronized.</span></span> 

<span data-ttu-id="db440-126">Šablona aplikace Excel bude obsahovat všechny prvky z rozložení dokumentu plánu rozpočtu, kde sloupec **Dostupné v listu** je nastaven na hodnotu True.</span><span class="sxs-lookup"><span data-stu-id="db440-126">The Excel template will contain all of the elements from the budget plan document layout, where the **Available in Worksheet** column is set to True.</span></span> <span data-ttu-id="db440-127">Překrývající se prvky nejsou v šabloně aplikace Excel povoleny.</span><span class="sxs-lookup"><span data-stu-id="db440-127">Overlapping elements are not allowed in the Excel template.</span></span> <span data-ttu-id="db440-128">Například pokud rozvržení obsahuje sloupce Žádost na 1. čtvrtletí, Žádost na 2. čtvrtletí, Žádost na 3. čtvrtletí a Žádost na 4. čtvrtletí a sloupec celkového požadavku, který představuje součet všech čtyřech sloupců čtvrtletí, lze v šabloně aplikace Excel použít pouze čtvrtletní sloupce nebo sloupec součtu.</span><span class="sxs-lookup"><span data-stu-id="db440-128">For example, if the layout contains Request Q1, Request Q2, Request Q3, and Request Q4 columns, and a total request column that represents a sum of all 4 quarterly columns, only the quarterly columns or total column is available to be used in the Excel template.</span></span> <span data-ttu-id="db440-129">Soubor aplikace Excel nemůže aktualizovat překrývající se sloupce se během aktualizace, protože data v tabulce by se mohla stát zastaralá a nepřesná.</span><span class="sxs-lookup"><span data-stu-id="db440-129">The Excel file cannot update overlapping columns during the update because data in the table could become out of date and inaccurate.</span></span>

<span data-ttu-id="db440-130">[![Příklad](./media/bpt4-1024x615.png)](./media/bpt4.png)</span><span class="sxs-lookup"><span data-stu-id="db440-130">[![Example](./media/bpt4-1024x615.png)](./media/bpt4.png)</span></span>

> [!NOTE] 
> <span data-ttu-id="db440-131">Chcete-li předejít možným problémům se zobrazením a úpravami dat plánu rozpočtu při použití aplikace Excel, měl by být přihlášen do aplikace Microsoft Dynamics 365 for Finance and Operations a datového konektoru doplňku Microsoft Dynamics pro Office stejný uživatel.</span><span class="sxs-lookup"><span data-stu-id="db440-131">To avoid potential issues with viewing and editing budget plan data using Excel, the same user should be logged into both Microsoft Dynamics 365 for Finance and Operations and the Microsoft Dynamics Office Add-in Data Connector.</span></span>

## <a name="add-a-header-to-budget-plan-document-template"></a><span data-ttu-id="db440-132">Přidání záhlaví do šablony dokumentu plánu rozpočtu</span><span class="sxs-lookup"><span data-stu-id="db440-132">Add a header to budget plan document template</span></span>
<span data-ttu-id="db440-133">Chcete-li přidat informace záhlaví, vyberte horní řádek v souboru aplikace Excel a vložte prázdné řádky.</span><span class="sxs-lookup"><span data-stu-id="db440-133">To add header information, select the top row in the Excel file and insert empty rows.</span></span> <span data-ttu-id="db440-134">Klikněte na tlačítko **Návrh** v **datovém konektoru**, pokud chcete přidat pole záhlaví do souboru aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="db440-134">Click **Design** in the **Data Connector** to add header fields to the Excel file.</span></span>

<span data-ttu-id="db440-135">[![bpt5](./media/bpt5-1024x615.png)](./media/bpt5.png)</span><span class="sxs-lookup"><span data-stu-id="db440-135">[![bpt5](./media/bpt5-1024x615.png)](./media/bpt5.png)</span></span> 

<span data-ttu-id="db440-136">Na kartě **Návrh** klikněte na pole **Přidat** a pak vyberte **BudgetPlanHeader** jako zdroj dat entity.</span><span class="sxs-lookup"><span data-stu-id="db440-136">In the **Design** tab, click **Add** fields, and then select **BudgetPlanHeader** as the entity data source.</span></span>

<span data-ttu-id="db440-137">[![bpt6](./media/bpt6-1024x615.png)](./media/bpt6.png)</span><span class="sxs-lookup"><span data-stu-id="db440-137">[![bpt6](./media/bpt6-1024x615.png)](./media/bpt6.png)</span></span>

<span data-ttu-id="db440-138">Kurzor přejděte do požadovaného umístění v souboru aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="db440-138">Point the cursor to the desired location in the Excel file.</span></span> <span data-ttu-id="db440-139">Chcete-li přidat popisek pole do vybraného umístění, klikněte na tlačítko **Přidat popisek**.</span><span class="sxs-lookup"><span data-stu-id="db440-139">Click **Add label** to add the field label to the selected location.</span></span> <span data-ttu-id="db440-140">Chcete-li přidat pole hodnoty na vybrané místo, zvolte možnost **Přidat hodnotu**.</span><span class="sxs-lookup"><span data-stu-id="db440-140">Select **Add Value** to add the value field to the selected place.</span></span> <span data-ttu-id="db440-141">Kliknutím na tlačítko **Hotovo** ukončíte návrháře.</span><span class="sxs-lookup"><span data-stu-id="db440-141">Click **Done** to close the designer.</span></span>

## <a name="bpt7mediabpt7pngmediabpt7png"></a><span data-ttu-id="db440-142">[![bpt7](./media/bpt7.png)](./media/bpt7.png)</span><span class="sxs-lookup"><span data-stu-id="db440-142">[![bpt7](./media/bpt7.png)](./media/bpt7.png)</span></span>

<a name="add-a-calculated-column-to-budget-plan-document-template-table"></a><span data-ttu-id="db440-143">Přidání vypočteného sloupce do tabulky šablony dokumentu plánu rozpočtu</span><span class="sxs-lookup"><span data-stu-id="db440-143">Add a calculated column to budget plan document template table</span></span>
--------------------------------------------------------------

<span data-ttu-id="db440-144">Poté se přidají vypočtené sloupce do vygenerované šablony dokumentu rozpočtu plánu.</span><span class="sxs-lookup"><span data-stu-id="db440-144">Next, calculated columns will be added to generated budget plan document template.</span></span> <span data-ttu-id="db440-145">Sloupec **Celkový požadavek**, který obsahuje souhrn sloupců požadavků na první až čtvrté čtvrtletí, a sloupec **Úprava**, který přepočítá sloupec **Celkový požadavek** předdefinovaným koeficientem.</span><span class="sxs-lookup"><span data-stu-id="db440-145">A **Total request** column, which summarizes Request Q1: Request Q4 columns, and an **Adjustment** column, which recalculates the **Total Request** column by a predefined factor.</span></span>

<span data-ttu-id="db440-146">Klikněte na tlačítko **Návrh** v **datovém konektoru**, pokud chcete přidat sloupce do tabulky.</span><span class="sxs-lookup"><span data-stu-id="db440-146">Click **Design** in the **Data connector** to add columns to the table.</span></span> <span data-ttu-id="db440-147">Klikněte na tlačítko **Upravit** vedle zdroje dat **BudgetPlanWorksheet** a začněte přidávat sloupce.</span><span class="sxs-lookup"><span data-stu-id="db440-147">Click **Edit** next to **BudgetPlanWorksheet** data source to start adding columns.</span></span>

<span data-ttu-id="db440-148">[![bpt8](./media/bpt8-1024x301.png)](./media/bpt8.png)</span><span class="sxs-lookup"><span data-stu-id="db440-148">[![bpt8](./media/bpt8-1024x301.png)](./media/bpt8.png)</span></span> 

<span data-ttu-id="db440-149">Vybraná skupina polí zobrazuje sloupce, které jsou k dispozici v šabloně.</span><span class="sxs-lookup"><span data-stu-id="db440-149">The selected field group displays the columns that are available in the template.</span></span> <span data-ttu-id="db440-150">Kliknutím na **Vzorec** přidejte nový sloupec.</span><span class="sxs-lookup"><span data-stu-id="db440-150">Click **Formula** to add a new column.</span></span> <span data-ttu-id="db440-151">Zadejte název nového sloupce a poté vložte vzorec do pole **Vzorec**.</span><span class="sxs-lookup"><span data-stu-id="db440-151">Name the new column and then paste the formula into the **Formula** field.</span></span> <span data-ttu-id="db440-152">Kliknutím na položku **Aktualizovat** vložte sloupec.</span><span class="sxs-lookup"><span data-stu-id="db440-152">Click **Update** to insert the column.</span></span>

<span data-ttu-id="db440-153">[![bpt12](./media/bpt12-1024x565.png)](./media/bpt12.png)</span><span class="sxs-lookup"><span data-stu-id="db440-153">[![bpt12](./media/bpt12-1024x565.png)](./media/bpt12.png)</span></span>

> [!NOTE] 
> <span data-ttu-id="db440-154">Abyste definovali vzorec, vytvořte vzorec v tabulce a zkopírujte ho do okna **Návrh**.</span><span class="sxs-lookup"><span data-stu-id="db440-154">To define the formula, create the formula in the spreadsheet, and then copy it to the **Design** window.</span></span> <span data-ttu-id="db440-155">Tabulka vázaná na aplikaci Finance and Operations se obvykle nazývá "AXTable1".</span><span class="sxs-lookup"><span data-stu-id="db440-155">A Finance and Operations bound table will typically be named "AXTable1".</span></span> <span data-ttu-id="db440-156">Například k sumarizaci sloupců požadavků na první až čtvrté čtvrtletí v tabulce je vzorec = AxTable1\[Požadavek na 1. čtvrtletí\]+ AxTable1\[Požadavek na 2. čtvrtletí\]+ AxTable1\[Požadavek na 3. čtvrtletí\]+ AxTable1\[Požadavek na 4. čtvrtletí\].</span><span class="sxs-lookup"><span data-stu-id="db440-156">For example, to summarize Request Q1 : Request Q4 columns in the spreadsheet, the formula = AxTable1\[Request Q1\]+AxTable1\[Request Q2\]+AxTable1\[Request Q3\]+AxTable1\[Request Q4\].</span></span>

<span data-ttu-id="db440-157">Opakujte tyto kroky pro vložení sloupce **Úprava**.</span><span class="sxs-lookup"><span data-stu-id="db440-157">Repeat these steps to insert the **Adjustment** column.</span></span> <span data-ttu-id="db440-158">Použijte vzorec = AxTable1\[Celkový požadavek\]\*$I$ 1 pro tento sloupec.</span><span class="sxs-lookup"><span data-stu-id="db440-158">Use formula = AxTable1\[Total request\]\*$I$1 for this column.</span></span> <span data-ttu-id="db440-159">Vezme se hodnota v buňce I1 a vynásobí se hodnoty ve sloupci **Celkový požadavek** pro výpočet částek úprav.</span><span class="sxs-lookup"><span data-stu-id="db440-159">This will take the value in cell I1 and multiply the values in the **Total request** column to calculate adjustment amounts.</span></span>

<span data-ttu-id="db440-160">Uložte a zavřete soubor aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="db440-160">Save and close the Excel file.</span></span> <span data-ttu-id="db440-161">Vraťte se aplikace Finance and Operations a v **Rozvržení** klikněte na **Šablona &gt; Odeslat** k odeslání uložené šablony aplikace Excel, která se použije pro plán rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="db440-161">Return to Finance and Operations, and in **Layouts**, click **Template &gt; Upload** to upload the saved Excel template to be used for the budget plan.</span></span> 

<span data-ttu-id="db440-162">[![bpt10](./media/bpt10-1024x352.png)](./media/bpt10.png)</span><span class="sxs-lookup"><span data-stu-id="db440-162">[![bpt10](./media/bpt10-1024x352.png)](./media/bpt10.png)</span></span> 

<span data-ttu-id="db440-163">Zavřete posuvník **Rozvržení**.</span><span class="sxs-lookup"><span data-stu-id="db440-163">Close the **Layouts** slider.</span></span> <span data-ttu-id="db440-164">Chcete-li zobrazit a upravit dokument v aplikaci Excel, v dokumentu **Plán rozpočtu** klikněte na tlačítko **List**.</span><span class="sxs-lookup"><span data-stu-id="db440-164">In **Budget plan** document, click **Worksheet** to view and edit the document in Excel.</span></span> <span data-ttu-id="db440-165">Všimněte si, že upravená šablona aplikace Excel byla použita k vytvoření tohoto listu plánu rozpočtu a vypočtené sloupce jsou aktualizovány pomocí vzorců, které byly definovány v předchozích krocích.</span><span class="sxs-lookup"><span data-stu-id="db440-165">Note that the adjusted Excel template was used to create this budget plan worksheet and calculated columns are updated using the formulas that were defined in the previous steps.</span></span> 

<span data-ttu-id="db440-166">[![bpt11](./media/bpt111-1024x431.png)](./media/bpt111.png)</span><span class="sxs-lookup"><span data-stu-id="db440-166">[![bpt11](./media/bpt111-1024x431.png)](./media/bpt111.png)</span></span>

## <a name="tips--tricks-for-creating-budget-plan-templates"></a><span data-ttu-id="db440-167">Tipy a triky pro vytvoření šablon plánu rozpočtu</span><span class="sxs-lookup"><span data-stu-id="db440-167">Tips & tricks for creating budget plan templates</span></span>
### <a name="can-i-add-and-use-additional-data-sources-to-a-budget-plan-template"></a><span data-ttu-id="db440-168">Mohu přidávat a používat další zdroje dat pro šablonu plánu rozpočtu?</span><span class="sxs-lookup"><span data-stu-id="db440-168">Can I add and use additional data sources to a budget plan template?</span></span>

<span data-ttu-id="db440-169">Ano. Chcete-li přidat další entity do stejného nebo jiných listů šablony aplikace Excel, můžete použít nabídku **Návrh**.</span><span class="sxs-lookup"><span data-stu-id="db440-169">Yes, you can use the **Design** menu to add additional entities to the same or other sheets in the Excel template.</span></span> <span data-ttu-id="db440-170">Můžete například přidat zdroj dat **BudgetPlanProposedProject** a vytvořit a udržovat tak seznam navrhovaných projektů současně při práci s daty plánu rozpočtu v aplikaci Excel.</span><span class="sxs-lookup"><span data-stu-id="db440-170">For example, you can add the **BudgetPlanProposedProject** data source to create and maintain a list of proposed projects at the same time when working with budget plan data in Excel.</span></span> <span data-ttu-id="db440-171">Pamatujte, že pokud zahrnete zdroje dat s velkým objemem, může to ovlivnit výkon sešitu aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="db440-171">Note that including high-volume data sources might impact performance of the Excel workbook.</span></span> 

<span data-ttu-id="db440-172">Můžete použít možnost **Filtr** v **datovém konektoru**, abyste přidali požadované filtry k dalším zdrojům dat.</span><span class="sxs-lookup"><span data-stu-id="db440-172">You can use the **Filter** option in the **Data Connector** to add desired filters to additional data sources.</span></span>

### <a name="can-i-hide-the-design-option-in-the-data-connector-for-other-users"></a><span data-ttu-id="db440-173">Můžu skrýt možnost návrhu v datovém konektoru pro ostatní uživatele?</span><span class="sxs-lookup"><span data-stu-id="db440-173">Can I hide the Design option in the Data connector for other users?</span></span>

<span data-ttu-id="db440-174">Ano. Otevřete možnosti **datového konektoru** a skryjte možnost **Návrh** před jinými uživateli.</span><span class="sxs-lookup"><span data-stu-id="db440-174">Yes, open the **Data Connector** options to hide the **Design** option from other users.</span></span>

<span data-ttu-id="db440-175">[![bpt13](./media/bpt13-1024x565.png)](./media/bpt13.png)</span><span class="sxs-lookup"><span data-stu-id="db440-175">[![bpt13](./media/bpt13-1024x565.png)](./media/bpt13.png)</span></span>

<span data-ttu-id="db440-176">Rozbalte **Možnosti datového konektoru** a zrušte zaškrtávací políčko **Povolit návrh**.</span><span class="sxs-lookup"><span data-stu-id="db440-176">Expand **Data connector options** and clear the **Enable design** check box.</span></span> <span data-ttu-id="db440-177">Tato akce skryje možnost **Návrh** z **datového konektoru**.</span><span class="sxs-lookup"><span data-stu-id="db440-177">This will hide the **Design** option from the **Data connector**.</span></span>

<span data-ttu-id="db440-178">[![bpt14](./media/bpt14-1024x592.png)](./media/bpt14.png)</span><span class="sxs-lookup"><span data-stu-id="db440-178">[![bpt14](./media/bpt14-1024x592.png)](./media/bpt14.png)</span></span>

### <a name="can-i-prevent-users-from-accidently-closing-the-data-connector-while-working-with-data"></a><span data-ttu-id="db440-179">Můžu zabránit uživatelům v náhodném uzavření datového konektoru během práce s daty?</span><span class="sxs-lookup"><span data-stu-id="db440-179">Can I prevent users from accidently closing the Data connector while working with data?</span></span>

<span data-ttu-id="db440-180">Doporučujeme šablonu uzamknout, abyste zabránili uživatelům v jejím uzavření.</span><span class="sxs-lookup"><span data-stu-id="db440-180">We recommend locking the template to prevent users from closing it.</span></span> <span data-ttu-id="db440-181">Zámek zapnete kliknutím na **Datový konektor**. V pravém horním rohu se zobrazí šipka.</span><span class="sxs-lookup"><span data-stu-id="db440-181">To turn on the lock, click the **Data connector**, in the top right corner an arrow appears.</span></span> 

<span data-ttu-id="db440-182">[![bpt15](./media/bpt15-1024x285.png)](./media/bpt15.png)</span><span class="sxs-lookup"><span data-stu-id="db440-182">[![bpt15](./media/bpt15-1024x285.png)](./media/bpt15.png)</span></span> 

<span data-ttu-id="db440-183">Klikněte na šipku pro další nabídku.</span><span class="sxs-lookup"><span data-stu-id="db440-183">Click the arrow for an additional menu.</span></span> <span data-ttu-id="db440-184">Vyberte **Uzamknout**.</span><span class="sxs-lookup"><span data-stu-id="db440-184">Select **Lock**.</span></span>

### <a name="bpt16mediabpt16-1024x614pngmediabpt16png"></a><span data-ttu-id="db440-185">[![bpt16](./media/bpt16-1024x614.png)](./media/bpt16.png)</span><span class="sxs-lookup"><span data-stu-id="db440-185">[![bpt16](./media/bpt16-1024x614.png)](./media/bpt16.png)</span></span>

### <a name="can-i-use-other-excel-features-like-cell-formatting-colors-conditional-formatting-and-charts-with-my-budget-plan-templates"></a><span data-ttu-id="db440-186">Můžu použít jiné funkce aplikace Excel, jako například formátování buněk, barvy, podmíněné formátování a grafy pro moje šablony plánu rozpočtu?</span><span class="sxs-lookup"><span data-stu-id="db440-186">Can I use other Excel features, like cell formatting, colors, conditional formatting, and charts with my budget plan templates?</span></span>

<span data-ttu-id="db440-187">Ano, většina standardních funkcí aplikace Excel bude fungovat i v šablonách plánu rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="db440-187">Yes, most of the standard Excel capabilities will work in budget plan templates.</span></span> <span data-ttu-id="db440-188">Doporučujeme používat barevné kódy pro uživatele k rozlišení mezi sloupci jen pro čtení a sloupci, které lze upravit.</span><span class="sxs-lookup"><span data-stu-id="db440-188">We recommend using color-coding for users to distinguish between read-only and editable columns.</span></span> <span data-ttu-id="db440-189">Podmíněné formátování lze použít ke zvýraznění problematických oblastí rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="db440-189">Conditional formatting can be used to highlight problematic areas of the budget.</span></span> <span data-ttu-id="db440-190">Součty sloupců lze snadno získat pomocí standardních vzorců aplikace Excel nad tabulkou.</span><span class="sxs-lookup"><span data-stu-id="db440-190">Column totals can easily be presented by using standard Excel formulas above the table.</span></span>

<span data-ttu-id="db440-191">Můžete také vytvořit a použít kontingenční tabulky a grafy pro další seskupení a vizualizace dat rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="db440-191">You can also create and use pivot tables and charts for additional groupings and visualizations of budget data.</span></span> <span data-ttu-id="db440-192">Na kartě **Data** ve skupině **Připojení** klikněte na tlačítko **Aktualizovat vše** a potom klikněte na tlačítko **Vlastnosti připojení**.</span><span class="sxs-lookup"><span data-stu-id="db440-192">On the **Data** tab, in the **Connections** group, click **Refresh All**, and then click **Connection Properties**.</span></span> <span data-ttu-id="db440-193">Klikněte na kartu **Použití**. Pod možností **Aktualizovat** zvolte zaškrtávací políčko **Aktualizovat data při otevření souboru**.</span><span class="sxs-lookup"><span data-stu-id="db440-193">Click the **Usage** tab. Under **Refresh**, select the **Refresh data when opening the file** check box.</span></span> 

<span data-ttu-id="db440-194">[![bpt17](./media/bpt17-1024x614.png)](./media/bpt17.png)</span><span class="sxs-lookup"><span data-stu-id="db440-194">[![bpt17](./media/bpt17-1024x614.png)](./media/bpt17.png)</span></span>




