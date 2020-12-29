---
title: Použití kurzu pro nástroj Regression Suite Automation Tool
description: Toto téma ukazuje, jak používat Regression Suite Automation Tool (RSAT). Popisuje různé funkce a poskytuje příklady, které používají pokročilé skriptování.
author: robinarh
manager: AnnBe
ms.date: 06/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 21761
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 798717b276e68949a9425350720bf683a37d6fb5
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/08/2020
ms.locfileid: "4692983"
---
# <a name="regression-suite-automation-tool-tutorial"></a><span data-ttu-id="ea379-104">Kurz pro nástroj Regression Suite Automation Tool</span><span class="sxs-lookup"><span data-stu-id="ea379-104">Regression suite automation tool tutorial</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="ea379-105">Pomocí nástrojů internetového prohlížeče můžete tuto stránku stáhnout a uložit ve formátu PDF.</span><span class="sxs-lookup"><span data-stu-id="ea379-105">Use your internet browser tools to download and save this page in pdf format.</span></span> 

<span data-ttu-id="ea379-106">Tento kurz prochází některými rozšířenými funkcemi nástroje Regression Suite Automation Tool (RSAT), zahrnuje přiřazení ukázky a popisuje strategii a klíčové body učení.</span><span class="sxs-lookup"><span data-stu-id="ea379-106">This tutorial walks through some of the advanced features of the Regression suite automation tool (RSAT), includes a demo assignment, and describes strategy and key learning points.</span></span> 

## <a name="notable-features-of-rsat-and-task-recorder"></a><span data-ttu-id="ea379-107">Významné funkce RSAT a Záznamník úloh</span><span class="sxs-lookup"><span data-stu-id="ea379-107">Notable Features of RSAT and Task recorder</span></span>

### <a name="validate-a-field-value"></a><span data-ttu-id="ea379-108">Ověření hodnoty pole</span><span class="sxs-lookup"><span data-stu-id="ea379-108">Validate a field value</span></span>

<span data-ttu-id="ea379-109">Nástroje RSAT umožňují do testovacího případu zahrnout kroky ověření pro ověření očekávaných hodnot.</span><span class="sxs-lookup"><span data-stu-id="ea379-109">RSAT allows you to include validation steps within your test case to validate expected values.</span></span> <span data-ttu-id="ea379-110">Další informace o této funkci naleznete v článku [Ověření očekávaných hodnot](../../dev-itpro/perf-test/rsat/rsat-validate-expected.md).</span><span class="sxs-lookup"><span data-stu-id="ea379-110">For information about this feature, see the article [Validate expected values](../../dev-itpro/perf-test/rsat/rsat-validate-expected.md).</span></span>

<span data-ttu-id="ea379-111">V následujícím příkladu je ukázáno, jak lze pomocí této funkce ověřit, zda je množství na skladě větší než 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="ea379-111">The following example shows how you can use this feature to validate whether the on-hand inventory is more than 0 (zero).</span></span>

1. <span data-ttu-id="ea379-112">V ukázkových datech společnosti **USMF** vytvořte záznam úloh, který má následující kroky:</span><span class="sxs-lookup"><span data-stu-id="ea379-112">In the demo data in the **USMF** company, create a task recording that has the following steps:</span></span>

    1. <span data-ttu-id="ea379-113">Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.</span><span class="sxs-lookup"><span data-stu-id="ea379-113">Go to **Product information management \> Products \> Released products**.</span></span>
    2. <span data-ttu-id="ea379-114">Použijte rychlý filtr pro hledání záznamů.</span><span class="sxs-lookup"><span data-stu-id="ea379-114">Use the Quick Filter to find records.</span></span> <span data-ttu-id="ea379-115">Například filtrujte na hodnotě **1000** pole **Číslo položky**.</span><span class="sxs-lookup"><span data-stu-id="ea379-115">For example, filter on a value of **1000** for the **Item number** field.</span></span>
    3. <span data-ttu-id="ea379-116">Vyberte **Zásoby na skladě**.</span><span class="sxs-lookup"><span data-stu-id="ea379-116">Select **On-hand inventory**.</span></span>
    4. <span data-ttu-id="ea379-117">Použijte rychlý filtr pro hledání záznamů.</span><span class="sxs-lookup"><span data-stu-id="ea379-117">Use the Quick Filter to find records.</span></span> <span data-ttu-id="ea379-118">Můžete například filtrovat na hodnotě **1** pro pole **Pracoviště**.</span><span class="sxs-lookup"><span data-stu-id="ea379-118">For example, filter on a value of **1** for the **Site** field.</span></span>
    5. <span data-ttu-id="ea379-119">Označte na seznamu vybraný řádek.</span><span class="sxs-lookup"><span data-stu-id="ea379-119">In the list, mark the selected row.</span></span>
    6. <span data-ttu-id="ea379-120">Ověřte, zda hodnota pole **Celkem k dispozici** je **411.0000000000000000**.</span><span class="sxs-lookup"><span data-stu-id="ea379-120">Validate that the value of the **Total available** field is **411.0000000000000000**.</span></span>

2. <span data-ttu-id="ea379-121">Uložte záznam úlohy a připojte jej k testovacímu případu v Azure Devops.</span><span class="sxs-lookup"><span data-stu-id="ea379-121">Save the task recording and attach it to your test case in Azure Devops.</span></span>
3. <span data-ttu-id="ea379-122">Přidejte testovací případ do testovacího plánu a načtěte testovací případ do RSAT.</span><span class="sxs-lookup"><span data-stu-id="ea379-122">Add the test case to the test plan, and load the test case into RSAT.</span></span>
4. <span data-ttu-id="ea379-123">Otevřete soubor parametrů aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="ea379-123">Open the Excel parameter file.</span></span> <span data-ttu-id="ea379-124">Na kartě **InventOnhandItem** se zobrazí část **Ověřit InventOnhandItem**, která obsahuje pole **Operátor**.</span><span class="sxs-lookup"><span data-stu-id="ea379-124">On the **InventOnhandItem** tab, you will see a **Validate InventOnhandItem** section that includes an **Operator** field.</span></span>

    ![Pole Operátor](./media/use_rsa_tool_08.png)

5. <span data-ttu-id="ea379-126">Chcete-li ověřit, zda bude množství na skladě vždy větší než 0, změňte hodnotu pole **Hodnota** z **411** na **0** a hodnotu pole **Operátor** od znaménka rovná se (**=**). na znaménko větší než (**\>**).</span><span class="sxs-lookup"><span data-stu-id="ea379-126">To validate whether the inventory on-hand will always be more than 0, change the value of the **Value** field from **411** to **0** and the value of the **Operator** field from an equal sign (**=**) to a greater than sign (**\>**).</span></span>

    ![Hodnoty polí Hodnota a Operátor byly změněny.](./media/use_rsa_tool_09.png)

6. <span data-ttu-id="ea379-128">Uložte a zavřete soubor parametrů aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="ea379-128">Save and close the Excel parameter file.</span></span>
7. <span data-ttu-id="ea379-129">Vyberte **Odeslat** pro uložení provedených změn souboru parametrů aplikace Excel do Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="ea379-129">Select **Upload** to save the changes that you made to the Excel parameter file to Azure DevOps.</span></span>

<span data-ttu-id="ea379-130">Nyní, pokud je hodnota pole **Celkem k dispozici** pro určitou položku ve skladu větší než 0 (nula), testy budou úspěšné, bez ohledu na skutečnou hodnotu zásob na skladě.</span><span class="sxs-lookup"><span data-stu-id="ea379-130">Now, if the value of the **Total Available** field for the specified item in inventory is more than 0 (zero), tests will pass, regardless of the actual on-hand inventory value.</span></span>

### <a name="saved-variables-and-chaining-of-test-cases"></a><span data-ttu-id="ea379-131">Uložené proměnné a zřetězení testovacích případů</span><span class="sxs-lookup"><span data-stu-id="ea379-131">Saved variables and chaining of test cases</span></span>

<span data-ttu-id="ea379-132">Jednou z klíčových funkcí nástroje RSAT je zřetězení testovacích případů, tj. schopnost testu předat hodnoty jiným testům.</span><span class="sxs-lookup"><span data-stu-id="ea379-132">One of the key features of RSAT is the chaining of test cases, that is, the ability of a test to pass variables to other tests.</span></span> <span data-ttu-id="ea379-133">Další informace naleznete v článku [Kopie proměnných pro zřetězení testovacích případů](../../dev-itpro/perf-test/rsat/rsat-chain-test-cases.md).</span><span class="sxs-lookup"><span data-stu-id="ea379-133">For more information, see the article [Copy variables to chain test cases](../../dev-itpro/perf-test/rsat/rsat-chain-test-cases.md).</span></span>

### <a name="derived-test-case"></a><span data-ttu-id="ea379-134">Odvozený testovací případ</span><span class="sxs-lookup"><span data-stu-id="ea379-134">Derived test case</span></span>

<span data-ttu-id="ea379-135">RSAT umožňuje používat stejný Záznam úloh s více testovacími případy, který umožňuje spuštění úlohy s různými konfiguracemi dat.</span><span class="sxs-lookup"><span data-stu-id="ea379-135">RSAT lets you use the same task recording with multiple test cases, enabling a task to run with different data configurations.</span></span> <span data-ttu-id="ea379-136">Další informace naleznete v článku [Odvozené testovací případy](../../dev-itpro/perf-test/rsat/rsat-derived-test-cases.md).</span><span class="sxs-lookup"><span data-stu-id="ea379-136">See the article [Derived test cases](../../dev-itpro/perf-test/rsat/rsat-derived-test-cases.md) for more information.</span></span>

### <a name="validate-notifications-and-messages"></a><span data-ttu-id="ea379-137">Ověřit oznámení a zprávy</span><span class="sxs-lookup"><span data-stu-id="ea379-137">Validate notifications and messages</span></span>

<span data-ttu-id="ea379-138">Tuto funkci lze použít k ověření, zda došlo k akci.</span><span class="sxs-lookup"><span data-stu-id="ea379-138">This feature can be used to validate whether an action occurred.</span></span> <span data-ttu-id="ea379-139">Je-li například vytvořena, odhadnuta a následně zahájena výrobní zakázka, aplikace zobrazí zprávu „Výroba - Zahájení“ a upozorní vás, že výrobní zakázka byla zahájena.</span><span class="sxs-lookup"><span data-stu-id="ea379-139">For example, when a production order is created, estimated, and then started, the app shows a "Production – Start" message to notify you that the production order has been started.</span></span>

![Oznámení Výroba - Zahájení](./media/use_rsa_tool_05.png)

<span data-ttu-id="ea379-141">Tuto zprávu můžete ověřit prostřednictvím RSAT zadáním textu zprávy na kartě **Ověření zprávy** souboru parametrů aplikace Excel pro příslušný záznam.</span><span class="sxs-lookup"><span data-stu-id="ea379-141">You can validate this message through RSAT by entering the message text on the **MessageValidation** tab of the Excel parameter file for the appropriate recording.</span></span>

![Karta Ověření zprávy](./media/use_rsa_tool_06.png)

<span data-ttu-id="ea379-143">Po spuštění testovacího případu se zpráva v souboru parametrů aplikace Excel porovná se zprávou zobrazenou.</span><span class="sxs-lookup"><span data-stu-id="ea379-143">After the test case is run, the message in the Excel parameter file is compared to the message that is shown.</span></span> <span data-ttu-id="ea379-144">Pokud se zprávy neshodují, testovací případ se nezdaří.</span><span class="sxs-lookup"><span data-stu-id="ea379-144">If the messages don't match, the test case will fail.</span></span>

> [!NOTE]
> <span data-ttu-id="ea379-145">Na kartě **Ověření zprávy** v souboru parametrů aplikace Excel můžete zadat více než jednu zprávu.</span><span class="sxs-lookup"><span data-stu-id="ea379-145">You can enter more than one message on the **MessageValidation** tab in the Excel parameter file.</span></span> <span data-ttu-id="ea379-146">Zprávy mohou být také chybové nebo varovné namísto informačních zpráv.</span><span class="sxs-lookup"><span data-stu-id="ea379-146">The messages also can be error or warning messages instead of informational messages.</span></span>

### <a name="snapshot"></a><span data-ttu-id="ea379-147">Snímek</span><span class="sxs-lookup"><span data-stu-id="ea379-147">Snapshot</span></span>

<span data-ttu-id="ea379-148">Tato funkce pořídí snímky obrazovek kroků, které byly provedeny při záznamu úloh.</span><span class="sxs-lookup"><span data-stu-id="ea379-148">This feature takes screenshots of the steps that were performed during task recording.</span></span> <span data-ttu-id="ea379-149">Je užitečný pro účely auditu nebo ladění.</span><span class="sxs-lookup"><span data-stu-id="ea379-149">It is useful for auditing or debugging purposes.</span></span>

- <span data-ttu-id="ea379-150">Chcete-li použít tuto funkci, otevřete soubor **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** v instalační složce sady RSAT (například **C:\\Program Files (x86)\\Regression Suite Automation Tool**) a změňte hodnotu následujícího prvku z **false** na **true**.</span><span class="sxs-lookup"><span data-stu-id="ea379-150">To use this feature, open the **Microsoft.Dynamics.RegressionSuite.WindowsApp.exe.config** file under the RSAT installation folder (for example, **C:\\Program Files (x86)\\Regression Suite Automation Tool**), and change the value of the following element from **false** to **true**.</span></span>

    ```xml
    <add key="VerboseSnapshotsEnabled" value="false" />
    ```

<span data-ttu-id="ea379-151">Když spustíte testovací případ, RSAT bude generovat snímky (obrázky) kroků ve složce přehrávání v testovacích případech v pracovním adresáři.</span><span class="sxs-lookup"><span data-stu-id="ea379-151">When your run the test case, RSAT will generate snapshots (images) of the steps in the playback folder of the test cases in the working diretory.</span></span> <span data-ttu-id="ea379-152">Používáte-li starší verzi nástroje RSAT, jsou obrázky uloženy do **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback** a pro každý spuštěný testovací případ je vytvořena samostatná složka.</span><span class="sxs-lookup"><span data-stu-id="ea379-152">If you are using an older version of RSAT, the images are saved to **C:\\Users\\\<Username\>\\AppData\\Roaming\\regressionTool\\playback**, a separate folder is created for each test case that is run.</span></span>

## <a name="assignment"></a><span data-ttu-id="ea379-153">Přiřazení</span><span class="sxs-lookup"><span data-stu-id="ea379-153">Assignment</span></span>

### <a name="scenario"></a><span data-ttu-id="ea379-154">Scénář</span><span class="sxs-lookup"><span data-stu-id="ea379-154">Scenario</span></span>

1. <span data-ttu-id="ea379-155">Návrhář produktu vytvoří nový uvolněný produkt.</span><span class="sxs-lookup"><span data-stu-id="ea379-155">The product designer creates a new released product.</span></span>
2. <span data-ttu-id="ea379-156">Vedoucí výroby iniciuje výrobní zakázku za účelem zvýšení zásob na dva kusy.</span><span class="sxs-lookup"><span data-stu-id="ea379-156">The production manager initiates a production order to bring the stock level to two pieces.</span></span>
3. <span data-ttu-id="ea379-157">Výroba zahájí a ukončí výrobní zakázku a ověří, že množství na skladě jsou dva kusy.</span><span class="sxs-lookup"><span data-stu-id="ea379-157">Manufacturing starts and ends the production order, and verifies that the on-hand quantity is two pieces.</span></span>
4. <span data-ttu-id="ea379-158">Prodejní tým obdrží objednávku na čtyři kusy nového produktu.</span><span class="sxs-lookup"><span data-stu-id="ea379-158">The sales team receives an order for four pieces of the new product.</span></span> <span data-ttu-id="ea379-159">Prodejní tým proto aktualizuje čisté požadavky prostřednictvím dynamického plánu.</span><span class="sxs-lookup"><span data-stu-id="ea379-159">Therefore, the sales team updates the net requirements via the dynamic plan.</span></span> <span data-ttu-id="ea379-160">Vzhledem k tomu, že žádná další kapacita není k dispozici, je výchozí zásada objednávky nastavena na hodnotu „koupit místo vyrobit“.</span><span class="sxs-lookup"><span data-stu-id="ea379-160">Because no additional capacity is available, the default order policy is set to "buy instead of make."</span></span> <span data-ttu-id="ea379-161">Proto se vytvoří plánovaná nákupní objednávka.</span><span class="sxs-lookup"><span data-stu-id="ea379-161">Therefore, a planned purchase order is created.</span></span>
5. <span data-ttu-id="ea379-162">Kupující přidá dodavatele, podepíše plánovanou nákupní objednávku a poté potvrdí nákupní objednávku.</span><span class="sxs-lookup"><span data-stu-id="ea379-162">The buyer adds a vendor, firms the planned purchase order, and then confirms the purchase order.</span></span>
6. <span data-ttu-id="ea379-163">Po doručení zakoupeného zboží do skladu vyhledá operátor skladu související nákupní objednávku a přijme zboží.</span><span class="sxs-lookup"><span data-stu-id="ea379-163">When the goods that were purchased arrive at the store, the store operator searches the related purchase order and receives the goods.</span></span> <span data-ttu-id="ea379-164">Vzhledem k tomu, že objednávka je nyní dokončena, lze zboží vydat a zabalit proti prodejní objednávce.</span><span class="sxs-lookup"><span data-stu-id="ea379-164">Because the order is now completed, goods can be picked and packed against the sales order.</span></span>
7. <span data-ttu-id="ea379-165">Finance zaúčtují nákupní fakturu a prodejní fakturu.</span><span class="sxs-lookup"><span data-stu-id="ea379-165">Finance posts the purchase invoice and sales invoice.</span></span>

<span data-ttu-id="ea379-166">Následující ilustrace znázorňuje tok pro tento scénář.</span><span class="sxs-lookup"><span data-stu-id="ea379-166">The following illustration shows the flow for this scenario.</span></span>

![Tok ukázkového scénáře](./media/use_rsa_tool_14.png)

<span data-ttu-id="ea379-168">Na následujícím obrázku je znázorněna hierarchie obchodních procesů pro tento scénář v modulu pro Modelování obchodních procesů LCS.</span><span class="sxs-lookup"><span data-stu-id="ea379-168">The following illustration shows the business processes hierarchy for this scenario in the LCS Business Process Modeler.</span></span>

![Obchodní procesy pro ukázkový scénář](./media/use_rsa_tool_15.png)

## <a name="strategy--key-learning"></a><span data-ttu-id="ea379-170">Strategie – klíčové učení</span><span class="sxs-lookup"><span data-stu-id="ea379-170">Strategy – Key learning</span></span>

### <a name="data"></a><span data-ttu-id="ea379-171">Údaje</span><span class="sxs-lookup"><span data-stu-id="ea379-171">Data</span></span>

- <span data-ttu-id="ea379-172">Ujistěte se, že máte reprezentativní datové objemy (kopie dat produkční/zlaté konfigurace a přenesená data).</span><span class="sxs-lookup"><span data-stu-id="ea379-172">Make sure that you have representative data volumes (a copy of production/golden configuration data plus migrated data).</span></span>
- <span data-ttu-id="ea379-173">Když generujete nová data pomocí záznamníku úloh, vytvořte názvy testů, které nekolidují s existujícími názvy (například použijte předponu **RSATxxx**).</span><span class="sxs-lookup"><span data-stu-id="ea379-173">When you generate new data via Task recorder, create test names that won't conflict with existing names (for example, use a prefix such as **RSATxxx**).</span></span>
- <span data-ttu-id="ea379-174">Použijte obnovení k určitému bodu v čase Azure- pro opětovné spuštění testů v prostředích, které nejsou v úrovni 1.</span><span class="sxs-lookup"><span data-stu-id="ea379-174">Use Azure Point-In-Time restore to rerun tests in non-Tier 1 environments.</span></span>
- <span data-ttu-id="ea379-175">Ačkoli můžete použít funkce Excelu **RANDOM** a **NOW** k vygenerování jedinečné kombinace, úsilí je poměrně vysoké.</span><span class="sxs-lookup"><span data-stu-id="ea379-175">Although you can use the **RANDOM** and **NOW** Excel functions to generate a unique combination, the effort is considerably high.</span></span> <span data-ttu-id="ea379-176">Následuje příklad.</span><span class="sxs-lookup"><span data-stu-id="ea379-176">Here is an example.</span></span>

    ```Excel
    product = "AT" &TEXT(NOW(),"yyymmddhhmm")
    ```

### <a name="task-recorder"></a><span data-ttu-id="ea379-177">Záznamník úkolů</span><span class="sxs-lookup"><span data-stu-id="ea379-177">Task recorder</span></span>

- <span data-ttu-id="ea379-178">Definujte scénáře před zahájením záznamu.</span><span class="sxs-lookup"><span data-stu-id="ea379-178">Define scenarios before you start recording.</span></span> <span data-ttu-id="ea379-179">Dobře spravovaný projekt má předdefinované scénáře testování.</span><span class="sxs-lookup"><span data-stu-id="ea379-179">A well-managed project has predefined test scenarios.</span></span> <span data-ttu-id="ea379-180">Chcete-li vytvořit testovací případ, zvažte, jak předvídatelné výsledky těchto testů jsou.</span><span class="sxs-lookup"><span data-stu-id="ea379-180">To build a test case, consider how predictable the outcome of those test scenarios is.</span></span>
- <span data-ttu-id="ea379-181">Záznamy rozdělte, pokud je provedete různými rolemi, nebo pokud se před dalším krokem vyskytl čas čekání nebo externí událost.</span><span class="sxs-lookup"><span data-stu-id="ea379-181">Split recordings if they are performed by different roles, or if there is waiting time or an external event before the next step.</span></span>
- <span data-ttu-id="ea379-182">Vyhněte se výběru hodnot v seznamech.</span><span class="sxs-lookup"><span data-stu-id="ea379-182">Avoid selecting values in lists.</span></span> <span data-ttu-id="ea379-183">Místo toho použijte textové formáty, jako například **FIFO**, **AudioRM** a **SiteWH**.</span><span class="sxs-lookup"><span data-stu-id="ea379-183">Instead, use text formats, such as **FIFO**, **AudioRM**, and **SiteWH**.</span></span> <span data-ttu-id="ea379-184">Vyberete-li možnost v seznamu, bude zaznamenána pozice hodnoty v seznamu, nikoli hodnota samotná.</span><span class="sxs-lookup"><span data-stu-id="ea379-184">When you select in a list, the position of the value in the list is recorded, not the value itself.</span></span> <span data-ttu-id="ea379-185">Pokud jsou do seznamu přidány položky, bude možné změnit pozici hodnoty.</span><span class="sxs-lookup"><span data-stu-id="ea379-185">If items are added to that list, the position of the value can change.</span></span> <span data-ttu-id="ea379-186">Proto bude nahrávka používat jiný parametr a může to mít vliv na zbytek scénáře.</span><span class="sxs-lookup"><span data-stu-id="ea379-186">Therefore, your recording will use a different parameter, and the rest of the scenario might be affected.</span></span>
- <span data-ttu-id="ea379-187">Zamyslete se nad chováním více uživatelů.</span><span class="sxs-lookup"><span data-stu-id="ea379-187">Think about multi-user behavior.</span></span> <span data-ttu-id="ea379-188">Nepředpokládejte například, že nově vytvořená prodejní objednávka bude vždy vybrána automaticky.</span><span class="sxs-lookup"><span data-stu-id="ea379-188">For example, don't assume that your newly created sales order will always be automatically selected.</span></span> <span data-ttu-id="ea379-189">Místo toho vždy použijte ke zjištění správné objednávky filtr.</span><span class="sxs-lookup"><span data-stu-id="ea379-189">Instead, always use the filter to find the correct order.</span></span>
- <span data-ttu-id="ea379-190">Použijte funkci kopírování v záznamníku úloh pro uložení názvu nově vytvořeného produktu, aby jej bylo možné použít ve zřetězených testovacích případech.</span><span class="sxs-lookup"><span data-stu-id="ea379-190">Use the Copy function in Task recorder to save the name of a newly created product so it can be used in chained test cases.</span></span>
- <span data-ttu-id="ea379-191">Použijte funkci ověření v záznamníku úloh pro nastavení kontrolních bodů, které ověřují, zda byly provedeny správné kroky.</span><span class="sxs-lookup"><span data-stu-id="ea379-191">Use the Validate function in Task recorder to set checkpoints that verify that steps have been run correctly.</span></span>

### <a name="rsat"></a><span data-ttu-id="ea379-192">RSAT</span><span class="sxs-lookup"><span data-stu-id="ea379-192">RSAT</span></span>

- <span data-ttu-id="ea379-193">Chcete-li spustit test v jiné společnosti, můžete změnit společnost na kartě **Obecné** v souboru parametrů aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="ea379-193">To run the test in another company, you can change the company on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="ea379-194">Zkontrolujte, zda jsou v nově vybrané společnosti k dispozici nastavení a data.</span><span class="sxs-lookup"><span data-stu-id="ea379-194">Make sure that settings and data are available in the newly selected company.</span></span>
- <span data-ttu-id="ea379-195">Testovacího uživatele můžete změnit na kartě **Obecné** v souboru parametrů aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="ea379-195">You can change the test user on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="ea379-196">Zadejte ID e-mailu uživatele, který spustí testovací případ.</span><span class="sxs-lookup"><span data-stu-id="ea379-196">Specify the email ID of the user who will run the test case.</span></span> <span data-ttu-id="ea379-197">Tímto způsobem lze testovací případ spustit pomocí oprávnění zabezpečení zadaného uživatele.</span><span class="sxs-lookup"><span data-stu-id="ea379-197">In this way, the test case can be run by using the security permissions of the specified user.</span></span>
- <span data-ttu-id="ea379-198">Chcete-li počkat před zahájením testu, můžete na kartě **Obecné** v souboru parametrů aplikace Excel definovat pauzu.</span><span class="sxs-lookup"><span data-stu-id="ea379-198">To wait before the test is started, you can define a pause on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="ea379-199">Toto pozastavení lze použít v dávkové úloze (například v případě, že je nutné spustit workflow ještě před provedením dalšího kroku).</span><span class="sxs-lookup"><span data-stu-id="ea379-199">This pause can be used in a batch job (for example, if a workflow must be run before the next step can be performed.)</span></span>

## <a name="advanced-scripting"></a><span data-ttu-id="ea379-200">Pokročilé skriptování</span><span class="sxs-lookup"><span data-stu-id="ea379-200">Advanced scripting</span></span>

### <a name="cli"></a><span data-ttu-id="ea379-201">CLI</span><span class="sxs-lookup"><span data-stu-id="ea379-201">CLI</span></span>

<span data-ttu-id="ea379-202">RSAT lze volat z okna **Příkazového řádku** nebo **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="ea379-202">RSAT can be called from a **Command Prompt** or **PowerShell** window.</span></span>

> [!NOTE]
> <span data-ttu-id="ea379-203">Ověřte, zda je proměnná prostředí **TestRoot** nastavena na cestu instalace RSAT.</span><span class="sxs-lookup"><span data-stu-id="ea379-203">Verify that the **TestRoot** environment variable is set to the RSAT installation path.</span></span> <span data-ttu-id="ea379-204">(V Microsoft Windows otevřete **Ovládací panel**, vyberte **Systém a zabezpečení \> Systém \> Pokročilá nastavení systému** a pak zvolte **Proměnné prostředí**.)</span><span class="sxs-lookup"><span data-stu-id="ea379-204">(In Microsoft Windows, open **Control Panel**, select **System and Security \> System \> Advanced system settings**, and then select **Environment Variables**.)</span></span>

1. <span data-ttu-id="ea379-205">Otevřete okno **příkazového řádku** nebo **PowerShell** jako správce.</span><span class="sxs-lookup"><span data-stu-id="ea379-205">Open a **Command Prompt** or **PowerShell** window as an admin.</span></span>
2. <span data-ttu-id="ea379-206">Přejděte do instalačního adresáře RSAT.</span><span class="sxs-lookup"><span data-stu-id="ea379-206">Navigate to the RSAT installation directory.</span></span>

    ```Console
    cd "c:\Program Files (x86)\Regression Suite Automation Tool\"
    ```

3. <span data-ttu-id="ea379-207">Vyvolejte seznam všech příkazů.</span><span class="sxs-lookup"><span data-stu-id="ea379-207">List all commands.</span></span>

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

#### <a name=""></a><span data-ttu-id="ea379-208">?</span><span class="sxs-lookup"><span data-stu-id="ea379-208">?</span></span> 
<span data-ttu-id="ea379-209">Zobrazí nápovědu ke všem dostupným příkazům a jejich parametrům.</span><span class="sxs-lookup"><span data-stu-id="ea379-209">Shows help about all available commands and their parameters.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``?``**``[command]``

##### <a name="optional-parameters"></a><span data-ttu-id="ea379-210">Volitelné parametry</span><span class="sxs-lookup"><span data-stu-id="ea379-210">Optional parameters</span></span>

**``command``**


<span data-ttu-id="ea379-211">Kde ``[command]`` je jeden z níže uvedených příkazů.</span><span class="sxs-lookup"><span data-stu-id="ea379-211">Where ``[command]`` is one of the commands specified below.</span></span>


#### <a name="about"></a><span data-ttu-id="ea379-212">O aplikaci</span><span class="sxs-lookup"><span data-stu-id="ea379-212">about</span></span>
<span data-ttu-id="ea379-213">Zobrazí aktuální verze.</span><span class="sxs-lookup"><span data-stu-id="ea379-213">Displays the current version.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``about``**

#### <a name="cls"></a><span data-ttu-id="ea379-214">cls</span><span class="sxs-lookup"><span data-stu-id="ea379-214">cls</span></span>
<span data-ttu-id="ea379-215">Vymaže obrazovku.</span><span class="sxs-lookup"><span data-stu-id="ea379-215">Clears the screen.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``cls``**


#### <a name="download"></a><span data-ttu-id="ea379-216">stáhnout</span><span class="sxs-lookup"><span data-stu-id="ea379-216">download</span></span>
<span data-ttu-id="ea379-217">Stáhne přílohy pro zadaný testovací případ do výstupního adresáře.</span><span class="sxs-lookup"><span data-stu-id="ea379-217">Downloads attachments for the specified test case to the output directory.</span></span> <span data-ttu-id="ea379-218">Pomocí příkazu ``list`` můžete získat všechny dostupné testovací případy.</span><span class="sxs-lookup"><span data-stu-id="ea379-218">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="ea379-219">Jako parametr **test_case_id** použijte libovolnou hodnotu z prvního sloupce.</span><span class="sxs-lookup"><span data-stu-id="ea379-219">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``download``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="ea379-220">Povinné parametry</span><span class="sxs-lookup"><span data-stu-id="ea379-220">Required parameters</span></span>
<span data-ttu-id="ea379-221">**``test_case_id``** Představuje ID testovacího případu.</span><span class="sxs-lookup"><span data-stu-id="ea379-221">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="ea379-222">**``output_dir``** Představuje výstupní adresář.</span><span class="sxs-lookup"><span data-stu-id="ea379-222">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="ea379-223">Adresář musí existovat.</span><span class="sxs-lookup"><span data-stu-id="ea379-223">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="ea379-224">Příklad</span><span class="sxs-lookup"><span data-stu-id="ea379-224">Examples</span></span>

``download 123 c:\temp\rsat``   
``download 765 c:\rsat\last``


#### <a name="edit"></a><span data-ttu-id="ea379-225">upravit</span><span class="sxs-lookup"><span data-stu-id="ea379-225">edit</span></span>
<span data-ttu-id="ea379-226">Umožňuje otevřít soubor parametrů v aplikaci Excel a upravit jej.</span><span class="sxs-lookup"><span data-stu-id="ea379-226">Allows you to open parameters file in Excel program and edit it.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``edit``**``[excel_file]``

##### <a name="required-parameters"></a><span data-ttu-id="ea379-227">Povinné parametry</span><span class="sxs-lookup"><span data-stu-id="ea379-227">Required parameters</span></span>
<span data-ttu-id="ea379-228">**``excel_file``** Musí obsahovat úplnou cestu k existujícímu souboru aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="ea379-228">**``excel_file``** Must contain a full path to an existing Excel file.</span></span>

##### <a name="examples"></a><span data-ttu-id="ea379-229">Příklad</span><span class="sxs-lookup"><span data-stu-id="ea379-229">Examples</span></span>
``edit c:\RSAT\TestCase_123_Base.xlsx``  
``edit e:\temp\TestCase_456_Base.xlsx``


#### <a name="generate"></a><span data-ttu-id="ea379-230">generovat</span><span class="sxs-lookup"><span data-stu-id="ea379-230">generate</span></span>
<span data-ttu-id="ea379-231">Generuje spuštění testu a soubory parametrů pro zadaný testovací případ v výstupním adresáři.</span><span class="sxs-lookup"><span data-stu-id="ea379-231">Generates test execution and parameter files for the specified test case in the output directory.</span></span>
<span data-ttu-id="ea379-232">Pomocí příkazu ``list`` můžete získat všechny dostupné testovací případy.</span><span class="sxs-lookup"><span data-stu-id="ea379-232">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="ea379-233">Jako parametr **test_case_id** použijte libovolnou hodnotu z prvního sloupce.</span><span class="sxs-lookup"><span data-stu-id="ea379-233">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generate``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="ea379-234">Povinné parametry</span><span class="sxs-lookup"><span data-stu-id="ea379-234">Required parameters</span></span>
<span data-ttu-id="ea379-235">**``test_case_id``** Představuje ID testovacího případu.</span><span class="sxs-lookup"><span data-stu-id="ea379-235">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="ea379-236">**``output_dir``** Představuje výstupní adresář.</span><span class="sxs-lookup"><span data-stu-id="ea379-236">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="ea379-237">Adresář musí existovat.</span><span class="sxs-lookup"><span data-stu-id="ea379-237">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="ea379-238">Příklad</span><span class="sxs-lookup"><span data-stu-id="ea379-238">Examples</span></span>
``generate 123 c:\temp\rsat``  
``generate 765 c:\rsat\last``


#### <a name="generatederived"></a><span data-ttu-id="ea379-239">generatederived</span><span class="sxs-lookup"><span data-stu-id="ea379-239">generatederived</span></span>
<span data-ttu-id="ea379-240">Generuje nový testovací případ odvozený od poskytnutého testovacího případu.</span><span class="sxs-lookup"><span data-stu-id="ea379-240">Generates a new test case, derived from the provided test case.</span></span> <span data-ttu-id="ea379-241">Pomocí příkazu ``list`` můžete získat všechny dostupné testovací případy.</span><span class="sxs-lookup"><span data-stu-id="ea379-241">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="ea379-242">Jako parametr **test_case_id** použijte libovolnou hodnotu z prvního sloupce.</span><span class="sxs-lookup"><span data-stu-id="ea379-242">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatederived``**``[parent_test_case_id] [test_plan_id] [test_suite_id]``

##### <a name="required-parameters"></a><span data-ttu-id="ea379-243">Povinné parametry</span><span class="sxs-lookup"><span data-stu-id="ea379-243">Required parameters</span></span>
<span data-ttu-id="ea379-244">**``parent_test_case_id``** Představuje ID nadřazeného testovacího případu.</span><span class="sxs-lookup"><span data-stu-id="ea379-244">**``parent_test_case_id``** Represents the parent test case ID.</span></span>  
<span data-ttu-id="ea379-245">**``test_plan_id``** Představuje ID testovacího plánu.</span><span class="sxs-lookup"><span data-stu-id="ea379-245">**``test_plan_id``** Represents the test plan ID.</span></span>  
<span data-ttu-id="ea379-246">**``test_suite_id``** Představuje ID testovací sady.</span><span class="sxs-lookup"><span data-stu-id="ea379-246">**``test_suite_id``** Represents the test suite ID.</span></span>

##### <a name="examples"></a><span data-ttu-id="ea379-247">Příklad</span><span class="sxs-lookup"><span data-stu-id="ea379-247">Examples</span></span>
``generatederived 123 8901 678``


#### <a name="generatetestonly"></a><span data-ttu-id="ea379-248">generatetestonly</span><span class="sxs-lookup"><span data-stu-id="ea379-248">generatetestonly</span></span>
<span data-ttu-id="ea379-249">Generuje pouze soubor spuštění testu pro zadaný testovací případ v výstupním adresáři.</span><span class="sxs-lookup"><span data-stu-id="ea379-249">Generates only test execution file for the specified test case in the output directory.</span></span> <span data-ttu-id="ea379-250">Pomocí příkazu ``list`` můžete získat všechny dostupné testovací případy.</span><span class="sxs-lookup"><span data-stu-id="ea379-250">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="ea379-251">Jako parametr **test_case_id** použijte libovolnou hodnotu z prvního sloupce.</span><span class="sxs-lookup"><span data-stu-id="ea379-251">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestonly``**``[test_case_id] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="ea379-252">Povinné parametry</span><span class="sxs-lookup"><span data-stu-id="ea379-252">Required parameters</span></span>
<span data-ttu-id="ea379-253">**``test_case_id``** Představuje ID testovacího případu.</span><span class="sxs-lookup"><span data-stu-id="ea379-253">**``test_case_id``** Represents the test case ID.</span></span>  
<span data-ttu-id="ea379-254">**``output_dir``** Představuje výstupní adresář.</span><span class="sxs-lookup"><span data-stu-id="ea379-254">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="ea379-255">Adresář musí existovat.</span><span class="sxs-lookup"><span data-stu-id="ea379-255">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="ea379-256">Příklad</span><span class="sxs-lookup"><span data-stu-id="ea379-256">Examples</span></span>
``generatetestonly 123 c:\temp\rsat``  
``generatetestonly 765 c:\rsat\last``


#### <a name="generatetestsuite"></a><span data-ttu-id="ea379-257">generatetestsuite</span><span class="sxs-lookup"><span data-stu-id="ea379-257">generatetestsuite</span></span>
<span data-ttu-id="ea379-258">Generuje všechny testovací případy pro zadanou sadu ve výstupním adresáři.</span><span class="sxs-lookup"><span data-stu-id="ea379-258">Generates all test cases for the specified suite in the output directory.</span></span>
<span data-ttu-id="ea379-259">Pomocí příkazu ``listtestsuitenames`` můžete získat všechny dostupné testovací sady.</span><span class="sxs-lookup"><span data-stu-id="ea379-259">You can use ``listtestsuitenames`` command to get all available test suits.</span></span> <span data-ttu-id="ea379-260">Jako parametr **test_suite_name** použijte libovolnou hodnotu z prvního sloupce.</span><span class="sxs-lookup"><span data-stu-id="ea379-260">Use any value from the column as a **test_suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``generatetestsuite``**``[test_suite_name] [output_dir]``

##### <a name="required-parameters"></a><span data-ttu-id="ea379-261">Povinné parametry</span><span class="sxs-lookup"><span data-stu-id="ea379-261">Required parameters</span></span>
<span data-ttu-id="ea379-262">**``test_suite_name``** Představuje název testovací sady.</span><span class="sxs-lookup"><span data-stu-id="ea379-262">**``test_suite_name``** Represents the test suite name.</span></span>  
<span data-ttu-id="ea379-263">**``output_dir``** Představuje výstupní adresář.</span><span class="sxs-lookup"><span data-stu-id="ea379-263">**``output_dir``** Represents the output directory.</span></span> <span data-ttu-id="ea379-264">Adresář musí existovat.</span><span class="sxs-lookup"><span data-stu-id="ea379-264">The directory must exist.</span></span>

##### <a name="examples"></a><span data-ttu-id="ea379-265">Příklad</span><span class="sxs-lookup"><span data-stu-id="ea379-265">Examples</span></span>
``generatetestsuite Tests c:\temp\rsat``   
``generatetestsuite Purchase c:\rsat\last``


#### <a name="help"></a><span data-ttu-id="ea379-266">nápověda</span><span class="sxs-lookup"><span data-stu-id="ea379-266">help</span></span>
<span data-ttu-id="ea379-267">Totožný s [?](#section)</span><span class="sxs-lookup"><span data-stu-id="ea379-267">Identical to the [?](#section)</span></span> <span data-ttu-id="ea379-268">příkaz</span><span class="sxs-lookup"><span data-stu-id="ea379-268">command</span></span>


#### <a name="list"></a><span data-ttu-id="ea379-269">seznamu</span><span class="sxs-lookup"><span data-stu-id="ea379-269">list</span></span>
<span data-ttu-id="ea379-270">Obsahuje seznam všech dostupných testovacích případů.</span><span class="sxs-lookup"><span data-stu-id="ea379-270">Lists all available test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``list``**


#### <a name="listtestplans"></a><span data-ttu-id="ea379-271">listtestplans</span><span class="sxs-lookup"><span data-stu-id="ea379-271">listtestplans</span></span>
<span data-ttu-id="ea379-272">Obsahuje seznam všech dostupných testovacích plánů.</span><span class="sxs-lookup"><span data-stu-id="ea379-272">Lists all available test plans.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestplans``**


#### <a name="listtestsuite"></a><span data-ttu-id="ea379-273">listtestsuite</span><span class="sxs-lookup"><span data-stu-id="ea379-273">listtestsuite</span></span>
<span data-ttu-id="ea379-274">Uvádí seznam testovacích případů pro zadanou testovací sadu.</span><span class="sxs-lookup"><span data-stu-id="ea379-274">Lists test cases for the specified test suite.</span></span> <span data-ttu-id="ea379-275">Pomocí příkazu ``listtestsuitenames`` můžete získat všechny dostupné testovací sady.</span><span class="sxs-lookup"><span data-stu-id="ea379-275">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="ea379-276">Jako parametr **suite_name** použijte libovolnou hodnotu z prvního sloupce.</span><span class="sxs-lookup"><span data-stu-id="ea379-276">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuite``**``[suite_name]``

##### <a name="required-parameters"></a><span data-ttu-id="ea379-277">Povinné parametry</span><span class="sxs-lookup"><span data-stu-id="ea379-277">Required parameters</span></span>
<span data-ttu-id="ea379-278">**``suite_name``** Název požadované sady.</span><span class="sxs-lookup"><span data-stu-id="ea379-278">**``suite_name``** Name of the desired suite.</span></span>

##### <a name="examples"></a><span data-ttu-id="ea379-279">Příklad</span><span class="sxs-lookup"><span data-stu-id="ea379-279">Examples</span></span>
``listtestsuite "sample suite name"``  
``listtestsuite NameOfTheSuite``


#### <a name="listtestsuitenames"></a><span data-ttu-id="ea379-280">listtestsuitenames</span><span class="sxs-lookup"><span data-stu-id="ea379-280">listtestsuitenames</span></span>
<span data-ttu-id="ea379-281">Obsahuje seznam všech dostupných testovacích sad.</span><span class="sxs-lookup"><span data-stu-id="ea379-281">Lists all available test suites.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``listtestsuitenames``**


#### <a name="playback"></a><span data-ttu-id="ea379-282">playback</span><span class="sxs-lookup"><span data-stu-id="ea379-282">playback</span></span>
<span data-ttu-id="ea379-283">Přehraje testovací případ pomocí souboru aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="ea379-283">Plays back a test case using an Excel file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playback``**``[excel_file]``

##### <a name="required-parameters"></a><span data-ttu-id="ea379-284">Povinné parametry</span><span class="sxs-lookup"><span data-stu-id="ea379-284">Required parameters</span></span>
<span data-ttu-id="ea379-285">**``excel_file``** Úplná cesta k souboru aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="ea379-285">**``excel_file``** A full path to the Excel file.</span></span> <span data-ttu-id="ea379-286">Soubor musí existovat.</span><span class="sxs-lookup"><span data-stu-id="ea379-286">File must exist.</span></span> 

##### <a name="examples"></a><span data-ttu-id="ea379-287">Příklad</span><span class="sxs-lookup"><span data-stu-id="ea379-287">Examples</span></span>
``
playback c:\RSAT\TestCaseParameters\sample1.xlsx
playback e:\temp\test.xlsx
``


#### <a name="playbackbyid"></a><span data-ttu-id="ea379-288">playbackbyid</span><span class="sxs-lookup"><span data-stu-id="ea379-288">playbackbyid</span></span>
<span data-ttu-id="ea379-289">Přehrává se více testovacích případů najednou.</span><span class="sxs-lookup"><span data-stu-id="ea379-289">Plays back multiple test cases at once.</span></span>
<span data-ttu-id="ea379-290">Pomocí příkazu ``list`` můžete získat všechny dostupné testovací případy.</span><span class="sxs-lookup"><span data-stu-id="ea379-290">You can use the ``list`` command to get all available test cases.</span></span> <span data-ttu-id="ea379-291">Jako parametr **test_case_id** použijte libovolnou hodnotu z prvního sloupce.</span><span class="sxs-lookup"><span data-stu-id="ea379-291">Use any value from the first column as a **test_case_id** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackbyid``**``[test_case_id1] [test_case_id2] ... [test_case_idN]``

##### <a name="required-parameters"></a><span data-ttu-id="ea379-292">Povinné parametry</span><span class="sxs-lookup"><span data-stu-id="ea379-292">Required parameters</span></span>
<span data-ttu-id="ea379-293">**``test_case_id1``** ID existujícího testovacího případu.</span><span class="sxs-lookup"><span data-stu-id="ea379-293">**``test_case_id1``** ID of exisiting test case.</span></span>  
<span data-ttu-id="ea379-294">**``test_case_id2``** ID existujícího testovacího případu.</span><span class="sxs-lookup"><span data-stu-id="ea379-294">**``test_case_id2``** ID of exisiting test case.</span></span>  
<span data-ttu-id="ea379-295">**``test_case_idN``** ID existujícího testovacího případu.</span><span class="sxs-lookup"><span data-stu-id="ea379-295">**``test_case_idN``** ID of exisiting test case.</span></span>  

##### <a name="examples"></a><span data-ttu-id="ea379-296">Příklad</span><span class="sxs-lookup"><span data-stu-id="ea379-296">Examples</span></span>
``playbackbyid 878``  
``playbackbyid 2345 667 135``


#### <a name="playbackmany"></a><span data-ttu-id="ea379-297">playbackmany</span><span class="sxs-lookup"><span data-stu-id="ea379-297">playbackmany</span></span>
<span data-ttu-id="ea379-298">Přehraje řadu testovacích případů najednou pomocí souborů aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="ea379-298">Plays back many test cases at once, using Excel files.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbackmany``**``[excel_file1] [excel_file2] ... [excel_fileN]``

##### <a name="required-parameters"></a><span data-ttu-id="ea379-299">Povinné parametry</span><span class="sxs-lookup"><span data-stu-id="ea379-299">Required parameters</span></span>
<span data-ttu-id="ea379-300">**``excel_file1``** Úplná cesta k souboru aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="ea379-300">**``excel_file1``** Full path to the Excel file.</span></span> <span data-ttu-id="ea379-301">Soubor musí existovat.</span><span class="sxs-lookup"><span data-stu-id="ea379-301">File must exist.</span></span>  
<span data-ttu-id="ea379-302">**``excel_file2``** Úplná cesta k souboru aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="ea379-302">**``excel_file2``** Full path to the Excel file.</span></span> <span data-ttu-id="ea379-303">Soubor musí existovat.</span><span class="sxs-lookup"><span data-stu-id="ea379-303">File must exist.</span></span>  
<span data-ttu-id="ea379-304">**``excel_fileN``** Úplná cesta k souboru aplikace Excel.</span><span class="sxs-lookup"><span data-stu-id="ea379-304">**``excel_fileN``** Full path to the Excel file.</span></span> <span data-ttu-id="ea379-305">Soubor musí existovat.</span><span class="sxs-lookup"><span data-stu-id="ea379-305">File must exist.</span></span>  

##### <a name="examples"></a><span data-ttu-id="ea379-306">Příklad</span><span class="sxs-lookup"><span data-stu-id="ea379-306">Examples</span></span>
``playbackmany c:\RSAT\TestCaseParameters\param1.xlsx``  
``playbackmany e:\temp\test.xlsx f:\rsat\sample1.xlsx c:\RSAT\sample2.xlsx``


#### <a name="playbacksuite"></a><span data-ttu-id="ea379-307">playbacksuite</span><span class="sxs-lookup"><span data-stu-id="ea379-307">playbacksuite</span></span>
<span data-ttu-id="ea379-308">Přehraje všechny testovací případy ze zadané sady testů.</span><span class="sxs-lookup"><span data-stu-id="ea379-308">Plays back all test cases from the specified test suite.</span></span> <span data-ttu-id="ea379-309">Pomocí příkazu ``listtestsuitenames`` můžete získat všechny dostupné testovací sady.</span><span class="sxs-lookup"><span data-stu-id="ea379-309">You can use ``listtestsuitenames`` command to get all available test suites.</span></span> <span data-ttu-id="ea379-310">Jako parametr **suite_name** použijte libovolnou hodnotu z prvního sloupce.</span><span class="sxs-lookup"><span data-stu-id="ea379-310">Use any value from first column as **suite_name** parameter.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``playbacksuite``**``[suite_name]``

##### <a name="required-parameters"></a><span data-ttu-id="ea379-311">Povinné parametry</span><span class="sxs-lookup"><span data-stu-id="ea379-311">Required parameters</span></span>
<span data-ttu-id="ea379-312">**``suite_name``** Název požadované sady.</span><span class="sxs-lookup"><span data-stu-id="ea379-312">**``suite_name``** Name of the desired suite.</span></span>

##### <a name="examples"></a><span data-ttu-id="ea379-313">Příklad</span><span class="sxs-lookup"><span data-stu-id="ea379-313">Examples</span></span>
``playbacksuite suiteName``  
``playbacksuite sample_suite``


#### <a name="quit"></a><span data-ttu-id="ea379-314">opustit</span><span class="sxs-lookup"><span data-stu-id="ea379-314">quit</span></span>
<span data-ttu-id="ea379-315">Zavře aplikaci.</span><span class="sxs-lookup"><span data-stu-id="ea379-315">Closes the  application.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``quit``**


#### <a name="upload"></a><span data-ttu-id="ea379-316">upload</span><span class="sxs-lookup"><span data-stu-id="ea379-316">upload</span></span>
<span data-ttu-id="ea379-317">Odešle všechny soubory náležející do zadané sady testů nebo testovacích případů.</span><span class="sxs-lookup"><span data-stu-id="ea379-317">Uploads all files belonging to the specified test suite or test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``upload``**``[suite_name] [testcase_id]``

#### <a name="required-parameters"></a><span data-ttu-id="ea379-318">Povinné parametry</span><span class="sxs-lookup"><span data-stu-id="ea379-318">Required parameters</span></span>
<span data-ttu-id="ea379-319">**``suite_name``** Odešle všechny soubory náležející do zadané testovací sady.</span><span class="sxs-lookup"><span data-stu-id="ea379-319">**``suite_name``** All files belonging to the specified test suite will be uploaded.</span></span>
<span data-ttu-id="ea379-320">**``testcase_id``** Odešle všechny soubory náležející do zadaných testovacích případů.</span><span class="sxs-lookup"><span data-stu-id="ea379-320">**``testcase_id``** All files beloning to the specified test case(s) will be uploaded.</span></span>

##### <a name="examples"></a><span data-ttu-id="ea379-321">Příklad</span><span class="sxs-lookup"><span data-stu-id="ea379-321">Examples</span></span>
``upload sample_suite``  
``upload 123``  
``upload 123 456``


#### <a name="uploadrecording"></a><span data-ttu-id="ea379-322">uploadrecording</span><span class="sxs-lookup"><span data-stu-id="ea379-322">uploadrecording</span></span>
<span data-ttu-id="ea379-323">Odešle pouze soubor nahrávky, který náleží do zadaných testovacích případů.</span><span class="sxs-lookup"><span data-stu-id="ea379-323">Uploads only recording file belonging to the specified test cases.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``uploadrecording``**``[testcase_id]``

##### <a name="required-parameters"></a><span data-ttu-id="ea379-324">Povinné parametry</span><span class="sxs-lookup"><span data-stu-id="ea379-324">Required parameters</span></span>
<span data-ttu-id="ea379-325">**``testcase_id``** Odešle soubor nahrávky, který náleží do zadaných testovacích případů.</span><span class="sxs-lookup"><span data-stu-id="ea379-325">**``testcase_id``** Recording file belonging to the specified test cases will be uploaded.</span></span>

##### <a name="examples"></a><span data-ttu-id="ea379-326">Příklad</span><span class="sxs-lookup"><span data-stu-id="ea379-326">Examples</span></span>
``uploadrecording 123``  
``uploadrecording 123 456``


#### <a name="usage"></a><span data-ttu-id="ea379-327">použití</span><span class="sxs-lookup"><span data-stu-id="ea379-327">usage</span></span>
<span data-ttu-id="ea379-328">Zobrazení dvou způsobů vyvolání této aplikace: jeden s použitím souboru výchozího nastavení, další poskytuje soubor nastavení.</span><span class="sxs-lookup"><span data-stu-id="ea379-328">Shows two ways to invoke this application: one using a default setting file, another one providing a setting file.</span></span>

``Microsoft.Dynamics.RegressionSuite.ConsoleApp``**``usage``**


### <a name="windows-powershell-examples"></a><span data-ttu-id="ea379-329">Příklad Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="ea379-329">Windows PowerShell examples</span></span>

[!IMPORTANT] <span data-ttu-id="ea379-330">Níže uvedené ukázkové skripty jsou poskytovány pro ilustrační účely a nejsou podporovány společností Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ea379-330">The example scripts below are provided AS IS for illustration purposes and are not supported by Microsoft.</span></span>

#### <a name="run-a-test-case-in-a-loop"></a><span data-ttu-id="ea379-331">Spuštění testovacího případu ve smyčce</span><span class="sxs-lookup"><span data-stu-id="ea379-331">Run a test case in a loop</span></span>

<span data-ttu-id="ea379-332">Máte testovací skript, který vytvoří nového odběratele.</span><span class="sxs-lookup"><span data-stu-id="ea379-332">You have a test script that creates a new customer.</span></span> <span data-ttu-id="ea379-333">Pomocí skriptování lze tento testovací případ spustit ve smyčce tak, že před spuštěním každé iterace náhodně použijete následující data:</span><span class="sxs-lookup"><span data-stu-id="ea379-333">Via scripting, this test case can be run in a loop by randomizing the following data before each iteration is run:</span></span>

- <span data-ttu-id="ea379-334">ID odběratele</span><span class="sxs-lookup"><span data-stu-id="ea379-334">Customer ID</span></span>
- <span data-ttu-id="ea379-335">Jméno zákazníka</span><span class="sxs-lookup"><span data-stu-id="ea379-335">Customer name</span></span>
- <span data-ttu-id="ea379-336">Adresa odběratele</span><span class="sxs-lookup"><span data-stu-id="ea379-336">Customer address</span></span>

<span data-ttu-id="ea379-337">ID zákazníka bude mít formát *ATCUS\<number\>*, kde \<number\> je hodnota mezi **000000001** a **999999999**.</span><span class="sxs-lookup"><span data-stu-id="ea379-337">The customer ID will be in the format *ATCUS\<number\>*, where \<number\> is a value between **000000001** and **999999999**.</span></span>

<span data-ttu-id="ea379-338">V následujícím příkladu je použit jeden parametr **start** pro definování prvního použitého čísla.</span><span class="sxs-lookup"><span data-stu-id="ea379-338">The following example uses one parameter, **start**, to define the first number that is used.</span></span> <span data-ttu-id="ea379-339">Aplikace používá k definování počtu odběratelů, které je nutné vytvořit, druhý parametr **nr**.</span><span class="sxs-lookup"><span data-stu-id="ea379-339">Is uses a second parameter, **nr**, to define the number of customers that must be created.</span></span> <span data-ttu-id="ea379-340">Parametry v souboru parametrů aplikace Excel jsou pro každou iteraci změněny pomocí funkce UpdateCustomer.</span><span class="sxs-lookup"><span data-stu-id="ea379-340">For each iteration, the parameters in the Excel parameter file are changed by using an UpdateCustomer function.</span></span> <span data-ttu-id="ea379-341">Poté bude příkazový řádek RSAT volán ve funkci RunTestCase.</span><span class="sxs-lookup"><span data-stu-id="ea379-341">Then the RSAT command line is called in a RunTestCase function.</span></span>

<span data-ttu-id="ea379-342">Otevřete Microsoft Windows PowerShell Integrated Scripting Environment (ISE) v režimu správy a vložte následující kód do okna s názvem **Untitled1. ps1.**</span><span class="sxs-lookup"><span data-stu-id="ea379-342">Open Microsoft Windows PowerShell Integrated Scripting Environment (ISE) in admin mode, and paste the following code into the window that is named **Untitled1.ps1**.</span></span>

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
$excelFilename = "full path to Excel parameter file"
l$sheetName = "DirPartyQuickCreateForm"
for ($i = $start; $i -lt $start + $nr; $i++ )
{
    $CustomerId = $i.ToString("000000000")
    Write-Host "customer : " $CustomerId
    UpdateCustomer $excelFilename $sheetName $CustomerId
    RunTestCase $excelFilename
```

#### <a name="run-a-script-that-depends-on-data-in-microsoft-dynamics-365"></a><span data-ttu-id="ea379-343">Spuštění skriptu, který závisí na datech v Microsoft Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="ea379-343">Run a script that depends on data in Microsoft Dynamics 365</span></span>

<span data-ttu-id="ea379-344">V následujícím příkladu je pomocí volání OData (Open Data Protocol) nalezen stav nákupní objednávky.</span><span class="sxs-lookup"><span data-stu-id="ea379-344">The following example uses an Open Data Protocol (OData) call to find the order status of a purchase order.</span></span> <span data-ttu-id="ea379-345">Pokud není stav **fakturován**, můžete například volat testovací případ RSAT, který zaúčtuje fakturu.</span><span class="sxs-lookup"><span data-stu-id="ea379-345">If the status isn't **invoiced**, you can, for example, call an RSAT test case that posts the invoice.</span></span>

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
