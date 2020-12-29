---
title: Automatizace testování s elektronickým výkaznictvím
description: V tomto tématu je vysvětleno, jak můžete pomocí funkce směrného plánu elektronického výkaznictví (ER) automatizovat testování některých funkcí.
author: NickSelin
manager: AnnBe
ms.date: 07/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERFormatBaselineTable, ERFormatMappingRunLogTable, ERParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.openlocfilehash: 0a2586afd56eef0f953454ad246ff3647a5b09d1
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681441"
---
# <a name="automate-testing-with-electronic-reporting"></a><span data-ttu-id="ac81c-103">Automatizace testování s elektronickým výkaznictvím</span><span class="sxs-lookup"><span data-stu-id="ac81c-103">Automate testing with Electronic reporting</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ac81c-104">V tomto tématu je vysvětleno, jak můžete pomocí systému elektronického výkaznictví (ER) automatizovat testování některých funkcí.</span><span class="sxs-lookup"><span data-stu-id="ac81c-104">This topic explains how you can use the Electronic reporting (ER) framework to automate testing of some functionality.</span></span> <span data-ttu-id="ac81c-105">Příklad v tomto tématu ukazuje, jak automatizovat testování zpracování platby dodavatele.</span><span class="sxs-lookup"><span data-stu-id="ac81c-105">The example in this topic shows how to automate the testing of vendor payment processing.</span></span>

<span data-ttu-id="ac81c-106">Aplikace používá systém ER ke generování platebních souborů a odpovídajících dokumentů během zpracování plateb dodavatele.</span><span class="sxs-lookup"><span data-stu-id="ac81c-106">The application uses the ER framework to generate payment files and corresponding documents during vendor payment processing.</span></span> <span data-ttu-id="ac81c-107">Systém ER se skládá z datového modelu, mapování modelu a formátovacích součástí, které podporují zpracování plateb pro různé typy plateb a generování dokumentů v různých formátech.</span><span class="sxs-lookup"><span data-stu-id="ac81c-107">The ER framework consists of a data model, model mappings, and format components that support payment processing for different payment types and the generation of documents in different formats.</span></span> <span data-ttu-id="ac81c-108">Tyto komponenty lze stáhnout ze služby Microsoft Dynamics Lifecycle Services (LCS) a importovat do instance.</span><span class="sxs-lookup"><span data-stu-id="ac81c-108">These components can be downloaded from Microsoft Dynamics Lifecycle Services (LCS) and imported into the instance.</span></span>

<span data-ttu-id="ac81c-109">Můžete také upravit každou komponentu Microsoft a použít ji jako základ pro vlastní komponentu.</span><span class="sxs-lookup"><span data-stu-id="ac81c-109">You also can customize each Microsoft component and use it as the basis of your own custom component.</span></span> <span data-ttu-id="ac81c-110">Vytvořením vlastní verze můžete provést změny, které podporují konkrétní požadavky.</span><span class="sxs-lookup"><span data-stu-id="ac81c-110">By creating a custom version, you can make changes that support specific requirements.</span></span> <span data-ttu-id="ac81c-111">Můžete například upravit datový model ER a mapování modelu ER pro přístup k datům aplikací specifickým pro odběratele, nebo můžete změnit formát ER pro úpravu rozvržení vygenerovaného dokumentu.</span><span class="sxs-lookup"><span data-stu-id="ac81c-111">For example, you can adjust the ER data model and ER model mapping to access customer-specific application data, or you can change an ER format to modify the layout of a generated document.</span></span>

<span data-ttu-id="ac81c-112">Můžete použít vlastní formáty ER pro zpracování souborů plateb, které generují platby dodavatelů, a také ke zpracování kontrolních sestav.</span><span class="sxs-lookup"><span data-stu-id="ac81c-112">You can use customized ER formats to process payment files that generate vendor payments and also to process control reports.</span></span> <span data-ttu-id="ac81c-113">V komponentách ER je podporováno vytváření verzí.</span><span class="sxs-lookup"><span data-stu-id="ac81c-113">Versioning is supported in ER components.</span></span> <span data-ttu-id="ac81c-114">Z tohoto důvodu může společnost Microsoft poskytnout aktualizované verze řešení ER pro zpracování plateb dodavatele a automaticky sloučit aktualizovanou verzi s přizpůsobenou komponentou tím, že ji znovu vytvoří.</span><span class="sxs-lookup"><span data-stu-id="ac81c-114">Therefore, Microsoft can provide updated versions of ER solutions for vendor payment processing, and you can automatically merge the updated version with your customized component by rebasing it.</span></span> <span data-ttu-id="ac81c-115">Je však nutné otestovat znovu vytvořenou verzi, abyste se ujistili, že funguje očekávaným způsobem.</span><span class="sxs-lookup"><span data-stu-id="ac81c-115">However, you must test the rebased version to make sure that it works as you expect.</span></span>

<span data-ttu-id="ac81c-116">Datové modely ER a mapování modelů ER jsou společné pro mnoho formátů ER, které se používají ke zpracování plateb různých typů a ke generování platebních dokumentů pro konkrétní zemi nebo oblast.</span><span class="sxs-lookup"><span data-stu-id="ac81c-116">ER data models and ER model mappings are common for many ER formats that are used to process payments of different types and to generate country/region-specific payment documents.</span></span> <span data-ttu-id="ac81c-117">Proto je důrazně doporučeno automatizovat přijímání uživatelů a testování integrace, takže je automaticky prováděno ve více společnostech, ale bere v úvahu kontext země/oblasti pro každou cílovou společnost za použití různých datových sad, atd.</span><span class="sxs-lookup"><span data-stu-id="ac81c-117">Therefore, it's highly desirable to automate user acceptance and integration testing so that it's automatically done in multiple companies but considers the country/region context of each target company, uses different datasets, and so on.</span></span>

<span data-ttu-id="ac81c-118">Další informace o tom, jak vytvořit vlastní verzi formátu, která je založena na formátu přijatém od poskytovatele konfigurace, naleznete v tématu [ER Upgrade formátu přijetím nové základní verze tohoto formátu](./tasks/er-upgrade-format.md).</span><span class="sxs-lookup"><span data-stu-id="ac81c-118">For more information about how to create a custom version of a format that is based on the format that you received from a configuration provider, see [ER Upgrade your format by adopting a new, base version of that format](./tasks/er-upgrade-format.md).</span></span>

## <a name="key-concepts"></a><span data-ttu-id="ac81c-119">Klíčové koncepty</span><span class="sxs-lookup"><span data-stu-id="ac81c-119">Key concepts</span></span>

<span data-ttu-id="ac81c-120">Funkční členové skupiny Power Users mohou vytvářet přijímání uživatelů a testování integrace bez nutnosti vytvářet zdrojový kód.</span><span class="sxs-lookup"><span data-stu-id="ac81c-120">Functional power users can author user acceptance and integration testing without having to write source code.</span></span>

- <span data-ttu-id="ac81c-121">Pomocí funkce směrného plánu ER můžete porovnat generované dokumenty s hlavními kopiemi.</span><span class="sxs-lookup"><span data-stu-id="ac81c-121">Use the ER baseline feature to compare generated documents to master copies.</span></span> <span data-ttu-id="ac81c-122">Více informací získáte v tématu [Sledování výsledků vygenerovaných sestav a jejich porovnání s hodnotami směrného plánu](er-trace-reports-compare-baseline.md).</span><span class="sxs-lookup"><span data-stu-id="ac81c-122">For more information, see [Trace generated report results and compare them with baseline values](er-trace-reports-compare-baseline.md).</span></span>
- <span data-ttu-id="ac81c-123">Pomocí záznamníku úloh můžete zaznamenávat testovací případy a zahrnovat hodnocení směrného plánu.</span><span class="sxs-lookup"><span data-stu-id="ac81c-123">Use Task recorder to record test cases, and include baseline assessment.</span></span> <span data-ttu-id="ac81c-124">Více informací viz [Zdroje záznamníku úloh](../user-interface/task-recorder.md).</span><span class="sxs-lookup"><span data-stu-id="ac81c-124">For more information, see [Task recorder resources](../user-interface/task-recorder.md).</span></span>
- <span data-ttu-id="ac81c-125">Seskupte testovací případy pro požadované scénáře testování.</span><span class="sxs-lookup"><span data-stu-id="ac81c-125">Group test cases for required test scenarios.</span></span> <span data-ttu-id="ac81c-126">Další informace naleznete v tématu [Vytvoření a automatizace testů](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md).</span><span class="sxs-lookup"><span data-stu-id="ac81c-126">For more information, see [Create and automate user acceptance tests](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md).</span></span>

    - <span data-ttu-id="ac81c-127">K vytvoření knihoven pro testy přijetí uživatelů použijte modelování podnikových procesů v LCS.</span><span class="sxs-lookup"><span data-stu-id="ac81c-127">Use Business process modeler (BPM) in LCS to make libraries for user acceptance tests.</span></span>
    - <span data-ttu-id="ac81c-128">Pomocí testovacích knihoven BPM vytvořte testovací plán a testovací sady ve službě Microsoft Azure DevOps Services (Azure DevOps).</span><span class="sxs-lookup"><span data-stu-id="ac81c-128">Use BPM test libraries to create a test plan and test suites in Microsoft Azure DevOps Services (Azure DevOps).</span></span>

<span data-ttu-id="ac81c-129">Funkční členové skupiny Power Users mohou spustit testy přijetí a integrace s uživatelem.</span><span class="sxs-lookup"><span data-stu-id="ac81c-129">Functional power users can run user acceptance and integration tests.</span></span>

- <span data-ttu-id="ac81c-130">Pomocí nástroje RSAT (Regression Suite Automation Tool) spusťte testovací případy požadované sady testů.</span><span class="sxs-lookup"><span data-stu-id="ac81c-130">Use Regression suite automation tool (RSAT) to run test cases of the desired test suite.</span></span>
- <span data-ttu-id="ac81c-131">Oznamte výsledky testování do aplikace Azure DevOps a pomocí této služby prozkoumejte tyto výsledky.</span><span class="sxs-lookup"><span data-stu-id="ac81c-131">Report the results of the testing to Azure DevOps, and use this service to investigate those results.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ac81c-132">Předpoklady</span><span class="sxs-lookup"><span data-stu-id="ac81c-132">Prerequisites</span></span>

<span data-ttu-id="ac81c-133">Před provedením úkolů v tomto tématu je třeba splnit následující předpoklady:</span><span class="sxs-lookup"><span data-stu-id="ac81c-133">Before you can complete the tasks in this topic, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="ac81c-134">Nasaďte topologii, která podporuje automatizaci testování.</span><span class="sxs-lookup"><span data-stu-id="ac81c-134">Deploy a topology that supports test automation.</span></span> <span data-ttu-id="ac81c-135">Musíte mít přístup do instance této topologie pro roli **Správce systému**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-135">You must have access to the instance of this topology for the **System administrator** role.</span></span> <span data-ttu-id="ac81c-136">Tato topologie musí obsahovat ukázková data, která budou použita v tomto příkladu.</span><span class="sxs-lookup"><span data-stu-id="ac81c-136">This topology must contain the demo data that will be used in this example.</span></span> <span data-ttu-id="ac81c-137">Další informace naleznete v tématu [Nasazení a použití prostředí, které podporuje automatizaci průběžného sestavení a testů](../perf-test/continuous-build-test-automation.md).</span><span class="sxs-lookup"><span data-stu-id="ac81c-137">For more information, see [Deploy and use an environment that supports continuous build and test automation](../perf-test/continuous-build-test-automation.md).</span></span>
- <span data-ttu-id="ac81c-138">Chcete-li automaticky spustit testy přijetí a integrace s uživatelem, je nutné nainstalovat RSAT do používané topologie a odpovídajícím způsobem ji nakonfigurovat.</span><span class="sxs-lookup"><span data-stu-id="ac81c-138">To run user acceptance and integration tests automatically, you must install RSAT in the topology that you're using and configure it in the appropriate manner.</span></span> <span data-ttu-id="ac81c-139">Informace o tom, jak instalovat a konfigurovat RSAT a jak je nakonfigurovat pro práci s aplikacemi Finance and Operations a Azure DevOps získáte v tématu [Regression Suite Automation Tool](https://www.microsoft.com/download/details.aspx?id=57357).</span><span class="sxs-lookup"><span data-stu-id="ac81c-139">For information about how to install and configure RSAT and configure it to work with Finance and Operations apps and Azure DevOps, see [Regression Suite Automation Tool](https://www.microsoft.com/download/details.aspx?id=57357).</span></span> <span data-ttu-id="ac81c-140">Věnujte pozornost předpokladům pro používání nástroje.</span><span class="sxs-lookup"><span data-stu-id="ac81c-140">Pay attention to the prerequisites for using the tool.</span></span> <span data-ttu-id="ac81c-141">Následující obrázek znázorňuje příklad nastavení RSAT.</span><span class="sxs-lookup"><span data-stu-id="ac81c-141">The following illustration shows an example of the RSAT settings.</span></span> <span data-ttu-id="ac81c-142">Modrý obdélník ohraničuje parametry, které určují přístup do Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="ac81c-142">The blue rectangle encloses the parameters that specify access to Azure DevOps.</span></span> <span data-ttu-id="ac81c-143">Zelený obdélník označuje parametry, které určují přístup k instanci.</span><span class="sxs-lookup"><span data-stu-id="ac81c-143">The green rectangle encloses the parameters that specify access to the instance.</span></span>

    <span data-ttu-id="ac81c-144">![Nastavení RSAT](media/GER-Configure.png "Snímek obrazovky dialogového okna Nastavení RSAT")</span><span class="sxs-lookup"><span data-stu-id="ac81c-144">![RSAT settings](media/GER-Configure.png "Screenshot of the RSAT Settings dialog box")</span></span>

- <span data-ttu-id="ac81c-145">K uspořádání testovacích případů v sadách za účelem zajištění správného pořadí provádění, aby bylo možné shromáždit protokoly provádění testů pro další hlášení a vyšetřování, musíte mít přístup Azure DevOps z nasazené topologie.</span><span class="sxs-lookup"><span data-stu-id="ac81c-145">To organize test cases in suites to help guarantee the correct execution sequence, so that you can collect logs of test executions for further reporting and investigation, you must have access to Azure DevOps from the deployed topology.</span></span>
- <span data-ttu-id="ac81c-146">Chcete-li dokončit příklad v tomto tématu, doporučujeme vám stáhnout [použití ER pro testy RSAT](https://go.microsoft.com/fwlink/?linkid=874684)</span><span class="sxs-lookup"><span data-stu-id="ac81c-146">To complete the example in this topic, we recommend that you download [ER usage for RSAT tests](https://go.microsoft.com/fwlink/?linkid=874684).</span></span> <span data-ttu-id="ac81c-147">Tento soubor zip obsahuje následující průvodce úkoly:</span><span class="sxs-lookup"><span data-stu-id="ac81c-147">This zip file contains the following task guides:</span></span>

    | <span data-ttu-id="ac81c-148">Obsah</span><span class="sxs-lookup"><span data-stu-id="ac81c-148">Content</span></span>                                           | <span data-ttu-id="ac81c-149">Název a umístění souboru</span><span class="sxs-lookup"><span data-stu-id="ac81c-149">File name and location</span></span> |
    |---------------------------------------------------|------------------------|
    | <span data-ttu-id="ac81c-150">Ukázkový záznam úloh pro přípravu dat k testování</span><span class="sxs-lookup"><span data-stu-id="ac81c-150">Sample task recording to prepare data for testing</span></span> | <span data-ttu-id="ac81c-151">Příprava\\záznam XML</span><span class="sxs-lookup"><span data-stu-id="ac81c-151">Prepare\\Recording.xml</span></span> |
    | <span data-ttu-id="ac81c-152">Ukázkový záznam úlohy zpracování platby dodavatele</span><span class="sxs-lookup"><span data-stu-id="ac81c-152">Sample task recording to process vendor payment</span></span>   | <span data-ttu-id="ac81c-153">Proces\\Recording.xml</span><span class="sxs-lookup"><span data-stu-id="ac81c-153">Process\\Recording.xml</span></span> |

## <a name="prepare-the-accounts-payable-module-to-process-vendor-payments"></a><span data-ttu-id="ac81c-154">Příprava modulu Závazky pro zpracování plateb dodavatele</span><span class="sxs-lookup"><span data-stu-id="ac81c-154">Prepare the Accounts payable module to process vendor payments</span></span>

1. <span data-ttu-id="ac81c-155">Přihlaste se k instanci.</span><span class="sxs-lookup"><span data-stu-id="ac81c-155">Sign in to your instance.</span></span>
2. <span data-ttu-id="ac81c-156">Stáhněte si následující konfigurace elektronického výkaznictví z úložiště LCS.</span><span class="sxs-lookup"><span data-stu-id="ac81c-156">Download the following ER configurations from LCS.</span></span> <span data-ttu-id="ac81c-157">Pokyny viz [Import konfigurace ze služby Lifecycle Services pro elektronické výkaznictví](./tasks/er-import-configuration-lifecycle-services.md).</span><span class="sxs-lookup"><span data-stu-id="ac81c-157">For instructions, see [ER Import a configuration from Lifecycle Services](./tasks/er-import-configuration-lifecycle-services.md).</span></span>

    - <span data-ttu-id="ac81c-158">**Model platby** Konfogurace modelu ER</span><span class="sxs-lookup"><span data-stu-id="ac81c-158">**Payment model** ER model configuration</span></span>
    - <span data-ttu-id="ac81c-159">**Mapování modelu platby 1611** Konfigurace mapování modelu ER</span><span class="sxs-lookup"><span data-stu-id="ac81c-159">**Payment model mapping 1611** ER model mapping configuration</span></span>
    - <span data-ttu-id="ac81c-160">**BACS (UK)** Konfigurace formátu ER</span><span class="sxs-lookup"><span data-stu-id="ac81c-160">**BACS (UK)** ER format configuration</span></span>

    <span data-ttu-id="ac81c-161">![Konfigurace elektronického výkaznictví](media/GER-Configurations.png "Snímek obrazovky stránky se směrným plánem v elektronickém výkaznictví")</span><span class="sxs-lookup"><span data-stu-id="ac81c-161">![Electronic reporting configurations](media/GER-Configurations.png "Screenshot of the Configurations page in Electronic reporting")</span></span>

3. <span data-ttu-id="ac81c-162">Vyberte ukázkovou datovou společnost **GBSI**, která má kontext země/oblasti ve Velké Británii.</span><span class="sxs-lookup"><span data-stu-id="ac81c-162">Select the **GBSI** demo data company, which has a country/region context in Great Britain.</span></span>
4. <span data-ttu-id="ac81c-163">Konfigurace parametrů závazků:</span><span class="sxs-lookup"><span data-stu-id="ac81c-163">Configure Accounts payable parameters:</span></span>

    1. <span data-ttu-id="ac81c-164">Přejděte do nabídky **Závazky \> Nastavení \> Metody platby**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-164">Go to **Accounts payable \> Payment setup \> Methods of payment**.</span></span>
    2. <span data-ttu-id="ac81c-165">Vyberte **Elektronický** způsob platby.</span><span class="sxs-lookup"><span data-stu-id="ac81c-165">Select the **Electronic** method of payment.</span></span>
    3. <span data-ttu-id="ac81c-166">Konfigurovat vybranou metodu platby tak, aby používala dříve stažený formát ER systému **BACS (UK)** ke zpracování plateb dodavatele:</span><span class="sxs-lookup"><span data-stu-id="ac81c-166">Configure the selected method of payment so that it uses the **BACS (UK)** ER format that you downloaded earlier for vendor payment processing:</span></span>

        1. <span data-ttu-id="ac81c-167">Na pevné záložce **Formáty souboru** nastavte volbu **Obecný formát elektronického exportu** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-167">On the **File formats** FastTab, set the **Generic electronic Export format** option to **Yes**.</span></span>
        2. <span data-ttu-id="ac81c-168">V poli **Exportovat konfiguraci formátu** vyberte **BACS (UK)**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-168">In the **Export format configuration** field, select **BACS (UK)**.</span></span>

    <span data-ttu-id="ac81c-169">![Stránka Metody platby](media/GER-APParameters.png "Snímek obrazovky stránky platebních metod")</span><span class="sxs-lookup"><span data-stu-id="ac81c-169">![Methods of payment page](media/GER-APParameters.png "Screenshot of the Methods of payment page")</span></span>

    > [!NOTE]
    > <span data-ttu-id="ac81c-170">Pokud používáte odvozenou verzi tohoto formátu ER, která byla vytvořena pro podporu vlastního nastavení, můžete tuto konfiguraci vybrat v **elektronické** metodě platby.</span><span class="sxs-lookup"><span data-stu-id="ac81c-170">If you have the derived version of this ER format that was created to support customizations, you can select this configuration in the **Electronic** method of payment.</span></span>

5. <span data-ttu-id="ac81c-171">Vytvoření ukázkové platby dodavatele:</span><span class="sxs-lookup"><span data-stu-id="ac81c-171">Create an example vendor payment:</span></span>

    1. <span data-ttu-id="ac81c-172">Přejděte na **Závazky \> Platby \> Deník plateb**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-172">Go to **Accounts payable \> Payments \> Payment journal**.</span></span>
    2. <span data-ttu-id="ac81c-173">Ujistěte se, že jste deník plateb nezaúčtovali.</span><span class="sxs-lookup"><span data-stu-id="ac81c-173">Make sure that you haven't posted the payment journal.</span></span>

        <span data-ttu-id="ac81c-174">![Stránka Deník plateb](media/GER-APJournal.png "Snímek obrazovky stránky deníku platby")</span><span class="sxs-lookup"><span data-stu-id="ac81c-174">![Payment journal page](media/GER-APJournal.png "Screenshot of the Payment journal page")</span></span>

    3. <span data-ttu-id="ac81c-175">Vyberte **Řádky** a zadejte řádek, který obsahuje následující informace.</span><span class="sxs-lookup"><span data-stu-id="ac81c-175">Select **Lines**, and enter a line that has the following information.</span></span>

        | <span data-ttu-id="ac81c-176">Pole</span><span class="sxs-lookup"><span data-stu-id="ac81c-176">Field</span></span>               | <span data-ttu-id="ac81c-177">Ukázková hodnota</span><span class="sxs-lookup"><span data-stu-id="ac81c-177">Example value</span></span>   |
        |---------------------|-----------------|
        | <span data-ttu-id="ac81c-178">Název dodavatele</span><span class="sxs-lookup"><span data-stu-id="ac81c-178">Vendor name</span></span>         | <span data-ttu-id="ac81c-179">GB\_SI\_000001</span><span class="sxs-lookup"><span data-stu-id="ac81c-179">GB\_SI\_000001</span></span>  |
        | <span data-ttu-id="ac81c-180">Má Dáti</span><span class="sxs-lookup"><span data-stu-id="ac81c-180">Debit</span></span>               | <span data-ttu-id="ac81c-181">1,000.00</span><span class="sxs-lookup"><span data-stu-id="ac81c-181">1,000.00</span></span>        |
        | <span data-ttu-id="ac81c-182">Měna</span><span class="sxs-lookup"><span data-stu-id="ac81c-182">Currency</span></span>            | <span data-ttu-id="ac81c-183">GBP</span><span class="sxs-lookup"><span data-stu-id="ac81c-183">GBP</span></span>             |
        | <span data-ttu-id="ac81c-184">Typ protiúčtu</span><span class="sxs-lookup"><span data-stu-id="ac81c-184">Offset account type</span></span> | <span data-ttu-id="ac81c-185">Banka</span><span class="sxs-lookup"><span data-stu-id="ac81c-185">Bank</span></span>            |
        | <span data-ttu-id="ac81c-186">Protiúčet</span><span class="sxs-lookup"><span data-stu-id="ac81c-186">Offset account</span></span>      | <span data-ttu-id="ac81c-187">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="ac81c-187">GBSI OPER</span></span>       |
        | <span data-ttu-id="ac81c-188">Metoda platby</span><span class="sxs-lookup"><span data-stu-id="ac81c-188">Method of payment</span></span>   | <span data-ttu-id="ac81c-189">Elektronicky</span><span class="sxs-lookup"><span data-stu-id="ac81c-189">Electronic</span></span>      |

    <span data-ttu-id="ac81c-190">![Stránka Platby dodavatelů](media/GER-APJournalLines.png "Snímek obrazovky stránky Platby dodavatele")</span><span class="sxs-lookup"><span data-stu-id="ac81c-190">![Vendor payments page](media/GER-APJournalLines.png "Screenshot of the Vendor payments page")</span></span>

## <a name="prepare-the-er-framework-to-test-vendor-payment-processing"></a><span data-ttu-id="ac81c-191">Příprava architektury ER pro testování zpracování plateb dodavatele</span><span class="sxs-lookup"><span data-stu-id="ac81c-191">Prepare the ER framework to test vendor payment processing</span></span>

### <a name="configure-er-parameters"></a><span data-ttu-id="ac81c-192">Konfigurace parametrů ER</span><span class="sxs-lookup"><span data-stu-id="ac81c-192">Configure ER parameters</span></span>

1. <span data-ttu-id="ac81c-193">Přejděte do nabídky **Správa organizace \> Elektronické výkaznictví \> Parametry elektronického výkaznictví**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-193">Go to **Organization administration \> Electronic reporting \> Electronic reporting parameters**.</span></span>
2. <span data-ttu-id="ac81c-194">Na kartě **přílohy** vyberte v poli **směrný plán** možnost **soubor** jako typ dokumentu, který používá systém správy dokumentů (DM) pro uchovávání dokumentů souvisejících se základní funkcí jako přílohy DM.</span><span class="sxs-lookup"><span data-stu-id="ac81c-194">On the **Attachments** tab, in the **Baseline** field, select **File** as the document type that the Document management (DM) framework uses to keep documents that are related to the baseline feature as DM attachments.</span></span>

    <span data-ttu-id="ac81c-195">![Stránka parametrů elektronického výkaznictví](media/GER-ERParameters.png "Snímek obrazovky stránky Parametry elektronického výkaznictví")</span><span class="sxs-lookup"><span data-stu-id="ac81c-195">![Electronic reporting parameters page](media/GER-ERParameters.png "Screenshot of the Electronic reporting parameters page")</span></span>

### <a name="generate-baseline-copies-of-vendor-paymentrelated-documents"></a><span data-ttu-id="ac81c-196">Generování kopií směrného plánu pro dokumenty související s platbami dodavatele</span><span class="sxs-lookup"><span data-stu-id="ac81c-196">Generate baseline copies of vendor payment–related documents</span></span>

1. <span data-ttu-id="ac81c-197">Přejděte na **Závazky \> Platby \> Deník plateb**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-197">Go to **Accounts payable \> Payments \> Payment journal**.</span></span>
2. <span data-ttu-id="ac81c-198">Vybrat **řádky**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-198">Select **Lines**.</span></span>
3. <span data-ttu-id="ac81c-199">Vyberte **Generovat platby**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-199">Select **Generate payments**.</span></span>
4. <span data-ttu-id="ac81c-200">Vyberte **Elektronický** způsob platby.</span><span class="sxs-lookup"><span data-stu-id="ac81c-200">Select the **Electronic** method of payment.</span></span>
5. <span data-ttu-id="ac81c-201">Vyberte bankovní účet **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-201">Select the **GBSI OPER** bank account.</span></span>
6. <span data-ttu-id="ac81c-202">Nastavte možnost **Vytisknout kontrolní sestavu** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-202">Set the **Print control report** option to **Yes**.</span></span>
7. <span data-ttu-id="ac81c-203">Stáhněte vygenerovaný výstup jako soubor zip.</span><span class="sxs-lookup"><span data-stu-id="ac81c-203">Download the generated output as a zip file.</span></span>
8. <span data-ttu-id="ac81c-204">Otevřete stažený soubor.</span><span class="sxs-lookup"><span data-stu-id="ac81c-204">Open the downloaded file.</span></span>
9. <span data-ttu-id="ac81c-205">Extrahujte následující soubory ze staženého souboru:</span><span class="sxs-lookup"><span data-stu-id="ac81c-205">Extract following files from the downloaded file:</span></span>

    - <span data-ttu-id="ac81c-206">**Soubor** soubor platby v textovém formátu</span><span class="sxs-lookup"><span data-stu-id="ac81c-206">**File** payment file in text format</span></span>
    - <span data-ttu-id="ac81c-207">Soubor kontrolní sestavy **ERVendOutPaymControlReport** ve formátu XLSX</span><span class="sxs-lookup"><span data-stu-id="ac81c-207">**ERVendOutPaymControlReport** control report file in XLSX format</span></span>

    <span data-ttu-id="ac81c-208">![Extrahované soubory](media/GER-APJournalProcessed.png "Snímek obrazovky názvů extrahovaných souborů v Průzkumníkovi Windows")</span><span class="sxs-lookup"><span data-stu-id="ac81c-208">![Extracted files](media/GER-APJournalProcessed.png "Screenshot of extracted file names in Windows explorer")</span></span>

### <a name="turn-on-the-er-baseline-feature"></a><span data-ttu-id="ac81c-209">Zapnutí funkce směrného plánu ER</span><span class="sxs-lookup"><span data-stu-id="ac81c-209">Turn on the ER baseline feature</span></span>

1. <span data-ttu-id="ac81c-210">Přejděte do části **Správa organizace \> Elektronické výkaznictví \> Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-210">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="ac81c-211">V podokně akcí na kartě **Konfigurace** zvolte **Parametry uživatele**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-211">On the Action Pane, on the **Configurations** tab, select **User parameters**.</span></span>
3. <span data-ttu-id="ac81c-212">Nastavte možnost **Spustit v režimu ladění** na **Ano**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-212">Set the **Run in debug mode** option to **Yes**.</span></span>

<span data-ttu-id="ac81c-213">Zapnutím parametru **spustit v režimu ladění** vynutíte, aby architektura ER prováděla následující akce po spuštění libovolného formátu ER generujícího odchozí dokumenty:</span><span class="sxs-lookup"><span data-stu-id="ac81c-213">By turning on the **Run in debug mode** parameter, you force the ER framework to perform the following actions after the execution of any ER format that generates outgoing documents:</span></span>

1. <span data-ttu-id="ac81c-214">Určuje, zda byl směrný plán konfigurován pro některou ze součástí provedeného formátu ER.</span><span class="sxs-lookup"><span data-stu-id="ac81c-214">Determine whether a baseline was configured for any of components of the executed ER format.</span></span>
2. <span data-ttu-id="ac81c-215">Určete, zda se každý nakonfigurovaný směrný plán použije za aktuálních podmínek (kód společnosti pro přihlášenou společnost, název souboru a příponu názvu souboru generovaného výstupu atd.).</span><span class="sxs-lookup"><span data-stu-id="ac81c-215">Determine whether each configured baseline is applicable in the current conditions (company code of the signed-in company, file name and file name extension of the generated output, and so on).</span></span>
3. <span data-ttu-id="ac81c-216">Pro každý použitelný směrný plán proveďte následující akce:</span><span class="sxs-lookup"><span data-stu-id="ac81c-216">For each applicable baseline, perform the following actions:</span></span>

    1. <span data-ttu-id="ac81c-217">Porovnejte výstup, který je generován při provádění formátu ER, s odpovídajícím směrným plánem.</span><span class="sxs-lookup"><span data-stu-id="ac81c-217">Compare the output that is generated during execution of the ER format with the corresponding baseline.</span></span>
    2. <span data-ttu-id="ac81c-218">Výsledky porovnání uložte do protokolu ladění konfigurací ER.</span><span class="sxs-lookup"><span data-stu-id="ac81c-218">Store the results of the comparison in the ER configurations debug log.</span></span>

### <a name="configure-er-baselines-for-vendor-payment-processing"></a><span data-ttu-id="ac81c-219">Konfigurace směrných plánů ER pro zpracování plateb dodavatele</span><span class="sxs-lookup"><span data-stu-id="ac81c-219">Configure ER baselines for vendor payment processing</span></span>

1. <span data-ttu-id="ac81c-220">Přejděte do části **Správa organizace \> Elektronické výkaznictví \> Konfigurace**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-220">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="ac81c-221">Vyberte **Směrné plány**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-221">Select **Baselines**.</span></span>
3. <span data-ttu-id="ac81c-222">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-222">Select **New**.</span></span>
4. <span data-ttu-id="ac81c-223">V poli **Reference** vyberte formát **BACS (UK)**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-223">In the **Reference** field, select the **BACS (UK)** format.</span></span>
5. <span data-ttu-id="ac81c-224">Vyberte **Přílohy**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-224">Select **Attachments**.</span></span>
6. <span data-ttu-id="ac81c-225">Přidání nového směrného plánu souboru platby dodavatele:</span><span class="sxs-lookup"><span data-stu-id="ac81c-225">Add a new baseline for the vendor payment file:</span></span>

    1. <span data-ttu-id="ac81c-226">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-226">Select **New**.</span></span>
    2. <span data-ttu-id="ac81c-227">V poli **Typ** vyberte **Soubor** Typ dokumentu DM, který jste nakonfigurovali v parametrech ER za účelem uložení artefaktů směrného plánu.</span><span class="sxs-lookup"><span data-stu-id="ac81c-227">In the **Type** field, select the **File** DM document type that you configured in the ER parameters to store baseline artifacts.</span></span>
    3. <span data-ttu-id="ac81c-228">Přejděte k výběru místně uloženého **souboru** platby souboru v textovém formátu.</span><span class="sxs-lookup"><span data-stu-id="ac81c-228">Browse to select the locally saved **File** payment file in text format.</span></span>
    4. <span data-ttu-id="ac81c-229">Do pole **Popis** zadejte **Soubor TXT platby**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-229">In the **Description** field, enter **Payment TXT file**.</span></span>

7. <span data-ttu-id="ac81c-230">Přidání nového směrného plánu pro sestavu řízení platby dodavatele:</span><span class="sxs-lookup"><span data-stu-id="ac81c-230">Add a new baseline for the control report for the vendor payment:</span></span>

    1. <span data-ttu-id="ac81c-231">Zvolte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-231">Select **New**.</span></span>
    2. <span data-ttu-id="ac81c-232">V poli **Typ** vyberte **Soubor** Typ dokumentu DM, který jste nakonfigurovali v parametrech ER za účelem uložení artefaktů směrného plánu.</span><span class="sxs-lookup"><span data-stu-id="ac81c-232">In the **Type** field, select the **File** DM document type that you configured in the ER parameters to store baseline artifacts.</span></span>
    3. <span data-ttu-id="ac81c-233">Přejděte k výběru místně uloženého kontrolního souboru sestavy **ERVendOutPaymControlReport** ve formátu XLSX.</span><span class="sxs-lookup"><span data-stu-id="ac81c-233">Browse to select the locally saved **ERVendOutPaymControlReport** control report file in XLSX format.</span></span>
    4. <span data-ttu-id="ac81c-234">Do pole **Popis** zadejte **Kontrolní sestava XLS platby**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-234">In the **Description** field, enter **Payment XLSX control report**.</span></span>

    <span data-ttu-id="ac81c-235">![Směrné plány pro soubor a řídicí sestavu platby dodavatele](media/GER-BaselineAttachments.png "Snímek obrazovky se stránkou konfigurace s vybranou sestavou platebního modulu XLSX")</span><span class="sxs-lookup"><span data-stu-id="ac81c-235">![Baselines for the vendor payment file and control report](media/GER-BaselineAttachments.png "Screenshot of the Configurations page with the Payment XLSX control report selected")</span></span>

8. <span data-ttu-id="ac81c-236">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ac81c-236">Close the page.</span></span>
9. <span data-ttu-id="ac81c-237">Na pevné záložce **Směrné plány** vyberte **Nový** ke konfiguraci směrného plánu pro soubor platby:</span><span class="sxs-lookup"><span data-stu-id="ac81c-237">On the **Baselines** FastTab, select **New** to configure a baseline for the payment file:</span></span>

    1. <span data-ttu-id="ac81c-238">Pojmenujte **Nastavení směrného plánu pro soubor platby**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-238">Name the line **Baseline setting for payment file**.</span></span>
    2. <span data-ttu-id="ac81c-239">V poli **název součásti souboru** vyberte možnost **soubor**, chcete-li použít tento směrný plán ve formátu výstupu ER, který generuje soubor platby v textovém formátu souboru BACS (UK).</span><span class="sxs-lookup"><span data-stu-id="ac81c-239">In the **File component name** field, select **file** to apply this baseline to the ER format output that generates the payment file in BACS (UK) text format.</span></span>
    3. <span data-ttu-id="ac81c-240">V poli **Společnosti** vyberte **GBSI**, chcete-li použít tento základní směrný plán při spuštění formátu ER **BACS (UK)** ve společnosti GBSI.</span><span class="sxs-lookup"><span data-stu-id="ac81c-240">In the **Companies** field, select **GBSI** to apply this baseline when the **BACS (UK)** ER format is run in the GBSI company.</span></span>
    4. <span data-ttu-id="ac81c-241">V poli **Maska názvu souboru** zadejte **\*.TXT** pro použití tohoto směrného plánu pouze pro výstupy formátu **souboru** s příponou **.txt**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-241">In **File name mask** field, enter **\*.TXT** to apply this baseline only to outputs of the **file** format component that have the **.txt** file name extension.</span></span>
    5. <span data-ttu-id="ac81c-242">V poli **směrný plán** vyberte **soubor txt platby**, aby se tento směrný plán používal pro porovnání s generovaným výstupem.</span><span class="sxs-lookup"><span data-stu-id="ac81c-242">In the **Baseline** field, select **Payment TXT file** so that this baseline is used for comparison with the generated output.</span></span>

10. <span data-ttu-id="ac81c-243">Vyberte **Nový** a nakonfigurujte směrný plán pro sestavu ovládacího prvku:</span><span class="sxs-lookup"><span data-stu-id="ac81c-243">Select **New** to configure a baseline for the control report:</span></span>

    1. <span data-ttu-id="ac81c-244">Pojmenujte řádek **Nastavení směrného plánu pro kontrolní sestavu**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-244">Name the line **Baseline setting for control report**.</span></span>
    2. <span data-ttu-id="ac81c-245">V poli **Název součásti souboru** vyberte možnost **ERVendOutPaymControlReport**, chcete-li použít tento směrný plán ve formátu výstupu ER, který generuje kontrolní sestavu.</span><span class="sxs-lookup"><span data-stu-id="ac81c-245">In the **File component name** field, select **ERVendOutPaymControlReport** to apply this baseline to the ER format output that generates the control report.</span></span>
    3. <span data-ttu-id="ac81c-246">V poli **Společnosti** vyberte **GBSI**, chcete-li použít tento základní směrný plán při spuštění formátu ER **BACS (UK)** ve společnosti GBSI.</span><span class="sxs-lookup"><span data-stu-id="ac81c-246">In the **Companies** field, select **GBSI** to apply this baseline when the **BACS (UK)** ER format is run in the GBSI company.</span></span>
    4. <span data-ttu-id="ac81c-247">V poli **Maska názvu souboru** zadejte **\*.XLSX** pro použití tohoto směrného plánu pouze pro výstupy formátu **ERVendOutPaymControlReport** s příponou **.xslx**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-247">In **File name mask** field, enter **\*.XLSX** to apply this baseline only to outputs of the **ERVendOutPaymControlReport** format component that have the **.xslx** file name extension.</span></span>
    5. <span data-ttu-id="ac81c-248">V poli **směrný plán** vyberte **kontrolní sestava XLS platby**, aby se tento směrný plán používal pro porovnání s generovaným výstupem.</span><span class="sxs-lookup"><span data-stu-id="ac81c-248">In the **Baseline** field, select **Payment XLSX control report** so that this baseline is used for comparison with the generated output.</span></span>

    <span data-ttu-id="ac81c-249">![Pevná záložka Směrné plány na stránce Konfigurace](media/GER-BaselineRules.png "Snímek obrazovky pevné záložky Směrné plány na stránce Konfigurace")</span><span class="sxs-lookup"><span data-stu-id="ac81c-249">![Baselines FastTab on the Configurations page](media/GER-BaselineRules.png "Screenshot of the Baselines FastTab on the Configurations page")</span></span>

## <a name="record-tests-to-validate-vendor-payment-processing"></a><span data-ttu-id="ac81c-250">Záznam testů pro ověření zpracování plateb dodavatele</span><span class="sxs-lookup"><span data-stu-id="ac81c-250">Record tests to validate vendor payment processing</span></span>

<span data-ttu-id="ac81c-251">Jako funkční uživatel Power User můžete zaznamenat vlastní kroky a otestovat tak zpracování plateb dodavatelů.</span><span class="sxs-lookup"><span data-stu-id="ac81c-251">As a functional power user, you can record your own steps to test vendor payment processing.</span></span> <span data-ttu-id="ac81c-252">Doporučujeme vám přehrát (a podle potřeby upravit) záznam úloh **Prepare\\Recording.xml**, který jste stáhli dříve.</span><span class="sxs-lookup"><span data-stu-id="ac81c-252">We recommend that you play (and edit, as required) the **Prepare\\Recording.xml** task recording that you downloaded earlier.</span></span> <span data-ttu-id="ac81c-253">Tento záznam slouží k nastavení všech testovacích dat do správného stavu.</span><span class="sxs-lookup"><span data-stu-id="ac81c-253">This recording is used to set all testing data to the correct state.</span></span> <span data-ttu-id="ac81c-254">Tento krok je vyžadován, protože testování může být provedeno mnohokrát a každý test musí používat data, která jsou ve stejném stavu.</span><span class="sxs-lookup"><span data-stu-id="ac81c-254">That step is required because the testing can be done many times, and every test must use data that is in the same state.</span></span>

### <a name="reset-user-settings"></a><span data-ttu-id="ac81c-255">Obnovit nastavení uživatele</span><span class="sxs-lookup"><span data-stu-id="ac81c-255">Reset user settings</span></span>

1. <span data-ttu-id="ac81c-256">Otevřete výchozí řídicí panel.</span><span class="sxs-lookup"><span data-stu-id="ac81c-256">Open the default dashboard.</span></span>
2. <span data-ttu-id="ac81c-257">Vyberte tlačítko **Nastavení** (symbol ozubeného kola).</span><span class="sxs-lookup"><span data-stu-id="ac81c-257">Select the **Settings** button (the gear symbol).</span></span>
3. <span data-ttu-id="ac81c-258">Vyberte **Možnosti uživatele**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-258">Select **User options**.</span></span>
4. <span data-ttu-id="ac81c-259">Vyberte **Údaje o využití**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-259">Select **Usage data**.</span></span>
5. <span data-ttu-id="ac81c-260">Vyberte **Obnovit**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-260">Select **Reset**.</span></span>
6. <span data-ttu-id="ac81c-261">Vyberte **Ano** pro potvrzení, že chcete resetovat údaje o použití.</span><span class="sxs-lookup"><span data-stu-id="ac81c-261">Select **Yes** to confirm that you want to reset usage data.</span></span>
7. <span data-ttu-id="ac81c-262">Zavřete stránku.</span><span class="sxs-lookup"><span data-stu-id="ac81c-262">Close the page.</span></span>

### <a name="record-the-steps-to-prepare-data-for-testing"></a><span data-ttu-id="ac81c-263">Záznam kroků pro přípravu dat pro testování</span><span class="sxs-lookup"><span data-stu-id="ac81c-263">Record the steps to prepare data for testing</span></span>

1. <span data-ttu-id="ac81c-264">Vyberte tlačítko **Nastavení** (symbol ozubeného kola).</span><span class="sxs-lookup"><span data-stu-id="ac81c-264">Select the **Settings** button (the gear symbol).</span></span>
2. <span data-ttu-id="ac81c-265">Vyberte **Záznamník úloh**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-265">Select **Task recorder**.</span></span>
3. <span data-ttu-id="ac81c-266">Vyberte **Záznam přehrávání**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-266">Select **Playback recording**.</span></span>
4. <span data-ttu-id="ac81c-267">Vyberte **Otevřít z tohoto počítače**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-267">Select **Open from this PC**.</span></span>
5. <span data-ttu-id="ac81c-268">Vyberte **Procházet** a vyberte místně uložený soubor **Prepare\\Recording.xml**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-268">Select **Browse**, and select the locally save **Prepare\\Recording.xml** file.</span></span>
6. <span data-ttu-id="ac81c-269">Vyberte **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-269">Select **Start**.</span></span>
7. <span data-ttu-id="ac81c-270">Vybírejte možnost **Přehrát další čekající krok**, dokud se nepřehrají všechny kroky v nahrávce.</span><span class="sxs-lookup"><span data-stu-id="ac81c-270">Keep selecting **Play next pending step** until all the steps in the recording have been played.</span></span>

<span data-ttu-id="ac81c-271">Tento záznam úloh provádí následující akce:</span><span class="sxs-lookup"><span data-stu-id="ac81c-271">This task recording performs the following actions:</span></span>

1. <span data-ttu-id="ac81c-272">Nastavte stav zpracovaného řádku platby na hodnotu **Žádný**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-272">Set the status of the processed payment line to **None**.</span></span>

    <span data-ttu-id="ac81c-273">![Záznam úkolu kroky 3 až 4](media/GER-Recording1Review1.png "Snímek obrazovky záznamu úkolu kroky 3 až 4")</span><span class="sxs-lookup"><span data-stu-id="ac81c-273">![Task recording steps 3 through 4](media/GER-Recording1Review1.png "Screenshot of task recording steps 3 through 4")</span></span>

2. <span data-ttu-id="ac81c-274">Zapněte parametr uživatele ER **Spustit v režimu ladění**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-274">Turn on the **Run in debug mode** ER user parameter.</span></span>

    <span data-ttu-id="ac81c-275">![Záznam úkolu kroky 9 až 10](media/GER-Recording1Review2.png "Snímek obrazovky záznamu úkolu kroky 9 až 10")</span><span class="sxs-lookup"><span data-stu-id="ac81c-275">![Task recording steps 9 through 10](media/GER-Recording1Review2.png "Screenshot of task recording steps 9 through 10")</span></span>

3. <span data-ttu-id="ac81c-276">Vyčistěte protokol ladění ER, který obsahuje výsledky porovnání vygenerovaných souborů do směrných plánů.</span><span class="sxs-lookup"><span data-stu-id="ac81c-276">Clean up the ER debug log that contains the results of the comparison of generated files to baselines.</span></span>

    <span data-ttu-id="ac81c-277">![Záznam úkolu kroky 13 až 15](media/GER-Recording1Review3.png "Snímek obrazovky záznamu úkolu kroky 13 až 15")</span><span class="sxs-lookup"><span data-stu-id="ac81c-277">![Task recording steps 13 through 15](media/GER-Recording1Review3.png "Screenshot of task recording steps 13 through 15")</span></span>

### <a name="record-the-steps-to-test-vendor-payment-processing"></a><span data-ttu-id="ac81c-278">Zaznamenejte kroky k testování zpracování plateb dodavatele</span><span class="sxs-lookup"><span data-stu-id="ac81c-278">Record the steps to test vendor payment processing</span></span>

<span data-ttu-id="ac81c-279">Doporučujeme vám přehrát (a podle potřeby upravit) záznam úloh **Process\\Recording.xml**, který jste stáhli dříve.</span><span class="sxs-lookup"><span data-stu-id="ac81c-279">We recommend that you play (and edit, as required) the **Process\\Recording.xml** task recording that you downloaded earlier.</span></span> <span data-ttu-id="ac81c-280">Tento záznam se používá ke zpracování plateb dodavateli a k ověření výsledků porovnání vygenerovaných dokumentů s odpovídajícími směrnými plány.</span><span class="sxs-lookup"><span data-stu-id="ac81c-280">This recording is used to process vendor payments and validate the results of the comparison of generated documents to corresponding baselines.</span></span>

1. <span data-ttu-id="ac81c-281">Vyberte tlačítko **Nastavení** (symbol ozubeného kola).</span><span class="sxs-lookup"><span data-stu-id="ac81c-281">Select the **Settings** button (the gear symbol).</span></span>
2. <span data-ttu-id="ac81c-282">Vyberte **Záznamník úloh**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-282">Select **Task recorder**.</span></span>
3. <span data-ttu-id="ac81c-283">Vyberte **Záznam přehrávání**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-283">Select **Playback recording**.</span></span>
4. <span data-ttu-id="ac81c-284">Vyberte **Otevřít z tohoto počítače**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-284">Select **Open from this PC**.</span></span>
5. <span data-ttu-id="ac81c-285">Vyberte **Procházet** a vyberte místně uložený soubor **Process\\Recording.xml**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-285">Select **Browse**, and select the locally saved **Process\\Recording.xml** file.</span></span>
6. <span data-ttu-id="ac81c-286">Vyberte **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-286">Select **Start**.</span></span>
7. <span data-ttu-id="ac81c-287">Vybírejte možnost **Přehrát další čekající krok**, dokud se nepřehrají všechny kroky v nahrávce.</span><span class="sxs-lookup"><span data-stu-id="ac81c-287">Keep selecting **Play next pending step** until all the steps in the recording have been played.</span></span>

<span data-ttu-id="ac81c-288">Tento záznam úloh provádí následující akce:</span><span class="sxs-lookup"><span data-stu-id="ac81c-288">This task recording performs the following actions:</span></span>

1. <span data-ttu-id="ac81c-289">Spusťte zpracování platby dodavateli.</span><span class="sxs-lookup"><span data-stu-id="ac81c-289">Start vendor payment processing.</span></span>
2. <span data-ttu-id="ac81c-290">Vyberte správné parametry modulu runtime a zapněte generování kontrolní sestavy.</span><span class="sxs-lookup"><span data-stu-id="ac81c-290">Select the correct runtime parameters, and turn on generation of a control report.</span></span>

    <span data-ttu-id="ac81c-291">![Záznam úkolu kroky 3 až 8](media/GER-Recording2Review1.png "Snímek obrazovky záznamu úkolu kroky 3 až 8")</span><span class="sxs-lookup"><span data-stu-id="ac81c-291">![Task recording steps 3 through 8](media/GER-Recording2Review1.png "Screenshot of task recording steps 3 through 8")</span></span>

3. <span data-ttu-id="ac81c-292">Přejděte k protokolu ladění ER pro zaznamenání výsledků porovnání vygenerovaných výstupů do odpovídajících směrných plánů.</span><span class="sxs-lookup"><span data-stu-id="ac81c-292">Access the ER debug log to record the results of the comparison of generated outputs to corresponding baselines.</span></span>

    <span data-ttu-id="ac81c-293">V protokolu ladění ER se výsledky porovnání zobrazí v poli **Generovaný text**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-293">In the ER debug log, the results of the comparison appear in the **Generated text** field.</span></span> <span data-ttu-id="ac81c-294">Pole **Komponenta formátu** a **Cesta formátu, která způsobila záznam do protokolu**, odkazují na komponentu souboru, pro kterou byl vygenerovaný výstup porovnán se směrným plánem.</span><span class="sxs-lookup"><span data-stu-id="ac81c-294">The **Format component** and **Format path that caused a log entry** fields refer to the file component for which the generated output has been compared to the baseline.</span></span>

    <span data-ttu-id="ac81c-295">![Položky na stránce Protokoly spuštění elektronického výkaznictví](media/GER-ERDebugLog.png "Snímek položek na stránce Protokoly spuštění Parametry elektronického výkaznictví")</span><span class="sxs-lookup"><span data-stu-id="ac81c-295">![Entries on the Electronic reporting run logs page](media/GER-ERDebugLog.png "Screenshot of entries on the Electronic reporting run logs page")</span></span>

4. <span data-ttu-id="ac81c-296">Porovnání aktuálního výstupu se směrným plánem je zaznamenáno pomocí možnosti **Ověřit** záznamník úloh a výběrem možnosti **Aktuální hodnota**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-296">The comparison of the current output to the baseline is recorded by using the **Validate** Task recorder option and selecting  **Current Value**.</span></span>

    <span data-ttu-id="ac81c-297">![Použití možnosti ověření pro porovnání s aktuální hodnotou](media/GER-TRRecordValidation.png "Snímek obrazovky použití možnosti ověření pro porovnání s aktuální hodnotou")</span><span class="sxs-lookup"><span data-stu-id="ac81c-297">![Using the Validate option for comparison with the current value](media/GER-TRRecordValidation.png "Screenshot of using the Validate option for comparison with the current value")</span></span>

    <span data-ttu-id="ac81c-298">Následující obrázek ukazuje, jak vypadají zaznamenané kroky ověření v záznamu úloh.</span><span class="sxs-lookup"><span data-stu-id="ac81c-298">The following illustration shows what the recorded validation steps look like in the task recording.</span></span>

    <span data-ttu-id="ac81c-299">![Záznam úkolu kroky 13 a 15](media/GER-Recording2Review2.png "Snímek obrazovky záznamu úkolu kroky 13 a 15")</span><span class="sxs-lookup"><span data-stu-id="ac81c-299">![Task recording steps 13 and 15](media/GER-Recording2Review2.png "Screenshot of task recording steps 13 and 15")</span></span>

## <a name="add-the-recorded-tests-to-azure-devops"></a><span data-ttu-id="ac81c-300">Přidání zaznamenaných testů do Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="ac81c-300">Add the recorded tests to Azure DevOps</span></span>

1. <span data-ttu-id="ac81c-301">Otevřete prostředí Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="ac81c-301">Open the Azure DevOps environment.</span></span>
2. <span data-ttu-id="ac81c-302">Vyberte projekt, který jste definovali v parametrech RSAT, [při konfiguraci nástroje](#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="ac81c-302">Select the project that you defined in the RSAT parameters when you [configured the tool](#prerequisites).</span></span>
3. <span data-ttu-id="ac81c-303">Vyberte zkušební plán, který jste definovali v parametrech RSAT, [při konfiguraci nástroje](#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="ac81c-303">Select the test plan that you defined in the RSAT parameters when you [configured the tool](#prerequisites).</span></span>
4. <span data-ttu-id="ac81c-304">Vytvořit nový testovací případ pro vybraný zkušební plán:</span><span class="sxs-lookup"><span data-stu-id="ac81c-304">Create a new test case for the selected test plan:</span></span>

    1. <span data-ttu-id="ac81c-305">Pojmenujte testovací případ **Příprava dat pro testování elektronické platby dodavatele**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-305">Name the test case **Prepare data to test processing of vendor's electronic payment**.</span></span>
    2. <span data-ttu-id="ac81c-306">Připojte soubor **Record. XML** ze složky **Připravit**, kterou jste stáhli dříve.</span><span class="sxs-lookup"><span data-stu-id="ac81c-306">Attach the **Recording.xml** file from the **Prepare** folder that you downloaded earlier.</span></span>

5. <span data-ttu-id="ac81c-307">Vytvořit nový testovací případ pro vybraný zkušební plán:</span><span class="sxs-lookup"><span data-stu-id="ac81c-307">Create a new test case for the selected test plan:</span></span>

    1. <span data-ttu-id="ac81c-308">Pojmenujte testovací případ **Zkušební zpracování plateb dodavatelů pomocí formátu systému BACS (UK)**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-308">Name the test case **Test processing of vendor payments by using ER format BACS (UK)**.</span></span>
    2. <span data-ttu-id="ac81c-309">Připojte soubor **Record. XML** ze složky **Proces**, kterou jste stáhli dříve.</span><span class="sxs-lookup"><span data-stu-id="ac81c-309">Attach the **Recording.xml** file from the **Process** folder that you downloaded earlier.</span></span>

    <span data-ttu-id="ac81c-310">![Nové testovací případy pro vybraný zkušební plán](media/GER-RSAT-DevOps-Tests-Passed.png "Snímek obrazovky Nové testovací případy pro vybraný zkušební plán")</span><span class="sxs-lookup"><span data-stu-id="ac81c-310">![New test cases for the selected test plan](media/GER-RSAT-DevOps-Tests-Passed.png "Screenshot of the new test cases for the selected test plan")</span></span>

> [!NOTE]
> <span data-ttu-id="ac81c-311">Věnujte pozornost správnému pořadí provedení přidaných testů.</span><span class="sxs-lookup"><span data-stu-id="ac81c-311">Pay attention to the correct execution order of the tests that are added.</span></span>

## <a name="prepare-rsat-to-run-the-recorded-tests"></a><span data-ttu-id="ac81c-312">Příprava RSAT pro spuštění zaznamenaných testů</span><span class="sxs-lookup"><span data-stu-id="ac81c-312">Prepare RSAT to run the recorded tests</span></span>

### <a name="load-the-tests-from-azure-devops-to-rsat"></a><span data-ttu-id="ac81c-313">Nahrání testů z Azure DevOps do RSAT</span><span class="sxs-lookup"><span data-stu-id="ac81c-313">Load the tests from Azure DevOps to RSAT</span></span>

1. <span data-ttu-id="ac81c-314">Otevřete v aktuální topologii místní aplikaci RSAT.</span><span class="sxs-lookup"><span data-stu-id="ac81c-314">Open the local RSAT application in the current topology.</span></span>
2. <span data-ttu-id="ac81c-315">Vyberte možnost **Load** k načtení testů, které se aktuálně nacházejí v aplikaci Azure DevOps, do RSAT.</span><span class="sxs-lookup"><span data-stu-id="ac81c-315">Select **Load** to load the tests that currently reside in Azure DevOps into RSAT.</span></span>

    <span data-ttu-id="ac81c-316">![Testy načtené na RSAT](media/GER-RSAT-RSAT-Tests-Loaded.png "Snímek obrazovky testů načtených na RSAT")</span><span class="sxs-lookup"><span data-stu-id="ac81c-316">![Tests loaded into RSAT](media/GER-RSAT-RSAT-Tests-Loaded.png "Screenshot of the tests loaded into RSAT")</span></span>

### <a name="create-automation-and-parameters-files"></a><span data-ttu-id="ac81c-317">Vytvoření souborů automatizace a parametrů</span><span class="sxs-lookup"><span data-stu-id="ac81c-317">Create automation and parameters files</span></span>

1. <span data-ttu-id="ac81c-318">V RSAT vyberte testy, které jste načetli z Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="ac81c-318">In RSAT, select the tests that you loaded from Azure DevOps.</span></span>
2. <span data-ttu-id="ac81c-319">Vyberte **Nový** k vytvoření souborů automatizace a parametrů RSAT.</span><span class="sxs-lookup"><span data-stu-id="ac81c-319">Select **New** to create RSAT automation and parameters files.</span></span>

    <span data-ttu-id="ac81c-320">![Automatizace RSAT a soubory parametrů vytvořené v RSAT](media/GER-RSAT-RSAT-Tests-Initiated.png "Snímek obrazovky Automatizace RSAT a soubory parametrů vytvořené v RSAT")</span><span class="sxs-lookup"><span data-stu-id="ac81c-320">![RSAT automation and parameters files created in RSAT](media/GER-RSAT-RSAT-Tests-Initiated.png "Screenshot of the RSAT automation and parameters files created in RSAT")</span></span>

### <a name="modify-the-parameters-files"></a><span data-ttu-id="ac81c-321">Změna souborů parametrů</span><span class="sxs-lookup"><span data-stu-id="ac81c-321">Modify the parameters files</span></span>

1. <span data-ttu-id="ac81c-322">V RSAT vyberte testovací případ **Příprava dat pro testování elektronické platby dodavatele**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-322">In RSAT, select the **Prepare data to test processing of vendor's electronic payment** test case.</span></span>
2. <span data-ttu-id="ac81c-323">Vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-323">Select **Edit**.</span></span>
3. <span data-ttu-id="ac81c-324">V sešitu Microsoft Excel, který je otevřen, změňte v listu **obecné** kód společnosti na **GBSI**, protože tato společnost bude použita k provedení testu.</span><span class="sxs-lookup"><span data-stu-id="ac81c-324">In the Microsoft Excel workbook that is opened, on the **General** worksheet, change the company code to **GBSI**, because this company will be used for test execution.</span></span>
4. <span data-ttu-id="ac81c-325">V RSAT vyberte testovací případ **Zkušební zpracování plateb dodavatelů pomocí formátu systému BACS (UK)**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-325">In RSAT, select the **Test processing of vendor payments by using ER format BACS (UK)** test case.</span></span>
5. <span data-ttu-id="ac81c-326">Vyberte možnost **Upravit**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-326">Select **Edit**.</span></span>
6. <span data-ttu-id="ac81c-327">V sešitu aplikace Excel, který je otevřen, změňte na listu **Obecné** kód společnosti na **GBSI.**</span><span class="sxs-lookup"><span data-stu-id="ac81c-327">In the Excel workbook that is opened, on the **General** worksheet, change the company code to **GBSI**.</span></span>
7. <span data-ttu-id="ac81c-328">V listu **ERFormatMappingRunLogTable** si povšimněte, že buňky A:3 a C:3 obsahují text polí v tabulce protokolu ladění ER, která slouží k ověření výsledků porovnání výstupu se směrným plánem.</span><span class="sxs-lookup"><span data-stu-id="ac81c-328">On the **ERFormatMappingRunLogTable** worksheet, notice that cells A:3 and C:3 contain the text of the fields in the ER debug log table that are used to validate the results of the comparison of the output to the baseline.</span></span> <span data-ttu-id="ac81c-329">Tyto texty budou použity k vyhodnocení záznamů protokolů ladění ER, které jsou vytvářeny při provádění testu.</span><span class="sxs-lookup"><span data-stu-id="ac81c-329">These texts will be used to evaluate ER debug log records that are created during test execution.</span></span>

    <span data-ttu-id="ac81c-330">![List ERFormatMappingRunLogTable](media/GER-RSAT-RSAT-ExcelParameters.png "Snímek obrazovky listu ERFormatMappingRunLogTable")</span><span class="sxs-lookup"><span data-stu-id="ac81c-330">![ERFormatMappingRunLogTable worksheet](media/GER-RSAT-RSAT-ExcelParameters.png "Screenshot of the ERFormatMappingRunLogTable worksheet")</span></span>

## <a name="run-the-tests-and-analyze-the-results"></a><span data-ttu-id="ac81c-331">Spuštění testů a analýza výsledků</span><span class="sxs-lookup"><span data-stu-id="ac81c-331">Run the tests and analyze the results</span></span>

### <a name="run-the-tests-in-rsat"></a><span data-ttu-id="ac81c-332">Spuštění testů v RSAT</span><span class="sxs-lookup"><span data-stu-id="ac81c-332">Run the tests in RSAT</span></span>

1. <span data-ttu-id="ac81c-333">V RSAT vyberte načtené testy.</span><span class="sxs-lookup"><span data-stu-id="ac81c-333">In RSAT, select the loaded tests.</span></span>
2. <span data-ttu-id="ac81c-334">Vyberte **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-334">Select **Run**.</span></span>

<span data-ttu-id="ac81c-335">Všimněte si, že testovací případy jsou automaticky spuštěny v aplikaci pomocí webového prohlížeče.</span><span class="sxs-lookup"><span data-stu-id="ac81c-335">Notice that test cases are automatically run in the application by using a web browser.</span></span>

### <a name="analyze-the-results-of-test-execution"></a><span data-ttu-id="ac81c-336">Analýza výsledků spuštění testu</span><span class="sxs-lookup"><span data-stu-id="ac81c-336">Analyze the results of test execution</span></span>

<span data-ttu-id="ac81c-337">Výsledky testu se ukládají na RSAT.</span><span class="sxs-lookup"><span data-stu-id="ac81c-337">The results of the test execution are stored in RSAT.</span></span> <span data-ttu-id="ac81c-338">Povšimněte si, že byly oba testy předány.</span><span class="sxs-lookup"><span data-stu-id="ac81c-338">Notice that both tests were passed.</span></span>

<span data-ttu-id="ac81c-339">![Testy předané v RSAT](media/GER-RSAT-RSAT-Tests-Passed.png "Snímek obrazovky testů, které byly předány v RSAT")</span><span class="sxs-lookup"><span data-stu-id="ac81c-339">![Tests that passed in RSAT](media/GER-RSAT-RSAT-Tests-Passed.png "Screenshot of tests that passed in RSAT")</span></span>

<span data-ttu-id="ac81c-340">Všimněte si, že výsledky spuštění testu jsou také odesílány do Azure DevOps, aby bylo možné provádět další analýzu.</span><span class="sxs-lookup"><span data-stu-id="ac81c-340">Notice that the results of the test execution are also sent to Azure DevOps so that you can do further analysis.</span></span>

<span data-ttu-id="ac81c-341">![Výsledky spuštění testu v Azure DevOps](media/GER-RSAT-DevOps-Tests-Added.png "Obrazovka výsledků spuštění testu v Azure DevOps")</span><span class="sxs-lookup"><span data-stu-id="ac81c-341">![Results of test execution in Azure DevOps](media/GER-RSAT-DevOps-Tests-Added.png "Screenshot of the results of test execution in Azure DevOps")</span></span>

### <a name="simulate-a-situation-where-tests-fail"></a><span data-ttu-id="ac81c-342">Simulace situace, kdy se testy nedaří</span><span class="sxs-lookup"><span data-stu-id="ac81c-342">Simulate a situation where tests fail</span></span>

<span data-ttu-id="ac81c-343">Tato sada testů musí selhat, pokud alespoň jeden z generovaných výstupů neodpovídá odpovídajícímu směrnému plánu.</span><span class="sxs-lookup"><span data-stu-id="ac81c-343">This test suite must fail when at least one of the generated outputs doesn't match the corresponding baseline.</span></span> <span data-ttu-id="ac81c-344">Chcete-li této situace dosáhnout, můžete použít odvozenou verzi formátu **BACS (UK)**, který bude generovat soubor platby s jiným obsahem než odpovídajícím směrným plánem.</span><span class="sxs-lookup"><span data-stu-id="ac81c-344">To achieve this situation, you can use your derived version of the **BACS (UK)** format that will generate a payment file that has different content than the corresponding baseline.</span></span> <span data-ttu-id="ac81c-345">Chcete-li tuto situaci simulovat, můžete použít stejný formát **BACS (UK)**, ale změnit částku platby na řádku zpracované platby.</span><span class="sxs-lookup"><span data-stu-id="ac81c-345">To simulate this situation, you can use the same **BACS (UK)** format but change the payment amount on the processed payment line.</span></span>

1. <span data-ttu-id="ac81c-346">Otevřete aplikaci a přejděte na **Závazky \> Platby \> Deník plateb**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-346">Open the application and go to **Accounts payable \> Payments \> Payment journal**.</span></span>
2. <span data-ttu-id="ac81c-347">Vybrat **řádky**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-347">Select **Lines**.</span></span>
3. <span data-ttu-id="ac81c-348">Vyberte řádek platby a poté vyberte **stav platby \> Žádný**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-348">Select the payment line, and then select **Payment status \> None**.</span></span>
4. <span data-ttu-id="ac81c-349">V poli **Debet** dáti změňte hodnotu z **1 000,00** na **2 000,00**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-349">In the **Debit** field, change the value from **1,000.00** to **2,000.00**.</span></span>
5. <span data-ttu-id="ac81c-350">Klepnutím na tlačítko **Uložit** uložte změny.</span><span class="sxs-lookup"><span data-stu-id="ac81c-350">Select **Save** to save your changes.</span></span>

### <a name="run-the-tests-in-rsat"></a><span data-ttu-id="ac81c-351">Spuštění testů v RSAT</span><span class="sxs-lookup"><span data-stu-id="ac81c-351">Run the tests in RSAT</span></span>

1. <span data-ttu-id="ac81c-352">V RSAT vyberte načtené testy.</span><span class="sxs-lookup"><span data-stu-id="ac81c-352">In RSAT, select the loaded tests.</span></span>
2. <span data-ttu-id="ac81c-353">Vyberte **Spustit**.</span><span class="sxs-lookup"><span data-stu-id="ac81c-353">Select **Run**.</span></span>

<span data-ttu-id="ac81c-354">Všimněte si, že testovací případy jsou automaticky spuštěny v aplikaci pomocí webového prohlížeče.</span><span class="sxs-lookup"><span data-stu-id="ac81c-354">Notice that test cases are automatically run in the application by using a web browser.</span></span>

### <a name="analyze-the-results-of-test-execution"></a><span data-ttu-id="ac81c-355">Analýza výsledků spuštění testu</span><span class="sxs-lookup"><span data-stu-id="ac81c-355">Analyze the results of test execution</span></span>

<span data-ttu-id="ac81c-356">Výsledky testu se ukládají na RSAT.</span><span class="sxs-lookup"><span data-stu-id="ac81c-356">The results of the test execution are stored in RSAT.</span></span> <span data-ttu-id="ac81c-357">Všimněte si, že druhý test selhal při druhém spuštění.</span><span class="sxs-lookup"><span data-stu-id="ac81c-357">Notice that the second test failed during the second execution.</span></span>

<span data-ttu-id="ac81c-358">![Neúspěšné výsledky testů v RSAT](media/GER-RSAT-RSAT-Tests-Failed.png "Snímek obrazovky neúspěšných výsledků testů v RSAT")</span><span class="sxs-lookup"><span data-stu-id="ac81c-358">![Failed test results in RSAT](media/GER-RSAT-RSAT-Tests-Failed.png "Screenshot of the failed test results in RSAT")</span></span>

<span data-ttu-id="ac81c-359">Všimněte si, že výsledky spuštění testu jsou také odesílány do Azure DevOps, aby bylo možné provádět další analýzu.</span><span class="sxs-lookup"><span data-stu-id="ac81c-359">Notice that the results of the test execution are also sent to Azure DevOps so that you can do further analysis.</span></span>

<span data-ttu-id="ac81c-360">![Neúspěšné výsledky testů v RSAT Azure DevOps](media/GER-RSAT-DevOps-Tests-Failed.png "Snímek obrazovky neúspěšných výsledků testů v Azure DevOps")</span><span class="sxs-lookup"><span data-stu-id="ac81c-360">![Failed test results in Azure DevOps](media/GER-RSAT-DevOps-Tests-Failed.png "Screenshot of the failed test results in Azure DevOps")</span></span>

<span data-ttu-id="ac81c-361">Můžete mít přístup ke stavu každého testu.</span><span class="sxs-lookup"><span data-stu-id="ac81c-361">You can access the status of each test.</span></span> <span data-ttu-id="ac81c-362">K protokolu spuštění můžete také přistupovat, abyste analyzovali důvody selhání.</span><span class="sxs-lookup"><span data-stu-id="ac81c-362">You can also access the execution log so that you analyze the reasons for any failure.</span></span> <span data-ttu-id="ac81c-363">Na následujícím obrázku protokol spuštění ukazuje, že k chybě došlo kvůli rozdílu v obsahu mezi vygenerovaným souborem platby a jeho směrným plánem.</span><span class="sxs-lookup"><span data-stu-id="ac81c-363">In the following illustration, the execution log shows that the failure occurred because of the difference in content between the generated payment file and its baseline.</span></span>

<span data-ttu-id="ac81c-364">![Protokol provádění pro analýzu chyb v Azure DevOps](media/GER-RSAT-DevOps-Tests-Failed-Log.png "Snímek obrazovky protokolu provádění s analýzou chyby v Azure DevOps")</span><span class="sxs-lookup"><span data-stu-id="ac81c-364">![Execution log for analyzing failure in Azure DevOps](media/GER-RSAT-DevOps-Tests-Failed-Log.png "Screenshot of the execution log for analyzing failure in Azure DevOps")</span></span>

<span data-ttu-id="ac81c-365">Proto, jak jste viděli, lze fungování formátu ER vyhodnotit automaticky pomocí RSAT jako testovací platformy a pomocí testovacích případů na základě záznamníku úloh, které používají funkci ER.</span><span class="sxs-lookup"><span data-stu-id="ac81c-365">Therefore, as you've seen, the functioning of any ER format can be evaluated automatically by using RSAT as the testing platform and by using Task recorder-based test cases that use the ER baseline feature.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ac81c-366">Další zdroje</span><span class="sxs-lookup"><span data-stu-id="ac81c-366">Additional resources</span></span>

- [<span data-ttu-id="ac81c-367">Zdroje záznamníku úloh</span><span class="sxs-lookup"><span data-stu-id="ac81c-367">Task recorder resources</span></span>](../user-interface/task-recorder.md)
- [<span data-ttu-id="ac81c-368">Regression Suite Automation Tool</span><span class="sxs-lookup"><span data-stu-id="ac81c-368">Regression suite automation tool</span></span>](https://www.microsoft.com/download/details.aspx?id=57357)
- [<span data-ttu-id="ac81c-369">Vytvoření a automatizace akceptačních testování uživatele</span><span class="sxs-lookup"><span data-stu-id="ac81c-369">Create and automate user acceptance tests</span></span>](../lifecycle-services/using-task-guides-and-bpm-to-create-user-acceptance-tests.md)
- [<span data-ttu-id="ac81c-370">Nasazení a používání prostředí podporujícího průběžné sestavování a automatizace testování</span><span class="sxs-lookup"><span data-stu-id="ac81c-370">Deploy and use an environment that supports continuous build and test automation</span></span>](../perf-test/continuous-build-test-automation.md)
- [<span data-ttu-id="ac81c-371">Sledování výsledků vygenerovaných sestav a jejich porovnání se základními hodnotami</span><span class="sxs-lookup"><span data-stu-id="ac81c-371">Trace generated report results and compare them with baseline values</span></span>](er-trace-reports-compare-baseline.md)
- [<span data-ttu-id="ac81c-372">Elektronické výkaznictví - Upgrade formátu přijetím nové základní verze tohoto formátu</span><span class="sxs-lookup"><span data-stu-id="ac81c-372">ER Upgrade your format by adopting a new, base version of that format</span></span>](tasks/er-upgrade-format.md)
- [<span data-ttu-id="ac81c-373">Import konfigurace ER ze služby Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="ac81c-373">ER Import a configuration from Lifecycle Services</span></span>](tasks/er-import-configuration-lifecycle-services.md)
