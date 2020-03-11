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
ms.openlocfilehash: 6cdaa89fb6d50ebaaaefe7f92d7224a1567d17d1
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070813"
---
# <a name="use-the-regression-suite-automation-tool-tutorial"></a><span data-ttu-id="a9f89-104">Použití kurzu pro Regression Suite Automation Tool</span><span class="sxs-lookup"><span data-stu-id="a9f89-104">Use the Regression suite automation tool tutorial</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="a9f89-105">Pomocí nástrojů internetového prohlížeče můžete tuto stránku stáhnout a uložit ve formátu PDF.</span><span class="sxs-lookup"><span data-stu-id="a9f89-105">Use your internet browser tools to download and save this page in pdf format.</span></span> 

<span data-ttu-id="a9f89-106">Tento kurz prochází některými rozšířenými funkcemi nástroje Regression Suite Automation Tool (RSAT), zahrnuje přiřazení ukázky a popisuje strategii a klíčové body učení.</span><span class="sxs-lookup"><span data-stu-id="a9f89-106">This tutorial walks through some of the advanced features of the Regression suite automation tool (RSAT), includes a demo assignment, and describes strategy and key learning points.</span></span>

## <a name="features-of-rsattask-recorder"></a><span data-ttu-id="a9f89-107">Funkce nástroje RSAT/Záznamník úloh</span><span class="sxs-lookup"><span data-stu-id="a9f89-107">Features of RSAT/Task recorder</span></span>

### <a name="validate-a-field-value"></a><span data-ttu-id="a9f89-108">Ověření hodnoty pole</span><span class="sxs-lookup"><span data-stu-id="a9f89-108">Validate a field value</span></span>

<span data-ttu-id="a9f89-109">Další informace o této funkci naleznete v tématu [Vytvoření nového záznamu úkolu, který má funkci ověření](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).</span><span class="sxs-lookup"><span data-stu-id="a9f89-109">For information about this feature, see the [Create a new task recording that has a Validate function](./hol-set-up-regression-suite-automation-tool.md#create-a-new-task-recording-that-has-a-validate-function).</span></span>

### <a name="saved-variable"></a><span data-ttu-id="a9f89-110">Uložená proměnná</span><span class="sxs-lookup"><span data-stu-id="a9f89-110">Saved variable</span></span>

<span data-ttu-id="a9f89-111">Další informace o této funkci naleznete v tématu [Úprava existujícího záznamu úkolu pro vytvoření uložené proměnné](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).</span><span class="sxs-lookup"><span data-stu-id="a9f89-111">For information about this feature, see the [Modify an existing task recording to create a saved variable](./hol-set-up-regression-suite-automation-tool.md#modify-an-existing-task-recording-to-create-a-saved-variable).</span></span>

### <a name="derived-test-case"></a><span data-ttu-id="a9f89-112">Odvozený testovací případ</span><span class="sxs-lookup"><span data-stu-id="a9f89-112">Derived test case</span></span>

1. <span data-ttu-id="a9f89-113">Spusťte Regression Suite Automation Tool (RSAT) a vyberte oba testovací případy, které jste vytvořili v [kurzu Nastavení a instalace nástroje Regression Suite Automation Tool](./hol-set-up-regression-suite-automation-tool.md).</span><span class="sxs-lookup"><span data-stu-id="a9f89-113">Open Regression suite automation tool (RSAT), and select both the test cases that you created in [Set up and install Regression suite automation tool tutorial](./hol-set-up-regression-suite-automation-tool.md).</span></span>
2. <span data-ttu-id="a9f89-114">Vyberte **Nový \> Odložit testovací případ**.</span><span class="sxs-lookup"><span data-stu-id="a9f89-114">Select **New \> Create derived test case**.</span></span>

    ![Vytvoření příkazu odvozeného testovacího případu v nabídce Nový](./media/use_rsa_tool_01.png)

3. <span data-ttu-id="a9f89-116">Zobrazí se zpráva oznamující, že pro každý vybraný testovací případ v aktuální sadě testů bude vytvořen odvozený testovací případ a že každý odvozený testovací případ bude mít svou vlastní kopii souboru parametrů aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="a9f89-116">You receive a message that states that a derived test case will be created for each selected test case in the current test suite, and that each derived test case will have its own copy of the Excel parameter file.</span></span> <span data-ttu-id="a9f89-117">Vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="a9f89-117">Select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a9f89-118">Spustíte-li odvozený testovací případ, použije se záznam úloh jeho nadřazeného testovacího případu a jeho vlastní kopie souboru parametrů aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="a9f89-118">When you run a derived test case, it uses the task recording of its parent test case and its own copy of the Excel parameter file.</span></span> <span data-ttu-id="a9f89-119">Tímto způsobem lze spustit stejný test s jinými parametry, aniž by bylo nutné udržovat více než jeden záznam úloh.</span><span class="sxs-lookup"><span data-stu-id="a9f89-119">In this way, you can run the same test with different parameters, without having to maintain more than one task recording.</span></span> <span data-ttu-id="a9f89-120">Odvozený testovací případ nemusí být součástí stejné sady testů jako nadřazený testovací případ.</span><span class="sxs-lookup"><span data-stu-id="a9f89-120">A derived test case doesn't have to be part of the same test suite as its parent test case.</span></span>

    ![Okno se zprávou](./media/use_rsa_tool_02.png)

    <span data-ttu-id="a9f89-122">Jsou vytvořeny dva další odvozené testovací případy a je pro ně zaškrtnuto políčko **Odvozený?**.</span><span class="sxs-lookup"><span data-stu-id="a9f89-122">Two additional derived test cases are created, and the **Derived?** check box is selected for them.</span></span>

    ![Vytvořené odvozené testovací případy](./media/use_rsa_tool_03.png)

    <span data-ttu-id="a9f89-124">Odvozený testovací případ je automaticky vytvořen v Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="a9f89-124">A derived test case is automatically created in Azure DevOps.</span></span> <span data-ttu-id="a9f89-125">Jedná se o podřízenou položku testovacího případu **Vytvoření nového produktu** a je označen speciálním klíčovým slovem: **RSAT:DerivedTestSteps**.</span><span class="sxs-lookup"><span data-stu-id="a9f89-125">It's a child item of the **Create a new product** test case and is tagged with a special keyword: **RSAT:DerivedTestSteps**.</span></span> <span data-ttu-id="a9f89-126">Tyto testovací případy se také automaticky přidají do plánu testování v Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="a9f89-126">These test cases are also automatically added to the test plan in Azure DevOps.</span></span>

    ![Klíčové slovo RSAT: DerivedTestSteps](./media/use_rsa_tool_04.png)

    > [!NOTE]
    > <span data-ttu-id="a9f89-128">Pokud z jakéhokoliv důvodu nejsou vytvořené odvozené testovací případy ve správném pořadí, přejděte do Azure DevOps a přeuspořádejte testovací případy v sadě testů, aby je mohl RSAT spustit ve správném pořadí.</span><span class="sxs-lookup"><span data-stu-id="a9f89-128">If, for any reason, the derived test cases that are created aren't in the correct order, go to Azure DevOps, and reorder the test cases in the test suite, so that RSAT can run them in the correct order.</span></span>

4. <span data-ttu-id="a9f89-129">Vyberte odvozené testovací případy a poté výběrem možnosti **Upravit** otevřete odpovídající soubory parametrů aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="a9f89-129">Select the derived test cases, and then select **Edit** to open the corresponding Excel parameter files.</span></span>
5. <span data-ttu-id="a9f89-130">Upravte tyto soubory parametrů aplikace Excel stejným způsobem, jakým jste upravili nadřazené soubory.</span><span class="sxs-lookup"><span data-stu-id="a9f89-130">Edit these Excel parameter files in the same way that you edited the parent files.</span></span> <span data-ttu-id="a9f89-131">Jinými slovy, ujistěte se, že je ID produktu nastaveno tak, aby bylo automaticky vygenerováno.</span><span class="sxs-lookup"><span data-stu-id="a9f89-131">In other words, make sure that the product ID is set so that it's automatically generated.</span></span> <span data-ttu-id="a9f89-132">Rovněž se ujistěte, že uložená proměnná je zkopírována do příslušných polí.</span><span class="sxs-lookup"><span data-stu-id="a9f89-132">Also make sure that the saved variable is copied to the relevant fields.</span></span>
6. <span data-ttu-id="a9f89-133">Na kartě **Obecné** v obou souborech parametrů aplikace Excel aktualizujte hodnotu pole **Společnost** na **USSI**, takže odvozené testovací případy se spustí proti jiné právnické osobě, než je nadřazený testovací případ.</span><span class="sxs-lookup"><span data-stu-id="a9f89-133">On the **General** tab of both Excel parameter files, update the value of the **Company** field to **USSI**, so that the derived test cases will be run against a different legal entity than the parent test case.</span></span> <span data-ttu-id="a9f89-134">Chcete-li testovací případy spustit proti konkrétnímu uživateli (nebo s rolí přidruženou k určitému uživateli), můžete aktualizovat hodnotu pole **Testovací uživatel**.</span><span class="sxs-lookup"><span data-stu-id="a9f89-134">To run the test cases against a specific user (or the role that is associated with a specific user), you can update the value of the **Test User** field.</span></span>
7. <span data-ttu-id="a9f89-135">Vyberte **Spustit** a ověřte, že je produkt vytvořen v právnické osobě USMF i v právnické osobě USSI.</span><span class="sxs-lookup"><span data-stu-id="a9f89-135">Select **Run**, and validate that the product is created in both the USMF legal entity and the USSI legal entity.</span></span>

### <a name="validate-notifications"></a><span data-ttu-id="a9f89-136">Ověření oznámení</span><span class="sxs-lookup"><span data-stu-id="a9f89-136">Validate notifications</span></span>

<span data-ttu-id="a9f89-137">Tuto funkci lze použít k ověření, zda došlo k akci.</span><span class="sxs-lookup"><span data-stu-id="a9f89-137">This feature can be used to validate whether an action occurred.</span></span> <span data-ttu-id="a9f89-138">Je-li například vytvořena, odhadnuta a následně zahájena výrobní zakázka, aplikace zobrazí zprávu „Výroba - Zahájení“ a upozorní vás, že výrobní zakázka byla zahájena.</span><span class="sxs-lookup"><span data-stu-id="a9f89-138">For example, when a production order is created, estimated, and then started, the app shows a "Production – Start" message to notify you that the production order has been started.</span></span>

![Oznámení Výroba - Zahájení](./media/use_rsa_tool_05.png)

<span data-ttu-id="a9f89-140">Tuto zprávu můžete ověřit prostřednictvím RSAT zadáním textu zprávy na kartě **Ověření zprávy** souboru parametrů aplikace Excel pro příslušný záznam.</span><span class="sxs-lookup"><span data-stu-id="a9f89-140">You can validate this message through RSAT by entering the message text on the **MessageValidation** tab of the Excel parameter file for the appropriate recording.</span></span>

![Karta Ověření zprávy](./media/use_rsa_tool_06.png)

<span data-ttu-id="a9f89-142">Po spuštění testovacího případu se zpráva v souboru parametrů aplikace Excel porovná se zprávou zobrazenou.</span><span class="sxs-lookup"><span data-stu-id="a9f89-142">After the test case is run, the message in the Excel parameter file is compared to the message that is shown.</span></span> <span data-ttu-id="a9f89-143">Pokud se zprávy neshodují, testovací případ se nezdaří.</span><span class="sxs-lookup"><span data-stu-id="a9f89-143">If the messages don't match, the test case will fail.</span></span>

> [!NOTE]
> <span data-ttu-id="a9f89-144">Na kartě **Ověření zprávy** v souboru parametrů aplikace Excel můžete zadat více než jednu zprávu.</span><span class="sxs-lookup"><span data-stu-id="a9f89-144">You can enter more than one message on the **MessageValidation** tab in the Excel parameter file.</span></span> <span data-ttu-id="a9f89-145">Zprávy mohou být také chybové nebo varovné namísto informačních zpráv.</span><span class="sxs-lookup"><span data-stu-id="a9f89-145">The messages also can be error or warning messages instead of informational messages.</span></span>

### <a name="validate-values-by-using-operators"></a><span data-ttu-id="a9f89-146">Ověření hodnot pomocí operátorů</span><span class="sxs-lookup"><span data-stu-id="a9f89-146">Validate values by using operators</span></span>

<span data-ttu-id="a9f89-147">V předchozích verzích RSAT bylo možné ověřit hodnoty pouze v případě, že se kontrolní hodnota rovnala očekávané hodnotě.</span><span class="sxs-lookup"><span data-stu-id="a9f89-147">In previous versions of RSAT, you could validate values only if a control value equaled an expected value.</span></span> <span data-ttu-id="a9f89-148">Nová funkce umožňuje ověřit, že proměnná není rovna, je menší než nebo je větší než zadaná hodnota.</span><span class="sxs-lookup"><span data-stu-id="a9f89-148">The new feature lets you validate that a variable isn't equal to, is less than, or is more than a specified value.</span></span>

- <span data-ttu-id="a9f89-149">Chcete-li použít tuto funkci, otevřete soubor **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** v instalační složce sady RSAT (například **C:\\Program Files (x86)\\Regression Suite Automation Tool**) a změňte hodnotu v následujícím prvku z **false** na **true**.</span><span class="sxs-lookup"><span data-stu-id="a9f89-149">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value in the following element from **false** to **true**.</span></span>

    ```xml
    <add key="AddOperatorFieldsToExcelValidation" value="false" />
    ```

    <span data-ttu-id="a9f89-150">V souboru parametrů aplikace Excel se zobrazí nový **Operátor**.</span><span class="sxs-lookup"><span data-stu-id="a9f89-150">In the Excel parameter file, a new **Operator** field appears.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a9f89-151">Pokud používáte starší verzi nástrojů RSAT, musíte vygenerovat nové soubory parametrů aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="a9f89-151">If you've been using an older version of RSAT, you must generate new Excel parameter files.</span></span>

    ![Pole Operátor](./media/use_rsa_tool_07.png)

<span data-ttu-id="a9f89-153">V následujícím příkladu je ukázáno, jak lze pomocí této funkce ověřit, zda je množství na skladě větší než 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="a9f89-153">The following example shows how you can use this feature to validate whether the on-hand inventory is more than 0 (zero).</span></span>

1. <span data-ttu-id="a9f89-154">V ukázkových datech společnosti **USMF** vytvořte záznam úloh, který má následující kroky:</span><span class="sxs-lookup"><span data-stu-id="a9f89-154">In the demo data in the **USMF** company, create a task recording that has the following steps:</span></span>

    1. <span data-ttu-id="a9f89-155">Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="a9f89-155">Go to **Product information management \> Products \> Released products**.</span></span>
    2. <span data-ttu-id="a9f89-156">Použijte rychlý filtr pro hledání záznamů.</span><span class="sxs-lookup"><span data-stu-id="a9f89-156">Use the Quick Filter to find records.</span></span> <span data-ttu-id="a9f89-157">Například filtrujte na hodnotě **1000** pole **Číslo položky**.</span><span class="sxs-lookup"><span data-stu-id="a9f89-157">For example, filter on a value of **1000** for the **Item number** field.</span></span>
    3. <span data-ttu-id="a9f89-158">Vyberte **Zásoby na skladě**.</span><span class="sxs-lookup"><span data-stu-id="a9f89-158">Select **On-hand inventory**.</span></span>
    4. <span data-ttu-id="a9f89-159">Použijte rychlý filtr pro hledání záznamů.</span><span class="sxs-lookup"><span data-stu-id="a9f89-159">Use the Quick Filter to find records.</span></span> <span data-ttu-id="a9f89-160">Můžete například filtrovat na hodnotě **1** pro pole **Pracoviště**.</span><span class="sxs-lookup"><span data-stu-id="a9f89-160">For example, filter on a value of **1** for the **Site** field.</span></span>
    5. <span data-ttu-id="a9f89-161">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="a9f89-161">In the list, mark the selected row.</span></span>
    6. <span data-ttu-id="a9f89-162">Ověřte, zda hodnota pole **Celkem k dispozici** je **411.0000000000000000**.</span><span class="sxs-lookup"><span data-stu-id="a9f89-162">Validate that the value of the **Total available** field is **411.0000000000000000**.</span></span>

2. <span data-ttu-id="a9f89-163">Uložte záznam úloh do knihovny BPM v LCS a synchronizujte ho do Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="a9f89-163">Save the task recording to the BPM library in LCS, and sync it to Azure DevOps.</span></span>
3. <span data-ttu-id="a9f89-164">Přidejte testovací případ do testovacího plánu a načtěte testovací případ do RSAT.</span><span class="sxs-lookup"><span data-stu-id="a9f89-164">Add the test case to the test plan, and load the test case into RSAT.</span></span>
4. <span data-ttu-id="a9f89-165">Otevřete soubor parametrů aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="a9f89-165">Open the Excel parameter file.</span></span> <span data-ttu-id="a9f89-166">Na kartě **InventOnhandItem** se zobrazí část **Ověřit InventOnhandItem**, která obsahuje pole **Operátor**.</span><span class="sxs-lookup"><span data-stu-id="a9f89-166">On the **InventOnhandItem** tab, you will see a **Validate InventOnhandItem** section that includes an **Operator** field.</span></span>

    ![Pole Operátor](./media/use_rsa_tool_08.png)

5. <span data-ttu-id="a9f89-168">Chcete-li ověřit, zda bude množství na skladě vždy větší než 0, změňte hodnotu pole **Hodnota** z **411** na **0** a hodnotu pole **Operátor** od znaménka rovná se (**=**). na znaménko větší než (**\>**).</span><span class="sxs-lookup"><span data-stu-id="a9f89-168">To validate whether the inventory on-hand will always be more than 0, change the value of the **Value** field from **411** to **0** and the value of the **Operator** field from an equal sign (**=**) to a greater than sign (**\>**).</span></span>

    ![Hodnoty polí Hodnota a Operátor byly změněny.](./media/use_rsa_tool_09.png)

6. <span data-ttu-id="a9f89-170">Uložte a zavřete soubor parametrů aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="a9f89-170">Save and close the Excel parameter file.</span></span>
7. <span data-ttu-id="a9f89-171">Vyberte **Odeslat** pro uložení provedených změn souboru parametrů aplikace Excel do Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="a9f89-171">Select **Upload** to save the changes that you made to the Excel parameter file to Azure DevOps.</span></span>

<span data-ttu-id="a9f89-172">Nyní, pokud je hodnota pole **Celkem k dispozici** pro určitou položku ve skladu větší než 0 (nula), testy budou úspěšné, bez ohledu na skutečnou hodnotu zásob na skladě.</span><span class="sxs-lookup"><span data-stu-id="a9f89-172">Now, if the value of the **Total Available** field for the specified item in inventory is more than 0 (zero), tests will pass, regardless of the actual on-hand inventory value.</span></span>

### <a name="generator-logs"></a><span data-ttu-id="a9f89-173">Protokoly generátoru</span><span class="sxs-lookup"><span data-stu-id="a9f89-173">Generator logs</span></span>

<span data-ttu-id="a9f89-174">Tato funkce vytvoří složku obsahující protokoly testovacích případů, které byly spuštěny.</span><span class="sxs-lookup"><span data-stu-id="a9f89-174">This feature creates a folder that contains the logs of the test cases that have been run.</span></span>

- <span data-ttu-id="a9f89-175">Chcete-li použít tuto funkci, otevřete soubor **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** v instalační složce sady RSAT (například **C:\\Program Files (x86)\\Regression Suite Automation Tool**) a změňte hodnotu v následujícím prvku z **false** na **true**.</span><span class="sxs-lookup"><span data-stu-id="a9f89-175">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value in the following element from **false** to **true**.</span></span>

    ```xml
    <add key="LogGeneration" value="false" />
    ```

<span data-ttu-id="a9f89-176">Po spuštění testovacích případů můžete vyhledat soubory protokolů ve složce **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.</span><span class="sxs-lookup"><span data-stu-id="a9f89-176">After the test cases are run, you can find the log files under **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\generatorLogs**.</span></span>

![Složka GeneratorLogs](./media/use_rsa_tool_10.png)

> [!NOTE]
> <span data-ttu-id="a9f89-178">Pokud existovaly testovací případy před změnou hodnoty v souboru. config, nebudou protokoly generovány pro tyto testovací případy, dokud nevytvoříte nové soubory spuštění testu.</span><span class="sxs-lookup"><span data-stu-id="a9f89-178">If there were existing test cases before you changed the value in the .config file, logs won't be generated for those test cases until you generate new test execution files.</span></span>
> 
> ![Příkaz Generovat pouze soubory spuštění testu v nabídce Nový](./media/use_rsa_tool_11.png)

### <a name="snapshot"></a><span data-ttu-id="a9f89-180">Snímek</span><span class="sxs-lookup"><span data-stu-id="a9f89-180">Snapshot</span></span>

<span data-ttu-id="a9f89-181">Tato funkce pořídí snímky obrazovek kroků, které byly provedeny při záznamu úloh.</span><span class="sxs-lookup"><span data-stu-id="a9f89-181">This feature takes screenshots of the steps that were performed during task recording.</span></span>

- <span data-ttu-id="a9f89-182">Chcete-li použít tuto funkci, otevřete soubor **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** v instalační složce sady RSAT (například **C:\\Program Files (x86)\\Regression Suite Automation Tool**) a změňte hodnotu následujícího prvku z **false** na **true**.</span><span class="sxs-lookup"><span data-stu-id="a9f89-182">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value of the following element from **false** to **true**.</span></span>

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

<span data-ttu-id="a9f89-183">Pro každý spuštěný testovací případ se vytvoří samostatná složka pod Under **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**.</span><span class="sxs-lookup"><span data-stu-id="a9f89-183">Under **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, a separate folder is created for each test case that is run.</span></span>

![Složka snímku pro testovací případ](./media/use_rsa_tool_12.png)

<span data-ttu-id="a9f89-185">V každé z těchto složek můžete vyhledat snímky kroků, které byly provedeny při spuštění testovacích případů.</span><span class="sxs-lookup"><span data-stu-id="a9f89-185">In each of these folders, you can find snapshots of the steps that were performed while the test cases were run.</span></span>

![Soubory snímků](./media/use_rsa_tool_13.png)

## <a name="assignment"></a><span data-ttu-id="a9f89-187">Přiřazení</span><span class="sxs-lookup"><span data-stu-id="a9f89-187">Assignment</span></span>

### <a name="scenario"></a><span data-ttu-id="a9f89-188">Scénář</span><span class="sxs-lookup"><span data-stu-id="a9f89-188">Scenario</span></span>

1. <span data-ttu-id="a9f89-189">Návrhář produktu vytvoří nový uvolněný produkt.</span><span class="sxs-lookup"><span data-stu-id="a9f89-189">The product designer creates a new released product.</span></span>
2. <span data-ttu-id="a9f89-190">Vedoucí výroby iniciuje výrobní zakázku za účelem zvýšení zásob na dva kusy.</span><span class="sxs-lookup"><span data-stu-id="a9f89-190">The production manager initiates a production order to bring the stock level to two pieces.</span></span>
3. <span data-ttu-id="a9f89-191">Výroba zahájí a ukončí výrobní zakázku a ověří, že množství na skladě jsou dva kusy.</span><span class="sxs-lookup"><span data-stu-id="a9f89-191">Manufacturing starts and ends the production order, and verifies that the on-hand quantity is two pieces.</span></span>
4. <span data-ttu-id="a9f89-192">Prodejní tým obdrží objednávku na čtyři kusy nového produktu.</span><span class="sxs-lookup"><span data-stu-id="a9f89-192">The sales team receives an order for four pieces of the new product.</span></span> <span data-ttu-id="a9f89-193">Prodejní tým proto aktualizuje čisté požadavky prostřednictvím dynamického plánu.</span><span class="sxs-lookup"><span data-stu-id="a9f89-193">Therefore, the sales team updates the net requirements via the dynamic plan.</span></span> <span data-ttu-id="a9f89-194">Vzhledem k tomu, že žádná další kapacita není k dispozici, je výchozí zásada objednávky nastavena na hodnotu „koupit místo vyrobit“.</span><span class="sxs-lookup"><span data-stu-id="a9f89-194">Because no additional capacity is available, the default order policy is set to "buy instead of make."</span></span> <span data-ttu-id="a9f89-195">Proto se vytvoří plánovaná nákupní objednávka.</span><span class="sxs-lookup"><span data-stu-id="a9f89-195">Therefore, a planned purchase order is created.</span></span>
5. <span data-ttu-id="a9f89-196">Kupující přidá dodavatele, podepíše plánovanou nákupní objednávku a poté potvrdí nákupní objednávku.</span><span class="sxs-lookup"><span data-stu-id="a9f89-196">The buyer adds a vendor, firms the planned purchase order, and then confirms the purchase order.</span></span>
6. <span data-ttu-id="a9f89-197">Po doručení zakoupeného zboží do skladu vyhledá operátor skladu související nákupní objednávku a přijme zboží.</span><span class="sxs-lookup"><span data-stu-id="a9f89-197">When the goods that were purchased arrive at the store, the store operator searches the related purchase order and receives the goods.</span></span> <span data-ttu-id="a9f89-198">Vzhledem k tomu, že objednávka je nyní dokončena, lze zboží vydat a zabalit proti prodejní objednávce.</span><span class="sxs-lookup"><span data-stu-id="a9f89-198">Because the order is now completed, goods can be picked and packed against the sales order.</span></span>
7. <span data-ttu-id="a9f89-199">Finance zaúčtují nákupní fakturu a prodejní fakturu.</span><span class="sxs-lookup"><span data-stu-id="a9f89-199">Finance posts the purchase invoice and sales invoice.</span></span>

<span data-ttu-id="a9f89-200">Následující ilustrace znázorňuje tok pro tento scénář.</span><span class="sxs-lookup"><span data-stu-id="a9f89-200">The following illustration shows the flow for this scenario.</span></span>

![Tok ukázkového scénáře](./media/use_rsa_tool_14.png)

<span data-ttu-id="a9f89-202">Následující ilustrace znázorňuje obchodní procesy pro tento scénář v RSAT.</span><span class="sxs-lookup"><span data-stu-id="a9f89-202">The following illustration shows the business processes for this scenario in RSAT.</span></span>

![Obchodní procesy pro ukázkový scénář](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a><span data-ttu-id="a9f89-204">Strategie – klíčové učení</span><span class="sxs-lookup"><span data-stu-id="a9f89-204">Strategy – Key learning</span></span>

### <a name="data"></a><span data-ttu-id="a9f89-205">Údaje</span><span class="sxs-lookup"><span data-stu-id="a9f89-205">Data</span></span>

- <span data-ttu-id="a9f89-206">Ujistěte se, že máte reprezentativní datové objemy (kopie dat produkční/zlaté konfigurace a přenesená data).</span><span class="sxs-lookup"><span data-stu-id="a9f89-206">Make sure that you have representative data volumes (a copy of production/golden configuration data plus migrated data).</span></span>
- <span data-ttu-id="a9f89-207">Když generujete nová data pomocí záznamníku úloh, vytvořte názvy testů, které nekolidují s existujícími názvy (například použijte předponu **RSATxxx**).</span><span class="sxs-lookup"><span data-stu-id="a9f89-207">When you generate new data via Task recorder, create test names that won't conflict with existing names (for example, use a prefix such as **RSATxxx**).</span></span>
- <span data-ttu-id="a9f89-208">Použijte obnovení k určitému bodu v čase Azure- pro opětovné spuštění testů v prostředích, které nejsou v úrovni 1.</span><span class="sxs-lookup"><span data-stu-id="a9f89-208">Use Azure Point-In-Time restore to rerun tests in non-Tier 1 environments.</span></span>
- <span data-ttu-id="a9f89-209">Ačkoli můžete použít funkce Excelu **RANDOM** a **NOW** k vygenerování jedinečné kombinace, úsilí je poměrně vysoké.</span><span class="sxs-lookup"><span data-stu-id="a9f89-209">Although you can use the **RANDOM** and **NOW** Excel functions to generate a unique combination, the effort is considerably high.</span></span> <span data-ttu-id="a9f89-210">Následuje příklad.</span><span class="sxs-lookup"><span data-stu-id="a9f89-210">Here is an example.</span></span>

    ```Excel
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a><span data-ttu-id="a9f89-211">Záznamník úkolů</span><span class="sxs-lookup"><span data-stu-id="a9f89-211">Task recorder</span></span>

- <span data-ttu-id="a9f89-212">Definujte scénáře před zahájením záznamu.</span><span class="sxs-lookup"><span data-stu-id="a9f89-212">Define scenarios before you start recording.</span></span> <span data-ttu-id="a9f89-213">Dobře spravovaný projekt má předdefinované scénáře testování.</span><span class="sxs-lookup"><span data-stu-id="a9f89-213">A well-managed project has predefined test scenarios.</span></span> <span data-ttu-id="a9f89-214">Chcete-li vytvořit testovací případ, zvažte, jak předvídatelné výsledky těchto testů jsou.</span><span class="sxs-lookup"><span data-stu-id="a9f89-214">To build a test case, consider how predictable the outcome of those test scenarios is.</span></span>
- <span data-ttu-id="a9f89-215">Záznamy rozdělte, pokud je provedete různými rolemi, nebo pokud se před dalším krokem vyskytl čas čekání nebo externí událost.</span><span class="sxs-lookup"><span data-stu-id="a9f89-215">Split recordings if they are performed by different roles, or if there is waiting time or an external event before the next step.</span></span>
- <span data-ttu-id="a9f89-216">Vyhněte se výběru hodnot v seznamech.</span><span class="sxs-lookup"><span data-stu-id="a9f89-216">Avoid selecting values in lists.</span></span> <span data-ttu-id="a9f89-217">Místo toho použijte textové formáty, jako například **FIFO**, **AudioRM** a **SiteWH**.</span><span class="sxs-lookup"><span data-stu-id="a9f89-217">Instead, use text formats, such as **FIFO**, **AudioRM**, and **SiteWH**.</span></span> <span data-ttu-id="a9f89-218">Vyberete-li možnost v seznamu, bude zaznamenána pozice hodnoty v seznamu, nikoli hodnota samotná.</span><span class="sxs-lookup"><span data-stu-id="a9f89-218">When you select in a list, the position of the value in the list is recorded, not the value itself.</span></span> <span data-ttu-id="a9f89-219">Pokud jsou do seznamu přidány položky, bude možné změnit pozici hodnoty.</span><span class="sxs-lookup"><span data-stu-id="a9f89-219">If items are added to that list, the position of the value can change.</span></span> <span data-ttu-id="a9f89-220">Proto bude nahrávka používat jiný parametr a může to mít vliv na zbytek scénáře.</span><span class="sxs-lookup"><span data-stu-id="a9f89-220">Therefore, your recording will use a different parameter, and the rest of the scenario might be affected.</span></span>
- <span data-ttu-id="a9f89-221">Zamyslete se nad chováním více uživatelů.</span><span class="sxs-lookup"><span data-stu-id="a9f89-221">Think about multi-user behavior.</span></span> <span data-ttu-id="a9f89-222">Nepředpokládejte například, že nově vytvořená prodejní objednávka bude vždy vybrána automaticky.</span><span class="sxs-lookup"><span data-stu-id="a9f89-222">For example, don't assume that your newly created sales order will always be automatically selected.</span></span> <span data-ttu-id="a9f89-223">Místo toho vždy použijte ke zjištění správné objednávky filtr.</span><span class="sxs-lookup"><span data-stu-id="a9f89-223">Instead, always use the filter to find the correct order.</span></span>
- <span data-ttu-id="a9f89-224">Použijte funkci kopírování v záznamníku úloh pro uložení názvu nově vytvořeného produktu, aby jej bylo možné použít ve zřetězených testovacích případech.</span><span class="sxs-lookup"><span data-stu-id="a9f89-224">Use the Copy function in Task recorder to save the name of a newly created product so it can be used in chained test cases.</span></span>
- <span data-ttu-id="a9f89-225">Použijte funkci ověření v záznamníku úloh pro nastavení kontrolních bodů, které ověřují, zda byly provedeny správné kroky.</span><span class="sxs-lookup"><span data-stu-id="a9f89-225">Use the Validate function in Task recorder to set checkpoints that verify that steps have been run correctly.</span></span>

### <a name="rsat"></a><span data-ttu-id="a9f89-226">RSAT</span><span class="sxs-lookup"><span data-stu-id="a9f89-226">RSAT</span></span>

- <span data-ttu-id="a9f89-227">Chcete-li spustit test v jiné společnosti, můžete změnit společnost na kartě **Obecné** v souboru parametrů aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="a9f89-227">To run the test in another company, you can change the company on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="a9f89-228">Zkontrolujte, zda jsou v nově vybrané společnosti k dispozici nastavení a data.</span><span class="sxs-lookup"><span data-stu-id="a9f89-228">Make sure that settings and data are available in the newly selected company.</span></span>
- <span data-ttu-id="a9f89-229">Testovacího uživatele můžete změnit na kartě **Obecné** v souboru parametrů aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="a9f89-229">You can change the test user on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="a9f89-230">Zadejte ID e-mailu uživatele, který spustí testovací případ.</span><span class="sxs-lookup"><span data-stu-id="a9f89-230">Specify the email ID of the user who will run the test case.</span></span> <span data-ttu-id="a9f89-231">Tímto způsobem lze testovací případ spustit pomocí oprávnění zabezpečení zadaného uživatele.</span><span class="sxs-lookup"><span data-stu-id="a9f89-231">In this way, the test case can be run by using the security permissions of the specified user.</span></span>
- <span data-ttu-id="a9f89-232">Chcete-li počkat před zahájením testu, můžete na kartě **Obecné** v souboru parametrů aplikace Excel definovat pauzu.</span><span class="sxs-lookup"><span data-stu-id="a9f89-232">To wait before the test is started, you can define a pause on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="a9f89-233">Toto pozastavení lze použít v dávkové úloze (například v případě, že je nutné spustit workflow ještě před provedením dalšího kroku).</span><span class="sxs-lookup"><span data-stu-id="a9f89-233">This pause can be used in a batch job (for example, if a workflow must be run before the next step can be performed.)</span></span>

## <a name="advanced-scripting"></a><span data-ttu-id="a9f89-234">Pokročilé skriptování</span><span class="sxs-lookup"><span data-stu-id="a9f89-234">Advanced scripting</span></span>

### <a name="cli"></a><span data-ttu-id="a9f89-235">CLI</span><span class="sxs-lookup"><span data-stu-id="a9f89-235">CLI</span></span>

<span data-ttu-id="a9f89-236">RSAT lze volat z okna **Příkazového řádku** nebo **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="a9f89-236">RSAT can be called from a **Command Prompt** or **PowerShell** window.</span></span>

> [!NOTE]
> <span data-ttu-id="a9f89-237">Ověřte, zda je proměnná prostředí **TestRoot** nastavena na cestu instalace RSAT.</span><span class="sxs-lookup"><span data-stu-id="a9f89-237">Verify that the **TestRoot** environment variable is set to the RSAT installation path.</span></span> <span data-ttu-id="a9f89-238">(V Microsoft Windows otevřete **Ovládací panel**, vyberte **Systém a zabezpečení \> Systém \> Pokročilá nastavení systému** a pak zvolte **Proměnné prostředí**.)</span><span class="sxs-lookup"><span data-stu-id="a9f89-238">(In Microsoft Windows, open **Control Panel**, select **System and Security \> System \> Advanced system settings**, and then select **Environment Variables**.)</span></span>

1. <span data-ttu-id="a9f89-239">Otevřete okno **příkazového řádku** nebo **PowerShell** jako správce.</span><span class="sxs-lookup"><span data-stu-id="a9f89-239">Open a **Command Prompt** or **PowerShell** window as an admin.</span></span>
2. <span data-ttu-id="a9f89-240">Přejděte do instalačního adresáře RSAT.</span><span class="sxs-lookup"><span data-stu-id="a9f89-240">Navigate to the RSAT installation directory.</span></span>

    ```Console
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. <span data-ttu-id="a9f89-241">Vyvolejte seznam všech příkazů.</span><span class="sxs-lookup"><span data-stu-id="a9f89-241">List all commands.</span></span>

    ```Console
    C:\Program Files (x86)\Regression Suite Automation Tool>Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe help

    Usage:
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe command
        or
        Microsoft.Dynamics.RegressionSuite.ConsoleApp.exe /settings "C:\Path to\file.settings" command

    Available commands:
        ?
        about
        cls
        download
        edit
        generate
        generatederived
        generatetestonly
        generatetestsuite
        help
        list
        listtestplans
        listtestsuite
        listtestsuitenames
        playback
        playbackbyid
        playbackmany
        playbacksuite
        quit
        upload
        uploadrecording
        usage
    ```

#### <a name=""></a><span data-ttu-id="a9f89-242">?</span><span class="sxs-lookup"><span data-stu-id="a9f89-242">?</span></span> 
<span data-ttu-id="a9f89-243">Zobrazí nápovědu ke všem dostupným příkazům a jejich parametrům.</span><span class="sxs-lookup"><span data-stu-id="a9f89-243">Shows help about all available commands and their parameters.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="optional-parameters"></a><span data-ttu-id="a9f89-244">Volitelné parametry</span><span class="sxs-lookup"><span data-stu-id="a9f89-244">Optional parameters</span></span>

**``command``**


<span data-ttu-id="a9f89-245">Kde ``[command]`` je jeden z níže uvedených příkazů.</span><span class="sxs-lookup"><span data-stu-id="a9f89-245">Where ``[command]`` is one of the commands specified below.</span></span>


#### <a name="about"></a><span data-ttu-id="a9f89-246">O aplikaci</span><span class="sxs-lookup"><span data-stu-id="a9f89-246">about</span></span>
<span data-ttu-id="a9f89-247">Zobrazí aktuální verze.</span><span class="sxs-lookup"><span data-stu-id="a9f89-247">Displays the current version.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a><span data-ttu-id="a9f89-248">cls</span><span class="sxs-lookup"><span data-stu-id="a9f89-248">cls</span></span>
<span data-ttu-id="a9f89-249">Vymaže obrazovku.</span><span class="sxs-lookup"><span data-stu-id="a9f89-249">Clears the screen.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**


#### <a name="download"></a><span data-ttu-id="a9f89-250">stáhnout</span><span class="sxs-lookup"><span data-stu-id="a9f89-250">download</span></span>
<span data-ttu-id="a9f89-251">Stáhne přílohy pro zadaný testovací případ do výstupního adresáře.</span><span class="sxs-lookup"><span data-stu-id="a9f89-251">Downloads attachments for the specified test case to the output directory.</span></span> <span data-ttu-id="a9f89-252">Pomocí příkazu ``list`` můžete získat všechny dostupné testovací případy.</span><span class="sxs-lookup"><span data-stu-id="a9f89-252">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="a9f89-253">Jako parametr **test_case_id** použijte libovolnou hodnotu z prvního sloupce.</span><span class="sxs-lookup"><span data-stu-id="a9f89-253">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="a9f89-254">Povinné parametry</span><span class="sxs-lookup"><span data-stu-id="a9f89-254">Required parameters</span></span>
<span data-ttu-id="a9f89-255">**``test_case_id``** Představuje ID testovacího případu.</span><span class="sxs-lookup"><span data-stu-id="a9f89-255">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="a9f89-256">**``output_dir``** Představuje výstupní adresář.</span><span class="sxs-lookup"><span data-stu-id="a9f89-256">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="a9f89-257">Adresář musí existovat.</span><span class="sxs-lookup"><span data-stu-id="a9f89-257">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="a9f89-258">Příklad</span><span class="sxs-lookup"><span data-stu-id="a9f89-258">Examples</span></span>

``download 123 c:\temp\rsat``   
``download 765 c:\rsat\last``


#### <a name="edit"></a><span data-ttu-id="a9f89-259">upravit</span><span class="sxs-lookup"><span data-stu-id="a9f89-259">edit</span></span>
<span data-ttu-id="a9f89-260">Umožňuje otevřít soubor parametrů v aplikaci Excel a upravit jej.</span><span class="sxs-lookup"><span data-stu-id="a9f89-260">Allows you to open parameters file in Excel program and edit it.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="required-parameters"></a><span data-ttu-id="a9f89-261">Povinné parametry</span><span class="sxs-lookup"><span data-stu-id="a9f89-261">Required parameters</span></span>
<span data-ttu-id="a9f89-262">**``excel_file``** Musí obsahovat úplnou cestu k existujícímu souboru aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="a9f89-262">**``excel_file``** Must contain a full path to an existing Excel file.</span></span>

##### <a name="examples"></a><span data-ttu-id="a9f89-263">Příklad</span><span class="sxs-lookup"><span data-stu-id="a9f89-263">Examples</span></span>
``edit c:\RSAT\TestCase_123_Base.xlsx``  
``edit e:\temp\TestCase_456_Base.xlsx``


#### <a name="generate"></a><span data-ttu-id="a9f89-264">generovat</span><span class="sxs-lookup"><span data-stu-id="a9f89-264">generate</span></span>
<span data-ttu-id="a9f89-265">Generuje spuštění testu a soubory parametrů pro zadaný testovací případ v výstupním adresáři.</span><span class="sxs-lookup"><span data-stu-id="a9f89-265">Generates test execution and parameter files for the specified test case in the output directory.</span></span>
<span data-ttu-id="a9f89-266">Pomocí příkazu ``list`` můžete získat všechny dostupné testovací případy.</span><span class="sxs-lookup"><span data-stu-id="a9f89-266">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="a9f89-267">Jako parametr **test_case_id** použijte libovolnou hodnotu z prvního sloupce.</span><span class="sxs-lookup"><span data-stu-id="a9f89-267">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="a9f89-268">Povinné parametry</span><span class="sxs-lookup"><span data-stu-id="a9f89-268">Required parameters</span></span>
<span data-ttu-id="a9f89-269">**``test_case_id``** Představuje ID testovacího případu.</span><span class="sxs-lookup"><span data-stu-id="a9f89-269">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="a9f89-270">**``output_dir``** Představuje výstupní adresář.</span><span class="sxs-lookup"><span data-stu-id="a9f89-270">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="a9f89-271">Adresář musí existovat.</span><span class="sxs-lookup"><span data-stu-id="a9f89-271">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="a9f89-272">Příklad</span><span class="sxs-lookup"><span data-stu-id="a9f89-272">Examples</span></span>
``generate 123 c:\temp\rsat``  
``generate 765 c:\rsat\last``


#### <a name="generatederived"></a><span data-ttu-id="a9f89-273">generatederived</span><span class="sxs-lookup"><span data-stu-id="a9f89-273">generatederived</span></span>
<span data-ttu-id="a9f89-274">Generuje nový testovací případ odvozený od poskytnutého testovacího případu.</span><span class="sxs-lookup"><span data-stu-id="a9f89-274">Generates a new test case, derived from the provided test case.</span></span> <span data-ttu-id="a9f89-275">Pomocí příkazu ``list`` můžete získat všechny dostupné testovací případy.</span><span class="sxs-lookup"><span data-stu-id="a9f89-275">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="a9f89-276">Jako parametr **test_case_id** použijte libovolnou hodnotu z prvního sloupce.</span><span class="sxs-lookup"><span data-stu-id="a9f89-276">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="required-parameters"></a><span data-ttu-id="a9f89-277">Povinné parametry</span><span class="sxs-lookup"><span data-stu-id="a9f89-277">Required parameters</span></span>
<span data-ttu-id="a9f89-278">**``parent_test_case_id``** Představuje ID nadřazeného testovacího případu.</span><span class="sxs-lookup"><span data-stu-id="a9f89-278">**``parent_test_case_id``** Represents the parent test case ID.</span></span>  
<span data-ttu-id="a9f89-279">**``test_plan_id``** Představuje ID testovacího plánu.</span><span class="sxs-lookup"><span data-stu-id="a9f89-279">**``test_plan_id``** Represents the test plan ID.</span></span>  
<span data-ttu-id="a9f89-280">**``test_suite_id``** Představuje ID testovací sady.</span><span class="sxs-lookup"><span data-stu-id="a9f89-280">**``test_suite_id``** Represents the test suite ID.</span></span>

##### <a name="examples"></a><span data-ttu-id="a9f89-281">Příklad</span><span class="sxs-lookup"><span data-stu-id="a9f89-281">Examples</span></span>
``generatederived 123 8901 678``


#### <a name="generatetestonly"></a><span data-ttu-id="a9f89-282">generatetestonly</span><span class="sxs-lookup"><span data-stu-id="a9f89-282">generatetestonly</span></span>
<span data-ttu-id="a9f89-283">Generuje pouze soubor spuštění testu pro zadaný testovací případ v výstupním adresáři.</span><span class="sxs-lookup"><span data-stu-id="a9f89-283">Generates only test execution file for the specified test case in the output directory.</span></span> <span data-ttu-id="a9f89-284">Pomocí příkazu ``list`` můžete získat všechny dostupné testovací případy.</span><span class="sxs-lookup"><span data-stu-id="a9f89-284">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="a9f89-285">Jako parametr **test_case_id** použijte libovolnou hodnotu z prvního sloupce.</span><span class="sxs-lookup"><span data-stu-id="a9f89-285">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="a9f89-286">Povinné parametry</span><span class="sxs-lookup"><span data-stu-id="a9f89-286">Required parameters</span></span>
<span data-ttu-id="a9f89-287">**``test_case_id``** Představuje ID testovacího případu.</span><span class="sxs-lookup"><span data-stu-id="a9f89-287">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="a9f89-288">**``output_dir``** Představuje výstupní adresář.</span><span class="sxs-lookup"><span data-stu-id="a9f89-288">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="a9f89-289">Adresář musí existovat.</span><span class="sxs-lookup"><span data-stu-id="a9f89-289">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="a9f89-290">Příklad</span><span class="sxs-lookup"><span data-stu-id="a9f89-290">Examples</span></span>
``generatetestonly 123 c:\temp\rsat``  
``generatetestonly 765 c:\rsat\last``


#### <a name="generatetestsuite"></a><span data-ttu-id="a9f89-291">generatetestsuite</span><span class="sxs-lookup"><span data-stu-id="a9f89-291">generatetestsuite</span></span>
<span data-ttu-id="a9f89-292">Generuje všechny testovací případy pro zadanou sadu ve výstupním adresáři.</span><span class="sxs-lookup"><span data-stu-id="a9f89-292">Generates all test cases for the specified suite in the output directory.</span></span>
<span data-ttu-id="a9f89-293">Pomocí příkazu ``listtestsuitenames`` můžete získat všechny dostupné testovací sady.</span><span class="sxs-lookup"><span data-stu-id="a9f89-293">You can use ``listtestsuitenames`` command to get all available test suits.</span></span> <span data-ttu-id="a9f89-294">Jako parametr **test_suite_name** použijte libovolnou hodnotu z prvního sloupce.</span><span class="sxs-lookup"><span data-stu-id="a9f89-294">Use any value from the column as a **test_suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[test_suite_name] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="a9f89-295">Povinné parametry</span><span class="sxs-lookup"><span data-stu-id="a9f89-295">Required parameters</span></span>
<span data-ttu-id="a9f89-296">**``test_suite_name``** Představuje název testovací sady.</span><span class="sxs-lookup"><span data-stu-id="a9f89-296">**``test_suite_name``** Represents the test suite name.</span></span>  
<span data-ttu-id="a9f89-297">**``output_dir``** Představuje výstupní adresář.</span><span class="sxs-lookup"><span data-stu-id="a9f89-297">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="a9f89-298">Adresář musí existovat.</span><span class="sxs-lookup"><span data-stu-id="a9f89-298">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="a9f89-299">Příklad</span><span class="sxs-lookup"><span data-stu-id="a9f89-299">Examples</span></span>
``generatetestsuite Tests c:\temp\rsat``   
``generatetestsuite Purchase c:\rsat\last``


#### <a name="help"></a><span data-ttu-id="a9f89-300">nápověda</span><span class="sxs-lookup"><span data-stu-id="a9f89-300">help</span></span>
<span data-ttu-id="a9f89-301">Totožný s [?](####?)</span><span class="sxs-lookup"><span data-stu-id="a9f89-301">Identical to the [?](####?)</span></span> <span data-ttu-id="a9f89-302">příkaz</span><span class="sxs-lookup"><span data-stu-id="a9f89-302">command</span></span>


#### <a name="list"></a><span data-ttu-id="a9f89-303">seznamu</span><span class="sxs-lookup"><span data-stu-id="a9f89-303">list</span></span>
<span data-ttu-id="a9f89-304">Obsahuje seznam všech dostupných testovacích případů.</span><span class="sxs-lookup"><span data-stu-id="a9f89-304">Lists all available test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**


#### <a name="listtestplans"></a><span data-ttu-id="a9f89-305">listtestplans</span><span class="sxs-lookup"><span data-stu-id="a9f89-305">listtestplans</span></span>
<span data-ttu-id="a9f89-306">Obsahuje seznam všech dostupných testovacích plánů.</span><span class="sxs-lookup"><span data-stu-id="a9f89-306">Lists all available test plans.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**


#### <a name="listtestsuite"></a><span data-ttu-id="a9f89-307">listtestsuite</span><span class="sxs-lookup"><span data-stu-id="a9f89-307">listtestsuite</span></span>
<span data-ttu-id="a9f89-308">Uvádí seznam testovacích případů pro zadanou testovací sadu.</span><span class="sxs-lookup"><span data-stu-id="a9f89-308">Lists test cases for the specified test suite.</span></span> <span data-ttu-id="a9f89-309">Pomocí příkazu ``listtestsuitenames`` můžete získat všechny dostupné testovací sady.</span><span class="sxs-lookup"><span data-stu-id="a9f89-309">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="a9f89-310">Jako parametr **suite_name** použijte libovolnou hodnotu z prvního sloupce.</span><span class="sxs-lookup"><span data-stu-id="a9f89-310">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[suite_name]``

##### <a name="required-parameters"></a><span data-ttu-id="a9f89-311">Povinné parametry</span><span class="sxs-lookup"><span data-stu-id="a9f89-311">Required parameters</span></span>
<span data-ttu-id="a9f89-312">**``suite_name``** Název požadované sady.</span><span class="sxs-lookup"><span data-stu-id="a9f89-312">**``suite_name``** Name of the desired suite.</span></span>

##### <a name="examples"></a><span data-ttu-id="a9f89-313">Příklad</span><span class="sxs-lookup"><span data-stu-id="a9f89-313">Examples</span></span>
``listtestsuite "sample suite name"``  
``listtestsuite NameOfTheSuite``


#### <a name="listtestsuitenames"></a><span data-ttu-id="a9f89-314">listtestsuitenames</span><span class="sxs-lookup"><span data-stu-id="a9f89-314">listtestsuitenames</span></span>
<span data-ttu-id="a9f89-315">Obsahuje seznam všech dostupných testovacích sad.</span><span class="sxs-lookup"><span data-stu-id="a9f89-315">Lists all available test suites.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**


#### <a name="playback"></a><span data-ttu-id="a9f89-316">playback</span><span class="sxs-lookup"><span data-stu-id="a9f89-316">playback</span></span>
<span data-ttu-id="a9f89-317">Přehraje testovací případ pomocí souboru aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="a9f89-317">Plays back a test case using an Excel file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[excel_file]``

##### <a name="required-parameters"></a><span data-ttu-id="a9f89-318">Povinné parametry</span><span class="sxs-lookup"><span data-stu-id="a9f89-318">Required parameters</span></span>
<span data-ttu-id="a9f89-319">**``excel_file``** Úplná cesta k souboru aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="a9f89-319">**``excel_file``** A full path to the Excel file.</span></span> <span data-ttu-id="a9f89-320">Soubor musí existovat.</span><span class="sxs-lookup"><span data-stu-id="a9f89-320">File must exist.</span></span> 

##### <a name="examples"></a><span data-ttu-id="a9f89-321">Příklad</span><span class="sxs-lookup"><span data-stu-id="a9f89-321">Examples</span></span>
``
playback c:\RSAT\TestCaseParameters\sample1.xlsx
playback e:\temp\test.xlsx
``


#### <a name="playbackbyid"></a><span data-ttu-id="a9f89-322">playbackbyid</span><span class="sxs-lookup"><span data-stu-id="a9f89-322">playbackbyid</span></span>
<span data-ttu-id="a9f89-323">Přehrává se více testovacích případů najednou.</span><span class="sxs-lookup"><span data-stu-id="a9f89-323">Plays back multiple test cases at once.</span></span>
<span data-ttu-id="a9f89-324">Pomocí příkazu ``list`` můžete získat všechny dostupné testovací případy.</span><span class="sxs-lookup"><span data-stu-id="a9f89-324">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="a9f89-325">Jako parametr **test_case_id** použijte libovolnou hodnotu z prvního sloupce.</span><span class="sxs-lookup"><span data-stu-id="a9f89-325">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="required-parameters"></a><span data-ttu-id="a9f89-326">Povinné parametry</span><span class="sxs-lookup"><span data-stu-id="a9f89-326">Required parameters</span></span>
<span data-ttu-id="a9f89-327">**``test_case_id1``** ID existujícího testovacího případu.</span><span class="sxs-lookup"><span data-stu-id="a9f89-327">**``test_case_id1``** ID of exisiting test case.</span></span>  
<span data-ttu-id="a9f89-328">**``test_case_id2``** ID existujícího testovacího případu.</span><span class="sxs-lookup"><span data-stu-id="a9f89-328">**``test_case_id2``** ID of exisiting test case.</span></span>  
<span data-ttu-id="a9f89-329">**``test_case_idN``** ID existujícího testovacího případu.</span><span class="sxs-lookup"><span data-stu-id="a9f89-329">**``test_case_idN``** ID of exisiting test case.</span></span>  

##### <a name="examples"></a><span data-ttu-id="a9f89-330">Příklad</span><span class="sxs-lookup"><span data-stu-id="a9f89-330">Examples</span></span>
``playbackbyid 878``  
``playbackbyid 2345 667 135``


#### <a name="playbackmany"></a><span data-ttu-id="a9f89-331">playbackmany</span><span class="sxs-lookup"><span data-stu-id="a9f89-331">playbackmany</span></span>
<span data-ttu-id="a9f89-332">Přehraje řadu testovacích případů najednou pomocí souborů aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="a9f89-332">Plays back many test cases at once, using Excel files.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[excel_file1] [excel_file2] ... [excel_fileN]``

##### <a name="required-parameters"></a><span data-ttu-id="a9f89-333">Povinné parametry</span><span class="sxs-lookup"><span data-stu-id="a9f89-333">Required parameters</span></span>
<span data-ttu-id="a9f89-334">**``excel_file1``** Úplná cesta k souboru aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="a9f89-334">**``excel_file1``** Full path to the Excel file.</span></span> <span data-ttu-id="a9f89-335">Soubor musí existovat.</span><span class="sxs-lookup"><span data-stu-id="a9f89-335">File must exist.</span></span>  
<span data-ttu-id="a9f89-336">**``excel_file2``** Úplná cesta k souboru aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="a9f89-336">**``excel_file2``** Full path to the Excel file.</span></span> <span data-ttu-id="a9f89-337">Soubor musí existovat.</span><span class="sxs-lookup"><span data-stu-id="a9f89-337">File must exist.</span></span>  
<span data-ttu-id="a9f89-338">**``excel_fileN``** Úplná cesta k souboru aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="a9f89-338">**``excel_fileN``** Full path to the Excel file.</span></span> <span data-ttu-id="a9f89-339">Soubor musí existovat.</span><span class="sxs-lookup"><span data-stu-id="a9f89-339">File must exist.</span></span>  

##### <a name="examples"></a><span data-ttu-id="a9f89-340">Příklad</span><span class="sxs-lookup"><span data-stu-id="a9f89-340">Examples</span></span>
``playbackmany c:\RSAT\TestCaseParameters\param1.xlsx``  
``playbackmany e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx``


#### <a name="playbacksuite"></a><span data-ttu-id="a9f89-341">playbacksuite</span><span class="sxs-lookup"><span data-stu-id="a9f89-341">playbacksuite</span></span>
<span data-ttu-id="a9f89-342">Přehraje všechny testovací případy ze zadané sady testů.</span><span class="sxs-lookup"><span data-stu-id="a9f89-342">Plays back all test cases from the specified test suite.</span></span> <span data-ttu-id="a9f89-343">Pomocí příkazu ``listtestsuitenames`` můžete získat všechny dostupné testovací sady.</span><span class="sxs-lookup"><span data-stu-id="a9f89-343">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="a9f89-344">Jako parametr **suite_name** použijte libovolnou hodnotu z prvního sloupce.</span><span class="sxs-lookup"><span data-stu-id="a9f89-344">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[suite_name]``

##### <a name="required-parameters"></a><span data-ttu-id="a9f89-345">Povinné parametry</span><span class="sxs-lookup"><span data-stu-id="a9f89-345">Required parameters</span></span>
<span data-ttu-id="a9f89-346">**``suite_name``** Název požadované sady.</span><span class="sxs-lookup"><span data-stu-id="a9f89-346">**``suite_name``** Name of the desired suite.</span></span>

##### <a name="examples"></a><span data-ttu-id="a9f89-347">Příklad</span><span class="sxs-lookup"><span data-stu-id="a9f89-347">Examples</span></span>
``playbacksuite suiteName``  
``playbacksuite sample_suite``


#### <a name="quit"></a><span data-ttu-id="a9f89-348">opustit</span><span class="sxs-lookup"><span data-stu-id="a9f89-348">quit</span></span>
<span data-ttu-id="a9f89-349">Zavře aplikaci.</span><span class="sxs-lookup"><span data-stu-id="a9f89-349">Closes the  application.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**


#### <a name="upload"></a><span data-ttu-id="a9f89-350">upload</span><span class="sxs-lookup"><span data-stu-id="a9f89-350">upload</span></span>
<span data-ttu-id="a9f89-351">Odešle všechny soubory náležející do zadané sady testů nebo testovacích případů.</span><span class="sxs-lookup"><span data-stu-id="a9f89-351">Uploads all files belonging to the specified test suite or test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``[suite_name] [testcase_id]``

#### <a name="required-parameters"></a><span data-ttu-id="a9f89-352">Povinné parametry</span><span class="sxs-lookup"><span data-stu-id="a9f89-352">Required parameters</span></span>
<span data-ttu-id="a9f89-353">**``suite_name``** Odešle všechny soubory náležející do zadané testovací sady.</span><span class="sxs-lookup"><span data-stu-id="a9f89-353">**``suite_name``** All files belonging to the specified test suite will be uploaded.</span></span>
<span data-ttu-id="a9f89-354">**``testcase_id``** Odešle všechny soubory náležející do zadaných testovacích případů.</span><span class="sxs-lookup"><span data-stu-id="a9f89-354">**``testcase_id``** All files beloning to the specified test case(s) will be uploaded.</span></span>

##### <a name="examples"></a><span data-ttu-id="a9f89-355">Příklad</span><span class="sxs-lookup"><span data-stu-id="a9f89-355">Examples</span></span>
``upload sample_suite``  
``upload 123``  
``upload 123 456``


#### <a name="uploadrecording"></a><span data-ttu-id="a9f89-356">uploadrecording</span><span class="sxs-lookup"><span data-stu-id="a9f89-356">uploadrecording</span></span>
<span data-ttu-id="a9f89-357">Odešle pouze soubor nahrávky, který náleží do zadaných testovacích případů.</span><span class="sxs-lookup"><span data-stu-id="a9f89-357">Uploads only recording file belonging to the specified test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[testcase_id]``

##### <a name="required-parameters"></a><span data-ttu-id="a9f89-358">Povinné parametry</span><span class="sxs-lookup"><span data-stu-id="a9f89-358">Required parameters</span></span>
<span data-ttu-id="a9f89-359">**``testcase_id``** Odešle soubor nahrávky, který náleží do zadaných testovacích případů.</span><span class="sxs-lookup"><span data-stu-id="a9f89-359">**``testcase_id``** Recording file belonging to the specified test cases will be uploaded.</span></span>

##### <a name="examples"></a><span data-ttu-id="a9f89-360">Příklad</span><span class="sxs-lookup"><span data-stu-id="a9f89-360">Examples</span></span>
``uploadrecording 123``  
``uploadrecording 123 456``


#### <a name="usage"></a><span data-ttu-id="a9f89-361">použití</span><span class="sxs-lookup"><span data-stu-id="a9f89-361">usage</span></span>
<span data-ttu-id="a9f89-362">Zobrazení dvou způsobů vyvolání této aplikace: jeden s použitím souboru výchozího nastavení, další poskytuje soubor nastavení.</span><span class="sxs-lookup"><span data-stu-id="a9f89-362">Shows two ways to invoke this application: one using a default setting file, another one providing a setting file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**


### <a name="windows-powershell-examples"></a><span data-ttu-id="a9f89-363">Příklad Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="a9f89-363">Windows PowerShell examples</span></span>

#### <a name="run-a-test-case-in-a-loop"></a><span data-ttu-id="a9f89-364">Spuštění testovacího případu ve smyčce</span><span class="sxs-lookup"><span data-stu-id="a9f89-364">Run a test case in a loop</span></span>

<span data-ttu-id="a9f89-365">Máte testovací skript, který vytvoří nového odběratele.</span><span class="sxs-lookup"><span data-stu-id="a9f89-365">You have a test script that creates a new customer.</span></span> <span data-ttu-id="a9f89-366">Pomocí skriptování lze tento testovací případ spustit ve smyčce tak, že před spuštěním každé iterace náhodně použijete následující data:</span><span class="sxs-lookup"><span data-stu-id="a9f89-366">Via scripting, this test case can be run in a loop by randomizing the following data before each iteration is run:</span></span>

- <span data-ttu-id="a9f89-367">ID odběratele</span><span class="sxs-lookup"><span data-stu-id="a9f89-367">Customer ID</span></span>
- <span data-ttu-id="a9f89-368">Jméno zákazníka</span><span class="sxs-lookup"><span data-stu-id="a9f89-368">Customer name</span></span>
- <span data-ttu-id="a9f89-369">Adresa odběratele</span><span class="sxs-lookup"><span data-stu-id="a9f89-369">Customer address</span></span>

<span data-ttu-id="a9f89-370">ID zákazníka bude mít formát *ATCUS\<číslo\>*, kde \<číslo\> je hodnota mezi **000000001** a **999999999**.</span><span class="sxs-lookup"><span data-stu-id="a9f89-370">The customer ID will be in the format *ATCUS\<number\>*, where \<number\> is a value between **000000001** and **999999999**.</span></span>

<span data-ttu-id="a9f89-371">V následujícím příkladu je použit jeden parametr **start** pro definování prvního použitého čísla.</span><span class="sxs-lookup"><span data-stu-id="a9f89-371">The following example uses one parameter, **start**, to define the first number that is used.</span></span> <span data-ttu-id="a9f89-372">Aplikace používá k definování počtu odběratelů, které je nutné vytvořit, druhý parametr **nr**.</span><span class="sxs-lookup"><span data-stu-id="a9f89-372">Is uses a second parameter, **nr**, to define the number of customers that must be created.</span></span> <span data-ttu-id="a9f89-373">Parametry v souboru parametrů aplikace Excel jsou pro každou iteraci změněny pomocí funkce UpdateCustomer.</span><span class="sxs-lookup"><span data-stu-id="a9f89-373">For each iteration, the parameters in the Excel parameter file are changed by using an UpdateCustomer function.</span></span> <span data-ttu-id="a9f89-374">Poté bude příkazový řádek RSAT volán ve funkci RunTestCase.</span><span class="sxs-lookup"><span data-stu-id="a9f89-374">Then the RSAT command line is called in a RunTestCase function.</span></span>

<span data-ttu-id="a9f89-375">Otevřete Microsoft Windows PowerShell Integrated Scripting Environment (ISE) v režimu správy a vložte následující kód do okna s názvem **Untitled1. ps1.**</span><span class="sxs-lookup"><span data-stu-id="a9f89-375">Open Microsoft Windows PowerShell Integrated Scripting Environment (ISE) in admin mode, and paste the following code into the window that is named **Untitled1.ps1**.</span></span>

```powershell
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

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a><span data-ttu-id="a9f89-376">Spuštění skriptu, který závisí na datech v Microsoft Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="a9f89-376">Run a script that depends on data in Microsoft Dynamics 365</span></span>

<span data-ttu-id="a9f89-377">V následujícím příkladu je pomocí volání OData (Open Data Protocol) nalezen stav nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="a9f89-377">The following example uses an Open Data Protocol (OData) call to find the order status of a purchase order.</span></span> <span data-ttu-id="a9f89-378">Pokud není stav **fakturován**, můžete například volat testovací případ RSAT, který zaúčtuje fakturu.</span><span class="sxs-lookup"><span data-stu-id="a9f89-378">If the status isn't **invoiced**, you can, for example, call an RSAT test case that posts the invoice.</span></span>

```xpp
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
