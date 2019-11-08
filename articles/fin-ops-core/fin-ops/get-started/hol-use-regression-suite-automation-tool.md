---
title: Použití kurzu pro nástroj Regression Suite Automation Tool
description: Toto téma ukazuje, jak používat Regression Suite Automation Tool (RSAT). Popisuje různé funkce a poskytuje příklady, které používají pokročilé skriptování.
author: kfend
manager: AnnBe
ms.date: 06/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 21761
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 9afa98156c58d10c19454430769a3d60343661dc
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550950"
---
# <a name="use-the-regression-suite-automation-tool-tutorial"></a><span data-ttu-id="b306f-104">Použití kurzu pro Regression Suite Automation Tool</span><span class="sxs-lookup"><span data-stu-id="b306f-104">Use the Regression suite automation tool tutorial</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="b306f-105">Pomocí nástrojů internetového prohlížeče můžete tuto stránku stáhnout a uložit ve formátu PDF.</span><span class="sxs-lookup"><span data-stu-id="b306f-105">Use your internet browser tools to download and save this page in pdf format.</span></span> 

<span data-ttu-id="b306f-106">Tento kurz prochází některými rozšířenými funkcemi nástroje Regression Suite Automation Tool (RSAT), zahrnuje přiřazení ukázky a popisuje strategii a klíčové body učení.</span><span class="sxs-lookup"><span data-stu-id="b306f-106">This tutorial walks through some of the advanced features of the Regression suite automation tool (RSAT), includes a demo assignment, and describes strategy and key learning points.</span></span>

## <a name="features-of-rsattask-recorder"></a><span data-ttu-id="b306f-107">Funkce nástroje RSAT/Záznamník úloh</span><span class="sxs-lookup"><span data-stu-id="b306f-107">Features of RSAT/Task recorder</span></span>

### <a name="validate-a-field-value"></a><span data-ttu-id="b306f-108">Ověření hodnoty pole</span><span class="sxs-lookup"><span data-stu-id="b306f-108">Validate a field value</span></span>

<span data-ttu-id="b306f-109">Další informace o této funkci naleznete v tématu [Vytvoření nového záznamu úkolu, který má funkci ověření](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).</span><span class="sxs-lookup"><span data-stu-id="b306f-109">For information about this feature, see the [Create a new task recording that has a Validate function](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).</span></span>

### <a name="saved-variable"></a><span data-ttu-id="b306f-110">Uložená proměnná</span><span class="sxs-lookup"><span data-stu-id="b306f-110">Saved variable</span></span>

<span data-ttu-id="b306f-111">Další informace o této funkci naleznete v tématu [Úprava existujícího záznamu úkolu pro vytvoření uložené proměnné](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).</span><span class="sxs-lookup"><span data-stu-id="b306f-111">For information about this feature, see the [Modify an existing task recording to create a saved variable](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).</span></span>

### <a name="derived-test-case"></a><span data-ttu-id="b306f-112">Odvozený testovací případ</span><span class="sxs-lookup"><span data-stu-id="b306f-112">Derived test case</span></span>

1. <span data-ttu-id="b306f-113">Spusťte Regression Suite Automation Tool (RSAT) a vyberte oba testovací případy, které jste vytvořili v [Nastavení a instalace nístroje Regression Suite Automation Tool](./hol-set-up-regression-suite-automation-tool.md).</span><span class="sxs-lookup"><span data-stu-id="b306f-113">Open Regression suite automation tool (RSAT), and select both the test cases that you created in [Set up and install Regression suite automation tool](./hol-set-up-regression-suite-automation-tool.md).</span></span>
2. <span data-ttu-id="b306f-114">Vyberte **Nový \> Odložit testovací případ**.</span><span class="sxs-lookup"><span data-stu-id="b306f-114">Select **New \> Create derived test case**.</span></span>

    ![Vytvoření příkazu odvozeného testovacího případu v nabídce Nový](./media/use_rsa_tool_01.png)

3. <span data-ttu-id="b306f-116">Zobrazí se zpráva oznamující, že pro každý vybraný testovací případ v aktuální sadě testů bude vytvořen odvozený testovací případ a že každý odvozený testovací případ bude mít svou vlastní kopii souboru parametrů aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="b306f-116">You receive a message that states that a derived test case will be created for each selected test case in the current test suite, and that each derived test case will have its own copy of the Excel parameter file.</span></span> <span data-ttu-id="b306f-117">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="b306f-117">Select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b306f-118">Spustíte-li odvozený testovací případ, použije se záznam úloh jeho nadřazeného testovacího případu a jeho vlastní kopie souboru parametrů aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="b306f-118">When you run a derived test case, it uses the task recording of its parent test case and its own copy of the Excel parameter file.</span></span> <span data-ttu-id="b306f-119">Tímto způsobem lze spustit stejný test s jinými parametry, aniž by bylo nutné udržovat více než jeden záznam úloh.</span><span class="sxs-lookup"><span data-stu-id="b306f-119">In this way, you can run the same test with different parameters, without having to maintain more than one task recording.</span></span> <span data-ttu-id="b306f-120">Odvozený testovací případ nemusí být součástí stejné sady testů jako nadřazený testovací případ.</span><span class="sxs-lookup"><span data-stu-id="b306f-120">A derived test case doesn't have to be part of the same test suite as its parent test case.</span></span>

    ![Okno se zprávou](./media/use_rsa_tool_02.png)

    <span data-ttu-id="b306f-122">Jsou vytvořeny dva další odvozené testovací případy a je pro ně zaškrtnuto políčko **Odvozený?**.</span><span class="sxs-lookup"><span data-stu-id="b306f-122">Two additional derived test cases are created, and the **Derived?** check box is selected for them.</span></span>

    ![Vytvořené odvozené testovací případy](./media/use_rsa_tool_03.png)

    <span data-ttu-id="b306f-124">Odvozený testovací případ je automaticky vytvořen v Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="b306f-124">A derived test case is automatically created in Azure DevOps.</span></span> <span data-ttu-id="b306f-125">Jedná se o podřízenou položku testovacího případu **Vytvoření nového produktu** a je označen speciálním klíčovým slovem: **RSAT:DerivedTestSteps**.</span><span class="sxs-lookup"><span data-stu-id="b306f-125">It's a child item of the **Create a new product** test case and is tagged with a special keyword: **RSAT:DerivedTestSteps**.</span></span> <span data-ttu-id="b306f-126">Tyto testovací případy se také automaticky přidají do plánu testování v Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="b306f-126">These test cases are also automatically added to the test plan in Azure DevOps.</span></span>

    ![Klíčové slovo RSAT: DerivedTestSteps](./media/use_rsa_tool_04.png)

    > [!NOTE]
    > <span data-ttu-id="b306f-128">Pokud z jakéhokoliv důvodu nejsou vytvořené odvozené testovací případy ve správném pořadí, přejděte do Azure DevOps a přeuspořádejte testovací případy v sadě testů, aby je mohl RSAT spustit ve správném pořadí.</span><span class="sxs-lookup"><span data-stu-id="b306f-128">If, for any reason, the derived test cases that are created aren't in the correct order, go to Azure DevOps, and reorder the test cases in the test suite, so that RSAT can run them in the correct order.</span></span>

4. <span data-ttu-id="b306f-129">Vyberte odvozené testovací případy a poté výběrem možnosti **Upravit** otevřete odpovídající soubory parametrů aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="b306f-129">Select the derived test cases, and then select **Edit** to open the corresponding Excel parameter files.</span></span>
5. <span data-ttu-id="b306f-130">Upravte tyto soubory parametrů aplikace Excel stejným způsobem, jakým jste upravili nadřazené soubory.</span><span class="sxs-lookup"><span data-stu-id="b306f-130">Edit these Excel parameter files in the same way that you edited the parent files.</span></span> <span data-ttu-id="b306f-131">Jinými slovy, ujistěte se, že je ID produktu nastaveno tak, aby bylo automaticky vygenerováno.</span><span class="sxs-lookup"><span data-stu-id="b306f-131">In other words, make sure that the product ID is set so that it's automatically generated.</span></span> <span data-ttu-id="b306f-132">Rovněž se ujistěte, že uložená proměnná je zkopírována do příslušných polí.</span><span class="sxs-lookup"><span data-stu-id="b306f-132">Also make sure that the saved variable is copied to the relevant fields.</span></span>
6. <span data-ttu-id="b306f-133">Na kartě **Obecné** v obou souborech parametrů aplikace Excel aktualizujte hodnotu pole **Společnost** na **USSI**, takže odvozené testovací případy se spustí proti jiné právnické osobě, než je nadřazený testovací případ.</span><span class="sxs-lookup"><span data-stu-id="b306f-133">On the **General** tab of both Excel parameter files, update the value of the **Company** field to **USSI**, so that the derived test cases will be run against a different legal entity than the parent test case.</span></span> <span data-ttu-id="b306f-134">Chcete-li testovací případy spustit proti konkrétnímu uživateli (nebo s rolí přidruženou k určitému uživateli), můžete aktualizovat hodnotu pole **Testovací uživatel**.</span><span class="sxs-lookup"><span data-stu-id="b306f-134">To run the test cases against a specific user (or the role that is associated with a specific user), you can update the value of the **Test User** field.</span></span>
7. <span data-ttu-id="b306f-135">Vyberte **Spustit** a ověřte, že je produkt vytvořen v právnické osobě USMF i v právnické osobě USSI.</span><span class="sxs-lookup"><span data-stu-id="b306f-135">Select **Run**, and validate that the product is created in both the USMF legal entity and the USSI legal entity.</span></span>

### <a name="validate-notifications"></a><span data-ttu-id="b306f-136">Ověření oznámení</span><span class="sxs-lookup"><span data-stu-id="b306f-136">Validate notifications</span></span>

<span data-ttu-id="b306f-137">Tuto funkci lze použít k ověření, zda došlo k akci.</span><span class="sxs-lookup"><span data-stu-id="b306f-137">This feature can be used to validate whether an action occurred.</span></span> <span data-ttu-id="b306f-138">Je-li například vytvořena, odhadnuta a následně zahájena výrobní zakázka, aplikace zobrazí zprávu „Výroba - Zahájení“ a upozorní vás, že výrobní zakázka byla zahájena.</span><span class="sxs-lookup"><span data-stu-id="b306f-138">For example, when a production order is created, estimated, and then started, the app shows a "Production – Start" message to notify you that the production order has been started.</span></span>

![Oznámení Výroba - Zahájení](./media/use_rsa_tool_05.png)

<span data-ttu-id="b306f-140">Tuto zprávu můžete ověřit prostřednictvím RSAT zadáním textu zprávy na kartě **Ověření zprávy** souboru parametrů aplikace Excel pro příslušný záznam.</span><span class="sxs-lookup"><span data-stu-id="b306f-140">You can validate this message through RSAT by entering the message text on the **MessageValidation** tab of the Excel parameter file for the appropriate recording.</span></span>

![Karta Ověření zprávy](./media/use_rsa_tool_06.png)

<span data-ttu-id="b306f-142">Po spuštění testovacího případu se zpráva v souboru parametrů aplikace Excel porovná se zprávou zobrazenou.</span><span class="sxs-lookup"><span data-stu-id="b306f-142">After the test case is run, the message in the Excel parameter file is compared to the message that is shown.</span></span> <span data-ttu-id="b306f-143">Pokud se zprávy neshodují, testovací případ se nezdaří.</span><span class="sxs-lookup"><span data-stu-id="b306f-143">If the messages don't match, the test case will fail.</span></span>

> [!NOTE]
> <span data-ttu-id="b306f-144">Na kartě **Ověření zprávy** v souboru parametrů aplikace Excel můžete zadat více než jednu zprávu.</span><span class="sxs-lookup"><span data-stu-id="b306f-144">You can enter more than one message on the **MessageValidation** tab in the Excel parameter file.</span></span> <span data-ttu-id="b306f-145">Zprávy mohou být také chybové nebo varovné namísto informačních zpráv.</span><span class="sxs-lookup"><span data-stu-id="b306f-145">The messages also can be error or warning messages instead of informational messages.</span></span>

### <a name="validate-values-by-using-operators"></a><span data-ttu-id="b306f-146">Ověření hodnot pomocí operátorů</span><span class="sxs-lookup"><span data-stu-id="b306f-146">Validate values by using operators</span></span>

<span data-ttu-id="b306f-147">V předchozích verzích RSAT bylo možné ověřit hodnoty pouze v případě, že se kontrolní hodnota rovnala očekávané hodnotě.</span><span class="sxs-lookup"><span data-stu-id="b306f-147">In previous versions of RSAT, you could validate values only if a control value equaled an expected value.</span></span> <span data-ttu-id="b306f-148">Nová funkce umožňuje ověřit, že proměnná není rovna, je menší než nebo je větší než zadaná hodnota.</span><span class="sxs-lookup"><span data-stu-id="b306f-148">The new feature lets you validate that a variable isn't equal to, is less than, or is more than a specified value.</span></span>

- <span data-ttu-id="b306f-149">Chcete-li použít tuto funkci, otevřete soubor **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** v instalační složce sady RSAT (například **C:\\Program Files (x86)\\Regression Suite Automation Tool**) a změňte hodnotu v následujícím prvku z **false** na **true**.</span><span class="sxs-lookup"><span data-stu-id="b306f-149">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value in the following element from **false** to **true**.</span></span>

    ```
    <add key="AddOperatorFieldsToExcelValidation" value="false" />
    ```

    <span data-ttu-id="b306f-150">V souboru parametrů aplikace Excel se zobrazí nový **Operátor**.</span><span class="sxs-lookup"><span data-stu-id="b306f-150">In the Excel parameter file, a new **Operator** field appears.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b306f-151">Pokud používáte starší verzi nástrojů RSAT, musíte vygenerovat nové soubory parametrů aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="b306f-151">If you've been using an older version of RSAT, you must generate new Excel parameter files.</span></span>

    ![Pole Operátor](./media/use_rsa_tool_07.png)

<span data-ttu-id="b306f-153">V následujícím příkladu je ukázáno, jak lze pomocí této funkce ověřit, zda je množství na skladě větší než 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="b306f-153">The following example shows how you can use this feature to validate whether the on-hand inventory is more than 0 (zero).</span></span>

1. <span data-ttu-id="b306f-154">V ukázkových datech společnosti **USMF** vytvořte záznam úloh, který má následující kroky:</span><span class="sxs-lookup"><span data-stu-id="b306f-154">In the demo data in the **USMF** company, create a task recording that has the following steps:</span></span>

    1. <span data-ttu-id="b306f-155">Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="b306f-155">Go to **Product information management \> Products \> Released products**.</span></span>
    2. <span data-ttu-id="b306f-156">Použijte rychlý filtr pro hledání záznamů.</span><span class="sxs-lookup"><span data-stu-id="b306f-156">Use the Quick Filter to find records.</span></span> <span data-ttu-id="b306f-157">Například filtrujte na hodnotě **1000** pole **Číslo položky**.</span><span class="sxs-lookup"><span data-stu-id="b306f-157">For example, filter on a value of **1000** for the **Item number** field.</span></span>
    3. <span data-ttu-id="b306f-158">Vyberte **Zásoby na skladě**.</span><span class="sxs-lookup"><span data-stu-id="b306f-158">Select **On-hand inventory**.</span></span>
    4. <span data-ttu-id="b306f-159">Použijte rychlý filtr pro hledání záznamů.</span><span class="sxs-lookup"><span data-stu-id="b306f-159">Use the Quick Filter to find records.</span></span> <span data-ttu-id="b306f-160">Můžete například filtrovat na hodnotě **1** pro pole **Pracoviště**.</span><span class="sxs-lookup"><span data-stu-id="b306f-160">For example, filter on a value of **1** for the **Site** field.</span></span>
    5. <span data-ttu-id="b306f-161">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="b306f-161">In the list, mark the selected row.</span></span>
    6. <span data-ttu-id="b306f-162">Ověřte, zda hodnota pole **Celkem k dispozici** je **411.0000000000000000**.</span><span class="sxs-lookup"><span data-stu-id="b306f-162">Validate that the value of the **Total available** field is **411.0000000000000000**.</span></span>

2. <span data-ttu-id="b306f-163">Uložte záznam úloh do knihovny BPM v LCS a synchronizujte ho do Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="b306f-163">Save the task recording to the BPM library in LCS, and sync it to Azure DevOps.</span></span>
3. <span data-ttu-id="b306f-164">Přidejte testovací případ do testovacího plánu a načtěte testovací případ do RSAT.</span><span class="sxs-lookup"><span data-stu-id="b306f-164">Add the test case to the test plan, and load the test case into RSAT.</span></span>
4. <span data-ttu-id="b306f-165">Otevřete soubor parametrů aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="b306f-165">Open the Excel parameter file.</span></span> <span data-ttu-id="b306f-166">Na kartě **InventOnhandItem** se zobrazí část **Ověřit InventOnhandItem**, která obsahuje pole **Operátor**.</span><span class="sxs-lookup"><span data-stu-id="b306f-166">On the **InventOnhandItem** tab, you will see a **Validate InventOnhandItem** section that includes an **Operator** field.</span></span>

    ![Pole Operátor](./media/use_rsa_tool_08.png)

5. <span data-ttu-id="b306f-168">Chcete-li ověřit, zda bude množství na skladě vždy větší než 0, změňte hodnotu pole **Hodnota** z **411** na **0** a hodnotu pole **Operátor** od znaménka rovná se (**=**). na znaménko větší než (**\>**).</span><span class="sxs-lookup"><span data-stu-id="b306f-168">To validate whether the inventory on-hand will always be more than 0, change the value of the **Value** field from **411** to **0** and the value of the **Operator** field from an equal sign (**=**) to a greater than sign (**\>**).</span></span>

    ![Hodnoty polí Hodnota a Operátor byly změněny.](./media/use_rsa_tool_09.png)

6. <span data-ttu-id="b306f-170">Uložte a zavřete soubor parametrů aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="b306f-170">Save and close the Excel parameter file.</span></span>
7. <span data-ttu-id="b306f-171">Vyberte **Odeslat** pro uložení provedených změn souboru parametrů aplikace Excel do Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="b306f-171">Select **Upload** to save the changes that you made to the Excel parameter file to Azure DevOps.</span></span>

<span data-ttu-id="b306f-172">Nyní, pokud je hodnota pole **Celkem k dispozici** pro určitou položku ve skladu větší než 0 (nula), testy budou úspěšné, bez ohledu na skutečnou hodnotu zásob na skladě.</span><span class="sxs-lookup"><span data-stu-id="b306f-172">Now, if the value of the **Total Available** field for the specified item in inventory is more than 0 (zero), tests will pass, regardless of the actual on-hand inventory value.</span></span>

### <a name="generator-logs"></a><span data-ttu-id="b306f-173">Protokoly generátoru</span><span class="sxs-lookup"><span data-stu-id="b306f-173">Generator logs</span></span>

<span data-ttu-id="b306f-174">Tato funkce vytvoří složku obsahující protokoly testovacích případů, které byly spuštěny.</span><span class="sxs-lookup"><span data-stu-id="b306f-174">This feature creates a folder that contains the logs of the test cases that have been run.</span></span>

- <span data-ttu-id="b306f-175">Chcete-li použít tuto funkci, otevřete soubor **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** v instalační složce sady RSAT (například **C:\\Program Files (x86)\\Regression Suite Automation Tool**) a změňte hodnotu v následujícím prvku z **false** na **true**.</span><span class="sxs-lookup"><span data-stu-id="b306f-175">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value in the following element from **false** to **true**.</span></span>

    ```
    <add key="LogGeneration" value="false" />
    ```

<span data-ttu-id="b306f-176">Po spuštění testovacích případů můžete vyhledat soubory protokolů ve složce **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.</span><span class="sxs-lookup"><span data-stu-id="b306f-176">After the test cases are run, you can find the log files under **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.</span></span>

![Složka GeneratorLogs](./media/use_rsa_tool_10.png)

> [!NOTE]
> <span data-ttu-id="b306f-178">Pokud existovaly testovací případy před změnou hodnoty v souboru. config, nebudou protokoly generovány pro tyto testovací případy, dokud nevytvoříte nové soubory spuštění testu.</span><span class="sxs-lookup"><span data-stu-id="b306f-178">If there were existing test cases before you changed the value in the .config file, logs won't be generated for those test cases until you generate new test execution files.</span></span>
> 
> ![Příkaz Generovat pouze soubory spuštění testu v nabídce Nový](./media/use_rsa_tool_11.png)

### <a name="snapshot"></a><span data-ttu-id="b306f-180">Snímek</span><span class="sxs-lookup"><span data-stu-id="b306f-180">Snapshot</span></span>

<span data-ttu-id="b306f-181">Tato funkce pořídí snímky obrazovek kroků, které byly provedeny při záznamu úloh.</span><span class="sxs-lookup"><span data-stu-id="b306f-181">This feature takes screenshots of the steps that were performed during task recording.</span></span>

- <span data-ttu-id="b306f-182">Chcete-li použít tuto funkci, otevřete soubor **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** v instalační složce sady RSAT (například **C:\\Program Files (x86)\\Regression Suite Automation Tool**) a změňte hodnotu následujícího prvku z **false** na **true**.</span><span class="sxs-lookup"><span data-stu-id="b306f-182">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value of the following element from **false** to **true**.</span></span>

    ```
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

<span data-ttu-id="b306f-183">Pro každý spuštěný testovací případ se vytvoří samostatná složka pod Under **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**.</span><span class="sxs-lookup"><span data-stu-id="b306f-183">Under **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, a separate folder is created for each test case that is run.</span></span>

![Složka snímku pro testovací případ](./media/use_rsa_tool_12.png)

<span data-ttu-id="b306f-185">V každé z těchto složek můžete vyhledat snímky kroků, které byly provedeny při spuštění testovacích případů.</span><span class="sxs-lookup"><span data-stu-id="b306f-185">In each of these folders, you can find snapshots of the steps that were performed while the test cases were run.</span></span>

![Soubory snímků](./media/use_rsa_tool_13.png)

## <a name="assignment"></a><span data-ttu-id="b306f-187">Přiřazení</span><span class="sxs-lookup"><span data-stu-id="b306f-187">Assignment</span></span>

### <a name="scenario"></a><span data-ttu-id="b306f-188">Scénář</span><span class="sxs-lookup"><span data-stu-id="b306f-188">Scenario</span></span>

1. <span data-ttu-id="b306f-189">Návrhář produktu vytvoří nový uvolněný produkt.</span><span class="sxs-lookup"><span data-stu-id="b306f-189">The product designer creates a new released product.</span></span>
2. <span data-ttu-id="b306f-190">Vedoucí výroby iniciuje výrobní zakázku za účelem zvýšení zásob na dva kusy.</span><span class="sxs-lookup"><span data-stu-id="b306f-190">The production manager initiates a production order to bring the stock level to two pieces.</span></span>
3. <span data-ttu-id="b306f-191">Výroba zahájí a ukončí výrobní zakázku a ověří, že množství na skladě jsou dva kusy.</span><span class="sxs-lookup"><span data-stu-id="b306f-191">Manufacturing starts and ends the production order, and verifies that the on-hand quantity is two pieces.</span></span>
4. <span data-ttu-id="b306f-192">Prodejní tým obdrží objednávku na čtyři kusy nového produktu.</span><span class="sxs-lookup"><span data-stu-id="b306f-192">The sales team receives an order for four pieces of the new product.</span></span> <span data-ttu-id="b306f-193">Prodejní tým proto aktualizuje čisté požadavky prostřednictvím dynamického plánu.</span><span class="sxs-lookup"><span data-stu-id="b306f-193">Therefore, the sales team updates the net requirements via the dynamic plan.</span></span> <span data-ttu-id="b306f-194">Vzhledem k tomu, že žádná další kapacita není k dispozici, je výchozí zásada objednávky nastavena na hodnotu „koupit místo vyrobit“.</span><span class="sxs-lookup"><span data-stu-id="b306f-194">Because no additional capacity is available, the default order policy is set to "buy instead of make."</span></span> <span data-ttu-id="b306f-195">Proto se vytvoří plánovaná nákupní objednávka.</span><span class="sxs-lookup"><span data-stu-id="b306f-195">Therefore, a planned purchase order is created.</span></span>
5. <span data-ttu-id="b306f-196">Kupující přidá dodavatele, podepíše plánovanou nákupní objednávku a poté potvrdí nákupní objednávku.</span><span class="sxs-lookup"><span data-stu-id="b306f-196">The buyer adds a vendor, firms the planned purchase order, and then confirms the purchase order.</span></span>
6. <span data-ttu-id="b306f-197">Po doručení zakoupeného zboží do skladu vyhledá operátor skladu související nákupní objednávku a přijme zboží.</span><span class="sxs-lookup"><span data-stu-id="b306f-197">When the goods that were purchased arrive at the store, the store operator searches the related purchase order and receives the goods.</span></span> <span data-ttu-id="b306f-198">Vzhledem k tomu, že objednávka je nyní dokončena, lze zboží vydat a zabalit proti prodejní objednávce.</span><span class="sxs-lookup"><span data-stu-id="b306f-198">Because the order is now completed, goods can be picked and packed against the sales order.</span></span>
7. <span data-ttu-id="b306f-199">Finance zaúčtují nákupní fakturu a prodejní fakturu.</span><span class="sxs-lookup"><span data-stu-id="b306f-199">Finance posts the purchase invoice and sales invoice.</span></span>

<span data-ttu-id="b306f-200">Následující ilustrace znázorňuje tok pro tento scénář.</span><span class="sxs-lookup"><span data-stu-id="b306f-200">The following illustration shows the flow for this scenario.</span></span>

![Tok ukázkového scénáře](./media/use_rsa_tool_14.png)

<span data-ttu-id="b306f-202">Následující ilustrace znázorňuje obchodní procesy pro tento scénář v RSAT.</span><span class="sxs-lookup"><span data-stu-id="b306f-202">The following illustration shows the business processes for this scenario in RSAT.</span></span>

![Obchodní procesy pro ukázkový scénář](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a><span data-ttu-id="b306f-204">Strategie – klíčové učení</span><span class="sxs-lookup"><span data-stu-id="b306f-204">Strategy – Key learning</span></span>

### <a name="data"></a><span data-ttu-id="b306f-205">Údaje</span><span class="sxs-lookup"><span data-stu-id="b306f-205">Data</span></span>

- <span data-ttu-id="b306f-206">Ujistěte se, že máte reprezentativní datové objemy (kopie dat produkční/zlaté konfigurace a přenesená data).</span><span class="sxs-lookup"><span data-stu-id="b306f-206">Make sure that you have representative data volumes (a copy of production/golden configuration data plus migrated data).</span></span>
- <span data-ttu-id="b306f-207">Když generujete nová data pomocí záznamníku úloh, vytvořte názvy testů, které nekolidují s existujícími názvy (například použijte předponu **RSATxxx**).</span><span class="sxs-lookup"><span data-stu-id="b306f-207">When you generate new data via Task recorder, create test names that won't conflict with existing names (for example, use a prefix such as **RSATxxx**).</span></span>
- <span data-ttu-id="b306f-208">Použijte obnovení k určitému bodu v čase Azure- pro opětovné spuštění testů v prostředích, které nejsou v úrovni 1.</span><span class="sxs-lookup"><span data-stu-id="b306f-208">Use Azure Point-In-Time restore to rerun tests in non-Tier 1 environments.</span></span>
- <span data-ttu-id="b306f-209">Ačkoli můžete použít funkce Excelu **RANDOM** a **NOW** k vygenerování jedinečné kombinace, úsilí je poměrně vysoké.</span><span class="sxs-lookup"><span data-stu-id="b306f-209">Although you can use the **RANDOM** and **NOW** Excel functions to generate a unique combination, the effort is considerably high.</span></span> <span data-ttu-id="b306f-210">Následuje příklad.</span><span class="sxs-lookup"><span data-stu-id="b306f-210">Here is an example.</span></span>

    ```
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a><span data-ttu-id="b306f-211">Záznamník úkolů</span><span class="sxs-lookup"><span data-stu-id="b306f-211">Task recorder</span></span>

- <span data-ttu-id="b306f-212">Definujte scénáře před zahájením záznamu.</span><span class="sxs-lookup"><span data-stu-id="b306f-212">Define scenarios before you start recording.</span></span> <span data-ttu-id="b306f-213">Dobře spravovaný projekt má předdefinované scénáře testování.</span><span class="sxs-lookup"><span data-stu-id="b306f-213">A well-managed project has predefined test scenarios.</span></span> <span data-ttu-id="b306f-214">Chcete-li vytvořit testovací případ, zvažte, jak předvídatelné výsledky těchto testů jsou.</span><span class="sxs-lookup"><span data-stu-id="b306f-214">To build a test case, consider how predictable the outcome of those test scenarios is.</span></span>
- <span data-ttu-id="b306f-215">Záznamy rozdělte, pokud je provedete různými rolemi, nebo pokud se před dalším krokem vyskytl čas čekání nebo externí událost.</span><span class="sxs-lookup"><span data-stu-id="b306f-215">Split recordings if they are performed by different roles, or if there is waiting time or an external event before the next step.</span></span>
- <span data-ttu-id="b306f-216">Vyhněte se výběru hodnot v seznamech.</span><span class="sxs-lookup"><span data-stu-id="b306f-216">Avoid selecting values in lists.</span></span> <span data-ttu-id="b306f-217">Místo toho použijte textové formáty, jako například **FIFO**, **AudioRM** a **SiteWH**.</span><span class="sxs-lookup"><span data-stu-id="b306f-217">Instead, use text formats, such as **FIFO**, **AudioRM**, and **SiteWH**.</span></span> <span data-ttu-id="b306f-218">Vyberete-li možnost v seznamu, bude zaznamenána pozice hodnoty v seznamu, nikoli hodnota samotná.</span><span class="sxs-lookup"><span data-stu-id="b306f-218">When you select in a list, the position of the value in the list is recorded, not the value itself.</span></span> <span data-ttu-id="b306f-219">Pokud jsou do seznamu přidány položky, bude možné změnit pozici hodnoty.</span><span class="sxs-lookup"><span data-stu-id="b306f-219">If items are added to that list, the position of the value can change.</span></span> <span data-ttu-id="b306f-220">Proto bude nahrávka používat jiný parametr a může to mít vliv na zbytek scénáře.</span><span class="sxs-lookup"><span data-stu-id="b306f-220">Therefore, your recording will use a different parameter, and the rest of the scenario might be affected.</span></span>
- <span data-ttu-id="b306f-221">Zamyslete se nad chováním více uživatelů.</span><span class="sxs-lookup"><span data-stu-id="b306f-221">Think about multi-user behavior.</span></span> <span data-ttu-id="b306f-222">Nepředpokládejte například, že nově vytvořená prodejní objednávka bude vždy vybrána automaticky.</span><span class="sxs-lookup"><span data-stu-id="b306f-222">For example, don't assume that your newly created sales order will always be automatically selected.</span></span> <span data-ttu-id="b306f-223">Místo toho vždy použijte ke zjištění správné objednávky filtr.</span><span class="sxs-lookup"><span data-stu-id="b306f-223">Instead, always use the filter to find the correct order.</span></span>
- <span data-ttu-id="b306f-224">Použijte funkci kopírování v záznamníku úloh pro uložení názvu nově vytvořeného produktu, aby jej bylo možné použít ve zřetězených testovacích případech.</span><span class="sxs-lookup"><span data-stu-id="b306f-224">Use the Copy function in Task recorder to save the name of a newly created product so it can be used in chained test cases.</span></span>
- <span data-ttu-id="b306f-225">Použijte funkci ověření v záznamníku úloh pro nastavení kontrolních bodů, které ověřují, zda byly provedeny správné kroky.</span><span class="sxs-lookup"><span data-stu-id="b306f-225">Use the Validate function in Task recorder to set checkpoints that verify that steps have been run correctly.</span></span>

### <a name="rsat"></a><span data-ttu-id="b306f-226">RSAT</span><span class="sxs-lookup"><span data-stu-id="b306f-226">RSAT</span></span>

- <span data-ttu-id="b306f-227">Chcete-li spustit test v jiné společnosti, můžete změnit společnost na kartě **Obecné** v souboru parametrů aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="b306f-227">To run the test in another company, you can change the company on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="b306f-228">Zkontrolujte, zda jsou v nově vybrané společnosti k dispozici nastavení a data.</span><span class="sxs-lookup"><span data-stu-id="b306f-228">Make sure that settings and data are available in the newly selected company.</span></span>
- <span data-ttu-id="b306f-229">Testovacího uživatele můžete změnit na kartě **Obecné** v souboru parametrů aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="b306f-229">You can change the test user on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="b306f-230">Zadejte ID e-mailu uživatele, který spustí testovací případ.</span><span class="sxs-lookup"><span data-stu-id="b306f-230">Specify the email ID of the user who will run the test case.</span></span> <span data-ttu-id="b306f-231">Tímto způsobem lze testovací případ spustit pomocí oprávnění zabezpečení zadaného uživatele.</span><span class="sxs-lookup"><span data-stu-id="b306f-231">In this way, the test case can be run by using the security permissions of the specified user.</span></span>
- <span data-ttu-id="b306f-232">Chcete-li počkat před zahájením testu, můžete na kartě **Obecné** v souboru parametrů aplikace Excel definovat pauzu.</span><span class="sxs-lookup"><span data-stu-id="b306f-232">To wait before the test is started, you can define a pause on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="b306f-233">Toto pozastavení lze použít v dávkové úloze (například v případě, že je nutné spustit workflow ještě před provedením dalšího kroku).</span><span class="sxs-lookup"><span data-stu-id="b306f-233">This pause can be used in a batch job (for example, if a workflow must be run before the next step can be performed.)</span></span>

## <a name="advanced-scripting"></a><span data-ttu-id="b306f-234">Pokročilé skriptování</span><span class="sxs-lookup"><span data-stu-id="b306f-234">Advanced scripting</span></span>

### <a name="command-line"></a><span data-ttu-id="b306f-235">Příkazový řádek</span><span class="sxs-lookup"><span data-stu-id="b306f-235">Command line</span></span>

<span data-ttu-id="b306f-236">RSAT lze volat z okna **příkazového řádku**.</span><span class="sxs-lookup"><span data-stu-id="b306f-236">RSAT can be called from a **Command Prompt** window.</span></span>

> [!NOTE]
> <span data-ttu-id="b306f-237">Ověřte, zda je proměnná prostředí **TestRoot** nastavena na cestu instalace RSAT.</span><span class="sxs-lookup"><span data-stu-id="b306f-237">Verify that the **TestRoot** environment variable is set to the RSAT installation path.</span></span> <span data-ttu-id="b306f-238">(V Microsoft Windows otevřete **Ovládací panel**, vyberte **Systém a zabezpečení \> Systém \> Pokročilá nastavení systému** a pak zvolte **Proměnné prostředí**.)</span><span class="sxs-lookup"><span data-stu-id="b306f-238">(In Microsoft Windows, open **Control Panel**, select **System and Security \> System \> Advanced system settings**, and then select **Environment Variables**.)</span></span>

1. <span data-ttu-id="b306f-239">Otevřete okno **příkazového řádku** jako správce.</span><span class="sxs-lookup"><span data-stu-id="b306f-239">Open a **Command Prompt** window as an admin.</span></span>
2. <span data-ttu-id="b306f-240">Spusťte nástroj z instalačního adresáře.</span><span class="sxs-lookup"><span data-stu-id="b306f-240">Run the tool from the installation directory.</span></span>

    ```
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. <span data-ttu-id="b306f-241">Vyvolejte seznam všech příkazů.</span><span class="sxs-lookup"><span data-stu-id="b306f-241">List all commands.</span></span>

    ```
    C:\Program Files (x86)\Regression Suite Automation Tool>Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe help

    Usage:
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe command
        or
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe /settings "C:\Path to\file.settings" command

    Available commands:
        list
        listtestsuite suite_name
        download test_case_id output_dir
        generate test_case_id output_dir
        generatederived parent_test_case_id test_plan_id test_suite_id
        generatetestonly test_case_id output_dir
        edit excel_file
        playback excel_file
        playbackmany excel_file1 [excel_file2 [.. excel_fileN]]
        playbackbyid test_case_id1 [test_case_id2 [.. test_case_idN]]
        playbacksuite suite_name
        clear
        help
        about
        quit
    ```

### <a name="windows-powershell-examples"></a><span data-ttu-id="b306f-242">Příklad Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="b306f-242">Windows PowerShell examples</span></span>

#### <a name="run-a-test-case-in-a-loop"></a><span data-ttu-id="b306f-243">Spuštění testovacího případu ve smyčce</span><span class="sxs-lookup"><span data-stu-id="b306f-243">Run a test case in a loop</span></span>

<span data-ttu-id="b306f-244">Máte testovací skript, který vytvoří nového odběratele.</span><span class="sxs-lookup"><span data-stu-id="b306f-244">You have a test script that creates a new customer.</span></span> <span data-ttu-id="b306f-245">Pomocí skriptování lze tento testovací případ spustit ve smyčce tak, že před spuštěním každé iterace náhodně použijete následující data:</span><span class="sxs-lookup"><span data-stu-id="b306f-245">Via scripting, this test case can be run in a loop by randomizing the following data before each iteration is run:</span></span>

- <span data-ttu-id="b306f-246">ID odběratele</span><span class="sxs-lookup"><span data-stu-id="b306f-246">Customer ID</span></span>
- <span data-ttu-id="b306f-247">Jméno zákazníka</span><span class="sxs-lookup"><span data-stu-id="b306f-247">Customer name</span></span>
- <span data-ttu-id="b306f-248">Adresa odběratele</span><span class="sxs-lookup"><span data-stu-id="b306f-248">Customer address</span></span>

<span data-ttu-id="b306f-249">ID zákazníka bude mít formát *ATCUS\<číslo\>*, kde \<číslo\> je hodnota mezi **000000001** a **999999999**.</span><span class="sxs-lookup"><span data-stu-id="b306f-249">The customer ID will be in the format *ATCUS\<number\>*, where \<number\> is a value between **000000001** and **999999999**.</span></span>

<span data-ttu-id="b306f-250">V následujícím příkladu je použit jeden parametr **start** pro definování prvního použitého čísla.</span><span class="sxs-lookup"><span data-stu-id="b306f-250">The following example uses one parameter, **start**, to define the first number that is used.</span></span> <span data-ttu-id="b306f-251">Aplikace používá k definování počtu odběratelů, které je nutné vytvořit, druhý parametr **nr**.</span><span class="sxs-lookup"><span data-stu-id="b306f-251">Is uses a second parameter, **nr**, to define the number of customers that must be created.</span></span> <span data-ttu-id="b306f-252">Parametry v souboru parametrů aplikace Excel jsou pro každou iteraci změněny pomocí funkce UpdateCustomer.</span><span class="sxs-lookup"><span data-stu-id="b306f-252">For each iteration, the parameters in the Excel parameter file are changed by using an UpdateCustomer function.</span></span> <span data-ttu-id="b306f-253">Poté bude příkazový řádek RSAT volán ve funkci RunTestCase.</span><span class="sxs-lookup"><span data-stu-id="b306f-253">Then the RSAT command line is called in a RunTestCase function.</span></span>

<span data-ttu-id="b306f-254">Otevřete Microsoft Windows PowerShell Integrated Scripting Environment (ISE) v režimu správy a vložte následující kód do okna s názvem **Untitled1. ps1.**</span><span class="sxs-lookup"><span data-stu-id="b306f-254">Open Microsoft Windows PowerShell Integrated Scripting Environment (ISE) in admin mode, and paste the following code into the window that is named **Untitled1.ps1**.</span></span>

```
param ( [int]$start = 1, [int]$nr = 1 )
function UpdateCustomer
{
    param ([string]$paramFilename, [string]$sheetName, [string]$CustId)
    $xl = New-Object -COM "Excel.Application"
    $xl.Visible = $false
    $wb = $xl.Workbooks.Open($paramFilename)
    $ws = $wb.Sheets.Item($sheetName)
    $ws.Cells.Item(3, 2).Value = "ATCUS" + $CustId
    $ws.Cells.Item(4, 2).Value = "Automated Test Customer " + $CustId
    $ws.Cells.Item(8, 2).Value = "Automated Test Street " + $CustId
    $wb.Save()
    $wb.Close()
    $xl.Quit()
    [System.Runtime.Interopservices.Marshal]::ReleaseComObject($xl)
}
function RunTestCase
{
    param ( [string]$filename )
    $cmd = "cd c:\Program Files (x86)\Regression Suite Automation Tool\ &&  "
    $cmd = $cmd + "Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe playback "
    $cmd = $cmd + $filename
    cmd /c $cmd
}
$excelFilename = "full path to excel file parameter file"
l$sheetName = "DirPartyQuickCreateForm"
for ($i = $start; $i -lt $start + $nr; $i++ )
{
    $CustomerId = $i.ToString("000000000")
    Write-Host "customer : " $CustomerId
    UpdateCustomer $excelFilename $sheetName $CustomerId
    RunTestCase $excelFilename
```

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a><span data-ttu-id="b306f-255">Spuštění skriptu, který závisí na datech v Microsoft Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="b306f-255">Run a script that depends on data in Microsoft Dynamics 365</span></span>

<span data-ttu-id="b306f-256">V následujícím příkladu je pomocí volání OData (Open Data Protocol) nalezen stav nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="b306f-256">The following example uses an Open Data Protocol (OData) call to find the order status of a purchase order.</span></span> <span data-ttu-id="b306f-257">Pokud není stav **fakturován**, můžete například volat testovací případ RSAT, který zaúčtuje fakturu.</span><span class="sxs-lookup"><span data-stu-id="b306f-257">If the status isn't **invoiced**, you can, for example, call an RSAT test case that posts the invoice.</span></span>

```
function Odata_Get
{
    Param ( [string] $environment, [string] $cmd )
    [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12
    $tenant = "your tenant"
    $creds = @{
        grant_type = "client_credentials"
        client_id = "your client application Id"
        client_secret = "your client secret"
        resource = $environment
    }
    $headers = $null
    $bearer = Invoke-RestMethod https://login.microsoftonline.com/$tenant/oauth2/token -Method Post -Body $creds -Headers $headers;
    $headers = @{
        Authorization = "Bearer " + $bearer.access_token
    }
    $Odata_cmd = $environment + '/data/' + $cmd
    return (Invoke-RestMethod -Uri $Odata_cmd -Method Get -Headers $headers -ContentType application/json )
}
function PurchaseOrderStatus
{
    Param ( [string] $environment, [string] $purchaseOrderNumber )
    $cmd = 'PurchaseOrderHeaders?$filter=PurchaseOrderNumber eq '
    $cmd = $cmd + "'" + $purchaseOrderNumber + "'"
    $response = Odata_Get -environment $environment -cmd $cmd
    return $response.value.PurchaseOrderStatus
}
$environment = "https://your environment"
$orderStatus = PurchaseOrderStatus -environment $environment -purchaseOrderNumber '000003'
if ($orderStatus -eq $null) {   write-host 'doesn''t exist'}
elseif ($orderStatus -ne 'invoiced') { RunTestCase "PostInvoice" }
```
